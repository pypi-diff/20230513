# Comparing `tmp/django-ckeditor-5-0.2.5.tar.gz` & `tmp/django-ckeditor-5-0.2.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-ckeditor-5-0.2.5.tar", last modified: Sat May 13 13:02:58 2023, max compression
+gzip compressed data, was "django-ckeditor-5-0.2.7.tar", last modified: Sat May 13 17:57:33 2023, max compression
```

## Comparing `django-ckeditor-5-0.2.5.tar` & `django-ckeditor-5-0.2.7.tar`

### file list

```diff
@@ -1,155 +1,155 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.951139 django-ckeditor-5-0.2.5/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      821 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/.github/FUNDING.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.955139 django-ckeditor-5-0.2.5/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/.github/workflows/lint_python.yml
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/.github/workflows/testpypi.yml
--rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1487 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      219 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     9263 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8138 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.955139 django-ckeditor-5-0.2.5/django_ckeditor_5/
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/.jshintrc
--rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/fields.py
--rw-r--r--   0 runner    (1001) docker     (123)       92 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/forms.py
--rw-r--r--   0 runner    (1001) docker     (123)   232306 2023-05-13 13:02:15.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)     2164 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.951139 django-ckeditor-5-0.2.5/django_ckeditor_5/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.955139 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/
--rw-r--r--   0 runner    (1001) docker     (123)     2635 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/app.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.963139 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/
--rw-r--r--   0 runner    (1001) docker     (123)   908796 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js
--rw-r--r--   0 runner    (1001) docker     (123)      593 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)  5638447 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.map
--rw-r--r--   0 runner    (1001) docker     (123)   121601 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css
--rw-r--r--   0 runner    (1001) docker     (123)   230439 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css.map
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.971139 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/
--rw-r--r--   0 runner    (1001) docker     (123)      882 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/af.js
--rw-r--r--   0 runner    (1001) docker     (123)    10948 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ar.js
--rw-r--r--   0 runner    (1001) docker     (123)     2364 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ast.js
--rw-r--r--   0 runner    (1001) docker     (123)     6718 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/az.js
--rw-r--r--   0 runner    (1001) docker     (123)    12743 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bg.js
--rw-r--r--   0 runner    (1001) docker     (123)    14330 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bn.js
--rw-r--r--   0 runner    (1001) docker     (123)     2119 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bs.js
--rw-r--r--   0 runner    (1001) docker     (123)     9239 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ca.js
--rw-r--r--   0 runner    (1001) docker     (123)     8902 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/cs.js
--rw-r--r--   0 runner    (1001) docker     (123)     8456 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/da.js
--rw-r--r--   0 runner    (1001) docker     (123)     7226 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de-ch.js
--rw-r--r--   0 runner    (1001) docker     (123)     8913 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de.js
--rw-r--r--   0 runner    (1001) docker     (123)    13328 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/el.js
--rw-r--r--   0 runner    (1001) docker     (123)     7719 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-au.js
--rw-r--r--   0 runner    (1001) docker     (123)     5788 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-gb.js
--rw-r--r--   0 runner    (1001) docker     (123)     2617 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eo.js
--rw-r--r--   0 runner    (1001) docker     (123)     1035 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es-co.js
--rw-r--r--   0 runner    (1001) docker     (123)     9037 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es.js
--rw-r--r--   0 runner    (1001) docker     (123)     8512 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/et.js
--rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eu.js
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fa.js
--rw-r--r--   0 runner    (1001) docker     (123)     8669 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fi.js
--rw-r--r--   0 runner    (1001) docker     (123)     9268 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fr.js
--rw-r--r--   0 runner    (1001) docker     (123)     8941 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gl.js
--rw-r--r--   0 runner    (1001) docker     (123)      621 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gu.js
--rw-r--r--   0 runner    (1001) docker     (123)    10335 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/he.js
--rw-r--r--   0 runner    (1001) docker     (123)     8718 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hi.js
--rw-r--r--   0 runner    (1001) docker     (123)     7622 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hr.js
--rw-r--r--   0 runner    (1001) docker     (123)     9036 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hu.js
--rw-r--r--   0 runner    (1001) docker     (123)     8156 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/id.js
--rw-r--r--   0 runner    (1001) docker     (123)     9431 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/it.js
--rw-r--r--   0 runner    (1001) docker     (123)     9800 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ja.js
--rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/jv.js
--rw-r--r--   0 runner    (1001) docker     (123)      466 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kk.js
--rw-r--r--   0 runner    (1001) docker     (123)     3819 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/km.js
--rw-r--r--   0 runner    (1001) docker     (123)     3237 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kn.js
--rw-r--r--   0 runner    (1001) docker     (123)     8732 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ko.js
--rw-r--r--   0 runner    (1001) docker     (123)     8118 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ku.js
--rw-r--r--   0 runner    (1001) docker     (123)     9391 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lt.js
--rw-r--r--   0 runner    (1001) docker     (123)     8969 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lv.js
--rw-r--r--   0 runner    (1001) docker     (123)     8279 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ms.js
--rw-r--r--   0 runner    (1001) docker     (123)     5086 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nb.js
--rw-r--r--   0 runner    (1001) docker     (123)     9269 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ne.js
--rw-r--r--   0 runner    (1001) docker     (123)     8679 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nl.js
--rw-r--r--   0 runner    (1001) docker     (123)     8343 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/no.js
--rw-r--r--   0 runner    (1001) docker     (123)      418 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/oc.js
--rw-r--r--   0 runner    (1001) docker     (123)     9269 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pl.js
--rw-r--r--   0 runner    (1001) docker     (123)     8825 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt-br.js
--rw-r--r--   0 runner    (1001) docker     (123)     9020 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt.js
--rw-r--r--   0 runner    (1001) docker     (123)     8927 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ro.js
--rw-r--r--   0 runner    (1001) docker     (123)    13125 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ru.js
--rw-r--r--   0 runner    (1001) docker     (123)     2033 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/si.js
--rw-r--r--   0 runner    (1001) docker     (123)     8888 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sk.js
--rw-r--r--   0 runner    (1001) docker     (123)     2021 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sl.js
--rw-r--r--   0 runner    (1001) docker     (123)     5492 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sq.js
--rw-r--r--   0 runner    (1001) docker     (123)     8796 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr-latn.js
--rw-r--r--   0 runner    (1001) docker     (123)    11755 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr.js
--rw-r--r--   0 runner    (1001) docker     (123)     8286 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sv.js
--rw-r--r--   0 runner    (1001) docker     (123)    14370 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/th.js
--rw-r--r--   0 runner    (1001) docker     (123)     7617 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tk.js
--rw-r--r--   0 runner    (1001) docker     (123)     8778 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tr.js
--rw-r--r--   0 runner    (1001) docker     (123)     3731 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tt.js
--rw-r--r--   0 runner    (1001) docker     (123)     5360 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ug.js
--rw-r--r--   0 runner    (1001) docker     (123)    12587 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uk.js
--rw-r--r--   0 runner    (1001) docker     (123)     7640 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ur.js
--rw-r--r--   0 runner    (1001) docker     (123)     7942 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uz.js
--rw-r--r--   0 runner    (1001) docker     (123)     9629 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/vi.js
--rw-r--r--   0 runner    (1001) docker     (123)     8074 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh-cn.js
--rw-r--r--   0 runner    (1001) docker     (123)     7681 2023-05-13 13:02:46.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.971139 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/src/
--rw-r--r--   0 runner    (1001) docker     (123)     3807 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/src/ckeditor.js
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/src/override-django.css
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.951139 django-ckeditor-5-0.2.5/django_ckeditor_5/templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.971139 django-ckeditor-5-0.2.5/django_ckeditor_5/templates/django_ckeditor_5/
--rw-r--r--   0 runner    (1001) docker     (123)      427 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/templates/django_ckeditor_5/widget.html
--rw-r--r--   0 runner    (1001) docker     (123)      147 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     1397 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/views.py
--rw-r--r--   0 runner    (1001) docker     (123)     2051 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/webpack.config.js
--rw-r--r--   0 runner    (1001) docker     (123)     2879 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/widgets.py
--rw-r--r--   0 runner    (1001) docker     (123)   136516 2023-05-13 13:02:15.000000 django-ckeditor-5-0.2.5/django_ckeditor_5/yarn.lock
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.955139 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9263 2023-05-13 13:02:58.000000 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6790 2023-05-13 13:02:58.000000 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:02:58.000000 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      419 2023-05-13 13:02:58.000000 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 13:02:58.000000 django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/articles/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      343 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/admin.py
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)      565 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/forms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/articles/migrations/
--rw-r--r--   0 runner    (1001) docker     (123)     1563 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/migrations/0001_initial.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/migrations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      878 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/models.py
--rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/storage.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/articles/templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/articles/templates/articles/
--rw-r--r--   0 runner    (1001) docker     (123)      838 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/templates/articles/article_detail.html
--rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/templates/articles/article_list.html
--rw-r--r--   0 runner    (1001) docker     (123)      287 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/templates/base.html
--rw-r--r--   0 runner    (1001) docker     (123)      240 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)     1117 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/articles/views.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.975139 django-ckeditor-5-0.2.5/example/blog/blog/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/blog/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/blog/asgi.py
--rw-r--r--   0 runner    (1001) docker     (123)     8371 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/blog/settings.py
--rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/blog/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/blog/wsgi.py
--rw-r--r--   0 runner    (1001) docker     (123)      177 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.951139 django-ckeditor-5-0.2.5/example/blog/fixtures/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/example/blog/fixtures/files/
--rw-r--r--   0 runner    (1001) docker     (123)    56624 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/fixtures/files/test.png
--rwxr-xr-x   0 runner    (1001) docker     (123)      624 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/manage.py
--rw-r--r--   0 runner    (1001) docker     (123)      440 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/example/blog/static_files/
--rw-r--r--   0 runner    (1001) docker     (123)     5318 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/static_files/custom.css
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/example/blog/tests/
--rw-r--r--   0 runner    (1001) docker     (123)    57286 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/tests/coverage.xml
--rw-r--r--   0 runner    (1001) docker     (123)      927 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/blog/tests/test_upload_file.py
--rw-r--r--   0 runner    (1001) docker     (123)      156 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/example/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2870 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:02:58.979139 django-ckeditor-5-0.2.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      170 2023-05-13 13:02:07.000000 django-ckeditor-5-0.2.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.374697 django-ckeditor-5-0.2.7/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      821 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/.github/FUNDING.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.374697 django-ckeditor-5-0.2.7/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/.github/workflows/lint_python.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      867 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/.github/workflows/testpypi.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1487 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     9263 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8138 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.378697 django-ckeditor-5-0.2.7/django_ckeditor_5/
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/.jshintrc
+-rw-r--r--   0 runner    (1001) docker     (123)       62 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/fields.py
+-rw-r--r--   0 runner    (1001) docker     (123)       92 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/forms.py
+-rw-r--r--   0 runner    (1001) docker     (123)   232306 2023-05-13 17:56:44.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2164 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.374697 django-ckeditor-5-0.2.7/django_ckeditor_5/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.378697 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/
+-rw-r--r--   0 runner    (1001) docker     (123)     2635 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/app.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.386697 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/
+-rw-r--r--   0 runner    (1001) docker     (123)   908796 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js
+-rw-r--r--   0 runner    (1001) docker     (123)      593 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)  5638447 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.map
+-rw-r--r--   0 runner    (1001) docker     (123)   121601 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css
+-rw-r--r--   0 runner    (1001) docker     (123)   230439 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css.map
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/
+-rw-r--r--   0 runner    (1001) docker     (123)      882 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/af.js
+-rw-r--r--   0 runner    (1001) docker     (123)    10948 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ar.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2364 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ast.js
+-rw-r--r--   0 runner    (1001) docker     (123)     6718 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/az.js
+-rw-r--r--   0 runner    (1001) docker     (123)    12743 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bg.js
+-rw-r--r--   0 runner    (1001) docker     (123)    14330 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bn.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2119 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bs.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9239 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ca.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8902 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/cs.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8456 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/da.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7226 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de-ch.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8913 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de.js
+-rw-r--r--   0 runner    (1001) docker     (123)    13328 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/el.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7719 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-au.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5788 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-gb.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2617 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eo.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1035 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es-co.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9037 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8512 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/et.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eu.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fa.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8669 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fi.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9268 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fr.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8941 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gl.js
+-rw-r--r--   0 runner    (1001) docker     (123)      621 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gu.js
+-rw-r--r--   0 runner    (1001) docker     (123)    10335 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/he.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8718 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hi.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7622 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hr.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9036 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hu.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8156 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/id.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9431 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/it.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9800 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ja.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/jv.js
+-rw-r--r--   0 runner    (1001) docker     (123)      466 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3819 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/km.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3237 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kn.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8732 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ko.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8118 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ku.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9391 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lt.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8969 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lv.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8279 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ms.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5086 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nb.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9269 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ne.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8679 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nl.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8343 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/no.js
+-rw-r--r--   0 runner    (1001) docker     (123)      418 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/oc.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9269 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pl.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8825 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt-br.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9020 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8927 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ro.js
+-rw-r--r--   0 runner    (1001) docker     (123)    13125 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ru.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2033 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/si.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8888 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2021 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sl.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5492 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sq.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8796 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr-latn.js
+-rw-r--r--   0 runner    (1001) docker     (123)    11755 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8286 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sv.js
+-rw-r--r--   0 runner    (1001) docker     (123)    14370 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/th.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7617 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8778 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tr.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3731 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tt.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5360 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ug.js
+-rw-r--r--   0 runner    (1001) docker     (123)    12587 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uk.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7640 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ur.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7942 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uz.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9629 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/vi.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8074 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh-cn.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7681 2023-05-13 17:57:18.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     3807 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/src/ckeditor.js
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/src/override-django.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.374697 django-ckeditor-5-0.2.7/django_ckeditor_5/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/django_ckeditor_5/templates/django_ckeditor_5/
+-rw-r--r--   0 runner    (1001) docker     (123)      427 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/templates/django_ckeditor_5/widget.html
+-rw-r--r--   0 runner    (1001) docker     (123)      147 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1397 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/views.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2051 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/webpack.config.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2879 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/widgets.py
+-rw-r--r--   0 runner    (1001) docker     (123)   136516 2023-05-13 17:56:44.000000 django-ckeditor-5-0.2.7/django_ckeditor_5/yarn.lock
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.378697 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9263 2023-05-13 17:57:33.000000 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6790 2023-05-13 17:57:33.000000 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 17:57:33.000000 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      419 2023-05-13 17:57:33.000000 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 17:57:33.000000 django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/example/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/example/blog/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/example/blog/articles/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      343 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)       91 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)      565 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/forms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/example/blog/articles/migrations/
+-rw-r--r--   0 runner    (1001) docker     (123)     1563 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/migrations/0001_initial.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/migrations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      878 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      366 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/storage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.394697 django-ckeditor-5-0.2.7/example/blog/articles/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/example/blog/articles/templates/articles/
+-rw-r--r--   0 runner    (1001) docker     (123)      838 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/templates/articles/article_detail.html
+-rw-r--r--   0 runner    (1001) docker     (123)      356 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/templates/articles/article_list.html
+-rw-r--r--   0 runner    (1001) docker     (123)      287 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/templates/base.html
+-rw-r--r--   0 runner    (1001) docker     (123)      240 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1117 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/articles/views.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/example/blog/blog/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/blog/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/blog/asgi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8371 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/blog/settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/blog/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/blog/wsgi.py
+-rw-r--r--   0 runner    (1001) docker     (123)      177 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.374697 django-ckeditor-5-0.2.7/example/blog/fixtures/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/example/blog/fixtures/files/
+-rw-r--r--   0 runner    (1001) docker     (123)    56624 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/fixtures/files/test.png
+-rwxr-xr-x   0 runner    (1001) docker     (123)      624 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/manage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      440 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/example/blog/static_files/
+-rw-r--r--   0 runner    (1001) docker     (123)     5318 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/static_files/custom.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/example/blog/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)    57286 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/tests/coverage.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      927 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/blog/tests/test_upload_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/example/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2870 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 17:57:33.398697 django-ckeditor-5-0.2.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      170 2023-05-13 17:56:31.000000 django-ckeditor-5-0.2.7/setup.py
```

### Comparing `django-ckeditor-5-0.2.5/.github/FUNDING.yml` & `django-ckeditor-5-0.2.7/.github/FUNDING.yml`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/.github/workflows/lint_python.yml` & `django-ckeditor-5-0.2.7/.github/workflows/lint_python.yml`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/.github/workflows/release.yml` & `django-ckeditor-5-0.2.7/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/.github/workflows/testpypi.yml` & `django-ckeditor-5-0.2.7/.github/workflows/testpypi.yml`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/.gitignore` & `django-ckeditor-5-0.2.7/.gitignore`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/LICENSE` & `django-ckeditor-5-0.2.7/LICENSE`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/PKG-INFO` & `django-ckeditor-5-0.2.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-ckeditor-5
-Version: 0.2.5
+Version: 0.2.7
 Summary: CKEditor 5 for Django.
 Author-email: Vladislav Khoboko <vladislah@gmail.com>
 License: BSD-3-Clause
 Project-URL: homepage, https://pypi.org/project/django-ckeditor-5/
 Project-URL: repository, https://github.com/hvlads/django-ckeditor-5
 Keywords: CKEditor,CKEditor5,Django
 Classifier: Environment :: Web Environment
```

