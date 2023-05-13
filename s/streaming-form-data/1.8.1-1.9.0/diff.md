# Comparing `tmp/streaming-form-data-1.8.1.tar.gz` & `tmp/streaming-form-data-1.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "streaming-form-data-1.8.1.tar", last modified: Sat Jan 30 09:55:08 2021, max compression
+gzip compressed data, was "streaming-form-data-1.9.0.tar", last modified: Sat Aug 14 18:13:42 2021, max compression
```

## Comparing `streaming-form-data-1.8.1.tar` & `streaming-form-data-1.9.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (117)        0 2021-01-30 09:55:08.076888 streaming-form-data-1.8.1/
--rw-r--r--   0 runner    (1001) docker     (117)     1077 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (117)     4114 2021-01-30 09:55:08.076888 streaming-form-data-1.8.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (117)     2463 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/README.md
--rw-r--r--   0 runner    (1001) docker     (117)       63 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (117)      218 2021-01-30 09:55:08.076888 streaming-form-data-1.8.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (117)     1487 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (117)        0 2021-01-30 09:55:08.076888 streaming-form-data-1.8.1/streaming_form_data/
--rw-r--r--   0 runner    (1001) docker     (117)      106 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/streaming_form_data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (117)   770183 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/streaming_form_data/_parser.c
--rw-r--r--   0 runner    (1001) docker     (117)     2175 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/streaming_form_data/parser.py
--rw-r--r--   0 runner    (1001) docker     (117)     3206 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/streaming_form_data/targets.py
--rw-r--r--   0 runner    (1001) docker     (117)      401 2021-01-30 09:55:04.000000 streaming-form-data-1.8.1/streaming_form_data/validators.py
-drwxr-xr-x   0 runner    (1001) docker     (117)        0 2021-01-30 09:55:08.076888 streaming-form-data-1.8.1/streaming_form_data.egg-info/
--rw-r--r--   0 runner    (1001) docker     (117)     4114 2021-01-30 09:55:07.000000 streaming-form-data-1.8.1/streaming_form_data.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (117)      384 2021-01-30 09:55:08.000000 streaming-form-data-1.8.1/streaming_form_data.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (117)        1 2021-01-30 09:55:07.000000 streaming-form-data-1.8.1/streaming_form_data.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (117)       20 2021-01-30 09:55:07.000000 streaming-form-data-1.8.1/streaming_form_data.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-08-14 18:13:42.457660 streaming-form-data-1.9.0/
+-rw-r--r--   0 runner    (1001) docker     (121)     1077 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (121)     4165 2021-08-14 18:13:42.457660 streaming-form-data-1.9.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2464 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (121)       63 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)      218 2021-08-14 18:13:42.461660 streaming-form-data-1.9.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1536 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-08-14 18:13:42.457660 streaming-form-data-1.9.0/streaming_form_data/
+-rw-r--r--   0 runner    (1001) docker     (121)      106 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/streaming_form_data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)   771914 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/streaming_form_data/_parser.c
+-rw-r--r--   0 runner    (1001) docker     (121)     2175 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/streaming_form_data/parser.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3206 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/streaming_form_data/targets.py
+-rw-r--r--   0 runner    (1001) docker     (121)      401 2021-08-14 18:13:38.000000 streaming-form-data-1.9.0/streaming_form_data/validators.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-08-14 18:13:42.457660 streaming-form-data-1.9.0/streaming_form_data.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     4165 2021-08-14 18:13:42.000000 streaming-form-data-1.9.0/streaming_form_data.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      384 2021-08-14 18:13:42.000000 streaming-form-data-1.9.0/streaming_form_data.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-08-14 18:13:42.000000 streaming-form-data-1.9.0/streaming_form_data.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       20 2021-08-14 18:13:42.000000 streaming-form-data-1.9.0/streaming_form_data.egg-info/top_level.txt
```

### Comparing `streaming-form-data-1.8.1/LICENSE.txt` & `streaming-form-data-1.9.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `streaming-form-data-1.8.1/PKG-INFO` & `streaming-form-data-1.9.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: streaming-form-data
-Version: 1.8.1
+Version: 1.9.0
 Summary: Streaming parser for multipart/form-data
 Home-page: https://github.com/siddhantgoel/streaming-form-data
 Author: Siddhant Goel
 Author-email: me@sgoel.dev
 License: UNKNOWN
 Description: # Streaming multipart/form-data parser
         
@@ -24,15 +24,15 @@
         ## Installation
         
         ```bash
         $ pip install streaming-form-data
         ```
         
         In case you prefer cloning the Github repository and installing manually, please
-        note that `master` is the development branch, so `stable` is what you should be
+        note that `develop` is the development branch, so `stable` is what you should be
         working with.
         
         ## Usage
         
         ```python
         >>> from streaming_form_data import StreamingFormDataParser
         >>> from streaming_form_data.targets import ValueTarget, FileTarget, NullTarget
