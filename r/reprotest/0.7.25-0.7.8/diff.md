# Comparing `tmp/reprotest-0.7.25.tar.gz` & `tmp/reprotest-0.7.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reprotest-0.7.25.tar", last modified: Sat May 13 13:43:19 2023, max compression
+gzip compressed data, was "dist/reprotest-0.7.8.tar", last modified: Mon Jul  9 13:37:47 2018, max compression
```

## Comparing `reprotest-0.7.25.tar` & `reprotest-0.7.8.tar`

### file list

```diff
@@ -1,42 +1,77 @@
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.710000 reprotest-0.7.25/
--rw-r--r--   0 user      (1000) user      (1000)       44 2017-01-24 21:21:51.000000 reprotest-0.7.25/MANIFEST.in
--rw-r--r--   0 user      (1000) user      (1000)    18805 2023-05-13 13:43:19.710000 reprotest-0.7.25/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)    18115 2023-02-20 10:43:25.000000 reprotest-0.7.25/README.rst
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.708000 reprotest-0.7.25/reprotest/
--rw-r--r--   0 user      (1000) user      (1000)    40919 2023-02-18 12:32:10.000000 reprotest-0.7.25/reprotest/__init__.py
--rw-r--r--   0 user      (1000) user      (1000)      201 2016-11-29 09:55:34.000000 reprotest-0.7.25/reprotest/__main__.py
--rw-r--r--   0 user      (1000) user      (1000)    29009 2023-02-20 10:39:28.000000 reprotest-0.7.25/reprotest/build.py
--rw-r--r--   0 user      (1000) user      (1000)     4400 2017-12-15 15:32:40.000000 reprotest-0.7.25/reprotest/environ.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.709000 reprotest-0.7.25/reprotest/lib/
--rw-r--r--   0 user      (1000) user      (1000)    22344 2017-12-15 15:32:40.000000 reprotest-0.7.25/reprotest/lib/VirtSubproc.py
--rw-r--r--   0 user      (1000) user      (1000)        0 2016-07-30 05:59:38.000000 reprotest-0.7.25/reprotest/lib/__init__.py
--rw-r--r--   0 user      (1000) user      (1000)    59401 2021-01-20 13:14:58.000000 reprotest-0.7.25/reprotest/lib/adt_testbed.py
--rw-r--r--   0 user      (1000) user      (1000)     3072 2016-11-29 09:55:34.000000 reprotest-0.7.25/reprotest/lib/adtlog.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.710000 reprotest-0.7.25/reprotest/lib/system_interface/
--rw-r--r--   0 user      (1000) user      (1000)     1357 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/lib/system_interface/__init__.py
--rw-r--r--   0 user      (1000) user      (1000)     1757 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/lib/system_interface/arch.py
--rw-r--r--   0 user      (1000) user      (1000)     1829 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/lib/system_interface/debian.py
--rw-r--r--   0 user      (1000) user      (1000)      607 2019-09-15 13:45:34.000000 reprotest-0.7.25/reprotest/lib/system_interface/fedora.py
--rw-r--r--   0 user      (1000) user      (1000)     1484 2020-02-08 13:55:16.000000 reprotest-0.7.25/reprotest/lib/system_interface/guix.py
--rw-r--r--   0 user      (1000) user      (1000)     7474 2019-09-15 13:45:34.000000 reprotest-0.7.25/reprotest/mdiffconf.py
--rw-r--r--   0 user      (1000) user      (1000)     6217 2022-09-05 00:20:41.000000 reprotest-0.7.25/reprotest/presets.py
--rw-r--r--   0 user      (1000) user      (1000)     5385 2017-12-15 15:32:40.000000 reprotest-0.7.25/reprotest/shell_syn.py
--rw-r--r--   0 user      (1000) user      (1000)     1373 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/utils.py
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.710000 reprotest-0.7.25/reprotest/virt/
--rwxr-xr-x   0 user      (1000) user      (1000)     2571 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-chroot
--rwxr-xr-x   0 user      (1000) user      (1000)    13114 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-lxc
--rwxr-xr-x   0 user      (1000) user      (1000)     8558 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-lxd
--rwxr-xr-x   0 user      (1000) user      (1000)     2148 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-null
--rwxr-xr-x   0 user      (1000) user      (1000)    23097 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-qemu
--rwxr-xr-x   0 user      (1000) user      (1000)     5929 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-schroot
--rwxr-xr-x   0 user      (1000) user      (1000)    18407 2017-09-30 07:39:30.000000 reprotest-0.7.25/reprotest/virt/autopkgtest-virt-ssh
-drwxr-xr-x   0 user      (1000) user      (1000)        0 2023-05-13 13:43:19.709000 reprotest-0.7.25/reprotest.egg-info/
--rw-r--r--   0 user      (1000) user      (1000)    18805 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1000)     1015 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1000)       45 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/entry_points.txt
--rw-r--r--   0 user      (1000) user      (1000)        1 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/not-zip-safe
--rw-r--r--   0 user      (1000) user      (1000)       39 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1000)       10 2023-05-13 13:43:19.000000 reprotest-0.7.25/reprotest.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1000)       80 2023-05-13 13:43:19.711000 reprotest-0.7.25/setup.cfg
--rw-r--r--   0 user      (1000) user      (1000)     1362 2023-05-12 13:02:17.000000 reprotest-0.7.25/setup.py
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       96 2017-02-14 08:52:29.000000 reprotest-0.7.8/.coveragerc
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     2677 2018-07-09 12:55:18.000000 reprotest-0.7.8/README-dev.rst
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/tests/
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     3090 2017-12-18 21:32:58.000000 reprotest-0.7.8/tests/mock_build.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     6076 2017-12-18 21:32:58.000000 reprotest-0.7.8/tests/test_reprotest.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1229 2017-12-18 21:32:58.000000 reprotest-0.7.8/tests/test_shell.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      843 2017-12-18 21:32:58.000000 reprotest-0.7.8/tests/test_mdiffconf.py
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)      175 2017-02-14 08:52:29.000000 reprotest-0.7.8/tests/mock_failure.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    16909 2017-12-18 21:32:58.000000 reprotest-0.7.8/README.rst
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest/
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest/virt/
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     2148 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-null
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     5929 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-schroot
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     8558 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-lxd
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)    13114 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-lxc
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)    18407 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-ssh
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     2571 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-chroot
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)    23097 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/virt/autopkgtest-virt-qemu
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1373 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/utils.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    39814 2018-07-09 13:11:23.000000 reprotest-0.7.8/reprotest/__init__.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      201 2017-02-14 08:52:29.000000 reprotest-0.7.8/reprotest/__main__.py
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest/lib/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     3072 2017-02-14 08:52:29.000000 reprotest-0.7.8/reprotest/lib/adtlog.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)        0 2017-02-14 08:52:29.000000 reprotest-0.7.8/reprotest/lib/__init__.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    59035 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/lib/adt_testbed.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    22344 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/lib/VirtSubproc.py
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest/lib/system_interface/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1357 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/lib/system_interface/__init__.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1757 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/lib/system_interface/arch.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1829 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/lib/system_interface/debian.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     5385 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/shell_syn.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     7474 2018-07-09 13:11:37.000000 reprotest-0.7.8/reprotest/mdiffconf.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     4663 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/presets.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    25908 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/build.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     4400 2017-12-18 21:32:58.000000 reprotest-0.7.8/reprotest/environ.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      101 2017-12-18 21:32:58.000000 reprotest-0.7.8/.gitignore
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/debian/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1851 2018-07-09 13:16:00.000000 reprotest-0.7.8/debian/control
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/debian/tests/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      257 2018-07-09 13:07:44.000000 reprotest-0.7.8/debian/tests/control
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      351 2017-12-18 21:32:58.000000 reprotest-0.7.8/debian/NEWS
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/debian/upstream/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    15042 2017-07-12 12:50:47.000000 reprotest-0.7.8/debian/upstream/signing-key.asc
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      285 2017-12-18 21:32:58.000000 reprotest-0.7.8/debian/TODO
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     1031 2017-12-18 21:32:58.000000 reprotest-0.7.8/debian/import-autopkgtest.sh
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     9487 2018-07-09 13:34:11.000000 reprotest-0.7.8/debian/changelog
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       40 2017-02-14 08:52:29.000000 reprotest-0.7.8/debian/gbp.conf
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     2122 2018-06-03 13:54:53.000000 reprotest-0.7.8/debian/copyright
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)     1626 2018-07-09 13:12:53.000000 reprotest-0.7.8/debian/rules
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       11 2017-02-14 08:52:29.000000 reprotest-0.7.8/debian/reprotest.docs
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       46 2017-02-14 08:52:29.000000 reprotest-0.7.8/debian/clean
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/debian/source/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      137 2017-02-14 08:52:55.000000 reprotest-0.7.8/debian/source/lintian-overrides
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       13 2017-02-14 08:52:29.000000 reprotest-0.7.8/debian/source/format
+-rw-r--r--   0 mattia    (1000) mattia    (1000)        3 2018-07-09 13:01:04.000000 reprotest-0.7.8/debian/compat
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      123 2018-07-09 13:27:17.000000 reprotest-0.7.8/debian/watch
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       16 2017-02-14 08:52:29.000000 reprotest-0.7.8/debian/reprotest.manpages
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/bin/
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)      571 2018-06-03 13:54:53.000000 reprotest-0.7.8/bin/reprotest
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    20813 2018-07-09 13:37:47.000000 reprotest-0.7.8/PKG-INFO
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/doc/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1009 2018-06-03 13:54:53.000000 reprotest-0.7.8/doc/Makefile
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      420 2017-12-18 21:32:58.000000 reprotest-0.7.8/doc/reprotest.h2m.0
+-rwxr-xr-x   0 mattia    (1000) mattia    (1000)       84 2017-02-14 08:52:29.000000 reprotest-0.7.8/doc/reprotest
+drwxr-xr-x   0 mattia    (1000) mattia    (1000)        0 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/
+-rw-r--r--   0 mattia    (1000) mattia    (1000)        1 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/dependency_links.txt
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1477 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/SOURCES.txt
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       23 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/requires.txt
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       10 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/top_level.txt
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       46 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/entry_points.txt
+-rw-r--r--   0 mattia    (1000) mattia    (1000)    20813 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/PKG-INFO
+-rw-r--r--   0 mattia    (1000) mattia    (1000)        1 2018-07-09 13:37:47.000000 reprotest-0.7.8/reprotest.egg-info/not-zip-safe
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       44 2017-02-14 08:52:29.000000 reprotest-0.7.8/MANIFEST.in
+-rw-r--r--   0 mattia    (1000) mattia    (1000)      709 2017-12-18 21:32:58.000000 reprotest-0.7.8/tox.ini
+-rw-r--r--   0 mattia    (1000) mattia    (1000)     1307 2018-06-03 13:54:53.000000 reprotest-0.7.8/setup.py
+-rw-r--r--   0 mattia    (1000) mattia    (1000)       80 2018-07-09 13:37:47.000000 reprotest-0.7.8/setup.cfg
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive
+POSIX tar archive (GNU)
```

### Comparing `reprotest-0.7.25/PKG-INFO` & `reprotest-0.7.8/README.rst`

 * *Files 5% similar despite different names*

```diff
@@ -1,73 +1,41 @@
-Metadata-Version: 2.1
-Name: reprotest
-Version: 0.7.25
-Summary: Build packages and check them for reproducibility.
-Home-page: https://salsa.debian.org/reproducible-builds/reprotest
-Author: Ximin Luo, Ceridwen
-Author-email: infinity0@debian.org, ceridwenv@gmail.com
-License: GPL-3+
-Classifier: Development Status :: 3 - Alpha
-Classifier: Intended Audience :: Developers
-Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
-Classifier: Operating System :: POSIX
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Topic :: Utilities
-Provides-Extra: compare
-
 reprotest
 =========
 
 reprotest builds the same source code twice in different environments, and then
 checks the binaries produced by each build for differences. If any are found,
 then ``diffoscope(1)`` (or if unavailable then ``diff(1)``) is used to display
 them in detail for later analysis.
 
 See the ``COMMAND-LINE EXAMPLES`` section further below to get you
 started, as well as more detailed explanations of all the command-line
 options. The same information is also available in
 ``/usr/share/doc/reprotest/README.rst`` or similar.
 
-.. the below hack gets rid of the python "usage" message in favour of the
-   the synopsis we manually defined in doc/$(PACKAGE).h2m.0
+.. raw:: manpage
+
+   .\" the below hack gets rid of the python "usage" message in favour of the
+   .\" the synopsis we manually defined in doc/$(PACKAGE).h2m.0
    .SS positional arguments:
    .\" end_of_description_header
 
 Command-line examples
 =====================
 
 The easiest way to run reprotest is via our presets::
 
     # Build the current directory in a null server (/tmp)
     $ reprotest .
     $ reprotest . -vv -- null -d # for very verbose output
 
-    # Build a make-based program
-    $ reprotest "make clean && make" mybinary
-
-    # Build a Debian package
-    $ apt-get source hello && cd hello-2.10
-    $ reprotest  auto -- null
-    # Build a Debian package and disable some variations
-    $ reprotest --vary=-user_group,-domain_host,-fileordering auto -- null
-
     # Build the given Debian source package in an schroot
     # See https://wiki.debian.org/sbuild for instructions on setting that up.
     $ reprotest reprotest_0.3.3.dsc -- schroot unstable-amd64-sbuild
 
-    # Build the given RPM source package
-    # Only null server (/tmp) is currently supported.
-    $ reprotest reprotest-0.7.16.src.rpm
-
-    # Build the given RPM source package and automatically install dependencies
-    $ reprotest --testbed-build-pre 'dnf -y builddep ./*.src.rpm' reprotest-0.7.16.src.rpm
-
-Currently, we only support this for Debian and RPM based packages, but are keen on
+Currently, we only support this for Debian packages, but are keen on
 adding more. If we don't have knowledge on how to build your file or
 directory, you can send a patch to us on adding this intelligence - see
 the reprotest.presets python module, and adapt the existing logic.
 
 In the meantime, you can use other parts of the CLI to build arbitrary things.
 You'll need to give two mandatory arguments, the build command to run and the
 build artifact file/pattern to test after running the build. For example::
@@ -230,17 +198,17 @@
 may not be intended to be distributed to other systems. For example: (1) for
 most distros' package builders, we don't care about the metadata of the output
 package files; only the file contents will be distributed to other systems. On
 the other hand, (2) when running something like `make install`, we *do* care
 about the metadata, because this is what will be recreated on another system.
 
 In developing reprotest, our experience has been that case (1) is more common
-and so we pass ``--exclude-directory-metadata=yes`` by default to diffoscope. If
+and so we pass ``--exclude-directory-metadata`` by default to diffoscope. If
 you find that you are using reprotest for case (2) then you should pass
-``--diffoscope-args=--exclude-directory-metadata=no`` to reprotest, to tell
+``--diffoscope-args=--no-exclude-directory-metadata`` to reprotest, to tell
 diffoscope to not ignore the metadata since it will be distributed and should
 therefore be reproducible. Otherwise, you may get a false-positive result.
 
 
 Variations
 ==========
 
@@ -302,21 +270,14 @@
     descriptors to use. Default is empty, in which case we randomly choose a
     time: either now (if the latest file-modtime in ``source_root`` is older
     than about half-a-year) or more than half-a-year in the future.
 
     Note that the clock continues to run during the build. It is possible for
     ``faketime(1)`` to freeze it, but we don't yet support that yet; it has a
     higher chance of causing your build to fail or misbehave.
-locales.locale
-    A semicolon-separated list one or more locales to test when
-    performing locales variations.
-    If multiple locales are specified, one will be chosen at random.
-    Locales with different properties than en_US.UTF-8 are fr_CH.UTF-8,
-    ru_RU.CP1251, kk_KZ.RK1048 or zh_CN.
-    Default is et_EE.UTF-8 if unspecified.
 
 The difference between --vary and --variations is that the former appends onto
 previous values but the latter resets them. Furthermore, the last value set for
 --variations is treated as the zeroth --vary argument. For example::
 
     reprotest --vary=-user_group
 
