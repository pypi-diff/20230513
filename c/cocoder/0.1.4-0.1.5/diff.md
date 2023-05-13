# Comparing `tmp/cocoder-0.1.4.tar.gz` & `tmp/cocoder-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cocoder-0.1.4.tar", last modified: Sat May 13 01:54:41 2023, max compression
+gzip compressed data, was "cocoder-0.1.5.tar", last modified: Sat May 13 17:14:41 2023, max compression
```

## Comparing `cocoder-0.1.4.tar` & `cocoder-0.1.5.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.598137 cocoder-0.1.4/
--rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.4/LICENSE
--rw-rw-rw-   0        0        0     7271 2023-05-13 01:54:41.596639 cocoder-0.1.4/PKG-INFO
--rw-rw-rw-   0        0        0     6374 2023-05-13 01:53:39.000000 cocoder-0.1.4/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.547228 cocoder-0.1.4/cocoder/
--rw-rw-rw-   0        0        0      504 2023-05-13 01:54:09.000000 cocoder-0.1.4/cocoder/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.574656 cocoder-0.1.4/cocoder/chatbase/
--rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.4/cocoder/chatbase/__init__.py
--rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.4/cocoder/chatbase/bard_receiver.py
--rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.4/cocoder/chatbase/openai_receiver.py
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.584956 cocoder-0.1.4/cocoder/ipython/
--rw-rw-rw-   0        0        0      583 2023-05-13 01:54:03.000000 cocoder-0.1.4/cocoder/ipython/__init__.py
--rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.4/cocoder/ipython/core.py
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.594640 cocoder-0.1.4/cocoder/python/
--rw-rw-rw-   0        0        0      487 2023-05-13 01:54:06.000000 cocoder-0.1.4/cocoder/python/__init__.py
--rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.4/cocoder/python/core.py
-drwxrwxrwx   0        0        0        0 2023-05-13 01:54:41.567654 cocoder-0.1.4/cocoder.egg-info/
--rw-rw-rw-   0        0        0     7271 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      435 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       15 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-13 01:54:41.000000 cocoder-0.1.4/cocoder.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 01:54:41.598137 cocoder-0.1.4/setup.cfg
--rw-rw-rw-   0        0        0     1775 2023-05-13 01:54:00.000000 cocoder-0.1.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.499531 cocoder-0.1.5/
+-rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.5/LICENSE
+-rw-rw-rw-   0        0        0     8313 2023-05-13 17:14:41.498523 cocoder-0.1.5/PKG-INFO
+-rw-rw-rw-   0        0        0     7416 2023-05-13 17:13:03.000000 cocoder-0.1.5/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.450405 cocoder-0.1.5/cocoder/
+-rw-rw-rw-   0        0        0      558 2023-05-13 17:14:28.000000 cocoder-0.1.5/cocoder/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.486558 cocoder-0.1.5/cocoder/chatbase/
+-rw-rw-rw-   0        0        0       52 2023-05-13 07:07:24.000000 cocoder-0.1.5/cocoder/chatbase/__init__.py
+-rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.5/cocoder/chatbase/bard_receiver.py
+-rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.5/cocoder/chatbase/openai_receiver.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.491829 cocoder-0.1.5/cocoder/ipython/
+-rw-rw-rw-   0        0        0      583 2023-05-13 17:14:20.000000 cocoder-0.1.5/cocoder/ipython/__init__.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.5/cocoder/ipython/core.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.496307 cocoder-0.1.5/cocoder/python/
+-rw-rw-rw-   0        0        0      487 2023-05-13 17:13:22.000000 cocoder-0.1.5/cocoder/python/__init__.py
+-rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.5/cocoder/python/core.py
+drwxrwxrwx   0        0        0        0 2023-05-13 17:14:41.480179 cocoder-0.1.5/cocoder.egg-info/
+-rw-rw-rw-   0        0        0     8313 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      435 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       15 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 17:14:41.000000 cocoder-0.1.5/cocoder.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 17:14:41.499531 cocoder-0.1.5/setup.cfg
+-rw-rw-rw-   0        0        0     1775 2023-05-13 17:14:25.000000 cocoder-0.1.5/setup.py
```

### Comparing `cocoder-0.1.4/LICENSE` & `cocoder-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.4/PKG-INFO` & `cocoder-0.1.5/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -1,46 +1,29 @@
-Metadata-Version: 2.1
-Name: cocoder
-Version: 0.1.4
-Home-page: https://github.com/dsdanielpark/Co-Coder
-Author: daniel park
-Author-email: parkminwoo1991@gmail.com
-Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
-Classifier: Development Status :: 2 - Pre-Alpha
-Classifier: Intended Audience :: Science/Research
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
-Requires-Python: >=3.6
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-Development Status :: 3 - Alpha <br>
-*Copyright (c) MinWoo Park 2023*
+<p align="center">
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="./assets/cocoder_main2.jpg"></a>
+</p>
 
-# Co-Coder
+<h3 align="center"> Your AI coding mate, Co-Coder. </h3>
 
-<p align="left">
-<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-blue"></a>
-<a href="https://pypi.org/project/bardapi/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<p align="center">
+<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-black"></a>
 <!-- <a href="https://pepy.tech/project/bardapi"><img alt="Downloads" src="https://pepy.tech/badge/bardapi"></a> -->
