# Comparing `tmp/dedlin-1.12.0.tar.gz` & `tmp/dedlin-1.13.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dedlin-1.12.0.tar", max compression
+gzip compressed data, was "dedlin-1.13.0.tar", max compression
```

## Comparing `dedlin-1.12.0.tar` & `dedlin-1.13.0.tar`

### file list

```diff
@@ -1,28 +1,36 @@
--rw-r--r--   0        0        0       42 2022-12-29 22:47:14.610685 dedlin-1.12.0/dedlin/__init__.py
--rw-r--r--   0        0        0     4182 2022-07-31 17:01:47.147103 dedlin-1.12.0/dedlin/__main__.py
--rw-r--r--   0        0        0     8353 2022-12-07 22:48:33.729761 dedlin-1.12.0/dedlin/basic_types.py
--rw-r--r--   0        0        0     3941 2022-07-31 17:01:47.125379 dedlin-1.12.0/dedlin/command_sources.py
--rw-r--r--   0        0        0    15212 2022-12-29 21:53:37.819545 dedlin-1.12.0/dedlin/document.py
--rw-r--r--   0        0        0     3113 2022-12-29 22:47:14.768636 dedlin-1.12.0/dedlin/document_sources.py
--rw-r--r--   0        0        0     1444 2022-07-31 02:28:51.370704 dedlin-1.12.0/dedlin/file_system.py
--rw-r--r--   0        0        0      190 2022-06-27 15:17:29.309984 dedlin-1.12.0/dedlin/flash.py
--rw-r--r--   0        0        0     1948 2022-07-31 17:02:36.145350 dedlin-1.12.0/dedlin/help_text.py
--rw-r--r--   0        0        0     1589 2022-07-06 01:16:10.673963 dedlin-1.12.0/dedlin/history_feature.py
--rw-r--r--   0        0        0      780 2022-06-26 01:45:04.623153 dedlin-1.12.0/dedlin/info_bar.py
--rw-r--r--   0        0        0     1726 2022-07-05 00:14:05.011630 dedlin-1.12.0/dedlin/logging_utils.py
--rw-r--r--   0        0        0     1970 2022-06-18 23:31:53.155666 dedlin-1.12.0/dedlin/lorem_data.py
--rw-r--r--   0        0        0    14279 2022-12-29 21:58:21.395469 dedlin-1.12.0/dedlin/main.py
--rw-r--r--   0        0        0    10368 2022-12-29 22:47:14.898958 dedlin-1.12.0/dedlin/parsers.py
--rw-r--r--   0        0        0      588 2022-07-04 17:56:26.713572 dedlin-1.12.0/dedlin/pygments_code.py
--rw-r--r--   0        0        0      697 2022-07-23 23:51:13.892750 dedlin-1.12.0/dedlin/rich_output.py
--rw-r--r--   0        0        0      580 2022-06-27 15:17:29.371983 dedlin-1.12.0/dedlin/spelling_overlay.py
--rw-r--r--   0        0        0        0 2022-06-09 18:10:08.703000 dedlin-1.12.0/dedlin/utils/__init__.py
--rw-r--r--   0        0        0      225 2022-06-19 21:12:46.591013 dedlin-1.12.0/dedlin/utils/exceptions.py
--rw-r--r--   0        0        0      366 2022-06-21 02:31:26.265490 dedlin-1.12.0/dedlin/utils/file_utils.py
--rw-r--r--   0        0        0      677 2022-06-26 01:40:42.646243 dedlin-1.12.0/dedlin/web.py
--rw-r--r--   0        0        0     1529 2022-12-08 00:17:58.932590 dedlin-1.12.0/dedlin/web_api.py
--rw-r--r--   0        0        0     1071 2022-06-16 01:43:23.611981 dedlin-1.12.0/LICENSE
--rw-r--r--   0        0        0     2904 2022-12-29 23:13:05.044192 dedlin-1.12.0/pyproject.toml
--rw-r--r--   0        0        0     1898 2022-12-29 21:29:39.447219 dedlin-1.12.0/README.md
--rw-r--r--   0        0        0     3053 1970-01-01 00:00:00.000000 dedlin-1.12.0/setup.py
--rw-r--r--   0        0        0     3357 1970-01-01 00:00:00.000000 dedlin-1.12.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-02-26 02:20:22.397674 dedlin-1.13.0/dedlin/__init__.py
+-rw-r--r--   0        0        0     4282 2023-05-13 18:30:05.436664 dedlin-1.13.0/dedlin/__main__.py
+-rw-r--r--   0        0        0     8790 2023-05-13 18:36:03.687054 dedlin-1.13.0/dedlin/basic_types.py
+-rw-r--r--   0        0        0     4005 2023-02-25 20:07:21.449444 dedlin-1.13.0/dedlin/command_sources.py
+-rw-r--r--   0        0        0    15363 2023-05-13 18:36:42.894018 dedlin-1.13.0/dedlin/document.py
+-rw-r--r--   0        0        0     3113 2022-12-29 22:47:14.768636 dedlin-1.13.0/dedlin/document_sources.py
+-rw-r--r--   0        0        0     2145 2023-05-13 18:30:05.467647 dedlin-1.13.0/dedlin/file_system.py
+-rw-r--r--   0        0        0      243 2023-05-13 18:30:05.398607 dedlin-1.13.0/dedlin/flash.py
+-rw-r--r--   0        0        0     1632 2023-05-13 18:30:05.520016 dedlin-1.13.0/dedlin/history_feature.py
+-rw-r--r--   0        0        0     1726 2022-07-05 00:14:05.011630 dedlin-1.13.0/dedlin/logging_utils.py
+-rw-r--r--   0        0        0    15662 2023-05-13 18:35:00.400481 dedlin-1.13.0/dedlin/main.py
+-rw-r--r--   0        0        0        0 2023-03-26 21:45:09.221680 dedlin-1.13.0/dedlin/outputters/__init__.py
+-rw-r--r--   0        0        0      355 2023-05-13 18:34:07.064200 dedlin-1.13.0/dedlin/outputters/plain.py
+-rw-r--r--   0        0        0      919 2023-05-13 18:30:05.330744 dedlin-1.13.0/dedlin/outputters/rich_output.py
+-rw-r--r--   0        0        0      653 2023-05-13 18:34:29.407911 dedlin-1.13.0/dedlin/outputters/talking_outputter.py
+-rw-r--r--   0        0        0    10936 2023-05-13 18:30:05.630575 dedlin-1.13.0/dedlin/parsers.py
+-rw-r--r--   0        0        0       80 2022-06-03 01:18:36.274653 dedlin-1.13.0/dedlin/py.typed
+-rw-r--r--   0        0        0      588 2022-07-04 17:56:26.713572 dedlin-1.13.0/dedlin/pygments_code.py
+-rw-r--r--   0        0        0     2215 2023-05-13 18:33:06.561257 dedlin-1.13.0/dedlin/string_comands.py
+-rw-r--r--   0        0        0        0 2023-03-26 22:05:33.927432 dedlin-1.13.0/dedlin/text/__init__.py
+-rw-r--r--   0        0        0     1948 2022-07-31 17:02:36.145350 dedlin-1.13.0/dedlin/text/help_text.py
+-rw-r--r--   0        0        0        0 2023-03-26 21:45:53.009840 dedlin-1.13.0/dedlin/tools/__init__.py
+-rw-r--r--   0        0        0      273 2023-05-13 18:30:05.403605 dedlin-1.13.0/dedlin/tools/export.py
+-rw-r--r--   0        0        0      780 2022-06-26 01:45:04.623153 dedlin-1.13.0/dedlin/tools/info_bar.py
+-rw-r--r--   0        0        0     1970 2022-06-18 23:31:53.155666 dedlin-1.13.0/dedlin/tools/lorem_data.py
+-rw-r--r--   0        0        0      595 2023-01-02 22:38:48.075545 dedlin-1.13.0/dedlin/tools/spelling_overlay.py
+-rw-r--r--   0        0        0      677 2022-06-26 01:40:42.646243 dedlin-1.13.0/dedlin/tools/web.py
+-rw-r--r--   0        0        0        0 2022-06-09 18:10:08.703000 dedlin-1.13.0/dedlin/utils/__init__.py
+-rw-r--r--   0        0        0      225 2022-06-19 21:12:46.591013 dedlin-1.13.0/dedlin/utils/exceptions.py
+-rw-r--r--   0        0        0      366 2022-06-21 02:31:26.265490 dedlin-1.13.0/dedlin/utils/file_utils.py
+-rw-r--r--   0        0        0     1529 2022-12-08 00:17:58.932590 dedlin-1.13.0/dedlin/web_api.py
+-rw-r--r--   0        0        0     1071 2022-06-16 01:43:23.611981 dedlin-1.13.0/LICENSE
+-rw-r--r--   0        0        0     3708 2023-05-13 18:37:28.881677 dedlin-1.13.0/pyproject.toml
+-rw-r--r--   0        0        0     2913 2023-05-13 18:31:15.766160 dedlin-1.13.0/README.md
+-rw-r--r--   0        0        0     4171 1970-01-01 00:00:00.000000 dedlin-1.13.0/setup.py
+-rw-r--r--   0        0        0     4418 1970-01-01 00:00:00.000000 dedlin-1.13.0/PKG-INFO
```

### Comparing `dedlin-1.12.0/dedlin/__main__.py` & `dedlin-1.13.0/dedlin/__main__.py`

 * *Files 10% similar despite different names*

```diff
@@ -12,14 +12,15 @@
   --version          Show version.
   --macro=<macro>    Run macro file.
   --echo             Echo commands.
   --halt_on_error    End program on error.
   --promptless_quit  Skip prompt on quit.
   --vim_mode         User hostile, no feedback.
   --verbose          Displaying all debugging info.
