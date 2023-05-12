# Comparing `tmp/similarity-ranker-1.0.0.tar.gz` & `tmp/similarity-ranker-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "similarity-ranker-1.0.0.tar", last modified: Fri May 12 15:10:17 2023, max compression
+gzip compressed data, was "similarity-ranker-1.0.1.tar", last modified: Fri May 12 22:46:31 2023, max compression
```

## Comparing `similarity-ranker-1.0.0.tar` & `similarity-ranker-1.0.1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 15:10:17.231867 similarity-ranker-1.0.0/
--rw-r--r--   0 chiubowen   (501) staff       (20)     1846 2023-05-12 15:10:17.231763 similarity-ranker-1.0.0/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)     1744 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/README.md
--rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-12 15:10:17.231897 similarity-ranker-1.0.0/setup.cfg
--rw-r--r--   0 chiubowen   (501) staff       (20)      532 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/setup.py
-drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 15:10:17.231585 similarity-ranker-1.0.0/similarity_ranker.egg-info/
--rw-r--r--   0 chiubowen   (501) staff       (20)     1846 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/PKG-INFO
--rw-r--r--   0 chiubowen   (501) staff       (20)      287 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/SOURCES.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/dependency_links.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       61 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/entry_points.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       34 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/requires.txt
--rw-r--r--   0 chiubowen   (501) staff       (20)       18 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.egg-info/top_level.txt
--rwxr-xr-x   0 chiubowen   (501) staff       (20)     2844 2023-05-12 15:10:17.000000 similarity-ranker-1.0.0/similarity_ranker.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 22:46:31.677071 similarity-ranker-1.0.1/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     1989 2023-05-12 22:46:31.676944 similarity-ranker-1.0.1/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)     1887 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/README.md
+-rw-r--r--   0 chiubowen   (501) staff       (20)       38 2023-05-12 22:46:31.677107 similarity-ranker-1.0.1/setup.cfg
+-rw-r--r--   0 chiubowen   (501) staff       (20)      532 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/setup.py
+drwxr-xr-x   0 chiubowen   (501) staff       (20)        0 2023-05-12 22:46:31.676766 similarity-ranker-1.0.1/similarity_ranker.egg-info/
+-rw-r--r--   0 chiubowen   (501) staff       (20)     1989 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/PKG-INFO
+-rw-r--r--   0 chiubowen   (501) staff       (20)      287 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/SOURCES.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)        1 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/dependency_links.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       61 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/entry_points.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       34 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/requires.txt
+-rw-r--r--   0 chiubowen   (501) staff       (20)       18 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.egg-info/top_level.txt
+-rwxr-xr-x   0 chiubowen   (501) staff       (20)     3214 2023-05-12 22:46:31.000000 similarity-ranker-1.0.1/similarity_ranker.py
```

### Comparing `similarity-ranker-1.0.0/PKG-INFO` & `similarity-ranker-1.0.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,17 @@
 Metadata-Version: 2.1
 Name: similarity-ranker
-Version: 1.0.0
+Version: 1.0.1
 Description-Content-Type: text/markdown
 
-# Similarity Ranker
-這個專案是用來找到與給定查詢句子最相似的嵌入向量。使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
+# 積木塊 Similarity Ranker v1.0.0 by Bowen Chiu
+- 找到與給定查詢句子 v.s. 最相似的嵌入向量
+- 這東西可以用來做任意 .txt & .pt 遞迴子目錄的相似度比對
+- 找出排名最相似的 top 10 輸出 .json
+- 使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
 
 ## 環境設置
 
 在開始之前，首先確保你已經安裝了以下的 Python 庫：
 ```
 python3 -m pip install similarity-ranker
 ```
```

### Comparing `similarity-ranker-1.0.0/README.md` & `similarity-ranker-1.0.1/similarity_ranker.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,9 +1,17 @@
-# Similarity Ranker
-這個專案是用來找到與給定查詢句子最相似的嵌入向量。使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
+Metadata-Version: 2.1
+Name: similarity-ranker
+Version: 1.0.1
+Description-Content-Type: text/markdown
+
+# 積木塊 Similarity Ranker v1.0.0 by Bowen Chiu
+- 找到與給定查詢句子 v.s. 最相似的嵌入向量
+- 這東西可以用來做任意 .txt & .pt 遞迴子目錄的相似度比對
+- 找出排名最相似的 top 10 輸出 .json
+- 使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
 
 ## 環境設置
 
 在開始之前，首先確保你已經安裝了以下的 Python 庫：
 ```
 python3 -m pip install similarity-ranker
 ```
