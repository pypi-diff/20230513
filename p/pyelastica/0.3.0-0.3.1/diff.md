# Comparing `tmp/pyelastica-0.3.0.tar.gz` & `tmp/pyelastica-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyelastica-0.3.0.tar", max compression
+gzip compressed data, was "pyelastica-0.3.1.tar", max compression
```

## Comparing `pyelastica-0.3.0.tar` & `pyelastica-0.3.1.tar`

### file list

```diff
@@ -1,58 +1,57 @@
--rw-r--r--   0        0        0     1072 2022-08-18 03:26:50.974325 pyelastica-0.3.0/LICENSE
--rw-r--r--   0        0        0     7747 2022-08-18 03:26:50.974325 pyelastica-0.3.0/README.md
--rw-r--r--   0        0        0      557 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/__init__.py
--rw-r--r--   0        0        0     9890 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/_calculus.py
--rw-r--r--   0        0        0      317 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/_elastica_numba.py
--rw-r--r--   0        0        0      247 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/_elastica_numpy.py
--rw-r--r--   0        0        0     9892 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/_linalg.py
--rw-r--r--   0        0        0    11793 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/_rotations.py
--rw-r--r--   0        0        0    28129 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/boundary_conditions.py
--rw-r--r--   0        0        0     8605 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/callback_functions.py
--rw-r--r--   0        0        0    11358 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/collision/AABBCollection.py
--rw-r--r--   0        0        0     9792 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/dissipation.py
--rw-r--r--   0        0        0        0 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/experimental/__init__.py
--rw-r--r--   0        0        0    15946 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/experimental/connection_contact_joint/generic_system_type_connection.py
--rw-r--r--   0        0        0     9642 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/experimental/connection_contact_joint/parallel_connection.py
--rw-r--r--   0        0        0     6171 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/experimental/interaction.py
--rw-r--r--   0        0        0    18933 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/external_forces.py
--rw-r--r--   0        0        0    36330 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/interaction.py
--rw-r--r--   0        0        0    38819 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/joint.py
--rw-r--r--   0        0        0      226 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/memory_block/__init__.py
--rw-r--r--   0        0        0     7773 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/memory_block/memory_block_rigid_body.py
--rw-r--r--   0        0        0    19865 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/memory_block/memory_block_rod.py
--rw-r--r--   0        0        0      517 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/__init__.py
--rw-r--r--   0        0        0     6517 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/base_system.py
--rw-r--r--   0        0        0     4726 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/callbacks.py
--rw-r--r--   0        0        0     9701 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/connections.py
--rw-r--r--   0        0        0     6646 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/constraints.py
--rw-r--r--   0        0        0     4170 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/damping.py
--rw-r--r--   0        0        0     5741 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/forcing.py
--rw-r--r--   0        0        0     1936 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/modules/memory_block.py
--rw-r--r--   0        0        0      210 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/reset_functions_for_block_structure/__init__.py
--rw-r--r--   0        0        0     1776 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/reset_functions_for_block_structure/_reset_ghost_vector_or_scalar.py
--rw-r--r--   0        0        0     2829 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/restart.py
--rw-r--r--   0        0        0      146 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rigidbody/__init__.py
--rw-r--r--   0        0        0     2967 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rigidbody/cylinder.py
--rw-r--r--   0        0        0    19355 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rigidbody/data_structures.py
--rw-r--r--   0        0        0     3001 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rigidbody/rigid_body.py
--rw-r--r--   0        0        0     2654 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rigidbody/sphere.py
--rw-r--r--   0        0        0      179 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/__init__.py
--rw-r--r--   0        0        0    31130 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/cosserat_rod.py
--rw-r--r--   0        0        0    19441 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/data_structures.py
--rw-r--r--   0        0        0    14251 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/factory_function.py
--rw-r--r--   0        0        0    28446 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/knot_theory.py
--rw-r--r--   0        0        0      595 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/rod/rod_base.py
--rw-r--r--   0        0        0     3485 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/systems/__init__.py
--rw-r--r--   0        0        0    16452 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/systems/analytical.py
--rw-r--r--   0        0        0     3835 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/timestepper/__init__.py
--rw-r--r--   0        0        0     2633 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/timestepper/_stepper_interface.py
--rw-r--r--   0        0        0     8009 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/timestepper/explicit_steppers.py
--rw-r--r--   0        0        0    10498 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/timestepper/symplectic_steppers.py
--rw-r--r--   0        0        0     5863 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/transformations.py
--rw-r--r--   0        0        0      184 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/typing.py
--rw-r--r--   0        0        0     5333 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/utils.py
--rw-r--r--   0        0        0       18 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/version.py
--rw-r--r--   0        0        0      570 2022-08-18 03:26:50.990325 pyelastica-0.3.0/elastica/wrappers.py
--rw-r--r--   0        0        0     3261 2022-08-18 03:26:50.998325 pyelastica-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     9627 2022-08-18 03:27:09.855790 pyelastica-0.3.0/setup.py
--rw-r--r--   0        0        0     9825 2022-08-18 03:27:09.856543 pyelastica-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1072 2023-05-12 22:18:14.329239 pyelastica-0.3.1/LICENSE
+-rw-r--r--   0        0        0     9625 2023-05-12 22:21:48.452892 pyelastica-0.3.1/README.md
+-rw-r--r--   0        0        0     2272 2023-05-12 22:18:14.332679 pyelastica-0.3.1/elastica/__init__.py
+-rw-r--r--   0        0        0     9877 2023-05-12 22:18:14.332807 pyelastica-0.3.1/elastica/_calculus.py
+-rw-r--r--   0        0        0     9879 2023-05-12 22:18:14.332934 pyelastica-0.3.1/elastica/_linalg.py
+-rw-r--r--   0        0        0    11780 2023-05-12 22:18:14.333063 pyelastica-0.3.1/elastica/_rotations.py
+-rw-r--r--   0        0        0     3505 2023-05-12 22:18:14.333284 pyelastica-0.3.1/elastica/_synchronize_periodic_boundary.py
+-rw-r--r--   0        0        0    27380 2023-05-12 22:18:14.333604 pyelastica-0.3.1/elastica/boundary_conditions.py
+-rw-r--r--   0        0        0     8541 2023-05-12 22:18:14.333749 pyelastica-0.3.1/elastica/callback_functions.py
+-rw-r--r--   0        0        0    11358 2022-05-30 02:18:59.374910 pyelastica-0.3.1/elastica/collision/AABBCollection.py
+-rw-r--r--   0        0        0    12044 2023-05-12 22:18:14.333890 pyelastica-0.3.1/elastica/dissipation.py
+-rw-r--r--   0        0        0        0 2022-05-30 02:18:59.375000 pyelastica-0.3.1/elastica/experimental/__init__.py
+-rw-r--r--   0        0        0    15823 2023-05-12 22:18:14.334053 pyelastica-0.3.1/elastica/experimental/connection_contact_joint/generic_system_type_connection.py
+-rw-r--r--   0        0        0     9642 2023-05-12 19:16:52.744915 pyelastica-0.3.1/elastica/experimental/connection_contact_joint/parallel_connection.py
+-rw-r--r--   0        0        0     5850 2023-05-12 22:18:14.334171 pyelastica-0.3.1/elastica/experimental/interaction.py
+-rw-r--r--   0        0        0    18842 2023-05-12 22:18:14.334323 pyelastica-0.3.1/elastica/external_forces.py
+-rw-r--r--   0        0        0    35996 2023-05-12 22:18:14.334677 pyelastica-0.3.1/elastica/interaction.py
+-rw-r--r--   0        0        0    39414 2023-05-12 22:18:14.334909 pyelastica-0.3.1/elastica/joint.py
+-rw-r--r--   0        0        0      111 2023-05-12 22:18:14.335015 pyelastica-0.3.1/elastica/memory_block/__init__.py
+-rw-r--r--   0        0        0     7515 2023-05-12 22:18:14.335246 pyelastica-0.3.1/elastica/memory_block/memory_block_rigid_body.py
+-rw-r--r--   0        0        0    27041 2023-05-12 22:18:14.335399 pyelastica-0.3.1/elastica/memory_block/memory_block_rod.py
+-rw-r--r--   0        0        0     7761 2023-05-12 22:18:14.335506 pyelastica-0.3.1/elastica/memory_block/memory_block_rod_base.py
+-rw-r--r--   0        0        0      390 2023-05-12 22:18:14.335613 pyelastica-0.3.1/elastica/modules/__init__.py
+-rw-r--r--   0        0        0     7657 2023-05-12 22:18:14.335859 pyelastica-0.3.1/elastica/modules/base_system.py
+-rw-r--r--   0        0        0     4726 2023-05-12 19:16:52.746366 pyelastica-0.3.1/elastica/modules/callbacks.py
+-rw-r--r--   0        0        0     9701 2023-05-12 19:16:52.746449 pyelastica-0.3.1/elastica/modules/connections.py
+-rw-r--r--   0        0        0     6627 2023-05-12 22:18:14.336039 pyelastica-0.3.1/elastica/modules/constraints.py
+-rw-r--r--   0        0        0     4170 2023-05-12 19:16:52.746631 pyelastica-0.3.1/elastica/modules/damping.py
+-rw-r--r--   0        0        0     5741 2023-05-12 19:16:52.746734 pyelastica-0.3.1/elastica/modules/forcing.py
+-rw-r--r--   0        0        0     2345 2023-05-12 22:18:14.336315 pyelastica-0.3.1/elastica/modules/memory_block.py
+-rw-r--r--   0        0        0      141 2023-05-12 22:18:14.336422 pyelastica-0.3.1/elastica/reset_functions_for_block_structure/__init__.py
+-rw-r--r--   0        0        0     1744 2023-05-12 22:18:14.336537 pyelastica-0.3.1/elastica/reset_functions_for_block_structure/_reset_ghost_vector_or_scalar.py
+-rw-r--r--   0        0        0     3002 2023-05-12 22:18:14.336771 pyelastica-0.3.1/elastica/restart.py
+-rw-r--r--   0        0        0       96 2023-05-12 22:18:14.336874 pyelastica-0.3.1/elastica/rigidbody/__init__.py
+-rw-r--r--   0        0        0     2944 2023-05-12 22:18:14.336989 pyelastica-0.3.1/elastica/rigidbody/cylinder.py
+-rw-r--r--   0        0        0    19346 2023-05-12 22:18:14.337174 pyelastica-0.3.1/elastica/rigidbody/data_structures.py
+-rw-r--r--   0        0        0     2945 2023-05-12 22:18:14.337381 pyelastica-0.3.1/elastica/rigidbody/rigid_body.py
+-rw-r--r--   0        0        0     2633 2023-05-12 22:18:14.337509 pyelastica-0.3.1/elastica/rigidbody/sphere.py
+-rw-r--r--   0        0        0      296 2023-05-12 22:18:14.337616 pyelastica-0.3.1/elastica/rod/__init__.py
+-rw-r--r--   0        0        0    34821 2023-05-12 22:18:14.337947 pyelastica-0.3.1/elastica/rod/cosserat_rod.py
+-rw-r--r--   0        0        0    19271 2023-05-12 22:18:14.338115 pyelastica-0.3.1/elastica/rod/data_structures.py
+-rw-r--r--   0        0        0    14848 2023-05-12 22:18:14.338430 pyelastica-0.3.1/elastica/rod/factory_function.py
+-rw-r--r--   0        0        0    28315 2023-05-12 22:18:14.338609 pyelastica-0.3.1/elastica/rod/knot_theory.py
+-rw-r--r--   0        0        0      595 2022-05-30 02:18:59.380183 pyelastica-0.3.1/elastica/rod/rod_base.py
+-rw-r--r--   0        0        0     3485 2023-05-12 19:16:52.747260 pyelastica-0.3.1/elastica/systems/__init__.py
+-rw-r--r--   0        0        0    16240 2023-05-12 22:18:14.338799 pyelastica-0.3.1/elastica/systems/analytical.py
+-rw-r--r--   0        0        0     3699 2023-05-12 22:18:14.338910 pyelastica-0.3.1/elastica/timestepper/__init__.py
+-rw-r--r--   0        0        0     2613 2023-05-12 22:18:14.339019 pyelastica-0.3.1/elastica/timestepper/_stepper_interface.py
+-rw-r--r--   0        0        0     8009 2022-05-30 02:18:59.381378 pyelastica-0.3.1/elastica/timestepper/explicit_steppers.py
+-rw-r--r--   0        0        0    10486 2023-05-12 22:18:14.339147 pyelastica-0.3.1/elastica/timestepper/symplectic_steppers.py
+-rw-r--r--   0        0        0     5800 2023-05-12 22:18:14.339259 pyelastica-0.3.1/elastica/transformations.py
+-rw-r--r--   0        0        0      184 2023-05-12 19:16:52.747449 pyelastica-0.3.1/elastica/typing.py
+-rw-r--r--   0        0        0     5314 2023-05-12 22:18:14.339377 pyelastica-0.3.1/elastica/utils.py
+-rw-r--r--   0        0        0       18 2023-05-12 22:18:14.339477 pyelastica-0.3.1/elastica/version.py
+-rw-r--r--   0        0        0      572 2023-05-12 22:18:14.339573 pyelastica-0.3.1/elastica/wrappers.py
+-rw-r--r--   0        0        0     3150 2023-05-12 22:18:14.352002 pyelastica-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0    11829 1970-01-01 00:00:00.000000 pyelastica-0.3.1/PKG-INFO
```

### Comparing `pyelastica-0.3.0/LICENSE` & `pyelastica-0.3.1/LICENSE`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2019-2022 GazzolaLab
+Copyright (c) 2019-2023 GazzolaLab
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `pyelastica-0.3.0/README.md` & `pyelastica-0.3.1/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -1,59 +1,90 @@
 <div align='center'>
 <h1> PyElastica </h1>
 
-[![Build_status][badge-travis]][link-travis] [![CI][badge-CI]][link-CI] [![Documentation Status][badge-docs-status]][link-docs-status] [![codecov][badge-codecov]][link-codecov] [![Downloads][badge-pepy-download-count]][link-pepy-download-count] [![Binder][badge-binder]][link-binder] [![Gitter][badge-gitter]][link-gitter]
+[![Build_status][badge-travis]][link-travis] [![CI][badge-CI]][link-CI] [![Documentation Status][badge-docs-status]][link-docs-status] [![codecov][badge-codecov]][link-codecov] [![Downloads][badge-pepy-download-count]][link-pepy-download-count] [![DOI][badge-doi]][link-doi] [![Binder][badge-binder]][link-binder] [![Gitter][badge-gitter]][link-gitter]
  </div>
- 
+
 PyElastica is the python implementation of **Elastica**: an *open-source* project for simulating assemblies of slender, one-dimensional structures using Cosserat Rod theory.
 
 [![gallery][link-readme-gallary]][link-project-website]
 
 Visit [cosseratrods.org][link-project-website] for more information and learn about Elastica and Cosserat rod theory.
 
-## How to Start 
+## How to Start
 [![PyPI version][badge-pypi]][link-pypi] [![Documentation Status][badge-docs-status]][link-docs-status]
 
-PyElastica is compatible with Python 3.7 - 3.10.
+PyElastica is compatible with Python 3.8 - 3.10.
 
 ~~~bash
-$ pip install pyelastica 
+$ pip install pyelastica
 ~~~
 
