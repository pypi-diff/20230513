# Comparing `tmp/num7-1.0.27.tar.gz` & `tmp/num7-1.0.28.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "num7-1.0.27.tar", last modified: Fri Feb 24 11:02:28 2023, max compression
+gzip compressed data, was "num7-1.0.28.tar", last modified: Sat May 13 12:17:22 2023, max compression
```

## Comparing `num7-1.0.27.tar` & `num7-1.0.28.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-02-24 11:02:28.623904 num7-1.0.27/
--rw-rw-rw-   0        0        0     1076 2022-12-08 18:40:54.000000 num7-1.0.27/LICENSE.txt
--rw-rw-rw-   0        0        0    20208 2023-02-24 11:02:28.618902 num7-1.0.27/PKG-INFO
--rw-rw-rw-   0        0        0    19720 2023-02-24 10:01:58.000000 num7-1.0.27/README.md
--rw-rw-rw-   0        0        0       42 2023-02-24 11:02:28.623904 num7-1.0.27/setup.cfg
--rw-rw-rw-   0        0        0      743 2023-02-24 10:58:32.000000 num7-1.0.27/setup.py
-drwxrwxrwx   0        0        0        0 2023-02-24 11:02:28.603905 num7-1.0.27/src/
-drwxrwxrwx   0        0        0        0 2023-02-24 11:02:28.618902 num7-1.0.27/src/num7.egg-info/
--rw-rw-rw-   0        0        0    20208 2023-02-24 11:02:28.000000 num7-1.0.27/src/num7.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      170 2023-02-24 11:02:28.000000 num7-1.0.27/src/num7.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-24 11:02:28.000000 num7-1.0.27/src/num7.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        5 2023-02-24 11:02:28.000000 num7-1.0.27/src/num7.egg-info/top_level.txt
--rw-rw-rw-   0        0        0    62366 2023-02-24 10:35:32.000000 num7-1.0.27/src/num7.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:17:22.087031 num7-1.0.28/
+-rw-rw-rw-   0        0        0     1076 2023-02-24 11:37:18.000000 num7-1.0.28/LICENSE.txt
+-rw-rw-rw-   0        0        0    20208 2023-05-13 12:17:22.083068 num7-1.0.28/PKG-INFO
+-rw-rw-rw-   0        0        0    19720 2023-02-24 10:01:58.000000 num7-1.0.28/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:17:22.087031 num7-1.0.28/setup.cfg
+-rw-rw-rw-   0        0        0      743 2023-05-13 12:12:12.000000 num7-1.0.28/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:17:22.063141 num7-1.0.28/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 12:17:22.081726 num7-1.0.28/src/num7.egg-info/
+-rw-rw-rw-   0        0        0    20208 2023-05-13 12:17:21.000000 num7-1.0.28/src/num7.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      170 2023-05-13 12:17:21.000000 num7-1.0.28/src/num7.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:17:21.000000 num7-1.0.28/src/num7.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        5 2023-05-13 12:17:21.000000 num7-1.0.28/src/num7.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0    62483 2023-05-13 12:07:09.000000 num7-1.0.28/src/num7.py
```

### Comparing `num7-1.0.27/LICENSE.txt` & `num7-1.0.28/LICENSE.txt`

 * *Files 10% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 
 
 MIT License
 
-Copyright (c) 2022 giocip
+Copyright (c) 2023 giocip
 
 Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
 
 The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
 
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

### Comparing `num7-1.0.27/PKG-INFO` & `num7-1.0.28/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: num7
-Version: 1.0.27
+Version: 1.0.28
 Summary: Num - SUPREME PRECISION GENERAL PURPOSE ARITHMETIC-LOGIC DECIMAL CLASS
 Home-page: https://github.com/giocip/num7
 Author: giocip
 Author-email: giocip7@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.11
```

### Comparing `num7-1.0.27/README.md` & `num7-1.0.28/README.md`

 * *Files identical despite different names*

### Comparing `num7-1.0.27/setup.py` & `num7-1.0.28/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup
 # read the contents of your README file
 from pathlib import Path
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
 setup(name='num7',
-	  version='1.0.27',
+	  version='1.0.28',
 	  description='Num - SUPREME PRECISION GENERAL PURPOSE ARITHMETIC-LOGIC DECIMAL CLASS',
       long_description=long_description,
       long_description_content_type='text/markdown',
 	  py_modules=['num7'],
 	  package_dir={'': 'src'},
 	  url='https://github.com/giocip/num7',
 	  author='giocip',
```

### Comparing `num7-1.0.27/src/num7.egg-info/PKG-INFO` & `num7-1.0.28/src/num7.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: num7
-Version: 1.0.27
+Version: 1.0.28
 Summary: Num - SUPREME PRECISION GENERAL PURPOSE ARITHMETIC-LOGIC DECIMAL CLASS
 Home-page: https://github.com/giocip/num7
 Author: giocip
 Author-email: giocip7@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3.11
```

### Comparing `num7-1.0.27/src/num7.py` & `num7-1.0.28/src/num7.py`

 * *Files 0% similar despite different names*

```diff
@@ -540,15 +540,15 @@
         else:
             self.n2 = '' #positive
         if self.L_n0 > 1:
             self.n0 = self.n0.lstrip('0') #clear LEFT  zeros
             if not len(self.n0): #if ''
                 self.n0 = '0'
         if self.L_n1 > 1:
-            self.n1 = self.n1.rstrip('0') #clear RIGTH zeros
+            self.n1 = self.n1.rstrip('0') #clear RIGHT zeros
             if not len(self.n1): #if ''
                 self.n1 = '0'                
         self.L_n0 = len(self.n0); self.L_n1 = len(self.n1) #check for new len       
         self.n = self.n2 + self.n0 + '.' + self.n1         #set all number cleaned 
         if self.n0 == '0' and self.n1 == '0': # zero get not any sign == BE CAREFUL!
             if self.n2 == '-' or n[0] == '+':
                 raise ValueError("Num.__init__ => zero can not be signed:", n)    																				  
@@ -806,14 +806,16 @@
     
     def __truediv__(self, sob) -> 'Num': 
         ''' (/) overloading binary floating point division operator  '''
         if type(sob) == int or Num.is_numstr(sob):
            sob = Num(sob)
         if type(sob) != Num:
             raise TypeError("Num.__truediv__ => type not valid:", sob)																	  
+        if sob == '0.0':
+            raise Exception('Num.__truediv__ => ZeroDivisionError: Num division by zero')
         if self.n == '0.0':
             return Num('0.0')
         if self.L_n1 > sob.L_n1:
             ze = self.L_n1 - sob.L_n1
             x1 = int(self.n2 + self.n0 + self.n1); x2 = int(sob.n2 + sob.n0 + sob.n1 + ze*'0')                 
             x3 = Num._divi_(x1, x2, self.d if self.d > sob.d else sob.d)
         else:
```

