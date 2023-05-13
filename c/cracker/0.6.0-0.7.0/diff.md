# Comparing `tmp/cracker-0.6.0.tar.gz` & `tmp/cracker-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cracker-0.6.0.tar", last modified: Mon Mar 27 02:02:16 2023, max compression
+gzip compressed data, was "cracker-0.7.0.tar", last modified: Sat May 13 19:36:43 2023, max compression
```

## Comparing `cracker-0.6.0.tar` & `cracker-0.7.0.tar`

### file list

```diff
@@ -1,53 +1,57 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.118511 cracker-0.6.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.106511 cracker-0.6.0/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.110511 cracker-0.6.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      731 2023-03-27 02:02:01.000000 cracker-0.6.0/.github/workflows/publish-pypi.yml
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-03-27 02:02:01.000000 cracker-0.6.0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-03-27 02:02:01.000000 cracker-0.6.0/.python-version
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-03-27 02:02:01.000000 cracker-0.6.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      496 2023-03-27 02:02:01.000000 cracker-0.6.0/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-03-27 02:02:16.118511 cracker-0.6.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3393 2023-03-27 02:02:01.000000 cracker-0.6.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.114511 cracker-0.6.0/cracker/
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.114511 cracker-0.6.0/cracker/config/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6500 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/config/configuration.py
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/config/default.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/config/parser.json
--rw-r--r--   0 runner    (1001) docker     (123)     5789 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/cracker.py
--rw-r--r--   0 runner    (1001) docker     (123)    10113 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/cracker_gui.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2206 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/icon.jpeg
--rwxr-xr-x   0 runner    (1001) docker     (123)     4856 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/icon.png
--rw-r--r--   0 runner    (1001) docker     (123)      921 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/keylogger.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/main.py
--rw-r--r--   0 runner    (1001) docker     (123)      834 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/mp3_helper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.118511 cracker-0.6.0/cracker/speaker/
--rw-r--r--   0 runner    (1001) docker     (123)      816 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/speaker/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      922 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/speaker/abstract_speaker.py
--rw-r--r--   0 runner    (1001) docker     (123)     1923 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/speaker/espeak.py
--rw-r--r--   0 runner    (1001) docker     (123)     3175 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/speaker/google.py
--rw-r--r--   0 runner    (1001) docker     (123)     3751 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/speaker/polly.py
--rw-r--r--   0 runner    (1001) docker     (123)      963 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/ssml.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.118511 cracker-0.6.0/cracker/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     2950 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/tests/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3288 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/tests/test_text_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     3195 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/text_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)   425270 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/themes.py
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.118511 cracker-0.6.0/cracker/view/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/view/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4998 2023-03-27 02:02:01.000000 cracker-0.6.0/cracker/view/config_window.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.114511 cracker-0.6.0/cracker.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      958 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       42 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      230 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-03-27 02:02:16.000000 cracker-0.6.0/cracker.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-03-27 02:02:01.000000 cracker-0.6.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-27 02:02:16.118511 cracker-0.6.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-27 02:02:16.118511 cracker-0.6.0/ubuntu/
--rw-r--r--   0 runner    (1001) docker     (123)      300 2023-03-27 02:02:01.000000 cracker-0.6.0/ubuntu/cracker.desktop
--rw-r--r--   0 runner    (1001) docker     (123)     4856 2023-03-27 02:02:01.000000 cracker-0.6.0/ubuntu/icon.png
--rwxr-xr-x   0 runner    (1001) docker     (123)      899 2023-03-27 02:02:01.000000 cracker-0.6.0/ubuntu/install_ubuntu.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.832904 cracker-0.7.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.836904 cracker-0.7.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      731 2023-05-13 19:36:31.000000 cracker-0.7.0/.github/workflows/publish-pypi.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-13 19:36:31.000000 cracker-0.7.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 19:36:31.000000 cracker-0.7.0/.python-version
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-05-13 19:36:31.000000 cracker-0.7.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      496 2023-05-13 19:36:31.000000 cracker-0.7.0/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-05-13 19:36:43.840904 cracker-0.7.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3393 2023-05-13 19:36:31.000000 cracker-0.7.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.836904 cracker-0.7.0/cracker/
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.836904 cracker-0.7.0/cracker/config/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6425 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/config/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/config/default.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/config/parser.json
+-rw-r--r--   0 runner    (1001) docker     (123)     5557 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/cracker.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10091 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/cracker_gui.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2206 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/icon.jpeg
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4856 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/icon.png
+-rw-r--r--   0 runner    (1001) docker     (123)      921 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/keylogger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/mp3_helper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/cracker/speaker/
+-rw-r--r--   0 runner    (1001) docker     (123)      816 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/speaker/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      878 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/speaker/abstract_speaker.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1923 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/speaker/espeak.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3093 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/speaker/google.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3928 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/speaker/polly.py
+-rw-r--r--   0 runner    (1001) docker     (123)      963 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/ssml.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/cracker/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2902 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/tests/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3288 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/tests/test_text_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3195 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/text_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)   425242 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/themes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/cracker/view/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/view/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/view/config_window.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4554 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/view/parser_config_tab.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2200 2023-05-13 19:36:31.000000 cracker-0.7.0/cracker/view/speaker_config_tab.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.836904 cracker-0.7.0/cracker.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      230 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-13 19:36:43.000000 cracker-0.7.0/cracker.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-05-13 19:36:31.000000 cracker-0.7.0/docs/macos.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-05-13 19:36:31.000000 cracker-0.7.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 19:36:43.840904 cracker-0.7.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 19:36:43.840904 cracker-0.7.0/ubuntu/
+-rw-r--r--   0 runner    (1001) docker     (123)      300 2023-05-13 19:36:31.000000 cracker-0.7.0/ubuntu/cracker.desktop
+-rw-r--r--   0 runner    (1001) docker     (123)     4856 2023-05-13 19:36:31.000000 cracker-0.7.0/ubuntu/icon.png
+-rwxr-xr-x   0 runner    (1001) docker     (123)      899 2023-05-13 19:36:31.000000 cracker-0.7.0/ubuntu/install_ubuntu.sh
```

### Comparing `cracker-0.6.0/.github/workflows/publish-pypi.yml` & `cracker-0.7.0/.github/workflows/publish-pypi.yml`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/LICENSE` & `cracker-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/PKG-INFO` & `cracker-0.7.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cracker
-Version: 0.6.0
+Version: 0.7.0
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 Provides-Extra: build
 Provides-Extra: test
 License-File: LICENSE
 
 # Cracker
```

