# Comparing `tmp/reasoner-pydantic-4.0.2.tar.gz` & `tmp/reasoner-pydantic-4.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reasoner-pydantic-4.0.2.tar", last modified: Thu May 11 17:40:46 2023, max compression
+gzip compressed data, was "reasoner-pydantic-4.0.3.tar", last modified: Fri May 12 22:46:32 2023, max compression
```

## Comparing `reasoner-pydantic-4.0.2.tar` & `reasoner-pydantic-4.0.3.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 17:40:46.253917 reasoner-pydantic-4.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-11 17:40:46.253917 reasoner-pydantic-4.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2748 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 17:40:46.253917 reasoner-pydantic-4.0.2/reasoner_pydantic/
--rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1143 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/auxgraphs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/base_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     4073 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/kgraph.py
--rw-r--r--   0 runner    (1001) docker     (123)     6226 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/message.py
--rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/metakg.py
--rw-r--r--   0 runner    (1001) docker     (123)     3826 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/qgraph.py
--rw-r--r--   0 runner    (1001) docker     (123)     4348 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/results.py
--rw-r--r--   0 runner    (1001) docker     (123)     4190 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/shared.py
--rw-r--r--   0 runner    (1001) docker     (123)     3554 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    12049 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/reasoner_pydantic/workflow.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 17:40:46.253917 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      582 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-11 17:40:46.000000 reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 17:40:46.253917 reasoner-pydantic-4.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      718 2023-05-11 17:40:42.000000 reasoner-pydantic-4.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:46:32.166085 reasoner-pydantic-4.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-12 22:46:32.166085 reasoner-pydantic-4.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2748 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:46:32.162085 reasoner-pydantic-4.0.3/reasoner_pydantic/
+-rw-r--r--   0 runner    (1001) docker     (123)     1171 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1143 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/auxgraphs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/base_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4065 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/kgraph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6226 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/message.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1444 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/metakg.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3826 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/qgraph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4348 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/results.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4166 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/shared.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3554 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12049 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/reasoner_pydantic/workflow.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:46:32.162085 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3060 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      582 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-12 22:46:32.000000 reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:46:32.166085 reasoner-pydantic-4.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      718 2023-05-12 22:46:28.000000 reasoner-pydantic-4.0.3/setup.py
```

### Comparing `reasoner-pydantic-4.0.2/PKG-INFO` & `reasoner-pydantic-4.0.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reasoner-pydantic
-Version: 4.0.2
+Version: 4.0.3
 Summary: Pydantic models for the Reasoner API data formats
 Home-page: https://github.com/TranslatorSRI/reasoner-pydantic
 Author: Kenneth Morton
 Author-email: kenny@covar.com
 License: MIT
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

### Comparing `reasoner-pydantic-4.0.2/README.md` & `reasoner-pydantic-4.0.3/README.md`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/__init__.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/__init__.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/auxgraphs.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/auxgraphs.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/base_model.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/base_model.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/kgraph.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/kgraph.py`

 * *Files 1% similar despite different names*

```diff
@@ -98,15 +98,15 @@
             if self.sources:
                 self.sources.update(other.sources)
             else:
                 self.sources = other.sources
 
     def get_primary_knowedge_source(self):
         for source in self.sources:
-            if source.resource_role == "biolink:primary_knowledge_source":
+            if source.resource_role == "primary_knowledge_source":
                 return source.resource_id
 
     def __hash__(self) -> int:
         primary_knowledge_source = self.get_primary_knowedge_source()
         return hash(
             (
                 self.subject,
```

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/message.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/message.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/metakg.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/metakg.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/qgraph.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/qgraph.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/results.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/results.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/shared.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/shared.py`

 * *Files 10% similar despite different names*

```diff
@@ -18,17 +18,17 @@
 class CURIE(str):
     """Compact URI."""
 
 
 class ResourceRoleEnum(str, Enum):
     """Types of resources"""
 
-    aggregator_knowledge_source = "biolink:aggregator_knowledge_source"
-    primary_knowledge_source = "biolink:primary_knowledge_source"
-    supporting_data_source = "biolink:supporting_data_source"
+    aggregator_knowledge_source = "aggregator_knowledge_source"
+    primary_knowledge_source = "primary_knowledge_source"
+    supporting_data_source = "supporting_data_source"
 
 
 class KnowledgeType(str, Enum):
     "Knowledge Type."
 
     lookup = "lookup"
     inferred = "inferred"
```

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/utils.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/utils.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic/workflow.py` & `reasoner-pydantic-4.0.3/reasoner_pydantic/workflow.py`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/PKG-INFO` & `reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reasoner-pydantic
-Version: 4.0.2
+Version: 4.0.3
 Summary: Pydantic models for the Reasoner API data formats
 Home-page: https://github.com/TranslatorSRI/reasoner-pydantic
 Author: Kenneth Morton
 Author-email: kenny@covar.com
 License: MIT
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

### Comparing `reasoner-pydantic-4.0.2/reasoner_pydantic.egg-info/SOURCES.txt` & `reasoner-pydantic-4.0.3/reasoner_pydantic.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `reasoner-pydantic-4.0.2/setup.py` & `reasoner-pydantic-4.0.3/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from pathlib import Path
 
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
 setup(
     name="reasoner-pydantic",
-    version="4.0.2",
+    version="4.0.3",
     author="Kenneth Morton",
     author_email="kenny@covar.com",
     url="https://github.com/TranslatorSRI/reasoner-pydantic",
     description="Pydantic models for the Reasoner API data formats",
     long_description=long_description,
     long_description_content_type="text/markdown",
     packages=["reasoner_pydantic"],
```

