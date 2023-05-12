# Comparing `tmp/adafruit-circuitpython-irremote-4.1.8.tar.gz` & `tmp/adafruit-circuitpython-irremote-4.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "adafruit-circuitpython-irremote-4.1.8.tar", last modified: Mon Aug 15 21:15:30 2022, max compression
+gzip compressed data, was "adafruit-circuitpython-irremote-4.1.9.tar", last modified: Mon Aug 22 18:41:19 2022, max compression
```

## Comparing `adafruit-circuitpython-irremote-4.1.8.tar` & `adafruit-circuitpython-irremote-4.1.9.tar`

### file list

```diff
@@ -1,48 +1,48 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.584203 adafruit-circuitpython-irremote-4.1.8/.github/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/.github/PULL_REQUEST_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (121)      880 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (121)     2535 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.github/workflows/build.yml
--rw-r--r--   0 runner    (1001) docker     (121)      479 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.github/workflows/failure-help-text.yml
--rw-r--r--   0 runner    (1001) docker     (121)     2966 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (121)     1648 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.gitignore
--rw-r--r--   0 runner    (1001) docker     (121)     1239 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (121)    16248 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.pylintrc
--rw-r--r--   0 runner    (1001) docker     (121)      388 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/.readthedocs.yaml
--rw-r--r--   0 runner    (1001) docker     (121)     6147 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (121)     1106 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/LICENSE
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/LICENSES/
--rw-r--r--   0 runner    (1001) docker     (121)    16814 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/LICENSES/CC-BY-4.0.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1108 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/LICENSES/MIT.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1211 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/LICENSES/Unlicense.txt
--rw-r--r--   0 runner    (1001) docker     (121)     4239 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3465 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/README.rst
--rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/README.rst.license
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     4239 2022-08-15 21:15:30.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      996 2022-08-15 21:15:30.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-15 21:15:30.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-08-15 21:15:30.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       18 2022-08-15 21:15:30.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)    14029 2022-08-15 21:15:22.000000 adafruit-circuitpython-irremote-4.1.8/adafruit_irremote.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/docs/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (121)     4414 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/_static/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (121)      105 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/_static/favicon.ico.license
--rw-r--r--   0 runner    (1001) docker     (121)      127 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/api.rst.license
--rw-r--r--   0 runner    (1001) docker     (121)     5111 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (121)      190 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/examples.rst
--rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/examples.rst.license
--rw-r--r--   0 runner    (1001) docker     (121)     1107 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/index.rst.license
--rw-r--r--   0 runner    (1001) docker     (121)      123 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/examples/
--rw-r--r--   0 runner    (1001) docker     (121)     1209 2022-08-15 21:15:22.000000 adafruit-circuitpython-irremote-4.1.8/examples/irremote_nonblocking.py
--rw-r--r--   0 runner    (1001) docker     (121)      814 2022-08-15 21:15:22.000000 adafruit-circuitpython-irremote-4.1.8/examples/irremote_simpletest.py
--rw-r--r--   0 runner    (1001) docker     (121)      926 2022-08-15 21:15:22.000000 adafruit-circuitpython-irremote-4.1.8/examples/irremote_transmit.py
--rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/optional_requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1250 2022-08-15 21:15:22.000000 adafruit-circuitpython-irremote-4.1.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-15 21:15:15.000000 adafruit-circuitpython-irremote-4.1.8/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-15 21:15:30.588203 adafruit-circuitpython-irremote-4.1.8/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.458977 adafruit-circuitpython-irremote-4.1.9/.github/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.458977 adafruit-circuitpython-irremote-4.1.9/.github/PULL_REQUEST_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (121)      880 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.458977 adafruit-circuitpython-irremote-4.1.9/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (121)     2535 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.github/workflows/build.yml
+-rw-r--r--   0 runner    (1001) docker     (121)      479 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.github/workflows/failure-help-text.yml
+-rw-r--r--   0 runner    (1001) docker     (121)     2966 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (121)     1648 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (121)     1239 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (121)    16248 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.pylintrc
+-rw-r--r--   0 runner    (1001) docker     (121)      388 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/.readthedocs.yaml
+-rw-r--r--   0 runner    (1001) docker     (121)     6147 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (121)     1106 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/LICENSE
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.458977 adafruit-circuitpython-irremote-4.1.9/LICENSES/
+-rw-r--r--   0 runner    (1001) docker     (121)    16814 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/LICENSES/CC-BY-4.0.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     1108 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/LICENSES/MIT.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     1211 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/LICENSES/Unlicense.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     4239 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     3465 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/README.rst
+-rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/README.rst.license
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     4239 2022-08-22 18:41:19.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      996 2022-08-22 18:41:19.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-08-22 18:41:19.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       12 2022-08-22 18:41:19.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       18 2022-08-22 18:41:19.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)    14029 2022-08-22 18:41:11.000000 adafruit-circuitpython-irremote-4.1.9/adafruit_irremote.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/docs/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (121)     4414 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/_static/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (121)      105 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/_static/favicon.ico.license
+-rw-r--r--   0 runner    (1001) docker     (121)      127 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/api.rst
+-rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/api.rst.license
+-rw-r--r--   0 runner    (1001) docker     (121)     5111 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (121)      190 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/examples.rst
+-rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/examples.rst.license
+-rw-r--r--   0 runner    (1001) docker     (121)     1107 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (121)       96 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/index.rst.license
+-rw-r--r--   0 runner    (1001) docker     (121)      123 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/examples/
+-rw-r--r--   0 runner    (1001) docker     (121)     1209 2022-08-22 18:41:11.000000 adafruit-circuitpython-irremote-4.1.9/examples/irremote_nonblocking.py
+-rw-r--r--   0 runner    (1001) docker     (121)      814 2022-08-22 18:41:11.000000 adafruit-circuitpython-irremote-4.1.9/examples/irremote_simpletest.py
+-rw-r--r--   0 runner    (1001) docker     (121)      926 2022-08-22 18:41:11.000000 adafruit-circuitpython-irremote-4.1.9/examples/irremote_transmit.py
+-rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/optional_requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     1250 2022-08-22 18:41:11.000000 adafruit-circuitpython-irremote-4.1.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)      108 2022-08-22 18:40:59.000000 adafruit-circuitpython-irremote-4.1.9/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-08-22 18:41:19.462977 adafruit-circuitpython-irremote-4.1.9/setup.cfg
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md` & `adafruit-circuitpython-irremote-4.1.9/.github/PULL_REQUEST_TEMPLATE/adafruit_circuitpython_pr.md`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/.github/workflows/build.yml` & `adafruit-circuitpython-irremote-4.1.9/.github/workflows/build.yml`

 * *Files 0% similar despite different names*

