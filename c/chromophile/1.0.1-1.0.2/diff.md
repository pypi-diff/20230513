# Comparing `tmp/chromophile-1.0.1.tar.gz` & `tmp/chromophile-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chromophile-1.0.1.tar", last modified: Sat Dec 31 05:15:57 2022, max compression
+gzip compressed data, was "chromophile-1.0.2.tar", last modified: Sat May 13 16:53:51 2023, max compression
```

## Comparing `chromophile-1.0.1.tar` & `chromophile-1.0.2.tar`

### file list

```diff
@@ -1,15 +1,17 @@
-drwxr-xr-x   0 krh        (501) staff       (20)        0 2022-12-31 05:15:57.940781 chromophile-1.0.1/
--rw-r--r--   0 krh        (501) staff       (20)     7048 2022-12-31 05:15:42.000000 chromophile-1.0.1/LICENSE.txt
--rw-r--r--   0 krh        (501) staff       (20)       31 2022-12-31 05:15:42.000000 chromophile-1.0.1/MANIFEST.in
--rw-r--r--   0 krh        (501) staff       (20)    10800 2022-12-31 05:15:57.940938 chromophile-1.0.1/PKG-INFO
--rw-r--r--   0 krh        (501) staff       (20)     1995 2022-12-31 05:15:42.000000 chromophile-1.0.1/README.rst
-drwxr-xr-x   0 krh        (501) staff       (20)        0 2022-12-31 05:15:57.939437 chromophile-1.0.1/chromophile/
--rw-r--r--   0 krh        (501) staff       (20)     9649 2022-12-31 05:15:42.000000 chromophile-1.0.1/chromophile/__init__.py
--rw-r--r--   0 krh        (501) staff       (20)    48864 2022-12-31 05:15:42.000000 chromophile-1.0.1/chromophile/_cmaps.dat
-drwxr-xr-x   0 krh        (501) staff       (20)        0 2022-12-31 05:15:57.940569 chromophile-1.0.1/chromophile.egg-info/
--rw-r--r--   0 krh        (501) staff       (20)    10800 2022-12-31 05:15:57.000000 chromophile-1.0.1/chromophile.egg-info/PKG-INFO
--rw-r--r--   0 krh        (501) staff       (20)      246 2022-12-31 05:15:57.000000 chromophile-1.0.1/chromophile.egg-info/SOURCES.txt
--rw-r--r--   0 krh        (501) staff       (20)        1 2022-12-31 05:15:57.000000 chromophile-1.0.1/chromophile.egg-info/dependency_links.txt
--rw-r--r--   0 krh        (501) staff       (20)       12 2022-12-31 05:15:57.000000 chromophile-1.0.1/chromophile.egg-info/top_level.txt
--rw-r--r--   0 krh        (501) staff       (20)      866 2022-12-31 05:15:42.000000 chromophile-1.0.1/pyproject.toml
--rw-r--r--   0 krh        (501) staff       (20)      147 2022-12-31 05:15:57.941439 chromophile-1.0.1/setup.cfg
+drwxr-xr-x   0 krh        (501) staff       (20)        0 2023-05-13 16:53:51.813351 chromophile-1.0.2/
+-rw-r--r--   0 krh        (501) staff       (20)     7048 2023-05-13 16:39:47.000000 chromophile-1.0.2/LICENSE.txt
+-rw-r--r--   0 krh        (501) staff       (20)       31 2023-05-13 16:39:47.000000 chromophile-1.0.2/MANIFEST.in
+-rw-r--r--   0 krh        (501) staff       (20)    10800 2023-05-13 16:53:51.813541 chromophile-1.0.2/PKG-INFO
+-rw-r--r--   0 krh        (501) staff       (20)     1995 2023-05-13 16:39:47.000000 chromophile-1.0.2/README.rst
+drwxr-xr-x   0 krh        (501) staff       (20)        0 2023-05-13 16:53:51.810599 chromophile-1.0.2/chromophile/
+-rw-r--r--   0 krh        (501) staff       (20)     9935 2023-05-13 16:39:47.000000 chromophile-1.0.2/chromophile/__init__.py
+-rw-r--r--   0 krh        (501) staff       (20)    48864 2023-05-13 16:39:47.000000 chromophile-1.0.2/chromophile/_cmaps.dat
+drwxr-xr-x   0 krh        (501) staff       (20)        0 2023-05-13 16:53:51.812573 chromophile-1.0.2/chromophile.egg-info/
+-rw-r--r--   0 krh        (501) staff       (20)    10800 2023-05-13 16:53:51.000000 chromophile-1.0.2/chromophile.egg-info/PKG-INFO
+-rw-r--r--   0 krh        (501) staff       (20)      272 2023-05-13 16:53:51.000000 chromophile-1.0.2/chromophile.egg-info/SOURCES.txt
+-rw-r--r--   0 krh        (501) staff       (20)        1 2023-05-13 16:53:51.000000 chromophile-1.0.2/chromophile.egg-info/dependency_links.txt
+-rw-r--r--   0 krh        (501) staff       (20)       12 2023-05-13 16:53:51.000000 chromophile-1.0.2/chromophile.egg-info/top_level.txt
+-rw-r--r--   0 krh        (501) staff       (20)      866 2023-05-13 16:39:47.000000 chromophile-1.0.2/pyproject.toml
+-rw-r--r--   0 krh        (501) staff       (20)      147 2023-05-13 16:53:51.814046 chromophile-1.0.2/setup.cfg
+drwxr-xr-x   0 krh        (501) staff       (20)        0 2023-05-13 16:53:51.812858 chromophile-1.0.2/tests/
+-rw-r--r--   0 krh        (501) staff       (20)     3386 2023-05-13 16:39:47.000000 chromophile-1.0.2/tests/test_chromophile.py
```

### Comparing `chromophile-1.0.1/LICENSE.txt` & `chromophile-1.0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `chromophile-1.0.1/PKG-INFO` & `chromophile-1.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromophile
-Version: 1.0.1
+Version: 1.0.2
 Summary: Color maps for continuous quantitative data
 Author-email: Kyle Hofmann <kyle.hofmann@gmail.com>
 License: Creative Commons Legal Code
         
         CC0 1.0 Universal
         
             CREATIVE COMMONS CORPORATION IS NOT A LAW FIRM AND DOES NOT PROVIDE
```

