# Comparing `tmp/parquet_tools-0.2.8.tar.gz` & `tmp/parquet_tools-0.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "parquet_tools-0.2.8.tar", last modified: Thu Aug 26 16:16:41 2021, max compression
+gzip compressed data, was "parquet_tools-0.2.9.tar", last modified: Tue Aug 31 11:55:18 2021, max compression
```

## Comparing `parquet_tools-0.2.8.tar` & `parquet_tools-0.2.9.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0     1079 2021-08-22 13:26:41.940241 parquet_tools-0.2.8/LICENSE.txt
--rw-r--r--   0        0        0     2881 2021-08-22 13:28:51.254279 parquet_tools-0.2.8/README.md
--rw-r--r--   0        0        0       89 2020-08-01 16:10:41.986741 parquet_tools-0.2.8/parquet_tools/__init__.py
--rw-r--r--   0        0        0      940 2021-06-11 17:00:06.837549 parquet_tools-0.2.8/parquet_tools/cli.py
--rw-r--r--   0        0        0        0 2020-06-10 12:29:01.316104 parquet_tools-0.2.8/parquet_tools/commands/__init__.py
--rw-r--r--   0        0        0     2370 2021-06-30 11:10:50.199843 parquet_tools-0.2.8/parquet_tools/commands/csv.py
--rw-r--r--   0        0        0     4368 2021-08-26 16:15:13.145308 parquet_tools-0.2.8/parquet_tools/commands/inspect.py
--rw-r--r--   0        0        0     2968 2021-06-11 17:00:06.840213 parquet_tools-0.2.8/parquet_tools/commands/show.py
--rw-r--r--   0        0        0     6345 2021-06-11 17:00:06.841052 parquet_tools-0.2.8/parquet_tools/commands/utils.py
--rw-r--r--   0        0        0        0 2020-08-01 16:10:41.987456 parquet_tools-0.2.8/parquet_tools/gen_py/__init__.py
--rw-r--r--   0        0        0       34 2020-08-01 16:10:41.988557 parquet_tools-0.2.8/parquet_tools/gen_py/parquet/__init__.py
--rw-r--r--   0        0        0      366 2020-08-01 16:10:41.989214 parquet_tools-0.2.8/parquet_tools/gen_py/parquet/constants.py
--rw-r--r--   0        0        0   184602 2020-08-01 16:10:41.991849 parquet_tools-0.2.8/parquet_tools/gen_py/parquet/ttypes.py
--rw-r--r--   0        0        0        0 2020-08-01 16:10:41.993083 parquet_tools-0.2.8/parquet_tools/parquet/__init__.py
--rw-r--r--   0        0        0      868 2020-08-01 16:10:41.994366 parquet_tools-0.2.8/parquet_tools/parquet/reader.py
--rw-r--r--   0        0        0      934 2021-08-26 16:15:27.839490 parquet_tools-0.2.8/pyproject.toml
--rw-r--r--   0        0        0     4069 2021-08-26 16:16:42.358150 parquet_tools-0.2.8/setup.py
--rw-r--r--   0        0        0     3705 2021-08-26 16:16:42.360133 parquet_tools-0.2.8/PKG-INFO
+-rw-r--r--   0        0        0     1079 2021-08-22 13:26:41.940241 parquet_tools-0.2.9/LICENSE.txt
+-rw-r--r--   0        0        0     2881 2021-08-22 13:28:51.254279 parquet_tools-0.2.9/README.md
+-rw-r--r--   0        0        0       89 2020-08-01 16:10:41.986741 parquet_tools-0.2.9/parquet_tools/__init__.py
+-rw-r--r--   0        0        0      940 2021-06-11 17:00:06.837549 parquet_tools-0.2.9/parquet_tools/cli.py
+-rw-r--r--   0        0        0        0 2020-06-10 12:29:01.316104 parquet_tools-0.2.9/parquet_tools/commands/__init__.py
+-rw-r--r--   0        0        0     2370 2021-06-30 11:10:50.199843 parquet_tools-0.2.9/parquet_tools/commands/csv.py
+-rw-r--r--   0        0        0     4368 2021-08-26 16:15:13.145308 parquet_tools-0.2.9/parquet_tools/commands/inspect.py
+-rw-r--r--   0        0        0     2968 2021-06-11 17:00:06.840213 parquet_tools-0.2.9/parquet_tools/commands/show.py
+-rw-r--r--   0        0        0     6345 2021-06-11 17:00:06.841052 parquet_tools-0.2.9/parquet_tools/commands/utils.py
+-rw-r--r--   0        0        0        0 2020-08-01 16:10:41.987456 parquet_tools-0.2.9/parquet_tools/gen_py/__init__.py
+-rw-r--r--   0        0        0       34 2020-08-01 16:10:41.988557 parquet_tools-0.2.9/parquet_tools/gen_py/parquet/__init__.py
+-rw-r--r--   0        0        0      366 2020-08-01 16:10:41.989214 parquet_tools-0.2.9/parquet_tools/gen_py/parquet/constants.py
+-rw-r--r--   0        0        0   184602 2020-08-01 16:10:41.991849 parquet_tools-0.2.9/parquet_tools/gen_py/parquet/ttypes.py
+-rw-r--r--   0        0        0        0 2020-08-01 16:10:41.993083 parquet_tools-0.2.9/parquet_tools/parquet/__init__.py
+-rw-r--r--   0        0        0      868 2020-08-01 16:10:41.994366 parquet_tools-0.2.9/parquet_tools/parquet/reader.py
+-rw-r--r--   0        0        0      915 2021-08-31 11:51:01.514265 parquet_tools-0.2.9/pyproject.toml
+-rw-r--r--   0        0        0     4040 2021-08-31 11:55:18.562605 parquet_tools-0.2.9/setup.py
+-rw-r--r--   0        0        0     3673 2021-08-31 11:55:18.563510 parquet_tools-0.2.9/PKG-INFO
```

### Comparing `parquet_tools-0.2.8/LICENSE.txt` & `parquet_tools-0.2.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/README.md` & `parquet_tools-0.2.9/README.md`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/cli.py` & `parquet_tools-0.2.9/parquet_tools/cli.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/commands/csv.py` & `parquet_tools-0.2.9/parquet_tools/commands/csv.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/commands/inspect.py` & `parquet_tools-0.2.9/parquet_tools/commands/inspect.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/commands/show.py` & `parquet_tools-0.2.9/parquet_tools/commands/show.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/commands/utils.py` & `parquet_tools-0.2.9/parquet_tools/commands/utils.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/gen_py/parquet/ttypes.py` & `parquet_tools-0.2.9/parquet_tools/gen_py/parquet/ttypes.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/parquet_tools/parquet/reader.py` & `parquet_tools-0.2.9/parquet_tools/parquet/reader.py`

 * *Files identical despite different names*

