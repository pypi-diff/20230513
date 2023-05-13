# Comparing `tmp/orjson_ddb-0.2.0-cp39-none-win_amd64.whl.zip` & `tmp/orjson_ddb-0.2.1-cp39-cp39-manylinux_2_28_x86_64.whl.zip`

## zipinfo {}

```diff
@@ -1,12 +1,12 @@
-Zip file size: 208531 bytes, number of entries: 10
--rw-r--r--  4.6 unx     9936 b- defN 22-Aug-29 07:10 orjson_ddb-0.2.0.dist-info/METADATA
--rw-r--r--  4.6 unx       95 b- defN 22-Aug-29 07:10 orjson_ddb-0.2.0.dist-info/WHEEL
--rw-r--r--  4.6 unx    11048 b- defN 22-Aug-29 07:10 orjson_ddb-0.2.0.dist-info/license_files/LICENSE-APACHE
--rw-r--r--  4.6 unx     1046 b- defN 22-Aug-29 07:10 orjson_ddb-0.2.0.dist-info/license_files/LICENSE-MIT
--rw-r--r--  4.6 unx      483 b- defN 22-Aug-29 07:10 orjson_ddb/boto_integration.py
--rw-r--r--  4.6 unx      734 b- defN 22-Aug-29 07:10 orjson_ddb/orjson_ddb.pyi
--rw-r--r--  4.6 unx        0 b- defN 22-Aug-29 07:10 orjson_ddb/py.typed
--rw-r--r--  4.6 unx      494 b- defN 22-Aug-29 07:10 orjson_ddb/__init__.py
--rwxr-xr-x  4.6 unx   397824 b- defN 22-Aug-29 07:10 orjson_ddb/orjson_ddb.cp39-win_amd64.pyd
--rw-r--r--  4.6 unx      854 b- defN 22-Aug-29 07:10 orjson_ddb-0.2.0.dist-info/RECORD
-10 files, 422514 bytes uncompressed, 207063 bytes compressed:  51.0%
+Zip file size: 157129 bytes, number of entries: 10
+-rw-r--r--  4.6 unx     9743 b- defN 23-May-13 11:04 orjson_ddb-0.2.1.dist-info/METADATA
+-rw-r--r--  4.6 unx      107 b- defN 23-May-13 11:04 orjson_ddb-0.2.1.dist-info/WHEEL
+-rw-r--r--  4.6 unx    10847 b- defN 23-May-13 11:04 orjson_ddb-0.2.1.dist-info/license_files/LICENSE-APACHE
+-rw-r--r--  4.6 unx     1023 b- defN 23-May-13 11:04 orjson_ddb-0.2.1.dist-info/license_files/LICENSE-MIT
+-rw-r--r--  4.6 unx        0 b- defN 23-May-13 11:04 orjson_ddb/py.typed
+-rw-r--r--  4.6 unx      463 b- defN 23-May-13 11:04 orjson_ddb/boto_integration.py
+-rw-r--r--  4.6 unx      705 b- defN 23-May-13 11:04 orjson_ddb/orjson_ddb.pyi
+-rw-r--r--  4.6 unx      476 b- defN 23-May-13 11:04 orjson_ddb/__init__.py
+-rwxr-xr-x  4.6 unx   300776 b- defN 23-May-13 11:04 orjson_ddb/orjson_ddb.cpython-39-x86_64-linux-gnu.so
+-rw-r--r--  4.6 unx      867 b- defN 23-May-13 11:04 orjson_ddb-0.2.1.dist-info/RECORD
+10 files, 325007 bytes uncompressed, 155637 bytes compressed:  52.1%
```

## zipnote {}

