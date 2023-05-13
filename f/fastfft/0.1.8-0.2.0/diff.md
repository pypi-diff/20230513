# Comparing `tmp/fastfft-0.1.8.tar.gz` & `tmp/fastfft-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastfft-0.1.8.tar", last modified: Fri May 12 16:21:10 2023, max compression
+gzip compressed data, was "fastfft-0.2.0.tar", last modified: Fri May 12 16:38:08 2023, max compression
```

## Comparing `fastfft-0.1.8.tar` & `fastfft-0.2.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:21:10.406489 fastfft-0.1.8/
--rw-rw-r--   0 root         (0) root         (0)     1069 2023-05-12 16:19:20.000000 fastfft-0.1.8/LICENSE.txt
--rw-rw-r--   0 root         (0) root         (0)       45 2023-05-12 16:19:20.000000 fastfft-0.1.8/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)     1679 2023-05-12 16:21:10.406489 fastfft-0.1.8/PKG-INFO
--rw-rw-r--   0 root         (0) root         (0)       80 2023-05-12 16:19:20.000000 fastfft-0.1.8/README.md
--rw-rw-r--   0 root         (0) root         (0)       27 2023-05-12 16:19:20.000000 fastfft-0.1.8/requirements-dev.txt
--rw-rw-r--   0 root         (0) root         (0)       13 2023-05-12 16:19:20.000000 fastfft-0.1.8/requirements.txt
--rw-rw-r--   0 root         (0) root         (0)     1543 2023-05-12 16:21:10.406489 fastfft-0.1.8/setup.cfg
--rw-rw-r--   0 root         (0) root         (0)     1339 2023-05-12 16:19:20.000000 fastfft-0.1.8/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:21:10.402489 fastfft-0.1.8/src/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:21:10.402489 fastfft-0.1.8/src/fastfft/
--rw-rw-r--   0 root         (0) root         (0)        0 2023-05-12 16:19:20.000000 fastfft-0.1.8/src/fastfft/__init__.py
--rw-r--r--   0 root         (0) root         (0)   222908 2023-05-12 16:21:01.000000 fastfft-0.1.8/src/fastfft/fft.cpp
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:21:10.402489 fastfft-0.1.8/src/fastfft.egg-info/
--rw-r--r--   0 root         (0) root         (0)     1679 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      361 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/not-zip-safe
--rw-r--r--   0 root         (0) root         (0)       43 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        8 2023-05-12 16:21:10.000000 fastfft-0.1.8/src/fastfft.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:21:10.406489 fastfft-0.1.8/tests/
--rw-rw-r--   0 root         (0) root         (0)      134 2023-05-12 16:19:20.000000 fastfft-0.1.8/tests/test_fft2.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:38:08.295604 fastfft-0.2.0/
+-rw-rw-r--   0 root         (0) root         (0)     1069 2023-05-12 16:19:20.000000 fastfft-0.2.0/LICENSE.txt
+-rw-rw-r--   0 root         (0) root         (0)       45 2023-05-12 16:19:20.000000 fastfft-0.2.0/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)     1686 2023-05-12 16:38:08.295604 fastfft-0.2.0/PKG-INFO
+-rw-rw-r--   0 root         (0) root         (0)       88 2023-05-12 16:37:18.000000 fastfft-0.2.0/README.md
+-rw-rw-r--   0 root         (0) root         (0)       27 2023-05-12 16:19:20.000000 fastfft-0.2.0/requirements-dev.txt
+-rw-rw-r--   0 root         (0) root         (0)       13 2023-05-12 16:19:20.000000 fastfft-0.2.0/requirements.txt
+-rw-rw-r--   0 root         (0) root         (0)     1543 2023-05-12 16:38:08.295604 fastfft-0.2.0/setup.cfg
+-rw-rw-r--   0 root         (0) root         (0)     1338 2023-05-12 16:33:00.000000 fastfft-0.2.0/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:38:08.291604 fastfft-0.2.0/src/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:38:08.291604 fastfft-0.2.0/src/fastfft/
+-rw-rw-r--   0 root         (0) root         (0)        0 2023-05-12 16:19:20.000000 fastfft-0.2.0/src/fastfft/__init__.py
+-rw-r--r--   0 root         (0) root         (0)   222554 2023-05-12 16:37:59.000000 fastfft-0.2.0/src/fastfft/fft.cpp
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:38:08.295604 fastfft-0.2.0/src/fastfft.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     1686 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      361 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/not-zip-safe
+-rw-r--r--   0 root         (0) root         (0)       43 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        8 2023-05-12 16:38:08.000000 fastfft-0.2.0/src/fastfft.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-12 16:38:08.295604 fastfft-0.2.0/tests/
+-rw-rw-r--   0 root         (0) root         (0)      134 2023-05-12 16:19:20.000000 fastfft-0.2.0/tests/test_fft2.py
```

### Comparing `fastfft-0.1.8/LICENSE.txt` & `fastfft-0.2.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `fastfft-0.1.8/PKG-INFO` & `fastfft-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fastfft
-Version: 0.1.8
+Version: 0.2.0
 Summary: Discrete Fourier transform implementation by the analog of the Cooley-Tukey algorithm.
 Home-page: https://github.com/BSaaber/fastfft
 Author: Maxim Movshin
 Author-email: maxim-movshin@yandex.ru
 License: MIT
 Project-URL: Documentation, https://github.com/BSaaber/fastfft
 Project-URL: Code, https://github.com/BSaaber/fastfft
@@ -31,10 +31,16 @@
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Requires-Python: >=3.4
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE.txt
 
-# Just a regular readme file
-
-This is package with fft algorithm implementation.
+# FASTFFT
+import
+```
+from fastfft.fft import fft2
+```
+use
+```
+fft([[1, 2], [3, 4]])
+```
```

### Comparing `fastfft-0.1.8/setup.cfg` & `fastfft-0.2.0/setup.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = fastfft
-version = 0.1.8
+version = 0.2.0
 description = Discrete Fourier transform implementation by the analog of the Cooley-Tukey algorithm.
 long_description = file: README.md
 long_description_content_type = text/markdown
 license = MIT
 author = Maxim Movshin
 author_email = maxim-movshin@yandex.ru
 url = https://github.com/BSaaber/fastfft
```

### Comparing `fastfft-0.1.8/setup.py` & `fastfft-0.2.0/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -20,15 +20,15 @@
                 sfile = path + ext
             sources.append(sfile)
         extension.sources[:] = sources
     return extensions
 
 
 extensions = [
-    Extension("fastfft.main", ["src/fastfft/fft.pyx"]),
+    Extension("fastfft.fft", ["src/fastfft/fft.pyx"]),
 ]
 
 CYTHONIZE = bool(int(os.getenv("CYTHONIZE", 0))) and cythonize is not None
 
 if CYTHONIZE:
     compiler_directives = {"language_level": 3, "embedsignature": True}
     extensions = cythonize(extensions, compiler_directives=compiler_directives)
```

### Comparing `fastfft-0.1.8/src/fastfft/fft.cpp` & `fastfft-0.2.0/src/fastfft/fft.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -7,20 +7,20 @@
             [
                 "CYTHON_CCOMPLEX",
                 "0"
             ]
         ],
         "depends": [],
         "language": "c++",
-        "name": "fastfft.main",
+        "name": "fastfft.fft",
         "sources": [
             "src/fastfft/fft.pyx"
         ]
     },
-    "module_name": "fastfft.main"
+    "module_name": "fastfft.fft"
 }
 END: Cython Metadata */
 
 #ifndef PY_SSIZE_T_CLEAN
 #define PY_SSIZE_T_CLEAN
 #endif /* PY_SSIZE_T_CLEAN */
 #include "Python.h"
@@ -768,16 +768,16 @@
   #ifdef __cplusplus
     #define __PYX_EXTERN_C extern "C"
   #else
     #define __PYX_EXTERN_C extern
   #endif
 #endif
 
-#define __PYX_HAVE__fastfft__main
-#define __PYX_HAVE_API__fastfft__main
+#define __PYX_HAVE__fastfft__fft
+#define __PYX_HAVE_API__fastfft__fft
 /* Early includes */
 #include "ios"
 #include "new"
 #include "stdexcept"
 #include "typeinfo"
 #include <vector>
 #include <complex>
@@ -1441,182 +1441,182 @@
 
 /* Module declarations from 'libcpp.vector' */
 
 /* Module declarations from 'libcpp.complex' */
 
 /* Module declarations from 'libcpp' */
 
