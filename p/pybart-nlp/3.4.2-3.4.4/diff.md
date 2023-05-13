# Comparing `tmp/pybart-nlp-3.4.2.tar.gz` & `tmp/pybart-nlp-3.4.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pybart-nlp-3.4.2.tar", last modified: Tue May  9 11:02:37 2023, max compression
+gzip compressed data, was "pybart-nlp-3.4.4.tar", last modified: Sat May 13 20:46:01 2023, max compression
```

## Comparing `pybart-nlp-3.4.2.tar` & `pybart-nlp-3.4.4.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 11:02:37.606593 pybart-nlp-3.4.2/
--rw-r--r--   0 runner    (1001) docker     (123)    11356 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     8544 2023-05-09 11:02:37.606593 pybart-nlp-3.4.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8065 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 11:02:37.606593 pybart-nlp-3.4.2/pybart/
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7314 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13824 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/conllu_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)    10695 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/constraints.py
--rw-r--r--   0 runner    (1001) docker     (123)    90101 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/converter.py
--rw-r--r--   0 runner    (1001) docker     (123)     5641 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/graph_token.py
--rw-r--r--   0 runner    (1001) docker     (123)    17717 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/matcher.py
--rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/pybart/spacy_wrapper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 11:02:37.606593 pybart-nlp-3.4.2/pybart_nlp.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     8544 2023-05-09 11:02:37.000000 pybart-nlp-3.4.2/pybart_nlp.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      326 2023-05-09 11:02:37.000000 pybart-nlp-3.4.2/pybart_nlp.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 11:02:37.000000 pybart-nlp-3.4.2/pybart_nlp.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-09 11:02:37.000000 pybart-nlp-3.4.2/pybart_nlp.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-09 11:02:37.606593 pybart-nlp-3.4.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      695 2023-05-09 11:02:21.000000 pybart-nlp-3.4.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:46:01.798363 pybart-nlp-3.4.4/
+-rw-r--r--   0 runner    (1001) docker     (123)    11356 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     8544 2023-05-13 20:46:01.798363 pybart-nlp-3.4.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8065 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:46:01.798363 pybart-nlp-3.4.4/pybart/
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7314 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13824 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/conllu_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10695 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/constraints.py
+-rw-r--r--   0 runner    (1001) docker     (123)    90095 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5756 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/graph_token.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17717 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/matcher.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/pybart/spacy_wrapper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 20:46:01.798363 pybart-nlp-3.4.4/pybart_nlp.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     8544 2023-05-13 20:46:01.000000 pybart-nlp-3.4.4/pybart_nlp.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      326 2023-05-13 20:46:01.000000 pybart-nlp-3.4.4/pybart_nlp.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 20:46:01.000000 pybart-nlp-3.4.4/pybart_nlp.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 20:46:01.000000 pybart-nlp-3.4.4/pybart_nlp.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 20:46:01.798363 pybart-nlp-3.4.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      695 2023-05-13 20:45:51.000000 pybart-nlp-3.4.4/setup.py
```

### Comparing `pybart-nlp-3.4.2/LICENSE` & `pybart-nlp-3.4.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/PKG-INFO` & `pybart-nlp-3.4.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybart-nlp
-Version: 3.4.2
+Version: 3.4.4
 Summary: python converter from UD-tree to BART-graph representations
 Home-page: https://github.com/allenai/pybart
 Author: Aryeh Tiktinsky
 Author-email: aryehgigi@gmail.com
 Classifier: Programming Language :: Python :: 3.7
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: pybart-nlp Version: 3.4.2 Summary: python converter
+Metadata-Version: 2.1 Name: pybart-nlp Version: 3.4.4 Summary: python converter
 from UD-tree to BART-graph representations Home-page: https://github.com/
 allenai/pybart Author: Aryeh Tiktinsky Author-email: aryehgigi@gmail.com
 Classifier: Programming Language :: Python :: 3.7 Classifier: License :: OSI
 Approved :: Apache Software License Classifier: Operating System :: OS
 Independent Requires-Python: >=3.7, <3.12 Description-Content-Type: text/
 markdown License-File: LICENSE ![CI](https://github.com/allenai/pybart/actions/
 workflows/ci.yml/badge.svg)
```

### Comparing `pybart-nlp-3.4.2/README.md` & `pybart-nlp-3.4.4/README.md`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart/api.py` & `pybart-nlp-3.4.4/pybart/api.py`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart/conllu_wrapper.py` & `pybart-nlp-3.4.4/pybart/conllu_wrapper.py`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart/constraints.py` & `pybart-nlp-3.4.4/pybart/constraints.py`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart/converter.py` & `pybart-nlp-3.4.4/pybart/converter.py`

 * *Files 0% similar despite different names*

```diff
@@ -505,15 +505,15 @@
 
     def extra_compound_propagation(sentence, matches, converter):
         for cur_match in matches:
             gov = cur_match.token("gov")
             compound = cur_match.token("compound")
             middle_man = cur_match.token("middle_man")
             for rel in cur_match.edge(middle_man, gov):
