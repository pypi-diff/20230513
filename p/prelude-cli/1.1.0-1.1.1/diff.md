# Comparing `tmp/prelude-cli-1.1.0.tar.gz` & `tmp/prelude-cli-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "prelude-cli-1.1.0.tar", last modified: Sun May  7 12:45:14 2023, max compression
+gzip compressed data, was "prelude-cli-1.1.1.tar", last modified: Sat May 13 20:31:48 2023, max compression
```

## Comparing `prelude-cli-1.1.0.tar` & `prelude-cli-1.1.1.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:45:14.854406 prelude-cli-1.1.0/
--rw-r--r--   0 pack       (501) staff       (20)     1069 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/LICENSE
--rw-r--r--   0 pack       (501) staff       (20)       31 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/MANIFEST.in
--rw-r--r--   0 pack       (501) staff       (20)      832 2023-05-07 12:45:14.854458 prelude-cli-1.1.0/PKG-INFO
--rw-r--r--   0 pack       (501) staff       (20)      391 2023-03-01 15:58:44.000000 prelude-cli-1.1.0/README.md
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:45:14.851429 prelude-cli-1.1.0/prelude_cli/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/prelude_cli/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)      775 2023-05-02 14:19:17.000000 prelude-cli-1.1.0/prelude_cli/cli.py
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-05-03 13:30:52.000000 prelude-cli-1.1.0/prelude_cli/spinner.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:45:14.852229 prelude-cli-1.1.0/prelude_cli/templates/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/prelude_cli/templates/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)      241 2023-05-04 16:11:50.000000 prelude-cli-1.1.0/prelude_cli/templates/template.go
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:45:14.854111 prelude-cli-1.1.0/prelude_cli/views/
--rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/prelude_cli/views/__init__.py
--rw-r--r--   0 pack       (501) staff       (20)     3872 2023-05-07 12:16:47.000000 prelude-cli-1.1.0/prelude_cli/views/build.py
--rw-r--r--   0 pack       (501) staff       (20)      552 2023-02-08 14:42:44.000000 prelude-cli-1.1.0/prelude_cli/views/configure.py
--rw-r--r--   0 pack       (501) staff       (20)     5021 2023-05-04 16:11:50.000000 prelude-cli-1.1.0/prelude_cli/views/detect.py
--rw-r--r--   0 pack       (501) staff       (20)     3256 2023-05-03 13:30:52.000000 prelude-cli-1.1.0/prelude_cli/views/iam.py
--rw-r--r--   0 pack       (501) staff       (20)     2246 2023-05-03 13:30:52.000000 prelude-cli-1.1.0/prelude_cli/views/partner.py
--rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-03 13:30:52.000000 prelude-cli-1.1.0/prelude_cli/views/shared.py
-drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-07 12:45:14.852046 prelude-cli-1.1.0/prelude_cli.egg-info/
--rw-r--r--   0 pack       (501) staff       (20)      832 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/PKG-INFO
--rw-r--r--   0 pack       (501) staff       (20)      598 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/SOURCES.txt
--rw-r--r--   0 pack       (501) staff       (20)        1 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/dependency_links.txt
--rw-r--r--   0 pack       (501) staff       (20)       48 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/entry_points.txt
--rw-r--r--   0 pack       (501) staff       (20)       32 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/requires.txt
--rw-r--r--   0 pack       (501) staff       (20)       12 2023-05-07 12:45:14.000000 prelude-cli-1.1.0/prelude_cli.egg-info/top_level.txt
--rw-r--r--   0 pack       (501) staff       (20)      103 2023-01-24 13:01:01.000000 prelude-cli-1.1.0/pyproject.toml
--rw-r--r--   0 pack       (501) staff       (20)      663 2023-05-07 12:45:14.854682 prelude-cli-1.1.0/setup.cfg
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:31:48.170530 prelude-cli-1.1.1/
+-rw-r--r--   0 pack       (501) staff       (20)     1069 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/LICENSE
+-rw-r--r--   0 pack       (501) staff       (20)       31 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/MANIFEST.in
+-rw-r--r--   0 pack       (501) staff       (20)      832 2023-05-13 20:31:48.170585 prelude-cli-1.1.1/PKG-INFO
+-rw-r--r--   0 pack       (501) staff       (20)      391 2023-03-01 15:58:44.000000 prelude-cli-1.1.1/README.md
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:31:48.167707 prelude-cli-1.1.1/prelude_cli/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/prelude_cli/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)      775 2023-05-02 14:19:17.000000 prelude-cli-1.1.1/prelude_cli/cli.py
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-05-03 13:30:52.000000 prelude-cli-1.1.1/prelude_cli/spinner.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:31:48.168581 prelude-cli-1.1.1/prelude_cli/templates/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/prelude_cli/templates/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)      241 2023-05-04 16:11:50.000000 prelude-cli-1.1.1/prelude_cli/templates/template.go
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:31:48.170245 prelude-cli-1.1.1/prelude_cli/views/
+-rw-r--r--   0 pack       (501) staff       (20)        0 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/prelude_cli/views/__init__.py
+-rw-r--r--   0 pack       (501) staff       (20)     4004 2023-05-13 20:12:56.000000 prelude-cli-1.1.1/prelude_cli/views/build.py
+-rw-r--r--   0 pack       (501) staff       (20)      552 2023-02-08 14:42:44.000000 prelude-cli-1.1.1/prelude_cli/views/configure.py
+-rw-r--r--   0 pack       (501) staff       (20)     5021 2023-05-04 16:11:50.000000 prelude-cli-1.1.1/prelude_cli/views/detect.py
+-rw-r--r--   0 pack       (501) staff       (20)     3494 2023-05-12 13:56:19.000000 prelude-cli-1.1.1/prelude_cli/views/iam.py
+-rw-r--r--   0 pack       (501) staff       (20)     2246 2023-05-03 13:30:52.000000 prelude-cli-1.1.1/prelude_cli/views/partner.py
+-rw-r--r--   0 pack       (501) staff       (20)     1139 2023-05-03 13:30:52.000000 prelude-cli-1.1.1/prelude_cli/views/shared.py
+drwxr-xr-x   0 pack       (501) staff       (20)        0 2023-05-13 20:31:48.168390 prelude-cli-1.1.1/prelude_cli.egg-info/
+-rw-r--r--   0 pack       (501) staff       (20)      832 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/PKG-INFO
+-rw-r--r--   0 pack       (501) staff       (20)      598 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/SOURCES.txt
+-rw-r--r--   0 pack       (501) staff       (20)        1 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/dependency_links.txt
+-rw-r--r--   0 pack       (501) staff       (20)       48 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/entry_points.txt
+-rw-r--r--   0 pack       (501) staff       (20)       32 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/requires.txt
+-rw-r--r--   0 pack       (501) staff       (20)       12 2023-05-13 20:31:48.000000 prelude-cli-1.1.1/prelude_cli.egg-info/top_level.txt
+-rw-r--r--   0 pack       (501) staff       (20)      103 2023-01-24 13:01:01.000000 prelude-cli-1.1.1/pyproject.toml
+-rw-r--r--   0 pack       (501) staff       (20)      663 2023-05-13 20:31:48.170810 prelude-cli-1.1.1/setup.cfg
```

### Comparing `prelude-cli-1.1.0/LICENSE` & `prelude-cli-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/PKG-INFO` & `prelude-cli-1.1.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prelude-cli
-Version: 1.1.0
+Version: 1.1.1
 Summary: For interacting with the Prelude SDK
 Home-page: https://github.com/preludeorg
 Author: Prelude Research
 Author-email: support@preludesecurity.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `prelude-cli-1.1.0/prelude_cli/cli.py` & `prelude-cli-1.1.1/prelude_cli/cli.py`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/prelude_cli/views/build.py` & `prelude-cli-1.1.1/prelude_cli/views/build.py`

 * *Files 5% similar despite different names*

```diff
@@ -52,15 +52,18 @@
         template = template.replace('$ID', test_id)
         template = template.replace('$NAME', name)
         template = template.replace('$UNIT', unit or '')
         template = template.replace('$CREATED', str(datetime.utcnow()))
         with Spinner():
             controller.upload(test_id=test_id, filename=basename, data=template)
 
