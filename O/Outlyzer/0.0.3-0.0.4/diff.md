# Comparing `tmp/Outlyzer-0.0.3.tar.gz` & `tmp/Outlyzer-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Outlyzer-0.0.3.tar", last modified: Thu Apr 27 16:23:51 2023, max compression
+gzip compressed data, was "Outlyzer-0.0.4.tar", last modified: Sat May 13 09:51:28 2023, max compression
```

## Comparing `Outlyzer-0.0.3.tar` & `Outlyzer-0.0.4.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-04-27 16:23:51.570791 Outlyzer-0.0.3/
--rw-rw-rw-   0        0        0    11558 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/LICENSE
-drwxrwxrwx   0        0        0        0 2023-04-27 16:23:51.539548 Outlyzer-0.0.3/Outlyzer/
--rw-rw-rw-   0        0        0        0 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/Outlyzer/__init__.py
--rw-rw-rw-   0        0        0      831 2023-04-27 16:20:33.000000 Outlyzer-0.0.3/Outlyzer/iqr.py
--rw-rw-rw-   0        0        0      730 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/Outlyzer/least_squares.py
--rw-rw-rw-   0        0        0      641 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/Outlyzer/probabilistic.py
--rw-rw-rw-   0        0        0      988 2023-04-24 14:36:53.000000 Outlyzer-0.0.3/Outlyzer/visual.py
--rw-rw-rw-   0        0        0      644 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/Outlyzer/zscore.py
-drwxrwxrwx   0        0        0        0 2023-04-27 16:23:51.570791 Outlyzer-0.0.3/Outlyzer.egg-info/
--rw-rw-rw-   0        0        0     1529 2023-04-27 16:23:51.000000 Outlyzer-0.0.3/Outlyzer.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      312 2023-04-27 16:23:51.000000 Outlyzer-0.0.3/Outlyzer.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-27 16:23:51.000000 Outlyzer-0.0.3/Outlyzer.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       30 2023-04-27 16:23:51.000000 Outlyzer-0.0.3/Outlyzer.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-04-27 16:23:51.000000 Outlyzer-0.0.3/Outlyzer.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1529 2023-04-27 16:23:51.570791 Outlyzer-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0      870 2023-04-24 08:52:04.000000 Outlyzer-0.0.3/README.md
--rw-rw-rw-   0        0        0       42 2023-04-27 16:23:51.570791 Outlyzer-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0     1030 2023-04-27 16:20:44.000000 Outlyzer-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:51:28.898265 Outlyzer-0.0.4/
+-rw-rw-rw-   0        0        0    22951 2023-04-27 17:20:22.000000 Outlyzer-0.0.4/LICENSE
+drwxrwxrwx   0        0        0        0 2023-05-13 09:51:28.838379 Outlyzer-0.0.4/Outlyzer/
+-rw-rw-rw-   0        0        0        0 2023-04-27 17:20:22.000000 Outlyzer-0.0.4/Outlyzer/__init__.py
+-rw-rw-rw-   0        0        0      807 2023-05-13 09:48:47.000000 Outlyzer-0.0.4/Outlyzer/iqr.py
+-rw-rw-rw-   0        0        0      708 2023-05-13 09:49:00.000000 Outlyzer-0.0.4/Outlyzer/least_squares.py
+-rw-rw-rw-   0        0        0      622 2023-05-13 09:49:11.000000 Outlyzer-0.0.4/Outlyzer/probabilistic.py
+-rw-rw-rw-   0        0        0      952 2023-05-13 09:49:24.000000 Outlyzer-0.0.4/Outlyzer/visual.py
+-rw-rw-rw-   0        0        0      624 2023-05-13 09:49:34.000000 Outlyzer-0.0.4/Outlyzer/zscore.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:51:28.889717 Outlyzer-0.0.4/Outlyzer.egg-info/
+-rw-rw-rw-   0        0        0     1842 2023-05-13 09:51:28.000000 Outlyzer-0.0.4/Outlyzer.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      312 2023-05-13 09:51:28.000000 Outlyzer-0.0.4/Outlyzer.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 09:51:28.000000 Outlyzer-0.0.4/Outlyzer.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       30 2023-05-13 09:51:28.000000 Outlyzer-0.0.4/Outlyzer.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 09:51:28.000000 Outlyzer-0.0.4/Outlyzer.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1842 2023-05-13 09:51:28.896271 Outlyzer-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0     1183 2023-04-27 17:20:22.000000 Outlyzer-0.0.4/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 09:51:28.899408 Outlyzer-0.0.4/setup.cfg
+-rw-rw-rw-   0        0        0     1030 2023-05-13 09:51:11.000000 Outlyzer-0.0.4/setup.py
```

### Comparing `Outlyzer-0.0.3/Outlyzer/least_squares.py` & `Outlyzer-0.0.4/Outlyzer/least_squares.py`

 * *Ordering differences only*

 * *Files 21% similar despite different names*

```diff
@@ -1,22 +1,22 @@
-from sklearn.decomposition import PCA
-from sklearn.linear_model import RANSACRegressor
-import numpy as np
-
-def detect_outliers_linear_regression(data):
-    """
-    Detect outliers using linear regression models (PCA, LMS) method.
-    
-    Parameters:
-        - data (numpy array or pandas DataFrame): Input data
-        
-    Returns:
-        - outliers (list): List of outlier indices
-    """
-    pca = PCA(n_components=1)
-    principal_components = pca.fit_transform(data)
-    residuals = data - pca.inverse_transform(principal_components)
-    
-    model = RANSACRegressor()
-    model.fit(principal_components, residuals)
-    outliers = np.where(model.inlier_mask_ == False)[0]
-    return outliers.tolist()
+from sklearn.decomposition import PCA
+from sklearn.linear_model import RANSACRegressor
+import numpy as np
+
+def detect_outliers_linear_regression(data):
+    """
+    Detect outliers using linear regression models (PCA, LMS) method.
+    
+    Parameters:
+        - data (numpy array or pandas DataFrame): Input data
+        
+    Returns:
+        - outliers (list): List of outlier indices
+    """
+    pca = PCA(n_components=1)
+    principal_components = pca.fit_transform(data)
+    residuals = data - pca.inverse_transform(principal_components)
+    
+    model = RANSACRegressor()
+    model.fit(principal_components, residuals)
+    outliers = np.where(model.inlier_mask_ == False)[0]
+    return outliers.tolist()
```

### Comparing `Outlyzer-0.0.3/Outlyzer.egg-info/PKG-INFO` & `Outlyzer-0.0.4/Outlyzer.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310d 0a4e 616d 653a 204f 7574  : 2.1..Name: Out
 00000020: 6c79 7a65 720d 0a56 6572 7369 6f6e 3a20  lyzer..Version: 
