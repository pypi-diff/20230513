# Comparing `tmp/wiretap-3.1.2-py3-none-any.whl.zip` & `tmp/wiretap-4.2.0-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 4686 bytes, number of entries: 7
--rw-rw-rw-  2.0 fat      199 b- defN 23-May-08 08:36 wiretap/__init__.py
+Zip file size: 4748 bytes, number of entries: 7
+-rw-rw-rw-  2.0 fat      131 b- defN 23-May-13 15:30 wiretap/__init__.py
 -rw-rw-rw-  2.0 fat      620 b- defN 23-Feb-08 09:16 wiretap/layers.py
--rw-rw-rw-  2.0 fat    10833 b- defN 23-May-08 09:53 wiretap/wiretap.py
--rw-rw-rw-  2.0 fat      244 b- defN 23-May-08 09:55 wiretap-3.1.2.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-May-08 09:55 wiretap-3.1.2.dist-info/WHEEL
--rw-rw-rw-  2.0 fat        8 b- defN 23-May-08 09:55 wiretap-3.1.2.dist-info/top_level.txt
--rw-rw-r--  2.0 fat      520 b- defN 23-May-08 09:55 wiretap-3.1.2.dist-info/RECORD
-7 files, 12516 bytes uncompressed, 3768 bytes compressed:  69.9%
+-rw-rw-rw-  2.0 fat    12190 b- defN 23-May-13 15:37 wiretap/wiretap.py
+-rw-rw-rw-  2.0 fat      244 b- defN 23-May-13 15:49 wiretap-4.2.0.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-May-13 15:49 wiretap-4.2.0.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat        8 b- defN 23-May-13 15:49 wiretap-4.2.0.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      520 b- defN 23-May-13 15:49 wiretap-4.2.0.dist-info/RECORD
+7 files, 13805 bytes uncompressed, 3830 bytes compressed:  72.3%
```

## zipnote {}

```diff
@@ -3,20 +3,20 @@
 
 Filename: wiretap/layers.py
 Comment: 
 
 Filename: wiretap/wiretap.py
 Comment: 
 
-Filename: wiretap-3.1.2.dist-info/METADATA
+Filename: wiretap-4.2.0.dist-info/METADATA
 Comment: 
 
-Filename: wiretap-3.1.2.dist-info/WHEEL
+Filename: wiretap-4.2.0.dist-info/WHEEL
 Comment: 
 
-Filename: wiretap-3.1.2.dist-info/top_level.txt
+Filename: wiretap-4.2.0.dist-info/top_level.txt
 Comment: 
 
-Filename: wiretap-3.1.2.dist-info/RECORD
+Filename: wiretap-4.2.0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## wiretap/__init__.py

```diff
@@ -1,11 +1,8 @@
 from .wiretap import (
     Logger,
-    OnStarted,
-    OnCompleted,
-    FormatStartDetails,
-    FormatResultDetails,
     SerializeDetails,
     MultiFormatter,
     telemetry,
-    collect,
+    telemetry_scope,
+    raw
 )
```

## wiretap/wiretap.py