-<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=blue"></a>
-<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
-<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a>
-<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-Coder&edge_flat=false"/></a>
+<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=black"></a>
+<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-black.svg"></a>
+<!-- <a href="https://pypi.org/project/cocoder/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a> -->
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false"/></a>
 </p>
 
-![](./assets/cocoder.gif)
+Co-Coder is a Python package that streamlines error debugging from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/) by providing hints, example code, and relevant Stack Overflow links, all by simply importing it and setting the environment variable.
+
+![](./assets/cocoder_230513.gif)
 
-This package is compatible with both Python and iPython. It enhances traceback error messages by appending hints and example codes related to the error. Prompt engineering allows you to get the answers you need quickly. With a one-time setup, you can receive debugging hints for multiple errors, saving time you would have spent searching on [StackOverflow](https://stackoverflow.com/) or Googling.
+The Python package Co-Coder shows information about errors from  [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/). Right below the tracebacked error, you will receive information about the error, debugging hints, and example code. Also, you can use it by modifying the prompt appropriately. Co-Coder helps you automatically get information about errors without Googling or Searching StackOverflow. If you use OpenAI's chatGPT model, it also returns links to Stack Overflow related to the error. 
+The Co-Coder package is executed by simply importing Co-Coder at Python or IPython. Just setting the proper environment variable once.
 
 <br>
 
 
 ## Install 
 The latest stable release (and required dependencies) can be installed from PyPI:
 ```
@@ -70,15 +53,15 @@
 - F12 for console
 - Session: Application → Cookies → Copy the value of  __Secure-1PSID cookie.
 
 <br>
 
 # Ipython
 
-### With Open AI chat GPT 
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English 
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/view?usp=share_link)
     ```python
     import cocoder.ipython
     import os
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
@@ -86,18 +69,18 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 
-### With Google Bard
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
-    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/view?usp=sharing)
+    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/view?usp=sharing)
 
     ```python
     import cocoder.ipython
     import os
     os.environ['_BARD_API_KEY'] = 'xxxxxxxxxxx'
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
@@ -125,30 +108,30 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 # Python
-### With Open AI chat GPT
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English <br>
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/view?usp=sharing)
 
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
     os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-turbo" 
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     sys.excepthook = ExceptPyCocoder.__call__
     print(1/0)
     ```
 
-### With Google Bard 
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/view?usp=sharing)
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_BARD_API_KEY'] = 'xxxxxxx'
@@ -160,23 +143,28 @@
     ```
 
 
 
 <br>
 
 ## Scripts
-In the BardAPI scripts [folder](./scripts/), I have released a script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and [Google-Bard](./scripts/google_api.ipynb). I hope they will help more developers.
+In the BardAPI scripts [folder](https://github.com/dsdanielpark/BARD_API/tree/main/scripts), I have released a script to help you compare [OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/google_api.ipynb). I hope they will help more developers.
 
 ## License 
-CoCoder: MIT <br>
+- CoCoder: MIT <br>
+
 Licenses apply the each [dependencies package](https://choosealicense.com/licenses/), and the created posts follow [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/).
 
 ## Bugs and Issues
 Sincerely grateful for any reports on new features or bugs. Your valuable feedback on the code is highly appreciated.
 
 ## Contacts
-:envelope: Core maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
-:envelope: E-mail: parkminwoo1991@gmail.com <br>
+- Maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
+- E-mail: parkminwoo1991@gmail.com <br>
 
 ## Reference 
 [1] https://github.com/dsdanielpark/BARD_API <br>
-[2] https://github.com/dsdanielpark/ExceptNotifier
+[2] https://github.com/dsdanielpark/ExceptNotifier <br><br>
+
+Development Status :: 3 - Alpha <br>
+*Copyright (c) MinWoo Park 2023*
+
```

#### html2text {}