### Comparing `cracker-0.6.0/README.md` & `cracker-0.7.0/README.md`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/config/configuration.py` & `cracker-0.7.0/cracker/config/configuration.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,71 +1,72 @@
 import json
 import os
 import pkgutil
-from typing import Any, Dict
+from typing import Any, Dict, Optional
 
 import yaml
 
 from cracker.speaker import LANGUAGES
-from cracker.utils import get_logger
+from cracker.utils import get_logger, deep_dict_merge
 
 
 class Configuration:
     """Holds configuration values for the application."""
 
     singleton = None
     _logger = get_logger(__name__)
 
     language_file = "voices.json"
     DEFAULT_CONFIG_PATH = "config/default.yaml"
     USER_CONFIG_DIR_PATH = os.path.expanduser("~/.config/cracker")
 
     languages = []
-    default_values = {}  # Additional values
 
     speaker = None
     language = None
     voice = None
     voices = []
     speed = 0
     credentials_file = {}
 
     regex_config = None
+    raw_config: Optional[Dict] = None
 
     def __new__(cls, *args, **kwargs):
         if not cls.singleton:
             cls.singleton = object.__new__(Configuration)
         return cls.singleton
 
     def read_config(self) -> Dict[str, Any]:
         """Reads configuration from file system.
 
-        Firstly checks whether there are any user defined config in ~/.cracker/.
+        Firstly checks whether there are any user defined config in ~/.config/cracker/.
         If config isn't there then it takes the default.
         """
         # Check defaults
         self._default_config = config = self.read_default_config()
 
         # Check if user has created config
         if os.path.isdir(self.USER_CONFIG_DIR_PATH):
             config = self._read_user_config(self.default_config)
 
-        return self.apply_config(config)
+        self.raw_config = self.apply_config(config)
+        return self.raw_config
 
     def read_default_config(self) -> Dict:
         data = pkgutil.get_data("cracker", self.DEFAULT_CONFIG_PATH)
         if data is None:
             raise FileNotFoundError(f"Could not find config file {self.DEFAULT_CONFIG_PATH}")
         return yaml.safe_load(data.decode("utf-8"))
 
     def _read_yaml(self, path: str) -> Dict:
         with open(path, "r") as f:
             return yaml.safe_load(f)
 