### Comparing `django-ckeditor-5-0.2.5/README.rst` & `django-ckeditor-5-0.2.7/README.rst`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/fields.py` & `django-ckeditor-5-0.2.7/django_ckeditor_5/fields.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/package-lock.json` & `django-ckeditor-5-0.2.7/django_ckeditor_5/package-lock.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.8999899193548387%*

 * *Differences: {"'packages'": "{'': {'version': '0.2.7'}}", "'version'": "'0.2.7'"}*

```diff
@@ -46,15 +46,15 @@
                 "style-loader": "3",
                 "terser-webpack-plugin": "^5.3.8",
                 "webpack": "5",
                 "webpack-cli": "5"
             },
             "license": "ISC",
             "name": "django_ckeditor_5",
-            "version": "0.2.5"
+            "version": "0.2.7"
         },
         "node_modules/@babel/code-frame": {
             "dependencies": {
                 "@babel/highlight": "^7.18.6"
             },
             "dev": true,
             "engines": {
@@ -6460,9 +6460,9 @@
             "integrity": "sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q==",
             "license": "MIT",
             "resolved": "https://registry.npmjs.org/yocto-queue/-/yocto-queue-0.1.0.tgz",
             "version": "0.1.0"
         }
     },
     "requires": true,
-    "version": "0.2.5"
+    "version": "0.2.7"
 }
```

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/package.json` & `django-ckeditor-5-0.2.7/django_ckeditor_5/package.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9444444444444444%*

 * *Differences: {"'version'": "'0.2.7'"}*