-/* Module declarations from 'fastfft.main' */
-static std::complex<double>  __pyx_v_7fastfft_4main_PI;
-static std::complex<double>  __pyx_v_7fastfft_4main_I;
-static std::complex<double>  __pyx_v_7fastfft_4main_MINUS_PI_2I;
-static std::complex<double>  __pyx_v_7fastfft_4main_PI_I;
-static void __pyx_f_7fastfft_4main__base2x2fft2(std::vector<std::vector<std::complex<double> > >  &); /*proto*/
-static std::complex<double>  __pyx_f_7fastfft_4main_W(double, double); /*proto*/
-static void __pyx_f_7fastfft_4main__fft2_square(std::vector<std::vector<std::complex<double> > >  &); /*proto*/
+/* Module declarations from 'fastfft.fft' */
+static std::complex<double>  __pyx_v_7fastfft_3fft_PI;
+static std::complex<double>  __pyx_v_7fastfft_3fft_I;
+static std::complex<double>  __pyx_v_7fastfft_3fft_MINUS_PI_2I;
+static std::complex<double>  __pyx_v_7fastfft_3fft_PI_I;
+static void __pyx_f_7fastfft_3fft__base2x2fft2(std::vector<std::vector<std::complex<double> > >  &); /*proto*/
+static std::complex<double>  __pyx_f_7fastfft_3fft_W(double, double); /*proto*/
+static void __pyx_f_7fastfft_3fft__fft2_square(std::vector<std::vector<std::complex<double> > >  &); /*proto*/
 static std::complex<double>  __pyx_convert_complex_from_py_double(PyObject *); /*proto*/
 static std::vector<std::complex<double> >  __pyx_convert_vector_from_py_std_3a__3a_complex_3c_double_3e___(PyObject *); /*proto*/
 static PyObject *__pyx_convert_complex_to_py_double(std::complex<double>  const &); /*proto*/
 static PyObject *__pyx_convert_vector_to_py_std_3a__3a_complex_3c_double_3e___(const std::vector<std::complex<double> >  &); /*proto*/
 static PyObject *__pyx_convert_vector_to_py_std_3a__3a_vector_3c_std_3a__3a_complex_3c_double_3e____3e___(const std::vector<std::vector<std::complex<double> > >  &); /*proto*/
-#define __Pyx_MODULE_NAME "fastfft.main"
-extern int __pyx_module_is_main_fastfft__main;
-int __pyx_module_is_main_fastfft__main = 0;
+#define __Pyx_MODULE_NAME "fastfft.fft"
+extern int __pyx_module_is_main_fastfft__fft;
+int __pyx_module_is_main_fastfft__fft = 0;
 
-/* Implementation of 'fastfft.main' */
+/* Implementation of 'fastfft.fft' */
 static PyObject *__pyx_builtin_range;
 static const char __pyx_k_fft2[] = "fft2";
 static const char __pyx_k_line[] = "line";
 static const char __pyx_k_main[] = "__main__";
 static const char __pyx_k_name[] = "__name__";
 static const char __pyx_k_test[] = "__test__";
 static const char __pyx_k_range[] = "range";
 static const char __pyx_k_matrix[] = "matrix";
 static const char __pyx_k_cpp_matrix[] = "cpp_matrix";
-static const char __pyx_k_fastfft_main[] = "fastfft.main";
+static const char __pyx_k_fastfft_fft[] = "fastfft.fft";
 static const char __pyx_k_cline_in_traceback[] = "cline_in_traceback";
 static const char __pyx_k_src_fastfft_fft_pyx[] = "src/fastfft/fft.pyx";
 static PyObject *__pyx_n_s_cline_in_traceback;
 static PyObject *__pyx_n_s_cpp_matrix;
-static PyObject *__pyx_n_s_fastfft_main;
+static PyObject *__pyx_n_s_fastfft_fft;
 static PyObject *__pyx_n_s_fft2;
 static PyObject *__pyx_n_s_line;
 static PyObject *__pyx_n_s_main;
 static PyObject *__pyx_n_s_matrix;
 static PyObject *__pyx_n_s_name;
 static PyObject *__pyx_n_s_range;
 static PyObject *__pyx_kp_s_src_fastfft_fft_pyx;
 static PyObject *__pyx_n_s_test;
-static PyObject *__pyx_pf_7fastfft_4main_fft2(CYTHON_UNUSED PyObject *__pyx_self, PyObject *__pyx_v_matrix); /* proto */
+static PyObject *__pyx_pf_7fastfft_3fft_fft2(CYTHON_UNUSED PyObject *__pyx_self, PyObject *__pyx_v_matrix); /* proto */
 static PyObject *__pyx_int_0;
 static PyObject *__pyx_int_2;
 static PyObject *__pyx_tuple_;
 static PyObject *__pyx_codeobj__2;
 /* Late includes */
 
-/* "src/fastfft/fft.pyx":17
+/* "fastfft/fft.pyx":17
  * 
  * 
  * cdef void _base2x2fft2(vector[vector[complex[double]]]& matrix):             # <<<<<<<<<<<<<<
  *     matrix[0][0], matrix[0][1] = matrix[0][0] + matrix[0][1], matrix[0][0] - matrix[0][1]
  *     matrix[1][0], matrix[1][1] = matrix[1][0] + matrix[1][1], matrix[1][0] - matrix[1][1]
  */
 
