# Comparing `tmp/squander-1.7.4.tar.gz` & `tmp/squander-1.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "squander-1.7.4.tar", last modified: Tue Feb 14 20:05:00 2023, max compression
+gzip compressed data, was "squander-1.8.0.tar", last modified: Sat May 13 12:18:39 2023, max compression
```

## Comparing `squander-1.7.4.tar` & `squander-1.8.0.tar`

### file list

```diff
@@ -1,174 +1,188 @@
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    15607 2023-02-14 20:03:12.000000 squander-1.7.4/CMakeLists.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    35149 2023-02-14 20:03:12.000000 squander-1.7.4/LICENSE
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)      121 2023-02-14 20:03:12.000000 squander-1.7.4/MANIFEST.in
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    14139 2023-02-14 20:05:00.470859 squander-1.7.4/PKG-INFO
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    13599 2023-02-14 20:03:12.000000 squander-1.7.4/README.md
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.454858 squander-1.7.4/cmake/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4306 2023-02-14 20:03:12.000000 squander-1.7.4/cmake/check_AVX.cmake
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.454858 squander-1.7.4/common/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6776 2023-02-14 20:03:12.000000 squander-1.7.4/common/Adam.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8316 2023-02-14 20:03:12.000000 squander-1.7.4/common/common.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5246 2023-02-14 20:03:12.000000 squander-1.7.4/common/common_DFE.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    14292 2023-02-14 20:03:12.000000 squander-1.7.4/common/dot.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.454858 squander-1.7.4/common/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3441 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/Adam.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)      216 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/Config.h.in
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2109 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/QGDTypes.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5293 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/common.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3009 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/common_DFE.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7626 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/dot.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2443 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/logging.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3812 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/matrix.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    13483 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/matrix_base.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3746 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/matrix_real.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1393 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/mpi_base.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1468 2023-02-14 20:03:12.000000 squander-1.7.4/common/include/numpy_interface.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2515 2023-02-14 20:03:12.000000 squander-1.7.4/common/logging.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5063 2023-02-14 20:03:12.000000 squander-1.7.4/common/matrix.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4489 2023-02-14 20:03:12.000000 squander-1.7.4/common/matrix_real.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1095 2023-02-14 20:03:12.000000 squander-1.7.4/common/mpi_base.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4808 2023-02-14 20:03:12.000000 squander-1.7.4/common/numpy_interface.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.458859 squander-1.7.4/decomposition/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    57025 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/Decomposition_Base.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    36916 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/N_Qubit_Decomposition.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    50283 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/N_Qubit_Decomposition_Base.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     9141 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/N_Qubit_Decomposition_Cost_Function.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    57633 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/N_Qubit_Decomposition_adaptive.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    12662 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/N_Qubit_Decomposition_custom.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    24591 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/Sub_Matrix_Decomposition.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8536 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/Sub_Matrix_Decomposition_Cost_Function.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.458859 squander-1.7.4/decomposition/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    15881 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/Decomposition_Base.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7119 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/N_Qubit_Decomposition.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    11864 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/N_Qubit_Decomposition_Base.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3381 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/N_Qubit_Decomposition_Cost_Function.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7424 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/N_Qubit_Decomposition_adaptive.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3346 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/N_Qubit_Decomposition_custom.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6810 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/Sub_Matrix_Decomposition.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3723 2023-02-14 20:03:12.000000 squander-1.7.4/decomposition/include/Sub_Matrix_Decomposition_Cost_Function.h
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/gates/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5728 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Adaptive.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4900 2023-02-14 20:03:12.000000 squander-1.7.4/gates/CH.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4937 2023-02-14 20:03:12.000000 squander-1.7.4/gates/CNOT.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5839 2023-02-14 20:03:12.000000 squander-1.7.4/gates/CRY.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4841 2023-02-14 20:03:12.000000 squander-1.7.4/gates/CZ.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7781 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Composite.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    10781 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Gate.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)   132499 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Gates_block.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8547 2023-02-14 20:03:12.000000 squander-1.7.4/gates/ON.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6819 2023-02-14 20:03:12.000000 squander-1.7.4/gates/RX.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6815 2023-02-14 20:03:12.000000 squander-1.7.4/gates/RY.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7110 2023-02-14 20:03:12.000000 squander-1.7.4/gates/RZ.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8697 2023-02-14 20:03:12.000000 squander-1.7.4/gates/SX.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     9587 2023-02-14 20:03:12.000000 squander-1.7.4/gates/SYC.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    15472 2023-02-14 20:03:12.000000 squander-1.7.4/gates/U3.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8769 2023-02-14 20:03:12.000000 squander-1.7.4/gates/UN.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7950 2023-02-14 20:03:12.000000 squander-1.7.4/gates/X.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5671 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Y.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5672 2023-02-14 20:03:12.000000 squander-1.7.4/gates/Z.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/gates/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3395 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Adaptive.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2428 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/CH.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2456 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/CNOT.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3097 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/CRY.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2427 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/CZ.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3594 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Composite.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5089 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Gate.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    15484 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Gates_block.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3412 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/ON.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2812 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/RX.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3080 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/RY.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2808 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/RZ.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2783 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/SX.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2428 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/SYC.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5985 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/U3.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     3412 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/UN.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2774 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/X.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2772 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Y.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2772 2023-02-14 20:03:12.000000 squander-1.7.4/gates/include/Z.h
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/gates/kernels/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     8113 2023-02-14 20:03:12.000000 squander-1.7.4/gates/kernels/apply_kernel_to_input_AVX.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/gates/kernels/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1182 2023-02-14 20:03:12.000000 squander-1.7.4/gates/kernels/include/apply_kernel_to_input_AVX.h
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/nn/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    18366 2023-02-14 20:03:12.000000 squander-1.7.4/nn/NN.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/nn/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5274 2023-02-14 20:03:12.000000 squander-1.7.4/nn/include/NN.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)      123 2023-02-14 20:03:12.000000 squander-1.7.4/pyproject.toml
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.462859 squander-1.7.4/qgd_python/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       27 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/__init__.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.466859 squander-1.7.4/qgd_python/decomposition/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4386 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/CMakeLists.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       27 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/__init__.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7661 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    36479 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_Wrapper.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    20874 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    65768 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive_Wrapper.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    14004 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    39286 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom_Wrapper.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.466859 squander-1.7.4/qgd_python/decomposition/test/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/__init__.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1982 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_Global_Phase.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5317 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_IBM.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1832 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_Project_Name.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     5742 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_QX2.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1710 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_Unitary.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4855 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_decomposition.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7461 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_fmo.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7193 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_heavy_hex.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4984 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/decomposition/test/test_parametric_circuit.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.466859 squander-1.7.4/qgd_python/gates/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    13547 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/CMakeLists.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/__init__.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6816 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_CH.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6756 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_CNOT.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6634 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_CZ.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    26458 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_Gates_Block.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6928 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_RX.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6927 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_RY.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6928 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_RZ.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6370 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_SX.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6700 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_SYC.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     9005 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_U3.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7364 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_X.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7974 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_Y.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     7975 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/qgd_Z.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/qgd_python/gates/test/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/__init__.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1614 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_CH.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1758 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_CNOT.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1713 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_CZ.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1633 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_RX.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1632 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_RY.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1756 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_RZ.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1612 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_SX.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1896 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_U3.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1608 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_X.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6878 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/gates/test/test_gates.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/qgd_python/nn/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1304 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/nn/CMakeLists.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       27 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/nn/__init__.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     2387 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/nn/qgd_nn.py
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     9635 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/nn/qgd_nn_Wrapper.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1573 2023-02-14 20:03:12.000000 squander-1.7.4/qgd_python/utils.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/random_unitary/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6628 2023-02-14 20:03:12.000000 squander-1.7.4/random_unitary/Random_Orthogonal.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    11039 2023-02-14 20:03:12.000000 squander-1.7.4/random_unitary/Random_Unitary.cpp
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/random_unitary/include/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1927 2023-02-14 20:03:12.000000 squander-1.7.4/random_unitary/include/Random_Orthogonal.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4476 2023-02-14 20:03:12.000000 squander-1.7.4/random_unitary/include/Random_Unitary.h
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       38 2023-02-14 20:05:00.470859 squander-1.7.4/setup.cfg
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1850 2023-02-14 20:03:47.000000 squander-1.7.4/setup.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/squander/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1249 2023-02-14 20:03:12.000000 squander-1.7.4/squander/__init__.py
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/squander.egg-info/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)    14139 2023-02-14 20:05:00.000000 squander-1.7.4/squander.egg-info/PKG-INFO
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4493 2023-02-14 20:05:00.000000 squander-1.7.4/squander.egg-info/SOURCES.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)        1 2023-02-14 20:05:00.000000 squander-1.7.4/squander.egg-info/dependency_links.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       50 2023-02-14 20:05:00.000000 squander-1.7.4/squander.egg-info/requires.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)       20 2023-02-14 20:05:00.000000 squander-1.7.4/squander.egg-info/top_level.txt
-drwxrwxr-x   0 rakytap   (1002) rakytap   (1002)        0 2023-02-14 20:05:00.470859 squander-1.7.4/test_standalone/
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     1996 2023-02-14 20:03:12.000000 squander-1.7.4/test_standalone/CMakeLists.txt
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     6325 2023-02-14 20:03:12.000000 squander-1.7.4/test_standalone/custom_gate_structure_test.cpp
--rw-rw-r--   0 rakytap   (1002) rakytap   (1002)     4837 2023-02-14 20:03:12.000000 squander-1.7.4/test_standalone/decomposition_test.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    15910 2023-05-13 12:17:13.000000 squander-1.8.0/CMakeLists.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    35149 2023-05-13 12:17:13.000000 squander-1.8.0/LICENSE
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)      121 2023-05-13 12:17:13.000000 squander-1.8.0/MANIFEST.in
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    17824 2023-05-13 12:18:39.478572 squander-1.8.0/PKG-INFO
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    17284 2023-05-13 12:17:13.000000 squander-1.8.0/README.md
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.462572 squander-1.8.0/cmake/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4306 2023-05-13 12:17:13.000000 squander-1.8.0/cmake/check_AVX.cmake
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.466572 squander-1.8.0/common/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6776 2023-05-13 12:17:13.000000 squander-1.8.0/common/Adam.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8316 2023-05-13 12:17:13.000000 squander-1.8.0/common/common.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5293 2023-05-13 12:17:13.000000 squander-1.8.0/common/common_DFE.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5524 2023-05-13 12:17:13.000000 squander-1.8.0/common/config_element.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    14292 2023-05-13 12:17:13.000000 squander-1.8.0/common/dot.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.466572 squander-1.8.0/common/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3441 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/Adam.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)      216 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/Config.h.in
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2109 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/QGDTypes.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5293 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/common.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3026 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/common_DFE.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3423 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/config_element.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7626 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/dot.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2443 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/logging.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3812 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/matrix.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    13485 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/matrix_base.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3746 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/matrix_real.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1393 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/mpi_base.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1468 2023-05-13 12:17:13.000000 squander-1.8.0/common/include/numpy_interface.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2515 2023-05-13 12:17:13.000000 squander-1.8.0/common/logging.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5065 2023-05-13 12:17:13.000000 squander-1.8.0/common/matrix.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4491 2023-05-13 12:17:13.000000 squander-1.8.0/common/matrix_real.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1095 2023-05-13 12:17:13.000000 squander-1.8.0/common/mpi_base.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4808 2023-05-13 12:17:13.000000 squander-1.8.0/common/numpy_interface.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.466572 squander-1.8.0/decomposition/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    57993 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/Decomposition_Base.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    37081 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/N_Qubit_Decomposition.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)   111147 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/N_Qubit_Decomposition_Base.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    16714 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/N_Qubit_Decomposition_Cost_Function.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    77244 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/N_Qubit_Decomposition_adaptive.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    12741 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/N_Qubit_Decomposition_custom.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    24660 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/Sub_Matrix_Decomposition.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8536 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/Sub_Matrix_Decomposition_Cost_Function.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.466572 squander-1.8.0/decomposition/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    16087 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/Decomposition_Base.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7166 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/N_Qubit_Decomposition.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    16028 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/N_Qubit_Decomposition_Base.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5077 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/N_Qubit_Decomposition_Cost_Function.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8301 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/N_Qubit_Decomposition_adaptive.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3393 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/N_Qubit_Decomposition_custom.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6860 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/Sub_Matrix_Decomposition.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3723 2023-05-13 12:17:13.000000 squander-1.8.0/decomposition/include/Sub_Matrix_Decomposition_Cost_Function.h
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/gates/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5728 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Adaptive.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4900 2023-05-13 12:17:13.000000 squander-1.8.0/gates/CH.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4937 2023-05-13 12:17:13.000000 squander-1.8.0/gates/CNOT.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5839 2023-05-13 12:17:13.000000 squander-1.8.0/gates/CRY.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4841 2023-05-13 12:17:13.000000 squander-1.8.0/gates/CZ.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7781 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Composite.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    11545 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Gate.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)   120998 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Gates_block.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8547 2023-05-13 12:17:13.000000 squander-1.8.0/gates/ON.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6819 2023-05-13 12:17:13.000000 squander-1.8.0/gates/RX.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6815 2023-05-13 12:17:13.000000 squander-1.8.0/gates/RY.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7110 2023-05-13 12:17:13.000000 squander-1.8.0/gates/RZ.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8697 2023-05-13 12:17:13.000000 squander-1.8.0/gates/SX.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     9587 2023-05-13 12:17:13.000000 squander-1.8.0/gates/SYC.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    15472 2023-05-13 12:17:13.000000 squander-1.8.0/gates/U3.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8769 2023-05-13 12:17:13.000000 squander-1.8.0/gates/UN.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7950 2023-05-13 12:17:13.000000 squander-1.8.0/gates/X.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5671 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Y.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5672 2023-05-13 12:17:13.000000 squander-1.8.0/gates/Z.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/gates/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3395 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Adaptive.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2428 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/CH.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2504 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/CNOT.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3113 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/CRY.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2427 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/CZ.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3594 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Composite.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5097 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Gate.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    15824 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Gates_block.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3412 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/ON.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2812 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/RX.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3088 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/RY.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2808 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/RZ.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2783 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/SX.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2428 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/SYC.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6017 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/U3.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3412 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/UN.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2774 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/X.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2772 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Y.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2772 2023-05-13 12:17:13.000000 squander-1.8.0/gates/include/Z.h
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/gates/kernels/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    23561 2023-05-13 12:17:13.000000 squander-1.8.0/gates/kernels/apply_kernel_to_input_AVX.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    32382 2023-05-13 12:17:13.000000 squander-1.8.0/gates/kernels/apply_kernel_to_state_vector_input.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/gates/kernels/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1786 2023-05-13 12:17:13.000000 squander-1.8.0/gates/kernels/include/apply_kernel_to_input_AVX.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2099 2023-05-13 12:17:13.000000 squander-1.8.0/gates/kernels/include/apply_kernel_to_state_vector_input.h
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/nn/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    18464 2023-05-13 12:17:13.000000 squander-1.8.0/nn/NN.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.470572 squander-1.8.0/nn/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5274 2023-05-13 12:17:13.000000 squander-1.8.0/nn/include/NN.h
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.474572 squander-1.8.0/optimization_engines/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     9698 2023-05-13 12:17:13.000000 squander-1.8.0/optimization_engines/RL_experience.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.474572 squander-1.8.0/optimization_engines/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3549 2023-05-13 12:17:13.000000 squander-1.8.0/optimization_engines/include/RL_experience.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)      123 2023-05-13 12:17:13.000000 squander-1.8.0/pyproject.toml
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.474572 squander-1.8.0/qgd_python/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       27 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/__init__.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.474572 squander-1.8.0/qgd_python/decomposition/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4386 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/CMakeLists.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       27 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/__init__.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7661 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    36730 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_Wrapper.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    24494 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    80282 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive_Wrapper.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    14278 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    41007 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom_Wrapper.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3367 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_State_Preparation_adaptive.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.474572 squander-1.8.0/qgd_python/decomposition/test/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/__init__.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    11024 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_Compression.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1927 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_Global_Phase.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7037 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_IBM.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1777 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_Project_Name.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5616 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_QX2.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4399 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_State_Preparation.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1656 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_Unitary.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4672 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_decomposition.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7190 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_fmo.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7018 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_heavy_hex.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5222 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_optmization_problem_combined.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4905 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/decomposition/test/test_parametric_circuit.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/qgd_python/gates/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    13547 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/CMakeLists.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/__init__.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8219 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_CH.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8160 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_CNOT.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8033 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_CZ.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    28536 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_Gates_Block.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8529 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_RX.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8528 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_RY.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8527 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_RZ.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7771 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_SX.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7801 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_SYC.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     9054 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_U3.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     7489 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_X.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8367 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_Y.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     8367 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/qgd_Z.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/qgd_python/gates/test/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/__init__.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3364 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_CH.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3409 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_CNOT.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3444 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_CZ.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3466 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_RX.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3348 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_RY.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3919 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_RZ.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3278 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_SX.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3676 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_U3.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3182 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_X.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3179 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_Y.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     3232 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_Z.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6878 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/gates/test/test_gates.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/qgd_python/nn/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1304 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/nn/CMakeLists.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       27 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/nn/__init__.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     2387 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/nn/qgd_nn.py
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     9635 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/nn/qgd_nn_Wrapper.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1573 2023-05-13 12:17:13.000000 squander-1.8.0/qgd_python/utils.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/random_unitary/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6628 2023-05-13 12:17:13.000000 squander-1.8.0/random_unitary/Random_Orthogonal.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    11039 2023-05-13 12:17:13.000000 squander-1.8.0/random_unitary/Random_Unitary.cpp
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/random_unitary/include/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1927 2023-05-13 12:17:13.000000 squander-1.8.0/random_unitary/include/Random_Orthogonal.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4476 2023-05-13 12:17:13.000000 squander-1.8.0/random_unitary/include/Random_Unitary.h
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       38 2023-05-13 12:18:39.478572 squander-1.8.0/setup.cfg
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1850 2023-05-13 12:17:13.000000 squander-1.8.0/setup.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/squander/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1442 2023-05-13 12:17:13.000000 squander-1.8.0/squander/__init__.py
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/squander.egg-info/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)    17824 2023-05-13 12:18:39.000000 squander-1.8.0/squander.egg-info/PKG-INFO
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     5051 2023-05-13 12:18:39.000000 squander-1.8.0/squander.egg-info/SOURCES.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)        1 2023-05-13 12:18:39.000000 squander-1.8.0/squander.egg-info/dependency_links.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       50 2023-05-13 12:18:39.000000 squander-1.8.0/squander.egg-info/requires.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)       20 2023-05-13 12:18:39.000000 squander-1.8.0/squander.egg-info/top_level.txt
+drwxrwxr-x   0 rakytap   (1000) rakytap   (1000)        0 2023-05-13 12:18:39.478572 squander-1.8.0/test_standalone/
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     1996 2023-05-13 12:17:13.000000 squander-1.8.0/test_standalone/CMakeLists.txt
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     6325 2023-05-13 12:17:13.000000 squander-1.8.0/test_standalone/custom_gate_structure_test.cpp
+-rw-rw-r--   0 rakytap   (1000) rakytap   (1000)     4837 2023-05-13 12:17:13.000000 squander-1.8.0/test_standalone/decomposition_test.cpp
```

### Comparing `squander-1.7.4/CMakeLists.txt` & `squander-1.8.0/CMakeLists.txt`

 * *Files 1% similar despite different names*

```diff
@@ -181,37 +181,37 @@
 elseif (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
   # using GCC
   message("-- Using GNU compiler")
   list(APPEND CXX_FLAGS_DEBUG "-g3" "-ggdb")
   list(APPEND CXX_FLAGS_RELEASE "-ftree-vectorize")
 
   if (${HAVE_AVX512F_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx512f" "-DUSE_AVX")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx512f" "-mfma" "-DUSE_AVX")
   elseif (${HAVE_AVX2_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx2" "-DUSE_AVX")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx2" "-mfma" "-DUSE_AVX")
     list(APPEND EXTRA_INCLUDES "./gates/kernels/include/")
   elseif (${HAVE_AVX_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx" "-DUSE_AVX")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx" "-mfma" "-DUSE_AVX")
   endif()
 
 
 elseif (CMAKE_CXX_COMPILER_ID STREQUAL "Intel")
   # using Intel C++
   message("-- Using Intel compiler")
   if (BLAS_IS_MKL)
     list(APPEND CXX_FLAGS_DEBUG "-mkl" "-tbb")
     list(APPEND CXX_FLAGS_RELEASE "-mkl" "-tbb")
   endif()
 
   if (${HAVE_AVX512F_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx512f" "-DUSE_AVX512F")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx512f" "-mfma" "-DUSE_AVX512F")
   elseif (${HAVE_AVX2_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx2" "-DUSE_AVX")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx2" "-mfma" "-DUSE_AVX")
   elseif (${HAVE_AVX_EXTENSIONS})
-    list(APPEND CXX_FLAGS_RELEASE "-mavx" "-DUSE_AVX")
+    list(APPEND CXX_FLAGS_RELEASE "-mavx" "-mfma" "-DUSE_AVX")
   endif()
 
 elseif (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
   # using Visual Studio C++
   message("-- Using Visual Studio C++ compiler")
 
   if (${HAVE_AVX512F_EXTENSIONS})
@@ -339,19 +339,21 @@
 
 
 endif()
 
 
 list(APPEND qgd_files 
     ${PROJECT_SOURCE_DIR}/common/common.cpp
+    ${PROJECT_SOURCE_DIR}/common/config_element.cpp
     ${PROJECT_SOURCE_DIR}/common/dot.cpp
     ${PROJECT_SOURCE_DIR}/common/matrix.cpp
     ${PROJECT_SOURCE_DIR}/common/matrix_real.cpp
     ${PROJECT_SOURCE_DIR}/common/logging.cpp
     ${PROJECT_SOURCE_DIR}/common/Adam.cpp
+    ${PROJECT_SOURCE_DIR}/optimization_engines/RL_experience.cpp
     ${PROJECT_SOURCE_DIR}/gates/CNOT.cpp
     ${PROJECT_SOURCE_DIR}/gates/SYC.cpp
     ${PROJECT_SOURCE_DIR}/gates/CZ.cpp
     ${PROJECT_SOURCE_DIR}/gates/CH.cpp
     ${PROJECT_SOURCE_DIR}/gates/Gate.cpp
     ${PROJECT_SOURCE_DIR}/gates/UN.cpp
     ${PROJECT_SOURCE_DIR}/gates/ON.cpp
@@ -364,14 +366,15 @@
     ${PROJECT_SOURCE_DIR}/gates/RY.cpp
     ${PROJECT_SOURCE_DIR}/gates/CRY.cpp
     ${PROJECT_SOURCE_DIR}/gates/Adaptive.cpp
     ${PROJECT_SOURCE_DIR}/gates/RX.cpp
     ${PROJECT_SOURCE_DIR}/gates/RZ.cpp
     ${PROJECT_SOURCE_DIR}/gates/Composite.cpp
     ${PROJECT_SOURCE_DIR}/gates/kernels/apply_kernel_to_input_AVX.cpp
+    ${PROJECT_SOURCE_DIR}/gates/kernels/apply_kernel_to_state_vector_input.cpp
     ${PROJECT_SOURCE_DIR}/nn/NN.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/Decomposition_Base.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/N_Qubit_Decomposition_Base.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/N_Qubit_Decomposition.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/N_Qubit_Decomposition_adaptive.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/N_Qubit_Decomposition_custom.cpp
     ${PROJECT_SOURCE_DIR}/decomposition/N_Qubit_Decomposition_Cost_Function.cpp
@@ -430,14 +433,15 @@
 
 target_include_directories(qgd PRIVATE
                             .
                             ./common/include
                             ./gates/include
                             ./decomposition/include
                             ./random_unitary/include
+                            ./optimization_engines/include
                             ./nn/include
                             ./gates/kernels/include
                             ${EXTRA_INCLUDES})
 
 
 
 set_target_properties(qgd PROPERTIES
```

### Comparing `squander-1.7.4/LICENSE` & `squander-1.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/PKG-INFO` & `squander-1.8.0/README.md`

 * *Files 13% similar despite different names*

```diff
@@ -1,23 +1,7 @@
-Metadata-Version: 2.1
-Name: squander
-Version: 1.7.4
-Summary: The C++ binding for the SQUANDER package
-Home-page: https://github.com/rakytap/sequential-quantum-gate-decomposer
-Maintainer: Peter Rakyta
-Maintainer-email: peter.rakyta@ttk.elte.hu
-License: GNU General Public License v3.0
-Keywords: test,cmake,extension
-Classifier: Intended Audience :: Developers
-Classifier: Natural Language :: English
-Classifier: Programming Language :: C
-Classifier: Programming Language :: C++
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)](https://doi.org/10.5281/zenodo.4508680)
  <a href="https://trackgit.com">
 <img src="https://us-central1-trackgit-analytics.cloudfunctions.net/token/ping/l0sfey1m19at85951dwl" alt="trackgit-views" />
 </a>
 
 # Sequential Quantum Gate Decomposer (SQUANDER)
 
@@ -224,16 +208,99 @@
 Thus, in order to get the decomposition of a unitary, one should rather provide the complex transpose of this unitary as the input for the SQUANDER decomposing process, as can be seen in the examples.
 
 
 ## Python Interface
 
 The SQUANDER package contains a Python interface allowing the access of the functionalities of the SQUANDER package from Python. 
 The usage of the SQUANDER Python interface is demonstrated in the example files in the directory **examples** located in the directory **path/to/SQUANDER/package**, or in test files located in sub-directories of **path/to/SQUANDER/package/qgd_python/*/test**. 
-The example files import the necessary **qgd_python** modules containing the wrapper classes to interface with the C++ SQUANDER library. 
-(So the SQUANDER package need to be installed or the compiled package needs to be added to the Python search path.)
+
+### Example code snippet
+
+Here we provide an example to use the SQUANDER package. The following python interface is accessible from version 1.8.0. 
+In this example we use two optimization engines for the decomposition:
+1. An evolutionary engine called AGENTS
+2. Second order gradient descend algorithm (BFGS)
+
+Firstly we construct a Python map to set hyper-parameters during the gate synthesis.
+
+        #Python map containing hyper-parameters
+        config = { 'max_outer_iterations': 1, 
+                    'max_inner_iterations_agent': 25000, 
+                    'max_inner_iterations_compression': 10000,
+                    'max_inner_iterations' : 500,
+                    'max_inner_iterations_final': 5000, 		
+                    'Randomized_Radius': 0.3, 
+                    'randomized_adaptive_layers': 1,
+                    'optimization_tolerance_agent': 1e-4,
+                    'optimization_tolerance': 1e-8,
+                    'agent_num': 10}
+ 
+Next we initialize the decomposition class with the unitary Umtx to be decomposed. 
+
+        # creating a class to decompose the unitary
+        from squander import N_Qubit_Decomposition_adaptive
+        cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config )
+
+The verbosity of the execution output can be controlled by the function call 
+
+        # setting the verbosity of the decomposition
+        cDecompose.set_Verbose( 3 )
+
+
+We construct the initial trial gate structure for the optimization consisting of 2 levels of adaptive layer. 
+(1 level is made of qubit_num*(qubit_num-1) two-qubit building blocks if all-to-all connectivity is assumed)
+
+
+        # adding decomposing layers to the gate structure
+        levels = 2
+        for idx in range(levels):
+            cDecompose.add_Adaptive_Layers()
+
+        cDecompose.add_Finalyzing_Layer_To_Gate_Structure()
+        
+We can construct an initial parameters set for the optimization by retrieving the number of free parameters. If the initial parameter set is not set, random parameters are used by default.
+
+        # setting intial parameter set
+        parameter_num = cDecompose.get_Parameter_Num()
+        parameters = np.zeros( (parameter_num,1), dtype=np.float64 )
+        cDecompose.set_Optimized_Parameters( parameters )
+
+We can use between several engines to solve the optimization problem. Here we use an evolutionary based algorithm named 'AGENTS'
+
+        # setting optimizer
+        cDecompose.set_Optimizer("AGENTS")
+	
+The optimization process is started by the function call	
+
+        # starting the decomposition
+        cDecompose.get_Initial_Circuit()
+	
+The optimization process terminates by either reaching the tolerance 'optimization_tolerance_agent' or by reaching the maximal iteration number 'max_inner_iterations_agent', or if the engines identifies a convergence to a local minimum. The SQUANDER framework enables one to continue the optimization using a different engine. In particular we set a second order gradient descend method 'BFGS' 
+
+        # setting optimizer
+        cDecompose.set_Optimizer("BFGS")
+
+        # continue the decomposition with a second optimizer method
+        cDecompose.get_Initial_Circuit()
+	
+After solving the optimization problem for the initial gate structure, we can initiate gate compression iterations. (This step can be omited.)	
+
+        # starting compression iterations
+        cDecompose.Compress_Circuit()
+	
+By finalizing the gate structure we replace the CRY gates with CNOT gates. (CRY gates with small rotation angle are approximately expressed with a single CNOT gate, so further optimization process needs to be initiated.)
+
+        # finalize the gate structure (replace CRY gates with CNOT gates)
+        cDecompose.Finalize_Circuit()
+
+Finally, we can retrieve the decomposed quantum circuit in QISKIT format.
+
+        # get the decomposing operations
+        quantum_circuit = cDecompose.get_Quantum_Circuit()
+
 
 
 ### How to cite us
 
 If you have found our work useful for your research project, please cite us by
 
 [1] Péter Rakyta, Zoltán Zimborás, Approaching the theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022). <br>
```

#### html2text {}

```diff
@@ -1,127 +1,120 @@
-Metadata-Version: 2.1 Name: squander Version: 1.7.4 Summary: The C++ binding
-for the SQUANDER package Home-page: https://github.com/rakytap/sequential-
-quantum-gate-decomposer Maintainer: Peter Rakyta Maintainer-email:
-peter.rakyta@ttk.elte.hu License: GNU General Public License v3.0 Keywords:
-test,cmake,extension Classifier: Intended Audience :: Developers Classifier:
-Natural Language :: English Classifier: Programming Language :: C Classifier:
-Programming Language :: C++ Description-Content-Type: text/markdown License-
-File: LICENSE [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)]
-(https://doi.org/10.5281/zenodo.4508680) [trackgit-views] # Sequential Quantum
-Gate Decomposer (SQUANDER) The Sequential Quantum Gate Decomposer (SQUANDER)
-package provides a novel solution to decompose any n-qubit unitaries into a
-sequence of one-qubit rotations and two-qubit controlled gates (such as
-controlled NOT or controlled phase gate). SQUANDER utilizes two novel gate
-synthesis techniques reported in Refereces [1] and [2]. (i) To synthesize
-general unitaries SQUANDER applies periodic layers of two-qubit and parametric
-one-qubit gates to an n-qubit unitary such that the resulting unitary is 1-
-qubit decoupled, i.e., is a tensor product of an (n-1)-qubit and a 1-qubit
-unitary. Continuing the decoupling procedure sequentially one arrives at the
-end to a full decomposition of the original unitary into 1- and 2-qubit gates.
-SQUANDER provides lower CNOT counts for generic n-qubit unitaries (up to n=6)
-than the previously provided lower bounds. (ii) An adaptive circuit compression
-is used to optimize quantum circuit by the application of parametric two-qubit
-gates in the synthesis process. The utilization of these parametric two-qubit
-gates in the circuit design allows one to transform the discrete combinatorial
-problem of circuit synthesis into an optimization problem over continuous
-variables. The circuit is then compressed by a sequential removal of two-qubit
-gates from the design, while the remaining building blocks are continuously
-adapted to the reduced gate structure by iterated learning cycles. The SQUANDER
-library is written in C/C++ providing a Python interface via [C++ extensions]
-(https://docs.python.org/3/library/ctypes.html). The present package is
-supplied with Python building script and CMake tools to ease its deployment.
-The SQUANDER package can be built with both Intel and GNU compilers, and can be
-link against various CBLAS libraries installed on the system. (So far the CLBAS
-libraries of the GNU Scientific Library, OpenBLAS and the Intel MKL packages
-were tested.) In the following we briefly summarize the steps to build, install
-and use the SQUANDER package. The project was supported by grant OTKA PD123927
-and by the Ministry of Innovation and Technology and the National Research,
-Development and Innovation Office within the Quantum Information National
-Laboratory of Hungary. Find the documantation of the SQUANDER package at
-[CodeDocs[xyz]](https://codedocs.xyz/rakytap/sequential-quantum-gate-
-decomposer/) ### Contact Us Have a question about the SQUANDER package? Don't
-hesitate to contact us at the following e-mails: * ZoltÃ¡n ZimborÃ¡s
-(researcher): zimboras.zoltan@wigner.hu * Peter Rakyta (developer):
-peter.rakyta@ttk.elte.hu ### Dependencies The optimization algorithm of
-SQUANDER relies on the [multimin](https://www.gnu.org/software/gsl/doc/html/
-multimin.html) component of the [GNU Scientific Library](https://www.gnu.org/
-software/gsl/doc/html/index.html). We developed and tested the SQUANDER package
-with GNU Scientific Library of version 2.5, 2.6 and 2.7. The dependencies
-necessary to compile and build the SQUANDER package are the followings: *
-[CMake](https://cmake.org/) (>=3.10.2) * [GNU Scientific Library](https://
-www.gnu.org/software/gsl/doc/html/index.html) (>=2.5, shipped with the gsl
-python package) * C++/C [Intel](https://software.intel.com/content/www/us/en/
-develop/tools/compilers/c-compilers.html) (>=14.0.1) or [GNU](https://
-gcc.gnu.org/) (>=v4.8.1) compiler * [TBB](https://github.com/oneapi-src/oneTBB)
-library (shipped with tbb-devel Python package) * [Intel MKL](https://
-software.intel.com/content/www/us/en/develop/tools/math-kernel-library.html)
-(optional) * [OpenBlas](https://www.openblas.net/) (optional, recommended) *
-[LAPACKE](https://www.netlib.org/lapack/lapacke.html) * [Doxygen](https://
-www.doxygen.nl/index.html) (optional) The Python interface of SQUANDER was
-developed and tested with Python 3.6-3.9. The SQUANDER Python interface needs
-the following packages to be installed on the system: * [Qiskit](https://
-qiskit.org/documentation/install.html) * [Numpy](https://numpy.org/install/) *
-[scipy](https://www.scipy.org/install.html) * [scikit-build](https://scikit-
-build.readthedocs.io/en/latest/) * [tbb-devel](https://pypi.org/project/tbb-
-devel/) (containing the TBB Library) * [gsl](https://anaconda.org/conda-forge/
-gsl) (containing the GNU Scientific Library) ### How to obtain GNU Scientific
-Library In order to build and use the SQUANDER we recommend the Anaconda
-virtual python environment providing all the required dependencies for
-SQUANDER. One can easily install the GNU Scientific Library for local users by
-the command $ conda install -c conda-forge gsl Alternatively, a python binding
-project alongside the GNU GSL library is accessible via pypi repository: $ pip
-install numpy swig $ pip install pygsl Here we describe an alternative way to
-deploy GNU Scientific Library from source by the end user without
-administrative privileges. The GNU Scientific Library can be downloaded from
-the site [https://www.gnu.org/software/gsl/](https://www.gnu.org/software/gsl/
-). After the downloaded package is extracted somewhere in the home directory of
-the user (**path/to/gsl/source**), one should configure the building
-environment using the **configure** tool. Depending on the individual settings
-the default compiler to be invoked might be different from HPC to HPC. To
-ensure the usage of the GNU compiler, the following shell command should be
-executed inside the directory **path/to/gsl/source**: $ ./configure --
-prefix=path/to/gsl FC=gfortran CC=gcc CXX=g++ (Similarly, Intel compiler can be
-forced by setting FC=ifort CC=icc and CXX=icpc.) The installation directory of
-the compiled GNU Scientific Library is given by **--prefix=path/to/gsl** (which
-is different from the directory path of the source files given by **path/to/
-gslsource**). To install GNU Scientific Library the user should have read and
-write permissions on the path **path/to/gsl** (which might be for example /
-home/username/gsl). After the successful configuration the GNU Scientific
-Library can be compiled by the shell command $ make The compilation of the GNU
-Scientific Library takes some time. When the compilation is done, the package
-(including the C header files and the static and shared libraries) is installed
-into the directory **path/to/gsl** by the shell command: $ make install ###
-Install SQUANDER from Python Package Index (PyPI) Since version 1.7.1 the
-SQUANDER package is accessible at Python Package Index (PyPI). The package can
-be installed on linux systems following the steps outlined below: $ pip install
-numpy swig tbb-devel wheel scikit-build ninja qiskit $ pip install pygsl $ pip
-install squander ### Download the SQUANDER package The developer version of the
-Quantum Gate Decomposer package can be downloaded from github repository
-[https://github.com/rakytap/quantum-gate-decomposer/tree/master](https://
-github.com/rakytap/quantum-gate-decomposer/tree/master). After the package is
-downloaded into the directory **path/to/SQUANDER/package** (which would be the
-path to the source code of the SQUANDER package), one can proceed to the
-compilation steps described in the next section. ### How to build the SQUANDER
-package The SQUANDER package is equipped with a Python build script and CMake
-tools to ease the compilation and the deployment of the package. To ensure that
-SQUANDER package would find the necessary libraries and header files during
-compilation time it is advised to define the following environment variables: $
-export GSL_LIB_DIR=path/to/gsl/lib(64) $ export GSL_INC_DIR=path/to/gsl/include
-The SQUANDER package is parallelized via Threading Building Block (TBB)
-libraries. If TBB is not present in the system, it can be easily installed via
-python package [tbb-devel](https://pypi.org/project/tbb-devel/). Alternatively
-the TBB libraries can be installed via apt or yum utility (sudo apt install
-libtbb-dev) or it can be downloaded from [https://github.com/oneapi-src/oneTBB]
-(https://github.com/oneapi-src/oneTBB) and built from source. In this case one
-should supply the necessary environment variables pointing to the header and
-library files of the TBB package. For newer Intel compilers the TBB package is
-part of the Intel compiler package, similarly to the MKL package. If the TBB
-library is located at non-standrad path or the SQUANDER package is compiled
-with GNU compiler, then setting the $ export TBB_LIB_DIR=path/to/TBB/lib(64) $
-export TBB_INC_DIR=path/to/TBB/include environment variables are sufficient for
+[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)](https://
+doi.org/10.5281/zenodo.4508680) [trackgit-views] # Sequential Quantum Gate
+Decomposer (SQUANDER) The Sequential Quantum Gate Decomposer (SQUANDER) package
+provides a novel solution to decompose any n-qubit unitaries into a sequence of
+one-qubit rotations and two-qubit controlled gates (such as controlled NOT or
+controlled phase gate). SQUANDER utilizes two novel gate synthesis techniques
+reported in Refereces [1] and [2]. (i) To synthesize general unitaries SQUANDER
+applies periodic layers of two-qubit and parametric one-qubit gates to an n-
+qubit unitary such that the resulting unitary is 1-qubit decoupled, i.e., is a
+tensor product of an (n-1)-qubit and a 1-qubit unitary. Continuing the
+decoupling procedure sequentially one arrives at the end to a full
+decomposition of the original unitary into 1- and 2-qubit gates. SQUANDER
+provides lower CNOT counts for generic n-qubit unitaries (up to n=6) than the
+previously provided lower bounds. (ii) An adaptive circuit compression is used
+to optimize quantum circuit by the application of parametric two-qubit gates in
+the synthesis process. The utilization of these parametric two-qubit gates in
+the circuit design allows one to transform the discrete combinatorial problem
+of circuit synthesis into an optimization problem over continuous variables.
+The circuit is then compressed by a sequential removal of two-qubit gates from
+the design, while the remaining building blocks are continuously adapted to the
+reduced gate structure by iterated learning cycles. The SQUANDER library is
+written in C/C++ providing a Python interface via [C++ extensions](https://
+docs.python.org/3/library/ctypes.html). The present package is supplied with
+Python building script and CMake tools to ease its deployment. The SQUANDER
+package can be built with both Intel and GNU compilers, and can be link against
+various CBLAS libraries installed on the system. (So far the CLBAS libraries of
+the GNU Scientific Library, OpenBLAS and the Intel MKL packages were tested.)
+In the following we briefly summarize the steps to build, install and use the
+SQUANDER package. The project was supported by grant OTKA PD123927 and by the
+Ministry of Innovation and Technology and the National Research, Development
+and Innovation Office within the Quantum Information National Laboratory of
+Hungary. Find the documantation of the SQUANDER package at [CodeDocs[xyz]]
+(https://codedocs.xyz/rakytap/sequential-quantum-gate-decomposer/) ### Contact
+Us Have a question about the SQUANDER package? Don't hesitate to contact us at
+the following e-mails: * ZoltÃ¡n ZimborÃ¡s (researcher):
+zimboras.zoltan@wigner.hu * Peter Rakyta (developer): peter.rakyta@ttk.elte.hu
+### Dependencies The optimization algorithm of SQUANDER relies on the
+[multimin](https://www.gnu.org/software/gsl/doc/html/multimin.html) component
+of the [GNU Scientific Library](https://www.gnu.org/software/gsl/doc/html/
+index.html). We developed and tested the SQUANDER package with GNU Scientific
+Library of version 2.5, 2.6 and 2.7. The dependencies necessary to compile and
+build the SQUANDER package are the followings: * [CMake](https://cmake.org/)
+(>=3.10.2) * [GNU Scientific Library](https://www.gnu.org/software/gsl/doc/
+html/index.html) (>=2.5, shipped with the gsl python package) * C++/C [Intel]
+(https://software.intel.com/content/www/us/en/develop/tools/compilers/c-
+compilers.html) (>=14.0.1) or [GNU](https://gcc.gnu.org/) (>=v4.8.1) compiler *
+[TBB](https://github.com/oneapi-src/oneTBB) library (shipped with tbb-devel
+Python package) * [Intel MKL](https://software.intel.com/content/www/us/en/
+develop/tools/math-kernel-library.html) (optional) * [OpenBlas](https://
+www.openblas.net/) (optional, recommended) * [LAPACKE](https://www.netlib.org/
+lapack/lapacke.html) * [Doxygen](https://www.doxygen.nl/index.html) (optional)
+The Python interface of SQUANDER was developed and tested with Python 3.6-3.9.
+The SQUANDER Python interface needs the following packages to be installed on
+the system: * [Qiskit](https://qiskit.org/documentation/install.html) * [Numpy]
+(https://numpy.org/install/) * [scipy](https://www.scipy.org/install.html) *
+[scikit-build](https://scikit-build.readthedocs.io/en/latest/) * [tbb-devel]
+(https://pypi.org/project/tbb-devel/) (containing the TBB Library) * [gsl]
+(https://anaconda.org/conda-forge/gsl) (containing the GNU Scientific Library)
+### How to obtain GNU Scientific Library In order to build and use the SQUANDER
+we recommend the Anaconda virtual python environment providing all the required
+dependencies for SQUANDER. One can easily install the GNU Scientific Library
+for local users by the command $ conda install -c conda-forge gsl
+Alternatively, a python binding project alongside the GNU GSL library is
+accessible via pypi repository: $ pip install numpy swig $ pip install pygsl
+Here we describe an alternative way to deploy GNU Scientific Library from
+source by the end user without administrative privileges. The GNU Scientific
+Library can be downloaded from the site [https://www.gnu.org/software/gsl/]
+(https://www.gnu.org/software/gsl/). After the downloaded package is extracted
+somewhere in the home directory of the user (**path/to/gsl/source**), one
+should configure the building environment using the **configure** tool.
+Depending on the individual settings the default compiler to be invoked might
+be different from HPC to HPC. To ensure the usage of the GNU compiler, the
+following shell command should be executed inside the directory **path/to/gsl/
+source**: $ ./configure --prefix=path/to/gsl FC=gfortran CC=gcc CXX=g++
+(Similarly, Intel compiler can be forced by setting FC=ifort CC=icc and
+CXX=icpc.) The installation directory of the compiled GNU Scientific Library is
+given by **--prefix=path/to/gsl** (which is different from the directory path
+of the source files given by **path/to/gslsource**). To install GNU Scientific
+Library the user should have read and write permissions on the path **path/to/
+gsl** (which might be for example /home/username/gsl). After the successful
+configuration the GNU Scientific Library can be compiled by the shell command $
+make The compilation of the GNU Scientific Library takes some time. When the
+compilation is done, the package (including the C header files and the static
+and shared libraries) is installed into the directory **path/to/gsl** by the
+shell command: $ make install ### Install SQUANDER from Python Package Index
+(PyPI) Since version 1.7.1 the SQUANDER package is accessible at Python Package
+Index (PyPI). The package can be installed on linux systems following the steps
+outlined below: $ pip install numpy swig tbb-devel wheel scikit-build ninja
+qiskit $ pip install pygsl $ pip install squander ### Download the SQUANDER
+package The developer version of the Quantum Gate Decomposer package can be
+downloaded from github repository [https://github.com/rakytap/quantum-gate-
+decomposer/tree/master](https://github.com/rakytap/quantum-gate-decomposer/
+tree/master). After the package is downloaded into the directory **path/to/
+SQUANDER/package** (which would be the path to the source code of the SQUANDER
+package), one can proceed to the compilation steps described in the next
+section. ### How to build the SQUANDER package The SQUANDER package is equipped
+with a Python build script and CMake tools to ease the compilation and the
+deployment of the package. To ensure that SQUANDER package would find the
+necessary libraries and header files during compilation time it is advised to
+define the following environment variables: $ export GSL_LIB_DIR=path/to/gsl/
+lib(64) $ export GSL_INC_DIR=path/to/gsl/include The SQUANDER package is
+parallelized via Threading Building Block (TBB) libraries. If TBB is not
+present in the system, it can be easily installed via python package [tbb-
+devel](https://pypi.org/project/tbb-devel/). Alternatively the TBB libraries
+can be installed via apt or yum utility (sudo apt install libtbb-dev) or it can
+be downloaded from [https://github.com/oneapi-src/oneTBB](https://github.com/
+oneapi-src/oneTBB) and built from source. In this case one should supply the
+necessary environment variables pointing to the header and library files of the
+TBB package. For newer Intel compilers the TBB package is part of the Intel
+compiler package, similarly to the MKL package. If the TBB library is located
+at non-standrad path or the SQUANDER package is compiled with GNU compiler,
+then setting the $ export TBB_LIB_DIR=path/to/TBB/lib(64) $ export
+TBB_INC_DIR=path/to/TBB/include environment variables are sufficient for
 successful compilation. When the TBB library is installed via a python package,
 setting the environment variables above is not necessary. The SQUANDER package
 with C++ Python extensions can be compiled via the Python script **setup.py**
 located in the root directory of the SQUANDER package. The script automatically
 finds out the CBLAS library working behind the numpy package and uses it in
 further linking. The **setup.py** script also build the C++ library of the
 SQUANDER package by making the appropriate CMake calls. ### Developer build We
@@ -164,19 +157,62 @@
 decomposition of a unitary, one should rather provide the complex transpose of
 this unitary as the input for the SQUANDER decomposing process, as can be seen
 in the examples. ## Python Interface The SQUANDER package contains a Python
 interface allowing the access of the functionalities of the SQUANDER package
 from Python. The usage of the SQUANDER Python interface is demonstrated in the
 example files in the directory **examples** located in the directory **path/to/
 SQUANDER/package**, or in test files located in sub-directories of **path/to/
-SQUANDER/package/qgd_python/*/test**. The example files import the necessary
-**qgd_python** modules containing the wrapper classes to interface with the C++
-SQUANDER library. (So the SQUANDER package need to be installed or the compiled
-package needs to be added to the Python search path.) ### How to cite us If you
-have found our work useful for your research project, please cite us by [1]
-PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the theoretical limit in quantum
-gate decomposition, Quantum 6, 710 (2022).
+SQUANDER/package/qgd_python/*/test**. ### Example code snippet Here we provide
+an example to use the SQUANDER package. The following python interface is
+accessible from version 1.8.0. In this example we use two optimization engines
+for the decomposition: 1. An evolutionary engine called AGENTS 2. Second order
+gradient descend algorithm (BFGS) Firstly we construct a Python map to set
+hyper-parameters during the gate synthesis. #Python map containing hyper-
+parameters config = { 'max_outer_iterations': 1, 'max_inner_iterations_agent':
+25000, 'max_inner_iterations_compression': 10000, 'max_inner_iterations' : 500,
+'max_inner_iterations_final': 5000, 'Randomized_Radius': 0.3,
+'randomized_adaptive_layers': 1, 'optimization_tolerance_agent': 1e-4,
+'optimization_tolerance': 1e-8, 'agent_num': 10} Next we initialize the
+decomposition class with the unitary Umtx to be decomposed. # creating a class
+to decompose the unitary from squander import N_Qubit_Decomposition_adaptive
+cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config ) The
+verbosity of the execution output can be controlled by the function call #
+setting the verbosity of the decomposition cDecompose.set_Verbose( 3 ) We
+construct the initial trial gate structure for the optimization consisting of 2
+levels of adaptive layer. (1 level is made of qubit_num*(qubit_num-1) two-qubit
+building blocks if all-to-all connectivity is assumed) # adding decomposing
+layers to the gate structure levels = 2 for idx in range(levels):
+cDecompose.add_Adaptive_Layers()
+cDecompose.add_Finalyzing_Layer_To_Gate_Structure() We can construct an initial
+parameters set for the optimization by retrieving the number of free
+parameters. If the initial parameter set is not set, random parameters are used
+by default. # setting intial parameter set parameter_num =
+cDecompose.get_Parameter_Num() parameters = np.zeros( (parameter_num,1),
+dtype=np.float64 ) cDecompose.set_Optimized_Parameters( parameters ) We can use
+between several engines to solve the optimization problem. Here we use an
+evolutionary based algorithm named 'AGENTS' # setting optimizer
+cDecompose.set_Optimizer("AGENTS") The optimization process is started by the
+function call # starting the decomposition cDecompose.get_Initial_Circuit() The
+optimization process terminates by either reaching the tolerance
+'optimization_tolerance_agent' or by reaching the maximal iteration number
+'max_inner_iterations_agent', or if the engines identifies a convergence to a
+local minimum. The SQUANDER framework enables one to continue the optimization
+using a different engine. In particular we set a second order gradient descend
+method 'BFGS' # setting optimizer cDecompose.set_Optimizer("BFGS") # continue
+the decomposition with a second optimizer method cDecompose.get_Initial_Circuit
+() After solving the optimization problem for the initial gate structure, we
+can initiate gate compression iterations. (This step can be omited.) # starting
+compression iterations cDecompose.Compress_Circuit() By finalizing the gate
+structure we replace the CRY gates with CNOT gates. (CRY gates with small
+rotation angle are approximately expressed with a single CNOT gate, so further
+optimization process needs to be initiated.) # finalize the gate structure
+(replace CRY gates with CNOT gates) cDecompose.Finalize_Circuit() Finally, we
+can retrieve the decomposed quantum circuit in QISKIT format. # get the
+decomposing operations quantum_circuit = cDecompose.get_Quantum_Circuit() ###
+How to cite us If you have found our work useful for your research project,
+please cite us by [1] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the
+theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022).
 [2] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Efficient quantum gate decomposition via
 adaptive circuit compression, arXiv:2203.04426.
 [3] Peter Rakyta, Gregory Morse, Jakab NÃ¡dori, Zita Majnay-TakÃ¡cs, Oskar
 Mencer, ZoltÃ¡n ZimborÃ¡s, Highly optimized quantum circuits synthesized via
 data-flow engines, arXiv:2211.07685
```

### Comparing `squander-1.7.4/README.md` & `squander-1.8.0/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,7 +1,23 @@
+Metadata-Version: 2.1
+Name: squander
+Version: 1.8.0
+Summary: The C++ binding for the SQUANDER package
+Home-page: https://github.com/rakytap/sequential-quantum-gate-decomposer
+Maintainer: Peter Rakyta
+Maintainer-email: peter.rakyta@ttk.elte.hu
+License: GNU General Public License v3.0
+Keywords: test,cmake,extension
+Classifier: Intended Audience :: Developers
+Classifier: Natural Language :: English
+Classifier: Programming Language :: C
+Classifier: Programming Language :: C++
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)](https://doi.org/10.5281/zenodo.4508680)
  <a href="https://trackgit.com">
 <img src="https://us-central1-trackgit-analytics.cloudfunctions.net/token/ping/l0sfey1m19at85951dwl" alt="trackgit-views" />
 </a>
 
 # Sequential Quantum Gate Decomposer (SQUANDER)
 
@@ -208,16 +224,99 @@
 Thus, in order to get the decomposition of a unitary, one should rather provide the complex transpose of this unitary as the input for the SQUANDER decomposing process, as can be seen in the examples.
 
 
 ## Python Interface
 
 The SQUANDER package contains a Python interface allowing the access of the functionalities of the SQUANDER package from Python. 
 The usage of the SQUANDER Python interface is demonstrated in the example files in the directory **examples** located in the directory **path/to/SQUANDER/package**, or in test files located in sub-directories of **path/to/SQUANDER/package/qgd_python/*/test**. 
-The example files import the necessary **qgd_python** modules containing the wrapper classes to interface with the C++ SQUANDER library. 
-(So the SQUANDER package need to be installed or the compiled package needs to be added to the Python search path.)
+
+### Example code snippet
+
+Here we provide an example to use the SQUANDER package. The following python interface is accessible from version 1.8.0. 
+In this example we use two optimization engines for the decomposition:
+1. An evolutionary engine called AGENTS
+2. Second order gradient descend algorithm (BFGS)
+
+Firstly we construct a Python map to set hyper-parameters during the gate synthesis.
+
+        #Python map containing hyper-parameters
+        config = { 'max_outer_iterations': 1, 
+                    'max_inner_iterations_agent': 25000, 
+                    'max_inner_iterations_compression': 10000,
+                    'max_inner_iterations' : 500,
+                    'max_inner_iterations_final': 5000, 		
+                    'Randomized_Radius': 0.3, 
+                    'randomized_adaptive_layers': 1,
+                    'optimization_tolerance_agent': 1e-4,
+                    'optimization_tolerance': 1e-8,
+                    'agent_num': 10}
+ 
+Next we initialize the decomposition class with the unitary Umtx to be decomposed. 
+
+        # creating a class to decompose the unitary
+        from squander import N_Qubit_Decomposition_adaptive
+        cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config )
+
+The verbosity of the execution output can be controlled by the function call 
+
+        # setting the verbosity of the decomposition
+        cDecompose.set_Verbose( 3 )
+
+
+We construct the initial trial gate structure for the optimization consisting of 2 levels of adaptive layer. 
+(1 level is made of qubit_num*(qubit_num-1) two-qubit building blocks if all-to-all connectivity is assumed)
+
+
+        # adding decomposing layers to the gate structure
+        levels = 2
+        for idx in range(levels):
+            cDecompose.add_Adaptive_Layers()
+
+        cDecompose.add_Finalyzing_Layer_To_Gate_Structure()
+        
+We can construct an initial parameters set for the optimization by retrieving the number of free parameters. If the initial parameter set is not set, random parameters are used by default.
+
+        # setting intial parameter set
+        parameter_num = cDecompose.get_Parameter_Num()
+        parameters = np.zeros( (parameter_num,1), dtype=np.float64 )
+        cDecompose.set_Optimized_Parameters( parameters )
+
+We can use between several engines to solve the optimization problem. Here we use an evolutionary based algorithm named 'AGENTS'
+
+        # setting optimizer
+        cDecompose.set_Optimizer("AGENTS")
+	
+The optimization process is started by the function call	
+
+        # starting the decomposition
+        cDecompose.get_Initial_Circuit()
+	
+The optimization process terminates by either reaching the tolerance 'optimization_tolerance_agent' or by reaching the maximal iteration number 'max_inner_iterations_agent', or if the engines identifies a convergence to a local minimum. The SQUANDER framework enables one to continue the optimization using a different engine. In particular we set a second order gradient descend method 'BFGS' 
+
+        # setting optimizer
+        cDecompose.set_Optimizer("BFGS")
+
+        # continue the decomposition with a second optimizer method
+        cDecompose.get_Initial_Circuit()
+	
+After solving the optimization problem for the initial gate structure, we can initiate gate compression iterations. (This step can be omited.)	
+
+        # starting compression iterations
+        cDecompose.Compress_Circuit()
+	
+By finalizing the gate structure we replace the CRY gates with CNOT gates. (CRY gates with small rotation angle are approximately expressed with a single CNOT gate, so further optimization process needs to be initiated.)
+
+        # finalize the gate structure (replace CRY gates with CNOT gates)
+        cDecompose.Finalize_Circuit()
+
+Finally, we can retrieve the decomposed quantum circuit in QISKIT format.
+
+        # get the decomposing operations
+        quantum_circuit = cDecompose.get_Quantum_Circuit()
+
 
 
 ### How to cite us
 
 If you have found our work useful for your research project, please cite us by
 
 [1] Péter Rakyta, Zoltán Zimborás, Approaching the theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022). <br>
```

#### html2text {}

```diff
@@ -1,120 +1,127 @@
-[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)](https://
-doi.org/10.5281/zenodo.4508680) [trackgit-views] # Sequential Quantum Gate
-Decomposer (SQUANDER) The Sequential Quantum Gate Decomposer (SQUANDER) package
-provides a novel solution to decompose any n-qubit unitaries into a sequence of
-one-qubit rotations and two-qubit controlled gates (such as controlled NOT or
-controlled phase gate). SQUANDER utilizes two novel gate synthesis techniques
-reported in Refereces [1] and [2]. (i) To synthesize general unitaries SQUANDER
-applies periodic layers of two-qubit and parametric one-qubit gates to an n-
-qubit unitary such that the resulting unitary is 1-qubit decoupled, i.e., is a
-tensor product of an (n-1)-qubit and a 1-qubit unitary. Continuing the
-decoupling procedure sequentially one arrives at the end to a full
-decomposition of the original unitary into 1- and 2-qubit gates. SQUANDER
-provides lower CNOT counts for generic n-qubit unitaries (up to n=6) than the
-previously provided lower bounds. (ii) An adaptive circuit compression is used
-to optimize quantum circuit by the application of parametric two-qubit gates in
-the synthesis process. The utilization of these parametric two-qubit gates in
-the circuit design allows one to transform the discrete combinatorial problem
-of circuit synthesis into an optimization problem over continuous variables.
-The circuit is then compressed by a sequential removal of two-qubit gates from
-the design, while the remaining building blocks are continuously adapted to the
-reduced gate structure by iterated learning cycles. The SQUANDER library is
-written in C/C++ providing a Python interface via [C++ extensions](https://
-docs.python.org/3/library/ctypes.html). The present package is supplied with
-Python building script and CMake tools to ease its deployment. The SQUANDER
-package can be built with both Intel and GNU compilers, and can be link against
-various CBLAS libraries installed on the system. (So far the CLBAS libraries of
-the GNU Scientific Library, OpenBLAS and the Intel MKL packages were tested.)
-In the following we briefly summarize the steps to build, install and use the
-SQUANDER package. The project was supported by grant OTKA PD123927 and by the
-Ministry of Innovation and Technology and the National Research, Development
-and Innovation Office within the Quantum Information National Laboratory of
-Hungary. Find the documantation of the SQUANDER package at [CodeDocs[xyz]]
-(https://codedocs.xyz/rakytap/sequential-quantum-gate-decomposer/) ### Contact
-Us Have a question about the SQUANDER package? Don't hesitate to contact us at
-the following e-mails: * ZoltÃ¡n ZimborÃ¡s (researcher):
-zimboras.zoltan@wigner.hu * Peter Rakyta (developer): peter.rakyta@ttk.elte.hu
-### Dependencies The optimization algorithm of SQUANDER relies on the
-[multimin](https://www.gnu.org/software/gsl/doc/html/multimin.html) component
-of the [GNU Scientific Library](https://www.gnu.org/software/gsl/doc/html/
-index.html). We developed and tested the SQUANDER package with GNU Scientific
-Library of version 2.5, 2.6 and 2.7. The dependencies necessary to compile and
-build the SQUANDER package are the followings: * [CMake](https://cmake.org/)
-(>=3.10.2) * [GNU Scientific Library](https://www.gnu.org/software/gsl/doc/
-html/index.html) (>=2.5, shipped with the gsl python package) * C++/C [Intel]
-(https://software.intel.com/content/www/us/en/develop/tools/compilers/c-
-compilers.html) (>=14.0.1) or [GNU](https://gcc.gnu.org/) (>=v4.8.1) compiler *
-[TBB](https://github.com/oneapi-src/oneTBB) library (shipped with tbb-devel
-Python package) * [Intel MKL](https://software.intel.com/content/www/us/en/
-develop/tools/math-kernel-library.html) (optional) * [OpenBlas](https://
-www.openblas.net/) (optional, recommended) * [LAPACKE](https://www.netlib.org/
-lapack/lapacke.html) * [Doxygen](https://www.doxygen.nl/index.html) (optional)
-The Python interface of SQUANDER was developed and tested with Python 3.6-3.9.
-The SQUANDER Python interface needs the following packages to be installed on
-the system: * [Qiskit](https://qiskit.org/documentation/install.html) * [Numpy]
-(https://numpy.org/install/) * [scipy](https://www.scipy.org/install.html) *
-[scikit-build](https://scikit-build.readthedocs.io/en/latest/) * [tbb-devel]
-(https://pypi.org/project/tbb-devel/) (containing the TBB Library) * [gsl]
-(https://anaconda.org/conda-forge/gsl) (containing the GNU Scientific Library)
-### How to obtain GNU Scientific Library In order to build and use the SQUANDER
-we recommend the Anaconda virtual python environment providing all the required
-dependencies for SQUANDER. One can easily install the GNU Scientific Library
-for local users by the command $ conda install -c conda-forge gsl
-Alternatively, a python binding project alongside the GNU GSL library is
-accessible via pypi repository: $ pip install numpy swig $ pip install pygsl
-Here we describe an alternative way to deploy GNU Scientific Library from
-source by the end user without administrative privileges. The GNU Scientific
-Library can be downloaded from the site [https://www.gnu.org/software/gsl/]
-(https://www.gnu.org/software/gsl/). After the downloaded package is extracted
-somewhere in the home directory of the user (**path/to/gsl/source**), one
-should configure the building environment using the **configure** tool.
-Depending on the individual settings the default compiler to be invoked might
-be different from HPC to HPC. To ensure the usage of the GNU compiler, the
-following shell command should be executed inside the directory **path/to/gsl/
-source**: $ ./configure --prefix=path/to/gsl FC=gfortran CC=gcc CXX=g++
-(Similarly, Intel compiler can be forced by setting FC=ifort CC=icc and
-CXX=icpc.) The installation directory of the compiled GNU Scientific Library is
-given by **--prefix=path/to/gsl** (which is different from the directory path
-of the source files given by **path/to/gslsource**). To install GNU Scientific
-Library the user should have read and write permissions on the path **path/to/
-gsl** (which might be for example /home/username/gsl). After the successful
-configuration the GNU Scientific Library can be compiled by the shell command $
-make The compilation of the GNU Scientific Library takes some time. When the
-compilation is done, the package (including the C header files and the static
-and shared libraries) is installed into the directory **path/to/gsl** by the
-shell command: $ make install ### Install SQUANDER from Python Package Index
-(PyPI) Since version 1.7.1 the SQUANDER package is accessible at Python Package
-Index (PyPI). The package can be installed on linux systems following the steps
-outlined below: $ pip install numpy swig tbb-devel wheel scikit-build ninja
-qiskit $ pip install pygsl $ pip install squander ### Download the SQUANDER
-package The developer version of the Quantum Gate Decomposer package can be
-downloaded from github repository [https://github.com/rakytap/quantum-gate-
-decomposer/tree/master](https://github.com/rakytap/quantum-gate-decomposer/
-tree/master). After the package is downloaded into the directory **path/to/
-SQUANDER/package** (which would be the path to the source code of the SQUANDER
-package), one can proceed to the compilation steps described in the next
-section. ### How to build the SQUANDER package The SQUANDER package is equipped
-with a Python build script and CMake tools to ease the compilation and the
-deployment of the package. To ensure that SQUANDER package would find the
-necessary libraries and header files during compilation time it is advised to
-define the following environment variables: $ export GSL_LIB_DIR=path/to/gsl/
-lib(64) $ export GSL_INC_DIR=path/to/gsl/include The SQUANDER package is
-parallelized via Threading Building Block (TBB) libraries. If TBB is not
-present in the system, it can be easily installed via python package [tbb-
-devel](https://pypi.org/project/tbb-devel/). Alternatively the TBB libraries
-can be installed via apt or yum utility (sudo apt install libtbb-dev) or it can
-be downloaded from [https://github.com/oneapi-src/oneTBB](https://github.com/
-oneapi-src/oneTBB) and built from source. In this case one should supply the
-necessary environment variables pointing to the header and library files of the
-TBB package. For newer Intel compilers the TBB package is part of the Intel
-compiler package, similarly to the MKL package. If the TBB library is located
-at non-standrad path or the SQUANDER package is compiled with GNU compiler,
-then setting the $ export TBB_LIB_DIR=path/to/TBB/lib(64) $ export
-TBB_INC_DIR=path/to/TBB/include environment variables are sufficient for
+Metadata-Version: 2.1 Name: squander Version: 1.8.0 Summary: The C++ binding
+for the SQUANDER package Home-page: https://github.com/rakytap/sequential-
+quantum-gate-decomposer Maintainer: Peter Rakyta Maintainer-email:
+peter.rakyta@ttk.elte.hu License: GNU General Public License v3.0 Keywords:
+test,cmake,extension Classifier: Intended Audience :: Developers Classifier:
+Natural Language :: English Classifier: Programming Language :: C Classifier:
+Programming Language :: C++ Description-Content-Type: text/markdown License-
+File: LICENSE [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)]
+(https://doi.org/10.5281/zenodo.4508680) [trackgit-views] # Sequential Quantum
+Gate Decomposer (SQUANDER) The Sequential Quantum Gate Decomposer (SQUANDER)
+package provides a novel solution to decompose any n-qubit unitaries into a
+sequence of one-qubit rotations and two-qubit controlled gates (such as
+controlled NOT or controlled phase gate). SQUANDER utilizes two novel gate
+synthesis techniques reported in Refereces [1] and [2]. (i) To synthesize
+general unitaries SQUANDER applies periodic layers of two-qubit and parametric
+one-qubit gates to an n-qubit unitary such that the resulting unitary is 1-
+qubit decoupled, i.e., is a tensor product of an (n-1)-qubit and a 1-qubit
+unitary. Continuing the decoupling procedure sequentially one arrives at the
+end to a full decomposition of the original unitary into 1- and 2-qubit gates.
+SQUANDER provides lower CNOT counts for generic n-qubit unitaries (up to n=6)
+than the previously provided lower bounds. (ii) An adaptive circuit compression
+is used to optimize quantum circuit by the application of parametric two-qubit
+gates in the synthesis process. The utilization of these parametric two-qubit
+gates in the circuit design allows one to transform the discrete combinatorial
+problem of circuit synthesis into an optimization problem over continuous
+variables. The circuit is then compressed by a sequential removal of two-qubit
+gates from the design, while the remaining building blocks are continuously
+adapted to the reduced gate structure by iterated learning cycles. The SQUANDER
+library is written in C/C++ providing a Python interface via [C++ extensions]
+(https://docs.python.org/3/library/ctypes.html). The present package is
+supplied with Python building script and CMake tools to ease its deployment.
+The SQUANDER package can be built with both Intel and GNU compilers, and can be
+link against various CBLAS libraries installed on the system. (So far the CLBAS
+libraries of the GNU Scientific Library, OpenBLAS and the Intel MKL packages
+were tested.) In the following we briefly summarize the steps to build, install
+and use the SQUANDER package. The project was supported by grant OTKA PD123927
+and by the Ministry of Innovation and Technology and the National Research,
+Development and Innovation Office within the Quantum Information National
+Laboratory of Hungary. Find the documantation of the SQUANDER package at
+[CodeDocs[xyz]](https://codedocs.xyz/rakytap/sequential-quantum-gate-
+decomposer/) ### Contact Us Have a question about the SQUANDER package? Don't
+hesitate to contact us at the following e-mails: * ZoltÃ¡n ZimborÃ¡s
+(researcher): zimboras.zoltan@wigner.hu * Peter Rakyta (developer):
+peter.rakyta@ttk.elte.hu ### Dependencies The optimization algorithm of
+SQUANDER relies on the [multimin](https://www.gnu.org/software/gsl/doc/html/
+multimin.html) component of the [GNU Scientific Library](https://www.gnu.org/
+software/gsl/doc/html/index.html). We developed and tested the SQUANDER package
+with GNU Scientific Library of version 2.5, 2.6 and 2.7. The dependencies
+necessary to compile and build the SQUANDER package are the followings: *
+[CMake](https://cmake.org/) (>=3.10.2) * [GNU Scientific Library](https://
+www.gnu.org/software/gsl/doc/html/index.html) (>=2.5, shipped with the gsl
+python package) * C++/C [Intel](https://software.intel.com/content/www/us/en/
+develop/tools/compilers/c-compilers.html) (>=14.0.1) or [GNU](https://
+gcc.gnu.org/) (>=v4.8.1) compiler * [TBB](https://github.com/oneapi-src/oneTBB)
+library (shipped with tbb-devel Python package) * [Intel MKL](https://
+software.intel.com/content/www/us/en/develop/tools/math-kernel-library.html)
+(optional) * [OpenBlas](https://www.openblas.net/) (optional, recommended) *
+[LAPACKE](https://www.netlib.org/lapack/lapacke.html) * [Doxygen](https://
+www.doxygen.nl/index.html) (optional) The Python interface of SQUANDER was
+developed and tested with Python 3.6-3.9. The SQUANDER Python interface needs
+the following packages to be installed on the system: * [Qiskit](https://
+qiskit.org/documentation/install.html) * [Numpy](https://numpy.org/install/) *
+[scipy](https://www.scipy.org/install.html) * [scikit-build](https://scikit-
+build.readthedocs.io/en/latest/) * [tbb-devel](https://pypi.org/project/tbb-
+devel/) (containing the TBB Library) * [gsl](https://anaconda.org/conda-forge/
+gsl) (containing the GNU Scientific Library) ### How to obtain GNU Scientific
+Library In order to build and use the SQUANDER we recommend the Anaconda
+virtual python environment providing all the required dependencies for
+SQUANDER. One can easily install the GNU Scientific Library for local users by
+the command $ conda install -c conda-forge gsl Alternatively, a python binding
+project alongside the GNU GSL library is accessible via pypi repository: $ pip
+install numpy swig $ pip install pygsl Here we describe an alternative way to
+deploy GNU Scientific Library from source by the end user without
+administrative privileges. The GNU Scientific Library can be downloaded from
+the site [https://www.gnu.org/software/gsl/](https://www.gnu.org/software/gsl/
+). After the downloaded package is extracted somewhere in the home directory of
+the user (**path/to/gsl/source**), one should configure the building
+environment using the **configure** tool. Depending on the individual settings
+the default compiler to be invoked might be different from HPC to HPC. To
+ensure the usage of the GNU compiler, the following shell command should be
+executed inside the directory **path/to/gsl/source**: $ ./configure --
+prefix=path/to/gsl FC=gfortran CC=gcc CXX=g++ (Similarly, Intel compiler can be
+forced by setting FC=ifort CC=icc and CXX=icpc.) The installation directory of
+the compiled GNU Scientific Library is given by **--prefix=path/to/gsl** (which
+is different from the directory path of the source files given by **path/to/
+gslsource**). To install GNU Scientific Library the user should have read and
+write permissions on the path **path/to/gsl** (which might be for example /
+home/username/gsl). After the successful configuration the GNU Scientific
+Library can be compiled by the shell command $ make The compilation of the GNU
+Scientific Library takes some time. When the compilation is done, the package
+(including the C header files and the static and shared libraries) is installed
+into the directory **path/to/gsl** by the shell command: $ make install ###
+Install SQUANDER from Python Package Index (PyPI) Since version 1.7.1 the
+SQUANDER package is accessible at Python Package Index (PyPI). The package can
+be installed on linux systems following the steps outlined below: $ pip install
+numpy swig tbb-devel wheel scikit-build ninja qiskit $ pip install pygsl $ pip
+install squander ### Download the SQUANDER package The developer version of the
+Quantum Gate Decomposer package can be downloaded from github repository
+[https://github.com/rakytap/quantum-gate-decomposer/tree/master](https://
+github.com/rakytap/quantum-gate-decomposer/tree/master). After the package is
+downloaded into the directory **path/to/SQUANDER/package** (which would be the
+path to the source code of the SQUANDER package), one can proceed to the
+compilation steps described in the next section. ### How to build the SQUANDER
+package The SQUANDER package is equipped with a Python build script and CMake
+tools to ease the compilation and the deployment of the package. To ensure that
+SQUANDER package would find the necessary libraries and header files during
+compilation time it is advised to define the following environment variables: $
+export GSL_LIB_DIR=path/to/gsl/lib(64) $ export GSL_INC_DIR=path/to/gsl/include
+The SQUANDER package is parallelized via Threading Building Block (TBB)
+libraries. If TBB is not present in the system, it can be easily installed via
+python package [tbb-devel](https://pypi.org/project/tbb-devel/). Alternatively
+the TBB libraries can be installed via apt or yum utility (sudo apt install
+libtbb-dev) or it can be downloaded from [https://github.com/oneapi-src/oneTBB]
+(https://github.com/oneapi-src/oneTBB) and built from source. In this case one
+should supply the necessary environment variables pointing to the header and
+library files of the TBB package. For newer Intel compilers the TBB package is
+part of the Intel compiler package, similarly to the MKL package. If the TBB
+library is located at non-standrad path or the SQUANDER package is compiled
+with GNU compiler, then setting the $ export TBB_LIB_DIR=path/to/TBB/lib(64) $
+export TBB_INC_DIR=path/to/TBB/include environment variables are sufficient for
 successful compilation. When the TBB library is installed via a python package,
 setting the environment variables above is not necessary. The SQUANDER package
 with C++ Python extensions can be compiled via the Python script **setup.py**
 located in the root directory of the SQUANDER package. The script automatically
 finds out the CBLAS library working behind the numpy package and uses it in
 further linking. The **setup.py** script also build the C++ library of the
 SQUANDER package by making the appropriate CMake calls. ### Developer build We
@@ -157,19 +164,62 @@
 decomposition of a unitary, one should rather provide the complex transpose of
 this unitary as the input for the SQUANDER decomposing process, as can be seen
 in the examples. ## Python Interface The SQUANDER package contains a Python
 interface allowing the access of the functionalities of the SQUANDER package
 from Python. The usage of the SQUANDER Python interface is demonstrated in the
 example files in the directory **examples** located in the directory **path/to/
 SQUANDER/package**, or in test files located in sub-directories of **path/to/
-SQUANDER/package/qgd_python/*/test**. The example files import the necessary
-**qgd_python** modules containing the wrapper classes to interface with the C++
-SQUANDER library. (So the SQUANDER package need to be installed or the compiled
-package needs to be added to the Python search path.) ### How to cite us If you
-have found our work useful for your research project, please cite us by [1]
-PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the theoretical limit in quantum
-gate decomposition, Quantum 6, 710 (2022).
+SQUANDER/package/qgd_python/*/test**. ### Example code snippet Here we provide
+an example to use the SQUANDER package. The following python interface is
+accessible from version 1.8.0. In this example we use two optimization engines
+for the decomposition: 1. An evolutionary engine called AGENTS 2. Second order
+gradient descend algorithm (BFGS) Firstly we construct a Python map to set
+hyper-parameters during the gate synthesis. #Python map containing hyper-
+parameters config = { 'max_outer_iterations': 1, 'max_inner_iterations_agent':
+25000, 'max_inner_iterations_compression': 10000, 'max_inner_iterations' : 500,
+'max_inner_iterations_final': 5000, 'Randomized_Radius': 0.3,
+'randomized_adaptive_layers': 1, 'optimization_tolerance_agent': 1e-4,
+'optimization_tolerance': 1e-8, 'agent_num': 10} Next we initialize the
+decomposition class with the unitary Umtx to be decomposed. # creating a class
+to decompose the unitary from squander import N_Qubit_Decomposition_adaptive
+cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config ) The
+verbosity of the execution output can be controlled by the function call #
+setting the verbosity of the decomposition cDecompose.set_Verbose( 3 ) We
+construct the initial trial gate structure for the optimization consisting of 2
+levels of adaptive layer. (1 level is made of qubit_num*(qubit_num-1) two-qubit
+building blocks if all-to-all connectivity is assumed) # adding decomposing
+layers to the gate structure levels = 2 for idx in range(levels):
+cDecompose.add_Adaptive_Layers()
+cDecompose.add_Finalyzing_Layer_To_Gate_Structure() We can construct an initial
+parameters set for the optimization by retrieving the number of free
+parameters. If the initial parameter set is not set, random parameters are used
+by default. # setting intial parameter set parameter_num =
+cDecompose.get_Parameter_Num() parameters = np.zeros( (parameter_num,1),
+dtype=np.float64 ) cDecompose.set_Optimized_Parameters( parameters ) We can use
+between several engines to solve the optimization problem. Here we use an
+evolutionary based algorithm named 'AGENTS' # setting optimizer
+cDecompose.set_Optimizer("AGENTS") The optimization process is started by the
+function call # starting the decomposition cDecompose.get_Initial_Circuit() The
+optimization process terminates by either reaching the tolerance
+'optimization_tolerance_agent' or by reaching the maximal iteration number
+'max_inner_iterations_agent', or if the engines identifies a convergence to a
+local minimum. The SQUANDER framework enables one to continue the optimization
+using a different engine. In particular we set a second order gradient descend
+method 'BFGS' # setting optimizer cDecompose.set_Optimizer("BFGS") # continue
+the decomposition with a second optimizer method cDecompose.get_Initial_Circuit
+() After solving the optimization problem for the initial gate structure, we
+can initiate gate compression iterations. (This step can be omited.) # starting
+compression iterations cDecompose.Compress_Circuit() By finalizing the gate
+structure we replace the CRY gates with CNOT gates. (CRY gates with small
+rotation angle are approximately expressed with a single CNOT gate, so further
+optimization process needs to be initiated.) # finalize the gate structure
+(replace CRY gates with CNOT gates) cDecompose.Finalize_Circuit() Finally, we
+can retrieve the decomposed quantum circuit in QISKIT format. # get the
+decomposing operations quantum_circuit = cDecompose.get_Quantum_Circuit() ###
+How to cite us If you have found our work useful for your research project,
+please cite us by [1] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the
+theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022).
 [2] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Efficient quantum gate decomposition via
 adaptive circuit compression, arXiv:2203.04426.
 [3] Peter Rakyta, Gregory Morse, Jakab NÃ¡dori, Zita Majnay-TakÃ¡cs, Oskar
 Mencer, ZoltÃ¡n ZimborÃ¡s, Highly optimized quantum circuits synthesized via
 data-flow engines, arXiv:2211.07685
```

### Comparing `squander-1.7.4/cmake/check_AVX.cmake` & `squander-1.8.0/cmake/check_AVX.cmake`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/Adam.cpp` & `squander-1.8.0/common/Adam.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/common.cpp` & `squander-1.8.0/common/common.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/common_DFE.cpp` & `squander-1.8.0/common/common_DFE.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -42,15 +42,15 @@
 /// mutex to guard DFE lib locking and unlocking
 std::recursive_mutex libmutex; //writing mutex
 std::mutex libreadmutex; //reader mutex
 
 
 size_t (*get_accelerator_avail_num_dll)() = NULL;
 size_t (*get_accelerator_free_num_dll)() = NULL;
-int (*calcqgdKernelDFE_dll)(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, double* trace) = NULL;
+int (*calcqgdKernelDFE_dll)(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, int traceOffset, double* trace) = NULL;
 int (*load2LMEM_dll)(QGD_Complex16* data, size_t rows, size_t cols) = NULL;
 void (*releive_DFE_dll)() = NULL;
 int (*initialize_DFE_dll)( int accelerator_num ) = NULL;
 int (*get_chained_gates_num_dll)() = NULL;
 
 // The ID of the class initializing the DFE lib
 int initialize_id = -1;
@@ -193,18 +193,18 @@
 
 }
 
 /**
 @brief ????????????
 @return ??????????
 */
-int calcqgdKernelDFE(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, double* trace) {
+int calcqgdKernelDFE(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, int traceOffset, double* trace) {
 
 
-    return calcqgdKernelDFE_dll(rows, cols, gates, gatesNum, gateSetNum, trace);
+    return calcqgdKernelDFE_dll(rows, cols, gates, gatesNum, gateSetNum, traceOffset, trace);
 
 }
 
 
 
 /**
 @brief ????????????
```

### Comparing `squander-1.7.4/common/dot.cpp` & `squander-1.8.0/common/dot.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/Adam.h` & `squander-1.8.0/common/include/Adam.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/QGDTypes.h` & `squander-1.8.0/common/include/QGDTypes.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/common.h` & `squander-1.8.0/common/include/common.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/common_DFE.h` & `squander-1.8.0/common/include/common_DFE.h`

 * *Files 2% similar despite different names*

```diff
@@ -93,15 +93,15 @@
 */
 int get_initialize_id();
 
 /**
 @brief ????????????
 @return ??????????
 */
-int calcqgdKernelDFE(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, double* trace);
+int calcqgdKernelDFE(size_t rows, size_t cols, DFEgate_kernel_type* gates, int gatesNum, int gateSetNum, int traceOffset, double* trace);
 
 
 /**
 @brief ????????????
 @return ??????????
 */
 int get_chained_gates_num();
```

### Comparing `squander-1.7.4/common/include/dot.h` & `squander-1.8.0/common/include/dot.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/logging.h` & `squander-1.8.0/common/include/logging.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/matrix.h` & `squander-1.8.0/common/include/matrix.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/matrix_base.h` & `squander-1.8.0/common/include/matrix_base.h`

 * *Files 0% similar despite different names*

```diff
@@ -427,15 +427,15 @@
   // logical variable indicating whether the matrix needs to be conjugated in CBLAS operations
   ret.conjugated = conjugated;
   // logical variable indicating whether the matrix needs to be transposed in CBLAS operations
   ret.transposed = transposed;
   // logical value indicating whether the class instance is the owner of the stored data or not. (If true, the data array is released in the destructor)
   ret.owner = true;
 
-  memcpy( ret.data, data, rows*cols*sizeof(scalar));
+  memcpy( ret.data, data, rows*stride*sizeof(scalar));
 
   return ret;
 
 }
```

### Comparing `squander-1.7.4/common/include/matrix_real.h` & `squander-1.8.0/common/include/matrix_real.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/mpi_base.h` & `squander-1.8.0/common/include/mpi_base.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/include/numpy_interface.h` & `squander-1.8.0/common/include/numpy_interface.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/logging.cpp` & `squander-1.8.0/common/logging.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/matrix.cpp` & `squander-1.8.0/common/matrix.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -109,15 +109,15 @@
   // logical variable indicating whether the matrix needs to be conjugated in CBLAS operations
   ret.conjugated = conjugated;
   // logical variable indicating whether the matrix needs to be transposed in CBLAS operations
   ret.transposed = transposed;
   // logical value indicating whether the class instance is the owner of the stored data or not. (If true, the data array is released in the destructor)
   ret.owner = true;
 
-  memcpy( ret.data, data, rows*cols*sizeof(QGD_Complex16));
+  memcpy( ret.data, data, rows*stride*sizeof(QGD_Complex16));
 
   return ret;
 
 }
 
 
 /**
```

### Comparing `squander-1.7.4/common/matrix_real.cpp` & `squander-1.8.0/common/matrix_real.cpp`

 * *Files 0% similar despite different names*

```diff
@@ -108,15 +108,15 @@
   // logical variable indicating whether the matrix needs to be conjugated in CBLAS operations
   ret.conjugated = conjugated;
   // logical variable indicating whether the matrix needs to be transposed in CBLAS operations
   ret.transposed = transposed;
   // logical value indicating whether the class instance is the owner of the stored data or not. (If true, the data array is released in the destructor)
   ret.owner = true;
 
-  memcpy( ret.data, data, rows*cols*sizeof(double));
+  memcpy( ret.data, data, rows*stride*sizeof(double));
 
   return ret;
 
 }
 
 
 /**
```

### Comparing `squander-1.7.4/common/mpi_base.cpp` & `squander-1.8.0/common/mpi_base.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/common/numpy_interface.cpp` & `squander-1.8.0/common/numpy_interface.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/decomposition/Decomposition_Base.cpp` & `squander-1.8.0/decomposition/Decomposition_Base.cpp`

 * *Files 3% similar despite different names*

```diff
@@ -67,18 +67,18 @@
     // number of iteratrion loops in the finale optimization
     //iteration_loops = dict()
 
     // The maximal allowed error of the optimization problem
     optimization_tolerance = 1e-7;
 
     // Maximal number of iteartions in the optimization process
-    max_iterations = 1e8;
+    max_outer_iterations = 1e8;
 
     // number of operators in one sub-layer of the optimization process
-    optimization_block = 1;
+    optimization_block = -1;
 
     // method to guess initial values for the optimization. Possible values: ZEROS, RANDOM, CLOSE_TO_ZERO (default)
     initial_guess = ZEROS;
 
     // The convergence threshold in the optimization process
     convergence_threshold = 1e-5;
     
@@ -110,15 +110,15 @@
 /** Contructor of the class
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary to be decomposed.
 @param initial_guess_in Type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
 @return An instance of the class
 */
-Decomposition_Base::Decomposition_Base( Matrix Umtx_in, int qbit_num_in, guess_type initial_guess_in= CLOSE_TO_ZERO ) : Gates_block(qbit_num_in) {
+Decomposition_Base::Decomposition_Base( Matrix Umtx_in, int qbit_num_in, std::map<std::string, Config_Element>& config_in, guess_type initial_guess_in= CLOSE_TO_ZERO ) : Gates_block(qbit_num_in) {
 
     Init_max_layer_num();
 
    
     // the unitary operator to be decomposed
     Umtx = Umtx_in;
    
@@ -149,18 +149,18 @@
     // number of iteratrion loops in the finale optimization
     //iteration_loops = dict()
 
     // The maximal allowed error of the optimization problem
     optimization_tolerance = 1e-7;
 
     // Maximal number of iteartions in the optimization process
-    max_iterations = 1e8;
+    max_outer_iterations = 1e8;
 
     // number of operators in one sub-layer of the optimization process
-    optimization_block = 1;
+    optimization_block = -1;
 
     // method to guess initial values for the optimization. Possible values: ZEROS, RANDOM, CLOSE_TO_ZERO (default)
     initial_guess = initial_guess_in;
 
     // The convergence threshold in the optimization process
     convergence_threshold = 1e-5;
     
@@ -168,14 +168,18 @@
     global_phase_factor.real = 1;
     global_phase_factor.imag = 0;
     
     //name of the SQUANDER project
     std::string projectname = "";
 
 
+    // config maps
+    config   = config_in;
+
+
     // Will be used to obtain a seed for the random number engine
     std::random_device rd;  
 
     // seedign the random generator
     gen = std::mt19937(rd());
 
 #if CBLAS==1
@@ -214,18 +218,18 @@
 */
 void Decomposition_Base::set_optimization_blocks( int optimization_block_in) {
     optimization_block = optimization_block_in;
 }
 
 /**
 @brief Call to set the maximal number of the iterations in the optimization process
-@param max_iterations_in maximal number of iteartions in the optimization process
+@param max_outer_iterations_in maximal number of iteartions in the optimization process
 */
-void Decomposition_Base::set_max_iteration( int max_iterations_in) {
-    max_iterations = max_iterations_in;
+void Decomposition_Base::set_max_iteration( int max_outer_iterations_in) {
+    max_outer_iterations = max_outer_iterations_in;
 }
 
 
 /**
 @brief After the main optimization problem is solved, the indepent qubits can be rotated into state |0> by this def. The constructed gates are added to the array of gates needed to the decomposition of the input unitary.
 */
 void Decomposition_Base::finalize_decomposition() {
@@ -406,14 +410,18 @@
         int parameter_num_loc = parameter_num;
 
         // store the initial unitary to be decomposed
         Matrix Umtx_loc = Umtx;
 
         // storing the initial computational parameters
         int optimization_block_loc = optimization_block;
+        
+        if ( optimization_block == -1 ) {
+            optimization_block = gates.size();
+        }
 
         // random generator of real numbers   
         std::uniform_real_distribution<> distrib_real(0.0, 2*M_PI);
 
         // the array storing the optimized parameters
         gsl_vector* optimized_parameters_gsl = gsl_vector_alloc (parameter_num_loc);
 
@@ -469,21 +477,32 @@
         // the identity matrix used in the calculations
         Matrix Identity =  create_identity( matrix_size );
 
 
         gsl_vector *solution_guess_gsl = NULL;
 
 
+        // maximal number of outer iterations overriden by config
+        long long max_outer_iterations_loc;
+        if ( config.count("max_outer_iterations") > 0 ) {
+            config["max_outer_iterations"].get_property( max_outer_iterations_loc );
+         
+        }
+        else {
+            max_outer_iterations_loc =max_outer_iterations;
+        }
+
+
         //measure the time for the decomposition
         tbb::tick_count start_time = tbb::tick_count::now();
 
         ////////////////////////////////////////
         // Start the iterations
-        int iter_idx;
-        for ( iter_idx=0; iter_idx<max_iterations; iter_idx++) {
+        long long iter_idx;
+        for ( iter_idx=0; iter_idx<max_outer_iterations_loc; iter_idx++) {
 
             //determine the range of blocks to be optimalized togedther
             block_idx_end = block_idx_start - optimization_block;
             if (block_idx_end < 0) {
                 block_idx_end = 0;
             }
 
@@ -578,44 +597,44 @@
             }
 
 
             // optimization result is displayed in each 500th iteration
             if (iter_idx % 500 == 0) {                
                 tbb::tick_count current_time = tbb::tick_count::now();
                 std::stringstream sstream;
-		sstream << "The minimum with " << layer_num << " layers after " << iter_idx << " iterations is " << current_minimum << " calculated in " << (current_time - start_time).seconds() << " seconds" << std::endl;
+		sstream << "The minimum with " << layer_num << " layers after " << iter_idx << " outer iterations is " << current_minimum << " calculated in " << (current_time - start_time).seconds() << " seconds" << std::endl;
 		print(sstream, 2);            
                 start_time = tbb::tick_count::now();
             }
 
 
             // calculate the variance of the last 10 minimums
             double minvec_std = sqrt(gsl_stats_variance_m( minimum_vec, 1, min_vec_num, minvec_mean));
 
             // conditions to break the iteration cycles
             if (std::abs(minvec_std/minimum_vec[min_vec_num-1]) < convergence_threshold ) {              
 		std::stringstream sstream;
-	        sstream << "The iterations converged to minimum " << current_minimum << " after " << iter_idx << " iterations with " << layer_num << " layers" << std::endl;
+	        sstream << "The iterations converged to minimum " << current_minimum << " after " << iter_idx << " outer iterations with " << layer_num << " layers" << std::endl;
 		print(sstream, 1);             
                 break;
             }
             else if (check_optimization_solution()) {
       		std::stringstream sstream;
-		sstream << "The minimum with " << layer_num << " layers after " << iter_idx << " iterations is " << current_minimum << std::endl;
+		sstream << "The minimum with " << layer_num << " layers after " << iter_idx << " outer iterations is " << current_minimum << std::endl;
 		print(sstream, 1);  		               
                 break;
             }
 
 
         }
 
 
-        if (iter_idx == max_iterations && max_iterations>1) {            
+        if (iter_idx == max_outer_iterations_loc && max_outer_iterations_loc>1) {            
 		std::stringstream sstream;
-		sstream << "Reached maximal number of iterations" << std::endl << std::endl;
+		sstream << "Reached maximal number of outer iterations" << std::endl << std::endl;
 		print(sstream, 1);
         }
 
         // restoring the parameters to originals
         optimization_block = optimization_block_loc;
 
         // store the result of the optimization
@@ -624,16 +643,14 @@
 
         parameter_num = parameter_num_loc;
 /*
         if (optimized_parameters != NULL ) {
             qgd_free( optimized_parameters );
         }
 */
-
-
         optimized_parameters_mtx = Matrix_real( 1, parameter_num );
         memcpy( optimized_parameters_mtx.get_data(), optimized_parameters_gsl->data, parameter_num*sizeof(double) );
 
 
         // free unnecessary resources
         gsl_vector_free(optimized_parameters_gsl);
         gsl_vector_free(solution_guess_gsl);
@@ -676,15 +693,23 @@
 
 /** check_optimization_solution
 @brief Checks the convergence of the optimization problem.
 @return Returns with true if the target global minimum was reached during the optimization process, or false otherwise.
 */
 bool Decomposition_Base::check_optimization_solution() {
 
-        return (std::abs(current_minimum - global_target_minimum) < optimization_tolerance);
+        double optimization_tolerance_loc;
+        if ( config.count("optimization_tolerance") > 0 ) {
+             config["optimization_tolerance"].get_property( optimization_tolerance_loc );  
+        }
+        else {
+            optimization_tolerance_loc = optimization_tolerance;
+        }       
+
+        return (std::abs(current_minimum - global_target_minimum) < optimization_tolerance_loc);
 
 }
 
 
 /**
 @brief Call to retrive a pointer to the unitary to be transformed
 @return Return with the unitary Umtx
```

### Comparing `squander-1.7.4/decomposition/N_Qubit_Decomposition.cpp` & `squander-1.8.0/decomposition/N_Qubit_Decomposition.cpp`

 * *Files 0% similar despite different names*

```diff
@@ -32,31 +32,33 @@
 @return An instance of the class
 */
 N_Qubit_Decomposition::N_Qubit_Decomposition() : N_Qubit_Decomposition_Base() {
 
     set_optimizer( BFGS );
 
 
+
 }
 
 
 
 
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-N_Qubit_Decomposition::N_Qubit_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in= CLOSE_TO_ZERO ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, optimize_layer_num_in, initial_guess_in) {
+N_Qubit_Decomposition::N_Qubit_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config_in, guess_type initial_guess_in= CLOSE_TO_ZERO ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, optimize_layer_num_in, config_in, initial_guess_in) {
 
     set_optimizer( BFGS );
+
 }
 
 
 
 /**
 @brief Destructor of the class
 */
@@ -100,15 +102,15 @@
     openblas_set_num_threads(1);
 #endif
 
     //measure the time for the decompositin
     tbb::tick_count start_time = tbb::tick_count::now();
 
     // create an instance of class to disentangle the given qubit pair
-    Sub_Matrix_Decomposition* cSub_decomposition = new Sub_Matrix_Decomposition(Umtx, qbit_num, optimize_layer_num, initial_guess);
+    Sub_Matrix_Decomposition* cSub_decomposition = new Sub_Matrix_Decomposition(Umtx, qbit_num, optimize_layer_num, config, initial_guess);
 
     // setting the verbosity
     cSub_decomposition->set_verbose( verbose );
 
     // setting the debugfile name
     cSub_decomposition->set_debugfile( debugfile_name );
 
@@ -130,15 +132,15 @@
     // The maximal error of the optimization problem
     cSub_decomposition->set_optimization_tolerance( optimization_tolerance );
 
     // setting the maximal number of iterations in the disentangling process
     cSub_decomposition->optimization_block = optimization_block;
 
     // setting the number of operators in one sub-layer of the disentangling process
-    //cSub_decomposition->max_iterations = self.max_iterations
+    //cSub_decomposition->max_outer_iterations = self.max_outer_iterations
 
     //start to disentangle the qubit pair
     cSub_decomposition->disentangle_submatrices();
     if ( !cSub_decomposition->subdisentaglement_done) {
         return;
     }
 //return;
@@ -159,16 +161,18 @@
 
         // simplify layers
         if (qbit_num>2) {
             simplify_layers();
         }
 
         int optimization_block_orig = optimization_block;
-        optimization_block = optimization_block*3;
-        //max_iterations = 4;
+        if ( optimization_block > 0 ) {
+            optimization_block = optimization_block*3;
+        }
+        //max_outer_iterations = 4;
 
 
         // final tuning of the decomposition parameters
         final_optimization();
 
         optimization_block = optimization_block_orig;
 
@@ -295,24 +299,24 @@
 
             }
         }
 
         // if the qubit number in the submatirx is greater than 2 new N-qubit decomposition is started
 
         // create class tp decompose submatrices
-        N_Qubit_Decomposition* cdecomposition = new N_Qubit_Decomposition(most_unitary_submatrix_mtx, qbit_num-1, optimize_layer_num, initial_guess);
+        N_Qubit_Decomposition* cdecomposition = new N_Qubit_Decomposition(most_unitary_submatrix_mtx, qbit_num-1, optimize_layer_num, config, initial_guess);
 
         // setting the verbosity
         cdecomposition->set_verbose( verbose );
 
         // setting the debugfile name
         cdecomposition->set_debugfile( debugfile_name );
 
         // Maximal number of iteartions in the optimization process
-        cdecomposition->set_max_iteration(max_iterations);
+        cdecomposition->set_max_iteration(max_outer_iterations);
 
         // Set the number of identical successive blocks in the sub-decomposition
         cdecomposition->set_identical_blocks(identical_blocks);
 
         // Set the maximal number of layers for the sub-decompositions
         cdecomposition->set_max_layer_num(max_layer_num);
 
@@ -772,15 +776,15 @@
             int col_idx = element_idx % 4;
             int row_idx = int((element_idx-col_idx)/4);
             submatrix[element_idx].real = full_matrix_reordered[col_idx*matrix_size+row_idx].real;
             submatrix[element_idx].imag = -full_matrix_reordered[col_idx*matrix_size+row_idx].imag;
         }
 
         // decompose the chosen 2-qubit unitary
-        N_Qubit_Decomposition* cdecomposition = new N_Qubit_Decomposition(submatrix, 2, true, initial_guess);
+        N_Qubit_Decomposition* cdecomposition = new N_Qubit_Decomposition(submatrix, 2, true, config, initial_guess);
 
         // set the maximal number of layers
         cdecomposition->set_max_layer_num( max_layer_num_loc );
 
         // suppress output messages
         cdecomposition->set_verbose( false );
```

### Comparing `squander-1.7.4/decomposition/N_Qubit_Decomposition_adaptive.cpp` & `squander-1.8.0/decomposition/N_Qubit_Decomposition_adaptive.cpp`

 * *Files 16% similar despite different names*

```diff
@@ -55,21 +55,21 @@
 
 
     // BFGS is better for smaller problems, while ADAM for larger ones
     if ( qbit_num <= 5 ) {
         set_optimizer( BFGS );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 4;
+        max_outer_iterations = 4;
     }
     else {
         set_optimizer( ADAM );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 1;
+        max_outer_iterations = 1;
     }
     
 
     // Boolean variable to determine whether randomized adaptive layers are used or not
     randomized_adaptive_layers = false;
 
 
@@ -77,42 +77,40 @@
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
+@param compression_enabled_in Optional logical value. If True(1) begin decomposition function will compress the circuit. If False(0) it will not. Compression can still be called in seperate wrapper function. 
 @return An instance of the class
 */
-N_Qubit_Decomposition_adaptive::N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, false, RANDOM, accelerator_num) {
+N_Qubit_Decomposition_adaptive::N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::map<std::string, Config_Element>& config, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, false, config, RANDOM, accelerator_num) {
 
 
     // set the level limit
     level_limit = level_limit_in;
     level_limit_min = level_limit_min_in;
 
-
-
-
     // BFGS is better for smaller problems, while ADAM for larger ones
     if ( qbit_num <= 5 ) {
         set_optimizer( BFGS );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 4;
+        max_outer_iterations = 4;
         
-        iter_max = 10000;
+        max_inner_iterations = 10000;
         gradient_threshold = 1e-8;
 
     }
     else {
         set_optimizer( ADAM );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 1;
+        max_outer_iterations = 1;
 
     }
 
     // Boolean variable to determine whether randomized adaptive layers are used or not
     randomized_adaptive_layers = false;
 
 
@@ -122,47 +120,48 @@
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
+@param compression_enabled_in Optional logical value. If True(1) begin decomposition function will compress the circuit. If False(0) it will not. Compression can still be called in seperate wrapper function. 
 @return An instance of the class
 */
-N_Qubit_Decomposition_adaptive::N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::vector<matrix_base<int>> topology_in, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, false, RANDOM, accelerator_num) {
+N_Qubit_Decomposition_adaptive::N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::vector<matrix_base<int>> topology_in, std::map<std::string, Config_Element>& config, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, false, config, RANDOM, accelerator_num) {
 
 
 
     // set the level limit
     level_limit = level_limit_in;
     level_limit_min = level_limit_min_in;
 
     // Maximal number of iteartions in the optimization process
-    max_iterations = 1;
+    max_outer_iterations = 1;
 
     gradient_threshold = 1e-8;
-
+    
     // setting the topology
     topology = topology_in;
 
 
 
 
     // BFGS is better for smaller problems, while ADAM for larger ones
     if ( qbit_num <= 5 ) {
         alg = BFGS;
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 4;
+        max_outer_iterations = 4;
     }
     else {
         alg = ADAM;
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 1;
+        max_outer_iterations = 1;
     }
 
     // Boolean variable to determine whether randomized adaptive layers are used or not
     randomized_adaptive_layers = false;
 
 }
 
@@ -221,36 +220,34 @@
 
     double optimization_tolerance_orig = optimization_tolerance;
 
 
     Gates_block* gate_structure_loc = NULL;
     if ( gates.size() > 0 ) {
         std::stringstream sstream;
-	sstream << "Using imported gate structure for the decomposition." << std::endl;
+        sstream << "Using imported gate structure for the decomposition." << std::endl;
         print(sstream, 1);	
 	        
         gate_structure_loc = optimize_imported_gate_structure(optimized_parameters_mtx);
     }
     else {
         std::stringstream sstream;
-	sstream << "Construct initial gate structure for the decomposition." << std::endl;
+        sstream << "Construct initial gate structure for the decomposition." << std::endl;
         print(sstream, 1);
         gate_structure_loc = determine_initial_gate_structure(optimized_parameters_mtx);
     }
 
 
-
     std::string filename("circuit_squander.binary");
     if (project_name != "") {
         filename = project_name+ "_" +filename;
     }
 
     export_gate_list_to_binary(optimized_parameters_mtx, gate_structure_loc, filename, verbose);
 
-
     sstream.str("");
     sstream << std::endl;
     sstream << std::endl;
     sstream << "**************************************************************" << std::endl;
     sstream << "***************** Compressing Gate structure *****************" << std::endl;
     sstream << "**************************************************************" << std::endl;
     print(sstream, 1);	    	
@@ -291,14 +288,15 @@
         }
 
         iter++;
 
         if (uncompressed_iter_num>10) break;
 
     }
+    
 
     sstream.str("");
     sstream << "**************************************************************" << std::endl;
     sstream << "************ Final tuning of the Gate structure **************" << std::endl;
     sstream << "**************************************************************" << std::endl;
     print(sstream, 1);	    	
     
@@ -317,48 +315,95 @@
     	
     Gates_block* gate_structure_tmp = replace_trivial_CRY_gates( gate_structure_loc, optimized_parameters_mtx );
     Matrix_real optimized_parameters_save = optimized_parameters_mtx;
 
     release_gates();
     optimized_parameters_mtx = optimized_parameters_save;
 
+    // solve the optimization problem
+    N_Qubit_Decomposition_custom cDecomp_custom;
+
+
+    std::map<std::string, Config_Element> config_copy;
+    config_copy.insert(config.begin(), config.end());
+    if ( config.count("max_inner_iterations_final") > 0 ) {
+        long long val;
+        config["max_inner_iterations_final"].get_property( val ); 
+        Config_Element element;
+        element.set_property( "max_inner_iterations", val ); 
+        config_copy["max_inner_iterations"] = element;
+    }
+
+
+    // solve the optimization problem in isolated optimization process
+    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, config_copy, initial_guess, accelerator_num);
+    cDecomp_custom.set_custom_gate_structure( gate_structure_tmp );
+    cDecomp_custom.set_optimized_parameters( optimized_parameters_mtx.get_data(), optimized_parameters_mtx.size() );
+    cDecomp_custom.set_optimization_blocks( gate_structure_loc->get_gate_num() );
+    cDecomp_custom.set_max_iteration( max_outer_iterations );
+    cDecomp_custom.set_verbose(verbose);
+    cDecomp_custom.set_cost_function_variant( cost_fnc );
+    cDecomp_custom.set_debugfile("");
+    cDecomp_custom.set_iteration_loops( iteration_loops );
+    cDecomp_custom.set_optimization_tolerance( optimization_tolerance ); 
+    cDecomp_custom.set_trace_offset( trace_offset ); 
+    cDecomp_custom.set_optimizer( alg );  
+    if (alg==ADAM || alg==BFGS2) { 
+        int param_num_loc = gate_structure_loc->get_parameter_num();
+        int max_inner_iterations_loc = (double)param_num_loc/852 * 1e7;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
+        cDecomp_custom.set_random_shift_count_max( 10000 );   
+        cDecomp_custom.set_adaptive_eta( true );      
+        cDecomp_custom.set_randomized_radius( radius );             
+    }
+    else if ( alg==ADAM_BATCHED ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 2500;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
+        cDecomp_custom.set_random_shift_count_max( 5 );   
+        cDecomp_custom.set_adaptive_eta( true );      
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
+    else if ( alg==BFGS ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 10000;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );    
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
+    cDecomp_custom.set_iteration_threshold_of_randomization( iteration_threshold_of_randomization );
+    cDecomp_custom.start_decomposition(true);
+    number_of_iters += cDecomp_custom.get_num_iters();
+
+    current_minimum = cDecomp_custom.get_current_minimum();
+    optimized_parameters_mtx = cDecomp_custom.get_optimized_parameters();
+
+
     combine( gate_structure_tmp );
     delete( gate_structure_tmp );
     delete( gate_structure_loc );
 
     sstream.str("");
     sstream << optimization_problem(optimized_parameters_mtx.get_data()) << std::endl;
     print(sstream, 3);	
     	
-    // reset the global minimum before final tuning
-    current_minimum = DBL_MAX;
-
-    set_adaptive_eta( true );
-
-    // final tuning of the decomposition parameters
-    final_optimization();
-
     std::string filename2("circuit_final.binary");
 
     if (project_name != "") {
         filename2=project_name+ "_"  +filename2;
     }
 
     export_gate_list_to_binary(optimized_parameters_mtx, this, filename2, verbose);  
 
     // prepare gates to export
     if (prepare_export) {
         prepare_gates_to_export();
     }
-
-    // calculating the final error of the decomposition
-    Matrix matrix_decomposed = get_transformed_matrix(optimized_parameters_mtx, gates.begin(), gates.size(), Umtx );
-    calc_decomposition_error( matrix_decomposed );
-
-
+    
+    decomposition_error = optimization_problem(optimized_parameters_mtx);
+    
     // get the number of gates used in the decomposition
     gates_num gates_num = get_gate_nums();
 
     
     sstream.str("");
     sstream << "In the decomposition with error = " << decomposition_error << " were used " << layer_num << " gates with:" << std::endl;
       
@@ -378,29 +423,344 @@
     
         sstream << std::endl;
         tbb::tick_count current_time = tbb::tick_count::now();
 
 	sstream << "--- In total " << (current_time - start_time).seconds() << " seconds elapsed during the decomposition ---" << std::endl;
     	print(sstream, 1);	    	
     	
-            
-         
-    
 
+#if BLAS==0 // undefined BLAS
+    omp_set_num_threads(num_threads);
+#elif BLAS==1 //MKL
+    MKL_Set_Num_Threads(num_threads);
+#elif BLAS==2 //OpenBLAS
+    openblas_set_num_threads(num_threads);
+#endif
+
+}
+void N_Qubit_Decomposition_adaptive::get_initial_circuit(){
+// temporarily turn off OpenMP parallelism
+#if BLAS==0 // undefined BLAS
+    num_threads = omp_get_max_threads();
+    omp_set_num_threads(1);
+#elif BLAS==1 // MKL
+    num_threads = mkl_get_max_threads();
+    MKL_Set_Num_Threads(1);
+#elif BLAS==2 //OpenBLAS
+    num_threads = openblas_get_num_threads();
+    openblas_set_num_threads(1);
+#endif
+    //measure the time for the decompositin
+    tbb::tick_count start_time = tbb::tick_count::now();
+
+    if (level_limit == 0 ) {
+        std::stringstream sstream;
+	sstream << "please increase level limit" << std::endl;
+        print(sstream, 0);	
+        return;
+    }
+
+
+
+    double optimization_tolerance_orig = optimization_tolerance;
+
+
+    Gates_block* gate_structure_loc = NULL;
+    if ( gates.size() > 0 ) {
+        std::stringstream sstream;
+        sstream << "Using imported gate structure for the decomposition." << std::endl;
+        print(sstream, 1);	
+	        
+        gate_structure_loc = optimize_imported_gate_structure(optimized_parameters_mtx);
+    }
+    else {
+        std::stringstream sstream;
+        sstream << "Construct initial gate structure for the decomposition." << std::endl;
+        print(sstream, 1);
+        gate_structure_loc = determine_initial_gate_structure(optimized_parameters_mtx);
+    }
+
+
+    std::string filename("circuit_squander.binary");
+    if (project_name != "") {
+        filename = project_name+ "_" +filename;
+    }
 
+    export_gate_list_to_binary(optimized_parameters_mtx, gate_structure_loc, filename, verbose);
+    std::string unitaryname("unitary_squander.binary");
+    if (project_name != "") {
+        filename = project_name+ "_" +unitaryname;
+    }
+    export_unitary(unitaryname);
+    release_gates();
+	combine( gate_structure_loc );
+	delete( gate_structure_loc );
 #if BLAS==0 // undefined BLAS
     omp_set_num_threads(num_threads);
 #elif BLAS==1 //MKL
     MKL_Set_Num_Threads(num_threads);
 #elif BLAS==2 //OpenBLAS
     openblas_set_num_threads(num_threads);
 #endif
+}
+
+void N_Qubit_Decomposition_adaptive::compress_circuit(){
+// temporarily turn off OpenMP parallelism
+#if BLAS==0 // undefined BLAS
+    num_threads = omp_get_max_threads();
+    omp_set_num_threads(1);
+#elif BLAS==1 // MKL
+    num_threads = mkl_get_max_threads();
+    MKL_Set_Num_Threads(1);
+#elif BLAS==2 //OpenBLAS
+    num_threads = openblas_get_num_threads();
+    openblas_set_num_threads(1);
+#endif
+	std::stringstream sstream;
+    sstream.str("");
+    sstream << std::endl;
+    sstream << std::endl;
+    sstream << "**************************************************************" << std::endl;
+    sstream << "***************** Compressing Gate structure *****************" << std::endl;
+    sstream << "**************************************************************" << std::endl;
+    print(sstream, 1);	    	
+	Gates_block* gate_structure_loc = NULL;
+    if ( gates.size() > 0 ) {
+		std::stringstream sstream;
+		sstream << "Using imported gate structure for the compression." << std::endl;
+		print(sstream, 1);	
+		    
+		gate_structure_loc =  static_cast<Gates_block*>(this)->clone();
+    }
+    else {
+        std::stringstream sstream;
+        sstream << "No circuit initalised." << std::endl;
+        print(sstream, 1);
+        return;
+    }
+    int iter = 0;
+    int uncompressed_iter_num = 0;
+    while ( iter<25 || uncompressed_iter_num <= 5 ) {
+        std::stringstream sstream;
+        sstream.str("");
+        sstream << "iteration " << iter+1 << ": ";
+        print(sstream, 1);	
+
+       
+        Gates_block* gate_structure_compressed = compress_gate_structure( gate_structure_loc );
+
+        if ( gate_structure_compressed->get_gate_num() < gate_structure_loc->get_gate_num() ) {
+            uncompressed_iter_num = 0;
+        }
+        else {
+            uncompressed_iter_num++;
+        }
+
+        if ( gate_structure_compressed != gate_structure_loc ) {
+            delete( gate_structure_loc );
+            gate_structure_loc = gate_structure_compressed;
+            gate_structure_compressed = NULL;
+            
 
+            std::string filename("circuit_compression.binary");
+            if (project_name != "") { 
+                filename=project_name+ "_"  +filename;
+            }
+
+            export_gate_list_to_binary(optimized_parameters_mtx, gate_structure_loc, filename, verbose); 
+            std::string filename_unitary("unitary_compression.binary");
+            export_unitary(filename_unitary);
+        }
+
+        iter++;
+
+        if (uncompressed_iter_num>10) break;
+            // store the decomposing gate structure
+    }
+    release_gates();
+	combine( gate_structure_loc );
+	delete( gate_structure_loc );
+#if BLAS==0 // undefined BLAS
+    omp_set_num_threads(num_threads);
+#elif BLAS==1 //MKL
+    MKL_Set_Num_Threads(num_threads);
+#elif BLAS==2 //OpenBLAS
+    openblas_set_num_threads(num_threads);
+#endif
 }
 
+void N_Qubit_Decomposition_adaptive::finalize_circuit(bool prepare_export){
+// temporarily turn off OpenMP parallelism
+#if BLAS==0 // undefined BLAS
+    num_threads = omp_get_max_threads();
+    omp_set_num_threads(1);
+#elif BLAS==1 // MKL
+    num_threads = mkl_get_max_threads();
+    MKL_Set_Num_Threads(1);
+#elif BLAS==2 //OpenBLAS
+    num_threads = openblas_get_num_threads();
+    openblas_set_num_threads(1);
+#endif
+	Gates_block* gate_structure_loc = NULL;
+    if ( gates.size() > 0 ) {
+        std::stringstream sstream;
+        sstream << "Using imported gate structure for the compression." << std::endl;
+        print(sstream, 1);	
+	        
+        gate_structure_loc =  static_cast<Gates_block*>(this)->clone();
+    }
+    else {
+        std::stringstream sstream;
+        sstream << "No circuit initalised." << std::endl;
+        print(sstream, 1);
+        return;
+    }
+    std::stringstream sstream;
+    sstream.str("");
+    sstream << "**************************************************************" << std::endl;
+    sstream << "************ Final tuning of the Gate structure **************" << std::endl;
+    sstream << "**************************************************************" << std::endl;
+    print(sstream, 1);	    	
+    
+	// maximal number of inner iterations overriden by config
+    if ( config.count("optimization_tolerance") > 0 ) {
+        long long value;
+        config["optimization_tolerance"].get_property( value );
+        optimization_tolerance = (double)value; 
+    }
+    else {optimization_tolerance = 1e-4;}
+
+
+
+    optimization_block = get_gate_num();
+
+
+    sstream.str("");
+    sstream << optimization_problem(optimized_parameters_mtx.get_data()) << std::endl;
+    print(sstream, 3);	
+    	
+    Gates_block* gate_structure_tmp = replace_trivial_CRY_gates( gate_structure_loc, optimized_parameters_mtx );
+    Matrix_real optimized_parameters_save = optimized_parameters_mtx;
+
+    release_gates();
+    optimized_parameters_mtx = optimized_parameters_save;
+
+    // solve the optimization problem
+    N_Qubit_Decomposition_custom cDecomp_custom;
+
+
+    std::map<std::string, Config_Element> config_copy;
+    config_copy.insert(config.begin(), config.end());
+    if ( config.count("max_inner_iterations_final") > 0 ) {
+        long long val;
+        config["max_inner_iterations_final"].get_property( val ); 
+        Config_Element element;
+        element.set_property( "max_inner_iterations", val ); 
+        config_copy["max_inner_iterations"] = element;
+    }
+
+
+    // solve the optimization problem in isolated optimization process
+    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, config_copy, initial_guess, accelerator_num);
+    cDecomp_custom.set_custom_gate_structure( gate_structure_tmp );
+    cDecomp_custom.set_optimized_parameters( optimized_parameters_mtx.get_data(), optimized_parameters_mtx.size() );
+    cDecomp_custom.set_optimization_blocks( gate_structure_loc->get_gate_num() );
+    cDecomp_custom.set_max_iteration( max_outer_iterations );
+    cDecomp_custom.set_verbose(verbose);
+    cDecomp_custom.set_cost_function_variant( cost_fnc );
+    cDecomp_custom.set_debugfile("");
+    cDecomp_custom.set_iteration_loops( iteration_loops );
+    cDecomp_custom.set_optimization_tolerance( optimization_tolerance ); 
+    cDecomp_custom.set_trace_offset( trace_offset ); 
+    cDecomp_custom.set_optimizer( alg );  
+    if (alg==ADAM || alg==BFGS2) { 
+        int param_num_loc = gate_structure_loc->get_parameter_num();
+        int max_inner_iterations_loc = (double)param_num_loc/852 * 1e7;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
+        cDecomp_custom.set_random_shift_count_max( 10000 );   
+        cDecomp_custom.set_adaptive_eta( true );      
+        cDecomp_custom.set_randomized_radius( radius );             
+    }
+    else if ( alg==ADAM_BATCHED ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 2500;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
+        cDecomp_custom.set_random_shift_count_max( 5 );   
+        cDecomp_custom.set_adaptive_eta( true );      
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
+    else if ( alg==BFGS ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 10000;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );    
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
+    cDecomp_custom.set_iteration_threshold_of_randomization( iteration_threshold_of_randomization );
+    cDecomp_custom.start_decomposition(true);
+    number_of_iters += cDecomp_custom.get_num_iters();
+
+    current_minimum = cDecomp_custom.get_current_minimum();
+    optimized_parameters_mtx = cDecomp_custom.get_optimized_parameters();
+
+
+    combine( gate_structure_tmp );
+    delete( gate_structure_tmp );
+    delete( gate_structure_loc );
+
+    sstream.str("");
+    sstream << optimization_problem(optimized_parameters_mtx.get_data()) << std::endl;
+    print(sstream, 3);	
+    	
+    std::string filename2("circuit_final.binary");
+
+    if (project_name != "") {
+        filename2=project_name+ "_"  +filename2;
+    }
+
+    export_gate_list_to_binary(optimized_parameters_mtx, this, filename2, verbose);  
+
+    // prepare gates to export
+    if (prepare_export) {
+        prepare_gates_to_export();
+    }
+    
+    decomposition_error = optimization_problem(optimized_parameters_mtx);
+    
+    // get the number of gates used in the decomposition
+    gates_num gates_num = get_gate_nums();
+
+    
+    sstream.str("");
+    sstream << "In the decomposition with error = " << decomposition_error << " were used " << layer_num << " gates with:" << std::endl;
+      
+        if ( gates_num.u3>0 ) sstream << gates_num.u3 << " U3 gates," << std::endl;
+        if ( gates_num.rx>0 ) sstream << gates_num.rx << " RX gates," << std::endl;
+        if ( gates_num.ry>0 ) sstream << gates_num.ry << " RY gates," << std::endl;
+        if ( gates_num.rz>0 ) sstream << gates_num.rz << " RZ gates," << std::endl;
+        if ( gates_num.cnot>0 ) sstream << gates_num.cnot << " CNOT gates," << std::endl;
+        if ( gates_num.cz>0 ) sstream << gates_num.cz << " CZ gates," << std::endl;
+        if ( gates_num.ch>0 ) sstream << gates_num.ch << " CH gates," << std::endl;
+        if ( gates_num.x>0 ) sstream << gates_num.x << " X gates," << std::endl;
+        if ( gates_num.sx>0 ) sstream << gates_num.sx << " SX gates," << std::endl; 
+        if ( gates_num.syc>0 ) sstream << gates_num.syc << " Sycamore gates," << std::endl;   
+        if ( gates_num.un>0 ) sstream << gates_num.un << " UN gates," << std::endl;
+        if ( gates_num.cry>0 ) sstream << gates_num.cry << " CRY gates," << std::endl;  
+        if ( gates_num.adap>0 ) sstream << gates_num.adap << " Adaptive gates," << std::endl;
+    
+        sstream << std::endl;
+    	print(sstream, 1);	    	
+    	
+#if BLAS==0 // undefined BLAS
+    omp_set_num_threads(num_threads);
+#elif BLAS==1 //MKL
+    MKL_Set_Num_Threads(num_threads);
+#elif BLAS==2 //OpenBLAS
+    openblas_set_num_threads(num_threads);
+#endif
+}
 
 /**
 @brief ??????????????
 */
 Gates_block* 
 N_Qubit_Decomposition_adaptive::optimize_imported_gate_structure(Matrix_real& optimized_parameters_mtx_loc) {
 
@@ -413,35 +773,52 @@
     std::stringstream sstream;
     sstream << "Starting optimization with " << gate_structure_loc->get_gate_num() << " decomposing layers." << std::endl;
     print(sstream, 1);	
 
     // solve the optimization problem
     N_Qubit_Decomposition_custom cDecomp_custom;
     // solve the optimization problem in isolated optimization process
-    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, initial_guess, accelerator_num);
+    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, config, initial_guess, accelerator_num);
     cDecomp_custom.set_custom_gate_structure( gate_structure_loc );
     cDecomp_custom.set_optimized_parameters( optimized_parameters_mtx_loc.get_data(), optimized_parameters_mtx_loc.size() );
     cDecomp_custom.set_optimization_blocks( gate_structure_loc->get_gate_num() );
-    cDecomp_custom.set_max_iteration( max_iterations );
+    cDecomp_custom.set_max_iteration( max_outer_iterations );
     cDecomp_custom.set_verbose(verbose);
     cDecomp_custom.set_cost_function_variant( cost_fnc );
     cDecomp_custom.set_debugfile("");
     cDecomp_custom.set_iteration_loops( iteration_loops );
     cDecomp_custom.set_optimization_tolerance( optimization_tolerance ); 
+    cDecomp_custom.set_trace_offset( trace_offset ); 
+    cDecomp_custom.set_optimizer( alg );  
+    cDecomp_custom.set_project_name( project_name );
     if (alg==ADAM || alg==BFGS2) { 
-        cDecomp_custom.set_optimizer( alg );  
         int param_num_loc = gate_structure_loc->get_parameter_num();
-        int iter_max_loc = (double)param_num_loc/852 * 1e7;
-        cDecomp_custom.set_iter_max( iter_max_loc );  
+        int max_inner_iterations_loc = (double)param_num_loc/852 * 1e7;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
         cDecomp_custom.set_random_shift_count_max( 10000 );   
         cDecomp_custom.set_adaptive_eta( true );      
         cDecomp_custom.set_randomized_radius( radius );             
     }
+    else if ( alg==ADAM_BATCHED ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 2500;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );  
+        cDecomp_custom.set_random_shift_count_max( 5 );   
+        cDecomp_custom.set_adaptive_eta( true );      
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
+    else if ( alg==BFGS ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 10000;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );    
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
     cDecomp_custom.set_iteration_threshold_of_randomization( iteration_threshold_of_randomization );
     cDecomp_custom.start_decomposition(true);
+    number_of_iters += cDecomp_custom.get_num_iters();
     //cDecomp_custom.list_gates(0);
 
     tbb::tick_count end_time_loc = tbb::tick_count::now();
 
     current_minimum = cDecomp_custom.get_current_minimum();
     optimized_parameters_mtx_loc = cDecomp_custom.get_optimized_parameters();
 
@@ -480,89 +857,130 @@
 Gates_block* 
 N_Qubit_Decomposition_adaptive::determine_initial_gate_structure(Matrix_real& optimized_parameters_mtx_loc) {
 
     // strages to store the optimized minimums in case of different cirquit depths
     std::vector<double> minimum_vec;
     std::vector<Gates_block*> gate_structure_vec;
     std::vector<Matrix_real> optimized_parameters_vec;
+    
+
 
     int level = level_limit_min;
     while ( current_minimum > optimization_tolerance && level <= level_limit) {
 
-        // reset optimized parameters
-        optimized_parameters_mtx_loc = Matrix_real(0,0);
-
-
         // create gate structure to be optimized
-        Gates_block* gate_structure_loc = new Gates_block(qbit_num);
-
+        Gates_block* gate_structure_loc = new Gates_block(qbit_num);  
+        
+        optimized_parameters_mtx_loc = Matrix_real(0,0);
+                   
         for (int idx=0; idx<level; idx++) {
 
             // create the new decomposing layer and add to the gate staructure
             add_adaptive_layers( gate_structure_loc );
 
         }
            
         // add finalyzing layer to the top of the gate structure
         add_finalyzing_layer( gate_structure_loc );
+            
 
         //measure the time for the decompositin
         tbb::tick_count start_time_loc = tbb::tick_count::now();
 
 
         N_Qubit_Decomposition_custom cDecomp_custom_random, cDecomp_custom_close_to_zero;
 
         std::stringstream sstream;
         sstream << "Starting optimization with " << gate_structure_loc->get_gate_num() << " decomposing layers." << std::endl;
-        print(sstream, 1);	
+        print(sstream, 1);
 
+	
+/*
 #ifndef __DFE__
         // try the decomposition withrandom and with close to zero initial values
         tbb::parallel_invoke(
             [&]{            
 #endif
+*/
                 // solve the optimization problem in isolated optimization process
-                cDecomp_custom_random = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, RANDOM, accelerator_num);
+                cDecomp_custom_random = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, config, RANDOM, accelerator_num);
                 cDecomp_custom_random.set_custom_gate_structure( gate_structure_loc );
                 cDecomp_custom_random.set_optimization_blocks( gate_structure_loc->get_gate_num() );
-                cDecomp_custom_random.set_max_iteration( max_iterations );
+                cDecomp_custom_random.set_max_iteration( max_outer_iterations );
+#ifndef __DFE__
                 cDecomp_custom_random.set_verbose(verbose);
+#else
+                cDecomp_custom_random.set_verbose(0);
+#endif
                 cDecomp_custom_random.set_cost_function_variant( cost_fnc );
                 cDecomp_custom_random.set_debugfile("");
                 cDecomp_custom_random.set_optimization_tolerance( optimization_tolerance );
+                cDecomp_custom_random.set_trace_offset( trace_offset ); 
+                cDecomp_custom_random.set_optimizer( alg );
+                cDecomp_custom_random.set_project_name( project_name );
                 if ( alg == ADAM || alg == BFGS2 ) {
-                    cDecomp_custom_random.set_optimizer( alg );  
                     int param_num_loc = gate_structure_loc->get_parameter_num();
-                    int iter_max_loc = (double)param_num_loc/852 * 1e7;
-                    cDecomp_custom_random.set_iter_max( iter_max_loc );  
+                    int max_inner_iterations_loc = (double)param_num_loc/852 * 1e7;
+                    cDecomp_custom_random.set_max_inner_iterations( max_inner_iterations_loc );  
                     cDecomp_custom_random.set_random_shift_count_max( 10000 );       
                     cDecomp_custom_random.set_adaptive_eta( true );    
                     cDecomp_custom_random.set_randomized_radius( radius );
                 }
+                else if ( alg==ADAM_BATCHED ) {
+                    cDecomp_custom_random.set_optimizer( alg );  
+                    int max_inner_iterations_loc = 2000;
+                    cDecomp_custom_random.set_max_inner_iterations( max_inner_iterations_loc );  
+                    cDecomp_custom_random.set_random_shift_count_max( 5 );   
+                    cDecomp_custom_random.set_adaptive_eta( true );      
+                    cDecomp_custom_random.set_randomized_radius( radius );   
+                }
+                else if ( alg==BFGS ) {
+                    cDecomp_custom_random.set_optimizer( alg );  
+                    int max_inner_iterations_loc = 10000;
+                    cDecomp_custom_random.set_max_inner_iterations( max_inner_iterations_loc );    
+                    cDecomp_custom_random.set_randomized_radius( radius );   
+                }
                 cDecomp_custom_random.set_iteration_threshold_of_randomization( iteration_threshold_of_randomization );
+                
+            
                 cDecomp_custom_random.start_decomposition(true);
+                
 
+                
+                number_of_iters += cDecomp_custom_random.get_num_iters(); // retrive the number of iterations spent on optimization
+/*
 #ifndef __DFE__
             },
             [&]{
                 // solve the optimization problem in isolated optimization process
                 cDecomp_custom_close_to_zero = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, CLOSE_TO_ZERO);
                 cDecomp_custom_close_to_zero.set_custom_gate_structure( gate_structure_loc );
                 cDecomp_custom_close_to_zero.set_optimization_blocks( gate_structure_loc->get_gate_num() );    
-                cDecomp_custom_close_to_zero.set_max_iteration( max_iterations );
+                cDecomp_custom_close_to_zero.set_max_iteration( max_outer_iterations );
                 cDecomp_custom_close_to_zero.set_verbose(0);
                 cDecomp_custom_close_to_zero.set_cost_function_variant( cost_fnc );
                 cDecomp_custom_close_to_zero.set_debugfile("");
                 cDecomp_custom_close_to_zero.set_optimization_tolerance( optimization_tolerance );  
-                cDecomp_custom_close_to_zero.start_decomposition(true);
+                cDecomp_custom_close_to_zero.set_optimizer( alg );
+                if ( alg == ADAM || alg == BFGS2 ) {
+                    int param_num_loc = gate_structure_loc->get_parameter_num();
+                    int max_inner_iterations_loc = (double)param_num_loc/852 * 1e7;
+                    cDecomp_custom_close_to_zero.set_max_inner_iterations( max_inner_iterations_loc );  
+                    cDecomp_custom_close_to_zero.set_random_shift_count_max( 10000 );       
+                    cDecomp_custom_close_to_zero.set_adaptive_eta( true );    
+                    cDecomp_custom_close_to_zero.set_randomized_radius( radius );
+                }
                 cDecomp_custom_close_to_zero.set_iteration_threshold_of_randomization( iteration_threshold_of_randomization );
+                cDecomp_custom.close_to_zero.set_trace_offset( trace_offset ); 
+                cDecomp_custom_close_to_zero.start_decomposition(true);
+                number_of_iters += cDecomp_custom_close_to_zero.get_num_iters();
                }
          );
 #endif
-
+*/
          tbb::tick_count end_time_loc = tbb::tick_count::now();
 /*
 #ifdef __DFE__
 return NULL;
 #endif
 */
          double current_minimum_random         = cDecomp_custom_random.get_current_minimum();
@@ -643,14 +1061,15 @@
     for (int idx=1; idx<(int)minimum_vec.size(); idx++) {
         if( current_minimum > minimum_vec[idx] ) {
             idx_min = idx;
             current_minimum = minimum_vec[idx];
         }
     }
      
+
     Gates_block* gate_structure_loc = gate_structure_vec[idx_min];
     optimized_parameters_mtx_loc = optimized_parameters_vec[idx_min];
 
     // release unnecesarry data
     for (int idx=0; idx<(int)minimum_vec.size(); idx++) {
         if( idx == idx_min ) {
             continue;
@@ -718,37 +1137,40 @@
 
     // preallocate panelties associated with the number of remaining two-qubit controlled gates
     std::vector<unsigned int> panelties(panelties_num, 1<<31);
     std::vector<Gates_block*> gate_structures_vec(panelties_num, NULL);
     std::vector<Matrix_real> optimized_parameters_vec(panelties_num, Matrix_real(0,0));
     std::vector<double> current_minimum_vec(panelties_num, DBL_MAX);
     std::vector<Matrix> Umtx_vec(panelties_num);
+    std::vector<int> iteration_num_vec(panelties_num, 0);
 
     for (int idx=0; idx<panelties_num; idx++) {
 
         Umtx = Umtx_orig.copy();
 
         double current_minimum_loc = DBL_MAX;//current_minimum;
+        int iteration_num = 0;
         Matrix_real optimized_parameters_loc = optimized_parameters_mtx.copy();
 
-        Gates_block* gate_structure_reduced = compress_gate_structure( gate_structure, layers_to_remove[idx], optimized_parameters_loc,  current_minimum_loc  );
+        Gates_block* gate_structure_reduced = compress_gate_structure( gate_structure, layers_to_remove[idx], optimized_parameters_loc,  current_minimum_loc, iteration_num  );
         if ( optimized_parameters_loc.size() == 0 ) optimized_parameters_loc = optimized_parameters_mtx.copy();
 
         // remove further adaptive gates if possible
         Gates_block* gate_structure_tmp;
         if ( gate_structure_reduced->get_gate_num() ==  gate_structure->get_gate_num() ) {
             gate_structure_tmp = gate_structure_reduced->clone();
         }
         else {
             gate_structure_tmp = remove_trivial_gates( gate_structure_reduced, optimized_parameters_loc, current_minimum_loc );
         }
         panelties[idx] = get_panelty(gate_structure_tmp, optimized_parameters_loc);
         gate_structures_vec[idx] = gate_structure_tmp;
         optimized_parameters_vec[idx] = optimized_parameters_loc;
         current_minimum_vec[idx] = current_minimum_loc;
+        iteration_num_vec[idx] = iteration_num;
         Umtx_vec[idx] = Umtx;
         
 
         delete(gate_structure_reduced);
 
 #ifdef __DFE__
         if ( current_minimum_vec[idx] < optimization_tolerance ) {
@@ -794,14 +1216,15 @@
     }
 
 
     // release the reduced gate structure, keep only the most efficient one
     gate_structure = gate_structures_vec[idx_min];
     optimized_parameters_mtx = optimized_parameters_vec[idx_min];
     current_minimum =  current_minimum_vec[idx_min];
+    number_of_iters += iteration_num_vec[idx_min];
     Umtx = Umtx_vec[idx_min];
     
     int layer_num = gate_structure->get_gate_num();
 
     if ( layer_num < layer_num_orig+1 ) {
        std::stringstream sstream;
        sstream << "gate structure reduced from " << layer_num_orig+1 << " to " << layer_num << " decomposing layers" << std::endl;
@@ -820,15 +1243,15 @@
 
 }
 
 /**
 @brief ???????????????
 */
 Gates_block* 
-N_Qubit_Decomposition_adaptive::compress_gate_structure( Gates_block* gate_structure, int layer_idx, Matrix_real& optimized_parameters, double& current_minimum_loc ) {
+N_Qubit_Decomposition_adaptive::compress_gate_structure( Gates_block* gate_structure, int layer_idx, Matrix_real& optimized_parameters, double& current_minimum_loc, int& iteration_num ) {
 
     // create reduced gate structure without layer indexed by layer_idx
     Gates_block* gate_structure_reduced = gate_structure->clone();
     gate_structure_reduced->release_gate( layer_idx );
 
     Matrix_real parameters_reduced;
     if ( optimized_parameters.size() > 0 ) {
@@ -837,35 +1260,55 @@
     else {
         parameters_reduced = Matrix_real(0, 0);
     }
     
 
 
     N_Qubit_Decomposition_custom cDecomp_custom;
+
+    std::map<std::string, Config_Element> config_copy;
+    config_copy.insert(config.begin(), config.end());
+    if ( config.count("max_inner_iterations_compression") > 0 ) {
+        long long val;
+        config["max_inner_iterations_compression"].get_property( val ); 
+        Config_Element element;
+        element.set_property( "max_inner_iterations", val ); 
+        config_copy["max_inner_iterations"] = element;
+    }
+
+
        
     // solve the optimization problem in isolated optimization process
-    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, initial_guess, accelerator_num);
+    cDecomp_custom = N_Qubit_Decomposition_custom( Umtx.copy(), qbit_num, false, config_copy, initial_guess, accelerator_num);
     cDecomp_custom.set_custom_gate_structure( gate_structure_reduced );
     cDecomp_custom.set_optimized_parameters( parameters_reduced.get_data(), parameters_reduced.size() );
     cDecomp_custom.set_verbose(0);
     cDecomp_custom.set_cost_function_variant( cost_fnc );
     cDecomp_custom.set_debugfile("");
-    cDecomp_custom.set_max_iteration( max_iterations );
+    cDecomp_custom.set_max_iteration( max_outer_iterations );
     cDecomp_custom.set_iteration_loops( iteration_loops );
     cDecomp_custom.set_optimization_blocks( gate_structure_reduced->get_gate_num() ) ;
     cDecomp_custom.set_optimization_tolerance( optimization_tolerance );
+    cDecomp_custom.set_trace_offset( trace_offset ); 
+    cDecomp_custom.set_optimizer( alg );
     if ( alg == ADAM || alg==BFGS2) {
-        cDecomp_custom.set_optimizer( alg );      
-        cDecomp_custom.set_iter_max( 1e5 );  
+        cDecomp_custom.set_max_inner_iterations( 1e5 );  
         cDecomp_custom.set_random_shift_count_max( 1 );     
         cDecomp_custom.set_adaptive_eta( false );
         cDecomp_custom.set_randomized_radius( radius );        
     }
+    else if ( alg==BFGS ) {
+        cDecomp_custom.set_optimizer( alg );  
+        int max_inner_iterations_loc = 100;
+        cDecomp_custom.set_max_inner_iterations( max_inner_iterations_loc );    
+        cDecomp_custom.set_randomized_radius( radius );   
+    }
     cDecomp_custom.set_iteration_threshold_of_randomization( 2500 );
     cDecomp_custom.start_decomposition(true);
+    iteration_num = cDecomp_custom.get_num_iters();
     double current_minimum_tmp = cDecomp_custom.get_current_minimum();
 
     if ( current_minimum_tmp < optimization_tolerance ) {
         //cDecomp_custom.list_gates(0);
         optimized_parameters = cDecomp_custom.get_optimized_parameters();
         current_minimum_loc = current_minimum_tmp;
         return gate_structure_reduced;
@@ -1200,16 +1643,18 @@
 
 
             std::stringstream sstream;
             sstream << "N_Qubit_Decomposition_adaptive::remove_trivial_gates: Removing trivial gateblock" << std::endl;
             print(sstream, 3);
                
             // remove gate from the structure
-            Gates_block* gate_structure_tmp = compress_gate_structure( gate_structure_loc, idx, optimized_parameters_loc, current_minimum_loc );
-
+            int iteration_num_loc = 0;
+            Gates_block* gate_structure_tmp = compress_gate_structure( gate_structure_loc, idx, optimized_parameters_loc, current_minimum_loc, iteration_num_loc );
+	    number_of_iters += iteration_num_loc;
+	    
             optimized_parameters = optimized_parameters_loc;
             delete( gate_structure_loc );
             gate_structure_loc = gate_structure_tmp;
             layer_num = gate_structure_loc->get_gate_num();   
             break;            
 
           
@@ -1365,16 +1810,25 @@
     for (int idx=0; idx<layers.size(); idx++) {
         Gates_block* layer = (Gates_block*)layers[idx];
         block->add_gate( layers[idx] );
 
     }
 */
 
+    bool randomized_adaptive_layers_loc;
+    if ( config.count("randomized_adaptive_layers") > 0 ) {
+        config["randomized_adaptive_layers"].get_property( randomized_adaptive_layers_loc );  
+    }
+    else {
+        randomized_adaptive_layers_loc = randomized_adaptive_layers;
+    }
+
+
     // make difference between randomized adaptive layers and deterministic one
-    if (randomized_adaptive_layers) {
+    if (randomized_adaptive_layers_loc) {
 
         std::uniform_int_distribution<> distrib_int(0, 5000);
 
         while (layers.size()>0) { 
             int idx = distrib_int(gen) % layers.size();
 
 #ifdef __MPI__
```

### Comparing `squander-1.7.4/decomposition/N_Qubit_Decomposition_custom.cpp` & `squander-1.8.0/decomposition/N_Qubit_Decomposition_custom.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -38,51 +38,51 @@
 
 
     // BFGS is better for smaller problems, while ADAM for larger ones
     if ( qbit_num <= 5 ) {
         set_optimizer( BFGS );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 4;
+        max_outer_iterations = 4;
     }
     else {
         set_optimizer( ADAM );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 1;
+        max_outer_iterations = 1;
     }
 
 }
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-N_Qubit_Decomposition_custom::N_Qubit_Decomposition_custom( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in= CLOSE_TO_ZERO, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, optimize_layer_num_in, initial_guess_in, accelerator_num) {
+N_Qubit_Decomposition_custom::N_Qubit_Decomposition_custom( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config, guess_type initial_guess_in= CLOSE_TO_ZERO, int accelerator_num ) : N_Qubit_Decomposition_Base(Umtx_in, qbit_num_in, optimize_layer_num_in, config, initial_guess_in, accelerator_num) {
 
     // initialize custom gate structure
     gate_structure = NULL;
 
 
     // BFGS is better for smaller problems, while ADAM for larger ones
     if ( qbit_num <= 5 ) {
         set_optimizer( BFGS );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 4;
+        max_outer_iterations = 4;
     }
     else {
         set_optimizer( ADAM );
 
         // Maximal number of iteartions in the optimization process
-        max_iterations = 1;
+        max_outer_iterations = 1;
     }
 
 }
 
 
 
 /**
```

### Comparing `squander-1.7.4/decomposition/Sub_Matrix_Decomposition.cpp` & `squander-1.8.0/decomposition/Sub_Matrix_Decomposition.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -59,15 +59,15 @@
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-Sub_Matrix_Decomposition::Sub_Matrix_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in=false, guess_type initial_guess_in= CLOSE_TO_ZERO ) : Decomposition_Base(Umtx_in, qbit_num_in, initial_guess_in) {
+Sub_Matrix_Decomposition::Sub_Matrix_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config_in, guess_type initial_guess_in= CLOSE_TO_ZERO ) : Decomposition_Base(Umtx_in, qbit_num_in, config_in, initial_guess_in) {
 
     // logical value. Set true if finding the minimum number of gate layers is required (default), or false when the maximal number of CNOT gates is used (ideal for general unitaries).
     optimize_layer_num  = optimize_layer_num_in;
 
     // A string describing the type of the class
     type = SUB_MATRIX_DECOMPOSITION_CLASS;
 
@@ -718,19 +718,19 @@
 /**
 @brief Create a clone of the present class.
 @return Return with a pointer pointing to the cloned object.
 */
 Sub_Matrix_Decomposition* Sub_Matrix_Decomposition::clone() {
 
 
-    Sub_Matrix_Decomposition* ret = new Sub_Matrix_Decomposition(Umtx, qbit_num, optimize_layer_num, initial_guess);
+    Sub_Matrix_Decomposition* ret = new Sub_Matrix_Decomposition(Umtx, qbit_num, optimize_layer_num, config, initial_guess);
 
     // setting computational parameters
     ret->set_identical_blocks( identical_blocks );
-    ret->set_max_iteration( max_iterations );
+    ret->set_max_iteration( max_outer_iterations );
     ret->set_optimization_blocks( optimization_block );
     ret->set_max_layer_num( max_layer_num );
     ret->set_iteration_loops( iteration_loops );
 
     if ( extract_gates(static_cast<Gates_block*>(ret)) != 0 ) {
 	std::stringstream sstream;
 	sstream << "Sub_Matrix_Decomposition::clone(): extracting gates was not succesfull\n" << std::endl;
```

### Comparing `squander-1.7.4/decomposition/Sub_Matrix_Decomposition_Cost_Function.cpp` & `squander-1.8.0/decomposition/Sub_Matrix_Decomposition_Cost_Function.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/decomposition/include/Decomposition_Base.h` & `squander-1.8.0/decomposition/include/Decomposition_Base.h`

 * *Files 1% similar despite different names*

```diff
@@ -47,14 +47,16 @@
 #include <cstdlib>
 #include <time.h>
 #include <ctime>
 #include "gsl/gsl_multimin.h"
 #include "gsl/gsl_statistics.h"
 #include <tbb/cache_aligned_allocator.h>
 
+#include "config_element.h"
+
 #include <random>
 
 /// @brief Type definition of the types of the initial guess
 typedef enum guess_type {ZEROS, RANDOM, CLOSE_TO_ZERO} guess_type;
 
 
 /**
@@ -76,14 +78,18 @@
     
     ///The global phase
     QGD_Complex16 global_phase_factor;
     
     ///the name of the project
     std::string project_name;
 
+    /// config metadata utilized during the optimization
+    std::map<std::string, Config_Element> config;
+
+
 protected:
 
     ///  A map of <int n: int num> indicating that how many layers should be used in the subdecomposition process for the subdecomposing of the nth qubits.
     std::map<int,int> max_layer_num;
 
     /// A map of <int n: int num> indicating the number of iteration in each step of the decomposition.
     std::map<int,int> iteration_loops;
@@ -115,15 +121,15 @@
     /// The global target minimum of the optimization problem
     double global_target_minimum;
 
     /// logical value describing whether the optimization problem was solved or not
     bool optimization_problem_solved;
 
     /// Maximal number of iterations allowed in the optimization process
-    int max_iterations;
+    int max_outer_iterations;
 
     /// type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
     guess_type initial_guess;
 
     /// Store the number of OpenMP threads. (During the calculations OpenMP multithreading is turned off.)
     int num_threads;
 
@@ -146,15 +152,15 @@
 /** Contructor of the class
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary to be decomposed.
 @param initial_guess_in Type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
 @return An instance of the class
 */
-Decomposition_Base( Matrix Umtx_in, int qbit_num_in, guess_type initial_guess_in);
+Decomposition_Base( Matrix Umtx_in, int qbit_num_in, std::map<std::string, Config_Element>& config_in, guess_type initial_guess_in);
 
 /**
 @brief Destructor of the class
 */
 virtual ~Decomposition_Base();
 
 
@@ -162,17 +168,17 @@
 @brief Call to set the number of gate blocks to be optimized in one shot
 @param optimization_block_in The number of gate blocks to be optimized in one shot
 */
 void set_optimization_blocks( int optimization_block_in );
 
 /**
 @brief Call to set the maximal number of the iterations in the optimization process
-@param max_iterations_in maximal number of iteartions in the optimization process
+@param max_outer_iterations_in maximal number of iteartions in the optimization process
 */
-void set_max_iteration( int max_iterations_in);
+void set_max_iteration( int max_outer_iterations_in);
 
 
 /**
 @brief After the main optimization problem is solved, the indepent qubits can be rotated into state |0> by this def. The constructed gates are added to the array of gates needed to the decomposition of the input unitary.
 */
 void finalize_decomposition();
```

### Comparing `squander-1.7.4/decomposition/include/N_Qubit_Decomposition.h` & `squander-1.8.0/decomposition/include/N_Qubit_Decomposition.h`

 * *Files 1% similar despite different names*

```diff
@@ -95,15 +95,15 @@
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-N_Qubit_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in );
+N_Qubit_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config, guess_type initial_guess_in );
 
 
 
 /**
 @brief Destructor of the class
 */
 virtual ~N_Qubit_Decomposition();
```

### Comparing `squander-1.7.4/decomposition/include/N_Qubit_Decomposition_Base.h` & `squander-1.8.0/decomposition/include/N_Qubit_Decomposition_Base.h`

 * *Files 23% similar despite different names*

```diff
@@ -23,15 +23,17 @@
 
 #ifndef N_Qubit_Decomposition_Base_H
 #define N_Qubit_Decomposition_Base_H
 
 #include "Decomposition_Base.h"
 
 /// @brief Type definition of the fifferent types of the cost function
-typedef enum cost_function_type {FROBENIUS_NORM, FROBENIUS_NORM_CORRECTION1, FROBENIUS_NORM_CORRECTION2} cost_function_type;
+typedef enum cost_function_type {FROBENIUS_NORM, FROBENIUS_NORM_CORRECTION1, FROBENIUS_NORM_CORRECTION2,
+    HILBERT_SCHMIDT_TEST, HILBERT_SCHMIDT_TEST_CORRECTION1, HILBERT_SCHMIDT_TEST_CORRECTION2,
+    SUM_OF_SQUARES} cost_function_type;
 
 
 
 #ifdef __cplusplus
 extern "C" 
 {
 #endif
@@ -55,28 +57,28 @@
 
 #ifdef __cplusplus
 }
 #endif
 
 
 /// implemented optimization algorithms
-enum optimization_aglorithms{ ADAM, BFGS, BFGS2 };
+enum optimization_aglorithms{ ADAM, BFGS, BFGS2, ADAM_BATCHED, AGENTS, COSINE, AGENTS_COMBINED };
 
 
 /**
 @brief A base class to determine the decomposition of an N-qubit unitary into a sequence of CNOT and U3 gates.
 This class contains the non-template implementation of the decomposition class.
 */
 class N_Qubit_Decomposition_Base : public Decomposition_Base {
 
 
 public:
 
     ///
-    int iter_max;
+    int max_inner_iterations;
     ///
     int gradient_threshold;
     /// 
     int random_shift_count_max;
     ///    
     double eta;
     /// unique id indentifying the instance of the class
@@ -95,31 +97,34 @@
     cost_function_type cost_fnc;
     ///
     double prev_cost_fnv_val;
     ///
     double correction1_scale;
     ///
     double correction2_scale;    
+    
+
+    /// number of iterations
+    int number_of_iters;
 
     /// logical variable indicating whether adaptive learning reate is used in the ADAM algorithm
     bool adaptive_eta;
     /// parameter to contron the radius of parameter randomization around the curren tminimum
     double radius;
     /// randomization rate
     double randomization_rate;
     /// threashold of count of iterations after what the parameters are randomized if the cost function does not deacrese fast enough
     unsigned long long iteration_threshold_of_randomization;
     /// number of utilized accelerators
     int accelerator_num;
 
+    /// The offset in the first columns from which the "trace" is calculated. In this case Tr(A) = sum_(i-offset=j) A_{ij}
+    int trace_offset;
 
 
-    Matrix_real randomization_probs;
-    matrix_base<int> randomized_probs;
-
     
 
 
 
 
 public:
 
@@ -135,15 +140,15 @@
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-N_Qubit_Decomposition_Base( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in, int accelerator_num_in=0 );
+N_Qubit_Decomposition_Base( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config, guess_type initial_guess_in, int accelerator_num_in=0 );
 
 
 
 /**
 @brief Destructor of the class
 */
 virtual ~N_Qubit_Decomposition_Base();
@@ -171,14 +176,37 @@
 @brief Call to solve layer by layer the optimization problem via calling one of the implemented algorithms. The optimalized parameters are stored in attribute optimized_parameters.
 @param num_of_parameters Number of parameters to be optimized
 @param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
 */
 void solve_layer_optimization_problem( int num_of_parameters, gsl_vector *solution_guess_gsl);
 
 
+/**
+@brief Call to solve layer by layer the optimization problem via the COSINE algorithm. The optimalized parameters are stored in attribute optimized_parameters.
+@param num_of_parameters Number of parameters to be optimized
+@param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
+*/
+void solve_layer_optimization_problem_COSINE( int num_of_parameters, gsl_vector *solution_guess_gsl);
+
+
+/**
+@brief Call to solve layer by layer the optimization problem via the AGENT algorithm. The optimalized parameters are stored in attribute optimized_parameters.
+@param num_of_parameters Number of parameters to be optimized
+@param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
+*/
+void solve_layer_optimization_problem_AGENTS( int num_of_parameters, gsl_vector *solution_guess_gsl);
+
+
+
+/**
+@brief Call to solve layer by layer the optimization problem via the AGENT COMBINED algorithm. The optimalized parameters are stored in attribute optimized_parameters.
+@param num_of_parameters Number of parameters to be optimized
+@param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
+*/
+void solve_layer_optimization_problem_AGENTS_COMBINED( int num_of_parameters, gsl_vector *solution_guess_gsl);
 
 
 /**
 @brief Call to solve layer by layer the optimization problem via BBFG algorithm. (optimal for smaller problems) The optimalized parameters are stored in attribute optimized_parameters.
 @param num_of_parameters Number of parameters to be optimized
 @param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
 */
@@ -189,26 +217,32 @@
 /**
 @brief Call to solve layer by layer the optimization problem via BBFG algorithm. The optimalized parameters are stored in attribute optimized_parameters.
 @param num_of_parameters Number of parameters to be optimized
 @param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
 */
 void solve_layer_optimization_problem_BFGS2( int num_of_parameters, gsl_vector *solution_guess_gsl);
 
+/**
+@brief Call to solve layer by layer the optimization problem via batched ADAM algorithm. (optimal for larger problems) The optimalized parameters are stored in attribute optimized_parameters.
+@param num_of_parameters Number of parameters to be optimized
+@param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
+*/
+void solve_layer_optimization_problem_ADAM_BATCHED( int num_of_parameters, gsl_vector *solution_guess_gsl);
 
 /**
 @brief Call to solve layer by layer the optimization problem via ADAM algorithm. (optimal for larger problems) The optimalized parameters are stored in attribute optimized_parameters.
 @param num_of_parameters Number of parameters to be optimized
 @param solution_guess_gsl A GNU Scientific Library vector containing the solution guess.
 */
 void solve_layer_optimization_problem_ADAM( int num_of_parameters, gsl_vector *solution_guess_gsl);
 
 /**
 @brief ?????????????
 */
-void randomize_parameters( Matrix_real& input, gsl_vector* output, const int randomization_succesful, const double& f0 );
+void randomize_parameters( Matrix_real& input, Matrix_real& output, const double& f0 );
 
 /**
 @brief The optimization problem of the final optimization
 @param parameters An array of the free parameters to be optimized. (The number of teh free paramaters should be equal to the number of parameters in one sub-layer)
 @return Returns with the cost function. (zero if the qubits are desintangled.)
 */
 double optimization_problem( double* parameters);
@@ -218,25 +252,51 @@
 @brief The optimization problem of the final optimization
 @param parameters An array of the free parameters to be optimized. (The number of teh free paramaters should be equal to the number of parameters in one sub-layer)
 @return Returns with the cost function. (zero if the qubits are desintangled.)
 */
 double optimization_problem( Matrix_real& parameters);
 
 
+/**
+@brief The optimization problem of the final optimization with batched input (implemented only for the Frobenius norm cost function)
+@param parameters An array of the free parameters to be optimized. (The number of teh free paramaters should be equal to the number of parameters in one sub-layer)
+@return Returns with the cost function. (zero if the qubits are desintangled.)
+*/
+Matrix_real optimization_problem_batched( std::vector<Matrix_real>& parameters_vec);
+
+
+/**
+@brief The optimization problem of the final optimization useful for gradient
+@param parameters A GNU Scientific Library containing the parameters to be optimized.
+@param void_instance A void pointer pointing to the instance of the current class.
+@param ret_temp A matrix to store trace in for gradient
+@return Returns with the cost function. (zero if the qubits are desintangled.)
+*/
+double optimization_problem( const gsl_vector* parameters, void* void_instance, Matrix ret_temp );
+
 
 /**
 @brief The optimization problem of the final optimization
 @param parameters A GNU Scientific Library containing the parameters to be optimized.
 @param void_instance A void pointer pointing to the instance of the current class.
 @return Returns with the cost function. (zero if the qubits are desintangled.)
 */
 static double optimization_problem( const gsl_vector* parameters, void* void_instance );
 
 
 /**
+@brief The optimization problem of the final optimization
+@param parameters A GNU Scientific Library vector containing the free parameters to be optimized.
+@param void_instance A void pointer pointing to the instance of the current class.
+@param grad A GNU Scientific Library vector containing the calculated gradient components.
+*/
+static Matrix_real optimization_problem_batch( int batchsize, const gsl_vector* parameters, void* void_instance );
+
+
+/**
 @brief Calculate the approximate derivative (f-f0)/(x-x0) of the cost function with respect to the free parameters.
 @param parameters A GNU Scientific Library vector containing the free parameters to be optimized.
 @param void_instance A void pointer pointing to the instance of the current class.
 @param grad A GNU Scientific Library vector containing the calculated gradient components.
 */
 static void optimization_problem_grad( const gsl_vector* parameters, void* void_instance, gsl_vector* grad );
 
@@ -247,24 +307,28 @@
 @param parameters A GNU Scientific Library vector containing the free parameters to be optimized.
 @param void_instance A void pointer pointing to the instance of the current class.
 @param f0 The value of the cost function at x0.
 @param grad A GNU Scientific Library vector containing the calculated gradient components.
 */
 static void optimization_problem_combined( const gsl_vector* parameters, void* void_instance, double* f0, gsl_vector* grad );
 
+static void optimization_problem_combined_unitary( const gsl_vector* parameters, void* void_instance, Matrix& Umtx, std::vector<Matrix>& Umtx_deriv );
 
 /**
 @brief Call to calculate both the cost function and the its gradient components.
 @param parameters The parameters for which the cost fuction shoule be calculated
 @param f0 The value of the cost function at x0.
 @param grad An array storing the calculated gradient components
 @param onlyCPU Set true to use only CPU in the calculations (has effect if compiled to use accelerator devices)
 */
 void optimization_problem_combined( const Matrix_real& parameters, double* f0, Matrix_real& grad );
 
+void optimization_problem_combined_unitary( const Matrix_real& parameters, Matrix& Umtx, std::vector<Matrix>& Umtx_deriv );
+
+Matrix_real optimization_problem_batch( Matrix_real batch );
 
 /**
 // @brief The optimization problem of the final optimization
 @param parameters A GNU Scientific Library containing the parameters to be optimized.
 @param void_instance A void pointer pointing to the instance of the current class.
 @return Returns with the cost function. (zero if the qubits are desintangled.)
 */
@@ -330,15 +394,15 @@
 void set_iteration_threshold_of_randomization( const unsigned long long& threshold  );
 
 
 
 /**
 @brief ?????????????
 */
-void set_iter_max( int iter_max_in  );
+void set_max_inner_iterations( int max_inner_iterations_in  );
 
 
 /**
 @brief ?????????????
 */
 void set_random_shift_count_max( int random_shift_count_max_in  );
 
@@ -356,27 +420,45 @@
 
 
 /**
 @brief ?????????????
 */
 void set_randomized_radius( double radius_in  );
 
+
+/**
+@brief Get the trace ffset used in the evaluation of the cost function
+*/
+int get_trace_offset();
+
+/**
+@brief Set the trace offset used in the evaluation of the cost function
+*/
+void set_trace_offset(int trace_offset_in);
+
+
+/**
+@brief Get the number of processed iterations during the optimization process
+*/
+int get_num_iters();
+
 #ifdef __DFE__
 
 /**
 @brief ?????????????
 */
 void upload_Umtx_to_DFE();
 
 
 /**
 @brief Get the number of accelerators to be reserved on DFEs on users demand.
 */
 int get_accelerator_num();
 
 
+
 #endif
 
 };
 
 
 #endif
```

### Comparing `squander-1.7.4/decomposition/include/N_Qubit_Decomposition_adaptive.h` & `squander-1.8.0/decomposition/include/N_Qubit_Decomposition_adaptive.h`

 * *Files 13% similar despite different names*

```diff
@@ -87,28 +87,30 @@
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
+@param compression_enabled_in Optional logical value. If True(1) begin decomposition function will compress the circuit. If False(0) it will not. Compression can still be called in seperate wrapper function. 
 @return An instance of the class
 */
-N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, int accelerator_num=0 );
+N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::map<std::string, Config_Element>& config, int accelerator_num=0 );
 
 
 /**
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
+@param compression_enabled Optional logical value. If True(1) begin decomposition function will compress the circuit. If False(0) it will not. Compression can still be called in seperate wrapper function. 
 @return An instance of the class
 */
-N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::vector<matrix_base<int>> topology_in, int accelerator_num=0 );
+N_Qubit_Decomposition_adaptive( Matrix Umtx_in, int qbit_num_in, int level_limit_in, int level_limit_min_in, std::vector<matrix_base<int>> topology_in, std::map<std::string, Config_Element>& config, int accelerator_num=0 );
 
 
 
 /**
 @brief Destructor of the class
 */
 virtual ~N_Qubit_Decomposition_adaptive();
@@ -118,14 +120,30 @@
 @brief Start the disentanglig process of the unitary
 @param finalize_decomp Optional logical parameter. If true (default), the decoupled qubits are rotated into state |0> when the disentangling of the qubits is done. Set to False to omit this procedure
 @param prepare_export Logical parameter. Set true to prepare the list of gates to be exported, or false otherwise.
 */
 virtual void start_decomposition(bool prepare_export=true);
 
 /**
+@brief get initial circuit
+*/
+virtual void get_initial_circuit();
+
+/**
+@brief Compress the circuit
+*/
+virtual void compress_circuit();
+
+/**
+@brief Finalize the circuit
+@param prepare_export Logical parameter. Set true to prepare the list of gates to be exported, or false otherwise.
+*/
+virtual void finalize_circuit(bool prepare_export=true);
+
+/**
 @brief ??????????????
 */
 Gates_block* optimize_imported_gate_structure(Matrix_real& optimized_parameters_mtx_loc);
 
 
 /**
 @brief ??????????????
@@ -138,15 +156,15 @@
 @brief ???????????????
 */
 Gates_block* compress_gate_structure( Gates_block* gate_structure );
 
 /**
 @brief ???????????????
 */
-Gates_block* compress_gate_structure( Gates_block* gate_structure, int layer_idx, Matrix_real& optimized_parameters, double& currnt_minimum_loc );
+Gates_block* compress_gate_structure( Gates_block* gate_structure, int layer_idx, Matrix_real& optimized_parameters, double& currnt_minimum_loc, int& iteration_num );
 
 /**
 @brief ???????????????
 */
 Gates_block* replace_trivial_CRY_gates( Gates_block* gate_structure, Matrix_real& optimized_parameters );
 
 /**
```

### Comparing `squander-1.7.4/decomposition/include/N_Qubit_Decomposition_custom.h` & `squander-1.8.0/decomposition/include/N_Qubit_Decomposition_custom.h`

 * *Files 5% similar despite different names*

```diff
@@ -56,15 +56,15 @@
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-N_Qubit_Decomposition_custom( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in, int accelerator_num=0 );
+N_Qubit_Decomposition_custom( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config, guess_type initial_guess_in, int accelerator_num=0 );
 
 
 
 /**
 @brief Destructor of the class
 */
 virtual ~N_Qubit_Decomposition_custom();
```

### Comparing `squander-1.7.4/decomposition/include/Sub_Matrix_Decomposition.h` & `squander-1.8.0/decomposition/include/Sub_Matrix_Decomposition.h`

 * *Files 2% similar despite different names*

```diff
@@ -64,15 +64,15 @@
 @brief Constructor of the class.
 @param Umtx_in The unitary matrix to be decomposed
 @param qbit_num_in The number of qubits spanning the unitary Umtx
 @param optimize_layer_num_in Optional logical value. If true, then the optimization tries to determine the lowest number of the layers needed for the decomposition. If False (default), the optimization is performed for the maximal number of layers.
 @param initial_guess_in Enumeration element indicating the method to guess initial values for the optimization. Possible values: 'zeros=0' ,'random=1', 'close_to_zero=2'
 @return An instance of the class
 */
-Sub_Matrix_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, guess_type initial_guess_in );
+Sub_Matrix_Decomposition( Matrix Umtx_in, int qbit_num_in, bool optimize_layer_num_in, std::map<std::string, Config_Element>& config_in, guess_type initial_guess_in );
 
 /**
 @brief Destructor of the class
 */
 ~Sub_Matrix_Decomposition();
```

### Comparing `squander-1.7.4/decomposition/include/Sub_Matrix_Decomposition_Cost_Function.h` & `squander-1.8.0/decomposition/include/Sub_Matrix_Decomposition_Cost_Function.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/Adaptive.cpp` & `squander-1.8.0/gates/Adaptive.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/CH.cpp` & `squander-1.8.0/gates/CH.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/CNOT.cpp` & `squander-1.8.0/gates/CNOT.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/CRY.cpp` & `squander-1.8.0/gates/CRY.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/CZ.cpp` & `squander-1.8.0/gates/CZ.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/Composite.cpp` & `squander-1.8.0/gates/Composite.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/Gate.cpp` & `squander-1.8.0/gates/Gate.cpp`

 * *Files 5% similar despite different names*

```diff
@@ -25,14 +25,15 @@
 #include "Gate.h"
 #include "common.h"
 
 #ifdef USE_AVX 
 #include "apply_kernel_to_input_AVX.h"
 #endif
 
+#include "apply_kernel_to_state_vector_input.h"
 
 /**
 @brief Deafult constructor of the class.
 @return An instance of the class
 */
 Gate::Gate() {
 
@@ -252,27 +253,47 @@
 /**
 @brief ???????????
 */
 void 
 Gate::apply_kernel_to(Matrix& u3_1qbit, Matrix& input, bool deriv) {
 
 
+    if ( input.cols == 1 && qbit_num<10 ) {
+        apply_kernel_to_state_vector_input_AVX(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
+        return;
+    }
+    else if ( input.cols == 1 ) {
+        apply_kernel_to_state_vector_input_parallel_AVX(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
+        return;
+    }
+
+
 #ifdef USE_AVX
 
-    apply_kernel_to_input_AVX(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
-    return;
+    if ( qbit_num < 4 ) {
+        apply_kernel_to_input_AVX_small(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
+        return;
+    }
+    else if ( qbit_num < 6 || (qbit_num < 10 && input.cols < 32) ) {
+        apply_kernel_to_input_AVX(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
+        return;
+     }
+    else {
+        apply_kernel_to_input_AVX_parallel(u3_1qbit, input, deriv, target_qbit, control_qbit, matrix_size);
+        return;
+     }
+
 
 #else
-    
+   
     int index_step_target = 1 << target_qbit;
     int current_idx = 0;
-    int current_idx_pair = current_idx+index_step_target;
 
 
-    while ( current_idx_pair < matrix_size ) {
+    for ( int current_idx_pair=current_idx + index_step_target; current_idx_pair<matrix_size; current_idx_pair=current_idx_pair+(index_step_target << 1) ) {
 
         for(int idx=0; idx<index_step_target; idx++) {  
         //tbb::parallel_for(0, index_step_target, 1, [&](int idx) {  
 
             int current_idx_loc = current_idx + idx;
             int current_idx_pair_loc = current_idx_pair + idx;
 
@@ -318,15 +339,14 @@
 
         
         //});
         }
 
 
         current_idx = current_idx + (index_step_target << 1);
-        current_idx_pair = current_idx_pair + (index_step_target << 1);
 
 
     }
 
 
 #endif // USE_AVX
```

### Comparing `squander-1.7.4/gates/Gates_block.cpp` & `squander-1.8.0/gates/Gates_block.cpp`

 * *Files 22% similar despite different names*

```diff
@@ -85,115 +85,30 @@
 void
 Gates_block::release_gates() {
 
     //free the alloctaed memory of the stored gates
     for(std::vector<Gate*>::iterator it = gates.begin(); it != gates.end(); ++it) {
 
         Gate* operation = *it;
-
-        if (operation->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_operation = static_cast<CNOT*>(operation);
-            delete cnot_operation;
-        }
-        else if (operation->get_type() == CZ_OPERATION) {
-            CZ* cz_operation = static_cast<CZ*>(operation);
-            delete cz_operation;
-        }
-        else if (operation->get_type() == CH_OPERATION) {
-            CH* ch_operation = static_cast<CH*>(operation);
-            delete ch_operation;
-        }
-        else if (operation->get_type() == SYC_OPERATION) {
-            SYC* syc_operation = static_cast<SYC*>(operation);
-            delete syc_operation;
-        }
-        else if (operation->get_type() == U3_OPERATION) {
-
-            U3* u3_operation = static_cast<U3*>(operation);
-            delete u3_operation;
-
-        }
-        else if (operation->get_type() == RY_OPERATION) {
-
-            RY* ry_operation = static_cast<RY*>(operation);
-            delete ry_operation;
-
-        }
-        else if (operation->get_type() == CRY_OPERATION) {
-
-            CRY* cry_operation = static_cast<CRY*>(operation);
-            delete cry_operation;
-
-        }
-        else if (operation->get_type() == RX_OPERATION) {
-
-            RX* rx_operation = static_cast<RX*>(operation);
-            delete rx_operation;
-
-        }
-        else if (operation->get_type() == RZ_OPERATION) {
-
-            RZ* rz_operation = static_cast<RZ*>(operation);
-            delete rz_operation;
-
-        }
-        else if (operation->get_type() == X_OPERATION) {
-
-            X* x_operation = static_cast<X*>(operation);
-            delete x_operation;
-
-        }
-        else if (operation->get_type() == Y_OPERATION) {
-
-            Y* y_operation = static_cast<Y*>(operation);
-            delete y_operation;
-
-        }
-        else if (operation->get_type() == Z_OPERATION) {
-
-            Z* z_operation = static_cast<Z*>(operation);
-            delete z_operation;
-
-        }
-        else if (operation->get_type() == SX_OPERATION) {
-
-            SX* sx_operation = static_cast<SX*>(operation);            
-            delete sx_operation;
-
-        }
-        else if (operation->get_type() == BLOCK_OPERATION) {
-
-            Gates_block* block_operation = static_cast<Gates_block*>(operation);
-            delete block_operation;
-
-        }
-        else if (operation->get_type() == GENERAL_OPERATION) {
+        switch (operation->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case U3_OPERATION: case RY_OPERATION:
+        case CRY_OPERATION: case RX_OPERATION:
+        case RZ_OPERATION: case X_OPERATION:
+        case Y_OPERATION: case Z_OPERATION:
+        case SX_OPERATION: case BLOCK_OPERATION:
+        case GENERAL_OPERATION: case UN_OPERATION:
+        case ON_OPERATION: case COMPOSITE_OPERATION:
+        case ADAPTIVE_OPERATION:
             delete operation;
-        }
-        else if (operation->get_type() == UN_OPERATION) {
-            UN* un_operation = static_cast<UN*>(operation);
-            delete un_operation;
-        }
-        else if (operation->get_type() == ON_OPERATION) {
-            ON* on_operation = static_cast<ON*>(operation);
-            delete on_operation;
-        }
-        else if (operation->get_type() == COMPOSITE_OPERATION) {
-            Composite* com_operation = static_cast<Composite*>(operation);
-            delete com_operation;
-        }
-        else if (operation->get_type() == ADAPTIVE_OPERATION) {
-
-            Adaptive* ad_operation = static_cast<Adaptive*>(operation);
-            delete ad_operation;
-
-        }
-        else {
+            break;
+        default:
             std::string err("Gates_block::release_gates(): unimplemented gate"); 
-            throw err;
+            throw err;        
         }
     }
     
     gates.clear();
     layer_num = 0;
     parameter_num = 0;
 
@@ -276,90 +191,73 @@
 
     for( int idx=gates.size()-1; idx>=0; idx--) {
 
         Gate* operation = gates[idx];
         parameters = parameters - operation->get_parameter_num();
         Matrix_real parameters_mtx(parameters, 1, operation->get_parameter_num());
 
-        if (operation->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_operation = static_cast<CNOT*>(operation);
-            cnot_operation->apply_to(input);
-        }
-        else if (operation->get_type() == CZ_OPERATION) {
-            CZ* cz_operation = static_cast<CZ*>(operation);
-            cz_operation->apply_to(input);
-        }
-        else if (operation->get_type() == CH_OPERATION) {
-            CH* ch_operation = static_cast<CH*>(operation);
-            ch_operation->apply_to(input);
-        }
-        else if (operation->get_type() == SYC_OPERATION) {
-            SYC* syc_operation = static_cast<SYC*>(operation);
-            syc_operation->apply_to(input);
-        }
-        else if (operation->get_type() == U3_OPERATION) {
+        switch (operation->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case X_OPERATION: case Y_OPERATION:
+        case Z_OPERATION: case SX_OPERATION:
+        case GENERAL_OPERATION:
+            operation->apply_to(input);
+            break;
+        case U3_OPERATION: {
             U3* u3_operation = static_cast<U3*>(operation);
-            u3_operation->apply_to( parameters_mtx, input );    
+            u3_operation->apply_to( parameters_mtx, input );
+            break;    
         }
-        else if (operation->get_type() == RX_OPERATION) {
+        case RX_OPERATION: {
             RX* rx_operation = static_cast<RX*>(operation);
-            rx_operation->apply_to( parameters_mtx, input ); 
+            rx_operation->apply_to( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == RY_OPERATION) {
+        case RY_OPERATION: {
             RY* ry_operation = static_cast<RY*>(operation);
-            ry_operation->apply_to( parameters_mtx, input ); 
+            ry_operation->apply_to( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == CRY_OPERATION) {
+        case CRY_OPERATION: {
             CRY* cry_operation = static_cast<CRY*>(operation);
             cry_operation->apply_to( parameters_mtx, input ); 
+            break;
         }
-        else if (operation->get_type() == RZ_OPERATION) {
+        case RZ_OPERATION: {
             RZ* rz_operation = static_cast<RZ*>(operation);
             rz_operation->apply_to( parameters_mtx, input ); 
-        }
-        else if (operation->get_type() == X_OPERATION) {
-            X* x_operation = static_cast<X*>(operation);
-            x_operation->apply_to( input ); 
-        }
-        else if (operation->get_type() == Y_OPERATION) {
-            Y* y_operation = static_cast<Y*>(operation);
-            y_operation->apply_to( input ); 
-        }
-        else if (operation->get_type() == Z_OPERATION) {
-            Z* z_operation = static_cast<Z*>(operation);
-            z_operation->apply_to( input ); 
-        }
-        else if (operation->get_type() == SX_OPERATION) {
-            SX* sx_operation = static_cast<SX*>(operation);
-            sx_operation->apply_to( input ); 
-        }
-        else if (operation->get_type() == GENERAL_OPERATION) {
-            operation->apply_to(input);
-        }
-        else if (operation->get_type() == UN_OPERATION) {
+            break;
+        }        
+        case UN_OPERATION: {
             UN* un_operation = static_cast<UN*>(operation);
             un_operation->apply_to(parameters_mtx, input);
+            break;
         }
-        else if (operation->get_type() == ON_OPERATION) {
+        case ON_OPERATION: {
             ON* on_operation = static_cast<ON*>(operation);
             on_operation->apply_to(parameters_mtx, input);
+            break;
         }
-        else if (operation->get_type() == BLOCK_OPERATION) {
+        case BLOCK_OPERATION: {
             Gates_block* block_operation = static_cast<Gates_block*>(operation);
             block_operation->apply_to(parameters_mtx, input);
+            break;
         }
-        else if (operation->get_type() == COMPOSITE_OPERATION) {
+        case COMPOSITE_OPERATION: {
             Composite* com_operation = static_cast<Composite*>(operation);
             com_operation->apply_to(parameters_mtx, input);
+            break;
         }
-        else if (operation->get_type() == ADAPTIVE_OPERATION) {
+        case ADAPTIVE_OPERATION: {
             Adaptive* ad_operation = static_cast<Adaptive*>(operation);
-            ad_operation->apply_to( parameters_mtx, input ); 
+            ad_operation->apply_to( parameters_mtx, input );
+            break; 
         }
-        else {
+        default:
             std::string err("Gates_block::apply_to: unimplemented gate"); 
             throw err;
         }
 
 #ifdef DEBUG
         if (input.isnan()) {
             std::stringstream sstream;
@@ -390,90 +288,73 @@
     double* parameters = parameters_mtx.get_data();
 
     for( int idx=0; idx<(int)gates.size(); idx++) {
 
         Gate* operation = gates[idx];
         Matrix_real parameters_mtx(parameters, 1, operation->get_parameter_num());
 
-        if (operation->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_operation = static_cast<CNOT*>(operation);
-            cnot_operation->apply_from_right(input);
-        }
-        else if (operation->get_type() == CZ_OPERATION) {
-            CZ* cz_operation = static_cast<CZ*>(operation);
-            cz_operation->apply_from_right(input);
-        }
-        else if (operation->get_type() == CH_OPERATION) {
-            CH* ch_operation = static_cast<CH*>(operation);
-            ch_operation->apply_from_right(input);
-        }
-        else if (operation->get_type() == SYC_OPERATION) {
-            SYC* syc_operation = static_cast<SYC*>(operation);
-            syc_operation->apply_from_right(input);
-        }
-        else if (operation->get_type() == U3_OPERATION) {
+        switch (operation->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case X_OPERATION: case Y_OPERATION:
+        case Z_OPERATION: case SX_OPERATION:
+        case GENERAL_OPERATION:
+            operation->apply_from_right(input);
+            break;
+        case U3_OPERATION: {
             U3* u3_operation = static_cast<U3*>(operation);
-            u3_operation->apply_from_right( parameters_mtx, input ); 
+            u3_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == RX_OPERATION) {
+        case RX_OPERATION: {
             RX* rx_operation = static_cast<RX*>(operation);
-            rx_operation->apply_from_right( parameters_mtx, input ); 
+            rx_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == RY_OPERATION) {
+        case RY_OPERATION: {
             RY* ry_operation = static_cast<RY*>(operation);
-            ry_operation->apply_from_right( parameters_mtx, input ); 
+            ry_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == CRY_OPERATION) {
+        case CRY_OPERATION: {
             CRY* cry_operation = static_cast<CRY*>(operation);
-            cry_operation->apply_from_right( parameters_mtx, input ); 
+            cry_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == RZ_OPERATION) {
+        case RZ_OPERATION: {
             RZ* rz_operation = static_cast<RZ*>(operation);
-            rz_operation->apply_from_right( parameters_mtx, input );         
-        }
-        else if (operation->get_type() == X_OPERATION) {
-            X* x_operation = static_cast<X*>(operation);
-            x_operation->apply_from_right( input ); 
-        }
-        else if (operation->get_type() == Y_OPERATION) {
-            Y* y_operation = static_cast<Y*>(operation);
-            y_operation->apply_from_right( input ); 
-        }
-        else if (operation->get_type() == Z_OPERATION) {
-            Z* z_operation = static_cast<Z*>(operation);
-            z_operation->apply_from_right( input ); 
+            rz_operation->apply_from_right( parameters_mtx, input );
+            break;         
         }
-        else if (operation->get_type() == SX_OPERATION) {
-            SX* sx_operation = static_cast<SX*>(operation);
-            sx_operation->apply_from_right( input ); 
-        }
-        else if (operation->get_type() == GENERAL_OPERATION) {
-            operation->apply_from_right(input);
-        }
-        else if (operation->get_type() == UN_OPERATION) {
+        case UN_OPERATION: {
             UN* un_operation = static_cast<UN*>(operation);
-            un_operation->apply_from_right( parameters_mtx, input ); 
+            un_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == ON_OPERATION) {
+        case ON_OPERATION: {
             ON* on_operation = static_cast<ON*>(operation);
-            on_operation->apply_from_right( parameters_mtx, input ); 
+            on_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == BLOCK_OPERATION) {
+        case BLOCK_OPERATION: {
             Gates_block* block_operation = static_cast<Gates_block*>(operation);
             block_operation->apply_from_right(parameters_mtx, input);
+            break;
         }
-        else if (operation->get_type() == COMPOSITE_OPERATION) {
+        case COMPOSITE_OPERATION: {
             Composite* com_operation = static_cast<Composite*>(operation);
-            com_operation->apply_from_right( parameters_mtx, input ); 
+            com_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else if (operation->get_type() == ADAPTIVE_OPERATION) {
+        case ADAPTIVE_OPERATION: {
             Adaptive* ad_operation = static_cast<Adaptive*>(operation);
-            ad_operation->apply_from_right( parameters_mtx, input ); 
+            ad_operation->apply_from_right( parameters_mtx, input );
+            break; 
         }
-        else {
+        default:
             std::string err("Gates_block::apply_from_right: unimplemented gate"); 
             throw err;
         }
 
         parameters = parameters + operation->get_parameter_num();
 
 #ifdef DEBUG
@@ -1512,14 +1393,71 @@
 @brief Call to get the number of free parameters
 @return Return with the number of parameters of the gates grouped in the gate block.
 */
 int Gates_block::get_parameter_num() {
     return parameter_num;
 }
 
+void Gates_block::get_parameter_max(Matrix_real &range_max) {
+    int parameter_idx = parameter_num;
+	double *data = range_max.get_data();
+        for(int op_idx = gates.size()-1; op_idx>=0; op_idx--) {
+
+            Gate* gate = gates[op_idx];
+            switch (gate->get_type()) {
+            case U3_OPERATION: {
+                U3* u3_gate = static_cast<U3*>(gate);
+
+                if ((u3_gate->get_parameter_num() == 1) && u3_gate->is_theta_parameter()) {
+		            data[parameter_idx-1] = 4 * M_PI;
+                    parameter_idx = parameter_idx - 1;
+
+                }
+                else if ((u3_gate->get_parameter_num() == 1) && (u3_gate->is_phi_parameter() || u3_gate->is_lambda_parameter())) {
+                    data[parameter_idx-1] = 2 * M_PI;
+                    parameter_idx = parameter_idx - 1;
+                }
+                else if ((u3_gate->get_parameter_num() == 2) && u3_gate->is_theta_parameter() && (u3_gate->is_phi_parameter() || u3_gate->is_lambda_parameter())) {
+                    data[parameter_idx-2] = 4 * M_PI;
+                    data[parameter_idx-1] = 2 * M_PI;
+                    parameter_idx = parameter_idx - 2;
+                }
+                else if ((u3_gate->get_parameter_num() == 2) && u3_gate->is_phi_parameter() && u3_gate->is_lambda_parameter() ) {
+                    data[parameter_idx-2] = 2 * M_PI;
+                    data[parameter_idx-1] = 2 * M_PI;
+                    parameter_idx = parameter_idx - 2;
+                }
+                else if ((u3_gate->get_parameter_num() == 3)) {
+                    data[parameter_idx-3] = 4 * M_PI;
+                    data[parameter_idx-2] = 2 * M_PI;
+                    data[parameter_idx-1] = 2 * M_PI;
+                    parameter_idx = parameter_idx - 3;
+                }
+                break; }
+            case RX_OPERATION:
+            case RY_OPERATION:
+            case CRY_OPERATION:
+            case ADAPTIVE_OPERATION:
+                data[parameter_idx-1] = 4 * M_PI;
+                parameter_idx = parameter_idx - 1;
+                break;
+            case BLOCK_OPERATION: {
+                Gates_block* block_gate = static_cast<Gates_block*>(gate);
+                Matrix_real parameters_layer(range_max.get_data() + parameter_idx - gate->get_parameter_num(), 1, gate->get_parameter_num() );
+                block_gate->get_parameter_max( parameters_layer );
+                parameter_idx = parameter_idx - block_gate->get_parameter_num();
+                break; }
+            default:
+                for (int i = 0; i < gate->get_parameter_num(); i++)
+                    data[parameter_idx-1-i] = 2 * M_PI;    
+                parameter_idx = parameter_idx - gate->get_parameter_num();
+            }
+        }
+}
+
 
 /**
 @brief Call to get the number of gates grouped in the class
 @return Return with the number of the gates grouped in the gate block.
 */
 int Gates_block::get_gate_num() {
     return gates.size();
@@ -1586,15 +1524,15 @@
 		
                 // get the inverse parameters of the U3 rotation
 
                 U3* u3_gate = static_cast<U3*>(gate);
 
                 if ((u3_gate->get_parameter_num() == 1) && u3_gate->is_theta_parameter()) {
 		   
-                    varphi = std::fmod( parameters_data[parameter_idx-1], 4*M_PI);
+                    vartheta = std::fmod( 2*parameters_data[parameter_idx-1], 4*M_PI);
                     varphi = 0;
                     varlambda =0;
                     parameter_idx = parameter_idx - 1;
 
                 }
                 else if ((u3_gate->get_parameter_num() == 1) && u3_gate->is_phi_parameter()) {
                     vartheta = 0;
@@ -1666,22 +1604,22 @@
 		std::stringstream sstream;
 		sstream << gate_idx << "th gate: RY on target qubit: " << ry_gate->get_target_qbit() << " and with parameters theta = " << vartheta << std::endl; 
 		print(sstream, 1);	    	
                 gate_idx = gate_idx + 1;
             }
             else if (gate->get_type() == CRY_OPERATION) {
                 // definig the rotation parameter
-                double Phi;
+                double vartheta;
                 // get the inverse parameters of the U3 rotation
                 CRY* cry_gate = static_cast<CRY*>(gate);
-                Phi = std::fmod( parameters_data[parameter_idx-1], 2*M_PI);
+                vartheta = std::fmod( 2*parameters_data[parameter_idx-1], 4*M_PI);
                 parameter_idx = parameter_idx - 1;
 
 		std::stringstream sstream;
-		sstream << gate_idx << "th gate: CRY on target qubit: " << cry_gate->get_target_qbit() << ", control qubit" << cry_gate->get_control_qbit() << " and with parameters Phi = " << Phi << std::endl;
+		sstream << gate_idx << "th gate: CRY on target qubit: " << cry_gate->get_target_qbit() << ", control qubit" << cry_gate->get_control_qbit() << " and with parameters theta = " << vartheta << std::endl;
 		print(sstream, 1);	    		                    
                 gate_idx = gate_idx + 1;
             }
             else if (gate->get_type() == RZ_OPERATION) {
                 // definig the rotation parameter
                 double varphi;
                 // get the inverse parameters of the U3 rotation
@@ -1758,15 +1696,15 @@
                 gate_idx = gate_idx + 1;
             }
             else if (gate->get_type() == ADAPTIVE_OPERATION) {
                 // definig the rotation parameter
                 double Theta;
                 // get the inverse parameters of the U3 rotation
                 Adaptive* ad_gate = static_cast<Adaptive*>(gate);
-                Theta = std::fmod( parameters_data[parameter_idx-1], 2*M_PI);
+                Theta = std::fmod( 2*parameters_data[parameter_idx-1], 4*M_PI);
                 parameter_idx = parameter_idx - 1;
 
 		std::stringstream sstream;
 		sstream << gate_idx << "th gate: Adaptive gate on target qubit: " << ad_gate->get_target_qbit() << ", control qubit " << ad_gate->get_control_qbit() << " and with parameters Theta = " << Theta << std::endl;
 		print(sstream, 1);	    	
                 gate_idx = gate_idx + 1;
             }
@@ -1937,128 +1875,29 @@
 void Gates_block::combine(Gates_block* op_block) {
 
     // getting the list of gates
     std::vector<Gate*> gates_in = op_block->get_gates();
 
     for(std::vector<Gate*>::iterator it = (gates_in).begin(); it != (gates_in).end(); ++it) {
         Gate* op = *it;
-
-        if (op->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_op = static_cast<CNOT*>( op );
-            CNOT* cnot_op_cloned = cnot_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cnot_op_cloned );
-            add_gate_to_end(op_cloned);
-        }
-        else if (op->get_type() == CZ_OPERATION) {
-            CZ* cz_op = static_cast<CZ*>( op );
-            CZ* cz_op_cloned = cz_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cz_op_cloned );
-            add_gate_to_end(op_cloned);
-        }
-        else if (op->get_type() == CH_OPERATION) {
-            CH* ch_op = static_cast<CH*>( op );
-            CH* ch_op_cloned = ch_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ch_op_cloned );
-            add_gate_to_end(op_cloned);
-        }
-        else if (op->get_type() == SYC_OPERATION) {
-            SYC* syc_op = static_cast<SYC*>( op );
-            SYC* syc_op_cloned = syc_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( syc_op_cloned );
-            add_gate_to_end(op_cloned);
-        }
-        else if (op->get_type() == U3_OPERATION) {
-            U3* u3_op = static_cast<U3*>( op );
-            U3* u3_op_cloned = u3_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( u3_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RX_OPERATION) {
-            RX* rx_op = static_cast<RX*>( op );
-            RX* rx_op_cloned = rx_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( rx_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RY_OPERATION) {
-            RY* ry_op = static_cast<RY*>( op );
-            RY* ry_op_cloned = ry_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ry_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == CRY_OPERATION) {
-            CRY* cry_op = static_cast<CRY*>( op );
-            CRY* cry_op_cloned = cry_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cry_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RZ_OPERATION) {
-            RZ* rz_op = static_cast<RZ*>( op );
-            RZ* rz_op_cloned = rz_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( rz_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == X_OPERATION) {
-            X* x_op = static_cast<X*>( op );
-            X* x_op_cloned = x_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( x_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == Y_OPERATION) {
-            Y* y_op = static_cast<Y*>( op );
-            Y* y_op_cloned = y_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( y_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == Z_OPERATION) {
-            Z* z_op = static_cast<Z*>( op );
-            Z* z_op_cloned = z_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( z_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == SX_OPERATION) {
-            SX* sx_op = static_cast<SX*>( op );
-            SX* sx_op_cloned = sx_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( sx_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == BLOCK_OPERATION) {
-            Gates_block* block_op = static_cast<Gates_block*>( op );
-            Gates_block* block_op_cloned = block_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( block_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == GENERAL_OPERATION) {
+        switch (op->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case U3_OPERATION: case RY_OPERATION:
+        case CRY_OPERATION: case RX_OPERATION:
+        case RZ_OPERATION: case X_OPERATION:
+        case Y_OPERATION: case Z_OPERATION:
+        case SX_OPERATION: case BLOCK_OPERATION:
+        case GENERAL_OPERATION: case UN_OPERATION:
+        case ON_OPERATION: case COMPOSITE_OPERATION:
+        case ADAPTIVE_OPERATION: {
             Gate* op_cloned = op->clone();
             add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == UN_OPERATION) {
-            UN* un_op = static_cast<UN*>( op );
-            UN* un_op_cloned = un_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( un_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == ON_OPERATION) {
-            ON* on_op = static_cast<ON*>( op );
-            ON* on_op_cloned = on_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( on_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == COMPOSITE_OPERATION) {
-            Composite* com_op = static_cast<Composite*>( op );
-            Composite* com_op_cloned = com_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( com_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == ADAPTIVE_OPERATION) {
-            Adaptive* ad_op = static_cast<Adaptive*>( op );
-            Adaptive* ad_op_cloned = ad_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ad_op_cloned );
-            add_gate_to_end( op_cloned );
-        }
-        else {
+            break; }
+        default:
             std::string err("Gates_block::combine: unimplemented gate"); 
             throw err;
         }
 
     }
 
 }
@@ -2072,91 +1911,28 @@
 
     // setting the number of qubits
     Gate::set_qbit_num(qbit_num_in);
 
     // setting the number of qubit in the gates
     for(std::vector<Gate*>::iterator it = gates.begin(); it != gates.end(); ++it) {
         Gate* op = *it;
-
-        if (op->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_op = static_cast<CNOT*>( op );
-            cnot_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == CZ_OPERATION) {
-            CZ* cz_op = static_cast<CZ*>( op );
-            cz_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == CH_OPERATION) {
-            CH* ch_op = static_cast<CH*>( op );
-            ch_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == SYC_OPERATION) {
-            SYC* syc_op = static_cast<SYC*>( op );
-            syc_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == U3_OPERATION) {
-            U3* u3_op = static_cast<U3*>( op );
-            u3_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == RX_OPERATION) {
-            RX* rx_op = static_cast<RX*>( op );
-            rx_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == RY_OPERATION) {
-            RY* ry_op = static_cast<RY*>( op );
-            ry_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == CRY_OPERATION) {
-            CRY* cry_op = static_cast<CRY*>( op );
-            cry_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == RZ_OPERATION) {
-            RZ* rz_op = static_cast<RZ*>( op );
-            rz_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == X_OPERATION) {
-            X* x_op = static_cast<X*>( op );
-            x_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == Y_OPERATION) {
-            Y* y_op = static_cast<Y*>( op );
-            y_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == Z_OPERATION) {
-            Z* z_op = static_cast<Z*>( op );
-            z_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == SX_OPERATION) {
-            SX* sx_op = static_cast<SX*>( op );
-            sx_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == BLOCK_OPERATION) {
-            Gates_block* block_op = static_cast<Gates_block*>( op );
-            block_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == UN_OPERATION) {
-            UN* un_op = static_cast<UN*>( op );
-            un_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == ON_OPERATION) {
-            ON* on_op = static_cast<ON*>( op );
-            on_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == COMPOSITE_OPERATION) {
-            Composite* com_op = static_cast<Composite*>( op );
-            com_op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == GENERAL_OPERATION) {
+        switch (op->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case U3_OPERATION: case RY_OPERATION:
+        case CRY_OPERATION: case RX_OPERATION:
+        case RZ_OPERATION: case X_OPERATION:
+        case Y_OPERATION: case Z_OPERATION:
+        case SX_OPERATION: case BLOCK_OPERATION:
+        case GENERAL_OPERATION: case UN_OPERATION:
+        case ON_OPERATION: case COMPOSITE_OPERATION:
+        case ADAPTIVE_OPERATION:
             op->set_qbit_num( qbit_num_in );
-        }
-        else if (op->get_type() == ADAPTIVE_OPERATION) {
-            Adaptive* ad_op = static_cast<Adaptive*>( op );
-            ad_op->set_qbit_num( qbit_num_in );
-        }
-        else {
+            break;
+        default:
             std::string err("Gates_block::set_qbit_num: unimplemented gate"); 
             throw err;
         }
     }
 }
 
 
@@ -2189,134 +1965,35 @@
 */
 int Gates_block::extract_gates( Gates_block* op_block ) {
 
     op_block->release_gates();
 
     for ( std::vector<Gate*>::iterator it=gates.begin(); it != gates.end(); ++it ) {
         Gate* op = *it;
-
-        if (op->get_type() == CNOT_OPERATION) {
-            CNOT* cnot_op = static_cast<CNOT*>( op );
-            CNOT* cnot_op_cloned = cnot_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cnot_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == CZ_OPERATION) {
-            CZ* cz_op = static_cast<CZ*>( op );
-            CZ* cz_op_cloned = cz_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cz_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == CH_OPERATION) {
-            CH* ch_op = static_cast<CH*>( op );
-            CH* ch_op_cloned = ch_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ch_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == SYC_OPERATION) {
-            SYC* syc_op = static_cast<SYC*>( op );
-            SYC* syc_op_cloned = syc_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( syc_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == U3_OPERATION) {
-            U3* u3_op = static_cast<U3*>( op );
-            U3* u3_op_cloned = u3_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( u3_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RX_OPERATION) {
-            RX* rx_op = static_cast<RX*>( op );
-            RX* rx_op_cloned = rx_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( rx_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RY_OPERATION) {
-            RY* ry_op = static_cast<RY*>( op );
-            RY* ry_op_cloned = ry_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ry_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == CRY_OPERATION) {
-            CRY* cry_op = static_cast<CRY*>( op );
-            CRY* cry_op_cloned = cry_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( cry_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == RZ_OPERATION) {
-            RZ* rz_op = static_cast<RZ*>( op );
-            RZ* rz_op_cloned = rz_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( rz_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == X_OPERATION) {
-            X* x_op = static_cast<X*>( op );
-            X* x_op_cloned = x_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( x_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == Y_OPERATION) {
-            Y* y_op = static_cast<Y*>( op );
-            Y* y_op_cloned = y_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( y_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == Z_OPERATION) {
-            Z* z_op = static_cast<Z*>( op );
-            Z* z_op_cloned = z_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( z_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == SX_OPERATION) {
-            SX* sx_op = static_cast<SX*>( op );
-            SX* sx_op_cloned = sx_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( sx_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == BLOCK_OPERATION) {
-            Gates_block* block_op = static_cast<Gates_block*>( op );
-            Gates_block* block_op_cloned = block_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( block_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == UN_OPERATION) {
-            UN* un_op = static_cast<UN*>( op );
-            UN* un_op_cloned = un_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( un_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == ON_OPERATION) {
-            ON* on_op = static_cast<ON*>( op );
-            ON* on_op_cloned = on_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( on_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == COMPOSITE_OPERATION) {
-            Composite* com_op = static_cast<Composite*>( op );
-            Composite* com_op_cloned = com_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( com_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == GENERAL_OPERATION) {
+        switch (op->get_type()) {
+        case CNOT_OPERATION: case CZ_OPERATION:
+        case CH_OPERATION: case SYC_OPERATION:
+        case U3_OPERATION: case RY_OPERATION:
+        case CRY_OPERATION: case RX_OPERATION:
+        case RZ_OPERATION: case X_OPERATION:
+        case Y_OPERATION: case Z_OPERATION:
+        case SX_OPERATION: case BLOCK_OPERATION:
+        case GENERAL_OPERATION: case UN_OPERATION:
+        case ON_OPERATION: case COMPOSITE_OPERATION:
+        case ADAPTIVE_OPERATION: {
             Gate* op_cloned = op->clone();
             op_block->add_gate_to_end( op_cloned );
-        }
-        else if (op->get_type() == ADAPTIVE_OPERATION) {
-            Adaptive* ad_op = static_cast<Adaptive*>( op );
-            Adaptive* ad_op_cloned = ad_op->clone();
-            Gate* op_cloned = static_cast<Gate*>( ad_op_cloned );
-            op_block->add_gate_to_end( op_cloned );
-        }
-        else {
+            break; }
+        default:
             std::string err("Gates_block::extract_gates: unimplemented gate"); 
             throw err;
         }
 
     }
-
+    
     return 0;
 
 }
 
 
 
 /**
@@ -2721,14 +2398,92 @@
 }
 
 
 /**
 @brief Method to create random initial parameters for the optimization
 @return 
 */
+DFEgate_kernel_type* 
+Gates_block::convert_to_batched_DFE_gates( std::vector<Matrix_real>& parameters_mtx_vec, int& gatesNum, int& gateSetNum, int& redundantGateSets ) {
+
+
+    gates_num gate_nums   = get_gate_nums();
+    int gates_total_num   = gate_nums.total; 
+    int chained_gates_num = get_chained_gates_num();
+    int gate_padding      = gates_total_num % chained_gates_num == 0 ? 0 : chained_gates_num - (gates_total_num % chained_gates_num);
+    gatesNum              = gates_total_num+gate_padding;
+/*
+std::cout << "chained gates num: " << chained_gates_num << std::endl;
+std::cout << "number of gates: " << gatesNum << std::endl;
+*/
+
+
+    gateSetNum = parameters_mtx_vec.size();
+
+#ifdef __MPI__
+    int rem = gateSetNum % (4 * world_size );
+    if ( rem == 0 ) {
+        redundantGateSets = 0;
+    }
+    else {
+        redundantGateSets = (4 * world_size ) - (gateSetNum % (4 * world_size ));
+        gateSetNum = gateSetNum + redundantGateSets;
+    }
+#else
+    int rem = gateSetNum % 4;
+    if ( rem == 0 ) {
+        redundantGateSets = 0;
+    }
+    else {
+        redundantGateSets = 4 - (gateSetNum % 4);
+        gateSetNum = gateSetNum + redundantGateSets;
+    }
+#endif
+
+    DFEgate_kernel_type* DFEgates = new DFEgate_kernel_type[gatesNum*gateSetNum];
+
+
+    tbb::parallel_for( 0, gateSetNum, 1, [&](int gateset_idx) {
+    
+        int gate_idx = gateset_idx * gatesNum;
+
+        if ( gateset_idx < parameters_mtx_vec.size() ) {
+            Matrix_real& parameters_mtx = parameters_mtx_vec[gateset_idx];
+            convert_to_DFE_gates( parameters_mtx, DFEgates, gate_idx );
+        }
+
+        // padding with identity gates
+        for (int idx=gate_idx; idx<(gateset_idx+1)*gatesNum; idx++ ){
+
+            DFEgate_kernel_type& DFEGate = DFEgates[idx];
+
+        
+            DFEGate.target_qbit = 0;
+            DFEGate.control_qbit = -1;
+            DFEGate.gate_type = U3_OPERATION;
+            DFEGate.ThetaOver2 = (int32_t)(0);
+            DFEGate.Phi = (int32_t)(0);
+            DFEGate.Lambda = (int32_t)(0); 
+            DFEGate.metadata = 0;
+
+            gate_idx++;
+
+        }
+
+    });
+    
+
+    return DFEgates;
+
+}
+
+/**
+@brief Method to create random initial parameters for the optimization
+@return 
+*/
 DFEgate_kernel_type* Gates_block::convert_to_DFE_gates( Matrix_real& parameters_mtx, int& gatesNum ) {
 
     int parameter_num = get_parameter_num();
     if ( parameter_num != parameters_mtx.size() ) {
         std::string error("N_Qubit_Decomposition_Base::convert_to_DFE_gates: wrong number of parameters");
         throw error;
     }
@@ -3474,16 +3229,15 @@
             fread_status = fread(&parameter_num_loc, sizeof(int), 1, pFile);
             //std::cout << "parameter_num_loc: " << parameter_num_loc << std::endl;
         
 
             int gates_num_loc;
             fread_status = fread(&gates_num_loc, sizeof(int), 1, pFile);
             //std::cout << "gates_num_loc: " << gates_num_loc << std::endl;
-            
-            gate_block_levels[ current_level ]->add_gate_to_end( static_cast<Gate*>(gate_block_inner) );
+                        
             gate_block_levels.push_back( gate_block_inner );
             gate_block_level_gates_num.push_back(gates_num_loc);
             current_level++;
         }
         else if (gt_type == ADAPTIVE_OPERATION) {
 
             sstream << "importing adaptive gate" << std::endl;
@@ -3506,14 +3260,15 @@
         else {
             std::string err("import_gate_list_from_binary: unimplemented gate"); 
             throw err;
         }
 
 
         if ( gate_block_level_gates_num[current_level] == 0 ) {
+            gate_block_levels[ current_level-1 ]->add_gate_to_end( static_cast<Gate*>(gate_block_levels[ current_level ]) );
             gate_block_levels.pop_back();
             gate_block_level_gates_num.pop_back();
             current_level--;
             gate_block_level_gates_num[current_level]--;
             sstream << "finishing gates block" << std::endl;
         }
```

### Comparing `squander-1.7.4/gates/ON.cpp` & `squander-1.8.0/gates/ON.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/RX.cpp` & `squander-1.8.0/gates/RX.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/RY.cpp` & `squander-1.8.0/gates/RY.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/RZ.cpp` & `squander-1.8.0/gates/RZ.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/SX.cpp` & `squander-1.8.0/gates/SX.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/SYC.cpp` & `squander-1.8.0/gates/SYC.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/U3.cpp` & `squander-1.8.0/gates/U3.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/UN.cpp` & `squander-1.8.0/gates/UN.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/X.cpp` & `squander-1.8.0/gates/X.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/Y.cpp` & `squander-1.8.0/gates/Y.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/Z.cpp` & `squander-1.8.0/gates/Z.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/Adaptive.h` & `squander-1.8.0/gates/include/Adaptive.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/CH.h` & `squander-1.8.0/gates/include/CH.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/CNOT.h` & `squander-1.8.0/gates/include/CNOT.h`

 * *Files 4% similar despite different names*

```diff
@@ -53,50 +53,50 @@
 @param control_qbit_in The identification number of the control qubit. (0 <= target_qbit <= qbit_num-1)
 */
 CNOT(int qbit_num_in, int target_qbit_in,  int control_qbit_in);
 
 /**
 @brief Destructor of the class
 */
-~CNOT();
+virtual ~CNOT();
 
 /**
 @brief Call to retrieve the operation matrix
 @return Returns with the matrix of the operation
 */
 Matrix get_matrix();
 
 /**
 @brief Call to apply the gate on the input array/matrix by CNOT*input
 @param input The input array on which the gate is applied
 */
-void apply_to( Matrix& input );
+virtual void apply_to( Matrix& input );
 
 
 /**
 @brief Call to apply the gate on the input array/matrix by input*CNOT
 @param input The input array on which the gate is applied
 */
-void apply_from_right( Matrix& input );
+virtual void apply_from_right( Matrix& input );
 
 
 /**
 @brief Call to set the number of qubits spanning the matrix of the operation
 @param qbit_num The number of qubits
 */
-void set_qbit_num(int qbit_num);
+virtual void set_qbit_num(int qbit_num);
 
 /**
 @brief Call to reorder the qubits in the matrix of the operation
 @param qbit_list The reordered list of qubits spanning the matrix
 */
-void reorder_qubits( std::vector<int> qbit_list);
+virtual void reorder_qubits( std::vector<int> qbit_list);
 
 /**
 @brief Call to create a clone of the present class
 @return Return with a pointer pointing to the cloned object
 */
-CNOT* clone();
+virtual CNOT* clone();
 
 };
 
 #endif //CNOT
```

### Comparing `squander-1.7.4/gates/include/CRY.h` & `squander-1.8.0/gates/include/CRY.h`

 * *Files 2% similar despite different names*

```diff
@@ -54,15 +54,15 @@
 @param lambda_in logical value indicating whether the matrix creation takes an argument lambda
 */
 CRY(int qbit_num_in, int target_qbit_in, int control_qbit_in);
 
 /**
 @brief Destructor of the class
 */
-~CRY();
+virtual ~CRY();
 
 /**
 @brief Call to retrieve the gate matrix
 @param parameters An array of parameters to calculate the matrix of the U3 gate.
 @return Returns with a matrix of the gate
 */
 //Matrix get_matrix( const double* parameters );
@@ -101,14 +101,14 @@
 */
 Matrix_real get_optimized_parameters();
 
 /**
 @brief Call to create a clone of the present class
 @return Return with a pointer pointing to the cloned object
 */
-CRY* clone();
+virtual CRY* clone();
 
 };
 
 
 #endif //CRY
```

### Comparing `squander-1.7.4/gates/include/CZ.h` & `squander-1.8.0/gates/include/CZ.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/Composite.h` & `squander-1.8.0/gates/include/Composite.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/Gate.h` & `squander-1.8.0/gates/include/Gate.h`

 * *Files 2% similar despite different names*

```diff
@@ -163,15 +163,15 @@
 */
 int get_qbit_num();
 
 /**
 @brief Call to create a clone of the present class
 @return Return with a pointer pointing to the cloned object
 */
-Gate* clone();
+virtual Gate* clone();
 
 protected:
 /**
 @brief ???????????
 */
 void apply_kernel_to( Matrix& u3_1qbit, Matrix& input, bool deriv=false );
```

### Comparing `squander-1.7.4/gates/include/Gates_block.h` & `squander-1.8.0/gates/include/Gates_block.h`

 * *Files 1% similar despite different names*

```diff
@@ -91,28 +91,28 @@
 void apply_to_list( Matrix_real& parameters, std::vector<Matrix> input );
 
 /**
 @brief Call to apply the gate on the input array/matrix Gates_block*input
 @param parameters An array of parameters to calculate the matrix of the U3 gate.
 @param input The input array on which the gate is applied
 */
-void apply_to( Matrix_real& parameters_mtx, Matrix& input );
+virtual void apply_to( Matrix_real& parameters_mtx, Matrix& input );
 
 
 /**
 @brief Call to apply the gate on the input array/matrix by input*CNOT
 @param input The input array on which the gate is applied
 */
-void apply_from_right( Matrix_real& parameters_mtx, Matrix& input );
+virtual void apply_from_right( Matrix_real& parameters_mtx, Matrix& input );
 
 
 /**
 @brief ???????????????
 */
-std::vector<Matrix> apply_derivate_to( Matrix_real& parameters_mtx, Matrix& input );
+virtual std::vector<Matrix> apply_derivate_to( Matrix_real& parameters_mtx, Matrix& input );
 
 
 
 
 /**
 @brief Append a U3 gate to the list of gates
 @param target_qbit The identification number of the targt qubit. (0 <= target_qbit <= qbit_num-1)
@@ -399,14 +399,15 @@
 
 /**
 @brief Call to get the number of free parameters
 @return Return with the number of parameters of the gates grouped in the gate block.
 */
 int get_parameter_num();
 
+void get_parameter_max(Matrix_real &range_max);
 
 /**
 @brief Call to get the number of gates grouped in the class
 @return Return with the number of the gates grouped in the gate block.
 */
 int get_gate_num();
 
@@ -419,15 +420,15 @@
 void list_gates( const Matrix_real &parameters, int start_index );
 
 
 /**
 @brief Call to reorder the qubits in the matrix of the gates
 @param qbit_list The reordered list of qubits spanning the matrix
 */
-void reorder_qubits( std::vector<int> qbit_list );
+virtual void reorder_qubits( std::vector<int> qbit_list );
 
 
 /**
 @brief Call to get the qubits involved in the gates stored in the block of gates.
 @return Return with a list of the invovled qubits
 */
 std::vector<int> get_involved_qubits();
@@ -452,22 +453,22 @@
 void combine(Gates_block* op_block);
 
 
 /**
 @brief Set the number of qubits spanning the matrix of the gates stored in the block of gates.
 @param qbit_num_in The number of qubits spanning the matrices.
 */
-void set_qbit_num( int qbit_num_in );
+virtual void set_qbit_num( int qbit_num_in );
 
 
 /**
 @brief Create a clone of the present class.
 @return Return with a pointer pointing to the cloned object.
 */
-Gates_block* clone();
+virtual Gates_block* clone();
 
 /**
 @brief Call to extract the gates stored in the class.
 @param op_block An instance of Gates_block class in which the gates will be stored. (The current gates will be erased)
 @return Return with 0 on success.
 */
 int extract_gates( Gates_block* op_block );
@@ -503,14 +504,21 @@
 
 /**
 @brief Method to create random initial parameters for the optimization
 @return 
 */
 void adjust_parameters_for_derivation( DFEgate_kernel_type* DFEgates, const int  gatesNum, int& gate_idx, int& gate_set_index );
 
+/**
+@brief Method to create random initial parameters for the optimization
+@return 
+*/
+DFEgate_kernel_type* convert_to_batched_DFE_gates( std::vector<Matrix_real>& parameters_mtx_vec, int& gatesNum, int& gateSetNum, int& redundantGateSets );
+
+
 
 /**
 @brief Method to create random initial parameters for the optimization
 @return 
 */
 DFEgate_kernel_type* convert_to_DFE_gates( Matrix_real& parameters_mtx, int& gatesNum );
```

### Comparing `squander-1.7.4/gates/include/ON.h` & `squander-1.8.0/gates/include/ON.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/RX.h` & `squander-1.8.0/gates/include/RX.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/RY.h` & `squander-1.8.0/gates/include/RY.h`

 * *Files 0% similar despite different names*

```diff
@@ -99,14 +99,14 @@
 */
 Matrix_real get_optimized_parameters();
 
 /**
 @brief Call to create a clone of the present class
 @return Return with a pointer pointing to the cloned object
 */
-RY* clone();
+virtual RY* clone();
 
 };
 
 
 #endif //U3
```

### Comparing `squander-1.7.4/gates/include/RZ.h` & `squander-1.8.0/gates/include/RZ.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/SX.h` & `squander-1.8.0/gates/include/SX.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/SYC.h` & `squander-1.8.0/gates/include/SYC.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/U3.h` & `squander-1.8.0/gates/include/U3.h`

 * *Files 5% similar despite different names*

```diff
@@ -71,15 +71,15 @@
 @param lambda_in logical value indicating whether the matrix creation takes an argument lambda
 */
 U3(int qbit_num_in, int target_qbit_in, bool theta_in, bool phi_in, bool lambda_in);
 
 /**
 @brief Destructor of the class
 */
-~U3();
+virtual ~U3();
 
 /**
 @brief Call to retrieve the gate matrix
 @param parameters An array of parameters to calculate the matrix of the U3 gate.
 @return Returns with a matrix of the gate
 */
 Matrix get_matrix( Matrix_real& parameters );
@@ -116,23 +116,23 @@
 
 
 
 /**
 @brief Call to set the number of qubits spanning the matrix of the gate
 @param qbit_num_in The number of qubits
 */
-void set_qbit_num(int qbit_num_in);
+virtual void set_qbit_num(int qbit_num_in);
 
 
 
 /**
 @brief Call to reorder the qubits in the matrix of the gate
 @param qbit_list The reordered list of qubits spanning the matrix
 */
-void reorder_qubits( std::vector<int> qbit_list);
+virtual void reorder_qubits( std::vector<int> qbit_list);
 
 /**
 @brief Call to check whether theta is a free parameter of the gate
 @return Returns with true if theta is a free parameter of the gate, or false otherwise.
 */
 bool is_theta_parameter();
 
@@ -160,15 +160,15 @@
 Matrix calc_one_qubit_u3(double Theta, double Phi, double Lambda );
 
 
 /**
 @brief Call to create a clone of the present class
 @return Return with a pointer pointing to the cloned object
 */
-U3* clone();
+virtual U3* clone();
 
 
 /**
 @brief Call to set the final optimized parameters of the gate.
 @param Theta Real parameter standing for the parameter theta.
 @param Phi Real parameter standing for the parameter phi.
 @param Lambda Real parameter standing for the parameter lambda.
```

### Comparing `squander-1.7.4/gates/include/UN.h` & `squander-1.8.0/gates/include/UN.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/X.h` & `squander-1.8.0/gates/include/X.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/Y.h` & `squander-1.8.0/gates/include/Y.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/include/Z.h` & `squander-1.8.0/gates/include/Z.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/gates/kernels/include/apply_kernel_to_input_AVX.h` & `squander-1.8.0/gates/kernels/include/apply_kernel_to_input_AVX.h`

 * *Files 16% similar despite different names*

```diff
@@ -23,16 +23,34 @@
 
 
 #ifndef apply_kerel_to_input_AVX_H
 #define apply_kerel_to_input_AVX_H
 
 #include "matrix.h"
 #include "common.h"
+
+/**
+@brief AVX kernel to apply single qubit gate kernel on an input matrix -- optimal for small number of qubits
+@param ????????
+@param ?????????
+*/
+void apply_kernel_to_input_AVX_small(Matrix& u3_1qbit, Matrix& input, const bool& deriv, const int& target_qbit, const int& control_qbit, const int& matrix_size);
+
+
+
 /**
 @brief AVX kernel to apply single qubit gate kernel on an input matrix
 @param ????????
 @param ?????????
 */
 void apply_kernel_to_input_AVX(Matrix& u3_1qbit, Matrix& input, const bool& deriv, const int& target_qbit, const int& control_qbit, const int& matrix_size);
 
 
+/**
+@brief parallel AVX kernel to apply single qubit gate kernel on an input matrix
+@param ????????
+@param ?????????
+*/
+void apply_kernel_to_input_AVX_parallel(Matrix& u3_1qbit, Matrix& input, const bool& deriv, const int& target_qbit, const int& control_qbit, const int& matrix_size);
+
+
 #endif
```

### Comparing `squander-1.7.4/nn/NN.cpp` & `squander-1.8.0/nn/NN.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -405,17 +405,20 @@
 
 
 
 
     //matrix size of the unitary
     int matrix_size = 1 << qbit_num;
 
+    // empty config parameters
+    std::map<std::string, Config_Element> config_int;
+
 
     // creating a class to decompose the unitary
-    N_Qubit_Decomposition_adaptive cDecompose( Matrix(0,0), qbit_num, 0, 0, topology );
+    N_Qubit_Decomposition_adaptive cDecompose( Matrix(0,0), qbit_num, 0, 0, topology, config_int );
         
     //adding decomposing layers to the gat structure
     for( int idx=0; idx<levels; idx++) {
         cDecompose.add_adaptive_layers();
     }        
 
     cDecompose.add_finalyzing_layer();
```

### Comparing `squander-1.7.4/nn/include/NN.h` & `squander-1.8.0/nn/include/NN.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/decomposition/CMakeLists.txt` & `squander-1.8.0/qgd_python/decomposition/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition.py` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition.py`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_Wrapper.cpp` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_Wrapper.cpp`

 * *Files 1% similar despite different names*

```diff
@@ -65,17 +65,17 @@
 @param Umtx An instance of class Matrix containing the unitary to be decomposed
 @param qbit_num Number of qubits spanning the unitary
 @param optimize_layer_num Logical value. Set true to optimize the number of decomposing layers during the decomposition procedure, or false otherwise.
 @param initial_guess Type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
 @return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 N_Qubit_Decomposition* 
-create_N_Qubit_Decomposition( Matrix& Umtx, int qbit_num, bool optimize_layer_num, guess_type initial_guess ) {
+create_N_Qubit_Decomposition( Matrix& Umtx, int qbit_num, bool optimize_layer_num, std::map<std::string, Config_Element>& config, guess_type initial_guess ) {
 
-    return new N_Qubit_Decomposition( Umtx, qbit_num, optimize_layer_num, initial_guess );
+    return new N_Qubit_Decomposition( Umtx, qbit_num, optimize_layer_num, config, initial_guess );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
@@ -189,17 +189,23 @@
         qgd_initial_guess = CLOSE_TO_ZERO;        
     }
     else {
         std::cout << "Wrong initial guess format. Using default ZEROS." << std::endl; 
         qgd_initial_guess = ZEROS;     
     }
 
+    // parse config and create C++ version of the hyperparameters
+
+    // integer type config metadata utilized during the optimization
+    std::map<std::string, Config_Element> config;
+
+
     // create an instance of the class N_Qubit_Decomposition
     if (qbit_num > 0 ) {
-        self->decomp =  create_N_Qubit_Decomposition( Umtx_mtx, qbit_num, optimize_layer_num, qgd_initial_guess);
+        self->decomp =  create_N_Qubit_Decomposition( Umtx_mtx, qbit_num, optimize_layer_num, config, qgd_initial_guess);
     }
     else {
         std::cout << "The number of qubits should be given as a positive integer, " << qbit_num << "  was given" << std::endl;
         return -1;
     }
```

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive.py` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive.py`

 * *Files 12% similar despite different names*

```diff
@@ -36,16 +36,17 @@
     
     
 ## 
 # @brief Constructor of the class.
 # @param Umtx The unitary matrix to be decomposed.
 # @param optimize_layer_num Set true to optimize the minimum number of operation layers required in the decomposition, or false when the predefined maximal number of layer gates is used (ideal for general unitaries).
 # @param initial_guess String indicating the method to guess initial values for the optimalization. Possible values: "zeros" ,"random", "close_to_zero".
+# @param compression_enabled_in Optional logical value. If True(1) begin decomposition function will compress the circuit. If False(0) it will not. Compression can still be called in seperate wrapper function. 
 # @return An instance of the class
-    def __init__( self, Umtx, level_limit_max=8, level_limit_min=0, topology=None, accelerator_num=0 ):
+    def __init__( self, Umtx, level_limit_max=8, level_limit_min=0, topology=None, config={}, accelerator_num=0 ):
 
         ## the number of qubits
         self.qbit_num = int(round( np.log2( len(Umtx) ) ))
 
         # validate input parameters
 
         topology_validated = list()
@@ -60,26 +61,51 @@
         elif topology == None:
             pass
         else:
             print("Input parameter topology should be a list of (int, int) describing the connected qubits in the topology")
             return
         
 
+        # config
+        if not( type(config) is dict):
+            print("Input parameter config should be a dictionary describing the following hyperparameters:") #TODO
+            return
+
         # call the constructor of the wrapper class
-        super(qgd_N_Qubit_Decomposition_adaptive, self).__init__(Umtx, self.qbit_num, level_limit_max, level_limit_min, topology=topology_validated, accelerator_num=accelerator_num)
+        super(qgd_N_Qubit_Decomposition_adaptive, self).__init__(Umtx, self.qbit_num, level_limit_max, level_limit_min, topology=topology_validated, config=config, accelerator_num=accelerator_num)
 
 
 ##
 # @brief Wrapper function to call the start_decomposition method of C++ class N_Qubit_Decomposition
 # @param prepare_export Logical parameter. Set true to prepare the list of gates to be exported, or false otherwise.
     def Start_Decomposition(self,prepare_export=True):
 
 	# call the C wrapper function
         super(qgd_N_Qubit_Decomposition_adaptive, self).Start_Decomposition(prepare_export=prepare_export)
+##
+# @brief Wrapper function to call the get_initial_circuit method of C++ class N_Qubit_Decomposition
+    def get_Initial_Circuit(self):
+
+	# call the C wrapper function
+        super(qgd_N_Qubit_Decomposition_adaptive, self).get_Initial_Circuit()
+        
+##
+# @brief Wrapper function to call the compress_circuit method of C++ class N_Qubit_Decomposition
+    def Compress_Circuit(self,prepare_export=True):
+
+	# call the C wrapper function
+        super(qgd_N_Qubit_Decomposition_adaptive, self).Compress_Circuit()
+
+##
+# @brief Wrapper function to call the finalize_circuit method of C++ class N_Qubit_Decomposition
+# @param prepare_export Logical parameter. Set true to prepare the list of gates to be exported, or false otherwise.
+    def Finalize_Circuit(self,prepare_export=True):
 
+	# call the C wrapper function
+        super(qgd_N_Qubit_Decomposition_adaptive, self).Finalize_Circuit(prepare_export=prepare_export)
 
 ##
 # @brief Call to reorder the qubits in the matrix of the gate
 # @param qbit_list The reordered list of qubits spanning the matrix
     def Reorder_Qubits( self, qbit_list ):
 
 	# call the C wrapper function
@@ -406,26 +432,28 @@
 # @brief Call to set unitary matrix from a binary file created from SQUANDER
     def set_Unitary_From_Binary( self, filename ):  
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).set_Unitary_From_Binary( filename )
  
 ##
 # @brief Call to set unitary matrix from a numpy array
+# @param Umtx_arr numpy complex array 
     def set_Unitary( self, Umtx_arr ):  
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).set_Unitary( Umtx_arr )
         
 ##
 # @brief Call to get unitary matrix
     def get_Unitary( self ):
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Unitary()
         
 ##
 # @brief Call to export unitary matrix to binary file
+# @param filename string
     def export_Unitary( self, filename ):
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).export_Unitary(filename)
 
 
 ##
 # @brief Call to get the number of free parameters in the gate structure used for the decomposition
@@ -436,26 +464,28 @@
 ##
 # @brief Call to get global phase
     def get_Global_Phase( self ):
 	
         return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Global_Phase()
 
 ##
-# @brief Call to set global phase 
+# @brief Call to set global phase
+# @param new_global_phase New global phase (in radians)
     def set_Global_Phase( self, new_global_phase ):
 	
         return super(qgd_N_Qubit_Decomposition_adaptive, self).set_Global_Phase(new_global_phase)
 ##
 # @brief Call to get the name of the SQUANDER project
     def get_Project_Name( self ):
 	
         return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Project_Name()
 
 ##
-# @brief Call to set the name of the SQUANDER project ( recommended format : *new project name*_ ) 
+# @brief Call to set the name of the SQUANDER project
+# @param project_name_new new project name
     def set_Project_Name( self, project_name_new ):
 	
         return super(qgd_N_Qubit_Decomposition_adaptive, self).set_Project_Name(project_name_new)
 ##
 # @brief Call to apply global phase on Unitary matrix
     def apply_Global_Phase_Factor( self ):
 	
@@ -475,18 +505,17 @@
 
 
 ##
 # @brief Call to apply the imported gate structure on the unitary. The transformed unitary is to be decomposed in the calculations, and the imported gate structure is released.
     def apply_Imported_Gate_Structure( self ):  
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).apply_Imported_Gate_Structure()
-
 ## 
 # @brief Call to set the optimizer used in the gate synthesis process
-# @param optimizer String indicating the optimizer. Possible values: "BFGS" ,"ADAM", "BFGS2".
+# @param optimizer String indicating the optimizer. Possible values: "BFGS" ,"ADAM", "BFGS2", "ADAM_BATCHED", "AGENTS", "COSINE", "AGENTS_COMBINED".
     def set_Optimizer( self, optimizer="BFGS" ):
 
         # Set the optimizer
         super(qgd_N_Qubit_Decomposition_adaptive, self).set_Optimizer(optimizer)  
 
 
 ##
@@ -496,52 +525,103 @@
 
   
         if parameters is None:
             print( "get_Matrix: arary of input parameters is None")
             return None
 
         return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Matrix( parameters )
-
+        
 ## 
 # @brief Call to set the optimizer used in the gate synthesis process
 # @param costfnc Variant of the cost function. Input argument 0 stands for FROBENIUS_NORM, 1 for FROBENIUS_NORM_CORRECTION1, 2 for FROBENIUS_NORM_CORRECTION2
     def set_Cost_Function_Variant( self, costfnc=0 ):
 
         # Set the optimizer
         super(qgd_N_Qubit_Decomposition_adaptive, self).set_Cost_Function_Variant(costfnc=costfnc)  
 
 
 ## 
 # @brief Call to set the threshold value for the count of interations, above which the parameters are randomized if the cost function does not decreases fast enough.
 # @param threshold The value of the threshold
     def set_Iteration_Threshold_of_Randomization( self, threshold=2500 ):
 
-        # Set the optimizer
+        # Set the threshold
         super(qgd_N_Qubit_Decomposition_adaptive, self).set_Iteration_Threshold_of_Randomization(threshold)  
 
 
 
 ## 
+# @brief Call to set the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}
+# @param trace_offset The trace offset to be set
+    def set_Trace_Offset( self, trace_offset=0 ):
+
+        # Set the trace offset
+        super(qgd_N_Qubit_Decomposition_adaptive, self).set_Trace_Offset(trace_offset=trace_offset)  
+
+
+## 
+# @brief Call to get the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}
+# @return Returns with the trace offset
+    def get_Trace_Offset( self ):
+
+        # Set the optimizer
+        return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Trace_Offset()  
+
+
+## 
+# @brief Call to evaluate the cost function.
+# @param parameters A float64 numpy array
+    def Optimization_Problem( self, parameters=None ):
+
+        if parameters is None:
+            print( "Optimization_Problem: array of input parameters is None")
+            return None
+
+        # evaluate the cost function and gradients
+        cost_function = super(qgd_N_Qubit_Decomposition_adaptive, self).Optimization_Problem(parameters)  
+
+
+        return cost_function
+
+
+## 
 # @brief Call to evaluate the cost function and the gradient components.
 # @param parameters A float64 numpy array
     def Optimization_Problem_Combined( self, parameters=None ):
 
         if parameters is None:
-            print( "Optimization_Problem_Combined: arary of input parameters is None")
+            print( "Optimization_Problem_Combined: array of input parameters is None")
             return None
 
         # evaluate the cost function and gradients
         cost_function, grad = super(qgd_N_Qubit_Decomposition_adaptive, self).Optimization_Problem_Combined(parameters)  
 
         grad = grad.reshape( (-1,))
 
         return cost_function, grad
 
-
-
 ## 
 # @brief Call to prepare the circuit to be exported into Qiskit format. (parameters and gates gets bound together, gate block structure is converted to plain structure).
     def Prepare_Gates_To_Export(self):
 
         # Set the optimizer
-        super(qgd_N_Qubit_Decomposition_adaptive, self).Prepare_Gates_To_Export()  
+        super(qgd_N_Qubit_Decomposition_adaptive, self).Prepare_Gates_To_Export()
 
+##
+# @brief Call to get the number of iterations  
+    def get_Num_of_Iters(self):
+    
+        return super(qgd_N_Qubit_Decomposition_adaptive, self).get_Num_of_Iters()
+    
+##
+# @brief Call to set the maximum number of iterations for each optimization loop
+# @param max_iters int number of maximum iterations each loop
+    def set_Max_Iterations(self, max_iters):
+        
+        super(qgd_N_Qubit_Decomposition_adaptive, self).set_Max_Iterations(max_iters)
+    
+##
+# @brief call to set the cost function type of the optimization problem
+# @param cost_func int argument 0 stands for FROBENIUS_NORM, 1 for FROBENIUS_NORM_CORRECTION1, 2 for FROBENIUS_NORM_CORRECTION2, 3 for HILBERT_SCHMIDT_TEST, 4 for HILBERT_SCHMIDT_TEST_CORRECTION1, 5 for HILBERT_SCHMIDT_TEST_CORRECTION2 see more at: https://arxiv.org/abs/2210.09191
+    def set_Cost_Function_Variant(self, cost_func):
+    
+        super(qgd_N_Qubit_Decomposition_adaptive, self).set_Cost_Function_Variant(cost_func)
```

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive_Wrapper.cpp` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive_Wrapper.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -66,17 +66,17 @@
 @param Umtx An instance of class Matrix containing the unitary to be decomposed
 @param qbit_num Number of qubits spanning the unitary
 @param level_limit The maximal number of layers used in the decomposition
 @param initial_guess Type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
 @return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 N_Qubit_Decomposition_adaptive* 
-create_N_Qubit_Decomposition_adaptive( Matrix& Umtx, int qbit_num, int level_limit, int level_limit_min, std::vector<matrix_base<int>> topology_in, int accelerator_num ) {
+create_N_Qubit_Decomposition_adaptive( Matrix& Umtx, int qbit_num, int level_limit, int level_limit_min, std::vector<matrix_base<int>> topology_in, std::map<std::string, Config_Element>& config, int accelerator_num ) {
 
-    return new N_Qubit_Decomposition_adaptive( Umtx, qbit_num, level_limit, level_limit_min, topology_in, accelerator_num );
+    return new N_Qubit_Decomposition_adaptive( Umtx, qbit_num, level_limit, level_limit_min, topology_in, config, accelerator_num );
 }
 
 
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition_adaptive class
@@ -151,27 +151,28 @@
 @param args A tuple of the input arguments: Umtx (numpy array), qbit_num (integer), optimize_layer_num (bool), initial_guess (string PyObject 
 @param kwds A tuple of keywords
 */
 static int
 qgd_N_Qubit_Decomposition_adaptive_Wrapper_init(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args, PyObject *kwds)
 {
     // The tuple of expected keywords
-    static char *kwlist[] = {(char*)"Umtx", (char*)"qbit_num", (char*)"level_limit_min", (char*)"method", (char*)"topology", (char*)"accelerator_num", NULL};
+    static char *kwlist[] = {(char*)"Umtx", (char*)"qbit_num", (char*)"level_limit_min", (char*)"method", (char*)"topology", (char*)"config", (char*)"accelerator_num", NULL};
  
     // initiate variables for input arguments
     PyObject *Umtx_arg = NULL;
+    PyObject *config_arg = NULL;
     int  qbit_num = -1; 
     int level_limit = 0;
     int level_limit_min = 0;
     PyObject *topology = NULL;
     int accelerator_num = 0;
 
     // parsing input arguments
-    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|OiiiOi", kwlist,
-                                     &Umtx_arg, &qbit_num, &level_limit, &level_limit_min, &topology, &accelerator_num))
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|OiiiOOi", kwlist,
+                                     &Umtx_arg, &qbit_num, &level_limit, &level_limit_min, &topology, &config_arg, &accelerator_num))
         return -1;
 
     // convert python object array to numpy C API array
     if ( Umtx_arg == NULL ) return -1;
     self->Umtx = PyArray_FROM_OTF(Umtx_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
 
     // test C-style contiguous memory allocation of the array
@@ -215,18 +216,59 @@
             item_Cpp[1] = (int) PyLong_AsLong( PyTuple_GetItem(item, 1 ) );
 
             topology_Cpp.push_back( item_Cpp );        
         }
     }
 
 
+    // parse config and create C++ version of the hyperparameters
+
+    bool is_dict = PyDict_Check( config_arg );
+    if (!is_dict) {
+        printf("Config object must be a python dictionary!\n");
+        return -1;
+    }
+
+    // integer type config metadata utilized during the optimization
+    std::map<std::string, Config_Element> config;
+
+
+    // keys and values of the config dict
+    PyObject *key, *value;
+    Py_ssize_t pos = 0;
+
+    while (PyDict_Next(config_arg, &pos, &key, &value)) {
+
+        // determine the initial guess type
+        PyObject* key_string = PyObject_Str(key);
+        PyObject* key_string_unicode = PyUnicode_AsEncodedString(key_string, "utf-8", "~E~");
+        const char* key_C = PyBytes_AS_STRING(key_string_unicode);
+
+        std::string key_Cpp( key_C );
+        Config_Element element;
+
+        if ( PyLong_Check( value ) ) { 
+            element.set_property( key_Cpp, PyLong_AsLongLong( value ) );
+            config[ key_Cpp ] = element;
+        }
+        else if ( PyFloat_Check( value ) ) {
+            element.set_property( key_Cpp, PyFloat_AsDouble( value ) );
+            config[ key_Cpp ] = element;
+        }
+        else {
+
+        }
+
+    }
+
+
     // create an instance of the class N_Qubit_Decomposition
     if (qbit_num > 0 ) {
         try {
-            self->decomp = create_N_Qubit_Decomposition_adaptive( Umtx_mtx, qbit_num, level_limit, level_limit_min, topology_Cpp, accelerator_num);
+            self->decomp = create_N_Qubit_Decomposition_adaptive( Umtx_mtx, qbit_num, level_limit, level_limit_min, topology_Cpp, config, accelerator_num);
         }
         catch (std::string err ) {
             PyErr_SetString(PyExc_Exception, err.c_str());
             return -1;
         }
     }
     else {
@@ -277,21 +319,99 @@
     
 
 
     return Py_BuildValue("i", 0);
 
 }
 
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Initial_Circuit(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self)
+{
 
+    // starting the decomposition
+    try {
+        self->decomp->get_initial_circuit();
+    }
+    catch (std::string err) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        std::cout << err << std::endl;
+        return NULL;
+    }
+    catch(...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    
 
 
+    return Py_BuildValue("i", 0);
 
+}
 
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_Compress_Circuit(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self)
+{
 
+    // starting the decomposition
+    try {
+        self->decomp->compress_circuit();
+    }
+    catch (std::string err) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        std::cout << err << std::endl;
+        return NULL;
+    }
+    catch(...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    
+
+
+    return Py_BuildValue("i", 0);
 
+}
+
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_Finalize_Circuit(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args, PyObject *kwds)
+{
+
+    // The tuple of expected keywords
+    static char *kwlist[] = {(char*)"prepare_export", NULL};
+
+    // initiate variables for input arguments
+    bool  prepare_export = true; 
+
+    // parsing input arguments
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|b", kwlist,
+                                     &prepare_export))
+        return Py_BuildValue("i", -1);
+
+    // starting the decomposition
+    try {
+        self->decomp->finalize_circuit(prepare_export);
+    }
+    catch (std::string err) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        std::cout << err << std::endl;
+        return NULL;
+    }
+    catch(...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    
+
+
+    return Py_BuildValue("i", 0);
+
+}
 
 /**
 @brief Wrapper function to get the number of decomposing gates.
 @param self A pointer pointing to an instance of the class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
 @return Returns with the number of gates
 */
 static PyObject *
@@ -721,14 +841,24 @@
 qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Parameter_Num( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self ) {
 
     int parameter_num = self->decomp->get_parameter_num();
 
     return Py_BuildValue("i", parameter_num);
 }
 
+/**
+@brief Get the number of free parameters in the gate structure used for the decomposition
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Num_of_Iters( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self ) {
+
+    int number_of_iters = self->decomp->get_num_iters();
+    
+    return Py_BuildValue("i", number_of_iters);
+}
 
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
 static PyObject *
@@ -854,15 +984,35 @@
         self->decomp->set_iteration_loops( key_int, value_int );
 
     }
 
     return Py_BuildValue("i", 0);
 }
 
+/**
+@brief Set the number of maximum iterations.
+@param self A pointer pointing to an instance of the class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
+@param args  (int) number of max iters.
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Max_Iterations(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args ) {
+
+    // initiate variables for input arguments
+    PyObject* max_iters_input; 
 
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|i", &max_iters_input )) return Py_BuildValue("i", -1);
+
+
+    //set the maximum number of iterations
+    self->decomp->set_max_inner_iterations(max_iters_input);
+
+
+    return Py_BuildValue("i", 0);
+}
 
 /**
 @brief Set the verbosity of the N_Qubit_Decomposition class
 @param self A pointer pointing to an instance of the class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
 @param args A tuple of the input arguments: verbose (int)
 verbose: Set False to suppress the output messages of the decompostion, or True (deafult) otherwise.
 */
@@ -1295,14 +1445,72 @@
     Unitary_mtx.set_owner(false);
     PyObject *Unitary_py = matrix_to_numpy( Unitary_mtx );
 
     return Unitary_py;
 }
 
 
+/**
+@brief Wrapper function to evaluate the cost function.
+@return teh value of the cost function
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args)
+{
+
+
+    PyObject* parameters_arg = NULL;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &parameters_arg )) {
+
+        std::string err( "Unsuccessful argument parsing not ");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;      
+
+    } 
+
+    // establish memory contiguous arrays for C calculations
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arg) && PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ){
+        Py_INCREF(parameters_arg);
+    }
+    else if (PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ) {
+        parameters_arg = PyArray_FROM_OTF(parameters_arg, NPY_FLOAT64, NPY_ARRAY_IN_ARRAY);
+    }
+    else {
+        std::string err( "Parameters should be should be real (given in float64 format)");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+
+    Matrix_real parameters_mtx = numpy2matrix_real( parameters_arg );
+    double f0;
+
+    try {
+        f0 = self->decomp->optimization_problem(parameters_mtx );
+    }
+    catch (std::string err ) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    catch (...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+    Py_DECREF(parameters_arg);
+
+
+    return Py_BuildValue("d", f0);
+}
+
+
 
 
 /**
 @brief Wrapper function to evaluate the cost function an dthe gradient components.
 @return Unitarty numpy matrix
 */
 static PyObject *
@@ -1310,15 +1518,15 @@
 {
 
 
     PyObject* parameters_arg = NULL;
 
 
     // parsing input arguments
-    if (!PyArg_ParseTuple(args, "|Oi", &parameters_arg )) {
+    if (!PyArg_ParseTuple(args, "|O", &parameters_arg )) {
 
         std::string err( "Unsuccessful argument parsing not ");
         PyErr_SetString(PyExc_Exception, err.c_str());
         return NULL;      
 
     } 
 
@@ -1356,19 +1564,147 @@
     // convert to numpy array
     grad_mtx.set_owner(false);
     PyObject *grad_py = matrix_real_to_numpy( grad_mtx );
 
     Py_DECREF(parameters_arg);
 
 
-    return Py_BuildValue("(dO)", f0, grad_py);
+    PyObject* p = Py_BuildValue("(dO)", f0, grad_py);
+    Py_DECREF(grad_py);
+    return p;
 }
 
+/**
+@brief Wrapper function to evaluate the unitary function and the unitary derivates.
+@return Unitarty numpy matrix
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem_Combined_Unitary( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args)
+{
+
+
+    PyObject* parameters_arg = NULL;
 
 
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &parameters_arg )) {
+
+        std::string err( "Unsuccessful argument parsing not ");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;      
+
+    } 
+
+    // establish memory contiguous arrays for C calculations
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arg) && PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ){
+        Py_INCREF(parameters_arg);
+    }
+    else if (PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ) {
+        parameters_arg = PyArray_FROM_OTF(parameters_arg, NPY_FLOAT64, NPY_ARRAY_IN_ARRAY);
+    }
+    else {
+        std::string err( "Parameters should be should be real (given in float64 format)");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+
+    Matrix_real parameters_mtx = numpy2matrix_real( parameters_arg );
+    Matrix Umtx;
+    std::vector<Matrix> Umtx_deriv;
+
+    try {
+        self->decomp->optimization_problem_combined_unitary(parameters_mtx, Umtx, Umtx_deriv );
+    }
+    catch (std::string err ) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    catch (...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+    // convert to numpy array
+    Umtx.set_owner(false);
+    PyObject *unitary_py = matrix_to_numpy( Umtx );
+    PyObject* graduni_py = PyList_New(Umtx_deriv.size());
+    for (size_t i = 0; i < Umtx_deriv.size(); i++) {
+        Umtx_deriv[i].set_owner(false);
+        PyList_SetItem(graduni_py, i, matrix_to_numpy(Umtx_deriv[i]));
+    }
+
+    Py_DECREF(parameters_arg);
+
+
+    PyObject* p = Py_BuildValue("(OO)", unitary_py, graduni_py);
+    Py_DECREF(unitary_py); Py_DECREF(graduni_py);
+    return p;
+}
+
+/**
+@brief Wrapper function to evaluate the cost function an dthe gradient components.
+@return Unitarty numpy matrix
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem_Batch( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args)
+{
+
+
+    PyObject* parameters_arg = NULL;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &parameters_arg )) {
+
+        std::string err( "Unsuccessful argument parsing not ");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;      
+
+    } 
+
+    // establish memory contiguous arrays for C calculations
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arg) && PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ){
+        Py_INCREF(parameters_arg);
+    }
+    else if (PyArray_TYPE(parameters_arg) == NPY_FLOAT64 ) {
+        parameters_arg = PyArray_FROM_OTF(parameters_arg, NPY_FLOAT64, NPY_ARRAY_IN_ARRAY);
+    }
+    else {
+        std::string err( "Parameters should be should be real (given in float64 format)");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+
+    Matrix_real parameters_mtx = numpy2matrix_real( parameters_arg );
+    Matrix_real result_mtx;
+
+    try {
+        result_mtx = self->decomp->optimization_problem_batch(parameters_mtx );
+    }
+    catch (std::string err ) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+    catch (...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+    // convert to numpy array
+    result_mtx.set_owner(false);
+    PyObject *result_py = matrix_real_to_numpy( result_mtx );
+
+    Py_DECREF(parameters_arg);
+
+    return result_py;
+}
 
 static PyObject *
 qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Unitary( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args ) {
 
        if ( self->Umtx != NULL ) {
            // release the unitary to be decomposed
            Py_DECREF(self->Umtx);    
@@ -1488,15 +1824,14 @@
 }
 
 
 
 /**
 @brief Wrapper function to set the radius in which randomized parameters are generated around the current minimum duting the optimization process
 @param self A pointer pointing to an instance of the class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
-@param args A tuple of the input arguments: gate_structure_dict (PyDict)
 @return Returns with zero on success.
 */
 static PyObject * qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Randomized_Radius( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args ) {
 
     // initiate variables for input arguments
     double radius = 1.0; 
 
@@ -1599,19 +1934,28 @@
     optimization_aglorithms qgd_optimizer;
     if ( strcmp("bfgs", optimizer_C) == 0 or strcmp("BFGS", optimizer_C) == 0) {
         qgd_optimizer = BFGS;        
     }
     else if ( strcmp("adam", optimizer_C)==0 or strcmp("ADAM", optimizer_C)==0) {
         qgd_optimizer = ADAM;        
     }
+    else if ( strcmp("adam_batched", optimizer_C)==0 or strcmp("ADAM_BATCHED", optimizer_C)==0) {
+        qgd_optimizer = ADAM_BATCHED;        
+    }
     else if ( strcmp("bfgs2", optimizer_C)==0 or strcmp("BFGS2", optimizer_C)==0) {
         qgd_optimizer = BFGS2;        
     }
+    else if ( strcmp("agents", optimizer_C)==0 or strcmp("AGENTS", optimizer_C)==0) {
+        qgd_optimizer = AGENTS;        
+    }
+    else if ( strcmp("agents_combined", optimizer_C)==0 or strcmp("AGENTS_COMBINED", optimizer_C)==0) {
+        qgd_optimizer = AGENTS_COMBINED;        
+    }
     else {
-        std::cout << "Wrong optimizer. Using default: BFGS rrrrrrrrrrrrrrr" << std::endl; 
+        std::cout << "Wrong optimizer. Using default: BFGS" << std::endl; 
         qgd_optimizer = BFGS;     
     }
 
 
     try {
         self->decomp->set_optimizer(qgd_optimizer);
     }
@@ -1722,14 +2066,92 @@
 
 
     return Py_BuildValue("i", 0);
 
 }
 
 
+
+/**
+@brief Wrapper function to set the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}
+@return Returns with zero on success.
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Trace_Offset( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self, PyObject *args, PyObject *kwds)
+{
+
+    // The tuple of expected keywords
+    static char *kwlist[] = {(char*)"trace_offset", NULL};
+
+    int trace_offset_arg = 0;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|i", kwlist, &trace_offset_arg)) {
+
+        std::string err( "Unsuccessful argument parsing");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;       
+ 
+    }
+   
+
+    try {
+        self->decomp->set_trace_offset(trace_offset_arg);
+    }
+    catch (std::string err) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        std::cout << err << std::endl;
+        return NULL;
+    }
+    catch(...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+
+    return Py_BuildValue("i", 0);
+
+}
+
+
+
+/**
+@brief Wrapper function to get the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}
+@return Returns with the trace offset
+*/
+static PyObject *
+qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Trace_Offset( qgd_N_Qubit_Decomposition_adaptive_Wrapper *self )
+{
+   
+    int trace_offset = 0;
+
+    try {
+        trace_offset = self->decomp->get_trace_offset();
+    }
+    catch (std::string err) {
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        std::cout << err << std::endl;
+        return NULL;
+    }
+    catch(...) {
+        std::string err( "Invalid pointer to decomposition class");
+        PyErr_SetString(PyExc_Exception, err.c_str());
+        return NULL;
+    }
+
+
+    return Py_BuildValue("i", trace_offset);
+
+}
+
+
+
+
 /**
 @brief Call to upload the unitary to the DFE. (Has no effect for non-DFE builds)
 */
 static PyObject *
 qgd_N_Qubit_Decomposition_adaptive_Wrapper_Upload_Umtx_to_DFE(qgd_N_Qubit_Decomposition_adaptive_Wrapper *self ) {
 
 #ifdef __DFE__
@@ -1792,14 +2214,23 @@
 /**
 @brief Structure containing metadata about the methods of class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
 */
 static PyMethodDef qgd_N_Qubit_Decomposition_adaptive_Wrapper_methods[] = {
     {"Start_Decomposition", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Start_Decomposition, METH_VARARGS | METH_KEYWORDS,
      "Method to start the decomposition."
     },
+    {"get_Initial_Circuit", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Initial_Circuit, METH_NOARGS,
+     "Method to get initial circuit in decomposition."
+    },
+    {"Compress_Circuit", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Compress_Circuit, METH_NOARGS,
+     "Method to compress gate structure."
+    },
+    {"Finalize_Circuit", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Finalize_Circuit, METH_VARARGS | METH_KEYWORDS,
+     "Method to finalize the decomposition."
+    },
     {"get_Gate_Num", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_gate_num, METH_NOARGS,
      "Method to get the number of decomposing gates."
     },
     {"get_Parameter_Num", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Parameter_Num, METH_NOARGS,
      "Call to get the number of free parameters in the gate structure used for the decomposition"
     },
     {"get_Optimized_Parameters", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Optimized_Parameters, METH_NOARGS,
@@ -1813,14 +2244,17 @@
     },
     {"get_Gates", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_gates, METH_NOARGS,
      "Method to get the tuple of decomposing gates."
     },
     {"List_Gates", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_List_Gates, METH_NOARGS,
      "Call to print the decomposing nitaries on standard output"
     },
+    {"get_Num_of_Iters", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Num_of_Iters, METH_NOARGS,
+     "Method to get the number of iterations."
+    },
     {"set_Max_Layer_Num", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Max_Layer_Num, METH_VARARGS,
      "Call to set the maximal number of layers used in the subdecomposition of the qbit-th qubit."
     },
     {"set_Iteration_Loops", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Iteration_Loops, METH_VARARGS,
      "Call to set the number of iteration loops during the subdecomposition of the qbit-th qubit."
     },
     {"set_Verbose", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Verbose, METH_VARARGS,
@@ -1891,32 +2325,50 @@
     },
     {"set_Randomized_Radius", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Randomized_Radius, METH_VARARGS,
      "Call to set the radius in which randomized parameters are generated around the current minimum duting the optimization process."
     },
     {"set_Optimizer", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Optimizer, METH_VARARGS | METH_KEYWORDS,
      "Wrapper method to to set the optimizer method for the gate synthesis."
     },
+    {"set_Max_Iterations", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Max_Iterations, METH_VARARGS | METH_VARARGS,
+     "Wrapper method to to set the maximum number of iterations for the gate synthesis."
+    },
     {"get_Matrix", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Matrix, METH_VARARGS,
      "Method to retrieve the unitary of the circuit."
     },
     {"set_Cost_Function_Variant", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Cost_Function_Variant, METH_VARARGS | METH_KEYWORDS,
-     "Wrapper method to to set the variant of the cost function. Input argument 0 stands for FROBENIUS_NORM, 1 for FROBENIUS_NORM_CORRECTION1, 2 for FROBENIUS_NORM_CORRECTION2"
+     "Wrapper method to to set the variant of the cost function. Input argument 0 stands for FROBENIUS_NORM, 1 for FROBENIUS_NORM_CORRECTION1, 2 for FROBENIUS_NORM_CORRECTION2, 3 for HILBERT_SCHMIDT_TEST, 4 for HILBERT_SCHMIDT_TEST_CORRECTION1, 5 for HILBERT_SCHMIDT_TEST_CORRECTION2."
     },
     {"set_Iteration_Threshold_of_Randomization", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Iteration_Threshold_of_Randomization, METH_VARARGS | METH_KEYWORDS,
      "Wrapper function to set the threshold value for the count of interations, above which the parameters are randomized if the cost function does not decreases fast enough."
     },
+    {"Optimization_Problem", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem, METH_VARARGS,
+     "Wrapper function to evaluate the cost function."
+    },
+    {"Optimization_Problem_Combined_Unitary", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem_Combined_Unitary, METH_VARARGS,
+     "Wrapper function to evaluate the unitary function and the gradient components."
+    },	
     {"Optimization_Problem_Combined", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem_Combined, METH_VARARGS,
      "Wrapper function to evaluate the cost function and the gradient components."
     },
+    {"Optimization_Problem_Batch", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Optimization_Problem_Batch, METH_VARARGS,
+     "Wrapper function to evaluate the cost function of batch."
+    },
     {"Upload_Umtx_to_DFE", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Upload_Umtx_to_DFE, METH_NOARGS,
      "Call to upload the unitary to the DFE. (Has no effect for non-DFE builds)"
     },
     {"Prepare_Gates_To_Export", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_Prepare_Gates_To_Export, METH_NOARGS,
      "Call to prepare the circuit to be exported into Qiskit format. (parameters and gates gets bound together, gate block structure is converted to plain structure)."
     },
+    {"get_Trace_Offset", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_get_Trace_Offset, METH_NOARGS,
+     "Call to get the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}"
+    },
+    {"set_Trace_Offset", (PyCFunction) qgd_N_Qubit_Decomposition_adaptive_Wrapper_set_Trace_Offset, METH_VARARGS | METH_KEYWORDS,
+     "Call to set the trace offset used in the cost function. In this case Tr(A) = sum_(i-offset=j) A_{ij}"
+    },
     {NULL}  /* Sentinel */
 };
 
 /**
 @brief A structure describing the type of the class qgd_N_Qubit_Decomposition_adaptive_Wrapper.
 */
 static PyTypeObject qgd_N_Qubit_Decomposition_adaptive_Wrapper_Type = {
```

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom.py` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom.py`

 * *Files 5% similar despite different names*

```diff
@@ -37,21 +37,26 @@
     
 ## 
 # @brief Constructor of the class.
 # @param Umtx The unitary matrix to be decomposed.
 # @param optimize_layer_num Set true to optimize the minimum number of operation layers required in the decomposition, or false when the predefined maximal number of layer gates is used (ideal for general unitaries).
 # @param initial_guess String indicating the method to guess initial values for the optimalization. Possible values: "zeros" ,"random", "close_to_zero".
 # @return An instance of the class
-    def __init__( self, Umtx, initial_guess="RANDOM", accelerator_num=0 ):
+    def __init__( self, Umtx, initial_guess="RANDOM", config={}, accelerator_num=0 ):
 
         ## the number of qubits
         self.qbit_num = int(round( np.log2( len(Umtx) ) ))
+        
+        # config
+        if not( type(config) is dict):
+            print("Input parameter config should be a dictionary describing the following hyperparameters:") #TODO
+            return
 
         # call the constructor of the wrapper class
-        super(qgd_N_Qubit_Decomposition_custom, self).__init__(Umtx, self.qbit_num, initial_guess, accelerator_num)
+        super(qgd_N_Qubit_Decomposition_custom, self).__init__(Umtx, self.qbit_num, initial_guess, config=config, accelerator_num=accelerator_num)
 
 
 
 ##
 # @brief Wrapper function to call the start_decomposition method of C++ class N_Qubit_Decomposition
 # @param prepare_export Logical parameter. Set true to prepare the list of gates to be exported, or false otherwise.
     def Start_Decomposition(self,prepare_export=True):
@@ -237,15 +242,15 @@
 # @param qc_in The quantum circuit to be imported
     def import_Qiskit_Circuit( self, qc_in ):  
 
         from qiskit import QuantumCircuit, transpile
         from qiskit.circuit import ParameterExpression
         from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
 
-        qc = qc_in#transpile(qc_in, optimization_level=3, basis_gates=['cz', 'cx', 'u3'], layout_method='sabre')
+        qc = transpile(qc_in, optimization_level=3, basis_gates=['cz', 'cx', 'u3'], layout_method='sabre')
         #print('Depth of Qiskit transpiled quantum circuit:', qc.depth())
         #print('Gate counts in Qiskit transpiled quantum circuit:', qc.count_ops())
 
         # get the register of qubits
         q_register = qc.qubits
 
         # get the size of the register
@@ -351,15 +356,15 @@
         self.set_Gate_Structure(Gates_Block_ret)
         self.set_Optimized_Parameters( np.flip(optimized_parameters,0) )      
         
 
 
 ## 
 # @brief Call to set the optimizer used in the gate synthesis process
-# @param optimizer String indicating the optimizer. Possible values: "BFGS" ,"ADAM", "BFGS2".
+# @param optimizer String indicating the optimizer. Possible values: "BFGS" ,"ADAM", "BFGS2", "AGENTS", "COSINE", "AGENTS_COMBINED".
 # @return An instance of the class
     def set_Optimizer( self, optimizer="BFGS" ):
 
         # Set the optimizer
         super(qgd_N_Qubit_Decomposition_custom, self).set_Optimizer(optimizer)
```

### Comparing `squander-1.7.4/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom_Wrapper.cpp` & `squander-1.8.0/qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom_Wrapper.cpp`

 * *Files 3% similar despite different names*

```diff
@@ -64,17 +64,17 @@
 @param Umtx An instance of class Matrix containing the unitary to be decomposed
 @param qbit_num Number of qubits spanning the unitary
 @param optimize_layer_num Logical value. Set true to optimize the number of decomposing layers during the decomposition procedure, or false otherwise.
 @param initial_guess Type to guess the initial values for the optimization. Possible values: ZEROS=0, RANDOM=1, CLOSE_TO_ZERO=2
 @return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 N_Qubit_Decomposition_custom* 
-create_N_Qubit_Decomposition_custom( Matrix& Umtx, int qbit_num, bool optimize_layer_num, guess_type initial_guess, int accelerator_num ) {
+create_N_Qubit_Decomposition_custom( Matrix& Umtx, int qbit_num, bool optimize_layer_num, guess_type initial_guess, std::map<std::string, Config_Element>& config, int accelerator_num ) {
 
-    return new N_Qubit_Decomposition_custom( Umtx, qbit_num, optimize_layer_num, initial_guess, accelerator_num );
+    return new N_Qubit_Decomposition_custom( Umtx, qbit_num, optimize_layer_num, config, initial_guess, accelerator_num );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition_custom class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition_custom class.
 */
@@ -140,25 +140,26 @@
 @param args A tuple of the input arguments: Umtx (numpy array), qbit_num (integer), optimize_layer_num (bool), initial_guess (string PyObject 
 @param kwds A tuple of keywords
 */
 static int
 qgd_N_Qubit_Decomposition_custom_Wrapper_init(qgd_N_Qubit_Decomposition_custom_Wrapper *self, PyObject *args, PyObject *kwds)
 {
     // The tuple of expected keywords
-    static char *kwlist[] = {(char*)"Umtx", (char*)"qbit_num", (char*)"initial_guess", (char*)"accelerator_num", NULL};
+    static char *kwlist[] = {(char*)"Umtx", (char*)"qbit_num", (char*)"initial_guess", (char*)"config", (char*)"accelerator_num", NULL};
  
     // initiate variables for input arguments
     PyObject *Umtx_arg = NULL;
+    PyObject *config_arg = NULL;    
     int  qbit_num = -1; 
     PyObject *initial_guess = NULL;
     int accelerator_num = 0;
 
     // parsing input arguments
-    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|OiOi", kwlist,
-                                     &Umtx_arg, &qbit_num, &initial_guess, &accelerator_num))
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|OiOOi", kwlist,
+                                     &Umtx_arg, &qbit_num, &initial_guess, &config_arg, &accelerator_num))
         return -1;
 
     // convert python object array to numpy C API array
     if ( Umtx_arg == NULL ) return -1;
     self->Umtx = PyArray_FROM_OTF(Umtx_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
 
     // test C-style contiguous memory allocation of the array
@@ -186,19 +187,53 @@
     else if ( strcmp("close_to_zero", initial_guess_C)==0 or strcmp("CLOSE_TO_ZERO", initial_guess_C)==0) {
         qgd_initial_guess = CLOSE_TO_ZERO;        
     }
     else {
         std::cout << "Wrong initial guess format. Using default ZEROS." << std::endl; 
         qgd_initial_guess = ZEROS;     
     }
+
+
+    // parse config and create C++ version of the hyperparameters
+
+    // integer type config metadata utilized during the optimization
+    std::map<std::string, Config_Element> config;
+
+    // keys and values of the config dict
+    PyObject *key, *value;
+    Py_ssize_t pos = 0;
+
+    while (PyDict_Next(config_arg, &pos, &key, &value)) {
+
+        // determine the initial guess type
+        PyObject* key_string = PyObject_Str(key);
+        PyObject* key_string_unicode = PyUnicode_AsEncodedString(key_string, "utf-8", "~E~");
+        const char* key_C = PyBytes_AS_STRING(key_string_unicode);
+
+        std::string key_Cpp( key_C );
+        Config_Element element;
+
+        if ( PyLong_Check( value ) ) { 
+            element.set_property( key_Cpp, PyLong_AsLongLong( value ) );
+            config[ key_Cpp ] = element;
+        }
+        else if ( PyFloat_Check( value ) ) {
+            element.set_property( key_Cpp, PyFloat_AsDouble( value ) );
+            config[ key_Cpp ] = element;
+        }
+        else {
+
+        }
+
+    }
   
     // create an instance of the class N_Qubit_Decomposition_custom
     if (qbit_num > 0 ) {
         try {
-            self->decomp =  create_N_Qubit_Decomposition_custom( Umtx_mtx, qbit_num, false, qgd_initial_guess, accelerator_num);
+            self->decomp =  create_N_Qubit_Decomposition_custom( Umtx_mtx, qbit_num, false, qgd_initial_guess, config, accelerator_num);
         }
         catch (std::string err ) {
             PyErr_SetString(PyExc_Exception, err.c_str());
             return -1;
         }
     }
     else {
@@ -859,15 +894,14 @@
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &gate_structure_py )) return Py_BuildValue("i", -1);
 
 
     // convert gate structure from PyObject to qgd_Gates_Block
     qgd_Gates_Block* qgd_op_block = (qgd_Gates_Block*) gate_structure_py;
-
     self->decomp->set_custom_gate_structure( qgd_op_block->gate );
 
     return Py_BuildValue("i", 0);
 
 
 }
 
@@ -968,19 +1002,31 @@
     optimization_aglorithms qgd_optimizer;
     if ( strcmp("bfgs", optimizer_C) == 0 or strcmp("BFGS", optimizer_C) == 0) {
         qgd_optimizer = BFGS;        
     }
     else if ( strcmp("adam", optimizer_C)==0 or strcmp("ADAM", optimizer_C)==0) {
         qgd_optimizer = ADAM;        
     }
+    else if ( strcmp("adam_batched", optimizer_C)==0 or strcmp("ADAM_BATCHED", optimizer_C)==0) {
+        qgd_optimizer = ADAM_BATCHED;        
+    }
+    else if ( strcmp("agents", optimizer_C)==0 or strcmp("AGENTS", optimizer_C)==0) {
+        qgd_optimizer = AGENTS;        
+    }
+    else if ( strcmp("cosine", optimizer_C)==0 or strcmp("COSINE", optimizer_C)==0) {
+        qgd_optimizer = COSINE;        
+    }
+    else if ( strcmp("agents_combined", optimizer_C)==0 or strcmp("AGENTS_COMBINED", optimizer_C)==0) {
+        qgd_optimizer = AGENTS_COMBINED;        
+    }
     else if ( strcmp("bfgs2", optimizer_C)==0 or strcmp("BFGS2", optimizer_C)==0) {
         qgd_optimizer = BFGS2;        
     }
     else {
-        std::cout << "Wrong optimizer. Using default: BFGS rrrrrrrrrrrrrrr" << std::endl; 
+        std::cout << "Wrong optimizer. Using default: BFGS" << std::endl; 
         qgd_optimizer = BFGS;     
     }
 
 
     try {
         self->decomp->set_optimizer(qgd_optimizer);
     }
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_Global_Phase.py` & `squander-1.8.0/qgd_python/decomposition/test/test_Global_Phase.py`

 * *Files 12% similar despite different names*

```diff
@@ -14,40 +14,40 @@
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
-## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \file test_Global_Phase.py
+## \brief Functionality test cases for the N_Qubit_Decomposition_adaptive class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
 
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition_adaptive import qgd_N_Qubit_Decomposition_adaptive
+from squander import N_Qubit_Decomposition_adaptive
 from scipy.io import loadmat
 
 def test_global_phase():
 	# load the unitary from file
 	data = loadmat('Umtx.mat')
 	# The unitary to be decomposed  
 	Umtx = data['Umtx']
 	# creating a class to decompose the unitary
-	cDecompose = qgd_N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
+	cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
 	angl = cDecompose.get_Global_Phase()
 	Umtx_assert = cDecompose.get_Unitary()
 
 	assert(np.abs(angl)<2*np.pi)
 
 	angl_new = np.pi/3
 	cDecompose.set_Global_Phase(angl_new)
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_IBM.py` & `squander-1.8.0/qgd_python/decomposition/test/test_IBM.py`

 * *Files 16% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 ## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
-from qgd_python.utils import get_unitary_from_qiskit_circuit
+from squander import utils
 
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
@@ -45,25 +45,25 @@
     def test_IBM_Chellenge(self):
         r"""
         This method is called by pytest. 
         Test to decompose a 4-qubit unitary of the IBM chellenge
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition        
+        from squander import N_Qubit_Decomposition        
         from scipy.io import loadmat
     
         # load the unitary from file
         data = loadmat('Umtx.mat')  
         # The unitary to be decomposed  
         Umtx = data['Umtx']
         
 
         # creating a class to decompose the unitary
-        cDecompose = qgd_N_Qubit_Decomposition( Umtx.conj().T, optimize_layer_num=True, initial_guess="CLOSE_TO_ZERO" )
+        cDecompose = N_Qubit_Decomposition( Umtx.conj().T, optimize_layer_num=True, initial_guess="CLOSE_TO_ZERO" )
         
 
         # set the number of successive identical blocks in the optimalization of disentanglement of the n-th qubits
         cDecompose.set_Identical_Blocks( {4: 2, 3: 1} )
 
         # set the maximal number of layers in the decomposition
         cDecompose.set_Max_Layer_Num( {4: 9, 3:4} )
@@ -90,15 +90,15 @@
         print(quantum_circuit)
 
 
         import numpy.linalg as LA
     
         # test the decomposition of the matrix
         # the unitary matrix from the result object
-        decomposed_matrix = get_unitary_from_qiskit_circuit( quantum_circuit ) 
+        decomposed_matrix = utils.get_unitary_from_qiskit_circuit( quantum_circuit ) 
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
     
         product_matrix = np.eye(16)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error = (np.real(np.trace(product_matrix)))/2
@@ -112,25 +112,25 @@
     def test_IBM_Chellenge_adaptive(self):
         r"""
         This method is called by pytest. 
         Test to decompose a 4-qubit unitary of the IBM chellenge
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition_adaptive import qgd_N_Qubit_Decomposition_adaptive       
+        from squander import N_Qubit_Decomposition_adaptive       
         from scipy.io import loadmat
     
         # load the unitary from file
         data = loadmat('Umtx.mat')  
         # The unitary to be decomposed  
         Umtx = data['Umtx']
         
 
         # creating a class to decompose the unitary
-        cDecompose = qgd_N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
+        cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
 
 
         # setting the verbosity of the decomposition
         cDecompose.set_Verbose( 3 )
 
         # starting the decomposition
         cDecompose.Start_Decomposition()
@@ -143,22 +143,81 @@
 
         # print the quantum circuit
         print(quantum_circuit)
 
         import numpy.linalg as LA
     
         # the unitary matrix from the result object
-        decomposed_matrix = get_unitary_from_qiskit_circuit( quantum_circuit )
+        decomposed_matrix = utils.get_unitary_from_qiskit_circuit( quantum_circuit )
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
     
         product_matrix = np.eye(16)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error = (np.real(np.trace(product_matrix)))/2
        
         print('The error of the decomposition is ' + str(decomposition_error))
 
         assert( decomposition_error < 1e-3 )
+
+
+
+
+
+    def test_IBM_Chellenge_adaptive_rectangular_input(self):
+        r"""
+        This method is called by pytest. 
+        Test to decompose a 4-qubit unitary of the IBM chellenge
+
+        """
+
+        from squander import N_Qubit_Decomposition_adaptive       
+        from scipy.io import loadmat
+    
+        # load the unitary from file
+        data = loadmat('Umtx.mat')  
+        # The unitary to be decomposed  
+        Umtx = data['Umtx']
+        Umtx = Umtx[0:14,:]
+        
+
+        # creating a class to decompose the unitary
+        cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
+
+
+        # setting the verbosity of the decomposition
+        cDecompose.set_Verbose( 3 )
+
+        # starting the decomposition
+        cDecompose.Start_Decomposition()
+
+        # list the decomposing operations
+        cDecompose.List_Gates()
+
+        # get the decomposing operations
+        quantum_circuit = cDecompose.get_Quantum_Circuit()
+
+        # print the quantum circuit
+        print(quantum_circuit)
+
+        import numpy.linalg as LA
+    
+        # the unitary matrix from the result object
+        decomposed_matrix = utils.get_unitary_from_qiskit_circuit( quantum_circuit )
+        decomposed_matrix = decomposed_matrix[0:14,:]
+        product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
+        phase = np.angle(product_matrix[0,0])
+        product_matrix = product_matrix*np.exp(-1j*phase)
+
+        print( product_matrix.shape )
+    
+        product_matrix = np.eye(product_matrix.shape[0])*2 - product_matrix - product_matrix.conj().T
+        # the error of the decomposition
+        decomposition_error = (np.real(np.trace(product_matrix)))/2
+       
+        print('The error of the decomposition is ' + str(decomposition_error))
+
+        assert( decomposition_error < 1e-3 )
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_Project_Name.py` & `squander-1.8.0/qgd_python/decomposition/test/test_Project_Name.py`

 * *Files 7% similar despite different names*

```diff
@@ -14,43 +14,43 @@
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
-## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \file test_Project_Name.py
+## \brief Functionality test cases for the N_Qubit_Decomposition_adaptive class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
 import os
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition_adaptive import qgd_N_Qubit_Decomposition_adaptive
+from squander import N_Qubit_Decomposition_adaptive
 from scipy.io import loadmat
 
 def test_Project_Name():
 
 	# load the unitary from file
 	data = loadmat('Umtx.mat')
 
 	# The unitary to be decomposed  
 	Umtx = data['Umtx']
 
 	# creating a class to decompose the unitary
-	cDecompose = qgd_N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
+	cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
 
 
 	project_name = cDecompose.get_Project_Name()
 	assert(project_name=="")
 
 	cDecompose.set_Project_Name("TEST")
 	project_name = cDecompose.get_Project_Name()
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_QX2.py` & `squander-1.8.0/qgd_python/decomposition/test/test_QX2.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,22 +15,22 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
 ## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \brief Functionality test cases for the N_Qubit_Decomposition class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
-from qgd_python.utils import get_unitary_from_qiskit_circuit
+from squander import utils
 
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
@@ -48,27 +48,27 @@
     def test_N_Qubit_Decomposition_QX2(self):
         r"""
         This method is called by pytest. 
         Test to define custom gate structure in the decomposition
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
+        from squander import N_Qubit_Decomposition
 
         # the number of qubits spanning the unitary
         qbit_num = 4
 
         # determine the soze of the unitary to be decomposed
         matrix_size = int(2**qbit_num)
    
         # creating a random unitary to be decomposed
         Umtx = unitary_group.rvs(matrix_size)
     
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition( Umtx.conj().T )
+        decomp = N_Qubit_Decomposition( Umtx.conj().T )
 
         # list of reordered qubits (original: (3,2,1,0) )
         reordered_qbits = (0,1,3,2)
 
         # adding custom gate structure to the decomposition
         decomp.Reorder_Qubits( reordered_qbits )
 
@@ -102,15 +102,15 @@
         # get the decomposing operations
         quantum_circuit = decomp.get_Quantum_Circuit()
 
         import numpy.linalg as LA
     
         # test the decomposition of the matrix
         # the unitary matrix from the result object
-        decomposed_matrix = np.asarray( get_unitary_from_qiskit_circuit( quantum_circuit ) )
+        decomposed_matrix = np.asarray( utils.get_unitary_from_qiskit_circuit( quantum_circuit ) )
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
     
         product_matrix = np.eye(matrix_size)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error = (np.real(np.trace(product_matrix)))/2
@@ -122,27 +122,27 @@
 
     def create_custom_gate_structure_QX2(self, qbit_num):
         r"""
         This method is called to create custom gate structure for the decomposition on IBM QX2
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
-        # creating an instance of the wrapper class qgd_Gates_Block
-        Gates_Block_ret = qgd_Gates_Block( qbit_num )
+        # creating an instance of the wrapper class Gates_Block
+        Gates_Block_ret = Gates_Block( qbit_num )
 
         disentangle_qbit = qbit_num - 1 
 
         
 
         for qbit in range(0, disentangle_qbit ):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
 
             if qbit == 0:
 
                 # add U3 fate to the block
                 Theta = True
                 Phi = False
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_Unitary.py` & `squander-1.8.0/qgd_python/decomposition/test/test_Unitary.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,39 +15,39 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
 ## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \brief Functionality test cases for the N_Qubit_Decomposition_adaptive class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
 
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition_adaptive import qgd_N_Qubit_Decomposition_adaptive
+from squander import N_Qubit_Decomposition_adaptive
 from scipy.io import loadmat
 
 def test_unitary():
 	# load the unitary from file
 	data = loadmat('Umtx.mat')
 	# The unitary to be decomposed  
 	Umtx = data['Umtx']
 	# creating a class to decompose the unitary
-	cDecompose = qgd_N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
+	cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, level_limit_max=5, level_limit_min=0 )
 	Umtx_assert = cDecompose.get_Unitary()
 
 	assert(np.sum(np.abs(Umtx_assert-Umtx.conj().T))<0.00001)
 
 	Umtx_assert[0,0]=1
 	cDecompose.set_Unitary(Umtx_assert)
 	Umtx_assert_new=cDecompose.get_Unitary()
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_decomposition.py` & `squander-1.8.0/qgd_python/decomposition/test/test_decomposition.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,100 +15,100 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
 ## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \brief Functionality test cases for the N_Qubit_Decomposition class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
-from qgd_python.utils import get_unitary_from_qiskit_circuit
+from squander import utils
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
 
 class Test_Decomposition:
     """This is a test class of the python iterface to the decompsition classes of the QGD package"""
 
-    def ctest_N_Qubit_Decomposition_creation(self):
+    def test_N_Qubit_Decomposition_creation(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of class N_Qubit_Decomposition.
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
+        from squander import N_Qubit_Decomposition
 
         # the number of qubits spanning the unitary
         qbit_num = 3
 
         # determine the soze of the unitary to be decomposed
         matrix_size = int(2**qbit_num)
    
         # creating a random unitary to be decomposed
         Umtx = unitary_group.rvs(matrix_size)
     
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition( Umtx.conj().T, optimize_layer_num=False, initial_guess="random" )
+        decomp = N_Qubit_Decomposition( Umtx.conj().T, optimize_layer_num=False, initial_guess="random" )
 
     def test_N_Qubit_Decomposition_3qubit(self):
         r"""
         This method is called by pytest. 
         Test to decompose a 3-qubit unitary
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
+        from squander import N_Qubit_Decomposition
 
         # the number of qubits spanning the unitary
         qbit_num = 3
 
         # determine the soze of the unitary to be decomposed
         matrix_size = int(2**qbit_num)
    
         # creating a random unitary to be decomposed
         Umtx = unitary_group.rvs(matrix_size)
 
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition( Umtx )
+        decomp = N_Qubit_Decomposition( Umtx )
 
         # start the decomposition
         decomp.Start_Decomposition(prepare_export=True)
 
         decomp.List_Gates()
 
     def test_N_Qubit_Decomposition_Qiskit_export(self):
         r"""
         This method is called by pytest. 
         Test to decompose a 2-qubit unitary and retrive the corresponding Qiskit circuit
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
+        from squander import N_Qubit_Decomposition
 
         # the number of qubits spanning the unitary
         qbit_num = 2
 
         # determine the soze of the unitary to be decomposed
         matrix_size = int(2**qbit_num)
    
         # creating a random unitary to be decomposed
         Umtx = unitary_group.rvs(matrix_size)
 
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition( Umtx.conj().T )
+        decomp = N_Qubit_Decomposition( Umtx.conj().T )
 
         # set the number of block to be optimized in one shot
         decomp.set_Optimization_Blocks( 20 )
 
         # setting the verbosity of the decomposition
         decomp.set_Verbose( 3 )
 
@@ -129,15 +129,15 @@
 
         from qiskit import execute
         import numpy.linalg as LA
     
         # test the decomposition of the matrix
     
         # the unitary matrix from the result object
-        decomposed_matrix = np.asarray( get_unitary_from_qiskit_circuit( quantum_circuit ) )
+        decomposed_matrix = np.asarray( utils.get_unitary_from_qiskit_circuit( quantum_circuit ) )
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
     
         product_matrix = np.eye(matrix_size)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error =  (np.real(np.trace(product_matrix)))/2
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_fmo.py` & `squander-1.8.0/qgd_python/decomposition/test/test_fmo.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 import numpy as np
 import scipy.constants as cnst
 import scipy.linalg as linalg
 
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition_custom import qgd_N_Qubit_Decomposition_custom
+from squander import N_Qubit_Decomposition
+from squander import N_Qubit_Decomposition_custom
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 from qiskit import assemble,Aer
 from qiskit import execute
-from qgd_python.utils import get_unitary_from_qiskit_circuit
+from squander import utils
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
@@ -25,26 +25,26 @@
     def create_custom_gate_structure_lin_3qubit(self, layer_num=2):
         """
         Add layers to disentangle the 3rd qubit from the others
         linear chain with IBM native operations
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
         qbit_num = 3
 
-        # creating an instance of the wrapper class qgd_Gates_Block
-        Gates_Block_ret = qgd_Gates_Block( qbit_num )
+        # creating an instance of the wrapper class Gates_Block
+        Gates_Block_ret = Gates_Block( qbit_num )
 
 
         for idx in range(0,layer_num,2):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
 #Rz Ry Rz = Rz Sx Rz Sx^+ Rz
 
             Layer.add_RZ( 2 ) 
             #Layer.add_RY( 2 ) 
             Layer.add_SX( 2 ) 
             Layer.add_RZ( 2 )
@@ -60,16 +60,16 @@
 
             # add CNOT gate to the block
             Layer.add_CNOT( 1, 2)
 
             Gates_Block_ret.add_Gates_Block( Layer )
 
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
             Layer.add_RZ( 1 ) 
             #Layer.add_RY( 1 ) 
             Layer.add_SX( 1 ) 
             Layer.add_RZ( 1 )
             Layer.add_X( 1 )  
             Layer.add_SX( 1 )
@@ -95,28 +95,28 @@
     def create_custom_gate_structure_lin_2qubit(self, layer_num=1, Gates_Block_ret=None):
         """
         Add layers to disentangle the final 2 qubits
         linear chain with IBM native operations
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
 
         qbit_num = 2
 
         if Gates_Block_ret == None:
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Gates_Block_ret = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Gates_Block_ret = Gates_Block( qbit_num )
 
 
         for idx in range(layer_num):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
             Layer.add_RZ( 1 ) 
             #Layer.add_RY( 1 ) 
             Layer.add_SX( 1 ) 
             Layer.add_RZ( 1 )
             Layer.add_X( 1 )  
             Layer.add_SX( 1 )
@@ -140,27 +140,27 @@
 
     def create_custom_gate_structure_finalyzing(self, qbit_num, Gates_Block_ret=None):
         """
         Rotating qubits into state |0>
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
 
 
         if Gates_Block_ret == None:
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Gates_Block_ret = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Gates_Block_ret = Gates_Block( qbit_num )
 
 
         for idx in range(qbit_num):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
             Layer.add_RZ( idx ) 
             #Layer.add_RY( idx ) 
             Layer.add_SX( idx ) 
             Layer.add_RZ( idx )
             Layer.add_X( idx )  
             Layer.add_SX( idx )
@@ -210,15 +210,15 @@
         # create custom gate structure for the decomposition
         gate_structure = self.create_custom_gate_structure_lin_3qubit(14)
         gate_structure = self.create_custom_gate_structure_lin_2qubit(3, gate_structure)
         gate_structure = self.create_custom_gate_structure_finalyzing(qbit_num, gate_structure)
 
 
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition_custom( Umtx.conj().T, initial_guess="random" )
+        decomp = N_Qubit_Decomposition_custom( Umtx.conj().T, initial_guess="random" )
 
         # adding custom gate structure to the decomposition
         decomp.set_Gate_Structure( gate_structure )
 
 
         # setting the tolerance of the optimization process. The final error of the decomposition would scale with the square root of this value.
         decomp.set_Optimization_Tolerance( 1e-6 )
@@ -236,15 +236,15 @@
 	
         # get the decomposing operations
         quantum_circuit = decomp.get_Quantum_Circuit()
         print(quantum_circuit )
 	
         # test the decomposition of the matrix
         # the unitary matrix from the result object
-        decomposed_matrix = np.asarray( get_unitary_from_qiskit_circuit( quantum_circuit ) )
+        decomposed_matrix = np.asarray( utils.get_unitary_from_qiskit_circuit( quantum_circuit ) )
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
 		
         product_matrix = np.eye(matrix_size)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error =  (np.real(np.trace(product_matrix)))/2
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_heavy_hex.py` & `squander-1.8.0/qgd_python/decomposition/test/test_heavy_hex.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,24 +14,23 @@
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 """
-## \file test_decomposition.py
-## \brief Functionality test cases for the qgd_N_Qubit_Decomposition class.
+## \file test_heavy_hex.py
+## \brief Functionality test cases for the N_Qubit_Decomposition class.
 
 
 
 # cerate unitary q-bit matrix
 from scipy.stats import unitary_group
 import numpy as np
-from qgd_python.utils import get_unitary_from_qiskit_circuit
-
+from squander import utils
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
     MPI_imported = False
 
@@ -42,27 +41,27 @@
     def test_N_Qubit_Decomposition_Heavy_Hex(self):
         r"""
         This method is called by pytest. 
         Test to define custom gate structure in the decomposition
 
         """
 
-        from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition
+        from squander import N_Qubit_Decomposition
 
         # the number of qubits spanning the unitary
         qbit_num = 4
 
         # determine the soze of the unitary to be decomposed
         matrix_size = int(2**qbit_num)
    
         # creating a random unitary to be decomposed
         Umtx = unitary_group.rvs(matrix_size)
     
         # creating an instance of the C++ class
-        decomp = qgd_N_Qubit_Decomposition( Umtx.conj().T)
+        decomp = N_Qubit_Decomposition( Umtx.conj().T)
 
 
         # create custom gate structure
         gate_structure = { 4: self.create_custom_gate_structure_heavy_hex_4(4), 3: self.create_custom_gate_structure_heavy_hex_3(3)}        
 
 
         # adding custom gate structure to the decomposition
@@ -86,15 +85,15 @@
         quantum_circuit = decomp.get_Quantum_Circuit()
 
         from qiskit import execute
         import numpy.linalg as LA
     
     
         # the unitary matrix from the result object
-        decomposed_matrix = np.asarray( get_unitary_from_qiskit_circuit( quantum_circuit ) )
+        decomposed_matrix = np.asarray( utils.get_unitary_from_qiskit_circuit( quantum_circuit ) )
         product_matrix = np.dot(Umtx,decomposed_matrix.conj().T)
         phase = np.angle(product_matrix[0,0])
         product_matrix = product_matrix*np.exp(-1j*phase)
     
         product_matrix = np.eye(matrix_size)*2 - product_matrix - product_matrix.conj().T
         # the error of the decomposition
         decomposition_error =  (np.real(np.trace(product_matrix)))/2
@@ -108,27 +107,27 @@
 
     def create_custom_gate_structure_heavy_hex_3(self, qbit_num):
         r"""
         This method is called to create custom gate structure for the decomposition on IBM QX2
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
-        # creating an instance of the wrapper class qgd_Gates_Block
-        Gates_Block_ret = qgd_Gates_Block( qbit_num )
+        # creating an instance of the wrapper class Gates_Block
+        Gates_Block_ret = Gates_Block( qbit_num )
 
         disentangle_qubit = qbit_num - 1 
 
         
 
         for qbit in range(0, disentangle_qubit ):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
 
             if qbit == 0:
 
                 # add U3 fate to the block
                 Theta = True
                 Phi = False
@@ -177,27 +176,27 @@
 
     def create_custom_gate_structure_heavy_hex_4(self, qbit_num):
         r"""
         This method is called to create custom gate structure for the decomposition on IBM QX2
 
         """
 
-        from qgd_python.gates.qgd_Gates_Block import qgd_Gates_Block
+        from squander import Gates_Block
 
-        # creating an instance of the wrapper class qgd_Gates_Block
-        Gates_Block_ret = qgd_Gates_Block( qbit_num )
+        # creating an instance of the wrapper class Gates_Block
+        Gates_Block_ret = Gates_Block( qbit_num )
 
         disentangle_qubit = qbit_num - 1 
 
         
 
         for qbit in range(0, disentangle_qubit ):
 
-            # creating an instance of the wrapper class qgd_Gates_Block
-            Layer = qgd_Gates_Block( qbit_num )
+            # creating an instance of the wrapper class Gates_Block
+            Layer = Gates_Block( qbit_num )
 
 
             if qbit == 0:
 
                 # add U3 fate to the block
                 Theta = True
                 Phi = False
```

### Comparing `squander-1.7.4/qgd_python/decomposition/test/test_parametric_circuit.py` & `squander-1.8.0/qgd_python/decomposition/test/test_parametric_circuit.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,16 +9,16 @@
 
 from qiskit import QuantumCircuit, transpile
 import numpy as np
 
 
 from qiskit import execute
 
-from qgd_python.utils import get_unitary_from_qiskit_circuit
-from qgd_python.decomposition.qgd_N_Qubit_Decomposition_custom import qgd_N_Qubit_Decomposition_custom
+from squander import utils
+from squander import N_Qubit_Decomposition_custom
 
 
 
 try:
     from mpi4py import MPI
     MPI_imported = True
 except ModuleNotFoundError:
@@ -122,21 +122,21 @@
 	#print(qc_trial)
 
 	##### getting the alpha dependent unitary
 	qc_orig = pauli_exponent(alpha )
 	qc_orig = transpile(qc_orig, optimization_level=3, basis_gates=['cx', 'u3'], layout_method='sabre')
 	#print('global phase: ', qc_orig.global_phase)
 
-	Umtx_orig = get_unitary_from_qiskit_circuit( qc_orig )
+	Umtx_orig = utils.get_unitary_from_qiskit_circuit( qc_orig )
         
 	iteration_max = 10
 	
 	for jdx in range(iteration_max):
         
-		cDecompose = qgd_N_Qubit_Decomposition_custom( Umtx_orig.conj().T )
+		cDecompose = N_Qubit_Decomposition_custom( Umtx_orig.conj().T )
 
 		# setting the tolerance of the optimization process. The final error of the decomposition would scale with the square root of this value.
 		cDecompose.set_Optimization_Tolerance( 1e-5 )
 
 		# importing the quantum circuit
 		cDecompose.import_Qiskit_Circuit(qc_trial)
 		
@@ -158,15 +158,15 @@
 		
 		# getting the new optimized parameters
 		optimized_parameters_loc = cDecompose.get_Optimized_Parameters()
 
 		qc_final = cDecompose.get_Quantum_Circuit()
 
 		# get the unitary of the final circuit
-		Umtx_recheck = get_unitary_from_qiskit_circuit( qc_final )
+		Umtx_recheck = utils.get_unitary_from_qiskit_circuit( qc_final )
 
 		# get the decomposition error
 		decomposition_error =  get_unitary_distance(Umtx_orig, Umtx_recheck)
 		print('recheck decomposition error: ', decomposition_error)
 
 		if decomposition_error < 1e-3:
 			break
```

### Comparing `squander-1.7.4/qgd_python/gates/CMakeLists.txt` & `squander-1.8.0/qgd_python/gates/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/gates/qgd_CH.cpp` & `squander-1.8.0/qgd_python/gates/qgd_X.cpp`

 * *Files 16% similar despite different names*

```diff
@@ -14,178 +14,222 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_CH.cpp
-\brief Python interface for the CH (i.e. controlled Hadamard) gate class
+\file qgd_X.cpp
+\brief Python interface for the X gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "CH.h"
+#include "X.h"
 #include "numpy_interface.h"
 
 
 
+
 /**
-@brief Type definition of the  qgd_CH Python class of the  qgd_CH module
+@brief Type definition of the qgd_X Python class of the qgd_X module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the CH gate
-    CH* gate;
-} qgd_CH;
+    /// Pointer to the C++ class of the X gate
+    X* gate;
+} qgd_X;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
-@param qbit_num Number of qubits spanning the unitary
-@param target_qbit The Id (0<= target_qbit < qbit_num ) of the target qubit.
-@param control_qbit The Id (0<= control_qbit < qbit_num ) of the control qubit.
-@return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
+@param qbit_num The number of qubits spanning the operation.
+@param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-CH* 
-create_CH( int qbit_num, int target_qbit, int control_qbit ) {
+X* 
+create_X( int qbit_num, int target_qbit ) {
 
-    return new CH( qbit_num, target_qbit, control_qbit );
+    return new X( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_CH( CH*  instance ) {
+release_X( X*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
+
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CH is destroyed
-@param self A pointer pointing to an instance of class  qgd_CH.
+@brief Method called when a python instance of the class qgd_X is destroyed
+@param self A pointer pointing to an instance of class qgd_X.
 */
 static void
- qgd_CH_dealloc(qgd_CH *self)
+qgd_X_dealloc(qgd_X *self)
 {
-    release_CH( self->gate );
+
+    // release the X gate
+    release_X( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CH is allocated
-@param type A pointer pointing to a structure describing the type of the class  qgd_CH.
+@brief Method called when a python instance of the class qgd_X is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_X.
 */
 static PyObject *
- qgd_CH_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_X_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_CH *self;
-    self = (qgd_CH *) type->tp_alloc(type, 0);
+    qgd_X *self;
+    self = (qgd_X *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CH is initialized
-@param self A pointer pointing to an instance of the class  qgd_CH.
-@param args A tuple of the input arguments: qbit_num (int), target_qbit (int), control_qbit (int)
+@brief Method called when a python instance of the class qgd_X is initialized
+@param self A pointer pointing to an instance of the class qgd_X.
+@param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
- qgd_CH_init(qgd_CH *self, PyObject *args, PyObject *kwds)
+qgd_X_init(qgd_X *self, PyObject *args, PyObject *kwds)
 {
-    static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", (char*)"control_qbit", NULL};
+    static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
-    int control_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
-    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|iii", kwlist,
-                                     &qbit_num, &target_qbit, &control_qbit))
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
+                                     &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_CH( qbit_num, target_qbit, control_qbit );
+        self->gate = create_X( qbit_num, target_qbit );
     }
+
+
+
+
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
-
 static PyObject *
-qgd_CH_get_Matrix( qgd_CH *self ) {
+qgd_X_get_Matrix( qgd_X *self ) {
 
-    Matrix CH_mtx = self->gate->get_matrix(  );
+   
+    Matrix X_mtx = self->gate->get_matrix(  );
     
     // convert to numpy array
-    CH_mtx.set_owner(false);
-    PyObject *CH_py = matrix_to_numpy( CH_mtx );
+    X_mtx.set_owner(false);
+    PyObject *X_py = matrix_to_numpy( X_mtx );
 
-    return CH_py;
+
+    return X_py;
 }
 
 
+
 /**
-@brief Structure containing metadata about the members of class  qgd_CH.
+@brief Call to apply the gate operation on the inut matrix
 */
-static PyMemberDef  qgd_CH_members[] = {
-    {NULL}  /* Sentinel */
-};
+static PyObject *
+qgd_X_apply_to( qgd_X *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
+
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+    PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+    self->gate->apply_to( unitary_mtx );
+    
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
+}
 
 
 
 /**
-@brief Structure containing metadata about the methods of class  qgd_CH.
+@brief Structure containing metadata about the members of class qgd_X.
 */
-//static PyMethodDef  qgd_CH_methods[] = {
-//    {NULL}  /* Sentinel */
-//};
+static PyMemberDef qgd_X_members[] = {
+    {NULL}  /* Sentinel */
+};
+
 
 /**
-@brief Structure containing metadata about the methods of class qgd_U3.
+@brief Structure containing metadata about the methods of class qgd_X.
 */
-static PyMethodDef qgd_CH_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_CH_get_Matrix, METH_NOARGS,
+static PyMethodDef qgd_X_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_X_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_X_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class  qgd_CH.
+@brief A structure describing the type of the class qgd_X.
 */
-static PyTypeObject  qgd_CH_Type = {
+static PyTypeObject  qgd_X_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_CH.qgd_CH", /*tp_name*/
-  sizeof(qgd_CH), /*tp_basicsize*/
+  "qgd_X.qgd_X", /*tp_name*/
+  sizeof(qgd_X), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor)  qgd_CH_dealloc, /*tp_dealloc*/
+  (destructor) qgd_X_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -203,32 +247,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a CH gate of the QGD package.", /*tp_doc*/
+  "Object to represent a X gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-   qgd_CH_methods, /*tp_methods*/
-   qgd_CH_members, /*tp_members*/
+  qgd_X_methods, /*tp_methods*/
+  qgd_X_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc)  qgd_CH_init, /*tp_init*/
+  (initproc) qgd_X_init, /*tp_init*/
   0, /*tp_alloc*/
-   qgd_CH_new, /*tp_new*/
+  qgd_X_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -245,42 +289,46 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_CH_Module = {
+static PyModuleDef  qgd_X_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_CH",
-    .m_doc = "Python binding for QGD CH gate",
+    .m_name = "qgd_X",
+    .m_doc = "Python binding for QGD X gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_CH(void)
+PyInit_qgd_X(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_CH_Type) < 0)
+    if (PyType_Ready(& qgd_X_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_CH_Module);
+    m = PyModule_Create(& qgd_X_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_CH_Type);
-    if (PyModule_AddObject(m, "qgd_CH", (PyObject *) & qgd_CH_Type) < 0) {
-        Py_DECREF(& qgd_CH_Type);
+    Py_INCREF(& qgd_X_Type);
+    if (PyModule_AddObject(m, "qgd_X", (PyObject *) & qgd_X_Type) < 0) {
+        Py_DECREF(& qgd_X_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
 
 
 
+
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_CNOT.cpp` & `squander-1.8.0/qgd_python/gates/qgd_CNOT.cpp`

 * *Files 20% similar despite different names*

```diff
@@ -142,31 +142,82 @@
     PyObject *CNOT_py = matrix_to_numpy( CNOT_mtx );
 
     return CNOT_py;
 }
 
 
 
+/**
+@brief Call to apply the gate operation on the inut matrix
+*/
+static PyObject *
+qgd_CNOT_apply_to( qgd_CNOT *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
+
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+
+    if ( PyArray_Check(unitary_arg) && PyArray_IS_C_CONTIGUOUS(unitary_arg) ) {
+        Py_INCREF(unitary_arg);
+    }
+    else {
+        unitary_arg = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+    }
+
+   PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+    self->gate->apply_to( unitary_mtx );
+    
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
+}
+
+
+
 
 /**
 @brief Structure containing metadata about the members of class  qgd_CNOT.
 */
 static PyMemberDef  qgd_CNOT_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
-
 /**
 @brief Structure containing metadata about the methods of class  qgd_CNOT.
 */
 static PyMethodDef  qgd_CNOT_methods[] = {
     {"get_Matrix", (PyCFunction) qgd_CNOT_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_CNOT_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
 @brief A structure describing the type of the class  qgd_CNOT.
 */
@@ -253,14 +304,17 @@
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
 PyInit_qgd_CNOT(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
     if (PyType_Ready(& qgd_CNOT_Type) < 0)
         return NULL;
 
     m = PyModule_Create(& qgd_CNOT_Module);
     if (m == NULL)
         return NULL;
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_CZ.cpp` & `squander-1.8.0/qgd_python/gates/qgd_CH.cpp`

 * *Files 21% similar despite different names*

```diff
@@ -14,104 +14,104 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_CZ.cpp
-\brief Python interface for the CZ gate class
+\file qgd_CH.cpp
+\brief Python interface for the CH (i.e. controlled Hadamard) gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "CZ.h"
+#include "CH.h"
 #include "numpy_interface.h"
 
 
 
 /**
-@brief Type definition of the  qgd_CZ Python class of the  qgd_CZ module
+@brief Type definition of the  qgd_CH Python class of the  qgd_CH module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the CZ gate
-    CZ* gate;
-} qgd_CZ;
+    /// Pointer to the C++ class of the CH gate
+    CH* gate;
+} qgd_CH;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num Number of qubits spanning the unitary
 @param target_qbit The Id (0<= target_qbit < qbit_num ) of the target qubit.
 @param control_qbit The Id (0<= control_qbit < qbit_num ) of the control qubit.
 @return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
 */
-CZ* 
-create_CZ( int qbit_num, int target_qbit, int control_qbit ) {
+CH* 
+create_CH( int qbit_num, int target_qbit, int control_qbit ) {
 
-    return new CZ( qbit_num, target_qbit, control_qbit );
+    return new CH( qbit_num, target_qbit, control_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_CZ( CZ*  instance ) {
+release_CH( CH*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CZ is destroyed
-@param self A pointer pointing to an instance of class  qgd_CZ.
+@brief Method called when a python instance of the class  qgd_CH is destroyed
+@param self A pointer pointing to an instance of class  qgd_CH.
 */
 static void
- qgd_CZ_dealloc(qgd_CZ *self)
+ qgd_CH_dealloc(qgd_CH *self)
 {
-    release_CZ( self->gate );
+    release_CH( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CZ is allocated
-@param type A pointer pointing to a structure describing the type of the class  qgd_CZ.
+@brief Method called when a python instance of the class  qgd_CH is allocated
+@param type A pointer pointing to a structure describing the type of the class  qgd_CH.
 */
 static PyObject *
- qgd_CZ_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+ qgd_CH_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_CZ *self;
-    self = (qgd_CZ *) type->tp_alloc(type, 0);
+    qgd_CH *self;
+    self = (qgd_CH *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class  qgd_CZ is initialized
-@param self A pointer pointing to an instance of the class  qgd_CZ.
+@brief Method called when a python instance of the class  qgd_CH is initialized
+@param self A pointer pointing to an instance of the class  qgd_CH.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), control_qbit (int)
 @param kwds A tuple of keywords
 */
 static int
- qgd_CZ_init(qgd_CZ *self, PyObject *args, PyObject *kwds)
+ qgd_CH_init(qgd_CH *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", (char*)"control_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
     int control_qbit = -1;
 
     if (PyArray_API == NULL) {
@@ -119,67 +119,127 @@
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|iii", kwlist,
                                      &qbit_num, &target_qbit, &control_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_CZ( qbit_num, target_qbit, control_qbit );
+        self->gate = create_CH( qbit_num, target_qbit, control_qbit );
     }
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
 
 static PyObject *
-qgd_CZ_get_Matrix( qgd_CZ *self ) {
+qgd_CH_get_Matrix( qgd_CH *self ) {
 
-    Matrix CZ_mtx = self->gate->get_matrix(  );
+    Matrix CH_mtx = self->gate->get_matrix(  );
     
     // convert to numpy array
-    CZ_mtx.set_owner(false);
-    PyObject *CZ_py = matrix_to_numpy( CZ_mtx );
+    CH_mtx.set_owner(false);
+    PyObject *CH_py = matrix_to_numpy( CH_mtx );
 
-    return CZ_py;
+    return CH_py;
 }
 
 
 
+
 /**
-@brief Structure containing metadata about the members of class  qgd_CZ.
+@brief Call to apply the gate operation on the inut matrix
 */
-static PyMemberDef  qgd_CZ_members[] = {
+static PyObject *
+qgd_CH_apply_to( qgd_CH *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
+
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+
+    if ( PyArray_Check(unitary_arg) && PyArray_IS_C_CONTIGUOUS(unitary_arg) ) {
+        Py_INCREF(unitary_arg);
+    }
+    else {
+        unitary_arg = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+    }
+
+   PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+    self->gate->apply_to( unitary_mtx );
+    
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
+}
+
+
+
+
+/**
+@brief Structure containing metadata about the members of class  qgd_CH.
+*/
+static PyMemberDef  qgd_CH_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
+/**
+@brief Structure containing metadata about the methods of class  qgd_CH.
+*/
+//static PyMethodDef  qgd_CH_methods[] = {
+//    {NULL}  /* Sentinel */
+//};
 
 /**
-@brief Structure containing metadata about the methods of class  qgd_CZ.
+@brief Structure containing metadata about the methods of class qgd_U3.
 */
-static PyMethodDef  qgd_CZ_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_CZ_get_Matrix, METH_NOARGS,
+static PyMethodDef qgd_CH_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_CH_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_CH_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class  qgd_CZ.
+@brief A structure describing the type of the class  qgd_CH.
 */
-static PyTypeObject  qgd_CZ_Type = {
+static PyTypeObject  qgd_CH_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_CZ.qgd_CZ", /*tp_name*/
-  sizeof(qgd_CZ), /*tp_basicsize*/
+  "qgd_CH.qgd_CH", /*tp_name*/
+  sizeof(qgd_CH), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor)  qgd_CZ_dealloc, /*tp_dealloc*/
+  (destructor)  qgd_CH_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -197,32 +257,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a CZ gate of the QGD package.", /*tp_doc*/
+  "Object to represent a CH gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-   qgd_CZ_methods, /*tp_methods*/
-   qgd_CZ_members, /*tp_members*/
+   qgd_CH_methods, /*tp_methods*/
+   qgd_CH_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc)  qgd_CZ_init, /*tp_init*/
+  (initproc)  qgd_CH_init, /*tp_init*/
   0, /*tp_alloc*/
-   qgd_CZ_new, /*tp_new*/
+   qgd_CH_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -239,39 +299,44 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_CZ_Module = {
+static PyModuleDef  qgd_CH_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_CZ",
-    .m_doc = "Python binding for QGD CZ gate",
+    .m_name = "qgd_CH",
+    .m_doc = "Python binding for QGD CH gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_CZ(void)
+PyInit_qgd_CH(void)
 {
+
+    // initialize Numpy API
+    import_array();
+
+
     PyObject *m;
-    if (PyType_Ready(& qgd_CZ_Type) < 0)
+    if (PyType_Ready(& qgd_CH_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_CZ_Module);
+    m = PyModule_Create(& qgd_CH_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_CZ_Type);
-    if (PyModule_AddObject(m, "qgd_CZ", (PyObject *) & qgd_CZ_Type) < 0) {
-        Py_DECREF(& qgd_CZ_Type);
+    Py_INCREF(& qgd_CH_Type);
+    if (PyModule_AddObject(m, "qgd_CH", (PyObject *) & qgd_CH_Type) < 0) {
+        Py_DECREF(& qgd_CH_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_Gates_Block.cpp` & `squander-1.8.0/qgd_python/gates/qgd_Gates_Block.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -696,14 +696,85 @@
 
     Py_DECREF(parameters_arr);
 
     return mtx_py;
 }
 
 
+
+/**
+@brief Get the number of free parameters in the gate structure used for the decomposition
+*/
+static PyObject *
+qgd_Gates_Block_get_Parameter_Num( qgd_Gates_Block *self ) {
+
+    int parameter_num = self->gate->get_parameter_num();
+
+    return Py_BuildValue("i", parameter_num);
+}
+
+
+
+/**
+@brief Call to apply the gate operation on the inut matrix
+*/
+static PyObject *
+qgd_Gates_Block_apply_to( qgd_Gates_Block *self, PyObject *args ) {
+
+    PyObject * parameters_arr = NULL;
+    PyObject * unitary_arg = NULL;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|OO", &parameters_arr, &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+    
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arr) ) {
+        Py_INCREF(parameters_arr);
+    }
+    else {
+        parameters_arr = PyArray_FROM_OTF(parameters_arr, NPY_DOUBLE, NPY_ARRAY_IN_ARRAY);
+    }
+
+    // get the C++ wrapper around the data
+    Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
+
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+    PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+
+    self->gate->apply_to( parameters_mtx, unitary_mtx );
+    
+    Py_DECREF(parameters_arr);
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
+}
+
+
+
+
+
 static PyMethodDef qgd_Gates_Block_Methods[] = {
     {"add_U3", (PyCFunction) qgd_Gates_Block_add_U3, METH_VARARGS | METH_KEYWORDS,
      "Call to add a U3 gate to the front of the gate structure"
     },
     {"add_RX", (PyCFunction) qgd_Gates_Block_add_RX, METH_VARARGS | METH_KEYWORDS,
      "Call to add a RX gate to the front of the gate structure"
     },
@@ -750,14 +821,20 @@
     {"convert_to_DFE_gates", (PyCFunction) qgd_Gates_block_convert_to_DFE_gates, METH_VARARGS,
      "Call to convert to DFE gates."
     },
 #endif
     {"get_Matrix", (PyCFunction) qgd_Gates_Block_get_Matrix, METH_VARARGS,
      "Method to get the matrix of the operation."
     },
+    {"get_Parameter_Num", (PyCFunction) qgd_Gates_Block_get_Parameter_Num, METH_NOARGS,
+     "Call to get the number of free parameters in the circuit"
+    },
+    {"apply_to", (PyCFunction) qgd_Gates_Block_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
 @brief A structure describing the type of the class Gates_Block.
 */
@@ -842,14 +919,18 @@
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
 PyInit_qgd_Gates_Block(void)
 {
+
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
     if (PyType_Ready(&qgd_Gates_Block_Type) < 0)
         return NULL;
 
     m = PyModule_Create(&qgd_Gates_Block_Module);
     if (m == NULL)
         return NULL;
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_RX.cpp` & `squander-1.8.0/qgd_python/gates/qgd_Z.cpp`

 * *Files 17% similar despite different names*

```diff
@@ -14,131 +14,132 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_RX.cpp
-\brief Python interface for the RX gate class
+\file qgd_Z.cpp
+\brief Python interface for the Z gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "RX.h"
+#include "Z.h"
 #include "numpy_interface.h"
 
 
 
 
 /**
-@brief Type definition of the qgd_RX Python class of the qgd_RX module
+@brief Type definition of the qgd_Z Python class of the qgd_Z module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the RX gate
-    RX* gate;
-} qgd_RX;
+    /// Pointer to the C++ class of the X gate
+    Z* gate;
+} qgd_Z;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num The number of qubits spanning the operation.
 @param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-RX* 
-create_RX( int qbit_num, int target_qbit ) {
+Z* 
+create_Z( int qbit_num, int target_qbit ) {
 
-    return new RX( qbit_num, target_qbit );
+    return new Z( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_RX( RX*  instance ) {
+release_Z( Z*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_RX is destroyed
-@param self A pointer pointing to an instance of class qgd_RX.
+@brief Method called when a python instance of the class qgd_Z is destroyed
+@param self A pointer pointing to an instance of class qgd_Z.
 */
 static void
-qgd_RX_dealloc(qgd_RX *self)
+qgd_Z_dealloc(qgd_Z *self)
 {
 
-    // release the RX gate
-    release_RX( self->gate );
+    // release the X gate
+    release_Z( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RX is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_RX.
+@brief Method called when a python instance of the class qgd_Z is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_Z.
 */
 static PyObject *
-qgd_RX_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_Z_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_RX *self;
-    self = (qgd_RX *) type->tp_alloc(type, 0);
+    qgd_Z *self;
+    self = (qgd_Z *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RX is initialized
-@param self A pointer pointing to an instance of the class qgd_RX.
+@brief Method called when a python instance of the class qgd_Z is initialized
+@param self A pointer pointing to an instance of the class qgd_Z.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
-qgd_RX_init(qgd_RX *self, PyObject *args, PyObject *kwds)
+qgd_Z_init(qgd_Z *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
                                      &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_RX( qbit_num, target_qbit );
+        self->gate = create_Z( qbit_num, target_qbit );
     }
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
+/**
 static PyObject *
-qgd_RX_get_Matrix( qgd_RX *self, PyObject *args ) {
+qgd_Z_get_Matrix( qgd_Z *self, PyObject *args ) {
 
     PyObject * parameters_arr = NULL;
 
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &parameters_arr )) 
         return Py_BuildValue("i", -1);
@@ -152,55 +153,117 @@
     }
 
 
     // get the C++ wrapper around the data
     Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
 
-    Matrix RX_mtx = self->gate->get_matrix( parameters_mtx );
+    Matrix Z_mtx = self->gate->get_matrix(  );
     
     // convert to numpy array
-    RX_mtx.set_owner(false);
-    PyObject *RX_py = matrix_to_numpy( RX_mtx );
+    Z_mtx.set_owner(false);
+    PyObject *Z_py = matrix_to_numpy( Z_mtx );
 
 
     Py_DECREF(parameters_arr);
 
-    return RX_py;
+    return Z_py;
+}
+
+*/
+/**
+@brief Extract the optimized parameters
+@param start_index The index of the first inverse gate
+*/
+static PyObject *
+qgd_Z_get_Matrix( qgd_Z *self ) {
+
+   
+    Matrix Z_mtx = self->gate->get_matrix(  );
+    
+    // convert to numpy array
+    Z_mtx.set_owner(false);
+    PyObject *Z_py = matrix_to_numpy( Z_mtx );
+
+
+    return Z_py;
+}
+
+/**
+@brief Call to apply the gate operation on the inut matrix
+*/
+static PyObject *
+qgd_Z_apply_to( qgd_Z *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+    PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+    self->gate->apply_to( unitary_mtx );
+    
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
 }
 
 
+
 /**
-@brief Structure containing metadata about the members of class qgd_RX.
+@brief Structure containing metadata about the members of class qgd_Z.
 */
-static PyMemberDef qgd_RX_members[] = {
+static PyMemberDef qgd_Z_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_RX.
+@brief Structure containing metadata about the methods of class qgd_Z.
 */
-static PyMethodDef qgd_RX_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_RX_get_Matrix, METH_VARARGS,
+static PyMethodDef qgd_Z_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_Z_get_Matrix, METH_VARARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_Z_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_RX.
+@brief A structure describing the type of the class qgd_Z.
 */
-static PyTypeObject  qgd_RX_Type = {
+static PyTypeObject  qgd_Z_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_RX.qgd_RX", /*tp_name*/
-  sizeof(qgd_RX), /*tp_basicsize*/
+  "qgd_Z.qgd_Z", /*tp_name*/
+  sizeof(qgd_Z), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_RX_dealloc, /*tp_dealloc*/
+  (destructor) qgd_Z_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -218,32 +281,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a RX gate of the QGD package.", /*tp_doc*/
+  "Object to represent a X gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_RX_methods, /*tp_methods*/
-  qgd_RX_members, /*tp_members*/
+  qgd_Z_methods, /*tp_methods*/
+  qgd_Z_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_RX_init, /*tp_init*/
+  (initproc) qgd_Z_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_RX_new, /*tp_new*/
+  qgd_Z_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -260,39 +323,42 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_RX_Module = {
+static PyModuleDef  qgd_Z_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_RX",
-    .m_doc = "Python binding for QGD RX gate",
+    .m_name = "qgd_Z",
+    .m_doc = "Python binding for QGD X gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_RX(void)
+PyInit_qgd_Z(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_RX_Type) < 0)
+    if (PyType_Ready(& qgd_Z_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_RX_Module);
+    m = PyModule_Create(& qgd_Z_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_RX_Type);
-    if (PyModule_AddObject(m, "qgd_RX", (PyObject *) & qgd_RX_Type) < 0) {
-        Py_DECREF(& qgd_RX_Type);
+    Py_INCREF(& qgd_Z_Type);
+    if (PyModule_AddObject(m, "qgd_Z", (PyObject *) & qgd_Z_Type) < 0) {
+        Py_DECREF(& qgd_Z_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_RY.cpp` & `squander-1.8.0/qgd_python/gates/qgd_SYC.cpp`

 * *Files 17% similar despite different names*

```diff
@@ -14,192 +14,217 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_RY.cpp
-\brief Python interface for the RY gate class
+\file qgd_SYC.cpp
+\brief Python interface for the Sycamore gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "RY.h"
+#include "SYC.h"
 #include "numpy_interface.h"
 
 
 
-
 /**
-@brief Type definition of the qgd_RY Python class of the qgd_RY module
+@brief Type definition of the  qgd_SYC Python class of the  qgd_SYC module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the RY gate
-    RY* gate;
-} qgd_RY;
+    /// Pointer to the C++ class of the SYC gate
+    SYC* gate;
+} qgd_SYC;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
-@param qbit_num The number of qubits spanning the operation.
-@param target_qbit The 0<=ID<qbit_num of the target qubit.
+@param qbit_num Number of qubits spanning the unitary
+@param target_qbit The Id (0<= target_qbit < qbit_num ) of the target qubit.
+@param control_qbit The Id (0<= control_qbit < qbit_num ) of the control qubit.
+@return Return with a void pointer pointing to an instance of N_Qubit_Decomposition class.
 */
-RY* 
-create_RY( int qbit_num, int target_qbit ) {
+SYC* 
+create_SYC( int qbit_num, int target_qbit, int control_qbit ) {
 
-    return new RY( qbit_num, target_qbit );
+    return new SYC( qbit_num, target_qbit, control_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_RY( RY*  instance ) {
+release_SYC( SYC*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
-
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_RY is destroyed
-@param self A pointer pointing to an instance of class qgd_RY.
+@brief Method called when a python instance of the class  qgd_SYC is destroyed
+@param self A pointer pointing to an instance of class  qgd_SYC.
 */
 static void
-qgd_RY_dealloc(qgd_RY *self)
+ qgd_SYC_dealloc(qgd_SYC *self)
 {
-
-    // release the RY gate
-    release_RY( self->gate );
+    release_SYC( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RY is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_RY.
+@brief Method called when a python instance of the class  qgd_SYC is allocated
+@param type A pointer pointing to a structure describing the type of the class  qgd_SYC.
 */
 static PyObject *
-qgd_RY_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+ qgd_SYC_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_RY *self;
-    self = (qgd_RY *) type->tp_alloc(type, 0);
+    qgd_SYC *self;
+    self = (qgd_SYC *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RY is initialized
-@param self A pointer pointing to an instance of the class qgd_RY.
-@param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
+@brief Method called when a python instance of the class  qgd_SYC is initialized
+@param self A pointer pointing to an instance of the class  qgd_SYC.
+@param args A tuple of the input arguments: qbit_num (int), target_qbit (int), control_qbit (int)
 @param kwds A tuple of keywords
 */
 static int
-qgd_RY_init(qgd_RY *self, PyObject *args, PyObject *kwds)
+ qgd_SYC_init(qgd_SYC *self, PyObject *args, PyObject *kwds)
 {
-    static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
+    static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", (char*)"control_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
+    int control_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
-    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
-                                     &qbit_num, &target_qbit))
+    if (!PyArg_ParseTupleAndKeywords(args, kwds, "|iii", kwlist,
+                                     &qbit_num, &target_qbit, &control_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_RY( qbit_num, target_qbit );
+        self->gate = create_SYC( qbit_num, target_qbit, control_qbit );
     }
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
+
+static PyObject *
+qgd_SYC_get_Matrix( qgd_SYC *self ) {
+
+    Matrix SYC_mtx = self->gate->get_matrix(  );
+    
+    // convert to numpy array
+    SYC_mtx.set_owner(false);
+    PyObject *SYC_py = matrix_to_numpy( SYC_mtx );
+
+    return SYC_py;
+}
+
+
+
+/**
+@brief Call to apply the gate operation on the inut matrix
+*/
 static PyObject *
-qgd_RY_get_Matrix( qgd_RY *self, PyObject *args ) {
+qgd_SYC_apply_to( qgd_SYC *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
 
-    PyObject * parameters_arr = NULL;
 
 
     // parsing input arguments
-    if (!PyArg_ParseTuple(args, "|O", &parameters_arr )) 
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
         return Py_BuildValue("i", -1);
 
-    
-    if ( PyArray_IS_C_CONTIGUOUS(parameters_arr) ) {
-        Py_INCREF(parameters_arr);
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+
+    if ( PyArray_Check(unitary_arg) && PyArray_IS_C_CONTIGUOUS(unitary_arg) ) {
+        Py_INCREF(unitary_arg);
     }
     else {
-        parameters_arr = PyArray_FROM_OTF(parameters_arr, NPY_DOUBLE, NPY_ARRAY_IN_ARRAY);
+        unitary_arg = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
     }
 
 
-    // get the C++ wrapper around the data
-    Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary_arg);
 
-    Matrix RY_mtx = self->gate->get_matrix( parameters_mtx );
+    self->gate->apply_to( unitary_mtx );
     
-    // convert to numpy array
-    RY_mtx.set_owner(false);
-    PyObject *RY_py = matrix_to_numpy( RY_mtx );
+    Py_DECREF(unitary_arg);
 
+    return Py_BuildValue("i", 0);
+}
 
-    Py_DECREF(parameters_arr);
 
-    return RY_py;
-}
 
 /**
-@brief Structure containing metadata about the members of class qgd_RY.
+@brief Structure containing metadata about the members of class  qgd_SYC.
 */
-static PyMemberDef qgd_RY_members[] = {
+static PyMemberDef  qgd_SYC_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_RY.
+@brief Structure containing metadata about the methods of class  qgd_SYC.
 */
-static PyMethodDef qgd_RY_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_RY_get_Matrix, METH_VARARGS,
+static PyMethodDef  qgd_SYC_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_SYC_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_SYC_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_RY.
+@brief A structure describing the type of the class  qgd_SYC.
 */
-static PyTypeObject  qgd_RY_Type = {
+static PyTypeObject  qgd_SYC_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_RY.qgd_RY", /*tp_name*/
-  sizeof(qgd_RY), /*tp_basicsize*/
+  "qgd_SYC.qgd_SYC", /*tp_name*/
+  sizeof(qgd_SYC), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_RY_dealloc, /*tp_dealloc*/
+  (destructor)  qgd_SYC_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -217,32 +242,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a RY gate of the QGD package.", /*tp_doc*/
+  "Object to represent a SYC gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_RY_methods, /*tp_methods*/
-  qgd_RY_members, /*tp_members*/
+   qgd_SYC_methods, /*tp_methods*/
+   qgd_SYC_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_RY_init, /*tp_init*/
+  (initproc)  qgd_SYC_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_RY_new, /*tp_new*/
+   qgd_SYC_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -259,43 +284,45 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_RY_Module = {
+static PyModuleDef  qgd_SYC_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_RY",
-    .m_doc = "Python binding for QGD RY gate",
+    .m_name = "qgd_SYC",
+    .m_doc = "Python binding for QGD SYC gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_RY(void)
+PyInit_qgd_SYC(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_RY_Type) < 0)
+    if (PyType_Ready(& qgd_SYC_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_RY_Module);
+    m = PyModule_Create(& qgd_SYC_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_RY_Type);
-    if (PyModule_AddObject(m, "qgd_RY", (PyObject *) & qgd_RY_Type) < 0) {
-        Py_DECREF(& qgd_RY_Type);
+    Py_INCREF(& qgd_SYC_Type);
+    if (PyModule_AddObject(m, "qgd_SYC", (PyObject *) & qgd_SYC_Type) < 0) {
+        Py_DECREF(& qgd_SYC_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
 
 
 
-
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_RZ.cpp` & `squander-1.8.0/qgd_python/gates/qgd_Y.cpp`

 * *Files 18% similar despite different names*

```diff
@@ -14,131 +14,133 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_RZ.cpp
-\brief Python interface for the RZ gate class
+\file qgd_Y.cpp
+\brief Python interface for the X gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "RZ.h"
+#include "Y.h"
 #include "numpy_interface.h"
 
 
 
 
 /**
-@brief Type definition of the qgd_RZ Python class of the qgd_RZ module
+@brief Type definition of the qgd_Y Python class of the qgd_Y module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the RZ gate
-    RZ* gate;
-} qgd_RZ;
+    /// Pointer to the C++ class of the X gate
+    Y* gate;
+} qgd_Y;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num The number of qubits spanning the operation.
 @param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-RZ* 
-create_RZ( int qbit_num, int target_qbit ) {
+Y* 
+create_Y( int qbit_num, int target_qbit ) {
 
-    return new RZ( qbit_num, target_qbit );
+    return new Y( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_RZ( RZ*  instance ) {
+release_Y( Y*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_RZ is destroyed
-@param self A pointer pointing to an instance of class qgd_RZ.
+@brief Method called when a python instance of the class qgd_Y is destroyed
+@param self A pointer pointing to an instance of class qgd_Y.
 */
 static void
-qgd_RZ_dealloc(qgd_RZ *self)
+qgd_Y_dealloc(qgd_Y *self)
 {
 
-    // release the RZ gate
-    release_RZ( self->gate );
+    // release the X gate
+    release_Y( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RZ is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_RZ.
+@brief Method called when a python instance of the class qgd_Y is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_Y.
 */
 static PyObject *
-qgd_RZ_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_Y_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_RZ *self;
-    self = (qgd_RZ *) type->tp_alloc(type, 0);
+    qgd_Y *self;
+    self = (qgd_Y *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_RZ is initialized
-@param self A pointer pointing to an instance of the class qgd_RZ.
+@brief Method called when a python instance of the class qgd_Y is initialized
+@param self A pointer pointing to an instance of the class qgd_Y.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
-qgd_RZ_init(qgd_RZ *self, PyObject *args, PyObject *kwds)
+qgd_Y_init(qgd_Y *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
                                      &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_RZ( qbit_num, target_qbit );
+        self->gate = create_Y( qbit_num, target_qbit );
     }
     return 0;
 }
 
+
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
+/**
 static PyObject *
-qgd_RZ_get_Matrix( qgd_RZ *self, PyObject *args ) {
+qgd_Y_get_Matrix( qgd_Y *self, PyObject *args ) {
 
     PyObject * parameters_arr = NULL;
 
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &parameters_arr )) 
         return Py_BuildValue("i", -1);
@@ -152,55 +154,117 @@
     }
 
 
     // get the C++ wrapper around the data
     Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
 
-    Matrix RZ_mtx = self->gate->get_matrix( parameters_mtx );
+    Matrix Y_mtx = self->gate->get_matrix(  );
     
     // convert to numpy array
-    RZ_mtx.set_owner(false);
-    PyObject *RZ_py = matrix_to_numpy( RZ_mtx );
+    Y_mtx.set_owner(false);
+    PyObject *Y_py = matrix_to_numpy( Y_mtx );
 
 
     Py_DECREF(parameters_arr);
 
-    return RZ_py;
+    return Y_py;
 }
+*/
 
+/**
+@brief Extract the optimized parameters
+@param start_index The index of the first inverse gate
+*/
+static PyObject *
+qgd_Y_get_Matrix( qgd_Y *self ) {
+
+   
+    Matrix Y_mtx = self->gate->get_matrix(  );
+    
+    // convert to numpy array
+    Y_mtx.set_owner(false);
+    PyObject *Y_py = matrix_to_numpy( Y_mtx );
+
+
+    return Y_py;
+}
 
 /**
-@brief Structure containing metadata about the members of class qgd_RZ.
+@brief Call to apply the gate operation on the inut matrix
 */
-static PyMemberDef qgd_RZ_members[] = {
+static PyObject *
+qgd_Y_apply_to( qgd_Y *self, PyObject *args ) {
+
+    PyObject * unitary_arg = NULL;
+
+
+    // parsing input arguments
+    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+        return Py_BuildValue("i", -1);
+
+
+    // convert python object array to numpy C API array
+    if ( unitary_arg == NULL ) {
+        PyErr_SetString(PyExc_Exception, "Input matrix was not given");
+        return NULL;
+    }
+
+    PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
+
+
+    // create QGD version of the input matrix
+    Matrix unitary_mtx = numpy2matrix(unitary);
+
+    self->gate->apply_to( unitary_mtx );
+    
+    Py_DECREF(unitary);
+
+    return Py_BuildValue("i", 0);
+}
+
+
+
+/**
+@brief Structure containing metadata about the members of class qgd_Y.
+*/
+static PyMemberDef qgd_Y_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_RZ.
+@brief Structure containing metadata about the methods of class qgd_Y.
 */
-static PyMethodDef qgd_RZ_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_RZ_get_Matrix, METH_VARARGS,
+static PyMethodDef qgd_Y_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_Y_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
     },
+    {"apply_to", (PyCFunction) qgd_Y_apply_to, METH_VARARGS,
+     "Call to apply the gate on the input matrix."
+    },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_RZ.
+@brief A structure describing the type of the class qgd_Y.
 */
-static PyTypeObject  qgd_RZ_Type = {
+static PyTypeObject  qgd_Y_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_RZ.qgd_RZ", /*tp_name*/
-  sizeof(qgd_RZ), /*tp_basicsize*/
+  "qgd_Y.qgd_Y", /*tp_name*/
+  sizeof(qgd_Y), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_RZ_dealloc, /*tp_dealloc*/
+  (destructor) qgd_Y_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -218,32 +282,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a RZ gate of the QGD package.", /*tp_doc*/
+  "Object to represent a X gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_RZ_methods, /*tp_methods*/
-  qgd_RZ_members, /*tp_members*/
+  qgd_Y_methods, /*tp_methods*/
+  qgd_Y_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_RZ_init, /*tp_init*/
+  (initproc) qgd_Y_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_RZ_new, /*tp_new*/
+  qgd_Y_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -260,39 +324,42 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_RZ_Module = {
+static PyModuleDef  qgd_Y_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_RZ",
-    .m_doc = "Python binding for QGD RZ gate",
+    .m_name = "qgd_Y",
+    .m_doc = "Python binding for QGD X gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_RZ(void)
+PyInit_qgd_Y(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_RZ_Type) < 0)
+    if (PyType_Ready(& qgd_Y_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_RZ_Module);
+    m = PyModule_Create(& qgd_Y_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_RZ_Type);
-    if (PyModule_AddObject(m, "qgd_RZ", (PyObject *) & qgd_RZ_Type) < 0) {
-        Py_DECREF(& qgd_RZ_Type);
+    Py_INCREF(& qgd_Y_Type);
+    if (PyModule_AddObject(m, "qgd_Y", (PyObject *) & qgd_Y_Type) < 0) {
+        Py_DECREF(& qgd_Y_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_U3.cpp` & `squander-1.8.0/qgd_python/gates/qgd_U3.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -344,14 +344,17 @@
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
 PyInit_qgd_U3(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
     if (PyType_Ready(& qgd_U3_Type) < 0)
         return NULL;
 
     m = PyModule_Create(& qgd_U3_Module);
     if (m == NULL)
         return NULL;
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_X.cpp` & `squander-1.8.0/qgd_python/gates/qgd_SX.cpp`

 * *Files 16% similar despite different names*

```diff
@@ -14,223 +14,225 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_X.cpp
-\brief Python interface for the X gate class
+\file qgd_SX.cpp
+\brief Python interface for the SX gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "X.h"
+#include "SX.h"
 #include "numpy_interface.h"
 
 
 
 
 /**
-@brief Type definition of the qgd_X Python class of the qgd_X module
+@brief Type definition of the qgd_SX Python class of the qgd_SX module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the X gate
-    X* gate;
-} qgd_X;
+    /// Pointer to the C++ class of the SX gate
+    SX* gate;
+} qgd_SX;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num The number of qubits spanning the operation.
 @param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-X* 
-create_X( int qbit_num, int target_qbit ) {
+SX* 
+create_SX( int qbit_num, int target_qbit ) {
 
-    return new X( qbit_num, target_qbit );
+    return new SX( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_X( X*  instance ) {
+release_SX( SX*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_X is destroyed
-@param self A pointer pointing to an instance of class qgd_X.
+@brief Method called when a python instance of the class qgd_SX is destroyed
+@param self A pointer pointing to an instance of class qgd_SX.
 */
 static void
-qgd_X_dealloc(qgd_X *self)
+qgd_SX_dealloc(qgd_SX *self)
 {
 
-    // release the X gate
-    release_X( self->gate );
+    // release the SX gate
+    release_SX( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_X is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_X.
+@brief Method called when a python instance of the class qgd_SX is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_SX.
 */
 static PyObject *
-qgd_X_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_SX_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_X *self;
-    self = (qgd_X *) type->tp_alloc(type, 0);
+    qgd_SX *self;
+    self = (qgd_SX *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_X is initialized
-@param self A pointer pointing to an instance of the class qgd_X.
+@brief Method called when a python instance of the class qgd_SX is initialized
+@param self A pointer pointing to an instance of the class qgd_SX.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
-qgd_X_init(qgd_X *self, PyObject *args, PyObject *kwds)
+qgd_SX_init(qgd_SX *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
                                      &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_X( qbit_num, target_qbit );
+        self->gate = create_SX( qbit_num, target_qbit );
     }
-
-
-
-
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
+
 static PyObject *
-qgd_X_get_Matrix( qgd_X *self ) {
+qgd_SX_get_Matrix( qgd_SX *self ) {
 
-   
-    Matrix X_mtx = self->gate->get_matrix(  );
+    Matrix SX_mtx = self->gate->get_matrix(  );
     
     // convert to numpy array
-    X_mtx.set_owner(false);
-    PyObject *X_py = matrix_to_numpy( X_mtx );
-
+    SX_mtx.set_owner(false);
+    PyObject *SX_py = matrix_to_numpy( SX_mtx );
 
-    return X_py;
+    return SX_py;
 }
 
 
 
 /**
 @brief Call to apply the gate operation on the inut matrix
 */
 static PyObject *
-qgd_X_apply_to( qgd_X *self, PyObject *args ) {
+qgd_SX_apply_to( qgd_SX *self, PyObject *args ) {
 
     PyObject * unitary_arg = NULL;
 
 
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
         return Py_BuildValue("i", -1);
 
-
     // convert python object array to numpy C API array
     if ( unitary_arg == NULL ) {
         PyErr_SetString(PyExc_Exception, "Input matrix was not given");
         return NULL;
     }
 
 
     if ( PyArray_Check(unitary_arg) && PyArray_IS_C_CONTIGUOUS(unitary_arg) ) {
         Py_INCREF(unitary_arg);
     }
     else {
         unitary_arg = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
     }
 
+   PyObject* unitary = PyArray_FROM_OTF(unitary_arg, NPY_COMPLEX128, NPY_ARRAY_IN_ARRAY);
+
+    // test C-style contiguous memory allocation of the array
+    if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
+        PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
+        return NULL;
+    }
 
 
     // create QGD version of the input matrix
-    Matrix unitary_mtx = numpy2matrix(unitary_arg);
+    Matrix unitary_mtx = numpy2matrix(unitary);
 
     self->gate->apply_to( unitary_mtx );
     
-    Py_DECREF(unitary_arg);
+    Py_DECREF(unitary);
 
     return Py_BuildValue("i", 0);
 }
 
 
 
+
 /**
-@brief Structure containing metadata about the members of class qgd_X.
+@brief Structure containing metadata about the members of class qgd_SX.
 */
-static PyMemberDef qgd_X_members[] = {
-    {NULL}  /* Sentinel */
+static PyMemberDef qgd_SX_members[] = {
+   {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_X.
+@brief Structure containing metadata about the methods of class qgd_SX.
 */
-static PyMethodDef qgd_X_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_X_get_Matrix, METH_NOARGS,
+static PyMethodDef qgd_SX_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_SX_get_Matrix, METH_NOARGS,
      "Method to get the matrix of the operation."
-    },
-    {"apply_to", (PyCFunction) qgd_X_apply_to, METH_VARARGS,
+    },   
+    {"apply_to", (PyCFunction) qgd_SX_apply_to, METH_VARARGS,
      "Call to apply the gate on the input matrix."
     },
-    {NULL}  /* Sentinel */
+  {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_X.
+@brief A structure describing the type of the class qgd_SX.
 */
-static PyTypeObject  qgd_X_Type = {
+static PyTypeObject  qgd_SX_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_X.qgd_X", /*tp_name*/
-  sizeof(qgd_X), /*tp_basicsize*/
+  "qgd_SX.qgd_SX", /*tp_name*/
+  sizeof(qgd_SX), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_X_dealloc, /*tp_dealloc*/
+  (destructor) qgd_SX_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -248,32 +250,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a X gate of the QGD package.", /*tp_doc*/
+  "Object to represent a SX gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_X_methods, /*tp_methods*/
-  qgd_X_members, /*tp_members*/
+  qgd_SX_methods, /*tp_methods*/
+  qgd_SX_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_X_init, /*tp_init*/
+  (initproc) qgd_SX_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_X_new, /*tp_new*/
+  qgd_SX_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -290,39 +292,42 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_X_Module = {
+static PyModuleDef  qgd_SX_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_X",
-    .m_doc = "Python binding for QGD X gate",
+    .m_name = "qgd_SX",
+    .m_doc = "Python binding for QGD SX gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_X(void)
+PyInit_qgd_SX(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_X_Type) < 0)
+    if (PyType_Ready(& qgd_SX_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_X_Module);
+    m = PyModule_Create(& qgd_SX_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_X_Type);
-    if (PyModule_AddObject(m, "qgd_X", (PyObject *) & qgd_X_Type) < 0) {
-        Py_DECREF(& qgd_X_Type);
+    Py_INCREF(& qgd_SX_Type);
+    if (PyModule_AddObject(m, "qgd_SX", (PyObject *) & qgd_SX_Type) < 0) {
+        Py_DECREF(& qgd_SX_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_Y.cpp` & `squander-1.8.0/qgd_python/gates/qgd_RY.cpp`

 * *Files 9% similar despite different names*

```diff
@@ -14,131 +14,131 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_Y.cpp
-\brief Python interface for the X gate class
+\file qgd_RY.cpp
+\brief Python interface for the RY gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "Y.h"
+#include "RY.h"
 #include "numpy_interface.h"
 
 
 
 
 /**
-@brief Type definition of the qgd_Y Python class of the qgd_Y module
+@brief Type definition of the qgd_RY Python class of the qgd_RY module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the X gate
-    Y* gate;
-} qgd_Y;
+    /// Pointer to the C++ class of the RY gate
+    RY* gate;
+} qgd_RY;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num The number of qubits spanning the operation.
 @param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-Y* 
-create_Y( int qbit_num, int target_qbit ) {
+RY* 
+create_RY( int qbit_num, int target_qbit ) {
 
-    return new Y( qbit_num, target_qbit );
+    return new RY( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_Y( Y*  instance ) {
+release_RY( RY*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_Y is destroyed
-@param self A pointer pointing to an instance of class qgd_Y.
+@brief Method called when a python instance of the class qgd_RY is destroyed
+@param self A pointer pointing to an instance of class qgd_RY.
 */
 static void
-qgd_Y_dealloc(qgd_Y *self)
+qgd_RY_dealloc(qgd_RY *self)
 {
 
-    // release the X gate
-    release_Y( self->gate );
+    // release the RY gate
+    release_RY( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_Y is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_Y.
+@brief Method called when a python instance of the class qgd_RY is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_RY.
 */
 static PyObject *
-qgd_Y_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_RY_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_Y *self;
-    self = (qgd_Y *) type->tp_alloc(type, 0);
+    qgd_RY *self;
+    self = (qgd_RY *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_Y is initialized
-@param self A pointer pointing to an instance of the class qgd_Y.
+@brief Method called when a python instance of the class qgd_RY is initialized
+@param self A pointer pointing to an instance of the class qgd_RY.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
-qgd_Y_init(qgd_Y *self, PyObject *args, PyObject *kwds)
+qgd_RY_init(qgd_RY *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
                                      &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_Y( qbit_num, target_qbit );
+        self->gate = create_RY( qbit_num, target_qbit );
     }
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
 static PyObject *
-qgd_Y_get_Matrix( qgd_Y *self, PyObject *args ) {
+qgd_RY_get_Matrix( qgd_RY *self, PyObject *args ) {
 
     PyObject * parameters_arr = NULL;
 
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &parameters_arr )) 
         return Py_BuildValue("i", -1);
@@ -152,40 +152,52 @@
     }
 
 
     // get the C++ wrapper around the data
     Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
 
-    Matrix X_mtx = self->gate->get_matrix(  );
+    Matrix RY_mtx = self->gate->get_matrix( parameters_mtx );
     
     // convert to numpy array
-    X_mtx.set_owner(false);
-    PyObject *X_py = matrix_to_numpy( X_mtx );
+    RY_mtx.set_owner(false);
+    PyObject *RY_py = matrix_to_numpy( RY_mtx );
 
 
     Py_DECREF(parameters_arr);
 
-    return X_py;
+    return RY_py;
 }
 
 
+
 /**
 @brief Call to apply the gate operation on the inut matrix
 */
 static PyObject *
-qgd_Y_apply_to( qgd_Y *self, PyObject *args ) {
+qgd_RY_apply_to( qgd_RY *self, PyObject *args ) {
 
+    PyObject * parameters_arr = NULL;
     PyObject * unitary_arg = NULL;
 
 
+
     // parsing input arguments
-    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+    if (!PyArg_ParseTuple(args, "|OO", &parameters_arr, &unitary_arg )) 
         return Py_BuildValue("i", -1);
+    
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arr) ) {
+        Py_INCREF(parameters_arr);
+    }
+    else {
+        parameters_arr = PyArray_FROM_OTF(parameters_arr, NPY_DOUBLE, NPY_ARRAY_IN_ARRAY);
+    }
 
+    // get the C++ wrapper around the data
+    Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
     // convert python object array to numpy C API array
     if ( unitary_arg == NULL ) {
         PyErr_SetString(PyExc_Exception, "Input matrix was not given");
         return NULL;
     }
 
@@ -193,58 +205,58 @@
 
     // test C-style contiguous memory allocation of the array
     if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
         PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
         return NULL;
     }
 
-
     // create QGD version of the input matrix
     Matrix unitary_mtx = numpy2matrix(unitary);
 
-    self->gate->apply_to( unitary_mtx );
+    self->gate->apply_to( parameters_mtx, unitary_mtx );
     
+    Py_DECREF(parameters_arr);
     Py_DECREF(unitary);
 
     return Py_BuildValue("i", 0);
 }
 
 
 
 /**
-@brief Structure containing metadata about the members of class qgd_Y.
+@brief Structure containing metadata about the members of class qgd_RY.
 */
-static PyMemberDef qgd_Y_members[] = {
+static PyMemberDef qgd_RY_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_Y.
+@brief Structure containing metadata about the methods of class qgd_RY.
 */
-static PyMethodDef qgd_Y_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_Y_get_Matrix, METH_VARARGS,
+static PyMethodDef qgd_RY_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_RY_get_Matrix, METH_VARARGS,
      "Method to get the matrix of the operation."
     },
-    {"apply_to", (PyCFunction) qgd_Y_apply_to, METH_VARARGS,
+    {"apply_to", (PyCFunction) qgd_RY_apply_to, METH_VARARGS,
      "Call to apply the gate on the input matrix."
     },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_Y.
+@brief A structure describing the type of the class qgd_RY.
 */
-static PyTypeObject  qgd_Y_Type = {
+static PyTypeObject  qgd_RY_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_Y.qgd_Y", /*tp_name*/
-  sizeof(qgd_Y), /*tp_basicsize*/
+  "qgd_RY.qgd_RY", /*tp_name*/
+  sizeof(qgd_RY), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_Y_dealloc, /*tp_dealloc*/
+  (destructor) qgd_RY_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -262,32 +274,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a X gate of the QGD package.", /*tp_doc*/
+  "Object to represent a RY gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_Y_methods, /*tp_methods*/
-  qgd_Y_members, /*tp_members*/
+  qgd_RY_methods, /*tp_methods*/
+  qgd_RY_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_Y_init, /*tp_init*/
+  (initproc) qgd_RY_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_Y_new, /*tp_new*/
+  qgd_RY_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -304,39 +316,42 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_Y_Module = {
+static PyModuleDef  qgd_RY_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_Y",
-    .m_doc = "Python binding for QGD X gate",
+    .m_name = "qgd_RY",
+    .m_doc = "Python binding for QGD RY gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_Y(void)
+PyInit_qgd_RY(void)
 {
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_Y_Type) < 0)
+    if (PyType_Ready(& qgd_RY_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_Y_Module);
+    m = PyModule_Create(& qgd_RY_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_Y_Type);
-    if (PyModule_AddObject(m, "qgd_Y", (PyObject *) & qgd_Y_Type) < 0) {
-        Py_DECREF(& qgd_Y_Type);
+    Py_INCREF(& qgd_RY_Type);
+    if (PyModule_AddObject(m, "qgd_RY", (PyObject *) & qgd_RY_Type) < 0) {
+        Py_DECREF(& qgd_RY_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/qgd_Z.cpp` & `squander-1.8.0/qgd_python/gates/qgd_RX.cpp`

 * *Files 11% similar despite different names*

```diff
@@ -14,131 +14,131 @@
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see http://www.gnu.org/licenses/.
 
 @author: Peter Rakyta, Ph.D.
 */
 /*
-\file qgd_Z.cpp
-\brief Python interface for the Z gate class
+\file qgd_RX.cpp
+\brief Python interface for the RX gate class
 */
 
 #define PY_SSIZE_T_CLEAN
 
 
 #include <Python.h>
 #include "structmember.h"
-#include "Z.h"
+#include "RX.h"
 #include "numpy_interface.h"
 
 
 
 
 /**
-@brief Type definition of the qgd_Z Python class of the qgd_Z module
+@brief Type definition of the qgd_RX Python class of the qgd_RX module
 */
 typedef struct {
     PyObject_HEAD
-    /// Pointer to the C++ class of the X gate
-    Z* gate;
-} qgd_Z;
+    /// Pointer to the C++ class of the RX gate
+    RX* gate;
+} qgd_RX;
 
 
 /**
 @brief Creates an instance of class N_Qubit_Decomposition and return with a pointer pointing to the class instance (C++ linking is needed)
 @param qbit_num The number of qubits spanning the operation.
 @param target_qbit The 0<=ID<qbit_num of the target qubit.
 */
-Z* 
-create_Z( int qbit_num, int target_qbit ) {
+RX* 
+create_RX( int qbit_num, int target_qbit ) {
 
-    return new Z( qbit_num, target_qbit );
+    return new RX( qbit_num, target_qbit );
 }
 
 
 /**
 @brief Call to deallocate an instance of N_Qubit_Decomposition class
 @param ptr A pointer pointing to an instance of N_Qubit_Decomposition class.
 */
 void
-release_Z( Z*  instance ) {
+release_RX( RX*  instance ) {
     delete instance;
     return;
 }
 
 
 
 
 
 extern "C"
 {
 
 
 /**
-@brief Method called when a python instance of the class qgd_Z is destroyed
-@param self A pointer pointing to an instance of class qgd_Z.
+@brief Method called when a python instance of the class qgd_RX is destroyed
+@param self A pointer pointing to an instance of class qgd_RX.
 */
 static void
-qgd_Z_dealloc(qgd_Z *self)
+qgd_RX_dealloc(qgd_RX *self)
 {
 
-    // release the X gate
-    release_Z( self->gate );
+    // release the RX gate
+    release_RX( self->gate );
 
     Py_TYPE(self)->tp_free((PyObject *) self);
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_Z is allocated
-@param type A pointer pointing to a structure describing the type of the class qgd_Z.
+@brief Method called when a python instance of the class qgd_RX is allocated
+@param type A pointer pointing to a structure describing the type of the class qgd_RX.
 */
 static PyObject *
-qgd_Z_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
+qgd_RX_new(PyTypeObject *type, PyObject *args, PyObject *kwds)
 {
-    qgd_Z *self;
-    self = (qgd_Z *) type->tp_alloc(type, 0);
+    qgd_RX *self;
+    self = (qgd_RX *) type->tp_alloc(type, 0);
     if (self != NULL) {}
     return (PyObject *) self;
 }
 
 
 /**
-@brief Method called when a python instance of the class qgd_Z is initialized
-@param self A pointer pointing to an instance of the class qgd_Z.
+@brief Method called when a python instance of the class qgd_RX is initialized
+@param self A pointer pointing to an instance of the class qgd_RX.
 @param args A tuple of the input arguments: qbit_num (int), target_qbit (int), Theta (bool) , Phi (bool), Lambda (bool)
 @param kwds A tuple of keywords
 */
 static int
-qgd_Z_init(qgd_Z *self, PyObject *args, PyObject *kwds)
+qgd_RX_init(qgd_RX *self, PyObject *args, PyObject *kwds)
 {
     static char *kwlist[] = {(char*)"qbit_num", (char*)"target_qbit", NULL};
     int  qbit_num = -1; 
     int target_qbit = -1;
 
     if (PyArray_API == NULL) {
         import_array();
     }
 
     if (!PyArg_ParseTupleAndKeywords(args, kwds, "|ii", kwlist,
                                      &qbit_num, &target_qbit))
         return -1;
 
     if (qbit_num != -1 && target_qbit != -1) {
-        self->gate = create_Z( qbit_num, target_qbit );
+        self->gate = create_RX( qbit_num, target_qbit );
     }
     return 0;
 }
 
 /**
 @brief Extract the optimized parameters
 @param start_index The index of the first inverse gate
 */
 static PyObject *
-qgd_Z_get_Matrix( qgd_Z *self, PyObject *args ) {
+qgd_RX_get_Matrix( qgd_RX *self, PyObject *args ) {
 
     PyObject * parameters_arr = NULL;
 
 
     // parsing input arguments
     if (!PyArg_ParseTuple(args, "|O", &parameters_arr )) 
         return Py_BuildValue("i", -1);
@@ -152,41 +152,52 @@
     }
 
 
     // get the C++ wrapper around the data
     Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
 
-    Matrix Z_mtx = self->gate->get_matrix(  );
+    Matrix RX_mtx = self->gate->get_matrix( parameters_mtx );
     
     // convert to numpy array
-    Z_mtx.set_owner(false);
-    PyObject *Z_py = matrix_to_numpy( Z_mtx );
+    RX_mtx.set_owner(false);
+    PyObject *RX_py = matrix_to_numpy( RX_mtx );
 
 
     Py_DECREF(parameters_arr);
 
-    return Z_py;
+    return RX_py;
 }
 
 
 
 /**
 @brief Call to apply the gate operation on the inut matrix
 */
 static PyObject *
-qgd_Z_apply_to( qgd_Z *self, PyObject *args ) {
+qgd_RX_apply_to( qgd_RX *self, PyObject *args ) {
 
+    PyObject * parameters_arr = NULL;
     PyObject * unitary_arg = NULL;
 
 
+
     // parsing input arguments
-    if (!PyArg_ParseTuple(args, "|O", &unitary_arg )) 
+    if (!PyArg_ParseTuple(args, "|OO", &parameters_arr, &unitary_arg )) 
         return Py_BuildValue("i", -1);
+    
+    if ( PyArray_IS_C_CONTIGUOUS(parameters_arr) ) {
+        Py_INCREF(parameters_arr);
+    }
+    else {
+        parameters_arr = PyArray_FROM_OTF(parameters_arr, NPY_DOUBLE, NPY_ARRAY_IN_ARRAY);
+    }
 
+    // get the C++ wrapper around the data
+    Matrix_real&& parameters_mtx = numpy2matrix_real( parameters_arr );
 
     // convert python object array to numpy C API array
     if ( unitary_arg == NULL ) {
         PyErr_SetString(PyExc_Exception, "Input matrix was not given");
         return NULL;
     }
 
@@ -194,58 +205,58 @@
 
     // test C-style contiguous memory allocation of the array
     if ( !PyArray_IS_C_CONTIGUOUS(unitary) ) {
         PyErr_SetString(PyExc_Exception, "input mtrix is not memory contiguous");
         return NULL;
     }
 
-
     // create QGD version of the input matrix
     Matrix unitary_mtx = numpy2matrix(unitary);
 
-    self->gate->apply_to( unitary_mtx );
+    self->gate->apply_to( parameters_mtx, unitary_mtx );
     
+    Py_DECREF(parameters_arr);
     Py_DECREF(unitary);
 
     return Py_BuildValue("i", 0);
 }
 
 
 
 /**
-@brief Structure containing metadata about the members of class qgd_Z.
+@brief Structure containing metadata about the members of class qgd_RX.
 */
-static PyMemberDef qgd_Z_members[] = {
+static PyMemberDef qgd_RX_members[] = {
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief Structure containing metadata about the methods of class qgd_Z.
+@brief Structure containing metadata about the methods of class qgd_RX.
 */
-static PyMethodDef qgd_Z_methods[] = {
-    {"get_Matrix", (PyCFunction) qgd_Z_get_Matrix, METH_VARARGS,
+static PyMethodDef qgd_RX_methods[] = {
+    {"get_Matrix", (PyCFunction) qgd_RX_get_Matrix, METH_VARARGS,
      "Method to get the matrix of the operation."
     },
-    {"apply_to", (PyCFunction) qgd_Z_apply_to, METH_VARARGS,
+    {"apply_to", (PyCFunction) qgd_RX_apply_to, METH_VARARGS,
      "Call to apply the gate on the input matrix."
     },
     {NULL}  /* Sentinel */
 };
 
 
 /**
-@brief A structure describing the type of the class qgd_Z.
+@brief A structure describing the type of the class qgd_RX.
 */
-static PyTypeObject  qgd_Z_Type = {
+static PyTypeObject  qgd_RX_Type = {
   PyVarObject_HEAD_INIT(NULL, 0)
-  "qgd_Z.qgd_Z", /*tp_name*/
-  sizeof(qgd_Z), /*tp_basicsize*/
+  "qgd_RX.qgd_RX", /*tp_name*/
+  sizeof(qgd_RX), /*tp_basicsize*/
   0, /*tp_itemsize*/
-  (destructor) qgd_Z_dealloc, /*tp_dealloc*/
+  (destructor) qgd_RX_dealloc, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
   0, /*tp_vectorcall_offset*/
   #endif
   0, /*tp_getattr*/
@@ -263,32 +274,32 @@
   0, /*tp_hash*/
   0, /*tp_call*/
   0, /*tp_str*/
   0, /*tp_getattro*/
   0, /*tp_setattro*/
   0, /*tp_as_buffer*/
   Py_TPFLAGS_DEFAULT | Py_TPFLAGS_BASETYPE, /*tp_flags*/
-  "Object to represent a X gate of the QGD package.", /*tp_doc*/
+  "Object to represent a RX gate of the QGD package.", /*tp_doc*/
   0, /*tp_traverse*/
   0, /*tp_clear*/
   0, /*tp_richcompare*/
   0, /*tp_weaklistoffset*/
   0, /*tp_iter*/
   0, /*tp_iternext*/
-  qgd_Z_methods, /*tp_methods*/
-  qgd_Z_members, /*tp_members*/
+  qgd_RX_methods, /*tp_methods*/
+  qgd_RX_members, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
   0, /*tp_dictoffset*/
-  (initproc) qgd_Z_init, /*tp_init*/
+  (initproc) qgd_RX_init, /*tp_init*/
   0, /*tp_alloc*/
-  qgd_Z_new, /*tp_new*/
+  qgd_RX_new, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
@@ -305,39 +316,43 @@
   #endif
 };
 
 
 /**
 @brief Structure containing metadata about the module.
 */
-static PyModuleDef  qgd_Z_Module = {
+static PyModuleDef  qgd_RX_Module = {
     PyModuleDef_HEAD_INIT,
-    .m_name = "qgd_Z",
-    .m_doc = "Python binding for QGD X gate",
+    .m_name = "qgd_RX",
+    .m_doc = "Python binding for QGD RX gate",
     .m_size = -1,
 };
 
 
 /**
 @brief Method called when the Python module is initialized
 */
 PyMODINIT_FUNC
-PyInit_qgd_Z(void)
+PyInit_qgd_RX(void)
 {
+
+    // initialize Numpy API
+    import_array();
+
     PyObject *m;
-    if (PyType_Ready(& qgd_Z_Type) < 0)
+    if (PyType_Ready(& qgd_RX_Type) < 0)
         return NULL;
 
-    m = PyModule_Create(& qgd_Z_Module);
+    m = PyModule_Create(& qgd_RX_Module);
     if (m == NULL)
         return NULL;
 
-    Py_INCREF(& qgd_Z_Type);
-    if (PyModule_AddObject(m, "qgd_Z", (PyObject *) & qgd_Z_Type) < 0) {
-        Py_DECREF(& qgd_Z_Type);
+    Py_INCREF(& qgd_RX_Type);
+    if (PyModule_AddObject(m, "qgd_RX", (PyObject *) & qgd_RX_Type) < 0) {
+        Py_DECREF(& qgd_RX_Type);
         Py_DECREF(m);
         return NULL;
     }
 
     return m;
 }
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_CH.py` & `squander-1.8.0/qgd_python/gates/test/test_Y.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,68 +1,108 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
+from qgd_python.gates.qgd_Y import qgd_Y
+from scipy.stats import unitary_group
 
-pi=np.pi
-
-#SQUANDER
 
 class Test_operations_squander:
-    """This is a test class of the python iterface to the gates of the QGD package"""
+    """This is a test class of the python iterface to compare the SQUANDER and the qiskit decomposition"""
 
 
 
-    def test_CH_squander(self):
+    def test_Y_get_matrix(self):          
         r"""
         This method is called by pytest. 
-        Test to create an instance of RX gate.
+        Test to create an instance of X gate and compare with qiskit.
         """
 
-        from qgd_python.gates.qgd_CH import qgd_CH
+        pi=np.pi
 
-        # number of qubits
-        qbit_num = 3
+        for qbit_num in range(1,7):
 
-        # target qbit
-        target_qbit = 0
+	    #SQUANDER#
 
-        # control_qbit
-        control_qbit = 1
+            target_qbit=qbit_num-1
 
-        # creating an instance of the C++ class
-        CH = qgd_CH( qbit_num, target_qbit, control_qbit )
+            Y = qgd_Y( qbit_num, target_qbit )
 
-        CH_squander = CH.get_Matrix(  )
-        
-        #print(CH_squander)
+            # get the matrix                
+            Y_squander = Y.get_Matrix( )
 
-#QISKIT
+	    #QISKIT
 
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
 
-        # Add the CH gate 
-        circuit.ch(control_qbit, target_qbit)
-        
-        # the unitary matrix from the result object
-        CH_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        CH_qiskit = np.asarray(CH_qiskit)
-        
-        # Draw the circuit        
-        #print(CH_qiskit)
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.y( target_qbit )
+
+            # the unitary matrix from the result object
+            Y_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            Y_qiskit = np.asarray(Y_qiskit)          
         
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=CH_squander-CH_qiskit
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=Y_squander-Y_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
+           
+
+    def test_Y_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of X gate and compare with qiskit.
+        """
+
+        pi=np.pi
+
+        for qbit_num in range(1,7):
+
+            # target qbit  
+            target_qbit=qbit_num-1
+
+            # creating an instance of the C++ class
+            Y = qgd_Y( qbit_num, target_qbit )
+   
+            #create text matrix for apply_to 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
+
+	    #QISKIT
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.y( target_qbit )
+
+            # the unitary matrix from the result object
+            Y_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            Y_qiskit = np.asarray(Y_qiskit)  
+   
+            # apply the gate on the input array/matrix  
+            #Y_qiskit_apply_gate=np.matmul(Y_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            Y_squander = test_matrix
+
+            # apply the gate on the input array/matrix                
+            Y.apply_to(Y_squander)          
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=Y_squander-Y_qiskit
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 )
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_CZ.py` & `squander-1.8.0/qgd_python/gates/test/test_X.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,65 +1,112 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
-
-pi=np.pi
-
+from qgd_python.gates.qgd_X import qgd_X
+from scipy.stats import unitary_group
 
 class Test_operations_squander:
     """This is a test class of the python iterface to compare the SQUANDER and the qiskit decomposition"""
-#SQUANDER#
 
-    def test_CZ_squander(self):
+
+
+    def test_X_get_matrix(self):          
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of X gate and compare with qiskit.
+        """
+
+        pi=np.pi
+
+        for qbit_num in range(1,7):
+
+	    #SQUANDER#
+
+            target_qbit=qbit_num-1
+
+            X = qgd_X( qbit_num, target_qbit )
+
+            # get the matrix                
+            X_squander = X.get_Matrix( ) 
+
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.x( target_qbit )
+
+            # the unitary matrix from the result object
+            X_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            X_qiskit = np.asarray(X_qiskit)          
+
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=X_squander-X_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
+           
+
+    def test_X_apply_to(self):
         r"""
         This method is called by pytest. 
-        Test to create an instance of U3 gate and compare with qiskit.
+        Test to create an instance of X gate and compare with qiskit.
         """
 
-        from qgd_python.gates.qgd_CZ import qgd_CZ
+        pi=np.pi
+
+        for qbit_num in range(1,7):
+
+
+
+            # target qbit  
+            target_qbit=qbit_num-1
+
+            # creating an instance of the C++ class
+            X = qgd_X( qbit_num, target_qbit )
+   
+            #create text matrix for apply_to 
+            test_matrix= np.identity( pow(2,qbit_num), dtype=complex )
+
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.x( target_qbit )
+
+            # the unitary matrix from the result object
+            X_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            X_qiskit = np.asarray(X_qiskit)
+   
+            # apply the gate on the input array/matrix  
+            #X_qiskit_apply_gate=np.matmul(X_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            X_squander = test_matrix
 
-        # number of qubits
-        qbit_num = 3
+            # apply the gate on the input array/matrix                
+            X.apply_to(X_squander)     
 
-        # target qbit
-        target_qbit = 0
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=X_squander-X_qiskit
 
-        # control qbit
-        control_qbit = 1
-     
-        # creating an instance of the C++ class
-        CZ = qgd_CZ( qbit_num, target_qbit, control_qbit )
-                
-        CZ_squander = CZ.get_Matrix( )
-        
-        #print(CZ_squander)
-
-#QISKIT
-
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
-
-        # Add the CNOT gate on control qbit and target qbit
-        circuit.cz( control_qbit, target_qbit )
-        
-        # the unitary matrix from the result object
-        CZ_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        CZ_qiskit = np.asarray(CZ_qiskit)
-        
-        # Draw the circuit        
-        #print(CZ_qiskit)
-        
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=CZ_squander-CZ_qiskit
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 ) 
+
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_RX.py` & `squander-1.8.0/qgd_python/gates/test/test_RY.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,65 +1,118 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
+from qgd_python.gates.qgd_RY import qgd_RY
+import math
+from scipy.stats import unitary_group
 
-pi=np.pi
-
-#SQUANDER
 class Test_operations_squander:
     """This is a test class of the python iterface to the gates of the QGD package"""
 
 
 
-    def test_RX_squander(self):
+    def test_RY_get_matrix(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of RX gate.
         """
 
-        from qgd_python.gates.qgd_RX import qgd_RX
+        pi=np.pi
 
-        # number of qubits
-        qbit_num = 3
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
 
-        # target qbit
-        target_qbit = 0
+        for qbit_num in range(1,7):
 
-        # creating an instance of the C++ class
-        RX = qgd_RX( qbit_num, target_qbit )
+            # target qbit
+            target_qbit = qbit_num-1
 
-        parameters = np.array( [pi/2*0.32] )
-        
-        RX_squander = RX.get_Matrix( parameters )
-        
-        #print(RX_squander)
-
-#QISKIT
-
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
-
-        # Add the u3 gate on qubit pi, pi,
-        circuit.rx(parameters[0]*2, target_qbit)
-
-        # the unitary matrix from the result object
-        RX_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        RX_qiskit = np.asarray(RX_qiskit)
-        
-        # Draw the circuit        
-        #print(RX_qiskit)
-        
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=RX_squander-RX_qiskit
+            # creating an instance of the C++ class
+            RY = qgd_RY( qbit_num, target_qbit )
+
+	    #SQUANDER
+
+            # get the matrix              
+            RY_squander = RY.get_Matrix( parameters )
+
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the ry gate on qubit pi, pi,
+            circuit.ry(parameters[0]*2, target_qbit)
+
+            # the unitary matrix from the result object
+            RY_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RY_qiskit = np.asarray(RY_qiskit)
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=RY_squander-RY_qiskit
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 )        
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )        
  
+    def test_RY_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
+
+
+        pi=np.pi
+
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            RY = qgd_RY( qbit_num, target_qbit )
+
+            #create text matrix 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
+
+	    #QISKIT      
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the ry gate on qubit pi, pi,
+            circuit.ry(parameters[0]*2, target_qbit)
+
+            # the unitary matrix from the result object
+            RY_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RY_qiskit = np.asarray(RY_qiskit)
+
+            # apply the gate on the input array/matrix 
+            #RY_qiskit_apply_gate=np.matmul(RY_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            RY_squander=test_matrix
+
+            # apply the gate on the input array/matrix                
+            RY.apply_to(parameters, RY_squander )
+
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=RY_squander-RY_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
+
+
+
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_RY.py` & `squander-1.8.0/qgd_python/gates/test/test_RX.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,65 +1,119 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
+from qgd_python.gates.qgd_RX import qgd_RX
+import math
+from scipy.stats import unitary_group
 
-pi=np.pi
-
-#SQUANDER
 class Test_operations_squander:
     """This is a test class of the python iterface to the gates of the QGD package"""
 
 
 
-    def test_RY_squander(self):
+    def test_RX_get_matrix(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of RX gate.
         """
 
-        from qgd_python.gates.qgd_RY import qgd_RY
+        pi=np.pi
 
-        # number of qubits
-        qbit_num = 3
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
 
-        # target qbit
-        target_qbit = 0
+        for qbit_num in range(1,7):
 
-        # creating an instance of the C++ class
-        RY = qgd_RY( qbit_num, target_qbit )
+            # target qbit
+            target_qbit = qbit_num-1
 
-        parameters = np.array( [pi/2*0.32] )
-        
-        RY_squander= RY.get_Matrix( parameters )
-        
-        #print(RY_squander)
+            # creating an instance of the C++ class
+            RX = qgd_RX( qbit_num, target_qbit )
 
+	    #SQUANDER
 
-#QISKIT
+            # get the matrix              
+            RX_squander = RX.get_Matrix( parameters )
 
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
+	    #QISKIT
 
-        # Add the u3 gate on qubit pi, pi,
-        circuit.ry(parameters[0]*2, target_qbit)
-        
-        # the unitary matrix from the result object
-        RY_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        RY_qiskit = np.asarray(RY_qiskit)
-        
-        # Draw the circuit        
-        #print(RY_qiskit)
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.rx(parameters[0]*2, target_qbit)
+
+            # the unitary matrix from the result object
+            RX_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RX_qiskit = np.asarray(RX_qiskit)
         
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=RY_squander-RY_qiskit
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=RX_squander-RX_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )        
+ 
+    def test_RX_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
+
+        pi=np.pi
+
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            RX = qgd_RX( qbit_num, target_qbit )
+
+            #create text matrix 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
+
+	    #QISKIT      
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.rx(parameters[0]*2, target_qbit)
+
+            # the unitary matrix from the result object
+            RX_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RX_qiskit = np.asarray(RX_qiskit)
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # apply the gate on the input array/matrix 
+            #RX_qiskit_apply_gate=np.matmul(RX_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            RX_squander=test_matrix
+
+            # apply the gate on the input array/matrix                
+            RX.apply_to(parameters, RX_squander )
+
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=RX_squander-RX_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 )
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_RZ.py` & `squander-1.8.0/qgd_python/gates/test/test_RZ.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,69 +1,123 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
+from qgd_python.gates.qgd_RZ import qgd_RZ
+import math
+from scipy.stats import unitary_group
 
-
-    
- 
-
-
-pi=np.pi
-
-#SQUANDER
 class Test_operations_squander:
     """This is a test class of the python iterface to the gates of the QGD package"""
 
 
 
-    def test_RZ_squander(self):
+    def test_RZ_get_matrix(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of RX gate.
         """
 
-        from qgd_python.gates.qgd_RZ import qgd_RZ
+        pi=np.pi
+
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            RZ = qgd_RZ( qbit_num, target_qbit )
 
-        # number of qubits
-        qbit_num = 1
+	    #SQUANDER
 
-        # target qbit
-        target_qbit = 0
+            # get the matrix              
+            RZ_squander = RZ.get_Matrix( parameters )
 
-        # creating an instance of the C++ class
-        RZ = qgd_RZ( qbit_num, target_qbit )
-
-        parameters = np.array( [pi/2*0.32 ] )
-        
-        RZ_squander= RZ.get_Matrix( parameters )
-        
-#QISKIT
-
-
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
-
-        # Add the u3 gate on qubit pi, pi,
-        circuit.rz(parameters[0], target_qbit)
-        
-        # the unitary matrix from the result object
-        RZ_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        RZ_qiskit = np.asarray(RZ_qiskit)
-        
-
-        # the unitary matrix from the result object
-        product_matrix = np.dot(RZ_squander, RZ_qiskit.conj().T)
-        phase = np.angle(product_matrix[0,0])
-        product_matrix = product_matrix*np.exp(-1j*phase)
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.rz(parameters[0], target_qbit)
+
+            # the unitary matrix from the result object
+            RZ_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RZ_qiskit = np.asarray(RZ_qiskit)
+      
+            # the unitary matrix from the result object
+            product_matrix = np.dot(RZ_squander, RZ_qiskit.conj().T)
+            phase = np.angle(product_matrix[0,0])
+            product_matrix = product_matrix*np.exp(-1j*phase)
     
-        product_matrix = np.eye(2)*2 - product_matrix - product_matrix.conj().T
-        # the error of the decomposition
-        error = (np.real(np.trace(product_matrix)))/2
+            product_matrix = np.eye(2**qbit_num)*(2) - product_matrix - product_matrix.conj().T
+            # the error of the decomposition
+            error = (np.real(np.trace(product_matrix)))/2
        
-        #print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 )
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )
+
+    def test_RZ_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
+        pi=np.pi
+
+        # parameters
+        parameters = np.array( [pi/2*0.32] )
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            RZ = qgd_RZ( qbit_num, target_qbit )
+
+            #create text matrix 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )     
+
+	    #QISKIT      
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.rz(parameters[0], target_qbit)
+
+            # the unitary matrix from the result object
+            RZ_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            RZ_qiskit = np.asarray(RZ_qiskit)
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # apply the gate on the input array/matrix 
+            #RZ_qiskit_apply_gate=np.matmul(RZ_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            RZ_squander=test_matrix
+
+            # apply the gate on the input array/matrix                
+            RZ.apply_to(parameters, RZ_squander )
+
+            # the unitary matrix from the result object
+            product_matrix = np.dot(RZ_squander, RZ_qiskit.conj().T)
+            phase = np.angle(product_matrix[0,0])
+            product_matrix = product_matrix*np.exp(-1j*phase)
+    
+            product_matrix = np.eye(2**qbit_num)*2 - product_matrix - product_matrix.conj().T
+            # the error of the decomposition
+            error = (np.real(np.trace(product_matrix)))/2
+
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
+
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_SX.py` & `squander-1.8.0/qgd_python/gates/test/test_SX.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,65 +1,112 @@
 import numpy as np
 import random
+import math
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
-
-pi=np.pi
-
+from qgd_python.gates.qgd_SX import qgd_SX
+from scipy.stats import unitary_group
+      
 
 class Test_operations_squander:
     """This is a test class of the python iterface to compare the SQUANDER and the qiskit decomposition"""
-#SQUANDER#
 
-    def test_SX_squander(self):
+
+
+
+    def test_SX_get_matrix(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of U3 gate and compare with qiskit.
         """
 
-        from qgd_python.gates.qgd_SX import qgd_SX
+        pi=np.pi
+
+        for qbit_num in range(1,7):
 
-        # number of qubits
-        qbit_num = 3
+            # target qbit
+            target_qbit = qbit_num-1
 
-        # target qbit
-        target_qbit = 0
+            # creating an instance of the C++ class
+            SX = qgd_SX( qbit_num, target_qbit )
 
-        # creating an instance of the C++ class
-        SX = qgd_SX( qbit_num, target_qbit )
-                
-        SX_squander = SX.get_Matrix( )
+	    #SQUANDER#
 
-	#print(SX_squander)
+            # get the matrix                       
+            SX_squander = SX.get_Matrix( )
+      
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.sx( target_qbit )
+
+            # the unitary matrix from the result object
+            SX_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            SX_qiskit = np.asarray(SX_qiskit)
         
- 
-#QISKIT
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=SX_squander-SX_qiskit
 
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
-        # Add the CNOT gate on control qbit and target qbit
-        circuit.sx( target_qbit )
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
 
-        # the unitary matrix from the result object
-        SX_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        SX_qiskit = np.asarray(SX_qiskit)
 
-        # Draw the circuit        
-        #print(SX_qiskit)
+    def test_SX_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
+
+        pi=np.pi
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            SX = qgd_SX( qbit_num, target_qbit )
         
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=SX_squander-SX_qiskit
+            #create text matrix 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
+
+	    #QISKIT      
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.sx( target_qbit )
+
+            # the unitary matrix from the result object
+            SX_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            SX_qiskit = np.asarray(SX_qiskit)
+
+            # apply the gate on the input array/matrix 
+            #SX_qiskit_apply_gate=np.matmul(SX_qiskit, test_matrix)
+
+	    #SQUANDER
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            SX_squander = test_matrix
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 ) 
+            # apply the gate on the input array/matrix                
+            SX.apply_to(SX_squander)       
 
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=SX_squander-SX_qiskit
 
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_U3.py` & `squander-1.8.0/qgd_python/gates/test/test_U3.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,80 +1,128 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
+from qgd_python.gates.qgd_U3 import qgd_U3
+import math
+from scipy.stats import unitary_group
 
-pi=np.pi
-
-#SQUANDER
 class Test_operations_squander:
     """This is a test class of the python iterface to compare the SQUANDER and the qiskit decomposition"""
 
 
 
-    def test_U3_squander(self):
+    def test_U3_get_matrix(self):
         r"""
         This method is called by pytest. 
-        Test to create an instance of U3 gate and compare with qiskit.
+        Test to create an instance of RX gate.
         """
+        pi=np.pi
+
+        # # set the free parameters
+        Theta = True
+        Phi = True
+        Lambda = True
+
+        parameters = np.array( [pi/2*0.32, pi*1.2, pi/2*0.89] )
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            U3 = qgd_U3( qbit_num, target_qbit, Theta, Phi, Lambda )
+
+	    #SQUANDER
+
+            # get the matrix              
+            U3_squander = U3.get_Matrix( parameters )
+
+	    #QISKIT
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.u(parameters[0]*2, parameters[1], parameters[2], target_qbit)
+
+            # the unitary matrix from the result object
+            U3_qiskit= get_unitary_from_qiskit_circuit( circuit )
+            U3_qiskit = np.asarray(U3_qiskit)
+        
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=U3_squander-U3_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
-        from qgd_python.gates.qgd_U3 import qgd_U3
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )        
+ 
+    def test_U3_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
 
-        # number of qubits
-        qbit_num = 2
+        pi=np.pi
 
-        # target qbit
-        target_qbit = 0
 
-        # set the free parameters
+        # # set the free parameters
         Theta = True
         Phi = True
-        Lambda = True        
+        Lambda = True
 
-        # creating an instance of the C++ class
-        U3 = qgd_U3( qbit_num, target_qbit, Theta, Phi, Lambda )
-        
         parameters = np.array( [pi/2*0.32, pi*1.2, pi/2*0.89] )
-        
-        U3_squander = U3.get_Matrix( parameters )
-        
-        #print(U3_squander)
 
-#QISKIT
+        for qbit_num in range(1,7):
 
-        
+            # target qbit
+            target_qbit = qbit_num-1
 
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
+            # creating an instance of the C++ class
+            U3 = qgd_U3( qbit_num, target_qbit, Theta, Phi, Lambda )
 
-        # Add the u3 gate on qubit pi, pi,
-        circuit.u(parameters[0]*2, parameters[1], parameters[2], target_qbit)             
-      
-        # the unitary matrix from the result object
-        U3_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        U3_qiskit = np.asarray(U3_qiskit)
-        
-        # Draw the circuit        
-        #print(U3_qiskit)
-        
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=U3_squander-U3_qiskit
+            #create text matrix 
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+	    #QISKIT      
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 )        
- 
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the RX gate on qubit pi, pi,
+            circuit.u(parameters[0]*2, parameters[1], parameters[2], target_qbit)
+
+            # the unitary matrix from the result object
+            U3_qiskit= get_unitary_from_qiskit_circuit( circuit )
+            U3_qiskit = np.asarray(U3_qiskit)
+
+            # apply the gate on the input array/matrix 
+            #U3_qiskit_apply_gate=np.matmul(U3_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            U3_squander=test_matrix
+
+            # apply the gate on the input array/matrix                
+            U3.apply_to(parameters, U3_squander )        
 
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=U3_squander-U3_qiskit
 
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 )
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_X.py` & `squander-1.8.0/qgd_python/gates/test/test_Z.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,62 +1,111 @@
 import numpy as np
 import random
 
 from qiskit import QuantumCircuit
 from qiskit.visualization import plot_histogram
 
 from qgd_python.utils import get_unitary_from_qiskit_circuit
-
-pi=np.pi
-
+from qgd_python.gates.qgd_Z import qgd_Z
+from scipy.stats import unitary_group
 
 class Test_operations_squander:
     """This is a test class of the python iterface to compare the SQUANDER and the qiskit decomposition"""
-#SQUANDER#
 
-    def test_X_squander(self):
+
+
+
+    def test_Z_get_matrix(self):
         r"""
         This method is called by pytest. 
         Test to create an instance of U3 gate and compare with qiskit.
         """
 
-        from qgd_python.gates.qgd_X import qgd_X
+        pi=np.pi
 
-        # number of qubits
-        qbit_num = 3
+        for qbit_num in range(1,7):
 
-        # target qbit
-        target_qbit = 0
+            # target qbit
+            target_qbit = qbit_num-1
 
-        # creating an instance of the C++ class
-        X = qgd_X( qbit_num, target_qbit )
-                
-        X_squander = X.get_Matrix( )
-        
-        #print(X_squander)
+            # creating an instance of the C++ class
+            Z = qgd_Z( qbit_num, target_qbit )
 
-#QISKIT
+	    #SQUANDER#
 
-        # Create a Quantum Circuit acting on the q register
-        circuit = QuantumCircuit(qbit_num)
+            # get the matrix                       
+            Z_squander = Z.get_Matrix( )
+      
+	    #QISKIT
 
-        # Add the CNOT gate on control qbit and target qbit
-        circuit.x( target_qbit )
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
 
-        # the unitary matrix from the result object
-        X_qiskit = get_unitary_from_qiskit_circuit( circuit )
-        X_qiskit = np.asarray(X_qiskit)
-        
-        # Draw the circuit        
-        #print(X_qiskit)
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.z( target_qbit )
+
+            # the unitary matrix from the result object
+            Z_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            Z_qiskit = np.asarray(Z_qiskit)
+
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=Z_squander-Z_qiskit
+
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
+
+            #print("Get_matrix: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
+
+
+    def test_Z_apply_to(self):
+        r"""
+        This method is called by pytest. 
+        Test to create an instance of U3 gate and compare with qiskit.
+        """
+
+        pi=np.pi
+
+        for qbit_num in range(1,7):
+
+            # target qbit
+            target_qbit = qbit_num-1
+
+            # creating an instance of the C++ class
+            Z = qgd_Z( qbit_num, target_qbit )
         
-        #the difference between the SQUANDER and the qiskit result        
-        delta_matrix=X_squander-X_qiskit
+            #create text matrix       
+            test_matrix= np.identity( 2**qbit_num, dtype=complex )
+
+	    #QISKIT      
+
+            # Create a Quantum Circuit acting on the q register
+            circuit = QuantumCircuit(qbit_num)
+
+            # Add the CNOT gate on control qbit and target qbit
+            circuit.z( target_qbit )
+
+            # the unitary matrix from the result object
+            Z_qiskit = get_unitary_from_qiskit_circuit( circuit )
+            Z_qiskit = np.asarray(Z_qiskit)
+
+            # apply the gate on the input array/matrix 
+            #Z_qiskit_apply_gate=np.matmul(Z_qiskit, test_matrix)
+
+	    #SQUANDER
+
+            Z_squander = test_matrix
+
+            # apply the gate on the input array/matrix                
+            Z.apply_to(Z_squander)       
 
-        # compute norm of matrix
-        error=np.linalg.norm(delta_matrix)
+            #the difference between the SQUANDER and the qiskit result        
+            delta_matrix=Z_squander-Z_qiskit
 
-        print("The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
-        assert( error < 1e-3 ) 
+            # compute norm of matrix
+            error=np.linalg.norm(delta_matrix)
 
+            #print("Apply_to: The difference between the SQUANDER and the qiskit result is: " , np.around(error,2))
+            assert( error < 1e-3 ) 
 
 
+
```

### Comparing `squander-1.7.4/qgd_python/gates/test/test_gates.py` & `squander-1.8.0/qgd_python/gates/test/test_gates.py`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/nn/CMakeLists.txt` & `squander-1.8.0/qgd_python/nn/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/nn/qgd_nn.py` & `squander-1.8.0/qgd_python/nn/qgd_nn.py`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/nn/qgd_nn_Wrapper.cpp` & `squander-1.8.0/qgd_python/nn/qgd_nn_Wrapper.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/qgd_python/utils.py` & `squander-1.8.0/qgd_python/utils.py`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/random_unitary/Random_Orthogonal.cpp` & `squander-1.8.0/random_unitary/Random_Orthogonal.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/random_unitary/Random_Unitary.cpp` & `squander-1.8.0/random_unitary/Random_Unitary.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/random_unitary/include/Random_Orthogonal.h` & `squander-1.8.0/random_unitary/include/Random_Orthogonal.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/random_unitary/include/Random_Unitary.h` & `squander-1.8.0/random_unitary/include/Random_Unitary.h`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/setup.py` & `squander-1.8.0/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -30,15 +30,15 @@
 setup(
     name="squander",
     packages=find_packages(
         exclude=(
             "test_standalone", "test_standalone.*",
         )
     ),
-    version='1.7.4',
+    version='1.8.0',
     url="https://github.com/rakytap/sequential-quantum-gate-decomposer", 
     maintainer="Peter Rakyta",
     maintainer_email="peter.rakyta@ttk.elte.hu",
     include_package_data=True,
     install_requires=[
         "setuptools>=40.8.0",
         "wheel",
```

### Comparing `squander-1.7.4/squander/__init__.py` & `squander-1.8.0/squander/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,14 @@
 # python exported interfaces of the SQUANDER package
 
+#
+from qgd_python import utils as utils
 #decomposition classes
 from qgd_python.decomposition.qgd_N_Qubit_Decomposition_adaptive import qgd_N_Qubit_Decomposition_adaptive as N_Qubit_Decomposition_adaptive
+from qgd_python.decomposition.qgd_N_Qubit_State_Preparation_adaptive import qgd_N_Qubit_State_Preparation_adaptive as N_Qubit_State_Preparation_adaptive
 from qgd_python.decomposition.qgd_N_Qubit_Decomposition_custom import qgd_N_Qubit_Decomposition_custom as N_Qubit_Decomposition_custom
 from qgd_python.decomposition.qgd_N_Qubit_Decomposition import qgd_N_Qubit_Decomposition as N_Qubit_Decomposition
 
 #gates
 from qgd_python.gates.qgd_U3 import qgd_U3 as U3
 from qgd_python.gates.qgd_X import qgd_X  as X
 from qgd_python.gates.qgd_Y import qgd_Y  as Y
```

### Comparing `squander-1.7.4/squander.egg-info/PKG-INFO` & `squander-1.8.0/squander.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: squander
-Version: 1.7.4
+Version: 1.8.0
 Summary: The C++ binding for the SQUANDER package
 Home-page: https://github.com/rakytap/sequential-quantum-gate-decomposer
 Maintainer: Peter Rakyta
 Maintainer-email: peter.rakyta@ttk.elte.hu
 License: GNU General Public License v3.0
 Keywords: test,cmake,extension
 Classifier: Intended Audience :: Developers
@@ -224,16 +224,99 @@
 Thus, in order to get the decomposition of a unitary, one should rather provide the complex transpose of this unitary as the input for the SQUANDER decomposing process, as can be seen in the examples.
 
 
 ## Python Interface
 
 The SQUANDER package contains a Python interface allowing the access of the functionalities of the SQUANDER package from Python. 
 The usage of the SQUANDER Python interface is demonstrated in the example files in the directory **examples** located in the directory **path/to/SQUANDER/package**, or in test files located in sub-directories of **path/to/SQUANDER/package/qgd_python/*/test**. 
-The example files import the necessary **qgd_python** modules containing the wrapper classes to interface with the C++ SQUANDER library. 
-(So the SQUANDER package need to be installed or the compiled package needs to be added to the Python search path.)
+
+### Example code snippet
+
+Here we provide an example to use the SQUANDER package. The following python interface is accessible from version 1.8.0. 
+In this example we use two optimization engines for the decomposition:
+1. An evolutionary engine called AGENTS
+2. Second order gradient descend algorithm (BFGS)
+
+Firstly we construct a Python map to set hyper-parameters during the gate synthesis.
+
+        #Python map containing hyper-parameters
+        config = { 'max_outer_iterations': 1, 
+                    'max_inner_iterations_agent': 25000, 
+                    'max_inner_iterations_compression': 10000,
+                    'max_inner_iterations' : 500,
+                    'max_inner_iterations_final': 5000, 		
+                    'Randomized_Radius': 0.3, 
+                    'randomized_adaptive_layers': 1,
+                    'optimization_tolerance_agent': 1e-4,
+                    'optimization_tolerance': 1e-8,
+                    'agent_num': 10}
+ 
+Next we initialize the decomposition class with the unitary Umtx to be decomposed. 
+
+        # creating a class to decompose the unitary
+        from squander import N_Qubit_Decomposition_adaptive
+        cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config )
+
+The verbosity of the execution output can be controlled by the function call 
+
+        # setting the verbosity of the decomposition
+        cDecompose.set_Verbose( 3 )
+
+
+We construct the initial trial gate structure for the optimization consisting of 2 levels of adaptive layer. 
+(1 level is made of qubit_num*(qubit_num-1) two-qubit building blocks if all-to-all connectivity is assumed)
+
+
+        # adding decomposing layers to the gate structure
+        levels = 2
+        for idx in range(levels):
+            cDecompose.add_Adaptive_Layers()
+
+        cDecompose.add_Finalyzing_Layer_To_Gate_Structure()
+        
+We can construct an initial parameters set for the optimization by retrieving the number of free parameters. If the initial parameter set is not set, random parameters are used by default.
+
+        # setting intial parameter set
+        parameter_num = cDecompose.get_Parameter_Num()
+        parameters = np.zeros( (parameter_num,1), dtype=np.float64 )
+        cDecompose.set_Optimized_Parameters( parameters )
+
+We can use between several engines to solve the optimization problem. Here we use an evolutionary based algorithm named 'AGENTS'
+
+        # setting optimizer
+        cDecompose.set_Optimizer("AGENTS")
+	
+The optimization process is started by the function call	
+
+        # starting the decomposition
+        cDecompose.get_Initial_Circuit()
+	
+The optimization process terminates by either reaching the tolerance 'optimization_tolerance_agent' or by reaching the maximal iteration number 'max_inner_iterations_agent', or if the engines identifies a convergence to a local minimum. The SQUANDER framework enables one to continue the optimization using a different engine. In particular we set a second order gradient descend method 'BFGS' 
+
+        # setting optimizer
+        cDecompose.set_Optimizer("BFGS")
+
+        # continue the decomposition with a second optimizer method
+        cDecompose.get_Initial_Circuit()
+	
+After solving the optimization problem for the initial gate structure, we can initiate gate compression iterations. (This step can be omited.)	
+
+        # starting compression iterations
+        cDecompose.Compress_Circuit()
+	
+By finalizing the gate structure we replace the CRY gates with CNOT gates. (CRY gates with small rotation angle are approximately expressed with a single CNOT gate, so further optimization process needs to be initiated.)
+
+        # finalize the gate structure (replace CRY gates with CNOT gates)
+        cDecompose.Finalize_Circuit()
+
+Finally, we can retrieve the decomposed quantum circuit in QISKIT format.
+
+        # get the decomposing operations
+        quantum_circuit = cDecompose.get_Quantum_Circuit()
+
 
 
 ### How to cite us
 
 If you have found our work useful for your research project, please cite us by
 
 [1] Péter Rakyta, Zoltán Zimborás, Approaching the theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022). <br>
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: squander Version: 1.7.4 Summary: The C++ binding
+Metadata-Version: 2.1 Name: squander Version: 1.8.0 Summary: The C++ binding
 for the SQUANDER package Home-page: https://github.com/rakytap/sequential-
 quantum-gate-decomposer Maintainer: Peter Rakyta Maintainer-email:
 peter.rakyta@ttk.elte.hu License: GNU General Public License v3.0 Keywords:
 test,cmake,extension Classifier: Intended Audience :: Developers Classifier:
 Natural Language :: English Classifier: Programming Language :: C Classifier:
 Programming Language :: C++ Description-Content-Type: text/markdown License-
 File: LICENSE [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4508680.svg)]
@@ -164,19 +164,62 @@
 decomposition of a unitary, one should rather provide the complex transpose of
 this unitary as the input for the SQUANDER decomposing process, as can be seen
 in the examples. ## Python Interface The SQUANDER package contains a Python
 interface allowing the access of the functionalities of the SQUANDER package
 from Python. The usage of the SQUANDER Python interface is demonstrated in the
 example files in the directory **examples** located in the directory **path/to/
 SQUANDER/package**, or in test files located in sub-directories of **path/to/
-SQUANDER/package/qgd_python/*/test**. The example files import the necessary
-**qgd_python** modules containing the wrapper classes to interface with the C++
-SQUANDER library. (So the SQUANDER package need to be installed or the compiled
-package needs to be added to the Python search path.) ### How to cite us If you
-have found our work useful for your research project, please cite us by [1]
-PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the theoretical limit in quantum
-gate decomposition, Quantum 6, 710 (2022).
+SQUANDER/package/qgd_python/*/test**. ### Example code snippet Here we provide
+an example to use the SQUANDER package. The following python interface is
+accessible from version 1.8.0. In this example we use two optimization engines
+for the decomposition: 1. An evolutionary engine called AGENTS 2. Second order
+gradient descend algorithm (BFGS) Firstly we construct a Python map to set
+hyper-parameters during the gate synthesis. #Python map containing hyper-
+parameters config = { 'max_outer_iterations': 1, 'max_inner_iterations_agent':
+25000, 'max_inner_iterations_compression': 10000, 'max_inner_iterations' : 500,
+'max_inner_iterations_final': 5000, 'Randomized_Radius': 0.3,
+'randomized_adaptive_layers': 1, 'optimization_tolerance_agent': 1e-4,
+'optimization_tolerance': 1e-8, 'agent_num': 10} Next we initialize the
+decomposition class with the unitary Umtx to be decomposed. # creating a class
+to decompose the unitary from squander import N_Qubit_Decomposition_adaptive
+cDecompose = N_Qubit_Decomposition_adaptive( Umtx.conj().T, config=config ) The
+verbosity of the execution output can be controlled by the function call #
+setting the verbosity of the decomposition cDecompose.set_Verbose( 3 ) We
+construct the initial trial gate structure for the optimization consisting of 2
+levels of adaptive layer. (1 level is made of qubit_num*(qubit_num-1) two-qubit
+building blocks if all-to-all connectivity is assumed) # adding decomposing
+layers to the gate structure levels = 2 for idx in range(levels):
+cDecompose.add_Adaptive_Layers()
+cDecompose.add_Finalyzing_Layer_To_Gate_Structure() We can construct an initial
+parameters set for the optimization by retrieving the number of free
+parameters. If the initial parameter set is not set, random parameters are used
+by default. # setting intial parameter set parameter_num =
+cDecompose.get_Parameter_Num() parameters = np.zeros( (parameter_num,1),
+dtype=np.float64 ) cDecompose.set_Optimized_Parameters( parameters ) We can use
+between several engines to solve the optimization problem. Here we use an
+evolutionary based algorithm named 'AGENTS' # setting optimizer
+cDecompose.set_Optimizer("AGENTS") The optimization process is started by the
+function call # starting the decomposition cDecompose.get_Initial_Circuit() The
+optimization process terminates by either reaching the tolerance
+'optimization_tolerance_agent' or by reaching the maximal iteration number
+'max_inner_iterations_agent', or if the engines identifies a convergence to a
+local minimum. The SQUANDER framework enables one to continue the optimization
+using a different engine. In particular we set a second order gradient descend
+method 'BFGS' # setting optimizer cDecompose.set_Optimizer("BFGS") # continue
+the decomposition with a second optimizer method cDecompose.get_Initial_Circuit
+() After solving the optimization problem for the initial gate structure, we
+can initiate gate compression iterations. (This step can be omited.) # starting
+compression iterations cDecompose.Compress_Circuit() By finalizing the gate
+structure we replace the CRY gates with CNOT gates. (CRY gates with small
+rotation angle are approximately expressed with a single CNOT gate, so further
+optimization process needs to be initiated.) # finalize the gate structure
+(replace CRY gates with CNOT gates) cDecompose.Finalize_Circuit() Finally, we
+can retrieve the decomposed quantum circuit in QISKIT format. # get the
+decomposing operations quantum_circuit = cDecompose.get_Quantum_Circuit() ###
+How to cite us If you have found our work useful for your research project,
+please cite us by [1] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Approaching the
+theoretical limit in quantum gate decomposition, Quantum 6, 710 (2022).
 [2] PÃ©ter Rakyta, ZoltÃ¡n ZimborÃ¡s, Efficient quantum gate decomposition via
 adaptive circuit compression, arXiv:2203.04426.
 [3] Peter Rakyta, Gregory Morse, Jakab NÃ¡dori, Zita Majnay-TakÃ¡cs, Oskar
 Mencer, ZoltÃ¡n ZimborÃ¡s, Highly optimized quantum circuits synthesized via
 data-flow engines, arXiv:2211.07685
```

### Comparing `squander-1.7.4/squander.egg-info/SOURCES.txt` & `squander-1.8.0/squander.egg-info/SOURCES.txt`

 * *Files 8% similar despite different names*

```diff
@@ -4,25 +4,27 @@
 README.md
 pyproject.toml
 setup.py
 cmake/check_AVX.cmake
 common/Adam.cpp
 common/common.cpp
 common/common_DFE.cpp
+common/config_element.cpp
 common/dot.cpp
 common/logging.cpp
 common/matrix.cpp
 common/matrix_real.cpp
 common/mpi_base.cpp
 common/numpy_interface.cpp
 common/include/Adam.h
 common/include/Config.h.in
 common/include/QGDTypes.h
 common/include/common.h
 common/include/common_DFE.h
+common/include/config_element.h
 common/include/dot.h
 common/include/logging.h
 common/include/matrix.h
 common/include/matrix_base.h
 common/include/matrix_real.h
 common/include/mpi_base.h
 common/include/numpy_interface.h
@@ -77,36 +79,44 @@
 gates/include/SYC.h
 gates/include/U3.h
 gates/include/UN.h
 gates/include/X.h
 gates/include/Y.h
 gates/include/Z.h
 gates/kernels/apply_kernel_to_input_AVX.cpp
+gates/kernels/apply_kernel_to_state_vector_input.cpp
 gates/kernels/include/apply_kernel_to_input_AVX.h
+gates/kernels/include/apply_kernel_to_state_vector_input.h
 nn/NN.cpp
 nn/include/NN.h
+optimization_engines/RL_experience.cpp
+optimization_engines/include/RL_experience.h
 qgd_python/__init__.py
 qgd_python/utils.py
 qgd_python/decomposition/CMakeLists.txt
 qgd_python/decomposition/__init__.py
 qgd_python/decomposition/qgd_N_Qubit_Decomposition.py
 qgd_python/decomposition/qgd_N_Qubit_Decomposition_Wrapper.cpp
 qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive.py
 qgd_python/decomposition/qgd_N_Qubit_Decomposition_adaptive_Wrapper.cpp
 qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom.py
 qgd_python/decomposition/qgd_N_Qubit_Decomposition_custom_Wrapper.cpp
+qgd_python/decomposition/qgd_N_Qubit_State_Preparation_adaptive.py
 qgd_python/decomposition/test/__init__.py
+qgd_python/decomposition/test/test_Compression.py
 qgd_python/decomposition/test/test_Global_Phase.py
 qgd_python/decomposition/test/test_IBM.py
 qgd_python/decomposition/test/test_Project_Name.py
 qgd_python/decomposition/test/test_QX2.py
+qgd_python/decomposition/test/test_State_Preparation.py
 qgd_python/decomposition/test/test_Unitary.py
 qgd_python/decomposition/test/test_decomposition.py
 qgd_python/decomposition/test/test_fmo.py
 qgd_python/decomposition/test/test_heavy_hex.py
+qgd_python/decomposition/test/test_optmization_problem_combined.py
 qgd_python/decomposition/test/test_parametric_circuit.py
 qgd_python/gates/CMakeLists.txt
 qgd_python/gates/__init__.py
 qgd_python/gates/qgd_CH.cpp
 qgd_python/gates/qgd_CNOT.cpp
 qgd_python/gates/qgd_CZ.cpp
 qgd_python/gates/qgd_Gates_Block.cpp
@@ -125,14 +135,16 @@
 qgd_python/gates/test/test_CZ.py
 qgd_python/gates/test/test_RX.py
 qgd_python/gates/test/test_RY.py
 qgd_python/gates/test/test_RZ.py
 qgd_python/gates/test/test_SX.py
 qgd_python/gates/test/test_U3.py
 qgd_python/gates/test/test_X.py
+qgd_python/gates/test/test_Y.py
+qgd_python/gates/test/test_Z.py
 qgd_python/gates/test/test_gates.py
 qgd_python/nn/CMakeLists.txt
 qgd_python/nn/__init__.py
 qgd_python/nn/qgd_nn.py
 qgd_python/nn/qgd_nn_Wrapper.cpp
 random_unitary/Random_Orthogonal.cpp
 random_unitary/Random_Unitary.cpp
```

### Comparing `squander-1.7.4/test_standalone/CMakeLists.txt` & `squander-1.8.0/test_standalone/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/test_standalone/custom_gate_structure_test.cpp` & `squander-1.8.0/test_standalone/custom_gate_structure_test.cpp`

 * *Files identical despite different names*

### Comparing `squander-1.7.4/test_standalone/decomposition_test.cpp` & `squander-1.8.0/test_standalone/decomposition_test.cpp`

 * *Files identical despite different names*