```diff
@@ -50,9 +50,9 @@
     "main": "index.js",
     "name": "django_ckeditor_5",
     "scripts": {
         "dev": "webpack --mode development",
         "prod": "webpack --mode production",
         "test": "echo \"Error: no test specified\" && exit 1"
     },
-    "version": "0.2.5"
+    "version": "0.2.7"
 }
```

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/app.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/app.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.LICENSE.txt` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.map` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/bundle.js.map`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css.map` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/styles.css.map`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/af.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/af.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ar.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ar.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ast.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ast.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/az.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/az.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bg.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bg.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bn.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bn.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bs.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/bs.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ca.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ca.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/cs.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/cs.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/da.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/da.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de-ch.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de-ch.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/de.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/el.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/el.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-au.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-au.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-gb.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/en-gb.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eo.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eo.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es-co.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es-co.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/es.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/et.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/et.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eu.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/eu.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fa.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fa.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fi.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fi.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fr.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/fr.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gl.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gl.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gu.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/gu.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/he.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/he.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hi.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hi.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hr.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hr.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hu.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/hu.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/id.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/id.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/it.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/it.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ja.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ja.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/jv.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/jv.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/km.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/km.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kn.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/kn.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ko.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ko.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ku.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ku.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lt.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lt.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lv.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/lv.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ms.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ms.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nb.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nb.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ne.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ne.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nl.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/nl.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/no.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/no.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pl.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pl.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt-br.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt-br.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/pt.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ro.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ro.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ru.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ru.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/si.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/si.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sk.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sk.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sl.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sl.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sq.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sq.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr-latn.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr-latn.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sr.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sv.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/sv.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/th.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/th.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tk.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tk.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tr.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tr.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tt.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/tt.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ug.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ug.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uk.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uk.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ur.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/ur.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uz.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/uz.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/vi.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/vi.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh-cn.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh-cn.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/dist/translations/zh.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/src/ckeditor.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/src/ckeditor.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/static/django_ckeditor_5/src/override-django.css` & `django-ckeditor-5-0.2.7/django_ckeditor_5/static/django_ckeditor_5/src/override-django.css`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/views.py` & `django-ckeditor-5-0.2.7/django_ckeditor_5/views.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/webpack.config.js` & `django-ckeditor-5-0.2.7/django_ckeditor_5/webpack.config.js`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/widgets.py` & `django-ckeditor-5-0.2.7/django_ckeditor_5/widgets.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5/yarn.lock` & `django-ckeditor-5-0.2.7/django_ckeditor_5/yarn.lock`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/PKG-INFO` & `django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-ckeditor-5
-Version: 0.2.5
+Version: 0.2.7
 Summary: CKEditor 5 for Django.
 Author-email: Vladislav Khoboko <vladislah@gmail.com>
 License: BSD-3-Clause
 Project-URL: homepage, https://pypi.org/project/django-ckeditor-5/
 Project-URL: repository, https://github.com/hvlads/django-ckeditor-5
 Keywords: CKEditor,CKEditor5,Django
 Classifier: Environment :: Web Environment