@@ -402,20 +363,14 @@
   scope to audit or prevent this.)
 
 If you see a difference that you really think should not be there, try passing
 ``--variations=-time`` to reprotest, and/or check our results on
 https://tests.reproducible-builds.org/ which use a different (more reliable)
 mechanism to vary the system time.
 
-Kernel
-------
-
-The "kernel" variation is currently not working for RPM based packages and other
-build process requiring `ldconfig`.  While building with this variation enabled,
-`ldconfig` complains about `FATAL: kernel too old` and aborts the build.
 
 Avoid sudo(1) password prompts
 ==============================
 
 There is currently no good way to do this. The following is an EXPERIMENTAL
 solution and is brittle and unclean. You will have to decide for yourself if
 it's worth it for your use-case::
```

### Comparing `reprotest-0.7.25/README.rst` & `reprotest-0.7.8/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,428 +1,419 @@
-reprotest
-=========
-
-reprotest builds the same source code twice in different environments, and then
-checks the binaries produced by each build for differences. If any are found,
-then ``diffoscope(1)`` (or if unavailable then ``diff(1)``) is used to display
-them in detail for later analysis.
-
-See the ``COMMAND-LINE EXAMPLES`` section further below to get you
-started, as well as more detailed explanations of all the command-line
-options. The same information is also available in
-``/usr/share/doc/reprotest/README.rst`` or similar.
-
-.. the below hack gets rid of the python "usage" message in favour of the
-   the synopsis we manually defined in doc/$(PACKAGE).h2m.0
-   .SS positional arguments:
-   .\" end_of_description_header
-
-Command-line examples
-=====================
-
-The easiest way to run reprotest is via our presets::
-
-    # Build the current directory in a null server (/tmp)
-    $ reprotest .
-    $ reprotest . -vv -- null -d # for very verbose output
-
-    # Build a make-based program
-    $ reprotest "make clean && make" mybinary
-
-    # Build a Debian package
-    $ apt-get source hello && cd hello-2.10
-    $ reprotest  auto -- null
-    # Build a Debian package and disable some variations
-    $ reprotest --vary=-user_group,-domain_host,-fileordering auto -- null
-
-    # Build the given Debian source package in an schroot
-    # See https://wiki.debian.org/sbuild for instructions on setting that up.
-    $ reprotest reprotest_0.3.3.dsc -- schroot unstable-amd64-sbuild
-
-    # Build the given RPM source package
-    # Only null server (/tmp) is currently supported.
-    $ reprotest reprotest-0.7.16.src.rpm
-
-    # Build the given RPM source package and automatically install dependencies
-    $ reprotest --testbed-build-pre 'dnf -y builddep ./*.src.rpm' reprotest-0.7.16.src.rpm
-
-Currently, we only support this for Debian and RPM based packages, but are keen on
-adding more. If we don't have knowledge on how to build your file or
-directory, you can send a patch to us on adding this intelligence - see
-the reprotest.presets python module, and adapt the existing logic.
-
-In the meantime, you can use other parts of the CLI to build arbitrary things.
-You'll need to give two mandatory arguments, the build command to run and the
-build artifact file/pattern to test after running the build. For example::
-
-    $ reprotest 'python3 setup.py bdist' 'dist/*.tar.gz'
-
-This runs the command on ``.``, the current working directory. To run it on a
-project located elsewhere::
-
-    $ reprotest -s ../path/to/other/project 'python3 setup.py bdist' 'dist/*.tar.gz'
-    $ reprotest -c 'python3 setup.py bdist' ../path/to/other/project 'dist/*.tar.gz'
-
-These two invocations are equivalent; you can pick the most convenient one
-for your use-case. When using these from a shell:
-
-  * If the build command has spaces, you will need to quote them, e.g.
-    ``reprotest "dpkg-buildpackage -b --no-sign" [..]``.
-
-  * If you want to use several build artifact patterns, or if you want to
-    use shell wildcards as a pattern, you will also need to quote them, e.g.
-    ``reprotest [..] "*.tar.gz *.tar.xz"``.
-
-  * If your build artifacts have spaces in their names, you will need to
-    quote these twice, e.g. ``'"a file with spaces.gz"'`` for a single
-    artifact or ``'"dir 1"/* "dir 2"/*'`` for multiple patterns.
-
-To get more help for the CLI, including documentation on optional
-arguments and what they do, run::
-
-    $ reprotest --help
-
-
-Running in a virtual server
-===========================
-
-You can also run the build inside what is called a "virtual server".
-This could be a container, a chroot, etc. You run them like this::
-
-    $ reprotest 'python3 setup.py bdist_wheel'   'dist/*.whl' -- qemu    /path/to/qemu.img
-    $ reprotest 'dpkg-buildpackage -b --no-sign' '../*.deb'   -- schroot unstable-amd64
-
-There are different server types available. See ``--help`` for a list of
-them, which appears near the top, in the "virtual\_server\_args" part of
-the "positional arguments" section.
-
-For each virtual server (e.g. "schroot"), you see which extra arguments
-it supports::
-
-    $ reprotest --help schroot
-
-When running builds inside a virtual server, you will probably have to
-give extra commands, in order to set up your build dependencies inside
-the virtual server. For example, to take you through what the "Debian
-directory" preset would look like, if we ran it using the full CLI::
-
-    # "Debian directory" preset
-    $ reprotest . -- schroot unstable-amd64-sbuild
-    # This is exactly equivalent to this:
-    $ reprotest -c auto . -- schroot unstable-amd64-sbuild
-    # In the non-preset full CLI, this is roughly similar to:
-    $ reprotest \
-        --testbed-init 'apt-get -y --no-install-recommends install \
-                        disorderfs faketime locales-all sudo util-linux; \
-                        test -c /dev/fuse || mknod -m 666 /dev/fuse c 10 229; \
-                        test -f /etc/mtab || ln -s ../proc/self/mounts /etc/mtab' \
-        --testbed-build-pre 'apt-get -y --no-install-recommends build-dep ./' \
-        --build-command 'dpkg-buildpackage --no-sign -b' \
-        . \
-        '../*.deb' \
-        -- \
-        schroot unstable-amd64-sbuild
-
-The ``--testbed-init`` argument is needed to set up basic tools, which
-reprotest needs in order to make the variations in the first place. This
-should be the same regardless of what package is being built, but might
-differ depending on what virtual\_server is being used.
-
-Next, we have ``--testbed-build-pre``, then ``--build-command`` (or ``-c``).
-For our Debian directory, we install build-dependencies using ``apt-get``,
-then we run the actual build command itself using ``dpkg-buildpackage(1)``.
-
-Then, we have the ``source_root`` and the ``artifact_pattern``. For
-reproducibility, we're only interested in the binary packages.
-
-Finally, we specify that this is to take place in the "schroot"
-virtual\_server with arguments "unstable-amd64-sbuild".
-
-Of course, all of this is a burden to remember, if you must run the same
-thing many times. So that is why adding new presets for new package types
-would be good.
-
-Here is a more complex example. It tells reprotest to store the build products
-into ``./artifacts`` to analyse later; and also tweaks the "Debian dsc" preset
-so that it uses our `experimental toolchain
-<https://wiki.debian.org/ReproducibleBuilds/ExperimentalToolchain>`__::
-
-    $ reprotest --store-dir=artifacts \
-        --auto-preset-expr '_.prepend.testbed_init("apt-get install -y wget; \
-            echo deb http://reproducible.alioth.debian.org/debian/ ./ >> /etc/apt/sources.list; \
-            wget -q -O- https://reproducible.alioth.debian.org/reproducible.asc | apt-key add -; \
-            apt-get update; apt-get upgrade -y; ")' \
-        ./bash_4.4-4.0~reproducible1.dsc \
-        -- \
-        schroot unstable-amd64-sbuild
-
-Alternatively, you can clone your unstable-amd64-sbuild chroot, add our repo to
-the cloned chroot, then use this chroot in place of "unstable-amd64-sbuild".
-That would allow you to omit the long ``--auto-preset-expr`` flag above.
-
-
-Config File
-===========
-
-You can also give options to reprotest via a config file. This is a
-time-saving measure similar to ``auto`` presets; the difference is that
-these are more suited for local builds that are suited to your personal
-purposes. (You may use both presets and config files in the same build.)
-
-The config file takes exactly the same options as the command-line interface,
-but with the additional restriction that the section name must match the ones
-given in the --help output. Whitespace is allowed if and only if the same
-command-line option allows whitespace. Finally, it is not possible to give
-positional arguments via this mechanism.
-
-Reprotest by default does not load any config file. You can tell it to load one
-with the ``--config-file`` or ``-f`` command line options. If you give it a
-directory such as ``.``, it will load ``.reprotestrc`` within that directory.
-
-A sample config file is below::
-
-    [basics]
-    verbosity = 1
-    variations =
-      environment
-      build_path
-      user_group.available+=builduser:builduser
-      fileordering
-      home
-      kernel
-      locales
-      exec_path
-      time
-      timezone
-      umask
-    store_dir =
-      /home/foo/build/reprotest-artifacts
-
-    [diff]
-    diffoscope_arg =
-      --debug
-
-
-Analysing diff output
-=====================
-
-Normally when diffoscope compares directories, it also compares the metadata of
-files in those directories - file permissions, owners, and so on.
-
-However depending on the circumstance, this filesystem-level metadata may or
-may not be intended to be distributed to other systems. For example: (1) for
-most distros' package builders, we don't care about the metadata of the output
-package files; only the file contents will be distributed to other systems. On
-the other hand, (2) when running something like `make install`, we *do* care
-about the metadata, because this is what will be recreated on another system.
-
-In developing reprotest, our experience has been that case (1) is more common
-and so we pass ``--exclude-directory-metadata=yes`` by default to diffoscope. If
-you find that you are using reprotest for case (2) then you should pass
-``--diffoscope-args=--exclude-directory-metadata=no`` to reprotest, to tell
-diffoscope to not ignore the metadata since it will be distributed and should
-therefore be reproducible. Otherwise, you may get a false-positive result.
-
-
-Variations
-==========
-
-The --vary and --variations flags in their simple forms, are a comma-separated
-list of variation names that indicate which variations to apply. The full list
-of names is given in the --help text for --variations.
-
-| \
-| In full detail, the flags are a comma-separated list of actions, as follows:
-|
-| +$variation (or $variation with no explicit operator)
-| -$variation
-|    Enable or disable a variation
-|
-| @$variation
-|    Enable a variation, resetting its parameters (see below) to default values.
-|
-| $variation.$param=$value
-| $variation.$param+=$value
-| $variation.$param-=$value
-|    Set/add/remove $value as/to/from the current value of the $param parameter
-     of the $variation.
-|
-| $variation.$param++
-| $variation.$param--
-|    Increment/decrement the value of the $param parameter of the $variation.
-
-Most variations do not have parameters, and for them only the + and - operators
-are relevant. The variations that accept parameters are:
-
-domain_host.use_sudo
-    An integer, whether to use sudo(1) together with unshare(1) to change the
-    system hostname and domainname. 0 means don't use sudo; any non-zero value
-    means to use sudo. Default is 0, however this is not recommended and make
-    may your build fail, see "Varying the domain and host names" for details.
-environment.variables
-    A semicolon-separated ordered set, specifying environment variables that
-    reprotest should try to vary. Default is "REPROTEST_CAPTURE_ENVIRONMENT".
-    Supports regex-based syntax e.g.
-
-    - PID=\\d{1,6}
-    - HOME=(/\\w{3,12}){1,4}
-    - (GO|PYTHON|)PATH=(/\\w{3,12}){1,4}(:(/\\w{3,12}){1,4}){0,4}
-
-    Special cases:
-
-    - $VARNAME= (empty RHS) to tell reprotest to delete the variable
-    - $VARNAME=.{0} to tell reprotest to actually set an empty value
-    - \\x2c and \\x3b to match or generate , and ; respectively.
-user_group.available
-    A semicolon-separated ordered set, specifying the available user+group
-    combinations that reprotest can ``sudo(1)`` to. Default is empty, in which
-    case the variation is a no-op, and you'll see a warning about this. Each
-    user+group should be given in the form $user:$group where either component
-    can be omitted, or else if there is no colon then it is interpreted as only
-    a $user, with no $group variation.
-time.faketimes
-    A semicolon-separated ordered set, specifying possible ``faketime(1)`` time
-    descriptors to use. Default is empty, in which case we randomly choose a
-    time: either now (if the latest file-modtime in ``source_root`` is older
-    than about half-a-year) or more than half-a-year in the future.
-
-    Note that the clock continues to run during the build. It is possible for
-    ``faketime(1)`` to freeze it, but we don't yet support that yet; it has a
-    higher chance of causing your build to fail or misbehave.
-locales.locale
-    A semicolon-separated list one or more locales to test when
-    performing locales variations.
-    If multiple locales are specified, one will be chosen at random.
-    Locales with different properties than en_US.UTF-8 are fr_CH.UTF-8,
-    ru_RU.CP1251, kk_KZ.RK1048 or zh_CN.
-    Default is et_EE.UTF-8 if unspecified.
-
-The difference between --vary and --variations is that the former appends onto
-previous values but the latter resets them. Furthermore, the last value set for
---variations is treated as the zeroth --vary argument. For example::
-
-    reprotest --vary=-user_group
-
-means to vary +all (the default value for --variations) and -user_group (the
-given value for --vary), whereas::
-
-    reprotest --variations=-all,locales --variations=home,time --vary=timezone --vary=-time
-
-means to vary home, time (the last given value for --variations), timezone, and
--time (the given multiple values for --vary), i.e. home and timezone.
-
-
-Notes on variations
-===================
-
-reprotest tries hard to perform variations without assuming it has full root
-access to the system. It also assumes other software may be running on the same
-system, so it does not perform system-level modifications that would affect
-other processes. Due to these assumptions, some variations are implemented
-using hacks at various levels of dirtiness, which are documented below.
-
-We will hopefully lift these assumptions for certain virtual_server contexts,
-in future. That would likely allow for smoother operation in those contexts.
-The assumptions will remain for the "null" (default) virtual_server however.
-
-Number of CPUs
---------------
-
-The control build uses only 1 CPU in order to try to reduce nondeterminism that
-might exist due to multithreading or multiprocessing. If you are sure your
-build is not affected by this (and good builds ought not to be), you can give
---min-cpus=99999 to use all available cores for both builds.
-
-Domain or host
---------------
-
-Doing this without sudo *may* result in your build failing.
-
-Failure is likely if your build must do system-related things - as opposed to
-only processing bits and bytes. This is because it runs in a separate namespace
-where your non-privileged user looks like it is "root", but this prevents the
-filesystem from recognising files owned by the real "root" user, amongst other
-things. This is a limitation of unshare(1) and it is not possible work around
-this in reprotest without heavy effort.
-
-Therefore, it is recommended to run this variation with use_sudo=1. To avoid
-password prompts, see the section "Avoid sudo(1) password prompts" below.
-
-When running inside a virtual-server:
-
-The non-sudo method fails with "Operation not permitted", even if you edited
-``/proc/sys/kernel/unprivileged_userns_clone``. The cause is currently unknown.
-
-The sudo method works only if you take measures to avoid sudo password prompts,
-since containers don't have a method to input this.
-
-User or group
--------------
-
-If you also vary fileordering at the same time (this is the case by default),
-each user you use needs to be in the "fuse" group. Do that by running `usermod
--aG fuse $OTHERUSER` as root.
-
-To avoid sudo(1) password prompts, see the section "Avoid sudo(1) password
-prompts" below.
-
-Time
-----
-
-The "time" variation uses ``faketime(1)`` which *sometimes* causes weird and
-hard-to-diagnose problems. In the past, this has included:
-
-- builds taking an infinite amount of time; though this should be fixed in
-  recent versions of reprotest.
-
-- builds with implausibly huge differences caused by ./configure scripts
-  producing different results with and without faketime. This still affects
-  bash and probably certain other packages using autotools.
-
-- builds accessing the network failing due to certificate expiration errors
-  and/or other time-related security errors. (Transparent builds of FOSS should
-  not access the network in the first place, but it's outside of reprotest's
-  scope to audit or prevent this.)
-
-If you see a difference that you really think should not be there, try passing
-``--variations=-time`` to reprotest, and/or check our results on
-https://tests.reproducible-builds.org/ which use a different (more reliable)
-mechanism to vary the system time.
-
-Kernel
-------
-
-The "kernel" variation is currently not working for RPM based packages and other
-build process requiring `ldconfig`.  While building with this variation enabled,
-`ldconfig` complains about `FATAL: kernel too old` and aborts the build.
-
-Avoid sudo(1) password prompts
-==============================
-
-There is currently no good way to do this. The following is an EXPERIMENTAL
-solution and is brittle and unclean. You will have to decide for yourself if
-it's worth it for your use-case::
-
-    $ reprotest --print-sudoers \
-        --variations=user_group.available+=guest-builder,domain_host.use_sudo=1 \
-        | sudo EDITOR=tee visudo -f /etc/sudoers.d/local-reprotest
-
-Make sure you set the variations you actually want to use. Obviously, don't
-pick privileged users for this purpose, such as root.
-
-(Simplifying the output using wildcards, would open up passwordless access to
-chown anything on your system, because wildcards here match whitespace. I don't
-know what the sudo authors were thinking.)
-
-No, this is not nice at all - suggestions and patches welcome.
-
-If you want to use this in a virtual server such as a chroot, you'll need to
-copy (or mount or otherwise map) the resulting sudoers file into your chroot.
-
-For example, for an schroot, you should (1) login to the source schroot and
-create an empty file `/etc/sudoers.d/local-reprotest` (this is important) and
-then (2) add the line:
-
-    /etc/sudoers.d/local-reprotest  /etc/sudoers.d/local-reprotest  none bind 0 0
-
-to your schroot's fstab.
-
+Metadata-Version: 1.1
+Name: reprotest
+Version: 0.7.8
+Summary: Build packages and check them for reproducibility.
+Home-page: https://salsa.debian.org/reproducible-builds/reprotest
+Author: Ximin Luo, Ceridwen
+Author-email: infinity0@debian.org, ceridwenv@gmail.com
+License: GPL-3+
+Description: reprotest
+        =========
+        
+        reprotest builds the same source code twice in different environments, and then
+        checks the binaries produced by each build for differences. If any are found,
+        then ``diffoscope(1)`` (or if unavailable then ``diff(1)``) is used to display
+        them in detail for later analysis.
+        
+        See the ``COMMAND-LINE EXAMPLES`` section further below to get you
+        started, as well as more detailed explanations of all the command-line
+        options. The same information is also available in
+        ``/usr/share/doc/reprotest/README.rst`` or similar.
+        
+        .. raw:: manpage
+        
+           .\" the below hack gets rid of the python "usage" message in favour of the
+           .\" the synopsis we manually defined in doc/$(PACKAGE).h2m.0
+           .SS positional arguments:
+           .\" end_of_description_header
+        
+        Command-line examples
+        =====================
+        
+        The easiest way to run reprotest is via our presets::
+        
+            # Build the current directory in a null server (/tmp)
+            $ reprotest .
+            $ reprotest . -vv -- null -d # for very verbose output
+        
+            # Build the given Debian source package in an schroot
+            # See https://wiki.debian.org/sbuild for instructions on setting that up.
+            $ reprotest reprotest_0.3.3.dsc -- schroot unstable-amd64-sbuild
+        
+        Currently, we only support this for Debian packages, but are keen on
+        adding more. If we don't have knowledge on how to build your file or
+        directory, you can send a patch to us on adding this intelligence - see
+        the reprotest.presets python module, and adapt the existing logic.
+        
+        In the meantime, you can use other parts of the CLI to build arbitrary things.
+        You'll need to give two mandatory arguments, the build command to run and the
+        build artifact file/pattern to test after running the build. For example::
+        
+            $ reprotest 'python3 setup.py bdist' 'dist/*.tar.gz'
+        
+        This runs the command on ``.``, the current working directory. To run it on a
+        project located elsewhere::
+        
+            $ reprotest -s ../path/to/other/project 'python3 setup.py bdist' 'dist/*.tar.gz'
+            $ reprotest -c 'python3 setup.py bdist' ../path/to/other/project 'dist/*.tar.gz'
+        
+        These two invocations are equivalent; you can pick the most convenient one
+        for your use-case. When using these from a shell:
+        
+          * If the build command has spaces, you will need to quote them, e.g.
+            ``reprotest "dpkg-buildpackage -b --no-sign" [..]``.
+        
+          * If you want to use several build artifact patterns, or if you want to
+            use shell wildcards as a pattern, you will also need to quote them, e.g.
+            ``reprotest [..] "*.tar.gz *.tar.xz"``.
+        
+          * If your build artifacts have spaces in their names, you will need to
+            quote these twice, e.g. ``'"a file with spaces.gz"'`` for a single
+            artifact or ``'"dir 1"/* "dir 2"/*'`` for multiple patterns.
+        
+        To get more help for the CLI, including documentation on optional
+        arguments and what they do, run::
+        
+            $ reprotest --help
+        
+        
+        Running in a virtual server
+        ===========================
+        
+        You can also run the build inside what is called a "virtual server".
+        This could be a container, a chroot, etc. You run them like this::
+        
+            $ reprotest 'python3 setup.py bdist_wheel'   'dist/*.whl' -- qemu    /path/to/qemu.img
+            $ reprotest 'dpkg-buildpackage -b --no-sign' '../*.deb'   -- schroot unstable-amd64
+        
+        There are different server types available. See ``--help`` for a list of
+        them, which appears near the top, in the "virtual\_server\_args" part of
+        the "positional arguments" section.
+        
+        For each virtual server (e.g. "schroot"), you see which extra arguments
+        it supports::
+        
+            $ reprotest --help schroot
+        
+        When running builds inside a virtual server, you will probably have to
+        give extra commands, in order to set up your build dependencies inside
+        the virtual server. For example, to take you through what the "Debian
+        directory" preset would look like, if we ran it using the full CLI::
+        
+            # "Debian directory" preset
+            $ reprotest . -- schroot unstable-amd64-sbuild
+            # This is exactly equivalent to this:
+            $ reprotest -c auto . -- schroot unstable-amd64-sbuild
+            # In the non-preset full CLI, this is roughly similar to:
+            $ reprotest \
+                --testbed-init 'apt-get -y --no-install-recommends install \
+                                disorderfs faketime locales-all sudo util-linux; \
+                                test -c /dev/fuse || mknod -m 666 /dev/fuse c 10 229; \
+                                test -f /etc/mtab || ln -s ../proc/self/mounts /etc/mtab' \
+                --testbed-build-pre 'apt-get -y --no-install-recommends build-dep ./' \
+                --build-command 'dpkg-buildpackage --no-sign -b' \
+                . \
+                '../*.deb' \
+                -- \
+                schroot unstable-amd64-sbuild
+        
+        The ``--testbed-init`` argument is needed to set up basic tools, which
+        reprotest needs in order to make the variations in the first place. This
+        should be the same regardless of what package is being built, but might
+        differ depending on what virtual\_server is being used.
+        
+        Next, we have ``--testbed-build-pre``, then ``--build-command`` (or ``-c``).
+        For our Debian directory, we install build-dependencies using ``apt-get``,
+        then we run the actual build command itself using ``dpkg-buildpackage(1)``.
+        
+        Then, we have the ``source_root`` and the ``artifact_pattern``. For
+        reproducibility, we're only interested in the binary packages.
+        
+        Finally, we specify that this is to take place in the "schroot"
+        virtual\_server with arguments "unstable-amd64-sbuild".
+        
+        Of course, all of this is a burden to remember, if you must run the same
+        thing many times. So that is why adding new presets for new package types
+        would be good.
+        
+        Here is a more complex example. It tells reprotest to store the build products
+        into ``./artifacts`` to analyse later; and also tweaks the "Debian dsc" preset
+        so that it uses our `experimental toolchain
+        <https://wiki.debian.org/ReproducibleBuilds/ExperimentalToolchain>`__::
+        
+            $ reprotest --store-dir=artifacts \
+                --auto-preset-expr '_.prepend.testbed_init("apt-get install -y wget; \
+                    echo deb http://reproducible.alioth.debian.org/debian/ ./ >> /etc/apt/sources.list; \
+                    wget -q -O- https://reproducible.alioth.debian.org/reproducible.asc | apt-key add -; \
+                    apt-get update; apt-get upgrade -y; ")' \
+                ./bash_4.4-4.0~reproducible1.dsc \
+                -- \
+                schroot unstable-amd64-sbuild
+        
+        Alternatively, you can clone your unstable-amd64-sbuild chroot, add our repo to
+        the cloned chroot, then use this chroot in place of "unstable-amd64-sbuild".
+        That would allow you to omit the long ``--auto-preset-expr`` flag above.
+        
+        
+        Config File
+        ===========
+        
+        You can also give options to reprotest via a config file. This is a
+        time-saving measure similar to ``auto`` presets; the difference is that
+        these are more suited for local builds that are suited to your personal
+        purposes. (You may use both presets and config files in the same build.)
+        
+        The config file takes exactly the same options as the command-line interface,
+        but with the additional restriction that the section name must match the ones
+        given in the --help output. Whitespace is allowed if and only if the same
+        command-line option allows whitespace. Finally, it is not possible to give
+        positional arguments via this mechanism.
+        
+        Reprotest by default does not load any config file. You can tell it to load one
+        with the ``--config-file`` or ``-f`` command line options. If you give it a
+        directory such as ``.``, it will load ``.reprotestrc`` within that directory.
+        
+        A sample config file is below::
+        
+            [basics]
+            verbosity = 1
+            variations =
+              environment
+              build_path
+              user_group.available+=builduser:builduser
+              fileordering
+              home
+              kernel
+              locales
+              exec_path
+              time
+              timezone
+              umask
+            store_dir =
+              /home/foo/build/reprotest-artifacts
+        
+            [diff]
+            diffoscope_arg =
+              --debug
+        
+        
+        Analysing diff output
+        =====================
+        
+        Normally when diffoscope compares directories, it also compares the metadata of
+        files in those directories - file permissions, owners, and so on.
+        
+        However depending on the circumstance, this filesystem-level metadata may or
+        may not be intended to be distributed to other systems. For example: (1) for
+        most distros' package builders, we don't care about the metadata of the output
+        package files; only the file contents will be distributed to other systems. On
+        the other hand, (2) when running something like `make install`, we *do* care
+        about the metadata, because this is what will be recreated on another system.
+        
+        In developing reprotest, our experience has been that case (1) is more common
+        and so we pass ``--exclude-directory-metadata`` by default to diffoscope. If
+        you find that you are using reprotest for case (2) then you should pass
+        ``--diffoscope-args=--no-exclude-directory-metadata`` to reprotest, to tell
+        diffoscope to not ignore the metadata since it will be distributed and should
+        therefore be reproducible. Otherwise, you may get a false-positive result.
+        
+        
+        Variations
+        ==========
+        
+        The --vary and --variations flags in their simple forms, are a comma-separated
+        list of variation names that indicate which variations to apply. The full list
+        of names is given in the --help text for --variations.
+        
+        | \
+        | In full detail, the flags are a comma-separated list of actions, as follows:
+        |
+        | +$variation (or $variation with no explicit operator)
+        | -$variation
+        |    Enable or disable a variation
+        |
+        | @$variation
+        |    Enable a variation, resetting its parameters (see below) to default values.
+        |
+        | $variation.$param=$value
+        | $variation.$param+=$value
+        | $variation.$param-=$value
+        |    Set/add/remove $value as/to/from the current value of the $param parameter
+             of the $variation.
+        |
+        | $variation.$param++
+        | $variation.$param--
+        |    Increment/decrement the value of the $param parameter of the $variation.
+        
+        Most variations do not have parameters, and for them only the + and - operators
+        are relevant. The variations that accept parameters are:
+        
+        domain_host.use_sudo
+            An integer, whether to use sudo(1) together with unshare(1) to change the
+            system hostname and domainname. 0 means don't use sudo; any non-zero value
+            means to use sudo. Default is 0, however this is not recommended and make
+            may your build fail, see "Varying the domain and host names" for details.
+        environment.variables
+            A semicolon-separated ordered set, specifying environment variables that
+            reprotest should try to vary. Default is "REPROTEST_CAPTURE_ENVIRONMENT".
+            Supports regex-based syntax e.g.
+        
+            - PID=\\d{1,6}
+            - HOME=(/\\w{3,12}){1,4}
+            - (GO|PYTHON|)PATH=(/\\w{3,12}){1,4}(:(/\\w{3,12}){1,4}){0,4}
+        
+            Special cases:
+        
+            - $VARNAME= (empty RHS) to tell reprotest to delete the variable
+            - $VARNAME=.{0} to tell reprotest to actually set an empty value
+            - \\x2c and \\x3b to match or generate , and ; respectively.
+        user_group.available
+            A semicolon-separated ordered set, specifying the available user+group
+            combinations that reprotest can ``sudo(1)`` to. Default is empty, in which
+            case the variation is a no-op, and you'll see a warning about this. Each
+            user+group should be given in the form $user:$group where either component
+            can be omitted, or else if there is no colon then it is interpreted as only
+            a $user, with no $group variation.
+        time.faketimes
+            A semicolon-separated ordered set, specifying possible ``faketime(1)`` time
+            descriptors to use. Default is empty, in which case we randomly choose a
+            time: either now (if the latest file-modtime in ``source_root`` is older
+            than about half-a-year) or more than half-a-year in the future.
+        
+            Note that the clock continues to run during the build. It is possible for
+            ``faketime(1)`` to freeze it, but we don't yet support that yet; it has a
+            higher chance of causing your build to fail or misbehave.
+        
+        The difference between --vary and --variations is that the former appends onto
+        previous values but the latter resets them. Furthermore, the last value set for
+        --variations is treated as the zeroth --vary argument. For example::
+        
+            reprotest --vary=-user_group
+        
+        means to vary +all (the default value for --variations) and -user_group (the
+        given value for --vary), whereas::
+        
+            reprotest --variations=-all,locales --variations=home,time --vary=timezone --vary=-time
+        
+        means to vary home, time (the last given value for --variations), timezone, and
+        -time (the given multiple values for --vary), i.e. home and timezone.
+        
+        
+        Notes on variations
+        ===================
+        
+        reprotest tries hard to perform variations without assuming it has full root
+        access to the system. It also assumes other software may be running on the same
+        system, so it does not perform system-level modifications that would affect
+        other processes. Due to these assumptions, some variations are implemented
+        using hacks at various levels of dirtiness, which are documented below.
+        
+        We will hopefully lift these assumptions for certain virtual_server contexts,
+        in future. That would likely allow for smoother operation in those contexts.
+        The assumptions will remain for the "null" (default) virtual_server however.
+        
+        Number of CPUs
+        --------------
+        
+        The control build uses only 1 CPU in order to try to reduce nondeterminism that
+        might exist due to multithreading or multiprocessing. If you are sure your
+        build is not affected by this (and good builds ought not to be), you can give
+        --min-cpus=99999 to use all available cores for both builds.
+        
+        Domain or host
+        --------------
+        
+        Doing this without sudo *may* result in your build failing.
+        
+        Failure is likely if your build must do system-related things - as opposed to
+        only processing bits and bytes. This is because it runs in a separate namespace
+        where your non-privileged user looks like it is "root", but this prevents the
+        filesystem from recognising files owned by the real "root" user, amongst other
+        things. This is a limitation of unshare(1) and it is not possible work around
+        this in reprotest without heavy effort.
+        
+        Therefore, it is recommended to run this variation with use_sudo=1. To avoid
+        password prompts, see the section "Avoid sudo(1) password prompts" below.
+        
+        When running inside a virtual-server:
+        
+        The non-sudo method fails with "Operation not permitted", even if you edited
+        ``/proc/sys/kernel/unprivileged_userns_clone``. The cause is currently unknown.
+        
+        The sudo method works only if you take measures to avoid sudo password prompts,
+        since containers don't have a method to input this.
+        
+        User or group
+        -------------
+        
+        If you also vary fileordering at the same time (this is the case by default),
+        each user you use needs to be in the "fuse" group. Do that by running `usermod
+        -aG fuse $OTHERUSER` as root.
+        
+        To avoid sudo(1) password prompts, see the section "Avoid sudo(1) password
+        prompts" below.
+        
+        Time
+        ----
+        
+        The "time" variation uses ``faketime(1)`` which *sometimes* causes weird and
+        hard-to-diagnose problems. In the past, this has included:
+        
+        - builds taking an infinite amount of time; though this should be fixed in
+          recent versions of reprotest.
+        
+        - builds with implausibly huge differences caused by ./configure scripts
+          producing different results with and without faketime. This still affects
+          bash and probably certain other packages using autotools.
+        
+        - builds accessing the network failing due to certificate expiration errors
+          and/or other time-related security errors. (Transparent builds of FOSS should
+          not access the network in the first place, but it's outside of reprotest's
+          scope to audit or prevent this.)
+        
+        If you see a difference that you really think should not be there, try passing
+        ``--variations=-time`` to reprotest, and/or check our results on
+        https://tests.reproducible-builds.org/ which use a different (more reliable)
+        mechanism to vary the system time.
+        
+        
+        Avoid sudo(1) password prompts
+        ==============================
+        
+        There is currently no good way to do this. The following is an EXPERIMENTAL
+        solution and is brittle and unclean. You will have to decide for yourself if
+        it's worth it for your use-case::
+        
+            $ reprotest --print-sudoers \
+                --variations=user_group.available+=guest-builder,domain_host.use_sudo=1 \
+                | sudo EDITOR=tee visudo -f /etc/sudoers.d/local-reprotest
+        
+        Make sure you set the variations you actually want to use. Obviously, don't
+        pick privileged users for this purpose, such as root.
+        
+        (Simplifying the output using wildcards, would open up passwordless access to
+        chown anything on your system, because wildcards here match whitespace. I don't
+        know what the sudo authors were thinking.)
+        
+        No, this is not nice at all - suggestions and patches welcome.
+        
+        If you want to use this in a virtual server such as a chroot, you'll need to
+        copy (or mount or otherwise map) the resulting sudoers file into your chroot.
+        
+        For example, for an schroot, you should (1) login to the source schroot and
+        create an empty file `/etc/sudoers.d/local-reprotest` (this is important) and
+        then (2) add the line:
+        
+            /etc/sudoers.d/local-reprotest  /etc/sudoers.d/local-reprotest  none bind 0 0
+        
+        to your schroot's fstab.
+        
+        
+Platform: UNKNOWN
+Classifier: Development Status :: 3 - Alpha
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
+Classifier: Operating System :: POSIX
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.5
+Classifier: Topic :: Utilities
```

### Comparing `reprotest-0.7.25/reprotest/__init__.py` & `reprotest-0.7.8/reprotest/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -50,15 +50,15 @@
 # most POSIX OSes.  Linux containers (lxc) and namespaces are specific
 # to Linux.  Some versions of BSD have jails (MacOS X?).  There are a
 # variety of other options including Docker etc that use different
 # approaches.
 
 class Testbed(adt_testbed.Testbed):
 
