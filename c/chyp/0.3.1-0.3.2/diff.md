# Comparing `tmp/chyp-0.3.1.tar.gz` & `tmp/chyp-0.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chyp-0.3.1.tar", last modified: Thu May 11 20:31:48 2023, max compression
+gzip compressed data, was "chyp-0.3.2.tar", last modified: Sat May 13 12:30:19 2023, max compression
```

## Comparing `chyp-0.3.1.tar` & `chyp-0.3.2.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-11 20:31:48.578058 chyp-0.3.1/
--rw-r--r--   0 aleger    (1000) aleger    (1000)    11357 2022-09-06 15:50:03.000000 chyp-0.3.1/LICENSE
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     9800 2023-05-11 20:31:48.578058 chyp-0.3.1/PKG-INFO
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     9259 2023-05-07 21:30:27.000000 chyp-0.3.1/README.md
-drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-11 20:31:48.574058 chyp-0.3.1/chyp/
--rw-rw-r--   0 aleger    (1000) aleger    (1000)      727 2023-05-01 10:30:52.000000 chyp-0.3.1/chyp/__init__.py
--rw-r--r--   0 aleger    (1000) aleger    (1000)      699 2023-05-01 10:09:37.000000 chyp-0.3.1/chyp/__main__.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)    16930 2023-05-08 13:24:18.000000 chyp-0.3.1/chyp/graph.py
-drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-11 20:31:48.578058 chyp-0.3.1/chyp/gui/
--rw-rw-r--   0 aleger    (1000) aleger    (1000)      634 2023-05-01 10:14:39.000000 chyp-0.3.1/chyp/gui/__init__.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     3739 2023-05-09 07:10:05.000000 chyp-0.3.1/chyp/gui/app.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     1108 2023-05-06 10:32:00.000000 chyp-0.3.1/chyp/gui/codeview.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     5986 2023-05-11 09:13:14.000000 chyp-0.3.1/chyp/gui/document.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)    15296 2023-05-11 09:14:44.000000 chyp-0.3.1/chyp/gui/editor.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     2283 2023-05-08 16:45:36.000000 chyp-0.3.1/chyp/gui/errorlist.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     7056 2023-05-05 22:42:20.000000 chyp-0.3.1/chyp/gui/graphscene.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     1242 2023-05-05 22:33:30.000000 chyp-0.3.1/chyp/gui/graphview.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     2357 2023-05-08 12:36:17.000000 chyp-0.3.1/chyp/gui/highlighter.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     1672 2023-05-05 22:32:53.000000 chyp-0.3.1/chyp/gui/mainwindow.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)    10405 2023-05-11 20:29:46.000000 chyp-0.3.1/chyp/layout.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)    11254 2023-05-10 22:12:14.000000 chyp-0.3.1/chyp/matcher.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     8707 2023-05-08 16:34:40.000000 chyp-0.3.1/chyp/parser.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     3774 2023-05-07 18:11:57.000000 chyp-0.3.1/chyp/rewrite.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     1775 2023-05-08 10:53:38.000000 chyp-0.3.1/chyp/rule.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     3068 2023-03-30 12:34:42.000000 chyp-0.3.1/chyp/scraps.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     4602 2023-05-11 09:04:26.000000 chyp-0.3.1/chyp/state.py
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     4143 2023-05-11 20:25:03.000000 chyp-0.3.1/chyp/term.py
-drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-11 20:31:48.578058 chyp-0.3.1/chyp.egg-info/
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     9800 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/PKG-INFO
--rw-rw-r--   0 aleger    (1000) aleger    (1000)      588 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/SOURCES.txt
--rw-rw-r--   0 aleger    (1000) aleger    (1000)        1 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/dependency_links.txt
--rw-rw-r--   0 aleger    (1000) aleger    (1000)       43 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/entry_points.txt
--rw-rw-r--   0 aleger    (1000) aleger    (1000)       40 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/requires.txt
--rw-rw-r--   0 aleger    (1000) aleger    (1000)        5 2023-05-11 20:31:48.000000 chyp-0.3.1/chyp.egg-info/top_level.txt
--rw-rw-r--   0 aleger    (1000) aleger    (1000)      161 2023-05-05 09:44:28.000000 chyp-0.3.1/pyproject.toml
--rw-rw-r--   0 aleger    (1000) aleger    (1000)       38 2023-05-11 20:31:48.578058 chyp-0.3.1/setup.cfg
--rw-rw-r--   0 aleger    (1000) aleger    (1000)     1065 2023-05-11 20:31:14.000000 chyp-0.3.1/setup.py
+drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-13 12:30:19.371249 chyp-0.3.2/
+-rw-r--r--   0 aleger    (1000) aleger    (1000)    11357 2022-09-06 15:50:03.000000 chyp-0.3.2/LICENSE
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     9929 2023-05-13 12:30:19.371249 chyp-0.3.2/PKG-INFO
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     9388 2023-05-13 12:23:04.000000 chyp-0.3.2/README.md
+drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-13 12:30:19.371249 chyp-0.3.2/chyp/
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)      727 2023-05-01 10:30:52.000000 chyp-0.3.2/chyp/__init__.py
+-rw-r--r--   0 aleger    (1000) aleger    (1000)      699 2023-05-01 10:09:37.000000 chyp-0.3.2/chyp/__main__.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)    16930 2023-05-08 13:24:18.000000 chyp-0.3.2/chyp/graph.py
+drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-13 12:30:19.371249 chyp-0.3.2/chyp/gui/
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)      634 2023-05-01 10:14:39.000000 chyp-0.3.2/chyp/gui/__init__.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     3739 2023-05-09 07:10:05.000000 chyp-0.3.2/chyp/gui/app.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     1108 2023-05-06 10:32:00.000000 chyp-0.3.2/chyp/gui/codeview.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     5986 2023-05-11 09:13:14.000000 chyp-0.3.2/chyp/gui/document.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)    15296 2023-05-11 09:14:44.000000 chyp-0.3.2/chyp/gui/editor.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     2283 2023-05-08 16:45:36.000000 chyp-0.3.2/chyp/gui/errorlist.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     7056 2023-05-05 22:42:20.000000 chyp-0.3.2/chyp/gui/graphscene.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     1242 2023-05-05 22:33:30.000000 chyp-0.3.2/chyp/gui/graphview.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     2357 2023-05-08 12:36:17.000000 chyp-0.3.2/chyp/gui/highlighter.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     1672 2023-05-05 22:32:53.000000 chyp-0.3.2/chyp/gui/mainwindow.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)    10454 2023-05-13 12:29:20.000000 chyp-0.3.2/chyp/layout.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)    11254 2023-05-10 22:12:14.000000 chyp-0.3.2/chyp/matcher.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     8791 2023-05-13 11:26:15.000000 chyp-0.3.2/chyp/parser.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     3774 2023-05-07 18:11:57.000000 chyp-0.3.2/chyp/rewrite.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     1775 2023-05-08 10:53:38.000000 chyp-0.3.2/chyp/rule.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     3068 2023-03-30 12:34:42.000000 chyp-0.3.2/chyp/scraps.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     4602 2023-05-11 09:04:26.000000 chyp-0.3.2/chyp/state.py
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     4143 2023-05-11 20:25:03.000000 chyp-0.3.2/chyp/term.py
+drwxrwxr-x   0 aleger    (1000) aleger    (1000)        0 2023-05-13 12:30:19.371249 chyp-0.3.2/chyp.egg-info/
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     9929 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/PKG-INFO
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)      588 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/SOURCES.txt
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)        1 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/dependency_links.txt
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)       43 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/entry_points.txt
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)       40 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/requires.txt
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)        5 2023-05-13 12:30:19.000000 chyp-0.3.2/chyp.egg-info/top_level.txt
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)      161 2023-05-05 09:44:28.000000 chyp-0.3.2/pyproject.toml
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)       38 2023-05-13 12:30:19.371249 chyp-0.3.2/setup.cfg
+-rw-rw-r--   0 aleger    (1000) aleger    (1000)     1065 2023-05-13 12:30:04.000000 chyp-0.3.2/setup.py
```

### Comparing `chyp-0.3.1/LICENSE` & `chyp-0.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/PKG-INFO` & `chyp-0.3.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chyp
-Version: 0.3.1
+Version: 0.3.2
 Summary: An interactive theorem prover for monoidal categories
 Home-page: https://github.com/akissinger/chyp
 Author: Aleks Kissinger
 Author-email: aleks0@gmail.com
 License: Apache2
 Project-URL: Bug Tracker, https://github.com/akissinger/chyp/issues
 Classifier: Programming Language :: Python :: 3