```

### Comparing `django-ckeditor-5-0.2.5/django_ckeditor_5.egg-info/SOURCES.txt` & `django-ckeditor-5-0.2.7/django_ckeditor_5.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/articles/forms.py` & `django-ckeditor-5-0.2.7/example/blog/articles/forms.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/articles/migrations/0001_initial.py` & `django-ckeditor-5-0.2.7/example/blog/articles/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/articles/models.py` & `django-ckeditor-5-0.2.7/example/blog/articles/models.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/articles/templates/articles/article_detail.html` & `django-ckeditor-5-0.2.7/example/blog/articles/templates/articles/article_detail.html`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/articles/views.py` & `django-ckeditor-5-0.2.7/example/blog/articles/views.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/blog/settings.py` & `django-ckeditor-5-0.2.7/example/blog/blog/settings.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/blog/urls.py` & `django-ckeditor-5-0.2.7/example/blog/blog/urls.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/fixtures/files/test.png` & `django-ckeditor-5-0.2.7/example/blog/fixtures/files/test.png`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/manage.py` & `django-ckeditor-5-0.2.7/example/blog/manage.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/static_files/custom.css` & `django-ckeditor-5-0.2.7/example/blog/static_files/custom.css`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/tests/coverage.xml` & `django-ckeditor-5-0.2.7/example/blog/tests/coverage.xml`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/example/blog/tests/test_upload_file.py` & `django-ckeditor-5-0.2.7/example/blog/tests/test_upload_file.py`

 * *Files identical despite different names*

### Comparing `django-ckeditor-5-0.2.5/pyproject.toml` & `django-ckeditor-5-0.2.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 [project]
 name = "django-ckeditor-5"
 description = "CKEditor 5 for Django."
 keywords = ["CKEditor", "CKEditor5", "Django"]
 license = {text = "BSD-3-Clause"}
 readme = "README.rst"
 requires-python = ">=3.7"
-version = "0.2.5"
+version = "0.2.7"
 
 authors = [
     {"name" = "Vladislav Khoboko", "email" = "vladislah@gmail.com"},
 ]
 
 classifiers = [
         "Environment :: Web Environment",
```

