# Comparing `tmp/rcp-colors-0.112.tar.gz` & `tmp/rcp-colors-0.113.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rcp-colors-0.112.tar", last modified: Sat May 13 03:10:17 2023, max compression
+gzip compressed data, was "rcp-colors-0.113.tar", last modified: Sat May 13 15:20:29 2023, max compression
```

## Comparing `rcp-colors-0.112.tar` & `rcp-colors-0.113.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 03:10:17.011979 rcp-colors-0.112/
--rw-rw-rw-   0        0        0      614 2023-05-13 03:10:17.010977 rcp-colors-0.112/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-13 03:10:16.976202 rcp-colors-0.112/rcp_colors/
--rw-rw-rw-   0        0        0       21 2023-05-13 02:58:35.000000 rcp-colors-0.112/rcp_colors/__init__.py
--rw-rw-rw-   0        0        0    28287 2023-05-13 02:56:30.000000 rcp-colors-0.112/rcp_colors/rcp.py
-drwxrwxrwx   0        0        0        0 2023-05-13 03:10:17.009009 rcp-colors-0.112/rcp_colors.egg-info/
--rw-rw-rw-   0        0        0      614 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      255 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       44 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       16 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-05-13 03:10:16.000000 rcp-colors-0.112/rcp_colors.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 03:10:17.011979 rcp-colors-0.112/setup.cfg
--rw-rw-rw-   0        0        0      993 2023-05-13 03:09:40.000000 rcp-colors-0.112/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:20:29.469708 rcp-colors-0.113/
+-rw-rw-rw-   0        0        0      750 2023-05-13 15:20:29.468708 rcp-colors-0.113/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 15:20:29.422618 rcp-colors-0.113/rcp_colors/
+-rw-rw-rw-   0        0        0       21 2023-05-13 02:58:35.000000 rcp-colors-0.113/rcp_colors/__init__.py
+-rw-rw-rw-   0        0        0    28474 2023-05-13 15:19:45.000000 rcp-colors-0.113/rcp_colors/rcp.py
+drwxrwxrwx   0        0        0        0 2023-05-13 15:20:29.465709 rcp-colors-0.113/rcp_colors.egg-info/
+-rw-rw-rw-   0        0        0      750 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      255 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       51 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 15:20:29.000000 rcp-colors-0.113/rcp_colors.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 15:20:29.470709 rcp-colors-0.113/setup.cfg
+-rw-rw-rw-   0        0        0     1135 2023-05-13 15:19:41.000000 rcp-colors-0.113/setup.py
```

### Comparing `rcp-colors-0.112/PKG-INFO` & `rcp-colors-0.113/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.112
+Version: 0.113
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
-Project-URL: Source, https://github.com/PlusPlusMan/rcp/
+Project-URL: Source, https://github.com/PlusPlusMan/RichColorPicker
+Project-URL: Bug Reports, https://github.com/PlusPlusMan/RichColorPicker/issues
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.6, <4
 Description-Content-Type: text/markdown
 
