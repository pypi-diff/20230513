# Comparing `tmp/thefittest-0.1.8.tar.gz` & `tmp/thefittest-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "G:\My Drive\4.GitHubClones\thefittest_msi\thefittest\thefittest\dist\.tmp-65yvryr7\thefittest-0.1.8.tar", last modified: Fri Mar 17 11:28:10 2023, max compression
+gzip compressed data, was "thefittest-0.1.9.tar", last modified: Sat Mar 18 10:28:51 2023, max compression
```

## Comparing `thefittest-0.1.8.tar` & `thefittest-0.1.9.tar`

### file list

```diff
@@ -1,100 +1,100 @@
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:10.000000 thefittest-0.1.8/
--rw-rw-rw-   0        0        0     1089 2023-02-20 04:21:15.000000 thefittest-0.1.8/LICENSE
--rw-rw-rw-   0        0        0     3159 2023-03-17 11:28:10.000000 thefittest-0.1.8/PKG-INFO
--rw-rw-rw-   0        0        0     2657 2023-03-17 11:17:51.000000 thefittest-0.1.8/README.md
--rw-rw-rw-   0        0        0      779 2023-03-17 11:27:44.000000 thefittest-0.1.8/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-03-17 11:28:10.000000 thefittest-0.1.8/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:08.000000 thefittest-0.1.8/src/
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:09.000000 thefittest-0.1.8/src/thefittest/
--rw-rw-rw-   0        0        0        2 2023-02-20 04:21:15.000000 thefittest-0.1.8/src/thefittest/__init__.py
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:09.000000 thefittest-0.1.8/src/thefittest/benchmarks/
--rw-rw-rw-   0        0        0     7167 2023-02-28 13:33:54.000000 thefittest-0.1.8/src/thefittest/benchmarks/CEC2005.py
--rw-rw-rw-   0        0        0      339 2023-02-28 13:33:20.000000 thefittest-0.1.8/src/thefittest/benchmarks/__init__.py
--rw-rw-rw-   0        0        0    34988 2023-03-11 09:47:23.000000 thefittest-0.1.8/src/thefittest/benchmarks/_optproblems.py
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:09.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/EF8F2_func_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D50.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_func_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D50.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_func_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D50.txt
--rw-rw-rw-   0        0        0      402 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/fbias_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D50.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_func_data.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/high_cond_elliptic_rot_data.txt
--rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D10.txt
--rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D2.txt
--rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D30.txt
--rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D50.txt
--rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_data.txt
--rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D10.txt
--rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D2.txt
--rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D30.txt
--rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D50.txt
--rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_data.txt
--rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D10.txt
--rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D2.txt
--rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D30.txt
--rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D50.txt
--rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D10.txt
--rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D2.txt
--rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D30.txt
--rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D50.txt
--rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_data.txt
--rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D10.txt
--rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D2.txt
--rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D30.txt
--rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D50.txt
--rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D50.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_func_data.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rosenbrock_func_data.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_102_data.txt
--rw-rw-rw-   0        0        0   161802 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_206_data.txt
--rw-rw-rw-   0        0        0   322002 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_213_data.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/sphere_func_data.txt
--rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D10.txt
--rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D2.txt
--rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D30.txt
--rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D50.txt
--rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_data.txt
--rw-rw-rw-   0        0        0     4067 2023-03-01 09:30:43.000000 thefittest-0.1.8/src/thefittest/benchmarks/symbolicregression17.py
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:10.000000 thefittest-0.1.8/src/thefittest/optimizers/
--rw-rw-rw-   0        0        0      356 2023-02-21 07:44:43.000000 thefittest-0.1.8/src/thefittest/optimizers/__init__.py
--rw-rw-rw-   0        0        0    11771 2023-03-16 12:43:54.000000 thefittest-0.1.8/src/thefittest/optimizers/_base.py
--rw-rw-rw-   0        0        0     7864 2023-03-11 09:50:09.000000 thefittest-0.1.8/src/thefittest/optimizers/_differentialevolution.py
--rw-rw-rw-   0        0        0     9306 2023-03-13 15:47:37.000000 thefittest-0.1.8/src/thefittest/optimizers/_geneticalgorithm.py
--rw-rw-rw-   0        0        0    10347 2023-03-17 09:06:22.000000 thefittest-0.1.8/src/thefittest/optimizers/_geneticprogramming.py
--rw-rw-rw-   0        0        0     9613 2023-03-11 09:52:55.000000 thefittest-0.1.8/src/thefittest/optimizers/_jade.py
--rw-rw-rw-   0        0        0     8370 2023-03-11 09:53:32.000000 thefittest-0.1.8/src/thefittest/optimizers/_jde.py
--rw-rw-rw-   0        0        0    11135 2023-03-11 09:54:25.000000 thefittest-0.1.8/src/thefittest/optimizers/_sade2005.py
--rw-rw-rw-   0        0        0    11589 2023-03-14 12:29:12.000000 thefittest-0.1.8/src/thefittest/optimizers/_selfcga.py
--rw-rw-rw-   0        0        0    11501 2023-03-17 10:39:47.000000 thefittest-0.1.8/src/thefittest/optimizers/_selfcgp.py
--rw-rw-rw-   0        0        0    10549 2023-03-11 09:57:11.000000 thefittest-0.1.8/src/thefittest/optimizers/_shade.py
--rw-rw-rw-   0        0        0     9312 2023-03-11 09:57:56.000000 thefittest-0.1.8/src/thefittest/optimizers/_shaga.py
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:10.000000 thefittest-0.1.8/src/thefittest/tools/
--rw-rw-rw-   0        0        0        0 2023-02-21 06:14:04.000000 thefittest-0.1.8/src/thefittest/tools/__init__.py
--rw-rw-rw-   0        0        0     3566 2023-03-15 09:11:56.000000 thefittest-0.1.8/src/thefittest/tools/generators.py
--rw-rw-rw-   0        0        0     3061 2023-03-16 13:55:43.000000 thefittest-0.1.8/src/thefittest/tools/numba_funcs.py
--rw-rw-rw-   0        0        0    18269 2023-03-17 09:15:00.000000 thefittest-0.1.8/src/thefittest/tools/operators.py
--rw-rw-rw-   0        0        0     6578 2023-03-16 14:29:09.000000 thefittest-0.1.8/src/thefittest/tools/transformations.py
-drwxrwxrwx   0        0        0        0 2023-03-17 11:28:09.000000 thefittest-0.1.8/src/thefittest.egg-info/
--rw-rw-rw-   0        0        0     3159 2023-03-17 11:28:08.000000 thefittest-0.1.8/src/thefittest.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     4662 2023-03-17 11:28:08.000000 thefittest-0.1.8/src/thefittest.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-03-17 11:28:08.000000 thefittest-0.1.8/src/thefittest.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-03-17 11:28:08.000000 thefittest-0.1.8/src/thefittest.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:51.700000 thefittest-0.1.9/
+-rw-rw-rw-   0        0        0     1089 2023-02-20 04:21:15.000000 thefittest-0.1.9/LICENSE
+-rw-rw-rw-   0        0        0     3166 2023-03-18 10:28:51.694000 thefittest-0.1.9/PKG-INFO
+-rw-rw-rw-   0        0        0     2657 2023-03-17 11:17:51.000000 thefittest-0.1.9/README.md
+-rw-rw-rw-   0        0        0      793 2023-03-18 10:27:53.000000 thefittest-0.1.9/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-03-18 10:28:51.698000 thefittest-0.1.9/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:50.531000 thefittest-0.1.9/src/
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:50.582000 thefittest-0.1.9/src/thefittest/
+-rw-rw-rw-   0        0        0        2 2023-02-20 04:21:15.000000 thefittest-0.1.9/src/thefittest/__init__.py
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:50.651000 thefittest-0.1.9/src/thefittest/benchmarks/
+-rw-rw-rw-   0        0        0     7167 2023-02-28 13:33:54.000000 thefittest-0.1.9/src/thefittest/benchmarks/CEC2005.py
+-rw-rw-rw-   0        0        0      339 2023-02-28 13:33:20.000000 thefittest-0.1.9/src/thefittest/benchmarks/__init__.py
+-rw-rw-rw-   0        0        0    34988 2023-03-11 09:47:23.000000 thefittest-0.1.9/src/thefittest/benchmarks/_optproblems.py
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:51.459000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/EF8F2_func_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D50.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_func_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D50.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_func_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D50.txt
+-rw-rw-rw-   0        0        0      402 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/fbias_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D50.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_func_data.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/high_cond_elliptic_rot_data.txt
+-rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D10.txt
+-rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D2.txt
+-rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D30.txt
+-rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D50.txt
+-rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_data.txt
+-rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D10.txt
+-rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D2.txt
+-rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D30.txt
+-rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D50.txt
+-rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_data.txt
+-rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D10.txt
+-rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D2.txt
+-rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D30.txt
+-rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D50.txt
+-rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D10.txt
+-rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D2.txt
+-rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D30.txt
+-rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D50.txt
+-rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_data.txt
+-rw-rw-rw-   0        0        0    25200 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D10.txt
+-rw-rw-rw-   0        0        0     1040 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D2.txt
+-rw-rw-rw-   0        0        0   225600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D30.txt
+-rw-rw-rw-   0        0        0   626000 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D50.txt
+-rw-rw-rw-   0        0        0    16020 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D50.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_func_data.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rosenbrock_func_data.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_102_data.txt
+-rw-rw-rw-   0        0        0   161802 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_206_data.txt
+-rw-rw-rw-   0        0        0   322002 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_213_data.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/sphere_func_data.txt
+-rw-rw-rw-   0        0        0     2520 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D10.txt
+-rw-rw-rw-   0        0        0      104 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D2.txt
+-rw-rw-rw-   0        0        0    22560 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D30.txt
+-rw-rw-rw-   0        0        0    62600 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D50.txt
+-rw-rw-rw-   0        0        0     1602 2023-02-20 04:21:16.000000 thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_data.txt
+-rw-rw-rw-   0        0        0     4067 2023-03-01 09:30:43.000000 thefittest-0.1.9/src/thefittest/benchmarks/symbolicregression17.py
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:51.629000 thefittest-0.1.9/src/thefittest/optimizers/
+-rw-rw-rw-   0        0        0      356 2023-02-21 07:44:43.000000 thefittest-0.1.9/src/thefittest/optimizers/__init__.py
+-rw-rw-rw-   0        0        0    11771 2023-03-16 12:43:54.000000 thefittest-0.1.9/src/thefittest/optimizers/_base.py
+-rw-rw-rw-   0        0        0     7864 2023-03-11 09:50:09.000000 thefittest-0.1.9/src/thefittest/optimizers/_differentialevolution.py
+-rw-rw-rw-   0        0        0     9306 2023-03-13 15:47:37.000000 thefittest-0.1.9/src/thefittest/optimizers/_geneticalgorithm.py
+-rw-rw-rw-   0        0        0    10347 2023-03-17 09:06:22.000000 thefittest-0.1.9/src/thefittest/optimizers/_geneticprogramming.py
+-rw-rw-rw-   0        0        0     9613 2023-03-11 09:52:55.000000 thefittest-0.1.9/src/thefittest/optimizers/_jade.py
+-rw-rw-rw-   0        0        0     8370 2023-03-11 09:53:32.000000 thefittest-0.1.9/src/thefittest/optimizers/_jde.py
+-rw-rw-rw-   0        0        0    11135 2023-03-11 09:54:25.000000 thefittest-0.1.9/src/thefittest/optimizers/_sade2005.py
+-rw-rw-rw-   0        0        0    11589 2023-03-14 12:29:12.000000 thefittest-0.1.9/src/thefittest/optimizers/_selfcga.py
+-rw-rw-rw-   0        0        0    11501 2023-03-18 09:05:48.000000 thefittest-0.1.9/src/thefittest/optimizers/_selfcgp.py
+-rw-rw-rw-   0        0        0    10549 2023-03-11 09:57:11.000000 thefittest-0.1.9/src/thefittest/optimizers/_shade.py
+-rw-rw-rw-   0        0        0     9312 2023-03-11 09:57:56.000000 thefittest-0.1.9/src/thefittest/optimizers/_shaga.py
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:51.689000 thefittest-0.1.9/src/thefittest/tools/
+-rw-rw-rw-   0        0        0        0 2023-02-21 06:14:04.000000 thefittest-0.1.9/src/thefittest/tools/__init__.py
+-rw-rw-rw-   0        0        0     3566 2023-03-15 09:11:56.000000 thefittest-0.1.9/src/thefittest/tools/generators.py
+-rw-rw-rw-   0        0        0     3282 2023-03-18 09:23:47.000000 thefittest-0.1.9/src/thefittest/tools/numba_funcs.py
+-rw-rw-rw-   0        0        0    18269 2023-03-17 09:15:00.000000 thefittest-0.1.9/src/thefittest/tools/operators.py
+-rw-rw-rw-   0        0        0     7924 2023-03-18 08:41:59.000000 thefittest-0.1.9/src/thefittest/tools/transformations.py
+drwxrwxrwx   0        0        0        0 2023-03-18 10:28:50.614000 thefittest-0.1.9/src/thefittest.egg-info/
+-rw-rw-rw-   0        0        0     3166 2023-03-18 10:28:50.000000 thefittest-0.1.9/src/thefittest.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     4662 2023-03-18 10:28:50.000000 thefittest-0.1.9/src/thefittest.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-03-18 10:28:50.000000 thefittest-0.1.9/src/thefittest.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-03-18 10:28:50.000000 thefittest-0.1.9/src/thefittest.egg-info/top_level.txt
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `thefittest-0.1.8/LICENSE` & `thefittest-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/PKG-INFO` & `thefittest-0.1.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 2.1
 Name: thefittest
-Version: 0.1.8
+Version: 0.1.9
 Summary: Implementation of data mining methods that use evolutionary algorithms
 Author-email: Pavel Sherstnev <sherstpasha99@gmail.com>
 Project-URL: Homepage, https://github.com/sherstpasha/thefittest
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
+Requires-Python: <=3.10,>=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # thefittest
 
 # the package contains methods
 * **Genetic algorithm** (Holland, J. H. (1992). Genetic algorithms. Scientific American, 267(1), 66-72):
```

