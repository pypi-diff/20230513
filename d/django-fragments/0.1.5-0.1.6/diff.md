# Comparing `tmp/django_fragments-0.1.5.tar.gz` & `tmp/django_fragments-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_fragments-0.1.5.tar", max compression
+gzip compressed data, was "django_fragments-0.1.6.tar", max compression
```

## Comparing `django_fragments-0.1.5.tar` & `django_fragments-0.1.6.tar`

### file list

```diff
@@ -1,30 +1,32 @@
--rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.5/LICENSE
--rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.5/README.md
--rw-r--r--   0        0        0       36 2023-05-12 14:54:30.129104 django_fragments-0.1.5/django_fragments/__init__.py
--rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.5/django_fragments/apps.py
--rw-r--r--   0        0        0     1255 2023-05-12 14:54:30.129513 django_fragments-0.1.5/django_fragments/forms.py
--rw-r--r--   0        0        0     7217 2023-05-12 14:54:30.130087 django_fragments-0.1.5/django_fragments/static/chooseDown.js
--rw-r--r--   0        0        0      823 2023-05-12 14:54:30.130507 django_fragments-0.1.5/django_fragments/templates/_nav.html
--rw-r--r--   0        0        0      743 2023-05-12 14:54:30.130818 django_fragments-0.1.5/django_fragments/templates/_test.html
--rw-r--r--   0        0        0      192 2023-05-12 14:54:30.130994 django_fragments-0.1.5/django_fragments/templates/about.html
--rw-r--r--   0        0        0      470 2023-05-12 14:54:30.131347 django_fragments-0.1.5/django_fragments/templates/contact.html
--rw-r--r--   0        0        0     1839 2023-05-12 14:54:30.131597 django_fragments-0.1.5/django_fragments/templates/down-list.html
--rw-r--r--   0        0        0      232 2023-05-12 14:54:30.131849 django_fragments-0.1.5/django_fragments/templates/home.html
--rw-r--r--   0        0        0      310 2023-05-12 14:54:30.132221 django_fragments-0.1.5/django_fragments/templates/item.html
--rw-r--r--   0        0        0      582 2023-05-12 14:54:30.132477 django_fragments-0.1.5/django_fragments/templates/msg.html
--rw-r--r--   0        0        0      331 2023-05-12 14:54:30.133019 django_fragments-0.1.5/django_fragments/templates/msg_form.html
--rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.5/django_fragments/templates/svg/heroicons_x_mark_mini.html
--rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.5/django_fragments/templates/test_snippet.html
--rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.5/django_fragments/templatetags/__init__.py
--rw-r--r--   0        0        0     6118 2023-05-11 16:23:17.630674 django_fragments-0.1.5/django_fragments/templatetags/fragments.py
--rw-r--r--   0        0        0     3435 2023-05-11 07:56:55.689314 django_fragments-0.1.5/django_fragments/templatetags/helpers.py
--rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.5/django_fragments/templatetags/og.py
--rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.5/django_fragments/templatetags/utils/__init__.py
--rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.5/django_fragments/templatetags/utils/filter_attrs.py
--rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.5/django_fragments/templatetags/utils/wrap_svg.py
--rw-r--r--   0        0        0     3279 2023-05-12 14:54:30.133346 django_fragments-0.1.5/django_fragments/tests.py
--rw-r--r--   0        0        0      472 2023-05-12 14:54:30.133617 django_fragments-0.1.5/django_fragments/urls.py
--rw-r--r--   0        0        0      579 2023-05-12 14:54:30.133874 django_fragments-0.1.5/django_fragments/utils.py
--rw-r--r--   0        0        0     1910 2023-05-12 14:54:30.134176 django_fragments-0.1.5/django_fragments/views.py
--rw-r--r--   0        0        0     1471 2023-05-12 15:08:33.821273 django_fragments-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     1536 1970-01-01 00:00:00.000000 django_fragments-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.6/LICENSE
+-rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.6/README.md
+-rw-r--r--   0        0        0       36 2023-05-12 14:54:30.129104 django_fragments-0.1.6/django_fragments/__init__.py
+-rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.6/django_fragments/apps.py
+-rw-r--r--   0        0        0     1705 2023-05-13 08:03:42.389176 django_fragments-0.1.6/django_fragments/forms.py
+-rw-r--r--   0        0        0     6126 2023-05-13 08:03:42.389593 django_fragments-0.1.6/django_fragments/static/doDropCommon.js
+-rw-r--r--   0        0        0     1008 2023-05-13 08:03:42.389898 django_fragments-0.1.6/django_fragments/static/doDropMenu.js
+-rw-r--r--   0        0        0     1543 2023-05-13 08:03:42.390306 django_fragments-0.1.6/django_fragments/static/doDropSelect.js
+-rw-r--r--   0        0        0      758 2023-05-13 08:03:42.390796 django_fragments-0.1.6/django_fragments/static/doTheme.js
+-rw-r--r--   0        0        0      695 2023-05-13 08:03:42.391367 django_fragments-0.1.6/django_fragments/templates/_nav.html
+-rw-r--r--   0        0        0      200 2023-05-13 08:03:42.391887 django_fragments-0.1.6/django_fragments/templates/about.html
+-rw-r--r--   0        0        0     1003 2023-05-13 08:03:42.392303 django_fragments-0.1.6/django_fragments/templates/base_template.html
+-rw-r--r--   0        0        0      478 2023-05-13 08:03:42.392713 django_fragments-0.1.6/django_fragments/templates/contact.html
+-rw-r--r--   0        0        0      404 2023-05-13 08:03:42.393026 django_fragments-0.1.6/django_fragments/templates/down-list.html
+-rw-r--r--   0        0        0      240 2023-05-13 08:03:42.393455 django_fragments-0.1.6/django_fragments/templates/home.html
+-rw-r--r--   0        0        0      582 2023-05-12 14:54:30.132477 django_fragments-0.1.6/django_fragments/templates/msg.html
+-rw-r--r--   0        0        0      405 2023-05-12 16:28:19.371173 django_fragments-0.1.6/django_fragments/templates/msg_form.html
+-rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.6/django_fragments/templates/svg/heroicons_x_mark_mini.html
+-rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.6/django_fragments/templates/test_snippet.html
+-rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.6/django_fragments/templatetags/__init__.py
+-rw-r--r--   0        0        0     6118 2023-05-11 16:23:17.630674 django_fragments-0.1.6/django_fragments/templatetags/fragments.py
+-rw-r--r--   0        0        0     3435 2023-05-11 07:56:55.689314 django_fragments-0.1.6/django_fragments/templatetags/helpers.py
+-rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.6/django_fragments/templatetags/og.py
+-rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.6/django_fragments/templatetags/utils/__init__.py
+-rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.6/django_fragments/templatetags/utils/filter_attrs.py
+-rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.6/django_fragments/templatetags/utils/wrap_svg.py
+-rw-r--r--   0        0        0     3279 2023-05-12 14:54:30.133346 django_fragments-0.1.6/django_fragments/tests.py
+-rw-r--r--   0        0        0      472 2023-05-12 14:54:30.133617 django_fragments-0.1.6/django_fragments/urls.py
+-rw-r--r--   0        0        0      579 2023-05-12 14:54:30.133874 django_fragments-0.1.6/django_fragments/utils.py
+-rw-r--r--   0        0        0     1910 2023-05-12 14:54:30.134176 django_fragments-0.1.6/django_fragments/views.py
+-rw-r--r--   0        0        0     1438 2023-05-13 08:03:42.396103 django_fragments-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0     1482 1970-01-01 00:00:00.000000 django_fragments-0.1.6/PKG-INFO
```

### Comparing `django_fragments-0.1.5/LICENSE` & `django_fragments-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/README.md` & `django_fragments-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/forms.py` & `django_fragments-0.1.6/django_fragments/forms.py`

 * *Files 21% similar despite different names*

```diff
@@ -9,20 +9,33 @@
     class MessageTag(models.IntegerChoices):
         DEBUG = 10
         INFO = 20
         SUCCESS = 25
         WARNING = 30
         ERROR = 40
 
