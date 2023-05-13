# Comparing `tmp/ciscoconfparse-1.7.8.tar.gz` & `tmp/ciscoconfparse-1.7.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ciscoconfparse-1.7.8.tar", max compression
+gzip compressed data, was "ciscoconfparse-1.7.9.tar", max compression
```

## Comparing `ciscoconfparse-1.7.8.tar` & `ciscoconfparse-1.7.9.tar`

### file list

```diff
@@ -1,23 +1,23 @@
--rw-r--r--   0        0        0    82507 2023-01-28 13:53:11.332983 ciscoconfparse-1.7.8/CHANGES.md
--rw-r--r--   0        0        0     3563 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/CONTRIBUTING.md
--rw-r--r--   0        0        0    32422 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/LICENSE
--rw-r--r--   0        0        0     9024 2023-01-27 14:44:53.397433 ciscoconfparse-1.7.8/Makefile
--rw-r--r--   0        0        0     8833 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/README.md
--rw-r--r--   0        0        0     1352 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/README_git_workflow.md
--rw-r--r--   0        0        0     1569 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/ciscoconfparse/__init__.py
--rw-r--r--   0        0        0     1483 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.8/ciscoconfparse/__main__.py
--rw-r--r--   0        0        0    44453 2023-01-22 23:50:12.814200 ciscoconfparse-1.7.8/ciscoconfparse/ccp_abc.py
--rw-r--r--   0        0        0   102068 2023-01-28 03:34:20.339474 ciscoconfparse-1.7.8/ciscoconfparse/ccp_util.py
--rw-r--r--   0        0        0   100845 2023-01-27 14:07:52.061774 ciscoconfparse-1.7.8/ciscoconfparse/ccp_util.py.0
--rw-r--r--   0        0        0   230772 2023-01-28 13:53:11.332983 ciscoconfparse-1.7.8/ciscoconfparse/ciscoconfparse.py
--rw-r--r--   0        0        0   227847 2023-01-27 14:02:37.936659 ciscoconfparse-1.7.8/ciscoconfparse/ciscoconfparse.py.0
--rw-r--r--   0        0        0     1546 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/errors.py
--rw-r--r--   0        0        0    44244 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/models_asa.py
--rw-r--r--   0        0        0    76274 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/models_cisco.py
--rw-r--r--   0        0        0    75908 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/models_iosxr.py
--rw-r--r--   0        0        0    25031 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/models_junos.py
--rw-r--r--   0        0        0    79156 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/models_nxos.py
--rw-r--r--   0        0        0     3392 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.8/ciscoconfparse/protocol_values.py
--rw-r--r--   0        0        0     2805 2023-01-28 13:53:11.336983 ciscoconfparse-1.7.8/pyproject.toml
--rw-r--r--   0        0        0     9905 1970-01-01 00:00:00.000000 ciscoconfparse-1.7.8/setup.py
--rw-r--r--   0        0        0    10653 1970-01-01 00:00:00.000000 ciscoconfparse-1.7.8/PKG-INFO
+-rw-r--r--   0        0        0    82610 2023-01-28 13:57:50.514676 ciscoconfparse-1.7.9/CHANGES.md
+-rw-r--r--   0        0        0     3563 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/CONTRIBUTING.md
+-rw-r--r--   0        0        0    32422 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/LICENSE
+-rw-r--r--   0        0        0     9024 2023-01-27 14:44:53.397433 ciscoconfparse-1.7.9/Makefile
+-rw-r--r--   0        0        0     8833 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/README.md
+-rw-r--r--   0        0        0     1352 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/README_git_workflow.md
+-rw-r--r--   0        0        0     1569 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/ciscoconfparse/__init__.py
+-rw-r--r--   0        0        0     1483 2023-01-22 23:50:12.810200 ciscoconfparse-1.7.9/ciscoconfparse/__main__.py
+-rw-r--r--   0        0        0    44453 2023-01-22 23:50:12.814200 ciscoconfparse-1.7.9/ciscoconfparse/ccp_abc.py
+-rw-r--r--   0        0        0   102068 2023-01-28 03:34:20.339474 ciscoconfparse-1.7.9/ciscoconfparse/ccp_util.py
+-rw-r--r--   0        0        0   100845 2023-01-27 14:07:52.061774 ciscoconfparse-1.7.9/ciscoconfparse/ccp_util.py.0
+-rw-r--r--   0        0        0   230772 2023-01-28 13:53:11.332983 ciscoconfparse-1.7.9/ciscoconfparse/ciscoconfparse.py
+-rw-r--r--   0        0        0   227847 2023-01-27 14:02:37.936659 ciscoconfparse-1.7.9/ciscoconfparse/ciscoconfparse.py.0
+-rw-r--r--   0        0        0     1546 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/errors.py
+-rw-r--r--   0        0        0    44244 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/models_asa.py
+-rw-r--r--   0        0        0    76274 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/models_cisco.py
+-rw-r--r--   0        0        0    75908 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/models_iosxr.py
+-rw-r--r--   0        0        0    25031 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/models_junos.py
+-rw-r--r--   0        0        0    79156 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/models_nxos.py
+-rw-r--r--   0        0        0     3392 2023-01-22 23:50:12.818200 ciscoconfparse-1.7.9/ciscoconfparse/protocol_values.py
+-rw-r--r--   0        0        0     2805 2023-01-28 13:57:50.514676 ciscoconfparse-1.7.9/pyproject.toml
+-rw-r--r--   0        0        0     9905 1970-01-01 00:00:00.000000 ciscoconfparse-1.7.9/setup.py
+-rw-r--r--   0        0        0    10653 1970-01-01 00:00:00.000000 ciscoconfparse-1.7.9/PKG-INFO
```

### Comparing `ciscoconfparse-1.7.8/CHANGES.md` & `ciscoconfparse-1.7.9/CHANGES.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,19 @@
 ## Version: GIT HEAD
 
 - Released: Not released
 - Summary:
     - Insert something here
 
