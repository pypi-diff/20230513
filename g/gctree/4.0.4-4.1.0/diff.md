# Comparing `tmp/gctree-4.0.4.tar.gz` & `tmp/gctree-4.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gctree-4.0.4.tar", last modified: Tue Jun  7 17:16:07 2022, max compression
+gzip compressed data, was "gctree-4.1.0.tar", last modified: Sat May 13 21:10:34 2023, max compression
```

## Comparing `gctree-4.0.4.tar` & `gctree-4.1.0.tar`

### file list

```diff
@@ -1,27 +1,32 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-07 17:16:07.516589 gctree-4.0.4/
--rw-r--r--   0 runner    (1001) docker     (121)    35141 2022-06-07 17:15:53.000000 gctree-4.0.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       49 2022-06-07 17:15:53.000000 gctree-4.0.4/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     1265 2022-06-07 17:16:07.516589 gctree-4.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      795 2022-06-07 17:15:53.000000 gctree-4.0.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-07 17:16:07.516589 gctree-4.0.4/gctree/
--rw-r--r--   0 runner    (1001) docker     (121)       72 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      498 2022-06-07 17:16:07.516589 gctree-4.0.4/gctree/_version.py
--rwxr-xr-x   0 runner    (1001) docker     (121)    80983 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/branching_processes.py
--rw-r--r--   0 runner    (1001) docker     (121)    25291 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/cli.py
--rwxr-xr-x   0 runner    (1001) docker     (121)     7706 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/deduplicate.py
--rw-r--r--   0 runner    (1001) docker     (121)     7370 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/isotype.py
--rw-r--r--   0 runner    (1001) docker     (121)    20607 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/isotyping.py
--rwxr-xr-x   0 runner    (1001) docker     (121)     2212 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/mkconfig.py
--rw-r--r--   0 runner    (1001) docker     (121)    21630 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/mutation_model.py
--rw-r--r--   0 runner    (1001) docker     (121)    11067 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/phylip_parse.py
--rwxr-xr-x   0 runner    (1001) docker     (121)     1158 2022-06-07 17:15:53.000000 gctree-4.0.4/gctree/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-07 17:16:07.516589 gctree-4.0.4/gctree.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     1265 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      469 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)      183 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)       87 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)        7 2022-06-07 17:16:07.000000 gctree-4.0.4/gctree.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      273 2022-06-07 17:16:07.516589 gctree-4.0.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1334 2022-06-07 17:15:53.000000 gctree-4.0.4/setup.py
--rw-r--r--   0 runner    (1001) docker     (121)    68611 2022-06-07 17:15:53.000000 gctree-4.0.4/versioneer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:10:34.653152 gctree-4.1.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    35141 2023-05-13 21:10:19.000000 gctree-4.1.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 21:10:19.000000 gctree-4.1.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1265 2023-05-13 21:10:34.653152 gctree-4.1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 21:10:19.000000 gctree-4.1.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:10:34.653152 gctree-4.1.0/gctree/
+-rw-r--r--   0 runner    (1001) docker     (123)       72 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      498 2023-05-13 21:10:34.653152 gctree-4.1.0/gctree/_version.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    81899 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/branching_processes.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25814 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/cli.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     7706 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/deduplicate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7370 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/isotype.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20657 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/isotyping.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2381 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/mkconfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23106 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/mutation_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11067 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/phylip_parse.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1158 2023-05-13 21:10:19.000000 gctree-4.1.0/gctree/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:10:34.653152 gctree-4.1.0/gctree.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1265 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      574 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 21:10:34.000000 gctree-4.1.0/gctree.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      273 2023-05-13 21:10:34.653152 gctree-4.1.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-05-13 21:10:19.000000 gctree-4.1.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 21:10:34.653152 gctree-4.1.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2421 2023-05-13 21:10:19.000000 gctree-4.1.0/tests/test_disambiguate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1891 2023-05-13 21:10:19.000000 gctree-4.1.0/tests/test_isotype.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7143 2023-05-13 21:10:19.000000 gctree-4.1.0/tests/test_likelihoods.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2775 2023-05-13 21:10:19.000000 gctree-4.1.0/tests/test_local_branching.py
+-rw-r--r--   0 runner    (1001) docker     (123)    68590 2023-05-13 21:10:19.000000 gctree-4.1.0/versioneer.py
```

### Comparing `gctree-4.0.4/LICENSE` & `gctree-4.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/PKG-INFO` & `gctree-4.1.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gctree
-Version: 4.0.4
+Version: 4.1.0
 Summary: phylogenetic inference of genotype-collapsed trees
 Home-page: https://github.com/matsengrp/gctree
 Author: Matsen Group
 Author-email: ematsen@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
 Classifier: Operating System :: OS Independent