```

### Comparing `similarity-ranker-1.0.0/setup.py` & `similarity-ranker-1.0.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup, find_packages
 
 with open('requirements.txt') as f:
     requirements = [line.strip() for line in f.readlines()]
 
 setup(
     name="similarity-ranker",
-    version="1.0.0",
+    version="1.0.1",
     packages=find_packages(),
     py_modules=['similarity_ranker'],
     install_requires=requirements,
     entry_points={
         'console_scripts': [
             'similarity_ranker = similarity_ranker:main',
         ],
```

### Comparing `similarity-ranker-1.0.0/similarity_ranker.egg-info/PKG-INFO` & `similarity-ranker-1.0.1/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,14 +1,12 @@
-Metadata-Version: 2.1
-Name: similarity-ranker
-Version: 1.0.0
-Description-Content-Type: text/markdown
-
-# Similarity Ranker
-這個專案是用來找到與給定查詢句子最相似的嵌入向量。使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
+# 積木塊 Similarity Ranker v1.0.0 by Bowen Chiu
+- 找到與給定查詢句子 v.s. 最相似的嵌入向量
+- 這東西可以用來做任意 .txt & .pt 遞迴子目錄的相似度比對
+- 找出排名最相似的 top 10 輸出 .json
+- 使用的是 Hugging Face Transformers 的 `paraphrase-multilingual-MiniLM-L12-v2` 模型。
 
 ## 環境設置
 
 在開始之前，首先確保你已經安裝了以下的 Python 庫：
 ```
 python3 -m pip install similarity-ranker
 ```
```

### Comparing `similarity-ranker-1.0.0/similarity_ranker.py` & `similarity-ranker-1.0.1/similarity_ranker.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,49 +1,51 @@
 #!/usr/bin/env python
-# similarity_ranker.py
 import argparse
 import glob
+import heapq
 import json
 import os
 
 import torch
 from scipy.spatial.distance import cosine
+# 1.2s 慢速瓶頸
 from sentence_transformers import SentenceTransformer
 
 
 def find_files(folder, extension):
     return glob.glob(f"{folder}/**/*{extension}", recursive=True)
 
 
-def query_embeddings(query, embeddings_folder):
+def query_embeddings(query, embeddings_folder, top_n):
+    # 1.5s 慢速瓶頸
     model = SentenceTransformer('paraphrase-multilingual-MiniLM-L12-v2')
-
     query_embedding = model.encode(query)
-
     embeddings_files = find_files(embeddings_folder, '.pt')
-
-    similarities = []
+    max_heap = []
     for embed_file in embeddings_files:
         embedding = torch.load(embed_file)
         similarity = 1 - cosine(query_embedding, embedding)
-        similarities.append((embed_file, similarity))
-
-    return sorted(similarities, key=lambda x: x[1], reverse=True)
+        if len(max_heap) < top_n:
+            heapq.heappush(max_heap, (similarity, embed_file))
+        elif max_heap[0][0] < similarity:
+            heapq.heappop(max_heap)
+            heapq.heappush(max_heap, (similarity, embed_file))
+    ranking = [(embed_file, similarity) for similarity, embed_file in sorted(max_heap, reverse=True)]
+    return ranking
 
 
 def save_ranking_to_json(prompt, ranking, txt_folder, output_file):
     txt_files = find_files(txt_folder, '.txt')
 
-    top_ranking = ranking[:10]
     result = {
         'prompt': prompt,
         'ranking': []
     }
 
-    for idx, (embed_file, similarity) in enumerate(top_ranking):
+    for idx, (embed_file, similarity) in enumerate(ranking):
         txt_file = os.path.splitext(embed_file)[0] + '.txt'
         txt_file_path = [f for f in txt_files if os.path.basename(f) == os.path.basename(txt_file)][0]
         with open(txt_file_path, 'r') as f:
             content = f.read()
 
         result['ranking'].append({
             'rank': idx + 1,
@@ -51,31 +53,33 @@
             'file': txt_file_path,
             'content': content
         })
 
     os.makedirs(os.path.dirname(output_file), exist_ok=True)
     with open(output_file, 'w', encoding='utf-8') as f:
         json.dump(result, f, ensure_ascii=False, indent=4)
-    with open(output_file, 'r') as f:
-        print(f.read())
+    print(result)
+    return result
 
 
 def parse_arguments():
     parser = argparse.ArgumentParser(
         description='Find the most similar embeddings for a given query sentence using Hugging Face Transformers.')
     parser.add_argument('--prompt', type=str, required=True, help='Prompt sentence for finding similar embeddings.')
     parser.add_argument('--txt-folder', type=str, required=True, help='Folder containing the txt files.')
     parser.add_argument('--embeddings-folder', type=str, required=True, help='Folder containing the embeddings files.')
     parser.add_argument('--output-json', type=str, default='data/top_similarity.json',
                         help='Output JSON file containing the top 10 similar txt files (default: data/top_similarity.json)')
+    parser.add_argument('--top-n', type=int, default=3,
+                        help='Top N results to maintain in the priority queue (default: 10)')
     return parser.parse_args()
 
 
 def main():
     args = parse_arguments()
-    ranking = query_embeddings(args.prompt, args.embeddings_folder)
+    ranking = query_embeddings(args.prompt, args.embeddings_folder, args.top_n)
     save_ranking_to_json(args.prompt, ranking, args.txt_folder, args.output_json)
-    print(f'Top 10 similar txt files saved to {args.output_json}')
+    print(f'Top similar txt files saved to {args.output_json}')
 
 
 if __name__ == '__main__':
     main()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

