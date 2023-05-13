# Comparing `tmp/hypebankapi-1.0.1.tar.gz` & `tmp/hypebankapi-1.0.2.tar.gz`

## Comparing `hypebankapi-1.0.1.tar` & `hypebankapi-1.0.2.tar`

### file list

```diff
@@ -1,14 +1,15 @@
--rw-r--r--   0        0        0      704 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/CODE_OF_CONDUCT.md
--rw-r--r--   0        0        0      675 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/CONTRIBUTING.md
--rw-r--r--   0        0        0       14 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/requirements.txt
--rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/.github/workflows/python-publish.yml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/src/hypebankapi/__init__.py
--rw-r--r--   0        0        0     2848 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/src/hypebankapi/banking.py
--rw-r--r--   0        0        0     6639 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/src/hypebankapi/hype.py
--rw-r--r--   0        0        0     1656 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/src/hypebankapi/main.py
--rw-r--r--   0        0        0     1012 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/src/hypebankapi/utils.py
--rw-r--r--   0        0        0     1849 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/.gitignore
--rw-r--r--   0        0        0    11341 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/LICENSE
--rw-r--r--   0        0        0     1597 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/README.md
--rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/pyproject.toml
--rw-r--r--   0        0        0     2277 2020-02-02 00:00:00.000000 hypebankapi-1.0.1/PKG-INFO
+-rw-r--r--   0        0        0      704 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/CODE_OF_CONDUCT.md
+-rw-r--r--   0        0        0      675 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/CONTRIBUTING.md
+-rw-r--r--   0        0        0       14 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/requirements.txt
+-rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/.github/workflows/python-publish.yml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/__init__.py
+-rw-r--r--   0        0        0     1690 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/__main__.py
+-rw-r--r--   0        0        0     2848 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/banking.py
+-rw-r--r--   0        0        0     6639 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/hype.py
+-rw-r--r--   0        0        0     1655 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/main.py
+-rw-r--r--   0        0        0     1012 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/src/hypebankapi/utils.py
+-rw-r--r--   0        0        0     1849 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/.gitignore
+-rw-r--r--   0        0        0    11341 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/LICENSE
+-rw-r--r--   0        0        0     1659 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/README.md
+-rw-r--r--   0        0        0      718 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/pyproject.toml
+-rw-r--r--   0        0        0     2324 2020-02-02 00:00:00.000000 hypebankapi-1.0.2/PKG-INFO
```

### Comparing `hypebankapi-1.0.1/CODE_OF_CONDUCT.md` & `hypebankapi-1.0.2/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/CONTRIBUTING.md` & `hypebankapi-1.0.2/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/.github/workflows/python-publish.yml` & `hypebankapi-1.0.2/.github/workflows/python-publish.yml`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
     runs-on: ubuntu-latest
 
     steps:
     - uses: actions/checkout@v3
     - name: Set up Python
       uses: actions/setup-python@v3
       with:
-        python-version: '3.x'
+        python-version: '3.8'
     - name: Install dependencies
       run: |
         python -m pip install --upgrade pip
         pip install build
     - name: Build package
       run: python -m build
     - name: Publish package
```

### Comparing `hypebankapi-1.0.1/src/hypebankapi/banking.py` & `hypebankapi-1.0.2/src/hypebankapi/banking.py`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/src/hypebankapi/hype.py` & `hypebankapi-1.0.2/src/hypebankapi/hype.py`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/src/hypebankapi/main.py` & `hypebankapi-1.0.2/src/hypebankapi/main.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 import argparse
-
-import banking
-from hype import Hype
 from getpass import getpass  # For interactive password input
-from utils import save_json
+
+from .banking import Banking
+from .hype import Hype
+from .utils import save_json
+
 
 if __name__ == "__main__":
     parser = argparse.ArgumentParser(
         prog="HypeAPI",
         description='Fetch data from Hype API and create JSON folder with profile, balance, card and movements information'
     )
     parser.add_argument('-m', '--email', help='Email address', required=True, type=str)
@@ -20,26 +21,26 @@
 
     h = Hype()
     h.login(args.email, password, args.birthdate)
     if args.verbose:
         print('Logged in. Waiting for OTP code...\n')
 
     # Wait for OTP code to arrive via SMS
-    h.otp2fa(int(input("OTP code: ")))
+    h.otp2fa(input("OTP code: "))
 
     # You are now logged in
     try:
         profile = h.get_profile()
         balance = h.get_balance()
         card = h.get_card()