+## Version: 1.7.9
+
+- Released: 2023-01-28
+- Summary:
+    - Fix unit tests to work with version 1.7.8+
+
 ## Version: 1.7.8
 
 - Released: 2023-01-28
 - Summary:
     - Validate that CiscoConfParse().ConfigObjs is None or instance of MutableSequence
     - Convert all checks for `collections.abc.Iterator` to `collections.abc.Sequence`; ref github issue #256
     - Streamline `CiscoConfParse().__init__()` logic and delegate `__init__()` tasks to dedicated methods.
```

### Comparing `ciscoconfparse-1.7.8/CONTRIBUTING.md` & `ciscoconfparse-1.7.9/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/LICENSE` & `ciscoconfparse-1.7.9/LICENSE`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/Makefile` & `ciscoconfparse-1.7.9/Makefile`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/README.md` & `ciscoconfparse-1.7.9/README.md`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/README_git_workflow.md` & `ciscoconfparse-1.7.9/README_git_workflow.md`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/__init__.py` & `ciscoconfparse-1.7.9/ciscoconfparse/__init__.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/__main__.py` & `ciscoconfparse-1.7.9/ciscoconfparse/__main__.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/ccp_abc.py` & `ciscoconfparse-1.7.9/ciscoconfparse/ccp_abc.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/ccp_util.py` & `ciscoconfparse-1.7.9/ciscoconfparse/ccp_util.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/ccp_util.py.0` & `ciscoconfparse-1.7.9/ciscoconfparse/ccp_util.py.0`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/ciscoconfparse.py` & `ciscoconfparse-1.7.9/ciscoconfparse/ciscoconfparse.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/ciscoconfparse.py.0` & `ciscoconfparse-1.7.9/ciscoconfparse/ciscoconfparse.py.0`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/errors.py` & `ciscoconfparse-1.7.9/ciscoconfparse/errors.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/models_asa.py` & `ciscoconfparse-1.7.9/ciscoconfparse/models_asa.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/models_cisco.py` & `ciscoconfparse-1.7.9/ciscoconfparse/models_cisco.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/models_iosxr.py` & `ciscoconfparse-1.7.9/ciscoconfparse/models_iosxr.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/models_junos.py` & `ciscoconfparse-1.7.9/ciscoconfparse/models_junos.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/models_nxos.py` & `ciscoconfparse-1.7.9/ciscoconfparse/models_nxos.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/ciscoconfparse/protocol_values.py` & `ciscoconfparse-1.7.9/ciscoconfparse/protocol_values.py`

 * *Files identical despite different names*

### Comparing `ciscoconfparse-1.7.8/pyproject.toml` & `ciscoconfparse-1.7.9/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 # [project] section work with 'pip install ciscoconfparse'.
 #
 ##############################################################################
 #[project]
 
 [tool.poetry]
 name = "ciscoconfparse"
