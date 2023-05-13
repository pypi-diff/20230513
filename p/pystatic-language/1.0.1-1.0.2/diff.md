# Comparing `tmp/pystatic-language-1.0.1.tar.gz` & `tmp/pystatic-language-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pystatic-language-1.0.1.tar", last modified: Sat Apr 15 12:25:21 2023, max compression
+gzip compressed data, was "pystatic-language-1.0.2.tar", last modified: Sat May 13 16:48:25 2023, max compression
```

## Comparing `pystatic-language-1.0.1.tar` & `pystatic-language-1.0.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-04-15 12:25:21.632373 pystatic-language-1.0.1/
--rw-rw-rw-   0        0        0      115 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/MANIFEST.in
--rw-rw-rw-   0        0        0     8940 2023-04-15 12:25:21.632373 pystatic-language-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     7852 2023-03-16 09:20:24.000000 pystatic-language-1.0.1/README.md
--rw-rw-rw-   0        0        0    12920 2023-03-17 11:12:17.000000 pystatic-language-1.0.1/build.py
--rw-rw-rw-   0        0        0      925 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pyproject.toml
-drwxrwxrwx   0        0        0        0 2023-04-15 12:25:21.621371 pystatic-language-1.0.1/pystatic/
--rw-rw-rw-   0        0        0     4714 2023-03-10 17:43:12.000000 pystatic-language-1.0.1/pystatic/base.py
--rw-rw-rw-   0        0        0     8401 2023-03-20 21:44:09.000000 pystatic-language-1.0.1/pystatic/casting.py
--rw-rw-rw-   0        0        0     1315 2023-03-10 17:42:36.000000 pystatic-language-1.0.1/pystatic/clean.py
--rw-rw-rw-   0        0        0      489 2023-03-16 09:08:51.000000 pystatic-language-1.0.1/pystatic/document.py
--rw-rw-rw-   0        0        0     4178 2023-03-11 17:32:18.000000 pystatic-language-1.0.1/pystatic/overload.py
--rw-rw-rw-   0        0        0     5874 2023-04-08 15:08:04.000000 pystatic-language-1.0.1/pystatic/private.py
--rw-rw-rw-   0        0        0     8117 2023-04-15 12:24:30.000000 pystatic-language-1.0.1/pystatic/types.py
-drwxrwxrwx   0        0        0        0 2023-04-15 12:25:21.631372 pystatic-language-1.0.1/pystatic_language.egg-info/
--rw-rw-rw-   0        0        0     8940 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pystatic_language.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      439 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pystatic_language.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pystatic_language.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       28 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pystatic_language.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-04-15 12:25:21.000000 pystatic-language-1.0.1/pystatic_language.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       24 2023-03-16 09:21:08.000000 pystatic-language-1.0.1/requirements-dev.txt
--rw-rw-rw-   0        0        0       15 2023-03-16 09:10:53.000000 pystatic-language-1.0.1/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-04-15 12:25:21.632373 pystatic-language-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1952 2023-04-15 12:25:17.000000 pystatic-language-1.0.1/setup.py
--rw-rw-rw-   0        0        0     2874 2023-04-08 15:05:57.000000 pystatic-language-1.0.1/test.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:48:25.773500 pystatic-language-1.0.2/
+-rw-rw-rw-   0        0        0      115 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     8940 2023-05-13 16:48:25.772498 pystatic-language-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     7852 2023-03-16 09:20:24.000000 pystatic-language-1.0.2/README.md
+-rw-rw-rw-   0        0        0    12920 2023-03-17 11:12:17.000000 pystatic-language-1.0.2/build.py
+-rw-rw-rw-   0        0        0      925 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pyproject.toml
+drwxrwxrwx   0        0        0        0 2023-05-13 16:48:25.755984 pystatic-language-1.0.2/pystatic/
+-rw-rw-rw-   0        0        0     4714 2023-03-10 17:43:12.000000 pystatic-language-1.0.2/pystatic/base.py
+-rw-rw-rw-   0        0        0     8401 2023-03-20 21:44:09.000000 pystatic-language-1.0.2/pystatic/casting.py
+-rw-rw-rw-   0        0        0     1315 2023-03-10 17:42:36.000000 pystatic-language-1.0.2/pystatic/clean.py
+-rw-rw-rw-   0        0        0      489 2023-03-16 09:08:51.000000 pystatic-language-1.0.2/pystatic/document.py
+-rw-rw-rw-   0        0        0     5828 2023-05-13 16:46:00.000000 pystatic-language-1.0.2/pystatic/overload.py
+-rw-rw-rw-   0        0        0     5879 2023-05-13 08:43:44.000000 pystatic-language-1.0.2/pystatic/private.py
+-rw-rw-rw-   0        0        0     8144 2023-05-13 08:43:44.000000 pystatic-language-1.0.2/pystatic/types.py
+drwxrwxrwx   0        0        0        0 2023-05-13 16:48:25.771494 pystatic-language-1.0.2/pystatic_language.egg-info/
+-rw-rw-rw-   0        0        0     8940 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pystatic_language.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      439 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pystatic_language.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pystatic_language.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       28 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pystatic_language.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 16:48:25.000000 pystatic-language-1.0.2/pystatic_language.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       24 2023-03-16 09:21:08.000000 pystatic-language-1.0.2/requirements-dev.txt
+-rw-rw-rw-   0        0        0       15 2023-03-16 09:10:53.000000 pystatic-language-1.0.2/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 16:48:25.773500 pystatic-language-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1952 2023-05-13 16:48:08.000000 pystatic-language-1.0.2/setup.py
+-rw-rw-rw-   0        0        0     3093 2023-05-13 16:47:31.000000 pystatic-language-1.0.2/test.py
```

### Comparing `pystatic-language-1.0.1/PKG-INFO` & `pystatic-language-1.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pystatic-language
-Version: 1.0.1
+Version: 1.0.2
 Summary: This package is a collection of methods and classes for making python more secure, robust, and reliable. This could be achieved through the simple usage of decorators, function calls and inheritance of base classes. Generally, this package can make python a programming language, closer to other static-typed languages, without losing python's dynamic powerful features and.
 Home-page: https://github.com/Shahaf-F-S/pystatic
 Author: Shahaf Frank-Shapir
 Author-email: shahaffrs@gmail.com
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pystatic-language-1.0.1/README.md` & `pystatic-language-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `pystatic-language-1.0.1/build.py` & `pystatic-language-1.0.2/build.py`

 * *Files identical despite different names*

