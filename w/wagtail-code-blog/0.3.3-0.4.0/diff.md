# Comparing `tmp/wagtail-code-blog-0.3.3.tar.gz` & `tmp/wagtail_code_blog-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "wagtail-code-blog-0.3.3.tar", max compression
+gzip compressed data, was "wagtail_code_blog-0.4.0.tar", max compression
```

## Comparing `wagtail-code-blog-0.3.3.tar` & `wagtail_code_blog-0.4.0.tar`

### file list

```diff
@@ -1,27 +1,25 @@
--rw-r--r--   0        0        0      107 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/README.md
--rw-r--r--   0        0        0     1950 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/pyproject.toml
--rw-r--r--   0        0        0        0 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/__init__.py
--rw-r--r--   0        0        0      296 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/apps.py
--rw-r--r--   0        0        0     1830 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0001_initial.py
--rw-r--r--   0        0        0      382 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0002_auto_20200302_0745.py
--rw-r--r--   0        0        0     1110 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0003_auto_20200307_0845.py
--rw-r--r--   0        0        0      437 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0004_auto_20200317_1728.py
--rw-r--r--   0        0        0      617 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0005_blogindexpage_search_image.py
--rw-r--r--   0        0        0        0 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/__init__.py
--rw-r--r--   0        0        0     4485 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/models.py
--rw-r--r--   0        0        0     2064 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/blog_index_page.css
--rw-r--r--   0        0        0      468 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/markdown_code_blocks.css
--rw-r--r--   0        0        0     4073 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/pygments.css
--rw-r--r--   0        0        0      370 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/responsive_width.css
--rw-r--r--   0        0        0    24556 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/images/default_user.png
--rw-r--r--   0        0        0     1697 2022-09-27 00:42:38.460291 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/input.css
--rw-r--r--   0        0        0    11299 2022-09-27 00:42:52.236456 wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/output.css
--rw-r--r--   0        0        0      208 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page.html
--rw-r--r--   0        0        0     1280 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_body.html
--rw-r--r--   0        0        0      216 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_head.html
--rw-r--r--   0        0        0      375 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_page.html
--rw-r--r--   0        0        0     1183 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_page_body.html
--rw-r--r--   0        0        0      678 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_page_head.html
--rw-r--r--   0        0        0      957 2022-09-27 00:42:38.464290 wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/static_dependencies.html
--rw-r--r--   0        0        0     1221 1970-01-01 00:00:00.000000 wagtail-code-blog-0.3.3/setup.py
--rw-r--r--   0        0        0     1489 1970-01-01 00:00:00.000000 wagtail-code-blog-0.3.3/PKG-INFO
+-rw-r--r--   0        0        0      107 2022-10-31 14:09:25.573057 wagtail_code_blog-0.4.0/README.md
+-rw-r--r--   0        0        0     1955 2023-05-13 15:08:56.918693 wagtail_code_blog-0.4.0/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 14:40:36.156994 wagtail_code_blog-0.4.0/wagtail_code_blog/__init__.py
+-rw-r--r--   0        0        0      296 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/apps.py
+-rw-r--r--   0        0        0     1830 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0001_initial.py
+-rw-r--r--   0        0        0      382 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0002_auto_20200302_0745.py
+-rw-r--r--   0        0        0     1110 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0003_auto_20200307_0845.py
+-rw-r--r--   0        0        0      437 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0004_auto_20200317_1728.py
+-rw-r--r--   0        0        0      617 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0005_blogindexpage_search_image.py
+-rw-r--r--   0        0        0        0 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/__init__.py
+-rw-r--r--   0        0        0     4407 2023-05-13 14:49:27.525988 wagtail_code_blog-0.4.0/wagtail_code_blog/models.py
+-rw-r--r--   0        0        0     2064 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/blog_index_page.css
+-rw-r--r--   0        0        0      468 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/markdown_code_blocks.css
+-rw-r--r--   0        0        0     4073 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/pygments.css
+-rw-r--r--   0        0        0      370 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/responsive_width.css
+-rw-r--r--   0        0        0    24556 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/images/default_user.png
+-rw-r--r--   0        0        0     1697 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/input.css
+-rw-r--r--   0        0        0      208 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page.html
+-rw-r--r--   0        0        0     1280 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_body.html
+-rw-r--r--   0        0        0      216 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_head.html
+-rw-r--r--   0        0        0      375 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_page.html
+-rw-r--r--   0        0        0     1183 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_page_body.html
+-rw-r--r--   0        0        0      678 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_page_head.html
+-rw-r--r--   0        0        0      957 2022-10-31 14:09:25.581057 wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/static_dependencies.html
+-rw-r--r--   0        0        0     1547 1970-01-01 00:00:00.000000 wagtail_code_blog-0.4.0/PKG-INFO
```

### Comparing `wagtail-code-blog-0.3.3/pyproject.toml` & `wagtail_code_blog-0.4.0/pyproject.toml`

 * *Files 7% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry>=0.12"]
 build-backend = "poetry.masonry.api"
 
 [tool.poetry]
 name = "wagtail-code-blog"
-version = "0.3.3"
+version = "0.4.0"
 license = "MIT"
 description = "A wagtail code blog"
 authors = ["Dani Hodovic <dani.hodovic@gmail.com>"]
 readme = "README.md"
 homepage = "https://github.com/honeylogic-io/wagtail-code-blog"
 repository = "https://github.com/honeylogic-io/wagtail-code-blog"
 documentation = "https://github.com/honeylogic-io/wagtail-code-blog"
@@ -31,38 +31,38 @@
   "Programming Language :: Python",
   "Programming Language :: Python :: 3",
   "Programming Language :: Python :: 3.9",
 ]
 
 [tool.poetry.dependencies]
 python = ">=3.9,<4.0"
-wagtail = "3.*"
-wagtail-metadata = "4.0.0"
+wagtail = "5.*"
+wagtail-metadata = "4.*"
 readtime = "^1.1.1"
 beautifulsoup4 = "4.8"
 django-json-ld = "^0.0.5 "
 django-model-utils = "^4.2.0"
 django = "4.*"
 
-[tool.poetry.dev-dependencies]
-pytest = "^5.3.5"
+[tool.poetry.group.dev.dependencies]
+pudb = "2022.1.2"
+pytest = "^7.3.1"
 pytest-django = "^3.8.0"
 pytest-gitignore = "^1.3"
 pytest-cov = "^2.8.1"
 coverage = "^5.0.2"
 django-stubs = "^1.4.0"
 black = "22.3.0"
 mypy = "^0.761"
 beautifulsoup4 = "^4.6.0"
 django-extensions = "^3.1.5"
 wagtail-foliage = "^0.1.1"
 isort = "^5.7.0"
-pudb = "^2019.2"
-pylint = "^2.7.2"
-pylint-django = "^2.0.14"
+pylint = "^2.17.4"
+pylint-django = "^2.5.3"
 werkzeug = "^1.0.0"
 wagtail-markdown = "^0.9.0"
 tox = "^3.14.5"
 django-browser-reload = "^1.3.0"
 
 [tool.isort]
 skip_glob = "**/migrations/*.py,**/fixtures/*.py,infra/**/*.py"
```

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0001_initial.py` & `wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0003_auto_20200307_0845.py` & `wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0003_auto_20200307_0845.py`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/migrations/0005_blogindexpage_search_image.py` & `wagtail_code_blog-0.4.0/wagtail_code_blog/migrations/0005_blogindexpage_search_image.py`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/models.py` & `wagtail_code_blog-0.4.0/wagtail_code_blog/models.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 # pylint: disable=arguments-differ,too-few-public-methods
 import readtime
 from bs4 import BeautifulSoup
 from django import forms
 from django.contrib.sites.models import Site
 from django.db import models
 from markdown import markdown
