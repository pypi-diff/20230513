# Comparing `tmp/a_pandas_ex_html_view-0.1.tar.gz` & `tmp/a_pandas_ex_html_view-0.11.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "a_pandas_ex_html_view-0.1.tar", last modified: Fri Oct  7 18:47:51 2022, max compression
+gzip compressed data, was "a_pandas_ex_html_view-0.11.tar", last modified: Sat May 13 10:28:19 2023, max compression
```

## Comparing `a_pandas_ex_html_view-0.1.tar` & `a_pandas_ex_html_view-0.11.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2022-10-07 18:47:51.536748 a_pandas_ex_html_view-0.1/
--rw-rw-rw-   0        0        0     1148 2022-10-07 18:47:46.000000 a_pandas_ex_html_view-0.1/LICENSE.rst
--rw-rw-rw-   0        0        0      173 2022-10-07 18:47:45.000000 a_pandas_ex_html_view-0.1/MANIFEST.in
--rw-rw-rw-   0        0        0     2919 2022-10-07 18:47:51.536748 a_pandas_ex_html_view-0.1/PKG-INFO
--rw-rw-rw-   0        0        0     1923 2022-10-07 18:46:00.000000 a_pandas_ex_html_view-0.1/README.md
-drwxrwxrwx   0        0        0        0 2022-10-07 18:47:51.533756 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/
--rw-rw-rw-   0        0        0     1069 2022-10-02 04:27:48.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/LICENSE
--rw-rw-rw-   0        0        0     1923 2022-10-07 18:46:00.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/README.MD
--rw-rw-rw-   0        0        0     6979 2022-10-07 18:24:52.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/__init__.py
--rw-rw-rw-   0        0        0       37 2022-10-07 18:47:50.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/requirements.txt
--rw-rw-rw-   0        0        0        2 2022-10-07 18:47:50.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/thirdparty.json
-drwxrwxrwx   0        0        0        0 2022-10-07 18:47:51.535750 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/
--rw-rw-rw-   0        0        0     2919 2022-10-07 18:47:51.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      449 2022-10-07 18:47:51.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-10-07 18:47:51.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       36 2022-10-07 18:47:51.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/requires.txt
--rw-rw-rw-   0        0        0       22 2022-10-07 18:47:51.000000 a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      115 2022-10-07 18:47:51.536748 a_pandas_ex_html_view-0.1/setup.cfg
--rw-rw-rw-   0        0        0     1510 2022-10-07 18:47:50.000000 a_pandas_ex_html_view-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:28:19.523467 a_pandas_ex_html_view-0.11/
+-rw-rw-rw-   0        0        0     1148 2023-05-13 10:28:10.000000 a_pandas_ex_html_view-0.11/LICENSE.rst
+-rw-rw-rw-   0        0        0      173 2023-05-13 10:28:09.000000 a_pandas_ex_html_view-0.11/MANIFEST.in
+-rw-rw-rw-   0        0        0     2601 2023-05-13 10:28:19.523467 a_pandas_ex_html_view-0.11/PKG-INFO
+-rw-rw-rw-   0        0        0     1923 2023-04-15 00:18:47.000000 a_pandas_ex_html_view-0.11/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 10:28:19.520476 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/
+-rw-rw-rw-   0        0        0     1069 2023-04-15 00:18:47.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/LICENSE
+-rw-rw-rw-   0        0        0     1923 2023-04-15 00:18:47.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/README.MD
+-rw-rw-rw-   0        0        0     6978 2023-05-13 10:24:28.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/__init__.py
+-rw-rw-rw-   0        0        0       63 2023-05-13 10:28:18.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/requirements.txt
+-rw-rw-rw-   0        0        0    16198 2023-05-13 10:28:18.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/thirdparty.json
+drwxrwxrwx   0        0        0        0 2023-05-13 10:28:19.523467 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/
+-rw-rw-rw-   0        0        0     2601 2023-05-13 10:28:19.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      449 2023-05-13 10:28:19.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 10:28:19.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       61 2023-05-13 10:28:19.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       22 2023-05-13 10:28:19.000000 a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       85 2023-05-13 10:28:19.524465 a_pandas_ex_html_view-0.11/setup.cfg
+-rw-rw-rw-   0        0        0     1483 2023-05-13 10:28:18.000000 a_pandas_ex_html_view-0.11/setup.py
```

### Comparing `a_pandas_ex_html_view-0.1/LICENSE.rst` & `a_pandas_ex_html_view-0.11/LICENSE.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 
  The MIT License (MIT)
