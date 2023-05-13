# Comparing `tmp/similarity-ranker-1.0.1.tar.gz` & `tmp/similarity-ranker-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "similarity-ranker-1.0.1.tar", last modified: Fri May 12 22:46:31 2023, max compression
+gzip compressed data, was "similarity-ranker-1.0.2.tar", last modified: Sat May 13 02:31:43 2023, max compression
```

## Comparing `similarity-ranker-1.0.1.tar` & `similarity-ranker-1.0.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 22:46:31.677071 similarity-ranker-1.0.1/
--rw-r--r--   0 chiubowen   (501) staff       (20)     1989 2023-05-12 22:46:31.676944 similarity-ranker-1.0.1/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)     1887 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/README.md
--rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-12 22:46:31.677107 similarity-ranker-1.0.1/setup.cfg
--rw-r--r--   0 chiubowen   (501) staff       (20)      532 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/setup.py
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 22:46:31.676766 similarity-ranker-1.0.1/similarity_ranker.egg-info/
--rw-r--r--   0 chiubowen   (501) staff       (20)     1989 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)      287 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/SOURCES.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/dependency_links.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       61 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/entry_points.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       34 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/requires.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       18 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/top_level.txt
--rwxr-xr-x   0 chiubowen   (501) staff       (20)     3214 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 02:31:43.861741 similarity-ranker-1.0.2/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     2062 2023-05-13 02:31:43.861626 similarity-ranker-1.0.2/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)     1887 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/README.md
+-rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-13 02:31:43.861777 similarity-ranker-1.0.2/setup.cfg
+-rw-r--r--   0 chiubowen   (501) staff       (20)      532 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/setup.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-13 02:31:43.861451 similarity-ranker-1.0.2/similarity_ranker.egg-info/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     2062 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)      287 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/SOURCES.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/dependency_links.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       62 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/entry_points.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       34 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/requires.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       18 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.egg-info/top_level.txt
+-rwxr-xr-x   0 chiubowen   (501) staff       (20)     3260 2023-05-13 02:31:43.000000 similarity-ranker-1.0.2/similarity_ranker.py
```

### Comparing `similarity-ranker-1.0.1/PKG-INFO` & `similarity-ranker-1.0.2/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,14 @@
 Metadata-Version: 2.1
 Name: similarity-ranker
-Version: 1.0.1
+Version: 1.0.2
+Summary: UNKNOWN
+Home-page: UNKNOWN
+License: UNKNOWN
+Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊 Similarity Ranker v1.0.0 by Bowen Chiu
 - 找到與給定查詢句子 v.s. 最相似的嵌入向量
 - 這東西可以用來做任意 .txt & .pt 遞迴子目錄的相似度比對
 - 找出排名最相似的 top 10 輸出 .json
 - 使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
@@ -73,7 +77,9 @@
 ```
 python3 -m similarity_ranker \
   --prompt "你的查詢句子" \
   --txt-folder "data/txt" \
   --embeddings-folder "data/embeddings" \
   --output-json "data/top_similarity.json"
 ```
+
+
```

### Comparing `similarity-ranker-1.0.1/README.md` & `similarity-ranker-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `similarity-ranker-1.0.1/setup.py` & `similarity-ranker-1.0.2/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     requirements = [line.strip() for line in f.readlines()]
 
 setup(
     name="similarity-ranker",
-    version="1.0.1",
+    version="1.0.2",
     packages=find_packages(),
     py_modules=['similarity_ranker'],
     install_requires=requirements,
     entry_points={
         'console_scripts': [
             'similarity_ranker = similarity_ranker:main',
         ],
```

### Comparing `similarity-ranker-1.0.1/similarity_ranker.egg-info/PKG-INFO` & `similarity-ranker-1.0.2/similarity_ranker.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,14 @@
 Metadata-Version: 2.1
 Name: similarity-ranker
-Version: 1.0.1
+Version: 1.0.2
+Summary: UNKNOWN
+Home-page: UNKNOWN
+License: UNKNOWN
+Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # 積木塊 Similarity Ranker v1.0.0 by Bowen Chiu
 - 找到與給定查詢句子 v.s. 最相似的嵌入向量
 - 這東西可以用來做任意 .txt & .pt 遞迴子目錄的相似度比對
 - 找出排名最相似的 top 10 輸出 .json
 - 使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
@@ -73,7 +77,9 @@
 ```
 python3 -m similarity_ranker \
   --prompt "你的查詢句子" \
   --txt-folder "data/txt" \
   --embeddings-folder "data/embeddings" \
   --output-json "data/top_similarity.json"
 ```
+
+
```

### Comparing `similarity-ranker-1.0.1/similarity_ranker.py` & `similarity-ranker-1.0.2/similarity_ranker.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 #!/usr/bin/env python
+# similarity_ranker
 import argparse
 import glob
 import heapq
 import json
 import os
 
 import torch
@@ -53,15 +54,15 @@
             'file': txt_file_path,
             'content': content
         })
 
     os.makedirs(os.path.dirname(output_file), exist_ok=True)
     with open(output_file, 'w', encoding='utf-8') as f:
         json.dump(result, f, ensure_ascii=False, indent=4)
-    print(result)
+    # print('similarity_ranker.py:',result)
     return result
 
 
 def parse_arguments():
     parser = argparse.ArgumentParser(
         description='Find the most similar embeddings for a given query sentence using Hugging Face Transformers.')
     parser.add_argument('--prompt', type=str, required=True, help='Prompt sentence for finding similar embeddings.')
```