### Comparing `thefittest-0.1.8/README.md` & `thefittest-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/pyproject.toml` & `thefittest-0.1.9/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,29 +1,29 @@
 [build-system]
-requires = ["setuptools>=57.4.0", "numpy==1.21.6", "numba==0.56.4"]
+requires = ["setuptools>=57.4.0", "numpy>=1.21.6,<=1.23", "numba>=0.56.4"]
 build-backend = "setuptools.build_meta"
 
 [tool.setuptools]
 include-package-data = true
 
 [tool.setuptools.packages.find]
 where = ["src"]
 
 [tool.setuptools.package-data]
 "*" = ["*.txt"]
 
 [project]
 name = "thefittest"
-version = "0.1.8"
+version = "0.1.9"
 authors = [
   { name="Pavel Sherstnev", email="sherstpasha99@gmail.com" },
 ]
 description = "Implementation of data mining methods that use evolutionary algorithms"
 readme = "README.md"
-requires-python = ">=3.7"
+requires-python = ">=3.7,<=3.10"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 
 [project.urls]
```

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/CEC2005.py` & `thefittest-0.1.9/src/thefittest/benchmarks/CEC2005.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/_optproblems.py` & `thefittest-0.1.9/src/thefittest/benchmarks/_optproblems.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/EF8F2_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/EF8F2_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/E_ScafferF6_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/E_ScafferF6_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/ackley_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/ackley_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/elliptic_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/elliptic_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/griewank_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/griewank_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/high_cond_elliptic_rot_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/high_cond_elliptic_rot_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D2.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D2.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func1_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func1_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D2.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D2.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func2_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func2_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D2.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D2.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_HM_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D2.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D2.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func3_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func3_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D2.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D2.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/hybrid_func4_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/hybrid_func4_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rastrigin_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rastrigin_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/rosenbrock_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/rosenbrock_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_102_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_102_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_206_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_206_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/schwefel_213_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/schwefel_213_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/sphere_func_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/sphere_func_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D10.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D10.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D30.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D30.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_M_D50.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_M_D50.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/shifts_data/weierstrass_data.txt` & `thefittest-0.1.9/src/thefittest/benchmarks/shifts_data/weierstrass_data.txt`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/benchmarks/symbolicregression17.py` & `thefittest-0.1.9/src/thefittest/benchmarks/symbolicregression17.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_base.py` & `thefittest-0.1.9/src/thefittest/optimizers/_base.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_differentialevolution.py` & `thefittest-0.1.9/src/thefittest/optimizers/_differentialevolution.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_geneticalgorithm.py` & `thefittest-0.1.9/src/thefittest/optimizers/_geneticalgorithm.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_geneticprogramming.py` & `thefittest-0.1.9/src/thefittest/optimizers/_geneticprogramming.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_jade.py` & `thefittest-0.1.9/src/thefittest/optimizers/_jade.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_jde.py` & `thefittest-0.1.9/src/thefittest/optimizers/_jde.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_sade2005.py` & `thefittest-0.1.9/src/thefittest/optimizers/_sade2005.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_selfcga.py` & `thefittest-0.1.9/src/thefittest/optimizers/_selfcga.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_selfcgp.py` & `thefittest-0.1.9/src/thefittest/optimizers/_selfcgp.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_shade.py` & `thefittest-0.1.9/src/thefittest/optimizers/_shade.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/optimizers/_shaga.py` & `thefittest-0.1.9/src/thefittest/optimizers/_shaga.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/tools/generators.py` & `thefittest-0.1.9/src/thefittest/tools/generators.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/tools/numba_funcs.py` & `thefittest-0.1.9/src/thefittest/tools/numba_funcs.py`

 * *Files 12% similar despite different names*

```diff
@@ -94,7 +94,15 @@
     indexes = np.arange(len(fitness))
     choosen = np.empty(quantity, dtype=np.int32)
     for i in range(quantity):
         tournament = np.random.choice(indexes, size=tour_size, replace=False)
         argmax = np.argmax(fitness[tournament])
         choosen[i] = tournament[argmax]
     return choosen