-static void __pyx_f_7fastfft_4main__base2x2fft2(std::vector<std::vector<std::complex<double> > >  &__pyx_v_matrix) {
+static void __pyx_f_7fastfft_3fft__base2x2fft2(std::vector<std::vector<std::complex<double> > >  &__pyx_v_matrix) {
   __Pyx_RefNannyDeclarations
   std::complex<double>  __pyx_t_1;
   std::complex<double>  __pyx_t_2;
   __Pyx_RefNannySetupContext("_base2x2fft2", 0);
 
-  /* "src/fastfft/fft.pyx":18
+  /* "fastfft/fft.pyx":18
  * 
  * cdef void _base2x2fft2(vector[vector[complex[double]]]& matrix):
  *     matrix[0][0], matrix[0][1] = matrix[0][0] + matrix[0][1], matrix[0][0] - matrix[0][1]             # <<<<<<<<<<<<<<
  *     matrix[1][0], matrix[1][1] = matrix[1][0] + matrix[1][1], matrix[1][0] - matrix[1][1]
  * 
  */
   __pyx_t_1 = (((__pyx_v_matrix[0])[0]) + ((__pyx_v_matrix[0])[1]));
   __pyx_t_2 = (((__pyx_v_matrix[0])[0]) - ((__pyx_v_matrix[0])[1]));
   ((__pyx_v_matrix[0])[0]) = __pyx_t_1;
   ((__pyx_v_matrix[0])[1]) = __pyx_t_2;
 
-  /* "src/fastfft/fft.pyx":19
+  /* "fastfft/fft.pyx":19
  * cdef void _base2x2fft2(vector[vector[complex[double]]]& matrix):
  *     matrix[0][0], matrix[0][1] = matrix[0][0] + matrix[0][1], matrix[0][0] - matrix[0][1]
  *     matrix[1][0], matrix[1][1] = matrix[1][0] + matrix[1][1], matrix[1][0] - matrix[1][1]             # <<<<<<<<<<<<<<
  * 
  *     matrix[0][0], matrix[1][0] = matrix[0][0] + matrix[1][0], matrix[0][0] - matrix[1][0]
  */
   __pyx_t_2 = (((__pyx_v_matrix[1])[0]) + ((__pyx_v_matrix[1])[1]));
   __pyx_t_1 = (((__pyx_v_matrix[1])[0]) - ((__pyx_v_matrix[1])[1]));
   ((__pyx_v_matrix[1])[0]) = __pyx_t_2;
   ((__pyx_v_matrix[1])[1]) = __pyx_t_1;
 
-  /* "src/fastfft/fft.pyx":21
+  /* "fastfft/fft.pyx":21
  *     matrix[1][0], matrix[1][1] = matrix[1][0] + matrix[1][1], matrix[1][0] - matrix[1][1]
  * 
  *     matrix[0][0], matrix[1][0] = matrix[0][0] + matrix[1][0], matrix[0][0] - matrix[1][0]             # <<<<<<<<<<<<<<
  *     matrix[0][1], matrix[1][1] = matrix[0][1] + matrix[1][1], matrix[0][1] - matrix[1][1]
  * 
  */
   __pyx_t_1 = (((__pyx_v_matrix[0])[0]) + ((__pyx_v_matrix[1])[0]));
   __pyx_t_2 = (((__pyx_v_matrix[0])[0]) - ((__pyx_v_matrix[1])[0]));
   ((__pyx_v_matrix[0])[0]) = __pyx_t_1;
   ((__pyx_v_matrix[1])[0]) = __pyx_t_2;
 
-  /* "src/fastfft/fft.pyx":22
+  /* "fastfft/fft.pyx":22
  * 
  *     matrix[0][0], matrix[1][0] = matrix[0][0] + matrix[1][0], matrix[0][0] - matrix[1][0]
  *     matrix[0][1], matrix[1][1] = matrix[0][1] + matrix[1][1], matrix[0][1] - matrix[1][1]             # <<<<<<<<<<<<<<
  * 
  * 
  */
   __pyx_t_2 = (((__pyx_v_matrix[0])[1]) + ((__pyx_v_matrix[1])[1]));
   __pyx_t_1 = (((__pyx_v_matrix[0])[1]) - ((__pyx_v_matrix[1])[1]));
   ((__pyx_v_matrix[0])[1]) = __pyx_t_2;
   ((__pyx_v_matrix[1])[1]) = __pyx_t_1;
 
-  /* "src/fastfft/fft.pyx":17
+  /* "fastfft/fft.pyx":17
  * 
  * 
  * cdef void _base2x2fft2(vector[vector[complex[double]]]& matrix):             # <<<<<<<<<<<<<<
  *     matrix[0][0], matrix[0][1] = matrix[0][0] + matrix[0][1], matrix[0][0] - matrix[0][1]
  *     matrix[1][0], matrix[1][1] = matrix[1][0] + matrix[1][1], matrix[1][0] - matrix[1][1]
  */
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
 }
 
-/* "src/fastfft/fft.pyx":25
+/* "fastfft/fft.pyx":25
  * 
  * 
  * cdef complex[double] W(double n, double m):             # <<<<<<<<<<<<<<
  *     return exp[double](MINUS_PI_2I * m / n)
  * 
  */
 
-static std::complex<double>  __pyx_f_7fastfft_4main_W(double __pyx_v_n, double __pyx_v_m) {
+static std::complex<double>  __pyx_f_7fastfft_3fft_W(double __pyx_v_n, double __pyx_v_m) {
   std::complex<double>  __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("W", 0);
 
-  /* "src/fastfft/fft.pyx":26
+  /* "fastfft/fft.pyx":26
  * 
  * cdef complex[double] W(double n, double m):
  *     return exp[double](MINUS_PI_2I * m / n)             # <<<<<<<<<<<<<<
  * 
  * 
  */
-  __pyx_r = std::exp<double>(((__pyx_v_7fastfft_4main_MINUS_PI_2I * __pyx_v_m) / __pyx_v_n));
+  __pyx_r = std::exp<double>(((__pyx_v_7fastfft_3fft_MINUS_PI_2I * __pyx_v_m) / __pyx_v_n));
   goto __pyx_L0;
 
-  /* "src/fastfft/fft.pyx":25
+  /* "fastfft/fft.pyx":25
  * 
  * 
  * cdef complex[double] W(double n, double m):             # <<<<<<<<<<<<<<
  *     return exp[double](MINUS_PI_2I * m / n)
  * 
  */
 
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
-/* "src/fastfft/fft.pyx":29
+/* "fastfft/fft.pyx":29
  * 
  * 
  * cdef void _fft2_square(vector[vector[complex[double]]]& matrix):             # <<<<<<<<<<<<<<
  *     cdef int n = matrix.size()
  *     cdef half_n = n // 2
  */
 
-static void __pyx_f_7fastfft_4main__fft2_square(std::vector<std::vector<std::complex<double> > >  &__pyx_v_matrix) {
+static void __pyx_f_7fastfft_3fft__fft2_square(std::vector<std::vector<std::complex<double> > >  &__pyx_v_matrix) {
   int __pyx_v_n;
   PyObject *__pyx_v_half_n = 0;
   std::vector<std::vector<std::complex<double> > >  __pyx_v_matrix00;
   std::vector<std::vector<std::complex<double> > >  __pyx_v_matrix01;
   std::vector<std::vector<std::complex<double> > >  __pyx_v_matrix10;
   std::vector<std::vector<std::complex<double> > >  __pyx_v_matrix11;
   std::vector<std::complex<double> >  __pyx_v_line0;
@@ -1643,113 +1643,113 @@
   std::vector<std::complex<double> > ::size_type __pyx_t_13;
   double __pyx_t_14;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("_fft2_square", 0);
 
-  /* "src/fastfft/fft.pyx":30
+  /* "fastfft/fft.pyx":30
  * 
  * cdef void _fft2_square(vector[vector[complex[double]]]& matrix):
  *     cdef int n = matrix.size()             # <<<<<<<<<<<<<<
  *     cdef half_n = n // 2
  *     if n == 2:
  */
   __pyx_v_n = __pyx_v_matrix.size();
 
-  /* "src/fastfft/fft.pyx":31
+  /* "fastfft/fft.pyx":31
  * cdef void _fft2_square(vector[vector[complex[double]]]& matrix):
  *     cdef int n = matrix.size()
  *     cdef half_n = n // 2             # <<<<<<<<<<<<<<
  *     if n == 2:
  *         _base2x2fft2(matrix)
  */
   __pyx_t_1 = __Pyx_PyInt_From_long(__Pyx_div_long(__pyx_v_n, 2)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 31, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   __pyx_v_half_n = __pyx_t_1;
   __pyx_t_1 = 0;
 
-  /* "src/fastfft/fft.pyx":32
+  /* "fastfft/fft.pyx":32
  *     cdef int n = matrix.size()
  *     cdef half_n = n // 2
  *     if n == 2:             # <<<<<<<<<<<<<<
  *         _base2x2fft2(matrix)
  *         return
  */
   __pyx_t_2 = ((__pyx_v_n == 2) != 0);
   if (__pyx_t_2) {
 
-    /* "src/fastfft/fft.pyx":33
+    /* "fastfft/fft.pyx":33
  *     cdef half_n = n // 2
  *     if n == 2:
  *         _base2x2fft2(matrix)             # <<<<<<<<<<<<<<
  *         return
  * 
  */
-    __pyx_f_7fastfft_4main__base2x2fft2(__pyx_v_matrix);
+    __pyx_f_7fastfft_3fft__base2x2fft2(__pyx_v_matrix);
 
-    /* "src/fastfft/fft.pyx":34
+    /* "fastfft/fft.pyx":34
  *     if n == 2:
  *         _base2x2fft2(matrix)
  *         return             # <<<<<<<<<<<<<<
  * 
  *     cdef vector[vector[complex[double]]] matrix00, matrix01, matrix10, matrix11
  */
     goto __pyx_L0;
 
-    /* "src/fastfft/fft.pyx":32
+    /* "fastfft/fft.pyx":32
  *     cdef int n = matrix.size()
  *     cdef half_n = n // 2
  *     if n == 2:             # <<<<<<<<<<<<<<
  *         _base2x2fft2(matrix)
  *         return
  */
   }
 
-  /* "src/fastfft/fft.pyx":38
+  /* "fastfft/fft.pyx":38
  *     cdef vector[vector[complex[double]]] matrix00, matrix01, matrix10, matrix11
  * 
  *     matrix00.reserve(half_n)             # <<<<<<<<<<<<<<
  *     matrix01.reserve(half_n)
  *     matrix10.reserve(half_n)
  */
   __pyx_t_3 = __Pyx_PyInt_As_size_t(__pyx_v_half_n); if (unlikely((__pyx_t_3 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 38, __pyx_L1_error)
   __pyx_v_matrix00.reserve(__pyx_t_3);
 
-  /* "src/fastfft/fft.pyx":39
+  /* "fastfft/fft.pyx":39
  * 
  *     matrix00.reserve(half_n)
  *     matrix01.reserve(half_n)             # <<<<<<<<<<<<<<
  *     matrix10.reserve(half_n)
  *     matrix11.reserve(half_n)
  */
   __pyx_t_3 = __Pyx_PyInt_As_size_t(__pyx_v_half_n); if (unlikely((__pyx_t_3 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 39, __pyx_L1_error)
   __pyx_v_matrix01.reserve(__pyx_t_3);
 
-  /* "src/fastfft/fft.pyx":40
+  /* "fastfft/fft.pyx":40
  *     matrix00.reserve(half_n)
  *     matrix01.reserve(half_n)
  *     matrix10.reserve(half_n)             # <<<<<<<<<<<<<<
  *     matrix11.reserve(half_n)
  * 
  */
   __pyx_t_3 = __Pyx_PyInt_As_size_t(__pyx_v_half_n); if (unlikely((__pyx_t_3 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 40, __pyx_L1_error)
   __pyx_v_matrix10.reserve(__pyx_t_3);
 
-  /* "src/fastfft/fft.pyx":41
+  /* "fastfft/fft.pyx":41
  *     matrix01.reserve(half_n)
  *     matrix10.reserve(half_n)
  *     matrix11.reserve(half_n)             # <<<<<<<<<<<<<<
  * 
  * 
  */
   __pyx_t_3 = __Pyx_PyInt_As_size_t(__pyx_v_half_n); if (unlikely((__pyx_t_3 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 41, __pyx_L1_error)
   __pyx_v_matrix11.reserve(__pyx_t_3);
 
-  /* "src/fastfft/fft.pyx":47
+  /* "fastfft/fft.pyx":47
  *     cdef vector[complex[double]] line1
  *     # todo - redo
  *     for i in range(half_n):             # <<<<<<<<<<<<<<
  *         line0.push_back(I)
  *         line1.push_back(I)
  */
   __pyx_t_1 = __Pyx_PyObject_CallOneArg(__pyx_builtin_range, __pyx_v_half_n); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 47, __pyx_L1_error)
@@ -1793,53 +1793,53 @@
         break;
       }
       __Pyx_GOTREF(__pyx_t_1);
     }
     __Pyx_XDECREF_SET(__pyx_v_i, __pyx_t_1);
     __pyx_t_1 = 0;
 
-    /* "src/fastfft/fft.pyx":48
+    /* "fastfft/fft.pyx":48
  *     # todo - redo
  *     for i in range(half_n):
  *         line0.push_back(I)             # <<<<<<<<<<<<<<
  *         line1.push_back(I)
  * 
  */
     try {
-      __pyx_v_line0.push_back(__pyx_v_7fastfft_4main_I);
+      __pyx_v_line0.push_back(__pyx_v_7fastfft_3fft_I);
     } catch(...) {
       __Pyx_CppExn2PyErr();
       __PYX_ERR(0, 48, __pyx_L1_error)
     }
 
-    /* "src/fastfft/fft.pyx":49
+    /* "fastfft/fft.pyx":49
  *     for i in range(half_n):
  *         line0.push_back(I)
  *         line1.push_back(I)             # <<<<<<<<<<<<<<
  * 
  *     for i in range(n):
  */
     try {
-      __pyx_v_line1.push_back(__pyx_v_7fastfft_4main_I);
+      __pyx_v_line1.push_back(__pyx_v_7fastfft_3fft_I);
     } catch(...) {
       __Pyx_CppExn2PyErr();
       __PYX_ERR(0, 49, __pyx_L1_error)
     }
 
-    /* "src/fastfft/fft.pyx":47
+    /* "fastfft/fft.pyx":47
  *     cdef vector[complex[double]] line1
  *     # todo - redo
  *     for i in range(half_n):             # <<<<<<<<<<<<<<
  *         line0.push_back(I)
  *         line1.push_back(I)
  */
   }
   __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
 
-  /* "src/fastfft/fft.pyx":51
+  /* "fastfft/fft.pyx":51
  *         line1.push_back(I)
  * 
  *     for i in range(n):             # <<<<<<<<<<<<<<
  *         for j in range(n):
  *             if j % 2 == 0:
  */
   __pyx_t_4 = __Pyx_PyInt_From_int(__pyx_v_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 51, __pyx_L1_error)
@@ -1886,15 +1886,15 @@
         break;
       }
       __Pyx_GOTREF(__pyx_t_1);
     }
     __Pyx_XDECREF_SET(__pyx_v_i, __pyx_t_1);
     __pyx_t_1 = 0;
 
-    /* "src/fastfft/fft.pyx":52
+    /* "fastfft/fft.pyx":52
  * 
  *     for i in range(n):
  *         for j in range(n):             # <<<<<<<<<<<<<<
  *             if j % 2 == 0:
  *                 line0[j // 2] = matrix[i][j]
  */
     __pyx_t_1 = __Pyx_PyInt_From_int(__pyx_v_n); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 52, __pyx_L1_error)
@@ -1941,15 +1941,15 @@
           break;
         }
         __Pyx_GOTREF(__pyx_t_7);
       }
       __Pyx_XDECREF_SET(__pyx_v_j, __pyx_t_7);
       __pyx_t_7 = 0;
 
-      /* "src/fastfft/fft.pyx":53
+      /* "fastfft/fft.pyx":53
  *     for i in range(n):
  *         for j in range(n):
  *             if j % 2 == 0:             # <<<<<<<<<<<<<<
  *                 line0[j // 2] = matrix[i][j]
  *             else:
  */
       __pyx_t_7 = __Pyx_PyInt_RemainderObjC(__pyx_v_j, __pyx_int_2, 2, 0, 0); if (unlikely(!__pyx_t_7)) __PYX_ERR(0, 53, __pyx_L1_error)
@@ -1957,40 +1957,40 @@
       __pyx_t_10 = __Pyx_PyInt_EqObjC(__pyx_t_7, __pyx_int_0, 0, 0); if (unlikely(!__pyx_t_10)) __PYX_ERR(0, 53, __pyx_L1_error)
       __Pyx_GOTREF(__pyx_t_10);
       __Pyx_DECREF(__pyx_t_7); __pyx_t_7 = 0;
       __pyx_t_2 = __Pyx_PyObject_IsTrue(__pyx_t_10); if (unlikely(__pyx_t_2 < 0)) __PYX_ERR(0, 53, __pyx_L1_error)
       __Pyx_DECREF(__pyx_t_10); __pyx_t_10 = 0;
       if (__pyx_t_2) {
 
-        /* "src/fastfft/fft.pyx":54
+        /* "fastfft/fft.pyx":54
  *         for j in range(n):
  *             if j % 2 == 0:
  *                 line0[j // 2] = matrix[i][j]             # <<<<<<<<<<<<<<
  *             else:
  *                 line1[j // 2] = matrix[i][j]
  */
         __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 54, __pyx_L1_error)
         __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 54, __pyx_L1_error)
         __pyx_t_10 = __Pyx_PyInt_FloorDivideObjC(__pyx_v_j, __pyx_int_2, 2, 0, 0); if (unlikely(!__pyx_t_10)) __PYX_ERR(0, 54, __pyx_L1_error)
         __Pyx_GOTREF(__pyx_t_10);
         __pyx_t_13 = __Pyx_PyInt_As_size_t(__pyx_t_10); if (unlikely((__pyx_t_13 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 54, __pyx_L1_error)
         __Pyx_DECREF(__pyx_t_10); __pyx_t_10 = 0;
         (__pyx_v_line0[__pyx_t_13]) = ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]);
 
-        /* "src/fastfft/fft.pyx":53
+        /* "fastfft/fft.pyx":53
  *     for i in range(n):
  *         for j in range(n):
  *             if j % 2 == 0:             # <<<<<<<<<<<<<<
  *                 line0[j // 2] = matrix[i][j]
  *             else:
  */
         goto __pyx_L10;
       }
 
-      /* "src/fastfft/fft.pyx":56
+      /* "fastfft/fft.pyx":56
  *                 line0[j // 2] = matrix[i][j]
  *             else:
  *                 line1[j // 2] = matrix[i][j]             # <<<<<<<<<<<<<<
  *         if i % 2 == 0:
  *             matrix00.push_back(line0)
  */
       /*else*/ {
@@ -2000,25 +2000,25 @@
         __Pyx_GOTREF(__pyx_t_10);
         __pyx_t_13 = __Pyx_PyInt_As_size_t(__pyx_t_10); if (unlikely((__pyx_t_13 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 56, __pyx_L1_error)
         __Pyx_DECREF(__pyx_t_10); __pyx_t_10 = 0;
         (__pyx_v_line1[__pyx_t_13]) = ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]);
       }
       __pyx_L10:;
 
-      /* "src/fastfft/fft.pyx":52
+      /* "fastfft/fft.pyx":52
  * 
  *     for i in range(n):
  *         for j in range(n):             # <<<<<<<<<<<<<<
  *             if j % 2 == 0:
  *                 line0[j // 2] = matrix[i][j]
  */
     }
     __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
 
-    /* "src/fastfft/fft.pyx":57
+    /* "fastfft/fft.pyx":57
  *             else:
  *                 line1[j // 2] = matrix[i][j]
  *         if i % 2 == 0:             # <<<<<<<<<<<<<<
  *             matrix00.push_back(line0)
  *             matrix01.push_back(line1)
  */
     __pyx_t_1 = __Pyx_PyInt_RemainderObjC(__pyx_v_i, __pyx_int_2, 2, 0, 0); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 57, __pyx_L1_error)
@@ -2026,68 +2026,68 @@
     __pyx_t_10 = __Pyx_PyInt_EqObjC(__pyx_t_1, __pyx_int_0, 0, 0); if (unlikely(!__pyx_t_10)) __PYX_ERR(0, 57, __pyx_L1_error)
     __Pyx_GOTREF(__pyx_t_10);
     __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
     __pyx_t_2 = __Pyx_PyObject_IsTrue(__pyx_t_10); if (unlikely(__pyx_t_2 < 0)) __PYX_ERR(0, 57, __pyx_L1_error)
     __Pyx_DECREF(__pyx_t_10); __pyx_t_10 = 0;
     if (__pyx_t_2) {
 
-      /* "src/fastfft/fft.pyx":58
+      /* "fastfft/fft.pyx":58
  *                 line1[j // 2] = matrix[i][j]
  *         if i % 2 == 0:
  *             matrix00.push_back(line0)             # <<<<<<<<<<<<<<
  *             matrix01.push_back(line1)
  *         else:
  */
       try {
         __pyx_v_matrix00.push_back(__pyx_v_line0);
       } catch(...) {
         __Pyx_CppExn2PyErr();
         __PYX_ERR(0, 58, __pyx_L1_error)
       }
 
-      /* "src/fastfft/fft.pyx":59
+      /* "fastfft/fft.pyx":59
  *         if i % 2 == 0:
  *             matrix00.push_back(line0)
  *             matrix01.push_back(line1)             # <<<<<<<<<<<<<<
  *         else:
  *             matrix10.push_back(line0)
  */
       try {
         __pyx_v_matrix01.push_back(__pyx_v_line1);
       } catch(...) {
         __Pyx_CppExn2PyErr();
         __PYX_ERR(0, 59, __pyx_L1_error)
       }
 
-      /* "src/fastfft/fft.pyx":57
+      /* "fastfft/fft.pyx":57
  *             else:
  *                 line1[j // 2] = matrix[i][j]
  *         if i % 2 == 0:             # <<<<<<<<<<<<<<
  *             matrix00.push_back(line0)
  *             matrix01.push_back(line1)
  */
       goto __pyx_L11;
     }
 
-    /* "src/fastfft/fft.pyx":61
+    /* "fastfft/fft.pyx":61
  *             matrix01.push_back(line1)
  *         else:
  *             matrix10.push_back(line0)             # <<<<<<<<<<<<<<
  *             matrix11.push_back(line1)
  * 
  */
     /*else*/ {
       try {
         __pyx_v_matrix10.push_back(__pyx_v_line0);
       } catch(...) {
         __Pyx_CppExn2PyErr();
         __PYX_ERR(0, 61, __pyx_L1_error)
       }
 
-      /* "src/fastfft/fft.pyx":62
+      /* "fastfft/fft.pyx":62
  *         else:
  *             matrix10.push_back(line0)
  *             matrix11.push_back(line1)             # <<<<<<<<<<<<<<
  * 
  *     _fft2_square(matrix00)
  */
       try {
@@ -2095,61 +2095,61 @@
       } catch(...) {
         __Pyx_CppExn2PyErr();
         __PYX_ERR(0, 62, __pyx_L1_error)
       }
     }
     __pyx_L11:;
 
-    /* "src/fastfft/fft.pyx":51
+    /* "fastfft/fft.pyx":51
  *         line1.push_back(I)
  * 
  *     for i in range(n):             # <<<<<<<<<<<<<<
  *         for j in range(n):
  *             if j % 2 == 0:
  */
   }
   __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
 