-                sentence[compound].add_edge(Label(f"{rel}c", src="compound", src_type="NULL", uncertain=True), sentence[gov])
+                sentence[compound].add_edge(Label(rel, src="compound", src_type="NULL", uncertain=True), sentence[gov])
 
     # here we add a subject relation for each amod relation (but in the opposite direction)
     extra_amod_propagation_constraint = Full(
         tokens=[
             Token(id="gov"),
             Token(id="amod", outgoing_edges=[HasNoLabel(arg) for arg in subj_options]),
         ],
```

### Comparing `pybart-nlp-3.4.2/pybart/graph_token.py` & `pybart-nlp-3.4.4/pybart/graph_token.py`

 * *Files 6% similar despite different names*

```diff
@@ -35,15 +35,19 @@
         bart = ""
         if self.src is not None:
             if not remove_bart_extra_info:
                 iid_str = "" if self.iid is None else "#" + str(self.iid)
                 dep_args = ", ".join(x for x in filter(None, [self.src_type, self.phrase, "UNC" if self.uncertain else None]))
                 bart = "@" + self.src + "(" + dep_args + ")" + iid_str
 
-        return self.base + eud + bart
+        # special cases for altering the base label
+        base = self.base
+        if self.src == "compound" and self.src_type == "NULL":
+            base += "c"
+        return base + eud + bart
 
     # operator overloading: less than
     def __lt__(self, other):
         return self.to_str(False, False) < other.to_str(False, False)
 
 
 class Token:
@@ -62,43 +66,43 @@
                      upos if upos else upos_copy,
                      xpos if xpos else xpos_copy,
                      feats if feats else feats_copy,
                      head if head else head_copy,
                      deprel if deprel else deprel_copy,
                      deps if deps else deps_copy,
                      misc if misc else misc_copy)
-    
+
     def add_child(self, child):
         self._children_list.append(child)
-    
+
     def remove_child(self, child):
         self._children_list.remove(child)
-    
+
     def get_children(self):
         return self._children_list
-    
+
     def get_children_with_rels(self):
         return [(child, list(child.get_new_relations(self))[0][1]) for child in self.get_children()]
 
     def get_conllu_string(self, remove_enhanced_extra_info, remove_bart_extra_info):
         # for 'deps' field, we need to sort the new relations and then add them with '|' separation,
         # as required by the format.
         sorted_ = sorted((h, sorted(rels)) for h, rels in self.get_new_relations())
         self._conllu_info["deps"] = "|".join([str(a.get_conllu_field('id')) + ":" + bb.to_str(remove_enhanced_extra_info, remove_bart_extra_info) for (a, b) in sorted_ for bb in b])
         return "\t".join([str(v) for v in self._conllu_info.values()])
-    
+
     def set_conllu_field(self, field, val):
         self._conllu_info[field] = val
-    
+
     def get_conllu_field(self, field):
         return self._conllu_info[field]
 
     def get_parents(self):
         return self._new_deps.keys()
-    
+
     def get_new_relations(self, given_head=None):
         if given_head:
             if given_head in self._new_deps:
                 return [(given_head, self._new_deps[given_head])]
             else:
                 return dict().items()
         else:
@@ -109,30 +113,30 @@
         if head in self._new_deps:
             if rel in self._new_deps[head]:
                 return
             self._new_deps[head] += [rel]
         else:
             self._new_deps[head] = [rel]
             head.add_child(self)
-    
+
     def remove_edge(self, rel, head):
         assert isinstance(rel, Label)
         if head in self._new_deps and rel in self._new_deps[head]:
             self._new_deps[head].remove(rel)
             if not self._new_deps[head]:
                 self._new_deps.pop(head)
                 head.remove_child(self)
-    
+
     def remove_all_edges(self):
         _ = [self.remove_edge(edge, head) for head, edges in list(self.get_new_relations()) for edge in edges]
-    
+
     def replace_edge(self, old_rel, new_rel, old_head, new_head):
         self.remove_edge(old_rel, old_head)
         self.add_edge(new_rel, new_head)
-    
+
     # operator overloading: less than
     def __lt__(self, other):
         return self.get_conllu_field('id') < other.get_conllu_field('id')
 
 
 def add_basic_edges(sentence):
     """Purpose: adds each basic deprel relation and the relevant father to its son.
```

### Comparing `pybart-nlp-3.4.2/pybart/matcher.py` & `pybart-nlp-3.4.4/pybart/matcher.py`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart/spacy_wrapper.py` & `pybart-nlp-3.4.4/pybart/spacy_wrapper.py`

 * *Files identical despite different names*

### Comparing `pybart-nlp-3.4.2/pybart_nlp.egg-info/PKG-INFO` & `pybart-nlp-3.4.4/pybart_nlp.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybart-nlp
-Version: 3.4.2
+Version: 3.4.4
 Summary: python converter from UD-tree to BART-graph representations
 Home-page: https://github.com/allenai/pybart
 Author: Aryeh Tiktinsky
 Author-email: aryehgigi@gmail.com
 Classifier: Programming Language :: Python :: 3.7
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: pybart-nlp Version: 3.4.2 Summary: python converter
+Metadata-Version: 2.1 Name: pybart-nlp Version: 3.4.4 Summary: python converter
 from UD-tree to BART-graph representations Home-page: https://github.com/
 allenai/pybart Author: Aryeh Tiktinsky Author-email: aryehgigi@gmail.com
 Classifier: Programming Language :: Python :: 3.7 Classifier: License :: OSI
 Approved :: Apache Software License Classifier: Operating System :: OS
 Independent Requires-Python: >=3.7, <3.12 Description-Content-Type: text/
 markdown License-File: LICENSE ![CI](https://github.com/allenai/pybart/actions/
 workflows/ci.yml/badge.svg)
```

### Comparing `pybart-nlp-3.4.2/setup.py` & `pybart-nlp-3.4.4/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pybart-nlp",
-    version="3.4.2",
+    version="3.4.4",
     author="Aryeh Tiktinsky",
     author_email="aryehgigi@gmail.com",
     description="python converter from UD-tree to BART-graph representations",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/allenai/pybart",
     packages=setuptools.find_packages(),
```

