# Comparing `tmp/stackdiac-0.0.1.dev23.tar.gz` & `tmp/stackdiac-0.0.1.dev24.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stackdiac-0.0.1.dev23.tar", max compression
+gzip compressed data, was "stackdiac-0.0.1.dev24.tar", max compression
```

## Comparing `stackdiac-0.0.1.dev23.tar` & `stackdiac-0.0.1.dev24.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0     1066 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/LICENSE
--rw-r--r--   0        0        0     1415 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/README.md
--rw-r--r--   0        0        0      576 2023-05-13 00:07:28.649487 stackdiac-0.0.1.dev23/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/__init__.py
--rw-r--r--   0        0        0       23 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/api/__init__.py
--rw-r--r--   0        0        0     1179 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/api/server.py
--rw-r--r--   0        0        0     1800 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/cli/__init__.py
--rw-r--r--   0        0        0      729 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/cli/build.py
--rw-r--r--   0        0        0     1594 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/cli/create.py
--rw-r--r--   0        0        0      464 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/cli/ui.py
--rw-r--r--   0        0        0      381 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/models/__init__.py
--rw-r--r--   0        0        0     1145 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/models/backend.py
--rw-r--r--   0        0        0     2582 2023-05-13 00:07:10.617254 stackdiac-0.0.1.dev23/stackdiac/models/binary.py
--rw-r--r--   0        0        0     3975 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/cluster.py
--rw-r--r--   0        0        0     2769 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/config.py
--rw-r--r--   0        0        0     1499 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/operation.py
--rw-r--r--   0        0        0      161 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/provider.py
--rw-r--r--   0        0        0     5172 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/repo.py
--rw-r--r--   0        0        0     1716 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/spec.py
--rw-r--r--   0        0        0     9330 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/models/stack.py
--rw-r--r--   0        0        0      108 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/stackd/__init__.py
--rw-r--r--   0        0        0      193 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/stackd/filters.py
--rw-r--r--   0        0        0      297 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/stackd/sdmod.py
--rw-r--r--   0        0        0    10541 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/stackd/stackd.py
--rw-r--r--   0        0        0   164360 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/ui/4753c5ba57962b4d7bf8.woff
--rw-r--r--   0        0        0   121340 2023-05-13 00:07:10.621254 stackdiac-0.0.1.dev23/stackdiac/ui/6d63d0501e5ed7b79dab.woff2
--rw-r--r--   0        0        0  1312628 2023-05-13 00:07:10.629254 stackdiac-0.0.1.dev23/stackdiac/ui/bundle.js
--rw-r--r--   0        0        0     2766 2023-05-13 00:07:10.629254 stackdiac-0.0.1.dev23/stackdiac/ui/bundle.js.LICENSE.txt
--rw-r--r--   0        0        0      415 2023-05-13 00:07:10.629254 stackdiac-0.0.1.dev23/stackdiac/ui/index.html
--rw-r--r--   0        0        0     2290 1970-01-01 00:00:00.000000 stackdiac-0.0.1.dev23/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/LICENSE
+-rw-r--r--   0        0        0     1415 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/README.md
+-rw-r--r--   0        0        0      576 2023-05-13 00:42:06.288285 stackdiac-0.0.1.dev24/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/__init__.py
+-rw-r--r--   0        0        0       23 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/api/__init__.py
+-rw-r--r--   0        0        0     1179 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/api/server.py
+-rw-r--r--   0        0        0     1800 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/cli/__init__.py
+-rw-r--r--   0        0        0      729 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/cli/build.py
+-rw-r--r--   0        0        0     1594 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/cli/create.py
+-rw-r--r--   0        0        0      464 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/cli/ui.py
+-rw-r--r--   0        0        0      381 2023-05-13 00:41:47.008184 stackdiac-0.0.1.dev24/stackdiac/models/__init__.py
+-rw-r--r--   0        0        0     1145 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/backend.py
+-rw-r--r--   0        0        0     2582 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/binary.py
+-rw-r--r--   0        0        0     3975 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/cluster.py
+-rw-r--r--   0        0        0     2769 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/config.py
+-rw-r--r--   0        0        0     1499 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/operation.py
+-rw-r--r--   0        0        0      161 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/provider.py
+-rw-r--r--   0        0        0     5172 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/repo.py
+-rw-r--r--   0        0        0     1716 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/spec.py
+-rw-r--r--   0        0        0     9330 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/models/stack.py
+-rw-r--r--   0        0        0      108 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/stackd/__init__.py
+-rw-r--r--   0        0        0      193 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/stackd/filters.py
+-rw-r--r--   0        0        0      297 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/stackd/sdmod.py
+-rw-r--r--   0        0        0    10541 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/stackd/stackd.py
+-rw-r--r--   0        0        0   164360 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/ui/4753c5ba57962b4d7bf8.woff
+-rw-r--r--   0        0        0   121340 2023-05-13 00:41:47.012184 stackdiac-0.0.1.dev24/stackdiac/ui/6d63d0501e5ed7b79dab.woff2
+-rw-r--r--   0        0        0  1312554 2023-05-13 00:41:47.020184 stackdiac-0.0.1.dev24/stackdiac/ui/bundle.js
+-rw-r--r--   0        0        0     2766 2023-05-13 00:41:47.020184 stackdiac-0.0.1.dev24/stackdiac/ui/bundle.js.LICENSE.txt
+-rw-r--r--   0        0        0      415 2023-05-13 00:41:47.020184 stackdiac-0.0.1.dev24/stackdiac/ui/index.html
+-rw-r--r--   0        0        0     2290 1970-01-01 00:00:00.000000 stackdiac-0.0.1.dev24/PKG-INFO
```

### Comparing `stackdiac-0.0.1.dev23/LICENSE` & `stackdiac-0.0.1.dev24/LICENSE`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/README.md` & `stackdiac-0.0.1.dev24/README.md`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/pyproject.toml` & `stackdiac-0.0.1.dev24/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "stackdiac"
-version = "0.0.1-dev23"
+version = "0.0.1-dev24"
 description = ""
 authors = ["sysr9 <38893296+sysr9@users.noreply.github.com>"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.10"
```

### Comparing `stackdiac-0.0.1.dev23/stackdiac/api/server.py` & `stackdiac-0.0.1.dev24/stackdiac/api/server.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/cli/__init__.py` & `stackdiac-0.0.1.dev24/stackdiac/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/cli/build.py` & `stackdiac-0.0.1.dev24/stackdiac/cli/build.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/cli/create.py` & `stackdiac-0.0.1.dev24/stackdiac/cli/create.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/backend.py` & `stackdiac-0.0.1.dev24/stackdiac/models/backend.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/binary.py` & `stackdiac-0.0.1.dev24/stackdiac/models/binary.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/cluster.py` & `stackdiac-0.0.1.dev24/stackdiac/models/cluster.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/config.py` & `stackdiac-0.0.1.dev24/stackdiac/models/config.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/operation.py` & `stackdiac-0.0.1.dev24/stackdiac/models/operation.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/repo.py` & `stackdiac-0.0.1.dev24/stackdiac/models/repo.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/spec.py` & `stackdiac-0.0.1.dev24/stackdiac/models/spec.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/models/stack.py` & `stackdiac-0.0.1.dev24/stackdiac/models/stack.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/stackd/stackd.py` & `stackdiac-0.0.1.dev24/stackdiac/stackd/stackd.py`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/ui/4753c5ba57962b4d7bf8.woff` & `stackdiac-0.0.1.dev24/stackdiac/ui/4753c5ba57962b4d7bf8.woff`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/ui/6d63d0501e5ed7b79dab.woff2` & `stackdiac-0.0.1.dev24/stackdiac/ui/6d63d0501e5ed7b79dab.woff2`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/stackdiac/ui/bundle.js` & `stackdiac-0.0.1.dev24/stackdiac/ui/bundle.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -30496,15 +30496,19 @@
                 }, e.createElement(Yt, {
                     className: "mr-auto"
                 }, Zt.map((function(t, n) {
                     return e.createElement(Xt.J, {
                         key: n,
                         to: t.url
                     }, e.createElement(Yt.Link, null, t.name))
-                })))))))
+                })))), e.createElement(Yt, {
+                    className: "ms-auto"
+                }, e.createElement(Yt.Link, {
+                    href: "/docs"
+                }, "API")))))
             },
             Jt = e.forwardRef((({
                 bsPrefix: e,
                 className: t,
                 as: n = "div",
                 ...r
             }, o) => {
@@ -35085,38 +35089,38 @@
             return ts = Object.assign || function(e) {
                 for (var t, n = 1, r = arguments.length; n < r; n++)
                     for (var o in t = arguments[n]) Object.prototype.hasOwnProperty.call(t, o) && (e[o] = t[o]);
                 return e
             }, ts.apply(this, arguments)
         };
         const ns = Qa(null, {
-                showConfigFileOffcanvas: function(e) {
+                showSpecOffcanvas: function(e) {
                     return {
                         type: es.ShowConfigFileOffcanvas,
-                        config_file: e
+                        spec: e
                     }
                 }
             })((function(t) {
-                var n = t.config_file,
+                var n = t.spec,
                     r = t.text,
                     o = void 0 === r ? null : r,
                     a = t.variant,
                     i = void 0 === a ? "light" : a,
                     s = t.className,
                     l = void 0 === s ? "mx-2 my-1" : s,
                     c = function(e, t) {
                         var n = {};
                         for (var r in e) Object.prototype.hasOwnProperty.call(e, r) && t.indexOf(r) < 0 && (n[r] = e[r]);
                         if (null != e && "function" == typeof Object.getOwnPropertySymbols) {
                             var o = 0;
                             for (r = Object.getOwnPropertySymbols(e); o < r.length; o++) t.indexOf(r[o]) < 0 && Object.prototype.propertyIsEnumerable.call(e, r[o]) && (n[r[o]] = e[r[o]])
                         }
                         return n
-                    }(t, ["config_file", "text", "variant", "className"]),
-                    d = c.showConfigFileOffcanvas;
+                    }(t, ["spec", "text", "variant", "className"]),
+                    d = c.showSpecOffcanvas;
                 return e.createElement(Ji, ts({
                     variant: i,
                     onClick: function() {
                         return d(n)
                     },
                     title: "Show specification",
                     className: l
@@ -35129,15 +35133,15 @@
                     n = t.data;
                 if (t.error, t.isLoading) return e.createElement("div", null, "Loading...");
                 var r = [{
                     name: "Show Config File",
                     icon: "file-earmark",
                     component: ns,
                     props: {
-                        config_file: n.conf.config_file
+                        spec: n.conf.spec
                     }
                 }];
                 return e.createElement(m, {
                     fluid: !0,
                     className: "mb-4"
                 }, e.createElement(en, null, e.createElement(nn, null, e.createElement(Xi, {
                     title: "Project",
@@ -35177,15 +35181,15 @@
                     for (var t, n = 1, r = arguments.length; n < r; n++)
                         for (var o in t = arguments[n]) Object.prototype.hasOwnProperty.call(t, o) && (e[o] = t[o]);
                     return e
                 }, is.apply(this, arguments)
             },
             ss = {
                 show: !1,
-                config_file: null
+                spec: null
             },
             ls = function(e) {
                 var t, n = function(e) {
                         return function(e) {
                             void 0 === e && (e = {});
                             var t = e.thunk,
                                 n = void 0 === t || t,
@@ -35217,25 +35221,25 @@
                     g = gr;
                 c && (g = Lr(Cr({
                     trace: !1
                 }, "object" == typeof c && c)));
                 var h = [m];
                 return Array.isArray(f) ? h = Sr([m], f) : "function" == typeof f && (h = f(h)), br(t, u, g.apply(void 0, h))
             }({
-                reducer: (as = {}, as[Ri.reducerPath] = Ri.reducer, as.ConfigFileOffcanvasStore = function(e, t) {
+                reducer: (as = {}, as[Ri.reducerPath] = Ri.reducer, as.SpecOffcanvasStore = function(e, t) {
                     switch (void 0 === e && (e = ss), t.type) {
                         case es.ShowConfigFileOffcanvas:
                             return is(is({}, e), {
                                 show: !0,
-                                config_file: t.config_file
+                                spec: t.spec
                             });
                         case es.HideConfigFileOffcanvas:
                             return is(is({}, e), {
                                 show: !1,
-                                config_file: null
+                                spec: null
                             });
                         default:
                             return e
                     }
                 }, as),
                 middleware: function(e) {
                     return e().concat(Ri.middleware)
@@ -35618,15 +35622,15 @@
                 return console.log(o, a, i, JSON.stringify(o, null, 2)), i ? e.createElement("div", null, "Loading...") : e.createElement(m, {
                     fluid: !0,
                     className: "mb-4"
                 }, e.createElement(en, null, e.createElement(nn, {
                     md: 12,
                     className: "mt-3"
                 }, e.createElement("h1", null, "Cluster: ", e.createElement("code", null, e.createElement("u", null, o.name)), e.createElement(ns, {
-                    config_file: o.config_file
+                    spec: o.spec
                 }))), e.createElement(nn, null), e.createElement(nn, {
                     md: 12
                 }, e.createElement(Is.Container, {
                     id: "{cluster-${clusterName}-tabs}",
                     defaultActiveKey: "first"
                 }, e.createElement(Ps, {
                     id: "{cluster-${clusterName}-tabs}",
@@ -35652,15 +35656,15 @@
                         return e.createElement(Ji, {
                             variant: "primary",
                             className: "mx-1 mb-2",
                             size: "sm",
                             key: t
                         }, t)
                     }))), e.createElement("td", null, e.createElement(ns, {
-                        config_file: n.stack.config_file,
+                        spec: n.stack.spec,
                         size: "sm"
                     })))
                 }))))), e.createElement(Is, {
                     eventKey: "vars",
                     title: "Variables"
                 }, e.createElement(Xi, {
                     title: "Variables",
@@ -36463,62 +36467,62 @@
                 italic: {
                     fontStyle: "italic"
                 }
             };
         var ll = o(3320);
         const cl = Qa((function(e) {
             return {
-                state: e.ConfigFileOffcanvasStore
+                state: e.SpecOffcanvasStore
             }
         }), {
-            hideConfigFileOffcanvas: function() {
+            hideSpecOffcanvas: function() {
                 return {
                     type: es.HideConfigFileOffcanvas
                 }
             }
         })((function(t) {
             var n = t.state,
-                r = t.hideConfigFileOffcanvas;
-            return null == n.config_file ? null : e.createElement(vt, {
+                r = t.hideSpecOffcanvas;
+            return null == n.spec ? null : e.createElement(vt, {
                 show: n.show,
                 onHide: r,
                 placement: "end"
             }, e.createElement(Is.Container, {
                 id: "cfo-tabs",
                 defaultActiveKey: "data"
             }, e.createElement(vt.Header, {
                 closeButton: !0
-            }, e.createElement(vt.Title, null, "file: ", n.config_file.relpath), e.createElement(Yt, {
+            }, e.createElement(vt.Title, null, "file: ", n.spec.relpath), e.createElement(Yt, {
                 variant: "pills",
                 className: "ms-auto me-2"
             }, e.createElement(Yt.Item, null, e.createElement(Yt.Link, {
                 eventKey: "data"
             }, "Data")), e.createElement(Yt.Item, null, e.createElement(Yt.Link, {
                 eventKey: "source"
             }, "Source")), e.createElement(Yt.Item, null, e.createElement(Yt.Link, {
                 eventKey: "rendered"
             }, "Rendered")))), e.createElement(vt.Body, null, e.createElement(Is.Content, null, e.createElement(Is.Pane, {
                 eventKey: "data",
                 title: "Data"
             }, e.createElement(il, {
                 language: "yaml",
                 style: sl
-            }, ll.dump(n.config_file.data))), e.createElement(Is.Pane, {
+            }, ll.dump(n.spec.data))), e.createElement(Is.Pane, {
                 eventKey: "source",
                 title: "Source"
             }, e.createElement(il, {
                 language: "yaml",
                 style: sl
-            }, n.config_file.source)), e.createElement(Is.Pane, {
+            }, n.spec.source)), e.createElement(Is.Pane, {
                 eventKey: "rendered",
                 title: "Rendered"
             }, e.createElement(il, {
                 language: "yaml",
                 style: sl
-            }, n.config_file.rendered))))))
+            }, n.spec.rendered))))))
         }));
         var dl = o(3379),
             ul = o.n(dl),
             pl = o(7795),
             fl = o.n(pl),
             bl = o(569),
             ml = o.n(bl),
```

### Comparing `stackdiac-0.0.1.dev23/stackdiac/ui/bundle.js.LICENSE.txt` & `stackdiac-0.0.1.dev24/stackdiac/ui/bundle.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `stackdiac-0.0.1.dev23/PKG-INFO` & `stackdiac-0.0.1.dev24/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stackdiac
-Version: 0.0.1.dev23
+Version: 0.0.1.dev24
 Summary: 
 License: MIT
 Author: sysr9
 Author-email: 38893296+sysr9@users.noreply.github.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