+    class OtherCategory(models.IntegerChoices):
+        IMPORTANT = 10
+        MEH = 20
+        INUTILE = 25
+
     message = forms.CharField(label="Message", widget=forms.Textarea(attrs={"rows": 3}))
     tag = forms.TypedChoiceField(
         label="Tag",
         choices=MessageTag.choices,
         initial=MessageTag.DEBUG,
         help_text="This is a message tag",
+        widget=forms.Select(attrs={"hidden": True}),
+    )
+    cat = forms.TypedChoiceField(
+        label="Relevance",
+        choices=OtherCategory.choices,
+        initial=OtherCategory.MEH,
+        help_text="This is a category",
+        widget=forms.Select(attrs={"hidden": True}),
     )
 
 
 class ContactForm(forms.Form):
     class Category(models.TextChoices):
         YES = "yes", _("Yes, I approve")
         NO = "no", _("No, I do not")
@@ -32,10 +45,11 @@
 
     template_name = "test_snippet.html"
     category = forms.TypedChoiceField(
         label="Thoughts",
         choices=Category.choices,
         initial=Category.NO,
         help_text="This is a category!",
+        widget=forms.Select(attrs={"hidden": True}),
     )
     email = forms.EmailField(label="Email", help_text="Testable form")
     message = forms.CharField(label="Message", widget=forms.Textarea(attrs={"rows": 3}))
