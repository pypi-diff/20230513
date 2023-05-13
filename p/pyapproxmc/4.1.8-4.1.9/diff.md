# Comparing `tmp/pyapproxmc-4.1.8.tar.gz` & `tmp/pyapproxmc-4.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyapproxmc-4.1.8.tar", last modified: Tue Oct 25 22:58:07 2022, max compression
+gzip compressed data, was "pyapproxmc-4.1.9.tar", last modified: Fri Feb 24 22:08:47 2023, max compression
```

## Comparing `pyapproxmc-4.1.8.tar` & `pyapproxmc-4.1.9.tar`

### file list

```diff
@@ -1,202 +1,203 @@
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.421051 pyapproxmc-4.1.8/
--rw-r--r--   0 soos      (1000) soos      (1000)     1117 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/LICENSE
--rw-r--r--   0 soos      (1000) soos      (1000)     3800 2022-10-25 22:58:07.421051 pyapproxmc-4.1.8/PKG-INFO
--rw-r--r--   0 soos      (1000) soos      (1000)     6738 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/README.md
--rw-r--r--   0 soos      (1000) soos      (1000)      810 2022-10-25 22:56:59.000000 pyapproxmc-4.1.8/pyproject.toml
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/arjun/
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/arjun/python/
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/arjun/python/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1571 2022-09-16 23:52:50.000000 pyapproxmc-4.1.8/python/arjun/python/src/GitSHA1.cpp
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/arjun/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1330 2022-09-16 19:18:06.000000 pyapproxmc-4.1.8/python/arjun/src/GitSHA1.h
--rw-r--r--   0 soos      (1000) soos      (1000)    14105 2022-09-16 19:18:06.000000 pyapproxmc-4.1.8/python/arjun/src/MersenneTwister.h
--rw-r--r--   0 soos      (1000) soos      (1000)    17543 2022-10-03 19:20:10.000000 pyapproxmc-4.1.8/python/arjun/src/arjun.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5972 2022-10-03 19:20:10.000000 pyapproxmc-4.1.8/python/arjun/src/arjun.h
--rw-r--r--   0 soos      (1000) soos      (1000)    11835 2022-09-17 16:12:33.000000 pyapproxmc-4.1.8/python/arjun/src/backward.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    12634 2022-10-03 19:20:10.000000 pyapproxmc-4.1.8/python/arjun/src/common.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     9173 2022-10-03 19:20:10.000000 pyapproxmc-4.1.8/python/arjun/src/common.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1937 2022-09-17 16:12:33.000000 pyapproxmc-4.1.8/python/arjun/src/config.h
--rw-r--r--   0 soos      (1000) soos      (1000)    19822 2022-10-03 19:20:10.000000 pyapproxmc-4.1.8/python/arjun/src/simplify.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4347 2022-09-16 19:18:06.000000 pyapproxmc-4.1.8/python/arjun/src/time_mem.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/cryptominisat/
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.381051 pyapproxmc-4.1.8/python/cryptominisat/python/
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.384384 pyapproxmc-4.1.8/python/cryptominisat/python/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1564 2022-09-16 23:54:59.000000 pyapproxmc-4.1.8/python/cryptominisat/python/src/GitSHA1.cpp
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.414385 pyapproxmc-4.1.8/python/cryptominisat/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1305 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/GitSHA1.h
--rw-r--r--   0 soos      (1000) soos      (1000)    13907 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/MersenneTwister.h
--rw-r--r--   0 soos      (1000) soos      (1000)     7583 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/Vec.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1954 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/XAlloc.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1677 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/alg.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4657 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/avgcalc.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3303 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/bitarray.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4747 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/boundedqueue.h
--rw-r--r--   0 soos      (1000) soos      (1000)    27004 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/bva.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5685 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/bva.h
--rw-r--r--   0 soos      (1000) soos      (1000)    13075 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cardfinder.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2368 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cardfinder.h
--rw-r--r--   0 soos      (1000) soos      (1000)    16843 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ccnr.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5212 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ccnr.h
--rw-r--r--   0 soos      (1000) soos      (1000)    10974 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_cms.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2628 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_cms.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6250 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_mersenne.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3743 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_abs.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2555 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_lgbm.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3291 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_py.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2607 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_xgb.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1701 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clabstraction.h
--rw-r--r--   0 soos      (1000) soos      (1000)    18484 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clause.h
--rw-r--r--   0 soos      (1000) soos      (1000)    11747 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clauseallocator.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4318 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clauseallocator.h
--rw-r--r--   0 soos      (1000) soos      (1000)    17759 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clausecleaner.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2953 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/clausecleaner.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1503 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cloffset.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1594 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cms_bosphorus.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2756 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cms_breakid.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3264 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cms_windows_includes.h
--rw-r--r--   0 soos      (1000) soos      (1000)    27989 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cnf.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    21681 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cnf.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1461 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/community_finder.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6042 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/completedetachreattacher.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2810 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/completedetachreattacher.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5819 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/constants.h
--rw-r--r--   0 soos      (1000) soos      (1000)    54911 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    14058 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6087 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat_c.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3984 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat_c.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5807 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/cset.h
--rw-r--r--   0 soos      (1000) soos      (1000)    24643 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/datasync.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4601 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/datasync.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2728 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/datasyncserver.h
--rw-r--r--   0 soos      (1000) soos      (1000)    18638 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/dimacsparser.h
--rw-r--r--   0 soos      (1000) soos      (1000)     9682 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerbin.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2971 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerbin.h
--rw-r--r--   0 soos      (1000) soos      (1000)    11071 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlitrem.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3041 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlitrem.h
--rw-r--r--   0 soos      (1000) soos      (1000)    21204 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlong.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3294 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlong.h
--rw-r--r--   0 soos      (1000) soos      (1000)    14419 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlongwithimpl.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5423 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/distillerlongwithimpl.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1182 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/frat.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    11740 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/frat.h
--rw-r--r--   0 soos      (1000) soos      (1000)    11052 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gatefinder.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4373 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gatefinder.h
--rw-r--r--   0 soos      (1000) soos      (1000)    54015 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gaussian.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     7175 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gaussian.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2068 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gausswatched.h
--rw-r--r--   0 soos      (1000) soos      (1000)    13174 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/get_clause_query.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2941 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/get_clause_query.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2012 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/gqueuedata.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2003 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/hasher.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6087 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/heap.h
--rw-r--r--   0 soos      (1000) soos      (1000)    21346 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/hyperengine.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3168 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/hyperengine.h
--rw-r--r--   0 soos      (1000) soos      (1000)    13562 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/intree.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3414 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/intree.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6209 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/ipasir.h
--rw-r--r--   0 soos      (1000) soos      (1000)     9629 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/lucky.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     1678 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/lucky.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3970 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/main.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1846 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/main_common.h
--rw-r--r--   0 soos      (1000) soos      (1000)    14458 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/matrixfinder.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2783 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/matrixfinder.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.414385 pyapproxmc-4.1.8/python/cryptominisat/src/msvc/
--rw-r--r--   0 soos      (1000) soos      (1000)     7728 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/msvc/stdint.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1897 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/mystack.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1840 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/nomutex.h
--rw-r--r--   0 soos      (1000) soos      (1000)   179723 2022-10-25 22:48:00.000000 pyapproxmc-4.1.8/python/cryptominisat/src/occsimplifier.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    20550 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/occsimplifier.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.414385 pyapproxmc-4.1.8/python/cryptominisat/src/oracle/
--rw-r--r--   0 soos      (1000) soos      (1000)     8417 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/oracle/bitset.hpp
--rw-r--r--   0 soos      (1000) soos      (1000)    30036 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/oracle/oracle.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5084 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/oracle/oracle.hpp
--rw-r--r--   0 soos      (1000) soos      (1000)     6580 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/oracle/utils.hpp
--rw-r--r--   0 soos      (1000) soos      (1000)     5048 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/packedmatrix.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6518 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/packedrow.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     8056 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/packedrow.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.417718 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/
--rw-r--r--   0 soos      (1000) soos      (1000)      148 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/config.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5179 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picogcnf.c
--rw-r--r--   0 soos      (1000) soos      (1000)     8396 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picomcs.c
--rw-r--r--   0 soos      (1000) soos      (1000)    12595 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picomus.c
--rw-r--r--   0 soos      (1000) soos      (1000)   162828 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picosat.c
--rw-r--r--   0 soos      (1000) soos      (1000)    28690 2022-10-06 21:28:44.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picosat.h
--rw-r--r--   0 soos      (1000) soos      (1000)      168 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/picosat/version.c
--rw-r--r--   0 soos      (1000) soos      (1000)     1242 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/popcnt.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1434 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/predict_func_type.h
--rw-r--r--   0 soos      (1000) soos      (1000)     8108 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/propby.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6150 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/propby_backup.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4038 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/propbyforgraph.h
--rw-r--r--   0 soos      (1000) soos      (1000)    30467 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/propengine.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    20663 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/propengine.h
--rw-r--r--   0 soos      (1000) soos      (1000)    47426 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/reducedb.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4617 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/reducedb.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4002 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/satzilla_features.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2540 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/satzilla_features_calc.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6078 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sccfinder.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4799 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sccfinder.h
--rw-r--r--   0 soos      (1000) soos      (1000)   121983 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/searcher.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    21044 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/searcher.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5702 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/searchhist.h
--rw-r--r--   0 soos      (1000) soos      (1000)     9705 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/searchstats.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3305 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/searchstats.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3402 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/shareddata.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1380 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/signalcode.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3891 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/simplefile.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3144 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sls.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     1540 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sls.h
--rw-r--r--   0 soos      (1000) soos      (1000)     7129 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solutionextender.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2230 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solutionextender.h
--rw-r--r--   0 soos      (1000) soos      (1000)   158005 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solver.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    22676 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solver.h
--rw-r--r--   0 soos      (1000) soos      (1000)    16273 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solverconf.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    16307 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solverconf.h
--rw-r--r--   0 soos      (1000) soos      (1000)    11964 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solvertypes.h
--rw-r--r--   0 soos      (1000) soos      (1000)     8981 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/solvertypesmini.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1383 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sql_tablestructure.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6571 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sqlitestats.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4803 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/sqlstats.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5746 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/str_impl_w_impl.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2600 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/str_impl_w_impl.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6107 2022-10-03 19:20:06.000000 pyapproxmc-4.1.8/python/cryptominisat/src/streambuffer.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6782 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/subsumeimplicit.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2814 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/subsumeimplicit.h
--rw-r--r--   0 soos      (1000) soos      (1000)    33553 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/subsumestrengthen.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     4395 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/subsumestrengthen.h
--rw-r--r--   0 soos      (1000) soos      (1000)     6889 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/time_mem.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3144 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/toplevelgauss.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1699 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/toplevelgaussabst.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4290 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/touchlist.h
--rw-r--r--   0 soos      (1000) soos      (1000)     1505 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/trim.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4231 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/vardata.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2013 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/vardistgen.h
--rw-r--r--   0 soos      (1000) soos      (1000)    38391 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/varreplacer.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    10002 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/varreplacer.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4402 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/varupdatehelper.h
--rw-r--r--   0 soos      (1000) soos      (1000)     3386 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/vmtf.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5118 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/watchalgos.h
--rw-r--r--   0 soos      (1000) soos      (1000)     4713 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/watcharray.h
--rw-r--r--   0 soos      (1000) soos      (1000)    13142 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/watcharray_handrolled.h
--rw-r--r--   0 soos      (1000) soos      (1000)     9466 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/watched.h
--rw-r--r--   0 soos      (1000) soos      (1000)     5072 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/xor.h
--rw-r--r--   0 soos      (1000) soos      (1000)    28603 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/xorfinder.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    10429 2022-09-16 19:17:58.000000 pyapproxmc-4.1.8/python/cryptominisat/src/xorfinder.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.417718 pyapproxmc-4.1.8/python/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1590 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/python/src/GitSHA1.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)    15301 2022-10-25 22:45:52.000000 pyapproxmc-4.1.8/python/src/pyapproxmc.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)      177 2022-10-25 22:58:07.421051 pyapproxmc-4.1.8/setup.cfg
--rw-r--r--   0 soos      (1000) soos      (1000)     5600 2022-10-25 22:47:35.000000 pyapproxmc-4.1.8/setup.py
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.421051 pyapproxmc-4.1.8/src/
--rw-r--r--   0 soos      (1000) soos      (1000)     1328 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/GitSHA1.h
--rw-r--r--   0 soos      (1000) soos      (1000)     8364 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/approxmc.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     3952 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/approxmc.h
--rw-r--r--   0 soos      (1000) soos      (1000)     2085 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/config.h
--rw-r--r--   0 soos      (1000) soos      (1000)    10764 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/constants.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     2035 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/constants.h
--rw-r--r--   0 soos      (1000) soos      (1000)    28383 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/counter.cpp
--rw-r--r--   0 soos      (1000) soos      (1000)     6018 2022-09-28 10:54:06.000000 pyapproxmc-4.1.8/src/counter.h
-drwxr-xr-x   0 soos      (1000) soos      (1000)        0 2022-10-25 22:58:07.421051 pyapproxmc-4.1.8/src/pyapproxmc.egg-info/
--rw-r--r--   0 soos      (1000) soos      (1000)     3800 2022-10-25 22:58:07.000000 pyapproxmc-4.1.8/src/pyapproxmc.egg-info/PKG-INFO
--rw-r--r--   0 soos      (1000) soos      (1000)     6759 2022-10-25 22:58:07.000000 pyapproxmc-4.1.8/src/pyapproxmc.egg-info/SOURCES.txt
--rw-r--r--   0 soos      (1000) soos      (1000)     4347 2019-03-02 11:51:51.000000 pyapproxmc-4.1.8/src/time_mem.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.790324 pyapproxmc-4.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1117 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3742 2023-02-24 22:08:47.790324 pyapproxmc-4.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     7804 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      810 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.754325 pyapproxmc-4.1.9/python/
+-rw-r--r--   0 runner    (1001) docker     (123)     1687 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/python/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.750325 pyapproxmc-4.1.9/python/arjun/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.750325 pyapproxmc-4.1.9/python/arjun/python/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.754325 pyapproxmc-4.1.9/python/arjun/python/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/python/src/GitSHA1.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.754325 pyapproxmc-4.1.9/python/arjun/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1330 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/GitSHA1.h
+-rw-r--r--   0 runner    (1001) docker     (123)    14105 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/MersenneTwister.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13500 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/arjun.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5950 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/arjun.h
+-rw-r--r--   0 runner    (1001) docker     (123)    12836 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/backward.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    12649 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/common.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     9142 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/common.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1960 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/config.h
+-rw-r--r--   0 runner    (1001) docker     (123)    20007 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/simplify.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-02-24 22:08:37.000000 pyapproxmc-4.1.9/python/arjun/src/time_mem.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.750325 pyapproxmc-4.1.9/python/cryptominisat/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.750325 pyapproxmc-4.1.9/python/cryptominisat/python/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.754325 pyapproxmc-4.1.9/python/cryptominisat/python/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/python/src/GitSHA1.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.786324 pyapproxmc-4.1.9/python/cryptominisat/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/GitSHA1.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13907 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/MersenneTwister.h
+-rw-r--r--   0 runner    (1001) docker     (123)     7583 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/Vec.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1954 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/XAlloc.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/alg.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4657 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/avgcalc.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3303 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/bitarray.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4766 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/boundedqueue.h
+-rw-r--r--   0 runner    (1001) docker     (123)    27004 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/bva.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5704 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/bva.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13075 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cardfinder.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2387 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cardfinder.h
+-rw-r--r--   0 runner    (1001) docker     (123)    16843 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ccnr.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5231 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ccnr.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10974 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_cms.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2628 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_cms.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6250 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_mersenne.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3762 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_abs.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2555 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_lgbm.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3291 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_py.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2607 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_xgb.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1721 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clabstraction.h
+-rw-r--r--   0 runner    (1001) docker     (123)    18503 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clause.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11747 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clauseallocator.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4318 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clauseallocator.h
+-rw-r--r--   0 runner    (1001) docker     (123)    17759 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clausecleaner.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2953 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/clausecleaner.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1503 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cloffset.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1594 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cms_bosphorus.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2756 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cms_breakid.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3264 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cms_windows_includes.h
+-rw-r--r--   0 runner    (1001) docker     (123)    27989 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cnf.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    21681 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cnf.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/community_finder.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6042 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/completedetachreattacher.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2810 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/completedetachreattacher.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5819 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/constants.h
+-rw-r--r--   0 runner    (1001) docker     (123)    54856 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    14038 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6087 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat_c.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3984 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat_c.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5807 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/cset.h
+-rw-r--r--   0 runner    (1001) docker     (123)    24643 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/datasync.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4601 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/datasync.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2728 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/datasyncserver.h
+-rw-r--r--   0 runner    (1001) docker     (123)    18638 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/dimacsparser.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9682 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerbin.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2971 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerbin.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11071 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlitrem.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3041 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlitrem.h
+-rw-r--r--   0 runner    (1001) docker     (123)    21204 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlong.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3294 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlong.h
+-rw-r--r--   0 runner    (1001) docker     (123)    14419 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlongwithimpl.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5423 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/distillerlongwithimpl.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1182 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/frat.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    11740 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/frat.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11052 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gatefinder.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4373 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gatefinder.h
+-rw-r--r--   0 runner    (1001) docker     (123)    54015 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gaussian.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     7175 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gaussian.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2068 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gausswatched.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13229 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/get_clause_query.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2941 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/get_clause_query.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2012 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/gqueuedata.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2003 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/hasher.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6087 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/heap.h
+-rw-r--r--   0 runner    (1001) docker     (123)    21346 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/hyperengine.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3168 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/hyperengine.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13562 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/intree.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3414 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/intree.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6209 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/ipasir.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9629 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/lucky.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     1678 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/lucky.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3970 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/main.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1846 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/main_common.h
+-rw-r--r--   0 runner    (1001) docker     (123)    14458 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/matrixfinder.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/matrixfinder.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.786324 pyapproxmc-4.1.9/python/cryptominisat/src/msvc/
+-rw-r--r--   0 runner    (1001) docker     (123)     7728 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/msvc/stdint.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/mystack.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1840 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/nomutex.h
+-rw-r--r--   0 runner    (1001) docker     (123)   176299 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/occsimplifier.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    20504 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/occsimplifier.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.786324 pyapproxmc-4.1.9/python/cryptominisat/src/oracle/
+-rw-r--r--   0 runner    (1001) docker     (123)     8454 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/oracle/bitset.hpp
+-rw-r--r--   0 runner    (1001) docker     (123)    30036 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/oracle/oracle.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5084 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/oracle/oracle.hpp
+-rw-r--r--   0 runner    (1001) docker     (123)     6580 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/oracle/utils.hpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5048 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/packedmatrix.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6518 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/packedrow.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     8056 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/packedrow.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.786324 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/
+-rw-r--r--   0 runner    (1001) docker     (123)      148 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/config.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5179 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picogcnf.c
+-rw-r--r--   0 runner    (1001) docker     (123)     8396 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picomcs.c
+-rw-r--r--   0 runner    (1001) docker     (123)    12595 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picomus.c
+-rw-r--r--   0 runner    (1001) docker     (123)   162828 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picosat.c
+-rw-r--r--   0 runner    (1001) docker     (123)    28679 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picosat.h
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/picosat/version.c
+-rw-r--r--   0 runner    (1001) docker     (123)     1242 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/popcnt.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1434 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/predict_func_type.h
+-rw-r--r--   0 runner    (1001) docker     (123)     8108 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/propby.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6150 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/propby_backup.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4038 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/propbyforgraph.h
+-rw-r--r--   0 runner    (1001) docker     (123)    30467 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/propengine.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    20663 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/propengine.h
+-rw-r--r--   0 runner    (1001) docker     (123)    47426 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/reducedb.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/reducedb.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4002 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/satzilla_features.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2540 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/satzilla_features_calc.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6078 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sccfinder.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4799 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sccfinder.h
+-rw-r--r--   0 runner    (1001) docker     (123)   121983 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/searcher.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    21044 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/searcher.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5702 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/searchhist.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9705 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/searchstats.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3305 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/searchstats.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3402 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/shareddata.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1380 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/signalcode.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3891 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/simplefile.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3144 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sls.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     1540 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sls.h
+-rw-r--r--   0 runner    (1001) docker     (123)     7129 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solutionextender.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2230 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solutionextender.h
+-rw-r--r--   0 runner    (1001) docker     (123)   158016 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solver.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    22651 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solver.h
+-rw-r--r--   0 runner    (1001) docker     (123)    16273 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solverconf.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    16307 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solverconf.h
+-rw-r--r--   0 runner    (1001) docker     (123)    11964 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solvertypes.h
+-rw-r--r--   0 runner    (1001) docker     (123)     8981 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/solvertypesmini.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sql_tablestructure.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6571 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sqlitestats.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/sqlstats.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5746 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/str_impl_w_impl.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2600 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/str_impl_w_impl.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6107 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/streambuffer.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6782 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/subsumeimplicit.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2814 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/subsumeimplicit.h
+-rw-r--r--   0 runner    (1001) docker     (123)    33553 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/subsumestrengthen.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     4395 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/subsumestrengthen.h
+-rw-r--r--   0 runner    (1001) docker     (123)     6889 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/time_mem.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3144 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/toplevelgauss.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/toplevelgaussabst.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4290 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/touchlist.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1505 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/trim.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4231 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/vardata.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2013 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/vardistgen.h
+-rw-r--r--   0 runner    (1001) docker     (123)    38391 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/varreplacer.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    10002 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/varreplacer.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4402 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/varupdatehelper.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3405 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/vmtf.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5118 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/watchalgos.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4732 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/watcharray.h
+-rw-r--r--   0 runner    (1001) docker     (123)    13161 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/watcharray_handrolled.h
+-rw-r--r--   0 runner    (1001) docker     (123)     9485 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/watched.h
+-rw-r--r--   0 runner    (1001) docker     (123)     5091 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/xor.h
+-rw-r--r--   0 runner    (1001) docker     (123)    28603 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/xorfinder.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    10448 2023-02-24 22:08:36.000000 pyapproxmc-4.1.9/python/cryptominisat/src/xorfinder.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.786324 pyapproxmc-4.1.9/python/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1590 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/python/src/GitSHA1.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    15255 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/python/src/pyapproxmc.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)      177 2023-02-24 22:08:47.790324 pyapproxmc-4.1.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     5600 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.790324 pyapproxmc-4.1.9/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1328 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/GitSHA1.h
+-rw-r--r--   0 runner    (1001) docker     (123)     8119 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/approxmc.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     3850 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/approxmc.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2050 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/config.h
+-rw-r--r--   0 runner    (1001) docker     (123)    10764 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/constants.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     2035 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/constants.h
+-rw-r--r--   0 runner    (1001) docker     (123)    25879 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/counter.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     5929 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/counter.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-24 22:08:47.790324 pyapproxmc-4.1.9/src/pyapproxmc.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3742 2023-02-24 22:08:47.000000 pyapproxmc-4.1.9/src/pyapproxmc.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6776 2023-02-24 22:08:47.000000 pyapproxmc-4.1.9/src/pyapproxmc.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-02-24 22:08:26.000000 pyapproxmc-4.1.9/src/time_mem.h
```

### Comparing `pyapproxmc-4.1.8/LICENSE` & `pyapproxmc-4.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/PKG-INFO` & `pyapproxmc-4.1.9/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyapproxmc
-Version: 4.1.8
+Version: 4.1.9
 Summary: Bindings to ApproxMC, an approximate model counter
 Home-page: https://github.com/meelgroup/approxmc
 Author-email: Mate Soos <soos.mate@gmail.com>
 Maintainer-email: Mate Soos <soos.mate@gmail.com>
 License: MIT License
         
         Copyright (c) 2018 Meel Group
