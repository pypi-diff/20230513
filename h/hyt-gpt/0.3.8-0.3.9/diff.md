# Comparing `tmp/hyt-gpt-0.3.8.tar.gz` & `tmp/hyt-gpt-0.3.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hyt-gpt-0.3.8.tar", last modified: Thu May 11 06:43:02 2023, max compression
+gzip compressed data, was "hyt-gpt-0.3.9.tar", last modified: Thu May 11 18:21:30 2023, max compression
```

## Comparing `hyt-gpt-0.3.8.tar` & `hyt-gpt-0.3.9.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 06:43:02.432431 hyt-gpt-0.3.8/
--rw-rw-r--   0 haibin    (1000) haibin    (1000)      702 2023-05-11 06:43:02.432431 hyt-gpt-0.3.8/PKG-INFO
-drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 06:43:02.432431 hyt-gpt-0.3.8/hyt_gpt/
--rw-rw-r--   0 haibin    (1000) haibin    (1000)        0 2023-03-26 03:01:59.000000 hyt-gpt-0.3.8/hyt_gpt/__init__.py
--rw-rw-r--   0 haibin    (1000) haibin    (1000)     4038 2023-05-11 05:46:57.000000 hyt-gpt-0.3.8/hyt_gpt/gpt.py
--rw-rw-r--   0 haibin    (1000) haibin    (1000)     2886 2023-03-26 03:01:59.000000 hyt-gpt-0.3.8/hyt_gpt/notion.py
--rw-rw-r--   0 haibin    (1000) haibin    (1000)    12461 2023-05-11 06:42:30.000000 hyt-gpt-0.3.8/hyt_gpt/youtube.py
-drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 06:43:02.432431 hyt-gpt-0.3.8/hyt_gpt.egg-info/
--rw-rw-r--   0 haibin    (1000) haibin    (1000)      702 2023-05-11 06:43:02.000000 hyt-gpt-0.3.8/hyt_gpt.egg-info/PKG-INFO
--rw-rw-r--   0 haibin    (1000) haibin    (1000)      204 2023-05-11 06:43:02.000000 hyt-gpt-0.3.8/hyt_gpt.egg-info/SOURCES.txt
--rw-rw-r--   0 haibin    (1000) haibin    (1000)        1 2023-05-11 06:43:02.000000 hyt-gpt-0.3.8/hyt_gpt.egg-info/dependency_links.txt
--rw-rw-r--   0 haibin    (1000) haibin    (1000)        8 2023-05-11 06:43:02.000000 hyt-gpt-0.3.8/hyt_gpt.egg-info/top_level.txt
--rw-rw-r--   0 haibin    (1000) haibin    (1000)       38 2023-05-11 06:43:02.432431 hyt-gpt-0.3.8/setup.cfg
--rw-rw-r--   0 haibin    (1000) haibin    (1000)      837 2023-05-11 06:42:53.000000 hyt-gpt-0.3.8/setup.py
+drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 18:21:30.244774 hyt-gpt-0.3.9/
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)      702 2023-05-11 18:21:30.244774 hyt-gpt-0.3.9/PKG-INFO
+drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 18:21:30.244774 hyt-gpt-0.3.9/hyt_gpt/
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)        0 2023-03-26 03:01:59.000000 hyt-gpt-0.3.9/hyt_gpt/__init__.py
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)     4038 2023-05-11 05:46:57.000000 hyt-gpt-0.3.9/hyt_gpt/gpt.py
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)     2886 2023-03-26 03:01:59.000000 hyt-gpt-0.3.9/hyt_gpt/notion.py
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)    15150 2023-05-11 18:20:38.000000 hyt-gpt-0.3.9/hyt_gpt/youtube.py
+drwxrwxr-x   0 haibin    (1000) haibin    (1000)        0 2023-05-11 18:21:30.244774 hyt-gpt-0.3.9/hyt_gpt.egg-info/
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)      702 2023-05-11 18:21:30.000000 hyt-gpt-0.3.9/hyt_gpt.egg-info/PKG-INFO
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)      204 2023-05-11 18:21:30.000000 hyt-gpt-0.3.9/hyt_gpt.egg-info/SOURCES.txt
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)        1 2023-05-11 18:21:30.000000 hyt-gpt-0.3.9/hyt_gpt.egg-info/dependency_links.txt
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)        8 2023-05-11 18:21:30.000000 hyt-gpt-0.3.9/hyt_gpt.egg-info/top_level.txt
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)       38 2023-05-11 18:21:30.244774 hyt-gpt-0.3.9/setup.cfg
+-rw-rw-r--   0 haibin    (1000) haibin    (1000)      837 2023-05-11 18:21:24.000000 hyt-gpt-0.3.9/setup.py
```

### Comparing `hyt-gpt-0.3.8/PKG-INFO` & `hyt-gpt-0.3.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyt-gpt
-Version: 0.3.8
+Version: 0.3.9
 Summary: A library for GPT and Youtube
 Author: Harbin
 Author-email: harbinfate@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `hyt-gpt-0.3.8/hyt_gpt/gpt.py` & `hyt-gpt-0.3.9/hyt_gpt/gpt.py`

 * *Files identical despite different names*

