# Comparing `tmp/pyqtorch-0.2.3.tar.gz` & `tmp/pyqtorch-0.2.4.tar.gz`

## Comparing `pyqtorch-0.2.3.tar` & `pyqtorch-0.2.4.tar`

### file list

```diff
@@ -1,77 +1,76 @@
--rw-r--r--   0        0        0      559 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.pre-commit-config.yaml
--rw-r--r--   0        0        0      276 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/README.md
--rw-r--r--   0        0        0     1555 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/mkdocs.yml
--rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/publish.sh
--rw-r--r--   0        0        0      227 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/readthedocs.yml
--rw-r--r--   0        0        0       52 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/setup.py
--rw-r--r--   0        0        0     1039 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.github/workflows/run-tests-and-mypy.yml
--rw-r--r--   0        0        0        1 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/.gitignore
--rw-r--r--   0        0        0       43 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/CACHEDIR.TAG
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/21836652c37a637f
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/2602555962d0fc4c
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/30645ad5f1f1dcfe
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/317d2f17a1075099
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/41d845d0f90a6417
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/617ac8c861e982f1
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/68cc7f39a1692629
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/71de32d0dc4ef210
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/7ab8961a5fd3e34a
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/7b50e93d7b401d37
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/7e9bc91eb0e4bec7
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/8446b77184378e13
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/8c22cf14dc3075f3
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/8f831c3208d022cd
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/963472f7f566f99d
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/9b70b475da072d2b
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/a3b4cbbb65fe8420
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/aaa2c54c6449792b
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/af9c8e117f709f43
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/c73abac16d830acc
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/ce5cb2c96a07a572
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/ce5dade58b1ccd69
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/d49ef2d71d47c091
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/df86f5c8bc05afc4
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/e69f22aa2552f985
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/f6f6f60064e20f97
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.ruff_cache/content/f78c2e380fc669b7
--rw-r--r--   0        0        0    57645 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/QAOA.ipynb
--rw-r--r--   0        0        0   154586 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/fit_function.ipynb
--rw-r--r--   0        0        0    74094 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/getting_started.ipynb
--rw-r--r--   0        0        0    14131 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/index.ipynb
--rw-r--r--   0        0        0    46162 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/deprecated/QAOA.ipynb
--rw-r--r--   0        0        0    19339 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/deprecated/bench.py
--rw-r--r--   0        0        0    74042 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/deprecated/fit_function.ipynb
--rw-r--r--   0        0        0   121176 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/deprecated/ham_evol_comparison.ipynb
--rw-r--r--   0        0        0     6459 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/docs/deprecated/state_evolution.ipynb
--rw-r--r--   0        0        0      842 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/__init__.py
--rw-r--r--   0        0        0     3544 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/ansatz.py
--rw-r--r--   0        0        0     1051 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/embedding.py
--rw-r--r--   0        0        0     3479 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/matrices.py
--rw-r--r--   0        0        0     6255 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/matrices_sparse.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/py.typed
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/converters/__init__.py
--rw-r--r--   0        0        0     1890 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/converters/store_ops.py
--rw-r--r--   0        0        0     2701 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/converters/to_qiskit.py
--rw-r--r--   0        0        0      581 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/__init__.py
--rw-r--r--   0        0        0    24532 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/batched_operation.py
--rw-r--r--   0        0        0     2341 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/circuit.py
--rw-r--r--   0        0        0     1719 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/measurement.py
--rw-r--r--   0        0        0    22213 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/operation.py
--rw-r--r--   0        0        0     5940 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/core/utils.py
--rw-r--r--   0        0        0      417 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/__init__.py
--rw-r--r--   0        0        0     2638 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/circuit.py
--rw-r--r--   0        0        0     5882 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/hamevo.py
--rw-r--r--   0        0        0     7730 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/parametric.py
--rw-r--r--   0        0        0     3417 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/primitive.py
--rw-r--r--   0        0        0      408 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyqtorch/modules/utils.py
--rw-r--r--   0        0        0     3046 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/conftest.py
--rw-r--r--   0        0        0     1453 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_batched_operations.py
--rw-r--r--   0        0        0     1121 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_converters.py
--rw-r--r--   0        0        0     3796 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_module_hamevo.py
--rw-r--r--   0        0        0     2639 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_modules.py
--rw-r--r--   0        0        0     4872 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_operations.py
--rw-r--r--   0        0        0     6496 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/tests/test_operations_hamevo.py
--rw-r--r--   0        0        0      446 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/.gitignore
--rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/LICENSE
--rw-r--r--   0        0        0     2634 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/pyproject.toml
--rw-r--r--   0        0        0     1460 2020-02-02 00:00:00.000000 pyqtorch-0.2.3/PKG-INFO
+-rw-r--r--   0        0        0      559 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      276 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/README.md
+-rw-r--r--   0        0        0     1555 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/mkdocs.yml
+-rw-r--r--   0        0        0      227 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/readthedocs.yml
+-rw-r--r--   0        0        0       52 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/setup.py
+-rw-r--r--   0        0        0     1039 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.github/workflows/run-tests-and-mypy.yml
+-rw-r--r--   0        0        0        1 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/.gitignore
+-rw-r--r--   0        0        0       43 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/CACHEDIR.TAG
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/21836652c37a637f
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/2602555962d0fc4c
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/30645ad5f1f1dcfe
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/317d2f17a1075099
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/41d845d0f90a6417
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/617ac8c861e982f1
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/68cc7f39a1692629
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/71de32d0dc4ef210
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/7ab8961a5fd3e34a
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/7b50e93d7b401d37
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/7e9bc91eb0e4bec7
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/8446b77184378e13
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/8c22cf14dc3075f3
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/8f831c3208d022cd
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/963472f7f566f99d
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/9b70b475da072d2b
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/a3b4cbbb65fe8420
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/aaa2c54c6449792b
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/af9c8e117f709f43
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/c73abac16d830acc
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/ce5cb2c96a07a572
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/ce5dade58b1ccd69
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/d49ef2d71d47c091
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/df86f5c8bc05afc4
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/e69f22aa2552f985
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/f6f6f60064e20f97
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.ruff_cache/content/f78c2e380fc669b7
+-rw-r--r--   0        0        0    57645 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/QAOA.ipynb
+-rw-r--r--   0        0        0   154586 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/fit_function.ipynb
+-rw-r--r--   0        0        0    74094 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/getting_started.ipynb
+-rw-r--r--   0        0        0    14131 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/index.ipynb
+-rw-r--r--   0        0        0    46162 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/deprecated/QAOA.ipynb
+-rw-r--r--   0        0        0    19339 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/deprecated/bench.py
+-rw-r--r--   0        0        0    74042 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/deprecated/fit_function.ipynb
+-rw-r--r--   0        0        0   121176 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/deprecated/ham_evol_comparison.ipynb
+-rw-r--r--   0        0        0     6459 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/docs/deprecated/state_evolution.ipynb
+-rw-r--r--   0        0        0      842 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/__init__.py
+-rw-r--r--   0        0        0     3544 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/ansatz.py
+-rw-r--r--   0        0        0     1051 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/embedding.py
+-rw-r--r--   0        0        0     3479 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/matrices.py
+-rw-r--r--   0        0        0     6255 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/matrices_sparse.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/py.typed
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/converters/__init__.py
+-rw-r--r--   0        0        0     1890 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/converters/store_ops.py
+-rw-r--r--   0        0        0     2701 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/converters/to_qiskit.py
+-rw-r--r--   0        0        0      581 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/__init__.py
+-rw-r--r--   0        0        0    24532 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/batched_operation.py
+-rw-r--r--   0        0        0     2341 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/circuit.py
+-rw-r--r--   0        0        0     1719 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/measurement.py
+-rw-r--r--   0        0        0    22213 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/operation.py
+-rw-r--r--   0        0        0     5940 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/core/utils.py
+-rw-r--r--   0        0        0      439 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/__init__.py
+-rw-r--r--   0        0        0     2728 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/circuit.py
+-rw-r--r--   0        0        0     7686 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/hamevo.py
+-rw-r--r--   0        0        0     7730 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/parametric.py
+-rw-r--r--   0        0        0     3417 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/primitive.py
+-rw-r--r--   0        0        0      408 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyqtorch/modules/utils.py
+-rw-r--r--   0        0        0     3046 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/conftest.py
+-rw-r--r--   0        0        0     1453 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_batched_operations.py
+-rw-r--r--   0        0        0     1121 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_converters.py
+-rw-r--r--   0        0        0     5104 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_module_hamevo.py
+-rw-r--r--   0        0        0     3281 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_modules.py
+-rw-r--r--   0        0        0     4872 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_operations.py
+-rw-r--r--   0        0        0     6496 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/tests/test_operations_hamevo.py
+-rw-r--r--   0        0        0      446 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/.gitignore
+-rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/LICENSE
+-rw-r--r--   0        0        0     2634 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/pyproject.toml
+-rw-r--r--   0        0        0     1460 2020-02-02 00:00:00.000000 pyqtorch-0.2.4/PKG-INFO
```