```diff
@@ -67,11 +67,11 @@
       run: |
         echo ::set-output name=pyproject-toml::$( find . -wholename './pyproject.toml' )
     - name: Build Python package
       if: contains(steps.need-pypi.outputs.pyproject-toml, 'pyproject.toml')
       run: |
         pip install --upgrade build twine
         for file in $(find -not -path "./.*" -not -path "./docs*" \( -name "*.py" -o -name "*.toml" \) ); do
-            sed -i -e "s/0.0.0-auto.0/1.2.3/" $file;
+            sed -i -e "s/0.0.0+auto.0/1.2.3/" $file;
         done;
         python -m build
         twine check dist/*
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/.github/workflows/release.yml` & `adafruit-circuitpython-irremote-4.1.9/.github/workflows/release.yml`

 * *Files 1% similar despite different names*

```diff
@@ -78,11 +78,11 @@
     - name: Build and publish
       if: contains(steps.need-pypi.outputs.pyproject-toml, 'pyproject.toml')
       env:
         TWINE_USERNAME: ${{ secrets.pypi_username }}
         TWINE_PASSWORD: ${{ secrets.pypi_password }}
       run: |
         for file in $(find -not -path "./.*" -not -path "./docs*" \( -name "*.py" -o -name "*.toml" \) ); do
-            sed -i -e "s/0.0.0-auto.0/${{github.event.release.tag_name}}/" $file;
+            sed -i -e "s/0.0.0+auto.0/${{github.event.release.tag_name}}/" $file;
         done;
         python -m build
         twine upload dist/*
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/.gitignore` & `adafruit-circuitpython-irremote-4.1.9/.gitignore`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/.pre-commit-config.yaml` & `adafruit-circuitpython-irremote-4.1.9/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/.pylintrc` & `adafruit-circuitpython-irremote-4.1.9/.pylintrc`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/CODE_OF_CONDUCT.md` & `adafruit-circuitpython-irremote-4.1.9/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/LICENSE` & `adafruit-circuitpython-irremote-4.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/LICENSES/CC-BY-4.0.txt` & `adafruit-circuitpython-irremote-4.1.9/LICENSES/CC-BY-4.0.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/LICENSES/MIT.txt` & `adafruit-circuitpython-irremote-4.1.9/LICENSES/MIT.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/LICENSES/Unlicense.txt` & `adafruit-circuitpython-irremote-4.1.9/LICENSES/Unlicense.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/PKG-INFO` & `adafruit-circuitpython-irremote-4.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: adafruit-circuitpython-irremote
-Version: 4.1.8
+Version: 4.1.9
 Summary: CircuitPython library for infrared transmit and receive.
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/adafruit/Adafruit_CircuitPython_IRRemote
 Keywords: adafruit,infrared,transmit,receive,tx,rx,ir,hardware,micropython,circuitpython
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/README.rst` & `adafruit-circuitpython-irremote-4.1.9/README.rst`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/PKG-INFO` & `adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: adafruit-circuitpython-irremote
-Version: 4.1.8
+Version: 4.1.9
 Summary: CircuitPython library for infrared transmit and receive.
 Author-email: Adafruit Industries <circuitpython@adafruit.com>
 License: MIT
 Project-URL: Homepage, https://github.com/adafruit/Adafruit_CircuitPython_IRRemote
 Keywords: adafruit,infrared,transmit,receive,tx,rx,ir,hardware,micropython,circuitpython
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/adafruit_circuitpython_irremote.egg-info/SOURCES.txt` & `adafruit-circuitpython-irremote-4.1.9/adafruit_circuitpython_irremote.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/adafruit_irremote.py` & `adafruit-circuitpython-irremote-4.1.9/adafruit_irremote.py`

 * *Files 0% similar despite different names*

```diff
@@ -50,15 +50,15 @@
   https://github.com/adafruit/circuitpython/releases
 
 """
 import array
 from collections import namedtuple
 import time
 
-__version__ = "4.1.8"
+__version__ = "4.1.9"
 __repo__ = "https://github.com/adafruit/Adafruit_CircuitPython_IRRemote.git"
 
 
 class IRDecodeException(Exception):
     """Generic decode exception"""
```

### Comparing `adafruit-circuitpython-irremote-4.1.8/docs/_static/favicon.ico` & `adafruit-circuitpython-irremote-4.1.9/docs/_static/favicon.ico`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/docs/conf.py` & `adafruit-circuitpython-irremote-4.1.9/docs/conf.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/docs/index.rst` & `adafruit-circuitpython-irremote-4.1.9/docs/index.rst`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/examples/irremote_nonblocking.py` & `adafruit-circuitpython-irremote-4.1.9/examples/irremote_nonblocking.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/examples/irremote_simpletest.py` & `adafruit-circuitpython-irremote-4.1.9/examples/irremote_simpletest.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/examples/irremote_transmit.py` & `adafruit-circuitpython-irremote-4.1.9/examples/irremote_transmit.py`

 * *Files identical despite different names*

### Comparing `adafruit-circuitpython-irremote-4.1.8/pyproject.toml` & `adafruit-circuitpython-irremote-4.1.9/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -8,15 +8,15 @@
     "wheel",
     "setuptools-scm",
 ]
 
 [project]
 name = "adafruit-circuitpython-irremote"
 description = "CircuitPython library for infrared transmit and receive."
-version = "4.1.8"
+version = "4.1.9"
 readme = "README.rst"
 authors = [
     {name = "Adafruit Industries", email = "circuitpython@adafruit.com"}
 ]
 urls = {Homepage = "https://github.com/adafruit/Adafruit_CircuitPython_IRRemote"}
 keywords = [
     "adafruit",
```

