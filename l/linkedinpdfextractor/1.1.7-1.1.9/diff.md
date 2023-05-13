# Comparing `tmp/linkedinpdfextractor-1.1.7.tar.gz` & `tmp/linkedinpdfextractor-1.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "linkedinpdfextractor-1.1.7.tar", last modified: Fri May  5 09:50:35 2023, max compression
+gzip compressed data, was "linkedinpdfextractor-1.1.9.tar", last modified: Sat May 13 05:38:43 2023, max compression
```

## Comparing `linkedinpdfextractor-1.1.7.tar` & `linkedinpdfextractor-1.1.9.tar`

### file list

```diff
@@ -1,89 +1,89 @@
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.359652 linkedinpdfextractor-1.1.7/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     8196 2023-05-05 08:33:17.000000 linkedinpdfextractor-1.1.7/.DS_Store
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1809 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.7/.gitignore
--rw-r--r--   0 seshivitakula   (501) staff       (20)       82 2023-04-21 07:18:22.000000 linkedinpdfextractor-1.1.7/AUTHORS.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)      128 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/CHANGELOG.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)    14010 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/CONTRIBUTING.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1078 2023-04-19 16:57:33.000000 linkedinpdfextractor-1.1.7/LICENSE.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2917 2023-05-05 09:50:35.359830 linkedinpdfextractor-1.1.7/PKG-INFO
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2408 2023-05-04 13:07:58.000000 linkedinpdfextractor-1.1.7/README.rst
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.326505 linkedinpdfextractor-1.1.7/docs/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1154 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/Makefile
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.326777 linkedinpdfextractor-1.1.7/docs/_static/
--rw-r--r--   0 seshivitakula   (501) staff       (20)       18 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/_static/.gitignore
--rw-r--r--   0 seshivitakula   (501) staff       (20)       41 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/authors.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)       43 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/changelog.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)     9807 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/conf.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)       33 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/contributing.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2373 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/index.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)       67 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/license.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)       39 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/readme.rst
--rw-r--r--   0 seshivitakula   (501) staff       (20)      233 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/docs/requirements.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)      346 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/pyproject.toml
--rw-r--r--   0 seshivitakula   (501) staff       (20)       46 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.7/requirements.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1249 2023-05-05 09:50:35.360787 linkedinpdfextractor-1.1.7/setup.cfg
--rw-r--r--   0 seshivitakula   (501) staff       (20)      720 2023-05-05 09:47:02.000000 linkedinpdfextractor-1.1.7/setup.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.327046 linkedinpdfextractor-1.1.7/src/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     6148 2023-04-19 11:25:51.000000 linkedinpdfextractor-1.1.7/src/.DS_Store
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.328658 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     6148 2023-04-19 11:27:25.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/.DS_Store
--rw-r--r--   0 seshivitakula   (501) staff       (20)      577 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/__init__.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     5950 2023-05-05 08:33:17.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/extractor.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.330127 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/
--rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/__init__.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.335524 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/
--rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/__init__.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2916 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/annotate.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     3691 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/sizemapper.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     5496 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/styledistribution.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.342767 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/
--rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/__init__.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1593 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/detectheader.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2985 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/headercompare.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     7296 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/parser.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2608 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/traversal.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.343685 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/
--rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/__init__.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4497 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/document.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2108 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/style.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4155 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/printer.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4983 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/source.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4253 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/utils.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4310 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/skeleton.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.346896 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2917 2023-05-05 09:50:35.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/PKG-INFO
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2518 2023-05-05 09:50:35.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/SOURCES.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)        1 2023-05-05 09:50:35.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/dependency_links.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)        1 2023-04-21 07:55:27.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/not-zip-safe
--rw-r--r--   0 seshivitakula   (501) staff       (20)      101 2023-05-05 09:50:35.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/requires.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)       23 2023-05-05 09:50:35.000000 linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/top_level.txt
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.350732 linkedinpdfextractor-1.1.7/tests/
--rw-r--r--   0 seshivitakula   (501) staff       (20)     8196 2023-05-05 08:33:17.000000 linkedinpdfextractor-1.1.7/tests/.DS_Store
--rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/__init__.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)      290 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/tests/conftest.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)      820 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/helper.py
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.357735 linkedinpdfextractor-1.1.7/tests/resources/
--rw-r--r--   0 seshivitakula   (501) staff       (20)   143869 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/5648.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)   401628 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/IE00BM67HT60-ATB-FS-DE-2020-2-28.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)    18836 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/SameSize_BoldTitle.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)    12108 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/SameSize_EnumeratedTitle.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)    12178 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/SameStyleOnly.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)    45965 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/interview_cheatsheet-excerpt.png
--rwxr-xr-x   0 seshivitakula   (501) staff       (20)   230787 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/interview_cheatsheet.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)    32674 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/lorem.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)   383508 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/paper.pdf
-drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-05 09:50:35.359384 linkedinpdfextractor-1.1.7/tests/resources/parsed/
--rw-r--r--   0 seshivitakula   (501) staff       (20)   215280 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/parsed/interview_cheatsheet.json
--rw-r--r--   0 seshivitakula   (501) staff       (20)    15753 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/parsed/interview_cheatsheet_pretty.txt
--rw-r--r--   0 seshivitakula   (501) staff       (20)    62812 2023-04-19 12:12:39.000000 linkedinpdfextractor-1.1.7/tests/resources/profile.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)   251982 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.7/tests/resources/samplepptx.pdf
--rw-r--r--   0 seshivitakula   (501) staff       (20)     1398 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_custom_use_cases.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)      656 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_document.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2304 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_headercompare.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4709 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_hierarchy.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     3202 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_printer.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)      597 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/tests/test_skeleton.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     4276 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_style_analyser.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     3865 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_traversal.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)      804 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.7/tests/test_utils.py
--rw-r--r--   0 seshivitakula   (501) staff       (20)     2690 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.7/tox.ini
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.538164 linkedinpdfextractor-1.1.9/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     8196 2023-05-05 08:33:17.000000 linkedinpdfextractor-1.1.9/.DS_Store
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1809 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.9/.gitignore
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       82 2023-04-21 07:18:22.000000 linkedinpdfextractor-1.1.9/AUTHORS.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      128 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/CHANGELOG.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    14010 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/CONTRIBUTING.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1078 2023-04-19 16:57:33.000000 linkedinpdfextractor-1.1.9/LICENSE.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2917 2023-05-13 05:38:43.538298 linkedinpdfextractor-1.1.9/PKG-INFO
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2408 2023-05-04 13:07:58.000000 linkedinpdfextractor-1.1.9/README.rst
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.515572 linkedinpdfextractor-1.1.9/docs/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1154 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/Makefile
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.515874 linkedinpdfextractor-1.1.9/docs/_static/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       18 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/_static/.gitignore
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       41 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/authors.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       43 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/changelog.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     9807 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/conf.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       33 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/contributing.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2373 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/index.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       67 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/license.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       39 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/readme.rst
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      233 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/docs/requirements.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      346 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/pyproject.toml
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       46 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.9/requirements.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1249 2023-05-13 05:38:43.539039 linkedinpdfextractor-1.1.9/setup.cfg
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      723 2023-05-05 10:18:51.000000 linkedinpdfextractor-1.1.9/setup.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.516158 linkedinpdfextractor-1.1.9/src/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     6148 2023-04-19 11:25:51.000000 linkedinpdfextractor-1.1.9/src/.DS_Store
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.517785 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     6148 2023-04-19 11:27:25.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/.DS_Store
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      577 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/__init__.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     5965 2023-05-13 05:16:31.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/extractor.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.519184 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/__init__.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.520744 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/__init__.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2916 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/annotate.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     3691 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/sizemapper.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     5496 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/styledistribution.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.522054 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/__init__.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1593 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/detectheader.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2985 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/headercompare.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     7296 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/parser.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2608 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/traversal.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.522835 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/__init__.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4497 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/document.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2108 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/style.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4155 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/printer.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4983 2023-04-21 06:26:32.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/source.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4253 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/utils.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4310 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/skeleton.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.524428 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2917 2023-05-13 05:38:43.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/PKG-INFO
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2518 2023-05-13 05:38:43.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/SOURCES.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        1 2023-05-13 05:38:43.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/dependency_links.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        1 2023-04-21 07:55:27.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/not-zip-safe
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      101 2023-05-13 05:38:43.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/requires.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)       23 2023-05-13 05:38:43.000000 linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/top_level.txt
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.527979 linkedinpdfextractor-1.1.9/tests/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     8196 2023-05-05 08:33:17.000000 linkedinpdfextractor-1.1.9/tests/.DS_Store
+-rw-r--r--   0 seshivitakula   (501) staff       (20)        0 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/__init__.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      290 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/tests/conftest.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      820 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/helper.py
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.536285 linkedinpdfextractor-1.1.9/tests/resources/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)   143869 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/5648.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)   401628 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/IE00BM67HT60-ATB-FS-DE-2020-2-28.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    18836 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/SameSize_BoldTitle.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    12108 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/SameSize_EnumeratedTitle.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    12178 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/SameStyleOnly.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    45965 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/interview_cheatsheet-excerpt.png
+-rwxr-xr-x   0 seshivitakula   (501) staff       (20)   230787 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/interview_cheatsheet.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    32674 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/lorem.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)   383508 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/paper.pdf
+drwxr-xr-x   0 seshivitakula   (501) staff       (20)        0 2023-05-13 05:38:43.537934 linkedinpdfextractor-1.1.9/tests/resources/parsed/
+-rw-r--r--   0 seshivitakula   (501) staff       (20)   215280 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/parsed/interview_cheatsheet.json
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    15753 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/parsed/interview_cheatsheet_pretty.txt
+-rw-r--r--   0 seshivitakula   (501) staff       (20)    62812 2023-04-19 12:12:39.000000 linkedinpdfextractor-1.1.9/tests/resources/profile.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)   251982 2023-04-17 18:56:43.000000 linkedinpdfextractor-1.1.9/tests/resources/samplepptx.pdf
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     1398 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_custom_use_cases.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      656 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_document.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2304 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_headercompare.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4709 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_hierarchy.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     3202 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_printer.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      597 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/tests/test_skeleton.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     4276 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_style_analyser.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     3865 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_traversal.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)      804 2023-04-24 06:24:13.000000 linkedinpdfextractor-1.1.9/tests/test_utils.py
+-rw-r--r--   0 seshivitakula   (501) staff       (20)     2690 2023-04-19 11:23:25.000000 linkedinpdfextractor-1.1.9/tox.ini
```

### Comparing `linkedinpdfextractor-1.1.7/.DS_Store` & `linkedinpdfextractor-1.1.9/.DS_Store`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/.gitignore` & `linkedinpdfextractor-1.1.9/.gitignore`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/CONTRIBUTING.rst` & `linkedinpdfextractor-1.1.9/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/LICENSE.txt` & `linkedinpdfextractor-1.1.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/PKG-INFO` & `linkedinpdfextractor-1.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: linkedinpdfextractor
-Version: 1.1.7
+Version: 1.1.9
 Summary: Add a short description here!
 Home-page: https://github.com/pyscaffold/pyscaffold/
 Author: Ketan Prabhu
 Author-email: ketan.prabhu@gigvistas.com
 License: MIT
 Project-URL: Documentation, https://pyscaffold.org/
 Platform: any