```diff
@@ -1,90 +1,92 @@
-Metadata-Version: 2.1 Name: cocoder Version: 0.1.4 Home-page: https://
-github.com/dsdanielpark/Co-Coder Author: daniel park Author-email:
-parkminwoo1991@gmail.com Keywords: Python Debuger,Python AI Debug,Realtime
-Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
-Classifier: Development Status :: 2 - Pre-Alpha Classifier: Intended Audience
-:: Science/Research Classifier: Natural Language :: English Classifier:
-Programming Language :: Python Classifier: Programming Language :: Python ::
-3.6 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
-Language :: Python :: 3.8 Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.6 Classifier: Topic ::
-Scientific/Engineering :: Artificial Intelligence Requires-Python: >=3.6
-Description-Content-Type: text/markdown License-File: LICENSE Development
-Status :: 3 - Alpha
-*Copyright (c) MinWoo Park 2023* # Co-Coder
-[PyPI package] [PyPI]  [commit update] [Code_style:_black] [https://
-www.buymeacoffee.com/assets/img/custom_images/orange_img.png] [https://
-hits.seeyoufarm.com/api/count/incr/
-badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-
-Coder&edge_flat=false]
-![](./assets/cocoder.gif) This package is compatible with both Python and
-iPython. It enhances traceback error messages by appending hints and example
-codes related to the error. Prompt engineering allows you to get the answers
-you need quickly. With a one-time setup, you can receive debugging hints for
-multiple errors, saving time you would have spent searching on [StackOverflow]
-(https://stackoverflow.com/) or Googling.
+                         [./assets/cocoder_main2.jpg]
+                   **** Your AI coding mate, Co-Coder. ****
+        [PyPI package]  [commit update] [Code_style:_black]  [https://
+                      hits.seeyoufarm.com/api/count/incr/
+          badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
+Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false]
+Co-Coder is a Python package that streamlines error debugging from [Open AI
+chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://
+bard.google.com/) by providing hints, example code, and relevant Stack Overflow
+links, all by simply importing it and setting the environment variable. ![](./
+assets/cocoder_230513.gif) The Python package Co-Coder shows information about
+errors from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google
+Bard](https://bard.google.com/). Right below the tracebacked error, you will
+receive information about the error, debugging hints, and example code. Also,
+you can use it by modifying the prompt appropriately. Co-Coder helps you
+automatically get information about errors without Googling or Searching
+StackOverflow. If you use OpenAI's chatGPT model, it also returns links to
+Stack Overflow related to the error. The Co-Coder package is executed by simply
+importing Co-Coder at Python or IPython. Just setting the proper environment
+variable once.
 ## Install The latest stable release (and required dependencies) can be
 installed from PyPI: ``` pip install cocoder ``` You may instead want to use
 the development version from Github: ``` pip install git+https://github.com/
 dsdanielpark/Co-Coder.git ```
 ## Tutorial Tutorials for all features can be found in this [folder](./
 tutorials/). Examples have been prepared for all possible cases.
 ## Authentication ### Open AI Visit [Open AI API](https://platform.openai.com/
 docs/introduction) for more information. - Visit https://platform.openai.com/
 account/api-keys - View API keys â + Create new secret key ### Google Bard
 See the Python package [BardAPI](https://github.com/dsdanielpark/bardapi) for
 more information. - Visit https://bard.google.com/ - F12 for console - Session:
 Application â Cookies â Copy the value of __Secure-1PSID cookie.
-# Ipython ### With Open AI chat GPT - Supported Language: English *English*
+# Ipython ### With [Open AI chat GPT](https://openai.com/blog/chatgpt) -
+Supported Language: English *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/
 view?usp=share_link) ```python import cocoder.ipython import os os.environ
 ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-
 turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in
