# Comparing `tmp/stocktracer-0.1.5.tar.gz` & `tmp/stocktracer-0.2.0.tar.gz`

## Comparing `stocktracer-0.1.5.tar` & `stocktracer-0.2.0.tar`

### file list

```diff
@@ -1,59 +1,70 @@
--rw-r--r--   0        0        0     5208 2020-02-02 00:00:00.000000 stocktracer-0.1.5/CODE_OF_CONDUCT.md
--rw-r--r--   0        0        0     1645 2020-02-02 00:00:00.000000 stocktracer-0.1.5/CONTRIBUTING.md
--rw-r--r--   0        0        0       53 2020-02-02 00:00:00.000000 stocktracer-0.1.5/Makefile
--rw-r--r--   0        0        0      564 2020-02-02 00:00:00.000000 stocktracer-0.1.5/Pipfile
--rw-r--r--   0        0        0    67701 2020-02-02 00:00:00.000000 stocktracer-0.1.5/Pipfile.lock
--rw-r--r--   0        0        0      482 2020-02-02 00:00:00.000000 stocktracer-0.1.5/SECURITY.md
--rwxr-xr-x   0        0        0      316 2020-02-02 00:00:00.000000 stocktracer-0.1.5/auto-format.sh
--rw-r--r--   0        0        0      479 2020-02-02 00:00:00.000000 stocktracer-0.1.5/conftest.py
--rw-r--r--   0        0        0     3192 2020-02-02 00:00:00.000000 stocktracer-0.1.5/mkdocs.yml
--rw-r--r--   0        0        0      194 2020-02-02 00:00:00.000000 stocktracer-0.1.5/pydocktest.json
--rw-r--r--   0        0        0     2289 2020-02-02 00:00:00.000000 stocktracer-0.1.5/requirements-dev.txt
--rw-r--r--   0        0        0      871 2020-02-02 00:00:00.000000 stocktracer-0.1.5/requirements.txt
--rw-r--r--   0        0        0      325 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/release.yml
--rw-r--r--   0        0        0      494 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0        0        0      604 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/ISSUE_TEMPLATE/feature_request.md
--rw-r--r--   0        0        0      916 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/cleanup.yml
--rw-r--r--   0        0        0      618 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/docs.yml
--rw-r--r--   0        0        0     1026 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/publish-pypi.yml
--rw-r--r--   0        0        0     3219 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/python.yml
--rw-r--r--   0        0        0      685 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/release-test.yml
--rw-r--r--   0        0        0      669 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.github/workflows/release.yml
--rw-r--r--   0        0        0     1014 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/gen_ref_pages.py
--rw-r--r--   0        0        0     2078 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/getting-started.md
--rw-r--r--   0        0        0     1322 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/index.md
--rw-r--r--   0        0        0     1429 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/analysis.md
--rw-r--r--   0        0        0      850 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/caching.md
--rw-r--r--   0        0        0    20504 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/data-retrieval.md
--rw-r--r--   0        0        0      372 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/index.md
--rw-r--r--   0        0        0     1598 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/reference.md
--rw-r--r--   0        0        0      854 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/design/report.md
--rw-r--r--   0        0        0      333 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/javascripts/mathjax.js
--rw-r--r--   0        0        0      184 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/javascripts/tablesort.js
--rw-r--r--   0        0        0      908 2020-02-02 00:00:00.000000 stocktracer-0.1.5/docs/stylesheets/extra.css
--rw-r--r--   0        0        0      128 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/__init__.py
--rw-r--r--   0        0        0      294 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/__main__.py
--rw-r--r--   0        0        0     2345 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/cli.py
--rw-r--r--   0        0        0      564 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/filter.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/analysis/__init__.py
--rw-r--r--   0        0        0     2418 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/analysis/diluted_eps.py
--rw-r--r--   0        0        0      937 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/analysis/stub.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/data/__init__.py
--rw-r--r--   0        0        0    19444 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/stocktracer/data/sec.py
--rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/.gitignore
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/__init__.py
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/test_filter.py
--rw-r--r--   0        0        0     7731 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/test_sec.py
--rw-r--r--   0        0        0     3251 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/test_sec_network.py
--rw-r--r--   0        0        0      547 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/test_xbrl.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/analysis/__init__.py
--rw-r--r--   0        0        0      797 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/analysis/test_diluted_eps.py
--rw-r--r--   0        0        0      655 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/analysis/test_stub.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/fixtures/__init__.py
--rw-r--r--   0        0        0      170 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/fixtures/network/__init__.py
--rw-r--r--   0        0        0      906 2020-02-02 00:00:00.000000 stocktracer-0.1.5/src/tests/fixtures/network/sec.py
--rw-r--r--   0        0        0     1883 2020-02-02 00:00:00.000000 stocktracer-0.1.5/.gitignore
--rw-r--r--   0        0        0    14197 2020-02-02 00:00:00.000000 stocktracer-0.1.5/LICENSE
--rw-r--r--   0        0        0     2557 2020-02-02 00:00:00.000000 stocktracer-0.1.5/README.md
--rw-r--r--   0        0        0     2655 2020-02-02 00:00:00.000000 stocktracer-0.1.5/pyproject.toml
--rw-r--r--   0        0        0    21104 2020-02-02 00:00:00.000000 stocktracer-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     5208 2020-02-02 00:00:00.000000 stocktracer-0.2.0/CODE_OF_CONDUCT.md
+-rw-r--r--   0        0        0     1645 2020-02-02 00:00:00.000000 stocktracer-0.2.0/CONTRIBUTING.md
+-rw-r--r--   0        0        0       53 2020-02-02 00:00:00.000000 stocktracer-0.2.0/Makefile
+-rw-r--r--   0        0        0      917 2020-02-02 00:00:00.000000 stocktracer-0.2.0/Pipfile
+-rw-r--r--   0        0        0   120246 2020-02-02 00:00:00.000000 stocktracer-0.2.0/Pipfile.lock
+-rw-r--r--   0        0        0      482 2020-02-02 00:00:00.000000 stocktracer-0.2.0/SECURITY.md
+-rwxr-xr-x   0        0        0      571 2020-02-02 00:00:00.000000 stocktracer-0.2.0/auto-format.sh
+-rw-r--r--   0        0        0      479 2020-02-02 00:00:00.000000 stocktracer-0.2.0/conftest.py
+-rw-r--r--   0        0        0     3266 2020-02-02 00:00:00.000000 stocktracer-0.2.0/mkdocs.yml
+-rw-r--r--   0        0        0      214 2020-02-02 00:00:00.000000 stocktracer-0.2.0/pydocktest.json
+-rw-r--r--   0        0        0      845 2020-02-02 00:00:00.000000 stocktracer-0.2.0/requirements.txt
+-rwxr-xr-x   0        0        0      366 2020-02-02 00:00:00.000000 stocktracer-0.2.0/smoke-test.sh
+-rw-r--r--   0        0        0      765 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/dependabot.yml
+-rw-r--r--   0        0        0     1269 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/pull_request_template.md
+-rw-r--r--   0        0        0      325 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/release.yml
+-rw-r--r--   0        0        0      494 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      604 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0        0        0      916 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/cleanup.yml
+-rw-r--r--   0        0        0     3473 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/codeql.yml
+-rw-r--r--   0        0        0      993 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/docs.yml
+-rw-r--r--   0        0        0     1138 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/publish-pypi.yml
+-rw-r--r--   0        0        0     4370 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/python.yml
+-rw-r--r--   0        0        0      685 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/release-test.yml
+-rw-r--r--   0        0        0      669 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.github/workflows/release.yml
+-rw-r--r--   0        0        0     1019 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/gen_ref_pages.py
+-rw-r--r--   0        0        0     1906 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/getting-started.md
+-rw-r--r--   0        0        0      721 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/index.md
+-rw-r--r--   0        0        0     1429 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/analysis.md
+-rw-r--r--   0        0        0      850 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/caching.md
+-rw-r--r--   0        0        0    20504 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/data-retrieval.md
+-rw-r--r--   0        0        0      372 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/index.md
+-rw-r--r--   0        0        0     1598 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/reference.md
+-rw-r--r--   0        0        0      854 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/design/report.md
+-rw-r--r--   0        0        0      333 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/javascripts/mathjax.js
+-rw-r--r--   0        0        0      184 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/javascripts/tablesort.js
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/__init__.py
+-rw-r--r--   0        0        0      854 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/__main__.py
+-rw-r--r--   0        0        0     5864 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/cli.py
+-rw-r--r--   0        0        0      633 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/filter.py
+-rw-r--r--   0        0        0     1363 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/interface.py
+-rw-r--r--   0        0        0       51 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/analysis/__init__.py
+-rw-r--r--   0        0        0     1280 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/analysis/annual_reports.py
+-rw-r--r--   0        0        0     2101 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/analysis/diluted_eps.py
+-rw-r--r--   0        0        0      655 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/analysis/stub.py
+-rw-r--r--   0        0        0       70 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/data/__init__.py
+-rw-r--r--   0        0        0    23631 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/stocktracer/data/sec.py
+-rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/.gitignore
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/__init__.py
+-rw-r--r--   0        0        0      938 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/test_cli.py
+-rw-r--r--   0        0        0     1164 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/test_filter.py
+-rw-r--r--   0        0        0      485 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/test_main.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/analysis/__init__.py
+-rw-r--r--   0        0        0      961 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/analysis/test_annual_reports.py
+-rw-r--r--   0        0        0     1023 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/analysis/test_diluted_eps.py
+-rw-r--r--   0        0        0      655 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/analysis/test_stub.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/fixtures/__init__.py
+-rw-r--r--   0        0        0      587 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/fixtures/network.py
+-rw-r--r--   0        0        0     7126 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/fixtures/unit.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/__init__.py
+-rw-r--r--   0        0        0     6507 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/test_DataSelector.py
+-rw-r--r--   0        0        0     1875 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/test_DataSetReader.py
+-rw-r--r--   0        0        0     2202 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/test_filter.py
+-rw-r--r--   0        0        0     3545 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/test_network.py
+-rw-r--r--   0        0        0     7257 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/src/tests/sec/test_sec.py
+-rw-r--r--   0        0        0      908 2020-02-02 00:00:00.000000 stocktracer-0.2.0/docs/stylesheets/extra.css
+-rw-r--r--   0        0        0     1902 2020-02-02 00:00:00.000000 stocktracer-0.2.0/.gitignore
+-rw-r--r--   0        0        0    14197 2020-02-02 00:00:00.000000 stocktracer-0.2.0/LICENSE
+-rw-r--r--   0        0        0     3201 2020-02-02 00:00:00.000000 stocktracer-0.2.0/README.md
+-rw-r--r--   0        0        0     3622 2020-02-02 00:00:00.000000 stocktracer-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0    21809 2020-02-02 00:00:00.000000 stocktracer-0.2.0/PKG-INFO
```

