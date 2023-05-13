# Comparing `tmp/opsvis-1.0.8.tar.gz` & `tmp/opsvis-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "opsvis-1.0.8.tar", last modified: Wed Jun 15 18:59:59 2022, max compression
+gzip compressed data, was "opsvis-1.0.9.tar", last modified: Thu Jun 16 17:33:55 2022, max compression
```

## Comparing `opsvis-1.0.8.tar` & `opsvis-1.0.9.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-15 18:59:59.641623 opsvis-1.0.8/
--rw-r--r--   0 sewi      (1000) sewi      (1000)    35149 2020-08-24 10:31:43.000000 opsvis-1.0.8/LICENSE
--rw-r--r--   0 sewi      (1000) sewi      (1000)     1006 2022-06-15 18:59:59.641623 opsvis-1.0.8/PKG-INFO
--rw-r--r--   0 sewi      (1000) sewi      (1000)      477 2021-09-28 08:54:43.000000 opsvis-1.0.8/README.md
-drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-15 18:59:59.641623 opsvis-1.0.8/opsvis/
--rw-r--r--   0 sewi      (1000) sewi      (1000)      277 2022-04-09 09:24:42.000000 opsvis-1.0.8/opsvis/__init__.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)    20830 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/anim.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)    40345 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/defo.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)     8441 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/fibsec.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)      195 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/importing_modules.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)    65880 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/model.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)    23540 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/secforces.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)     3930 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/settings.py
--rw-r--r--   0 sewi      (1000) sewi      (1000)    34720 2022-06-15 18:59:02.000000 opsvis-1.0.8/opsvis/stress.py
-drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-15 18:59:59.641623 opsvis-1.0.8/opsvis.egg-info/
--rw-r--r--   0 sewi      (1000) sewi      (1000)     1006 2022-06-15 18:59:59.000000 opsvis-1.0.8/opsvis.egg-info/PKG-INFO
--rw-r--r--   0 sewi      (1000) sewi      (1000)      357 2022-06-15 18:59:59.000000 opsvis-1.0.8/opsvis.egg-info/SOURCES.txt
--rw-r--r--   0 sewi      (1000) sewi      (1000)        1 2022-06-15 18:59:59.000000 opsvis-1.0.8/opsvis.egg-info/dependency_links.txt
--rw-r--r--   0 sewi      (1000) sewi      (1000)       11 2022-06-15 18:59:59.000000 opsvis-1.0.8/opsvis.egg-info/requires.txt
--rw-r--r--   0 sewi      (1000) sewi      (1000)        7 2022-06-15 18:59:59.000000 opsvis-1.0.8/opsvis.egg-info/top_level.txt
--rw-r--r--   0 sewi      (1000) sewi      (1000)      104 2021-09-23 09:12:02.000000 opsvis-1.0.8/pyproject.toml
--rw-r--r--   0 sewi      (1000) sewi      (1000)      668 2022-06-15 18:59:59.641623 opsvis-1.0.8/setup.cfg
+drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-16 17:33:55.894154 opsvis-1.0.9/
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    35149 2020-08-24 10:31:43.000000 opsvis-1.0.9/LICENSE
+-rw-r--r--   0 sewi      (1000) sewi      (1000)     1006 2022-06-16 17:33:55.894154 opsvis-1.0.9/PKG-INFO
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      477 2021-09-28 08:54:43.000000 opsvis-1.0.9/README.md
+drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-16 17:33:55.894154 opsvis-1.0.9/opsvis/
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      277 2022-04-09 09:24:42.000000 opsvis-1.0.9/opsvis/__init__.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    20830 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/anim.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    40345 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/defo.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)     8441 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/fibsec.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      195 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/importing_modules.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    65880 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/model.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    23625 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/secforces.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)     3930 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/settings.py
+-rw-r--r--   0 sewi      (1000) sewi      (1000)    34720 2022-06-16 17:31:41.000000 opsvis-1.0.9/opsvis/stress.py
+drwxr-xr-x   0 sewi      (1000) sewi      (1000)        0 2022-06-16 17:33:55.894154 opsvis-1.0.9/opsvis.egg-info/
+-rw-r--r--   0 sewi      (1000) sewi      (1000)     1006 2022-06-16 17:33:55.000000 opsvis-1.0.9/opsvis.egg-info/PKG-INFO
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      357 2022-06-16 17:33:55.000000 opsvis-1.0.9/opsvis.egg-info/SOURCES.txt
+-rw-r--r--   0 sewi      (1000) sewi      (1000)        1 2022-06-16 17:33:55.000000 opsvis-1.0.9/opsvis.egg-info/dependency_links.txt
+-rw-r--r--   0 sewi      (1000) sewi      (1000)       11 2022-06-16 17:33:55.000000 opsvis-1.0.9/opsvis.egg-info/requires.txt
+-rw-r--r--   0 sewi      (1000) sewi      (1000)        7 2022-06-16 17:33:55.000000 opsvis-1.0.9/opsvis.egg-info/top_level.txt
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      104 2021-09-23 09:12:02.000000 opsvis-1.0.9/pyproject.toml
+-rw-r--r--   0 sewi      (1000) sewi      (1000)      668 2022-06-16 17:33:55.894154 opsvis-1.0.9/setup.cfg
```

### Comparing `opsvis-1.0.8/LICENSE` & `opsvis-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/PKG-INFO` & `opsvis-1.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: opsvis
-Version: 1.0.8
+Version: 1.0.9
 Summary: OpenSeesPy (OpenSees) Python postprocessing and visualization module
 Home-page: https://github.com/sewkokot/opsvis
 Author: Seweryn Kokot
 Author-email: sewkokot@gmail.com
 Project-URL: Bug Tracker, https://github.com/sewkokot/opsvis/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `opsvis-1.0.8/opsvis/anim.py` & `opsvis-1.0.9/opsvis/anim.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis/defo.py` & `opsvis-1.0.9/opsvis/defo.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis/fibsec.py` & `opsvis-1.0.9/opsvis/fibsec.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis/model.py` & `opsvis-1.0.9/opsvis/model.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis/secforces.py` & `opsvis-1.0.9/opsvis/secforces.py`

 * *Files 1% similar despite different names*