-    def _write_yaml(self, config: Dict, path: str):
+    def _write_yaml(self, config: Dict):
         """Writes configuration to file system."""
         with open(self.user_config_path, "w") as f:
             yaml.safe_dump(config, f)
 
     @property
     def user_config_path(self):
         return os.path.join(self.USER_CONFIG_DIR_PATH, "settings.yaml")
@@ -81,34 +82,31 @@
             self._logger.debug("Creating user dir in '%s'", self.USER_CONFIG_DIR_PATH)
             os.mkdir(self.USER_CONFIG_DIR_PATH)
 
         if not os.path.isfile(self.user_config_path):
             return config
 
         user_config = self._read_yaml(self.user_config_path)
-
-        out_config = {}
-        all_keys = set(config.keys()).union(user_config.keys())
-        for key in all_keys:
-            k_config = {**config.get(key, {}), **user_config.get(key, {})}
-            out_config[key] = k_config
+        out_config = deep_dict_merge(config, user_config)
 
         return out_config
 
-    def save_user_config(self):
+    def save_user_config(self, extra_config: Optional[Dict] = None) -> None:
         assert self.default_config
         config = self._read_user_config(self.default_config)
 
         config["cracker"] = {
             "speaker": self.speaker or self.default_config["cracker"]["speaker"],
             "language": self.language or self.default_config["cracker"]["language"],
             "speed": str(self.speed) or self.default_config["cracker"]["speed"],
             "voice": self.voice or self.default_config["cracker"].get("voice", ""),
         }
-        self._write_yaml(config, self.user_config_path)
+        if extra_config is not None:
+            config = deep_dict_merge(config, extra_config)
+        self._write_yaml(config)
 
     def apply_config(self, configuration: Dict) -> Dict[str, Any]:
         """Applies parsed config to Cracker and UI components.
 
         Returns:
             Dict of the most important values which might be used by other components.
             This includes: speaker, language, speed and voices with their settings.
@@ -124,37 +122,36 @@
         _config["speed"] = self.speed = int(config["speed"])
         _config["voice"] = self.voice = config_speakers[self.speaker.lower()].get("voice", "")
 
         # Augment setting based on speaker
         speaker_config = self.load_speaker_config(self.speaker, self.language)
         _config.update(speaker_config)
 
-        # 
+        #
         for speaker, s_config in configuration["speakers"].items():
             self._logger.debug(speaker)
             _config[speaker.lower()] = {
                 "voice": s_config["voice"],
                 "credentials_file": s_config.get("credentials_file", ""),
             }
 
         # Check for different than default AWS profile_name
-        if self.speaker == "polly" and "profile_name" in config_speakers["polly"]:
-            self.default_values["profile_name"] = config_speakers["polly"]["profile_name"]
+        _config["polly"]["profile_name"] = config_speakers.get("polly", {}).get("profile_name", "default")
 
         if self.voice not in self.lang_voices:
             _config["voice"] = self.voice = self.lang_voices[0]
 
         if self.parser_config_path is not None:
             self.regex_config = self.load_regex_config()
 
         return _config
 
     def load_speaker_config(self, speaker, language=None):
         """Loads speaker's default and available configuration.
-        
+
         Args:
             speaker: Name of the speaker.
             language: Language to be used. If None then the default language is used.
 
         Returns:
             Dict with available configuration for the speaker, e.g. all voices and languages.
 
@@ -175,8 +172,7 @@
         """From provided path to a config it extracts configuration for the TextParser"""
         regex_config = None
         file_content = pkgutil.get_data("cracker", self.parser_config_path)
         if file_content is None:
             raise FileNotFoundError(f"Could not find config file {self.parser_config_path}")
         regex_config = json.loads(file_content.decode("utf-8"))["parser_rules"]
         return regex_config
-
```

### Comparing `cracker-0.6.0/cracker/config/parser.json` & `cracker-0.7.0/cracker/config/parser.json`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/cracker.py` & `cracker-0.7.0/cracker/cracker.py`

 * *Files 6% similar despite different names*

