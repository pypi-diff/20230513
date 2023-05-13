# Comparing `tmp/hledger_args-0.0.5.tar.gz` & `tmp/hledger_args-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hledger_args-0.0.5.tar", last modified: Thu May 11 02:16:36 2023, max compression
+gzip compressed data, was "hledger_args-0.0.6.tar", last modified: Sat May 13 15:27:11 2023, max compression
```

## Comparing `hledger_args-0.0.5.tar` & `hledger_args-0.0.6.tar`

### file list

```diff
@@ -1,38 +1,39 @@
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.423049 hledger_args-0.0.5/
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4504 2023-05-11 02:16:36.423049 hledger_args-0.0.5/PKG-INFO
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4164 2023-05-11 02:06:47.000000 hledger_args-0.0.5/README.md
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.415049 hledger_args-0.0.5/docs/
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4164 2023-05-11 02:06:47.000000 hledger_args-0.0.5/docs/README.md
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.417049 hledger_args-0.0.5/hledger_args/
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)        0 2023-05-09 16:42:28.000000 hledger_args-0.0.5/hledger_args/__init__.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)       84 2023-05-09 19:53:32.000000 hledger_args-0.0.5/hledger_args/__main__.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1288 2023-05-09 16:59:35.000000 hledger_args-0.0.5/hledger_args/base_args.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1199 2023-05-09 16:57:24.000000 hledger_args-0.0.5/hledger_args/batch_args.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     3132 2023-05-11 02:12:14.000000 hledger_args-0.0.5/hledger_args/cli.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4684 2023-05-11 02:15:32.000000 hledger_args-0.0.5/hledger_args/inter_args.py
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     3115 2023-05-09 16:55:37.000000 hledger_args-0.0.5/hledger_args/options.py
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.418049 hledger_args-0.0.5/hledger_args.egg-info/
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4504 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/PKG-INFO
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)      718 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/SOURCES.txt
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)        1 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/dependency_links.txt
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)       60 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/entry_points.txt
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)       29 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/requires.txt
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)       40 2023-05-11 02:16:36.000000 hledger_args-0.0.5/hledger_args.egg-info/top_level.txt
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1152 2023-05-11 02:14:53.000000 hledger_args-0.0.5/pyproject.toml
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)       38 2023-05-11 02:16:36.424049 hledger_args-0.0.5/setup.cfg
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.418049 hledger_args-0.0.5/tests/
--rw-r--r--   0 eduardo   (1000) eduardo   (1000)        0 2023-05-09 16:42:22.000000 hledger_args-0.0.5/tests/__init__.py
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.415049 hledger_args-0.0.5/venv/
-drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-11 02:16:36.423049 hledger_args-0.0.5/venv/bin/
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      627 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2html.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      749 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2html4.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)     1094 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2html5.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      826 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2latex.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      649 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2man.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      815 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2odt.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)     1753 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2odt_prepstyles.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      634 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2pseudoxml.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      670 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2s5.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      906 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2xetex.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      635 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rst2xml.py
--rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      703 2023-05-09 16:48:40.000000 hledger_args-0.0.5/venv/bin/rstpep2html.py
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.354608 hledger_args-0.0.6/
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4504 2023-05-13 15:27:11.354608 hledger_args-0.0.6/PKG-INFO
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4164 2023-05-11 02:06:47.000000 hledger_args-0.0.6/README.md
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.348608 hledger_args-0.0.6/docs/
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4164 2023-05-11 02:06:47.000000 hledger_args-0.0.6/docs/README.md
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.350607 hledger_args-0.0.6/hledger_args/
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)        0 2023-05-09 16:42:28.000000 hledger_args-0.0.6/hledger_args/__init__.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)       84 2023-05-09 19:53:32.000000 hledger_args-0.0.6/hledger_args/__main__.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1288 2023-05-11 14:44:16.000000 hledger_args-0.0.6/hledger_args/base_args.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1396 2023-05-13 15:06:47.000000 hledger_args-0.0.6/hledger_args/batch_args.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     3512 2023-05-13 15:27:04.000000 hledger_args-0.0.6/hledger_args/cli.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4819 2023-05-13 15:05:41.000000 hledger_args-0.0.6/hledger_args/inter_args.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     3115 2023-05-09 16:55:37.000000 hledger_args-0.0.6/hledger_args/options.py
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1203 2023-05-13 15:16:12.000000 hledger_args-0.0.6/hledger_args/output_result.py
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.351608 hledger_args-0.0.6/hledger_args.egg-info/
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     4504 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/PKG-INFO
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)      748 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/SOURCES.txt
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)        1 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/dependency_links.txt
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)       60 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/entry_points.txt
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)       29 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/requires.txt
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)       40 2023-05-13 15:27:11.000000 hledger_args-0.0.6/hledger_args.egg-info/top_level.txt
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)     1152 2023-05-13 15:26:02.000000 hledger_args-0.0.6/pyproject.toml
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)       38 2023-05-13 15:27:11.354608 hledger_args-0.0.6/setup.cfg
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.351608 hledger_args-0.0.6/tests/
+-rw-r--r--   0 eduardo   (1000) eduardo   (1000)        0 2023-05-09 16:42:22.000000 hledger_args-0.0.6/tests/__init__.py
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.347607 hledger_args-0.0.6/venv/
+drwxr-xr-x   0 eduardo   (1000) eduardo   (1000)        0 2023-05-13 15:27:11.353608 hledger_args-0.0.6/venv/bin/
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      627 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2html.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      749 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2html4.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)     1094 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2html5.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      826 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2latex.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      649 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2man.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      815 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2odt.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)     1753 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2odt_prepstyles.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      634 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2pseudoxml.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      670 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2s5.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      906 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2xetex.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      635 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rst2xml.py
+-rwxr-xr-x   0 eduardo   (1000) eduardo   (1000)      703 2023-05-09 16:48:40.000000 hledger_args-0.0.6/venv/bin/rstpep2html.py
```

### Comparing `hledger_args-0.0.5/PKG-INFO` & `hledger_args-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hledger_args
-Version: 0.0.5
+Version: 0.0.6
 License: MIT License
 Project-URL: homepage, https://github.com/edkedk99/hledger-args
 Project-URL: documentation, https://edkedk99.github.io/hledger-args/
 Project-URL: repository, https://github.com/edkedk99/hledger-args
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `hledger_args-0.0.5/README.md` & `hledger_args-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/docs/README.md` & `hledger_args-0.0.6/docs/README.md`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/hledger_args/base_args.py` & `hledger_args-0.0.6/hledger_args/base_args.py`

 * *Files 3% similar despite different names*

```diff
@@ -37,8 +37,8 @@
 
         base_comm = ["hledger", *self.files_comm, *options_list]
         proc = subprocess.run(base_comm, capture_output=True, check=True)
         report = proc.stdout.decode("utf8")
 
         base_comm_str = shlex.join(base_comm)
         print(f"stderr: {base_comm_str}\n", file=sys.stderr)