### Comparing `pyqtorch-0.2.3/.pre-commit-config.yaml` & `pyqtorch-0.2.4/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/mkdocs.yml` & `pyqtorch-0.2.4/mkdocs.yml`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/.github/workflows/run-tests-and-mypy.yml` & `pyqtorch-0.2.4/.github/workflows/run-tests-and-mypy.yml`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/QAOA.ipynb` & `pyqtorch-0.2.4/docs/QAOA.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/fit_function.ipynb` & `pyqtorch-0.2.4/docs/fit_function.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/getting_started.ipynb` & `pyqtorch-0.2.4/docs/getting_started.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/index.ipynb` & `pyqtorch-0.2.4/docs/index.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/deprecated/QAOA.ipynb` & `pyqtorch-0.2.4/docs/deprecated/QAOA.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/deprecated/bench.py` & `pyqtorch-0.2.4/docs/deprecated/bench.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/deprecated/fit_function.ipynb` & `pyqtorch-0.2.4/docs/deprecated/fit_function.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/deprecated/ham_evol_comparison.ipynb` & `pyqtorch-0.2.4/docs/deprecated/ham_evol_comparison.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/docs/deprecated/state_evolution.ipynb` & `pyqtorch-0.2.4/docs/deprecated/state_evolution.ipynb`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/__init__.py` & `pyqtorch-0.2.4/pyqtorch/__init__.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/ansatz.py` & `pyqtorch-0.2.4/pyqtorch/ansatz.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/embedding.py` & `pyqtorch-0.2.4/pyqtorch/embedding.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/matrices.py` & `pyqtorch-0.2.4/pyqtorch/matrices.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/matrices_sparse.py` & `pyqtorch-0.2.4/pyqtorch/matrices_sparse.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/converters/store_ops.py` & `pyqtorch-0.2.4/pyqtorch/converters/store_ops.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/converters/to_qiskit.py` & `pyqtorch-0.2.4/pyqtorch/converters/to_qiskit.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/__init__.py` & `pyqtorch-0.2.4/pyqtorch/core/__init__.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/batched_operation.py` & `pyqtorch-0.2.4/pyqtorch/core/batched_operation.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/circuit.py` & `pyqtorch-0.2.4/pyqtorch/core/circuit.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/measurement.py` & `pyqtorch-0.2.4/pyqtorch/core/measurement.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/operation.py` & `pyqtorch-0.2.4/pyqtorch/core/operation.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/core/utils.py` & `pyqtorch-0.2.4/pyqtorch/core/utils.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/modules/circuit.py` & `pyqtorch-0.2.4/pyqtorch/modules/circuit.py`

 * *Files 2% similar despite different names*

