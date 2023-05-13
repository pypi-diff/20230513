# Comparing `tmp/pymultiastar-0.0.6.tar.gz` & `tmp/pymultiastar-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymultiastar-0.0.6.tar", last modified: Wed Nov  9 12:37:21 2022, max compression
+gzip compressed data, was "pymultiastar-0.0.7.tar", last modified: Wed Nov  9 12:37:21 2022, max compression
```

## Comparing `pymultiastar-0.0.6.tar` & `pymultiastar-0.0.7.tar`

### file list

```diff
@@ -1,59 +1,63 @@
--rw-r--r--   0        0        0      162 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/.github/dependabot.yml
--rw-r--r--   0        0        0      581 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/.github/workflows/pip.yml
--rw-r--r--   0        0        0     1732 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/.github/workflows/wheels.yml
--rw-r--r--   0        0        0     2137 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/.gitignore
--rw-r--r--   0        0        0     1417 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/.pre-commit-config.yaml
--rw-r--r--   0        0        0      345 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/CMakeLists.txt
--rw-r--r--   0        0        0     1071 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/LICENSE
--rw-r--r--   0        0        0     3873 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/README.md
--rw-r--r--   0        0        0   585757 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/assets/imgs/newyork_map.png
--rw-r--r--   0        0        0   578063 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/assets/imgs/newyork_solved_1.png
--rw-r--r--   0        0        0   543823 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/assets/imgs/newyork_solved_2.png
--rw-r--r--   0        0        0    99021 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/assets/imgs/tradeoff.png
--rw-r--r--   0        0        0      427 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/contributing.md
--rw-r--r--   0        0        0       24 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/contributing.md
--rw-r--r--   0        0        0       92 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/css/material.css
--rw-r--r--   0        0        0      253 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/css/mkdocstrings.css
--rw-r--r--   0        0        0     1033 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/css/style.css
--rw-r--r--   0        0        0      978 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/gen_ref_nav.py
--rw-r--r--   0        0        0       18 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/index.md
--rw-r--r--   0        0        0       24 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/license.md
--rw-r--r--   0        0        0       28 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/tutorials/geoplanner.md
--rw-r--r--   0        0        0      507 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/docs/tutorials/simple.md
--rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/__init__.py
--rw-r--r--   0        0        0      212 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/log.py
--rw-r--r--   0        0        0     1806 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/run_maze_2d.py
--rw-r--r--   0        0        0     3313 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/run_scenarios.py
--rw-r--r--   0        0        0     1202 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/run_simple_demo.py
--rw-r--r--   0        0        0     1021 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/examples/run_simple_world_3d.py
--rw-r--r--   0        0        0     1854 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/mkdocs.yml
--rw-r--r--   0        0        0      431 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/noxfile.py
--rw-r--r--   0        0        0       13 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/output/.gitignore
--rw-r--r--   0        0        0     1475 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/pyproject.toml
--rw-r--r--   0        0        0       53 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/scripts/upload.sh
--rw-r--r--   0        0        0     8764 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/include/pymultiastar.hpp
--rw-r--r--   0        0        0     3063 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/main.cpp
--rw-r--r--   0        0        0      108 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/__init__.py
--rw-r--r--   0        0        0     2221 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/_core.pyi
--rw-r--r--   0        0        0      395 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/geoplanner/__init__.py
--rw-r--r--   0        0        0     8307 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/geoplanner/geoplanner.py
--rw-r--r--   0        0        0     4970 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/geoplanner/helper.py
--rw-r--r--   0        0        0      109 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/geoplanner/log.py
--rw-r--r--   0        0        0     2626 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/geoplanner/types.py
--rw-r--r--   0        0        0      538 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/types.py
--rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/visualization/__init__.py
--rw-r--r--   0        0        0     1727 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/visualization/img2d_helpers.py
--rw-r--r--   0        0        0      112 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/visualization/log.py
--rw-r--r--   0        0        0     6549 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar/visualization/vis3d_helpers.py
--rw-r--r--   0        0        0    18133 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/src/pymultiastar.cpp
--rw-r--r--   0        0        0       11 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/.gitignore
--rw-r--r--   0        0        0  1869483 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/maze_large.png
--rw-r--r--   0        0        0    38313 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/maze_small.png
--rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/world/.gitignore
--rw-r--r--   0        0        0     2582 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/world/annarbor/plan.json
--rw-r--r--   0        0        0 38263232 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/world/annarbor/voxel_map.npy
--rw-r--r--   0        0        0     4540 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/world/newyork/plan.json
--rw-r--r--   0        0        0 68625128 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/fixtures/world/newyork/voxel_map.npy
--rw-r--r--   0        0        0     1364 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/test_basic.py
--rw-r--r--   0        0        0      646 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/tests/test_geo_helper.py
--rw-r--r--   0        0        0     5601 2022-11-09 12:37:21.000000 pymultiastar-0.0.6/PKG-INFO
+-rw-r--r--   0        0        0      162 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/.github/dependabot.yml
+-rw-r--r--   0        0        0      581 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/.github/workflows/pip.yml
+-rw-r--r--   0        0        0     1732 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/.github/workflows/wheels.yml
+-rw-r--r--   0        0        0     2137 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/.gitignore
+-rw-r--r--   0        0        0     1417 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      345 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/CMakeLists.txt
+-rw-r--r--   0        0        0     1071 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/LICENSE
+-rw-r--r--   0        0        0     5378 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/README.md
+-rw-r--r--   0        0        0   585757 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/newyork_map.png
+-rw-r--r--   0        0        0   578063 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/newyork_solved_1.png
+-rw-r--r--   0        0        0   543823 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/newyork_solved_2.png
+-rw-r--r--   0        0        0   839076 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/simple_world_3d.png
+-rw-r--r--   0        0        0    22832 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/simple_world_3d_tradeoff.png
+-rw-r--r--   0        0        0    99021 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/assets/imgs/tradeoff.png
+-rw-r--r--   0        0        0      427 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/contributing.md
+-rw-r--r--   0        0        0       24 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/contributing.md
+-rw-r--r--   0        0        0       92 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/css/material.css
+-rw-r--r--   0        0        0      253 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/css/mkdocstrings.css
+-rw-r--r--   0        0        0     1033 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/css/style.css
+-rw-r--r--   0        0        0     1613 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/gen_ref_nav.py
+-rw-r--r--   0        0        0       18 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/index.md
+-rw-r--r--   0        0        0      394 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/js/mathjaxhelper.js
+-rw-r--r--   0        0        0       24 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/license.md
+-rw-r--r--   0        0        0      209 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/reference/index.md
+-rw-r--r--   0        0        0       28 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/tutorials/geoplanner.md
+-rw-r--r--   0        0        0      531 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/docs/tutorials/simple.md
+-rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/__init__.py
+-rw-r--r--   0        0        0      212 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/log.py
+-rw-r--r--   0        0        0     1831 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/run_maze_2d.py
+-rw-r--r--   0        0        0     3698 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/run_scenarios.py
+-rw-r--r--   0        0        0     1202 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/run_simple_demo.py
+-rw-r--r--   0        0        0     2521 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/examples/run_simple_world_3d.py
+-rw-r--r--   0        0        0     2012 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/mkdocs.yml
+-rw-r--r--   0        0        0      431 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/noxfile.py
+-rw-r--r--   0        0        0       13 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/output/.gitignore
+-rw-r--r--   0        0        0     1537 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/pyproject.toml
+-rw-r--r--   0        0        0       53 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/scripts/upload.sh
+-rw-r--r--   0        0        0     8764 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/include/pymultiastar.hpp
+-rw-r--r--   0        0        0     3063 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/main.cpp
+-rw-r--r--   0        0        0     1392 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/__init__.py
+-rw-r--r--   0        0        0     2984 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/_core.pyi
+-rw-r--r--   0        0        0      395 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/geoplanner/__init__.py
+-rw-r--r--   0        0        0     8648 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/geoplanner/geoplanner.py
+-rw-r--r--   0        0        0     4970 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/geoplanner/helper.py
+-rw-r--r--   0        0        0      109 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/geoplanner/log.py
+-rw-r--r--   0        0        0     2807 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/geoplanner/types.py
+-rw-r--r--   0        0        0      653 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/types.py
+-rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/visualization/__init__.py
+-rw-r--r--   0        0        0     1914 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/visualization/img2d_helpers.py
+-rw-r--r--   0        0        0      112 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/visualization/log.py
+-rw-r--r--   0        0        0     9641 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar/visualization/vis3d_helpers.py
+-rw-r--r--   0        0        0    18133 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/src/pymultiastar.cpp
+-rw-r--r--   0        0        0       11 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/.gitignore
+-rw-r--r--   0        0        0  1869483 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/maze_large.png
+-rw-r--r--   0        0        0    38313 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/maze_small.png
+-rw-r--r--   0        0        0        0 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/world/.gitignore
+-rw-r--r--   0        0        0     2582 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/world/annarbor/plan.json
+-rw-r--r--   0        0        0 38263232 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/world/annarbor/voxel_map.npy
+-rw-r--r--   0        0        0     4540 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/world/newyork/plan.json
+-rw-r--r--   0        0        0 68625128 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/fixtures/world/newyork/voxel_map.npy
+-rw-r--r--   0        0        0     1364 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/test_basic.py
+-rw-r--r--   0        0        0      646 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/tests/test_geo_helper.py
+-rw-r--r--   0        0        0     7283 2022-11-09 12:37:21.000000 pymultiastar-0.0.7/PKG-INFO
```

### Comparing `pymultiastar-0.0.6/.github/workflows/pip.yml` & `pymultiastar-0.0.7/.github/workflows/pip.yml`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/.github/workflows/wheels.yml` & `pymultiastar-0.0.7/.github/workflows/wheels.yml`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/.gitignore` & `pymultiastar-0.0.7/.gitignore`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/.pre-commit-config.yaml` & `pymultiastar-0.0.7/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/LICENSE` & `pymultiastar-0.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/README.md` & `pymultiastar-0.0.7/README.md`

 * *Files 18% similar despite different names*