+
+
+@njit(int32(int32[:], int32[:]))
+def find_first_difference_between_two(array_1, array_2):
+    for i in range(min(len(array_1), len(array_2))):
+        if array_1[i] != array_2[i]:
+            break
+    return i
```

### Comparing `thefittest-0.1.8/src/thefittest/tools/operators.py` & `thefittest-0.1.9/src/thefittest/tools/operators.py`

 * *Files identical despite different names*

### Comparing `thefittest-0.1.8/src/thefittest/tools/transformations.py` & `thefittest-0.1.9/src/thefittest/tools/transformations.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 import numpy as np
 from .numba_funcs import find_common_id_in_trees
+from .numba_funcs import find_first_difference_between_two
+from .numba_funcs import find_end_subtree_from_i
 from numba.typed import List
 
 
 def root_mean_square_error(y_true, y_predict):
     return np.sqrt(np.mean((y_true - y_predict)**2))
 
 
 def coefficient_determination(y_true, y_predict):
     mean = np.mean(y_true)
     residual_sum = np.sum((y_true - y_predict)**2)
     total_sum = np.sum((y_true - mean)**2)
     return 1 - residual_sum/total_sum
 
 
-def common_region_(trees):
+def common_region(trees):
     terminate = False
     indexes = []
     common_indexes = []
     border_indexes = []
     for tree in trees:
         indexes.append(list(range(len(tree.nodes))))
         common_indexes.append([])