-        print(report)
+        return report
```

### Comparing `hledger_args-0.0.5/hledger_args/batch_args.py` & `hledger_args-0.0.6/hledger_args/batch_args.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,23 @@
 from typing import Optional, Tuple
 
 from .base_args import BaseArgs
 
 
 class BatchArgs(BaseArgs):
-    def __init__(self, files: Tuple[str, ...]) -> None:
+    def __init__(
+        self,
+        files: Tuple[str, ...],
+        name: Optional[str],
+        hledger_options: Tuple[str, str],
+    ) -> None:
         super().__init__(files)
+        self.name = name
+        self.hledger_options = hledger_options
+        self.report = self.run_batch()
 
     @property
     def available_txt(self):
         text = "Available args\n\n"
 
         text += "No interactive allowed args (Report)\n"
         text += "----------------------------\n"
@@ -19,18 +27,17 @@
         if len(self.has_ask) > 0:
             text += "Interactive-only args (Report)\n"
             text += "------------------------------\n"
             has_ask_str = "\n".join(self.has_ask)
             text += has_ask_str + "\n\n"
         return text
 
-    def run_batch(self, name: Optional[str], hledger_options: Tuple[str, str]):
-        if not name:
-            print(self.available_txt)
-            return
-        elif name not in self.names:
-            raise KeyError(f"{name} not found.\n\n{self.available_txt}")
-        elif name in self.has_ask:
-            raise KeyError(f"{name} is interactive only.\n\n{self.available_txt}")
+    def run_batch(self):
+        if not self.name:
+            return f"Missing command\n\n{self.available_txt}"
+        elif self.name not in self.names:
+            raise KeyError(f"{self.name} not found.\n\n{self.available_txt}")
+        elif self.name in self.has_ask:
+            raise KeyError(f"{self.name} is interactive only.\n\n{self.available_txt}")
         else:
