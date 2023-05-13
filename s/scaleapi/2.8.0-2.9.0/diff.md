# Comparing `tmp/scaleapi-2.8.0.tar.gz` & `tmp/scaleapi-2.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/scaleapi-2.8.0.tar", last modified: Wed Apr 13 21:19:44 2022, max compression
+gzip compressed data, was "dist/scaleapi-2.9.0.tar", last modified: Fri Apr 29 04:18:49 2022, max compression
```

## Comparing `scaleapi-2.8.0.tar` & `scaleapi-2.9.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-13 21:19:44.000000 scaleapi-2.8.0/
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi/
--rw-r--r--   0 circleci  (3434) circleci  (3434)    27959 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/__init__.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)       52 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/_version.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     5123 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/api.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1457 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/batches.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      298 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/evaluation_tasks.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     2304 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/exceptions.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      520 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/files.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      861 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/projects.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      651 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/quality_tasks.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     2370 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/tasks.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      288 2022-04-13 21:19:35.000000 scaleapi-2.8.0/scaleapi/training_tasks.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/
--rw-r--r--   0 circleci  (3434) circleci  (3434)    23343 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/PKG-INFO
--rw-r--r--   0 circleci  (3434) circleci  (3434)      428 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/SOURCES.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        1 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/dependency_links.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)       33 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/requires.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        9 2022-04-13 21:19:44.000000 scaleapi-2.8.0/scaleapi.egg-info/top_level.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)    17758 2022-04-13 21:19:35.000000 scaleapi-2.8.0/README.rst
--rw-r--r--   0 circleci  (3434) circleci  (3434)      224 2022-04-13 21:19:44.000000 scaleapi-2.8.0/setup.cfg
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1794 2022-04-13 21:19:35.000000 scaleapi-2.8.0/setup.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)    23343 2022-04-13 21:19:44.000000 scaleapi-2.8.0/PKG-INFO
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-29 04:18:49.000000 scaleapi-2.9.0/
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    29137 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/__init__.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)       52 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/_version.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     5362 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/api.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1457 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/batches.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      298 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/evaluation_tasks.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     2304 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/exceptions.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      520 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/files.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      861 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/projects.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      651 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/quality_tasks.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     2696 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/tasks.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      288 2022-04-29 04:18:41.000000 scaleapi-2.9.0/scaleapi/training_tasks.py
+drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    24986 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/PKG-INFO
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      428 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/SOURCES.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)        1 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/dependency_links.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)       33 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/requires.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)        9 2022-04-29 04:18:49.000000 scaleapi-2.9.0/scaleapi.egg-info/top_level.txt
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    19057 2022-04-29 04:18:41.000000 scaleapi-2.9.0/README.rst
+-rw-r--r--   0 circleci  (3434) circleci  (3434)      224 2022-04-29 04:18:49.000000 scaleapi-2.9.0/setup.cfg
+-rw-r--r--   0 circleci  (3434) circleci  (3434)     1794 2022-04-29 04:18:41.000000 scaleapi-2.9.0/setup.py
+-rw-r--r--   0 circleci  (3434) circleci  (3434)    24986 2022-04-29 04:18:49.000000 scaleapi-2.9.0/PKG-INFO
```

### Comparing `scaleapi-2.8.0/scaleapi/__init__.py` & `scaleapi-2.9.0/scaleapi/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -60,28 +60,64 @@
                 Task identifier
         Returns:
             Task:
         """
         endpoint = f"task/{task_id}"
         return Task(self.api.get_request(endpoint), self)
 
-    def cancel_task(self, task_id: str) -> Task:
+    def cancel_task(self, task_id: str, clear_unique_id: bool = False) -> Task:
         """Cancels a task and returns the associated task.
         Raises a ScaleException if it has already been canceled.
 
         Args:
             task_id (str):
                 Task id
