# Comparing `tmp/knic_jupyter-0.1.6.tar.gz` & `tmp/knic_jupyter-0.1.7.tar.gz`

## Comparing `knic_jupyter-0.1.6.tar` & `knic_jupyter-0.1.7.tar`

### file list

```diff
@@ -1,52 +1,52 @@
--rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.eslintignore
--rw-r--r--   0        0        0     1026 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.eslintrc.js
--rw-r--r--   0        0        0       65 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.prettierignore
--rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.prettierrc
--rw-r--r--   0        0        0      260 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.stylelintrc
--rw-r--r--   0        0        0       86 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/CHANGELOG.md
--rw-r--r--   0        0        0      481 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/Dockerfile
--rw-r--r--   0        0        0     6067 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/GEO-R-6a.ipynb
--rw-r--r--   0        0        0      461 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/MANIFEST.in
--rw-r--r--   0        0        0     2273 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/RELEASE.md
--rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/babel.config.js
--rw-r--r--   0        0        0      689 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/config.py
--rw-r--r--   0        0        0      481 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/docker-compose.yaml
--rw-r--r--   0        0        0     2984 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/environment.yaml
--rw-r--r--   0        0        0      173 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/install.json
--rw-r--r--   0        0        0      864 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/jest.config.js
--rw-r--r--   0        0        0     3802 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/package.json
--rw-r--r--   0        0        0     1731 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/requirements.txt
--rwxr-xr-x   0        0        0       94 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/run-jupyter-lab.sh
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/setup.py
--rw-r--r--   0        0        0      568 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/tsconfig.json
--rw-r--r--   0        0        0   388358 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/yarn.lock
--rw-r--r--   0        0        0    21236 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/build_log.json
--rw-r--r--   0        0        0     3574 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/package.json
--rw-r--r--   0        0        0    20043 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js
--rw-r--r--   0        0        0    21258 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js.map
--rw-r--r--   0        0        0    29216 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/remoteEntry.b6d7521bce2045fa4b93.js
--rw-r--r--   0        0        0    27936 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/remoteEntry.b6d7521bce2045fa4b93.js.map
--rw-r--r--   0        0        0      155 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/style.js
--rw-r--r--   0        0        0     4596 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js
--rw-r--r--   0        0        0     1781 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js.map
--rw-r--r--   0        0        0   135674 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js
--rw-r--r--   0        0        0   117914 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js.map
--rw-r--r--   0        0        0    12054 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js
--rw-r--r--   0        0        0    13784 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js.map
--rw-r--r--   0        0        0   195842 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js
--rw-r--r--   0        0        0   230605 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js.map
--rw-r--r--   0        0        0    12737 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/src/index.ts
--rw-r--r--   0        0        0      187 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/src/__tests__/KNICS_Jupyter_frontend.spec.ts
--rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/style/base.css
--rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/style/index.css
--rw-r--r--   0        0        0       21 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/style/index.js
--rw-r--r--   0        0        0     3343 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/ui-tests/README.md
--rw-r--r--   0        0        0      609 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/ui-tests/jupyter_server_test_config.py
--rw-r--r--   0        0        0      330 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/ui-tests/package.json
--rw-r--r--   0        0        0      340 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/ui-tests/playwright.config.js
--rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/ui-tests/tests/KNICS_Jupyter_frontend.spec.ts
--rw-r--r--   0        0        0     1540 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/.gitignore
--rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/LICENSE
--rw-r--r--   0        0        0     1414 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/README.md
--rw-r--r--   0        0        0     2328 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/pyproject.toml
--rw-r--r--   0        0        0     4182 2020-02-02 00:00:00.000000 knic_jupyter-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.eslintignore
+-rw-r--r--   0        0        0     1026 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.eslintrc.js
+-rw-r--r--   0        0        0       65 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.prettierignore
+-rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.prettierrc
+-rw-r--r--   0        0        0      260 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.stylelintrc
+-rw-r--r--   0        0        0       86 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/CHANGELOG.md
+-rw-r--r--   0        0        0      481 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/Dockerfile
+-rw-r--r--   0        0        0     6095 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/GEO-R-6a.ipynb
+-rw-r--r--   0        0        0      461 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/MANIFEST.in
+-rw-r--r--   0        0        0     2273 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/RELEASE.md
+-rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/babel.config.js
+-rw-r--r--   0        0        0      689 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/config.py
+-rw-r--r--   0        0        0      481 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/docker-compose.yaml
+-rw-r--r--   0        0        0     2984 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/environment.yaml
+-rw-r--r--   0        0        0      173 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/install.json
+-rw-r--r--   0        0        0      864 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/jest.config.js
+-rw-r--r--   0        0        0     3802 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/package.json
+-rw-r--r--   0        0        0     1731 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/requirements.txt
+-rwxr-xr-x   0        0        0      229 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/run-jupyter-lab.sh
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/setup.py
+-rw-r--r--   0        0        0      568 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/tsconfig.json
+-rw-r--r--   0        0        0   388358 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/yarn.lock
+-rw-r--r--   0        0        0    21236 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/build_log.json
+-rw-r--r--   0        0        0     3574 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/package.json
+-rw-r--r--   0        0        0    20043 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js
+-rw-r--r--   0        0        0    21258 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js.map
+-rw-r--r--   0        0        0    29216 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/remoteEntry.477e3e82ace7c6b5b6c2.js
+-rw-r--r--   0        0        0    27936 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/remoteEntry.477e3e82ace7c6b5b6c2.js.map
+-rw-r--r--   0        0        0      155 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/style.js
+-rw-r--r--   0        0        0     4596 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js
+-rw-r--r--   0        0        0     1781 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js.map
+-rw-r--r--   0        0        0   135674 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js
+-rw-r--r--   0        0        0   117914 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js.map
+-rw-r--r--   0        0        0    12054 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js
+-rw-r--r--   0        0        0    13784 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js.map
+-rw-r--r--   0        0        0   195842 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js
+-rw-r--r--   0        0        0   230605 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js.map
+-rw-r--r--   0        0        0    12737 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/src/index.ts
+-rw-r--r--   0        0        0      187 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/src/__tests__/KNICS_Jupyter_frontend.spec.ts
+-rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/style/base.css
+-rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/style/index.css
+-rw-r--r--   0        0        0       21 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/style/index.js
+-rw-r--r--   0        0        0     3343 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/ui-tests/README.md
+-rw-r--r--   0        0        0      609 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/ui-tests/jupyter_server_test_config.py
+-rw-r--r--   0        0        0      330 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/ui-tests/package.json
+-rw-r--r--   0        0        0      340 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/ui-tests/playwright.config.js
+-rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/ui-tests/tests/KNICS_Jupyter_frontend.spec.ts
+-rw-r--r--   0        0        0     1540 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1090 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/LICENSE
+-rw-r--r--   0        0        0     1414 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/README.md
+-rw-r--r--   0        0        0     2328 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     4182 2020-02-02 00:00:00.000000 knic_jupyter-0.1.7/PKG-INFO
```

