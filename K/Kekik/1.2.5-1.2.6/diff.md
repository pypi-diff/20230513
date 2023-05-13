# Comparing `tmp/Kekik-1.2.5.tar.gz` & `tmp/Kekik-1.2.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Kekik-1.2.5.tar", last modified: Mon Apr 10 14:50:35 2023, max compression
+gzip compressed data, was "Kekik-1.2.6.tar", last modified: Sat May 13 11:09:43 2023, max compression
```

## Comparing `Kekik-1.2.5.tar` & `Kekik-1.2.6.tar`

### file list

```diff
@@ -1,40 +1,40 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 14:50:35.174618 Kekik-1.2.5/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 14:50:35.170618 Kekik-1.2.5/Kekik/
--rw-r--r--   0 runner    (1001) docker     (123)     1375 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/BIST.py
--rw-r--r--   0 runner    (1001) docker     (123)     7020 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/Nesne.py
--rw-r--r--   0 runner    (1001) docker     (123)      912 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3033 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      423 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/csv2dict.py
--rw-r--r--   0 runner    (1001) docker     (123)      560 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/dict2csv.py
--rw-r--r--   0 runner    (1001) docker     (123)     1935 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/dict2json.py
--rw-r--r--   0 runner    (1001) docker     (123)      357 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/dosya2set.py
--rw-r--r--   0 runner    (1001) docker     (123)     1554 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/dosya_indir.py
--rw-r--r--   0 runner    (1001) docker     (123)     1256 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/hwid_kontrol.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 14:50:35.174618 Kekik-1.2.5/Kekik/kisi_ver/
--rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/kisi_ver/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   189486 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/kisi_ver/biyografiler.py
--rw-r--r--   0 runner    (1001) docker     (123)    88066 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/kisi_ver/isimler.py
--rw-r--r--   0 runner    (1001) docker     (123)    78485 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/kisi_ver/soyisimler.py
--rw-r--r--   0 runner    (1001) docker     (123)      682 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/link_islemleri.py
--rw-r--r--   0 runner    (1001) docker     (123)     5635 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/list2html.py
--rw-r--r--   0 runner    (1001) docker     (123)      314 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/liste_fetis.py
--rw-r--r--   0 runner    (1001) docker     (123)     1209 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/mail_gonder.py
--rw-r--r--   0 runner    (1001) docker     (123)      597 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/okunabilir_byte.py
--rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/proxy_ver.py
--rw-r--r--   0 runner    (1001) docker     (123)      832 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/qr_ver.py
--rw-r--r--   0 runner    (1001) docker     (123)     3362 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/ses_fetis.py
--rw-r--r--   0 runner    (1001) docker     (123)      789 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/slugify.py
--rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/txt_fetis.py
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-04-10 14:50:15.000000 Kekik-1.2.5/Kekik/zaman_donustur.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-10 14:50:35.170618 Kekik-1.2.5/Kekik.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    10468 2023-04-10 14:50:35.000000 Kekik-1.2.5/Kekik.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      696 2023-04-10 14:50:35.000000 Kekik-1.2.5/Kekik.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-10 14:50:35.000000 Kekik-1.2.5/Kekik.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-04-10 14:50:35.000000 Kekik-1.2.5/Kekik.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-04-10 14:50:35.000000 Kekik-1.2.5/Kekik.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-04-10 14:50:15.000000 Kekik-1.2.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-04-10 14:50:15.000000 Kekik-1.2.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    10468 2023-04-10 14:50:35.174618 Kekik-1.2.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9880 2023-04-10 14:50:15.000000 Kekik-1.2.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-10 14:50:35.174618 Kekik-1.2.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-04-10 14:50:15.000000 Kekik-1.2.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:09:43.714169 Kekik-1.2.6/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:09:43.714169 Kekik-1.2.6/Kekik/
+-rw-r--r--   0 runner    (1001) docker     (123)     1375 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/BIST.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7020 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/Nesne.py
+-rw-r--r--   0 runner    (1001) docker     (123)      912 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3033 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      423 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/csv2dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)      560 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/dict2csv.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1935 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/dict2json.py
+-rw-r--r--   0 runner    (1001) docker     (123)      357 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/dosya2set.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1554 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/dosya_indir.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1256 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/hwid_kontrol.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:09:43.714169 Kekik-1.2.6/Kekik/kisi_ver/
+-rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/kisi_ver/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   189486 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/kisi_ver/biyografiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)    88066 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/kisi_ver/isimler.py
+-rw-r--r--   0 runner    (1001) docker     (123)    78485 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/kisi_ver/soyisimler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      682 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/link_islemleri.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7212 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/list2html.py
+-rw-r--r--   0 runner    (1001) docker     (123)      314 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/liste_fetis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1209 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/mail_gonder.py
+-rw-r--r--   0 runner    (1001) docker     (123)      597 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/okunabilir_byte.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/proxy_ver.py
+-rw-r--r--   0 runner    (1001) docker     (123)      832 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/qr_ver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3362 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/ses_fetis.py
+-rw-r--r--   0 runner    (1001) docker     (123)      789 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/slugify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/txt_fetis.py
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-13 11:09:25.000000 Kekik-1.2.6/Kekik/zaman_donustur.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 11:09:43.714169 Kekik-1.2.6/Kekik.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    10468 2023-05-13 11:09:43.000000 Kekik-1.2.6/Kekik.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      696 2023-05-13 11:09:43.000000 Kekik-1.2.6/Kekik.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 11:09:43.000000 Kekik-1.2.6/Kekik.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-05-13 11:09:43.000000 Kekik-1.2.6/Kekik.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-05-13 11:09:43.000000 Kekik-1.2.6/Kekik.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 11:09:25.000000 Kekik-1.2.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-13 11:09:25.000000 Kekik-1.2.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    10468 2023-05-13 11:09:43.714169 Kekik-1.2.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9880 2023-05-13 11:09:25.000000 Kekik-1.2.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 11:09:43.714169 Kekik-1.2.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-13 11:09:25.000000 Kekik-1.2.6/setup.py
```

### Comparing `Kekik-1.2.5/Kekik/BIST.py` & `Kekik-1.2.6/Kekik/BIST.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/Nesne.py` & `Kekik-1.2.6/Kekik/Nesne.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/__init__.py` & `Kekik-1.2.6/Kekik/__init__.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/cli.py` & `Kekik-1.2.6/Kekik/cli.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/dict2csv.py` & `Kekik-1.2.6/Kekik/dict2csv.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/dict2json.py` & `Kekik-1.2.6/Kekik/dict2json.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/dosya_indir.py` & `Kekik-1.2.6/Kekik/dosya_indir.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/hwid_kontrol.py` & `Kekik-1.2.6/Kekik/hwid_kontrol.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/kisi_ver/__init__.py` & `Kekik-1.2.6/Kekik/kisi_ver/__init__.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/kisi_ver/biyografiler.py` & `Kekik-1.2.6/Kekik/kisi_ver/biyografiler.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/kisi_ver/isimler.py` & `Kekik-1.2.6/Kekik/kisi_ver/isimler.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/kisi_ver/soyisimler.py` & `Kekik-1.2.6/Kekik/kisi_ver/soyisimler.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/link_islemleri.py` & `Kekik-1.2.6/Kekik/link_islemleri.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/mail_gonder.py` & `Kekik-1.2.6/Kekik/mail_gonder.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/okunabilir_byte.py` & `Kekik-1.2.6/Kekik/okunabilir_byte.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/proxy_ver.py` & `Kekik-1.2.6/Kekik/proxy_ver.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/qr_ver.py` & `Kekik-1.2.6/Kekik/qr_ver.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/ses_fetis.py` & `Kekik-1.2.6/Kekik/ses_fetis.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/slugify.py` & `Kekik-1.2.6/Kekik/slugify.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/txt_fetis.py` & `Kekik-1.2.6/Kekik/txt_fetis.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik/zaman_donustur.py` & `Kekik-1.2.6/Kekik/zaman_donustur.py`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/Kekik.egg-info/PKG-INFO` & `Kekik-1.2.6/Kekik.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Kekik
-Version: 1.2.5
+Version: 1.2.6
 Summary: İşlerimizi kolaylaştıracak fonksiyonların el altında durduğu kütüphane..
 Home-page: https://github.com/keyiflerolsun/Kekik
 Author: keyiflerolsun
 Author-email: keyiflerolsun@gmail.com
 License: GPLv3+
 Keywords: Kekik,KekikAkademi,keyiflerolsun
 Classifier: Development Status :: 5 - Production/Stable
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: Kekik Version: 1.2.5 Summary: Ä°Ålerimizi
+Metadata-Version: 2.1 Name: Kekik Version: 1.2.6 Summary: Ä°Ålerimizi
 kolaylaÅtÄ±racak fonksiyonlarÄ±n el altÄ±nda durduÄu kÃ¼tÃ¼phane.. Home-page:
 https://github.com/keyiflerolsun/Kekik Author: keyiflerolsun Author-email:
 keyiflerolsun@gmail.com License: GPLv3+ Keywords:
 Kekik,KekikAkademi,keyiflerolsun Classifier: Development Status :: 5 -
 Production/Stable Classifier: License :: OSI Approved :: GNU General Public
 License v3 or later (GPLv3+) Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.10 Description-Content-Type: text/markdown License-File:
```