```diff
@@ -43,16 +43,19 @@
     def forward(self, state: torch.Tensor, thetas: torch.Tensor = None) -> torch.Tensor:
         for op in self.operations:
             state = op(state, thetas)
         return state
 
     @property
     def _device(self) -> torch.device:
-        (_, buffer) = next(self.named_buffers())
-        return buffer.device
+        try:
+            (_, buffer) = next(self.named_buffers())
+            return buffer.device
+        except StopIteration:
+            return torch.device("cpu")
 
     def init_state(self, batch_size: int) -> torch.Tensor:
         return zero_state(self.n_qubits, batch_size, device=self._device)
 
 
 def FeaturemapLayer(n_qubits: int, Op: Any) -> QuantumCircuit:
     operations = [Op([i], n_qubits) for i in range(n_qubits)]
```

### Comparing `pyqtorch-0.2.3/pyqtorch/modules/hamevo.py` & `pyqtorch-0.2.4/pyqtorch/modules/hamevo.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from __future__ import annotations
 
 from functools import lru_cache
 from typing import Any, Optional, Tuple
 
 import torch
+from torch.nn import Module
 
 from pyqtorch.core.utils import _apply_batch_gate
 from pyqtorch.modules.utils import is_diag, is_real
 
 BATCH_DIM = 2
 
 
