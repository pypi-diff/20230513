# Comparing `tmp/nonstd-0.0.5.tar.gz` & `tmp/nonstd-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonstd-0.0.5.tar", max compression
+gzip compressed data, was "nonstd-0.0.6.tar", max compression
```

## Comparing `nonstd-0.0.5.tar` & `nonstd-0.0.6.tar`

### file list

```diff
@@ -1,10 +1,9 @@
--rw-r--r--   0        0        0      226 2022-10-07 18:40:14.007136 nonstd-0.0.5/README.md
--rw-r--r--   0        0        0        0 2022-09-19 13:55:15.915217 nonstd-0.0.5/nonstd/__init__.py
--rw-r--r--   0        0        0     1011 2022-10-05 15:07:44.855811 nonstd-0.0.5/nonstd/derivative.py
--rw-r--r--   0        0        0     6592 2023-03-08 14:47:09.655257 nonstd-0.0.5/nonstd/distributions.py
--rw-r--r--   0        0        0      900 2023-03-05 12:31:49.390212 nonstd-0.0.5/nonstd/logging.py
--rw-r--r--   0        0        0    10241 2023-02-02 15:27:56.717083 nonstd-0.0.5/nonstd/sequence.py
--rw-r--r--   0        0        0     1532 2023-02-02 15:36:31.084857 nonstd-0.0.5/nonstd/sequence_math.py
--rw-r--r--   0        0        0      539 2023-03-08 15:11:34.872874 nonstd-0.0.5/pyproject.toml
--rw-r--r--   0        0        0      905 1970-01-01 00:00:00.000000 nonstd-0.0.5/setup.py
--rw-r--r--   0        0        0      802 1970-01-01 00:00:00.000000 nonstd-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      226 2022-10-07 18:40:14.007136 nonstd-0.0.6/README.md
+-rw-r--r--   0        0        0        0 2022-09-19 13:55:15.915217 nonstd-0.0.6/nonstd/__init__.py
+-rw-r--r--   0        0        0     1119 2023-05-11 17:20:08.640707 nonstd-0.0.6/nonstd/derivative.py
+-rw-r--r--   0        0        0     9740 2023-05-11 20:32:44.919166 nonstd-0.0.6/nonstd/distributions.py
+-rw-r--r--   0        0        0      900 2023-05-11 10:37:06.980105 nonstd-0.0.6/nonstd/logging.py
+-rw-r--r--   0        0        0    12222 2023-05-11 17:20:08.641178 nonstd-0.0.6/nonstd/sequence.py
+-rw-r--r--   0        0        0     1685 2023-05-11 17:20:08.641331 nonstd-0.0.6/nonstd/sequence_math.py
+-rw-r--r--   0        0        0      600 2023-05-13 13:35:38.303646 nonstd-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0      809 1970-01-01 00:00:00.000000 nonstd-0.0.6/PKG-INFO
```

### Comparing `nonstd-0.0.5/nonstd/derivative.py` & `nonstd-0.0.6/nonstd/derivative.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,37 +1,37 @@
 from typing import Optional
 
 import scipy.misc
 
 
 def by_kwarg(f, x0: dict, deriv_dim: str, dx: Optional[float] = None) -> float:
-	"""
-	TODO: add tests
+    """
+    TODO: add tests
 
-	Wrapper around ``scipy.misc.derivative`` to handle keyword arguments, instead of being limited to positional arguments.
-	Uses currying [0].
+    Wrapper around ``scipy.misc.derivative`` to handle keyword arguments, instead of being limited to positional arguments.
+    Uses currying [0].
 
-	[0]: https://en.wikipedia.org/wiki/Currying
+    [0]: https://en.wikipedia.org/wiki/Currying
 
-	:param f: Function to differentiate
-	:param x0: Point at which to differentiate, given as a dict of ``{argument_name: value}``
-	:param deriv_dim: The name of dimension along which to differentiate, as a ``str`
-	:param dx: Explicitly set the finite difference passed to SciPy.
-
-	:return: The derivative of ``f`` with respect to ``deriv_dim`` at ``x0``.
-	"""
-
-	if dx is None:
-		if x0[deriv_dim] != 0:
-			dx = x0[deriv_dim] / 100
-		else:
-			dx = 1e-12
-
-	def curried_f(x):
-		"""
-		``f`` expressed as a function of the relevant dimension only
-		"""
-		kwargs = x0
-		kwargs[deriv_dim] = x
-		return f(**kwargs)
+    :param f: Function to differentiate
+    :param x0: Point at which to differentiate, given as a dict of ``{argument_name: value}``
+    :param deriv_dim: The name of dimension along which to differentiate, as a ``str`
+    :param dx: Explicitly set the finite difference passed to SciPy.
+
+    :return: The derivative of ``f`` with respect to ``deriv_dim`` at ``x0``.
+    """
+
+    if dx is None:
+        if x0[deriv_dim] != 0:
+            dx = x0[deriv_dim] / 100
+        else:
+            dx = 1e-12
+
+    def curried_f(x):
+        """
+        ``f`` expressed as a function of the relevant dimension only
+        """
+        kwargs = x0
+        kwargs[deriv_dim] = x
+        return f(**kwargs)
 
-	return scipy.misc.derivative(curried_f, x0=x0[deriv_dim], dx=dx)
+    return scipy.misc.derivative(curried_f, x0=x0[deriv_dim], dx=dx)
```

### Comparing `nonstd-0.0.5/nonstd/logging.py` & `nonstd-0.0.6/nonstd/logging.py`

 * *Files identical despite different names*

### Comparing `nonstd-0.0.5/pyproject.toml` & `nonstd-0.0.6/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,23 +1,26 @@
 [tool.poetry]
 name = "nonstd"
-version = "0.0.5"
+version = "0.0.6"
 description = "Tom's non-standard library of useful classes and functions."
 authors = ["tadamcz <tadamczewskipublic@gmail.com>"]
 readme = "README.md"
 homepage = "https://github.com/tadamcz/nonstd"
 
 [tool.poetry.dependencies]
 python = ">=3.8,<3.12"
-scipy = ">=1,<1.9"
+scipy = "^1.10.1"
 
 [tool.poetry.dev-dependencies]
 pytest = "^7.1.3"
 pytest-pycharm = "^0.7.0"
 
 [tool.poetry.group.dev.dependencies]
 bump2version = "^1.0.1"
+pytest-kwparametrize = "^0.0.3"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
+[tool.black]
+line-length = 100
```

### Comparing `nonstd-0.0.5/PKG-INFO` & `nonstd-0.0.6/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: nonstd
-Version: 0.0.5
+Version: 0.0.6
 Summary: Tom's non-standard library of useful classes and functions.
 Home-page: https://github.com/tadamcz/nonstd
 Author: tadamcz
 Author-email: tadamczewskipublic@gmail.com
 Requires-Python: >=3.8,<3.12
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: scipy (>=1,<1.9)
+Requires-Dist: scipy (>=1.10.1,<2.0.0)
 Description-Content-Type: text/markdown
 
 # My non-standard library
 Personal collection of Python utilities.  
 
 # Installation
 This package is available on PyPi as `nonstd`. If you're using `poetry` for example, you would install it as:
```

