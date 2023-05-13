# Comparing `tmp/pyjaws-0.0.8.tar.gz` & `tmp/pyjaws-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyjaws-0.0.8.tar", last modified: Sat May 13 12:55:16 2023, max compression
+gzip compressed data, was "pyjaws-0.0.9.tar", last modified: Sat May 13 14:34:05 2023, max compression
```

## Comparing `pyjaws-0.0.8.tar` & `pyjaws-0.0.9.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)     4508 2023-05-13 12:55:16.803060 pyjaws-0.0.8/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws/
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws/api/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5734 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/jobs.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/runtime.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws/api/templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws/api/templates/macros/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/templates/macros/cluster.j2
--rw-r--r--   0 runner    (1001) docker     (123)     1254 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/templates/macros/task.j2
--rw-r--r--   0 runner    (1001) docker     (123)      631 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/api/templates/workflow.j2
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws/client/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyjaws/client/entrypoint.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 12:55:16.803060 pyjaws-0.0.8/pyjaws.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4508 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      469 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 12:55:16.000000 pyjaws-0.0.8/pyjaws.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      763 2023-05-13 12:55:07.000000 pyjaws-0.0.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 12:55:16.803060 pyjaws-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      941 2023-05-13 12:55:07.000000 pyjaws-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.174948 pyjaws-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     4528 2023-05-13 14:34:05.174948 pyjaws-0.0.9/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.170948 pyjaws-0.0.9/pyjaws/
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.170948 pyjaws-0.0.9/pyjaws/api/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5756 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/jobs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/runtime.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.170948 pyjaws-0.0.9/pyjaws/api/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.174948 pyjaws-0.0.9/pyjaws/api/templates/macros/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/templates/macros/cluster.j2
+-rw-r--r--   0 runner    (1001) docker     (123)     1484 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/templates/macros/task.j2
+-rw-r--r--   0 runner    (1001) docker     (123)      631 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/api/templates/workflow.j2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.174948 pyjaws-0.0.9/pyjaws/client/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2091 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyjaws/client/entrypoint.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:05.170948 pyjaws-0.0.9/pyjaws.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4528 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      469 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       57 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-05-13 14:34:05.000000 pyjaws-0.0.9/pyjaws.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      763 2023-05-13 14:33:56.000000 pyjaws-0.0.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:34:05.174948 pyjaws-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      941 2023-05-13 14:33:56.000000 pyjaws-0.0.9/setup.py
```

### Comparing `pyjaws-0.0.8/PKG-INFO` & `pyjaws-0.0.9/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyjaws
-Version: 0.0.8
+Version: 0.0.9
 Author: Rafael Pierre
 Description-Content-Type: text/markdown
 
 # PyJaws: A Pythonic Way to Define Databricks Jobs and Workflows
 
 <p align="center">
         <img src="https://raw.githubusercontent.com/rafaelpierre/pyjaws/main/img/pyjaws.png" class="align-center" />