-00000030: 302e 302e 330d 0a53 756d 6d61 7279 3a20  0.0.3..Summary: 
+00000030: 302e 302e 340d 0a53 756d 6d61 7279 3a20  0.0.4..Summary: 
 00000040: 4f75 746c 6965 7220 6465 7465 6374 696f  Outlier detectio
 00000050: 6e0d 0a48 6f6d 652d 7061 6765 3a20 6874  n..Home-page: ht
 00000060: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
 00000070: 2f44 6576 7061 7269 6861 7235 2f4f 7574  /Devparihar5/Out
 00000080: 6c79 7a65 720d 0a41 7574 686f 723a 2044  lyzer..Author: D
 00000090: 6576 656e 6472 6120 5061 7269 6861 720d  evendra Parihar.
 000000a0: 0a41 7574 686f 722d 656d 6169 6c3a 2064  .Author-email: d
@@ -58,39 +58,59 @@
 00000390: 6720 6f75 746c 6965 7273 2c20 6173 2077  g outliers, as w
 000003a0: 656c 6c20 6173 2076 6973 7561 6c69 7a61  ell as visualiza
 000003b0: 7469 6f6e 2d62 6173 6564 206d 6574 686f  tion-based metho
 000003c0: 6473 2075 7369 6e67 2073 6361 7474 6572  ds using scatter
 000003d0: 2070 6c6f 7473 2c20 626f 7820 706c 6f74   plots, box plot
 000003e0: 732c 2061 6e64 206f 7468 6572 2074 7970  s, and other typ
 000003f0: 6573 206f 6620 7669 7375 616c 697a 6174  es of visualizat