```diff
@@ -4,17 +4,17 @@
 
 **What do you mean by discrete?**
 
 The map provided should be a 3D voxel grid(i, j, k), a 3D NumPy array, which the planner searches. A cell with the value 0.0 is considered free space. A cell with the value 1.0 is considered an obstacle and cannot be traversed (this value is configurable). Values between 0.0 and 1.0 can be traversed but with a penalty (penalty weight is configurable).
 
 **What do you mean by multiple goals with heterogenous values?**
 
-A normal A-star planner has a start location and one goal. This Multi-Goal planner allows you to provide multiple goal cells each having different values. Goals with lower values are more desirable. This planner will try to find the optimal **goal** *and* **path** which minimizes an objective function. It must be understood that the planner doesn't just find a path. It finds the goal and the corresponding optimal path that minimizes some larger objective function. 
+A normal A-star planner has a start location and one goal. This Multi-Goal planner allows you to provide multiple goal cells each having different values. Goals with lower values are more desirable. This planner will try to find the optimal **goal** *and* **path** which minimizes an objective function. It must be understood that the planner doesn't just find a path. It finds the *one* goal and the corresponding optimal path that minimizes some larger objective function. 
 
-**What is the objective function?**
+**What is the larger objective function?**
 
 The objective function is the minimization of total risk ($r_t$), which is the combination of path risk ($r_p$) and goal risk $r_g$. In my research the goals were landing sites, therefore I called the latter landing site risk $r_l$. 
 Below is an excerpt from my paper that discusses this trade-off between objectives:
 
     The figure below shows an example Pareto frontier that minimizes two objectives: landing
     site risk and path risk. Each purple dot represents a landing site. The x-axis represents
     landing site risk and the y-axis represents path risk to that site. The green line
@@ -26,21 +26,35 @@
 
 $$
 r_t = w_l \cdot r_l + w_p · r_p
 $$
 
 ![Tradeoff](https://raw.githubusercontent.com/JeremyBYU/pymultiastar/master/assets/imgs/tradeoff.png)
 
-**What precisely are these two objectives and how do they relate to the planner?**
+Given the weighting between the two objectives, **one** of the purple dots on the green line is considered the "best" goal/path pair and will have minimum total risk. Here's the kicker though: you do **not** know the path risk *until* you do path planning. However, path planning is very expensive. PyMultiAStar will search for the optimal goal/path such that we minimize our expensive path planning procedures, often only needing to perform path planning 1-3 times on average.
+
+**How do you minimize path planning? How do you know when to stop searching?**
+
+We first sort the goals by their *minimum* total risk $r_{t,min}$ where
+
+$$r_{t,min} = w_{g} \cdot r_{g} + w_p \cdot  h(\mathbf{start}, \mathbf{goal}) / R$$
+
+where $h$ is an admissible heuristic and $R$ is a normalizing constant. Basically, we are bounding the minimum path distance which in turn bounds total risk. $R$ is usually the largest distance permissible during path planning. This entire list is very cheap to compute and sort.
+
+The first goal in this sorted list is the most *likely* to be the lowest total risk, but we don't know until we do path planning. After path planning to this goal, we can determine the **true** path risk and calculate the total risk. If the goal's total risk is less than the *next* goal's **minimum** total risk, we can guarantee we found the optimal solution to our objective function. We can stop searching! 
+
+**What precisely are these objectives and where are the details of the planner?**
 
 See the following sections in the paper linked above: 
 
-- Definition of Path **Cost**: Section 1.3.2, Equations 1.6-1.8
-- Definition of Path **Risk**: Section 1.5, Equation 1.17
-- Definition of Landing Site (Goal) **Risk**: Section 1.4.4, Equation 1.9
+- Definition of **Path Cost**: Section 1.3.2, Equations 1.6-1.8
+- Definition of **Path Risk**: Section 1.5, Equation 1.17
+- Definition of **Landing Site (Goal) Risk**: Section 1.4.4, Equation 1.9. This can be defined as anything for your specific problem.
+- Definition of **Total Risk**: Section 1.6.2, Equation 1.18. 
+- Proof of Planner: Section 1.6.3
 
 
 ## Install
 
 Binary Wheels are provided for you on `PyPi`:
 
 1. Discrete Multi-Goal Planner - `pip install pymultiastar` - This exposes the class `PyMultiAStar`
@@ -52,11 +66,7 @@
 ## How to use
 
 Below are some examples:
 
 1. `run_simple_world_3d.py`. Shows a very simple example of a small 3D world with multiple goals.
 2. `run_maze_2d.py` - Demonstrates that 2D A-star path planning is a subset of the Multi-Goal Planner. It loads a 2D image of a maze as a single slice in a 3D world and has only 1 goal. 
 3. `run_scenarios.py` - Shows how to use the GeoPlanner and plan in a 3D world.
-
-## Notes
-
-inside pymultiastar map data - (i,j,k) is the row, column, depth
```