```

### Comparing `gctree-4.0.4/README.md` & `gctree-4.1.0/README.md`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/gctree/branching_processes.py` & `gctree-4.1.0/gctree/branching_processes.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,10 @@
-r"""
-This module contains classes for simulation and inference for a binary
+r"""This module contains classes for simulation and inference for a binary
 branching process with mutation in which the tree is collapsed to nodes that
-count the number of clonal leaves of each type.
-"""
+count the number of clonal leaves of each type."""
 
 from __future__ import annotations
 
 import gctree.utils
 from gctree.isotyping import _isotype_dagfuncs, _isotype_annotation_dagfuncs
 from gctree.mutation_model import _mutability_dagfuncs
 from gctree.phylip_parse import disambiguate
@@ -28,15 +26,15 @@
 import pickle
 import functools
 import collections as coll
 import historydag as hdag
 import multiset
 import matplotlib as mp
 import matplotlib.pyplot as plt
-from typing import Tuple, Dict, List, Union, Set, Callable, Mapping, Sequence
+from typing import Tuple, Dict, List, Union, Set, Callable, Mapping, Sequence, Optional
 from decimal import Decimal
 
 
 class CollapsedTree:
     r"""A collapsed tree, modeled as an infinite type Galton-Watson process run
     to extinction.
 
@@ -49,15 +47,17 @@
             Can be ommitted on initializaion, and later simulated.
             If a tree is provided, names of nodes with abundance 0 will not be preserved.
         allow_repeats: tolerate the existence of nodes with the same genotype after collapse, e.g. in sister clades.
     """
 
     _max_ll_cache: Dict[Tuple[float, float], Tuple[int, int]] = {}
 
-    def __init__(self, tree: ete3.TreeNode = None, allow_repeats: bool = False):
+    def __init__(
+        self, tree: Optional[ete3.TreeNode] = None, allow_repeats: bool = False
+    ):
         if tree is not None:
             self.tree = tree.copy()
             self.tree.dist = 0
 
             def merge_isotype_dicts(parent_isotype, child_isotype):
                 # values are abundances and keys are isotypes.
                 parent_isotype = dict(parent_isotype)
@@ -372,15 +372,16 @@
 
     @np.errstate(all="raise")
     def ll(
         self,
         p: np.float64,
         q: np.float64,
     ) -> Tuple[np.float64, np.ndarray]:
-        r"""Log likelihood of branching process parameters :math:`(p, q)` given tree topology :math:`T` and genotype abundances :math:`A`.
+        r"""Log likelihood of branching process parameters :math:`(p, q)` given
+        tree topology :math:`T` and genotype abundances :math:`A`.
 
         .. math::
             \ell(p, q; T, A) = \log\mathbb{P}(T, A \mid p, q)
 
         Args:
             p: branching probability
             q: mutation probability
@@ -434,24 +435,24 @@
     def __repr__(self):
         r"""return a string representation for printing."""
         return str(self.tree)
 
     def render(
         self,
         outfile: str,
-        scale: float = None,
+        scale: Optional[float] = None,
         branch_margin: float = 0,
-        node_size: float = None,
+        node_size: Optional[float] = None,
         idlabel: bool = False,
-        colormap: Dict = None,
-        frame: int = None,
-        position_map: List = None,
-        chain_split: int = None,
-        frame2: int = None,
-        position_map2: List = None,
+        colormap: Optional[Dict] = None,
+        frame: Optional[int] = None,
+        position_map: Optional[List] = None,
+        chain_split: Optional[int] = None,
+        frame2: Optional[int] = None,
+        position_map2: Optional[List] = None,
         show_support: bool = False,
     ):
         r"""Render to tree image file.
 
         Args:
             outfile: file name to render to, filetype inferred from suffix, .svg for color
             scale: branch length scale in pixels (set automatically if ``None``)
@@ -636,37 +637,47 @@
             )
         return tree_copy.render(outfile, tree_style=ts)
 
     def feature_colormap(
         self,
         feature: str,
         cmap: str = "viridis",
-        vmin: float = None,
-        vmax: float = None,
+        vmin: Optional[float] = None,
+        vmax: Optional[float] = None,
+        scale: str = "linear",
+        **kwargs,
     ) -> Dict[str, str]:
         r"""Generate a colormap based on a continuous tree feature.
 
         Args:
             feature: feature name (all nodes in tree attribute must have this feature)
-            cmap: any matplotlib color palette: https://matplotlib.org/stable/gallery/color/colormap_reference.html
+            cmap: any `matplotlib color palette name <https://matplotlib.org/stable/gallery/color/colormap_reference.html>`_
             vmin: minimum value for colormap (default to minimum of the feature over the tree)
             vmax: maximum value for colormap (default to maximum of the feature over the tree)