-here." print(1/0) ``` ### With Google Bard - Supported Language: Korean,
-English, Japanese *English*
+here." print(1/0) ``` ### With [Google Bard](https://bard.google.com/) -
+Supported Language: Korean, English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
-(https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/
+(https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' # os.environ['_PROMPT_COMMAND'] = "You can
 make customized prompt in here." print(1/0) ``` *Korean*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1yZJKjkV3zQI-sJkS48PDpePqxoMMfYRA/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='ko' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
 (1/0) ``` *Japanese*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/178mt8_kkBN4-z408No_4qW8XfCWSL-wh/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='jp' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
-(1/0) ``` # Python ### With Open AI chat GPT - Supported Language: English
+(1/0) ``` # Python ### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
+- Supported Language: English
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] =
 "gpt-3.5-turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized
 prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/0) ``` ###
-With Google Bard - Supported Language: Korean, English, Japanese *English*
+With [Google Bard](https://bard.google.com/) - Supported Language: Korean,
+English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_BARD_API_KEY'] = 'xxxxxxx' # os.environ
 ["_BARD_ADVICE_LANG"]='ko','jp' # os.environ['_PROMPT_COMMAND']="You can make
 customized prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/
 0) ```
-## Scripts In the BardAPI scripts [folder](./scripts/), I have released a
-script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and
-[Google-Bard](./scripts/google_api.ipynb). I hope they will help more
-developers. ## License CoCoder: MIT
+## Scripts In the BardAPI scripts [folder](https://github.com/dsdanielpark/
+BARD_API/tree/main/scripts), I have released a script to help you compare
+[OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/
+openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/
+blob/main/scripts/google_api.ipynb). I hope they will help more developers. ##
+License - CoCoder: MIT
 Licenses apply the each [dependencies package](https://choosealicense.com/
 licenses/), and the created posts follow [CC BY-NC-SA](https://
 creativecommons.org/licenses/by-nc-sa/4.0/). ## Bugs and Issues Sincerely
 grateful for any reports on new features or bugs. Your valuable feedback on the
-code is highly appreciated. ## Contacts :envelope: Core maintainer: [Daniel
-Park, South Korea](https://github.com/DSDanielPark)
-:envelope: E-mail: parkminwoo1991@gmail.com
+code is highly appreciated. ## Contacts - Maintainer: [Daniel Park, South
+Korea](https://github.com/DSDanielPark)
+- E-mail: parkminwoo1991@gmail.com
 ## Reference [1] https://github.com/dsdanielpark/BARD_API
 [2] https://github.com/dsdanielpark/ExceptNotifier
+
+Development Status :: 3 - Alpha
+*Copyright (c) MinWoo Park 2023*
```

### Comparing `cocoder-0.1.4/README.md` & `cocoder-0.1.5/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,25 +1,50 @@
-Development Status :: 3 - Alpha <br>
-*Copyright (c) MinWoo Park 2023*
+Metadata-Version: 2.1
+Name: cocoder
+Version: 0.1.5
+Home-page: https://github.com/dsdanielpark/Co-Coder
+Author: daniel park
+Author-email: parkminwoo1991@gmail.com
+Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
+Classifier: Development Status :: 2 - Pre-Alpha
+Classifier: Intended Audience :: Science/Research
+Classifier: Natural Language :: English
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3.6
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3.6
+Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
+Requires-Python: >=3.6
+Description-Content-Type: text/markdown
+License-File: LICENSE
 
-# Co-Coder
+<p align="center">
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="./assets/cocoder_main2.jpg"></a>
+</p>
 
-<p align="left">
-<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-blue"></a>
-<a href="https://pypi.org/project/bardapi/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<h3 align="center"> Your AI coding mate, Co-Coder. </h3>
+
+<p align="center">
+<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-black"></a>
 <!-- <a href="https://pepy.tech/project/bardapi"><img alt="Downloads" src="https://pepy.tech/badge/bardapi"></a> -->
-<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=blue"></a>
-<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
-<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a>
-<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-Coder&edge_flat=false"/></a>
+<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=black"></a>
+<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-black.svg"></a>
+<!-- <a href="https://pypi.org/project/cocoder/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a> -->
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false"/></a>
 </p>
 
-![](./assets/cocoder.gif)
+Co-Coder is a Python package that streamlines error debugging from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/) by providing hints, example code, and relevant Stack Overflow links, all by simply importing it and setting the environment variable.
+
+![](./assets/cocoder_230513.gif)
 
-This package is compatible with both Python and iPython. It enhances traceback error messages by appending hints and example codes related to the error. Prompt engineering allows you to get the answers you need quickly. With a one-time setup, you can receive debugging hints for multiple errors, saving time you would have spent searching on [StackOverflow](https://stackoverflow.com/) or Googling.
+The Python package Co-Coder shows information about errors from  [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/). Right below the tracebacked error, you will receive information about the error, debugging hints, and example code. Also, you can use it by modifying the prompt appropriately. Co-Coder helps you automatically get information about errors without Googling or Searching StackOverflow. If you use OpenAI's chatGPT model, it also returns links to Stack Overflow related to the error. 
+The Co-Coder package is executed by simply importing Co-Coder at Python or IPython. Just setting the proper environment variable once.
 
 <br>
 
 
 ## Install 
 The latest stable release (and required dependencies) can be installed from PyPI:
 ```
@@ -49,15 +74,15 @@
 - F12 for console
 - Session: Application → Cookies → Copy the value of  __Secure-1PSID cookie.
 
 <br>
 
 # Ipython
 
-### With Open AI chat GPT 
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English 
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/view?usp=share_link)
     ```python
     import cocoder.ipython
     import os
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
@@ -65,18 +90,18 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 
-### With Google Bard
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
-    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/view?usp=sharing)
+    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/view?usp=sharing)
 
     ```python
     import cocoder.ipython
     import os
     os.environ['_BARD_API_KEY'] = 'xxxxxxxxxxx'
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
@@ -104,30 +129,30 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 # Python
-### With Open AI chat GPT
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English <br>
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/view?usp=sharing)
 
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
     os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-turbo" 
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     sys.excepthook = ExceptPyCocoder.__call__
     print(1/0)
     ```
 
-### With Google Bard 
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/view?usp=sharing)
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_BARD_API_KEY'] = 'xxxxxxx'
@@ -139,23 +164,28 @@
     ```
 
 
 
 <br>
 
 ## Scripts
-In the BardAPI scripts [folder](./scripts/), I have released a script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and [Google-Bard](./scripts/google_api.ipynb). I hope they will help more developers.
+In the BardAPI scripts [folder](https://github.com/dsdanielpark/BARD_API/tree/main/scripts), I have released a script to help you compare [OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/google_api.ipynb). I hope they will help more developers.
 
 ## License 
-CoCoder: MIT <br>
+- CoCoder: MIT <br>
+
 Licenses apply the each [dependencies package](https://choosealicense.com/licenses/), and the created posts follow [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/).
 
 ## Bugs and Issues
 Sincerely grateful for any reports on new features or bugs. Your valuable feedback on the code is highly appreciated.
 
 ## Contacts
-:envelope: Core maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
-:envelope: E-mail: parkminwoo1991@gmail.com <br>
+- Maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
+- E-mail: parkminwoo1991@gmail.com <br>
 
 ## Reference 
 [1] https://github.com/dsdanielpark/BARD_API <br>
-[2] https://github.com/dsdanielpark/ExceptNotifier
+[2] https://github.com/dsdanielpark/ExceptNotifier <br><br>
+
+Development Status :: 3 - Alpha <br>
+*Copyright (c) MinWoo Park 2023*
+
```

#### html2text {}

