# Comparing `tmp/bisque_metadoc-0.6.3.24-py3-none-any.whl.zip` & `tmp/bisque_metadoc-0.6.3.25-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,13 +1,13 @@
-Zip file size: 10694 bytes, number of entries: 11
--rw-r--r--  2.0 unx      167 b- defN 23-Apr-07 23:04 bq/__init__.py
--rw-r--r--  2.0 unx       73 b- defN 23-Apr-07 23:04 bq/metadoc/__init__.py
--rw-r--r--  2.0 unx     2467 b- defN 23-Apr-07 23:04 bq/metadoc/etree.py
--rw-r--r--  2.0 unx    24152 b- defN 23-Apr-07 23:04 bq/metadoc/formats.py
--rw-r--r--  2.0 unx     1010 b- defN 23-Apr-07 23:04 bq/metadoc/logging.py
--rw-r--r--  2.0 unx      167 b- defN 23-Apr-07 23:04 bq/metadoc/version.py
--rw-r--r--  2.0 unx     4486 b- defN 23-Apr-07 23:04 bq/metadoc/xmldict.py
--rw-r--r--  2.0 unx      457 b- defN 23-Apr-07 23:04 bisque_metadoc-0.6.3.24.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Apr-07 23:04 bisque_metadoc-0.6.3.24.dist-info/WHEEL
--rw-r--r--  2.0 unx        3 b- defN 23-Apr-07 23:04 bisque_metadoc-0.6.3.24.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      871 b- defN 23-Apr-07 23:04 bisque_metadoc-0.6.3.24.dist-info/RECORD
-11 files, 33945 bytes uncompressed, 9222 bytes compressed:  72.8%
+Zip file size: 10812 bytes, number of entries: 11
+-rw-r--r--  2.0 unx      167 b- defN 23-May-13 03:06 bq/__init__.py
+-rw-r--r--  2.0 unx       73 b- defN 23-May-13 03:06 bq/metadoc/__init__.py
+-rw-r--r--  2.0 unx     2467 b- defN 23-May-13 03:06 bq/metadoc/etree.py
+-rw-r--r--  2.0 unx    24260 b- defN 23-May-13 03:06 bq/metadoc/formats.py
+-rw-r--r--  2.0 unx     1020 b- defN 23-May-13 03:06 bq/metadoc/logging.py
+-rw-r--r--  2.0 unx      167 b- defN 23-May-13 03:06 bq/metadoc/version.py
+-rw-r--r--  2.0 unx     4486 b- defN 23-May-13 03:06 bq/metadoc/xmldict.py
+-rw-r--r--  2.0 unx      641 b- defN 23-May-13 03:06 bisque_metadoc-0.6.3.25.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-May-13 03:06 bisque_metadoc-0.6.3.25.dist-info/WHEEL
+-rw-r--r--  2.0 unx        3 b- defN 23-May-13 03:06 bisque_metadoc-0.6.3.25.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      871 b- defN 23-May-13 03:06 bisque_metadoc-0.6.3.25.dist-info/RECORD
+11 files, 34247 bytes uncompressed, 9340 bytes compressed:  72.7%
```

## zipnote {}

```diff
@@ -15,20 +15,20 @@
 
 Filename: bq/metadoc/version.py
 Comment: 
 
 Filename: bq/metadoc/xmldict.py
 Comment: 
 
-Filename: bisque_metadoc-0.6.3.24.dist-info/METADATA
+Filename: bisque_metadoc-0.6.3.25.dist-info/METADATA
 Comment: 
 
-Filename: bisque_metadoc-0.6.3.24.dist-info/WHEEL
+Filename: bisque_metadoc-0.6.3.25.dist-info/WHEEL
 Comment: 
 
-Filename: bisque_metadoc-0.6.3.24.dist-info/top_level.txt
+Filename: bisque_metadoc-0.6.3.25.dist-info/top_level.txt
 Comment: 
 
-Filename: bisque_metadoc-0.6.3.24.dist-info/RECORD
+Filename: bisque_metadoc-0.6.3.25.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## bq/metadoc/formats.py