+            scale: ``linear`` (default), ``log``, or ``symlog`` (must also provide ``linthresh`` kwarg)
+            kwargs: additional keyword arguments for scale transformation
 
         Returns:
             Dictionary of node names to hex color strings, which may be used as the colormap in :meth:`gctree.CollapsedTree.render`
         """
         cmap = mp.cm.get_cmap(cmap)
 
         if vmin is None:
             vmin = np.nanmin([getattr(node, feature) for node in self.tree.traverse()])
         if vmax is None:
             vmax = np.nanmax([getattr(node, feature) for node in self.tree.traverse()])
 
-        # define the minimum and maximum values for our colormap
-        norm = mp.colors.Normalize(vmin=vmin, vmax=vmax)
+        if scale == "linear":
+            norm = mp.colors.Normalize(vmin=vmin, vmax=vmax)
+        elif scale == "log":
+            norm = mp.colors.LogNorm(vmin=vmin, vmax=vmax)
+        elif scale == "symlog":
+            norm = mp.colors.SymLogNorm(vmin=vmin, vmax=vmax, **kwargs)
+        else:
+            raise ValueError(f"unrecognize scale: {scale}")
 
         return {
             node.name: mp.colors.to_hex(cmap(norm(getattr(node, feature))))
             for node in self.tree.traverse()
         }
 
     def write(self, file_name: str):
@@ -814,18 +825,19 @@
                 if partition1.isdisjoint(partition2):
                     return True
         return False
 
     def support(
         self,
         bootstrap_trees_list: List[CollapsedTree],
-        weights: List[np.float64] = None,
+        weights: Optional[List[np.float64]] = None,
         compatibility: bool = False,
     ):
-        r"""Compute support from a list of bootstrap :class:`CollapsedTree` objects, and add to tree attibute.
+        r"""Compute support from a list of bootstrap :class:`CollapsedTree`
+        objects, and add to tree attibute.
 
         Args:
             bootstrap_trees_list: List of trees
             weights: weights for each tree, perhaps for weighting parsimony degenerate trees
             compatibility: counts trees that don't disconfirm the split.
         """
         for node in self.tree.get_descendants():
@@ -847,25 +859,27 @@
                         supported = True
                 if supported:
                     support += weights[i] if weights is not None else 1
                 if compatible:
                     compatibility_ += weights[i] if weights is not None else 1
             node.support = compatibility_ if compatibility else support
 
