# Comparing `tmp/django_fragments-0.1.4.tar.gz` & `tmp/django_fragments-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_fragments-0.1.4.tar", max compression
+gzip compressed data, was "django_fragments-0.1.5.tar", max compression
```

## Comparing `django_fragments-0.1.4.tar` & `django_fragments-0.1.5.tar`

### file list

```diff
@@ -1,28 +1,30 @@
--rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.4/LICENSE
--rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.4/README.md
--rw-r--r--   0        0        0       27 2023-05-10 21:50:52.993055 django_fragments-0.1.4/django_fragments/__init__.py
--rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.4/django_fragments/apps.py
--rw-r--r--   0        0        0      768 2023-05-11 09:07:30.714263 django_fragments-0.1.4/django_fragments/forms.py
--rw-r--r--   0        0        0     7290 2023-05-11 16:15:20.214703 django_fragments-0.1.4/django_fragments/static/chooseDown.js
--rw-r--r--   0        0        0      823 2023-05-11 12:28:18.550507 django_fragments-0.1.4/django_fragments/templates/_nav.html
--rw-r--r--   0        0        0      617 2023-05-11 07:27:50.457784 django_fragments-0.1.4/django_fragments/templates/_test.html
--rw-r--r--   0        0        0      157 2023-05-11 10:48:10.438973 django_fragments-0.1.4/django_fragments/templates/about.html
--rw-r--r--   0        0        0      487 2023-05-11 15:02:41.021713 django_fragments-0.1.4/django_fragments/templates/contact.html
--rw-r--r--   0        0        0     1354 2023-05-11 16:23:13.912005 django_fragments-0.1.4/django_fragments/templates/down-list.html
--rw-r--r--   0        0        0      159 2023-05-11 05:32:45.338924 django_fragments-0.1.4/django_fragments/templates/home.html
--rw-r--r--   0        0        0      310 2023-05-11 12:36:00.534956 django_fragments-0.1.4/django_fragments/templates/item.html
--rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.4/django_fragments/templates/svg/heroicons_x_mark_mini.html
--rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.4/django_fragments/templates/test_snippet.html
--rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.4/django_fragments/templatetags/__init__.py
--rw-r--r--   0        0        0     6118 2023-05-11 16:23:17.630674 django_fragments-0.1.4/django_fragments/templatetags/fragments.py
--rw-r--r--   0        0        0     3435 2023-05-11 07:56:55.689314 django_fragments-0.1.4/django_fragments/templatetags/helpers.py
--rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.4/django_fragments/templatetags/og.py
--rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.4/django_fragments/templatetags/utils/__init__.py
--rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.4/django_fragments/templatetags/utils/filter_attrs.py
--rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.4/django_fragments/templatetags/utils/wrap_svg.py
--rw-r--r--   0        0        0     7329 2023-05-11 12:42:51.123535 django_fragments-0.1.4/django_fragments/tests.py
--rw-r--r--   0        0        0      401 2023-05-11 10:47:46.916870 django_fragments-0.1.4/django_fragments/urls.py
--rw-r--r--   0        0        0      424 2023-05-11 03:15:18.733152 django_fragments-0.1.4/django_fragments/utils.py
--rw-r--r--   0        0        0      730 2023-05-11 10:47:25.364482 django_fragments-0.1.4/django_fragments/views.py
--rw-r--r--   0        0        0     1439 2023-05-12 03:16:41.449020 django_fragments-0.1.4/pyproject.toml
--rw-r--r--   0        0        0     1536 1970-01-01 00:00:00.000000 django_fragments-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.5/LICENSE
+-rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.5/README.md
+-rw-r--r--   0        0        0       36 2023-05-12 14:54:30.129104 django_fragments-0.1.5/django_fragments/__init__.py
+-rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.5/django_fragments/apps.py
+-rw-r--r--   0        0        0     1255 2023-05-12 14:54:30.129513 django_fragments-0.1.5/django_fragments/forms.py
+-rw-r--r--   0        0        0     7217 2023-05-12 14:54:30.130087 django_fragments-0.1.5/django_fragments/static/chooseDown.js
+-rw-r--r--   0        0        0      823 2023-05-12 14:54:30.130507 django_fragments-0.1.5/django_fragments/templates/_nav.html
+-rw-r--r--   0        0        0      743 2023-05-12 14:54:30.130818 django_fragments-0.1.5/django_fragments/templates/_test.html
+-rw-r--r--   0        0        0      192 2023-05-12 14:54:30.130994 django_fragments-0.1.5/django_fragments/templates/about.html
+-rw-r--r--   0        0        0      470 2023-05-12 14:54:30.131347 django_fragments-0.1.5/django_fragments/templates/contact.html
+-rw-r--r--   0        0        0     1839 2023-05-12 14:54:30.131597 django_fragments-0.1.5/django_fragments/templates/down-list.html
+-rw-r--r--   0        0        0      232 2023-05-12 14:54:30.131849 django_fragments-0.1.5/django_fragments/templates/home.html
+-rw-r--r--   0        0        0      310 2023-05-12 14:54:30.132221 django_fragments-0.1.5/django_fragments/templates/item.html
+-rw-r--r--   0        0        0      582 2023-05-12 14:54:30.132477 django_fragments-0.1.5/django_fragments/templates/msg.html
+-rw-r--r--   0        0        0      331 2023-05-12 14:54:30.133019 django_fragments-0.1.5/django_fragments/templates/msg_form.html
+-rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.5/django_fragments/templates/svg/heroicons_x_mark_mini.html
+-rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.5/django_fragments/templates/test_snippet.html
+-rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.5/django_fragments/templatetags/__init__.py
+-rw-r--r--   0        0        0     6118 2023-05-11 16:23:17.630674 django_fragments-0.1.5/django_fragments/templatetags/fragments.py
+-rw-r--r--   0        0        0     3435 2023-05-11 07:56:55.689314 django_fragments-0.1.5/django_fragments/templatetags/helpers.py
+-rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.5/django_fragments/templatetags/og.py
+-rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.5/django_fragments/templatetags/utils/__init__.py
+-rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.5/django_fragments/templatetags/utils/filter_attrs.py
+-rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.5/django_fragments/templatetags/utils/wrap_svg.py
+-rw-r--r--   0        0        0     3279 2023-05-12 14:54:30.133346 django_fragments-0.1.5/django_fragments/tests.py
+-rw-r--r--   0        0        0      472 2023-05-12 14:54:30.133617 django_fragments-0.1.5/django_fragments/urls.py
+-rw-r--r--   0        0        0      579 2023-05-12 14:54:30.133874 django_fragments-0.1.5/django_fragments/utils.py
+-rw-r--r--   0        0        0     1910 2023-05-12 14:54:30.134176 django_fragments-0.1.5/django_fragments/views.py
+-rw-r--r--   0        0        0     1471 2023-05-12 15:08:33.821273 django_fragments-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     1536 1970-01-01 00:00:00.000000 django_fragments-0.1.5/PKG-INFO
```

### Comparing `django_fragments-0.1.4/LICENSE` & `django_fragments-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/README.md` & `django_fragments-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/static/chooseDown.js` & `django_fragments-0.1.5/django_fragments/static/chooseDown.js`

 * *Files 4% similar despite different names*

#### js-beautify {}

```diff
@@ -8,15 +8,15 @@
     }
 
     function setManyIds(els, id, prefix) {
         if (!els) {
             return false;
         }
         for (let i = 0; i < els.length; i++) {
-            setId(els[i], id, `${prefix}-${i + 1}`);
+            setId(els[i], id, `${prefix}-${i}`);
         }
         return els;
     }
 
     let container = document.getElementById(id) || false;
     if (!container) {
         throw "Missing container.";
@@ -49,15 +49,15 @@
  * When a valid event occurs that converts this candidate choice to the actual selected choice,
  * the node is dispatched with the a `userHasChosen` event, and nodes are re-hidden.
  *
  * @param {*} selectable_group_id
  */
 function chooseDown(selectable_group_id) {
     const [button, nodeList, nodeItems] = verifySelectable(selectable_group_id);
-    const arrowKeys = ["ArrowDown", "ArrowUp", "ArrowRight", "ArrowLeft"];
+    const arrowKeys = ["ArrowDown", "ArrowUp"];
     const eventToEmit = new Event("userHasChosen", {
         bubbles: false,
         cancelable: false,
     });
 
     // add event listener to each focusable item
     const nodeOptions = Array.prototype.slice.call(nodeItems); // to use forEach
@@ -104,88 +104,86 @@
         nodeList.setAttribute("aria-activedescendant", node.id); // assign active
         if (evt && evt.type === "keydown" && arrowKeys.includes(evt.key))
             node.scrollIntoView({
                 block: "start",
                 inline: "nearest",
             }); // keydown into middle of long item list
 
-        console.log(`focused ${node.id}`);
+        // console.log(`focused ${node.id}`);
     }
 
     // Ready button events which shows / hides / focuses nodes
     button.addEventListener(
         "blur",
         (evt) => {
             if (evt.relatedTarget) {
-                console.log(`blurred: ${evt.relatedTarget.id}`);
+                // console.log(`blurred: ${evt.relatedTarget.id}`);
                 if (evt.relatedTarget === nodeList) {
-                    let node = nodeItems[parseInt(button.dataset.index) - 1];
-                    console.log(`matched ${node.id}`);
+                    let node = nodeItems[parseInt(button.dataset.index)];
+                    // console.log(`matched ${node.id}`);
                     node.dispatchEvent(eventToEmit);
                 } else {
                     nodeOptions.forEach((node) => {
                         if (evt.relatedTarget.id === node.id) {
-                            console.log(`matched ${node.id}`);
+                            // console.log(`matched ${node.id}`);
                             node.dispatchEvent(eventToEmit);
                         }
                     });
                 }
             }
-            console.log(`targeted: ${evt.target.id}`);
+            // console.log(`targeted: ${evt.target.id}`);
             if (evt.target.id === button.id) {
                 /// debugger;
-                let node = nodeItems[parseInt(button.dataset.index) - 1];
-                console.log(`matched ${node.id}`);
+                let node = nodeItems[parseInt(button.dataset.index)];
+                // console.log(`matched ${node.id}`);
                 node.dispatchEvent(eventToEmit);
             }
             hideBox(evt);
         },
         false
     );
     button.addEventListener(
         "click",
         (evt) => {
-            console.log(`click on: ${evt} ${evt.relatedTarget}`);
+            // console.log(`click on: ${evt} ${evt.relatedTarget}`);
             toggleBox(evt);
         },
         false
     );
     button.addEventListener("touchstart", (evt) => {
         evt.preventDefault(); // without this, will auto-mouse click
         toggleBox(evt);
     });
     button.addEventListener("keydown", (evt) => {
-        if (!button.dataset.index) button.dataset.index = 1; // if index not set
+        if (!button.dataset.index) button.dataset.index = 0; // if index not set
         if (button.getAttribute("aria-expanded") === "true") {
             switch (evt.key) {
                 case "Tab":
                 case "Escape":
                     hideBox(evt);
                     break;
 
                 case "ArrowDown":
-                case "ArrowRight":
                     let currDownIndex = parseInt(button.dataset.index);
-                    currDownIndex === nodeItems.length ?
-                        (button.dataset.index = 1) :
+                    currDownIndex === nodeItems.length - 1 ?
+                        (button.dataset.index = 0) :
                         (button.dataset.index = currDownIndex + 1);
-                    markFocus(nodeItems[parseInt(button.dataset.index) - 1], evt);
+                    markFocus(nodeItems[parseInt(button.dataset.index)], evt);
                     break;
 
                 case "ArrowUp":
-                case "ArrowLeft":
                     let currUpIndex = parseInt(button.dataset.index);
-                    currUpIndex === 1 ?
-                        (button.dataset.index = nodeItems.length) :
+                    currUpIndex === 0 ?
+                        (button.dataset.index = nodeItems.length - 1) :
                         (button.dataset.index = currUpIndex - 1);
-                    markFocus(nodeItems[parseInt(button.dataset.index) - 1], evt);
+                    markFocus(nodeItems[parseInt(button.dataset.index)], evt);
                     break;
 
                 case "Enter":
-                    const currNode = nodeItems[parseInt(button.dataset.index) - 1];
+                    const currNode = nodeItems[parseInt(button.dataset.index)];
                     currNode.dispatchEvent(eventToEmit);
                     break;
             }
         }
     });
 
     function toggleBox(evt) {
@@ -195,22 +193,22 @@
             hideBox(evt);
     }
 
     function showBox(evt) {
         nodeList.removeAttribute("hidden");
         button.setAttribute("aria-expanded", "true");
         button.setAttribute("aria-hidden", "false");
-        console.log(`show ${nodeList.id} ${evt.type}`);
-        if (!button.dataset.index) button.dataset.index = 1; // if index not set
-        const focusable = nodeItems[parseInt(button.dataset.index) - 1];
+        // console.log(`show ${nodeList.id} ${evt.type}`);
+        if (!button.dataset.index) button.dataset.index = 0; // if index not set
+        const focusable = nodeItems[parseInt(button.dataset.index)];
         if (focusable && focusable.contains(evt.target)) markFocus(focusable);
     }
 
     function hideBox(evt) {
         if (button.getAttribute("aria-expanded") === "true") {
             nodeList.setAttribute("hidden", "true");
             button.setAttribute("aria-expanded", "false");
             button.setAttribute("aria-hidden", "true");
         }
-        console.log(`hide ${nodeList.id} ${evt.target} ${evt.type}`);
+        // console.log(`hide ${nodeList.id} ${evt.target} ${evt.type}`);
     }
 }