-    def check_exec2(self, argv, stdout=False, kind='install', xenv=[]):
+    def check_exec2(self, argv, stdout=False, kind='short', xenv=[]):
         """Like check_exec but does not bomb on stderr, and can pass xenv."""
         (code, out, err) = self.execute(argv,
                                         stdout=(stdout and subprocess.PIPE or None),
                                         xenv=xenv, kind=kind)
         if code != 0:
             self.bomb('"%s" failed with status %i' % (' '.join(argv), code),
                       adtlog.AutopkgtestError)
@@ -87,15 +87,15 @@
     should_clean = True
     try:
         yield testbed
     except GeneratorExit:
         pass
     except BaseException as e:
         if no_clean_on_error:
-            logger.warning("preserving temporary files in: %s", testbed.scratch)
+            logger.warn("preserving temporary files in: %s", testbed.scratch)
             should_clean = False
         raise
     finally:
         if should_clean:
             testbed.stop()
         else:
             # give VirtSubproc a command it doesn't recognise, to force a non-zero Quit
@@ -260,37 +260,37 @@
     'virtual_server_args testbed_pre testbed_init testbed_build_pre host_distro')):
     @classmethod
     def of(cls, virtual_server_args=[], testbed_pre=None, testbed_init=None, testbed_build_pre=None, host_distro=None):
         return cls(virtual_server_args, testbed_pre, testbed_init, testbed_build_pre, host_distro)
 
 
 class TestArgs(collections.namedtuple('_Test',
-    'build_command source_root artifact_pattern result_dir source_pattern no_clean_on_error diffoscope_args control_build')):
+    'build_command source_root artifact_pattern result_dir source_pattern no_clean_on_error diffoscope_args')):
     @classmethod
     def of(cls, build_command, source_root, artifact_pattern, result_dir=None,
-                source_pattern=None, no_clean_on_error=False, diffoscope_args=['diffoscope'], control_build=None):
+                source_pattern=None, no_clean_on_error=False, diffoscope_args=['diffoscope']):
         artifact_pattern = shell_syn.sanitize_globs(artifact_pattern)
         logger.debug("artifact_pattern sanitized to: %s", artifact_pattern)
 
         if source_pattern:
             source_pattern = shell_syn.sanitize_globs(source_pattern)
             logger.debug("source_pattern sanitized to: %s", source_pattern)
         return cls(build_command, source_root, artifact_pattern, result_dir,
-                   source_pattern, no_clean_on_error, diffoscope_args, control_build)
+                   source_pattern, no_clean_on_error, diffoscope_args)
 
     @coroutine
     def corun_builds(self, testbed_args):
         """A coroutine for running the builds.
 
         .>>> proc = self.corun_builds(testbed_args)
         .>>> for name, var in variations:
         .>>>     local_dist = proc.send((name, var))
         .>>>     ...
         """