@@ -159,7 +160,52 @@
         else:
             H_T = torch.transpose(self.H, 0, -1)
             evol_exp_arg = H_T * (-1j * t_evo).view((-1, 1, 1))
             evol_operator_T = torch.linalg.matrix_exp(evol_exp_arg)
             evol_operator = torch.transpose(evol_operator_T, 0, -1)
 
         return _apply_batch_gate(state, evol_operator, self.qubits, self.n_qubits, batch_size_h)
+
+
+class HamiltonianEvolution(Module):
+    def __init__(self, qubits: Any, n_qubits: int, n_steps: int = 100):
+        super().__init__()
+        self.qubits = qubits
+        self.n_qubits = n_qubits
+        self.n_steps = n_steps
+
+    def forward(self, H: torch.Tensor, t: torch.Tensor, state: torch.Tensor) -> torch.Tensor:
+        return self.apply(H, t, state)
+
+    def apply(self, H: torch.Tensor, t: torch.Tensor, state: torch.Tensor) -> torch.Tensor:
+        if len(H.size()) < 3:
+            H = H.unsqueeze(2)
+        batch_size_h = H.size()[BATCH_DIM]
+
+        # Check if all hamiltonians in the batch are diagonal
+        diag_check = torch.tensor([is_diag(H[..., i]) for i in range(batch_size_h)])
+        batch_is_diag = bool(torch.prod(diag_check))
+
+        batch_size_t = len(t)
+        t_evo = torch.zeros(batch_size_h).to(torch.cdouble)
+
+        if batch_size_t >= batch_size_h:
+            t_evo = t[:batch_size_h]
+        else:
+            if batch_size_t == 1:
+                t_evo[:] = t[0]
+            else:
+                t_evo[:batch_size_t] = t
+
+        if batch_is_diag:
+            # Skips the matrix exponential for diagonal hamiltonians
+            H_diagonals = torch.diagonal(H)
+            evol_exp_arg = H_diagonals * (-1j * t_evo).view((-1, 1))
+            evol_operator_T = torch.diag_embed(torch.exp(evol_exp_arg))
+            evol_operator = torch.transpose(evol_operator_T, 0, -1)
+        else:
+            H_T = torch.transpose(H, 0, -1)
+            evol_exp_arg = H_T * (-1j * t_evo).view((-1, 1, 1))
+            evol_operator_T = torch.linalg.matrix_exp(evol_exp_arg)
+            evol_operator = torch.transpose(evol_operator_T, 0, -1)
+
+        return _apply_batch_gate(state, evol_operator, self.qubits, self.n_qubits, batch_size_h)
```

### Comparing `pyqtorch-0.2.3/pyqtorch/modules/parametric.py` & `pyqtorch-0.2.4/pyqtorch/modules/parametric.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyqtorch/modules/primitive.py` & `pyqtorch-0.2.4/pyqtorch/modules/primitive.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/tests/conftest.py` & `pyqtorch-0.2.4/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/tests/test_batched_operations.py` & `pyqtorch-0.2.4/tests/test_batched_operations.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/tests/test_converters.py` & `pyqtorch-0.2.4/tests/test_converters.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/tests/test_module_hamevo.py` & `pyqtorch-0.2.4/tests/test_module_hamevo.py`

 * *Files 21% similar despite different names*

```diff
@@ -58,14 +58,48 @@
         H_diag = torch.diag(get_diag)
         H_batch[..., i] = H_diag
     return H_batch
 
 
 @pytest.mark.parametrize(
     "ham_evo",
+    [pyq.HamiltonianEvolution],
+)
+def test_ham_modules_single(ham_evo: torch.nn.Module) -> None:
+    n_qubits = 4
+    H = Hamiltonian(1)
+    t_evo = torch.tensor([torch.pi / 4], dtype=torch.cdouble)
+    hamevo = ham_evo(range(n_qubits), n_qubits)
+    psi = pyq.uniform_state(n_qubits)
+    psi_star = hamevo(H, t_evo, psi)
+    result = overlap(psi_star, psi)
+    result = result if isinstance(result, float) else result[0]
+    assert isclose(result, 0.5)
+
+
+@pytest.mark.parametrize(
+    "ham_evo",
+    [pyq.HamiltonianEvolution],
+)
+def test_hamiltonianevolution_batch(ham_evo: torch.nn.Module) -> None:
+    n_qubits = 4
+    batch_size = 2
+    H = Hamiltonian(batch_size)
+    t_evo = torch.tensor([torch.pi / 4], dtype=torch.cdouble)
+
+    hamevo = ham_evo(range(n_qubits), n_qubits)
+    psi = pyq.uniform_state(n_qubits, batch_size)
+    psi_star = hamevo(H, t_evo, psi)
+    result = overlap(psi_star, psi)
+
+    assert map(isclose, zip(result, [0.5, 0.5]))  # type: ignore [arg-type]
+
+
+@pytest.mark.parametrize(
+    "ham_evo",
     [pyq.HamEvo, pyq.HamEvoEig, pyq.HamEvoExp],
 )
 def test_hamevo_modules_single(ham_evo: torch.nn.Module) -> None:
     n_qubits = 4
     H = Hamiltonian(1)
     t_evo = torch.tensor([torch.pi / 4], dtype=torch.cdouble)
     hamevo = ham_evo(H, t_evo, range(n_qubits), n_qubits)
