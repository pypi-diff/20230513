# Comparing `tmp/django_fragments-0.1.7.tar.gz` & `tmp/django_fragments-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_fragments-0.1.7.tar", max compression
+gzip compressed data, was "django_fragments-0.1.8.tar", max compression
```

## Comparing `django_fragments-0.1.7.tar` & `django_fragments-0.1.8.tar`

### file list

```diff
@@ -1,34 +1,34 @@
--rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.7/LICENSE
--rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.7/README.md
--rw-r--r--   0        0        0       36 2023-05-12 14:54:30.129104 django_fragments-0.1.7/django_fragments/__init__.py
--rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.7/django_fragments/apps.py
--rw-r--r--   0        0        0     1705 2023-05-13 08:03:42.389176 django_fragments-0.1.7/django_fragments/forms.py
--rw-r--r--   0        0        0     6126 2023-05-13 08:03:42.389593 django_fragments-0.1.7/django_fragments/static/doDropCommon.js
--rw-r--r--   0        0        0     1008 2023-05-13 08:03:42.389898 django_fragments-0.1.7/django_fragments/static/doDropMenu.js
--rw-r--r--   0        0        0     1543 2023-05-13 08:03:42.390306 django_fragments-0.1.7/django_fragments/static/doDropSelect.js
--rw-r--r--   0        0        0      758 2023-05-13 08:03:42.390796 django_fragments-0.1.7/django_fragments/static/doTheme.js
--rw-r--r--   0        0        0      727 2023-05-13 10:29:52.302478 django_fragments-0.1.7/django_fragments/templates/_nav.html
--rw-r--r--   0        0        0      200 2023-05-13 08:03:42.391887 django_fragments-0.1.7/django_fragments/templates/about.html
--rw-r--r--   0        0        0      980 2023-05-13 08:24:45.209331 django_fragments-0.1.7/django_fragments/templates/base_template.html
--rw-r--r--   0        0        0      478 2023-05-13 08:03:42.392713 django_fragments-0.1.7/django_fragments/templates/contact.html
--rw-r--r--   0        0        0      404 2023-05-13 08:03:42.393026 django_fragments-0.1.7/django_fragments/templates/down-list.html
--rw-r--r--   0        0        0      240 2023-05-13 08:03:42.393455 django_fragments-0.1.7/django_fragments/templates/home.html
--rw-r--r--   0        0        0      582 2023-05-12 14:54:30.132477 django_fragments-0.1.7/django_fragments/templates/msg.html
--rw-r--r--   0        0        0      405 2023-05-12 16:28:19.371173 django_fragments-0.1.7/django_fragments/templates/msg_form.html
--rw-r--r--   0        0        0      376 2023-05-13 08:51:34.198976 django_fragments-0.1.7/django_fragments/templates/svg/heroicons_moon.html
--rw-r--r--   0        0        0      393 2023-05-13 08:51:18.444332 django_fragments-0.1.7/django_fragments/templates/svg/heroicons_sun.html
--rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.7/django_fragments/templates/svg/heroicons_x_mark_mini.html
--rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.7/django_fragments/templates/test_snippet.html
--rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.7/django_fragments/templatetags/__init__.py
--rw-r--r--   0        0        0    10847 2023-05-13 10:39:38.859494 django_fragments-0.1.7/django_fragments/templatetags/fragments.py
--rw-r--r--   0        0        0     3821 2023-05-13 08:24:33.561434 django_fragments-0.1.7/django_fragments/templatetags/helpers.py
--rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.7/django_fragments/templatetags/og.py
--rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.7/django_fragments/templatetags/utils/__init__.py
--rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.7/django_fragments/templatetags/utils/filter_attrs.py
--rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.7/django_fragments/templatetags/utils/wrap_svg.py
--rw-r--r--   0        0        0     3279 2023-05-12 14:54:30.133346 django_fragments-0.1.7/django_fragments/tests.py
--rw-r--r--   0        0        0      472 2023-05-12 14:54:30.133617 django_fragments-0.1.7/django_fragments/urls.py
--rw-r--r--   0        0        0      883 2023-05-13 08:36:20.754601 django_fragments-0.1.7/django_fragments/utils.py
--rw-r--r--   0        0        0     1910 2023-05-12 14:54:30.134176 django_fragments-0.1.7/django_fragments/views.py
--rw-r--r--   0        0        0     1494 2023-05-13 09:02:11.200373 django_fragments-0.1.7/pyproject.toml
--rw-r--r--   0        0        0     1482 1970-01-01 00:00:00.000000 django_fragments-0.1.7/PKG-INFO
+-rw-r--r--   0        0        0     1491 2023-05-09 09:45:58.288456 django_fragments-0.1.8/LICENSE
+-rw-r--r--   0        0        0      690 2023-05-11 04:39:18.008492 django_fragments-0.1.8/README.md
+-rw-r--r--   0        0        0       36 2023-05-12 14:54:30.129104 django_fragments-0.1.8/django_fragments/__init__.py
+-rw-r--r--   0        0        0      163 2023-05-08 11:11:49.135944 django_fragments-0.1.8/django_fragments/apps.py
+-rw-r--r--   0        0        0     1705 2023-05-13 08:03:42.389176 django_fragments-0.1.8/django_fragments/forms.py
+-rw-r--r--   0        0        0     6714 2023-05-13 12:07:41.006691 django_fragments-0.1.8/django_fragments/static/doDropCommon.js
+-rw-r--r--   0        0        0     1012 2023-05-13 12:08:17.116673 django_fragments-0.1.8/django_fragments/static/doDropMenu.js
+-rw-r--r--   0        0        0     1553 2023-05-13 12:07:06.529481 django_fragments-0.1.8/django_fragments/static/doDropSelect.js
+-rw-r--r--   0        0        0     1009 2023-05-13 11:44:41.739827 django_fragments-0.1.8/django_fragments/static/doTheme.js
+-rw-r--r--   0        0        0      727 2023-05-13 10:29:52.302478 django_fragments-0.1.8/django_fragments/templates/_nav.html
+-rw-r--r--   0        0        0      200 2023-05-13 08:03:42.391887 django_fragments-0.1.8/django_fragments/templates/about.html
+-rw-r--r--   0        0        0     1192 2023-05-13 12:02:59.632816 django_fragments-0.1.8/django_fragments/templates/base_template.html
+-rw-r--r--   0        0        0      478 2023-05-13 08:03:42.392713 django_fragments-0.1.8/django_fragments/templates/contact.html
+-rw-r--r--   0        0        0      404 2023-05-13 08:03:42.393026 django_fragments-0.1.8/django_fragments/templates/down-list.html
+-rw-r--r--   0        0        0      240 2023-05-13 08:03:42.393455 django_fragments-0.1.8/django_fragments/templates/home.html
+-rw-r--r--   0        0        0      582 2023-05-12 14:54:30.132477 django_fragments-0.1.8/django_fragments/templates/msg.html
+-rw-r--r--   0        0        0      405 2023-05-12 16:28:19.371173 django_fragments-0.1.8/django_fragments/templates/msg_form.html
+-rw-r--r--   0        0        0      376 2023-05-13 08:51:34.198976 django_fragments-0.1.8/django_fragments/templates/svg/heroicons_moon.html
+-rw-r--r--   0        0        0      393 2023-05-13 08:51:18.444332 django_fragments-0.1.8/django_fragments/templates/svg/heroicons_sun.html
+-rw-r--r--   0        0        0      292 2023-05-07 15:19:00.977243 django_fragments-0.1.8/django_fragments/templates/svg/heroicons_x_mark_mini.html
+-rw-r--r--   0        0        0      131 2023-05-11 03:15:53.053123 django_fragments-0.1.8/django_fragments/templates/test_snippet.html
+-rw-r--r--   0        0        0        0 2023-05-07 23:31:34.843055 django_fragments-0.1.8/django_fragments/templatetags/__init__.py
+-rw-r--r--   0        0        0    10865 2023-05-13 13:22:52.479548 django_fragments-0.1.8/django_fragments/templatetags/fragments.py
+-rw-r--r--   0        0        0     3822 2023-05-13 12:20:59.741080 django_fragments-0.1.8/django_fragments/templatetags/helpers.py
+-rw-r--r--   0        0        0     1649 2023-05-09 09:40:55.305731 django_fragments-0.1.8/django_fragments/templatetags/og.py
+-rw-r--r--   0        0        0       70 2023-05-08 02:09:45.909742 django_fragments-0.1.8/django_fragments/templatetags/utils/__init__.py
+-rw-r--r--   0        0        0     2157 2023-05-08 02:17:55.382358 django_fragments-0.1.8/django_fragments/templatetags/utils/filter_attrs.py
+-rw-r--r--   0        0        0     4146 2023-05-08 08:19:35.581999 django_fragments-0.1.8/django_fragments/templatetags/utils/wrap_svg.py
+-rw-r--r--   0        0        0     3279 2023-05-12 14:54:30.133346 django_fragments-0.1.8/django_fragments/tests.py
+-rw-r--r--   0        0        0      472 2023-05-12 14:54:30.133617 django_fragments-0.1.8/django_fragments/urls.py
+-rw-r--r--   0        0        0      883 2023-05-13 08:36:20.754601 django_fragments-0.1.8/django_fragments/utils.py
+-rw-r--r--   0        0        0     1910 2023-05-12 14:54:30.134176 django_fragments-0.1.8/django_fragments/views.py
+-rw-r--r--   0        0        0     1494 2023-05-13 13:29:27.920862 django_fragments-0.1.8/pyproject.toml
+-rw-r--r--   0        0        0     1482 1970-01-01 00:00:00.000000 django_fragments-0.1.8/PKG-INFO
```

### Comparing `django_fragments-0.1.7/LICENSE` & `django_fragments-0.1.8/LICENSE`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/README.md` & `django_fragments-0.1.8/README.md`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/forms.py` & `django_fragments-0.1.8/django_fragments/forms.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/static/doDropCommon.js` & `django_fragments-0.1.8/django_fragments/static/doDropCommon.js`

 * *Files 12% similar despite different names*

#### js-beautify {}

```diff
@@ -1,26 +1,45 @@
-function setIndex(el, id, suffix) {
+/**
+ * Combines base `id` with a `suffix` and store it as the id attribute of the element `el`
+ * @param {*} el
+ * @param {*} id
+ * @param {*} suffix
+ * @returns a DOM node
+ */
+function addSuffixId(el, id, suffix) {
     if (!el) {
         return false;
     }
     el.setAttribute("id", `${id}-${suffix}`);
     return el;
 }
 
+/**
+ * Combines base `id` with a `prefix` and store it as the id attribute of all elements `els`
+ * @param {*} els
+ * @param {*} id
+ * @param {*} prefix
+ * @returns
+ */
 function setManyIds(els, id, prefix) {
     if (!els) {
         return false;
     }
     for (let i = 0; i < els.length; i++) {
-        setIndex(els[i], id, `${prefix}-${i}`);
+        addSuffixId(els[i], id, `${prefix}-${i}`);
     }
     return els;
 }
 
-function isDownable(items) {
+/**
+ * Return the DOM node `items` if all are present, otherwise throw an error.
+ * @param {*} items
+ * @returns Array of DOM nodes.
+ */
+function isExists(items) {
     for (let item of items) {
         if (!item) {
             throw "Missing element.";
         }
     }
     return items;
 }
@@ -36,20 +55,20 @@
         this.nodeItems = nodeItems;
         this.nodeList = nodeList;
         this.nodeList.setAttribute("aria-orientation", "vertical");
         this.nodeList.setAttribute("tab-index", "-1");
 
         this.focusFunc = focusFunc;
         this.chooseFunc = chooseFunc;
-        this.nodeOptions = this.prepareOptions(nodeItems);
+        this.nodeOptions = this.prepItems(nodeItems);
 
-        this.prepareButtonKeydowns();
-        this.prepareButtonBlur();
-        this.prepareButtonClick();
-        this.prepareButtonTouch();
+        this.prepButtonKeydowns();
+        this.prepButtonBlur();
+        this.prepButtonClick();
+        this.prepButtonTouch();
     }
 
     getButtonIndex() {
         let val = parseInt(this.button.dataset.index);
         // console.log(`Index of node: ${val}`);
         return val;
     }
@@ -77,31 +96,34 @@
             this.nodeList.setAttribute("hidden", "true");
             this.button.setAttribute("aria-expanded", "false");
             this.button.setAttribute("aria-hidden", "true");
         }
         // console.log(`hide ${this.nodeList.id} ${evt.target} ${evt.type}`);
     }
 