```diff
@@ -47,28 +47,24 @@
         self.key_manager.stop()
 
     def get_speaker(self, speaker_name, player) -> AbstractSpeaker:
         config = self.config.read_config()
         _name = speaker_name.lower()
         if _name == Polly.__name__.lower():
             self._logger.info("Using AWS Polly")
-            profile_name = config.get("polly", {}).get("profile_name", "default")
-            self._logger.debug("Using AWS profile: %s", profile_name)
-            return Polly(player, profile_name)
+            return Polly(player)
         elif _name == Google.__name__.lower():
             self._logger.info("Using Google TTS")
             credentials_file = config.get("google", {}).get("credentials_file")
             self._logger.debug("Using credentials file: %s", credentials_file)
             return Google(player, credentials_file)
         elif _name == Espeak.__name__.lower():
             self._logger.info("Using ESpeak")
             return Espeak(player)
-        raise ValueError(
-            f"No speaker was selected. Provided speaker name '{speaker_name}'"
-        )
+        raise ValueError(f"No speaker was selected. Provided speaker name '{speaker_name}'")
 
     def run(self):
         self.gui.init()
         self.set_action()
         self.gui.show()
 
     def reduce_text(self):
@@ -123,33 +119,29 @@
         else:
             self.player.pause()
 
     def stop_text(self):
         self.speaker.stop_text()
 
     def _prepare_config(self):
-        config = dict(
-            rate=self.gui.rate, volume=self.gui.volume, voice=self.gui.config.voice
-        )
+        config = dict(rate=self.gui.rate, volume=self.gui.volume, voice=self.gui.config.voice)
         return config
 
     def change_speaker(self, speaker_name):
         """Action on changing speaker.
 
         Important: Each speaker has its own configuration. These values should be updated on change.
         """
         self.speaker = self.SPEAKER[speaker_name](self.player)
         self.gui.change_speaker(speaker_name)
 
     def set_action(self):
         self.gui.stop_action.triggered.connect(self.stop_text)
         self.gui.read_action.triggered.connect(self.read_text_area)
-        self.gui.clipboard_read_action.triggered.connect(
-            self.toggle_read_text_clipboard
-        )
+        self.gui.clipboard_read_action.triggered.connect(self.toggle_read_text_clipboard)
         self.gui.toggle_action.triggered.connect(self.toggle_read)
         self.gui.reduce_action.triggered.connect(self.reduce_text)
         self.gui.wiki_action.triggered.connect(self.wiki_text)
         self.gui.speakerW.currentTextChanged.connect(self.change_speaker)
 
         self.key_manager.GlobalReadSignal.connect(self.toggle_read_text_clipboard)
```

### Comparing `cracker-0.6.0/cracker/cracker_gui.py` & `cracker-0.7.0/cracker/cracker_gui.py`

 * *Files 0% similar despite different names*

```diff
@@ -141,17 +141,15 @@
         # Speaker - label and widget
         assert self.config.speaker, "Speaker needs to be defined"
 
         self.speakerLabel = QLabel("Speaker:")
         self.speakerW = QComboBox(self)
         self.speakerW.addItems(self.speakers.keys())
         self.speakerW.setMinimumContentsLength(10)
-        self.speakerW.setCurrentIndex(
-            list(self.speakers.keys()).index(self.config.speaker.capitalize())
-        )
+        self.speakerW.setCurrentIndex(list(self.speakers.keys()).index(self.config.speaker.capitalize()))
         self.speakerW.currentTextChanged.connect(self.change_speaker)
         menuLayout.addWidget(self.speakerLabel, 0, 0)
         menuLayout.addWidget(self.speakerW, 1, 0)
 
         # Voice - label and selector
         self.speedLabel = QLabel("Speed:")
         self.speedW = QSpinBox()
```

### Comparing `cracker-0.6.0/cracker/icon.jpeg` & `cracker-0.7.0/cracker/icon.jpeg`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/icon.png` & `cracker-0.7.0/cracker/icon.png`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/keylogger.py` & `cracker-0.7.0/cracker/keylogger.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/main.py` & `cracker-0.7.0/cracker/main.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/mp3_helper.py` & `cracker-0.7.0/cracker/mp3_helper.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/speaker/__init__.py` & `cracker-0.7.0/cracker/speaker/__init__.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/speaker/abstract_speaker.py` & `cracker-0.7.0/cracker/speaker/abstract_speaker.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,23 +15,19 @@
     text_cleaners = [
         (re.compile(r"\n"), ". "),
         (re.compile(r"&"), "and"),
     ]
 
     @abc.abstractmethod
     def read_text(self, text: str, **config) -> None:
-        return NotImplementedError(
-            "Class %s doesn't implement `read_text()`" % self.__class__.__name__
-        )
+        return NotImplementedError("Class %s doesn't implement `read_text()`" % self.__class__.__name__)
 
     @abc.abstractmethod
     def stop_text(self) -> None:
-        return NotImplementedError(
-            "Class %s doesn't implement `stop_text()`" % self.__class__.__name__
-        )
+        return NotImplementedError("Class %s doesn't implement `stop_text()`" % self.__class__.__name__)
 
     @classmethod
     def clean_text(cls, text):
         text = text.translate(dict.fromkeys(range(8)))
         for compiled_regex, sub in cls.text_cleaners:
             text = compiled_regex.sub(sub, text)
         return text
```

### Comparing `cracker-0.6.0/cracker/speaker/espeak.py` & `cracker-0.7.0/cracker/speaker/espeak.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/speaker/google.py` & `cracker-0.7.0/cracker/speaker/google.py`

 * *Files 8% similar despite different names*

```diff
@@ -28,17 +28,15 @@
         self.player = player
 
     def _connect_google(self, credentials_file=None):
         try:
             if credentials_file is not None:
                 self._logger.info("Using credentials file: %s", credentials_file)
                 full_path = os.path.expanduser(credentials_file)