### Comparing `stocktracer-0.1.5/CODE_OF_CONDUCT.md` & `stocktracer-0.2.0/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/CONTRIBUTING.md` & `stocktracer-0.2.0/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/Pipfile.lock` & `stocktracer-0.2.0/Pipfile.lock`

 * *Files 21% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.694546568627451%*

 * *Differences: {"'_meta'": "{'hash': {'sha256': "*

 * *            "'f4a3a7db8986818c8371ea6201e219a82f625300e4d58155576451d9883fcbe0'}}",*

 * * "'default'": "{'certifi': {'hashes': "*

 * *              "['sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7', "*

 * *              "'sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716'], "*

 * *              "'version': '==2023.5.7'}, 'platformdirs': {'hashes': "*

 * *              "['sha256:412dae91f52a6f84830f39a8078cecd0e866cb72294a5c66808e74d5e88d251f', "*

 * *     […]*

```diff
@@ -1,11 +1,11 @@
 {
     "_meta": {
         "hash": {
-            "sha256": "003e4b1a7014839cb7087349f973ddf490cfc0162cccb195262c5f25d5dd1c2e"
+            "sha256": "f4a3a7db8986818c8371ea6201e219a82f625300e4d58155576451d9883fcbe0"
         },
         "pipfile-spec": 6,
         "requires": {
             "python_version": "3.10"
         },
         "sources": [
             {
@@ -20,29 +20,37 @@
             "hashes": [
                 "sha256:1f28b4522cdc2fb4256ac1a020c78acf9cba2c6b461ccd2c126f3aa8e8335d04",
                 "sha256:6279836d581513a26f1bf235f9acd333bc9115683f14f7e8fae46c98fc50e015"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==23.1.0"
         },
+        "beartype": {
+            "hashes": [
+                "sha256:546e6e8dcdda1d6d9f906ea4eb1518aa01c9c5f5a440e495917b2daf53cbd598",
+                "sha256:8010a34921dfd5c074ea09c5f3a67a90a97492d41d2977c053a46e7d43816644"
+            ],
+            "index": "pypi",
+            "version": "==0.14.0"
+        },
         "cattrs": {
             "hashes": [
                 "sha256:bc12b1f0d000b9f9bee83335887d532a1d3e99a833d1bf0882151c97d3e68c21",
                 "sha256:f0eed5642399423cf656e7b66ce92cdc5b963ecafd041d1b24d136fdde7acf6d"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==22.2.0"
         },
         "certifi": {
             "hashes": [
-                "sha256:35824b4c3a97115964b408844d64aa14db1cc518f6562e8d7261699d1350a9e3",
-                "sha256:4ad3232f5e926d6718ec31cfc1fcadfde020920e278684144551c91769c7bc18"
+                "sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7",
+                "sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716"
             ],
             "markers": "python_version >= '3.6'",
-            "version": "==2022.12.7"
+            "version": "==2023.5.7"
         },
         "charset-normalizer": {
             "hashes": [
                 "sha256:04afa6387e2b282cf78ff3dbce20f0cc071c12dc8f685bd40960cc68644cfea6",
                 "sha256:04eefcee095f58eaabe6dc3cc2262f3bcd776d2c67005880894f447b3f2cb9c1",
                 "sha256:0be65ccf618c1e7ac9b849c315cc2e8a8751d9cfdaa43027d4f6624bd587ab7e",
                 "sha256:0c95f12b74681e9ae127728f7e5409cbbef9cd914d5896ef238cc779b8152373",
@@ -117,14 +125,22 @@
                 "sha256:f645caaf0008bacf349875a974220f1f1da349c5dbe7c4ec93048cdc785a3326",
                 "sha256:f8303414c7b03f794347ad062c0516cee0e15f7a612abd0ce1e25caf6ceb47df",
                 "sha256:fca62a8301b605b954ad2e9c3666f9d97f63872aa4efcae5492baca2056b74ab"
             ],
             "markers": "python_full_version >= '3.7.0'",
             "version": "==3.1.0"
         },
+        "diskcache": {
+            "hashes": [
+                "sha256:558c6a2d5d7c721bb00e40711803d6804850c9f76c426ed81ecc627fe9d2ce2d",
+                "sha256:e4c978532feff5814c4cc00fe1e11e40501985946643d73220d41ee7737c72c3"
+            ],
+            "index": "pypi",
+            "version": "==5.6.1"
+        },
         "exceptiongroup": {
             "hashes": [
                 "sha256:232c37c63e4f682982c8b6459f33a8981039e5fb8756b2074364e5055c498c9e",
                 "sha256:d484c3090ba2889ae2928419117447a14daf3c1231d5e30d0aae34f354f01785"
             ],
             "markers": "python_version < '3.11'",
             "version": "==1.1.1"
@@ -207,19 +223,19 @@
                 "sha256:fe7914d8ddb2d54b900cec264c090b88d141a1eed605c9539a187dbc2547f022"
             ],
             "index": "pypi",
             "version": "==2.0.1"
         },
         "platformdirs": {
             "hashes": [
-                "sha256:47692bc24c1958e8b0f13dd727307cff1db103fca36399f457da8e05f222fdc4",
-                "sha256:7954a68d0ba23558d753f73437c55f89027cf8f5108c19844d4b82e5af396335"
+                "sha256:412dae91f52a6f84830f39a8078cecd0e866cb72294a5c66808e74d5e88d251f",
+                "sha256:e2378146f1964972c03c085bb5662ae80b2b8c06226c54b2ff4aa9483e8a13a5"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==3.5.0"
+            "version": "==3.5.1"
         },
         "python-dateutil": {
             "hashes": [
                 "sha256:0123cacc1627ae19ddf3c27a5de5bd67ee4586fbdd6440d9748f8abb483d3e86",
                 "sha256:961d03dc3453ebbc59dbdea9e4e11c5651520a876d0f4db161e8674aae935da9"
             ],
             "index": "pypi",
@@ -230,19 +246,19 @@
                 "sha256:1d8ce29db189191fb55338ee6d0387d82ab59f3d00eac103412d64e0ebd0c588",
                 "sha256:a151b3abb88eda1d4e34a9814df37de2a80e301e68ba0fd856fb9b46bfbbbffb"
             ],
             "version": "==2023.3"
         },
         "requests": {
             "hashes": [
-                "sha256:e8f3c9be120d3333921d213eef078af392fba3933ab7ed2d1cba3b56f2568c3b",
-                "sha256:f2e34a75f4749019bb0e3effb66683630e4ffeaf75819fb51bebef1bf5aef059"
+                "sha256:10e94cc4f3121ee6da529d358cdaeaff2f1c409cd377dbc72b825852f2f7e294",
+                "sha256:239d7d4458afcb28a692cdd298d87542235f4ca8d36d03a15bfc128a6559a2f4"
             ],
             "index": "pypi",
-            "version": "==2.29.0"
+            "version": "==2.30.0"
         },
         "requests-cache": {
             "hashes": [
                 "sha256:55c5765c26fd98a38c633d6e3931a507b7708cdd07c0afb48773d0718ac15969",
                 "sha256:d42e6c2f11de54e6a134c9a00c5ca2a3c8edde3c3f2bdfd942586fafa8990e14"
             ],
             "index": "pypi",
@@ -286,22 +302,38 @@
                 "sha256:ec3c301f04e5bb676d333a7fa162fa977ad2ca04b7e652bfc9fac4e405728eed"
             ],
             "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'",
             "version": "==1.4.3"
         },
         "urllib3": {
             "hashes": [
-                "sha256:8a388717b9476f934a21484e8c8e61875ab60644d29b9b39e11e4b9dc1c6b305",
-                "sha256:aa751d169e23c7479ce47a0cb0da579e3ede798f994f5816a74e4f4500dcea42"
+                "sha256:61717a1095d7e155cdb737ac7bb2f4324a858a1e2e6466f6d03ff630ca68d3cc",
+                "sha256:d055c2f9d38dc53c808f6fdc8eab7360b6fdbbde02340ed25cfbcd817c62469e"
             ],
-            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'",
-            "version": "==1.26.15"
+            "markers": "python_version >= '3.7'",
+            "version": "==2.0.2"
         }
     },
     "develop": {
+        "astroid": {
+            "hashes": [
+                "sha256:a1b8543ef9d36ea777194bc9b17f5f8678d2c56ee6a45b2c2f17eec96f242347",
+                "sha256:c81e1c7fbac615037744d067a9bb5f9aeb655edf59b63ee8b59585475d6f80d8"
+            ],
+            "markers": "python_full_version >= '3.7.2'",
+            "version": "==2.15.4"
+        },
+        "babel": {
+            "hashes": [
+                "sha256:b4246fb7677d3b98f501a39d43396d3cafdc8eadb045f4a31be01863f655c610",
+                "sha256:cc2d99999cd01d44420ae725a21c9e3711b3aadc7976d6147f622d8581963455"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.12.1"
+        },
         "black": {
             "hashes": [
                 "sha256:064101748afa12ad2291c2b91c960be28b817c0c7eaa35bec09cc63aa56493c5",
                 "sha256:0945e13506be58bf7db93ee5853243eb368ace1c08a24c65ce108986eac65915",
                 "sha256:11c410f71b876f961d1de77b9699ad19f939094c3a677323f43d7a29855fe326",
                 "sha256:1c7b8d606e728a41ea1ccbd7264677e494e87cf630e399262ced92d4a8dac940",
                 "sha256:1d06691f1eb8de91cd1b322f21e3bfc9efe0c7ca1f0e1eb1db44ea367dff656b",
@@ -335,19 +367,19 @@
                 "sha256:d5b71264afdb5951d6704482aac78de887c80691c52b88a9ad195983ca2c9269"
             ],
             "index": "pypi",
             "version": "==0.10.0"
         },
         "certifi": {
             "hashes": [
-                "sha256:35824b4c3a97115964b408844d64aa14db1cc518f6562e8d7261699d1350a9e3",
-                "sha256:4ad3232f5e926d6718ec31cfc1fcadfde020920e278684144551c91769c7bc18"
+                "sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7",
+                "sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716"
             ],
             "markers": "python_version >= '3.6'",
-            "version": "==2022.12.7"
+            "version": "==2023.5.7"
         },
         "charset-normalizer": {
             "hashes": [
                 "sha256:04afa6387e2b282cf78ff3dbce20f0cc071c12dc8f685bd40960cc68644cfea6",
                 "sha256:04eefcee095f58eaabe6dc3cc2262f3bcd776d2c67005880894f447b3f2cb9c1",
                 "sha256:0be65ccf618c1e7ac9b849c315cc2e8a8751d9cfdaa43027d4f6624bd587ab7e",
                 "sha256:0c95f12b74681e9ae127728f7e5409cbbef9cd914d5896ef238cc779b8152373",
@@ -502,14 +534,22 @@
             "hashes": [
                 "sha256:b32a8bb5d2df585207c119d6c01567b81fba690c9c10a753bfe27a335bfc43ea",
                 "sha256:f42015f31d386b351d4226389b387ae173207058832fbf5c8ec4b40e27b16026"
             ],
             "index": "pypi",
             "version": "==3.3.1"
         },
+        "dill": {
+            "hashes": [
+                "sha256:a07ffd2351b8c678dfc4a856a3005f8067aea51d6ba6c700796a4d9e280f39f0",
+                "sha256:e5db55f3687856d8fbdab002ed78544e1c4559a130302693d839dfe8f93f2373"
+            ],
+            "markers": "python_version < '3.11'",
+            "version": "==0.3.6"
+        },
         "docopt": {
             "hashes": [
                 "sha256:49b3a825280bd66b3aa83585ef59c4a8c82f2c8a522dbe754a8bc8d08c85c491"
             ],
             "version": "==0.6.2"
         },
         "exceptiongroup": {
@@ -523,21 +563,37 @@
         "ghp-import": {
             "hashes": [
                 "sha256:8337dd7b50877f163d4c0289bc1f1c7f127550241988d568c1db512c4324a619",
                 "sha256:9c535c4c61193c2df8871222567d7fd7e5014d835f97dc7b7439069e2413d343"
             ],
             "version": "==2.1.0"
         },
+        "gitdb": {
+            "hashes": [
+                "sha256:6eb990b69df4e15bad899ea868dc46572c3f75339735663b81de79b06f17eb9a",
+                "sha256:c286cf298426064079ed96a9e4a9d39e7f3e9bf15ba60701e95f5492f28415c7"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==4.0.10"
+        },
+        "gitpython": {
+            "hashes": [
+                "sha256:8ce3bcf69adfdf7c7d503e78fd3b1c492af782d58893b650adb2ac8912ddd573",
+                "sha256:f04893614f6aa713a60cbbe1e6a97403ef633103cdd0ef5eb6efe0deb98dbe8d"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==3.1.31"
+        },
         "griffe": {
             "hashes": [
-                "sha256:833990074c8c0b323a55f37f72265fdd841cb0a756122303505bf4bc80800e82",
-                "sha256:8d6bc40e7bede3fb5879598c1f71b8902d245804ab59ae55516f864b2bdc25c6"
+                "sha256:088c25fb22f8d1f1add5d3b58a86a3969993181a36ca55b3fa33096a3f3b1a23",
+                "sha256:685350067286229e80a18b8989d6acbd43abdf8b763591221d19c56f4108549e"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==0.27.2"
+            "version": "==0.27.4"
         },
         "idna": {
             "hashes": [
                 "sha256:814f528e8dead7d329833b91c5faa87d60bf71824cd12a7530b5526063d02cb4",
                 "sha256:90b77e79eaa3eba6de819a0c442c0b4ceefc341a7a2ab77d7562bf49f425c5c2"
             ],
             "markers": "python_version >= '3.5'",
@@ -563,14 +619,56 @@
             "hashes": [
                 "sha256:31351a702a408a9e7595a8fc6150fc3f43bb6bf7e319770cbc0db9df9437e852",
                 "sha256:6088930bfe239f0e6710546ab9c19c9ef35e29792895fed6e6e31a023a182a61"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==3.1.2"
         },
+        "lazy-object-proxy": {
+            "hashes": [
+                "sha256:09763491ce220c0299688940f8dc2c5d05fd1f45af1e42e636b2e8b2303e4382",
+                "sha256:0a891e4e41b54fd5b8313b96399f8b0e173bbbfc03c7631f01efbe29bb0bcf82",
+                "sha256:189bbd5d41ae7a498397287c408617fe5c48633e7755287b21d741f7db2706a9",
+                "sha256:18b78ec83edbbeb69efdc0e9c1cb41a3b1b1ed11ddd8ded602464c3fc6020494",
+                "sha256:1aa3de4088c89a1b69f8ec0dcc169aa725b0ff017899ac568fe44ddc1396df46",
+                "sha256:212774e4dfa851e74d393a2370871e174d7ff0ebc980907723bb67d25c8a7c30",
+                "sha256:2d0daa332786cf3bb49e10dc6a17a52f6a8f9601b4cf5c295a4f85854d61de63",
+                "sha256:5f83ac4d83ef0ab017683d715ed356e30dd48a93746309c8f3517e1287523ef4",
+                "sha256:659fb5809fa4629b8a1ac5106f669cfc7bef26fbb389dda53b3e010d1ac4ebae",
+                "sha256:660c94ea760b3ce47d1855a30984c78327500493d396eac4dfd8bd82041b22be",
+                "sha256:66a3de4a3ec06cd8af3f61b8e1ec67614fbb7c995d02fa224813cb7afefee701",
+                "sha256:721532711daa7db0d8b779b0bb0318fa87af1c10d7fe5e52ef30f8eff254d0cd",
+                "sha256:7322c3d6f1766d4ef1e51a465f47955f1e8123caee67dd641e67d539a534d006",
+                "sha256:79a31b086e7e68b24b99b23d57723ef7e2c6d81ed21007b6281ebcd1688acb0a",
+                "sha256:81fc4d08b062b535d95c9ea70dbe8a335c45c04029878e62d744bdced5141586",
+                "sha256:8fa02eaab317b1e9e03f69aab1f91e120e7899b392c4fc19807a8278a07a97e8",
+                "sha256:9090d8e53235aa280fc9239a86ae3ea8ac58eff66a705fa6aa2ec4968b95c821",
+                "sha256:946d27deaff6cf8452ed0dba83ba38839a87f4f7a9732e8f9fd4107b21e6ff07",
+                "sha256:9990d8e71b9f6488e91ad25f322898c136b008d87bf852ff65391b004da5e17b",
+                "sha256:9cd077f3d04a58e83d04b20e334f678c2b0ff9879b9375ed107d5d07ff160171",
+                "sha256:9e7551208b2aded9c1447453ee366f1c4070602b3d932ace044715d89666899b",
+                "sha256:9f5fa4a61ce2438267163891961cfd5e32ec97a2c444e5b842d574251ade27d2",
+                "sha256:b40387277b0ed2d0602b8293b94d7257e17d1479e257b4de114ea11a8cb7f2d7",
+                "sha256:bfb38f9ffb53b942f2b5954e0f610f1e721ccebe9cce9025a38c8ccf4a5183a4",
+                "sha256:cbf9b082426036e19c6924a9ce90c740a9861e2bdc27a4834fd0a910742ac1e8",
+                "sha256:d9e25ef10a39e8afe59a5c348a4dbf29b4868ab76269f81ce1674494e2565a6e",
+                "sha256:db1c1722726f47e10e0b5fdbf15ac3b8adb58c091d12b3ab713965795036985f",
+                "sha256:e7c21c95cae3c05c14aafffe2865bbd5e377cfc1348c4f7751d9dc9a48ca4bda",
+                "sha256:e8c6cfb338b133fbdbc5cfaa10fe3c6aeea827db80c978dbd13bc9dd8526b7d4",
+                "sha256:ea806fd4c37bf7e7ad82537b0757999264d5f70c45468447bb2b91afdbe73a6e",
+                "sha256:edd20c5a55acb67c7ed471fa2b5fb66cb17f61430b7a6b9c3b4a1e40293b1671",
+                "sha256:f0117049dd1d5635bbff65444496c90e0baa48ea405125c088e93d9cf4525b11",
+                "sha256:f0705c376533ed2a9e5e97aacdbfe04cecd71e0aa84c7c0595d02ef93b6e4455",
+                "sha256:f12ad7126ae0c98d601a7ee504c1122bcef553d1d5e0c3bfa77b16b3968d2734",
+                "sha256:f2457189d8257dd41ae9b434ba33298aec198e30adf2dcdaaa3a28b9994f6adb",
+                "sha256:f699ac1c768270c9e384e4cbd268d6e67aebcfae6cd623b4d7c3bfde5a35db59"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==1.9.0"
+        },
         "markdown": {
             "hashes": [
                 "sha256:cbb516f16218e643d8e0a95b309f77eb118cb138d39a4f27851e6a63581db874",
                 "sha256:f5da449a6e1c989a4cea2631aa8ee67caa5a2ef855d551c88f9e309f4634c621"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==3.3.7"
@@ -627,14 +725,22 @@
                 "sha256:f1cd098434e83e656abf198f103a8207a8187c0fc110306691a2e94a78d0abb2",
                 "sha256:f2bfb563d0211ce16b63c7cb9395d2c682a23187f54c3d79bfec33e6705473c6",
                 "sha256:f8ffb705ffcf5ddd0e80b65ddf7bed7ee4f5a441ea7d3419e861a12eaf41af58"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==2.1.2"
         },
+        "mccabe": {
+            "hashes": [
+                "sha256:348e0240c33b60bbdf4e523192ef919f28cb2c3d7d5c7794f74009290f236325",
+                "sha256:6c2d30ab6be0e4a46919781807b4f0d834ebdd6c6e3dca0bda5a15f863427b6e"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==0.7.0"
+        },
         "mergedeep": {
             "hashes": [
                 "sha256:0096d52e9dad9939c3d975a774666af186eda617e6ca84df4c94dec30004f2a8",
                 "sha256:70775750742b25c0d8f36c55aed03d24c3384d17c951b3175d898bd778ef0307"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==1.3.4"
@@ -659,29 +765,37 @@
             "hashes": [
                 "sha256:4c7cf256b5d67062a788f6b1d035e157fc1a9498c2399be9af5257d4ff4d19bc",
                 "sha256:7ac060096f3f40bd19039e7277dd3050be9a453c8ac578645844d4d91d7978ea"
             ],
             "index": "pypi",
             "version": "==0.5.0"
         },
+        "mkdocs-git-revision-date-localized-plugin": {
+            "hashes": [
+                "sha256:540b9c930d8d48630c090b72ac2c3900ac2ed0799b23738a33b88e31f5198fe7",
+                "sha256:7752edd7c4dcaa9383e9a5b6a4f729831a62d604b0c43b319331127720c6a2bf"
+            ],
+            "index": "pypi",
+            "version": "==1.2.0"
+        },
         "mkdocs-literate-nav": {
             "hashes": [
                 "sha256:81ccbea18163ae8e10bd0bd39237fe70c32a1f2dff6c170779f5d52dd98a0470",
                 "sha256:8c1b84714e5974da5e44e011ec0069275ae7647270c13a679662cf6ffce675a4"
             ],
             "index": "pypi",
             "version": "==0.6.0"
         },
         "mkdocs-material": {
             "hashes": [
-                "sha256:74d8da1371ab3a326868fe47bae3cbc4aa22e93c048b4ca5117e6817b88bd734",
-                "sha256:7db24261cb17400e132c46d17eea712bfe71056d892a9beba32cf68210297141"
+                "sha256:f5d473eb79d6640a5e668d4b2ab5b9de5e76ae0a0e2d864112df0cfe9016dc1d",
+                "sha256:fbc86d50ec2cf34d40d5c4365780f290ceedde23f1a0704323b34e7f16b0c0dd"
             ],
             "index": "pypi",
-            "version": "==9.1.9"
+            "version": "==9.1.11"
         },
         "mkdocs-material-extensions": {
             "hashes": [
                 "sha256:9c003da71e2cc2493d910237448c672e00cefc800d3d6ae93d2fc69979e3bd93",
                 "sha256:e41d9f38e4798b6617ad98ca8f7f1157b1e4385ac1459ca1e4ea219b556df945"
             ],
             "index": "pypi",
@@ -701,19 +815,19 @@
                 "sha256:949ef8da92df9d692ca07be50616459a6b536083a25520fd54b00e8814ce019b"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==0.21.2"
         },
         "mkdocstrings-python": {
             "hashes": [
-                "sha256:00e02b5d3d444f9abdec2398f9ba0c73e15deab78685f793f5801fd4d62a5b6f",
-                "sha256:da0a54d7d46523a25a5227f0ecc74b491291bd9d36fc71445bfb0ea64283e287"
+                "sha256:b89d849df990204f909d5452548b6936a185f912da06208a93909bebe25d6e67",
+                "sha256:c59d67009a7a85172f4da990d8523e95606b6a1ff93a22a2351ad3b5f8cafed1"
             ],
             "index": "pypi",
-            "version": "==0.9.0"
+            "version": "==1.0.0"
         },
         "mock": {
             "hashes": [
                 "sha256:06f18d7d65b44428202b145a9a36e99c2ee00d1eb992df0caf881d4664377891",
                 "sha256:0e0bc5ba78b8db3667ad636d964eb963dc97a59f04c6f6214c5f0e4a8f726c56"
             ],
             "index": "pypi",
@@ -741,19 +855,19 @@
                 "sha256:d8af70af76652554bd134c22b3e8a1cc46ed7d91edcdd721ef1a0c51a84a5293"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==0.11.1"
         },
         "platformdirs": {
             "hashes": [
-                "sha256:47692bc24c1958e8b0f13dd727307cff1db103fca36399f457da8e05f222fdc4",
-                "sha256:7954a68d0ba23558d753f73437c55f89027cf8f5108c19844d4b82e5af396335"
+                "sha256:412dae91f52a6f84830f39a8078cecd0e866cb72294a5c66808e74d5e88d251f",
+                "sha256:e2378146f1964972c03c085bb5662ae80b2b8c06226c54b2ff4aa9483e8a13a5"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==3.5.0"
+            "version": "==3.5.1"
         },
         "pluggy": {
             "hashes": [
                 "sha256:4224373bacce55f955a878bf9cfa763c1e360858e330072059e10bad68531159",
                 "sha256:74134bbf457f031a36d68416e1509f34bd5ccc019f0bcc952c7b909d06b37bd3"
             ],
             "markers": "python_version >= '3.6'",
@@ -762,14 +876,25 @@
         "py-cpuinfo": {
             "hashes": [
                 "sha256:3cdbbf3fac90dc6f118bfd64384f309edeadd902d7c8fb17f02ffa1fc3f49690",
                 "sha256:859625bc251f64e21f077d099d4162689c762b5d6a4c3c97553d56241c9674d5"
             ],
             "version": "==9.0.0"
         },
+        "pydocstyle": {
+            "extras": [
+                "toml"
+            ],
+            "hashes": [
+                "sha256:118762d452a49d6b05e194ef344a55822987a462831ade91ec5c06fd2169d019",
+                "sha256:7ce43f0c0ac87b07494eb9c0b462c0b73e6ff276807f204d6b53edc72b7e44e1"
+            ],
+            "index": "pypi",
+            "version": "==6.3.0"
+        },
         "pydoctest": {
             "hashes": [
                 "sha256:5a218e10d7d1ec3acdf3d3c93b09ab64920846a464fd8880dcd263c67f27793a",
                 "sha256:696b82d8207ff791c6c9e9cf98f7af05563daded229108520a23d1ac4e8a2ce0"
             ],
             "index": "pypi",
             "version": "==0.1.22"
@@ -778,14 +903,22 @@
             "hashes": [
                 "sha256:8ace4d3c1dd481894b2005f560ead0f9f19ee64fe983366be1a21e171d12775c",
                 "sha256:db2db3deb4b4179f399a09054b023b6a586b76499d36965813c71aa8ed7b5fd1"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==2.15.1"
         },
+        "pylint": {
+            "hashes": [
+                "sha256:5dcf1d9e19f41f38e4e85d10f511e5b9c35e1aa74251bf95cdd8cb23584e2db1",
+                "sha256:7a1145fb08c251bdb5cca11739722ce64a63db479283d10ce718b2460e54123c"
+            ],
+            "index": "pypi",
+            "version": "==2.17.4"
+        },
         "pymdown-extensions": {
             "hashes": [
                 "sha256:a499191d8d869f30339de86fcf072a787e86c42b6f16f280f5c2cf174182b7f3",
                 "sha256:f7e86c1d3981f23d9dc43294488ecb54abadd05b0be4bf8f0e15efc90f7853ff"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==9.11"
@@ -826,14 +959,21 @@
             "hashes": [
                 "sha256:0123cacc1627ae19ddf3c27a5de5bd67ee4586fbdd6440d9748f8abb483d3e86",
                 "sha256:961d03dc3453ebbc59dbdea9e4e11c5651520a876d0f4db161e8674aae935da9"
             ],
             "index": "pypi",
             "version": "==2.8.2"
         },
+        "pytz": {
+            "hashes": [
+                "sha256:1d8ce29db189191fb55338ee6d0387d82ab59f3d00eac103412d64e0ebd0c588",
+                "sha256:a151b3abb88eda1d4e34a9814df37de2a80e301e68ba0fd856fb9b46bfbbbffb"
+            ],
+            "version": "==2023.3"
+        },
         "pyyaml": {
             "hashes": [
                 "sha256:01b45c0191e6d66c470b6cf1b9531a771a83c1c4208272ead47a3ae4f2f603bf",
                 "sha256:0283c35a6a9fbf047493e3a0ce8d79ef5030852c51e9d911a27badfde0605293",
                 "sha256:055d937d65826939cb044fc8c9b08889e8c743fdc6a32b33e2390f66013e449b",
                 "sha256:07751360502caac1c067a8132d150cf3d61339af5691fe9e87803040dbc5db57",
                 "sha256:0b4624f379dab24d3725ffde76559cff63d9ec94e1736b556dacdfebe5ab6d4b",
@@ -976,66 +1116,744 @@
                 "sha256:fee0016cc35a8a91e8cc9312ab26a6fe638d484131a7afa79e1ce6165328a135"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==2023.5.5"
         },
         "requests": {
             "hashes": [
-                "sha256:e8f3c9be120d3333921d213eef078af392fba3933ab7ed2d1cba3b56f2568c3b",
-                "sha256:f2e34a75f4749019bb0e3effb66683630e4ffeaf75819fb51bebef1bf5aef059"
+                "sha256:10e94cc4f3121ee6da529d358cdaeaff2f1c409cd377dbc72b825852f2f7e294",
+                "sha256:239d7d4458afcb28a692cdd298d87542235f4ca8d36d03a15bfc128a6559a2f4"
             ],
             "index": "pypi",
-            "version": "==2.29.0"
+            "version": "==2.30.0"
         },
         "ruff": {
             "hashes": [
-                "sha256:04ec5d75e4bca754cedd20d53e2ba4920d6259e7579abfb2e8e30c3c80e41b17",
-                "sha256:05ee163a046fc593d150179d23f4af447fb82f3e59cd34e031ea0868c65bb8e8",
-                "sha256:068a82a29d80848a56e3d9d4308e6e0ca8b2ecdaf5ac342a292545a59b7f2c21",
-                "sha256:18a29ed37bf8cfe6dce8a2db56c313a64c0804095108753621f3c3321e0c9c5f",
-                "sha256:323ae6c1702b26c96d0fbf939c5959c37e79021f86b70f63634df918bc77f36e",
-                "sha256:3e2c38449548e122f2612843a7c04e22b4fd491656955c57b8cb05df11639ad6",
-                "sha256:4564e0f245eb515c6ed63988c21e9c40bcfd485cd1ec63bdd790f9a81d301f15",
-                "sha256:484e395d1984ab9e1e66bd42e7a5192decfee86998d07d36ee50b2fadccc8734",
-                "sha256:5a8658ebcc37d62f72840cbdf564171c1a2b6831db482b4d917962541a2f4a44",
-                "sha256:67326fdc9ac0a1b13e229c6e24e8d115863c52cd710faaaaa588851535281d6c",
-                "sha256:71fd865ebacc1083259b3fb7e3eb45235a86e62e21830b8a6b067be0ec54aa2e",
-                "sha256:8fcd4b693ca1374eb7a5796581c90689f884f98f388740d94f0702fd30f8f78f",
-                "sha256:91c6eb4f979b661a2dd850d9ac803842bb7b66d4926de84f09c787af82590f73",
-                "sha256:cd4f60ffc3eb15802c554a9c8581bf2117c4d3d06fbc57e0ba58f04cb1aaa47f",
-                "sha256:d628de91e2be7a83128526636097d2dd890669a06143f826f6c591d79aeefbc4",
-                "sha256:d97ba8db0fb601ffe9ee996ebb97c698e427a2fd4514fefbe7b803111354f783",
-                "sha256:ec2fa192c035b8b68cc2b91049c561cd69543e2b8c4d157d9aa7727320bedcca"
+                "sha256:1d5a8de2fbaf91ea5699451a06f4074e7a312accfa774ad9327cde3e4fda2081",
+                "sha256:2a9b38bdb40a998cbc677db55b6225a6c4fadcf8819eb30695e1b8470942426b",
+                "sha256:30ddfe22de6ce4eb1260408f4480bbbce998f954dbf470228a21a9b2c45955e4",
+                "sha256:4057eb539a1d88eb84e9f6a36e0a999e0f261ed850ae5d5817e68968e7b89ed9",
+                "sha256:5028950f7af9b119d43d91b215d5044976e43b96a0d1458d193ef0dd3c587bf8",
+                "sha256:53c17f0dab19ddc22b254b087d1381b601b155acfa8feed514f0d6a413d0ab3a",
+                "sha256:62a9578b48cfd292c64ea3d28681dc16b1aa7445b7a7709a2884510fc0822118",
+                "sha256:9ac13b11d9ad3001de9d637974ec5402a67cefdf9fffc3929ab44c2fcbb850a1",
+                "sha256:9e9db5ccb810742d621f93272e3cc23b5f277d8d00c4a79668835d26ccbe48dd",
+                "sha256:a11bd0889e88d3342e7bc514554bb4461bf6cc30ec115821c2425cfaac0b1b6a",
+                "sha256:a8b44a245b60512403a6a03a5b5212da274d33862225c5eed3bcf12037eb19bb",
+                "sha256:aa17b13cd3f29fc57d06bf34c31f21d043735cc9a681203d634549b0e41047d1",
+                "sha256:b279fa55ea175ef953208a6d8bfbcdcffac1c39b38cdb8c2bfafe9222add70bb",
+                "sha256:c78470656e33d32ddc54e8482b1b0fc6de58f1195586731e5ff1405d74421499",
+                "sha256:d0f9967f84da42d28e3d9d9354cc1575f96ed69e6e40a7d4b780a7a0418d9409",
+                "sha256:d586e69ab5cbf521a1910b733412a5735936f6a610d805b89d35b6647e2a66aa",
+                "sha256:f54facf286103006171a00ce20388d88ed1d6732db3b49c11feb9bf3d46f90e9"
             ],
             "index": "pypi",
-            "version": "==0.0.264"
+            "version": "==0.0.265"
         },
         "six": {
             "hashes": [
                 "sha256:1e61c37477a1626458e36f7b1d82aa5c9b094fa4802892072e49de9c60c4c926",
                 "sha256:8abb2f1d86890a2dfb989f9a77cfcfd3e47c2a354b01111771326f8aa26e0254"
             ],
             "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
             "version": "==1.16.0"
         },
+        "smmap": {
+            "hashes": [
+                "sha256:2aba19d6a040e78d8b09de5c57e96207b09ed71d8e55ce0959eeee6c8e190d94",
+                "sha256:c840e62059cd3be204b0c9c9f74be2c09d5648eddd4580d9314c3ecde0b30936"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==5.0.0"
+        },
+        "snowballstemmer": {
+            "hashes": [
+                "sha256:09b16deb8547d3412ad7b590689584cd0fe25ec8db3be37788be3810cbf19cb1",
+                "sha256:c8e1716e83cc398ae16824e5572ae04e0d9fc2c6b985fb0f900f5f0c96ecba1a"
+            ],
+            "version": "==2.2.0"
+        },
         "tomli": {
             "hashes": [
                 "sha256:939de3e7a6161af0c887ef91b7d41a53e7c5a1ca976325f429cb46ea9bc30ecc",
                 "sha256:de526c12914f0c550d15924c62d72abc48d6fe7364aa87328337a31007fe8a4f"
             ],
             "markers": "python_version < '3.11'",
             "version": "==2.0.1"
         },
+        "tomlkit": {
+            "hashes": [
+                "sha256:8c726c4c202bdb148667835f68d68780b9a003a9ec34167b6c673b38eff2a171",
+                "sha256:9330fc7faa1db67b541b28e62018c17d20be733177d290a13b24c62d1614e0c3"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.11.8"
+        },
+        "typing-extensions": {
+            "hashes": [
+                "sha256:5cb5f4a79139d699607b3ef622a1dedafa84e115ab0024e0d9c044a9479ca7cb",
+                "sha256:fb33085c39dd998ac16d1431ebc293a8b3eedd00fd4a32de0ff79002c19511b4"
+            ],
+            "markers": "python_version < '3.11'",
+            "version": "==4.5.0"
+        },
         "urllib3": {
             "hashes": [
-                "sha256:8a388717b9476f934a21484e8c8e61875ab60644d29b9b39e11e4b9dc1c6b305",
-                "sha256:aa751d169e23c7479ce47a0cb0da579e3ede798f994f5816a74e4f4500dcea42"
+                "sha256:61717a1095d7e155cdb737ac7bb2f4324a858a1e2e6466f6d03ff630ca68d3cc",
+                "sha256:d055c2f9d38dc53c808f6fdc8eab7360b6fdbbde02340ed25cfbcd817c62469e"
             ],
-            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'",
-            "version": "==1.26.15"
+            "markers": "python_version >= '3.7'",
+            "version": "==2.0.2"
+        },
+        "watchdog": {
+            "hashes": [
+                "sha256:0e06ab8858a76e1219e68c7573dfeba9dd1c0219476c5a44d5333b01d7e1743a",
+                "sha256:13bbbb462ee42ec3c5723e1205be8ced776f05b100e4737518c67c8325cf6100",
+                "sha256:233b5817932685d39a7896b1090353fc8efc1ef99c9c054e46c8002561252fb8",
+                "sha256:25f70b4aa53bd743729c7475d7ec41093a580528b100e9a8c5b5efe8899592fc",
+                "sha256:2b57a1e730af3156d13b7fdddfc23dea6487fceca29fc75c5a868beed29177ae",
+                "sha256:336adfc6f5cc4e037d52db31194f7581ff744b67382eb6021c868322e32eef41",
+                "sha256:3aa7f6a12e831ddfe78cdd4f8996af9cf334fd6346531b16cec61c3b3c0d8da0",
+                "sha256:3ed7c71a9dccfe838c2f0b6314ed0d9b22e77d268c67e015450a29036a81f60f",
+                "sha256:4c9956d27be0bb08fc5f30d9d0179a855436e655f046d288e2bcc11adfae893c",
+                "sha256:4d98a320595da7a7c5a18fc48cb633c2e73cda78f93cac2ef42d42bf609a33f9",
+                "sha256:4f94069eb16657d2c6faada4624c39464f65c05606af50bb7902e036e3219be3",
+                "sha256:5113334cf8cf0ac8cd45e1f8309a603291b614191c9add34d33075727a967709",
+                "sha256:51f90f73b4697bac9c9a78394c3acbbd331ccd3655c11be1a15ae6fe289a8c83",
+                "sha256:5d9f3a10e02d7371cd929b5d8f11e87d4bad890212ed3901f9b4d68767bee759",
+                "sha256:7ade88d0d778b1b222adebcc0927428f883db07017618a5e684fd03b83342bd9",
+                "sha256:7c5f84b5194c24dd573fa6472685b2a27cc5a17fe5f7b6fd40345378ca6812e3",
+                "sha256:7e447d172af52ad204d19982739aa2346245cc5ba6f579d16dac4bfec226d2e7",
+                "sha256:8ae9cda41fa114e28faf86cb137d751a17ffd0316d1c34ccf2235e8a84365c7f",
+                "sha256:8f3ceecd20d71067c7fd4c9e832d4e22584318983cabc013dbf3f70ea95de346",
+                "sha256:9fac43a7466eb73e64a9940ac9ed6369baa39b3bf221ae23493a9ec4d0022674",
+                "sha256:a70a8dcde91be523c35b2bf96196edc5730edb347e374c7de7cd20c43ed95397",
+                "sha256:adfdeab2da79ea2f76f87eb42a3ab1966a5313e5a69a0213a3cc06ef692b0e96",
+                "sha256:ba07e92756c97e3aca0912b5cbc4e5ad802f4557212788e72a72a47ff376950d",
+                "sha256:c07253088265c363d1ddf4b3cdb808d59a0468ecd017770ed716991620b8f77a",
+                "sha256:c9d8c8ec7efb887333cf71e328e39cffbf771d8f8f95d308ea4125bf5f90ba64",
+                "sha256:d00e6be486affb5781468457b21a6cbe848c33ef43f9ea4a73b4882e5f188a44",
+                "sha256:d429c2430c93b7903914e4db9a966c7f2b068dd2ebdd2fa9b9ce094c7d459f33"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==3.0.0"
+        },
+        "wrapt": {
+            "hashes": [
+                "sha256:02fce1852f755f44f95af51f69d22e45080102e9d00258053b79367d07af39c0",
+                "sha256:077ff0d1f9d9e4ce6476c1a924a3332452c1406e59d90a2cf24aeb29eeac9420",
+                "sha256:078e2a1a86544e644a68422f881c48b84fef6d18f8c7a957ffd3f2e0a74a0d4a",
+                "sha256:0970ddb69bba00670e58955f8019bec4a42d1785db3faa043c33d81de2bf843c",
+                "sha256:1286eb30261894e4c70d124d44b7fd07825340869945c79d05bda53a40caa079",
+                "sha256:21f6d9a0d5b3a207cdf7acf8e58d7d13d463e639f0c7e01d82cdb671e6cb7923",
+                "sha256:230ae493696a371f1dbffaad3dafbb742a4d27a0afd2b1aecebe52b740167e7f",
+                "sha256:26458da5653aa5b3d8dc8b24192f574a58984c749401f98fff994d41d3f08da1",
+                "sha256:2cf56d0e237280baed46f0b5316661da892565ff58309d4d2ed7dba763d984b8",
+                "sha256:2e51de54d4fb8fb50d6ee8327f9828306a959ae394d3e01a1ba8b2f937747d86",
+                "sha256:2fbfbca668dd15b744418265a9607baa970c347eefd0db6a518aaf0cfbd153c0",
+                "sha256:38adf7198f8f154502883242f9fe7333ab05a5b02de7d83aa2d88ea621f13364",
+                "sha256:3a8564f283394634a7a7054b7983e47dbf39c07712d7b177b37e03f2467a024e",
+                "sha256:3abbe948c3cbde2689370a262a8d04e32ec2dd4f27103669a45c6929bcdbfe7c",
+                "sha256:3bbe623731d03b186b3d6b0d6f51865bf598587c38d6f7b0be2e27414f7f214e",
+                "sha256:40737a081d7497efea35ab9304b829b857f21558acfc7b3272f908d33b0d9d4c",
+                "sha256:41d07d029dd4157ae27beab04d22b8e261eddfc6ecd64ff7000b10dc8b3a5727",
+                "sha256:46ed616d5fb42f98630ed70c3529541408166c22cdfd4540b88d5f21006b0eff",
+                "sha256:493d389a2b63c88ad56cdc35d0fa5752daac56ca755805b1b0c530f785767d5e",
+                "sha256:4ff0d20f2e670800d3ed2b220d40984162089a6e2c9646fdb09b85e6f9a8fc29",
+                "sha256:54accd4b8bc202966bafafd16e69da9d5640ff92389d33d28555c5fd4f25ccb7",
+                "sha256:56374914b132c702aa9aa9959c550004b8847148f95e1b824772d453ac204a72",
+                "sha256:578383d740457fa790fdf85e6d346fda1416a40549fe8db08e5e9bd281c6a475",
+                "sha256:58d7a75d731e8c63614222bcb21dd992b4ab01a399f1f09dd82af17bbfc2368a",
+                "sha256:5c5aa28df055697d7c37d2099a7bc09f559d5053c3349b1ad0c39000e611d317",
+                "sha256:5fc8e02f5984a55d2c653f5fea93531e9836abbd84342c1d1e17abc4a15084c2",
+                "sha256:63424c681923b9f3bfbc5e3205aafe790904053d42ddcc08542181a30a7a51bd",
+                "sha256:64b1df0f83706b4ef4cfb4fb0e4c2669100fd7ecacfb59e091fad300d4e04640",
+                "sha256:74934ebd71950e3db69960a7da29204f89624dde411afbfb3b4858c1409b1e98",
+                "sha256:75669d77bb2c071333417617a235324a1618dba66f82a750362eccbe5b61d248",
+                "sha256:75760a47c06b5974aa5e01949bf7e66d2af4d08cb8c1d6516af5e39595397f5e",
+                "sha256:76407ab327158c510f44ded207e2f76b657303e17cb7a572ffe2f5a8a48aa04d",
+                "sha256:76e9c727a874b4856d11a32fb0b389afc61ce8aaf281ada613713ddeadd1cfec",
+                "sha256:77d4c1b881076c3ba173484dfa53d3582c1c8ff1f914c6461ab70c8428b796c1",
+                "sha256:780c82a41dc493b62fc5884fb1d3a3b81106642c5c5c78d6a0d4cbe96d62ba7e",
+                "sha256:7dc0713bf81287a00516ef43137273b23ee414fe41a3c14be10dd95ed98a2df9",
+                "sha256:7eebcdbe3677e58dd4c0e03b4f2cfa346ed4049687d839adad68cc38bb559c92",
+                "sha256:896689fddba4f23ef7c718279e42f8834041a21342d95e56922e1c10c0cc7afb",
+                "sha256:96177eb5645b1c6985f5c11d03fc2dbda9ad24ec0f3a46dcce91445747e15094",
+                "sha256:96e25c8603a155559231c19c0349245eeb4ac0096fe3c1d0be5c47e075bd4f46",
+                "sha256:9d37ac69edc5614b90516807de32d08cb8e7b12260a285ee330955604ed9dd29",
+                "sha256:9ed6aa0726b9b60911f4aed8ec5b8dd7bf3491476015819f56473ffaef8959bd",
+                "sha256:a487f72a25904e2b4bbc0817ce7a8de94363bd7e79890510174da9d901c38705",
+                "sha256:a4cbb9ff5795cd66f0066bdf5947f170f5d63a9274f99bdbca02fd973adcf2a8",
+                "sha256:a74d56552ddbde46c246b5b89199cb3fd182f9c346c784e1a93e4dc3f5ec9975",
+                "sha256:a89ce3fd220ff144bd9d54da333ec0de0399b52c9ac3d2ce34b569cf1a5748fb",
+                "sha256:abd52a09d03adf9c763d706df707c343293d5d106aea53483e0ec8d9e310ad5e",
+                "sha256:abd8f36c99512755b8456047b7be10372fca271bf1467a1caa88db991e7c421b",
+                "sha256:af5bd9ccb188f6a5fdda9f1f09d9f4c86cc8a539bd48a0bfdc97723970348418",
+                "sha256:b02f21c1e2074943312d03d243ac4388319f2456576b2c6023041c4d57cd7019",
+                "sha256:b06fa97478a5f478fb05e1980980a7cdf2712015493b44d0c87606c1513ed5b1",
+                "sha256:b0724f05c396b0a4c36a3226c31648385deb6a65d8992644c12a4963c70326ba",
+                "sha256:b130fe77361d6771ecf5a219d8e0817d61b236b7d8b37cc045172e574ed219e6",
+                "sha256:b56d5519e470d3f2fe4aa7585f0632b060d532d0696c5bdfb5e8319e1d0f69a2",
+                "sha256:b67b819628e3b748fd3c2192c15fb951f549d0f47c0449af0764d7647302fda3",
+                "sha256:ba1711cda2d30634a7e452fc79eabcadaffedf241ff206db2ee93dd2c89a60e7",
+                "sha256:bbeccb1aa40ab88cd29e6c7d8585582c99548f55f9b2581dfc5ba68c59a85752",
+                "sha256:bd84395aab8e4d36263cd1b9308cd504f6cf713b7d6d3ce25ea55670baec5416",
+                "sha256:c99f4309f5145b93eca6e35ac1a988f0dc0a7ccf9ccdcd78d3c0adf57224e62f",
+                "sha256:ca1cccf838cd28d5a0883b342474c630ac48cac5df0ee6eacc9c7290f76b11c1",
+                "sha256:cd525e0e52a5ff16653a3fc9e3dd827981917d34996600bbc34c05d048ca35cc",
+                "sha256:cdb4f085756c96a3af04e6eca7f08b1345e94b53af8921b25c72f096e704e145",
+                "sha256:ce42618f67741d4697684e501ef02f29e758a123aa2d669e2d964ff734ee00ee",
+                "sha256:d06730c6aed78cee4126234cf2d071e01b44b915e725a6cb439a879ec9754a3a",
+                "sha256:d5fe3e099cf07d0fb5a1e23d399e5d4d1ca3e6dfcbe5c8570ccff3e9208274f7",
+                "sha256:d6bcbfc99f55655c3d93feb7ef3800bd5bbe963a755687cbf1f490a71fb7794b",
+                "sha256:d787272ed958a05b2c86311d3a4135d3c2aeea4fc655705f074130aa57d71653",
+                "sha256:e169e957c33576f47e21864cf3fc9ff47c223a4ebca8960079b8bd36cb014fd0",
+                "sha256:e20076a211cd6f9b44a6be58f7eeafa7ab5720eb796975d0c03f05b47d89eb90",
+                "sha256:e826aadda3cae59295b95343db8f3d965fb31059da7de01ee8d1c40a60398b29",
+                "sha256:eef4d64c650f33347c1f9266fa5ae001440b232ad9b98f1f43dfe7a79435c0a6",
+                "sha256:f2e69b3ed24544b0d3dbe2c5c0ba5153ce50dcebb576fdc4696d52aa22db6034",
+                "sha256:f87ec75864c37c4c6cb908d282e1969e79763e0d9becdfe9fe5473b7bb1e5f09",
+                "sha256:fbec11614dba0424ca72f4e8ba3c420dba07b4a7c206c8c8e4e73f2e98f4c559",
+                "sha256:fd69666217b62fa5d7c6aa88e507493a34dec4fa20c5bd925e4bc12fce586639"
+            ],
+            "markers": "python_version < '3.11'",
+            "version": "==1.15.0"
+        }
+    },
+    "docs": {
+        "babel": {
+            "hashes": [
+                "sha256:b4246fb7677d3b98f501a39d43396d3cafdc8eadb045f4a31be01863f655c610",
+                "sha256:cc2d99999cd01d44420ae725a21c9e3711b3aadc7976d6147f622d8581963455"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.12.1"
+        },
+        "certifi": {
+            "hashes": [
+                "sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7",
+                "sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==2023.5.7"
+        },
+        "charset-normalizer": {
+            "hashes": [
+                "sha256:04afa6387e2b282cf78ff3dbce20f0cc071c12dc8f685bd40960cc68644cfea6",
+                "sha256:04eefcee095f58eaabe6dc3cc2262f3bcd776d2c67005880894f447b3f2cb9c1",
+                "sha256:0be65ccf618c1e7ac9b849c315cc2e8a8751d9cfdaa43027d4f6624bd587ab7e",
+                "sha256:0c95f12b74681e9ae127728f7e5409cbbef9cd914d5896ef238cc779b8152373",
+                "sha256:0ca564606d2caafb0abe6d1b5311c2649e8071eb241b2d64e75a0d0065107e62",
+                "sha256:10c93628d7497c81686e8e5e557aafa78f230cd9e77dd0c40032ef90c18f2230",
+                "sha256:11d117e6c63e8f495412d37e7dc2e2fff09c34b2d09dbe2bee3c6229577818be",
+                "sha256:11d3bcb7be35e7b1bba2c23beedac81ee893ac9871d0ba79effc7fc01167db6c",
+                "sha256:12a2b561af122e3d94cdb97fe6fb2bb2b82cef0cdca131646fdb940a1eda04f0",
+                "sha256:12d1a39aa6b8c6f6248bb54550efcc1c38ce0d8096a146638fd4738e42284448",
+                "sha256:1435ae15108b1cb6fffbcea2af3d468683b7afed0169ad718451f8db5d1aff6f",
+                "sha256:1c60b9c202d00052183c9be85e5eaf18a4ada0a47d188a83c8f5c5b23252f649",
+                "sha256:1e8fcdd8f672a1c4fc8d0bd3a2b576b152d2a349782d1eb0f6b8e52e9954731d",
+                "sha256:20064ead0717cf9a73a6d1e779b23d149b53daf971169289ed2ed43a71e8d3b0",
+                "sha256:21fa558996782fc226b529fdd2ed7866c2c6ec91cee82735c98a197fae39f706",
+                "sha256:22908891a380d50738e1f978667536f6c6b526a2064156203d418f4856d6e86a",
+                "sha256:3160a0fd9754aab7d47f95a6b63ab355388d890163eb03b2d2b87ab0a30cfa59",
+                "sha256:322102cdf1ab682ecc7d9b1c5eed4ec59657a65e1c146a0da342b78f4112db23",
+                "sha256:34e0a2f9c370eb95597aae63bf85eb5e96826d81e3dcf88b8886012906f509b5",
+                "sha256:3573d376454d956553c356df45bb824262c397c6e26ce43e8203c4c540ee0acb",
+                "sha256:3747443b6a904001473370d7810aa19c3a180ccd52a7157aacc264a5ac79265e",
+                "sha256:38e812a197bf8e71a59fe55b757a84c1f946d0ac114acafaafaf21667a7e169e",
+                "sha256:3a06f32c9634a8705f4ca9946d667609f52cf130d5548881401f1eb2c39b1e2c",
+                "sha256:3a5fc78f9e3f501a1614a98f7c54d3969f3ad9bba8ba3d9b438c3bc5d047dd28",
+                "sha256:3d9098b479e78c85080c98e1e35ff40b4a31d8953102bb0fd7d1b6f8a2111a3d",
+                "sha256:3dc5b6a8ecfdc5748a7e429782598e4f17ef378e3e272eeb1340ea57c9109f41",
+                "sha256:4155b51ae05ed47199dc5b2a4e62abccb274cee6b01da5b895099b61b1982974",
+                "sha256:49919f8400b5e49e961f320c735388ee686a62327e773fa5b3ce6721f7e785ce",
+                "sha256:53d0a3fa5f8af98a1e261de6a3943ca631c526635eb5817a87a59d9a57ebf48f",
+                "sha256:5f008525e02908b20e04707a4f704cd286d94718f48bb33edddc7d7b584dddc1",
+                "sha256:628c985afb2c7d27a4800bfb609e03985aaecb42f955049957814e0491d4006d",
+                "sha256:65ed923f84a6844de5fd29726b888e58c62820e0769b76565480e1fdc3d062f8",
+                "sha256:6734e606355834f13445b6adc38b53c0fd45f1a56a9ba06c2058f86893ae8017",
+                "sha256:6baf0baf0d5d265fa7944feb9f7451cc316bfe30e8df1a61b1bb08577c554f31",
+                "sha256:6f4f4668e1831850ebcc2fd0b1cd11721947b6dc7c00bf1c6bd3c929ae14f2c7",
+                "sha256:6f5c2e7bc8a4bf7c426599765b1bd33217ec84023033672c1e9a8b35eaeaaaf8",
+                "sha256:6f6c7a8a57e9405cad7485f4c9d3172ae486cfef1344b5ddd8e5239582d7355e",
+                "sha256:7381c66e0561c5757ffe616af869b916c8b4e42b367ab29fedc98481d1e74e14",
+                "sha256:73dc03a6a7e30b7edc5b01b601e53e7fc924b04e1835e8e407c12c037e81adbd",
+                "sha256:74db0052d985cf37fa111828d0dd230776ac99c740e1a758ad99094be4f1803d",
+                "sha256:75f2568b4189dda1c567339b48cba4ac7384accb9c2a7ed655cd86b04055c795",
+                "sha256:78cacd03e79d009d95635e7d6ff12c21eb89b894c354bd2b2ed0b4763373693b",
+                "sha256:80d1543d58bd3d6c271b66abf454d437a438dff01c3e62fdbcd68f2a11310d4b",
+                "sha256:830d2948a5ec37c386d3170c483063798d7879037492540f10a475e3fd6f244b",
+                "sha256:891cf9b48776b5c61c700b55a598621fdb7b1e301a550365571e9624f270c203",
+                "sha256:8f25e17ab3039b05f762b0a55ae0b3632b2e073d9c8fc88e89aca31a6198e88f",
+                "sha256:9a3267620866c9d17b959a84dd0bd2d45719b817245e49371ead79ed4f710d19",
+                "sha256:a04f86f41a8916fe45ac5024ec477f41f886b3c435da2d4e3d2709b22ab02af1",
+                "sha256:aaf53a6cebad0eae578f062c7d462155eada9c172bd8c4d250b8c1d8eb7f916a",
+                "sha256:abc1185d79f47c0a7aaf7e2412a0eb2c03b724581139193d2d82b3ad8cbb00ac",
+                "sha256:ac0aa6cd53ab9a31d397f8303f92c42f534693528fafbdb997c82bae6e477ad9",
+                "sha256:ac3775e3311661d4adace3697a52ac0bab17edd166087d493b52d4f4f553f9f0",
+                "sha256:b06f0d3bf045158d2fb8837c5785fe9ff9b8c93358be64461a1089f5da983137",
+                "sha256:b116502087ce8a6b7a5f1814568ccbd0e9f6cfd99948aa59b0e241dc57cf739f",
+                "sha256:b82fab78e0b1329e183a65260581de4375f619167478dddab510c6c6fb04d9b6",
+                "sha256:bd7163182133c0c7701b25e604cf1611c0d87712e56e88e7ee5d72deab3e76b5",
+                "sha256:c36bcbc0d5174a80d6cccf43a0ecaca44e81d25be4b7f90f0ed7bcfbb5a00909",
+                "sha256:c3af8e0f07399d3176b179f2e2634c3ce9c1301379a6b8c9c9aeecd481da494f",
+                "sha256:c84132a54c750fda57729d1e2599bb598f5fa0344085dbde5003ba429a4798c0",
+                "sha256:cb7b2ab0188829593b9de646545175547a70d9a6e2b63bf2cd87a0a391599324",
+                "sha256:cca4def576f47a09a943666b8f829606bcb17e2bc2d5911a46c8f8da45f56755",
+                "sha256:cf6511efa4801b9b38dc5546d7547d5b5c6ef4b081c60b23e4d941d0eba9cbeb",
+                "sha256:d16fd5252f883eb074ca55cb622bc0bee49b979ae4e8639fff6ca3ff44f9f854",
+                "sha256:d2686f91611f9e17f4548dbf050e75b079bbc2a82be565832bc8ea9047b61c8c",
+                "sha256:d7fc3fca01da18fbabe4625d64bb612b533533ed10045a2ac3dd194bfa656b60",
+                "sha256:dd5653e67b149503c68c4018bf07e42eeed6b4e956b24c00ccdf93ac79cdff84",
+                "sha256:de5695a6f1d8340b12a5d6d4484290ee74d61e467c39ff03b39e30df62cf83a0",
+                "sha256:e0ac8959c929593fee38da1c2b64ee9778733cdf03c482c9ff1d508b6b593b2b",
+                "sha256:e1b25e3ad6c909f398df8921780d6a3d120d8c09466720226fc621605b6f92b1",
+                "sha256:e633940f28c1e913615fd624fcdd72fdba807bf53ea6925d6a588e84e1151531",
+                "sha256:e89df2958e5159b811af9ff0f92614dabf4ff617c03a4c1c6ff53bf1c399e0e1",
+                "sha256:ea9f9c6034ea2d93d9147818f17c2a0860d41b71c38b9ce4d55f21b6f9165a11",
+                "sha256:f645caaf0008bacf349875a974220f1f1da349c5dbe7c4ec93048cdc785a3326",
+                "sha256:f8303414c7b03f794347ad062c0516cee0e15f7a612abd0ce1e25caf6ceb47df",
+                "sha256:fca62a8301b605b954ad2e9c3666f9d97f63872aa4efcae5492baca2056b74ab"
+            ],
+            "markers": "python_full_version >= '3.7.0'",
+            "version": "==3.1.0"
+        },
+        "click": {
+            "hashes": [
+                "sha256:7682dc8afb30297001674575ea00d1814d808d6a36af415a82bd481d37ba7b8e",
+                "sha256:bb4d8133cb15a609f44e8213d9b391b0809795062913b383c62be0ee95b1db48"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==8.1.3"
+        },
+        "colorama": {
+            "hashes": [
+                "sha256:08695f5cb7ed6e0531a20572697297273c47b8cae5a63ffc6d6ed5c201be6e44",
+                "sha256:4f1d9991f5acc0ca119f9d443620b77f9d6b33703e51011c16baf57afb285fc6"
+            ],
+            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6'",
+            "version": "==0.4.6"
+        },
+        "ghp-import": {
+            "hashes": [
+                "sha256:8337dd7b50877f163d4c0289bc1f1c7f127550241988d568c1db512c4324a619",
+                "sha256:9c535c4c61193c2df8871222567d7fd7e5014d835f97dc7b7439069e2413d343"
+            ],
+            "version": "==2.1.0"
+        },
+        "gitdb": {
+            "hashes": [
+                "sha256:6eb990b69df4e15bad899ea868dc46572c3f75339735663b81de79b06f17eb9a",
+                "sha256:c286cf298426064079ed96a9e4a9d39e7f3e9bf15ba60701e95f5492f28415c7"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==4.0.10"
+        },
+        "gitpython": {
+            "hashes": [
+                "sha256:8ce3bcf69adfdf7c7d503e78fd3b1c492af782d58893b650adb2ac8912ddd573",
+                "sha256:f04893614f6aa713a60cbbe1e6a97403ef633103cdd0ef5eb6efe0deb98dbe8d"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==3.1.31"
+        },
+        "griffe": {
+            "hashes": [
+                "sha256:15b48fc3cebfc1c1a1a2f6e8177f6644a4a54517322e08e224fdf671454b34d7",
+                "sha256:96fbc7a264bdb32b4da227bed6a16f2509e028a12d7471dbb48c2785bb01817f"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.27.5"
+        },
+        "idna": {
+            "hashes": [
+                "sha256:814f528e8dead7d329833b91c5faa87d60bf71824cd12a7530b5526063d02cb4",
+                "sha256:90b77e79eaa3eba6de819a0c442c0b4ceefc341a7a2ab77d7562bf49f425c5c2"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==3.4"
+        },
+        "jinja2": {
+            "hashes": [
+                "sha256:31351a702a408a9e7595a8fc6150fc3f43bb6bf7e319770cbc0db9df9437e852",
+                "sha256:6088930bfe239f0e6710546ab9c19c9ef35e29792895fed6e6e31a023a182a61"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==3.1.2"
+        },
+        "markdown": {
+            "hashes": [
+                "sha256:cbb516f16218e643d8e0a95b309f77eb118cb138d39a4f27851e6a63581db874",
+                "sha256:f5da449a6e1c989a4cea2631aa8ee67caa5a2ef855d551c88f9e309f4634c621"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==3.3.7"
+        },
+        "markupsafe": {
+            "hashes": [
+                "sha256:0576fe974b40a400449768941d5d0858cc624e3249dfd1e0c33674e5c7ca7aed",
+                "sha256:085fd3201e7b12809f9e6e9bc1e5c96a368c8523fad5afb02afe3c051ae4afcc",
+                "sha256:090376d812fb6ac5f171e5938e82e7f2d7adc2b629101cec0db8b267815c85e2",
+                "sha256:0b462104ba25f1ac006fdab8b6a01ebbfbce9ed37fd37fd4acd70c67c973e460",
+                "sha256:137678c63c977754abe9086a3ec011e8fd985ab90631145dfb9294ad09c102a7",
+                "sha256:1bea30e9bf331f3fef67e0a3877b2288593c98a21ccb2cf29b74c581a4eb3af0",
+                "sha256:22152d00bf4a9c7c83960521fc558f55a1adbc0631fbb00a9471e097b19d72e1",
+                "sha256:22731d79ed2eb25059ae3df1dfc9cb1546691cc41f4e3130fe6bfbc3ecbbecfa",
+                "sha256:2298c859cfc5463f1b64bd55cb3e602528db6fa0f3cfd568d3605c50678f8f03",
+                "sha256:28057e985dace2f478e042eaa15606c7efccb700797660629da387eb289b9323",
+                "sha256:2e7821bffe00aa6bd07a23913b7f4e01328c3d5cc0b40b36c0bd81d362faeb65",
+                "sha256:2ec4f2d48ae59bbb9d1f9d7efb9236ab81429a764dedca114f5fdabbc3788013",
+                "sha256:340bea174e9761308703ae988e982005aedf427de816d1afe98147668cc03036",
+                "sha256:40627dcf047dadb22cd25ea7ecfe9cbf3bbbad0482ee5920b582f3809c97654f",
+                "sha256:40dfd3fefbef579ee058f139733ac336312663c6706d1163b82b3003fb1925c4",
+                "sha256:4cf06cdc1dda95223e9d2d3c58d3b178aa5dacb35ee7e3bbac10e4e1faacb419",
+                "sha256:50c42830a633fa0cf9e7d27664637532791bfc31c731a87b202d2d8ac40c3ea2",
+                "sha256:55f44b440d491028addb3b88f72207d71eeebfb7b5dbf0643f7c023ae1fba619",
+                "sha256:608e7073dfa9e38a85d38474c082d4281f4ce276ac0010224eaba11e929dd53a",
+                "sha256:63ba06c9941e46fa389d389644e2d8225e0e3e5ebcc4ff1ea8506dce646f8c8a",
+                "sha256:65608c35bfb8a76763f37036547f7adfd09270fbdbf96608be2bead319728fcd",
+                "sha256:665a36ae6f8f20a4676b53224e33d456a6f5a72657d9c83c2aa00765072f31f7",
+                "sha256:6d6607f98fcf17e534162f0709aaad3ab7a96032723d8ac8750ffe17ae5a0666",
+                "sha256:7313ce6a199651c4ed9d7e4cfb4aa56fe923b1adf9af3b420ee14e6d9a73df65",
+                "sha256:7668b52e102d0ed87cb082380a7e2e1e78737ddecdde129acadb0eccc5423859",
+                "sha256:7df70907e00c970c60b9ef2938d894a9381f38e6b9db73c5be35e59d92e06625",
+                "sha256:7e007132af78ea9df29495dbf7b5824cb71648d7133cf7848a2a5dd00d36f9ff",
+                "sha256:835fb5e38fd89328e9c81067fd642b3593c33e1e17e2fdbf77f5676abb14a156",
+                "sha256:8bca7e26c1dd751236cfb0c6c72d4ad61d986e9a41bbf76cb445f69488b2a2bd",
+                "sha256:8db032bf0ce9022a8e41a22598eefc802314e81b879ae093f36ce9ddf39ab1ba",
+                "sha256:99625a92da8229df6d44335e6fcc558a5037dd0a760e11d84be2260e6f37002f",
+                "sha256:9cad97ab29dfc3f0249b483412c85c8ef4766d96cdf9dcf5a1e3caa3f3661cf1",
+                "sha256:a4abaec6ca3ad8660690236d11bfe28dfd707778e2442b45addd2f086d6ef094",
+                "sha256:a6e40afa7f45939ca356f348c8e23048e02cb109ced1eb8420961b2f40fb373a",
+                "sha256:a6f2fcca746e8d5910e18782f976489939d54a91f9411c32051b4aab2bd7c513",
+                "sha256:a806db027852538d2ad7555b203300173dd1b77ba116de92da9afbc3a3be3eed",
+                "sha256:abcabc8c2b26036d62d4c746381a6f7cf60aafcc653198ad678306986b09450d",
+                "sha256:b8526c6d437855442cdd3d87eede9c425c4445ea011ca38d937db299382e6fa3",
+                "sha256:bb06feb762bade6bf3c8b844462274db0c76acc95c52abe8dbed28ae3d44a147",
+                "sha256:c0a33bc9f02c2b17c3ea382f91b4db0e6cde90b63b296422a939886a7a80de1c",
+                "sha256:c4a549890a45f57f1ebf99c067a4ad0cb423a05544accaf2b065246827ed9603",
+                "sha256:ca244fa73f50a800cf8c3ebf7fd93149ec37f5cb9596aa8873ae2c1d23498601",
+                "sha256:cf877ab4ed6e302ec1d04952ca358b381a882fbd9d1b07cccbfd61783561f98a",
+                "sha256:d9d971ec1e79906046aa3ca266de79eac42f1dbf3612a05dc9368125952bd1a1",
+                "sha256:da25303d91526aac3672ee6d49a2f3db2d9502a4a60b55519feb1a4c7714e07d",
+                "sha256:e55e40ff0cc8cc5c07996915ad367fa47da6b3fc091fdadca7f5403239c5fec3",
+                "sha256:f03a532d7dee1bed20bc4884194a16160a2de9ffc6354b3878ec9682bb623c54",
+                "sha256:f1cd098434e83e656abf198f103a8207a8187c0fc110306691a2e94a78d0abb2",
+                "sha256:f2bfb563d0211ce16b63c7cb9395d2c682a23187f54c3d79bfec33e6705473c6",
+                "sha256:f8ffb705ffcf5ddd0e80b65ddf7bed7ee4f5a441ea7d3419e861a12eaf41af58"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.1.2"
+        },
+        "mergedeep": {
+            "hashes": [
+                "sha256:0096d52e9dad9939c3d975a774666af186eda617e6ca84df4c94dec30004f2a8",
+                "sha256:70775750742b25c0d8f36c55aed03d24c3384d17c951b3175d898bd778ef0307"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==1.3.4"
+        },
+        "mkdocs": {
+            "hashes": [
+                "sha256:5955093bbd4dd2e9403c5afaf57324ad8b04f16886512a3ee6ef828956481c57",
+                "sha256:6ee46d309bda331aac915cd24aab882c179a933bd9e77b80ce7d2eaaa3f689dd"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==1.4.3"
+        },
+        "mkdocs-autorefs": {
+            "hashes": [
+                "sha256:70748a7bd025f9ecd6d6feeba8ba63f8e891a1af55f48e366d6d6e78493aba84",
+                "sha256:a2248a9501b29dc0cc8ba4c09f4f47ff121945f6ce33d760f145d6f89d313f5b"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.4.1"
+        },
+        "mkdocs-gen-files": {
+            "hashes": [
+                "sha256:4c7cf256b5d67062a788f6b1d035e157fc1a9498c2399be9af5257d4ff4d19bc",
+                "sha256:7ac060096f3f40bd19039e7277dd3050be9a453c8ac578645844d4d91d7978ea"
+            ],
+            "index": "pypi",
+            "version": "==0.5.0"
+        },
+        "mkdocs-git-revision-date-localized-plugin": {
+            "hashes": [
+                "sha256:540b9c930d8d48630c090b72ac2c3900ac2ed0799b23738a33b88e31f5198fe7",
+                "sha256:7752edd7c4dcaa9383e9a5b6a4f729831a62d604b0c43b319331127720c6a2bf"
+            ],
+            "index": "pypi",
+            "version": "==1.2.0"
+        },
+        "mkdocs-literate-nav": {
+            "hashes": [
+                "sha256:81ccbea18163ae8e10bd0bd39237fe70c32a1f2dff6c170779f5d52dd98a0470",
+                "sha256:8c1b84714e5974da5e44e011ec0069275ae7647270c13a679662cf6ffce675a4"
+            ],
+            "index": "pypi",
+            "version": "==0.6.0"
+        },
+        "mkdocs-material": {
+            "hashes": [
+                "sha256:68c57d95d10104179c8c3ce9a88ee9d2322a5145b3d0f1f38ff686253fb5ec98",
+                "sha256:d4ebe9b5031ce63a265c19fb5eab4d27ea4edadb05de206372e831b2b7570fb5"
+            ],
+            "index": "pypi",
+            "version": "==9.1.12"
+        },
+        "mkdocs-material-extensions": {
+            "hashes": [
+                "sha256:9c003da71e2cc2493d910237448c672e00cefc800d3d6ae93d2fc69979e3bd93",
+                "sha256:e41d9f38e4798b6617ad98ca8f7f1157b1e4385ac1459ca1e4ea219b556df945"
+            ],
+            "index": "pypi",
+            "version": "==1.1.1"
+        },
+        "mkdocs-section-index": {
+            "hashes": [
+                "sha256:1f6359287b0a823d6297cf1cb6c0a49ed75851d0d1cea8b425b207a45ce10141",
+                "sha256:fa8b1ce0649326b1873c6460c1df2bb0c4825fd21e3dd416f13ec212d31edf12"
+            ],
+            "index": "pypi",
+            "version": "==0.3.5"
+        },
+        "mkdocstrings": {
+            "hashes": [
+                "sha256:304e56a2e90595708a38a13a278e538a67ad82052dd5c8b71f77a604a4f3d911",
+                "sha256:949ef8da92df9d692ca07be50616459a6b536083a25520fd54b00e8814ce019b"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.21.2"
+        },
+        "mkdocstrings-python": {
+            "hashes": [
+                "sha256:b89d849df990204f909d5452548b6936a185f912da06208a93909bebe25d6e67",
+                "sha256:c59d67009a7a85172f4da990d8523e95606b6a1ff93a22a2351ad3b5f8cafed1"
+            ],
+            "index": "pypi",
+            "version": "==1.0.0"
+        },
+        "packaging": {
+            "hashes": [
+                "sha256:994793af429502c4ea2ebf6bf664629d07c1a9fe974af92966e4b8d2df7edc61",
+                "sha256:a392980d2b6cffa644431898be54b0045151319d1e7ec34f0cfed48767dd334f"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==23.1"
+        },
+        "pygments": {
+            "hashes": [
+                "sha256:8ace4d3c1dd481894b2005f560ead0f9f19ee64fe983366be1a21e171d12775c",
+                "sha256:db2db3deb4b4179f399a09054b023b6a586b76499d36965813c71aa8ed7b5fd1"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.15.1"
+        },
+        "pymdown-extensions": {
+            "hashes": [
+                "sha256:a499191d8d869f30339de86fcf072a787e86c42b6f16f280f5c2cf174182b7f3",
+                "sha256:f7e86c1d3981f23d9dc43294488ecb54abadd05b0be4bf8f0e15efc90f7853ff"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==9.11"
+        },
+        "python-dateutil": {
+            "hashes": [
+                "sha256:0123cacc1627ae19ddf3c27a5de5bd67ee4586fbdd6440d9748f8abb483d3e86",
+                "sha256:961d03dc3453ebbc59dbdea9e4e11c5651520a876d0f4db161e8674aae935da9"
+            ],
+            "index": "pypi",
+            "version": "==2.8.2"
+        },
+        "pytz": {
+            "hashes": [
+                "sha256:1d8ce29db189191fb55338ee6d0387d82ab59f3d00eac103412d64e0ebd0c588",
+                "sha256:a151b3abb88eda1d4e34a9814df37de2a80e301e68ba0fd856fb9b46bfbbbffb"
+            ],
+            "version": "==2023.3"
+        },
+        "pyyaml": {
+            "hashes": [
+                "sha256:01b45c0191e6d66c470b6cf1b9531a771a83c1c4208272ead47a3ae4f2f603bf",
+                "sha256:0283c35a6a9fbf047493e3a0ce8d79ef5030852c51e9d911a27badfde0605293",
+                "sha256:055d937d65826939cb044fc8c9b08889e8c743fdc6a32b33e2390f66013e449b",
+                "sha256:07751360502caac1c067a8132d150cf3d61339af5691fe9e87803040dbc5db57",
+                "sha256:0b4624f379dab24d3725ffde76559cff63d9ec94e1736b556dacdfebe5ab6d4b",
+                "sha256:0ce82d761c532fe4ec3f87fc45688bdd3a4c1dc5e0b4a19814b9009a29baefd4",
+                "sha256:1e4747bc279b4f613a09eb64bba2ba602d8a6664c6ce6396a4d0cd413a50ce07",
+                "sha256:213c60cd50106436cc818accf5baa1aba61c0189ff610f64f4a3e8c6726218ba",
+                "sha256:231710d57adfd809ef5d34183b8ed1eeae3f76459c18fb4a0b373ad56bedcdd9",
+                "sha256:277a0ef2981ca40581a47093e9e2d13b3f1fbbeffae064c1d21bfceba2030287",
+                "sha256:2cd5df3de48857ed0544b34e2d40e9fac445930039f3cfe4bcc592a1f836d513",
+                "sha256:40527857252b61eacd1d9af500c3337ba8deb8fc298940291486c465c8b46ec0",
+                "sha256:432557aa2c09802be39460360ddffd48156e30721f5e8d917f01d31694216782",
+                "sha256:473f9edb243cb1935ab5a084eb238d842fb8f404ed2193a915d1784b5a6b5fc0",
+                "sha256:48c346915c114f5fdb3ead70312bd042a953a8ce5c7106d5bfb1a5254e47da92",
+                "sha256:50602afada6d6cbfad699b0c7bb50d5ccffa7e46a3d738092afddc1f9758427f",
+                "sha256:68fb519c14306fec9720a2a5b45bc9f0c8d1b9c72adf45c37baedfcd949c35a2",
+                "sha256:77f396e6ef4c73fdc33a9157446466f1cff553d979bd00ecb64385760c6babdc",
+                "sha256:81957921f441d50af23654aa6c5e5eaf9b06aba7f0a19c18a538dc7ef291c5a1",
+                "sha256:819b3830a1543db06c4d4b865e70ded25be52a2e0631ccd2f6a47a2822f2fd7c",
+                "sha256:897b80890765f037df3403d22bab41627ca8811ae55e9a722fd0392850ec4d86",
+                "sha256:98c4d36e99714e55cfbaaee6dd5badbc9a1ec339ebfc3b1f52e293aee6bb71a4",
+                "sha256:9df7ed3b3d2e0ecfe09e14741b857df43adb5a3ddadc919a2d94fbdf78fea53c",
+                "sha256:9fa600030013c4de8165339db93d182b9431076eb98eb40ee068700c9c813e34",
+                "sha256:a80a78046a72361de73f8f395f1f1e49f956c6be882eed58505a15f3e430962b",
+                "sha256:afa17f5bc4d1b10afd4466fd3a44dc0e245382deca5b3c353d8b757f9e3ecb8d",
+                "sha256:b3d267842bf12586ba6c734f89d1f5b871df0273157918b0ccefa29deb05c21c",
+                "sha256:b5b9eccad747aabaaffbc6064800670f0c297e52c12754eb1d976c57e4f74dcb",
+                "sha256:bfaef573a63ba8923503d27530362590ff4f576c626d86a9fed95822a8255fd7",
+                "sha256:c5687b8d43cf58545ade1fe3e055f70eac7a5a1a0bf42824308d868289a95737",
+                "sha256:cba8c411ef271aa037d7357a2bc8f9ee8b58b9965831d9e51baf703280dc73d3",
+                "sha256:d15a181d1ecd0d4270dc32edb46f7cb7733c7c508857278d3d378d14d606db2d",
+                "sha256:d4b0ba9512519522b118090257be113b9468d804b19d63c71dbcf4a48fa32358",
+                "sha256:d4db7c7aef085872ef65a8fd7d6d09a14ae91f691dec3e87ee5ee0539d516f53",
+                "sha256:d4eccecf9adf6fbcc6861a38015c2a64f38b9d94838ac1810a9023a0609e1b78",
+                "sha256:d67d839ede4ed1b28a4e8909735fc992a923cdb84e618544973d7dfc71540803",
+                "sha256:daf496c58a8c52083df09b80c860005194014c3698698d1a57cbcfa182142a3a",
+                "sha256:dbad0e9d368bb989f4515da330b88a057617d16b6a8245084f1b05400f24609f",
+                "sha256:e61ceaab6f49fb8bdfaa0f92c4b57bcfbea54c09277b1b4f7ac376bfb7a7c174",
+                "sha256:f84fbc98b019fef2ee9a1cb3ce93e3187a6df0b2538a651bfb890254ba9f90b5"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==6.0"
+        },
+        "pyyaml-env-tag": {
+            "hashes": [
+                "sha256:70092675bda14fdec33b31ba77e7543de9ddc88f2e5b99160396572d11525bdb",
+                "sha256:af31106dec8a4d68c60207c1886031cbf839b68aa7abccdb19868200532c2069"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==0.1"
+        },
+        "regex": {
+            "hashes": [
+                "sha256:02f4541550459c08fdd6f97aa4e24c6f1932eec780d58a2faa2068253df7d6ff",
+                "sha256:0a69cf0c00c4d4a929c6c7717fd918414cab0d6132a49a6d8fc3ded1988ed2ea",
+                "sha256:0bbd5dcb19603ab8d2781fac60114fb89aee8494f4505ae7ad141a3314abb1f9",
+                "sha256:10250a093741ec7bf74bcd2039e697f519b028518f605ff2aa7ac1e9c9f97423",
+                "sha256:10374c84ee58c44575b667310d5bbfa89fb2e64e52349720a0182c0017512f6c",
+                "sha256:1189fbbb21e2c117fda5303653b61905aeeeea23de4a94d400b0487eb16d2d60",
+                "sha256:1307aa4daa1cbb23823d8238e1f61292fd07e4e5d8d38a6efff00b67a7cdb764",
+                "sha256:144b5b017646b5a9392a5554a1e5db0000ae637be4971c9747566775fc96e1b2",
+                "sha256:171c52e320fe29260da550d81c6b99f6f8402450dc7777ef5ced2e848f3b6f8f",
+                "sha256:18196c16a584619c7c1d843497c069955d7629ad4a3fdee240eb347f4a2c9dbe",
+                "sha256:18f05d14f14a812fe9723f13afafefe6b74ca042d99f8884e62dbd34dcccf3e2",
+                "sha256:1ecf3dcff71f0c0fe3e555201cbe749fa66aae8d18f80d2cc4de8e66df37390a",
+                "sha256:21e90a288e6ba4bf44c25c6a946cb9b0f00b73044d74308b5e0afd190338297c",
+                "sha256:23d86ad2121b3c4fc78c58f95e19173790e22ac05996df69b84e12da5816cb17",
+                "sha256:256f7f4c6ba145f62f7a441a003c94b8b1af78cee2cccacfc1e835f93bc09426",
+                "sha256:290fd35219486dfbc00b0de72f455ecdd63e59b528991a6aec9fdfc0ce85672e",
+                "sha256:2e9c4f778514a560a9c9aa8e5538bee759b55f6c1dcd35613ad72523fd9175b8",
+                "sha256:338994d3d4ca4cf12f09822e025731a5bdd3a37aaa571fa52659e85ca793fb67",
+                "sha256:33d430a23b661629661f1fe8395be2004006bc792bb9fc7c53911d661b69dd7e",
+                "sha256:385992d5ecf1a93cb85adff2f73e0402dd9ac29b71b7006d342cc920816e6f32",
+                "sha256:3d45864693351c15531f7e76f545ec35000d50848daa833cead96edae1665559",
+                "sha256:40005cbd383438aecf715a7b47fe1e3dcbc889a36461ed416bdec07e0ef1db66",
+                "sha256:4035d6945cb961c90c3e1c1ca2feb526175bcfed44dfb1cc77db4fdced060d3e",
+                "sha256:445d6f4fc3bd9fc2bf0416164454f90acab8858cd5a041403d7a11e3356980e8",
+                "sha256:48c9ec56579d4ba1c88f42302194b8ae2350265cb60c64b7b9a88dcb7fbde309",
+                "sha256:4a5059bd585e9e9504ef9c07e4bc15b0a621ba20504388875d66b8b30a5c4d18",
+                "sha256:4a6e4b0e0531223f53bad07ddf733af490ba2b8367f62342b92b39b29f72735a",
+                "sha256:4b870b6f632fc74941cadc2a0f3064ed8409e6f8ee226cdfd2a85ae50473aa94",
+                "sha256:50fd2d9b36938d4dcecbd684777dd12a407add4f9f934f235c66372e630772b0",
+                "sha256:53e22e4460f0245b468ee645156a4f84d0fc35a12d9ba79bd7d79bdcd2f9629d",
+                "sha256:586a011f77f8a2da4b888774174cd266e69e917a67ba072c7fc0e91878178a80",
+                "sha256:59597cd6315d3439ed4b074febe84a439c33928dd34396941b4d377692eca810",
+                "sha256:59e4b729eae1a0919f9e4c0fc635fbcc9db59c74ad98d684f4877be3d2607dd6",
+                "sha256:5a0f874ee8c0bc820e649c900243c6d1e6dc435b81da1492046716f14f1a2a96",
+                "sha256:5ac2b7d341dc1bd102be849d6dd33b09701223a851105b2754339e390be0627a",
+                "sha256:5e3f4468b8c6fd2fd33c218bbd0a1559e6a6fcf185af8bb0cc43f3b5bfb7d636",
+                "sha256:6164d4e2a82f9ebd7752a06bd6c504791bedc6418c0196cd0a23afb7f3e12b2d",
+                "sha256:6893544e06bae009916a5658ce7207e26ed17385149f35a3125f5259951f1bbe",
+                "sha256:690a17db524ee6ac4a27efc5406530dd90e7a7a69d8360235323d0e5dafb8f5b",
+                "sha256:6b8d0c153f07a953636b9cdb3011b733cadd4178123ef728ccc4d5969e67f3c2",
+                "sha256:72a28979cc667e5f82ef433db009184e7ac277844eea0f7f4d254b789517941d",
+                "sha256:72aa4746993a28c841e05889f3f1b1e5d14df8d3daa157d6001a34c98102b393",
+                "sha256:732176f5427e72fa2325b05c58ad0b45af341c459910d766f814b0584ac1f9ac",
+                "sha256:7918a1b83dd70dc04ab5ed24c78ae833ae8ea228cef84e08597c408286edc926",
+                "sha256:7923470d6056a9590247ff729c05e8e0f06bbd4efa6569c916943cb2d9b68b91",
+                "sha256:7d76a8a1fc9da08296462a18f16620ba73bcbf5909e42383b253ef34d9d5141e",
+                "sha256:811040d7f3dd9c55eb0d8b00b5dcb7fd9ae1761c454f444fd9f37fe5ec57143a",
+                "sha256:821a88b878b6589c5068f4cc2cfeb2c64e343a196bc9d7ac68ea8c2a776acd46",
+                "sha256:84397d3f750d153ebd7f958efaa92b45fea170200e2df5e0e1fd4d85b7e3f58a",
+                "sha256:844671c9c1150fcdac46d43198364034b961bd520f2c4fdaabfc7c7d7138a2dd",
+                "sha256:890a09cb0a62198bff92eda98b2b507305dd3abf974778bae3287f98b48907d3",
+                "sha256:8f08276466fedb9e36e5193a96cb944928301152879ec20c2d723d1031cd4ddd",
+                "sha256:8f5e06df94fff8c4c85f98c6487f6636848e1dc85ce17ab7d1931df4a081f657",
+                "sha256:921473a93bcea4d00295799ab929522fc650e85c6b9f27ae1e6bb32a790ea7d3",
+                "sha256:941b3f1b2392f0bcd6abf1bc7a322787d6db4e7457be6d1ffd3a693426a755f2",
+                "sha256:9b320677521aabf666cdd6e99baee4fb5ac3996349c3b7f8e7c4eee1c00dfe3a",
+                "sha256:9c3efee9bb53cbe7b285760c81f28ac80dc15fa48b5fe7e58b52752e642553f1",
+                "sha256:9fda3e50abad8d0f48df621cf75adc73c63f7243cbe0e3b2171392b445401550",
+                "sha256:a4c5da39bca4f7979eefcbb36efea04471cd68db2d38fcbb4ee2c6d440699833",
+                "sha256:a56c18f21ac98209da9c54ae3ebb3b6f6e772038681d6cb43b8d53da3b09ee81",
+                "sha256:a623564d810e7a953ff1357f7799c14bc9beeab699aacc8b7ab7822da1e952b8",
+                "sha256:a8906669b03c63266b6a7693d1f487b02647beb12adea20f8840c1a087e2dfb5",
+                "sha256:a99757ad7fe5c8a2bb44829fc57ced11253e10f462233c1255fe03888e06bc19",
+                "sha256:aa7d032c1d84726aa9edeb6accf079b4caa87151ca9fabacef31fa028186c66d",
+                "sha256:aad5524c2aedaf9aa14ef1bc9327f8abd915699dea457d339bebbe2f0d218f86",
+                "sha256:afb1c70ec1e594a547f38ad6bf5e3d60304ce7539e677c1429eebab115bce56e",
+                "sha256:b6365703e8cf1644b82104cdd05270d1a9f043119a168d66c55684b1b557d008",
+                "sha256:b8b942d8b3ce765dbc3b1dad0a944712a89b5de290ce8f72681e22b3c55f3cc8",
+                "sha256:ba73a14e9c8f9ac409863543cde3290dba39098fc261f717dc337ea72d3ebad2",
+                "sha256:bd7b68fd2e79d59d86dcbc1ccd6e2ca09c505343445daaa4e07f43c8a9cc34da",
+                "sha256:bd966475e963122ee0a7118ec9024388c602d12ac72860f6eea119a3928be053",
+                "sha256:c2ce65bdeaf0a386bb3b533a28de3994e8e13b464ac15e1e67e4603dd88787fa",
+                "sha256:c64d5abe91a3dfe5ff250c6bb267ef00dbc01501518225b45a5f9def458f31fb",
+                "sha256:c8c143a65ce3ca42e54d8e6fcaf465b6b672ed1c6c90022794a802fb93105d22",
+                "sha256:cd46f30e758629c3ee91713529cfbe107ac50d27110fdcc326a42ce2acf4dafc",
+                "sha256:ced02e3bd55e16e89c08bbc8128cff0884d96e7f7a5633d3dc366b6d95fcd1d6",
+                "sha256:cf123225945aa58b3057d0fba67e8061c62d14cc8a4202630f8057df70189051",
+                "sha256:d19e57f888b00cd04fc38f5e18d0efbd91ccba2d45039453ab2236e6eec48d4d",
+                "sha256:d1cbe6b5be3b9b698d8cc4ee4dee7e017ad655e83361cd0ea8e653d65e469468",
+                "sha256:db09e6c18977a33fea26fe67b7a842f706c67cf8bda1450974d0ae0dd63570df",
+                "sha256:de2f780c3242ea114dd01f84848655356af4dd561501896c751d7b885ea6d3a1",
+                "sha256:e2205a81f815b5bb17e46e74cc946c575b484e5f0acfcb805fb252d67e22938d",
+                "sha256:e645c757183ee0e13f0bbe56508598e2d9cd42b8abc6c0599d53b0d0b8dd1479",
+                "sha256:f2910502f718828cecc8beff004917dcf577fc5f8f5dd40ffb1ea7612124547b",
+                "sha256:f764e4dfafa288e2eba21231f455d209f4709436baeebb05bdecfb5d8ddc3d35",
+                "sha256:f83fe9e10f9d0b6cf580564d4d23845b9d692e4c91bd8be57733958e4c602956",
+                "sha256:fb2b495dd94b02de8215625948132cc2ea360ae84fe6634cd19b6567709c8ae2",
+                "sha256:fee0016cc35a8a91e8cc9312ab26a6fe638d484131a7afa79e1ce6165328a135"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==2023.5.5"
+        },
+        "requests": {
+            "hashes": [
+                "sha256:10e94cc4f3121ee6da529d358cdaeaff2f1c409cd377dbc72b825852f2f7e294",
+                "sha256:239d7d4458afcb28a692cdd298d87542235f4ca8d36d03a15bfc128a6559a2f4"
+            ],
+            "index": "pypi",
+            "version": "==2.30.0"
+        },
+        "six": {
+            "hashes": [
+                "sha256:1e61c37477a1626458e36f7b1d82aa5c9b094fa4802892072e49de9c60c4c926",
+                "sha256:8abb2f1d86890a2dfb989f9a77cfcfd3e47c2a354b01111771326f8aa26e0254"
+            ],
+            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
+            "version": "==1.16.0"
+        },
+        "smmap": {
+            "hashes": [
+                "sha256:2aba19d6a040e78d8b09de5c57e96207b09ed71d8e55ce0959eeee6c8e190d94",
+                "sha256:c840e62059cd3be204b0c9c9f74be2c09d5648eddd4580d9314c3ecde0b30936"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==5.0.0"
+        },
+        "urllib3": {
+            "hashes": [
+                "sha256:61717a1095d7e155cdb737ac7bb2f4324a858a1e2e6466f6d03ff630ca68d3cc",
+                "sha256:d055c2f9d38dc53c808f6fdc8eab7360b6fdbbde02340ed25cfbcd817c62469e"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.0.2"
         },
         "watchdog": {
             "hashes": [
                 "sha256:0e06ab8858a76e1219e68c7573dfeba9dd1c0219476c5a44d5333b01d7e1743a",
                 "sha256:13bbbb462ee42ec3c5723e1205be8ced776f05b100e4737518c67c8325cf6100",
                 "sha256:233b5817932685d39a7896b1090353fc8efc1ef99c9c054e46c8002561252fb8",
                 "sha256:25f70b4aa53bd743729c7475d7ec41093a580528b100e9a8c5b5efe8899592fc",
```

### Comparing `stocktracer-0.1.5/mkdocs.yml` & `stocktracer-0.2.0/mkdocs.yml`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,20 @@
 site_name: StockTracer
+nav:
+  - Welcome: index.md
+  - Getting Started: getting-started.md
+  - Design:
+      # - design/index.md
+      # - Data Retrieval: design/data-retrieval.md
+      # - Analysis: design/analysis.md
+      # - Report: design/report.md
+      - Caching: design/caching.md
+      - Reference: design/reference.md
+  - Code Reference: reference/
+  
 theme:
   name: material
   palette:
     scheme: default
     primary: green
   icon:
     repo: fontawesome/brands/github
@@ -31,14 +43,16 @@
   - gen-files:
       scripts:
       - docs/gen_ref_pages.py 
   - mkdocstrings
   - literate-nav:
       nav_file: SUMMARY.md
   - section-index
+  - git-revision-date-localized:
+      enable_creation_date: false
 markdown_extensions:
   - tables
   - admonition
   - pymdownx.details
   - pymdownx.superfences:
       custom_fences:
         - name: mermaid
@@ -87,18 +101,7 @@
 
       Additionally, we use cookies to recognize your repeated visits and preferences, as well
       as to measure the effectiveness of our documentation and whether users
       find what they're searching for. With your consent, you're helping us to
       make our documentation better. 
 copyright: Copyright &copy; 2023 Gary Yund
 
-nav:
-  - Welcome: index.md
-  - Getting Started: getting-started.md
-  - Design:
-      - design/index.md
-      - Data Retrieval: design/data-retrieval.md
-      # - Analysis: design/analysis.md
-      # - Report: design/report.md
-      - Caching: design/caching.md
-      - Reference: design/reference.md
-  - Code Reference: reference/
```

#### html2text {}

```diff
@@ -1,20 +1,25 @@
-site_name: StockTracer theme: name: material palette: scheme: default primary:
-green icon: repo: fontawesome/brands/github edit: material/pencil view:
-material/eye features: - content.action.edit - navigation.instant -
-navigation.tracking - navigation.sections - navigation.footer # -
-navigation.indexes - toc.follow - toc.integrate # - navigation.expand -
-navigation.tabs - navigation.top # - header.autohide repo_url: https://
-github.com/gyund/fundamental-analysis repo_name: gyund/fundamental-analysis
-edit_uri: edit/main/docs/docs/ plugins: - search - tags - gen-files: scripts: -
-docs/gen_ref_pages.py - mkdocstrings - literate-nav: nav_file: SUMMARY.md -
-section-index markdown_extensions: - tables - admonition - pymdownx.details -
-pymdownx.superfences: custom_fences: - name: mermaid class: mermaid format:
-!!python/name:pymdownx.superfences.fence_code_format - pymdownx.arithmatex:
-generic: true - pymdownx.highlight: anchor_linenums: true line_spans: __span
+site_name: StockTracer nav: - Welcome: index.md - Getting Started: getting-
+started.md - Design: # - design/index.md # - Data Retrieval: design/data-
+retrieval.md # - Analysis: design/analysis.md # - Report: design/report.md -
+Caching: design/caching.md - Reference: design/reference.md - Code Reference:
+reference/ theme: name: material palette: scheme: default primary: green icon:
+repo: fontawesome/brands/github edit: material/pencil view: material/eye
+features: - content.action.edit - navigation.instant - navigation.tracking -
+navigation.sections - navigation.footer # - navigation.indexes - toc.follow -
+toc.integrate # - navigation.expand - navigation.tabs - navigation.top # -
+header.autohide repo_url: https://github.com/gyund/fundamental-analysis
+repo_name: gyund/fundamental-analysis edit_uri: edit/main/docs/docs/ plugins: -
+search - tags - gen-files: scripts: - docs/gen_ref_pages.py - mkdocstrings -
+literate-nav: nav_file: SUMMARY.md - section-index - git-revision-date-
+localized: enable_creation_date: false markdown_extensions: - tables -
+admonition - pymdownx.details - pymdownx.superfences: custom_fences: - name:
+mermaid class: mermaid format: !!python/name:
+pymdownx.superfences.fence_code_format - pymdownx.arithmatex: generic: true -
+pymdownx.highlight: anchor_linenums: true line_spans: __span
 pygments_lang_class: true - pymdownx.inlinehilite - pymdownx.snippets -
 pymdownx.tabbed: alternate_style: true - pymdownx.emoji: emoji_index: !!python/
 name:materialx.emoji.twemoji emoji_generator: !!python/name:
 materialx.emoji.to_svg extra_javascript: - https://unpkg.com/tablesort@5.3.0/
 dist/tablesort.min.js - javascripts/tablesort.js - javascripts/mathjax.js -
 https://polyfill.io/v3/polyfill.min.js?features=es6 - https://cdn.jsdelivr.net/
 npm/mathjax@3/es5/tex-mml-chtml.js extra_css: - stylesheets/extra.css extra:
@@ -27,12 +32,8 @@
 use only and are not considered advice or recommendations. This project makes
 no performance claims or guarantees. Please read the license for this project.
 Usage of any data is at your own risk.
 
 Additionally, we use cookies to recognize your repeated visits and preferences,
 as well as to measure the effectiveness of our documentation and whether users
 find what they're searching for. With your consent, you're helping us to make
-our documentation better. copyright: Copyright © 2023 Gary Yund nav: - Welcome:
-index.md - Getting Started: getting-started.md - Design: - design/index.md -
-Data Retrieval: design/data-retrieval.md # - Analysis: design/analysis.md # -
-Report: design/report.md - Caching: design/caching.md - Reference: design/
-reference.md - Code Reference: reference/
+our documentation better. copyright: Copyright © 2023 Gary Yund
```

### Comparing `stocktracer-0.1.5/requirements.txt` & `stocktracer-0.2.0/requirements.txt`

 * *Files 12% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 -i https://pypi.org/simple
 attrs==23.1.0 ; python_version >= '3.7'
+beartype==0.14.0
 cattrs==22.2.0 ; python_version >= '3.7'
-certifi==2022.12.7 ; python_version >= '3.6'
+certifi==2023.5.7 ; python_version >= '3.6'
 charset-normalizer==3.1.0 ; python_full_version >= '3.7.0'
+diskcache==5.6.1
 exceptiongroup==1.1.1 ; python_version < '3.11'
 fire==0.5.0
 idna==3.4 ; python_version >= '3.5'
 numpy==1.24.3 ; python_version >= '3.10'
 pandas==2.0.1
-platformdirs==3.5.0 ; python_version >= '3.7'
+platformdirs==3.5.1 ; python_version >= '3.7'
 python-dateutil==2.8.2
 pytz==2023.3
-requests==2.29.0
+requests==2.30.0
 requests-cache==1.0.1
 six==1.16.0 ; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'
 tabulate==0.9.0
 termcolor==2.3.0 ; python_version >= '3.7'
 tzdata==2023.3 ; python_version >= '2'
 url-normalize==1.4.3 ; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'
-urllib3==1.26.15 ; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'
+urllib3==2.0.2 ; python_version >= '3.7'
```

### Comparing `stocktracer-0.1.5/.github/ISSUE_TEMPLATE/feature_request.md` & `stocktracer-0.2.0/.github/ISSUE_TEMPLATE/feature_request.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/.github/workflows/cleanup.yml` & `stocktracer-0.2.0/.github/workflows/cleanup.yml`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/.github/workflows/publish-pypi.yml` & `stocktracer-0.2.0/.github/workflows/publish-pypi.yml`

 * *Files 11% similar despite different names*

```diff
@@ -4,15 +4,15 @@
     workflow_call:
         inputs:
             ENVIRONMENT:
                 required: true
                 type: string
 
 concurrency:
-    group: ${{ github.ref }}
+    group: publish-${{ inputs.ENVIRONMENT }}-${{ github.ref }}
     cancel-in-progress: true
 
 jobs:
   pypi:
     runs-on: ubuntu-latest
     environment: ${{ inputs.ENVIRONMENT }}
         # url: https://test-pypi.org/p/<your-pypi-project-name>
@@ -23,14 +23,16 @@
       - name: Set up Python
         uses: actions/setup-python@v4
         with:
           python-version: '3.10'
       - name: Install dependencies
         run: |
           python -m pip install --upgrade pip
+          pip install pipenv
+          pipenv requirements > requirements.txt
           pip install build
       - name: Build package
         # run: python -m build
         run: python3 -m build
       - name: Publish package
         uses: pypa/gh-action-pypi-publish@a56da0b891b3dc519c7ee3284aff1fad93cc8598
         with:
```

### Comparing `stocktracer-0.1.5/.github/workflows/python.yml` & `stocktracer-0.2.0/.github/workflows/python.yml`

 * *Files 24% similar despite different names*

```diff
@@ -1,17 +1,22 @@
 name: tests
 
 on:
   push:
     branches: [ "main" ]
   pull_request:
     branches: [ "main" ]
+    types:
+      - opened
+      - synchronize
+      - reopened
+      - ready_for_review
 
 concurrency:
-  group: ${{ github.ref }}
+  group: python-${{ github.ref }}
   cancel-in-progress: true
   
 jobs:
   build:
     permissions:
       pull-requests: write
       contents: read
@@ -32,62 +37,94 @@
         uses: actions/setup-python@v4
         with:
           python-version: ${{ matrix.python-version }}
           cache: 'pip'
       - name: Install dependencies
         run: |
           python -m pip install --upgrade pip
-          pip install -r requirements-dev.txt
+          pip install pipenv
+          pipenv requirements --dev > requirements.txt
+          pip install -r requirements.txt
       - name: Cache Network Requests
         uses: actions/cache@v3
         with:
-          key: sqlite-${{ hashFiles('**/tests/fixtures/network/**') }}
+          key: sqlite-${{ hashFiles('**/tests/fixtures/network.py') }}
           path: |
             **/.ticker-cache/*.sqlite
-      - name: Test with pytest
+        if: ${{ !github.event.pull_request.draft }}
+      - name: Run - unit-tests
         run: |
-          coverage run -m pytest --run-webtest --doctest-modules
+          coverage run -m pytest --doctest-modules
+          # coverage run -m pytest --run-webtest --doctest-modules
           coverage report
           # coveralls --service=github
-      - name: Run smoke test
+      # Just to cut down on network testing while initially iterating
+      - name: Run - network-tests
         run: |
-          coverage run -a -m stocktracer --help
-          coverage run -a -m stocktracer analyze --help
-          coverage run -a -m stocktracer export --help
-          coverage report
+          coverage run -a -m pytest -m webtest --run-webtest
+        if: ${{ !github.event.pull_request.draft }}
       - name: Coveralls
         run: |
           coveralls --service=github
       # - name: Coveralls
       #   uses: coverallsapp/github-action@v2
       #   with:
       #     github-token: ${{ secrets.GITHUB_TOKEN }}
       #     flag-name: run-${{ join(matrix.*, '-') }}
       #     parallel: true
       #     format: python
       #   if: ${{ success() }}
+      
+      # - name: Upload pytest test results
+      #   uses: actions/upload-artifact@v3
+      #   with:
+      #     name: pytest-results-${{ matrix.python-version }}
+      #     path: junit/test-results-${{ matrix.python-version }}.xml
+      #   # Use always() to always run this step to publish test results when there are test failures
+      #   if: ${{ always() }}
+
+  lint:
+    runs-on: ubuntu-latest
+    steps:
+      - uses: actions/checkout@v3
+      - name: Set up Python ${{ matrix.python-version }}
+        uses: actions/setup-python@v4
+        with:
+          python-version: ${{ matrix.python-version }}
+          cache: 'pip'
+      - name: Install dependencies
+        run: |
+          python -m pip install --upgrade pip
+          pip install pipenv
+          pipenv requirements --dev > requirements.txt
+          pip install -r requirements.txt
       - name: Lint - Ruff 
         run: |
           ruff src 
         if: ${{ always() }}
       - name: Lint - Black
         run: |
           black --check src
         if: ${{ always() }}
       - name: Lint - isort
         run: |
           isort --check src
         if: ${{ always() }}
-      # - name: Upload pytest test results
-      #   uses: actions/upload-artifact@v3
-      #   with:
-      #     name: pytest-results-${{ matrix.python-version }}
-      #     path: junit/test-results-${{ matrix.python-version }}.xml
-      #   # Use always() to always run this step to publish test results when there are test failures
+      - name: Lint - pylint (src/stocktracer)
+        run: |
+          pylint src/stocktracer
+        if: ${{ always() }}
+      # - name: Lint - pydocstyle
+      #   run: |
+      #     pydocstyle
       #   if: ${{ always() }}
+      - name: Lint - pydoctest
+        run: |
+          PYTHONPATH=src pipenv run pydoctest --config pydocktest.json
+        if: ${{ always() }}
 
   finish:
     needs: build
     if: ${{ always() }}
     runs-on: ubuntu-latest
     env:
       GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Comparing `stocktracer-0.1.5/.github/workflows/release-test.yml` & `stocktracer-0.2.0/.github/workflows/release-test.yml`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/.github/workflows/release.yml` & `stocktracer-0.2.0/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/gen_ref_pages.py` & `stocktracer-0.2.0/docs/gen_ref_pages.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 from pathlib import Path
 
 import mkdocs_gen_files
 
 nav = mkdocs_gen_files.Nav()
 
-for path in sorted(Path("src/ticker").rglob("*.py")):  # 
+for path in sorted(Path("src/stocktracer").rglob("*.py")):  # 
     module_path = path.relative_to(".").with_suffix("")  # 
     doc_path = path.relative_to(".").with_suffix(".md")  # 
     full_doc_path = Path("reference", doc_path)  # 
 
     parts = list(module_path.parts)
 
     if parts[-1] == "__init__":  #
```

### Comparing `stocktracer-0.1.5/docs/getting-started.md` & `stocktracer-0.2.0/docs/getting-started.md`

 * *Files 8% similar despite different names*

```diff
@@ -34,23 +34,20 @@
 
 
 ## Plugins
 
 If you wish to use your own analysis plugin, create your own module that implements this interface:
 
 ```python
-from ticker.cli import Options, ReportOptions
 from ticker.data.sec import DataSelector as SecDataSelector
 from ticker.filter import Selectors,SecFilter
 
 def analyze(options: Options) -> None:
     print("This is where we would start to process information, but we're not right now")
 
-def report(options: ReportOptions) -> None: 
-    print("This is where we would report our findings, but we're not right now")
 ```
 
 Then call the tool in the following manner:
 
 ```sh
 python -m ticker analyze --tickers aapl,msft --analysis_plugin 'mypkg.analysis'
 ```
```

### Comparing `stocktracer-0.1.5/docs/design/analysis.md` & `stocktracer-0.2.0/docs/design/analysis.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/design/caching.md` & `stocktracer-0.2.0/docs/design/caching.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/design/data-retrieval.md` & `stocktracer-0.2.0/docs/design/data-retrieval.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/design/reference.md` & `stocktracer-0.2.0/docs/design/reference.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/design/report.md` & `stocktracer-0.2.0/docs/design/report.md`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/docs/stylesheets/extra.css` & `stocktracer-0.2.0/docs/stylesheets/extra.css`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/src/stocktracer/analysis/diluted_eps.py` & `stocktracer-0.2.0/docs/src/stocktracer/analysis/diluted_eps.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 import logging
+from typing import Optional
 
 import numpy as np
 import pandas as pd
+from beartype import beartype
 
-from stocktracer.cli import Options, ReportOptions
-from stocktracer.data.sec import DataSelector as SecDataSelector
 from stocktracer.data.sec import Filter as SecFilter
-from stocktracer.data.sec import ReportDate
 from stocktracer.data.sec import Sec as SecDataSource
+from stocktracer.interface import Analysis as AnalysisInterface
 
 logger = logging.getLogger(__name__)
 
 
+@beartype
 def trendline(data: pd.Series, order: int = 1) -> float:
-    """Calculate the trend of a series
+    """Calculate the trend of a series.
 
     >>> trendline(pd.Series((1,2,3)))
     1.0000000000000004
 
     Args:
         data (pd.Series): _description_
         order (int): _description_. Defaults to 1.
@@ -26,54 +27,41 @@
         float: slope of the trend line
     """
     coeffs = np.polyfit(data.index.values, list(data), order)
     slope = coeffs[-2]
     return float(slope)
 
 
-def analyze(options: Options) -> None:
-    """Perform an analysis on the earnings per share over time
+@beartype
+class Analysis(AnalysisInterface):
+    """Perform an analysis on the earnings per share over time."""
+
+    under_development = True
+    years_of_analysis = 5
+
+    def analyze(self) -> Optional[pd.DataFrame]:
+        # Create the filter we'll use to scrape the results
+        sec_filter = SecFilter(
+            tags=["EarningsPerShareDiluted"],
+            years=self.years_of_analysis,
+            last_report=self.options.last_report,
+            only_annual=True,  # We only want the 10-K
+        )
+
+        # Create an SEC Data Source
+        assert self.options is not None
+        assert self.options.cache_path is not None
+        sec = SecDataSource(storage_path=self.options.cache_path)
+        sec.select_data(tickers=self.options.tickers, filter=sec_filter)
+
+        # # Show a quick dump of the data
+        # logger.info(f"\n{data_selector.data}")
+
+        # # Get only the EPSD Data
+        eps_diluted = sec_filter.filtered_data.query("tag == 'EarningsPerShareDiluted'")
+        # TODO: Figure this out
+        # return eps_diluted.groupby(["cik"]).apply(lambda x: pd.Series(trendline(x.value),
+        #                                                               index=["trend"]))
+        return eps_diluted
 
-    Args:
-        options (Options): options to use for processing
-    """
-    # Create the filter we'll use to scrape the results
-    sec_filter = SecFilter(
-        tags=["EarningsPerShareDiluted"],
-        years=1,  # Over the past 5 years
-        last_report=ReportDate(year=2023, quarter=1),
-        only_annual=True,  # We only want the 10-K
-    )
-
-    # Create an SEC Data Source
-    sec = SecDataSource(storage_path=options.cache_path)
-    data_selector = sec.getData(tickers=options.tickers, filter=sec_filter)
-
-    # Show a quick dump of the data
-    logger.info(f"\n{data_selector.data}")
-
-    results = list[tuple[str, int]]
-    for t in options.tickers:
-        ticker_ds = data_selector.select(ticker=t)
-        try:
-            eps_diluted = ticker_ds.EarningsPerShareDiluted
-            trend = trendline(data=eps_diluted)
-            results.append((t, trend))
-        except AttributeError as ex:
-            logger.warning(f"{t}: {ex}")
-
-    print(f"Trends:\n{results}")
-
-
-def report(options: ReportOptions) -> None:
-    """Generate a report
-
-    As a stub, this does nothing, but normally it provides a mechanism
-    to customize the report generated from the analysis phase.
-
-    This allows you to keep processed data in a intermediary format and create reports from
-    already processed data without having to do it again.
-
-    Args:
-        options (ReportOptions): Reporting options to use for processing
-    """
-    print("This is where we would report our findings, but we're not right now")
+    # Reuse documentation from parent
+    analyze.__doc__ = AnalysisInterface.analyze.__doc__
```

### Comparing `stocktracer-0.1.5/src/stocktracer/data/sec.py` & `stocktracer-0.2.0/docs/src/stocktracer/data/sec.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,112 +1,255 @@
+"""This data source grabs information from quarterly SEC data archives."""
 import logging
-import math
 from datetime import date, timedelta
 from io import BytesIO
 from pathlib import Path
-from typing import Literal, get_args
+from typing import Literal, Optional, SupportsInt
 from zipfile import ZipFile
 
+import numpy as np
 import pandas as pd
-from requests_cache import CachedSession, FileCache, SQLiteCache
+from beartype import beartype
+from beartype.typing import Callable, Sequence
+from requests_cache import CachedSession, SQLiteCache
 
 logger = logging.getLogger(__name__)
 
-default_chunk_size = 1000000
+DEFAULT_CHUNK_SIZE = 1000000
+pd.set_option("mode.chained_assignment", "raise")
 
 
+@beartype
 class ReportDate:
     def __init__(
         self,
-        year: int = date.today().year,
-        quarter: int = math.floor((date.today().month - 1) / 3) + 1,
+        year: int | None = None,
+        quarter: int | None = None,
     ):
-        if year > date.today().year:
+        """ReportDate is used to select and identify archives created by the SEC.
+
+        Args:
+            year (int, optional): Year of the archive. Defaults to date.today().year.
+            quarter (int, optional): Quarter the archive was created. Defaults to ((date.today().month - 1) // 3)+1.
+
+        Raises:
+            ValueError: If the value for quarter or year is invalid
+        """
+        self.year = date.today().year if year is None else year
+        self.quarter = (
+            ((date.today().month - 1) // 3) + 1 if quarter is None else quarter
+        )
+
+        if self.year > date.today().year:
             raise ValueError(
                 "you cannot request reports in the future...that would be illegal :)"
             )
-        if not quarter in range(1, 5):
+        if self.quarter not in range(1, 5):
             raise ValueError(
                 f"the quarter must be a value between 1 and 4 - given: {quarter}"
             )
-        self.year = year
-        self.quarter = quarter
 
-    def __eq__(self, other: "ReportDate") -> bool:
-        """
+    def __str__(self) -> str:
+        return f"{self.year}-q{self.quarter}"
 
-        Args:
-            other ('ReportDate'): _description_
+    def __repr__(self) -> str:
+        return f"ReportDate({self.year},{self.quarter})"
 
-        Returns:
-            bool: true if equal
-        """
+    def __eq__(self, other: "ReportDate") -> bool:
         return self.quarter == other.quarter and self.year == other.year
 
 
+@beartype
 class TickerReader:
-    def __init__(self, data: bytes):
+    def __init__(self, data: str):
         self._data = pd.read_json(data, orient="index")
 
-    def getCik(self, ticker: str) -> int:
-        """Get the Cik from the stock ticker
+    def convert_to_cik(self, ticker: str) -> np.int64:
+        """Get the Cik from the stock ticker.
 
         Args:
             ticker (str): stock ticker. The case does not matter.
 
+        Raises:
+            LookupError: If ticker is not found
+
         Returns:
-            int: cik
+            np.int64: cik
         """
-        result = self._data[self._data.ticker == ticker.upper()]
+        result = self._data[
+            self._data.ticker == ticker.upper()  # pylint: disable=no-member
+        ]  # pylint: disable=no-member
+        if result.empty:
+            raise LookupError(f"unable to find ticker: {ticker}")
         return result.cik_str.iloc[0]
 
-    def getTicker(self, cik: int) -> str:
-        """Get the stock ticker from the Cik number
+    def convert_to_ticker(self, cik: int) -> str:
+        """Get the stock ticker from the Cik number.
 
         Args:
             cik (int): Cik number for the stock
 
         Returns:
             str: stock ticker
         """
-        result = self._data[self._data.cik_str == cik]
+        result = self._data[self._data.cik_str == cik]  # pylint: disable=no-member
         return result.ticker.iloc[0]
 
+    def contains(self, tickers: frozenset) -> bool:
+        """Check that the tickers provided exist.
+
+        Args:
+            tickers (frozenset): tickers to check
+
+        Returns:
+            bool: if all the tickers are found
+        """
+        for t in tickers:
+            self.convert_to_cik(t)
+
+        return True
+
 
 period_focus_options = Literal["FY", "Q1", "Q2", "Q3", "Q4"]
 
 
+@beartype
 class Filter:
+    class Table:
+        """This is a table that is the output from a `Filter.select()` call.
+
+        When data is converted, it creates a pivot table that looks like the following:
+
+                                                        value
+            cik    tag
+            320193 EntityCommonStockSharesOutstanding   4000.0
+                    FakeAttributeTag                     400.0
+            ...
+
+
+        """
+
+        def __init__(self, table: pd.DataFrame) -> None:
+            self.data = table
+
+        def __str__(self) -> str:
+            return str(self.data)
+
+        @property
+        def tags(self):
+            return self.data.index.get_level_values("tag").unique()
+
+        def get_value(self, ticker_or_cik: str | int, tag: str) -> SupportsInt:
+            # TODO: access the either the ticker or cik index
+            if isinstance(ticker_or_cik, int):
+                return self.data.query(
+                    f'cik == {ticker_or_cik} and tag == "{tag}"'
+                ).values[0]
+            # Lookup convert ticker to cik
+            ticker_or_cik = ticker_or_cik.upper()
+            return self.data.query(
+                f'ticker == "{ticker_or_cik}" and tag == "{tag}"'
+            ).values[0]
+
     def __init__(
         self,
-        tags: list[str],
-        years: int = 5,
+        tags: Optional[list[str]] = None,
+        years: int = 1,
         last_report: ReportDate = ReportDate(),
         only_annual: bool = True,
     ) -> None:
         """Filter for SEC tools to scrape relevant information when processing records.
 
         This is an important concept to dealing with large data sets. It allows us to chunk processing
         into batches and find/locate only records of interest. Without these filters, the tool would
         require absurd amounts of memory and storage to process.
 
         Args:
-            tags (list[str]): list of tags found in the SEC report, such as 'EntityCommonStockSharesOutstanding'
-            years (int): years of reports desired. Defaults to 5.
+            tags (Optional[list[str]]): list of tags found in the SEC report, such as 'EntityCommonStockSharesOutstanding'
+            years (int): years of reports desired. Defaults to 1.
             last_report (ReportDate): most recent SEC data dump identified by the year an quarter. Defaults to ReportDate().
             only_annual (bool): If true, only scrape the annual reports. Defaults to True.
         """
         self.tags = tags
         self.years = years
         self.last_report = last_report
         self.only_annual = only_annual
         self._cik_list: set[int] = None
+        self._filtered_data: pd.DataFrame = None
+
+    @property
+    def filtered_data(self) -> pd.DataFrame:
+        """Filtered data looks like this(in csv format):
+
+        .. code-block:: text
+
+            ticker,tag,cik,ddate,uom,value,period,fy,fp,title
+            TMO,EarningsPerShareDiluted,97745,2022-12-31,USD,17.63,2022-12-31,2022.0,FY,THERMO FISHER SCIENTIFIC INC.
+            TMO,EarningsPerShareDiluted,97745,2020-12-31,USD,15.96,2022-12-31,2022.0,FY,THERMO FISHER SCIENTIFIC INC.
+            TMO,EarningsPerShareDiluted,97745,2021-12-31,USD,19.46,2022-12-31,2022.0,FY,THERMO FISHER SCIENTIFIC INC.
+
+        Returns:
+            pd.DataFrame: _description_
+        """
+        return self._filtered_data
+
+    @filtered_data.setter
+    def filtered_data(self, filtered_data: pd.DataFrame):
+        self._filtered_data = filtered_data
+
+    def __str__(self) -> str:
+        """
+        >>> print(Filter(["Income","Debt"],5,ReportDate(2023,1)))
+        Filter on 2023-q1 and the previous 5 years
+        Annual Only: True
+        CIK(s): None
+        Tags: Income,Debt
+        """
+        return f"""Filter on {self.last_report} and the previous {self.years} years
+Annual Only: {self.only_annual}
+CIK(s): {','.join([str(i) for i in self._cik_list]) if self._cik_list else 'None'}
+Tags: {','.join(self.tags) if self.tags else 'None'}"""
+
+    def select(
+        self,
+        aggregate_func: Optional[
+            Callable | Literal["mean", "std", "var", "sum", "min", "max"]
+        ] = "mean",
+        tickers: Optional[Sequence[str]] = None,
+    ) -> Table:
+        """Select only a subset of the data matching the specified criteria.
+
+        Args:
+            aggregate_func (Optional[Callable | Literal['mean', 'std', 'var', 'sum', 'min','max']]): Numpy function to use for aggregating the results. This should be a function like `numpy.average` or `numpy.sum`.
+            tickers (Optional[Sequence[str]]): ticker symbol for the company
+
+        Returns:
+            Filter.Table: Object that represents a pivot table with the data requested
+        """
+        if tickers is not None:
+            tickers = [t.upper() for t in tickers]
+            logger.debug(f"ticker filter: {tickers}")
+
+        data = (
+            self.filtered_data
+            if tickers is None
+            else self.filtered_data.query("ticker in @tickers")
+        )
+        logger.debug(f"pre-pivot:\n{data}")
+        table: pd.DataFrame = pd.pivot_table(
+            data,
+            values="value",
+            index=["cik", "tag", "ticker"],
+            aggfunc=aggregate_func,
+        )
+        return Filter.Table(table)
 
-    def getCikList(self) -> set[int]:
-        """Retrieves a list of CIK values corresponding to the tickers being looked up
+    @property
+    def ciks(self) -> set[int]:
+        """Retrieves a list of CIK values corresponding to the tickers being looked up.
 
         The SEC object will call populateCikList to generate this information. This helps
         with dependency injection by avoiding the Filter having to maintain references to
         these helper objects for temporary processing. It also lets us stub out the information
         provided without having to involve heavier utilities or network access.
 
         Raises:
@@ -117,59 +260,62 @@
         """
         if self._cik_list is None:
             raise LookupError(
                 "Filter was not provided a mapping of cik's based on the tickers."
             )
         return self._cik_list
 
-    def populateCikList(self, tickers: list[str], ticker_reader: TickerReader) -> None:
+    def populate_ciks(
+        self, tickers: frozenset[str], ticker_reader: TickerReader
+    ) -> None:
         """Populates the filter's CIK list to be used for filtering.
 
         The Filter doesn't need the ticker symbols. If we expand to other data sources,
         we would have to repeat ticker symbols. For now, the only info we need in the
         report is the CIK values to find the corresponding stocks.
 
         Args:
-            tickers (list[str]): ticker symbols to search for
+            tickers (frozenset[str]): ticker symbols to search for
             ticker_reader (TickerReader): reader to convert ticker symbols to CIK values
         """
         self._cik_list = set()
         for ticker in tickers:
-            cik = ticker_reader.getCik(ticker)
+            cik = ticker_reader.convert_to_cik(ticker)
             self._cik_list.add(cik)
 
-    def getFocusPeriod(self) -> list[str]:
-        """Get the focus period for the report
+    @property
+    def focus_period(self) -> list[str]:
+        """Get the focus period for the report.
 
         Companies file quarterly reports. The annual report replaces the quarterly
         report depending on when that is reported. Typically Q4 is replaced with FY
         for the annual reports.
 
         Returns:
             list[str]: list of focus periods to use for the filter
         """
         if self.only_annual:
             return ["FY"]
-        else:
-            return ["FY", "Q1", "Q2", "Q3", "Q4"]
+        return ["FY", "Q1", "Q2", "Q3", "Q4"]
 
-    def getRequiredReports(self) -> list[ReportDate]:
+    @property
+    def required_reports(self) -> list[ReportDate]:
         """Get a list of required reports to download for all the quarters.
 
         The list generated will include an extra quarter so that you will always be
         able to do analysis from the current quarter to the previous quarter.
 
         Also note that it doesn't matter if you specify only_annual=True. Because
         companies don't have the same fiscal year, we have to check every quarterly
         report just to see if their annual report is in there.
 
         Returns:
             list[ReportDate]: list of report dates to retrieve
         """
-        dl_list: list[ReportDate] = list()
+        dl_list: list[ReportDate] = []
         next_report = self.last_report
         final_report = ReportDate(
             self.last_report.year - self.years, self.last_report.quarter
         )
         while 1:
             dl_list.append(
                 ReportDate(year=next_report.year, quarter=next_report.quarter)
@@ -180,70 +326,78 @@
                 next_report.quarter = 4
                 next_report.year -= 1
             else:
                 next_report.quarter -= 1
         return dl_list
 
 
+@beartype
 class DataSetReader:
-    """Reads the data from a zip file retrieved from the SEC website"""
+    """Reads the data from a zip file retrieved from the SEC website."""
 
     def __init__(self, zip_data: bytes) -> None:
         self.zip_data = BytesIO(zip_data)
 
-    def processZip(self, filter: Filter) -> pd.DataFrame:
-        """Process a zip archive with the provided filter
+    def process_zip(self, filter: Filter) -> Optional[pd.DataFrame]:
+        """Process a zip archive with the provided filter.
 
         Args:
             filter (Filter): results to filter out of the zip archive
 
         Raises:
             ImportError: the filter doesn't match anything
 
         Returns:
-            pd.DataFrame: filtered data
+            Optional[pd.DataFrame]: filtered data
         """
         with ZipFile(self.zip_data) as myzip:
             # Process the mapping first
             logger.debug("opening sub.txt")
             with myzip.open("sub.txt") as myfile:
                 # Get reports that are 10-K or 10-Q
-                sub_dataframe = DataSetReader._processSubText(myfile, filter)
+                sub_dataframe = DataSetReader._process_sub_text(myfile, filter)
 
                 if sub_dataframe is None or sub_dataframe.empty:
                     raise ImportError("nothing found in sub.txt matching the filter")
 
                 with myzip.open("num.txt") as myfile:
-                    return DataSetReader._processNumText(myfile, filter, sub_dataframe)
-
-    def _processNumText(
-        filepath_or_buffer, filter: Filter, sub_dataframe: pd.DataFrame
-    ) -> pd.DataFrame:
-        """Contains the numerical data
+                    return DataSetReader._process_num_text(
+                        myfile, filter, sub_dataframe
+                    )
+
+    @classmethod
+    def _process_num_text(
+        cls, filepath_or_buffer, filter: Filter, sub_dataframe: pd.DataFrame
+    ) -> Optional[pd.DataFrame]:
+        """Contains the numerical data.
 
         adsh	tag	version	coreg	ddate	qtrs	uom	value	footnote
 
         """
         logger.debug("processing num.txt")
         reader = pd.read_csv(
             filepath_or_buffer,
             delimiter="\t",
             usecols=["adsh", "tag", "ddate", "uom", "value"],
             index_col=["adsh", "tag"],
-            chunksize=default_chunk_size,
+            chunksize=DEFAULT_CHUNK_SIZE,
             parse_dates=["ddate"],
         )
 
         filtered_data: pd.DataFrame = None
         chunk: pd.DataFrame
         for chunk in reader:
             # We want only the tables in left if they join on the key, so inner it is
             data = chunk.join(sub_dataframe, how="inner")
-            tag_list = filter.tags
-            data = data.query("tag in @tag_list")
+
+            # Additional Filtering if needed
+            if filter.tags is not None:
+                tag_list = filter.tags  # pylint: disable=unused-variable
+                data = data.query("tag in @tag_list")
+
             if data.empty:  # pragma: no cover
                 logger.debug(f"chunk:\n{chunk}")
                 logger.debug(f"sub_dataframe:\n{sub_dataframe}")
                 continue
 
             if filtered_data is None:
                 filtered_data = data
@@ -251,63 +405,71 @@
                 filtered_data.merge(data)
 
             filtered_data.merge(data)
         if filtered_data is not None:  # pragma: no cover
             logger.debug(f"Filtered Records (head+5): {filtered_data.head()}")
         return filtered_data
 
-    def _processSubText(filepath_or_buffer, filter: Filter) -> pd.DataFrame:
-        """Contains the submissions
+    @classmethod
+    def _process_sub_text(
+        cls, filepath_or_buffer, filter: Filter
+    ) -> Optional[pd.DataFrame]:
+        """Contains the submissions.
 
         adsh	cik	name	sic	countryba	stprba	cityba	zipba	bas1	bas2	baph	countryma
         stprma	cityma	zipma	mas1	mas2	countryinc	stprinc	ein	former	changed	afs	wksi
         fye	form	period	fy	fp	filed	accepted	prevrpt	detail	instance	nciks	aciks
         """
-        assert True == isinstance(filter, Filter)
         logger.debug("processing sub.txt")
-        focus_periods = filter.getFocusPeriod()
-        cik_list = filter.getCikList()
+        focus_periods = filter.focus_period
+        cik_list = filter.ciks  # pylint: disable=unused-variable
+
+        oldest_fy = filter.last_report.year - filter.years
+        query_str = f"cik in @cik_list and fp in @focus_periods and fy >= {oldest_fy}"
+        logger.debug(f"Query string: {query_str}")
         reader = pd.read_csv(
             filepath_or_buffer,
             delimiter="\t",
             usecols=["adsh", "cik", "period", "fy", "fp"],
             index_col=["adsh", "cik"],
-            chunksize=default_chunk_size,
+            chunksize=DEFAULT_CHUNK_SIZE,
             parse_dates=["period"],
         )
         logger.debug(f"keeping only these focus periods: {focus_periods}")
         filtered_data: pd.DataFrame = None
         chunk: pd.DataFrame
         for chunk in reader:
-            data = chunk.query("cik in @cik_list and fp in @focus_periods")
+            data = chunk.query(query_str)
             if data.empty:
                 continue
             if filtered_data is None:
                 filtered_data = data
             else:
                 filtered_data.merge(data)
         if filtered_data is not None:
             logger.debug(f"Filtered Records (head+5):\n{filtered_data.head()}")
         return filtered_data
 
 
+@beartype
 class DownloadManager:
     # Format of zip example: 2023q1.zip
     _base_url = "https://www.sec.gov/files/dera/data/financial-statement-data-sets"
 
     _company_tickers_url = "https://www.sec.gov/files/company_tickers.json"
 
     def __init__(
         self, ticker_session: CachedSession, data_session: CachedSession
     ) -> None:
         self._ticker_session = ticker_session
         self._data_session = data_session
 
-    def getTickers(self) -> TickerReader:
-        """Get the CIK ticker mappings. This must be done before processing reports
+    @property
+    def ticker_reader(self) -> TickerReader:
+        """Get the CIK ticker mappings. This must be done before processing reports.
 
         The SEC stores the mappings of the CIK values to tickers in a JSON file.
         We can download and cache this information essentially for a year. We're
         not interested in companies that recently listed because they don't have a
         long regulated record of reported earnings. When we process the records, we can
         ignore cik values that are not in this list.
 
@@ -322,156 +484,120 @@
 
         """
         response = self._ticker_session.get(self._company_tickers_url)
         if response.from_cache:  # pragma: no cover
             logger.info("Retrieved tickers->cik mapping from cache")
         if response.status_code == 200:  # pragma: no cover
             return TickerReader(response.content.decode())
-        else:  # pragma: no cover
-            return TickerReader(pd.DataFrame())
+        return TickerReader(pd.DataFrame())  # pragma: no cover
 
-    def _createDownloadUri(self, report_date: ReportDate) -> str:
+    def _create_download_uri(self, report_date: ReportDate) -> str:
         file = f"{report_date.year}q{report_date.quarter}.zip"
         return "/".join([self._base_url, file])
 
-    def getData(self, report_date: ReportDate) -> DataSetReader:
-        """Retrieves from a cache or makes a request to retrieve archived quarterly data.
+    def get_quarterly_report(self, report_date: ReportDate) -> Optional[DataSetReader]:
+        """Retrieve from a cache or make a request archived quarterly data.
 
         This allows us to download data independent of actually processing it, allowing
         us to prefetch information we need if we like.
 
         Args:
             report_date (ReportDate): information specifying the quarterly dump to retrieve
 
         Returns:
-            DataSetReader: this object helps process the data received more granularly
+            Optional[DataSetReader]: this object helps process the data received more granularly
         """
-        request = self._createDownloadUri(report_date)
+        request = self._create_download_uri(report_date)
         response = self._data_session.get(request)
         if response.from_cache:
             logger.info(f"Retrieved {request} from cache")
         if response.status_code == 200:
             return DataSetReader(response.content)
-        else:
-            return DataSetReader(pd.DataFrame())
-
-
-class DataSelector:
-    """A DataSelector contains all the data we know about.
-
-    The purpose of this class is to narrow down and select relevant subsets of the data
-    based on specific criteria.
-    """
-
-    _report_types = Literal["quarterly", "annual"]
-    _period_focus = Literal["FY", "Q1", "Q2", "Q3", "Q4"]
-
-    def __init__(self, data: pd.DataFrame, ticker_reader: TickerReader) -> None:
-        """Class for helping select data
-
-        This helps the user to some extent avoid some specifics about the pandas table structure.
-
-        Args:
-            data (pd.DataFrame): Filtered data from processing
-            ticker_reader (TickerReader): Reader that helps convert tickers to CIKs
-        """
-        self.data: pd.DataFrame = data
-        self._ticker_reader: TickerReader = ticker_reader
-
-    def getTags(self) -> pd.Index:
-        """Get a list of the tag values filtered from the results
-
-        Returns:
-            pd.Index: tag values
-        """
-        return self.data.index.get_level_values("tag").unique()
-
-    def _getCik(self, ticker: str):
-        return self._ticker_reader.getCik(ticker)
-
-    def filterByTicker(self, ticker: str, data: pd.DataFrame = None) -> pd.DataFrame:
-        """Filter results using the ticker symbol.
-
-        Args:
-            ticker (str): ticker to select
-            data (pd.DataFrame): alternate data to use for filtering. Use this if you've previously filtered the data and are using this in addition.
-
-        Returns:
-            pd.DataFrame: Filtered result containing ticker results
-        """
-        assert isinstance(ticker, str)
-        assert data is None or isinstance(data, pd.DataFrame)
-        cik = self._getCik(ticker)
-
-        # Supply the object default if not provided in the method
-        if data is None or data.empty:
-            data = self.data
-        return data.query(f"cik == {cik}")
-
-    def select(
-        self,
-        ticker: str,
-    ) -> pd.DataFrame:
-        """Select only a subset of the data matching the specified criteria
-
-        Args:
-            ticker (str): ticker symbol for the company
-
-        Returns:
-            pd.DataFrame: filtered DataFrame
-        """
-        assert True == isinstance(ticker, str)
-        # Filter out the Stock
-        df = self.filterByTicker(ticker=ticker)
-        return df
+        return None  # pragma: no cover
 
 
+@beartype
 class DataSetCollector:
+    """Take care of downloading all the data sets and aggregate them into a single structure."""
+
     def __init__(self, download_manager: DownloadManager):
         self.download_manager = download_manager
 
-    """ Take care of downloading all the data sets and aggregate them into a single structure """
-
-    def getData(self, filter: Filter) -> pd.DataFrame:
-        """Collect data based on the provided filter
+    def get_data(self, filter: Filter) -> None:
+        """Collect data based on the provided filter.
 
         Args:
             filter (Filter): SEC specific filter of how to filter the results
 
-        Returns:
-            pd.DataFrame: filtered results
+        Raises:
+            LookupError: when there are no results matching the filter
+
         """
-        df = None
-        report_dates = filter.getRequiredReports()
+        data_frame = None
+        report_dates = filter.required_reports
         logger.info(f"Creating Unified Data record for these reports: {report_dates}")
         for r in report_dates:
-            reader = self.download_manager.getData(r)
-            try:
-                data = reader.processZip(filter)
-                if df is None:
-                    logger.debug(f"keys: {data.keys()}")
-                    df = data
-                else:
-                    # df = pd.concat(df, data)
-                    df.merge(right=data)
-            except ImportError as e:
-                # Note, when searching for annual reports, this will generally occur 1/4 times
-                # if we're only searching for one stock's tags
-                logger.warning(f"{r} did not have any matches for the provided filter")
+            reader = self.download_manager.get_quarterly_report(r)
+            if isinstance(reader, DataSetReader):
+                try:
+                    data = reader.process_zip(filter)
+                    if data is None or data.empty:
+                        logger.debug(f"no results captured in report {r}")
+                    elif data_frame is None:
+                        logger.debug(f"keys: {data.keys()}")
+                        data_frame = data
+                    else:
+                        # df = pd.concat(df, data)
+                        data_frame.merge(right=data)
+                except ImportError:
+                    # Note, when searching for annual reports, this will generally occur 1/4 times
+                    # if we're only searching for one stock's tags
+                    logger.debug(
+                        f"{r} did not have any matches for the provided filter"
+                    )
+                    logger.debug(f"{filter}")
         logger.info(f"Created Unified Data record for these reports: {report_dates}")
-        logger.debug(f"keys: {df.keys()}")
-        logger.debug(f"Rows: {len(df)}")
-        logger.debug(df.head())
-        return df
+        if data_frame is not None:
+            logger.debug(f"keys: {data_frame.keys()}")
+            logger.debug(f"Rows: {len(data_frame)}")
+            logger.debug(data_frame.head())
+        else:
+            raise LookupError("No data matching the filter was retrieved")
+
+        # Now add an index for ticker values to pair with the cik
+        logger.debug(f"filtered_df_before_merge:\n{data_frame.to_csv()}")
+        data_frame = data_frame.reset_index().merge(
+            right=self.download_manager.ticker_reader._data,
+            how="inner",
+            left_on="cik",
+            right_on=["cik_str"],
+        )
+
+        # Columns at this point look like this
+        #  ,adsh,tag,cik,ddate,uom,value,period,fy,fp,cik_str,ticker,title
+        # 0,0000097745-23-000008,EarningsPerShareDiluted,97745,2022-12-31,USD,17.63,2022-12-31,2022.0,FY,97745,TMO,THERMO FISHER SCIENTIFIC INC.
+        # 1,0000097745-23-000008,EarningsPerShareDiluted,97745,2020-12-31,USD,15.96,2022-12-31,2022.0,FY,97745,TMO,THERMO FISHER SCIENTIFIC INC.
+        # 2,0000097745-23-000008,EarningsPerShareDiluted,97745,2021-12-31,USD,19.46,2022-12-31,2022.0,FY,97745,TMO,THERMO FISHER SCIENTIFIC INC..
+
+        data_frame = data_frame.drop(columns=["cik_str", "adsh"]).set_index(
+            ["ticker", "tag", "cik"]
+        )
 
+        logger.debug(f"filtered_df:\n{data_frame.to_csv()}")
+        filter.filtered_data = data_frame
 
+
+@beartype
 class Sec:
     def __init__(self, storage_path: Path):
-        if not isinstance(storage_path, Path):
-            raise ValueError("storage_path is required")
+        """Object for handling requests for information relating to SEC data dumps.
+
+        Args:
+            storage_path (Path): Where to store the results.
+        """
         storage_path.mkdir(parents=True, exist_ok=True)
         data_session = CachedSession(
             "data",
             backend=SQLiteCache(db_path=storage_path / "data"),
             serializer="pickle",
             expire_after=timedelta(days=365 * 5),
             stale_if_error=True,
@@ -480,42 +606,26 @@
             "tickers",
             backend=SQLiteCache(db_path=storage_path / "tickers"),
             expire_after=timedelta(days=365),
             stale_if_error=True,
         )
         self.download_manager = DownloadManager(ticker_session, data_session)
 
-    def getData(self, tickers: list[str], filter: Filter) -> DataSelector:
+    def select_data(self, tickers: frozenset[str], filter: Filter) -> Filter:
         """Initiate the retrieval of ticker information based on the provided filters.
 
+        Filtered data is stored with the filter
+
         Args:
-            tickers (list[str]): ticker symbols you want information about
+            tickers (frozenset[str]): ticker symbols you want information about
             filter (Filter): SEC specific data to scrape from the reports
 
         Returns:
-            DataSelector: Helper for processing the filtered results
+            Filter: filter with filtered data
         """
         collector = DataSetCollector(self.download_manager)
-        ticker_map = self.download_manager.getTickers()
-        filter.populateCikList(tickers=tickers, ticker_reader=ticker_map)
-        filtered_data = collector.getData(filter)
-        return DataSelector(data=filtered_data, ticker_reader=ticker_map)
-
-    # def update(self, tickers: list, years: int = 5, last_report: ReportDate = ReportDate()) -> DataSelector:
-    #     """ Update the database with information about the following stocks.
-
-    #     When this command runs, it will pull updates starting from
-
-    #     Args:
-    #         tickers (list): only store and catalog information about these tickers
-    #         years (int): number of years to go back in time. Defaults to 5.
-    #         last_report (ReportDate): only retrieve reports from this quarter and before
-
-    #     Returns:
-    #         DataSelector: with the extracted data from the report
-    #     """
-    #     # Download reports for each quarter and update records for tickers specified
-    #     download_list = Sec._getDownloadList(years, last_report)
-    #     collector = DataSetCollector(self.download_manager)
-    #     data = collector.getData(download_list)
-    #     ticker_map = self.download_manager.getTickers()
-    #     return DataSelector(data, ticker_map)
+        ticker_reader = self.download_manager.ticker_reader
+        if ticker_reader.contains(tickers):
+            filter.populate_ciks(tickers=tickers, ticker_reader=ticker_reader)
+            collector.get_data(filter)
+
+        return filter
```

### Comparing `stocktracer-0.1.5/src/tests/test_filter.py` & `stocktracer-0.2.0/docs/src/tests/test_filter.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,23 +1,26 @@
 import pytest
 
 import stocktracer.filter as Filter
 from stocktracer.data.sec import Filter as SecFilter
+from stocktracer.data.sec import ReportDate
 
 
 def test_Selectors_init():
     with pytest.raises(TypeError, match="missing 2 required positional arguments"):
         Filter.Selectors()
     with pytest.raises(TypeError, match="missing 1 required positional argument"):
         Filter.Selectors(ticker_filter={"aapl"})
-    with pytest.raises(TypeError, match="missing 1 required positional argument"):
-        Filter.Selectors(ticker_filter={"aapl"}, sec_filter=SecFilter())
+
+    default_selector = Filter.Selectors(ticker_filter={"aapl"}, sec_filter=SecFilter())
+    assert default_selector.sec_filter.last_report is not None
+    assert default_selector.sec_filter.only_annual is True
     selector = Filter.Selectors(
         ticker_filter={"aapl"},
-        sec_filter=SecFilter(tags={"EntityCommonStockSharesOutstanding"}),
+        sec_filter=SecFilter(tags=["EntityCommonStockSharesOutstanding"]),
     )
     assert "aapl" in selector.ticker_filter
     assert "EntityCommonStockSharesOutstanding" in selector.sec_filter.tags
 
     selector = Filter.Selectors(
         ticker_filter=["aapl"],
         sec_filter=SecFilter(tags=["EntityCommonStockSharesOutstanding"]),
```

### Comparing `stocktracer-0.1.5/src/tests/test_sec_network.py` & `stocktracer-0.2.0/docs/src/tests/sec/test_network.py`

 * *Files 24% similar despite different names*

```diff
@@ -4,86 +4,85 @@
 from datetime import date
 from pathlib import Path
 
 import mock
 import pytest
 
 import stocktracer.filter as Filter
-from stocktracer.cli import Cli
-from stocktracer.data.sec import DataSelector, DataSetReader
 from stocktracer.data.sec import Filter as SecFilter
 from stocktracer.data.sec import ReportDate
 from stocktracer.data.sec import Sec
 from stocktracer.data.sec import Sec as SecDataSource
-from stocktracer.data.sec import TickerReader
-from tests.fixtures.network.sec import (
-    filter_aapl,
-    sec_dataselector_2023q1,
-    sec_instance,
-)
+from tests.fixtures.network import filter_aapl, sec_dataselector_2023q1, sec_instance
 
 logger = logging.getLogger(__name__)
 
 
 @pytest.mark.webtest
+class TestTickerReader:
+    def test_contains(self, sec_instance: Sec):
+        ticker_reader = sec_instance.download_manager.ticker_reader
+        assert ticker_reader.contains(frozenset(("aapl", "msft")))
+        with pytest.raises(LookupError, match="unable to find ticker: invalid"):
+            ticker_reader.contains(frozenset(("aapl", "msft", "invalid")))
+
+
+@pytest.mark.webtest
 class TestDownloadManager:
     def test_getTickers(self, sec_instance: Sec):
-        tickers = sec_instance.download_manager.getTickers()
-        assert tickers.getCik("AAPL") == 320193
-        assert tickers.getCik("aapl") == 320193
-        assert tickers.getTicker(320193) == "AAPL"
-
-    def test_benchmark_getTickers(self, sec_instance: Sec, benchmark):
-        benchmark(sec_instance.download_manager.getTickers)
+        ticker_reader = sec_instance.download_manager.ticker_reader
+        assert ticker_reader.convert_to_cik("AAPL") == 320193
+        assert ticker_reader.convert_to_cik("aapl") == 320193
+        assert ticker_reader.convert_to_ticker(320193) == "AAPL"
 
-    def test_getData(self, sec_dataselector_2023q1: Sec):
-        report: DataSelector = sec_dataselector_2023q1
+    def test_getData(self, sec_dataselector_2023q1: Filter.Selectors):
+        report: Filter.Selectors = sec_dataselector_2023q1
 
-        tags = report.getTags()
+        tags = report.sec_filter.tags
         logger.debug(f"tags({len(tags)}): {tags}")
         assert len(tags) > 0
         # TODO: Verify access semantics so we can create a query API on the extracted data
         # aapl =  df[df.adsh == '0000320193-23-000005']
         # assert aapl.empty == False
 
 
 @pytest.mark.webtest
 def test_update(sec_instance: Sec, filter_aapl: Filter.Selectors):
     # pytest.skip(
     #     "skip until we can resolve performance issues with large data sets")
-    data_selector = sec_instance.getData(
-        tickers=["aapl"], filter=filter_aapl.sec_filter
+    sec_instance.select_data(tickers=frozenset(["aapl"]), filter=filter_aapl.sec_filter)
+    assert filter_aapl.sec_filter.filtered_data.empty == False
+    logger.debug(
+        f"There are {len(filter_aapl.sec_filter.filtered_data)} records about apple"
     )
-    assert data_selector.data.empty == False
-    logger.debug(f"There are {len(data_selector.data)} records about apple")
-    logger.debug(data_selector.data)
-    # logger.debug(data_selector.data.to_markdown())
+    logger.debug(filter_aapl.sec_filter.filtered_data)
+    # logger.debug(filter_aapl.sec_filter.filtered_data.to_markdown())
 
     # There should only be one record based on the filter
-    EntityCommonStockSharesOutstanding = data_selector.data.query(
+    EntityCommonStockSharesOutstanding = filter_aapl.sec_filter.filtered_data.query(
         "cik == 320193 and tag == 'EntityCommonStockSharesOutstanding'"
     )
     eo_series = EntityCommonStockSharesOutstanding.value
 
     assert len(eo_series) == 1
     assert eo_series[0] == 15821946000
-    assert True == len(data_selector.data) == 1
+    assert True == len(filter_aapl.sec_filter.filtered_data) == 1
 
 
 @pytest.mark.webtest
 def test_multi_stock_request_over_1year(sec_instance: SecDataSource):
     # Create the filter we'll use to scrape the results
     sec_filter = SecFilter(
         tags=["EarningsPerShareDiluted"],
-        years=1,  # Over the past 5 years
+        years=1,  # Over the past 1 year
         last_report=ReportDate(year=2023, quarter=1),
         only_annual=True,  # We only want the 10-K
     )
-    tickers = ["aapl", "msft", "goog", "tmo"]
-    data_selector = sec_instance.getData(tickers=tickers, filter=sec_filter)
-    logger.debug(data_selector)
+    tickers = frozenset(["aapl", "msft", "goog", "tmo"])
+    sec_instance.select_data(tickers=tickers, filter=sec_filter)
+    logger.debug(sec_filter.filtered_data)
     # Get series for data and make sure they're all yearly-focus(YF)/annual reports
     yearly_focus_periods = "FY"
     quarterly_focus_periods = ("Q1", "Q2", "Q3", "Q4")
-    assert False == data_selector.data.query("fp in @yearly_focus_periods").empty
-    qfp_results = data_selector.data.query("fp in @quarterly_focus_periods")
+    assert False == sec_filter.filtered_data.query("fp in @yearly_focus_periods").empty
+    qfp_results = sec_filter.filtered_data.query("fp in @quarterly_focus_periods")
     assert True == qfp_results.empty
```

### Comparing `stocktracer-0.1.5/.gitignore` & `stocktracer-0.2.0/.gitignore`

 * *Files 1% similar despite different names*

```diff
@@ -130,9 +130,11 @@
 
 # vscode
 .vscode/
 
 # Project
 .edgar-filings/
 *.sqlite3
+*.sqlite
 .ticker-cache
-.ticker-report
+.ticker-report
+.results/
```

### Comparing `stocktracer-0.1.5/LICENSE` & `stocktracer-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `stocktracer-0.1.5/pyproject.toml` & `stocktracer-0.2.0/pyproject.toml`

 * *Files 17% similar despite different names*

```diff
@@ -4,30 +4,31 @@
 
 [tool.hatch.build.targets.wheel]
 only-include = ["src/stocktracer"]
 sources = ["src"]
 
 [project]
 name = "stocktracer"
-version = "0.1.5"
+version = "0.2.0"
 authors = [
   { name="Gary Yund", email="gary.yund@gmail.com" },
 ]
-description = "Tools for aggregating efficient ways to consume and process publically traded equities on the US stock market. Includes caching SEC data dump processing."
+description = "Tools for aggregating efficient ways to consume and process publically traded equities on the US stock market. Includes support for SEC quarterly data processing."
 readme = "README.md"
 requires-python = ">=3.10"
 license = {file = "LICENSE"}
 keywords = [ "sec-tools", "fundamental analysis", "stocks" ]
 classifiers = [
     "License :: OSI Approved :: Eclipse Public License 2.0 (EPL-2.0)",
     "Operating System :: OS Independent",
     "Topic :: Scientific/Engineering :: Information Analysis",
     "Topic :: Office/Business :: Financial :: Investment",
     "Intended Audience :: Science/Research",
     "Development Status :: 2 - Pre-Alpha",
+    "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11"
 ]
 
 dynamic = ["dependencies"]
 
 [tool.hatch.metadata.hooks.requirements_txt]
@@ -39,15 +40,15 @@
 
 [project.scripts]
 stocktracer = "stocktracer.__main__:main_cli"
 
 [tool.pytest.ini_options]
 # log_cli = true
 log_cli_level = "INFO"
-log_cli_format = "%(asctime)s [%(levelname)8s] %(message)s (%(filename)s:%(lineno)s)"
+log_cli_format = "%(asctime)s [%(levelname)8s] %(message)s (%(pathname)s:%(lineno)s)"
 log_cli_date_format = "%Y-%m-%d %H:%M:%S"
 testpaths = [
     "src/",
 ]
 # addopts = [
 #     "--import-mode=importlib",
 # ]
@@ -90,8 +91,42 @@
     "def __repr__",
     "if self.debug:",
     "if settings.DEBUG",
     "raise AssertionError",
     "raise NotImplementedError",
     "if 0:",
     "if __name__ == .__main__.:"
-    ]
+    ]
+
+[tool.pydocstyle]
+inherit = false
+match = '(?!(test_|conftest)).*\.py'
+match_dir = '^(?!(venv|tests|poc)).*'
+convention = "pep257"
+ignore_self_only_init = true
+
+[tool.pylint.main]
+source-roots = ["src"]
+fail-under = 9
+fail-on = [
+    # "redefined-builtin",    # unintended sideaffects
+    "unused-variable",      # cleaner code
+    "unused-import",        # cleaner code
+    "no-self-argument",     # possible bug, annotate correctly
+    "use-list-literal",     # cleaner code
+    "no-else-return",       # cleaner code
+    "no-member",            # make explicit for clarity 
+    # "invalid-name",         # consistency
+    ]
+
+[tool.pylint."messages control"]
+
+logging-format-style = "new"
+disable = ["line-too-long", "logging-fstring-interpolation", "too-few-public-methods"]
+# disable=["W1203"]
+# disable=["all"]
+
+[tool.pylint.format]
+max-line-length = "88"
+
+[tool.pylint.reports]
+output-format = ["colorized"]
```

### Comparing `stocktracer-0.1.5/PKG-INFO` & `stocktracer-0.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: stocktracer
-Version: 0.1.5
-Summary: Tools for aggregating efficient ways to consume and process publically traded equities on the US stock market. Includes caching SEC data dump processing.
+Version: 0.2.0
+Summary: Tools for aggregating efficient ways to consume and process publically traded equities on the US stock market. Includes support for SEC quarterly data processing.
 Project-URL: Homepage, https://gyund.github.io/fundamental-analysis/
 Project-URL: Bug Tracker, https://github.com/gyund/fundamental-analysis/issues
 Author-email: Gary Yund <gary.yund@gmail.com>
 License: Eclipse Public License - v 2.0
         
             THE ACCOMPANYING PROGRAM IS PROVIDED UNDER THE TERMS OF THIS ECLIPSE
             PUBLIC LICENSE ("AGREEMENT"). ANY USE, REPRODUCTION OR DISTRIBUTION
@@ -284,47 +284,53 @@
           You may add additional accurate notices of copyright ownership.
 License-File: LICENSE
 Keywords: fundamental analysis,sec-tools,stocks
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: Eclipse Public License 2.0 (EPL-2.0)
 Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Office/Business :: Financial :: Investment
 Classifier: Topic :: Scientific/Engineering :: Information Analysis
 Requires-Python: >=3.10
 Requires-Dist: attrs==23.1.0; python_version >= '3.7'
+Requires-Dist: beartype==0.14.0
 Requires-Dist: cattrs==22.2.0; python_version >= '3.7'
-Requires-Dist: certifi==2022.12.7; python_version >= '3.6'
+Requires-Dist: certifi==2023.5.7; python_version >= '3.6'
 Requires-Dist: charset-normalizer==3.1.0; python_full_version >= '3.7.0'
+Requires-Dist: diskcache==5.6.1
 Requires-Dist: exceptiongroup==1.1.1; python_version < '3.11'
 Requires-Dist: fire==0.5.0
 Requires-Dist: idna==3.4; python_version >= '3.5'
 Requires-Dist: numpy==1.24.3; python_version >= '3.10'
 Requires-Dist: pandas==2.0.1
-Requires-Dist: platformdirs==3.5.0; python_version >= '3.7'
+Requires-Dist: platformdirs==3.5.1; python_version >= '3.7'
 Requires-Dist: python-dateutil==2.8.2
 Requires-Dist: pytz==2023.3
 Requires-Dist: requests-cache==1.0.1
-Requires-Dist: requests==2.29.0
+Requires-Dist: requests==2.30.0
 Requires-Dist: six==1.16.0; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'
 Requires-Dist: tabulate==0.9.0
 Requires-Dist: termcolor==2.3.0; python_version >= '3.7'
 Requires-Dist: tzdata==2023.3; python_version >= '2'
 Requires-Dist: url-normalize==1.4.3; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'
-Requires-Dist: urllib3==1.26.15; python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5'
+Requires-Dist: urllib3==2.0.2; python_version >= '3.7'
 Description-Content-Type: text/markdown
 
 <p align="center">
     <a href='https://github.com/gyund/fundamental-analysis/blob/main/LICENSE'><img alt="License" src="https://img.shields.io/github/license/gyund/fundamental-analysis"></a>
-    <img alt="License" src="https://img.shields.io/badge/python-3.10%2B-blue">
+    <img alt="PyPI - Python Version" src="https://img.shields.io/pypi/pyversions/stocktracer">
     <a href='https://github.com/gyund/fundamental-analysis/actions/workflows/python.yml'><img alt="Test Status" src="https://github.com/gyund/fundamental-analysis/actions/workflows/python.yml/badge.svg?service=github"></a>
-    <a href='https://coveralls.io/github/gyund/fundamental-analysis?branch=main'><img src='https://coveralls.io/repos/github/gyund/fundamental-analysis/badge.svg?branch=main&service=github' alt='Coverage Status' /></a>
-    <img alt="PyPI - Status" src="https://img.shields.io/pypi/status/stocktracer?">
+    <a href='https://coveralls.io/github/gyund/fundamental-analysis?branch=main'><img src='https://coveralls.io/repos/github/gyund/fundamental-analysis/badge.svg' alt='Coverage Status' /></a>
+    <a href="https://beartype.readthedocs.io"><img src="https://raw.githubusercontent.com/beartype/beartype-assets/main/badge/bear-ified.svg?" alt="bear-ified"></a>
+    <a href="https://github.com/psf/black"><img src="https://img.shields.io/badge/code%20style-black-000000.svg" alt="Code style: black"></a>
+    <img alt="PyPI - Downloads" src="https://img.shields.io/pypi/dm/stocktracer">
+    <img alt="PyPI - Status" src="https://img.shields.io/pypi/status/stocktracer">
 </p>
 
 # StockTracer
 
 **Stock Analysis Framework**
 
 The goal of this project is aggregate a variety of ways to consume information about a particular equity traded on the US stock market and provide a modular mechanism to process it. Core tenants of this project include:
@@ -351,21 +357,24 @@
 # Help
 stocktracer
 
 ```
 
 ### Developers
 
-Make sure you have `pipenv` installed through a package manager or through pip. You may also use the generated `requirements.txt` but note that these are generated using `pipenv` when we make changes to to dependencies.
+Make sure you have `pipenv` installed through a package manager or through pip.
 
 ```sh
 pipenv install --dev
 
 # Perform analysis (not supported yet)
 PYTHONPATH=src pipenv run python -m stocktracer analyze --tickers aapl,msft
+PYTHONPATH=src pipenv run python -m stocktracer analyze --tickers aapl,msft -a stocktracer.analysis.diluted_eps
+PYTHONPATH=src pipenv run python -m stocktracer analyze --tickers aapl,msft -a stocktracer.analysis.diluted_eps --report-format csv
+PYTHONPATH=src pipenv run python -m stocktracer analyze --tickers aapl,msft -a stocktracer.analysis.diluted_eps --report-format json --report-file my_results.json
 
 # Help
 PYTHONPATH=src pipenv run python -m stocktracer
 
 # Run Unit Tests
 pipenv run pytest
 ```
```