-00000400: 696f 6e73 2e0d 0a0d 0a55 7361 6765 3a0d  ions.....Usage:.
-00000410: 0a0d 0a20 2020 202d 2049 6d70 6f72 7420  ...    - Import 
-00000420: 7468 6520 6465 7369 7265 6420 6d65 7468  the desired meth
-00000430: 6f64 2066 726f 6d20 7468 6520 6c69 6272  od from the libr
-00000440: 6172 792c 2065 2e67 2e3a 0d0a 2020 2020  ary, e.g.:..    
-00000450: 2020 2020 6672 6f6d 204f 7574 6c79 7a65      from Outlyze
-00000460: 722e 7a73 636f 7265 2069 6d70 6f72 7420  r.zscore import 
-00000470: 6465 7465 6374 5f6f 7574 6c69 6572 735f  detect_outliers_
-00000480: 7a73 636f 7265 2020 2020 2020 2020 0d0a  zscore        ..
-00000490: 2020 2020 2020 2020 6672 6f6d 204f 7574          from Out
-000004a0: 6c79 7a65 722e 6971 7220 696d 706f 7274  lyzer.iqr import
-000004b0: 2064 6574 6563 745f 6f75 746c 6965 7273   detect_outliers
-000004c0: 5f69 7172 0d0a 0d0a 2020 2020 2d20 5061  _iqr....    - Pa
-000004d0: 7373 2079 6f75 7220 6461 7461 7365 7420  ss your dataset 
-000004e0: 6f72 2064 6174 6120 7365 7269 6573 2074  or data series t
-000004f0: 6f20 7468 6520 7265 7370 6563 7469 7665  o the respective
-00000500: 2066 756e 6374 696f 6e2c 2065 2e67 2e3a   function, e.g.:
-00000510: 0d0a 2020 2020 2020 2020 6f75 746c 6965  ..        outlie
-00000520: 7273 5f7a 7363 6f72 6520 3d20 6465 7465  rs_zscore = dete
-00000530: 6374 5f6f 7574 6c69 6572 735f 7a73 636f  ct_outliers_zsco
-00000540: 7265 2864 6174 6129 0d0a 2020 2020 2020  re(data)..      
-00000550: 2020 6f75 746c 6965 7273 5f69 7172 203d    outliers_iqr =
-00000560: 2064 6574 6563 745f 6f75 746c 6965 7273   detect_outliers
-00000570: 5f69 7172 2864 6174 6129 0d0a 2020 2020  _iqr(data)..    
-00000580: 0d0a 2020 2020 5468 6520 6675 6e63 7469  ..    The functi
-00000590: 6f6e 7320 7769 6c6c 2072 6574 7572 6e20  ons will return 
-000005a0: 6120 626f 6f6c 6561 6e20 6172 7261 7920  a boolean array 
-000005b0: 696e 6469 6361 7469 6e67 2077 6865 7468  indicating wheth
-000005c0: 6572 2065 6163 6820 6461 7461 2070 6f69  er each data poi
-000005d0: 6e74 2069 7320 616e 206f 7574 6c69 6572  nt is an outlier
-000005e0: 2028 5472 7565 2920 6f72 206e 6f74 2028   (True) or not (
-000005f0: 4661 6c73 6529 2e0d 0a                   False)...
+00000400: 696f 6e73 2e0d 0a0d 0a0d 0a23 2320 496e  ions.......## In
+00000410: 7374 616c 6c61 7469 6f6e 0d0a 596f 7520  stallation..You 
+00000420: 6361 6e20 696e 7374 616c 6c20 4f75 746c  can install Outl
+00000430: 797a 6572 2075 7369 6e67 2070 6970 3a0d  yzer using pip:.
+00000440: 0a60 6060 0d0a 7069 7020 696e 7374 616c  .```..pip instal
+00000450: 6c20 6f75 746c 797a 6572 0d0a 6060 600d  l outlyzer..```.
+00000460: 0a0d 0a0d 0a55 7361 6765 3a0d 0a0d 0a20  .....Usage:.... 
+00000470: 2020 202d 2049 6d70 6f72 7420 7468 6520     - Import the 
+00000480: 6465 7369 7265 6420 6d65 7468 6f64 2066  desired method f
+00000490: 726f 6d20 7468 6520 6c69 6272 6172 792c  rom the library,
+000004a0: 2065 2e67 2e3a 0d0a 2020 2020 2020 2020   e.g.:..        
+000004b0: 6672 6f6d 204f 7574 6c79 7a65 722e 7a73  from Outlyzer.zs
+000004c0: 636f 7265 2069 6d70 6f72 7420 6465 7465  core import dete
+000004d0: 6374 5f6f 7574 6c69 6572 735f 7a73 636f  ct_outliers_zsco
+000004e0: 7265 2020 2020 2020 2020 0d0a 2020 2020  re        ..    
+000004f0: 2020 2020 6672 6f6d 204f 7574 6c79 7a65      from Outlyze
+00000500: 722e 6971 7220 696d 706f 7274 2064 6574  r.iqr import det
+00000510: 6563 745f 6f75 746c 6965 7273 5f69 7172  ect_outliers_iqr
+00000520: 0d0a 0d0a 2020 2020 2d20 5061 7373 2079  ....    - Pass y
+00000530: 6f75 7220 6461 7461 7365 7420 6f72 2064  our dataset or d
+00000540: 6174 6120 7365 7269 6573 2074 6f20 7468  ata series to th
+00000550: 6520 7265 7370 6563 7469 7665 2066 756e  e respective fun
+00000560: 6374 696f 6e2c 2065 2e67 2e3a 0d0a 2020  ction, e.g.:..  
+00000570: 2020 2020 2020 6f75 746c 6965 7273 5f7a        outliers_z
+00000580: 7363 6f72 6520 3d20 6465 7465 6374 5f6f  score = detect_o
+00000590: 7574 6c69 6572 735f 7a73 636f 7265 2864  utliers_zscore(d
+000005a0: 6174 6129 0d0a 2020 2020 2020 2020 6f75  ata)..        ou
+000005b0: 746c 6965 7273 5f69 7172 203d 2064 6574  tliers_iqr = det
+000005c0: 6563 745f 6f75 746c 6965 7273 5f69 7172  ect_outliers_iqr
+000005d0: 2864 6174 6129 0d0a 2020 2020 0d0a 2020  (data)..    ..  
+000005e0: 2020 5468 6520 6675 6e63 7469 6f6e 7320    The functions 
+000005f0: 7769 6c6c 2072 6574 7572 6e20 6120 626f  will return a bo
+00000600: 6f6c 6561 6e20 6172 7261 7920 696e 6469  olean array indi
+00000610: 6361 7469 6e67 2077 6865 7468 6572 2065  cating whether e
+00000620: 6163 6820 6461 7461 2070 6f69 6e74 2069  ach data point i
+00000630: 7320 616e 206f 7574 6c69 6572 2028 5472  s an outlier (Tr
+00000640: 7565 2920 6f72 206e 6f74 2028 4661 6c73  ue) or not (Fals
+00000650: 6529 2e0d 0a0d 0a0d 0a23 2320 0d0a 3c70  e).......## ..<p
+00000660: 2061 6c69 676e 3d22 6365 6e74 6572 223e   align="center">
+00000670: 0d0a 2020 3c61 2068 7265 663d 2268 7474  ..  <a href="htt
+00000680: 7073 3a2f 2f73 7461 722d 6869 7374 6f72  ps://star-histor
+00000690: 792e 636f 6d2f 2364 6576 7061 7269 6861  y.com/#devpariha
+000006a0: 7235 2f4f 7574 6c79 7a65 7226 4461 7465  r5/Outlyzer&Date
+000006b0: 223e 0d0a 2020 2020 3c69 6d67 2073 7263  ">..    <img src
+000006c0: 3d22 6874 7470 733a 2f2f 6170 692e 7374  ="https://api.st
+000006d0: 6172 2d68 6973 746f 7279 2e63 6f6d 2f73  ar-history.com/s
+000006e0: 7667 3f72 6570 6f73 3d44 6576 7061 7269  vg?repos=Devpari
+000006f0: 6861 7235 2f4f 7574 6c79 7a65 7226 7479  har5/Outlyzer&ty
+00000700: 7065 3d44 6174 6522 2061 6c74 3d22 5374  pe=Date" alt="St
+00000710: 6172 2048 6973 746f 7279 2043 6861 7274  ar History Chart
+00000720: 223e 0d0a 2020 3c2f 613e 0d0a 3c2f 703e  ">..  </a>..</p>
+00000730: 0d0a                                     ..
```

### Comparing `Outlyzer-0.0.3/PKG-INFO` & `Outlyzer-0.0.4/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310d 0a4e 616d 653a 204f 7574  : 2.1..Name: Out
 00000020: 6c79 7a65 720d 0a56 6572 7369 6f6e 3a20  lyzer..Version: 