```diff
@@ -465,18 +465,18 @@
                     res = etree.SubElement(parent, "tag", name=tag, **attrs)
         if val is not None:
             res.text = str(val)  # TODO: allow different value types
         self.node = res
 
     def __getstate__(self):
         return self.serialize()
+
     def __setstate__(self, s):
         self.node = self.deserialize(s).node
 
-
     @staticmethod
     def convert(internal):
         if isinstance(internal, Metadoc):
             return internal
         if isinstance(internal, etree._Element):
             return Metadoc(et=internal)
         elif isinstance(internal, etree._ElementTree):
@@ -680,14 +680,18 @@
         # escape any empty strings (XML is not round-tripable for empty strings in text nodes!)
         return _tostring_fix_empty(self.node, encoding="unicode")
 
     def __str__(self):
         return self.serialize()
         # TODO: better return as JSON
 
+    def __repr__(self):
+        return f"metadoc:{self.serialize()}"
+        # TODO: better return as JSON
+
     def _path_to_xpath(self, path):
         path = path.strip()
         if re.match(
             r"^[\w]", path
         ):  # TODO: right now every tag has to start with '/' otherwise the regex below won't work
             path = "./" + path
         res = ""
```

## bq/metadoc/logging.py

```diff
@@ -24,15 +24,15 @@
 
 def get_ip():
     s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
     try:
         # doesn't even have to be reachable
         s.connect(("10.255.255.255", 1))
         IP = s.getsockname()[0]
-    except:
+    except Exception:
         IP = "127.0.0.1"
     finally:
         s.close()
     return IP
 
 
 class BQContextFilter(logging.Filter):
```

## bq/metadoc/version.py

```diff
@@ -1,4 +1,4 @@
 # file generated by setuptools_scm
 # don't change, don't track in version control
-__version__ = version = '0.6.3.24'
-__version_tuple__ = version_tuple = (0, 6, 3, 24)
+__version__ = version = '0.6.3.25'
+__version_tuple__ = version_tuple = (0, 6, 3, 25)
```

## Comparing `bisque_metadoc-0.6.3.24.dist-info/RECORD` & `bisque_metadoc-0.6.3.25.dist-info/RECORD`

 * *Files 14% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 bq/__init__.py,sha256=xiybI6MFP1EFRXvSb-33FlFs5jN4FImlrmD2D0jWs6g,167
 bq/metadoc/__init__.py,sha256=l9gw3A8XoRuAewpCkNfBA0nFUNnu0PDuTpmhh8w85uk,73
 bq/metadoc/etree.py,sha256=tM0QCHhRryUMl3U6Wb7SNK2niAIANBSiu34x40K3Qwg,2467
-bq/metadoc/formats.py,sha256=iFs0-sf6z-n7dpsON8ww-sqEXbGutSqAaCp8f_gRe9k,24152
-bq/metadoc/logging.py,sha256=HJZeAPGBttoEz7OcZl_brbherhAVeltUfzjcbfzF-xU,1010
-bq/metadoc/version.py,sha256=ycvmaDCAx1y2-1nLVRihQSNeFw8X_-e_hnah7nynhUY,167
+bq/metadoc/formats.py,sha256=6JhLM7pEpRShuzEebdtgYdhd5gUI_nQuRI2U2pWGmmQ,24260
+bq/metadoc/logging.py,sha256=vYuf2-OuZFvIw-lAj1R_BWpRbud92vqUxiIFEMF8eOo,1020
+bq/metadoc/version.py,sha256=cDUEOZd7CB8S3t5FZGlyi2sTQBrw3zUsI_MGkkFbgWo,167
 bq/metadoc/xmldict.py,sha256=ZIk0_XMMfBSe2JDsQhjXBSx4R70qLj-bfjN5Ebufh4c,4486
-bisque_metadoc-0.6.3.24.dist-info/METADATA,sha256=_e96mBE124eqf_4ddk8Bukr94Zu0tytNtcRfiv3IiYE,457
-bisque_metadoc-0.6.3.24.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-bisque_metadoc-0.6.3.24.dist-info/top_level.txt,sha256=w5z7Un4-v3yqVMurNio-Srl-AUvtPOxZ3tZh4Eb8RHo,3
-bisque_metadoc-0.6.3.24.dist-info/RECORD,,
+bisque_metadoc-0.6.3.25.dist-info/METADATA,sha256=0caiMiDj3DW2sIFpWCcsqdKZKLmhAbuQMEOQbfTpAh8,641
+bisque_metadoc-0.6.3.25.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+bisque_metadoc-0.6.3.25.dist-info/top_level.txt,sha256=w5z7Un4-v3yqVMurNio-Srl-AUvtPOxZ3tZh4Eb8RHo,3
+bisque_metadoc-0.6.3.25.dist-info/RECORD,,
```

