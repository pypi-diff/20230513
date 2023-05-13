# Comparing `tmp/dbterd-1.2.0b4.tar.gz` & `tmp/dbterd-1.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dbterd-1.2.0b4.tar", max compression
+gzip compressed data, was "dbterd-1.2.1.tar", max compression
```

## Comparing `dbterd-1.2.0b4.tar` & `dbterd-1.2.1.tar`

### file list

```diff
@@ -1,41 +1,41 @@
--rw-r--r--   0        0        0      203 2023-05-05 06:58:50.218731 dbterd-1.2.0b4/LICENSE
--rw-r--r--   0        0        0     2972 2023-05-05 06:58:50.218731 dbterd-1.2.0b4/README.md
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/__init__.py
--rw-r--r--   0        0        0       37 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/__main__.py
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/__init__.py
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/algos/__init__.py
--rw-r--r--   0        0        0     4801 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/algos/base.py
--rw-r--r--   0        0        0     3157 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/algos/filter.py
--rw-r--r--   0        0        0      592 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/algos/meta.py
--rw-r--r--   0        0        0     4558 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/algos/test_relationship.py
--rw-r--r--   0        0        0     2575 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/base.py
--rw-r--r--   0        0        0      560 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/factory.py
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/__init__.py
--rw-r--r--   0        0        0      306 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/constants.py
--rw-r--r--   0        0        0      296 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/d2/__init__.py
--rw-r--r--   0        0        0     1591 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/d2/d2_test_relationship.py
--rw-r--r--   0        0        0      304 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/dbml/__init__.py
--rw-r--r--   0        0        0     2167 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/dbml/dbml_test_relationship.py
--rw-r--r--   0        0        0      168 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/default.py
--rw-r--r--   0        0        0      320 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/graphviz/__init__.py
--rw-r--r--   0        0        0     2778 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
--rw-r--r--   0        0        0      316 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/mermaid/__init__.py
--rw-r--r--   0        0        0     2162 2023-05-05 06:58:50.222731 dbterd-1.2.0b4/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
--rw-r--r--   0        0        0      320 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/adapters/targets/plantuml/__init__.py
--rw-r--r--   0        0        0     2012 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
--rw-r--r--   0        0        0      222 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/adapters/worker.py
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/cli/__init__.py
--rw-r--r--   0        0        0     2026 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/cli/main.py
--rw-r--r--   0        0        0     1928 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/cli/params.py
--rw-r--r--   0        0        0      164 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/constants.py
--rw-r--r--   0        0        0      284 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/default.py
--rw-r--r--   0        0        0        0 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/__init__.py
--rw-r--r--   0        0        0      721 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/cli_messaging.py
--rw-r--r--   0        0        0      877 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/dict.py
--rw-r--r--   0        0        0     4494 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/file.py
--rw-r--r--   0        0        0     1022 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/jsonify.py
--rw-r--r--   0        0        0      976 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/log.py
--rw-r--r--   0        0        0     1605 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/helpers/yaml.py
--rw-r--r--   0        0        0       94 2023-05-05 06:58:50.226731 dbterd-1.2.0b4/dbterd/main.py
--rw-r--r--   0        0        0     2097 2023-05-05 06:59:07.858634 dbterd-1.2.0b4/pyproject.toml
--rw-r--r--   0        0        0     4021 1970-01-01 00:00:00.000000 dbterd-1.2.0b4/PKG-INFO
+-rw-r--r--   0        0        0      203 2023-05-13 04:22:36.666970 dbterd-1.2.1/LICENSE
+-rw-r--r--   0        0        0     3217 2023-05-13 04:22:36.666970 dbterd-1.2.1/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/__init__.py
+-rw-r--r--   0        0        0       37 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/__main__.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/__init__.py
+-rw-r--r--   0        0        0     4801 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/base.py
+-rw-r--r--   0        0        0     3157 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/filter.py
+-rw-r--r--   0        0        0      592 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/meta.py
+-rw-r--r--   0        0        0     4558 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/algos/test_relationship.py
+-rw-r--r--   0        0        0     2575 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/base.py
+-rw-r--r--   0        0        0      560 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/factory.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/__init__.py
+-rw-r--r--   0        0        0      306 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/constants.py
+-rw-r--r--   0        0        0      296 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/d2/__init__.py
+-rw-r--r--   0        0        0     1591 2023-05-13 04:22:36.670970 dbterd-1.2.1/dbterd/adapters/targets/d2/d2_test_relationship.py
+-rw-r--r--   0        0        0      304 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/dbml/__init__.py
+-rw-r--r--   0        0        0     2167 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/dbml/dbml_test_relationship.py
+-rw-r--r--   0        0        0      168 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/default.py
+-rw-r--r--   0        0        0      320 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/graphviz/__init__.py
+-rw-r--r--   0        0        0     2778 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py
+-rw-r--r--   0        0        0      316 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/mermaid/__init__.py
+-rw-r--r--   0        0        0     2162 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py
+-rw-r--r--   0        0        0      320 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/plantuml/__init__.py
+-rw-r--r--   0        0        0     2012 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py
+-rw-r--r--   0        0        0      222 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/adapters/worker.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/__init__.py
+-rw-r--r--   0        0        0     2026 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/main.py
+-rw-r--r--   0        0        0     1928 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/cli/params.py
+-rw-r--r--   0        0        0      164 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/constants.py
+-rw-r--r--   0        0        0      284 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/default.py
+-rw-r--r--   0        0        0        0 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/__init__.py
+-rw-r--r--   0        0        0      721 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/cli_messaging.py
+-rw-r--r--   0        0        0      877 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/dict.py
+-rw-r--r--   0        0        0     4494 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/file.py
+-rw-r--r--   0        0        0     1022 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/jsonify.py
+-rw-r--r--   0        0        0      976 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/log.py
+-rw-r--r--   0        0        0     1605 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/helpers/yaml.py
+-rw-r--r--   0        0        0       94 2023-05-13 04:22:36.674970 dbterd-1.2.1/dbterd/main.py
+-rw-r--r--   0        0        0     2061 2023-05-13 04:22:52.348138 dbterd-1.2.1/pyproject.toml
+-rw-r--r--   0        0        0     4230 1970-01-01 00:00:00.000000 dbterd-1.2.1/PKG-INFO
```

### Comparing `dbterd-1.2.0b4/README.md` & `dbterd-1.2.1/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # dbterd
 
-CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/d), [Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML](https://plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2](https://d2lang.com/)) from dbt artifact files (required: `manifest.json`, `catalog.json`)
+CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/d), [Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML](https://plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2](https://d2lang.com/)) from dbt artifact files (required: [![dbt](https://img.shields.io/badge/manifest.json-upto--v9-3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/) [![dbt](https://img.shields.io/badge/catalog.json-upto--v1-3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/))
 
 [![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://pypi.org/project/dbterd/)
 ![python-cli](https://img.shields.io/badge/CLI-Python-FFCE3E?labelColor=14354C&logo=python&logoColor=white)
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
 [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
 [![codecov](https://codecov.io/gh/datnguye/dbterd/branch/main/graph/badge.svg?token=N7DMQBLH4P)](https://codecov.io/gh/datnguye/dbterd)
```

#### html2text {}

```diff
@@ -1,16 +1,20 @@
 # dbterd CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/
 d), [Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML]
 (https://plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2]
-(https://d2lang.com/)) from dbt artifact files (required: `manifest.json`,
-`catalog.json`) [![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://
-pypi.org/project/dbterd/) ![python-cli](https://img.shields.io/badge/CLI-
-Python-FFCE3E?labelColor=14354C&logo=python&logoColor=white) [![License: MIT]
-(https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/
-licenses/MIT) [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-
+(https://d2lang.com/)) from dbt artifact files (required: [![dbt](https://
+img.shields.io/badge/manifest.json-upto--v9-
+3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/)
+[![dbt](https://img.shields.io/badge/catalog.json-upto--v1-
+3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/))
+[![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://pypi.org/
+project/dbterd/) ![python-cli](https://img.shields.io/badge/CLI-Python-
+FFCE3E?labelColor=14354C&logo=python&logoColor=white) [![License: MIT](https://
+img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/
+MIT) [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-
 3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org) [!
 [codecov](https://codecov.io/gh/datnguye/dbterd/branch/main/graph/
 badge.svg?token=N7DMQBLH4P)](https://codecov.io/gh/datnguye/dbterd) ```bash pip
 install dbterd --upgrade ``` Verify installed version: ```bash dbterd --version
 ``` ## Quick examine with existing samples ```bash # select all models in
 dbt_resto dbterd run -ad samples/dbtresto # select all models in dbt_resto,
 Select multiple dbt resources dbterd run -ad samples/dbtresto -rt model -rt
```

### Comparing `dbterd-1.2.0b4/dbterd/adapters/algos/base.py` & `dbterd-1.2.1/dbterd/adapters/algos/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/algos/filter.py` & `dbterd-1.2.1/dbterd/adapters/algos/filter.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/algos/meta.py` & `dbterd-1.2.1/dbterd/adapters/algos/meta.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/algos/test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/algos/test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/base.py` & `dbterd-1.2.1/dbterd/adapters/base.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/factory.py` & `dbterd-1.2.1/dbterd/adapters/factory.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/targets/d2/d2_test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/targets/d2/d2_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/targets/dbml/dbml_test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/targets/dbml/dbml_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/targets/graphviz/graphviz_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/targets/mermaid/mermaid_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py` & `dbterd-1.2.1/dbterd/adapters/targets/plantuml/plantuml_test_relationship.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/cli/main.py` & `dbterd-1.2.1/dbterd/cli/main.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/cli/params.py` & `dbterd-1.2.1/dbterd/cli/params.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/cli_messaging.py` & `dbterd-1.2.1/dbterd/helpers/cli_messaging.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/dict.py` & `dbterd-1.2.1/dbterd/helpers/dict.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/file.py` & `dbterd-1.2.1/dbterd/helpers/file.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/jsonify.py` & `dbterd-1.2.1/dbterd/helpers/jsonify.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/log.py` & `dbterd-1.2.1/dbterd/helpers/log.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/dbterd/helpers/yaml.py` & `dbterd-1.2.1/dbterd/helpers/yaml.py`

 * *Files identical despite different names*

### Comparing `dbterd-1.2.0b4/pyproject.toml` & `dbterd-1.2.1/pyproject.toml`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "dbterd"
-version = "1.2.0b4"
-description = "dbterd is a Command Line Interface (CLI) to convert dbt manifest.json file to diagram file"
+version = "1.2.1"
+description = "CLI to generate ERD Diagram file from dbt artifact files"
 authors = ["Dat Nguyen <datnguyen.it09@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/datnguye/dbterd"
 repository = "https://github.com/datnguye/dbterd"
 keywords = ["flake8", "markdown", "lint"]
 classifiers = [
@@ -25,15 +25,15 @@
 
 [tool.poetry.scripts]
 dbterd = "dbterd.main:main"
 
 [tool.poetry.dependencies]
 python = "^3.9"
 click = "^8.1.3"
-dbt-artifacts-parser = "^0.2.3"
+dbt-artifacts-parser = "^0.3.1"
 
 [tool.poetry.group.dev.dependencies]
 pytest = "^6.2.5"
 pytest-sugar = "^0.9.6"
 black = "^22.10.0"
 coverage = {version = "^6.5.0", extras = ["toml"]}
 poethepoet = "^0.16.4"
```

### Comparing `dbterd-1.2.0b4/PKG-INFO` & `dbterd-1.2.1/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: dbterd
-Version: 1.2.0b4
-Summary: dbterd is a Command Line Interface (CLI) to convert dbt manifest.json file to diagram file
+Version: 1.2.1
+Summary: CLI to generate ERD Diagram file from dbt artifact files
 Home-page: https://github.com/datnguye/dbterd
 License: MIT
 Keywords: flake8,markdown,lint
 Author: Dat Nguyen
 Author-email: datnguyen.it09@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Environment :: Console
@@ -15,21 +15,21 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Documentation
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Topic :: Software Development :: Quality Assurance
 Requires-Dist: click (>=8.1.3,<9.0.0)
-Requires-Dist: dbt-artifacts-parser (>=0.2.3,<0.3.0)
+Requires-Dist: dbt-artifacts-parser (>=0.3.1,<0.4.0)
 Project-URL: Repository, https://github.com/datnguye/dbterd
 Description-Content-Type: text/markdown
 
 # dbterd
 
-CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/d), [Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML](https://plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2](https://d2lang.com/)) from dbt artifact files (required: `manifest.json`, `catalog.json`)
+CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/d), [Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML](https://plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2](https://d2lang.com/)) from dbt artifact files (required: [![dbt](https://img.shields.io/badge/manifest.json-upto--v9-3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/) [![dbt](https://img.shields.io/badge/catalog.json-upto--v1-3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/))
 
 [![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://pypi.org/project/dbterd/)
 ![python-cli](https://img.shields.io/badge/CLI-Python-FFCE3E?labelColor=14354C&logo=python&logoColor=white)
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
 [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
 [![codecov](https://codecov.io/gh/datnguye/dbterd/branch/main/graph/badge.svg?token=N7DMQBLH4P)](https://codecov.io/gh/datnguye/dbterd)
```

#### html2text {}

```diff
@@ -1,30 +1,33 @@
-Metadata-Version: 2.1 Name: dbterd Version: 1.2.0b4 Summary: dbterd is a
-Command Line Interface (CLI) to convert dbt manifest.json file to diagram file
-Home-page: https://github.com/datnguye/dbterd License: MIT Keywords:
-flake8,markdown,lint Author: Dat Nguyen Author-email: datnguyen.it09@gmail.com
-Requires-Python: >=3.9,<4.0 Classifier: Environment :: Console Classifier:
-License :: OSI Approved :: MIT License Classifier: Operating System :: OS
-Independent Classifier: Programming Language :: Python :: 3 Classifier:
-Programming Language :: Python :: 3.9 Classifier: Programming Language ::
-Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Classifier:
-Topic :: Software Development :: Documentation Classifier: Topic :: Software
-Development :: Libraries :: Python Modules Classifier: Topic :: Software
-Development :: Quality Assurance Requires-Dist: click (>=8.1.3,<9.0.0)
-Requires-Dist: dbt-artifacts-parser (>=0.2.3,<0.3.0) Project-URL: Repository,
-https://github.com/datnguye/dbterd Description-Content-Type: text/markdown #
-dbterd CLI to generate Diagram-as-a-code file ([DBML](https://dbdiagram.io/d),
-[Mermaid](https://mermaid-js.github.io/mermaid-live-editor/), [PlantUML](https:
-//plantuml.com/ie-diagram), [GraphViz](https://graphviz.org/), [D2](https://
-d2lang.com/)) from dbt artifact files (required: `manifest.json`,
-`catalog.json`) [![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://
-pypi.org/project/dbterd/) ![python-cli](https://img.shields.io/badge/CLI-
-Python-FFCE3E?labelColor=14354C&logo=python&logoColor=white) [![License: MIT]
-(https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/
-licenses/MIT) [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-
+Metadata-Version: 2.1 Name: dbterd Version: 1.2.1 Summary: CLI to generate ERD
+Diagram file from dbt artifact files Home-page: https://github.com/datnguye/
+dbterd License: MIT Keywords: flake8,markdown,lint Author: Dat Nguyen Author-
+email: datnguyen.it09@gmail.com Requires-Python: >=3.9,<4.0 Classifier:
+Environment :: Console Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent Classifier: Programming Language
+:: Python :: 3 Classifier: Programming Language :: Python :: 3.9 Classifier:
+Programming Language :: Python :: 3.10 Classifier: Programming Language ::
+Python :: 3.11 Classifier: Topic :: Software Development :: Documentation
+Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Classifier: Topic :: Software Development :: Quality Assurance Requires-Dist:
+click (>=8.1.3,<9.0.0) Requires-Dist: dbt-artifacts-parser (>=0.3.1,<0.4.0)
+Project-URL: Repository, https://github.com/datnguye/dbterd Description-
+Content-Type: text/markdown # dbterd CLI to generate Diagram-as-a-code file (
+[DBML](https://dbdiagram.io/d), [Mermaid](https://mermaid-js.github.io/mermaid-
+live-editor/), [PlantUML](https://plantuml.com/ie-diagram), [GraphViz](https://
+graphviz.org/), [D2](https://d2lang.com/)) from dbt artifact files (required:
+[![dbt](https://img.shields.io/badge/manifest.json-upto--v9-
+3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/)
+[![dbt](https://img.shields.io/badge/catalog.json-upto--v1-
+3776AB.svg?style=flat&logo=dbt&logoColor=orange)](https://schemas.getdbt.com/))
+[![PyPI version](https://badge.fury.io/py/dbterd.svg)](https://pypi.org/
+project/dbterd/) ![python-cli](https://img.shields.io/badge/CLI-Python-
+FFCE3E?labelColor=14354C&logo=python&logoColor=white) [![License: MIT](https://
+img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/
+MIT) [![python](https://img.shields.io/badge/Python-3.9|3.10|3.11-
 3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org) [!
 [codecov](https://codecov.io/gh/datnguye/dbterd/branch/main/graph/
 badge.svg?token=N7DMQBLH4P)](https://codecov.io/gh/datnguye/dbterd) ```bash pip
 install dbterd --upgrade ``` Verify installed version: ```bash dbterd --version
 ``` ## Quick examine with existing samples ```bash # select all models in
 dbt_resto dbterd run -ad samples/dbtresto # select all models in dbt_resto,
 Select multiple dbt resources dbterd run -ad samples/dbtresto -rt model -rt
```