-  /* "src/fastfft/fft.pyx":64
+  /* "fastfft/fft.pyx":64
  *             matrix11.push_back(line1)
  * 
  *     _fft2_square(matrix00)             # <<<<<<<<<<<<<<
  *     _fft2_square(matrix01)
  *     _fft2_square(matrix10)
  */
-  __pyx_f_7fastfft_4main__fft2_square(__pyx_v_matrix00);
+  __pyx_f_7fastfft_3fft__fft2_square(__pyx_v_matrix00);
 
-  /* "src/fastfft/fft.pyx":65
+  /* "fastfft/fft.pyx":65
  * 
  *     _fft2_square(matrix00)
  *     _fft2_square(matrix01)             # <<<<<<<<<<<<<<
  *     _fft2_square(matrix10)
  *     _fft2_square(matrix11)
  */
-  __pyx_f_7fastfft_4main__fft2_square(__pyx_v_matrix01);
+  __pyx_f_7fastfft_3fft__fft2_square(__pyx_v_matrix01);
 
-  /* "src/fastfft/fft.pyx":66
+  /* "fastfft/fft.pyx":66
  *     _fft2_square(matrix00)
  *     _fft2_square(matrix01)
  *     _fft2_square(matrix10)             # <<<<<<<<<<<<<<
  *     _fft2_square(matrix11)
  * 
  */
