# Comparing `tmp/submerger-1.0.4.tar.gz` & `tmp/submerger-2023.5.13.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "submerger-1.0.4.tar", last modified: Tue Feb 14 11:36:36 2023, max compression
+gzip compressed data, was "submerger-2023.5.13.tar", last modified: Sat May 13 21:37:32 2023, max compression
```

## Comparing `submerger-1.0.4.tar` & `submerger-2023.5.13.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-02-14 11:36:36.063344 submerger-1.0.4/
--rw-rw-rw-   0 root         (0) root         (0)    35068 2023-02-14 11:36:26.000000 submerger-1.0.4/LICENSE
--rw-r--r--   0 root         (0) root         (0)     2135 2023-02-14 11:36:36.063344 submerger-1.0.4/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)     1834 2023-02-14 11:36:26.000000 submerger-1.0.4/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-02-14 11:36:36.057343 submerger-1.0.4/bin/
--rwxrwxrwx   0 root         (0) root         (0)     8180 2023-02-14 11:36:26.000000 submerger-1.0.4/bin/submerge
--rw-r--r--   0 root         (0) root         (0)       38 2023-02-14 11:36:36.063344 submerger-1.0.4/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)      621 2023-02-14 11:36:26.000000 submerger-1.0.4/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-02-14 11:36:36.059344 submerger-1.0.4/submerger/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      803 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/merge_subtitles.py
--rw-rw-rw-   0 root         (0) root         (0)     3401 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/subtitle.py
--rw-rw-rw-   0 root         (0) root         (0)     1109 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/subtitle_format.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-02-14 11:36:36.062344 submerger-1.0.4/submerger/test/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      453 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/execute_command.py
--rw-rw-rw-   0 root         (0) root         (0)     3620 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/integration_test_submerger.py
--rw-rw-rw-   0 root         (0) root         (0)      755 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/lint_test_submerger.py
--rw-rw-rw-   0 root         (0) root         (0)     1758 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/test_merge_subtitle.py
--rw-rw-rw-   0 root         (0) root         (0)     1675 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/test_subtitle.py
--rw-rw-rw-   0 root         (0) root         (0)     2955 2023-02-14 11:36:26.000000 submerger-1.0.4/submerger/test/test_subtitle_format.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-02-14 11:36:36.060344 submerger-1.0.4/submerger.egg-info/
--rw-r--r--   0 root         (0) root         (0)     2135 2023-02-14 11:36:36.000000 submerger-1.0.4/submerger.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      558 2023-02-14 11:36:36.000000 submerger-1.0.4/submerger.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-02-14 11:36:36.000000 submerger-1.0.4/submerger.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       19 2023-02-14 11:36:36.000000 submerger-1.0.4/submerger.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       10 2023-02-14 11:36:36.000000 submerger-1.0.4/submerger.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:32.695977 submerger-2023.5.13/
+-rw-rw-rw-   0 root         (0) root         (0)    35068 2023-05-13 21:37:22.000000 submerger-2023.5.13/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     2139 2023-05-13 21:37:32.694977 submerger-2023.5.13/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     1834 2023-05-13 21:37:22.000000 submerger-2023.5.13/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:32.689977 submerger-2023.5.13/bin/
+-rwxrwxrwx   0 root         (0) root         (0)     8644 2023-05-13 21:37:22.000000 submerger-2023.5.13/bin/submerge
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 21:37:32.695977 submerger-2023.5.13/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)      626 2023-05-13 21:37:32.000000 submerger-2023.5.13/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:32.690977 submerger-2023.5.13/submerger/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      803 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/merge_subtitles.py
+-rw-rw-rw-   0 root         (0) root         (0)     3401 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/subtitle.py
+-rw-rw-rw-   0 root         (0) root         (0)     1109 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/subtitle_format.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:32.694977 submerger-2023.5.13/submerger/test/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      453 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/execute_command.py
+-rw-rw-rw-   0 root         (0) root         (0)     3268 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/integration_test_submerger.py
+-rw-rw-rw-   0 root         (0) root         (0)      755 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/lint_test_submerger.py
+-rw-rw-rw-   0 root         (0) root         (0)     1758 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/test_merge_subtitle.py
+-rw-rw-rw-   0 root         (0) root         (0)     1675 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/test_subtitle.py
+-rw-rw-rw-   0 root         (0) root         (0)     2955 2023-05-13 21:37:22.000000 submerger-2023.5.13/submerger/test/test_subtitle_format.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 21:37:32.692977 submerger-2023.5.13/submerger.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     2139 2023-05-13 21:37:32.000000 submerger-2023.5.13/submerger.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      558 2023-05-13 21:37:32.000000 submerger-2023.5.13/submerger.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 21:37:32.000000 submerger-2023.5.13/submerger.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       19 2023-05-13 21:37:32.000000 submerger-2023.5.13/submerger.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       10 2023-05-13 21:37:32.000000 submerger-2023.5.13/submerger.egg-info/top_level.txt
```

### Comparing `submerger-1.0.4/LICENSE` & `submerger-2023.5.13/LICENSE`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/PKG-INFO` & `submerger-2023.5.13/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: submerger
-Version: 1.0.4
+Version: 2023.5.13
 Summary: Subtitle merging tool
 Home-page: https://gitlab.com/andr1i/submerger
 Author: Andrii Valiukh
 Author-email: andrii.valiukh0@gmail.com
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
```