+  --blind_mode       Optimize for blind users (experimental).
 """
 import logging
 import logging.config
 import sys
 import traceback
 from pathlib import Path
 from typing import Generator, Optional
@@ -27,15 +28,16 @@
 from docopt import docopt
 
 from dedlin.command_sources import CommandGenerator, InteractiveGenerator
 from dedlin.document_sources import PrefillInputter, SimpleInputter, input_with_prefill
 from dedlin.flash import title_screen
 from dedlin.logging_utils import configure_logging
 from dedlin.main import Dedlin
-from dedlin.rich_output import RichPrinter
+from dedlin.outputters import rich_output, talking_outputter
+from dedlin.outputters.plain import plain_printer
 
 logger = logging.getLogger(__name__)
 
 
 def main() -> None:
     """Main function."""
     arguments = docopt(__doc__, version="1.4.0")
@@ -43,68 +45,67 @@
         arguments["<file>"],
         echo=bool(arguments["--echo"]),
         halt_on_error=bool(arguments["--halt_on_error"]),
         macro_file_name=arguments["--macro"],
         quit_safety=not arguments["--promptless_quit"],
         vim_mode=bool(arguments["--vim_mode"]),
         verbose=bool(arguments["--verbose"]),
+        blind_mode=bool(arguments["--blind_mode"]),
     )
     sys.exit(0)
 
 
 def run(
     file_name: Optional[str] = None,
     macro_file_name: Optional[str] = None,
     echo: bool = False,
     halt_on_error: bool = False,
     quit_safety: bool = False,
     vim_mode: bool = False,
     verbose: bool = False,
+    blind_mode: bool = False,
 ) -> Dedlin:
     """Set up everything except things from command line"""
     if verbose:
         config = configure_logging()
         logging.config.dictConfig(config)
         logger.info("Verbose mode enabled")
 
     if not macro_file_name:
-        title_screen()
+        title_screen(blind_mode)
 
-    rich_printer = RichPrinter()
-
-    def printer(text: Optional[str], end: str = "\n") -> None:
-        text = "" if text is None else text
-        rich_printer.print(text, end="")
+    if blind_mode:
+        logger.info("Blind mode. UI should talk.")
+        printer = talking_outputter.printer
+        echo = True
+    elif file_name and file_name.endswith(".py"):
+        logger.info("Rich mode. UI should be colorful.")
+        printer = rich_output.printer
+    else:
+        logger.info("Plain mode. UI should be dull.")
+        printer = plain_printer
 
     if macro_file_name:
         the_command_generator = CommandGenerator(Path(macro_file_name))
         # command_handler = the_generator.generate()
     else:
         the_command_generator = InteractiveGenerator()
         the_command_generator.prompt = " * "
         # command_handler = the_interactive_generator.generate()
 
     def document_inputter(prompt: str, text: str = "") -> Generator[str, None, None]:
         """Get input from the user"""
         while True:
             yield input_with_prefill(prompt, text)
 
-    def plain_printer(text: Optional[str], end: str = "\n") -> None:
-        text = "" if text is None else text
-        if text.endswith("\n"):
-            text = text[:-1]
-            print(text, end="")
-        else:
-            print(text, end=end)
-
     dedlin = Dedlin(
         inputter=the_command_generator,  # InteractiveGenerator(),
         insert_document_inputter=SimpleInputter(),
         edit_document_inputter=PrefillInputter(),
-        outputter=printer if file_name and file_name.endswith(".py") else plain_printer,
+        outputter=printer,
     )
 
     # save on crash but hides error info
     # sys.excepthook = lambda type, value, tb: dedlin.save_document() if dedlin.doc.dirty else None
 
     dedlin.halt_on_error = halt_on_error
     dedlin.echo = echo
```

### Comparing `dedlin-1.12.0/dedlin/basic_types.py` & `dedlin-1.13.0/dedlin/basic_types.py`

 * *Files 4% similar despite different names*

```diff
@@ -32,14 +32,17 @@
     DELETE = auto()
     REPLACE = auto()
 
     # file and exit
     QUIT = auto()
     EXIT = auto()
     TRANSFER = auto()
+    EXPORT = auto()
+
+    # Add text
     BROWSE = auto()
 
     # reorder commands
     MOVE = auto()
     COPY = auto()
     SHUFFLE = auto()
     SORT = auto()
@@ -53,14 +56,36 @@
     # other
     HELP = auto()
     UNDO = auto()
     UNKNOWN = auto()
     INFO = auto()
     CRASH = auto()
 
+    # print
+    PRINT = auto()
+
+    # Block String commands
+    INDENT = auto()
+    DEDENT = auto()
+
+    # String commands
+    TITLE = auto()
+    SWAPCASE = auto()
+    CASEFOLD = auto()
+    CAPITALIZE = auto()
+    UPPER = auto()
+    LOWER = auto()
+    EXPANDTABS = auto()
+    RJUST = auto()
+    LJUST = auto()
+    CENTER = auto()
+    RSTRIP = auto()
+    LSTRIP = auto()
+    STRIP = auto()
+
 
 @dataclass(frozen=True)
 class LineRange:
     """A 1-base range of lines
 
     TODO: refactor to start + positive offset and end is a convenience property
     """
@@ -237,15 +262,15 @@
                 return False
         return True
 
     def format(self) -> str:
         """Format the command as a string"""
         range_part = self.line_range.format() if self.line_range is not None else ""
         phrase_part = self.phrases.format() if self.phrases is not None else ""
-        return " ".join([range_part, self.command.name, phrase_part])
+        return " ".join([range_part, self.command.name, phrase_part]).strip()
 
 
 def try_parse_int(value: str, default_value: Optional[int] = None) -> Optional[int]:
     """ "Parse int without raising errors"""
     try:
         return int(value)
     except ValueError:
