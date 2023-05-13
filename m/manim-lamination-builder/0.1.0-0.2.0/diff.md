# Comparing `tmp/manim_lamination_builder-0.1.0.tar.gz` & `tmp/manim_lamination_builder-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "manim_lamination_builder-0.1.0.tar", last modified: Fri Feb 24 16:13:09 2023, max compression
+gzip compressed data, was "manim_lamination_builder-0.2.0.tar", last modified: Sat May 13 16:27:15 2023, max compression
```

## Comparing `manim_lamination_builder-0.1.0.tar` & `manim_lamination_builder-0.2.0.tar`

### file list

```diff
@@ -1,12 +1,22 @@
-drwxr-xr-x   0 forrest   (1000) forrest   (1000)        0 2023-02-24 16:13:09.818139 manim_lamination_builder-0.1.0/
--rw-r--r--   0 forrest   (1000) forrest   (1000)    34523 2023-02-24 00:36:13.000000 manim_lamination_builder-0.1.0/LICENSE
--rw-r--r--   0 forrest   (1000) forrest   (1000)    42080 2023-02-24 16:13:09.818139 manim_lamination_builder-0.1.0/PKG-INFO
--rw-r--r--   0 forrest   (1000) forrest   (1000)     1819 2023-02-24 00:41:23.000000 manim_lamination_builder-0.1.0/README.md
-drwxr-xr-x   0 forrest   (1000) forrest   (1000)        0 2023-02-24 16:13:09.818139 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/
--rw-r--r--   0 forrest   (1000) forrest   (1000)    42080 2023-02-24 16:13:09.000000 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/PKG-INFO
--rw-r--r--   0 forrest   (1000) forrest   (1000)      271 2023-02-24 16:13:09.000000 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/SOURCES.txt
--rw-r--r--   0 forrest   (1000) forrest   (1000)        1 2023-02-24 16:13:09.000000 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/dependency_links.txt
--rw-r--r--   0 forrest   (1000) forrest   (1000)        6 2023-02-24 16:13:09.000000 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/requires.txt
--rw-r--r--   0 forrest   (1000) forrest   (1000)        6 2023-02-24 16:13:09.000000 manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/top_level.txt
--rw-r--r--   0 forrest   (1000) forrest   (1000)      706 2023-02-24 16:13:04.000000 manim_lamination_builder-0.1.0/pyproject.toml
--rw-r--r--   0 forrest   (1000) forrest   (1000)       38 2023-02-24 16:13:09.818139 manim_lamination_builder-0.1.0/setup.cfg
+drwxr-xr-x   0 forrest   (1000) forrest   (1000)        0 2023-05-13 16:27:15.891479 manim_lamination_builder-0.2.0/
+-rw-r--r--   0 forrest   (1000) forrest   (1000)    34523 2023-02-24 00:36:13.000000 manim_lamination_builder-0.2.0/LICENSE
+-rw-r--r--   0 forrest   (1000) forrest   (1000)    43066 2023-05-13 16:27:15.891479 manim_lamination_builder-0.2.0/PKG-INFO
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     2724 2023-04-02 00:57:01.000000 manim_lamination_builder-0.2.0/README.md
+drwxr-xr-x   0 forrest   (1000) forrest   (1000)        0 2023-05-13 16:27:15.891479 manim_lamination_builder-0.2.0/manim_lamination_builder/
+-rw-r--r--   0 forrest   (1000) forrest   (1000)      960 2023-05-13 16:25:33.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/__init__.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     4412 2023-05-13 16:17:33.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/animation.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     3132 2023-05-13 15:20:55.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/chord.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     2846 2023-05-13 15:21:01.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/custom_json.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     4398 2023-05-13 16:20:40.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/generate.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     3455 2023-05-13 15:21:27.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/lamination.py
+-rwxr-xr-x   0 forrest   (1000) forrest   (1000)     1600 2023-05-13 15:22:17.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/main.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     4464 2023-05-13 15:22:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/morph.py
+-rw-r--r--   0 forrest   (1000) forrest   (1000)     6826 2023-05-13 14:47:08.000000 manim_lamination_builder-0.2.0/manim_lamination_builder/points.py
+drwxr-xr-x   0 forrest   (1000) forrest   (1000)        0 2023-05-13 16:27:15.891479 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/
+-rw-r--r--   0 forrest   (1000) forrest   (1000)    43066 2023-05-13 16:27:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/PKG-INFO
+-rw-r--r--   0 forrest   (1000) forrest   (1000)      598 2023-05-13 16:27:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/SOURCES.txt
+-rw-r--r--   0 forrest   (1000) forrest   (1000)        1 2023-05-13 16:27:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/dependency_links.txt
+-rw-r--r--   0 forrest   (1000) forrest   (1000)       12 2023-05-13 16:27:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/requires.txt
+-rw-r--r--   0 forrest   (1000) forrest   (1000)       25 2023-05-13 16:27:15.000000 manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/top_level.txt
+-rw-r--r--   0 forrest   (1000) forrest   (1000)      668 2023-05-11 15:29:33.000000 manim_lamination_builder-0.2.0/pyproject.toml
+-rw-r--r--   0 forrest   (1000) forrest   (1000)       38 2023-05-13 16:27:15.891479 manim_lamination_builder-0.2.0/setup.cfg
```

### Comparing `manim_lamination_builder-0.1.0/LICENSE` & `manim_lamination_builder-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `manim_lamination_builder-0.1.0/PKG-INFO` & `manim_lamination_builder-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: manim_lamination_builder
-Version: 0.1.0
+Version: 0.2.0
 Summary: a replacement to lamination builder that uses manim instead of the browser
 Author-email: Forrest Hilton <forrestmhilton@gmail.com>
 License:                     GNU AFFERO GENERAL PUBLIC LICENSE
                                Version 3, 19 November 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -661,51 +661,72 @@
         specific requirements.
         
           You should also get your employer (if you work as a programmer) or school,
         if any, to sign a "copyright disclaimer" for the program, if necessary.
         For more information on this, and how to apply and follow the GNU AGPL, see
         <https://www.gnu.org/licenses/>.
         
+Project-URL: Homepage, https://github.com/ForrestHilton/manim-lamination-builder
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
+# WORK IN PROGRESS -- THE FEATURES NOT USED IN THE EXAMPLE DON'T WORK YET
+
 This is a re-implementation of [lamination-builder](https://csfalcione.github.io/lamination-builder/) that runs in python without dependencies on a browser and focusing on convenient generation of figures. Instead it uses [Manim](https://github.com/ManimCommunity/manim/), and which has several dependencies. 
 
-The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to righ and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
+The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to right and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
 
 Each lamination may have of the following fields: polygons, chords (must be a list of lists of length two), point_lables, point_colors ("*" for default color which defaults to red), and points. Omissions in each field will be filled based on the fields that proceed it in the list above. Each lamination must have a "radix" which is the base.
 
 # Example:
 ```
 [
   {
-    "polygons":[["_001","_010","_100"]],
-    "chords":[["_100","2"]],
-    "point_lables": {"_001": "starting point", "_010": "maps to _100"},
-    "point_colors": {"*": "blue", "_001": "red"},
-    "points": ["1","2","_3"],
-    "radix": 4
+    polygons:[["_001","_010","_100"]],
+    chords:[["_1","2"]],
+    points: ["3"],
+    radix: 4
   },
   {
-    "radix": 3
-  }
+    "polygons": [["0_003", "0_030", "0_300"], 
+      ["1_003", "3_030", "3_300"], 
+      ["2_003", "2_030", "2_300"], 
+      ["3_003", "1_030", "1_300"]], 
+    "chords": [], 
+    "points": [], 
+    "radix": 4
+  },
+  { radix: 4}
 ]
 ```
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/contrived_example.png "Render of json above")
+
+# Installation: (correct python packaging is on the TODO list)
+Please refer to [to manim's installation instructions](https://docs.manim.community/en/stable/installation.html). It and its dependencies are required, with the possible exception of tex.
+```
+pip install manim json json5
+git clone https://github.com/ForrestHilton/python-lamination-builder
+```
+
+Add the project to you PYTHONPATH in a settings file, if you wish to import the python files.
+
 # Usage: 
-commandline TODO
+```
+/path/to/python-lamination-builder/main.py file.json
+```
 
-Installation:
-Follow the manim installation steps.
 
 Feature requests will be entertained. I have yet to see a need for any of the following features: mapping forward, pull backs, automatically placing descriptions or tittles at the top. This is intended to be used in combination with other tools like latex and your own python scripts. I hope this is a reasonable API.
 
 
+# example output from my research
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/example.png "Example Output from my Reasearch")
 
 # License
 Licensed under the The AGPLv3 License (AGPLv3)
 Copyright (c) 2023 Forrest M. Hilton <forrestmhilton@gmail.com>
 You should have received a copy of the GNU Affero General Public License
 along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

### Comparing `manim_lamination_builder-0.1.0/README.md` & `manim_lamination_builder-0.2.0/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -1,37 +1,57 @@
+# WORK IN PROGRESS -- THE FEATURES NOT USED IN THE EXAMPLE DON'T WORK YET
+
 This is a re-implementation of [lamination-builder](https://csfalcione.github.io/lamination-builder/) that runs in python without dependencies on a browser and focusing on convenient generation of figures. Instead it uses [Manim](https://github.com/ManimCommunity/manim/), and which has several dependencies. 
 
-The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to righ and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
+The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to right and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
 
 Each lamination may have of the following fields: polygons, chords (must be a list of lists of length two), point_lables, point_colors ("*" for default color which defaults to red), and points. Omissions in each field will be filled based on the fields that proceed it in the list above. Each lamination must have a "radix" which is the base.
 
 # Example:
 ```
 [
   {
-    "polygons":[["_001","_010","_100"]],
-    "chords":[["_100","2"]],
-    "point_lables": {"_001": "starting point", "_010": "maps to _100"},
-    "point_colors": {"*": "blue", "_001": "red"},
-    "points": ["1","2","_3"],
-    "radix": 4
+    polygons:[["_001","_010","_100"]],
+    chords:[["_1","2"]],
+    points: ["3"],
+    radix: 4
   },
   {
-    "radix": 3
-  }
+    "polygons": [["0_003", "0_030", "0_300"], 
+      ["1_003", "3_030", "3_300"], 
+      ["2_003", "2_030", "2_300"], 
+      ["3_003", "1_030", "1_300"]], 
+    "chords": [], 
+    "points": [], 
+    "radix": 4
+  },
+  { radix: 4}
 ]
 ```
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/contrived_example.png "Render of json above")
+
+# Installation: (correct python packaging is on the TODO list)
+Please refer to [to manim's installation instructions](https://docs.manim.community/en/stable/installation.html). It and its dependencies are required, with the possible exception of tex.
+```
+pip install manim json json5
+git clone https://github.com/ForrestHilton/python-lamination-builder
+```
+
+Add the project to you PYTHONPATH in a settings file, if you wish to import the python files.
+
 # Usage: 
-commandline TODO
+```
+/path/to/python-lamination-builder/main.py file.json
+```
 
-Installation:
-Follow the manim installation steps.
 
 Feature requests will be entertained. I have yet to see a need for any of the following features: mapping forward, pull backs, automatically placing descriptions or tittles at the top. This is intended to be used in combination with other tools like latex and your own python scripts. I hope this is a reasonable API.
 
 
+# example output from my research
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/example.png "Example Output from my Reasearch")
 
 # License
 Licensed under the The AGPLv3 License (AGPLv3)
 Copyright (c) 2023 Forrest M. Hilton <forrestmhilton@gmail.com>
 You should have received a copy of the GNU Affero General Public License
 along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