```diff
@@ -1,78 +1,104 @@
-Development Status :: 3 - Alpha
-*Copyright (c) MinWoo Park 2023* # Co-Coder
-[PyPI package] [PyPI]  [commit update] [Code_style:_black] [https://
-www.buymeacoffee.com/assets/img/custom_images/orange_img.png] [https://
-hits.seeyoufarm.com/api/count/incr/
-badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-
-Coder&edge_flat=false]
-![](./assets/cocoder.gif) This package is compatible with both Python and
-iPython. It enhances traceback error messages by appending hints and example
-codes related to the error. Prompt engineering allows you to get the answers
-you need quickly. With a one-time setup, you can receive debugging hints for
-multiple errors, saving time you would have spent searching on [StackOverflow]
-(https://stackoverflow.com/) or Googling.
+Metadata-Version: 2.1 Name: cocoder Version: 0.1.5 Home-page: https://
+github.com/dsdanielpark/Co-Coder Author: daniel park Author-email:
+parkminwoo1991@gmail.com Keywords: Python Debuger,Python AI Debug,Realtime
+Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
+Classifier: Development Status :: 2 - Pre-Alpha Classifier: Intended Audience
+:: Science/Research Classifier: Natural Language :: English Classifier:
+Programming Language :: Python Classifier: Programming Language :: Python ::
+3.6 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
+Language :: Python :: 3.8 Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3.6 Classifier: Topic ::
+Scientific/Engineering :: Artificial Intelligence Requires-Python: >=3.6
+Description-Content-Type: text/markdown License-File: LICENSE
+                         [./assets/cocoder_main2.jpg]
+                   **** Your AI coding mate, Co-Coder. ****
+        [PyPI package]  [commit update] [Code_style:_black]  [https://
+                      hits.seeyoufarm.com/api/count/incr/
+          badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
+Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false]
+Co-Coder is a Python package that streamlines error debugging from [Open AI
+chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://
+bard.google.com/) by providing hints, example code, and relevant Stack Overflow
+links, all by simply importing it and setting the environment variable. ![](./
+assets/cocoder_230513.gif) The Python package Co-Coder shows information about
+errors from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google
+Bard](https://bard.google.com/). Right below the tracebacked error, you will
+receive information about the error, debugging hints, and example code. Also,
+you can use it by modifying the prompt appropriately. Co-Coder helps you
+automatically get information about errors without Googling or Searching
+StackOverflow. If you use OpenAI's chatGPT model, it also returns links to
+Stack Overflow related to the error. The Co-Coder package is executed by simply
+importing Co-Coder at Python or IPython. Just setting the proper environment
+variable once.
 ## Install The latest stable release (and required dependencies) can be
 installed from PyPI: ``` pip install cocoder ``` You may instead want to use
 the development version from Github: ``` pip install git+https://github.com/
 dsdanielpark/Co-Coder.git ```
 ## Tutorial Tutorials for all features can be found in this [folder](./
 tutorials/). Examples have been prepared for all possible cases.
 ## Authentication ### Open AI Visit [Open AI API](https://platform.openai.com/
 docs/introduction) for more information. - Visit https://platform.openai.com/
 account/api-keys - View API keys â + Create new secret key ### Google Bard
 See the Python package [BardAPI](https://github.com/dsdanielpark/bardapi) for
 more information. - Visit https://bard.google.com/ - F12 for console - Session:
 Application â Cookies â Copy the value of __Secure-1PSID cookie.
-# Ipython ### With Open AI chat GPT - Supported Language: English *English*
+# Ipython ### With [Open AI chat GPT](https://openai.com/blog/chatgpt) -
+Supported Language: English *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/
 view?usp=share_link) ```python import cocoder.ipython import os os.environ
 ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-
 turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in