### Comparing `hyt-gpt-0.3.8/hyt_gpt/notion.py` & `hyt-gpt-0.3.9/hyt_gpt/notion.py`

 * *Files identical despite different names*

### Comparing `hyt-gpt-0.3.8/hyt_gpt/youtube.py` & `hyt-gpt-0.3.9/hyt_gpt/youtube.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,19 +1,23 @@
 import logging
 import re
 import os
 import subprocess
 import io
 import sys
+import traceback
+import pycountry
 from typing import Dict, Any, List, Union, Tuple, Optional
 from .gpt import seg_transcript, chat_gpt
 from datetime import datetime
+from collections import Counter
 from youtube_transcript_api import YouTubeTranscriptApi
 from pydub import AudioSegment
 from pydub.utils import make_chunks
+from celery import Task
 
 # TODO: Use google.cloud.speech_v2 instead of google.cloud.speech_v1p1beta1
 # TODO: Use cloud storage instead of local storage
 # from google.cloud.speech_v2 import SpeechClient
 # from google.cloud.speech_v2.types import cloud_speech
 from google.cloud import speech_v1p1beta1 as speech
 
@@ -29,36 +33,56 @@
 
 
 class HytGpt:
     def __init__(self, gpt_key: str, prompt: str):
         self.gpt_key = gpt_key
         self.prompt = prompt
 
-    def summary(self, ylink: str) -> Dict[str, Any]:
+    def fetch_subtitles(self, ylink: str, task_instance: Optional[Task] = None) -> Dict[str, Any]:
         if not self.is_valid_youtube_url(ylink):
             return {
                 "status": "failed",
                 "url": ylink,
                 "subtitles": [],
                 "summaries": "Invalid youtube url",
             }
+        HytGpt.update_task_instance(task_instance, 0)
         subtitles, language = self.__youtube_subtitle(ylink)
         if not subtitles:
             try:
-                subtitles = self.transcribe_youtube_video(ylink)
+                subtitles, language = self.transcribe_youtube_video(ylink, task_instance)
             except Exception as e:
                 print(f"Exception occurred in transcription: {str(e)}")
+                traceback.print_exc()
                 return {
                     "status": "failed",
                     "url": ylink,
                     "subtitles": subtitles,
+                    "language": language,
                     "summaries": "Subtitle retrieval failed",
                 }
+        HytGpt.update_task_instance(task_instance, 1)
+        return {
+            "status": "success",
+            "url": ylink,
+            "subtitles": subtitles,
+            "language": language,
+            "summaries": "Subtitle retrieval succeeded",
+        }
 
+    def summary(
+        self,
+        ylink: str,
+        subtitles: start_duration_transcript_t,
+        language: str,
+        task_instance: Optional[Task] = None,
+    ) -> Dict[str, Any]:
+        HytGpt.update_task_instance(task_instance, 0)
         seged_text = seg_transcript(subtitles)
