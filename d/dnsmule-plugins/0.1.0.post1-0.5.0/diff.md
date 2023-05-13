# Comparing `tmp/dnsmule-plugins-0.1.0.post1.tar.gz` & `tmp/dnsmule-plugins-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dnsmule-plugins-0.1.0.post1.tar", last modified: Mon Mar 13 14:11:45 2023, max compression
+gzip compressed data, was "dnsmule-plugins-0.5.0.tar", last modified: Sat May 13 17:41:07 2023, max compression
```

## Comparing `dnsmule-plugins-0.1.0.post1.tar` & `dnsmule-plugins-0.5.0.tar`

### file list

```diff
@@ -1,29 +1,44 @@
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.867000 dnsmule-plugins-0.1.0.post1/
--rw-r--r--   0 jonium     (501) staff       (20)     4872 2023-03-13 14:11:45.866613 dnsmule-plugins-0.1.0.post1/PKG-INFO
--rw-r--r--   0 jonium     (501) staff       (20)     4123 2023-03-13 14:08:31.000000 dnsmule-plugins-0.1.0.post1/README.md
--rw-r--r--   0 jonium     (501) staff       (20)       38 2023-03-13 14:11:45.867038 dnsmule-plugins-0.1.0.post1/setup.cfg
--rw-r--r--   0 jonium     (501) staff       (20)     1514 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/setup.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.862573 dnsmule-plugins-0.1.0.post1/src/
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.863172 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/
--rw-r--r--   0 jonium     (501) staff       (20)      140 2023-03-13 14:10:18.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/__init__.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.864535 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/
--rw-r--r--   0 jonium     (501) staff       (20)      600 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     5324 2023-03-13 12:22:52.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/certificates.py
--rw-r--r--   0 jonium     (501) staff       (20)     1652 2023-03-13 12:25:13.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/rule.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.865313 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ipranges/
--rw-r--r--   0 jonium     (501) staff       (20)      263 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ipranges/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     4448 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ipranges/ranges.py
--rw-r--r--   0 jonium     (501) staff       (20)     2870 2023-03-13 12:44:23.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ipranges/rule.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.865684 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ptrscan/
--rw-r--r--   0 jonium     (501) staff       (20)      585 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ptrscan/__init__.py
--rw-r--r--   0 jonium     (501) staff       (20)     2730 2023-03-13 07:50:12.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ptrscan/rule.py
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.863743 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/
--rw-r--r--   0 jonium     (501) staff       (20)     4872 2023-03-13 14:11:45.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/PKG-INFO
--rw-r--r--   0 jonium     (501) staff       (20)      654 2023-03-13 14:11:45.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/SOURCES.txt
--rw-r--r--   0 jonium     (501) staff       (20)        1 2023-03-13 14:11:45.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/dependency_links.txt
--rw-r--r--   0 jonium     (501) staff       (20)       39 2023-03-13 14:11:45.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/requires.txt
--rw-r--r--   0 jonium     (501) staff       (20)       16 2023-03-13 14:11:45.000000 dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/top_level.txt
-drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-03-13 14:11:45.866338 dnsmule-plugins-0.1.0.post1/test/
--rw-r--r--   0 jonium     (501) staff       (20)     2175 2023-03-13 12:30:50.000000 dnsmule-plugins-0.1.0.post1/test/test_certcheck.py
--rw-r--r--   0 jonium     (501) staff       (20)     1624 2023-03-13 12:08:18.000000 dnsmule-plugins-0.1.0.post1/test/test_certificates.py
--rw-r--r--   0 jonium     (501) staff       (20)     2911 2023-03-13 12:51:17.000000 dnsmule-plugins-0.1.0.post1/test/test_ipranges.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.233670 dnsmule-plugins-0.5.0/
+-rw-r--r--   0 jonium     (501) staff       (20)     4693 2023-05-13 17:41:07.233469 dnsmule-plugins-0.5.0/PKG-INFO
+-rw-r--r--   0 jonium     (501) staff       (20)     3934 2023-05-09 13:07:06.000000 dnsmule-plugins-0.5.0/README.md
+-rw-r--r--   0 jonium     (501) staff       (20)       38 2023-05-13 17:41:07.233719 dnsmule-plugins-0.5.0/setup.cfg
+-rw-r--r--   0 jonium     (501) staff       (20)     1597 2023-05-13 11:43:22.000000 dnsmule-plugins-0.5.0/setup.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.223397 dnsmule-plugins-0.5.0/src/
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.224430 dnsmule-plugins-0.5.0/src/dnsmule_plugins/
+-rw-r--r--   0 jonium     (501) staff       (20)      134 2023-05-09 13:07:06.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/__init__.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.227088 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/
+-rw-r--r--   0 jonium     (501) staff       (20)      569 2023-05-13 12:34:45.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)      591 2023-05-10 11:29:17.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/adapter.py
+-rw-r--r--   0 jonium     (501) staff       (20)     5514 2023-05-10 10:10:12.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/certificates.py
+-rw-r--r--   0 jonium     (501) staff       (20)      842 2023-05-12 15:44:26.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/domains.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1608 2023-05-13 12:34:45.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/rule.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.227957 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/
+-rw-r--r--   0 jonium     (501) staff       (20)      271 2023-05-10 10:10:12.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)      791 2023-05-13 11:18:33.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/iprange.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.230319 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/
+-rw-r--r--   0 jonium     (501) staff       (20)      302 2023-05-12 23:14:04.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1373 2023-05-13 12:10:26.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/_core.py
+-rw-r--r--   0 jonium     (501) staff       (20)      557 2023-05-12 22:46:44.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/amazon.py
+-rw-r--r--   0 jonium     (501) staff       (20)      612 2023-05-13 11:16:35.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/cloudflare.py
+-rw-r--r--   0 jonium     (501) staff       (20)      517 2023-05-12 23:00:03.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/digitalocean.py
+-rw-r--r--   0 jonium     (501) staff       (20)      979 2023-05-12 22:46:44.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/google.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1671 2023-05-12 23:07:19.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/providers/microsoft.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2462 2023-05-13 12:36:23.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/rule.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.230876 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ptrscan/
+-rw-r--r--   0 jonium     (501) staff       (20)      277 2023-05-10 10:10:12.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ptrscan/__init__.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1605 2023-05-10 10:10:12.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins/ptrscan/rule.py
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.225288 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/
+-rw-r--r--   0 jonium     (501) staff       (20)     4693 2023-05-13 17:41:07.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/PKG-INFO
+-rw-r--r--   0 jonium     (501) staff       (20)     1231 2023-05-13 17:41:07.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/SOURCES.txt
+-rw-r--r--   0 jonium     (501) staff       (20)        1 2023-05-13 17:41:07.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/dependency_links.txt
+-rw-r--r--   0 jonium     (501) staff       (20)       67 2023-05-13 17:41:07.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/requires.txt
+-rw-r--r--   0 jonium     (501) staff       (20)       16 2023-05-13 17:41:07.000000 dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/top_level.txt
+drwxr-xr-x   0 jonium     (501) staff       (20)        0 2023-05-13 17:41:07.233101 dnsmule-plugins-0.5.0/test/
+-rw-r--r--   0 jonium     (501) staff       (20)     2952 2023-05-13 12:36:53.000000 dnsmule-plugins-0.5.0/test/test_certcheck.py
+-rw-r--r--   0 jonium     (501) staff       (20)     1248 2023-05-10 11:26:14.000000 dnsmule-plugins-0.5.0/test/test_certcheck_adapter.py
+-rw-r--r--   0 jonium     (501) staff       (20)      785 2023-05-12 15:46:10.000000 dnsmule-plugins-0.5.0/test/test_certcheck_domains.py
+-rw-r--r--   0 jonium     (501) staff       (20)     9345 2023-05-09 13:07:06.000000 dnsmule-plugins-0.5.0/test/test_certificates.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2478 2023-05-12 22:46:44.000000 dnsmule-plugins-0.5.0/test/test_ipranges.py
+-rw-r--r--   0 jonium     (501) staff       (20)      692 2023-05-09 13:07:06.000000 dnsmule-plugins-0.5.0/test/test_plugins_registration.py
+-rw-r--r--   0 jonium     (501) staff       (20)     3280 2023-05-09 13:07:06.000000 dnsmule-plugins-0.5.0/test/test_ptrscan.py
+-rw-r--r--   0 jonium     (501) staff       (20)     2028 2023-05-13 12:13:57.000000 dnsmule-plugins-0.5.0/test/test_ranges.py
```

### Comparing `dnsmule-plugins-0.1.0.post1/PKG-INFO` & `dnsmule-plugins-0.5.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnsmule-plugins
-Version: 0.1.0.post1
+Version: 0.5.0
 Summary: Plugins for DNSMule
 Home-page: https://github.com/joniumGit/dnsmule
 Author: joniumGit
 Author-email: 52005121+joniumGit@users.noreply.github.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/joniumGit/dnsmule/issues
 Project-URL: Source, https://github.com/joniumGit/dnsmule
