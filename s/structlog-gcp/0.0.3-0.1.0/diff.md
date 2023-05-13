# Comparing `tmp/structlog_gcp-0.0.3.tar.gz` & `tmp/structlog_gcp-0.1.0.tar.gz`

## Comparing `structlog_gcp-0.0.3.tar` & `structlog_gcp-0.1.0.tar`

### file list

```diff
@@ -1,42 +1,335 @@
--rw-r--r--   0        0        0    53248 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.coverage
--rw-r--r--   0        0        0       30 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.flake8
--rw-r--r--   0        0        0      157 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.github/renovate.json5
--rw-r--r--   0        0        0     1876 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.github/workflows/build-test-release.yml
--rw-r--r--   0        0        0       37 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.pytest_cache/.gitignore
--rw-r--r--   0        0        0      191 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.pytest_cache/CACHEDIR.TAG
--rw-r--r--   0        0        0      302 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.pytest_cache/README.md
--rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.pytest_cache/v/cache/nodeids
--rw-r--r--   0        0        0        2 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/.pytest_cache/v/cache/stepwise
--rw-r--r--   0        0        0    47225 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/docs/errors.png
--rw-r--r--   0        0        0    45056 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/docs/logs.png
--rw-r--r--   0        0        0      504 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/examples/cloud-function/.gcloudignore
--rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/examples/cloud-function/Makefile
--rw-r--r--   0        0        0     1987 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/examples/cloud-function/main.py
--rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/examples/cloud-function/requirements.txt
--rw-r--r--   0        0        0       27 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/.gitignore
--rw-r--r--   0        0        0    20650 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/coverage_html.js
--rw-r--r--   0        0        0     4995 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76___init___py.html
--rw-r--r--   0        0        0    10701 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_base_py.html
--rw-r--r--   0        0        0    32208 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_errors_py.html
--rw-r--r--   0        0        0    33046 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_processors_py.html
--rw-r--r--   0        0        0     6039 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_types_py.html
--rw-r--r--   0        0        0     1732 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/favicon_32.png
--rw-r--r--   0        0        0     5742 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/index.html
--rw-r--r--   0        0        0     9004 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/keybd_closed.png
--rw-r--r--   0        0        0     9003 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/keybd_open.png
--rw-r--r--   0        0        0     1138 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/status.json
--rw-r--r--   0        0        0    12429 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/htmlcov/style.css
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/__about__.py
--rw-r--r--   0        0        0       45 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/__init__.py
--rw-r--r--   0        0        0      569 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/base.py
--rw-r--r--   0        0        0     3857 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/errors.py
--rw-r--r--   0        0        0     4037 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/processors.py
--rw-r--r--   0        0        0      212 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/structlog_gcp/types.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/tests/__init__.py
--rw-r--r--   0        0        0      751 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/tests/conftest.py
--rw-r--r--   0        0        0      822 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/tests/fakes.py
--rw-r--r--   0        0        0     1568 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/tests/test_log.py
--rw-r--r--   0        0        0     1094 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/LICENSE
--rw-r--r--   0        0        0     2690 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/README.md
--rw-r--r--   0        0        0     1628 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/pyproject.toml
--rw-r--r--   0        0        0     3597 2020-02-02 00:00:00.000000 structlog_gcp-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0    53248 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.coverage
+-rw-r--r--   0        0        0       30 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.flake8
+-rw-r--r--   0        0        0      157 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.github/renovate.json5
+-rw-r--r--   0        0        0     2125 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.github/workflows/build-test-release.yml
+-rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/.gitignore
+-rw-r--r--   0        0        0      190 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/CACHEDIR.TAG
+-rw-r--r--   0        0        0       15 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/missing_stubs
+-rw-r--r--   0        0        0        2 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/@plugins_snapshot.json
+-rw-r--r--   0        0        0     7866 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/__future__.data.json
+-rw-r--r--   0        0        0     1597 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/__future__.meta.json
+-rw-r--r--   0        0        0   180413 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_ast.data.json
+-rw-r--r--   0        0        0     1667 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_ast.meta.json
+-rw-r--r--   0        0        0    52445 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_codecs.data.json
+-rw-r--r--   0        0        0     1707 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_codecs.meta.json
+-rw-r--r--   0        0        0    18272 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_collections_abc.data.json
+-rw-r--r--   0        0        0     1633 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_collections_abc.meta.json
+-rw-r--r--   0        0        0     3170 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_ctypes.data.json
+-rw-r--r--   0        0        0     1632 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_ctypes.meta.json
+-rw-r--r--   0        0        0   113974 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_operator.data.json
+-rw-r--r--   0        0        0     1644 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_operator.meta.json
+-rw-r--r--   0        0        0   136426 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_socket.data.json
+-rw-r--r--   0        0        0     1694 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_socket.meta.json
+-rw-r--r--   0        0        0    23906 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_thread.data.json
+-rw-r--r--   0        0        0     1668 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_thread.meta.json
+-rw-r--r--   0        0        0    13123 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_warnings.data.json
+-rw-r--r--   0        0        0     1571 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_warnings.meta.json
+-rw-r--r--   0        0        0    27354 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_weakref.data.json
+-rw-r--r--   0        0        0     1655 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_weakref.meta.json
+-rw-r--r--   0        0        0    50474 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_weakrefset.data.json
+-rw-r--r--   0        0        0     1661 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_weakrefset.meta.json
+-rw-r--r--   0        0        0    23381 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/abc.data.json
+-rw-r--r--   0        0        0     1621 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/abc.meta.json
+-rw-r--r--   0        0        0    60721 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/array.data.json
+-rw-r--r--   0        0        0     1676 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/array.meta.json
+-rw-r--r--   0        0        0  1130457 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/builtins.data.json
+-rw-r--r--   0        0        0     1758 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/builtins.meta.json
+-rw-r--r--   0        0        0   123362 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/codecs.data.json
+-rw-r--r--   0        0        0     1718 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/codecs.meta.json
+-rw-r--r--   0        0        0   109249 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/contextlib.data.json
+-rw-r--r--   0        0        0     1657 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/contextlib.meta.json
+-rw-r--r--   0        0        0    37812 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/contextvars.data.json
+-rw-r--r--   0        0        0     1661 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/contextvars.meta.json
+-rw-r--r--   0        0        0     5454 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/copy.data.json
+-rw-r--r--   0        0        0     1560 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/copy.meta.json
+-rw-r--r--   0        0        0    11889 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/copyreg.data.json
+-rw-r--r--   0        0        0     1629 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/copyreg.meta.json
+-rw-r--r--   0        0        0    57790 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/dataclasses.data.json
+-rw-r--r--   0        0        0     1672 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/dataclasses.meta.json
+-rw-r--r--   0        0        0   142253 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/datetime.data.json
+-rw-r--r--   0        0        0     1632 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/datetime.meta.json
+-rw-r--r--   0        0        0    62951 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/dis.data.json
+-rw-r--r--   0        0        0     1659 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/dis.meta.json
+-rw-r--r--   0        0        0    90168 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/enum.data.json
+-rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/enum.meta.json
+-rw-r--r--   0        0        0    27321 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/errno.data.json
+-rw-r--r--   0        0        0     1597 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/errno.meta.json
+-rw-r--r--   0        0        0   132112 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/functools.data.json
+-rw-r--r--   0        0        0     1656 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/functools.meta.json
+-rw-r--r--   0        0        0    22433 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/genericpath.data.json
+-rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/genericpath.meta.json
+-rw-r--r--   0        0        0   330933 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/inspect.data.json
+-rw-r--r--   0        0        0     1697 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/inspect.meta.json
+-rw-r--r--   0        0        0    85382 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/io.data.json
+-rw-r--r--   0        0        0     1720 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/io.meta.json
+-rw-r--r--   0        0        0    28812 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/mmap.data.json
+-rw-r--r--   0        0        0     1675 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/mmap.meta.json
+-rw-r--r--   0        0        0     6139 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/opcode.data.json
+-rw-r--r--   0        0        0     1618 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/opcode.meta.json
+-rw-r--r--   0        0        0    49243 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/operator.data.json
+-rw-r--r--   0        0        0     1639 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/operator.meta.json
+-rw-r--r--   0        0        0    87533 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/pathlib.data.json
+-rw-r--r--   0        0        0     1729 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/pathlib.meta.json
+-rw-r--r--   0        0        0    44438 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/pickle.data.json
+-rw-r--r--   0        0        0     1677 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/pickle.meta.json
+-rw-r--r--   0        0        0    75242 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/posixpath.data.json
+-rw-r--r--   0        0        0     1674 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/posixpath.meta.json
+-rw-r--r--   0        0        0    30433 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/queue.data.json
+-rw-r--r--   0        0        0     1619 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/queue.meta.json
+-rw-r--r--   0        0        0   167590 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/re.data.json
+-rw-r--r--   0        0        0     1748 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/re.meta.json
+-rw-r--r--   0        0        0    60475 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/selectors.data.json
+-rw-r--r--   0        0        0     1696 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/selectors.meta.json
+-rw-r--r--   0        0        0   115899 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/socket.data.json
+-rw-r--r--   0        0        0     1738 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/socket.meta.json
+-rw-r--r--   0        0        0    14418 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_compile.data.json
+-rw-r--r--   0        0        0     1619 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_compile.meta.json
+-rw-r--r--   0        0        0    28525 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_constants.data.json
+-rw-r--r--   0        0        0     1631 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_constants.meta.json
+-rw-r--r--   0        0        0    49786 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_parse.data.json
+-rw-r--r--   0        0        0     1674 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sre_parse.meta.json
+-rw-r--r--   0        0        0   191514 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/ssl.data.json
+-rw-r--r--   0        0        0     1737 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/ssl.meta.json
+-rw-r--r--   0        0        0    27793 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/string.data.json
+-rw-r--r--   0        0        0     1659 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/string.meta.json
+-rw-r--r--   0        0        0   162209 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/subprocess.data.json
+-rw-r--r--   0        0        0     1722 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/subprocess.meta.json
+-rw-r--r--   0        0        0   148699 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sys.data.json
+-rw-r--r--   0        0        0     1707 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/sys.meta.json
+-rw-r--r--   0        0        0    64760 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/threading.data.json
+-rw-r--r--   0        0        0     1671 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/threading.meta.json
+-rw-r--r--   0        0        0    43650 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/time.data.json
+-rw-r--r--   0        0        0     1612 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/time.meta.json
+-rw-r--r--   0        0        0    57063 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/traceback.data.json
+-rw-r--r--   0        0        0     1656 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/traceback.meta.json
+-rw-r--r--   0        0        0   239677 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/types.data.json
+-rw-r--r--   0        0        0     1685 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/types.meta.json
+-rw-r--r--   0        0        0   432279 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/typing.data.json
+-rw-r--r--   0        0        0     1736 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/typing.meta.json
+-rw-r--r--   0        0        0    57890 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/typing_extensions.data.json
+-rw-r--r--   0        0        0     1691 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/typing_extensions.meta.json
+-rw-r--r--   0        0        0    33631 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/uuid.data.json
+-rw-r--r--   0        0        0     1677 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/uuid.meta.json
+-rw-r--r--   0        0        0    23834 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/warnings.data.json
+-rw-r--r--   0        0        0     1671 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/warnings.meta.json
+-rw-r--r--   0        0        0   142973 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/weakref.data.json
+-rw-r--r--   0        0        0     1677 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/weakref.meta.json
+-rw-r--r--   0        0        0    89099 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_typeshed/__init__.data.json
+-rw-r--r--   0        0        0     1736 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/_typeshed/__init__.meta.json
+-rw-r--r--   0        0        0    11429 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/__init__.data.json
+-rw-r--r--   0        0        0     2009 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/__init__.meta.json
+-rw-r--r--   0        0        0   104690 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/base_events.data.json
+-rw-r--r--   0        0        0     1903 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/base_events.meta.json
+-rw-r--r--   0        0        0    22647 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/coroutines.data.json
+-rw-r--r--   0        0        0     1663 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/coroutines.meta.json
+-rw-r--r--   0        0        0   202113 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/events.data.json
+-rw-r--r--   0        0        0     1925 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/events.meta.json
+-rw-r--r--   0        0        0     9895 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/exceptions.data.json
+-rw-r--r--   0        0        0     1618 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/exceptions.meta.json
+-rw-r--r--   0        0        0    36843 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/futures.data.json
+-rw-r--r--   0        0        0     1785 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/futures.meta.json
+-rw-r--r--   0        0        0    38458 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/locks.data.json
+-rw-r--r--   0        0        0     1761 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/locks.meta.json
+-rw-r--r--   0        0        0     2604 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/mixins.data.json
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/mixins.meta.json
+-rw-r--r--   0        0        0    17304 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/protocols.data.json
+-rw-r--r--   0        0        0     1697 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/protocols.meta.json
+-rw-r--r--   0        0        0    23140 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/queues.data.json
+-rw-r--r--   0        0        0     1642 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/queues.meta.json
+-rw-r--r--   0        0        0    10870 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/runners.data.json
+-rw-r--r--   0        0        0     1695 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/runners.meta.json
+-rw-r--r--   0        0        0     3868 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/selector_events.data.json
+-rw-r--r--   0        0        0     1680 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/selector_events.meta.json
+-rw-r--r--   0        0        0    36115 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/streams.data.json
+-rw-r--r--   0        0        0     1781 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/streams.meta.json
+-rw-r--r--   0        0        0    24189 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/subprocess.data.json
+-rw-r--r--   0        0        0     1801 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/subprocess.meta.json
+-rw-r--r--   0        0        0     8325 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/taskgroups.data.json
+-rw-r--r--   0        0        0     1707 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/taskgroups.meta.json
+-rw-r--r--   0        0        0   101563 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/tasks.data.json
+-rw-r--r--   0        0        0     1804 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/tasks.meta.json
+-rw-r--r--   0        0        0     5602 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/threads.data.json
+-rw-r--r--   0        0        0     1628 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/threads.meta.json
+-rw-r--r--   0        0        0     9581 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/timeouts.data.json
+-rw-r--r--   0        0        0     1621 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/timeouts.meta.json
+-rw-r--r--   0        0        0    27531 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/transports.data.json
+-rw-r--r--   0        0        0     1669 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/transports.meta.json
+-rw-r--r--   0        0        0    59058 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/unix_events.data.json
+-rw-r--r--   0        0        0     1772 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/asyncio/unix_events.meta.json
+-rw-r--r--   0        0        0   408033 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/collections/__init__.data.json
+-rw-r--r--   0        0        0     1747 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/collections/__init__.meta.json
+-rw-r--r--   0        0        0     3776 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/collections/abc.data.json
+-rw-r--r--   0        0        0     1605 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/collections/abc.meta.json
+-rw-r--r--   0        0        0     1572 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/__init__.data.json
+-rw-r--r--   0        0        0     1580 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/__init__.meta.json
+-rw-r--r--   0        0        0     4587 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/__init__.data.json
+-rw-r--r--   0        0        0     1724 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/__init__.meta.json
+-rw-r--r--   0        0        0    72750 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/_base.data.json
+-rw-r--r--   0        0        0     1717 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/_base.meta.json
+-rw-r--r--   0        0        0    60990 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/process.data.json
+-rw-r--r--   0        0        0     1937 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/process.meta.json
+-rw-r--r--   0        0        0    21941 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/thread.data.json
+-rw-r--r--   0        0        0     1756 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/concurrent/futures/thread.meta.json
+-rw-r--r--   0        0        0   129028 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/ctypes/__init__.data.json
+-rw-r--r--   0        0        0     1713 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/ctypes/__init__.meta.json
+-rw-r--r--   0        0        0     7483 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/__init__.data.json
+-rw-r--r--   0        0        0     1657 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/__init__.meta.json
+-rw-r--r--   0        0        0    12245 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/charset.data.json
+-rw-r--r--   0        0        0     1602 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/charset.meta.json
+-rw-r--r--   0        0        0     7294 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/contentmanager.data.json
+-rw-r--r--   0        0        0     1634 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/contentmanager.meta.json
+-rw-r--r--   0        0        0    25118 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/errors.data.json
+-rw-r--r--   0        0        0     1606 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/errors.meta.json
+-rw-r--r--   0        0        0     9199 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/header.data.json
+-rw-r--r--   0        0        0     1619 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/header.meta.json
+-rw-r--r--   0        0        0    79315 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/message.data.json
+-rw-r--r--   0        0        0     1722 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/message.meta.json
+-rw-r--r--   0        0        0    30902 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/policy.data.json
+-rw-r--r--   0        0        0     1683 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/email/policy.meta.json
+-rw-r--r--   0        0        0     6170 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/__init__.data.json
+-rw-r--r--   0        0        0     1634 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/__init__.meta.json
+-rw-r--r--   0        0        0    70624 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/abc.data.json
+-rw-r--r--   0        0        0     1780 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/abc.meta.json
+-rw-r--r--   0        0        0    64616 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/machinery.data.json
+-rw-r--r--   0        0        0     1769 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/machinery.meta.json
+-rw-r--r--   0        0        0    91164 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/metadata/__init__.data.json
+-rw-r--r--   0        0        0     1778 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/metadata/__init__.meta.json
+-rw-r--r--   0        0        0    11980 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/metadata/_meta.data.json
+-rw-r--r--   0        0        0     1622 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/importlib/metadata/_meta.meta.json
+-rw-r--r--   0        0        0    15424 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/__init__.data.json
+-rw-r--r--   0        0        0     1646 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/__init__.meta.json
+-rw-r--r--   0        0        0    14549 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/decoder.data.json
+-rw-r--r--   0        0        0     1599 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/decoder.meta.json
+-rw-r--r--   0        0        0    10929 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/encoder.data.json
+-rw-r--r--   0        0        0     1608 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/json/encoder.meta.json
+-rw-r--r--   0        0        0   144430 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/logging/__init__.data.json
+-rw-r--r--   0        0        0     1733 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/logging/__init__.meta.json
+-rw-r--r--   0        0        0    31427 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/__init__.data.json
+-rw-r--r--   0        0        0     2003 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/__init__.meta.json
+-rw-r--r--   0        0        0    30686 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/connection.data.json
+-rw-r--r--   0        0        0     1773 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/connection.meta.json
+-rw-r--r--   0        0        0    95638 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/context.data.json
+-rw-r--r--   0        0        0     2152 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/context.meta.json
+-rw-r--r--   0        0        0   148166 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/managers.data.json
+-rw-r--r--   0        0        0     1818 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/managers.meta.json
+-rw-r--r--   0        0        0    51454 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/pool.data.json
+-rw-r--r--   0        0        0     1679 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/pool.meta.json
+-rw-r--r--   0        0        0     9063 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_fork.data.json
+-rw-r--r--   0        0        0     1672 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_fork.meta.json
+-rw-r--r--   0        0        0     5786 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_forkserver.data.json
+-rw-r--r--   0        0        0     1711 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_forkserver.meta.json
+-rw-r--r--   0        0        0     6456 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_spawn_posix.data.json
+-rw-r--r--   0        0        0     1713 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_spawn_posix.meta.json
+-rw-r--r--   0        0        0     2022 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_spawn_win32.data.json
+-rw-r--r--   0        0        0     1686 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/popen_spawn_win32.meta.json
+-rw-r--r--   0        0        0    17731 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/process.data.json
+-rw-r--r--   0        0        0     1649 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/process.meta.json
+-rw-r--r--   0        0        0    19769 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/queues.data.json
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/queues.meta.json
+-rw-r--r--   0        0        0    28927 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/reduction.data.json
+-rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/reduction.meta.json
+-rw-r--r--   0        0        0    29488 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/shared_memory.data.json
+-rw-r--r--   0        0        0     1697 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/shared_memory.meta.json
+-rw-r--r--   0        0        0    67422 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/sharedctypes.data.json
+-rw-r--r--   0        0        0     1762 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/sharedctypes.meta.json
+-rw-r--r--   0        0        0     9867 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/spawn.data.json
+-rw-r--r--   0        0        0     1628 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/spawn.meta.json
+-rw-r--r--   0        0        0    25592 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/synchronize.data.json
+-rw-r--r--   0        0        0     1730 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/synchronize.meta.json
+-rw-r--r--   0        0        0    23597 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/util.data.json
+-rw-r--r--   0        0        0     1686 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/multiprocessing/util.meta.json
+-rw-r--r--   0        0        0   350788 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/os/__init__.data.json
+-rw-r--r--   0        0        0     1772 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/os/__init__.meta.json
+-rw-r--r--   0        0        0     4953 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/os/path.data.json
+-rw-r--r--   0        0        0     1594 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/os/path.meta.json
+-rw-r--r--   0        0        0     6724 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/__init__.data.json
+-rw-r--r--   0        0        0     2192 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/__init__.meta.json
+-rw-r--r--   0        0        0    13427 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_base.data.json
+-rw-r--r--   0        0        0     1740 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_base.meta.json
+-rw-r--r--   0        0        0    32317 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_config.data.json
+-rw-r--r--   0        0        0     1867 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_config.meta.json
+-rw-r--r--   0        0        0     4467 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_frames.data.json
+-rw-r--r--   0        0        0     1700 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_frames.meta.json
+-rw-r--r--   0        0        0     5013 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_generic.data.json
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_generic.meta.json
+-rw-r--r--   0        0        0     5797 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_greenlets.data.json
+-rw-r--r--   0        0        0     1620 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_greenlets.meta.json
+-rw-r--r--   0        0        0    13554 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_log_levels.data.json
+-rw-r--r--   0        0        0     1785 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_log_levels.meta.json
+-rw-r--r--   0        0        0    51708 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_output.data.json
+-rw-r--r--   0        0        0     1720 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_output.meta.json
+-rw-r--r--   0        0        0     4098 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_utils.data.json
+-rw-r--r--   0        0        0     1639 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/_utils.meta.json
+-rw-r--r--   0        0        0    10494 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/contextvars.data.json
+-rw-r--r--   0        0        0     1762 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/contextvars.meta.json
+-rw-r--r--   0        0        0    37593 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/dev.data.json
+-rw-r--r--   0        0        0     1890 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/dev.meta.json
+-rw-r--r--   0        0        0     2258 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/exceptions.data.json
+-rw-r--r--   0        0        0     1589 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/exceptions.meta.json
+-rw-r--r--   0        0        0    70459 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/processors.data.json
+-rw-r--r--   0        0        0     2075 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/processors.meta.json
+-rw-r--r--   0        0        0    93538 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/stdlib.data.json
+-rw-r--r--   0        0        0     1993 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/stdlib.meta.json
+-rw-r--r--   0        0        0    48213 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/testing.data.json
+-rw-r--r--   0        0        0     1679 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/testing.meta.json
+-rw-r--r--   0        0        0    27569 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/threadlocal.data.json
+-rw-r--r--   0        0        0     1914 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/threadlocal.meta.json
+-rw-r--r--   0        0        0    28817 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/tracebacks.data.json
+-rw-r--r--   0        0        0     1810 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/tracebacks.meta.json
+-rw-r--r--   0        0        0    26769 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/twisted.data.json
+-rw-r--r--   0        0        0     1866 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/twisted.meta.json
+-rw-r--r--   0        0        0     3091 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/types.data.json
+-rw-r--r--   0        0        0     1603 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/types.meta.json
+-rw-r--r--   0        0        0    39339 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/typing.data.json
+-rw-r--r--   0        0        0     1649 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog/typing.meta.json
+-rw-r--r--   0        0        0     1522 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/__about__.data.json
+-rw-r--r--   0        0        0     1467 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/__about__.meta.json
+-rw-r--r--   0        0        0     1985 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/__init__.data.json
+-rw-r--r--   0        0        0     1481 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/__init__.meta.json
+-rw-r--r--   0        0        0     2374 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/base.data.json
+-rw-r--r--   0        0        0     1562 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/base.meta.json
+-rw-r--r--   0        0        0    10876 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/errors.data.json
+-rw-r--r--   0        0        0     1567 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/errors.meta.json
+-rw-r--r--   0        0        0    13224 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/processors.data.json
+-rw-r--r--   0        0        0     1674 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/processors.meta.json
+-rw-r--r--   0        0        0     1997 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/types.data.json
+-rw-r--r--   0        0        0     1460 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.mypy_cache/3.11/structlog_gcp/types.meta.json
+-rw-r--r--   0        0        0       37 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.pytest_cache/.gitignore
+-rw-r--r--   0        0        0      191 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.pytest_cache/CACHEDIR.TAG
+-rw-r--r--   0        0        0      302 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.pytest_cache/README.md
+-rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.pytest_cache/v/cache/nodeids
+-rw-r--r--   0        0        0        2 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/.pytest_cache/v/cache/stepwise
+-rw-r--r--   0        0        0    47225 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/docs/errors.png
+-rw-r--r--   0        0        0    45056 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/docs/logs.png
+-rw-r--r--   0        0        0      504 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/examples/cloud-function/.gcloudignore
+-rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/examples/cloud-function/Makefile
+-rw-r--r--   0        0        0     1976 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/examples/cloud-function/main.py
+-rw-r--r--   0        0        0       73 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/examples/cloud-function/requirements.txt
+-rw-r--r--   0        0        0       27 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/.gitignore
+-rw-r--r--   0        0        0    21359 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/coverage_html.js
+-rw-r--r--   0        0        0     5684 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76___init___py.html
+-rw-r--r--   0        0        0    10402 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_base_py.html
+-rw-r--r--   0        0        0    32072 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_errors_py.html
+-rw-r--r--   0        0        0    35226 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_processors_py.html
+-rw-r--r--   0        0        0     6039 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_types_py.html
+-rw-r--r--   0        0        0     1732 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/favicon_32.png
+-rw-r--r--   0        0        0     5742 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/index.html
+-rw-r--r--   0        0        0     9004 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/keybd_closed.png
+-rw-r--r--   0        0        0     9003 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/keybd_open.png
+-rw-r--r--   0        0        0     1137 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/status.json
+-rw-r--r--   0        0        0    12387 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/htmlcov/style.css
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/__about__.py
+-rw-r--r--   0        0        0       88 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/__init__.py
+-rw-r--r--   0        0        0      526 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/base.py
+-rw-r--r--   0        0        0     3879 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/errors.py
+-rw-r--r--   0        0        0     4320 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/processors.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/py.typed
+-rw-r--r--   0        0        0      212 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/structlog_gcp/types.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/tests/__init__.py
+-rw-r--r--   0        0        0      740 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/tests/conftest.py
+-rw-r--r--   0        0        0      822 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/tests/fakes.py
+-rw-r--r--   0        0        0     1568 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/tests/test_log.py
+-rw-r--r--   0        0        0     1094 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/LICENSE
+-rw-r--r--   0        0        0     2678 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/README.md
+-rw-r--r--   0        0        0     1665 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0     3585 2020-02-02 00:00:00.000000 structlog_gcp-0.1.0/PKG-INFO
```