+        HytGpt.update_task_instance(task_instance, 0.2)
         summaried_text = ""
         i = 1
 
         for entry in seged_text:
             try:
                 response = chat_gpt(
                     self.gpt_key, self.prompt.format(language=language), entry
@@ -72,16 +96,56 @@
             summaried_text += response + "\n"
         response_data = {
             "status": "success",
             "url": ylink,
             "subtitles": subtitles,
             "summaries": summaried_text,
         }
+        HytGpt.update_task_instance(task_instance, 1)
         return response_data
 
+    def transcribe_youtube_video(
+        self, ylink: str, task_instance: Optional[Task] = None
+    ) -> Tuple[start_duration_transcript_t, str]:
+        video_id = HytGpt.get_youtube_id(ylink)
+        output_file = f"{video_id}.mp3"
+
+        self.__download_youtube_audio(ylink, output_file)
+        HytGpt.update_task_instance(task_instance, 0.1)
+
+        chunk_duration_ms = 60000  # Duration of each audio chunk in milliseconds
+        audio_chunks = self.__split_audio_file(video_id, chunk_duration_ms)
+        HytGpt.update_task_instance(task_instance, 0.2)
+
+        transcripts = []
+        for i, chunk in enumerate(audio_chunks):
+            print(f"Transcribing chunk {i + 1}/{len(audio_chunks)}...")
+            transcripts += self.__transcribe_audio_file(chunk)
+            HytGpt.update_task_instance(task_instance, 0.2 + 0.7 * (i + 1) / len(audio_chunks))
+            os.remove(chunk)
+
+        common_language_code = self.__most_common_language_code(transcripts)
+        common_language_name = self.__language_code_to_name(common_language_code)
+        HytGpt.update_task_instance(task_instance, 0.98)
+
+        os.remove(output_file)
+        return transcripts, common_language_name
+
+    @staticmethod
+    def update_task_instance(task_instance: Optional[Task], progress: float):
+        """
+        Update the task instance with the progress
+        
+        :param task_instance: The task instance
+        :param progress: The progress of the task (between 0 and 1)
+        """
+        if task_instance:
+            progress = int(progress * 100)
+            task_instance.update_state(state="PROGRESS", meta={"progress": progress})
+
     @staticmethod
     def is_valid_youtube_url(url):
         # Regular expression pattern for YouTube URLs
         youtube_url_pattern = re.compile(
             r"(https?://)?(www\.)?(youtube\.com|youtu\.?be)/.+"
         )
 
@@ -133,32 +197,34 @@
                 combined_texts.append(current_text)
                 current_text = next_segment["text"]
 
             current_segment = next_segment
 
         combined_texts.append(current_text)
         return combined_texts
+    
+    def __most_common_language_code(self, results):
+        language_codes = [result["language_code"] for result in results]
+        most_common_code = Counter(language_codes).most_common(1)[0][0]
+        return most_common_code
+    
+    def __language_code_to_name(self, language_code: str) -> str:
+        # Split the language code into parts
+        parts = language_code.split("-")
+
+        # Get the language and region objects from pycountry
+        language = pycountry.languages.get(alpha_3=parts[0])
+        script = pycountry.scripts.get(code=parts[1]) if len(parts) > 1 else None
+
+        # Build the language name string
+        language_name = language.name
+        if script:
+            language_name += f" ({script.name})"
 
-    def transcribe_youtube_video(self, ylink: str) -> start_duration_transcript_t:
-        video_id = HytGpt.get_youtube_id(ylink)
-        output_file = f"{video_id}.mp3"
-
-        self.__download_youtube_audio(ylink, output_file)
-
-        chunk_duration_ms = 60000  # Duration of each audio chunk in milliseconds
-        audio_chunks = self.__split_audio_file(video_id, chunk_duration_ms)
-
-        transcripts = []
-        for i, chunk in enumerate(audio_chunks):
-            print(f"Transcribing chunk {i + 1}/{len(audio_chunks)}...")
-            transcripts += self.__transcribe_audio_file(chunk)
-            os.remove(chunk)
-
-        os.remove(output_file)
-        return transcripts
+        return language_name
 
     def __parse_transcripts(self, results) -> start_duration_transcript_t:
         formatted_results = []
 
         for result in results:
             alternative = result.alternatives[0]  # Select the first alternative
             transcript = alternative.transcript
@@ -231,18 +297,19 @@
         """Get the subtitle of the youtube video
         Args:
             url (str): The url of the youtube video
         Returns:
             Tuple[Union[List[Dict[str, str]], None], str]: The subtitle of the youtube video
         """
         video_id = self.get_youtube_id(url)
-        try :
+        try:
             list = YouTubeTranscriptApi.list_transcripts(video_id)
         except Exception as e:
             logging.error(e)
+            traceback.print_exc()
             return None, ""
         logging.debug(list)
 
         for transcript in list:
             if transcript.language_code in ["en", "zh", "zh-Hans", "zh-Hant"]:
                 return transcript.fetch(), transcript.language
         return None, ""
```

### Comparing `hyt-gpt-0.3.8/hyt_gpt.egg-info/PKG-INFO` & `hyt-gpt-0.3.9/hyt_gpt.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyt-gpt
-Version: 0.3.8
+Version: 0.3.9
 Summary: A library for GPT and Youtube
 Author: Harbin
 Author-email: harbinfate@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `hyt-gpt-0.3.8/setup.py` & `hyt-gpt-0.3.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages, find_namespace_packages
 
 setup(
     name='hyt-gpt',
-    version='0.3.8',
+    version='0.3.9',
     description='A library for GPT and Youtube',
     author='Harbin',
     author_email='harbinfate@gmail.com',
     packages=find_packages(),
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Developers',
```

