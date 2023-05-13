# Comparing `tmp/indecode-1.2.1-py3-none-any.whl.zip` & `tmp/indecode-1.3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,7 +1,7 @@
-Zip file size: 1893 bytes, number of entries: 5
--rw-r--r--  2.0 unx     1666 b- defN 23-Mar-17 14:14 indecode.py
--rw-r--r--  2.0 unx      623 b- defN 23-Mar-17 14:14 indecode-1.2.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Mar-17 14:14 indecode-1.2.1.dist-info/WHEEL
--rw-r--r--  2.0 unx        9 b- defN 23-Mar-17 14:14 indecode-1.2.1.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      368 b- defN 23-Mar-17 14:14 indecode-1.2.1.dist-info/RECORD
-5 files, 2758 bytes uncompressed, 1205 bytes compressed:  56.3%
+Zip file size: 2228 bytes, number of entries: 5
+-rw-r--r--  2.0 unx     2902 b- defN 23-May-13 13:13 indecode.py
+-rw-r--r--  2.0 unx     1023 b- defN 23-May-13 13:17 indecode-1.3.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-May-13 13:17 indecode-1.3.dist-info/WHEEL
+-rw-r--r--  2.0 unx        9 b- defN 23-May-13 13:17 indecode-1.3.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      361 b- defN 23-May-13 13:17 indecode-1.3.dist-info/RECORD
+5 files, 4387 bytes uncompressed, 1556 bytes compressed:  64.5%
```

## zipnote {}

```diff
@@ -1,16 +1,16 @@
 Filename: indecode.py
 Comment: 
 
-Filename: indecode-1.2.1.dist-info/METADATA
+Filename: indecode-1.3.dist-info/METADATA
 Comment: 
 
-Filename: indecode-1.2.1.dist-info/WHEEL
+Filename: indecode-1.3.dist-info/WHEEL
 Comment: 
 
-Filename: indecode-1.2.1.dist-info/top_level.txt
+Filename: indecode-1.3.dist-info/top_level.txt
 Comment: 
 
-Filename: indecode-1.2.1.dist-info/RECORD
+Filename: indecode-1.3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## indecode.py

```diff
@@ -1,36 +1,67 @@
 import random
-__version__="1.2.1"
+__version__="1.3"
 text="hello"
 carac=["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z","A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z","0","1","2","3","4","5","6","7","8","9","&","é","~",'"',"#","{","}","(",")","[","]","-","è","_","\\","ç","^","à","@","°","+","=","ê","ë","$","£","%","ù","µ","*",",","?",".",";",":","/","!","§"]
+class CodeError(Exception):
+    pass
+class DecodeError(Exception):
+    pass
+class KeyElementError(Exception):
+    pass
+class KeyLengthError(Exception):
+    pass
 def generate_key():
     carac=["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z","A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z","0","1","2","3","4","5","6","7","8","9","&","é","~",'"',"#","{","}","(",")","[","]","-","è","_","\\","ç","^","à","@","°","+","=","ê","ë","$","£","%","ù","µ","*",",","?",".",";",":","/","!","§"]
     random.shuffle(carac)
     key=""
     for i in range(len(carac)):
         key=key+carac[i]
     return key
 def code(text,key):
     newtext=""
     incode={}
-    liste=[]
+    if not type(text)==str:
+        raise TypeError("text argument must be a string")
+    if not type(key)==str:
+        raise TypeError("key argument must be a string")
+    keylist=list(key)
+    if not len(keylist)==len(carac):
+        raise KeyLengthError("the key is not of the expected length.")
+    for i in range(len(keylist)):
+        if not keylist[i] in carac:
+            raise KeyElementError("'"+keylist[i]+"' must not be in the key.")
     for i in range(len(key)):
         incode.update({carac[i]:key[i]})
     incode.update({" ":" "})
     for i in range(len(text)):
+        if not text[i] in carac:
+            raise CodeError("'"+text[i]+"' is not encodable.")
         newtext=newtext+incode[text[i]]
     return newtext
-def decode(test,key):
+def decode(text,key):
     newtext=""
     uncode={}
+    if not type(text)==str:
+        raise TypeError("text argument must be a string")
+    if not type(key)==str:
+        raise TypeError("key argument must be a string")
+    keylist=list(key)
+    if not len(keylist)==len(carac):
+        raise KeyLengthError("the key is not of the expected length.")
+    for i in range(len(keylist)):
+        if not keylist[i] in carac:
+            raise KeyElementError("'"+keylist[i]+"' must not be in the key.")
     for i in range(len(key)):
         uncode.update({key[i]:carac[i]})
     uncode.update({" ":" "})
-    for i in range(len(test)):
-        newtext=newtext+uncode[test[i]]
+    for i in range(len(text)):
+        if not text[i] in carac:
+            raise DecodeError("'"+text[i]+"' is not decodable.")
+        newtext=newtext+uncode[text[i]]
     return newtext
 if __name__=="__main__":
     keya=generate_key()
     print(keya)
     icode=code(text,keya)
     print(icode)
     decod=decode(icode,keya)
```

