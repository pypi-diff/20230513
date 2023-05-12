# Comparing `tmp/fast_poibin-0.2.6.tar.gz` & `tmp/fast_poibin-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fast_poibin-0.2.6.tar", max compression
+gzip compressed data, was "fast_poibin-0.3.0.tar", max compression
```

## Comparing `fast_poibin-0.2.6.tar` & `fast_poibin-0.3.0.tar`

### file list

```diff
@@ -1,9 +1,10 @@
--rw-r--r--   0        0        0      369 2023-01-08 23:12:58.424504 fast_poibin-0.2.6/fast_poibin/__init__.py
--rw-r--r--   0        0        0     5603 2023-01-08 10:35:21.905022 fast_poibin-0.2.6/fast_poibin/pmf.py
--rw-r--r--   0        0        0     2376 2023-01-08 14:24:20.647672 fast_poibin-0.2.6/fast_poibin/poibin.py
--rw-r--r--   0        0        0        0 2023-01-08 23:02:33.444285 fast_poibin-0.2.6/fast_poibin/py.typed
--rw-r--r--   0        0        0    16725 2023-01-07 04:37:14.459723 fast_poibin-0.2.6/LICENSE
--rw-r--r--   0        0        0     1504 2023-01-08 23:16:08.046380 fast_poibin-0.2.6/pyproject.toml
--rw-r--r--   0        0        0     1155 2023-01-08 18:01:06.890526 fast_poibin-0.2.6/README.md
--rw-r--r--   0        0        0     1930 1970-01-01 00:00:00.000000 fast_poibin-0.2.6/setup.py
--rw-r--r--   0        0        0     1996 1970-01-01 00:00:00.000000 fast_poibin-0.2.6/PKG-INFO
+-rw-r--r--   0        0        0      369 2023-01-08 23:12:58.424504 fast_poibin-0.3.0/fast_poibin/__init__.py
+-rw-r--r--   0        0        0     2204 2023-05-12 21:50:23.988697 fast_poibin-0.3.0/fast_poibin/check_accuracy.py
+-rw-r--r--   0        0        0     5593 2023-05-12 20:58:01.085858 fast_poibin-0.3.0/fast_poibin/pmf.py
+-rw-r--r--   0        0        0     3387 2023-05-12 22:46:57.706988 fast_poibin-0.3.0/fast_poibin/poibin.py
+-rw-r--r--   0        0        0        0 2023-01-08 23:02:33.444285 fast_poibin-0.3.0/fast_poibin/py.typed
+-rw-r--r--   0        0        0    16725 2023-01-07 04:37:14.459723 fast_poibin-0.3.0/LICENSE
+-rw-r--r--   0        0        0     1504 2023-05-12 22:47:47.157221 fast_poibin-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0     1005 2023-05-12 22:46:57.705989 fast_poibin-0.3.0/README.md
+-rw-r--r--   0        0        0     1780 1970-01-01 00:00:00.000000 fast_poibin-0.3.0/setup.py
+-rw-r--r--   0        0        0     1846 1970-01-01 00:00:00.000000 fast_poibin-0.3.0/PKG-INFO
```

### Comparing `fast_poibin-0.2.6/fast_poibin/pmf.py` & `fast_poibin-0.3.0/fast_poibin/pmf.py`

 * *Files 2% similar despite different names*

```diff
@@ -58,30 +58,29 @@
 def calc_pmf_dp(probabilities: npt.NDArray[np.float64]) -> npt.NDArray[np.float64]:
     """Calculate PMF of Poisson binomial distribution by dynamic programming.
 
     Complexity:
         Time: O(N^2)
         Space: O(N)
     """