### Comparing `structlog_gcp-0.0.3/.coverage` & `structlog_gcp-0.1.0/.coverage`

 * *Files 5% similar despite different names*

#### sqlite3 {} .dump

```diff
@@ -12,15 +12,15 @@
     unique (key)
     -- Possible keys:
     --  'has_arcs' boolean      -- Is this data recording branches?
     --  'sys_argv' text         -- The coverage command line that recorded the data.
     --  'version' text          -- The version of coverage.py that made the file.
     --  'when' text             -- Datetime when the file was created.
 );
-INSERT INTO meta VALUES('version','7.2.2');
+INSERT INTO meta VALUES('version','7.2.5');
 INSERT INTO meta VALUES('has_arcs','1');
 CREATE TABLE file (
     -- A row per file measured.
     id integer primary key,
     path text,
     unique (path)
 );
@@ -53,193 +53,211 @@
     fromno integer,             -- line number jumped from.
     tono integer,               -- line number jumped to.
     foreign key (file_id) references file (id),
     foreign key (context_id) references context (id),
     unique (file_id, context_id, fromno, tono)
 );
 INSERT INTO arc VALUES(1,1,-1,1);
-INSERT INTO arc VALUES(1,1,1,-1);
+INSERT INTO arc VALUES(1,1,3,-1);
+INSERT INTO arc VALUES(1,1,4,3);
+INSERT INTO arc VALUES(1,1,1,4);
 INSERT INTO arc VALUES(2,1,-1,1);
-INSERT INTO arc VALUES(2,1,1,4);
-INSERT INTO arc VALUES(2,1,-4,4);
-INSERT INTO arc VALUES(2,1,5,8);
-INSERT INTO arc VALUES(2,1,4,5);
-INSERT INTO arc VALUES(2,1,4,-1);
-INSERT INTO arc VALUES(2,1,8,-4);
-INSERT INTO arc VALUES(2,1,-5,6);
-INSERT INTO arc VALUES(2,1,6,-5);
-INSERT INTO arc VALUES(2,1,-8,9);
-INSERT INTO arc VALUES(2,1,9,11);
+INSERT INTO arc VALUES(2,1,1,3);
+INSERT INTO arc VALUES(2,1,3,6);
+INSERT INTO arc VALUES(2,1,-6,7);
+INSERT INTO arc VALUES(2,1,6,-1);
+INSERT INTO arc VALUES(2,1,7,9);
+INSERT INTO arc VALUES(2,1,9,10);
+INSERT INTO arc VALUES(2,1,10,11);
 INSERT INTO arc VALUES(2,1,11,12);
 INSERT INTO arc VALUES(2,1,12,13);
 INSERT INTO arc VALUES(2,1,13,14);
 INSERT INTO arc VALUES(2,1,14,15);
-INSERT INTO arc VALUES(2,1,15,16);
-INSERT INTO arc VALUES(2,1,16,17);
-INSERT INTO arc VALUES(2,1,17,19);
-INSERT INTO arc VALUES(2,1,19,-8);
+INSERT INTO arc VALUES(2,1,15,17);
+INSERT INTO arc VALUES(2,1,17,-6);
 INSERT INTO arc VALUES(3,1,-1,1);
 INSERT INTO arc VALUES(3,1,1,3);
-INSERT INTO arc VALUES(3,1,3,5);
-INSERT INTO arc VALUES(3,1,5,8);
-INSERT INTO arc VALUES(3,1,8,30);
-INSERT INTO arc VALUES(3,1,-8,14);
-INSERT INTO arc VALUES(3,1,14,15);
-INSERT INTO arc VALUES(3,1,15,16);
-INSERT INTO arc VALUES(3,1,16,-8);
-INSERT INTO arc VALUES(3,1,15,20);
-INSERT INTO arc VALUES(3,1,18,25);
-INSERT INTO arc VALUES(3,1,20,21);
-INSERT INTO arc VALUES(3,1,21,18);
-INSERT INTO arc VALUES(3,1,25,27);
-INSERT INTO arc VALUES(3,1,27,-8);
-INSERT INTO arc VALUES(3,1,30,62);
-INSERT INTO arc VALUES(3,1,30,31);
-INSERT INTO arc VALUES(3,1,-30,30);
-INSERT INTO arc VALUES(3,1,31,36);
-INSERT INTO arc VALUES(3,1,36,39);
-INSERT INTO arc VALUES(3,1,-36,37);
-INSERT INTO arc VALUES(3,1,37,-36);
-INSERT INTO arc VALUES(3,1,39,46);
-INSERT INTO arc VALUES(3,1,-39,42);
+INSERT INTO arc VALUES(3,1,3,4);
+INSERT INTO arc VALUES(3,1,4,6);
+INSERT INTO arc VALUES(3,1,6,9);
+INSERT INTO arc VALUES(3,1,9,10);
+INSERT INTO arc VALUES(3,1,10,9);
+INSERT INTO arc VALUES(3,1,9,11);
+INSERT INTO arc VALUES(3,1,11,9);
+INSERT INTO arc VALUES(3,1,9,33);
+INSERT INTO arc VALUES(3,1,-9,17);
+INSERT INTO arc VALUES(3,1,17,18);
+INSERT INTO arc VALUES(3,1,18,19);
+INSERT INTO arc VALUES(3,1,19,-9);
+INSERT INTO arc VALUES(3,1,18,23);
+INSERT INTO arc VALUES(3,1,21,28);
+INSERT INTO arc VALUES(3,1,23,24);
+INSERT INTO arc VALUES(3,1,24,21);
+INSERT INTO arc VALUES(3,1,28,30);
+INSERT INTO arc VALUES(3,1,30,-9);
+INSERT INTO arc VALUES(3,1,-33,33);
+INSERT INTO arc VALUES(3,1,33,34);
+INSERT INTO arc VALUES(3,1,34,39);
+INSERT INTO arc VALUES(3,1,33,63);
+INSERT INTO arc VALUES(3,1,39,42);
+INSERT INTO arc VALUES(3,1,-39,40);
 INSERT INTO arc VALUES(3,1,40,-39);
-INSERT INTO arc VALUES(3,1,42,43);
-INSERT INTO arc VALUES(3,1,43,40);
-INSERT INTO arc VALUES(3,1,46,-30);
-INSERT INTO arc VALUES(3,1,-46,47);
-INSERT INTO arc VALUES(3,1,47,48);
+INSERT INTO arc VALUES(3,1,42,45);
+INSERT INTO arc VALUES(3,1,-42,43);
+INSERT INTO arc VALUES(3,1,43,-42);
+INSERT INTO arc VALUES(3,1,45,46);
+INSERT INTO arc VALUES(3,1,46,45);
+INSERT INTO arc VALUES(3,1,45,47);
+INSERT INTO arc VALUES(3,1,47,45);
+INSERT INTO arc VALUES(3,1,45,-33);
+INSERT INTO arc VALUES(3,1,-45,48);
 INSERT INTO arc VALUES(3,1,48,49);
-INSERT INTO arc VALUES(3,1,49,-46);
-INSERT INTO arc VALUES(3,1,48,51);
-INSERT INTO arc VALUES(3,1,51,52);
-INSERT INTO arc VALUES(3,1,52,55);
-INSERT INTO arc VALUES(3,1,55,56);
+INSERT INTO arc VALUES(3,1,49,50);
+INSERT INTO arc VALUES(3,1,50,-45);
+INSERT INTO arc VALUES(3,1,49,52);
+INSERT INTO arc VALUES(3,1,52,53);
+INSERT INTO arc VALUES(3,1,53,56);
 INSERT INTO arc VALUES(3,1,56,57);
-INSERT INTO arc VALUES(3,1,57,59);
-INSERT INTO arc VALUES(3,1,59,-46);
-INSERT INTO arc VALUES(3,1,-62,62);
-INSERT INTO arc VALUES(3,1,62,63);
-INSERT INTO arc VALUES(3,1,63,68);
-INSERT INTO arc VALUES(3,1,62,-1);
-INSERT INTO arc VALUES(3,1,68,74);
-INSERT INTO arc VALUES(3,1,-68,69);
-INSERT INTO arc VALUES(3,1,69,72);
-INSERT INTO arc VALUES(3,1,72,-68);
-INSERT INTO arc VALUES(3,1,74,77);
-INSERT INTO arc VALUES(3,1,-74,75);
-INSERT INTO arc VALUES(3,1,75,-74);
-INSERT INTO arc VALUES(3,1,77,89);
-INSERT INTO arc VALUES(3,1,-77,78);
-INSERT INTO arc VALUES(3,1,78,83);
-INSERT INTO arc VALUES(3,1,81,87);
-INSERT INTO arc VALUES(3,1,83,84);
-INSERT INTO arc VALUES(3,1,84,81);
-INSERT INTO arc VALUES(3,1,87,-77);
-INSERT INTO arc VALUES(3,1,89,-62);
-INSERT INTO arc VALUES(3,1,-89,90);
-INSERT INTO arc VALUES(3,1,90,92);
-INSERT INTO arc VALUES(3,1,92,93);
-INSERT INTO arc VALUES(3,1,93,-89);
-INSERT INTO arc VALUES(3,1,92,95);
-INSERT INTO arc VALUES(3,1,95,97);
-INSERT INTO arc VALUES(3,1,97,100);
-INSERT INTO arc VALUES(3,1,99,102);
-INSERT INTO arc VALUES(3,1,100,99);
-INSERT INTO arc VALUES(3,1,102,106);
-INSERT INTO arc VALUES(3,1,106,108);
-INSERT INTO arc VALUES(3,1,108,-89);
+INSERT INTO arc VALUES(3,1,57,58);
+INSERT INTO arc VALUES(3,1,58,60);
+INSERT INTO arc VALUES(3,1,60,-45);
+INSERT INTO arc VALUES(3,1,-63,63);
+INSERT INTO arc VALUES(3,1,63,64);
+INSERT INTO arc VALUES(3,1,64,72);
+INSERT INTO arc VALUES(3,1,63,-1);
+INSERT INTO arc VALUES(3,1,72,75);
+INSERT INTO arc VALUES(3,1,-72,73);
+INSERT INTO arc VALUES(3,1,73,-72);
+INSERT INTO arc VALUES(3,1,75,78);
+INSERT INTO arc VALUES(3,1,-75,76);
+INSERT INTO arc VALUES(3,1,76,-75);
+INSERT INTO arc VALUES(3,1,78,88);
+INSERT INTO arc VALUES(3,1,-78,82);
+INSERT INTO arc VALUES(3,1,80,86);
+INSERT INTO arc VALUES(3,1,82,83);
+INSERT INTO arc VALUES(3,1,83,80);
+INSERT INTO arc VALUES(3,1,86,-78);
+INSERT INTO arc VALUES(3,1,88,89);
+INSERT INTO arc VALUES(3,1,89,88);
+INSERT INTO arc VALUES(3,1,88,90);
+INSERT INTO arc VALUES(3,1,90,88);
+INSERT INTO arc VALUES(3,1,88,-63);
+INSERT INTO arc VALUES(3,1,-88,91);
+INSERT INTO arc VALUES(3,1,91,93);
+INSERT INTO arc VALUES(3,1,93,94);
+INSERT INTO arc VALUES(3,1,94,-88);
+INSERT INTO arc VALUES(3,1,93,98);
+INSERT INTO arc VALUES(3,1,98,97);
+INSERT INTO arc VALUES(3,1,97,101);
+INSERT INTO arc VALUES(3,1,101,102);
+INSERT INTO arc VALUES(3,1,102,103);
+INSERT INTO arc VALUES(3,1,103,105);
+INSERT INTO arc VALUES(3,1,105,-88);
 INSERT INTO arc VALUES(4,1,-1,2);
 INSERT INTO arc VALUES(4,1,2,1);
 INSERT INTO arc VALUES(4,1,1,5);
 INSERT INTO arc VALUES(4,1,5,7);
 INSERT INTO arc VALUES(4,1,7,-1);
-INSERT INTO arc VALUES(5,1,-1,5);
-INSERT INTO arc VALUES(5,1,5,7);
-INSERT INTO arc VALUES(5,1,7,10);
-INSERT INTO arc VALUES(5,1,-10,10);
-INSERT INTO arc VALUES(5,1,10,11);
-INSERT INTO arc VALUES(5,1,11,13);
-INSERT INTO arc VALUES(5,1,13,22);
-INSERT INTO arc VALUES(5,1,10,32);
-INSERT INTO arc VALUES(5,1,-13,16);
-INSERT INTO arc VALUES(5,1,16,18);
-INSERT INTO arc VALUES(5,1,14,-13);
-INSERT INTO arc VALUES(5,1,18,19);
-INSERT INTO arc VALUES(5,1,19,14);
-INSERT INTO arc VALUES(5,1,22,-10);
-INSERT INTO arc VALUES(5,1,-22,24);
+INSERT INTO arc VALUES(5,1,-1,6);
+INSERT INTO arc VALUES(5,1,6,7);
+INSERT INTO arc VALUES(5,1,7,9);
+INSERT INTO arc VALUES(5,1,9,12);
+INSERT INTO arc VALUES(5,1,-12,12);
+INSERT INTO arc VALUES(5,1,12,13);
+INSERT INTO arc VALUES(5,1,13,15);
+INSERT INTO arc VALUES(5,1,15,24);
+INSERT INTO arc VALUES(5,1,12,36);
+INSERT INTO arc VALUES(5,1,-15,18);
+INSERT INTO arc VALUES(5,1,18,20);
+INSERT INTO arc VALUES(5,1,16,-15);
+INSERT INTO arc VALUES(5,1,20,21);
+INSERT INTO arc VALUES(5,1,21,16);
+INSERT INTO arc VALUES(5,1,24,-12);
 INSERT INTO arc VALUES(5,1,24,25);
-INSERT INTO arc VALUES(5,1,25,23);
-INSERT INTO arc VALUES(5,1,23,28);
+INSERT INTO arc VALUES(5,1,25,24);
+INSERT INTO arc VALUES(5,1,26,24);
+INSERT INTO arc VALUES(5,1,24,26);
+INSERT INTO arc VALUES(5,1,-24,28);
 INSERT INTO arc VALUES(5,1,28,29);
-INSERT INTO arc VALUES(5,1,29,-22);
-INSERT INTO arc VALUES(5,1,-32,32);
+INSERT INTO arc VALUES(5,1,29,27);
+INSERT INTO arc VALUES(5,1,27,32);
 INSERT INTO arc VALUES(5,1,32,33);
-INSERT INTO arc VALUES(5,1,33,35);
-INSERT INTO arc VALUES(5,1,35,41);
-INSERT INTO arc VALUES(5,1,32,50);
-INSERT INTO arc VALUES(5,1,-35,37);
-INSERT INTO arc VALUES(5,1,37,38);
-INSERT INTO arc VALUES(5,1,38,36);
-INSERT INTO arc VALUES(5,1,36,-35);
-INSERT INTO arc VALUES(5,1,41,-32);
-INSERT INTO arc VALUES(5,1,-41,42);
+INSERT INTO arc VALUES(5,1,33,-24);
+INSERT INTO arc VALUES(5,1,-36,36);
+INSERT INTO arc VALUES(5,1,36,37);
+INSERT INTO arc VALUES(5,1,37,39);
+INSERT INTO arc VALUES(5,1,39,42);
+INSERT INTO arc VALUES(5,1,36,53);
+INSERT INTO arc VALUES(5,1,-39,40);
+INSERT INTO arc VALUES(5,1,42,43);
+INSERT INTO arc VALUES(5,1,43,42);
 INSERT INTO arc VALUES(5,1,42,44);
-INSERT INTO arc VALUES(5,1,44,47);
-INSERT INTO arc VALUES(5,1,44,45);
+INSERT INTO arc VALUES(5,1,44,42);
+INSERT INTO arc VALUES(5,1,42,-36);
+INSERT INTO arc VALUES(5,1,40,-39);
+INSERT INTO arc VALUES(5,1,-42,45);
 INSERT INTO arc VALUES(5,1,45,47);
-INSERT INTO arc VALUES(5,1,47,-41);
-INSERT INTO arc VALUES(5,1,-50,50);
-INSERT INTO arc VALUES(5,1,50,51);
-INSERT INTO arc VALUES(5,1,51,53);
-INSERT INTO arc VALUES(5,1,53,70);
-INSERT INTO arc VALUES(5,1,50,90);
-INSERT INTO arc VALUES(5,1,-53,54);
-INSERT INTO arc VALUES(5,1,54,58);
-INSERT INTO arc VALUES(5,1,57,-53);
-INSERT INTO arc VALUES(5,1,58,59);
-INSERT INTO arc VALUES(5,1,59,60);
-INSERT INTO arc VALUES(5,1,60,62);
+INSERT INTO arc VALUES(5,1,47,50);
+INSERT INTO arc VALUES(5,1,50,-42);
+INSERT INTO arc VALUES(5,1,47,48);
+INSERT INTO arc VALUES(5,1,-53,53);
+INSERT INTO arc VALUES(5,1,53,54);
+INSERT INTO arc VALUES(5,1,54,56);
+INSERT INTO arc VALUES(5,1,56,73);
+INSERT INTO arc VALUES(5,1,53,92);
+INSERT INTO arc VALUES(5,1,-56,57);
+INSERT INTO arc VALUES(5,1,57,61);
+INSERT INTO arc VALUES(5,1,60,-56);
+INSERT INTO arc VALUES(5,1,61,62);
 INSERT INTO arc VALUES(5,1,62,63);
-INSERT INTO arc VALUES(5,1,63,64);
-INSERT INTO arc VALUES(5,1,64,65);
-INSERT INTO arc VALUES(5,1,65,57);
-INSERT INTO arc VALUES(5,1,70,77);
-INSERT INTO arc VALUES(5,1,-70,73);
-INSERT INTO arc VALUES(5,1,71,-70);
-INSERT INTO arc VALUES(5,1,73,74);
-INSERT INTO arc VALUES(5,1,74,71);
-INSERT INTO arc VALUES(5,1,77,-50);
-INSERT INTO arc VALUES(5,1,-77,83);
-INSERT INTO arc VALUES(5,1,83,84);
-INSERT INTO arc VALUES(5,1,84,86);
-INSERT INTO arc VALUES(5,1,86,87);
-INSERT INTO arc VALUES(5,1,87,-77);
-INSERT INTO arc VALUES(5,1,-90,90);
-INSERT INTO arc VALUES(5,1,90,91);
-INSERT INTO arc VALUES(5,1,91,93);
-INSERT INTO arc VALUES(5,1,93,105);
-INSERT INTO arc VALUES(5,1,90,-1);
-INSERT INTO arc VALUES(5,1,-93,95);
-INSERT INTO arc VALUES(5,1,95,97);
-INSERT INTO arc VALUES(5,1,97,98);
-INSERT INTO arc VALUES(5,1,98,99);
+INSERT INTO arc VALUES(5,1,63,65);
+INSERT INTO arc VALUES(5,1,65,66);
+INSERT INTO arc VALUES(5,1,66,67);
+INSERT INTO arc VALUES(5,1,67,68);
+INSERT INTO arc VALUES(5,1,68,60);
+INSERT INTO arc VALUES(5,1,73,77);
+INSERT INTO arc VALUES(5,1,-73,75);
+INSERT INTO arc VALUES(5,1,75,-73);
+INSERT INTO arc VALUES(5,1,77,78);
+INSERT INTO arc VALUES(5,1,78,77);
+INSERT INTO arc VALUES(5,1,77,79);
+INSERT INTO arc VALUES(5,1,79,77);
+INSERT INTO arc VALUES(5,1,77,-53);
+INSERT INTO arc VALUES(5,1,-77,85);
+INSERT INTO arc VALUES(5,1,85,86);
+INSERT INTO arc VALUES(5,1,86,88);
+INSERT INTO arc VALUES(5,1,88,89);
+INSERT INTO arc VALUES(5,1,89,-77);
+INSERT INTO arc VALUES(5,1,-92,92);
+INSERT INTO arc VALUES(5,1,92,93);
+INSERT INTO arc VALUES(5,1,93,95);
+INSERT INTO arc VALUES(5,1,95,107);
+INSERT INTO arc VALUES(5,1,92,-1);
+INSERT INTO arc VALUES(5,1,-95,97);
+INSERT INTO arc VALUES(5,1,97,99);
 INSERT INTO arc VALUES(5,1,99,100);
-INSERT INTO arc VALUES(5,1,100,96);
-INSERT INTO arc VALUES(5,1,96,95);
-INSERT INTO arc VALUES(5,1,95,103);
-INSERT INTO arc VALUES(5,1,103,-93);
-INSERT INTO arc VALUES(5,1,105,-90);
-INSERT INTO arc VALUES(5,1,-105,107);
+INSERT INTO arc VALUES(5,1,100,101);
+INSERT INTO arc VALUES(5,1,101,102);
+INSERT INTO arc VALUES(5,1,102,98);
+INSERT INTO arc VALUES(5,1,98,97);
+INSERT INTO arc VALUES(5,1,97,105);
+INSERT INTO arc VALUES(5,1,105,-95);
 INSERT INTO arc VALUES(5,1,107,108);
-INSERT INTO arc VALUES(5,1,108,109);
-INSERT INTO arc VALUES(5,1,109,106);
-INSERT INTO arc VALUES(5,1,106,112);
-INSERT INTO arc VALUES(5,1,112,114);
-INSERT INTO arc VALUES(5,1,114,-105);
+INSERT INTO arc VALUES(5,1,108,107);
+INSERT INTO arc VALUES(5,1,107,109);
+INSERT INTO arc VALUES(5,1,109,107);
+INSERT INTO arc VALUES(5,1,107,-92);
+INSERT INTO arc VALUES(5,1,-107,111);
+INSERT INTO arc VALUES(5,1,111,112);
+INSERT INTO arc VALUES(5,1,112,113);
+INSERT INTO arc VALUES(5,1,113,110);
+INSERT INTO arc VALUES(5,1,110,116);
+INSERT INTO arc VALUES(5,1,116,118);
+INSERT INTO arc VALUES(5,1,118,-107);
+INSERT INTO arc VALUES(5,1,48,50);
 CREATE TABLE tracer (
     -- A row per file indicating the tracer used for that file.
     file_id integer primary key,
     tracer text,
     foreign key (file_id) references file (id)
 );
 INSERT INTO tracer VALUES(1,'');
```