-  __pyx_f_7fastfft_4main__fft2_square(__pyx_v_matrix10);
+  __pyx_f_7fastfft_3fft__fft2_square(__pyx_v_matrix10);
 
-  /* "src/fastfft/fft.pyx":67
+  /* "fastfft/fft.pyx":67
  *     _fft2_square(matrix01)
  *     _fft2_square(matrix10)
  *     _fft2_square(matrix11)             # <<<<<<<<<<<<<<
  * 
  * 
  */
-  __pyx_f_7fastfft_4main__fft2_square(__pyx_v_matrix11);
+  __pyx_f_7fastfft_3fft__fft2_square(__pyx_v_matrix11);
 
-  /* "src/fastfft/fft.pyx":72
+  /* "fastfft/fft.pyx":72
  *     cdef complex[double] v00, vW10, vW01, vW11
  * 
  *     for i in range(half_n):             # <<<<<<<<<<<<<<
  *         for j in range(half_n):
  *             v00 = matrix00[i][j]
  */
   __pyx_t_4 = __Pyx_PyObject_CallOneArg(__pyx_builtin_range, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 72, __pyx_L1_error)
@@ -2193,15 +2193,15 @@
         break;
       }
       __Pyx_GOTREF(__pyx_t_4);
     }
     __Pyx_XDECREF_SET(__pyx_v_i, __pyx_t_4);
     __pyx_t_4 = 0;
 
-    /* "src/fastfft/fft.pyx":73
+    /* "fastfft/fft.pyx":73
  * 
  *     for i in range(half_n):
  *         for j in range(half_n):             # <<<<<<<<<<<<<<
  *             v00 = matrix00[i][j]
  *             vW10 = matrix10[i][j] * W(n, i)
  */
     __pyx_t_4 = __Pyx_PyObject_CallOneArg(__pyx_builtin_range, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 73, __pyx_L1_error)
@@ -2245,104 +2245,104 @@
           break;
         }
         __Pyx_GOTREF(__pyx_t_4);
       }
       __Pyx_XDECREF_SET(__pyx_v_j, __pyx_t_4);
       __pyx_t_4 = 0;
 
-      /* "src/fastfft/fft.pyx":74
+      /* "fastfft/fft.pyx":74
  *     for i in range(half_n):
  *         for j in range(half_n):
  *             v00 = matrix00[i][j]             # <<<<<<<<<<<<<<
  *             vW10 = matrix10[i][j] * W(n, i)
  *             vW01 = matrix10[i][j] * W(n, j)
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 74, __pyx_L1_error)
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 74, __pyx_L1_error)
       __pyx_v_v00 = ((__pyx_v_matrix00[__pyx_t_11])[__pyx_t_12]);
 
-      /* "src/fastfft/fft.pyx":75
+      /* "fastfft/fft.pyx":75
  *         for j in range(half_n):
  *             v00 = matrix00[i][j]
  *             vW10 = matrix10[i][j] * W(n, i)             # <<<<<<<<<<<<<<
  *             vW01 = matrix10[i][j] * W(n, j)
  *             vW11 = matrix10[i][j] * W(n, i + i)
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 75, __pyx_L1_error)
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 75, __pyx_L1_error)
       __pyx_t_14 = __pyx_PyFloat_AsDouble(__pyx_v_i); if (unlikely((__pyx_t_14 == (double)-1) && PyErr_Occurred())) __PYX_ERR(0, 75, __pyx_L1_error)
-      __pyx_v_vW10 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_4main_W(__pyx_v_n, __pyx_t_14));
+      __pyx_v_vW10 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_3fft_W(__pyx_v_n, __pyx_t_14));
 
-      /* "src/fastfft/fft.pyx":76
+      /* "fastfft/fft.pyx":76
  *             v00 = matrix00[i][j]
  *             vW10 = matrix10[i][j] * W(n, i)
  *             vW01 = matrix10[i][j] * W(n, j)             # <<<<<<<<<<<<<<
  *             vW11 = matrix10[i][j] * W(n, i + i)
  * 
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 76, __pyx_L1_error)
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 76, __pyx_L1_error)
       __pyx_t_14 = __pyx_PyFloat_AsDouble(__pyx_v_j); if (unlikely((__pyx_t_14 == (double)-1) && PyErr_Occurred())) __PYX_ERR(0, 76, __pyx_L1_error)
-      __pyx_v_vW01 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_4main_W(__pyx_v_n, __pyx_t_14));
+      __pyx_v_vW01 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_3fft_W(__pyx_v_n, __pyx_t_14));
 
-      /* "src/fastfft/fft.pyx":77
+      /* "fastfft/fft.pyx":77
  *             vW10 = matrix10[i][j] * W(n, i)
  *             vW01 = matrix10[i][j] * W(n, j)
  *             vW11 = matrix10[i][j] * W(n, i + i)             # <<<<<<<<<<<<<<
  * 
  *             matrix[i][j] = v00 + vW10 + vW01 + vW11
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 77, __pyx_L1_error)
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 77, __pyx_L1_error)
       __pyx_t_4 = PyNumber_Add(__pyx_v_i, __pyx_v_i); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 77, __pyx_L1_error)
       __Pyx_GOTREF(__pyx_t_4);
       __pyx_t_14 = __pyx_PyFloat_AsDouble(__pyx_t_4); if (unlikely((__pyx_t_14 == (double)-1) && PyErr_Occurred())) __PYX_ERR(0, 77, __pyx_L1_error)
       __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
-      __pyx_v_vW11 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_4main_W(__pyx_v_n, __pyx_t_14));
+      __pyx_v_vW11 = (((__pyx_v_matrix10[__pyx_t_11])[__pyx_t_12]) * __pyx_f_7fastfft_3fft_W(__pyx_v_n, __pyx_t_14));
 
-      /* "src/fastfft/fft.pyx":79
+      /* "fastfft/fft.pyx":79
  *             vW11 = matrix10[i][j] * W(n, i + i)
  * 
  *             matrix[i][j] = v00 + vW10 + vW01 + vW11             # <<<<<<<<<<<<<<
  *             matrix[i + half_n][j] = v00 - vW10 + vW01 - vW11
  *             matrix[i][j + half_n] = v00 + vW10 - vW01 - vW11
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 79, __pyx_L1_error)
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 79, __pyx_L1_error)
       ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]) = (((__pyx_v_v00 + __pyx_v_vW10) + __pyx_v_vW01) + __pyx_v_vW11);
 
-      /* "src/fastfft/fft.pyx":80
+      /* "fastfft/fft.pyx":80
  * 
  *             matrix[i][j] = v00 + vW10 + vW01 + vW11
  *             matrix[i + half_n][j] = v00 - vW10 + vW01 - vW11             # <<<<<<<<<<<<<<
  *             matrix[i][j + half_n] = v00 + vW10 - vW01 - vW11
  *             matrix[i + half_n][j + half_n] = v00 - vW10 - vW01 + vW11
  */
       __pyx_t_4 = PyNumber_Add(__pyx_v_i, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 80, __pyx_L1_error)
       __Pyx_GOTREF(__pyx_t_4);
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_t_4); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 80, __pyx_L1_error)
       __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_v_j); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 80, __pyx_L1_error)
       ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]) = (((__pyx_v_v00 - __pyx_v_vW10) + __pyx_v_vW01) - __pyx_v_vW11);
 