@@ -90,10 +90,11 @@
 Classifier: Topic :: Internet :: WWW/HTTP :: Dynamic Content
 Classifier: Topic :: Internet :: WWW/HTTP :: HTTP Servers
 Classifier: Programming Language :: Cython
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3 :: Only
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

### Comparing `streaming-form-data-1.8.1/README.md` & `streaming-form-data-1.9.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 ## Installation
 
 ```bash
 $ pip install streaming-form-data
 ```
 
 In case you prefer cloning the Github repository and installing manually, please
-note that `master` is the development branch, so `stable` is what you should be
+note that `develop` is the development branch, so `stable` is what you should be
 working with.
 
 ## Usage
 
 ```python
 >>> from streaming_form_data import StreamingFormDataParser
 >>> from streaming_form_data.targets import ValueTarget, FileTarget, NullTarget
```

### Comparing `streaming-form-data-1.8.1/setup.py` & `streaming-form-data-1.9.0/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 
 with open(here.joinpath('README.md')) as fd:
     long_description = fd.read()
 
 
 setup(
     name='streaming-form-data',
-    version='1.8.1',
+    version='1.9.0',
     description='Streaming parser for multipart/form-data',
     long_description=long_description,
     long_description_content_type='text/markdown',
     packages=find_packages(),
     ext_modules=[
         Extension(
             'streaming_form_data._parser', ['streaming_form_data/_parser.c'],
@@ -34,12 +34,13 @@
         'Topic :: Internet :: WWW/HTTP :: Dynamic Content',
         'Topic :: Internet :: WWW/HTTP :: HTTP Servers',
         'Programming Language :: Cython',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
+        'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3 :: Only',
     ],
     keywords='form-data, forms, http, multipart, web',
     python_requires='>=3.6',
 )
```

### Comparing `streaming-form-data-1.8.1/streaming_form_data/_parser.c` & `streaming-form-data-1.9.0/streaming_form_data/_parser.c`

 * *Files 0% similar despite different names*

```diff
@@ -1,18 +1,20 @@
-/* Generated by Cython 0.29.21 */
+/* Generated by Cython 0.29.24 */
 
+#ifndef PY_SSIZE_T_CLEAN
 #define PY_SSIZE_T_CLEAN
+#endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
 #elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
     #error Cython requires Python 2.6+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_21"
-#define CYTHON_HEX_VERSION 0x001D15F0
+#define CYTHON_ABI "0_29_24"
+#define CYTHON_HEX_VERSION 0x001D18F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
 #if !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
@@ -422,25 +424,33 @@
 #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX >= 0x030500A1 && CYTHON_USE_UNICODE_INTERNALS
 #define __Pyx_PyDict_GetItemStr(dict, name)  _PyDict_GetItem_KnownHash(dict, name, ((PyASCIIObject *) name)->hash)
 #else
 #define __Pyx_PyDict_GetItemStr(dict, name)  PyDict_GetItem(dict, name)
 #endif
 #if PY_VERSION_HEX > 0x03030000 && defined(PyUnicode_KIND)
   #define CYTHON_PEP393_ENABLED 1
+  #if defined(PyUnicode_IS_READY)
   #define __Pyx_PyUnicode_READY(op)       (likely(PyUnicode_IS_READY(op)) ?\
                                               0 : _PyUnicode_Ready((PyObject *)(op)))
+  #else
+  #define __Pyx_PyUnicode_READY(op)       (0)
+  #endif
   #define __Pyx_PyUnicode_GET_LENGTH(u)   PyUnicode_GET_LENGTH(u)
   #define __Pyx_PyUnicode_READ_CHAR(u, i) PyUnicode_READ_CHAR(u, i)
   #define __Pyx_PyUnicode_MAX_CHAR_VALUE(u)   PyUnicode_MAX_CHAR_VALUE(u)
   #define __Pyx_PyUnicode_KIND(u)         PyUnicode_KIND(u)
   #define __Pyx_PyUnicode_DATA(u)         PyUnicode_DATA(u)
   #define __Pyx_PyUnicode_READ(k, d, i)   PyUnicode_READ(k, d, i)
   #define __Pyx_PyUnicode_WRITE(k, d, i, ch)  PyUnicode_WRITE(k, d, i, ch)
   #if defined(PyUnicode_IS_READY) && defined(PyUnicode_GET_SIZE)