```

### Comparing `linkedinpdfextractor-1.1.7/README.rst` & `linkedinpdfextractor-1.1.9/README.rst`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/docs/Makefile` & `linkedinpdfextractor-1.1.9/docs/Makefile`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/docs/conf.py` & `linkedinpdfextractor-1.1.9/docs/conf.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/docs/index.rst` & `linkedinpdfextractor-1.1.9/docs/index.rst`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/setup.cfg` & `linkedinpdfextractor-1.1.9/setup.cfg`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/setup.py` & `linkedinpdfextractor-1.1.9/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,8 +15,10 @@
         setup(use_scm_version=True)
     except Exception as e:
         print("\n\nAn error occurred while building the project:", e)
         print(
             "\n\nPlease ensure you have the most updated version of setuptools, setuptools_scm, and wheel with:\n"
             "   pip install -U setuptools setuptools_scm wheel\n\n"
         )
-        raise
+        raise
+
+
```

### Comparing `linkedinpdfextractor-1.1.7/src/.DS_Store` & `linkedinpdfextractor-1.1.9/src/.DS_Store`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/.DS_Store` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/.DS_Store`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/__init__.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/__init__.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/extractor.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/extractor.py`

 * *Files 1% similar despite different names*

```diff
@@ -113,15 +113,15 @@
     experience = Experience()
     education = Education()
     i = 0
     for index, row in data.iterrows():
         if (row['level'] == 1 and row["mean_size"] == 26.0 and row["max_size"] == 26.0):
             user.name = row["text"]
         elif (row['level'] == 1 and row["mean_size"] == 12.0 and row["max_size"] == 12.0):
-            user.title = row["text"]
+            user.title = row["text"].split('\n')[0]
         elif (row['level'] == 2 and row["mean_size"] == 12.0 and row["max_size"] == 12.0 and row["type"] == "Summary"):
             summary.description.append(row["text"])
         elif (row['level'] == 3 and row["mean_size"] == 10.5 and row["max_size"] == 10.5 and row["type"] == "Contact"):
             contact.description = row["text"]
         elif (row['level'] == 3 and row["mean_size"] == 10.5 and row["max_size"] == 10.5 and row["type"] == "Top Skills"):
             user.skills.append(row["text"])
         elif(row['level'] == 2 and row["type"] == "Experience"):
```

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/annotate.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/annotate.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/sizemapper.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/sizemapper.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/analysis/styledistribution.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/analysis/styledistribution.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/detectheader.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/detectheader.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/headercompare.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/headercompare.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/parser.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/parser.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/hierarchy/traversal.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/hierarchy/traversal.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/document.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/document.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/model/style.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/model/style.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/printer.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/printer.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/source.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/source.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/pdfstructure/utils.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/pdfstructure/utils.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedin_pdf_extractor/skeleton.py` & `linkedinpdfextractor-1.1.9/src/linkedin_pdf_extractor/skeleton.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/PKG-INFO` & `linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: linkedinpdfextractor
-Version: 1.1.7
+Version: 1.1.9
 Summary: Add a short description here!
 Home-page: https://github.com/pyscaffold/pyscaffold/
 Author: Ketan Prabhu
 Author-email: ketan.prabhu@gigvistas.com
 License: MIT
 Project-URL: Documentation, https://pyscaffold.org/
 Platform: any
