# Comparing `tmp/aeroot-0.3.7.tar.gz` & `tmp/aeroot-0.3.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aeroot-0.3.7.tar", last modified: Sat May  6 14:34:29 2023, max compression
+gzip compressed data, was "aeroot-0.3.8.tar", last modified: Fri May 12 23:59:03 2023, max compression
```

## Comparing `aeroot-0.3.7.tar` & `aeroot-0.3.8.tar`

### file list

```diff
@@ -1,64 +1,65 @@
-drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-06 14:34:29.975760 aeroot-0.3.7/
--rw-rw-r--   0 eric      (1000) eric      (1000)    11340 2023-03-26 13:18:16.000000 aeroot-0.3.7/LICENSE.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)       77 2023-03-26 13:18:16.000000 aeroot-0.3.7/MANIFEST.in
--rw-rw-r--   0 eric      (1000) eric      (1000)     7264 2023-05-06 14:34:29.975760 aeroot-0.3.7/PKG-INFO
--rw-rw-r--   0 eric      (1000) eric      (1000)     6859 2023-05-06 14:28:24.000000 aeroot-0.3.7/README.md
-drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-06 14:34:29.971759 aeroot-0.3.7/aeroot/
--rw-rw-r--   0 eric      (1000) eric      (1000)       45 2023-05-06 14:33:04.000000 aeroot-0.3.7/aeroot/__init__.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     1238 2023-03-26 13:18:16.000000 aeroot-0.3.7/aeroot/aeroot.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     8051 2023-05-06 14:28:24.000000 aeroot-0.3.7/aeroot/avd.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     2442 2023-03-26 13:18:16.000000 aeroot-0.3.7/aeroot/cli.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     1516 2023-03-26 13:18:16.000000 aeroot-0.3.7/aeroot/emulator.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     5442 2023-03-26 13:18:16.000000 aeroot-0.3.7/aeroot/gdb.py
--rw-rw-r--   0 eric      (1000) eric      (1000)     1745 2023-03-26 13:18:16.000000 aeroot-0.3.7/aeroot/util.py
-drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-06 14:34:29.971759 aeroot-0.3.7/aeroot.egg-info/
--rw-rw-r--   0 eric      (1000) eric      (1000)     7264 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/PKG-INFO
--rw-rw-r--   0 eric      (1000) eric      (1000)     2860 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/SOURCES.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)        1 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/dependency_links.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)       43 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/entry_points.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)       49 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/requires.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)       14 2023-05-06 14:34:29.000000 aeroot-0.3.7/aeroot.egg-info/top_level.txt
-drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-06 14:34:29.967759 aeroot-0.3.7/config/
-drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-06 14:34:29.975760 aeroot-0.3.7/config/kernel/
--rw-rw-r--   0 eric      (1000) eric      (1000)      255 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/3.10.0+_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      259 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/3.18.56+_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      259 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/3.18.91+_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      286 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/4.14.112+_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      288 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/4.14.112+_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      285 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/4.4.124+_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      287 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/4.4.124+_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.102-android13-0-00549-g255b30f804ac-ab8238117_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      329 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.102-android13-0-00549-g255b30f804ac-ab8238117_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      336 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.107-android13-2-00451-g7ba447d0399b-ab8409457_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.15-android12-0-01814-gfca78df78ef2-ab7137072_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.21-android12-0-01012-gcc574f0d3698-ab7214561_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.21-android12-0-01145-ge82381ad9a3f-ab7230153_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.35-android12-4-00865-gd9d0c09e0a3b-ab7349034_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.4-android12-0-03442-gf2684370d34d-ab7068937_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.43-android12-6-00231-g54e7412d4ff9-ab7460289_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.43-android12-9-00001-ga30f38980440-ab7882141_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      326 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.66-android12-9-00022-g2d6a43c0364d-ab7992900_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.10.66-android12-9-00041-gfa9c9074531e-ab7914766_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.15.32-android13-3-00067-g7b5e736d7c63-ab8474665_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.15.41-android13-6-02245-g158384f20d1e-ab8610100_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.15.41-android13-8-00055-g4f5025129fe8-ab8949913_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.15.41-android13-8-00205-gf1bf82c3dacd-ab8747247_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.15.83-android14-5-00138-g5e28b848962c-ab9412825_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.36-00815-g3b29042c17b1_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.36-00815-g3b29042c17b1_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.43-00621-g90087296b3b1_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.43-00621-g90087296b3b1_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.47-01061-g22e35a1de440_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.47-01061-g22e35a1de440_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.54-android11-0-00619-g476c942d9b3e-ab6722723_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.54-android11-0-00619-g476c942d9b3e-ab6722723_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.61-android11-2-00064-g4271ad6e8ade-ab6991359_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.86-android11-2-00006-gae78026f427c-ab7595864_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_i686.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.7/config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-05-06 14:28:24.000000 aeroot-0.3.7/config/kernel/6.1.12-android14-0-00356-g116e1532b95d-ab9618665_x86_64.yaml
--rw-rw-r--   0 eric      (1000) eric      (1000)       49 2023-03-26 13:18:16.000000 aeroot-0.3.7/requirements.txt
--rw-rw-r--   0 eric      (1000) eric      (1000)       38 2023-05-06 14:34:29.975760 aeroot-0.3.7/setup.cfg
--rw-rw-r--   0 eric      (1000) eric      (1000)     1119 2023-03-26 13:18:16.000000 aeroot-0.3.7/setup.py
+drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-12 23:59:03.746709 aeroot-0.3.8/
+-rw-rw-r--   0 eric      (1000) eric      (1000)    11340 2023-03-26 13:18:16.000000 aeroot-0.3.8/LICENSE.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)       77 2023-03-26 13:18:16.000000 aeroot-0.3.8/MANIFEST.in
+-rw-rw-r--   0 eric      (1000) eric      (1000)     7370 2023-05-12 23:59:03.746709 aeroot-0.3.8/PKG-INFO
+-rw-rw-r--   0 eric      (1000) eric      (1000)     6965 2023-05-12 23:58:36.000000 aeroot-0.3.8/README.md
+drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-12 23:59:03.738709 aeroot-0.3.8/aeroot/
+-rw-rw-r--   0 eric      (1000) eric      (1000)       45 2023-05-12 23:58:36.000000 aeroot-0.3.8/aeroot/__init__.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     1238 2023-03-26 13:18:16.000000 aeroot-0.3.8/aeroot/aeroot.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     8051 2023-05-06 14:28:24.000000 aeroot-0.3.8/aeroot/avd.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     2442 2023-03-26 13:18:16.000000 aeroot-0.3.8/aeroot/cli.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     1516 2023-03-26 13:18:16.000000 aeroot-0.3.8/aeroot/emulator.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     5442 2023-03-26 13:18:16.000000 aeroot-0.3.8/aeroot/gdb.py
+-rw-rw-r--   0 eric      (1000) eric      (1000)     1745 2023-03-26 13:18:16.000000 aeroot-0.3.8/aeroot/util.py
+drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-12 23:59:03.738709 aeroot-0.3.8/aeroot.egg-info/
+-rw-rw-r--   0 eric      (1000) eric      (1000)     7370 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/PKG-INFO
+-rw-rw-r--   0 eric      (1000) eric      (1000)     2935 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/SOURCES.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)        1 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/dependency_links.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)       43 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/entry_points.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)       49 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/requires.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)       14 2023-05-12 23:59:03.000000 aeroot-0.3.8/aeroot.egg-info/top_level.txt
+drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-12 23:59:03.734709 aeroot-0.3.8/config/
+drwxrwxr-x   0 eric      (1000) eric      (1000)        0 2023-05-12 23:59:03.742709 aeroot-0.3.8/config/kernel/
+-rw-rw-r--   0 eric      (1000) eric      (1000)      255 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/3.10.0+_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      259 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/3.18.56+_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      259 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/3.18.91+_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      286 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/4.14.112+_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      288 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/4.14.112+_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      285 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/4.4.124+_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      287 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/4.4.124+_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.102-android13-0-00549-g255b30f804ac-ab8238117_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      329 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.102-android13-0-00549-g255b30f804ac-ab8238117_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      336 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.107-android13-2-00451-g7ba447d0399b-ab8409457_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.15-android12-0-01814-gfca78df78ef2-ab7137072_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.21-android12-0-01012-gcc574f0d3698-ab7214561_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.21-android12-0-01145-ge82381ad9a3f-ab7230153_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.35-android12-4-00865-gd9d0c09e0a3b-ab7349034_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.4-android12-0-03442-gf2684370d34d-ab7068937_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.43-android12-6-00231-g54e7412d4ff9-ab7460289_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.43-android12-9-00001-ga30f38980440-ab7882141_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      326 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.66-android12-9-00022-g2d6a43c0364d-ab7992900_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.10.66-android12-9-00041-gfa9c9074531e-ab7914766_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.15.32-android13-3-00067-g7b5e736d7c63-ab8474665_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.15.41-android13-6-02245-g158384f20d1e-ab8610100_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.15.41-android13-8-00055-g4f5025129fe8-ab8949913_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.15.41-android13-8-00205-gf1bf82c3dacd-ab8747247_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      328 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.15.83-android14-5-00138-g5e28b848962c-ab9412825_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.36-00815-g3b29042c17b1_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.36-00815-g3b29042c17b1_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.43-00621-g90087296b3b1_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.43-00621-g90087296b3b1_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      303 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.47-01061-g22e35a1de440_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      305 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.47-01061-g22e35a1de440_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.54-android11-0-00619-g476c942d9b3e-ab6722723_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.54-android11-0-00619-g476c942d9b3e-ab6722723_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.61-android11-2-00064-g4271ad6e8ade-ab6991359_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.86-android11-2-00006-gae78026f427c-ab7595864_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      325 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_i686.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-03-26 13:18:16.000000 aeroot-0.3.8/config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-05-06 14:28:24.000000 aeroot-0.3.8/config/kernel/6.1.12-android14-0-00356-g116e1532b95d-ab9618665_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)      327 2023-05-12 23:58:36.000000 aeroot-0.3.8/config/kernel/6.1.21-android14-3-01811-g9e35a21ec03f-ab9850788_x86_64.yaml
+-rw-rw-r--   0 eric      (1000) eric      (1000)       49 2023-03-26 13:18:16.000000 aeroot-0.3.8/requirements.txt
+-rw-rw-r--   0 eric      (1000) eric      (1000)       38 2023-05-12 23:59:03.746709 aeroot-0.3.8/setup.cfg
+-rw-rw-r--   0 eric      (1000) eric      (1000)     1119 2023-03-26 13:18:16.000000 aeroot-0.3.8/setup.py
```

### Comparing `aeroot-0.3.7/LICENSE.txt` & `aeroot-0.3.8/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/PKG-INFO` & `aeroot-0.3.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aeroot
-Version: 0.3.7
+Version: 0.3.8
 Summary: Android Emulator Rooting system
 Home-page: https://github.com/quarkslab/AERoot
 Author: Eric Le Guevel (ha0)
 Author-email: eleguevel@quarkslab.com
 License: Apache License 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Security