+  #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX >= 0x03090000
+  #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != (likely(PyUnicode_IS_READY(u)) ? PyUnicode_GET_LENGTH(u) : ((PyCompactUnicodeObject *)(u))->wstr_length))
+  #else
   #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != (likely(PyUnicode_IS_READY(u)) ? PyUnicode_GET_LENGTH(u) : PyUnicode_GET_SIZE(u)))
+  #endif
   #else
   #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != PyUnicode_GET_LENGTH(u))
   #endif
 #else
   #define CYTHON_PEP393_ENABLED 0
   #define PyUnicode_1BYTE_KIND  1
   #define PyUnicode_2BYTE_KIND  2
@@ -1514,42 +1524,47 @@
 static PyCodeObject *__pyx_find_code_object(int code_line);
 static void __pyx_insert_code_object(int code_line, PyCodeObject* code_object);
 
 /* AddTraceback.proto */
 static void __Pyx_AddTraceback(const char *funcname, int c_line,
                                int py_line, const char *filename);
 
-/* CIntToPy.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_FinderState(enum __pyx_t_19streaming_form_data_7_parser_FinderState value);
-
-/* CIntToPy.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ParserState(enum __pyx_t_19streaming_form_data_7_parser_ParserState value);
-
-/* CIntToPy.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_unsigned_char(unsigned char value);
-
-/* CIntToPy.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value);
+/* GCCDiagnostics.proto */
+#if defined(__GNUC__) && (__GNUC__ > 4 || (__GNUC__ == 4 && __GNUC_MINOR__ >= 6))
+#define __Pyx_HAS_GCC_DIAGNOSTIC
+#endif
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE size_t __Pyx_PyInt_As_size_t(PyObject *);
 
+/* CIntToPy.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_FinderState(enum __pyx_t_19streaming_form_data_7_parser_FinderState value);
+
 /* CIntFromPy.proto */
 static CYTHON_INLINE enum __pyx_t_19streaming_form_data_7_parser_FinderState __Pyx_PyInt_As_enum____pyx_t_19streaming_form_data_7_parser_FinderState(PyObject *);
 
+/* CIntToPy.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ParserState(enum __pyx_t_19streaming_form_data_7_parser_ParserState value);
+
 /* CIntFromPy.proto */
 static CYTHON_INLINE enum __pyx_t_19streaming_form_data_7_parser_ParserState __Pyx_PyInt_As_enum____pyx_t_19streaming_form_data_7_parser_ParserState(PyObject *);
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE unsigned char __Pyx_PyInt_As_unsigned_char(PyObject *);
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *);
 
 /* CIntToPy.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_unsigned_char(unsigned char value);
+
+/* CIntToPy.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value);
+
+/* CIntToPy.proto */
 static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ErrorGroup(enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup value);
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *);
 
 /* FastTypeChecks.proto */
 #if CYTHON_COMPILING_IN_CPYTHON
