# Comparing `tmp/atenpdu-0.6.0.tar.gz` & `tmp/atenpdu-0.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "atenpdu-0.6.0.tar", max compression
+gzip compressed data, was "atenpdu-0.6.1.tar", max compression
```

## Comparing `atenpdu-0.6.0.tar` & `atenpdu-0.6.1.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     1062 2022-12-19 14:13:25.197000 atenpdu-0.6.0/LICENSE
--rw-r--r--   0        0        0     1095 2022-12-19 15:24:35.982000 atenpdu-0.6.0/README.md
--rw-r--r--   0        0        0     6672 2023-04-21 20:13:52.937060 atenpdu-0.6.0/atenpdu/__init__.py
--rw-r--r--   0        0        0   102790 2022-12-19 15:04:28.586000 atenpdu-0.6.0/atenpdu/mibs/ATEN-PE-CFG.py
--rwxr-xr-x   0        0        0     6343 2022-12-19 15:16:22.450000 atenpdu-0.6.0/atenpdu/pductl.py
--rw-r--r--   0        0        0     1045 2023-04-21 20:15:13.975062 atenpdu-0.6.0/pyproject.toml
--rw-r--r--   0        0        0     1952 1970-01-01 00:00:00.000000 atenpdu-0.6.0/setup.py
--rw-r--r--   0        0        0     2150 1970-01-01 00:00:00.000000 atenpdu-0.6.0/PKG-INFO
+-rw-r--r--   0        0        0     1062 2022-12-19 14:13:25.197000 atenpdu-0.6.1/LICENSE
+-rw-r--r--   0        0        0     1095 2022-12-19 15:24:35.982000 atenpdu-0.6.1/README.md
+-rw-r--r--   0        0        0     6666 2023-05-13 13:04:03.617000 atenpdu-0.6.1/atenpdu/__init__.py
+-rw-r--r--   0        0        0   102790 2022-12-19 15:04:28.586000 atenpdu-0.6.1/atenpdu/mibs/ATEN-PE-CFG.py
+-rwxr-xr-x   0        0        0     6343 2022-12-19 15:16:22.450000 atenpdu-0.6.1/atenpdu/pductl.py
+-rw-r--r--   0        0        0     1045 2023-05-13 13:07:37.089000 atenpdu-0.6.1/pyproject.toml
+-rw-r--r--   0        0        0     1952 1970-01-01 00:00:00.000000 atenpdu-0.6.1/setup.py
+-rw-r--r--   0        0        0     2150 1970-01-01 00:00:00.000000 atenpdu-0.6.1/PKG-INFO
```

### Comparing `atenpdu-0.6.0/LICENSE` & `atenpdu-0.6.1/LICENSE`

 * *Files identical despite different names*

### Comparing `atenpdu-0.6.0/README.md` & `atenpdu-0.6.1/README.md`

 * *Files identical despite different names*

### Comparing `atenpdu-0.6.0/atenpdu/__init__.py` & `atenpdu-0.6.1/atenpdu/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -101,15 +101,15 @@
                         set_result = await setCmd(
                             *self._snmp_args,
                             *[
                                 ObjectType(ObjectIdentity(self._MIB_MODULE, obj, *args), value)
                                 for obj, value in objects_values.items()
                             ],
                         )
-                        err_indication, err_status, _, _ = await set_result
+                        err_indication, err_status, _, _ = set_result
                 except asyncio.exceptions.TimeoutError:
                     pass
                 else:
                     break
             else:
                 raise AtenPEError("Timeout")
```

### Comparing `atenpdu-0.6.0/atenpdu/mibs/ATEN-PE-CFG.py` & `atenpdu-0.6.1/atenpdu/mibs/ATEN-PE-CFG.py`

 * *Files identical despite different names*

### Comparing `atenpdu-0.6.0/atenpdu/pductl.py` & `atenpdu-0.6.1/atenpdu/pductl.py`

 * *Files identical despite different names*

### Comparing `atenpdu-0.6.0/pyproject.toml` & `atenpdu-0.6.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 target-version = ['py38']
 
 [tool.isort]
 profile = "black"
 
 [tool.poetry]
 name = "atenpdu"
-version = "0.6.0"
+version = "0.6.1"
 description = "Interface for ATEN-PE PDUs"
 authors = ["Andreas Oberritter <obi@saftware.de>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/mtdcr/pductl"
 classifiers = [
     "Development Status :: 4 - Beta",
```

### Comparing `atenpdu-0.6.0/setup.py` & `atenpdu-0.6.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 ['async-timeout>=4.0.2,<5.0.0', 'pysnmplib>=5.0.21,<6.0.0']
 
 entry_points = \
 {'console_scripts': ['pductl = atenpdu.pductl:run']}
 
 setup_kwargs = {
     'name': 'atenpdu',
-    'version': '0.6.0',
+    'version': '0.6.1',
     'description': 'Interface for ATEN-PE PDUs',
     'long_description': '# pductl - Control outlets of ATEN PE PDUs\n\n## Installation\n\n```sh\npip install atenpdu\n```\n \n## Example configuration [~/.pductl]\n```json\n{\n  "format": 1,\n  "pdus": {\n    "pdu1": {\n      "node": "pdu1",\n      "service": "snmp",\n      "username": "administrator",\n      "authkey": "AAAAAAAAAAAAAA",\n      "privkey": "BBBBBBBBBBBBBB"\n    },\n    "pdu2": {\n      "authkey": "CCCCCCCCCCCCCC",\n      "privkey": "DDDDDDDDDDDDDD"\n    },\n    "pdu3": {\n      "node": "192.168.21.19",\n      "service": "16161",\n      "username": "joe",\n      "authkey": "EEEEEEEEEEEEEE",\n      "privkey": "FFFFFFFFFFFFFF"\n    },\n    "pdu4": {\n      "community": "private"\n    },\n    "pdu5": {\n    }\n  }\n}\n```\n\n* `authkey` and `privkey` are required for SNMPv3. On absence, SNMPv2c gets used.\n* `community` defaults to `private` for SNMPv2c.\n* `node` defaults to PDU entry\'s name.\n* `service` defaults to `snmp`, i.e. port 161.\n* `username` defaults to `administrator` for SNMPv3.\n\n## Usage\n\n```sh\npductl [-p <PDU>] list\npductl [-p <PDU>] <on|off|reboot|status> <OUTLET> [<OUTLET> ...]\n```\n\nUse `ALL` to select all outlets.\n',
     'author': 'Andreas Oberritter',
     'author_email': 'obi@saftware.de',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/mtdcr/pductl',
```

### Comparing `atenpdu-0.6.0/PKG-INFO` & `atenpdu-0.6.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: atenpdu
-Version: 0.6.0
+Version: 0.6.1
 Summary: Interface for ATEN-PE PDUs
 Home-page: https://github.com/mtdcr/pductl
 License: MIT
 Author: Andreas Oberritter
 Author-email: obi@saftware.de
 Requires-Python: >=3.8.1,<4.0.0
 Classifier: Development Status :: 4 - Beta
```