### Comparing `structlog_gcp-0.0.3/.github/workflows/build-test-release.yml` & `structlog_gcp-0.1.0/.github/workflows/build-test-release.yml`

 * *Files 15% similar despite different names*

```diff
@@ -1,14 +1,10 @@
 name: Build & maybe upload PyPI package
 
 on:
-  push:
-    branches:
-      - main
-
   pull_request:
     branches:
       - main
 
   release:
     types:
       - published
@@ -23,25 +19,37 @@
     name: Build & verify package
     runs-on: ubuntu-latest
 
     steps:
       - name: Checkout
         uses: actions/checkout@v3
 
-      - name: Setup Poetry
-        run: pipx install hatch
-
       - name: Setup Python
         uses: actions/setup-python@v4
         with:
           python-version: "3.11"
 
+      - name: Setup Hatch
+        run: pipx install hatch
+
       - name: Test
         run: hatch run pytest --color=yes
 
+      - name: mypy
+        run: hatch run mypy structlog_gcp
+
+      - name: flake8
+        run: hatch run flake8 structlog_gcp
+
+      - name: black
+        run: hatch run black --check --diff structlog_gcp
+
+      - name: isort
+        run: hatch run isort --check --diff structlog_gcp
+
       - name: Build
         run: hatch build --clean
 
       - name: Upload package
         uses: actions/upload-artifact@v3
         with:
           name: Packages
```

### Comparing `structlog_gcp-0.0.3/docs/errors.png` & `structlog_gcp-0.1.0/docs/errors.png`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/docs/logs.png` & `structlog_gcp-0.1.0/docs/logs.png`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/examples/cloud-function/main.py` & `structlog_gcp-0.1.0/examples/cloud-function/main.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 import functions_framework
 import google.cloud.error_reporting
 import google.cloud.logging
 import structlog
 
 import structlog_gcp
 