-version = "1.7.8"
+version = "1.7.9"
 description = "Parse, Audit, Query, Build, and Modify Cisco IOS-style and JunOS-style configs"
 license = "GPL-3.0-only"
 authors = ["Mike Pennington <mike@pennington.net>"]
 readme = "README.md"
 keywords = ["Parse", "audit", "query", "modify", "Cisco IOS", "Cisco", "NXOS", "ASA", "Juniper"]
 classifiers=[
     "Development Status :: 5 - Production/Stable",
```

### Comparing `ciscoconfparse-1.7.8/setup.py` & `ciscoconfparse-1.7.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,15 +12,15 @@
  'dnspython>=2.2.0,<3.0.0',
  'loguru==0.6.0',
  'passlib>=1.7.4,<2.0.0',
  'toml>=0.10.2']
 
 setup_kwargs = {
     'name': 'ciscoconfparse',
-    'version': '1.7.8',
+    'version': '1.7.9',
     'description': 'Parse, Audit, Query, Build, and Modify Cisco IOS-style and JunOS-style configs',
     'long_description': 'ciscoconfparse\n==============\n\n[![Github unittest workflow][4]][5] [![Code Health][37]][38] [![git commits][41]][42] [![Repo Code Grade][43]][44]  [![Version][2]][3] [![Downloads][6]][7] [![License][8]][9]\n\n\nIntroduction: What is ciscoconfparse?\n-------------------------------------\n\nShort answer: ciscoconfparse is a [Python][10] library\nthat helps you quickly answer questions like these about your\nCisco configurations:\n\n- What interfaces are shutdown?\n- Which interfaces are in trunk mode?\n- What address and subnet mask is assigned to each interface?\n- Which interfaces are missing a critical command?\n- Is this configuration missing a standard config line?\n\nIt can help you:\n\n- Audit existing router / switch / firewall / wlc configurations\n- Modify existing configurations\n- Build new configurations\n\nSpeaking generally, the library examines an IOS-style config and breaks\nit into a set of linked parent / child relationships. You can perform\ncomplex queries about these relationships.\n\n[![Cisco IOS config: Parent / child][11]][11]\n\nUsage\n-----\n\nThe following code will parse a configuration stored in\n\\\'exampleswitch.conf\\\' and select interfaces that are shutdown.\n\n```python\nfrom ciscoconfparse import CiscoConfParse\n\nparse = CiscoConfParse(\'exampleswitch.conf\', syntax=\'ios\')\n\nfor intf_obj in parse.find_objects_w_child(\'^interface\', \'^\\s+shutdown\'):\n    print("Shutdown: " + intf_obj.text)\n```\n\nThe next example will find the IP address assigned to interfaces.\n\n```python\nfrom ciscoconfparse import CiscoConfParse\n\nparse = CiscoConfParse(\'exampleswitch.conf\', syntax=\'ios\')\n\nfor intf_obj in parse.find_objects(\'^interface\'):\n\n    intf_name = intf_obj.re_match_typed(\'^interface\\s+(\\S.+?)$\')\n\n    # Search children of all interfaces for a regex match and return\n    # the value matched in regex match group 1.  If there is no match,\n    # return a default value: \'\'\n    intf_ip_addr = intf_obj.re_match_iter_typed(\n        r\'ip\\saddress\\s(\\d+\\.\\d+\\.\\d+\\.\\d+)\\s\', result_type=str,\n        group=1, default=\'\')\n    print("{0}: {1}".format(intf_name, intf_ip_addr))\n```\n\nWhat if we don\\\'t use Cisco?\n----------------------------\n\nDon\\\'t let that stop you.\n\nAs of CiscoConfParse 1.2.4, you can parse [brace-delimited configurations][13] into a Cisco IOS style (see [Github Issue \\#17][14]), which means that CiscoConfParse can parse these configurations:\n\n- Juniper Networks Junos\n- Palo Alto Networks Firewall configurations\n- F5 Networks configurations\n\nCiscoConfParse also handles anything that has a Cisco IOS style of configuration, which includes:\n\n- Cisco IOS, Cisco Nexus, Cisco IOS-XR, Cisco IOS-XE, Aironet OS, Cisco ASA, Cisco CatOS\n- Arista EOS\n- Brocade\n- HP Switches\n- Force 10 Switches\n- Dell PowerConnect Switches\n- Extreme Networks\n- Enterasys\n- Screenos\n\nDocs\n----\n\n- The latest copy of the docs are [archived on the web][15]\n- There is also a [CiscoConfParse Tutorial][16]\n\nEditing the Package\n-------------------\n\n-   `git clone https://github.com/mpenning/ciscoconfparse`\n-   `cd ciscoconfparse`\n-   `git checkout -b develop`\n-   Add / modify / delete on the `develop` branch\n-   `make test`\n-   If tests run clean, `git commit` all the pending changes on the `develop` branch\n-   (as required) Edit the version number in [pyproject.toml][12]\n-   `git checkout main`\n-   `git merge develop`\n-   `make test`\n-   `make repo-push`\n-   `make pypi`\n\nPre-requisites\n--------------\n\n[The ciscoconfparse python package][3] requires Python versions 3.7+ (note: Python version 3.7.0 has a bug - ref [Github issue \\#117][18], but version 3.7.1 works); the OS should not matter.\n\nInstallation and Downloads\n--------------------------\n\n-   Use `poetry` for Python3.x\\... :\n\n        python -m pip install ciscoconfparse\n\nIf you\\\'re interested in the source, you can always pull from the [github repo][17]:\n\n- Download from [the github repo][17]: :\n\n        git clone git://github.com/mpenning/ciscoconfparse\n        cd ciscoconfparse/\n        python -m pip install .\n\nGithub Star History\n-------------------\n\n[![Github Star History Chart][40]][40]\n\nOther Resources\n---------------\n\n- [Dive into Python3](http://www.diveintopython3.net/) is a good way to learn Python\n- [Team CYMRU][30] has a [Secure IOS Template][29], which is especially useful for external-facing routers / switches\n- [Cisco\\\'s Guide to hardening IOS devices][31]\n- [Center for Internet Security Benchmarks][32] (An email address, cookies, and javascript are required)\n\nBug Tracker and Support\n-----------------------\n\n- Please report any suggestions, bug reports, or annoyances with a [github bug report][24].\n- If you\\\'re having problems with general python issues, consider searching for a solution on [Stack Overflow][33].  If you can\\\'t find a solution for your problem or need more help, you can [ask on Stack Overflow][34] or [reddit/r/Python][39].\n- If you\\\'re having problems with your Cisco devices, you can contact:\n  - [Cisco TAC][28]\n  - [reddit/r/Cisco][35]\n  - [reddit/r/networking][36]\n  - [NetworkEngineering.se][23]\n\nUnit-Tests\n----------\n\nThe project\\\'s [test workflow][1] checks ciscoconfparse on Python versions 3.6 and higher, as well as a [pypy JIT][22] executable.\n\nClick the image below for details; the current build status is: [![Github unittest status][4]][5]\n\nSphinx Documentation\n--------------------\n\nBuilding the ciscoconfparse documentation tarball comes down to this one wierd trick:\n\n- `cd sphinx-doc/`\n- `pip install -r ./requirements.txt;  # install Sphinx dependencies`\n- `pip install -r ../requirements.txt; # install ccp dependencies`\n- `make html`\n\nLicense and Copyright\n---------------------\n\n[ciscoconfparse][3] is licensed [GPLv3][21]\n\n- Copyright (C) 2021-2022 David Michael Pennington\n- Copyright (C) 2020-2021 David Michael Pennington at Cisco Systems (post-acquisition: Cisco acquired ThousandEyes)\n- Copyright (C) 2019 David Michael Pennington at ThousandEyes\n- Copyright (C) 2012-2019 David Michael Pennington at Samsung Data Services\n- Copyright (C) 2011-2012 David Michael Pennington at Dell Computer Corp\n- Copyright (C) 2007-2011 David Michael Pennington\n\nThe word \\"Cisco\\" is a registered trademark of [Cisco Systems][27].\n\nAuthor\n------\n\n[ciscoconfparse][3] was written by [David Michael Pennington][25] (mike \\[\\~at\\~\\] pennington \\[.dot.\\] net).\n\n\n  [1]: https://github.com/mpenning/ciscoconfparse/tree/master/.github/workflows\n  [2]: https://img.shields.io/pypi/v/ciscoconfparse.svg\n  [3]: https://pypi.python.org/pypi/ciscoconfparse/\n  [4]: https://github.com/mpenning/ciscoconfparse/actions/workflows/tests.yml/badge.svg\n  [5]: https://github.com/mpenning/ciscoconfparse/actions/workflows/tests.yml\n  [6]: https://pepy.tech/badge/ciscoconfparse\n  [7]: https://pepy.tech/project/ciscoconfparse\n  [8]: http://img.shields.io/badge/license-GPLv3-blue.svg\n  [9]: https://www.gnu.org/copyleft/gpl.html\n  [10]: https://www.python.org\n  [11]: https://raw.githubusercontent.com/mpenning/ciscoconfparse/master/sphinx-doc/_static/ciscoconfparse_overview_75pct.png\n  [12]: https://github.com/mpenning/ciscoconfparse/blob/main/pyproject.toml\n  [13]: https://github.com/mpenning/ciscoconfparse/blob/master/configs/sample_01.junos\n  [14]: https://github.com/mpenning/ciscoconfparse/issues/17\n  [15]: http://www.pennington.net/py/ciscoconfparse/\n  [16]: http://pennington.net/tutorial/ciscoconfparse/ccp_tutorial.html\n  [17]: https://github.com/mpenning/ciscoconfparse\n  [18]: https://github.com/mpenning/ciscoconfparse/issues/117\n  [19]: https://github.com/mpenning/ciscoconfparse/issues/13\n  [20]: https://github.com/CrackerJackMack/\n  [21]: http://www.gnu.org/licenses/gpl-3.0.html\n  [22]: https://pypy.org\n  [23]: https://networkengineering.stackexchange.com/\n  [24]: https://github.com/mpenning/ciscoconfparse/issues/new/choose\n  [25]: https://github.com/mpenning\n  [26]: https://github.com/muir\n  [27]: https://www.cisco.com/\n  [28]: https://www.cisco.com/go/support\n  [29]: https://www.cymru.com/Documents/secure-ios-template.html\n  [30]: https://team-cymru.com/company/\n  [31]: http://www.cisco.com/c/en/us/support/docs/ip/access-lists/13608-21.html\n  [32]: https://learn.cisecurity.org/benchmarks\n  [33]: https://stackoverflow.com\n  [34]: http://stackoverflow.com/questions/ask\n  [35]: https://www.reddit.com/r/Cisco/\n  [36]: https://www.reddit.com/r/networking\n  [37]: https://snyk.io/advisor/python/ciscoconfparse/badge.svg\n  [38]: https://snyk.io/advisor/python/ciscoconfparse\n  [39]: https://www.reddit.com/r/Python/\n  [40]: https://api.star-history.com/svg?repos=mpenning/ciscoconfparse&type=Date\n  [41]: https://img.shields.io/github/commit-activity/m/mpenning/ciscoconfparse\n  [42]: https://img.shields.io/github/commit-activity/m/mpenning/ciscoconfparse\n  [43]: https://www.codefactor.io/Content/badges/B.svg\n  [44]: https://www.codefactor.io/repository/github/mpenning/ciscoconfparse/\n',
     'author': 'Mike Pennington',
     'author_email': 'mike@pennington.net',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `ciscoconfparse-1.7.8/PKG-INFO` & `ciscoconfparse-1.7.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ciscoconfparse
-Version: 1.7.8
+Version: 1.7.9
 Summary: Parse, Audit, Query, Build, and Modify Cisco IOS-style and JunOS-style configs
 License: GPL-3.0-only
 Keywords: Parse,audit,query,modify,Cisco IOS,Cisco,NXOS,ASA,Juniper
 Author: Mike Pennington
 Author-email: mike@pennington.net
 Requires-Python: >=3.7.2,<4.0.0
 Classifier: Development Status :: 5 - Production/Stable
```