-here." print(1/0) ``` ### With Google Bard - Supported Language: Korean,
-English, Japanese *English*
+here." print(1/0) ``` ### With [Google Bard](https://bard.google.com/) -
+Supported Language: Korean, English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
-(https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/
+(https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' # os.environ['_PROMPT_COMMAND'] = "You can
 make customized prompt in here." print(1/0) ``` *Korean*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1yZJKjkV3zQI-sJkS48PDpePqxoMMfYRA/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='ko' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
 (1/0) ``` *Japanese*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/178mt8_kkBN4-z408No_4qW8XfCWSL-wh/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='jp' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
-(1/0) ``` # Python ### With Open AI chat GPT - Supported Language: English
+(1/0) ``` # Python ### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
+- Supported Language: English
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] =
 "gpt-3.5-turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized
 prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/0) ``` ###
-With Google Bard - Supported Language: Korean, English, Japanese *English*
+With [Google Bard](https://bard.google.com/) - Supported Language: Korean,
+English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_BARD_API_KEY'] = 'xxxxxxx' # os.environ
 ["_BARD_ADVICE_LANG"]='ko','jp' # os.environ['_PROMPT_COMMAND']="You can make
 customized prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/
 0) ```
-## Scripts In the BardAPI scripts [folder](./scripts/), I have released a
-script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and
-[Google-Bard](./scripts/google_api.ipynb). I hope they will help more
-developers. ## License CoCoder: MIT
+## Scripts In the BardAPI scripts [folder](https://github.com/dsdanielpark/
+BARD_API/tree/main/scripts), I have released a script to help you compare
+[OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/
+openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/
+blob/main/scripts/google_api.ipynb). I hope they will help more developers. ##
+License - CoCoder: MIT
 Licenses apply the each [dependencies package](https://choosealicense.com/
 licenses/), and the created posts follow [CC BY-NC-SA](https://
 creativecommons.org/licenses/by-nc-sa/4.0/). ## Bugs and Issues Sincerely
 grateful for any reports on new features or bugs. Your valuable feedback on the
-code is highly appreciated. ## Contacts :envelope: Core maintainer: [Daniel
-Park, South Korea](https://github.com/DSDanielPark)
-:envelope: E-mail: parkminwoo1991@gmail.com
+code is highly appreciated. ## Contacts - Maintainer: [Daniel Park, South
+Korea](https://github.com/DSDanielPark)
+- E-mail: parkminwoo1991@gmail.com
 ## Reference [1] https://github.com/dsdanielpark/BARD_API
 [2] https://github.com/dsdanielpark/ExceptNotifier
+
+Development Status :: 3 - Alpha
+*Copyright (c) MinWoo Park 2023*
```

### Comparing `cocoder-0.1.4/cocoder/chatbase/bard_receiver.py` & `cocoder-0.1.5/cocoder/chatbase/bard_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.4/cocoder/chatbase/openai_receiver.py` & `cocoder-0.1.5/cocoder/chatbase/openai_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.4/cocoder/ipython/__init__.py` & `cocoder-0.1.5/cocoder/ipython/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -6,10 +6,10 @@
 from cocoder.chatbase.openai_receiver import get_resp_openai_advice
 
 try:
     get_ipython().set_custom_exc((Exception,), ExceptIpyCocoder)
 except:
     pass
 
-__version__ = "0.1.4"
+__version__ = "0.1.5"
 __author__ = "daniel park <parkminwoo1991@gmail.com>"
 __all__ = ["ExceptIpyCocoder", "receive_bard_advice", "receive_openai_advice", "get_resp_openai_advice"]
```

### Comparing `cocoder-0.1.4/cocoder/ipython/core.py` & `cocoder-0.1.5/cocoder/ipython/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.4/cocoder/python/core.py` & `cocoder-0.1.5/cocoder/python/core.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.4/cocoder.egg-info/PKG-INFO` & `cocoder-0.1.5/cocoder.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.4
+Version: 0.1.5
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
@@ -15,32 +15,36 @@
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-Development Status :: 3 - Alpha <br>
-*Copyright (c) MinWoo Park 2023*
+<p align="center">
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="./assets/cocoder_main2.jpg"></a>
+</p>
 
-# Co-Coder
+<h3 align="center"> Your AI coding mate, Co-Coder. </h3>
 
-<p align="left">
-<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-blue"></a>
-<a href="https://pypi.org/project/bardapi/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<p align="center">
+<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-CoCoder-black"></a>
 <!-- <a href="https://pepy.tech/project/bardapi"><img alt="Downloads" src="https://pepy.tech/badge/bardapi"></a> -->
-<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=blue"></a>
-<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
-<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a>
-<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-Coder&edge_flat=false"/></a>
+<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Co-Coder?color=black"></a>
+<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-black.svg"></a>
+<!-- <a href="https://pypi.org/project/cocoder/"><img alt="PyPI" src="https://img.shields.io/pypi/v/cocoder"></a>
+<a href="https://www.buymeacoffee.com/parkminwoo"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" height="20px"></a> -->
+<a href="https://github.com/dsdanielpark/Co-Coder"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false"/></a>
 </p>
 
-![](./assets/cocoder.gif)
+Co-Coder is a Python package that streamlines error debugging from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/) by providing hints, example code, and relevant Stack Overflow links, all by simply importing it and setting the environment variable.
 
-This package is compatible with both Python and iPython. It enhances traceback error messages by appending hints and example codes related to the error. Prompt engineering allows you to get the answers you need quickly. With a one-time setup, you can receive debugging hints for multiple errors, saving time you would have spent searching on [StackOverflow](https://stackoverflow.com/) or Googling.
+![](./assets/cocoder_230513.gif)
+
+The Python package Co-Coder shows information about errors from  [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://bard.google.com/). Right below the tracebacked error, you will receive information about the error, debugging hints, and example code. Also, you can use it by modifying the prompt appropriately. Co-Coder helps you automatically get information about errors without Googling or Searching StackOverflow. If you use OpenAI's chatGPT model, it also returns links to Stack Overflow related to the error. 
+The Co-Coder package is executed by simply importing Co-Coder at Python or IPython. Just setting the proper environment variable once.
 
 <br>
 
 
 ## Install 
 The latest stable release (and required dependencies) can be installed from PyPI:
 ```
@@ -70,15 +74,15 @@
 - F12 for console
 - Session: Application → Cookies → Copy the value of  __Secure-1PSID cookie.
 
 <br>
 
 # Ipython
 
-### With Open AI chat GPT 
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English 
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/view?usp=share_link)
     ```python
     import cocoder.ipython
     import os
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
@@ -86,18 +90,18 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 
-### With Google Bard
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
-    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/view?usp=sharing)
+    *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/view?usp=sharing)
 
     ```python
     import cocoder.ipython
     import os
     os.environ['_BARD_API_KEY'] = 'xxxxxxxxxxx'
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
@@ -125,30 +129,30 @@
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     print(1/0)
     ```
 
 
 # Python
-### With Open AI chat GPT
+### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
 - Supported Language: English <br>
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/view?usp=sharing)
 
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx'
     os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-turbo" 
     # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here."
 
     sys.excepthook = ExceptPyCocoder.__call__
     print(1/0)
     ```
 
-### With Google Bard 
+### With [Google Bard](https://bard.google.com/)
 - Supported Language: Korean, English, Japanese
 
     *English* <br> [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/view?usp=sharing)
     ```python
     from cocoder import ExceptPyCocoder
     import os, sys
     os.environ['_BARD_API_KEY'] = 'xxxxxxx'
