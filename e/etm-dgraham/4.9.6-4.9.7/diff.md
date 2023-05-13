# Comparing `tmp/etm-dgraham-4.9.6.tar.gz` & `tmp/etm-dgraham-4.9.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "etm-dgraham-4.9.6.tar", last modified: Tue Nov 15 13:44:00 2022, max compression
+gzip compressed data, was "etm-dgraham-4.9.7.tar", last modified: Tue Nov 15 18:42:54 2022, max compression
```

## Comparing `etm-dgraham-4.9.6.tar` & `etm-dgraham-4.9.7.tar`

### file list

```diff
@@ -1,48 +1,48 @@
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.552894 etm-dgraham-4.9.6/
--rw-r--r--   0 dag        (501) staff       (20)     3480 2022-11-15 13:40:42.000000 etm-dgraham-4.9.6/CHANGES.txt
--rw-rw-rw-   0 dag        (501) staff       (20)       37 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/MANIFEST.in
--rw-r--r--   0 dag        (501) staff       (20)   117499 2022-11-15 13:44:00.552752 etm-dgraham-4.9.6/PKG-INFO
--rw-r--r--   0 dag        (501) staff       (20)   116587 2022-11-15 01:37:02.000000 etm-dgraham-4.9.6/README.md
--rw-rw-rw-   0 dag        (501) staff       (20)       25 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/_config.yml
--rwxr-xr-x   0 dag        (501) staff       (20)     3572 2022-01-11 23:35:52.000000 etm-dgraham-4.9.6/bump.py
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.545695 etm-dgraham-4.9.6/docs/
--rwxr-xr-x   0 dag        (501) staff       (20)     7571 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/docs/index_konnections.md
--rwxr-xr-x   0 dag        (501) staff       (20)     8246 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/docs/index_usedtime.md
--rwxr-xr-x   0 dag        (501) staff       (20)     4732 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/docs/multiple_timers.md
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.548719 etm-dgraham-4.9.6/etm/
--rwxr-xr-x   0 dag        (501) staff       (20)        0 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/etm/__init__.py
--rwxr-xr-x   0 dag        (501) staff       (20)     9461 2022-11-11 17:43:50.000000 etm-dgraham-4.9.6/etm/__main__.py
--rwxr-xr-x   0 dag        (501) staff       (20)       17 2022-11-15 13:40:42.000000 etm-dgraham-4.9.6/etm/__version__.py
--rwxr-xr-x   0 dag        (501) staff       (20)    10739 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/etm/data.py
--rwxr-xr-x   0 dag        (501) staff       (20)    20798 2022-06-28 16:10:19.000000 etm-dgraham-4.9.6/etm/ical.py
--rwxr-xr-x   0 dag        (501) staff       (20)   252757 2022-11-13 21:52:18.000000 etm-dgraham-4.9.6/etm/model.py
--rwxr-xr-x   0 dag        (501) staff       (20)    32495 2022-11-13 19:09:25.000000 etm-dgraham-4.9.6/etm/options.py
--rwxr-xr-x   0 dag        (501) staff       (20)    23699 2022-11-15 13:40:42.000000 etm-dgraham-4.9.6/etm/report.py
--rwxr-xr-x   0 dag        (501) staff       (20)    86147 2022-11-15 13:40:42.000000 etm-dgraham-4.9.6/etm/view.py
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.550791 etm-dgraham-4.9.6/etm_dgraham.egg-info/
--rwxrwxrwx   0 dag        (501) staff       (20)   117499 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/PKG-INFO
--rwxrwxrwx   0 dag        (501) staff       (20)   102652 2020-06-03 14:25:34.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/PKG-INFO [conflicted]
--rwxrwxrwx   0 dag        (501) staff       (20)      504 2020-06-03 14:25:34.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/SOURCES [conflicted].txt
--rwxrwxrwx   0 dag        (501) staff       (20)      886 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/SOURCES.txt
--rwxrwxrwx   0 dag        (501) staff       (20)        1 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/dependency_links.txt
--rwxrwxrwx   0 dag        (501) staff       (20)       71 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/entry_points.txt
--rwxrwxrwx   0 dag        (501) staff       (20)      316 2020-06-03 14:25:34.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/requires [conflicted].txt
--rwxrwxrwx   0 dag        (501) staff       (20)      333 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/requires.txt
--rwxrwxrwx   0 dag        (501) staff       (20)        4 2020-06-03 14:25:34.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/top_level [conflicted].txt
--rwxrwxrwx   0 dag        (501) staff       (20)        4 2022-11-15 13:44:00.000000 etm-dgraham-4.9.6/etm_dgraham.egg-info/top_level.txt
--rw-rw-rw-   0 dag        (501) staff       (20)    28934 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/etmlogo.png
--rw-rw-rw-   0 dag        (501) staff       (20)     7047 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/etmlogo_small.png
--rw-rw-rw-   0 dag        (501) staff       (20)    36594 2020-07-27 15:42:26.000000 etm-dgraham-4.9.6/etmview_agenda.png
--rwxrwxrwx   0 dag        (501) staff       (20)     1005 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/namedcolors.py
--rw-rw-rw-   0 dag        (501) staff       (20)    91778 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/new.png
--rw-rw-rw-   0 dag        (501) staff       (20)      326 2020-06-03 13:02:08.000000 etm-dgraham-4.9.6/requirements.txt
--rw-r--r--   0 dag        (501) staff       (20)       38 2022-11-15 13:44:00.552927 etm-dgraham-4.9.6/setup.cfg
--rwxr-xr-x   0 dag        (501) staff       (20)     5110 2022-10-24 21:26:00.000000 etm-dgraham-4.9.6/setup.py
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.550923 etm-dgraham-4.9.6/test/
--rw-r--r--   0 dag        (501) staff       (20)     1155 2022-03-22 15:05:47.000000 etm-dgraham-4.9.6/test/test_parser.py
-drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 13:44:00.552363 etm-dgraham-4.9.6/utilities/
--rwxr-xr-x   0 dag        (501) staff       (20)     1078 2021-12-29 14:26:10.000000 etm-dgraham-4.9.6/utilities/colons_to_slashes.py
--rwxrwxrwx   0 dag        (501) staff       (20)     2089 2020-07-27 15:42:26.000000 etm-dgraham-4.9.6/utilities/etm_in
--rwxrwxrwx   0 dag        (501) staff       (20)     4834 2020-10-30 02:00:48.000000 etm-dgraham-4.9.6/utilities/inbasket
--rwxrwxrwx   0 dag        (501) staff       (20)     4123 2020-07-29 20:29:15.000000 etm-dgraham-4.9.6/utilities/make_examples.py
--rwxrwxrwx   0 dag        (501) staff       (20)      643 2020-10-20 14:57:04.000000 etm-dgraham-4.9.6/utilities/open_in_mutt
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.831356 etm-dgraham-4.9.7/
+-rw-r--r--   0 dag        (501) staff       (20)     3417 2022-11-15 18:34:18.000000 etm-dgraham-4.9.7/CHANGES.txt
+-rw-rw-rw-   0 dag        (501) staff       (20)       37 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/MANIFEST.in
+-rw-r--r--   0 dag        (501) staff       (20)   117499 2022-11-15 18:42:54.831200 etm-dgraham-4.9.7/PKG-INFO
+-rw-r--r--   0 dag        (501) staff       (20)   116587 2022-11-15 01:37:02.000000 etm-dgraham-4.9.7/README.md
+-rw-rw-rw-   0 dag        (501) staff       (20)       25 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/_config.yml
+-rwxr-xr-x   0 dag        (501) staff       (20)     3862 2022-11-15 18:30:57.000000 etm-dgraham-4.9.7/bump.py
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.823535 etm-dgraham-4.9.7/docs/
+-rwxr-xr-x   0 dag        (501) staff       (20)     7571 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/docs/index_konnections.md
+-rwxr-xr-x   0 dag        (501) staff       (20)     8246 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/docs/index_usedtime.md
+-rwxr-xr-x   0 dag        (501) staff       (20)     4732 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/docs/multiple_timers.md
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.827174 etm-dgraham-4.9.7/etm/
+-rwxr-xr-x   0 dag        (501) staff       (20)        0 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/etm/__init__.py
+-rwxr-xr-x   0 dag        (501) staff       (20)     9461 2022-11-11 17:43:50.000000 etm-dgraham-4.9.7/etm/__main__.py
+-rwxr-xr-x   0 dag        (501) staff       (20)       17 2022-11-15 18:34:18.000000 etm-dgraham-4.9.7/etm/__version__.py
+-rwxr-xr-x   0 dag        (501) staff       (20)    10739 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/etm/data.py
+-rwxr-xr-x   0 dag        (501) staff       (20)    20798 2022-06-28 16:10:19.000000 etm-dgraham-4.9.7/etm/ical.py
+-rwxr-xr-x   0 dag        (501) staff       (20)   252804 2022-11-15 18:34:18.000000 etm-dgraham-4.9.7/etm/model.py
+-rwxr-xr-x   0 dag        (501) staff       (20)    32495 2022-11-13 19:09:25.000000 etm-dgraham-4.9.7/etm/options.py
+-rwxr-xr-x   0 dag        (501) staff       (20)    23699 2022-11-15 13:40:42.000000 etm-dgraham-4.9.7/etm/report.py
+-rwxr-xr-x   0 dag        (501) staff       (20)    86196 2022-11-15 18:34:18.000000 etm-dgraham-4.9.7/etm/view.py
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.829309 etm-dgraham-4.9.7/etm_dgraham.egg-info/
+-rwxrwxrwx   0 dag        (501) staff       (20)   117499 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/PKG-INFO
+-rwxrwxrwx   0 dag        (501) staff       (20)   102652 2020-06-03 14:25:34.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/PKG-INFO [conflicted]
+-rwxrwxrwx   0 dag        (501) staff       (20)      504 2020-06-03 14:25:34.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/SOURCES [conflicted].txt
+-rwxrwxrwx   0 dag        (501) staff       (20)      886 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/SOURCES.txt
+-rwxrwxrwx   0 dag        (501) staff       (20)        1 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/dependency_links.txt
+-rwxrwxrwx   0 dag        (501) staff       (20)       71 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/entry_points.txt
+-rwxrwxrwx   0 dag        (501) staff       (20)      316 2020-06-03 14:25:34.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/requires [conflicted].txt
+-rwxrwxrwx   0 dag        (501) staff       (20)      333 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/requires.txt
+-rwxrwxrwx   0 dag        (501) staff       (20)        4 2020-06-03 14:25:34.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/top_level [conflicted].txt
+-rwxrwxrwx   0 dag        (501) staff       (20)        4 2022-11-15 18:42:54.000000 etm-dgraham-4.9.7/etm_dgraham.egg-info/top_level.txt
+-rw-rw-rw-   0 dag        (501) staff       (20)    28934 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/etmlogo.png
+-rw-rw-rw-   0 dag        (501) staff       (20)     7047 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/etmlogo_small.png
+-rw-rw-rw-   0 dag        (501) staff       (20)    36594 2020-07-27 15:42:26.000000 etm-dgraham-4.9.7/etmview_agenda.png
+-rwxrwxrwx   0 dag        (501) staff       (20)     1005 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/namedcolors.py
+-rw-rw-rw-   0 dag        (501) staff       (20)    91778 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/new.png
+-rw-rw-rw-   0 dag        (501) staff       (20)      326 2020-06-03 13:02:08.000000 etm-dgraham-4.9.7/requirements.txt
+-rw-r--r--   0 dag        (501) staff       (20)       38 2022-11-15 18:42:54.831391 etm-dgraham-4.9.7/setup.cfg
+-rwxr-xr-x   0 dag        (501) staff       (20)     5110 2022-10-24 21:26:00.000000 etm-dgraham-4.9.7/setup.py
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.829431 etm-dgraham-4.9.7/test/
+-rw-r--r--   0 dag        (501) staff       (20)     1155 2022-03-22 15:05:47.000000 etm-dgraham-4.9.7/test/test_parser.py
+drwxr-xr-x   0 dag        (501) staff       (20)        0 2022-11-15 18:42:54.830787 etm-dgraham-4.9.7/utilities/
+-rwxr-xr-x   0 dag        (501) staff       (20)     1078 2021-12-29 14:26:10.000000 etm-dgraham-4.9.7/utilities/colons_to_slashes.py
+-rwxrwxrwx   0 dag        (501) staff       (20)     2089 2020-07-27 15:42:26.000000 etm-dgraham-4.9.7/utilities/etm_in
+-rwxrwxrwx   0 dag        (501) staff       (20)     4834 2020-10-30 02:00:48.000000 etm-dgraham-4.9.7/utilities/inbasket
+-rwxrwxrwx   0 dag        (501) staff       (20)     4123 2020-07-29 20:29:15.000000 etm-dgraham-4.9.7/utilities/make_examples.py
+-rwxrwxrwx   0 dag        (501) staff       (20)      643 2020-10-20 14:57:04.000000 etm-dgraham-4.9.7/utilities/open_in_mutt
```

### Comparing `etm-dgraham-4.9.6/CHANGES.txt` & `etm-dgraham-4.9.7/CHANGES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -1,13 +1,21 @@
-Recent tagged changes as of 2022-11-15T08:40:16.307569-05:00:
-- 0 seconds ago (HEAD -> busy, tag: 4.9.6) Daniel Graham
+Recent tagged changes as of 2022-11-15T13:34:13.719827-05:00:
+- 0 seconds ago (HEAD -> working, tag: 4.9.7) Daniel Graham
+    b4f22a66 2022-11-15 13:34:13 -0500
+    Tagged version 4.9.7.
+
+- 14 minutes ago (tag: 4.9.8) Daniel Graham
+    3e3e5c77 2022-11-15 13:20:24 -0500
+    Tagged version 4.9.8.
+
+- 5 hours ago (tag: 4.9.6) Daniel Graham
     6015ec88 2022-11-15 08:40:16 -0500
     Tagged version 4.9.6.
 
