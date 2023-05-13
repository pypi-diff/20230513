# Comparing `tmp/xklb-1.26.29.tar.gz` & `tmp/xklb-1.26.30.tar.gz`

## Comparing `xklb-1.26.29.tar` & `xklb-1.26.30.tar`

### file list

```diff
@@ -1,57 +1,57 @@
--rw-r--r--   0        0        0      119 2020-02-02 00:00:00.000000 xklb-1.26.29/.gitattributes
--rw-r--r--   0        0        0      284 2020-02-02 00:00:00.000000 xklb-1.26.29/TODO
--rw-r--r--   0        0        0     1666 2020-02-02 00:00:00.000000 xklb-1.26.29/Windows.md
--rw-r--r--   0        0        0   417004 2020-02-02 00:00:00.000000 xklb-1.26.29/pdm.lock
--rw-r--r--   0        0        0    16847 2020-02-02 00:00:00.000000 xklb-1.26.29/readme.py
--rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 xklb-1.26.29/.github/FUNDING.yml
--rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 xklb-1.26.29/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 xklb-1.26.29/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 xklb-1.26.29/.github/workflows/push.yaml
--rw-r--r--   0        0        0      624 2020-02-02 00:00:00.000000 xklb-1.26.29/sql/transfer.sql
--rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/__init__.py
--rw-r--r--   0        0        0     6996 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/av.py
--rw-r--r--   0        0        0     6866 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/books.py
--rw-r--r--   0        0        0     7536 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/consts.py
--rw-r--r--   0        0        0     7940 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/db.py
--rw-r--r--   0        0        0     7061 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/dl_config.py
--rw-r--r--   0        0        0    14853 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/dl_extract.py
--rw-r--r--   0        0        0    14486 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/fs_extract.py
--rw-r--r--   0        0        0     6158 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/gui.py
--rw-r--r--   0        0        0     6056 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/hn_extract.py
--rw-r--r--   0        0        0     9635 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/lb.py
--rw-r--r--   0        0        0    35723 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/play_actions.py
--rw-r--r--   0        0        0     4545 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/playback.py
--rw-r--r--   0        0        0    26800 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/player.py
--rw-r--r--   0        0        0    14733 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/praw_extract.py
--rw-r--r--   0        0        0    16181 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/stats.py
--rw-r--r--   0        0        0     4109 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/subtitle.py
--rw-r--r--   0        0        0    12091 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/tabs_actions.py
--rw-r--r--   0        0        0     3639 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/tabs_extract.py
--rw-r--r--   0        0        0    21844 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/tube_backend.py
--rw-r--r--   0        0        0     6378 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/tube_extract.py
--rw-r--r--   0        0        0    28274 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/utils.py
--rw-r--r--   0        0        0      644 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/__init__.py
--rw-r--r--   0        0        0     4605 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/bigdirs.py
--rw-r--r--   0        0        0     2775 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/christen.py
--rw-r--r--   0        0        0     2185 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/copy_play_counts.py
--rw-r--r--   0        0        0     8267 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/dedupe.py
--rw-r--r--   0        0        0     2400 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/merge_dbs.py
--rw-r--r--   0        0        0     4022 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/merge_online_local.py
--rw-r--r--   0        0        0     7013 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/move_list.py
--rw-r--r--   0        0        0      754 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/optimize_db.py
--rw-r--r--   0        0        0     9492 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/redownload.py
--rw-r--r--   0        0        0     2335 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/relmv.py
--rw-r--r--   0        0        0    17200 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/scatter.py
--rw-r--r--   0        0        0     2712 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/streaming_tab_loader.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/__init__.py
--rw-r--r--   0        0        0    17101 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/data.py
--rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/extract_links.py
--rw-r--r--   0        0        0     1629 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/nouns.py
--rw-r--r--   0        0        0     2777 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/pushshift.py
--rw-r--r--   0        0        0     2310 2020-02-02 00:00:00.000000 xklb-1.26.29/xklb/scripts/mining/reddit_selftext.py
--rw-r--r--   0        0        0     8385 2020-02-02 00:00:00.000000 xklb-1.26.29/assets/kotobago.png
--rw-r--r--   0        0        0     1462 2020-02-02 00:00:00.000000 xklb-1.26.29/.gitignore
--rw-r--r--   0        0        0     1676 2020-02-02 00:00:00.000000 xklb-1.26.29/LICENSE
--rw-r--r--   0        0        0    40521 2020-02-02 00:00:00.000000 xklb-1.26.29/README.md
--rw-r--r--   0        0        0     2571 2020-02-02 00:00:00.000000 xklb-1.26.29/pyproject.toml
--rw-r--r--   0        0        0    44036 2020-02-02 00:00:00.000000 xklb-1.26.29/PKG-INFO
+-rw-r--r--   0        0        0      119 2020-02-02 00:00:00.000000 xklb-1.26.30/.gitattributes
+-rw-r--r--   0        0        0      284 2020-02-02 00:00:00.000000 xklb-1.26.30/TODO
+-rw-r--r--   0        0        0     1666 2020-02-02 00:00:00.000000 xklb-1.26.30/Windows.md
+-rw-r--r--   0        0        0   417004 2020-02-02 00:00:00.000000 xklb-1.26.30/pdm.lock
+-rw-r--r--   0        0        0    16847 2020-02-02 00:00:00.000000 xklb-1.26.30/readme.py
+-rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 xklb-1.26.30/.github/FUNDING.yml
+-rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 xklb-1.26.30/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 xklb-1.26.30/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 xklb-1.26.30/.github/workflows/push.yaml
+-rw-r--r--   0        0        0      624 2020-02-02 00:00:00.000000 xklb-1.26.30/sql/transfer.sql
+-rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/__init__.py
+-rw-r--r--   0        0        0     6996 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/av.py
+-rw-r--r--   0        0        0     6866 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/books.py
+-rw-r--r--   0        0        0     7536 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/consts.py
+-rw-r--r--   0        0        0     7940 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/db.py
+-rw-r--r--   0        0        0     7061 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/dl_config.py
+-rw-r--r--   0        0        0    14853 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/dl_extract.py
+-rw-r--r--   0        0        0    14486 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/fs_extract.py
+-rw-r--r--   0        0        0     6158 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/gui.py
+-rw-r--r--   0        0        0     6056 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/hn_extract.py
+-rw-r--r--   0        0        0     9635 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/lb.py
+-rw-r--r--   0        0        0    35723 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/play_actions.py
+-rw-r--r--   0        0        0     4545 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/playback.py
+-rw-r--r--   0        0        0    26800 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/player.py
+-rw-r--r--   0        0        0    14733 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/praw_extract.py
+-rw-r--r--   0        0        0    16181 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/stats.py
+-rw-r--r--   0        0        0     4109 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/subtitle.py
+-rw-r--r--   0        0        0    12091 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/tabs_actions.py
+-rw-r--r--   0        0        0     3639 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/tabs_extract.py
+-rw-r--r--   0        0        0    21877 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/tube_backend.py
+-rw-r--r--   0        0        0     6378 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/tube_extract.py
+-rw-r--r--   0        0        0    28274 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/utils.py
+-rw-r--r--   0        0        0      644 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/__init__.py
+-rw-r--r--   0        0        0     4605 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/bigdirs.py
+-rw-r--r--   0        0        0     2775 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/christen.py
+-rw-r--r--   0        0        0     2185 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/copy_play_counts.py
+-rw-r--r--   0        0        0     8267 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/dedupe.py
+-rw-r--r--   0        0        0     2400 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/merge_dbs.py
+-rw-r--r--   0        0        0     4022 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/merge_online_local.py
+-rw-r--r--   0        0        0     7013 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/move_list.py
+-rw-r--r--   0        0        0      754 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/optimize_db.py
+-rw-r--r--   0        0        0     9492 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/redownload.py
+-rw-r--r--   0        0        0     2335 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/relmv.py
+-rw-r--r--   0        0        0    17200 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/scatter.py
+-rw-r--r--   0        0        0     2712 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/streaming_tab_loader.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/__init__.py
+-rw-r--r--   0        0        0    17101 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/data.py
+-rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/extract_links.py
+-rw-r--r--   0        0        0     1629 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/nouns.py
+-rw-r--r--   0        0        0     2777 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/pushshift.py
+-rw-r--r--   0        0        0     2310 2020-02-02 00:00:00.000000 xklb-1.26.30/xklb/scripts/mining/reddit_selftext.py
+-rw-r--r--   0        0        0     8385 2020-02-02 00:00:00.000000 xklb-1.26.30/assets/kotobago.png
+-rw-r--r--   0        0        0     1462 2020-02-02 00:00:00.000000 xklb-1.26.30/.gitignore
+-rw-r--r--   0        0        0     1676 2020-02-02 00:00:00.000000 xklb-1.26.30/LICENSE
+-rw-r--r--   0        0        0    40521 2020-02-02 00:00:00.000000 xklb-1.26.30/README.md
+-rw-r--r--   0        0        0     2571 2020-02-02 00:00:00.000000 xklb-1.26.30/pyproject.toml
+-rw-r--r--   0        0        0    44036 2020-02-02 00:00:00.000000 xklb-1.26.30/PKG-INFO
```