@@ -56,14 +56,15 @@
 | 5.10.107-android13-2-00451-g7ba447d0399b-ab8409457 |        | ✓      | 13.0                         |
 | 5.15.32-android13-3-00067-g7b5e736d7c63-ab8474665  |        | ✓      | 13.0                         |
 | 5.15.41-android13-6-02245-g158384f20d1e-ab8610100  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00205-gf1bf82c3dacd-ab8747247  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00055-g4f5025129fe8-ab8949913  |        | ✓      | 13.0                         |
 | 5.15.83-android14-5-00138-g5e28b848962c-ab9412825  |        | ✓      | 14.0                         |
 | 6.1.12-android14-0-00356-g116e1532b95d-ab9618665   |        | ✓      | 14.0                         |
+| 6.1.21-android14-3-01811-g9e35a21ec03f-ab9850788   |        | ✓      | 14.0                         |
 
 # Requirements
 
 AERoot requires [gdb](https://www.gnu.org/software/gdb/) (with Python support enabled) to run properly.
 
 # Installation
```

### Comparing `aeroot-0.3.7/README.md` & `aeroot-0.3.8/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -42,14 +42,15 @@
 | 5.10.107-android13-2-00451-g7ba447d0399b-ab8409457 |        | ✓      | 13.0                         |
 | 5.15.32-android13-3-00067-g7b5e736d7c63-ab8474665  |        | ✓      | 13.0                         |
 | 5.15.41-android13-6-02245-g158384f20d1e-ab8610100  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00205-gf1bf82c3dacd-ab8747247  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00055-g4f5025129fe8-ab8949913  |        | ✓      | 13.0                         |
 | 5.15.83-android14-5-00138-g5e28b848962c-ab9412825  |        | ✓      | 14.0                         |
 | 6.1.12-android14-0-00356-g116e1532b95d-ab9618665   |        | ✓      | 14.0                         |
+| 6.1.21-android14-3-01811-g9e35a21ec03f-ab9850788   |        | ✓      | 14.0                         |
 
 # Requirements
 
 AERoot requires [gdb](https://www.gnu.org/software/gdb/) (with Python support enabled) to run properly.
 
 # Installation
```

### Comparing `aeroot-0.3.7/aeroot/aeroot.py` & `aeroot-0.3.8/aeroot/aeroot.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot/avd.py` & `aeroot-0.3.8/aeroot/avd.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot/cli.py` & `aeroot-0.3.8/aeroot/cli.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot/emulator.py` & `aeroot-0.3.8/aeroot/emulator.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot/gdb.py` & `aeroot-0.3.8/aeroot/gdb.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot/util.py` & `aeroot-0.3.8/aeroot/util.py`

 * *Files identical despite different names*

### Comparing `aeroot-0.3.7/aeroot.egg-info/PKG-INFO` & `aeroot-0.3.8/aeroot.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aeroot
-Version: 0.3.7
+Version: 0.3.8
 Summary: Android Emulator Rooting system
 Home-page: https://github.com/quarkslab/AERoot
 Author: Eric Le Guevel (ha0)
 Author-email: eleguevel@quarkslab.com
 License: Apache License 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Security
@@ -56,14 +56,15 @@
 | 5.10.107-android13-2-00451-g7ba447d0399b-ab8409457 |        | ✓      | 13.0                         |
 | 5.15.32-android13-3-00067-g7b5e736d7c63-ab8474665  |        | ✓      | 13.0                         |
 | 5.15.41-android13-6-02245-g158384f20d1e-ab8610100  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00205-gf1bf82c3dacd-ab8747247  |        | ✓      | 13.0                         |
 | 5.15.41-android13-8-00055-g4f5025129fe8-ab8949913  |        | ✓      | 13.0                         |
 | 5.15.83-android14-5-00138-g5e28b848962c-ab9412825  |        | ✓      | 14.0                         |
 | 6.1.12-android14-0-00356-g116e1532b95d-ab9618665   |        | ✓      | 14.0                         |
+| 6.1.21-android14-3-01811-g9e35a21ec03f-ab9850788   |        | ✓      | 14.0                         |
 
 # Requirements
 
 AERoot requires [gdb](https://www.gnu.org/software/gdb/) (with Python support enabled) to run properly.
 
 # Installation
```

### Comparing `aeroot-0.3.7/aeroot.egg-info/SOURCES.txt` & `aeroot-0.3.8/aeroot.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -50,8 +50,9 @@
 config/kernel/5.4.54-android11-0-00619-g476c942d9b3e-ab6722723_x86_64.yaml
 config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_i686.yaml
 config/kernel/5.4.61-android11-0-00791-gbad091cc4bf3-ab6833933_x86_64.yaml
 config/kernel/5.4.61-android11-2-00064-g4271ad6e8ade-ab6991359_x86_64.yaml
 config/kernel/5.4.86-android11-2-00006-gae78026f427c-ab7595864_x86_64.yaml
 config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_i686.yaml
 config/kernel/5.4.86-android11-2-00040-g29b2beadc627-ab7157994_x86_64.yaml
-config/kernel/6.1.12-android14-0-00356-g116e1532b95d-ab9618665_x86_64.yaml
+config/kernel/6.1.12-android14-0-00356-g116e1532b95d-ab9618665_x86_64.yaml
+config/kernel/6.1.21-android14-3-01811-g9e35a21ec03f-ab9850788_x86_64.yaml
```

### Comparing `aeroot-0.3.7/setup.py` & `aeroot-0.3.8/setup.py`

 * *Files identical despite different names*