-Terminal based rich color picker app
+Terminal based rich color picker app. Type rcp-colors in your terminal to start.
```

### Comparing `rcp-colors-0.112/rcp_colors/rcp.py` & `rcp-colors-0.113/rcp_colors/rcp.py`

 * *Files 1% similar despite different names*

```diff
@@ -134,35 +134,38 @@
 
 class ComputedApp(App):
     global data_file
     
     DEFAULT_CSS = """
 Screen {
     layout: horizontal;
-    height: 100%
+    height: 100%;
+    overflow: auto auto;
 }
 
 #main {
     dock: top;
     height: 100%;
+    overflow: auto auto;
 }
 
 #title {
     margin: 1 0 0 0;
     align: center top;
 }
+
 .title-label {
     background: $boost;
     text-align: center;
     color: $secondary-lighten-2;
     border: vkey $secondary;
 }
 
 .color { /* Color panel representing current color for hsl and rgb panels*/
-    height: 20fr;
+    height: 15fr;
     border: hkey $secondary;
     margin: 2 0;
     text-align: center;
     align: center middle;
     border-title-color: $secondary-lighten-2;
     border-title-style: bold italic;
     border-title-align: center;
@@ -261,15 +264,15 @@
     width: 90%;
 }
 
 #saved-colors-container {
     border: round $accent;
     color: red;
     margin: 1 2;
-    height: 35fr;
+    height: auto;
     background: $primary-background-darken-1;
 
 }
 
 .content-container {
     align: center bottom;
     background: $boost;
@@ -342,17 +345,18 @@
 
 #color-name-input {
     margin: 2 10;
     height: auto;
 }
 
 #colors-main-container {
-    margin: 2 1;
+    margin: 1 1;
     height: 30fr;
-    width: 100%
+    width: 100%;
+    border: round $boost;
 }
 
 #color-option-list {
     margin: 0 2 0 2;
     background: $panel;
     border: round $panel;
     color: $secondary;
@@ -375,16 +379,18 @@
     width: 100%;
     color: $secondary;
     border: round $secondary;
     text-align: center;
 }
 
 #markdown-container {
-    height: 40;
+    overflow: hidden hidden;
+    height: auto;
     border: round $boost-lighten-3;
+    margin: 0 2 2 0;
 }
 
 #about-markdown {
     margin: 0 2;
 }
     """
     BINDINGS = [
@@ -723,14 +729,15 @@
                     self.color_hex = Color.parse(component)
                 except Exception:
                     self.color_hex = Color.parse("transparent")
 
     
     def on_input_submitted(self, event: Input.Submitted) -> None:
         self.set_focus(None)
+        print(f"{self.query_one('#hex').value}")
 
 def main():
     app = ComputedApp()
     app.run()
     
 if __name__ == "__main__":
     app = ComputedApp()
```

### Comparing `rcp-colors-0.112/rcp_colors.egg-info/PKG-INFO` & `rcp-colors-0.113/rcp_colors.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 Metadata-Version: 2.1
 Name: rcp-colors
-Version: 0.112
+Version: 0.113
 Summary: A Rich Color Picker app
 Home-page: https://github.com/PlusPlusMan/rcp
 Author: PlusPlusMan
 Author-email: contact@plusplusman.com
-Project-URL: Source, https://github.com/PlusPlusMan/rcp/
+Project-URL: Source, https://github.com/PlusPlusMan/RichColorPicker
+Project-URL: Bug Reports, https://github.com/PlusPlusMan/RichColorPicker/issues
 Keywords: color picker,terminal app rgb hsl hex colors
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.6, <4
 Description-Content-Type: text/markdown
 
-Terminal based rich color picker app
+Terminal based rich color picker app. Type rcp-colors in your terminal to start.
```

### Comparing `rcp-colors-0.112/setup.py` & `rcp-colors-0.113/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 setup(
     name='rcp-colors',
-    version='0.112',
+    version='0.113',
     packages=find_packages(),
     description='A Rich Color Picker app',
-    long_description='Terminal based rich color picker app',
+    long_description='Terminal based rich color picker app. Type rcp-colors in your terminal to start.',
     long_description_content_type='text/markdown',
     url='https://github.com/PlusPlusMan/rcp',
     author='PlusPlusMan',
     author_email='contact@plusplusman.com',
     classifiers=[
         'Development Status :: 3 - Alpha',
         'Intended Audience :: Developers',
@@ -20,14 +20,15 @@
     python_requires='>=3.6, <4',
     install_requires=[
         'textual',
         'appdirs',
     ],
     entry_points={
         'console_scripts': [
-            'rcp=rcp_colors.rcp:main',
+            'rcp-colors=rcp_colors.rcp:main',
         ],
     },
     project_urls={
-        'Source': 'https://github.com/PlusPlusMan/rcp/',
+        'Source': 'https://github.com/PlusPlusMan/RichColorPicker',
+        'Bug Reports': 'https://github.com/PlusPlusMan/RichColorPicker/issues'
     },
 )
```