-gcp_logs = structlog_gcp.StructlogGCP()
-structlog.configure(processors=gcp_logs.build_processors())
+processors = structlog_gcp.build_processors()
+structlog.configure(processors=processors)
 
 
 @functions_framework.http
 def test_func1(request):
     """Test the logging framework.
 
     * `GET` the deployed URL to trigger the `structlog-gcp` behavior
```

### Comparing `structlog_gcp-0.0.3/htmlcov/coverage_html.js` & `structlog_gcp-0.1.0/htmlcov/coverage_html.js`

 * *Files 3% similar despite different names*

#### js-beautify {}

```diff
@@ -221,15 +221,15 @@
 // -- pyfile stuff --
 
 coverage.LINE_FILTERS_STORAGE = "COVERAGE_LINE_FILTERS";
 
 coverage.pyfile_ready = function() {
     // If we're directed to a particular line number, highlight the line.
     var frag = location.hash;
-    if (frag.length > 2 && frag[1] === 't') {
+    if (frag.length > 2 && frag[1] === "t") {
         document.querySelector(frag).closest(".n").classList.add("highlight");
         coverage.set_sel(parseInt(frag.substr(2), 10));
     } else {
         coverage.set_sel(0);
     }
 
     on_click(".button_toggle_run", coverage.toggle_lines);
@@ -268,14 +268,18 @@
         coverage.set_line_visibilty(cls, coverage.filters[cls]);
     }
 
     coverage.assign_shortkeys();
     coverage.init_scroll_markers();
     coverage.wire_up_sticky_header();
 
+    document.querySelectorAll("[id^=ctxs]").forEach(
+        cbox => cbox.addEventListener("click", coverage.expand_contexts)
+    );
+
     // Rebuild scroll markers when the window height changes.
     window.addEventListener("resize", coverage.build_scroll_markers);
 };
 
 coverage.toggle_lines = function(event) {
     const btn = event.target.closest("button");
     const category = btn.value
@@ -540,38 +544,38 @@
         top: to_pos,
         behavior: "smooth"
     });
 };
 
 coverage.init_scroll_markers = function() {
     // Init some variables
-    coverage.lines_len = document.querySelectorAll('#source > p').length;
+    coverage.lines_len = document.querySelectorAll("#source > p").length;
 
     // Build html
     coverage.build_scroll_markers();
 };
 
 coverage.build_scroll_markers = function() {
-    const temp_scroll_marker = document.getElementById('scroll_marker')
+    const temp_scroll_marker = document.getElementById("scroll_marker")
     if (temp_scroll_marker) temp_scroll_marker.remove();
     // Don't build markers if the window has no scroll bar.
     if (document.body.scrollHeight <= window.innerHeight) {
         return;
     }
 
     const marker_scale = window.innerHeight / document.body.scrollHeight;
     const line_height = Math.min(Math.max(3, window.innerHeight / coverage.lines_len), 10);
 
     let previous_line = -99,
         last_mark, last_top;
 
     const scroll_marker = document.createElement("div");
     scroll_marker.id = "scroll_marker";
-    document.getElementById('source').querySelectorAll(
-        'p.show_run, p.show_mis, p.show_exc, p.show_exc, p.show_par'
+    document.getElementById("source").querySelectorAll(
+        "p.show_run, p.show_mis, p.show_exc, p.show_exc, p.show_par"
     ).forEach(element => {
         const line_top = Math.floor(element.offsetTop * marker_scale);
         const line_number = parseInt(element.querySelector(".n a").id.substr(1));
 
         if (line_number === previous_line + 1) {
             // If this solid missed block just make previous mark higher.
             last_mark.style.height = `${line_top + line_height - last_top}px`;
@@ -590,32 +594,48 @@
     });
 
     // Append last to prevent layout calculation
     document.body.append(scroll_marker);
 };
 
 coverage.wire_up_sticky_header = function() {
-    const header = document.querySelector('header');
+    const header = document.querySelector("header");
     const header_bottom = (
-        header.querySelector('.content h2').getBoundingClientRect().top -
+        header.querySelector(".content h2").getBoundingClientRect().top -
         header.getBoundingClientRect().top
     );
 
     function updateHeader() {
         if (window.scrollY > header_bottom) {
-            header.classList.add('sticky');
+            header.classList.add("sticky");
         } else {
-            header.classList.remove('sticky');
+            header.classList.remove("sticky");
         }
     }
 
-    window.addEventListener('scroll', updateHeader);
+    window.addEventListener("scroll", updateHeader);
     updateHeader();
 };
 
+coverage.expand_contexts = function(e) {
+    var ctxs = e.target.parentNode.querySelector(".ctxs");
+
+    if (!ctxs.classList.contains("expanded")) {
+        var ctxs_text = ctxs.textContent;
+        var width = Number(ctxs_text[0]);
+        ctxs.textContent = "";
+        for (var i = 1; i < ctxs_text.length; i += width) {
+            key = ctxs_text.substring(i, i + width).trim();
+            ctxs.appendChild(document.createTextNode(contexts[key]));
+            ctxs.appendChild(document.createElement("br"));
+        }
+        ctxs.classList.add("expanded");
+    }
+};
+
 document.addEventListener("DOMContentLoaded", () => {
     if (document.body.classList.contains("indexfile")) {
         coverage.index_ready();
     } else {
         coverage.pyfile_ready();
     }
 });
```

### Comparing `structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_base_py.html` & `structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_base_py.html`

 * *Files 2% similar despite different names*

```diff
@@ -51,68 +51,66 @@
                     <p>
                         <kbd>?</kbd> &nbsp; show/hide this help
                     </p>
                 </div>
             </div>
         </aside>
         <h2>
-            <span class="text">14 statements &nbsp;</span>
-            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">14<span class="text"> run</span></button>
+            <span class="text">12 statements &nbsp;</span>
+            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">12<span class="text"> run</span></button>
             <button type="button" class="mis show_mis button_toggle_mis" value="mis" data-shortcut="m" title="Toggle lines missing">0<span class="text"> missing</span></button>
             <button type="button" class="exc show_exc button_toggle_exc" value="exc" data-shortcut="x" title="Toggle lines excluded">0<span class="text"> excluded</span></button>
             <button type="button" class="par run show_par button_toggle_par" value="par" data-shortcut="p" title="Toggle lines partially run">0<span class="text"> partial</span></button>
         </h2>
         <p class="text">
             <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76___init___py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
             <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
         <aside class="hidden">
             <button type="button" class="button_next_chunk" data-shortcut="j"/>
             <button type="button" class="button_prev_chunk" data-shortcut="k"/>
             <button type="button" class="button_top_of_page" data-shortcut="0"/>
             <button type="button" class="button_first_chunk" data-shortcut="1"/>
             <button type="button" class="button_prev_file" data-shortcut="["/>
             <button type="button" class="button_next_file" data-shortcut="]"/>
             <button type="button" class="button_to_index" data-shortcut="u"/>
             <button type="button" class="button_show_hide_help" data-shortcut="?"/>
         </aside>
     </div>
 </header>
 <main id="source">
-    <p class="run"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="key">from</span> <span class="op">.</span> <span class="key">import</span> <span class="nam">errors</span><span class="op">,</span> <span class="nam">processors</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="key">from</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">typing</span> <span class="key">import</span> <span class="nam">Processor</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t2" href="#t2">2</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t4" href="#t4">4</a></span><span class="t"><span class="key">class</span> <span class="nam">StructlogGCP</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t">        <span class="key">pass</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t8" href="#t8">8</a></span><span class="t">    <span class="key">def</span> <span class="nam">build_processors</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t">        <span class="nam">procs</span> <span class="op">=</span> <span class="op">[</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t10" href="#t10">10</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CoreCloudLogging</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">LogSeverity</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CodeLocation</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">ReportException</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">ReportError</span><span class="op">(</span><span class="op">[</span><span class="str">"CRITICAL"</span><span class="op">]</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">append</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">add_service_context</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">        <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">FormatAsCloudLogging</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t18" href="#t18">18</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t19" href="#t19">19</a></span><span class="t">        <span class="key">return</span> <span class="nam">procs</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t"><span class="key">from</span> <span class="op">.</span> <span class="key">import</span> <span class="nam">errors</span><span class="op">,</span> <span class="nam">processors</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t4" href="#t4">4</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t"><span class="key">def</span> <span class="nam">build_processors</span><span class="op">(</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t">    <span class="nam">procs</span> <span class="op">=</span> <span class="op">[</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t8" href="#t8">8</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CoreCloudLogging</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t10" href="#t10">10</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">LogSeverity</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CodeLocation</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">ReportException</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">ReportError</span><span class="op">(</span><span class="op">[</span><span class="str">"CRITICAL"</span><span class="op">]</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">append</span><span class="op">(</span><span class="nam">errors</span><span class="op">.</span><span class="nam">add_service_context</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t">    <span class="nam">procs</span><span class="op">.</span><span class="nam">extend</span><span class="op">(</span><span class="nam">processors</span><span class="op">.</span><span class="nam">FormatAsCloudLogging</span><span class="op">(</span><span class="op">)</span><span class="op">.</span><span class="nam">setup</span><span class="op">(</span><span class="op">)</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">    <span class="key">return</span> <span class="nam">procs</span>&nbsp;</span><span class="r"></span></p>
 </main>
 <footer>
     <div class="content">
         <p>
             <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76___init___py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
             <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
 </footer>
 </body>
 </html>
```

#### html2text {}

```diff
@@ -5,34 +5,32 @@
 r m x p   toggle line displays
 j k   next/prev highlighted chunk
 0   (zero) top of page
 1   (one) first highlighted chunk
 [ ]   prev/next file
 u   up to the index
 ?   show/hide this help
-***** 14 statements   14 run 0 missing 0 excluded 0 partial *****
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+***** 12 statements   12 run 0 missing 0 excluded 0 partial *****
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
 
 
-1from . import errors, processors 
+1from structlog.typing import Processor 
 2 
-3 
-4class StructlogGCP: 
-5 def __init__(self): 
-6 pass 
-7 
-8 def build_processors(self): 
-9 procs = [] 
-10 
-11 procs.extend(processors.CoreCloudLogging().setup()) 
-12 procs.extend(processors.LogSeverity().setup()) 
-13 procs.extend(processors.CodeLocation().setup()) 
-14 procs.extend(errors.ReportException().setup()) 
-15 procs.extend(errors.ReportError(["CRITICAL"]).setup()) 
-16 procs.append(errors.add_service_context) 
-17 procs.extend(processors.FormatAsCloudLogging().setup()) 
-18 
-19 return procs 
+3from . import errors, processors 
+4 
+5 
+6def build_processors() -> list[Processor]: 
+7 procs = [] 
+8 
+9 procs.extend(processors.CoreCloudLogging().setup()) 
+10 procs.extend(processors.LogSeverity().setup()) 
+11 procs.extend(processors.CodeLocation().setup()) 
+12 procs.extend(errors.ReportException().setup()) 
+13 procs.extend(errors.ReportError(["CRITICAL"]).setup()) 
+14 procs.append(errors.add_service_context) 
+15 procs.extend(processors.FormatAsCloudLogging().setup()) 
+16 
+17 return procs 
 
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
```

### Comparing `structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_errors_py.html` & `structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_processors_py.html`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 <!DOCTYPE html>
 <html>
 <head>
     <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
-    <title>Coverage for structlog_gcp/errors.py: 93%</title>
+    <title>Coverage for structlog_gcp/processors.py: 100%</title>
     <link rel="icon" sizes="32x32" href="favicon_32.png">
     <link rel="stylesheet" href="style.css" type="text/css">
     <script type="text/javascript" src="coverage_html.js" defer></script>
 </head>
 <body class="pyfile">
 <header>
     <div class="content">
         <h1>
-            <span class="text">Coverage for </span><b>structlog_gcp/errors.py</b>:
-            <span class="pc_cov">93%</span>
+            <span class="text">Coverage for </span><b>structlog_gcp/processors.py</b>:
+            <span class="pc_cov">100%</span>
         </h1>
         <aside id="help_panel_wrapper">
             <input id="help_panel_state" type="checkbox">
             <label for="help_panel_state">
                 <img id="keyboard_icon" src="keybd_closed.png" alt="Show/hide keyboard shortcuts" />
             </label>
             <div id="help_panel">
@@ -51,157 +51,167 @@
                     <p>
                         <kbd>?</kbd> &nbsp; show/hide this help
                     </p>
                 </div>
             </div>
         </aside>
         <h2>
-            <span class="text">47 statements &nbsp;</span>
-            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">45<span class="text"> run</span></button>
-            <button type="button" class="mis show_mis button_toggle_mis" value="mis" data-shortcut="m" title="Toggle lines missing">2<span class="text"> missing</span></button>
+            <span class="text">37 statements &nbsp;</span>
+            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">37<span class="text"> run</span></button>
+            <button type="button" class="mis show_mis button_toggle_mis" value="mis" data-shortcut="m" title="Toggle lines missing">0<span class="text"> missing</span></button>
             <button type="button" class="exc show_exc button_toggle_exc" value="exc" data-shortcut="x" title="Toggle lines excluded">0<span class="text"> excluded</span></button>
-            <button type="button" class="par run show_par button_toggle_par" value="par" data-shortcut="p" title="Toggle lines partially run">2<span class="text"> partial</span></button>
+            <button type="button" class="par run show_par button_toggle_par" value="par" data-shortcut="p" title="Toggle lines partially run">0<span class="text"> partial</span></button>
         </h2>
         <p class="text">
-            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_base_py.html">&#xab; prev</a> &nbsp; &nbsp;
+            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
-            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xbb; next</a>
+            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_types_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
         <aside class="hidden">
             <button type="button" class="button_next_chunk" data-shortcut="j"/>
             <button type="button" class="button_prev_chunk" data-shortcut="k"/>
             <button type="button" class="button_top_of_page" data-shortcut="0"/>
             <button type="button" class="button_first_chunk" data-shortcut="1"/>
             <button type="button" class="button_prev_file" data-shortcut="["/>
             <button type="button" class="button_next_file" data-shortcut="]"/>
             <button type="button" class="button_to_index" data-shortcut="u"/>
             <button type="button" class="button_show_hide_help" data-shortcut="?"/>
         </aside>
     </div>
 </header>
 <main id="source">
-    <p class="run"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="key">import</span> <span class="nam">os</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t2" href="#t2">2</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t"><span class="key">import</span> <span class="nam">structlog</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="com"># https://cloud.google.com/functions/docs/monitoring/logging#writing_structured_logs</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t2" href="#t2">2</a></span><span class="t"><span class="com"># https://cloud.google.com/logging/docs/agent/logging/configuration#process-payload</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t"><span class="com"># https://cloud.google.com/logging/docs/structured-logging#special-payload-fields</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t4" href="#t4">4</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t"><span class="key">from</span> <span class="op">.</span><span class="nam">types</span> <span class="key">import</span> <span class="nam">CLOUD_LOGGING_KEY</span><span class="op">,</span> <span class="nam">ERROR_EVENT_TYPE</span><span class="op">,</span> <span class="nam">SOURCE_LOCATION_KEY</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t8" href="#t8">8</a></span><span class="t"><span class="key">def</span> <span class="nam">add_service_context</span><span class="op">(</span><span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t">    <span class="str">"""Add a service context in which an error has occurred.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t"><span class="key">import</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t"><span class="key">from</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">typing</span> <span class="key">import</span> <span class="nam">EventDict</span><span class="op">,</span> <span class="nam">Processor</span><span class="op">,</span> <span class="nam">WrappedLogger</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t8" href="#t8">8</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t"><span class="key">from</span> <span class="op">.</span><span class="nam">types</span> <span class="key">import</span> <span class="nam">CLOUD_LOGGING_KEY</span><span class="op">,</span> <span class="nam">SOURCE_LOCATION_KEY</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t10" href="#t10">10</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t"><span class="str">    This is part of the Error Reporting API, so it's only added when an error happens.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t"><span class="str">    """</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t">    <span class="nam">event_type</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"@type"</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t">    <span class="key">if</span> <span class="nam">event_type</span> <span class="op">!=</span> <span class="nam">ERROR_EVENT_TYPE</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t18" href="#t18">18</a></span><span class="t">    <span class="nam">service_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t19" href="#t19">19</a></span><span class="t">        <span class="com"># https://cloud.google.com/functions/docs/configuring/env-var#runtime_environment_variables_set_automatically</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t20" href="#t20">20</a></span><span class="t">        <span class="str">"service"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_SERVICE"</span><span class="op">,</span> <span class="str">"unknown service"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t21" href="#t21">21</a></span><span class="t">        <span class="str">"version"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_REVISION"</span><span class="op">,</span> <span class="str">"unknown version"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t22" href="#t22">22</a></span><span class="t">    <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t"><span class="key">class</span> <span class="nam">CoreCloudLogging</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">    <span class="str">"""Initialize the Google Cloud Logging event message"""</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">            <span class="com"># If some value is in bytes, decode it to a unicode str.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t18" href="#t18">18</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">UnicodeDecoder</span><span class="op">(</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t19" href="#t19">19</a></span><span class="t">            <span class="com"># Add a timestamp in ISO 8601 format.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t20" href="#t20">20</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">TimeStamper</span><span class="op">(</span><span class="nam">fmt</span><span class="op">=</span><span class="str">"iso"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t21" href="#t21">21</a></span><span class="t">            <span class="nam">self</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t22" href="#t22">22</a></span><span class="t">        <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t23" href="#t23">23</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t24" href="#t24">24</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ServiceContext</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t25" href="#t25">25</a></span><span class="t">    <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"serviceContext"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">service_context</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t26" href="#t26">26</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t27" href="#t27">27</a></span><span class="t">    <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t28" href="#t28">28</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t29" href="#t29">29</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t30" href="#t30">30</a></span><span class="t"><span class="key">class</span> <span class="nam">ReportException</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t31" href="#t31">31</a></span><span class="t">    <span class="str">"""Transform exception into a Google Cloud Error Reporting event."""</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t32" href="#t32">32</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t33" href="#t33">33</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t34" href="#t34">34</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t24" href="#t24">24</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t25" href="#t25">25</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t26" href="#t26">26</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t27" href="#t27">27</a></span><span class="t">        <span class="nam">value</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t28" href="#t28">28</a></span><span class="t">            <span class="str">"message"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"event"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t29" href="#t29">29</a></span><span class="t">            <span class="str">"time"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"timestamp"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t30" href="#t30">30</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t31" href="#t31">31</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t32" href="#t32">32</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span> <span class="op">=</span> <span class="nam">value</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t33" href="#t33">33</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t34" href="#t34">34</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t35" href="#t35">35</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t36" href="#t36">36</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">log_level</span><span class="op">=</span><span class="str">"CRITICAL"</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t37" href="#t37">37</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">log_level</span> <span class="op">=</span> <span class="nam">log_level</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t36" href="#t36">36</a></span><span class="t"><span class="key">class</span> <span class="nam">FormatAsCloudLogging</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t37" href="#t37">37</a></span><span class="t">    <span class="str">"""Finalize the Google Cloud Logging event message and replace the logging event"""</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t38" href="#t38">38</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t39" href="#t39">39</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t40" href="#t40">40</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t41" href="#t41">41</a></span><span class="t">            <span class="com"># structlog.processors.ExceptionRenderer(self.format_exception),</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t42" href="#t42">42</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">format_exc_info</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t43" href="#t43">43</a></span><span class="t">            <span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t44" href="#t44">44</a></span><span class="t">        <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t45" href="#t45">45</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t46" href="#t46">46</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t47" href="#t47">47</a></span><span class="t">        <span class="nam">exception</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"exception"</span><span class="op">,</span> <span class="key">None</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t48" href="#t48">48</a></span><span class="t">        <span class="key">if</span> <span class="nam">exception</span> <span class="key">is</span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t49" href="#t49">49</a></span><span class="t">            <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t50" href="#t50">50</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t51" href="#t51">51</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"@type"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">ERROR_EVENT_TYPE</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t52" href="#t52">52</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">log_level</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t53" href="#t53">53</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t54" href="#t54">54</a></span><span class="t">        <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t55" href="#t55">55</a></span><span class="t">        <span class="nam">message</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"message"</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t56" href="#t56">56</a></span><span class="t">        <span class="nam">error_message</span> <span class="op">=</span> <span class="str">f"{message}\n{exception}"</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t57" href="#t57">57</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"stack_trace"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">error_message</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t39" href="#t39">39</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t40" href="#t40">40</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">self</span><span class="op">,</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">JSONRenderer</span><span class="op">(</span><span class="op">)</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t41" href="#t41">41</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t42" href="#t42">42</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t43" href="#t43">43</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t44" href="#t44">44</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t45" href="#t45">45</a></span><span class="t">        <span class="nam">event</span><span class="op">:</span> <span class="nam">EventDict</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t46" href="#t46">46</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t47" href="#t47">47</a></span><span class="t">        <span class="key">if</span> <span class="nam">event_dict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t48" href="#t48">48</a></span><span class="t">            <span class="nam">event</span><span class="op">[</span><span class="str">"logging.googleapis.com/labels"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t49" href="#t49">49</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t50" href="#t50">50</a></span><span class="t">        <span class="key">return</span> <span class="nam">event</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t51" href="#t51">51</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t52" href="#t52">52</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t53" href="#t53">53</a></span><span class="t"><span class="key">class</span> <span class="nam">LogSeverity</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t54" href="#t54">54</a></span><span class="t">    <span class="str">"""Set the severity using the Google Cloud Logging severities"""</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t55" href="#t55">55</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t56" href="#t56">56</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t57" href="#t57">57</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">default</span> <span class="op">=</span> <span class="str">"notset"</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t58" href="#t58">58</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t59" href="#t59">59</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t60" href="#t60">60</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t61" href="#t61">61</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t62" href="#t62">62</a></span><span class="t"><span class="key">class</span> <span class="nam">ReportError</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t63" href="#t63">63</a></span><span class="t">    <span class="str">"""Report to Google Cloud Error Reporting specific log severities"""</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t64" href="#t64">64</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t65" href="#t65">65</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t66" href="#t66">66</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t67" href="#t67">67</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t68" href="#t68">68</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">severities</span><span class="op">=</span><span class="key">None</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="par run show_par"><span class="n"><a id="t69" href="#t69">69</a></span><span class="t">        <span class="key">if</span> <span class="nam">severities</span> <span class="key">is</span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"><span class="annotate short">69&#x202F;&#x219B;&#x202F;70</span><span class="annotate long">line 69 didn't jump to line 70, because the condition on line 69 was never true</span></span></p>
-    <p class="mis show_mis"><span class="n"><a id="t70" href="#t70">70</a></span><span class="t">            <span class="nam">severities</span> <span class="op">=</span> <span class="op">[</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t71" href="#t71">71</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t72" href="#t72">72</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">severities</span> <span class="op">=</span> <span class="nam">severities</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t73" href="#t73">73</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t74" href="#t74">74</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t75" href="#t75">75</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t59" href="#t59">59</a></span><span class="t">        <span class="com"># From Python's logging level to Google level</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t60" href="#t60">60</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">mapping</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t61" href="#t61">61</a></span><span class="t">            <span class="str">"notset"</span><span class="op">:</span> <span class="str">"DEFAULT"</span><span class="op">,</span>  <span class="com"># The log entry has no assigned severity level.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t62" href="#t62">62</a></span><span class="t">            <span class="str">"debug"</span><span class="op">:</span> <span class="str">"DEBUG"</span><span class="op">,</span>  <span class="com"># Debug or trace information.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t63" href="#t63">63</a></span><span class="t">            <span class="str">"info"</span><span class="op">:</span> <span class="str">"INFO"</span><span class="op">,</span>  <span class="com"># Routine information, such as ongoing status or performance.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t64" href="#t64">64</a></span><span class="t">            <span class="com"># "notice": "NOTICE", # Normal but significant events, such as start up, shut down, or a configuration change.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t65" href="#t65">65</a></span><span class="t">            <span class="str">"warn"</span><span class="op">:</span> <span class="str">"WARNING"</span><span class="op">,</span>  <span class="com"># Warning events might cause problems.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t66" href="#t66">66</a></span><span class="t">            <span class="str">"warning"</span><span class="op">:</span> <span class="str">"WARNING"</span><span class="op">,</span>  <span class="com"># Warning events might cause problems.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t67" href="#t67">67</a></span><span class="t">            <span class="str">"error"</span><span class="op">:</span> <span class="str">"ERROR"</span><span class="op">,</span>  <span class="com"># Error events are likely to cause problems.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t68" href="#t68">68</a></span><span class="t">            <span class="str">"critical"</span><span class="op">:</span> <span class="str">"CRITICAL"</span><span class="op">,</span>  <span class="com"># Critical events cause more severe problems or outages.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t69" href="#t69">69</a></span><span class="t">            <span class="com"># "alert": "ALERT", # A person must take an action immediately.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t70" href="#t70">70</a></span><span class="t">            <span class="com"># "emergency": "EMERGENCY", #       One or more systems are unusable.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t71" href="#t71">71</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t72" href="#t72">72</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t73" href="#t73">73</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t74" href="#t74">74</a></span><span class="t">        <span class="com"># Add log level to event dict.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t75" href="#t75">75</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">add_log_level</span><span class="op">,</span> <span class="nam">self</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t76" href="#t76">76</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t77" href="#t77">77</a></span><span class="t">    <span class="key">def</span> <span class="nam">_build_service_context</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t78" href="#t78">78</a></span><span class="t">        <span class="key">import</span> <span class="nam">os</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t79" href="#t79">79</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t80" href="#t80">80</a></span><span class="t">        <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ServiceContext</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t81" href="#t81">81</a></span><span class="t">        <span class="nam">service_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t82" href="#t82">82</a></span><span class="t">            <span class="com"># https://cloud.google.com/functions/docs/configuring/env-var#runtime_environment_variables_set_automatically</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t83" href="#t83">83</a></span><span class="t">            <span class="str">"service"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_SERVICE"</span><span class="op">,</span> <span class="str">"unknown service"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t84" href="#t84">84</a></span><span class="t">            <span class="str">"version"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_REVISION"</span><span class="op">,</span> <span class="str">"unknown version"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t85" href="#t85">85</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t86" href="#t86">86</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t87" href="#t87">87</a></span><span class="t">        <span class="key">return</span> <span class="nam">service_context</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t88" href="#t88">88</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t89" href="#t89">89</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t90" href="#t90">90</a></span><span class="t">        <span class="nam">severity</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t77" href="#t77">77</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t78" href="#t78">78</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t79" href="#t79">79</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t80" href="#t80">80</a></span><span class="t">        <span class="str">"""Format a Python log level value as a GCP log severity.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t81" href="#t81">81</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t82" href="#t82">82</a></span><span class="t"><span class="str">        See: https://cloud.google.com/logging/docs/reference/v2/rest/v2/LogEntry#LogSeverity</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t83" href="#t83">83</a></span><span class="t"><span class="str">        """</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t84" href="#t84">84</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t85" href="#t85">85</a></span><span class="t">        <span class="nam">log_level</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"level"</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t86" href="#t86">86</a></span><span class="t">        <span class="nam">severity</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">mapping</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="nam">log_level</span><span class="op">,</span> <span class="nam">self</span><span class="op">.</span><span class="nam">default</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t87" href="#t87">87</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t88" href="#t88">88</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">severity</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t89" href="#t89">89</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t90" href="#t90">90</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t91" href="#t91">91</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t92" href="#t92">92</a></span><span class="t">        <span class="key">if</span> <span class="nam">severity</span> <span class="key">not</span> <span class="key">in</span> <span class="nam">self</span><span class="op">.</span><span class="nam">severities</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t93" href="#t93">93</a></span><span class="t">            <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t92" href="#t92">92</a></span><span class="t"><span class="key">class</span> <span class="nam">CodeLocation</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t93" href="#t93">93</a></span><span class="t">    <span class="str">"""Inject the location of the logging message into the logs"""</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t94" href="#t94">94</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t95" href="#t95">95</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"@type"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">ERROR_EVENT_TYPE</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t96" href="#t96">96</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="par run show_par"><span class="n"><a id="t97" href="#t97">97</a></span><span class="t">        <span class="key">if</span> <span class="nam">SOURCE_LOCATION_KEY</span> <span class="key">in</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"><span class="annotate short">97&#x202F;&#x219B;&#x202F;104</span><span class="annotate long">line 97 didn't jump to line 104, because the condition on line 97 was never false</span></span></p>
-    <p class="pln"><span class="n"><a id="t98" href="#t98">98</a></span><span class="t">            <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ErrorContext</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t99" href="#t99">99</a></span><span class="t">            <span class="nam">error_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t100" href="#t100">100</a></span><span class="t">                <span class="str">"reportLocation"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="nam">SOURCE_LOCATION_KEY</span><span class="op">]</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t101" href="#t101">101</a></span><span class="t">            <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t102" href="#t102">102</a></span><span class="t">            <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"context"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">error_context</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t103" href="#t103">103</a></span><span class="t">        <span class="key">else</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="mis show_mis"><span class="n"><a id="t104" href="#t104">104</a></span><span class="t">            <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"context"</span><span class="op">]</span> <span class="op">=</span> <span class="str">"no location :("</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t105" href="#t105">105</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t106" href="#t106">106</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"serviceContext"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">_build_service_context</span><span class="op">(</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t107" href="#t107">107</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t108" href="#t108">108</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t95" href="#t95">95</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t96" href="#t96">96</a></span><span class="t">        <span class="com"># Add callsite parameters.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t97" href="#t97">97</a></span><span class="t">        <span class="nam">call_site_proc</span> <span class="op">=</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameterAdder</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t98" href="#t98">98</a></span><span class="t">            <span class="nam">parameters</span><span class="op">=</span><span class="op">[</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t99" href="#t99">99</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">PATHNAME</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t100" href="#t100">100</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">MODULE</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t101" href="#t101">101</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">FUNC_NAME</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t102" href="#t102">102</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">LINENO</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t103" href="#t103">103</a></span><span class="t">            <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t104" href="#t104">104</a></span><span class="t">        <span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t105" href="#t105">105</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">call_site_proc</span><span class="op">,</span> <span class="nam">self</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t106" href="#t106">106</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t107" href="#t107">107</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t108" href="#t108">108</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t109" href="#t109">109</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t110" href="#t110">110</a></span><span class="t">        <span class="nam">location</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t111" href="#t111">111</a></span><span class="t">            <span class="str">"file"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"pathname"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t112" href="#t112">112</a></span><span class="t">            <span class="str">"line"</span><span class="op">:</span> <span class="nam">str</span><span class="op">(</span><span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"lineno"</span><span class="op">)</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t113" href="#t113">113</a></span><span class="t">            <span class="str">"function"</span><span class="op">:</span> <span class="str">f"{event_dict.pop('module')}:{event_dict.pop('func_name')}"</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t114" href="#t114">114</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t115" href="#t115">115</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t116" href="#t116">116</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="nam">SOURCE_LOCATION_KEY</span><span class="op">]</span> <span class="op">=</span> <span class="nam">location</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t117" href="#t117">117</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t118" href="#t118">118</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
 </main>
 <footer>
     <div class="content">
         <p>