-      /* "src/fastfft/fft.pyx":81
+      /* "fastfft/fft.pyx":81
  *             matrix[i][j] = v00 + vW10 + vW01 + vW11
  *             matrix[i + half_n][j] = v00 - vW10 + vW01 - vW11
  *             matrix[i][j + half_n] = v00 + vW10 - vW01 - vW11             # <<<<<<<<<<<<<<
  *             matrix[i + half_n][j + half_n] = v00 - vW10 - vW01 + vW11
  * 
  */
       __pyx_t_11 = __Pyx_PyInt_As_size_t(__pyx_v_i); if (unlikely((__pyx_t_11 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 81, __pyx_L1_error)
       __pyx_t_4 = PyNumber_Add(__pyx_v_j, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 81, __pyx_L1_error)
       __Pyx_GOTREF(__pyx_t_4);
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_t_4); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 81, __pyx_L1_error)
       __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
       ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]) = (((__pyx_v_v00 + __pyx_v_vW10) - __pyx_v_vW01) - __pyx_v_vW11);
 
-      /* "src/fastfft/fft.pyx":82
+      /* "fastfft/fft.pyx":82
  *             matrix[i + half_n][j] = v00 - vW10 + vW01 - vW11
  *             matrix[i][j + half_n] = v00 + vW10 - vW01 - vW11
  *             matrix[i + half_n][j + half_n] = v00 - vW10 - vW01 + vW11             # <<<<<<<<<<<<<<
  * 
  * 
  */
       __pyx_t_4 = PyNumber_Add(__pyx_v_i, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 82, __pyx_L1_error)
@@ -2351,106 +2351,106 @@
       __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
       __pyx_t_4 = PyNumber_Add(__pyx_v_j, __pyx_v_half_n); if (unlikely(!__pyx_t_4)) __PYX_ERR(0, 82, __pyx_L1_error)
       __Pyx_GOTREF(__pyx_t_4);
       __pyx_t_12 = __Pyx_PyInt_As_size_t(__pyx_t_4); if (unlikely((__pyx_t_12 == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 82, __pyx_L1_error)
       __Pyx_DECREF(__pyx_t_4); __pyx_t_4 = 0;
       ((__pyx_v_matrix[__pyx_t_11])[__pyx_t_12]) = (((__pyx_v_v00 - __pyx_v_vW10) - __pyx_v_vW01) + __pyx_v_vW11);
 
-      /* "src/fastfft/fft.pyx":73
+      /* "fastfft/fft.pyx":73
  * 
  *     for i in range(half_n):
  *         for j in range(half_n):             # <<<<<<<<<<<<<<
  *             v00 = matrix00[i][j]
  *             vW10 = matrix10[i][j] * W(n, i)
  */
     }
     __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
 
-    /* "src/fastfft/fft.pyx":72
+    /* "fastfft/fft.pyx":72
  *     cdef complex[double] v00, vW10, vW01, vW11
  * 
  *     for i in range(half_n):             # <<<<<<<<<<<<<<
  *         for j in range(half_n):
  *             v00 = matrix00[i][j]
  */
   }
   __Pyx_DECREF(__pyx_t_10); __pyx_t_10 = 0;
 
-  /* "src/fastfft/fft.pyx":29
+  /* "fastfft/fft.pyx":29
  * 
  * 
  * cdef void _fft2_square(vector[vector[complex[double]]]& matrix):             # <<<<<<<<<<<<<<
  *     cdef int n = matrix.size()
  *     cdef half_n = n // 2
  */
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
   __Pyx_XDECREF(__pyx_t_4);
   __Pyx_XDECREF(__pyx_t_7);
   __Pyx_XDECREF(__pyx_t_10);
-  __Pyx_WriteUnraisable("fastfft.main._fft2_square", __pyx_clineno, __pyx_lineno, __pyx_filename, 1, 0);
+  __Pyx_WriteUnraisable("fastfft.fft._fft2_square", __pyx_clineno, __pyx_lineno, __pyx_filename, 1, 0);
   __pyx_L0:;
   __Pyx_XDECREF(__pyx_v_half_n);
   __Pyx_XDECREF(__pyx_v_i);
   __Pyx_XDECREF(__pyx_v_j);
   __Pyx_RefNannyFinishContext();
 }
 
-/* "src/fastfft/fft.pyx":85
+/* "fastfft/fft.pyx":85
  * 
  * 
  * def fft2(matrix):             # <<<<<<<<<<<<<<
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  */
 
 /* Python wrapper */
-static PyObject *__pyx_pw_7fastfft_4main_1fft2(PyObject *__pyx_self, PyObject *__pyx_v_matrix); /*proto*/
-static char __pyx_doc_7fastfft_4main_fft2[] = "fft2(matrix)";
-static PyMethodDef __pyx_mdef_7fastfft_4main_1fft2 = {"fft2", (PyCFunction)__pyx_pw_7fastfft_4main_1fft2, METH_O, __pyx_doc_7fastfft_4main_fft2};
-static PyObject *__pyx_pw_7fastfft_4main_1fft2(PyObject *__pyx_self, PyObject *__pyx_v_matrix) {
+static PyObject *__pyx_pw_7fastfft_3fft_1fft2(PyObject *__pyx_self, PyObject *__pyx_v_matrix); /*proto*/
+static char __pyx_doc_7fastfft_3fft_fft2[] = "fft2(matrix)";
+static PyMethodDef __pyx_mdef_7fastfft_3fft_1fft2 = {"fft2", (PyCFunction)__pyx_pw_7fastfft_3fft_1fft2, METH_O, __pyx_doc_7fastfft_3fft_fft2};
+static PyObject *__pyx_pw_7fastfft_3fft_1fft2(PyObject *__pyx_self, PyObject *__pyx_v_matrix) {
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("fft2 (wrapper)", 0);
-  __pyx_r = __pyx_pf_7fastfft_4main_fft2(__pyx_self, ((PyObject *)__pyx_v_matrix));
+  __pyx_r = __pyx_pf_7fastfft_3fft_fft2(__pyx_self, ((PyObject *)__pyx_v_matrix));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
-static PyObject *__pyx_pf_7fastfft_4main_fft2(CYTHON_UNUSED PyObject *__pyx_self, PyObject *__pyx_v_matrix) {
+static PyObject *__pyx_pf_7fastfft_3fft_fft2(CYTHON_UNUSED PyObject *__pyx_self, PyObject *__pyx_v_matrix) {
   std::vector<std::vector<std::complex<double> > >  __pyx_v_cpp_matrix;
   PyObject *__pyx_v_line = NULL;
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   Py_ssize_t __pyx_t_1;
   PyObject *__pyx_t_2 = NULL;
   PyObject *(*__pyx_t_3)(PyObject *);
   PyObject *__pyx_t_4 = NULL;
   std::vector<std::complex<double> >  __pyx_t_5;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("fft2", 0);
 
-  /* "src/fastfft/fft.pyx":87
+  /* "fastfft/fft.pyx":87
  * def fft2(matrix):
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))             # <<<<<<<<<<<<<<
  *     for line in matrix:
  *        cpp_matrix.push_back(line)
  */
   __pyx_t_1 = PyObject_Length(__pyx_v_matrix); if (unlikely(__pyx_t_1 == ((Py_ssize_t)-1))) __PYX_ERR(0, 87, __pyx_L1_error)
   __pyx_v_cpp_matrix.reserve(__pyx_t_1);
 
-  /* "src/fastfft/fft.pyx":88
+  /* "fastfft/fft.pyx":88
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  *     for line in matrix:             # <<<<<<<<<<<<<<
  *        cpp_matrix.push_back(line)
  *     _fft2_square(cpp_matrix)
  */
   if (likely(PyList_CheckExact(__pyx_v_matrix)) || PyTuple_CheckExact(__pyx_v_matrix)) {
@@ -2491,72 +2491,72 @@
         break;
       }
       __Pyx_GOTREF(__pyx_t_4);
     }
     __Pyx_XDECREF_SET(__pyx_v_line, __pyx_t_4);
     __pyx_t_4 = 0;
 
-    /* "src/fastfft/fft.pyx":89
+    /* "fastfft/fft.pyx":89
  *     cpp_matrix.reserve(len(matrix))
  *     for line in matrix:
  *        cpp_matrix.push_back(line)             # <<<<<<<<<<<<<<
  *     _fft2_square(cpp_matrix)
  *     return cpp_matrix
  */
     __pyx_t_5 = __pyx_convert_vector_from_py_std_3a__3a_complex_3c_double_3e___(__pyx_v_line); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 89, __pyx_L1_error)
     try {
       __pyx_v_cpp_matrix.push_back(__pyx_t_5);
     } catch(...) {
       __Pyx_CppExn2PyErr();
       __PYX_ERR(0, 89, __pyx_L1_error)
     }
 
-    /* "src/fastfft/fft.pyx":88
+    /* "fastfft/fft.pyx":88
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  *     for line in matrix:             # <<<<<<<<<<<<<<
  *        cpp_matrix.push_back(line)
  *     _fft2_square(cpp_matrix)
  */
   }
   __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
 
-  /* "src/fastfft/fft.pyx":90
+  /* "fastfft/fft.pyx":90
  *     for line in matrix:
  *        cpp_matrix.push_back(line)
  *     _fft2_square(cpp_matrix)             # <<<<<<<<<<<<<<
  *     return cpp_matrix
  */
-  __pyx_f_7fastfft_4main__fft2_square(__pyx_v_cpp_matrix);
+  __pyx_f_7fastfft_3fft__fft2_square(__pyx_v_cpp_matrix);
 
-  /* "src/fastfft/fft.pyx":91
+  /* "fastfft/fft.pyx":91
  *        cpp_matrix.push_back(line)
  *     _fft2_square(cpp_matrix)
  *     return cpp_matrix             # <<<<<<<<<<<<<<
  */
   __Pyx_XDECREF(__pyx_r);
   __pyx_t_2 = __pyx_convert_vector_to_py_std_3a__3a_vector_3c_std_3a__3a_complex_3c_double_3e____3e___(__pyx_v_cpp_matrix); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 91, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_2);
   __pyx_r = __pyx_t_2;
   __pyx_t_2 = 0;
   goto __pyx_L0;
 
