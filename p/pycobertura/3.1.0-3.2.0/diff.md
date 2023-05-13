# Comparing `tmp/pycobertura-3.1.0.tar.gz` & `tmp/pycobertura-3.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pycobertura-3.1.0.tar", last modified: Sat Apr 29 17:18:42 2023, max compression
+gzip compressed data, was "pycobertura-3.2.0.tar", last modified: Sat May 13 04:10:13 2023, max compression
```

## Comparing `pycobertura-3.1.0.tar` & `pycobertura-3.2.0.tar`

### file list

```diff
@@ -1,136 +1,137 @@
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.534694 pycobertura-3.1.0/
--rw-r--r--   0 alexandre   (501) staff       (20)       32 2022-10-07 08:01:13.000000 pycobertura-3.1.0/.coveragerc
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.512155 pycobertura-3.1.0/.github/
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.516533 pycobertura-3.1.0/.github/workflows/
--rw-r--r--   0 alexandre   (501) staff       (20)      642 2022-03-20 16:09:41.000000 pycobertura-3.1.0/.github/workflows/build-and-test-pycobertura.yml
--rw-r--r--   0 alexandre   (501) staff       (20)      604 2022-03-03 22:33:26.000000 pycobertura-3.1.0/.gitignore
--rw-r--r--   0 alexandre   (501) staff       (20)    15419 2023-04-29 17:17:00.000000 pycobertura-3.1.0/CHANGES.md
--rw-r--r--   0 alexandre   (501) staff       (20)     1103 2022-03-03 22:33:26.000000 pycobertura-3.1.0/LICENSE
--rw-r--r--   0 alexandre   (501) staff       (20)    23730 2023-04-29 17:18:42.534819 pycobertura-3.1.0/PKG-INFO
--rw-r--r--   0 alexandre   (501) staff       (20)    22744 2023-04-29 17:12:19.000000 pycobertura-3.1.0/README.md
--rw-r--r--   0 alexandre   (501) staff       (20)        6 2023-04-29 17:15:54.000000 pycobertura-3.1.0/__version__
--rw-r--r--   0 alexandre   (501) staff       (20)     2697 2022-01-04 01:58:44.000000 pycobertura-3.1.0/aysha-logo.svg
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.518534 pycobertura-3.1.0/images/
--rw-r--r--   0 alexandre   (501) staff       (20)    30894 2022-03-03 22:33:26.000000 pycobertura-3.1.0/images/example_csv_diff_output.png
--rw-r--r--   0 alexandre   (501) staff       (20)   115395 2023-04-29 17:12:19.000000 pycobertura-3.1.0/images/example_github_annotation_show.png
--rw-r--r--   0 alexandre   (501) staff       (20)    61287 2022-03-03 22:33:26.000000 pycobertura-3.1.0/images/example_json_output.png
--rw-r--r--   0 alexandre   (501) staff       (20)    53710 2022-03-03 22:33:26.000000 pycobertura-3.1.0/images/example_markdown_diff_output.png
--rw-r--r--   0 alexandre   (501) staff       (20)    45822 2022-03-03 22:33:26.000000 pycobertura-3.1.0/images/example_yaml_output.png
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.520728 pycobertura-3.1.0/pycobertura/
--rw-r--r--   0 alexandre   (501) staff       (20)      119 2022-01-04 01:58:44.000000 pycobertura-3.1.0/pycobertura/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)     8792 2023-04-29 17:12:19.000000 pycobertura-3.1.0/pycobertura/cli.py
--rw-r--r--   0 alexandre   (501) staff       (20)    15355 2022-10-24 18:43:16.000000 pycobertura-3.1.0/pycobertura/cobertura.py
--rw-r--r--   0 alexandre   (501) staff       (20)     4886 2023-04-29 17:12:17.000000 pycobertura-3.1.0/pycobertura/filesystem.py
--rw-r--r--   0 alexandre   (501) staff       (20)      203 2023-04-05 07:16:26.000000 pycobertura-3.1.0/pycobertura/merge.py
--rw-r--r--   0 alexandre   (501) staff       (20)    16812 2023-04-29 17:12:19.000000 pycobertura-3.1.0/pycobertura/reporters.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.523199 pycobertura-3.1.0/pycobertura/templates/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/pycobertura/templates/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      624 2022-10-07 08:01:13.000000 pycobertura-3.1.0/pycobertura/templates/filters.py
--rw-r--r--   0 alexandre   (501) staff       (20)     2805 2022-03-04 19:55:00.000000 pycobertura-3.1.0/pycobertura/templates/html-delta.jinja2
--rw-r--r--   0 alexandre   (501) staff       (20)     1764 2022-03-03 22:33:26.000000 pycobertura-3.1.0/pycobertura/templates/html.jinja2
--rw-r--r--   0 alexandre   (501) staff       (20)      473 2022-01-04 01:58:44.000000 pycobertura-3.1.0/pycobertura/templates/macro.source.jinja2
--rw-r--r--   0 alexandre   (501) staff       (20)     7797 2022-01-04 01:58:44.000000 pycobertura-3.1.0/pycobertura/templates/normalize.css
--rw-r--r--   0 alexandre   (501) staff       (20)    11452 2022-01-04 01:58:44.000000 pycobertura-3.1.0/pycobertura/templates/skeleton.css
--rw-r--r--   0 alexandre   (501) staff       (20)     7151 2022-10-07 23:42:24.000000 pycobertura-3.1.0/pycobertura/utils.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.521979 pycobertura-3.1.0/pycobertura.egg-info/
--rw-r--r--   0 alexandre   (501) staff       (20)    23730 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/PKG-INFO
--rw-r--r--   0 alexandre   (501) staff       (20)     3363 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/SOURCES.txt
--rw-r--r--   0 alexandre   (501) staff       (20)        1 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/dependency_links.txt
--rw-r--r--   0 alexandre   (501) staff       (20)       60 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/entry_points.txt
--rw-r--r--   0 alexandre   (501) staff       (20)        1 2022-03-04 19:49:40.000000 pycobertura-3.1.0/pycobertura.egg-info/not-zip-safe
--rw-r--r--   0 alexandre   (501) staff       (20)       44 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/requires.txt
--rw-r--r--   0 alexandre   (501) staff       (20)       12 2023-04-29 17:18:42.000000 pycobertura-3.1.0/pycobertura.egg-info/top_level.txt
--rw-r--r--   0 alexandre   (501) staff       (20)      122 2022-03-03 22:33:26.000000 pycobertura-3.1.0/pyproject.toml
--rw-r--r--   0 alexandre   (501) staff       (20)      997 2022-10-07 08:01:13.000000 pycobertura-3.1.0/pytest.ini
--rwxr-xr-x   0 alexandre   (501) staff       (20)      415 2022-10-09 09:37:38.000000 pycobertura-3.1.0/release.sh
--rw-r--r--   0 alexandre   (501) staff       (20)     1300 2023-04-29 17:18:42.535201 pycobertura-3.1.0/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)       38 2022-03-03 22:33:26.000000 pycobertura-3.1.0/setup.py
--rw-r--r--   0 alexandre   (501) staff       (20)       82 2022-10-07 08:01:13.000000 pycobertura-3.1.0/test-requirements.txt
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.527942 pycobertura-3.1.0/tests/
--rw-r--r--   0 alexandre   (501) staff       (20)       64 2022-10-07 23:42:24.000000 pycobertura-3.1.0/tests/.testgitignore
--rw-r--r--   0 alexandre   (501) staff       (20)      748 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/README.generate-dummy-coverage-for-testing.md
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1162 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/cobertura-generated-by-istanbul-from-coffeescript.xml
--rw-r--r--   0 alexandre   (501) staff       (20)     7963 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/cobertura.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.528612 pycobertura-3.1.0/tests/dummy/
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.534570 pycobertura-3.1.0/tests/dummy/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)       41 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)       20 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/dummy/dummy2.py
--rw-r--r--   0 alexandre   (501) staff       (20)      995 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/dummy-with-prefix.zip
--rw-r--r--   0 alexandre   (501) staff       (20)      687 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/dummy.zip
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)      179 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy/test_dummy.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.528904 pycobertura-3.1.0/tests/dummy.linestatus/
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.529053 pycobertura-3.1.0/tests/dummy.linestatus/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)       14 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.linestatus/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      623 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.linestatus/test1.xml
--rw-r--r--   0 alexandre   (501) staff       (20)      578 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.linestatus/test2.xml
--rw-r--r--   0 alexandre   (501) staff       (20)      861 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.original-better-cov.xml
--rw-r--r--   0 alexandre   (501) staff       (20)      852 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.original-full-cov.xml
--rw-r--r--   0 alexandre   (501) staff       (20)      858 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.original.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.529530 pycobertura-3.1.0/tests/dummy.source1/
--rw-r--r--   0 alexandre   (501) staff       (20)     1456 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.530105 pycobertura-3.1.0/tests/dummy.source1/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)       56 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)       20 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/dummy/dummy2.py
--rw-r--r--   0 alexandre   (501) staff       (20)       64 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/dummy/dummy4.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)      119 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source1/test_dummy.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.530563 pycobertura-3.1.0/tests/dummy.source2/
--rw-r--r--   0 alexandre   (501) staff       (20)     1423 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.531062 pycobertura-3.1.0/tests/dummy.source2/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)       56 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)       44 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/dummy/dummy2.py
--rw-r--r--   0 alexandre   (501) staff       (20)      209 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/dummy/dummy3.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)      179 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.source2/test_dummy.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.531488 pycobertura-3.1.0/tests/dummy.uncovered/
--rw-r--r--   0 alexandre   (501) staff       (20)     1178 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.532431 pycobertura-3.1.0/tests/dummy.uncovered/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      114 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)      178 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered/test_dummy.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.531929 pycobertura-3.1.0/tests/dummy.uncovered.addcode/
--rw-r--r--   0 alexandre   (501) staff       (20)     1250 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered.addcode/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.532183 pycobertura-3.1.0/tests/dummy.uncovered.addcode/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered.addcode/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      185 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered.addcode/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered.addcode/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)      178 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.uncovered.addcode/test_dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1093 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.with-dummy2-better-and-worse.xml
--rw-r--r--   0 alexandre   (501) staff       (20)     1092 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.with-dummy2-better-cov.xml
--rw-r--r--   0 alexandre   (501) staff       (20)     1080 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.with-dummy2-full-cov.xml
--rw-r--r--   0 alexandre   (501) staff       (20)     1090 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.with-dummy2-no-cov.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.533163 pycobertura-3.1.0/tests/dummy.zeroexit1/
--rw-r--r--   0 alexandre   (501) staff       (20)      969 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit1/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.533474 pycobertura-3.1.0/tests/dummy.zeroexit1/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit1/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      108 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit1/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit1/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)       58 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit1/test_dummy.py
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.533954 pycobertura-3.1.0/tests/dummy.zeroexit2/
--rw-r--r--   0 alexandre   (501) staff       (20)     1000 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit2/coverage.xml
-drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-04-29 17:18:42.534205 pycobertura-3.1.0/tests/dummy.zeroexit2/dummy/
--rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit2/dummy/__init__.py
--rw-r--r--   0 alexandre   (501) staff       (20)      134 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit2/dummy/dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit2/setup.cfg
--rw-r--r--   0 alexandre   (501) staff       (20)       68 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/dummy.zeroexit2/test_dummy.py
--rw-r--r--   0 alexandre   (501) staff       (20)    29409 2023-04-29 17:12:19.000000 pycobertura-3.1.0/tests/test_cli.py
--rw-r--r--   0 alexandre   (501) staff       (20)     9064 2022-03-03 22:33:26.000000 pycobertura-3.1.0/tests/test_cobertura.py
--rw-r--r--   0 alexandre   (501) staff       (20)     5737 2022-10-07 08:01:13.000000 pycobertura-3.1.0/tests/test_cobertura_diff.py
--rw-r--r--   0 alexandre   (501) staff       (20)      127 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_colorize.py
--rw-r--r--   0 alexandre   (501) staff       (20)      429 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_extrapolate_coverage.py
--rw-r--r--   0 alexandre   (501) staff       (20)     6494 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_filesystem.py
--rw-r--r--   0 alexandre   (501) staff       (20)     6429 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_hunkify_coverage.py
--rw-r--r--   0 alexandre   (501) staff       (20)      187 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_imports.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1166 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_rangify.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1076 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/test_reconcile_lines.py
--rw-r--r--   0 alexandre   (501) staff       (20)      926 2022-10-07 23:42:24.000000 pycobertura-3.1.0/tests/test_regex_utils.py
--rw-r--r--   0 alexandre   (501) staff       (20)    20163 2023-04-29 17:12:19.000000 pycobertura-3.1.0/tests/test_reporters.py
--rw-r--r--   0 alexandre   (501) staff       (20)     1175 2022-03-03 22:33:26.000000 pycobertura-3.1.0/tests/test_stringify.py
--rw-r--r--   0 alexandre   (501) staff       (20)      420 2022-01-04 01:58:44.000000 pycobertura-3.1.0/tests/utils.py
--rw-r--r--   0 alexandre   (501) staff       (20)      528 2022-10-07 08:01:13.000000 pycobertura-3.1.0/tox.ini
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.571233 pycobertura-3.2.0/
+-rw-r--r--   0 alexandre   (501) staff       (20)       32 2022-10-07 08:01:13.000000 pycobertura-3.2.0/.coveragerc
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.548811 pycobertura-3.2.0/.github/
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.552763 pycobertura-3.2.0/.github/workflows/
+-rw-r--r--   0 alexandre   (501) staff       (20)      642 2022-03-20 16:09:41.000000 pycobertura-3.2.0/.github/workflows/build-and-test-pycobertura.yml
+-rw-r--r--   0 alexandre   (501) staff       (20)      604 2022-03-03 22:33:26.000000 pycobertura-3.2.0/.gitignore
+-rw-r--r--   0 alexandre   (501) staff       (20)    15532 2023-05-13 04:09:27.000000 pycobertura-3.2.0/CHANGES.md
+-rw-r--r--   0 alexandre   (501) staff       (20)     1103 2022-03-03 22:33:26.000000 pycobertura-3.2.0/LICENSE
+-rw-r--r--   0 alexandre   (501) staff       (20)    24292 2023-05-13 04:10:13.571343 pycobertura-3.2.0/PKG-INFO
+-rw-r--r--   0 alexandre   (501) staff       (20)    23306 2023-05-13 04:07:52.000000 pycobertura-3.2.0/README.md
+-rw-r--r--   0 alexandre   (501) staff       (20)        6 2023-05-13 04:08:58.000000 pycobertura-3.2.0/__version__
+-rw-r--r--   0 alexandre   (501) staff       (20)     2697 2022-01-04 01:58:44.000000 pycobertura-3.2.0/aysha-logo.svg
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.556563 pycobertura-3.2.0/images/
+-rw-r--r--   0 alexandre   (501) staff       (20)    30894 2022-03-03 22:33:26.000000 pycobertura-3.2.0/images/example_csv_diff_output.png
+-rw-r--r--   0 alexandre   (501) staff       (20)   172765 2023-05-13 04:07:52.000000 pycobertura-3.2.0/images/example_github_annotation_diff.png
+-rw-r--r--   0 alexandre   (501) staff       (20)   103005 2023-04-29 17:28:15.000000 pycobertura-3.2.0/images/example_github_annotation_show.png
+-rw-r--r--   0 alexandre   (501) staff       (20)    61287 2022-03-03 22:33:26.000000 pycobertura-3.2.0/images/example_json_output.png
+-rw-r--r--   0 alexandre   (501) staff       (20)    53710 2022-03-03 22:33:26.000000 pycobertura-3.2.0/images/example_markdown_diff_output.png
+-rw-r--r--   0 alexandre   (501) staff       (20)    45822 2022-03-03 22:33:26.000000 pycobertura-3.2.0/images/example_yaml_output.png
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.558408 pycobertura-3.2.0/pycobertura/
+-rw-r--r--   0 alexandre   (501) staff       (20)      119 2022-01-04 01:58:44.000000 pycobertura-3.2.0/pycobertura/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     9607 2023-05-13 04:07:52.000000 pycobertura-3.2.0/pycobertura/cli.py
+-rw-r--r--   0 alexandre   (501) staff       (20)    15355 2022-10-24 18:43:16.000000 pycobertura-3.2.0/pycobertura/cobertura.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     4886 2023-04-29 17:12:17.000000 pycobertura-3.2.0/pycobertura/filesystem.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      203 2023-04-05 07:16:26.000000 pycobertura-3.2.0/pycobertura/merge.py
+-rw-r--r--   0 alexandre   (501) staff       (20)    17838 2023-05-13 04:07:52.000000 pycobertura-3.2.0/pycobertura/reporters.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.560701 pycobertura-3.2.0/pycobertura/templates/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/pycobertura/templates/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      624 2022-10-07 08:01:13.000000 pycobertura-3.2.0/pycobertura/templates/filters.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     2805 2022-03-04 19:55:00.000000 pycobertura-3.2.0/pycobertura/templates/html-delta.jinja2
+-rw-r--r--   0 alexandre   (501) staff       (20)     1764 2022-03-03 22:33:26.000000 pycobertura-3.2.0/pycobertura/templates/html.jinja2
+-rw-r--r--   0 alexandre   (501) staff       (20)      473 2022-01-04 01:58:44.000000 pycobertura-3.2.0/pycobertura/templates/macro.source.jinja2
+-rw-r--r--   0 alexandre   (501) staff       (20)     7797 2022-01-04 01:58:44.000000 pycobertura-3.2.0/pycobertura/templates/normalize.css
+-rw-r--r--   0 alexandre   (501) staff       (20)    11452 2022-01-04 01:58:44.000000 pycobertura-3.2.0/pycobertura/templates/skeleton.css
+-rw-r--r--   0 alexandre   (501) staff       (20)     7151 2022-10-07 23:42:24.000000 pycobertura-3.2.0/pycobertura/utils.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.559466 pycobertura-3.2.0/pycobertura.egg-info/
+-rw-r--r--   0 alexandre   (501) staff       (20)    24292 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/PKG-INFO
+-rw-r--r--   0 alexandre   (501) staff       (20)     3405 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/SOURCES.txt
+-rw-r--r--   0 alexandre   (501) staff       (20)        1 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/dependency_links.txt
+-rw-r--r--   0 alexandre   (501) staff       (20)       60 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/entry_points.txt
+-rw-r--r--   0 alexandre   (501) staff       (20)        1 2022-03-04 19:49:40.000000 pycobertura-3.2.0/pycobertura.egg-info/not-zip-safe
+-rw-r--r--   0 alexandre   (501) staff       (20)       44 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/requires.txt
+-rw-r--r--   0 alexandre   (501) staff       (20)       12 2023-05-13 04:10:13.000000 pycobertura-3.2.0/pycobertura.egg-info/top_level.txt
+-rw-r--r--   0 alexandre   (501) staff       (20)      122 2022-03-03 22:33:26.000000 pycobertura-3.2.0/pyproject.toml
+-rw-r--r--   0 alexandre   (501) staff       (20)      997 2022-10-07 08:01:13.000000 pycobertura-3.2.0/pytest.ini
+-rwxr-xr-x   0 alexandre   (501) staff       (20)      415 2022-10-09 09:37:38.000000 pycobertura-3.2.0/release.sh
+-rw-r--r--   0 alexandre   (501) staff       (20)     1300 2023-05-13 04:10:13.571691 pycobertura-3.2.0/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)       38 2022-03-03 22:33:26.000000 pycobertura-3.2.0/setup.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       82 2022-10-07 08:01:13.000000 pycobertura-3.2.0/test-requirements.txt
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.565121 pycobertura-3.2.0/tests/
+-rw-r--r--   0 alexandre   (501) staff       (20)       64 2022-10-07 23:42:24.000000 pycobertura-3.2.0/tests/.testgitignore
+-rw-r--r--   0 alexandre   (501) staff       (20)      748 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/README.generate-dummy-coverage-for-testing.md
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1162 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/cobertura-generated-by-istanbul-from-coffeescript.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)     7963 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/cobertura.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.565744 pycobertura-3.2.0/tests/dummy/
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.571097 pycobertura-3.2.0/tests/dummy/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       41 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       20 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/dummy/dummy2.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      995 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/dummy-with-prefix.zip
+-rw-r--r--   0 alexandre   (501) staff       (20)      687 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/dummy.zip
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)      179 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy/test_dummy.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.566044 pycobertura-3.2.0/tests/dummy.linestatus/
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.566190 pycobertura-3.2.0/tests/dummy.linestatus/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)       14 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.linestatus/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      623 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.linestatus/test1.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)      578 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.linestatus/test2.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)      861 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.original-better-cov.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)      852 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.original-full-cov.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)      858 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.original.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.566771 pycobertura-3.2.0/tests/dummy.source1/
+-rw-r--r--   0 alexandre   (501) staff       (20)     1456 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.567307 pycobertura-3.2.0/tests/dummy.source1/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       56 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       20 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/dummy/dummy2.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       64 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/dummy/dummy4.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)      119 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source1/test_dummy.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.567704 pycobertura-3.2.0/tests/dummy.source2/
+-rw-r--r--   0 alexandre   (501) staff       (20)     1423 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.568200 pycobertura-3.2.0/tests/dummy.source2/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       56 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)       44 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/dummy/dummy2.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      209 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/dummy/dummy3.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)      179 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.source2/test_dummy.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.568606 pycobertura-3.2.0/tests/dummy.uncovered/
+-rw-r--r--   0 alexandre   (501) staff       (20)     1178 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.569455 pycobertura-3.2.0/tests/dummy.uncovered/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      114 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)      178 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered/test_dummy.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.569009 pycobertura-3.2.0/tests/dummy.uncovered.addcode/
+-rw-r--r--   0 alexandre   (501) staff       (20)     1250 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered.addcode/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.569234 pycobertura-3.2.0/tests/dummy.uncovered.addcode/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered.addcode/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      185 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered.addcode/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered.addcode/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)      178 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.uncovered.addcode/test_dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1093 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.with-dummy2-better-and-worse.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)     1092 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.with-dummy2-better-cov.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)     1080 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.with-dummy2-full-cov.xml
+-rw-r--r--   0 alexandre   (501) staff       (20)     1090 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.with-dummy2-no-cov.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.569884 pycobertura-3.2.0/tests/dummy.zeroexit1/
+-rw-r--r--   0 alexandre   (501) staff       (20)      969 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit1/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.570123 pycobertura-3.2.0/tests/dummy.zeroexit1/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit1/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      108 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit1/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit1/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)       58 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit1/test_dummy.py
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.570521 pycobertura-3.2.0/tests/dummy.zeroexit2/
+-rw-r--r--   0 alexandre   (501) staff       (20)     1000 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit2/coverage.xml
+drwxr-xr-x   0 alexandre   (501) staff       (20)        0 2023-05-13 04:10:13.570748 pycobertura-3.2.0/tests/dummy.zeroexit2/dummy/
+-rw-r--r--   0 alexandre   (501) staff       (20)        0 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit2/dummy/__init__.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      134 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit2/dummy/dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1032 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit2/setup.cfg
+-rw-r--r--   0 alexandre   (501) staff       (20)       68 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/dummy.zeroexit2/test_dummy.py
+-rw-r--r--   0 alexandre   (501) staff       (20)    30824 2023-05-13 04:07:52.000000 pycobertura-3.2.0/tests/test_cli.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     9064 2022-03-03 22:33:26.000000 pycobertura-3.2.0/tests/test_cobertura.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     5737 2022-10-07 08:01:13.000000 pycobertura-3.2.0/tests/test_cobertura_diff.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      127 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_colorize.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      429 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_extrapolate_coverage.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     6494 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_filesystem.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     6429 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_hunkify_coverage.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      187 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_imports.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1166 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_rangify.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1076 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/test_reconcile_lines.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      926 2022-10-07 23:42:24.000000 pycobertura-3.2.0/tests/test_regex_utils.py
+-rw-r--r--   0 alexandre   (501) staff       (20)    21608 2023-05-13 04:07:52.000000 pycobertura-3.2.0/tests/test_reporters.py
+-rw-r--r--   0 alexandre   (501) staff       (20)     1175 2022-03-03 22:33:26.000000 pycobertura-3.2.0/tests/test_stringify.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      420 2022-01-04 01:58:44.000000 pycobertura-3.2.0/tests/utils.py
+-rw-r--r--   0 alexandre   (501) staff       (20)      528 2022-10-07 08:01:13.000000 pycobertura-3.2.0/tox.ini
```

### Comparing `pycobertura-3.1.0/.github/workflows/build-and-test-pycobertura.yml` & `pycobertura-3.2.0/.github/workflows/build-and-test-pycobertura.yml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/.gitignore` & `pycobertura-3.2.0/.gitignore`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/CHANGES.md` & `pycobertura-3.2.0/CHANGES.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,15 @@
 # Release Notes
 
 ## Unreleased
 
+## 3.2.0 (2023-05-12)
+
+* `pycobertura diff` now supports output format: `github-annotation`. Thanks @goatwu1993
+
 ## 3.1.0 (2023-04-29)
 
 * `pycobertura show` now supports output format: `github-annotation`. Thanks @goatwu1993
 
 ## 3.0.0 (2022-10-08)
 
 * BACKWARD INCOMPATIBLE:
```