```diff
@@ -1,31 +1,31 @@
-Filename: orjson_ddb-0.2.0.dist-info/METADATA
+Filename: orjson_ddb-0.2.1.dist-info/METADATA
 Comment: 
 
-Filename: orjson_ddb-0.2.0.dist-info/WHEEL
+Filename: orjson_ddb-0.2.1.dist-info/WHEEL
 Comment: 
 
-Filename: orjson_ddb-0.2.0.dist-info/license_files/LICENSE-APACHE
+Filename: orjson_ddb-0.2.1.dist-info/license_files/LICENSE-APACHE
 Comment: 
 
-Filename: orjson_ddb-0.2.0.dist-info/license_files/LICENSE-MIT
+Filename: orjson_ddb-0.2.1.dist-info/license_files/LICENSE-MIT
 Comment: 
 
-Filename: orjson_ddb/boto_integration.py
+Filename: orjson_ddb/py.typed
 Comment: 
 
-Filename: orjson_ddb/orjson_ddb.pyi
+Filename: orjson_ddb/boto_integration.py
 Comment: 
 
-Filename: orjson_ddb/py.typed
+Filename: orjson_ddb/orjson_ddb.pyi
 Comment: 
 
 Filename: orjson_ddb/__init__.py
 Comment: 
 
-Filename: orjson_ddb/orjson_ddb.cp39-win_amd64.pyd
+Filename: orjson_ddb/orjson_ddb.cpython-39-x86_64-linux-gnu.so
 Comment: 
 
-Filename: orjson_ddb-0.2.0.dist-info/RECORD
+Filename: orjson_ddb-0.2.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## orjson_ddb/boto_integration.py

 * *Ordering differences only*

```diff
@@ -1,20 +1,20 @@
-import contextlib
-
-from botocore.parsers import PROTOCOL_PARSERS
-from .orjson_ddb import loads
-
-
-@contextlib.contextmanager
-def ddb_json_parser():
-    # Start the timer
-    _parser = PROTOCOL_PARSERS.get("json")
-    old_parser = getattr(_parser, "_handle_json_body")
-
-    def new_parser(self, raw_body, shape):
-        return loads(raw_body)
-
-    setattr(_parser, "_handle_json_body", new_parser)
-
-    yield
-
-    setattr(_parser, "_handle_json_body", old_parser)
+import contextlib
+
+from botocore.parsers import PROTOCOL_PARSERS
+from .orjson_ddb import loads
+
+
+@contextlib.contextmanager
+def ddb_json_parser():
+    # Start the timer
+    _parser = PROTOCOL_PARSERS.get("json")
+    old_parser = getattr(_parser, "_handle_json_body")
+
+    def new_parser(self, raw_body, shape):
+        return loads(raw_body)
+
+    setattr(_parser, "_handle_json_body", new_parser)
+
+    yield
+
+    setattr(_parser, "_handle_json_body", old_parser)
```

## orjson_ddb/orjson_ddb.pyi

 * *Ordering differences only*

```diff
@@ -1,29 +1,29 @@
-import json
-from typing import Any, Callable, Optional, Union
-
-__version__: str
-
-def dumps(
-    __obj: Any,
-    default: Optional[Callable[[Any], Any]] = ...,
-    option: Optional[int] = ...,
-) -> bytes: ...
-def loads(__obj: Union[bytes, bytearray, memoryview, str]) -> Any: ...
-
-class JSONDecodeError(json.JSONDecodeError): ...
-class JSONEncodeError(TypeError): ...
-
-OPT_APPEND_NEWLINE: int
-OPT_INDENT_2: int
-OPT_NAIVE_UTC: int
-OPT_NON_STR_KEYS: int
-OPT_OMIT_MICROSECONDS: int
-OPT_PASSTHROUGH_DATACLASS: int
-OPT_PASSTHROUGH_DATETIME: int
-OPT_PASSTHROUGH_SUBCLASS: int
-OPT_SERIALIZE_DATACLASS: int
-OPT_SERIALIZE_NUMPY: int
-OPT_SERIALIZE_UUID: int
-OPT_SORT_KEYS: int
-OPT_STRICT_INTEGER: int
-OPT_UTC_Z: int
+import json
+from typing import Any, Callable, Optional, Union
+
+__version__: str
+
+def dumps(
+    __obj: Any,
+    default: Optional[Callable[[Any], Any]] = ...,
+    option: Optional[int] = ...,
+) -> bytes: ...
+def loads(__obj: Union[bytes, bytearray, memoryview, str]) -> Any: ...
+
+class JSONDecodeError(json.JSONDecodeError): ...
+class JSONEncodeError(TypeError): ...
+
+OPT_APPEND_NEWLINE: int
+OPT_INDENT_2: int
+OPT_NAIVE_UTC: int
+OPT_NON_STR_KEYS: int
+OPT_OMIT_MICROSECONDS: int
+OPT_PASSTHROUGH_DATACLASS: int
+OPT_PASSTHROUGH_DATETIME: int
+OPT_PASSTHROUGH_SUBCLASS: int
+OPT_SERIALIZE_DATACLASS: int
+OPT_SERIALIZE_NUMPY: int
+OPT_SERIALIZE_UUID: int
+OPT_SORT_KEYS: int
+OPT_STRICT_INTEGER: int
+OPT_UTC_Z: int
```

## orjson_ddb/__init__.py

 * *Ordering differences only*

```diff
@@ -1,18 +1,18 @@
-from .orjson_ddb import (
-    __version__, dumps, loads, JSONDecodeError, JSONEncodeError,
-    OPT_APPEND_NEWLINE,
-    OPT_INDENT_2,
-    OPT_NAIVE_UTC,
-    OPT_NON_STR_KEYS,
-    OPT_OMIT_MICROSECONDS,
-    OPT_PASSTHROUGH_DATACLASS,
-    OPT_PASSTHROUGH_DATETIME,
-    OPT_PASSTHROUGH_SUBCLASS,
-    OPT_SERIALIZE_DATACLASS,
-    OPT_SERIALIZE_NUMPY,
-    OPT_SERIALIZE_UUID,
-    OPT_SORT_KEYS,
-    OPT_STRICT_INTEGER,
-    OPT_UTC_Z,
-)
-from .boto_integration import ddb_json_parser
+from .orjson_ddb import (
+    __version__, dumps, loads, JSONDecodeError, JSONEncodeError,
+    OPT_APPEND_NEWLINE,
+    OPT_INDENT_2,
+    OPT_NAIVE_UTC,
+    OPT_NON_STR_KEYS,
+    OPT_OMIT_MICROSECONDS,
+    OPT_PASSTHROUGH_DATACLASS,
+    OPT_PASSTHROUGH_DATETIME,
+    OPT_PASSTHROUGH_SUBCLASS,
+    OPT_SERIALIZE_DATACLASS,
+    OPT_SERIALIZE_NUMPY,
+    OPT_SERIALIZE_UUID,
+    OPT_SORT_KEYS,
+    OPT_STRICT_INTEGER,
+    OPT_UTC_Z,
+)
+from .boto_integration import ddb_json_parser
```

## Comparing `orjson_ddb-0.2.0.dist-info/METADATA` & `orjson_ddb-0.2.1.dist-info/METADATA`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: orjson_ddb
-Version: 0.2.0
+Version: 0.2.1
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX :: Linux
@@ -26,201 +26,201 @@
 Author: Mattia Fantoni <mattia.fantoni@gmail.com>
 Author-email: Mattia Fantoni <mattia.fantoni@gmail.com>
 License: Apache-2.0 OR MIT
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
 Project-URL: Source Code, https://github.com/MattFanto/orjson-ddb
 
-# orjson-ddb
-
-orjson-ddb is a fast DynamoDB native JSON library for Python. 
-It is a fork/reboot of [orjson](https://github.com/ijl/orjson) (from which it inherits the [fast performance](https://github.com/ijl/orjson#performance)) 
-adapted to serialize and deserialize DDB native JSON format in Python.
-Compared to [boto3](https://github.com/boto/boto3) DynamoDB [TypeDeserializer](https://github.com/boto/boto3/blob/1.24.61/boto3/dynamodb/types.py#L82), 
-it deserializes DynamoDB response 10x faster and deserialize float numbers (e.g. `{"N": "0.13"}`) to float instead of Decimal.
-
-orjson-ddb supports CPython 3.7, 3.8, 3.9, 3.10, and 3.11. It distributes x86_64/amd64,
-aarch64/armv8, and arm7 wheels for Linux, amd64 and aarch64 wheels for macOS,
-and amd64 wheels for Windows. orjson-ddb does not support PyPy. Releases
-follow semantic versioning and serializing a new object type
-without an opt-in flag is considered a breaking change.
-
-The repository and issue tracker is [github.com/MattFanto/orjson-ddb](https://github.com/MattFanto/orjson-ddb), 
-and patches may be submitted there. There is a [CHANGELOG](https://github.com/MattFanto/orjson-ddb/blob/master/CHANGELOG.md)
-available in the repository.
-
-1. [Usage](https://github.com/MattFanto/orjson-ddb#usage)
-    1. [Install](https://github.com/MattFanto/orjson-ddb#install)
-    2. [Quickstart](https://github.com/MattFanto/orjson-ddb#quickstart)
-    3. [Deserialize](https://github.com/MattFanto/orjson-ddb#deserialize)
-    4. [Serialize](https://github.com/MattFanto/orjson-ddb#serialize)
-2. [Testing](https://github.com/MattFanto/orjson-ddb#testing)
-3. [Performance](https://github.com/MattFanto/orjson-ddb#performance)
-    1. [Latency](https://github.com/MattFanto/orjson-ddb#latency)
-    2. [Memory](https://github.com/MattFanto/orjson-ddb#memory)
-    3. [Reproducing](https://github.com/MattFanto/orjson-ddb#reproducing)
-4. [Questions](https://github.com/MattFanto/orjson-ddb#questions)
-5. [Packaging](https://github.com/MattFanto/orjson-ddb#packaging)
-6. [License](https://github.com/MattFanto/orjson-ddb#license)
-
-## Usage
-
-### Install
-
-To install a wheel from PyPI:
-
-```sh
-pip install --upgrade "pip>=20.3" # manylinux_x_y, universal2 wheel support
-pip install --upgrade orjson-ddb
-```
-
-To build a wheel, see [packaging](https://github.com/MattFanto/orjson-ddb#packaging).
-
-### Deserialize
-
-This library exposes a function `loads` which can deserializer DynamoDB response into a Python dictionary.
-This can be used to parse the API response from DynamoDB, as an example if you are using the REST API:
-```python
-import requests
-import orjson_ddb
-
-response = requests.post("https://dynamodb.us-east-1.amazonaws.com/", data={
-   "TableName": "some_table", 
-   "Key": {"pk": {"S": "pk1"}, "sk": {"S": "sk1"}}
-}, headers={
-   # some headers
-})
-data = orjson_ddb.loads(response.content)
-```
-The same results can be achieved when using boto3 via a context manager provided by the library:
-```python
-import boto3
-from orjson_ddb import ddb_json_parser
-
-
-dynamodb_client = boto3.client("dynamodb", region_name="us-east-1")
-with ddb_json_parser():
-   resp = dynamodb_client.get_item(
-      TableName="some_table",
-      Key={"pk": {"S": "pk1"}, "sk": {"S": "sk1"}}
-   )
-print(resp["Items"])
-# {'sk': 'sk1', 'pk': 'pk1', 'data': {'some_number': 0.123, 'some_string': 'hello'}}
-```
-This context manager tells boto3 to use `orjson_ddb.loads` to deserialize the DynamoDB response.
-The output dictionary doesn't contain any reference to the DynamoDB Native format and the result is the same of
-what you would get with `boto3.resource('dynamodb').Table('some_table').get_item(Key={"pk": "pk1", "sk": "sk1"})["Item"]`
-except for "N" type being translated directly to int or float instead of Decimal.
-
-N.B. Unfortunately at the moment it is not possible to use this library with `boto3.resource`.
-
-
-### Serialize
-
-Serialization of python dictionary to DynamoDB Native JSON format is not available yet.
-
-
-## Performance
-
-Deserialization performance of orjson-ddb is better than
-boto3, dynamodb-json-util. The benchmarks are done on
-fixtures of real data converted to DynamoDB native format:
-
-* twitter.json, 631.5KiB, results of a search on Twitter for "一", containing
-CJK strings, dictionaries of strings and arrays of dictionaries, indented.
-
-* github.json, 55.8KiB, a GitHub activity feed, containing dictionaries of
-strings and arrays of dictionaries, not indented.
-
-* citm_catalog.json, 1.7MiB, concert data, containing nested dictionaries of
-strings and arrays of integers, indented.
-
-* canada.json, 2.2MiB, coordinates of the Canadian border in GeoJSON
-format, containing floats and arrays, indented.
-
-### Latency
-
-#### twitter.json deserialization
-
-| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
-|--------------------|---------------------------------|-------------------------|----------------------|
-| orjson-ddb         |                            2.17 |                   459.7 |                 1    |
-| boto3-json         |                           18.61 |                    54.1 |                 8.57 |
-| dynamodb-json-util |                           54.13 |                    18.4 |                24.92 |
-
-#### citm_catalog.json deserialization
-
-| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
-|--------------------|---------------------------------|-------------------------|----------------------|
-| orjson-ddb         |                            4.43 |                   240.3 |                 1    |
-| boto3-json         |                           53.3  |                    18.6 |                12.03 |
-| dynamodb-json-util |                           57.27 |                    17.5 |                12.93 |
-
-#### canada.json deserialization
-
-| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
-|--------------------|---------------------------------|-------------------------|----------------------|
-| orjson-ddb         |                           19.22 |                    52   |                 1    |
-| boto3-json         |                          221.83 |                     4.5 |                11.54 |
-| dynamodb-json-util |                          244.14 |                     4.1 |                12.7  |
-
-
-### Reproducing
-
-The above was measured using Python 3.9.13 on Linux (amd64) with
-orjson-ddb 0.1.1, boto3==1.21.27, dynamodb-json==1.3
-
-The latency results can be reproduced using the `pybench` and `graph`
-scripts.
-
-## Questions
-
-### Why can't I install it from PyPI?
-
-Probably `pip` needs to be upgraded to version 20.3 or later to support
-the latest manylinux_x_y or universal2 wheel formats.
-
-### "Cargo, the Rust package manager, is not installed or is not on PATH."
-
-This happens when there are no binary wheels (like manylinux) for your
-platform on PyPI. You can install [Rust](https://www.rust-lang.org/) through
-`rustup` or a package manager and then it will compile.
-
-### Will it support PyPy?
-
-Probably not.
-
-## Packaging
-
-To package orjson-ddb requires at least [Rust](https://www.rust-lang.org/) 1.57
-and the [maturin](https://github.com/PyO3/maturin) build tool. The recommended
-build command is:
-
-```sh
-maturin build --release --strip
-```
-
-It benefits from also having a C build environment to compile a faster
-deserialization backend. See this project's `manylinux_2_28` builds for an
-example using clang and LTO.
-
-The project's own CI tests against `nightly-2022-07-26` and stable 1.54. It
-is prudent to pin the nightly version because that channel can introduce
-breaking changes.
-
-orjson-ddb is tested for amd64, aarch64, and arm7 on Linux. It is tested for
-amd64 on macOS and cross-compiles for aarch64. For Windows it is tested on
-amd64.
-
-There are no runtime dependencies other than libc.
-
-Tests are included in the source distribution on PyPI. The
-requirements to run the tests are specified in `test/requirements.txt`. The
-tests should be run as part of the build. It can be run with
-`pytest -q test`.
-
-## License
-
-orjson was written by ijl <ijl@mailbox.org>, copyright 2018 - 2021, licensed under both the Apache 2 and MIT licenses.
-
-orjson-ddb was forked from orjson and is maintained by Mattia Fantoni <mattia.fantoni@gmail.com>, licensed same as orjson.
+# orjson-ddb
+
+orjson-ddb is a fast DynamoDB native JSON library for Python. 
+It is a fork/reboot of [orjson](https://github.com/ijl/orjson) (from which it inherits the [fast performance](https://github.com/ijl/orjson#performance)) 
+adapted to serialize and deserialize DDB native JSON format in Python.
+Compared to [boto3](https://github.com/boto/boto3) DynamoDB [TypeDeserializer](https://github.com/boto/boto3/blob/1.24.61/boto3/dynamodb/types.py#L82), 
+it deserializes DynamoDB response 10x faster and deserialize float numbers (e.g. `{"N": "0.13"}`) to float instead of Decimal.
+
+orjson-ddb supports CPython 3.7, 3.8, 3.9, 3.10, and 3.11. It distributes x86_64/amd64,
+aarch64/armv8, and arm7 wheels for Linux, amd64 and aarch64 wheels for macOS,
+and amd64 wheels for Windows. orjson-ddb does not support PyPy. Releases
+follow semantic versioning and serializing a new object type
+without an opt-in flag is considered a breaking change.
+
+The repository and issue tracker is [github.com/MattFanto/orjson-ddb](https://github.com/MattFanto/orjson-ddb), 
+and patches may be submitted there. There is a [CHANGELOG](https://github.com/MattFanto/orjson-ddb/blob/master/CHANGELOG.md)
+available in the repository.
+
+1. [Usage](https://github.com/MattFanto/orjson-ddb#usage)
+    1. [Install](https://github.com/MattFanto/orjson-ddb#install)
+    2. [Quickstart](https://github.com/MattFanto/orjson-ddb#quickstart)
+    3. [Deserialize](https://github.com/MattFanto/orjson-ddb#deserialize)
+    4. [Serialize](https://github.com/MattFanto/orjson-ddb#serialize)
+2. [Testing](https://github.com/MattFanto/orjson-ddb#testing)
+3. [Performance](https://github.com/MattFanto/orjson-ddb#performance)
+    1. [Latency](https://github.com/MattFanto/orjson-ddb#latency)
+    2. [Memory](https://github.com/MattFanto/orjson-ddb#memory)
+    3. [Reproducing](https://github.com/MattFanto/orjson-ddb#reproducing)
+4. [Questions](https://github.com/MattFanto/orjson-ddb#questions)
+5. [Packaging](https://github.com/MattFanto/orjson-ddb#packaging)
+6. [License](https://github.com/MattFanto/orjson-ddb#license)
+
+## Usage
+
+### Install
+
+To install a wheel from PyPI:
+
+```sh
+pip install --upgrade "pip>=20.3" # manylinux_x_y, universal2 wheel support
+pip install --upgrade orjson-ddb
+```
+
+To build a wheel, see [packaging](https://github.com/MattFanto/orjson-ddb#packaging).
+
+### Deserialize
+
+This library exposes a function `loads` which can deserializer DynamoDB response into a Python dictionary.
+This can be used to parse the API response from DynamoDB, as an example if you are using the REST API:
+```python
+import requests
+import orjson_ddb
+
+response = requests.post("https://dynamodb.us-east-1.amazonaws.com/", data={
+   "TableName": "some_table", 
+   "Key": {"pk": {"S": "pk1"}, "sk": {"S": "sk1"}}
+}, headers={
+   # some headers
+})
+data = orjson_ddb.loads(response.content)
+```
+The same results can be achieved when using boto3 via a context manager provided by the library:
+```python
+import boto3
+from orjson_ddb import ddb_json_parser
+
+
+dynamodb_client = boto3.client("dynamodb", region_name="us-east-1")
+with ddb_json_parser():
+   resp = dynamodb_client.get_item(
+      TableName="some_table",
+      Key={"pk": {"S": "pk1"}, "sk": {"S": "sk1"}}
+   )
+print(resp["Items"])
+# {'sk': 'sk1', 'pk': 'pk1', 'data': {'some_number': 0.123, 'some_string': 'hello'}}
+```
+This context manager tells boto3 to use `orjson_ddb.loads` to deserialize the DynamoDB response.
+The output dictionary doesn't contain any reference to the DynamoDB Native format and the result is the same of
+what you would get with `boto3.resource('dynamodb').Table('some_table').get_item(Key={"pk": "pk1", "sk": "sk1"})["Item"]`
+except for "N" type being translated directly to int or float instead of Decimal.
+
+N.B. Unfortunately at the moment it is not possible to use this library with `boto3.resource`.
+
+
+### Serialize
+
+Serialization of python dictionary to DynamoDB Native JSON format is not available yet.
+
+
+## Performance
+
+Deserialization performance of orjson-ddb is better than
+boto3, dynamodb-json-util. The benchmarks are done on
+fixtures of real data converted to DynamoDB native format:
+
+* twitter.json, 631.5KiB, results of a search on Twitter for "一", containing
+CJK strings, dictionaries of strings and arrays of dictionaries, indented.
+
+* github.json, 55.8KiB, a GitHub activity feed, containing dictionaries of
+strings and arrays of dictionaries, not indented.
+
+* citm_catalog.json, 1.7MiB, concert data, containing nested dictionaries of
+strings and arrays of integers, indented.
+
+* canada.json, 2.2MiB, coordinates of the Canadian border in GeoJSON
+format, containing floats and arrays, indented.
+
+### Latency
+
+#### twitter.json deserialization
+
+| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
+|--------------------|---------------------------------|-------------------------|----------------------|
+| orjson-ddb         |                            2.17 |                   459.7 |                 1    |
+| boto3-json         |                           18.61 |                    54.1 |                 8.57 |
+| dynamodb-json-util |                           54.13 |                    18.4 |                24.92 |
+
+#### citm_catalog.json deserialization
+
+| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
+|--------------------|---------------------------------|-------------------------|----------------------|
+| orjson-ddb         |                            4.43 |                   240.3 |                 1    |
+| boto3-json         |                           53.3  |                    18.6 |                12.03 |
+| dynamodb-json-util |                           57.27 |                    17.5 |                12.93 |
+
+#### canada.json deserialization
+
+| Library            |   Median latency (milliseconds) |   Operations per second |   Relative (latency) |
+|--------------------|---------------------------------|-------------------------|----------------------|
+| orjson-ddb         |                           19.22 |                    52   |                 1    |
+| boto3-json         |                          221.83 |                     4.5 |                11.54 |
+| dynamodb-json-util |                          244.14 |                     4.1 |                12.7  |
+
+
+### Reproducing
+
+The above was measured using Python 3.9.13 on Linux (amd64) with
+orjson-ddb 0.1.1, boto3==1.21.27, dynamodb-json==1.3
+
+The latency results can be reproduced using the `pybench` and `graph`
+scripts.
+
+## Questions
+
+### Why can't I install it from PyPI?
+
+Probably `pip` needs to be upgraded to version 20.3 or later to support
+the latest manylinux_x_y or universal2 wheel formats.
+
+### "Cargo, the Rust package manager, is not installed or is not on PATH."
+
+This happens when there are no binary wheels (like manylinux) for your
+platform on PyPI. You can install [Rust](https://www.rust-lang.org/) through
+`rustup` or a package manager and then it will compile.
+
+### Will it support PyPy?
+
+Probably not.
+
+## Packaging
+
+To package orjson-ddb requires at least [Rust](https://www.rust-lang.org/) 1.57
+and the [maturin](https://github.com/PyO3/maturin) build tool. The recommended
+build command is:
+
+```sh
+maturin build --release --strip
+```
+
+It benefits from also having a C build environment to compile a faster
+deserialization backend. See this project's `manylinux_2_28` builds for an
+example using clang and LTO.
+
+The project's own CI tests against `nightly-2022-07-26` and stable 1.54. It
+is prudent to pin the nightly version because that channel can introduce
+breaking changes.
+
+orjson-ddb is tested for amd64, aarch64, and arm7 on Linux. It is tested for
+amd64 on macOS and cross-compiles for aarch64. For Windows it is tested on
+amd64.
+
+There are no runtime dependencies other than libc.
+
+Tests are included in the source distribution on PyPI. The
+requirements to run the tests are specified in `test/requirements.txt`. The
+tests should be run as part of the build. It can be run with
+`pytest -q test`.
+
+## License
+
+orjson was written by ijl <ijl@mailbox.org>, copyright 2018 - 2021, licensed under both the Apache 2 and MIT licenses.
+
+orjson-ddb was forked from orjson and is maintained by Mattia Fantoni <mattia.fantoni@gmail.com>, licensed same as orjson.
```