@@ -160,23 +164,28 @@
     ```
 
 
 
 <br>
 
 ## Scripts
-In the BardAPI scripts [folder](./scripts/), I have released a script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and [Google-Bard](./scripts/google_api.ipynb). I hope they will help more developers.
+In the BardAPI scripts [folder](https://github.com/dsdanielpark/BARD_API/tree/main/scripts), I have released a script to help you compare [OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/google_api.ipynb). I hope they will help more developers.
 
 ## License 
-CoCoder: MIT <br>
+- CoCoder: MIT <br>
+
 Licenses apply the each [dependencies package](https://choosealicense.com/licenses/), and the created posts follow [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/).
 
 ## Bugs and Issues
 Sincerely grateful for any reports on new features or bugs. Your valuable feedback on the code is highly appreciated.
 
 ## Contacts
-:envelope: Core maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
-:envelope: E-mail: parkminwoo1991@gmail.com <br>
+- Maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
+- E-mail: parkminwoo1991@gmail.com <br>
 
 ## Reference 
 [1] https://github.com/dsdanielpark/BARD_API <br>
-[2] https://github.com/dsdanielpark/ExceptNotifier
+[2] https://github.com/dsdanielpark/ExceptNotifier <br><br>
+
+Development Status :: 3 - Alpha <br>
+*Copyright (c) MinWoo Park 2023*
+
```

#### html2text {}

```diff
@@ -1,90 +1,104 @@
-Metadata-Version: 2.1 Name: cocoder Version: 0.1.4 Home-page: https://
+Metadata-Version: 2.1 Name: cocoder Version: 0.1.5 Home-page: https://
 github.com/dsdanielpark/Co-Coder Author: daniel park Author-email:
 parkminwoo1991@gmail.com Keywords: Python Debuger,Python AI Debug,Realtime
 Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha Classifier: Intended Audience
 :: Science/Research Classifier: Natural Language :: English Classifier:
 Programming Language :: Python Classifier: Programming Language :: Python ::
 3.6 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.6 Classifier: Topic ::
 Scientific/Engineering :: Artificial Intelligence Requires-Python: >=3.6
-Description-Content-Type: text/markdown License-File: LICENSE Development
-Status :: 3 - Alpha
-*Copyright (c) MinWoo Park 2023* # Co-Coder
-[PyPI package] [PyPI]  [commit update] [Code_style:_black] [https://
-www.buymeacoffee.com/assets/img/custom_images/orange_img.png] [https://
-hits.seeyoufarm.com/api/count/incr/
-badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
-Coder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Co-
-Coder&edge_flat=false]
-![](./assets/cocoder.gif) This package is compatible with both Python and
-iPython. It enhances traceback error messages by appending hints and example
-codes related to the error. Prompt engineering allows you to get the answers
-you need quickly. With a one-time setup, you can receive debugging hints for
-multiple errors, saving time you would have spent searching on [StackOverflow]
-(https://stackoverflow.com/) or Googling.
+Description-Content-Type: text/markdown License-File: LICENSE
+                         [./assets/cocoder_main2.jpg]
+                   **** Your AI coding mate, Co-Coder. ****
+        [PyPI package]  [commit update] [Code_style:_black]  [https://
+                      hits.seeyoufarm.com/api/count/incr/
+          badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FCo-
+Coder&count_bg=%23000000&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=CoCoder&edge_flat=false]
+Co-Coder is a Python package that streamlines error debugging from [Open AI
+chat GPT](https://openai.com/blog/chatgpt) and [Google Bard](https://
+bard.google.com/) by providing hints, example code, and relevant Stack Overflow
+links, all by simply importing it and setting the environment variable. ![](./
+assets/cocoder_230513.gif) The Python package Co-Coder shows information about
+errors from [Open AI chat GPT](https://openai.com/blog/chatgpt) and [Google
+Bard](https://bard.google.com/). Right below the tracebacked error, you will
+receive information about the error, debugging hints, and example code. Also,
+you can use it by modifying the prompt appropriately. Co-Coder helps you
+automatically get information about errors without Googling or Searching
+StackOverflow. If you use OpenAI's chatGPT model, it also returns links to
+Stack Overflow related to the error. The Co-Coder package is executed by simply
+importing Co-Coder at Python or IPython. Just setting the proper environment
+variable once.
 ## Install The latest stable release (and required dependencies) can be
 installed from PyPI: ``` pip install cocoder ``` You may instead want to use
 the development version from Github: ``` pip install git+https://github.com/
 dsdanielpark/Co-Coder.git ```
 ## Tutorial Tutorials for all features can be found in this [folder](./
 tutorials/). Examples have been prepared for all possible cases.
 ## Authentication ### Open AI Visit [Open AI API](https://platform.openai.com/
 docs/introduction) for more information. - Visit https://platform.openai.com/
 account/api-keys - View API keys â + Create new secret key ### Google Bard
 See the Python package [BardAPI](https://github.com/dsdanielpark/bardapi) for
 more information. - Visit https://bard.google.com/ - F12 for console - Session:
 Application â Cookies â Copy the value of __Secure-1PSID cookie.
-# Ipython ### With Open AI chat GPT - Supported Language: English *English*
+# Ipython ### With [Open AI chat GPT](https://openai.com/blog/chatgpt) -
+Supported Language: English *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1i8PLhWY2YRIUtRV7Llf2dHn4x8RYmCYi/
 view?usp=share_link) ```python import cocoder.ipython import os os.environ
 ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] = "gpt-3.5-
 turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in