### Comparing `Kekik-1.2.5/Kekik.egg-info/SOURCES.txt` & `Kekik-1.2.6/Kekik.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/LICENSE` & `Kekik-1.2.6/LICENSE`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/PKG-INFO` & `Kekik-1.2.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Kekik
-Version: 1.2.5
+Version: 1.2.6
 Summary: İşlerimizi kolaylaştıracak fonksiyonların el altında durduğu kütüphane..
 Home-page: https://github.com/keyiflerolsun/Kekik
 Author: keyiflerolsun
 Author-email: keyiflerolsun@gmail.com
 License: GPLv3+
 Keywords: Kekik,KekikAkademi,keyiflerolsun
 Classifier: Development Status :: 5 - Production/Stable
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: Kekik Version: 1.2.5 Summary: Ä°Ålerimizi
+Metadata-Version: 2.1 Name: Kekik Version: 1.2.6 Summary: Ä°Ålerimizi
 kolaylaÅtÄ±racak fonksiyonlarÄ±n el altÄ±nda durduÄu kÃ¼tÃ¼phane.. Home-page:
 https://github.com/keyiflerolsun/Kekik Author: keyiflerolsun Author-email:
 keyiflerolsun@gmail.com License: GPLv3+ Keywords:
 Kekik,KekikAkademi,keyiflerolsun Classifier: Development Status :: 5 -
 Production/Stable Classifier: License :: OSI Approved :: GNU General Public
 License v3 or later (GPLv3+) Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.10 Description-Content-Type: text/markdown License-File:
```

### Comparing `Kekik-1.2.5/README.md` & `Kekik-1.2.6/README.md`

 * *Files identical despite different names*

### Comparing `Kekik-1.2.5/setup.py` & `Kekik-1.2.6/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 setup(
     author       = "keyiflerolsun",
     author_email = "keyiflerolsun@gmail.com",
 
     packages     = ["Kekik"],
 
     name         = "Kekik",
-    version      = "1.2.5",
+    version      = "1.2.6",
     url          = "https://github.com/keyiflerolsun/Kekik",
     description  = "İşlerimizi kolaylaştıracak fonksiyonların el altında durduğu kütüphane..",
     keywords     = ["Kekik", "KekikAkademi", "keyiflerolsun"],
 
     long_description_content_type = "text/markdown",
     long_description              = "".join(open("README.md", encoding="utf-8").readlines()),
     include_package_data          = True,
@@ -29,14 +29,17 @@
     python_requires  = ">=3.10",
     install_requires = [
         "setuptools",
         "wheel",
         "pytz",
         "requests",
         "aiohttp",
+        "httpx",
+        "parsel",
+        "cssselect",
         # "thispersondoesnotexist",
         "simplejson",
         "rich",
         "tabulate",
         "tqdm",
         "qrcode",
         "pyfiglet",
```