@@ -262,15 +287,14 @@
         ...
 
 
 def null_printer(text: str, end: str = "") -> None:
     """
     Do nothing implementation of Printable
     """
-    ...
 
 
 @runtime_checkable
 class CommandGeneratorProtocol(Protocol):
     """Something stateful and that can generate commands"""
 
     prompt: str
@@ -291,8 +315,7 @@
     prompt: str
     default: str
 
     def generate(
         self,
     ) -> Generator[str, None, None]:
         """Generate strings"""
-        ...
```

### Comparing `dedlin-1.12.0/dedlin/command_sources.py` & `dedlin-1.13.0/dedlin/command_sources.py`

 * *Files 4% similar despite different names*

```diff
@@ -94,15 +94,17 @@
     def generate(
         self,
     ) -> Generator[Command, None, None]:
         """Turn a file into a bunch of commands"""
 
         with open(str(self.macro_path), encoding="utf-8") as file:
             for line in file:
-                command = parse_command(line, current_line=self.current_line, document_length=self.document_length)
+                command = parse_command(
+                    line.strip("\n").strip("\r"), current_line=self.current_line, document_length=self.document_length
+                )
                 yield command
 
 
 class InMemoryCommandGenerator:
     """A bunch of predefined commands"""
 
     def __init__(self, commands: Iterable[Command]):
```

### Comparing `dedlin-1.12.0/dedlin/document.py` & `dedlin-1.13.0/dedlin/document.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,33 +4,36 @@
 import logging
 import random
 from typing import Generator, Optional
 
 import icontract
 from pydantic.dataclasses import dataclass
 
