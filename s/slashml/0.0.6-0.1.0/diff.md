# Comparing `tmp/slashml-0.0.6.tar.gz` & `tmp/slashml-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/Users/faizank/workspace/experiments/live_projects/slashml/sdk_tests/slashml/dist/.tmp-d_ea_6v9/slashml-0.0.6.tar", last modified: Thu May 11 05:12:50 2023, max compression
+gzip compressed data, was "/Users/faizank/workspace/experiments/live_projects/slashml/sdk_tests/slashml/dist/.tmp-hl4q8mjl/slashml-0.1.0.tar", last modified: Sat May 13 05:57:20 2023, max compression
```

## Comparing `slashml-0.0.6.tar` & `slashml-0.1.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-11 05:12:50.756911 slashml-0.0.6/
--rw-r--r--   0 faizank    (501) staff       (20)     1064 2023-04-24 05:35:14.000000 slashml-0.0.6/LICENSE.txt
--rw-r--r--   0 faizank    (501) staff       (20)     5452 2023-05-11 05:12:50.756733 slashml-0.0.6/PKG-INFO
--rw-r--r--   0 faizank    (501) staff       (20)     5132 2023-05-11 05:12:25.000000 slashml-0.0.6/README.md
--rw-r--r--   0 faizank    (501) staff       (20)       38 2023-05-11 05:12:50.756969 slashml-0.0.6/setup.cfg
--rw-r--r--   0 faizank    (501) staff       (20)     1022 2023-05-11 05:12:25.000000 slashml-0.0.6/setup.py
-drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-11 05:12:50.755482 slashml-0.0.6/slashml/
--rw-r--r--   0 faizank    (501) staff       (20)      190 2023-05-08 20:59:11.000000 slashml-0.0.6/slashml/__init__.py
--rw-r--r--   0 faizank    (501) staff       (20)     2219 2023-05-11 05:12:25.000000 slashml-0.0.6/slashml/speech_to_text.py
--rw-r--r--   0 faizank    (501) staff       (20)     1780 2023-05-11 05:12:25.000000 slashml-0.0.6/slashml/text_summarization.py
--rw-r--r--   0 faizank    (501) staff       (20)     1759 2023-05-11 05:12:25.000000 slashml-0.0.6/slashml/text_to_speech.py
--rw-r--r--   0 faizank    (501) staff       (20)     1257 2023-05-08 22:40:33.000000 slashml-0.0.6/slashml/utils.py
-drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-11 05:12:50.756525 slashml-0.0.6/slashml.egg-info/
--rw-r--r--   0 faizank    (501) staff       (20)     5452 2023-05-11 05:12:50.000000 slashml-0.0.6/slashml.egg-info/PKG-INFO
--rw-r--r--   0 faizank    (501) staff       (20)      313 2023-05-11 05:12:50.000000 slashml-0.0.6/slashml.egg-info/SOURCES.txt
--rw-r--r--   0 faizank    (501) staff       (20)        1 2023-05-11 05:12:50.000000 slashml-0.0.6/slashml.egg-info/dependency_links.txt
--rw-r--r--   0 faizank    (501) staff       (20)       31 2023-05-11 05:12:50.000000 slashml-0.0.6/slashml.egg-info/requires.txt
--rw-r--r--   0 faizank    (501) staff       (20)        8 2023-05-11 05:12:50.000000 slashml-0.0.6/slashml.egg-info/top_level.txt
+drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-13 05:57:20.763928 slashml-0.1.0/
+-rw-r--r--   0 faizank    (501) staff       (20)     1064 2023-04-24 05:35:14.000000 slashml-0.1.0/LICENSE.txt
+-rw-r--r--   0 faizank    (501) staff       (20)     5539 2023-05-13 05:57:20.763738 slashml-0.1.0/PKG-INFO
+-rw-r--r--   0 faizank    (501) staff       (20)     5219 2023-05-13 05:57:02.000000 slashml-0.1.0/README.md
+-rw-r--r--   0 faizank    (501) staff       (20)       38 2023-05-13 05:57:20.763981 slashml-0.1.0/setup.cfg
+-rw-r--r--   0 faizank    (501) staff       (20)     1022 2023-05-13 05:57:02.000000 slashml-0.1.0/setup.py
+drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-13 05:57:20.762528 slashml-0.1.0/slashml/
+-rw-r--r--   0 faizank    (501) staff       (20)      190 2023-05-08 20:59:11.000000 slashml-0.1.0/slashml/__init__.py
+-rw-r--r--   0 faizank    (501) staff       (20)     2325 2023-05-13 05:57:02.000000 slashml-0.1.0/slashml/speech_to_text.py
+-rw-r--r--   0 faizank    (501) staff       (20)     1780 2023-05-11 05:12:25.000000 slashml-0.1.0/slashml/text_summarization.py
+-rw-r--r--   0 faizank    (501) staff       (20)     1759 2023-05-11 05:12:25.000000 slashml-0.1.0/slashml/text_to_speech.py
+-rw-r--r--   0 faizank    (501) staff       (20)     1257 2023-05-13 03:15:49.000000 slashml-0.1.0/slashml/utils.py
+drwxr-xr-x   0 faizank    (501) staff       (20)        0 2023-05-13 05:57:20.763512 slashml-0.1.0/slashml.egg-info/
+-rw-r--r--   0 faizank    (501) staff       (20)     5539 2023-05-13 05:57:20.000000 slashml-0.1.0/slashml.egg-info/PKG-INFO
+-rw-r--r--   0 faizank    (501) staff       (20)      313 2023-05-13 05:57:20.000000 slashml-0.1.0/slashml.egg-info/SOURCES.txt
+-rw-r--r--   0 faizank    (501) staff       (20)        1 2023-05-13 05:57:20.000000 slashml-0.1.0/slashml.egg-info/dependency_links.txt
+-rw-r--r--   0 faizank    (501) staff       (20)       31 2023-05-13 05:57:20.000000 slashml-0.1.0/slashml.egg-info/requires.txt
+-rw-r--r--   0 faizank    (501) staff       (20)        8 2023-05-13 05:57:20.000000 slashml-0.1.0/slashml.egg-info/top_level.txt
```

### Comparing `slashml-0.0.6/LICENSE.txt` & `slashml-0.1.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `slashml-0.0.6/PKG-INFO` & `slashml-0.1.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: slashml
-Version: 0.0.6
+Version: 0.1.0
 Summary: A Python client for interacting with SlashML servicesDeveloped by SlashML.
 Home-page: https://slashml.com/
 Author: eff-kay
 Author-email: faiizan14@gmail.com
 License: MIT
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
@@ -117,17 +117,19 @@
 If the user preferes using the API calls directly, the documentation is available [here](https://docs.slashml.com/).
 
 ## Available service providers
 
 ### Speech-to-text
 For transcription, SlashML supports the following service providers:
 
-* [AssemblyAI](https://github.com/AssemblyAI)
+* [AssemblyAI](https://www.assemblyai.com/)
 * [AWS](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/transcribe.html) 
 * Whisper ([OpenAI](https://openai.com/blog/whisper/))
+* [GOOGLE](https://cloud.google.com/speech-to-text)
+* [DEEPGRAM](https://deepgram.com/) 
 
 ### Summarization
 For text summarization, SlashML supports the following service providers:
 
 * Meta Bart (thru [Huggin-face](https://huggingface.co/facebook/bart-large-cnn?text=The+tower+is+324+metres+%281%2C063+ft%29+tall%2C+about+the+same+height+as+an+81-storey+building%2C+and+the+tallest+structure+in+Paris.+Its+base+is+square%2C+measuring+125+metres+%28410+ft%29+on+each+side.+During+its+construction%2C+the+Eiffel+Tower+surpassed+the+Washington+Monument+to+become+the+tallest+man-made+structure+in+the+world%2C+a+title+it+held+for+41+years+until+the+Chrysler+Building+in+New+York+City+was+finished+in+1930.+It+was+the+first+structure+to+reach+a+height+of+300+metres.+Due+to+the+addition+of+a+broadcasting+aerial+at+the+top+of+the+tower+in+1957%2C+it+is+now+taller+than+the+Chrysler+Building+by+5.2+metres+%2817+ft%29.+Excluding+transmitters%2C+the+Eiffel+Tower+is+the+second+tallest+free-standing+structure+in+France+after+the+Millau+Viaduct))
 * Da-Vinci ([OpenAI](https://beta.openai.com/docs/models/overview))
```