### Comparing `xklb-1.26.29/Windows.md` & `xklb-1.26.30/Windows.md`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/pdm.lock` & `xklb-1.26.30/pdm.lock`

 * *Files 1% similar despite different names*

```diff
@@ -590,15 +590,15 @@
 name = "pillow"
 version = "9.5.0"
 requires_python = ">=3.7"
 summary = "Python Imaging Library (Fork)"
 
 [[package]]
 name = "platformdirs"
-version = "3.5.0"
+version = "3.5.1"
 requires_python = ">=3.7"
 summary = "A small Python package for determining appropriate platform-specific dirs, e.g. a \"user data dir\"."
 
 [[package]]
 name = "pluggy"
 version = "1.0.0"
 requires_python = ">=3.6"
@@ -821,15 +821,15 @@
     "markdown-it-py<3.0.0,>=2.2.0",
     "pygments<3.0.0,>=2.13.0",
     "typing-extensions<5.0,>=4.0.0; python_version < \"3.9\"",
 ]
 
 [[package]]
 name = "ruff"
-version = "0.0.265"
+version = "0.0.267"
 requires_python = ">=3.7"
 summary = "An extremely fast Python linter, written in Rust."
 
 [[package]]
 name = "scalene"
 version = "1.5.19"
 requires_python = ">=3.8"
@@ -2239,17 +2239,17 @@
     {url = "https://files.pythonhosted.org/packages/d9/0e/7c6f054022235830dc2c37ec83e947d9ca09b0b0361e1e5e29983da92294/Pillow-9.5.0-pp38-pypy38_pp73-win_amd64.whl", hash = "sha256:cb841572862f629b99725ebaec3287fc6d275be9b14443ea746c1dd325053cbd"},
     {url = "https://files.pythonhosted.org/packages/db/5c/ba9e291850f594f89436cdca93d36c6f8610d4fb7833a6c257f4481d4174/Pillow-9.5.0-cp38-cp38-musllinux_1_1_x86_64.whl", hash = "sha256:662da1f3f89a302cc22faa9f14a262c2e3951f9dbc9617609a47521c69dd9f8f"},
     {url = "https://files.pythonhosted.org/packages/e7/2a/f3ed578595f8486ee2cc07434460097d89aedd406a3db849b890ca8ec416/Pillow-9.5.0-cp39-cp39-musllinux_1_1_aarch64.whl", hash = "sha256:a127ae76092974abfbfa38ca2d12cbeddcdeac0fb71f9627cc1135bedaf9d51a"},
     {url = "https://files.pythonhosted.org/packages/ec/7d/01404982db598f271ac7c0d0207860f60ab9288cfacce9872eb567cfbfe3/Pillow-9.5.0-cp37-cp37m-macosx_10_10_x86_64.whl", hash = "sha256:5d4ebf8e1db4441a55c509c4baa7a0587a0210f7cd25fcfe74dbbce7a4bd1906"},
     {url = "https://files.pythonhosted.org/packages/f2/43/0892913d499c8df2c88dee69d59e77de19e0c51754a9be82023880641c09/Pillow-9.5.0-cp39-cp39-manylinux_2_17_i686.manylinux2014_i686.whl", hash = "sha256:8aca1152d93dcc27dc55395604dcfc55bed5f25ef4c98716a928bacba90d33a3"},
     {url = "https://files.pythonhosted.org/packages/ff/fc/48a51c0fe2a00d5def57b9981a1e0f8339b516351da7a51500383d833bc8/Pillow-9.5.0-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl", hash = "sha256:608488bdcbdb4ba7837461442b90ea6f3079397ddc968c31265c1e056964f1ef"},
 ]
-"platformdirs 3.5.0" = [
-    {url = "https://files.pythonhosted.org/packages/91/17/3836ffe140abb245726d0e21c5b9b984e2569e7027c20d12e969ec69bd8a/platformdirs-3.5.0.tar.gz", hash = "sha256:7954a68d0ba23558d753f73437c55f89027cf8f5108c19844d4b82e5af396335"},
-    {url = "https://files.pythonhosted.org/packages/ce/cf/279b73aae00f7ba9d5d7664156ef323ebbf16fb556285bb223ecc45031aa/platformdirs-3.5.0-py3-none-any.whl", hash = "sha256:47692bc24c1958e8b0f13dd727307cff1db103fca36399f457da8e05f222fdc4"},
+"platformdirs 3.5.1" = [
+    {url = "https://files.pythonhosted.org/packages/89/7e/c6ff9ddcf93b9b36c90d88111c4db354afab7f9a58c7ac3257fa717f1268/platformdirs-3.5.1-py3-none-any.whl", hash = "sha256:e2378146f1964972c03c085bb5662ae80b2b8c06226c54b2ff4aa9483e8a13a5"},
+    {url = "https://files.pythonhosted.org/packages/9c/0e/ae9ef1049d4b5697e79250c4b2e72796e4152228e67733389868229c92bb/platformdirs-3.5.1.tar.gz", hash = "sha256:412dae91f52a6f84830f39a8078cecd0e866cb72294a5c66808e74d5e88d251f"},
 ]
 "pluggy 1.0.0" = [
     {url = "https://files.pythonhosted.org/packages/9e/01/f38e2ff29715251cf25532b9082a1589ab7e4f571ced434f98d0139336dc/pluggy-1.0.0-py2.py3-none-any.whl", hash = "sha256:74134bbf457f031a36d68416e1509f34bd5ccc019f0bcc952c7b909d06b37bd3"},
     {url = "https://files.pythonhosted.org/packages/a1/16/db2d7de3474b6e37cbb9c008965ee63835bba517e22cdb8c35b5116b5ce1/pluggy-1.0.0.tar.gz", hash = "sha256:4224373bacce55f955a878bf9cfa763c1e360858e330072059e10bad68531159"},
 ]
 "praw 7.7.0" = [
     {url = "https://files.pythonhosted.org/packages/b3/93/55ae62910b94b46ecdd0ee8765289304f8df8deeaa1df7a96b0831c637ff/praw-7.7.0-py3-none-any.whl", hash = "sha256:22155c4b3006733a5ab0754136cf2226917747b61ec037ee335246fe0db5420e"},
@@ -2556,32 +2556,32 @@
     {url = "https://files.pythonhosted.org/packages/45/1e/0c169c6a5381e241ba7404532c16a21d86ab872c9bed8bdcd4c423954103/requests-2.24.0-py2.py3-none-any.whl", hash = "sha256:fe75cc94a9443b9246fc7049224f75604b113c36acb93f87b80ed42c44cbb898"},
     {url = "https://files.pythonhosted.org/packages/da/67/672b422d9daf07365259958912ba533a0ecab839d4084c487a5fe9a5405f/requests-2.24.0.tar.gz", hash = "sha256:b3559a131db72c33ee969480840fff4bb6dd111de7dd27c8ee1f820f4f00231b"},
 ]
 "rich 13.3.5" = [
     {url = "https://files.pythonhosted.org/packages/39/03/6de23bdd88f5ee7f8b03f94f6e88108f5d7ffe6d207e95cdb06d9aa4cd57/rich-13.3.5-py3-none-any.whl", hash = "sha256:69cdf53799e63f38b95b9bf9c875f8c90e78dd62b2f00c13a911c7a3b9fa4704"},
     {url = "https://files.pythonhosted.org/packages/3d/0b/8dd34d20929c4b5e474db2e64426175469c2b7fea5ba71c6d4b3397a9729/rich-13.3.5.tar.gz", hash = "sha256:2d11b9b8dd03868f09b4fffadc84a6a8cda574e40dc90821bd845720ebb8e89c"},
 ]
-"ruff 0.0.265" = [
-    {url = "https://files.pythonhosted.org/packages/27/ee/674d3816cbffa55e4fad4446e2815c783ca0648180a905418edfd664bc50/ruff-0.0.265-py3-none-macosx_10_7_x86_64.whl", hash = "sha256:30ddfe22de6ce4eb1260408f4480bbbce998f954dbf470228a21a9b2c45955e4"},
-    {url = "https://files.pythonhosted.org/packages/40/8d/fbd44882b6ef61c8be8fa9ce6448bb99ff105816ac22e2f2116473809c6d/ruff-0.0.265-py3-none-musllinux_1_2_x86_64.whl", hash = "sha256:1d5a8de2fbaf91ea5699451a06f4074e7a312accfa774ad9327cde3e4fda2081"},
-    {url = "https://files.pythonhosted.org/packages/41/33/f9043ba8a20a667d888adc81768ebdaadaa0d2b760da61912682d62bbff8/ruff-0.0.265-py3-none-win_amd64.whl", hash = "sha256:f54facf286103006171a00ce20388d88ed1d6732db3b49c11feb9bf3d46f90e9"},
-    {url = "https://files.pythonhosted.org/packages/77/cc/8806e6aaf8dc0cd4f41444f5423c31d691b7acf0386665406823f9528e45/ruff-0.0.265-py3-none-win_arm64.whl", hash = "sha256:c78470656e33d32ddc54e8482b1b0fc6de58f1195586731e5ff1405d74421499"},
-    {url = "https://files.pythonhosted.org/packages/94/67/f875768b8ecfbc6264a9fc5e10735359f23b2ac98194bf0512555225b987/ruff-0.0.265-py3-none-manylinux_2_17_ppc64.manylinux2014_ppc64.whl", hash = "sha256:5028950f7af9b119d43d91b215d5044976e43b96a0d1458d193ef0dd3c587bf8"},
-    {url = "https://files.pythonhosted.org/packages/9d/07/7178c1b251c2bfed0676e7f8cd76d6107a5e89b2d1b7b464c084b311dfe6/ruff-0.0.265-py3-none-manylinux_2_17_i686.manylinux2014_i686.whl", hash = "sha256:b279fa55ea175ef953208a6d8bfbcdcffac1c39b38cdb8c2bfafe9222add70bb"},
-    {url = "https://files.pythonhosted.org/packages/9e/35/fb24000483a56339ffe3c00c8b0d12c4ca99201f7f2f30f4799202a20a83/ruff-0.0.265-py3-none-manylinux_2_17_armv7l.manylinux2014_armv7l.whl", hash = "sha256:a8b44a245b60512403a6a03a5b5212da274d33862225c5eed3bcf12037eb19bb"},
-    {url = "https://files.pythonhosted.org/packages/a1/00/135639453182b6c64c507f448764d78f8df90bcd19e4b0e16427407709e0/ruff-0.0.265-py3-none-musllinux_1_2_aarch64.whl", hash = "sha256:9ac13b11d9ad3001de9d637974ec5402a67cefdf9fffc3929ab44c2fcbb850a1"},
-    {url = "https://files.pythonhosted.org/packages/b2/bc/b14c0de95721ef6bd3a1dcfe7b4ce9f368c72a2d5aed7c98e767771c860c/ruff-0.0.265-py3-none-musllinux_1_2_i686.whl", hash = "sha256:d0f9967f84da42d28e3d9d9354cc1575f96ed69e6e40a7d4b780a7a0418d9409"},
-    {url = "https://files.pythonhosted.org/packages/b3/1d/0e544e4b73bafbe88f6c39bce5306fdbf5af07e9d004fe023eeedf9ee548/ruff-0.0.265-py3-none-manylinux_2_17_s390x.manylinux2014_s390x.whl", hash = "sha256:d586e69ab5cbf521a1910b733412a5735936f6a610d805b89d35b6647e2a66aa"},
-    {url = "https://files.pythonhosted.org/packages/b4/c4/7b8b05279a11ba30cf99eb628dbfd2fbf7219c192eb78f9585280bc3ae69/ruff-0.0.265-py3-none-musllinux_1_2_armv7l.whl", hash = "sha256:62a9578b48cfd292c64ea3d28681dc16b1aa7445b7a7709a2884510fc0822118"},
-    {url = "https://files.pythonhosted.org/packages/c7/87/9b9d14b1778edb4ce03e0e80ab9378e12e402dce2b5cd27403b6670b6ed6/ruff-0.0.265-py3-none-manylinux_2_17_ppc64le.manylinux2014_ppc64le.whl", hash = "sha256:4057eb539a1d88eb84e9f6a36e0a999e0f261ed850ae5d5817e68968e7b89ed9"},
-    {url = "https://files.pythonhosted.org/packages/d1/c3/2aeec2adaff3cfa95d713283089568ee905f759e18d034646e3aa85a6282/ruff-0.0.265.tar.gz", hash = "sha256:53c17f0dab19ddc22b254b087d1381b601b155acfa8feed514f0d6a413d0ab3a"},
-    {url = "https://files.pythonhosted.org/packages/e3/d1/433db20e8ef8f67ff7cfa32fdf6b9adb0592a1269fd93e230fd0dfbf64f2/ruff-0.0.265-py3-none-win32.whl", hash = "sha256:9e9db5ccb810742d621f93272e3cc23b5f277d8d00c4a79668835d26ccbe48dd"},
-    {url = "https://files.pythonhosted.org/packages/e7/c3/157c421412809780430110b766f8bdad65b55f0671c00c778d827dbb6f35/ruff-0.0.265-py3-none-manylinux_2_17_aarch64.manylinux2014_aarch64.whl", hash = "sha256:2a9b38bdb40a998cbc677db55b6225a6c4fadcf8819eb30695e1b8470942426b"},
-    {url = "https://files.pythonhosted.org/packages/f4/1c/5161404f7231c37e951f7dce3a4f623733a6563c17724189d003602ce55f/ruff-0.0.265-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.whl", hash = "sha256:aa17b13cd3f29fc57d06bf34c31f21d043735cc9a681203d634549b0e41047d1"},
-    {url = "https://files.pythonhosted.org/packages/fd/ac/1c40dc44ed92744c3a9ca6f07ed2d83f0431d71a02766a7a478e2112fb59/ruff-0.0.265-py3-none-macosx_10_9_x86_64.macosx_11_0_arm64.macosx_10_9_universal2.whl", hash = "sha256:a11bd0889e88d3342e7bc514554bb4461bf6cc30ec115821c2425cfaac0b1b6a"},
+"ruff 0.0.267" = [
+    {url = "https://files.pythonhosted.org/packages/1e/6c/a5a28b7c4df1316ff0ede0ce51af3a9af76b23c6f19a2d9edcd28036aa8d/ruff-0.0.267-py3-none-musllinux_1_2_x86_64.whl", hash = "sha256:5a898953949e37c109dd242cfcf9841e065319995ebb7cdfd213b446094a942f"},
+    {url = "https://files.pythonhosted.org/packages/21/80/c68a5d5117f84b6d4892cf8a5e1b164bd5b14bc0894ce0cba5343e40f132/ruff-0.0.267-py3-none-manylinux_2_17_i686.manylinux2014_i686.whl", hash = "sha256:9adf1307fa9d840d1acaa477eb04f9702032a483214c409fca9dc46f5f157fe3"},
+    {url = "https://files.pythonhosted.org/packages/3e/52/d1015fa5a13e9bd11b7a4e1147f541e52fe666b550f14e9ca1249bdc447b/ruff-0.0.267-py3-none-musllinux_1_2_i686.whl", hash = "sha256:786de30723c71fc46b80a173c3313fc0dbe73c96bd9da8dd1212cbc2f84cdfb2"},
+    {url = "https://files.pythonhosted.org/packages/45/1e/f423a80da2217137ef3d287aec70d978ae71038cce92cdc61659ebb4a063/ruff-0.0.267-py3-none-musllinux_1_2_armv7l.whl", hash = "sha256:2107cec3699ca4d7bd41543dc1d475c97ae3a21ea9212238b5c2088fa8ee7722"},
+    {url = "https://files.pythonhosted.org/packages/53/0c/8897fc309498b48fc60552c714264e91fda10c44defa9401a5c6288cb198/ruff-0.0.267-py3-none-manylinux_2_17_aarch64.manylinux2014_aarch64.whl", hash = "sha256:bbe104f21a429b77eb5ac276bd5352fd8c0e1fbb580b4c772f77ee8c76825654"},
+    {url = "https://files.pythonhosted.org/packages/53/49/fe3e44b5ebd9456e4e0acf79d9c0a777da59f170b7b95e2438f7e10deb15/ruff-0.0.267-py3-none-musllinux_1_2_aarch64.whl", hash = "sha256:45d61a2b01bdf61581a2ee039503a08aa603dc74a6bbe6fb5d1ce3052f5370e5"},
+    {url = "https://files.pythonhosted.org/packages/54/e3/eaa63e3a5c03613088ca00857ba4cf6e6e0e7463a183633a2083b167d02f/ruff-0.0.267-py3-none-win_amd64.whl", hash = "sha256:d09aecc9f5845586ba90911d815f9772c5a6dcf2e34be58c6017ecb124534ac4"},
+    {url = "https://files.pythonhosted.org/packages/56/8f/0ea8e8023f2005e86d9177a250ac0bda008143e5d38f3c21301d81fc09ac/ruff-0.0.267-py3-none-win32.whl", hash = "sha256:d12ab329474c46b96d962e2bdb92e3ad2144981fe41b89c7770f370646c0101f"},
+    {url = "https://files.pythonhosted.org/packages/5d/ba/5dfcde964c63c37e825889dc706afd8641c5460a01eeb6764b2440d1ba25/ruff-0.0.267-py3-none-manylinux_2_17_s390x.manylinux2014_s390x.whl", hash = "sha256:f731d81cb939e757b0335b0090f18ca2e9ff8bcc8e6a1cf909245958949b6e11"},
+    {url = "https://files.pythonhosted.org/packages/67/85/249e6d52ed6272cdb9785e00bd8f1f7b7ac9ed3285c42300137faabb50ae/ruff-0.0.267-py3-none-win_arm64.whl", hash = "sha256:7df7eb5f8d791566ba97cc0b144981b9c080a5b861abaf4bb35a26c8a77b83e9"},
+    {url = "https://files.pythonhosted.org/packages/6d/7d/1c3a89baa73a7880db0706092b668061c172cda6a7ac510646af54bd746a/ruff-0.0.267-py3-none-macosx_10_9_x86_64.macosx_11_0_arm64.macosx_10_9_universal2.whl", hash = "sha256:67254ae34c38cba109fdc52e4a70887de1f850fb3971e5eeef343db67305d1c1"},
+    {url = "https://files.pythonhosted.org/packages/96/e4/c9a745407e204e755fa39a1819dc602662fef90fd9b00f44aac3b4d67176/ruff-0.0.267-py3-none-manylinux_2_17_ppc64.manylinux2014_ppc64.whl", hash = "sha256:0afca3633c8e2b6c0a48ad0061180b641b3b404d68d7e6736aab301c8024c424"},
+    {url = "https://files.pythonhosted.org/packages/b8/3e/ef28832b87a177b3815c6e1fbe314498359122d671e8d80eca22a933784f/ruff-0.0.267-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.whl", hash = "sha256:20c594eb56c19063ef5a57f89340e64c6550e169d6a29408a45130a8c3068adc"},
+    {url = "https://files.pythonhosted.org/packages/d9/da/ee9b62a02de95d716522095e62e7b2fb94dba13d9943e27400c59813bfb5/ruff-0.0.267.tar.gz", hash = "sha256:632cec7bbaf3c06fcf0a72a1dd029b7d8b7f424ba95a574aaa135f5d20a00af7"},
+    {url = "https://files.pythonhosted.org/packages/f1/7a/08f4803d440ee8fac3f007ca41e1a061fa529833c90b3b8dd37662393bbf/ruff-0.0.267-py3-none-manylinux_2_17_armv7l.manylinux2014_armv7l.whl", hash = "sha256:db33deef2a5e1cf528ca51cc59dd764122a48a19a6c776283b223d147041153f"},
+    {url = "https://files.pythonhosted.org/packages/fa/25/cd00b70d749cff37dc567e7267926211ddfaeb8b4eb05aed43d0decfceea/ruff-0.0.267-py3-none-manylinux_2_17_ppc64le.manylinux2014_ppc64le.whl", hash = "sha256:2972241065b1c911bce3db808837ed10f4f6f8a8e15520a4242d291083605ab6"},
+    {url = "https://files.pythonhosted.org/packages/fb/09/6db9f4e8f5dbbe82a72abf2b89cc2bd5033ebee9767187428061e93b4e17/ruff-0.0.267-py3-none-macosx_10_7_x86_64.whl", hash = "sha256:4adbbbe314d8fcc539a245065bad89446a3cef2e0c9cf70bf7bb9ed6fe31856d"},
 ]
 "scalene 1.5.19" = [
     {url = "https://files.pythonhosted.org/packages/11/19/c973ecc43b18076df6c7efff7bec280d02d48d8245f46d94b7e90cf306f2/scalene-1.5.19-cp39-cp39-win_amd64.whl", hash = "sha256:d1fd5d83f3c022ddc46049f29823351b8dbdb8590f5803358fa6034784601f24"},
     {url = "https://files.pythonhosted.org/packages/19/54/d89426ab970f1cb3850b0374967ae22d831d0091efeb2c1d8e8d02ac2a19/scalene-1.5.19-cp39-cp39-macosx_11_7_universal2.whl", hash = "sha256:6c08f3bc0b6355db3c34f0e9aea1b291e64675bb832e19758ee751918787cac0"},
     {url = "https://files.pythonhosted.org/packages/49/11/5a2fa4567eee217609e0a627534f5fb60d0c1f768b43a93145a2ea24e39b/scalene-1.5.19-cp38-cp38-manylinux_2_24_x86_64.whl", hash = "sha256:f67f39321548c06de440319bdd70c41c14b6c50d4748226a101402995677cade"},
     {url = "https://files.pythonhosted.org/packages/5e/3c/b1f159a11f0949f3f27b18af1cc68ee301088a7337efc7d961684bdd3f46/scalene-1.5.19-cp37-cp37m-macosx_10_15_universal2.whl", hash = "sha256:58fb40d031081a55e813f292b2d85b64d7558a372832d8e456f7fe2113adf182"},
     {url = "https://files.pythonhosted.org/packages/65/c3/ebaf00eef807b8da6c5b0c4eb6627f0a67538a25ac7e3858347e15c55d22/scalene-1.5.19-cp38-cp38-win_amd64.whl", hash = "sha256:7a1d452ad4d32cf8adb8b86cae4e5b9c7bff866fff1c43618f9ad114b9ecac32"},
```

