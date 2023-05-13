# Comparing `tmp/jumpthegun-0.0.8.tar.gz` & `tmp/jumpthegun-0.0.9.tar.gz`

## Comparing `jumpthegun-0.0.8.tar` & `jumpthegun-0.0.9.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0      125 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/.flake8
--rw-r--r--   0        0        0      469 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/.pre-commit-config.yaml
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/test_requirements.txt
--rw-r--r--   0        0        0      561 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tox.ini
--rwxr-xr-x   0        0        0     5725 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun.sh
--rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/__init__.py
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/__version__.py
--rw-r--r--   0        0        0    13304 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/jumpthegunctl.py
--rw-r--r--   0        0        0     3900 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/output_redirect.py
--rw-r--r--   0        0        0      475 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/testutils.py
--rw-r--r--   0        0        0     2081 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/tools.py
--rw-r--r--   0        0        0      547 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/utils.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/__init__.py
--rw-r--r--   0        0        0     1210 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/LICENSE
--rw-r--r--   0        0        0      860 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/README.md
--rw-r--r--   0        0        0        6 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/VERSION
--rw-r--r--   0        0        0     1315 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/__init__.py
--rw-r--r--   0        0        0     8896 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_api.py
--rw-r--r--   0        0        0      399 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_error.py
--rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_soft.py
--rw-r--r--   0        0        0     1578 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_unix.py
--rw-r--r--   0        0        0      594 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_util.py
--rw-r--r--   0        0        0     1890 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_windows.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/py.typed
--rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/version.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/__init__.py
--rw-r--r--   0        0        0     7516 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/test_jumpthegun.py
--rw-r--r--   0        0        0      436 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/test_tools.py
--rw-r--r--   0        0        0       30 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/testproj/.flake8
--rw-r--r--   0        0        0       59 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/testproj/bad.py
--rw-r--r--   0        0        0       94 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/testproj/good.py
--rw-r--r--   0        0        0      280 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/tests/testproj/pyproject.toml
--rw-r--r--   0        0        0     1860 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/.gitignore
--rw-r--r--   0        0        0     1081 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/LICENSE
--rw-r--r--   0        0        0     4789 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/README.md
--rw-r--r--   0        0        0     1984 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/pyproject.toml
--rw-r--r--   0        0        0     5949 2020-02-02 00:00:00.000000 jumpthegun-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0      125 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/.flake8
+-rw-r--r--   0        0        0      469 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/.pre-commit-config.yaml
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/test_requirements.txt
+-rw-r--r--   0        0        0      561 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tox.ini
+-rwxr-xr-x   0        0        0     5725 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun.sh
+-rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/__init__.py
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/__version__.py
+-rw-r--r--   0        0        0    13634 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/jumpthegunctl.py
+-rw-r--r--   0        0        0     3900 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/output_redirect.py
+-rw-r--r--   0        0        0      475 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/testutils.py
+-rw-r--r--   0        0        0     2081 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/tools.py
+-rw-r--r--   0        0        0      547 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/utils.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/__init__.py
+-rw-r--r--   0        0        0     1210 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/LICENSE
+-rw-r--r--   0        0        0      860 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/README.md
+-rw-r--r--   0        0        0        6 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/VERSION
+-rw-r--r--   0        0        0     1315 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/__init__.py
+-rw-r--r--   0        0        0     8896 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_api.py
+-rw-r--r--   0        0        0      399 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_error.py
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_soft.py
+-rw-r--r--   0        0        0     1578 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_unix.py
+-rw-r--r--   0        0        0      594 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_util.py
+-rw-r--r--   0        0        0     1890 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_windows.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/py.typed
+-rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/version.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/__init__.py
+-rw-r--r--   0        0        0     7516 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/test_jumpthegun.py
+-rw-r--r--   0        0        0      436 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/test_tools.py
+-rw-r--r--   0        0        0       30 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/testproj/.flake8
+-rw-r--r--   0        0        0       59 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/testproj/bad.py
+-rw-r--r--   0        0        0       94 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/testproj/good.py
+-rw-r--r--   0        0        0      280 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/tests/testproj/pyproject.toml
+-rw-r--r--   0        0        0     1860 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/.gitignore
+-rw-r--r--   0        0        0     1081 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/LICENSE
+-rw-r--r--   0        0        0     4789 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/README.md
+-rw-r--r--   0        0        0     1984 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0     5949 2020-02-02 00:00:00.000000 jumpthegun-0.0.9/PKG-INFO
```

### Comparing `jumpthegun-0.0.8/tox.ini` & `jumpthegun-0.0.9/tox.ini`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun.sh` & `jumpthegun-0.0.9/src/jumpthegun.sh`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/jumpthegunctl.py` & `jumpthegun-0.0.9/src/jumpthegun/jumpthegunctl.py`

 * *Files 2% similar despite different names*

```diff
@@ -204,15 +204,19 @@
     #
     # Override sys.stdout and sys.stderr while loading the tool runner,
     # so that any references to them kept during module imports (e.g for
     # setting up logging) already reference the overrides.
     output_redirector = SocketOutputRedirector()
     with output_redirector.override_outputs_for_imports():
         tool_entrypoint = get_tool_entrypoint(tool_name)