+            clear_unique_id (boolean):
+                Option to clear unique id when the task is deleted
 
         Returns:
             Task
         """
-        endpoint = f"task/{task_id}/cancel"
+        if clear_unique_id:
+            endpoint = f"task/{task_id}/cancel?clear_unique_id=true"
+        else:
+            endpoint = f"task/{task_id}/cancel"
         return Task(self.api.post_request(endpoint), self)
 
+    def update_task_unique_id(self, task_id: str, unique_id: str) -> Task:
+        """Updates a task's unique_id and returns the associated task.
+        Raises a ScaleDuplicateResource exception if unique_id
+        is already in use.
+
+        Args:
+            task_id (str):
+                Task id
+            unique_id (str):
+                unique_id to set
+
+        Returns:
+            Task
+        """
+        payload = dict(unique_id=unique_id)
+        endpoint = f"task/{task_id}/unique_id"
+        return Task(self.api.post_request(endpoint, body=payload), self)
+
+    def clear_task_unique_id(self, task_id: str) -> Task:
+        """Clears a task's unique_id and returns the associated task.
+
+        Args:
+            task_id (str):
+                Task id
+
+        Returns:
+            Task
+        """
+        endpoint = f"task/{task_id}/unique_id"
+        return Task(self.api.delete_request(endpoint), self)
+
     def tasks(self, **kwargs) -> Tasklist:
         """Returns a list of your tasks.
         Returns up to 100 at a time, to get more, use the
         next_token param passed back.
 
         Valid Args:
             start_time (str):
```

### Comparing `scaleapi-2.8.0/scaleapi/api.py` & `scaleapi-2.9.0/scaleapi/api.py`

 * *Files 3% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 
 SCALE_API_BASE_URL_V1 = "https://api.scale.com/v1"
 
 # Parameters for HTTP retry
 HTTP_TOTAL_RETRIES = 3  # Number of total retries
 HTTP_RETRY_BACKOFF_FACTOR = 2  # Wait 1, 2, 4 seconds between retries
 HTTP_STATUS_FORCE_LIST = [408, 429] + list(range(500, 531))
-HTTP_RETRY_ALLOWED_METHODS = frozenset({"GET", "POST"})
+HTTP_RETRY_ALLOWED_METHODS = frozenset({"GET", "POST", "DELETE"})
 
 
 class Api:
     """Internal Api reference for handling http operations"""
 
     def __init__(self, api_key, user_agent_extension=None, api_instance_url=None):
         if api_key == "" or api_key is None:
@@ -130,14 +130,20 @@
             else self._headers_multipart_form_data,
             auth=self._auth,
             body=body,
             files=files,
             data=data,
         )
 
+    def delete_request(self, endpoint, params=None):
+        """Generic DELETE Request Wrapper"""
+        return self._api_request(
+            "DELETE", endpoint, headers=self._headers, auth=self._auth, params=params
+        )
+
     @staticmethod
     def _generate_useragent(extension: str = None) -> str:
         """Generates UserAgent parameter with module, Python
         and OS details
 
         Args:
             extension (str, optional): Option to extend UserAgent
```

### Comparing `scaleapi-2.8.0/scaleapi/batches.py` & `scaleapi-2.9.0/scaleapi/batches.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/scaleapi/exceptions.py` & `scaleapi-2.9.0/scaleapi/exceptions.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/scaleapi/files.py` & `scaleapi-2.9.0/scaleapi/files.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/scaleapi/projects.py` & `scaleapi-2.9.0/scaleapi/projects.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/scaleapi/quality_tasks.py` & `scaleapi-2.9.0/scaleapi/quality_tasks.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/scaleapi/tasks.py` & `scaleapi-2.9.0/scaleapi/tasks.py`

 * *Files 11% similar despite different names*

```diff
@@ -80,10 +80,18 @@
         """
         return self._json
 
     def refresh(self):
         """Refreshes the task details."""
         self._json = self._client.get_task(self.id).as_dict()
 
-    def cancel(self):
+    def cancel(self, clear_unique_id: bool = False):
         """Cancels the task"""
-        self._client.cancel_task(self.id)
+        self._client.cancel_task(self.id, clear_unique_id)
+
+    def update_unique_id(self, unique_id: str):
+        """Updates unique_id of a task"""
+        self._client.update_task_unique_id(self.id, unique_id)
+
+    def clear_unique_id(self):
+        """Clears unique_id of a task"""
+        self._client.clear_task_unique_id(self.id)
```