@@ -38,28 +40,65 @@
 
             if inner_break:
                 for j in range(0, len(indexes)):
                     border_indexes[j].append(indexes[j][i])
                 break
 
         for j in range(len(indexes)):
-            _, right = trees[j].subtree_(common_indexes[j][-1])
+            _, right = trees[j].subtree(common_indexes[j][-1])
             delete_to = indexes[j].index(right-1) + 1
             indexes[j] = indexes[j][delete_to:]
 
             if len(indexes[j]) < 1:
                 terminate = True
                 break
 
     return common_indexes, border_indexes
 
 
-def common_region(trees):
-    n_args_list = [tree.n_args for tree in trees]
-    return find_common_id_in_trees(List(n_args_list))
+def common_region_two_trees(n_args_array_1, n_args_array_2):
+    index_list_1 = range(len(n_args_array_1))
+    index_list_2 = range(len(n_args_array_2))
+    index_1 = 0
+    index_2 = 0
+
+    common_1 = []
+    common_2 = []
+    border_1 = []
+    border_2 = []
+
+    while True:
+        if index_1 < len(n_args_array_1) and index_2 < len(n_args_array_2):
+            id_1 = index_1
+            id_2 = index_2
+            end = find_first_difference_between_two(n_args_array_1[id_1:],
+                                                    n_args_array_2[id_2:])
+            index_1 = index_1 + end
+            index_2 = index_2 + end
+            common_1.extend(index_list_1[id_1:index_1+1])
+            common_2.extend(index_list_2[id_2:index_2+1])
+
+        if len(n_args_array_1)-1 > index_1 or len(n_args_array_2)-1 > index_2:
+            border_1.append(index_1)
+            border_2.append(index_2)
+            index_1 = find_end_subtree_from_i(index_1, n_args_array_1)
+            index_2 = find_end_subtree_from_i(index_2, n_args_array_2)
+        else:
+            break
+
+    return [common_1, common_2], [border_1, border_2]
+
+
+def common_region_(trees):
+    if len(trees) == 2:
+        to_return = common_region_two_trees(trees[0].n_args, trees[1].n_args)
+    else:
+        to_return = common_region_(trees)
+
+    return to_return
 
 
 def donothing(x):
     return x
 
 
 def numpy_group_by(group, by):
```

### Comparing `thefittest-0.1.8/src/thefittest.egg-info/PKG-INFO` & `thefittest-0.1.9/src/thefittest.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 2.1
 Name: thefittest
-Version: 0.1.8
+Version: 0.1.9
 Summary: Implementation of data mining methods that use evolutionary algorithms
 Author-email: Pavel Sherstnev <sherstpasha99@gmail.com>
 Project-URL: Homepage, https://github.com/sherstpasha/thefittest
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
+Requires-Python: <=3.10,>=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # thefittest
 
 # the package contains methods
 * **Genetic algorithm** (Holland, J. H. (1992). Genetic algorithms. Scientific American, 267(1), 66-72):
```

### Comparing `thefittest-0.1.8/src/thefittest.egg-info/SOURCES.txt` & `thefittest-0.1.9/src/thefittest.egg-info/SOURCES.txt`

 * *Files identical despite different names*

