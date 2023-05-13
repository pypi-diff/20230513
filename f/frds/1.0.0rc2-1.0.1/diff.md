# Comparing `tmp/frds-1.0.0rc2.tar.gz` & `tmp/frds-1.0.1.tar.gz`

## Comparing `frds-1.0.0rc2.tar` & `frds-1.0.1.tar`

### file list

```diff
@@ -1,38 +1,41 @@
--rw-r--r--   0        0        0      310 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.pylintrc
--rw-r--r--   0        0        0     3399 2020-02-02 00:00:00.000000 frds-1.0.0rc2/mkdocs.yml
--rw-r--r--   0        0        0       64 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/FUNDING.yml
--rw-r--r--   0        0        0      594 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0        0        0      857 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/build-and-deploy-docs.yml
--rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/publish-to-test-pypi.yml
--rw-r--r--   0        0        0      606 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.github/workflows/test.yml
--rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/CNAME
--rw-r--r--   0        0        0     3952 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/index.md
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures.md
--rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_icon.png
--rw-r--r--   0        0        0    58143 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_icon_white.png
--rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/images/frds_logo.png
--rw-r--r--   0        0        0     2310 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/absorption_ratio.md
--rw-r--r--   0        0        0     1280 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/contingent_claim_analysis.md
--rw-r--r--   0        0        0     2166 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/distress_insurance_premium.md
--rw-r--r--   0        0        0     1521 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/marginal_expected_shortfall.md
--rw-r--r--   0        0        0     3743 2020-02-02 00:00:00.000000 frds-1.0.0rc2/docs/measures/systemic_expected_shortfall.md
--rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.0rc2/images/frds_icon.png
--rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.0rc2/images/frds_logo.png
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/__init__.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/__init__.py
--rw-r--r--   0        0        0     1412 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/absorption_ratio.py
--rw-r--r--   0        0        0     3102 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/contingent_claims_analysis.py
--rw-r--r--   0        0        0     4538 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/distress_insurance_premium.py
--rw-r--r--   0        0        0     1231 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/marginal_expected_shortfall.py
--rw-r--r--   0        0        0     1809 2020-02-02 00:00:00.000000 frds-1.0.0rc2/src/frds/measures/systemic_expected_shortfall.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/__init__.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/__init__.py
--rw-r--r--   0        0        0     2367 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_absorption_ratio.py
--rw-r--r--   0        0        0     1036 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_distress_insurance_premium.py
--rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_marginal_expected_shortfall.py
--rw-r--r--   0        0        0      789 2020-02-02 00:00:00.000000 frds-1.0.0rc2/tests/measures/test_systemic_expected_shortfall.py
--rw-r--r--   0        0        0     1819 2020-02-02 00:00:00.000000 frds-1.0.0rc2/.gitignore
--rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 frds-1.0.0rc2/LICENSE
--rw-r--r--   0        0        0     2958 2020-02-02 00:00:00.000000 frds-1.0.0rc2/README.md
--rw-r--r--   0        0        0      916 2020-02-02 00:00:00.000000 frds-1.0.0rc2/pyproject.toml
--rw-r--r--   0        0        0     3846 2020-02-02 00:00:00.000000 frds-1.0.0rc2/PKG-INFO
+-rw-r--r--   0        0        0      310 2020-02-02 00:00:00.000000 frds-1.0.1/.pylintrc
+-rw-r--r--   0        0        0     3440 2020-02-02 00:00:00.000000 frds-1.0.1/mkdocs.yml
+-rw-r--r--   0        0        0       64 2020-02-02 00:00:00.000000 frds-1.0.1/.github/FUNDING.yml
+-rw-r--r--   0        0        0      594 2020-02-02 00:00:00.000000 frds-1.0.1/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      857 2020-02-02 00:00:00.000000 frds-1.0.1/.github/workflows/build-and-deploy-docs.yml
+-rw-r--r--   0        0        0     1341 2020-02-02 00:00:00.000000 frds-1.0.1/.github/workflows/publish.yml
+-rw-r--r--   0        0        0      606 2020-02-02 00:00:00.000000 frds-1.0.1/.github/workflows/test.yml
+-rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 frds-1.0.1/docs/CNAME
+-rw-r--r--   0        0        0     3952 2020-02-02 00:00:00.000000 frds-1.0.1/docs/index.md
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures.md
+-rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.1/docs/images/frds_icon.png
+-rw-r--r--   0        0        0    58143 2020-02-02 00:00:00.000000 frds-1.0.1/docs/images/frds_icon_white.png
+-rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.1/docs/images/frds_logo.png
+-rw-r--r--   0        0        0     2310 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/absorption_ratio.md
+-rw-r--r--   0        0        0     1280 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/contingent_claim_analysis.md
+-rw-r--r--   0        0        0     2166 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/distress_insurance_premium.md
+-rw-r--r--   0        0        0     1521 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/marginal_expected_shortfall.md
+-rw-r--r--   0        0        0     3743 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/systemic_expected_shortfall.md
+-rw-r--r--   0        0        0     2104 2020-02-02 00:00:00.000000 frds-1.0.1/docs/measures/z_score.md
+-rw-r--r--   0        0        0   143526 2020-02-02 00:00:00.000000 frds-1.0.1/images/frds_icon.png
+-rw-r--r--   0        0        0   132433 2020-02-02 00:00:00.000000 frds-1.0.1/images/frds_logo.png
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/__init__.py
+-rw-r--r--   0        0        0     1412 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/absorption_ratio.py
+-rw-r--r--   0        0        0     3102 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/contingent_claims_analysis.py
+-rw-r--r--   0        0        0     4538 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/distress_insurance_premium.py
+-rw-r--r--   0        0        0     1231 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/marginal_expected_shortfall.py
+-rw-r--r--   0        0        0     1809 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/systemic_expected_shortfall.py
+-rw-r--r--   0        0        0      708 2020-02-02 00:00:00.000000 frds-1.0.1/src/frds/measures/z_score.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.1/tests/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/__init__.py
+-rw-r--r--   0        0        0     2367 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/test_absorption_ratio.py
+-rw-r--r--   0        0        0     1036 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/test_distress_insurance_premium.py
+-rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/test_marginal_expected_shortfall.py
+-rw-r--r--   0        0        0      789 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/test_systemic_expected_shortfall.py
+-rw-r--r--   0        0        0      263 2020-02-02 00:00:00.000000 frds-1.0.1/tests/measures/test_z_score.py
+-rw-r--r--   0        0        0     1819 2020-02-02 00:00:00.000000 frds-1.0.1/.gitignore
+-rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 frds-1.0.1/LICENSE
+-rw-r--r--   0        0        0     2958 2020-02-02 00:00:00.000000 frds-1.0.1/README.md
+-rw-r--r--   0        0        0      913 2020-02-02 00:00:00.000000 frds-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     3843 2020-02-02 00:00:00.000000 frds-1.0.1/PKG-INFO
```