### Comparing `scaleapi-2.8.0/scaleapi.egg-info/PKG-INFO` & `scaleapi-2.9.0/scaleapi.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scaleapi
-Version: 2.8.0
+Version: 2.9.0
 Summary: The official Python client library for Scale AI, the Data Platform for AI
 Home-page: https://github.com/scaleapi/scaleapi-python-client
 Author: Scale AI
 Author-email: support@scale.com
 License: UNKNOWN
 Description: *********************
         Scale AI | Python SDK
@@ -232,14 +232,57 @@
         
         __ https://docs.scale.com/reference#cancel-task
         
         .. code-block :: python
         
             task = client.cancel_task('30553edd0b6a93f8f05f0fee')
         
+            # If you also want to clear 'unique_id' of a task while canceling
+            task = client.cancel_task('30553edd0b6a93f8f05f0fee', clear_unique_id=True)
+        
+            # cancel() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.cancel()
+        
+            # If you also want to clear 'unique_id' of a task while canceling
+            task.cancel(clear_unique_id=True)
+        
+        
+        Update A Task's Unique Id
+        ^^^^^^^^^^^^^^^^^^^^^^^^^
+        
+        Update a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+        
+        __ https://docs.scale.com/reference/update-task-unique-id
+        
+        .. code-block :: python
+        
+            task = client.update_task_unique_id('30553edd0b6a93f8f05f0fee', "new_unique_id")
+        
+            # update_unique_id() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.update_unique_id("new_unique_id")
+        
+        
+        Clear A Task's Unique Id
+        ^^^^^^^^^^^^^^^^^^^^^^^^^
+        
+        Clear a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+        
+        __ https://docs.scale.com/reference/delete-task-unique-id
+        
+        .. code-block :: python
+        
+            task = client.clear_task_unique_id('30553edd0b6a93f8f05f0fee')
+        
+            # clear_unique_id() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.clear_unique_id()
+        
+        
         Batches
         _______
         
         Create Batch
         ^^^^^^^^^^^^
         
         Create a new Batch. Check out `Scale's API documentation`__ for more information.
@@ -355,15 +398,15 @@
                 project_name = "Test_Project",
                 task_type = TaskType.ImageAnnotation,
                 params = {"instruction": "Please label the kittens"},
             )
         
             print(project.name)  # Test_Project
         
-        Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists. 
+        Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists.
         
         Retrieve Project
         ^^^^^^^^^^^^^^^^
         
         Retrieve a single Project. Check out `Scale's API documentation`__ for more information.
         
         __ https://docs.scale.com/reference#project-retrieval
```

### Comparing `scaleapi-2.8.0/README.rst` & `scaleapi-2.9.0/README.rst`

 * *Files 7% similar despite different names*

```diff
@@ -224,14 +224,57 @@
 
 __ https://docs.scale.com/reference#cancel-task
 
 .. code-block :: python
 
     task = client.cancel_task('30553edd0b6a93f8f05f0fee')
 
+    # If you also want to clear 'unique_id' of a task while canceling
+    task = client.cancel_task('30553edd0b6a93f8f05f0fee', clear_unique_id=True)
+
+    # cancel() is also available on task object
+    task = client.get_task('30553edd0b6a93f8f05f0fee')
+    task.cancel()
+
+    # If you also want to clear 'unique_id' of a task while canceling
+    task.cancel(clear_unique_id=True)
+
+
+Update A Task's Unique Id
+^^^^^^^^^^^^^^^^^^^^^^^^^
+
+Update a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+
+__ https://docs.scale.com/reference/update-task-unique-id
+
+.. code-block :: python
+
+    task = client.update_task_unique_id('30553edd0b6a93f8f05f0fee', "new_unique_id")
+
+    # update_unique_id() is also available on task object
+    task = client.get_task('30553edd0b6a93f8f05f0fee')
+    task.update_unique_id("new_unique_id")
+
+
+Clear A Task's Unique Id
+^^^^^^^^^^^^^^^^^^^^^^^^^
+
+Clear a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+
+__ https://docs.scale.com/reference/delete-task-unique-id
+
+.. code-block :: python
+
+    task = client.clear_task_unique_id('30553edd0b6a93f8f05f0fee')
+
+    # clear_unique_id() is also available on task object
+    task = client.get_task('30553edd0b6a93f8f05f0fee')
+    task.clear_unique_id()
+
+
 Batches
 _______
 
 Create Batch
 ^^^^^^^^^^^^
 
 Create a new Batch. Check out `Scale's API documentation`__ for more information.