@@ -13,15 +13,16 @@
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Internet
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
-Provides-Extra: optional
+Provides-Extra: dev
+Provides-Extra: full
 
 # Plugins for DNSMule
 
 It is recommended to look through each module to see what arguments they take.
 
 #### Certcheck
 
@@ -134,19 +135,14 @@
 
 ```text
 IP::PTR::SAMPLE_RULE::AREA.HOSTER.EXAMPLE.COM
 ```
 
 Any resolved `PTR` records are also added to `result.data['resolvedPointers']`.
 
-This plugin requires the following dependencies:
-
-- `dnspython`
-- `dnsmule.backends.DNSPythonBackend`
-
 ## Example
 
 In YAML the plugins are placed in their own `plugins` block:
 
 ```yaml
 plugins:
   - name: dnsmule_plugins.PTRScanPlugin
@@ -163,15 +159,15 @@
 from dnsmule.backends.dnspython import DNSPythonBackend
 from dnsmule.loader import load_and_append_rule
 from dnsmule_plugins import certcheck, ipranges, ptrscan
 
 mule = DNSMule.make(Rules(), DNSPythonBackend())
 
 certcheck.CertCheckPlugin(callback=False).register(mule)
-ipranges.IPRangesPlugin().register(mule.rules)
+ipranges.IPRangesPlugin().register(mule)
 
 load_and_append_rule(
     mule.rules,
     RRType.A,
     'ip.certs',
     {
         'name': 'certcheck',
@@ -189,18 +185,17 @@
             'microsoft',
             'google',
         ]
     },
 
 )
 
-if mule.backend_type == 'DNSPythonBackend':
-    ptrscan.PTRScanPlugin().register(mule)
-    load_and_append_rule(
-        mule.rules,
-        RRType.A,
-        'ip.ptr',
-        {
-            'name': 'ptrscan'
-        },
-    )
+ptrscan.PTRScanPlugin().register(mule)
+load_and_append_rule(
+    mule.rules,
+    RRType.A,
+    'ip.ptr',
+    {
+        'name': 'ptrscan'
+    },
+)
 ```