-- 12 hours ago (tag: 4.9.5) Daniel Graham
+- 17 hours ago (tag: 4.9.5) Daniel Graham
     250004cc 2022-11-14 20:36:44 -0500
     Tagged version 4.9.5. Added support for argument replacements in
     saved queries.
 
 - 3 days ago (tag: 4.9.4) Daniel Graham
     c71d75c2 2022-11-12 12:10:39 -0500
     Tagged version 4.9.4. Restore cursor position after auto refresh
@@ -83,16 +91,7 @@
 - 4 weeks ago (tag: 4.7.17) Daniel Graham
     475d89a9 2022-10-17 08:03:21 -0400
     Tagged version 4.7.17.
 
 - 5 weeks ago (tag: 4.7.16) Daniel Graham
     90083942 2022-10-14 11:14:51 -0400
     Tagged version 4.7.16.
-
-- 5 months ago (tag: 4.7.15) Daniel Graham
-    f449fc6d 2022-06-28 12:52:48 -0400
-    Tagged version 4.7.15.
-
-- 5 months ago (tag: 4.7.14) Daniel Graham
-    c47de41b 2022-06-28 12:10:03 -0400
-    Tagged version 4.7.14. Handle missing summaries and UTC datetimes
-    in ics imports.
```

### Comparing `etm-dgraham-4.9.6/PKG-INFO` & `etm-dgraham-4.9.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: etm-dgraham
-Version: 4.9.6
+Version: 4.9.7
 Summary: event and task manager
 Home-page: https://dagraham.github.io/etm-dgraham/
 Author: Daniel A Graham
 Author-email: dnlgrhm@gmail.com
 License: GPL
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `etm-dgraham-4.9.6/README.md` & `etm-dgraham-4.9.7/README.md`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/bump.py` & `etm-dgraham-4.9.7/bump.py`

 * *Files 8% similar despite different names*

```diff
@@ -123,10 +123,18 @@
     check_output(f"git tag -a -f '{new_version}' -m '{version_info}'")
 
     count = 20
     check_output(f"echo 'Recent tagged changes as of {pendulum.now()}:' > CHANGES.txt")
     check_output(f"git log --pretty=format:'- %ar%d %an%n    %h %ai%n%w(70,4,4)%B' --max-count={count} --no-walk --tags >> CHANGES.txt")
     check_output(f"git commit -a --amend -m '{tmsg}'")
 
