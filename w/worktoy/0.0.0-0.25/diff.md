# Comparing `tmp/worktoy-0.0.0.tar.gz` & `tmp/worktoy-0.25.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "worktoy-0.0.0.tar", last modified: Tue Apr 25 23:54:41 2023, max compression
+gzip compressed data, was "worktoy-0.25.tar", last modified: Sat May 13 03:51:54 2023, max compression
```

## Comparing `worktoy-0.0.0.tar` & `worktoy-0.25.tar`

### file list

```diff
@@ -1,20 +1,34 @@
-drwxrwxrwx   0        0        0        0 2023-04-25 23:54:41.623481 worktoy-0.0.0/
--rw-rw-rw-   0        0        0     1235 2023-04-25 23:29:20.000000 worktoy-0.0.0/LICENSE
--rw-rw-rw-   0        0        0       77 2023-04-25 23:54:41.623481 worktoy-0.0.0/PKG-INFO
--rw-rw-rw-   0        0        0       99 2023-04-25 23:40:59.000000 worktoy-0.0.0/README.md
--rw-rw-rw-   0        0        0       88 2023-04-25 23:54:24.000000 worktoy-0.0.0/pyproject.toml
--rw-rw-rw-   0        0        0      586 2023-04-25 23:54:41.625494 worktoy-0.0.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-04-25 23:54:41.607487 worktoy-0.0.0/src/
-drwxrwxrwx   0        0        0        0 2023-04-25 23:54:41.618486 worktoy-0.0.0/src/worktoy/
--rw-rw-rw-   0        0        0      701 2023-04-25 19:25:24.000000 worktoy-0.0.0/src/worktoy/__init__.py
--rw-rw-rw-   0        0        0     3617 2023-04-25 13:08:22.000000 worktoy-0.0.0/src/worktoy/_discio.py
--rw-rw-rw-   0        0        0     2011 2023-04-25 13:05:57.000000 worktoy-0.0.0/src/worktoy/_hashpipes.py
--rw-rw-rw-   0        0        0     2480 2023-04-25 19:28:22.000000 worktoy-0.0.0/src/worktoy/_maybe.py
--rw-rw-rw-   0        0        0      598 2023-04-25 12:46:35.000000 worktoy-0.0.0/src/worktoy/_parseerror.py
--rw-rw-rw-   0        0        0     2554 2023-04-25 14:19:11.000000 worktoy-0.0.0/src/worktoy/_stringtools.py
--rw-rw-rw-   0        0        0      503 2023-04-25 12:53:21.000000 worktoy-0.0.0/src/worktoy/_typenames.py
-drwxrwxrwx   0        0        0        0 2023-04-25 23:54:41.622481 worktoy-0.0.0/src/worktoy.egg-info/
--rw-rw-rw-   0        0        0       77 2023-04-25 23:54:41.000000 worktoy-0.0.0/src/worktoy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      358 2023-04-25 23:54:41.000000 worktoy-0.0.0/src/worktoy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-25 23:54:41.000000 worktoy-0.0.0/src/worktoy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-04-25 23:54:41.000000 worktoy-0.0.0/src/worktoy.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.305395 worktoy-0.25/
+-rw-rw-rw-   0        0        0     1096 2023-05-12 03:07:56.000000 worktoy-0.25/LICENSE
+-rw-rw-rw-   0        0        0     7155 2023-05-13 03:51:54.305395 worktoy-0.25/PKG-INFO
+-rw-rw-rw-   0        0        0     6650 2023-05-12 18:41:19.000000 worktoy-0.25/README.md
+-rw-rw-rw-   0        0        0      595 2023-05-13 03:09:55.000000 worktoy-0.25/pyproject.toml
+-rw-rw-rw-   0        0        0      585 2023-05-13 03:51:54.306396 worktoy-0.25/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.279425 worktoy-0.25/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.290341 worktoy-0.25/src/worktoy/
+-rw-rw-rw-   0        0        0      414 2023-05-12 18:45:18.000000 worktoy-0.25/src/worktoy/__init__.py
+-rw-rw-rw-   0        0        0      901 2023-05-12 19:25:01.000000 worktoy-0.25/src/worktoy/_anywayuwantit.py
+-rw-rw-rw-   0        0        0     3279 2023-05-12 20:26:22.000000 worktoy-0.25/src/worktoy/_callmemaybe.py
+-rw-rw-rw-   0        0        0      438 2023-05-12 06:13:52.000000 worktoy-0.25/src/worktoy/_maybe.py
+-rw-rw-rw-   0        0        0      497 2023-05-12 06:17:00.000000 worktoy-0.25/src/worktoy/_maybeType.py
+-rw-rw-rw-   0        0        0      775 2023-05-12 10:47:24.000000 worktoy-0.25/src/worktoy/_maybeTypes.py
+-rw-rw-rw-   0        0        0     3304 2023-05-12 09:36:50.000000 worktoy-0.25/src/worktoy/_searchKeys.py
+-rw-rw-rw-   0        0        0     2421 2023-05-12 11:53:37.000000 worktoy-0.25/src/worktoy/_stringlist.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.297124 worktoy-0.25/src/worktoy/mockdata/
+-rw-rw-rw-   0        0        0      234 2023-05-12 16:56:26.000000 worktoy-0.25/src/worktoy/mockdata/__init__.py
+-rw-rw-rw-   0        0        0     3575 2023-05-12 17:55:55.000000 worktoy-0.25/src/worktoy/mockdata/_intfactory.py
+-rw-rw-rw-   0        0        0      920 2023-05-12 10:47:13.000000 worktoy-0.25/src/worktoy/mockdata/_strfactory.py
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.295143 worktoy-0.25/src/worktoy.egg-info/
+-rw-rw-rw-   0        0        0     7155 2023-05-13 03:51:54.000000 worktoy-0.25/src/worktoy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      699 2023-05-13 03:51:54.000000 worktoy-0.25/src/worktoy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 03:51:54.000000 worktoy-0.25/src/worktoy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       13 2023-05-13 03:51:54.000000 worktoy-0.25/src/worktoy.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 03:51:54.303907 worktoy-0.25/tests/
+-rw-rw-rw-   0        0        0     5886 2023-05-12 09:45:06.000000 worktoy-0.25/tests/testSearchKeys.py
+-rw-rw-rw-   0        0        0     3145 2023-05-12 20:23:16.000000 worktoy-0.25/tests/test__callmemaybe.py
+-rw-rw-rw-   0        0        0     1163 2023-05-12 19:23:01.000000 worktoy-0.25/tests/test__intfactory.py
+-rw-rw-rw-   0        0        0      750 2023-05-12 07:23:58.000000 worktoy-0.25/tests/test__maybe.py
+-rw-rw-rw-   0        0        0     1141 2023-05-12 08:31:06.000000 worktoy-0.25/tests/test__maybeType.py
+-rw-rw-rw-   0        0        0     1722 2023-05-12 09:48:15.000000 worktoy-0.25/tests/test__maybeTypes.py
+-rw-rw-rw-   0        0        0     1553 2023-05-12 10:42:03.000000 worktoy-0.25/tests/test__strfactory.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 12:13:26.000000 worktoy-0.25/tests/test__stringlist.py
```

### Comparing `worktoy-0.0.0/setup.cfg` & `worktoy-0.25/setup.cfg`

 * *Files 3% similar despite different names*

```diff
@@ -1,37 +1,37 @@
 00000000: 5b4d 4554 4144 4154 415d 0d0a 6e61 6d65  [METADATA]..name
 00000010: 203d 2057 6f72 6b54 6f79 0d0a 7665 7273   = WorkToy..vers