### Comparing `knic_jupyter-0.1.6/.eslintrc.js` & `knic_jupyter-0.1.7/.eslintrc.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/GEO-R-6a.ipynb` & `knic_jupyter-0.1.7/GEO-R-6a.ipynb`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9970012626262627%*

 * *Differences: {"'cells'": "{1: {'execution_count': 23}, 2: {'execution_count': 24}, 4: {'execution_count': 7, "*

 * *            "'outputs': {0: {'text': ['CHANGELOG.md         docker-compose.yaml  "*

 * *            "\\x1b[31mrun-jupyter-lab.sh\\x1b[m\\x1b[m\\n', 'Dockerfile           "*

 * *            "environment.yaml     setup.py\\n', 'GEO-R-6a.ipynb       install.json         "*

 * *            "\\x1b[34msrc\\x1b[m\\x1b[m\\n', 'LICENSE              jest.config.js       "*

 * *            "\\x1b[34mstyle\\x1b[m\\x1b[m\\n', 'MANIFEST.in      […]*

```diff
@@ -6,26 +6,26 @@
             "metadata": {},
             "source": [
                 "Initialize geonames notebook"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 1,
+            "execution_count": 23,
             "id": "d072f855-1a3d-4881-a082-b2171205e7a5",
             "metadata": {},
             "outputs": [],
             "source": [
                 "from kgtk.functions import kgtk\n",
                 "edges_path = 'data/geonames_sample.tsv.gz'"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 2,
+            "execution_count": 24,
             "id": "861574d8-c6e0-4c09-a5bc-5147ac3e2f91",
             "metadata": {},
             "outputs": [
                 {
                     "name": "stdout",
                     "output_type": "stream",
                     "text": [
@@ -43,31 +43,32 @@
             "metadata": {},
             "source": [
                 "Find all locations, sorted by population"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 2,
+            "execution_count": 7,
             "id": "06a51eb8-2e07-4d43-9222-089f0765b1fa",
             "metadata": {},
             "outputs": [
                 {
                     "name": "stdout",
                     "output_type": "stream",
                     "text": [
-                        "CHANGELOG.md         docker-compose.yaml  requirements.txt\n",
-                        "Dockerfile           environment.yaml     \u001b[31mrun-jupyter-lab.sh\u001b[m\u001b[m\n",
-                        "GEO-R-6a.ipynb       install.json         setup.py\n",
-                        "LICENSE              jest.config.js       \u001b[34msrc\u001b[m\u001b[m\n",
-                        "MANIFEST.in          \u001b[34mknic-jupyter\u001b[m\u001b[m         \u001b[34mstyle\u001b[m\u001b[m\n",
-                        "README.md            \u001b[34mlib\u001b[m\u001b[m                  tsconfig.json\n",
-                        "RELEASE.md           \u001b[34mnode_modules\u001b[m\u001b[m         tsconfig.tsbuildinfo\n",
-                        "babel.config.js      package.json         \u001b[34mui-tests\u001b[m\u001b[m\n",
-                        "\u001b[34mdist\u001b[m\u001b[m                 pyproject.toml       yarn.lock\n"
+                        "CHANGELOG.md         docker-compose.yaml  \u001b[31mrun-jupyter-lab.sh\u001b[m\u001b[m\n",
+                        "Dockerfile           environment.yaml     setup.py\n",
+                        "GEO-R-6a.ipynb       install.json         \u001b[34msrc\u001b[m\u001b[m\n",
+                        "LICENSE              jest.config.js       \u001b[34mstyle\u001b[m\u001b[m\n",
+                        "MANIFEST.in          \u001b[34mknic-jupyter\u001b[m\u001b[m         tsconfig.json\n",
+                        "README.md            \u001b[34mlib\u001b[m\u001b[m                  tsconfig.tsbuildinfo\n",
+                        "RELEASE.md           \u001b[34mnode_modules\u001b[m\u001b[m         \u001b[34mui-tests\u001b[m\u001b[m\n",
+                        "babel.config.js      package.json         yarn.lock\n",
+                        "config.py            pyproject.toml\n",
+                        "\u001b[34mdist\u001b[m\u001b[m                 requirements.txt\n"
                     ]
                 }
             ],
             "source": [
                 "!ls"
             ]
         },
```

### Comparing `knic_jupyter-0.1.6/RELEASE.md` & `knic_jupyter-0.1.7/RELEASE.md`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/config.py` & `knic_jupyter-0.1.7/config.py`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/environment.yaml` & `knic_jupyter-0.1.7/environment.yaml`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/jest.config.js` & `knic_jupyter-0.1.7/jest.config.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/package.json` & `knic_jupyter-0.1.7/package.json`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.975%*

 * *Differences: {"'version'": "'0.1.7'"}*

```diff
@@ -97,9 +97,9 @@
     "sideEffects": [
         "style/*.css",
         "style/index.js"
     ],
     "style": "style/index.css",
     "styleModule": "style/index.js",
     "types": "lib/index.d.ts",
-    "version": "0.1.6"
+    "version": "0.1.7"
 }
```

### Comparing `knic_jupyter-0.1.6/requirements.txt` & `knic_jupyter-0.1.7/requirements.txt`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/tsconfig.json` & `knic_jupyter-0.1.7/tsconfig.json`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/yarn.lock` & `knic_jupyter-0.1.7/yarn.lock`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/build_log.json` & `knic_jupyter-0.1.7/knic-jupyter/labextension/build_log.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9999993348233291%*

 * *Differences: {'0': "{'plugins': {1: {'_options': {'shared': {'knic-jupyter': {'version': '0.1.6'}}}}}}"}*

```diff
@@ -605,15 +605,15 @@
                         "@types/node": {},
                         "@types/uuid": {},
                         "axios": {},
                         "dexie": {},
                         "knic-jupyter": {
                             "import": "/Users/gleb/knic/knic-jupyter/lib/index.js",
                             "singleton": true,
-                            "version": "0.1.5"
+                            "version": "0.1.6"
                         },
                         "react": {
                             "import": false,
                             "requiredVersion": "^17.0.1",
                             "singleton": true
                         },
                         "react-dom": {
```

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/package.json` & `knic_jupyter-0.1.7/knic-jupyter/labextension/package.json`

 * *Files 2% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9743055555555555%*

 * *Differences: {"'jupyterlab'": "{'_build': {'load': 'static/remoteEntry.477e3e82ace7c6b5b6c2.js'}}",*

 * * "'version'": "'0.1.6'"}*

```diff
@@ -49,15 +49,15 @@
                 "jlpm clean:all"
             ]
         }
     },
     "jupyterlab": {
         "_build": {
             "extension": "./extension",
-            "load": "static/remoteEntry.b6d7521bce2045fa4b93.js",
+            "load": "static/remoteEntry.477e3e82ace7c6b5b6c2.js",
             "style": "./style"
         },
         "extension": true,
         "outputDir": "knic-jupyter/labextension"
     },
     "keywords": [
         "knic",
@@ -102,9 +102,9 @@
     "sideEffects": [
         "style/*.css",
         "style/index.js"
     ],
     "style": "style/index.css",
     "styleModule": "style/index.js",
     "types": "lib/index.d.ts",
-    "version": "0.1.5"
+    "version": "0.1.6"
 }
