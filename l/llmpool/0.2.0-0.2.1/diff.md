# Comparing `tmp/llmpool-0.2.0-py3-none-any.whl.zip` & `tmp/llmpool-0.2.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,12 +1,12 @@
-Zip file size: 9627 bytes, number of entries: 10
--rw-rw-rw-  2.0 unx      157 b- defN 23-May-09 04:51 llmpool/__init__.py
--rw-rw-rw-  2.0 unx     4114 b- defN 23-May-09 04:48 llmpool/local_model.py
--rw-rw-rw-  2.0 unx      668 b- defN 23-May-09 04:50 llmpool/model.py
--rw-rw-rw-  2.0 unx     2817 b- defN 23-May-09 04:50 llmpool/model_pool.py
--rw-rw-rw-  2.0 unx     2312 b- defN 23-May-09 04:48 llmpool/remote_model.py
--rw-rw-rw-  2.0 unx    11357 b- defN 23-May-09 04:51 llmpool-0.2.0.dist-info/LICENSE
--rw-rw-rw-  2.0 unx     2409 b- defN 23-May-09 04:51 llmpool-0.2.0.dist-info/METADATA
--rw-rw-rw-  2.0 unx       92 b- defN 23-May-09 04:51 llmpool-0.2.0.dist-info/WHEEL
--rw-rw-rw-  2.0 unx        8 b- defN 23-May-09 04:51 llmpool-0.2.0.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      770 b- defN 23-May-09 04:51 llmpool-0.2.0.dist-info/RECORD
-10 files, 24704 bytes uncompressed, 8325 bytes compressed:  66.3%
+Zip file size: 9647 bytes, number of entries: 10
+-rw-r--r--  2.0 unx      157 b- defN 23-May-13 14:12 llmpool/__init__.py
+-rw-r--r--  2.0 unx     4202 b- defN 23-May-13 14:11 llmpool/local_model.py
+-rw-r--r--  2.0 unx      668 b- defN 23-May-13 14:10 llmpool/model.py
+-rw-r--r--  2.0 unx     2817 b- defN 23-May-13 14:10 llmpool/model_pool.py
+-rw-r--r--  2.0 unx     2312 b- defN 23-May-13 14:10 llmpool/remote_model.py
+-rw-r--r--  2.0 unx    11357 b- defN 23-May-13 14:12 llmpool-0.2.1.dist-info/LICENSE
+-rw-r--r--  2.0 unx     2409 b- defN 23-May-13 14:12 llmpool-0.2.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-May-13 14:12 llmpool-0.2.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx        8 b- defN 23-May-13 14:12 llmpool-0.2.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      770 b- defN 23-May-13 14:12 llmpool-0.2.1.dist-info/RECORD
+10 files, 24792 bytes uncompressed, 8345 bytes compressed:  66.3%
```

## zipnote {}

```diff
@@ -9,23 +9,23 @@
 
 Filename: llmpool/model_pool.py
 Comment: 
 
 Filename: llmpool/remote_model.py
 Comment: 
 
-Filename: llmpool-0.2.0.dist-info/LICENSE
+Filename: llmpool-0.2.1.dist-info/LICENSE
 Comment: 
 
-Filename: llmpool-0.2.0.dist-info/METADATA
+Filename: llmpool-0.2.1.dist-info/METADATA
 Comment: 
 
-Filename: llmpool-0.2.0.dist-info/WHEEL
+Filename: llmpool-0.2.1.dist-info/WHEEL
 Comment: 
 
-Filename: llmpool-0.2.0.dist-info/top_level.txt
+Filename: llmpool-0.2.1.dist-info/top_level.txt
 Comment: 
 
-Filename: llmpool-0.2.0.dist-info/RECORD
+Filename: llmpool-0.2.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## llmpool/__init__.py

```diff
@@ -1,5 +1,5 @@
-__version__ = '0.2.0'
+__version__ = '0.2.1'
 
 from .local_model import LocalLLModel, LocalLoRALLModel
 from .model_pool import LLModelPool
 from .remote_model import TxtGenIfLLModel
```

## llmpool/local_model.py