+    ans = input("switch to master, merge working and push to origin? [yN] ")
+    if ans.lower() != 'y':
+        print('cancelled')
+        sys.exit()
+    ok, res = check_output(f"git checkout master && git merge working && git push && git checkout working")
+    if res:
+        print(res)
+
 else:
     print(f"retained version: {version}")
```

### Comparing `etm-dgraham-4.9.6/docs/index_konnections.md` & `etm-dgraham-4.9.7/docs/index_konnections.md`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/docs/index_usedtime.md` & `etm-dgraham-4.9.7/docs/index_usedtime.md`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/docs/multiple_timers.md` & `etm-dgraham-4.9.7/docs/multiple_timers.md`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/__main__.py` & `etm-dgraham-4.9.7/etm/__main__.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/data.py` & `etm-dgraham-4.9.7/etm/data.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/ical.py` & `etm-dgraham-4.9.7/etm/ical.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/model.py` & `etm-dgraham-4.9.7/etm/model.py`

 * *Files 0% similar despite different names*

```diff
@@ -6398,18 +6398,18 @@
                         sort_dt = sort_dt[:-4] + '24%%'
 
 
                 dtb = None
                 dta = None
 
                 if item['itemtype'] == '*' and 'w' in item:
-                    itemtype = "~"
                     b, a = item['w']
                     dtb = dt - b if b else None
                     if dtb:
+                        itemtype = "↱"
                         sort_b = dtb.format("YYYYMMDDHHmm")
                         rhb = fmt_time(dtb).ljust(rhc_width, ' ')
                         rows.append(
                                 {
                                     'id': item.doc_id,
                                     'job': None,
                                     'instance': instance,
@@ -6453,14 +6453,15 @@
                 if item['itemtype'] == '*' and 'w' in item:
                     if 'e' in item:
                         dta = dt + item['e'] + a if a else None
                     else:
                         dta = dt + a if a else None
 
                     if dta:
+                        itemtype = "↳"
                         sort_a = dta.format("YYYYMMDDHHmm")
                         rha = fmt_time(dta).rjust(rhc_width, ' ')
                         rows.append(
                                 {
                                     'id': item.doc_id,
                                     'job': None,
                                     'instance': instance,
```