-    def local_branching(self, tau=1, tau0=0.1, infinite_root_branch=True):
+    def local_branching(
+        self, tau=1, tau0=1, infinite_root_branch=True, nan_root_lbr=False
+    ):
         r"""Add local branching statistics (Neher et al. 2014) as tree node
-        features to the ETE tree attribute.
-        After execution, all nodes will have new features ``LBI``
-        (local branching index) and ``LBR`` (local branching ratio, below Vs
-        above the node)
+        features to the ETE tree attribute. After execution, all nodes will
+        have new features ``LBI`` (local branching index) and ``LBR`` (local
+        branching ratio, below Vs above the node)
 
         Args:
             tau: decay timescale for exponential filter
             tau0: effective branch length for branches with zero mutations
             infinite_root_branch: calculate assuming the root node has an infinite branch
+            nan_root_lbr: replace the root LBR value with ``np.nan``
         """
         # the fixed integral contribution for clonal cells indicated by abundance annotations
         clone_contribution = tau * (1 - np.exp(-tau0 / tau))
 
         # post-order traversal to populate downward integrals for each node
         for node in self.tree.traverse(strategy="postorder"):
             if node.is_leaf():
@@ -900,14 +914,17 @@
 
         # finally, compute LBI (LBR) as the sum (ratio) of downward and upward integrals at each node
         for node in self.tree.traverse():
             node_LB_down_total = sum(node.LB_down.values())
             node.LBI = node_LB_down_total + node.LB_up
             node.LBR = node_LB_down_total / node.LB_up
 