-00000030: 302e 302e 330d 0a53 756d 6d61 7279 3a20  0.0.3..Summary: 
+00000030: 302e 302e 340d 0a53 756d 6d61 7279 3a20  0.0.4..Summary: 
 00000040: 4f75 746c 6965 7220 6465 7465 6374 696f  Outlier detectio
 00000050: 6e0d 0a48 6f6d 652d 7061 6765 3a20 6874  n..Home-page: ht
 00000060: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
 00000070: 2f44 6576 7061 7269 6861 7235 2f4f 7574  /Devparihar5/Out
 00000080: 6c79 7a65 720d 0a41 7574 686f 723a 2044  lyzer..Author: D
 00000090: 6576 656e 6472 6120 5061 7269 6861 720d  evendra Parihar.
 000000a0: 0a41 7574 686f 722d 656d 6169 6c3a 2064  .Author-email: d
@@ -58,39 +58,59 @@
 00000390: 6720 6f75 746c 6965 7273 2c20 6173 2077  g outliers, as w
 000003a0: 656c 6c20 6173 2076 6973 7561 6c69 7a61  ell as visualiza
 000003b0: 7469 6f6e 2d62 6173 6564 206d 6574 686f  tion-based metho
 000003c0: 6473 2075 7369 6e67 2073 6361 7474 6572  ds using scatter
 000003d0: 2070 6c6f 7473 2c20 626f 7820 706c 6f74   plots, box plot
 000003e0: 732c 2061 6e64 206f 7468 6572 2074 7970  s, and other typ
 000003f0: 6573 206f 6620 7669 7375 616c 697a 6174  es of visualizat