```diff
@@ -385,16 +385,17 @@
         else:
             fig, ax = plt.subplots()
 
         if fig_lbrt:
             fleft, fbottom, fright, ftop = fig_lbrt
             fig.subplots_adjust(left=fleft, bottom=fbottom, right=fright, top=ftop)
 
-    model.plot_model(node_labels=0, element_labels=0, fmt_model=fmt_model_secforce,
-                     node_supports=False, ax=ax)
+    ax = model.plot_model(node_labels=0, element_labels=0,
+                          fmt_model=fmt_model_secforce,
+                          node_supports=False, ax=ax)
 
     maxVal, minVal = -np.inf, np.inf
     ele_tags = ops.getEleTags()
 
     Ew = model.get_Ew_data_from_ops_domain()
 
     for ele_tag in ele_tags:
@@ -507,19 +508,19 @@
 
                     if maxVal_ind != 0 or maxVal_ind != nep - 1:
                         ax.text(s_p[maxVal_ind, 0], s_p[maxVal_ind, 1],
                                 f'{ss[maxVal_ind]:.5g}', va=va, ha=ha)
 
     if node_supports:
         node_tags = ops.getNodeTags()
-        model._plot_supports(node_tags, ax)
+        ax = model._plot_supports(node_tags, ax)
 
     # ax.grid(False)
 
-    return minVal, maxVal
+    return minVal, maxVal, ax
 
 
 def section_force_diagram_3d(sf_type, sfac=1., nep=17,
                              fmt_secforce1=fmt_secforce1,
                              fmt_secforce2=fmt_secforce2,
                              ref_vert_lines=True,
                              end_max_values=True,
@@ -582,16 +583,17 @@
 
     ax.set_xlabel('X')
     ax.set_ylabel('Y')
     ax.set_zlabel('Z')
 
     ax.view_init(azim=azim, elev=elev)
 
-    model.plot_model(node_labels=0, element_labels=0, fmt_model=fmt_model_secforce,
-                     node_supports=False, ax=ax)
+    ax = model.plot_model(node_labels=0, element_labels=0,
+                          fmt_model=fmt_model_secforce,
+                          node_supports=False, ax=ax)
 
     Ew = model.get_Ew_data_from_ops_domain_3d()
 
     for i, ele_tag in enumerate(ele_tags):
 
         # by default no element load
         eload_data = [['-beamUniform', 0., 0., 0.]]
@@ -703,8 +705,8 @@
                 ax.text(s_p[minVal_ind, 0], s_p[minVal_ind, 1], s_p[minVal_ind, 2],
                         f'{ss[minVal_ind]:.5g}', va=va, ha=ha)
 
             if maxVal_ind != 0 or maxVal_ind != nep - 1:
                 ax.text(s_p[maxVal_ind, 0], s_p[maxVal_ind, 1], s_p[maxVal_ind, 2],
                         f'{ss[maxVal_ind]:.5g}', va=va, ha=ha)
 
-    return minVal, maxVal
+    return minVal, maxVal, ax
```

### Comparing `opsvis-1.0.8/opsvis/settings.py` & `opsvis-1.0.9/opsvis/settings.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis/stress.py` & `opsvis-1.0.9/opsvis/stress.py`

 * *Files identical despite different names*

### Comparing `opsvis-1.0.8/opsvis.egg-info/PKG-INFO` & `opsvis-1.0.9/opsvis.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: opsvis
-Version: 1.0.8
+Version: 1.0.9
 Summary: OpenSeesPy (OpenSees) Python postprocessing and visualization module
 Home-page: https://github.com/sewkokot/opsvis
 Author: Seweryn Kokot
 Author-email: sewkokot@gmail.com
 Project-URL: Bug Tracker, https://github.com/sewkokot/opsvis/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `opsvis-1.0.8/setup.cfg` & `opsvis-1.0.9/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = opsvis
-version = 1.0.8
+version = 1.0.9
 author = Seweryn Kokot
 author_email = sewkokot@gmail.com
 description = OpenSeesPy (OpenSees) Python postprocessing and visualization module
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/sewkokot/opsvis
 project_urls =
```