```

### Comparing `django_fragments-0.1.4/django_fragments/templates/_nav.html` & `django_fragments-0.1.5/django_fragments/templates/_nav.html`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/templatetags/fragments.py` & `django_fragments-0.1.5/django_fragments/templatetags/fragments.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/templatetags/helpers.py` & `django_fragments-0.1.5/django_fragments/templatetags/helpers.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/templatetags/og.py` & `django_fragments-0.1.5/django_fragments/templatetags/og.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/templatetags/utils/filter_attrs.py` & `django_fragments-0.1.5/django_fragments/templatetags/utils/filter_attrs.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/django_fragments/templatetags/utils/wrap_svg.py` & `django_fragments-0.1.5/django_fragments/templatetags/utils/wrap_svg.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.4/pyproject.toml` & `django_fragments-0.1.5/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "django-fragments"
 description = "Custom template tags for common html idioms in Django."
-version = "0.1.4"
+version = "0.1.5"
 authors = ["Marcelino G. Veloso III <mars@veloso.one>"]
 readme = "README.md"
 homepage = "https://mv3.dev"
 repository = "https://github.com/justmars/django-fragments"
 documentation = "https://mv3.dev/django-fragments"
 classifiers = [
   "Programming Language :: Python :: 3.11",
@@ -27,14 +27,15 @@
 pytest-django = "^4.5.1"
 pytest-cov = "^2.12"
 pre-commit = "^2.21"
 mkdocs = "^1.4"
 mkdocstrings = { extras = ["python"], version = "^0.20.0" }
 mkdocs-material = "^9.1"
 ipykernel = "^6.22.0"
+django-debug-toolbar = "^4.0.0"
 
 [tool.pytest.ini_options]
 minversion = "7.3"
 addopts = "-ra -q -vv --ds=config.settings --doctest-modules --cov"
 filterwarnings = [
   "ignore::DeprecationWarning", # DeprecationWarning: pkg_resources is deprecated as an API
 ]
```

### Comparing `django_fragments-0.1.4/PKG-INFO` & `django_fragments-0.1.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-fragments
-Version: 0.1.4
+Version: 0.1.5
 Summary: Custom template tags for common html idioms in Django.
 Home-page: https://mv3.dev
 Author: Marcelino G. Veloso III
 Author-email: mars@veloso.one
 Requires-Python: >=3.11,<4.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: Pytest
```