-00000400: 696f 6e73 2e0d 0a0d 0a55 7361 6765 3a0d  ions.....Usage:.
-00000410: 0a0d 0a20 2020 202d 2049 6d70 6f72 7420  ...    - Import 
-00000420: 7468 6520 6465 7369 7265 6420 6d65 7468  the desired meth
-00000430: 6f64 2066 726f 6d20 7468 6520 6c69 6272  od from the libr
-00000440: 6172 792c 2065 2e67 2e3a 0d0a 2020 2020  ary, e.g.:..    
-00000450: 2020 2020 6672 6f6d 204f 7574 6c79 7a65      from Outlyze
-00000460: 722e 7a73 636f 7265 2069 6d70 6f72 7420  r.zscore import 
-00000470: 6465 7465 6374 5f6f 7574 6c69 6572 735f  detect_outliers_
-00000480: 7a73 636f 7265 2020 2020 2020 2020 0d0a  zscore        ..
-00000490: 2020 2020 2020 2020 6672 6f6d 204f 7574          from Out
-000004a0: 6c79 7a65 722e 6971 7220 696d 706f 7274  lyzer.iqr import
-000004b0: 2064 6574 6563 745f 6f75 746c 6965 7273   detect_outliers
-000004c0: 5f69 7172 0d0a 0d0a 2020 2020 2d20 5061  _iqr....    - Pa
-000004d0: 7373 2079 6f75 7220 6461 7461 7365 7420  ss your dataset 
-000004e0: 6f72 2064 6174 6120 7365 7269 6573 2074  or data series t
-000004f0: 6f20 7468 6520 7265 7370 6563 7469 7665  o the respective
-00000500: 2066 756e 6374 696f 6e2c 2065 2e67 2e3a   function, e.g.:
-00000510: 0d0a 2020 2020 2020 2020 6f75 746c 6965  ..        outlie
-00000520: 7273 5f7a 7363 6f72 6520 3d20 6465 7465  rs_zscore = dete
-00000530: 6374 5f6f 7574 6c69 6572 735f 7a73 636f  ct_outliers_zsco
-00000540: 7265 2864 6174 6129 0d0a 2020 2020 2020  re(data)..      
-00000550: 2020 6f75 746c 6965 7273 5f69 7172 203d    outliers_iqr =
-00000560: 2064 6574 6563 745f 6f75 746c 6965 7273   detect_outliers
-00000570: 5f69 7172 2864 6174 6129 0d0a 2020 2020  _iqr(data)..    
-00000580: 0d0a 2020 2020 5468 6520 6675 6e63 7469  ..    The functi
-00000590: 6f6e 7320 7769 6c6c 2072 6574 7572 6e20  ons will return 
-000005a0: 6120 626f 6f6c 6561 6e20 6172 7261 7920  a boolean array 
-000005b0: 696e 6469 6361 7469 6e67 2077 6865 7468  indicating wheth
-000005c0: 6572 2065 6163 6820 6461 7461 2070 6f69  er each data poi
-000005d0: 6e74 2069 7320 616e 206f 7574 6c69 6572  nt is an outlier
-000005e0: 2028 5472 7565 2920 6f72 206e 6f74 2028   (True) or not (
-000005f0: 4661 6c73 6529 2e0d 0a                   False)...
+00000400: 696f 6e73 2e0d 0a0d 0a0d 0a23 2320 496e  ions.......## In
+00000410: 7374 616c 6c61 7469 6f6e 0d0a 596f 7520  stallation..You 
+00000420: 6361 6e20 696e 7374 616c 6c20 4f75 746c  can install Outl
+00000430: 797a 6572 2075 7369 6e67 2070 6970 3a0d  yzer using pip:.
+00000440: 0a60 6060 0d0a 7069 7020 696e 7374 616c  .```..pip instal
+00000450: 6c20 6f75 746c 797a 6572 0d0a 6060 600d  l outlyzer..```.
+00000460: 0a0d 0a0d 0a55 7361 6765 3a0d 0a0d 0a20  .....Usage:.... 
+00000470: 2020 202d 2049 6d70 6f72 7420 7468 6520     - Import the 
+00000480: 6465 7369 7265 6420 6d65 7468 6f64 2066  desired method f
+00000490: 726f 6d20 7468 6520 6c69 6272 6172 792c  rom the library,
+000004a0: 2065 2e67 2e3a 0d0a 2020 2020 2020 2020   e.g.:..        
+000004b0: 6672 6f6d 204f 7574 6c79 7a65 722e 7a73  from Outlyzer.zs
+000004c0: 636f 7265 2069 6d70 6f72 7420 6465 7465  core import dete
+000004d0: 6374 5f6f 7574 6c69 6572 735f 7a73 636f  ct_outliers_zsco
+000004e0: 7265 2020 2020 2020 2020 0d0a 2020 2020  re        ..    
+000004f0: 2020 2020 6672 6f6d 204f 7574 6c79 7a65      from Outlyze
+00000500: 722e 6971 7220 696d 706f 7274 2064 6574  r.iqr import det
+00000510: 6563 745f 6f75 746c 6965 7273 5f69 7172  ect_outliers_iqr
+00000520: 0d0a 0d0a 2020 2020 2d20 5061 7373 2079  ....    - Pass y
+00000530: 6f75 7220 6461 7461 7365 7420 6f72 2064  our dataset or d
+00000540: 6174 6120 7365 7269 6573 2074 6f20 7468  ata series to th
+00000550: 6520 7265 7370 6563 7469 7665 2066 756e  e respective fun
+00000560: 6374 696f 6e2c 2065 2e67 2e3a 0d0a 2020  ction, e.g.:..  
+00000570: 2020 2020 2020 6f75 746c 6965 7273 5f7a        outliers_z
+00000580: 7363 6f72 6520 3d20 6465 7465 6374 5f6f  score = detect_o
+00000590: 7574 6c69 6572 735f 7a73 636f 7265 2864  utliers_zscore(d
+000005a0: 6174 6129 0d0a 2020 2020 2020 2020 6f75  ata)..        ou
+000005b0: 746c 6965 7273 5f69 7172 203d 2064 6574  tliers_iqr = det
+000005c0: 6563 745f 6f75 746c 6965 7273 5f69 7172  ect_outliers_iqr
+000005d0: 2864 6174 6129 0d0a 2020 2020 0d0a 2020  (data)..    ..  
+000005e0: 2020 5468 6520 6675 6e63 7469 6f6e 7320    The functions 
+000005f0: 7769 6c6c 2072 6574 7572 6e20 6120 626f  will return a bo
+00000600: 6f6c 6561 6e20 6172 7261 7920 696e 6469  olean array indi
+00000610: 6361 7469 6e67 2077 6865 7468 6572 2065  cating whether e
+00000620: 6163 6820 6461 7461 2070 6f69 6e74 2069  ach data point i
+00000630: 7320 616e 206f 7574 6c69 6572 2028 5472  s an outlier (Tr
+00000640: 7565 2920 6f72 206e 6f74 2028 4661 6c73  ue) or not (Fals
+00000650: 6529 2e0d 0a0d 0a0d 0a23 2320 0d0a 3c70  e).......## ..<p
+00000660: 2061 6c69 676e 3d22 6365 6e74 6572 223e   align="center">
+00000670: 0d0a 2020 3c61 2068 7265 663d 2268 7474  ..  <a href="htt
+00000680: 7073 3a2f 2f73 7461 722d 6869 7374 6f72  ps://star-histor
+00000690: 792e 636f 6d2f 2364 6576 7061 7269 6861  y.com/#devpariha
+000006a0: 7235 2f4f 7574 6c79 7a65 7226 4461 7465  r5/Outlyzer&Date
+000006b0: 223e 0d0a 2020 2020 3c69 6d67 2073 7263  ">..    <img src
+000006c0: 3d22 6874 7470 733a 2f2f 6170 692e 7374  ="https://api.st
+000006d0: 6172 2d68 6973 746f 7279 2e63 6f6d 2f73  ar-history.com/s
+000006e0: 7667 3f72 6570 6f73 3d44 6576 7061 7269  vg?repos=Devpari
+000006f0: 6861 7235 2f4f 7574 6c79 7a65 7226 7479  har5/Outlyzer&ty
+00000700: 7065 3d44 6174 6522 2061 6c74 3d22 5374  pe=Date" alt="St
+00000710: 6172 2048 6973 746f 7279 2043 6861 7274  ar History Chart
+00000720: 223e 0d0a 2020 3c2f 613e 0d0a 3c2f 703e  ">..  </a>..</p>
+00000730: 0d0a                                     ..
```

### Comparing `Outlyzer-0.0.3/setup.py` & `Outlyzer-0.0.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '0.0.3'
+VERSION = '0.0.4'
 DESCRIPTION = 'Outlier detection'
 with open('README.md', 'r') as f:
     LONG_DESCRIPTION = f.read()
 
 # Setting up
 setup(
     name="Outlyzer",
```