@@ -108,10 +142,15 @@
     hamevo_rk4 = pyq.HamEvo(H_batch, t_evo, range(n_qubits), n_qubits)
     psi_rk4 = hamevo_rk4.forward(psi_0)
     hamevo_eig = pyq.HamEvoEig(H_batch, t_evo, range(n_qubits), n_qubits)
     psi_eig = hamevo_eig.forward(psi_0)
     hamevo_exp = pyq.HamEvoExp(H_batch, t_evo, range(n_qubits), n_qubits)
     psi_exp = hamevo_exp.forward(psi_0)
 
-    assert torch.allclose(psi_rk4, psi_eig)
-    assert torch.allclose(psi_rk4, psi_eig)
-    assert torch.allclose(psi_eig, psi_exp)
+    hamiltonian_evolution = pyq.HamiltonianEvolution(range(n_qubits), n_qubits)
+    psi_ham = hamiltonian_evolution(H_batch, t_evo, psi_0)
+
+    # assert torch.allclose(psi_rk4, psi_eig)
+    # assert torch.allclose(psi_rk4, psi_eig)
+    # assert torch.allclose(psi_eig, psi_exp)
+    tensors = [psi_rk4, psi_eig, psi_exp, psi_ham]
+    assert all(torch.allclose(tensors[i], tensors[0]) for i in range(1, len(tensors)))
```

### Comparing `pyqtorch-0.2.3/tests/test_modules.py` & `pyqtorch-0.2.4/tests/test_modules.py`

 * *Files 10% similar despite different names*

```diff
@@ -75,13 +75,33 @@
 
     # g = torch.autograd.grad(circ, thetas)
     dres_theta = torch.autograd.grad(res, phi, torch.ones_like(res), create_graph=True)[0]
     assert not torch.all(torch.isnan(dres_theta))
 
 
 @pytest.mark.parametrize("batch_size", [1, 2, 4, 6])