```

### Comparing `dnsmule-plugins-0.1.0.post1/README.md` & `dnsmule-plugins-0.5.0/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -113,19 +113,14 @@
 
 ```text
 IP::PTR::SAMPLE_RULE::AREA.HOSTER.EXAMPLE.COM
 ```
 
 Any resolved `PTR` records are also added to `result.data['resolvedPointers']`.
 
-This plugin requires the following dependencies:
-
-- `dnspython`
-- `dnsmule.backends.DNSPythonBackend`
-
 ## Example
 
 In YAML the plugins are placed in their own `plugins` block:
 
 ```yaml
 plugins:
   - name: dnsmule_plugins.PTRScanPlugin
@@ -142,15 +137,15 @@
 from dnsmule.backends.dnspython import DNSPythonBackend
 from dnsmule.loader import load_and_append_rule
 from dnsmule_plugins import certcheck, ipranges, ptrscan
 
 mule = DNSMule.make(Rules(), DNSPythonBackend())
 
 certcheck.CertCheckPlugin(callback=False).register(mule)
-ipranges.IPRangesPlugin().register(mule.rules)
+ipranges.IPRangesPlugin().register(mule)
 
 load_and_append_rule(
     mule.rules,
     RRType.A,
     'ip.certs',
     {
         'name': 'certcheck',
@@ -168,18 +163,17 @@
             'microsoft',
             'google',
         ]
     },
 
 )
 
-if mule.backend_type == 'DNSPythonBackend':
-    ptrscan.PTRScanPlugin().register(mule)
-    load_and_append_rule(
-        mule.rules,
-        RRType.A,
-        'ip.ptr',
-        {
-            'name': 'ptrscan'
-        },
-    )
+ptrscan.PTRScanPlugin().register(mule)
+load_and_append_rule(
+    mule.rules,
+    RRType.A,
+    'ip.ptr',
+    {
+        'name': 'ptrscan'
+    },
+)
 ```
