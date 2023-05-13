# Comparing `tmp/midjourney_api-1.0.2.tar.gz` & `tmp/midjourney_api-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "midjourney_api-1.0.2.tar", last modified: Sat May 13 21:06:37 2023, max compression
+gzip compressed data, was "midjourney_api-1.0.3.tar", last modified: Sat May 13 21:31:23 2023, max compression
```

## Comparing `midjourney_api-1.0.2.tar` & `midjourney_api-1.0.3.tar`

### file list

```diff
@@ -1,5 +1,5 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.631140 midjourney_api-1.0.2/
--rw-rw-rw-   0        0        0      862 2023-05-13 21:06:37.631140 midjourney_api-1.0.2/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 21:06:37.630130 midjourney_api-1.0.2/midjourney_api/
--rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.835466 midjourney_api-1.0.2/midjourney_api/__init__.py
--rw-rw-rw-   0        0        0     1702 2023-05-13 21:06:28.107535 midjourney_api-1.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 21:31:23.630205 midjourney_api-1.0.3/
+-rw-rw-rw-   0        0        0     9284 2023-05-13 21:31:23.632206 midjourney_api-1.0.3/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 21:31:23.629204 midjourney_api-1.0.3/midjourney_api/
+-rw-rw-rw-   0        0        0     5916 2023-05-13 18:17:05.835466 midjourney_api-1.0.3/midjourney_api/__init__.py
+-rw-rw-rw-   0        0        0     1804 2023-05-13 21:31:14.112613 midjourney_api-1.0.3/setup.py
```

### Comparing `midjourney_api-1.0.2/midjourney_api/__init__.py` & `midjourney_api-1.0.3/midjourney_api/__init__.py`

 * *Files identical despite different names*

### Comparing `midjourney_api-1.0.2/setup.py` & `midjourney_api-1.0.3/setup.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,25 +1,32 @@
 from distutils.core import setup
+
+import pypandoc
+
 setup(
-  name = 'midjourney_api',         # How you named your package folder (MyLib)
-  packages = ['midjourney_api'],   # Chose the same as "name"
-  version = '1.0.2',      # Start with a small number and increase it with every change you make
-  license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
-  description = 'Midjourney API wrapper by The Next Leg',   # Give a short description about your library
-  author = 'The Next leg',                   # Type in your name
-  author_email = 'support@thenextleg.io',      # Type in your E-Mail
-  url = 'https://github.com/midjourney-api-the-next-leg/python-midjourney-api',   # Provide either the link to your github or to your website
-  download_url = 'https://github.com/midjourney-api-the-next-leg/python-midjourney-api/archive/refs/tags/v1.0.0.tar.gz',    # I explain this later on
-  keywords = ['MIDJOURNEY', 'API', 'THE_NEXT_LEG'],   # Keywords that define your package best
-  readme='README.md',
-  install_requires=[],
-  classifiers=[
-    'Development Status :: 3 - Alpha',      # Chose either "3 - Alpha", "4 - Beta" or "5 - Production/Stable" as the current state of your package
-    'Intended Audience :: Developers',      # Define that your audience are developers
-    'Topic :: Software Development :: Build Tools',
-    'License :: OSI Approved :: MIT License',   # Again, pick a license
-    'Programming Language :: Python :: 3',      #Specify which pyhton versions that you want to support
-    'Programming Language :: Python :: 3.4',
-    'Programming Language :: Python :: 3.5',
-    'Programming Language :: Python :: 3.6',
-  ],
-)
+    name="midjourney_api",  # How you named your package folder (MyLib)
+    packages=["midjourney_api"],  # Chose the same as "name"
+    version="1.0.3",  # Start with a small number and increase it with every change you make
+    license="MIT",  # Chose a license from here: https://help.github.com/articles/licensing-a-repository
+    long_description=pypandoc.convert_file("README.md", "rst").replace("\r", ""),
+    description="Midjourney API wrapper by The Next Leg",  # Give a short description about your library
+    author="The Next leg",  # Type in your name
+    author_email="support@thenextleg.io",  # Type in your E-Mail
+    url="https://github.com/midjourney-api-the-next-leg/python-midjourney-api",  # Provide either the link to your github or to your website
+    download_url="https://github.com/midjourney-api-the-next-leg/python-midjourney-api/archive/refs/tags/v1.0.0.tar.gz",  # I explain this later on
+    keywords=[
+        "MIDJOURNEY",
+        "API",
+        "THE_NEXT_LEG",
+    ],  # Keywords that define your package best
+    install_requires=[],
+    classifiers=[
+        "Development Status :: 3 - Alpha",  # Chose either "3 - Alpha", "4 - Beta" or "5 - Production/Stable" as the current state of your package
+        "Intended Audience :: Developers",  # Define that your audience are developers
+        "Topic :: Software Development :: Build Tools",
+        "License :: OSI Approved :: MIT License",  # Again, pick a license
+        "Programming Language :: Python :: 3",  # Specify which pyhton versions that you want to support
+        "Programming Language :: Python :: 3.4",
+        "Programming Language :: Python :: 3.5",
+        "Programming Language :: Python :: 3.6",
+    ],
+)
```