```

### Comparing `django_fragments-0.1.5/django_fragments/templates/msg.html` & `django_fragments-0.1.6/django_fragments/templates/msg.html`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/templatetags/fragments.py` & `django_fragments-0.1.6/django_fragments/templatetags/fragments.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/templatetags/helpers.py` & `django_fragments-0.1.6/django_fragments/templatetags/helpers.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/templatetags/og.py` & `django_fragments-0.1.6/django_fragments/templatetags/og.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/templatetags/utils/filter_attrs.py` & `django_fragments-0.1.6/django_fragments/templatetags/utils/filter_attrs.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/templatetags/utils/wrap_svg.py` & `django_fragments-0.1.6/django_fragments/templatetags/utils/wrap_svg.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/tests.py` & `django_fragments-0.1.6/django_fragments/tests.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/utils.py` & `django_fragments-0.1.6/django_fragments/utils.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/django_fragments/views.py` & `django_fragments-0.1.6/django_fragments/views.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.5/pyproject.toml` & `django_fragments-0.1.6/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "django-fragments"
 description = "Custom template tags for common html idioms in Django."
-version = "0.1.5"
+version = "0.1.6"
 authors = ["Marcelino G. Veloso III <mars@veloso.one>"]
 readme = "README.md"
 homepage = "https://mv3.dev"
 repository = "https://github.com/justmars/django-fragments"
 documentation = "https://mv3.dev/django-fragments"
 classifiers = [
   "Programming Language :: Python :: 3.11",
@@ -15,15 +15,14 @@
 ]
 
 [tool.poetry.dependencies]
 python = "^3.11"
 django = "^4.2"
 beautifulsoup4 = "^4.12.2"
 markdown = "^3.3.7"
-django-widget-tweaks = "^1.4.12"
 
 [tool.poetry.group.dev.dependencies]
 rich = "^13.3"
 pytest = "^7.2"
 pytest-django = "^4.5.1"
 pytest-cov = "^2.12"
 pre-commit = "^2.21"
```

### Comparing `django_fragments-0.1.5/PKG-INFO` & `django_fragments-0.1.6/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,23 @@
 Metadata-Version: 2.1
 Name: django-fragments
-Version: 0.1.5
+Version: 0.1.6
 Summary: Custom template tags for common html idioms in Django.
 Home-page: https://mv3.dev
 Author: Marcelino G. Veloso III
 Author-email: mars@veloso.one
 Requires-Python: >=3.11,<4.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: Pytest
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Typing :: Typed
 Requires-Dist: beautifulsoup4 (>=4.12.2,<5.0.0)
 Requires-Dist: django (>=4.2,<5.0)
-Requires-Dist: django-widget-tweaks (>=1.4.12,<2.0.0)
 Requires-Dist: markdown (>=3.3.7,<4.0.0)
 Project-URL: Documentation, https://mv3.dev/django-fragments
 Project-URL: Repository, https://github.com/justmars/django-fragments
 Description-Content-Type: text/markdown
 
 # django-fragments
```