### Comparing `pystatic-language-1.0.1/pyproject.toml` & `pystatic-language-1.0.2/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = 'pystatic-language'
-version = '1.0.1'
+version = '1.0.2'
 description = "This package is a collection of methods and classes for making python more secure, robust, and reliable. This could be achieved through the simple usage of decorators, function calls and inheritance of base classes. Generally, this package can make python a programming language, closer to other static-typed languages, without losing python's dynamic powerful features and."
 classifiers = [
 	'Intended Audience :: Developers',
 	'License :: OSI Approved :: MIT License',
 	'Programming Language :: Python',
 	'Programming Language :: Python :: 3',
 	'Programming Language :: Python :: 3.8',
```

### Comparing `pystatic-language-1.0.1/pystatic/base.py` & `pystatic-language-1.0.2/pystatic/base.py`

 * *Files identical despite different names*

### Comparing `pystatic-language-1.0.1/pystatic/casting.py` & `pystatic-language-1.0.2/pystatic/casting.py`

 * *Files identical despite different names*

### Comparing `pystatic-language-1.0.1/pystatic/clean.py` & `pystatic-language-1.0.2/pystatic/clean.py`

 * *Files identical despite different names*

### Comparing `pystatic-language-1.0.1/pystatic/private.py` & `pystatic-language-1.0.2/pystatic/private.py`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,15 @@
 
     else:
         obj = type(obj)
         base = 'object of type '
     # end if
 
     return f"{base}{repr(obj)} has no attribute '{name}'"
-# end error_message
+# end type_error_message
 
 def in_scope(obj: Any, levels: Optional[int] = 2) -> Any:
     """
     Checks if the statement is inside the scope of the object class.
 
     :param obj: The instance of the class.
     :param levels: The amount of levels to search in.
```

### Comparing `pystatic-language-1.0.1/pystatic/types.py` & `pystatic-language-1.0.2/pystatic/types.py`

 * *Files 2% similar despite different names*

```diff
@@ -21,31 +21,31 @@
 class Config(metaclass=ABCMeta):
     """A class for config settings and system control."""
 
     enforce = True
     crush = True
 # end Config
 
-def error_message(
+def type_error_message(
         obj: Union[Type, Callable], name: str, incorrect: Any, correct: Any
 ) -> str:
     """
-    Defines the class attributes.
+    Returns the error message.
 
     :param obj: The object to wrap.
     :param name: The attribute's name.
     :param incorrect: The incorrect value.
     :param correct: The correct value.
     """
     
     return (
         f"Unexpected type {incorrect} was passed to {name} "
         f"when calling {obj}, but should have been {correct} instead."
     )
-# end error_message
+# end type_error_message
 
 class RuntimeTypeError(TypeError):
     """A class to represent a runtime type error."""
 
     def __init__(
             self,
             obj: Union[Type, Callable],
@@ -59,15 +59,15 @@
         :param obj: The object to wrap.
         :param name: The attribute's name.
         :param incorrect: The incorrect value.
         :param correct: The correct value.
         """
 
         super().__init__(
-            error_message(
+            type_error_message(
                 obj=obj, name=name, incorrect=incorrect,
                 correct=correct
             )
         )
     # end __init__
 # end RuntimeValueTypeError
 
@@ -139,15 +139,15 @@
                     raise RuntimeTypeError(
                         obj=obj, name=key, correct=value,
                         incorrect=type(parameters[key])
                     )
                 
                 else:
                     warnings.warn(
-                        error_message(
+                        type_error_message(
                             obj=obj, name=key, correct=value,
                             incorrect=type(parameters[key])
                         ), RuntimeTypeWarning
                     )
                 # end if
             # end try
         # end for
@@ -165,15 +165,15 @@
                     raise RuntimeTypeError(
                         obj=obj, name=key, incorrect=type(data),
                         correct=obj.__annotations__[key]
                     )
                 
                 else:
                     warnings.warn(
-                        error_message(
+                        type_error_message(
                             obj=obj, name=key, incorrect=type(data),
                             correct=obj.__annotations__[key]
                         ), RuntimeTypeWarning
                     )
                 # end if
             # end try
         # end if
@@ -280,15 +280,15 @@
             raise RuntimeTypeError(
                 obj=value, name=name, incorrect=type(value),
                 correct=hint
             )
 
         else:
             warnings.warn(
-                error_message(
+                type_error_message(
                     obj=value, name=name, incorrect=type(value),
                     correct=hint
                 ), RuntimeTypeWarning
             )
         # end if
     # end try
 # end typecheck
```

### Comparing `pystatic-language-1.0.1/pystatic_language.egg-info/PKG-INFO` & `pystatic-language-1.0.2/pystatic_language.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pystatic-language
-Version: 1.0.1
+Version: 1.0.2
 Summary: This package is a collection of methods and classes for making python more secure, robust, and reliable. This could be achieved through the simple usage of decorators, function calls and inheritance of base classes. Generally, this package can make python a programming language, closer to other static-typed languages, without losing python's dynamic powerful features and.
 Home-page: https://github.com/Shahaf-F-S/pystatic
 Author: Shahaf Frank-Shapir
 Author-email: shahaffrs@gmail.com
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `pystatic-language-1.0.1/setup.py` & `pystatic-language-1.0.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -23,15 +23,15 @@
         ],
         include=[
             "test.py"
         ],
         requirements="requirements.txt",
         dev_requirements="requirements-dev.txt",
         name='pystatic-language',
-        version='1.0.1',
+        version='1.0.2',
         description=(
             "This package is a collection of methods and classes for "
             "making python more secure, robust, and reliable. "
             "This could be achieved through the simple usage of decorators, "
             "function calls and inheritance of base classes. "
             "Generally, this package can make python a programming language, "
             "closer to other static-typed languages, "
```

### Comparing `pystatic-language-1.0.1/test.py` & `pystatic-language-1.0.2/test.py`

 * *Files 3% similar despite different names*

```diff
@@ -60,20 +60,30 @@
 
         self.__d = 0
         print("\t\t>>> self.__d = 0")
         print("\t\t>>> print(self.__d)")
         print(f"\t\t{self.__d}\n")
 
     @overload
+    def a(self):
+        pass
+
+    @a.overload
     def a(self, x: int):
         print("\n\tdef a(self, x: int):")
         print(f"\n\t\t>>> print(type(x))")
         print(f"\t\t{type(x)}\n")
 
     @a.overload
+    def a(self, x: str):
+        print("\n\tdef a(self, x: str):")
+        print(f"\n\t\t>>> print(type(x))")
+        print(f"\t\t{type(x)}\n")
+
+    @a.overload
     @staticmethod
     def a(x: float):
         print("\n\t@staticmethod\n\tdef a(x: float):")
         print(f"\n\t\t>>> print(type(x))")
         print(f"\t\t{type(x)}\n")
 
     @a.overload
@@ -87,15 +97,15 @@
     def b(self, x: int):
         print("\n\t@statictypes(crush=False)\n\tdef b(self, x: int):")
         print(f"\n\t\t>>> print(type(x))")
         print(f"\t\t{type(x)}\n")
 
 foo = Foo()
 
-foo.a(0)
+foo.a('')
 foo.a(0.0)
 
 Foo.a(0)
 Foo.a(0.0)
 
 foo.b(0)
 # noinspection PyTypeChecker
```

