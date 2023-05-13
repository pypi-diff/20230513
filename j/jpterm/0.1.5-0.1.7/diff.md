# Comparing `tmp/jpterm-0.1.5.tar.gz` & `tmp/jpterm-0.1.7.tar.gz`

## Comparing `jpterm-0.1.5.tar` & `jpterm-0.1.7.tar`

### file list

```diff
@@ -1,98 +1,115 @@
--rw-r--r--   0        0        0      467 2020-02-02 00:00:00.000000 jpterm-0.1.5/.pre-commit-config.yaml
--rw-r--r--   0        0        0     2533 2020-02-02 00:00:00.000000 jpterm-0.1.5/CHANGELOG.md
--rw-r--r--   0        0        0      467 2020-02-02 00:00:00.000000 jpterm-0.1.5/config.yaml
--rw-r--r--   0        0        0      936 2020-02-02 00:00:00.000000 jpterm-0.1.5/.github/workflows/test.yml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/jpterm/__init__.py
--rw-r--r--   0        0        0     1283 2020-02-02 00:00:00.000000 jpterm-0.1.5/jpterm/cli.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/cell/LICENSE.txt
--rw-r--r--   0        0        0       24 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/cell/README.md
--rw-r--r--   0        0        0      985 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/cell/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/cell/txl_cell/__init__.py
--rw-r--r--   0        0        0     1120 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/cell/txl_cell/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/editors/LICENSE.txt
--rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/editors/README.md
--rw-r--r--   0        0        0     1001 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/editors/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/editors/txl_editors/__init__.py
--rw-r--r--   0        0        0     2647 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/editors/txl_editors/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/file_browser/LICENSE.txt
--rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/file_browser/README.md
--rw-r--r--   0        0        0     1030 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/file_browser/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/file_browser/txl_filebrowser/__init__.py
--rw-r--r--   0        0        0     5219 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/file_browser/txl_filebrowser/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/image_viewer/LICENSE.txt
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/image_viewer/README.md
--rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/image_viewer/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/image_viewer/txl_image_viewer/__init__.py
--rw-r--r--   0        0        0     1851 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/image_viewer/txl_image_viewer/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/LICENSE.txt
--rw-r--r--   0        0        0       32 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/README.md
--rw-r--r--   0        0        0     1043 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/__init__.py
--rw-r--r--   0        0        0     2515 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/components.py
--rw-r--r--   0        0        0     4316 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/footer.py
--rw-r--r--   0        0        0      249 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/header.py
--rw-r--r--   0        0        0      327 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/jpterm.css
--rw-r--r--   0        0        0      612 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/jpterm/txl_jpterm/main_area.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/launcher/LICENSE.txt
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/launcher/README.md
--rw-r--r--   0        0        0     1009 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/launcher/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/launcher/txl_launcher/__init__.py
--rw-r--r--   0        0        0     1319 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/launcher/txl_launcher/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_contents/LICENSE.txt
--rw-r--r--   0        0        0       32 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_contents/README.md
--rw-r--r--   0        0        0     1043 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_contents/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_contents/txl_local_contents/__init__.py
--rw-r--r--   0        0        0     1382 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_contents/txl_local_contents/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_terminals/LICENSE.txt
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_terminals/README.md
--rw-r--r--   0        0        0     1050 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_terminals/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_terminals/txl_local_terminals/__init__.py
--rw-r--r--   0        0        0     3381 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/local_terminals/txl_local_terminals/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook/LICENSE.txt
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook/README.md
--rw-r--r--   0        0        0     1037 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook/txl_notebook/__init__.py
--rw-r--r--   0        0        0      658 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook/txl_notebook/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_editor/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_editor/README.md
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_editor/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_editor/txl_notebook_editor/__init__.py
--rw-r--r--   0        0        0     2016 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_editor/txl_notebook_editor/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_viewer/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_viewer/README.md
--rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_viewer/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_viewer/txl_notebook_viewer/__init__.py
--rw-r--r--   0        0        0     5126 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/notebook_viewer/txl_notebook_viewer/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_contents/LICENSE.txt
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_contents/README.md
--rw-r--r--   0        0        0     1151 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_contents/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_contents/txl_remote_contents/__init__.py
--rw-r--r--   0        0        0     5431 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_contents/txl_remote_contents/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_terminals/LICENSE.txt
--rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_terminals/README.md
--rw-r--r--   0        0        0     1096 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_terminals/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_terminals/txl_remote_terminals/__init__.py
--rw-r--r--   0        0        0     3639 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/remote_terminals/txl_remote_terminals/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/terminal/LICENSE.txt
--rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/terminal/README.md
--rw-r--r--   0        0        0     1034 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/terminal/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/terminal/txl_terminal/__init__.py
--rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/terminal/txl_terminal/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/text_viewer/LICENSE.txt
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/text_viewer/README.md
--rw-r--r--   0        0        0     1027 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/text_viewer/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/text_viewer/txl_text_viewer/__init__.py
--rw-r--r--   0        0        0     2217 2020-02-02 00:00:00.000000 jpterm-0.1.5/plugins/text_viewer/txl_text_viewer/components.py
--rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/LICENSE.txt
--rw-r--r--   0        0        0       36 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/README.md
--rw-r--r--   0        0        0      934 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/pyproject.toml
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/txl/__init__.py
--rw-r--r--   0        0        0     1658 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/txl/app.py
--rw-r--r--   0        0        0     2233 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/txl/base.py
--rw-r--r--   0        0        0      761 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/txl/cli.py
--rw-r--r--   0        0        0      605 2020-02-02 00:00:00.000000 jpterm-0.1.5/txl/txl/hooks.py
--rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 jpterm-0.1.5/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 jpterm-0.1.5/LICENSE
--rw-r--r--   0        0        0     1753 2020-02-02 00:00:00.000000 jpterm-0.1.5/README.md
--rw-r--r--   0        0        0     2731 2020-02-02 00:00:00.000000 jpterm-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     2576 2020-02-02 00:00:00.000000 jpterm-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0      572 2020-02-02 00:00:00.000000 jpterm-0.1.7/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     3300 2020-02-02 00:00:00.000000 jpterm-0.1.7/CHANGELOG.md
+-rw-r--r--   0        0        0      467 2020-02-02 00:00:00.000000 jpterm-0.1.7/config.yaml
+-rw-r--r--   0        0        0      936 2020-02-02 00:00:00.000000 jpterm-0.1.7/.github/workflows/test.yml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/jpterm/__init__.py
+-rw-r--r--   0        0        0     1376 2020-02-02 00:00:00.000000 jpterm-0.1.7/jpterm/cli.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/cell/LICENSE.txt
+-rw-r--r--   0        0        0       24 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/cell/README.md
+-rw-r--r--   0        0        0      985 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/cell/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/cell/txl_cell/__init__.py
+-rw-r--r--   0        0        0     1121 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/cell/txl_cell/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/editors/LICENSE.txt
+-rw-r--r--   0        0        0       25 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/editors/README.md
+-rw-r--r--   0        0        0     1001 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/editors/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/editors/txl_editors/__init__.py
+-rw-r--r--   0        0        0     2648 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/editors/txl_editors/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/file_browser/LICENSE.txt
+-rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/file_browser/README.md
+-rw-r--r--   0        0        0     1030 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/file_browser/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/file_browser/txl_filebrowser/__init__.py
+-rw-r--r--   0        0        0     5220 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/file_browser/txl_filebrowser/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/image_viewer/LICENSE.txt
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/image_viewer/README.md
+-rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/image_viewer/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/image_viewer/txl_image_viewer/__init__.py
+-rw-r--r--   0        0        0     2238 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/image_viewer/txl_image_viewer/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/LICENSE.txt
+-rw-r--r--   0        0        0       32 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/README.md
+-rw-r--r--   0        0        0     1043 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/__init__.py
+-rw-r--r--   0        0        0     2516 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/components.py
+-rw-r--r--   0        0        0     4162 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/footer.py
+-rw-r--r--   0        0        0      249 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/header.py
+-rw-r--r--   0        0        0      327 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/jpterm.css
+-rw-r--r--   0        0        0      612 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/jpterm/txl_jpterm/main_area.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/launcher/LICENSE.txt
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/launcher/README.md
+-rw-r--r--   0        0        0     1009 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/launcher/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/launcher/txl_launcher/__init__.py
+-rw-r--r--   0        0        0     1320 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/launcher/txl_launcher/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_contents/LICENSE.txt
+-rw-r--r--   0        0        0       32 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_contents/README.md
+-rw-r--r--   0        0        0     1043 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_contents/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_contents/txl_local_contents/__init__.py
+-rw-r--r--   0        0        0     1347 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_contents/txl_local_contents/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/LICENSE.txt
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/README.md
+-rw-r--r--   0        0        0     1105 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/__init__.py
+-rw-r--r--   0        0        0      650 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/components.py
+-rw-r--r--   0        0        0     2823 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/connect.py
+-rw-r--r--   0        0        0     9369 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/driver.py
+-rw-r--r--   0        0        0     1922 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/kernelspec.py
+-rw-r--r--   0        0        0     4120 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/message.py
+-rw-r--r--   0        0        0     2930 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_kernels/txl_local_kernels/paths.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_terminals/LICENSE.txt
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_terminals/README.md
+-rw-r--r--   0        0        0     1050 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_terminals/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_terminals/txl_local_terminals/__init__.py
+-rw-r--r--   0        0        0     3382 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/local_terminals/txl_local_terminals/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook/LICENSE.txt
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook/README.md
+-rw-r--r--   0        0        0     1037 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook/txl_notebook/__init__.py
+-rw-r--r--   0        0        0      705 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook/txl_notebook/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_editor/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_editor/README.md
+-rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_editor/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_editor/txl_notebook_editor/__init__.py
+-rw-r--r--   0        0        0     2017 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_editor/txl_notebook_editor/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_viewer/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_viewer/README.md
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_viewer/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_viewer/txl_notebook_viewer/__init__.py
+-rw-r--r--   0        0        0     6481 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/notebook_viewer/txl_notebook_viewer/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_contents/LICENSE.txt
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_contents/README.md
+-rw-r--r--   0        0        0     1148 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_contents/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_contents/txl_remote_contents/__init__.py
+-rw-r--r--   0        0        0     4801 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_contents/txl_remote_contents/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/LICENSE.txt
+-rw-r--r--   0        0        0       32 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/README.md
+-rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/txl_remote_kernels/__init__.py
+-rw-r--r--   0        0        0      893 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/txl_remote_kernels/components.py
+-rw-r--r--   0        0        0     9026 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/txl_remote_kernels/driver.py
+-rw-r--r--   0        0        0     3126 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_kernels/txl_remote_kernels/message.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_terminals/LICENSE.txt
+-rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_terminals/README.md
+-rw-r--r--   0        0        0     1096 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_terminals/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_terminals/txl_remote_terminals/__init__.py
+-rw-r--r--   0        0        0     3813 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/remote_terminals/txl_remote_terminals/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/terminal/LICENSE.txt
+-rw-r--r--   0        0        0       35 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/terminal/README.md
+-rw-r--r--   0        0        0     1034 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/terminal/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/terminal/txl_terminal/__init__.py
+-rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/terminal/txl_terminal/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/text_viewer/LICENSE.txt
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/text_viewer/README.md
+-rw-r--r--   0        0        0     1027 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/text_viewer/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/text_viewer/txl_text_viewer/__init__.py
+-rw-r--r--   0        0        0     2299 2020-02-02 00:00:00.000000 jpterm-0.1.7/plugins/text_viewer/txl_text_viewer/components.py
+-rw-r--r--   0        0        0     1106 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/LICENSE.txt
+-rw-r--r--   0        0        0       36 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/README.md
+-rw-r--r--   0        0        0      938 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/pyproject.toml
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/txl/__init__.py
+-rw-r--r--   0        0        0     1659 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/txl/app.py
+-rw-r--r--   0        0        0     2266 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/txl/base.py
+-rw-r--r--   0        0        0      761 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/txl/cli.py
+-rw-r--r--   0        0        0      605 2020-02-02 00:00:00.000000 jpterm-0.1.7/txl/txl/hooks.py
+-rw-r--r--   0        0        0       12 2020-02-02 00:00:00.000000 jpterm-0.1.7/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 jpterm-0.1.7/LICENSE
+-rw-r--r--   0        0        0     1753 2020-02-02 00:00:00.000000 jpterm-0.1.7/README.md
+-rw-r--r--   0        0        0     3188 2020-02-02 00:00:00.000000 jpterm-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     2692 2020-02-02 00:00:00.000000 jpterm-0.1.7/PKG-INFO
```