```

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/lib_index_js.8adebee2c486ebf03cbc.js.map`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/remoteEntry.b6d7521bce2045fa4b93.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/remoteEntry.477e3e82ace7c6b5b6c2.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -433,15 +433,15 @@
                 /******/
                 case "default": {
                     /******/
                     register("axios", "1.4.0", () => (__webpack_require__.e("vendors-node_modules_axios_index_js").then(() => (() => (__webpack_require__( /*! ./node_modules/axios/index.js */ "./node_modules/axios/index.js"))))));
                     /******/
                     register("dexie", "3.2.3", () => (__webpack_require__.e("vendors-node_modules_dexie_dist_modern_dexie_mjs").then(() => (() => (__webpack_require__( /*! ./node_modules/dexie/dist/modern/dexie.mjs */ "./node_modules/dexie/dist/modern/dexie.mjs"))))));
                     /******/
-                    register("knic-jupyter", "0.1.5", () => (__webpack_require__.e("lib_index_js").then(() => (() => (__webpack_require__( /*! ./lib/index.js */ "./lib/index.js"))))));
+                    register("knic-jupyter", "0.1.6", () => (__webpack_require__.e("lib_index_js").then(() => (() => (__webpack_require__( /*! ./lib/index.js */ "./lib/index.js"))))));
                     /******/
                 }
                 /******/
                 break;
                 /******/
             }
             /******/
@@ -1090,8 +1090,8 @@
     /******/
     var __webpack_exports__ = __webpack_require__("webpack/container/entry/knic-jupyter");
     /******/
     (_JUPYTERLAB = typeof _JUPYTERLAB === "undefined" ? {} : _JUPYTERLAB)["knic-jupyter"] = __webpack_exports__;
     /******/
     /******/
 })();
