# Comparing `tmp/data-science-toolkit-0.0.998.tar.gz` & `tmp/data-science-toolkit-0.0.999.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "E:\projects\dst\dist\tmpbtha92fh\data-science-toolkit-0.0.998.tar", last modified: Fri May 12 20:59:47 2023, max compression
+gzip compressed data, was "E:\projects\dst\dist\tmpzj8mfama\data-science-toolkit-0.0.999.tar", last modified: Sat May 13 00:45:18 2023, max compression
```

## Comparing `data-science-toolkit-0.0.998.tar` & `data-science-toolkit-0.0.999.tar`

### file list

```diff
@@ -1,43 +1,29 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/
--rw-rw-rw-   0        0        0      104 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/.gitignore
--rw-rw-rw-   0        0        0      734 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/.readthedocs.yaml
--rw-rw-rw-   0        0        0     1096 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/LICENSE
--rw-rw-rw-   0        0        0     1965 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/PKG-INFO
--rw-rw-rw-   0        0        0     1355 2022-04-14 01:06:21.000000 data-science-toolkit-0.0.998/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:46.000000 data-science-toolkit-0.0.998/docs/
--rw-rw-rw-   0        0        0     2215 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/docs/conf.py
--rw-rw-rw-   0        0        0      970 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/docs/dst.rst
--rw-rw-rw-   0        0        0      412 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/docs/index.rst
--rw-rw-rw-   0        0        0       53 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/docs/modules.rst
--rw-rw-rw-   0        0        0     1974 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/docs/requirements.txt
--rw-rw-rw-   0        0        0      600 2022-11-21 16:03:48.000000 data-science-toolkit-0.0.998/dst_test.ipynb
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/media/
--rw-rw-rw-   0        0        0   176934 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/media/dst_logo.png
--rw-rw-rw-   0        0        0      387 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/pyproject.toml
--rw-rw-rw-   0        0        0     1636 2023-02-28 18:14:23.000000 data-science-toolkit-0.0.998/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/setup.cfg
--rw-rw-rw-   0        0        0     1412 2023-05-12 20:57:13.000000 data-science-toolkit-0.0.998/setup.py
--rw-rw-rw-   0        0        0      714 2022-03-26 21:26:37.000000 data-science-toolkit-0.0.998/setupp.cfg
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:46.000000 data-science-toolkit-0.0.998/src/
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/
--rw-rw-rw-   0        0        0        0 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/__init__.py
--rw-rw-rw-   0        0        0    10268 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/chart.py
--rw-rw-rw-   0        0        0     6375 2022-05-20 00:30:43.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/csm.py
--rw-rw-rw-   0        0        0    70325 2023-05-12 20:58:24.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/dataframe.py
--rw-rw-rw-   0        0        0    12467 2022-05-20 00:36:43.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/gis.py
--rw-rw-rw-   0        0        0     8456 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/imagefactory.py
--rw-rw-rw-   0        0        0    17398 2023-03-01 01:36:35.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/lib.py
--rw-rw-rw-   0        0        0    28669 2023-03-15 23:27:50.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/model.py
--rw-rw-rw-   0        0        0     7636 2022-05-20 00:33:21.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/r3.py
--rw-rw-rw-   0        0        0     4983 2021-02-01 01:53:23.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/rl.py
--rw-rw-rw-   0        0        0     1445 2022-05-19 23:54:12.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/rl_dqn.py
--rw-rw-rw-   0        0        0     5488 2023-03-15 23:28:40.000000 data-science-toolkit-0.0.998/src/data_science_toolkit/vectorizer.py
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/
--rw-rw-rw-   0        0        0     1965 2023-05-12 20:59:41.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      896 2023-05-12 20:59:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 20:59:41.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      198 2023-05-12 20:59:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/requires.txt
--rw-rw-rw-   0        0        0       21 2023-05-12 20:59:42.000000 data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-12 20:59:47.000000 data-science-toolkit-0.0.998/test/
--rw-rw-rw-   0        0        0      597 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/test/kitchen.py
--rw-rw-rw-   0        0        0       85 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.998/test/test.py
+drwxrwxrwx   0        0        0        0 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/
+-rw-rw-rw-   0        0        0     1096 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/LICENSE
+-rw-rw-rw-   0        0        0     1965 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/PKG-INFO
+-rw-rw-rw-   0        0        0     1355 2022-04-14 01:06:21.000000 data-science-toolkit-0.0.999/README.md
+-rw-rw-rw-   0        0        0      387 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/setup.cfg
+-rw-rw-rw-   0        0        0     1435 2023-05-13 00:44:55.000000 data-science-toolkit-0.0.999/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 00:45:17.000000 data-science-toolkit-0.0.999/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/
+-rw-rw-rw-   0        0        0        0 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/__init__.py
+-rw-rw-rw-   0        0        0    10268 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/chart.py
+-rw-rw-rw-   0        0        0     6375 2022-05-20 00:30:43.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/csm.py
+-rw-rw-rw-   0        0        0    70325 2023-05-12 20:58:24.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/dataframe.py
+-rw-rw-rw-   0        0        0    12467 2022-05-20 00:36:43.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/gis.py
+-rw-rw-rw-   0        0        0     8456 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/imagefactory.py
+-rw-rw-rw-   0        0        0    25115 2023-05-13 00:40:51.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/lib.py
+-rw-rw-rw-   0        0        0    28669 2023-03-15 23:27:50.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/model.py
+-rw-rw-rw-   0        0        0     7636 2022-05-20 00:33:21.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/r3.py
+-rw-rw-rw-   0        0        0     4983 2021-02-01 01:53:23.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/rl.py
+-rw-rw-rw-   0        0        0     1445 2022-05-19 23:54:12.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/rl_dqn.py
+-rw-rw-rw-   0        0        0     5488 2023-03-15 23:28:40.000000 data-science-toolkit-0.0.999/src/data_science_toolkit/vectorizer.py
+drwxrwxrwx   0        0        0        0 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/
+-rw-rw-rw-   0        0        0     1965 2023-05-13 00:45:13.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      709 2023-05-13 00:45:15.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 00:45:13.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      209 2023-05-13 00:45:14.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-05-13 00:45:14.000000 data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 00:45:18.000000 data-science-toolkit-0.0.999/test/
+-rw-rw-rw-   0        0        0       85 2022-03-25 12:00:42.000000 data-science-toolkit-0.0.999/test/test.py
```

### Comparing `data-science-toolkit-0.0.998/LICENSE` & `data-science-toolkit-0.0.999/LICENSE`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/PKG-INFO` & `data-science-toolkit-0.0.999/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: data-science-toolkit
-Version: 0.0.998
+Version: 0.0.999
 Summary: Data Science Toolkit (DST) is a Python library that helps implement data science related project with ease.
 Home-page: https://github.com/elhachimi-ch/dst
 Author: EL HACHIMI CHOUAIB
 Author-email: elhachimi.ch@gmail.com
 Project-URL: Bug Tracker, https://github.com/elhachimi-ch/dst/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `data-science-toolkit-0.0.998/README.md` & `data-science-toolkit-0.0.999/README.md`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/setup.py` & `data-science-toolkit-0.0.999/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
     
     
 setuptools.setup(
     name="data-science-toolkit",
-    version="0.0.998",
+    version="0.0.999",
     author="EL HACHIMI CHOUAIB",
     author_email="elhachimi.ch@gmail.com",
     description="Data Science Toolkit (DST) is a Python library that helps implement data science related project with ease.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/elhachimi-ch/dst",
     project_urls={
@@ -41,10 +41,11 @@
         "scikit-image",
         "unidecode",
         "emoji>=1.7",
         "textblob",
         "nltk",
         "wordcloud",
         "optuna",
-        "contextily"
+        "contextily",
+        "langdetect"
     ],
 )
```

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/chart.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/chart.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/csm.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/csm.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/dataframe.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/dataframe.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/gis.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/gis.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/imagefactory.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/imagefactory.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/model.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/model.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/r3.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/r3.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/rl.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/rl.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/rl_dqn.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/rl_dqn.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit/vectorizer.py` & `data-science-toolkit-0.0.999/src/data_science_toolkit/vectorizer.py`

 * *Files identical despite different names*

### Comparing `data-science-toolkit-0.0.998/src/data_science_toolkit.egg-info/PKG-INFO` & `data-science-toolkit-0.0.999/src/data_science_toolkit.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: data-science-toolkit
-Version: 0.0.998
+Version: 0.0.999
 Summary: Data Science Toolkit (DST) is a Python library that helps implement data science related project with ease.
 Home-page: https://github.com/elhachimi-ch/dst
 Author: EL HACHIMI CHOUAIB
 Author-email: elhachimi.ch@gmail.com
 Project-URL: Bug Tracker, https://github.com/elhachimi-ch/dst/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

