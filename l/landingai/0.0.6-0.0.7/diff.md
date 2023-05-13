# Comparing `tmp/landingai-0.0.6.tar.gz` & `tmp/landingai-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "landingai-0.0.6.tar", max compression
+gzip compressed data, was "landingai-0.0.7.tar", max compression
```

## Comparing `landingai-0.0.6.tar` & `landingai-0.0.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     3987 2023-05-13 03:55:22.057474 landingai-0.0.6/README.md
--rw-r--r--   0        0        0       40 2023-05-11 23:35:20.932651 landingai-0.0.6/landingai/__init__.py
--rw-r--r--   0        0        0     3372 2023-05-12 22:53:01.555726 landingai-0.0.6/landingai/common.py
--rw-r--r--   0        0        0     7385 2023-05-13 03:23:15.112923 landingai-0.0.6/landingai/predict.py
--rw-r--r--   0        0        0     2107 2023-05-12 22:53:01.563372 landingai-0.0.6/landingai/visualize.py
--rw-r--r--   0        0        0     1200 2023-05-13 03:53:53.389155 landingai-0.0.6/pyproject.toml
--rw-r--r--   0        0        0     4889 1970-01-01 00:00:00.000000 landingai-0.0.6/PKG-INFO
+-rw-r--r--   0        0        0     4043 2023-05-13 04:06:14.490952 landingai-0.0.7/README.md
+-rw-r--r--   0        0        0       40 2023-05-11 23:35:20.932651 landingai-0.0.7/landingai/__init__.py
+-rw-r--r--   0        0        0     3372 2023-05-12 22:53:01.555726 landingai-0.0.7/landingai/common.py
+-rw-r--r--   0        0        0     7385 2023-05-13 03:23:15.112923 landingai-0.0.7/landingai/predict.py
+-rw-r--r--   0        0        0     2107 2023-05-12 22:53:01.563372 landingai-0.0.7/landingai/visualize.py
+-rw-r--r--   0        0        0     1200 2023-05-13 04:07:34.540957 landingai-0.0.7/pyproject.toml
+-rw-r--r--   0        0        0     4945 1970-01-01 00:00:00.000000 landingai-0.0.7/PKG-INFO
```

### Comparing `landingai-0.0.6/README.md` & `landingai-0.0.7/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 This repository contains LandingLens development library and running examples showing how to integrate LandingLens on a variety of scenarios. All the examples show different ways to acquire images from multiple sources and techniques to process the results. Jupyter notebooks focus on ease of use while Python apps include more robust and complete examples.
 
 <!-- Generated using https://www.tablesgenerator.com/markdown_tables -->
 | example | description | language |
 |---|---|---|
 | [Company logo identification](https://github.com/landing-ai/landingai-python-v1/blob/main/examples/webcam-collab-notebook/webcam-collab-notebook.ipynb) | This notebook can run directly in Google collab using the web browser camera to detect Landing AI logo | Jupyter Notebook [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/landing-ai/landingai-python-v1/blob/main/examples/webcam-collab-notebook/webcam-collab-notebook.ipynb)|
 | [Door monitoring for home automation](https://github.com/landing-ai/landingai-python-v1/blob/main/examples/rtsp-capture-notebook/rtsp-capture.ipynb) | This notebook uses an object detection model to determine whether a door is open or closed. The notebook can acquire images directly from an RTSP camera | Jupyter Notebook |
-| [Streaming capture service](examples/capture-service/run.py) | This application shows how to do continuous acquisition from an image sensor using RTSP. | Python application |
+| [Streaming capture service](https://github.com/landing-ai/landingai-python-v1/tree/main/examples/capture-service) | This application shows how to do continuous acquisition from an image sensor using RTSP. | Python application |
 
 ## Install the library
 
 ```bash
 pip install landingai
 ```
 
@@ -55,23 +55,23 @@
 
 Here is an example to show you how to run the `rtsp-capture` example locally in a shell environment:
 
 NOTE: it's recommended to create a new Python virtual environment first.
 
 1. Clone the repo to local: `git clone https://github.com/landing-ai/landingai-python-v1.git`
 2. Install the library: `pip install landingai`
-3. Run: `python landingai-python-v1/examples/rtsp-capture/run.py`
+3. Run: `python landingai-python-v1/examples/capture-service/run.py`
 
-## Building the LandingLens library locally (for developers and contributors)
+## Building the LandingLens library locally (for contributors)
 
 Most of the time you won't need to build the library since it is included on this repository and also published to pypi.
 
-But if you want to contribute to the repo, you can follow the below steps:
+But if you want to contribute to the repo, you can follow the below steps.
 
-### Install poetry
+### Prerequisite - Install poetry
 
 > See more from the [official doc](https://python-poetry.org/docs/#installation).
 
 For Linux, macOS, Windows (WSL):
 
 ```
 curl -sSL https://install.python-poetry.org | python3 -
```

### Comparing `landingai-0.0.6/landingai/common.py` & `landingai-0.0.7/landingai/common.py`

 * *Files identical despite different names*

### Comparing `landingai-0.0.6/landingai/predict.py` & `landingai-0.0.7/landingai/predict.py`

 * *Files identical despite different names*

### Comparing `landingai-0.0.6/landingai/visualize.py` & `landingai-0.0.7/landingai/visualize.py`

 * *Files identical despite different names*

### Comparing `landingai-0.0.6/pyproject.toml` & `landingai-0.0.7/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "landingai"
-version = "0.0.6"
+version = "0.0.7"
 description = "Helper library for interacting with Landing AI LandingLens"
 authors = ["Landing AI <dev@landing.ai>"]
 readme = "README.md"
 packages = [{include = "landingai"}]
 
 [tool.poetry.urls]
 "Homepage" = "https://landing.ai"
```

### Comparing `landingai-0.0.6/PKG-INFO` & `landingai-0.0.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: landingai
-Version: 0.0.6
+Version: 0.0.7
 Summary: Helper library for interacting with Landing AI LandingLens
 Author: Landing AI
 Author-email: dev@landing.ai
 Requires-Python: >=3.8
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -29,15 +29,15 @@
 This repository contains LandingLens development library and running examples showing how to integrate LandingLens on a variety of scenarios. All the examples show different ways to acquire images from multiple sources and techniques to process the results. Jupyter notebooks focus on ease of use while Python apps include more robust and complete examples.
 
 <!-- Generated using https://www.tablesgenerator.com/markdown_tables -->
 | example | description | language |
 |---|---|---|
 | [Company logo identification](https://github.com/landing-ai/landingai-python-v1/blob/main/examples/webcam-collab-notebook/webcam-collab-notebook.ipynb) | This notebook can run directly in Google collab using the web browser camera to detect Landing AI logo | Jupyter Notebook [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/landing-ai/landingai-python-v1/blob/main/examples/webcam-collab-notebook/webcam-collab-notebook.ipynb)|
 | [Door monitoring for home automation](https://github.com/landing-ai/landingai-python-v1/blob/main/examples/rtsp-capture-notebook/rtsp-capture.ipynb) | This notebook uses an object detection model to determine whether a door is open or closed. The notebook can acquire images directly from an RTSP camera | Jupyter Notebook |
-| [Streaming capture service](examples/capture-service/run.py) | This application shows how to do continuous acquisition from an image sensor using RTSP. | Python application |
+| [Streaming capture service](https://github.com/landing-ai/landingai-python-v1/tree/main/examples/capture-service) | This application shows how to do continuous acquisition from an image sensor using RTSP. | Python application |
 
 ## Install the library
 
 ```bash
 pip install landingai
 ```
 
@@ -78,23 +78,23 @@
 
 Here is an example to show you how to run the `rtsp-capture` example locally in a shell environment:
 
 NOTE: it's recommended to create a new Python virtual environment first.
 
 1. Clone the repo to local: `git clone https://github.com/landing-ai/landingai-python-v1.git`
 2. Install the library: `pip install landingai`
-3. Run: `python landingai-python-v1/examples/rtsp-capture/run.py`
+3. Run: `python landingai-python-v1/examples/capture-service/run.py`
 
-## Building the LandingLens library locally (for developers and contributors)
+## Building the LandingLens library locally (for contributors)
 
 Most of the time you won't need to build the library since it is included on this repository and also published to pypi.
 
-But if you want to contribute to the repo, you can follow the below steps:
+But if you want to contribute to the repo, you can follow the below steps.
 
-### Install poetry
+### Prerequisite - Install poetry
 
 > See more from the [official doc](https://python-poetry.org/docs/#installation).
 
 For Linux, macOS, Windows (WSL):
 
 ```
 curl -sSL https://install.python-poetry.org | python3 -
```