+import dedlin.tools.lorem_data as lorem_data
+import dedlin.tools.spelling_overlay as spelling_overlay
 from dedlin.basic_types import LineRange, Phrases, StringGeneratorProtocol
-from dedlin.lorem_data import LOREM_IPSUM
-from dedlin.spelling_overlay import check
+from dedlin.utils.exceptions import DedlinException
 
 logger = logging.getLogger(__name__)
 
 
 @dataclass(frozen=True)
 class EditStatus:
+    """Status of edit operation"""
+
     can_edit_again: bool
     line_edited: Optional[int]
     text: Optional[str]
 
 
 # noinspection PyShadowingBuiltins
 # pylint: disable=redefined-builtin
 def print(*args, **kwargs):
     """Discourage accidental usage of print"""
-    raise Exception("Don't call UI from here.")
+    raise DedlinException("Don't call UI from here.")
 
 
 # What does current line mean when there are 0 lines anyhow? Allow 0 or 1.
 # print(self.current_line) is None and
 @icontract.invariant(lambda self: all("\n" not in line and "\r" not in line for line in self.lines))
 @icontract.invariant(
     lambda self: (1 <= self.current_line <= len(self.lines) or self.current_line in (0, 1) and not self.lines),
@@ -141,21 +144,20 @@
 
         # repair if necessary
         if self.current_line >= len(self.lines):
             self.current_line = len(self.lines)
 
     def spell(self, line_range: LineRange) -> Generator[tuple[str, str], None, None]:
         """Show spelling errors in range"""
-        line_number = 1
 
         # reset current line to start of range.
         self.current_line = line_range.start
         for line_text in self.lines[line_range.start - 1 : line_range.end]:
             end = "" if line_text[:-1] == "\n" else "\n"
-            yield f"   {self.current_line} : {check(line_text)}", end
+            yield f"   {self.current_line} : {spelling_overlay.check(line_text)}", end
             self.current_line += 1
 
     def copy(self, line_range: Optional[LineRange], target_line: int) -> None:
         """Copy lines to target_line"""
         if not line_range:
             line_range = LineRange(1, len(self.lines) - 1)
 
@@ -335,25 +337,25 @@
                 line_number += 1
         logger.debug(f"Inserted at {line_number}")
         return Phrases(accumulated_lines)
 
     def lorem(self, line_range: Optional[LineRange]) -> None:
         """Add lorem ipsum to lines"""
         if not line_range:
-            line_range = LineRange(1, len(LOREM_IPSUM) - 1)
+            line_range = LineRange(1, len(lorem_data.LOREM_IPSUM) - 1)
 
         self.backup()
         # TODO: generate from a specified range of Lorem?
         lines_to_generate = line_range.start
         if lines_to_generate == 0:
-            lines_to_generate = len(LOREM_IPSUM)
+            lines_to_generate = len(lorem_data.LOREM_IPSUM)
 
         for i in range(0, lines_to_generate):
-            if i < len(LOREM_IPSUM):
-                self.lines.append(LOREM_IPSUM[i])
+            if i < len(lorem_data.LOREM_IPSUM):
+                self.lines.append(lorem_data.LOREM_IPSUM[i])
                 self.dirty = True  # this is ugly
         logger.debug(f"Generated {lines_to_generate} lines")
 
     def undo(self) -> None:
         """Undo last change"""
         self.lines = self.previous_lines
         self.previous_current_line = self.current_line
```

### Comparing `dedlin-1.12.0/dedlin/document_sources.py` & `dedlin-1.13.0/dedlin/document_sources.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/file_system.py` & `dedlin-1.13.0/dedlin/file_system.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,22 +2,24 @@
 Class for reading and writing lines to disk.
 
 This could be document lines or macro lines.
 """
 from pathlib import Path
 from typing import Optional
 
+from dedlin.tools.export import export_markdown
+
 
 def read_or_create_file(path: Path) -> list[str]:
     """Attempt to read file, create if it doesn't exist"""
 
     if path:
         print(f"Editing {path.absolute()}")
         if not path.exists():
-            with open(str(path.absolute()), "w", encoding="utf-8") as file:
+            with open(str(path.absolute()), "w", encoding="utf-8"):
                 pass
         lines = read_file(path)
     else:
         lines = []
     return lines
 
 
@@ -34,15 +36,30 @@
             elif line.endswith("\r\n") or line.endswith("\n\r"):
                 lines.append(line[:-2])
             else:
                 lines.append(line)
     return lines
 
 
-def save_and_overwrite(path: Path, lines: list[str]):
+def save_and_overwrite(path: Path, lines: list[str], preferred_line_break: str) -> None:
     """Save a file and overwrite it"""
     if not path:
         raise TypeError("No file path")
     with open(str(path), "w", encoding="utf-8") as file:
         file.seek(0)
-        # TODO: make this use preferred line break
-        file.writelines(line + "\n" for line in lines)
+        file.writelines(line + preferred_line_break for line in lines)
+
+
+def export(path: Path, lines: list[str], preferred_line_break: str) -> None:
+    """Save a file and overwrite it"""
+    if not path:
+        raise TypeError("No file path")
+    if path.suffix.lower() == ".html":
+        html_name = path.rename(path.with_suffix(".html"))
+        with open(str(html_name), "w", encoding="utf-8") as file:
+            file.seek(0)
+            file.write(export_markdown(lines, preferred_line_break))
+    else:
+        with open(str(path), "w", encoding="utf-8") as file:
+            file.seek(0)
+            # TODO: make this use preferred line break
+            file.writelines(line + "\n" for line in lines)
```

### Comparing `dedlin-1.12.0/dedlin/help_text.py` & `dedlin-1.13.0/dedlin/text/help_text.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/history_feature.py` & `dedlin-1.13.0/dedlin/history_feature.py`

 * *Files 5% similar despite different names*

```diff
@@ -36,14 +36,14 @@
 
     def make_sequential_history_file_name(self) -> str:
         """
         Make a sequential history file name
         """
         return f"history{self.count_files_in_history_folder()}.ed"
 
-    def write_command_to_history_file(self, command: str) -> None:
+    def write_command_to_history_file(self, command: str, preferred_line_break: str) -> None:
         """
         Write a command to the history file
         """
         with open(self.history_file, "a", encoding="utf-8") as file_handle:
             file_handle.write(command)
-            file_handle.write("\n")
+            file_handle.write(preferred_line_break)
```

### Comparing `dedlin-1.12.0/dedlin/info_bar.py` & `dedlin-1.13.0/dedlin/tools/info_bar.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/logging_utils.py` & `dedlin-1.13.0/dedlin/logging_utils.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/lorem_data.py` & `dedlin-1.13.0/dedlin/tools/lorem_data.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/main.py` & `dedlin-1.13.0/dedlin/main.py`

 * *Files 8% similar despite different names*

```diff
@@ -4,31 +4,32 @@
 Handles UI and links command parser to the document object
 """
 import logging
 import signal
 from pathlib import Path
 from typing import Any, Callable, Optional
 
-import dedlin.help_text as help_text
+import dedlin.file_system as file_system
+import dedlin.text.help_text as help_text
 from dedlin.basic_types import (
     Command,
     Commands,
     LineRange,
     Phrases,
     Printable,
     null_printer,
 )
 from dedlin.command_sources import InMemoryCommandGenerator
 from dedlin.document import Document
 from dedlin.document_sources import InMemoryInputter, PrefillInputter
-from dedlin.file_system import read_or_create_file, save_and_overwrite
 from dedlin.history_feature import HistoryLog
-from dedlin.info_bar import display_info
+from dedlin.string_comands import process_strings
+from dedlin.tools.info_bar import display_info
+from dedlin.tools.web import fetch_page_as_rows
 from dedlin.utils.exceptions import DedlinException
-from dedlin.web import fetch_page_as_rows
 
 logger = logging.getLogger(__name__)
 
 
 class Dedlin:
     """Application for Dedlin
 
@@ -68,14 +69,19 @@
 
         self.echo = False
         """Write cleaned up text of command to screen"""
 
         self.verbose = False
         """Write logging to screen, even if quiet or vim mode is enabled"""
 
+        self.blind_mode = True
+        """Assume user can't see at all"""
+
+        self.preferred_line_break = "\n"
+
         self.file_path: Optional[Path] = None
         self.history: list[Command] = []
         self.history_log = HistoryLog()
         self.macro_file_name: Optional[Path] = None
 
     def entry_point(self, file_name: Optional[str] = None, macro_file_name: Optional[str] = None) -> int:
         """Entry point for Dedlin"""
@@ -90,15 +96,15 @@
 
         if self.vim_mode or self.quiet:
             self.echo = False
             self.command_outputter = null_printer
 
         self.macro_file_name = Path(macro_file_name) if macro_file_name else None
         self.file_path = Path(file_name) if file_name else None
-        lines = read_or_create_file(self.file_path)
+        lines = file_system.read_or_create_file(self.file_path)
 
         self.doc = Document(
             insert_inputter=self.insert_document_inputter,
             edit_inputter=self.edit_document_inputter,
             lines=lines,
         )
         self.command_inputter.prompt = " * "
@@ -117,19 +123,23 @@
                 self.feedback("Unknown command")
                 continue
 
             if not command.validate():
                 self.feedback(f"Invalid command {command}")
 
             self.history.append(command)
-            self.history_log.write_command_to_history_file(command.format())
+            self.history_log.write_command_to_history_file(command.format(), self.preferred_line_break)
             self.echo_if_needed(command.format())
 
             if command.command == Commands.REDO:
-                command = self.history[-2]
+                try:
+                    command = self.history[-2]
+                except IndexError:
+                    self.feedback("Nothing to redo, not enough history")
+                    continue
                 self.history.append(command)
                 self.echo_if_needed(command.original_text)
 
             if command.command == Commands.BROWSE:
                 if self.doc.dirty:
                     self.feedback("Discarding current document")
                 if command.phrases and command.phrases.first is None:
@@ -154,15 +164,15 @@
             elif command.command == Commands.SPELL and command.line_range:
                 for line, end in self.doc.spell(command.line_range):
                     self.document_outputter(line, end=end)
             elif command.command == Commands.DELETE and command.line_range:
                 if self.doc.delete(command.line_range):
                     self.feedback(f"Deleted lines {command.line_range.start} to {command.line_range.end}")
                 else:
-                    self.feedback(f"Could not delete")
+                    self.feedback("Could not delete")
             elif command.command in (Commands.EXIT, Commands.QUIT):
                 if self.vim_mode:
                     continue
                 if command.command == Commands.QUIT and self.doc.dirty and self.quit_safety:
                     # TODO: Q & E are a mess.
                     # self.command_outputter("Save changes? (y/n) ", end="")
                     # if "y" in next(generate):
@@ -262,22 +272,45 @@
                     for text in help_text.SPECIFIC_HELP.values():
                         self.feedback("")
                         self.feedback(text)
                 elif command.phrases and command.phrases.first.upper() in help_text.SPECIFIC_HELP:
                     self.feedback(help_text.SPECIFIC_HELP[command.phrases.first.upper()])
                 else:
                     self.feedback("Don't have help for that category")
+            elif command.command == Commands.EXPORT:
+                file_system.export(self.file_path, self.doc.lines, self.preferred_line_break)
+                self.feedback("Exported to")
+            elif command.command in (
+                Commands.TITLE,
+                Commands.SWAPCASE,
+                Commands.CASEFOLD,
+                Commands.CAPITALIZE,
+                Commands.UPPER,
+                Commands.LOWER,
+                Commands.EXPANDTABS,
+                Commands.RJUST,
+                Commands.LJUST,
+                Commands.CENTER,
+                Commands.RSTRIP,
+                Commands.LSTRIP,
+                Commands.STRIP,
+            ):
+                process_strings(self.doc.lines, command)
             elif command.command == Commands.UNKNOWN:
                 self.feedback("Unknown command, type HELP for help")
                 if self.halt_on_error:
                     raise Exception(f"Unknown command {command.original_text}")
             else:
                 self.feedback(f"Command {command.command} not implemented")
 
-            self.feedback(f"--- Current line is {self.doc.current_line}, {len(self.doc.lines)} lines total ---")
+            if self.blind_mode:
+                status = f"Current line {self.doc.current_line} of {len(self.doc.lines)}"
+            else:
+                status = f"--- Current line is {self.doc.current_line}, {len(self.doc.lines)} lines total ---"
+            self.feedback(status)
         return 0
 
     def feedback(self, string, end="\n") -> None:
         """Output feedback to the user"""
         if not (self.vim_mode or self.quiet):
             self.command_outputter(string, end)
             return
@@ -296,22 +329,24 @@
     def save_document(self, phrases: Optional[Phrases] = None):
         """Save the document to the file"""
 
         # TODO: Refactor and guarantee that the file exists when saved
         if self.doc:
             if self.file_path is not None and phrases is not None:
                 self.file_path = Path(phrases.first)
-            save_and_overwrite(self.file_path, self.doc.lines)
+            file_system.save_and_overwrite(self.file_path, self.doc.lines, self.preferred_line_break)
             self.doc.dirty = False
 
     def save_macro(self):
         """Save the document to the file"""
-        save_and_overwrite(Path("history.ed"), [_.original_text for _ in self.history])
+        file_system.save_and_overwrite(
+            Path("history.ed"), [_.original_text for _ in self.history], self.preferred_line_break
+        )
 
     def final_report(self) -> None:
         """Print out the final report"""
         self.feedback(f"History saved to {self.history_log.history_file_string}")
 
-    def save_on_crash(self, type: Optional[Exception], value: Any, tb: Any) -> None:
+    def save_on_crash(self, exception_type: Optional[Exception], value: Any, tb: Any) -> None:
         """Save the document to the file"""
         self.save_document()
-        raise type
+        raise exception_type
```

### Comparing `dedlin-1.12.0/dedlin/parsers.py` & `dedlin-1.13.0/dedlin/parsers.py`

 * *Files 5% similar despite different names*

```diff
@@ -35,15 +35,15 @@
         repeat = try_parse_int(parts[2]) if len(parts) > 2 else 1
 
         if start == 1 and end == 0:
             end = 1 if document_length == 0 else document_length
 
         # TODO: need better parser errors
         if start is None or end is None or repeat is None:
-            logger.warning(f"Range invalid:{value}")
+            logger.warning(f"Range invalid:{value}. start:{start}, end:{end}, repeat:{repeat}")
             return None
 
         candidate = LineRange(start=start, offset=end - start, repeat=repeat)
 
         # TODO: need better parser errors
         if not candidate.validate():
             logger.warning(f"Candidate invalid: {candidate}")
@@ -120,14 +120,28 @@
     Commands.HISTORY: ("HISTORY",),
     Commands.MACRO: ("MACRO",),
     Commands.BROWSE: ("BROWSE",),
     Commands.CURRENT: ("CURRENT",),
     Commands.SHUFFLE: ("SHUFFLE",),
     Commands.SORT: ("SORT",),
     Commands.REVERSE: ("REVERSE",),
+    # String Commands
+    Commands.TITLE: ("TITLE",),
+    Commands.SWAPCASE: ("SWAPCASE",),
+    Commands.CASEFOLD: ("CASEFOLD",),
+    Commands.CAPITALIZE: ("CAPITALIZE",),
+    Commands.UPPER: ("UPPER",),
+    Commands.LOWER: ("LOWER",),
+    Commands.EXPANDTABS: ("EXPANDTABS",),
+    Commands.RJUST: ("RJUST",),
+    Commands.LJUST: ("LJUST",),
+    Commands.CENTER: ("CENTER",),
+    Commands.RSTRIP: ("RSTRIP",),
+    Commands.LSTRIP: ("LSTRIP",),
+    Commands.STRIP: ("STRIP",),
 }
 
 
 def parse_range_only(
     just_command: str,
     front_part: str,
     original_text: str,
@@ -161,14 +175,15 @@
     Commands.COPY: ("COPY",),  # 1 phrase
     Commands.MOVE: ("MOVE",),  # 1 phrase
     Commands.SEARCH: ("S", "SEARCH"),  # 1 phrase
     Commands.REPLACE: ("R", "REPLACE"),  # 2 phrases
     Commands.HELP: ("HELP",),
     Commands.PUSH: ("PUSH",),
     Commands.CRASH: ("CRASH",),
+    Commands.EXPORT: ("EXPORT",),
 }
 
 
 def parse_search_replace(
     front_part: str, phrases: Optional[Phrases], original_text: str, current_line: int, document_length: int
 ) -> Optional[Command]:
     """Parse a command that has a line range and phrases"""