-        with open(basename, 'w') as test_code:
+        test_dir = PurePath(test_id, basename)
+        Path(test_id).mkdir(parents=True, exist_ok=True)
+        
+        with open(test_dir, 'w', encoding='utf8') as test_code:
             test_code.write(template)
             click.secho(f'Created {basename}', fg='green')
 
 
 @build.command('delete-test')
 @click.argument('test')
 @click.confirmation_option(prompt='Are you sure?')
@@ -104,15 +107,15 @@
             return match.group(0)
         raise FileNotFoundError('You must supply a test ID or include it in the path')
 
     def upload(p: Path):
         with open(p, 'rb') as data:
             with Spinner():
                 controller.upload(test_id=identifier, filename=p.name, data=data.read(), binary=True)
-            click.secho(f'Uploaded {path}', fg='green')
+            click.secho(f'Uploaded {p.name}', fg='green')
 
     identifier = test or test_id()
     
     if Path(path).is_file():
         upload(p=Path(path))
     else:
         for obj in Path(path).rglob('*'):
```

### Comparing `prelude-cli-1.1.0/prelude_cli/views/configure.py` & `prelude-cli-1.1.1/prelude_cli/views/configure.py`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/prelude_cli/views/detect.py` & `prelude-cli-1.1.1/prelude_cli/views/detect.py`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/prelude_cli/views/iam.py` & `prelude-cli-1.1.1/prelude_cli/views/iam.py`

 * *Files 16% similar despite different names*

```diff
@@ -17,17 +17,18 @@
 
 @iam.command('create-account')
 @click.pass_obj
 @handle_api_error
 @click.confirmation_option(prompt='Overwrite local account credentials for selected profile?')
 def register_account(controller):
     """ Register a new account """