### Comparing `parquet_tools-0.2.8/pyproject.toml` & `parquet_tools-0.2.9/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,37 @@
 [tool.poetry]
 name = "parquet_tools"
-version = "0.2.8"
+version = "0.2.9"
 description = "Easy install parquet-tools"
 authors = ["Kentaro Ueda <kentaro.ueda.kentaro@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/ktrueda/parquet-tools"
 homepage = "https://github.com/ktrueda/parquet-tools"
 keywords = ["parquet-tools", "parquet"]
 exclude = ["parquet_tools/parquet.thrift", "parquet_tools/README.md"]
 
 [tool.poetry.dependencies]
 python = "^3.8"
 halo = "^0.0.29"
-pyarrow = "^0.17.1"
-pandas = "^1.0.4"
+pyarrow = "*"
+pandas = "^1"
 tabulate = "^0.8.7"
-boto3 = "^1.13.25"
+boto3 = "^1.13"
 thrift = "^0.13.0"
 colorama = "^0.4.3"
 
 [tool.poetry.dev-dependencies]
 autopep8 = "^1.5.3"
 flake8 = "^3.8.3"
 mypy = "^0.780"
 pylint = "^2.5.3"
 pytest = "^5.4.3"
 pytest-mock = "^3.1.1"
-moto = "^1.3.14"
+moto = "*"
 wheel = "^0.34.2"
 twine = "^3.1.1"
 
 [tool.poetry.scripts]
 parquet-tools = "parquet_tools.cli:main"
 [build-system]
 requires = ["poetry>=0.12"]
```

### Comparing `parquet_tools-0.2.8/setup.py` & `parquet_tools-0.2.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,28 +8,28 @@
  'parquet_tools.gen_py.parquet',
  'parquet_tools.parquet']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