@@ -347,15 +390,15 @@
         project_name = "Test_Project",
         task_type = TaskType.ImageAnnotation,
         params = {"instruction": "Please label the kittens"},
     )
 
     print(project.name)  # Test_Project
 
-Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists. 
+Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists.
 
 Retrieve Project
 ^^^^^^^^^^^^^^^^
 
 Retrieve a single Project. Check out `Scale's API documentation`__ for more information.
 
 __ https://docs.scale.com/reference#project-retrieval
```

### Comparing `scaleapi-2.8.0/setup.py` & `scaleapi-2.9.0/setup.py`

 * *Files identical despite different names*

### Comparing `scaleapi-2.8.0/PKG-INFO` & `scaleapi-2.9.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scaleapi
-Version: 2.8.0
+Version: 2.9.0
 Summary: The official Python client library for Scale AI, the Data Platform for AI
 Home-page: https://github.com/scaleapi/scaleapi-python-client
 Author: Scale AI
 Author-email: support@scale.com
 License: UNKNOWN
 Description: *********************
         Scale AI | Python SDK
@@ -232,14 +232,57 @@
         
         __ https://docs.scale.com/reference#cancel-task
         
         .. code-block :: python
         
             task = client.cancel_task('30553edd0b6a93f8f05f0fee')
         
+            # If you also want to clear 'unique_id' of a task while canceling
+            task = client.cancel_task('30553edd0b6a93f8f05f0fee', clear_unique_id=True)
+        
+            # cancel() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.cancel()
+        
+            # If you also want to clear 'unique_id' of a task while canceling
+            task.cancel(clear_unique_id=True)
+        
+        
+        Update A Task's Unique Id
+        ^^^^^^^^^^^^^^^^^^^^^^^^^
+        
+        Update a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+        
+        __ https://docs.scale.com/reference/update-task-unique-id
+        
+        .. code-block :: python
+        
+            task = client.update_task_unique_id('30553edd0b6a93f8f05f0fee', "new_unique_id")
+        
+            # update_unique_id() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.update_unique_id("new_unique_id")
+        
+        
+        Clear A Task's Unique Id
+        ^^^^^^^^^^^^^^^^^^^^^^^^^
+        
+        Clear a given task's unique_id. Check out `Scale's API documentation`__ for more information.
+        
+        __ https://docs.scale.com/reference/delete-task-unique-id
+        
+        .. code-block :: python
+        
+            task = client.clear_task_unique_id('30553edd0b6a93f8f05f0fee')
+        
+            # clear_unique_id() is also available on task object
+            task = client.get_task('30553edd0b6a93f8f05f0fee')
+            task.clear_unique_id()
+        
+        
         Batches
         _______
         
         Create Batch
         ^^^^^^^^^^^^
         
         Create a new Batch. Check out `Scale's API documentation`__ for more information.
@@ -355,15 +398,15 @@
                 project_name = "Test_Project",
                 task_type = TaskType.ImageAnnotation,
                 params = {"instruction": "Please label the kittens"},
             )
         
             print(project.name)  # Test_Project
         
-        Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists. 
+        Specify ``rapid=true`` for Rapid projects and ``studio=true`` for Studio projects. Throws ``ScaleDuplicateResource`` exception if a project with the same name already exists.
         
         Retrieve Project
         ^^^^^^^^^^^^^^^^
         
         Retrieve a single Project. Check out `Scale's API documentation`__ for more information.
         
         __ https://docs.scale.com/reference#project-retrieval
```

