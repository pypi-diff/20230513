# Comparing `tmp/dasosdemo-0.0.1.tar.gz` & `tmp/dasosdemo-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dasosdemo-0.0.1.tar", last modified: Fri May  5 20:16:16 2023, max compression
+gzip compressed data, was "dasosdemo-0.0.2.tar", last modified: Sat May 13 17:02:44 2023, max compression
```

## Comparing `dasosdemo-0.0.1.tar` & `dasosdemo-0.0.2.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-05-05 20:16:16.977822 dasosdemo-0.0.1/
--rw-rw-rw-   0        0        0     1103 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/LICENSE
--rw-rw-rw-   0        0        0      129 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/MANIFEST.in
--rw-rw-rw-   0        0        0     1136 2023-05-05 20:16:16.977822 dasosdemo-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      390 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-05 20:16:16.962195 dasosdemo-0.0.1/dasosdemo/
--rw-rw-rw-   0        0        0      154 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/dasosdemo/__init__.py
--rw-rw-rw-   0        0        0      194 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/dasosdemo/common.py
--rw-rw-rw-   0        0        0       20 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/dasosdemo/dasosdemo.py
-drwxrwxrwx   0        0        0        0 2023-05-05 20:16:16.977822 dasosdemo-0.0.1/dasosdemo.egg-info/
--rw-rw-rw-   0        0        0     1136 2023-05-05 20:16:15.000000 dasosdemo-0.0.1/dasosdemo.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      294 2023-05-05 20:16:15.000000 dasosdemo-0.0.1/dasosdemo.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-05 20:16:15.000000 dasosdemo-0.0.1/dasosdemo.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-05-05 20:16:15.000000 dasosdemo-0.0.1/dasosdemo.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       10 2023-05-05 20:16:15.000000 dasosdemo-0.0.1/dasosdemo.egg-info/top_level.txt
--rw-rw-rw-   0        0        0        0 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/requirements.txt
--rw-rw-rw-   0        0        0      417 2023-05-05 20:16:16.977822 dasosdemo-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1765 2023-05-05 19:00:58.000000 dasosdemo-0.0.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:02:44.685121 dasosdemo-0.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-05-13 17:02:44.685121 dasosdemo-0.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      373 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:02:44.685121 dasosdemo-0.0.2/dasosdemo/
+-rw-r--r--   0 runner    (1001) docker     (123)      149 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/dasosdemo/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      188 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/dasosdemo/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/dasosdemo/dasosdemo.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:02:44.685121 dasosdemo-0.0.2/dasosdemo.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1098 2023-05-13 17:02:44.000000 dasosdemo-0.0.2/dasosdemo.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-05-13 17:02:44.000000 dasosdemo-0.0.2/dasosdemo.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:02:44.000000 dasosdemo-0.0.2/dasosdemo.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:02:44.000000 dasosdemo-0.0.2/dasosdemo.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-13 17:02:44.000000 dasosdemo-0.0.2/dasosdemo.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      392 2023-05-13 17:02:44.685121 dasosdemo-0.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1708 2023-05-13 17:02:34.000000 dasosdemo-0.0.2/setup.py
```

### Comparing `dasosdemo-0.0.1/LICENSE` & `dasosdemo-0.0.2/LICENSE`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,22 +1,22 @@
-MIT License
-
-Copyright (c) 2023, Christoforos Karanikas
-
-Permission is hereby granted, free of charge, to any person obtaining a copy
-of this software and associated documentation files (the "Software"), to deal
-in the Software without restriction, including without limitation the rights
-to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-copies of the Software, and to permit persons to whom the Software is
-furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all
-copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
-SOFTWARE.
-
+MIT License
+
+Copyright (c) 2023, Christoforos Karanikas
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
+
```

### Comparing `dasosdemo-0.0.1/PKG-INFO` & `dasosdemo-0.0.2/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,38 +1,38 @@
-Metadata-Version: 2.1
-Name: dasosdemo
-Version: 0.0.1
-Summary: My first Python package.
-Home-page: https://github.com/kriskaran/dasosdemo
-Author: Christoforos Karanikas
-Author-email: christoforoskaranikas@yahoo.gr
-License: MIT license
-Keywords: dasosdemo
-Classifier: Intended Audience :: Developers
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.8
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-# dasosdemo
-
-
-[![image](https://img.shields.io/pypi/v/dasosdemo.svg)](https://pypi.python.org/pypi/dasosdemo)
-[![image](https://img.shields.io/conda/vn/conda-forge/dasosdemo.svg)](https://anaconda.org/conda-forge/dasosdemo)
-
-
-**My first Python package.**
-
-
--   Free software: MIT license
--   Documentation: https://kriskaran.github.io/dasosdemo
-    
-
-## Features
-
--   TODO
+Metadata-Version: 2.1
+Name: dasosdemo
+Version: 0.0.2
+Summary: My first Python package.
+Home-page: https://github.com/kriskaran/dasosdemo
+Author: Christoforos Karanikas
+Author-email: christoforoskaranikas@yahoo.gr
+License: MIT license
+Keywords: dasosdemo
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Python: >=3.8
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+# dasosdemo
+
+
+[![image](https://img.shields.io/pypi/v/dasosdemo.svg)](https://pypi.python.org/pypi/dasosdemo)
+[![image](https://img.shields.io/conda/vn/conda-forge/dasosdemo.svg)](https://anaconda.org/conda-forge/dasosdemo)
+
+
+**My first Python package.**
+
+
+-   Free software: MIT license
+-   Documentation: https://kriskaran.github.io/dasosdemo
+    
+
+## Features
+
+-   TODO
```

### Comparing `dasosdemo-0.0.1/dasosdemo.egg-info/PKG-INFO` & `dasosdemo-0.0.2/dasosdemo.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,38 +1,38 @@
-Metadata-Version: 2.1
-Name: dasosdemo
-Version: 0.0.1
-Summary: My first Python package.
-Home-page: https://github.com/kriskaran/dasosdemo
-Author: Christoforos Karanikas
-Author-email: christoforoskaranikas@yahoo.gr
-License: MIT license
-Keywords: dasosdemo
-Classifier: Intended Audience :: Developers
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.8
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-# dasosdemo
-
-
-[![image](https://img.shields.io/pypi/v/dasosdemo.svg)](https://pypi.python.org/pypi/dasosdemo)
-[![image](https://img.shields.io/conda/vn/conda-forge/dasosdemo.svg)](https://anaconda.org/conda-forge/dasosdemo)
-
-
-**My first Python package.**
-
-
--   Free software: MIT license
--   Documentation: https://kriskaran.github.io/dasosdemo
-    
-
-## Features
-
--   TODO
+Metadata-Version: 2.1
+Name: dasosdemo
+Version: 0.0.2
+Summary: My first Python package.
+Home-page: https://github.com/kriskaran/dasosdemo
+Author: Christoforos Karanikas
+Author-email: christoforoskaranikas@yahoo.gr
+License: MIT license
+Keywords: dasosdemo
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Python: >=3.8
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+# dasosdemo
+
+
+[![image](https://img.shields.io/pypi/v/dasosdemo.svg)](https://pypi.python.org/pypi/dasosdemo)
+[![image](https://img.shields.io/conda/vn/conda-forge/dasosdemo.svg)](https://anaconda.org/conda-forge/dasosdemo)
+
+
+**My first Python package.**
+
+
+-   Free software: MIT license
+-   Documentation: https://kriskaran.github.io/dasosdemo
+    
+
+## Features
+
+-   TODO
```