```

### Comparing `linkedinpdfextractor-1.1.7/src/linkedinpdfextractor.egg-info/SOURCES.txt` & `linkedinpdfextractor-1.1.9/src/linkedinpdfextractor.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/.DS_Store` & `linkedinpdfextractor-1.1.9/tests/.DS_Store`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/helper.py` & `linkedinpdfextractor-1.1.9/tests/helper.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/5648.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/5648.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/IE00BM67HT60-ATB-FS-DE-2020-2-28.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/IE00BM67HT60-ATB-FS-DE-2020-2-28.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/SameSize_BoldTitle.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/SameSize_BoldTitle.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/SameSize_EnumeratedTitle.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/SameSize_EnumeratedTitle.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/SameStyleOnly.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/SameStyleOnly.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/interview_cheatsheet-excerpt.png` & `linkedinpdfextractor-1.1.9/tests/resources/interview_cheatsheet-excerpt.png`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/interview_cheatsheet.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/interview_cheatsheet.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/lorem.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/lorem.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/paper.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/paper.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/parsed/interview_cheatsheet.json` & `linkedinpdfextractor-1.1.9/tests/resources/parsed/interview_cheatsheet.json`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/parsed/interview_cheatsheet_pretty.txt` & `linkedinpdfextractor-1.1.9/tests/resources/parsed/interview_cheatsheet_pretty.txt`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/profile.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/profile.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/resources/samplepptx.pdf` & `linkedinpdfextractor-1.1.9/tests/resources/samplepptx.pdf`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_custom_use_cases.py` & `linkedinpdfextractor-1.1.9/tests/test_custom_use_cases.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_document.py` & `linkedinpdfextractor-1.1.9/tests/test_document.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_headercompare.py` & `linkedinpdfextractor-1.1.9/tests/test_headercompare.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_hierarchy.py` & `linkedinpdfextractor-1.1.9/tests/test_hierarchy.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_printer.py` & `linkedinpdfextractor-1.1.9/tests/test_printer.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_skeleton.py` & `linkedinpdfextractor-1.1.9/tests/test_skeleton.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_style_analyser.py` & `linkedinpdfextractor-1.1.9/tests/test_style_analyser.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_traversal.py` & `linkedinpdfextractor-1.1.9/tests/test_traversal.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tests/test_utils.py` & `linkedinpdfextractor-1.1.9/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `linkedinpdfextractor-1.1.7/tox.ini` & `linkedinpdfextractor-1.1.9/tox.ini`

 * *Files identical despite different names*