-                self.client = texttospeech.TextToSpeechClient.from_service_account_json(
-                    full_path
-                )
+                self.client = texttospeech.TextToSpeechClient.from_service_account_json(full_path)
             else:
                 self._logger.info("Using default credentials file")
                 self.client = texttospeech.TextToSpeechClient()
         except Exception as e:
             self._logger.exception(
                 "Unable to connect to Google with the credentials file '%s'. "
                 "Please verify that configuration file exists.",
@@ -63,21 +61,17 @@
             response = self.ask_google(parted_text, voice)
             filename = create_filename(AbstractSpeaker.TMP_FILEPATH, idx)
             saved_filepath = save_mp3(response.audio_content, filename)
             filepaths.append(saved_filepath)
         self.play_files(filepaths)
 
     def ask_google(self, text: str, voice):
-        audio_config = texttospeech.AudioConfig(
-            audio_encoding=texttospeech.AudioEncoding.MP3
-        )
+        audio_config = texttospeech.AudioConfig(audio_encoding=texttospeech.AudioEncoding.MP3)
         synth_speech = texttospeech.SynthesisInput(text=text)
-        response = self.client.synthesize_speech(
-            input=synth_speech, voice=voice, audio_config=audio_config
-        )
+        response = self.client.synthesize_speech(input=synth_speech, voice=voice, audio_config=audio_config)
         return response
 
     def play_files(self, filepaths):
         playlist = QMediaPlaylist(self.player)
         for filepath in filepaths:
             url = QUrl.fromLocalFile(filepath)
             playlist.addMedia(QMediaContent(url))
```

### Comparing `cracker-0.6.0/cracker/speaker/polly.py` & `cracker-0.7.0/cracker/speaker/polly.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import os
 from typing import List
 
 import boto3
 from PyQt5.QtCore import QUrl
 from PyQt5.QtMultimedia import QMediaContent, QMediaPlaylist
 
+from cracker.config import Configuration
 from cracker.mp3_helper import create_filename, save_mp3
 from cracker.speaker import POLLY_LANGUAGES
 from cracker.ssml import SSML
 from cracker.text_parser import TextParser
 from cracker.utils import get_logger
 
 from .abstract_speaker import AbstractSpeaker
@@ -20,35 +21,38 @@
     _logger = get_logger(__name__)
 
     RATES = ["x-slow", "slow", "medium", "fast", "x-fast"]
     VOLUMES = ["x-soft", "soft", "medium", "loud", "x-loud"]
 
     LANGUAGES = POLLY_LANGUAGES
 
-    def __init__(self, player, profile_name="default"):
+    def __init__(self, player):
         self._cached_ssml = SSML()
         self._cached_filepath = ""
         self._cached_voice = ""
-        self._connect_aws(profile_name)
+
+        self.config = Configuration()
+        aws_profile = self.config.read_config()["polly"]["profile_name"]
+        self._logger.debug("Using AWS profile: %s", aws_profile)
+        self._connect_aws(aws_profile)
         self.player = player
 
     def __del__(self):
         try:
             os.remove(self._cached_filepath)
         except (OSError, TypeError):
             pass
 
     def _connect_aws(self, profile_name: str):
         try:
             session = boto3.Session(profile_name=profile_name)
             self.client = session.client("polly")
         except Exception as e:
             self._logger.exception(
-                "Unable to connect to AWS with the profile '%s'. "
-                "Please verify that configuration file exists.",
+                "Unable to connect to AWS with the profile '%s'. " "Please verify that configuration file exists.",
                 profile_name,
             )
             raise e
 
     def save_cache(self, ssml: SSML, filepaths: List[str], voice):
         self._cached_ssml = ssml
         self._cached_filepaths = filepaths
```

### Comparing `cracker-0.6.0/cracker/ssml.py` & `cracker-0.7.0/cracker/ssml.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/tests/test_config.py` & `cracker-0.7.0/cracker/tests/test_config.py`

 * *Files 5% similar despite different names*

```diff
@@ -39,17 +39,15 @@
     mock_isfile.assert_called_once_with(config.user_config_path)
 
 
 @patch("cracker.config.configuration.os.path.isfile", return_value=True)
 @patch("cracker.config.configuration.os.path.isdir", return_value=True)
 def test_read_user_config_dir_file_exist(mock_isdir, mock_isfile):
     config = Configuration()
-    test_config = {
-        "cracker": {"speaker": "polly", "language": "Polish", "voice": "Maria"}
-    }
+    test_config = {"cracker": {"speaker": "polly", "language": "Polish", "voice": "Maria"}}
     config._read_yaml = MagicMock(return_value=test_config)
 
     out = config._read_user_config(
         {
             "cracker": {
                 "speaker": "polly",
                 "language": "English",
@@ -94,10 +92,9 @@
         {
             "cracker": {
                 "speaker": "polly",
                 "language": "English",
                 "speed": "2",
                 "voice": "Joanna",
             }
-        },
-        config.user_config_path,
+        }
     )
```

### Comparing `cracker-0.6.0/cracker/tests/test_text_parser.py` & `cracker-0.7.0/cracker/tests/test_text_parser.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/text_parser.py` & `cracker-0.7.0/cracker/text_parser.py`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/cracker/themes.py` & `cracker-0.7.0/cracker/themes.py`

 * *Files 0% similar despite different names*

```diff
@@ -7126,19 +7126,15 @@
     qt_resource_struct = qt_resource_struct_v1
 else:
     rcc_version = 2
     qt_resource_struct = qt_resource_struct_v2
 
 
 def qInitResources():
-    QtCore.qRegisterResourceData(
-        rcc_version, qt_resource_struct, qt_resource_name, qt_resource_data
-    )
+    QtCore.qRegisterResourceData(rcc_version, qt_resource_struct, qt_resource_name, qt_resource_data)
 
 
 def qCleanupResources():
-    QtCore.qUnregisterResourceData(
-        rcc_version, qt_resource_struct, qt_resource_name, qt_resource_data
-    )
+    QtCore.qUnregisterResourceData(rcc_version, qt_resource_struct, qt_resource_name, qt_resource_data)
 
 
 qInitResources()
```

### Comparing `cracker-0.6.0/cracker/view/config_window.py` & `cracker-0.7.0/cracker/view/parser_config_tab.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,56 +1,42 @@
 import json
 import logging
 import pkgutil
 from typing import Any, Dict, Optional
 
-from PyQt5.QtWidgets import QCheckBox, QGridLayout, QLabel, QLineEdit, QPushButton, QWidget
-
+from PyQt5.QtWidgets import QCheckBox, QGridLayout, QLabel, QLineEdit, QWidget
 from cracker.config import Configuration
 
 
-class ConfigWindow(QWidget):
+class ParserConfig(QWidget):
     _logger = logging.getLogger(__name__)
 
-    option_row_offset = 1
-
-    def __init__(self):
+    def __init__(self, regex_file_path=""):
         super().__init__()
 
         self.config = Configuration()
 
-        self.regex_file_path = ""
+        self.regex_file_path = regex_file_path
         self.regex_config = {}
-        self.setWindowTitle("Configuration")
+        # self.setWindowTitle("Configuration")
 
-        self._layout = QGridLayout()
-        self.setLayout(self._layout)
-
-        self.cancel_btn = QPushButton("Cancel")
-        self.cancel_btn.released.connect(self.cancel_action)
-        self.confirm_btn = QPushButton("Ok")
-        self.confirm_btn.released.connect(self.confirm_action)
-        self._layout.addWidget(self.cancel_btn, 1, 3)
-        self._layout.addWidget(self.confirm_btn, 1, 4)
-
-        self.resize(500, self.height())
+        self.layout = QGridLayout()
+        self.setLayout(self.layout)
 
     def init(self, regex_file_path=""):
         self.regex_file_path = regex_file_path
 
         self.regex_config = self.refresh_reduce_rules()
         self.create_options(self.regex_config)
 
-    def cancel_action(self):
-        self.hide()
-
     def confirm_action(self):
         self.check_update()
-        self.config.regex_config = self.get_regex_config()
-        self.hide()
+        # self.config.regex_config = self.get_regex_config()
+        # self.hide()
+        return self.get_regex_config()
 
     def clearLayout(layout):
         while layout.count():
             child = layout.takeAt(0)
             if child.widget():
                 child.widget().deleteLater()
 
@@ -74,27 +60,23 @@
             name = regex_entry["name"]
             regex_config[name] = regex_entry
 
         return regex_config
 
     def create_options(self, options):
         regex_config_options = RegexConfigOptions(options)
-        self._layout.addWidget(regex_config_options, 0, 0, 1, 5)
+        self.layout.addWidget(regex_config_options, 0, 0, 1, 5)
 
     def check_update(self) -> None:
         """Iterate through every option and see it they're active"""
         assert self.regex_config, "Regex config hasn't been loaded"
         regex_config_options_layout = self.layout.itemAtPosition(0, 0).widget().layout
         for row in range(1, regex_config_options_layout.rowCount()):
-            active_box = regex_config_options_layout.itemAtPosition(
-                row, RegexConfigOptions.ACTIVE_POS
-            ).widget()
-            name_widget = regex_config_options_layout.itemAtPosition(
-                row, RegexConfigOptions.NAME_POS
-            ).widget()
+            active_box = regex_config_options_layout.itemAtPosition(row, RegexConfigOptions.ACTIVE_POS).widget()
+            name_widget = regex_config_options_layout.itemAtPosition(row, RegexConfigOptions.NAME_POS).widget()
             name = name_widget.text()
             if name in self.regex_config:
                 self.regex_config[name]["active"] = active_box.isChecked()
 
     def get_regex_config(self):
         assert self.regex_config, "Regex config hasn't been loaded"
         return self.regex_config.values()
```

### Comparing `cracker-0.6.0/cracker.egg-info/PKG-INFO` & `cracker-0.7.0/cracker.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cracker
-Version: 0.6.0
+Version: 0.7.0
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 Provides-Extra: build
 Provides-Extra: test
 License-File: LICENSE
 
 # Cracker
```

### Comparing `cracker-0.6.0/cracker.egg-info/SOURCES.txt` & `cracker-0.7.0/cracker.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -32,10 +32,13 @@
 cracker/speaker/espeak.py
 cracker/speaker/google.py
 cracker/speaker/polly.py
 cracker/tests/test_config.py
 cracker/tests/test_text_parser.py
 cracker/view/__init__.py
 cracker/view/config_window.py
+cracker/view/parser_config_tab.py
+cracker/view/speaker_config_tab.py
+docs/macos.md
 ubuntu/cracker.desktop
 ubuntu/icon.png
 ubuntu/install_ubuntu.sh
```

### Comparing `cracker-0.6.0/pyproject.toml` & `cracker-0.7.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -32,15 +32,15 @@
 include = ["cracker*"]
 
 [tool.isort]
 line_length = 120
 profile = "black"
 
 [tool.black]
-max-line-length = 120
+line-length = 120
 
 [tool.pytest.ini_options]
 addopts = "-p no:warnings"
 filterwarnings = [
     #"error",
     #"ignore::UserWarning",
     # note the use of single quote below to denote "raw" strings in TOML
```

### Comparing `cracker-0.6.0/ubuntu/icon.png` & `cracker-0.7.0/ubuntu/icon.png`

 * *Files identical despite different names*

### Comparing `cracker-0.6.0/ubuntu/install_ubuntu.sh` & `cracker-0.7.0/ubuntu/install_ubuntu.sh`

 * *Files identical despite different names*