### Comparing `slashml-0.0.6/README.md` & `slashml-0.1.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -105,17 +105,19 @@
 If the user preferes using the API calls directly, the documentation is available [here](https://docs.slashml.com/).
 
 ## Available service providers
 
 ### Speech-to-text
 For transcription, SlashML supports the following service providers:
 
-* [AssemblyAI](https://github.com/AssemblyAI)
+* [AssemblyAI](https://www.assemblyai.com/)
 * [AWS](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/transcribe.html) 
 * Whisper ([OpenAI](https://openai.com/blog/whisper/))
+* [GOOGLE](https://cloud.google.com/speech-to-text)
+* [DEEPGRAM](https://deepgram.com/) 
 
 ### Summarization
 For text summarization, SlashML supports the following service providers:
 
 * Meta Bart (thru [Huggin-face](https://huggingface.co/facebook/bart-large-cnn?text=The+tower+is+324+metres+%281%2C063+ft%29+tall%2C+about+the+same+height+as+an+81-storey+building%2C+and+the+tallest+structure+in+Paris.+Its+base+is+square%2C+measuring+125+metres+%28410+ft%29+on+each+side.+During+its+construction%2C+the+Eiffel+Tower+surpassed+the+Washington+Monument+to+become+the+tallest+man-made+structure+in+the+world%2C+a+title+it+held+for+41+years+until+the+Chrysler+Building+in+New+York+City+was+finished+in+1930.+It+was+the+first+structure+to+reach+a+height+of+300+metres.+Due+to+the+addition+of+a+broadcasting+aerial+at+the+top+of+the+tower+in+1957%2C+it+is+now+taller+than+the+Chrysler+Building+by+5.2+metres+%2817+ft%29.+Excluding+transmitters%2C+the+Eiffel+Tower+is+the+second+tallest+free-standing+structure+in+France+after+the+Millau+Viaduct))
 * Da-Vinci ([OpenAI](https://beta.openai.com/docs/models/overview))
```

### Comparing `slashml-0.0.6/setup.py` & `slashml-0.1.0/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 # Read the contents of the README file
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setup(
     name="slashml",
-    version="0.0.6",
+    version="0.1.0",
     url="https://slashml.com/",
     author="eff-kay",
     author_email="faiizan14@gmail.com",
     description=(
         "A Python client for interacting with SlashML services" "Developed by SlashML."
     ),
     long_description=long_description,  # Use the contents of the README file
```

### Comparing `slashml-0.0.6/slashml/speech_to_text.py` & `slashml-0.1.0/slashml/text_to_speech.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,64 +1,49 @@
 import requests
 import time
+
 from enum import Enum
 from .utils import generateURL, baseUrl, generateHeaders, formatResponse, getTaskStatus
 
 
-class SpeechToText:
+class TextToSpeech:
     class ServiceProvider(Enum):
-        ASSEMBLY = "assembly"
+        GOOGLE = "google"
         AWS = "aws"
-        WHISPER = "whisper"
 
         @classmethod
         def choices(cls):
             return [key.value for key in cls]
 
-    _base_url = baseUrl("speech-to-text", "v1")
+    _base_url = baseUrl("text-to-speech", "v1")
     _headers = None
 
     def __init__(self, api_key: str = None):
         self._headers = generateHeaders(api_key)
 
-    def upload_audio(self, file_location: str):
-        url = generateURL(self._base_url, "upload")
-        files = [("audio", ("test_audio.mp3", open(file_location, "rb"), "audio/mpeg"))]
-        response = requests.post(url, headers=self._headers, files=files)
-        return formatResponse(response)
-
-    def submit_job(self, upload_url: str, service_provider: ServiceProvider):
+    def submit_job(self, text: str, service_provider: ServiceProvider):
         url = generateURL(self._base_url, "jobs")
-        payload = {
-            "uploaded_audio_url": upload_url,
-            "service_provider": service_provider.value,
-        }
+        payload = {"text": text, "service_provider": service_provider.value}
         response = requests.post(url, headers=self._headers, data=payload)
         return formatResponse(response)
 
     def status(self, job_id: str, service_provider: ServiceProvider):
         return getTaskStatus(self._base_url, self._headers, job_id, service_provider)
-
-    def execute(self, upload_url: str, service_provider: ServiceProvider):
+    
+    def execute(self, text: str, service_provider: ServiceProvider):
         url = generateURL(self._base_url, "jobs")
-
-        payload = {
-            "uploaded_audio_url": upload_url,
-            "service_provider": service_provider.value,
-        }
-
+        payload = {"text": text, "service_provider": service_provider.value}
         response = requests.post(url, headers=self._headers, data=payload)
         job = formatResponse(response)
 
         assert job.status != "ERROR", f"{job}"
         print(f"Got Job ID: {job.id}")
-        
+
         # check job status
         response = getTaskStatus(self._base_url, self._headers, job.id, service_provider)
 
         while response.status == "IN_PROGRESS":
             time.sleep(5)
             response = getTaskStatus(self._base_url, self._headers, job.id, service_provider)
             print(f"Response = {response}. Retrying in 5 seconds")
-
+        
         return response
-
```

### Comparing `slashml-0.0.6/slashml/text_summarization.py` & `slashml-0.1.0/slashml/text_summarization.py`

 * *Files identical despite different names*

### Comparing `slashml-0.0.6/slashml/text_to_speech.py` & `slashml-0.1.0/slashml/speech_to_text.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,49 +1,67 @@
 import requests
 import time
-
 from enum import Enum
 from .utils import generateURL, baseUrl, generateHeaders, formatResponse, getTaskStatus
 
 
-class TextToSpeech:
+class SpeechToText:
     class ServiceProvider(Enum):
-        GOOGLE = "google"
+        ASSEMBLY = "assembly"
         AWS = "aws"
+        WHISPER = "whisper"
+        DEEPGRAM = 'deepgram'
+        GOOGLE = 'google'
 
         @classmethod
         def choices(cls):
             return [key.value for key in cls]
 
-    _base_url = baseUrl("text-to-speech", "v1")
+    _base_url = baseUrl("speech-to-text", "v1")
     _headers = None
 
     def __init__(self, api_key: str = None):
         self._headers = generateHeaders(api_key)
 
-    def submit_job(self, text: str, service_provider: ServiceProvider):
+    def upload_audio(self, file_location: str):
+        url = generateURL(self._base_url, "upload")
+        files = [("audio", ("test_audio.mp3", open(file_location, "rb"), "audio/mpeg"))]
+        response = requests.post(url, headers=self._headers, files=files)
+        return formatResponse(response)
+
+    def submit_job(self, upload_url: str, service_provider: ServiceProvider):
         url = generateURL(self._base_url, "jobs")
-        payload = {"text": text, "service_provider": service_provider.value}
+        payload = {
+            "uploaded_audio_url": upload_url,
+            "service_provider": service_provider.value,
+        }
         response = requests.post(url, headers=self._headers, data=payload)
         return formatResponse(response)
 
     def status(self, job_id: str, service_provider: ServiceProvider):
         return getTaskStatus(self._base_url, self._headers, job_id, service_provider)
-    
-    def execute(self, text: str, service_provider: ServiceProvider):
+
+    def execute(self, upload_url: str, service_provider: ServiceProvider):
         url = generateURL(self._base_url, "jobs")
-        payload = {"text": text, "service_provider": service_provider.value}
+
+        payload = {
+            "uploaded_audio_url": upload_url,
+            "service_provider": service_provider.value,
+        }
+
         response = requests.post(url, headers=self._headers, data=payload)
         job = formatResponse(response)
 
         assert job.status != "ERROR", f"{job}"
         print(f"Got Job ID: {job.id}")
-
+        
         # check job status
         response = getTaskStatus(self._base_url, self._headers, job.id, service_provider)
 
+        # while response.status == "IN_PROGRESS":
         while response.status == "IN_PROGRESS":
             time.sleep(5)
             response = getTaskStatus(self._base_url, self._headers, job.id, service_provider)
             print(f"Response = {response}. Retrying in 5 seconds")
-        
+
         return response
+
```

### Comparing `slashml-0.0.6/slashml/utils.py` & `slashml-0.1.0/slashml/utils.py`

 * *Files identical despite different names*

### Comparing `slashml-0.0.6/slashml.egg-info/PKG-INFO` & `slashml-0.1.0/slashml.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: slashml
-Version: 0.0.6
+Version: 0.1.0
 Summary: A Python client for interacting with SlashML servicesDeveloped by SlashML.
 Home-page: https://slashml.com/
 Author: eff-kay
 Author-email: faiizan14@gmail.com
 License: MIT
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
@@ -117,17 +117,19 @@
 If the user preferes using the API calls directly, the documentation is available [here](https://docs.slashml.com/).
 
 ## Available service providers
 
 ### Speech-to-text
 For transcription, SlashML supports the following service providers:
 
-* [AssemblyAI](https://github.com/AssemblyAI)
+* [AssemblyAI](https://www.assemblyai.com/)
 * [AWS](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/transcribe.html) 
 * Whisper ([OpenAI](https://openai.com/blog/whisper/))
+* [GOOGLE](https://cloud.google.com/speech-to-text)
+* [DEEPGRAM](https://deepgram.com/) 
 
 ### Summarization
 For text summarization, SlashML supports the following service providers:
 
 * Meta Bart (thru [Huggin-face](https://huggingface.co/facebook/bart-large-cnn?text=The+tower+is+324+metres+%281%2C063+ft%29+tall%2C+about+the+same+height+as+an+81-storey+building%2C+and+the+tallest+structure+in+Paris.+Its+base+is+square%2C+measuring+125+metres+%28410+ft%29+on+each+side.+During+its+construction%2C+the+Eiffel+Tower+surpassed+the+Washington+Monument+to+become+the+tallest+man-made+structure+in+the+world%2C+a+title+it+held+for+41+years+until+the+Chrysler+Building+in+New+York+City+was+finished+in+1930.+It+was+the+first+structure+to+reach+a+height+of+300+metres.+Due+to+the+addition+of+a+broadcasting+aerial+at+the+top+of+the+tower+in+1957%2C+it+is+now+taller+than+the+Chrysler+Building+by+5.2+metres+%2817+ft%29.+Excluding+transmitters%2C+the+Eiffel+Tower+is+the+second+tallest+free-standing+structure+in+France+after+the+Millau+Viaduct))
 * Da-Vinci ([OpenAI](https://beta.openai.com/docs/models/overview))
```

