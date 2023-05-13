# Comparing `tmp/hf_hub_ctranslate2-1.0.2.tar.gz` & `tmp/hf_hub_ctranslate2-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hf_hub_ctranslate2-1.0.2.tar", last modified: Mon May  1 23:57:00 2023, max compression
+gzip compressed data, was "hf_hub_ctranslate2-1.0.3.tar", last modified: Sat May 13 21:12:44 2023, max compression
```

## Comparing `hf_hub_ctranslate2-1.0.2.tar` & `hf_hub_ctranslate2-1.0.3.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 23:57:00.014430 hf_hub_ctranslate2-1.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-01 23:57:00.014430 hf_hub_ctranslate2-1.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3226 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 23:57:00.014430 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-01 23:57:00.000000 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      296 2023-05-01 23:57:00.000000 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-01 23:57:00.000000 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       75 2023-05-01 23:57:00.000000 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-01 23:57:00.000000 hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-01 23:57:00.014430 hf_hub_ctranslate2-1.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-01 23:57:00.014430 hf_hub_ctranslate2-1.0.2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1692 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/tests/test_translate.py
--rw-r--r--   0 runner    (1001) docker     (123)      149 2023-05-01 23:56:50.000000 hf_hub_ctranslate2-1.0.2/tests/test_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:44.740648 hf_hub_ctranslate2-1.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-13 21:12:44.740648 hf_hub_ctranslate2-1.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3226 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:44.740648 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3744 2023-05-13 21:12:44.000000 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      296 2023-05-13 21:12:44.000000 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:12:44.000000 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       75 2023-05-13 21:12:44.000000 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:12:44.000000 hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 21:12:44.740648 hf_hub_ctranslate2-1.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:12:44.740648 hf_hub_ctranslate2-1.0.3/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2403 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/tests/test_translate.py
+-rw-r--r--   0 runner    (1001) docker     (123)      149 2023-05-13 21:12:30.000000 hf_hub_ctranslate2-1.0.3/tests/test_version.py
```

### Comparing `hf_hub_ctranslate2-1.0.2/LICENSE` & `hf_hub_ctranslate2-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `hf_hub_ctranslate2-1.0.2/PKG-INFO` & `hf_hub_ctranslate2-1.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hf_hub_ctranslate2
-Version: 1.0.2
+Version: 1.0.3
 Summary: Connecting Transfromers on HuggingfaceHub with Ctranslate2 
 Home-page: https://github.com/michaelfeil/hf-hub-ctranslate2
 Author: Michael Feil
 License: MIT
 Project-URL: Bug Tracker, https://github.com/michaelfeil/hf-hub-ctranslate2/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `hf_hub_ctranslate2-1.0.2/README.md` & `hf_hub_ctranslate2-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `hf_hub_ctranslate2-1.0.2/hf_hub_ctranslate2.egg-info/PKG-INFO` & `hf_hub_ctranslate2-1.0.3/hf_hub_ctranslate2.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hf-hub-ctranslate2
-Version: 1.0.2
+Version: 1.0.3
 Summary: Connecting Transfromers on HuggingfaceHub with Ctranslate2 
 Home-page: https://github.com/michaelfeil/hf-hub-ctranslate2
 Author: Michael Feil
 License: MIT
 Project-URL: Bug Tracker, https://github.com/michaelfeil/hf-hub-ctranslate2/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `hf_hub_ctranslate2-1.0.2/setup.py` & `hf_hub_ctranslate2-1.0.3/setup.py`

 * *Files identical despite different names*

### Comparing `hf_hub_ctranslate2-1.0.2/tests/test_translate.py` & `hf_hub_ctranslate2-1.0.3/tests/test_translate.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from hf_hub_ctranslate2 import TranslatorCT2fromHfHub, GeneratorCT2fromHfHub
+from hf_hub_ctranslate2 import TranslatorCT2fromHfHub, GeneratorCT2fromHfHub, MultiLingualTranslatorCT2fromHfHub
 from hf_hub_ctranslate2._private.utils import download_model
 from transformers import AutoTokenizer
 
 
 def test_translator(model_name="michaelfeil/ct2fast-flan-alpaca-base"):
     model = TranslatorCT2fromHfHub(
         model_name_or_path=model_name, device="cpu", compute_type="int8"
@@ -13,14 +13,31 @@
     )
     assert len(outputs) == 2
     assert len(outputs[0]) != len(outputs[1])
     assert "flan" in outputs[0].lower()
     for o in outputs:
         assert isinstance(o, str)
 
+def test_multilingualtranslator(model_name="michaelfeil/ct2fast-m2m100_418M"):
+    model = MultiLingualTranslatorCT2fromHfHub(
+        model_name_or_path=model_name, device="cpu", compute_type="int8",
+        tokenizer=AutoTokenizer.from_pretrained(f"facebook/{model_name.split('-')[-1]}")
+    )
+
+    outputs = model.generate(
+        ["How do you call a fast Flamingo?", "Wie geht es dir?"],
+        src_lang=["en", "de"],
+        tgt_lang=["de", "fr"]
+    )
+    assert len(outputs) == 2
+    assert len(outputs[0]) != len(outputs[1])
+    assert "nennt" in outputs[0].lower()
+    assert "comment" in outputs[1].lower()
+    for o in outputs:
+        assert isinstance(o, str)
 
 def test_generator(model_name="michaelfeil/ct2fast-pythia-160m"):
     model = GeneratorCT2fromHfHub(
         model_name_or_path=model_name, device="cpu", compute_type="int8"
     )
 
     outputs = model.generate(
```