@@ -262,15 +277,15 @@
     just_command_chars = []
     alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
     for char in command:
         if char in alphabet and not found_first_alpha:
             found_first_alpha = True
         if found_first_alpha and char in alphabet:
             just_command_chars.append(char)
-        if found_first_alpha and not char in alphabet:
+        if found_first_alpha and char not in alphabet:
             break
         front_part_chars.append(char)
 
     front_part = "".join(front_part_chars)
     just_command = "".join(just_command_chars)
     location_of_command = original_text_upper.find(just_command)
```

### Comparing `dedlin-1.12.0/dedlin/pygments_code.py` & `dedlin-1.13.0/dedlin/pygments_code.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/rich_output.py` & `dedlin-1.13.0/dedlin/outputters/rich_output.py`

 * *Files 10% similar despite different names*

```diff
@@ -10,16 +10,25 @@
 
     def __init__(self) -> None:
         """Set up initial state"""
         self.console = Console()
 
     def print(self, text: str, end: Optional[str]) -> None:
         """Syntax highlighting"""
+        text = "" if text is None else text
         if text and text.endswith("\n"):
             text = text[:-1]
         syntax = Syntax(
             text,
             "python",
             # theme="monokai",
             line_numbers=False,
         )
         self.console.print(syntax, end=end)