### Comparing `submerger-1.0.4/README.md` & `submerger-2023.5.13/README.md`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/bin/submerge` & `submerger-2023.5.13/bin/submerge`

 * *Files 4% similar despite different names*

```diff
@@ -46,24 +46,33 @@
 
 async def merge_global(
         series_dir: Path,
         base_lang: str,
         secondary_lang: str,
 ) -> None:
     async def get_raw_subtitles(episode_path: Path, language: str) -> str:
+        # ./foo_ep1.ger.srt
+        local_subtitle_path = series_dir / \
+            f'{episode_path.stem}.{language}.srt'
+        if (local_subtitle_path.exists()
+                and os.stat(local_subtitle_path).st_size >= MIN_SUBTITLE_SIZE_BYTES):
+            with open(local_subtitle_path, encoding='utf-8') as subtitles:
+                return subtitles.read()
+
+        #  ./foo_ep1/German.srt
         for subtitle_path in sorted(series_dir.glob(f'**/{episode_path.stem}/*')):
             subtitles_name = subtitle_path.stem.lower()
             subtitle_suffix = subtitle_path.suffix.lower()
             if (subtitle_suffix == '.srt'
                     and os.stat(Path(subtitle_path)).st_size >= MIN_SUBTITLE_SIZE_BYTES
                     and re.search(f'^[^a-z]*{language}', subtitles_name)):
                 with open(subtitle_path, encoding='utf-8') as subtitles:
                     return subtitles.read()
 
-        return await extract_subtitles(episode_path, language)
+        return await extract_subtitles_from_media_file(episode_path, language)
 
     for episode in sorted(series_dir.glob('*')):
         if episode.suffix.lower() not in VIDEO_FILE_FORMATS:
             continue
 
         base_lang_subs, secondary_lang_subs = '', ''
         errors = []
@@ -89,15 +98,15 @@
                 base_lang_subs,
                 BASE_SUBTITLE_FORMAT,
                 secondary_lang_subs,
                 SECONDARY_SUBTITLE_FORMAT,
             ))
 
 
-async def extract_subtitles(video: Path, language: str) -> str:
+async def extract_subtitles_from_media_file(video: Path, language: str) -> str:
     ffmpeg_command = [
         'ffmpeg',
         '-i',
         str(video),
         '-map',
         f'0:m:language:{language}',
         '-map',
@@ -105,15 +114,15 @@
         '-map',
         '-0:a',
         '-f',
         'srt',
         'pipe:1',
     ]
 
-    # Execute ffmpeg command
+    # Execute `ffmpeg` command
     pipe = await asyncio.create_subprocess_exec(
         *ffmpeg_command,
         stdout=asyncio.subprocess.PIPE,
         stderr=asyncio.subprocess.PIPE,
     )
 
     stdout, _ = await pipe.communicate()
@@ -129,17 +138,17 @@
         video: Path,
         file_to_write: Path,
         base_lang: str,
         additional_lang: str,
 ) -> None:
     with open(file_to_write, 'w', encoding='utf-8') as dual_subtitle:
         dual_subtitle.write(merge_subtitles(
-            await extract_subtitles(video, base_lang),
+            await extract_subtitles_from_media_file(video, base_lang),
             BASE_SUBTITLE_FORMAT,
-            await extract_subtitles(video, additional_lang),
+            await extract_subtitles_from_media_file(video, additional_lang),
             SECONDARY_SUBTITLE_FORMAT,
         ))
 
 
 async def run():
     # pylint: disable=too-many-return-statements
     parser = argparse.ArgumentParser()
```

### Comparing `submerger-1.0.4/setup.py` & `submerger-2023.5.13/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 setup(
     author='Andrii Valiukh',
     author_email='andrii.valiukh0@gmail.com',
     description='Subtitle merging tool',
     long_description=long_description,
     long_description_content_type='text/markdown',
     name='submerger',
-    version='1.0.4',
+    version='2023.05.13',
     url='https://gitlab.com/andr1i/submerger',
     packages=find_packages(),
     python_requires=">=3.10",
     install_requires=[],
     extras_require={'dev': [
         'mypy',
         'pylint',
```

### Comparing `submerger-1.0.4/submerger/merge_subtitles.py` & `submerger-2023.5.13/submerger/merge_subtitles.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/subtitle.py` & `submerger-2023.5.13/submerger/subtitle.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/subtitle_format.py` & `submerger-2023.5.13/submerger/subtitle_format.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/test/lint_test_submerger.py` & `submerger-2023.5.13/submerger/test/lint_test_submerger.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/test/test_merge_subtitle.py` & `submerger-2023.5.13/submerger/test/test_merge_subtitle.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/test/test_subtitle.py` & `submerger-2023.5.13/submerger/test/test_subtitle.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger/test/test_subtitle_format.py` & `submerger-2023.5.13/submerger/test/test_subtitle_format.py`

 * *Files identical despite different names*

### Comparing `submerger-1.0.4/submerger.egg-info/PKG-INFO` & `submerger-2023.5.13/submerger.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: submerger
-Version: 1.0.4
+Version: 2023.5.13
 Summary: Subtitle merging tool
 Home-page: https://gitlab.com/andr1i/submerger
 Author: Andrii Valiukh
 Author-email: andrii.valiukh0@gmail.com
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
```

### Comparing `submerger-1.0.4/submerger.egg-info/SOURCES.txt` & `submerger-2023.5.13/submerger.egg-info/SOURCES.txt`

 * *Files identical despite different names*