-        movements = h.get_movements(limit=int(args.limit))
+        movements = h.get_movements(limit=args.limit)
 
         save_json(profile, 'profile.json')
         save_json(balance, 'balance.json')
         save_json(card, 'card.json')
         save_json(movements, 'movements.json')
         if args.verbose:
             print('JSON folder created!')
-    except banking.Banking.AuthenticationFailure:
+    except Banking.AuthenticationFailure:
         # Token has expired
         h.renew()
         print('Renew Token')
```

### Comparing `hypebankapi-1.0.1/src/hypebankapi/utils.py` & `hypebankapi-1.0.2/src/hypebankapi/utils.py`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/.gitignore` & `hypebankapi-1.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/LICENSE` & `hypebankapi-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `hypebankapi-1.0.1/README.md` & `hypebankapi-1.0.2/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,25 +1,30 @@
 # 🌟 HypeAPI
 
 Unofficial Python module for interacting with the HYPE card API.
 
 ## 📝 Notes
 - HYPE only allows the use of one device at a time. Logging in with this module will disconnect you from the application and vice versa.
 
+## Pypi
+```python
+pip install -U HypeBankAPI
+```
+
 ## 🚀 Usage
 ```python
 from hypebankapi import Hype, utils
 from getpass import getpass
 
 h = Hype()
-h.login(EMAIL, getpass(), BIRTH-DATE) # Change EMAIL and BIRTH-DATE
+h.login(EMAIL, getpass('Hype password: '), BIRTH-DATE) # Change EMAIL and BIRTH-DATE
 
 # Wait for OTP code to arrive via SMS
 
-h.otp2fa(int(input("OTP: ")))
+h.otp2fa(input("OTP: "))
 
 profile = h.get_profile()
 balance = h.get_balance()
 card = h.get_card()
 movements = h.get_movements(limit=50) # change the limit of transactions fetched
 
 utils.save_json(profile, 'profile.json')
```

### Comparing `hypebankapi-1.0.1/pyproject.toml` & `hypebankapi-1.0.2/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "HypeBankAPI"
-version = "1.0.1"
+version = "1.0.2"
 authors = [
   { name="Matteo Fasulo", email="mat.fasulo@gmail.com" },
 ]
 description = "API for Hype card holders"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.8",
     "Natural Language :: English",
     "License :: OSI Approved :: Apache Software License",
     "Operating System :: OS Independent",
 ]
 dependencies = [
-    "lxml ~=4.9.2",
-    "requests ~=2.30.0",
+    "lxml",
+    "requests",
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/MatteoFasulo/HypeAPI/tree/pypi"
 "Bug Tracker" = "https://github.com/MatteoFasulo/HypeAPI/issues"
```

### Comparing `hypebankapi-1.0.1/PKG-INFO` & `hypebankapi-1.0.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,43 +1,48 @@
 Metadata-Version: 2.1
 Name: HypeBankAPI
-Version: 1.0.1
+Version: 1.0.2
 Summary: API for Hype card holders
 Project-URL: Homepage, https://github.com/MatteoFasulo/HypeAPI/tree/pypi
 Project-URL: Bug Tracker, https://github.com/MatteoFasulo/HypeAPI/issues
 Author-email: Matteo Fasulo <mat.fasulo@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.7
-Requires-Dist: lxml~=4.9.2
-Requires-Dist: requests~=2.30.0
+Requires-Dist: lxml
+Requires-Dist: requests
 Description-Content-Type: text/markdown
 
 # 🌟 HypeAPI
 
 Unofficial Python module for interacting with the HYPE card API.
 
 ## 📝 Notes
 - HYPE only allows the use of one device at a time. Logging in with this module will disconnect you from the application and vice versa.
 
+## Pypi
+```python
+pip install -U HypeBankAPI
+```
+
 ## 🚀 Usage
 ```python
 from hypebankapi import Hype, utils
 from getpass import getpass
 
 h = Hype()
-h.login(EMAIL, getpass(), BIRTH-DATE) # Change EMAIL and BIRTH-DATE
+h.login(EMAIL, getpass('Hype password: '), BIRTH-DATE) # Change EMAIL and BIRTH-DATE
 
 # Wait for OTP code to arrive via SMS
 
-h.otp2fa(int(input("OTP: ")))
+h.otp2fa(input("OTP: "))
 
 profile = h.get_profile()
 balance = h.get_balance()
 card = h.get_card()
 movements = h.get_movements(limit=50) # change the limit of transactions fetched
 
 utils.save_json(profile, 'profile.json')
```