### Comparing `pymultiastar-0.0.6/assets/imgs/newyork_map.png` & `pymultiastar-0.0.7/assets/imgs/newyork_map.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/assets/imgs/newyork_solved_1.png` & `pymultiastar-0.0.7/assets/imgs/newyork_solved_1.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/assets/imgs/newyork_solved_2.png` & `pymultiastar-0.0.7/assets/imgs/newyork_solved_2.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/assets/imgs/tradeoff.png` & `pymultiastar-0.0.7/assets/imgs/tradeoff.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/docs/css/style.css` & `pymultiastar-0.0.7/docs/css/style.css`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/examples/run_maze_2d.py` & `pymultiastar-0.0.7/examples/run_maze_2d.py`

 * *Files 5% similar despite different names*

```diff
@@ -30,14 +30,15 @@
     # parameters to initialize multi goal a star search
     params = dict(
         map_res=1.0,
         obstacle_value=1.0,  # An obstacle will be the value 1.0
         normalizing_path_cost=maze_data["normalizing_path_cost"],
         goal_weight=0.5,
         path_weight=0.5,
+        allow_diag=False
     )
 
     planner = pmstar.PyMultiAStar(maze_data["map"], **params)
     t0 = perf_counter()
     path, meta = planner.search_multiple(
         start_cell, goal_cells
     )
```

### Comparing `pymultiastar-0.0.6/examples/run_scenarios.py` & `pymultiastar-0.0.7/examples/run_scenarios.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from pathlib import Path
 import typer
 import json
 import uuid
 import logging