-            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_base_py.html">&#xab; prev</a> &nbsp; &nbsp;
+            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
-            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xbb; next</a>
+            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_types_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
 </footer>
 </body>
 </html>
```

#### html2text {}

```diff
@@ -1,141 +1,145 @@
 
-****** Coverage for structlog_gcp/errors.py: 93% ******
+****** Coverage for structlog_gcp/processors.py: 100% ******
  ⁰  [Show/hide keyboard shortcuts]
 Shortcuts on this page
 r m x p   toggle line displays
 j k   next/prev highlighted chunk
 0   (zero) top of page
 1   (one) first highlighted chunk
 [ ]   prev/next file
 u   up to the index
 ?   show/hide this help
-***** 47 statements   45 run 2 missing 0 excluded 2 partial *****
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+***** 37 statements   37 run 0 missing 0 excluded 0 partial *****
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
 
 
-1import os 
-2 
-3import structlog 
+1# https://cloud.google.com/functions/docs/monitoring/
+logging#writing_structured_logs 
+2# https://cloud.google.com/logging/docs/agent/logging/configuration#process-
+payload 
+3# https://cloud.google.com/logging/docs/structured-logging#special-payload-
+fields 
 4 
-5from .types import CLOUD_LOGGING_KEY, ERROR_EVENT_TYPE, SOURCE_LOCATION_KEY 
-6 
-7 
-8def add_service_context(logger, method_name, event_dict): 
-9 """Add a service context in which an error has occurred. 
+5 
+6import structlog.processors 
+7from structlog.typing import EventDict, Processor, WrappedLogger 
+8 
+9from .types import CLOUD_LOGGING_KEY, SOURCE_LOCATION_KEY 
 10 
-11 This is part of the Error Reporting API, so it's only added when an error
-happens. 
-12 """ 
-13 
-14 event_type = event_dict[CLOUD_LOGGING_KEY].get("@type") 
-15 if event_type != ERROR_EVENT_TYPE: 
-16 return event_dict 
-17 
-18 service_context = { 
-19 # https://cloud.google.com/functions/docs/configuring/env-
-var#runtime_environment_variables_set_automatically 
-20 "service": os.environ.get("K_SERVICE", "unknown service"), 
-21 "version": os.environ.get("K_REVISION", "unknown version"), 
-22 } 
+11 
+12class CoreCloudLogging: 
+13 """Initialize the Google Cloud Logging event message""" 
+14 
+15 def setup(self) -> list[Processor]: 
+16 return [ 
+17 # If some value is in bytes, decode it to a unicode str. 
+18 structlog.processors.UnicodeDecoder(), 
+19 # Add a timestamp in ISO 8601 format. 
+20 structlog.processors.TimeStamper(fmt="iso"), 
+21 self, 
+22 ] 
 23 
-24 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
-ServiceContext 
-25 event_dict[CLOUD_LOGGING_KEY]["serviceContext"] = service_context 
-26 
-27 return event_dict 
-28 
-29 
-30class ReportException: 
-31 """Transform exception into a Google Cloud Error Reporting event.""" 
-32 
-33 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
-projects.events/report 
-34 # https://cloud.google.com/error-reporting/docs/formatting-error-
-messages#log-entry-examples 
+24 def __call__( 
+25 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+26 ) -> EventDict: 
+27 value = { 
+28 "message": event_dict.pop("event"), 
+29 "time": event_dict.pop("timestamp"), 
+30 } 
+31 
+32 event_dict[CLOUD_LOGGING_KEY] = value 
+33 return event_dict 
+34 
 35 
-36 def __init__(self, log_level="CRITICAL"): 
-37 self.log_level = log_level 
+36class FormatAsCloudLogging: 
+37 """Finalize the Google Cloud Logging event message and replace the logging
+event""" 
 38 
-39 def setup(self): 
-40 return [ 
-41 # structlog.processors.ExceptionRenderer(self.format_exception), 
-42 structlog.processors.format_exc_info, 
-43 self.__call__, 
-44 ] 
-45 
-46 def __call__(self, logger, method_name, event_dict): 
-47 exception = event_dict.pop("exception", None) 
-48 if exception is None: 
-49 return event_dict 
-50 
-51 event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE 
-52 event_dict[CLOUD_LOGGING_KEY]["severity"] = self.log_level 
-53 
-54 # https://cloud.google.com/error-reporting/docs/formatting-error-messages 
-55 message = event_dict[CLOUD_LOGGING_KEY]["message"] 
-56 error_message = f"{message}\n{exception}" 
-57 event_dict[CLOUD_LOGGING_KEY]["stack_trace"] = error_message 
+39 def setup(self) -> list[Processor]: 
+40 return [self, structlog.processors.JSONRenderer()] 
+41 
+42 def __call__( 
+43 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+44 ) -> EventDict: 
+45 event: EventDict = event_dict.pop(CLOUD_LOGGING_KEY) 
+46 
+47 if event_dict: 
+48 event["logging.googleapis.com/labels"] = event_dict 
+49 
+50 return event 
+51 
+52 
+53class LogSeverity: 
+54 """Set the severity using the Google Cloud Logging severities""" 
+55 
+56 def __init__(self) -> None: 
+57 self.default = "notset" 
 58 
-59 return event_dict 
-60 
-61 
-62class ReportError: 
-63 """Report to Google Cloud Error Reporting specific log severities""" 
-64 
-65 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
-projects.events/report 
-66 # https://cloud.google.com/error-reporting/docs/formatting-error-
-messages#log-entry-examples 
-67 
-68 def __init__(self, severities=None): 
-69 if severities is None: 69&#x202F;&#x219B;&#x202F;70line 69 didn't jump to
-line 70, because the condition on line 69 was never true
-70 severities = [] 
-71 
-72 self.severities = severities 
-73 
-74 def setup(self): 
-75 return [self.__call__] 
+59 # From Python's logging level to Google level 
+60 self.mapping = { 
+61 "notset": "DEFAULT", # The log entry has no assigned severity level. 
+62 "debug": "DEBUG", # Debug or trace information. 
+63 "info": "INFO", # Routine information, such as ongoing status or
+performance. 
+64 # "notice": "NOTICE", # Normal but significant events, such as start up,
+shut down, or a configuration change. 
+65 "warn": "WARNING", # Warning events might cause problems. 
+66 "warning": "WARNING", # Warning events might cause problems. 
+67 "error": "ERROR", # Error events are likely to cause problems. 
+68 "critical": "CRITICAL", # Critical events cause more severe problems or
+outages. 
+69 # "alert": "ALERT", # A person must take an action immediately. 
+70 # "emergency": "EMERGENCY", # One or more systems are unusable. 
+71 } 
+72 
+73 def setup(self) -> list[Processor]: 
+74 # Add log level to event dict. 
+75 return [structlog.processors.add_log_level, self] 
 76 
-77 def _build_service_context(self): 
-78 import os 
-79 
-80 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
-ServiceContext 
-81 service_context = { 
-82 # https://cloud.google.com/functions/docs/configuring/env-
-var#runtime_environment_variables_set_automatically 
-83 "service": os.environ.get("K_SERVICE", "unknown service"), 
-84 "version": os.environ.get("K_REVISION", "unknown version"), 
-85 } 
-86 
-87 return service_context 
-88 
-89 def __call__(self, logger, method_name, event_dict): 
-90 severity = event_dict[CLOUD_LOGGING_KEY]["severity"] 
+77 def __call__( 
+78 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+79 ) -> EventDict: 
+80 """Format a Python log level value as a GCP log severity. 
+81 
+82 See: https://cloud.google.com/logging/docs/reference/v2/rest/v2/
+LogEntry#LogSeverity 
+83 """ 
+84 
+85 log_level = event_dict.pop("level") 
+86 severity = self.mapping.get(log_level, self.default) 
+87 
+88 event_dict[CLOUD_LOGGING_KEY]["severity"] = severity 
+89 return event_dict 
+90 
 91 
-92 if severity not in self.severities: 
-93 return event_dict 
+92class CodeLocation: 
+93 """Inject the location of the logging message into the logs""" 
 94 
