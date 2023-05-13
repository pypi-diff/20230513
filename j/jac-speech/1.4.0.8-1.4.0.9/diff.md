# Comparing `tmp/jac_speech-1.4.0.8.tar.gz` & `tmp/jac_speech-1.4.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jac_speech-1.4.0.8.tar", last modified: Wed Feb  8 14:13:32 2023, max compression
+gzip compressed data, was "jac_speech-1.4.0.9.tar", last modified: Tue Feb 14 17:26:45 2023, max compression
```

## Comparing `jac_speech-1.4.0.8.tar` & `jac_speech-1.4.0.9.tar`

### file list

```diff
@@ -1,57 +1,29 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.141526 jac_speech-1.4.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)      238 2023-02-08 14:13:32.141526 jac_speech-1.4.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.129526 jac_speech-1.4.0.8/jac_speech/
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      316 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.133526 jac_speech-1.4.0.8/jac_speech/stt/
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/stt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       82 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/stt/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5815 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/stt/stt.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.133526 jac_speech-1.4.0.8/jac_speech/tts/
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9025 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/action_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      464 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/config.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      113 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.133526 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.133526 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4369 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/audio_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4851 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/layers.py
--rw-r--r--   0 runner    (1001) docker     (123)     6363 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/stft.py
--rw-r--r--   0 runner    (1001) docker     (123)     3542 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/common/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    28180 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tacotron2/model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.137526 jac_speech-1.4.0.8/jac_speech/tts/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tests/test_tts.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.137526 jac_speech-1.4.0.8/jac_speech/tts/text/
--rw-r--r--   0 runner    (1001) docker     (123)     2437 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/text/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/text/cleaners.py
--rw-r--r--   0 runner    (1001) docker     (123)     2609 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/text/cmudict.py
--rw-r--r--   0 runner    (1001) docker     (123)     2483 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/text/numbers.py
--rw-r--r--   0 runner    (1001) docker     (123)      864 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/text/symbols.py
--rw-r--r--   0 runner    (1001) docker     (123)     2998 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/tts.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.137526 jac_speech-1.4.0.8/jac_speech/tts/waveglow/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/waveglow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/waveglow/denoiser.py
--rw-r--r--   0 runner    (1001) docker     (123)    13399 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/tts/waveglow/model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.141526 jac_speech-1.4.0.8/jac_speech/vc_tts/
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/action_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3339 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/models.json
--rw-r--r--   0 runner    (1001) docker     (123)       84 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.141526 jac_speech-1.4.0.8/jac_speech/vc_tts/text/
--rw-r--r--   0 runner    (1001) docker     (123)      263 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/text/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/text/cleaners.py
--rw-r--r--   0 runner    (1001) docker     (123)     2483 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/text/numbers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/jac_speech/vc_tts/vc_tts.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-08 14:13:32.129526 jac_speech-1.4.0.8/jac_speech.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      238 2023-02-08 14:13:32.000000 jac_speech-1.4.0.8/jac_speech.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1348 2023-02-08 14:13:32.000000 jac_speech-1.4.0.8/jac_speech.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-08 14:13:32.000000 jac_speech-1.4.0.8/jac_speech.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-02-08 14:13:32.000000 jac_speech-1.4.0.8/jac_speech.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-02-08 14:13:32.000000 jac_speech-1.4.0.8/jac_speech.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-08 14:13:32.141526 jac_speech-1.4.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2019 2023-02-08 14:13:12.000000 jac_speech-1.4.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)      218 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.432230 jac_speech-1.4.0.9/jac_speech/
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      316 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/jac_speech/stt/
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/stt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       82 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/stt/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5815 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/stt/stt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/jac_speech/vc_tts/
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/action_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3339 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/models.json
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/jac_speech/vc_tts/text/
+-rw-r--r--   0 runner    (1001) docker     (123)      263 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/text/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/text/cleaners.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2483 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/text/numbers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/jac_speech/vc_tts/vc_tts.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-14 17:26:45.432230 jac_speech-1.4.0.9/jac_speech.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      218 2023-02-14 17:26:45.000000 jac_speech-1.4.0.9/jac_speech.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-02-14 17:26:45.000000 jac_speech-1.4.0.9/jac_speech.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-14 17:26:45.000000 jac_speech-1.4.0.9/jac_speech.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      370 2023-02-14 17:26:45.000000 jac_speech-1.4.0.9/jac_speech.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-02-14 17:26:45.000000 jac_speech-1.4.0.9/jac_speech.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-14 17:26:45.436230 jac_speech-1.4.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2012 2023-02-14 17:25:58.000000 jac_speech-1.4.0.9/setup.py
```

### Comparing `jac_speech-1.4.0.8/README.md` & `jac_speech-1.4.0.9/README.md`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/stt/stt.py` & `jac_speech-1.4.0.9/jac_speech/stt/stt.py`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/tts/text/cleaners.py` & `jac_speech-1.4.0.9/jac_speech/vc_tts/text/cleaners.py`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/tts/text/numbers.py` & `jac_speech-1.4.0.9/jac_speech/vc_tts/text/numbers.py`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/vc_tts/action_utils.py` & `jac_speech-1.4.0.9/jac_speech/vc_tts/action_utils.py`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/vc_tts/models.json` & `jac_speech-1.4.0.9/jac_speech/vc_tts/models.json`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/jac_speech/vc_tts/vc_tts.py` & `jac_speech-1.4.0.9/jac_speech/vc_tts/vc_tts.py`

 * *Files identical despite different names*

### Comparing `jac_speech-1.4.0.8/setup.py` & `jac_speech-1.4.0.9/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools.command.install import install
 import atexit
 import sys
 import platform
 import os
 
 
-MODULES = ["stt", "tts", "vc_tts"]
+MODULES = ["stt", "vc_tts"]
 INSTALLABLE_MODULES = []
 
 
 def _post_install():
     UNSUPPORTED_MODULES = [
         module for module in MODULES if module not in INSTALLABLE_MODULES
     ]
```