+        env_before = dict(os.environ)
         tool_runner = tool_entrypoint.load()
+        env_after = dict(os.environ)
+        changed_env_vars = dict(set(env_after.items()) - set(env_before.items()))
+        deleted_env_vars = set(env_before) - set(env_after)
 
     pid_file_path, port_file_path = get_pid_and_port_file_paths(tool_name)
 
     if pid_file_path.exists():
         file_pid = int(pid_file_path.read_text())
         if pid_exists(file_pid):
             raise DaemonAlreadyExistsError(tool_name=tool_name)
@@ -305,14 +309,17 @@
     os.chdir(pwd)
 
     # Read and set env vars
     env_vars_str: str = rfile.read(int(rfile.readline())).decode()
     split_lines = (line.split("=", 1) for line in env_vars_str.split("\0"))
     env_vars: Dict[str, str] = dict(line for line in split_lines if len(line) == 2)
     env_vars.pop("_", None)
+    for var_name in deleted_env_vars:
+        env_vars.pop(var_name, None)
+    env_vars.update(changed_env_vars)
     for env_var_name in set(os.environ) - set(env_vars):
         del os.environ[env_var_name]
     os.environ.update(env_vars)
 
     sys.stdin.close()
     sys.stdin = io.TextIOWrapper(cast(BinaryIO, StdinWrapper(conn)))
     output_redirector.set_socket(conn)
```

### Comparing `jumpthegun-0.0.8/src/jumpthegun/output_redirect.py` & `jumpthegun-0.0.9/src/jumpthegun/output_redirect.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/tools.py` & `jumpthegun-0.0.9/src/jumpthegun/tools.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/utils.py` & `jumpthegun-0.0.9/src/jumpthegun/utils.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/LICENSE` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/LICENSE`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/README.md` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/README.md`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/__init__.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/__init__.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_api.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_api.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_soft.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_soft.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_unix.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_unix.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_util.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_util.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/src/jumpthegun/_vendor/filelock/_windows.py` & `jumpthegun-0.0.9/src/jumpthegun/_vendor/filelock/_windows.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/tests/test_jumpthegun.py` & `jumpthegun-0.0.9/tests/test_jumpthegun.py`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/.gitignore` & `jumpthegun-0.0.9/.gitignore`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/LICENSE` & `jumpthegun-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/README.md` & `jumpthegun-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/pyproject.toml` & `jumpthegun-0.0.9/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jumpthegun-0.0.8/PKG-INFO` & `jumpthegun-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jumpthegun
-Version: 0.0.8
+Version: 0.0.9
 Summary: Make Python CLI tools win the speed race, by cheating!
 Project-URL: Homepage, https://github.com/taleinat/jumpthegun
 Author-email: Tal Einat <taleinat@gmail.com>
 License: Apache-2.0
 License-File: LICENSE
 Keywords: cli
 Classifier: Development Status :: 1 - Planning
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: jumpthegun Version: 0.0.8 Summary: Make Python CLI
+Metadata-Version: 2.1 Name: jumpthegun Version: 0.0.9 Summary: Make Python CLI
 tools win the speed race, by cheating! Project-URL: Homepage, https://
 github.com/taleinat/jumpthegun Author-email: Tal Einat
 gmail.com> License: Apache-2.0 License-File: LICENSE Keywords: cli Classifier:
 Development Status :: 1 - Planning Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers Classifier: License :: OSI Approved
 :: Apache Software License Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: POSIX :: Linux Classifier: Programming Language
```