### Comparing `etm-dgraham-4.9.6/etm/options.py` & `etm-dgraham-4.9.7/etm/options.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/report.py` & `etm-dgraham-4.9.7/etm/report.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm/view.py` & `etm-dgraham-4.9.7/etm/view.py`

 * *Files 0% similar despite different names*

```diff
@@ -1176,15 +1176,17 @@
         '<': 'pastdue',
         '>': 'begin',
         '%': 'journal',
         '*': 'event',
         '-': 'available',
         '+': 'waiting',
         '✓': 'finished',
-        '~': 'wrap',
+        '~': 'missing',
+        '↱': 'wrap',
+        '↳': 'wrap',
         }
 
 def first_char(s):
     """
     Return the first non-whitespace character in s.
     """
     if not s.strip():
```

### Comparing `etm-dgraham-4.9.6/etm_dgraham.egg-info/PKG-INFO` & `etm-dgraham-4.9.7/etm_dgraham.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: etm-dgraham
-Version: 4.9.6
+Version: 4.9.7
 Summary: event and task manager
 Home-page: https://dagraham.github.io/etm-dgraham/
 Author: Daniel A Graham
 Author-email: dnlgrhm@gmail.com
 License: GPL
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `etm-dgraham-4.9.6/etm_dgraham.egg-info/PKG-INFO [conflicted]` & `etm-dgraham-4.9.7/etm_dgraham.egg-info/PKG-INFO [conflicted]`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etm_dgraham.egg-info/SOURCES.txt` & `etm-dgraham-4.9.7/etm_dgraham.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etmlogo.png` & `etm-dgraham-4.9.7/etmlogo.png`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etmlogo_small.png` & `etm-dgraham-4.9.7/etmlogo_small.png`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/etmview_agenda.png` & `etm-dgraham-4.9.7/etmview_agenda.png`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/namedcolors.py` & `etm-dgraham-4.9.7/namedcolors.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/new.png` & `etm-dgraham-4.9.7/new.png`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/setup.py` & `etm-dgraham-4.9.7/setup.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/test/test_parser.py` & `etm-dgraham-4.9.7/test/test_parser.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/utilities/colons_to_slashes.py` & `etm-dgraham-4.9.7/utilities/colons_to_slashes.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/utilities/etm_in` & `etm-dgraham-4.9.7/utilities/etm_in`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/utilities/inbasket` & `etm-dgraham-4.9.7/utilities/inbasket`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/utilities/make_examples.py` & `etm-dgraham-4.9.7/utilities/make_examples.py`

 * *Files identical despite different names*

### Comparing `etm-dgraham-4.9.6/utilities/open_in_mutt` & `etm-dgraham-4.9.7/utilities/open_in_mutt`

 * *Files identical despite different names*