```diff
@@ -1,23 +1,31 @@
 import asyncio
 import contextlib
+import dataclasses
 import enum
 import functools
 import inspect
 import json
 import logging
 import sys
 import uuid
-import collections.abc
-import abc
 from collections.abc import Generator
 from contextvars import ContextVar
 from datetime import datetime, date
 from timeit import default_timer as timer
-from typing import Dict, Callable, Any, Protocol, Optional, Iterator, TypeVar
+from typing import Dict, Callable, Any, Protocol, Optional, Iterator, TypeVar, TypeAlias
+
+FormatOptions: TypeAlias = str | Callable[[Any], Any]
+TValue = TypeVar("TValue")
+NO_DETAILS: dict[str, Any] = {}
+
+DEFAULT_FORMATS: Dict[str, str] = {
+    "classic": "{asctime}.{msecs:.0f} | {levelname} | {module}.{funcName} | {message}",
+    "wiretap": "{asctime}.{msecs:.0f} {indent} {levelname} | {module}.{funcName} | {status} | {elapsed:.3f}s | {message} | {details} | node://{parent}/{node} | {attachment}",
+}
 
 _scope: ContextVar[Optional["Logger"]] = ContextVar("_scope", default=None)
 
 
 class SerializeDetails(Protocol):
     def __call__(self, value: Optional[Dict[str, Any]]) -> str | None: ...
 
@@ -29,114 +37,77 @@
 
 class _JsonDateTimeEncoder(json.JSONEncoder):
     def default(self, o: Any) -> Any:
         if isinstance(o, (date, datetime)):
             return o.isoformat()
 
 
-DEFAULT_FORMATS: Dict[str, str] = {
-    "classic": "{asctime}.{msecs:.0f} | {levelname} | {module}.{funcName} | {message}",
-    "wiretap": "{asctime}.{msecs:.0f} [{indent}] {levelname} | {module}.{funcName} | {status} | {elapsed} | {details} | [{parent}/{node}] | {attachment}",
-}
-
-
 class MultiFormatter(logging.Formatter):
-    formats: Dict[str, str] = DEFAULT_FORMATS
+    formats: Dict[str, str] = {}
     indent: str = "."
     values: Optional[Dict[str, Any]] = None
     serialize_details: SerializeDetails = SerializeDetailsToJson()
 
     def format(self, record: logging.LogRecord) -> str:
         record.levelname = record.levelname.lower()
-        record.values = self.values or {}
+        record.__dict__.update(self.values or {})  # Unpack values.
 
         if hasattr(record, "details") and isinstance(record.details, dict):
-            record.indent = self.indent * record.details["depth"]
+            record.indent = self.indent * record.__dict__.pop("_depth", 1)
             record.details = self.serialize_details(record.details)
 
-        self._style._fmt = self.formats["classic"]
-
         if hasattr(record, "status"):
-            self._style._fmt = self.formats["wiretap"]
-
-        if hasattr(record, "format"):
-            self._style._fmt = record.format
+            self._style._fmt = self.formats["wiretap"] if "wiretap" in self.formats else DEFAULT_FORMATS["wiretap"]
+        else:
+            self._style._fmt = self.formats["classic"] if "classin" in self.formats else DEFAULT_FORMATS["classic"]
 
-        self.formats = DEFAULT_FORMATS | self.formats
         return super().format(record)
 
 
-class OnStarted(Protocol):
-    """Allows you to create details from function arguments."""
-
-    def __call__(self, params: Dict[str, Any]) -> Dict[str, Any]: ...
-
+def raw(value: TValue) -> TValue:
+    return value
 
-class OnCompleted(Protocol):
-    """Allows you to create details from function result."""
 
-    def __call__(self, result: Optional[Any]) -> Dict[str, Any]: ...
-
-
-class EmptyOnStarted:
-    def __call__(self, params: Dict[str, Any]) -> Dict[str, Any]:
-        return {}
-
-
-class EmptyOnCompleted(OnCompleted):
-    def __call__(self, result: Optional[Any]) -> Dict[str, Any]:
-        return {}
-
-
-def _format_detail(value: Any, formats: Optional[str | Callable[[Any], Any]]) -> Optional[Any]:
+def multi_format(value: Any, value_format: FormatOptions) -> Optional[Any]:
     if not value:
         return None
 
-    if isinstance(value, enum.Enum):
-        value = value.value
+    if isinstance(value_format, str):
+        return format(value, value_format)
 
-    if not formats:
-        return value
+    if callable(value_format):
+        return value_format(value)
 
-    if isinstance(formats, str):
-        return format(value, formats)
+    raise ValueError(f"Unsupported details format: {type(value_format)}. Expected: {FormatOptions}.")
 
-    if callable(formats):
-        return formats(value)
 
-    raise ValueError(f"Details format supports only [str | Callable[[Any], Any] not {type(formats)}")
-
-
-class FormatStartDetails(OnStarted):
-    def __init__(self, **details):
-        self.details = details
-
-    def __call__(self, params: Dict[str, Any]) -> Dict[str, Any]:
-        return {key: _format_detail(params.get(key, None), self.details[key]) for key in self.details}
+def create_args_details(args: dict[str, Any], args_format: FormatOptions | dict[str, FormatOptions]) -> dict[str, Any]:
+    if args_format == NO_DETAILS:
+        return {}
 
+    if not args:
+        return {"args": None}
 
-class FormatResultDetails(OnCompleted):
-    def __init__(self, formats: Optional[str | Callable[[Any], Any]] = None, **details):
-        self.formats = formats
-        self.details = details
+    if isinstance(args_format, dict):
+        return {"args": {key: multi_format(args.get(key, None), args_format[key]) for key in args_format}}
 
-    def __call__(self, value: Optional[Any]) -> Dict[str, Any]:
-        if not value:
-            return dict(result=None)
+    return {"args": {key: multi_format(args.get(key, None), args_format) for key in args}}
 
-        if self.formats:
-            return dict(result=_format_detail(value, self.formats))
 
-        if self.details:
-            return {key: _format_detail(value, self.details[key]) for key in self.details}
+def create_result_details(result: Any | None, result_format: FormatOptions | dict[str, FormatOptions]) -> dict[str, Any]:
+    if result_format == NO_DETAILS:
+        return {}
 
-        return dict(result=value)
+    if not result:
+        return {"result": None}
 
+    if isinstance(result_format, dict):
+        return {"result": {key: multi_format(result, result_format[key]) for key in result_format}}
 
-TResult = TypeVar("TResult")
+    return {"result": multi_format(result, result_format)}
 
 
 class Logger:
 
     def __init__(self, module: Optional[str], scope: str, parent: Optional["Logger"] = None):
         self.id = uuid.uuid4()
         self.module = module
@@ -145,88 +116,146 @@
         self.depth = sum(1 for _ in self)
         self._start = timer()
         self._finalized = False
         self._logger = logging.getLogger(f"{module}.{scope}")
 
     @property
     def elapsed(self) -> float:
-        return round(timer() - self._start, 3)
+        return timer() - self._start
 
-    def started(self, **details):
+    def started(
+            self,
+            message: Optional[str] = None,
+            details: Optional[dict[str, Any]] = None,
+            attachment: Optional[Any] = None
+    ):
         self._logger.setLevel(logging.INFO)
         self._start = timer()
-        self._log(**details)
+        self._log(message, details, attachment)
 
-    def running(self, **details):
+    def running(
+            self,
+            message: Optional[str] = None,
+            details: Optional[dict[str, Any]] = None,
+            attachment: Optional[Any] = None
+    ):
         self._logger.setLevel(logging.DEBUG)
-        self._log(**details)
+        self._log(message, details, attachment)
 
-    def completed(self, result: Optional[TResult] = None, details_factory: OnCompleted = EmptyOnCompleted(), **details) -> Optional[TResult]:
+    def completed(
+            self,
+            message: Optional[str] = None,
+            details: Optional[dict[str, Any]] = None,
+            attachment: Optional[Any] = None,
+            result: Optional[TValue] = None,
+            result_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    ) -> Optional[TValue]:
         self._logger.setLevel(logging.INFO)
-        self._log(**(details_factory(result) | details))
+        self._log(message, details, attachment, result, result_format)
         return result
 
-    def canceled(self, result: Optional[TResult] = None, details_factory: OnCompleted = EmptyOnCompleted(), **details) -> Optional[TResult]:
+    def canceled(
+            self,
+            message: Optional[str] = None,
+            details: Optional[dict[str, Any]] = None,
+            attachment: Optional[Any] = None,
+            result: Optional[TValue] = None,
+            result_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    ) -> Optional[TValue]:
         self._logger.setLevel(logging.WARNING)
-        self._log(**(details_factory(result) | details))
+        self._log(message, details, attachment, result, result_format)
         return result
 
-    def faulted(self, result: Optional[TResult] = None, details_factory: OnCompleted = EmptyOnCompleted(), **details) -> Optional[TResult]:
+    def faulted(
+            self,
+            message: Optional[str] = None,
+            details: Optional[dict[str, Any]] = None,
+            attachment: Optional[Any] = None,
+            result: Optional[TValue] = None,
+            result_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    ) -> Optional[TValue]:
         self._logger.setLevel(logging.ERROR)
-        self._log(**(details_factory(result) | details))
+        self._log(message, details, attachment, result, result_format)
         return result
 
-    def _log(self, **kwargs):
+    def _log(
+            self,
+            message: Optional[str],
+            details: Optional[dict[str, Any]],
+            attachment: Optional[Any],
+            result: Optional[TValue] = None,
+            result_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    ):
         if self._finalized:
             return
 
+        details = (details or {}) | create_result_details(result, result_format)
+
         status = inspect.stack()[1][3]
         with _use_custom_log_record_factory(
                 _set_exc_text,
                 functools.partial(_set_module_name, name=self.module),
                 functools.partial(_set_func_name, name=self.scope),
-                functools.partial(_set_attachment, value=kwargs.pop("attachment", None)),
+                functools.partial(_set_attachment, value=attachment),
         ):
-            exc_info = all(sys.exc_info()) and status in [self.faulted.__name__]  # Dump the exception or in case of a fault.
-            self._logger.log(level=self._logger.level, msg=None, exc_info=exc_info, extra={
+            exc_info = all(sys.exc_info()) and status in [self.faulted.__name__]  # Dump the exception only when faulted.
+            self._logger.log(level=self._logger.level, msg=message, exc_info=exc_info, extra={
                 "parent": self.parent.id if self.parent else None,
                 "node": self.id,
                 "status": status,
                 "elapsed": self.elapsed,
-                "details": kwargs | {"depth": self.depth}
+                "details": details or NO_DETAILS,
+                "_depth": self.depth
             })
 
         self._finalized = status in [self.completed.__name__, self.canceled.__name__, self.faulted.__name__]
 
     def __iter__(self):
         current = self
         while current:
             yield current
             current = current.parent
 
 
 @contextlib.contextmanager
-def collect(module: Optional[str], name: str, **kwargs) -> Iterator[Logger]:
+def telemetry_scope(
+        module: Optional[str],
+        name: str,
+        message: Optional[str] = None,
+        details: Optional[dict[str, Any]] = None,
+        attachment: Optional[Any] = None
+) -> Iterator[Logger]:
     """Begins a new telemetry scope."""
     logger = Logger(module, name, _scope.get())
     token = _scope.set(logger)
     try:
-        logger.started(**kwargs)
+        logger.started(message, details, attachment)
         yield logger
-        logger.completed(test="blub!")
+        logger.completed()
     except:  # noqa
         logger.faulted()
         raise
     finally:
         _scope.reset(token)
 
 
-def telemetry(on_started: OnStarted = EmptyOnStarted(), on_completed: OnCompleted = EmptyOnCompleted(), attachment: Optional[Any] = None):
+def telemetry(
+        include_args: bool | FormatOptions | dict[str, FormatOptions] = False,
+        include_result: bool | FormatOptions | dict[str, FormatOptions] = False
+):
     """Provides telemetry for the decorated function."""
 
+    args_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    if include_args:
+        args_format = raw if isinstance(include_args, bool) else include_args
+
+    result_format: FormatOptions | dict[str, FormatOptions] = NO_DETAILS
+    if include_result:
+        result_format = raw if isinstance(include_result, bool) else include_result
+
     def factory(decoratee):
         module = inspect.getmodule(decoratee)
         module_name = module.__name__ if module else None
         scope_name = decoratee.__name__
 
         def inject_logger(logger: Logger, d: Dict):
             """Injects Logger if required."""
@@ -239,32 +268,31 @@
             arg_pairs = zip(inspect.getfullargspec(decoratee).args, range(len(decoratee_args)))
             # Turn arg_pairs into a dictionary and combine it with decoratee_kwargs.
             return {t[0]: decoratee_args[t[1]] for t in arg_pairs} | decoratee_kwargs
 
         if asyncio.iscoroutinefunction(decoratee):
             @functools.wraps(decoratee)
             async def decorator(*decoratee_args, **decoratee_kwargs):
-                start_details = on_started(params(*decoratee_args, **decoratee_kwargs)) | dict(attachment=attachment)
-                with collect(module_name, scope_name, **start_details) as scope:
+                details = create_args_details(params(*decoratee_args, **decoratee_kwargs), args_format)
+                with telemetry_scope(module_name, scope_name, details=details) as scope:
                     inject_logger(scope, decoratee_kwargs)
-                    scope.started(**(on_started(params(*decoratee_args, **decoratee_kwargs)) or {}))
                     result = await decoratee(*decoratee_args, **decoratee_kwargs)
-                    return scope.completed(result, on_completed)
+                    return scope.completed(result=result, result_format=result_format)
 
             decorator.__signature__ = inspect.signature(decoratee)
             return decorator
 
         else:
             @functools.wraps(decoratee)
             def decorator(*decoratee_args, **decoratee_kwargs):
-                start_details = on_started(params(*decoratee_args, **decoratee_kwargs)) | dict(attachment=attachment)
-                with collect(module_name, scope_name, **start_details) as scope:
+                details = create_args_details(params(*decoratee_args, **decoratee_kwargs), args_format)
+                with telemetry_scope(module_name, scope_name, details=details) as scope:
                     inject_logger(scope, decoratee_kwargs)
                     result = decoratee(*decoratee_args, **decoratee_kwargs)
-                    return scope.completed(result, on_completed)
+                    return scope.completed(result=result, result_format=result_format)
 
             decorator.__signature__ = inspect.signature(decoratee)
             return decorator
 
     return factory
```