-95 event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE 
-96 
-97 if SOURCE_LOCATION_KEY in event_dict[CLOUD_LOGGING_KEY]:
- 97&#x202F;&#x219B;&#x202F;104line 97 didn't jump to line 104, because the
-condition on line 97 was never false
-98 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
-ErrorContext 
-99 error_context = { 
-100 "reportLocation": event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY], 
-101 } 
-102 event_dict[CLOUD_LOGGING_KEY]["context"] = error_context 
-103 else: 
-104 event_dict[CLOUD_LOGGING_KEY]["context"] = "no location :(" 
-105 
-106 event_dict[CLOUD_LOGGING_KEY]["serviceContext"] =
-self._build_service_context() 
-107 
-108 return event_dict 
+95 def setup(self) -> list[Processor]: 
+96 # Add callsite parameters. 
+97 call_site_proc = structlog.processors.CallsiteParameterAdder( 
+98 parameters=[ 
+99 structlog.processors.CallsiteParameter.PATHNAME, 
+100 structlog.processors.CallsiteParameter.MODULE, 
+101 structlog.processors.CallsiteParameter.FUNC_NAME, 
+102 structlog.processors.CallsiteParameter.LINENO, 
+103 ] 
+104 ) 
+105 return [call_site_proc, self] 
+106 
+107 def __call__( 
+108 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+109 ) -> EventDict: 
+110 location = { 
+111 "file": event_dict.pop("pathname"), 
+112 "line": str(event_dict.pop("lineno")), 
+113 "function": f"{event_dict.pop('module')}:{event_dict.pop('func_name')}", 
+114 } 
+115 
+116 event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY] = location 
+117 
+118 return event_dict 
 
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
```

### Comparing `structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_processors_py.html` & `structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_errors_py.html`

 * *Files 8% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 <!DOCTYPE html>
 <html>
 <head>
     <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
-    <title>Coverage for structlog_gcp/processors.py: 100%</title>
+    <title>Coverage for structlog_gcp/errors.py: 100%</title>
     <link rel="icon" sizes="32x32" href="favicon_32.png">
     <link rel="stylesheet" href="style.css" type="text/css">
     <script type="text/javascript" src="coverage_html.js" defer></script>
 </head>
 <body class="pyfile">
 <header>
     <div class="content">
         <h1>
-            <span class="text">Coverage for </span><b>structlog_gcp/processors.py</b>:
+            <span class="text">Coverage for </span><b>structlog_gcp/errors.py</b>:
             <span class="pc_cov">100%</span>
         </h1>
         <aside id="help_panel_wrapper">
             <input id="help_panel_state" type="checkbox">
             <label for="help_panel_state">
                 <img id="keyboard_icon" src="keybd_closed.png" alt="Show/hide keyboard shortcuts" />
             </label>
@@ -51,163 +51,154 @@
                     <p>
                         <kbd>?</kbd> &nbsp; show/hide this help
                     </p>
                 </div>
             </div>
         </aside>
         <h2>
-            <span class="text">36 statements &nbsp;</span>
-            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">36<span class="text"> run</span></button>
+            <span class="text">43 statements &nbsp;</span>
+            <button type="button" class="run button_toggle_run" value="run" data-shortcut="r" title="Toggle lines run">43<span class="text"> run</span></button>
             <button type="button" class="mis show_mis button_toggle_mis" value="mis" data-shortcut="m" title="Toggle lines missing">0<span class="text"> missing</span></button>
             <button type="button" class="exc show_exc button_toggle_exc" value="exc" data-shortcut="x" title="Toggle lines excluded">0<span class="text"> excluded</span></button>
             <button type="button" class="par run show_par button_toggle_par" value="par" data-shortcut="p" title="Toggle lines partially run">0<span class="text"> partial</span></button>
         </h2>
         <p class="text">
-            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xab; prev</a> &nbsp; &nbsp;
+            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_base_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
-            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_types_py.html">&#xbb; next</a>
+            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
         <aside class="hidden">
             <button type="button" class="button_next_chunk" data-shortcut="j"/>
             <button type="button" class="button_prev_chunk" data-shortcut="k"/>
             <button type="button" class="button_top_of_page" data-shortcut="0"/>
             <button type="button" class="button_first_chunk" data-shortcut="1"/>
             <button type="button" class="button_prev_file" data-shortcut="["/>
             <button type="button" class="button_next_file" data-shortcut="]"/>
             <button type="button" class="button_to_index" data-shortcut="u"/>
             <button type="button" class="button_show_hide_help" data-shortcut="?"/>
         </aside>
     </div>
 </header>
 <main id="source">
-    <p class="pln"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="com"># https://cloud.google.com/functions/docs/monitoring/logging#writing_structured_logs</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t2" href="#t2">2</a></span><span class="t"><span class="com"># https://cloud.google.com/logging/docs/agent/logging/configuration#process-payload</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t"><span class="com"># https://cloud.google.com/logging/docs/structured-logging#special-payload-fields</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t4" href="#t4">4</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t"><span class="key">import</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t"><span class="key">from</span> <span class="op">.</span><span class="nam">types</span> <span class="key">import</span> <span class="nam">CLOUD_LOGGING_KEY</span><span class="op">,</span> <span class="nam">SOURCE_LOCATION_KEY</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t1" href="#t1">1</a></span><span class="t"><span class="key">import</span> <span class="nam">os</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t2" href="#t2">2</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t3" href="#t3">3</a></span><span class="t"><span class="key">import</span> <span class="nam">structlog</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t4" href="#t4">4</a></span><span class="t"><span class="key">from</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">typing</span> <span class="key">import</span> <span class="nam">EventDict</span><span class="op">,</span> <span class="nam">Processor</span><span class="op">,</span> <span class="nam">WrappedLogger</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t5" href="#t5">5</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t6" href="#t6">6</a></span><span class="t"><span class="key">from</span> <span class="op">.</span><span class="nam">types</span> <span class="key">import</span> <span class="nam">CLOUD_LOGGING_KEY</span><span class="op">,</span> <span class="nam">ERROR_EVENT_TYPE</span><span class="op">,</span> <span class="nam">SOURCE_LOCATION_KEY</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t7" href="#t7">7</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t8" href="#t8">8</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t10" href="#t10">10</a></span><span class="t"><span class="key">class</span> <span class="nam">CoreCloudLogging</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t">    <span class="str">"""Initialize the Google Cloud Logging event message"""</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t">            <span class="com"># If some value is in bytes, decode it to a unicode str.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">UnicodeDecoder</span><span class="op">(</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">            <span class="com"># Add a timestamp in ISO 8601 format.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t18" href="#t18">18</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">TimeStamper</span><span class="op">(</span><span class="nam">fmt</span><span class="op">=</span><span class="str">"iso"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t19" href="#t19">19</a></span><span class="t">            <span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t20" href="#t20">20</a></span><span class="t">        <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t21" href="#t21">21</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t22" href="#t22">22</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t23" href="#t23">23</a></span><span class="t">        <span class="nam">value</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t24" href="#t24">24</a></span><span class="t">            <span class="str">"message"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"event"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t25" href="#t25">25</a></span><span class="t">            <span class="str">"time"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"timestamp"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t26" href="#t26">26</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t27" href="#t27">27</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t28" href="#t28">28</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span> <span class="op">=</span> <span class="nam">value</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t29" href="#t29">29</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t30" href="#t30">30</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t9" href="#t9">9</a></span><span class="t"><span class="key">def</span> <span class="nam">add_service_context</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t10" href="#t10">10</a></span><span class="t">    <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t11" href="#t11">11</a></span><span class="t"><span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t12" href="#t12">12</a></span><span class="t">    <span class="str">"""Add a service context in which an error has occurred.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t13" href="#t13">13</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t14" href="#t14">14</a></span><span class="t"><span class="str">    This is part of the Error Reporting API, so it's only added when an error happens.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t15" href="#t15">15</a></span><span class="t"><span class="str">    """</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t16" href="#t16">16</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t17" href="#t17">17</a></span><span class="t">    <span class="nam">event_type</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"@type"</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t18" href="#t18">18</a></span><span class="t">    <span class="key">if</span> <span class="nam">event_type</span> <span class="op">!=</span> <span class="nam">ERROR_EVENT_TYPE</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t19" href="#t19">19</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t20" href="#t20">20</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t21" href="#t21">21</a></span><span class="t">    <span class="nam">service_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t22" href="#t22">22</a></span><span class="t">        <span class="com"># https://cloud.google.com/functions/docs/configuring/env-var#runtime_environment_variables_set_automatically</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t23" href="#t23">23</a></span><span class="t">        <span class="str">"service"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_SERVICE"</span><span class="op">,</span> <span class="str">"unknown service"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t24" href="#t24">24</a></span><span class="t">        <span class="str">"version"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_REVISION"</span><span class="op">,</span> <span class="str">"unknown version"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t25" href="#t25">25</a></span><span class="t">    <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t26" href="#t26">26</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t27" href="#t27">27</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ServiceContext</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t28" href="#t28">28</a></span><span class="t">    <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"serviceContext"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">service_context</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t29" href="#t29">29</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t30" href="#t30">30</a></span><span class="t">    <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t31" href="#t31">31</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t32" href="#t32">32</a></span><span class="t"><span class="key">class</span> <span class="nam">FormatAsCloudLogging</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t33" href="#t33">33</a></span><span class="t">    <span class="str">"""Finalize the Google Cloud Logging event message and replace the logging event"""</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t34" href="#t34">34</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t35" href="#t35">35</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t36" href="#t36">36</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t37" href="#t37">37</a></span><span class="t">            <span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t38" href="#t38">38</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">JSONRenderer</span><span class="op">(</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t39" href="#t39">39</a></span><span class="t">        <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t40" href="#t40">40</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t41" href="#t41">41</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t42" href="#t42">42</a></span><span class="t">        <span class="nam">event</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t43" href="#t43">43</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t44" href="#t44">44</a></span><span class="t">        <span class="key">if</span> <span class="nam">event_dict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t45" href="#t45">45</a></span><span class="t">            <span class="nam">event</span><span class="op">[</span><span class="str">"logging.googleapis.com/labels"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t46" href="#t46">46</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t47" href="#t47">47</a></span><span class="t">        <span class="key">return</span> <span class="nam">event</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t48" href="#t48">48</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t49" href="#t49">49</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t50" href="#t50">50</a></span><span class="t"><span class="key">class</span> <span class="nam">LogSeverity</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t51" href="#t51">51</a></span><span class="t">    <span class="str">"""Set the severity using the Google Cloud Logging severities"""</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t52" href="#t52">52</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t53" href="#t53">53</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t54" href="#t54">54</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">default</span> <span class="op">=</span> <span class="str">"notset"</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t55" href="#t55">55</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t56" href="#t56">56</a></span><span class="t">        <span class="com"># From Python's logging level to Google level</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t57" href="#t57">57</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">mapping</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t58" href="#t58">58</a></span><span class="t">            <span class="str">"notset"</span><span class="op">:</span> <span class="str">"DEFAULT"</span><span class="op">,</span>  <span class="com"># The log entry has no assigned severity level.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t59" href="#t59">59</a></span><span class="t">            <span class="str">"debug"</span><span class="op">:</span> <span class="str">"DEBUG"</span><span class="op">,</span>  <span class="com"># Debug or trace information.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t60" href="#t60">60</a></span><span class="t">            <span class="str">"info"</span><span class="op">:</span> <span class="str">"INFO"</span><span class="op">,</span>  <span class="com"># Routine information, such as ongoing status or performance.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t61" href="#t61">61</a></span><span class="t">            <span class="com"># "notice": "NOTICE", # Normal but significant events, such as start up, shut down, or a configuration change.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t62" href="#t62">62</a></span><span class="t">            <span class="str">"warn"</span><span class="op">:</span> <span class="str">"WARNING"</span><span class="op">,</span>  <span class="com"># Warning events might cause problems.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t63" href="#t63">63</a></span><span class="t">            <span class="str">"warning"</span><span class="op">:</span> <span class="str">"WARNING"</span><span class="op">,</span>  <span class="com"># Warning events might cause problems.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t64" href="#t64">64</a></span><span class="t">            <span class="str">"error"</span><span class="op">:</span> <span class="str">"ERROR"</span><span class="op">,</span>  <span class="com"># Error events are likely to cause problems.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t65" href="#t65">65</a></span><span class="t">            <span class="str">"critical"</span><span class="op">:</span> <span class="str">"CRITICAL"</span><span class="op">,</span>  <span class="com"># Critical events cause more severe problems or outages.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t66" href="#t66">66</a></span><span class="t">            <span class="com"># "alert": "ALERT", # A person must take an action immediately.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t67" href="#t67">67</a></span><span class="t">            <span class="com"># "emergency": "EMERGENCY", #       One or more systems are unusable.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t68" href="#t68">68</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t69" href="#t69">69</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t70" href="#t70">70</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t71" href="#t71">71</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t72" href="#t72">72</a></span><span class="t">            <span class="com"># Add log level to event dict.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t73" href="#t73">73</a></span><span class="t">            <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">add_log_level</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t74" href="#t74">74</a></span><span class="t">            <span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t75" href="#t75">75</a></span><span class="t">        <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t76" href="#t76">76</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t77" href="#t77">77</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t78" href="#t78">78</a></span><span class="t">        <span class="str">"""Format a Python log level value as a GCP log severity.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t79" href="#t79">79</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t80" href="#t80">80</a></span><span class="t"><span class="str">        See: https://cloud.google.com/logging/docs/reference/v2/rest/v2/LogEntry#LogSeverity</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t81" href="#t81">81</a></span><span class="t"><span class="str">        """</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t82" href="#t82">82</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t83" href="#t83">83</a></span><span class="t">        <span class="nam">log_level</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"level"</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t84" href="#t84">84</a></span><span class="t">        <span class="nam">severity</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">mapping</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="nam">log_level</span><span class="op">,</span> <span class="nam">self</span><span class="op">.</span><span class="nam">default</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t32" href="#t32">32</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t33" href="#t33">33</a></span><span class="t"><span class="key">class</span> <span class="nam">ReportException</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t34" href="#t34">34</a></span><span class="t">    <span class="str">"""Transform exception into a Google Cloud Error Reporting event."""</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t35" href="#t35">35</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t36" href="#t36">36</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t37" href="#t37">37</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t38" href="#t38">38</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t39" href="#t39">39</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">log_level</span><span class="op">:</span> <span class="nam">str</span> <span class="op">=</span> <span class="str">"CRITICAL"</span><span class="op">)</span> <span class="op">-></span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t40" href="#t40">40</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">log_level</span> <span class="op">=</span> <span class="nam">log_level</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t41" href="#t41">41</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t42" href="#t42">42</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t43" href="#t43">43</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">format_exc_info</span><span class="op">,</span> <span class="nam">self</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t44" href="#t44">44</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t45" href="#t45">45</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t46" href="#t46">46</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t47" href="#t47">47</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t48" href="#t48">48</a></span><span class="t">        <span class="nam">exception</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"exception"</span><span class="op">,</span> <span class="key">None</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t49" href="#t49">49</a></span><span class="t">        <span class="key">if</span> <span class="nam">exception</span> <span class="key">is</span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t50" href="#t50">50</a></span><span class="t">            <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t51" href="#t51">51</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t52" href="#t52">52</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"@type"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">ERROR_EVENT_TYPE</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t53" href="#t53">53</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">log_level</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t54" href="#t54">54</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t55" href="#t55">55</a></span><span class="t">        <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t56" href="#t56">56</a></span><span class="t">        <span class="nam">message</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"message"</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t57" href="#t57">57</a></span><span class="t">        <span class="nam">error_message</span> <span class="op">=</span> <span class="str">f"{message}\n{exception}"</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t58" href="#t58">58</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"stack_trace"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">error_message</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t59" href="#t59">59</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t60" href="#t60">60</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t61" href="#t61">61</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t62" href="#t62">62</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t63" href="#t63">63</a></span><span class="t"><span class="key">class</span> <span class="nam">ReportError</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t64" href="#t64">64</a></span><span class="t">    <span class="str">"""Report to Google Cloud Error Reporting specific log severities</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t65" href="#t65">65</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t66" href="#t66">66</a></span><span class="t"><span class="str">    This class assumes the :ref:`.processors.CodeLocation` processor ran before.</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t67" href="#t67">67</a></span><span class="t"><span class="str">    """</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t68" href="#t68">68</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t69" href="#t69">69</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t70" href="#t70">70</a></span><span class="t">    <span class="com"># https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t71" href="#t71">71</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t72" href="#t72">72</a></span><span class="t">    <span class="key">def</span> <span class="nam">__init__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">severities</span><span class="op">:</span> <span class="nam">list</span><span class="op">[</span><span class="nam">str</span><span class="op">]</span><span class="op">)</span> <span class="op">-></span> <span class="key">None</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t73" href="#t73">73</a></span><span class="t">        <span class="nam">self</span><span class="op">.</span><span class="nam">severities</span> <span class="op">=</span> <span class="nam">severities</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t74" href="#t74">74</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t75" href="#t75">75</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">list</span><span class="op">[</span><span class="nam">Processor</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t76" href="#t76">76</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">self</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t77" href="#t77">77</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t78" href="#t78">78</a></span><span class="t">    <span class="key">def</span> <span class="nam">_build_service_context</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span> <span class="op">-></span> <span class="nam">dict</span><span class="op">[</span><span class="nam">str</span><span class="op">,</span> <span class="nam">str</span><span class="op">]</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t79" href="#t79">79</a></span><span class="t">        <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ServiceContext</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t80" href="#t80">80</a></span><span class="t">        <span class="nam">service_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t81" href="#t81">81</a></span><span class="t">            <span class="com"># https://cloud.google.com/functions/docs/configuring/env-var#runtime_environment_variables_set_automatically</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t82" href="#t82">82</a></span><span class="t">            <span class="str">"service"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_SERVICE"</span><span class="op">,</span> <span class="str">"unknown service"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t83" href="#t83">83</a></span><span class="t">            <span class="str">"version"</span><span class="op">:</span> <span class="nam">os</span><span class="op">.</span><span class="nam">environ</span><span class="op">.</span><span class="nam">get</span><span class="op">(</span><span class="str">"K_REVISION"</span><span class="op">,</span> <span class="str">"unknown version"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t84" href="#t84">84</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t85" href="#t85">85</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t86" href="#t86">86</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">severity</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t87" href="#t87">87</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t88" href="#t88">88</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t89" href="#t89">89</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t90" href="#t90">90</a></span><span class="t"><span class="key">class</span> <span class="nam">CodeLocation</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t91" href="#t91">91</a></span><span class="t">    <span class="str">"""Inject the location of the logging message into the logs"""</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t86" href="#t86">86</a></span><span class="t">        <span class="key">return</span> <span class="nam">service_context</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t87" href="#t87">87</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t88" href="#t88">88</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t89" href="#t89">89</a></span><span class="t">        <span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">:</span> <span class="nam">WrappedLogger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">:</span> <span class="nam">str</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">:</span> <span class="nam">EventDict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t90" href="#t90">90</a></span><span class="t">    <span class="op">)</span> <span class="op">-></span> <span class="nam">EventDict</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t91" href="#t91">91</a></span><span class="t">        <span class="nam">severity</span> <span class="op">=</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"severity"</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t92" href="#t92">92</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t93" href="#t93">93</a></span><span class="t">    <span class="key">def</span> <span class="nam">setup</span><span class="op">(</span><span class="nam">self</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t94" href="#t94">94</a></span><span class="t">        <span class="com"># Add callsite parameters.</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t95" href="#t95">95</a></span><span class="t">        <span class="nam">call_site_proc</span> <span class="op">=</span> <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameterAdder</span><span class="op">(</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t96" href="#t96">96</a></span><span class="t">            <span class="nam">parameters</span><span class="op">=</span><span class="op">[</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t97" href="#t97">97</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">PATHNAME</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t98" href="#t98">98</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">MODULE</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t99" href="#t99">99</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">FUNC_NAME</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t100" href="#t100">100</a></span><span class="t">                <span class="nam">structlog</span><span class="op">.</span><span class="nam">processors</span><span class="op">.</span><span class="nam">CallsiteParameter</span><span class="op">.</span><span class="nam">LINENO</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t101" href="#t101">101</a></span><span class="t">            <span class="op">]</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t102" href="#t102">102</a></span><span class="t">        <span class="op">)</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t103" href="#t103">103</a></span><span class="t">        <span class="key">return</span> <span class="op">[</span><span class="nam">call_site_proc</span><span class="op">,</span> <span class="nam">self</span><span class="op">.</span><span class="nam">__call__</span><span class="op">]</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t93" href="#t93">93</a></span><span class="t">        <span class="key">if</span> <span class="nam">severity</span> <span class="key">not</span> <span class="key">in</span> <span class="nam">self</span><span class="op">.</span><span class="nam">severities</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t94" href="#t94">94</a></span><span class="t">            <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t95" href="#t95">95</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t96" href="#t96">96</a></span><span class="t">        <span class="com"># https://cloud.google.com/error-reporting/reference/rest/v1beta1/ErrorContext</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t97" href="#t97">97</a></span><span class="t">        <span class="nam">error_context</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t98" href="#t98">98</a></span><span class="t">            <span class="str">"reportLocation"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="nam">SOURCE_LOCATION_KEY</span><span class="op">]</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t99" href="#t99">99</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
+    <p class="pln"><span class="n"><a id="t100" href="#t100">100</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t101" href="#t101">101</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"@type"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">ERROR_EVENT_TYPE</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t102" href="#t102">102</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"context"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">error_context</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t103" href="#t103">103</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="str">"serviceContext"</span><span class="op">]</span> <span class="op">=</span> <span class="nam">self</span><span class="op">.</span><span class="nam">_build_service_context</span><span class="op">(</span><span class="op">)</span>&nbsp;</span><span class="r"></span></p>
     <p class="pln"><span class="n"><a id="t104" href="#t104">104</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t105" href="#t105">105</a></span><span class="t">    <span class="key">def</span> <span class="nam">__call__</span><span class="op">(</span><span class="nam">self</span><span class="op">,</span> <span class="nam">logger</span><span class="op">,</span> <span class="nam">method_name</span><span class="op">,</span> <span class="nam">event_dict</span><span class="op">)</span><span class="op">:</span>&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t106" href="#t106">106</a></span><span class="t">        <span class="nam">location</span> <span class="op">=</span> <span class="op">{</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t107" href="#t107">107</a></span><span class="t">            <span class="str">"file"</span><span class="op">:</span> <span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"pathname"</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t108" href="#t108">108</a></span><span class="t">            <span class="str">"line"</span><span class="op">:</span> <span class="nam">str</span><span class="op">(</span><span class="nam">event_dict</span><span class="op">.</span><span class="nam">pop</span><span class="op">(</span><span class="str">"lineno"</span><span class="op">)</span><span class="op">)</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t109" href="#t109">109</a></span><span class="t">            <span class="str">"function"</span><span class="op">:</span> <span class="str">f"{event_dict.pop('module')}:{event_dict.pop('func_name')}"</span><span class="op">,</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t110" href="#t110">110</a></span><span class="t">        <span class="op">}</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t111" href="#t111">111</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t112" href="#t112">112</a></span><span class="t">        <span class="nam">event_dict</span><span class="op">[</span><span class="nam">CLOUD_LOGGING_KEY</span><span class="op">]</span><span class="op">[</span><span class="nam">SOURCE_LOCATION_KEY</span><span class="op">]</span> <span class="op">=</span> <span class="nam">location</span>&nbsp;</span><span class="r"></span></p>
-    <p class="pln"><span class="n"><a id="t113" href="#t113">113</a></span><span class="t">&nbsp;</span><span class="r"></span></p>
-    <p class="run"><span class="n"><a id="t114" href="#t114">114</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
+    <p class="run"><span class="n"><a id="t105" href="#t105">105</a></span><span class="t">        <span class="key">return</span> <span class="nam">event_dict</span>&nbsp;</span><span class="r"></span></p>
 </main>
 <footer>
     <div class="content">
         <p>
-            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_errors_py.html">&#xab; prev</a> &nbsp; &nbsp;
+            <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_base_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
-            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_types_py.html">&#xbb; next</a>
+            <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
 </footer>
 </body>
 </html>
```