-here." print(1/0) ``` ### With Google Bard - Supported Language: Korean,
-English, Japanese *English*
+here." print(1/0) ``` ### With [Google Bard](https://bard.google.com/) -
+Supported Language: Korean, English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
-(https://drive.google.com/file/d/1G0bkZRUXAxbWBBrJoAfLhsTxGIZcHeLq/
+(https://drive.google.com/file/d/1vNrmxhNnfwbEPB2Qr-dkh9yWP4RuhehL/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' # os.environ['_PROMPT_COMMAND'] = "You can
 make customized prompt in here." print(1/0) ``` *Korean*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1yZJKjkV3zQI-sJkS48PDpePqxoMMfYRA/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='ko' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
 (1/0) ``` *Japanese*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/178mt8_kkBN4-z408No_4qW8XfCWSL-wh/
 view?usp=sharing) ```python import cocoder.ipython import os os.environ
 ['_BARD_API_KEY'] = 'xxxxxxxxxxx' os.environ["_BARD_ADVICE_LANG"]='jp' #
 os.environ['_PROMPT_COMMAND'] = "You can make customized prompt in here." print
-(1/0) ``` # Python ### With Open AI chat GPT - Supported Language: English
+(1/0) ``` # Python ### With [Open AI chat GPT](https://openai.com/blog/chatgpt)
+- Supported Language: English
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1zh2tX0Xtq5YqrWgNiJ9nF1RmaJgAvQ8E/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_OPEN_AI_API'] = 'sk-xxxxxxxxxxx' os.environ['_OPEN_AI_MODEL'] =
 "gpt-3.5-turbo" # os.environ['_PROMPT_COMMAND'] = "You can make customized
 prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/0) ``` ###
-With Google Bard - Supported Language: Korean, English, Japanese *English*
+With [Google Bard](https://bard.google.com/) - Supported Language: Korean,
+English, Japanese *English*
 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
 (https://drive.google.com/file/d/1Ax3y7_2PgBsuK_d6z374vvYrmClSp7JX/
 view?usp=sharing) ```python from cocoder import ExceptPyCocoder import os, sys
 os.environ['_BARD_API_KEY'] = 'xxxxxxx' # os.environ
 ["_BARD_ADVICE_LANG"]='ko','jp' # os.environ['_PROMPT_COMMAND']="You can make
 customized prompt in here." sys.excepthook = ExceptPyCocoder.__call__ print(1/
 0) ```
-## Scripts In the BardAPI scripts [folder](./scripts/), I have released a
-script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and
-[Google-Bard](./scripts/google_api.ipynb). I hope they will help more
-developers. ## License CoCoder: MIT
+## Scripts In the BardAPI scripts [folder](https://github.com/dsdanielpark/
+BARD_API/tree/main/scripts), I have released a script to help you compare
+[OpenAI-ChatGPT](https://github.com/dsdanielpark/BARD_API/blob/main/scripts/
+openai_api.ipynb) and [Google-Bard](https://github.com/dsdanielpark/BARD_API/
+blob/main/scripts/google_api.ipynb). I hope they will help more developers. ##
+License - CoCoder: MIT
 Licenses apply the each [dependencies package](https://choosealicense.com/
 licenses/), and the created posts follow [CC BY-NC-SA](https://
 creativecommons.org/licenses/by-nc-sa/4.0/). ## Bugs and Issues Sincerely
 grateful for any reports on new features or bugs. Your valuable feedback on the
-code is highly appreciated. ## Contacts :envelope: Core maintainer: [Daniel
-Park, South Korea](https://github.com/DSDanielPark)
-:envelope: E-mail: parkminwoo1991@gmail.com
+code is highly appreciated. ## Contacts - Maintainer: [Daniel Park, South
+Korea](https://github.com/DSDanielPark)
+- E-mail: parkminwoo1991@gmail.com
 ## Reference [1] https://github.com/dsdanielpark/BARD_API
 [2] https://github.com/dsdanielpark/ExceptNotifier
+
+Development Status :: 3 - Alpha
+*Copyright (c) MinWoo Park 2023*
```

### Comparing `cocoder-0.1.4/setup.py` & `cocoder-0.1.5/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 
 version = get_version()
 
 
 setup(
     name="cocoder",
-    version="0.1.4",
+    version="0.1.5",
     author="daniel park",
     author_email="parkminwoo1991@gmail.com",
     description="",
     long_description=get_long_description(),
     long_description_content_type="text/markdown",
     url="https://github.com/dsdanielpark/Co-Coder",
     packages=find_packages(exclude=[]),
```