-    handle = click.prompt('Enter a handle')
+    email = click.prompt('Enter your email')
+    name = click.prompt('(Optional) Enter your name', default='', show_default=False)
     with Spinner():
-        data = controller.new_account(handle=handle)
+        data = controller.new_account(user_email=email, user_name=name)
     print_json(data=data)
     print("\nCheck your email to verify your account.\n")
 
 
 @iam.command('update-account')
 @click.option('-m', '--mode',
               help='provide a mode',
@@ -48,32 +49,35 @@
     """ Get account details """
     with Spinner():
         data = controller.get_account()
     print_json(data=data)
 
 
 @iam.command('create-user')
-@click.option('-d', '--days', help='days this account should remain active', default=365, type=int)
-@click.option('-p', '--permission', help='provide a permission level', default=Permission.SERVICE.name,
-              type=click.Choice([p.name for p in Permission], case_sensitive=False), show_default=True)
-@click.argument('handle')
+@click.option('-d', '--days', help='days this user will remain active', default=365, type=int)
+@click.option('-p', '--permission', help='user permission level', default=Permission.SERVICE.name,
+              type=click.Choice([p.name for p in Permission if p != Permission.INVALID], case_sensitive=False), show_default=True)
+@click.option('-n', '--name', help='name of user', default='', type=str)
+@click.argument('email')
 @click.pass_obj
 @handle_api_error
-def create_user(controller, permission, handle, days):
+def create_user(controller, days, permission, name, email):
     """ Create a new user in your account """
     expires = datetime.utcnow() + timedelta(days=days)
     with Spinner():
         data = controller.create_user(
-            handle=handle,
+            email=email,
             permission=Permission[permission.upper()].value,
+            name=name,
             expires=expires
         )
     print_json(data=data)
     if permission != Permission.SERVICE.name:
-        print("\nCheck your email to verify your account.\n")
+        print("\nNew user must check their email to verify their account.\n")
+
 
 @iam.command('delete-user')
 @click.confirmation_option(prompt='Are you sure?')
 @click.argument('handle')
 @click.pass_obj
 @handle_api_error
 def delete_user(controller, handle):
```

### Comparing `prelude-cli-1.1.0/prelude_cli/views/partner.py` & `prelude-cli-1.1.1/prelude_cli/views/partner.py`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/prelude_cli/views/shared.py` & `prelude-cli-1.1.1/prelude_cli/views/shared.py`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/prelude_cli.egg-info/PKG-INFO` & `prelude-cli-1.1.1/prelude_cli.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: prelude-cli
-Version: 1.1.0
+Version: 1.1.1
 Summary: For interacting with the Prelude SDK
 Home-page: https://github.com/preludeorg
 Author: Prelude Research
 Author-email: support@preludesecurity.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `prelude-cli-1.1.0/prelude_cli.egg-info/SOURCES.txt` & `prelude-cli-1.1.1/prelude_cli.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `prelude-cli-1.1.0/setup.cfg` & `prelude-cli-1.1.1/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = prelude-cli
-version = 1.1.0
+version = 1.1.1
 author = Prelude Research
 author_email = support@preludesecurity.com
 description = For interacting with the Prelude SDK
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/preludeorg
 classifiers = 
@@ -13,15 +13,15 @@
 	Operating System :: OS Independent
 
 [options]
 packages = find:
 include_package_data = True
 python_requires = >=3.8
 install_requires = 
-	prelude-sdk == 1.1.0
+	prelude-sdk == 1.1.1
 	click > 8
 	rich
 
 [options.entry_points]
 console_scripts = 
 	prelude = prelude_cli.cli:cli
```