+
+
+rich_printer = RichPrinter()
+
+
+def printer(text: Optional[str], end: str = "\n") -> None:
+    text = "" if text is None else text
+    rich_printer.print(text, end="")
```

### Comparing `dedlin-1.12.0/dedlin/spelling_overlay.py` & `dedlin-1.13.0/dedlin/tools/spelling_overlay.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,11 +11,11 @@
     Add a 'did you mean' suggestion to each incorrect word
     """
     # find those words that may be misspelled
     misspelled = spell.unknown(spell.split_words(line))
     new_line = line
     for word in misspelled:
         correction = spell.correction(word)
-        if correction != word:
+        if correction != word and correction:
             replacement = f"{word} (did you mean {correction}?)"
             new_line = new_line.replace(word, replacement)
     return new_line
```

### Comparing `dedlin-1.12.0/dedlin/web.py` & `dedlin-1.13.0/dedlin/tools/web.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/dedlin/web_api.py` & `dedlin-1.13.0/dedlin/web_api.py`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/LICENSE` & `dedlin-1.13.0/LICENSE`

 * *Files identical despite different names*

### Comparing `dedlin-1.12.0/pyproject.toml` & `dedlin-1.13.0/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dedlin"
-version = "1.12.0"
+version = "1.13.0"
 description = "Line editor, edlin clone with many improvements"
 authors = ["Matthew Martin <matthewdeanmartin@gmail.com>"]
 keywords = ["editor", "edlin", "line editor",]
 classifiers = [
     "Development Status :: 3 - Alpha",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
@@ -58,14 +58,20 @@
 # browser
 html2text = "*"
 requests = "*"
 
 # ascii art/fonts
 art = "*"
 
+# Accessibilty
+pyttsx3 = "*"
+
+# printer support
+mistune = "*"
+
 # web api
 fastapi = { version = "*", optional = true }
 uvicorn = { version = "*", optional = true }
 
 [tool.poetry.extras]
 webapi = ["fastapi","uvicorn"]
 
@@ -120,7 +126,49 @@
 default_section = "THIRDPARTY"
 force_grid_wrap = 0
 include_trailing_comma = true
 known_first_party = ["dedlin"]
 line_length = 88
 multi_line_output = 3
 use_parentheses = true
+
+[tool.ruff]
+line-length = 1000
+
+# Enable Pyflakes `E` and `F` codes by default.
+select = ["E", "F"]
+ignore = [
+    "E722",
+    "E501",
+]
+
+# Exclude a variety of commonly ignored directories.
+exclude = [
+    "dead_code",
+    ".bzr",
+    ".direnv",
+    ".eggs",
+    ".git",
+    ".hg",
+    ".mypy_cache",
+    ".nox",
+    ".pants.d",
+    ".ruff_cache",
+    ".svn",
+    ".tox",
+    ".venv",
+    "__pypackages__",
+    "_build",
+    "buck-out",
+    "build",
+    "dist",
+    "node_modules",
+    "venv",
+    "hide"
+]
+per-file-ignores = { }
+
+# Allow unused variables when underscore-prefixed.
+dummy-variable-rgx = "^(_+|(_+[a-zA-Z0-9_]*[a-zA-Z0-9]+?))$"
+
+# Assume Python 3.10.
+target-version = "py311"
```

### Comparing `dedlin-1.12.0/README.md` & `dedlin-1.13.0/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -1,32 +1,53 @@
 # dedlin
 
 Dedlin is an interactive line-by-line text editor and a DSL. Line editors
 suck, but they are easy to write and the DSL is mildly interesting.
 
-This is not intended to be backwards compatible with anything. I have made
-changes to make the app less user hostile, but there is a `--vim_mode`
+While this is a clone of [edlin](https://en.wikipedia.org/wiki/Edlin), this is not intended to be backwards compatible
+with anything. I have made changes to make the app less user hostile, but there is a `--vim_mode`
 where all help, warnings, feedback will be suppressed.
 
+## Badges
+
+![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/pypi/dedlin)
+
+[![Downloads](https://static.pepy.tech/personalized-badge/dedlin?period=month&units=international_system&left_color=black&right_color=orange&left_text=Downloads)](https://pepy.tech/project/dedlin)
+
+[![CodeFactor](https://www.codefactor.io/repository/github/matthewdeanmartin/dedlin/badge)](https://www.codefactor.io/repository/github/matthewdeanmartin/dedlin)
 
 ## Installation
 
 Requires python 3.11 or higher. Someday I'll write a standalone installer for it.
 
+Install globally in an isolated virtual environment. This is a good idea.
+
 ```bash
-pip install dedlin
+pipx install dedlin
+```
+
+Run pre-built image with docker. Painful, but you're using an edlin clone, so that is what you're looking for.
+
+```powershell
+# This is should work in powershell or linux bash. Not windows git-bash.
+docker run --rm -it -v "${PWD}/:/app"  ghcr.io/matthewdeanmartin/dedlin:latest file.txt
 ```
 
 ## Usage
+
 Launch and edit file_name.txt
+
+If you installed with `pip` or `pipx`
+
 ```bash
-python -m dedlin file_name.txt
+dedlin file_name.txt
 ```
 
 Command line help
+
 ```
 > python -m dedlin --help
 Dedlin.
 
 An improved version of the edlin.
 
 Usage:
@@ -39,17 +60,19 @@
   --version          Show version.
   --macro=<macro>    Run macro file.
   --echo             Echo commands.
   --halt_on_error    End program on error.
   --promptless_quit  Skip prompt on quit.
   --vim_mode         User hostile, no feedback.
   --verbose          Displaying all debugging info.
+  --blind_mode       Optimize for blind users (experimental).
 ```
 
 Sample session
+
 ```
    _          _  _  _
  __| | ___  __| || |(_) _ _
 / _` |/ -_)/ _` || || || ' \
 \__,_|\___|\__,_||_||_||_||_|
 
 
@@ -79,12 +102,12 @@
    5 : ghost peppers
    6 : tortillas
 
 ? * EXIT
 1,6 EXIT
 ```
 
-
 # Documentation
+
 - [User Manual](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/user_manual.md)
 - [Developer roadmap](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/TODO.md)
 - [Prior Art](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/prior_art.md)
```

### Comparing `dedlin-1.12.0/PKG-INFO` & `dedlin-1.13.0/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dedlin
-Version: 1.12.0
+Version: 1.13.0
 Summary: Line editor, edlin clone with many improvements
 Home-page: https://github.com/matthewdeanmartin/dedlin
 License: MIT
 Keywords: editor,edlin,line editor
 Author: Matthew Martin
 Author-email: matthewdeanmartin@gmail.com
 Requires-Python: >=3.11,<4.0
@@ -18,17 +18,19 @@
 Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: webapi
 Requires-Dist: art
 Requires-Dist: docopt-ng
 Requires-Dist: fastapi ; extra == "webapi"
 Requires-Dist: html2text
 Requires-Dist: icontract
+Requires-Dist: mistune
 Requires-Dist: pydantic
 Requires-Dist: pygments
 Requires-Dist: pyspellchecker
+Requires-Dist: pyttsx3
 Requires-Dist: pywin32 ; sys_platform == "win32"
 Requires-Dist: questionary
 Requires-Dist: requests
 Requires-Dist: rich
 Requires-Dist: textstat
 Requires-Dist: uvicorn ; extra == "webapi"
 Project-URL: Bug Tracker, https://github.com/matthewdeanmartin/dedlin/issues
@@ -38,34 +40,55 @@
 Description-Content-Type: text/markdown
 
 # dedlin
 
 Dedlin is an interactive line-by-line text editor and a DSL. Line editors
 suck, but they are easy to write and the DSL is mildly interesting.
 
-This is not intended to be backwards compatible with anything. I have made
-changes to make the app less user hostile, but there is a `--vim_mode`
+While this is a clone of [edlin](https://en.wikipedia.org/wiki/Edlin), this is not intended to be backwards compatible
+with anything. I have made changes to make the app less user hostile, but there is a `--vim_mode`
 where all help, warnings, feedback will be suppressed.
 
+## Badges
+
+![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/pypi/dedlin)
+
+[![Downloads](https://static.pepy.tech/personalized-badge/dedlin?period=month&units=international_system&left_color=black&right_color=orange&left_text=Downloads)](https://pepy.tech/project/dedlin)
+
+[![CodeFactor](https://www.codefactor.io/repository/github/matthewdeanmartin/dedlin/badge)](https://www.codefactor.io/repository/github/matthewdeanmartin/dedlin)
 
 ## Installation
 
 Requires python 3.11 or higher. Someday I'll write a standalone installer for it.
 
+Install globally in an isolated virtual environment. This is a good idea.
+
 ```bash
-pip install dedlin
+pipx install dedlin
+```
+
+Run pre-built image with docker. Painful, but you're using an edlin clone, so that is what you're looking for.
+
+```powershell
+# This is should work in powershell or linux bash. Not windows git-bash.
+docker run --rm -it -v "${PWD}/:/app"  ghcr.io/matthewdeanmartin/dedlin:latest file.txt
 ```
 
 ## Usage
+
 Launch and edit file_name.txt
+
+If you installed with `pip` or `pipx`
+
 ```bash
-python -m dedlin file_name.txt
+dedlin file_name.txt
 ```
 
 Command line help
+
 ```
 > python -m dedlin --help
 Dedlin.
 
 An improved version of the edlin.
 
 Usage:
@@ -78,17 +101,19 @@
   --version          Show version.
   --macro=<macro>    Run macro file.
   --echo             Echo commands.
   --halt_on_error    End program on error.
   --promptless_quit  Skip prompt on quit.
   --vim_mode         User hostile, no feedback.
   --verbose          Displaying all debugging info.
+  --blind_mode       Optimize for blind users (experimental).
 ```
 
 Sample session
+
 ```
    _          _  _  _
  __| | ___  __| || |(_) _ _
 / _` |/ -_)/ _` || || || ' \
 \__,_|\___|\__,_||_||_||_||_|
 
 
@@ -118,13 +143,13 @@
    5 : ghost peppers
    6 : tortillas
 
 ? * EXIT
 1,6 EXIT
 ```
 
-
 # Documentation
+
 - [User Manual](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/user_manual.md)
 - [Developer roadmap](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/TODO.md)
 - [Prior Art](https://github.com/matthewdeanmartin/dedlin/blob/main/docs/prior_art.md)
```