@@ -13,15 +13,15 @@
 
 <hr />
 
 ![python](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white) ![black](https://img.shields.io/badge/code%20style-black-000000.svg?style=for-the-badge) ![ruff](https://img.shields.io/badge/lint-ruff-gold?style=for-the-badge) ![cov](https://raw.githubusercontent.com/rafaelpierre/pyjaws/59dbf9248c65b3e3f1e66ce0ef8d6ce2218fa3b7/img/coverage.svg) ![databricks](https://img.shields.io/badge/Databricks-FF3621.svg?style=for-the-badge&logo=Databricks&logoColor=white) ![Jinja](https://img.shields.io/badge/jinja-white.svg?style=for-the-badge&logo=jinja&logoColor=black)
 
 <hr />
 
-* **PyJaws** enables declaring Databricks Jobs and Workflows as Python code, allowing for:
+* **PyJaws** enables declaring [Databricks Jobs and Workflows](https://docs.databricks.com/workflows/index.html) as Python code, allowing for:
    * Code Linting
    * Formatting
    * Parameter Validation
    * Modularity and reusability
 * In addition to those, **PyJaws** also provides some nice features such as [cycle detection](https://networkx.org/documentation/stable/reference/algorithms/cycles.html) out of the box.
 
 Folks who have used Python-based orchestration tools such as [Apache Airflow](https://airflow.apache.org/), [Luigi](https://luigi.readthedocs.io/en/stable/) and [Mage](https://pypi.org/project/mage-ai/) will be familiar with the concepts and the API if **PyJaws**.
@@ -41,15 +41,15 @@
 * **PyJaws** can be tested locally for development purposes. To run unit tests, make sure `tox`, `pytest`, `pytest-cov`, and `coverage` are installed and from a bash terminal, simply run `tox`.
 
 ## Getting Started
 
 * First step is installing `pyjaws`:
 
 ```bash
-pip install https://github.com/rafaelpierre/pyjaws
+pip install pyjaws
 ```
 
 * Once it's installed, define your Databricks Workspace authentication variables:
 
 ```bash
 export DATABRICKS_HOST = ...
 export DATABRICKS_TOKEN = ...
```

### Comparing `pyjaws-0.0.8/pyjaws/api/base.py` & `pyjaws-0.0.9/pyjaws/api/base.py`

 * *Files 2% similar despite different names*

```diff
@@ -64,14 +64,15 @@
     Params:
         key: Task key.
         existing_cluster_id: Cluster ID for running the task.
         libraries: List of Python libraries to be installed.
     """
 
     key: str
+    package_name: str
     entrypoint: str
     task_name: str
     cluster: Cluster
     parameters: List[str] = []
     dependencies: Optional[List[Task]] = None
     libraries: Optional[List[dict]] = None
```

### Comparing `pyjaws-0.0.8/pyjaws/api/jobs.py` & `pyjaws-0.0.9/pyjaws/api/jobs.py`

 * *Files 14% similar despite different names*

```diff
@@ -15,14 +15,15 @@
     logging.info(f"Creating workflow: {json_workflow}")
 
     try:
         api_client = ApiClient(
             host=os.environ["DATABRICKS_HOST"],
             token=os.environ["DATABRICKS_TOKEN"],
         )
+        logging.info(f"Deploying jobs to {os.environ['DATABRICKS_HOST']}")
         result = None
         jobs_api = JobsApi(api_client)
         existing_jobs = jobs_api._list_jobs_by_name(name=workflow.name)
 
         if overwrite and existing_jobs:
             for job in existing_jobs:
                 json_ = {
```

### Comparing `pyjaws-0.0.8/pyjaws/api/templates/macros/cluster.j2` & `pyjaws-0.0.9/pyjaws/api/templates/macros/cluster.j2`

 * *Files identical despite different names*

### Comparing `pyjaws-0.0.8/pyjaws/api/templates/macros/task.j2` & `pyjaws-0.0.9/pyjaws/api/templates/macros/task.j2`

 * *Files 22% similar despite different names*

```diff
@@ -12,24 +12,31 @@
         {% endif %}
     ],
     {% if workflow_task.cluster %}
     "job_cluster_key": "{{ workflow_task.cluster.job_cluster_key }}"
     {% elif workflow_task.existing_cluster_id %}
     "existing_cluster_id": "{{ workflow_task.existing_cluster_id }}",
     {% endif %},
+    {% if workflow_task.libraries %}
     "libraries": [
-        {% if workflow_task.libraries %}
         {% for library in workflow_task.libraries %}
-        {"{{ library.source }}": "{{ library.path }}"},
+            {% for source, target in library.items() %}
+            {% if source == "pypi" %}
+            {"pypi": {
+                "package": "{{ target['package'] }}"
+                }
+            },
+            {% endif %}
+            {% endfor %}
         {% endfor %}
-        {% endif %}
     ],
+    {% endif %}
     "python_wheel_task": {
-        "package_name": "husk",
-        "entry_point": "husk",
+        "package_name": "workflow_task.package_name",
+        "entry_point": "workflow_task.entrypoint",
         "parameters": [
             "{{ workflow_task.entrypoint }}",
             "{{ workflow_task.task_name }}",
             {% for param in workflow_task.parameters %}
             "{{ param }}",
             {% endfor %}
         ]
```

### Comparing `pyjaws-0.0.8/pyjaws/api/templates/workflow.j2` & `pyjaws-0.0.9/pyjaws/api/templates/workflow.j2`

 * *Files identical despite different names*

### Comparing `pyjaws-0.0.8/pyjaws/client/entrypoint.py` & `pyjaws-0.0.9/pyjaws/client/entrypoint.py`

 * *Files 8% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 @click.command(name="create")
 @click.argument("input_folder", type=str, default="./")
 @click.option(
     "--overwrite",
     is_flag=True,
     show_default=True,
-    default=False,
+    default=True,
     help="Overwrite existing workflow.",
 )
 def create(input_folder: str, overwrite: bool = False):
     """
     Creates a Jobs Workflow for the Python job definitions stored in
     input_folder.
```

### Comparing `pyjaws-0.0.8/pyjaws.egg-info/PKG-INFO` & `pyjaws-0.0.9/pyjaws.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyjaws
-Version: 0.0.8
+Version: 0.0.9
 Author: Rafael Pierre
 Description-Content-Type: text/markdown
 
 # PyJaws: A Pythonic Way to Define Databricks Jobs and Workflows
 
 <p align="center">
         <img src="https://raw.githubusercontent.com/rafaelpierre/pyjaws/main/img/pyjaws.png" class="align-center" />
@@ -13,15 +13,15 @@
 
 <hr />
 
 ![python](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white) ![black](https://img.shields.io/badge/code%20style-black-000000.svg?style=for-the-badge) ![ruff](https://img.shields.io/badge/lint-ruff-gold?style=for-the-badge) ![cov](https://raw.githubusercontent.com/rafaelpierre/pyjaws/59dbf9248c65b3e3f1e66ce0ef8d6ce2218fa3b7/img/coverage.svg) ![databricks](https://img.shields.io/badge/Databricks-FF3621.svg?style=for-the-badge&logo=Databricks&logoColor=white) ![Jinja](https://img.shields.io/badge/jinja-white.svg?style=for-the-badge&logo=jinja&logoColor=black)
 
 <hr />
 
-* **PyJaws** enables declaring Databricks Jobs and Workflows as Python code, allowing for:
+* **PyJaws** enables declaring [Databricks Jobs and Workflows](https://docs.databricks.com/workflows/index.html) as Python code, allowing for:
    * Code Linting
    * Formatting
    * Parameter Validation
    * Modularity and reusability
 * In addition to those, **PyJaws** also provides some nice features such as [cycle detection](https://networkx.org/documentation/stable/reference/algorithms/cycles.html) out of the box.
 
 Folks who have used Python-based orchestration tools such as [Apache Airflow](https://airflow.apache.org/), [Luigi](https://luigi.readthedocs.io/en/stable/) and [Mage](https://pypi.org/project/mage-ai/) will be familiar with the concepts and the API if **PyJaws**.
@@ -41,15 +41,15 @@
 * **PyJaws** can be tested locally for development purposes. To run unit tests, make sure `tox`, `pytest`, `pytest-cov`, and `coverage` are installed and from a bash terminal, simply run `tox`.
 
 ## Getting Started
 
 * First step is installing `pyjaws`:
 
 ```bash
-pip install https://github.com/rafaelpierre/pyjaws
+pip install pyjaws
 ```
 
 * Once it's installed, define your Databricks Workspace authentication variables:
 
 ```bash
 export DATABRICKS_HOST = ...
 export DATABRICKS_TOKEN = ...
```

### Comparing `pyjaws-0.0.8/pyproject.toml` & `pyjaws-0.0.9/pyproject.toml`

 * *Files identical despite different names*

### Comparing `pyjaws-0.0.8/setup.py` & `pyjaws-0.0.9/setup.py`

 * *Files identical despite different names*