-        build_command, source_root, artifact_pattern, result_dir, source_pattern, no_clean_on_error, diffoscope_args, control_build = self
+        build_command, source_root, artifact_pattern, result_dir, source_pattern, no_clean_on_error, diffoscope_args = self
         virtual_server_args, testbed_pre, testbed_init, testbed_build_pre, host_distro = testbed_args
 
         if not source_root:
             raise ValueError("invalid source root: %s" % source_root)
         if os.path.isfile(source_root):
             source_root = os.path.normpath(os.path.dirname(source_root))
         source_root = str(source_root)
@@ -350,27 +350,21 @@
         run_or_tee(['sh', '-ec', 'find %s -type f -exec sha256sum "{}" \;' % self.artifact_pattern],
             'SHA256SUMS', self.result_dir,
             cwd=os.path.join(dist_control, VSRC_DIR))
 
 
 def check(test_args, testbed_args, build_variations=Variations.of(VariationSpec.default())):
     # default argument [] is safe here because we never mutate it.
-    _, _, artifact_pattern, store_dir, _, _, diffoscope_args, control_build = test_args
+    _, _, artifact_pattern, store_dir, _, _, diffoscope_args = test_args
     with empty_or_temp_dir(store_dir, "store_dir") as result_dir:
         assert store_dir == result_dir or store_dir is None
         proc = test_args._replace(result_dir=result_dir).corun_builds(testbed_args)
 
         bnames = ["control"] + ["experiment-%s" % i for i in range(1, len(build_variations))]
-
-        if control_build:
-            local_dists = [control_build]
-        else:
-            local_dists = [proc.send(("control", build_variations[0]))]
-
-        local_dists += [proc.send(nv) for nv in zip(bnames[1:], build_variations[1:])]
+        local_dists = [proc.send(nv) for nv in zip(bnames, build_variations)]
 
         retcodes = collections.OrderedDict(
             (bname, run_diff(local_dists[0], dist, diffoscope_args, store_dir))
             for bname, dist in zip(bnames, local_dists[1:]))
 
         retcode = max(retcodes.values())
         if retcode == 0:
@@ -387,15 +381,15 @@
             raise RuntimeError("diffoscope exited non-boolean %s" % retcode)
 
         return not retcode
 
 
 def check_auto(test_args, testbed_args, build_variations=Variations.of(VariationSpec.default())):
     # default argument [] is safe here because we never mutate it.
-    _, _, _, store_dir, _, _, diffoscope_args, _ = test_args
+    _, _, _, store_dir, _, _, diffoscope_args = test_args
     with empty_or_temp_dir(store_dir, "store_dir") as result_dir:
         assert store_dir == result_dir or store_dir is None
         proc = test_args._replace(result_dir=result_dir).corun_builds(testbed_args)
 
         var_x0, var_x1 = build_variations
         dist_x0 = proc.send(("control", var_x0))
         is_reproducible = lambda name, var: test_args.check_reproducible(proc, dist_x0, name, var)
@@ -427,15 +421,15 @@
         print(" ".join(unreproducibles))
         print("The build is probably reproducible when varying other things.")
         return False
 
 
 def check_env(test_args, testbed_args, build_variations=Variations.of(VariationSpec.default())):
     # default argument [] is safe here because we never mutate it.
-    _, _, artifact_pattern, store_dir, _, _, diffoscope_args, _ = test_args
+    _, _, artifact_pattern, store_dir, _, _, diffoscope_args = test_args
     with empty_or_temp_dir(store_dir, "store_dir") as result_dir:
         assert store_dir == result_dir or store_dir is None
         proc = test_args._replace(result_dir=result_dir).corun_builds(testbed_args)
 
         var_x0, var_x1 = build_variations
         dist_x0 = proc.send(("control", var_x0))
         is_reproducible = lambda name, var: test_args.check_reproducible(proc, dist_x0, name, var)
@@ -541,16 +535,15 @@
         help='Show this help message and exit. When given an argument, '
         'show instead the help message for that virtual server and exit. ')
     parser.add_argument('-f', '--config-file', default=None,
         help='File to load configuration from. (Default: %(default)s)')
 
     group1 = parser.add_argument_group('basic options')
     group1.add_argument('--verbosity', type=int, default=0,
-        help='An integer. Control which messages are displayed (0: quiet ('
-             'warning/error only), 1: info, 2: debug).')
+        help='An integer.  Control which messages are displayed.')
     group1.add_argument('-v', '--verbose', dest='verbosity', action='count',
         help='Like --verbosity, but given multiple times without arguments.')
     group1.add_argument('--host-distro', default=None,
         help='The distribution that will run the tests (Default: %(default)s)')
     group1.add_argument('-s', '--source-root', default=None, metavar='PATH',
         help='Root of the source tree, that is copied to the virtual server '
         'and made available during the build. If a file is given here, then '
@@ -563,16 +556,15 @@
     group1.add_argument('-c', '--build-command', default=None, metavar='COMMANDS',
         help='Build command to execute. If this is "auto" then reprotest will '
         'guess how to build the given source_root, in which case various other '
         'options may be automatically set-if-unset. Default: auto'),
     group1.add_argument('--store-dir', default=None, metavar='DIRECTORY',
         help='Save the artifacts in this directory, which must be empty or '
         'non-existent. Otherwise, the artifacts will be deleted and you only '
-        'see their hashes (if reproducible) or the diff output (if not). See '
-        'also --no-clean-on-error.')
+        'see their hashes (if reproducible) or the diff output (if not).')
     group1.add_argument('--variations', default="+all",
         help='Build variations to test as a comma-separated list of variation '
         'names. Default is "+all", equivalent to "%s", testing all available '
         'variations. See the man page section on VARIATIONS for more advanced '
         'syntax options, including tweaking how certain variations work.' %
         VariationSpec.default_long_string())
     group1.add_argument('--vary', metavar='VARIATIONS', default=[], action='append',
@@ -602,15 +594,15 @@
     group1.add_argument('--dont-vary', default=[], action='append', help=argparse.SUPPRESS)
 
     group2 = parser.add_argument_group('diff options')
     group2.add_argument('--diffoscope-arg', action='append', metavar='ARG',
         help='Give extra arguments to diffoscope when running it. Default: '
         '%(default)s. Arguments are {}-formatted with: {0} the name of each '
         'experiment run, and {1} the path of the experiment output.',
-        default=['--exclude-directory-metadata=yes'])
+        default=['--exclude-directory-metadata'])
     group2.add_argument('--diffoscope', default='diffoscope', metavar='PATH',
         help='Path to diffoscope(1). Default: %(default)s')
     group2.add_argument('--no-diffoscope', action='store_true', default=False,
         help='Don\'t run diffoscope; instead run diff(1). Useful if you '
         'don\'t want to install diffoscope and/or just want a quick answer '
         'on whether the reproduction was successful or not, without spending '
         'time to compute all the detailed differences.')
@@ -638,19 +630,14 @@
         'Useful for debugging but will leave cruft on your system depending on '
         'the virtual_server used; we hint about some but there may be others.')
     group3.add_argument('--dry-run', action='store_true', default=False,
         help='Don\'t run the builds, just print what would happen.')
     group3.add_argument('--print-sudoers', action='store_true', default=False,
         help='Print a sudoers file for passwordless operation using the given '
         '--variations, useful for user_group.available, domain_host.use_sudo.')
-    group3.add_argument('--control-build',  default=None,
-        help='Override control build with artifacts located on this path. '
-        'Allows reusing previous build as baseline.')
-    group3.add_argument('--append-build-command',  default=None, metavar='COMMANDS',
-        help='Append arguments to the build command')
 
     return parser
 
 
 def command_line(parser, argv):
     # parse_known_args does not exactly do what we want - we want everything
     # after '--' to belong to virtual_server_args, but parse_known_args instead
@@ -688,15 +675,15 @@
 
     return args
 
 
 def get_main_spec(parsed_args):
     variations = [parsed_args.variations] + parsed_args.vary
     if parsed_args.dont_vary:
-        logger.warning("--dont-vary is deprecated; use --vary=-$variation instead")
+        logger.warn("--dont-vary is deprecated; use --vary=-$variation instead")
         variations += ["-%s" % a for x in parsed_args.dont_vary for a in x.split(",")]
     return VariationSpec().extend(variations)
 
 
 def run(argv, dry_run=None):
     # Argparse exits with status code 2 if something goes wrong, which
     # is already the right status exit code for reprotest.
@@ -730,27 +717,27 @@
             build_command = first_arg
         elif not first_arg:
             print("No <source_root> or <build_command> provided. See --help for options.")
             sys.exit(2)
         elif first_arg == "auto":
             build_command = first_arg
             if parsed_args.artifact_pattern:
-                logger.warning("old CLI form `reprotest auto <source_root>` detected, "
+                logger.warn("old CLI form `reprotest auto <source_root>` detected, "
                     "setting source_root to the second argument: %s", parsed_args.artifact_pattern)
-                logger.warning("to avoid this warning, use instead `reprotest <source_root>` "
+                logger.warn("to avoid this warning, use instead `reprotest <source_root>` "
                     "or (if really necessary) `reprotest -s <source_root> auto <artifact>`")
                 source_root = parsed_args.artifact_pattern
                 parsed_args.artifact_pattern = None
         elif os.path.exists(first_arg):
             source_root = first_arg
         else:
             parts = shlex.split(first_arg)
             if len(parts) == 1:
                 if shutil.which(parts[0]) is None:
-                    logger.warning("XXX")
+                    logger.warn("XXX")
                     raise RuntimeError("Not found, neither as a file nor as a command: %s" % first_arg)
             # if len(parts) > 1 then it could be something like '( command )'
             # which is valid despite '(' not existing.
             build_command = first_arg
     build_command = build_command or parsed_args.build_command or "auto"
     source_root = source_root or parsed_args.source_root or '.'
 
@@ -780,26 +767,25 @@
         testbed_build_pre = testbed_build_pre or values.testbed_build_pre
         if values.diffoscope_args is not None:
             diffoscope_args = values.diffoscope_args + diffoscope_args
         if values.source_pattern is not None:
             source_pattern = values.source_pattern + (" " + source_pattern if source_pattern else "")
 
     # Variations args
-    spec = get_main_spec(parsed_args)
-    specs = [spec]
+    specs = [get_main_spec(parsed_args)]
     if parsed_args.auto_build:
         check_func = check_auto
     elif parsed_args.env_build:
         check_func = check_env
     else:
         for extra_build in parsed_args.extra_build:
             specs.append(spec.extend(extra_build))
         check_func = check
     if parsed_args.min_cpus is None and not dry_run:
-        logger.warning("The control build runs on 1 CPU by default, give --min-cpus to increase this.")
+        logger.warn("The control build runs on 1 CPU by default, give --min-cpus to increase this.")
     min_cpus = parsed_args.min_cpus or 1
     build_variations = Variations.of(
         *specs,
         verbosity=verbosity,
         min_cpus=min_cpus,
         # TODO: make this configurable via command line
         base_faketime='@%d' % build.auto_source_date_epoch(source_root))
@@ -809,44 +795,37 @@
         missing = [(var, tool_missing(action))
             for spec in specs
             for var, vary, action in spec.actions()
             if vary]
         missing = [(var, tools) for var, tools in missing if tools]
         for var, tools in missing:
             if tools:
-                logger.warning("Varying '%s' requires these program(s): %s", var, ", ".join(tools))
+                logger.warn("Varying '%s' requires these program(s): %s", var, ", ".join(tools))
         if missing:
-            logger.warning("Your build will probably fail, either install them or disable the variations.")
-            logger.warning("(From a system package manager, simply install the 'optional' or 'recommended' "
+            logger.warn("Your build will probably fail, either install them or disable the variations.")
+            logger.warn("(From a system package manager, simply install the 'optional' or 'recommended' "
                          "dependencies of reprotest.)")
 
     # Remaining args
     host_distro = parsed_args.host_distro
     store_dir = parsed_args.store_dir
     no_clean_on_error = parsed_args.no_clean_on_error
     diffoscope = parsed_args.diffoscope
     if parsed_args.no_diffoscope:
         diffoscope_args = None
-    elif shutil.which('diffoscope'):
-        diffoscope_args = [diffoscope] + diffoscope_args
     else:
-        logger.warning("diffoscope not available, falling back to regular diff")
-        diffoscope_args = None
-    control_build = parsed_args.control_build
-    append_build_command = parsed_args.append_build_command
-    if append_build_command :
-        build_command = ' '.join([build_command, append_build_command])
+        diffoscope_args = [diffoscope] + diffoscope_args
 
     if not artifact_pattern:
         print("No <artifact> to test for differences provided. See --help for options.")
         sys.exit(2)
 
     testbed_args = TestbedArgs.of(virtual_server_args, testbed_pre, testbed_init, testbed_build_pre, host_distro)
     test_args = TestArgs.of(build_command, source_root, artifact_pattern, store_dir,
-                            source_pattern, no_clean_on_error, diffoscope_args, control_build)
+                            source_pattern, no_clean_on_error, diffoscope_args)
 
     check_args = (test_args, testbed_args, build_variations)
     if dry_run:
         return check_args
     else:
         try:
             return 0 if check_func(*check_args) else 1
```

### Comparing `reprotest-0.7.25/reprotest/build.py` & `reprotest-0.7.8/reprotest/build.py`

 * *Files 10% similar despite different names*

```diff
@@ -5,15 +5,14 @@
 import functools
 import getpass
 import grp
 import logging
 import os
 import shlex
 import shutil
-import struct
 import random
 import time
 import types
 
 from reprotest import environ
 from reprotest import mdiffconf
 from reprotest import shell_syn
@@ -203,26 +202,22 @@
         return build
     added, removed = [], []
     for k, v in environ.parse_environ_templates(ctx.spec.environment.variables):
         if v is None:
             removed += [k]
         else:
             added += [(k, v)]
-    if ctx.verbosity >= 1:
-        logger.info("ENVIRONMENT variation: added = (" + ','.join(map(str, added)) + ") removed = " + ''.join(removed))
     return build.modify_env(added, removed)
 
 def domain_host(ctx, build, vary):
     if not vary:
         return build
     hostname = "reprotest-capture-hostname"
     domainname = "reprotest-capture-domainname"
     _ = build
-    if ctx.verbosity >= 1:
-        logger.info("DOMAIN_HOST variation: hostname = " + hostname + " domainname = " + domainname)
 
     # TODO: below only works on linux, of course..
     if ctx.spec.domain_host.use_sudo:
         ns_uts = '%s/ns-%s' % (build.aux_tree, "uts")
         _ = _.append_setup_exec('touch', ns_uts)
         # create our unshare
         ns_args = ['--uts=%s' % ns_uts]
@@ -231,16 +226,16 @@
         # configure our unshare
         nsenter = SUDO + ['nsenter'] + ns_args
         _ = _.append_setup_exec(*nsenter, 'hostname', hostname)
         _ = _.append_setup_exec(*nsenter, 'domainname', domainname)
         # wrap our build command
         _ = _.prepend_to_build_command(*SUDO, '-E', *(nsenter[len(SUDO):]), *make_sudo_command(*current_user_group()))
     else:
-        logger.warning("Not using sudo for domain_host; your build may fail. See man page for other options.")
-        logger.warning("Be sure to `echo 1 > /proc/sys/kernel/unprivileged_userns_clone` if on a Debian system.")
+        logger.warn("Not using sudo for domain_host; your build may fail. See man page for other options.")
+        logger.warn("Be sure to `echo 1 > /proc/sys/kernel/unprivileged_userns_clone` if on a Debian system.")
         if "user_group" in ctx.spec and ctx.spec.user_group.available:
             logger.error("Incompatible variations: domain_host.use_sudo False, user_group.available non-empty.")
             raise ValueError("Incompatible variations; check the log for details.")
         _ = _.prepend_to_build_command(*"unshare -r --uts".split(),
             "sh", "-ec", r"""
             hostname {1}
             domainname "{2}"
@@ -250,24 +245,20 @@
 # Note: this has to go before fileordering because we can't move mountpoints
 # TODO: this variation makes it impossible to parallelise the build, for most
 # of the current virtual servers. (It's theoretically possible to make it work)
 def build_path(ctx, build, vary):
     if vary:
         return build
     const_path = os.path.join(dirname(build.tree), 'const_build_path')
-    if ctx.verbosity >= 1:
-        logger.info("BUILD_PATH variation: const_path = " + const_path)
     return build.move_tree(build.tree, const_path, True)
 
 @tool_required("disorderfs")
 def fileordering(ctx, build, vary):
     if not vary:
         return build
-    if ctx.verbosity >= 1:
-        logger.info("DISORDERFS variation: --shuffle-dirents=yes")
 
     old_tree = os.path.join(dirname(build.tree), basename(build.tree) + '-before-disorderfs', '')
     _ = build.move_tree(build.tree, old_tree, False)
     _ = _.append_setup_exec('mkdir', '-p', build.tree)
     _ = _.prepend_cleanup_exec('rmdir', build.tree)
     disorderfs = ['disorderfs'] + (['>&2'] if ctx.verbosity >= 2 else ['-q'])
     _ = _.append_setup_exec_raw(*disorderfs, *map(shlex.quote, ['--shuffle-dirents=yes', old_tree, build.tree]))
@@ -279,59 +270,33 @@
 
 # Note: this has to go after anything that might modify 'tree' e.g. build_path
 def home(ctx, build, vary):
     if not vary:
         # choose an existent HOME, see Debian bug #860428
         return build.add_env('HOME', build.tree)
     else:
-        if ctx.verbosity >= 1:
-            logger.info("HOME variation: HOME = /nonexistent/second-build")
         return build.add_env('HOME', '/nonexistent/second-build')
 
 # TODO: uname is a POSIX standard.  The related Linux command
 # (setarch) only affects uname at the moment according to the docs.
 # FreeBSD changes uname with environment variables.  Wikipedia has a
 # reference to a setname command on another Unix variant:
 # https://en.wikipedia.org/wiki/Uname
 def kernel(ctx, build, vary):
     _ = build
     if not vary:
         _ = _.append_setup_exec_raw('SETARCH_ARCH=$(uname -m)')
     else:
-        _ = _.append_setup_exec_raw('SETARCH_ARCH=$(for a in $(setarch --list); do setarch $a true && echo $a || true; done)')
-        # Perform realistic shuffling of architectures depending
-        # on the bitness of application.
-        # 64-bit binaries can NOT be executed on 32-bit CPU,
-        # so filter out setarch's PER_LINUX32 architectures:
-        #
-        # echo $(grep -ioe "{PER_LINUX.*,.*$" /tmp/setarch.c |
-        #     grep -v machine | grep PER_LINUX32 | awk '{print $2}' | sort -Vu) | sed 's/,//g;s/"//g'
-        _ = _.append_setup_exec_raw('DROP_ARCH="-v -e ^$(uname -m)\$"')
-        _ = _.append_setup_exec_raw('WORDSIZE={}'.format(struct.calcsize("P")*8))
-        _ = _.append_setup_exec_raw('if [ $WORDSIZE -eq 64 ]; then \
-    for _ARCH_TO_DROP in armh armv7b armv7l \
-        armv8b armv8l arm athlon i386 i486 \
-        i586 i686 linux32 mips32 mips parisc32 \
-        parisc ppc32le ppc32 ppcle ppc s390 \
-        sparc32bash sparc32 sparc; \
-    do \
-        DROP_ARCH="$DROP_ARCH -e ^$_ARCH_TO_DROP\$"; \
-    done; \
-fi')
-        _ = _.append_setup_exec_raw('SETARCH_ARCH=$(echo "$SETARCH_ARCH" | grep $DROP_ARCH | shuf -n1)')
+        _ = _.append_setup_exec_raw('SETARCH_ARCH=$(setarch --list | grep -vF "$(uname -m)" | shuf | head -n1)')
         _ = _.append_setup_exec_raw('KERNEL_VERSION=$(uname -r)')
         _ = _.append_setup_exec_raw('if [ ${KERNEL_VERSION#2.6} = $KERNEL_VERSION ]; then SETARCH_OPTS=--uname-2.6; fi')
-        if ctx.verbosity >= 1:
-            _ = _.append_setup_exec_raw('echo "INFO:reprotest.build:KERNEL variation: SETARCH_ARCH = \'$SETARCH_ARCH\' SETARCH_OPTS = \'$SETARCH_OPTS\'" >&2')
     return _.prepend_to_build_command_raw('setarch', '$SETARCH_ARCH', '$SETARCH_OPTS')
 
 def aslr(ctx, build, vary):
     if vary:
-        if ctx.verbosity >= 1:
-            logger.info("ASLR variation: ASLR enabled")
         return build
     return build.append_setup_exec_raw('SETARCH_OPTS="$SETARCH_OPTS -R"')
 
 def num_cpus(ctx, build, vary):
     _ = build
     _ = _.append_setup_exec_raw('CPU_MAX=$(nproc)')
     _ = _.append_setup_exec_raw('CPU_MIN=$({ echo $CPU_MAX; echo %s; } | sort -n | head -n1)' % ctx.min_cpus)
@@ -342,18 +307,16 @@
     else:
         # random number between min_cpus and $(nproc)
         _ = _.append_setup_exec_raw('CPU_NUM=$(if [ $CPU_MIN = $CPU_MAX ]; \
             then echo $CPU_MIN; echo >&2 "only 1 CPU is available; num_cpus is ineffective"; \
             else shuf -i$((CPU_MIN + 1))-$CPU_MAX -n1; fi)')
 
     # select CPU_NUM random cpus from the range 0..$((CPU_MAX-1))
-    _ = _.append_setup_exec_raw("export CPU_LIST=\"$(echo $(shuf -i0-$((CPU_MAX - 1)) -n$CPU_NUM) | tr ' ' ,)\"")
-    if vary and ctx.verbosity >= 1:
-        _ = _.append_setup_exec_raw('echo "INFO:reprotest.build:NUM_CPUS variation: cpu_list = $CPU_LIST" >&2')
-    return _.prepend_to_build_command_raw('taskset', '-a', '-c', '$CPU_LIST')
+    cpu_list = "$(echo $(shuf -i0-$((CPU_MAX - 1)) -n$CPU_NUM) | tr ' ' ,)"
+    return _.prepend_to_build_command_raw('taskset', '-a', '-c', cpu_list)
 
 # TODO: if this locale doesn't exist on the system, Python's
 # locales.getlocale() will return (None, None) rather than this
 # locale.  I imagine it will also probably cause false positives with
 # builds being reproducible when they aren't because of locale-based
 # issues if this locale isn't installed.  The right solution here is
 # for this locale to be encoded into the dependencies so installing it
@@ -363,86 +326,69 @@
 
 # TODO: what exact locales and how to many test is probably a mailing
 # list question.
 def locales(ctx, build, vary):
     if not vary:
         return build.add_env('LANG', 'C.UTF-8').add_env('LANGUAGE', 'en_US:en')
     else:
-        # Use an Estonian locale by default, which has interesting sort order for ASCII characters
-        loc = 'et_EE.UTF-8'
-        if ctx.spec.locales.locale:
-            loc = random.choice(ctx.spec.locales.locale)
-        if ctx.verbosity >= 1:
-            logger.info("LOCALE variation: LC_ALL = " + loc + " LANGUAGE = " + loc + ":fr")
+        # if there is an issue with this being random, we could instead select it
+        # based on a deterministic hash of the inputs
+        loc = random.choice(['fr_CH.UTF-8', 'es_ES', 'ru_RU.CP1251', 'kk_KZ.RK1048', 'zh_CN'])
         return build.add_env('LANG', loc).add_env('LC_ALL', loc).add_env('LANGUAGE', '%s:fr' % loc)
 
 def exec_path(ctx, build, vary):
     if not vary:
         return build
-    if ctx.verbosity >= 1:
-        logger.info("EXEC_PATH variation: PATH = " + build.env['PATH'] + ':/i_capture_the_path')
     return build.add_env('PATH', build.env['PATH'] + ':/i_capture_the_path')
 
 # This doesn't require superuser privileges, but the chsh command
 # affects all user shells, which would be bad.
 # # def shell(ctx, script, env, tree):
 #     return script, env, tree
 # FIXME: also test differences with /bin/sh as bash vs dash
 
 def timezone(ctx, build, vary):
     # These time zones are theoretically in the POSIX time zone format
     # (http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap08.html#tag_08),
     # so they should be cross-platform compatible.
     if not vary:
-        if ctx.verbosity >= 1:
-            logger.info("TIMEZONE variation: TZ=GMT+12")
         return build.add_env('TZ', 'GMT+12')
     else:
-        if ctx.verbosity >= 1:
-            logger.info("TIMEZONE variation: TZ=GMT-14")
         return build.add_env('TZ', 'GMT-14')
 
 @tool_required("faketime")
 def faketime(ctx, build, vary):
-    if "time" not in ctx.spec:
-        return build
     if not vary:
         # fix the time at base_faketime
         faket = ctx.base_faketime
     elif ctx.spec.time.faketimes:
         faket = random.choice(ctx.spec.time.faketimes)
     else:
         now = time.time()
         base = int(ctx.base_faketime[1:]) if ctx.base_faketime.startswith("@") else now
         # 15552000 = 180 days
         if base < now - 15552000 and not random.randint(0, 1):
             # if ctx.base_faketime is far in the past, with 1/2 probability
             # reuse the current time and don't fake it
-            if ctx.verbosity >= 1:
-                logger.info("FAKETIME variation: enabled but chosen randomly not to fake!")
             return build
         else:
             # otherwise use a date far in the future
             faket = '+%sdays+%shours+%sminutes' % (
                 random.randint(180, 540), random.randint(0, 23), random.randint(0, 59))
 
     # faketime's manpages are stupidly misleading; it also modifies file timestamps.
     # this is only mentioned in the README. we do not want this, it really really
     # messes with GNU make and other buildsystems that look at timestamps.
     # set NO_FAKE_STAT=1 avoids this.
-    if ctx.verbosity >= 1:
-        logger.info("FAKETIME variation: faketime = " + faket)
     return build.add_env('NO_FAKE_STAT', '1').prepend_to_build_command('faketime', faket)
 
 def umask(ctx, build, vary):
     if not vary:
         return build.append_setup_exec('umask', '0022')
     else:
-        if ctx.verbosity >= 1:
-            logger.info("UMASK variation: umask 0002")
         return build.append_setup_exec('umask', '0002')
 
 
 def current_user_group():
     return getpass.getuser(), grp.getgrgid(os.getgid()).gr_name
 
 
@@ -473,15 +419,15 @@
 # as the other user (e.g. due to permissions).
 @tool_required("sudo")
 def user_group(ctx, build, vary):
     if not vary:
         return build
 
     if not ctx.spec.user_group.available:
-        logger.warning("IGNORING user_group variation; supply more usergroups "
+        logger.warn("IGNORING user_group variation; supply more usergroups "
         "with --variations=user_group.available+=USER1:GROUP1;USER2:GROUP2 or "
         "alternatively, suppress this warning with --variations=-user_group")
         return build
 
     olduser, oldgroup = current_user_group()
     user_group = random.choice(list(set(ctx.spec.user_group.available) - set([(olduser, oldgroup)])))
     user, group = parse_user_group(user_group)
@@ -573,28 +519,23 @@
 
 
 class DomainHostVariation(collections.namedtuple('_DomainHostVariation', 'use_sudo')):
     @classmethod
     def default(cls):
         return cls(0)
 
-class LocalesVariation(collections.namedtuple('_LocaleVariation', 'locale')):
-    @classmethod
-    def default(cls):
-        return cls(mdiffconf.strlist_set(";"))
 
 class VariationSpec(mdiffconf.ImmutableNamespace):
     @classmethod
     def default(cls, variations=VARIATIONS):
         default_overrides = {
             "environment": EnvironmentVariation.default(),
             "user_group": UserGroupVariation.default(),
             "time": TimeVariation.default(),
             "domain_host": DomainHostVariation.default(),
-            "locales": LocalesVariation.default(),
         }
         return cls(**{k: default_overrides.get(k, True) for k in variations})
 
     @classmethod
     def default_long_string(cls):
         actions = cls.default().actions()
         return ", ".join("+" + a[0] for a in actions)
@@ -632,16 +573,16 @@
 
     @property
     def replace(self):
         return AttributeReplacer(self, [])
 
 
 def print_sudoers(spec):
-    logger.warning("This feature is EXPERIMENTAL, use at your own risk.")
-    logger.warning("The output may be out-of-date, please file bugs if it doesn't work...")
+    logger.warn("This feature is EXPERIMENTAL, use at your own risk.")
+    logger.warn("The output may be out-of-date, please file bugs if it doesn't work...")
 
     user, group = current_user_group()
     a = "[a-zA-Z0-9]"
     b = "/tmp/reprotest.{0}{0}{0}{0}{0}{0}".format(a)
     variables = {
         "user": user,
         "group": group,
```

### Comparing `reprotest-0.7.25/reprotest/environ.py` & `reprotest-0.7.8/reprotest/environ.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/lib/VirtSubproc.py` & `reprotest-0.7.8/reprotest/lib/VirtSubproc.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/lib/adt_testbed.py` & `reprotest-0.7.8/reprotest/lib/adt_testbed.py`

 * *Files 1% similar despite different names*

```diff
@@ -35,32 +35,24 @@
 import urllib.parse
 
 # Don't need this in reprotest, try to be distro-agnostic
 #from debian import debian_support
 
 from reprotest.lib.system_interface.debian import DebianInterface
 from reprotest.lib.system_interface.arch import ArchInterface
-from reprotest.lib.system_interface.fedora import FedoraInterface
-from reprotest.lib.system_interface.guix import GuixInterface
 from reprotest.lib import adtlog
 from reprotest.lib import VirtSubproc
 
 SYSTEM_INTERFACES = {
         'debian': DebianInterface,
-        'arch': ArchInterface,
-        'fedora': FedoraInterface,
-        'guix': GuixInterface,
+        'arch': ArchInterface
         }
 
-timeouts = {
-    'copy': int(os.getenv('REPROTEST_TIMEOUT_COPY', 300)),
-    'install': int(os.getenv('REPROTEST_TIMEOUT_INSTALL', 3000)),
-    'test': int(os.getenv('REPROTEST_TIMEOUT_TEST', 10000)),
-    'build': int(os.getenv('REPROTEST_TIMEOUT_BUILD', 100000)),
-}
+timeouts = {'short': 100, 'copy': 300, 'install': 3000, 'test': 10000,
+            'build': 100000}
 
 
 class Testbed:
     def __init__(self, vserver_argv, output_dir, user,
                  setup_commands=[], setup_commands_boot=[], add_apt_pockets=[],
                  copy_files=[], host_distro=None):
         self.sp = None
@@ -207,18 +199,18 @@
                              self.last_reboot_marker and (', last reboot marker: ' + self.last_reboot_marker) or ''))
 
         # get CPU info
         if self.nproc is None:
             cpu_info = self.check_exec(['sh', '-c', 'nproc; cat /proc/cpuinfo 2>/dev/null || true'],
                                        stdout=True).strip()
             self.nproc = cpu_info.split('\n', 1)[0]
-            m = re.search(r'^(model.*name|cpu)\s*:\s*(.*)$', cpu_info, re.MULTILINE | re.IGNORECASE)
+            m = re.search('^(model.*name|cpu)\s*:\s*(.*)$', cpu_info, re.MULTILINE | re.IGNORECASE)
             if m:
                 self.cpu_model = m.group(2)
-            m = re.search(r'^(flags|features)\s*:\s*(.*)$', cpu_info, re.MULTILINE | re.IGNORECASE)
+            m = re.search('^(flags|features)\s*:\s*(.*)$', cpu_info, re.MULTILINE | re.IGNORECASE)
             if m:
                 self.cpu_flags = m.group(2)
 
         xenv = ['AUTOPKGTEST_IS_SETUP_BOOT_COMMAND=1']
         if self.user:
             xenv.append('AUTOPKGTEST_NORMAL_USER=' + self.user)
             xenv.append('ADT_NORMAL_USER=' + self.user)
@@ -433,15 +425,15 @@
         al = cmd + args
         self.send(' '.join(al))
         ll = self.expect('ok', nresults)
         if unquote:
             ll = list(map(urllib.parse.unquote, ll))
         return ll
 
-    def execute(self, argv, xenv=[], stdout=None, stderr=None, kind='install'):
+    def execute(self, argv, xenv=[], stdout=None, stderr=None, kind='short'):
         '''Run command in testbed.
 
         The commands stdout/err will be piped directly to autopkgtest and its log
         files, unless redirection happens with the stdout/stderr arguments
         (passed to Popen).
 
         Return (exit code, stdout, stderr). stdout/err will be None when output
@@ -491,15 +483,15 @@
 
         if proc.returncode in (254, 255):
             self.command('auxverb_debug_fail')
             self.bomb('testbed auxverb failed with exit code %i' % proc.returncode)
 
         return (proc.returncode, out, err)
 
-    def check_exec(self, argv, stdout=False, kind='install'):
+    def check_exec(self, argv, stdout=False, kind='short'):
         '''Run argv in testbed.
 
         If stdout is True, capture stdout and return it. Otherwise, don't
         redirect and return None.
 
         argv must succeed and not print any stderr.
         '''
```

### Comparing `reprotest-0.7.25/reprotest/lib/adtlog.py` & `reprotest-0.7.8/reprotest/lib/adtlog.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/lib/system_interface/__init__.py` & `reprotest-0.7.8/reprotest/lib/system_interface/__init__.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/lib/system_interface/arch.py` & `reprotest-0.7.8/reprotest/lib/system_interface/arch.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/lib/system_interface/debian.py` & `reprotest-0.7.8/reprotest/lib/system_interface/debian.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/mdiffconf.py` & `reprotest-0.7.8/reprotest/mdiffconf.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/presets.py` & `reprotest-0.7.8/reprotest/presets.py`

 * *Files 18% similar despite different names*

```diff
@@ -59,85 +59,46 @@
     @property
     def re_replace(self):
         """Do a regex-replace on the given attribute."""
         return AttributeFunctor(self, lambda s, pattern, repl, **kwargs: re.sub(pattern, repl, s, **kwargs))
 
 
 PRESET_DEB_DIR = ReprotestPreset(
-    build_command='dpkg-buildpackage --no-sign -b',
-    artifact_pattern='../*.*deb',
-    testbed_pre=None,
-    testbed_init=None,
-    testbed_build_pre=None,
-    source_pattern=None,
-    diffoscope_args=[],
+    build_command = 'dpkg-buildpackage --no-sign -b',
+    artifact_pattern = '../*.deb',
+    testbed_pre = None,
+    testbed_init = None,
+    testbed_build_pre = None,
+    source_pattern = None,
+    diffoscope_args = [],
 )
 
-PRESET_RPM_DIR = ReprotestPreset(
-    build_command='rpmbuild --rebuild',
-    artifact_pattern='rpmbuild/RPMS/*.rpm',
-    testbed_pre=None,
-    testbed_init=None,
-    testbed_build_pre=None,
-    source_pattern='*.src.rpm',
-    diffoscope_args=[],
-)
-
-
-# DEB
 def preset_deb_schroot(fn, preset):
     return preset.set.testbed_init(
         # need to symlink /etc/mtab to work around a fusermount(1) deficiency
         'apt-get -y --no-install-recommends install disorderfs fakeroot faketime locales-all sudo util-linux; \
         test -c /dev/fuse || mknod -m 666 /dev/fuse c 10 229; \
         test -f /etc/mtab || ln -s ../proc/self/mounts /etc/mtab'
     ).set.testbed_build_pre(
         'apt-get -y --no-install-recommends build-dep ./"%s"' % fn)
 
-
-def preset_deb_dsc(fn, aux):
-    # we use "$(basename "$PWD")" so that the dirname varies iff we are varying the whole build path
-    return PRESET_DEB_DIR.prepend.build_command(
-            'dpkg-source -x "%s" "$(basename "$PWD")" && cd "$(basename "$PWD")" && ' % fn
-        ).set.artifact_pattern("*.*deb"
-        ).set.source_pattern(" ".join(shlex.quote(a) for a in [fn] + aux))
-
-
 def parse_dsc_aux(path):
     dscfiles = subprocess.check_output(["egrep",
         # this regex comes from dcmd(1) from the devscripts package
         r"^ [0-9a-f]{32} [0-9]+ ((([a-zA-Z0-9_.-]+/)?[a-zA-Z0-9_.-]+|-) ([a-zA-Z]+|-) )?(.*)$",
         path])
     return [x.split()[-1].decode("utf-8") for x in dscfiles.splitlines()]
 
+def preset_deb_dsc(fn, aux):
+    # we use "$(basename "$PWD")" so that the dirname varies iff we are varying the whole build path
+    return PRESET_DEB_DIR.prepend.build_command(
+            'dpkg-source -x "%s" "$(basename "$PWD")" && cd "$(basename "$PWD")" && ' % fn
+        ).set.artifact_pattern("*.deb"
+        ).set.source_pattern(" ".join(shlex.quote(a) for a in [fn] + aux))
 
-# RPM
-def preset_rpm_rpmbuild(fn):
-    # We ensure to have generated RPMs into temporary HOME folder and not in
-    # rpmbuild/RPMS/%%{ARCH}/
-    extra_build_command = [
-        '--define "_build_name_fmt %%{NAME}-%%{VERSION}-%%{RELEASE}.%%{ARCH}.rpm"',
-        '--define "_topdir $PWD/rpmbuild"',
-        '%s' % fn
-        ]
-
-    # rpmbuild needs to be told to use reproducible specific options
-    extra_build_command += ['--define "source_date_epoch_from_changelog Y"']
-    extra_build_command += ['--define "clamp_mtime_to_source_date_epoch Y"']
-    extra_build_command += ['--define "use_source_date_epoch_as_buildtime Y"']
-
-    # Disable %clean stage: workaround issue when running with +fileordering
-    extra_build_command += ['--noclean']
-    extra_build_command += ['; rm -rf $PWD/rpmbuild/BUILD*']
-
-    extra_build_command = ' '.join(extra_build_command)
-    return PRESET_RPM_DIR.append.build_command(' %s' % extra_build_command)
-
-
-###
 def get_presets(buildfile, virtual_server):
     fn = os.path.basename(buildfile)
     parts = os.path.splitext(fn)
     if os.path.isdir(buildfile):
         if os.path.isdir(os.path.join(buildfile, "debian")):
             if virtual_server == "null":
                 return PRESET_DEB_DIR
@@ -145,16 +106,9 @@
                 return preset_deb_schroot(".", PRESET_DEB_DIR)
     elif os.path.isfile(buildfile):
         if parts[1] == '.dsc':
             if virtual_server == "null":
                 return preset_deb_dsc(fn, parse_dsc_aux(buildfile))
             else:
                 return preset_deb_schroot(fn, preset_deb_dsc(fn, parse_dsc_aux(buildfile)))
-        elif parts[1] == '.rpm':
-            if os.path.splitext(parts[0])[1] != '.src':
-                raise ValueError('cannot determine .src.rpm')
-            if virtual_server == "null":
-                return preset_rpm_rpmbuild(fn)
-            else:
-                raise ValueError("only 'null' virtual_server is currently available for source RPM")
     raise ValueError('unrecognised file type: "%s"; try giving '
                      'an appropriate --build-command' % buildfile)
```

### Comparing `reprotest-0.7.25/reprotest/shell_syn.py` & `reprotest-0.7.8/reprotest/shell_syn.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/utils.py` & `reprotest-0.7.8/reprotest/utils.py`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-chroot` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-chroot`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-lxc` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-lxc`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-lxd` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-lxd`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-null` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-null`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-qemu` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-qemu`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-schroot` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-schroot`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest/virt/autopkgtest-virt-ssh` & `reprotest-0.7.8/reprotest/virt/autopkgtest-virt-ssh`

 * *Files identical despite different names*

### Comparing `reprotest-0.7.25/reprotest.egg-info/PKG-INFO` & `reprotest-0.7.8/reprotest.egg-info/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,446 +1,419 @@
-Metadata-Version: 2.1
+Metadata-Version: 1.1
 Name: reprotest
-Version: 0.7.25
+Version: 0.7.8
 Summary: Build packages and check them for reproducibility.
 Home-page: https://salsa.debian.org/reproducible-builds/reprotest
 Author: Ximin Luo, Ceridwen
 Author-email: infinity0@debian.org, ceridwenv@gmail.com
 License: GPL-3+
+Description: reprotest
+        =========
+        
+        reprotest builds the same source code twice in different environments, and then
+        checks the binaries produced by each build for differences. If any are found,
+        then ``diffoscope(1)`` (or if unavailable then ``diff(1)``) is used to display
+        them in detail for later analysis.
+        
+        See the ``COMMAND-LINE EXAMPLES`` section further below to get you
+        started, as well as more detailed explanations of all the command-line
+        options. The same information is also available in
+        ``/usr/share/doc/reprotest/README.rst`` or similar.
+        
+        .. raw:: manpage
+        
+           .\" the below hack gets rid of the python "usage" message in favour of the
+           .\" the synopsis we manually defined in doc/$(PACKAGE).h2m.0
+           .SS positional arguments:
+           .\" end_of_description_header
+        
+        Command-line examples
+        =====================
+        
+        The easiest way to run reprotest is via our presets::
+        
+            # Build the current directory in a null server (/tmp)
+            $ reprotest .
+            $ reprotest . -vv -- null -d # for very verbose output
+        
+            # Build the given Debian source package in an schroot
+            # See https://wiki.debian.org/sbuild for instructions on setting that up.
+            $ reprotest reprotest_0.3.3.dsc -- schroot unstable-amd64-sbuild
+        
+        Currently, we only support this for Debian packages, but are keen on
+        adding more. If we don't have knowledge on how to build your file or
+        directory, you can send a patch to us on adding this intelligence - see
+        the reprotest.presets python module, and adapt the existing logic.
+        
+        In the meantime, you can use other parts of the CLI to build arbitrary things.
+        You'll need to give two mandatory arguments, the build command to run and the
+        build artifact file/pattern to test after running the build. For example::
+        
+            $ reprotest 'python3 setup.py bdist' 'dist/*.tar.gz'
+        
+        This runs the command on ``.``, the current working directory. To run it on a
+        project located elsewhere::
+        
+            $ reprotest -s ../path/to/other/project 'python3 setup.py bdist' 'dist/*.tar.gz'
+            $ reprotest -c 'python3 setup.py bdist' ../path/to/other/project 'dist/*.tar.gz'
+        
+        These two invocations are equivalent; you can pick the most convenient one
+        for your use-case. When using these from a shell:
+        
+          * If the build command has spaces, you will need to quote them, e.g.
+            ``reprotest "dpkg-buildpackage -b --no-sign" [..]``.
+        
+          * If you want to use several build artifact patterns, or if you want to
+            use shell wildcards as a pattern, you will also need to quote them, e.g.
+            ``reprotest [..] "*.tar.gz *.tar.xz"``.
+        
+          * If your build artifacts have spaces in their names, you will need to
+            quote these twice, e.g. ``'"a file with spaces.gz"'`` for a single
+            artifact or ``'"dir 1"/* "dir 2"/*'`` for multiple patterns.
+        
+        To get more help for the CLI, including documentation on optional
+        arguments and what they do, run::
+        
+            $ reprotest --help
+        
+        
+        Running in a virtual server
+        ===========================
+        
+        You can also run the build inside what is called a "virtual server".
+        This could be a container, a chroot, etc. You run them like this::
+        
+            $ reprotest 'python3 setup.py bdist_wheel'   'dist/*.whl' -- qemu    /path/to/qemu.img
+            $ reprotest 'dpkg-buildpackage -b --no-sign' '../*.deb'   -- schroot unstable-amd64
+        
+        There are different server types available. See ``--help`` for a list of
+        them, which appears near the top, in the "virtual\_server\_args" part of
+        the "positional arguments" section.
+        
+        For each virtual server (e.g. "schroot"), you see which extra arguments
+        it supports::
+        
+            $ reprotest --help schroot
+        
+        When running builds inside a virtual server, you will probably have to
+        give extra commands, in order to set up your build dependencies inside
+        the virtual server. For example, to take you through what the "Debian
+        directory" preset would look like, if we ran it using the full CLI::
+        
+            # "Debian directory" preset
+            $ reprotest . -- schroot unstable-amd64-sbuild
+            # This is exactly equivalent to this:
+            $ reprotest -c auto . -- schroot unstable-amd64-sbuild
+            # In the non-preset full CLI, this is roughly similar to:
+            $ reprotest \
+                --testbed-init 'apt-get -y --no-install-recommends install \
+                                disorderfs faketime locales-all sudo util-linux; \
+                                test -c /dev/fuse || mknod -m 666 /dev/fuse c 10 229; \
+                                test -f /etc/mtab || ln -s ../proc/self/mounts /etc/mtab' \
+                --testbed-build-pre 'apt-get -y --no-install-recommends build-dep ./' \
+                --build-command 'dpkg-buildpackage --no-sign -b' \
+                . \
+                '../*.deb' \
+                -- \
+                schroot unstable-amd64-sbuild
+        
+        The ``--testbed-init`` argument is needed to set up basic tools, which
+        reprotest needs in order to make the variations in the first place. This
+        should be the same regardless of what package is being built, but might
+        differ depending on what virtual\_server is being used.
+        
+        Next, we have ``--testbed-build-pre``, then ``--build-command`` (or ``-c``).
+        For our Debian directory, we install build-dependencies using ``apt-get``,
+        then we run the actual build command itself using ``dpkg-buildpackage(1)``.
+        
+        Then, we have the ``source_root`` and the ``artifact_pattern``. For
+        reproducibility, we're only interested in the binary packages.
+        
+        Finally, we specify that this is to take place in the "schroot"
+        virtual\_server with arguments "unstable-amd64-sbuild".
+        
+        Of course, all of this is a burden to remember, if you must run the same
+        thing many times. So that is why adding new presets for new package types
+        would be good.
+        
+        Here is a more complex example. It tells reprotest to store the build products
+        into ``./artifacts`` to analyse later; and also tweaks the "Debian dsc" preset
+        so that it uses our `experimental toolchain
+        <https://wiki.debian.org/ReproducibleBuilds/ExperimentalToolchain>`__::
+        
+            $ reprotest --store-dir=artifacts \
+                --auto-preset-expr '_.prepend.testbed_init("apt-get install -y wget; \
+                    echo deb http://reproducible.alioth.debian.org/debian/ ./ >> /etc/apt/sources.list; \
+                    wget -q -O- https://reproducible.alioth.debian.org/reproducible.asc | apt-key add -; \
+                    apt-get update; apt-get upgrade -y; ")' \
+                ./bash_4.4-4.0~reproducible1.dsc \
+                -- \
+                schroot unstable-amd64-sbuild
+        
+        Alternatively, you can clone your unstable-amd64-sbuild chroot, add our repo to
+        the cloned chroot, then use this chroot in place of "unstable-amd64-sbuild".
+        That would allow you to omit the long ``--auto-preset-expr`` flag above.
+        
+        
+        Config File
+        ===========
+        
+        You can also give options to reprotest via a config file. This is a
+        time-saving measure similar to ``auto`` presets; the difference is that
+        these are more suited for local builds that are suited to your personal
+        purposes. (You may use both presets and config files in the same build.)
+        
+        The config file takes exactly the same options as the command-line interface,
+        but with the additional restriction that the section name must match the ones
+        given in the --help output. Whitespace is allowed if and only if the same
+        command-line option allows whitespace. Finally, it is not possible to give
+        positional arguments via this mechanism.
+        
+        Reprotest by default does not load any config file. You can tell it to load one
+        with the ``--config-file`` or ``-f`` command line options. If you give it a
+        directory such as ``.``, it will load ``.reprotestrc`` within that directory.
+        
+        A sample config file is below::
+        
+            [basics]
+            verbosity = 1
+            variations =
+              environment
+              build_path
+              user_group.available+=builduser:builduser
+              fileordering
+              home
+              kernel
+              locales
+              exec_path
+              time
+              timezone
+              umask
+            store_dir =
+              /home/foo/build/reprotest-artifacts
+        
+            [diff]
+            diffoscope_arg =
+              --debug
+        
+        
+        Analysing diff output
+        =====================
+        
+        Normally when diffoscope compares directories, it also compares the metadata of
+        files in those directories - file permissions, owners, and so on.
+        
+        However depending on the circumstance, this filesystem-level metadata may or
+        may not be intended to be distributed to other systems. For example: (1) for
+        most distros' package builders, we don't care about the metadata of the output
+        package files; only the file contents will be distributed to other systems. On
+        the other hand, (2) when running something like `make install`, we *do* care
+        about the metadata, because this is what will be recreated on another system.
+        
+        In developing reprotest, our experience has been that case (1) is more common
+        and so we pass ``--exclude-directory-metadata`` by default to diffoscope. If
+        you find that you are using reprotest for case (2) then you should pass
+        ``--diffoscope-args=--no-exclude-directory-metadata`` to reprotest, to tell
+        diffoscope to not ignore the metadata since it will be distributed and should
+        therefore be reproducible. Otherwise, you may get a false-positive result.
+        
+        
+        Variations
+        ==========
+        
+        The --vary and --variations flags in their simple forms, are a comma-separated
+        list of variation names that indicate which variations to apply. The full list
+        of names is given in the --help text for --variations.
+        
+        | \
+        | In full detail, the flags are a comma-separated list of actions, as follows:
+        |
+        | +$variation (or $variation with no explicit operator)
+        | -$variation
+        |    Enable or disable a variation
+        |
+        | @$variation
+        |    Enable a variation, resetting its parameters (see below) to default values.
+        |
+        | $variation.$param=$value
+        | $variation.$param+=$value
+        | $variation.$param-=$value
+        |    Set/add/remove $value as/to/from the current value of the $param parameter
+             of the $variation.
+        |
+        | $variation.$param++
+        | $variation.$param--
+        |    Increment/decrement the value of the $param parameter of the $variation.
+        
+        Most variations do not have parameters, and for them only the + and - operators
+        are relevant. The variations that accept parameters are:
+        
+        domain_host.use_sudo
+            An integer, whether to use sudo(1) together with unshare(1) to change the
+            system hostname and domainname. 0 means don't use sudo; any non-zero value
+            means to use sudo. Default is 0, however this is not recommended and make
+            may your build fail, see "Varying the domain and host names" for details.
+        environment.variables
+            A semicolon-separated ordered set, specifying environment variables that
+            reprotest should try to vary. Default is "REPROTEST_CAPTURE_ENVIRONMENT".
+            Supports regex-based syntax e.g.
+        
+            - PID=\\d{1,6}
+            - HOME=(/\\w{3,12}){1,4}
+            - (GO|PYTHON|)PATH=(/\\w{3,12}){1,4}(:(/\\w{3,12}){1,4}){0,4}
+        
+            Special cases:
+        
+            - $VARNAME= (empty RHS) to tell reprotest to delete the variable
+            - $VARNAME=.{0} to tell reprotest to actually set an empty value
+            - \\x2c and \\x3b to match or generate , and ; respectively.
+        user_group.available
+            A semicolon-separated ordered set, specifying the available user+group
+            combinations that reprotest can ``sudo(1)`` to. Default is empty, in which
+            case the variation is a no-op, and you'll see a warning about this. Each
+            user+group should be given in the form $user:$group where either component
+            can be omitted, or else if there is no colon then it is interpreted as only
+            a $user, with no $group variation.
+        time.faketimes
+            A semicolon-separated ordered set, specifying possible ``faketime(1)`` time
+            descriptors to use. Default is empty, in which case we randomly choose a
+            time: either now (if the latest file-modtime in ``source_root`` is older
+            than about half-a-year) or more than half-a-year in the future.
+        
+            Note that the clock continues to run during the build. It is possible for
+            ``faketime(1)`` to freeze it, but we don't yet support that yet; it has a
+            higher chance of causing your build to fail or misbehave.
+        
+        The difference between --vary and --variations is that the former appends onto
+        previous values but the latter resets them. Furthermore, the last value set for
+        --variations is treated as the zeroth --vary argument. For example::
+        
+            reprotest --vary=-user_group
+        
+        means to vary +all (the default value for --variations) and -user_group (the
+        given value for --vary), whereas::
+        
+            reprotest --variations=-all,locales --variations=home,time --vary=timezone --vary=-time
+        
+        means to vary home, time (the last given value for --variations), timezone, and
+        -time (the given multiple values for --vary), i.e. home and timezone.
+        
+        
+        Notes on variations
+        ===================
+        
+        reprotest tries hard to perform variations without assuming it has full root
+        access to the system. It also assumes other software may be running on the same
+        system, so it does not perform system-level modifications that would affect
+        other processes. Due to these assumptions, some variations are implemented
+        using hacks at various levels of dirtiness, which are documented below.
+        
+        We will hopefully lift these assumptions for certain virtual_server contexts,
+        in future. That would likely allow for smoother operation in those contexts.
+        The assumptions will remain for the "null" (default) virtual_server however.
+        
+        Number of CPUs
+        --------------
+        
+        The control build uses only 1 CPU in order to try to reduce nondeterminism that
+        might exist due to multithreading or multiprocessing. If you are sure your
+        build is not affected by this (and good builds ought not to be), you can give
+        --min-cpus=99999 to use all available cores for both builds.
+        
+        Domain or host
+        --------------
+        
+        Doing this without sudo *may* result in your build failing.
+        
+        Failure is likely if your build must do system-related things - as opposed to
+        only processing bits and bytes. This is because it runs in a separate namespace
+        where your non-privileged user looks like it is "root", but this prevents the
+        filesystem from recognising files owned by the real "root" user, amongst other
+        things. This is a limitation of unshare(1) and it is not possible work around
+        this in reprotest without heavy effort.
+        
+        Therefore, it is recommended to run this variation with use_sudo=1. To avoid
+        password prompts, see the section "Avoid sudo(1) password prompts" below.
+        
+        When running inside a virtual-server:
+        
+        The non-sudo method fails with "Operation not permitted", even if you edited
+        ``/proc/sys/kernel/unprivileged_userns_clone``. The cause is currently unknown.
+        
+        The sudo method works only if you take measures to avoid sudo password prompts,
+        since containers don't have a method to input this.
+        
+        User or group
+        -------------
+        
+        If you also vary fileordering at the same time (this is the case by default),
+        each user you use needs to be in the "fuse" group. Do that by running `usermod
+        -aG fuse $OTHERUSER` as root.
+        
+        To avoid sudo(1) password prompts, see the section "Avoid sudo(1) password
+        prompts" below.
+        
+        Time
+        ----
+        
+        The "time" variation uses ``faketime(1)`` which *sometimes* causes weird and
+        hard-to-diagnose problems. In the past, this has included:
+        
+        - builds taking an infinite amount of time; though this should be fixed in
+          recent versions of reprotest.
+        
+        - builds with implausibly huge differences caused by ./configure scripts
+          producing different results with and without faketime. This still affects
+          bash and probably certain other packages using autotools.
+        
+        - builds accessing the network failing due to certificate expiration errors
+          and/or other time-related security errors. (Transparent builds of FOSS should
+          not access the network in the first place, but it's outside of reprotest's
+          scope to audit or prevent this.)
+        
+        If you see a difference that you really think should not be there, try passing
+        ``--variations=-time`` to reprotest, and/or check our results on
+        https://tests.reproducible-builds.org/ which use a different (more reliable)
+        mechanism to vary the system time.
+        
+        
+        Avoid sudo(1) password prompts
+        ==============================
+        
+        There is currently no good way to do this. The following is an EXPERIMENTAL
+        solution and is brittle and unclean. You will have to decide for yourself if
+        it's worth it for your use-case::
+        
+            $ reprotest --print-sudoers \
+                --variations=user_group.available+=guest-builder,domain_host.use_sudo=1 \
+                | sudo EDITOR=tee visudo -f /etc/sudoers.d/local-reprotest
+        
+        Make sure you set the variations you actually want to use. Obviously, don't
+        pick privileged users for this purpose, such as root.
+        
+        (Simplifying the output using wildcards, would open up passwordless access to
+        chown anything on your system, because wildcards here match whitespace. I don't
+        know what the sudo authors were thinking.)
+        
+        No, this is not nice at all - suggestions and patches welcome.
+        
+        If you want to use this in a virtual server such as a chroot, you'll need to
+        copy (or mount or otherwise map) the resulting sudoers file into your chroot.
+        
+        For example, for an schroot, you should (1) login to the source schroot and
+        create an empty file `/etc/sudoers.d/local-reprotest` (this is important) and
+        then (2) add the line:
+        
+            /etc/sudoers.d/local-reprotest  /etc/sudoers.d/local-reprotest  none bind 0 0
+        
+        to your schroot's fstab.
+        
+        
+Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.5
 Classifier: Topic :: Utilities
-Provides-Extra: compare
-
-reprotest
-=========
-
-reprotest builds the same source code twice in different environments, and then
-checks the binaries produced by each build for differences. If any are found,
-then ``diffoscope(1)`` (or if unavailable then ``diff(1)``) is used to display
-them in detail for later analysis.
-
-See the ``COMMAND-LINE EXAMPLES`` section further below to get you
-started, as well as more detailed explanations of all the command-line
-options. The same information is also available in
-``/usr/share/doc/reprotest/README.rst`` or similar.
-
-.. the below hack gets rid of the python "usage" message in favour of the
-   the synopsis we manually defined in doc/$(PACKAGE).h2m.0
-   .SS positional arguments:
-   .\" end_of_description_header
-
-Command-line examples
-=====================
-
-The easiest way to run reprotest is via our presets::
-
-    # Build the current directory in a null server (/tmp)
-    $ reprotest .
-    $ reprotest . -vv -- null -d # for very verbose output
-
-    # Build a make-based program
-    $ reprotest "make clean && make" mybinary
-
-    # Build a Debian package
-    $ apt-get source hello && cd hello-2.10
-    $ reprotest  auto -- null
-    # Build a Debian package and disable some variations
-    $ reprotest --vary=-user_group,-domain_host,-fileordering auto -- null
-
-    # Build the given Debian source package in an schroot
-    # See https://wiki.debian.org/sbuild for instructions on setting that up.
-    $ reprotest reprotest_0.3.3.dsc -- schroot unstable-amd64-sbuild
-
-    # Build the given RPM source package
-    # Only null server (/tmp) is currently supported.
-    $ reprotest reprotest-0.7.16.src.rpm
-
-    # Build the given RPM source package and automatically install dependencies
-    $ reprotest --testbed-build-pre 'dnf -y builddep ./*.src.rpm' reprotest-0.7.16.src.rpm
-
-Currently, we only support this for Debian and RPM based packages, but are keen on
-adding more. If we don't have knowledge on how to build your file or
-directory, you can send a patch to us on adding this intelligence - see
-the reprotest.presets python module, and adapt the existing logic.
-
-In the meantime, you can use other parts of the CLI to build arbitrary things.
-You'll need to give two mandatory arguments, the build command to run and the
-build artifact file/pattern to test after running the build. For example::
-
-    $ reprotest 'python3 setup.py bdist' 'dist/*.tar.gz'
-
-This runs the command on ``.``, the current working directory. To run it on a
-project located elsewhere::
-
-    $ reprotest -s ../path/to/other/project 'python3 setup.py bdist' 'dist/*.tar.gz'
-    $ reprotest -c 'python3 setup.py bdist' ../path/to/other/project 'dist/*.tar.gz'
-
-These two invocations are equivalent; you can pick the most convenient one
-for your use-case. When using these from a shell:
-
-  * If the build command has spaces, you will need to quote them, e.g.
-    ``reprotest "dpkg-buildpackage -b --no-sign" [..]``.
-
-  * If you want to use several build artifact patterns, or if you want to
-    use shell wildcards as a pattern, you will also need to quote them, e.g.
-    ``reprotest [..] "*.tar.gz *.tar.xz"``.
-
-  * If your build artifacts have spaces in their names, you will need to
-    quote these twice, e.g. ``'"a file with spaces.gz"'`` for a single
-    artifact or ``'"dir 1"/* "dir 2"/*'`` for multiple patterns.
-
-To get more help for the CLI, including documentation on optional
-arguments and what they do, run::
-
-    $ reprotest --help
-
-
-Running in a virtual server
-===========================
-
-You can also run the build inside what is called a "virtual server".
-This could be a container, a chroot, etc. You run them like this::
-
-    $ reprotest 'python3 setup.py bdist_wheel'   'dist/*.whl' -- qemu    /path/to/qemu.img
-    $ reprotest 'dpkg-buildpackage -b --no-sign' '../*.deb'   -- schroot unstable-amd64
-
-There are different server types available. See ``--help`` for a list of
-them, which appears near the top, in the "virtual\_server\_args" part of
-the "positional arguments" section.
-
-For each virtual server (e.g. "schroot"), you see which extra arguments
-it supports::
-
-    $ reprotest --help schroot
-
-When running builds inside a virtual server, you will probably have to
-give extra commands, in order to set up your build dependencies inside
-the virtual server. For example, to take you through what the "Debian
-directory" preset would look like, if we ran it using the full CLI::
-
-    # "Debian directory" preset
-    $ reprotest . -- schroot unstable-amd64-sbuild
-    # This is exactly equivalent to this:
-    $ reprotest -c auto . -- schroot unstable-amd64-sbuild
-    # In the non-preset full CLI, this is roughly similar to:
-    $ reprotest \
-        --testbed-init 'apt-get -y --no-install-recommends install \
-                        disorderfs faketime locales-all sudo util-linux; \
-                        test -c /dev/fuse || mknod -m 666 /dev/fuse c 10 229; \
-                        test -f /etc/mtab || ln -s ../proc/self/mounts /etc/mtab' \
-        --testbed-build-pre 'apt-get -y --no-install-recommends build-dep ./' \
-        --build-command 'dpkg-buildpackage --no-sign -b' \
-        . \
-        '../*.deb' \
-        -- \
-        schroot unstable-amd64-sbuild
-
-The ``--testbed-init`` argument is needed to set up basic tools, which
-reprotest needs in order to make the variations in the first place. This
-should be the same regardless of what package is being built, but might
-differ depending on what virtual\_server is being used.
-
-Next, we have ``--testbed-build-pre``, then ``--build-command`` (or ``-c``).
-For our Debian directory, we install build-dependencies using ``apt-get``,
-then we run the actual build command itself using ``dpkg-buildpackage(1)``.
-
-Then, we have the ``source_root`` and the ``artifact_pattern``. For
-reproducibility, we're only interested in the binary packages.
-
-Finally, we specify that this is to take place in the "schroot"
-virtual\_server with arguments "unstable-amd64-sbuild".
-
-Of course, all of this is a burden to remember, if you must run the same
-thing many times. So that is why adding new presets for new package types
-would be good.
-
-Here is a more complex example. It tells reprotest to store the build products
-into ``./artifacts`` to analyse later; and also tweaks the "Debian dsc" preset
-so that it uses our `experimental toolchain
-<https://wiki.debian.org/ReproducibleBuilds/ExperimentalToolchain>`__::
-
-    $ reprotest --store-dir=artifacts \
-        --auto-preset-expr '_.prepend.testbed_init("apt-get install -y wget; \
-            echo deb http://reproducible.alioth.debian.org/debian/ ./ >> /etc/apt/sources.list; \
-            wget -q -O- https://reproducible.alioth.debian.org/reproducible.asc | apt-key add -; \
-            apt-get update; apt-get upgrade -y; ")' \
-        ./bash_4.4-4.0~reproducible1.dsc \
-        -- \
-        schroot unstable-amd64-sbuild
-
-Alternatively, you can clone your unstable-amd64-sbuild chroot, add our repo to
-the cloned chroot, then use this chroot in place of "unstable-amd64-sbuild".
-That would allow you to omit the long ``--auto-preset-expr`` flag above.
-
-
-Config File
-===========
-
-You can also give options to reprotest via a config file. This is a
-time-saving measure similar to ``auto`` presets; the difference is that
-these are more suited for local builds that are suited to your personal
-purposes. (You may use both presets and config files in the same build.)
-
-The config file takes exactly the same options as the command-line interface,
-but with the additional restriction that the section name must match the ones
-given in the --help output. Whitespace is allowed if and only if the same
-command-line option allows whitespace. Finally, it is not possible to give
-positional arguments via this mechanism.
-
-Reprotest by default does not load any config file. You can tell it to load one
-with the ``--config-file`` or ``-f`` command line options. If you give it a
-directory such as ``.``, it will load ``.reprotestrc`` within that directory.
-
-A sample config file is below::
-
-    [basics]
-    verbosity = 1
-    variations =
-      environment
-      build_path
-      user_group.available+=builduser:builduser
-      fileordering
-      home
-      kernel
-      locales
-      exec_path
-      time
-      timezone
-      umask
-    store_dir =
-      /home/foo/build/reprotest-artifacts
-
-    [diff]
-    diffoscope_arg =
-      --debug
-
-
-Analysing diff output
-=====================
-
-Normally when diffoscope compares directories, it also compares the metadata of
-files in those directories - file permissions, owners, and so on.
-
-However depending on the circumstance, this filesystem-level metadata may or
-may not be intended to be distributed to other systems. For example: (1) for
-most distros' package builders, we don't care about the metadata of the output
-package files; only the file contents will be distributed to other systems. On
-the other hand, (2) when running something like `make install`, we *do* care
-about the metadata, because this is what will be recreated on another system.
-
-In developing reprotest, our experience has been that case (1) is more common
-and so we pass ``--exclude-directory-metadata=yes`` by default to diffoscope. If
-you find that you are using reprotest for case (2) then you should pass
-``--diffoscope-args=--exclude-directory-metadata=no`` to reprotest, to tell
-diffoscope to not ignore the metadata since it will be distributed and should
-therefore be reproducible. Otherwise, you may get a false-positive result.
-
-
-Variations
-==========
-
-The --vary and --variations flags in their simple forms, are a comma-separated
-list of variation names that indicate which variations to apply. The full list
-of names is given in the --help text for --variations.
-
-| \
-| In full detail, the flags are a comma-separated list of actions, as follows:
-|
-| +$variation (or $variation with no explicit operator)
-| -$variation
-|    Enable or disable a variation
-|
-| @$variation
-|    Enable a variation, resetting its parameters (see below) to default values.
-|
-| $variation.$param=$value
-| $variation.$param+=$value
-| $variation.$param-=$value
-|    Set/add/remove $value as/to/from the current value of the $param parameter
-     of the $variation.
-|
-| $variation.$param++
-| $variation.$param--
-|    Increment/decrement the value of the $param parameter of the $variation.
-
-Most variations do not have parameters, and for them only the + and - operators
-are relevant. The variations that accept parameters are:
-
-domain_host.use_sudo
-    An integer, whether to use sudo(1) together with unshare(1) to change the
-    system hostname and domainname. 0 means don't use sudo; any non-zero value
-    means to use sudo. Default is 0, however this is not recommended and make
-    may your build fail, see "Varying the domain and host names" for details.
-environment.variables
-    A semicolon-separated ordered set, specifying environment variables that
-    reprotest should try to vary. Default is "REPROTEST_CAPTURE_ENVIRONMENT".
-    Supports regex-based syntax e.g.
-
-    - PID=\\d{1,6}
-    - HOME=(/\\w{3,12}){1,4}
-    - (GO|PYTHON|)PATH=(/\\w{3,12}){1,4}(:(/\\w{3,12}){1,4}){0,4}
-
-    Special cases:
-
-    - $VARNAME= (empty RHS) to tell reprotest to delete the variable
-    - $VARNAME=.{0} to tell reprotest to actually set an empty value
-    - \\x2c and \\x3b to match or generate , and ; respectively.
-user_group.available
-    A semicolon-separated ordered set, specifying the available user+group
-    combinations that reprotest can ``sudo(1)`` to. Default is empty, in which
-    case the variation is a no-op, and you'll see a warning about this. Each
-    user+group should be given in the form $user:$group where either component
-    can be omitted, or else if there is no colon then it is interpreted as only
-    a $user, with no $group variation.
-time.faketimes
-    A semicolon-separated ordered set, specifying possible ``faketime(1)`` time
-    descriptors to use. Default is empty, in which case we randomly choose a
-    time: either now (if the latest file-modtime in ``source_root`` is older
-    than about half-a-year) or more than half-a-year in the future.
-
-    Note that the clock continues to run during the build. It is possible for
-    ``faketime(1)`` to freeze it, but we don't yet support that yet; it has a
-    higher chance of causing your build to fail or misbehave.
-locales.locale
-    A semicolon-separated list one or more locales to test when
-    performing locales variations.
-    If multiple locales are specified, one will be chosen at random.
-    Locales with different properties than en_US.UTF-8 are fr_CH.UTF-8,
-    ru_RU.CP1251, kk_KZ.RK1048 or zh_CN.
-    Default is et_EE.UTF-8 if unspecified.
-
-The difference between --vary and --variations is that the former appends onto
-previous values but the latter resets them. Furthermore, the last value set for
---variations is treated as the zeroth --vary argument. For example::
-
-    reprotest --vary=-user_group
-
-means to vary +all (the default value for --variations) and -user_group (the
-given value for --vary), whereas::
-
-    reprotest --variations=-all,locales --variations=home,time --vary=timezone --vary=-time
-
-means to vary home, time (the last given value for --variations), timezone, and
--time (the given multiple values for --vary), i.e. home and timezone.
-
-
-Notes on variations
-===================
-
-reprotest tries hard to perform variations without assuming it has full root
-access to the system. It also assumes other software may be running on the same
-system, so it does not perform system-level modifications that would affect
-other processes. Due to these assumptions, some variations are implemented
-using hacks at various levels of dirtiness, which are documented below.
-
-We will hopefully lift these assumptions for certain virtual_server contexts,
-in future. That would likely allow for smoother operation in those contexts.
-The assumptions will remain for the "null" (default) virtual_server however.
-
-Number of CPUs
---------------
-
-The control build uses only 1 CPU in order to try to reduce nondeterminism that
-might exist due to multithreading or multiprocessing. If you are sure your
-build is not affected by this (and good builds ought not to be), you can give
---min-cpus=99999 to use all available cores for both builds.
-
-Domain or host
---------------
-
-Doing this without sudo *may* result in your build failing.
-
-Failure is likely if your build must do system-related things - as opposed to
-only processing bits and bytes. This is because it runs in a separate namespace
-where your non-privileged user looks like it is "root", but this prevents the
-filesystem from recognising files owned by the real "root" user, amongst other
-things. This is a limitation of unshare(1) and it is not possible work around
-this in reprotest without heavy effort.
-
-Therefore, it is recommended to run this variation with use_sudo=1. To avoid
-password prompts, see the section "Avoid sudo(1) password prompts" below.
-
-When running inside a virtual-server:
-
-The non-sudo method fails with "Operation not permitted", even if you edited
-``/proc/sys/kernel/unprivileged_userns_clone``. The cause is currently unknown.
-
-The sudo method works only if you take measures to avoid sudo password prompts,
-since containers don't have a method to input this.
-
-User or group
--------------
-
-If you also vary fileordering at the same time (this is the case by default),
-each user you use needs to be in the "fuse" group. Do that by running `usermod
--aG fuse $OTHERUSER` as root.
-
-To avoid sudo(1) password prompts, see the section "Avoid sudo(1) password
-prompts" below.
-
-Time
-----
-
-The "time" variation uses ``faketime(1)`` which *sometimes* causes weird and
-hard-to-diagnose problems. In the past, this has included:
-
-- builds taking an infinite amount of time; though this should be fixed in
-  recent versions of reprotest.
-
-- builds with implausibly huge differences caused by ./configure scripts
-  producing different results with and without faketime. This still affects
-  bash and probably certain other packages using autotools.
-
-- builds accessing the network failing due to certificate expiration errors
-  and/or other time-related security errors. (Transparent builds of FOSS should
-  not access the network in the first place, but it's outside of reprotest's
-  scope to audit or prevent this.)
-
-If you see a difference that you really think should not be there, try passing
-``--variations=-time`` to reprotest, and/or check our results on
-https://tests.reproducible-builds.org/ which use a different (more reliable)
-mechanism to vary the system time.
-
-Kernel
-------
-
-The "kernel" variation is currently not working for RPM based packages and other
-build process requiring `ldconfig`.  While building with this variation enabled,
-`ldconfig` complains about `FATAL: kernel too old` and aborts the build.
-
-Avoid sudo(1) password prompts
-==============================
-
-There is currently no good way to do this. The following is an EXPERIMENTAL
-solution and is brittle and unclean. You will have to decide for yourself if
-it's worth it for your use-case::
-
-    $ reprotest --print-sudoers \
-        --variations=user_group.available+=guest-builder,domain_host.use_sudo=1 \
-        | sudo EDITOR=tee visudo -f /etc/sudoers.d/local-reprotest
-
-Make sure you set the variations you actually want to use. Obviously, don't
-pick privileged users for this purpose, such as root.
-
-(Simplifying the output using wildcards, would open up passwordless access to
-chown anything on your system, because wildcards here match whitespace. I don't
-know what the sudo authors were thinking.)
-
-No, this is not nice at all - suggestions and patches welcome.
-
-If you want to use this in a virtual server such as a chroot, you'll need to
-copy (or mount or otherwise map) the resulting sudoers file into your chroot.
-
-For example, for an schroot, you should (1) login to the source schroot and
-create an empty file `/etc/sudoers.d/local-reprotest` (this is important) and
-then (2) add the line:
-
-    /etc/sudoers.d/local-reprotest  /etc/sudoers.d/local-reprotest  none bind 0 0
-
-to your schroot's fstab.
-
```

### Comparing `reprotest-0.7.25/setup.py` & `reprotest-0.7.8/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -2,40 +2,38 @@
 
 # Licensed under the GPL: https://www.gnu.org/licenses/gpl-3.0.en.html
 # For details: reprotest/debian/copyright
 
 from setuptools import setup, find_packages
 
 setup(name='reprotest',
-      version='0.7.25',
+      version='0.7.8',
       description='Build packages and check them for reproducibility.',
       long_description=open('README.rst', encoding='utf-8').read(),
       author='Ximin Luo, Ceridwen',
       author_email='infinity0@debian.org, ceridwenv@gmail.com',
       license='GPL-3+',
       url='https://salsa.debian.org/reproducible-builds/reprotest',
       packages=find_packages(),
       entry_points={
           'console_scripts': [
               'reprotest = reprotest:main'
               ],
           },
       install_requires=[
+          'diffoscope',
           'rstr',
           'distro',
           ],
-      extras_require={
-          'compare': ['diffoscope>=112'],
-          },
       classifiers=[
           'Development Status :: 3 - Alpha',
           'Intended Audience :: Developers',
           'License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)',
           'Operating System :: POSIX',
           'Programming Language :: Python',
           'Programming Language :: Python :: 3',
-          'Programming Language :: Python :: 3.9',
+          'Programming Language :: Python :: 3.5',
           'Topic :: Utilities',
           ],
       zip_safe=False,
       include_package_data=True
       )
```