+        if nan_root_lbr:
+            self.tree.LBR = np.nan
+
 
 def _requires_dag(func):
     @functools.wraps(func)
     def wrapper(self, *args, **kwargs):
         if self._forest is None:
             raise NotImplementedError(
                 f"CollapsedForest class method {func.__name__} may only be called on instances "
@@ -929,15 +946,15 @@
 
     Args:
         forest: list of :class:`ete3.Tree`
     """
 
     def __init__(
         self,
-        forest: List[Union[CollapsedTree, ete3.Tree]] = None,
+        forest: Optional[List[Union[CollapsedTree, ete3.Tree]]] = None,
     ):
         if forest is not None:
             if len(forest) == 0:
                 raise ValueError("passed empty tree list")
             if isinstance(forest[0], CollapsedTree):
                 forest = [ctree.tree for ctree in forest]
             elif not isinstance(forest[0], ete3.Tree):
@@ -972,15 +989,16 @@
             self._validation_stats = None
         self._cm_countlist = None
         self._ctrees = None
         self.parameters = None
         self.is_isotyped = False
 
     def simulate(self, p: np.float64, q: np.float64, n_trees: int):
-        r"""Simulate a forest of collapsed trees. Overwrites existing forest attribute.
+        r"""Simulate a forest of collapsed trees. Overwrites existing forest
+        attribute.
 
         Args:
             p: branching probability
             q: mutation probability
             n_trees: number of trees
         """
         self._forest = None
@@ -995,15 +1013,18 @@
     @np.errstate(all="raise")
     def ll(
         self,
         p: np.float64,
         q: np.float64,
         marginal: bool = False,
     ) -> Tuple[np.float64, np.ndarray]:
-        r"""Log likelihood of branching process parameters :math:`(p, q)` given tree topologies :math:`T_1, \dots, T_n` and corresponding genotype abundances vectors :math:`A_1, \dots, A_n` for each of :math:`n` trees in the forest.
+        r"""Log likelihood of branching process parameters :math:`(p, q)` given
+        tree topologies :math:`T_1, \dots, T_n` and corresponding genotype
+        abundances vectors :math:`A_1, \dots, A_n` for each of :math:`n` trees
+        in the forest.
 
         If ``marginal=False`` (the default), compute the joint log likelihood
 
         .. math::
             \ell(p, q; T, A) = \sum_{i=1}^n\log\mathbb{P}(T_i, A_i \mid p, q),
 
         otherwise compute the marginal log likelihood
@@ -1094,19 +1115,19 @@
         """
         self.parameters = _mle_helper(self.ll, **kwargs)
         return self.parameters
 
     @_requires_dag
     def filter_trees(
         self,
-        ranking_coeffs: Sequence[float] = None,
-        mutability_file: str = None,
-        substitution_file: str = None,
+        ranking_coeffs: Optional[Sequence[float]] = None,
+        mutability_file: Optional[str] = None,
+        substitution_file: Optional[str] = None,
         ignore_isotype: bool = False,
-        chain_split: int = None,
+        chain_split: Optional[int] = None,
         verbose: bool = False,
         outbase: str = "gctree.out",
         summarize_forest: bool = False,
         tree_stats: bool = False,
     ) -> CollapsedForest:
         """Filter trees according to specified criteria.
 
@@ -1380,19 +1401,19 @@
             tdag = self._forest.copy()
             tdag.trim_topology(ctopology, collapse_leaves=True)
             yield self._trimmed_self(tdag)
 
     @_requires_dag
     def add_isotypes(
         self,
-        isotypemap: Mapping[str, str] = None,
-        isotypemap_file: str = None,
-        idmap: Mapping[str, Set[str]] = None,
-        idmap_file: str = None,
-        isotype_names: Sequence[str] = None,
+        isotypemap: Optional[Mapping[str, str]] = None,
+        isotypemap_file: Optional[str] = None,
+        idmap: Optional[Mapping[str, Set[str]]] = None,
+        idmap_file: Optional[str] = None,
+        isotype_names: Optional[Sequence[str]] = None,
     ):
         """Adds isotype annotations, including inferred ancestral isotypes, to
         all nodes in stored trees."""
         self.is_isotyped = True
 
         iso_funcs = _isotype_annotation_dagfuncs(
             isotypemap_file=isotypemap_file,
@@ -1615,14 +1636,15 @@
     if not result.success:
         warnings.warn("optimization not sucessful, " + result.message, RuntimeWarning)
     return result.x[0], result.x[1]
 
 
 def _lltree(cm_counts, p: np.float64, q: np.float64) -> Tuple[np.float64, np.ndarray]:
     r"""Log likelihood of branching process parameters :math:`(p, q)`
+
     .. math::
         \ell(p, q; T, A) = \log\mathbb{P}(T, A \mid p, q)
 
     Args:
         cm_counts: an iterable containing tuples `((c, m), n)` where `n` is the number of nodes
             in the tree with abundance `c` and `m` mutant clades
         p: branching probability
```

### Comparing `gctree-4.0.4/gctree/cli.py` & `gctree-4.1.0/gctree/cli.py`

 * *Files 2% similar despite different names*

```diff
@@ -588,24 +588,29 @@
     )
     parser_infer.add_argument(
         "--mutability",
         type=str,
         default=None,
         help=(
             "Path to mutability model file. If --mutability and --substitution are both provided, "
-            "they will be used to rank trees after likelihood and isotype parsimony."
+            "they will be used to rank trees after likelihood and isotype parsimony. This shall be a csv file"
+            "with the first column containing fivemers, and the second column containing mutability scores."
+            "See a file excerpt in the documentation for :meth:`mutation_model.MutationModel`."
         ),
     )
     parser_infer.add_argument(
         "--substitution",
         type=str,
         default=None,
         help=(
             "Path to substitution model file. If --mutability and --substitution are both provided, "
             "they will be used to rank trees after likelihood and isotype parsimony."
+            "This shall be a csv file with the first column containing fivemers, and the next four"
+            "columns containing targeting probabilities for bases A, C, G, and T, respectively."
+            "See a file excerpt in the documentation for :meth:`mutation_model.MutationModel`."
         ),
     )
     parser_infer.add_argument(
         "--ranking_coeffs",
         type=float,
         nargs=3,
         default=None,
```

### Comparing `gctree-4.0.4/gctree/deduplicate.py` & `gctree-4.1.0/gctree/deduplicate.py`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/gctree/isotype.py` & `gctree-4.1.0/gctree/isotype.py`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/gctree/isotyping.py` & `gctree-4.1.0/gctree/isotyping.py`

 * *Files 1% similar despite different names*

```diff
@@ -442,19 +442,19 @@
             "accum_func": sum,
         },
         name="Isotype Pars.",
     )
 
 
 def _isotype_annotation_dagfuncs(
-    isotypemap: Mapping[str, str] = None,
-    isotypemap_file: str = None,
-    idmap: Mapping[str, Set[str]] = None,
-    idmap_file: str = None,
-    isotype_names: Sequence[str] = None,
+    isotypemap: Optional[Mapping[str, str]] = None,
+    isotypemap_file: Optional[str] = None,
+    idmap: Optional[Mapping[str, Set[str]]] = None,
+    idmap_file: Optional[str] = None,
+    isotype_names: Optional[Sequence[str]] = None,
 ) -> hdag.utils.AddFuncDict:
     """Return functions for annotating history DAG nodes with inferred
     isotypes.
 
     Args:
         isotypemap: A dictionary mapping original IDs to observed isotype names
         isotypemap_file: A csv file providing an `isotypemap`
```

### Comparing `gctree-4.0.4/gctree/mkconfig.py` & `gctree-4.1.0/gctree/mkconfig.py`

 * *Files 13% similar despite different names*

```diff
@@ -8,29 +8,33 @@
 responses from stdin.  The config file generated by this script is
 meant to mimic the responses to the expected prompts.
 
 Typical usage is,
 
      $ mkconfig sequence.phy > dnapars.cfg
      $ dnapars < dnapars.cfg
-
 """
 import os
 import argparse
 
 
 def get_parser():
     parser = argparse.ArgumentParser(description=__doc__)
 
     parser.add_argument("phylip", help="PHYLIP input", type=str)
     parser.add_argument("treeprog", help="dnapars, dnaml, or seqboot", type=str)
     parser.add_argument(
         "--quick", action="store_true", help="quicker (less thourough) dnapars"
     )
     parser.add_argument(
+        "--jumble",
+        default=10,
+        help="search tree space with this many random permutations of the input sequences",
+    )
+    parser.add_argument(
         "--bootstrap",
         type=int,
         default=0,
         help="input is seqboot output with this many samples",
     )
     return parser
 
@@ -44,15 +48,15 @@
         print("Y")
         # random seed for bootstrap (odd integer)
         print("1")
         return
     print("J")
     # random seed for tree search
     print("1")
-    print("10")
+    print(args.jumble)
     if args.bootstrap:
         print("M")
         print("D")
         print(args.bootstrap)
     if args.treeprog == "dnapars":
         print("O")  # Outgroup root
         print(1)  # arbitrary root on first
```

### Comparing `gctree-4.0.4/gctree/mutation_model.py` & `gctree-4.1.0/gctree/mutation_model.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,53 +6,94 @@
 import numpy as np
 from scipy.stats import poisson
 import random
 import scipy
 from Bio.Seq import Seq
 import historydag as hdag
 from multiset import FrozenMultiset
-from typing import Tuple, List, Callable
+from typing import Tuple, List, Callable, Optional
 
 
 class MutationModel:
     r"""A class for a mutation model, and functions to mutate sequences.
 
     Args:
         mutability_file: S5F format mutabilities
         substitution_file: S5F format substitution biases
         mutation_order: whether or not to mutate sequences using a context sensitive manner
                         where mutation order matters
         with_replacement: allow the same position to mutate multiple times on a single branch
+
+    Notes:
+        ``mutability_file`` shall be a csv file with the first column containing fivemers,
+        and the second column containing mutability scores.
+        An example can be found at https://bitbucket.org/kleinstein/shazam/src/master/data-raw/HS5F_Mutability.csv
+
+        For example:
+
+        .. code-block:: text
+
+            Fivemer,Mutability,...
+            TCGGG,0.03542,...
+            GCCGG,0.02241675,...
+            GCCGC,0.06789,...
+            .
+            .
+            .
+
+
+        ``substitution_file`` shall be a csv file with the first column containing fivemers,
+        and the next four columns containing targeting probabilities for bases A, C, G,
+        and T, respectively.
+        An example can be found at https://bitbucket.org/kleinstein/shazam/src/master/data-raw/HS5F_Substitution.csv
+
+        For example:
+
+        .. code-block:: text
+
+            Fivemer,A,C,G,T,...
+            AAAAA,0,0.33,0.33,0.34,...
+            AAAAC,0,0.5000,0.2500,0.2500,...
+            AAAAG,0,0.65,0.15,0.20,...
+            .
+            .
+            .
     """
 
     def __init__(
         self,
-        mutability_file: str = None,
-        substitution_file: str = None,
+        mutability_file: Optional[str] = None,
+        substitution_file: Optional[str] = None,
         mutation_order: bool = True,
         with_replacement: bool = True,
     ):
         self.mutation_order = mutation_order
         self.with_replacement = with_replacement
         if mutability_file is not None and substitution_file is not None:
             self.context_model = {}
             with open(mutability_file, "r") as f:
                 # eat header
                 f.readline()
                 for line in f:
-                    motif, score = line.replace('"', "").split()[:2]
+                    if line[0] == '"':
+                        motif, score = line.replace('"', "").split()[:2]
+                    else:
+                        motif, score = line.replace(",", " ").split()[:2]
                     self.context_model[motif] = float(score)
 
             # kmer k
             self.k = None
             with open(substitution_file, "r") as f:
                 # eat header
                 f.readline()
                 for line in f:
-                    fields = line.replace('"', "").split()
+                    if line[0] == '"':
+                        fields = line.replace('"', "").split()
+                    else:
+                        fields = line.replace(",", " ").split()
                     motif = fields[0]
                     if self.k is None:
                         self.k = len(motif)
                         assert self.k % 2 == 1
                     else:
                         assert len(motif) == self.k
                     self.context_model[motif] = (
@@ -65,16 +106,17 @@
     @staticmethod
     def _disambiguate(sequence):
         r"""generator of all possible nt sequences implied by a sequence
         containing ambiguous bases."""
         return _sequence_disambiguations(sequence)
 
     def mutability(self, kmer: str) -> Tuple[np.float64, np.float64]:
-        r"""Returns the mutability of a central base of :math:`k`-mer, along with
-        nucleotide bias averages over ambiguous ``"N"`` nucleotide identities.
+        r"""Returns the mutability of a central base of :math:`k`-mer, along
+        with nucleotide bias averages over ambiguous ``"N"`` nucleotide
+        identities.
 
         Args:
             kmer: nucleotide :math:`k`-mer
         """
         if self.context_model is None:
             raise ValueError("kmer mutability only defined for context models")
         if len(kmer) != self.k:
@@ -120,15 +162,17 @@
             sequence = "N" * (self.k // 2) + sequence + "N" * (self.k // 2)
             # mutabilities of each nucleotide
             return [
                 self.mutability(sequence[(i - self.k // 2) : (i + self.k // 2 + 1)])
                 for i in range(self.k // 2, len(sequence) - self.k // 2)
             ]
 
-    def mutate(self, sequence: str, lambda0: np.float64 = 1, frame: int = None) -> str:
+    def mutate(
+        self, sequence: str, lambda0: np.float64 = 1, frame: Optional[int] = None
+    ) -> str:
         r"""Mutate a sequence, with lamdba0 the baseline mutability. Cannot
         mutate the same position multiple times.
 
         Args:
             sequence: nucleotide sequence to mutate
             lambda0: a baseline mutation rate
             frame: the reading frame of the first postition
@@ -197,25 +241,26 @@
                 ] = original_base  # <-- we only get here if we are retrying
 
         return sequence
 
     def simulate(
         self,
         sequence: str,
-        seq_bounds: Tuple[Tuple[int, int], Tuple[int, int]] = None,
+        seq_bounds: Optional[Tuple[Tuple[int, int], Tuple[int, int]]] = None,
         fitness_function: Callable = lambda seq: 0.9,
         lambda0: List[np.float64] = [1],
-        frame: int = None,
+        frame: Optional[int] = None,
         N_init: int = 1,
-        N: int = None,
-        T: int = None,
-        n: int = None,
+        N: Optional[int] = None,
+        T: Optional[int] = None,
+        n: Optional[int] = None,
         verbose: bool = False,
     ) -> TreeNode:
-        r"""Simulate a neutral binary branching process with the mutation model, returning a :class:`ete3.Treenode` object.
+        r"""Simulate a neutral binary branching process with the mutation model,
+        returning a :class:`ete3.Treenode` object.
 
         Args:
             sequence: root nucleotide sequence
             seq_bounds: ranges for two subsequences used as two parallel genes
             fitness_function: mean number offspring as a function of sequence
             lambda0: baseline mutation rate(s)
             frame: coding frame of starting position(s)
```

### Comparing `gctree-4.0.4/gctree/phylip_parse.py` & `gctree-4.1.0/gctree/phylip_parse.py`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/gctree/utils.py` & `gctree-4.1.0/gctree/utils.py`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/gctree.egg-info/PKG-INFO` & `gctree-4.1.0/gctree.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gctree
-Version: 4.0.4
+Version: 4.1.0
 Summary: phylogenetic inference of genotype-collapsed trees
 Home-page: https://github.com/matsengrp/gctree
 Author: Matsen Group
 Author-email: ematsen@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
 Classifier: Operating System :: OS Independent
```

### Comparing `gctree-4.0.4/setup.py` & `gctree-4.1.0/setup.py`

 * *Files identical despite different names*

### Comparing `gctree-4.0.4/versioneer.py` & `gctree-4.1.0/versioneer.py`

 * *Files 1% similar despite different names*

```diff
@@ -171,16 +171,16 @@
 ### Subprojects
 
 Versioneer has limited support for source trees in which `setup.py` is not in
 the root directory (e.g. `setup.py` and `.git/` are *not* siblings). The are
 two common reasons why `setup.py` might not be in the root:
 
 * Source trees which contain multiple subprojects, such as
-  [Buildbot](https://github.com/buildbot/buildbot), which contains both
-  "master" and "slave" subprojects, each with their own `setup.py`,
+  [Buildbot](https://github.com/buildbot/buildbot), which contains
+  multiple subprojects, each with their own `setup.py`,
   `setup.cfg`, and `tox.ini`. Projects like these produce multiple PyPI
   distributions (and upload multiple independently-installable tarballs).
 * Source trees whose main purpose is to contain a C library, but which also
   provide bindings to Python (and perhaps other langauges) in subdirectories.
 
 Versioneer will look for `.git` in parent directories, and most operations
 should get the right version string. However `pip` and `setuptools` have bugs
@@ -605,15 +605,15 @@
     if not tags:
         # Either we're using git < 1.8.3, or there really are no tags. We use
         # a heuristic: assume all version tags have a digit. The old git %%d
         # expansion behaves like git log --decorate=short and strips out the
         # refs/heads/ and refs/tags/ prefixes that would let us distinguish
         # between branches and tags. By ignoring refnames without digits, we
         # filter out many common branch names like "release" and
-        # "stabilization", as well as "HEAD" and "master".
+        # "stabilization", as well as "HEAD" and "main".
         tags = set([r for r in refs if re.search(r'\d', r)])
         if verbose:
             print("discarding '%%s', no digits" %% ",".join(refs - tags))
     if verbose:
         print("likely tags: %%s" %% ",".join(sorted(tags)))
     for ref in sorted(tags):
         # sorting will prefer e.g. "2.0" over "2.0rc1"
@@ -997,15 +997,15 @@
     if not tags:
         # Either we're using git < 1.8.3, or there really are no tags. We use
         # a heuristic: assume all version tags have a digit. The old git %d
         # expansion behaves like git log --decorate=short and strips out the
         # refs/heads/ and refs/tags/ prefixes that would let us distinguish
         # between branches and tags. By ignoring refnames without digits, we
         # filter out many common branch names like "release" and
-        # "stabilization", as well as "HEAD" and "master".
+        # "stabilization", as well as "HEAD" and "main".
         tags = set([r for r in refs if re.search(r'\d', r)])
         if verbose:
             print("discarding '%s', no digits" % ",".join(refs - tags))
     if verbose:
         print("likely tags: %s" % ",".join(sorted(tags)))
     for ref in sorted(tags):
         # sorting will prefer e.g. "2.0" over "2.0rc1"
```