## Comparing `orjson_ddb-0.2.0.dist-info/license_files/LICENSE-APACHE` & `orjson_ddb-0.2.1.dist-info/license_files/LICENSE-APACHE`

 * *Ordering differences only*

 * *Files 14% similar despite different names*

```diff
@@ -1,201 +1,201 @@
-                              Apache License
-                        Version 2.0, January 2004
-                     http://www.apache.org/licenses/
-
-TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
-
-1. Definitions.
-
-   "License" shall mean the terms and conditions for use, reproduction,
-   and distribution as defined by Sections 1 through 9 of this document.
-
-   "Licensor" shall mean the copyright owner or entity authorized by
-   the copyright owner that is granting the License.
-
-   "Legal Entity" shall mean the union of the acting entity and all
-   other entities that control, are controlled by, or are under common
-   control with that entity. For the purposes of this definition,
-   "control" means (i) the power, direct or indirect, to cause the
-   direction or management of such entity, whether by contract or
-   otherwise, or (ii) ownership of fifty percent (50%) or more of the
-   outstanding shares, or (iii) beneficial ownership of such entity.
-
-   "You" (or "Your") shall mean an individual or Legal Entity
-   exercising permissions granted by this License.
-
-   "Source" form shall mean the preferred form for making modifications,
-   including but not limited to software source code, documentation
-   source, and configuration files.
-
-   "Object" form shall mean any form resulting from mechanical
-   transformation or translation of a Source form, including but
-   not limited to compiled object code, generated documentation,
-   and conversions to other media types.
-
-   "Work" shall mean the work of authorship, whether in Source or
-   Object form, made available under the License, as indicated by a
-   copyright notice that is included in or attached to the work
-   (an example is provided in the Appendix below).
-
-   "Derivative Works" shall mean any work, whether in Source or Object
-   form, that is based on (or derived from) the Work and for which the
-   editorial revisions, annotations, elaborations, or other modifications
-   represent, as a whole, an original work of authorship. For the purposes
-   of this License, Derivative Works shall not include works that remain
-   separable from, or merely link (or bind by name) to the interfaces of,
-   the Work and Derivative Works thereof.
-
-   "Contribution" shall mean any work of authorship, including
-   the original version of the Work and any modifications or additions
-   to that Work or Derivative Works thereof, that is intentionally
-   submitted to Licensor for inclusion in the Work by the copyright owner
-   or by an individual or Legal Entity authorized to submit on behalf of
-   the copyright owner. For the purposes of this definition, "submitted"
-   means any form of electronic, verbal, or written communication sent
-   to the Licensor or its representatives, including but not limited to
-   communication on electronic mailing lists, source code control systems,
-   and issue tracking systems that are managed by, or on behalf of, the
-   Licensor for the purpose of discussing and improving the Work, but
-   excluding communication that is conspicuously marked or otherwise
-   designated in writing by the copyright owner as "Not a Contribution."
-
-   "Contributor" shall mean Licensor and any individual or Legal Entity
-   on behalf of whom a Contribution has been received by Licensor and
-   subsequently incorporated within the Work.
-
-2. Grant of Copyright License. Subject to the terms and conditions of
-   this License, each Contributor hereby grants to You a perpetual,
-   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
-   copyright license to reproduce, prepare Derivative Works of,
-   publicly display, publicly perform, sublicense, and distribute the
-   Work and such Derivative Works in Source or Object form.
-
-3. Grant of Patent License. Subject to the terms and conditions of
-   this License, each Contributor hereby grants to You a perpetual,
-   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
-   (except as stated in this section) patent license to make, have made,
-   use, offer to sell, sell, import, and otherwise transfer the Work,
-   where such license applies only to those patent claims licensable
-   by such Contributor that are necessarily infringed by their
-   Contribution(s) alone or by combination of their Contribution(s)
-   with the Work to which such Contribution(s) was submitted. If You
-   institute patent litigation against any entity (including a
-   cross-claim or counterclaim in a lawsuit) alleging that the Work
-   or a Contribution incorporated within the Work constitutes direct
-   or contributory patent infringement, then any patent licenses
-   granted to You under this License for that Work shall terminate
-   as of the date such litigation is filed.
-
-4. Redistribution. You may reproduce and distribute copies of the
-   Work or Derivative Works thereof in any medium, with or without
-   modifications, and in Source or Object form, provided that You
-   meet the following conditions:
-
-   (a) You must give any other recipients of the Work or
-       Derivative Works a copy of this License; and
-
-   (b) You must cause any modified files to carry prominent notices
-       stating that You changed the files; and
-
-   (c) You must retain, in the Source form of any Derivative Works
-       that You distribute, all copyright, patent, trademark, and
-       attribution notices from the Source form of the Work,
-       excluding those notices that do not pertain to any part of
-       the Derivative Works; and
-
-   (d) If the Work includes a "NOTICE" text file as part of its
-       distribution, then any Derivative Works that You distribute must
-       include a readable copy of the attribution notices contained
-       within such NOTICE file, excluding those notices that do not
-       pertain to any part of the Derivative Works, in at least one
-       of the following places: within a NOTICE text file distributed
-       as part of the Derivative Works; within the Source form or
-       documentation, if provided along with the Derivative Works; or,
-       within a display generated by the Derivative Works, if and
-       wherever such third-party notices normally appear. The contents
-       of the NOTICE file are for informational purposes only and
-       do not modify the License. You may add Your own attribution
-       notices within Derivative Works that You distribute, alongside
-       or as an addendum to the NOTICE text from the Work, provided
-       that such additional attribution notices cannot be construed
-       as modifying the License.
-
-   You may add Your own copyright statement to Your modifications and
-   may provide additional or different license terms and conditions
-   for use, reproduction, or distribution of Your modifications, or
-   for any such Derivative Works as a whole, provided Your use,
-   reproduction, and distribution of the Work otherwise complies with
-   the conditions stated in this License.
-
-5. Submission of Contributions. Unless You explicitly state otherwise,
-   any Contribution intentionally submitted for inclusion in the Work
-   by You to the Licensor shall be under the terms and conditions of
-   this License, without any additional terms or conditions.
-   Notwithstanding the above, nothing herein shall supersede or modify
-   the terms of any separate license agreement you may have executed
-   with Licensor regarding such Contributions.
-
-6. Trademarks. This License does not grant permission to use the trade
-   names, trademarks, service marks, or product names of the Licensor,
-   except as required for reasonable and customary use in describing the
-   origin of the Work and reproducing the content of the NOTICE file.
-
-7. Disclaimer of Warranty. Unless required by applicable law or
-   agreed to in writing, Licensor provides the Work (and each
-   Contributor provides its Contributions) on an "AS IS" BASIS,
-   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
-   implied, including, without limitation, any warranties or conditions
-   of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
-   PARTICULAR PURPOSE. You are solely responsible for determining the
-   appropriateness of using or redistributing the Work and assume any
-   risks associated with Your exercise of permissions under this License.
-
-8. Limitation of Liability. In no event and under no legal theory,
-   whether in tort (including negligence), contract, or otherwise,
-   unless required by applicable law (such as deliberate and grossly
-   negligent acts) or agreed to in writing, shall any Contributor be
-   liable to You for damages, including any direct, indirect, special,
-   incidental, or consequential damages of any character arising as a
-   result of this License or out of the use or inability to use the
-   Work (including but not limited to damages for loss of goodwill,
-   work stoppage, computer failure or malfunction, or any and all
-   other commercial damages or losses), even if such Contributor
-   has been advised of the possibility of such damages.
-
-9. Accepting Warranty or Additional Liability. While redistributing
-   the Work or Derivative Works thereof, You may choose to offer,
-   and charge a fee for, acceptance of support, warranty, indemnity,
-   or other liability obligations and/or rights consistent with this
-   License. However, in accepting such obligations, You may act only
-   on Your own behalf and on Your sole responsibility, not on behalf
-   of any other Contributor, and only if You agree to indemnify,
-   defend, and hold each Contributor harmless for any liability
-   incurred by, or claims asserted against, such Contributor by reason
-   of your accepting any such warranty or additional liability.
-
-END OF TERMS AND CONDITIONS
-
-APPENDIX: How to apply the Apache License to your work.
-
-   To apply the Apache License to your work, attach the following
-   boilerplate notice, with the fields enclosed by brackets "[]"
-   replaced with your own identifying information. (Don't include
-   the brackets!)  The text should be enclosed in the appropriate
-   comment syntax for the file format. We also recommend that a
-   file or class name and description of purpose be included on the
-   same "printed page" as the copyright notice for easier
-   identification within third-party archives.
-
-Copyright [yyyy] [name of copyright owner]
-
-Licensed under the Apache License, Version 2.0 (the "License");
-you may not use this file except in compliance with the License.
-You may obtain a copy of the License at
-
-	http://www.apache.org/licenses/LICENSE-2.0
-
-Unless required by applicable law or agreed to in writing, software
-distributed under the License is distributed on an "AS IS" BASIS,
-WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
-See the License for the specific language governing permissions and
-limitations under the License.
+                              Apache License
+                        Version 2.0, January 2004
+                     http://www.apache.org/licenses/
+
+TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
+
+1. Definitions.
+
+   "License" shall mean the terms and conditions for use, reproduction,
+   and distribution as defined by Sections 1 through 9 of this document.
+
+   "Licensor" shall mean the copyright owner or entity authorized by
+   the copyright owner that is granting the License.
+
+   "Legal Entity" shall mean the union of the acting entity and all
+   other entities that control, are controlled by, or are under common
+   control with that entity. For the purposes of this definition,
+   "control" means (i) the power, direct or indirect, to cause the
+   direction or management of such entity, whether by contract or
+   otherwise, or (ii) ownership of fifty percent (50%) or more of the
+   outstanding shares, or (iii) beneficial ownership of such entity.
+
+   "You" (or "Your") shall mean an individual or Legal Entity
+   exercising permissions granted by this License.
+
+   "Source" form shall mean the preferred form for making modifications,
+   including but not limited to software source code, documentation
+   source, and configuration files.
+
+   "Object" form shall mean any form resulting from mechanical
+   transformation or translation of a Source form, including but
+   not limited to compiled object code, generated documentation,
+   and conversions to other media types.
+
+   "Work" shall mean the work of authorship, whether in Source or
+   Object form, made available under the License, as indicated by a
+   copyright notice that is included in or attached to the work
+   (an example is provided in the Appendix below).
+
+   "Derivative Works" shall mean any work, whether in Source or Object
+   form, that is based on (or derived from) the Work and for which the
+   editorial revisions, annotations, elaborations, or other modifications
+   represent, as a whole, an original work of authorship. For the purposes
+   of this License, Derivative Works shall not include works that remain
+   separable from, or merely link (or bind by name) to the interfaces of,
+   the Work and Derivative Works thereof.
+
+   "Contribution" shall mean any work of authorship, including
+   the original version of the Work and any modifications or additions
+   to that Work or Derivative Works thereof, that is intentionally
+   submitted to Licensor for inclusion in the Work by the copyright owner
+   or by an individual or Legal Entity authorized to submit on behalf of
+   the copyright owner. For the purposes of this definition, "submitted"
+   means any form of electronic, verbal, or written communication sent
+   to the Licensor or its representatives, including but not limited to
+   communication on electronic mailing lists, source code control systems,
+   and issue tracking systems that are managed by, or on behalf of, the
+   Licensor for the purpose of discussing and improving the Work, but
+   excluding communication that is conspicuously marked or otherwise
+   designated in writing by the copyright owner as "Not a Contribution."
+
+   "Contributor" shall mean Licensor and any individual or Legal Entity
+   on behalf of whom a Contribution has been received by Licensor and
+   subsequently incorporated within the Work.
+
+2. Grant of Copyright License. Subject to the terms and conditions of
+   this License, each Contributor hereby grants to You a perpetual,
+   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
+   copyright license to reproduce, prepare Derivative Works of,
+   publicly display, publicly perform, sublicense, and distribute the
+   Work and such Derivative Works in Source or Object form.
+
+3. Grant of Patent License. Subject to the terms and conditions of
+   this License, each Contributor hereby grants to You a perpetual,
+   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
+   (except as stated in this section) patent license to make, have made,
+   use, offer to sell, sell, import, and otherwise transfer the Work,
+   where such license applies only to those patent claims licensable
+   by such Contributor that are necessarily infringed by their
+   Contribution(s) alone or by combination of their Contribution(s)
+   with the Work to which such Contribution(s) was submitted. If You
+   institute patent litigation against any entity (including a
+   cross-claim or counterclaim in a lawsuit) alleging that the Work
+   or a Contribution incorporated within the Work constitutes direct
+   or contributory patent infringement, then any patent licenses
+   granted to You under this License for that Work shall terminate
+   as of the date such litigation is filed.
+
+4. Redistribution. You may reproduce and distribute copies of the
+   Work or Derivative Works thereof in any medium, with or without
+   modifications, and in Source or Object form, provided that You
+   meet the following conditions:
+
+   (a) You must give any other recipients of the Work or
+       Derivative Works a copy of this License; and
+
+   (b) You must cause any modified files to carry prominent notices
+       stating that You changed the files; and
+
+   (c) You must retain, in the Source form of any Derivative Works
+       that You distribute, all copyright, patent, trademark, and
+       attribution notices from the Source form of the Work,
+       excluding those notices that do not pertain to any part of
+       the Derivative Works; and
+
+   (d) If the Work includes a "NOTICE" text file as part of its
+       distribution, then any Derivative Works that You distribute must
+       include a readable copy of the attribution notices contained
+       within such NOTICE file, excluding those notices that do not
+       pertain to any part of the Derivative Works, in at least one
+       of the following places: within a NOTICE text file distributed
+       as part of the Derivative Works; within the Source form or
+       documentation, if provided along with the Derivative Works; or,
+       within a display generated by the Derivative Works, if and
+       wherever such third-party notices normally appear. The contents
+       of the NOTICE file are for informational purposes only and
+       do not modify the License. You may add Your own attribution
+       notices within Derivative Works that You distribute, alongside
+       or as an addendum to the NOTICE text from the Work, provided
+       that such additional attribution notices cannot be construed
+       as modifying the License.
+
+   You may add Your own copyright statement to Your modifications and
+   may provide additional or different license terms and conditions
+   for use, reproduction, or distribution of Your modifications, or
+   for any such Derivative Works as a whole, provided Your use,
+   reproduction, and distribution of the Work otherwise complies with
+   the conditions stated in this License.
+
+5. Submission of Contributions. Unless You explicitly state otherwise,
+   any Contribution intentionally submitted for inclusion in the Work
+   by You to the Licensor shall be under the terms and conditions of
+   this License, without any additional terms or conditions.
+   Notwithstanding the above, nothing herein shall supersede or modify
+   the terms of any separate license agreement you may have executed
+   with Licensor regarding such Contributions.
+
+6. Trademarks. This License does not grant permission to use the trade
+   names, trademarks, service marks, or product names of the Licensor,
+   except as required for reasonable and customary use in describing the
+   origin of the Work and reproducing the content of the NOTICE file.
+
+7. Disclaimer of Warranty. Unless required by applicable law or
+   agreed to in writing, Licensor provides the Work (and each
+   Contributor provides its Contributions) on an "AS IS" BASIS,
+   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
+   implied, including, without limitation, any warranties or conditions
+   of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
+   PARTICULAR PURPOSE. You are solely responsible for determining the
+   appropriateness of using or redistributing the Work and assume any
+   risks associated with Your exercise of permissions under this License.
+
+8. Limitation of Liability. In no event and under no legal theory,
+   whether in tort (including negligence), contract, or otherwise,
+   unless required by applicable law (such as deliberate and grossly
+   negligent acts) or agreed to in writing, shall any Contributor be
+   liable to You for damages, including any direct, indirect, special,
+   incidental, or consequential damages of any character arising as a
+   result of this License or out of the use or inability to use the
+   Work (including but not limited to damages for loss of goodwill,
+   work stoppage, computer failure or malfunction, or any and all
+   other commercial damages or losses), even if such Contributor
+   has been advised of the possibility of such damages.
+
+9. Accepting Warranty or Additional Liability. While redistributing
+   the Work or Derivative Works thereof, You may choose to offer,
+   and charge a fee for, acceptance of support, warranty, indemnity,
+   or other liability obligations and/or rights consistent with this
+   License. However, in accepting such obligations, You may act only
+   on Your own behalf and on Your sole responsibility, not on behalf
+   of any other Contributor, and only if You agree to indemnify,
+   defend, and hold each Contributor harmless for any liability
+   incurred by, or claims asserted against, such Contributor by reason
+   of your accepting any such warranty or additional liability.
+
+END OF TERMS AND CONDITIONS
+
+APPENDIX: How to apply the Apache License to your work.
+
+   To apply the Apache License to your work, attach the following
+   boilerplate notice, with the fields enclosed by brackets "[]"
+   replaced with your own identifying information. (Don't include
+   the brackets!)  The text should be enclosed in the appropriate
+   comment syntax for the file format. We also recommend that a
+   file or class name and description of purpose be included on the
+   same "printed page" as the copyright notice for easier
+   identification within third-party archives.
+
+Copyright [yyyy] [name of copyright owner]
+
+Licensed under the Apache License, Version 2.0 (the "License");
+you may not use this file except in compliance with the License.
+You may obtain a copy of the License at
+
+	http://www.apache.org/licenses/LICENSE-2.0
+
+Unless required by applicable law or agreed to in writing, software
+distributed under the License is distributed on an "AS IS" BASIS,
+WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
+See the License for the specific language governing permissions and
+limitations under the License.
```