-            options = self.args[name]
-            self.run_args(options, hledger_options)
+            options = self.args[self.name]
+            return self.run_args(options, self.hledger_options)
```

### Comparing `hledger_args-0.0.5/hledger_args/cli.py` & `hledger_args-0.0.6/hledger_args/cli.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,11 +1,13 @@
-from typing import Tuple
+from typing import Optional, Tuple
 
 import rich_click as click
 
+from hledger_args.output_result import output_report
+
 from .batch_args import BatchArgs
 from .inter_args import InteractiveArgs
 
 CONTEXT_SETTINGS = dict(help_option_names=["-h", "--help"])
 
 click.rich_click.USE_MARKDOWN = True
 click.rich_click.SHOW_ARGUMENTS = True
@@ -34,18 +36,35 @@
 @click.option(
     "-i",
     "--interactive",
     is_flag=True,
     required=False,
     help="Run in interactive mode by answering the prompts. [NAME] and [EXTRA_HLEDGER_OPTIONS] are not used in this mode.",
 )
+@click.option(
+    "-d",
+    "--pdf-dir",
+    type=click.Path(
+        file_okay=False,
+        dir_okay=True,
+    ),
+    required=False,
+)
+@click.option(
+    "-o", "--pdf-file", type=click.Path(file_okay=True, dir_okay=False), required=False
+)
 @click.argument("name", type=click.STRING, required=False)
 @click.argument("extra_hledger_options", nargs=-1)
 def cli(
-    file: str, interactive: bool, name: str, extra_hledger_options: Tuple[str, ...]
+    file: str,
+    interactive: bool,
+    name: str,
+    extra_hledger_options: Tuple[str, ...],
+    pdf_dir: Optional[str],
+    pdf_file: Optional[str],
 ):
     """
      ---
 
      **NAME**: Command name to run saved in the journal sub directives. Not available in Interactive mode
 
     **EXTRA_HLEDGER_OPTIONS**: Extra options to send to hledger command. Not available in Interactive mode.
@@ -73,11 +92,11 @@
      #+args buy_aapl:bal desc:\"Buy AAPL\"
      #+args aapl_cur:bal desc:\"Buy AAPL\" cur:{commodity}
     ```
     """
 
     if interactive:
         args = InteractiveArgs((file,))
-        args.menu()
     else:
-        args = BatchArgs((file,))
-        args.run_batch(name, extra_hledger_options)
+        args = BatchArgs((file,), name, extra_hledger_options)
+
+    output_report(args, pdf_dir, pdf_file)
```

### Comparing `hledger_args-0.0.5/hledger_args/inter_args.py` & `hledger_args-0.0.6/hledger_args/inter_args.py`

 * *Files 4% similar despite different names*

```diff
@@ -36,14 +36,16 @@
     )
     return question
 
 
 class InteractiveArgs(BaseArgs):
     def __init__(self, files: Tuple[str, ...]) -> None:
         super().__init__(files)
+        self.name = self.menu()
+        self.report = self.get_report()
 
     def ask_placeholder(self, placeholder: str) -> str:
         if placeholder == "account":
             choices = self.get_hledger_lines(["accounts"])
             answer = custom_autocomplete(placeholder, choices).ask()
         elif placeholder == "tag":
             tags = self.get_hledger_lines(["tags"])