#### html2text {}

```diff
@@ -1,141 +1,136 @@
 
-****** Coverage for structlog_gcp/processors.py: 100% ******
+****** Coverage for structlog_gcp/errors.py: 100% ******
  ⁰  [Show/hide keyboard shortcuts]
 Shortcuts on this page
 r m x p   toggle line displays
 j k   next/prev highlighted chunk
 0   (zero) top of page
 1   (one) first highlighted chunk
 [ ]   prev/next file
 u   up to the index
 ?   show/hide this help
-***** 36 statements   36 run 0 missing 0 excluded 0 partial *****
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+***** 43 statements   43 run 0 missing 0 excluded 0 partial *****
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
 
 
-1# https://cloud.google.com/functions/docs/monitoring/
-logging#writing_structured_logs 
-2# https://cloud.google.com/logging/docs/agent/logging/configuration#process-
-payload 
-3# https://cloud.google.com/logging/docs/structured-logging#special-payload-
-fields 
-4 
-5import structlog.processors 
-6 
-7from .types import CLOUD_LOGGING_KEY, SOURCE_LOCATION_KEY 
+1import os 
+2 
+3import structlog 
+4from structlog.typing import EventDict, Processor, WrappedLogger 
+5 
+6from .types import CLOUD_LOGGING_KEY, ERROR_EVENT_TYPE, SOURCE_LOCATION_KEY 
+7 
 8 
-9 
-10class CoreCloudLogging: 
-11 """Initialize the Google Cloud Logging event message""" 
-12 
-13 def setup(self): 
-14 return [ 
-15 # If some value is in bytes, decode it to a unicode str. 
-16 structlog.processors.UnicodeDecoder(), 
-17 # Add a timestamp in ISO 8601 format. 
-18 structlog.processors.TimeStamper(fmt="iso"), 
-19 self.__call__, 
-20 ] 
-21 
-22 def __call__(self, logger, method_name, event_dict): 
-23 value = { 
-24 "message": event_dict.pop("event"), 
-25 "time": event_dict.pop("timestamp"), 
-26 } 
-27 
-28 event_dict[CLOUD_LOGGING_KEY] = value 
-29 return event_dict 
-30 
+9def add_service_context( 
+10 logger: WrappedLogger, method_name: str, event_dict: EventDict 
+11) -> EventDict: 
+12 """Add a service context in which an error has occurred. 
+13 
+14 This is part of the Error Reporting API, so it's only added when an error
+happens. 
+15 """ 
+16 
+17 event_type = event_dict[CLOUD_LOGGING_KEY].get("@type") 
+18 if event_type != ERROR_EVENT_TYPE: 
+19 return event_dict 
+20 
+21 service_context = { 
+22 # https://cloud.google.com/functions/docs/configuring/env-
+var#runtime_environment_variables_set_automatically 
+23 "service": os.environ.get("K_SERVICE", "unknown service"), 
+24 "version": os.environ.get("K_REVISION", "unknown version"), 
+25 } 
+26 
+27 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
+ServiceContext 
+28 event_dict[CLOUD_LOGGING_KEY]["serviceContext"] = service_context 
+29 
+30 return event_dict 
 31 
-32class FormatAsCloudLogging: 
-33 """Finalize the Google Cloud Logging event message and replace the logging
-event""" 
-34 
-35 def setup(self): 
-36 return [ 
-37 self.__call__, 
-38 structlog.processors.JSONRenderer(), 
-39 ] 
-40 
-41 def __call__(self, logger, method_name, event_dict): 
-42 event = event_dict.pop(CLOUD_LOGGING_KEY) 
-43 
-44 if event_dict: 
-45 event["logging.googleapis.com/labels"] = event_dict 
-46 
-47 return event 
-48 
-49 
-50class LogSeverity: 
-51 """Set the severity using the Google Cloud Logging severities""" 
-52 
-53 def __init__(self): 
-54 self.default = "notset" 
-55 
-56 # From Python's logging level to Google level 
-57 self.mapping = { 
-58 "notset": "DEFAULT", # The log entry has no assigned severity level. 
-59 "debug": "DEBUG", # Debug or trace information. 
-60 "info": "INFO", # Routine information, such as ongoing status or
-performance. 
-61 # "notice": "NOTICE", # Normal but significant events, such as start up,
-shut down, or a configuration change. 
-62 "warn": "WARNING", # Warning events might cause problems. 
-63 "warning": "WARNING", # Warning events might cause problems. 
-64 "error": "ERROR", # Error events are likely to cause problems. 
-65 "critical": "CRITICAL", # Critical events cause more severe problems or
-outages. 
-66 # "alert": "ALERT", # A person must take an action immediately. 
-67 # "emergency": "EMERGENCY", # One or more systems are unusable. 
-68 } 
-69 
-70 def setup(self): 
-71 return [ 
-72 # Add log level to event dict. 
-73 structlog.processors.add_log_level, 
-74 self.__call__, 
-75 ] 
-76 
-77 def __call__(self, logger, method_name, event_dict): 
-78 """Format a Python log level value as a GCP log severity. 
-79 
-80 See: https://cloud.google.com/logging/docs/reference/v2/rest/v2/
-LogEntry#LogSeverity 
-81 """ 
-82 
-83 log_level = event_dict.pop("level") 
-84 severity = self.mapping.get(log_level, self.default) 
+32 
+33class ReportException: 
+34 """Transform exception into a Google Cloud Error Reporting event.""" 
+35 
+36 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
+projects.events/report 
+37 # https://cloud.google.com/error-reporting/docs/formatting-error-
+messages#log-entry-examples 
+38 
+39 def __init__(self, log_level: str = "CRITICAL") -> None: 
+40 self.log_level = log_level 
+41 
+42 def setup(self) -> list[Processor]: 
+43 return [structlog.processors.format_exc_info, self] 
+44 
+45 def __call__( 
+46 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+47 ) -> EventDict: 
+48 exception = event_dict.pop("exception", None) 
+49 if exception is None: 
+50 return event_dict 
+51 
+52 event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE 
+53 event_dict[CLOUD_LOGGING_KEY]["severity"] = self.log_level 
+54 
+55 # https://cloud.google.com/error-reporting/docs/formatting-error-messages 
+56 message = event_dict[CLOUD_LOGGING_KEY]["message"] 
+57 error_message = f"{message}\n{exception}" 
+58 event_dict[CLOUD_LOGGING_KEY]["stack_trace"] = error_message 
+59 
+60 return event_dict 
+61 
+62 
+63class ReportError: 
+64 """Report to Google Cloud Error Reporting specific log severities 
+65 
+66 This class assumes the :ref:`.processors.CodeLocation` processor ran
+before. 
+67 """ 
+68 
+69 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
+projects.events/report 
+70 # https://cloud.google.com/error-reporting/docs/formatting-error-
+messages#log-entry-examples 
+71 
+72 def __init__(self, severities: list[str]) -> None: 
+73 self.severities = severities 
+74 
+75 def setup(self) -> list[Processor]: 
+76 return [self] 
+77 
+78 def _build_service_context(self) -> dict[str, str]: 
+79 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
+ServiceContext 
+80 service_context = { 
+81 # https://cloud.google.com/functions/docs/configuring/env-
+var#runtime_environment_variables_set_automatically 
+82 "service": os.environ.get("K_SERVICE", "unknown service"), 
+83 "version": os.environ.get("K_REVISION", "unknown version"), 
+84 } 
 85 
-86 event_dict[CLOUD_LOGGING_KEY]["severity"] = severity 
-87 return event_dict 
-88 
-89 
-90class CodeLocation: 
-91 """Inject the location of the logging message into the logs""" 
+86 return service_context 
+87 
+88 def __call__( 
+89 self, logger: WrappedLogger, method_name: str, event_dict: EventDict 
+90 ) -> EventDict: 
+91 severity = event_dict[CLOUD_LOGGING_KEY]["severity"] 
 92 
-93 def setup(self): 
-94 # Add callsite parameters. 
-95 call_site_proc = structlog.processors.CallsiteParameterAdder( 
-96 parameters=[ 
-97 structlog.processors.CallsiteParameter.PATHNAME, 
-98 structlog.processors.CallsiteParameter.MODULE, 
-99 structlog.processors.CallsiteParameter.FUNC_NAME, 
-100 structlog.processors.CallsiteParameter.LINENO, 
-101 ] 
-102 ) 
-103 return [call_site_proc, self.__call__] 
+93 if severity not in self.severities: 
+94 return event_dict 
+95 
+96 # https://cloud.google.com/error-reporting/reference/rest/v1beta1/
+ErrorContext 
+97 error_context = { 
+98 "reportLocation": event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY], 
+99 } 
+100 
+101 event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE 
+102 event_dict[CLOUD_LOGGING_KEY]["context"] = error_context 
+103 event_dict[CLOUD_LOGGING_KEY]["serviceContext"] =
+self._build_service_context() 
 104 
-105 def __call__(self, logger, method_name, event_dict): 
-106 location = { 
-107 "file": event_dict.pop("pathname"), 
-108 "line": str(event_dict.pop("lineno")), 
-109 "function": f"{event_dict.pop('module')}:{event_dict.pop('func_name')}", 
-110 } 
-111 
-112 event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY] = location 
-113 
-114 return event_dict 
+105 return event_dict 
 
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
```

### Comparing `structlog_gcp-0.0.3/htmlcov/d_3c47d5ccd311be76_types_py.html` & `structlog_gcp-0.1.0/htmlcov/d_3c47d5ccd311be76_types_py.html`

 * *Files 2% similar despite different names*

```diff
@@ -62,16 +62,16 @@
             <button type="button" class="par run show_par button_toggle_par" value="par" data-shortcut="p" title="Toggle lines partially run">0<span class="text"> partial</span></button>
         </h2>
         <p class="text">
             <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
             <a id="nextFileLink" class="nav" href="index.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
         <aside class="hidden">
             <button type="button" class="button_next_chunk" data-shortcut="j"/>
             <button type="button" class="button_prev_chunk" data-shortcut="k"/>
             <button type="button" class="button_top_of_page" data-shortcut="0"/>
             <button type="button" class="button_first_chunk" data-shortcut="1"/>
             <button type="button" class="button_prev_file" data-shortcut="["/>
@@ -93,14 +93,14 @@
 <footer>
     <div class="content">
         <p>
             <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_processors_py.html">&#xab; prev</a> &nbsp; &nbsp;
             <a id="indexLink" class="nav" href="index.html">&Hat; index</a> &nbsp; &nbsp;
             <a id="nextFileLink" class="nav" href="index.html">&#xbb; next</a>
             &nbsp; &nbsp; &nbsp;
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
 </footer>
 </body>
 </html>
```

#### html2text {}

```diff
@@ -6,22 +6,22 @@
 j k   next/prev highlighted chunk
 0   (zero) top of page
 1   (one) first highlighted chunk
 [ ]   prev/next file
 u   up to the index
 ?   show/hide this help
 ***** 3 statements   3 run 0 missing 0 excluded 0 partial *****
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
 
 
 1ERROR_EVENT_TYPE = ( 
 2 "type.googleapis.com/
 google.devtools.clouderrorreporting.v1beta1.ReportedErrorEvent" 
 3) 
 4 
 5SOURCE_LOCATION_KEY = "logging.googleapis.com/sourceLocation" 
 6 
 7CLOUD_LOGGING_KEY = "cloud-logging" 
 
-&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.2, created
-at 2023-04-02 11:04 +0000
+&#xab;_prev     &Hat;_index     &#xbb;_next       coverage.py_v7.2.5, created
+at 2023-05-13 18:00 +0000
```

### Comparing `structlog_gcp-0.0.3/htmlcov/favicon_32.png` & `structlog_gcp-0.1.0/htmlcov/favicon_32.png`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/htmlcov/index.html` & `structlog_gcp-0.1.0/htmlcov/index.html`

 * *Files 9% similar despite different names*

```diff
@@ -7,15 +7,15 @@
     <link rel="stylesheet" href="style.css" type="text/css">
     <script type="text/javascript" src="coverage_html.js" defer></script>
 </head>
 <body class="indexfile">
 <header>
     <div class="content">
         <h1>Coverage report:
-            <span class="pc_cov">96%</span>
+            <span class="pc_cov">100%</span>
         </h1>
         <aside id="help_panel_wrapper">
             <input id="help_panel_state" type="checkbox">
             <label for="help_panel_state">
                 <img id="keyboard_icon" src="keybd_closed.png" alt="Show/hide keyboard shortcuts" />
             </label>
             <div id="help_panel">
@@ -42,16 +42,16 @@
                 </div>
             </div>
         </aside>
         <form id="filter_container">
             <input id="filter" type="text" value="" placeholder="filter..." />
         </form>
         <p class="text">
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
 </header>
 <main id="index">
     <table class="index" data-sortable>
         <thead>
             <tr class="tablehead" title="Click to sort">
@@ -63,79 +63,79 @@
                 <th aria-sort="none" data-default-sort-order="descending" data-shortcut="p">partial</th>
                 <th class="right" aria-sort="none" data-shortcut="c">coverage</th>
             </tr>
         </thead>
         <tbody>
             <tr class="file">
                 <td class="name left"><a href="d_3c47d5ccd311be76___init___py.html">structlog_gcp/__init__.py</a></td>
-                <td>1</td>
+                <td>2</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
-                <td class="right" data-ratio="1 1">100%</td>
+                <td class="right" data-ratio="2 2">100%</td>
             </tr>
             <tr class="file">
                 <td class="name left"><a href="d_3c47d5ccd311be76_base_py.html">structlog_gcp/base.py</a></td>
-                <td>14</td>
+                <td>12</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
-                <td class="right" data-ratio="14 14">100%</td>
+                <td class="right" data-ratio="12 12">100%</td>
             </tr>
             <tr class="file">
                 <td class="name left"><a href="d_3c47d5ccd311be76_errors_py.html">structlog_gcp/errors.py</a></td>
-                <td>47</td>
-                <td>2</td>
+                <td>43</td>
                 <td>0</td>
-                <td>10</td>
-                <td>2</td>
-                <td class="right" data-ratio="53 57">93%</td>
+                <td>0</td>
+                <td>6</td>
+                <td>0</td>
+                <td class="right" data-ratio="49 49">100%</td>
             </tr>
             <tr class="file">
                 <td class="name left"><a href="d_3c47d5ccd311be76_processors_py.html">structlog_gcp/processors.py</a></td>
-                <td>36</td>
+                <td>37</td>
                 <td>0</td>
                 <td>0</td>
                 <td>2</td>
                 <td>0</td>
-                <td class="right" data-ratio="38 38">100%</td>
+                <td class="right" data-ratio="39 39">100%</td>
             </tr>
             <tr class="file">
                 <td class="name left"><a href="d_3c47d5ccd311be76_types_py.html">structlog_gcp/types.py</a></td>
                 <td>3</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
                 <td>0</td>
                 <td class="right" data-ratio="3 3">100%</td>
             </tr>
         </tbody>
         <tfoot>
             <tr class="total">
                 <td class="name left">Total</td>
-                <td>101</td>
-                <td>2</td>
+                <td>97</td>
                 <td>0</td>
-                <td>12</td>
-                <td>2</td>
-                <td class="right" data-ratio="109 113">96%</td>
+                <td>0</td>
+                <td>8</td>
+                <td>0</td>
+                <td class="right" data-ratio="105 105">100%</td>
             </tr>
         </tfoot>
     </table>
     <p id="no_rows">
         No items found using the specified filter.
     </p>
 </main>
 <footer>
     <div class="content">
         <p>
-            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.2">coverage.py v7.2.2</a>,
-            created at 2023-04-02 11:04 +0000
+            <a class="nav" href="https://coverage.readthedocs.io/en/7.2.5">coverage.py v7.2.5</a>,
+            created at 2023-05-13 18:00 +0000
         </p>
     </div>
     <aside class="hidden">
         <a id="prevFileLink" class="nav" href="d_3c47d5ccd311be76_types_py.html"/>
         <a id="nextFileLink" class="nav" href="d_3c47d5ccd311be76___init___py.html"/>
         <button type="button" class="button_prev_file" data-shortcut="["/>
         <button type="button" class="button_next_file" data-shortcut="]"/>
```

#### html2text {}