### Comparing `chromophile-1.0.1/README.rst` & `chromophile-1.0.2/README.rst`

 * *Files identical despite different names*

### Comparing `chromophile-1.0.1/chromophile/__init__.py` & `chromophile-1.0.2/chromophile/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,15 +54,15 @@
 objects.  They are also displayed in the online documentation.
 """
 
 import importlib.resources
 import itertools
 
 
-__version__ = '1.0.1'
+__version__ = '1.0.2'
 __all__ = ('cmap', 'palette')
 
 _INDEX = (
     ('cp_cyc_isolum_dark', 360),
     ('cp_cyc_isolum_light', 360),
     ('cp_cyc_isolum_wide', 360),
     ('cp_cyc_red_cyan_valley', 360),
@@ -249,32 +249,40 @@
                 f"cp_cyc_{'_'.join(all_colors)}_hill_r",
                 [*data[:len(data) // 2][::-1], *data[len(data) // 2:][::-1]]
                 )
 
 
 def _init_mpl(cmaps):
     import numpy as np
+    import matplotlib as mpl
     from matplotlib.colors import ListedColormap
-    from matplotlib.cm import register_cmap
+
+    major, minor, *_ = map(int, mpl.__version__.split('.'))
+    if (major, minor) >= (3, 6):
+        def register_cmap(name, cm):
+            mpl.colormaps.register(cm)
+    else:
+        from matplotlib.cm import register_cmap
 
     cmap = _attrdict()
     for name, data in cmaps:
         mpl_colors = np.array(data, dtype=np.float64)
         mpl_colors /= 255.
         mpl_colors += 1./(2.*255.)
         np.clip(mpl_colors, 0.0, 1.0, out=mpl_colors)
         mpl_colors.setflags(write=False)
 
         mpl_cmap = ListedColormap(mpl_colors, name=name)
         register_cmap(name, mpl_cmap)
         cmap[name] = mpl_cmap
 
     for alias, name in _expanded_aliases:
-        register_cmap(alias, cmap[name])
-        cmap[alias] = cmap[name]
+        aliased_cmap = ListedColormap(cmap[name].colors, name=alias)
+        register_cmap(alias, aliased_cmap)
+        cmap[alias] = aliased_cmap
     return cmap
 
 
 def _init_bokeh(cmaps):
     palette = _attrdict()
     for name, data in cmaps:
         palette[name] = (
```

### Comparing `chromophile-1.0.1/chromophile/_cmaps.dat` & `chromophile-1.0.2/chromophile/_cmaps.dat`

 * *Files identical despite different names*

### Comparing `chromophile-1.0.1/chromophile.egg-info/PKG-INFO` & `chromophile-1.0.2/chromophile.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromophile
-Version: 1.0.1
+Version: 1.0.2
 Summary: Color maps for continuous quantitative data
 Author-email: Kyle Hofmann <kyle.hofmann@gmail.com>
 License: Creative Commons Legal Code
         
         CC0 1.0 Universal
         
             CREATIVE COMMONS CORPORATION IS NOT A LAW FIRM AND DOES NOT PROVIDE
```

### Comparing `chromophile-1.0.1/pyproject.toml` & `chromophile-1.0.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=40.9"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "chromophile"
-version = "1.0.1"
+version = "1.0.2"
 authors = [
   { name="Kyle Hofmann", email="kyle.hofmann@gmail.com" },
 ]
 description = "Color maps for continuous quantitative data"
 readme = "README.rst"
 license = { file="LICENSE.txt" }
 requires-python = ">=3.7"
```