### Comparing `jpterm-0.1.5/CHANGELOG.md` & `jpterm-0.1.7/CHANGELOG.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,32 @@
 # Changes in jpterm {#changelog}
 
 <!-- <START NEW CHANGELOG ENTRY> -->
 
+## 0.1.7
+
+No merged PRs
+
+<!-- <END NEW CHANGELOG ENTRY> -->
+
+## 0.1.6
+
+([Full Changelog](https://github.com/davidbrochart/jpterm/compare/v0.1.5...73f499d42b32c7b93ff3ee2728e6750fcbdef121))
+
+### Merged PRs
+
+- Pass ycell to kernel.execute() [#30](https://github.com/davidbrochart/jpterm/pull/30) ([@davidbrochart](https://github.com/davidbrochart))
+- Add kernel plugins [#27](https://github.com/davidbrochart/jpterm/pull/27) ([@davidbrochart](https://github.com/davidbrochart))
+
+### Contributors to this release
+
+([GitHub contributors page for this release](https://github.com/davidbrochart/jpterm/graphs/contributors?from=2023-01-08&to=2023-01-21&type=c))
+
+[@davidbrochart](https://github.com/search?q=repo%3Adavidbrochart%2Fjpterm+involves%3Adavidbrochart+updated%3A2023-01-08..2023-01-21&type=Issues)
+
 ## 0.1.5
 
 ([Full Changelog](https://github.com/davidbrochart/jpterm/compare/v0.1.4...007de833910667a3f57a5e3b9a52534da486d3e4))
 
 ### Merged PRs
 
 - Add image viewer plugin [#29](https://github.com/davidbrochart/jpterm/pull/29) ([@davidbrochart](https://github.com/davidbrochart))
@@ -15,16 +36,14 @@
 
 ### Contributors to this release
 
 ([GitHub contributors page for this release](https://github.com/davidbrochart/jpterm/graphs/contributors?from=2022-12-27&to=2023-01-08&type=c))
 
 [@davidbrochart](https://github.com/search?q=repo%3Adavidbrochart%2Fjpterm+involves%3Adavidbrochart+updated%3A2022-12-27..2023-01-08&type=Issues)
 
-<!-- <END NEW CHANGELOG ENTRY> -->
-
 ## 0.1.4
 
 ([Full Changelog](https://github.com/davidbrochart/jpterm/compare/v0.1.3...2b22def80c01327cbca14c857d4ac3a1e93b6782))
 
 ### Merged PRs
 
 - Add launcher plugin [#23](https://github.com/davidbrochart/jpterm/pull/23) ([@davidbrochart](https://github.com/davidbrochart))
```

### Comparing `jpterm-0.1.5/.github/workflows/test.yml` & `jpterm-0.1.7/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/jpterm/cli.py` & `jpterm-0.1.7/jpterm/cli.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,24 +1,28 @@
 import rich_click as click
+
 from txl.cli import set_main, txl_main
 
 
 def jpterm_main(kwargs):
     server = kwargs.pop("server")
     collaborative = kwargs.pop("collaborative")
     set_ = list(kwargs["set_"])
+    locals = "[txl_local_contents,txl_local_terminals,txl_local_kernels]"
+    remotes = "[txl_remote_contents,txl_remote_terminals,txl_remote_kernels]"
     if server:
-        set_.append("component.disable=[txl_local_contents,txl_local_terminals]")
-        set_.append("component.enable=[txl_remote_contents,txl_remote_terminals]")
+        set_.append(f"component.disable={locals}")
+        set_.append(f"component.enable={remotes}")
         set_.append(f"component.components.contents.url={server}")
-        set_.append(f"component.components.contents.collaborative={collaborative}")
         set_.append(f"component.components.terminals.url={server}")
+        set_.append(f"component.components.kernels.url={server}")
+        set_.append(f"component.components.contents.collaborative={collaborative}")
     else:
-        set_.append("component.disable=[txl_remote_contents,txl_remote_terminals]")
-        set_.append("component.enable=[txl_local_contents,txl_local_terminals]")
+        set_.append(f"component.disable={remotes}")
+        set_.append(f"component.enable={locals}")
     kwargs["set_"] = set_
     return kwargs
 
 
 def main():
     set_main(jpterm_main)
     decorators = [
```

### Comparing `jpterm-0.1.5/plugins/cell/LICENSE.txt` & `jpterm-0.1.7/plugins/cell/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/cell/pyproject.toml` & `jpterm-0.1.7/plugins/cell/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/cell/txl_cell/components.py` & `jpterm-0.1.7/plugins/cell/txl_cell/components.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from typing import Any, Dict, List
 
 from asphalt.core import Component, Context
+
 from txl.base import Cell, CellFactory
 from txl.hooks import register_component
 
 
 class _Cell(Cell):
     """A cell."""
```

### Comparing `jpterm-0.1.5/plugins/editors/LICENSE.txt` & `jpterm-0.1.7/plugins/editors/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/editors/pyproject.toml` & `jpterm-0.1.7/plugins/editors/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/editors/txl_editors/components.py` & `jpterm-0.1.7/plugins/editors/txl_editors/components.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from pathlib import Path
 from typing import Callable, Dict, List
 
 from asphalt.core import Component, Context
 from textual.containers import Container
 from textual.widgets._header import HeaderTitle
+
 from txl.base import Editor, Editors, FileOpenEvent, Footer, Header, MainArea
 from txl.hooks import register_component
 
 
 class EditorsMeta(type(Editors), type(Container)):
     pass
```

### Comparing `jpterm-0.1.5/plugins/file_browser/LICENSE.txt` & `jpterm-0.1.7/plugins/file_browser/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/file_browser/pyproject.toml` & `jpterm-0.1.7/plugins/file_browser/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/file_browser/txl_filebrowser/components.py` & `jpterm-0.1.7/plugins/file_browser/txl_filebrowser/components.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,20 @@
 from __future__ import annotations
 
-from dataclasses import dataclass
 import os.path
+from dataclasses import dataclass
 from typing import ClassVar
 
 from asphalt.core import Component, Context
 from rich.style import Style
 from rich.text import Text, TextType
-from textual.message import Message
 from textual._types import MessageTarget
-from textual.widgets._tree import Tree, TreeNode, TOGGLE_STYLE
+from textual.message import Message
+from textual.widgets._tree import TOGGLE_STYLE, Tree, TreeNode
+
 from txl.base import Contents, FileBrowser
 from txl.hooks import register_component
 
 
 @dataclass
 class DirEntry:
     path: str
```

### Comparing `jpterm-0.1.5/plugins/image_viewer/LICENSE.txt` & `jpterm-0.1.7/plugins/image_viewer/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/image_viewer/pyproject.toml` & `jpterm-0.1.7/plugins/image_viewer/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/image_viewer/txl_image_viewer/components.py` & `jpterm-0.1.7/plugins/image_viewer/txl_image_viewer/components.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 import os
 import tempfile
 
 from asphalt.core import Component, Context
 from PIL import Image
-from textual_imageview.viewer import ImageViewer
 from textual.widget import Widget
-from txl.base import Editor, Editors, Contents, FileOpenEvent
+from textual_imageview.viewer import ImageViewer
+
+from txl.base import Contents, Editor, Editors, FileOpenEvent
 from txl.hooks import register_component
 
 
 class ImageViewerMeta(type(Editor), type(Widget)):
     pass
 
 
@@ -17,32 +18,43 @@
 
     contents: Contents
     path: str
 
     def __init__(self, contents: Contents) -> None:
         super().__init__()
         self.contents = contents
+        self.image_viewer = None
 
     async def on_open(self, event: FileOpenEvent) -> None:
         await self.open(event.path)
 
     async def open(self, path: str) -> None:
-        data = await self.contents.get(path, type="bytes", on_change=self.on_change)
+        self.ydoc = await self.contents.get(path, type="blob")
+        self.data = self.ydoc.source
+        self.update_viewer()
+        self.ydoc.observe(self.on_change)
+
+    def update_viewer(self):
+        if not self.data:
+            return
         f = tempfile.NamedTemporaryFile(delete=False)
         try:
-            f.write(data)
+            f.write(self.data)
             f.close()
         finally:
             image = Image.open(f.name)
             os.unlink(f.name)
-        image_viewer = ImageViewer(image)
-        self.mount(image_viewer)
-
-    def on_change(self, value):
-        pass
+        if self.image_viewer:
+            self.image_viewer.remove()
+        self.image_viewer = ImageViewer(image)
+        self.mount(self.image_viewer)
+
+    def on_change(self, target, event):
+        self.data = self.ydoc.source
+        self.update_viewer()
 
 
 class ImageViewerComponent(Component):
     def __init__(self, register: bool = True):
         super().__init__()
         self.register = register
 
@@ -53,14 +65,16 @@
         contents = await ctx.request_resource(Contents, "contents")
 
         def image_viewer_factory():
             return _ImageViewer(contents)
 
         if self.register:
             editors = await ctx.request_resource(Editors, "editors")
-            editors.register_editor_factory(image_viewer_factory, [".png"])
+            editors.register_editor_factory(
+                image_viewer_factory, [".png", ".jpg", ".jpeg"]
+            )
         else:
             image_viewer = image_viewer_factory()
             ctx.add_resource(image_viewer, name="image_viewer", types=Editor)
 
 
 c = register_component("image_viewer", ImageViewerComponent)
```

### Comparing `jpterm-0.1.5/plugins/jpterm/LICENSE.txt` & `jpterm-0.1.7/plugins/jpterm/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/jpterm/pyproject.toml` & `jpterm-0.1.7/plugins/jpterm/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/jpterm/txl_jpterm/components.py` & `jpterm-0.1.7/plugins/jpterm/txl_jpterm/components.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from asphalt.core import Component, Context
 from textual.app import App, ComposeResult
 from textual.containers import Container
 from textual.reactive import var
-from txl.base import Editors, FileBrowser, Launcher, Footer, Header, MainArea
+
+from txl.base import Editors, FileBrowser, Footer, Header, Launcher, MainArea
 from txl.hooks import register_component
 
 from .footer import Footer as _Footer
 from .header import Header as _Header
 from .main_area import MainArea as _MainArea
```

### Comparing `jpterm-0.1.5/plugins/jpterm/txl_jpterm/footer.py` & `jpterm-0.1.7/plugins/jpterm/txl_jpterm/footer.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 from __future__ import annotations
 
 from collections import defaultdict
 
 import rich.repr
 from rich.console import RenderableType
 from rich.text import Text
-
 from textual import events
 from textual.reactive import Reactive, watch
 from textual.widget import Widget
 
 from txl.base import Footer as AbstractFooter
 
 
@@ -126,19 +125,14 @@
                     else binding.action,
                     "key": binding.key,
                 },
             )
             text.append_text(key_text)
         return text
 
-    def update_bindings(self, bindings) -> None:
-        self._bindings = bindings
-        self._key_text = self.make_key_text()
-        self.refresh()
-
     def post_render(self, renderable):
         return renderable
 
     def render(self) -> RenderableType:
         if self._key_text is None:
             self._key_text = self.make_key_text()
         return self._key_text
```

### Comparing `jpterm-0.1.5/plugins/jpterm/txl_jpterm/main_area.py` & `jpterm-0.1.7/plugins/jpterm/txl_jpterm/main_area.py`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/launcher/LICENSE.txt` & `jpterm-0.1.7/plugins/launcher/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/launcher/pyproject.toml` & `jpterm-0.1.7/plugins/launcher/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/launcher/txl_launcher/components.py` & `jpterm-0.1.7/plugins/launcher/txl_launcher/components.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from asphalt.core import Component, Context
 from textual.widget import Widget
 from textual.widgets import Button
+
 from txl.base import Launcher, MainArea
 from txl.hooks import register_component
 
 
 class LauncherMeta(type(Launcher), type(Widget)):
     pass
```

### Comparing `jpterm-0.1.5/plugins/local_contents/LICENSE.txt` & `jpterm-0.1.7/plugins/local_contents/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/local_contents/pyproject.toml` & `jpterm-0.1.7/plugins/local_contents/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/local_terminals/LICENSE.txt` & `jpterm-0.1.7/plugins/local_kernels/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/local_terminals/pyproject.toml` & `jpterm-0.1.7/plugins/local_terminals/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/local_terminals/txl_local_terminals/components.py` & `jpterm-0.1.7/plugins/local_terminals/txl_local_terminals/components.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,15 +5,16 @@
 import shlex
 import struct
 import termios
 
 from asphalt.core import Component, Context
 from textual.widget import Widget
 from textual.widgets._header import HeaderTitle
-from txl.base import Terminals, TerminalFactory, Header, Launcher
+
+from txl.base import Header, Launcher, TerminalFactory, Terminals
 from txl.hooks import register_component
 
 
 class TerminalsMeta(type(Terminals), type(Widget)):
     pass
```

### Comparing `jpterm-0.1.5/plugins/notebook/LICENSE.txt` & `jpterm-0.1.7/plugins/local_terminals/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/notebook/pyproject.toml` & `jpterm-0.1.7/plugins/notebook/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
-  "jupyter_ydoc >=0.3.0a1"
+  "jupyter_ydoc >=0.3.0a4"
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/notebook"
 
 [project.entry-points.txl_component]
```

### Comparing `jpterm-0.1.5/plugins/notebook_editor/LICENSE.txt` & `jpterm-0.1.7/plugins/notebook/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/notebook_editor/pyproject.toml` & `jpterm-0.1.7/plugins/notebook_editor/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/notebook_editor/txl_notebook_editor/components.py` & `jpterm-0.1.7/plugins/notebook_editor/txl_notebook_editor/components.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from asphalt.core import Component, Context
 from textual.binding import Binding
 from textual.containers import Container
-from txl.base import CellFactory, Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import CellFactory, Contents, Editor, Editors, FileOpenEvent
 from txl.hooks import register_component
 
 
 class NotebookEditorMeta(type(Editor), type(Container)):
     pass
```

### Comparing `jpterm-0.1.5/plugins/notebook_viewer/LICENSE.txt` & `jpterm-0.1.7/plugins/notebook_editor/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/notebook_viewer/pyproject.toml` & `jpterm-0.1.7/plugins/notebook_viewer/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/notebook_viewer/txl_notebook_viewer/components.py` & `jpterm-0.1.7/plugins/notebook_viewer/txl_notebook_viewer/components.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 from typing import Optional, Tuple
 
 from asphalt.core import Component, Context
 from rich.markdown import Markdown
 from rich.panel import Panel
 from rich.syntax import Syntax
 from rich.text import Text
+from textual import events
 from textual.widgets import DataTable
-from txl.base import Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import Contents, Editor, Editors, FileOpenEvent, Kernels, NotebookFactory
 from txl.hooks import register_component
 
 
 def _line_range(
     head: Optional[int], tail: Optional[int], num_lines: int
 ) -> Optional[Tuple[int, int]]:
     if head and tail:
@@ -27,41 +29,56 @@
 
 
 class NotebookViewerMeta(type(Editor), type(DataTable)):
     pass
 
 
 class NotebookViewer(Editor, DataTable, metaclass=NotebookViewerMeta):
-    def __init__(self, contents: Contents) -> None:
+    def __init__(
+        self, contents: Contents, notebook: NotebookFactory, kernels: Kernels
+    ) -> None:
         super().__init__()
         self.contents = contents
+        self.notebook = notebook
+        self.kernels = kernels
+        self.kernel = None
+        self._row_to_cell_idx = []
+        self._selected_cell_idx = None
 
     async def on_open(self, event: FileOpenEvent) -> None:
         await self.open(event.path)
 
     async def open(self, path: str) -> None:
-        self.nb = await self.contents.get(path, type="json", on_change=self.on_change)
+        self.ynb = await self.contents.get(path, type="notebook")
+        ipynb = self.ynb.source
+        self.language = (
+            ipynb.get("metadata", {}).get("kernelspec", {}).get("language", "")
+        )
+        kernel_name = ipynb.get("metadata", {}).get("kernelspec", {}).get("name")
+        if kernel_name:
+            self.kernel = self.kernels(kernel_name)
         self.update_viewer()
+        self.ynb.observe(self.on_change)
 
     def update_viewer(self):
+        self.clear()
+
         self.add_column("", width=10)
         self.add_column("", width=100)
 
         head = None
         tail = None
-        lexer = None
-        lexer = lexer or self.nb.get("metadata", {}).get("kernelspec", {}).get(
-            "language", ""
-        )
         theme = "ansi_dark"
 
-        if "cells" not in self.nb:
+        if self.ynb.cell_number == 0:
             return
 
-        for cell in self.nb["cells"]:
+        self._row_to_cell_idx = []
+        for i_cell in range(self.ynb.cell_number):
+            cell = self.ynb.get_cell(i_cell)
             execution_count = (
                 f"[green]In [[#66ff00]{cell['execution_count'] or ' '}"
                 "[/#66ff00]]:[/green]"
                 if "execution_count" in cell
                 else ""
             )
 
@@ -70,15 +87,15 @@
             if cell["cell_type"] == "code":
                 if execution_count:
                     execution_count = "\n" + execution_count
                 line_range = _line_range(head, tail, num_lines)
                 renderable = Panel(
                     Syntax(
                         source,
-                        lexer,
+                        self.language,
                         theme=theme,
                         line_numbers=True,
                         indent_guides=True,
                         word_wrap=False,
                         line_range=line_range,
                     ),
                     border_style="dim",
@@ -86,14 +103,15 @@
                 num_lines += 2
             elif cell["cell_type"] == "markdown":
                 renderable = Markdown(source, code_theme=theme, hyperlinks=True)
             else:
                 renderable = Text(source)
 
             self.add_row(execution_count, renderable, height=num_lines)
+            self._row_to_cell_idx.append(i_cell)
 
             for output in cell.get("outputs", []):
                 output_type = output["output_type"]
                 execution_count = ""
                 if output_type == "stream":
                     text = "".join(output["text"])
                     renderable = Text.from_ansi(text)
@@ -114,34 +132,48 @@
                         text = data
                         renderable += Text.from_ansi(text)
                 else:
                     continue
 
                 num_lines = len(text.splitlines())
                 self.add_row(execution_count, renderable, height=num_lines)
+                self._row_to_cell_idx.append(i_cell)
 
-    def on_change(self, nb):
-        self.nb = nb
-        self.clear()
+    def on_click(self, event: events.Click) -> None:
+        DataTable.on_click(self, event)
+        if self.show_cursor and self.cursor_type != "none":
+            meta = self.get_style_at(event.x, event.y).meta
+            if meta:
+                self._selected_cell_idx = self._row_to_cell_idx[meta["row"]]
+
+    def on_change(self, target, event):
         self.update_viewer()
 
+    async def key_e(self) -> None:
+        if self.kernel:
+            ycell = self.ynb._ycells[self._selected_cell_idx]
+            await self.kernel.execute(self.ynb.ydoc, ycell)
+            print(f"Executed {ycell}")
+
 
 class NotebookViewerComponent(Component):
     def __init__(self, register: bool = True):
         super().__init__()
         self.register = register
 
     async def start(
         self,
         ctx: Context,
     ) -> None:
         contents = await ctx.request_resource(Contents, "contents")
+        notebook = await ctx.request_resource(NotebookFactory, "notebook")
+        kernels = await ctx.request_resource(Kernels, "kernels")
 
         def notebook_viewer_factory():
-            return NotebookViewer(contents)
+            return NotebookViewer(contents, notebook, kernels)
 
         if self.register:
             editors = await ctx.request_resource(Editors, "editors")
             editors.register_editor_factory(notebook_viewer_factory, [".ipynb"])
         else:
             notebook_viewer = notebook_viewer_factory()
             ctx.add_resource(notebook_viewer, name="notebook_viewer", types=Editor)
```

### Comparing `jpterm-0.1.5/plugins/remote_contents/LICENSE.txt` & `jpterm-0.1.7/plugins/notebook_viewer/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/remote_contents/pyproject.toml` & `jpterm-0.1.7/plugins/remote_contents/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -22,17 +22,17 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
   "httpx>=0.23.1",
-  "httpx-ws>=0.2.4",
-  "jupyter_ydoc >=0.3.0a1,<1",
-  "ypy-websocket >=0.3.2,<1",
+  "httpx-ws>=0.2.6",
+  "jupyter_ydoc >=0.3.0a4",
+  "ypy-websocket >=0.8.2,<1",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/remote_contents"
 
 [project.entry-points.txl_component]
```

### Comparing `jpterm-0.1.5/plugins/remote_contents/txl_remote_contents/components.py` & `jpterm-0.1.7/plugins/remote_contents/txl_remote_contents/components.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 import asyncio
-import base64
 import json
-from functools import partial
-from typing import Any, Callable, Dict, List, Optional, Union
+from typing import Any, Dict, List, Union
 from urllib import parse
 
 import httpx
 import y_py as Y
 from asphalt.core import Component, Context
 from httpx_ws import aconnect_ws
 from jupyter_ydoc import ydocs
+from ypy_websocket import WebsocketProvider
+
 from txl.base import Contents
 from txl.hooks import register_component
-from ypy_websocket import WebsocketProvider
 
 
 class Websocket:
     def __init__(self, websocket, roomid: str):
         self.websocket = websocket
         self.roomid = roomid
 
@@ -79,76 +78,63 @@
         i = base_url.find(":")
         self.ws_url = ("wss" if base_url[i - 1] == "s" else "ws") + base_url[i:]
 
     async def get(
         self,
         path: str,
         is_dir: bool = False,
-        type: str = "text",
-        on_change: Optional[Callable] = None,
-    ) -> Union[List, str, bytes, Dict[str, Any]]:
+        type: str = "unicode",
+    ) -> Union[List, Y.YDoc]:
         path = "" if path == "." else path
         if is_dir or not self.collaborative:
             async with httpx.AsyncClient() as client:
                 r = await client.get(
                     f"{self.base_url}/api/contents/{path}",
                     params={**{"content": 1}, **self.query_params},
                     cookies=self.cookies,
                 )
             self.cookies.update(r.cookies)
             model = r.json()
-            if model["type"] == "file":
-                document = model["content"]
-            elif model["type"] == "notebook":
-                document = model["content"]
-                if isinstance(model["content"], (str, bytes)):
-                    document = json.loads(model["content"])
-            elif model["type"] == "directory":
+            if model["type"] == "directory":
                 dir_list = [Entry(entry) for entry in model["content"]]
-                document = sorted(
+                return sorted(
                     dir_list, key=lambda entry: (not entry.is_dir(), entry.name)
                 )
-            if model["format"] == "base64":
-                document = document.encode()
-                document = base64.b64decode(document)
-            return document
+            document = model["content"]
+            if type == "notebook":
+                if isinstance(model["content"], (str, bytes)):
+                    # jupyverse doesn't return JSON
+                    document = json.loads(model["content"])
+            jupyter_ydoc = ydocs[type]()
+            jupyter_ydoc.source = document
+            return jupyter_ydoc
 
         else:
-            # it's a collaborative document
-            doc_format = "json" if path.endswith(".ipynb") else "text"
-            doc_type = "notebook" if path.endswith(".ipynb") else "file"
+            doc_format = {"blob": "base64"}.get(type, "text")
+            doc_type = type  # if type == "notebook" else "file"
             async with httpx.AsyncClient() as client:
                 r = await client.put(
                     f"{self.base_url}/api/yjs/roomid/{path}",
                     json={"format": doc_format, "type": doc_type},
                     params={**self.query_params},
                     cookies=self.cookies,
                 )
             self.cookies.update(r.cookies)
             roomid = r.text
             ydoc = Y.YDoc()
-            jupyter_ydoc = ydocs[doc_type](ydoc)
-            if on_change:
-                jupyter_ydoc.observe(partial(self.on_change, jupyter_ydoc, on_change))
+            jupyter_ydoc = ydocs[type](ydoc)
             asyncio.create_task(self._websocket_provider(roomid, ydoc))
-            if doc_type == "notebook":
-                return {}
-            else:
-                return ""
+            return jupyter_ydoc
 
     async def _websocket_provider(self, roomid, ydoc):
         ws_url = f"{self.ws_url}/api/yjs/{roomid}"
         async with aconnect_ws(ws_url, cookies=self.cookies) as websocket:
             WebsocketProvider(ydoc, Websocket(websocket, roomid))
             await asyncio.Future()
 
-    def on_change(self, jupyter_ydoc, on_change: Callable, events) -> None:
-        content = jupyter_ydoc.get()
-        on_change(content)
-
 
 class ContentsComponent(Component):
     def __init__(self, url: str = "http://127.0.0.1:8000", collaborative: bool = True):
         super().__init__()
         self.url = url
         self.collaborative = collaborative
```

### Comparing `jpterm-0.1.5/plugins/remote_terminals/LICENSE.txt` & `jpterm-0.1.7/plugins/remote_contents/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/remote_terminals/pyproject.toml` & `jpterm-0.1.7/plugins/remote_terminals/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -22,15 +22,15 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "txl",
   "httpx>=0.23.1",
-  "httpx-ws>=0.2.4",
+  "httpx-ws>=0.2.6",
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/plugins/remote_terminals"
 
 [project.entry-points.txl_component]
```

### Comparing `jpterm-0.1.5/plugins/remote_terminals/txl_remote_terminals/components.py` & `jpterm-0.1.7/plugins/remote_terminals/txl_remote_terminals/components.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 import asyncio
 from typing import Dict, List
+from urllib import parse
 
 import httpx
+import httpx_ws
 from asphalt.core import Component, Context
 from httpx_ws import aconnect_ws
 from textual.widget import Widget
 from textual.widgets._header import HeaderTitle
-from txl.base import TerminalFactory, Terminals, Header, Launcher
+
+from txl.base import Header, Launcher, TerminalFactory, Terminals
 from txl.hooks import register_component
-from urllib import parse
 
 
 class TerminalsMeta(type(Terminals), type(Widget)):
     pass
 
 
 class RemoteTerminals(Terminals, Widget, metaclass=TerminalsMeta):
@@ -56,29 +58,33 @@
             terminal.focus()
             await self.mount(terminal)
             terminal.set_size(self.size)
             async with aconnect_ws(
                 f"{self.ws_url}/terminals/websocket/{name}", cookies=self.cookies
             ) as self.websocket:
                 asyncio.create_task(self._recv())
-                asyncio.create_task(self._send())
+                self.send_task = asyncio.create_task(self._send())
                 await self._done.wait()
 
     async def _send(self):
         while True:
             message = await self._send_queue.get()
             try:
                 await self.websocket.send_json(message)
             except BaseException:
                 self._done.set()
                 break
 
     async def _recv(self):
         while True:
-            message = await self.websocket.receive_json()
+            try:
+                message = await self.websocket.receive_json()
+            except httpx_ws._api.WebSocketNetworkError:
+                self.send_task.cancel()
+                return
             await self._recv_queue.put(message)
 
 
 class RemoteTerminalsComponent(Component):
     def __init__(self, url: str = "http://127.0.0.1:8000"):
         super().__init__()
         self.url = url
```

### Comparing `jpterm-0.1.5/plugins/terminal/LICENSE.txt` & `jpterm-0.1.7/plugins/remote_kernels/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/terminal/pyproject.toml` & `jpterm-0.1.7/plugins/terminal/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/terminal/txl_terminal/components.py` & `jpterm-0.1.7/plugins/terminal/txl_terminal/components.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 
 import pyte
 from asphalt.core import Component, Context
 from rich.console import RenderableType
 from rich.text import Text
 from textual import events
 from textual.widget import Widget
-from txl.base import TerminalFactory, Terminal
-from txl.hooks import register_component
 
+from txl.base import Terminal, TerminalFactory
+from txl.hooks import register_component
 
 CTRL_KEYS = {
     "left": "\u001b[D",
     "right": "\u001b[C",
     "up": "\u001b[A",
     "down": "\u001b[B",
 }
```

### Comparing `jpterm-0.1.5/plugins/text_viewer/LICENSE.txt` & `jpterm-0.1.7/plugins/remote_terminals/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/text_viewer/pyproject.toml` & `jpterm-0.1.7/plugins/text_viewer/pyproject.toml`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/plugins/text_viewer/txl_text_viewer/components.py` & `jpterm-0.1.7/plugins/text_viewer/txl_text_viewer/components.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from asphalt.core import Component, Context
 from rich.syntax import Syntax
 from rich.traceback import Traceback
 from textual.widgets import Static
-from txl.base import Editor, Editors, Contents, FileOpenEvent
+
+from txl.base import Contents, Editor, Editors, FileOpenEvent
 from txl.hooks import register_component
 
 
 class TextViewerMeta(type(Editor), type(Static)):
     pass
 
 
@@ -21,16 +22,18 @@
         self.contents = contents
 
     async def on_open(self, event: FileOpenEvent) -> None:
         await self.open(event.path)
 
     async def open(self, path: str) -> None:
         self.path = path
-        self.text = await self.contents.get(path, type="text", on_change=self.on_change)
+        self.ytext = await self.contents.get(path, type="unicode")
+        self.text = self.ytext.source
         self.update_viewer()
+        self.ytext.observe(self.on_change)
 
     def update_viewer(self):
         try:
             lexer = Syntax.guess_lexer(self.path, code=self.text)
             syntax = Syntax(
                 self.text,
                 lexer=lexer,
@@ -44,16 +47,16 @@
         else:
             self.update(syntax)
             self.sub_title = self.path
 
     def on_mount(self):
         self.expand
 
-    def on_change(self, text):
-        self.text = text
+    def on_change(self, target, event):
+        self.text = self.ytext.source
         self.update_viewer()
 
 
 class TextViewerComponent(Component):
     def __init__(self, register: bool = True):
         super().__init__()
         self.register = register
```

### Comparing `jpterm-0.1.5/txl/LICENSE.txt` & `jpterm-0.1.7/plugins/terminal/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/txl/pyproject.toml` & `jpterm-0.1.7/txl/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "txl"
-description = ''
+description = ""
 readme = "README.md"
 requires-python = ">=3.7"
 license = "MIT"
 keywords = []
 authors = [
   { name = "David Brochart", email = "david.brochart@gmail.com" },
 ]
@@ -20,17 +20,17 @@
   "Programming Language :: Python :: 3.9",
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
-  "pluggy>=1.0.0,<2",
-  "asphalt>=4.11.0,<5",
-  "textual>=0.8.0,<1"
+  "pluggy >=1.0.0,<2",
+  "asphalt >=4.11.0,<5",
+  "textual >=0.10.1,<1"
 ]
 dynamic = ["version"]
 
 [project.urls]
 Source = "https://github.com/davidbrochart/jpterm/txl"
 
 [tool.hatch.version]
```

### Comparing `jpterm-0.1.5/txl/txl/app.py` & `jpterm-0.1.7/txl/txl/app.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from asphalt.core import CLIApplicationComponent, Context
 from asphalt.core.cli import run as asphalt_run
 from pluggy import PluginManager
 from textual.app import App
+
 from txl import hooks
 from txl.hooks import HookType
 
 
 def get_pluggin_manager(hook_type: HookType) -> PluginManager:
     pm = PluginManager(hook_type.value)
     pm.add_hookspecs(hooks)
```

### Comparing `jpterm-0.1.5/txl/txl/cli.py` & `jpterm-0.1.7/txl/txl/cli.py`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/txl/txl/hooks.py` & `jpterm-0.1.7/txl/txl/hooks.py`

 * *Ordering differences only*

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from enum import Enum
 from typing import Any, Dict, Tuple
 
-from asphalt.core import Component
 import pluggy
+from asphalt.core import Component
 
 
 class HookType(Enum):
     COMPONENT = "txl_component"
 
 
 @pluggy.HookspecMarker(HookType.COMPONENT.value)
```

### Comparing `jpterm-0.1.5/LICENSE` & `jpterm-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/README.md` & `jpterm-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `jpterm-0.1.5/pyproject.toml` & `jpterm-0.1.7/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -19,18 +19,21 @@
     #"txl_cell >=0.1.0",
     "txl_editors >=0.1.0",
     "txl_file_browser >=0.1.0",
     "txl_image_viewer >=0.1.0",
     "txl_jpterm >=0.1.0",
     "txl_local_contents >=0.1.0",
     "txl_local_terminals >=0.1.0",
+    "txl_local_kernels >=0.1.0",
+    "txl_notebook >=0.1.0",
     #"txl_notebook_editor >=0.1.0",
     "txl_notebook_viewer >=0.1.0",
     "txl_remote_contents >=0.1.0",
     "txl_remote_terminals >=0.1.0",
+    "txl_remote_kernels >=0.1.0",
     "txl_text_viewer >=0.1.0",
     "txl_terminal >=0.1.0",
     "txl_launcher>=0.1.0",
 ]
 
 [project.scripts]
 jpterm = "jpterm.cli:main"
@@ -39,26 +42,30 @@
 Homepage = "https://github.com/davidbrochart/jpterm"
 
 [tool.hatch.version]
 path = "jpterm/__init__.py"
 
 [tool.hatch.envs.dev]
 pre-install-commands = [
+    "pip install textual[dev]",
     "pip install -e ./txl",
     #"pip install -e ./plugins/cell",
     "pip install -e ./plugins/editors",
     "pip install -e ./plugins/file_browser",
     "pip install -e ./plugins/image_viewer",
     "pip install -e ./plugins/jpterm",
     "pip install -e ./plugins/local_contents",
     "pip install -e ./plugins/local_terminals",
+    "pip install -e ./plugins/local_kernels",
+    "pip install -e ./plugins/notebook",
     #"pip install -e ./plugins/notebook_editor",
     "pip install -e ./plugins/notebook_viewer",
     "pip install -e ./plugins/remote_contents",
     "pip install -e ./plugins/remote_terminals",
+    "pip install -e ./plugins/remote_kernels",
     "pip install -e ./plugins/text_viewer",
     "pip install -e ./plugins/terminal",
     "pip install -e ./plugins/launcher",
 
     "pip install --pre jupyterlab",
 ]
 
@@ -68,17 +75,25 @@
     "plugins/cell:txl_cell",
     "plugins/editors:txl_editors",
     "plugins/file_browser:txl_file_browser",
     "plugins/image_viewer:txl_image_viewer",
     "plugins/jpterm:txl_jpterm",
     "plugins/local_contents:txl_local_contents",
     "plugins/local_terminals:txl_local_terminals",
+    "plugins/local_kernels:txl_local_kernels",
     "plugins/notebook:txl_notebook",
     "plugins/notebook_editor:txl_notebook_editor",
     "plugins/notebook_viewer:txl_notebook_viewer",
     "plugins/remote_contents:txl_remote_contents",
     "plugins/remote_terminals:txl_remote_terminals",
+    "plugins/remote_kernels:txl_remote_kernels",
     "plugins/terminal:txl_terminal",
     "plugins/text_viewer:txl_text_viewer",
     "plugins/launcher:txl_launcher",
-    ".:jpterm:txl,txl_cell,txl_editors,txl_file_browser,txl_image_viewer,txl_jpterm,txl_local_contents,txl_local_terminals,txl_notebook,txl_notebook_editor,txl_notebook_viewer,txl_remote_contents,txl_remote_terminals,txl_terminal,txl_text_viewer,txl_launcher"
+    ".:jpterm:txl,txl_cell,txl_editors,txl_file_browser,txl_image_viewer,txl_jpterm,txl_local_contents,txl_local_terminals,txl_local_kernels,txl_notebook,txl_notebook_editor,txl_notebook_viewer,txl_remote_contents,txl_remote_terminals,txl_remote_kernels,txl_terminal,txl_text_viewer,txl_launcher"
 ]
+
+[tool.ruff]
+line-length = 100
+
+[tool.isort]
+profile = "black"
```

### Comparing `jpterm-0.1.5/PKG-INFO` & `jpterm-0.1.7/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,27 +1,30 @@
 Metadata-Version: 2.1
 Name: jpterm
-Version: 0.1.5
+Version: 0.1.7
 Summary: Jupyter in the terminal
 Project-URL: Homepage, https://github.com/davidbrochart/jpterm
 Author-email: David Brochart <david.brochart@gmail.com>
 License: MIT
 License-File: LICENSE
 Keywords: jupyter,textual
 Requires-Python: >=3.7
 Requires-Dist: rich-click>=1.6.0
 Requires-Dist: txl-editors>=0.1.0
 Requires-Dist: txl-file-browser>=0.1.0
 Requires-Dist: txl-image-viewer>=0.1.0
 Requires-Dist: txl-jpterm>=0.1.0
 Requires-Dist: txl-launcher>=0.1.0
 Requires-Dist: txl-local-contents>=0.1.0
+Requires-Dist: txl-local-kernels>=0.1.0
 Requires-Dist: txl-local-terminals>=0.1.0
 Requires-Dist: txl-notebook-viewer>=0.1.0
+Requires-Dist: txl-notebook>=0.1.0
 Requires-Dist: txl-remote-contents>=0.1.0
+Requires-Dist: txl-remote-kernels>=0.1.0
 Requires-Dist: txl-remote-terminals>=0.1.0
 Requires-Dist: txl-terminal>=0.1.0
 Requires-Dist: txl-text-viewer>=0.1.0
 Description-Content-Type: text/markdown
 
 [![Build Status](https://github.com/davidbrochart/jpterm/workflows/CI/badge.svg)](https://github.com/davidbrochart/jpterm/actions)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
```