+def test_empy_circuit(batch_size: int) -> None:
+    n_qubits = 2
+    device = "cuda" if torch.cuda.is_available() else "cpu"
+    dtype = torch.cdouble
+
+    ops: list = []
+    circ = pyq.QuantumCircuit(n_qubits, ops).to(device=device, dtype=dtype)
+
+    state = circ.init_state(batch_size)
+    phi = torch.rand(batch_size, device=device, dtype=dtype, requires_grad=True)
+
+    assert circ(state, phi).size() == (2, 2, batch_size)
+
+    state = pyq.zero_state(n_qubits, batch_size=batch_size, device=device, dtype=dtype)
+
+    res = circ(state, phi)
+    assert not torch.all(torch.isnan(res))
+
+
+@pytest.mark.parametrize("batch_size", [1, 2, 4, 6])
 def test_U_gate(batch_size: int) -> None:
     n_qubits = 1
     u = pyq.U([0], n_qubits)
     x = torch.rand(3, batch_size)
     state = pyq.zero_state(n_qubits, batch_size=batch_size, device="cpu", dtype=torch.cdouble)
     assert not torch.all(torch.isnan(u(state, x)))
```

### Comparing `pyqtorch-0.2.3/tests/test_operations.py` & `pyqtorch-0.2.4/tests/test_operations.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/tests/test_operations_hamevo.py` & `pyqtorch-0.2.4/tests/test_operations_hamevo.py`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/LICENSE` & `pyqtorch-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pyqtorch-0.2.3/pyproject.toml` & `pyqtorch-0.2.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -10,15 +10,15 @@
     { name = "Aleksander Wennersteen", email = "aleksander.wennersteen@pasqal.com" },
     { name = "Mario Dagrada", email = "mario.dagrada@pasqal.com" },
     { name = "Dominik Seitz", email = "dominik.seitz@pasqal.com" },
     { name = "Niklas Heim", email = "niklas.heim@pasqal.com" },
 ]
 requires-python = ">=3.8.1,<3.11"
 license = {text = "Proprietary"}
-version = "0.2.3"
+version = "0.2.4"
 classifiers=[
     "License :: Other/Proprietary License",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
```

### Comparing `pyqtorch-0.2.3/PKG-INFO` & `pyqtorch-0.2.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyqtorch
-Version: 0.2.3
+Version: 0.2.4
 Summary: An efficient, large-scale emulator designed for quantum machine learning, seamlessly integrated with a PyTorch backend. Please refer to https://pyqtorch.readthedocs.io/en/latest/ for setup and usage info, along with the full documentation.
 Author-email: Slimane Thabet <slimane.thabet@pasqal.com>, Aleksander Wennersteen <aleksander.wennersteen@pasqal.com>, Mario Dagrada <mario.dagrada@pasqal.com>, Dominik Seitz <dominik.seitz@pasqal.com>, Niklas Heim <niklas.heim@pasqal.com>
 License: Proprietary
 License-File: LICENSE
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
```