-00000020: 696f 6e20 3d20 302e 3030 310d 0a61 7574  ion = 0.001..aut
-00000030: 686f 7220 3d20 4173 6765 7220 4a6f 6e20  hor = Asger Jon 
-00000040: 5669 7374 6973 656e 0d0a 6175 7468 6f72  Vistisen..author
-00000050: 5f65 6d61 696c 203d 2061 7367 6572 6a6f  _email = asgerjo
-00000060: 6e32 4067 6d61 696c 2e63 6f6d 0d0a 6465  n2@gmail.com..de
-00000070: 7363 7269 7074 696f 6e20 3d20 4120 436f  scription = A Co
-00000080: 6c6c 6563 7469 6f6e 206f 6620 5574 696c  llection of Util
-00000090: 6974 6965 730d 0a6c 6f6e 675f 6465 7363  ities..long_desc
-000000a0: 7269 7074 696f 6e20 3d20 6669 6c65 3a52  ription = file:R
-000000b0: 4541 444d 452e 6d64 2c4c 4943 454e 5345  EADME.md,LICENSE
-000000c0: 0d0a 6c6f 6e67 5f64 6573 6372 6970 7469  ..long_descripti
-000000d0: 6f6e 5f63 6f6e 7465 6e74 5f74 7970 6520  on_content_type 
-000000e0: 3d20 7465 7874 2f6d 6172 6b64 6f77 6e0d  = text/markdown.
-000000f0: 0a75 726c 203d 200d 0a70 726f 6a65 6374  .url = ..project
-00000100: 5f75 726c 7320 3d20 0d0a 636c 6173 7369  _urls = ..classi
-00000110: 6669 6572 7320 3d20 0d0a 0950 726f 6772  fiers = ...Progr
-00000120: 616d 6d69 6e67 204c 616e 6775 6167 653a  amming Language:
-00000130: 3a50 7974 686f 6e3a 3a33 0d0a 094c 4943  :Python::3...LIC
-00000140: 454e 5345 3a3a 0d0a 094f 7065 7261 7469  ENSE::...Operati
-00000150: 6e67 2053 7973 7465 6d3a 3a4f 5320 496e  ng System::OS In
-00000160: 6465 7065 6e64 656e 740d 0a6b 6579 776f  dependent..keywo
-00000170: 7264 7320 3d20 0d0a 0975 7469 6c69 7469  rds = ...utiliti
-00000180: 6573 0d0a 0963 6f6e 7665 6e69 656e 6365  es...convenience
-00000190: 0d0a 0941 7367 6572 204a 6f6e 2056 6973  ...Asger Jon Vis
-000001a0: 7469 7365 6e0d 0a0d 0a5b 4f50 5449 4f4e  tisen....[OPTION
-000001b0: 535d 0d0a 7061 636b 6167 655f 6469 7220  S]..package_dir 
-000001c0: 3d20 0d0a 093d 7372 630d 0a70 6163 6b61  = ...=src..packa
-000001d0: 6765 7320 3d20 6669 6e64 3a0d 0a70 7974  ges = find:..pyt
-000001e0: 686f 6e5f 7265 7175 6972 6573 203d 203e  hon_requires = >
-000001f0: 3d33 2e36 0d0a 0d0a 5b6f 7074 696f 6e73  =3.6....[options
-00000200: 2e70 6163 6b61 6765 732e 6669 6e64 5d0d  .packages.find].
-00000210: 0a77 6865 7265 203d 2073 7263 0d0a 0d0a  .where = src....
-00000220: 5b65 6767 5f69 6e66 6f5d 0d0a 7461 675f  [egg_info]..tag_
-00000230: 6275 696c 6420 3d20 0d0a 7461 675f 6461  build = ..tag_da
-00000240: 7465 203d 2030 0d0a 0d0a                 te = 0....
+00000020: 696f 6e20 3d20 302e 3235 0d0a 6175 7468  ion = 0.25..auth
+00000030: 6f72 203d 2041 7367 6572 204a 6f6e 2056  or = Asger Jon V
+00000040: 6973 7469 7365 6e0d 0a61 7574 686f 725f  istisen..author_
+00000050: 656d 6169 6c20 3d20 6173 6765 726a 6f6e  email = asgerjon
+00000060: 3240 676d 6169 6c2e 636f 6d0d 0a64 6573  2@gmail.com..des
+00000070: 6372 6970 7469 6f6e 203d 2041 2043 6f6c  cription = A Col
+00000080: 6c65 6374 696f 6e20 6f66 2055 7469 6c69  lection of Utili
+00000090: 7469 6573 0d0a 6c6f 6e67 5f64 6573 6372  ties..long_descr
+000000a0: 6970 7469 6f6e 203d 2066 696c 653a 5245  iption = file:RE
+000000b0: 4144 4d45 2e6d 642c 4c49 4345 4e53 450d  ADME.md,LICENSE.
+000000c0: 0a6c 6f6e 675f 6465 7363 7269 7074 696f  .long_descriptio
+000000d0: 6e5f 636f 6e74 656e 745f 7479 7065 203d  n_content_type =
+000000e0: 2074 6578 742f 6d61 726b 646f 776e 0d0a   text/markdown..
+000000f0: 7572 6c20 3d20 0d0a 7072 6f6a 6563 745f  url = ..project_
+00000100: 7572 6c73 203d 200d 0a63 6c61 7373 6966  urls = ..classif
+00000110: 6965 7273 203d 200d 0a09 5072 6f67 7261  iers = ...Progra
+00000120: 6d6d 696e 6720 4c61 6e67 7561 6765 3a3a  mming Language::
+00000130: 5079 7468 6f6e 3a3a 330d 0a09 4c49 4345  Python::3...LICE
+00000140: 4e53 453a 3a0d 0a09 4f70 6572 6174 696e  NSE::...Operatin
+00000150: 6720 5379 7374 656d 3a3a 4f53 2049 6e64  g System::OS Ind
+00000160: 6570 656e 6465 6e74 0d0a 6b65 7977 6f72  ependent..keywor
+00000170: 6473 203d 200d 0a09 7574 696c 6974 6965  ds = ...utilitie
+00000180: 730d 0a09 636f 6e76 656e 6965 6e63 650d  s...convenience.
+00000190: 0a09 4173 6765 7220 4a6f 6e20 5669 7374  ..Asger Jon Vist
+000001a0: 6973 656e 0d0a 0d0a 5b4f 5054 494f 4e53  isen....[OPTIONS
+000001b0: 5d0d 0a70 6163 6b61 6765 5f64 6972 203d  ]..package_dir =
+000001c0: 200d 0a09 3d73 7263 0d0a 7061 636b 6167   ...=src..packag
+000001d0: 6573 203d 2066 696e 643a 0d0a 7079 7468  es = find:..pyth
+000001e0: 6f6e 5f72 6571 7569 7265 7320 3d20 3e3d  on_requires = >=
+000001f0: 332e 380d 0a0d 0a5b 6f70 7469 6f6e 732e  3.8....[options.
+00000200: 7061 636b 6167 6573 2e66 696e 645d 0d0a  packages.find]..
+00000210: 7768 6572 6520 3d20 7372 630d 0a0d 0a5b  where = src....[
+00000220: 6567 675f 696e 666f 5d0d 0a74 6167 5f62  egg_info]..tag_b
+00000230: 7569 6c64 203d 200d 0a74 6167 5f64 6174  uild = ..tag_dat
+00000240: 6520 3d20 300d 0a0d 0a                   e = 0....
```