-from wagtail.admin.edit_handlers import FieldPanel, MultiFieldPanel
-from wagtail.core.models import Page
-from wagtail.images.edit_handlers import ImageChooserPanel
+from wagtail.admin.panels import FieldPanel, MultiFieldPanel
 from wagtail.images.models import Image
+from wagtail.models import Page
 from wagtail.search import index
 from wagtail.users.models import UserProfile
 from wagtailmetadata.models import MetadataPageMixin
 
 default_author = "John Doe"
 
 
@@ -43,15 +42,15 @@
 
     subpage_types = ["wagtail_code_blog.BlogPage"]
 
     content_panels = Page.content_panels + [
         FieldPanel("heading"),
         FieldPanel("description"),
         FieldPanel("background_color"),
-        ImageChooserPanel("image"),
+        FieldPanel("image"),
     ]
 
     def get_context(self, request):
         ctx = super().get_context(request)
         ctx["posts"] = (
             BlogPage.objects.child_of(self).live().order_by("-date")  # type:ignore
         )
```

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/blog_index_page.css` & `wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/blog_index_page.css`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/css/pygments.css` & `wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/css/pygments.css`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/images/default_user.png` & `wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/images/default_user.png`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/static/wagtail_code_blog/input.css` & `wagtail_code_blog-0.4.0/wagtail_code_blog/static/wagtail_code_blog/input.css`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_body.html` & `wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_index_page_body.html`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_page_body.html` & `wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_page_body.html`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/blog_page_head.html` & `wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/blog_page_head.html`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/wagtail_code_blog/templates/wagtail_code_blog/static_dependencies.html` & `wagtail_code_blog-0.4.0/wagtail_code_blog/templates/wagtail_code_blog/static_dependencies.html`

 * *Files identical despite different names*

### Comparing `wagtail-code-blog-0.3.3/PKG-INFO` & `wagtail_code_blog-0.4.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: wagtail-code-blog
-Version: 0.3.3
+Version: 0.4.0
 Summary: A wagtail code blog
 Home-page: https://github.com/honeylogic-io/wagtail-code-blog
 License: MIT
 Keywords: wagtail,django,blog,cms
 Author: Dani Hodovic
 Author-email: dani.hodovic@gmail.com
 Requires-Python: >=3.9,<4.0
@@ -15,23 +15,24 @@
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Requires-Dist: beautifulsoup4 (==4.8)
 Requires-Dist: django (>=4.0.0,<5.0.0)
 Requires-Dist: django-json-ld (>=0.0.5,<0.0.6)
 Requires-Dist: django-model-utils (>=4.2.0,<5.0.0)
 Requires-Dist: readtime (>=1.1.1,<2.0.0)
-Requires-Dist: wagtail (>=3.0.0,<4.0.0)
-Requires-Dist: wagtail-metadata (==4.0.0)
+Requires-Dist: wagtail (>=5.0.0,<6.0.0)
+Requires-Dist: wagtail-metadata (>=4.0.0,<5.0.0)
 Project-URL: Documentation, https://github.com/honeylogic-io/wagtail-code-blog
 Project-URL: Repository, https://github.com/honeylogic-io/wagtail-code-blog
 Description-Content-Type: text/markdown
 
 # A code blog for wagtail
 
 Built with wagtail-code-blog:
```