-from pymultiastar.visualization.vis3d_helpers import visualize_plan
+from pymultiastar.visualization.vis3d_helpers import visualize_plan, plot_pareto
 from pymultiastar.geoplanner.helper import EnhancedJSONEncoder
 from rich.prompt import Prompt
 
 from pymultiastar.geoplanner import (
     GeoPlanner,
     Scenario,
     GPS,
@@ -20,14 +20,15 @@
 
 app = typer.Typer()
 THIS_DIR = Path(__file__).parent
 WORLD_DIR = Path(__file__).parent.parent / "tests" / "fixtures" / "world"
 ANNARBOR_PLAN = WORLD_DIR / "annarbor/plan.json"
 OUTPUT_DIR = THIS_DIR.parent / "output"
 
+
 def plan_scenario(scenario: Scenario, geo_planner: GeoPlanner):
     start_pos = GPS(*scenario["position"])
     if scenario.get("landing_sites") is None:
         raise NotImplementedError(
             "This module relies upon the user providing landing sites"
         )
     assert scenario["landing_sites"] is not None
@@ -46,31 +47,44 @@
 
     logger.debug("Start Pos: %s", start_pos)
     logger.debug("Landing Sites: %s", ls_list)
 
     result = geo_planner.plan_multi_goal(start_pos, ls_list)
     logger.debug("Plan Result: %s", result)
 
-    return dict(
-        start_gps=start_pos,
-        ls_list=ls_list,
-        geo_planner=geo_planner,
-        plan_results=result,
+    actions = [
+        (
+            "Show Pareto Plot",
+            lambda x: plot_pareto(
+                geo_planner, start_pos, ls_list, geo_planner.planner_kwargs.to_dict()
+            ),
+        )
+    ]
+
+    return (
+        dict(
+            start_gps=start_pos,
+            ls_list=ls_list,
+            geo_planner=geo_planner,
+            plan_results=result,
+        ),
+        actions,
     )
 
+
 @app.command()
 def run_city_plan(
     plan: Path = ANNARBOR_PLAN,
     log_level: LogLevel = typer.Option(
         LogLevel.INFO.value,
         help="Specify log level",
     ),
-    run_all_scenarios:bool = False,
-    visualize:bool = False,
-    output_dir:Path = OUTPUT_DIR
+    run_all_scenarios: bool = False,
+    visualize: bool = False,
+    output_dir: Path = OUTPUT_DIR,
 ):
     # set log level
     logger.setLevel(getattr(logging, log_level.value))
     logging.getLogger().setLevel(getattr(logging, log_level.value))
 
     # read planner data
     geo_planner, planner_data = create_planner_from_configuration(plan)
@@ -84,25 +98,27 @@
         scenario_str = Prompt.ask(
             "Choose a scenario",
             choices=[scenario["name"] for scenario in scenarios],
             default=scenarios[0]["name"],
         )
         scenario = next(item for item in scenarios if item["name"] == scenario_str)
         chosen_scenarios.append(scenario)
+    else:
+        chosen_scenarios = scenarios
 
     for scenario in chosen_scenarios:
-        scenario_result = plan_scenario(scenario, geo_planner)
-        scenario_results.append(scenario_result['plan_results'])
+        scenario_result, actions = plan_scenario(scenario, geo_planner)
+        scenario_results.append(scenario_result["plan_results"])
         if visualize:
-            visualize_plan(planner_data, scenario_result, xres=voxel_meta["xres"])
+            visualize_plan(
+                planner_data, scenario_result, xres=voxel_meta["xres"], actions=actions
+            )
 
-    file_name = planner_data.get('name', str(uuid.uuid4())) + ".json"
+    file_name = planner_data.get("name", str(uuid.uuid4())) + ".json"
     output_fp = output_dir / file_name
     logger.info("Writing file to %s", output_fp)
-    with open(output_fp, 'w') as fh:
+    with open(output_fp, "w") as fh:
         json.dump(scenario_results, fh, cls=EnhancedJSONEncoder, indent=2)
 
 
-
-
 if __name__ == "__main__":
     app()
```

### Comparing `pymultiastar-0.0.6/examples/run_simple_demo.py` & `pymultiastar-0.0.7/examples/run_simple_demo.py`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/mkdocs.yml` & `pymultiastar-0.0.7/mkdocs.yml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 site_name: "PyMultiAStar"
 site_description: "Multi-Goal A* with Heterogenous Values"
-site_url: "https://JeremyBYU.github.io/pymultiastar-cpp"
+site_url: "https://JeremyBYU.github.io/pymultiastar"
 repo_url: "https://github.com/JeremyBYU/pymultiastar"
 edit_uri: "blob/master/docs/"
 repo_name: "JeremyBYU/pymultiastar"
 watch: [README.md, src/]
 
 nav:
 - Home:
@@ -37,14 +37,18 @@
     scheme: slate
     primary: black
     accent: lime
     toggle:
       icon: material/weather-night
       name: Switch to light mode
 
+extra_javascript: 
+    - js/mathjaxhelper.js
+    - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js
+
 extra_css:
 - css/style.css
 - css/material.css
 - css/mkdocstrings.css
 
 markdown_extensions:
 - admonition
@@ -56,14 +60,16 @@
     check_paths: true
 - pymdownx.superfences
 - pymdownx.tabbed:
     alternate_style: true
 - pymdownx.tasklist
 - toc:
     permalink: "¤"
+# - mdx_math:
+#     enable_dollar_delimiter: True
 
 plugins:
 - search
 - markdown-exec
 - gen-files:
     scripts:
     - docs/gen_ref_nav.py
```

### Comparing `pymultiastar-0.0.6/pyproject.toml` & `pymultiastar-0.0.7/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "pymultiastar"
-version = "0.0.6"
+version = "0.0.7"
 description="Multi-goal A* with cpp bindings to python"
 readme = "README.md"
 authors = [
   { name = "Jeremy Castagno", email = "jeremybyu@gmail.com" },
 ]
 requires-python = ">=3.9"
 classifiers = [
@@ -22,22 +22,22 @@
 requires = ["scikit-build-core>=0.3.3", "pybind11"]
 build-backend = "scikit_build_core.build"
 
 [project.optional-dependencies]
 geo = ["pyproj>=3.0"]
 test = ["pytest", "Pillow", "pyproj>=3.0"]
 docs = ["mkdocstrings[python]", "mkdocs-autorefs>=0.3.1",
-      "pymdown-extensions>=6.3", "mkdocs>=1.3",
+      "pymdown-extensions>=6.3", "mkdocs>=1.3", "griffe>=0.27.5", "python-markdown-math",
       "mkdocs-coverage>=0.2", "mkdocs-gen-files>=0.3",
       "mkdocs-literate-nav>=0.4","mkdocs-material>=7.3",
       "mkdocs-section-index>=0.3", "mkdocstrings-python>=0.5.1",
       "markdown-callouts>=0.2","markdown-exec>=0.5"]
 
 dev = ["black", "open3d>=0.17", "matplotlib", 
-      "rich", "typer", "ipdb", "Pillow", 
+      "rich", "typer", "ipdb", "Pillow", "pandas", "seaborn",
       "pymultiastar[geo,test]"]
 
 
 [tool.scikit-build]
 wheel.expand-macos-universal-tags = true
 
 [tool.cibuildwheel]
```

### Comparing `pymultiastar-0.0.6/src/include/pymultiastar.hpp` & `pymultiastar-0.0.7/src/include/pymultiastar.hpp`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/src/main.cpp` & `pymultiastar-0.0.7/src/main.cpp`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/src/pymultiastar/_core.pyi` & `pymultiastar-0.0.7/src/pymultiastar/_core.pyi`

 * *Files 19% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 from typing import List, Tuple
 from .types import ArrayFloatMxNxK, CellPath, MultiPlannerResult, Cell
 
 __version__: str
 
 class PyMultiAStar(object):
     """
-    A planner that will search for **multiple** goals with **heterogenous** values 
+    A planner that will search for **multiple** goals with **heterogenous** values
     using a 3D A-star **discrete** planner.
     """
+
     def __init__(
         self,
         map: ArrayFloatMxNxK,
         allow_diag: bool = False,
         map_res: float = 2.0,
         obstacle_value: float = 1.0,
         normalizing_path_cost: float = 1.0,
@@ -19,15 +20,15 @@
         path_weight: float = 0.5,
         keep_nodes: bool = False,
         path_w0: float = 1.0,
     ) -> None:
         """Creates the multi-goal planner.
 
         Args:
-            map (ArrayFloatMxNxK): 3D NumPy array, often called the voxel grid. 
+            map (ArrayFloatMxNxK): 3D NumPy array, often called the voxel grid.
                                    index (i,j,k) corresponds to (y, x, z)
             allow_diag (bool, optional): Allows diagonal travel in map. Defaults to False.
             map_res (float, optional): The length (m) of an edge in the voxel grid. Defaults to 2.0.
             obstacle_value (float, optional): The value of an obstacle in the map. Defaults to 1.0.
             normalizing_path_cost (float, optional): The length and penalities of a path must
                                                     be normalized. This should generally be the
                                                     the longest path acceptable. Defaults to 1.0.
@@ -37,8 +38,33 @@
                                          may result in less dynamic memory allocations if many
                                          goals are being searched for. Defaults to False.
             path_w0 (float, optional): The path cost penalty multiplier when encountering
                                         a potential field. Defaults to 1.0.
         """
     def search_multiple(
         self, start_cell: Cell, goal_cells: List[Tuple[Cell, float]]
-    ) -> Tuple[CellPath, MultiPlannerResult]: ...
+    ) -> Tuple[CellPath, MultiPlannerResult]:
+        """Will search though the map finding the optimal goal/path pair.
+
+        Args:
+            start_cell (Cell): The start voxel cell in the map
+            goal_cells (List[Tuple[Cell, float]]): A list of goal cells and their 
+                                                   corresponding goal risk
+
+        Returns:
+            Tuple[CellPath, MultiPlannerResult]: The cell path and full planner results
+        """
+        ...
+
+    def search_single(
+        self, start_cell: Cell, goal_cells: Cell
+    ) -> Tuple[CellPath, float]:
+        """Single A* search
+
+        Args:
+            start_cell (Cell): Start Cell
+            goal_cells (Cell): End Cell
+
+        Returns:
+            Tuple[CellPath, float]: Path and Path Cost
+        """
+        ...
```

### Comparing `pymultiastar-0.0.6/src/pymultiastar/geoplanner/geoplanner.py` & `pymultiastar-0.0.7/src/pymultiastar/geoplanner/geoplanner.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from typing import List, Tuple, Optional
 from pathlib import Path
 import json
 
 import numpy as np
 from pyproj import Transformer
 
-from ..types import ArrayFloatMxNxK
+from ..types import ArrayFloatMxNxK, CellPath
 from .types import (PlannerKwargs, VoxelMeta, GPS, LandingSite, GeoMultiPlannerResult, Coord)
 from .helper import (
     convert_cost_map_to_float,
     prepare_planning_args_optimized,
     voxel_cell_to_projected,
     voxel_projected_to_cell,
     get_free_neighbor_cell,
@@ -190,15 +190,22 @@
     def transform_projected_to_zero_origin(self, coord:Coord) -> Coord:
         # import ipdb; ipdb.set_trace()
         x_meters = coord[0] - self.voxel_meta['xmin']
         y_meters = coord[1] - self.voxel_meta['ymin']
         z_meters = coord[2] - self.voxel_meta['zmin']
         
         return (x_meters, y_meters, z_meters)
-
+    
+    def search_single(self, start_position: GPS, ls:LandingSite) -> Optional[Tuple[CellPath, float]]:
+        result = self.plan_multi_goal(start_position, [ls])
+        if result is None:
+            return None
+        path_cost = result["goal_path_cost"]
+        path = result["path_cells"]
+        return (path, path_cost)
 
 
 def create_planner_from_configuration(plan: Path):
     with open(plan, "r") as fh:
         planner_data = json.load(fh)
     planner_data["cost_map_fp"] = plan.parent / planner_data["cost_map_fp"]
     voxel_meta: VoxelMeta = planner_data["voxel_meta"]
```

### Comparing `pymultiastar-0.0.6/src/pymultiastar/geoplanner/helper.py` & `pymultiastar-0.0.7/src/pymultiastar/geoplanner/helper.py`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/src/pymultiastar/geoplanner/types.py` & `pymultiastar-0.0.7/src/pymultiastar/geoplanner/types.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,91 +1,104 @@
 from dataclasses import dataclass, asdict, fields
 from typing import Dict, List, Tuple, TypedDict, Optional
 import numpy as np
-from ..types import ArrayFloatMxNxK, Cell, CellPath
+from ..types import ArrayFloatMxNxK, Coord, CoordRisk, CellPath
 
 
-Coord = Tuple[float, float, float]
 CoordPath = List[Coord]
 
-class SuperDataClass():
+
+class SuperDataClass:
     def to_dict(self) -> Dict:
         return asdict(self)
+
     @classmethod
     def from_dict(cls, dict_):
         class_fields = {f.name for f in fields(cls)}
-        return cls(**{k: v for k, v in dict_.items() if k in class_fields}) 
+        return cls(**{k: v for k, v in dict_.items() if k in class_fields})
+
 
 @dataclass
 class PlannerKwargs(SuperDataClass):
     allow_diag: bool = True
-    map_res:float = 2.0
-    obstacle_value:float = 1.0
-    normalizing_path_cost:float = 1.0
-    goal_weight:float = 0.5
+    map_res: float = 2.0
+    obstacle_value: float = 1.0
+    normalizing_path_cost: float = 1.0
+    goal_weight: float = 0.5
     path_weight: float = 0.5
     keep_nodes: bool = False
     path_w0: float = 1.0
 
+
 class Scenario(TypedDict):
-    name:str
-    details:Optional[str]
-    position: Coord # assumed to be in GPS!
+    name: str
+    details: Optional[str]
+    position: Coord  # assumed to be in GPS!
     active: Optional[bool]
     landing_sites: Optional[List[Dict]]
     planner_kwargs: Optional[Dict]
 
+
 class VoxelMeta(TypedDict):
-    srid:str
-    nrows:int
-    ncols:int
-    nslices:int
-    xres:float
-    yres:float
-    zres:float
-    xmin:float
-    ymin:float
-    zmin:float
+    srid: str
+    nrows: int
+    ncols: int
+    nslices: int
+    xres: float
+    yres: float
+    zres: float
+    xmin: float
+    ymin: float
+    zmin: float
+
 
 class Plan(TypedDict):
-    name:str
+    name: str
     cost_map_fp: str
     voxel_meta: VoxelMeta
     map_bbox: Optional[Dict]
     planner_kwargs: PlannerKwargs
     scenarios: List[Scenario]
+
+
 @dataclass
-class GPS():
+class GPS:
     lat: float
     lon: float
     alt: float = np.nan
 
     def to_array(self, always_xy=False) -> List:
         if always_xy:
             return [self.lon, self.lat, self.alt]
         else:
             return [self.lat, self.lon, self.alt]
 
     @staticmethod
-    def from_gps_string(centroid:str, alt=np.nan, reverse=False):
+    def from_gps_string(centroid: str, alt=np.nan, reverse=False):
         """Converts a lat-long string to a GPS object. Optionally handles height and projection"""
-        centroid_ = centroid.split(',')
+        centroid_ = centroid.split(",")
         # reverse lat,lon if necessary
         if reverse:
-            centroid_ = centroid_[::-1] 
+            centroid_ = centroid_[::-1]
         gps = GPS(float(centroid_[0]), float(centroid_[1]), alt=alt)
         return gps
 
+
 @dataclass
 class LandingSite(SuperDataClass):
     centroid: GPS
     "The centroid of the landing site in GPS coordinates"
     landing_site_risk: float
     "The normalized risk of this landing site [0-1]"
 
+    def __str__(self):
+        result = f"GPS: {self.centroid.lat:.4f}, {self.centroid.lon:.4f}, \
+{self.centroid.alt:.1f}; Risk: {self.landing_site_risk:.1f}"
+        return result
+
 
 class GeoMultiPlannerResult(TypedDict):
     start_position: GPS
     path_cells: CellPath
     path_projected: CoordPath
     path_projected_zero_origin: CoordPath
     path_length: float
@@ -93,8 +106,7 @@
     valid_landing_site_indices: List[int]
     goal_index: int
     total_goal_searches: int
     goal_total_cost: float
     goal_path_cost: float
     goal_value: float
     num_expansions: int
-
```

### Comparing `pymultiastar-0.0.6/src/pymultiastar/types.py` & `pymultiastar-0.0.7/src/pymultiastar/types.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,15 +1,21 @@
 from typing import List, Annotated, Literal, Tuple, TypedDict
 import numpy.typing as npt
 import numpy as np
-import logging
 from enum import Enum
 
+from typing import TypeVar
+
+T = TypeVar("T", float, int)
+
 ArrayFloatMxNxK = Annotated[npt.NDArray[np.float32], Literal["M", "N", "K"]]
-Cell = Tuple[int, int, int]
+Coord = Tuple[T, T, T]
+Cell = Coord[int]
+CoordRisk = Tuple[Coord[T], float]
+CoordPath = List[Coord]
 CellPath = List[Cell]
 
 class MultiPlannerResult(TypedDict):
     goal_index: int
     total_goal_searches: int
     goal_total_cost: float
     goal_path_cost: float
```

### Comparing `pymultiastar-0.0.6/src/pymultiastar/visualization/img2d_helpers.py` & `pymultiastar-0.0.7/src/pymultiastar/visualization/img2d_helpers.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,32 +1,39 @@
 import numpy as np
 from pathlib import Path
 from PIL import Image, ImageDraw
 import shutil
 from .log import logger
 
-def get_maze(img_path: Path, offset=3):
+
+from typing import TypedDict
+
+class MazeReturn(TypedDict):
+    img: np.ndarray
+    map: np.ndarray
+    normalizing_path_cost: float
+
+def get_maze(img_path: Path, offset=3) -> MazeReturn:
     """This will load an image of maze into a 3D numpy array
 
     Args:
         img_path (Path): Path to img holding maze
         offset (int, optional): Where to offset to start and finish. Defaults to 3.
 
     Returns:
-        dict: Returns a dictionary of maze data
+        MazeReturn: Returns a dictionary of maze data
     """
-    img = np.asarray(Image.open(img_path))
+    img:np.ndarray = np.asarray(Image.open(img_path))
     logger.debug(f"Maze name: {img_path.name}, Shape: {img.shape}")
     logger.debug(f"Unique values: {np.unique(img)}")
     # convert to float and an empty third dimension
-    img_f = np.expand_dims((img / np.max(img)).astype(np.float32), axis=2)
+    img_f:np.ndarray = np.expand_dims((img / np.max(img)).astype(np.float32), axis=2)
     # Best case scenario is a diagonal path, lets guess it will be 50% bigger
-    normalizing_path_cost = 1.5 * np.sqrt(img.shape[0] ** 2 + img.shape[1] ** 2)
-
-    return dict(
+    normalizing_path_cost:float = 1.5 * np.sqrt(img.shape[0] ** 2 + img.shape[1] ** 2)
+    return MazeReturn(
         img=img,
         map=img_f,
         normalizing_path_cost=normalizing_path_cost,
     )
 
 def write_path_to_maze(img_path: Path, path:np.array, width=1):
     """This will write the solution of the maze as a red line
```

### Comparing `pymultiastar-0.0.6/src/pymultiastar.cpp` & `pymultiastar-0.0.7/src/pymultiastar.cpp`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/maze_large.png` & `pymultiastar-0.0.7/tests/fixtures/maze_large.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/maze_small.png` & `pymultiastar-0.0.7/tests/fixtures/maze_small.png`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/world/annarbor/plan.json` & `pymultiastar-0.0.7/tests/fixtures/world/annarbor/plan.json`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/world/annarbor/voxel_map.npy` & `pymultiastar-0.0.7/tests/fixtures/world/annarbor/voxel_map.npy`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/world/newyork/plan.json` & `pymultiastar-0.0.7/tests/fixtures/world/newyork/plan.json`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/fixtures/world/newyork/voxel_map.npy` & `pymultiastar-0.0.7/tests/fixtures/world/newyork/voxel_map.npy`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/test_basic.py` & `pymultiastar-0.0.7/tests/test_basic.py`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/tests/test_geo_helper.py` & `pymultiastar-0.0.7/tests/test_geo_helper.py`

 * *Files identical despite different names*

### Comparing `pymultiastar-0.0.6/PKG-INFO` & `pymultiastar-0.0.7/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pymultiastar
-Version: 0.0.6
+Version: 0.0.7
 Summary: Multi-goal A* with cpp bindings to python
 Author-Email: Jeremy Castagno <jeremybyu@gmail.com>
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
@@ -14,14 +14,16 @@
 Requires-Dist: pytest; extra == "test"
 Requires-Dist: Pillow; extra == "test"
 Requires-Dist: pyproj>=3.0; extra == "test"
 Requires-Dist: mkdocstrings[python]; extra == "docs"
 Requires-Dist: mkdocs-autorefs>=0.3.1; extra == "docs"
 Requires-Dist: pymdown-extensions>=6.3; extra == "docs"
 Requires-Dist: mkdocs>=1.3; extra == "docs"
+Requires-Dist: griffe>=0.27.5; extra == "docs"
+Requires-Dist: python-markdown-math; extra == "docs"
 Requires-Dist: mkdocs-coverage>=0.2; extra == "docs"
 Requires-Dist: mkdocs-gen-files>=0.3; extra == "docs"
 Requires-Dist: mkdocs-literate-nav>=0.4; extra == "docs"
 Requires-Dist: mkdocs-material>=7.3; extra == "docs"
 Requires-Dist: mkdocs-section-index>=0.3; extra == "docs"
 Requires-Dist: mkdocstrings-python>=0.5.1; extra == "docs"
 Requires-Dist: markdown-callouts>=0.2; extra == "docs"
@@ -29,14 +31,16 @@
 Requires-Dist: black; extra == "dev"
 Requires-Dist: open3d>=0.17; extra == "dev"
 Requires-Dist: matplotlib; extra == "dev"
 Requires-Dist: rich; extra == "dev"
 Requires-Dist: typer; extra == "dev"
 Requires-Dist: ipdb; extra == "dev"
 Requires-Dist: Pillow; extra == "dev"
+Requires-Dist: pandas; extra == "dev"
+Requires-Dist: seaborn; extra == "dev"
 Requires-Dist: pymultiastar[geo,test]; extra == "dev"
 Provides-Extra: geo
 Provides-Extra: test
 Provides-Extra: docs
 Provides-Extra: dev
 Description-Content-Type: text/markdown
 
@@ -46,17 +50,17 @@
 
 **What do you mean by discrete?**
 
 The map provided should be a 3D voxel grid(i, j, k), a 3D NumPy array, which the planner searches. A cell with the value 0.0 is considered free space. A cell with the value 1.0 is considered an obstacle and cannot be traversed (this value is configurable). Values between 0.0 and 1.0 can be traversed but with a penalty (penalty weight is configurable).
 
 **What do you mean by multiple goals with heterogenous values?**
 
-A normal A-star planner has a start location and one goal. This Multi-Goal planner allows you to provide multiple goal cells each having different values. Goals with lower values are more desirable. This planner will try to find the optimal **goal** *and* **path** which minimizes an objective function. It must be understood that the planner doesn't just find a path. It finds the goal and the corresponding optimal path that minimizes some larger objective function. 
+A normal A-star planner has a start location and one goal. This Multi-Goal planner allows you to provide multiple goal cells each having different values. Goals with lower values are more desirable. This planner will try to find the optimal **goal** *and* **path** which minimizes an objective function. It must be understood that the planner doesn't just find a path. It finds the *one* goal and the corresponding optimal path that minimizes some larger objective function. 
 
-**What is the objective function?**
+**What is the larger objective function?**
 
 The objective function is the minimization of total risk ($r_t$), which is the combination of path risk ($r_p$) and goal risk $r_g$. In my research the goals were landing sites, therefore I called the latter landing site risk $r_l$. 
 Below is an excerpt from my paper that discusses this trade-off between objectives:
 
     The figure below shows an example Pareto frontier that minimizes two objectives: landing
     site risk and path risk. Each purple dot represents a landing site. The x-axis represents
     landing site risk and the y-axis represents path risk to that site. The green line
@@ -68,21 +72,35 @@
 
 $$
 r_t = w_l \cdot r_l + w_p · r_p
 $$
 
 ![Tradeoff](https://raw.githubusercontent.com/JeremyBYU/pymultiastar/master/assets/imgs/tradeoff.png)
 
-**What precisely are these two objectives and how do they relate to the planner?**
+Given the weighting between the two objectives, **one** of the purple dots on the green line is considered the "best" goal/path pair and will have minimum total risk. Here's the kicker though: you do **not** know the path risk *until* you do path planning. However, path planning is very expensive. PyMultiAStar will search for the optimal goal/path such that we minimize our expensive path planning procedures, often only needing to perform path planning 1-3 times on average.
+
+**How do you minimize path planning? How do you know when to stop searching?**
+
+We first sort the goals by their *minimum* total risk $r_{t,min}$ where
+
+$$r_{t,min} = w_{g} \cdot r_{g} + w_p \cdot  h(\mathbf{start}, \mathbf{goal}) / R$$
+
+where $h$ is an admissible heuristic and $R$ is a normalizing constant. Basically, we are bounding the minimum path distance which in turn bounds total risk. $R$ is usually the largest distance permissible during path planning. This entire list is very cheap to compute and sort.
+
+The first goal in this sorted list is the most *likely* to be the lowest total risk, but we don't know until we do path planning. After path planning to this goal, we can determine the **true** path risk and calculate the total risk. If the goal's total risk is less than the *next* goal's **minimum** total risk, we can guarantee we found the optimal solution to our objective function. We can stop searching! 
+
+**What precisely are these objectives and where are the details of the planner?**
 
 See the following sections in the paper linked above: 
 
-- Definition of Path **Cost**: Section 1.3.2, Equations 1.6-1.8
-- Definition of Path **Risk**: Section 1.5, Equation 1.17
-- Definition of Landing Site (Goal) **Risk**: Section 1.4.4, Equation 1.9
+- Definition of **Path Cost**: Section 1.3.2, Equations 1.6-1.8
+- Definition of **Path Risk**: Section 1.5, Equation 1.17
+- Definition of **Landing Site (Goal) Risk**: Section 1.4.4, Equation 1.9. This can be defined as anything for your specific problem.
+- Definition of **Total Risk**: Section 1.6.2, Equation 1.18. 
+- Proof of Planner: Section 1.6.3
 
 
 ## Install
 
 Binary Wheels are provided for you on `PyPi`:
 
 1. Discrete Multi-Goal Planner - `pip install pymultiastar` - This exposes the class `PyMultiAStar`
@@ -94,11 +112,7 @@
 ## How to use
 
 Below are some examples:
 
 1. `run_simple_world_3d.py`. Shows a very simple example of a small 3D world with multiple goals.
 2. `run_maze_2d.py` - Demonstrates that 2D A-star path planning is a subset of the Multi-Goal Planner. It loads a 2D image of a maze as a single slice in a 3D world and has only 1 goal. 
 3. `run_scenarios.py` - Shows how to use the GeoPlanner and plan in a 3D world.
-
-## Notes
-
-inside pymultiastar map data - (i,j,k) is the row, column, depth
```

