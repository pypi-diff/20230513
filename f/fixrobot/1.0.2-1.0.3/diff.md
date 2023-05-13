# Comparing `tmp/fixrobot-1.0.2.tar.gz` & `tmp/fixrobot-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fixrobot-1.0.2.tar", last modified: Sat May 13 13:54:42 2023, max compression
+gzip compressed data, was "fixrobot-1.0.3.tar", last modified: Sat May 13 14:03:19 2023, max compression
```

## Comparing `fixrobot-1.0.2.tar` & `fixrobot-1.0.3.tar`

### file list

```diff
@@ -1,94 +1,94 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.678863 fixrobot-1.0.2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.666863 fixrobot-1.0.2/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.670863 fixrobot-1.0.2/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.github/workflows/github-actions.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      430 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.github/workflows/publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.gitignore
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.670863 fixrobot-1.0.2/.idea/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      441 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/FIXRobot.iml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.670863 fixrobot-1.0.2/.idea/inspectionProfiles/
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/inspectionProfiles/profiles_settings.xml
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/misc.xml
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/modules.xml
--rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-13 13:54:34.000000 fixrobot-1.0.2/.idea/vcs.xml
--rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-05-13 13:54:34.000000 fixrobot-1.0.2/INSTALL
--rw-r--r--   0 runner    (1001) docker     (123)    34989 2023-05-13 13:54:34.000000 fixrobot-1.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 13:54:34.000000 fixrobot-1.0.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 13:54:42.678863 fixrobot-1.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2754 2023-05-13 13:54:34.000000 fixrobot-1.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:34.000000 fixrobot-1.0.2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 13:54:34.000000 fixrobot-1.0.2/desktop.ini
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.670863 fixrobot-1.0.2/docs/
--rw-r--r--   0 runner    (1001) docker     (123)    31596 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/FIXRobot.html
--rw-r--r--   0 runner    (1001) docker     (123)    24073 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/FIXRobot.tests.html
--rw-r--r--   0 runner    (1001) docker     (123)      683 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     3992 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/README.html
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/generate_doc.sh
--rw-r--r--   0 runner    (1001) docker     (123)    22149 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/genindex.html
--rw-r--r--   0 runner    (1001) docker     (123)     4805 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     4527 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/modules.html
--rw-r--r--   0 runner    (1001) docker     (123)     1002 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/objects.inv
--rw-r--r--   0 runner    (1001) docker     (123)     4632 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/py-modindex.html
--rw-r--r--   0 runner    (1001) docker     (123)     3082 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/search.html
--rw-r--r--   0 runner    (1001) docker     (123)     8267 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/searchindex.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.670863 fixrobot-1.0.2/docs/source/
--rw-r--r--   0 runner    (1001) docker     (123)      378 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/FIXRobot.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1114 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/FIXRobot.tests.rst
--rw-r--r--   0 runner    (1001) docker     (123)      816 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5109 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)       61 2023-05-13 13:54:34.000000 fixrobot-1.0.2/docs/source/modules.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.674863 fixrobot-1.0.2/env/
--rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/CLIENT-EXECUTOR-FIX42.ini
--rw-r--r--   0 runner    (1001) docker     (123)      661 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/CLIENT-EXECUTOR-FIX50.ini
--rw-r--r--   0 runner    (1001) docker     (123)     8255 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/DEFAULTMESSAGES.ini
--rw-r--r--   0 runner    (1001) docker     (123)      549 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/EXECUTOR-CLIENT-FIX42.ini
--rw-r--r--   0 runner    (1001) docker     (123)      654 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/EXECUTOR-CLIENT-FIX50.ini
--rw-r--r--   0 runner    (1001) docker     (123)      175 2023-05-13 13:54:34.000000 fixrobot-1.0.2/env/connections.ini
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.674863 fixrobot-1.0.2/fixrobot/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    64321 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/fixrobot.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.674863 fixrobot-1.0.2/fixrobot/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     6382 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/FIX42RobotUnitTest_ShouldFail.py
--rw-r--r--   0 runner    (1001) docker     (123)    24745 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/FIX42RobotUnitTest_ShouldPass.py
--rw-r--r--   0 runner    (1001) docker     (123)     6358 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/FIX50RobotUnitTest_ShouldFail.py
--rw-r--r--   0 runner    (1001) docker     (123)    24713 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/FIX50RobotUnitTest_ShouldPass.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3673 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runPyTest.bat
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runPyTest.sh
--rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runPyTestAll.bat
--rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runPyTestAll.sh
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runTest.bat
--rwxr-xr-x   0 runner    (1001) docker     (123)       81 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runTest.sh
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runTestAll.bat
--rwxr-xr-x   0 runner    (1001) docker     (123)      160 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/runTestAll.sh
--rw-r--r--   0 runner    (1001) docker     (123)     5376 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/test_FIX42RobotPyTest_ShouldFail.py
--rw-r--r--   0 runner    (1001) docker     (123)    24918 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/test_FIX42RobotPyTest_ShouldPass.py
--rw-r--r--   0 runner    (1001) docker     (123)     5376 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/test_FIX50RobotPyTest_ShouldFail.py
--rw-r--r--   0 runner    (1001) docker     (123)    25016 2023-05-13 13:54:34.000000 fixrobot-1.0.2/fixrobot/tests/test_FIX50RobotPyTest_ShouldPass.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.674863 fixrobot-1.0.2/fixrobot.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      519 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       61 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 13:54:42.000000 fixrobot-1.0.2/fixrobot.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      429 2023-05-13 13:54:34.000000 fixrobot-1.0.2/github_actions_requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 13:54:34.000000 fixrobot-1.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 13:54:34.000000 fixrobot-1.0.2/pytest.ini
--rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 13:54:34.000000 fixrobot-1.0.2/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      846 2023-05-13 13:54:42.678863 fixrobot-1.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     3499 2023-05-13 13:54:34.000000 fixrobot-1.0.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:42.678863 fixrobot-1.0.2/spec/
--rw-r--r--   0 runner    (1001) docker     (123)    38359 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX40.xml
--rw-r--r--   0 runner    (1001) docker     (123)    59730 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX41.xml
--rw-r--r--   0 runner    (1001) docker     (123)   132750 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX42.xml
--rw-r--r--   0 runner    (1001) docker     (123)   214212 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX43.xml
--rw-r--r--   0 runner    (1001) docker     (123)   326909 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX44.xml
--rw-r--r--   0 runner    (1001) docker     (123)   404345 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX50.xml
--rw-r--r--   0 runner    (1001) docker     (123)   477210 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX50SP1.xml
--rw-r--r--   0 runner    (1001) docker     (123)   504133 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIX50SP2.xml
--rw-r--r--   0 runner    (1001) docker     (123)    16458 2023-05-13 13:54:34.000000 fixrobot-1.0.2/spec/FIXT11.xml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.475640 fixrobot-1.0.3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.447640 fixrobot-1.0.3/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.455640 fixrobot-1.0.3/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.github/workflows/github-actions.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.github/workflows/publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1156 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.gitignore
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.455640 fixrobot-1.0.3/.idea/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      441 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/FIXRobot.iml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.455640 fixrobot-1.0.3/.idea/inspectionProfiles/
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/inspectionProfiles/profiles_settings.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/misc.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/modules.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      167 2023-05-13 14:03:10.000000 fixrobot-1.0.3/.idea/vcs.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-05-13 14:03:10.000000 fixrobot-1.0.3/INSTALL
+-rw-r--r--   0 runner    (1001) docker     (123)    34989 2023-05-13 14:03:10.000000 fixrobot-1.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-05-13 14:03:10.000000 fixrobot-1.0.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:03:19.475640 fixrobot-1.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2754 2023-05-13 14:03:10.000000 fixrobot-1.0.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:10.000000 fixrobot-1.0.3/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 14:03:10.000000 fixrobot-1.0.3/desktop.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.459640 fixrobot-1.0.3/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)    31596 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/FIXRobot.html
+-rw-r--r--   0 runner    (1001) docker     (123)    24073 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/FIXRobot.tests.html
+-rw-r--r--   0 runner    (1001) docker     (123)      683 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     3992 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/README.html
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/generate_doc.sh
+-rw-r--r--   0 runner    (1001) docker     (123)    22149 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/genindex.html
+-rw-r--r--   0 runner    (1001) docker     (123)     4805 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     4527 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/modules.html
+-rw-r--r--   0 runner    (1001) docker     (123)     1002 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/objects.inv
+-rw-r--r--   0 runner    (1001) docker     (123)     4632 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/py-modindex.html
+-rw-r--r--   0 runner    (1001) docker     (123)     3082 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/search.html
+-rw-r--r--   0 runner    (1001) docker     (123)     8267 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/searchindex.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.459640 fixrobot-1.0.3/docs/source/
+-rw-r--r--   0 runner    (1001) docker     (123)      378 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/FIXRobot.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1114 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/FIXRobot.tests.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      816 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/README.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5109 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       61 2023-05-13 14:03:10.000000 fixrobot-1.0.3/docs/source/modules.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.463640 fixrobot-1.0.3/env/
+-rw-r--r--   0 runner    (1001) docker     (123)      554 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/CLIENT-EXECUTOR-FIX42.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      661 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/CLIENT-EXECUTOR-FIX50.ini
+-rw-r--r--   0 runner    (1001) docker     (123)     8255 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/DEFAULTMESSAGES.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      549 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/EXECUTOR-CLIENT-FIX42.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      654 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/EXECUTOR-CLIENT-FIX50.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      175 2023-05-13 14:03:10.000000 fixrobot-1.0.3/env/connections.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.463640 fixrobot-1.0.3/fixrobot/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    64321 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/fixrobot.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.471640 fixrobot-1.0.3/fixrobot/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     6382 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/FIX42RobotUnitTest_ShouldFail.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24745 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/FIX42RobotUnitTest_ShouldPass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6358 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/FIX50RobotUnitTest_ShouldFail.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24713 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/FIX50RobotUnitTest_ShouldPass.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3673 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runPyTest.bat
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runPyTest.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runPyTestAll.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runPyTestAll.sh
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runTest.bat
+-rwxr-xr-x   0 runner    (1001) docker     (123)       81 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runTest.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runTestAll.bat
+-rwxr-xr-x   0 runner    (1001) docker     (123)      160 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/runTestAll.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     5376 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/test_FIX42RobotPyTest_ShouldFail.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24918 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/test_FIX42RobotPyTest_ShouldPass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5376 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/test_FIX50RobotPyTest_ShouldFail.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25016 2023-05-13 14:03:10.000000 fixrobot-1.0.3/fixrobot/tests/test_FIX50RobotPyTest_ShouldPass.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.463640 fixrobot-1.0.3/fixrobot.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       61 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-05-13 14:03:19.000000 fixrobot-1.0.3/fixrobot.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      429 2023-05-13 14:03:10.000000 fixrobot-1.0.3/github_actions_requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 14:03:10.000000 fixrobot-1.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      355 2023-05-13 14:03:10.000000 fixrobot-1.0.3/pytest.ini
+-rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-13 14:03:10.000000 fixrobot-1.0.3/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      846 2023-05-13 14:03:19.475640 fixrobot-1.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     3511 2023-05-13 14:03:10.000000 fixrobot-1.0.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:03:19.475640 fixrobot-1.0.3/spec/
+-rw-r--r--   0 runner    (1001) docker     (123)    38359 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX40.xml
+-rw-r--r--   0 runner    (1001) docker     (123)    59730 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX41.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   132750 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX42.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   214212 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX43.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   326909 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX44.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   404345 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX50.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   477210 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX50SP1.xml
+-rw-r--r--   0 runner    (1001) docker     (123)   504133 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIX50SP2.xml
+-rw-r--r--   0 runner    (1001) docker     (123)    16458 2023-05-13 14:03:10.000000 fixrobot-1.0.3/spec/FIXT11.xml
```

### Comparing `fixrobot-1.0.2/.github/workflows/github-actions.yaml` & `fixrobot-1.0.3/.github/workflows/github-actions.yaml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/.gitignore` & `fixrobot-1.0.3/.gitignore`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/INSTALL` & `fixrobot-1.0.3/INSTALL`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/LICENSE` & `fixrobot-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/README.md` & `fixrobot-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/FIXRobot.html` & `fixrobot-1.0.3/docs/FIXRobot.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/FIXRobot.tests.html` & `fixrobot-1.0.3/docs/FIXRobot.tests.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/Makefile` & `fixrobot-1.0.3/docs/Makefile`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/README.html` & `fixrobot-1.0.3/docs/README.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/genindex.html` & `fixrobot-1.0.3/docs/genindex.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/index.html` & `fixrobot-1.0.3/docs/index.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/modules.html` & `fixrobot-1.0.3/docs/modules.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/objects.inv` & `fixrobot-1.0.3/docs/objects.inv`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/py-modindex.html` & `fixrobot-1.0.3/docs/py-modindex.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/search.html` & `fixrobot-1.0.3/docs/search.html`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/searchindex.js` & `fixrobot-1.0.3/docs/searchindex.js`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/source/FIXRobot.tests.rst` & `fixrobot-1.0.3/docs/source/FIXRobot.tests.rst`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/source/README.rst` & `fixrobot-1.0.3/docs/source/README.rst`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/docs/source/conf.py` & `fixrobot-1.0.3/docs/source/conf.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/env/CLIENT-EXECUTOR-FIX42.ini` & `fixrobot-1.0.3/env/CLIENT-EXECUTOR-FIX42.ini`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/env/CLIENT-EXECUTOR-FIX50.ini` & `fixrobot-1.0.3/env/CLIENT-EXECUTOR-FIX50.ini`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/env/DEFAULTMESSAGES.ini` & `fixrobot-1.0.3/env/DEFAULTMESSAGES.ini`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/env/EXECUTOR-CLIENT-FIX42.ini` & `fixrobot-1.0.3/env/EXECUTOR-CLIENT-FIX42.ini`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/env/EXECUTOR-CLIENT-FIX50.ini` & `fixrobot-1.0.3/env/EXECUTOR-CLIENT-FIX50.ini`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/fixrobot.py` & `fixrobot-1.0.3/fixrobot/fixrobot.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/FIX42RobotUnitTest_ShouldFail.py` & `fixrobot-1.0.3/fixrobot/tests/FIX42RobotUnitTest_ShouldFail.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/FIX42RobotUnitTest_ShouldPass.py` & `fixrobot-1.0.3/fixrobot/tests/FIX42RobotUnitTest_ShouldPass.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/FIX50RobotUnitTest_ShouldFail.py` & `fixrobot-1.0.3/fixrobot/tests/FIX50RobotUnitTest_ShouldFail.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/FIX50RobotUnitTest_ShouldPass.py` & `fixrobot-1.0.3/fixrobot/tests/FIX50RobotUnitTest_ShouldPass.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/conftest.py` & `fixrobot-1.0.3/fixrobot/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/test_FIX42RobotPyTest_ShouldFail.py` & `fixrobot-1.0.3/fixrobot/tests/test_FIX42RobotPyTest_ShouldFail.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/test_FIX42RobotPyTest_ShouldPass.py` & `fixrobot-1.0.3/fixrobot/tests/test_FIX42RobotPyTest_ShouldPass.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/test_FIX50RobotPyTest_ShouldFail.py` & `fixrobot-1.0.3/fixrobot/tests/test_FIX50RobotPyTest_ShouldFail.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot/tests/test_FIX50RobotPyTest_ShouldPass.py` & `fixrobot-1.0.3/fixrobot/tests/test_FIX50RobotPyTest_ShouldPass.py`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/fixrobot.egg-info/SOURCES.txt` & `fixrobot-1.0.3/fixrobot.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/requirements.txt` & `fixrobot-1.0.3/requirements.txt`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/setup.cfg` & `fixrobot-1.0.3/setup.cfg`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/setup.py` & `fixrobot-1.0.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,14 +38,14 @@
 
 setup(
    name='fixrobot',
    version='1.0',
    description='A useful module to test FIX connectivity and FIX engines. Usage: import fixrobot',
    license="MIT",
    long_description='A useful module to test FIX connectivity and FIX engines. Usage: import fixrobot',
-   author='Man Foo',
+   author='Anand P Subramanian',
    author_email='quickfixrobot@gmail.com',
    url="https://github.com/quickfixrobot",
    packages=['fixrobot'],  #same as name
    install_requires=['wheel', 'configparser', 'pytest'], #external packages as dependencies
 
 )
```

### Comparing `fixrobot-1.0.2/spec/FIX40.xml` & `fixrobot-1.0.3/spec/FIX40.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX41.xml` & `fixrobot-1.0.3/spec/FIX41.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX42.xml` & `fixrobot-1.0.3/spec/FIX42.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX43.xml` & `fixrobot-1.0.3/spec/FIX43.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX44.xml` & `fixrobot-1.0.3/spec/FIX44.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX50.xml` & `fixrobot-1.0.3/spec/FIX50.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX50SP1.xml` & `fixrobot-1.0.3/spec/FIX50SP1.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIX50SP2.xml` & `fixrobot-1.0.3/spec/FIX50SP2.xml`

 * *Files identical despite different names*

### Comparing `fixrobot-1.0.2/spec/FIXT11.xml` & `fixrobot-1.0.3/spec/FIXT11.xml`

 * *Files identical despite different names*