### Comparing `xklb-1.26.29/readme.py` & `xklb-1.26.30/readme.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/.github/ISSUE_TEMPLATE/bug_report.md` & `xklb-1.26.30/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/.github/ISSUE_TEMPLATE/feature_request.md` & `xklb-1.26.30/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/.github/workflows/push.yaml` & `xklb-1.26.30/.github/workflows/push.yaml`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/sql/transfer.sql` & `xklb-1.26.30/sql/transfer.sql`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/av.py` & `xklb-1.26.30/xklb/av.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/books.py` & `xklb-1.26.30/xklb/books.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/consts.py` & `xklb-1.26.30/xklb/consts.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/db.py` & `xklb-1.26.30/xklb/db.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/dl_config.py` & `xklb-1.26.30/xklb/dl_config.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/dl_extract.py` & `xklb-1.26.30/xklb/dl_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/fs_extract.py` & `xklb-1.26.30/xklb/fs_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/gui.py` & `xklb-1.26.30/xklb/gui.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/hn_extract.py` & `xklb-1.26.30/xklb/hn_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/lb.py` & `xklb-1.26.30/xklb/lb.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/play_actions.py` & `xklb-1.26.30/xklb/play_actions.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/playback.py` & `xklb-1.26.30/xklb/playback.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/player.py` & `xklb-1.26.30/xklb/player.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/praw_extract.py` & `xklb-1.26.30/xklb/praw_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/stats.py` & `xklb-1.26.30/xklb/stats.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/subtitle.py` & `xklb-1.26.30/xklb/subtitle.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/tabs_actions.py` & `xklb-1.26.30/xklb/tabs_actions.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/tabs_extract.py` & `xklb-1.26.30/xklb/tabs_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/tube_backend.py` & `xklb-1.26.30/xklb/tube_backend.py`

 * *Files 1% similar despite different names*