@@ -13036,19 +13051,17 @@
   if (__pyx_AsyncGen_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_StopAsyncIteration_USED
   if (__pyx_StopAsyncIteration_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   /*--- Library function declarations ---*/
   /*--- Threads initialization code ---*/
-  #if defined(__PYX_FORCE_INIT_THREADS) && __PYX_FORCE_INIT_THREADS
-  #ifdef WITH_THREAD /* Python build with threading support? */
+  #if defined(WITH_THREAD) && PY_VERSION_HEX < 0x030700F0 && defined(__PYX_FORCE_INIT_THREADS) && __PYX_FORCE_INIT_THREADS
   PyEval_InitThreads();
   #endif
-  #endif
   /*--- Module creation code ---*/
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   __pyx_m = __pyx_pyinit_module;
   Py_INCREF(__pyx_m);
   #else
   #if PY_MAJOR_VERSION < 3
   __pyx_m = Py_InitModule4("_parser", __pyx_methods, 0, 0, PYTHON_API_VERSION); Py_XINCREF(__pyx_m);
@@ -13911,15 +13924,15 @@
                  (num_expected == 1) ? "" : "s", num_found);
 }
 
 /* PyObjectCall */
 #if CYTHON_COMPILING_IN_CPYTHON
 static CYTHON_INLINE PyObject* __Pyx_PyObject_Call(PyObject *func, PyObject *arg, PyObject *kw) {
     PyObject *result;
-    ternaryfunc call = func->ob_type->tp_call;
+    ternaryfunc call = Py_TYPE(func)->tp_call;
     if (unlikely(!call))
         return PyObject_Call(func, arg, kw);
     if (unlikely(Py_EnterRecursiveCall((char*)" while calling a Python object")))
         return NULL;
     result = (*call)(func, arg, kw);
     Py_LeaveRecursiveCall();
     if (unlikely(!result) && unlikely(!PyErr_Occurred())) {
@@ -14349,15 +14362,15 @@
         return __Pyx_PyFunction_FastCall(func, &arg, 1);
     }
 #endif
     if (likely(PyCFunction_Check(func))) {
         if (likely(PyCFunction_GET_FLAGS(func) & METH_O)) {
             return __Pyx_PyObject_CallMethO(func, arg);
 #if CYTHON_FAST_PYCCALL
-        } else if (PyCFunction_GET_FLAGS(func) & METH_FASTCALL) {
+        } else if (__Pyx_PyFastCFunction_Check(func)) {
             return __Pyx_PyCFunction_FastCall(func, &arg, 1);
 #endif
         }
     }
     return __Pyx__PyObject_CallOneArg(func, arg);
 }
 #else
@@ -15818,15 +15831,16 @@
     {(char *) "__module__", T_OBJECT, offsetof(PyCFunctionObject, m_module), PY_WRITE_RESTRICTED, 0},
     {0, 0, 0,  0, 0}
 };
 static PyObject *
 __Pyx_CyFunction_reduce(__pyx_CyFunctionObject *m, CYTHON_UNUSED PyObject *args)
 {
 #if PY_MAJOR_VERSION >= 3
-    return PyUnicode_FromString(m->func.m_ml->ml_name);
+    Py_INCREF(m->func_qualname);
+    return m->func_qualname;
 #else
     return PyString_FromString(m->func.m_ml->ml_name);
 #endif
 }
 static PyMethodDef __pyx_CyFunction_methods[] = {
     {"__reduce__", (PyCFunction)__Pyx_CyFunction_reduce, METH_VARARGS, 0},
     {0, 0, 0, 0}
@@ -16483,141 +16497,24 @@
                 else\
                     goto raise_overflow;\
             }\
         }\
         return (target_type) value;\
     }
 
