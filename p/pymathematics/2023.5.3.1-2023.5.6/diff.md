# Comparing `tmp/pymathematics-2023.5.3.1.tar.gz` & `tmp/pymathematics-2023.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymathematics-2023.5.3.1.tar", last modified: Wed May  3 16:24:11 2023, max compression
+gzip compressed data, was "pymathematics-2023.5.6.tar", last modified: Sat May  6 17:55:58 2023, max compression
```

## Comparing `pymathematics-2023.5.3.1.tar` & `pymathematics-2023.5.6.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-03 16:24:11.898458 pymathematics-2023.5.3.1/
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)     1088 2023-04-16 06:03:02.000000 pymathematics-2023.5.3.1/LICENSE
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      508 2023-05-03 16:24:11.868453 pymathematics-2023.5.3.1/PKG-INFO
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      167 2023-05-03 16:21:23.000000 pymathematics-2023.5.3.1/README.md
-drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-03 16:24:11.345451 pymathematics-2023.5.3.1/pymathematics/
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)    27658 2023-05-03 16:19:20.000000 pymathematics-2023.5.3.1/pymathematics/__init__.py
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      112 2023-05-03 16:21:49.000000 pymathematics-2023.5.3.1/pymathematics/info.py
-drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-03 16:24:11.758459 pymathematics-2023.5.3.1/pymathematics.egg-info/
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      508 2023-05-03 16:24:10.000000 pymathematics-2023.5.3.1/pymathematics.egg-info/PKG-INFO
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      258 2023-05-03 16:24:10.000000 pymathematics-2023.5.3.1/pymathematics.egg-info/SOURCES.txt
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        1 2023-05-03 16:24:10.000000 pymathematics-2023.5.3.1/pymathematics.egg-info/dependency_links.txt
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        6 2023-05-03 16:24:10.000000 pymathematics-2023.5.3.1/pymathematics.egg-info/requires.txt
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)       14 2023-05-03 16:24:10.000000 pymathematics-2023.5.3.1/pymathematics.egg-info/top_level.txt
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)       38 2023-05-03 16:24:11.907455 pymathematics-2023.5.3.1/setup.cfg
--rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      697 2023-05-03 16:21:28.000000 pymathematics-2023.5.3.1/setup.py
+drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-06 17:55:58.581357 pymathematics-2023.5.6/
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)     1088 2023-04-16 06:03:02.000000 pymathematics-2023.5.6/LICENSE
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      506 2023-05-06 17:55:58.572364 pymathematics-2023.5.6/PKG-INFO
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      165 2023-05-06 11:17:21.000000 pymathematics-2023.5.6/README.md
+drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-06 17:55:58.196655 pymathematics-2023.5.6/pymathematics/
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)    29051 2023-05-06 11:17:39.000000 pymathematics-2023.5.6/pymathematics/__init__.py
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      110 2023-05-06 11:16:56.000000 pymathematics-2023.5.6/pymathematics/info.py
+drwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        0 2023-05-06 17:55:58.513354 pymathematics-2023.5.6/pymathematics.egg-info/
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      506 2023-05-06 17:55:53.000000 pymathematics-2023.5.6/pymathematics.egg-info/PKG-INFO
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      258 2023-05-06 17:55:53.000000 pymathematics-2023.5.6/pymathematics.egg-info/SOURCES.txt
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        1 2023-05-06 17:55:53.000000 pymathematics-2023.5.6/pymathematics.egg-info/dependency_links.txt
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)        6 2023-05-06 17:55:53.000000 pymathematics-2023.5.6/pymathematics.egg-info/requires.txt
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)       14 2023-05-06 17:55:53.000000 pymathematics-2023.5.6/pymathematics.egg-info/top_level.txt
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)       38 2023-05-06 17:55:58.584358 pymathematics-2023.5.6/setup.cfg
+-rwxrwxrwx   0 sahil-rajwar  (1000) sahil-rajwar  (1000)      695 2023-05-06 11:17:28.000000 pymathematics-2023.5.6/setup.py
```

### Comparing `pymathematics-2023.5.3.1/LICENSE` & `pymathematics-2023.5.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pymathematics-2023.5.3.1/pymathematics/__init__.py` & `pymathematics-2023.5.6/pymathematics/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 Provides
   1. fast and accurate calculations
   2. work with vectors, matrices and sets
   3. statistics, basic mathematics calculation
 
   >>> from pymathematics import *
   >>> about.version
-  ... 2023.4.28
+  ... 2023.5.6
   >>> about.homepage
   ... "https://github.com/Sahil-Rajwar-2004/pymathematics"
   >>> sqrt(4)
   ... 2.0
   >>> constants.inf
   ... inf
   >>> constants.pi
@@ -21,15 +21,14 @@
   >>> constants.e
   ... 2.7182818284590452353602874713527
   >>> mean([1,2,3,4,5])
   ... 5.5
 """
 
 import sympy
-
 from .info import (
     author,version,homepage
 )
 
 class about:
     author = author
     version = version
@@ -37,14 +36,50 @@
 
 class constants:
     pi = 3.1415926535897932384626433832795
     e = 2.7182818284590452353602874713527
     inf = float("inf")
     nan = float("nan")
 
+class absolute_zero_temperature:
+    kelvin = 0
+    celsius = -273.15
+    fahrenheit = -459.67
+
+class temperature:
+    def c2k(celsius):
+        if celsius < absolute_zero_temperature.celsius:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return celsius+273.15
+
+    def c2f(celsius):
+        if celsius < absolute_zero_temperature.celsius:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return celsius*1.8+32
+
+    def k2c(kelvin):
+        if kelvin < absolute_zero_temperature.kelvin:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return kelvin-273.15
+
+    def k2f(kelvin):
+        if kelvin < absolute_zero_temperature.kelvin:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return temperature.k2c(kelvin)*1.8+32
+
+    def f2c(fahrenheit):
+        if fahrenheit < absolute_zero_temperature.fahrenheit:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return (fahrenheit-32)*0.5556
+
+    def f2k(fahrenheit):
+        if fahrenheit < absolute_zero_temperature.fahrenheit:
+            raise ValueError("below absolute zero temperature doesn't exist")
+        return temperature.f2c(fahrenheit)+273.15
+
 class vector:
     def cross_product(vector1:list,vector2:list) -> int|float:
         if len(vector1) != 3 or len(vector2) != 3:
             raise ValueError("vector should have 3 directions")
         return [vector1[1]*vector2[2]-vector2[1]*vector1[2],-(vector1[0]*vector2[2]-vector2[0]*vector1[2]),vector1[0]*vector2[1]-vector2[0]*vector1[1]]
 
     def dot_product(vector1:list,vector2:list) -> int|float:
@@ -827,7 +862,10 @@
     result = []
     std_dev = standard_deviation(array)
     m = mean(array)
     for x in array:
         each = (1/(std_dev*sqrt(2*constants.pi)))*exp(-((x-m)**2)/(2*(std_dev**2)))
         result.append(each)
     return result
+
+def sigmoid(x:int) -> float:
+    return 1/(1+constants.e**(-x))
```

### Comparing `pymathematics-2023.5.3.1/setup.py` & `pymathematics-2023.5.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup,find_packages
 
 setup(
     name = "pymathematics",
-    version = "2023.5.3.1",
+    version = "2023.5.6",
     description = "package for mathematics",
     long_description = "for more info, check the github repository",
     author = "Sahil Rajwar",
     maintainer = "its_Sahil",
     author_email = "justsahilrajwar2004@gmail.com",
     packages = ["pymathematics"],
     license = "MIT",
```

