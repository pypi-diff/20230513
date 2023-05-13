# Comparing `tmp/gato-toolkit-0.3.0.tar.gz` & `tmp/gato-toolkit-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gato-toolkit-0.3.0.tar", last modified: Fri May 12 21:41:44 2023, max compression
+gzip compressed data, was "gato-toolkit-0.3.1.tar", last modified: Sat May 13 10:20:11 2023, max compression
```

## Comparing `gato-toolkit-0.3.0.tar` & `gato-toolkit-0.3.1.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.684356 gato-toolkit-0.3.0/
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1070 2023-05-11 12:21:41.000000 gato-toolkit-0.3.0/LICENSE
--rw-r--r--   0 lucaslofaro   (501) staff       (20)       71 2023-05-12 04:29:48.000000 gato-toolkit-0.3.0/MANIFEST.in
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     2258 2023-05-12 21:41:44.683396 gato-toolkit-0.3.0/PKG-INFO
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1773 2023-05-11 12:58:50.000000 gato-toolkit-0.3.0/README.md
--rw-r--r--   0 lucaslofaro   (501) staff       (20)       38 2023-05-12 21:41:44.684530 gato-toolkit-0.3.0/setup.cfg
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      884 2023-05-12 21:41:31.000000 gato-toolkit-0.3.0/setup.py
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.672627 gato-toolkit-0.3.0/src/
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.678477 gato-toolkit-0.3.0/src/gato/
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.679045 gato-toolkit-0.3.0/src/gato/.config/
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      677 2023-05-04 05:53:25.000000 gato-toolkit-0.3.0/src/gato/.config/action-system-message.txt
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.681815 gato-toolkit-0.3.0/src/gato/.config/scenario-params/
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      240 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/categories.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      160 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/domains.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)    22221 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/entropies.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      123 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/regions.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      271 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/scopes.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      134 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-params/severities.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1577 2023-05-04 05:53:23.000000 gato-toolkit-0.3.0/src/gato/.config/scenario-system-messages.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)        0 2023-05-11 23:28:21.000000 gato-toolkit-0.3.0/src/gato/__init__.py
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      574 2023-05-12 06:55:28.000000 gato-toolkit-0.3.0/src/gato/entity.py
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1240 2023-05-12 21:33:19.000000 gato-toolkit-0.3.0/src/gato/generator.py
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1547 2023-05-12 21:33:19.000000 gato-toolkit-0.3.0/src/gato/llm.py
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     2071 2023-05-12 09:50:28.000000 gato-toolkit-0.3.0/src/gato/prompt.py
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     1271 2023-05-12 21:33:19.000000 gato-toolkit-0.3.0/src/gato/service.py
-drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-12 21:41:44.683017 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/
--rw-r--r--   0 lucaslofaro   (501) staff       (20)     2258 2023-05-12 21:41:44.000000 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/PKG-INFO
--rw-r--r--   0 lucaslofaro   (501) staff       (20)      720 2023-05-12 21:41:44.000000 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/SOURCES.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)        1 2023-05-12 21:41:44.000000 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/dependency_links.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)       32 2023-05-12 21:41:44.000000 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/requires.txt
--rw-r--r--   0 lucaslofaro   (501) staff       (20)        5 2023-05-12 21:41:44.000000 gato-toolkit-0.3.0/src/gato_toolkit.egg-info/top_level.txt
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.699267 gato-toolkit-0.3.1/
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     1070 2023-05-11 12:21:41.000000 gato-toolkit-0.3.1/LICENSE
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)       71 2023-05-12 04:29:48.000000 gato-toolkit-0.3.1/MANIFEST.in
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     4416 2023-05-13 10:20:11.698434 gato-toolkit-0.3.1/PKG-INFO
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     3931 2023-05-13 09:03:43.000000 gato-toolkit-0.3.1/README.md
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)       38 2023-05-13 10:20:11.699390 gato-toolkit-0.3.1/setup.cfg
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      884 2023-05-13 10:19:48.000000 gato-toolkit-0.3.1/setup.py
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.689041 gato-toolkit-0.3.1/src/
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.692699 gato-toolkit-0.3.1/src/gato/
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.693541 gato-toolkit-0.3.1/src/gato/.config/
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      677 2023-05-04 05:53:25.000000 gato-toolkit-0.3.1/src/gato/.config/action-system-message.txt
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.696354 gato-toolkit-0.3.1/src/gato/.config/scenario-params/
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      240 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/categories.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      160 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/domains.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)    22221 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/entropies.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      123 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/regions.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      271 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/scopes.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      134 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-params/severities.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     1577 2023-05-04 05:53:23.000000 gato-toolkit-0.3.1/src/gato/.config/scenario-system-messages.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)        0 2023-05-11 23:28:21.000000 gato-toolkit-0.3.1/src/gato/__init__.py
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      574 2023-05-12 06:55:28.000000 gato-toolkit-0.3.1/src/gato/entity.py
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     1240 2023-05-12 21:33:19.000000 gato-toolkit-0.3.1/src/gato/generator.py
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     1547 2023-05-12 21:33:19.000000 gato-toolkit-0.3.1/src/gato/llm.py
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     2071 2023-05-12 09:50:28.000000 gato-toolkit-0.3.1/src/gato/prompt.py
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     1271 2023-05-12 21:33:19.000000 gato-toolkit-0.3.1/src/gato/service.py
+drwxr-xr-x   0 lucaslofaro   (501) staff       (20)        0 2023-05-13 10:20:11.697824 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)     4416 2023-05-13 10:20:11.000000 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/PKG-INFO
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)      720 2023-05-13 10:20:11.000000 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/SOURCES.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)        1 2023-05-13 10:20:11.000000 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/dependency_links.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)       32 2023-05-13 10:20:11.000000 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/requires.txt
+-rw-r--r--   0 lucaslofaro   (501) staff       (20)        5 2023-05-13 10:20:11.000000 gato-toolkit-0.3.1/src/gato_toolkit.egg-info/top_level.txt
```

### Comparing `gato-toolkit-0.3.0/LICENSE` & `gato-toolkit-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/setup.py` & `gato-toolkit-0.3.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 def get_long_description():
     with open('README.md') as file:
         return file.read()
 
 
 setup(
     name="gato-toolkit",
-    version="0.3.0",
+    version="0.3.1",
     description="A toolkit for furthering research on AI alignment.",
     url="https://github.com/FyZyX/gato-toolkit",
     author="Lucas Lofaro <lucasmlofaro@gmail.com>",
     packages=find_packages(where="src"),
     package_dir={"": "src"},
     include_package_data=True,
     license='MIT',
```

### Comparing `gato-toolkit-0.3.0/src/gato/.config/action-system-message.txt` & `gato-toolkit-0.3.1/src/gato/.config/action-system-message.txt`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/.config/scenario-params/entropies.txt` & `gato-toolkit-0.3.1/src/gato/.config/scenario-params/entropies.txt`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/.config/scenario-system-messages.txt` & `gato-toolkit-0.3.1/src/gato/.config/scenario-system-messages.txt`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/entity.py` & `gato-toolkit-0.3.1/src/gato/entity.py`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/generator.py` & `gato-toolkit-0.3.1/src/gato/generator.py`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/llm.py` & `gato-toolkit-0.3.1/src/gato/llm.py`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/prompt.py` & `gato-toolkit-0.3.1/src/gato/prompt.py`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato/service.py` & `gato-toolkit-0.3.1/src/gato/service.py`

 * *Files identical despite different names*

### Comparing `gato-toolkit-0.3.0/src/gato_toolkit.egg-info/SOURCES.txt` & `gato-toolkit-0.3.1/src/gato_toolkit.egg-info/SOURCES.txt`

 * *Files identical despite different names*

