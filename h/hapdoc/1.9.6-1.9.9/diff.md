# Comparing `tmp/hapdoc-1.9.6.tar.gz` & `tmp/hapdoc-1.9.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hapdoc-1.9.6.tar", last modified: Sat Apr  8 03:29:47 2023, max compression
+gzip compressed data, was "hapdoc-1.9.9.tar", last modified: Wed Apr 12 06:14:33 2023, max compression
```

## Comparing `hapdoc-1.9.6.tar` & `hapdoc-1.9.9.tar`

### file list

```diff
@@ -1,32 +1,32 @@
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.891423 hapdoc-1.9.6/
--rw-rw-rw-   0        0        0     1085 2023-02-05 04:11:14.000000 hapdoc-1.9.6/LICENSE
--rw-rw-rw-   0        0        0       33 2023-03-26 12:25:42.000000 hapdoc-1.9.6/MANIFEST.in
--rw-rw-rw-   0        0        0     3386 2023-04-08 03:29:47.891423 hapdoc-1.9.6/PKG-INFO
--rw-rw-rw-   0        0        0     2546 2023-04-05 05:08:04.000000 hapdoc-1.9.6/README.md
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.861418 hapdoc-1.9.6/hapdoc/
--rw-rw-rw-   0        0        0     1552 2023-04-07 03:20:08.000000 hapdoc-1.9.6/hapdoc/__init__.py
--rw-rw-rw-   0        0        0      143 2023-03-24 08:02:32.000000 hapdoc-1.9.6/hapdoc/__main__.py
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.884427 hapdoc-1.9.6/hapdoc/autodocker/
--rw-rw-rw-   0        0        0     3445 2023-04-05 12:30:09.000000 hapdoc-1.9.6/hapdoc/autodocker/__init__.py
--rw-rw-rw-   0        0        0     1802 2023-04-04 15:32:08.000000 hapdoc-1.9.6/hapdoc/autodocker/abc.py
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.888417 hapdoc-1.9.6/hapdoc/autodocker/filetypes/
--rw-rw-rw-   0        0        0      141 2023-04-04 15:28:59.000000 hapdoc-1.9.6/hapdoc/autodocker/filetypes/__init__.py
--rw-rw-rw-   0        0        0     1588 2023-04-04 15:28:21.000000 hapdoc-1.9.6/hapdoc/autodocker/filetypes/fastapi.py
--rw-rw-rw-   0        0        0     3499 2023-04-05 04:49:11.000000 hapdoc-1.9.6/hapdoc/autodocker/filetypes/js.py
--rw-rw-rw-   0        0        0     4682 2023-04-08 03:27:27.000000 hapdoc-1.9.6/hapdoc/autodocker/filetypes/py.py
--rw-rw-rw-   0        0        0    13119 2023-04-07 16:11:06.000000 hapdoc-1.9.6/hapdoc/hapdoc.py
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.889417 hapdoc-1.9.6/hapdoc/md/
--rw-rw-rw-   0        0        0     3936 2023-04-05 14:12:12.000000 hapdoc-1.9.6/hapdoc/md/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.855420 hapdoc-1.9.6/hapdoc/templates/
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.889417 hapdoc-1.9.6/hapdoc/templates/vitepress/
--rw-rw-rw-   0        0        0    18129 2023-04-07 03:35:17.000000 hapdoc-1.9.6/hapdoc/templates/vitepress/index.html
--rw-rw-rw-   0        0        0     4982 2023-04-05 12:43:48.000000 hapdoc-1.9.6/hapdoc/utils.py
-drwxrwxrwx   0        0        0        0 2023-04-08 03:29:47.883422 hapdoc-1.9.6/hapdoc.egg-info/
--rw-rw-rw-   0        0        0     3386 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      553 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       49 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       29 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-04-08 03:29:47.000000 hapdoc-1.9.6/hapdoc.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-08 03:29:47.891423 hapdoc-1.9.6/setup.cfg
--rw-rw-rw-   0        0        0     1878 2023-04-08 03:29:21.000000 hapdoc-1.9.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.026356 hapdoc-1.9.9/
+-rw-rw-rw-   0        0        0     1085 2023-02-05 04:11:14.000000 hapdoc-1.9.9/LICENSE
+-rw-rw-rw-   0        0        0       33 2023-03-26 12:25:42.000000 hapdoc-1.9.9/MANIFEST.in
+-rw-rw-rw-   0        0        0     3599 2023-04-12 06:14:33.024340 hapdoc-1.9.9/PKG-INFO
+-rw-rw-rw-   0        0        0     2759 2023-04-12 05:20:44.000000 hapdoc-1.9.9/README.md
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:32.974349 hapdoc-1.9.9/hapdoc/
+-rw-rw-rw-   0        0        0     1552 2023-04-12 06:06:26.000000 hapdoc-1.9.9/hapdoc/__init__.py
+-rw-rw-rw-   0        0        0      143 2023-03-24 08:02:32.000000 hapdoc-1.9.9/hapdoc/__main__.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.007342 hapdoc-1.9.9/hapdoc/autodocker/
+-rw-rw-rw-   0        0        0     3600 2023-04-12 05:54:44.000000 hapdoc-1.9.9/hapdoc/autodocker/__init__.py
+-rw-rw-rw-   0        0        0     1802 2023-04-04 15:32:08.000000 hapdoc-1.9.9/hapdoc/autodocker/abc.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.017345 hapdoc-1.9.9/hapdoc/autodocker/filetypes/
+-rw-rw-rw-   0        0        0      141 2023-04-04 15:28:59.000000 hapdoc-1.9.9/hapdoc/autodocker/filetypes/__init__.py
+-rw-rw-rw-   0        0        0     1588 2023-04-04 15:28:21.000000 hapdoc-1.9.9/hapdoc/autodocker/filetypes/fastapi.py
+-rw-rw-rw-   0        0        0     3499 2023-04-05 04:49:11.000000 hapdoc-1.9.9/hapdoc/autodocker/filetypes/js.py
+-rw-rw-rw-   0        0        0     4682 2023-04-08 03:27:27.000000 hapdoc-1.9.9/hapdoc/autodocker/filetypes/py.py
+-rw-rw-rw-   0        0        0    13597 2023-04-12 06:10:14.000000 hapdoc-1.9.9/hapdoc/hapdoc.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.019341 hapdoc-1.9.9/hapdoc/md/
+-rw-rw-rw-   0        0        0     3936 2023-04-05 14:12:12.000000 hapdoc-1.9.9/hapdoc/md/__init__.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:32.954342 hapdoc-1.9.9/hapdoc/templates/
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.021352 hapdoc-1.9.9/hapdoc/templates/vitepress/
+-rw-rw-rw-   0        0        0    15504 2023-04-12 05:35:05.000000 hapdoc-1.9.9/hapdoc/templates/vitepress/index.html
+-rw-rw-rw-   0        0        0     5365 2023-04-12 06:11:49.000000 hapdoc-1.9.9/hapdoc/utils.py
+drwxrwxrwx   0        0        0        0 2023-04-12 06:14:33.001345 hapdoc-1.9.9/hapdoc.egg-info/
+-rw-rw-rw-   0        0        0     3599 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      553 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       49 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       29 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-04-12 06:14:32.000000 hapdoc-1.9.9/hapdoc.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-04-12 06:14:33.027361 hapdoc-1.9.9/setup.cfg
+-rw-rw-rw-   0        0        0     1925 2023-04-12 04:31:26.000000 hapdoc-1.9.9/setup.py
```

### Comparing `hapdoc-1.9.6/LICENSE` & `hapdoc-1.9.9/LICENSE`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/PKG-INFO` & `hapdoc-1.9.9/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hapdoc
-Version: 1.9.6
+Version: 1.9.9
 Summary: autodoc tool for everything
 Home-page: https://github.com/HapticX/hapdoc
 Author: Ethosa
 Author-email: social.ethosa@gmail.com
 Maintainer: HapticX
 Maintainer-email: hapticx.company@gmail.com
 License: MIT
@@ -45,16 +45,19 @@
 ### Features :sparkles:
 - Supported projects:
   - `Python`
   - `FastAPI`
   - `JavaScript`
 - Generate Markdown docs via `gen` command.
 - Build docs into HTML via `build` command.
+- Build Markdown docs into JSON via `md2json` command.
 - Serve generated docs at your server via `serve` command.
-- Create your own templates via `tmpl-new` command.
+- Create your own templates via `tmpl-new`.
+- See your saved templates via `tmpl-list`.
+- Prepare your docs with [`project.hapdoc`](https://github.com/HapticX/hapdoc/blob/master/project.hapdoc) config file.
 
 ## Installing 📥
 via `pypi` 📦
 ```bash
 pip install hapdoc --upgrade
 ```
 via `git` 💾
```