### Comparing `pycobertura-3.1.0/LICENSE` & `pycobertura-3.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/PKG-INFO` & `pycobertura-3.2.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,31 +1,7 @@
-Metadata-Version: 2.1
-Name: pycobertura
-Version: 3.1.0
-Summary: "A Cobertura coverage parser that can diff reports and show coverage progress."
-Home-page: https://github.com/aconrad/pycobertura
-Author: "Alex Conrad"
-Author-email: "alexandre.conrad@gmail.com"
-Maintainer: "Alex Conrad"
-Maintainer-email: "alexandre.conrad@gmail.com"
-Keywords: "cobertura coverage diff report parser parse xml"
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Natural Language :: English
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 # pycobertura
 
 ![pycobertura logo](https://raw.githubusercontent.com/aconrad/pycobertura/master/aysha-logo.svg)
 
 A code coverage diff tool for Cobertura reports.
 
 ![pycobertura](https://github.com/aconrad/pycobertura/actions/workflows/build-and-test-pycobertura.yml/badge.svg)
@@ -302,14 +278,27 @@
 
 ```shell
 pycobertura diff --format yaml tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
 ```
 
 ![Example output of yaml formatted pycobertura diff command](images/example_yaml_output.png)
 
+The following shows how to generate GitHub annotations given a coverage file.
+
+```shell
+$ pycobertura diff --format github-annotation tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
+::notice file=dummy/dummy2.py,line=5,endLine=5,title=pycobertura::not covered
+::notice file=dummy/dummy3.py,line=1,endLine=2,title=pycobertura::not covered
+```
+
+If you run it in GitHub Actions/Apps, the above log generates check annotations.
+
+![Example output of github-annotation formatted pycobertura diff command](images/example_github_annotation_diff.png)
+
+
 ### Option to exclude files via --ignore-regex-option
 You can specify the `--ignore-regex` option to exclude files that have a certain pattern either by specifying the path to a `.gitignore` file or by entering a Python regex.
 Examples:
 ```
 pycobertura show tests/cobertura.xml
 Filename                          Stmts    Miss  Cover    Missing
 ------------------------------  -------  ------  -------  ---------
```

### Comparing `pycobertura-3.1.0/README.md` & `pycobertura-3.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,31 @@
+Metadata-Version: 2.1
+Name: pycobertura
+Version: 3.2.0
+Summary: "A Cobertura coverage parser that can diff reports and show coverage progress."
+Home-page: https://github.com/aconrad/pycobertura
+Author: "Alex Conrad"
+Author-email: "alexandre.conrad@gmail.com"
+Maintainer: "Alex Conrad"
+Maintainer-email: "alexandre.conrad@gmail.com"
+Keywords: "cobertura coverage diff report parser parse xml"
+Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3 :: Only
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 # pycobertura
 
 ![pycobertura logo](https://raw.githubusercontent.com/aconrad/pycobertura/master/aysha-logo.svg)
 
 A code coverage diff tool for Cobertura reports.
 
 ![pycobertura](https://github.com/aconrad/pycobertura/actions/workflows/build-and-test-pycobertura.yml/badge.svg)
@@ -278,14 +302,27 @@
 
 ```shell
 pycobertura diff --format yaml tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
 ```
 
 ![Example output of yaml formatted pycobertura diff command](images/example_yaml_output.png)
 
+The following shows how to generate GitHub annotations given a coverage file.
+
+```shell
+$ pycobertura diff --format github-annotation tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
+::notice file=dummy/dummy2.py,line=5,endLine=5,title=pycobertura::not covered
+::notice file=dummy/dummy3.py,line=1,endLine=2,title=pycobertura::not covered
+```
+
+If you run it in GitHub Actions/Apps, the above log generates check annotations.
+
+![Example output of github-annotation formatted pycobertura diff command](images/example_github_annotation_diff.png)
+
+
 ### Option to exclude files via --ignore-regex-option
 You can specify the `--ignore-regex` option to exclude files that have a certain pattern either by specifying the path to a `.gitignore` file or by entering a Python regex.
 Examples:
 ```
 pycobertura show tests/cobertura.xml
 Filename                          Stmts    Miss  Cover    Missing
 ------------------------------  -------  ------  -------  ---------
```

### Comparing `pycobertura-3.1.0/aysha-logo.svg` & `pycobertura-3.2.0/aysha-logo.svg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/images/example_csv_diff_output.png` & `pycobertura-3.2.0/images/example_csv_diff_output.png`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/images/example_json_output.png` & `pycobertura-3.2.0/images/example_json_output.png`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/images/example_markdown_diff_output.png` & `pycobertura-3.2.0/images/example_markdown_diff_output.png`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/images/example_yaml_output.png` & `pycobertura-3.2.0/images/example_yaml_output.png`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/cli.py` & `pycobertura-3.2.0/pycobertura/cli.py`

 * *Files 8% similar despite different names*

```diff
@@ -11,14 +11,15 @@
     YamlReporter,
     HtmlReporterDelta,
     TextReporterDelta,
     CsvReporterDelta,
     MarkdownReporterDelta,
     JsonReporterDelta,
     YamlReporterDelta,
+    GitHubAnnotationReporterDelta,
 )
 from pycobertura.filesystem import filesystem_factory
 from pycobertura.utils import get_dir_from_file_path
 
 pycobertura = click.Group()
 
 
@@ -160,14 +161,15 @@
 delta_reporters = {
     "text": TextReporterDelta,
     "csv": CsvReporterDelta,
     "markdown": MarkdownReporterDelta,
     "html": HtmlReporterDelta,
     "json": JsonReporterDelta,
     "yaml": YamlReporterDelta,
+    "github-annotation": GitHubAnnotationReporterDelta,
 }
 
 
 @pycobertura.command(
     help="""\
 The diff command compares and shows the changes between two Cobertura reports.
 
@@ -247,27 +249,48 @@
     default=True,
     help="Show missing lines and source code. When enabled (default), this "
     "option requires access to the source code that was used to generate "
     "both Cobertura reports (see --source1 and --source2). When "
     "`--no-source` is passed, missing lines and the source code will "
     "not be displayed.",
 )
+@click.option(
+    "--annotation-title",
+    default="pycobertura",
+    type=str,
+    help="annotation title for github annotation format",
+)
+@click.option(
+    "--annotation-level",
+    default="notice",
+    type=str,
+    help="annotation level for github annotation format",
+)
+@click.option(
+    "--annotation-message",
+    default="not covered",
+    type=str,
+    help="annotation message for github annotation format",
+)
 def diff(
     cobertura_file1,
     cobertura_file2,
     ignore_regex,
     delimiter,
     color,
     format,
     output,
     source1,
     source2,
     source_prefix1,
     source_prefix2,
     source,
+    annotation_level,
+    annotation_title,
+    annotation_message,
 ):
     """compare coverage of two Cobertura reports"""
     # Assume that the source is located in the same directory as the provided
     # coverage files if no source directories are provided.
     if not source1:
         source1 = get_dir_from_file_path(cobertura_file1)
 
@@ -289,14 +312,20 @@
     if format in {"text", "csv", "json", "markdown", "yaml"}:
         color = isatty if color is None else color is True
         reporter_kwargs["color"] = color
 
     reporter = Reporter(*reporter_args, **reporter_kwargs)
     if format == "csv":
         report = reporter.generate(delimiter)
+    elif format == "github-annotation":
+        report = reporter.generate(
+            annotation_level=annotation_level,
+            annotation_message=annotation_message,
+            annotation_title=annotation_title,
+        )
     else:
         report = reporter.generate()
 
     if not isinstance(report, bytes):
         report = report.encode("utf-8")
 
     click.echo(report, file=output, nl=isatty, color=color)
```

### Comparing `pycobertura-3.1.0/pycobertura/cobertura.py` & `pycobertura-3.2.0/pycobertura/cobertura.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/filesystem.py` & `pycobertura-3.2.0/pycobertura/filesystem.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/reporters.py` & `pycobertura-3.2.0/pycobertura/reporters.py`

 * *Files 7% similar despite different names*

```diff
@@ -477,7 +477,36 @@
         start_line_num: int,
         end_line_num: int,
         annotation_level: str,
         annotation_title: str,
         annotation_message: str,
     ):
         return f"::{annotation_level} file={file_name},line={start_line_num},endLine={end_line_num},title={annotation_title}::{annotation_message}"  # noqa
+
+
+class GitHubAnnotationReporterDelta(DeltaReporter):
+    def generate(
+        self,
+        annotation_level: str,
+        annotation_title: str,
+        annotation_message: str,
+    ):
+        lines = self.get_report_lines()
+        stats_dict = self.per_file_stats(lines)
+        result_strs = []
+
+        for file_stat in stats_dict["files"]:
+            for range_start, range_end in rangify(
+                [int(line) for line in file_stat["Missing"]]
+            ):
+                result_strs.append(
+                    GitHubAnnotationReporter.to_github_annotation_message(
+                        file_name=file_stat["Filename"],
+                        start_line_num=range_start,
+                        end_line_num=range_end,
+                        annotation_level=annotation_level,
+                        annotation_title=annotation_title,
+                        annotation_message=annotation_message,
+                    )
+                )
+        result = "\n".join(result_strs)
+        return result
```

### Comparing `pycobertura-3.1.0/pycobertura/templates/filters.py` & `pycobertura-3.2.0/pycobertura/templates/filters.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/templates/html-delta.jinja2` & `pycobertura-3.2.0/pycobertura/templates/html-delta.jinja2`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/templates/html.jinja2` & `pycobertura-3.2.0/pycobertura/templates/html.jinja2`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/templates/normalize.css` & `pycobertura-3.2.0/pycobertura/templates/normalize.css`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/templates/skeleton.css` & `pycobertura-3.2.0/pycobertura/templates/skeleton.css`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura/utils.py` & `pycobertura-3.2.0/pycobertura/utils.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/pycobertura.egg-info/PKG-INFO` & `pycobertura-3.2.0/pycobertura.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pycobertura
-Version: 3.1.0
+Version: 3.2.0
 Summary: "A Cobertura coverage parser that can diff reports and show coverage progress."
 Home-page: https://github.com/aconrad/pycobertura
 Author: "Alex Conrad"
 Author-email: "alexandre.conrad@gmail.com"
 Maintainer: "Alex Conrad"
 Maintainer-email: "alexandre.conrad@gmail.com"
 Keywords: "cobertura coverage diff report parser parse xml"
@@ -302,14 +302,27 @@
 
 ```shell
 pycobertura diff --format yaml tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
 ```
 
 ![Example output of yaml formatted pycobertura diff command](images/example_yaml_output.png)
 
+The following shows how to generate GitHub annotations given a coverage file.
+
+```shell
+$ pycobertura diff --format github-annotation tests/dummy.source1/coverage.xml tests/dummy.source2/coverage.xml
+::notice file=dummy/dummy2.py,line=5,endLine=5,title=pycobertura::not covered
+::notice file=dummy/dummy3.py,line=1,endLine=2,title=pycobertura::not covered
+```
+
+If you run it in GitHub Actions/Apps, the above log generates check annotations.
+
+![Example output of github-annotation formatted pycobertura diff command](images/example_github_annotation_diff.png)
+
+
 ### Option to exclude files via --ignore-regex-option
 You can specify the `--ignore-regex` option to exclude files that have a certain pattern either by specifying the path to a `.gitignore` file or by entering a Python regex.
 Examples:
 ```
 pycobertura show tests/cobertura.xml
 Filename                          Stmts    Miss  Cover    Missing
 ------------------------------  -------  ------  -------  ---------
```

### Comparing `pycobertura-3.1.0/pycobertura.egg-info/SOURCES.txt` & `pycobertura-3.2.0/pycobertura.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -10,14 +10,15 @@
 release.sh
 setup.cfg
 setup.py
 test-requirements.txt
 tox.ini
 .github/workflows/build-and-test-pycobertura.yml
 images/example_csv_diff_output.png
+images/example_github_annotation_diff.png
 images/example_github_annotation_show.png
 images/example_json_output.png
 images/example_markdown_diff_output.png
 images/example_yaml_output.png
 pycobertura/__init__.py
 pycobertura/cli.py
 pycobertura/cobertura.py
```

### Comparing `pycobertura-3.1.0/pytest.ini` & `pycobertura-3.2.0/pytest.ini`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/setup.cfg` & `pycobertura-3.2.0/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/README.generate-dummy-coverage-for-testing.md` & `pycobertura-3.2.0/tests/README.generate-dummy-coverage-for-testing.md`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/cobertura-generated-by-istanbul-from-coffeescript.xml` & `pycobertura-3.2.0/tests/cobertura-generated-by-istanbul-from-coffeescript.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/cobertura.xml` & `pycobertura-3.2.0/tests/cobertura.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy/dummy-with-prefix.zip` & `pycobertura-3.2.0/tests/dummy/dummy-with-prefix.zip`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy/dummy.zip` & `pycobertura-3.2.0/tests/dummy/dummy.zip`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy/setup.cfg` & `pycobertura-3.2.0/tests/dummy/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.linestatus/test1.xml` & `pycobertura-3.2.0/tests/dummy.linestatus/test1.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.linestatus/test2.xml` & `pycobertura-3.2.0/tests/dummy.linestatus/test2.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.original-better-cov.xml` & `pycobertura-3.2.0/tests/dummy.original-better-cov.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.original-full-cov.xml` & `pycobertura-3.2.0/tests/dummy.original-full-cov.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.original.xml` & `pycobertura-3.2.0/tests/dummy.original.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.source1/coverage.xml` & `pycobertura-3.2.0/tests/dummy.source1/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.source1/setup.cfg` & `pycobertura-3.2.0/tests/dummy.source1/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.source2/coverage.xml` & `pycobertura-3.2.0/tests/dummy.source2/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.source2/setup.cfg` & `pycobertura-3.2.0/tests/dummy.source2/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.uncovered/coverage.xml` & `pycobertura-3.2.0/tests/dummy.uncovered/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.uncovered/setup.cfg` & `pycobertura-3.2.0/tests/dummy.uncovered/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.uncovered.addcode/coverage.xml` & `pycobertura-3.2.0/tests/dummy.uncovered.addcode/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.uncovered.addcode/setup.cfg` & `pycobertura-3.2.0/tests/dummy.uncovered.addcode/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.with-dummy2-better-and-worse.xml` & `pycobertura-3.2.0/tests/dummy.with-dummy2-better-and-worse.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.with-dummy2-better-cov.xml` & `pycobertura-3.2.0/tests/dummy.with-dummy2-better-cov.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.with-dummy2-full-cov.xml` & `pycobertura-3.2.0/tests/dummy.with-dummy2-full-cov.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.with-dummy2-no-cov.xml` & `pycobertura-3.2.0/tests/dummy.with-dummy2-no-cov.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.zeroexit1/coverage.xml` & `pycobertura-3.2.0/tests/dummy.zeroexit1/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.zeroexit1/setup.cfg` & `pycobertura-3.2.0/tests/dummy.zeroexit1/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.zeroexit2/coverage.xml` & `pycobertura-3.2.0/tests/dummy.zeroexit2/coverage.xml`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/dummy.zeroexit2/setup.cfg` & `pycobertura-3.2.0/tests/dummy.zeroexit2/setup.cfg`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_cli.py` & `pycobertura-3.2.0/tests/test_cli.py`

 * *Files 8% similar despite different names*

```diff
@@ -772,14 +772,51 @@
   Miss: '+1'
   Cover: +31.06%
 
 """
     assert result.exit_code == ExitCodes.COVERAGE_WORSENED
 
 
+def test_diff__format_github_annotation():
+    from pycobertura.cli import diff, ExitCodes
+
+    runner = CliRunner()
+    for opt in ('-f', '--format'):
+        result = runner.invoke(diff, [
+            opt, 'github-annotation',
+            'tests/dummy.source1/coverage.xml',
+            'tests/dummy.source2/coverage.xml',
+        ], catch_exceptions=False)
+        assert result.output == """\
+::notice file=dummy/dummy2.py,line=5,endLine=5,title=pycobertura::not covered
+::notice file=dummy/dummy3.py,line=1,endLine=2,title=pycobertura::not covered
+"""
+        assert result.exit_code == ExitCodes.COVERAGE_WORSENED
+
+
+def test_diff__format_github_annotation_custom_annotation_input():
+    from pycobertura.cli import diff, ExitCodes
+
+    runner = CliRunner()
+    for opt in ('-f', '--format'):
+        result = runner.invoke(diff, [
+            opt, 'github-annotation',
+            'tests/dummy.source1/coverage.xml',
+            'tests/dummy.source2/coverage.xml',
+            "--annotation-title=coverage.py",
+            "--annotation-level=error",
+            "--annotation-message=missing coverage",
+        ], catch_exceptions=False)
+        assert result.output == """\
+::error file=dummy/dummy2.py,line=5,endLine=5,title=coverage.py::missing coverage
+::error file=dummy/dummy3.py,line=1,endLine=2,title=coverage.py::missing coverage
+"""
+        assert result.exit_code == ExitCodes.COVERAGE_WORSENED
+
+
 def test_diff__format_html__no_source_on_disk():
     from pycobertura.cli import diff
     from pycobertura.filesystem import FileSystem
 
     runner = CliRunner()
     pytest.raises(FileSystem.FileNotFound, runner.invoke, diff, [
         '--format', 'html',
```

### Comparing `pycobertura-3.1.0/tests/test_cobertura.py` & `pycobertura-3.2.0/tests/test_cobertura.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_cobertura_diff.py` & `pycobertura-3.2.0/tests/test_cobertura_diff.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_filesystem.py` & `pycobertura-3.2.0/tests/test_filesystem.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_hunkify_coverage.py` & `pycobertura-3.2.0/tests/test_hunkify_coverage.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_rangify.py` & `pycobertura-3.2.0/tests/test_rangify.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_reconcile_lines.py` & `pycobertura-3.2.0/tests/test_reconcile_lines.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_regex_utils.py` & `pycobertura-3.2.0/tests/test_regex_utils.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tests/test_reporters.py` & `pycobertura-3.2.0/tests/test_reporters.py`

 * *Files 6% similar despite different names*

```diff
@@ -701,7 +701,48 @@
         report.generate(
             annotation_level="error",
             annotation_title="JCov",
             annotation_message="missing coverage",
         )
         == expected_custom_output
     )
+
+
+@pytest.mark.parametrize(
+    "report1, report2, config, expected_default_output, expected_custom_output",
+    [
+        (
+            "tests/dummy.source1/coverage.xml",
+            "tests/dummy.source2/coverage.xml",
+            {
+                "annotation_level":"error",
+                "annotation_title":"JCov",
+                "annotation_message":"missing coverage"
+            },
+            """\
+::notice file=dummy/dummy2.py,line=5,endLine=5,title=pycobertura::not covered
+::notice file=dummy/dummy3.py,line=1,endLine=2,title=pycobertura::not covered""",
+            """\
+::error file=dummy/dummy2.py,line=5,endLine=5,title=JCov::missing coverage
+::error file=dummy/dummy3.py,line=1,endLine=2,title=JCov::missing coverage""",
+        ),
+    ],
+)
+def test_github_annotation_report_delta(
+    report1, report2, config, expected_default_output, expected_custom_output
+):
+    from pycobertura.reporters import GitHubAnnotationReporterDelta
+
+    cobertura1 = make_cobertura(report1)
+    cobertura2 = make_cobertura(report2)
+
+    default_config = {
+        "annotation_level": "notice",
+        "annotation_title": "pycobertura",
+        "annotation_message": "not covered",
+    }
+    report_delta = GitHubAnnotationReporterDelta(
+        cobertura1, cobertura2, show_missing=False
+    )
+    assert report_delta.generate(**default_config) == expected_default_output
+    assert report_delta.generate(**config) == expected_custom_output
+
```

### Comparing `pycobertura-3.1.0/tests/test_stringify.py` & `pycobertura-3.2.0/tests/test_stringify.py`

 * *Files identical despite different names*

### Comparing `pycobertura-3.1.0/tox.ini` & `pycobertura-3.2.0/tox.ini`

 * *Files identical despite different names*