+    // determine whether button is expanded and then toggle
     toggleBox(evt) {
         evt.preventDefault();
         this.button.getAttribute("aria-expanded") !== "true" ?
             this.showBox(evt) :
             this.hideBox(evt);
     }
 
+    // get integer from node id attribute
     nodeDigit(node) {
         return node.id.match(/\d+$/);
     }
 
+    // set node id attribute
     setButtonIndex(val) {
         this.button.dataset.index = val;
     }
 
     // make list options focusable via events
-    prepareOptions(nodeItems) {
+    prepItems(nodeItems) {
         let nodes = Array.prototype.slice.call(nodeItems);
         nodes.forEach((node) => {
             node.setAttribute("role", "option");
             node.setAttribute("aria-selected", "false");
             node.setAttribute("tab-index", "-1");
 
             node.addEventListener("mouseover", () => {
@@ -127,21 +149,22 @@
                     passive: false
                 }
             );
         });
         return nodes;
     }
 
-    prepareButtonKeydowns() {
+    //
+    prepButtonKeydowns() {
         this.button.addEventListener("keydown", (evt) => {
             if (this.button.getAttribute("aria-expanded") === "true") {
                 switch (evt.key) {
                     case "Tab":
                     case "Escape":
-                        hideBox(evt);
+                        this.hideBox(evt);
                         break;
 
                     case "ArrowDown":
                         let currDownIndex = this.getButtonIndex();
                         currDownIndex === this.nodeItems.length - 1 ?
                             this.setButtonIndex(0) :
                             this.setButtonIndex(currDownIndex + 1);
@@ -173,15 +196,15 @@
                         break;
                 }
             }
         });
     }
 
     // Ready button events which shows / hides / focuses nodes
-    prepareButtonBlur() {
+    prepButtonBlur() {
         this.button.addEventListener(
             "blur",
             (evt) => {
                 if (evt.relatedTarget) {
                     // console.log(`blurred: ${evt.relatedTarget.id}`);
                     if (evt.relatedTarget === this.nodeList) {
                         this.chooseFunc();
@@ -196,26 +219,26 @@
                     }
                 }
             },
             false
         );
     }
 
-    prepareButtonClick() {
+    prepButtonClick() {
         this.button.addEventListener(
             "click",
             (evt) => {
                 // console.log(`click on: ${evt} ${evt.relatedTarget}`);
                 this.toggleBox(evt);
             },
             false
         );
     }
 
-    prepareButtonTouch() {
+    prepButtonTouch() {
         this.button.addEventListener(
             "touchstart",
             (evt) => {
                 evt.preventDefault(); // without this, will auto-mouse click
                 this.toggleBox(evt);
             }, {
                 passive: false
```

### Comparing `django_fragments-0.1.7/django_fragments/static/doDropMenu.js` & `django_fragments-0.1.8/django_fragments/static/doDropMenu.js`

 * *Files 16% similar despite different names*

#### js-beautify {}

```diff
@@ -1,12 +1,12 @@
 function doMenu(id) {
-    const [container, button, nodeList, nodeItems] = isDownable([
+    const [container, button, nodeList, nodeItems] = isExists([
         document.getElementById(id),
-        setIndex(document.querySelector(`#${id} button`), id, "btn"),
-        setIndex(document.querySelector(`#${id} ul[role=menu]`), id, "listbox"),
+        addSuffixId(document.querySelector(`#${id} button`), id, "btn"),
+        addSuffixId(document.querySelector(`#${id} ul[role=menu]`), id, "listbox"),
         setManyIds(
             document.querySelectorAll(`#${id} ul[hidden][role=menu] > li`),
             id,
             "option"
         ),
         document.querySelectorAll(`#${id} ul[hidden][role=menu] > li a`),
     ]);
```

### Comparing `django_fragments-0.1.7/django_fragments/static/doDropSelect.js` & `django_fragments-0.1.8/django_fragments/static/doDropSelect.js`

 * *Files 10% similar despite different names*

#### js-beautify {}

```diff
@@ -3,21 +3,21 @@
         container,
         hiddenSelect,
         label,
         button,
         buttonSpan,
         nodeList,
         nodeItems,
-    ] = isDownable([
+    ] = isExists([
         document.getElementById(id),
         document.querySelector(`#${id} > select[hidden]`),
-        setIndex(document.querySelector(`#${id} label`), id, "label"),
-        setIndex(document.querySelector(`#${id} button`), id, "btn"),
-        setIndex(document.querySelector(`#${id} button > span`), id, "txt"),
-        setIndex(
+        addSuffixId(document.querySelector(`#${id} label`), id, "label"),
+        addSuffixId(document.querySelector(`#${id} button`), id, "btn"),
+        addSuffixId(document.querySelector(`#${id} button > span`), id, "txt"),
+        addSuffixId(
             document.querySelector(`#${id} ul[hidden][role=listbox]`),
             id,
             "listbox"
         ),
         setManyIds(
             document.querySelectorAll(`#${id} ul[hidden][role=listbox] > li`),
             id,
```

### Comparing `django_fragments-0.1.7/django_fragments/static/doTheme.js` & `django_fragments-0.1.8/django_fragments/static/doTheme.js`

 * *Files 18% similar despite different names*

#### js-beautify {}

```diff
@@ -1,27 +1,35 @@
-const htmlKls = document.documentElement.classList;
+/** Refers to `<html class="">` */
+const baseKlass = document.documentElement.classList;
 
+function setTheme(val) {
+    baseKlass.add(val);
+    localStorage.setItem("theme", val);
+}
+
+/** Check if localStorage populated then adjust <html> accordingly; if not available,
+ *  determine user preference, finally default to light mode.
+ */
 function themeHTML() {
     if (localStorage.getItem("theme") === "dark") {
-        htmlKls.add("dark");
+        baseKlass.add("dark");
     } else if (localStorage.getItem("theme") === "light") {
-        htmlKls.add("light");
+        baseKlass.add("light");
     } else if (window.matchMedia("(prefers-color-scheme: dark)")) {
-        htmlKls.add("dark");
-        localStorage.setItem("theme", "dark");
+        setTheme("dark");
     } else {
-        htmlKls.add("light");
-        localStorage.setItem("theme", "light");
+        setTheme("light");
     }
 }
 
+/** Based on `baseKlass`, toggle its opposite, e.g. if 'light', make 'dark' then
+ * storage the result in LocalStorage under `theme` variable.
+ */
 function toggleTheme() {
-    if (htmlKls.contains("dark")) {
-        htmlKls.remove("dark");
-        htmlKls.add("light");
-        localStorage.setItem("theme", "light");
-    } else if (htmlKls.contains("light")) {
-        htmlKls.remove("light");
-        htmlKls.add("dark");
-        localStorage.setItem("theme", "dark");
+    if (baseKlass.contains("dark")) {
+        baseKlass.remove("dark");
+        setTheme("light");
+    } else if (baseKlass.contains("light")) {
+        baseKlass.remove("light");
+        setTheme("dark");
     }
 }
```

### Comparing `django_fragments-0.1.7/django_fragments/templates/_nav.html` & `django_fragments-0.1.8/django_fragments/templates/_nav.html`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/templates/base_template.html` & `django_fragments-0.1.8/django_fragments/templates/base_template.html`

 * *Files 12% similar despite different names*

```diff
@@ -1,21 +1,30 @@
 {% load static fragments %}
 <!DOCTYPE html>
 <script src="{% static 'doTheme.js' %}"></script>
 <script src="{% static 'doDropCommon.js' %}"></script>
 <script src="{% static 'doDropSelect.js' %}"></script>
 <script src="{% static 'doDropMenu.js' %}"></script>
 <script>themeHTML()</script>
+
 <html lang="en">
   <head>
     <meta charset="utf-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <meta name="robots" content="noindex">
     <link rel="stylesheet" href="https://unpkg.com/missing.css@1.0.9/dist/missing.min.css">
-    <title>django-fragments sample</title>
+    {% og_title 'django fragments sample' %}
+    {% og_desc 'demo of django-fragments' %}
+    {% og_img url="https://gravatar.com/mgv3" alt="Sample desc of image" %}
+    <style>
+      svg {
+        width: 12px;
+        height: 12px;
+      }
+    </style>
   </head>
   <body {% htmx_csrf %} class="container">
     {% include './_nav.html' %}
     <main>
       {% block content %}
       {% endblock content %}
     </main>
```

#### html2text {}

```diff
@@ -1,7 +1,9 @@
 {% load static fragments %}
 
 
 
+ {% og_title 'django fragments sample' %} {% og_desc 'demo of django-fragments'
+%} {% og_img url="https://gravatar.com/mgv3" alt="Sample desc of image" %}
 % htmx_csrf %} class="container"> {% include './_nav.html' %}  {% block content
 %} {% endblock content %}  {% block footer %} {% include './msg.html' %} {%
 endblock footer %}
```

### Comparing `django_fragments-0.1.7/django_fragments/templates/msg.html` & `django_fragments-0.1.8/django_fragments/templates/msg.html`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/templatetags/fragments.py` & `django_fragments-0.1.8/django_fragments/templatetags/fragments.py`

 * *Files 2% similar despite different names*

```diff
@@ -83,37 +83,37 @@
         name (str): The prefixless (prefix_) name of the `html` file containing an `<svg>` icon, presumes to be formatted and included in the proper folder previously.
         css (str, optional): Previously defined CSS to add to the `<svg>` icon. Defaults to None.
         prefix (str, optional): Source of the svg file; needs to be declared in `settings.py`.
         folder (str, optional): Where to find the template; needs to be declared in `settings.py`.
         **kwargs (dict): The following kwargs: `pre_`, `post_`, and `parent_` args are respected by `start_html_tag_helpers`
 
     Returns:
-        SafeString: Small HTML fragment visually representing an svg icon but which may contain related tags.
+        SafeText: Small HTML fragment visually representing an svg icon but which may contain related tags.
     """  # noqa: E501
     path = folder / f"{prefix}_{name}.html"
     html = render_to_string(str(path))
     svg_with_kwargs = wrap_svg(html_markup=html, css=css, **kwargs)
     return mark_safe(str(svg_with_kwargs).strip())
 
 
 @register.simple_tag
 def toggle_icons(
     btn_kls: str | None = "theme-toggler",
     aria_label: str | None = "Toggle mode",
     **kwargs,
-):
+) -> SafeText:
     """Toggle icons. Returns an HTML fragment implementing two `{% icon %}`'s surrounded by a single button which,
     when clicked, implements the toggleTheme() functionality from `doTheme.js`
 
     Args:
         btn_kls (str | None, optional): _description_. Defaults to "theme-toggler".
         aria_label (str | None, optional): _description_. Defaults to "Toggle mode".
 
     Returns:
-        SafeString: HTML fragment button
+        SafeText: HTML fragment button
     """
     return mark_safe(
         Template("""
             {% load fragments %}
             {% whitespaceless %}
             <button onclick=toggleTheme() type="button" class="{{ btn_kls }}" aria-label="{{aria_label}}">
                 {{ icon1 }}
@@ -146,15 +146,15 @@
     icon1_pre_class: str | None = "sr-only",
     icon2_name: str | None = "moon",
     icon2_css: str | None = "moon_css",
     icon2_parent_class: str | None = "icon2_svg",
     icon2_pre_text: str | None = "Dark mode",
     icon2_pre_class: str | None = "sr-only",
     **kwargs,
-):
+) -> SafeText:
     """A wrapper over `toggle_icons()` but specific to a toggle for the common sun and moon
     pattern.
 
     Each icon uses the same signature as {% icon %}. To apply a value to the first icon,
     use the prefix `icon_1`. To apply a value to the second icon, use the prefix `icon_2`. If
     none are supplied, icon_1 will contain defaults for 'sun', icon_2 will contain defaults
     for 'moon'.
@@ -182,15 +182,15 @@
         icon2_name (str | None, optional): Will be used to create second {% icon %}. Defaults to "moon".
         icon2_css (str | None, optional): Will be used to create second {% icon %}. Defaults to "moon_css".
         icon2_parent_class (str | None, optional): Will be used to create second {% icon %}. Defaults to "icon2_svg".
         icon2_pre_text (str | None, optional): Will be used to create second {% icon %}. Defaults to "Dark mode".
         icon2_pre_class (str | None, optional): Will be used to create second {% icon %}. Defaults to "sr-only".
 
     Returns:
-        SafeString: HTML fragment button
+        SafeText: HTML fragment button
     """
     return toggle_icons(
         btn_kls=btn_kls,
         aria_label=aria_label,
         **(
             dict(
                 icon1_name=icon1_name,
```

### Comparing `django_fragments-0.1.7/django_fragments/templatetags/helpers.py` & `django_fragments-0.1.8/django_fragments/templatetags/helpers.py`

 * *Files 2% similar despite different names*

```diff
@@ -32,15 +32,15 @@
     [hernantz](https://hernantz.github.io/inline-form-validation-with-django-and-htmx.html).
     It makes use of various tags from [htmx](https://htmx.org).
 
     The gist: form is prematurely submitted (because of `hx-post`) as an AJAX-request,
     the partial template response will `hx-swap` an `hx-target`. In other words, the
     old field is replaced by the same field... but now as a result of `form.is_valid()`.
 
-    The response,if it contains errors, will include an error list for the field.
+    The response, if it contains errors, will include an error list for the field.
 
     Instead of rendering the entire partial response, the use of `hx-select` limits the
     replacement to a segment of the partial response.
 
     Args:
         bound (BoundField): A Django field with data previously submitted
         url (str): Where the form is submitted.
```

### Comparing `django_fragments-0.1.7/django_fragments/templatetags/og.py` & `django_fragments-0.1.8/django_fragments/templatetags/og.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/templatetags/utils/filter_attrs.py` & `django_fragments-0.1.8/django_fragments/templatetags/utils/filter_attrs.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/templatetags/utils/wrap_svg.py` & `django_fragments-0.1.8/django_fragments/templatetags/utils/wrap_svg.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/tests.py` & `django_fragments-0.1.8/django_fragments/tests.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/utils.py` & `django_fragments-0.1.8/django_fragments/utils.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/django_fragments/views.py` & `django_fragments-0.1.8/django_fragments/views.py`

 * *Files identical despite different names*

### Comparing `django_fragments-0.1.7/pyproject.toml` & `django_fragments-0.1.8/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "django-fragments"
 description = "Custom template tags for common html idioms in Django."
-version = "0.1.7"
+version = "0.1.8"
 authors = ["Marcelino G. Veloso III <mars@veloso.one>"]
 readme = "README.md"
 homepage = "https://mv3.dev"
 repository = "https://github.com/justmars/django-fragments"
 documentation = "https://mv3.dev/django-fragments"
 classifiers = [
   "Programming Language :: Python :: 3.11",
```

### Comparing `django_fragments-0.1.7/PKG-INFO` & `django_fragments-0.1.8/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-fragments
-Version: 0.1.7
+Version: 0.1.8
 Summary: Custom template tags for common html idioms in Django.
 Home-page: https://mv3.dev
 Author: Marcelino G. Veloso III
 Author-email: mars@veloso.one
 Requires-Python: >=3.11,<4.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: Pytest
```