```diff
@@ -463,14 +463,15 @@
     if Path(info["local_path"]).exists():
         fs_args = argparse.Namespace(
             profile=args.profile,
             scan_subtitles=args.profile == DBType.video,
             delete_unplayable=False,
             ocr=False,
             speech_recognition=False,
+            check_corrupt=False,
         )
         fs_tags = utils.dict_filter_bool(fs_extract.extract_metadata(fs_args, info["local_path"]), keep_0=False) or {}
         fs_extract.clean_up_temp_dirs()
     else:
         fs_tags = {}
 
     tube_entry = consolidate(info) or {}
```

### Comparing `xklb-1.26.29/xklb/tube_extract.py` & `xklb-1.26.30/xklb/tube_extract.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/utils.py` & `xklb-1.26.30/xklb/utils.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/__init__.py` & `xklb-1.26.30/xklb/scripts/__init__.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/bigdirs.py` & `xklb-1.26.30/xklb/scripts/bigdirs.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/christen.py` & `xklb-1.26.30/xklb/scripts/christen.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/copy_play_counts.py` & `xklb-1.26.30/xklb/scripts/copy_play_counts.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/dedupe.py` & `xklb-1.26.30/xklb/scripts/dedupe.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/merge_dbs.py` & `xklb-1.26.30/xklb/scripts/merge_dbs.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/merge_online_local.py` & `xklb-1.26.30/xklb/scripts/merge_online_local.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/move_list.py` & `xklb-1.26.30/xklb/scripts/move_list.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/optimize_db.py` & `xklb-1.26.30/xklb/scripts/optimize_db.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/redownload.py` & `xklb-1.26.30/xklb/scripts/redownload.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/relmv.py` & `xklb-1.26.30/xklb/scripts/relmv.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/scatter.py` & `xklb-1.26.30/xklb/scripts/scatter.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/streaming_tab_loader.py` & `xklb-1.26.30/xklb/scripts/streaming_tab_loader.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/mining/data.py` & `xklb-1.26.30/xklb/scripts/mining/data.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/mining/extract_links.py` & `xklb-1.26.30/xklb/scripts/mining/extract_links.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/mining/nouns.py` & `xklb-1.26.30/xklb/scripts/mining/nouns.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/mining/pushshift.py` & `xklb-1.26.30/xklb/scripts/mining/pushshift.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/xklb/scripts/mining/reddit_selftext.py` & `xklb-1.26.30/xklb/scripts/mining/reddit_selftext.py`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/assets/kotobago.png` & `xklb-1.26.30/assets/kotobago.png`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/.gitignore` & `xklb-1.26.30/.gitignore`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/LICENSE` & `xklb-1.26.30/LICENSE`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/README.md` & `xklb-1.26.30/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
     pip install xklb
 
 ## Examples
 
 <details><summary>List all subcommands</summary>
 
     $ library
