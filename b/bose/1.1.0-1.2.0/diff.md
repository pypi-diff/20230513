# Comparing `tmp/bose-1.1.0.tar.gz` & `tmp/bose-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bose-1.1.0.tar", last modified: Tue May  9 15:57:22 2023, max compression
+gzip compressed data, was "bose-1.2.0.tar", last modified: Sat May 13 09:44:27 2023, max compression
```

## Comparing `bose-1.1.0.tar` & `bose-1.2.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-05-09 15:57:22.667518 bose-1.1.0/
--rw-rw-rw-   0        0        0     8678 2023-05-09 15:57:22.669516 bose-1.1.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-09 15:57:22.667518 bose-1.1.0/bose/
--rw-rw-rw-   0        0        0      303 2023-05-09 12:16:48.786461 bose-1.1.0/bose/__init__.py
--rw-rw-rw-   0        0        0     2861 2023-05-09 09:08:49.452740 bose-1.1.0/bose/base_data.py
--rw-rw-rw-   0        0        0     3646 2023-05-09 15:26:36.574181 bose-1.1.0/bose/base_task.py
--rw-rw-rw-   0        0        0     7265 2023-05-09 15:15:30.436760 bose-1.1.0/bose/create_driver.py
--rw-rw-rw-   0        0        0     1559 2023-05-09 09:26:46.769040 bose-1.1.0/bose/download_driver.py
--rw-rw-rw-   0        0        0     2493 2023-05-09 07:32:15.014678 bose-1.1.0/bose/local_storage.py
--rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.1.0/bose/opponent.py
--rw-rw-rw-   0        0        0     3173 2023-05-09 15:50:46.922925 bose-1.1.0/bose/output.py
--rw-rw-rw-   0        0        0     1654 2023-05-09 12:06:31.715212 bose-1.1.0/bose/task_info.py
--rw-rw-rw-   0        0        0     7337 2023-05-09 11:56:53.677609 bose-1.1.0/bose/user_agent.py
--rw-rw-rw-   0        0        0     5882 2023-05-09 11:32:50.275917 bose-1.1.0/bose/utils.py
--rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.1.0/bose/wait.py
--rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.1.0/bose/window_size.py
--rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.1.0/setup.cfg
--rw-rw-rw-   0        0        0     2189 2023-05-09 15:57:09.812603 bose-1.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:44:27.369315 bose-1.2.0/
+-rw-rw-rw-   0        0        0     1503 2023-05-13 09:44:27.370314 bose-1.2.0/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 09:44:27.368326 bose-1.2.0/bose/
+-rw-rw-rw-   0        0        0      348 2023-05-10 06:44:37.337926 bose-1.2.0/bose/__init__.py
+-rw-rw-rw-   0        0        0     3657 2023-05-10 09:24:37.900794 bose-1.2.0/bose/base_data.py
+-rw-rw-rw-   0        0        0     5252 2023-05-13 08:16:49.683340 bose-1.2.0/bose/base_task.py
+-rw-rw-rw-   0        0        0     7331 2023-05-10 09:27:31.379871 bose-1.2.0/bose/create_driver.py
+-rw-rw-rw-   0        0        0     1391 2023-05-10 10:36:24.892682 bose-1.2.0/bose/download_driver.py
+-rw-rw-rw-   0        0        0     2905 2023-05-10 10:11:04.901186 bose-1.2.0/bose/local_storage.py
+-rw-rw-rw-   0        0        0       80 2023-05-09 06:14:41.273740 bose-1.2.0/bose/opponent.py
+-rw-rw-rw-   0        0        0     3173 2023-05-09 15:50:46.922925 bose-1.2.0/bose/output.py
+-rw-rw-rw-   0        0        0     1654 2023-05-09 12:06:31.715212 bose-1.2.0/bose/task_info.py
+-rw-rw-rw-   0        0        0     7361 2023-05-10 09:24:37.900794 bose-1.2.0/bose/user_agent.py
+-rw-rw-rw-   0        0        0     6050 2023-05-10 10:34:20.625623 bose-1.2.0/bose/utils.py
+-rw-rw-rw-   0        0        0       60 2023-05-09 06:15:17.436327 bose-1.2.0/bose/wait.py
+-rw-rw-rw-   0        0        0     1203 2023-05-09 07:09:28.075948 bose-1.2.0/bose/window_size.py
+-rw-rw-rw-   0        0        0       40 2022-10-28 11:26:12.145036 bose-1.2.0/setup.cfg
+-rw-rw-rw-   0        0        0     2189 2023-05-10 08:18:54.462936 bose-1.2.0/setup.py
```

### Comparing `bose-1.1.0/bose/create_driver.py` & `bose-1.2.0/bose/create_driver.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,21 +12,21 @@
 import os
 
 class RetryException(Exception):
     pass
 
 
 class BrowserConfig:
-    def __init__(self, user_agent=None, window_size=WindowSize.window_size_1920_1080, profile=None, is_eager=False, use_undetected_driver=False):
+    def __init__(self, user_agent=None, window_size=WindowSize.window_size_1920_1080, profile=None, is_eager=False, use_undetected_driver=False, close_on_crash = False):
         self.user_agent = user_agent
         self.window_size = window_size
         self.profile = profile
         self.is_eager = is_eager
         self.use_undetected_driver = use_undetected_driver
-
+        self.close_on_crash = close_on_crash
 
 def delete_cache(driver):
     print('Deleting Cache')
     driver.command_executor._commands['SEND_COMMAND'] = (
         'POST', '/session/$sessionId/chromium/send_command'
     )
     driver.execute('SEND_COMMAND', dict(
@@ -77,14 +77,15 @@
             window_size = window_size
     
     window_size = WindowSize.window_size_to_string(window_size)
     options.add_argument(f"--window-size={window_size}")
 
     if profile is not None:
         profile = str(profile)
+
     if user_agent == None:
         if profile == None:
             user_agent = UserAgentInstance.get_random()
         else:
             user_agent = UserAgentInstance.get_hashed(profile)
     else: 
         if user_agent == UserAgent.RANDOM:
@@ -139,27 +140,26 @@
 def get_driver_path():
     executable_name = "chromedriver.exe" if is_windows() else "chromedriver"
     dest_path = f"build/{executable_name}"
     return dest_path
 
 def create_driver(config: BrowserConfig):
     def run():
-
         is_undetected = config.use_undetected_driver
         options = ChromeOptions() if is_undetected else GoogleChromeOptions()
 
         if is_docker():
             print("Running in Docker, So adding sandbox arguments")
             options.arguments.extend(
                 ["--no-sandbox", "--disable-setuid-sandbox"])
 
         driver_attributes = add_essential_options(options, config.profile, config.window_size, config.user_agent)
 
         if driver_attributes["profile"] is not None:
-            driver_string = "Creating Driver with profile '{}', window_size={}, and user_agent={}".format(driver_attributes["profile"], driver_attributes["window_size"], driver_attributes["user_agent"])
+            driver_string = "Creating Driver with profile {}, window_size={}, and user_agent={}".format(driver_attributes["profile"], driver_attributes["window_size"], driver_attributes["user_agent"])
         else:
             driver_string = "Creating Driver with window_size={} and user_agent={}".format(driver_attributes["window_size"], driver_attributes["user_agent"])
       
         if config.is_eager:
             desired_capabilities = get_eager_startegy()
         else:
             desired_capabilities = None
```

### Comparing `bose-1.1.0/bose/download_driver.py` & `bose-1.2.0/bose/download_driver.py`

 * *Files 7% similar despite different names*

```diff
@@ -19,18 +19,14 @@
 
     # Delete the build directory
     shutil.rmtree(build_dir, ignore_errors=True)
 
     # Create the build directory again
     os.makedirs(build_dir)
 
-def get_driver_path():
-    executable_name = "chromedriver.exe" if is_windows() else "chromedriver"
-    dest_path = f"build/{executable_name}"
-    return dest_path
 
 def move_driver():
     major_version = get_major_version(get_chrome_version())
 
     executable_name = "chromedriver.exe" if is_windows() else "chromedriver"
 
     def move_chromedriver():
```

### Comparing `bose-1.1.0/bose/local_storage.py` & `bose-1.2.0/bose/local_storage.py`

 * *Files 21% similar despite different names*

```diff
@@ -49,14 +49,27 @@
         self.commit_to_disk()
 
     def remove_item(self, key: str) -> None: 
         if key in self.json_data:
             self.json_data.pop(key)
             self.commit_to_disk()
 
+
+    # def get_new_number(self):
+    #     seen = self.get_item('seen', [])
+        
+    #     if len(seen) == 0:
+    #         max_seen = 0
+    #     else:
+    #         max_seen = max(seen)
+        
+    #     new =  max_seen + 1
+    #     self.set_item('seen', seen + [new])
+    #     return new
+
     def clear(self) -> None:
         if os.path.isfile(self.json_path):
             os.remove(self.json_path)
         self.json_data = {}
         self.commit_to_disk()
     
 class _LocalStorage:
@@ -71,14 +84,17 @@
 
     def remove_item(self, item: str) -> None:
         self.storage_backend_instance.remove_item(item)
 
     def clear(self):
         self.storage_backend_instance.clear()
 
+    # def get_new_number(self):
+    #     return self.storage_backend_instance.get_new_number()
+
 LocalStorage = _LocalStorage()
 
 if __name__ == "__main__":
     t = _LocalStorage()
     
     print(t.get_item("a"))
     print(t.set_item("a" ,"ss"))
```

### Comparing `bose-1.1.0/bose/output.py` & `bose-1.2.0/bose/output.py`

 * *Files identical despite different names*

### Comparing `bose-1.1.0/bose/task_info.py` & `bose-1.2.0/bose/task_info.py`

 * *Files identical despite different names*

### Comparing `bose-1.1.0/bose/user_agent.py` & `bose-1.2.0/bose/user_agent.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from .base_data import BaseData
-from .utils import is_windows, is_mac
+from .utils import is_windows, is_mac, write_json
 
 def get_correct_agent(windows, mac, linux):
     if is_windows():
         return windows
     elif is_mac():
         return mac
     else:
@@ -112,10 +112,10 @@
 
         return result
 
 
 UserAgentInstance = UserAgent()
 if __name__ == '__main__':
     UserAgentInstance = UserAgent()
-    print(UserAgentInstance.get_hashed('a'))
-    print(UserAgentInstance.get_hashed('a'))
-    print(UserAgentInstance.get_hashed('b'))
+    print(UserAgentInstance.get_random_cycled())
+    print(UserAgentInstance.get_random_cycled())
+    print(UserAgentInstance.get_random_cycled())
```

### Comparing `bose-1.1.0/bose/utils.py` & `bose-1.2.0/bose/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -255,7 +255,12 @@
         users = json.load(fp)
         return users
     
 def write_json(data, path,  indent=4):
     with open(path, 'w') as fp:
         json.dump(data, fp, indent=indent)
 
+
+def get_driver_path():
+    executable_name = "chromedriver.exe" if is_windows() else "chromedriver"
+    dest_path = f"build/{executable_name}"
+    return dest_path
```

### Comparing `bose-1.1.0/bose/window_size.py` & `bose-1.2.0/bose/window_size.py`

 * *Files identical despite different names*

### Comparing `bose-1.1.0/setup.py` & `bose-1.2.0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 cpython_dependencies = [
     "PyDispatcher>=2.0.5",
 ]
 
 setup(
     name='bose',
     packages=['bose'],
-    version='1.1.0',
+    version='1.2.0',
     license='MIT',
     project_urls={
         "Documentation": "https://omkar.cloud/bose/docs/",
         "Source": "https://github.com/omkarcloud/boss",
         "Tracker": "https://github.com/omkarcloud/boss/issues",
     },
```