-//# sourceMappingURL=remoteEntry.b6d7521bce2045fa4b93.js.map
+//# sourceMappingURL=remoteEntry.477e3e82ace7c6b5b6c2.js.map
```

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/remoteEntry.b6d7521bce2045fa4b93.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/remoteEntry.477e3e82ace7c6b5b6c2.js.map`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9210526315789475%*

 * *Differences: {"'file'": "'remoteEntry.477e3e82ace7c6b5b6c2.js'",*

 * * "'sourcesContent'": "{insert: [(10, '__webpack_require__.S = {};\\nvar initPromises = {};\\nvar "*

 * *                     'initTokens = {};\\n__webpack_require__.I = (name, initScope) => '*

 * *                     '{\\n\\tif(!initScope) initScope = [];\\n\\t// handling circular init '*

 * *                     'calls\\n\\tvar initToken = initTokens[name];\\n\\tif(!initToken) initToken = '*

 * *                     'initTokens[name] = {};\\n\\tif(initScope.indexOf(initToke […]*

```diff
@@ -1,9 +1,9 @@
 {
-    "file": "remoteEntry.b6d7521bce2045fa4b93.js",
+    "file": "remoteEntry.477e3e82ace7c6b5b6c2.js",
     "mappings": ";;;;;;;;;;;AAAA;AACA;AACA;AACA,EAAE;AACF;AACA;AACA,EAAE;AACF;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA,IAAI;AACJ;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;AACA;;AAEA;AACA;AACA;AACA;AACA,CAAC;;;;;;UCpCD;UACA;;UAEA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;UACA;;UAEA;UACA;;UAEA;UACA;UACA;;UAEA;UACA;;UAEA;UACA;;;;;WC5BA;WACA;WACA;WACA;WACA;WACA,iCAAiC,WAAW;WAC5C;WACA;;;;;WCPA;WACA;WACA;WACA;WACA,yCAAyC,wCAAwC;WACjF;WACA;WACA;;;;;WCPA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,EAAE;WACF;;;;;WCRA;WACA;WACA;WACA,8BAA8B,mVAAmV;WACjX;;;;;WCJA;WACA;WACA;WACA;WACA,GAAG;WACH;WACA;WACA,CAAC;;;;;WCPD;;;;;WCAA;WACA;WACA;WACA;WACA,uBAAuB,4BAA4B;WACnD;WACA;WACA;WACA,iBAAiB,oBAAoB;WACrC;WACA,mGAAmG,YAAY;WAC/G;WACA;WACA;WACA;WACA;;WAEA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,mEAAmE,iCAAiC;WACpG;WACA;WACA;WACA;;;;;WCxCA;WACA;WACA;WACA,uDAAuD,iBAAiB;WACxE;WACA,gDAAgD,aAAa;WAC7D;;;;;WCNA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,oJAAoJ;WACpJ;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,IAAI,aAAa;WACjB;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;;;;;WC/CA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;;;;;WClBA;WACA;WACA,WAAW,6BAA6B,iBAAiB,GAAG,qEAAqE;WACjI;WACA;WACA;WACA,qCAAqC,aAAa,EAAE,wDAAwD,2BAA2B,4BAA4B,2BAA2B,+CAA+C,mCAAmC;WAChR;WACA;WACA;WACA,qBAAqB,8BAA8B,SAAS,sDAAsD,gBAAgB,eAAe,KAAK,6DAA6D,SAAS,SAAS,QAAQ,eAAe,KAAK,eAAe,qGAAqG,WAAW,aAAa;WAC7Y;WACA;WACA;WACA,gBAAgB,8BAA8B,qBAAqB,YAAY,sBAAsB,SAAS,iDAAiD,6FAA6F,WAAW,uBAAuB,2BAA2B,wBAAwB,KAAK,oCAAoC,oBAAoB,wBAAwB,oBAAoB,SAAS,KAAK,yBAAyB,KAAK,gCAAgC,yBAAyB,QAAQ,eAAe,KAAK,eAAe,4DAA4D;WACtoB;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,EAAE;WACF;WACA;WACA;WACA;WACA;WACA;WACA,EAAE;WACF;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,EAAE;WACF;WACA;WACA;WACA;WACA;WACA;WACA;WACA,EAAE;WACF;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,CAAC;;WAED;WACA;WACA;WACA,CAAC;WACD;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA,CAAC;WACD;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,MAAM;WACN,KAAK,WAAW;WAChB,GAAG;WACH;WACA;;;;;WChLA;;WAEA;WACA;WACA;WACA;WACA;WACA;;WAEA;WACA;WACA;WACA,iCAAiC;;WAEjC;WACA;WACA;WACA,KAAK;WACL,eAAe;WACf;WACA;WACA;;WAEA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,MAAM;WACN;WACA;WACA;;WAEA;;WAEA;;WAEA;;WAEA;;WAEA;;WAEA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA;WACA,MAAM,qBAAqB;WAC3B;WACA;WACA;WACA;WACA;WACA;;WAEA;;WAEA;WACA;WACA;;;;;WCrFA;;;;;UEAA;UACA;UACA;UACA",
     "names": [],
     "sourceRoot": "",
     "sources": [
         "webpack://knic-jupyter/webpack/container-entry",
         "webpack://knic-jupyter/webpack/bootstrap",
         "webpack://knic-jupyter/webpack/runtime/compat get default export",
@@ -30,15 +30,15 @@
         "// define getter functions for harmony exports\n__webpack_require__.d = (exports, definition) => {\n\tfor(var key in definition) {\n\t\tif(__webpack_require__.o(definition, key) && !__webpack_require__.o(exports, key)) {\n\t\t\tObject.defineProperty(exports, key, { enumerable: true, get: definition[key] });\n\t\t}\n\t}\n};",
         "__webpack_require__.f = {};\n// This file contains only the entry chunk.\n// The chunk loading function for additional chunks\n__webpack_require__.e = (chunkId) => {\n\treturn Promise.all(Object.keys(__webpack_require__.f).reduce((promises, key) => {\n\t\t__webpack_require__.f[key](chunkId, promises);\n\t\treturn promises;\n\t}, []));\n};",
         "// This function allow to reference async chunks\n__webpack_require__.u = (chunkId) => {\n\t// return url for filenames based on template\n\treturn \"\" + chunkId + \".\" + {\"lib_index_js\":\"8adebee2c486ebf03cbc\",\"vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1\":\"a0ffbb03a81b5fb1c68c\",\"style_index_js\":\"f52bc77755c454c42949\",\"vendors-node_modules_axios_index_js\":\"1ca6784f009c20db95e8\",\"vendors-node_modules_dexie_dist_modern_dexie_mjs\":\"0aea58707561a10ac2f5\"}[chunkId] + \".js\";\n};",
         "__webpack_require__.g = (function() {\n\tif (typeof globalThis === 'object') return globalThis;\n\ttry {\n\t\treturn this || new Function('return this')();\n\t} catch (e) {\n\t\tif (typeof window === 'object') return window;\n\t}\n})();",
         "__webpack_require__.o = (obj, prop) => (Object.prototype.hasOwnProperty.call(obj, prop))",
         "var inProgress = {};\nvar dataWebpackPrefix = \"knic-jupyter:\";\n// loadScript function to load a script via script tag\n__webpack_require__.l = (url, done, key, chunkId) => {\n\tif(inProgress[url]) { inProgress[url].push(done); return; }\n\tvar script, needAttach;\n\tif(key !== undefined) {\n\t\tvar scripts = document.getElementsByTagName(\"script\");\n\t\tfor(var i = 0; i < scripts.length; i++) {\n\t\t\tvar s = scripts[i];\n\t\t\tif(s.getAttribute(\"src\") == url || s.getAttribute(\"data-webpack\") == dataWebpackPrefix + key) { script = s; break; }\n\t\t}\n\t}\n\tif(!script) {\n\t\tneedAttach = true;\n\t\tscript = document.createElement('script');\n\n\t\tscript.charset = 'utf-8';\n\t\tscript.timeout = 120;\n\t\tif (__webpack_require__.nc) {\n\t\t\tscript.setAttribute(\"nonce\", __webpack_require__.nc);\n\t\t}\n\t\tscript.setAttribute(\"data-webpack\", dataWebpackPrefix + key);\n\t\tscript.src = url;\n\t}\n\tinProgress[url] = [done];\n\tvar onScriptComplete = (prev, event) => {\n\t\t// avoid mem leaks in IE.\n\t\tscript.onerror = script.onload = null;\n\t\tclearTimeout(timeout);\n\t\tvar doneFns = inProgress[url];\n\t\tdelete inProgress[url];\n\t\tscript.parentNode && script.parentNode.removeChild(script);\n\t\tdoneFns && doneFns.forEach((fn) => (fn(event)));\n\t\tif(prev) return prev(event);\n\t}\n\tvar timeout = setTimeout(onScriptComplete.bind(null, undefined, { type: 'timeout', target: script }), 120000);\n\tscript.onerror = onScriptComplete.bind(null, script.onerror);\n\tscript.onload = onScriptComplete.bind(null, script.onload);\n\tneedAttach && document.head.appendChild(script);\n};",
         "// define __esModule on exports\n__webpack_require__.r = (exports) => {\n\tif(typeof Symbol !== 'undefined' && Symbol.toStringTag) {\n\t\tObject.defineProperty(exports, Symbol.toStringTag, { value: 'Module' });\n\t}\n\tObject.defineProperty(exports, '__esModule', { value: true });\n};",
-        "__webpack_require__.S = {};\nvar initPromises = {};\nvar initTokens = {};\n__webpack_require__.I = (name, initScope) => {\n\tif(!initScope) initScope = [];\n\t// handling circular init calls\n\tvar initToken = initTokens[name];\n\tif(!initToken) initToken = initTokens[name] = {};\n\tif(initScope.indexOf(initToken) >= 0) return;\n\tinitScope.push(initToken);\n\t// only runs once\n\tif(initPromises[name]) return initPromises[name];\n\t// creates a new share scope if needed\n\tif(!__webpack_require__.o(__webpack_require__.S, name)) __webpack_require__.S[name] = {};\n\t// runs all init snippets from all modules reachable\n\tvar scope = __webpack_require__.S[name];\n\tvar warn = (msg) => {\n\t\tif (typeof console !== \"undefined\" && console.warn) console.warn(msg);\n\t};\n\tvar uniqueName = \"knic-jupyter\";\n\tvar register = (name, version, factory, eager) => {\n\t\tvar versions = scope[name] = scope[name] || {};\n\t\tvar activeVersion = versions[version];\n\t\tif(!activeVersion || (!activeVersion.loaded && (!eager != !activeVersion.eager ? eager : uniqueName > activeVersion.from))) versions[version] = { get: factory, from: uniqueName, eager: !!eager };\n\t};\n\tvar initExternal = (id) => {\n\t\tvar handleError = (err) => (warn(\"Initialization of sharing external failed: \" + err));\n\t\ttry {\n\t\t\tvar module = __webpack_require__(id);\n\t\t\tif(!module) return;\n\t\t\tvar initFn = (module) => (module && module.init && module.init(__webpack_require__.S[name], initScope))\n\t\t\tif(module.then) return promises.push(module.then(initFn, handleError));\n\t\t\tvar initResult = initFn(module);\n\t\t\tif(initResult && initResult.then) return promises.push(initResult['catch'](handleError));\n\t\t} catch(err) { handleError(err); }\n\t}\n\tvar promises = [];\n\tswitch(name) {\n\t\tcase \"default\": {\n\t\t\tregister(\"axios\", \"1.4.0\", () => (__webpack_require__.e(\"vendors-node_modules_axios_index_js\").then(() => (() => (__webpack_require__(/*! ./node_modules/axios/index.js */ \"./node_modules/axios/index.js\"))))));\n\t\t\tregister(\"dexie\", \"3.2.3\", () => (__webpack_require__.e(\"vendors-node_modules_dexie_dist_modern_dexie_mjs\").then(() => (() => (__webpack_require__(/*! ./node_modules/dexie/dist/modern/dexie.mjs */ \"./node_modules/dexie/dist/modern/dexie.mjs\"))))));\n\t\t\tregister(\"knic-jupyter\", \"0.1.5\", () => (__webpack_require__.e(\"lib_index_js\").then(() => (() => (__webpack_require__(/*! ./lib/index.js */ \"./lib/index.js\"))))));\n\t\t}\n\t\tbreak;\n\t}\n\tif(!promises.length) return initPromises[name] = 1;\n\treturn initPromises[name] = Promise.all(promises).then(() => (initPromises[name] = 1));\n};",
+        "__webpack_require__.S = {};\nvar initPromises = {};\nvar initTokens = {};\n__webpack_require__.I = (name, initScope) => {\n\tif(!initScope) initScope = [];\n\t// handling circular init calls\n\tvar initToken = initTokens[name];\n\tif(!initToken) initToken = initTokens[name] = {};\n\tif(initScope.indexOf(initToken) >= 0) return;\n\tinitScope.push(initToken);\n\t// only runs once\n\tif(initPromises[name]) return initPromises[name];\n\t// creates a new share scope if needed\n\tif(!__webpack_require__.o(__webpack_require__.S, name)) __webpack_require__.S[name] = {};\n\t// runs all init snippets from all modules reachable\n\tvar scope = __webpack_require__.S[name];\n\tvar warn = (msg) => {\n\t\tif (typeof console !== \"undefined\" && console.warn) console.warn(msg);\n\t};\n\tvar uniqueName = \"knic-jupyter\";\n\tvar register = (name, version, factory, eager) => {\n\t\tvar versions = scope[name] = scope[name] || {};\n\t\tvar activeVersion = versions[version];\n\t\tif(!activeVersion || (!activeVersion.loaded && (!eager != !activeVersion.eager ? eager : uniqueName > activeVersion.from))) versions[version] = { get: factory, from: uniqueName, eager: !!eager };\n\t};\n\tvar initExternal = (id) => {\n\t\tvar handleError = (err) => (warn(\"Initialization of sharing external failed: \" + err));\n\t\ttry {\n\t\t\tvar module = __webpack_require__(id);\n\t\t\tif(!module) return;\n\t\t\tvar initFn = (module) => (module && module.init && module.init(__webpack_require__.S[name], initScope))\n\t\t\tif(module.then) return promises.push(module.then(initFn, handleError));\n\t\t\tvar initResult = initFn(module);\n\t\t\tif(initResult && initResult.then) return promises.push(initResult['catch'](handleError));\n\t\t} catch(err) { handleError(err); }\n\t}\n\tvar promises = [];\n\tswitch(name) {\n\t\tcase \"default\": {\n\t\t\tregister(\"axios\", \"1.4.0\", () => (__webpack_require__.e(\"vendors-node_modules_axios_index_js\").then(() => (() => (__webpack_require__(/*! ./node_modules/axios/index.js */ \"./node_modules/axios/index.js\"))))));\n\t\t\tregister(\"dexie\", \"3.2.3\", () => (__webpack_require__.e(\"vendors-node_modules_dexie_dist_modern_dexie_mjs\").then(() => (() => (__webpack_require__(/*! ./node_modules/dexie/dist/modern/dexie.mjs */ \"./node_modules/dexie/dist/modern/dexie.mjs\"))))));\n\t\t\tregister(\"knic-jupyter\", \"0.1.6\", () => (__webpack_require__.e(\"lib_index_js\").then(() => (() => (__webpack_require__(/*! ./lib/index.js */ \"./lib/index.js\"))))));\n\t\t}\n\t\tbreak;\n\t}\n\tif(!promises.length) return initPromises[name] = 1;\n\treturn initPromises[name] = Promise.all(promises).then(() => (initPromises[name] = 1));\n};",
         "var scriptUrl;\nif (__webpack_require__.g.importScripts) scriptUrl = __webpack_require__.g.location + \"\";\nvar document = __webpack_require__.g.document;\nif (!scriptUrl && document) {\n\tif (document.currentScript)\n\t\tscriptUrl = document.currentScript.src;\n\tif (!scriptUrl) {\n\t\tvar scripts = document.getElementsByTagName(\"script\");\n\t\tif(scripts.length) {\n\t\t\tvar i = scripts.length - 1;\n\t\t\twhile (i > -1 && !scriptUrl) scriptUrl = scripts[i--].src;\n\t\t}\n\t}\n}\n// When supporting browsers where an automatic publicPath is not supported you must specify an output.publicPath manually via configuration\n// or pass an empty string (\"\") and set the __webpack_public_path__ variable from your code to use your own logic.\nif (!scriptUrl) throw new Error(\"Automatic publicPath is not supported in this browser\");\nscriptUrl = scriptUrl.replace(/#.*$/, \"\").replace(/\\?.*$/, \"\").replace(/\\/[^\\/]+$/, \"/\");\n__webpack_require__.p = scriptUrl;",
         "var parseVersion = (str) => {\n\t// see webpack/lib/util/semver.js for original code\n\tvar p=p=>{return p.split(\".\").map((p=>{return+p==p?+p:p}))},n=/^([^-+]+)?(?:-([^+]+))?(?:\\+(.+))?$/.exec(str),r=n[1]?p(n[1]):[];return n[2]&&(r.length++,r.push.apply(r,p(n[2]))),n[3]&&(r.push([]),r.push.apply(r,p(n[3]))),r;\n}\nvar versionLt = (a, b) => {\n\t// see webpack/lib/util/semver.js for original code\n\ta=parseVersion(a),b=parseVersion(b);for(var r=0;;){if(r>=a.length)return r<b.length&&\"u\"!=(typeof b[r])[0];var e=a[r],n=(typeof e)[0];if(r>=b.length)return\"u\"==n;var t=b[r],f=(typeof t)[0];if(n!=f)return\"o\"==n&&\"n\"==f||(\"s\"==f||\"u\"==n);if(\"o\"!=n&&\"u\"!=n&&e!=t)return e<t;r++}\n}\nvar rangeToString = (range) => {\n\t// see webpack/lib/util/semver.js for original code\n\tvar r=range[0],n=\"\";if(1===range.length)return\"*\";if(r+.5){n+=0==r?\">=\":-1==r?\"<\":1==r?\"^\":2==r?\"~\":r>0?\"=\":\"!=\";for(var e=1,a=1;a<range.length;a++){e--,n+=\"u\"==(typeof(t=range[a]))[0]?\"-\":(e>0?\".\":\"\")+(e=2,t)}return n}var g=[];for(a=1;a<range.length;a++){var t=range[a];g.push(0===t?\"not(\"+o()+\")\":1===t?\"(\"+o()+\" || \"+o()+\")\":2===t?g.pop()+\" \"+g.pop():rangeToString(t))}return o();function o(){return g.pop().replace(/^\\((.+)\\)$/,\"$1\")}\n}\nvar satisfy = (range, version) => {\n\t// see webpack/lib/util/semver.js for original code\n\tif(0 in range){version=parseVersion(version);var e=range[0],r=e<0;r&&(e=-e-1);for(var n=0,i=1,a=!0;;i++,n++){var f,s,g=i<range.length?(typeof range[i])[0]:\"\";if(n>=version.length||\"o\"==(s=(typeof(f=version[n]))[0]))return!a||(\"u\"==g?i>e&&!r:\"\"==g!=r);if(\"u\"==s){if(!a||\"u\"!=g)return!1}else if(a)if(g==s)if(i<=e){if(f!=range[i])return!1}else{if(r?f>range[i]:f<range[i])return!1;f!=range[i]&&(a=!1)}else if(\"s\"!=g&&\"n\"!=g){if(r||i<=e)return!1;a=!1,i--}else{if(i<=e||s<g!=r)return!1;a=!1}else\"s\"!=g&&\"n\"!=g&&(a=!1,i--)}}var t=[],o=t.pop.bind(t);for(n=1;n<range.length;n++){var u=range[n];t.push(1==u?o()|o():2==u?o()&o():u?satisfy(u,version):!o())}return!!o();\n}\nvar ensureExistence = (scopeName, key) => {\n\tvar scope = __webpack_require__.S[scopeName];\n\tif(!scope || !__webpack_require__.o(scope, key)) throw new Error(\"Shared module \" + key + \" doesn't exist in shared scope \" + scopeName);\n\treturn scope;\n};\nvar findVersion = (scope, key) => {\n\tvar versions = scope[key];\n\tvar key = Object.keys(versions).reduce((a, b) => {\n\t\treturn !a || versionLt(a, b) ? b : a;\n\t}, 0);\n\treturn key && versions[key]\n};\nvar findSingletonVersionKey = (scope, key) => {\n\tvar versions = scope[key];\n\treturn Object.keys(versions).reduce((a, b) => {\n\t\treturn !a || (!versions[a].loaded && versionLt(a, b)) ? b : a;\n\t}, 0);\n};\nvar getInvalidSingletonVersionMessage = (scope, key, version, requiredVersion) => {\n\treturn \"Unsatisfied version \" + version + \" from \" + (version && scope[key][version].from) + \" of shared singleton module \" + key + \" (required \" + rangeToString(requiredVersion) + \")\"\n};\nvar getSingleton = (scope, scopeName, key, requiredVersion) => {\n\tvar version = findSingletonVersionKey(scope, key);\n\treturn get(scope[key][version]);\n};\nvar getSingletonVersion = (scope, scopeName, key, requiredVersion) => {\n\tvar version = findSingletonVersionKey(scope, key);\n\tif (!satisfy(requiredVersion, version)) warn(getInvalidSingletonVersionMessage(scope, key, version, requiredVersion));\n\treturn get(scope[key][version]);\n};\nvar getStrictSingletonVersion = (scope, scopeName, key, requiredVersion) => {\n\tvar version = findSingletonVersionKey(scope, key);\n\tif (!satisfy(requiredVersion, version)) throw new Error(getInvalidSingletonVersionMessage(scope, key, version, requiredVersion));\n\treturn get(scope[key][version]);\n};\nvar findValidVersion = (scope, key, requiredVersion) => {\n\tvar versions = scope[key];\n\tvar key = Object.keys(versions).reduce((a, b) => {\n\t\tif (!satisfy(requiredVersion, b)) return a;\n\t\treturn !a || versionLt(a, b) ? b : a;\n\t}, 0);\n\treturn key && versions[key]\n};\nvar getInvalidVersionMessage = (scope, scopeName, key, requiredVersion) => {\n\tvar versions = scope[key];\n\treturn \"No satisfying version (\" + rangeToString(requiredVersion) + \") of shared module \" + key + \" found in shared scope \" + scopeName + \".\\n\" +\n\t\t\"Available versions: \" + Object.keys(versions).map((key) => {\n\t\treturn key + \" from \" + versions[key].from;\n\t}).join(\", \");\n};\nvar getValidVersion = (scope, scopeName, key, requiredVersion) => {\n\tvar entry = findValidVersion(scope, key, requiredVersion);\n\tif(entry) return get(entry);\n\tthrow new Error(getInvalidVersionMessage(scope, scopeName, key, requiredVersion));\n};\nvar warn = (msg) => {\n\tif (typeof console !== \"undefined\" && console.warn) console.warn(msg);\n};\nvar warnInvalidVersion = (scope, scopeName, key, requiredVersion) => {\n\twarn(getInvalidVersionMessage(scope, scopeName, key, requiredVersion));\n};\nvar get = (entry) => {\n\tentry.loaded = 1;\n\treturn entry.get()\n};\nvar init = (fn) => (function(scopeName, a, b, c) {\n\tvar promise = __webpack_require__.I(scopeName);\n\tif (promise && promise.then) return promise.then(fn.bind(fn, scopeName, __webpack_require__.S[scopeName], a, b, c));\n\treturn fn(scopeName, __webpack_require__.S[scopeName], a, b, c);\n});\n\nvar load = /*#__PURE__*/ init((scopeName, scope, key) => {\n\tensureExistence(scopeName, key);\n\treturn get(findVersion(scope, key));\n});\nvar loadFallback = /*#__PURE__*/ init((scopeName, scope, key, fallback) => {\n\treturn scope && __webpack_require__.o(scope, key) ? get(findVersion(scope, key)) : fallback();\n});\nvar loadVersionCheck = /*#__PURE__*/ init((scopeName, scope, key, version) => {\n\tensureExistence(scopeName, key);\n\treturn get(findValidVersion(scope, key, version) || warnInvalidVersion(scope, scopeName, key, version) || findVersion(scope, key));\n});\nvar loadSingleton = /*#__PURE__*/ init((scopeName, scope, key) => {\n\tensureExistence(scopeName, key);\n\treturn getSingleton(scope, scopeName, key);\n});\nvar loadSingletonVersionCheck = /*#__PURE__*/ init((scopeName, scope, key, version) => {\n\tensureExistence(scopeName, key);\n\treturn getSingletonVersion(scope, scopeName, key, version);\n});\nvar loadStrictVersionCheck = /*#__PURE__*/ init((scopeName, scope, key, version) => {\n\tensureExistence(scopeName, key);\n\treturn getValidVersion(scope, scopeName, key, version);\n});\nvar loadStrictSingletonVersionCheck = /*#__PURE__*/ init((scopeName, scope, key, version) => {\n\tensureExistence(scopeName, key);\n\treturn getStrictSingletonVersion(scope, scopeName, key, version);\n});\nvar loadVersionCheckFallback = /*#__PURE__*/ init((scopeName, scope, key, version, fallback) => {\n\tif(!scope || !__webpack_require__.o(scope, key)) return fallback();\n\treturn get(findValidVersion(scope, key, version) || warnInvalidVersion(scope, scopeName, key, version) || findVersion(scope, key));\n});\nvar loadSingletonFallback = /*#__PURE__*/ init((scopeName, scope, key, fallback) => {\n\tif(!scope || !__webpack_require__.o(scope, key)) return fallback();\n\treturn getSingleton(scope, scopeName, key);\n});\nvar loadSingletonVersionCheckFallback = /*#__PURE__*/ init((scopeName, scope, key, version, fallback) => {\n\tif(!scope || !__webpack_require__.o(scope, key)) return fallback();\n\treturn getSingletonVersion(scope, scopeName, key, version);\n});\nvar loadStrictVersionCheckFallback = /*#__PURE__*/ init((scopeName, scope, key, version, fallback) => {\n\tvar entry = scope && __webpack_require__.o(scope, key) && findValidVersion(scope, key, version);\n\treturn entry ? get(entry) : fallback();\n});\nvar loadStrictSingletonVersionCheckFallback = /*#__PURE__*/ init((scopeName, scope, key, version, fallback) => {\n\tif(!scope || !__webpack_require__.o(scope, key)) return fallback();\n\treturn getStrictSingletonVersion(scope, scopeName, key, version);\n});\nvar installedModules = {};\nvar moduleToHandlerMapping = {\n\t\"webpack/sharing/consume/default/@jupyterlab/notebook\": () => (loadSingletonVersionCheck(\"default\", \"@jupyterlab/notebook\", [1,3,6,3])),\n\t\"webpack/sharing/consume/default/@lumino/coreutils\": () => (loadSingletonVersionCheck(\"default\", \"@lumino/coreutils\", [1,1,11,0])),\n\t\"webpack/sharing/consume/default/dexie/dexie\": () => (loadStrictVersionCheckFallback(\"default\", \"dexie\", [1,3,2,2], () => (__webpack_require__.e(\"vendors-node_modules_dexie_dist_modern_dexie_mjs\").then(() => (() => (__webpack_require__(/*! dexie */ \"./node_modules/dexie/dist/modern/dexie.mjs\"))))))),\n\t\"webpack/sharing/consume/default/axios/axios\": () => (loadStrictVersionCheckFallback(\"default\", \"axios\", [1,1,1,3], () => (__webpack_require__.e(\"vendors-node_modules_axios_index_js\").then(() => (() => (__webpack_require__(/*! axios */ \"./node_modules/axios/index.js\")))))))\n};\n// no consumes in initial chunks\nvar chunkMapping = {\n\t\"lib_index_js\": [\n\t\t\"webpack/sharing/consume/default/@jupyterlab/notebook\",\n\t\t\"webpack/sharing/consume/default/@lumino/coreutils\",\n\t\t\"webpack/sharing/consume/default/dexie/dexie\",\n\t\t\"webpack/sharing/consume/default/axios/axios\"\n\t]\n};\n__webpack_require__.f.consumes = (chunkId, promises) => {\n\tif(__webpack_require__.o(chunkMapping, chunkId)) {\n\t\tchunkMapping[chunkId].forEach((id) => {\n\t\t\tif(__webpack_require__.o(installedModules, id)) return promises.push(installedModules[id]);\n\t\t\tvar onFactory = (factory) => {\n\t\t\t\tinstalledModules[id] = 0;\n\t\t\t\t__webpack_require__.m[id] = (module) => {\n\t\t\t\t\tdelete __webpack_require__.c[id];\n\t\t\t\t\tmodule.exports = factory();\n\t\t\t\t}\n\t\t\t};\n\t\t\tvar onError = (error) => {\n\t\t\t\tdelete installedModules[id];\n\t\t\t\t__webpack_require__.m[id] = (module) => {\n\t\t\t\t\tdelete __webpack_require__.c[id];\n\t\t\t\t\tthrow error;\n\t\t\t\t}\n\t\t\t};\n\t\t\ttry {\n\t\t\t\tvar promise = moduleToHandlerMapping[id]();\n\t\t\t\tif(promise.then) {\n\t\t\t\t\tpromises.push(installedModules[id] = promise.then(onFactory)['catch'](onError));\n\t\t\t\t} else onFactory(promise);\n\t\t\t} catch(e) { onError(e); }\n\t\t});\n\t}\n}",
         "// no baseURI\n\n// object to store loaded and loading chunks\n// undefined = chunk not loaded, null = chunk preloaded/prefetched\n// [resolve, reject, Promise] = chunk loading, 0 = chunk loaded\nvar installedChunks = {\n\t\"knic-jupyter\": 0\n};\n\n__webpack_require__.f.j = (chunkId, promises) => {\n\t\t// JSONP chunk loading for javascript\n\t\tvar installedChunkData = __webpack_require__.o(installedChunks, chunkId) ? installedChunks[chunkId] : undefined;\n\t\tif(installedChunkData !== 0) { // 0 means \"already installed\".\n\n\t\t\t// a Promise means \"currently loading\".\n\t\t\tif(installedChunkData) {\n\t\t\t\tpromises.push(installedChunkData[2]);\n\t\t\t} else {\n\t\t\t\tif(true) { // all chunks have JS\n\t\t\t\t\t// setup Promise in chunk cache\n\t\t\t\t\tvar promise = new Promise((resolve, reject) => (installedChunkData = installedChunks[chunkId] = [resolve, reject]));\n\t\t\t\t\tpromises.push(installedChunkData[2] = promise);\n\n\t\t\t\t\t// start chunk loading\n\t\t\t\t\tvar url = __webpack_require__.p + __webpack_require__.u(chunkId);\n\t\t\t\t\t// create error before stack unwound to get useful stacktrace later\n\t\t\t\t\tvar error = new Error();\n\t\t\t\t\tvar loadingEnded = (event) => {\n\t\t\t\t\t\tif(__webpack_require__.o(installedChunks, chunkId)) {\n\t\t\t\t\t\t\tinstalledChunkData = installedChunks[chunkId];\n\t\t\t\t\t\t\tif(installedChunkData !== 0) installedChunks[chunkId] = undefined;\n\t\t\t\t\t\t\tif(installedChunkData) {\n\t\t\t\t\t\t\t\tvar errorType = event && (event.type === 'load' ? 'missing' : event.type);\n\t\t\t\t\t\t\t\tvar realSrc = event && event.target && event.target.src;\n\t\t\t\t\t\t\t\terror.message = 'Loading chunk ' + chunkId + ' failed.\\n(' + errorType + ': ' + realSrc + ')';\n\t\t\t\t\t\t\t\terror.name = 'ChunkLoadError';\n\t\t\t\t\t\t\t\terror.type = errorType;\n\t\t\t\t\t\t\t\terror.request = realSrc;\n\t\t\t\t\t\t\t\tinstalledChunkData[1](error);\n\t\t\t\t\t\t\t}\n\t\t\t\t\t\t}\n\t\t\t\t\t};\n\t\t\t\t\t__webpack_require__.l(url, loadingEnded, \"chunk-\" + chunkId, chunkId);\n\t\t\t\t} else installedChunks[chunkId] = 0;\n\t\t\t}\n\t\t}\n};\n\n// no prefetching\n\n// no preloaded\n\n// no HMR\n\n// no HMR manifest\n\n// no on chunks loaded\n\n// install a JSONP callback for chunk loading\nvar webpackJsonpCallback = (parentChunkLoadingFunction, data) => {\n\tvar [chunkIds, moreModules, runtime] = data;\n\t// add \"moreModules\" to the modules object,\n\t// then flag all \"chunkIds\" as loaded and fire callback\n\tvar moduleId, chunkId, i = 0;\n\tif(chunkIds.some((id) => (installedChunks[id] !== 0))) {\n\t\tfor(moduleId in moreModules) {\n\t\t\tif(__webpack_require__.o(moreModules, moduleId)) {\n\t\t\t\t__webpack_require__.m[moduleId] = moreModules[moduleId];\n\t\t\t}\n\t\t}\n\t\tif(runtime) var result = runtime(__webpack_require__);\n\t}\n\tif(parentChunkLoadingFunction) parentChunkLoadingFunction(data);\n\tfor(;i < chunkIds.length; i++) {\n\t\tchunkId = chunkIds[i];\n\t\tif(__webpack_require__.o(installedChunks, chunkId) && installedChunks[chunkId]) {\n\t\t\tinstalledChunks[chunkId][0]();\n\t\t}\n\t\tinstalledChunks[chunkId] = 0;\n\t}\n\n}\n\nvar chunkLoadingGlobal = self[\"webpackChunkknic_jupyter\"] = self[\"webpackChunkknic_jupyter\"] || [];\nchunkLoadingGlobal.forEach(webpackJsonpCallback.bind(null, 0));\nchunkLoadingGlobal.push = webpackJsonpCallback.bind(null, chunkLoadingGlobal.push.bind(chunkLoadingGlobal));",
         "__webpack_require__.nc = undefined;",
         "",
         "// module cache are used so entry inlining is disabled\n// startup\n// Load entry module and return exports\nvar __webpack_exports__ = __webpack_require__(\"webpack/container/entry/knic-jupyter\");\n",
         ""
```

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/style_index_js.f52bc77755c454c42949.js.map`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_axios_index_js.1ca6784f009c20db95e8.js.map`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_css-loader_dist_runtime_api_js-node_modules_css-loader_dist_runtime_cssW-72eba1.a0ffbb03a81b5fb1c68c.js.map`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js.map` & `knic_jupyter-0.1.7/knic-jupyter/labextension/static/vendors-node_modules_dexie_dist_modern_dexie_mjs.0aea58707561a10ac2f5.js.map`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/src/index.ts` & `knic_jupyter-0.1.7/src/index.ts`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/ui-tests/README.md` & `knic_jupyter-0.1.7/ui-tests/README.md`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/ui-tests/jupyter_server_test_config.py` & `knic_jupyter-0.1.7/ui-tests/jupyter_server_test_config.py`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/.gitignore` & `knic_jupyter-0.1.7/.gitignore`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/LICENSE` & `knic_jupyter-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/README.md` & `knic_jupyter-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/pyproject.toml` & `knic_jupyter-0.1.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `knic_jupyter-0.1.6/PKG-INFO` & `knic_jupyter-0.1.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: knic-jupyter
-Version: 0.1.6
+Version: 0.1.7
 Summary: A JupyterLab extension.
 Project-URL: Homepage, https://github.com/usc-isi-i2/knic-jupyter
 Project-URL: Bug Tracker, https://github.com/usc-isi-i2/knic-jupyter/issues
 Project-URL: Repository, https://github.com/usc-isi-i2/knic-jupyter.git
 License: MIT License
         
         Copyright (c) 2017 University of Southern California
```