-    xk media library subcommands (v1.26.029)
+    xk media library subcommands (v1.26.030)
 
     local media:
       lb fsadd                 Create a local media database; Add folders
       lb fsupdate              Refresh database: add new files, mark deleted
 
       lb listen                Listen to local and online media
       lb watch                 Watch local and online media
```

### Comparing `xklb-1.26.29/pyproject.toml` & `xklb-1.26.30/pyproject.toml`

 * *Files identical despite different names*

### Comparing `xklb-1.26.29/PKG-INFO` & `xklb-1.26.30/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xklb
-Version: 1.26.29
+Version: 1.26.30
 Summary: xk library
 Project-URL: documentation, https://github.com/chapmanjacobd/library/wiki/Usage
 Project-URL: homepage, https://github.com/chapmanjacobd/library/
 Project-URL: repository, https://github.com/chapmanjacobd/library/
 Author-email: Jacob Chapman <7908073+chapmanjacobd@users.noreply.github.com>
 License: BSD 3-Clause No Nuclear License
         
@@ -99,15 +99,15 @@
     pip install xklb
 
 ## Examples
 
 <details><summary>List all subcommands</summary>
 
     $ library
-    xk media library subcommands (v1.26.029)
+    xk media library subcommands (v1.26.030)
 
     local media:
       lb fsadd                 Create a local media database; Add folders
       lb fsupdate              Refresh database: add new files, mark deleted
 
       lb listen                Listen to local and online media
       lb watch                 Watch local and online media
```