-    n = len(probabilities)
-    dp = np.zeros(n + 1, dtype=np.float64)
+    dp = np.zeros(len(probabilities) + 1, dtype=np.float64)
     dp[0] = 1.0
     for i, prob in enumerate(probabilities):
         for j in range(i + 1, 0, -1):
             dp[j] = dp[j] * (1 - prob) + dp[j - 1] * prob
         dp[0] *= 1 - prob
     return dp
 
 
 # calc_pmf uses numpy.convolve instead of FFT under this threshold. This value was decided
 # based on the experiment in https://github.com/privet-kitty/fast-poibin/issues/1.
 FFT_THRESHOLD = 1024
 
 # calc_pmf first performs DP on each subarray of this length. This value was decided
-# based on the experiment in https://github.com/privet-kitty/fast-poibin/issues/3
+# based on the experiment in https://github.com/privet-kitty/fast-poibin/issues/5
 DP_STEP = 255
 
 
 # FIXME: This type definition is a compromise.
 # 1. 1D np.ndarray is not Sequence. I couldn't find an appropriate iterable type that
 # contains np.ndarray.
 # 2. I'm not sure whether np.floating[Any] is a decent type for generic float.
```

### Comparing `fast_poibin-0.2.6/LICENSE` & `fast_poibin-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `fast_poibin-0.2.6/pyproject.toml` & `fast_poibin-0.3.0/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [tool.poetry]
 name = "fast-poibin"
-version = "0.2.6"
+version = "0.3.0"
 description = "Package for computing PMF and CDF of Poisson binomial distribution."
 authors = ["Hugo Sansaqua <privet.kitty99@gmail.com>"]
 license = "MPL-2.0"
 readme = "README.md"
 repository = "https://github.com/privet-kitty/fast-poibin"
 documentation = "https://privet-kitty.github.io/fast-poibin/"
 packages = [{include = "fast_poibin"}]
 
 [tool.poetry.dependencies]
 python = "^3.8"
 numpy = "^1.23.0"
-numba = "^0.56.0"
+numba = "^0.57.0"
 
 [tool.poetry.group.dev.dependencies]
 mypy = "^0.991"
 flake8 = "^5.0.4"
 black = "^22.12.0"
 isort = "^5.11.4"
 poethepoet = "^0.17.1"
```