### Comparing `frds-1.0.0rc2/mkdocs.yml` & `frds-1.0.1/mkdocs.yml`

 * *Files 2% similar despite different names*

```diff
@@ -125,9 +125,10 @@
       - measures.md
       - Banking:
           - Absoprtion ratio: measures/absorption_ratio.md
           - Contingent claim analysis: measures/contingent_claim_analysis.md
           - Distress insurance premium: measures/distress_insurance_premium.md
           - Marginal expected shortfall: measures/marginal_expected_shortfall.md
           - Systemic expected shortfall: measures/systemic_expected_shortfall.md
+          - Z-score: measures/z_score.md
   - Author Site: https://mingze-gao.com
```

### Comparing `frds-1.0.0rc2/.github/ISSUE_TEMPLATE/bug_report.md` & `frds-1.0.1/.github/ISSUE_TEMPLATE/bug_report.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/.github/workflows/build-and-deploy-docs.yml` & `frds-1.0.1/.github/workflows/build-and-deploy-docs.yml`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/.github/workflows/publish-to-test-pypi.yml` & `frds-1.0.1/.github/workflows/publish.yml`

 * *Files 24% similar despite different names*

```diff
@@ -1,23 +1,34 @@
-name: Publish Python 🐍 distributions 📦 to PyPI and TestPyPI
+name: Publish Python
 
 on: 
   push:
     tags:
       - "v*" # Push events to matching v*, i.e. v1.0, v20.15.10
 jobs:
   build-n-publish:
-    name: Build and publish Python 🐍 distributions 📦 to PyPI and TestPyPI
+    name: Build and publish
     runs-on: ubuntu-latest
     steps:
     - uses: actions/checkout@v3
     - name: Set up Python
       uses: actions/setup-python@v4
       with:
         python-version: "3.x"
+         
+    - name: Create Release
+      id: create_release
+      uses: actions/create-release@v1
+      env:
+        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
+      with:
+        tag_name: ${{ github.ref }}
+        release_name: Release ${{ github.ref }}
+        draft: false
+        prerelease: false
     - name: Install pypa/build
       run: >-
         python -m
         pip install
         build
         --user
     - name: Build a binary wheel and a source tarball
@@ -33,8 +44,8 @@
       with:
         password: ${{ secrets.TEST_PYPI_API_TOKEN }}
         repository-url: https://test.pypi.org/legacy/
     - name: Publish distribution 📦 to PyPI
       if: startsWith(github.ref, 'refs/tags')
       uses: pypa/gh-action-pypi-publish@release/v1
       with:
-        password: ${{ secrets.PYPI_API_TOKEN }}
+        password: ${{ secrets.PYPI_API_TOKEN }}
```