### Comparing `manim_lamination_builder-0.1.0/manim_lamination_builder.egg-info/PKG-INFO` & `manim_lamination_builder-0.2.0/manim_lamination_builder.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: manim-lamination-builder
-Version: 0.1.0
+Version: 0.2.0
 Summary: a replacement to lamination builder that uses manim instead of the browser
 Author-email: Forrest Hilton <forrestmhilton@gmail.com>
 License:                     GNU AFFERO GENERAL PUBLIC LICENSE
                                Version 3, 19 November 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -661,51 +661,72 @@
         specific requirements.
         
           You should also get your employer (if you work as a programmer) or school,
         if any, to sign a "copyright disclaimer" for the program, if necessary.
         For more information on this, and how to apply and follow the GNU AGPL, see
         <https://www.gnu.org/licenses/>.
         
+Project-URL: Homepage, https://github.com/ForrestHilton/manim-lamination-builder
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
+# WORK IN PROGRESS -- THE FEATURES NOT USED IN THE EXAMPLE DON'T WORK YET
+
 This is a re-implementation of [lamination-builder](https://csfalcione.github.io/lamination-builder/) that runs in python without dependencies on a browser and focusing on convenient generation of figures. Instead it uses [Manim](https://github.com/ManimCommunity/manim/), and which has several dependencies. 
 
-The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to righ and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
+The input format is as follows: A list of laminations to be placed in the figure (tilling is a best effort left to right and top to bottom Placemen based on a 16:9 screen). The blank lamination is permited.
 
 Each lamination may have of the following fields: polygons, chords (must be a list of lists of length two), point_lables, point_colors ("*" for default color which defaults to red), and points. Omissions in each field will be filled based on the fields that proceed it in the list above. Each lamination must have a "radix" which is the base.
 
 # Example:
 ```
 [
   {
-    "polygons":[["_001","_010","_100"]],
-    "chords":[["_100","2"]],
-    "point_lables": {"_001": "starting point", "_010": "maps to _100"},
-    "point_colors": {"*": "blue", "_001": "red"},
-    "points": ["1","2","_3"],
-    "radix": 4
+    polygons:[["_001","_010","_100"]],
+    chords:[["_1","2"]],
+    points: ["3"],
+    radix: 4
   },
   {
-    "radix": 3
-  }
+    "polygons": [["0_003", "0_030", "0_300"], 
+      ["1_003", "3_030", "3_300"], 
+      ["2_003", "2_030", "2_300"], 
+      ["3_003", "1_030", "1_300"]], 
+    "chords": [], 
+    "points": [], 
+    "radix": 4
+  },
+  { radix: 4}
 ]
 ```
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/contrived_example.png "Render of json above")
+
+# Installation: (correct python packaging is on the TODO list)
+Please refer to [to manim's installation instructions](https://docs.manim.community/en/stable/installation.html). It and its dependencies are required, with the possible exception of tex.
+```
+pip install manim json json5
+git clone https://github.com/ForrestHilton/python-lamination-builder
+```
+
+Add the project to you PYTHONPATH in a settings file, if you wish to import the python files.
+
 # Usage: 
-commandline TODO
+```
+/path/to/python-lamination-builder/main.py file.json
+```
 
-Installation:
-Follow the manim installation steps.
 
 Feature requests will be entertained. I have yet to see a need for any of the following features: mapping forward, pull backs, automatically placing descriptions or tittles at the top. This is intended to be used in combination with other tools like latex and your own python scripts. I hope this is a reasonable API.
 
 
+# example output from my research
+![please enable images](https://github.com/ForrestHilton/python-lamination-builder/blob/main/example.png "Example Output from my Reasearch")
 
 # License
 Licensed under the The AGPLv3 License (AGPLv3)
 Copyright (c) 2023 Forrest M. Hilton <forrestmhilton@gmail.com>
 You should have received a copy of the GNU Affero General Public License
 along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

### Comparing `manim_lamination_builder-0.1.0/pyproject.toml` & `manim_lamination_builder-0.2.0/pyproject.toml`

 * *Files 25% similar despite different names*

```diff
@@ -1,24 +1,23 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "manim_lamination_builder"
-version = "0.1.0"
+version = "0.2.0"
 authors = [
   { name="Forrest Hilton", email="forrestmhilton@gmail.com" },
 ]
 description = "a replacement to lamination builder that uses manim instead of the browser"
 readme = "README.md"
 requires-python = ">=3.7"
 license = {file = "LICENSE"}
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 dependencies = [
-  "manim"
+  "manim", "json5"
 ]
 [project.urls]
-# "Homepage" = "https://github.com/pypa/sampleproject"
-# "Bug Tracker" = "https://github.com/pypa/sampleproject/issues"
+"Homepage" = "https://github.com/ForrestHilton/manim-lamination-builder"
```