```diff
@@ -1,22 +1,22 @@
 
-****** Coverage report: 96% ******
+****** Coverage report: 100% ******
  ⁰  [Show/hide keyboard shortcuts]
 Shortcuts on this page
 n s m x b p c   change column sorting
 [ ]   prev/next file
 ?   show/hide this help
 [                    ]
-coverage.py_v7.2.2, created at 2023-04-02 11:04 +0000
+coverage.py_v7.2.5, created at 2023-05-13 18:00 +0000
 
 Module                    statements missing excluded branches partial coverage
-structlog_gcp/__init__.py 1          0       0        0        0       100%
-structlog_gcp/base.py     14         0       0        0        0       100%
-structlog_gcp/errors.py   47         2       0        10       2       93%
-structlog_gcp/            36         0       0        2        0       100%
+structlog_gcp/__init__.py 2          0       0        0        0       100%
+structlog_gcp/base.py     12         0       0        0        0       100%
+structlog_gcp/errors.py   43         0       0        6        0       100%
+structlog_gcp/            37         0       0        2        0       100%
 processors.py
 structlog_gcp/types.py    3          0       0        0        0       100%
-Total                     101        2       0        12       2       96%
+Total                     97         0       0        8        0       100%
 No items found using the specified filter.
 
-coverage.py_v7.2.2, created at 2023-04-02 11:04 +0000
+coverage.py_v7.2.5, created at 2023-05-13 18:00 +0000
  ____
```

### Comparing `structlog_gcp-0.0.3/htmlcov/keybd_closed.png` & `structlog_gcp-0.1.0/htmlcov/keybd_closed.png`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/htmlcov/keybd_open.png` & `structlog_gcp-0.1.0/htmlcov/keybd_open.png`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/htmlcov/status.json` & `structlog_gcp-0.1.0/htmlcov/status.json`

 * *Files 14% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.7367521367521368%*

 * *Differences: {"'files'": "{'d_3c47d5ccd311be76___init___py': {'hash': '014de9557f9883e08d31c8696a44a79c', "*

 * *            "'index': {'nums': {insert: [(2, 2)], delete: [1]}}}, 'd_3c47d5ccd311be76_base_py': "*

 * *            "{'hash': '85439c3859f84e39cfbb2cf25aca7db2', 'index': {'nums': {insert: [(2, 12)], "*

 * *            "delete: [2]}}}, 'd_3c47d5ccd311be76_errors_py': {'hash': "*

 * *            "'aea1226a3793fd3efc4d3d776c4e1355', 'index': {'nums': {insert: [(2, 43), (4, 0), (5, "*

 * *            "6), (6, 0), (7, 0)], delete: [7, 6,  […]*

```diff
@@ -1,68 +1,68 @@
 {
     "files": {
         "d_3c47d5ccd311be76___init___py": {
-            "hash": "40fcbb9414d97ef7a4b800f42b1936d9",
+            "hash": "014de9557f9883e08d31c8696a44a79c",
             "index": {
                 "html_filename": "d_3c47d5ccd311be76___init___py.html",
                 "nums": [
                     0,
                     1,
-                    1,
+                    2,
                     0,
                     0,
                     0,
                     0,
                     0
                 ],
                 "relative_filename": "structlog_gcp/__init__.py"
             }
         },
         "d_3c47d5ccd311be76_base_py": {
-            "hash": "edf5931536a6a7441e525598eb3bf391",
+            "hash": "85439c3859f84e39cfbb2cf25aca7db2",
             "index": {
                 "html_filename": "d_3c47d5ccd311be76_base_py.html",
                 "nums": [
                     0,
                     1,
-                    14,
+                    12,
                     0,
                     0,
                     0,
                     0,
                     0
                 ],
                 "relative_filename": "structlog_gcp/base.py"
             }
         },
         "d_3c47d5ccd311be76_errors_py": {
-            "hash": "6e768c31a9a9fbd4dad585a4e89a4781",
+            "hash": "aea1226a3793fd3efc4d3d776c4e1355",
             "index": {
                 "html_filename": "d_3c47d5ccd311be76_errors_py.html",
                 "nums": [
                     0,
                     1,
-                    47,
+                    43,
                     0,
-                    2,
-                    10,
-                    2,
-                    2
+                    0,
+                    6,
+                    0,
+                    0
                 ],
                 "relative_filename": "structlog_gcp/errors.py"
             }
         },
         "d_3c47d5ccd311be76_processors_py": {
-            "hash": "bb58299a26b4e9868fef108b908632b0",
+            "hash": "75815df2de852145b7b25ebcc493ae98",
             "index": {
                 "html_filename": "d_3c47d5ccd311be76_processors_py.html",
                 "nums": [
                     0,
                     1,
-                    36,
+                    37,
                     0,
                     0,
                     2,
                     0,
                     0
                 ],
                 "relative_filename": "structlog_gcp/processors.py"
@@ -83,10 +83,10 @@
                     0
                 ],
                 "relative_filename": "structlog_gcp/types.py"
             }
         }
     },
     "format": 2,
-    "globals": "9ea54f3e64e2b7c84ddaaec7d0a4323c",
-    "version": "7.2.2"
+    "globals": "ac529cbac2153880c2bc35dae3590af3",
+    "version": "7.2.5"
 }
```

### Comparing `structlog_gcp-0.0.3/htmlcov/style.css` & `structlog_gcp-0.1.0/htmlcov/style.css`

 * *Files 0% similar despite different names*

```diff
@@ -254,20 +254,18 @@
 
 #source p input:checked ~ .ctxs { padding: .25em .5em; overflow-y: scroll; max-height: 10.5em; }
 
 #source p label.ctx { color: #999; display: inline-block; padding: 0 .5em; font-size: .8333em; }
 
 @media (prefers-color-scheme: dark) { #source p label.ctx { color: #777; } }
 
-#source p .ctxs { display: block; max-height: 0; overflow-y: hidden; transition: all .2s; padding: 0 .5em; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Ubuntu, Cantarell, "Helvetica Neue", sans-serif; white-space: nowrap; background: #d0e8ff; border-radius: .25em; margin-right: 1.75em; }
+#source p .ctxs { display: block; max-height: 0; overflow-y: hidden; transition: all .2s; padding: 0 .5em; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Ubuntu, Cantarell, "Helvetica Neue", sans-serif; white-space: nowrap; background: #d0e8ff; border-radius: .25em; margin-right: 1.75em; text-align: right; }
 
 @media (prefers-color-scheme: dark) { #source p .ctxs { background: #056; } }
 
-#source p .ctxs span { display: block; text-align: right; }
-
 #index { font-family: SFMono-Regular, Menlo, Monaco, Consolas, monospace; font-size: 0.875em; }
 
 #index table.index { margin-left: -.5em; }
 
 #index td, #index th { text-align: right; width: 5em; padding: .25em .5em; border-bottom: 1px solid #eee; }
 
 @media (prefers-color-scheme: dark) { #index td, #index th { border-color: #333; } }
```

### Comparing `structlog_gcp-0.0.3/structlog_gcp/errors.py` & `structlog_gcp-0.1.0/structlog_gcp/errors.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,18 @@
 import os
 
 import structlog
+from structlog.typing import EventDict, Processor, WrappedLogger
 
 from .types import CLOUD_LOGGING_KEY, ERROR_EVENT_TYPE, SOURCE_LOCATION_KEY
 
 
-def add_service_context(logger, method_name, event_dict):
+def add_service_context(
+    logger: WrappedLogger, method_name: str, event_dict: EventDict
+) -> EventDict:
     """Add a service context in which an error has occurred.
 
     This is part of the Error Reporting API, so it's only added when an error happens.
     """
 
     event_type = event_dict[CLOUD_LOGGING_KEY].get("@type")
     if event_type != ERROR_EVENT_TYPE:
@@ -29,25 +32,23 @@
 
 class ReportException:
     """Transform exception into a Google Cloud Error Reporting event."""
 
     # https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report
     # https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples
 
-    def __init__(self, log_level="CRITICAL"):
+    def __init__(self, log_level: str = "CRITICAL") -> None:
         self.log_level = log_level
 
-    def setup(self):
-        return [
-            # structlog.processors.ExceptionRenderer(self.format_exception),
-            structlog.processors.format_exc_info,
-            self.__call__,
-        ]
+    def setup(self) -> list[Processor]:
+        return [structlog.processors.format_exc_info, self]
 
-    def __call__(self, logger, method_name, event_dict):
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
         exception = event_dict.pop("exception", None)
         if exception is None:
             return event_dict
 
         event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE
         event_dict[CLOUD_LOGGING_KEY]["severity"] = self.log_level
 
@@ -56,53 +57,49 @@
         error_message = f"{message}\n{exception}"
         event_dict[CLOUD_LOGGING_KEY]["stack_trace"] = error_message
 
         return event_dict
 
 
 class ReportError:
-    """Report to Google Cloud Error Reporting specific log severities"""
+    """Report to Google Cloud Error Reporting specific log severities
+
+    This class assumes the :ref:`.processors.CodeLocation` processor ran before.
+    """
 
     # https://cloud.google.com/error-reporting/reference/rest/v1beta1/projects.events/report
     # https://cloud.google.com/error-reporting/docs/formatting-error-messages#log-entry-examples
 
-    def __init__(self, severities=None):
-        if severities is None:
-            severities = []
-
+    def __init__(self, severities: list[str]) -> None:
         self.severities = severities
 
-    def setup(self):
-        return [self.__call__]
-
-    def _build_service_context(self):
-        import os
+    def setup(self) -> list[Processor]:
+        return [self]
 
+    def _build_service_context(self) -> dict[str, str]:
         # https://cloud.google.com/error-reporting/reference/rest/v1beta1/ServiceContext
         service_context = {
             # https://cloud.google.com/functions/docs/configuring/env-var#runtime_environment_variables_set_automatically
             "service": os.environ.get("K_SERVICE", "unknown service"),
             "version": os.environ.get("K_REVISION", "unknown version"),
         }
 
         return service_context
 
-    def __call__(self, logger, method_name, event_dict):
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
         severity = event_dict[CLOUD_LOGGING_KEY]["severity"]
 
         if severity not in self.severities:
             return event_dict
 
-        event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE
-
-        if SOURCE_LOCATION_KEY in event_dict[CLOUD_LOGGING_KEY]:
-            # https://cloud.google.com/error-reporting/reference/rest/v1beta1/ErrorContext
-            error_context = {
-                "reportLocation": event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY],
-            }
-            event_dict[CLOUD_LOGGING_KEY]["context"] = error_context
-        else:
-            event_dict[CLOUD_LOGGING_KEY]["context"] = "no location :("
+        # https://cloud.google.com/error-reporting/reference/rest/v1beta1/ErrorContext
+        error_context = {
+            "reportLocation": event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY],
+        }
 
+        event_dict[CLOUD_LOGGING_KEY]["@type"] = ERROR_EVENT_TYPE
+        event_dict[CLOUD_LOGGING_KEY]["context"] = error_context
         event_dict[CLOUD_LOGGING_KEY]["serviceContext"] = self._build_service_context()
 
         return event_dict
```

### Comparing `structlog_gcp-0.0.3/structlog_gcp/processors.py` & `structlog_gcp-0.1.0/structlog_gcp/processors.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,60 +1,63 @@
 # https://cloud.google.com/functions/docs/monitoring/logging#writing_structured_logs
 # https://cloud.google.com/logging/docs/agent/logging/configuration#process-payload
 # https://cloud.google.com/logging/docs/structured-logging#special-payload-fields
 
+
 import structlog.processors
+from structlog.typing import EventDict, Processor, WrappedLogger
 
 from .types import CLOUD_LOGGING_KEY, SOURCE_LOCATION_KEY
 
 
 class CoreCloudLogging:
     """Initialize the Google Cloud Logging event message"""
 
-    def setup(self):
+    def setup(self) -> list[Processor]:
         return [
             # If some value is in bytes, decode it to a unicode str.
             structlog.processors.UnicodeDecoder(),
             # Add a timestamp in ISO 8601 format.
             structlog.processors.TimeStamper(fmt="iso"),
-            self.__call__,
+            self,
         ]
 
-    def __call__(self, logger, method_name, event_dict):
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
         value = {
             "message": event_dict.pop("event"),
             "time": event_dict.pop("timestamp"),
         }
 
         event_dict[CLOUD_LOGGING_KEY] = value
         return event_dict
 
 
 class FormatAsCloudLogging:
     """Finalize the Google Cloud Logging event message and replace the logging event"""
 
-    def setup(self):
-        return [
-            self.__call__,
-            structlog.processors.JSONRenderer(),
-        ]
+    def setup(self) -> list[Processor]:
+        return [self, structlog.processors.JSONRenderer()]
 
-    def __call__(self, logger, method_name, event_dict):
-        event = event_dict.pop(CLOUD_LOGGING_KEY)
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
+        event: EventDict = event_dict.pop(CLOUD_LOGGING_KEY)
 
         if event_dict:
             event["logging.googleapis.com/labels"] = event_dict
 
         return event
 
 
 class LogSeverity:
     """Set the severity using the Google Cloud Logging severities"""
 
-    def __init__(self):
+    def __init__(self) -> None:
         self.default = "notset"
 
         # From Python's logging level to Google level
         self.mapping = {
             "notset": "DEFAULT",  # The log entry has no assigned severity level.
             "debug": "DEBUG",  # Debug or trace information.
             "info": "INFO",  # Routine information, such as ongoing status or performance.
@@ -63,22 +66,21 @@
             "warning": "WARNING",  # Warning events might cause problems.
             "error": "ERROR",  # Error events are likely to cause problems.
             "critical": "CRITICAL",  # Critical events cause more severe problems or outages.
             # "alert": "ALERT", # A person must take an action immediately.
             # "emergency": "EMERGENCY", #	One or more systems are unusable.
         }
 
-    def setup(self):
-        return [
-            # Add log level to event dict.
-            structlog.processors.add_log_level,
-            self.__call__,
-        ]
-
-    def __call__(self, logger, method_name, event_dict):
+    def setup(self) -> list[Processor]:
+        # Add log level to event dict.
+        return [structlog.processors.add_log_level, self]
+
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
         """Format a Python log level value as a GCP log severity.
 
         See: https://cloud.google.com/logging/docs/reference/v2/rest/v2/LogEntry#LogSeverity
         """
 
         log_level = event_dict.pop("level")
         severity = self.mapping.get(log_level, self.default)
@@ -86,27 +88,29 @@
         event_dict[CLOUD_LOGGING_KEY]["severity"] = severity
         return event_dict
 
 
 class CodeLocation:
     """Inject the location of the logging message into the logs"""
 
-    def setup(self):
+    def setup(self) -> list[Processor]:
         # Add callsite parameters.
         call_site_proc = structlog.processors.CallsiteParameterAdder(
             parameters=[
                 structlog.processors.CallsiteParameter.PATHNAME,
                 structlog.processors.CallsiteParameter.MODULE,
                 structlog.processors.CallsiteParameter.FUNC_NAME,
                 structlog.processors.CallsiteParameter.LINENO,
             ]
         )
-        return [call_site_proc, self.__call__]
+        return [call_site_proc, self]
 
-    def __call__(self, logger, method_name, event_dict):
+    def __call__(
+        self, logger: WrappedLogger, method_name: str, event_dict: EventDict
+    ) -> EventDict:
         location = {
             "file": event_dict.pop("pathname"),
             "line": str(event_dict.pop("lineno")),
             "function": f"{event_dict.pop('module')}:{event_dict.pop('func_name')}",
         }
 
         event_dict[CLOUD_LOGGING_KEY][SOURCE_LOCATION_KEY] = location
```

### Comparing `structlog_gcp-0.0.3/tests/conftest.py` & `structlog_gcp-0.1.0/tests/conftest.py`

 * *Files 18% similar despite different names*

```diff
@@ -18,13 +18,13 @@
             side_effect=fakes.CallsiteParameterAdder,
         ),
         patch("structlog.processors.TimeStamper", side_effect=fakes.TimeStamper),
         patch(
             "structlog.processors.format_exc_info", side_effect=fakes.format_exc_info
         ),
     ):
-        gcp_logs = structlog_gcp.StructlogGCP()
-        structlog.configure(processors=gcp_logs.build_processors())
+        processors = structlog_gcp.build_processors()
+        structlog.configure(processors=processors)
         logger = structlog.get_logger()
         yield logger
 
     structlog.reset_defaults()
```

### Comparing `structlog_gcp-0.0.3/tests/fakes.py` & `structlog_gcp-0.1.0/tests/fakes.py`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/tests/test_log.py` & `structlog_gcp-0.1.0/tests/test_log.py`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/LICENSE` & `structlog_gcp-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `structlog_gcp-0.0.3/README.md` & `structlog_gcp-0.1.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -37,17 +37,16 @@
 Then, configure `structlog` as usual, using the Structlog processors the package
 provides:
 
 ```python
 import structlog
 import structlog_gcp
 
-gcp_logs = structlog_gcp.StructlogGCP()
-
-structlog.configure(processors=gcp_logs.build_processors())
+processors = structlog_gcp.build_processors()
+structlog.configure(processors=processors)
 ```
 
 Then, you can use `structlog` as usual:
 
 ```python
 logger = structlog.get_logger().bind(arg1="something")
```

### Comparing `structlog_gcp-0.0.3/pyproject.toml` & `structlog_gcp-0.1.0/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -33,18 +33,19 @@
 
 [tool.hatch.version]
 path = "structlog_gcp/__about__.py"
 
 [tool.hatch.envs.default]
 dependencies = [
   "black",
+  "flake8",
   "isort",
+  "mypy",
   "pytest",
   "pytest-cov",
-  "flake8",
 ]
 
 [tool.hatch.envs.default.scripts]
 test = "pytest"
 
 [tool.pytest.ini_options]
 addopts = [
@@ -71,7 +72,10 @@
   "no cov",
   "if __name__ == .__main__.:",
   "if TYPE_CHECKING:",
 ]
 
 [tool.isort]
 profile = "black"
+
+[tool.mypy]
+strict = true
```

### Comparing `structlog_gcp-0.0.3/PKG-INFO` & `structlog_gcp-0.1.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: structlog-gcp
-Version: 0.0.3
+Version: 0.1.0
 Summary: A structlog set of processors to output as Google Cloud Logging format
 Project-URL: Documentation, https://github.com/multani/structlog-gcp#readme
 Project-URL: Issues, https://github.com/multani/structlog-gcp/issues
 Project-URL: Source, https://github.com/multani/structlog-gcp
 Author-email: Jonathan Ballet <jon@multani.info>
 License-Expression: MIT
 License-File: LICENSE
@@ -58,17 +58,16 @@
 Then, configure `structlog` as usual, using the Structlog processors the package
 provides:
 
 ```python
 import structlog
 import structlog_gcp
 
-gcp_logs = structlog_gcp.StructlogGCP()
-
-structlog.configure(processors=gcp_logs.build_processors())
+processors = structlog_gcp.build_processors()
+structlog.configure(processors=processors)
 ```
 
 Then, you can use `structlog` as usual:
 
 ```python
 logger = structlog.get_logger().bind(arg1="something")
```