### Comparing `hapdoc-1.9.6/README.md` & `hapdoc-1.9.9/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -21,16 +21,19 @@
 ### Features :sparkles:
 - Supported projects:
   - `Python`
   - `FastAPI`
   - `JavaScript`
 - Generate Markdown docs via `gen` command.
 - Build docs into HTML via `build` command.
+- Build Markdown docs into JSON via `md2json` command.
 - Serve generated docs at your server via `serve` command.
-- Create your own templates via `tmpl-new` command.
+- Create your own templates via `tmpl-new`.
+- See your saved templates via `tmpl-list`.
+- Prepare your docs with [`project.hapdoc`](https://github.com/HapticX/hapdoc/blob/master/project.hapdoc) config file.
 
 ## Installing 📥
 via `pypi` 📦
 ```bash
 pip install hapdoc --upgrade
 ```
 via `git` 💾
```

### Comparing `hapdoc-1.9.6/hapdoc/__init__.py` & `hapdoc-1.9.9/hapdoc/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -34,8 +34,8 @@
 - `project-types`: Displays available project types.
 - `serve`: Starts server at host and port.
 - `tmpl-list`: List of saved templates.
 - `tmpl-new`: Create a new template.
 
 """
 
-__version__ = '1.9.3'
+__version__ = '1.9.9'
```

### Comparing `hapdoc-1.9.6/hapdoc/autodocker/__init__.py` & `hapdoc-1.9.9/hapdoc/autodocker/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -96,21 +96,24 @@
     :param output_dir: output directory name
     :param ignore_files: ignore file extensions list
     :param extend: extended file types list
     :param file_types: dictionary of supported file types
     :return:
     """
     # Exclude ignored file extensions
+    for ptype in extend:
+        for i in _config[ptype]['file_types']:
+            if i not in ignore_files:
+                file_types[i] = _config[ptype]['file_types'][i]
     file_extensions = (
         [i for i in file_types.keys() if i not in ignore_files]
         if ignore_files else
         list(file_types)
     )
-    if extend:
-        file_extensions += extend
+    print(file_extensions)
     if path.isdir(project_path):
         # Project path is directory
         files = [i for i in _iter_dir(project_path) if path.splitext(i)[1] in file_extensions]
         length = len(files)
         for i, filename in enumerate(files):
             _, ext = path.splitext(filename)
             file_types[ext].process(file_types[ext], f'{path.join(project_path, filename)}', output_dir)
```

### Comparing `hapdoc-1.9.6/hapdoc/autodocker/abc.py` & `hapdoc-1.9.9/hapdoc/autodocker/abc.py`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/hapdoc/autodocker/filetypes/fastapi.py` & `hapdoc-1.9.9/hapdoc/autodocker/filetypes/fastapi.py`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/hapdoc/autodocker/filetypes/js.py` & `hapdoc-1.9.9/hapdoc/autodocker/filetypes/js.py`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/hapdoc/autodocker/filetypes/py.py` & `hapdoc-1.9.9/hapdoc/autodocker/filetypes/py.py`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/hapdoc/hapdoc.py` & `hapdoc-1.9.9/hapdoc/hapdoc.py`

 * *Files 10% similar despite different names*

```diff
@@ -14,15 +14,16 @@
 from fastapi import status
 from jinja2 import FileSystemLoader, Environment, select_autoescape
 
 from .md import Md2Html
 from .utils import (
     show_all_projects, generate_md_files,
     cast_md_dir_to_json, load_user_templates,
-    create_new_user_template, get_user_template_path
+    create_new_user_template, get_user_template_path,
+    load_conf
 )
 from . import __version__
 
 
 app = FastAPI(docs_url=None, redoc_url=None)
 app.add_middleware(
     CORSMiddleware,
@@ -60,15 +61,15 @@
 
 @hapdoc.command()
 def tmpl_list():
     """
     This command displays a list of all templates that have been saved by the current user.
     It is useful for quickly checking which templates are available for use.
     """
-    templates_list = load_user_templates()
+    load_user_templates()
 
 
 @hapdoc.command()
 def tmpl_new():
     """
     The `tml_new` command creates a new template and saves it for future use.
     The user will be prompted to provide a name for the template and
@@ -88,33 +89,37 @@
     '-O', '--outdir', 'output_directory',
     help='Output directory path',
     default=None, type=str
 )
 @click.option(
     '-r', '--root', 'root',
     help='Root path, by default uses working directory',
-    default='', type=str
+    default=None, type=str
 )
 @click.option(
     '-e', '--extension', 'ext',
     help='File extensions in generated JSON',
     default=None, type=str
 )
 def md2json(directory: str, output_directory: str, output_file: str, root: str, ext: str):
     """
     The md2json command converts Markdown files (.md) in a directory to JSON format,
     which can be used for rendering the files using the jinja2 templating engine.
     This command is useful for converting Markdown files to a format that
     can be easily parsed and manipulated by other tools.
     """
+    root = load_conf('root', root, '')
+
     if ext is None:
         ext = ".md"
     data = cast_md_dir_to_json(directory, root, False, ext)
     click.echo(click.style("Generated", fg="bright_green"))
 
+    root = load_conf('root', root)
+
     if output_directory is not None:
         makedirs(output_directory, exist_ok=True)
         with open(path.join(output_directory, output_file), 'w', encoding='utf-8') as file:
             file.write(dumps(data, indent=4))
         click.echo(click.style(f"Saved at {output_directory}/{output_file}", fg="bright_green"))
     else:
         with open(output_file, 'w', encoding='utf-8') as file:
@@ -133,15 +138,15 @@
     '-i', '--ignore', 'ignore',
     help='Ignore file extensions separated by comma',
     default='', type=str
 )
 @click.option(
     '-e', '--extend', 'extend',
     help='Extend doc by specified doctypes separated by comma',
-    default='', type=str
+    default=None, type=str
 )
 @click.option(
     '-o', '--out', 'output',
     help='Output docs folder',
     default='docs', type=str
 )
 def gen(
@@ -166,19 +171,19 @@
 )
 @click.option(
     '-p', '--port', 'port',
     default='5000', type=str
 )
 @click.option(
     '-t', '--template', 'templates_folder',
-    default='hapdoc/templates/vitepress', type=str
+    default=None, type=str
 )
 @click.option(
     '-T', '--title', 'title',
-    default='HapDoc', type=str
+    default=None, type=str
 )
 @click.option(
     '-a', '--accent', 'accent_color',
     default='#c27bd4', type=str
 )
 @click.option(
     '-b', '--background', 'background_color',
@@ -202,15 +207,15 @@
     '-ls', '--light-surface', 'light_surface_color',
     help='Light Surface color',
     default='#dedede', type=str
 )
 @click.option(
     '-dv', '--doc-version', 'doc_version',
     help='Generated documentation version',
-    default='1.0.0', type=str
+    default=None, type=str
 )
 def serve(
         host: str,
         port: str,
         docs: str,
         templates_folder: str,
         title: str,
@@ -222,14 +227,18 @@
         light_surface_color: str,
         doc_version: str,
 ):
     """
     The `serve` command starts a web server using FastAPI and uvicorn and
     provides access to Markdown files in a web browser.
     """
+    doc_version = load_conf('version', doc_version, '1.0.0')
+    title = load_conf('title', title, 'HapDoc')
+    templates_folder = load_conf('template', templates_folder, 'hapdoc/templates/vitepress')
+
     user_template = get_user_template_path(templates_folder)
     env = Environment(
         loader=FileSystemLoader(user_template if user_template else templates_folder),
         autoescape=select_autoescape()
     )
     template = env.get_template('index.html')
     sidebar = cast_md_dir_to_json(docs)
@@ -287,29 +296,29 @@
     '-i', '--ignore', 'ignore',
     help='Ignore file extensions separated by comma',
     default='', type=str
 )
 @click.option(
     '-e', '--extend', 'extend',
     help='Extend doc by specified docs types separated by comma',
-    default='', type=str
+    default=None, type=str
 )
 @click.option(
     '-o', '--out', 'output',
     help='Output docs folder',
     default='buildocs', type=str
 )
 @click.option(
     '-t', '--template', 'templates_folder',
-    default='hapdoc/templates/vitepress', type=str
+    default=None, type=str
 )
 @click.option(
     '-T', '--title', 'title',
     help='Page title',
-    default='HapDoc', type=str
+    default=None, type=str
 )
 @click.option(
     '-a', '--accent', 'accent_color',
     help='Accent color',
     default='#c27bd4', type=str
 )
 @click.option(
@@ -341,15 +350,15 @@
     '-r', '--root', 'root',
     help='Root path, by default uses working directory',
     default=None, type=str
 )
 @click.option(
     '-dv', '--doc-version', 'doc_version',
     help='Generated documentation version',
-    default='1.0.0', type=str
+    default=None, type=str
 )
 def build(
         docs: str,
         templates_folder: str,
         title: str,
         accent_color: str,
         background_color: str,
@@ -364,14 +373,19 @@
         root: str,
         doc_version: str,
 ):
     """
     This command generates documentation for a project by first creating Markdown
     files and then converting them to HTML files.
     """
+    doc_version = load_conf('version', doc_version, '1.0.0')
+    root = load_conf('root', root, '/')
+    title = load_conf('title', title, 'HapDoc')
+    templates_folder = load_conf('template', templates_folder, 'hapdoc/templates/vitepress')
+
     user_template = get_user_template_path(templates_folder)
     env = Environment(
         loader=FileSystemLoader(user_template if user_template else templates_folder),
         autoescape=select_autoescape()
     )
     template = env.get_template('index.html')
     generate_md_files(docs, document_type, ignore, extend, output)
```

### Comparing `hapdoc-1.9.6/hapdoc/md/__init__.py` & `hapdoc-1.9.9/hapdoc/md/__init__.py`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/hapdoc/templates/vitepress/index.html` & `hapdoc-1.9.9/hapdoc/templates/vitepress/index.html`

 * *Files 18% similar despite different names*

```diff
@@ -58,17 +58,21 @@
           >
             <i id="themeIcon" class="fas fa-moon absolute"></i>
           </div>
           <p id="themeString" class="w-16">Dark</p>
         </div>
       </div>
     </div>
-    <!-- SideBar (desktop) -->
-    <div class="hidden xl:block xl:fixed left-0 top-12 flex flex-col w-3/12 z-40 dark:bg-surface-color bg-light-surface-color min-h-screen h-full">
-      <div class="ml-36 pt-2 mr-2 border-t-[1px] dark:border-white/10 border-black/10 border-t-[1px]" id="line"></div>
+
+    <!-- SideBar -->
+    <div
+      class="fixed w-full xl:w-3/12 xl:block left-0 top-12 flex flex-col z-40 text-2xl xl:text-base dark:bg-surface-color bg-light-surface-color min-h-screen h-full transition-all"
+      id="sidebar"
+    >
+      <div class="hidden xl:block ml-36 pt-2 mr-2 border-t-[1px] dark:border-white/10 border-black/10 border-t-[1px]" id="line"></div>
       <div class="flex flex-col gap-2 pl-32 h-full">
         {% macro sidebar(key, item) %}
           <!-- SideBar item -->
           <div class="flex flex-col gap-2 border-white border-opacity-10 mt-2">
             <div class="flex pl-2 flex-col w-full font-bold">
               {% if item._items %}
                 <div class="flex w-full items-center gap-2 cursor-pointer" onclick="toggleList('{{ item._data.id }}')">
@@ -85,15 +89,15 @@
                   {% for k, i in item._items.items() %}
                     {% if not i._data.url %}
                       {{- sidebar(key, i) -}}
                     {% else %}
                       <a
                         href="{{ i._data.url }}"
                         id="{{ i._data.url }}href"
-                        class="select-none pl-8 opacity-50 hover:opacity-100 transition-all duration-300">
+                        class="select-none pl-8 opacity-50 hover:opacity-100 transition-all duration-700">
                         {{ i._data.title }}
                       </a>
                     {% endif %}
                   {% endfor %}
                 </div>
               {% else %}
                 <a
@@ -110,62 +114,14 @@
           {% for key, item in side.items() %}
             {{ sidebar(key, item) }}
           {% endfor %}
         </div>
       </div>
     </div>
 
-    <!-- Sidebar (mobile) -->
-    <div class="fixed top-12 left-0 z-40 w-full h-full flex flex-col gap-2 text-2xl dark:bg-surface-color bg-light-surface-color transition-all" id="sideBarPhone">
-      {% macro sidebar_mobile(key, item) %}
-        <!-- SideBar item -->
-        <div class="flex flex-col gap-2 dark:border-white border-black border-opacity-10 mt-2">
-          <div class="flex pl-2 flex-col w-full font-bold">
-            {% if item._items %}
-              <div class="flex w-full items-center gap-2 cursor-pointer" onclick="toggleList('{{ item._data.id }}')">
-                <i
-                  class="fas fa-sort-down opacity-70 transition-all ease-out select-none"
-                  id="{{ item._data.id }}-icon-mobile"
-                ></i>
-                <p class="select-none">
-                  {{ item._data.title }}
-                </p>
-              </div>
-              <div class="flex flex-col h-fit w-full" id="{{ item._data.id }}-list-mobile" style="display: flex">
-                {% for k, i in item._items.items() %}
-                  {% if not i._data.url %}
-                    {{- sidebar_mobile(key, i) -}}
-                  {% else %}
-                    <a
-                      href="{{ i._data.url }}"
-                      id="{{ i._data.url }}hrefMobile"
-                      class="select-none pl-8 opacity-50 hover:opacity-100 transition-all duration-300">
-                      {{ i._data.title }}
-                    </a>
-                  {% endif %}
-                {% endfor %}
-              </div>
-            {% else %}
-              <a
-                href="{{ item._data.url }}"
-                id="{{ item._data.url }}hrefMobile"
-                class="select-none pl-8 w-full opacity-50 hover:opacity-100 transition-all duration-300">
-                {{ item._data.title }}
-              </a>
-            {% endif %}
-          </div>
-        </div>
-      {% endmacro %}
-      <div class="px-2">
-        {% for key, item in side.items() %}
-          {{ sidebar_mobile(key, item) }}
-        {% endfor %}
-      </div>
-    </div>
-
     <div class="h-full w-3/12 hidden xl:block"></div>
 
     <!-- Content -->
     <div class="w-full xl:w-9/12 xl:pr-64 py-4 dark:bg-background-color bg-light-background-color relative">
       <div class="w-full h-full pt-20 flex px-12 xl:px-32 gap-20">
         <!-- Page data -->
         <div class="flex flex-col gap-4 w-full xl:w-3/4">
@@ -345,15 +301,15 @@
     }
   </style>
 
   <script>
     // Get elements
     const titleRefs = document.getElementsByClassName("titleRef");
     const header = document.getElementById('header');
-    const sidebar = document.getElementById('sideBarPhone');
+    const sidebar = document.getElementById('sidebar');
     const sandwich = document.getElementById('sandwich');
     const themeIcon = document.getElementById('themeIcon');
     const themeString = document.getElementById('themeString');
     const themeButton = document.getElementById('themeButton');
     const titleRefsArray = [...titleRefs];
 
     let isDark = true;
@@ -400,28 +356,22 @@
         link.style.visibility = 'hidden';
       })
     });
 
     function toggleList(itemID) {
       const listElem = document.getElementById(`${itemID}-list`);
       const iconElem = document.getElementById(`${itemID}-icon`);
-      const listElemMobile = document.getElementById(`${itemID}-list-mobile`);
-      const iconElemMobile = document.getElementById(`${itemID}-icon-mobile`);
 
       // toggle
       listElem.style.display === 'flex' ? (() => {
         listElem.style.display = 'none';
         iconElem.style.transform = 'rotate(-90deg)';
-        listElemMobile.style.display = 'none';
-        iconElemMobile.style.transform = 'rotate(-90deg)';
       })() : (() => {
         listElem.style.display = 'flex';
         iconElem.style.transform = 'rotate(0deg)';
-        listElemMobile.style.display = 'flex';
-        iconElemMobile.style.transform = 'rotate(0deg)';
       })();
     }
 
     // Mobile
     let showSidebar = true;
     function sideBarSwitcher() {
       showSidebar = !showSidebar;
@@ -449,27 +399,22 @@
         pageEl.classList.toggle('opacity-90', isSelected);
         pageEl.classList.toggle('opacity-60', !isSelected);
       }
     }
 
     {% if selected %}
       const href = document.getElementById("{{ selected }}href");
-      const hrefMobile = document.getElementById("{{ selected }}hrefMobile");
       href.className += " opacity-90 dark:text-accent-color text-light-accent-color";
-      hrefMobile.className += " opacity-90 dark:text-accent-color text-light-accent-color";
     {% endif %}
 
-    window.addEventListener("scroll", ev => {
-      checkScroll(window.scrollY);
-    });
-
-    window.addEventListener("load", ev => {checkScroll(window.scrollY)});
+    window.addEventListener("scroll", ev => checkScroll(window.scrollY));
+    window.addEventListener("load", ev => checkScroll(window.scrollY));
 
     sandwich.addEventListener('click', sideBarSwitcher);
-    sideBarSwitcher();
+    // sideBarSwitcher();
 
     function handleTheme(changed) {
       if (changed) {
         if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
           document.documentElement.className = 'dark';
           localStorage.theme = 'dark';
           isDark = true;
```

#### html2text {}

```diff
@@ -14,20 +14,10 @@
 {% if item._items %}
 {{ item._data.title }}
 {% for k, i in item._items.items() %} {% if not i._data.url %} {{- sidebar(key,
 i) -}} {% else %} {{_i._data.title_}} {% endif %} {% endfor %}
 {% else %} {{_item._data.title_}} {% endif %}
 {% endmacro %}
 {% for key, item in side.items() %} {{ sidebar(key, item) }} {% endfor %}
-{% macro sidebar_mobile(key, item) %}
-{% if item._items %}
-{{ item._data.title }}
-{% for k, i in item._items.items() %} {% if not i._data.url %} {{-
-sidebar_mobile(key, i) -}} {% else %} {{_i._data.title_}} {% endif %} {% endfor
-%}
-{% else %} {{_item._data.title_}} {% endif %}
-{% endmacro %}
-{% for key, item in side.items() %} {{ sidebar_mobile(key, item) }} {% endfor
-%}
 {{ pageData|safe }}
 On this page
 {% for i in titleRefs %} {{_i.title|safe_}} {% endfor %}
```

### Comparing `hapdoc-1.9.6/hapdoc/utils.py` & `hapdoc-1.9.9/hapdoc/utils.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,21 +2,32 @@
 """
 Provides some CLI utils
 """
 import click
 from os import path, makedirs, listdir, sep
 from time import time
 from glob import glob
+from configparser import ConfigParser
 
 from .autodocker import all_project_types, generate
 
 
 _DIRECTORY = path.join(path.expanduser('~'), 'HapticX', 'hapdoc', 'templates')
 _LIBRARY_PATH = path.abspath(__file__).replace('\\', '/').rsplit('/', 1)[0]
 
+_CONFIG = ConfigParser(inline_comment_prefixes=('#', ';'))
+_CONFIG.read("project.hapdoc")
+_CONFIG = _CONFIG['HapDoc']
+
+
+def load_conf(key: str, argument: str | None, default: str) -> str:
+    if argument is None:
+        return _CONFIG.get(key, fallback=default)
+    return argument
+
 
 def show_all_projects():
     """Shows all project types"""
     all_types = all_project_types()
     for project_type in all_types:
         click.echo(f'- {project_type}')
 
@@ -65,14 +76,15 @@
 
     :param project_path: Path to project directory or file
     :param document_type: Available file extension
     :param ignore: Ignore file extensions separated by comma
     :param extend: Extend file extensions separated by comma
     :param output: Output directory
     """
+    extend = extend.split(',') if extend else []
     ignore_list = [
         ext.strip() if ext.strip().startswith('.') else f'.{ext.strip()}'
         for ext in ignore.split(',')
     ]
     start = time()
     with click.progressbar(
             label='Generating docs',
```

### Comparing `hapdoc-1.9.6/hapdoc.egg-info/PKG-INFO` & `hapdoc-1.9.9/hapdoc.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hapdoc
-Version: 1.9.6
+Version: 1.9.9
 Summary: autodoc tool for everything
 Home-page: https://github.com/HapticX/hapdoc
 Author: Ethosa
 Author-email: social.ethosa@gmail.com
 Maintainer: HapticX
 Maintainer-email: hapticx.company@gmail.com
 License: MIT
@@ -45,16 +45,19 @@
 ### Features :sparkles:
 - Supported projects:
   - `Python`
   - `FastAPI`
   - `JavaScript`
 - Generate Markdown docs via `gen` command.
 - Build docs into HTML via `build` command.
+- Build Markdown docs into JSON via `md2json` command.
 - Serve generated docs at your server via `serve` command.
-- Create your own templates via `tmpl-new` command.
+- Create your own templates via `tmpl-new`.
+- See your saved templates via `tmpl-list`.
+- Prepare your docs with [`project.hapdoc`](https://github.com/HapticX/hapdoc/blob/master/project.hapdoc) config file.
 
 ## Installing 📥
 via `pypi` 📦
 ```bash
 pip install hapdoc --upgrade
 ```
 via `git` 💾
```

### Comparing `hapdoc-1.9.6/hapdoc.egg-info/SOURCES.txt` & `hapdoc-1.9.9/hapdoc.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `hapdoc-1.9.6/setup.py` & `hapdoc-1.9.9/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 """
 Provides setup script
 """
 from os import path, makedirs
-from setuptools import setup, find_packages
+from setuptools import setup, find_packages, version
+
+from hapdoc import __version__
 
 
 # Load readme
 with open('README.md', 'r', encoding='utf-8') as file:
     long_description = file.read()
 
 
@@ -26,15 +28,15 @@
     long_description=long_description,
     long_description_content_type='text/markdown',
     author='Ethosa',
     author_email='social.ethosa@gmail.com',
     maintainer='HapticX',
     maintainer_email='hapticx.company@gmail.com',
     url='https://github.com/HapticX/hapdoc',
-    version='1.9.6',
+    version=__version__,
     packages=find_packages(),
     py_modules=['hapdoc'],
     install_requires=['click', 'fastapi', 'uvicorn', 'jinja2'],
     package_data={
         'hapdoc': ['*.html']
     },
     include_package_data=True,
```