@@ -42,58 +42,58 @@
 Classifier: Topic :: Utilities
 Requires-Python: >=3.5
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # pyapproxmc: bindings to the ApproxMC model counter
 
-This directory provides Python bindings to CryptoMiniSat on the C++ level,
-i.e. when importing pycryptosat, the CryptoMiniSat solver becomes part of the
+This directory provides Python bindings to ApproxMC on the C++ level,
+i.e. when importing pyapproxmc, the ApproxMC counter becomes part of the
 Python process itself.
 
-## Compiling
-The pyapproxmc python package compiles separately from ApproxMC, the binary.
 
-In order to compile, install the python developer tools:
+## Installing
 
 ```
-apt-get install python-dev
+pip install pyapproxmc
 ```
 
-Then:
+## Compiling
+If you don't want to use the pip package, you can compile it:
 
 ```
+apt-get install python-dev
 cd python
 git clone https://github.com/msoos/cryptominisat
 git clone https://github.com/meelgroup/arjun
 cd ..
 python -m build
 
 You will then find the files under "dist/".
 ```
 
 ## Usage
 
-The ``pyapproxmc`` module has one object, ``Counter`` that has two functions
-``count`` and ``add_clause``.
+The `pyapproxmc` module has one object, `Counter` that has two functions
+`count` and `add_clause`.
 
-The funcion ``add_clause()`` takes an iterable list of literals such as
+The function ``add_clause()`` takes an iterable list of literals such as
 ``[1, 2]`` which represents the truth ``1 or 2 = True``. For example,
 ``add_clause([1])`` sets variable ``1`` to ``True``.
 
-The function ``count()`` solves the system of equations that have been added
-with ``add_clause()``:
+The function `count()` counts the number of solutions to the system of constraints
+that have been added with `add_clause()`:
 
 ```
-   >>> from pyapproxmc import Counter
-   >>> s = Counter()
-   >>> s.add_clause([1, 2])
-   >>> cells, hashes = s.count()
-   >>> print "There are ", cells*2**hashes, " solutions, approximately"
-   There are 55 solutions, approximately
+>>> from pyapproxmc import Counter
+>>> s = Counter()
+>>> s.add_clause([1, 2])
+>>> cells, hashes = s.count()
+>>> print("There are approx ", cells*2**hashes, " solutions")
+There are 55 solutions, approximately
 ```
 
 The return value is a tuple of cells and hashes. Which gives how many solutions
 there are, probabilistically approximately
 
 You can give the following arguments to `Counter`:
 * `seed` -- sets the random seed