-  /* "src/fastfft/fft.pyx":85
+  /* "fastfft/fft.pyx":85
  * 
  * 
  * def fft2(matrix):             # <<<<<<<<<<<<<<
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  */
 
   /* function exit code */
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_2);
   __Pyx_XDECREF(__pyx_t_4);
-  __Pyx_AddTraceback("fastfft.main.fft2", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_AddTraceback("fastfft.fft.fft2", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XDECREF(__pyx_v_line);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -2936,25 +2936,25 @@
 static PyMethodDef __pyx_methods[] = {
   {0, 0, 0, 0}
 };
 
 #if PY_MAJOR_VERSION >= 3
 #if CYTHON_PEP489_MULTI_PHASE_INIT
 static PyObject* __pyx_pymod_create(PyObject *spec, PyModuleDef *def); /*proto*/
-static int __pyx_pymod_exec_main(PyObject* module); /*proto*/
+static int __pyx_pymod_exec_fft(PyObject* module); /*proto*/
 static PyModuleDef_Slot __pyx_moduledef_slots[] = {
   {Py_mod_create, (void*)__pyx_pymod_create},
-  {Py_mod_exec, (void*)__pyx_pymod_exec_main},
+  {Py_mod_exec, (void*)__pyx_pymod_exec_fft},
   {0, NULL}
 };
 #endif
 
 static struct PyModuleDef __pyx_moduledef = {
     PyModuleDef_HEAD_INIT,
-    "main",
+    "fft",
     0, /* m_doc */
   #if CYTHON_PEP489_MULTI_PHASE_INIT
     0, /* m_size */
   #else
     -1, /* m_size */
   #endif
     __pyx_methods /* m_methods */,
@@ -2977,15 +2977,15 @@
     #define CYTHON_SMALL_CODE
 #endif
 #endif
 
 static __Pyx_StringTabEntry __pyx_string_tab[] = {
   {&__pyx_n_s_cline_in_traceback, __pyx_k_cline_in_traceback, sizeof(__pyx_k_cline_in_traceback), 0, 0, 1, 1},
   {&__pyx_n_s_cpp_matrix, __pyx_k_cpp_matrix, sizeof(__pyx_k_cpp_matrix), 0, 0, 1, 1},
-  {&__pyx_n_s_fastfft_main, __pyx_k_fastfft_main, sizeof(__pyx_k_fastfft_main), 0, 0, 1, 1},
+  {&__pyx_n_s_fastfft_fft, __pyx_k_fastfft_fft, sizeof(__pyx_k_fastfft_fft), 0, 0, 1, 1},
   {&__pyx_n_s_fft2, __pyx_k_fft2, sizeof(__pyx_k_fft2), 0, 0, 1, 1},
   {&__pyx_n_s_line, __pyx_k_line, sizeof(__pyx_k_line), 0, 0, 1, 1},
   {&__pyx_n_s_main, __pyx_k_main, sizeof(__pyx_k_main), 0, 0, 1, 1},
   {&__pyx_n_s_matrix, __pyx_k_matrix, sizeof(__pyx_k_matrix), 0, 0, 1, 1},
   {&__pyx_n_s_name, __pyx_k_name, sizeof(__pyx_k_name), 0, 0, 1, 1},
   {&__pyx_n_s_range, __pyx_k_range, sizeof(__pyx_k_range), 0, 0, 1, 1},
   {&__pyx_kp_s_src_fastfft_fft_pyx, __pyx_k_src_fastfft_fft_pyx, sizeof(__pyx_k_src_fastfft_fft_pyx), 0, 0, 1, 0},
@@ -2999,15 +2999,15 @@
   return -1;
 }
 
 static CYTHON_SMALL_CODE int __Pyx_InitCachedConstants(void) {
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__Pyx_InitCachedConstants", 0);
 
-  /* "src/fastfft/fft.pyx":85
+  /* "fastfft/fft.pyx":85
  * 
  * 
  * def fft2(matrix):             # <<<<<<<<<<<<<<
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  */
   __pyx_tuple_ = PyTuple_Pack(3, __pyx_n_s_matrix, __pyx_n_s_cpp_matrix, __pyx_n_s_line); if (unlikely(!__pyx_tuple_)) __PYX_ERR(0, 85, __pyx_L1_error)
@@ -3109,19 +3109,19 @@
 #else
 #define __Pyx_PyMODINIT_FUNC PyObject *
 #endif
 #endif
 
 
 #if PY_MAJOR_VERSION < 3
-__Pyx_PyMODINIT_FUNC initmain(void) CYTHON_SMALL_CODE; /*proto*/
-__Pyx_PyMODINIT_FUNC initmain(void)
+__Pyx_PyMODINIT_FUNC initfft(void) CYTHON_SMALL_CODE; /*proto*/
+__Pyx_PyMODINIT_FUNC initfft(void)
 #else
-__Pyx_PyMODINIT_FUNC PyInit_main(void) CYTHON_SMALL_CODE; /*proto*/
-__Pyx_PyMODINIT_FUNC PyInit_main(void)
+__Pyx_PyMODINIT_FUNC PyInit_fft(void) CYTHON_SMALL_CODE; /*proto*/
+__Pyx_PyMODINIT_FUNC PyInit_fft(void)
 #if CYTHON_PEP489_MULTI_PHASE_INIT
 {
   return PyModuleDef_Init(&__pyx_moduledef);
 }
 static CYTHON_SMALL_CODE int __Pyx_check_single_interpreter(void) {
     #if PY_VERSION_HEX >= 0x030700A1
     static PY_INT64_T main_interpreter_id = -1;
@@ -3180,42 +3180,42 @@
     return module;
 bad:
     Py_XDECREF(module);
     return NULL;
 }
 
 
-static CYTHON_SMALL_CODE int __pyx_pymod_exec_main(PyObject *__pyx_pyinit_module)
+static CYTHON_SMALL_CODE int __pyx_pymod_exec_fft(PyObject *__pyx_pyinit_module)
 #endif
 #endif
 {
   PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannyDeclarations
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   if (__pyx_m) {
     if (__pyx_m == __pyx_pyinit_module) return 0;
-    PyErr_SetString(PyExc_RuntimeError, "Module 'main' has already been imported. Re-initialisation is not supported.");
+    PyErr_SetString(PyExc_RuntimeError, "Module 'fft' has already been imported. Re-initialisation is not supported.");
     return -1;
   }
   #elif PY_MAJOR_VERSION >= 3
   if (__pyx_m) return __Pyx_NewRef(__pyx_m);
   #endif
   #if CYTHON_REFNANNY
 __Pyx_RefNanny = __Pyx_RefNannyImportAPI("refnanny");
 if (!__Pyx_RefNanny) {
   PyErr_Clear();
   __Pyx_RefNanny = __Pyx_RefNannyImportAPI("Cython.Runtime.refnanny");
   if (!__Pyx_RefNanny)
       Py_FatalError("failed to import 'refnanny' module");
 }
 #endif
-  __Pyx_RefNannySetupContext("__Pyx_PyMODINIT_FUNC PyInit_main(void)", 0);
+  __Pyx_RefNannySetupContext("__Pyx_PyMODINIT_FUNC PyInit_fft(void)", 0);
   if (__Pyx_check_binary_version() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #ifdef __Pxy_PyFrame_Initialize_Offsets
   __Pxy_PyFrame_Initialize_Offsets();
   #endif
   __pyx_empty_tuple = PyTuple_New(0); if (unlikely(!__pyx_empty_tuple)) __PYX_ERR(0, 1, __pyx_L1_error)
   __pyx_empty_bytes = PyBytes_FromStringAndSize("", 0); if (unlikely(!__pyx_empty_bytes)) __PYX_ERR(0, 1, __pyx_L1_error)
   __pyx_empty_unicode = PyUnicode_FromStringAndSize("", 0); if (unlikely(!__pyx_empty_unicode)) __PYX_ERR(0, 1, __pyx_L1_error)
@@ -3244,15 +3244,15 @@
   #endif
   /*--- Module creation code ---*/
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   __pyx_m = __pyx_pyinit_module;
   Py_INCREF(__pyx_m);
   #else
   #if PY_MAJOR_VERSION < 3
-  __pyx_m = Py_InitModule4("main", __pyx_methods, 0, 0, PYTHON_API_VERSION); Py_XINCREF(__pyx_m);
+  __pyx_m = Py_InitModule4("fft", __pyx_methods, 0, 0, PYTHON_API_VERSION); Py_XINCREF(__pyx_m);
   #else
   __pyx_m = PyModule_Create(&__pyx_moduledef);
   #endif
   if (unlikely(!__pyx_m)) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   __pyx_d = PyModule_GetDict(__pyx_m); if (unlikely(!__pyx_d)) __PYX_ERR(0, 1, __pyx_L1_error)
   Py_INCREF(__pyx_d);
@@ -3262,22 +3262,22 @@
   Py_INCREF(__pyx_cython_runtime);
   if (PyObject_SetAttrString(__pyx_m, "__builtins__", __pyx_b) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   /*--- Initialize various global constants etc. ---*/
   if (__Pyx_InitGlobals() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #if PY_MAJOR_VERSION < 3 && (__PYX_DEFAULT_STRING_ENCODING_IS_ASCII || __PYX_DEFAULT_STRING_ENCODING_IS_DEFAULT)
   if (__Pyx_init_sys_getdefaultencoding_params() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
-  if (__pyx_module_is_main_fastfft__main) {
+  if (__pyx_module_is_main_fastfft__fft) {
     if (PyObject_SetAttr(__pyx_m, __pyx_n_s_name, __pyx_n_s_main) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   }
   #if PY_MAJOR_VERSION >= 3
   {
     PyObject *modules = PyImport_GetModuleDict(); if (unlikely(!modules)) __PYX_ERR(0, 1, __pyx_L1_error)
-    if (!PyDict_GetItemString(modules, "fastfft.main")) {
-      if (unlikely(PyDict_SetItemString(modules, "fastfft.main", __pyx_m) < 0)) __PYX_ERR(0, 1, __pyx_L1_error)
+    if (!PyDict_GetItemString(modules, "fastfft.fft")) {
+      if (unlikely(PyDict_SetItemString(modules, "fastfft.fft", __pyx_m) < 0)) __PYX_ERR(0, 1, __pyx_L1_error)
     }
   }
   #endif
   /*--- Builtin init code ---*/
   if (__Pyx_InitCachedBuiltins() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   /*--- Constants init code ---*/
   if (__Pyx_InitCachedConstants() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
@@ -3290,63 +3290,63 @@
   (void)__Pyx_modinit_variable_import_code();
   (void)__Pyx_modinit_function_import_code();
   /*--- Execution code ---*/
   #if defined(__Pyx_Generator_USED) || defined(__Pyx_Coroutine_USED)
   if (__Pyx_patch_abc() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
 
-  /* "src/fastfft/fft.pyx":10
+  /* "fastfft/fft.pyx":10
  * 
  * cdef complex[double] PI
  * PI.real(3.141592653589793238462643383279)             # <<<<<<<<<<<<<<
  * cdef complex[double] I
  * I.imag(1)
  */
-  __pyx_v_7fastfft_4main_PI.real(3.141592653589793238462643383279);
+  __pyx_v_7fastfft_3fft_PI.real(3.141592653589793238462643383279);
 
-  /* "src/fastfft/fft.pyx":12
+  /* "fastfft/fft.pyx":12
  * PI.real(3.141592653589793238462643383279)
  * cdef complex[double] I
  * I.imag(1)             # <<<<<<<<<<<<<<
  * cdef complex[double] MINUS_PI_2I = PI * I * (-2)
  * cdef complex[double] PI_I = PI * I
  */
-  __pyx_v_7fastfft_4main_I.imag(1.0);
+  __pyx_v_7fastfft_3fft_I.imag(1.0);
 
-  /* "src/fastfft/fft.pyx":13
+  /* "fastfft/fft.pyx":13
  * cdef complex[double] I
  * I.imag(1)
  * cdef complex[double] MINUS_PI_2I = PI * I * (-2)             # <<<<<<<<<<<<<<
  * cdef complex[double] PI_I = PI * I
  * 
  */
-  __pyx_v_7fastfft_4main_MINUS_PI_2I = ((__pyx_v_7fastfft_4main_PI * __pyx_v_7fastfft_4main_I) * -2.0);
+  __pyx_v_7fastfft_3fft_MINUS_PI_2I = ((__pyx_v_7fastfft_3fft_PI * __pyx_v_7fastfft_3fft_I) * -2.0);
 
-  /* "src/fastfft/fft.pyx":14
+  /* "fastfft/fft.pyx":14
  * I.imag(1)
  * cdef complex[double] MINUS_PI_2I = PI * I * (-2)
  * cdef complex[double] PI_I = PI * I             # <<<<<<<<<<<<<<
  * 
  * 
  */
-  __pyx_v_7fastfft_4main_PI_I = (__pyx_v_7fastfft_4main_PI * __pyx_v_7fastfft_4main_I);
+  __pyx_v_7fastfft_3fft_PI_I = (__pyx_v_7fastfft_3fft_PI * __pyx_v_7fastfft_3fft_I);
 
-  /* "src/fastfft/fft.pyx":85
+  /* "fastfft/fft.pyx":85
  * 
  * 
  * def fft2(matrix):             # <<<<<<<<<<<<<<
  *     cdef vector[vector[complex[double]]] cpp_matrix
  *     cpp_matrix.reserve(len(matrix))
  */
-  __pyx_t_1 = PyCFunction_NewEx(&__pyx_mdef_7fastfft_4main_1fft2, NULL, __pyx_n_s_fastfft_main); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 85, __pyx_L1_error)
+  __pyx_t_1 = PyCFunction_NewEx(&__pyx_mdef_7fastfft_3fft_1fft2, NULL, __pyx_n_s_fastfft_fft); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 85, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   if (PyDict_SetItem(__pyx_d, __pyx_n_s_fft2, __pyx_t_1) < 0) __PYX_ERR(0, 85, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
 
-  /* "src/fastfft/fft.pyx":1
+  /* "fastfft/fft.pyx":1
  * # distutils: language=c++             # <<<<<<<<<<<<<<
  * # distutils: define_macros=CYTHON_CCOMPLEX=0
  * 
  */
   __pyx_t_1 = __Pyx_PyDict_NewPresized(0); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 1, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   if (PyDict_SetItem(__pyx_d, __pyx_n_s_test, __pyx_t_1) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
@@ -3363,19 +3363,19 @@
   /*--- Wrapped vars code ---*/
 
   goto __pyx_L0;
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
   if (__pyx_m) {
     if (__pyx_d) {
-      __Pyx_AddTraceback("init fastfft.main", __pyx_clineno, __pyx_lineno, __pyx_filename);
+      __Pyx_AddTraceback("init fastfft.fft", __pyx_clineno, __pyx_lineno, __pyx_filename);
     }
     Py_CLEAR(__pyx_m);
   } else if (!PyErr_Occurred()) {
-    PyErr_SetString(PyExc_ImportError, "init fastfft.main");
+    PyErr_SetString(PyExc_ImportError, "init fastfft.fft");
   }
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   return (__pyx_m != NULL) ? 0 : -1;
   #elif PY_MAJOR_VERSION >= 3
   return __pyx_m;
```

### Comparing `fastfft-0.1.8/src/fastfft.egg-info/PKG-INFO` & `fastfft-0.2.0/src/fastfft.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fastfft
-Version: 0.1.8
+Version: 0.2.0
 Summary: Discrete Fourier transform implementation by the analog of the Cooley-Tukey algorithm.
 Home-page: https://github.com/BSaaber/fastfft
 Author: Maxim Movshin
 Author-email: maxim-movshin@yandex.ru
 License: MIT
 Project-URL: Documentation, https://github.com/BSaaber/fastfft
 Project-URL: Code, https://github.com/BSaaber/fastfft
@@ -31,10 +31,16 @@
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Requires-Python: >=3.4
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE.txt
 
-# Just a regular readme file
-
-This is package with fft algorithm implementation.
+# FASTFFT
+import
+```
+from fastfft.fft import fft2
+```
+use
+```
+fft([[1, 2], [3, 4]])
+```
```