### Comparing `frds-1.0.0rc2/.github/workflows/test.yml` & `frds-1.0.1/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/index.md` & `frds-1.0.1/docs/index.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/images/frds_icon.png` & `frds-1.0.1/docs/images/frds_icon.png`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/images/frds_icon_white.png` & `frds-1.0.1/docs/images/frds_icon_white.png`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/images/frds_logo.png` & `frds-1.0.1/docs/images/frds_logo.png`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/measures/absorption_ratio.md` & `frds-1.0.1/docs/measures/absorption_ratio.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/measures/contingent_claim_analysis.md` & `frds-1.0.1/docs/measures/contingent_claim_analysis.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/measures/distress_insurance_premium.md` & `frds-1.0.1/docs/measures/distress_insurance_premium.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/measures/marginal_expected_shortfall.md` & `frds-1.0.1/docs/measures/marginal_expected_shortfall.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/docs/measures/systemic_expected_shortfall.md` & `frds-1.0.1/docs/measures/systemic_expected_shortfall.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/images/frds_icon.png` & `frds-1.0.1/images/frds_icon.png`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/images/frds_logo.png` & `frds-1.0.1/images/frds_logo.png`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/src/frds/measures/absorption_ratio.py` & `frds-1.0.1/src/frds/measures/absorption_ratio.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/src/frds/measures/contingent_claims_analysis.py` & `frds-1.0.1/src/frds/measures/contingent_claims_analysis.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/src/frds/measures/distress_insurance_premium.py` & `frds-1.0.1/src/frds/measures/distress_insurance_premium.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/src/frds/measures/marginal_expected_shortfall.py` & `frds-1.0.1/src/frds/measures/marginal_expected_shortfall.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/src/frds/measures/systemic_expected_shortfall.py` & `frds-1.0.1/src/frds/measures/systemic_expected_shortfall.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/tests/measures/test_absorption_ratio.py` & `frds-1.0.1/tests/measures/test_absorption_ratio.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/tests/measures/test_distress_insurance_premium.py` & `frds-1.0.1/tests/measures/test_distress_insurance_premium.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/tests/measures/test_marginal_expected_shortfall.py` & `frds-1.0.1/tests/measures/test_marginal_expected_shortfall.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/tests/measures/test_systemic_expected_shortfall.py` & `frds-1.0.1/tests/measures/test_systemic_expected_shortfall.py`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/.gitignore` & `frds-1.0.1/.gitignore`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/LICENSE` & `frds-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/README.md` & `frds-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `frds-1.0.0rc2/pyproject.toml` & `frds-1.0.1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "frds"
-version = "1.0.0rc2"
+version = "1.0.1"
 authors = [
   { name="Mingze Gao", email="adrian.gao@outlook.com" },
 ]
 description = "Financial Research Data Services"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `frds-1.0.0rc2/PKG-INFO` & `frds-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: frds
-Version: 1.0.0rc2
+Version: 1.0.1
 Summary: Financial Research Data Services
 Project-URL: homepage, https://github.com/mgao6767/frds
 Project-URL: documentation, https://frds.io
 Author-email: Mingze Gao <adrian.gao@outlook.com>
 License: MIT License
 License-File: LICENSE
 Classifier: Intended Audience :: Education
```