```

### Comparing `pyapproxmc-4.1.8/README.md` & `pyapproxmc-4.1.9/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -9,15 +9,49 @@
 This work is by Mate Soos, Stephan Gocht, and Kuldeep S. Meel, as [published in AAAI-19](https://www.comp.nus.edu.sg/~meel/Papers/aaai19-sm.pdf) and [in CAV2020](https://www.comp.nus.edu.sg/~meel/Papers/cav20-sgm.pdf). A large part of the work is in CryptoMiniSat [here](https://github.com/msoos/cryptominisat).
 
 ApproxMC handles CNF formulas and performs approximate counting. 
 
 1. If you are interested in exact model counting, visit our exact counter [Ganak](http://github.com/meelgroup/ganak)
 2. If you are instead interested in DNF formulas, visit our DNF counter [DNFApproxMC](https://gitlab.com/Shrotri/DNF_Counting).
 
-## How to Build
+## How to use the Python interface
+
+Install using pip:
+
+```
+pip install pyapproxmc
+```
+
+Then you can use it as:
+
+```
+import pyapproxmc
+c = pyapproxmc.Counter()
+c.add_clause([1,2,3])
+c.add_clause([3,20])
+count = c.count()
+print("Approximate count is: %d*2**%d" % (count[0], count[1]))
+```
+
+The above will print that `Approximate count is: 88*2**13`. Since the largest variable in the clauses was 20, the system contained 2**20 (i.e. 1048576) potential models. However, some of these models were prohibited by the two clauses, and so only approximately 88*2**13 (i.e. 720896) models remained.
+
+If you want to count over a projection set, you need to call `count(projection_set)`, for example:
+
+```
+import pyapproxmc
+c = pyapproxmc.Counter()
+c.add_clause([1,2,3])
+c.add_clause([3,20])
+count = c.count(range(1,10))
+print("Approximate count is: %d*2**%d" % (count[0], count[1]))
+```
+
+This now prints `Approximate count is: 56*2**3`, which corresponds to the approximate count of models, projected over variables 1..10.
+
+## How to Build a Binary
 To build on Linux, you will need the following:
 ```
 sudo apt-get install build-essential cmake
 sudo apt-get install zlib1g-dev libboost-program-options-dev
 apt-get install libgmp3-dev
 ```
 
@@ -43,18 +77,18 @@
 cd approxmc
 mkdir build && cd build
 cmake ..
 make
 sudo make install
 ```
 
-## How to Use
+## How to Use the Binary
 First, you must translate your problem to CNF and just pass your file as input to ApproxMC. Voila -- and it will print the number of solutions of the given CNF formula.
 
-### Sampling Set
+### Providing a Sampling Set
 For some applications, one is not interested in solutions over all the variables and instead interested in counting the number of unique solutions to a subset of variables, called sampling set. ApproxMC allows you to specify the sampling set using the following modified version of DIMACS format:
 
 ```
 $ cat myfile.cnf
 c ind 1 3 4 6 7 8 10 0
 p cnf 500 1
 3 4 0
@@ -82,15 +116,15 @@
 [appmc] FINISHED ApproxMC T: 0.04 s
 c [appmc] Number of solutions is: 48*2**1
 s mc 96
 ```
 ApproxMC reports that we have approximately `96 (=48*2)` solutions to the CNF's independent support. This is because for variables 3 and 4 we have banned the `false,false` solution, so out of their 4 possible settings, one is banned. Therefore, we have `2^5 * (4-1) = 96` solutions.
 
 ### Guarantees
-ApproxMC provides so-called "PAC", or Probably Approximately Correct, guarantees. In less fancy words, the system guarntees that the solution found is within a certain tolerance (called "epsilon") with a certain probability (called "delta"). The default tolerance and probability, i.e. epsilon and delta values, are set to 0.8 and 0.2, respectively. Both values are configurable.
+ApproxMC provides so-called "PAC", or Probably Approximately Correct, guarantees. In less fancy words, the system guarantees that the solution found is within a certain tolerance (called "epsilon") with a certain probability (called "delta"). The default tolerance and probability, i.e. epsilon and delta values, are set to 0.8 and 0.2, respectively. Both values are configurable.
 
 ### Library usage
 
 The system can be used as a library:
 
 ```
 #include <approxmc/approxmc.h>
@@ -132,15 +166,15 @@
 Note: this is beta version release, not recommended for general use. We are currently working on a tight integration of sparse XORs into ApproxMC based on our [LICS-20](http://comp.nus.edu.sg/~meel/Papers/lics20-ma.pdf) paper. You can turn on the sparse XORs using the flag "sparse" but beware as reported in LICS-20 paper, this may slow down in some cases; it is likely to give a significant speedup if the number of solutions is very large. 
 
 
 ### Issues, questions, bugs, etc.
 Please click on "issues" at the top and [create a new issue](https://github.com/meelgroup/mis/issues/new). All issues are responded to promptly.
 
 ## How to Cite
-If you use ApproxMC, please cite the following papers: [CAV20](https://www.comp.nus.edu.sg/~meel/bib/SM19.bib), [AAAI19](https://www.comp.nus.edu.sg/~meel/bib/SM19.bib) and [IJCAI16](https://www.comp.nus.edu.sg/~meel/bib/CMV16.bib).
+If you use ApproxMC, please cite the following papers: [CAV20](https://dblp.uni-trier.de/rec/conf/cav/SoosGM20.html?view=bibtex), [AAAI19](https://www.comp.nus.edu.sg/~meel/bib/SM19.bib) and [IJCAI16](https://www.comp.nus.edu.sg/~meel/bib/CMV16.bib).
 
 If you use sparse XORs, please also cite the [LICS20](https://www.comp.nus.edu.sg/~meel/bib/MA20.bib) paper. 
 
 ApproxMC builds on a series of papers on hashing-based approach: [Related Publications](https://www.comp.nus.edu.sg/~meel/publications.html)
 
 The benchmarks used in our evaluation can be found [here](https://www.comp.nus.edu.sg/~meel/Benchmarks/).
```

### Comparing `pyapproxmc-4.1.8/pyproject.toml` & `pyapproxmc-4.1.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=42", "wheel", "toml", "pathlib"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "pyapproxmc"
-version = "4.1.8"
+version = "4.1.9"
 description = "Bindings to ApproxMC, an approximate model counter"
 keywords = ["sat", "model-counting"]
 license = { file = "LICENSE" }
 maintainers = [{name="Mate Soos", email="soos.mate@gmail.com"}]
 authors = [{name="Mate Soos", email="soos.mate@gmail.com"}]
 classifiers = [
     "Development Status :: 4 - Beta",
```

### Comparing `pyapproxmc-4.1.8/python/arjun/python/src/GitSHA1.cpp` & `pyapproxmc-4.1.9/python/arjun/python/src/GitSHA1.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/arjun/src/GitSHA1.h` & `pyapproxmc-4.1.9/python/arjun/src/GitSHA1.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/arjun/src/MersenneTwister.h` & `pyapproxmc-4.1.9/python/arjun/src/MersenneTwister.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/arjun/src/arjun.cpp` & `pyapproxmc-4.1.9/python/arjun/src/arjun.cpp`

 * *Files 27% similar despite different names*

```diff
@@ -37,14 +37,26 @@
 #if defined _WIN32
     #define DLL_PUBLIC __declspec(dllexport)
 #else
     #define DLL_PUBLIC __attribute__ ((visibility ("default")))
     #define DLL_LOCAL  __attribute__ ((visibility ("hidden")))
 #endif
 
+#define set_get_macro(TYPE, NAME) \
+DLL_PUBLIC void Arjun::set_##NAME (TYPE NAME) \
+{ \
+    arjdata->common.conf.NAME = NAME; \
+} \
+DLL_PUBLIC TYPE Arjun::get_##NAME () const \
+{ \
+    return arjdata->common.conf.NAME; \
+} \
+
+
+
 namespace ArjunNS {
     struct ArjPrivateData {
         Common common;
     };
 }
 
 using namespace ArjunNS;
@@ -124,17 +136,23 @@
 }
 
 DLL_PUBLIC std::string Arjun::get_compilation_env()
 {
     return arjdata->common.solver->get_compilation_env();
 }
 
+DLL_PUBLIC const std::vector<Lit>& Arjun::get_orig_cnf()
+{
+    return arjdata->common.orig_cnf;
+}
+
 DLL_PUBLIC vector<uint32_t> Arjun::get_indep_set()
 {
     double starTime = cpuTime();
+    arjdata->common.orig_cnf = arjdata->common.get_cnf();
     if (!arjdata->common.preproc_and_duplicate()) goto end;
 
     //Backward
     if (arjdata->common.conf.backward) {
         arjdata->common.backward_round();
     }
 
@@ -192,215 +210,38 @@
 }
 
 DLL_PUBLIC void Arjun::set_seed(uint32_t seed)
 {
     arjdata->common.random_source.seed(seed);
 }
 
-
-DLL_PUBLIC void Arjun::set_fast_backw(bool fast_backw)
-{
-    arjdata->common.conf.fast_backw = fast_backw;
-}
-
-DLL_PUBLIC void Arjun::set_distill(bool distill)
-{
-    arjdata->common.conf.distill = distill;
-}
-
-DLL_PUBLIC void Arjun::set_intree(bool intree)
-{
-    arjdata->common.conf.intree = intree;
-}
-
-DLL_PUBLIC void Arjun::set_guess(bool guess)
-{
-    arjdata->common.conf.guess = guess;
-}
-
-DLL_PUBLIC void Arjun::set_pre_simplify(bool simp)
-{
-    arjdata->common.conf.pre_simplify = simp;
-}
-
-DLL_PUBLIC void Arjun::set_simp(bool simp)
-{
-    arjdata->common.conf.simp = simp;
-}
-
-DLL_PUBLIC void Arjun::set_incidence_sort(uint32_t incidence_sort)
-{
-    arjdata->common.conf.incidence_sort = incidence_sort;
-}
-
-DLL_PUBLIC void Arjun::set_or_gate_based(bool or_gate_based)
-{
-    arjdata->common.conf.or_gate_based = or_gate_based;
-}
-
-DLL_PUBLIC void Arjun::set_xor_gates_based(bool xor_gates_based)
-{
-    arjdata->common.conf.xor_gates_based = xor_gates_based;
-}
-
-DLL_PUBLIC void Arjun::set_probe_based(bool probe_based)
-{
-    arjdata->common.conf.probe_based = probe_based;
-}
-
-DLL_PUBLIC void Arjun::set_forward(bool forward)
-{
-    arjdata->common.conf.forward = forward;
-}
-
-DLL_PUBLIC void Arjun::set_backward(bool backward)
-{
-    //assert(backward && "We MUST have backward or we cannot work");
-    arjdata->common.conf.backward = backward;
-}
-
-DLL_PUBLIC void Arjun::set_assign_fwd_val(bool assign_fwd_val)
-{
-    arjdata->common.conf.assign_fwd_val = assign_fwd_val;
-}
-
-DLL_PUBLIC void Arjun::set_backw_max_confl(uint32_t backw_max_confl)
-{
-    arjdata->common.conf.backw_max_confl = backw_max_confl;
-}
-
-DLL_PUBLIC void Arjun::set_backbone_simpl_max_confl(uint64_t backbone_simpl_max_confl)
-{
-    arjdata->common.conf.backbone_simpl_max_confl = backbone_simpl_max_confl;
-}
-
-DLL_PUBLIC long unsigned Arjun::get_backbone_simpl_max_confl() const
-{
-    return arjdata->common.conf.backbone_simpl_max_confl;
-}
-
 DLL_PUBLIC uint32_t Arjun::get_verbosity() const
 {
     return arjdata->common.conf.verb;
 }
 
-DLL_PUBLIC bool Arjun::get_fast_backw() const
-{
-    return arjdata->common.conf.fast_backw;
-}
-
-DLL_PUBLIC bool Arjun::get_distill() const
-{
-    return arjdata->common.conf.distill;
-}
-
-DLL_PUBLIC bool Arjun::get_intree() const
-{
-    return arjdata->common.conf.intree;
-}
-
-DLL_PUBLIC bool Arjun::get_guess() const
-{
-    return arjdata->common.conf.guess;
-}
-
-DLL_PUBLIC bool Arjun::get_pre_simplify() const
-{
-    return arjdata->common.conf.pre_simplify;
-}
-
-DLL_PUBLIC uint32_t Arjun::get_incidence_sort() const
-{
-    return arjdata->common.conf.incidence_sort;
-}
-
-DLL_PUBLIC bool Arjun::get_or_gate_based() const
-{
-    return arjdata->common.conf.or_gate_based;
-}
-
-DLL_PUBLIC bool Arjun::get_xor_gates_based() const
-{
-    return arjdata->common.conf.xor_gates_based;
-}
-
-DLL_PUBLIC bool Arjun::get_probe_based() const
-{
-    return arjdata->common.conf.probe_based;
-}
-
-DLL_PUBLIC bool Arjun::get_forward() const
-{
-    return arjdata->common.conf.forward;
-}
-
-DLL_PUBLIC bool Arjun::get_backward() const
-{
-    return arjdata->common.conf.backward;
-}
-
-DLL_PUBLIC bool Arjun::get_assign_fwd_val() const
-{
-    return arjdata->common.conf.assign_fwd_val;
-}
-
-DLL_PUBLIC uint32_t Arjun::get_backw_max_confl() const
-{
-    return arjdata->common.conf.backw_max_confl;
-}
-
-DLL_PUBLIC void Arjun::set_gauss_jordan(bool gauss_jordan)
-{
-    arjdata->common.conf.gauss_jordan = gauss_jordan;
-}
-
-DLL_PUBLIC bool Arjun::get_gauss_jordan() const
-{
-    return arjdata->common.conf.gauss_jordan;
-}
-
-DLL_PUBLIC void Arjun::set_regularly_simplify(bool reg_simp)
-{
-    arjdata->common.conf.regularly_simplify = reg_simp;
-}
-
-DLL_PUBLIC bool Arjun::get_regularly_simplify() const
-{
-    return arjdata->common.conf.regularly_simplify;
-}
-
-DLL_PUBLIC void Arjun::set_fwd_group(uint32_t forward_group)
-{
-    arjdata->common.conf.forward_group = forward_group;
-}
-
-DLL_PUBLIC uint32_t Arjun::get_fwd_group() const
-{
-    return arjdata->common.conf.forward_group;
-}
-
-DLL_PUBLIC void Arjun::set_ite_gate_based(bool ite_gate_based)
-{
-    arjdata->common.conf.ite_gate_based = ite_gate_based;
-}
-
-DLL_PUBLIC bool Arjun::get_ite_gate_based() const
-{
-    return arjdata->common.conf.ite_gate_based;
-}
-
-DLL_PUBLIC void Arjun::set_irreg_gate_based(const bool irreg_gate_based)
-{
-    arjdata->common.conf.irreg_gate_based = irreg_gate_based;
-}
-
-DLL_PUBLIC bool Arjun::get_irreg_gate_based() const
-{
-    return arjdata->common.conf.irreg_gate_based;
-}
+set_get_macro(bool, fast_backw)
+set_get_macro(bool, distill)
+set_get_macro(bool, intree)
+set_get_macro(bool, bve_pre_simplify)
+set_get_macro(bool, simp)
+set_get_macro(uint32_t, unknown_sort)
+set_get_macro(uint32_t, incidence_count)
+set_get_macro(bool, or_gate_based)
+set_get_macro(bool, xor_gates_based)
+set_get_macro(bool, probe_based)
+set_get_macro(bool, backward)
+set_get_macro(uint32_t, backw_max_confl)
+set_get_macro(uint64_t, backbone_simpl_max_confl)
+set_get_macro(bool, gauss_jordan)
+set_get_macro(bool, ite_gate_based)
+set_get_macro(bool, irreg_gate_based)
+set_get_macro(double, no_gates_below)
+set_get_macro(std::string, specified_order_fname)
+set_get_macro(bool, backbone_simpl)
 
 DLL_PUBLIC vector<Lit> Arjun::get_zero_assigned_lits() const
 {
     vector<Lit> ret;
     vector<Lit> lits = arjdata->common.solver->get_zero_assigned_lits();
     for(const auto& lit: lits) {
         if (lit.var() < arjdata->common.orig_num_vars) {
@@ -422,24 +263,14 @@
             ret.push_back(bx);
         }
     }
 
     return ret;
 }
 
-DLL_PUBLIC void Arjun::set_backbone_simpl(bool backbone_simpl)
-{
-    arjdata->common.conf.backbone_simpl = backbone_simpl;
-}
-
-DLL_PUBLIC bool Arjun::get_backbone_simpl() const
-{
-    return arjdata->common.conf.backbone_simpl;
-}
-
 DLL_PUBLIC void Arjun::varreplace()
 {
     //arjdata->common.solver->backbone_simpl();
     std::string tmp("must-scc-vrepl, cl-consolidate");
     arjdata->common.solver->simplify(NULL, &tmp);
 }
 
@@ -477,164 +308,150 @@
             num_cls++;
         }
     }
     arjdata->common.solver->end_getting_small_clauses();
     return cnf;
 }
 
-static std::pair<vector<vector<Lit>>, uint32_t> get_simplified_renumbered_cnf(SATSolver* solver, vector<uint32_t>& sampl_vars)
+static void get_simplified_cnf(
+        SATSolver* solver, vector<uint32_t>& sampl_vars, const bool renumber,
+        vector<vector<Lit>>& cnf, uint32_t& nvars)
 {
-    vector<vector<Lit>> cnf;
+    assert(cnf.empty());
     solver->start_getting_small_clauses(
         std::numeric_limits<uint32_t>::max(),
         std::numeric_limits<uint32_t>::max(),
         false, //red
         false, //bva vars
-        true); //simplified
-
-    sampl_vars = solver->translate_sampl_set(sampl_vars);
+        renumber); //simplified
+    if (renumber) sampl_vars = solver->translate_sampl_set(sampl_vars);
 
     bool ret = true;
     vector<Lit> clause;
     while(ret) {
         ret = solver->get_next_small_clause(clause);
         if (ret) {
             cnf.push_back(clause);
         }
     }
     solver->end_getting_small_clauses();
-    return std::make_pair(cnf, solver->simplified_nvars());
+    nvars = renumber ? solver->simplified_nvars() :  solver->nVars();
 }
 
-static vector<Lit> fill_solver_no_empty(
-    const vector<uint32_t>& sampl_vars,
-    const vector<uint32_t>& empty_vars,
+static void fill_solver(
     const uint32_t orig_num_vars,
     SATSolver& solver, // Solver here is EMPTY
     Arjun* arjun)
 {
-    // We create a new Solver that has all variables (except empty)
-    solver.new_vars(orig_num_vars-empty_vars.size());
-    vector<char> seen(orig_num_vars, 0);
-    vector<uint32_t> mymap;
-    for(auto const& e: empty_vars) {
-        assert(e < orig_num_vars);
-        seen[e] = 1;
-    }
-
-    uint32_t at = 0;
-    for(uint32_t i = 0; i < orig_num_vars; i++) {
-        if (!seen[i]) {
-            mymap.push_back(at);
-            at++;
-        } else {
-            mymap.push_back(numeric_limits<uint32_t>::max());
-        }
-    }
-    assert(at == solver.nVars());
+    solver.new_vars(orig_num_vars);
 
-    //NOTE: we can have binary XORs that refer to EMPTY. This is because
-    //      var x (in sampling set) was replaced by var y, which became empty.
-    vector<Lit> tmp;
-    uint32_t sz = 0;
-    bool ok = true;
+    /* This below would work... except it doesn't work because
+     * it's been transformed, and some of that transformation is
+     * detrimental to simplifying the CNF
     uint32_t num_cls;
     const auto cnf = arjun->get_internal_cnf(num_cls);
+     */
+
+    // Inject original CNF
+    const auto cnf = arjun->get_orig_cnf();
+    vector<Lit> cl;
     for(const auto& l: cnf) {
         if (l != lit_Undef) {
-            if (seen[l.var()] == 1) ok = false;
-            if (ok) tmp.push_back(Lit(mymap[l.var()], l.sign()));
-            sz++;
+            assert(l.var() < orig_num_vars);
+            cl.push_back(l);
             continue;
         }
-        if (ok) solver.add_clause(tmp);
-        else assert(sz == 2);
-        tmp.clear();
-        ok = true;
-        sz = 0;
+        solver.add_clause(cl);
+        cl.clear();
     }
 
-    arjun->varreplace();
+    // inject set vars
+    const auto lits =  arjun->get_zero_assigned_lits();
+    for(const auto& l: lits) {
+        if (l.var() < orig_num_vars) {
+            cl.clear();
+            cl.push_back(l);
+            solver.add_clause(cl);
+        }
+    }
 
+    // inject bin-xor clauses
     auto bin_xors = arjun->get_all_binary_xors();
     vector<uint32_t> dummy_v;
     for(const auto& bx: bin_xors) {
         dummy_v.clear();
-        if (seen[bx.first.var()] == 0 && seen[bx.second.var()] == 0) { // see note above
-            dummy_v.push_back(mymap[bx.first.var()]);
-            dummy_v.push_back(mymap[bx.second.var()]);
-            solver.add_xor_clause(dummy_v, bx.first.sign()^bx.second.sign());
-        }
-    }
-
-    vector<Lit> dont_elim;
-    set<Lit> dont_elim_set;
-    for(const auto& v: sampl_vars) {
-        if (seen[v]) continue;
-        dont_elim_set.insert(Lit(mymap[v], false));
+        dummy_v.push_back(bx.first.var());
+        dummy_v.push_back(bx.second.var());
+        solver.add_xor_clause(dummy_v, bx.first.sign()^bx.second.sign());
     }
-    for(const auto& l: dont_elim_set) dont_elim.push_back(l);
-
-    return dont_elim;
 }
 
-DLL_PUBLIC std::tuple<pair<vector<vector<Lit>>, uint32_t>, vector<uint32_t>, uint32_t>
-Arjun::get_fully_simplified_renumbered_cnf(
+DLL_PUBLIC SimplifiedCNF Arjun::get_fully_simplified_renumbered_cnf(
     const vector<uint32_t>& sampl_vars, //contains empty_vars!
-    const vector<uint32_t>& empty_vars,
     const uint32_t orig_num_vars,
     const bool sparsify,
     const bool renumber)
 {
     CMSat::SATSolver solver;
     solver.set_verbosity(arjdata->common.conf.verb);
     solver.set_renumber(renumber);
     solver.set_scc(renumber);
-    auto dont_elim = fill_solver_no_empty(
-        sampl_vars, empty_vars, orig_num_vars, solver, this);
+
+    // Create a new SAT solver that contains no empties.
+    // dont_elim now how no empties in it
+    fill_solver(orig_num_vars, solver, this);
+    vector<Lit> dont_elim;
+    for(uint32_t v: sampl_vars) dont_elim.push_back(Lit(v, false));
 
     //Below works VERY WELL for: ProcessBean, pollard, track1_116.mcc2020_cnf
     //   and blasted_TR_b14_even3_linear.cnf.gz.no_w.cnf
     //with CMS ef6ea7e87e00bde50c0cce0c1e13a012191c4e1c and Arjun 5f2dfe814e07ee6ee0dde65b1350b5c343209ed0
     solver.set_min_bva_gain(0);
     solver.set_varelim_check_resolvent_subs(true);
     solver.set_max_red_linkin_size(0);
     solver.set_timeout_all_calls(100);
     solver.set_weaken_time_limitM(2000);
     solver.set_occ_based_lit_rem_time_limitM(500);
 
-
     // occ-ternary-res not used
     // eqlit-find ? (too slow)
     string str("full-probe, sub-cls-with-bin, must-scc-vrepl, must-scc-vrepl, distill-cls-onlyrem, sub-impl, occ-resolv-subs, occ-del-blocked, occ-backw-sub, occ-rem-with-orgates, occ-bve, occ-ternary-res, ");
     solver.simplify(&dont_elim, &str);
     str = string(",intree-probe, occ-backw-sub-str, sub-str-cls-with-bin, clean-cls, distill-cls,distill-bins, ") + str;
 
     solver.simplify(&dont_elim, &str);
     solver.simplify(&dont_elim, &str);
     solver.simplify(&dont_elim, &str);
     if (sparsify) {
-        str = string("sparsify,") + str;
-        solver.simplify(&dont_elim, &str);
+        string str2 = string("sparsify,") + str;
+        solver.simplify(&dont_elim, &str2);
     }
+    //one more without sparsify
+    solver.simplify(&dont_elim, &str);
 
     str = string("");
     if (arjdata->common.definitely_satisfiable) {
         str += string("occ-rem-unconn-assumps, ");
     }
     str += string(", must-scc-vrepl, must-renumber");
     solver.simplify(&dont_elim, &str);
 
-    vector<uint32_t> new_sampl_set;
-    for(const auto& l: dont_elim) new_sampl_set.push_back(l.var());
-    auto cnf = get_simplified_renumbered_cnf(&solver, new_sampl_set);
-    return std::make_tuple(cnf, new_sampl_set, empty_vars.size());
+    vector<uint32_t> new_sampl_vars (sampl_vars);
+    SimplifiedCNF cnf;
+    get_simplified_cnf(&solver, new_sampl_vars, renumber, cnf.cnf, cnf.nvars);
+
+    vector<uint32_t> empty_occs;
+    if (arjdata->common.conf.empty_occs_based)
+        solver.find_equiv_subformula(new_sampl_vars, empty_occs);
+    std::sort(new_sampl_vars.begin(), new_sampl_vars.end());
+    cnf.sampling_vars = new_sampl_vars;
+    cnf.empty_occs = empty_occs.size();
+    return cnf;
 }
 
-
 DLL_PUBLIC void Arjun::set_pred_forever_cutoff(int pred_forever_cutoff)
 {
     arjdata->common.solver->set_pred_forever_cutoff(pred_forever_cutoff);
 }
 
 DLL_PUBLIC void Arjun::set_every_pred_reduce(int every_pred_reduce)
 {
@@ -642,11 +459,7 @@
 }
 
 DLL_PUBLIC void Arjun::set_empty_occs_based(const bool empty_occs_based)
 {
     arjdata->common.conf.empty_occs_based = empty_occs_based;
 }
 
-DLL_PUBLIC void Arjun::set_mirror_empty(const bool mirror_empty)
-{
-    arjdata->common.conf.mirror_empty = mirror_empty;
-}
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/arjun.h` & `pyapproxmc-4.1.9/python/arjun/src/arjun.h`

 * *Files 5% similar despite different names*

```diff
@@ -31,14 +31,21 @@
 #ifdef CMS_LOCAL_BUILD
 #include "cryptominisat.h"
 #else
 #include <cryptominisat5/cryptominisat.h>
 #endif
 
 namespace ArjunNS {
+    struct SimplifiedCNF {
+        std::vector<std::vector<CMSat::Lit>> cnf;
+        std::vector<uint32_t> sampling_vars;
+        uint32_t nvars;
+        uint32_t empty_occs;
+    };
+
     struct ArjPrivateData;
     #ifdef _WIN32
     class __declspec(dllexport) Arjun
     #else
     class Arjun
     #endif
     {
@@ -69,75 +76,70 @@
         std::vector<uint32_t> get_empty_occ_sampl_vars() const;
 
         //Get clauses
         void start_getting_small_clauses(uint32_t max_len, uint32_t max_glue, bool red = true);
         bool get_next_small_clause(std::vector<CMSat::Lit>& ret); //returns FALSE if no more
         void end_getting_small_clauses();
         const std::vector<CMSat::Lit> get_internal_cnf(uint32_t& num_cls) const;
-        std::tuple<std::pair<std::vector<std::vector<CMSat::Lit>>, uint32_t>, std::vector<uint32_t>, uint32_t>
-            get_fully_simplified_renumbered_cnf(
+        SimplifiedCNF get_fully_simplified_renumbered_cnf(
             const std::vector<uint32_t>& sampl_vars,
-            const std::vector<uint32_t>& empty_vars,
             const uint32_t orig_num_vars,
             const bool sparsify = true,
             const bool renumber = true);
         const std::vector<CMSat::BNN*>& get_bnns() const;
         std::vector<CMSat::Lit> get_zero_assigned_lits() const;
         std::vector<std::pair<CMSat::Lit, CMSat::Lit> > get_all_binary_xors() const;
+        const std::vector<CMSat::Lit>& get_orig_cnf();
 
         //Set config
         void set_seed(uint32_t seed);
         void set_verbosity(uint32_t verb);
         void set_fast_backw(bool fast_backw);
         void set_distill(bool distill);
         void set_intree(bool intree);
-        void set_guess(bool guess);
         void set_simp(bool simp);
-        void set_pre_simplify(bool simp);
-        void set_incidence_sort(uint32_t incidence_sort);
+        void set_bve_pre_simplify(bool bve_pre_simp);
+        void set_unknown_sort(uint32_t unknown_sort);
+        void set_incidence_count(uint32_t incidence_count);
         void set_or_gate_based(bool or_gate_based);
         void set_xor_gates_based(bool xor_gates_based);
         void set_probe_based(bool probe_based);
-        void set_forward(bool forward);
         void set_backward(bool backward);
-        void set_assign_fwd_val(bool assign_fwd_val);
         void set_backw_max_confl(uint32_t backw_max_confl);
         void set_gauss_jordan(bool gauss_jordan);
-        void set_regularly_simplify(bool reg_simp);
-        void set_fwd_group(uint32_t forward_group);
         void set_find_xors(bool find_xors);
         void set_backbone_simpl(bool backbone_simpl);
         void set_ite_gate_based(bool ite_gate_based);
         void set_irreg_gate_based(const bool irreg_gate_based);
         void set_gate_sort_special(bool gate_sort_special);
         void set_backbone_simpl_max_confl(uint64_t backbone_simpl_max_confl);
         //void set_polar_mode(CMSat::PolarityMode mode);
+        void set_no_gates_below(double no_gates_below);
         void set_pred_forever_cutoff(int pred_forever_cutoff = -1);
         void set_every_pred_reduce(int every_pred_reduce = -1);
         void set_empty_occs_based(const bool empty_occs_based);
-        void set_mirror_empty(const bool mirror_empty);
+        void set_specified_order_fname(std::string specified_order_fname);
 
         //Get config
+        std::string get_specified_order_fname() const;
+        double get_no_gates_below() const;
+        bool get_simp() const;
         uint32_t get_verbosity() const;
         bool get_fast_backw() const;
         bool get_distill() const;
         bool get_intree() const;
-        bool get_guess() const;
-        bool get_pre_simplify() const;
-        uint32_t get_incidence_sort() const;
+        bool get_bve_pre_simplify() const;
+        uint32_t get_incidence_count() const;
+        uint32_t get_unknown_sort() const;
         bool get_or_gate_based() const;
         bool get_xor_gates_based() const;
         bool get_probe_based() const;
-        bool get_forward() const;
         bool get_backward() const;
-        bool get_assign_fwd_val() const;
         uint32_t get_backw_max_confl() const;
         bool get_gauss_jordan() const;
-        bool get_regularly_simplify() const;
-        uint32_t get_fwd_group() const;
         bool get_find_xors() const;
         bool get_backbone_simpl() const;
         bool get_ite_gate_based() const;
         bool get_irreg_gate_based() const;
         bool get_gate_sort_special() const;
 
         long unsigned get_backbone_simpl_max_confl() const;
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/backward.cpp` & `pyapproxmc-4.1.9/python/arjun/src/backward.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -19,14 +19,16 @@
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
  */
 
 #include "common.h"
+#include <set>
+
 using namespace ArjunInt;
 
 void Common::fill_assumptions_backward(
     vector<Lit>& assumptions,
     vector<uint32_t>& unknown,
     const vector<char>& unknown_set,
     const vector<uint32_t>& indep)
@@ -90,21 +92,46 @@
         assert(x < orig_num_vars);
         assert(unknown_set[x] == 0 && "No var should be in 'sampling_set' twice!");
         unknown.push_back(x);
         unknown_set[x] = 1;
     }
 
     sort_unknown(unknown);
+
+    if (conf.specified_order_fname != "") {
+        std::set<uint32_t> old_unknown(unknown.begin(), unknown.end());
+        unknown.clear();
+
+        std::ifstream infile(conf.specified_order_fname);
+        std::string line;
+        uint32_t line_num = 1;
+        while (std::getline(infile, line))
+        {
+            std::istringstream iss(line);
+            int a;
+            if (!(iss >> a)) {
+                cout << "ERROR: the file '" << conf.specified_order_fname << "' contains a line we cannot parse to be a variable number" << endl;
+                cout << "ERROR line number: " << line_num << std::endl;
+                cout << "ERROR: lines should ONLY contain a single variable" << endl;
+                exit(-1);
+            }
+            if (old_unknown.find(a) == old_unknown.end()) {
+                cout << "WARNING: the variable " << a << " is in the order file but not in the original order." << endl;
+            }
+            unknown.push_back(a);
+            line_num++;
+        }
+    }
+
     if (conf.verb >= 4) {
         cout << "Sorted output: "<< endl;
         for (const auto& v:unknown) {
-            cout
-            << "Var: " << std::setw(6) << v
-            << " inc: " << std::setw(6) << incidence[v]
-            << " prop-inc: " << std::setw(6) << incidence_probing[v];
+            cout << "c var: " << v << " occ: " << incidence[v]
+            //<< " prop-inc: " << std::setw(6) << incidence_probing[v]
+            << endl;
             if (var_to_num_communities.size() > v) {
                 cout << " fan-out to comms: " << std::setw(6) << var_to_num_communities[v].size();
             }
             cout << endl;
         }
     }
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/common.cpp` & `pyapproxmc-4.1.9/python/arjun/src/common.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -208,20 +208,22 @@
     incidence.resize(orig_num_vars, 0);
     incidence_probing.resize(orig_num_vars, 0);
     assert(solver->nVars() == orig_num_vars);
     vector<uint32_t> inc = solver->get_lit_incidence();
     assert(inc.size() == orig_num_vars*2);
     for(uint32_t i = 0; i < orig_num_vars; i++) {
         Lit l = Lit(i, true);
-        if (conf.incidence_sort == 10) {
+        if (conf.incidence_count == 1) {
             incidence[l.var()] = inc[l.toInt()] + inc[(~l).toInt()];
-        } else if (conf.incidence_sort == 11) {
+        } else if (conf.incidence_count == 2) {
             incidence[l.var()] = std::max(inc[l.toInt()], inc[(~l).toInt()]);
-        } else {
+        } else if (conf.incidence_count == 3) {
             incidence[l.var()] = std::min(inc[l.toInt()],inc[(~l).toInt()]);
+        } else {
+            assert(false && "This is NOT accepted incidence count");
         }
     }
 }
 
 void Common::set_up_solver()
 {
     assert(solver == NULL);
@@ -286,45 +288,44 @@
 bool Common::preproc_and_duplicate()
 {
     orig_num_vars = solver->nVars();
     seen.clear();
     seen.resize(solver->nVars(), 0);
 
     get_incidence();
-    if (conf.incidence_sort == 4 || conf.incidence_sort == 5) {
-        #ifdef LOUVAIN_COMMS
-        calc_community_parts();
-        #else
-        cout << "ERROR: you must compile with louvain community libraries for this to work. Install https://github.com/meelgroup/louvain-community first." << endl;
-        exit(-1);
-        #endif
-    }
+    calc_community_parts();
     if (conf.simp && !simplify()) return false;
+    get_incidence();
     duplicate_problem();
     if (conf.simp && !simplify_bve_only()) return false;
     add_fixed_clauses();
     if (!run_gauss_jordan()) return false;
 
     //Seen needs re-init, because we got new variables
     seen.clear(); seen.resize(solver->nVars(), 0);
 
-    solver->set_simplify(conf.regularly_simplify && conf.simp);
+    solver->set_simplify(conf.simp);
     solver->set_intree_probe(conf.intree && conf.simp);
     solver->set_distill(conf.distill && conf.simp);
     solver->set_find_xors(conf.gauss_jordan && conf.simp);
     return true;
 }
 
-#ifdef LOUVAIN_COMMS
 void Common::calc_community_parts()
 {
-    double myTime = cpuTime();
-    if (conf.verb) {
-        cout << "c [arjun] Calculating Louvain Communities..." << endl;
+    if (!(conf.unknown_sort == 4 || conf.unknown_sort == 5)) {
+        return;
     }
+    #ifndef LOUVAIN_COMMS
+    cout << "ERROR: you must compile with louvain community libraries for this to work."
+        << " Install https://github.com/meelgroup/louvain-community first." << endl;
+    exit(-1);
+    #else
+    double myTime = cpuTime();
+    verb_print(1, "[arjun] Calculating Louvain Communities...");
 
     vector<vector<Lit>> cnf;
     solver->start_getting_small_clauses(
         std::numeric_limits<uint32_t>::max(),
         std::numeric_limits<uint32_t>::max(),
         false);
 
@@ -410,15 +411,12 @@
                 uint32_t comm = commpart[cl[i2].var()];
                 var_to_num_communities[v].insert(comm);
             }
         }
     }
     solver->end_getting_small_clauses();
 
-    if (conf.verb) {
-        cout << "c [mis-comm] Number of communities: " << commpart_incs.size()
-        << " T: " << (cpuTime() - myTime)
-        << endl;
-    }
+    verb_print(1, "[mis-comm] Number of communities: " << commpart_incs.size() \
+            << " T: " << (cpuTime() - myTime));
+#endif
 }
 
-#endif
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/common.h` & `pyapproxmc-4.1.9/python/arjun/src/common.h`

 * *Files 6% similar despite different names*

```diff
@@ -46,15 +46,14 @@
 #endif
 
 #include "time_mem.h"
 #include "config.h"
 
 using namespace CMSat;
 using std::cout;
-using std::cerr;
 using std::endl;
 using std::map;
 using std::set;
 using std::string;
 using std::vector;
 
 namespace ArjunInt {
@@ -110,29 +109,29 @@
 
     //total incidence in a commpart. Maps commpart->maxinc
     vector<uint32_t> commpart_incs;
 
     vector<Lit> dont_elim;
     vector<Lit> tmp_implied_by;
 
+    // cnf as we parsed it in (no simplification whatsoever)
+    vector<Lit> orig_cnf;
 
     void update_sampling_set(
         const vector<uint32_t>& unknown,
         const vector<char>& unknown_set,
         const vector<uint32_t>& indep
     );
     bool preproc_and_duplicate();
     void add_fixed_clauses();
     void print_orig_sampling_set();
     void start_with_clean_sampling_set();
     void duplicate_problem();
     void get_incidence();
-    #ifdef LOUVAIN_COMMS
     void calc_community_parts();
-    #endif
     void set_up_solver();
     vector<Lit> get_cnf();
     std::mt19937 random_source = std::mt19937(0);
 
     //simp
     vector<uint32_t> toClear;
     bool simplify();
@@ -261,29 +260,26 @@
 
         //Put parts with smaller MAX incidence first
         auto part_a_inc = comm->commpart_incs.at(part_a);
         auto part_b_inc = comm->commpart_incs.at(part_b);
         if (part_a_inc != part_b_inc) {
             return part_a_inc < part_b_inc;
         }
-        return false;
 
         auto a_inc = comm->incidence[a];
         auto b_inc = comm->incidence[b];
         if (a_inc != b_inc) {
             return a_inc > b_inc; //"a" has larger incidence -> return TRUE
         }
         return a < b;
     }
 
     const Common* comm;
 };
 
-
-
 struct IncidenceSorterCommPartToOtherComm
 {
     IncidenceSorterCommPartToOtherComm(const Common* _comm) :
         comm(_comm)
     {}
 
     bool operator()(const uint32_t a, const uint32_t b) {
@@ -308,25 +304,25 @@
 
     const Common* comm;
 };
 
 template<class T>
 void Common::sort_unknown(T& unknown)
 {
-    if (conf.incidence_sort == 1 || conf.incidence_sort >= 10) {
+    if (conf.unknown_sort == 1) {
         std::sort(unknown.begin(), unknown.end(), IncidenceSorter<uint32_t>(incidence));
-    } else if (conf.incidence_sort == 2) {
+    } else if (conf.unknown_sort == 2) {
         std::sort(unknown.begin(), unknown.end(), IncidenceSorter2<uint32_t>(incidence, incidence_probing));
-    } else if (conf.incidence_sort == 3) {
+    } else if (conf.unknown_sort == 3) {
         std::sort(unknown.begin(), unknown.end(), IncidenceSorter<uint32_t>(incidence_probing));
-    } else if (conf.incidence_sort == 4) {
+    } else if (conf.unknown_sort == 4) {
         std::sort(unknown.begin(), unknown.end(), IncidenceSorterCommPart(this));
-    } else if (conf.incidence_sort == 5) {
+    } else if (conf.unknown_sort == 5) {
         std::sort(unknown.begin(), unknown.end(), IncidenceSorterCommPartToOtherComm(this));
-    } else if (conf.incidence_sort == 6) {
+    } else if (conf.unknown_sort == 6) {
         std::shuffle(unknown.begin(), unknown.end(), random_source);
     } else {
         cout << "ERROR: wrong sorting mechanism given" << endl;
         exit(-1);
     }
 }
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/config.h` & `pyapproxmc-4.1.9/python/arjun/src/config.h`

 * *Files 20% similar despite different names*

```diff
@@ -21,42 +21,41 @@
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
  */
 
 #ifndef CONFIG_H
 #define CONFIG_H
 
+#include <cstdint>
+#include <string>
+
 namespace ArjunInt {
 
 struct Config {
     int verb = 3;
     int seed = 0;
     int simp = 1;
     int fast_backw = 1;
     int distill = 1;
-    int regularly_simplify = 1;
     int intree = 1;
-    int guess = 0;
-    int pre_simplify = 1;
-    int incidence_sort = 1;
+    int bve_pre_simplify = 1;
+    int incidence_count = 3; // this determines what incidence MEANS
+    int unknown_sort = 1; // this determines HOW we sort
     int or_gate_based = 1;
     int xor_gates_based = 1;
     int ite_gate_based = 1;
     int irreg_gate_based = 1;
-    int mirror_empty = 1;
-    int empty_occs_based = 0;
+    int empty_occs_based = 1;
     int probe_based = 1;
-    int forward = 0;
-    int forward_group = 10;
     int backward = 1;
-    int assign_fwd_val = 0;
     int gauss_jordan = 0;
     int backbone_simpl = 0;
+    double no_gates_below = 0.01;
+    std::string specified_order_fname;
     unsigned long backbone_simpl_max_confl = 10ULL*1000ULL;
-    uint32_t backw_max_confl = 500;
-    uint32_t guess_max_confl = 1000;
+    uint32_t backw_max_confl = 5000;
 };
 
 }
 
 //ARJUN_CONFIG_H
 #endif
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/simplify.cpp` & `pyapproxmc-4.1.9/python/arjun/src/simplify.cpp`

 * *Files 7% similar despite different names*

```diff
@@ -44,21 +44,29 @@
 bool Common::simplify()
 {
     assert(conf.simp);
     check_no_duplicate_in_sampling_set();
     auto old_size = sampling_set->size();
     double myTime = cpuTime();
 
+    if (sampling_set->size() < 10000) {
+        cout << "c WARNING: Turning off gates, because the sampling size is small, so we can just do it" << endl;
+        conf.xor_gates_based = 0;
+        conf.ite_gate_based = 0;
+        conf.or_gate_based = 0;
+        conf.irreg_gate_based = 0;
+    }
+
     if (conf.xor_gates_based || conf.or_gate_based || conf.ite_gate_based) {
         remove_definable_by_gates();
     }
     if (conf.irreg_gate_based) remove_definable_by_irreg_gates();
     if (conf.empty_occs_based) find_equiv_subformula();
 
-    if (conf.pre_simplify) {
+    if (conf.bve_pre_simplify) {
         verb_print(1, "[arjun-simp] CMS::simplify() with no BVE, intree probe...");
         double simpTime = cpuTime();
         solver->set_bve(0);
         solver->set_intree_probe(1);
         if (solver->simplify() == l_False) return false;
         solver->set_intree_probe(conf.intree);
         verb_print(1,"[arjun-simp] CMS::simplify() with no BVE finished."
@@ -75,15 +83,14 @@
         if (ret == l_True) definitely_satisfiable = true;
         solver->set_verbosity(std::max<int>(conf.verb-2, 0));
     }
 
     remove_eq_literals();
     remove_zero_assigned_literals();
     if (conf.probe_based && !probe_all()) return false;
-
     if (conf.empty_occs_based) find_equiv_subformula();
     if (conf.irreg_gate_based) remove_definable_by_irreg_gates();
 
     solver->set_verbosity(std::max<int>(conf.verb-2, 0));
 
     verb_print(1, "[arjun] simplification finished "
         << " removed: " << (old_size-sampling_set->size())
@@ -91,28 +98,14 @@
         << stats_line_percent(old_size-sampling_set->size(), old_size)
         << " T: " << (cpuTime() - myTime));
 
     check_no_duplicate_in_sampling_set();
     return true;
 }
 
-struct IncSorterAsc
-{
-    IncSorterAsc(const vector<uint32_t>& _inc) :
-        inc(_inc)
-    {}
-
-    bool operator()(const uint32_t a, const uint32_t b) const {
-        //Return that the order is OK when "a" has less incidence than "b"
-        return inc[a] < inc[b];
-    }
-
-    const vector<uint32_t>& inc;
-};
-
 bool Common::backbone_simpl()
 {
     if (conf.verb) {
         cout << "c [backbone-simpl] starting backbone simplification..." << endl;
     }
     uint64_t last_sum_conflicts = 0;
     int64_t max_confl = conf.backbone_simpl_max_confl;
@@ -274,27 +267,14 @@
         << stats_line_percent(old_size-sampling_set->size(), old_size)
         << " T: " << (cpuTime() - myTime) << endl;
     }
 
     return true;
 }
 
-struct OccurSorter {
-    OccurSorter(const vector<vector<uint32_t>>& _occ) :
-        occ(_occ)
-    {}
-
-    bool operator()(uint32_t v1, uint32_t v2) const {
-        return occ[v1].size() < occ[v2].size();
-    }
-
-    const vector<vector<uint32_t>>& occ;
-
-};
-
 enum class gate_t {or_gate, xor_gate, ite_gate};
 
 struct GateOccurs
 {
     GateOccurs(gate_t _t, uint32_t _at) :
         t(_t),
         at(_at)
@@ -393,25 +373,37 @@
         if (all_orig && num == itegate.get_all().size()) {
             rhs_incidence[itegate.rhs.var()]++;
             vars_gate_occurs[itegate.rhs.var()].push_back(GateOccurs(gate_t::ite_gate, i));
             potential++;
         }
     }
 
-
     if (conf.verb > 4) cout << "c [arjun-simp] XOR Potential: " << potential << endl;
 
     order_sampl_set_for_simp();
     uint32_t non_zero_occs = 0;
-    uint32_t seen_set_0 = 0;
+
+    // If this is large, it means it'd get removed anyway:
+    //       bottom of the pie, we go through the pile in reverse order to try to remove
+    vector<double> var_to_rel_position(orig_num_vars, 1.0);
+    for(uint32_t i = 0; i < sampling_set->size(); i++) {
+        assert(sampling_set->at(i) < orig_num_vars);
+        var_to_rel_position[sampling_set->at(i)] = (double)(sampling_set->size()-i)/(double)sampling_set->size();
+    }
+
     for(uint32_t v: *sampling_set) {
         assert(seen[v]);
         if (vars_gate_occurs[v].size() == 0) {
             continue;
         }
+
+        // Only try removing if it's at the bottom X percent of unknown_sort
+        // If 0.01 is SMALLER, then we have to remove with backward LESS
+        if (var_to_rel_position[v] < conf.no_gates_below) continue;
+
         non_zero_occs++;
         //cout << "Trying to define var " << v << " size of lookup: " << vars_xor_occurs[v].size() << endl;
 
         //Define v as a function of the other variables in the XOR
         for(const auto& gate: vars_gate_occurs[v]) {
             if (gate.t == gate_t::xor_gate) {
                 const auto& x = xors[gate.at];
@@ -432,15 +424,14 @@
                     //have been set to be defined themselves. Cycle could happen.
                     continue;
                 }
 
                 //All good, we can define v in terms of the other variables
                 assert(found_v);
                 seen[v] = 0;
-                seen_set_0++;
                 break;
             } else if (gate.t == gate_t::or_gate) {
                 const auto& o = ors[gate.at];
                 bool ok = true;
                 for(auto& or_l: o.get_lhs()) {
                     if (!seen[or_l.var()]) {
                         ok = false;
@@ -449,15 +440,14 @@
                 }
                 if (!ok) {
                     //In the meanwhile, the variable that could define this
                     //have been set to be defined themselves. Cycle could happen.
                     continue;
                 }
                 seen[v] = 0;
-                seen_set_0++;
                 break;
             } else if (gate.t == gate_t::ite_gate) {
                 const auto& ite = ites[gate.at];
                 bool ok = true;
                 for(auto& ite_l: ite.lhs) {
                     if (!seen[ite_l.var()]) {
                         ok = false;
@@ -466,15 +456,14 @@
                 }
                 if (!ok) {
                     //In the meanwhile, the variable that could define this
                     //have been set to be defined themselves. Cycle could happen.
                     continue;
                 }
                 seen[v] = 0;
-                seen_set_0++;
                 break;
             } else {
                 assert(false);
             }
         }
     }
 
@@ -503,26 +492,26 @@
 
     return changed;
 }
 
 void Common::order_sampl_set_for_simp()
 {
     get_incidence();
-    std::sort(sampling_set->begin(), sampling_set->end(), IncidenceSorter<uint32_t>(incidence));
+    sort_unknown(*sampling_set);
     std::reverse(sampling_set->begin(), sampling_set->end()); //we want most likely independent as last
 }
 
 void Common::find_equiv_subformula()
 {
     assert(conf.empty_occs_based);
     const double myTime = cpuTime();
     uint32_t old_size = sampling_set->size();
 
     solver->set_verbosity(std::max<int>(conf.verb-2, 0));
-    solver->find_equiv_subformula(*sampling_set, empty_occs, conf.mirror_empty);
+    solver->find_equiv_subformula(*sampling_set, empty_occs);
 
     if (conf.verb) {
         cout << "c [arjun-simp] equiv-subform"
         << " removed: " << (old_size-sampling_set->size())
         << " perc: " << std::fixed << std::setprecision(2)
         << stats_line_percent(old_size-sampling_set->size(), old_size)
         << " total equiv_subform now: " << empty_occs.size()
```

### Comparing `pyapproxmc-4.1.8/python/arjun/src/time_mem.h` & `pyapproxmc-4.1.9/python/arjun/src/time_mem.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/python/src/GitSHA1.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/python/src/GitSHA1.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/GitSHA1.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/GitSHA1.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/MersenneTwister.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/MersenneTwister.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/Vec.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/Vec.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/XAlloc.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/XAlloc.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/alg.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/alg.h`

 * *Files 5% similar despite different names*

```diff
@@ -16,14 +16,15 @@
 DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT
 OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
 *******************************************************************************/
 
 #ifndef Alg_h
 #define Alg_h
 
+#include <cstdint>
 #include <iostream>
 #include "solvertypes.h"
 #include "watched.h"
 #include "constants.h"
 
 namespace CMSat {
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/avgcalc.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/avgcalc.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/bitarray.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/bitarray.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/boundedqueue.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/boundedqueue.h`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,15 @@
 #define BOUNDEDQUEUE_H
 
 #include "constants.h"
 #include "avgcalc.h"
 #include <cassert>
 #include <vector>
 #include <cstring>
+#include <cstdint>
 #include <sstream>
 #include <iomanip>
 
 namespace CMSat {
 using std::vector;
 
 template <class T, class T2 = uint64_t>
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/bva.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/bva.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/bva.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/bva.h`

 * *Files 2% similar despite different names*

```diff
@@ -23,14 +23,15 @@
 #ifndef __BVA_H__
 #define __BVA_H__
 
 #include "heap.h"
 #include "watched.h"
 #include "clause.h"
 #include "touchlist.h"
+#include <cstdint>
 #include <vector>
 using std::vector;
 
 namespace CMSat {
 
 class Solver;
 class OccSimplifier;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cardfinder.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/cardfinder.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cardfinder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cardfinder.h`

 * *Files 2% similar despite different names*

```diff
@@ -23,14 +23,15 @@
 #ifndef _CARDFINDER_H_
 #define _CARDFINDER_H_
 
 #include <vector>
 #include <set>
 #include <iostream>
 #include <algorithm>
+#include <cstdint>
 #include <set>
 #include <limits>
 #include "xor.h"
 #include "cset.h"
 #include "watcharray.h"
 
 using std::vector;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ccnr.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/ccnr.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ccnr.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/ccnr.h`

 * *Files 1% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 ***********************************************/
 
 #ifndef CCNR_H
 #define CCNR_H
 
+#include <cstdint>
 #include <string>
 #include <vector>
 #include "ccnr_mersenne.h"
 
 using std::vector;
 
 namespace CCNR {
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_cms.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_cms.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_cms.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_cms.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ccnr_mersenne.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/ccnr_mersenne.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_abs.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_abs.h`

 * *Files 1% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 ***********************************************/
 
 #ifndef _CLPREDICTORS_ABST_H__
 #define _CLPREDICTORS_ABST_H__
 
+#include <cstdint>
 #include <vector>
 #include <cassert>
 #include <string>
 #include <cmath>
 #include <xgboost/c_api.h>
 #include "clause.h"
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_lgbm.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_lgbm.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_py.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_py.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cl_predictors_xgb.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cl_predictors_xgb.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clabstraction.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/clabstraction.h`

 * *Files 6% similar despite different names*

```diff
@@ -20,14 +20,16 @@
 THE SOFTWARE.
 ***********************************************/
 
 
 #ifndef __CL_ABSTRACTION__H__
 #define __CL_ABSTRACTION__H__
 
+#include <cstdint>
+
 typedef uint32_t cl_abst_type;
 static const int cl_abst_modulo = 29;
 
 inline cl_abst_type abst_var(const uint32_t v)
 {
     return 1UL << (v % cl_abst_modulo);
 }
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clause.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/clause.h`

 * *Files 0% similar despite different names*

```diff
@@ -21,14 +21,15 @@
 ***********************************************/
 
 
 #ifndef CLAUSE_H
 #define CLAUSE_H
 
 #include <cstdio>
+#include <cstdint>
 #include <vector>
 #include <sys/types.h>
 #include <string.h>
 #include <limits>
 
 #include "solverconf.h"
 #include "solvertypes.h"
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clauseallocator.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/clauseallocator.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clauseallocator.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/clauseallocator.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clausecleaner.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/clausecleaner.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/clausecleaner.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/clausecleaner.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cloffset.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cloffset.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cms_bosphorus.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cms_bosphorus.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cms_breakid.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cms_breakid.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cms_windows_includes.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cms_windows_includes.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cnf.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/cnf.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cnf.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cnf.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/community_finder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/community_finder.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/completedetachreattacher.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/completedetachreattacher.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/completedetachreattacher.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/completedetachreattacher.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/constants.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/constants.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -202,104 +202,104 @@
         case 0: {
             //default setup
             break;
         }
 
         case 1: {
             //Minisat-like
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.varElimRatioPerIter = 1;
             conf.restartType = Restart::geom;
             conf.polarity_mode = CMSat::PolarityMode::polarmode_neg;
 
             conf.inc_max_temp_lev2_red_cls = 1.02;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0.5;
             break;
         }
         case 2: {
-            conf.branch_strategy_setup = "vsidsx";
+            conf.branch_strategy_setup = "vsids";
 //             conf.polar_best_inv_every_n = 100;
             break;
         }
         case 3: {
             //Similar to CMS 2.9 except we look at learnt DB size insteead
             //of conflicts to see if we need to clean.
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0.5;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0;
             conf.glue_put_lev0_if_below_or_eq = 0;
             conf.inc_max_temp_lev2_red_cls = 1.03;
             break;
         }
         case 4: {
             //Similar to CMS 5.0
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.varElimRatioPerIter = 0.4;
             conf.every_lev1_reduce = 0;
             conf.every_lev2_reduce = 0;
             conf.do_bva = false;
             conf.max_temp_lev2_learnt_clauses = 30000;
             conf.glue_put_lev0_if_below_or_eq = 4;
 
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0.5;
             break;
         }
         case 5: {
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.never_stop_search = true;
             break;
         }
         case 6: {
             //Maple with backtrack
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
 //             conf.polar_stable_every_n = 10000;
             break;
         }
         case 7: {
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.do_bva = false;
             conf.glue_put_lev0_if_below_or_eq = 2;
             conf.varElimRatioPerIter = 1;
             conf.inc_max_temp_lev2_red_cls = 1.04;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0.1;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0.3;
             break;
         }
         case 8: {
             //Different glue limit
-            conf.branch_strategy_setup = "maple2";
+            conf.branch_strategy_setup = "vmtf";
             conf.glue_put_lev0_if_below_or_eq = 2;
             conf.glue_put_lev1_if_below_or_eq = 2;
             break;
         }
         case 9: {
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
 //             conf.polar_stable_every_n = 1;
             break;
         }
         case 10: {
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.polarity_mode = CMSat::PolarityMode::polarmode_pos;
 //             conf.polar_stable_every_n = 100000;
             break;
         }
         case 11: {
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.varElimRatioPerIter = 1;
             conf.restartType = Restart::geom;
 
             conf.inc_max_temp_lev2_red_cls = 1.01;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0.3;
             break;
         }
         case 12: {
-            conf.branch_strategy_setup = "maple1";
+            conf.branch_strategy_setup = "vmtf";
             conf.inc_max_temp_lev2_red_cls = 1.001;
 //             conf.polar_stable_every_n = 7;
 //             conf.polar_best_inv_every_n = 6;
             break;
         }
 
         case 13: {
@@ -311,15 +311,15 @@
             conf.inc_max_temp_lev2_red_cls = 1.02;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::glue)] = 0;
             conf.ratio_keep_clauses[clean_to_int(ClauseClean::activity)] = 0.5;
             break;
         }
         case 14: {
             //Different glue limit
-            conf.branch_strategy_setup = "vsids1";
+            conf.branch_strategy_setup = "vsids";
             conf.do_bva = false;
             conf.doMinimRedMoreMore = 1;
             conf.glue_put_lev0_if_below_or_eq = 4;
             //conf.glue_put_lev2_if_below_or_eq = 8;
             conf.max_num_lits_more_more_red_min = 3;
             conf.max_glue_more_minim = 4;
             break;
@@ -348,15 +348,15 @@
         }
         case 17: {
             //conf.max_temporary_learnt_clauses = 10000;
             conf.do_bva = true;
             break;
         }
         case 18: {
-            conf.branch_strategy_setup = "vsids1+vsids2";
+            conf.branch_strategy_setup = "vsids";
             conf.every_lev1_reduce = 0;
             conf.every_lev2_reduce = 0;
             conf.glue_put_lev1_if_below_or_eq = 0;
             conf.max_temp_lev2_learnt_clauses = 10000;
             break;
         }
 
@@ -370,31 +370,31 @@
 //             conf.polar_stable_every_n = 4;
             //conf.max_temporary_learnt_clauses = 10000;
             break;
         }
 
         case 20: {
             //Luby
-            conf.branch_strategy_setup = "maple2";
+            conf.branch_strategy_setup = "vmtf";
             conf.restart_inc = 1.5;
             conf.restart_first = 100;
             conf.restartType = Restart::luby;
 //             conf.polar_stable_every_n = 2;
             break;
         }
 
         case 21: {
-            conf.branch_strategy_setup = "vsids2";
+            conf.branch_strategy_setup = "vsids";
             conf.glue_put_lev0_if_below_or_eq = 3;
             conf.glue_put_lev1_if_below_or_eq = 5;
             break;
         }
 
         case 22: {
-            conf.branch_strategy_setup = "maple1";
+            conf.branch_strategy_setup = "vmtf";
             conf.doMinimRedMoreMore = 0;
             conf.orig_global_timeout_multiplier = 5;
             conf.num_conflicts_of_search_inc = 1.15;
             conf.more_red_minim_limit_binary = 600;
             conf.max_num_lits_more_more_red_min = 20;
             //conf.max_temporary_learnt_clauses = 10000;
             break;
@@ -1521,17 +1521,17 @@
 
 DLL_PUBLIC std::vector<uint32_t> SATSolver::remove_definable_by_irreg_gate(const vector<uint32_t>& vars)
 {
     return data->solvers[0]->remove_definable_by_irreg_gate(vars);
 }
 
 DLL_PUBLIC void SATSolver::find_equiv_subformula(
-    std::vector<uint32_t>& sampl_vars, std::vector<uint32_t>& empty_vars, const bool mirror)
+    std::vector<uint32_t>& sampl_vars, std::vector<uint32_t>& empty_vars)
 {
-    return data->solvers[0]->find_equiv_subformula(sampl_vars, empty_vars, mirror);
+    return data->solvers[0]->find_equiv_subformula(sampl_vars, empty_vars);
 }
 
 DLL_PUBLIC lbool SATSolver::find_fast_backw(FastBackwData fast_backw)
 {
     assert(data->solvers.size() == 1);
     data->solvers[0]->fast_backw = fast_backw;
     bool backup_doVarElim = data->solvers[0]->conf.doVarElim;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat.h`

 * *Files 1% similar despite different names*

```diff
@@ -102,15 +102,15 @@
         void set_allow_otf_gauss(); //allow on-the-fly gaussian elimination
         /**
          * CPU time (in seconds) that can be consumed before the next call to solve() must return
          *
          * Because the elapsed CPU time depends on both the number of
          * threads, and the activity of these threads, the elapsed time
          * can wildly differ from wall clock time.
-         * 
+         *
          * \pre max_time >= 0
          */
         void set_max_time(double max_time);
         /**
          * Conflicts that can be consumed before the next call to solve() must return
          *
          * \pre max_confl >= 0
@@ -212,15 +212,15 @@
 
         //////////////////////
         // EXPERIMENTAL
         std::vector<std::pair<std::vector<uint32_t>, bool> > get_recovered_xors(bool xor_together_xors) const; //get XORs recovered. If "xor_together_xors" is TRUE, then xors that share a variable (and ONLY they share them) will be XORed together
         std::vector<OrGate> get_recovered_or_gates();
         std::vector<ITEGate> get_recovered_ite_gates();
         std::vector<uint32_t> remove_definable_by_irreg_gate(const std::vector<uint32_t>& vars);
-        void find_equiv_subformula(std::vector<uint32_t>& sampl_vars, std::vector<uint32_t>& empty_vars, const bool mirror);
+        void find_equiv_subformula(std::vector<uint32_t>& sampl_vars, std::vector<uint32_t>& empty_vars);
         std::vector<uint32_t> get_var_incidence();
         std::vector<uint32_t> get_lit_incidence();
         std::vector<uint32_t> get_var_incidence_also_red();
         std::vector<double> get_vsids_scores();
 
         lbool find_fast_backw(FastBackwData fast_backw);
         void remove_and_clean_all();
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat_c.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat_c.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cryptominisat_c.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cryptominisat_c.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/cset.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/cset.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/datasync.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/datasync.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/datasync.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/datasync.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/datasyncserver.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/datasyncserver.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/dimacsparser.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/dimacsparser.h`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -68,17 +68,17 @@
         bool parse_and_add_bnn_clause(C& in);
         #endif
         bool match(C& in, const char* str);
         bool parse_header(C& in);
         bool parseComments(C& in, const std::string& str);
         std::string stringify(uint32_t x) const;
         bool check_var(const uint32_t var);
+        bool parseWeight(C& in);
 
         #ifdef DEBUG_DIMACSPARSER_CMS
-        bool parseWeight(C& in);
         bool parse_solve_simp_comment(C& in, const bool solve);
         void write_solution_to_debuglib_file(const lbool ret) const;
         #endif
 
         bool parseIndependentSet(C& in);
         std::string get_debuglib_fname() const;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerbin.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerbin.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerbin.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerbin.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlitrem.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlitrem.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlitrem.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlitrem.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlong.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlong.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlong.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlong.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlongwithimpl.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlongwithimpl.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/distillerlongwithimpl.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/distillerlongwithimpl.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/frat.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/frat.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/frat.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/frat.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gatefinder.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/gatefinder.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gatefinder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/gatefinder.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gaussian.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/gaussian.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gaussian.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/gaussian.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gausswatched.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/gausswatched.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/get_clause_query.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/get_clause_query.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -89,14 +89,15 @@
 {
     if (simplified) {
         assert(solver->get_num_bva_vars() == 0);
         vector<uint32_t> ret;
         for(uint32_t v: sampl_set) {
             v = solver->varReplacer->get_var_replaced_with_outer(v);
             v = solver->map_outer_to_inter(v);
+            if (solver->value(v) != l_Undef) continue;
             assert(solver->varData[v].removed == Removed::none);
             if (!solver->seen[v]) {
                 ret.push_back(v);
                 solver->seen[v] = 1;
             }
         }
         for(uint32_t v: sampl_set) {
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/get_clause_query.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/get_clause_query.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/gqueuedata.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/gqueuedata.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/hasher.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/hasher.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/heap.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/heap.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/hyperengine.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/hyperengine.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/hyperengine.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/hyperengine.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/intree.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/intree.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/intree.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/intree.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/ipasir.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/ipasir.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/lucky.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/lucky.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/lucky.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/lucky.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/main.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/main.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/main_common.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/main_common.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/matrixfinder.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/matrixfinder.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/matrixfinder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/matrixfinder.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/msvc/stdint.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/msvc/stdint.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/mystack.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/mystack.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/nomutex.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/nomutex.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/occsimplifier.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/occsimplifier.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -75,17 +75,15 @@
 #define VERBOSE_DEBUG_XOR_FINDER
 #define VERBOSE_DEBUG_VARELIM
 #endif
 
 using namespace CMSat;
 using std::cout;
 using std::endl;
-using std::sort;
 using std::unique;
-using std::array;
 
 //#define VERBOSE_DEBUG_VARELIM
 //#define VERBOSE_DEBUG_XOR_FINDER
 //#define BIT_MORE_VERBOSITY
 //#define TOUCH_LESS
 //#define VERBOSE_ORGATE_REPLACE
 //#define VERBOSE_DEBUG_ASYMTE
@@ -1627,120 +1625,14 @@
         } else {
             assert(false);
         }
     }
     return added;
 }
 
-// check that (F | x = True) == (F | x = False)
-bool OccSimplifier::check_equiv_subformula(Lit lit)
-{
-    // Too expensive to check these
-    if (solver->watches[lit].size() + solver->watches[~lit].size() > 100) {
-        return false;
-    }
-
-    // This is not NECCESSARILY needed, due to subsumption & redundant clauses
-    if (solver->watches[lit].size() != solver->watches[~lit].size())
-        return false;
-
-    // Match binary clauses first
-    int num_bins = 0;
-    bool ok = true;
-    for(auto const& w: solver->watches[lit]) {
-        if (w.isBin() && !w.red()) {
-            seen[w.lit2().toInt()] = 1;
-            num_bins++;
-        }
-    }
-    for(auto const& w: solver->watches[~lit]) {
-        if (w.isBin() && !w.red()) {
-            if (seen[w.lit2().toInt()] == 0) {
-                ok = false;
-                break;
-            } else {
-                num_bins--;
-            }
-            seen[w.lit2().toInt()] = 0;
-        }
-    }
-    if (num_bins != 0) ok = false; // match must be exact
-
-    // Cleanup
-    for(auto const& w: solver->watches[lit]) {
-        if (w.isBin() && !w.red()) {
-            if (seen[w.lit2().toInt()] != 0) ok = false; // must match both
-            seen[w.lit2().toInt()] = 0;
-        }
-    }
-
-    if (!ok) return false;
-
-    // Match long clauses, mark covered ~lit clauses
-    equiv_subformula_cls.clear();
-    for(auto const& w: solver->watches[lit]) {
-        if (!w.isClause()) continue;
-        Clause* cl = solver->cl_alloc.ptr(w.get_offset());
-        if (cl->getRemoved() || cl->red()) continue;
-        assert(!cl->stats.marked_clause);
-
-        bool found = false;
-        for(auto const& w2: solver->watches[~lit]) {
-            if (!w2.isClause()) continue;
-            Clause* cl2 = solver->cl_alloc.ptr(w2.get_offset());
-            if (cl2->getRemoved() || cl2->red()) continue;
-            if (cl2->size() != cl->size()) continue;
-            if (cl2->abst != cl->abst) continue;
-
-            bool this_cl_ok = true;
-            for(uint32_t i = 0; i < cl->size(); i++) {
-                if ((*cl)[i] != (*cl2)[i]) {
-                    if ((*cl)[i] == ~(*cl2)[i] && (*cl)[i] == lit) {
-                        //cout << "*cl: " << *cl << " cl2: " << *cl2 << " lit: " << lit << endl;
-                        // the expected difference, on lit. ignore.
-                    } else {
-                        this_cl_ok = false;
-                        break;
-                    }
-                }
-            }
-            if (this_cl_ok) {
-                equiv_subformula_cls.push_back(std::make_pair(w.get_offset(), w2.get_offset()));
-                cl2->stats.marked_clause = true;
-                found = true;
-                break;
-            }
-        }
-        if (!found) {
-            ok = false;
-            break;
-        }
-    }
-
-    // Check that the ~lit clauses have all beeen covered
-    // and clean up "marked_clause" markers
-    bool reverse_covered = true;
-    for(auto const& w2: solver->watches[~lit]) {
-        if (!w2.isClause()) continue;
-        Clause* cl2 = solver->cl_alloc.ptr(w2.get_offset());
-        if (cl2->getRemoved() || cl2->red()) continue;
-
-        if (!cl2->stats.marked_clause) {
-            reverse_covered = false;
-        }
-        cl2->stats.marked_clause = false;
-    }
-
-    if (ok && reverse_covered) {
-        elim_var_by_str(lit.var(), equiv_subformula_cls);
-        return true;
-    }
-    return false;
-}
-
 bool OccSimplifier::elim_var_by_str(uint32_t var, const vector<pair<ClOffset, ClOffset>>& cls)
 {
     Lit l(var, false);
 
     // Remove binaries, add units.
     solver->watches[l].copyTo(poss);
     for(auto const& w: poss) {
@@ -1902,15 +1794,15 @@
 
     solver->conf.maxOccurRedMB = backup;
     finishUp(origTrailSize);
     return ret;
 }
 
 void OccSimplifier::find_equiv_subformula(
-    vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars, bool mirror_empty)
+    vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars)
 {
     assert(solver->okay());
     assert(solver->prop_at_head());
     if (!setup()) return;
 
     auto origTrailSize = solver->trail_size();
     startup = false;
@@ -2613,17 +2505,15 @@
 
 bool OccSimplifier::ternary_res()
 {
     assert(solver->okay());
     assert(cl_to_add_ternary.empty());
     assert(solver->prop_at_head());
     assert(cl_to_free_later.empty());
-    if (clauses.empty()) {
-        return solver->okay();
-    }
+    if (clauses.empty()) return solver->okay();
 
     double myTime = cpuTime();
     int64_t orig_ternary_res_time_limit = ternary_res_time_limit;
     auto old_limit_to_decrease = limit_to_decrease;
     limit_to_decrease = &ternary_res_time_limit;
     Sub1Ret sub1_ret;
 
@@ -2683,14 +2573,15 @@
     return solver->okay();
 }
 
 bool OccSimplifier::perform_ternary(Clause* cl, ClOffset offs, Sub1Ret& sub1_ret)
 {
     assert(cl->size() == 3);
     assert(!cl->red());
+    assert(solver->okay());
 
     cl->is_ternary_resolved = 1;
     *limit_to_decrease -= 3;
     for(const Lit l: *cl) {
         seen[l.toInt()] = 1;
     }
 
@@ -2761,14 +2652,15 @@
             newCl->stats.extra_pos = solver->red_stats_extra.size()-1;
             #endif
             ClOffset off = solver->cl_alloc.get_offset(newCl);
             if (!sub_str->backw_sub_str_with_long(off, sub1_ret)) {
                 return false;
             }
         } else {
+            if (!solver->okay()) return false;
             //We'd need to check sub1_ret and see if it subsumed an irred
             // then fix it up. Can't be bothered.
 //             if (!sub_str->backw_sub_str_with_impl(finalLits_ternary, sub1_ret)) {
 //                 return false;
 //             }
         }
         *limit_to_decrease-=20;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/occsimplifier.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/occsimplifier.h`

 * *Files 0% similar despite different names*

```diff
@@ -45,15 +45,14 @@
 
 namespace CMSat {
 
 using std::vector;
 using std::map;
 using std::set;
 using std::pair;
-using std::priority_queue;
 
 class ClauseCleaner;
 class SolutionExtender;
 class Solver;
 class TopLevelGaussAbst;
 class SubsumeStrengthen;
 class BVA;
@@ -195,15 +194,15 @@
 
     //Called from main
     vector<OrGate> recover_or_gates();
     vector<ITEGate> recover_ite_gates();
 
     // definable vars
     vector<uint32_t> remove_definable_by_irreg_gate(const vector<uint32_t>& vars);
-    void find_equiv_subformula(vector<uint32_t>& empty_vars, vector<uint32_t>& sampl_vars, bool mirror_empty);
+    void find_equiv_subformula(vector<uint32_t>& empty_vars, vector<uint32_t>& sampl_vars);
     bool elim_var_by_str(uint32_t var, const vector<pair<ClOffset, ClOffset>>& cls);
     uint32_t add_cls_to_picosat_definable(const Lit wsLit);
     PicoSAT* picosat = NULL;
     int lit_to_picolit(const Lit l);
     uint32_t picolits_added = 0;
     vector<int> var_to_picovar;
     vector<uint32_t> picovars_used;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/oracle/bitset.hpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/oracle/bitset.hpp`

 * *Files 1% similar despite different names*

```diff
@@ -26,14 +26,15 @@
 #include <cstdlib>
 #include <vector>
 #include <cstring>
 #include <random>
 #include <limits>
 #include <cassert>
 #include <functional>
+#include "../cms_windows_includes.h"
 
 #define BITS 64
 
 namespace sspp {
 class Bitset {
  public:
   uint64_t* data_;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/oracle/oracle.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/oracle/oracle.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/oracle/oracle.hpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/oracle/oracle.hpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/oracle/utils.hpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/oracle/utils.hpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/packedmatrix.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/packedmatrix.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/packedrow.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/packedrow.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/packedrow.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/packedrow.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picogcnf.c` & `pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picogcnf.c`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picomcs.c` & `pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picomcs.c`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picomus.c` & `pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picomus.c`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picosat.c` & `pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picosat.c`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/picosat/picosat.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/picosat/picosat.h`

 * *Files 0% similar despite different names*

```diff
@@ -116,15 +116,15 @@
 /* Disable/Enable all pre-processing, currently only failed literal probing.
  *
  *  new_plain_value != 0    only 'plain' solving, so no preprocessing
  *  new_plain_value == 0    allow preprocessing
  */
 void picosat_set_plain (PicoSAT *, int new_plain_value);
 
-/* Set default initial phase: 
+/* Set default initial phase:
  *
  *   0 = false
  *   1 = true
  *   2 = Jeroslow-Wang (default)
  *   3 = random initial phase
  *
  * After a variable has been assigned the first time, it will always
@@ -149,15 +149,15 @@
  */
 void picosat_set_default_phase_lit (PicoSAT *, int lit, int phase);
 
 /* You can reset all phases by the following function.
  */
 void picosat_reset_phases (PicoSAT *);
 
-/* Scores can be erased as well.  Note, however, that even after erasing 
+/* Scores can be erased as well.  Note, however, that even after erasing
  * scores and phases, learned clauses are kept.  In addition head tail
  * pointers for literals are not moved either.  So expect a difference
  * between calling the solver in incremental mode or with a fresh copy of
  * the CNF.
  */
 void picosat_reset_scores (PicoSAT *);
 
@@ -190,15 +190,15 @@
 /* If you ever want to extract cores or proof traces with the current
  * instance of PicoSAT initialized with 'picosat_init', then make sure to
  * call 'picosat_enable_trace_generation' right after 'picosat_init'.   This
  * is not necessary if you only use 'picosat_set_incremental_rup_file'.
  *
  * NOTE, trace generation code is not necessarily included, e.g. if you
  * configure PicoSAT with full optimzation as './configure.sh -O' or with
- 
+
  * you do not get any results by trying to generate traces.
  *
  * The return value is non-zero if code for generating traces is included
  * and it is zero if traces can not be generated.
  */
 int picosat_enable_trace_generation (PicoSAT *);
 
@@ -255,15 +255,15 @@
  * generated by 'picosat_push'.
  */
 int picosat_failed_context (PicoSAT *, int lit);
 
 /* Returns the literal that assumes the current context or zero if the
  * outer context has been reached.
  */
-int picosat_context (PicoSAT *);	
+int picosat_context (PicoSAT *);
 
 /* Closes the current context and recycles the literal generated for
  * assuming this context.  The return value is the literal for the new
  * outer context or zero if the outer most context has been reached.
  */
 int picosat_pop (PicoSAT *);
 
@@ -326,39 +326,39 @@
 /* Print the CNF to the given file in DIMACS format.
  */
 void picosat_print (PicoSAT *, FILE *);
 
 /* You can add arbitrary many assumptions before the next 'picosat_sat'
  * call.  This is similar to the using assumptions in MiniSAT, except that
  * for PicoSAT you do not have to collect all your assumptions in a vector
- * yourself.  In PicoSAT you can add one after the other, to be used in the 
+ * yourself.  In PicoSAT you can add one after the other, to be used in the
  * next call to 'picosat_sat'.
  *
  * These assumptions can be interpreted as adding unit clauses with those
  * assumptions as literals.  However these assumption clauses are only valid
  * for exactly the next call to 'picosat_sat', and will be removed
  * afterwards, e.g. in following future calls to 'picosat_sat' after the
  * next 'picosat_sat' call, unless they are assumed again trough
  * 'picosat_assume'.
  *
  * More precisely, assumptions actually remain valid even after the next
  * call to 'picosat_sat' has returned.  Valid means they remain 'assumed'
  * internally until a call to 'picosat_add', 'picosat_assume', or a second
  * 'picosat_sat', following the first 'picosat_sat'.  The reason for keeping
  * them valid is to allow 'picosat_failed_assumption' to return correct
- * values.  
+ * values.
  *
  * Example:
  *
  *   picosat_assume (1);        // assume unit clause '1 0'
  *   picosat_assume (-2);       // additionally assume clause '-2 0'
  *   res = picosat_sat (1000);  // assumes 1 and -2 to hold
  *                              // 1000 decisions max.
  *
- *   if (res == PICOSAT_UNSATISFIABLE) 
+ *   if (res == PICOSAT_UNSATISFIABLE)
  *     {
  *       if (picosat_failed_assumption (1))
  *         // unit clause '1 0' was necessary to derive UNSAT
  *
  *       if (picosat_failed_assumption (-2))
  *         // unit clause '-2 0' was necessary to derive UNSAT
  *
@@ -543,15 +543,15 @@
  *
  * can be used to iterate over all maximal consistent subsets of
  * the set of assumptions {a1,a2,a3,a4}.
  *
  * It could be beneficial to set the default phase of assumptions
  * to true (positive).  This might speed up the computation.
  */
-const int * 
+const int *
 picosat_next_maximal_satisfiable_subset_of_assumptions (PicoSAT *);
 
 /* Similarly we can iterate over all minimal correcting assumption sets.
  * See the CAMUS literature [M. Liffiton, K. Sakallah JAR 2008].
  *
  * The result contains each assumed literal only once, even if it
  * was assumed multiple times (in contrast to the maximal consistent
@@ -588,15 +588,15 @@
 /* Assume that a previous call to 'picosat_sat' in incremental usage,
  * returned 'SATISFIABLE'.  Then a couple of clauses and optionally new
  * variables were added (a new variable is a variable that has an index
  * larger then the maximum variable added so far).  The next call to
  * 'picosat_sat' also returns 'SATISFIABLE'. If this function
  * 'picosat_changed' returns '0', then the assignment to the old variables
  * is guaranteed to not have changed.  Otherwise it might have changed.
- * 
+ *
  * The return value to this function is only valid until new clauses are
  * added through 'picosat_add', an assumption is made through
  * 'picosat_assume', or again 'picosat_sat' is called.  This is the same
  * assumption as for 'picosat_deref'.
  *
  * TODO currently this function might also return a non zero value even if
  * the old assignment did not change, because it only checks whether the
@@ -617,15 +617,15 @@
  * probably only work in non-incremental mode or without using
  * 'picosat_assume'.
  */
 
 /* This function determines whether the i'th added original clause is in the
  * core.  The 'i' is the return value of 'picosat_add', which starts at zero
  * and is incremented by one after a original clause is added (that is after
- * 'picosat_add (0)').  For the index 'i' the following has to hold: 
+ * 'picosat_add (0)').  For the index 'i' the following has to hold:
  *
  *   0 <= i < picosat_added_original_clauses ()
  */
 int picosat_coreclause (PicoSAT *, int i);
 
 /* This function gives access to the variable core, which is made up of the
  * variables that were resolved in deriving the empty clause.
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/popcnt.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/popcnt.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/predict_func_type.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/predict_func_type.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/propby.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/propby.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/propby_backup.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/propby_backup.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/propbyforgraph.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/propbyforgraph.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/propengine.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/propengine.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/propengine.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/propengine.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/reducedb.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/reducedb.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/reducedb.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/reducedb.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/satzilla_features.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/satzilla_features.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/satzilla_features_calc.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/satzilla_features_calc.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sccfinder.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/sccfinder.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sccfinder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/sccfinder.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/searcher.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/searcher.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/searcher.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/searcher.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/searchhist.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/searchhist.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/searchstats.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/searchstats.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/searchstats.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/searchstats.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/shareddata.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/shareddata.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/signalcode.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/signalcode.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/simplefile.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/simplefile.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sls.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/sls.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sls.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/sls.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solutionextender.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/solutionextender.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solutionextender.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/solutionextender.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solver.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/solver.cpp`

 * *Files 0% similar despite different names*

```diff
@@ -3728,14 +3728,15 @@
     return units;
 }
 
 vector<Xor> Solver::get_recovered_xors(const bool xor_together_xors)
 {
     vector<Xor> xors_ret;
     if (!okay()) return xors_ret;
+    if (!clear_gauss_matrices()) return xors_ret;
 
     lbool ret = execute_inprocess_strategy(false, "occ-xor");
     if (ret == l_False) return xors_ret;
 
     auto xors = xorclauses;
     xors.insert(xors.end(), xorclauses_unused.begin(), xorclauses_unused.end());
     if (xor_together_xors) {
@@ -4780,18 +4781,18 @@
 vector<uint32_t> Solver::remove_definable_by_irreg_gate(const vector<uint32_t>& vars)
 {
     if (!okay()) return vector<uint32_t>{};
     return occsimplifier->remove_definable_by_irreg_gate(vars);
 }
 
 void Solver::find_equiv_subformula(
-    vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars, const bool mirror_empty)
+    vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars)
 {
     if (!okay()) return;
-    return occsimplifier->find_equiv_subformula(sampl_vars, empty_vars, mirror_empty);
+    return occsimplifier->find_equiv_subformula(sampl_vars, empty_vars);
 }
 
 bool Solver::remove_and_clean_all() {
     return clauseCleaner->remove_and_clean_all();
 }
 
 void Solver::set_max_confl(uint64_t max_confl)
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solver.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/solver.h`

 * *Files 2% similar despite different names*

```diff
@@ -288,15 +288,15 @@
         // Gates
         vector<OrGate> get_recovered_or_gates();
         vector<ITEGate> get_recovered_ite_gates();
         vector<pair<Lit, Lit> > get_all_binary_xors() const;
         vector<Xor> get_recovered_xors(const bool xor_together_xors);
         vector<uint32_t> remove_definable_by_irreg_gate(const vector<uint32_t>& vars);
         void find_equiv_subformula(
-            vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars, const bool mirror_empty);
+            vector<uint32_t>& sampl_vars, vector<uint32_t>& empty_vars);
 
         bool remove_and_clean_all();
         vector<Lit> get_toplevel_units_internal(bool outer_numbering) const;
 
         // Gauss-Jordan
         bool init_all_matrices();
         void detach_xor_clauses(
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solverconf.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/solverconf.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solverconf.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/solverconf.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solvertypes.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/solvertypes.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/solvertypesmini.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/solvertypesmini.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sql_tablestructure.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/sql_tablestructure.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sqlitestats.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/sqlitestats.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/sqlstats.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/sqlstats.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/str_impl_w_impl.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/str_impl_w_impl.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/str_impl_w_impl.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/str_impl_w_impl.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/streambuffer.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/streambuffer.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/subsumeimplicit.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/subsumeimplicit.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/subsumeimplicit.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/subsumeimplicit.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/subsumestrengthen.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/subsumestrengthen.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/subsumestrengthen.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/subsumestrengthen.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/time_mem.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/time_mem.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/toplevelgauss.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/toplevelgauss.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/toplevelgaussabst.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/toplevelgaussabst.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/touchlist.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/touchlist.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/trim.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/trim.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/vardata.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/vardata.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/vardistgen.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/vardistgen.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/varreplacer.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/varreplacer.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/varreplacer.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/varreplacer.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/varupdatehelper.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/varupdatehelper.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/vmtf.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/vmtf.h`

 * *Files 2% similar despite different names*

```diff
@@ -18,14 +18,15 @@
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 ***********************************************/
 
 #ifndef VMTF_H
 
+#include <cstdint>
 #include <vector>
 #include <cstdint>
 #include "constants.h"
 using std::vector;
 
 namespace CMSat {
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/watchalgos.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/watchalgos.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/watcharray.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/watcharray.h`

 * *Files 1% similar despite different names*

```diff
@@ -22,14 +22,15 @@
 ***************************************************************/
 
 #ifndef __WATCHARRAY_H__
 #define __WATCHARRAY_H__
 
 #include "watched.h"
 #include "Vec.h"
+#include <cstdint>
 #include <vector>
 
 namespace CMSat {
 using std::vector;
 
 typedef vec<Watched>& watch_subarray;
 typedef const vec<Watched>& watch_subarray_const;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/watcharray_handrolled.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/watcharray_handrolled.h`

 * *Files 1% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 ***********************************************/
 
 #ifndef __WATCHARRAY_H__
 #define __WATCHARRAY_H__
 
+#include <cstdint>
 #include <stdlib.h>
 #include "watched.h"
 #include <vector>
 
 namespace CMSat {
 using std::vector;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/watched.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/watched.h`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,15 @@
 //#define DEBUG_WATCHED
 
 #include "clabstraction.h"
 #include "constants.h"
 #include "cloffset.h"
 #include "solvertypes.h"
 
+#include <cstdint>
 #include <limits>
 #include <string.h>
 
 
 namespace CMSat {
 
 enum class WatchType {
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/xor.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/xor.h`

 * *Files 3% similar despite different names*

```diff
@@ -21,14 +21,15 @@
 ***********************************************/
 
 #ifndef _XOR_H_
 #define _XOR_H_
 
 #include "solvertypes.h"
 
+#include <cstdint>
 #include <vector>
 #include <set>
 #include <iostream>
 #include <algorithm>
 #ifdef USE_TBUDDY
 #include <pseudoboolean.h>
 namespace tbdd = trustbdd;
```

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/xorfinder.cpp` & `pyapproxmc-4.1.9/python/cryptominisat/src/xorfinder.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/cryptominisat/src/xorfinder.h` & `pyapproxmc-4.1.9/python/cryptominisat/src/xorfinder.h`

 * *Files 1% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 ***********************************************/
 
 #ifndef _XORFINDER_H_
 #define _XORFINDER_H_
 
+#include <cstdint>
 #include <vector>
 #include <set>
 #include <iostream>
 #include <algorithm>
 #include <set>
 #include <limits>
 #include "constants.h"
```

### Comparing `pyapproxmc-4.1.8/python/src/GitSHA1.cpp` & `pyapproxmc-4.1.9/python/src/GitSHA1.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/python/src/pyapproxmc.cpp` & `pyapproxmc-4.1.9/python/src/pyapproxmc.cpp`

 * *Files 0% similar despite different names*

```diff
@@ -81,16 +81,16 @@
         return;
     }
 
     if (self->verbosity < 0) {
         PyErr_SetString(PyExc_ValueError, "verbosity must be at least 0");
         return;
     }
-    if (self->epsilon <= 0 || self->epsilon >= 1) {
-        PyErr_SetString(PyExc_ValueError, "epsilon must be greater or equal to 0, and less than 1");
+    if (self->epsilon <= 0) {
+        PyErr_SetString(PyExc_ValueError, "epsilon must be greater than 0");
         return;
     }
     if (self->delta < 0 || self->delta >= 1) {
         PyErr_SetString(PyExc_ValueError, "delta must be greater or equal to 0, and less than 1");
         return;
     }
```

### Comparing `pyapproxmc-4.1.8/setup.py` & `pyapproxmc-4.1.9/setup.py`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/src/GitSHA1.h` & `pyapproxmc-4.1.9/src/GitSHA1.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/src/approxmc.cpp` & `pyapproxmc-4.1.9/src/approxmc.cpp`

 * *Files 6% similar despite different names*

```diff
@@ -297,24 +297,14 @@
 
 
 DLL_PUBLIC const std::vector<uint32_t>& AppMC::get_sampling_set() const
 {
     return data->conf.sampling_set;
 }
 
-DLL_PUBLIC void AppMC::set_cont_recomp_indep_set(bool cont_recomp_indep_set)
-{
-    data->conf.cont_recomp_indep_set = cont_recomp_indep_set;
-}
-
-DLL_PUBLIC bool AppMC::get_cont_recomp_indep_set()
-{
-    return data->conf.cont_recomp_indep_set;
-}
-
 DLL_PUBLIC void AppMC::set_dump_intermediary_cnf(const bool dump_intermediary_cnf)
 {
     data->conf.dump_intermediary_cnf = dump_intermediary_cnf;
 }
 
 DLL_PUBLIC void AppMC::print_stats(const double start_time)
 {
```

### Comparing `pyapproxmc-4.1.8/src/approxmc.h` & `pyapproxmc-4.1.9/src/approxmc.h`

 * *Files 4% similar despite different names*

```diff
@@ -100,27 +100,25 @@
     void set_verb_cls(uint32_t verb_cls);
     void set_var_elim_ratio(double var_elim_ratio);
     void set_detach_xors(uint32_t detach_xors);
     void set_reuse_models(uint32_t reuse_models);
     void set_force_sol_extension(uint32_t force_sol_extension);
     void set_sparse(uint32_t sparse);
     void set_simplify(uint32_t simplify);
-    void set_cont_recomp_indep_set(bool cont_recomp_indep_set);
     void set_dump_intermediary_cnf(const bool dump_intermediary_cnf);
 
     //Querying default values
     const std::vector<uint32_t>& get_sampling_set() const;
     double get_epsilon();
     uint32_t get_seed();
     double get_delta();
     uint32_t get_simplify();
     double get_var_elim_ratio();
     uint32_t get_sparse();
     bool get_reuse_models();
-    bool get_cont_recomp_indep_set();
 
 private:
     ////////////////////////////
     // Do not bother with this, it's private
     ////////////////////////////
     AppMCPrivateData* data;
 };
```

### Comparing `pyapproxmc-4.1.8/src/config.h` & `pyapproxmc-4.1.9/src/config.h`

 * *Files 3% similar despite different names*

```diff
@@ -40,15 +40,14 @@
     double epsilon = 0.80; //Tolerance.  CAV-2020 paper default
     double delta = 0.2;    //Confidence. CAV-2020 paper default
     int sparse = 0;
     unsigned verb = 0;
     unsigned verb_cls = 0;
     uint32_t seed = 1;
     int simplify = 1;
-    int cont_recomp_indep_set = 0;
     double var_elim_ratio = 1.6;
     int reuse_models = 1;
     int force_sol_extension = 0;
     std::vector<uint32_t> sampling_set;
     std::string logfilename = "";
     int cms_detach_xor = 1;
     int dump_intermediary_cnf = 0;
```

### Comparing `pyapproxmc-4.1.8/src/constants.cpp` & `pyapproxmc-4.1.9/src/constants.cpp`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/src/constants.h` & `pyapproxmc-4.1.9/src/constants.h`

 * *Files identical despite different names*

### Comparing `pyapproxmc-4.1.8/src/counter.cpp` & `pyapproxmc-4.1.9/src/counter.cpp`

 * *Files 3% similar despite different names*

```diff
@@ -54,17 +54,15 @@
 #include <arjun/arjun.h>
 #endif
 
 #define verb_print(a, x) \
     do { if (conf.verb >= a) {std::cout << "c " << x << std::endl;} } while (0)
 
 using std::cout;
-using std::cerr;
 using std::endl;
-using std::list;
 using std::map;
 using namespace AppMCInt;
 
 Hash Counter::add_hash(uint32_t hash_index, SparseData& sparse_data)
 {
     const string randomBits =
         gen_rnd_bits(conf.sampling_set.size(), hash_index, sparse_data);
@@ -363,19 +361,16 @@
     solver->set_full_bve(1);
     solver->set_bva(1);
     solver->set_scc(1);
 
     solver->simplify();
 
     solver->set_sls(0);
-    //solver->set_intree_probe(0);
     solver->set_full_bve(0);
     solver->set_bva(0);
-    //solver->set_distill(0);
-    //solver->set_scc(0);
 }
 
 //Set up probabilities, threshold and measurements
 void Counter::set_up_probs_threshold_measurements(
     uint32_t& measurements, SparseData& sparse_data)
 {
     int best_match = -1;
@@ -430,59 +425,29 @@
     int64_t hashCount = conf.start_iter;
 
     SparseData sparse_data(-1);
     HashesModels hm;
     uint32_t measurements;
     set_up_probs_threshold_measurements(measurements, sparse_data);
 
-    verb_print(1, "[appmc] Starting up, initial measurement");
-    if (hashCount == 0) {
-        verb_print(1, "[appmc] Checking if there are at least threshold+1 solutions...");
-        double myTime = cpuTime();
-        if (conf.simplify >= 1) simplify();
-        const int64_t init_num_sols = bounded_sol_count(
-            threshold+1, //max solutions
-            NULL, // no assumptions
-            hashCount,
-            &hm
-        ).solutions;
-        verb_print(2, "[appmc] Initial number of solutions: " << init_num_sols);
-
-        write_log(false, //not sampling
-                  0, 0,
-                  init_num_sols == (threshold + 1),
-                  init_num_sols, 0, cpuTime() - myTime);
-
-        //Din't find at least threshold+1
-        if (init_num_sols <= threshold) {
-            if (conf.verb) {
-                cout << "c [appmc] Did not find at least threshold+1 ("
-                << threshold << ") we found only " << init_num_sols
-                << ", i.e. we got exact count" << endl;
-            }
-
-            ApproxMC::SolCount ret_count;
-            ret_count.valid = true;
-            ret_count.cellSolCount = init_num_sols;
-            ret_count.hashCount = 0;
-            return ret_count;
-        }
-        hashCount++;
-    }
     verb_print(1, "[appmc] Starting at hash count: " << hashCount);
 
     int64_t mPrev = hashCount;
     numHashList.clear();
     numCountList.clear();
 
     //See Algorithm 1 in paper "Algorithmic Improvements in Approximate Counting
     //for Probabilistic Inference: From Linear to Logarithmic SAT Calls"
     //https://www.ijcai.org/Proceedings/16/Papers/503.pdf
     for (uint32_t j = 0; j < measurements; j++) {
         one_measurement_count(mPrev, j, sparse_data, &hm);
+        if (mPrev == 0) {
+            // Exact count, no need to measure multiple times.
+            break;
+        }
         sparse_data.next_index = 0;
         if (conf.simplify >= 1 && j+1 < measurements) simplify();
         hm.clear();
     }
     assert(numHashList.size() > 0 && "UNSAT should not be possible");
 
     return calc_est_count();
@@ -528,69 +493,29 @@
         }
     }
 
     cout << "c [sparse] No match. Using default 0.5" << endl;
     return -1;
 }
 
-void Counter::cont_recomp_indep_set(const vector<Lit>& assumps)
-{
-    ArjunNS::Arjun arjun;
-    arjun.set_verbosity(0);
-    bool ret = true;
-    solver->start_getting_small_clauses(
-        std::numeric_limits<uint32_t>::max(),
-        std::numeric_limits<uint32_t>::max(),
-        false,
-        true);
-    vector<Lit> clause;
-    arjun.new_vars(solver->nVars());
-    while (ret) {
-        ret = solver->get_next_small_clause(clause);
-        if (!ret) {
-            break;
-        }
-
-        //Deal with variables that we never added but are used to blast XORs
-        //inside CMS. So, we actually can get variables back that we never added
-        for(const auto l: clause) {
-            if (l.var() >= arjun.nVars()) {
-                arjun.new_vars(1+l.var()-arjun.nVars());
-            }
-        }
-        arjun.add_clause(clause);
-
-    }
-
-    //Add assumptions
-    for(auto x: assumps) {
-        clause.clear();
-        clause.push_back(x);
-        arjun.add_clause(clause);
-    }
-    cout << "Arjun has more vars by: "
-    << (arjun.nVars() - solver->nVars()) << endl;
-
-    solver->end_getting_small_clauses();
-    arjun.set_starting_sampling_set(conf.sampling_set);
-    auto sampl_set = arjun.get_indep_set();
-    cout << "Arjun says new indep set size is: " << sampl_set.size()
-    << " -- gain: " << (conf.sampling_set.size()-sampl_set.size())
-    << endl;
-}
-
 //See Algorithm 2+3 in paper "Algorithmic Improvements in Approximate Counting
 //for Probabilistic Inference: From Linear to Logarithmic SAT Calls"
 //https://www.ijcai.org/Proceedings/16/Papers/503.pdf
 void Counter::one_measurement_count(
     int64_t& mPrev,
-    const int iter,
+    const unsigned iter,
     SparseData sparse_data,
     HashesModels* hm)
 {
+    if (conf.sampling_set.empty()) {
+        numHashList.push_back(0);
+        numCountList.push_back(1);
+        return;
+    }
+
     //Tells the number of solutions found at hash number N
     //sols_for_hash[N] tells the number of solutions found when N hashes were added
     map<uint64_t,int64_t> sols_for_hash;
 
     //threshold_sols[hash_num]==1 tells us that at hash_num number of hashes
     //there were found to be FULL threshold number of solutions
     //threshold_sols[hash_num]==0 tells that there were less than threshold
@@ -610,17 +535,14 @@
     //The key idea is that we first do an exponential search and then do binary search
     //This is implemented by using two sentinels: lowerFib and upperFib. The correct answer
     // is always between lowFib and upperFib. We do exponential search until upperFib < lowerFib/2
     // Once upperFib < lowerFib/2; we do a binary search.
     while (numExplored < total_max_xors) {
         uint64_t cur_hash_count = hashCount;
         const vector<Lit> assumps = set_num_hashes(hashCount, hm->hashes, sparse_data);
-        if (conf.cont_recomp_indep_set) {
-            cont_recomp_indep_set(assumps);
-        }
 
         if (conf.verb) {
             cout << "c [appmc] "
             "[ " << std::setw(7) << std::setprecision(2) << std::fixed
             << (cpuTimeTotal()-startTime)
             << " ]"
             << " round: " << std::setw(2) << iter
@@ -644,16 +566,17 @@
 
         if (num_sols < threshold + 1) {
             numExplored = lowerFib + total_max_xors - hashCount;
 
             //one less hash count had threshold solutions
             //this one has less than threshold
             //so this is the real deal!
-            if (threshold_sols.find(hashCount-1) != threshold_sols.end()
-                && threshold_sols[hashCount-1] == 1
+            if (hashCount == 0 ||
+                    (threshold_sols.find(hashCount-1) != threshold_sols.end()
+                    && threshold_sols[hashCount-1] == 1)
             ) {
                 numHashList.push_back(hashCount);
                 numCountList.push_back(num_sols);
                 mPrev = hashCount;
                 return;
             }
 
@@ -698,21 +621,23 @@
                 && std::abs(hashCount - mPrev) < 2
             ) {
                 //Doing linear, this is a re-count
                 lowerFib = hashCount;
                 hashCount++;
             } else if (lowerFib + (hashCount-lowerFib)*2 >= upperFib-1) {
 
-                // Whenever the above condition is satisfied, we are in binary sesarch mode
+                // Whenever the above condition is satisfied, we are in binary search mode
                 lowerFib = hashCount;
                 hashCount = (lowerFib+upperFib)/2;
             } else {
 
                 // We are in exponential search mode.
+                auto old_hashCount = hashCount;
                 hashCount = lowerFib + (hashCount-lowerFib)*2;
+                if (old_hashCount == hashCount) hashCount++;
             }
         }
         hashPrev = cur_hash_count;
     }
 }
 bool Counter::gen_rhs()
 {
@@ -875,22 +800,20 @@
     const HashesModels* const hm,
     const uint32_t hashCount
 )
 {
     for(uint32_t var: conf.sampling_set) assert(model[var] != l_Undef);
     if (!hm) return;
 
-    uint32_t checked = 0;
     for(const auto& h: hm->hashes) {
         //This hash is number: h.first
         //Only has to match hashes at & below
         //Notice that "h.first" is numbered from 0, so it's a "<" not "<="
         if (h.first < hashCount) {
             //cout << "Checking model against hash " << h.first << endl;
-            checked++;
             assert(check_model_against_hash(h.second, model));
         }
     }
 }
 
 bool Counter::check_model_against_hash(const Hash& h, const vector<lbool>& model)
 {
```

### Comparing `pyapproxmc-4.1.8/src/counter.h` & `pyapproxmc-4.1.9/src/counter.h`

 * *Files 1% similar despite different names*

```diff
@@ -38,16 +38,14 @@
 #include <mutex>
 #include "approxmc.h"
 #include "constants.h"
 
 using std::string;
 using std::vector;
 using std::map;
-using std::cout;
-using std::endl;
 using namespace CMSat;
 
 namespace AppMCInt {
 
 struct SavedModel
 {
     SavedModel(uint32_t _hash_num, const vector<lbool>& _model) :
@@ -137,24 +135,23 @@
     );
     vector<Lit> set_num_hashes(
         uint32_t num_wanted,
         map<uint64_t, Hash>& hashes,
         SparseData& sparse_data
     );
     void simplify();
-    void cont_recomp_indep_set(const vector<Lit>& assumps);
 
     ////////////////
     //Helper functions
     ////////////////
     void dump_cnf_from_solver(const vector<Lit>& assumps);
     void print_xor(const vector<uint32_t>& vars, const uint32_t rhs);
     void one_measurement_count(
         int64_t& mPrev,
-        const int iter,
+        const unsigned iter,
         SparseData sparse_data,
         HashesModels* hm
     );
     void write_log(
         bool sampling,
         int iter,
         uint32_t hashCount,
```

### Comparing `pyapproxmc-4.1.8/src/pyapproxmc.egg-info/PKG-INFO` & `pyapproxmc-4.1.9/src/pyapproxmc.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyapproxmc
-Version: 4.1.8
+Version: 4.1.9
 Summary: Bindings to ApproxMC, an approximate model counter
 Home-page: https://github.com/meelgroup/approxmc
 Author-email: Mate Soos <soos.mate@gmail.com>
 Maintainer-email: Mate Soos <soos.mate@gmail.com>
 License: MIT License
         
         Copyright (c) 2018 Meel Group
@@ -42,58 +42,58 @@
 Classifier: Topic :: Utilities
 Requires-Python: >=3.5
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # pyapproxmc: bindings to the ApproxMC model counter
 
-This directory provides Python bindings to CryptoMiniSat on the C++ level,
-i.e. when importing pycryptosat, the CryptoMiniSat solver becomes part of the
+This directory provides Python bindings to ApproxMC on the C++ level,
+i.e. when importing pyapproxmc, the ApproxMC counter becomes part of the
 Python process itself.
 
-## Compiling
-The pyapproxmc python package compiles separately from ApproxMC, the binary.
 
-In order to compile, install the python developer tools:
+## Installing
 
 ```
-apt-get install python-dev
+pip install pyapproxmc
 ```
 
-Then:
+## Compiling
+If you don't want to use the pip package, you can compile it:
 
 ```
+apt-get install python-dev
 cd python
 git clone https://github.com/msoos/cryptominisat
 git clone https://github.com/meelgroup/arjun
 cd ..
 python -m build
 
 You will then find the files under "dist/".
 ```
 
 ## Usage
 
-The ``pyapproxmc`` module has one object, ``Counter`` that has two functions
-``count`` and ``add_clause``.
+The `pyapproxmc` module has one object, `Counter` that has two functions
+`count` and `add_clause`.
 
-The funcion ``add_clause()`` takes an iterable list of literals such as
+The function ``add_clause()`` takes an iterable list of literals such as
 ``[1, 2]`` which represents the truth ``1 or 2 = True``. For example,
 ``add_clause([1])`` sets variable ``1`` to ``True``.
 
-The function ``count()`` solves the system of equations that have been added
-with ``add_clause()``:
+The function `count()` counts the number of solutions to the system of constraints
+that have been added with `add_clause()`:
 
 ```
-   >>> from pyapproxmc import Counter
-   >>> s = Counter()
-   >>> s.add_clause([1, 2])
-   >>> cells, hashes = s.count()
-   >>> print "There are ", cells*2**hashes, " solutions, approximately"
-   There are 55 solutions, approximately
+>>> from pyapproxmc import Counter
+>>> s = Counter()
+>>> s.add_clause([1, 2])
+>>> cells, hashes = s.count()
+>>> print("There are approx ", cells*2**hashes, " solutions")
+There are 55 solutions, approximately
 ```
 
 The return value is a tuple of cells and hashes. Which gives how many solutions
 there are, probabilistically approximately
 
 You can give the following arguments to `Counter`:
 * `seed` -- sets the random seed
```

### Comparing `pyapproxmc-4.1.8/src/pyapproxmc.egg-info/SOURCES.txt` & `pyapproxmc-4.1.9/src/pyapproxmc.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 LICENSE
 README.md
 pyproject.toml
 setup.cfg
 setup.py
+python/README.md
 python/arjun/python/src/GitSHA1.cpp
 python/arjun/src/GitSHA1.h
 python/arjun/src/MersenneTwister.h
 python/arjun/src/arjun.cpp
 python/arjun/src/arjun.h
 python/arjun/src/backward.cpp
 python/arjun/src/common.cpp
```

### Comparing `pyapproxmc-4.1.8/src/time_mem.h` & `pyapproxmc-4.1.9/src/time_mem.h`

 * *Files identical despite different names*

