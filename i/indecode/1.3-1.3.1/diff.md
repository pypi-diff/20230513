# Comparing `tmp/indecode-1.3-py3-none-any.whl.zip` & `tmp/indecode-1.3.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,7 +1,7 @@
-Zip file size: 2228 bytes, number of entries: 5
--rw-r--r--  2.0 unx     2902 b- defN 23-May-13 13:13 indecode.py
--rw-r--r--  2.0 unx     1023 b- defN 23-May-13 13:17 indecode-1.3.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-May-13 13:17 indecode-1.3.dist-info/WHEEL
--rw-r--r--  2.0 unx        9 b- defN 23-May-13 13:17 indecode-1.3.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      361 b- defN 23-May-13 13:17 indecode-1.3.dist-info/RECORD
-5 files, 4387 bytes uncompressed, 1556 bytes compressed:  64.5%
+Zip file size: 2263 bytes, number of entries: 5
+-rw-r--r--  2.0 unx     2912 b- defN 23-May-13 17:34 indecode.py
+-rw-r--r--  2.0 unx     1025 b- defN 23-May-13 17:35 indecode-1.3.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-May-13 17:35 indecode-1.3.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx        9 b- defN 23-May-13 17:35 indecode-1.3.1.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      369 b- defN 23-May-13 17:35 indecode-1.3.1.dist-info/RECORD
+5 files, 4407 bytes uncompressed, 1575 bytes compressed:  64.3%
```

## zipnote {}

```diff
@@ -1,16 +1,16 @@
 Filename: indecode.py
 Comment: 
 
-Filename: indecode-1.3.dist-info/METADATA
+Filename: indecode-1.3.1.dist-info/METADATA
 Comment: 
 
-Filename: indecode-1.3.dist-info/WHEEL
+Filename: indecode-1.3.1.dist-info/WHEEL
 Comment: 
 
-Filename: indecode-1.3.dist-info/top_level.txt
+Filename: indecode-1.3.1.dist-info/top_level.txt
 Comment: 
 
-Filename: indecode-1.3.dist-info/RECORD
+Filename: indecode-1.3.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## indecode.py

```diff
@@ -1,10 +1,10 @@
 import random
-__version__="1.3"
-text="hello"
+__version__="1.3.1"
+text="hello world"
 carac=["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z","A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z","0","1","2","3","4","5","6","7","8","9","&","é","~",'"',"#","{","}","(",")","[","]","-","è","_","\\","ç","^","à","@","°","+","=","ê","ë","$","£","%","ù","µ","*",",","?",".",";",":","/","!","§"]
 class CodeError(Exception):
     pass
 class DecodeError(Exception):
     pass
 class KeyElementError(Exception):
     pass
@@ -30,15 +30,15 @@
     for i in range(len(keylist)):
         if not keylist[i] in carac:
             raise KeyElementError("'"+keylist[i]+"' must not be in the key.")
     for i in range(len(key)):
         incode.update({carac[i]:key[i]})
     incode.update({" ":" "})
     for i in range(len(text)):
-        if not text[i] in carac:
+        if not text[i] in incode:
             raise CodeError("'"+text[i]+"' is not encodable.")
         newtext=newtext+incode[text[i]]
     return newtext
 def decode(text,key):
     newtext=""
     uncode={}
     if not type(text)==str:
@@ -51,15 +51,15 @@
     for i in range(len(keylist)):
         if not keylist[i] in carac:
             raise KeyElementError("'"+keylist[i]+"' must not be in the key.")
     for i in range(len(key)):
         uncode.update({key[i]:carac[i]})
     uncode.update({" ":" "})
     for i in range(len(text)):
-        if not text[i] in carac:
+        if not text[i] in uncode:
             raise DecodeError("'"+text[i]+"' is not decodable.")
         newtext=newtext+uncode[text[i]]
     return newtext
 if __name__=="__main__":
     keya=generate_key()
     print(keya)
     icode=code(text,keya)
```

## Comparing `indecode-1.3.dist-info/METADATA` & `indecode-1.3.1.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: indecode
-Version: 1.3
+Version: 1.3.1
 Summary: Code and decode string
 Author: lolo859
 License: UNKNOWN
 Keywords: code,incode,indecode,decode,incode,indc
 Platform: UNKNOWN
 Classifier: Natural Language :: French
 Classifier: Topic :: Security :: Cryptography
```

