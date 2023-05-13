# Comparing `tmp/business-profile-yelp-local-python-0.0.2.tar.gz` & `tmp/business-profile-yelp-local-python-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "business-profile-yelp-local-python-0.0.2.tar", last modified: Thu May 11 16:31:07 2023, max compression
+gzip compressed data, was "business-profile-yelp-local-python-0.0.3.tar", last modified: Sat May 13 14:55:06 2023, max compression
```

## Comparing `business-profile-yelp-local-python-0.0.2.tar` & `business-profile-yelp-local-python-0.0.3.tar`

### file list

```diff
@@ -1,11 +1,13 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 16:31:07.611994 business-profile-yelp-local-python-0.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)      488 2023-05-11 16:31:07.611994 business-profile-yelp-local-python-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-11 16:30:52.000000 business-profile-yelp-local-python-0.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 16:31:07.611994 business-profile-yelp-local-python-0.0.2/business_profile_yelp_local_python.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      488 2023-05-11 16:31:07.000000 business-profile-yelp-local-python-0.0.2/business_profile_yelp_local_python.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-05-11 16:31:07.000000 business-profile-yelp-local-python-0.0.2/business_profile_yelp_local_python.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 16:31:07.000000 business-profile-yelp-local-python-0.0.2/business_profile_yelp_local_python.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 16:31:07.000000 business-profile-yelp-local-python-0.0.2/business_profile_yelp_local_python.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-05-11 16:30:52.000000 business-profile-yelp-local-python-0.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 16:31:07.611994 business-profile-yelp-local-python-0.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      729 2023-05-11 16:30:52.000000 business-profile-yelp-local-python-0.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:55:06.567211 business-profile-yelp-local-python-0.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)      506 2023-05-13 14:55:06.567211 business-profile-yelp-local-python-0.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-13 14:54:55.000000 business-profile-yelp-local-python-0.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:55:06.567211 business-profile-yelp-local-python-0.0.3/business_profile_yelp_local_python.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      506 2023-05-13 14:55:06.000000 business-profile-yelp-local-python-0.0.3/business_profile_yelp_local_python.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      280 2023-05-13 14:55:06.000000 business-profile-yelp-local-python-0.0.3/business_profile_yelp_local_python.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:55:06.000000 business-profile-yelp-local-python-0.0.3/business_profile_yelp_local_python.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:55:06.000000 business-profile-yelp-local-python-0.0.3/business_profile_yelp_local_python.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-05-13 14:54:55.000000 business-profile-yelp-local-python-0.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:55:06.567211 business-profile-yelp-local-python-0.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      747 2023-05-13 14:54:55.000000 business-profile-yelp-local-python-0.0.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:55:06.567211 business-profile-yelp-local-python-0.0.3/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      254 2023-05-13 14:54:55.000000 business-profile-yelp-local-python-0.0.3/tests/tests.py
```

### Comparing `business-profile-yelp-local-python-0.0.2/setup.py` & `business-profile-yelp-local-python-0.0.3/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 import setuptools
 # used by python -m build
 # python -m build needs pyproject.toml or setup.py
 setuptools.setup(
      name='business-profile-yelp-local-python',  
-     version='0.0.2',
+     version='0.0.3',
      author="Circles",
      author_email="info@circles.life",
-     description="PyPI Package for Circles Local XXX Python",
-     long_description="This is a package for sharing common XXX function used in different repositories",
+     description="PyPI Package for Circles Local Yelp Profile Python",
+     long_description="This is a package for sharing common yelp service function used in different repositories",
      long_description_content_type="text/markdown",
      url="https://github.com/javatechy/dokr",
      packages=setuptools.find_packages(),
      classifiers=[
          "Programming Language :: Python :: 3",
          "License :: Other/Proprietary License",
          "Operating System :: OS Independent",
```