- Copyright (c) 2022 Johannes Fischer
+ Copyright (c) 2023 Johannes Fischer
  
  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:
```

### Comparing `a_pandas_ex_html_view-0.1/PKG-INFO` & `a_pandas_ex_html_view-0.11/a_pandas_ex_html_view.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,77 +1,71 @@
 Metadata-Version: 2.1
-Name: a_pandas_ex_html_view
-Version: 0.1
+Name: a-pandas-ex-html-view
+Version: 0.11
 Summary: View/save any Pandas DataFrame/Series as HTML, works with MultiIndex as well
 Home-page: https://github.com/hansalemaos/a_pandas_ex_html_view
 Author: Johannes Fischer
-Author-email: <aulasparticularesdealemaosp@gmail.com>
+Author-email: aulasparticularesdealemaosp@gmail.com
 License: MIT
 Keywords: json,dict,list,HTML,CSS
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Topic :: Scientific/Engineering :: Visualization
+Classifier: Programming Language :: Python :: 3.10
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Classifier: Topic :: Text Editors :: Text Processing
-Classifier: Topic :: Text Processing :: General
-Classifier: Topic :: Text Processing :: Indexing
-Classifier: Topic :: Text Processing :: Filters
 Classifier: Topic :: Utilities
 Description-Content-Type: text/markdown
 License-File: LICENSE.rst
 
+### DataFrame / Series in your browser
 