### Comparing `fast_poibin-0.2.6/README.md` & `fast_poibin-0.3.0/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,7 +1,28 @@
+Metadata-Version: 2.1
+Name: fast-poibin
+Version: 0.3.0
+Summary: Package for computing PMF and CDF of Poisson binomial distribution.
+Home-page: https://github.com/privet-kitty/fast-poibin
+License: MPL-2.0
+Author: Hugo Sansaqua
+Author-email: privet.kitty99@gmail.com
+Requires-Python: >=3.8,<4.0
+Classifier: License :: OSI Approved
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: numba (>=0.57.0,<0.58.0)
+Requires-Dist: numpy (>=1.23.0,<2.0.0)
+Project-URL: Documentation, https://privet-kitty.github.io/fast-poibin/
+Project-URL: Repository, https://github.com/privet-kitty/fast-poibin
+Description-Content-Type: text/markdown
+
 # fast-poibin
 
 [![Build Status](https://github.com/privet-kitty/fast-poibin/workflows/CI/badge.svg)](https://github.com/privet-kitty/fast-poibin/actions)
 [![Coverage Status](https://coveralls.io/repos/github/privet-kitty/fast-poibin/badge.svg?branch=main)](https://coveralls.io/github/privet-kitty/fast-poibin?branch=main)
 [![PyPI Version](https://img.shields.io/pypi/v/fast-poibin)](https://pypi.org/project/fast-poibin/)
 
 
@@ -17,15 +38,15 @@
 
 
 ```bash
 pip install fast-poibin
 ```
 
 
-You need Python version 3.8 or later. As of this writing, Python 3.11 isn't supported, but it will be available as soon as [numba supports it](https://github.com/numba/numba/issues/8304).
+You need Python version 3.8 or later.
 
 ## Basic Usage
 
 
 ```python
 >>> from fast_poibin import PoiBin
 >>> poibin = PoiBin([0.1, 0.2, 0.2])
@@ -37,7 +58,8 @@
 
 
 
 
 ## Copyright
 
 Copyright (c) 2023 Hugo Sansaqua.
+
```

### Comparing `fast_poibin-0.2.6/setup.py` & `fast_poibin-0.3.0/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -4,21 +4,21 @@
 packages = \
 ['fast_poibin']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
-['numba>=0.56.0,<0.57.0', 'numpy>=1.23.0,<2.0.0']
+['numba>=0.57.0,<0.58.0', 'numpy>=1.23.0,<2.0.0']
 
 setup_kwargs = {
     'name': 'fast-poibin',
-    'version': '0.2.6',
+    'version': '0.3.0',
     'description': 'Package for computing PMF and CDF of Poisson binomial distribution.',
-    'long_description': "# fast-poibin\n\n[![Build Status](https://github.com/privet-kitty/fast-poibin/workflows/CI/badge.svg)](https://github.com/privet-kitty/fast-poibin/actions)\n[![Coverage Status](https://coveralls.io/repos/github/privet-kitty/fast-poibin/badge.svg?branch=main)](https://coveralls.io/github/privet-kitty/fast-poibin?branch=main)\n[![PyPI Version](https://img.shields.io/pypi/v/fast-poibin)](https://pypi.org/project/fast-poibin/)\n\n\nfast-poibin is a Python package for efficiently computing PMF or CDF of Poisson binomial distribution.\n\n\n- API Reference: https://privet-kitty.github.io/fast-poibin/\n- Repository: https://github.com/privet-kitty/fast-poibin/\n\n\n## Installation\n\n\n\n```bash\npip install fast-poibin\n```\n\n\nYou need Python version 3.8 or later. As of this writing, Python 3.11 isn't supported, but it will be available as soon as [numba supports it](https://github.com/numba/numba/issues/8304).\n\n## Basic Usage\n\n\n```python\n>>> from fast_poibin import PoiBin\n>>> poibin = PoiBin([0.1, 0.2, 0.2])\n>>> poibin.pmf\narray([0.576, 0.352, 0.068, 0.004])\n>>> poibin.cdf\narray([0.576, 0.928, 0.996, 1.   ])\n```\n\n\n\n\n## Copyright\n\nCopyright (c) 2023 Hugo Sansaqua.\n",
+    'long_description': '# fast-poibin\n\n[![Build Status](https://github.com/privet-kitty/fast-poibin/workflows/CI/badge.svg)](https://github.com/privet-kitty/fast-poibin/actions)\n[![Coverage Status](https://coveralls.io/repos/github/privet-kitty/fast-poibin/badge.svg?branch=main)](https://coveralls.io/github/privet-kitty/fast-poibin?branch=main)\n[![PyPI Version](https://img.shields.io/pypi/v/fast-poibin)](https://pypi.org/project/fast-poibin/)\n\n\nfast-poibin is a Python package for efficiently computing PMF or CDF of Poisson binomial distribution.\n\n\n- API Reference: https://privet-kitty.github.io/fast-poibin/\n- Repository: https://github.com/privet-kitty/fast-poibin/\n\n\n## Installation\n\n\n\n```bash\npip install fast-poibin\n```\n\n\nYou need Python version 3.8 or later.\n\n## Basic Usage\n\n\n```python\n>>> from fast_poibin import PoiBin\n>>> poibin = PoiBin([0.1, 0.2, 0.2])\n>>> poibin.pmf\narray([0.576, 0.352, 0.068, 0.004])\n>>> poibin.cdf\narray([0.576, 0.928, 0.996, 1.   ])\n```\n\n\n\n\n## Copyright\n\nCopyright (c) 2023 Hugo Sansaqua.\n',
     'author': 'Hugo Sansaqua',
     'author_email': 'privet.kitty99@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/privet-kitty/fast-poibin',
     'packages': packages,
     'package_data': package_data,
```