-/* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_FinderState(enum __pyx_t_19streaming_form_data_7_parser_FinderState value) {
-    const enum __pyx_t_19streaming_form_data_7_parser_FinderState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) ((enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0 - (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 1), const_zero = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0;
-    const int is_unsigned = neg_one > const_zero;
-    if (is_unsigned) {
-        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) < sizeof(long)) {
-            return PyInt_FromLong((long) value);
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(unsigned long)) {
-            return PyLong_FromUnsignedLong((unsigned long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(unsigned PY_LONG_LONG)) {
-            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
-#endif
-        }
-    } else {
-        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(long)) {
-            return PyInt_FromLong((long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(PY_LONG_LONG)) {
-            return PyLong_FromLongLong((PY_LONG_LONG) value);
-#endif
-        }
-    }
-    {
-        int one = 1; int little = (int)*(unsigned char *)&one;
-        unsigned char *bytes = (unsigned char *)&value;
-        return _PyLong_FromByteArray(bytes, sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState),
-                                     little, !is_unsigned);
-    }
-}
-
-/* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ParserState(enum __pyx_t_19streaming_form_data_7_parser_ParserState value) {
-    const enum __pyx_t_19streaming_form_data_7_parser_ParserState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) ((enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0 - (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 1), const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0;
-    const int is_unsigned = neg_one > const_zero;
-    if (is_unsigned) {
-        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) < sizeof(long)) {
-            return PyInt_FromLong((long) value);
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(unsigned long)) {
-            return PyLong_FromUnsignedLong((unsigned long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(unsigned PY_LONG_LONG)) {
-            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
-#endif
-        }
-    } else {
-        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(long)) {
-            return PyInt_FromLong((long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(PY_LONG_LONG)) {
-            return PyLong_FromLongLong((PY_LONG_LONG) value);
-#endif
-        }
-    }
-    {
-        int one = 1; int little = (int)*(unsigned char *)&one;
-        unsigned char *bytes = (unsigned char *)&value;
-        return _PyLong_FromByteArray(bytes, sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState),
-                                     little, !is_unsigned);
-    }
-}
-
-/* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_unsigned_char(unsigned char value) {
-    const unsigned char neg_one = (unsigned char) ((unsigned char) 0 - (unsigned char) 1), const_zero = (unsigned char) 0;
-    const int is_unsigned = neg_one > const_zero;
-    if (is_unsigned) {
-        if (sizeof(unsigned char) < sizeof(long)) {
-            return PyInt_FromLong((long) value);
-        } else if (sizeof(unsigned char) <= sizeof(unsigned long)) {
-            return PyLong_FromUnsignedLong((unsigned long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(unsigned char) <= sizeof(unsigned PY_LONG_LONG)) {
-            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
-#endif
-        }
-    } else {
-        if (sizeof(unsigned char) <= sizeof(long)) {
-            return PyInt_FromLong((long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(unsigned char) <= sizeof(PY_LONG_LONG)) {
-            return PyLong_FromLongLong((PY_LONG_LONG) value);
-#endif
-        }
-    }
-    {
-        int one = 1; int little = (int)*(unsigned char *)&one;
-        unsigned char *bytes = (unsigned char *)&value;
-        return _PyLong_FromByteArray(bytes, sizeof(unsigned char),
-                                     little, !is_unsigned);
-    }
-}
-
-/* CIntToPy */
-static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
-    const long neg_one = (long) ((long) 0 - (long) 1), const_zero = (long) 0;
-    const int is_unsigned = neg_one > const_zero;
-    if (is_unsigned) {
-        if (sizeof(long) < sizeof(long)) {
-            return PyInt_FromLong((long) value);
-        } else if (sizeof(long) <= sizeof(unsigned long)) {
-            return PyLong_FromUnsignedLong((unsigned long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(long) <= sizeof(unsigned PY_LONG_LONG)) {
-            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
-#endif
-        }
-    } else {
-        if (sizeof(long) <= sizeof(long)) {
-            return PyInt_FromLong((long) value);
-#ifdef HAVE_LONG_LONG
-        } else if (sizeof(long) <= sizeof(PY_LONG_LONG)) {
-            return PyLong_FromLongLong((PY_LONG_LONG) value);
-#endif
-        }
-    }
-    {
-        int one = 1; int little = (int)*(unsigned char *)&one;
-        unsigned char *bytes = (unsigned char *)&value;
-        return _PyLong_FromByteArray(bytes, sizeof(long),
-                                     little, !is_unsigned);
-    }
-}
-
 /* CIntFromPy */
 static CYTHON_INLINE size_t __Pyx_PyInt_As_size_t(PyObject *x) {
-    const size_t neg_one = (size_t) ((size_t) 0 - (size_t) 1), const_zero = (size_t) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const size_t neg_one = (size_t) -1, const_zero = (size_t) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(size_t) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(size_t, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
@@ -16796,17 +16693,62 @@
     return (size_t) -1;
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to size_t");
     return (size_t) -1;
 }
 
+/* CIntToPy */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_FinderState(enum __pyx_t_19streaming_form_data_7_parser_FinderState value) {
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const enum __pyx_t_19streaming_form_data_7_parser_FinderState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) -1, const_zero = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
+    const int is_unsigned = neg_one > const_zero;
+    if (is_unsigned) {
+        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) < sizeof(long)) {
+            return PyInt_FromLong((long) value);
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(unsigned long)) {
+            return PyLong_FromUnsignedLong((unsigned long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(unsigned PY_LONG_LONG)) {
+            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
+#endif
+        }
+    } else {
+        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(long)) {
+            return PyInt_FromLong((long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) <= sizeof(PY_LONG_LONG)) {
+            return PyLong_FromLongLong((PY_LONG_LONG) value);
+#endif
+        }
+    }
+    {
+        int one = 1; int little = (int)*(unsigned char *)&one;
+        unsigned char *bytes = (unsigned char *)&value;
+        return _PyLong_FromByteArray(bytes, sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState),
+                                     little, !is_unsigned);
+    }
+}
+
 /* CIntFromPy */
 static CYTHON_INLINE enum __pyx_t_19streaming_form_data_7_parser_FinderState __Pyx_PyInt_As_enum____pyx_t_19streaming_form_data_7_parser_FinderState(PyObject *x) {
-    const enum __pyx_t_19streaming_form_data_7_parser_FinderState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) ((enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0 - (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 1), const_zero = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const enum __pyx_t_19streaming_form_data_7_parser_FinderState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) -1, const_zero = (enum __pyx_t_19streaming_form_data_7_parser_FinderState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_FinderState) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(enum __pyx_t_19streaming_form_data_7_parser_FinderState, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
@@ -16985,17 +16927,62 @@
     return (enum __pyx_t_19streaming_form_data_7_parser_FinderState) -1;
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to enum __pyx_t_19streaming_form_data_7_parser_FinderState");
     return (enum __pyx_t_19streaming_form_data_7_parser_FinderState) -1;
 }
 
+/* CIntToPy */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ParserState(enum __pyx_t_19streaming_form_data_7_parser_ParserState value) {
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const enum __pyx_t_19streaming_form_data_7_parser_ParserState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) -1, const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
+    const int is_unsigned = neg_one > const_zero;
+    if (is_unsigned) {
+        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) < sizeof(long)) {
+            return PyInt_FromLong((long) value);
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(unsigned long)) {
+            return PyLong_FromUnsignedLong((unsigned long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(unsigned PY_LONG_LONG)) {
+            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
+#endif
+        }
+    } else {
+        if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(long)) {
+            return PyInt_FromLong((long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) <= sizeof(PY_LONG_LONG)) {
+            return PyLong_FromLongLong((PY_LONG_LONG) value);
+#endif
+        }
+    }
+    {
+        int one = 1; int little = (int)*(unsigned char *)&one;
+        unsigned char *bytes = (unsigned char *)&value;
+        return _PyLong_FromByteArray(bytes, sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState),
+                                     little, !is_unsigned);
+    }
+}
+
 /* CIntFromPy */
 static CYTHON_INLINE enum __pyx_t_19streaming_form_data_7_parser_ParserState __Pyx_PyInt_As_enum____pyx_t_19streaming_form_data_7_parser_ParserState(PyObject *x) {
-    const enum __pyx_t_19streaming_form_data_7_parser_ParserState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) ((enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0 - (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 1), const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const enum __pyx_t_19streaming_form_data_7_parser_ParserState neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) -1, const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ParserState) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ParserState) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(enum __pyx_t_19streaming_form_data_7_parser_ParserState, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
@@ -17176,15 +17163,22 @@
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to enum __pyx_t_19streaming_form_data_7_parser_ParserState");
     return (enum __pyx_t_19streaming_form_data_7_parser_ParserState) -1;
 }
 
 /* CIntFromPy */
 static CYTHON_INLINE unsigned char __Pyx_PyInt_As_unsigned_char(PyObject *x) {
-    const unsigned char neg_one = (unsigned char) ((unsigned char) 0 - (unsigned char) 1), const_zero = (unsigned char) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const unsigned char neg_one = (unsigned char) -1, const_zero = (unsigned char) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(unsigned char) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(unsigned char, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
@@ -17365,15 +17359,22 @@
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to unsigned char");
     return (unsigned char) -1;
 }
 
 /* CIntFromPy */
 static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *x) {
-    const long neg_one = (long) ((long) 0 - (long) 1), const_zero = (long) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const long neg_one = (long) -1, const_zero = (long) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(long) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(long, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
@@ -17553,16 +17554,99 @@
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to long");
     return (long) -1;
 }
 
 /* CIntToPy */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_unsigned_char(unsigned char value) {
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const unsigned char neg_one = (unsigned char) -1, const_zero = (unsigned char) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
+    const int is_unsigned = neg_one > const_zero;
+    if (is_unsigned) {
+        if (sizeof(unsigned char) < sizeof(long)) {
+            return PyInt_FromLong((long) value);
+        } else if (sizeof(unsigned char) <= sizeof(unsigned long)) {
+            return PyLong_FromUnsignedLong((unsigned long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(unsigned char) <= sizeof(unsigned PY_LONG_LONG)) {
+            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
+#endif
+        }
+    } else {
+        if (sizeof(unsigned char) <= sizeof(long)) {
+            return PyInt_FromLong((long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(unsigned char) <= sizeof(PY_LONG_LONG)) {
+            return PyLong_FromLongLong((PY_LONG_LONG) value);
+#endif
+        }
+    }
+    {
+        int one = 1; int little = (int)*(unsigned char *)&one;
+        unsigned char *bytes = (unsigned char *)&value;
+        return _PyLong_FromByteArray(bytes, sizeof(unsigned char),
+                                     little, !is_unsigned);
+    }
+}
+
+/* CIntToPy */
+static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const long neg_one = (long) -1, const_zero = (long) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
+    const int is_unsigned = neg_one > const_zero;
+    if (is_unsigned) {
+        if (sizeof(long) < sizeof(long)) {
+            return PyInt_FromLong((long) value);
+        } else if (sizeof(long) <= sizeof(unsigned long)) {
+            return PyLong_FromUnsignedLong((unsigned long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(long) <= sizeof(unsigned PY_LONG_LONG)) {
+            return PyLong_FromUnsignedLongLong((unsigned PY_LONG_LONG) value);
+#endif
+        }
+    } else {
+        if (sizeof(long) <= sizeof(long)) {
+            return PyInt_FromLong((long) value);
+#ifdef HAVE_LONG_LONG
+        } else if (sizeof(long) <= sizeof(PY_LONG_LONG)) {
+            return PyLong_FromLongLong((PY_LONG_LONG) value);
+#endif
+        }
+    }
+    {
+        int one = 1; int little = (int)*(unsigned char *)&one;
+        unsigned char *bytes = (unsigned char *)&value;
+        return _PyLong_FromByteArray(bytes, sizeof(long),
+                                     little, !is_unsigned);
+    }
+}
+
+/* CIntToPy */
 static CYTHON_INLINE PyObject* __Pyx_PyInt_From_enum____pyx_t_19streaming_form_data_7_parser_ErrorGroup(enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup value) {
-    const enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) ((enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) 0 - (enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) 1), const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup neg_one = (enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) -1, const_zero = (enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
     if (is_unsigned) {
         if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) < sizeof(long)) {
             return PyInt_FromLong((long) value);
         } else if (sizeof(enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup) <= sizeof(unsigned long)) {
             return PyLong_FromUnsignedLong((unsigned long) value);
 #ifdef HAVE_LONG_LONG
@@ -17585,15 +17669,22 @@
         return _PyLong_FromByteArray(bytes, sizeof(enum __pyx_t_19streaming_form_data_7_parser_ErrorGroup),
                                      little, !is_unsigned);
     }
 }
 
 /* CIntFromPy */
 static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *x) {
-    const int neg_one = (int) ((int) 0 - (int) 1), const_zero = (int) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const int neg_one = (int) -1, const_zero = (int) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
         if (sizeof(int) < sizeof(long)) {
             __PYX_VERIFY_RETURN_INT(int, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
```

### Comparing `streaming-form-data-1.8.1/streaming_form_data/parser.py` & `streaming-form-data-1.9.0/streaming_form_data/parser.py`

 * *Files identical despite different names*

### Comparing `streaming-form-data-1.8.1/streaming_form_data/targets.py` & `streaming-form-data-1.9.0/streaming_form_data/targets.py`

 * *Files identical despite different names*

### Comparing `streaming-form-data-1.8.1/streaming_form_data.egg-info/PKG-INFO` & `streaming-form-data-1.9.0/streaming_form_data.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: streaming-form-data
-Version: 1.8.1
+Version: 1.9.0
 Summary: Streaming parser for multipart/form-data
 Home-page: https://github.com/siddhantgoel/streaming-form-data
 Author: Siddhant Goel
 Author-email: me@sgoel.dev
 License: UNKNOWN
 Description: # Streaming multipart/form-data parser
         
@@ -24,15 +24,15 @@
         ## Installation
         
         ```bash
         $ pip install streaming-form-data
         ```
         
         In case you prefer cloning the Github repository and installing manually, please
-        note that `master` is the development branch, so `stable` is what you should be
+        note that `develop` is the development branch, so `stable` is what you should be
         working with.
         
         ## Usage
         
         ```python
         >>> from streaming_form_data import StreamingFormDataParser
         >>> from streaming_form_data.targets import ValueTarget, FileTarget, NullTarget
@@ -90,10 +90,11 @@
 Classifier: Topic :: Internet :: WWW/HTTP :: Dynamic Content
 Classifier: Topic :: Internet :: WWW/HTTP :: HTTP Servers
 Classifier: Programming Language :: Cython
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3 :: Only
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
```

