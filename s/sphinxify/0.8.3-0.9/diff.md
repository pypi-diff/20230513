# Comparing `tmp/sphinxify-0.8.3.tar.gz` & `tmp/sphinxify-0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sphinxify-0.8.3.tar", last modified: Sun Feb 28 06:15:14 2021, max compression
+gzip compressed data, was "sphinxify-0.9.tar", last modified: Tue Mar 15 13:08:02 2022, max compression
```

## Comparing `sphinxify-0.8.3.tar` & `sphinxify-0.9.tar`

### file list

```diff
@@ -1,19 +1,25 @@
--rw-r--r--   0        0        0     1602 2021-02-28 06:15:10.890588 sphinxify-0.8.3/.github/workflows/pythonpackage.yml
--rw-r--r--   0        0        0     1187 2021-02-28 06:15:10.890588 sphinxify-0.8.3/.gitignore
--rw-r--r--   0        0        0     1549 2021-02-28 06:15:10.890588 sphinxify-0.8.3/LICENSE
--rw-r--r--   0        0        0      692 2021-02-28 06:15:10.890588 sphinxify-0.8.3/README.md
--rw-r--r--   0        0        0      899 2021-02-28 06:15:10.890588 sphinxify-0.8.3/pyproject.toml
--rwxr-xr-x   0        0        0    10948 2021-02-28 06:15:10.890588 sphinxify-0.8.3/sphinxify.py
--rw-r--r--   0        0        0       38 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/expected/enum_inline.txt
--rw-r--r--   0        0        0      170 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/expected/html_whitespace.txt
--rw-r--r--   0        0        0       32 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/expected/multiple_single_line.txt
--rw-r--r--   0        0        0      437 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/expected/param_no_indent.txt
--rw-r--r--   0        0        0      141 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/expected/tag_soup.txt
--rw-r--r--   0        0        0       46 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/input/enum_inline.txt
--rw-r--r--   0        0        0      212 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/input/html_whitespace.txt
--rw-r--r--   0        0        0       40 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/input/multiple_single_line.txt
--rw-r--r--   0        0        0      436 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/input/param_no_indent.txt
--rw-r--r--   0        0        0      183 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/input/tag_soup.txt
--rwxr-xr-x   0        0        0      158 2021-02-28 06:15:10.890588 sphinxify-0.8.3/tests/test.sh
--rw-r--r--   0        0        0      622 1970-01-01 00:00:00.000000 sphinxify-0.8.3/setup.py
--rw-r--r--   0        0        0      200 1970-01-01 00:00:00.000000 sphinxify-0.8.3/PKG-INFO
+-rw-r--r--   0        0        0     1376 2022-03-15 13:07:57.046063 sphinxify-0.9/.github/workflows/pythonpackage.yml
+-rw-r--r--   0        0        0     1187 2022-03-15 13:07:57.046063 sphinxify-0.9/.gitignore
+-rw-r--r--   0        0        0      726 2022-03-15 13:07:57.046063 sphinxify-0.9/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1549 2022-03-15 13:07:57.046063 sphinxify-0.9/LICENSE
+-rw-r--r--   0        0        0      692 2022-03-15 13:07:57.046063 sphinxify-0.9/README.md
+-rw-r--r--   0        0        0      899 2022-03-15 13:07:57.046063 sphinxify-0.9/pyproject.toml
+-rwxr-xr-x   0        0        0    10997 2022-03-15 13:07:57.046063 sphinxify-0.9/sphinxify.py
+-rw-r--r--   0        0        0       38 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/enum_inline.txt
+-rw-r--r--   0        0        0      170 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/html_whitespace.txt
+-rw-r--r--   0        0        0       32 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/multiple_single_line.txt
+-rw-r--r--   0        0        0      437 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/param_no_indent.txt
+-rw-r--r--   0        0        0       49 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/snake_case_words.txt
+-rw-r--r--   0        0        0      141 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/tag_soup.txt
+-rw-r--r--   0        0        0       50 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/trailing_underscores.txt
+-rw-r--r--   0        0        0       29 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/expected/underscore_word.txt
+-rw-r--r--   0        0        0       46 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/enum_inline.txt
+-rw-r--r--   0        0        0      212 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/html_whitespace.txt
+-rw-r--r--   0        0        0       40 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/multiple_single_line.txt
+-rw-r--r--   0        0        0      436 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/param_no_indent.txt
+-rw-r--r--   0        0        0       49 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/snake_case_words.txt
+-rw-r--r--   0        0        0      183 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/tag_soup.txt
+-rw-r--r--   0        0        0       49 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/trailing_underscores.txt
+-rw-r--r--   0        0        0       29 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/input/underscore_word.txt
+-rwxr-xr-x   0        0        0      158 2022-03-15 13:07:57.046063 sphinxify-0.9/tests/test.sh
+-rw-r--r--   0        0        0     1563 1970-01-01 00:00:00.000000 sphinxify-0.9/PKG-INFO
```

### Comparing `sphinxify-0.8.3/.github/workflows/pythonpackage.yml` & `sphinxify-0.9/.github/workflows/pythonpackage.yml`

 * *Files 6% similar despite different names*

```diff
@@ -4,37 +4,31 @@
 jobs:
   check:
     runs-on: ubuntu-latest
 
     steps:
     - uses: actions/checkout@v2
     - uses: actions/setup-python@v2