-### DataFrame / Series in your browser
-
-```python
-#Based on pypi.org/project/any-iter-to-html-table/
-from a_pandas_ex_html_view import pd_add_html_view
-import pandas as pd
-pd_add_html_view() #this adds to new methods to pandas
-df = pd.read_csv("https://github.com/pandas-dev/pandas/raw/main/doc/data/titanic.csv")
-df.ds_html_view() #for whole DataFrame
-df.Name.ds_html_view() #for Series
-```
-
-![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandastable.png)
-
-![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandasseries.png)
-
-### For DataFrames with MultiIndex
-
-If you create your MultiIndexed DataFrame using [a-pandas-ex-plode-tool · PyPI](https://pypi.org/project/a-pandas-ex-plode-tool/)
-
-a_pandas_ex_html_view will format the DataFrame in the prettiest way possible :)
-
-![](https://github.com/hansalemaos/screenshots/raw/main/pandsnesteddicthtml.png)
-
-```python
-from a_pandas_ex_plode_tool import pd_add_explode_tools
-pd_add_explode_tools()
-data = {
-    "glossary": {
-        "title": "example glossary",
-        "GlossDiv": {
-            "title": "S",
-            "GlossList": {
-                "GlossEntry": {
-                    "ID": "SGML",
-                    "SortAs": "SGML",
-                    "GlossTerm": "Standard Generalized Markup Language",
-                    "Acronym": "SGML",
-                    "Abbrev": "ISO 8879:1986",
-                    "GlossDef": {
-                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
-                        "GlossSeeAlso": ["GML", "XML"],
-                    },
-                    "GlossSee": "markup",
-                }
-            },
-        },
-    }
-}
-df = pd.Q_AnyNestedIterable_2df(data)
-df.ds_html_view()   
-#if you don't want to open it in browser, just save it to your HDD:
-df.ds_html_view('f:\\testhtml.html') 
-```
+```python
+#Based on pypi.org/project/any-iter-to-html-table/
+from a_pandas_ex_html_view import pd_add_html_view
+import pandas as pd
+pd_add_html_view() #this adds to new methods to pandas
+df = pd.read_csv("https://github.com/pandas-dev/pandas/raw/main/doc/data/titanic.csv")
+df.ds_html_view() #for whole DataFrame
+df.Name.ds_html_view() #for Series
+```
+
+![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandastable.png)
+
+![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandasseries.png)
+
+### For DataFrames with MultiIndex
+
+If you create your MultiIndexed DataFrame using [a-pandas-ex-plode-tool Â· PyPI](https://pypi.org/project/a-pandas-ex-plode-tool/)
+
+a_pandas_ex_html_view will format the DataFrame in the prettiest way possible :)
+
+![](https://github.com/hansalemaos/screenshots/raw/main/pandsnesteddicthtml.png)
+
+```python
+from a_pandas_ex_plode_tool import pd_add_explode_tools
+pd_add_explode_tools()
+data = {
+    "glossary": {
+        "title": "example glossary",
+        "GlossDiv": {
+            "title": "S",
+            "GlossList": {
+                "GlossEntry": {
+                    "ID": "SGML",
+                    "SortAs": "SGML",
+                    "GlossTerm": "Standard Generalized Markup Language",
+                    "Acronym": "SGML",
+                    "Abbrev": "ISO 8879:1986",
+                    "GlossDef": {
+                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
+                        "GlossSeeAlso": ["GML", "XML"],
+                    },
+                    "GlossSee": "markup",
+                }
+            },
+        },
+    }
+}
+df = pd.Q_AnyNestedIterable_2df(data)
+df.ds_html_view()   
+#if you don't want to open it in browser, just save it to your HDD:
+df.ds_html_view('f:\\testhtml.html') 
+```
```

### Comparing `a_pandas_ex_html_view-0.1/README.md` & `a_pandas_ex_html_view-0.11/README.md`

 * *Files identical despite different names*

### Comparing `a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/LICENSE` & `a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/LICENSE`

 * *Files identical despite different names*

### Comparing `a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/README.MD` & `a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/README.MD`

 * *Files identical despite different names*

### Comparing `a_pandas_ex_html_view-0.1/a_pandas_ex_html_view/__init__.py` & `a_pandas_ex_html_view-0.11/a_pandas_ex_html_view/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 import webbrowser
 from typing import Union
 from pandas.core.frame import DataFrame, Series
 import regex
 import pandas as pd
 from tempfile import TemporaryDirectory
 from a_pandas_ex_plode_tool import unstacked_df_back_to_multiindex, _unstack_df
-from aa_pandas_ex_df_to_string import ds_to_string
+from a_pandas_ex_df_to_string import ds_to_string
 
 _tmp_dict_pd = TemporaryDirectory()
 
 
 def series_to_dataframe(
     df: Union[pd.Series, pd.DataFrame]
 ) -> (Union[pd.Series, pd.DataFrame], bool):
```

### Comparing `a_pandas_ex_html_view-0.1/a_pandas_ex_html_view.egg-info/PKG-INFO` & `a_pandas_ex_html_view-0.11/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,77 +1,71 @@
 Metadata-Version: 2.1
-Name: a-pandas-ex-html-view
-Version: 0.1
+Name: a_pandas_ex_html_view
+Version: 0.11
 Summary: View/save any Pandas DataFrame/Series as HTML, works with MultiIndex as well
 Home-page: https://github.com/hansalemaos/a_pandas_ex_html_view
 Author: Johannes Fischer
-Author-email: <aulasparticularesdealemaosp@gmail.com>
+Author-email: aulasparticularesdealemaosp@gmail.com
 License: MIT
 Keywords: json,dict,list,HTML,CSS
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Topic :: Scientific/Engineering :: Visualization
+Classifier: Programming Language :: Python :: 3.10
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Classifier: Topic :: Text Editors :: Text Processing
-Classifier: Topic :: Text Processing :: General
-Classifier: Topic :: Text Processing :: Indexing
-Classifier: Topic :: Text Processing :: Filters
 Classifier: Topic :: Utilities
 Description-Content-Type: text/markdown
 License-File: LICENSE.rst
 
+### DataFrame / Series in your browser
 
-### DataFrame / Series in your browser
-
-```python
-#Based on pypi.org/project/any-iter-to-html-table/
-from a_pandas_ex_html_view import pd_add_html_view
-import pandas as pd
-pd_add_html_view() #this adds to new methods to pandas
-df = pd.read_csv("https://github.com/pandas-dev/pandas/raw/main/doc/data/titanic.csv")
-df.ds_html_view() #for whole DataFrame
-df.Name.ds_html_view() #for Series
-```
-
-![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandastable.png)
-
-![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandasseries.png)
-
-### For DataFrames with MultiIndex
-
-If you create your MultiIndexed DataFrame using [a-pandas-ex-plode-tool · PyPI](https://pypi.org/project/a-pandas-ex-plode-tool/)
-
-a_pandas_ex_html_view will format the DataFrame in the prettiest way possible :)
-
-![](https://github.com/hansalemaos/screenshots/raw/main/pandsnesteddicthtml.png)
-
-```python
-from a_pandas_ex_plode_tool import pd_add_explode_tools
-pd_add_explode_tools()
-data = {
-    "glossary": {
-        "title": "example glossary",
-        "GlossDiv": {
-            "title": "S",
-            "GlossList": {
-                "GlossEntry": {
-                    "ID": "SGML",
-                    "SortAs": "SGML",
-                    "GlossTerm": "Standard Generalized Markup Language",
-                    "Acronym": "SGML",
-                    "Abbrev": "ISO 8879:1986",
-                    "GlossDef": {
-                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
-                        "GlossSeeAlso": ["GML", "XML"],
-                    },
-                    "GlossSee": "markup",
-                }
-            },
-        },
-    }
-}
-df = pd.Q_AnyNestedIterable_2df(data)
-df.ds_html_view()   
-#if you don't want to open it in browser, just save it to your HDD:
-df.ds_html_view('f:\\testhtml.html') 
-```
+```python
+#Based on pypi.org/project/any-iter-to-html-table/
+from a_pandas_ex_html_view import pd_add_html_view
+import pandas as pd
+pd_add_html_view() #this adds to new methods to pandas
+df = pd.read_csv("https://github.com/pandas-dev/pandas/raw/main/doc/data/titanic.csv")
+df.ds_html_view() #for whole DataFrame
+df.Name.ds_html_view() #for Series
+```
+
+![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandastable.png)
+
+![](https://github.com/hansalemaos/screenshots/raw/main/screenshotpandasseries.png)
+
+### For DataFrames with MultiIndex
+
+If you create your MultiIndexed DataFrame using [a-pandas-ex-plode-tool Â· PyPI](https://pypi.org/project/a-pandas-ex-plode-tool/)
+
+a_pandas_ex_html_view will format the DataFrame in the prettiest way possible :)
+
+![](https://github.com/hansalemaos/screenshots/raw/main/pandsnesteddicthtml.png)
+
+```python
+from a_pandas_ex_plode_tool import pd_add_explode_tools
+pd_add_explode_tools()
+data = {
+    "glossary": {
+        "title": "example glossary",
+        "GlossDiv": {
+            "title": "S",
+            "GlossList": {
+                "GlossEntry": {
+                    "ID": "SGML",
+                    "SortAs": "SGML",
+                    "GlossTerm": "Standard Generalized Markup Language",
+                    "Acronym": "SGML",
+                    "Abbrev": "ISO 8879:1986",
+                    "GlossDef": {
+                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
+                        "GlossSeeAlso": ["GML", "XML"],
+                    },
+                    "GlossSee": "markup",
+                }
+            },
+        },
+    }
+}
+df = pd.Q_AnyNestedIterable_2df(data)
+df.ds_html_view()   
+#if you don't want to open it in browser, just save it to your HDD:
+df.ds_html_view('f:\\testhtml.html') 
+```
```