@@ -51,14 +51,16 @@
 
 The main way to interact with Chyp is by writing `*.chyp` prover files. These are source files written in a simple declarative language that lets you:
 1. define generators,
 2. build terms by composing generators,
 3. define rewrite rules (i.e. axioms), and
 4. prove new rules by rewriting.
 
+You can find some examples of `*.chyp` files in the [examples](https://github.com/akissinger/chyp/tree/master/examples) folder.
+
 ## Defining generators and terms
 
 Generators are defined via the `gen` statement, which takes a name, a number of input wires, and a number of output wires. For example, we can define three new generators `f`, `g`, and `h` with various arities as follows:
 
     gen f : 2 -> 1
     gen g : 1 -> 2
     gen h : 1 -> 1
```

### Comparing `chyp-0.3.1/README.md` & `chyp-0.3.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -35,14 +35,16 @@
 
 The main way to interact with Chyp is by writing `*.chyp` prover files. These are source files written in a simple declarative language that lets you:
 1. define generators,
 2. build terms by composing generators,
 3. define rewrite rules (i.e. axioms), and
 4. prove new rules by rewriting.
 
+You can find some examples of `*.chyp` files in the [examples](https://github.com/akissinger/chyp/tree/master/examples) folder.
+
 ## Defining generators and terms
 
 Generators are defined via the `gen` statement, which takes a name, a number of input wires, and a number of output wires. For example, we can define three new generators `f`, `g`, and `h` with various arities as follows:
 
     gen f : 2 -> 1
     gen g : 1 -> 2
     gen h : 1 -> 1
```

### Comparing `chyp-0.3.1/chyp/__init__.py` & `chyp-0.3.2/chyp/__init__.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/__main__.py` & `chyp-0.3.2/chyp/__main__.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/graph.py` & `chyp-0.3.2/chyp/graph.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/__init__.py` & `chyp-0.3.2/chyp/gui/__init__.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/app.py` & `chyp-0.3.2/chyp/gui/app.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/codeview.py` & `chyp-0.3.2/chyp/gui/codeview.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/document.py` & `chyp-0.3.2/chyp/gui/document.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/editor.py` & `chyp-0.3.2/chyp/gui/editor.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/errorlist.py` & `chyp-0.3.2/chyp/gui/errorlist.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/graphscene.py` & `chyp-0.3.2/chyp/gui/graphscene.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/graphview.py` & `chyp-0.3.2/chyp/gui/graphview.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/highlighter.py` & `chyp-0.3.2/chyp/gui/highlighter.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/gui/mainwindow.py` & `chyp-0.3.2/chyp/gui/mainwindow.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/layout.py` & `chyp-0.3.2/chyp/layout.py`

 * *Files 1% similar despite different names*

```diff
@@ -101,18 +101,19 @@
 
     # problem = Problem(Minimize(cp.sum_squares(cp.vstack(opt))), constr)
     problem = Problem(Minimize(cp.norm1(cp.vstack(opt))), constr)
     problem.solve()
     min = None
     max = None
     for v,i in vtab.items():
-        y = vy.value[i]
-        if min is None or y < min: min = y
-        if max is None or y > max: max = y
-        g.vertex_data(v).y = y
+        if not vy.value is None:
+            y = vy.value[i]
+            if min is None or y < min: min = y
+            if max is None or y > max: max = y
+            g.vertex_data(v).y = y
 
     if not min is None and not max is None:
         yshift = (min + max) * 0.5
         for v in g.vertices():
             g.vertex_data(v).y -= yshift
     else:
         yshift = 0
```

### Comparing `chyp-0.3.1/chyp/matcher.py` & `chyp-0.3.2/chyp/matcher.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/parser.py` & `chyp-0.3.2/chyp/parser.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,19 +11,20 @@
     gen : "gen" var ":" num "->" num
     let : "let" var "=" term
     rule : "rule" var ":" term (eq | le) term
     rewrite : "rewrite" [converse] var ":" term rewrite_part*
     rewrite_part : (eq | le) term_hole [ "by" [converse] rule_ref ]
     converse : "-"
     ?term  : par_term | seq
-    ?par_term : "(" term ")" | par | perm | id | term_ref
+    ?par_term : "(" term ")" | par | perm | id | id0 | term_ref
     par : par_term "*" par_term
     seq : term ";" term
     perm : "sw" [ "[" num ("," num)* "]" ]
     id : "id"
+    id0 : "id0"
 
     eq : "=" | "=="
     le : "<=" | "~>"
     num : INT
     var : CNAME
     term_ref : CNAME
     rule_ref : CNAME
@@ -60,14 +61,17 @@
     
     def num(self, items: List[Any]) -> int:
         return int(items[0])
 
     def id(self, _: List[Any]) -> Graph:
         return identity()
 
+    def id0(self, _: List[Any]) -> Graph:
+        return Graph()
+
     def eq(self, _: List[Any]) -> bool:
         return True
 
     def le(self, _: List[Any]) -> bool:
         return False
 
     @v_args(meta=True)
@@ -203,15 +207,15 @@
     def rewrite_part(self, meta: Meta, items: List[Any]) -> Tuple[int, int, int, bool, Optional[Rule], Optional[Graph]]:
         equiv = items[0]
         t_start,t_end,rhs = items[1]
         converse = True if items[2] else False
 
         rule = items[3] if items[3] else self.rules['refl']
         if rule and converse:
-            rule = items[3].converse()
+            rule = rule.converse()
 
         if equiv and rule and not rule.equiv:
             rule = None
 
         return (meta.end_pos, t_start, t_end, equiv, rule, rhs)
```

### Comparing `chyp-0.3.1/chyp/rewrite.py` & `chyp-0.3.2/chyp/rewrite.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/rule.py` & `chyp-0.3.2/chyp/rule.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/scraps.py` & `chyp-0.3.2/chyp/scraps.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/state.py` & `chyp-0.3.2/chyp/state.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp/term.py` & `chyp-0.3.2/chyp/term.py`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/chyp.egg-info/PKG-INFO` & `chyp-0.3.2/chyp.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chyp
-Version: 0.3.1
+Version: 0.3.2
 Summary: An interactive theorem prover for monoidal categories
 Home-page: https://github.com/akissinger/chyp
 Author: Aleks Kissinger
 Author-email: aleks0@gmail.com
 License: Apache2
 Project-URL: Bug Tracker, https://github.com/akissinger/chyp/issues
 Classifier: Programming Language :: Python :: 3
@@ -51,14 +51,16 @@
 
 The main way to interact with Chyp is by writing `*.chyp` prover files. These are source files written in a simple declarative language that lets you:
 1. define generators,
 2. build terms by composing generators,
 3. define rewrite rules (i.e. axioms), and
 4. prove new rules by rewriting.
 
+You can find some examples of `*.chyp` files in the [examples](https://github.com/akissinger/chyp/tree/master/examples) folder.
+
 ## Defining generators and terms
 
 Generators are defined via the `gen` statement, which takes a name, a number of input wires, and a number of output wires. For example, we can define three new generators `f`, `g`, and `h` with various arities as follows:
 
     gen f : 2 -> 1
     gen g : 1 -> 2
     gen h : 1 -> 1
```

### Comparing `chyp-0.3.1/chyp.egg-info/SOURCES.txt` & `chyp-0.3.2/chyp.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `chyp-0.3.1/setup.py` & `chyp-0.3.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     long_description = fh.read()
 
 
 data_files = []
 
 setuptools.setup(
     name="chyp",
-    version="0.3.1",
+    version="0.3.2",
     author="Aleks Kissinger",
     author_email="aleks0@gmail.com",
     description="An interactive theorem prover for monoidal categories",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/akissinger/chyp",
     project_urls={
```