-    - name: Lint with flake8
-      run: |
-        pip install flake8 flake8-bugbear
-        flake8 . --count --select=E9,F,B,B9 --show-source --statistics
     - name: Type check with mypy
       uses: tsuyoshicho/action-mypy@v3
       with:
         github_token: ${{ secrets.GITHUB_TOKEN }}
         reporter: github-check
-    - name: Check formatting with black
-      uses: psf/black@stable
 
   test:
     runs-on: ubuntu-latest
     strategy:
       max-parallel: 4
       matrix:
         python-version:
           - 3.6
           - 3.7
           - 3.8
           - 3.9
-          - 3.10-dev
+          - '3.10'
 
     steps:
     - uses: actions/checkout@v2
     - name: Set up Python ${{ matrix.python-version }}
       uses: actions/setup-python@v2
       with:
         python-version: ${{ matrix.python-version }}
```

### Comparing `sphinxify-0.8.3/.gitignore` & `sphinxify-0.9/.gitignore`

 * *Files identical despite different names*

### Comparing `sphinxify-0.8.3/LICENSE` & `sphinxify-0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `sphinxify-0.8.3/README.md` & `sphinxify-0.9/README.md`

 * *Files identical despite different names*

### Comparing `sphinxify-0.8.3/pyproject.toml` & `sphinxify-0.9/pyproject.toml`

 * *Files identical despite different names*

### Comparing `sphinxify-0.8.3/sphinxify.py` & `sphinxify-0.9/sphinxify.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 import collections
 import re
 import sys
 import textwrap
 from dataclasses import dataclass
 from typing import Callable, List, Optional
 
-__version__ = "0.8.3"
+__version__ = "0.9"
 
 FIND_FUNC_RE = r"(.*)\n\s*((?:(?:public|protected|private|static|final|synchronized|abstract|default|native)\s+)+)(?:([\w<>[\]]+)\s+)?(\w+)\s*\(([^)]*)\)"
 
 TYPE_MAPPING = {
     "ArrayList": "List",
     "<": "[",
     ">": "]",
@@ -165,22 +165,24 @@
             for tag, inline, role in (
                 ("b", "**", "strong"),
                 ("strong", "**", "strong"),
                 ("i", "*", "emphasis"),
                 ("em", "*", "emphasis"),
             ):
                 if line.count(f"<{tag}>") == line.count(f"</{tag}>"):
-                    line = re.sub(fr"</?{tag}>", inline, line)
+                    line = re.sub(rf"</?{tag}>", inline, line)
                 else:
                     line = line.replace(f"<{tag}>", f":{role}:`")
                     line = line.replace(f"</{tag}>", "`")
 
             line = line.replace("<sub>", ":sub:`").replace("</sub>", "`")
             line = line.replace("<sup>", ":sup:`").replace("</sup>", "`")
 
+            line = re.sub(r"\B_\b", r"\\_", line)
+
             line = line.strip()
 
             current_lines.append(line)
 
         text = "\n".join(desc_lines).strip()
         text = re.sub("\n{2,}", "\n\n", text)
```