## Comparing `orjson_ddb-0.2.0.dist-info/license_files/LICENSE-MIT` & `orjson_ddb-0.2.1.dist-info/license_files/LICENSE-MIT`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,23 +1,23 @@
-Permission is hereby granted, free of charge, to any
-person obtaining a copy of this software and associated
-documentation files (the "Software"), to deal in the
-Software without restriction, including without
-limitation the rights to use, copy, modify, merge,
-publish, distribute, sublicense, and/or sell copies of
-the Software, and to permit persons to whom the Software
-is furnished to do so, subject to the following
-conditions:
-
-The above copyright notice and this permission notice
-shall be included in all copies or substantial portions
-of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF
-ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED
-TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
-PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT
-SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
-CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
-OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR
-IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
-DEALINGS IN THE SOFTWARE.
+Permission is hereby granted, free of charge, to any
+person obtaining a copy of this software and associated
+documentation files (the "Software"), to deal in the
+Software without restriction, including without
+limitation the rights to use, copy, modify, merge,
+publish, distribute, sublicense, and/or sell copies of
+the Software, and to permit persons to whom the Software
+is furnished to do so, subject to the following
+conditions:
+
+The above copyright notice and this permission notice
+shall be included in all copies or substantial portions
+of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF
+ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED
+TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
+PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT
+SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
+CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
+OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR
+IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
+DEALINGS IN THE SOFTWARE.
```