-['boto3>=1.13.25,<2.0.0',
+['boto3>=1.13,<2.0',
  'colorama>=0.4.3,<0.5.0',
  'halo>=0.0.29,<0.0.30',
- 'pandas>=1.0.4,<2.0.0',
- 'pyarrow>=0.17.1,<0.18.0',
+ 'pandas>=1,<2',
+ 'pyarrow',
  'tabulate>=0.8.7,<0.9.0',
  'thrift>=0.13.0,<0.14.0']
 
 entry_points = \
 {'console_scripts': ['parquet-tools = parquet_tools.cli:main']}
 
 setup_kwargs = {
     'name': 'parquet-tools',
-    'version': '0.2.8',
+    'version': '0.2.9',
     'description': 'Easy install parquet-tools',
     'long_description': '# parquet-tools\n\n![Run Unittest](https://github.com/ktrueda/parquet-tools/workflows/Run%20Unittest/badge.svg)\n![Run CLI test](https://github.com/ktrueda/parquet-tools/workflows/Run%20CLI%20test/badge.svg)\n\nThis is a pip installable [parquet-tools](https://github.com/apache/parquet-mr).\nIn other words, parquet-tools is a CLI tools of [Apache Arrow](https://github.com/apache/arrow).\nYou can show parquet file content/schema on local disk or on Amazon S3.\nIt is incompatible with original parquet-tools.\n\n## Features\n\n- Read Parquet data (local file or file on S3)\n- Read Parquet metadata/schema (local file or file on S3)\n\n## Installation\n\n```bash\n$ pip install parquet-tools\n```\n\n## Usage\n\n```bash\n$ parquet-tools --help\nusage: parquet-tools [-h] {show,csv,inspect} ...\n\nparquet CLI tools\n\npositional arguments:\n  {show,csv,inspect}\n    show              Show human readble format. see `show -h`\n    csv               Cat csv style. see `csv -h`\n    inspect           Inspect parquet file. see `inspect -h`\n\noptional arguments:\n  -h, --help          show this help message and exit\n```\n\n## Usage Examples\n\n#### Show local parquet file\n\n```bash\n$ parquet-tools show test.parquet\n+-------+-------+---------+\n|   one | two   | three   |\n|-------+-------+---------|\n|  -1   | foo   | True    |\n| nan   | bar   | False   |\n|   2.5 | baz   | True    |\n+-------+-------+---------+\n```\n\n#### Show parquet file on S3\n\n```bash\n$ parquet-tools show s3://bucket-name/prefix/*\n+-------+-------+---------+\n|   one | two   | three   |\n|-------+-------+---------|\n|  -1   | foo   | True    |\n| nan   | bar   | False   |\n|   2.5 | baz   | True    |\n+-------+-------+---------+\n```\n\n\n#### Inspect parquet file schema\n\n```bash\n$ parquet-tools inspect /path/to/parquet\n```\n\n<details>\n\n<summary>Inspect output</summary>\n\n```\n############ file meta data ############\ncreated_by: parquet-cpp version 1.5.1-SNAPSHOT\nnum_columns: 3\nnum_rows: 3\nnum_row_groups: 1\nformat_version: 1.0\nserialized_size: 2226\n\n\n############ Columns ############\none\ntwo\nthree\n\n############ Column(one) ############\nname: one\npath: one\nmax_definition_level: 1\nmax_repetition_level: 0\nphysical_type: DOUBLE\nlogical_type: None\nconverted_type (legacy): NONE\n\n############ Column(two) ############\nname: two\npath: two\nmax_definition_level: 1\nmax_repetition_level: 0\nphysical_type: BYTE_ARRAY\nlogical_type: String\nconverted_type (legacy): UTF8\n\n############ Column(three) ############\nname: three\npath: three\nmax_definition_level: 1\nmax_repetition_level: 0\nphysical_type: BOOLEAN\nlogical_type: None\nconverted_type (legacy): NONE\n```\n</details>\n\n#### Cat CSV parquet and transform [csvq](https://github.com/mithrandie/csvq)\n\n```bash\n$ parquet-tools csv s3://bucket-name/test.parquet |csvq "select one, three where three"\n+-------+-------+\n|  one  | three |\n+-------+-------+\n| -1.0  | True  |\n| 2.5   | True  |\n+-------+-------+\n```\n',
     'author': 'Kentaro Ueda',
     'author_email': 'kentaro.ueda.kentaro@gmail.com',
     'maintainer': None,
     'maintainer_email': None,
     'url': 'https://github.com/ktrueda/parquet-tools',
```

### Comparing `parquet_tools-0.2.8/PKG-INFO` & `parquet_tools-0.2.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: parquet-tools
-Version: 0.2.8
+Version: 0.2.9
 Summary: Easy install parquet-tools
 Home-page: https://github.com/ktrueda/parquet-tools
 License: MIT
 Keywords: parquet-tools,parquet
 Author: Kentaro Ueda
 Author-email: kentaro.ueda.kentaro@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
-Requires-Dist: boto3 (>=1.13.25,<2.0.0)
+Requires-Dist: boto3 (>=1.13,<2.0)
 Requires-Dist: colorama (>=0.4.3,<0.5.0)
 Requires-Dist: halo (>=0.0.29,<0.0.30)
-Requires-Dist: pandas (>=1.0.4,<2.0.0)
-Requires-Dist: pyarrow (>=0.17.1,<0.18.0)
+Requires-Dist: pandas (>=1,<2)
+Requires-Dist: pyarrow
 Requires-Dist: tabulate (>=0.8.7,<0.9.0)
 Requires-Dist: thrift (>=0.13.0,<0.14.0)
 Project-URL: Repository, https://github.com/ktrueda/parquet-tools
 Description-Content-Type: text/markdown
 
 # parquet-tools
```