@@ -116,18 +118,20 @@
         base_comm = ["hledger", *self.files_comm, *cmds]
         proc = subprocess.run(base_comm, capture_output=True, check=True)
         report = proc.stdout.decode("utf8")
         report_list = [line for line in report.split("\n") if line != ""]
         return report_list
 
     def menu(self):
-        name = questionary.select(
+        name: str = questionary.select(
             "Choose report",
             choices=list(self.names),
             use_shortcuts=True,
             use_indicator=False,
             show_selected=False,
         ).ask()
+        return name
 
-        options_str = self.args[name]
+    def get_report(self):
+        options_str = self.args[self.name]
         replaced = self.replace_options(options_str)
-        self.run_args(replaced)
+        return self.run_args(replaced)
```

### Comparing `hledger_args-0.0.5/hledger_args/options.py` & `hledger_args-0.0.6/hledger_args/options.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/hledger_args.egg-info/PKG-INFO` & `hledger_args-0.0.6/hledger_args.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hledger-args
-Version: 0.0.5
+Version: 0.0.6
 License: MIT License
 Project-URL: homepage, https://github.com/edkedk99/hledger-args
 Project-URL: documentation, https://edkedk99.github.io/hledger-args/
 Project-URL: repository, https://github.com/edkedk99/hledger-args
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `hledger_args-0.0.5/hledger_args.egg-info/SOURCES.txt` & `hledger_args-0.0.6/hledger_args.egg-info/SOURCES.txt`

 * *Files 8% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 hledger_args/__init__.py
 hledger_args/__main__.py
 hledger_args/base_args.py
 hledger_args/batch_args.py
 hledger_args/cli.py
 hledger_args/inter_args.py
 hledger_args/options.py
+hledger_args/output_result.py
 hledger_args.egg-info/PKG-INFO
 hledger_args.egg-info/SOURCES.txt
 hledger_args.egg-info/dependency_links.txt
 hledger_args.egg-info/entry_points.txt
 hledger_args.egg-info/requires.txt
 hledger_args.egg-info/top_level.txt
 tests/__init__.py
```

### Comparing `hledger_args-0.0.5/pyproject.toml` & `hledger_args-0.0.6/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 keyword = ["hledger","PTA", "investments", "accounting"]
 classifiers = [""]
 author = "Eduardo"
 author_email = "edkedk99@hotmail.com"
 
 [project]
 name = "hledger_args"
-version = "0.0.5"
+version = "0.0.6"
 readme= "docs/README.md"
 requires-python = ">=3.8"
 license = {text = "MIT License"}
 dependencies = [
 	     "click",
 	     "rich_click",
 	     "questionary"
```

### Comparing `hledger_args-0.0.5/venv/bin/rst2html.py` & `hledger_args-0.0.6/venv/bin/rst2html.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2html4.py` & `hledger_args-0.0.6/venv/bin/rst2html4.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2html5.py` & `hledger_args-0.0.6/venv/bin/rst2html5.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2latex.py` & `hledger_args-0.0.6/venv/bin/rst2latex.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2man.py` & `hledger_args-0.0.6/venv/bin/rst2man.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2odt.py` & `hledger_args-0.0.6/venv/bin/rst2odt.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2odt_prepstyles.py` & `hledger_args-0.0.6/venv/bin/rst2odt_prepstyles.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2pseudoxml.py` & `hledger_args-0.0.6/venv/bin/rst2pseudoxml.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2s5.py` & `hledger_args-0.0.6/venv/bin/rst2s5.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2xetex.py` & `hledger_args-0.0.6/venv/bin/rst2xetex.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rst2xml.py` & `hledger_args-0.0.6/venv/bin/rst2xml.py`

 * *Files identical despite different names*

### Comparing `hledger_args-0.0.5/venv/bin/rstpep2html.py` & `hledger_args-0.0.6/venv/bin/rstpep2html.py`

 * *Files identical despite different names*