+With this you get a minimal version with very little dependencies.
+
+All options:
+- `magnetism`: use this if you want to simulate magnetic Cosserat rods
+interacting with external magnetic environments (details can be found [here](https://github.com/armantekinalp/MagnetoPyElastica)) .
+- `examples`: installs dependencies to run example cases,
+found under the folder `examples`.
+- `docs`: packages to build documentation
+
+Options can be combined e.g.
+```bash
+pip install "pyelastica[magnetism,examples,docs]"
+```
+
 Documentation of PyElastica is available [here][link-docs-website].
 
+Example cases for simulating magnetic Cosserat rods can be found [here](https://github.com/armantekinalp/MagnetoPyElastica).
 ## Citation
 
 We ask that any publications which use Elastica cite as following:
 
 ```
-@misc{tekinalp2022pyelastica,
-  title={PyElastica: A computational framework for Cosserat rod assemblies},
-  author={Tekinalp, Arman and Kim, Seung Hyun and Parthasarathy, Tejaswin and Bhosale, Yashraj},
-  journal={https://github.com/GazzolaLab/PyElastica},
-  year={2022},
-  publisher={GitHub}
+@software{arman_tekinalp_2023_7931429,
+  author       = {Arman Tekinalp and
+                  Seung Hyun Kim and
+                  Yashraj Bhosale and
+                  Tejaswin Parthasarathy and
+                  Noel Naughton and
+                  Ilia Nasiriziba and
+                  Songyuan Cui and
+                  Maximilian Stölzle and
+                  Chia-Hsien (Cathy) Shih and
+                  Mattia Gazzola
+                  },
+  title        = {GazzolaLab/PyElastica: v0.3.1},
+  month        = may,
+  year         = 2023,
+  publisher    = {Zenodo},
+  version      = {v0.3.1},
+  doi          = {10.5281/zenodo.7931429},
+  url          = {https://doi.org/10.5281/zenodo.7931429}
 }
 ```
 
 <details>
   <summary><h4>References</h4></summary>
- 
+
 - Gazzola, Dudte, McCormick, Mahadevan, <strong>Forward and inverse problems in the mechanics of soft filaments</strong>, Royal Society Open Science, 2018. doi: [10.1098/rsos.171628](https://doi.org/10.1098/rsos.171628)
 - Zhang, Chan, Parthasarathy, Gazzola, <strong>Modeling and simulation of complex dynamic musculoskeletal architectures</strong>, Nature Communications, 2019. doi: [10.1038/s41467-019-12759-5](https://doi.org/10.1038/s41467-019-12759-5)
 
 </details>
 
 ## List of publications and submissions
-
-- [Control-oriented modeling of bend propagation in an octopus arm](https://arxiv.org/abs/2110.07211) (UIUC, 2021)
+- [Topology, dynamics, and control of an octopus-analog muscular hydrostat](https://arxiv.org/abs/2304.08413) (UIUC, 2023)
+- [Hierarchical control and learning of a foraging CyberOctopus](https://arxiv.org/abs/2302.05811) (UIUC, 2023)
+- [Energy-shaping control of a muscular octopus arm moving in three dimensions](https://royalsocietypublishing.org/doi/full/10.1098/rspa.2022.0593) (UIUC, 2023) (Proceedings of the Royal Society A 2023)
+- [A sensory feedback control law for octopus arm movements](https://ieeexplore.ieee.org/abstract/document/9993021/) (UIUC, 2022) (IEEE CDC 2022)
+- [Control-oriented modeling of bend propagation in an octopus arm](https://ieeexplore.ieee.org/abstract/document/9867689/) (UIUC, 2021) (IEEE ACC 2022)
 - [A physics-informed, vision-based method to reconstruct all deformation modes in slender bodies](https://arxiv.org/abs/2109.08372) (UIUC, 2021) (IEEE ICRA 2022) [code](https://github.com/GazzolaLab/BR2-vision-based-smoothing)
-- [Optimal control of a soft CyberOctopus arm](https://ieeexplore.ieee.org/document/9483284) (UIUC, 2021) (ACC 2021)
+- [Optimal control of a soft CyberOctopus arm](https://ieeexplore.ieee.org/document/9483284) (UIUC, 2021) (IEEE ACC 2021)
 - [Elastica: A compliant mechanics environment for soft robotic control](https://ieeexplore.ieee.org/document/9369003) (UIUC, 2021) (IEEE RA-L 2021)
-- [Controlling a CyberOctopus soft arm with muscle-like actuation](https://arxiv.org/abs/2010.03368) (UIUC, 2020)
+- [Controlling a CyberOctopus soft arm with muscle-like actuation](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9683318) (UIUC, 2020) (IEEE CDC 2021)
 - [Energy shaping control of a CyberOctopus soft arm](https://ieeexplore.ieee.org/document/9304408) (UIUC, 2020) (IEEE CDC 2020)
 
 ## Tutorials
 [![Binder][badge-binder-tutorial]][link-binder]
 
 We have created several Jupyter notebooks and Python scripts to help users get started with PyElastica. The Jupyter notebooks are available on Binder, allowing you to try out some of the tutorials without having to install PyElastica.
 
@@ -66,16 +97,18 @@
 PyElastica is developed by the [Gazzola Lab][link-lab-website] at the University of Illinois at Urbana-Champaign.
 
 ## Senior Developers ✨
 _Names arranged alphabetically_
 - Arman Tekinalp
 - Chia-Hsien Shih (Cathy)
 - Fan Kiat Chan
+- Ilia Nasiriziba
 - Noel Naughton
 - [Seung Hyun Kim](https://github.com/skim0119)
+- Songyuan Cui
 - Tejaswin Parthasarathy (Teja)
 - [Yashraj Bhosale](https://github.com/bhosale2)
 
 [//]: # (Collection of URLs.)
 
 [link-readme-gallary]: https://github.com/skim0119/PyElastica/blob/assets_logo/assets/alpha_gallery.gif
 
@@ -87,17 +120,19 @@
 [badge-travis]: https://travis-ci.com/GazzolaLab/PyElastica.svg?branch=master
 [badge-CI]: https://github.com/GazzolaLab/PyElastica/workflows/CI/badge.svg
 [badge-docs-status]: https://readthedocs.org/projects/pyelastica/badge/?version=latest
 [badge-binder]: https://mybinder.org/badge_logo.svg
 [badge-pepy-download-count]: https://pepy.tech/badge/pyelastica
 [badge-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica/branch/master/graph/badge.svg
 [badge-gitter]: https://badges.gitter.im/PyElastica/community.svg
+[badge-doi]: https://zenodo.org/badge/254172891.svg
 [link-pypi]: https://badge.fury.io/py/pyelastica
 [link-travis]: https://travis-ci.com/github/GazzolaLab/PyElastica
 [link-CI]: https://github.com/GazzolaLab/PyElastica/actions
 [link-docs-status]: https://docs.cosseratrods.org/en/latest/?badge=latest
 [link-pepy-download-count]: https://pepy.tech/project/pyelastica
 [link-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica
 
 [badge-binder-tutorial]: https://img.shields.io/badge/Launch-PyElastica%20Tutorials-579ACA.svg?logo=data:image/png;base64,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
 [link-binder]: https://mybinder.org/v2/gh/GazzolaLab/PyElastica/master?filepath=examples%2FBinder%2F0_PyElastica_Tutorials_Overview.ipynb
 [link-gitter]: https://gitter.im/PyElastica/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
+[link-doi]: https://zenodo.org/badge/latestdoi/254172891
```

### Comparing `pyelastica-0.3.0/elastica/_calculus.py` & `pyelastica-0.3.1/elastica/_calculus.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 __doc__ = """ Quadrature and difference kernels """
 import numpy as np
 from numpy import zeros, empty
-import numba
 from numba import njit
 from elastica.reset_functions_for_block_structure._reset_ghost_vector_or_scalar import (
     _reset_vector_ghost,
 )
 import functools
```

### Comparing `pyelastica-0.3.0/elastica/_linalg.py` & `pyelastica-0.3.1/elastica/_linalg.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 __doc__ = """ Convenient linear algebra kernels """
 import numpy as np
-import numba
 from numba import njit
 from numpy import sqrt
 import functools
 from itertools import permutations
 from elastica.utils import perm_parity
```

### Comparing `pyelastica-0.3.0/elastica/_rotations.py` & `pyelastica-0.3.1/elastica/_rotations.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,14 @@
 
 import numpy as np
 from numpy import sin
 from numpy import cos
 from numpy import sqrt
 from numpy import arccos
 
-import numba
 from numba import njit
 
 from elastica._linalg import _batch_matmul
 
 
 @njit(cache=True)
 def _get_rotation_matrix(scale: float, axis_collection):
```

### Comparing `pyelastica-0.3.0/elastica/boundary_conditions.py` & `pyelastica-0.3.1/elastica/boundary_conditions.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,32 +1,21 @@
 __doc__ = """ Built-in boundary condition implementationss """
-__all__ = [
-    "ConstraintBase",
-    "FreeBC",
-    "OneEndFixedBC",
-    "GeneralConstraint",
-    "FixedConstraint",
-    "HelicalBucklingBC",
-]
 
 import warnings
-from typing import Optional, Type, Union
+from typing import Optional
 
 import numpy as np
 
 from abc import ABC, abstractmethod
 
-import numba
 from numba import njit
 
 from elastica._linalg import _batch_matvec, _batch_matrix_transpose
 from elastica._rotations import _get_rotation_matrix
-from elastica.rod import RodBase
-from elastica.rigidbody import RigidBodyBase
-from elastica.typing import SystemType
+from elastica.typing import SystemType, RodType
 
 
 class ConstraintBase(ABC):
     """Base class for constraint and displacement boundary condition implementation.
 
     Notes
     -----
@@ -37,15 +26,15 @@
         ----------
         system : RodBase or RigidBodyBase
         node_indices : None or numpy.ndarray
         element_indices : None or numpy.ndarray
 
     """
 
-    _system: Union[Type[RodBase], Type[RigidBodyBase]]
+    _system: SystemType
     _constrained_position_idx: np.ndarray
     _constrained_director_idx: np.ndarray
 
     def __init__(self, *args, **kwargs):
         """Initialize boundary condition"""
         try:
             self._system = kwargs["_system"]
@@ -57,15 +46,15 @@
             )
         except KeyError:
             raise KeyError(
                 "Please use simulator.constrain(...).using(...) syntax to establish constraint."
             )
 
     @property
-    def system(self) -> Union[Type[RodBase], Type[RigidBodyBase]]:
+    def system(self) -> SystemType:
         """get system (rod or rigid body) reference"""
         return self._system
 
     @property
     def constrained_position_idx(self) -> Optional[np.ndarray]:
         """get position-indices passed to "using" """
         # TODO: This should be immutable somehow
@@ -74,41 +63,37 @@
     @property
     def constrained_director_idx(self) -> Optional[np.ndarray]:
         """get director-indices passed to "using" """
         # TODO: This should be immutable somehow
         return self._constrained_director_idx
 
     @abstractmethod
-    def constrain_values(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_values(self, system: SystemType, time: float) -> None:
         # TODO: In the future, we can remove rod and use self.system
         """
         Constrain values (position and/or directors) of a rod object.
 
         Parameters
         ----------
-        rod : Union[Type[RodBase], Type[RigidBodyBase]]
+        system : SystemType
             Rod or rigid-body object.
         time : float
             The time of simulation.
         """
         pass
 
     @abstractmethod
-    def constrain_rates(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_rates(self, system: SystemType, time: float) -> None:
         # TODO: In the future, we can remove rod and use self.system
         """
         Constrain rates (velocity and/or omega) of a rod object.
 
         Parameters
         ----------
-        rod : Union[Type[RodBase], Type[RigidBodyBase]]
+        system : SystemType
             Rod or rigid-body object.
         time : float
             The time of simulation.
 
         """
         pass
 
@@ -117,23 +102,19 @@
     """
     Boundary condition template.
     """
 
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
 
-    def constrain_values(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_values(self, system: SystemType, time: float) -> None:
         """In FreeBC, this routine simply passes."""
         pass
 
-    def constrain_rates(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_rates(self, system: SystemType, time: float) -> None:
         """In FreeBC, this routine simply passes."""
         pass
 
 
 class FreeRod(FreeBC):
     # Please clear this part beyond version 0.3.0
     """Deprecated 0.2.1: Same implementation as FreeBC"""
@@ -174,34 +155,30 @@
         constrained_director_idx : tuple
             Tuple of director-indices that will be constrained
         """
         super().__init__(**kwargs)
         self.fixed_position_collection = np.array(fixed_position)
         self.fixed_directors_collection = np.array(fixed_directors)
 
-    def constrain_values(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
-        # rod.position_collection[..., 0] = self.fixed_position
-        # rod.director_collection[..., 0] = self.fixed_directors
+    def constrain_values(self, system: SystemType, time: float) -> None:
+        # system.position_collection[..., 0] = self.fixed_position
+        # system.director_collection[..., 0] = self.fixed_directors
         self.compute_constrain_values(
-            rod.position_collection,
+            system.position_collection,
             self.fixed_position_collection,
-            rod.director_collection,
+            system.director_collection,
             self.fixed_directors_collection,
         )
 
-    def constrain_rates(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
-        # rod.velocity_collection[..., 0] = 0.0
-        # rod.omega_collection[..., 0] = 0.0
+    def constrain_rates(self, system: SystemType, time: float) -> None:
+        # system.velocity_collection[..., 0] = 0.0
+        # system.omega_collection[..., 0] = 0.0
         self.compute_constrain_rates(
-            rod.velocity_collection,
-            rod.omega_collection,
+            system.velocity_collection,
+            system.omega_collection,
         )
 
     @staticmethod
     @njit(cache=True)
     def compute_constrain_values(
         position_collection,
         fixed_position_collection,
@@ -266,15 +243,15 @@
     Constraining position is equivalent to setting 0 translational DOF.
     Constraining director is equivalent to setting 0 rotational DOF.
 
     Examples
     --------
     How to fix all translational and rotational dof except allowing twisting around the z-axis in an inertial frame:
 
-    >>> simulator.constrain(rod).using(
+    >>> simulator.constrain(system).using(
     ...    GeneralConstraint,
     ...    constrained_position_idx=(0,),
     ...    constrained_director_idx=(0,),
     ...    translational_constraint_selector=np.array([True, True, True]),
     ...    rotational_constraint_selector=np.array([True, True, False]),
     ... )
 
@@ -500,15 +477,15 @@
     ...    constrained_director_idx=(0,-1)
     ... )
 
     How to pin the middle of the rod (10th node), without constraining the rotational DOF.
 
     >>> simulator.constrain(rod).using(
     ...    FixedConstraint,
-    ...    constrained_position_idx=(10)
+    ...    constrained_position_idx=(10,)
     ... )
 
     See Also
     --------
     GeneralConstraint: Generalized constraint with configurable DOF.
     """
 
@@ -527,41 +504,37 @@
         super().__init__(
             *args,
             translational_constraint_selector=np.array([True, True, True]),
             rotational_constraint_selector=np.array([True, True, True]),
             **kwargs,
         )
 
-    def constrain_values(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_values(self, system: SystemType, time: float) -> None:
         if self.constrained_position_idx.size:
             self.nb_constrain_translational_values(
-                rod.position_collection,
+                system.position_collection,
                 self.fixed_positions,
                 self.constrained_position_idx,
             )
         if self.constrained_director_idx.size:
             self.nb_constraint_rotational_values(
-                rod.director_collection,
+                system.director_collection,
                 self.fixed_directors,
                 self.constrained_director_idx,
             )
 
-    def constrain_rates(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_rates(self, system: SystemType, time: float) -> None:
         if self.constrained_position_idx.size:
             self.nb_constrain_translational_rates(
-                rod.velocity_collection,
+                system.velocity_collection,
                 self.constrained_position_idx,
             )
         if self.constrained_director_idx.size:
             self.nb_constrain_rotational_rates(
-                rod.omega_collection,
+                system.omega_collection,
                 self.constrained_director_idx,
             )
 
     @staticmethod
     @njit(cache=True)
     def nb_constraint_rotational_values(
         director_collection, fixed_director_collection, indices
@@ -741,27 +714,23 @@
             @ director_start
         )  # rotation_matrix wants vectors 3,1
         self.final_end_directors = (
             _get_rotation_matrix(-theta, direction.reshape(3, 1)).reshape(3, 3)
             @ director_end
         )  # rotation_matrix wants vectors 3,1
 
-    def constrain_values(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_values(self, rod: RodType, time: float) -> None:
         if time > self.twisting_time:
             rod.position_collection[..., 0] = self.final_start_position
             rod.position_collection[..., -1] = self.final_end_position
 
             rod.director_collection[..., 0] = self.final_start_directors
             rod.director_collection[..., -1] = self.final_end_directors
 
-    def constrain_rates(
-        self, rod: Union[Type[RodBase], Type[RigidBodyBase]], time: float
-    ) -> None:
+    def constrain_rates(self, rod: RodType, time: float) -> None:
         if time > self.twisting_time:
             rod.velocity_collection[..., 0] = 0.0
             rod.omega_collection[..., 0] = 0.0
 
             rod.velocity_collection[..., -1] = 0.0
             rod.omega_collection[..., -1] = 0.0
```

### Comparing `pyelastica-0.3.0/elastica/callback_functions.py` & `pyelastica-0.3.1/elastica/callback_functions.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 __doc__ = """ Module contains callback classes to save simulation data for rod-like objects """
-__all__ = ["CallBackBaseClass", "MyCallBack", "ExportCallBack"]
 
 import os
 import sys
 import numpy as np
 import logging
 
 from collections import defaultdict
```

### Comparing `pyelastica-0.3.0/elastica/collision/AABBCollection.py` & `pyelastica-0.3.1/elastica/collision/AABBCollection.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/experimental/connection_contact_joint/generic_system_type_connection.py` & `pyelastica-0.3.1/elastica/experimental/connection_contact_joint/generic_system_type_connection.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,12 @@
 __doc__ = (
     """ Module containing joint classes to connect rods and rigid bodies together. """
 )
-__all__ = ["GenericSystemTypeFreeJoint", "GenericSystemTypeFixedJoint"]
 from elastica.joint import FreeJoint, FixedJoint
 from elastica.typing import SystemType
-from elastica.utils import Tolerance, MaxDimension
 import numpy as np
 from typing import Optional
 
 # Experimental implementation for `joint` modules: #122 #149
 #   - Enable the joint between `rod` and `rigid-body`
 #   - Allow joint to form offset from the node/COM
 #   - Generalized version for joint system
```

### Comparing `pyelastica-0.3.0/elastica/experimental/connection_contact_joint/parallel_connection.py` & `pyelastica-0.3.1/elastica/experimental/connection_contact_joint/parallel_connection.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/experimental/interaction.py` & `pyelastica-0.3.1/elastica/experimental/interaction.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,36 +1,22 @@
 __doc__ = """ Experimental interaction implementation."""
-__all__ = [
-    "AnisotropicFrictionalPlaneRigidBody",
-]
 
 
 import numpy as np
 from elastica.external_forces import NoForces
-from elastica.interaction import *
 from elastica.interaction import (
     find_slipping_elements,
     apply_normal_force_numba_rigid_body,
     InteractionPlaneRigidBody,
 )
 
-import numba
 from numba import njit
 from elastica._linalg import (
-    _batch_matmul,
-    _batch_matvec,
-    _batch_cross,
-    _batch_norm,
     _batch_dot,
-    _batch_product_i_k_to_ik,
-    _batch_product_i_ik_to_k,
     _batch_product_k_ik_to_ik,
-    _batch_vector_sum,
-    _batch_matrix_transpose,
-    _batch_vec_oneD_vec_cross,
 )
 
 
 class AnisotropicFrictionalPlaneRigidBody(NoForces, InteractionPlaneRigidBody):
     def __init__(
         self,
         k,
```

### Comparing `pyelastica-0.3.0/elastica/external_forces.py` & `pyelastica-0.3.1/elastica/external_forces.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,23 +1,16 @@
-__doc__ = """ Numba implementation module for boundary condition implementations that apply external forces to the rod."""
-__all__ = [
-    "NoForces",
-    "GravityForces",
-    "EndpointForces",
-    "UniformTorques",
-    "UniformForces",
-    "MuscleTorques",
-    "EndpointForcesSinusoidal",
-]
+__doc__ = """ Numba implementation module for boundary condition implementations that apply
+external forces to the system."""
+
 
 import numpy as np
 from elastica._linalg import _batch_matvec
+from elastica.typing import SystemType, RodType
 from elastica.utils import _bspline
 
-import numba
 from numba import njit
 from elastica._linalg import _batch_product_i_k_to_ik
 
 
 class NoForces:
     """
     This is the base class for external forcing boundary conditions applied to rod-like objects.
@@ -31,43 +24,41 @@
 
     def __init__(self):
         """
         NoForces class does not need any input parameters.
         """
         pass
 
-    def apply_forces(self, system, time: np.float64 = 0.0):
+    def apply_forces(self, system: SystemType, time: np.float64 = 0.0):
         """Apply forces to a rod-like object.
 
         In NoForces class, this routine simply passes.
 
         Parameters
         ----------
-        system : object
-            System that is Rod-like.
+        system : SystemType
+            Rod or rigid-body object
         time : float
             The time of simulation.
 
         Returns
         -------
 
-
         """
-
         pass
 
-    def apply_torques(self, system, time: np.float64 = 0.0):
+    def apply_torques(self, system: SystemType, time: np.float64 = 0.0):
         """Apply torques to a rod-like object.
 
         In NoForces class, this routine simply passes.
 
         Parameters
         ----------
-        system : object
-            System that is Rod-like.
+        system : SystemType
+            Rod or rigid-body object
         time : float
             The time of simulation.
 
         Returns
         -------
 
         """
@@ -93,15 +84,15 @@
         acc_gravity: numpy.ndarray
             1D (dim) array containing data with 'float' type. Gravitational acceleration vector.
 
         """
         super(GravityForces, self).__init__()
         self.acc_gravity = acc_gravity
 
-    def apply_forces(self, system, time=0.0):
+    def apply_forces(self, system: SystemType, time=0.0):
         self.compute_gravity_forces(
             self.acc_gravity, system.mass, system.external_forces
         )
 
     @staticmethod
     @njit(cache=True)
     def compute_gravity_forces(acc_gravity, mass, external_forces):
@@ -128,44 +119,44 @@
 class EndpointForces(NoForces):
     """
     This class applies constant forces on the endpoint nodes.
 
         Attributes
         ----------
         start_force: numpy.ndarray
-            1D (dim) array containing data with 'float' type. Force applied to first node of the rod-like object.
+            1D (dim) array containing data with 'float' type. Force applied to first node of the system.
         end_force: numpy.ndarray
-            1D (dim) array containing data with 'float' type. Force applied to last node of the rod-like object.
+            1D (dim) array containing data with 'float' type. Force applied to last node of the system.
         ramp_up_time: float
             Applied forces are ramped up until ramp up time.
 
     """
 
     def __init__(self, start_force, end_force, ramp_up_time):
         """
 
         Parameters
         ----------
         start_force: numpy.ndarray
             1D (dim) array containing data with 'float' type.
-            Force applied to first node of the rod-like object.
+            Force applied to first node of the system.
         end_force: numpy.ndarray
             1D (dim) array containing data with 'float' type.
-            Force applied to last node of the rod-like object.
+            Force applied to last node of the system.
         ramp_up_time: float
             Applied forces are ramped up until ramp up time.
 
         """
         super(EndpointForces, self).__init__()
         self.start_force = start_force
         self.end_force = end_force
         assert ramp_up_time > 0.0
         self.ramp_up_time = ramp_up_time
 
-    def apply_forces(self, system, time=0.0):
+    def apply_forces(self, system: SystemType, time=0.0):
         self.compute_end_point_forces(
             system.external_forces,
             self.start_force,
             self.end_force,
             time,
             self.ramp_up_time,
         )
@@ -182,15 +173,15 @@
         ----------
         external_forces: numpy.ndarray
             2D (dim, blocksize) array containing data with 'float' type. External force vector.
         start_force: numpy.ndarray
             1D (dim) array containing data with 'float' type.
         end_force: numpy.ndarray
             1D (dim) array containing data with 'float' type.
-            Force applied to last node of the rod-like object.
+            Force applied to last node of the system.
         time: float
         ramp_up_time: float
             Applied forces are ramped up until ramp up time.
 
         Returns
         -------
 
@@ -221,15 +212,15 @@
         direction: numpy.ndarray
             1D (dim) array containing data with 'float' type.
             Direction in which torque applied.
         """
         super(UniformTorques, self).__init__()
         self.torque = torque * direction
 
-    def apply_torques(self, system, time: np.float64 = 0.0):
+    def apply_torques(self, system: SystemType, time: np.float64 = 0.0):
         n_elems = system.n_elems
         torque_on_one_element = (
             _batch_product_i_k_to_ik(self.torque, np.ones((n_elems))) / n_elems
         )
         system.external_torques += _batch_matvec(
             system.director_collection, torque_on_one_element
         )
@@ -255,22 +246,22 @@
         direction: numpy.ndarray
             1D (dim) array containing data with 'float' type.
             Direction in which force applied.
         """
         super(UniformForces, self).__init__()
         self.force = (force * direction).reshape(3, 1)
 
-    def apply_forces(self, system, time: np.float64 = 0.0):
-        force_on_one_element = self.force / system.n_elems
+    def apply_forces(self, rod: RodType, time: np.float64 = 0.0):
+        force_on_one_element = self.force / rod.n_elems
 
-        system.external_forces += force_on_one_element
+        rod.external_forces += force_on_one_element
 
         # Because mass of first and last node is half
-        system.external_forces[..., 0] -= 0.5 * force_on_one_element[:, 0]
-        system.external_forces[..., -1] -= 0.5 * force_on_one_element[:, 0]
+        rod.external_forces[..., 0] -= 0.5 * force_on_one_element[:, 0]
+        rod.external_forces[..., -1] -= 0.5 * force_on_one_element[:, 0]
 
 
 class MuscleTorques(NoForces):
     """
     This class applies muscle torques along the body. The applied muscle torques are treated
     as applied external forces. This class can apply
     muscle torques as a traveling wave with a beta spline or only
@@ -368,26 +359,26 @@
                 -------
 
                 """
                 return np.ones(input.shape)
 
             self.my_spline = constant_function(self.s)
 
-    def apply_torques(self, system, time: np.float64 = 0.0):
+    def apply_torques(self, rod: RodType, time: np.float64 = 0.0):
         self.compute_muscle_torques(
             time,
             self.my_spline,
             self.s,
             self.angular_frequency,
             self.wave_number,
             self.phase_shift,
             self.ramp_up_time,
             self.direction,
-            system.director_collection,
-            system.external_torques,
+            rod.director_collection,
+            rod.external_torques,
         )
 
     @staticmethod
     @njit(cache=True)
     def compute_muscle_torques(
         time,
         my_spline,
@@ -508,39 +499,39 @@
         normal_direction=np.array([0, 1, 0]),
     ):
         """
 
         Parameters
         ----------
         start_force_mag: float
-            Magnitude of the force that is applied to the start of the rod (node 0).
+            Magnitude of the force that is applied to the start of the system (node 0).
         end_force_mag: float
-            Magnitude of the force that is applied to the end of the rod (node -1).
+            Magnitude of the force that is applied to the end of the system (node -1).
         ramp_up_time: float
             Applied muscle torques are ramped up until ramp up time.
         tangent_direction: np.ndarray
             An array (3,) contains type float.
-            This is the tangent direction of the rod, or normal of the plane that forces applied.
+            This is the tangent direction of the system, or normal of the plane that forces applied.
         normal_direction: np.ndarray
             An array (3,) contains type float.
-            This is the normal direction of the rod.
+            This is the normal direction of the system.
         """
         super(EndpointForcesSinusoidal, self).__init__()
         # Start force
         self.start_force_mag = start_force_mag
         self.end_force_mag = end_force_mag
 
         # Applied force directions
         self.normal_direction = normal_direction
         self.roll_direction = np.cross(normal_direction, tangent_direction)
 
         assert ramp_up_time >= 0.0
         self.ramp_up_time = ramp_up_time
 
-    def apply_forces(self, system, time=0.0):
+    def apply_forces(self, system: SystemType, time=0.0):
 
         if time < self.ramp_up_time:
             # When time smaller than ramp up time apply the force in normal direction
             # First pull the rod upward or downward direction some time.
             start_force = -2.0 * self.start_force_mag * self.normal_direction
             end_force = -2.0 * self.end_force_mag * self.normal_direction
```

### Comparing `pyelastica-0.3.0/elastica/interaction.py` & `pyelastica-0.3.1/elastica/interaction.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,8 @@
 __doc__ = """ Numba implementation module containing interactions between a rod and its environment."""
-__all__ = [
-    "AnisotropicFrictionalPlane",
-    "InteractionPlane",
-    "InteractionPlaneRigidBody",
-    "SlenderBodyTheory",
-]
 
 
 import numpy as np
 from elastica.external_forces import NoForces
 
 
 from numba import njit
@@ -20,15 +14,14 @@
     _batch_product_i_k_to_ik,
     _batch_product_i_ik_to_k,
     _batch_product_k_ik_to_ik,
     _batch_vector_sum,
     _batch_matrix_transpose,
     _batch_vec_oneD_vec_cross,
 )
-import warnings
 
 
 @njit(cache=True)
 def find_slipping_elements(velocity_slip, velocity_threshold):
     """
     This function takes the velocity of elements and checks if they are larger than the threshold velocity.
     If the velocity of elements is larger than threshold velocity, that means those elements are slipping.
@@ -103,24 +96,20 @@
     output[..., 0] += 0.5 * input[..., 0]
     output[..., -1] += 0.5 * input[..., -1]
 
     return output
 
 
 def nodes_to_elements(input):
-    warnings.warn(
-        # Change the warning to error on v0.3.1
-        # Remove the function beyond v0.4.0
-        "This function is now deprecated (issue #80). Please use "
-        "elastica.interaction.node_to_element_mass_or_force() "
-        "instead for node-to-element interpolation of mass/forces. "
-        "The function will be removed in the future (v0.3.1).",
-        DeprecationWarning,
+    # Remove the function beyond v0.4.0
+    raise NotImplementedError(
+        "This function is removed in v0.3.1. Please use\n"
+        "elastica.interaction.node_to_element_mass_or_force()\n"
+        "instead for node-to-element interpolation of mass/forces."
     )
-    return node_to_element_mass_or_force(input)
 
 
 @njit(cache=True)
 def elements_to_nodes_inplace(vector_in_element_frame, vector_in_node_frame):
     """
     Updating nodal forces using the forces computed on elements
     Parameters
```

### Comparing `pyelastica-0.3.0/elastica/joint.py` & `pyelastica-0.3.1/elastica/joint.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 __doc__ = """ Module containing joint classes to connect multiple rods together. """
-__all__ = ["FreeJoint", "HingeJoint", "FixedJoint", "ExternalContact", "SelfContact"]
+
 from elastica._linalg import _batch_product_k_ik_to_ik
 from elastica._rotations import _inv_rotate
+from elastica.typing import SystemType, RodType
 from math import sqrt
 import numba
 import numpy as np
 
 
 class FreeJoint:
     """
@@ -39,65 +40,69 @@
         nu: float
            Damping coefficient of the joint.
 
         """
         self.k = k
         self.nu = nu
 
-    def apply_forces(self, rod_one, index_one, rod_two, index_two):
+    def apply_forces(
+        self, system_one: SystemType, index_one, system_two: SystemType, index_two
+    ):
         """
         Apply joint force to the connected rod objects.
 
         Parameters
         ----------
-        rod_one : object
-            Rod-like object
+        system_one : object
+            Rod or rigid-body object
         index_one : int
             Index of first rod for joint.
-        rod_two : object
-            Rod-like object
+        system_two : object
+            Rod or rigid-body object
         index_two : int
             Index of second rod for joint.
 
         Returns
         -------
 
         """
         end_distance_vector = (
-            rod_two.position_collection[..., index_two]
-            - rod_one.position_collection[..., index_one]
+            system_two.position_collection[..., index_two]
+            - system_one.position_collection[..., index_one]
         )
         elastic_force = self.k * end_distance_vector
 
         relative_velocity = (
-            rod_two.velocity_collection[..., index_two]
-            - rod_one.velocity_collection[..., index_one]
+            system_two.velocity_collection[..., index_two]
+            - system_one.velocity_collection[..., index_one]
         )
         damping_force = self.nu * relative_velocity
 
         contact_force = elastic_force + damping_force
-        rod_one.external_forces[..., index_one] += contact_force
-        rod_two.external_forces[..., index_two] -= contact_force
+        system_one.external_forces[..., index_one] += contact_force
+        system_two.external_forces[..., index_two] -= contact_force
 
         return
 
-    def apply_torques(self, rod_one, index_one, rod_two, index_two):
+    def apply_torques(
+        self, system_one: SystemType, index_one, system_two: SystemType, index_two
+    ):
         """
         Apply restoring joint torques to the connected rod objects.
 
         In FreeJoint class, this routine simply passes.
 
         Parameters
         ----------
-        rod_one : object
-            Rod-like object
+        system_one : object
+            Rod or rigid-body object
         index_one : int
             Index of first rod for joint.
-        rod_two : object
-            Rod-like object
+        system_two : object
+            Rod or rigid-body object
         index_two : int
             Index of second rod for joint.
 
         Returns
         -------
 
         """
@@ -145,18 +150,30 @@
         # unitize the normal vector
         self.normal_direction = normal_direction / np.linalg.norm(normal_direction)
         # additional in-plane constraint through restoring torque
         # stiffness of the restoring constraint -- tuned empirically
         self.kt = kt
 
     # Apply force is same as free joint
-    def apply_forces(self, system_one, index_one, system_two, index_two):
+    def apply_forces(
+        self,
+        system_one: SystemType,
+        index_one,
+        system_two: SystemType,
+        index_two,
+    ):
         return super().apply_forces(system_one, index_one, system_two, index_two)
 
-    def apply_torques(self, system_one, index_one, system_two, index_two):
+    def apply_torques(
+        self,
+        system_one: SystemType,
+        index_one,
+        system_two: SystemType,
+        index_two,
+    ):
         # current tangent direction of the `index_two` element of system two
         system_two_tangent = system_two.director_collection[2, :, index_two]
 
         # projection of the tangent of system two onto the plane normal
         force_direction = (
             -np.dot(system_two_tangent, self.normal_direction) * self.normal_direction
         )
@@ -233,18 +250,30 @@
         #  are available in the __init__
         if rest_rotation_matrix is None:
             rest_rotation_matrix = np.eye(3)
         assert rest_rotation_matrix.shape == (3, 3), "Rest rotation matrix must be 3x3"
         self.rest_rotation_matrix = rest_rotation_matrix
 
     # Apply force is same as free joint
-    def apply_forces(self, rod_one, index_one, rod_two, index_two):
-        return super().apply_forces(rod_one, index_one, rod_two, index_two)
+    def apply_forces(
+        self,
+        system_one: SystemType,
+        index_one,
+        system_two: SystemType,
+        index_two,
+    ):
+        return super().apply_forces(system_one, index_one, system_two, index_two)
 
-    def apply_torques(self, system_one, index_one, system_two, index_two):
+    def apply_torques(
+        self,
+        system_one: SystemType,
+        index_one,
+        system_two: SystemType,
+        index_two,
+    ):
         # collect directors of systems one and two
         # note that systems can be either rods or rigid bodies
         system_one_director = system_one.director_collection[..., index_one]
         system_two_director = system_two.director_collection[..., index_two]
 
         # rel_rot: C_12 = C_1I @ C_I2
         # C_12 is relative rotation matrix from system 1 to system 2
@@ -279,47 +308,52 @@
         torque = self.kt * rot_vec_inertial_frame - self.nut * dev_omega
 
         # The opposite torques will be applied to system one and two after rotating the torques into the local frame
         system_one.external_torques[..., index_one] -= system_one_director @ torque
         system_two.external_torques[..., index_two] += system_two_director @ torque
 
 
-def get_relative_rotation_two_systems(system_one, index_one, system_two, index_two):
+def get_relative_rotation_two_systems(
+    system_one: SystemType,
+    index_one,
+    system_two: SystemType,
+    index_two,
+):
     """
     Compute the relative rotation matrix C_12 between system one and system two at the specified elements.
 
     Examples
     ----------
     How to get the relative rotation between two systems (e.g. the rotation from end of rod one to base of rod two):
 
-        >>> rel_rot_mat = get_relative_rotation_two_systems(rod1, -1, rod2, 0)
+        >>> rel_rot_mat = get_relative_rotation_two_systems(system1, -1, system2, 0)
 
     How to initialize a FixedJoint with a rest rotation between the two systems,
     which is enforced throughout the simulation:
 
         >>> simulator.connect(
-        ...    first_rod=rod1, second_rod=rod2, first_connect_idx=-1, second_connect_idx=0
+        ...    first_rod=system1, second_rod=system2, first_connect_idx=-1, second_connect_idx=0
         ... ).using(
         ...    FixedJoint,
         ...    ku=1e6, nu=0.0, kt=1e3, nut=0.0,
-        ...    rest_rotation_matrix=get_relative_rotation_two_systems(rod1, -1, rod2, 0)
+        ...    rest_rotation_matrix=get_relative_rotation_two_systems(system1, -1, system2, 0)
         ... )
 
     See Also
     ---------
     FixedJoint
 
     Parameters
     ----------
-    rod_one : object
-        Rod-like object
+    system_one : SystemType
+        Rod or rigid-body object
     index_one : int
         Index of first rod for joint.
-    rod_two : object
-        Rod-like object
+    system_two : SystemType
+        Rod or rigid-body object
     index_two : int
         Index of second rod for joint.
 
     Returns
     -------
     relative_rotation_matrix : np.array
         Relative rotation matrix C_12 between the two systems for their current state.
@@ -917,15 +951,21 @@
         friction_coefficient : float
             For Coulombic friction coefficient for rigid-body and rod contact.
         """
         super().__init__(k, nu)
         self.velocity_damping_coefficient = velocity_damping_coefficient
         self.friction_coefficient = friction_coefficient
 
-    def apply_forces(self, rod_one, index_one, rod_two, index_two):
+    def apply_forces(
+        self,
+        rod_one: RodType,
+        index_one,
+        rod_two: SystemType,
+        index_two,
+    ):
         # del index_one, index_two
 
         # TODO: raise error during the initialization if rod one is rigid body.
 
         # If rod two has one element, then it is rigid body.
         if rod_two.n_elems == 1:
             cylinder_two = rod_two
@@ -1015,15 +1055,15 @@
     This class is modeling self contact of rod.
 
     """
 
     def __init__(self, k, nu):
         super().__init__(k, nu)
 
-    def apply_forces(self, rod_one, index_one, rod_two, index_two):
+    def apply_forces(self, rod_one: RodType, index_one, rod_two: SystemType, index_two):
         # del index_one, index_two
 
         _calculate_contact_forces_self_rod(
             rod_one.position_collection[
                 ..., :-1
             ],  # Discount last node, we want element start position
             rod_one.radius,
```

### Comparing `pyelastica-0.3.0/elastica/memory_block/memory_block_rigid_body.py` & `pyelastica-0.3.1/elastica/memory_block/memory_block_rigid_body.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,28 +1,22 @@
 __doc__ = """Create block-structure class for collection of rigid body systems."""
 import numpy as np
-from typing import Sequence
+from typing import Sequence, List
 
-from elastica.rigidbody import RigidBodyBase, Cylinder
-
-# from elastica.rigidbody.rigid_body import RigidBody
+from elastica.rigidbody import RigidBodyBase
 from elastica.rigidbody.data_structures import _RigidRodSymplecticStepperMixin
-from elastica.rod.data_structures import _RodSymplecticStepperMixin
-from elastica.reset_functions_for_block_structure import _reset_scalar_ghost
-from elastica.rod.cosserat_rod import CosseratRod
-from elastica.rigidbody import sphere, cylinder
-from elastica._linalg import _batch_matvec, _batch_cross
 
 
 class MemoryBlockRigidBody(RigidBodyBase, _RigidRodSymplecticStepperMixin):
-    def __init__(self, systems: Sequence):
+    def __init__(self, systems: Sequence, system_idx_list: List[int]):
 
         self.n_bodies = len(systems)
         self.n_elems = self.n_bodies
         self.n_nodes = self.n_elems
+        self.system_idx_list = np.array(system_idx_list, dtype=np.int64)
 
         # Allocate block structure using system collection.
         self.allocate_block_variables_scalars(systems)
         self.allocate_block_variables_vectors(systems)
         self.allocate_block_variables_matrix(systems)
         self.allocate_block_variables_for_symplectic_stepper(systems)
```

### Comparing `pyelastica-0.3.0/elastica/memory_block/memory_block_rod.py` & `pyelastica-0.3.1/elastica/memory_block/memory_block_rod.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,80 +1,75 @@
 __doc__ = """Create block-structure class for collection of Cosserat rod systems."""
 import numpy as np
 from typing import Sequence
-
+from elastica.memory_block.memory_block_rod_base import (
+    MemoryBlockRodBase,
+    make_block_memory_metadata,
+    make_block_memory_periodic_boundary_metadata,
+)
 from elastica.rod.data_structures import _RodSymplecticStepperMixin
 from elastica.reset_functions_for_block_structure import _reset_scalar_ghost
-from elastica.rod.cosserat_rod import CosseratRod
-
-
-def make_block_memory_metadata(n_elems_in_rods):
-    """
-    This function, takes number of elements of each rod as an numpy array and computes,
-    ghost nodes, elements and voronoi element indexes and numbers and returns it.
-
-    Parameters
-    ----------
-    n_elems_in_rods
-
-    Returns
-    -------
-
-    """
-    n_nodes_in_rods = n_elems_in_rods + 1
-    n_voronois_in_rods = n_elems_in_rods - 1
-
-    n_rods = n_elems_in_rods.shape[0]
-
-    # Gap between two rods have one ghost node
-    # n_nodes_with_ghosts = np.sum(n_nodes_in_rods) + (n_rods - 1)
-    # Gap between two rods have two ghost elements : comes out to n_nodes_with_ghosts - 1
-    n_elems_with_ghosts = np.sum(n_elems_in_rods) + 2 * (n_rods - 1)
-    # Gap between two rods have three ghost voronois : comes out to n_nodes_with_ghosts - 2
-    # n_voronoi_with_ghosts = np.sum(n_voronois_in_rods) + 3 * (n_rods - 1)
-
-    # To be nulled
-    ghost_nodes_idx = np.zeros(((n_rods - 1),), dtype=np.int64)
-    ghost_nodes_idx[:] = n_nodes_in_rods[:-1]
-    ghost_nodes_idx = np.cumsum(ghost_nodes_idx)
-    # Add [0, 1, 2, ... n_rods-2] to the ghost_nodes idx to accommodate miscounting
-    ghost_nodes_idx += np.arange(0, n_rods - 1, dtype=np.int64)
-
-    ghost_elems_idx = np.zeros((2 * (n_rods - 1),), dtype=np.int64)
-    ghost_elems_idx[::2] = n_elems_in_rods[:-1]
-    ghost_elems_idx[1::2] = 1
-    ghost_elems_idx = np.cumsum(ghost_elems_idx)
-    # Add [0, 0, 1, 1, 2, 2, ... n_rods-2, n_rods-2] to the ghost_elems idx to accommodate miscounting
-    ghost_elems_idx += np.repeat(np.arange(0, n_rods - 1, dtype=np.int64), 2)
-
-    ghost_voronoi_idx = np.zeros((3 * (n_rods - 1),), dtype=np.int64)
-    ghost_voronoi_idx[::3] = n_voronois_in_rods[:-1]
-    ghost_voronoi_idx[1::3] = 1
-    ghost_voronoi_idx[2::3] = 1
-    ghost_voronoi_idx = np.cumsum(ghost_voronoi_idx)
-    # Add [0, 0, 0, 1, 1, 1, 2, 2, 2, ... n_rods-2, n_rods-2, n_rods-2] to the ghost_voronoi idx
-    # to accommodate miscounting
-    ghost_voronoi_idx += np.repeat(np.arange(0, n_rods - 1, dtype=np.int64), 3)
-
-    return n_elems_with_ghosts, ghost_nodes_idx, ghost_elems_idx, ghost_voronoi_idx
+from elastica.rod.cosserat_rod import (
+    CosseratRod,
+    _compute_sigma_kappa_for_blockstructure,
+)
+from elastica._synchronize_periodic_boundary import (
+    _synchronize_periodic_boundary_of_vector_collection,
+    _synchronize_periodic_boundary_of_scalar_collection,
+    _synchronize_periodic_boundary_of_matrix_collection,
+)
 
 
-class MemoryBlockCosseratRod(CosseratRod, _RodSymplecticStepperMixin):
+class MemoryBlockCosseratRod(
+    MemoryBlockRodBase, CosseratRod, _RodSymplecticStepperMixin
+):
     """
     Memory block class for Cosserat rod equations. This class is derived from Cosserat Rod class in order to inherit
     the methods of Cosserat rod class. This class takes the cosserat rod object (systems) and creates big
     arrays to store the system data and returns a reference of that data to the systems.
     Thus each system is now in contiguous memory, so it is faster to compute Cosserat rod equations.
 
     TODO: need more documentation!
     """
 
-    def __init__(self, systems: Sequence):
+    def __init__(self, systems: Sequence, system_idx_list):
+
+        # separate straight and ring rods
+        system_straight_rod = []
+        system_ring_rod = []
+        system_idx_list_ring_rod = []
+        system_idx_list_straight_rod = []
+        for k, system_to_be_added in enumerate(systems):
+
+            if system_to_be_added.ring_rod_flag:
+                system_ring_rod.append(system_to_be_added)
+                system_idx_list_ring_rod.append(system_idx_list[k])
+                self.ring_rod_flag = True
+            else:
+                system_straight_rod.append(system_to_be_added)
+                system_idx_list_straight_rod.append(system_idx_list[k])
+
+        # Sorted systems
+        systems = system_straight_rod + system_ring_rod
+        self.system_idx_list = np.array(
+            system_idx_list_straight_rod + system_idx_list_ring_rod, dtype=np.int64
+        )
+
+        n_elems_straight_rods = np.array(
+            [x.n_elems for x in system_straight_rod], dtype=np.int64
+        )
+        n_elems_ring_rods = np.array(
+            [x.n_elems for x in system_ring_rod], dtype=np.int64
+        )
 
-        self.n_elems_in_rods = np.array([x.n_elems for x in systems], dtype=np.int64)
+        n_straight_rods = len(system_straight_rod)
+        n_ring_rods = len(system_ring_rod)
+
+        # self.n_elems_in_rods = np.array([x.n_elems for x in systems], dtype=np.int)
+        self.n_elems_in_rods = np.hstack((n_elems_straight_rods, n_elems_ring_rods + 2))
         self.n_rods = len(systems)
         (
             self.n_elems,
             self.ghost_nodes_idx,
             self.ghost_elems_idx,
             self.ghost_voronoi_idx,
         ) = make_block_memory_metadata(self.n_elems_in_rods)
@@ -93,26 +88,134 @@
         self.start_idx_in_rod_elems = np.hstack((0, self.ghost_elems_idx[1::2] + 1))
         self.end_idx_in_rod_elems = np.hstack((self.ghost_elems_idx[::2], self.n_elems))
         self.start_idx_in_rod_voronoi = np.hstack((0, self.ghost_voronoi_idx[2::3] + 1))
         self.end_idx_in_rod_voronoi = np.hstack(
             (self.ghost_voronoi_idx[::3], self.n_voronoi)
         )
 
+        # Periodic boundaries are only used if there is a ring rod present in the simulation, otherwise below
+        # arrays are empty.
+        (
+            _,
+            self.periodic_boundary_nodes_idx,
+            self.periodic_boundary_elems_idx,
+            self.periodic_boundary_voronoi_idx,
+        ) = make_block_memory_periodic_boundary_metadata(n_elems_ring_rods)
+
+        """
+        If there are ring rods appended to simulation, then start and end idx of rod nodes, elements and voronoi
+        have to be updated, to accommodate the periodic boundaries. Periodic boundaries can only accessed by
+        memory block  and rods does not have access to periodic boundaries.
+        """
+        if n_ring_rods != 0:
+            """
+            Number of nodes, elements and voronoi of the ring rod is same. When user wants to access to the rod, they
+            will also see that. However, in order to be compatible with block structure implementation, it has to be
+            n_nodes=n_elems+1 and n_voronoi=n_elems-1. Thus, we add these periodic nodes, element and voronoi at the
+            end of the rod. We need 3 periodic nodes,  2 periodic elements and 1 periodic voronoi.
+            Below you will see some magic numbers such as 1, 2, and 3. These are related with the number of periodic
+            nodes, element and voronoi.
+            For example if user sets 50 elements for one ring rod with 50 elements then we need two periodic element
+            at the start and end of the rod. So there are total of 52 elements on memory block including periodic ones.
+            In our numerical method n_nodes=n_elems+1 and n_voronoi=n_elems-1 so there are 53 nodes and 51 voronoi.
+            This requires 3 additional periodic nodes and 1 additional periodic voronoi. We add one of this periodic
+            node at the start of the rod and two at the end of the rod.
+
+            So below magic number 3 is coming from having extra 3 periodic nodes for each ring rod.
+                self.start_idx_in_rod_nodes[:] = (
+                    self.periodic_boundary_nodes_idx[0, 0::3] + 1
+                )
+
+            Same idea is used for elements and voronoi as well.
+            """
+            if n_straight_rods != 0:
+                # Here the idea of adding ghost nodes, elems and voronoi of straight rods is that, in memory block
+                # we place first straight rods, then ring rods.
+                # TODO: in future consider a better implementation for packing problem.
+                # +1 is because we want to start from next idx, where periodic boundary starts
+                self.periodic_boundary_nodes_idx += (
+                    self.ghost_nodes_idx[n_straight_rods - 1] + 1
+                )
+                self.periodic_boundary_elems_idx += (
+                    self.ghost_elems_idx[1::2][n_straight_rods - 1] + 1
+                )
+                self.periodic_boundary_voronoi_idx += (
+                    self.ghost_voronoi_idx[2::3][n_straight_rods - 1] + 1
+                )
+
+                # Compute the start and end of the rod nodes again. This time, boundary cells are added.
+                self.start_idx_in_rod_nodes[n_straight_rods:] = (
+                    self.periodic_boundary_nodes_idx[0, 0::3] + 1
+                )
+                self.end_idx_in_rod_nodes[
+                    n_straight_rods:
+                ] = self.periodic_boundary_nodes_idx[0, 1::3]
+
+                self.start_idx_in_rod_elems[n_straight_rods:] = (
+                    self.periodic_boundary_elems_idx[0, 0::2] + 1
+                )
+                self.end_idx_in_rod_elems[
+                    n_straight_rods:
+                ] = self.periodic_boundary_elems_idx[0, 1::2]
+
+                self.start_idx_in_rod_voronoi[n_straight_rods:] = (
+                    self.periodic_boundary_voronoi_idx[0, :] + 1
+                )
+            else:
+                # Compute the start and end of the rod nodes again. This time, boundary cells are added.
+                self.start_idx_in_rod_nodes[:] = (
+                    self.periodic_boundary_nodes_idx[0, 0::3] + 1
+                )
+                self.end_idx_in_rod_nodes[:] = self.periodic_boundary_nodes_idx[0, 1::3]
+
+                self.start_idx_in_rod_elems[:] = (
+                    self.periodic_boundary_elems_idx[0, 0::2] + 1
+                )
+                self.end_idx_in_rod_elems[:] = self.periodic_boundary_elems_idx[0, 1::2]
+
+                self.start_idx_in_rod_voronoi[:] = (
+                    self.periodic_boundary_voronoi_idx[0, :] + 1
+                )
+
         # Allocate block structure using system collection.
         self.allocate_block_variables_in_nodes(systems)
         self.allocate_block_variables_in_elements(systems)
         self.allocate_blocks_variables_in_voronoi(systems)
         self.allocate_blocks_variables_for_symplectic_stepper(systems)
 
         # Reset ghosts of mass, rest length and rest voronoi length to 1. Otherwise
         # since ghosts are not modified, this causes a division by zero error.
         _reset_scalar_ghost(self.mass, self.ghost_nodes_idx, 1.0)
         _reset_scalar_ghost(self.rest_lengths, self.ghost_elems_idx, 1.0)
         _reset_scalar_ghost(self.rest_voronoi_lengths, self.ghost_voronoi_idx, 1.0)
 
+        # Compute strains for the block
+        _compute_sigma_kappa_for_blockstructure(self)
+
+        # If n_elems_with_boundary defined and passed with kwargs, then this rod is ring and we need to know
+        # how many boundary elements is rod containing.
+        if n_ring_rods != 0:
+            for sys_idx, system_to_be_added in enumerate(system_ring_rod):
+                if np.count_nonzero(system_to_be_added.rest_sigma) == 0:
+                    # Ring rod has to have non-zero rest sigma. If user did not set something, then Elastica will
+                    # calculate it.
+                    system_to_be_added.rest_sigma[:] = system_to_be_added.sigma[:]
+                if np.count_nonzero(system_to_be_added.rest_kappa) == 0:
+                    # Ring rod has to have non-zero rest kappa. If user did not set something, then Elastica will
+                    # calculate it.
+                    system_to_be_added.rest_kappa[:] = system_to_be_added.kappa[:]
+
+            # We update periodic elements and voronoi because they are used in difference and trapezoidal kernels.
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.rest_sigma, self.periodic_boundary_elems_idx
+            )
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.rest_kappa, self.periodic_boundary_voronoi_idx
+            )
+
         # Initialize the mixin class for symplectic time-stepper.
         _RodSymplecticStepperMixin.__init__(self)
 
     def allocate_block_variables_in_nodes(self, systems: Sequence):
         """
         This function takes system collection and allocates the variables on
         node for block-structure and references allocated variables back to the
@@ -125,18 +228,15 @@
         Returns
         -------
 
         """
 
         # Things in nodes that are scalars
         #             0 ("mass", float64[:]),
-        map_scalar_dofs_in_rod_nodes = {
-            "mass": 0,
-            "dissipation_constant_for_forces": 1,
-        }
+        map_scalar_dofs_in_rod_nodes = {"mass": 0}
         self.scalar_dofs_in_rod_nodes = np.zeros(
             (len(map_scalar_dofs_in_rod_nodes), self.n_nodes)
         )
         for k, v in map_scalar_dofs_in_rod_nodes.items():
             self.__dict__[k] = np.lib.stride_tricks.as_strided(
                 self.scalar_dofs_in_rod_nodes[v], (self.n_nodes,)
             )
@@ -145,26 +245,28 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_nodes[system_idx]
                 end_idx = self.end_idx_in_rod_nodes[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic node boundaries
+            _synchronize_periodic_boundary_of_scalar_collection(
+                self.__dict__[k], self.periodic_boundary_nodes_idx
+            )
 
         # Things in nodes that are vectors
         #             0 ("position_collection", float64[:, :]),
         #             1 ("internal_forces", float64[:, :]),
         #             2 ("external_forces", float64[:, :]),
-        #             3 ("damping_forces", float64[:, :]),
         # 6 in total
         map_vector_dofs_in_rod_nodes = {
             "position_collection": 0,
             "internal_forces": 1,
             "external_forces": 2,
-            "damping_forces": 3,
         }
         self.vector_dofs_in_rod_nodes = np.zeros(
             (len(map_vector_dofs_in_rod_nodes), 3 * self.n_nodes)
         )
         for k, v in map_vector_dofs_in_rod_nodes.items():
             self.__dict__[k] = np.lib.stride_tricks.as_strided(
                 self.vector_dofs_in_rod_nodes[v], (3, self.n_nodes)
@@ -174,14 +276,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_nodes[system_idx]
                 end_idx = self.end_idx_in_rod_nodes[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic node boundaries
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.__dict__[k], self.periodic_boundary_nodes_idx
+            )
 
         # Things in nodes that are matrices
         # Null set
 
     def allocate_block_variables_in_elements(self, systems: Sequence):
         """
         This function takes system collection and allocates the variables on
@@ -201,25 +307,22 @@
         #             0 ("radius", float64[:]),
         #             1 ("volume", float64[:]),
         #             2 ("density", float64[:]),
         #             3 ("lengths", float64[:]),
         #             4 ("rest_lengths", float64[:]),
         #             5 ("dilatation", float64[:]),
         #             6 ("dilatation_rate", float64[:]),
-        #             7 ("dissipation_constant_for_forces", float64[:]),
-        #             8 ("dissipation_constant_for_torques", float64[:])
         map_scalar_dofs_in_rod_elems = {
             "radius": 0,
             "volume": 1,
             "density": 2,
             "lengths": 3,
             "rest_lengths": 4,
             "dilatation": 5,
             "dilatation_rate": 6,
-            "dissipation_constant_for_torques": 7,
         }
         self.scalar_dofs_in_rod_elems = np.zeros(
             (len(map_scalar_dofs_in_rod_elems), self.n_elems)
         )
         for k, v in map_scalar_dofs_in_rod_elems.items():
             self.__dict__[k] = np.lib.stride_tricks.as_strided(
                 self.scalar_dofs_in_rod_elems[v], (self.n_elems,)
@@ -229,31 +332,33 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_elems[system_idx]
                 end_idx = self.end_idx_in_rod_elems[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic element boundaries
+            _synchronize_periodic_boundary_of_scalar_collection(
+                self.__dict__[k], self.periodic_boundary_elems_idx
+            )
 
         # Things in elements that are vectors
         #             0 ("tangents", float64[:, :]),
         #             1 ("sigma", float64[:, :]),
         #             2 ("rest_sigma", float64[:, :]),
         #             3 ("internal_torques", float64[:, :]),
         #             4 ("external_torques", float64[:, :]),
-        #             5 ("damping_torques", float64[:, :]),
         #             6 ("internal_stress", float64[:, :]),
         map_vector_dofs_in_rod_elems = {
             "tangents": 0,
             "sigma": 1,
             "rest_sigma": 2,
             "internal_torques": 3,
             "external_torques": 4,
-            "damping_torques": 5,
-            "internal_stress": 6,
+            "internal_stress": 5,
         }
         self.vector_dofs_in_rod_elems = np.zeros(
             (len(map_vector_dofs_in_rod_elems), 3 * self.n_elems)
         )
         for k, v in map_vector_dofs_in_rod_elems.items():
             self.__dict__[k] = np.lib.stride_tricks.as_strided(
                 self.vector_dofs_in_rod_elems[v], (3, self.n_elems)
@@ -263,14 +368,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_elems[system_idx]
                 end_idx = self.end_idx_in_rod_elems[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic element boundaries
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.__dict__[k], self.periodic_boundary_elems_idx
+            )
 
         # Things in elements that are matrices
         #             0 ("director_collection", float64[:, :, :]),
         #             1 ("mass_second_moment_of_inertia", float64[:, :, :]),
         #             2 ("inv_mass_second_moment_of_inertia", float64[:, :, :]),
         #             3 ("shear_matrix", float64[:, :, :]),
         map_matrix_dofs_in_rod_elems = {
@@ -291,14 +400,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_elems[system_idx]
                 end_idx = self.end_idx_in_rod_elems[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic element boundaries
+            _synchronize_periodic_boundary_of_matrix_collection(
+                self.__dict__[k], self.periodic_boundary_elems_idx
+            )
 
     def allocate_blocks_variables_in_voronoi(self, systems: Sequence):
         """
         This function takes system collection and allocates the variables on
         voronoi for block-structure and references allocated variables back to the
         systems.
 
@@ -330,14 +443,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_voronoi[system_idx]
                 end_idx = self.end_idx_in_rod_voronoi[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic voronoi boundaries
+            _synchronize_periodic_boundary_of_scalar_collection(
+                self.__dict__[k], self.periodic_boundary_voronoi_idx
+            )
 
         # Things in voronoi that are vectors
         #             0 ("kappa", float64[:, :]),
         #             1 ("rest_kappa", float64[:, :]),
         #             2 ("internal_couple", float64[:, :]),
         map_vector_dofs_in_rod_voronois = {
             "kappa": 0,
@@ -356,14 +473,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_voronoi[system_idx]
                 end_idx = self.end_idx_in_rod_voronoi[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic voronoi boundaries
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.__dict__[k], self.periodic_boundary_voronoi_idx
+            )
 
         # Things in voronoi that are matrices
         #             0 ("bend_matrix", float64[:, :, :]),
         map_matrix_dofs_in_rod_voronois = {"bend_matrix": 0}
         self.matrix_dofs_in_rod_voronois = np.zeros(
             (len(map_matrix_dofs_in_rod_voronois), 9 * self.n_voronoi)
         )
@@ -377,14 +498,18 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_voronoi[system_idx]
                 end_idx = self.end_idx_in_rod_voronoi[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic voronoi boundaries
+            _synchronize_periodic_boundary_of_matrix_collection(
+                self.__dict__[k], self.periodic_boundary_voronoi_idx
+            )
 
     def allocate_blocks_variables_for_symplectic_stepper(self, systems: Sequence):
         """
         This function takes system collection and allocates the variables used by symplectic
         stepper for block-structure and references allocated variables back to the systems.
 
         Parameters
@@ -452,21 +577,29 @@
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_nodes[system_idx]
                 end_idx = self.end_idx_in_rod_nodes[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic node boundaries
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.__dict__[k], self.periodic_boundary_nodes_idx
+            )
 
         # Copy systems variables on nodes to block structure
         map_rate_collection_dofs_in_rod_elems = {
             "omega_collection": 0,
             "alpha_collection": 1,
         }
         for k, v in map_rate_collection_dofs_in_rod_elems.items():
             for system_idx, system in enumerate(systems):
                 start_idx = self.start_idx_in_rod_elems[system_idx]
                 end_idx = self.end_idx_in_rod_elems[system_idx]
                 self.__dict__[k][..., start_idx:end_idx] = system.__dict__[k].copy()
                 system.__dict__[k] = np.ndarray.view(
                     self.__dict__[k][..., start_idx:end_idx]
                 )
+            # synchronize the periodic node boundaries
+            _synchronize_periodic_boundary_of_vector_collection(
+                self.__dict__[k], self.periodic_boundary_elems_idx
+            )
```

### Comparing `pyelastica-0.3.0/elastica/modules/base_system.py` & `pyelastica-0.3.1/elastica/modules/base_system.py`

 * *Files 14% similar despite different names*

```diff
@@ -4,19 +4,19 @@
 
 Basic coordinating for multiple, smaller systems that have an independently integrable
 interface (i.e. works with symplectic or explicit routines `timestepper.py`.)
 """
 from typing import Iterable, Callable, AnyStr
 
 from collections.abc import MutableSequence
-from itertools import chain
 
 from elastica.rod import RodBase
 from elastica.rigidbody import RigidBodyBase
 from elastica.modules.memory_block import construct_memory_block_structures
+from elastica._synchronize_periodic_boundary import _ConstrainPeriodicBoundaries
 
 
 class BaseSystemCollection(MutableSequence):
     """
     Base System for simulator classes. Every simulation class written by the user
     must be derived from the BaseSystemCollection class; otherwise the simulation will
     proceed.
@@ -138,14 +138,30 @@
 
         # This generates more straight-forward error.
         assert self._finalize_flag is not True, "The finalize cannot be called twice."
 
         # construct memory block
         self._memory_blocks = construct_memory_block_structures(self._systems)
 
+        """
+        In case memory block have ring rod, then periodic boundaries have to be synched. In order to synchronize
+        periodic boundaries, a new constrain for memory block rod added called as _ConstrainPeriodicBoundaries. This
+        constrain will synchronize the only periodic boundaries of position, director, velocity and omega variables.
+        """
+        for i in range(len(self._memory_blocks)):
+            # append the memory block to the simulation as a system. Memory block is the final system in the simulation.
+            self.append(self._memory_blocks[i])
+            if hasattr(self._memory_blocks[i], "ring_rod_flag"):
+                # Apply the constrain to synchronize the periodic boundaries of the memory rod. Find the memory block
+                # sys idx among other systems added and then apply boundary conditions.
+                memory_block_idx = self._get_sys_idx_if_valid(self._memory_blocks[i])
+                self.constrain(self._systems[memory_block_idx]).using(
+                    _ConstrainPeriodicBoundaries,
+                )
+
         # Recurrent call finalize functions for all components.
         for finalize in self._feature_group_finalize:
             finalize()
 
         # Clear the finalize feature group, just for the safety.
         self._feature_group_finalize.clear()
         self._feature_group_finalize = None
```

### Comparing `pyelastica-0.3.0/elastica/modules/callbacks.py` & `pyelastica-0.3.1/elastica/modules/callbacks.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/modules/connections.py` & `pyelastica-0.3.1/elastica/modules/connections.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/modules/constraints.py` & `pyelastica-0.3.1/elastica/modules/constraints.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 __doc__ = """
 Constraints
 -----------
 
 Provides the constraints interface to enforce displacement boundary conditions (see `boundary_conditions.py`).
 """
 
-import numpy as np
 from elastica.boundary_conditions import ConstraintBase
 
 
 class Constraints:
     """
     The Constraints class is a module for enforcing displacement boundary conditions.
     To enforce boundary conditions on rod-like objects, the simulator class
```

### Comparing `pyelastica-0.3.0/elastica/modules/damping.py` & `pyelastica-0.3.1/elastica/modules/damping.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/modules/forcing.py` & `pyelastica-0.3.1/elastica/modules/forcing.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/modules/memory_block.py` & `pyelastica-0.3.1/elastica/modules/memory_block.py`

 * *Files 20% similar despite different names*

```diff
@@ -17,22 +17,26 @@
     Returns
     -------
 
     """
     _memory_blocks = []
     temp_list_for_cosserat_rod_systems = []
     temp_list_for_rigid_body_systems = []
+    temp_list_for_cosserat_rod_systems_idx = []
+    temp_list_for_rigid_body_systems_idx = []
 
     for system_idx, sys_to_be_added in enumerate(systems):
 
         if issubclass(sys_to_be_added.__class__, RodBase):
             temp_list_for_cosserat_rod_systems.append(sys_to_be_added)
+            temp_list_for_cosserat_rod_systems_idx.append(system_idx)
 
         elif issubclass(sys_to_be_added.__class__, RigidBodyBase):
             temp_list_for_rigid_body_systems.append(sys_to_be_added)
+            temp_list_for_rigid_body_systems_idx.append(system_idx)
 
         else:
             raise TypeError(
                 "{0}\n"
                 "is not a system passing validity\n"
                 "checks for constructing block structure. If you are sure that\n"
                 "{0}\n"
@@ -40,14 +44,21 @@
                 "it here with correct memory block implementation.\n"
                 "The allowed types are\n"
                 "{1} {2}".format(sys_to_be_added.__class__, RodBase, RigidBodyBase)
             )
 
     if temp_list_for_cosserat_rod_systems:
         _memory_blocks.append(
-            MemoryBlockCosseratRod(temp_list_for_cosserat_rod_systems)
+            MemoryBlockCosseratRod(
+                temp_list_for_cosserat_rod_systems,
+                temp_list_for_cosserat_rod_systems_idx,
+            )
         )
 
     if temp_list_for_rigid_body_systems:
-        _memory_blocks.append(MemoryBlockRigidBody(temp_list_for_rigid_body_systems))
+        _memory_blocks.append(
+            MemoryBlockRigidBody(
+                temp_list_for_rigid_body_systems, temp_list_for_rigid_body_systems_idx
+            )
+        )
 
     return _memory_blocks
```

### Comparing `pyelastica-0.3.0/elastica/reset_functions_for_block_structure/_reset_ghost_vector_or_scalar.py` & `pyelastica-0.3.1/elastica/reset_functions_for_block_structure/_reset_ghost_vector_or_scalar.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 __doc__ = """Reset the ghost vectors or scalar variables using functions implemented in Numba"""
 
-import numpy as np
-import numba
 from numba import njit
 
 
 @njit(cache=True)
 def _reset_vector_ghost(input, ghost_idx, reset_value=0.0):
     """
     This function resets the ghost of an input vector collection. Default reset value is 0.0.
```

### Comparing `pyelastica-0.3.0/elastica/restart.py` & `pyelastica-0.3.1/elastica/restart.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 __doc__ = """Generate or load restart file implementations."""
-__all__ = ["save_state", "load_state"]
+
 import numpy as np
 import os
 from itertools import groupby
+from .memory_block import MemoryBlockCosseratRod, MemoryBlockRigidBody
 
 
 def all_equal(iterable):
     """
     Checks if all elements of list are equal.
     Parameters
     ----------
@@ -37,14 +38,18 @@
     time : float
         Simulation time.
     verbose : boolean
 
     """
     os.makedirs(directory, exist_ok=True)
     for idx, rod in enumerate(simulator):
+        if isinstance(rod, MemoryBlockCosseratRod) or isinstance(
+            rod, MemoryBlockRigidBody
+        ):
+            continue
         path = os.path.join(directory, "system_{}.npz".format(idx))
         np.savez(path, time=time, **rod.__dict__)
 
     if verbose:
         print("Save complete: {}".format(directory))
 
 
@@ -65,14 +70,18 @@
     Returns
     ------
     time : float
         Simulation time of systems when they are saved.
     """
     time_list = []  # Simulation time of rods when they are saved.
     for idx, rod in enumerate(simulator):
+        if isinstance(rod, MemoryBlockCosseratRod) or isinstance(
+            rod, MemoryBlockRigidBody
+        ):
+            continue
         path = os.path.join(directory, "system_{}.npz".format(idx))
         data = np.load(path, allow_pickle=True)
         for key, value in data.items():
             if key == "time":
                 time_list.append(value.item())
                 continue
 
@@ -84,15 +93,11 @@
                 setattr(rod, key, value)
 
     if not all_equal(time_list):
         raise ValueError(
             "Restart time of loaded rods are different, check your inputs!"
         )
 
-    # Apply boundary conditions, after loading the systems.
-    simulator.constrain_values(0.0)
-    simulator.constrain_rates(0.0)
-
     if verbose:
         print("Load complete: {}".format(directory))
 
     return time_list[0]
```

### Comparing `pyelastica-0.3.0/elastica/rigidbody/cylinder.py` & `pyelastica-0.3.1/elastica/rigidbody/cylinder.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 __doc__ = """"""
-__all__ = ["Cylinder"]
 
 import numpy as np
 
 from elastica._linalg import _batch_cross
 from elastica.utils import MaxDimension
 from elastica.rigidbody.rigid_body import RigidBodyBase
```

### Comparing `pyelastica-0.3.0/elastica/rigidbody/data_structures.py` & `pyelastica-0.3.1/elastica/rigidbody/data_structures.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 __doc__ = "Data structure wrapper for rod components"
 
 import numpy as np
 
-from elastica._rotations import _get_rotation_matrix, _rotate
+from elastica._rotations import _get_rotation_matrix
 from elastica.rod.data_structures import _RodSymplecticStepperMixin
 
 """
 # FIXME : Explicit Stepper doesn't work as States lose the
 # views they initially had when working with a timestepper.
 class _RigidRodExplicitStepperMixin:
     def __init__(self):
```

### Comparing `pyelastica-0.3.0/elastica/rigidbody/rigid_body.py` & `pyelastica-0.3.1/elastica/rigidbody/rigid_body.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 __doc__ = """"""
 
 import numpy as np
-from abc import ABC, abstractmethod
+from abc import ABC
 from elastica._linalg import _batch_matvec, _batch_cross
-from elastica.utils import MaxDimension
 
 
 class RigidBodyBase(ABC):
     """
     Base class for rigid body classes.
 
     Notes
```

### Comparing `pyelastica-0.3.0/elastica/rigidbody/sphere.py` & `pyelastica-0.3.1/elastica/rigidbody/sphere.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 __doc__ = """"""
-__all__ = ["Sphere"]
 
 import numpy as np
 
 from elastica._linalg import _batch_cross
 from elastica.utils import MaxDimension
 from elastica.rigidbody.rigid_body import RigidBodyBase
```

### Comparing `pyelastica-0.3.0/elastica/rod/cosserat_rod.py` & `pyelastica-0.3.1/elastica/rod/cosserat_rod.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 __doc__ = """ Rod classes and implementation details """
-__all__ = ["CosseratRod"]
 
-import typing
 
 import numpy as np
 import functools
 import numba
 from elastica.rod import RodBase
 from elastica._linalg import (
     _batch_cross,
@@ -18,24 +16,59 @@
 from elastica.rod.knot_theory import KnotTheory
 from elastica._calculus import (
     quadrature_kernel_for_block_structure,
     difference_kernel_for_block_structure,
     _difference,
     _average,
 )
+from typing import Optional
 
 position_difference_kernel = _difference
 position_average = _average
 
 
 @functools.lru_cache(maxsize=1)
 def _get_z_vector():
     return np.array([0.0, 0.0, 1.0]).reshape(3, -1)
 
 
+def _compute_sigma_kappa_for_blockstructure(memory_block):
+    """
+    This function is a wrapper to call functions which computes shear stretch, strain and bending twist and strain.
+
+    Parameters
+    ----------
+    memory_block : object
+
+    Returns
+    -------
+
+    """
+    _compute_shear_stretch_strains(
+        memory_block.position_collection,
+        memory_block.volume,
+        memory_block.lengths,
+        memory_block.tangents,
+        memory_block.radius,
+        memory_block.rest_lengths,
+        memory_block.rest_voronoi_lengths,
+        memory_block.dilatation,
+        memory_block.voronoi_dilatation,
+        memory_block.director_collection,
+        memory_block.sigma,
+    )
+
+    # Compute bending twist strains for the block
+    _compute_bending_twist_strains(
+        memory_block.director_collection,
+        memory_block.rest_voronoi_lengths,
+        memory_block.kappa,
+    )
+
+
 class CosseratRod(RodBase, KnotTheory):
     """
     Cosserat Rod class. This is the preferred class for rods because it is derived from some
     of the essential base classes.
 
         Attributes
         ----------
@@ -73,21 +106,14 @@
             Rod node masses. Note that masses are stored on the nodes, not on elements.
         mass_second_moment_of_inertia: numpy.ndarray
             3D (dim, dim, n_elems) array containing data with 'float' type.
             Rod element mass second moment of interia.
         inv_mass_second_moment_of_inertia: numpy.ndarray
             3D (dim, dim, n_elems) array containing data with 'float' type.
             Rod element inverse mass moment of inertia.
-        dissipation_constant_for_forces: numpy.ndarray
-            1D (n_elems) array containing data with 'float' type.
-            Rod element dissipation coefficient (nu).
-        dissipation_constant_for_torques: numpy.ndarray
-            1D (n_elems) array containing data with 'float' type.
-            Rod element dissipation (nu).
-            Can be customized by passing 'nu_for_torques'.
         rest_voronoi_lengths: numpy.ndarray
             1D (n_voronoi) array containing data with 'float' type.
             Rod lengths on the voronoi domain at the rest configuration.
         internal_forces: numpy.ndarray
             2D (dim, n_nodes) array containing data with 'float' type.
             Rod node internal forces. Note that internal forces are stored on the node, not on elements.
         internal_torques: numpy.ndarray
@@ -132,16 +158,14 @@
         mass_second_moment_of_inertia,
         inv_mass_second_moment_of_inertia,
         shear_matrix,
         bend_matrix,
         density,
         volume,
         mass,
-        dissipation_constant_for_forces,
-        dissipation_constant_for_torques,
         internal_forces,
         internal_torques,
         external_forces,
         external_torques,
         lengths,
         rest_lengths,
         tangents,
@@ -151,16 +175,15 @@
         rest_voronoi_lengths,
         sigma,
         kappa,
         rest_sigma,
         rest_kappa,
         internal_stress,
         internal_couple,
-        damping_forces,
-        damping_torques,
+        ring_rod_flag,
     ):
         self.n_elems = n_elements
         self.position_collection = position
         self.velocity_collection = velocity
         self.omega_collection = omega
         self.acceleration_collection = acceleration
         self.alpha_collection = angular_acceleration
@@ -169,16 +192,14 @@
         self.mass_second_moment_of_inertia = mass_second_moment_of_inertia
         self.inv_mass_second_moment_of_inertia = inv_mass_second_moment_of_inertia
         self.shear_matrix = shear_matrix
         self.bend_matrix = bend_matrix
         self.density = density
         self.volume = volume
         self.mass = mass
-        self.dissipation_constant_for_forces = dissipation_constant_for_forces
-        self.dissipation_constant_for_torques = dissipation_constant_for_torques
         self.internal_forces = internal_forces
         self.internal_torques = internal_torques
         self.external_forces = external_forces
         self.external_torques = external_torques
         self.lengths = lengths
         self.rest_lengths = rest_lengths
         self.tangents = tangents
@@ -188,50 +209,52 @@
         self.rest_voronoi_lengths = rest_voronoi_lengths
         self.sigma = sigma
         self.kappa = kappa
         self.rest_sigma = rest_sigma
         self.rest_kappa = rest_kappa
         self.internal_stress = internal_stress
         self.internal_couple = internal_couple
-        self.damping_forces = damping_forces
-        self.damping_torques = damping_torques
+        self.ring_rod_flag = ring_rod_flag
 
-        # Compute shear stretch and strains.
-        _compute_shear_stretch_strains(
-            self.position_collection,
-            self.volume,
-            self.lengths,
-            self.tangents,
-            self.radius,
-            self.rest_lengths,
-            self.rest_voronoi_lengths,
-            self.dilatation,
-            self.voronoi_dilatation,
-            self.director_collection,
-            self.sigma,
-        )
+        if not self.ring_rod_flag:
+            # For ring rod there are no periodic elements so below code won't run.
+            # We add periodic elements at the memory block construction.
+            # Compute shear stretch and strains.
+            _compute_shear_stretch_strains(
+                self.position_collection,
+                self.volume,
+                self.lengths,
+                self.tangents,
+                self.radius,
+                self.rest_lengths,
+                self.rest_voronoi_lengths,
+                self.dilatation,
+                self.voronoi_dilatation,
+                self.director_collection,
+                self.sigma,
+            )
 
-        # Compute bending twist strains
-        _compute_bending_twist_strains(
-            self.director_collection, self.rest_voronoi_lengths, self.kappa
-        )
+            # Compute bending twist strains
+            _compute_bending_twist_strains(
+                self.director_collection, self.rest_voronoi_lengths, self.kappa
+            )
 
     @classmethod
     def straight_rod(
         cls,
         n_elements: int,
         start: np.ndarray,
         direction: np.ndarray,
         normal: np.ndarray,
         base_length: float,
         base_radius: float,
         density: float,
-        nu: float,
+        *,
+        nu: Optional[float] = None,
         youngs_modulus: float,
-        *args,
         **kwargs,
     ):
         """
         Cosserat rod constructor for straight-rod geometry.
 
 
         Notes
@@ -239,15 +262,16 @@
         Since we expect the Cosserat Rod to simulate soft rod, Poisson's ratio is set to 0.5 by default.
         It is possible to give additional argument "shear_modulus" or "poisson_ratio" to specify extra modulus.
 
 
         Parameters
         ----------
         n_elements : int
-            Number of element. Must be greater than 3. Generarally recommended to start with 40-50, and adjust the resolution.
+            Number of element. Must be greater than 3.
+            Generally recommended to start with 40-50, and adjust the resolution.
         start : NDArray[3, float]
             Starting coordinate in 3D
         direction : NDArray[3, float]
             Direction of the rod in 3D
         normal : NDArray[3, float]
             Normal vector of the rod in 3D
         base_length : float
@@ -256,26 +280,34 @@
             Uniform radius of the rod
         density : float
             Density of the rod
         nu : float
             Damping coefficient for Rayleigh damping
         youngs_modulus : float
             Young's modulus
-        *args : tuple
-            Additional arguments should be passed as keyward arguments.
-            (e.g. shear_modulus, poisson_ratio)
         **kwargs : dict, optional
             The "position" and/or "directors" can be overrided by passing "position" and "directors" argument. Remember, the shape of the "position" is (3,n_elements+1) and the shape of the "directors" is (3,3,n_elements).
 
         Returns
         -------
         CosseratRod
 
         """
 
+        if nu is not None:
+            raise ValueError(
+                # Remove the option to set internal nu inside, beyond v0.4.0
+                "The option to set damping coefficient (nu) for the rod during rod\n"
+                "initialisation is now deprecated. Instead, for adding damping to rods,\n"
+                "please derive your simulation class from the add-on Damping mixin class.\n"
+                "For reference see the class elastica.dissipation.AnalyticalLinearDamper(),\n"
+                "and for usage check examples/axial_stretching.py"
+            )
+        # Straight rod is not ring rod set flag to false
+        ring_rod_flag = False
         (
             n_elements,
             position,
             velocities,
             omegas,
             accelerations,
             angular_accelerations,
@@ -284,16 +316,14 @@
             mass_second_moment_of_inertia,
             inv_mass_second_moment_of_inertia,
             shear_matrix,
             bend_matrix,
             density,
             volume,
             mass,
-            dissipation_constant_for_forces,
-            dissipation_constant_for_torques,
             internal_forces,
             internal_torques,
             external_forces,
             external_torques,
             lengths,
             rest_lengths,
             tangents,
@@ -303,27 +333,24 @@
             rest_voronoi_lengths,
             sigma,
             kappa,
             rest_sigma,
             rest_kappa,
             internal_stress,
             internal_couple,
-            damping_forces,
-            damping_torques,
         ) = allocate(
             n_elements,
-            start,
             direction,
             normal,
             base_length,
             base_radius,
             density,
-            nu,
             youngs_modulus,
-            *args,
+            rod_origin_position=start,
+            ring_rod_flag=ring_rod_flag,
             **kwargs,
         )
 
         return cls(
             n_elements,
             position,
             velocities,
@@ -335,16 +362,14 @@
             mass_second_moment_of_inertia,
             inv_mass_second_moment_of_inertia,
             shear_matrix,
             bend_matrix,
             density,
             volume,
             mass,
-            dissipation_constant_for_forces,
-            dissipation_constant_for_torques,
             internal_forces,
             internal_torques,
             external_forces,
             external_torques,
             lengths,
             rest_lengths,
             tangents,
@@ -354,16 +379,162 @@
             rest_voronoi_lengths,
             sigma,
             kappa,
             rest_sigma,
             rest_kappa,
             internal_stress,
             internal_couple,
-            damping_forces,
-            damping_torques,
+            ring_rod_flag,
+        )
+
+    @classmethod
+    def ring_rod(
+        cls,
+        n_elements: int,
+        ring_center_position: np.ndarray,
+        direction: np.ndarray,
+        normal: np.ndarray,
+        base_length: float,
+        base_radius: float,
+        density: float,
+        *,
+        nu: Optional[float] = None,
+        youngs_modulus: float,
+        **kwargs,
+    ):
+        """
+        Cosserat rod constructor for straight-rod geometry.
+
+
+        Notes
+        -----
+        Since we expect the Cosserat Rod to simulate soft rod, Poisson's ratio is set to 0.5 by default.
+        It is possible to give additional argument "shear_modulus" or "poisson_ratio" to specify extra modulus.
+
+
+        Parameters
+        ----------
+        n_elements : int
+            Number of element. Must be greater than 3. Generarally recommended to start with 40-50, and adjust the resolution.
+        ring_center_position : NDArray[3, float]
+            Center coordinate for ring rod in 3D
+        direction : NDArray[3, float]
+            Direction of the rod in 3D
+        normal : NDArray[3, float]
+            Normal vector of the rod in 3D
+        base_length : float
+            Total length of the rod
+        base_radius : float
+            Uniform radius of the rod
+        density : float
+            Density of the rod
+        nu : float
+            Damping coefficient for Rayleigh damping
+        youngs_modulus : float
+            Young's modulus
+        **kwargs : dict, optional
+            The "position" and/or "directors" can be overrided by passing "position" and "directors" argument. Remember, the shape of the "position" is (3,n_elements+1) and the shape of the "directors" is (3,3,n_elements).
+
+        Returns
+        -------
+        CosseratRod
+
+        """
+
+        if nu is not None:
+            raise ValueError(
+                # Remove the option to set internal nu inside, beyond v0.4.0
+                "The option to set damping coefficient (nu) for the rod during rod\n"
+                "initialisation is now deprecated. Instead, for adding damping to rods,\n"
+                "please derive your simulation class from the add-on Damping mixin class.\n"
+                "For reference see the class elastica.dissipation.AnalyticalLinearDamper(),\n"
+                "and for usage check examples/axial_stretching.py"
+            )
+        # Straight rod is not ring rod set flag to false
+        ring_rod_flag = True
+        (
+            n_elements,
+            position,
+            velocities,
+            omegas,
+            accelerations,
+            angular_accelerations,
+            directors,
+            radius,
+            mass_second_moment_of_inertia,
+            inv_mass_second_moment_of_inertia,
+            shear_matrix,
+            bend_matrix,
+            density_array,
+            volume,
+            mass,
+            internal_forces,
+            internal_torques,
+            external_forces,
+            external_torques,
+            lengths,
+            rest_lengths,
+            tangents,
+            dilatation,
+            dilatation_rate,
+            voronoi_dilatation,
+            rest_voronoi_lengths,
+            sigma,
+            kappa,
+            rest_sigma,
+            rest_kappa,
+            internal_stress,
+            internal_couple,
+        ) = allocate(
+            n_elements,
+            direction,
+            normal,
+            base_length,
+            base_radius,
+            density,
+            youngs_modulus,
+            rod_origin_position=ring_center_position,
+            ring_rod_flag=ring_rod_flag,
+            **kwargs,
+        )
+
+        return cls(
+            n_elements,
+            position,
+            velocities,
+            omegas,
+            accelerations,
+            angular_accelerations,
+            directors,
+            radius,
+            mass_second_moment_of_inertia,
+            inv_mass_second_moment_of_inertia,
+            shear_matrix,
+            bend_matrix,
+            density_array,
+            volume,
+            mass,
+            internal_forces,
+            internal_torques,
+            external_forces,
+            external_torques,
+            lengths,
+            rest_lengths,
+            tangents,
+            dilatation,
+            dilatation_rate,
+            voronoi_dilatation,
+            rest_voronoi_lengths,
+            sigma,
+            kappa,
+            rest_sigma,
+            rest_kappa,
+            internal_stress,
+            internal_couple,
+            ring_rod_flag,
         )
 
     def compute_internal_forces_and_torques(self, time):
         """
         Compute internal forces and torques. We need to compute internal forces and torques before the acceleration because
         they are used in interaction. Thus in order to speed up simulation, we will compute internal forces and torques
         one time and use them. Previously, we were computing internal forces and torques multiple times in interaction.
@@ -386,17 +557,14 @@
             self.dilatation,
             self.voronoi_dilatation,
             self.director_collection,
             self.sigma,
             self.rest_sigma,
             self.shear_matrix,
             self.internal_stress,
-            self.velocity_collection,
-            self.dissipation_constant_for_forces,
-            self.damping_forces,
             self.internal_forces,
             self.ghost_elems_idx,
         )
 
         _compute_internal_torques(
             self.position_collection,
             self.velocity_collection,
@@ -411,16 +579,14 @@
             self.voronoi_dilatation,
             self.mass_second_moment_of_inertia,
             self.omega_collection,
             self.internal_stress,
             self.internal_couple,
             self.dilatation,
             self.dilatation_rate,
-            self.dissipation_constant_for_torques,
-            self.damping_torques,
             self.internal_torques,
             self.ghost_voronoi_idx,
         )
 
     # Interface to time-stepper mixins (Symplectic, Explicit), which calls this method
     def update_accelerations(self, time):
         """
@@ -719,34 +885,14 @@
         for k in range(blocksize):
             temp[i, k] = kappa[i, k] - rest_kappa[i, k]
 
     internal_couple[:] = _batch_matvec(bend_matrix, temp)
 
 
 @numba.njit(cache=True)
-def _compute_damping_forces(
-    damping_forces,
-    velocity_collection,
-    dissipation_constant_for_forces,
-):
-    """
-    Update <damping force> given <velocity>
-    """
-
-    # Internal damping forces.
-    blocksize = velocity_collection.shape[1]
-
-    for i in range(3):
-        for k in range(blocksize):
-            damping_forces[i, k] = (
-                dissipation_constant_for_forces[k] * velocity_collection[i, k]
-            )
-
-
-@numba.njit(cache=True)
 def _compute_internal_forces(
     position_collection,
     volume,
     lengths,
     tangents,
     radius,
     rest_lengths,
@@ -754,22 +900,19 @@
     dilatation,
     voronoi_dilatation,
     director_collection,
     sigma,
     rest_sigma,
     shear_matrix,
     internal_stress,
-    velocity_collection,
-    dissipation_constant_for_forces,
-    damping_forces,
     internal_forces,
     ghost_elems_idx,
 ):
     """
-    Update <internal force> given <director, internal_stress, velocity and damping force>.
+    Update <internal force> given <director, internal_stress and velocity>.
     """
 
     # Compute n_l and cache it using internal_stress
     # Be careful about usage though
     _compute_internal_shear_stretch_stresses_from_model(
         position_collection,
         volume,
@@ -797,43 +940,20 @@
         for j in range(3):
             for k in range(blocksize):
                 cosserat_internal_stress[i, k] += (
                     director_collection[j, i, k] * internal_stress[j, k]
                 )
 
     cosserat_internal_stress /= dilatation
-
-    _compute_damping_forces(
-        damping_forces,
-        velocity_collection,
-        dissipation_constant_for_forces,
-    )
-
-    internal_forces[:] = (
-        difference_kernel_for_block_structure(cosserat_internal_stress, ghost_elems_idx)
-        - damping_forces
+    internal_forces[:] = difference_kernel_for_block_structure(
+        cosserat_internal_stress, ghost_elems_idx
     )
 
 
 @numba.njit(cache=True)
-def _compute_damping_torques(
-    damping_torques, omega_collection, dissipation_constant_for_torques
-):
-    """
-    Update <damping torque> given <angular velocity>.
-    """
-    blocksize = omega_collection.shape[1]
-    for i in range(3):
-        for k in range(blocksize):
-            damping_torques[i, k] = (
-                dissipation_constant_for_torques[k] * omega_collection[i, k]
-            )
-
-
-@numba.njit(cache=True)
 def _compute_internal_torques(
     position_collection,
     velocity_collection,
     tangents,
     lengths,
     rest_lengths,
     director_collection,
@@ -844,16 +964,14 @@
     voronoi_dilatation,
     mass_second_moment_of_inertia,
     omega_collection,
     internal_stress,
     internal_couple,
     dilatation,
     dilatation_rate,
-    dissipation_constant_for_torques,
-    damping_torques,
     internal_torques,
     ghost_voronoi_idx,
 ):
     """
     Update <internal torque>.
     """
     # Compute \tau_l and cache it using internal_couple
@@ -904,28 +1022,23 @@
     lagrangian_transport = _batch_cross(J_omega_upon_e, omega_collection)
 
     # Note : in the computation of dilatation_rate, there is an optimization opportunity as dilatation rate has
     # a dilatation-like term in the numerator, which we cancel here
     # (J \omega_L / e^2) . (de/dt)
     unsteady_dilatation = J_omega_upon_e * dilatation_rate / dilatation
 
-    _compute_damping_torques(
-        damping_torques, omega_collection, dissipation_constant_for_torques
-    )
-
     blocksize = internal_torques.shape[1]
     for i in range(3):
         for k in range(blocksize):
             internal_torques[i, k] = (
                 bend_twist_couple_2D[i, k]
                 + bend_twist_couple_3D[i, k]
                 + shear_stretch_couple[i, k]
                 + lagrangian_transport[i, k]
                 + unsteady_dilatation[i, k]
-                - damping_torques[i, k]
             )
 
 
 @numba.njit(cache=True)
 def _update_accelerations(
     acceleration_collection,
     internal_forces,
```

### Comparing `pyelastica-0.3.0/elastica/rod/data_structures.py` & `pyelastica-0.3.1/elastica/rod/data_structures.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,10 @@
 __doc__ = "Data structure wrapper for rod components"
-__all__ = [
-    "_RodSymplecticStepperMixin",
-    "_bootstrap_from_data",
-    "_State",
-    "_DerivativeState",
-    "_KinematicState",
-    "_DynamicState",
-]
+
 import numpy as np
-import numba
 from numba import njit
 from elastica._rotations import _get_rotation_matrix, _rotate
 from elastica._linalg import _batch_matmul
 
 
 # FIXME : Explicit Stepper doesn't work as States lose the
 # views they initially had when working with a timestepper.
```

### Comparing `pyelastica-0.3.0/elastica/rod/factory_function.py` & `pyelastica-0.3.1/elastica/rod/factory_function.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,61 +1,86 @@
 __doc__ = """ Factory function to allocate variables for Cosserat Rod"""
-__all__ = ["allocate"]
 from typing import Optional, Tuple
 import logging
 import numpy as np
 from numpy.testing import assert_allclose
 from elastica.utils import MaxDimension, Tolerance
 from elastica._linalg import _batch_cross, _batch_norm, _batch_dot
 
 
 def allocate(
     n_elements,
-    start,
     direction,
     normal,
     base_length,
     base_radius,
     density,
-    nu,
     youngs_modulus: float,
-    nu_for_torques: Optional[float] = None,
+    *,
+    rod_origin_position: np.ndarray,
+    ring_rod_flag: bool,
     shear_modulus: Optional[float] = None,
     position: Optional[np.ndarray] = None,
     directors: Optional[np.ndarray] = None,
     rest_sigma: Optional[np.ndarray] = None,
     rest_kappa: Optional[np.ndarray] = None,
-    *args,
     **kwargs,
 ):
     log = logging.getLogger()
 
     if "poisson_ratio" in kwargs:
         # Deprecation warning for poission_ratio
         raise NameError(
             "Poisson's ratio is deprecated for Cosserat Rod for clarity. Please provide shear_modulus instead."
         )
 
     # sanity checks here
-    assert n_elements > 1
+    assert n_elements > 2 if ring_rod_flag else n_elements > 1
     assert base_length > Tolerance.atol()
     assert np.sqrt(np.dot(normal, normal)) > Tolerance.atol()
     assert np.sqrt(np.dot(direction, direction)) > Tolerance.atol()
 
+    # define the number of nodes and voronoi elements based on if rod is
+    # straight and open or closed and ring shaped
+    n_nodes = n_elements if ring_rod_flag else n_elements + 1
+    n_voronoi_elements = n_elements if ring_rod_flag else n_elements - 1
+
     # check if position is given.
     if position is None:  # Generate straight and uniform rod
         # Set the position array
-        position = np.zeros((MaxDimension.value(), n_elements + 1))
-        end = start + direction * base_length
-        for i in range(0, 3):
-            position[i, ...] = np.linspace(start[i], end[i], n_elements + 1)
-    _position_validity_checker(position, start, n_elements)
+        position = np.zeros((MaxDimension.value(), n_nodes))
+        if not ring_rod_flag:  # i.e. a straight open rod
+            start = rod_origin_position
+            end = start + direction * base_length
+            for i in range(0, 3):
+                position[i, ...] = np.linspace(start[i], end[i], n_elements + 1)
+            _position_validity_checker(position, start, n_elements)
+        else:  # i.e a closed ring rod
+            ring_center_position = rod_origin_position
+            binormal = np.cross(direction, normal)
+            for i in range(n_elements):
+                position[..., i] = (
+                    base_length
+                    / (2 * np.pi)
+                    * (
+                        np.cos(2 * np.pi / n_elements * i) * binormal
+                        + np.sin(2 * np.pi / n_elements * i) * direction
+                    )
+                ) + ring_center_position
+            _position_validity_checker_ring_rod(
+                position, ring_center_position, n_elements
+            )
 
     # Compute rest lengths and tangents
-    position_diff = position[..., 1:] - position[..., :-1]
+    position_for_difference = (
+        np.hstack((position, position[..., 0].reshape(3, 1)))
+        if ring_rod_flag
+        else position
+    )
+    position_diff = position_for_difference[..., 1:] - position_for_difference[..., :-1]
     rest_lengths = _batch_norm(position_diff)
     tangents = position_diff / rest_lengths
     normal /= np.linalg.norm(normal)
 
     if directors is None:  # Generate straight uniform rod
         # Set the directors matrix
         directors = np.zeros((MaxDimension.value(), MaxDimension.value(), n_elements))
@@ -155,137 +180,92 @@
                 alpha_c * shear_modulus * A0[i],
                 youngs_modulus * A0[i],
             ],
         )
 
     # Bend/Twist matrix
     bend_matrix = np.zeros(
-        (MaxDimension.value(), MaxDimension.value(), n_elements), np.float64
+        (MaxDimension.value(), MaxDimension.value(), n_voronoi_elements + 1), np.float64
     )
     for i in range(n_elements):
         np.fill_diagonal(
             bend_matrix[..., i],
             [
                 youngs_modulus * I0_1[i],
                 youngs_modulus * I0_2[i],
                 shear_modulus * I0_3[i],
             ],
         )
+    if ring_rod_flag:  # wrap around the value in the last element
+        bend_matrix[..., -1] = bend_matrix[..., 0]
     for i in range(0, MaxDimension.value()):
         assert np.all(
             bend_matrix[i, i, :] > Tolerance.atol()
         ), " Bend matrix has to be greater than 0."
 
     # Compute bend matrix in Voronoi Domain
+    rest_lengths_temp_for_voronoi = (
+        np.hstack((rest_lengths, rest_lengths[0])) if ring_rod_flag else rest_lengths
+    )
     bend_matrix = (
-        bend_matrix[..., 1:] * rest_lengths[1:]
-        + bend_matrix[..., :-1] * rest_lengths[0:-1]
-    ) / (rest_lengths[1:] + rest_lengths[:-1])
+        bend_matrix[..., 1:] * rest_lengths_temp_for_voronoi[1:]
+        + bend_matrix[..., :-1] * rest_lengths_temp_for_voronoi[0:-1]
+    ) / (rest_lengths_temp_for_voronoi[1:] + rest_lengths_temp_for_voronoi[:-1])
 
     # Compute volume of elements
     volume = np.pi * radius ** 2 * rest_lengths
 
     # Compute mass of elements
-    mass = np.zeros(n_elements + 1)
-    mass[:-1] += 0.5 * density * volume
-    mass[1:] += 0.5 * density * volume
-
-    # Set dissipation constant or nu array
-    log.warning(
-        # Remove warning and add error if nu provided in v0.3.1
-        # Remove the option to set internal nu inside, beyond v0.4.0
-        "The option to set damping coefficient (nu) for the rod during rod "
-        "initialisation is now deprecated. Instead, for adding damping to rods, "
-        "please derive your simulation class from the add-on Damping mixin class. "
-        "For reference see the class elastica.dissipation.AnalyticalLinearDamper(), "
-        "and for usage check examples/axial_stretching.py "
-        "The option to set damping coefficient (nu) during rod construction "
-        "will be removed in the future (v0.3.1)."
-    )
-    dissipation_constant_for_forces = np.zeros((n_elements + 1))
-    # Check if the user input nu is valid
-    nu_temp = np.array(nu)
-    _assert_dim(nu_temp, 2, "dissipation constant (nu) for forces)")
-    dissipation_constant_for_forces[:] = nu * mass
-    # Check if the elements of dissipation constant greater than tolerance
-    assert np.all(
-        dissipation_constant_for_forces >= 0.0
-    ), " Dissipation constant(nu) has to be equal or greater than 0."
-
-    # Custom nu for torques
-    dissipation_constant_for_torques = np.zeros((n_elements))
-
-    if nu_for_torques is None:
-        dissipation_constant_for_torques[:] = (
-            dissipation_constant_for_forces[1:] + dissipation_constant_for_forces[:-1]
-        ) / 2
-        # Treat the end elements carefully, since end nodes only have one neighboring element we need to add all of
-        # their dissipation.
-        dissipation_constant_for_torques[0] += (dissipation_constant_for_forces[0]) / 2
-        dissipation_constant_for_torques[-1] += (
-            dissipation_constant_for_forces[-1]
-        ) / 2
+    mass = np.zeros(n_nodes)
+    if not ring_rod_flag:
+        mass[:-1] += 0.5 * density * volume
+        mass[1:] += 0.5 * density * volume
     else:
-        elemental_mass = (mass[1:] + mass[:-1]) / 2.0
-        # Treat the end elements carefully, since end nodes only have one neighboring element we need to add all of
-        # their mass.
-        elemental_mass[0] += mass[0] / 2.0
-        elemental_mass[-1] += mass[-1] / 2.0
-        dissipation_constant_for_torques[:] = (
-            np.asarray(nu_for_torques) * elemental_mass
-        )
-    _assert_dim(
-        dissipation_constant_for_torques, 2, "dissipation constant (nu) for torque)"
-    )
+        mass[:] = density * volume
 
     # Generate rest sigma and rest kappa, use user input if defined
     # set rest strains and curvature to be  zero at start
     # if found in kwargs modify (say for curved rod)
     if rest_sigma is None:
         rest_sigma = np.zeros((MaxDimension.value(), n_elements))
     _assert_shape(rest_sigma, (MaxDimension.value(), n_elements), "rest_sigma")
 
     if rest_kappa is None:
-        rest_kappa = np.zeros((MaxDimension.value(), n_elements - 1))
-    _assert_shape(rest_kappa, (MaxDimension.value(), n_elements - 1), "rest_kappa")
+        rest_kappa = np.zeros((MaxDimension.value(), n_voronoi_elements))
+    _assert_shape(rest_kappa, (MaxDimension.value(), n_voronoi_elements), "rest_kappa")
 
     # Compute rest voronoi length
-    rest_voronoi_lengths = 0.5 * (rest_lengths[1:] + rest_lengths[:-1])
+    rest_voronoi_lengths = 0.5 * (
+        rest_lengths_temp_for_voronoi[1:] + rest_lengths_temp_for_voronoi[:-1]
+    )
 
     # Allocate arrays for Cosserat Rod equations
-    velocities = np.zeros((MaxDimension.value(), n_elements + 1))
+    velocities = np.zeros((MaxDimension.value(), n_nodes))
     omegas = np.zeros((MaxDimension.value(), n_elements))
     accelerations = 0.0 * velocities
     angular_accelerations = 0.0 * omegas
-    # _vector_states = np.hstack(
-    #     (position, velocities, omegas, accelerations, angular_accelerations)
-    # )
-    # _matrix_states = directors.copy()
 
     internal_forces = 0.0 * accelerations
     internal_torques = 0.0 * angular_accelerations
 
     external_forces = 0.0 * accelerations
     external_torques = 0.0 * angular_accelerations
 
     lengths = np.zeros((n_elements))
     tangents = np.zeros((3, n_elements))
 
     dilatation = np.zeros((n_elements))
-    voronoi_dilatation = np.zeros((n_elements - 1))
+    voronoi_dilatation = np.zeros((n_voronoi_elements))
     dilatation_rate = np.zeros((n_elements))
 
     sigma = np.zeros((3, n_elements))
-    kappa = np.zeros((3, n_elements - 1))
+    kappa = np.zeros((3, n_voronoi_elements))
 
     internal_stress = np.zeros((3, n_elements))
-    internal_couple = np.zeros((3, n_elements - 1))
-
-    damping_forces = np.zeros((3, n_elements + 1))
-    damping_torques = np.zeros((3, n_elements))
+    internal_couple = np.zeros((3, n_voronoi_elements))
 
     return (
         n_elements,
         position,
         velocities,
         omegas,
         accelerations,
@@ -295,16 +275,14 @@
         mass_second_moment_of_inertia,
         inv_mass_second_moment_of_inertia,
         shear_matrix,
         bend_matrix,
         density_array,
         volume,
         mass,
-        dissipation_constant_for_forces,
-        dissipation_constant_for_torques,
         internal_forces,
         internal_torques,
         external_forces,
         external_torques,
         lengths,
         rest_lengths,
         tangents,
@@ -314,19 +292,53 @@
         rest_voronoi_lengths,
         sigma,
         kappa,
         rest_sigma,
         rest_kappa,
         internal_stress,
         internal_couple,
-        damping_forces,
-        damping_torques,
     )
 
 
+"""
+Cosserat rod constructor for straight-rod or ring rod geometry.
+
+
+Notes
+-----
+Since we expect the Cosserat Rod to simulate soft rod, Poisson's ratio is set to 0.5 by default.
+It is possible to give additional argument "shear_modulus" or "poisson_ratio" to specify extra modulus.
+
+
+Parameters
+----------
+n_elements : int
+    Number of element. Must be greater than 3. Generally recommended to start with 40-50, and adjust the resolution.
+direction : NDArray[3, float]
+    Direction of the rod in 3D
+normal : NDArray[3, float]
+    Normal vector of the rod in 3D
+base_length : float
+    Total length of the rod
+base_radius : float
+    Uniform radius of the rod
+density : float
+    Density of the rod
+youngs_modulus : float
+    Young's modulus
+**kwargs : dict, optional
+    The "position" and/or "directors" can be overrided by passing "position" and "directors" argument.
+    Remember, the shape of the "position" is (3,n_elements+1) and the shape of the "directors" is (3,3,n_elements).
+
+Returns
+-------
+
+"""
+
+
 def _assert_dim(vector, max_dim: int, name: str):
     assert vector.ndim < max_dim, (
         f"Input {name} dimension is not correct {vector.shape}"
         + f" It should be maximum {max_dim}D vector or single floating number."
     )
 
 
@@ -395,7 +407,23 @@
     # Check if computed tangents from position is the same with d3
     assert_allclose(
         tangents,
         d3,
         atol=Tolerance.atol(),
         err_msg=" Tangent vector computed using node positions is different than d3 vector of input directors",
     )
+
+
+def _position_validity_checker_ring_rod(position, ring_center_position, n_elements):
+    """Checker on user-defined position validity"""
+    _assert_shape(position, (MaxDimension.value(), n_elements), "position")
+
+    # Check if the start position of the rod and first entry of position array are the same
+    assert_allclose(
+        np.mean(position, axis=1),
+        ring_center_position,
+        atol=Tolerance.atol(),
+        err_msg=str(
+            "Ring rod center " + " (" + str(np.mean(position, axis=1)) + " ) "
+            " is different than ring center " + " (" + str(ring_center_position) + " ) "
+        ),
+    )
```

### Comparing `pyelastica-0.3.0/elastica/rod/knot_theory.py` & `pyelastica-0.3.1/elastica/rod/knot_theory.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,21 +5,14 @@
 Following example cases includes computing LWT quantities to study the bifurcation:
 
 - `Example case (PlectonemesCase) <https://github.com/GazzolaLab/PyElastica/blob/master/examples/RodContactCase/RodSelfContact/PlectonemesCase/plectoneme_case.py>`_
 - `Example case (SolenoidCase) <https://github.com/GazzolaLab/PyElastica/blob/master/examples/RodContactCase/RodSelfContact/SolenoidsCase/solenoid_case.py>`_
 
 The details discussion is included in `N Charles et. al. PRL (2019) <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.123.208003>`_.
 """
-__all__ = [
-    "KnotTheoryCompatibleProtocol",
-    "KnotTheory",
-    "compute_twist",
-    "compute_link",
-    "compute_writhe",
-]
 
 import sys
 
 if sys.version_info.minor >= 8:
     # typing Protocol is introduced in python 3.8
     from typing import Protocol
 elif sys.version_info.minor < 8:
```

### Comparing `pyelastica-0.3.0/elastica/rod/rod_base.py` & `pyelastica-0.3.1/elastica/rod/rod_base.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/systems/__init__.py` & `pyelastica-0.3.1/elastica/systems/__init__.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/systems/analytical.py` & `pyelastica-0.3.1/elastica/systems/analytical.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,12 @@
 __doc__ = "Analytically integrable systems, used primarily for testing time-steppers of Elastica Numba implementation"
 
 import numpy as np
-import numba
-from elastica._rotations import _get_rotation_matrix, _rotate
-from elastica._linalg import _batch_matmul
+from elastica._rotations import _rotate
 from elastica.rod.data_structures import _RodSymplecticStepperMixin
-from elastica.rod.data_structures import _bootstrap_from_data
-from elastica.rod.data_structures import _KinematicState, _DynamicState
 
 
 class BaseStatefulSystem:
     def __init__(self):
         pass
 
     @property
```

### Comparing `pyelastica-0.3.0/elastica/timestepper/__init__.py` & `pyelastica-0.3.1/elastica/timestepper/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,9 @@
 __doc__ = """Timestepping utilities to be used with Rod and RigidBody classes"""
-__all__ = [
-    "integrate",
-    "PositionVerlet",
-    "PEFRL",
-    "RungeKutta4",
-    "EulerForward",
-    "extend_stepper_interface",
-]
+
 
 import numpy as np
 from tqdm import tqdm
 from elastica.timestepper.symplectic_steppers import (
     SymplecticStepperTag,
     PositionVerlet,
     PEFRL,
```

### Comparing `pyelastica-0.3.0/elastica/timestepper/_stepper_interface.py` & `pyelastica-0.3.1/elastica/timestepper/_stepper_interface.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 __doc__ = "Time stepper interface"
 
-import numpy as np
-
 
 class _TimeStepper:
     """Interface classes for all time-steppers"""
 
     def __init__(self):
         pass
```

### Comparing `pyelastica-0.3.0/elastica/timestepper/explicit_steppers.py` & `pyelastica-0.3.1/elastica/timestepper/explicit_steppers.py`

 * *Files identical despite different names*

### Comparing `pyelastica-0.3.0/elastica/timestepper/symplectic_steppers.py` & `pyelastica-0.3.1/elastica/timestepper/symplectic_steppers.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 __doc__ = """Symplectic time steppers and concepts for integrating the kinematic and dynamic equations of rod-like objects.  """
 
 import numpy as np
-import math
 
 # from elastica._elastica_numba._timestepper._symplectic_steppers import (
 #     SymplecticStepperTag,
 #     PositionVerlet,
 #     PEFRL,
 # )
```

### Comparing `pyelastica-0.3.0/elastica/transformations.py` & `pyelastica-0.3.1/elastica/transformations.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 __doc__ = """ Rotation interface functions"""
-__all__ = ["skew_symmetrize", "inv_skew_symmetrize", "rotate"]
 
 import numpy as np
 
 from elastica._rotations import (
     _inv_skew_symmetrize,
     _skew_symmetrize,
     _rotate,
```

### Comparing `pyelastica-0.3.0/elastica/utils.py` & `pyelastica-0.3.1/elastica/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 """ Handy utilities
 """
-__all__ = ["isqrt"]
+
 import functools
 import numpy as np
 from numpy import finfo, float64
 from itertools import islice
 from scipy.interpolate import BSpline
```

### Comparing `pyelastica-0.3.0/elastica/wrappers.py` & `pyelastica-0.3.1/elastica/wrappers.py`

 * *Files 18% similar despite different names*

```diff
@@ -4,18 +4,20 @@
     "BaseSystemCollection",
     "Connections",
     "Constraints",
     "Forcing",
     "CallBacks",
     "Damping",
 ]
+
 from elastica.modules.base_system import BaseSystemCollection
 from elastica.modules.connections import Connections
 from elastica.modules.constraints import Constraints
 from elastica.modules.forcing import Forcing
 from elastica.modules.callbacks import CallBacks
 from elastica.modules.damping import Damping
 
+
 warnings.warn(
     "elastica.wrappers is refactored to elastica.modules in version 0.3.0.",
     DeprecationWarning,
 )
```

### Comparing `pyelastica-0.3.0/setup.py` & `pyelastica-0.3.1/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,55 +1,182 @@
-# -*- coding: utf-8 -*-
-from setuptools import setup
-
-packages = \
-['elastica',
- 'elastica.collision',
- 'elastica.experimental',
- 'elastica.experimental.connection_contact_joint',
- 'elastica.memory_block',
- 'elastica.modules',
- 'elastica.reset_functions_for_block_structure',
- 'elastica.rigidbody',
- 'elastica.rod',
- 'elastica.systems',
- 'elastica.timestepper']
-
-package_data = \
-{'': ['*']}
-
-install_requires = \
-['numba>=0.55.0,<0.56.0',
- 'numpy>=1.19.2,<2.0.0',
- 'scipy>=1.5.2,<2.0.0',
- 'tqdm>=4.61.1,<5.0.0']
-
-extras_require = \
-{'docs': ['Sphinx[docs]>=4.4.0,<5.0.0',
-          'sphinx-book-theme[docs]>=0.3.2,<0.4.0',
-          'readthedocs-sphinx-search[docs]>=0.1.1,<0.2.0',
-          'sphinx-autodoc-typehints[docs]>=1.17.1,<2.0.0',
-          'myst-parser[docs]>=0.17.2,<0.18.0',
-          'numpydoc[docs]>=1.3.1,<2.0.0',
-          'docutils[docs]>=0.17.1,<0.18.0'],
- 'examples': ['cma[examples]>=3.2.2,<4.0.0',
-              'matplotlib[examples]>=3.3.2,<4.0.0']}
-
-setup_kwargs = {
-    'name': 'pyelastica',
-    'version': '0.3.0',
-    'description': 'Elastica is a software to simulate the dynamics of filaments that, at every cross-section, can undergo all six possible modes of deformation, allowing the filament to bend, twist, stretch and shear, while interacting with complex environments via muscular activity, surface contact, friction and hydrodynamics.',
-    'long_description': "<div align='center'>\n<h1> PyElastica </h1>\n\n[![Build_status][badge-travis]][link-travis] [![CI][badge-CI]][link-CI] [![Documentation Status][badge-docs-status]][link-docs-status] [![codecov][badge-codecov]][link-codecov] [![Downloads][badge-pepy-download-count]][link-pepy-download-count] [![Binder][badge-binder]][link-binder] [![Gitter][badge-gitter]][link-gitter]\n </div>\n \nPyElastica is the python implementation of **Elastica**: an *open-source* project for simulating assemblies of slender, one-dimensional structures using Cosserat Rod theory.\n\n[![gallery][link-readme-gallary]][link-project-website]\n\nVisit [cosseratrods.org][link-project-website] for more information and learn about Elastica and Cosserat rod theory.\n\n## How to Start \n[![PyPI version][badge-pypi]][link-pypi] [![Documentation Status][badge-docs-status]][link-docs-status]\n\nPyElastica is compatible with Python 3.7 - 3.10.\n\n~~~bash\n$ pip install pyelastica \n~~~\n\nDocumentation of PyElastica is available [here][link-docs-website].\n\n## Citation\n\nWe ask that any publications which use Elastica cite as following:\n\n```\n@misc{tekinalp2022pyelastica,\n  title={PyElastica: A computational framework for Cosserat rod assemblies},\n  author={Tekinalp, Arman and Kim, Seung Hyun and Parthasarathy, Tejaswin and Bhosale, Yashraj},\n  journal={https://github.com/GazzolaLab/PyElastica},\n  year={2022},\n  publisher={GitHub}\n}\n```\n\n<details>\n  <summary><h4>References</h4></summary>\n \n- Gazzola, Dudte, McCormick, Mahadevan, <strong>Forward and inverse problems in the mechanics of soft filaments</strong>, Royal Society Open Science, 2018. doi: [10.1098/rsos.171628](https://doi.org/10.1098/rsos.171628)\n- Zhang, Chan, Parthasarathy, Gazzola, <strong>Modeling and simulation of complex dynamic musculoskeletal architectures</strong>, Nature Communications, 2019. doi: [10.1038/s41467-019-12759-5](https://doi.org/10.1038/s41467-019-12759-5)\n\n</details>\n\n## List of publications and submissions\n\n- [Control-oriented modeling of bend propagation in an octopus arm](https://arxiv.org/abs/2110.07211) (UIUC, 2021)\n- [A physics-informed, vision-based method to reconstruct all deformation modes in slender bodies](https://arxiv.org/abs/2109.08372) (UIUC, 2021) (IEEE ICRA 2022) [code](https://github.com/GazzolaLab/BR2-vision-based-smoothing)\n- [Optimal control of a soft CyberOctopus arm](https://ieeexplore.ieee.org/document/9483284) (UIUC, 2021) (ACC 2021)\n- [Elastica: A compliant mechanics environment for soft robotic control](https://ieeexplore.ieee.org/document/9369003) (UIUC, 2021) (IEEE RA-L 2021)\n- [Controlling a CyberOctopus soft arm with muscle-like actuation](https://arxiv.org/abs/2010.03368) (UIUC, 2020)\n- [Energy shaping control of a CyberOctopus soft arm](https://ieeexplore.ieee.org/document/9304408) (UIUC, 2020) (IEEE CDC 2020)\n\n## Tutorials\n[![Binder][badge-binder-tutorial]][link-binder]\n\nWe have created several Jupyter notebooks and Python scripts to help users get started with PyElastica. The Jupyter notebooks are available on Binder, allowing you to try out some of the tutorials without having to install PyElastica.\n\nWe have also included an example script for visualizing PyElastica simulations using POVray. This script is located in the examples folder ([`examples/visualization`](examples/visualization)).\n\n## Contribution\n\nIf you would like to participate, please read our [contribution guideline](CONTRIBUTING.md)\n\nPyElastica is developed by the [Gazzola Lab][link-lab-website] at the University of Illinois at Urbana-Champaign.\n\n## Senior Developers ✨\n_Names arranged alphabetically_\n- Arman Tekinalp\n- Chia-Hsien Shih (Cathy)\n- Fan Kiat Chan\n- Noel Naughton\n- [Seung Hyun Kim](https://github.com/skim0119)\n- Tejaswin Parthasarathy (Teja)\n- [Yashraj Bhosale](https://github.com/bhosale2)\n\n[//]: # (Collection of URLs.)\n\n[link-readme-gallary]: https://github.com/skim0119/PyElastica/blob/assets_logo/assets/alpha_gallery.gif\n\n[link-project-website]: https://cosseratrods.org\n[link-lab-website]: http://mattia-lab.com/\n[link-docs-website]: https://docs.cosseratrods.org/\n\n[badge-pypi]: https://badge.fury.io/py/pyelastica.svg\n[badge-travis]: https://travis-ci.com/GazzolaLab/PyElastica.svg?branch=master\n[badge-CI]: https://github.com/GazzolaLab/PyElastica/workflows/CI/badge.svg\n[badge-docs-status]: https://readthedocs.org/projects/pyelastica/badge/?version=latest\n[badge-binder]: https://mybinder.org/badge_logo.svg\n[badge-pepy-download-count]: https://pepy.tech/badge/pyelastica\n[badge-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica/branch/master/graph/badge.svg\n[badge-gitter]: https://badges.gitter.im/PyElastica/community.svg\n[link-pypi]: https://badge.fury.io/py/pyelastica\n[link-travis]: https://travis-ci.com/github/GazzolaLab/PyElastica\n[link-CI]: https://github.com/GazzolaLab/PyElastica/actions\n[link-docs-status]: https://docs.cosseratrods.org/en/latest/?badge=latest\n[link-pepy-download-count]: https://pepy.tech/project/pyelastica\n[link-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica\n\n[badge-binder-tutorial]: https://img.shields.io/badge/Launch-PyElastica%20Tutorials-579ACA.svg?logo=data:image/png;base64,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\n[link-binder]: https://mybinder.org/v2/gh/GazzolaLab/PyElastica/master?filepath=examples%2FBinder%2F0_PyElastica_Tutorials_Overview.ipynb\n[link-gitter]: https://gitter.im/PyElastica/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge\n",
-    'author': 'GazzolaLab',
-    'author_email': 'armant2@illinois.edu',
-    'maintainer': None,
-    'maintainer_email': None,
-    'url': 'https://www.cosseratrods.org/',
-    'packages': packages,
-    'package_data': package_data,
-    'install_requires': install_requires,
-    'extras_require': extras_require,
-    'python_requires': '>=3.7,<3.11',
+Metadata-Version: 2.1
+Name: pyelastica
+Version: 0.3.1
+Summary: Elastica is a software to simulate the dynamics of filaments that, at every cross-section, can undergo all six possible modes of deformation, allowing the filament to bend, twist, stretch and shear, while interacting with complex environments via muscular activity, surface contact, friction and hydrodynamics.
+Home-page: https://www.cosseratrods.org/
+License: MIT
+Author: GazzolaLab
+Author-email: armant2@illinois.edu
+Requires-Python: >=3.8,<3.11
+Classifier: Development Status :: 3 - Alpha
+Classifier: Intended Audience :: Education
+Classifier: Intended Audience :: Science/Research
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: Implementation :: CPython
+Provides-Extra: docs
+Provides-Extra: examples
+Provides-Extra: magnetism
+Requires-Dist: Sphinx (>=6.1,<7.0) ; extra == "docs"
+Requires-Dist: cma (>=3.2.2,<4.0.0) ; extra == "examples"
+Requires-Dist: docutils (>=0.18,<0.19) ; extra == "docs"
+Requires-Dist: magneto_pyelastica (>=0.0.1,<0.0.2) ; extra == "magnetism"
+Requires-Dist: matplotlib (>=3.3.2,<4.0.0) ; extra == "examples"
+Requires-Dist: myst-parser (>=1.0,<2.0) ; extra == "docs"
+Requires-Dist: numba (>=0.55.0,<0.56.0)
+Requires-Dist: numpy (>=1.19.2,<2.0.0)
+Requires-Dist: numpydoc (>=1.3.1,<2.0.0) ; extra == "docs"
+Requires-Dist: readthedocs-sphinx-search (>=0.1.1,<0.2.0) ; extra == "docs"
+Requires-Dist: scipy (>=1.5.2,<2.0.0)
+Requires-Dist: sphinx-autodoc-typehints (>=1.21,<2.0) ; extra == "docs"
+Requires-Dist: sphinx-book-theme (>=1.0,<2.0) ; extra == "docs"
+Requires-Dist: tqdm (>=4.61.1,<5.0.0)
+Project-URL: Documentation, https://docs.cosseratrods.org/en/latest/
+Project-URL: Repository, https://github.com/GazzolaLab/PyElastica
+Description-Content-Type: text/markdown
+
+<div align='center'>
+<h1> PyElastica </h1>
+
+[![Build_status][badge-travis]][link-travis] [![CI][badge-CI]][link-CI] [![Documentation Status][badge-docs-status]][link-docs-status] [![codecov][badge-codecov]][link-codecov] [![Downloads][badge-pepy-download-count]][link-pepy-download-count] [![DOI][badge-doi]][link-doi] [![Binder][badge-binder]][link-binder] [![Gitter][badge-gitter]][link-gitter]
+ </div>
+
+PyElastica is the python implementation of **Elastica**: an *open-source* project for simulating assemblies of slender, one-dimensional structures using Cosserat Rod theory.
+
+[![gallery][link-readme-gallary]][link-project-website]
+
+Visit [cosseratrods.org][link-project-website] for more information and learn about Elastica and Cosserat rod theory.
+
+## How to Start
+[![PyPI version][badge-pypi]][link-pypi] [![Documentation Status][badge-docs-status]][link-docs-status]
+
+PyElastica is compatible with Python 3.8 - 3.10.
+
+~~~bash
+$ pip install pyelastica
+~~~
+
+With this you get a minimal version with very little dependencies.
+
+All options:
+- `magnetism`: use this if you want to simulate magnetic Cosserat rods
+interacting with external magnetic environments (details can be found [here](https://github.com/armantekinalp/MagnetoPyElastica)) .
+- `examples`: installs dependencies to run example cases,
+found under the folder `examples`.
+- `docs`: packages to build documentation
+
+Options can be combined e.g.
+```bash
+pip install "pyelastica[magnetism,examples,docs]"
+```
+
+Documentation of PyElastica is available [here][link-docs-website].
+
+Example cases for simulating magnetic Cosserat rods can be found [here](https://github.com/armantekinalp/MagnetoPyElastica).
+## Citation
+
+We ask that any publications which use Elastica cite as following:
+
+```
+@software{arman_tekinalp_2023_7931429,
+  author       = {Arman Tekinalp and
+                  Seung Hyun Kim and
+                  Yashraj Bhosale and
+                  Tejaswin Parthasarathy and
+                  Noel Naughton and
+                  Ilia Nasiriziba and
+                  Songyuan Cui and
+                  Maximilian Stölzle and
+                  Chia-Hsien (Cathy) Shih and
+                  Mattia Gazzola
+                  },
+  title        = {GazzolaLab/PyElastica: v0.3.1},
+  month        = may,
+  year         = 2023,
+  publisher    = {Zenodo},
+  version      = {v0.3.1},
+  doi          = {10.5281/zenodo.7931429},
+  url          = {https://doi.org/10.5281/zenodo.7931429}
 }
+```
+
+<details>
+  <summary><h4>References</h4></summary>
+
+- Gazzola, Dudte, McCormick, Mahadevan, <strong>Forward and inverse problems in the mechanics of soft filaments</strong>, Royal Society Open Science, 2018. doi: [10.1098/rsos.171628](https://doi.org/10.1098/rsos.171628)
+- Zhang, Chan, Parthasarathy, Gazzola, <strong>Modeling and simulation of complex dynamic musculoskeletal architectures</strong>, Nature Communications, 2019. doi: [10.1038/s41467-019-12759-5](https://doi.org/10.1038/s41467-019-12759-5)
 
+</details>
+
+## List of publications and submissions
+- [Topology, dynamics, and control of an octopus-analog muscular hydrostat](https://arxiv.org/abs/2304.08413) (UIUC, 2023)
+- [Hierarchical control and learning of a foraging CyberOctopus](https://arxiv.org/abs/2302.05811) (UIUC, 2023)
+- [Energy-shaping control of a muscular octopus arm moving in three dimensions](https://royalsocietypublishing.org/doi/full/10.1098/rspa.2022.0593) (UIUC, 2023) (Proceedings of the Royal Society A 2023)
+- [A sensory feedback control law for octopus arm movements](https://ieeexplore.ieee.org/abstract/document/9993021/) (UIUC, 2022) (IEEE CDC 2022)
+- [Control-oriented modeling of bend propagation in an octopus arm](https://ieeexplore.ieee.org/abstract/document/9867689/) (UIUC, 2021) (IEEE ACC 2022)
+- [A physics-informed, vision-based method to reconstruct all deformation modes in slender bodies](https://arxiv.org/abs/2109.08372) (UIUC, 2021) (IEEE ICRA 2022) [code](https://github.com/GazzolaLab/BR2-vision-based-smoothing)
+- [Optimal control of a soft CyberOctopus arm](https://ieeexplore.ieee.org/document/9483284) (UIUC, 2021) (IEEE ACC 2021)
+- [Elastica: A compliant mechanics environment for soft robotic control](https://ieeexplore.ieee.org/document/9369003) (UIUC, 2021) (IEEE RA-L 2021)
+- [Controlling a CyberOctopus soft arm with muscle-like actuation](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9683318) (UIUC, 2020) (IEEE CDC 2021)
+- [Energy shaping control of a CyberOctopus soft arm](https://ieeexplore.ieee.org/document/9304408) (UIUC, 2020) (IEEE CDC 2020)
+
+## Tutorials
+[![Binder][badge-binder-tutorial]][link-binder]
+
+We have created several Jupyter notebooks and Python scripts to help users get started with PyElastica. The Jupyter notebooks are available on Binder, allowing you to try out some of the tutorials without having to install PyElastica.
+
+We have also included an example script for visualizing PyElastica simulations using POVray. This script is located in the examples folder ([`examples/visualization`](examples/visualization)).
+
+## Contribution
+
+If you would like to participate, please read our [contribution guideline](CONTRIBUTING.md)
+
+PyElastica is developed by the [Gazzola Lab][link-lab-website] at the University of Illinois at Urbana-Champaign.
+
+## Senior Developers ✨
+_Names arranged alphabetically_
+- Arman Tekinalp
+- Chia-Hsien Shih (Cathy)
+- Fan Kiat Chan
+- Ilia Nasiriziba
+- Noel Naughton
+- [Seung Hyun Kim](https://github.com/skim0119)
+- Songyuan Cui
+- Tejaswin Parthasarathy (Teja)
+- [Yashraj Bhosale](https://github.com/bhosale2)
+
+[//]: # (Collection of URLs.)
+
+[link-readme-gallary]: https://github.com/skim0119/PyElastica/blob/assets_logo/assets/alpha_gallery.gif
+
+[link-project-website]: https://cosseratrods.org
+[link-lab-website]: http://mattia-lab.com/
+[link-docs-website]: https://docs.cosseratrods.org/
+
+[badge-pypi]: https://badge.fury.io/py/pyelastica.svg
+[badge-travis]: https://travis-ci.com/GazzolaLab/PyElastica.svg?branch=master
+[badge-CI]: https://github.com/GazzolaLab/PyElastica/workflows/CI/badge.svg
+[badge-docs-status]: https://readthedocs.org/projects/pyelastica/badge/?version=latest
+[badge-binder]: https://mybinder.org/badge_logo.svg
+[badge-pepy-download-count]: https://pepy.tech/badge/pyelastica
+[badge-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica/branch/master/graph/badge.svg
+[badge-gitter]: https://badges.gitter.im/PyElastica/community.svg
+[badge-doi]: https://zenodo.org/badge/254172891.svg
+[link-pypi]: https://badge.fury.io/py/pyelastica
+[link-travis]: https://travis-ci.com/github/GazzolaLab/PyElastica
+[link-CI]: https://github.com/GazzolaLab/PyElastica/actions
+[link-docs-status]: https://docs.cosseratrods.org/en/latest/?badge=latest
+[link-pepy-download-count]: https://pepy.tech/project/pyelastica
+[link-codecov]: https://codecov.io/gh/GazzolaLab/PyElastica
+
+[badge-binder-tutorial]: https://img.shields.io/badge/Launch-PyElastica%20Tutorials-579ACA.svg?logo=data:image/png;base64,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
+[link-binder]: https://mybinder.org/v2/gh/GazzolaLab/PyElastica/master?filepath=examples%2FBinder%2F0_PyElastica_Tutorials_Overview.ipynb
+[link-gitter]: https://gitter.im/PyElastica/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
+[link-doi]: https://zenodo.org/badge/latestdoi/254172891
 
-setup(**setup_kwargs)
```