```diff
@@ -8,17 +8,18 @@
 
 from llmpool.model import LLModel
 
 class LocalLLModel(LLModel):
     def __init__(
         self, name, gen_config, base, device='cuda',
         model_cls=AutoModel, tokenizer_cls=AutoTokenizer,
-        load_in_8bit=True, apply_bettertransformer=False
+        load_in_8bit=True, apply_bettertransformer=False,
+        metadata=None,
     ):
-        super().__init__(name, gen_config)
+        super().__init__(name, gen_config, metadata)
 
         self.device = device
         self.tokenizer = tokenizer_cls.from_pretrained(base)
         self.model = model_cls.from_pretrained(
             base,
             load_in_8bit=load_in_8bit,
             device_map="auto",
@@ -102,18 +103,21 @@
             )
             return decoded              
 
 class LocalLoRALLModel(LocalLLModel):
     def __init__(
         self, name, gen_config, base, lora, device='cuda',
         model_cls=AutoModel, tokenizer_cls=AutoTokenizer,
-        load_in_8bit=True, apply_bettertransformer=False
+        load_in_8bit=True, apply_bettertransformer=False,
+        metadata=None
     ):
         super().__init__(
             name, gen_config, base, 
             device, model_cls, tokenizer_cls,
-            load_in_8bit, apply_bettertransformer)
+            load_in_8bit, apply_bettertransformer,
+            metadata
+        )
 
         self.model = PeftModel.from_pretrained(
             self.model, lora, 
             device_map={'': 0}
         )
```

## Comparing `llmpool-0.2.0.dist-info/LICENSE` & `llmpool-0.2.1.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `llmpool-0.2.0.dist-info/METADATA` & `llmpool-0.2.1.dist-info/METADATA`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: llmpool
-Version: 0.2.0
+Version: 0.2.1
 Summary: Large Language Models' pool management library
 Home-page: https://github.com/deep-diver/LLM-Pool
 Author: chansung park
 Author-email: deep.diver.csp@gmail.com
 Keywords: LLM,instance pool,management
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3.8
```

## Comparing `llmpool-0.2.0.dist-info/RECORD` & `llmpool-0.2.1.dist-info/RECORD`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-llmpool/__init__.py,sha256=euji_hfMqXlEFcvF-2D3xvK1b9YO6T5RI8hDCTlUDME,157
-llmpool/local_model.py,sha256=WA5xK0vJPVP0rathgkah3OpcY3tJLIvAsMFAk9ENP1U,4114
+llmpool/__init__.py,sha256=5vUs-CGMOcTfpIwrt4HY1UuuYWnsKB7bHaAMl0tqA2g,157
+llmpool/local_model.py,sha256=xHxcG0L91T0xliZqsBHwTiPqXY2LXgQRemPejm2NFmU,4202
 llmpool/model.py,sha256=iZPRIwUAd76bH__pDTcx9ef1-DY55F6etOROb44F1qk,668
 llmpool/model_pool.py,sha256=v5cwRDHSldPS_uO_9fS9nhZypNuTmfjXhqCL_KSRfmQ,2817
 llmpool/remote_model.py,sha256=Rw5tapaqbJ1V3Y9BrkA8z60yk_SvfSVN-PDPnsBN5SY,2312
-llmpool-0.2.0.dist-info/LICENSE,sha256=xx0jnfkXJvxRnG63LTGOxlggYnIysveWIZ6H3PNdCrQ,11357
-llmpool-0.2.0.dist-info/METADATA,sha256=pF1tKVmjxNDGcQPqoP_7OT883ZMwXWhppX-RxacOoW4,2409
-llmpool-0.2.0.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-llmpool-0.2.0.dist-info/top_level.txt,sha256=1kKiMvue6u12IMQD92YMn4xdcQPDejrD0VuDl-pOCjE,8
-llmpool-0.2.0.dist-info/RECORD,,
+llmpool-0.2.1.dist-info/LICENSE,sha256=xx0jnfkXJvxRnG63LTGOxlggYnIysveWIZ6H3PNdCrQ,11357
+llmpool-0.2.1.dist-info/METADATA,sha256=EImBNuepk1qRZfHEaqQQdsY6xTCowG_ssewL3Km__aE,2409
+llmpool-0.2.1.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+llmpool-0.2.1.dist-info/top_level.txt,sha256=1kKiMvue6u12IMQD92YMn4xdcQPDejrD0VuDl-pOCjE,8
+llmpool-0.2.1.dist-info/RECORD,,
```

