# Comparing `tmp/dufuz-0.1.3-py3-none-any.whl.zip` & `tmp/dufuz-0.1.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,21 +1,21 @@
-Zip file size: 13366 bytes, number of entries: 19
+Zip file size: 13356 bytes, number of entries: 19
 -rw-rw-rw-  2.0 fat      106 b- defN 23-May-03 15:34 dufuz/__init__.py
 -rw-rw-rw-  2.0 fat      675 b- defN 23-May-07 10:55 dufuz/__main__.py
 -rw-rw-rw-  2.0 fat      704 b- defN 23-Apr-28 07:27 dufuz/defuzzify.py
 -rw-rw-rw-  2.0 fat     2394 b- defN 23-May-07 10:44 dufuz/dfn.py
 -rw-rw-rw-  2.0 fat      653 b- defN 23-Apr-29 09:10 dufuz/monitor.py
 -rw-rw-rw-  2.0 fat      479 b- defN 23-May-07 01:19 dufuz/negation.py
 -rw-rw-rw-  2.0 fat      339 b- defN 23-May-07 01:12 dufuz/tnorm.py
 -rw-rw-rw-  2.0 fat      104 b- defN 23-May-02 11:51 dufuz/core/__init__.py
 -rw-rw-rw-  2.0 fat     1150 b- defN 23-May-02 12:15 dufuz/core/domain.py
--rw-rw-rw-  2.0 fat     8055 b- defN 23-May-07 10:52 dufuz/core/environment.py
+-rw-rw-rw-  2.0 fat     8055 b- defN 23-May-13 20:41 dufuz/core/environment.py
 -rw-rw-rw-  2.0 fat     3751 b- defN 23-May-07 09:59 dufuz/core/number.py
 -rw-rw-rw-  2.0 fat       49 b- defN 23-May-02 21:48 dufuz/interpreter/__init__.py
--rw-rw-rw-  2.0 fat    13522 b- defN 23-May-10 18:28 dufuz/interpreter/interpret.py
+-rw-rw-rw-  2.0 fat    13490 b- defN 23-May-13 20:59 dufuz/interpreter/interpret.py
 -rw-rw-rw-  2.0 fat     1212 b- defN 23-May-06 08:07 dufuz/interpreter/lexer.py
 -rw-rw-rw-  2.0 fat     5265 b- defN 23-May-06 08:07 dufuz/interpreter/parser.py
--rw-rw-rw-  2.0 fat      899 b- defN 23-May-10 18:48 dufuz-0.1.3.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-May-10 18:48 dufuz-0.1.3.dist-info/WHEEL
--rw-rw-rw-  2.0 fat        6 b- defN 23-May-10 18:48 dufuz-0.1.3.dist-info/top_level.txt
-?rw-rw-r--  2.0 fat     1445 b- defN 23-May-10 18:48 dufuz-0.1.3.dist-info/RECORD
-19 files, 40900 bytes uncompressed, 11040 bytes compressed:  73.0%
+-rw-rw-rw-  2.0 fat      899 b- defN 23-May-13 21:00 dufuz-0.1.4.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-May-13 21:00 dufuz-0.1.4.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat        6 b- defN 23-May-13 21:00 dufuz-0.1.4.dist-info/top_level.txt
+?rw-rw-r--  2.0 fat     1445 b- defN 23-May-13 21:00 dufuz-0.1.4.dist-info/RECORD
+19 files, 40868 bytes uncompressed, 11030 bytes compressed:  73.0%
```

## zipnote {}

```diff
@@ -39,20 +39,20 @@
 
 Filename: dufuz/interpreter/lexer.py
 Comment: 
 
 Filename: dufuz/interpreter/parser.py
 Comment: 
 
-Filename: dufuz-0.1.3.dist-info/METADATA
+Filename: dufuz-0.1.4.dist-info/METADATA
 Comment: 
 
-Filename: dufuz-0.1.3.dist-info/WHEEL
+Filename: dufuz-0.1.4.dist-info/WHEEL
 Comment: 
 
-Filename: dufuz-0.1.3.dist-info/top_level.txt
+Filename: dufuz-0.1.4.dist-info/top_level.txt
 Comment: 
 
-Filename: dufuz-0.1.3.dist-info/RECORD
+Filename: dufuz-0.1.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## dufuz/interpreter/interpret.py

```diff
@@ -12,21 +12,20 @@
     def __call__(self, a, b=None, inc=None):
         if b is None:
             a, b = 0, a
         if inc is None:
             inc = 1
         x = a if isinstance(a, Number) else Number([1], Domain([a], self.env.spawner))
         while True:
-            next_x = x+inc
-            comparison = self.env.spawner.apply(operator.lt, next_x, b)  # treat crisp arithmetics as fuzzy too
+            comparison = self.env.spawner.apply(operator.lt, x, b)  # treat crisp arithmetics as fuzzy too
             if comparison.todict().get(True, 0) <= 0:
                 break
             toyield = self.env.spawner.If(comparison, x, None)
             yield toyield
-            x = next_x
+            x = x + inc
 
 
 class Variable:
     def __init__(self, executor, name):
         self.executor = executor
         self.name = name
```

## Comparing `dufuz-0.1.3.dist-info/METADATA` & `dufuz-0.1.4.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dufuz
-Version: 0.1.3
+Version: 0.1.4
 Summary: Discrete numeric fuzzy sets in Python algorithms.
 Home-page: https://github.com/maniospas/dufuz
 Author: Emmanouil (Manios) Krasanakis
 Author-email: maniospas@hotmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