```

### Comparing `dnsmule-plugins-0.1.0.post1/setup.py` & `dnsmule-plugins-0.5.0/setup.py`

 * *Files 23% similar despite different names*

```diff
@@ -37,18 +37,22 @@
             'dnsmule_plugins',
             'dnsmule_plugins.*',
         )
     ),
     python_requires='>=3.7',
     install_requires=[
         'dnsmule',
-        'httpx',
     ],
     extras_require={
-        'optional': [
+        'dev': [
+            'pytest',
+            'pytest-cov',
+            'cryptography',
+        ],
+        'full': [
             'cryptography',
         ]
     },
     project_urls={
         'Bug Reports': f'{repo}/issues',
         'Source': repo,
     },
```

### Comparing `dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/certificates.py` & `dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/certificates.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,42 +1,54 @@
 import datetime
 import socket
+import ssl
 from dataclasses import dataclass
 from typing import List, Optional, Tuple
 
-from dnsmule.config import get_logger
+from dnsmule.logger import get_logger
 
 
-@dataclass(frozen=True, unsafe_hash=True, eq=True)
+@dataclass(frozen=True, eq=True)
 class Certificate:
     version: str
     common: str
     alts: List[str]
     issuer: str
     valid_until: datetime.datetime
     valid_from: datetime.datetime
 
+    def __hash__(self):
+        return hash(self.common)
+
     def to_json(self):
         from dataclasses import asdict
         data = asdict(self)
         return {
-            'valid_until': data.pop('valid_until').isoformat(),
-            'valid_from': data.pop('valid_from').isoformat(),
             **data,
+            'valid_until': data['valid_until'].isoformat(),
+            'valid_from': data['valid_from'].isoformat(),
         }
 
+    @classmethod
+    def from_json(cls, data):
+        data = {
+            **data,
+            'valid_until': datetime.datetime.fromisoformat(data['valid_until']),
+            'valid_from': datetime.datetime.fromisoformat(data['valid_from']),
+        }
+        return cls(**data)
+
 
 @dataclass
 class Address:
     family: socket.AddressFamily
     tuple: Tuple
 
 
 def collect_certificate_cryptography(address: Address, timeout: float):
-    import ssl
     try:
         from cryptography.x509 import load_pem_x509_certificates
         from cryptography.x509.oid import NameOID
         from cryptography.x509.oid import ExtensionOID
         from cryptography.x509.extensions import SubjectAlternativeName, DNSName, ExtensionNotFound
         cert = ssl.get_server_certificate(address.tuple[0:2], timeout=timeout)
         cert = load_pem_x509_certificates(cert.encode())[0]
@@ -56,15 +68,15 @@
         return cert
     except ImportError:
         pass
     except Exception as e:
         get_logger().warning(
             'CERTS-CRYPTOGRAPHY: Failed to get cert for %s:%s (%s)',
             *address.tuple[0:2],
-            type(e).__name__,
+            repr(e),
         )
 
 
 def issuer_str(issuer):
     mapper = {
         'commonName': 'CN',
         'organizationName': 'O',
@@ -76,15 +88,14 @@
         f'{mapper[key]}=' + value.replace(',', r'\,').replace('=', r'\=')
         for key, value in map(lambda t: t[0], issuer[::-1])
     )
 
 
 def massage_certificate_stdlib(certificate):
     if certificate:
-        import ssl
         return {
             'common': next(
                 value
                 for entry in certificate['subject']
                 for field, value in entry
                 if field == 'commonName'
             ),
@@ -101,66 +112,63 @@
                 ssl.cert_time_to_seconds(certificate['notBefore']),
             ),
             'version': 'v%d' % certificate.get('version'),
         }
 
 
 def collect_certificate_stdlib(address: Address, timeout: float):
-    import ssl
-    import socket
     try:
         ctx = ssl.create_default_context()
         ctx.check_hostname = False
         with socket.socket(address.family, socket.SOCK_STREAM) as raw_socket:
             raw_socket.settimeout(timeout)
             with ctx.wrap_socket(raw_socket, do_handshake_on_connect=True) as s:
                 s.connect(address.tuple)
                 return massage_certificate_stdlib(s.getpeercert(binary_form=False))
     except Exception as e:
         get_logger().warning(
             'CERTS-STDLIB: Failed to get cert for %s:%s (%s)',
             *address.tuple[0:2],
-            type(e).__name__,
+            repr(e),
         )
 
 
 def collect_certificate(
         address: Address,
         timeout: float = 1.,
         prefer_stdlib: bool = True,
 ) -> Optional[Certificate]:
+    try:
+        import cryptography
+        use_crypto = True
+    except ImportError:
+        use_crypto = False
+    cert = None
     if prefer_stdlib:
         cert = collect_certificate_stdlib(address, timeout)
-    else:
-        try:
-            import cryptography
-        except ImportError:
-            get_logger().error('Cryptography not installed')
-            raise
-        cert = None
-    if not cert:
+    if not cert and use_crypto:
         cert = collect_certificate_cryptography(address, timeout)
     return Certificate(**cert) if cert else None
 
 
 def collect_certificates(host: str, port: int, **kwargs) -> List[Certificate]:
-    import socket
     out = []
     try:
         for family, _, _, _, info in socket.getaddrinfo(host, port, proto=socket.IPPROTO_TCP):
             cert = collect_certificate(Address(family=family, tuple=info), **kwargs)
             if cert:
                 out.append(cert)
     except socket.error:
         pass
     return out
 
 
 def resolve_domain_from_certificate(cert: Certificate) -> List[str]:
-    """Returns all names from a certificate retrieved from an ip-address
+    """
+    Returns all names from a certificate retrieved from an ip-address
 
     Common name is the first one if available followed by any alternative names
     """
     if cert is not None:
         return [cert.common, *cert.alts]
     else:
         return []
```

### Comparing `dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/certcheck/rule.py` & `dnsmule-plugins-0.5.0/src/dnsmule_plugins/certcheck/rule.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,60 +1,57 @@
-from typing import Callable, Collection, List
+from typing import Callable, Collection, List, Optional
 
-from dnsmule.definitions import Record, Result
-from dnsmule.rules import Rule
-from dnsmule.utils import process_domains
+from dnsmule import Rule, Result, Record
+from dnsmule.utils import extend_set
 from . import certificates
+from .domains import process_domains
+from .adapter import load_result, save_result
 
 
 class CertChecker(Rule):
+    id = 'ip.certs'
+
     ports: List[int] = [443, 8443]
     timeout: float = 1
     stdlib: bool = False
     callback: bool = False
 
-    _callback: Callable[[Collection[str]], None]
+    _callback: Callable[[str, ...], None]
 
     @staticmethod
-    def creator(callback: Callable[[Collection[str]], None]):
-
+    def creator(callback: Optional[Callable[[Collection[str]], None]]):
         def registerer(**kwargs):
             rule = CertChecker(**kwargs)
             rule._callback = callback
             return rule
 
         return registerer
 
     def __call__(self, record: Record) -> Result:
-        address: str = record.data.to_text()
-        certs = []
-        for port in self.ports:
-            certs.extend(
-                certificates.collect_certificates(
-                    address,
-                    port=port,
-                    timeout=self.timeout,
-                    prefer_stdlib=self.stdlib,
-                )
+        certs = {
+            cert
+            for port in self.ports
+            for cert in certificates.collect_certificates(
+                record.text,
+                port=port,
+                timeout=self.timeout,
+                prefer_stdlib=self.stdlib,
             )
-        domains = set()
-        issuers = set()
-        for cert in certs:
-            issuers.add(cert.issuer)
-            domains.update(certificates.resolve_domain_from_certificate(cert))
-        domains = process_domains(*domains)
-        result = record.result()
-
-        certs = [c.to_json() for c in certs]
-        if 'resolvedCertificates' not in result.data:
-            result.data['resolvedCertificates'] = certs
-        else:
-            result.data['resolvedCertificates'].extend(certs)
-
-        if self.callback:
-            self._callback(domains)
-        return result
+        }
+        if certs:
+            load_result(record.result)
+            extend_set(record.result.data, 'resolvedCertificates', certs)
+            save_result(record.result)
+            if self.callback:
+                domains = [*process_domains(
+                    domain
+                    for cert in certs
+                    for domain in certificates.resolve_domain_from_certificate(cert)
+                    if domain != record.domain
+                )]
+                self._callback(*domains)
+        return record.result
 
 
 __all__ = [
     'CertChecker',
 ]
```

### Comparing `dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins/ipranges/rule.py` & `dnsmule-plugins-0.5.0/src/dnsmule_plugins/ipranges/rule.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,88 +1,72 @@
 import asyncio
 import datetime
-from typing import List, Optional, Dict
+from concurrent.futures import ThreadPoolExecutor, wait, ALL_COMPLETED
+from typing import List, Optional, Dict, cast
 
 from dnsmule.definitions import Record, Result
-from dnsmule.rules import DynamicRule
-from . import ranges
+from dnsmule.logger import get_logger
+from dnsmule.rules import Rule
+from .iprange import IPvXRange
+from .providers import Providers
 
 
-class IpRangeChecker(DynamicRule):
+class IpRangeChecker(Rule):
+    id = 'ip.ranges'
+
     providers: List[str]
+    interval_hours: int = 10
 
     _last_fetch: Optional[datetime.datetime] = None
-    _provider_ranges: Dict[str, List[ranges.IPvXRange]]
+    _provider_ranges: Dict[str, List[IPvXRange]]
     _task: asyncio.Task
 
     def __init__(self, **kwargs):
         kwargs['code'] = 'pass'
         super().__init__(**kwargs)
         self.globals = {}
-        self.providers = [*{*self.providers}] if hasattr(self, 'providers') else []
-        self._provider_ranges = {}
+        self.providers = [*{*self.providers}] if hasattr(self, 'providers') else Providers.all()
+        self._provider_ranges = cast(Dict[str, List[IPvXRange]], {})
         for provider in self.providers:
-            # If this fails it will throw
-            self._get_fetcher(provider)
+            if not Providers.available(provider):
+                raise KeyError(f'Provider {provider} does not exist')
+
+    def fetch_provider(self, provider: str):
+        self._provider_ranges[provider] = Providers.fetch(provider)
 
-    def update_fetched(self, *_, **__):
-        self._last_fetch = datetime.datetime.now()
-        del self._task
-
-    def start_fetching(self):
-        self._task = asyncio.create_task(self.fetch_ranges())
-        self._task.add_done_callback(self.update_fetched)
-
-    def init(self, *_, **__):
-        self.start_fetching()
-
-    @staticmethod
-    def _get_fetcher(provider: str):
-        return getattr(ranges, f'fetch_{provider}_ip_ranges')
-
-    async def fetch_provider(self, provider: str):
-        if provider not in self._provider_ranges:
-            self._provider_ranges[provider] = await asyncio.create_task(self._get_fetcher(provider)())
-
-    async def fetch_ranges(self):
-        tasks = []
-        for k in self.providers:
-            tasks.append(asyncio.create_task(self.fetch_provider(k)))
-        if tasks:
-            try:
-                await asyncio.wait(tasks, return_when=asyncio.ALL_COMPLETED)
-            except:
-                coro = asyncio.gather(*tasks)
-                coro.cancel()
-                try:
-                    await coro
-                except (asyncio.TimeoutError, asyncio.CancelledError):
-                    pass
-                raise
-
-    async def check_fetch(self):
-        if hasattr(self, '_task'):
-            await self._task
-        elif not self._last_fetch or abs(datetime.datetime.now() - self._last_fetch) > datetime.timedelta(hours=1):
-            self._provider_ranges.clear()
-            self.start_fetching()
-            await self._task
-
-    async def __call__(self, record: Record) -> Result:
-        await self.check_fetch()
-        result = record.result()
-        address: str = record.data.to_text()
+    def fetch_ranges(self):
+        with ThreadPoolExecutor() as tp:
+            tasks = []
+            for k in self.providers:
+                tasks.append(tp.submit(self.fetch_provider, k))
+            if tasks:
+                wait(tasks, return_when=ALL_COMPLETED)
+                for t in tasks:
+                    if t.done() and t.exception() is not None:
+                        get_logger().error('Failed to fetch ranges', exc_info=t.exception())
+
+    def check_fetch(self):
+        if (
+                not self._last_fetch
+                or abs(datetime.datetime.now() - self._last_fetch) > datetime.timedelta(hours=self.interval_hours)
+        ):
+            self.fetch_ranges()
+            self._last_fetch = datetime.datetime.now()
+
+    def __call__(self, record: Record) -> Result:
+        self.check_fetch()
+        address: str = record.text
         for provider, p_ranges in self._provider_ranges.items():
             for p_range in p_ranges:
                 if address in p_range:
-                    result.tags.add(
+                    record.result.tags.add(
                         f'IP::RANGES'
                         f'::{self.name.upper()}'
                         f'::{p_range.service.upper()}'
                         f'::{p_range.region.upper()}'
                     )
-        return result
+        return record.result
 
 
 __all__ = [
     'IpRangeChecker',
 ]
```

### Comparing `dnsmule-plugins-0.1.0.post1/src/dnsmule_plugins.egg-info/PKG-INFO` & `dnsmule-plugins-0.5.0/src/dnsmule_plugins.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnsmule-plugins
-Version: 0.1.0.post1
+Version: 0.5.0
 Summary: Plugins for DNSMule
 Home-page: https://github.com/joniumGit/dnsmule
 Author: joniumGit
 Author-email: 52005121+joniumGit@users.noreply.github.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/joniumGit/dnsmule/issues
 Project-URL: Source, https://github.com/joniumGit/dnsmule
@@ -13,15 +13,16 @@
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Internet
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
-Provides-Extra: optional
+Provides-Extra: dev
+Provides-Extra: full
 
 # Plugins for DNSMule
 
 It is recommended to look through each module to see what arguments they take.
 
 #### Certcheck
 
@@ -134,19 +135,14 @@
 
 ```text
 IP::PTR::SAMPLE_RULE::AREA.HOSTER.EXAMPLE.COM
 ```
 
 Any resolved `PTR` records are also added to `result.data['resolvedPointers']`.
 
-This plugin requires the following dependencies:
-
-- `dnspython`
-- `dnsmule.backends.DNSPythonBackend`
-
 ## Example
 
 In YAML the plugins are placed in their own `plugins` block:
 
 ```yaml
 plugins:
   - name: dnsmule_plugins.PTRScanPlugin
@@ -163,15 +159,15 @@
 from dnsmule.backends.dnspython import DNSPythonBackend
 from dnsmule.loader import load_and_append_rule
 from dnsmule_plugins import certcheck, ipranges, ptrscan
 
 mule = DNSMule.make(Rules(), DNSPythonBackend())
 
 certcheck.CertCheckPlugin(callback=False).register(mule)
-ipranges.IPRangesPlugin().register(mule.rules)
+ipranges.IPRangesPlugin().register(mule)
 
 load_and_append_rule(
     mule.rules,
     RRType.A,
     'ip.certs',
     {
         'name': 'certcheck',
@@ -189,18 +185,17 @@
             'microsoft',
             'google',
         ]
     },
 
 )
 
-if mule.backend_type == 'DNSPythonBackend':
-    ptrscan.PTRScanPlugin().register(mule)
-    load_and_append_rule(
-        mule.rules,
-        RRType.A,
-        'ip.ptr',
-        {
-            'name': 'ptrscan'
-        },
-    )
+ptrscan.PTRScanPlugin().register(mule)
+load_and_append_rule(
+    mule.rules,
+    RRType.A,
+    'ip.ptr',
+    {
+        'name': 'ptrscan'
+    },
+)
 ```
```

### Comparing `dnsmule-plugins-0.1.0.post1/test/test_certcheck.py` & `dnsmule-plugins-0.5.0/test/test_certcheck.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,43 +1,58 @@
 import datetime
 
 import pytest
 
-from dnsmule import Record, RRType
+from dnsmule import Record, RRType, Result, Domain
 from dnsmule_plugins.certcheck import rule
 from dnsmule_plugins.certcheck.certificates import Certificate
 
 
 @pytest.fixture
 def mock_collection(monkeypatch):
     with monkeypatch.context() as m:
         result = []
         m.setattr(rule.certificates, 'collect_certificates', lambda *_, **__: result)
         yield result
 
 
-def test_certcheck_rule_creator_returns_callable():
+def test_rule_creator_returns_callable():
     def dummy():
         pass
 
     creator = rule.CertChecker.creator(dummy)
 
     assert callable(creator), 'Failed to create callable'
     assert creator()._callback is dummy, 'Failed to bind callback'
 
 
-def test_certcheck_call(mock_collection):
+def test_call(mock_collection):
     check = rule.CertChecker()
-    r = Record('', RRType.A, '')
-    assert check(r)['resolvedCertificates'] == [], 'Failed to produce output'
+    r = Record(Domain(''), RRType.A, '')
+    assert 'resolvedCertificates' not in check(r).data, 'Added key without data to add'
 
 
-def test_certcheck_call_add_domains(mock_collection):
+def test_call_adds_key(mock_collection):
+    mock_collection.append(Certificate(
+        version='v3',
+        common='a.com',
+        alts=['b.com'],
+        valid_from=datetime.datetime.now(),
+        valid_until=datetime.datetime.now(),
+        issuer='',
+    ))
+    check = rule.CertChecker()
+    r = Record(Domain(''), RRType.A, '')
+    assert 'resolvedCertificates' in check(r).data, 'Failed to add key'
+
+
+def test_call_add_certs(mock_collection):
     check = rule.CertChecker(ports=[443])
-    r = Record('', RRType.A, '')
+    r = Record(Domain(''), RRType.A, '')
+    r.existing = Result(Domain(''))
 
     cert1 = Certificate(
         version='v3',
         common='d.com',
         alts=['e.com'],
         valid_from=datetime.datetime.now(),
         valid_until=datetime.datetime.now(),
@@ -49,29 +64,38 @@
         common='a.com',
         alts=['b.com'],
         valid_from=datetime.datetime.now(),
         valid_until=datetime.datetime.now(),
         issuer='',
     )
 
-    r.result()['resolvedCertificates'] = [cert1.to_json()]
+    r.existing.data['resolvedCertificates'] = [cert1.to_json()]
     mock_collection.append(cert2)
+    mock_collection.append(cert1)
+
+    result = check(r)
+
+    assert len((check(r)).data['resolvedCertificates']) == 2, 'Failed to remove duplicates'
+
+    certs = result.data['resolvedCertificates']
+    assert cert1.to_json() in certs, 'Failed to append existing data'
+    assert cert2.to_json() in certs, 'Failed to append data'
 
-    assert check(r)['resolvedCertificates'] == [cert1.to_json(), cert2.to_json()], 'Failed to append data'
+    assert len((check(r)).data['resolvedCertificates']) == 2, 'Failed to remove duplicates'
 
 
-def test_certcheck_callback_with_domains(mock_collection):
+def test_callback_with_domains(mock_collection):
     result = set()
 
-    def callback(domains):
+    def callback(*domains):
         result.update(domains)
 
     check = rule.CertChecker.creator(callback)(ports=[443], callback=True)
 
-    r = Record('', RRType.A, '')
+    r = Record(Domain(''), RRType.A, '')
 
     cert1 = Certificate(
         version='v3',
         common='a.com',
         alts=['b.com'],
         valid_from=datetime.datetime.now(),
         valid_until=datetime.datetime.now(),
```

### Comparing `dnsmule-plugins-0.1.0.post1/test/test_ipranges.py` & `dnsmule-plugins-0.5.0/test/test_ipranges.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,106 +1,85 @@
 import datetime
-from asyncio import sleep
 from ipaddress import IPv4Network
+from time import sleep
 
 import pytest
 
-from _async import async_test
 from dnsmule import Record, RRType
-from dnsmule_plugins.ipranges.ranges import IPvXRange
+from dnsmule_plugins.ipranges.iprange import IPvXRange
 from dnsmule_plugins.ipranges.rule import IpRangeChecker
 
 
-@async_test
-async def test_ipranges_task():
+def test_task():
     checker = IpRangeChecker(providers=[])
 
     assert checker._last_fetch is None, 'Spawned with fetch time'
 
-    async def fetch_ranges():
-        await sleep(.1)
+    def fetch_ranges():
+        sleep(.1)
 
     checker.fetch_ranges = fetch_ranges
 
-    await checker.check_fetch()
+    checker.check_fetch()
 
     assert not hasattr(checker, '_task'), 'Task did not get deleted'
     assert checker._last_fetch is not None, 'Missing fetch time'
 
 
-@async_test
-async def test_ipranges_task_if_task_exists():
+def test_task_if_task_exists():
     checker = IpRangeChecker(providers=[])
     called = []
 
-    async def fetch_ranges():
+    def fetch_ranges():
         called.append('fetch')
 
-    checker._task = fetch_ranges()
-
-    await checker.check_fetch()
-    assert called == ['fetch'], 'Task was not awaited'
-
-
-@async_test
-async def test_ipranges_task_if_not_recent():
-    """Visible from coverage only
-    """
-    checker = IpRangeChecker(providers=[])
-    called = []
-
-    async def fetch_ranges():
-        await sleep(.1)
-        called.append('fetch')
-
-    def start_fetch():
-        checker._task = fetch_ranges()
-
-    checker.start_fetching = start_fetch
-
-    checker._last_fetch = datetime.datetime.now()
-    await checker.check_fetch()
-    assert len(called) == 0, 'Task was called'
+    checker.fetch_ranges = fetch_ranges
 
-    checker._last_fetch = checker._last_fetch - datetime.timedelta(days=1)
-    await checker.check_fetch()
-    assert len(called) == 1, 'Task was not called'
+    checker.check_fetch()
+    assert called == ['fetch'], 'Not fetched'
 
 
-def test_ipranges_unknown_provider():
-    with pytest.raises(AttributeError):
+def test_unknown_provider():
+    with pytest.raises(Exception):
         IpRangeChecker(providers=['adwadawdawdawdwad'])
 
 
-@async_test
-async def test_ipranges_provider_tags():
+def test_provider_tags():
     rule = IpRangeChecker(providers=[], name='test_rule')
     rule._provider_ranges['test_provider'] = [IPvXRange(
         address=IPv4Network('127.0.0.0/31'),
         region='test_region',
         service='test_service',
     )]
     r = Record('', RRType.A, '127.0.0.1')
     rule._last_fetch = datetime.datetime.now()
-    await rule(r)
-    assert 'IP::RANGES::TEST_RULE::TEST_SERVICE::TEST_REGION' in r.result()
+    rule(r)
+    assert 'IP::RANGES::TEST_RULE::TEST_SERVICE::TEST_REGION' in r.result
 
 
-@async_test
-async def test_ipranges_provider_no_tags_if_no_match():
+def test_provider_no_tags_if_no_match():
     rule = IpRangeChecker(providers=[], name='test_rule')
     rule._provider_ranges['test_provider'] = [IPvXRange(
         address=IPv4Network('128.0.0.0/24'),
         region='test_region',
         service='test_service',
     )]
     r = Record('', RRType.A, '127.0.0.1')
     rule._last_fetch = datetime.datetime.now()
-    await rule(r)
-    assert len(r.result().tags) == 0, 'Had a tag'
+    rule(r)
+    assert len(r.result.tags) == 0, 'Had a tag'
 
 
-@async_test
-async def test_ipranges_provider_empty_provider_fetch_ok():
+def test_provider_empty_provider_fetch_ok():
     rule = IpRangeChecker(providers=[], name='test_rule')
-    await rule.check_fetch()
+    rule.check_fetch()
     assert rule._last_fetch is not None, 'Failed fetch'
+
+
+def test_fetcher_for_provider(monkeypatch):
+    sentinel = object()
+    with monkeypatch.context() as m:
+        from dnsmule_plugins.ipranges.providers import Providers
+        m.setitem(Providers._mapping, 'mock', lambda: sentinel)
+        checker = IpRangeChecker(providers=['mock'])
+        checker.fetch_provider('mock')
+        assert checker._provider_ranges['mock'] is sentinel, 'Failed to get provider from package or failed to call'
```

