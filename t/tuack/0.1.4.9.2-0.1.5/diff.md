# Comparing `tmp/tuack-0.1.4.9.2.tar.gz` & `tmp/tuack-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\tuack-0.1.4.9.2.tar", last modified: Wed Jan 15 09:03:23 2020, max compression
+gzip compressed data, was "tuack-0.1.5.tar", last modified: Sat May 13 04:22:15 2023, max compression
```

## Comparing `tuack-0.1.4.9.2.tar` & `tuack-0.1.5.tar`

### file list

```diff
@@ -1,105 +1,107 @@
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/
--rw-rw-rw-   0        0        0       17 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/MANIFEST.in
--rw-rw-rw-   0        0        0      440 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/PKG-INFO
--rw-rw-rw-   0        0        0     1649 2019-10-16 02:22:58.000000 tuack-0.1.4.9.2/README.md
--rw-rw-rw-   0        0        0       42 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/setup.cfg
--rw-rw-rw-   0        0        0     1760 2020-01-15 09:02:49.000000 tuack-0.1.4.9.2/setup.py
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/
--rw-rw-rw-   0        0        0      116 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/__init__.py
--rw-rw-rw-   0        0        0    31194 2020-01-07 12:45:54.000000 tuack-0.1.4.9.2/tuack/base.py
--rw-rw-rw-   0        0        0    12826 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/doc.py
--rw-rw-rw-   0        0        0    20793 2020-01-07 12:21:32.000000 tuack-0.1.4.9.2/tuack/dump.py
--rw-rw-rw-   0        0        0    14100 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/gen.py
--rw-rw-rw-   0        0        0     2252 2019-07-04 06:53:24.000000 tuack-0.1.4.9.2/tuack/install.py
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/lex/
--rw-rw-rw-   0        0        0        0 2018-09-07 13:38:42.000000 tuack-0.1.4.9.2/tuack/lex/compile.log
--rw-rw-rw-   0        0        0      971 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/compile.pyinc
--rw-rw-rw-   0        0        0  2295192 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/format-linux
--rw-rw-rw-   0        0        0    61896 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/format-mac
--rwxrwxrwx   0        0        0  2178321 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/format-win.exe
--rw-rw-rw-   0        0        0      320 2018-08-27 16:45:43.000000 tuack-0.1.4.9.2/tuack/lex/hehe.log
--rw-rw-rw-   0        0        0    11191 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/lex.l
--rw-rw-rw-   0        0        0    94066 2018-09-07 13:38:42.000000 tuack-0.1.4.9.2/tuack/lex/lex.yy.c
--rw-rw-rw-   0        0        0    36942 2018-06-11 12:35:41.000000 tuack-0.1.4.9.2/tuack/lex/lex.yy.o
--rw-rw-rw-   0        0        0      185 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/main.h
--rw-rw-rw-   0        0        0    42594 2018-09-07 13:38:42.000000 tuack-0.1.4.9.2/tuack/lex/yacc.tab.c
--rw-rw-rw-   0        0        0     1906 2018-09-07 13:38:42.000000 tuack-0.1.4.9.2/tuack/lex/yacc.tab.h
--rw-rw-rw-   0        0        0     9007 2018-06-11 12:35:41.000000 tuack-0.1.4.9.2/tuack/lex/yacc.tab.o
--rw-rw-rw-   0        0        0      388 2019-01-19 08:45:10.000000 tuack-0.1.4.9.2/tuack/lex/yacc.y
--rw-rw-rw-   0        0        0    11826 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/load.py
--rw-rw-rw-   0        0        0     3605 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/num2chinese.py
--rw-rw-rw-   0        0        0    12608 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/packer.py
--rw-rw-rw-   0        0        0    22613 2020-01-11 13:37:36.000000 tuack-0.1.4.9.2/tuack/ren.py
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample/
--rw-rw-rw-   0        0        0     7909 2019-07-04 06:53:24.000000 tuack-0.1.4.9.2/tuack/sample/arbiter_e.sample
--rw-rw-rw-   0        0        0     2104 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample/chk.cpp
--rw-rw-rw-   0        0        0      170 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/sample/contest.gitignore
--rw-rw-rw-   0        0        0      251 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/sample/contest.json
--rw-rw-rw-   0        0        0      162 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample/day.gitignore
--rw-rw-rw-   0        0        0      197 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/sample/day.json
--rw-rw-rw-   0        0        0      342 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample/empty.gitattributes
--rw-rw-rw-   0        0        0      222 2020-01-07 12:45:54.000000 tuack-0.1.4.9.2/tuack/sample/empty.gitignore
--rw-rw-rw-   0        0        0      411 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample/empty.json
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample/precautions/
--rw-rw-rw-   0        0        0       56 2019-07-04 06:53:24.000000 tuack-0.1.4.9.2/tuack/sample/precautions/zh-cn.md
--rw-rw-rw-   0        0        0      342 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/sample/problem.gitattributes
--rw-rw-rw-   0        0        0      222 2020-01-07 12:45:54.000000 tuack-0.1.4.9.2/tuack/sample/problem.gitignore
--rw-rw-rw-   0        0        0      439 2019-07-04 06:53:24.000000 tuack-0.1.4.9.2/tuack/sample/problem.json
--rw-rw-rw-   0        0        0       76 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/sample/uoj.json
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:21.000000 tuack-0.1.4.9.2/tuack/sample-empty/
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-empty/statement/
--rw-rw-rw-   0        0        0      380 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-empty/statement/zh-cn.md
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:21.000000 tuack-0.1.4.9.2/tuack/sample-problem/
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/data/
--rw-rw-rw-   0        0        0       43 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/data/1.ans
--rw-rw-rw-   0        0        0       42 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/data/1.in
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/down/
--rw-rw-rw-   0        0        0       77 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/down/1.ans
--rw-rw-rw-   0        0        0       75 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/down/1.in
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/pre/
--rw-rw-rw-   0        0        0       78 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/pre/1.ans
--rw-rw-rw-   0        0        0       76 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/pre/1.in
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/resources/
--rw-rw-rw-   0        0        0  3293583 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/resources/sample.png
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/solution/
--rw-rw-rw-   0        0        0     1940 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/solution/zh-cn.md
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/statement/
--rw-rw-rw-   0        0        0     6385 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/statement/zh-cn.md
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack/sample-problem/tables/
--rw-rw-rw-   0        0        0     1141 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/tables/data.pyinc
--rw-rw-rw-   0        0        0     1181 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/tables/json_data.json
--rw-rw-rw-   0        0        0      198 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/sample-problem/tables/table.json
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/tuack/templates/
--rw-rw-rw-   0        0        0      862 2019-07-28 04:19:11.000000 tuack-0.1.4.9.2/tuack/templates/ccc.tex.jinja
--rw-rw-rw-   0        0        0    71170 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/templates/ccpc.png
--rw-rw-rw-   0        0        0     1166 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/ccpc.tex.jinja
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:21.000000 tuack-0.1.4.9.2/tuack/templates/en/
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/tuack/templates/en/LC_MESSAGES/
--rw-rw-rw-   0        0        0     2978 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/en/LC_MESSAGES/lang.mo
--rw-rw-rw-   0        0        0     3681 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/en/LC_MESSAGES/lang.po
--rw-rw-rw-   0        0        0       77 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/font.html.jinja
--rw-rw-rw-   0        0        0       70 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/font.tex.jinja
--rw-rw-rw-   0        0        0      627 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/hand.tex.jinja
--rw-rw-rw-   0        0        0      141 2019-10-16 02:12:01.000000 tuack-0.1.4.9.2/tuack/templates/image.html.jinja
--rw-rw-rw-   0        0        0      504 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/image.tex.jinja
--rw-rw-rw-   0        0        0     4764 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/problem_base.md.jinja
--rw-rw-rw-   0        0        0     1051 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/table.html.jinja
--rw-rw-rw-   0        0        0      386 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/table.md.jinja
--rw-rw-rw-   0        0        0     2295 2018-03-03 08:40:18.000000 tuack-0.1.4.9.2/tuack/templates/table.tex.jinja
--rw-rw-rw-   0        0        0     2032 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/template_base.tex.jinja
--rw-rw-rw-   0        0        0      182 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/template_base.tex.jinja.tex
--rw-rw-rw-   0        0        0    10611 2020-01-11 14:07:15.000000 tuack-0.1.4.9.2/tuack/templates/tuack.cls
--rw-rw-rw-   0        0        0     8162 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/templates/tuoi.tex.jinja
--rw-rw-rw-   0        0        0     1358 2019-07-04 06:53:25.000000 tuack-0.1.4.9.2/tuack/templates/tupc.tex.jinja
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:21.000000 tuack-0.1.4.9.2/tuack/templates/zh-cn/
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:23.000000 tuack-0.1.4.9.2/tuack/templates/zh-cn/LC_MESSAGES/
--rw-rw-rw-   0        0        0     2996 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/zh-cn/LC_MESSAGES/lang.mo
--rw-rw-rw-   0        0        0     3213 2019-01-19 08:45:11.000000 tuack-0.1.4.9.2/tuack/templates/zh-cn/LC_MESSAGES/lang.po
--rw-rw-rw-   0        0        0    16856 2020-01-07 11:56:00.000000 tuack-0.1.4.9.2/tuack/test.py
--rw-rw-rw-   0        0        0     3084 2019-07-04 06:53:25.000000 tuack-0.1.4.9.2/tuack/tools.py
-drwxrwxrwx   0        0        0        0 2020-01-15 09:03:22.000000 tuack-0.1.4.9.2/tuack.egg-info/
--rw-rw-rw-   0        0        0      440 2020-01-15 09:03:19.000000 tuack-0.1.4.9.2/tuack.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2212 2020-01-15 09:03:20.000000 tuack-0.1.4.9.2/tuack.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2020-01-15 09:03:19.000000 tuack-0.1.4.9.2/tuack.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       53 2020-01-15 09:03:19.000000 tuack-0.1.4.9.2/tuack.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2020-01-15 09:03:19.000000 tuack-0.1.4.9.2/tuack.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.336016 tuack-0.1.5/
+-rw-rw-rw-   0        0        0    35055 2019-01-19 08:45:12.000000 tuack-0.1.5/LICENSE
+-rw-rw-rw-   0        0        0       17 2018-03-03 08:40:20.000000 tuack-0.1.5/MANIFEST.in
+-rw-rw-rw-   0        0        0      518 2023-05-13 04:22:15.336016 tuack-0.1.5/PKG-INFO
+-rw-rw-rw-   0        0        0     1717 2023-01-09 01:26:59.000000 tuack-0.1.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 04:22:15.336016 tuack-0.1.5/setup.cfg
+-rw-rw-rw-   0        0        0     1926 2023-05-13 04:18:17.000000 tuack-0.1.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.885832 tuack-0.1.5/tuack/
+-rw-rw-rw-   0        0        0      116 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/__init__.py
+-rw-rw-rw-   0        0        0    34145 2023-05-13 04:08:47.000000 tuack-0.1.5/tuack/base.py
+-rw-rw-rw-   0        0        0    13348 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/doc.py
+-rw-rw-rw-   0        0        0    27313 2023-05-13 04:13:10.000000 tuack-0.1.5/tuack/dump.py
+-rw-rw-rw-   0        0        0    14486 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/gen.py
+-rw-rw-rw-   0        0        0     2334 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/install.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.097790 tuack-0.1.5/tuack/lex/
+-rw-rw-rw-   0        0        0        0 2018-09-07 13:38:42.000000 tuack-0.1.5/tuack/lex/compile.log
+-rw-rw-rw-   0        0        0      971 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/compile.pyinc
+-rw-rw-rw-   0        0        0  2295192 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/format-linux
+-rw-rw-rw-   0        0        0    61896 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/format-mac
+-rwxrwxrwx   0        0        0  2178321 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/format-win.exe
+-rw-rw-rw-   0        0        0      320 2018-08-27 16:45:44.000000 tuack-0.1.5/tuack/lex/hehe.log
+-rw-rw-rw-   0        0        0    11191 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/lex.l
+-rw-rw-rw-   0        0        0    94066 2018-09-07 13:38:44.000000 tuack-0.1.5/tuack/lex/lex.yy.c
+-rw-rw-rw-   0        0        0    36942 2018-06-11 12:35:42.000000 tuack-0.1.5/tuack/lex/lex.yy.o
+-rw-rw-rw-   0        0        0      185 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/main.h
+-rw-rw-rw-   0        0        0    42594 2018-09-07 13:38:44.000000 tuack-0.1.5/tuack/lex/yacc.tab.c
+-rw-rw-rw-   0        0        0     1906 2018-09-07 13:38:44.000000 tuack-0.1.5/tuack/lex/yacc.tab.h
+-rw-rw-rw-   0        0        0     9007 2018-06-11 12:35:42.000000 tuack-0.1.5/tuack/lex/yacc.tab.o
+-rw-rw-rw-   0        0        0      388 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/lex/yacc.y
+-rw-rw-rw-   0        0        0    12225 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/load.py
+-rw-rw-rw-   0        0        0     3605 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/num2chinese.py
+-rw-rw-rw-   0        0        0    12608 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/packer.py
+-rw-rw-rw-   0        0        0    24468 2023-04-24 01:29:13.000000 tuack-0.1.5/tuack/ren.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.163722 tuack-0.1.5/tuack/sample/
+-rw-rw-rw-   0        0        0     7909 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/arbiter_e.noi_linux1.sample
+-rw-rw-rw-   0        0        0    23576 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/arbiter_e.sample
+-rw-rw-rw-   0        0        0     5586 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/chk.cpp
+-rw-rw-rw-   0        0        0      195 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/contest.gitignore
+-rw-rw-rw-   0        0        0      266 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/contest.json
+-rw-rw-rw-   0        0        0      186 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/day.gitignore
+-rw-rw-rw-   0        0        0      207 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/day.json
+-rw-rw-rw-   0        0        0      351 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/empty.gitattributes
+-rw-rw-rw-   0        0        0      254 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/empty.gitignore
+-rw-rw-rw-   0        0        0      435 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/empty.json
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.218786 tuack-0.1.5/tuack/sample/precautions/
+-rw-rw-rw-   0        0        0       60 2022-08-12 11:20:32.000000 tuack-0.1.5/tuack/sample/precautions/zh-cn.md
+-rw-rw-rw-   0        0        0      342 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/sample/problem.gitattributes
+-rw-rw-rw-   0        0        0      254 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/problem.gitignore
+-rw-rw-rw-   0        0        0      466 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample/problem.json
+-rw-rw-rw-   0        0        0       76 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/sample/uoj.json
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.835087 tuack-0.1.5/tuack/sample-empty/
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.164705 tuack-0.1.5/tuack/sample-empty/statement/
+-rw-rw-rw-   0        0        0      411 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-empty/statement/zh-cn.md
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.836609 tuack-0.1.5/tuack/sample-problem/
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.175668 tuack-0.1.5/tuack/sample-problem/data/
+-rw-rw-rw-   0        0        0       44 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/data/1.ans
+-rw-rw-rw-   0        0        0       43 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/data/1.in
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.184637 tuack-0.1.5/tuack/sample-problem/down/
+-rw-rw-rw-   0        0        0       79 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/down/1.ans
+-rw-rw-rw-   0        0        0       77 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/down/1.in
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.191624 tuack-0.1.5/tuack/sample-problem/pre/
+-rw-rw-rw-   0        0        0       80 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/pre/1.ans
+-rw-rw-rw-   0        0        0       78 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/pre/1.in
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.199809 tuack-0.1.5/tuack/sample-problem/resources/
+-rw-rw-rw-   0        0        0  3293583 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/resources/sample.png
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.201798 tuack-0.1.5/tuack/sample-problem/solution/
+-rw-rw-rw-   0        0        0     1968 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/solution/zh-cn.md
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.202785 tuack-0.1.5/tuack/sample-problem/statement/
+-rw-rw-rw-   0        0        0     6819 2023-04-24 01:30:55.000000 tuack-0.1.5/tuack/sample-problem/statement/zh-cn.md
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.218786 tuack-0.1.5/tuack/sample-problem/tables/
+-rw-rw-rw-   0        0        0     1062 2023-03-28 10:24:11.000000 tuack-0.1.5/tuack/sample-problem/tables/data.pyinc
+-rw-rw-rw-   0        0        0     1227 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/tables/json_data.json
+-rw-rw-rw-   0        0        0      205 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/sample-problem/tables/table.json
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.315086 tuack-0.1.5/tuack/templates/
+-rw-rw-rw-   0        0        0      911 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/ccc.tex.jinja
+-rw-rw-rw-   0        0        0    71170 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/templates/ccpc.png
+-rw-rw-rw-   0        0        0     1240 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/ccpc.tex.jinja
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.836609 tuack-0.1.5/tuack/templates/en/
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.326051 tuack-0.1.5/tuack/templates/en/LC_MESSAGES/
+-rw-rw-rw-   0        0        0     2978 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/en/LC_MESSAGES/lang.mo
+-rw-rw-rw-   0        0        0     3681 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/en/LC_MESSAGES/lang.po
+-rw-rw-rw-   0        0        0       77 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/font.html.jinja
+-rw-rw-rw-   0        0        0       70 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/font.tex.jinja
+-rw-rw-rw-   0        0        0      670 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/hand.tex.jinja
+-rw-rw-rw-   0        0        0      144 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/image.html.jinja
+-rw-rw-rw-   0        0        0      530 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/image.tex.jinja
+-rw-rw-rw-   0        0        0     5116 2023-04-24 08:07:57.000000 tuack-0.1.5/tuack/templates/problem_base.md.jinja
+-rw-rw-rw-   0        0        0     1051 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/table.html.jinja
+-rw-rw-rw-   0        0        0      402 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/table.md.jinja
+-rw-rw-rw-   0        0        0     2295 2018-03-03 08:40:20.000000 tuack-0.1.5/tuack/templates/table.tex.jinja
+-rw-rw-rw-   0        0        0     2125 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/template_base.tex.jinja
+-rw-rw-rw-   0        0        0      182 2019-01-19 08:45:12.000000 tuack-0.1.5/tuack/templates/template_base.tex.jinja.tex
+-rw-rw-rw-   0        0        0     4756 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/tuack.cls
+-rw-rw-rw-   0        0        0     8743 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/tuoi.tex.jinja
+-rw-rw-rw-   0        0        0     1443 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/tupc.tex.jinja
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.836609 tuack-0.1.5/tuack/templates/zh-cn/
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:15.335022 tuack-0.1.5/tuack/templates/zh-cn/LC_MESSAGES/
+-rw-rw-rw-   0        0        0     3139 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/zh-cn/LC_MESSAGES/lang.mo
+-rw-rw-rw-   0        0        0     3543 2023-01-09 01:26:59.000000 tuack-0.1.5/tuack/templates/zh-cn/LC_MESSAGES/lang.po
+-rw-rw-rw-   0        0        0    17692 2023-01-09 01:27:42.000000 tuack-0.1.5/tuack/test.py
+-rw-rw-rw-   0        0        0     3777 2023-02-22 09:36:20.000000 tuack-0.1.5/tuack/tools.py
+drwxrwxrwx   0        0        0        0 2023-05-13 04:22:14.895797 tuack-0.1.5/tuack.egg-info/
+-rw-rw-rw-   0        0        0      518 2023-05-13 04:22:14.000000 tuack-0.1.5/tuack.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2261 2023-05-13 04:22:14.000000 tuack-0.1.5/tuack.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 04:22:14.000000 tuack-0.1.5/tuack.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       77 2023-05-13 04:22:14.000000 tuack-0.1.5/tuack.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-05-13 04:22:14.000000 tuack-0.1.5/tuack.egg-info/top_level.txt
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `tuack-0.1.4.9.2/README.md` & `tuack-0.1.5/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -1,24 +1,26 @@
-## 简介
-
-一般在 4 个地方更新：
-
-* [https://gitee.com/mulab/oi_tools](https://gitee.com/mulab/oi_tools)：主要的工作地址，所有分支都会在这里；可以提 issue。
-* [https://git.thusaac.com/publish/tuack](https://git.thusaac.com/publish/tuack)：最近算协服务器又没人管了，正常所有分支都会在这里；非清华贵系算协成员不能提 issue。
-* [https://saac.cs.tsinghua.edu.cn/publish/tuack](https://git.thusaac.org/publish/tuack)：清华校内的服务器现在搬到这里了。
-* [https://github.com/Mulab11/tuack](https://github.com/Mulab11/tuack)：可以提 issue，可能不会及时更新。
-
-此外如果有任何疑问或建议，知道我 QQ 或微信的小伙伴也可以用这些工具告诉我。
-
-这个轮子打算逐步实现：
-
-* 合作：通过共同使用git和遵循一些约定，降低合作命题者之间版本控制，题面修改，代码、数据交换，bug修复等的成本。
-* 规范：对题目的各个方面进行评估，找出可能出错的风险点，帮助出题人减少出锅的概率。
-* 适配：尽量支持从现有的各类评测工具导入数据和导出到各类评测工具中，实现多种格式题面的书写和导出。
-
-这个轮子主要是面向出题人、OJ站长和教师，方便大家造题和分享题目。
-
-目前这个轮子还在you开yi发dui中bug。如果希望我们支持其他格式的题面，其他工具的导入导出，对这个轮子有任何建议或意见，发现了任何bug，或是有兴趣加入我们，欢迎随时联系。
-
-## 文档
-
-[文档在这里](https://git.thusaac.com/publish/tuack/wikis/home)
+## 简介
+
+一般在 4 个地方更新：
+
+* [https://gitee.com/mulab/oi_tools](https://gitee.com/mulab/oi_tools)：主要的工作地址，所有分支都会在这里；可以提 issue。
+* [https://git.thusaac.com/publish/tuack](https://git.thusaac.com/publish/tuack)：最近算协服务器又没人管了，正常所有分支都会在这里；非清华贵系算协成员不能提 issue。
+* [https://saac.cs.tsinghua.edu.cn/publish/tuack](https://git.thusaac.org/publish/tuack)：清华校内的服务器现在搬到这里了。
+* [https://github.com/Mulab11/tuack](https://github.com/Mulab11/tuack)：可以提 issue，可能不会及时更新。
+
+此外如果有任何疑问或建议，知道我 QQ 或微信的小伙伴也可以用这些工具告诉我。
+
+这个轮子打算逐步实现：
+
+* 合作：通过共同使用git和遵循一些约定，降低合作命题者之间版本控制，题面修改，代码、数据交换，bug修复等的成本。
+* 规范：对题目的各个方面进行评估，找出可能出错的风险点，帮助出题人减少出锅的概率。
+* 适配：尽量支持从现有的各类评测工具导入数据和导出到各类评测工具中，实现多种格式题面的书写和导出。
+
+这个轮子主要是面向出题人、OJ站长和教师，方便大家造题和分享题目。
+
+目前这个轮子还在you开yi发dui中bug。如果希望我们支持其他格式的题面，其他工具的导入导出，对这个轮子有任何建议或意见，发现了任何bug，或是有兴趣加入我们，欢迎随时联系。
+
+## 文档
+
+[文档在这里](https://gitee.com/mulab/oi_tools/wikis/home)
+
+这个文档有一些图是坏的，待修。
```

### Comparing `tuack-0.1.4.9.2/setup.py` & `tuack-0.1.5/setup.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,64 +1,65 @@
-from setuptools import setup, find_packages
-from setuptools.command.develop import develop
-from setuptools.command.install import install
-from subprocess import check_call
-import platform
-
-def check():
-	system = platform.system()
-	if system == 'Linux':
-		check_call("sudo apt-get install pandoc git git-lfs".split())
-		check_call("git lfs install".split())
-	elif system == 'Darwin':
-		check_call("brew update".split())
-		check_call("brew install pandoc".split())
-		check_call("brew install git".split())
-		check_call("brew install git-lfs".split())
-		check_call("git lfs install".split())
-
-class PostDevelopCommand(develop):
-	"""Post-installation for development mode."""
-	def run(self):
-		#check()
-		develop.run(self)
-
-class PostInstallCommand(install):
-	"""Post-installation for installation mode."""
-	def run(self):
-		#check()
-		install.run(self)
-
-requires = [
-	'jinja2 >= 2.10',
-	'natsort >= 6.0.0',
-	'pyyaml >= 5.1',
-	'rarfile >= 3.0'
-]
-
-setup(
-	name = 'tuack',
-	version = '0.1.4.9.2',
-	packages = find_packages(),
-	author = 'Chen Xumin, Zhang Ruizhe, Liu Xiaoyi, Chen Junkun',
-	author_email = 'chen.xm.mu@gmail.com, 657228726@qq.com, circuitcoder0@gmail.com, 1261954105@qq.com',
-	url = '',
-	license = 'https://git.thusaac.com/publish/tuack/blob/master/LICENSE',
-	description = 'Tools for generating an Tsinghua/OI/ICPC-styled problem or contest for multiple judges.',
-	cmdclass={
-		'develop': PostDevelopCommand,
-		'install': PostInstallCommand,
-	},
-	#requires = requires,
-	install_requires = requires,
-	setup_requires = requires,
-	package_data = {
-		'tuack': [
-			'templates/*.*', 'templates/*/*/*',
-			'sample/*.*', 'sample/*/*',
-			'sample-problem/*.*', 'sample-problem/*/*',
-			'sample-empty/*.*', 'sample-empty/*/*',
-			'lex/*.*', 'lex/*'
-		]
-	}
-)
-
+from setuptools import setup, find_packages
+from setuptools.command.develop import develop
+from setuptools.command.install import install
+from subprocess import check_call
+import platform
+
+def check():
+	system = platform.system()
+	if system == 'Linux':
+		check_call("sudo apt-get install pandoc git git-lfs".split())
+		check_call("git lfs install".split())
+	elif system == 'Darwin':
+		check_call("brew update".split())
+		check_call("brew install pandoc".split())
+		check_call("brew install git".split())
+		check_call("brew install git-lfs".split())
+		check_call("git lfs install".split())
+
+class PostDevelopCommand(develop):
+	"""Post-installation for development mode."""
+	def run(self):
+		#check()
+		develop.run(self)
+
+class PostInstallCommand(install):
+	"""Post-installation for installation mode."""
+	def run(self):
+		#check()
+		install.run(self)
+
+requires = [
+	'jinja2 >= 3.0',
+	'natsort >= 6.0.0',
+	'pyyaml >= 5.1',
+	'rarfile >= 3.0',
+	'requests_toolbelt >= 0.9.1'
+]
+
+setup(
+	name = 'tuack',
+	version = '0.1.5',
+	packages = find_packages(),
+	author = 'Chenxu Min, Zhang Ruizhe, Liu Xiaoyi, Chen Junkun, Chen Shengqi, Luo Lingxiao, Cheng Yuxuan',
+	author_email = 'chen.xm.mu@gmail.com, 657228726@qq.com, circuitcoder0@gmail.com, 1261954105@qq.com, i@harrychen.xyz, 0.0@pku.edu.cn',
+	url = '',
+	license = 'https://git.thusaac.com/publish/tuack/blob/master/LICENSE',
+	description = 'Tools for generating an Tsinghua/OI/ICPC-styled problem or contest for multiple judges.',
+	cmdclass={
+		'develop': PostDevelopCommand,
+		'install': PostInstallCommand,
+	},
+	#requires = requires,
+	install_requires = requires,
+	setup_requires = requires,
+	package_data = {
+		'tuack': [
+			'templates/*.*', 'templates/*/*/*',
+			'sample/*.*', 'sample/*/*',
+			'sample-problem/*.*', 'sample-problem/*/*',
+			'sample-empty/*.*', 'sample-empty/*/*',
+			'lex/*.*', 'lex/*'
+		]
+	}
+)
+
```

### Comparing `tuack-0.1.4.9.2/tuack/base.py` & `tuack-0.1.5/tuack/base.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,962 +1,1006 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-import platform
-import logging
-import traceback
-import yaml
-
-python_version = sys.version_info.major
-if python_version == 2:
-	reload(sys)
-	sys.setdefaultencoding('utf-8')
-
-class Memory(str):
-	'''
-	'5KB'，'10 MB'，'8M'格式的字符串s，允许用Memory(s).GB，Memory(s).B等形式转换单位
-	'''
-	units = {
-		'B' : 1,
-		'K' : 2 ** 10,
-		'KB' : 2 ** 10,
-		'Ki' : 2 ** 10,
-		'KiB' : 2 ** 10,
-		'M' : 2 ** 20,
-		'MB' : 2 ** 20,
-		'Mi' : 2 ** 20,
-		'MiB' : 2 ** 20,
-		'G' : 2 ** 30,
-		'GB' : 2 ** 30,
-		'Gi' : 2 ** 30,
-		'GiB' : 2 ** 30,
-		'T' : 2 ** 40,
-		'TB' : 2 ** 40,
-		'Ti' : 2 ** 40,
-		'TiB' : 2 ** 40,
-		'P' : 2 ** 50,
-		'PB' : 2 ** 50,
-		'Pi' : 2 ** 50,
-		'PiB' : 2 ** 50
-	}
-	def __new__(self, val):
-		return super(Memory, self).__new__(self, val)
-	def byte(self):
-		if self[-1] == 'B':
-			sp = 2 if self[-2] in self.units else 3 if self[-3:-1] in self.units else 1
-		else:
-			sp = 1
-		un = self.units[self[-sp:]]
-		return float(self[:-sp]) * un
-	def __init__(self, val):
-		super(Memory, self).__init__()
-		b = self.byte()
-		for key, val in self.units.items():
-			self.__setattr__(key, b / val)
-
-json_version = 2
-work = None
-system = platform.system()
-out_system = system
-windows_stack_size = 536870912
-diff_tool = 'diff' if system != 'Windows' else 'fc'
-time_multiplier = 3.
-elf_suffix = '' if system != 'Windows' else '.exe'
-problem_skip = re.compile(r'^(data|down|tables|resources|gen|pre)$')
-user_skip = re.compile(r'^(data|down|pre|val|.*validate.*|gen|chk|checker|report|check.*|make_data|data_maker|data_make|make|dmk|generate|generator|makedata|spj|judge|tables|tmp|.*\.tmp|.*\.temp|temp|.*\.test|.*\.dir)(\..*)?$')
-compilers = {
-	'cpp' : lambda name, args, macros = '', ml = Memory('512 MB'): 'g++ %s.cpp -o %s %s %s %s' % (name, name, args, macros, '' if system != 'Windows' else '-Wl,--stack=%d' % int(ml.B)),
-	'c' : lambda name, args, macros = '', ml = Memory('512 MB'): 'gcc %s.c -o %s %s %s %s' % (name, name, args, macros, '' if system != 'Windows' else '-Wl,--stack=%d' % int(ml.B)),
-	# I don't know how to change stack size, nor add #define in pascal
-	'pas' : lambda name, args, macros = '', ml = Memory('512 MB'): 'fpc %s.pas %s' % (name, args),
-	'java' : lambda name, args, macros = '', ml = Memory('512 MB'): 'javac %s.java %s -J-Xms%dm -J-Xmx%dm' % (name, args, int(Memory(ml).MB) // 16, int(Memory(ml).MB) // 4),
-	'py' : lambda name, args, macros = '', ml = Memory('512 MB'): ''
-}
-runners = {
-	'cpp' : None,
-	'c' : None,
-	'pas' : None,
-	'java' : lambda name, ml = None: 'java -Xms%dm -Xmx%dm %s' % (int(Memory(ml).MB) // 16, int(Memory(ml).MB), name),
-	'py' : lambda name, ml = None: 'python %s.py' % name
-}
-macros = {
-	'uoj' : '-DONLINE_JUDGE',
-	'noi' : '-D__ARBITER__',
-	'release' : '',
-	'test' : '-D__TUACK__ -DONLINE_JUDGE'
-}
-
-copied_data = set()
-no_compiling = False
-path = os.path.dirname(os.path.realpath(__file__))
-
-log = logging.getLogger()
-log.setLevel(logging.DEBUG)
-
-class NoFileException(Exception):
-	pass
-
-pjoin = lambda *args : os.path.join(*args).rstrip('/').rstrip('\\')
-rjoin = lambda *args : '/'.join(args).strip('/')
-
-natsort_warned = None
-
-try:
-	tool_path = (path if system == 'Windows' and not os.path.expanduser("~") else pjoin(os.path.expanduser("~"), '.tuack'))
-except:
-	tool_path = path
-if not os.path.exists(tool_path):
-	os.makedirs(tool_path)
-
-if system == 'Windows':
-	format_checker_name = 'format-win.exe'
-elif system == 'Darwin':
-	format_checker_name = 'format-mac'
-else:
-	format_checker_name = 'format-linux'
-
-class Configure(dict):
-	'''
-	描述一个conf.json的对象
-	'''
-	@staticmethod
-	def merge_item(base, ext):
-		'''
-		用于合并继承和原始的dict元素
-		'''
-		if type(base) == type(ext) == list:
-			return base + ext
-		elif type(base) != dict or type(ext) != dict:
-			log.error('Extend conf.json error, type of key `%s` doesn\'t match.' % key)
-			raise TypeError('extend error %s' % key)
-		ret = base.copy()
-		for key, val in ext.items():
-			if key.endswith('+'):
-				k = key[:-1]
-				ret[k] = merge_item(base[k], val)
-			else:
-				ret[key] = val
-		return ret
-
-	def __init__(self, val, path = None, parent = None):
-		if type(val) == dict:
-			super(Configure, self).__init__(val)
-		elif type(val) == str:
-			super(Configure, self).__init__(json.loads(val))
-		elif type(val) == bytes:
-			super(Configure, self).__init__(json.loads(val.decode('utf-8')))
-		else:
-			raise Exception('Can\'t translate this object to a Configure.')
-		self.folder = self['folder']
-		self.parent = parent
-		self.language = None
-		self.path = path
-		self.sub = []
-
-	def lang(self):
-		return self.language
-
-	def tr(self, key):
-		val = self[key]
-		if type(val) != dict:
-			return val
-		if lang and lang in val:
-			return val[lang]
-		if self.lang() and self.lang() in val:
-			return val[self.lang()]
-		for k, v in val.items():
-			return v
-		return None
-
-	def __contains__(self, key):
-		return super(Configure, self).__contains__(key + '+') or super(Configure, self).__contains__(key) or (self.parent and key in self.parent)
-
-	def getitem(self, key, trans = lambda prob, val, key, depth : val, depth = 0):
-		if super(Configure, self).__contains__(key + '+'):
-			cur = trans(self, super(Configure, self).__getitem__(key + '+'), key, depth)
-			return self.merge_item(cur, self.parent.getitem(key, trans, depth + 1)) if self.parent else cur
-		if super(Configure, self).__contains__(key):
-			return trans(self, super(Configure, self).__getitem__(key), key, depth)
-		return self.parent.getitem(key, trans, depth + 1) if self.parent else None
-
-	def __getitem__(self, key):
-		return self.getitem(key)
-
-	def set_default(self, path = None):
-		self.all = True
-		if 'name' not in self:
-			self['name'] = path
-		return self
-
-	def probs(self, pick = False, no_repeat = False):
-		if no_repeat == True:
-			no_repeat = set()
-		if no_repeat != False:
-			path = os.path.abspath(self.path)
-			if path in no_repeat:
-				return
-			no_repeat.add(path)
-		pick |= not sub_set or self.route in sub_set
-		if type(self) == Problem:
-			if pick or any_prefix(self.route):
-				self.all = pick
-				yield self
-		else:
-			for sub in self.sub:
-				for prob in sub.probs(pick, no_repeat = no_repeat):
-					yield prob
-
-	def days(self, pick = False, no_repeat = False):
-		if no_repeat == True:
-			no_repeat = set()
-		if no_repeat != False:
-			path = os.path.abspath(self.path)
-			if path in no_repeat:
-				return
-			no_repeat.add(path)
-		pick |= not sub_set or self.route in sub_set
-		if type(self) == Problem:
-			return
-		if type(self) == Day:
-			if pick or any_prefix(self.route):
-				self.all = pick
-				yield self
-		else:
-			for sub in self.sub:
-				for day in sub.days(pick, no_repeat = no_repeat):
-					yield day
-
-	def name_lang(self):
-		return self['name'] + ('-' + globals()['lang'] if globals()['lang'] else '')
-
-def probs(item = None, pick = False, no_repeat = False):
-	if not item:
-		item = conf
-	return conf.probs(pick, no_repeat)
-
-def days(item = None, pick = False, no_repeat = False):
-	if not item:
-		item = conf
-	return conf.days(pick, no_repeat)
-
-class Contest(Configure):
-	def __init__(self, *args):
-		super(Contest, self).__init__(*args)
-
-class Day(Configure):
-	def __init__(self, *args):
-		super(Day, self).__init__(*args)
-
-class DataPath(str):
-	def __new__(self, val):
-		return super(DataPath, self).__new__(self, '*' * val['depth'] + val['case'])
-	def __init__(self, val):
-		self.data = val
-		super(DataPath, self).__init__()
-	def __getitem__(self, key):
-		return self.data[key]
-	def full(self):
-		return pjoin(self['prefix'], self['key'], self['case'])
-
-def sorter():
-	global natsort_warned
-	try:
-		if not natsort_warned:
-			check_install('natsort')
-		import natsort
-		return lambda inp : natsort.natsorted(inp, alg = natsort.ns.IGNORECASE)
-	except:
-		if not natsort_warned:
-			log.warning(u'`natsort`用于给测试点名称排序，不使用的话可能会出现10排在2前面的情况。')
-			natsort_warned = True
-		return sorted
-
-class Datum(dict):
-	def __init__(self, datum, prob = None, key = 'data'):
-		super(Datum, self).__init__(datum)
-		self.prob = prob
-		self.key = key
-	def ml(self):
-		return Memory(self['memory limit']) if 'memory limit' in self else self.prob.ml()
-
-class Problem(Configure):
-	def statement(self, cur_lang = None):
-		if not cur_lang and lang:
-			cur_lang = lang
-		if cur_lang:
-			source = pjoin(self.path, 'statement', cur_lang + '.md')
-			if os.path.exists(source):
-				self.language = cur_lang
-				return source
-		for source, self.language in (
-			(pjoin(self.path, 'statement', 'zh-cn.md'), 'zh-cn'),
-			(pjoin(self.path, 'statement', 'en.md'), 'en'),
-			(pjoin(self.path, 'description.md'), None)
-		):
-			if os.path.exists(source):
-				return source
-		raise NoFileException('No md file found.')
-	def lang(self):
-		try:
-			self.statement()
-			return self.language
-		except NoFileException as e:
-			return None
-	def __init__(self, *args):
-		super(Problem, self).__init__(*args)
-		self.chk = None
-		self.data = self.get_data('data')
-		self.samples = self.get_data('samples')
-		self.pre = self.get_data('pre')
-	def set_default(self, path = None):
-		super(Problem, self).set_default(path)
-		if 'title' not in self and 'cnname' in self:
-			self['title'] = {'zh-cn' : self.pop('cnname')}
-		for data, cases, attr, key in [('data', 'test cases', 'test_cases', 'data'), ('samples', 'sample count', 'sample_cases', 'down'), ('pre', 'pre count', 'pre_cases', 'pre')]:
-			tc = set()
-			if hasattr(self, data) and self.__getattribute__(data) != None:
-				for datum in self.__getattribute__(data):
-					tc |= set(datum['cases'])
-			else:
-				self[data] = []
-			if cases in self and type(self[cases]) == int:
-				log.warning(u'`%s`字段不再使用，使用`python -m tuack.gen upgrade`升级。' % cases)
-				#to_dp = lambda i : DataPath({'case' : self['name'] + str(i), 'key' : key, 'depth' : 0, 'prefix' : self.path})
-				#self[data] = [{'cases' : [
-				#	to_dp(i) for i in range(1, self.pop(cases) + 1) \
-				#	if to_dp(i) not in tc
-				#]}]
-			self.__setattr__(attr, sorter()(list(tc)))
-	def set_score(self):
-		if 'packed' in self:
-			log.warning(u'题目`%s`的`packed`字段不再有效，但仍可以存在，用`python -m tuack.gen upgrade`升级。' % self.route)
-		num_unscored = 0
-		total_score = 0.0
-		if not self.data:
-			self.packed = False
-			return
-		for datum in self.data:
-			if 'score' in datum:
-				datum.score = datum['score']
-				total_score += datum['score']
-			else:
-				num_unscored += 1
-		if num_unscored != 0:
-			item_score = (100. - total_score) / num_unscored
-			for datum in self.data:
-				if 'score' not in datum:
-					datum.score = item_score
-		if num_unscored == len(self.data):
-			self.packed = False
-			self.score = 100.
-		else:
-			self.packed = True
-			if num_unscored != 0:
-				log.warning(u'题目`%s`有%d个包设置了`score`，有%d个没有；总分共设%f分，将剩下%f分平分给没有的包。' % (
-					self.route,
-					len(self.data) - num_unscored,
-					num_unscored,
-					total_score,
-					100 - total_score
-				))
-				log.info(u'如果你需要不等分+打包测试，请每个包设置`score`；否则请每个包都不设置`score`，此时是每个测试点同分而不是每个包同分。')
-				log.info(u'一部分包设置`score`，另一部分不设置将可能导致导出其他格式时出现问题。')
-				self.score = 100.0
-			else:
-				if abs(total_score - 100) > 1e-6:
-					log.warning(u'题目`%s`总分是%f分，不是100分。' % (self.route, total_score))
-				self.score = total_score
-
-	def extend_pathed(self, path):
-		if path.startswith(':'):
-			return self.parent.extend_pathed(path[1:])
-		return pjoin(self.path, path)
-
-	def users(self):
-		def users_pathed(self, users, key = '', depth = 0):
-			if type(users) != dict:
-				log.warning(u'`json.conf`中，`users`项%s:%s已经过时，但仍可以使用，用`python -m tuack.gen upgrade`升级' % (key, users))
-				return {
-					'path' : self.extend_pathed(users),
-					'expected' : {}
-				}
-			elif depth == 2:
-				# Is detailed description
-				if "path" not in users:
-					# Ill-formed
-					log.warning(u'`users`项%s:%s不含`path`项' % (key, users))
-					return None
-				return {
-					'path' : self.extend_pathed(users["path"]),
-					'expected' : users["expected"] if "expected" in users else {}
-				}
-
-			return {
-				key : val
-				for key, val in \
-				((key, users_pathed(self, val, key, depth + 1)) for key, val in users.items()) \
-				if val
-			}
-		return self.getitem('users', users_pathed)
-	
-	def expect(self, user, algo, score):
-		'''
-		Check expected scores
-		'''
-		exp = self.users()[user][algo]['expected']
-		algo_failed = False
-		if type(exp) == dict:
-			for symbol, value in exp.items():
-				algo_failed |= not eval('score %s %s' % (symbol, value))
-		elif type(exp) == list:
-			for pred in exp:
-				algo_failed |= not eval('score %s' % pred)
-		elif type(exp) == str:
-			algo_failed |= not eval('score %s' % exp)
-		elif exp is None:
-			pass
-		else:
-			log.warning('`expected`字段必须是字符串、数组或字典。')
-		return not algo_failed
-
-	def get_data(self, key):
-		def data_pathed(self, data, key, depth):
-			key_map = {
-				'data' : 'data',
-				'samples' : 'down',
-				'pre' : 'pre'
-			}
-			ret = []
-			for datum in data:
-				tmp = []
-				for case in datum['cases']:
-					cur = self
-					dep = depth
-					cas = str(case)
-					while cas.startswith(':'):
-						cas = cas[1:]
-						dep -= 1
-						cur = cur.parent
-					tmp.append(DataPath({'case' : cas, 'key' : key_map[key], 'depth' : dep, 'prefix' : cur.path}))
-				datum_fixed = datum.copy()
-				datum_fixed['cases'] = tmp
-				ret.append(Datum(datum_fixed, self, key))
-			return ret
-		return self.getitem(key, data_pathed)
-
-	def ml(self):
-		return Memory(self.get('memory limit', '2 GB'))
-
-	def memory_limit(self):
-		return self.ml()
-
-#mem_json = {}	# 题目复用的话，需要记忆化
-
-def load_json(path = '.', route = None):
-	#abs_path = os.path.abspath(path)
-	#if abs_path in mem_json:
-	#	return mem_json[abs_path]
-	for name in ['conf.yaml', 'conf.json', 'prob.json']:
-		try:
-			full_path = pjoin(path, name)
-			if os.path.isfile(full_path):
-				inp = open(full_path, 'rb').read().decode('utf-8')
-				if name.endswith('json'):
-					conf = json.loads(inp)
-				elif name.endswith('yaml'):
-					conf = yaml.full_load(inp)
-				if conf.get('version', -1) > json_version:
-					log.warning(u'`conf.*`版本高于`tuack`，请升级`tuack`。')
-				if 'folder' not in conf:
-					conf['folder'] = 'problem'
-				args = [conf, path]
-				if conf['folder'] == 'extend':
-					base_conf = load_json(pjoin(path, conf['base path']))
-					folder = base_conf.folder
-					args.append(base_conf)
-				else:
-					folder = conf['folder']
-				conf = eval(folder.capitalize())(*args)
-				if conf['folder'] == 'extend':
-					conf.folder = base_conf.folder
-				conf.set_default(os.path.basename(path))
-				conf.route = '' if route == None else rjoin(route, conf['name'])
-				if conf.folder == 'problem':
-					conf.set_score()
-				if 'subdir' in conf:
-					conf.sub = [
-						load_json(pjoin(path, sub), conf.route) \
-						for sub in conf['subdir']
-					]
-				#mem_json[abs_path] = conf
-				return conf
-		except Exception as e:
-			log.error(u'文件`%s`错误或子目录下文件错误。' % pjoin(path, name))
-			log.info(e)
-			raise e
-	else:
-		raise NoFileException(u'路径`%s`下找不到conf.*。' % path)
-
-def del_redundance(conf, red):
-	for key in red:
-		try:
-			conf.pop(key)
-		except:
-			pass
-	if not conf['name'] or conf['name'] == '.':
-		conf.pop('name')
-	return conf
-
-dump_formats = {
-	'json' : lambda conf : json.dumps(conf, indent = 2, sort_keys = True, ensure_ascii = False).encode('utf-8'),
-	'yaml' : lambda conf : yaml.safe_dump(dict(conf), encoding = 'utf-8', allow_unicode = True)
-}
-
-def save_json(conf):
-	for s in conf.sub:
-		save_json(s)
-	try:
-		open(pjoin(conf.path, 'conf.' + dump_format), 'wb').write(dump_formats[dump_format](conf))
-	except Exception as e:
-		log.error(u'不支持配置文件格式`%s`。' % dump_format)
-		log.info(e)
-
-def any_prefix(pre, st = None):
-	if not st:
-		st = sub_set
-	for s in st:
-		if s == pre:
-			return 1
-		if pre == '' or s.startswith(pre + '/'):
-			return 2
-	return 0
-
-def mkdir(name):
-	if not os.path.exists(name):
-		os.makedirs(name)
-
-def remkdir(name):
-	while True:
-		try:
-			shutil.rmtree(name, ignore_errors = True)
-			time.sleep(0.1)
-			if not os.path.exists(name):
-				os.makedirs(name)
-			break
-		except Exception as e:
-			log.warning('Can\'t delete %s' % name)
-			log.warning(e)
-
-def copy(source, name, target):
-	full_source = pjoin(source, name)
-	if not os.path.exists(full_source):
-		raise NoFileException('No such file or path `%s`.' % full_source)
-	copied_data.add(full_source)
-	if os.path.isdir(full_source):
-		if full_source.endswith('.dir') or no_compiling:
-			full_target = (pjoin(target, name) if os.path.exists(target) else target)
-			if full_source.endswith('.dir'):
-				full_target = full_target[:-4]
-			shutil.copytree(full_source, full_target)
-		else:
-			# TODO: make if there is a makefile
-			ret = os.getcwd()
-			os.chdir(pjoin(source, name))
-			cpp_file = name + '.cpp'
-			elf_file = name + elf_suffix
-			check_install('g++')
-			if os.system('g++ %s -o %s -O2 -std=c++14 -Wall' % (cpp_file, elf_file)) != 0:
-				os.chdir(ret)
-				log.error(u'`%s`编译失败。' % pjoin(full_source, cpp_file))
-				return True
-			else:
-				os.chdir(ret)
-				log.info(u'`%s`编译成功。' % pjoin(full_source, cpp_file))
-			shutil.move(pjoin(full_source, elf_file), target)
-	else:
-		shutil.copy(full_source, target)
-	return True
-
-def xopen_file(path):
-	try:
-		if system == 'Windows':
-			os.startfile(path)
-		elif system == 'Darwin':
-			subprocess.call(["open", path])
-		else:
-			subprocess.call(["xdg-open", path])
-	except Exception as e:
-		log.warning(u'打开文件`%s`失败。' % path)
-		log.info(e)
-
-def deal_args():
-	global do_copy_files, do_test_progs, do_release, works, start_file, do_pack, langs, lang, sub_set, out_system, args, do_zip, do_encript, do_render, time_multiplier, git_lfs, dump_format, user_time, water_mark
-	do_render = True
-	works = []
-	args = []
-	langs = [None]
-	lang = None
-	sub_set = None
-	start_file = True
-	do_pack = True
-	do_zip = False
-	do_encript = False
-	git_lfs = False
-	user_time = False
-	dump_format = 'yaml'
-	water_mark = False
-	l = len(sys.argv)
-	i = 1
-	while i < l:
-		if sys.argv[i] == '-i':
-			i += 1
-			os.chdir(sys.argv[i])
-		elif sys.argv[i] == '-p':
-			i += 1
-			sub_set = set(sys.argv[i].split(','))
-		elif sys.argv[i] == '-o':
-			i += 1
-			out_system = sys.argv[i]
-		elif sys.argv[i] == '-d':
-			i += 1
-			dump_format = sys.argv[i]
-		elif sys.argv[i] == '-s':
-			start_file = False
-		elif sys.argv[i] == '-k':
-			do_pack = False
-		elif sys.argv[i] == '-z':
-			do_zip = True
-		elif sys.argv[i] == '-g':
-			git_lfs = True
-		elif sys.argv[i] == '-r':
-			do_render = False
-		elif sys.argv[i] == '-e':
-			do_zip = True
-			do_encript = True
-		elif sys.argv[i] == '-u':
-			user_time = True
-		elif sys.argv[i] == '-l':
-			i += 1
-			langs = set(sys.argv[i].split(','))
-		elif sys.argv[i] == '-t':
-			i += 1
-			time_multiplier = float(sys.argv[i])
-		elif sys.argv[i] == '-w':
-			i += 1
-			water_mark = sys.argv[i]
-		elif sys.argv[i] == '-h' or sys.argv[i] == '--help':
-			log.info(u'详细用法见文档：https://git.thusaac.com/publish/tuack/wikis。')
-			log.info(u'python 脚本 [[[工作1],工作2],...] [[[选项1] 选项2] ...] [[[参数1] 参数2] ...]')
-			log.info(u'工作必须在参数前面，工作用逗号隔开，选项和参数用空格隔开。')
-			log.info(u'只有有逗号的项目可以用逗号获得多个结果，逗号前后不能有空白符。')
-			log.info(u'这套工具的大多数脚本都可以在比赛、比赛日和题目目录下运行。')
-			log.info(u'选项：')
-			log.info(u'  -i PATH             指定PATH作为工作路径，否则使用当前路径。')
-			log.info(u'  -s                  对于有输出的文件的操作，输出完以后不自动打开文件。')
-			log.info(u'  -p day0/sleep,day2  只对day0/sleep和day2进行本次操作；此路径是基于当前文件夹的，')
-			log.info(u'                      例如：在比赛日目录如day1下，则可以直接指定题目如exam；')
-			log.info(u'                      对于test，还可以指定用户或算法，如day1/problem/vfk/std.cpp。')
-			log.info(u'  -t 6.0              对于test，设置掐断时间为6.0*时间限制，用于对比不同程序的时限。')
-			log.info(u'  -o SYSTEM           对于ren，输出指定操作系统的题面，可选Windows和Linux。')
-			log.info(u'  -l zh-cn,en         对于ren，指定输出语言，不指定默认为zh-cn。')
-			log.info(u'  -w logo.png         对于ren，给PDF添加水印，默认不添加。')
-			log.info(u'  -r                  对于dump，不先尝试渲染题面。')
-			log.info(u'  -g                  对于gen，使用git-lfs。')
-			log.info(u'  -d json             对于gen，规定配置文件格式，支持json、yaml，默认yaml。')
-			log.info(u'  -u                  对于test，在linux下使用user time做测试，默认real time。')
-			
-			return False
-		else:
-			if len(works) == 0:
-				works = sys.argv[i].split(',')
-			else:
-				args += sys.argv[i].split(',')
-		i += 1
-	return True
-
-def custom_conf():
-	get_tool_conf()
-	c = env_conf['file_log'] if 'file_log' in env_conf else {}
-	file_log = logging.FileHandler(
-		c['path'] if 'path' in c else 'tuack.log',
-		mode = c['mode'] if 'mode' in c else 'a',
-		encoding = c['encoding'] if 'encoding' in c else None
-	)
-	file_log.setLevel(c['level'] if 'level' in c else logging.INFO)
-	file_log.setFormatter(logging.Formatter(
-		c['format'] if 'format' in c else '[%(levelname).1s]%(filename)s:%(funcName)s:%(lineno)d:%(message)s'
-	))
-	log.addHandler(file_log)
-
-	c = env_conf['bash_log'] if 'bash_log' in env_conf else {}
-	if 'encoding' in c:
-		class MyStream(object):
-			def __init__(self, stream):
-				self.stream = stream
-			def write(self, s):
-				self.stream.buffer.write(s.encode(c['encoding']))
-				self.stream.flush()
-			def flush(self):
-				self.stream.flush()
-		bash_log = logging.StreamHandler(MyStream(sys.stdout))
-	else:
-		bash_log = logging.StreamHandler()
-	bash_log.setLevel(c['level'] if 'level' in c else logging.DEBUG)
-	bash_log.setFormatter(logging.Formatter(
-		c['format'] if 'format' in c else '[%(levelname).1s]%(message)s'
-	))
-	log.addHandler(bash_log)
-
-def init():
-	import __main__
-	global conf
-	custom_conf()
-	if not deal_args():
-		return False
-	log.info(
-		('脚本%s，工程路径%s，参数%s，开始于%s。' if python_version == 2 else u'脚本%s，工程路径%s，参数%s，开始于%s。') % (
-			__main__.__file__, os.getcwd(), str(sys.argv[1:]), str(datetime.datetime.now())
-		)
-	)
-	conf = load_json()
-	try:
-		check_install('git')
-		check_install('git_lfs')
-	except:
-		pass
-	return True
-
-def tr(item):
-	if 'zh-cn' in item:
-		return item['zh-cn']
-	elif 'en' in item:
-		return item['en']
-	elif len(item) > 1:
-		for val in item.values():
-			return val
-	else:
-		return 'Unknown'
-
-def run_r(cmd, path):
-	for f in os.listdir(path):
-		cpath = pjoin(path, f)
-		if os.path.isfile(cpath):
-			cmd(cpath)
-		else:
-			run_r(cmd, cpath)
-
-def get_tool_conf():
-	def get_sys_env():
-		return '$'.join([
-			os.environ[key]
-			for key in ['OS', 'SESSIONNAME', 'USERNAME', 'COMPUTERNAME', 'USERDOMAIN', 'USER', 'SHELL', 'SESSION'] \
-			if key in os.environ
-		] + ['py%x' % sys.hexversion])
-	global env_conf
-	try:
-		tool_conf = json.loads(open(pjoin(tool_path, 'conf.json'), 'rb').read().decode('utf-8'))
-	except:
-		tool_conf = {}
-	sys_env = get_sys_env()
-	if sys_env not in tool_conf:
-		tool_conf[sys_env] = {}
-	env_conf = tool_conf[sys_env]
-	return tool_conf
-
-def check_install(pack):
-	def check_import(pack, extra_info = '', pack_name = None, level = logging.ERROR):
-		try:
-			__import__(pack)
-		except Exception as e:
-			log.log(level, u'python包%s没有安装，使用 pip install %s 安装。%s' % (pack, pack_name if pack_name else pack, extra_info))
-			if system == 'Windows':
-				log.info(u'如果pip没有安装，Windows下推荐用Anaconda等集成环境。')
-			if system == 'Linux':
-				log.info(u'如果pip没有安装，Ubuntu下用 sudo apt install python-pip 安装。')
-			raise e
-	check_pyside = lambda : check_import('PySide', u'注意这个包只能在 python2 下使用。', 'pyside')
-	check_jinja2 = lambda : check_import('jinja2')
-	check_natsort = lambda : check_import('natsort', level = logging.WARNING)
-	check_gettext = lambda : check_import('gettext')
-	def check_pandoc():
-		ret = os.system('pandoc -v')
-		if ret != 0:
-			log.error(u'格式转换工具pandoc没有安装。')
-			if system == 'Windows':
-				log.info(u'Windows用户去官方网站下载安装，安装好后把pandoc.exe所在路径添加到环境变量PATH中。')
-			if system == 'Linux':
-				log.info(u'Ubuntu下用 sudo apt install pandoc 安装。')
-			raise Exception('pandoc not found')
-	def check_xelatex():
-		ret = os.system('xelatex --version')
-		if ret != 0:
-			log.error(u'TeX渲染工具XeLaTeX没有安装。')
-			if system == 'Windows':
-				log.info(u'Windows下可以先安装MiKTeX，在首次运行的时候会再提示安装后续文件。')
-			if system == 'Linux':
-				log.info(u'Ubuntu下先用 sudo apt install texlive-xetex texlive-fonts-recommended texlive-latex-extra 安装工具；')
-				log.info(u'然后一般会因为缺少有些字体而报错（Windows有使用权，但Ubuntu没有，所以没有预装这些字体）。')
-				log.info(u'可以使用下列页面上的方法安装缺少的字体或是把win下的字体复制过来。')
-				log.info(u'http://linux-wiki.cn/wiki/zh-hans/LaTeX%E4%B8%AD%E6%96%87%E6%8E%92%E7%89%88%EF%BC%88%E4%BD%BF%E7%94%A8XeTeX%EF%BC%89')
-			raise Exception('xelatex not found')
-	def check_git():
-		ret = os.system('git --version')
-		if ret != 0:
-			log.warning(u'版本管理工具git没有安装，如果工程用git维护则你的修改可能无法成功提交。')
-			log.info(u'一个可能的安装教程见这里：')
-			log.info(u'https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git')
-			if system == 'Windows':
-				log.info(u'Windows下有多种不同的git版本，大家可以多交流好用的版本。')
-			log.info(u'git入门可以参看这里：')
-			log.info(u'http://rogerdudler.github.io/git-guide/index.zh.html')
-			log.info(u'一般推荐用ssh方式克隆仓库，并用公私钥保证安全，添加密钥的方式一般仓库的git网页上能找到。')
-			raise Exception('git not found')
-	def check_git_lfs():
-		ret = os.system('git lfs')
-		if ret != 0:
-			log.warning(u'git大文件系统lfs没有安装，如果工程使用了它你可能无法同步。')
-			log.info(u'因为有些评测数据比较大，所以一般要求用git lfs大文件系统（Large File System）管理评测数据（in/ans）')
-			log.info(u'一个可能的安装教程见这里：')
-			log.info(u'https://git-lfs.github.com/')
-			log.info(u'如果你用本工具的generator生成题目工程，那么你装好lfs以后一般可以不用再手工指定in和ans文件用lfs管理。')
-			log.info(u'如果你的多人合作工程用到了lfs，请务必不要在没有安装lfs前把数据添加到工程中！')
-			raise Exception('git lfs not found')
-
-	def check_gpp():
-		ret = os.system('g++ -v')
-		if ret != 0:
-			log.warning(u'g++未安装，将可能无法测试C++代码。')
-			raise Exception('g++ not found')
-	
-	def check_gcc():
-		ret = os.system('gcc -v')
-		if ret != 0:
-			log.warning(u'gcc未安装，将可能无法测试C代码。')
-			raise Exception('gcc not found')
-			
-	def check_java():
-		ret = os.system('javac -version')
-		if ret != 0:
-			log.warning(u'javac未安装，将可能无法测试Java代码。')
-			raise Exception('javac not found')
-		ret = os.system('java -version')
-		if ret != 0:
-			log.warning(u'java未安装，将可能无法测试Java代码。')
-			raise Exception('java not found')
-
-	def check_py2():
-		ret = os.system('python2 --version')
-		if ret != 0:
-			log.warning(u'python2未安装，将可能无法测试Python2代码。')
-			raise Exception('python2 not found')
-
-	def check_py3():
-		ret = os.system('python3 --version')
-		if ret != 0:
-			log.warning(u'python3未安装，将可能无法测试Python3代码。')
-			raise Exception('python3 not found')
-
-	def check_py():
-		ret = os.system('python --version')
-		if ret != 0:
-			log.warning(u'python未安装，将可能无法测试Python代码。')
-			raise Exception('python not found')
-			
-	def check_flex():
-		ret = os.system('flex --version')
-		if ret != 0:
-			log.warning(u'flex未安装，将可能无法检查题面格式。')
-			raise Exception('flex not found')
-
-	def check_bison():
-		ret = os.system('bison --version')
-		if ret != 0:
-			log.warning(u'bison未安装，将可能无法检查题面格式。')
-			raise Exception('bison not found')
-			
-	def check_format():
-		ret = os.system('%s -v' % pjoin(tool_path, format_checker_name))
-		if ret != 0:
-			log.warning(u'format checker未安装，使用`python -m tuack.install format`安装。')
-			raise Exception('format not found')
-			
-	def check_unrar():
-		ret = os.system('unrar --version')
-		if ret != 0:
-			log.warning(u'unrar未安装，将无法解压rar文件，请安装unrar。')
-			log.warning(u'对于Windows用户，你可以将WinRar的安装目录添加到PATH。')
-			raise Exception('unrar not found')
-
-	if pack in {'g++', 'cpp'}:
-		pack = 'gpp'
-	if pack == 'c':
-		pack = 'gcc'
-	global tool_conf
-	tool_conf = get_tool_conf()
-	if 'installed' not in env_conf:
-		env_conf['installed'] = {}
-	if pack in env_conf['installed'] and env_conf['installed'][pack]:
-		return True
-	eval('check_' + pack)()
-	env_conf['installed'][pack] = True
-
-	open(pjoin(tool_path, 'conf.json'), 'wb').write(json.dumps(tool_conf, indent = 2, sort_keys = True).encode('utf-8'))
-	return True
-
-def change_eol(path, eol):
-	import uuid
-	ufname = str(uuid.uuid4()) + '.tmp'
-	space_end = False
-	is_text = True
-	with open(ufname, 'wb') as f:
-		try:
-			for idx, line in enumerate(open(path, 'rb')):
-				line = line.rstrip(b'\r\n')
-				f.write(line + eol)
-				if not space_end and (line.endswith(b' ') or line.endswith(b'\t')):
-					log.warning(u'换行符转换：文件`%s`第%d行末尾有空白符。' % (path, idx + 1))
-					space_end = True
-				for code in ['utf-8', 'gbk']:
-					try:
-						if '\0' in line.decode(code):
-							raise Exception('`\\0` in line')
-						break
-					except:
-						pass
-				else:
-					is_text = False
-					log.info(u'换行符转换：文件`%s`不是文本文件。' % path)
-					break
-		except:
-			is_test = False
-	if is_text:
-		os.remove(path)
-		time.sleep(0.1)
-		os.rename(ufname, path)
-	else:
-		os.remove(ufname)
-
-unix2dos = lambda path : change_eol(path, b'\r\n')
-dos2unix = lambda path : change_eol(path, b'\n')
-
-wiki = lambda name : name
-
-def run_exc(func):
-	try:
-		return (True, func())
-	except Exception as e:
-		log.error(e)
-		log.info(traceback.format_exc())
-		return (False, None)
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+import platform
+import logging
+import traceback
+import yaml
+from inspect import isfunction
+
+python_version = (sys.version_info.major, sys.version_info.minor, sys.version_info.micro)
+if python_version[0] == 2:
+	reload(sys)
+	sys.setdefaultencoding('utf-8')
+
+class Memory(str):
+	'''
+	'5KB'，'10 MB'，'8M'格式的字符串s，允许用Memory(s).GB，Memory(s).B等形式转换单位
+	'''
+	units = {
+		'B' : 1,
+		'K' : 2 ** 10,
+		'KB' : 2 ** 10,
+		'Ki' : 2 ** 10,
+		'KiB' : 2 ** 10,
+		'M' : 2 ** 20,
+		'MB' : 2 ** 20,
+		'Mi' : 2 ** 20,
+		'MiB' : 2 ** 20,
+		'G' : 2 ** 30,
+		'GB' : 2 ** 30,
+		'Gi' : 2 ** 30,
+		'GiB' : 2 ** 30,
+		'T' : 2 ** 40,
+		'TB' : 2 ** 40,
+		'Ti' : 2 ** 40,
+		'TiB' : 2 ** 40,
+		'P' : 2 ** 50,
+		'PB' : 2 ** 50,
+		'Pi' : 2 ** 50,
+		'PiB' : 2 ** 50
+	}
+	def __new__(self, val):
+		return super(Memory, self).__new__(self, val)
+	def byte(self):
+		if self[-1] == 'B':
+			sp = 2 if self[-2] in self.units else 3 if self[-3:-1] in self.units else 1
+		else:
+			sp = 1
+		un = self.units[self[-sp:]]
+		return float(self[:-sp]) * un
+	def __init__(self, val):
+		super(Memory, self).__init__()
+		b = self.byte()
+		for key, val in self.units.items():
+			self.__setattr__(key, b / val)
+
+json_version = 2
+work = None
+system = platform.system()
+out_system = system
+def get_linux_version():
+	try:
+		return open('/etc/issue').read().split('')[0]
+	except:
+		return 'Unknown'
+if system == 'Linux':
+	linux_version = get_linux_version()
+windows_stack_size = 536870912
+diff_tool = 'diff' if system != 'Windows' else 'fc'
+time_multiplier = 3.
+elf_suffix = '' if system != 'Windows' else '.exe'
+problem_skip = re.compile(r'^(data|down|tables|resources|gen|pre)$')
+user_skip = re.compile(r'^(data|down|pre|val|.*validate.*|gen|chk|checker|report|check.*|make_data|data_maker|data_make|make|dmk|generate|generator|makedata|spj|judge|tables|tmp|.*\.tmp|.*\.temp|temp|.*\.test|.*\.dir)(\..*)?$')
+compilers = {
+	'cpp' : lambda name, args, macros = '', ml = Memory('512 MB'): 'g++ %s.cpp -o %s %s %s %s' % (name, name, args, macros, '' if system != 'Windows' else '-Wl,--stack=%d' % int(ml.B)),
+	'c' : lambda name, args, macros = '', ml = Memory('512 MB'): 'gcc %s.c -o %s %s %s %s' % (name, name, args, macros, '' if system != 'Windows' else '-Wl,--stack=%d' % int(ml.B)),
+	# I don't know how to change stack size, nor add #define in pascal
+	'pas' : lambda name, args, macros = '', ml = Memory('512 MB'): 'fpc %s.pas %s' % (name, args),
+	'java' : lambda name, args, macros = '', ml = Memory('512 MB'): 'javac %s.java %s -J-Xms%dm -J-Xmx%dm' % (name, args, int(Memory(ml).MB) // 16, int(Memory(ml).MB) // 4),
+	'py' : lambda name, args, macros = '', ml = Memory('512 MB'): ''
+}
+
+# 必须用函数，而不是lambda表达式才能并行
+def java_runner(name, ml = None):
+	return 'java -Xms%dm -Xmx%dm %s' % (int(Memory(ml).MB) // 16, int(Memory(ml).MB), name)
+
+def py_runner(name, ml = None):
+	return 'python3 %s.py' % name
+
+runners = {
+	'cpp' : None,
+	'c' : None,
+	'pas' : None,
+	'java' : java_runner,
+	'py' : py_runner
+}
+macros = {
+	'uoj' : '-DONLINE_JUDGE',
+	'noi' : '-D__ARBITER__',
+	'release' : '',
+	'test' : '-D__TUACK__ -DONLINE_JUDGE'
+}
+
+copied_data = set()
+no_compiling = False
+path = os.path.dirname(os.path.realpath(__file__))
+
+log = logging.getLogger()
+log.setLevel(logging.DEBUG)
+
+class NoFileException(Exception):
+	pass
+
+pjoin = lambda *args : os.path.join(*args).rstrip('/').rstrip('\\')
+rjoin = lambda *args : '/'.join(args).strip('/')
+
+natsort_warned = None
+
+try:
+	tool_path = (path if system == 'Windows' and not os.path.expanduser("~") else pjoin(os.path.expanduser("~"), '.tuack'))
+except:
+	tool_path = path
+if not os.path.exists(tool_path):
+	os.makedirs(tool_path)
+
+if system == 'Windows':
+	format_checker_name = 'format-win.exe'
+elif system == 'Darwin':
+	format_checker_name = 'format-mac'
+else:
+	format_checker_name = 'format-linux'
+
+class Configure(dict):
+	'''
+	描述一个conf.json的对象
+	'''
+	@staticmethod
+	def merge_item(base, ext):
+		'''
+		用于合并继承和原始的dict元素
+		'''
+		if type(base) == type(ext) == list:
+			return base + ext
+		elif type(base) != dict or type(ext) != dict:
+			log.error('Extend conf.json error, type of key `%s` doesn\'t match.' % key)
+			raise TypeError('extend error %s' % key)
+		ret = base.copy()
+		for key, val in ext.items():
+			if key.endswith('+'):
+				k = key[:-1]
+				ret[k] = merge_item(base[k], val)
+			else:
+				ret[key] = val
+		return ret
+
+	def __init__(self, val, path = None, parent = None):
+		if type(val) == dict:
+			super(Configure, self).__init__(val)
+		elif type(val) == str:
+			super(Configure, self).__init__(json.loads(val))
+		elif type(val) == bytes:
+			super(Configure, self).__init__(json.loads(val.decode('utf-8')))
+		else:
+			raise Exception('Can\'t translate this object to a Configure.')
+		self.folder = self['folder']
+		self.parent = parent
+		self.language = None
+		self.path = path
+		self.sub = []
+
+	def lang(self):
+		return self.language
+
+	def tr(self, key):
+		val = self[key]
+		if type(val) != dict:
+			return val
+		if lang and lang in val:
+			return val[lang]
+		if self.lang() and self.lang() in val:
+			return val[self.lang()]
+		for k, v in val.items():
+			return v
+		return None
+
+	def __contains__(self, key):
+		return super(Configure, self).__contains__(key + '+') or super(Configure, self).__contains__(key) or (self.parent and key in self.parent)
+
+	def getitem(self, key, trans = lambda prob, val, key, depth : val, depth = 0):
+		if super(Configure, self).__contains__(key + '+'):
+			cur = trans(self, super(Configure, self).__getitem__(key + '+'), key, depth)
+			return self.merge_item(cur, self.parent.getitem(key, trans, depth + 1)) if self.parent else cur
+		if super(Configure, self).__contains__(key):
+			return trans(self, super(Configure, self).__getitem__(key), key, depth)
+		return self.parent.getitem(key, trans, depth + 1) if self.parent else None
+
+	def __getitem__(self, key):
+		return self.getitem(key)
+
+	def set_default(self, path = None):
+		self.all = True
+		if 'name' not in self:
+			self['name'] = path
+		return self
+
+	def probs(self, pick = False, no_repeat = False):
+		if no_repeat == True:
+			no_repeat = set()
+		if no_repeat != False:
+			path = os.path.abspath(self.path)
+			if path in no_repeat:
+				return
+			no_repeat.add(path)
+		pick |= not sub_set or self.route in sub_set
+		if type(self) == Problem:
+			if pick or any_prefix(self.route):
+				self.all = pick
+				yield self
+		else:
+			for sub in self.sub:
+				for prob in sub.probs(pick, no_repeat = no_repeat):
+					yield prob
+
+	def days(self, pick = False, no_repeat = False):
+		if no_repeat == True:
+			no_repeat = set()
+		if no_repeat != False:
+			path = os.path.abspath(self.path)
+			if path in no_repeat:
+				return
+			no_repeat.add(path)
+		pick |= not sub_set or self.route in sub_set
+		if type(self) == Problem:
+			return
+		if type(self) == Day:
+			if pick or any_prefix(self.route):
+				self.all = pick
+				yield self
+		elif type(self) == Contest:
+			for sub in self.sub:
+				if type(sub) == Day:
+					for day in sub.days(pick, no_repeat = no_repeat):
+						yield day
+
+	def name_lang(self):
+		return self['name'] + ('-' + globals()['lang'] if globals()['lang'] else '')
+
+def probs(item = None, pick = False, no_repeat = False):
+	if not item:
+		item = conf
+	return conf.probs(pick, no_repeat)
+
+def days(item = None, pick = False, no_repeat = False):
+	if not item:
+		item = conf
+	return conf.days(pick, no_repeat)
+
+class Contest(Configure):
+	def __init__(self, *args):
+		super(Contest, self).__init__(*args)
+
+class Day(Configure):
+	def __init__(self, *args):
+		super(Day, self).__init__(*args)
+
+class DataPath(str):
+	def __new__(self, val):
+		return super(DataPath, self).__new__(self, '*' * val['depth'] + val['case'])
+	def __init__(self, val):
+		self.data = val
+		super(DataPath, self).__init__()
+	def __getitem__(self, key):
+		return self.data[key]
+	def full(self):
+		return pjoin(self['prefix'], self['key'], self['case'])
+
+def sorter():
+	global natsort_warned
+	try:
+		if not natsort_warned:
+			check_install('natsort')
+		import natsort
+		return lambda inp : natsort.natsorted(inp, alg = natsort.ns.IGNORECASE)
+	except:
+		if not natsort_warned:
+			log.warning(u'`natsort`用于给测试点名称排序，不使用的话可能会出现10排在2前面的情况。')
+			natsort_warned = True
+		return sorted
+
+class Datum(dict):
+	def __init__(self, datum, prob = None, key = 'data'):
+		super(Datum, self).__init__(datum)
+		self.prob = prob
+		self.key = key
+	def ml(self):
+		return Memory(self['memory limit']) if 'memory limit' in self else self.prob.ml()
+
+class Problem(Configure):
+	def statement(self, cur_lang = None):
+		if not cur_lang and lang:
+			cur_lang = lang
+		if cur_lang:
+			source = pjoin(self.path, 'statement', cur_lang + '.md')
+			if os.path.exists(source):
+				self.language = cur_lang
+				return source
+		for source, self.language in (
+			(pjoin(self.path, 'statement', 'zh-cn.md'), 'zh-cn'),
+			(pjoin(self.path, 'statement', 'en.md'), 'en'),
+			(pjoin(self.path, 'description.md'), None)
+		):
+			if os.path.exists(source):
+				return source
+		raise NoFileException('No md file found.')
+	def lang(self):
+		try:
+			self.statement()
+			return self.language
+		except NoFileException as e:
+			return None
+	def __init__(self, *args):
+		super(Problem, self).__init__(*args)
+		self.chk = None
+		self.data = self.get_data('data')
+		self.samples = self.get_data('samples')
+		self.pre = self.get_data('pre')
+	def set_default(self, path = None):
+		super(Problem, self).set_default(path)
+		if 'title' not in self and 'cnname' in self:
+			self['title'] = {'zh-cn' : self.pop('cnname')}
+		for data, cases, attr, key in [('data', 'test cases', 'test_cases', 'data'), ('samples', 'sample count', 'sample_cases', 'down'), ('pre', 'pre count', 'pre_cases', 'pre')]:
+			tc = set()
+			if hasattr(self, data) and self.__getattribute__(data) != None:
+				for datum in self.__getattribute__(data):
+					tc |= set(datum['cases'])
+			else:
+				self[data] = []
+			if cases in self and type(self[cases]) == int:
+				log.warning(u'`%s`字段不再使用，使用`python -m tuack.gen upgrade`升级。' % cases)
+				#to_dp = lambda i : DataPath({'case' : self['name'] + str(i), 'key' : key, 'depth' : 0, 'prefix' : self.path})
+				#self[data] = [{'cases' : [
+				#	to_dp(i) for i in range(1, self.pop(cases) + 1) \
+				#	if to_dp(i) not in tc
+				#]}]
+			self.__setattr__(attr, sorter()(list(tc)))
+	def set_score(self):
+		if 'packed' in self:
+			log.warning(u'题目`%s`的`packed`字段不再有效，但仍可以存在，用`python -m tuack.gen upgrade`升级。' % self.route)
+		for key, packed in [('data', ''), ('pre', '_pre'), ('down', '_sample')]:
+			if not hasattr(self, key):
+				self.__setattr__('packed' + packed, False)
+				return
+			num_unscored = 0
+			total_score = 0.0
+			data_objs = self.__getattribute__(key)
+			if data_objs is None:
+				continue
+			for datum in data_objs:
+				if 'score' in datum:
+					datum.score = datum['score']
+					total_score += datum['score']
+				else:
+					num_unscored += 1
+			if num_unscored != 0:
+				item_score = (100. - total_score) / num_unscored
+				for datum in data_objs:
+					if 'score' not in datum:
+						datum.score = item_score
+			if num_unscored == len(data_objs):
+				self.__setattr__('packed' + packed, False)
+				self.__setattr__('score' + packed, 100.)
+			else:
+				self.__setattr__('packed' + packed, True)
+				if num_unscored != 0:
+					log.warning(u'题目`%s`有%d个包设置了`score`，有%d个没有；总分共设%f分，将剩下%f分平分给没有的包。' % (
+						self.route,
+						len(data_objs) - num_unscored,
+						num_unscored,
+						total_score,
+						100 - total_score
+					))
+					log.info(u'如果你需要不等分+打包测试，请每个包设置`score`；否则请每个包都不设置`score`，此时是每个测试点同分而不是每个包同分。')
+					log.info(u'一部分包设置`score`，另一部分不设置将可能导致导出其他格式时出现问题。')
+					if key != 'data':
+						log.warning(u'以上信息属于这道题的%s，不属于标准测试点。' % {'pre' : u'预测试点', 'down': u'样例'}[key])
+					self.__setattr__('score' + packed, 100.)
+				else:
+					if abs(total_score - 100) > 1e-6:
+						log.warning(u'题目`%s`总分是%f分，不是100分。' % (self.route, total_score))
+						if key != 'data':
+							log.warning(u'以上信息属于这道题的%s，不属于标准测试点。' % {'pre' : u'预测试点', 'down': u'样例'}[key])
+					self.__setattr__('score' + packed, total_score)
+
+	def extend_pathed(self, path):
+		if path.startswith(':'):
+			return self.parent.extend_pathed(path[1:])
+		return pjoin(self.path, path)
+
+	def users(self):
+		def users_pathed(self, users, key = '', depth = 0):
+			if type(users) != dict:
+				log.warning(u'`json.conf`中，`users`项%s:%s已经过时，但仍可以使用，用`python -m tuack.gen upgrade`升级' % (key, users))
+				return {
+					'path' : self.extend_pathed(users),
+					'expected' : {}
+				}
+			elif depth == 2:
+				# Is detailed description
+				if "path" not in users:
+					# Ill-formed
+					log.warning(u'`users`项%s:%s不含`path`项' % (key, users))
+					return None
+				return {
+					'path' : self.extend_pathed(users["path"]),
+					'expected' : users["expected"] if "expected" in users else {}
+				}
+
+			return {
+				key : val
+				for key, val in \
+				((key, users_pathed(self, val, key, depth + 1)) for key, val in users.items()) \
+				if val
+			}
+		return self.getitem('users', users_pathed)
+	
+	def expect(self, user, algo, score):
+		'''
+		Check expected scores
+		'''
+		exp = self.users()[user][algo]['expected']
+		algo_failed = False
+		if type(exp) == dict:
+			for symbol, value in exp.items():
+				algo_failed |= not eval('round(score, 8) %s %s' % (symbol, value))
+		elif type(exp) == list:
+			for pred in exp:
+				algo_failed |= not eval('round(score, 8) %s' % pred)
+		elif type(exp) == str:
+			algo_failed |= not eval('round(score, 8) %s' % exp)
+		elif exp is None:
+			pass
+		else:
+			log.warning('`expected`字段必须是字符串、数组或字典。')
+		return not algo_failed
+
+	def get_data(self, key):
+		def data_pathed(self, data, key, depth):
+			key_map = {
+				'data' : 'data',
+				'samples' : 'down',
+				'pre' : 'pre'
+			}
+			ret = []
+			for datum in data:
+				tmp = []
+				for case in datum['cases']:
+					cur = self
+					dep = depth
+					cas = str(case)
+					while cas.startswith(':'):
+						cas = cas[1:]
+						dep -= 1
+						cur = cur.parent
+					tmp.append(DataPath({'case' : cas, 'key' : key_map[key], 'depth' : dep, 'prefix' : cur.path}))
+				datum_fixed = datum.copy()
+				datum_fixed['cases'] = tmp
+				ret.append(Datum(datum_fixed, self, key))
+			return ret
+		return self.getitem(key, data_pathed)
+
+	def ml(self):
+		return Memory(self.get('memory limit', '2 GB'))
+
+	def memory_limit(self):
+		return self.ml()
+
+#mem_json = {}	# 题目复用的话，需要记忆化
+
+def load_json(path = '.', route = None):
+	#abs_path = os.path.abspath(path)
+	#if abs_path in mem_json:
+	#	return mem_json[abs_path]
+	for name in ['conf.yaml', 'conf.json', 'prob.json']:
+		try:
+			full_path = pjoin(path, name)
+			if os.path.isfile(full_path):
+				inp = open(full_path, 'rb').read().decode('utf-8')
+				if name.endswith('json'):
+					conf = json.loads(inp)
+				elif name.endswith('yaml'):
+					conf = yaml.full_load(inp)
+				if conf.get('version', -1) > json_version:
+					log.warning(u'`conf.*`版本高于`tuack`，请升级`tuack`。')
+				if 'folder' not in conf:
+					conf['folder'] = 'problem'
+				args = [conf, path]
+				if conf['folder'] == 'extend':
+					base_conf = load_json(pjoin(path, conf['base path']))
+					folder = base_conf.folder
+					args.append(base_conf)
+				else:
+					folder = conf['folder']
+				conf = eval(folder.capitalize())(*args)
+				if conf['folder'] == 'extend':
+					conf.folder = base_conf.folder
+				conf.set_default(os.path.basename(path))
+				conf.route = '' if route == None else rjoin(route, conf['name'])
+				if conf.folder == 'problem':
+					conf.set_score()
+				if 'subdir' in conf:
+					conf.sub = []
+					for sub in conf['subdir']:
+						ret = load_json(pjoin(path, sub), conf.route)
+						if ret:
+							conf.sub.append(ret)
+				#mem_json[abs_path] = conf
+				return conf
+		except Exception as e:
+			log.warning(u'文件`%s`错误。' % pjoin(path, name))
+			log.info(e)
+			log.info('可能会导致运行到该目录下出现问题。')
+	else:
+		#raise NoFileException(u'路径`%s`下找不到conf.*。' % path)
+		log.warning(u'路径`%s`下找不到conf.*。' % path)
+		log.info('可能会导致运行到该目录下出现问题。')
+
+def del_redundance(conf, red):
+	for key in red:
+		try:
+			conf.pop(key)
+		except:
+			pass
+	if not conf['name'] or conf['name'] == '.':
+		conf.pop('name')
+	return conf
+
+dump_formats = {
+	'json' : lambda conf : json.dumps(conf, indent = 2, sort_keys = True, ensure_ascii = False).encode('utf-8'),
+	'yaml' : lambda conf : yaml.safe_dump(dict(conf), encoding = 'utf-8', allow_unicode = True)
+}
+
+def save_json(conf):
+	for s in conf.sub:
+		save_json(s)
+	try:
+		open(pjoin(conf.path, 'conf.' + dump_format), 'wb').write(dump_formats[dump_format](conf))
+	except Exception as e:
+		log.error(u'不支持配置文件格式`%s`。' % dump_format)
+		log.info(e)
+
+def any_prefix(pre, st = None):
+	if not st:
+		st = sub_set
+	for s in st:
+		if s == pre:
+			return 1
+		if pre == '' or s.startswith(pre + '/'):
+			return 2
+	return 0
+
+def mkdir(name):
+	if not os.path.exists(name):
+		os.makedirs(name)
+
+def remkdir(name):
+	while True:
+		try:
+			shutil.rmtree(name, ignore_errors = True)
+			time.sleep(0.1)
+			if not os.path.exists(name):
+				os.makedirs(name)
+			break
+		except Exception as e:
+			log.warning('Can\'t delete %s' % name)
+			log.warning(e)
+
+def copy(source, name, target):
+	full_source = pjoin(source, name)
+	if not os.path.exists(full_source):
+		raise NoFileException('No such file or path `%s`.' % full_source)
+	copied_data.add(full_source)
+	if os.path.isdir(full_source):
+		if full_source.endswith('.dir') or no_compiling:
+			full_target = (pjoin(target, name) if os.path.exists(target) else target)
+			if full_source.endswith('.dir'):
+				full_target = full_target[:-4]
+			shutil.copytree(full_source, full_target)
+		else:
+			# TODO: make if there is a makefile
+			ret = os.getcwd()
+			os.chdir(pjoin(source, name))
+			cpp_file = name + '.cpp'
+			elf_file = name + elf_suffix
+			check_install('g++')
+			if os.system('g++ %s -o %s -O2 -std=c++14 -Wall' % (cpp_file, elf_file)) != 0:
+				os.chdir(ret)
+				log.error(u'`%s`编译失败。' % pjoin(full_source, cpp_file))
+				return True
+			else:
+				os.chdir(ret)
+				log.info(u'`%s`编译成功。' % pjoin(full_source, cpp_file))
+			shutil.move(pjoin(full_source, elf_file), target)
+	else:
+		shutil.copy(full_source, target)
+	return True
+
+def shutil_copy(source, target):
+	func = shutil.copytree if os.path.isdir(source) else shutil.copy
+	func(source, target)
+
+def xopen_file(path):
+	try:
+		if system == 'Windows':
+			os.startfile(path)
+		elif system == 'Darwin':
+			subprocess.call(["open", path])
+		else:
+			subprocess.call(["xdg-open", path])
+	except Exception as e:
+		log.warning(u'打开文件`%s`失败。' % path)
+		log.info(e)
+
+def deal_args():
+	global do_copy_files, do_test_progs, do_release, works, start_file, do_pack, langs, lang, sub_set, out_system, args, do_zip, do_encript, do_render, time_multiplier, git_lfs, dump_format, user_time, water_mark, noi_pas_c
+	do_render = True
+	works = []
+	args = []
+	langs = [None]
+	lang = None
+	sub_set = None
+	start_file = True
+	do_pack = True
+	do_zip = False
+	do_encript = False
+	git_lfs = False
+	user_time = False
+	dump_format = 'yaml'
+	water_mark = False
+	noi_pas_c = False
+	l = len(sys.argv)
+	i = 1
+	while i < l:
+		if sys.argv[i] == '-i':
+			i += 1
+			os.chdir(sys.argv[i])
+		elif sys.argv[i] == '-p':
+			i += 1
+			sub_set = set(sys.argv[i].split(','))
+		elif sys.argv[i] == '-o':
+			i += 1
+			out_system = sys.argv[i]
+		elif sys.argv[i] == '-d':
+			i += 1
+			dump_format = sys.argv[i]
+		elif sys.argv[i] == '-s':
+			start_file = False
+		elif sys.argv[i] == '-k':
+			do_pack = False
+		elif sys.argv[i] == '-z':
+			do_zip = True
+		elif sys.argv[i] == '-g':
+			git_lfs = True
+		elif sys.argv[i] == '-r':
+			do_render = False
+		elif sys.argv[i] == '-e':
+			do_zip = True
+			do_encript = True
+		elif sys.argv[i] == '-u':
+			user_time = True
+		elif sys.argv[i] == '-l':
+			i += 1
+			langs = set(sys.argv[i].split(','))
+		elif sys.argv[i] == '-t':
+			i += 1
+			time_multiplier = float(sys.argv[i])
+		elif sys.argv[i] == '--noi-pas-c':
+			noi_pas_c = True
+		elif sys.argv[i] == '-w':
+			i += 1
+			water_mark = sys.argv[i]
+		elif sys.argv[i] == '-h' or sys.argv[i] == '--help':
+			log.info(u'详细用法见文档：https://git.thusaac.com/publish/tuack/wikis。')
+			log.info(u'python 脚本 [[[工作1],工作2],...] [[[选项1] 选项2] ...] [[[参数1] 参数2] ...]')
+			log.info(u'工作必须在参数前面，工作用逗号隔开，选项和参数用空格隔开。')
+			log.info(u'只有有逗号的项目可以用逗号获得多个结果，逗号前后不能有空白符。')
+			log.info(u'这套工具的大多数脚本都可以在比赛、比赛日和题目目录下运行。')
+			log.info(u'选项：')
+			log.info(u'  -i PATH             指定PATH作为工作路径，否则使用当前路径。')
+			log.info(u'  -s                  对于有输出的文件的操作，输出完以后不自动打开文件。')
+			log.info(u'  -p day0/sleep,day2  只对day0/sleep和day2进行本次操作；此路径是基于当前文件夹的，')
+			log.info(u'                      例如：在比赛日目录如day1下，则可以直接指定题目如exam；')
+			log.info(u'                      对于test，还可以指定用户或算法，如day1/problem/vfk/std.cpp。')
+			log.info(u'  -t 6.0              对于test，设置掐断时间为6.0*时间限制，用于对比不同程序的时限。')
+			log.info(u'  -o SYSTEM           对于ren，输出指定操作系统的题面，可选Windows和Linux。')
+			log.info(u'  -l zh-cn,en         对于ren，指定输出语言，不指定默认为zh-cn。')
+			log.info(u'  -w logo.png         对于ren，给PDF添加水印，默认不添加。')
+			log.info(u'  --noi-pas-c         对于ren渲染noi格式，强制在封面添加pas和c。')
+			log.info(u'  -r                  对于dump，不先尝试渲染题面。')
+			log.info(u'  -g                  对于gen，使用git-lfs。')
+			log.info(u'  -d json             对于gen，规定配置文件格式，支持json、yaml，默认yaml。')
+			log.info(u'  -u                  对于test，在linux下使用user time做测试，默认real time。')
+			
+			return False
+		else:
+			if len(works) == 0:
+				works = sys.argv[i].split(',')
+			else:
+				args += sys.argv[i].split(',')
+		i += 1
+	return True
+
+def custom_conf():
+	get_tool_conf()
+	c = env_conf['file_log'] if 'file_log' in env_conf else {}
+	file_log = logging.FileHandler(
+		c['path'] if 'path' in c else 'tuack.log',
+		mode = c['mode'] if 'mode' in c else 'a',
+		encoding = c['encoding'] if 'encoding' in c else None
+	)
+	file_log.setLevel(c['level'] if 'level' in c else logging.INFO)
+	file_log.setFormatter(logging.Formatter(
+		c['format'] if 'format' in c else '[%(levelname).1s]%(filename)s:%(funcName)s:%(lineno)d:%(message)s'
+	))
+	log.addHandler(file_log)
+
+	c = env_conf['bash_log'] if 'bash_log' in env_conf else {}
+	if 'encoding' in c:
+		class MyStream(object):
+			def __init__(self, stream):
+				self.stream = stream
+			def write(self, s):
+				self.stream.buffer.write(s.encode(c['encoding']))
+				self.stream.flush()
+			def flush(self):
+				self.stream.flush()
+		bash_log = logging.StreamHandler(MyStream(sys.stdout))
+	else:
+		bash_log = logging.StreamHandler()
+	bash_log.setLevel(c['level'] if 'level' in c else logging.DEBUG)
+	bash_log.setFormatter(logging.Formatter(
+		c['format'] if 'format' in c else '[%(levelname).1s]%(message)s'
+	))
+	log.addHandler(bash_log)
+
+def init():
+	import __main__
+	global conf
+	custom_conf()
+	if not deal_args():
+		return False
+	log.info(
+		('脚本%s，工程路径%s，参数%s，开始于%s。' if python_version[0] == 2 else u'脚本%s，工程路径%s，参数%s，开始于%s。') % (
+			__main__.__file__, os.getcwd(), str(sys.argv[1:]), str(datetime.datetime.now())
+		)
+	)
+	conf = load_json()
+	try:
+		check_install('git')
+		check_install('git_lfs')
+	except:
+		pass
+	return True
+
+def tr(item):
+	if 'zh-cn' in item:
+		return item['zh-cn']
+	elif 'en' in item:
+		return item['en']
+	elif len(item) > 1:
+		for val in item.values():
+			return val
+	else:
+		return 'Unknown'
+
+def run_r(cmd, path):
+	for f in os.listdir(path):
+		cpath = pjoin(path, f)
+		if os.path.isfile(cpath):
+			cmd(cpath)
+		else:
+			run_r(cmd, cpath)
+
+def get_tool_conf():
+	def get_sys_env():
+		return '$'.join([
+			os.environ[key]
+			for key in ['OS', 'SESSIONNAME', 'USERNAME', 'COMPUTERNAME', 'USERDOMAIN', 'USER', 'SHELL', 'SESSION'] \
+			if key in os.environ
+		] + ['py%x' % sys.hexversion])
+	global env_conf
+	try:
+		tool_conf = json.loads(open(pjoin(tool_path, 'conf.json'), 'rb').read().decode('utf-8'))
+	except:
+		tool_conf = {}
+	sys_env = get_sys_env()
+	if sys_env not in tool_conf:
+		tool_conf[sys_env] = {}
+	env_conf = tool_conf[sys_env]
+	return tool_conf
+
+def check_install(pack):
+	def check_import(pack, extra_info = '', pack_name = None, level = logging.ERROR):
+		try:
+			__import__(pack)
+		except Exception as e:
+			log.log(level, u'python包%s没有安装，使用 pip install %s 安装。%s' % (pack, pack_name if pack_name else pack, extra_info))
+			if system == 'Windows':
+				log.info(u'如果pip没有安装，Windows下推荐用Anaconda等集成环境。')
+			if system == 'Linux':
+				log.info(u'如果pip没有安装，Ubuntu下用 sudo apt install python-pip 安装。')
+			raise e
+	check_pyside = lambda : check_import('PySide', u'注意这个包只能在 python2 下使用。', 'pyside')
+	check_natsort = lambda : check_import('natsort', level = logging.WARNING)
+	def check_pandoc():
+		ret = os.system('pandoc -v')
+		if ret != 0:
+			log.error(u'格式转换工具pandoc没有安装。')
+			if system == 'Windows':
+				log.info(u'Windows用户去官方网站下载安装，安装好后把pandoc.exe所在路径添加到环境变量PATH中。')
+			if system == 'Linux':
+				log.info(u'Ubuntu下用 sudo apt install pandoc 安装。')
+			raise Exception('pandoc not found')
+	def check_xelatex():
+		ret = os.system('xelatex --version')
+		if ret != 0:
+			log.error(u'TeX渲染工具XeLaTeX没有安装。')
+			if system == 'Windows':
+				log.info(u'Windows下可以先安装MiKTeX，在首次运行的时候会再提示安装后续文件。')
+			if system == 'Linux':
+				log.info(u'Ubuntu下先用 sudo apt install texlive-xetex texlive-fonts-recommended texlive-latex-extra 安装工具；')
+				log.info(u'然后一般会因为缺少有些字体而报错（Windows有使用权，但Ubuntu没有，所以没有预装这些字体）。')
+				log.info(u'可以使用下列页面上的方法安装缺少的字体或是把win下的字体复制过来。')
+				log.info(u'http://linux-wiki.cn/wiki/zh-hans/LaTeX%E4%B8%AD%E6%96%87%E6%8E%92%E7%89%88%EF%BC%88%E4%BD%BF%E7%94%A8XeTeX%EF%BC%89')
+			raise Exception('xelatex not found')
+	def check_git():
+		ret = os.system('git --version')
+		if ret != 0:
+			log.warning(u'版本管理工具git没有安装，如果工程用git维护则你的修改可能无法成功提交。')
+			log.info(u'一个可能的安装教程见这里：')
+			log.info(u'https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git')
+			if system == 'Windows':
+				log.info(u'Windows下有多种不同的git版本，大家可以多交流好用的版本。')
+			log.info(u'git入门可以参看这里：')
+			log.info(u'http://rogerdudler.github.io/git-guide/index.zh.html')
+			log.info(u'一般推荐用ssh方式克隆仓库，并用公私钥保证安全，添加密钥的方式一般仓库的git网页上能找到。')
+			raise Exception('git not found')
+	def check_git_lfs():
+		ret = os.system('git lfs')
+		if ret != 0:
+			log.warning(u'git大文件系统lfs没有安装，如果工程使用了它你可能无法同步。')
+			log.info(u'因为有些评测数据比较大，所以一般要求用git lfs大文件系统（Large File System）管理评测数据（in/ans）')
+			log.info(u'一个可能的安装教程见这里：')
+			log.info(u'https://git-lfs.github.com/')
+			log.info(u'如果你用本工具的generator生成题目工程，那么你装好lfs以后一般可以不用再手工指定in和ans文件用lfs管理。')
+			log.info(u'如果你的多人合作工程用到了lfs，请务必不要在没有安装lfs前把数据添加到工程中！')
+			raise Exception('git lfs not found')
+
+	def check_gpp():
+		ret = os.system('g++ -v')
+		if ret != 0:
+			log.warning(u'g++未安装，将可能无法测试C++代码。')
+			raise Exception('g++ not found')
+	
+	def check_gcc():
+		ret = os.system('gcc -v')
+		if ret != 0:
+			log.warning(u'gcc未安装，将可能无法测试C代码。')
+			raise Exception('gcc not found')
+			
+	def check_java():
+		ret = os.system('javac -version')
+		if ret != 0:
+			log.warning(u'javac未安装，将可能无法测试Java代码。')
+			raise Exception('javac not found')
+		ret = os.system('java -version')
+		if ret != 0:
+			log.warning(u'java未安装，将可能无法测试Java代码。')
+			raise Exception('java not found')
+
+	def check_py2():
+		ret = os.system('python2 --version')
+		if ret != 0:
+			log.warning(u'python2未安装，将可能无法测试Python2代码。')
+			raise Exception('python2 not found')
+
+	def check_py3():
+		ret = os.system('python3 --version')
+		if ret != 0:
+			log.warning(u'python3未安装，将可能无法测试Python3代码。')
+			raise Exception('python3 not found')
+
+	def check_py():
+		ret = os.system('python --version')
+		if ret != 0:
+			log.warning(u'python未安装，将可能无法测试Python代码。')
+			raise Exception('python not found')
+			
+	def check_flex():
+		ret = os.system('flex --version')
+		if ret != 0:
+			log.warning(u'flex未安装，将可能无法检查题面格式。')
+			raise Exception('flex not found')
+
+	def check_bison():
+		ret = os.system('bison --version')
+		if ret != 0:
+			log.warning(u'bison未安装，将可能无法检查题面格式。')
+			raise Exception('bison not found')
+			
+	def check_format():
+		ret = os.system('"%s" -v' % pjoin(tool_path, format_checker_name))
+		if ret != 0:
+			log.warning(u'format checker未安装，使用`python -m tuack.install format`安装。')
+			raise Exception('format not found')
+			
+	def check_unrar():
+		ret = os.system('unrar --version')
+		if ret != 0:
+			log.warning(u'unrar未安装，将无法解压rar文件，请安装unrar。')
+			log.warning(u'对于Windows用户，你可以将WinRar的安装目录添加到PATH。')
+			raise Exception('unrar not found')
+
+	def check_time():
+		ret = os.system('time ls')
+		if ret != 0:
+			log.warning(u'time未安装，将无法测试运行时间。')
+			log.warning(u'类Ubuntu用户可以用apt install time安装。')
+			raise Exception('time not found')
+
+	if pack in {'g++', 'cpp'}:
+		pack = 'gpp'
+	if pack == 'c':
+		pack = 'gcc'
+	global tool_conf
+	tool_conf = get_tool_conf()
+	if 'installed' not in env_conf:
+		env_conf['installed'] = {}
+	if pack in env_conf['installed'] and env_conf['installed'][pack]:
+		return True
+	if isfunction('check_' + pack):
+		eval('check_' + pack)()
+	else:
+		check_import(pack)
+	env_conf['installed'][pack] = True
+
+	open(pjoin(tool_path, 'conf.json'), 'wb').write(json.dumps(tool_conf, indent = 2, sort_keys = True).encode('utf-8'))
+	return True
+
+def change_eol(path, eol, show_path = None):
+	import uuid
+	ufname = str(uuid.uuid4()) + '.tmp'
+	space_end = False
+	is_text = True
+	with open(ufname, 'wb') as f:
+		try:
+			for idx, line in enumerate(open(path, 'rb')):
+				line = line.rstrip(b'\r\n')
+				f.write(line + eol)
+				if not space_end and (line.endswith(b' ') or line.endswith(b'\t')):
+					log.warning(u'换行符转换：文件`%s`第%d行末尾有空白符。' % (show_path if show_path else path, idx + 1))
+					space_end = True
+				for code in ['utf-8', 'gbk']:
+					try:
+						if '\0' in line.decode(code):
+							raise Exception('`\\0` in line')
+						break
+					except:
+						pass
+				else:
+					is_text = False
+					log.info(u'换行符转换：文件`%s`不是文本文件。' % (show_path if show_path else path))
+					break
+		except:
+			is_text = False
+	if is_text:
+		os.remove(path)
+		time.sleep(0.1)
+		os.rename(ufname, path)
+	else:
+		os.remove(ufname)
+
+unix2dos = lambda path, show_path = None : change_eol(path, b'\r\n', show_path)
+dos2unix = lambda path, show_path = None : change_eol(path, b'\n', show_path)
+
+wiki = lambda name : name
+
+def run_exc(func):
+	try:
+		return (True, func())
+	except Exception as e:
+		log.error(e)
+		log.info(traceback.format_exc())
+		return (False, None)
```

### Comparing `tuack-0.1.4.9.2/tuack/doc.py` & `tuack-0.1.5/tuack/doc.py`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,522 +1,522 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-import platform
-from . import base
-from .base import log, pjoin
-
-vars_re = r"\{%-? *do *vars\.__setitem__\( *'sample_id' *, *(\d+) *\) -%\}"
-
-title_choices = {
-	'sample' : {
-		u'样例(\\d+)?',
-		u'输入输出样例(\\d+)?',
-		u'样例输入输出(\\d+)?',
-		u'测试用例(\\d+)?',
-		r'sample\s*(\d+)?',
-		vars_re
-	},
-	'sample input' : {
-		u'样例(\\d+)?输入(\\d+)?',
-		u'输入(\\d+)?样例(\\d+)?',
-		r'sample\s*input\s*(\d+)?',
-		r'input\s*sample\s*(\d+)?'
-	},
-	'sample output' : {
-		u'样例(\\d+)?输出(\\d+)?',
-		u'输出(\\d+)?样例(\\d+)?',
-		r'sample\s*output\s*(\d+)?',
-		r'output\s*sample\s*(\d+)?'
-	},
-	'sample explanation' : {
-		u'样例(\\d+)?说明(\\d+)?',
-		u'样例(\\d+)?解释(\\d+)?',
-		r'sample\s*explanation\s*(\d+)?'
-	},
-	'input' : {
-		u'输入',
-		'input'
-	},
-	'output' : {
-		u'输出',
-		'output'
-	},
-	'explanation' : {
-		u'解释',
-		u'说明',
-		'explanation'
-	},
-	'input format' : {
-		u'输入格式',
-		u'输入说明',
-		u'输入要求',
-		'input format'
-	},
-	'output format' : {
-		u'输出格式',
-		u'输出说明',
-		u'输出要求',
-		'output format'
-	},
-	'description' : {
-		u'题目描述',
-		u'题目说明',
-		u'题目',
-		u'问题描述',
-		u'问题说明',
-		u'问题',
-		'description',
-		'statement',
-	},
-	'background' : {
-		u'题目背景',
-		u'背景',
-		'background',
-	},
-	'hint' : {
-		u'提示',
-		u'温馨提示',
-		u'hint'
-	},
-	'subtasks' : {
-		u'(数据规模|要求|限制|约束|约定|子任务)(与(数据规模|要求|限制|约束|约定|子任务))?',
-		r'subtask(s?)'
-	},
-	'scoring' : {
-		u'评分方式',
-		'scoring'
-	}
-}
-
-new_re_symbols = {
-	r'\C' : '[\u4e00-\u9fbf]',
-	r'\P' : '[\uff00-\uffef\u3000-\u303f\u2000-\u203f]'
-}
-
-text_patterns = {
-	u'中文和英文、字符串或公式中间没有空格' : r'\C(?:\w|`|\$)',
-	u'英文、字符串或公式和中文中间没有空格' : r'(?:\w|`|\$)\C',
-	u'中文之间有空格' : r'\C \C',
-	u'使用了英文标点或不在公式中的运算符号' : '[,\\.\\?\\:;\'"\\[\\]\\{\\}!\\\\\\|\\(\\)\\+=]'
-}
-
-title_re = re.compile('^(' + '|'.join(['|'.join(value) for value in title_choices.values()]) + ')$')
-std_title_re = re.compile('^\{\{ *s\( *\'(.*)\' *(( *, *[-+.\'\"a-zA-Z0-9_ ]+)*)\) *\}\} *$')
-doc_title_re = u'^#* *( *【|\{\{ *_ *\( *\')?(%s)(\' *\) *\}\}|】)?( *\{#.*\})? *#* *$'
-html_equation_re = re.compile(r'\\\[(.*)\\\]\{\.math \.inline\}')
-format_log_re = re.compile(r'^(\w) (\d+) (.*)$')
-
-math_trans = {
-	'*' : '',
-	u'≤' : r' \le',
-	u'≥' : r' \ge',
-	u'←' : r' \leftarrow',
-	u'→' : r' \rightarrow',
-	u'×' : r' \times',
-	u'∑' : r' \sum',
-	r'\$' : ''
-}
-
-def is_digit(s):
-	for c in s:
-		if not '0' <= c <= '9':
-			return False
-	return True
-
-def is_english(s):
-	for c in s:
-		if not('a' <= c <= 'z' and 'A' <= c <= 'Z'):
-			return False
-	return True
-
-def is_chinese(s):
-	for c in s:
-		if not u'\u4e00' <= c <= u'\u9fbf':
-			return False
-	return True
-
-def get_text(s):
-	ret = ''
-	for c in s:
-		if is_chinese(c) or is_english(c) or is_digit(c):
-			ret += c
-	return ret.lower()
-	
-def html_math2tex_math(s):
-	ret = ''
-	i = 0
-	l = len(s)
-	in_sup = False
-	in_sub = False
-	while True:
-		if i == l:
-			break
-		if i + 1 < l:
-			flag = False
-			if s[i:i+2] == '\*':
-				ret += '*'
-			elif s[i:i+2] == '\^':
-				if in_sup:
-					ret += ' }'
-				else:
-					ret += '^{ '
-				in_sup ^= True
-			elif s[i:i+2] == '\~':
-				if in_sub:
-					ret += ' }'
-				else:
-					ret += '_{ '
-				in_sub ^= True
-			elif s[i:i+2] in math_trans:
-				ret += math_trans[s[i:i+2]]
-			else:
-				flag = True
-			if not flag:
-				i += 2
-				continue
-		if s[i] in math_trans:
-			ret += math_trans[s[i]]
-		else:
-			ret += s[i]
-		i += 1
-	return ret
-
-class Section:
-	used = {'input' : 0, 'output' : 0}
-	def __init__(self, name = None, args = None):
-		self.name = name
-		if args == None:
-			self.args = []
-		else:
-			self.args = args
-		self.lines = []
-	def clear_paragraph(self):
-		flag = True
-		for idx, line in enumerate(self.lines):
-			if idx % 2 == 1 and line.rstrip('\n\r') != '':
-				flag = False
-		if flag:
-			self.lines = [line for idx, line in enumerate(self.lines) if idx % 2 == 0]
-	def write(self, f, idx = None):
-		if self.name == 'sample':
-			if len(self.lines) == 0:
-				return
-			else:
-				self.args.append('')
-		for name, suf in [('input', '.in'), ('output', '.ans')]:
-			if self.name == 'sample ' + name or self.name == name:
-				self.used[name] += 1
-				self.clear_paragraph()
-				with open(pjoin(base.prob.path, 'down', str(self.used[name]) + suf), 'w') as ff:
-					if len(self.lines) > 1 and self.lines[0].startswith('```'):
-						lines = self.lines[1:-1]
-					else:
-						lines = self.lines
-					for line in lines:
-						ff.write(line + '\n')
-				if name == 'input':
-					f.write(b'{{ s(\'sample\', %d) }}\n\n{{ self.sample_text() }}\n\n' % self.used[name])
-				return
-		if idx == 0:
-			f.write(b'{{ self.title() }}\n')
-		if idx == 0 and self.name and self.name not in title_choices:
-			base.prob['title'][base.prob.lang()] = self.name.strip()
-		elif self.name:
-			f.write(("\n{{ s('%s'%s) }}\n\n" % (
-				self.name,
-				', ' + ', '.join(map(json.dumps, self.args)) if len(self.args) > 0 else ''
-			)).encode('utf-8'))
-		for line in self.lines:
-			f.write((line + '\n').encode('utf-8'))
-	def is_empty(self):
-		return not self.name and len(self.lines) == 0
-	def format_line(self, line):
-		ret = line
-		while True:
-			m = html_equation_re.search(ret)
-			if not m:
-				break
-			while True:
-				sm = m
-				l, r = sm.span()
-				sub = sm.string[l:r - 1]
-				m = html_equation_re.search(sub)
-				if m:
-					continue
-				sub = sm.string[l:r]
-				res = sm.group(1)
-				ret = ret.replace(sub, '$%s$' % html_math2tex_math(res))
-				break
-		return ret
-	def format(self):
-		self.lines = [self.format_line(line) for line in self.lines]
-
-def sure_title(line):
-	inp = line
-	if inp.startswith('##'):
-		return True
-	if inp.startswith(u'【') and inp.endswith(u'】'):
-		return True
-	if std_title_re.match(inp):
-		return True
-	if re.match(vars_re, inp):
-		return True
-	txt = get_text(inp)
-	if title_re.match(txt):
-		return True
-	return False
-
-def get_title(line):
-	m = std_title_re.match(line)
-	if m:
-		gps = m.groups()
-		name = gps[0]
-		args = json.loads('[' + ','.join(gps[1].split(',')[1:]) + ']')
-		return name, args
-	m = re.match(doc_title_re % '[-+.\'\"a-zA-Z0-9_ \u4e00-\u9fa5\u3040-\u309f\u30a0-\u30ff]+', line.lower())
-	if m:
-		title = m.group(2)
-		m = title_re.match(title)
-		if m:
-			for key, pts in title_choices.items():
-				for pt in pts:
-					m = re.match('^' + pt + '$', title)
-					if m:
-						name = key
-						args = []
-						if key.startswith('sample'):
-							for s in m.groups():
-								if s and s != '':
-									args = [json.loads(s)]
-									log.debug(args)
-									break
-						return name, args
-		return title, []
-	return line, []
-
-def to_sections(lines):
-	def clear(buff):
-		if buff != []:
-			cur.lines.append(' '.join(buff))
-			cur.lines.append('')
-			buff = []
-		return buff
-	sections = []
-	cur = Section()
-	buff = []
-	in_quote = False
-	in_quote_space = False
-	in_quote_tab = False
-	in_equation = False
-	in_table = False
-	last_title = 0
-	for line in lines:
-		if in_quote_space:
-			if line.startswith('    '):
-				cur.lines.append(line.lstrip(' '))
-				continue
-			else:
-				in_quote_space = False
-				cur.lines.append('```')
-		elif in_quote_tab:
-			if line.startswith('\t'):
-				cur.lines.append(line.lstrip(' '))
-				continue
-			else:
-				in_quote_tab = False
-				cur.lines.append('```')
-		elif in_table:
-			if line.startswith('  '):
-				cur.lines.append(line)
-				continue
-			else:
-				in_table = False
-		if in_quote:
-			if line == '```':
-				in_quote = False
-			cur.lines.append(line)
-		elif in_equation:
-			if line == '$$':
-				in_quote = False
-			cur.lines.append(line)
-		else:
-			last_title = last_title - 1 if last_title >= 1 else 0
-			if line.startswith('```'):
-				in_quote = True
-				buff = clear(buff)
-				cur.lines.append(line)
-			elif line.strip() == '$$':
-				in_equation = True
-				buff = clear(buff)
-				cur.lines.append(line)
-			elif sure_title(line):
-				buff = clear(buff)
-				title, args = get_title(line)
-				if not cur.is_empty():
-					sections.append(cur)
-				cur = Section(title, args)
-				last_title = 2
-			elif line.startswith('    '):
-				in_quote_space = True
-				buff = clear(buff)
-				cur.lines.append('```')
-				cur.lines.append(line.lstrip(' '))
-			elif line.startswith('\t'):
-				in_quote_space = True
-				buff = clear(buff)
-				cur.lines.append('```')
-				cur.lines.append(line.lstrip(' '))
-			elif line.startswith('  '):
-				in_table = True
-				buff = clear(buff)
-				cur.lines.append(line)
-			elif line.startswith('------'):
-				if last_title >= 1:
-					continue
-				if buff != []:
-					buff.pop()
-				buff = clear(buff)
-				title, args = get_title(last)
-				if not cur.is_empty():
-					sections.append(cur)
-				cur = Section(title, args)
-			elif line == '':
-				buff = clear(buff)
-			else:
-				buff.append(line)
-		last = line
-	buff = clear(buff)
-	if not cur.is_empty():
-		sections.append(cur)
-	return sections
-
-def format():
-	for base.prob in base.probs():
-		prob = base.prob
-		path = pjoin(base.conf.path, 'statement', base.conf.lang() + '.md')
-		lines = [line.rstrip(b'\r\n').decode('utf-8') for line in open(path, 'rb').readlines()]
-		sections = to_sections(lines)
-		for section in sections:
-			section.format()
-		with open(path, 'wb') as f:
-			for idx, section in enumerate(sections):
-				section.write(f, idx)
-	base.save_json(base.conf)
-
-def format_check_one(path):
-	log.info(u'检查文件`%s`。' % path)
-	widths = [
-		(126, 1), (159, 0), (687, 1), (710, 0), (711, 1), 
-		(727, 0), (733, 1), (879, 0), (1154, 1), (1161, 0), 
-		(4347, 1), (4447, 2), (7467, 1), (7521, 0), (8369, 1), 
-		(8426, 0), (9000, 1), (9002, 2), (11021, 1), (12350, 2), 
-		(12351, 1), (12438, 2), (12442, 0), (19893, 2), (19967, 1),
-		(55203, 2), (63743, 1), (64106, 2), (65039, 1), (65059, 0),
-		(65131, 2), (65279, 1), (65376, 2), (65500, 1), (65510, 2),
-		(120831, 1), (262141, 2), (1114109, 1),
-	]
-	def get_width(o):
-		if o == '\t':
-			return 4
-		o = ord(o)
-		if o == 0xe or o == 0xf:
-			return 0
-		for num, wid in widths:
-			if o <= num:
-				return wid
-		return 1
-	def output():
-		level = {
-			'E' : log.error,
-			'W' : log.warning,
-			'I' : log.info,
-			'D' : log.debug,
-		}[logs[idx][0]]
-		level(u'第%d行，第%d个字：%s' % (lineno, col, logs[idx][2]))
-		lef = col - 10 if col > 10 else 0
-		rig = min(lef + 21, len(code.rstrip()))
-		log.info(code[lef:rig].replace('\u200b', '?').replace('\t', '    '))
-		lef_cur = 0
-		for c in code[:lef]:
-			lef_cur += get_width(c)
-		log.info(' ' * (cur - lef_cur) + u'↑')
-	os.system('%s < %s > format.tmp 2> format.log' % (
-		pjoin(base.tool_path, base.format_checker_name),
-		path
-	))
-	tot = 0
-	logs = []
-	for line in open('format.log', 'rb'):
-		m = format_log_re.match(line.decode('utf-8').rstrip())
-		if m:
-			logs.append((m.group(1), int(m.group(2)), m.group(3)))
-	if len(logs) == 0:
-		return
-	idx = 0
-	for lineno, line in enumerate(open(path, 'rb'), 1):
-		code = line.decode('utf-8')
-		cur = 0
-		for col, ch in enumerate(code):
-			tot += len(ch.encode('utf-8'))
-			if tot >= logs[idx][1]:
-				output()
-				idx += 1
-			if idx >= len(logs):
-				return
-			cur += get_width(ch)
-
-def format_check():
-	base.check_install('format')
-	for base.prob in base.probs():
-		prob = base.prob
-		path = pjoin(prob.path, 'statement', 'zh-cn.md')
-		format_check_one(path)
-
-def load():
-	if len(base.args) != 1:
-		log.error(u'无法转换，必须传入恰好一个参数。')
-		sys.exit(1)
-	if base.conf.folder != 'problem':
-		log.error(u'只能处理单个题目，请到题目目录下进行操作。')
-		sys.exit(1)
-	os.system('pandoc %s -o %s' % (base.args[0], pjoin(base.conf.path, 'statement', base.conf.lang() + '.md')))
-
-class_list = {
-	'load' : load,
-	'format' : format,
-	'check' : format_check
-}
-
-if __name__ == '__main__':
-	try:
-		if base.init():
-			base.check_install('pandoc')
-			base.check_install('jinja2')
-			for base.work in base.works:
-				for base.lang in base.langs:
-					base.run_exc(class_list[base.work])
-		else:
-			log.info(u'这是用来处理题面的工具。')
-			log.info(u'支持的工作：')
-			log.info(u'  load     必须包含一个参数输入文件名，表示要导入的题面。')
-			log.info(u'  format   尝试对当前的中文题面进行简单的格式化，危险操作请注意备份。')
-			log.info(u'  check    对题面进行格式检查。')
-			sys.exit(1)
-	except base.NoFileException as e:
-		log.error(e)
-		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
-		sys.exit(1)
-
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+import platform
+from . import base
+from .base import log, pjoin
+
+vars_re = r"\{%-? *do *vars\.__setitem__\( *'sample_id' *, *(\d+) *\) -%\}"
+
+title_choices = {
+	'sample' : {
+		u'样例(\\d+)?',
+		u'输入输出样例(\\d+)?',
+		u'样例输入输出(\\d+)?',
+		u'测试用例(\\d+)?',
+		r'sample\s*(\d+)?',
+		vars_re
+	},
+	'sample input' : {
+		u'样例(\\d+)?输入(\\d+)?',
+		u'输入(\\d+)?样例(\\d+)?',
+		r'sample\s*input\s*(\d+)?',
+		r'input\s*sample\s*(\d+)?'
+	},
+	'sample output' : {
+		u'样例(\\d+)?输出(\\d+)?',
+		u'输出(\\d+)?样例(\\d+)?',
+		r'sample\s*output\s*(\d+)?',
+		r'output\s*sample\s*(\d+)?'
+	},
+	'sample explanation' : {
+		u'样例(\\d+)?说明(\\d+)?',
+		u'样例(\\d+)?解释(\\d+)?',
+		r'sample\s*explanation\s*(\d+)?'
+	},
+	'input' : {
+		u'输入',
+		'input'
+	},
+	'output' : {
+		u'输出',
+		'output'
+	},
+	'explanation' : {
+		u'解释',
+		u'说明',
+		'explanation'
+	},
+	'input format' : {
+		u'输入格式',
+		u'输入说明',
+		u'输入要求',
+		'input format'
+	},
+	'output format' : {
+		u'输出格式',
+		u'输出说明',
+		u'输出要求',
+		'output format'
+	},
+	'description' : {
+		u'题目描述',
+		u'题目说明',
+		u'题目',
+		u'问题描述',
+		u'问题说明',
+		u'问题',
+		'description',
+		'statement',
+	},
+	'background' : {
+		u'题目背景',
+		u'背景',
+		'background',
+	},
+	'hint' : {
+		u'提示',
+		u'温馨提示',
+		u'hint'
+	},
+	'subtasks' : {
+		u'(数据规模|要求|限制|约束|约定|子任务)(与(数据规模|要求|限制|约束|约定|子任务))?',
+		r'subtask(s?)'
+	},
+	'scoring' : {
+		u'评分方式',
+		'scoring'
+	}
+}
+
+new_re_symbols = {
+	r'\C' : '[\u4e00-\u9fbf]',
+	r'\P' : '[\uff00-\uffef\u3000-\u303f\u2000-\u203f]'
+}
+
+text_patterns = {
+	u'中文和英文、字符串或公式中间没有空格' : r'\C(?:\w|`|\$)',
+	u'英文、字符串或公式和中文中间没有空格' : r'(?:\w|`|\$)\C',
+	u'中文之间有空格' : r'\C \C',
+	u'使用了英文标点或不在公式中的运算符号' : '[,\\.\\?\\:;\'"\\[\\]\\{\\}!\\\\\\|\\(\\)\\+=]'
+}
+
+title_re = re.compile('^(' + '|'.join(['|'.join(value) for value in title_choices.values()]) + ')$')
+std_title_re = re.compile('^\{\{ *s\( *\'(.*)\' *(( *, *[-+.\'\"a-zA-Z0-9_ ]+)*)\) *\}\} *$')
+doc_title_re = u'^#* *( *【|\{\{ *_ *\( *\')?(%s)(\' *\) *\}\}|】)?( *\{#.*\})? *#* *$'
+html_equation_re = re.compile(r'\\\[(.*)\\\]\{\.math \.inline\}')
+format_log_re = re.compile(r'^(\w) (\d+) (.*)$')
+
+math_trans = {
+	'*' : '',
+	u'≤' : r' \le',
+	u'≥' : r' \ge',
+	u'←' : r' \leftarrow',
+	u'→' : r' \rightarrow',
+	u'×' : r' \times',
+	u'∑' : r' \sum',
+	r'\$' : ''
+}
+
+def is_digit(s):
+	for c in s:
+		if not '0' <= c <= '9':
+			return False
+	return True
+
+def is_english(s):
+	for c in s:
+		if not('a' <= c <= 'z' and 'A' <= c <= 'Z'):
+			return False
+	return True
+
+def is_chinese(s):
+	for c in s:
+		if not u'\u4e00' <= c <= u'\u9fbf':
+			return False
+	return True
+
+def get_text(s):
+	ret = ''
+	for c in s:
+		if is_chinese(c) or is_english(c) or is_digit(c):
+			ret += c
+	return ret.lower()
+	
+def html_math2tex_math(s):
+	ret = ''
+	i = 0
+	l = len(s)
+	in_sup = False
+	in_sub = False
+	while True:
+		if i == l:
+			break
+		if i + 1 < l:
+			flag = False
+			if s[i:i+2] == '\*':
+				ret += '*'
+			elif s[i:i+2] == '\^':
+				if in_sup:
+					ret += ' }'
+				else:
+					ret += '^{ '
+				in_sup ^= True
+			elif s[i:i+2] == '\~':
+				if in_sub:
+					ret += ' }'
+				else:
+					ret += '_{ '
+				in_sub ^= True
+			elif s[i:i+2] in math_trans:
+				ret += math_trans[s[i:i+2]]
+			else:
+				flag = True
+			if not flag:
+				i += 2
+				continue
+		if s[i] in math_trans:
+			ret += math_trans[s[i]]
+		else:
+			ret += s[i]
+		i += 1
+	return ret
+
+class Section:
+	used = {'input' : 0, 'output' : 0}
+	def __init__(self, name = None, args = None):
+		self.name = name
+		if args == None:
+			self.args = []
+		else:
+			self.args = args
+		self.lines = []
+	def clear_paragraph(self):
+		flag = True
+		for idx, line in enumerate(self.lines):
+			if idx % 2 == 1 and line.rstrip('\n\r') != '':
+				flag = False
+		if flag:
+			self.lines = [line for idx, line in enumerate(self.lines) if idx % 2 == 0]
+	def write(self, f, idx = None):
+		if self.name == 'sample':
+			if len(self.lines) == 0:
+				return
+			else:
+				self.args.append('')
+		for name, suf in [('input', '.in'), ('output', '.ans')]:
+			if self.name == 'sample ' + name or self.name == name:
+				self.used[name] += 1
+				self.clear_paragraph()
+				with open(pjoin(base.prob.path, 'down', str(self.used[name]) + suf), 'w') as ff:
+					if len(self.lines) > 1 and self.lines[0].startswith('```'):
+						lines = self.lines[1:-1]
+					else:
+						lines = self.lines
+					for line in lines:
+						ff.write(line + '\n')
+				if name == 'input':
+					f.write(b'{{ s(\'sample\', %d) }}\n\n{{ self.sample_text() }}\n\n' % self.used[name])
+				return
+		if idx == 0:
+			f.write(b'{{ self.title() }}\n')
+		if idx == 0 and self.name and self.name not in title_choices:
+			base.prob['title'][base.prob.lang()] = self.name.strip()
+		elif self.name:
+			f.write(("\n{{ s('%s'%s) }}\n\n" % (
+				self.name,
+				', ' + ', '.join(map(json.dumps, self.args)) if len(self.args) > 0 else ''
+			)).encode('utf-8'))
+		for line in self.lines:
+			f.write((line + '\n').encode('utf-8'))
+	def is_empty(self):
+		return not self.name and len(self.lines) == 0
+	def format_line(self, line):
+		ret = line
+		while True:
+			m = html_equation_re.search(ret)
+			if not m:
+				break
+			while True:
+				sm = m
+				l, r = sm.span()
+				sub = sm.string[l:r - 1]
+				m = html_equation_re.search(sub)
+				if m:
+					continue
+				sub = sm.string[l:r]
+				res = sm.group(1)
+				ret = ret.replace(sub, '$%s$' % html_math2tex_math(res))
+				break
+		return ret
+	def format(self):
+		self.lines = [self.format_line(line) for line in self.lines]
+
+def sure_title(line):
+	inp = line
+	if inp.startswith('##'):
+		return True
+	if inp.startswith(u'【') and inp.endswith(u'】'):
+		return True
+	if std_title_re.match(inp):
+		return True
+	if re.match(vars_re, inp):
+		return True
+	txt = get_text(inp)
+	if title_re.match(txt):
+		return True
+	return False
+
+def get_title(line):
+	m = std_title_re.match(line)
+	if m:
+		gps = m.groups()
+		name = gps[0]
+		args = json.loads('[' + ','.join(gps[1].split(',')[1:]) + ']')
+		return name, args
+	m = re.match(doc_title_re % '[-+.\'\"a-zA-Z0-9_ \u4e00-\u9fa5\u3040-\u309f\u30a0-\u30ff]+', line.lower())
+	if m:
+		title = m.group(2)
+		m = title_re.match(title)
+		if m:
+			for key, pts in title_choices.items():
+				for pt in pts:
+					m = re.match('^' + pt + '$', title)
+					if m:
+						name = key
+						args = []
+						if key.startswith('sample'):
+							for s in m.groups():
+								if s and s != '':
+									args = [json.loads(s)]
+									log.debug(args)
+									break
+						return name, args
+		return title, []
+	return line, []
+
+def to_sections(lines):
+	def clear(buff):
+		if buff != []:
+			cur.lines.append(' '.join(buff))
+			cur.lines.append('')
+			buff = []
+		return buff
+	sections = []
+	cur = Section()
+	buff = []
+	in_quote = False
+	in_quote_space = False
+	in_quote_tab = False
+	in_equation = False
+	in_table = False
+	last_title = 0
+	for line in lines:
+		if in_quote_space:
+			if line.startswith('    '):
+				cur.lines.append(line.lstrip(' '))
+				continue
+			else:
+				in_quote_space = False
+				cur.lines.append('```')
+		elif in_quote_tab:
+			if line.startswith('\t'):
+				cur.lines.append(line.lstrip(' '))
+				continue
+			else:
+				in_quote_tab = False
+				cur.lines.append('```')
+		elif in_table:
+			if line.startswith('  '):
+				cur.lines.append(line)
+				continue
+			else:
+				in_table = False
+		if in_quote:
+			if line == '```':
+				in_quote = False
+			cur.lines.append(line)
+		elif in_equation:
+			if line == '$$':
+				in_quote = False
+			cur.lines.append(line)
+		else:
+			last_title = last_title - 1 if last_title >= 1 else 0
+			if line.startswith('```'):
+				in_quote = True
+				buff = clear(buff)
+				cur.lines.append(line)
+			elif line.strip() == '$$':
+				in_equation = True
+				buff = clear(buff)
+				cur.lines.append(line)
+			elif sure_title(line):
+				buff = clear(buff)
+				title, args = get_title(line)
+				if not cur.is_empty():
+					sections.append(cur)
+				cur = Section(title, args)
+				last_title = 2
+			elif line.startswith('    '):
+				in_quote_space = True
+				buff = clear(buff)
+				cur.lines.append('```')
+				cur.lines.append(line.lstrip(' '))
+			elif line.startswith('\t'):
+				in_quote_space = True
+				buff = clear(buff)
+				cur.lines.append('```')
+				cur.lines.append(line.lstrip(' '))
+			elif line.startswith('  '):
+				in_table = True
+				buff = clear(buff)
+				cur.lines.append(line)
+			elif line.startswith('------'):
+				if last_title >= 1:
+					continue
+				if buff != []:
+					buff.pop()
+				buff = clear(buff)
+				title, args = get_title(last)
+				if not cur.is_empty():
+					sections.append(cur)
+				cur = Section(title, args)
+			elif line == '':
+				buff = clear(buff)
+			else:
+				buff.append(line)
+		last = line
+	buff = clear(buff)
+	if not cur.is_empty():
+		sections.append(cur)
+	return sections
+
+def format():
+	for base.prob in base.probs():
+		prob = base.prob
+		path = pjoin(base.conf.path, 'statement', base.conf.lang() + '.md')
+		lines = [line.rstrip(b'\r\n').decode('utf-8') for line in open(path, 'rb').readlines()]
+		sections = to_sections(lines)
+		for section in sections:
+			section.format()
+		with open(path, 'wb') as f:
+			for idx, section in enumerate(sections):
+				section.write(f, idx)
+	base.save_json(base.conf)
+
+def format_check_one(path):
+	log.info(u'检查文件`%s`。' % path)
+	widths = [
+		(126, 1), (159, 0), (687, 1), (710, 0), (711, 1), 
+		(727, 0), (733, 1), (879, 0), (1154, 1), (1161, 0), 
+		(4347, 1), (4447, 2), (7467, 1), (7521, 0), (8369, 1), 
+		(8426, 0), (9000, 1), (9002, 2), (11021, 1), (12350, 2), 
+		(12351, 1), (12438, 2), (12442, 0), (19893, 2), (19967, 1),
+		(55203, 2), (63743, 1), (64106, 2), (65039, 1), (65059, 0),
+		(65131, 2), (65279, 1), (65376, 2), (65500, 1), (65510, 2),
+		(120831, 1), (262141, 2), (1114109, 1),
+	]
+	def get_width(o):
+		if o == '\t':
+			return 4
+		o = ord(o)
+		if o == 0xe or o == 0xf:
+			return 0
+		for num, wid in widths:
+			if o <= num:
+				return wid
+		return 1
+	def output():
+		level = {
+			'E' : log.error,
+			'W' : log.warning,
+			'I' : log.info,
+			'D' : log.debug,
+		}[logs[idx][0]]
+		level(u'第%d行，第%d个字：%s' % (lineno, col, logs[idx][2]))
+		lef = col - 10 if col > 10 else 0
+		rig = min(lef + 21, len(code.rstrip()))
+		log.info(code[lef:rig].replace('\u200b', '?').replace('\t', '    '))
+		lef_cur = 0
+		for c in code[:lef]:
+			lef_cur += get_width(c)
+		log.info(' ' * (cur - lef_cur) + u'↑')
+	os.system('%s < %s > format.tmp 2> format.log' % (
+		pjoin(base.tool_path, base.format_checker_name),
+		path
+	))
+	tot = 0
+	logs = []
+	for line in open('format.log', 'rb'):
+		m = format_log_re.match(line.decode('utf-8').rstrip())
+		if m:
+			logs.append((m.group(1), int(m.group(2)), m.group(3)))
+	if len(logs) == 0:
+		return
+	idx = 0
+	for lineno, line in enumerate(open(path, 'rb'), 1):
+		code = line.decode('utf-8')
+		cur = 0
+		for col, ch in enumerate(code):
+			tot += len(ch.encode('utf-8'))
+			if tot >= logs[idx][1]:
+				output()
+				idx += 1
+			if idx >= len(logs):
+				return
+			cur += get_width(ch)
+
+def format_check():
+	base.check_install('format')
+	for base.prob in base.probs():
+		prob = base.prob
+		path = pjoin(prob.path, 'statement', 'zh-cn.md')
+		format_check_one(path)
+
+def load():
+	if len(base.args) != 1:
+		log.error(u'无法转换，必须传入恰好一个参数。')
+		sys.exit(1)
+	if base.conf.folder != 'problem':
+		log.error(u'只能处理单个题目，请到题目目录下进行操作。')
+		sys.exit(1)
+	os.system('pandoc %s -o %s' % (base.args[0], pjoin(base.conf.path, 'statement', base.conf.lang() + '.md')))
+
+class_list = {
+	'load' : load,
+	'format' : format,
+	'check' : format_check
+}
+
+if __name__ == '__main__':
+	try:
+		if base.init():
+			base.check_install('pandoc')
+			base.check_install('jinja2')
+			for base.work in base.works:
+				for base.lang in base.langs:
+					base.run_exc(class_list[base.work])
+		else:
+			log.info(u'这是用来处理题面的工具。')
+			log.info(u'支持的工作：')
+			log.info(u'  load     必须包含一个参数输入文件名，表示要导入的题面。')
+			log.info(u'  format   尝试对当前的中文题面进行简单的格式化，危险操作请注意备份。')
+			log.info(u'  check    对题面进行格式检查。')
+			sys.exit(1)
+	except base.NoFileException as e:
+		log.error(e)
+		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
+		sys.exit(1)
+
```

### Comparing `tuack-0.1.4.9.2/tuack/dump.py` & `tuack-0.1.5/tuack/dump.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,554 +1,701 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-import platform
-from . import base
-from .base import log, pjoin
-import requests
-
-
-def lemon(conf = None):
-	base.check_install('pyside')
-	if not conf:
-		if base.conf.folder == 'problem':
-			raise Exception('Can\'t dump a single problem to lemon, try to dump a day or a contest.')
-		base.remkdir('lemon')
-		if base.conf.folder == 'day':
-			lemon(base.conf)
-		else:
-			for day in base.days():
-				os.makedirs(base.pjoin('lemon', day.route))
-				lemon(day)
-		return
-	log.info(u'导出lemon工程：%s' % conf.route)
-	os.makedirs(base.pjoin('lemon', conf.route, 'data'))
-	os.makedirs(base.pjoin('lemon', conf.route, 'source'))
-	jzp_magic = 0x20111127
-	zlib_magic = 0x185E
-	import zlib
-	from PySide import QtCore
-	obuff = QtCore.QByteArray()
-	ost = QtCore.QDataStream(obuff, QtCore.QIODevice.WriteOnly)
-	ost.writeQString(conf['name'])
-	probs = list(conf.probs())
-	ost.writeInt32(len(probs))
-	for prob in probs:
-		log.info(u'导出lemon题目：%s' % prob.route)
-		ost.writeQString(base.tr(prob['title']))
-		ost.writeQString(prob['name'])
-		ost.writeQString(prob['name'] + '.in')
-		ost.writeQString(prob['name'] + '.out')
-		ost.writeBool(False)
-		ost.writeBool(False)
-		ost.writeInt32(1 if prob['type'] == 'output' else 0)
-		ost.writeInt32(1)		# Judge Type TODO: What if there is spj (code = 4)
-		ost.writeQString('--ignore-space-change --text --brief')
-		ost.writeInt32(3)		# real precision (float number error bound)
-		ost.writeQString('')	# spj route TODO: What if there is spj
-		ost.writeInt32(len([i for i in prob.get('compile', {}) if i in {'cpp', 'c', 'pas'}]))
-		for key, val in prob.get('compile', {}).items():
-			try:
-				ost.writeQString({
-					'cpp' : 'g++',
-					'c' : 'gcc',
-					'pas' : 'fpc'
-				}[key])
-				ost.writeQString(val)
-			except:
-				pass
-		ost.writeQString('out')
-		if prob.packed:
-			ost.writeInt32(len(prob['data']))
-			for datum in prob['data']:
-				ost.writeInt32(datum['score'])
-				ost.writeInt32(datum.get('time limit', prob.get('time limit', 0)) * 1000)
-				ost.writeInt32(base.Memory(datum.get('memory limit', prob.get('memory limit', '0 B'))).MB)
-				tc = datum['cases']
-				ost.writeInt32(len(tc))
-				for c in tc:
-					ost.writeQString(base.pjoin(prob['name'], str(c) + '.in'))
-				ost.writeInt32(len(tc))
-				for c in tc:
-					ost.writeQString(base.pjoin(prob['name'], str(c) + '.ans'))
-		else:
-			score = (100. / len(prob.test_cases) if len(prob.test_cases) > 0 else 0.)
-			ost.writeInt32(len(prob.test_cases))
-			for c in prob.test_cases:
-				ost.writeInt32(score)
-				ost.writeInt32(prob['time limit'] * 1000)
-				ost.writeInt32(prob.memory_limit().MB)
-				ost.writeInt32(1)
-				ost.writeQString(base.pjoin(prob['name'], str(c) + '.in'))
-				ost.writeInt32(1)
-				ost.writeQString(base.pjoin(prob['name'], str(c) + '.ans'))
-		
-		sp = list(prob.route.split('/'))
-		target = ['lemon'] + sp[:-1] + ['data', sp[-1]]
-		shutil.copytree(base.pjoin(prob.path, 'data'), base.pjoin(*target))
-	
-	compressed = QtCore.QByteArray(zlib.compress(str(obuff)))
-	obuff = QtCore.QByteArray()
-	ost = QtCore.QDataStream(obuff, QtCore.QIODevice.WriteOnly)
-	ost.writeUInt32(zlib_magic)
-	ost.writeRawData(str(compressed))
-	file_ = QtCore.QFile(base.pjoin('lemon', conf.route, conf['name'] + '.cdf'))
-	file_.open(QtCore.QIODevice.WriteOnly)
-	ofs = QtCore.QDataStream(file_)
-	ofs.writeUInt32(jzp_magic)
-	ofs.writeUInt16(QtCore.qChecksum(str(obuff), len(obuff)))
-	ofs.writeUInt32(len(obuff))
-	ofs.writeRawData(str(obuff))
-	file_.close()
-	
-	base.run_r(base.unix2dos, base.pjoin('lemon', conf.route, 'data'))
-	
-	if base.do_zip:
-		import zipfile
-		with zipfile.ZipFile(base.pjoin('lemon', conf.route) + '.zip', 'w') as z:
-			base.run_r(lambda path : z.write(path), base.pjoin('lemon', conf.route))
-	log.warning(u'目前SPJ的支持暂时还没有实现，有需要请手工配置。')
-	log.warning(u'目前lemon的编译选项是写在注册表里的，暂时没有实现该功能，请手工配置。')
-
-def arbiter_main(conf = None,daynum = 0):
-	def arbiter_info(info, filename):
-		with open(filename,'wb') as ofile:
-			for key, val in info.items():
-				ofile.write(('%s%s\n' % (key, val)).encode('gbk'))
-	if not conf:
-		log.info('makedirs')
-		if not os.path.exists('arbiter'):
-			base.remkdir('arbiter')
-		base.remkdir(pjoin('arbiter', 'main'))
-		os.makedirs(base.pjoin('arbiter', 'main','data'))
-		os.makedirs(base.pjoin('arbiter', 'main','final'))
-		os.makedirs(base.pjoin('arbiter', 'main','players'))
-		os.makedirs(base.pjoin('arbiter', 'main','result'))
-		os.makedirs(base.pjoin('arbiter', 'main','filter'))
-		os.makedirs(base.pjoin('arbiter', 'main','tmp'))
-		if base.conf.folder == 'problem':
-			raise Exception('Can\'t dump a single problem to arbiter, try to dump a day or a contest.')
-		if base.conf.folder == 'day':
-			arbiter(base.days())
-		else:
-			for idx, day in enumerate(base.days(), start = 1):
-				os.makedirs(base.pjoin('arbiter', 'main','players','day%d' % idx))
-				os.makedirs(base.pjoin('arbiter', 'main','result','day%d' % idx))
-				arbiter_main(day,idx)
-			log.info('dos2unix')
-			base.run_r(base.dos2unix, base.pjoin('arbiter', 'main', 'data'))
-			shutil.copytree(base.pjoin('arbiter', 'main','data'),base.pjoin('arbiter', 'main','evaldata'))	#这里也不能直接copy，见下面的处理方式
-			cfg = {}
-			cfg['NAME='] = base.conf['name']
-			cfg['DAYNUM='] = idx
-			cfg['ENV='] = 'env.info'
-			cfg['PLAYER='] = 'player.info'
-			cfg['TEAM='] = 'team.info'
-			cfg['MISC='] = 'misc.info'
-			arbiter_info(cfg,base.pjoin('arbiter', 'main','setup.cfg'))
-			team = {}
-			arbiter_info(team,base.pjoin('arbiter', 'main','team.info'))
-			'''arbiter_info(userlist,base.pjoin('arbiter','player.info'))'''
-		return
-	dayinfo = {}
-	dayinfo['NAME='] = u'第'+str(daynum)+u'场'+u'--机试'
-	dayinfo['PLAYERDIR='] = ''
-	dayinfo['CASEDIR='] = ''
-	dayinfo['BASESCORE='] = 0
-	dayinfo['TASKNUM='] = len(conf['subdir'])
-	arbiter_info(dayinfo,base.pjoin('arbiter', 'main', 'day%d.info' % daynum))
-	for probnum, prob in enumerate(conf.sub, start = 1):
-		log.info(prob['name'])
-		probinfo = {}
-		probinfo['TITLE='] = ''
-		probinfo['NAME='] = prob['name']
-		probinfo['RUN='] = ''
-		probinfo['INFILESUFFIX='] = 'in'
-		probinfo['ANSFILESUFFIX='] = 'ans'
-		probinfo['PLUG='] = prob['name']+'_e'
-		if prob['type'] == 'program':
-			probinfo['TYPE='] = 'SOURCE'
-		else:
-			log.warning(u'暂时只支持非交互式程序题。')
-		probinfo['LIMIT='] = int(prob['time limit'])
-		probinfo['MEMLIMITS='] = int(prob.memory_limit().MB)
-		probinfo['SAMPLES='] = len(prob.test_cases)
-		score_per_case = 100 // len(prob.test_cases)
-		if not prob.packed and score_per_case * len(prob.test_cases) != 100:
-			log.warning(u'测试点数量不是100的约数，分数无法均分为整数。')
-		probinfo['CCL=c@gcc'] = ' -o %o %i ' + prob['compile']['c']
-		probinfo['CCL=cpp@g++'] = ' -o %o %i ' + prob['compile']['cpp']
-		probinfo['CCL=pas@fpc'] = ' %i ' + prob['compile']['pas']
-		idx = 0
-		for datum in prob.data:
-			if prob.packed and len(datum['cases']) > 1:
-				log.warning(u'Arbiter不支持打包评测，将把该包得分均分给包中各测试点，无法整除时总分将不正确。')
-			for case in datum['cases']:
-			#for idx, case in enumerate(prob.test_cases, start = 1):
-				idx += 1
-				'''print('copyfile %s'%base.pjoin(prob.path,'data',case+'.in'))'''
-				shutil.copy(
-					base.pjoin(prob.path,'data',str(case)+'.in'),
-					base.pjoin('arbiter', 'main','data',prob['name']+str(idx)+'.in')
-				)
-				'''print('copyfile %s'%base.pjoin(prob.path,'data',case+'.ans'))'''
-				shutil.copy(
-					base.pjoin(prob.path,'data',str(case)+'.ans'),
-					base.pjoin('arbiter', 'main','data',prob['name']+str(idx)+'.ans')
-				)
-				if prob.packed:
-					probinfo['MARK='+str(idx)+'@'] = str(int(datum['score'] / len(datum['cases'])))
-				else:
-					probinfo['MARK='+str(idx)+'@'] = str(int(score_per_case))
-		'''for idx, userdir in enumerate(prob['users'],start = 1):
-			for idx2, code in enumerate(prob['users'][userdir],start = 1):
-				dirname = prob['name']+'-'+str(idx)+str(idx2)
-				codename = userdir + code
-				tmplist = prob['users'][userdir][code].split('/')
-				codedir = base.pjoin(prob.path,*tmplist)
-				os.makedirs(base.pjoin('arbiter','players',conf['name'],dirname,prob['name']))
-				shutil.copy(codedir,base.pjoin('arbiter','players',conf['name'],dirname,prob['name']))
-				userlist[dirname + '@'] =  codename'''
-		shutil.copy(base.pjoin(base.path,'sample','arbiter_e.sample'),base.pjoin('arbiter', 'main','filter',prob['name']+'_e'))
-		arbiter_info(probinfo,base.pjoin('arbiter', 'main','task'+str(daynum)+'_'+str(probnum)+'.info'))
-
-def arbiter_down(conf = None):
-	if not conf:
-		conf = base.conf
-		if not os.path.exists('arbiter'):
-			base.remkdir('arbiter')
-		base.remkdir(pjoin('arbiter', 'down'))
-	if conf.folder == 'problem':
-		raise Exception('Can\'t dump a single problem to arbiter, try to dump a day or a contest.')
-	if conf.folder == 'contest':
-		for idx, day in enumerate(base.days(), start = 1):
-			os.makedirs(base.pjoin(pjoin('arbiter', 'down'), day['name']))
-			arbiter_down(day)
-		log.info('dos2unix')
-		base.run_r(base.dos2unix, base.pjoin(pjoin('arbiter', 'down')))
-		return
-	for prob in conf.probs():
-		log.info(prob.route)
-		os.makedirs(base.pjoin(pjoin('arbiter', 'down'), prob.route))
-		for idx, case in enumerate(prob.sample_cases, start = 1):
-			shutil.copy(
-				base.pjoin(prob.path,'down',str(case)+'.in'),
-				base.pjoin('arbiter', 'down', prob.route, prob['name']+str(idx)+'.in')
-			)
-			shutil.copy(
-				base.pjoin(prob.path,'down',str(case)+'.ans'),
-				base.pjoin('arbiter', 'down', prob.route, prob['name']+str(idx)+'.ans')
-			)
-
-def arbiter():
-	base.remkdir('arbiter')
-	arbiter_main()
-	arbiter_down()
-
-def tsinsen_oj():
-	import random
-	if type(base.conf) != base.Problem:
-		log.error(u'只能转换一道题目，请到相应题目目录下运行')
-		return
-	hash_ch = list(map(
-		chr,
-		[ord('a') + i for i in range(26)] + \
-		[ord('A') + i for i in range(26)] + \
-		[ord('0') + i for i in range(10)]
-	))
-	hash = lambda l = 10 : ''.join([hash_ch[random.randint(0, len(hash_ch) - 1)] for i in range(l)])
-	if not os.path.exists('tsinsen-oj'):
-		os.makedirs('tsinsen-oj')
-	for day in base.days():
-		p = base.pjoin('tsinsen-oj', day.route)
-		if not os.path.exists(p):
-			os.makedirs(p)
-	for prob in base.probs():
-		p = base.pjoin('tsinsen-oj', prob.route)
-		if not os.path.exists(p):
-			os.makedirs(p)
-		if os.path.exists(base.pjoin(prob.path, 'down')):
-			with zipfile.ZipFile(base.pjoin('tsinsen-oj', prob.route, 'down.zip'), 'w') as z:
-				base.run_r(lambda path : z.write(path), base.pjoin(prob.path, 'down'))
-			prob.tsinsen_down = hash(8)
-		else:
-			prob.tsinsen_down = None
-		files = {}
-		path = base.pjoin(prob.path, 'resources')
-		if os.path.exists(path):
-			base.run_r(lambda p : files.__setitem__(p[len(path) + 1:], hash(8)), path)
-		prob.tsinsen_files = files
-	if base.do_render:
-		from . import ren
-		tmp = base.start_file
-		base.start_file = False
-		ren.Html('tsinsen-oj').run()
-		base.start_file = tmp
-	else:
-		log.warning(u'如果你使用了文件，不重新渲染题面会导致tsinsen的文件失效。')
-	
-	read_file = lambda path : open(path, 'rb').read().decode('utf-8')
-	
-	Title = lambda : prob.tr('title')
-	CheckPoint = lambda : prob['key words'] if 'key words' in prob else ''
-	TestMethod = lambda : 'DEFAULT'
-	InputFileName = lambda : ''
-	OutputFileName = lambda : ''
-	TimeLimit = lambda : '%.1fs' % prob['time limit']
-	MemoryLimit = lambda : '%.1fMB' % prob.memory_limit().MB
-	
-	def Checkers():
-		path = base.pjoin('data', 'chk', 'chk.cpp')
-		if os.path.exists(path):
-			return open(path, 'rb').read().decode('utf-8')
-		else:
-			return '\n'
-	def Description():
-		path = pjoin('statements', 'tsinsen-oj', prob.route if prob.route != '' else prob['name']) + '.html'
-		if not os.path.exists(path):
-			log.warning(u'找不到题面，你可能需要自己手工添加题面。')
-			return ''
-		header = u'<p>下载目录：<img src="/RequireFile.do?fid=%s" alt="另存为图片下载" />（另存为图片下载）</p>\n' % prob.tsinsen_down
-		return header + read_file(path)
-	def Solution():
-		for user, codes in prob['users'].items():
-			for name, path in codes.items():
-				if prob.expect(user, name, 100):
-					return read_file(path['path'])
-		for user, codes in prob['users'].items():
-			for name, path in codes.items():
-				return read_file(path)
-		return ''
-	def add_shell(name, func):
-		h = hash()
-		ret = '%s=\n' % name
-		ret += '======================%s\n' % h
-		res = func()
-		if not res.endswith('\n'):
-			res += '\n'
-		ret += res
-		ret += '======================%s\n' % h
-		return ret.encode('utf-8')
-	def to_base64(path):
-		import base64
-		s = base64.b64encode(open(path, 'rb').read()).decode('utf-8')
-		return '\n'.join(s[pos:pos+76] for pos in range(0, len(s), 76))
-	tokens = [
-		'Title', 'CheckPoint', 'Checkers', 'TestMethod', 'Description',
-		'InputFileName', 'OutputFileName', 'Solution', 'TimeLimit', 'MemoryLimit'
-	]
-	for prob in base.probs():
-		result_file = base.pjoin('tsinsen-oj', prob.route) + '.txt'
-		with open(result_file, 'wb') as f:
-			for token in tokens:
-				f.write(add_shell(token, eval(token)))
-			if prob.packed:
-				log.warning(u'清橙OJ不支持打包评测和指定测试点分值，直接将所有测试点视为相同。')
-			for datum in prob.test_cases:
-				f.write(add_shell('InData', lambda : read_file(base.pjoin('data', datum + '.in'))))
-				f.write(add_shell('OutData', lambda : read_file(base.pjoin('data', datum + '.ans'))))
-			if prob.tsinsen_down:
-				f.write(add_shell('FileName', lambda : 'down.zip'))
-				f.write(add_shell('File(%s)' % prob.tsinsen_down, lambda : to_base64(base.pjoin('tsinsen-oj', prob.route, 'down.zip'))))
-			for key, val in prob.tsinsen_files.items():
-				f.write(add_shell('FileName', lambda : key.replace('/', '-').replace('\\', '-')))
-				f.write(add_shell('File(%s)' % val, lambda : to_base64(base.pjoin(prob.path, 'resources', key))))
-		if base.start_file:
-			base.xopen_file(result_file)
-
-def tuoj_down(conf = None):
-	if not conf:
-		conf = base.conf
-		if not os.path.exists('tuoj'):
-			base.remkdir('tuoj')
-		base.remkdir(pjoin('tuoj', 'down'))
-	if conf.folder == 'contest':
-		for day in base.days():
-			os.makedirs(base.pjoin(pjoin('tuoj', 'down'), day['name']))
-			tuoj_down(day)
-		return
-	for prob in conf.probs():
-		log.info(prob.route)
-		os.makedirs(base.pjoin(pjoin('tuoj', 'down'), prob.route))
-		for idx, case in enumerate(prob.sample_cases, start = 1):
-			shutil.copy(
-				base.pjoin(prob.path, 'down', str(case) + '.in'),
-				base.pjoin('tuoj', 'down', prob.route, str(case) + '.in')
-			)
-			shutil.copy(
-				base.pjoin(prob.path, 'down',str(case) + '.ans'),
-				base.pjoin('tuoj', 'down', prob.route, str(case) + '.ans')
-			)
-		base.run_r(base.dos2unix, base.pjoin(pjoin('tuoj', 'down', prob.route)))
-
-def loj_prob(conf):
-	global save_flag
-	headers = {
-		'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'
-	}
-	tool_conf = base.tool_conf[base.work]['default']
-	cookies = tool_conf['cookies']
-	pid = conf.get('pid', {}).get(base.work + '-default', 0)
-	host = tool_conf['main']
-	data = {
-		'title' : conf.tr('title'),
-		'description' : 'place holder',
-		'input_format' : 'place holder',
-		'output_format' : 'place holder',
-		'example' : 'place holder',
-		'limit_and_hint' : 'place holder',
-		'tags' : conf.get('tags', {}).get(base.work + '-default', [])
-	}
-	def post(url, data = None, files = None):
-		r = requests.post(
-			host + url,
-			headers = headers,
-			stream = True,
-			cookies = cookies,
-			data = data,
-			files = files
-		)
-		if not r.ok:
-			log.error(u'网站连接失败，错误代码%s，错误信息见`error.log`。' % r.status_code)
-			with open('error.log', 'a') as f:
-				f.write(u'运行时间：' + str(datetime.datetime.now()) + '\n')
-				f.write(u'url：' + r.url + '\n')
-				f.write(r.text)
-		return r
-	if pid == 0:
-		r = post('/problem/%d/edit' % pid, data)
-		pid = int(r.url.split('/')[-1])
-		conf.setdefault('pid', {})
-		conf['pid'][base.work + '-default'] = pid
-		save_flag = True
-	path = pjoin('statements', base.work, conf.route if conf.route != '' else conf['name']) + '.md'
-	data['description'] = open(path, 'rb').read()
-	post('/problem/%d/edit' % pid, data)
-	import zipfile, uuid
-	data_yml = {
-		'inputFile' : '#.in',
-		'outputFile' : '#.ans',
-		'subtasks' : [{
-			'score' : datum.score if conf.packed else 100 / len(conf.test_cases) * len(datum['cases']),
-			'type' : 'min' if conf.packed else 'sum',
-			'cases' : [str(c) for c in datum['cases']]
-		} for datum in conf.data]
-	}
-	if os.path.exists(pjoin(conf.path, 'data', 'chk', 'chk.cpp')):
-		data_yml['specialJudge'] = {
-			'language' : 'cpp17',
-			'fileName' : 'spj_cpp.cpp'
-		}
-	if conf['type'] == 'output':
-		data_yml['userOutput'] = '#.out'
-	open(pjoin(base.work, 'data', conf.route + '.yml'), 'wb').write(base.dump_formats['yaml'](data_yml))
-	def pack(z, path, fname):
-		id = str(uuid.uuid4()) + '.tmp'
-		shutil.copy(pjoin(path, fname), id)
-		time.sleep(0.1)
-		base.dos2unix(id)
-		z.write(id, fname)
-		os.remove(id)
-	with zipfile.ZipFile(pjoin(base.work, 'data', conf.route + '.zip'), 'w') as z:
-		for id in conf.test_cases:
-			pack(z, pjoin(conf.path, 'data'), id + '.in')
-			pack(z, pjoin(conf.path, 'data'), id + '.ans')
-		if os.path.exists(pjoin(conf.path, 'data', 'chk', 'chk.cpp')):
-			z.write(pjoin(conf.path, 'data', 'chk', 'chk.cpp'), 'spj_cpp.cpp')
-		if os.path.exists(pjoin(base.work, 'data', conf.route + '.yml')):
-			z.write(pjoin(base.work, 'data', conf.route + '.yml'), 'data.yml')
-	with zipfile.ZipFile(pjoin(base.work, 'down', conf.route + '.zip'), 'w') as z:
-		if os.path.exists(pjoin(conf.path, 'down')):
-			for name in os.listdir(pjoin(conf.path, 'down')):
-				pack(z, pjoin(conf.path, 'down'), name)
-	with zipfile.ZipFile(pjoin(base.work, 'resources', conf.route + '.zip'), 'w') as z:
-		try:
-			for name in os.listdir(pjoin(conf.path, 'resources')):
-				pack(z, pjoin(conf.path, 'resources'), name)
-		except Exception as e:
-			log.warning(u'没有找到资源文件。')
-	files = [
-		('testdata', ("data.zip", open(pjoin(base.work, 'data', conf.route + '.zip'), "rb"))),
-		('additional_file', ("down.zip", open(pjoin(base.work, 'down', conf.route + '.zip'), "rb")))
-	]
-	data = {
-		'type' : {'program' : 'traditional', 'output' : 'submit-answer', 'interactive' : 'interaction', 'hand' : 'hand'}[conf['type']]
-	}
-	if conf['type'] != 'output':
-		data['time_limit'] = int(conf.get('time limit', 0) * 1000)
-		data['memory_limit'] = int(conf.ml().MB)
-	post('/problem/%d/manage' % pid, data, files)
-	files = [
-		('images', ("resources.zip", open(pjoin(base.work, 'resources', conf.route + '.zip'), "rb")))
-	]
-	post('/problem/%d/upload_resource' % pid, files = files)
-
-def loj():
-	global save_flag
-	save_flag = False
-	syz_host = base.tool_conf.get(base.work, {}).get('default')
-	if not syz_host:
-		log.error(u'没有配置%s的地址。' % base.work)
-		if base.system == 'Windows':
-			log.info(u'在tuack的安装目录中找到conf.json。')
-		else:
-			log.info(u'在~/.tuack中找到conf.json。')
-		log.info(u'添加%s的相关字段，详见`https://git.thusaac.com/publish/tuack/wikis/导出题目`。' % base.work)
-		return
-	if not os.path.exists(base.work):
-		base.remkdir(base.work)
-	base.remkdir(pjoin(base.work, 'data'))
-	base.remkdir(pjoin(base.work, 'down'))
-	base.remkdir(pjoin(base.work, 'resources'))
-	if base.conf.folder == 'contest':
-		for day in base.days():
-			os.makedirs(base.pjoin(pjoin(base.work, 'data'), day.route))
-			os.makedirs(base.pjoin(pjoin(base.work, 'down'), day.route))
-			os.makedirs(base.pjoin(pjoin(base.work, 'resources'), day.route))
-	if base.do_render:
-		from . import ren
-		tmp = base.start_file
-		base.start_file = False
-		ren.Markdown(base.work).run()
-		base.start_file = tmp
-	else:
-		pass
-	for prob in base.probs():
-		loj_prob(prob)
-	if save_flag:
-		base.save_json(base.conf)
-		
-work_list = {
-	'lemon' : lemon,
-	'arbiter' : arbiter,
-	'arbiter-main' : arbiter_main,
-	'arbiter-down' : arbiter_down,
-	'tsinsen-oj' : tsinsen_oj,
-	'tuoj-down' : tuoj_down,
-	'loj' : loj,
-	'ipuoj' : loj
-}
-
-if __name__ == '__main__':
-	try:
-		if base.init():
-			for base.work in base.works:
-				base.run_exc(work_list[base.work])
-		else:
-			log.info(u'这个工具用于导出成其他类型的工程。')
-			log.info(u'支持的工作：%s' % ','.join(sorted(work_list.keys())))
-	except base.NoFileException as e:
-		log.error(e)
-		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+import platform
+from . import base
+from .base import log, pjoin
+import requests
+import traceback
+from requests_toolbelt.multipart.encoder import MultipartEncoder, MultipartEncoderMonitor
+
+def lemon(conf = None):
+	py_version = base.python_version[0]
+	if py_version == 2:
+		base.check_install('pyside')
+		from PySide import QtCore
+	if not conf:
+		if base.conf.folder == 'problem':
+			raise Exception('Can\'t dump a single problem to lemon, try to dump a day or a contest.')
+		base.remkdir('lemon')
+		if base.conf.folder == 'day':
+			lemon(base.conf)
+		else:
+			for day in base.days():
+				os.makedirs(base.pjoin('lemon', day.route))
+				lemon(day)
+		return
+	log.info(u'导出lemon工程：%s' % conf.route)
+	os.makedirs(base.pjoin('lemon', conf.route, 'data'))
+	os.makedirs(base.pjoin('lemon', conf.route, 'source'))
+	if py_version == 2:
+		jzp_magic = 0x20111127
+		zlib_magic = 0x185E
+		import zlib
+		obuff = QtCore.QByteArray()
+		ost = QtCore.QDataStream(obuff, QtCore.QIODevice.WriteOnly)
+		ost.writeQString(conf['name'])
+		probs = list(conf.probs())
+		ost.writeInt32(len(probs))
+		for prob in probs:
+			log.info(u'导出lemon题目：%s' % prob.route)
+			ost.writeQString(base.tr(prob['title']))
+			ost.writeQString(prob['name'])
+			ost.writeQString(prob['name'] + '.in')
+			ost.writeQString(prob['name'] + '.out')
+			ost.writeBool(False)
+			ost.writeBool(False)
+			ost.writeInt32(1 if prob['type'] == 'output' else 0)
+			ost.writeInt32(1)		# Judge Type TODO: What if there is spj (code = 4)
+			ost.writeQString('--ignore-space-change --text --brief')
+			ost.writeInt32(3)		# real precision (float number error bound)
+			ost.writeQString('')	# spj route TODO: What if there is spj
+			ost.writeInt32(len([i for i in prob.get('compile', {}) if i in {'cpp', 'c', 'pas'}]))
+			for key, val in prob.get('compile', {}).items():
+				try:
+					ost.writeQString({
+						'cpp' : 'g++',
+						'c' : 'gcc',
+						'pas' : 'fpc'
+					}[key])
+					ost.writeQString(val)
+				except:
+					pass
+			ost.writeQString('out')
+			if prob.packed:
+				ost.writeInt32(len(prob['data']))
+				for datum in prob['data']:
+					ost.writeInt32(datum['score'])
+					ost.writeInt32(datum.get('time limit', prob.get('time limit', 0)) * 1000)
+					ost.writeInt32(base.Memory(datum.get('memory limit', prob.get('memory limit', '0 B'))).MB)
+					tc = datum['cases']
+					ost.writeInt32(len(tc))
+					for c in tc:
+						ost.writeQString(base.pjoin(prob['name'], str(c) + '.in'))
+					ost.writeInt32(len(tc))
+					for c in tc:
+						ost.writeQString(base.pjoin(prob['name'], str(c) + '.ans'))
+			else:
+				score = (100. / len(prob.test_cases) if len(prob.test_cases) > 0 else 0.)
+				if 100 % len(prob.test_cases) != 0:
+					log.warning('测试点个数不是100的约数，总分将不是整百。')
+				ost.writeInt32(len(prob.test_cases))
+				for c in prob.test_cases:
+					ost.writeInt32(int(score + .5))
+					ost.writeInt32(int(prob['time limit'] * 1000 + .5))
+					ost.writeInt32(int(prob.memory_limit().MB + .5))
+					ost.writeInt32(1)
+					ost.writeQString(base.pjoin(prob['name'], str(c) + '.in'))
+					ost.writeInt32(1)
+					ost.writeQString(base.pjoin(prob['name'], str(c) + '.ans'))
+			
+			sp = list(prob.route.split('/'))
+			target = ['lemon'] + sp[:-1] + ['data', sp[-1]]
+			shutil.copytree(base.pjoin(prob.path, 'data'), base.pjoin(*target))
+
+		ss = lambda s : str(s) if py_version == 2 else s
+		compressed = QtCore.QByteArray(zlib.compress(ss(obuff)))
+		obuff = QtCore.QByteArray()
+		ost = QtCore.QDataStream(obuff, QtCore.QIODevice.WriteOnly)
+		ost.writeUInt32(zlib_magic)
+		ost.writeRawData(ss(compressed))
+		file_ = QtCore.QFile(base.pjoin('lemon', conf.route, conf['name'] + '.cdf'))
+		file_.open(QtCore.QIODevice.WriteOnly)
+		ofs = QtCore.QDataStream(file_)
+		ofs.writeUInt32(jzp_magic)
+		ofs.writeUInt16(QtCore.qChecksum(ss(obuff), len(obuff)))
+		ofs.writeUInt32(len(obuff))
+		ofs.writeRawData(ss(obuff))
+		file_.close()
+	else:
+		probs = list(conf.probs())
+		tasks = []
+		for prob in probs:
+			log.info(u'导出lemon题目：%s' % prob.route)
+			if prob.packed:
+				cases = [
+					{
+						"fullScore": int(datum['score'] + .5),
+						"timeLimit": int(datum.get('time limit', prob.get('time limit', 0)) * 1000 + .5),
+						"memoryLimit": int(base.Memory(datum.get('memory limit', prob.get('memory limit', '0 B'))).MB + .5),
+						"inputFiles": [
+							base.pjoin(prob['name'], str(c) + '.in') \
+							for c in datum['cases']
+						],
+						"outputFiles": [
+							base.pjoin(prob['name'], str(c) + '.ans') \
+							for c in datum['cases']
+						]
+					} for datum in prob['data']
+				]
+			else:
+				score = (100. / len(prob.test_cases) if len(prob.test_cases) > 0 else 0.)
+				if 100 % len(prob.test_cases) != 0:
+					log.warning('测试点个数不是100的约数，总分将不是整百。')
+				cases = [
+					{
+						"fullScore": int(score + .5),
+						"timeLimit": int(prob['time limit'] * 1000 + .5),
+						"memoryLimit": int(prob.memory_limit().MB + .5),
+						"inputFiles": [
+							base.pjoin(prob['name'], str(c) + '.in')
+						],
+						"outputFiles": [
+							base.pjoin(prob['name'], str(c) + '.ans')
+						]
+					} for c in prob.test_cases
+				]
+			tasks.append({
+				'answerFileExtension' : 'out',
+				"comparisonMode": 1,	#TODO: What if there is spj (code = 4)
+				"diffArguments": "--ignore-space-change --text --brief",
+				"inputFileName": prob['name'] + '.in',
+				"outputFileName": prob['name'] + '.out',
+				"problemTitle": base.tr(prob['title']),
+				"realPrecision": 3,		#float number error bound
+				"sourceFileName": prob['name'],
+				"specialJudge": "",		#TODO: What if there is spj
+				"standardInputCheck": False,
+				"standardOutputCheck": False,
+				"subFolderCheck": False,
+				"taskType": 1 if prob['type'] == 'output' else 0,
+				"compilerConfiguration": {
+					{
+						'cpp' : 'g++',
+						'c' : 'gcc',
+						'pas' : 'fpc',
+						'py' : 'python',
+						'java' : 'javac'
+					}[i] : 'default' for i in prob.get('compile', {}) if i in {'cpp', 'c', 'pas', 'py', 'java'}
+				},
+				"testCases" : cases
+			})
+			sp = list(prob.route.split('/'))
+			target = ['lemon'] + sp[:-1] + ['data', sp[-1]]
+			shutil.copytree(base.pjoin(prob.path, 'data'), base.pjoin(*target))
+		open(base.pjoin('lemon', conf.route, conf['name'] + '.cdf'), 'wb').write(json.dumps({
+			"contestTitle" : conf['name'],
+			"contestants" : [],
+			"tasks" : tasks
+		}).encode('utf-8'))
+	
+	base.run_r(base.unix2dos, base.pjoin('lemon', conf.route, 'data'))
+	
+	if base.do_zip:
+		import zipfile
+		with zipfile.ZipFile(base.pjoin('lemon', conf.route) + '.zip', 'w') as z:
+			base.run_r(lambda path : z.write(path), base.pjoin('lemon', conf.route))
+	log.warning(u'目前SPJ的支持暂时还没有实现，有需要请手工配置。')
+	log.warning(u'目前lemon的编译选项是写在注册表里的，暂时没有实现该功能，请手工配置。')
+
+def arbiter_main(conf = None,daynum = 0):
+	def arbiter_info(info, filename):
+		with open(filename,'wb') as ofile:
+			for key, val in info.items():
+				ofile.write(('%s%s\n' % (key, val)).encode('utf-8'))
+	if not conf:
+		log.info('makedirs')
+		if not os.path.exists('arbiter'):
+			base.remkdir('arbiter')
+		base.remkdir(pjoin('arbiter', 'main'))
+		os.makedirs(base.pjoin('arbiter', 'main','data'))
+		os.makedirs(base.pjoin('arbiter', 'main','final'))
+		os.makedirs(base.pjoin('arbiter', 'main','players'))
+		os.makedirs(base.pjoin('arbiter', 'main','result'))
+		os.makedirs(base.pjoin('arbiter', 'main','filter'))
+		os.makedirs(base.pjoin('arbiter', 'main','tmp'))
+		if base.conf.folder == 'problem':
+			raise Exception('Can\'t dump a single problem to arbiter, try to dump a day or a contest.')
+		if base.conf.folder == 'day':
+			arbiter(base.days())
+		else:
+			for idx, day in enumerate(base.days(), start = 1):
+				os.makedirs(base.pjoin('arbiter', 'main','players','day%d' % idx))
+				os.makedirs(base.pjoin('arbiter', 'main','result','day%d' % idx))
+				arbiter_main(day,idx)
+			log.info('dos2unix')
+			base.run_r(base.dos2unix, base.pjoin('arbiter', 'main', 'data'))
+			shutil.copytree(base.pjoin('arbiter', 'main','data'),base.pjoin('arbiter', 'main','evaldata'))	#这里也不能直接copy，见下面的处理方式
+			cfg = {}
+			cfg['NAME='] = base.conf['name']
+			cfg['DAYNUM='] = idx
+			cfg['ENV='] = 'env.info'
+			cfg['PLAYER='] = 'player.info'
+			cfg['TEAM='] = 'team.info'
+			cfg['MISC='] = 'misc.info'
+			arbiter_info(cfg,base.pjoin('arbiter', 'main','setup.cfg'))
+			team = {}
+			arbiter_info(team,base.pjoin('arbiter', 'main','team.info'))
+			'''arbiter_info(userlist,base.pjoin('arbiter','player.info'))'''
+		return
+	dayinfo = {}
+	dayinfo['NAME='] = u'第'+str(daynum)+u'场'+u'--机试'
+	dayinfo['PLAYERDIR='] = ''
+	dayinfo['CASEDIR='] = ''
+	dayinfo['BASESCORE='] = 0
+	dayinfo['TASKNUM='] = len(conf['subdir'])
+	arbiter_info(dayinfo,base.pjoin('arbiter', 'main', 'day%d.info' % daynum))
+	for probnum, prob in enumerate(conf.sub, start = 1):
+		log.info(prob['name'])
+		probinfo = {}
+		probinfo['TITLE='] = ''
+		probinfo['NAME='] = prob['name']
+		probinfo['RUN='] = ''
+		probinfo['INFILESUFFIX='] = 'in'
+		probinfo['ANSFILESUFFIX='] = 'ans'
+		probinfo['PLUG='] = prob['name']+'_e'
+		if prob['type'] == 'program':
+			probinfo['TYPE='] = 'SOURCE'
+		else:
+			log.warning(u'暂时只支持非交互式程序题。')
+		probinfo['LIMIT='] = prob['time limit']
+		probinfo['MEMLIMITS='] = int(prob.memory_limit().MB)
+		probinfo['SAMPLES='] = len(prob.test_cases)
+		score_per_case = 100 // len(prob.test_cases)
+		if not prob.packed and score_per_case * len(prob.test_cases) != 100:
+			log.warning(u'测试点数量不是100的约数，分数无法均分为整数。')
+		probinfo['CCL=c@gcc'] = ' -o %o %i ' + prob['compile'].get('c', '')
+		probinfo['CCL=cpp@g++'] = ' -o %o %i ' + prob['compile'].get('cpp', '')
+		probinfo['CCL=pas@fpc'] = ' %i ' + prob['compile'].get('pas', '')
+		idx = 0
+		for datum in prob.data:
+			if prob.packed and len(datum['cases']) > 1:
+				log.warning(u'Arbiter不支持打包评测，将把该包得分均分给包中各测试点，无法整除时总分将不正确。')
+			for case in datum['cases']:
+			#for idx, case in enumerate(prob.test_cases, start = 1):
+				idx += 1
+				'''print('copyfile %s'%base.pjoin(prob.path,'data',case+'.in'))'''
+				shutil.copy(
+					base.pjoin(prob.path,'data',str(case)+'.in'),
+					base.pjoin('arbiter', 'main','data',prob['name']+str(idx)+'.in')
+				)
+				'''print('copyfile %s'%base.pjoin(prob.path,'data',case+'.ans'))'''
+				shutil.copy(
+					base.pjoin(prob.path,'data',str(case)+'.ans'),
+					base.pjoin('arbiter', 'main','data',prob['name']+str(idx)+'.ans')
+				)
+				if prob.packed:
+					probinfo['MARK='+str(idx)+'@'] = str(int(datum['score'] / len(datum['cases'])))
+				else:
+					probinfo['MARK='+str(idx)+'@'] = str(int(score_per_case))
+		'''for idx, userdir in enumerate(prob['users'],start = 1):
+			for idx2, code in enumerate(prob['users'][userdir],start = 1):
+				dirname = prob['name']+'-'+str(idx)+str(idx2)
+				codename = userdir + code
+				tmplist = prob['users'][userdir][code].split('/')
+				codedir = base.pjoin(prob.path,*tmplist)
+				os.makedirs(base.pjoin('arbiter','players',conf['name'],dirname,prob['name']))
+				shutil.copy(codedir,base.pjoin('arbiter','players',conf['name'],dirname,prob['name']))
+				userlist[dirname + '@'] =  codename'''
+		shutil.copy(base.pjoin(base.path,'sample','arbiter_e.sample'),base.pjoin('arbiter', 'main','filter',prob['name']+'_e'))
+		arbiter_info(probinfo,base.pjoin('arbiter', 'main','task'+str(daynum)+'_'+str(probnum)+'.info'))
+
+def arbiter_down(conf = None):
+	if not conf:
+		conf = base.conf
+		if not os.path.exists('arbiter'):
+			base.remkdir('arbiter')
+		base.remkdir(pjoin('arbiter', 'down'))
+	if conf.folder == 'problem':
+		raise Exception('Can\'t dump a single problem to arbiter, try to dump a day or a contest.')
+	if conf.folder == 'contest':
+		for idx, day in enumerate(base.days(), start = 1):
+			os.makedirs(base.pjoin(pjoin('arbiter', 'down'), day['name']))
+			arbiter_down(day)
+		return
+	for prob in conf.probs():
+		log.info(prob.route)
+		os.makedirs(base.pjoin(pjoin('arbiter', 'down'), prob.route))
+		vis = set()
+		for idx, case in enumerate(prob.sample_cases, start = 1):
+			for suf in ('.in', '.ans'):
+				s_name = base.pjoin(prob.path, 'down', str(case) + suf)
+				t_name = base.pjoin('arbiter', 'down', prob.route, prob['name'] + str(idx) + suf)
+				base.shutil_copy(s_name, t_name)
+				vis.add(str(case) + suf)
+		for fname in os.listdir(base.pjoin(prob.path, 'down')):
+			if fname not in vis:
+				log.info(f"找到了不在down列表中的文件{fname}")
+				base.shutil_copy(
+					base.pjoin(prob.path, 'down', fname),
+					base.pjoin('arbiter', 'down', prob.route, fname)
+				)
+	log.info('dos2unix')
+	base.run_r(base.dos2unix, base.pjoin(pjoin('arbiter', 'down', conf.route)))
+
+def arbiter():
+	base.remkdir('arbiter')
+	arbiter_main()
+	arbiter_down()
+
+def tsinsen_oj():
+	import random
+	if type(base.conf) != base.Problem:
+		log.error(u'只能转换一道题目，请到相应题目目录下运行')
+		return
+	hash_ch = list(map(
+		chr,
+		[ord('a') + i for i in range(26)] + \
+		[ord('A') + i for i in range(26)] + \
+		[ord('0') + i for i in range(10)]
+	))
+	hash = lambda l = 10 : ''.join([hash_ch[random.randint(0, len(hash_ch) - 1)] for i in range(l)])
+	if not os.path.exists('tsinsen-oj'):
+		os.makedirs('tsinsen-oj')
+	for day in base.days():
+		p = base.pjoin('tsinsen-oj', day.route)
+		if not os.path.exists(p):
+			os.makedirs(p)
+	for prob in base.probs():
+		p = base.pjoin('tsinsen-oj', prob.route)
+		if not os.path.exists(p):
+			os.makedirs(p)
+		if os.path.exists(base.pjoin(prob.path, 'down')):
+			with zipfile.ZipFile(base.pjoin('tsinsen-oj', prob.route, 'down.zip'), 'w') as z:
+				base.run_r(lambda path : z.write(path), base.pjoin(prob.path, 'down'))
+			prob.tsinsen_down = hash(8)
+		else:
+			prob.tsinsen_down = None
+		files = {}
+		path = base.pjoin(prob.path, 'resources')
+		if os.path.exists(path):
+			base.run_r(lambda p : files.__setitem__(p[len(path) + 1:], hash(8)), path)
+		prob.tsinsen_files = files
+	if base.do_render:
+		from . import ren
+		tmp = base.start_file
+		base.start_file = False
+		ren.Html('tsinsen-oj').run()
+		base.start_file = tmp
+	else:
+		log.warning(u'如果你使用了文件，不重新渲染题面会导致tsinsen的文件失效。')
+	
+	read_file = lambda path : open(path, 'rb').read().decode('utf-8')
+	
+	Title = lambda : prob.tr('title')
+	CheckPoint = lambda : prob['key words'] if 'key words' in prob else ''
+	TestMethod = lambda : 'DEFAULT'
+	InputFileName = lambda : ''
+	OutputFileName = lambda : ''
+	TimeLimit = lambda : '%.1fs' % prob['time limit']
+	MemoryLimit = lambda : '%.1fMB' % prob.memory_limit().MB
+	
+	def Checkers():
+		path = base.pjoin('data', 'chk', 'chk.cpp')
+		if os.path.exists(path):
+			return open(path, 'rb').read().decode('utf-8')
+		else:
+			return '\n'
+	def Description():
+		path = pjoin('statements', 'tsinsen-oj', prob.route if prob.route != '' else prob['name']) + '.html'
+		if not os.path.exists(path):
+			log.warning(u'找不到题面，你可能需要自己手工添加题面。')
+			return ''
+		header = u'<p>下载目录：<img src="/RequireFile.do?fid=%s" alt="另存为图片下载" />（另存为图片下载）</p>\n' % prob.tsinsen_down
+		return header + read_file(path)
+	def Solution():
+		for user, codes in prob['users'].items():
+			for name, path in codes.items():
+				if prob.expect(user, name, 100):
+					return read_file(path['path'])
+		for user, codes in prob['users'].items():
+			for name, path in codes.items():
+				return read_file(path)
+		return ''
+	def add_shell(name, func):
+		h = hash()
+		ret = '%s=\n' % name
+		ret += '======================%s\n' % h
+		res = func()
+		if not res.endswith('\n'):
+			res += '\n'
+		ret += res
+		ret += '======================%s\n' % h
+		return ret.encode('utf-8')
+	def to_base64(path):
+		import base64
+		s = base64.b64encode(open(path, 'rb').read()).decode('utf-8')
+		return '\n'.join(s[pos:pos+76] for pos in range(0, len(s), 76))
+	tokens = [
+		'Title', 'CheckPoint', 'Checkers', 'TestMethod', 'Description',
+		'InputFileName', 'OutputFileName', 'Solution', 'TimeLimit', 'MemoryLimit'
+	]
+	for prob in base.probs():
+		result_file = base.pjoin('tsinsen-oj', prob.route) + '.txt'
+		with open(result_file, 'wb') as f:
+			for token in tokens:
+				f.write(add_shell(token, eval(token)))
+			if prob.packed:
+				log.warning(u'清橙OJ不支持打包评测和指定测试点分值，直接将所有测试点视为相同。')
+			for datum in prob.test_cases:
+				f.write(add_shell('InData', lambda : read_file(base.pjoin('data', datum + '.in'))))
+				f.write(add_shell('OutData', lambda : read_file(base.pjoin('data', datum + '.ans'))))
+			if prob.tsinsen_down:
+				f.write(add_shell('FileName', lambda : 'down.zip'))
+				f.write(add_shell('File(%s)' % prob.tsinsen_down, lambda : to_base64(base.pjoin('tsinsen-oj', prob.route, 'down.zip'))))
+			for key, val in prob.tsinsen_files.items():
+				f.write(add_shell('FileName', lambda : key.replace('/', '-').replace('\\', '-')))
+				f.write(add_shell('File(%s)' % val, lambda : to_base64(base.pjoin(prob.path, 'resources', key))))
+		if base.start_file:
+			base.xopen_file(result_file)
+
+def tuoj_down(conf = None):
+	if not conf:
+		conf = base.conf
+		if not os.path.exists('tuoj'):
+			base.remkdir('tuoj')
+		base.remkdir(pjoin('tuoj', 'down'))
+	if conf.folder == 'contest':
+		for day in base.days():
+			os.makedirs(base.pjoin(pjoin('tuoj', 'down'), day['name']))
+			tuoj_down(day)
+		return
+	for prob in conf.probs():
+		log.info(prob.route)
+		os.makedirs(base.pjoin(pjoin('tuoj', 'down'), prob.route))
+		for idx, case in enumerate(prob.sample_cases, start = 1):
+			shutil.copy(
+				base.pjoin(prob.path, 'down', str(case) + '.in'),
+				base.pjoin('tuoj', 'down', prob.route, str(case) + '.in')
+			)
+			shutil.copy(
+				base.pjoin(prob.path, 'down',str(case) + '.ans'),
+				base.pjoin('tuoj', 'down', prob.route, str(case) + '.ans')
+			)
+		base.run_r(base.dos2unix, base.pjoin(pjoin('tuoj', 'down', prob.route)))
+
+def loj_prob(conf, pre = False):
+	if not pre and len(conf.get('pre', [])) > 0:
+		loj_prob(conf, True)
+	global save_flag
+	headers = {
+		'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'
+	}
+	tool_conf = base.tool_conf[base.work]['default']
+	cookies = tool_conf['cookies']
+	pid_key = 'pid' if not pre else 'pid-pre'
+	tag_key = 'tags' if not pre else 'tags-pre'
+	pid = conf.get(pid_key, {}).get(base.work + '-default', 0)
+	host = tool_conf['main']
+	data = {
+		'file_name' : conf['name'],
+		'title' : conf.tr('title') + (u'（预测试）' if pre else ''),
+		'description' : 'place holder',
+		'input_format' : 'place holder',
+		'output_format' : 'place holder',
+		'example' : 'place holder',
+		'limit_and_hint' : 'place holder',
+		'tags' : conf.get(tag_key, {}).get(base.work + '-default', [])
+	}
+	def file_callback(m):
+		p = (m.bytes_read / m.len) * 100
+		print('上传 %.1f%%（%.1f KiB/%.1f KiB）    ' % (p, m.bytes_read / 1024, m.len / 1024), end = '\r')
+		sys.stdout.flush()
+	def post(url, data = None, files = None):
+		if files:
+			d = dict(files)
+			if not data:
+				data = {}
+			for k, v in data.items():
+				d[k] = str(v)
+			d = MultipartEncoder(d)
+			d = MultipartEncoderMonitor(d, file_callback)
+			h = headers.copy()
+			h['Content-Type'] = d.content_type
+		else:
+			d = data
+			h = headers
+		r = requests.post(
+			host + url,
+			headers = h,
+			stream = True,
+			cookies = cookies,
+			data = d
+		)
+		if not r.ok:
+			log.error(u'网站连接失败，错误代码%s，错误信息见`error.log`。' % r.status_code)
+			with open('error.log', 'a') as f:
+				f.write(u'运行时间：' + str(datetime.datetime.now()) + '\n')
+				f.write(u'url：' + r.url + '\n')
+				f.write(r.text)
+		return r
+	if pid == 0:
+		r = post('/problem/%d/edit' % pid, data)
+		pid = int(r.url.split('/')[-1])
+		conf.setdefault(pid_key, {})
+		conf[pid_key][base.work + '-default'] = pid
+		save_flag = True
+	path = pjoin('statements', base.work, conf.route if conf.route != '' else conf['name']) + '.md'
+	data['description'] = open(path, 'rb').read()
+	post('/problem/%d/edit' % pid, data)
+	import zipfile, uuid
+	conf_data = conf.data if not pre else conf.pre
+	packed = conf.packed if not pre else conf.packed_pre
+	cases = conf.test_cases if not pre else conf.pre_cases
+	data_yml = {
+		'inputFile' : '#.in',
+		'outputFile' : '#.ans',
+		'subtasks' : [{
+			'score' : datum.score if packed else 100 / len(cases) * len(datum['cases']),
+			'type' : 'min' if packed else 'sum',
+			'cases' : [str(c) for c in datum['cases']]
+		} for datum in conf_data]
+	}
+	if os.path.exists(pjoin(conf.path, 'data', 'chk', 'chk.cpp')):
+		data_yml['specialJudge'] = {
+			'language' : 'cpp17',
+			'fileName' : 'spj_cpp.cpp'
+		}
+	if conf['type'] == 'output':
+		data_yml['userOutput'] = (conf['name'] if conf.get('file io') else '') + '#.out'
+	if conf.get('extra'):
+		files = [{'name' : exname, 'dest' : exname} for exname in conf['extra']]
+		data_yml['extraSourceFiles'] = [
+			{'language' : lan, 'files' : files} \
+			for lan in ['cpp', 'c', 'cpp11', 'cpp17']
+		]
+	data_path = 'data' if not pre else 'pre'
+	open(pjoin(base.work, data_path, conf.route + '.yml'), 'wb').write(base.dump_formats['yaml'](data_yml))
+	def pack(z, path, fname, force_file = False):
+		full_path = pjoin(path, fname)
+		print(u"打包文件`%s`  " % full_path, end = '\r')
+		sys.stdout.flush()
+		if os.path.isdir(full_path):
+			if not force_file:
+				for sub in os.listdir(full_path):
+					pack(z, path, pjoin(fname, sub))
+				return
+			else:
+				log.warning(u'支持版本的`%s`不能是文件夹，用空文件代替。' % pjoin)
+				id = str(uuid.uuid4()) + '.tmp'
+				open(id, 'w')
+		else:
+			id = str(uuid.uuid4()) + '.tmp'
+			base.shutil_copy(full_path, id)
+		time.sleep(0.1)
+		base.dos2unix(id, full_path)
+		z.write(id, fname)
+		os.remove(id)
+	data_path = 'data' if not pre else 'pre'
+	with zipfile.ZipFile(pjoin(base.work, data_path, conf.route + '.zip'), 'w') as z:
+		for id in (conf.test_cases if not pre else conf.pre_cases):
+			pack(z, pjoin(conf.path, data_path), id + '.in', force_file = True)
+			pack(z, pjoin(conf.path, data_path), id + '.ans', force_file = True)
+		if os.path.exists(pjoin(conf.path, 'data', 'chk', 'chk.cpp')):
+			z.write(pjoin(conf.path, 'data', 'chk', 'chk.cpp'), 'spj_cpp.cpp')
+		if os.path.exists(pjoin(base.work, data_path, conf.route + '.yml')):
+			z.write(pjoin(base.work, data_path, conf.route + '.yml'), 'data.yml')
+		if conf.get('extra'):
+			for exname in conf['extra']:
+				z.write(pjoin(conf.path, 'extra', exname), exname)
+	files = [
+		('testdata', ("data.zip", open(pjoin(base.work, data_path, conf.route + '.zip'), "rb"))),
+	]
+	with zipfile.ZipFile(pjoin(base.work, 'resources', conf.route + '.zip'), 'w') as z:
+		try:
+			for name in os.listdir(pjoin(conf.path, 'resources')):
+				pack(z, pjoin(conf.path, 'resources'), name)
+		except Exception as e:
+			log.info(u'没有找到资源文件。')
+	if os.path.exists(pjoin(conf.path, 'down')) and len(list(os.listdir(pjoin(conf.path, 'down')))) > 0:
+		with zipfile.ZipFile(pjoin(base.work, 'down', conf.route + '.zip'), 'w') as z:
+			if conf['type'] == 'output':
+				for id in conf.test_cases:
+					pack(z, conf.path, pjoin('data', id + '.in'))
+				for name in os.listdir(pjoin(conf.path, 'down')):
+					pack(z, conf.path, pjoin('down', name))
+			else:
+				for name in os.listdir(pjoin(conf.path, 'down')):
+					pack(z, pjoin(conf.path, 'down'), name)
+		files.append(('additional_file', ("down.zip", open(pjoin(base.work, 'down', conf.route + '.zip'), "rb"))))
+	data = {
+		'type' : {'program' : 'traditional', 'output' : 'submit-answer', 'interactive' : 'interaction', 'hand' : 'hand'}.get(conf['type'], conf['type'])
+	}
+	if conf['type'] != 'output':
+		data['time_limit'] = int(conf.get('time limit', 0) * 1000)
+		data['memory_limit'] = int(conf.ml().MB)
+	if conf.get('file io'):
+		data['io_method'] = 'file-io'
+		data['file_io_input_name'] = conf.get('input_table', {}).get('zh-cn', conf['name'] + '.in')
+		data['file_io_output_name'] = conf.get('output_table', {}).get('zh-cn', conf['name'] + '.out')
+	post('/problem/%d/manage' % pid, data, files)
+	files = [
+		('images', ("resources.zip", open(pjoin(base.work, 'resources', conf.route + '.zip'), "rb")))
+	]
+	post('/problem/%d/upload_resource' % pid, files = files)
+
+def loj():
+	global save_flag
+	save_flag = False
+	syz_host = base.tool_conf.get(base.work, {}).get('default')
+	if not syz_host:
+		log.error(u'没有配置%s的地址。' % base.work)
+		if base.system == 'Windows':
+			log.info(u'在tuack的安装目录中找到conf.json。')
+		else:
+			log.info(u'在~/.tuack中找到conf.json。')
+		log.info(u'添加%s的相关字段，详见`https://git.thusaac.com/publish/tuack/wikis/导出题目`。' % base.work)
+		return
+	if not os.path.exists(base.work):
+		base.remkdir(base.work)
+	base.remkdir(pjoin(base.work, 'data'))
+	base.remkdir(pjoin(base.work, 'pre'))
+	base.remkdir(pjoin(base.work, 'down'))
+	base.remkdir(pjoin(base.work, 'resources'))
+	if base.conf.folder == 'contest':
+		for day in base.days():
+			os.makedirs(base.pjoin(pjoin(base.work, 'data'), day.route))
+			os.makedirs(base.pjoin(pjoin(base.work, 'down'), day.route))
+			os.makedirs(base.pjoin(pjoin(base.work, 'pre'), day.route))
+			os.makedirs(base.pjoin(pjoin(base.work, 'resources'), day.route))
+	if base.do_render:
+		from . import ren
+		tmp = base.start_file
+		base.start_file = False
+		ren.Markdown(base.work).run()
+		base.start_file = tmp
+	else:
+		pass
+	for prob in base.probs():
+		try:
+			loj_prob(prob)
+		except Exception as e:
+			traceback.print_exc()
+			log.error(u'输出题目`%s`时发生错误`%s`，具体信息如上所示。' % (prob['name'], e))
+	if save_flag:
+		base.save_json(base.conf)
+		
+work_list = {
+	'lemon' : lemon,
+	'arbiter' : arbiter,
+	'arbiter-main' : arbiter_main,
+	'arbiter-down' : arbiter_down,
+	'tsinsen-oj' : tsinsen_oj,
+	'tuoj-down' : tuoj_down,
+	'loj' : loj,
+	'ipuoj' : loj
+}
+
+if __name__ == '__main__':
+	try:
+		if base.init():
+			for base.work in base.works:
+				base.run_exc(work_list[base.work])
+		else:
+			log.info(u'这个工具用于导出成其他类型的工程。')
+			log.info(u'支持的工作：%s' % ','.join(sorted(work_list.keys())))
+	except base.NoFileException as e:
+		log.error(e)
+		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
```

### Comparing `tuack-0.1.4.9.2/tuack/gen.py` & `tuack-0.1.5/tuack/gen.py`

 * *Ordering differences only*

 * *Files 12% similar despite different names*

```diff
@@ -1,386 +1,386 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-from . import num2chinese
-import platform
-from . import base
-from .base import log, pjoin
-
-def find_all_data(kind, folder, key, conf = None):
-	if not conf:
-		conf = base.conf
-	def find_data(path = ''):
-		full_path = pjoin(prob.path, folder, path)
-		for f in os.listdir(full_path):
-			if os.path.isfile(pjoin(full_path, f)):
-				if not f.endswith('.in'):
-					continue
-				fans = pjoin(full_path, f[:-3]) + '.ans'
-				if not os.path.exists(fans) or not os.path.isfile(fans):
-					continue
-				name = base.rjoin(path, f[:-3])
-				if name not in new_data and name not in exist_data:
-					new_data.add(name)
-			else:
-				find_data(base.rjoin(path, f))
-	def parse(data):
-		tmp = base.sorter()(map(str, list(data)))
-		ret = []
-		for i in tmp:
-			try:
-				ret.append(int(i))
-			except Exception as e:
-				ret.append(i)
-		return ret
-	for prob in conf.probs(no_repeat = True):
-		log.info(u'在题目`%s`下搜索%s数据。' % (prob.route, key))
-		is_lfs = os.path.exists(pjoin(prob.path, '.gitattributes'))
-		new_data = set()
-		exist_data = set(map(str, prob.__getattribute__(key)))
-		try:
-			find_data()
-		except Exception as e:
-			log.warning(e)
-		new_data = parse(new_data)
-		for datum in new_data:
-			log.info(u'发现新数据`%s`。' % (pjoin(prob.path, folder, str(datum))))
-		if not is_lfs:
-			for tdata in (exist_data, new_data):
-				for datum in tdata:
-					for suf in ('.in', '.out', '.ans'):
-						fname = pjoin(prob.path, folder, str(datum) + suf)
-						if os.path.exists(fname) and os.path.getsize(fname) >= 1024 * 1024:
-							log.warning(u'题目`%s`下%s数据达到了1MiB，建议在该题下使用`python tuack.gen lfs`。' % (prob.route, key))
-							break
-					else:
-						continue
-					break
-				else:
-					continue
-				break
-		prob.__getattribute__(key).__iadd__(new_data)
-		if kind not in prob:
-			prob[kind] = []
-		if len(new_data) > 0:
-			prob[kind].append({'cases' : new_data})
-		base.save_json(prob)
-	
-def find_all_code():
-	def find_code(user, path):
-		full_path = pjoin(prob.path, user, path)
-		for f in os.listdir(full_path):
-			if base.user_skip.match(f):
-				continue
-			if os.path.isfile(pjoin(full_path, f)):
-				for key in base.compilers:
-					if not f.endswith('.' + key):
-						continue
-					code_path = base.rjoin(user, path, f).replace('//', '/')
-					if code_path not in exist_code:
-						prob['users'][user][base.rjoin(path, f).replace('//', '/')] = {
-							'path' : code_path,
-							'expected' : '== 100' if 'std' in code_path or prob['name'] in code_path else []
-						}
-						log.info(u'发现新源代码`%s`。' % code_path)
-					break
-			else:
-				find_code(user, base.rjoin(path, f))
-
-	for prob in base.probs(no_repeat = True):
-		if prob['type'] == 'output':
-			log.info(u'题目`%s`是提交答案题，跳过。' % prob.route)
-			continue
-		log.info(u'在题目`%s`下搜索源代码。' % prob.route)
-		if 'users' not in prob:
-			prob['users'] = {}
-		exist_code = set()
-		for user, algos in prob['users'].items():
-			for algo, path in algos.items():
-				exist_code.add((path['path'] if type(path) == dict else path).replace('//', '/'))
-		for f in os.listdir(prob.path):
-			if base.user_skip.match(f) or os.path.isfile(pjoin(prob.path, f)):
-				continue
-			if f not in prob['users']:
-				prob['users'][f] = {}
-			find_code(f, '')
-			if len(prob['users'][f]) == 0:
-				prob['users'].pop(f)
-		base.save_json(prob)
-
-def sample_copy(src, tgt = None, path = '', base_path = 'sample'):
-	if not tgt:
-		tgt = src
-	full_tgt = pjoin(path, tgt)
-	if os.path.exists(full_tgt) and not os.path.isfile(full_tgt):
-		full_tgt = pjoin(full_tgt, src)
-	if not os.path.exists(full_tgt):
-		log.info(u'生成文件`%s`' % full_tgt)
-		base.copy(
-			pjoin(base.path, base_path),
-			src,
-			full_tgt
-		)
-
-def new_dir(folder, args = None):
-	if not args:
-		args = base.args
-	if len(args) == 0:
-		dirs = ['.']
-	else:
-		if not base.conf:
-			log.error(u'当前文件夹下没有找到合法的`conf.json`文件。')
-			log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
-			return
-		if folder == 'contest':
-			log.error(u'文件夹层次错误：比赛工程不能放在其他工程中。')
-			return
-		if folder == 'day' and base.conf.folder != 'contest':
-			log.error(u'文件夹层次错误：比赛日工程只能放在比赛工程中。')
-			return
-		if (folder == 'problem' or folder == 'empty') and base.conf.folder != 'day':
-			log.error(u'文件夹层次错误：题目工程只能放在比赛日工程中。')
-			return
-		dirs = args
-	for path in dirs:
-		if not os.path.exists(path):
-			os.makedirs(path)
-		if path != '.' and path in base.conf['subdir']:
-			log.warning(u'`%s`已经在工程中了，跳过它的建立。' % path)
-			log.info(u'如果需要强制建立，需要将其从`conf.yaml`中移除。')
-			continue
-		copy = lambda src, tgt = None: sample_copy(src, tgt, path)
-		def copy_conf(inp):
-			if base.dump_format != 'json':
-				open(pjoin(path, 'conf.' + base.dump_format), 'wb').write(
-					base.dump_formats[base.dump_format](
-						json.loads(open(pjoin(base.path, 'sample', inp), 'rb').read().decode('utf-8'))
-					)
-				)
-			else:
-				copy(inp, 'conf.json')
-		copy(folder + '.gitignore', '.gitignore')
-		copy_conf(folder + '.json')
-		if folder == 'problem' or folder == 'empty':
-			if base.git_lfs:
-				copy(folder + '.gitattributes', '.gitattributes')
-			else:
-				log.info(u'现在不默认用git-lfs，如需，用`python -m tuack.gen lfs`添加。')
-			for ff in ('data', 'down', 'pre', 'statement', 'tables', 'resources', 'solution'):
-				st_path = pjoin(path, ff)
-				if not os.path.exists(st_path):
-					os.makedirs(st_path)
-				if not os.path.exists(pjoin(base.path, 'sample-' + folder, ff)):
-					continue
-				for f in os.listdir(pjoin(base.path, 'sample-' + folder, ff)):
-					sample_copy(pjoin(ff, f), pjoin(ff, f), path, 'sample-' + folder)
-		if path != '.':
-			conf = base.load_json(path)
-			conf['name'] = path
-			conf.path = path
-			if path == 'day0':
-				conf['title']['zh-cn'] = u'试机'
-			elif path[:3] == 'day':
-				try:
-					num = int(path[3:])
-					conf['title']['zh-cn'] = u'第' + num2chinese.num2chinese(num) + u'试'
-				except Exception as e:
-					pass
-			base.save_json(conf)
-	if len(args) != 0:
-		for arg in args:
-			if arg not in base.conf['subdir']:
-				base.conf['subdir'].append(arg)
-		base.save_json(base.conf)
-
-def upgrade():
-	if base.conf:	#是conf.json格式的老版本
-		used = {}
-		def upgrade_r(conf):
-			'''
-			非最新版本return False
-			'''
-			def upgrade_None(conf):
-				log.info(u'将`%s`从None版本升级到0版本。' % conf.route)
-				conf['version'] = 0
-				if conf.folder == 'problem':
-					for folder, cases, key in [('data', 'test cases', 'data'), ('down', 'sample count', 'samples')]:
-						if cases in conf:
-							cnt = conf.pop(cases)
-							for i in range(1, cnt + 1):
-								for suf in ['.in', '.ans']:
-									try:
-										ff = pjoin(conf.path, folder, conf['name'] + str(i) + suf)
-										ft = pjoin(conf.path, folder, str(i) + suf)
-										os.rename(ff, ft)
-									except FileNotFoundError as e:
-										if os.path.exists(ft):
-											log.info('`%s`已经改名，跳过重命名。' % ft)
-										else:
-											log.error('`%s`和`%s`都找不到，可能你的文件命名错误。' % (ff, ft))
-							work_list[key](conf)
-				return False
-			def upgrade_0(conf):
-				log.info(u'将`%s`从0版本升级到1版本。' % conf.route)
-				conf['version'] = 1
-				if conf.folder == 'problem':
-					if 'users' not in conf:
-						conf['users'] = {}
-					if 'pre' not in conf:
-						conf['pre'] = []
-					for user, algos in conf['users'].items():
-						for algo in algos:
-							if type(algos[algo]) == str:
-								algos[algo] = {'path' : algos[algo], 'expected' : {}}
-				return False
-			def upgrade_1(conf):
-				log.info(u'将`%s`从1版本升级到2版本。' % conf.route)
-				conf['version'] = 2
-				if conf.folder == 'problem':
-					if 'users' not in conf:
-						conf['users'] = {}
-					if 'packed' in conf:
-						conf.pop('packed')
-					for user, algos in conf['users'].items():
-						for algo, info in algos.items():
-							if type(info.get('expected', None)) == dict:
-								info['expected'] = ['%s %s' % (key, val) for key, val in info['expected'].items()]
-								if len(info['expected']) == 1:
-									info['expected'] = info['expected'][0]
-				return False
-			def upgrade_2(conf):
-				log.info(u'`%s`是最新版本。' % conf.route)
-				return True
-			path = os.path.abspath(conf.path)
-			if path in used:
-				for key in used[path]:
-					conf[key] = used[path][key]
-			while not eval('upgrade_' + str(conf['version']))(conf):
-				pass
-			for sub in conf.sub:
-				upgrade_r(sub)
-			used[path] = conf
-		upgrade_r(base.conf)
-		base.save_json(base.conf)
-	else:			#是prob(s).json格式的老版本
-		if not os.path.exists('probs.json'):
-			log.error(u'找不到`probs.json`。')
-			return
-		old_json = json.loads(open('probs.json', 'rb').read().decode('utf-8'))
-		new_dir('contest', [])
-		base.conf = base.load_json()
-		base.conf.pop('version')
-		new_dir('day', base.sorter()(old_json.keys()))
-		base.conf = base.load_json()
-		for day in base.conf.sub:
-			day.pop('version')
-			day['subdir'] += [prob for prob in old_json[day['name']]]
-		base.save_json(base.conf)
-		base.conf = base.load_json()
-		upgrade()
-
-def copy_lfs():
-	for prob in base.probs(no_repeat = True):
-		copy = lambda src, tgt = None: sample_copy(src, tgt, prob.path)
-		copy('problem.gitattributes', '.gitattributes')
-
-def copy_chk():
-	if base.conf['folder'] != 'problem':
-		log.error(u'答案校验器只能添加给题目工程，请到题目目录下运行。')
-		return
-	for prob in base.probs(no_repeat = True):
-		copy = lambda src, tgt = None: sample_copy(src, tgt, prob.path)
-		if not os.path.exists(pjoin(prob.path, 'data', 'chk')):
-			os.makedirs(pjoin(prob.path, 'data', 'chk'))
-		copy('chk.cpp', pjoin('data', 'chk'))
-
-def copy_prec():
-	if base.conf['folder'] != 'contest':
-		log.error(u'考生须知只能添加给比赛工程。')
-		return
-	path = '.'
-	copy = lambda src, tgt = None: sample_copy(src, tgt, path)
-	for ff in ('precautions', ):
-		st_path = pjoin(path, ff)
-		if not os.path.exists(st_path):
-			os.makedirs(st_path)
-		for f in os.listdir(pjoin(base.path, 'sample', ff)):
-			copy(pjoin(ff, f), pjoin(ff, f))
-
-work_list = {
-	'data' : lambda conf = None: find_all_data('data', 'data', 'test_cases', conf),
-	'samples' : lambda conf = None: find_all_data('samples', 'down', 'sample_cases', conf),
-	'pre' : lambda conf = None: find_all_data('pre', 'pre', 'pre_cases', conf),
-	'code' : find_all_code,
-	'contest' : lambda : new_dir('contest'),
-	'day' : lambda : new_dir('day'),
-	'problem' : lambda : new_dir('problem'),
-	'empty' : lambda : new_dir('empty'),
-	'upgrade' : upgrade,
-	'lfs' : copy_lfs,
-	'chk' : copy_chk,
-	'prec' : copy_prec
-}
-work_list['auto'] = lambda : [work_list[key]() for key in ['data', 'samples', 'pre', 'code']]
-work_list['n'] = work_list['contest']
-work_list['d'] = work_list['day']
-work_list['p'] = work_list['problem']
-work_list['e'] = work_list['empty']
-work_list['t'] = work_list['data']
-work_list['s'] = work_list['samples']
-work_list['u'] = work_list['upgrade']
-work_list['a'] = work_list['auto']
-
-if __name__ == '__main__':
-	try:
-		result = base.init()
-	except base.NoFileException as e:
-		base.conf = None
-		result = True
-	if result:
-		for base.work in base.works:
-			base.run_exc(work_list[base.work])
-	else:
-		log.info(u'这个工具用于快速建立一道题目。')
-		log.info(u'支持的工作：')
-		log.info(u'  contest  在当前目录下生成一场比赛，不支持参数。')
-		log.info(u'  n        同contest。')
-		log.info(u'  day      无参数表示在当前目录下生成一个比赛日，比赛日可以是独立的工程；')
-		log.info(u'           有参数表示在当前比赛下依次生成名叫参数1，参数2，…的比赛日，')
-		log.info(u'           有参数必须保证当前目录是比赛。')
-		log.info(u'  d        同day。')
-		log.info(u'  problem  无参数表示在当前目录下生成一道题目，题目可以是独立的工程；')
-		log.info(u'           有参数表示在当前比赛日下依次生成名叫参数1，参数2，…的题目，')
-		log.info(u'           有参数必须保证当前目录是比赛日。')
-		log.info(u'  p        同problem。')
-		log.info(u'  empty    无参数表示在当前目录下生成一道无例子的题目，题目可以是独立的工程；')
-		log.info(u'           有参数表示在当前比赛日下依次生成名叫参数1，参数2，…的题目，')
-		log.info(u'           有参数必须保证当前目录是比赛日。')
-		log.info(u'  e        同empty。')
-		log.info(u'  data     在题目工程的data文件夹中搜索数据并添加到配置文件。')
-		log.info(u'           对于比赛工程和比赛日工程，此操作将应用于所有子题目工程，下同。')
-		log.info(u'  t        同data。')
-		log.info(u'  samples  在题目工程的down文件夹中搜索样例并添加到配置文件。')
-		log.info(u'  s        同samples。')
-		log.info(u'  pre      在题目工程的pre文件夹中搜索预测试数据并添加到配置文件。')
-		log.info(u'  code     在题目工程的非数据文件夹中搜索源代码并添加到配置文件。')
-		log.info(u'  c        同code。')
-		log.info(u'  auto     等于一次性做了上述4件事情。')
-		log.info(u'  a        同auto。')
-		log.info(u'  lfs      用git-lfs维护所有的*.in/out/ans，当数据较大时使用。')
-		log.info(u'  chk      添加一个空的答案校验器或称spj，建议在此基础上修改以兼容。')
-		log.info(u'  prec     对于比赛工程，添加考生须知文件。')
-		log.info(u'  upgrade  升级老版本工程到现在版本的工程。')
-		log.info(u'  u        同upgrade。')
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+from . import num2chinese
+import platform
+from . import base
+from .base import log, pjoin
+
+def find_all_data(kind, folder, key, conf = None):
+	if not conf:
+		conf = base.conf
+	def find_data(path = ''):
+		full_path = pjoin(prob.path, folder, path)
+		for f in os.listdir(full_path):
+			if os.path.isfile(pjoin(full_path, f)):
+				if not f.endswith('.in'):
+					continue
+				fans = pjoin(full_path, f[:-3]) + '.ans'
+				if not os.path.exists(fans) or not os.path.isfile(fans):
+					continue
+				name = base.rjoin(path, f[:-3])
+				if name not in new_data and name not in exist_data:
+					new_data.add(name)
+			else:
+				find_data(base.rjoin(path, f))
+	def parse(data):
+		tmp = base.sorter()(map(str, list(data)))
+		ret = []
+		for i in tmp:
+			try:
+				ret.append(int(i))
+			except Exception as e:
+				ret.append(i)
+		return ret
+	for prob in conf.probs(no_repeat = True):
+		log.info(u'在题目`%s`下搜索%s数据。' % (prob.route, key))
+		is_lfs = os.path.exists(pjoin(prob.path, '.gitattributes'))
+		new_data = set()
+		exist_data = set(map(str, prob.__getattribute__(key)))
+		try:
+			find_data()
+		except Exception as e:
+			log.warning(e)
+		new_data = parse(new_data)
+		for datum in new_data:
+			log.info(u'发现新数据`%s`。' % (pjoin(prob.path, folder, str(datum))))
+		if not is_lfs:
+			for tdata in (exist_data, new_data):
+				for datum in tdata:
+					for suf in ('.in', '.out', '.ans'):
+						fname = pjoin(prob.path, folder, str(datum) + suf)
+						if os.path.exists(fname) and os.path.getsize(fname) >= 1024 * 1024:
+							log.warning(u'题目`%s`下%s数据达到了1MiB，建议在该题下使用`python tuack.gen lfs`。' % (prob.route, key))
+							break
+					else:
+						continue
+					break
+				else:
+					continue
+				break
+		prob.__getattribute__(key).__iadd__(new_data)
+		if kind not in prob:
+			prob[kind] = []
+		if len(new_data) > 0:
+			prob[kind].append({'cases' : new_data})
+		base.save_json(prob)
+	
+def find_all_code():
+	def find_code(user, path):
+		full_path = pjoin(prob.path, user, path)
+		for f in os.listdir(full_path):
+			if base.user_skip.match(f):
+				continue
+			if os.path.isfile(pjoin(full_path, f)):
+				for key in base.compilers:
+					if not f.endswith('.' + key):
+						continue
+					code_path = base.rjoin(user, path, f).replace('//', '/')
+					if code_path not in exist_code:
+						prob['users'][user][base.rjoin(path, f).replace('//', '/')] = {
+							'path' : code_path,
+							'expected' : '== 100' if 'std' in code_path or prob['name'] in code_path else []
+						}
+						log.info(u'发现新源代码`%s`。' % code_path)
+					break
+			else:
+				find_code(user, base.rjoin(path, f))
+
+	for prob in base.probs(no_repeat = True):
+		if prob['type'] == 'output':
+			log.info(u'题目`%s`是提交答案题，跳过。' % prob.route)
+			continue
+		log.info(u'在题目`%s`下搜索源代码。' % prob.route)
+		if 'users' not in prob:
+			prob['users'] = {}
+		exist_code = set()
+		for user, algos in prob['users'].items():
+			for algo, path in algos.items():
+				exist_code.add((path['path'] if type(path) == dict else path).replace('//', '/'))
+		for f in os.listdir(prob.path):
+			if base.user_skip.match(f) or os.path.isfile(pjoin(prob.path, f)):
+				continue
+			if f not in prob['users']:
+				prob['users'][f] = {}
+			find_code(f, '')
+			if len(prob['users'][f]) == 0:
+				prob['users'].pop(f)
+		base.save_json(prob)
+
+def sample_copy(src, tgt = None, path = '', base_path = 'sample'):
+	if not tgt:
+		tgt = src
+	full_tgt = pjoin(path, tgt)
+	if os.path.exists(full_tgt) and not os.path.isfile(full_tgt):
+		full_tgt = pjoin(full_tgt, src)
+	if not os.path.exists(full_tgt):
+		log.info(u'生成文件`%s`' % full_tgt)
+		base.copy(
+			pjoin(base.path, base_path),
+			src,
+			full_tgt
+		)
+
+def new_dir(folder, args = None):
+	if not args:
+		args = base.args
+	if len(args) == 0:
+		dirs = ['.']
+	else:
+		if not base.conf:
+			log.error(u'当前文件夹下没有找到合法的`conf.json`文件。')
+			log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
+			return
+		if folder == 'contest':
+			log.error(u'文件夹层次错误：比赛工程不能放在其他工程中。')
+			return
+		if folder == 'day' and base.conf.folder != 'contest':
+			log.error(u'文件夹层次错误：比赛日工程只能放在比赛工程中。')
+			return
+		if (folder == 'problem' or folder == 'empty') and base.conf.folder != 'day':
+			log.error(u'文件夹层次错误：题目工程只能放在比赛日工程中。')
+			return
+		dirs = args
+	for path in dirs:
+		if not os.path.exists(path):
+			os.makedirs(path)
+		if path != '.' and path in base.conf['subdir']:
+			log.warning(u'`%s`已经在工程中了，跳过它的建立。' % path)
+			log.info(u'如果需要强制建立，需要将其从`conf.yaml`中移除。')
+			continue
+		copy = lambda src, tgt = None: sample_copy(src, tgt, path)
+		def copy_conf(inp):
+			if base.dump_format != 'json':
+				open(pjoin(path, 'conf.' + base.dump_format), 'wb').write(
+					base.dump_formats[base.dump_format](
+						json.loads(open(pjoin(base.path, 'sample', inp), 'rb').read().decode('utf-8'))
+					)
+				)
+			else:
+				copy(inp, 'conf.json')
+		copy(folder + '.gitignore', '.gitignore')
+		copy_conf(folder + '.json')
+		if folder == 'problem' or folder == 'empty':
+			if base.git_lfs:
+				copy(folder + '.gitattributes', '.gitattributes')
+			else:
+				log.info(u'现在不默认用git-lfs，如需，用`python -m tuack.gen lfs`添加。')
+			for ff in ('data', 'down', 'pre', 'statement', 'tables', 'resources', 'solution'):
+				st_path = pjoin(path, ff)
+				if not os.path.exists(st_path):
+					os.makedirs(st_path)
+				if not os.path.exists(pjoin(base.path, 'sample-' + folder, ff)):
+					continue
+				for f in os.listdir(pjoin(base.path, 'sample-' + folder, ff)):
+					sample_copy(pjoin(ff, f), pjoin(ff, f), path, 'sample-' + folder)
+		if path != '.':
+			conf = base.load_json(path)
+			conf['name'] = path
+			conf.path = path
+			if path == 'day0':
+				conf['title']['zh-cn'] = u'试机'
+			elif path[:3] == 'day':
+				try:
+					num = int(path[3:])
+					conf['title']['zh-cn'] = u'第' + num2chinese.num2chinese(num) + u'试'
+				except Exception as e:
+					pass
+			base.save_json(conf)
+	if len(args) != 0:
+		for arg in args:
+			if arg not in base.conf['subdir']:
+				base.conf['subdir'].append(arg)
+		base.save_json(base.conf)
+
+def upgrade():
+	if base.conf:	#是conf.json格式的老版本
+		used = {}
+		def upgrade_r(conf):
+			'''
+			非最新版本return False
+			'''
+			def upgrade_None(conf):
+				log.info(u'将`%s`从None版本升级到0版本。' % conf.route)
+				conf['version'] = 0
+				if conf.folder == 'problem':
+					for folder, cases, key in [('data', 'test cases', 'data'), ('down', 'sample count', 'samples')]:
+						if cases in conf:
+							cnt = conf.pop(cases)
+							for i in range(1, cnt + 1):
+								for suf in ['.in', '.ans']:
+									try:
+										ff = pjoin(conf.path, folder, conf['name'] + str(i) + suf)
+										ft = pjoin(conf.path, folder, str(i) + suf)
+										os.rename(ff, ft)
+									except FileNotFoundError as e:
+										if os.path.exists(ft):
+											log.info('`%s`已经改名，跳过重命名。' % ft)
+										else:
+											log.error('`%s`和`%s`都找不到，可能你的文件命名错误。' % (ff, ft))
+							work_list[key](conf)
+				return False
+			def upgrade_0(conf):
+				log.info(u'将`%s`从0版本升级到1版本。' % conf.route)
+				conf['version'] = 1
+				if conf.folder == 'problem':
+					if 'users' not in conf:
+						conf['users'] = {}
+					if 'pre' not in conf:
+						conf['pre'] = []
+					for user, algos in conf['users'].items():
+						for algo in algos:
+							if type(algos[algo]) == str:
+								algos[algo] = {'path' : algos[algo], 'expected' : {}}
+				return False
+			def upgrade_1(conf):
+				log.info(u'将`%s`从1版本升级到2版本。' % conf.route)
+				conf['version'] = 2
+				if conf.folder == 'problem':
+					if 'users' not in conf:
+						conf['users'] = {}
+					if 'packed' in conf:
+						conf.pop('packed')
+					for user, algos in conf['users'].items():
+						for algo, info in algos.items():
+							if type(info.get('expected', None)) == dict:
+								info['expected'] = ['%s %s' % (key, val) for key, val in info['expected'].items()]
+								if len(info['expected']) == 1:
+									info['expected'] = info['expected'][0]
+				return False
+			def upgrade_2(conf):
+				log.info(u'`%s`是最新版本。' % conf.route)
+				return True
+			path = os.path.abspath(conf.path)
+			if path in used:
+				for key in used[path]:
+					conf[key] = used[path][key]
+			while not eval('upgrade_' + str(conf['version']))(conf):
+				pass
+			for sub in conf.sub:
+				upgrade_r(sub)
+			used[path] = conf
+		upgrade_r(base.conf)
+		base.save_json(base.conf)
+	else:			#是prob(s).json格式的老版本
+		if not os.path.exists('probs.json'):
+			log.error(u'找不到`probs.json`。')
+			return
+		old_json = json.loads(open('probs.json', 'rb').read().decode('utf-8'))
+		new_dir('contest', [])
+		base.conf = base.load_json()
+		base.conf.pop('version')
+		new_dir('day', base.sorter()(old_json.keys()))
+		base.conf = base.load_json()
+		for day in base.conf.sub:
+			day.pop('version')
+			day['subdir'] += [prob for prob in old_json[day['name']]]
+		base.save_json(base.conf)
+		base.conf = base.load_json()
+		upgrade()
+
+def copy_lfs():
+	for prob in base.probs(no_repeat = True):
+		copy = lambda src, tgt = None: sample_copy(src, tgt, prob.path)
+		copy('problem.gitattributes', '.gitattributes')
+
+def copy_chk():
+	if base.conf['folder'] != 'problem':
+		log.error(u'答案校验器只能添加给题目工程，请到题目目录下运行。')
+		return
+	for prob in base.probs(no_repeat = True):
+		copy = lambda src, tgt = None: sample_copy(src, tgt, prob.path)
+		if not os.path.exists(pjoin(prob.path, 'data', 'chk')):
+			os.makedirs(pjoin(prob.path, 'data', 'chk'))
+		copy('chk.cpp', pjoin('data', 'chk'))
+
+def copy_prec():
+	if base.conf['folder'] != 'contest':
+		log.error(u'考生须知只能添加给比赛工程。')
+		return
+	path = '.'
+	copy = lambda src, tgt = None: sample_copy(src, tgt, path)
+	for ff in ('precautions', ):
+		st_path = pjoin(path, ff)
+		if not os.path.exists(st_path):
+			os.makedirs(st_path)
+		for f in os.listdir(pjoin(base.path, 'sample', ff)):
+			copy(pjoin(ff, f), pjoin(ff, f))
+
+work_list = {
+	'data' : lambda conf = None: find_all_data('data', 'data', 'test_cases', conf),
+	'samples' : lambda conf = None: find_all_data('samples', 'down', 'sample_cases', conf),
+	'pre' : lambda conf = None: find_all_data('pre', 'pre', 'pre_cases', conf),
+	'code' : find_all_code,
+	'contest' : lambda : new_dir('contest'),
+	'day' : lambda : new_dir('day'),
+	'problem' : lambda : new_dir('problem'),
+	'empty' : lambda : new_dir('empty'),
+	'upgrade' : upgrade,
+	'lfs' : copy_lfs,
+	'chk' : copy_chk,
+	'prec' : copy_prec
+}
+work_list['auto'] = lambda : [work_list[key]() for key in ['data', 'samples', 'pre', 'code']]
+work_list['n'] = work_list['contest']
+work_list['d'] = work_list['day']
+work_list['p'] = work_list['problem']
+work_list['e'] = work_list['empty']
+work_list['t'] = work_list['data']
+work_list['s'] = work_list['samples']
+work_list['u'] = work_list['upgrade']
+work_list['a'] = work_list['auto']
+
+if __name__ == '__main__':
+	try:
+		result = base.init()
+	except base.NoFileException as e:
+		base.conf = None
+		result = True
+	if result:
+		for base.work in base.works:
+			base.run_exc(work_list[base.work])
+	else:
+		log.info(u'这个工具用于快速建立一道题目。')
+		log.info(u'支持的工作：')
+		log.info(u'  contest  在当前目录下生成一场比赛，不支持参数。')
+		log.info(u'  n        同contest。')
+		log.info(u'  day      无参数表示在当前目录下生成一个比赛日，比赛日可以是独立的工程；')
+		log.info(u'           有参数表示在当前比赛下依次生成名叫参数1，参数2，…的比赛日，')
+		log.info(u'           有参数必须保证当前目录是比赛。')
+		log.info(u'  d        同day。')
+		log.info(u'  problem  无参数表示在当前目录下生成一道题目，题目可以是独立的工程；')
+		log.info(u'           有参数表示在当前比赛日下依次生成名叫参数1，参数2，…的题目，')
+		log.info(u'           有参数必须保证当前目录是比赛日。')
+		log.info(u'  p        同problem。')
+		log.info(u'  empty    无参数表示在当前目录下生成一道无例子的题目，题目可以是独立的工程；')
+		log.info(u'           有参数表示在当前比赛日下依次生成名叫参数1，参数2，…的题目，')
+		log.info(u'           有参数必须保证当前目录是比赛日。')
+		log.info(u'  e        同empty。')
+		log.info(u'  data     在题目工程的data文件夹中搜索数据并添加到配置文件。')
+		log.info(u'           对于比赛工程和比赛日工程，此操作将应用于所有子题目工程，下同。')
+		log.info(u'  t        同data。')
+		log.info(u'  samples  在题目工程的down文件夹中搜索样例并添加到配置文件。')
+		log.info(u'  s        同samples。')
+		log.info(u'  pre      在题目工程的pre文件夹中搜索预测试数据并添加到配置文件。')
+		log.info(u'  code     在题目工程的非数据文件夹中搜索源代码并添加到配置文件。')
+		log.info(u'  c        同code。')
+		log.info(u'  auto     等于一次性做了上述4件事情。')
+		log.info(u'  a        同auto。')
+		log.info(u'  lfs      用git-lfs维护所有的*.in/out/ans，当数据较大时使用。')
+		log.info(u'  chk      添加一个空的答案校验器或称spj，建议在此基础上修改以兼容。')
+		log.info(u'  prec     对于比赛工程，添加考生须知文件。')
+		log.info(u'  upgrade  升级老版本工程到现在版本的工程。')
+		log.info(u'  u        同upgrade。')
```

### Comparing `tuack-0.1.4.9.2/tuack/lex/compile.pyinc` & `tuack-0.1.5/tuack/lex/compile.pyinc`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/format-linux` & `tuack-0.1.5/tuack/lex/format-linux`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/format-mac` & `tuack-0.1.5/tuack/lex/format-mac`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/format-win.exe` & `tuack-0.1.5/tuack/lex/format-win.exe`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/lex.l` & `tuack-0.1.5/tuack/lex/lex.l`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/lex.yy.c` & `tuack-0.1.5/tuack/lex/lex.yy.c`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/lex.yy.o` & `tuack-0.1.5/tuack/lex/lex.yy.o`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/yacc.tab.c` & `tuack-0.1.5/tuack/lex/yacc.tab.c`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/yacc.tab.h` & `tuack-0.1.5/tuack/lex/yacc.tab.h`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/lex/yacc.tab.o` & `tuack-0.1.5/tuack/lex/yacc.tab.o`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/num2chinese.py` & `tuack-0.1.5/tuack/num2chinese.py`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/packer.py` & `tuack-0.1.5/tuack/packer.py`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/ren.py` & `tuack-0.1.5/tuack/ren.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,723 +1,749 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-import platform
-import gettext
-import yaml
-from . import base
-from .base import log, pjoin
-try:
-	import jinja2
-except:
-	pass
-from . import tools
-import uuid
-import traceback
-
-work_class = {
-	'noi' : {'noi'},
-	'ccpc' : {'ccpc'},
-	'uoj' : {'uoj'},
-	'loj' : {'loj'},
-	'ipuoj' : {'ipuoj'},
-	'tupc' : {'tupc'},
-	'tuoj-pc' : {'tupc', 'tuoj'},
-	'tuoi' : {'tuoi'},
-	'tuoj-oi' : {'tuoi', 'tuoj'},
-	'tuoj' : {'tuoj'},
-	'thuoj' : {'thuoj'},
-	'hand' : {'hand'},
-	'ccc' : {'ccc-tex', 'ccc-md'},
-	'ccc-tex' : {'ccc-tex'},
-	'ccc-md' : {'ccc-md'},
-	'tsinsen-oj' : {'tsinsen-oj'},
-	'tex' : {'noi', 'ccpc', 'tupc', 'tuoi', 'ccc-tex', 'hand'},
-	'md' : {'uoj', 'tuoj', 'ccc-md', 'loj', 'ipuoj'},
-	'html' : {'tsinsen-oj'},
-	'doku' : {'thuoj'}
-}
-io_styles = {
-	'noi' : 'fio',
-	'ccpc' : 'stdio',
-	'uoj' : 'stdio',
-	'tuoj' : 'stdio',
-	'ccc' : 'stdio',
-	'tuoi' : 'stdio',
-	'tupc' : 'stdio',
-	'tsinsen-oj' : 'stdio',
-	'loj' : 'stdio',
-	'ipuoj' : 'stdio',
-	'thuoj' : 'stdio',
-	'hand' : 'stdio'
-}
-base_templates = {
-	'noi' : 'tuoi',
-	'tuoi' : 'tuoi',
-	'tupc' : 'tupc',
-	'ccpc' : 'ccpc',
-	'ccc' : 'ccc',
-	'hand' : 'hand'
-}
-
-secondary_dict = {}
-env = None
-pandoc_version = None
-
-def detect_pandoc_version():
-	global pandoc_version
-	if pandoc_version is not None:
-		return
-	cp = subprocess.Popen(['pandoc', '-v'], stdout = subprocess.PIPE)
-	line = cp.stdout.read().decode().splitlines()[0]
-	pandoc_version = line.split()[-1]
-
-def get_pandoc_option():
-	detect_pandoc_version()
-	if pandoc_version.startswith('2.'):
-		option = '--listings -f markdown-smart -t latex-smart'
-	else:
-		option = '--no-tex-ligatures --listings -t latex'
-	return option
-
-def get_template(fname, lang = None):
-	global env
-	if base.lang:
-		lang = base.lang
-	if not lang:
-		lang = 'zh-cn'
-	if env == None or base.system == 'Darwin' or (lang and env['lang'] != lang):
-		env = {
-			'env' : jinja2.Environment(
-				loader = jinja2.FileSystemLoader(pjoin(os.getcwd(), 'tmp')),
-				extensions = ['jinja2.ext.do', 'jinja2.ext.with_', 'jinja2.ext.i18n']
-			),
-			'lang' : lang
-		}
-		try:
-			tra = gettext.translation('lang', os.getcwd() + '/tmp', [env['lang']])
-			env['env'].install_gettext_translations(tra)
-		except FileNotFoundError as e:
-			log.warning(u'没有%s这种语言的翻译表可用。' % lang)
-	return env['env'].get_template(fname)
-
-def table(path, name, temp, context, options):
-	if options == None:
-		options = {}
-	for suf in ['.py', '.pyinc', '.json', '.yaml', '.yml']:
-		try:
-			base.copy(path, name + suf, pjoin('tmp', 'table' + suf))
-			log.info(u'渲染表格`%s`，参数%s' % (base.pjoin(path, name + suf), str(options)))
-			break
-		except base.NoFileException as e:
-			pass
-	else:
-		raise base.NoFileException(u'找不到表格`%s.*`' % base.pjoin(path, name))
-	if suf == '.json':
-		res = get_template('table.json', context['prob'].lang()).render(context, options = options)
-		try:
-			table = json.loads(res)
-		except Exception as e:
-			open(pjoin('tmp', 'table.tmp.json'), 'w').write(res)
-			log.error(u'json文件错误`tmp/table.tmp.json`')
-			raise e
-		os.remove(pjoin('tmp', 'table.json'))
-	elif suf == '.yaml' or suf == '.yml':
-		try:
-			table = yaml.full_load(open(base.pjoin('tmp', 'table' + suf), 'rb').read().decode('utf-8'))
-		except Exception as e:
-			open(pjoin('tmp', 'table.tmp.json'), 'w').write(res)
-			log.error(u'json文件错误`tmp/table.tmp.json`')
-			raise e
-	elif suf == '.py' or suf == '.pyinc':
-		def merge_ver(table):
-			ret = [row for row in table]
-			last = ret[-1]
-			for i in range(len(table) - 2, 0, -1):
-				for j in range(len(last)):
-					if last[j] == ret[i][j]:
-						last[j] = None
-				last = ret[i]
-			return ret
-		code = 'def render(context, options, merge_ver):\n'
-		code += '\tglobal val\n'
-		code += '\tfor key, val in context.items():\n'
-		code += '\t\texec(\'%s = val\' % key, globals())\n'
-		for line in open(base.pjoin('tmp', 'table' + suf), 'rb'):
-			code += '\t' + line.decode('utf-8').rstrip() + '\n'
-		namespace = {}
-		exec(code, namespace)
-		try:
-			table = json.loads(json.dumps(namespace['render'](context, options, merge_ver)))
-		except Exception as e:
-			log.error(e)
-			lines = traceback.format_exc().splitlines()
-			for idx, line in enumerate(lines):
-				if '<string>' in line:
-					m = re.match(r'^.*line (\d*),.*$', line)
-					if m:
-						lineno = int(m.group(1)) - 4
-						log.info('  File "%s", line %d' % (base.pjoin(path, name + suf), lineno))
-						log.info(code.splitlines()[lineno + 3][1:])
-						for i in range(idx + 1, len(lines)):
-							log.info(lines[i])
-						break
-			else:
-				raise e
-			raise e
-	if context.get('comp') in {'loj', 'ipuoj'} and len(table) > 0:
-		last_line = [None] * len(table[0])
-		for i in range(len(table)):
-			for j in range(len(table[i])):
-				if table[i][j] == None:
-					table[i][j] = last_line[j]
-				else:
-					last_line[j] = table[i][j]
-	cnt = [[1] * len(row) for row in table]
-	max_len = len(table[-1])
-	for i in range(len(table) - 2, -1, -1):
-		max_len = max(max_len, len(table[i]))
-		for j in range(min(len(table[i]), len(table[i + 1]))):
-			if table[i + 1][j] == None:
-				cnt[i][j] += cnt[i + 1][j]
-	ret = get_template(temp, context['prob'].lang()).render(context, table = table, cnt = cnt, width = max_len, options = options)
-	return ret
-
-def to_arg(dic):
-	return ','.join(['%s = %s' % (key, val if type(val) != str else json.dumps(val)) for key, val in dic.items()])
-
-def uoj_title(text):	## 很显然，这个是在瞎整，不过UOJ为什么从二级标题开始用？修改标题字体大小应该改CSS而不是题目嘛
-	in_quote = 0
-	result = []
-	for line in text.split(b'\n'):
-		if in_quote == 0 and line.startswith(b'#'):
-			result.append(b'#' + line)
-		else:
-			result.append(line)
-		in_quote ^= line.count(b'```') & 1
-	return b'\n'.join(result)
-	
-def loj_bug(text):		## 学弟也学着我瞎整，伤心QAQ
-	# TODO: Avoid duplication
-	in_quote = 0
-	result = []
-	for line in text.split(b'\n'):
-		if in_quote == 0 and line.startswith(b'<table'):
-			result.append(line
-				.replace(b'$<', b'$ <')   # LOJ Markdown 渲染的已知 bug
-			)
-		else:
-			result.append(line)
-		in_quote ^= line.count(b'```') & 1
-	return b'\n'.join(result)
-
-class Base(object):
-	def __init__(self, comp, conf = None):
-		self.conf = (base.conf if conf == None else conf)
-		self.comp = comp
-		self.day = None
-		self.contest = None
-		self.prob = None
-		self.path = None
-		self.prec = None
-		self.secondary_dict = {}
-		self.io_style = io_styles[comp]
-
-	def file_name(self, name):
-		if self.comp == 'noi':
-			return self.prob['name'] + '/' + name
-		elif self.comp == 'uoj':
-			return name
-		else:
-			return name
-
-	def secondary(self, s, sp = None):
-		if sp != None:
-			if type(sp) == str:
-				sp = [sp]
-			in_set = False
-			for i in sp:
-				if i in work_class and base.work in work_class[i]:
-					in_set = True
-					break
-			if not in_set:
-				return ''
-		if self.work == 'tex' or self.work == 'html' or self.work == 'doku':
-			id = str(uuid.uuid4())
-			self.secondary_dict[id] = s
-			return id
-		else:
-			return ' {{ ' + s + ' }} '
-
-	def resource(self, name):
-		if self.comp in {'loj', 'ipuoj'} and self.prob.get('pid', {}).get(self.comp + '-default'):
-			return '/../problem/show_image/%d/' % self.prob.get('pid', {}).get(self.comp + '-default') + name
-		return self.prob['name'] + '/' + name
-		
-	def down_file(self, name):
-		ret = ''
-		fname = pjoin(self.prob.path, 'down', name)
-		length_warned = False
-		for idx, line in enumerate(open(fname, 'rb')):
-			if len(line) > 60 and not length_warned:
-				log.warning(u'文件`%s`的第%d行太长，建议只提供下发而不渲染到题面。' % (fname, idx + 1))
-				length_warned = True
-			ret += line.decode('utf-8')
-		return ret
-
-	def hide_file(self, name):
-		ret = ''
-		fname = pjoin(self.prob.path, 'hide', name)
-		length_warned = False
-		for idx, line in enumerate(open(fname, 'rb')):
-			if len(line) > 60 and not length_warned:
-				log.warning(u'文件`%s`的第%d行太长，建议只提供下发而不渲染到题面。' % (fname, idx + 1))
-				length_warned = True
-			ret += line.decode('utf-8')
-		if self.comp not in work_class['tex']:
-			if ret < 20:
-				return u'隐藏内容'
-			c = len(ret) // 20
-			ret =  ret[:c] + u'……隐藏内容……' + ret[-c:]
-		return ret
-		
-	def titlize(self, title, args, lang = None):
-		if base.lang:
-			lang = base.lang
-		if not lang:
-			lang = 'zh-cn'
-		if title == 'sample':
-			if len(args) > 0:
-				self.context['vars']['sample_id'] = args[0]
-			if len(args) <= 1:
-				return ''
-		tra = gettext.translation('lang', os.getcwd() + '/tmp', [env['lang']])
-		ret = tra.gettext(title)
-		if len(args) > 0:
-			try:
-				ret = ret % args
-			except Exception as e:
-				ret = ret + ''.join(map(str, args))
-		else:
-			try:
-				ret = ret % ('',)
-			except Exception as e:
-				pass
-		return '## ' + ret
-
-	def ren_prob_md_j(self):
-		time.sleep(0.5)
-		log.info(u'渲染题目题面 %s %s' % (self.comp, self.prob.route))
-		try:
-			shutil.copy(self.prob.statement(), pjoin('tmp', 'problem.md.jinja'))
-			time.sleep(0.1)
-		except base.NoFileException as e:
-			log.error(u'找不到题面文件，建议使用`python -m tuack.gen problem`生成题目工程。')
-			return
-		self.context = {
-			'prob' : self.prob,
-			'args' : self.prob.get('args'),
-			'data' : self.prob.get('data'),
-			'samples' : self.prob.get('samples'),
-			'pre' : self.prob.get('pre'),
-			'dargs' : tools.a(self.prob.get('data')),
-			'pargs' : tools.a(self.prob.get('pre')),
-			'sargs' : tools.a(self.prob.get('samples')),
-			'aargs' : tools.a(self.prob.get('data'), self.prob.get('pre'), self.prob.get('samples')),
-			'day' : self.day,
-			'contest' : self.contest,
-			'io_style' : self.io_style,
-			'comp' : self.comp,
-			'tools' : tools,
-			'tl' : tools,
-			'base' : base,
-			'common' : base,
-			'file_name' : self.file_name,
-			'down_file' : self.down_file,
-			'resource' : self.resource,
-			'render' : self.secondary,
-			'precautions' : self.prec,
-			'json' : json,
-			'vars' : {},
-			's' : lambda title, *args : self.titlize(title, args, self.prob.lang())
-		}
-		self.context['img'] = lambda src, env = None, **argw : self.context['render'](
-			"template('image', resource = resource(%s), %s)" % (json.dumps(src), to_arg(argw)),
-			env
-		)
-		self.context['font'] = lambda txt, env = None, **argw : self.context['render'](
-			"template('font', txt = %s, %s)" % (json.dumps(txt), to_arg(argw)),
-			env
-		)
-		self.context['tbl'] = lambda src, env = None, **argw : self.context['render'](
-			"table(%s, %s)" % (json.dumps(src), argw),
-			env
-		)
-		if self.comp == 'tsinsen-oj' and 'tsinsen_files' in dir(self.prob):
-			self.context['resource'] = lambda name : '/RequireFile.do?fid=%s' % self.prob.tsinsen_files[name]
-		open(pjoin('tmp', 'problem.md'), 'wb') \
-			.write(get_template('problem_base.md.jinja', self.prob.lang())
-				.render(self.context)
-				.encode('utf-8')
-			)
-		time.sleep(0.1)
-
-	def check_install(self):
-		pass
-
-	def before(self):
-		base.mkdir('statements')
-		shutil.rmtree('tmp', ignore_errors = True)
-		time.sleep(0.1)
-		shutil.copytree(pjoin(base.path, 'templates'), 'tmp')
-		base.mkdir(pjoin('statements', self.comp))
-		if self.conf.folder == 'contest':
-			self.contest = self.conf
-		elif self.conf.folder == 'day':
-			self.day = self.conf
-		elif self.conf.folder == 'problem':
-			self.prob = self.conf
-
-	def move_resource(self):
-		if os.path.exists(pjoin(self.prob.path, 'resources')):
-			shutil.rmtree(self.path, ignore_errors = True)
-			time.sleep(0.1)
-			shutil.copytree(pjoin(self.prob.path, 'resources'), (self.path if self.prob.route != '' else pjoin(self.path, self.prob['name'])))
-
-	def gen_paths(self):
-		self.path = pjoin('statements', self.comp)
-		if self.prob.route != '':
-			self.path = pjoin(self.path, self.prob.route)
-		self.result_path = self.path + ('-' + base.lang if base.lang else '')
-		if self.prob.route == '':
-			self.result_path = pjoin(self.result_path, self.prob['name'])
-		self.result_path += '.' + self.work
-
-	def main(self):
-		if self.conf.folder == 'contest':
-			for self.day in self.conf.days():
-				if not os.path.exists(pjoin('statements', self.comp, self.day.route)):
-					os.makedirs(pjoin('statements', self.comp, self.day.route))
-		if self.comp == 'tsinsen-oj':
-			log.warning(u'如果你使用了resource，你可能需要使用dumper才能获得正确上传清橙的文件。')
-		for self.prob in self.conf.probs():
-			self.gen_paths()
-			self.move_resource()
-			self.ren_prob_md_j()
-			self.ren_prob_rest()
-			self.start_file()
-
-	def final(self):
-		shutil.rmtree('tmp', ignore_errors = True)
-
-	def run(self):
-		self.check_install()
-		self.before()
-		self.main()
-		self.final()
-
-	def start_file(self):
-		if base.start_file:
-			base.xopen_file(self.result_path)
-
-class Latex(Base):
-	work = 'tex'
-	day_templates = {
-		'noi' : 'tuoi',
-		'tuoi' : 'tuoi',
-		'tupc' : 'tupc',
-		'ccpc' : 'ccpc',
-		'ccc' : 'ccc',
-		'hand' : 'hand'
-	}
-
-	def resource(self, name):
-		return pjoin('..', self.prob.path, 'resources', name).replace('\\', '/')
-
-	def check_install(self):
-		base.check_install('pandoc')
-		base.check_install('xelatex')
-		base.check_install('gettext')
-
-	def ren_prec(self):
-		if not os.path.exists(base.pjoin(self.conf.path, 'precautions', 'zh-cn.md')):
-			return
-		context = {
-			'io_style' : self.io_style,
-			'comp' : self.comp,
-			'tools' : tools,
-			'tl' : tools,
-			'base' : base,
-			'json' : json
-		}
-		base.copy(base.pjoin(self.conf.path, 'precautions'), 'zh-cn.md', 'tmp')
-		open(base.pjoin('tmp', 'precautions.md'), 'wb') \
-			.write(get_template('zh-cn.md').render(context, conf = self.conf).encode('utf-8'))
-		os.system('pandoc %s %s -o %s' % (
-			get_pandoc_option(),
-			pjoin('tmp', 'precautions.md'),
-			pjoin('tmp', 'precautions.tex')
-		))
-		self.prec = open(pjoin('tmp', 'precautions.tex'), 'rb').read().decode('utf-8')
-
-	def ren_day_prec(self):
-		if not os.path.exists(base.pjoin(self.day.path, 'precautions', 'zh-cn.md')):
-			return
-		context = {
-			'io_style' : self.io_style,
-			'comp' : self.comp,
-			'tools' : tools,
-			'tl' : tools,
-			'base' : base,
-			'json' : json
-		}
-		base.copy(base.pjoin(self.day.path, 'precautions'), 'zh-cn.md', 'tmp')
-		open(base.pjoin('tmp', 'precautions.md'), 'wb') \
-			.write(get_template('zh-cn.md').render(context, conf = self.day).encode('utf-8'))
-		os.system('pandoc %s %s -o %s' % (
-			get_pandoc_option(),
-			pjoin('tmp', 'precautions.md'),
-			pjoin('tmp', 'precautions.tex')
-		))
-		self.prec = open(pjoin('tmp', 'precautions.tex'), 'rb').read().decode('utf-8')
-
-	def ren_prob_tex(self):
-		os.system('pandoc %s %s -o %s' % (
-			get_pandoc_option(),
-			pjoin('tmp', 'problem.md'),
-			pjoin('tmp', 'problem.tex')
-		))
-		tex = open(pjoin('tmp', 'problem.tex'), 'rb').read().decode('utf-8')
-		for key, val in self.secondary_dict.items():	## 如果未来发生了性能问题，这里可以先写到一个文件里然后再解析
-			open(pjoin('tmp', key + '.tex.jinja'), 'wb').write(
-				('{{ ' + val + ' }}').encode('utf-8')
-			)
-			ret = get_template(key + '.tex.jinja', self.prob.lang()).render(
-				self.context,
-				template = lambda temp_name, **context : get_template(temp_name + '.tex.jinja', self.prob.lang()).render(context),
-				table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.tex.jinja', self.context, options)
-			)
-			tex = tex.replace(key, ret)
-		self.secondary_dict = {}
-		return tex
-
-	def gen_compile(self):
-		clangs = {l for prob in self.probs for l in prob.get('compile', {}).keys()}
-		ret = {}
-		for clang in clangs:
-			cur = []
-			for prob in self.probs:
-				if prob['type'] != 'output':
-					if clang in prob['compile']:
-						cur.append({
-							'option' : prob['compile'][clang] + (' -Wl,--stack=%d' % prob.memory_limit().B if clang in {'cpp', 'c'} and base.out_system == 'Windows' else ''),
-							'cnt' : 1,
-							'use' : True
-						})
-					else:
-						cur.append({'option' : u'不可用', 'cnt' : 1, 'use' : False})
-				else:
-					cur.append({'option' : 'N/A', 'cnt' : 1, 'use' : False})
-			last = []
-			for p in cur:
-				if len(last) == 0 or p['option'] != last[-1]['option']:
-					last.append(p)
-				else:
-					last[-1]['cnt'] += 1
-			ret[clang] = last
-		return ret
-
-	def ren_day_pdf(self):
-		log.info(u'渲染比赛日题面 %s %s' % (self.comp, self.day.route if self.day else self.conf.route))
-		self.context.pop('prob')
-		self.context.pop('file_name')
-		self.context.pop('down_file')
-		self.context.pop('resource')
-		self.context.pop('render')
-		self.context['probs'] = self.probs
-		self.context['problems'] = self.tex_problems
-		self.context['compile'] = self.gen_compile()
-		self.context['water_mark'] = base.water_mark
-		if base.water_mark:
-			shutil.copy(base.water_mark, 'tmp/water_mark.' + base.water_mark.split('.')[-1])
-		all_problem_statement = get_template('%s.tex.jinja' % base_templates[self.comp]).render(self.context)
-		try:
-			open(pjoin('tmp', 'problems.tex'), 'wb') \
-				.write(all_problem_statement.encode('utf-8'))
-		except Exception as e:
-			log.info(u'渲染出错的文件为`tmp/problems.tmp.tex`')
-			open(pjoin('tmp', 'problems.tmp.tex'), 'wb') \
-				.write(all_problem_statement.encode('utf-8'))
-			raise e
-		log.info(u'开始使用xelatex渲染题面。')
-		os.chdir('tmp')
-		os.system('xelatex -interaction=batchmode problems.tex')
-		os.system('xelatex -interaction=batchmode problems.tex')
-		if not os.path.exists('problems.pdf'):
-			log.warning(u'题面渲染失败，尝试使用关闭静默模式渲染。')
-			os.system('xelatex problems.tex')
-			os.system('xelatex problems.tex')
-		if not os.path.exists('problems.pdf'):
-			log.error(u'题面渲染失败，请检查`tmp`目录下各文件。')
-		os.chdir('..')
-		shutil.copy(pjoin('tmp', 'problems.pdf'), self.result_path)
-
-	def ren_day(self):
-		if self.day:
-			day_name = self.day['name']
-			self.probs = list(self.day.probs())
-		else:
-			day_name = u'测试'
-			self.probs = [self.prob]
-		if len(self.probs) == 0:
-			log.info(u'指定目录`%s`下没有题目可渲染。' % (self.day.path if self.day else self.conf.path))
-			return
-		self.tex_problems = []
-		for self.prob in self.probs:
-			self.ren_prob_md_j()
-			self.tex_problems.append(self.ren_prob_tex())
-		self.ren_day_pdf()
-		self.start_file()
-
-	def main(self):
-		self.ren_prec()
-		self.day_template = self.day_templates[self.comp]
-		if self.conf.folder != 'problem':
-			for self.day in base.days():
-				self.result_path = pjoin('statements', self.comp, self.day.name_lang() + '.pdf')
-				self.ren_day_prec()
-				self.ren_day()
-		else:
-			self.result_path = pjoin('statements', self.comp, self.conf.name_lang() + '.pdf')
-			self.ren_day()
-
-class Markdown(Base):
-	work = 'md'
-	def ren_prob_rest(self):
-		table_suf = 'html' if self.comp != 'loj' else 'md'
-		result_md = get_template('problem.md', self.prob.lang()).render(
-			self.context,
-			template = lambda temp_name, **context : get_template(temp_name + '.html.jinja', self.prob.lang()).render(context),
-			table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.'+ table_suf +'.jinja', self.context, options)
-		).encode('utf-8')
-		if self.comp == 'uoj':
-			result_md = uoj_title(result_md)
-		elif self.comp in {'loj', 'ipuoj'}:
-			result_md = loj_bug(result_md)
-		open(self.result_path, 'wb').write(result_md)
-
-class Html(Base):
-	work = 'html'
-	def check_install(self):
-		base.check_install('pandoc')
-
-	def ren_prob_rest(self):
-		if self.comp == 'tsinsen-oj':
-			with open(pjoin('tmp', 'problem.2.md'), 'wb') as f:
-				for line in open(pjoin('tmp', 'problem.md'), 'rb'):
-					if re.match(b'^##[^#]', line):
-						line = (u'## 【%s】\n' % line[2:].strip().decode('utf-8')).encode('utf-8')
-					f.write(line)
-		else:
-			base.copy('tmp', 'problem.md', pjoin('tmp', 'problem.2.md'))
-		txt = open(pjoin('tmp', 'problem.2.md'), 'rb').read().decode('utf-8')
-		for key, val in self.secondary_dict.items():
-			txt = txt.replace(key, '{{ ' + val + ' }}')
-		open(pjoin('tmp', 'problem.3.md'), 'wb').write(
-			txt.encode('utf-8')
-		)
-		open(base.pjoin('tmp', 'problem.4.md'), 'wb') \
-			.write(get_template('problem.3.md', self.prob.lang())
-				.render(
-					self.context,
-					template = lambda temp_name, **context : get_template(temp_name + '.html.jinja', self.prob.lang()).render(context),
-					table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.html.jinja', self.context, options)
-				).encode('utf-8')
-			)
-		os.system('pandoc %s -o %s' % (
-			pjoin('tmp', 'problem.4.md'),
-			self.result_path
-		))
-
-class DoKuWiki(Base):
-	work = 'doku'
-	def check_install(self):
-		base.check_install('pandoc')
-
-	def ren_prob_rest(self):
-		os.system('pandoc %s -o %s -w dokuwiki' % (
-			pjoin('tmp', 'problem.md'),
-			pjoin('tmp', 'problem.doku')
-		))
-		txt = open(pjoin('tmp', 'problem.doku'), 'rb').read().decode('utf-8')
-		for key, val in self.secondary_dict.items():
-			txt = txt.replace(key, '{{ ' + val + ' }}')
-		open(pjoin('tmp', 'problem.2.doku'), 'wb').write(
-			txt.encode('utf-8')
-		)
-		open(self.result_path, 'wb') \
-			.write(get_template('problem.2.doku', self.prob.lang())
-				.render(
-					self.context,
-					template = lambda temp_name, **context : '<HTML>' + get_template(temp_name + '.html.jinja', self.prob.lang()).render(context) + '</HTML>',
-					table = lambda name, options = None : '<HTML>' + table(pjoin(self.prob.path, 'tables'), name, 'table.html.jinja', self.context, options).strip() + '</HTML>'
-				).encode('utf-8')
-			)
-
-class_list = {
-	'ccpc' : Latex,
-	'uoj' : Markdown,
-	'tupc' : Latex,
-	'tuoi' : Latex,
-	'noi' : Latex,
-	'tuoj' : Markdown,
-	'ccc-tex' : Latex,
-	'ccc-md' : Markdown,
-	'tsinsen-oj' : Html,
-	'loj' : Markdown,
-	'ipuoj' : Markdown,
-	'thuoj' : DoKuWiki,
-	'hand' : Latex
-}
-
-comp_list = {
-	'ccpc' : 'ccpc',
-	'uoj' : 'uoj',
-	'tupc' : 'tupc',
-	'tuoi' : 'tuoi',
-	'noi' : 'noi',
-	'tuoj' : 'tuoj',
-	'ccc-tex' : 'ccc',
-	'ccc-md' : 'ccc',
-	'tsinsen-oj' : 'tsinsen-oj',
-	'loj' : 'loj',
-	'ipuoj' : 'ipuoj',
-	'thuoj' : 'thuoj',
-	'hand' : 'hand'
-}
-
-if __name__ == '__main__':
-	try:
-		if base.init():
-			base.check_install('jinja2')
-			for base.work in base.works:
-				for base.lang in base.langs:
-					base.run_exc(class_list[base.work](comp_list[base.work]).run)
-		else:
-			log.info(u'这个工具用于渲染题面。')
-			log.info(u'支持的工作：%s' % ','.join(sorted(class_list.keys())))
-	except base.NoFileException as e:
-		log.error(e)
-		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+import platform
+import gettext
+import yaml
+from . import base
+from .base import log, pjoin
+try:
+	import jinja2
+except:
+	pass
+from . import tools
+import uuid
+import traceback
+
+work_class = {
+	'noi' : {'noi'},
+	'ccpc' : {'ccpc'},
+	'uoj' : {'uoj'},
+	'loj' : {'loj'},
+	'ipuoj' : {'ipuoj'},
+	'tupc' : {'tupc'},
+	'tuoj-pc' : {'tupc', 'tuoj'},
+	'tuoi' : {'tuoi'},
+	'tuoj-oi' : {'tuoi', 'tuoj'},
+	'tuoj' : {'tuoj'},
+	'thuoj' : {'thuoj'},
+	'hand' : {'hand'},
+	'ccc' : {'ccc-tex', 'ccc-md'},
+	'ccc-tex' : {'ccc-tex'},
+	'ccc-md' : {'ccc-md'},
+	'tsinsen-oj' : {'tsinsen-oj'},
+	'tex' : {'noi', 'ccpc', 'tupc', 'tuoi', 'ccc-tex', 'hand'},
+	'md' : {'uoj', 'tuoj', 'ccc-md', 'loj', 'ipuoj'},
+	'html' : {'tsinsen-oj'},
+	'doku' : {'thuoj'},
+	'syzoj_like' : {'loj', 'ipuoj'}
+}
+io_styles = {
+	'noi' : 'fio',
+	'ccpc' : 'stdio',
+	'uoj' : 'stdio',
+	'tuoj' : 'stdio',
+	'ccc' : 'stdio',
+	'tuoi' : 'stdio',
+	'tupc' : 'stdio',
+	'tsinsen-oj' : 'stdio',
+	'loj' : 'stdio',
+	'ipuoj' : 'stdio',
+	'thuoj' : 'stdio',
+	'hand' : 'stdio'
+}
+base_templates = {
+	'noi' : 'tuoi',
+	'tuoi' : 'tuoi',
+	'tupc' : 'tupc',
+	'ccpc' : 'ccpc',
+	'ccc' : 'ccc',
+	'hand' : 'hand'
+}
+
+secondary_dict = {}
+env = None
+pandoc_version = None
+
+def detect_pandoc_version():
+	global pandoc_version
+	if pandoc_version is not None:
+		return
+	cp = subprocess.Popen(['pandoc', '-v'], stdout = subprocess.PIPE)
+	line = cp.stdout.read().decode().splitlines()[0]
+	pandoc_version = line.split()[-1]
+
+def get_pandoc_option():
+	detect_pandoc_version()
+	if pandoc_version.startswith('2.'):
+		option = '--listings -f markdown-smart -t latex-smart'
+	else:
+		option = '--no-tex-ligatures --listings -t latex'
+	return option
+
+def get_template(fname, lang = None):
+	global env
+	if base.lang:
+		lang = base.lang
+	if not lang:
+		lang = 'zh-cn'
+	if env == None or base.system == 'Darwin' or (lang and env['lang'] != lang):
+		env = {
+			'env' : jinja2.Environment(
+				loader = jinja2.FileSystemLoader(pjoin(os.getcwd(), 'tmp')),
+				extensions = ['jinja2.ext.do', 'jinja2.ext.i18n']
+			),
+			'lang' : lang
+		}
+		try:
+			tra = gettext.translation('lang', os.getcwd() + '/tmp', [env['lang']])
+			env['env'].install_gettext_translations(tra)
+		except FileNotFoundError as e:
+			log.warning(u'没有%s这种语言的翻译表可用。' % lang)
+	return env['env'].get_template(fname)
+
+def table(path, name, temp, context, options):
+	if options == None:
+		options = {}
+	for suf in ['.py', '.pyinc', '.json', '.yaml', '.yml']:
+		try:
+			base.copy(path, name + suf, pjoin('tmp', 'table' + suf))
+			log.info(u'渲染表格`%s`，参数%s' % (base.pjoin(path, name + suf), str(options)))
+			break
+		except base.NoFileException as e:
+			pass
+	else:
+		raise base.NoFileException(u'找不到表格`%s.*`' % base.pjoin(path, name))
+	def merge_ver(table, titled = None):
+		if titled is not None:
+			options['titled'] = titled
+		return table
+	def merge(table):
+		titled = options.get('titled', True)
+		ret = [row for row in table]
+		last = ret[-1]
+		for i in range(len(table) - 2, -1, -1):
+			for j in range(len(last)):
+				cur = ret[i][j]
+				if type(cur) == tuple:
+					cur = cur[0]
+				las = last[j]
+				if type(las) == tuple:
+					las, opt = las
+				else:
+					opt = {}
+				if (not titled or i != 0) and las == cur and not opt.get('no_merge') and options.get('merge') != False:
+					last[j] = None
+				if (opt.get('no_merge') or options.get('merge') == False) and context.get('comp') in work_class['syzoj_like']:
+					last[j] = str(las) + f"<!--{ uuid.uuid4() }-->"
+			last = ret[i]
+		return ret
+	if suf == '.json':
+		res = get_template('table.json', context['prob'].lang()).render(context, options = options)
+		try:
+			table = json.loads(res)
+		except Exception as e:
+			open(pjoin('tmp', 'table.tmp.json'), 'w').write(res)
+			log.error(u'json文件错误`tmp/table.tmp.json`')
+			raise e
+		os.remove(pjoin('tmp', 'table.json'))
+	elif suf == '.yaml' or suf == '.yml':
+		try:
+			table = yaml.full_load(open(base.pjoin('tmp', 'table' + suf), 'rb').read().decode('utf-8'))
+		except Exception as e:
+			open(pjoin('tmp', 'table.tmp.json'), 'w').write(res)
+			log.error(u'json文件错误`tmp/table.tmp.json`')
+			raise e
+	elif suf == '.py' or suf == '.pyinc':
+		no_merge = lambda item : (item, {'no_merge' : True})
+		code = 'def render(context, options, merge_ver, no_merge):\n'
+		code += '\tglobal val\n'
+		code += '\tfor key, val in context.items():\n'
+		code += '\t\texec(\'%s = val\' % key, globals())\n'
+		for line in open(base.pjoin('tmp', 'table' + suf), 'rb'):
+			code += '\t' + line.decode('utf-8').rstrip() + '\n'
+		namespace = {}
+		exec(code, namespace)
+		try:
+			table = namespace['render'](context, options, merge_ver, no_merge)
+		except Exception as e:
+			log.error(e)
+			lines = traceback.format_exc().splitlines()
+			for idx, line in enumerate(lines):
+				if '<string>' in line:
+					m = re.match(r'^.*line (\d*),.*$', line)
+					if m:
+						lineno = int(m.group(1)) - 4
+						log.info('  File "%s", line %d' % (base.pjoin(path, name + suf), lineno))
+						log.info(code.splitlines()[lineno + 3][1:])
+						for i in range(idx + 1, len(lines)):
+							log.info(lines[i])
+						break
+			else:
+				raise e
+			raise e
+	table = merge(table)
+	table = json.loads(json.dumps(table))
+	if context.get('comp') in work_class['syzoj_like'] and len(table) > 0:
+		last_line = [None] * len(table[0])
+		for i in range(len(table)):
+			for j in range(len(table[i])):
+				if table[i][j] == None:
+					table[i][j] = last_line[j]
+				else:
+					last_line[j] = table[i][j]
+	cnt = [[1] * len(row) for row in table]
+	max_len = len(table[-1])
+	for i in range(len(table) - 2, -1, -1):
+		max_len = max(max_len, len(table[i]))
+		for j in range(min(len(table[i]), len(table[i + 1]))):
+			if table[i + 1][j] == None:
+				cnt[i][j] += cnt[i + 1][j]
+	ret = get_template(temp, context['prob'].lang()).render(context, table = table, cnt = cnt, width = max_len, options = options)
+	return ret
+
+def to_arg(dic):
+	return ','.join(['%s = %s' % (key, val if type(val) != str else json.dumps(val)) for key, val in dic.items()])
+
+def uoj_title(text):	## 很显然，这个是在瞎整，不过UOJ为什么从二级标题开始用？修改标题字体大小应该改CSS而不是题目嘛
+	in_quote = 0
+	result = []
+	for line in text.split(b'\n'):
+		if in_quote == 0 and line.startswith(b'#'):
+			result.append(b'#' + line)
+		else:
+			result.append(line)
+		in_quote ^= line.count(b'```') & 1
+	return b'\n'.join(result)
+	
+def loj_bug(text):		## 学弟也学着我瞎整，伤心QAQ
+	# TODO: Avoid duplication
+	in_quote = 0
+	result = []
+	for line in text.split(b'\n'):
+		if in_quote == 0 and line.startswith(b'<table'):
+			result.append(line
+				.replace(b'$<', b'$ <')   # LOJ Markdown 渲染的已知 bug
+			)
+		else:
+			result.append(line)
+		in_quote ^= line.count(b'```') & 1
+	return b'\n'.join(result)
+
+class Base(object):
+	def __init__(self, comp, conf = None):
+		self.conf = (base.conf if conf == None else conf)
+		self.comp = comp
+		self.day = None
+		self.contest = None
+		self.prob = None
+		self.path = None
+		self.prec = None
+		self.secondary_dict = {}
+		self.io_style = io_styles[comp]
+
+	def file_name(self, name):
+		if self.comp == 'noi':
+			return self.prob['name'] + '/' + name
+		elif self.comp == 'uoj':
+			return name
+		else:
+			return name
+
+	def secondary(self, s, sp = None):
+		if sp != None:
+			if type(sp) == str:
+				sp = [sp]
+			in_set = False
+			for i in sp:
+				if i in work_class and base.work in work_class[i]:
+					in_set = True
+					break
+			if not in_set:
+				return ''
+		if self.work == 'tex' or self.work == 'html' or self.work == 'doku':
+			id = str(uuid.uuid4())
+			self.secondary_dict[id] = s
+			return id
+		else:
+			return ' {{ ' + s + ' }} '
+
+	def resource(self, name):
+		if self.comp in work_class['syzoj_like'] and self.prob.get('pid', {}).get(self.comp + '-default'):
+			return '/../problem/show_image/%d/' % self.prob.get('pid', {}).get(self.comp + '-default') + name
+		return self.prob['name'] + '/' + name
+		
+	def down_file(self, name):
+		ret = ''
+		fname = pjoin(self.prob.path, 'down', name)
+		length_warned = False
+		for idx, line in enumerate(open(fname, 'rb')):
+			if len(line) > 60 and not length_warned:
+				log.warning(u'文件`%s`的第%d行太长，建议只提供下发而不渲染到题面。' % (fname, idx + 1))
+				length_warned = True
+			ret += line.decode('utf-8')
+		return ret
+
+	def hide_file(self, name):
+		ret = ''
+		fname = pjoin(self.prob.path, 'hide', name)
+		length_warned = False
+		for idx, line in enumerate(open(fname, 'rb')):
+			if len(line) > 60 and not length_warned:
+				log.warning(u'文件`%s`的第%d行太长，建议只提供下发而不渲染到题面。' % (fname, idx + 1))
+				length_warned = True
+			ret += line.decode('utf-8')
+		if self.comp not in work_class['tex']:
+			if ret < 20:
+				return u'隐藏内容'
+			c = len(ret) // 20
+			ret =  ret[:c] + u'……隐藏内容……' + ret[-c:]
+		return ret
+		
+	def titlize(self, title, args, lang = None):
+		if base.lang:
+			lang = base.lang
+		if not lang:
+			lang = 'zh-cn'
+		if title == 'sample':
+			if len(args) > 0:
+				self.context['vars']['sample_id'] = args[0]
+			if len(args) <= 1:
+				return ''
+		tra = gettext.translation('lang', os.getcwd() + '/tmp', [env['lang']])
+		ret = tra.gettext(title)
+		if len(args) > 0:
+			try:
+				ret = ret % args
+			except Exception as e:
+				ret = ret + ''.join(map(str, args))
+		else:
+			try:
+				ret = ret % ('',)
+			except Exception as e:
+				pass
+		return '## ' + ret
+
+	def ren_prob_md_j(self):
+		time.sleep(0.5)
+		log.info(u'渲染题目题面 %s %s' % (self.comp, self.prob.route))
+		try:
+			shutil.copy(self.prob.statement(), pjoin('tmp', 'problem.md.jinja'))
+			time.sleep(0.1)
+		except base.NoFileException as e:
+			log.error(u'找不到题面文件，建议使用`python -m tuack.gen problem`生成题目工程。')
+			return
+		self.context = {
+			'prob' : self.prob,
+			'args' : self.prob.get('args'),
+			'data' : self.prob.get('data'),
+			'samples' : self.prob.get('samples'),
+			'pre' : self.prob.get('pre'),
+			'dargs' : tools.a(self.prob.get('data')),
+			'pargs' : tools.a(self.prob.get('pre')),
+			'sargs' : tools.a(self.prob.get('samples')),
+			'aargs' : tools.a(self.prob, self.prob.get('data'), self.prob.get('pre'), self.prob.get('samples'), [self.prob]),
+			'day' : self.day,
+			'contest' : self.contest,
+			'io_style' : self.io_style,
+			'comp' : self.comp,
+			'tools' : tools,
+			'tl' : tools,
+			'base' : base,
+			'common' : base,
+			'file_name' : self.file_name,
+			'down_file' : self.down_file,
+			'resource' : self.resource,
+			'render' : self.secondary,
+			'precautions' : self.prec,
+			'json' : json,
+			'vars' : {},
+			's' : lambda title, *args : self.titlize(title, args, self.prob.lang()),
+			'input_file_name': None,
+			'output_file_name': None,
+			'work_class' : work_class,
+			'noi_pas_c': base.noi_pas_c
+		}
+		if self.prob.get('file io'):
+			self.context['input_file_name'] = self.prob.get('input_table', {}).get('zh-cn', self.prob['name'] + '.in')
+			self.context['output_file_name'] = self.prob.get('output_table', {}).get('zh-cn', self.prob['name'] + '.out')
+		self.context['img'] = lambda src, env = None, **argw : self.context['render'](
+			"template('image', resource = resource(%s), %s)" % (json.dumps(src), to_arg(argw)),
+			env
+		)
+		self.context['font'] = lambda txt, env = None, **argw : self.context['render'](
+			"template('font', txt = %s, %s)" % (json.dumps(txt), to_arg(argw)),
+			env
+		)
+		self.context['tbl'] = lambda src, env = None, **argw : self.context['render'](
+			"table(%s, %s)" % (json.dumps(src), argw),
+			env
+		)
+		if self.comp == 'tsinsen-oj' and 'tsinsen_files' in dir(self.prob):
+			self.context['resource'] = lambda name : '/RequireFile.do?fid=%s' % self.prob.tsinsen_files[name]
+		open(pjoin('tmp', 'problem.md'), 'wb') \
+			.write(get_template('problem_base.md.jinja', self.prob.lang())
+				.render(self.context)
+				.encode('utf-8')
+			)
+		time.sleep(0.1)
+
+	def check_install(self):
+		pass
+
+	def before(self):
+		base.mkdir('statements')
+		shutil.rmtree('tmp', ignore_errors = True)
+		time.sleep(0.1)
+		shutil.copytree(pjoin(base.path, 'templates'), 'tmp')
+		base.mkdir(pjoin('statements', self.comp))
+		if self.conf.folder == 'contest':
+			self.contest = self.conf
+		elif self.conf.folder == 'day':
+			self.day = self.conf
+		elif self.conf.folder == 'problem':
+			self.prob = self.conf
+
+	def move_resource(self):
+		if os.path.exists(pjoin(self.prob.path, 'resources')):
+			shutil.rmtree(self.path, ignore_errors = True)
+			time.sleep(0.1)
+			shutil.copytree(pjoin(self.prob.path, 'resources'), (self.path if self.prob.route != '' else pjoin(self.path, self.prob['name'])))
+
+	def gen_paths(self):
+		self.path = pjoin('statements', self.comp)
+		if self.prob.route != '':
+			self.path = pjoin(self.path, self.prob.route)
+		self.result_path = self.path + ('-' + base.lang if base.lang else '')
+		if self.prob.route == '':
+			self.result_path = pjoin(self.result_path, self.prob['name'])
+		self.result_path += '.' + self.work
+
+	def main(self):
+		if self.conf.folder == 'contest':
+			for self.day in self.conf.days():
+				if not os.path.exists(pjoin('statements', self.comp, self.day.route)):
+					os.makedirs(pjoin('statements', self.comp, self.day.route))
+		if self.comp == 'tsinsen-oj':
+			log.warning(u'如果你使用了resource，你可能需要使用dumper才能获得正确上传清橙的文件。')
+		for self.prob in self.conf.probs():
+			self.gen_paths()
+			self.move_resource()
+			self.ren_prob_md_j()
+			self.ren_prob_rest()
+			self.start_file()
+
+	def final(self):
+		shutil.rmtree('tmp', ignore_errors = True)
+
+	def run(self):
+		self.check_install()
+		self.before()
+		self.main()
+		self.final()
+
+	def start_file(self):
+		if base.start_file:
+			base.xopen_file(self.result_path)
+
+class Latex(Base):
+	work = 'tex'
+	day_templates = {
+		'noi' : 'tuoi',
+		'tuoi' : 'tuoi',
+		'tupc' : 'tupc',
+		'ccpc' : 'ccpc',
+		'ccc' : 'ccc',
+		'hand' : 'hand'
+	}
+
+	def resource(self, name):
+		return pjoin('..', self.prob.path, 'resources', name).replace('\\', '/')
+
+	def check_install(self):
+		base.check_install('pandoc')
+		base.check_install('xelatex')
+		base.check_install('gettext')
+
+	def ren_prec(self):
+		if not os.path.exists(base.pjoin(self.conf.path, 'precautions', 'zh-cn.md')):
+			return
+		context = {
+			'io_style' : self.io_style,
+			'comp' : self.comp,
+			'tools' : tools,
+			'tl' : tools,
+			'base' : base,
+			'json' : json
+		}
+		base.copy(base.pjoin(self.conf.path, 'precautions'), 'zh-cn.md', 'tmp')
+		open(base.pjoin('tmp', 'precautions.md'), 'wb') \
+			.write(get_template('zh-cn.md').render(context, conf = self.conf).encode('utf-8'))
+		os.system('pandoc %s %s -o %s' % (
+			get_pandoc_option(),
+			pjoin('tmp', 'precautions.md'),
+			pjoin('tmp', 'precautions.tex')
+		))
+		self.prec = open(pjoin('tmp', 'precautions.tex'), 'rb').read().decode('utf-8')
+
+	def ren_day_prec(self):
+		if not os.path.exists(base.pjoin(self.day.path, 'precautions', 'zh-cn.md')):
+			return
+		context = {
+			'io_style' : self.io_style,
+			'comp' : self.comp,
+			'tools' : tools,
+			'tl' : tools,
+			'base' : base,
+			'json' : json
+		}
+		base.copy(base.pjoin(self.day.path, 'precautions'), 'zh-cn.md', 'tmp')
+		open(base.pjoin('tmp', 'precautions.md'), 'wb') \
+			.write(get_template('zh-cn.md').render(context, conf = self.day).encode('utf-8'))
+		os.system('pandoc %s %s -o %s' % (
+			get_pandoc_option(),
+			pjoin('tmp', 'precautions.md'),
+			pjoin('tmp', 'precautions.tex')
+		))
+		self.prec = open(pjoin('tmp', 'precautions.tex'), 'rb').read().decode('utf-8')
+
+	def ren_prob_tex(self):
+		os.system('pandoc %s %s -o %s' % (
+			get_pandoc_option(),
+			pjoin('tmp', 'problem.md'),
+			pjoin('tmp', 'problem.tex')
+		))
+		tex = open(pjoin('tmp', 'problem.tex'), 'rb').read().decode('utf-8')
+		for key, val in self.secondary_dict.items():	## 如果未来发生了性能问题，这里可以先写到一个文件里然后再解析
+			open(pjoin('tmp', key + '.tex.jinja'), 'wb').write(
+				('{{ ' + val + ' }}').encode('utf-8')
+			)
+			ret = get_template(key + '.tex.jinja', self.prob.lang()).render(
+				self.context,
+				template = lambda temp_name, **context : get_template(temp_name + '.tex.jinja', self.prob.lang()).render(context),
+				table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.tex.jinja', self.context, options)
+			)
+			tex = tex.replace(key, ret)
+		self.secondary_dict = {}
+		return tex
+
+	def gen_compile(self):
+		clangs = {l for prob in self.probs for l in prob.get('compile', {}).keys()}
+		ret = {}
+		for clang in clangs:
+			cur = []
+			for prob in self.probs:
+				if prob['type'] != 'output':
+					if clang in prob['compile']:
+						cur.append({
+							'option' : prob['compile'][clang] + (' -Wl,--stack=%d' % prob.memory_limit().B if clang in {'cpp', 'c'} and base.out_system == 'Windows' else ''),
+							'cnt' : 1,
+							'use' : True
+						})
+					else:
+						cur.append({'option' : u'不可用', 'cnt' : 1, 'use' : False})
+				else:
+					cur.append({'option' : 'N/A', 'cnt' : 1, 'use' : False})
+			last = []
+			for p in cur:
+				if len(last) == 0 or p['option'] != last[-1]['option']:
+					last.append(p)
+				else:
+					last[-1]['cnt'] += 1
+			ret[clang] = last
+		return ret
+
+	def ren_day_pdf(self):
+		log.info(u'渲染比赛日题面 %s %s' % (self.comp, self.day.route if self.day else self.conf.route))
+		self.context.pop('prob')
+		self.context.pop('file_name')
+		self.context.pop('down_file')
+		self.context.pop('resource')
+		self.context.pop('render')
+		self.context['probs'] = self.probs
+		self.context['problems'] = self.tex_problems
+		self.context['compile'] = self.gen_compile()
+		self.context['water_mark'] = base.water_mark
+		if base.water_mark:
+			shutil.copy(base.water_mark, 'tmp/water_mark.' + base.water_mark.split('.')[-1])
+		all_problem_statement = get_template('%s.tex.jinja' % base_templates[self.comp]).render(self.context)
+		try:
+			open(pjoin('tmp', 'problems.tex'), 'wb') \
+				.write(all_problem_statement.encode('utf-8'))
+		except Exception as e:
+			log.info(u'渲染出错的文件为`tmp/problems.tmp.tex`')
+			open(pjoin('tmp', 'problems.tmp.tex'), 'wb') \
+				.write(all_problem_statement.encode('utf-8'))
+			raise e
+		log.info(u'开始使用xelatex渲染题面。')
+		os.chdir('tmp')
+		os.system('xelatex -interaction=batchmode problems.tex')
+		os.system('xelatex -interaction=batchmode problems.tex')
+		if not os.path.exists('problems.pdf'):
+			log.warning(u'题面渲染失败，尝试使用关闭静默模式渲染。')
+			os.system('xelatex problems.tex')
+			os.system('xelatex problems.tex')
+		if not os.path.exists('problems.pdf'):
+			log.error(u'题面渲染失败，请检查`tmp`目录下各文件。')
+		os.chdir('..')
+		shutil.copy(pjoin('tmp', 'problems.pdf'), self.result_path)
+
+	def ren_day(self):
+		if self.day:
+			day_name = self.day['name']
+			self.probs = list(self.day.probs())
+		else:
+			day_name = u'测试'
+			self.probs = [self.prob]
+		if len(self.probs) == 0:
+			log.info(u'指定目录`%s`下没有题目可渲染。' % (self.day.path if self.day else self.conf.path))
+			return
+		self.tex_problems = []
+		for self.prob in self.probs:
+			self.ren_prob_md_j()
+			self.tex_problems.append(self.ren_prob_tex())
+		self.ren_day_pdf()
+		self.start_file()
+
+	def main(self):
+		self.ren_prec()
+		self.day_template = self.day_templates[self.comp]
+		if self.conf.folder != 'problem':
+			for self.day in base.days():
+				self.result_path = pjoin('statements', self.comp, self.day.name_lang() + '.pdf')
+				self.ren_day_prec()
+				self.ren_day()
+		else:
+			self.result_path = pjoin('statements', self.comp, self.conf.name_lang() + '.pdf')
+			self.ren_day()
+
+class Markdown(Base):
+	work = 'md'
+	def ren_prob_rest(self):
+		table_suf = 'html' if self.comp not in work_class['syzoj_like'] else 'md'
+		result_md = get_template('problem.md', self.prob.lang()).render(
+			self.context,
+			template = lambda temp_name, **context : get_template(temp_name + '.html.jinja', self.prob.lang()).render(context),
+			table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.'+ table_suf +'.jinja', self.context, options)
+		).encode('utf-8')
+		if self.comp == 'uoj':
+			result_md = uoj_title(result_md)
+		elif self.comp in work_class['syzoj_like']:
+			result_md = loj_bug(result_md)
+		open(self.result_path, 'wb').write(result_md)
+
+class Html(Base):
+	work = 'html'
+	def check_install(self):
+		base.check_install('pandoc')
+
+	def ren_prob_rest(self):
+		if self.comp == 'tsinsen-oj':
+			with open(pjoin('tmp', 'problem.2.md'), 'wb') as f:
+				for line in open(pjoin('tmp', 'problem.md'), 'rb'):
+					if re.match(b'^##[^#]', line):
+						line = (u'## 【%s】\n' % line[2:].strip().decode('utf-8')).encode('utf-8')
+					f.write(line)
+		else:
+			base.copy('tmp', 'problem.md', pjoin('tmp', 'problem.2.md'))
+		txt = open(pjoin('tmp', 'problem.2.md'), 'rb').read().decode('utf-8')
+		for key, val in self.secondary_dict.items():
+			txt = txt.replace(key, '{{ ' + val + ' }}')
+		open(pjoin('tmp', 'problem.3.md'), 'wb').write(
+			txt.encode('utf-8')
+		)
+		open(base.pjoin('tmp', 'problem.4.md'), 'wb') \
+			.write(get_template('problem.3.md', self.prob.lang())
+				.render(
+					self.context,
+					template = lambda temp_name, **context : get_template(temp_name + '.html.jinja', self.prob.lang()).render(context),
+					table = lambda name, options = None : table(pjoin(self.prob.path, 'tables'), name, 'table.html.jinja', self.context, options)
+				).encode('utf-8')
+			)
+		os.system('pandoc %s -o %s' % (
+			pjoin('tmp', 'problem.4.md'),
+			self.result_path
+		))
+
+class DoKuWiki(Base):
+	work = 'doku'
+	def check_install(self):
+		base.check_install('pandoc')
+
+	def ren_prob_rest(self):
+		os.system('pandoc %s -o %s -w dokuwiki' % (
+			pjoin('tmp', 'problem.md'),
+			pjoin('tmp', 'problem.doku')
+		))
+		txt = open(pjoin('tmp', 'problem.doku'), 'rb').read().decode('utf-8')
+		for key, val in self.secondary_dict.items():
+			txt = txt.replace(key, '{{ ' + val + ' }}')
+		open(pjoin('tmp', 'problem.2.doku'), 'wb').write(
+			txt.encode('utf-8')
+		)
+		open(self.result_path, 'wb') \
+			.write(get_template('problem.2.doku', self.prob.lang())
+				.render(
+					self.context,
+					template = lambda temp_name, **context : '<HTML>' + get_template(temp_name + '.html.jinja', self.prob.lang()).render(context) + '</HTML>',
+					table = lambda name, options = None : '<HTML>' + table(pjoin(self.prob.path, 'tables'), name, 'table.html.jinja', self.context, options).strip() + '</HTML>'
+				).encode('utf-8')
+			)
+
+class_list = {
+	'ccpc' : Latex,
+	'uoj' : Markdown,
+	'tupc' : Latex,
+	'tuoi' : Latex,
+	'noi' : Latex,
+	'tuoj' : Markdown,
+	'ccc-tex' : Latex,
+	'ccc-md' : Markdown,
+	'tsinsen-oj' : Html,
+	'loj' : Markdown,
+	'ipuoj' : Markdown,
+	'thuoj' : DoKuWiki,
+	'hand' : Latex
+}
+
+comp_list = {
+	'ccpc' : 'ccpc',
+	'uoj' : 'uoj',
+	'tupc' : 'tupc',
+	'tuoi' : 'tuoi',
+	'noi' : 'noi',
+	'tuoj' : 'tuoj',
+	'ccc-tex' : 'ccc',
+	'ccc-md' : 'ccc',
+	'tsinsen-oj' : 'tsinsen-oj',
+	'loj' : 'loj',
+	'ipuoj' : 'ipuoj',
+	'thuoj' : 'thuoj',
+	'hand' : 'hand'
+}
+
+if __name__ == '__main__':
+	try:
+		if base.init():
+			base.check_install('jinja2')
+			for base.work in base.works:
+				for base.lang in base.langs:
+					base.run_exc(class_list[base.work](comp_list[base.work]).run)
+		else:
+			log.info(u'这个工具用于渲染题面。')
+			log.info(u'支持的工作：%s' % ','.join(sorted(class_list.keys())))
+	except base.NoFileException as e:
+		log.error(e)
+		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
```

### Comparing `tuack-0.1.4.9.2/tuack/sample/arbiter_e.sample` & `tuack-0.1.5/tuack/sample/arbiter_e.noi_linux1.sample`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/sample-problem/resources/sample.png` & `tuack-0.1.5/tuack/sample-problem/resources/sample.png`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/sample-problem/solution/zh-cn.md` & `tuack-0.1.5/tuack/sample-problem/solution/zh-cn.md`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,28 +1,28 @@
-{{ self.title() }}
-
-作者，版权声明等
-
-## 题目简述
-
-可以把题目的要点再说一遍。
-
-## 子任务设计
-
-如果有的话，也许需要解释一下部分分都是怎么设计的。
-
-## 算法1：暴力
-
-列举一下常见的不推荐写法：
-
-| 不推荐写法          | 推荐写法                                    | 解释                                       |
-| -------------- | --------------------------------------- | ---------------------------------------- |
-| $O(n^3)$       | $O\left(n^3 \right)$                    | 长得比较高的括号里的东西，要告诉括号把高出来的部分括进去             |
-| $log(n)$       | $\log{n}$                               | `log` 是有专门的正体符号，不要用斜体的变量格式               |
-| $max$          | $\max$                                  | 同上                                       |
-| $a~mod~Q$      | $a\bmod Q$                              | 我们常用的 `mod` 是 `\bmod`                    |
-| $O(n*m/32)$    | $O\left(\frac{nm}{w}\right)$，其中 $w$ 是字长 | 大O的常数是忽略的，没有意义；这么写容易误导人在O里面写常数；星号不是乘号，可以不写或用 `\times` 或 `\cdot` |
-| 第k(k<j)个       | 第 $k$（$k<j$）个                           | 数学表达式应当用表达式，行文中的标点符号（这里是表解释的圆括号）要统一用中文标点（也可以像数学书上统一用英文标点） |
-| $d[a[i][b[j]]$ | $d\left(a_i, b_j\right)$                | 方括号表下标比较少见，一般用圆括号和下标                     |
-| $a~xor~b$      | $a~\mathrm{xor}~b$                      | 不存在的算符可以用 `\mathrm{}` 造出来                |
-| 输出“Yes”（不包含引号） | 输出 `Yes`                                | 字符串有专门的格式可以用，不用使用引号加正文                   |
-
+{{ self.title() }}
+
+作者，版权声明等
+
+## 题目简述
+
+可以把题目的要点再说一遍。
+
+## 子任务设计
+
+如果有的话，也许需要解释一下部分分都是怎么设计的。
+
+## 算法1：暴力
+
+列举一下常见的不推荐写法：
+
+| 不推荐写法          | 推荐写法                                    | 解释                                       |
+| -------------- | --------------------------------------- | ---------------------------------------- |
+| $O(n^3)$       | $O\left(n^3 \right)$                    | 长得比较高的括号里的东西，要告诉括号把高出来的部分括进去             |
+| $log(n)$       | $\log{n}$                               | `log` 是有专门的正体符号，不要用斜体的变量格式               |
+| $max$          | $\max$                                  | 同上                                       |
+| $a~mod~Q$      | $a\bmod Q$                              | 我们常用的 `mod` 是 `\bmod`                    |
+| $O(n*m/32)$    | $O\left(\frac{nm}{w}\right)$，其中 $w$ 是字长 | 大O的常数是忽略的，没有意义；这么写容易误导人在O里面写常数；星号不是乘号，可以不写或用 `\times` 或 `\cdot` |
+| 第k(k<j)个       | 第 $k$（$k<j$）个                           | 数学表达式应当用表达式，行文中的标点符号（这里是表解释的圆括号）要统一用中文标点（也可以像数学书上统一用英文标点） |
+| $d[a[i][b[j]]$ | $d\left(a_i, b_j\right)$                | 方括号表下标比较少见，一般用圆括号和下标                     |
+| $a~xor~b$      | $a~\mathrm{xor}~b$                      | 不存在的算符可以用 `\mathrm{}` 造出来                |
+| 输出“Yes”（不包含引号） | 输出 `Yes`                                | 字符串有专门的格式可以用，不用使用引号加正文                   |
+
```

### Comparing `tuack-0.1.4.9.2/tuack/sample-problem/statement/zh-cn.md` & `tuack-0.1.5/tuack/sample-problem/statement/zh-cn.md`

 * *Files 21% similar despite different names*

```diff
@@ -1,134 +1,136 @@
-{{ self.title() }}
-
-{{ s('background') }}
-
-这样的子标题会被程序自动处理，可以方便翻译和提取每个部分等。如果你想自己定义子标签（尽管我们一般**不推荐**自己定义 s 标签），或者不需要国际化的话，你可将这些子标题直接写成这样：
-
-```
-{{ s('如何使用交互库') }}
-### 对于使用C/C++的选手
-```
-
-If you want an English statement file, just copy this file as *en.md* and replace any Chinese text into English.
-
-更加详细的题目书写文档在[这里](https://git.thusaac.org/publish/tuack/wikis/%E9%A2%98%E9%9D%A2%E7%9A%84%E4%B9%A6%E5%86%99)。
-
-如果你不需要某些章节，可以直接删除。比如这一段是“题目背景”，很多题目其实并不需要这一段。
-
-子标题请**不要**自己手动加方括号 `【】` 。
-
-{{ s('description') }}
-
-**要强调的东西**这么写。一般只有 *file_name* 使用斜体，不用斜体表强调。
-
-行内的公式：$\sin \left(a x + b \right)$。注意使用规范的公式书写方式，例如一些常见错误的正确写法为：
-
-```
-\sin	#有斜杠
-\log
-\max
-\bmod	#最常用的取模是bmod
-a~\mathrm{xor}~b	#不存在的算符可以这么造
-O\left(\frac{nm}{w}\right)
-#用left和right把括号变高以括住比较高的式子
-#不要用*和/表示乘除号，而用省略乘号、\times、\cdot和\div、分数表示
-d\left(a_i, b_j\right)	#多用括号和下标表示下标和参数，尽量不用方括号
-```
-
-行间的公式：
-$$
-\frac{-b\pm\sqrt{b^2-4ac} }{2a}
-$$
-
-1. 第一点
-2. 第二点
-
-* 第一点
-* 第二点
-
-字符串或代码 `This is a string`，文件名是斜体，代码是字符串。注意英文、字符串、公式和中文之间要**加一个空格**，和标点符号之间不加空格。注意按照《[标点符号用法](http://www.moe.gov.cn/ewebeditor/uploadfile/2015/01/13/20150113091548267.pdf)》（教育部国标 GB/T 15834-2011）使用标点符号，注意不要有**错别字**、**语病**。
-
-成块的代码、数据这么写：
-
-```
-int main(int argc, char** argv);
-```
-
-除公式内可以使用 tex 的部分语法外，不要直接使用任何 html 语法和 tex 语法。替代方案如下：
-
-不要用 markdown 自带的语法插入图片（因为目前支持不好），用下列语法插入图片：
-
-{{ img('sample.png', size = 0.5, align = 'middle', inline = False, caption='图片样例', label='fig:sample') }}
-
-其中 `inline` 为 `False` 表示这是一个独占一行的图片，此时支持 `align`，选项为 `left`，`middle` 或 `right`。后面这些参数可以不写。如果添加了 `caption` 字段，则对于 tex 的渲染结果，会在图片下方出现类似于“图1：图片样例”字样。
-
-图片需要保存在试题目录的 `resources` 子目录下。
-
-如果有本工具不能提供的功能，需要直接使用 tex 或 html 代码的，请使用下列方式以免另外一种格式下出错。（注意代码不要放在```中）
-
-```python
-{{ render(json.dumps('\\clearpage'), 'tuoi') }}
-{{ render(json.dumps('<a href="http://oj.thusaac.org">TUOJ</a>'), 'html') }}
-```
-
-上述第一个例子是为了排版好看强行加入一个分页符的意思，其中 `tuoi` 表示只在生成 TUOI 风格题面的时候使用这个；第二个例子是在生成任何 html 格式题目的时候加入一个广告（雾）。
-
-可选的参数有 `html`，`md`，`tex`，`noi`，`uoj`，`ccpc`，`ccc`，`tuoj`，`ccc-tex`，`ccc-md`，`tuoi`，`tupc`。参数可以有多个，写成一个数组即可，例如 `['tuoi', 'noi']`。
-
-**不要在题面里直接写tex或html代码！**
-
-{{ s('input format') }}
-
-{{ self.input_file() }}
-
-上面会根据具体的评测环境说明输入是文件还是标准输入等。
-
-输入的第一行包含一个正整数 $n$，保证 $n \le {{ tl.hn(args['n']) }}$。←这是引用 *conf.yaml* 中的 `args` 的 `n` 项，然后用“好看”的格式输出。“好看”的格式如 `10^9`，`1,000,000,007`。
-
-引用 *conf.yaml* 的方法是使用变量 `prob`，例如可以写成 `prob.args['n']`，还可以写成 `prob['args']['n']`。引用 `args` 项、`data` 项、`samples` 项和 `pre` 项可以简写成例如 `args['n']` 或 `args.n`。在下文的表格中也一样。
-
-输入的第二行包含一个正整数 $m$，保证 $m \le {{ tl.hn(aargs.max('m')) }}$。
-
-↑`aargs.min` 是取出 `data` 项、`samples` 项和 `pre` 项中的所有同名变量的最小值，类似的函数还有 `max` 和 `sum`。形如 `aargs['m']` 可以取出所有同名变量的迭代器。和 python 的 `dict` 类似，还可以用形如 `aargs.get('m', 0)` 指定“如果没有某项用什么对象补空”，`sum`、`min` 和 `max` 类似。如果只取出 `data` 项、`samples` 项或 `pre` 项中的同名函数，使用 `dargs`、`sargs` 或 `pargs`。
-
-`tl` 是 `tools` 的简写，是一组工具。除 `hn` 外，还包括内建函数如 `tl.int`，`math` 中的对象或函数如 `tl.sin`，`datetime` 中的对象或函数如 `tl.time` 类，`num2chinese` 函数（可以把数字转化成中文）。
-
-{{ s('output format') }}
-
-{{ self.output_file() }}
-
-输出一个字符串 `Yes`。出题人在写题面的时候注意**不要**写成 `“Yes”（不包含引号）`。
-
-{{ s('sample', 1) }}
-
-{{ self.sample_text() }}
-
-上面是自动读入样例 `1.in/ans`（存储在 `down` 文件夹内） 然后渲染到题面中；如果只有一组样例，则去掉 `1` 或将其替换成空串，样例仍然保存成 `1.in/ans`。上面的 `1` 可以是字符串。
-
-{{ self.title_sample_description() }}
-
-这是第一组数据的样例说明。
-
-{{ s('sample', 2) }}
-
-{{ self.sample_file() }}
-
-上面是只提示存在第二组样例，但不渲染到题面中。
-
-{{ s('subtasks') }}
-
-不要使用markdown原生的表格，使用下列方式渲染一个表格，其中表格存放在试题目录的 `tables` 子目录下。
-
-{{ tbl('data') }}
-
-{{ tbl('table', width = [1, 6]) }}
-
-原理上用一个二维的 json 表格或 python 表格存储，`null` 表示和上一行合并，不支持横向合并。建议用 python 的格式写，如例子中的 `data.pyinc`，这样可以根据数据生成；跟数据无关的表格则可以像 `table.json` 那样存储。
-
-{{ s('scoring') }}
-
-这是评分方法，如果有必要的话。
-
-{{ s('hint') }}
-
+{{ self.title() }}
+
+{{ s('background') }}
+
+这样的子标题会被程序自动处理，可以方便翻译和提取每个部分等。如果你想自己定义子标签（尽管我们一般**不推荐**自己定义 s 标签），或者不需要国际化的话，你可将这些子标题直接写成这样：
+
+```
+{{ s('如何使用交互库') }}
+### 对于使用C/C++的选手
+```
+
+If you want an English statement file, just copy this file as *en.md* and replace any Chinese text into English.
+
+更加详细的题目书写文档在[这里](https://git.thusaac.org/publish/tuack/wikis/%E9%A2%98%E9%9D%A2%E7%9A%84%E4%B9%A6%E5%86%99)。
+
+如果你不需要某些章节，可以直接删除。比如这一段是“题目背景”，很多题目其实并不需要这一段。
+
+子标题请**不要**自己手动加方括号 `【】` 。
+
+{{ s('description') }}
+
+**要强调的东西**这么写。一般只有 *file_name* 使用斜体，不用斜体表强调。
+
+行内的公式：$\sin \left(a x + b \right)$。注意使用规范的公式书写方式，例如一些常见错误的正确写法为：
+
+```
+\sin	#有斜杠
+\log
+\max
+\bmod	#最常用的取模是bmod
+a~\mathrm{xor}~b	#不存在的算符可以这么造
+O\left(\frac{nm}{w}\right)
+#用left和right把括号变高以括住比较高的式子
+#不要用*和/表示乘除号，而用省略乘号、\times、\cdot和\div、分数表示
+d\left(a_i, b_j\right)	#多用括号和下标表示下标和参数，尽量不用方括号
+```
+
+行间的公式：
+$$
+\frac{-b\pm\sqrt{b^2-4ac} }{2a}
+$$
+
+1. 第一点
+2. 第二点
+
+* 第一点
+* 第二点
+
+字符串或代码 `This is a string`，文件名是斜体，代码是字符串。注意英文、字符串、公式和中文之间要**加一个空格**，和标点符号之间不加空格。注意按照《[标点符号用法](http://www.moe.gov.cn/ewebeditor/uploadfile/2015/01/13/20150113091548267.pdf)》（教育部国标 GB/T 15834-2011）使用标点符号，注意不要有**错别字**、**语病**。
+
+成块的代码、数据这么写：
+
+```
+int main(int argc, char** argv);
+```
+
+除公式内可以使用 tex 的部分语法外，不要直接使用任何 html 语法和 tex 语法。替代方案如下：
+
+不要用 markdown 自带的语法插入图片（因为目前支持不好），用下列语法插入图片：
+
+{{ img('sample.png', size = 0.5, align = 'middle', inline = False, caption='图片样例', label='fig:sample') }}
+
+其中 `inline` 为 `False` 表示这是一个独占一行的图片，此时支持 `align`，选项为 `left`，`middle` 或 `right`。后面这些参数可以不写。如果添加了 `caption` 字段，则对于 tex 的渲染结果，会在图片下方出现类似于“图1：图片样例”字样。
+
+图片需要保存在试题目录的 `resources` 子目录下。
+
+如果有本工具不能提供的功能，需要直接使用 tex 或 html 代码的，请使用下列方式以免另外一种格式下出错。（注意代码不要放在```中）
+
+```python
+{{ render(json.dumps('\\clearpage'), 'tuoi') }}
+{{ render(json.dumps('<a href="http://oj.thusaac.org">TUOJ</a>'), 'html') }}
+```
+
+上述第一个例子是为了排版好看强行加入一个分页符的意思，其中 `tuoi` 表示只在生成 TUOI 风格题面的时候使用这个；第二个例子是在生成任何 html 格式题目的时候加入一个广告（雾）。
+
+可选的参数有 `html`，`md`，`tex`，`noi`，`uoj`，`ccpc`，`ccc`，`tuoj`，`ccc-tex`，`ccc-md`，`tuoi`，`tupc`。参数可以有多个，写成一个数组即可，例如 `['tuoi', 'noi']`。
+
+**不要在题面里直接写tex或html代码！**
+
+{{ s('input format') }}
+
+{{ self.input_file() }}
+
+上面会根据具体的评测环境说明输入是文件还是标准输入等。
+
+输入的第一行包含一个正整数 $n$，保证 $n \le {{ tl.hn(args['n']) }}$。←这是引用 *conf.yaml* 中的 `args` 的 `n` 项，然后用“好看”的格式输出。“好看”的格式如 `10^9`，`1,000,000,007`。
+
+引用 *conf.yaml* 的方法是使用变量 `prob`，例如可以写成 `prob.args['n']`，还可以写成 `prob['args']['n']`。引用 `args` 项、`data` 项、`samples` 项和 `pre` 项可以简写成例如 `args['n']` 或 `args.n`。在下文的表格中也一样。
+
+输入的第二行包含一个正整数 $m$，保证 $m \le {{ tl.hn(aargs.max('m')) }}$。
+
+↑`aargs.min` 是取出 `data` 项、`samples` 项和 `pre` 项中的所有同名变量的最小值，类似的函数还有 `max` 和 `sum`。形如 `aargs['m']` 可以取出所有同名变量的迭代器。和 python 的 `dict` 类似，还可以用形如 `aargs.get('m', 0)` 指定“如果没有某项用什么对象补空”，`sum`、`min` 和 `max` 类似。如果只取出 `data` 项、`samples` 项或 `pre` 项中的同名函数，使用 `dargs`、`sargs` 或 `pargs`。
+
+`tl` 是 `tools` 的简写，是一组工具。除 `hn` 外，还包括内建函数如 `tl.int`，`math` 中的对象或函数如 `tl.sin`，`datetime` 中的对象或函数如 `tl.time` 类，`num2chinese` 函数（可以把数字转化成中文）。
+
+{{ s('output format') }}
+
+{{ self.output_file() }}
+
+输出一个字符串 `Yes`。出题人在写题面的时候注意**不要**写成 `“Yes”（不包含引号）`。
+
+{{ s('sample', 1) }}
+
+{{ self.sample_text() }}
+
+上面是自动读入样例 `1.in/ans`（存储在 `down` 文件夹内） 然后渲染到题面中；如果只有一组样例，则去掉 `1` 或将其替换成空串，样例仍然保存成 `1.in/ans`。上面的 `1` 可以是字符串。
+
+{{ self.title_sample_description() }}
+
+这是第一组数据的样例说明。
+
+{{ s('sample', 2) }}
+
+{{ self.sample_file() }}
+
+上面是只提示存在第二组样例，但不渲染到题面中。
+
+{{ s('subtasks') }}
+
+不要使用markdown原生的表格，使用下列方式渲染一个表格，其中表格存放在试题目录的 `tables` 子目录下。
+
+{{ tbl('data') }}
+
+{{ tbl('table', width = [1, 6], merge = False, titled = True) }}
+
+原理上用一个二维的 json 表格或 python 表格存储。会自动纵向合并相同的格子，如果添加了 `merge = False` 则不会合并。不支持横向合并。建议用 python 的格式写，如例子中的 `data.pyinc`，这样可以根据数据生成；跟数据无关的表格则可以像 `table.json` 那样存储。`titled` 表示在要合并的前提下，第一行是否参与合并。
+
+如果自己手动造表格，可以用 `null` 表示和上一行合并，可以用 `no_merge` 函数表示强制不合并特定的格子。
+
+{{ s('scoring') }}
+
+这是评分方法，如果有必要的话。
+
+{{ s('hint') }}
+
 这里是一个非常温馨的提示。
```

#### html2text {}

```diff
@@ -78,15 +78,20 @@
 æå°å¶æ¿æ¢æç©ºä¸²ï¼æ ·ä¾ä»ç¶ä¿å­æ `1.in/ans`ãä¸é¢ç `1`
 å¯ä»¥æ¯å­ç¬¦ä¸²ã {{ self.title_sample_description() }}
 è¿æ¯ç¬¬ä¸ç»æ°æ®çæ ·ä¾è¯´æã {{ s('sample', 2) }} {
 { self.sample_file() }}
 ä¸é¢æ¯åªæç¤ºå­å¨ç¬¬äºç»æ ·ä¾ï¼ä½ä¸æ¸²æå°é¢é¢ä¸­ã {{ s
 ('subtasks') }}
 ä¸è¦ä½¿ç¨markdownåççè¡¨æ ¼ï¼ä½¿ç¨ä¸åæ¹å¼æ¸²æä¸ä¸ªè¡¨æ ¼ï¼å¶ä¸­è¡¨æ ¼å­æ¾å¨è¯é¢ç®å½ç
-`tables` å­ç®å½ä¸ã {{ tbl('data') }} {{ tbl('table', width = [1, 6]) }}
-åçä¸ç¨ä¸ä¸ªäºç»´ç json è¡¨æ ¼æ python è¡¨æ ¼å­å¨ï¼`null`
-è¡¨ç¤ºåä¸ä¸è¡åå¹¶ï¼ä¸æ¯ææ¨ªååå¹¶ãå»ºè®®ç¨ python
+`tables` å­ç®å½ä¸ã {{ tbl('data') }} {{ tbl('table', width = [1, 6],
+merge = False, titled = True) }} åçä¸ç¨ä¸ä¸ªäºç»´ç json è¡¨æ ¼æ
+python è¡¨æ ¼å­å¨ãä¼èªå¨çºµååå¹¶ç¸åçæ ¼å­ï¼å¦ææ·»å äº
+`merge = False` åä¸ä¼åå¹¶ãä¸æ¯ææ¨ªååå¹¶ãå»ºè®®ç¨ python
 çæ ¼å¼åï¼å¦ä¾å­ä¸­ç
 `data.pyinc`ï¼è¿æ ·å¯ä»¥æ ¹æ®æ°æ®çæï¼è·æ°æ®æ å³çè¡¨æ ¼åå¯ä»¥å
-`table.json` é£æ ·å­å¨ã {{ s('scoring') }}
+`table.json` é£æ ·å­å¨ã`titled`
+è¡¨ç¤ºå¨è¦åå¹¶çåæä¸ï¼ç¬¬ä¸è¡æ¯å¦åä¸åå¹¶ã
+å¦æèªå·±æå¨é è¡¨æ ¼ï¼å¯ä»¥ç¨ `null`
+è¡¨ç¤ºåä¸ä¸è¡åå¹¶ï¼å¯ä»¥ç¨ `no_merge`
+å½æ°è¡¨ç¤ºå¼ºå¶ä¸åå¹¶ç¹å®çæ ¼å­ã {{ s('scoring') }}
 è¿æ¯è¯åæ¹æ³ï¼å¦ææå¿è¦çè¯ã {{ s('hint') }}
 è¿éæ¯ä¸ä¸ªéå¸¸æ¸©é¦¨çæç¤ºã
```

### Comparing `tuack-0.1.4.9.2/tuack/sample-problem/tables/json_data.json` & `tuack-0.1.5/tuack/sample-problem/tables/json_data.json`

 * *Ordering differences only*

 * *Files 14% similar despite different names*

```diff
@@ -1,46 +1,46 @@
-[
-	["$n, m$","测试点","$c$"]
-	{%- set last = None -%}
-	{% for datum in prob['data'] %}
-	,[
-		{%- if last and datum.args[0] == last[0] and datum.args[1] == last[1] -%}
-			null
-		{%- elif datum.args[0] == -1 and datum.args[1] == -1 -%}
-			"无约束"
-		{%- else -%}
-			"
-			{%- if datum.args[0] != -1 -%}
-				$n,m \\le {{ tools.js_hn(datum.args[0]) }}$
-			{%- endif -%}
-			{%- if datum.args[0] != -1 and datum.args[1] != -1 -%}
-				并且
-			{%- endif -%}
-			{%- if datum.args[1] != -1 -%}
-				$nm \\le {{ tools.js_hn(datum.args[1]) }}$
-			{%- endif -%}
-			"
-		{%- endif -%},"
-		{%- for i in datum['cases'] -%}
-			{{- i -}}
-			{%- if not loop.last -%}
-				,
-			{%- endif -%}
-		{%- endfor -%}",
-		{%- if last and datum.args[2] == last[2] and datum.args[3] == last[3] -%}
-			null
-		{%- else -%}"$
-			{%- if datum.args[2] == 0 -%}
-				c \\le nm
-			{%- elif datum.args[2] == 1 -%}
-				c \\le {{ tools.js_hn(datum.args[3]) }}
-			{%- elif datum.args[2] == 2 -%}
-				\\sum_{}^{}c \\le {{ tools.js_hn(datum.args[3]) }}
-			{%- elif datum.args[2] == 3 -%}
-				c = {{ tools.js_hn(datum.args[3]) }}
-			{%- endif -%}
-			$"
-		{%- endif -%}
-		{%- set last = datum['args'] -%}
-	]
-	{% endfor %}
-]
+[
+	["$n, m$","测试点","$c$"]
+	{%- set last = None -%}
+	{% for datum in prob['data'] %}
+	,[
+		{%- if last and datum.args[0] == last[0] and datum.args[1] == last[1] -%}
+			null
+		{%- elif datum.args[0] == -1 and datum.args[1] == -1 -%}
+			"无约束"
+		{%- else -%}
+			"
+			{%- if datum.args[0] != -1 -%}
+				$n,m \\le {{ tools.js_hn(datum.args[0]) }}$
+			{%- endif -%}
+			{%- if datum.args[0] != -1 and datum.args[1] != -1 -%}
+				并且
+			{%- endif -%}
+			{%- if datum.args[1] != -1 -%}
+				$nm \\le {{ tools.js_hn(datum.args[1]) }}$
+			{%- endif -%}
+			"
+		{%- endif -%},"
+		{%- for i in datum['cases'] -%}
+			{{- i -}}
+			{%- if not loop.last -%}
+				,
+			{%- endif -%}
+		{%- endfor -%}",
+		{%- if last and datum.args[2] == last[2] and datum.args[3] == last[3] -%}
+			null
+		{%- else -%}"$
+			{%- if datum.args[2] == 0 -%}
+				c \\le nm
+			{%- elif datum.args[2] == 1 -%}
+				c \\le {{ tools.js_hn(datum.args[3]) }}
+			{%- elif datum.args[2] == 2 -%}
+				\\sum_{}^{}c \\le {{ tools.js_hn(datum.args[3]) }}
+			{%- elif datum.args[2] == 3 -%}
+				c = {{ tools.js_hn(datum.args[3]) }}
+			{%- endif -%}
+			$"
+		{%- endif -%}
+		{%- set last = datum['args'] -%}
+	]
+	{% endfor %}
+]
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/ccpc.png` & `tuack-0.1.5/tuack/templates/ccpc.png`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/templates/ccpc.tex.jinja` & `tuack-0.1.5/tuack/templates/ccpc.tex.jinja`

 * *Files 18% similar despite different names*

```diff
@@ -1,67 +1,67 @@
-{% extends 'template_base.tex.jinja' %}
-
-{% block header %}
-
-\lhead{\parbox{\textwidth}{\textnormal{
-	\footnotesize \mytitle
-	\ifdefined\subtitle
-		（\subtitle）
-	\fi
-}}}
-
-\rhead{\parbox{\textwidth}{\raggedleft\textnormal{
-	\footnotesize
-	\nouppercase \leftmark
-}}}
-\chead{}
-\lfoot{}
-\cfoot{\parbox{\textwidth}{\centering \footnotesize 第 \thepage{} 页 ~~~~ 共 \pageref{LastPage} 页}}
-\rfoot{}
-
-{% endblock %}
-
-{% block cover %}
-
-\thispagestyle{Cover}
-\begin{center}
-	{\includegraphics[scale=0.35]{ccpc.png} \par}  \vskip 2em
-	\ifdefined\engtitle
-		{\hei \xiaochu \engtitle } 
-	\fi
-	\ifdefined\subtitle
-		{\hei \xiaochu \subtitle } 
-	\fi
-	\par 
-	\ifdefined\theday
-		{\kai \chuhao \theday \par} \vskip 1em 
-	\fi
-	\ifdefined\thetime
-		{\hei \sanhao \thetime \par}
-	\fi
-\end{center}
-
-\setcounter{tocdepth}{1}
-
-\tableofcontents
-
-{% endblock %}
-
-{% block statements %}
-
-{% for i in range(problems.__len__()) %}
-	\clearpage
-	\begin{center}
-		{\large \section{ 
-			{{ tools.chr(tools.ord('A') + i) }} . 
-			{{ probs[i].tr('title') }} ~~/~~ 
-			{{ probs[i]['name'].capitalize() }}
-		} }
-	\end{center}
-	
-	{{ problems[i] }}
-
-{% endfor %}
-
-{% endblock %}
-
-\end{document}
+{% extends 'template_base.tex.jinja' %}
+
+{% block header %}
+
+\lhead{\parbox{\textwidth}{\textnormal{
+	\footnotesize \mytitle
+	\ifdefined\subtitle
+		（\subtitle）
+	\fi
+}}}
+
+\rhead{\parbox{\textwidth}{\raggedleft\textnormal{
+	\footnotesize
+	\nouppercase \leftmark
+}}}
+\chead{}
+\lfoot{}
+\cfoot{\parbox{\textwidth}{\centering \footnotesize 第 \thepage{} 页 ~~~~ 共 \pageref{LastPage} 页}}
+\rfoot{}
+
+{% endblock %}
+
+{% block cover %}
+
+\thispagestyle{Cover}
+\begin{center}
+	{\includegraphics[scale=0.35]{ccpc.png} \par}  \vskip 2em
+	\ifdefined\engtitle
+		{\heiti\xiaochu \engtitle } 
+	\fi
+	\ifdefined\subtitle
+		{\heiti\xiaochu \subtitle } 
+	\fi
+	\par 
+	\ifdefined\theday
+		{\kaishu \chuhao \theday \par} \vskip 1em 
+	\fi
+	\ifdefined\thetime
+		{\heiti \sanhao \thetime \par}
+	\fi
+\end{center}
+
+\setcounter{tocdepth}{1}
+
+\tableofcontents
+
+{% endblock %}
+
+{% block statements %}
+
+{% for i in range(problems.__len__()) %}
+	\clearpage
+	\begin{center}
+		{\large \section{ 
+			{{ tools.chr(tools.ord('A') + i) }} . 
+			{{ probs[i].tr('title') }} ~~/~~ 
+			{{ probs[i]['name'].capitalize() }}
+		} }
+	\end{center}
+	
+	{{ problems[i] }}
+
+{% endfor %}
+
+{% endblock %}
+
+\end{document}
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/en/LC_MESSAGES/lang.mo` & `tuack-0.1.5/tuack/templates/en/LC_MESSAGES/lang.mo`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/templates/en/LC_MESSAGES/lang.po` & `tuack-0.1.5/tuack/templates/en/LC_MESSAGES/lang.po`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/templates/hand.tex.jinja` & `tuack-0.1.5/tuack/templates/hand.tex.jinja`

 * *Files 24% similar despite different names*

```diff
@@ -1,37 +1,37 @@
-{% extends 'template_base.tex.jinja' %}
-
-{% block cover %}
-
-\begin{center}
-	\ifdefined\theday
-		{\kai \sanhao \theday \par} \vskip 1em 
-	\fi
-\end{center}
-
-{% endblock %}
-
-{% block statements %}
-
-{% if precautions %}
-	{{ precautions }}
-{% endif %}
-
-
-{% for i in range(problems.__len__()) %}
-	
-
-{% if probs[i].lang() == 'zh-cn' %}
-	\renewcommand{\sqbr}[1]{【#1】}
-	\titleformat{\subsection}{\hei\banxiaosi}{}{1em}{\sqbr}
-{% else %}
-	\renewcommand{\sqbr}[1]{ \textbf{ #1 } }
-	\titleformat{\subsection}{\hei\sanhao}{}{0em}{\sqbr}
-{% endif %}
-
-\praragraph{ {{ probs[i].name }} }. {{ problems[i] }}
-
-{% endfor %}
-
-
-{% endblock %}
-
+{% extends 'template_base.tex.jinja' %}
+
+{% block cover %}
+
+\begin{center}
+	\ifdefined\theday
+		{\kaishu \sanhao \theday \par} \vskip 1em 
+	\fi
+\end{center}
+
+{% endblock %}
+
+{% block statements %}
+
+{% if precautions %}
+	{{ precautions }}
+{% endif %}
+
+
+{% for i in range(problems.__len__()) %}
+	
+
+{% if probs[i].lang() == 'zh-cn' %}
+	\renewcommand{\sqbr}[1]{【#1】}
+	\titleformat{\subsection}{\heiti\banxiaosi}{}{1em}{\sqbr}
+{% else %}
+	\renewcommand{\sqbr}[1]{ \textbf{ #1 } }
+	\titleformat{\subsection}{\heiti\sanhao}{}{0em}{\sqbr}
+{% endif %}
+
+\paragraph{ {{ probs[i].name }} }. {{ problems[i] }}
+
+{% endfor %}
+
+
+{% endblock %}
+
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/table.html.jinja` & `tuack-0.1.5/tuack/templates/table.html.jinja`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/templates/table.tex.jinja` & `tuack-0.1.5/tuack/templates/table.tex.jinja`

 * *Files identical despite different names*

### Comparing `tuack-0.1.4.9.2/tuack/templates/template_base.tex.jinja` & `tuack-0.1.5/tuack/templates/template_base.tex.jinja`

 * *Ordering differences only*

 * *Files 13% similar despite different names*

```diff
@@ -1,93 +1,93 @@
-\documentclass{tuack}
-
-{% if not base.lang or base.lang == 'zh-cn' %}
-	\renewcommand{\figurename}{图}
-{% endif %}
-
-\def\thecontent { {{_('Content')}} }
-
-{% if water_mark %}
-
-\usepackage{draftwatermark}
-
-\SetWatermarkAngle{0}
-
-\SetWatermarkText{\includegraphics{water_mark.png} }
-
-{% endif %}
-
-{% block base %}{% endblock %}
-
-\begin{document}
-
-{% if contest and 'title' in contest %}
-	\title{ {{- contest.tr('title') -}} }
-	\def\mytitle{ {{- contest.tr('title') -}} }
-	{% if contest.tr('title').__len__() > 10 %}
-		\def\longtitle{ {{- contest.tr('title') -}} }
-	{% endif %}
-{% else %}
-	\title{ 预览输出 }
-	\def\mytitle{ 预览输出 }
-{% endif %}
-
-{% if contest and 'subtitle' in contest %}
-	\def\subtitle{ {{- contest.tr('subtitle') -}} }
-{% endif %}
-
-{% if contest and 'subsubtitle' in contest %}
-	\def\subsubtitle{ {{- contest.tr('subsubtitle') -}} }
-{% endif %}
-
-{% if contest and 'short title' in contest %}
-	\def\engtitle{ {{- contest.tr('short title') -}} }
-{% endif %}
-
-{% if day and 'title' in day %}
-	\def\theday{ {{- day.tr('title') -}} }
-{% endif %}
-
-{% if day and 'start time' in day and 'end time' in day %}
-	\def\thetime{
-		{{ _('Time:') }}
-		{{ tools.time_range(day['start time'], day['end time'], _('year'), _('month'), _('day')).replace('~', '$\\sim$').replace(' ', ' ') }}
-	}
-{% endif %}
-
-{% if contest and 'place' in contest %}
-	\def\place{ {{contest.place['en']}} }
-{% endif %}
-
-{% block header %}
-
-\rhead{\parbox{\textwidth}{\raggedleft\textnormal{
-	\footnotesize
-	\ifdefined \theday
-		\theday
-	\fi
-	\nouppercase \rightmark
-}}}
-\lhead{\parbox{\textwidth}{\textnormal{\footnotesize\mytitle
-	\ifdefined\subtitle
-		\subtitle
-	\fi
-}}}
-\chead{}
-\lfoot{}
-\cfoot{\parbox{\textwidth}{
-	\centering \footnotesize {
-{% if not base.lang or base.lang == 'zh-cn' -%}
-	第 \thepage{} 页 ~~~~ 共 \pageref{LastPage} 页
-{%- elif base.lang == 'en' -%}
-	page \thepage{} / \pageref{LastPage}
-{%- endif -%}
-} } }
-\rfoot{}
-
-{% endblock %}
-
-{% block cover %}{% endblock %}
-
-{% block statements %}{% endblock %}
-
-\end{document}
+\documentclass{tuack}
+
+{% if not base.lang or base.lang == 'zh-cn' %}
+	\renewcommand{\figurename}{图}
+{% endif %}
+
+\def\thecontent { {{_('Content')}} }
+
+{% if water_mark %}
+
+\usepackage{draftwatermark}
+
+\SetWatermarkAngle{0}
+
+\SetWatermarkText{\includegraphics{water_mark.png} }
+
+{% endif %}
+
+{% block base %}{% endblock %}
+
+\begin{document}
+
+{% if contest and 'title' in contest %}
+	\title{ {{- contest.tr('title') -}} }
+	\def\mytitle{ {{- contest.tr('title') -}} }
+	{% if contest.tr('title').__len__() > 10 %}
+		\def\longtitle{ {{- contest.tr('title') -}} }
+	{% endif %}
+{% else %}
+	\title{ 预览输出 }
+	\def\mytitle{ 预览输出 }
+{% endif %}
+
+{% if contest and 'subtitle' in contest %}
+	\def\subtitle{ {{- contest.tr('subtitle') -}} }
+{% endif %}
+
+{% if contest and 'subsubtitle' in contest %}
+	\def\subsubtitle{ {{- contest.tr('subsubtitle') -}} }
+{% endif %}
+
+{% if contest and 'short title' in contest %}
+	\def\engtitle{ {{- contest.tr('short title') -}} }
+{% endif %}
+
+{% if day and 'title' in day %}
+	\def\theday{ {{- day.tr('title') -}} }
+{% endif %}
+
+{% if day and 'start time' in day and 'end time' in day %}
+	\def\thetime{
+		{{ _('Time:') }}
+		{{ tools.time_range(day['start time'], day['end time'], _('year'), _('month'), _('day')).replace('~', '$\\sim$').replace(' ', ' ') }}
+	}
+{% endif %}
+
+{% if contest and 'place' in contest %}
+	\def\place{ {{contest.place['en']}} }
+{% endif %}
+
+{% block header %}
+
+\rhead{\parbox{\textwidth}{\raggedleft\textnormal{
+	\footnotesize
+	\ifdefined \theday
+		\theday
+	\fi
+	\nouppercase \rightmark
+}}}
+\lhead{\parbox{\textwidth}{\textnormal{\footnotesize\mytitle
+	\ifdefined\subtitle
+		\subtitle
+	\fi
+}}}
+\chead{}
+\lfoot{}
+\cfoot{\parbox{\textwidth}{
+	\centering \footnotesize {
+{% if not base.lang or base.lang == 'zh-cn' -%}
+	第 \thepage{} 页 ~~~~ 共 \pageref{LastPage} 页
+{%- elif base.lang == 'en' -%}
+	page \thepage{} / \pageref{LastPage}
+{%- endif -%}
+} } }
+\rfoot{}
+
+{% endblock %}
+
+{% block cover %}{% endblock %}
+
+{% block statements %}{% endblock %}
+
+\end{document}
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/tuoi.tex.jinja` & `tuack-0.1.5/tuack/templates/tuoi.tex.jinja`

 * *Files 25% similar despite different names*

```diff
@@ -1,346 +1,354 @@
-{% extends 'template_base.tex.jinja' %}
-
-{% block cover %}
-
-\thispagestyle{Cover}
-
-{% if precautions %}
-
-	\begin{center}
-		\ifdefined\longtitle\centerline\fi{\erhao \bf \thetitle} \par
-		\ifdefined\subtitle
-			{\erhao \hei \subtitle \par}
-		\fi
-		\ifdefined\engtitle
-			{\xiaoyi \hei \engtitle \par}
-		\fi
-		\ifdefined\theday
-			{\kai \erhao \theday \par}
-		\fi
-		\ifdefined\thetime
-			{\hei \xiaosan \thetime \par}
-		\fi
-	\end{center}
-
-{% else %}
-
-	\null
-	\begin{center}
-		\ifdefined\thetitle
-			\ifdefined\longtitle\centerline\fi{\yihao \bf \thetitle} \par
-		\fi
-		\ifdefined\subtitle
-			{\yihao \hei \subtitle \par} \vskip 1em
-		\fi
-		\ifdefined\engtitle
-			{\yihao \xiaochu \engtitle \par} \vskip 1em
-		\fi
-		\ifdefined\theday
-			{\kai \xiaoyi \theday \par} \vskip 1em 
-		\fi
-		\ifdefined\thetime
-			{\hei \sanhao \thetime \par}
-		\fi
-	\end{center}
-	\vskip 1em
-
-{% endif %}
-	
-\begin{center}
-\begin{tabularx}{\the \textwidth}{
-		|
-		{%- if probs.__len__() == 4 -%}
-			p{0.20 \textwidth}
-		{%- elif probs.__len__() == 3 -%}
-			p{0.22 \textwidth}
-		{%- else -%}
-			p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
-		{%- endif -%}
-		|
-		{%- for i in range(probs.__len__()) %}X|{% endfor-%}
-	}
-	\hline
-		题目名称
-		{%- for prob in probs -%}
-			& {{ prob.tr('title') }}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		题目类型
-		{%- for prob in probs -%}
-			&
-			{% if prob['type'] == 'program' %}
-				传统型
-			{% elif prob['type'] == 'output' %}
-				提交答案型
-			{% else %}
-				交互型
-			{% endif %}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-{% if comp == 'noi' %}
-	{% if base.out_system != 'Windows' %}
-		目录
-		{%- for prob in probs -%}
-			& {\ttfamily {{ prob['name'].replace('_', '\\_') }} }
-		{%- endfor -%} 
-		\tabularnewline
-	\hline
-	{%endif%}
-		可执行文件名
-		{%- for prob in probs -%}
-			&
-			{% if prob['type'] != 'output' %}
-				{\ttfamily {{ prob['name'].replace('_', '\\_') + ('.exe' if base.out_system == 'Windows' else '') }} }
-			{% else %}
-				N/A
-			{% endif %}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-{% endif %}
-		输入{% if io_style == 'fio' %}文件名{% endif %}
-		{%- for prob in probs -%}
-			&
-			{%- if 'input_table' in prob -%}
-				{{ prob.tr('input_table') }}
-			{%- elif io_style == 'fio' -%}
-				{%- if prob['type'] != 'output' -%}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.in }
-				{%- else -%}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}*.in }
-				{%- endif -%}
-			{%- else -%}
-				{%- if prob['type'] != 'output' -%}
-					标准输入
-				{%- else -%}
-					{\ttfamily *.in }
-				{%- endif -%}
-			{%- endif -%}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		输出{% if io_style == 'fio' %}文件名{% endif %}
-		{%- for prob in probs -%}
-			&
-			{%- if 'output_table' in prob -%}
-				{{ prob.tr('output_table') }}
-			{%- elif io_style == 'fio' -%}
-				{%- if prob['type'] != 'output' -%}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.out }
-				{%- else -%}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}*.out }
-				{%- endif -%}
-			{%- else -%}
-				{%- if prob['type'] != 'output' -%}
-					标准输出
-				{%- else -%}
-					{\ttfamily *.out }
-				{%- endif -%}
-			{%- endif -%}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		每个测试点时限
-		{%- for prob in probs -%}
-			&
-			{% if prob['type'] != 'output' %}
-				{{ prob['time limit'] }}秒
-			{% else %}
-				N/A
-			{% endif %}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		内存限制
-		{%- for prob in probs -%}
-			&
-			{% if prob['type'] != 'output' %}
-				{{ prob['memory limit'] }}
-			{% else %}
-				N/A
-			{% endif %}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		子任务数目
-		{%- for prob in probs -%}
-			& {{ prob.test_cases.__len__() if not prob.packed else prob.data.__len__() }}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-		测试点是否等分
-		{%- for prob in probs -%}
-			& {{ _("yes") if not prob.packed else _("no") }}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-	{% if probs.__len__() >= 1 and probs[0].pre_cases.__len__() >= 1 %}
-		预测试点数目
-		{%- for prob in probs -%}
-			& {{ prob.pre_cases.__len__() }}
-		{%- endfor -%}
-		\tabularnewline
-	\hline
-	{% endif %}
-\end{tabularx}
-\end{center}
-
-{% if comp == 'noi' %}
-	提交源程序文件名
-	\begin{center}
-	\begin{tabularx}{\the \textwidth}{
-			|
-			{%- if probs.__len__() == 4 -%}
-				p{0.20 \textwidth}
-			{%- elif probs.__len__() == 3 -%}
-				p{0.22 \textwidth}
-			{%- else -%}
-				p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
-			{%- endif -%}
-			|
-			{%- for i in range(probs.__len__()) %}X|{% endfor-%}
-		}
-		\hline
-			对于C++ {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in probs -%}
-				&
-				{% if prob['type'] != 'output' %}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.cpp }
-				{% else %}
-					N/A
-				{% endif %}
-			{%- endfor -%}
-			\tabularnewline
-		\hline
-			对于C {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in probs -%}
-				&
-				{% if prob['type'] != 'output' %}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.c }
-				{% else %}
-					N/A
-				{% endif %}
-			{%- endfor -%}
-			\tabularnewline
-		\hline
-			对于Pascal {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in probs -%}
-				&
-				{% if prob['type'] != 'output' %}
-					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.pas }
-				{% else %}
-					N/A
-				{% endif %}
-			{%- endfor -%}
-			\tabularnewline
-		\hline
-	\end{tabularx}
-	\end{center}
-
-	编译选项
-	\begin{center}
-	\begin{tabularx}{\the \textwidth}{
-			|
-			{%- if probs.__len__() == 4 -%}
-				p{0.20 \textwidth}
-			{%- elif probs.__len__() == 3 -%}
-				p{0.22 \textwidth}
-			{%- else -%}
-				p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
-			{%- endif -%}
-			|
-			{%- for i in range(probs.__len__()) %}X|{% endfor-%}
-		}
-		{% if 'cpp' in compile %}
-		\hline
-			对于C++ {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in compile['cpp'] -%}
-				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
-					&
-					{%- if prob['cnt'] == probs.__len__() -%}
-						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
-					{%- endif -%}
-					{%- if prob['use'] -%}
-						\ttfamily {{ prob['option'] }}
-					{%- else -%}
-						{ {{ prob['option'] }} }
-					{%- endif -%}
-					{%- if prob['cnt'] == probs.__len__() -%}
-						} }
-					{%- endif -%}
-				{% endfor %}
-			{%- endfor -%}
-			\tabularnewline
-		{% endif %}
-		{% if 'c' in compile %}
-		\hline
-			对于C {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in compile['c'] -%}
-				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
-					&
-					{%- if prob['cnt'] == probs.__len__() -%}
-						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
-					{%- endif -%}
-					{%- if prob['use'] -%}
-						\ttfamily {{ prob['option'] }}
-					{%- else -%}
-						{ {{ prob['option'] }} }
-					{%- endif -%}
-					{%- if prob['cnt'] == probs.__len__() -%}
-						} }
-					{%- endif -%}
-				{% endfor %}
-			{%- endfor -%}
-			\tabularnewline
-		{% endif %}
-		{% if 'pas' in compile %}
-		\hline
-			对于Pascal {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
-			{%- for prob in compile['pas'] -%}
-				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
-					&
-					{%- if prob['cnt'] == probs.__len__() -%}
-						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
-					{%- endif -%}
-					{%- if prob['use'] -%}
-						\ttfamily {{ prob['option'] }}
-					{%- else -%}
-						{ {{ prob['option'] }} }
-					{%- endif -%}
-					{%- if prob['cnt'] == probs.__len__() -%}
-						} }
-					{%- endif -%}
-				{% endfor %}
-			{%- endfor -%}
-			\tabularnewline
-		{% endif %}
-		\hline
-	\end{tabularx}
-	\end{center}
-{% endif %}
-
-{% if precautions %}
-	{{ precautions }}
-{% endif %}
-
-
-{% endblock %}
-
-{% block statements %}
-
-{% for i in range(problems.__len__()) %}
-
-	\clearpage
-
-	\begin{center}
-		\section{ {{probs[i].tr('title')}}（{{ probs[i]['name'].replace('_', '\\_') }}） }
-	\end{center}
-	
-	{{ problems[i] }}
-
-{% endfor %}
-
-{% endblock %}
-
+{% extends 'template_base.tex.jinja' %}
+
+{% block cover %}
+
+\thispagestyle{Cover}
+
+{% if precautions %}
+
+	\begin{center}
+		\ifdefined\longtitle\centerline\fi{\erhao \bf \thetitle} \par
+		\ifdefined\subtitle
+			{\erhao \heiti \subtitle \par}
+		\fi
+		\ifdefined\engtitle
+			{\xiaoyi \heiti \engtitle \par}
+		\fi
+		\ifdefined\theday
+			{\erhao \kaishu \theday \par}
+		\fi
+		\ifdefined\thetime
+			{\xiaosan \heiti \thetime \par}
+		\fi
+	\end{center}
+
+{% else %}
+
+	\null
+	\begin{center}
+		\ifdefined\thetitle
+			\ifdefined\longtitle\centerline\fi{\yihao \bf \thetitle} \par
+		\fi
+		\ifdefined\subtitle
+			{\yihao \heiti \subtitle \par} \vskip 1em
+		\fi
+		\ifdefined\engtitle
+			{\yihao \heiti \engtitle \par} \vskip 1em
+		\fi
+		\ifdefined\theday
+			{\xiaoyi \kaishu \theday \par} \vskip 1em 
+		\fi
+		\ifdefined\thetime
+			{\sanhao \heiti \thetime \par}
+		\fi
+	\end{center}
+	\vskip 1em
+
+{% endif %}
+	
+\begin{center}
+\begin{tabularx}{\the \textwidth}{
+		|
+		{%- if probs.__len__() == 4 -%}
+			p{0.20 \textwidth}
+		{%- elif probs.__len__() == 3 -%}
+			p{0.22 \textwidth}
+		{%- else -%}
+			p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
+		{%- endif -%}
+		|
+		{%- for i in range(probs.__len__()) %}X|{% endfor-%}
+	}
+	\hline
+		题目名称
+		{%- for prob in probs -%}
+			& {{ prob.tr('title') }}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		题目类型
+		{%- for prob in probs -%}
+			&
+			{% if prob['type'] == 'program' %}
+				传统型
+			{% elif prob['type'] == 'output' %}
+				提交答案型
+			{% else %}
+				交互型
+			{% endif %}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+{% if comp == 'noi' %}
+	{% if base.out_system != 'Windows' %}
+		目录
+		{%- for prob in probs -%}
+			& {\ttfamily {{ prob['name'].replace('_', '\\_') }} }
+		{%- endfor -%} 
+		\tabularnewline
+	\hline
+	{%endif%}
+		可执行文件名
+		{%- for prob in probs -%}
+			&
+			{% if prob['type'] != 'output' %}
+				{\ttfamily {{ prob['name'].replace('_', '\\_') + ('.exe' if base.out_system == 'Windows' else '') }} }
+			{% else %}
+				N/A
+			{% endif %}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+{% endif %}
+		输入{% if io_style == 'fio' %}文件名{% endif %}
+		{%- for prob in probs -%}
+			&
+			{%- if 'input_table' in prob -%}
+				{{ prob.tr('input_table') }}
+			{%- elif io_style == 'fio' -%}
+				{%- if prob['type'] != 'output' -%}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.in }
+				{%- else -%}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}*.in }
+				{%- endif -%}
+			{%- else -%}
+				{%- if prob['type'] != 'output' -%}
+					标准输入
+				{%- else -%}
+					{\ttfamily *.in }
+				{%- endif -%}
+			{%- endif -%}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		输出{% if io_style == 'fio' %}文件名{% endif %}
+		{%- for prob in probs -%}
+			&
+			{%- if 'output_table' in prob -%}
+				{{ prob.tr('output_table') }}
+			{%- elif io_style == 'fio' -%}
+				{%- if prob['type'] != 'output' -%}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.out }
+				{%- else -%}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}*.out }
+				{%- endif -%}
+			{%- else -%}
+				{%- if prob['type'] != 'output' -%}
+					标准输出
+				{%- else -%}
+					{\ttfamily *.out }
+				{%- endif -%}
+			{%- endif -%}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		每个测试点时限
+		{%- for prob in probs -%}
+			&
+			{% if prob['type'] != 'output' %}
+				{{ prob['time limit'] }}秒
+			{% else %}
+				N/A
+			{% endif %}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		内存限制
+		{%- for prob in probs -%}
+			&
+			{% if prob['type'] != 'output' %}
+				{{ prob['memory limit'] }}
+			{% else %}
+				N/A
+			{% endif %}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		{% if comp == 'noi' -%}
+		测试点数目
+		{%- else -%}
+		子任务数目
+		{%- endif -%}
+		{%- for prob in probs -%}
+			& {{ prob.test_cases.__len__() if not prob.packed else prob.data.__len__() }}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+		测试点是否等分
+		{%- for prob in probs -%}
+			& {{ _("yes") if not prob.packed else _("no") }}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+	{% if probs.__len__() >= 1 and probs[0].pre_cases.__len__() >= 1 %}
+		预测试点数目
+		{%- for prob in probs -%}
+			& {{ prob.pre_cases.__len__() }}
+		{%- endfor -%}
+		\tabularnewline
+	\hline
+	{% endif %}
+\end{tabularx}
+\end{center}
+
+{% if comp == 'noi' %}
+	提交源程序文件名
+	\begin{center}
+	\begin{tabularx}{\the \textwidth}{
+			|
+			{%- if probs.__len__() == 4 -%}
+				p{0.20 \textwidth}
+			{%- elif probs.__len__() == 3 -%}
+				p{0.22 \textwidth}
+			{%- else -%}
+				p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
+			{%- endif -%}
+			|
+			{%- for i in range(probs.__len__()) %}X|{% endfor-%}
+		}
+		\hline
+			对于C++ {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in probs -%}
+				&
+				{% if prob['type'] != 'output' %}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.cpp }
+				{% else %}
+					N/A
+				{% endif %}
+			{%- endfor -%}
+			\tabularnewline
+		\hline
+		{% if 'c' in compile and noi_pas_c %}
+			对于C {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in probs -%}
+				&
+				{% if prob['type'] != 'output' %}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.c }
+				{% else %}
+					N/A
+				{% endif %}
+			{%- endfor -%}
+			\tabularnewline
+		\hline
+		{% endif %}
+		{% if 'pas' in compile and noi_pas_c %}
+			对于Pascal {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in probs -%}
+				&
+				{% if prob['type'] != 'output' %}
+					{\ttfamily {{ prob['name'].replace('_', '\\_') }}.pas }
+				{% else %}
+					N/A
+				{% endif %}
+			{%- endfor -%}
+			\tabularnewline
+		\hline
+		{% endif %}
+	\end{tabularx}
+	\end{center}
+
+	编译选项
+	\begin{center}
+	\begin{tabularx}{\the \textwidth}{
+			|
+			{%- if probs.__len__() == 4 -%}
+				p{0.20 \textwidth}
+			{%- elif probs.__len__() == 3 -%}
+				p{0.22 \textwidth}
+			{%- else -%}
+				p{ {{ 1.0 / (probs.__len__() + 1) }} \textwidth}
+			{%- endif -%}
+			|
+			{%- for i in range(probs.__len__()) %}X|{% endfor-%}
+		}
+		{% if 'cpp' in compile %}
+		\hline
+			对于C++ {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in compile['cpp'] -%}
+				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
+					&
+					{%- if prob['cnt'] == probs.__len__() -%}
+						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
+					{%- endif -%}
+					{%- if prob['use'] -%}
+						\ttfamily {{ prob['option'] }}
+					{%- else -%}
+						{ {{ prob['option'] }} }
+					{%- endif -%}
+					{%- if prob['cnt'] == probs.__len__() -%}
+						} }
+					{%- endif -%}
+				{% endfor %}
+			{%- endfor -%}
+			\tabularnewline
+		{% endif %}
+		{% if 'c' in compile and noi_pas_c %}
+		\hline
+			对于C {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in compile['c'] -%}
+				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
+					&
+					{%- if prob['cnt'] == probs.__len__() -%}
+						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
+					{%- endif -%}
+					{%- if prob['use'] -%}
+						\ttfamily {{ prob['option'] }}
+					{%- else -%}
+						{ {{ prob['option'] }} }
+					{%- endif -%}
+					{%- if prob['cnt'] == probs.__len__() -%}
+						} }
+					{%- endif -%}
+				{% endfor %}
+			{%- endfor -%}
+			\tabularnewline
+		{% endif %}
+		{% if 'pas' in compile and noi_pas_c %}
+		\hline
+			对于Pascal {% if probs.__len__() < 5 %} \tabto{5.5em} {% endif %} 语言
+			{%- for prob in compile['pas'] -%}
+				{% for i in range(prob['cnt'] if prob['cnt'] != probs.__len__() else 1) %}
+					&
+					{%- if prob['cnt'] == probs.__len__() -%}
+						\multicolumn{ {{- prob['cnt'] -}} }{@{}X|}{\parbox{ \hsize }{ \centering
+					{%- endif -%}
+					{%- if prob['use'] -%}
+						\ttfamily {{ prob['option'] }}
+					{%- else -%}
+						{ {{ prob['option'] }} }
+					{%- endif -%}
+					{%- if prob['cnt'] == probs.__len__() -%}
+						} }
+					{%- endif -%}
+				{% endfor %}
+			{%- endfor -%}
+			\tabularnewline
+		{% endif %}
+		\hline
+	\end{tabularx}
+	\end{center}
+{% endif %}
+
+{% if precautions %}
+	{{ precautions }}
+{% endif %}
+
+
+{% endblock %}
+
+{% block statements %}
+
+{% for i in range(problems.__len__()) %}
+
+	\clearpage
+
+	\begin{center}
+		\section{ {{probs[i].tr('title')}}（{{ probs[i]['name'].replace('_', '\\_') }}） }
+	\end{center}
+	
+	{{ problems[i] }}
+
+{% endfor %}
+
+{% endblock %}
+
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/tupc.tex.jinja` & `tuack-0.1.5/tuack/templates/tupc.tex.jinja`

 * *Files 26% similar despite different names*

```diff
@@ -1,70 +1,70 @@
-{% extends 'template_base.tex.jinja' %}
-
-{% block cover %}
-
-\thispagestyle{Cover}
-\begin{center}
-	\ifdefined\thetitle
-		\ifdefined\longtitle\centerline\fi{\yihao \bf \thetitle} \par
-	\fi
-	\ifdefined\subtitle
-		{\hei \yihao \subtitle \par}
-	\fi
-	\ifdefined\subsubtitle
-		{\hei \yihao \subsubtitle \par}
-	\fi
-	\ifdefined\engtitle
-		{\xiaoyi \hei \engtitle \par}
-	\fi
-	\vskip 1em 
-	\ifdefined\theday
-		{\kai \chuhao \theday \par} \vskip 1em 
-	\fi
-	\ifdefined\thetime
-		{\hei \sanhao \thetime \par}
-	\fi
-\end{center}
-
-\setcounter{tocdepth}{1}
-
-\tableofcontents
-
-{% endblock %}
-
-{% block statements %}
-
-{% for i in range(problems.__len__()) %}
-	\clearpage
-	\begin{center}
-		\section{ 
-			{%- if 'number' in probs[i] -%}
-				{{ tools.chr(tools.ord('A') + probs[i].number) }}
-			{%- else -%}
-				{{ tools.chr(tools.ord('A') + i) }}
-			{%- endif -%} . ~
-			{{- probs[i].tr('title') -}} 
-			~~/~~ 
-			{% if probs[i].lang() == 'en' %}
-			{{- probs[i]['name'] -}}
-			{% else %}
-			{{- probs[i]['name'].capitalize() -}}
-			{% endif %}
-		}
-	\end{center}
-	
-{% if probs[i].lang() == 'zh-cn' %}
-	\renewcommand{\sqbr}[1]{【#1】}
-	\titleformat{\subsection}{\hei\banxiaosi}{}{1em}{\sqbr}
-{% else %}
-	\renewcommand{\sqbr}[1]{ \textbf{ #1 } }
-	\titleformat{\subsection}{\hei\sanhao}{}{0em}{\sqbr}
-{% endif %}
-
-	
-	{{ problems[i] }}
-
-{% endfor %}
-
-{% endblock %}
-
-\end{document}
+{% extends 'template_base.tex.jinja' %}
+
+{% block cover %}
+
+\thispagestyle{Cover}
+\begin{center}
+	\ifdefined\thetitle
+		\ifdefined\longtitle\centerline\fi{\yihao \bf \thetitle} \par
+	\fi
+	\ifdefined\subtitle
+		{\yihao \heiti \subtitle \par}
+	\fi
+	\ifdefined\subsubtitle
+		{\yihao \heiti \subsubtitle \par}
+	\fi
+	\ifdefined\engtitle
+		{\xiaoyi \heiti \engtitle \par}
+	\fi
+	\vskip 1em 
+	\ifdefined\theday
+		{\chuhao \kaishu \theday \par} \vskip 1em 
+	\fi
+	\ifdefined\thetime
+		{\sanhao \heiti \thetime \par}
+	\fi
+\end{center}
+
+\setcounter{tocdepth}{1}
+
+\tableofcontents
+
+{% endblock %}
+
+{% block statements %}
+
+{% for i in range(problems.__len__()) %}
+	\clearpage
+	\begin{center}
+		\section{ 
+			{%- if 'number' in probs[i] -%}
+				{{ tools.chr(tools.ord('A') + probs[i].number) }}
+			{%- else -%}
+				{{ tools.chr(tools.ord('A') + i) }}
+			{%- endif -%} . ~
+			{{- probs[i].tr('title') -}} 
+			~~/~~ 
+			{% if probs[i].lang() == 'en' %}
+			{{- probs[i]['name'] -}}
+			{% else %}
+			{{- probs[i]['name'].capitalize() -}}
+			{% endif %}
+		}
+	\end{center}
+	
+{% if probs[i].lang() == 'zh-cn' %}
+	\renewcommand{\sqbr}[1]{【#1】}
+	\titleformat{\subsection}{\heiti\banxiaosi}{}{1em}{\sqbr}
+{% else %}
+	\renewcommand{\sqbr}[1]{ \textbf{ #1 } }
+	\titleformat{\subsection}{\heiti\sanhao}{}{0em}{\sqbr}
+{% endif %}
+
+	
+	{{ problems[i] }}
+
+{% endfor %}
+
+{% endblock %}
+
+\end{document}
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/zh-cn/LC_MESSAGES/lang.mo` & `tuack-0.1.5/tuack/templates/zh-cn/LC_MESSAGES/lang.mo`

 * *Files 11% similar despite different names*

#### msgunfmt {}

```diff
@@ -47,14 +47,17 @@
 
 msgid "Output"
 msgstr "输出"
 
 msgid "Output Format"
 msgstr "输出格式"
 
+msgid "Read from the file *%s*."
+msgstr "从文件 *%s* 中读入数据。"
+
 msgid "Read from the file *%s.in*."
 msgstr "从文件 *%s.in* 中读入数据。"
 
 msgid "Read from the standard input."
 msgstr "从标准输入读入数据。"
 
 msgid "Related files:"
@@ -98,14 +101,17 @@
 
 msgid "Time limit:"
 msgstr "时间限制："
 
 msgid "Time:"
 msgstr "时间："
 
+msgid "Write to the file *%s*."
+msgstr "输出到文件 *%s* 中。"
+
 msgid "Write to the file *%s.out*."
 msgstr "输出到文件 *%s.out* 中。"
 
 msgid "Write to the standard output."
 msgstr "输出到标准输出。"
 
 msgid "background"
```

### Comparing `tuack-0.1.4.9.2/tuack/templates/zh-cn/LC_MESSAGES/lang.po` & `tuack-0.1.5/tuack/templates/zh-cn/LC_MESSAGES/lang.po`

 * *Files 24% similar despite different names*

```diff
@@ -1,177 +1,183 @@
-# SOME DESCRIPTIVE TITLE.
-# Copyright (C) YEAR ORGANIZATION
-# FIRST AUTHOR <EMAIL@ADDRESS>, YEAR.
-#
-msgid ""
-msgstr ""
-"Project-Id-Version: PACKAGE VERSION\n"
-"POT-Creation-Date: 2017-04-30 20:08+0800\n"
-"PO-Revision-Date: YEAR-MO-DA HO:MI+ZONE\n"
-"Last-Translator: FULL NAME <EMAIL@ADDRESS>\n"
-"Language-Team: LANGUAGE <LL@li.org>\n"
-"MIME-Version: 1.0\n"
-"Content-Type: text/plain; charset=utf-8\n"
-"Content-Transfer-Encoding: utf-8\n"
-"Generated-By: pygettext.py 1.5\n"
-
-msgid "Read from the standard input."
-msgstr "从标准输入读入数据。"
-
-msgid "Sample"
-msgstr "样例"
-
-msgid "sample"
-msgstr "样例"
-
-msgid "Sample Input %s"
-msgstr "样例%s输入"
-
-msgid "sample input"
-msgstr "样例%s输入"
-
-msgid "Input"
-msgstr "输入"
-
-msgid "input"
-msgstr "输入"
-
-msgid "Sample Output %s"
-msgstr "样例%s输出"
-
-msgid "sample output"
-msgstr "样例%s输出"
-
-msgid "Output"
-msgstr "输出"
-
-msgid "output"
-msgstr "输出"
-
-msgid "Explanation"
-msgstr "解释"
-
-msgid "explanation"
-msgstr "解释"
-
-msgid "Sample Explanation %s"
-msgstr "样例%s解释"
-
-msgid "sample explanation"
-msgstr "样例%s解释"
-
-msgid "Input Format"
-msgstr "输入格式"
-
-msgid "input format"
-msgstr "输入格式"
-
-msgid "Output Format"
-msgstr "输出格式"
-
-msgid "output format"
-msgstr "输出格式"
-
-msgid "Description"
-msgstr "题目描述"
-
-msgid "description"
-msgstr "题目描述"
-
-msgid "Background"
-msgstr "题目背景"
-
-msgid "background"
-msgstr "题目背景"
-
-msgid "Hint"
-msgstr "提示"
-
-msgid "hint"
-msgstr "提示"
-
-msgid "Subtasks"
-msgstr "子任务"
-
-msgid "subtasks"
-msgstr "子任务"
-
-msgid "Scoring"
-msgstr "评分方式"
-
-msgid "scoring"
-msgstr "评分方式"
-
-msgid "Time limit:"
-msgstr "时间限制："
-
-msgid "Time limit"
-msgstr "时间限制"
-
-msgid "Memory limit:"
-msgstr "空间限制："
-
-msgid "Memory limit"
-msgstr "空间限制"
-
-msgid "second(s)"
-msgstr "秒"
-
-msgid "Read from the file *%s.in*."
-msgstr "从文件 *%s.in* 中读入数据。"
-
-msgid "Write to the standard output."
-msgstr "输出到标准输出。"
-
-msgid "Write to the file *%s.out*."
-msgstr "输出到文件 *%s.out* 中。"
-
-msgid "download files"
-msgstr "下载目录"
-
-msgid "user's home path"
-msgstr "选手目录"
-
-msgid "problem path"
-msgstr "题目目录"
-
-msgid "See *%(in)s* and *%(ans)s* in the %(path)s."
-msgstr "见%(path)s下的 *%(in)s* 与 *%(ans)s*。"
-
-msgid "Related files:"
-msgstr "相关文件："
-
-msgid "This is an output-only problem."
-msgstr "这是一道提交答案题。"
-
-msgid "This is an interactive problem."
-msgstr "这是一道交互题。"
-
-msgid "Time:"
-msgstr "时间："
-
-msgid "year"
-msgstr "年"
-
-msgid "month"
-msgstr "月"
-
-msgid "day"
-msgstr "日"
-
-msgid "Content"
-msgstr "目~~录"
-
-msgid "This is an output-only problem. There are %d input files named *%s1.in* ~ *%s%d.in*."
-msgstr "这是一道提交答案题，共有%d组输入数据，这些数据命名为 *%s1.in* ~ *%s%d.in*。"
-
-msgid "For each input file, you should accomplish an output file named *%s1.out* ~ *%s%d.out*."
-msgstr "对于每组输入数据，你需要提交相应的输出文件 *%s1.out* ~ *%s%d.out*。"
-
-msgid "Case related"
-msgstr "见题面"
-
-msgid "yes"
-msgstr "是"
-
-msgid "no"
-msgstr "否"
+# SOME DESCRIPTIVE TITLE.
+# Copyright (C) YEAR ORGANIZATION
+# FIRST AUTHOR <EMAIL@ADDRESS>, YEAR.
+#
+msgid ""
+msgstr ""
+"Project-Id-Version: PACKAGE VERSION\n"
+"POT-Creation-Date: 2017-04-30 20:08+0800\n"
+"PO-Revision-Date: YEAR-MO-DA HO:MI+ZONE\n"
+"Last-Translator: FULL NAME <EMAIL@ADDRESS>\n"
+"Language-Team: LANGUAGE <LL@li.org>\n"
+"MIME-Version: 1.0\n"
+"Content-Type: text/plain; charset=utf-8\n"
+"Content-Transfer-Encoding: utf-8\n"
+"Generated-By: pygettext.py 1.5\n"
+
+msgid "Read from the standard input."
+msgstr "从标准输入读入数据。"
+
+msgid "Sample"
+msgstr "样例"
+
+msgid "sample"
+msgstr "样例"
+
+msgid "Sample Input %s"
+msgstr "样例%s输入"
+
+msgid "sample input"
+msgstr "样例%s输入"
+
+msgid "Input"
+msgstr "输入"
+
+msgid "input"
+msgstr "输入"
+
+msgid "Sample Output %s"
+msgstr "样例%s输出"
+
+msgid "sample output"
+msgstr "样例%s输出"
+
+msgid "Output"
+msgstr "输出"
+
+msgid "output"
+msgstr "输出"
+
+msgid "Explanation"
+msgstr "解释"
+
+msgid "explanation"
+msgstr "解释"
+
+msgid "Sample Explanation %s"
+msgstr "样例%s解释"
+
+msgid "sample explanation"
+msgstr "样例%s解释"
+
+msgid "Input Format"
+msgstr "输入格式"
+
+msgid "input format"
+msgstr "输入格式"
+
+msgid "Output Format"
+msgstr "输出格式"
+
+msgid "output format"
+msgstr "输出格式"
+
+msgid "Description"
+msgstr "题目描述"
+
+msgid "description"
+msgstr "题目描述"
+
+msgid "Background"
+msgstr "题目背景"
+
+msgid "background"
+msgstr "题目背景"
+
+msgid "Hint"
+msgstr "提示"
+
+msgid "hint"
+msgstr "提示"
+
+msgid "Subtasks"
+msgstr "子任务"
+
+msgid "subtasks"
+msgstr "子任务"
+
+msgid "Scoring"
+msgstr "评分方式"
+
+msgid "scoring"
+msgstr "评分方式"
+
+msgid "Time limit:"
+msgstr "时间限制："
+
+msgid "Time limit"
+msgstr "时间限制"
+
+msgid "Memory limit:"
+msgstr "空间限制："
+
+msgid "Memory limit"
+msgstr "空间限制"
+
+msgid "second(s)"
+msgstr "秒"
+
+msgid "Read from the file *%s.in*."
+msgstr "从文件 *%s.in* 中读入数据。"
+
+msgid "Read from the file *%s*."
+msgstr "从文件 *%s* 中读入数据。"
+
+msgid "Write to the standard output."
+msgstr "输出到标准输出。"
+
+msgid "Write to the file *%s.out*."
+msgstr "输出到文件 *%s.out* 中。"
+
+msgid "Write to the file *%s*."
+msgstr "输出到文件 *%s* 中。"
+
+msgid "download files"
+msgstr "下载目录"
+
+msgid "user's home path"
+msgstr "选手目录"
+
+msgid "problem path"
+msgstr "题目目录"
+
+msgid "See *%(in)s* and *%(ans)s* in the %(path)s."
+msgstr "见%(path)s下的 *%(in)s* 与 *%(ans)s*。"
+
+msgid "Related files:"
+msgstr "相关文件："
+
+msgid "This is an output-only problem."
+msgstr "这是一道提交答案题。"
+
+msgid "This is an interactive problem."
+msgstr "这是一道交互题。"
+
+msgid "Time:"
+msgstr "时间："
+
+msgid "year"
+msgstr "年"
+
+msgid "month"
+msgstr "月"
+
+msgid "day"
+msgstr "日"
+
+msgid "Content"
+msgstr "目~~录"
+
+msgid "This is an output-only problem. There are %d input files named *%s1.in* ~ *%s%d.in*."
+msgstr "这是一道提交答案题，共有%d组输入数据，这些数据命名为 *%s1.in* ~ *%s%d.in*。"
+
+msgid "For each input file, you should accomplish an output file named *%s1.out* ~ *%s%d.out*."
+msgstr "对于每组输入数据，你需要提交相应的输出文件 *%s1.out* ~ *%s%d.out*。"
+
+msgid "Case related"
+msgstr "见题面"
+
+msgid "yes"
+msgstr "是"
+
+msgid "no"
+msgstr "否"
```

### Comparing `tuack-0.1.4.9.2/tuack/test.py` & `tuack-0.1.5/tuack/test.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,497 +1,504 @@
-# -*- coding: utf-8 -*-
-
-from __future__ import print_function
-import os
-import re
-import sys
-import json
-import datetime
-import shutil
-import subprocess
-import time
-import signal
-import zipfile
-from multiprocessing import Process, Queue
-from functools import wraps
-from threading import Timer
-import platform
-from . import base
-from .base import log, pjoin, rjoin
-import traceback
-
-def time2float(inp):
-	m = re.match(r'(\d*)(:|h)(\d*)(:|m)(\d*\.?\d*)s?', inp)
-	if m:
-		return float(m.group(1)) * 3600 + float(m.group(3)) * 60 + float(m.group(5))
-	m = re.match(r'(\d*)(:|m)(\d*\.?\d*)s?', inp)
-	if m:
-		return float(m.group(1)) * 60 + float(m.group(3))
-	m = re.match(r'(\d*\.?\d*)s?', inp)
-	if m:
-		return float(m.group(1))
-	raise Exception('Timer broken')
-
-def run_windows(name, tl, ml, input = None, output = None, vm = None):
-	'''
-	On windows, memory limit is not considered.
-	'''
-	timer = time.perf_counter if sys.version >= '3.3' else time.clock
-	try:
-		fin = (open(input) if input else None)
-		fout = (open(output, 'w') if output else None)
-		t = timer()
-		pro = subprocess.Popen(vm(name, ml) if vm else name, stdin = fin, stdout = fout)
-		if fout:
-			fout.close()
-		if fin:
-			fin.close()
-	except:
-		return 'Can\'t run program.', 0.0
-	while True:
-		ret = pro.poll()
-		if ret != None:
-			t = timer() - t
-			if ret == 0:
-				ret = None
-			else:
-				ret = 'Runtime error %d.' % ret
-			break
-		if (timer() - t) >= tl * base.time_multiplier:
-			pro.kill()
-			t = 0.0
-			ret = 'Time out.'
-			break
-		time.sleep(1e-2)
-	time.sleep(1e-2)
-	return ret, t
-
-def runner_linux(name, que, ml, input = None, output = None, vm = None):
-	pro = subprocess.Popen(
-		'%s time -f "%%%s" -o timer %s %s %s' % (
-			'ulimit -v %d;' % int(base.Memory(ml).KB) if vm != base.runners['java'] else '',
-			'U' if base.user_time else 'E',
-			vm(name, ml) if vm else './%s' % name,
-			'< %s' % input if input else '',
-			'> %s' % output if output else '',
-		),
-		shell = True,
-		preexec_fn = os.setsid
-	)
-	que.put(pro.pid)
-	ret = pro.wait()
-	que.put(ret)
-	
-def run_linux(name, tl, ml, input = None, output = None, vm = None):
-	que = Queue()
-	pro = Process(target = runner_linux, args = (name, que, ml, input, output, vm))
-	pro.start()
-	pro.join(tl * base.time_multiplier)
-	if que.qsize() == 0:
-		log.error('Runner broken.')
-	elif que.qsize() == 1:
-		ret = 'Time out.'
-		pid = que.get()
-		os.killpg(os.getpgid(pid), signal.SIGTERM)
-		t = 0.
-	else:
-		pid = que.get()
-		ret = que.get()
-		if ret == 0:
-			try:
-				t = time2float(open('timer').readline())
-			except Exception as e:
-				log.warning('Timer broken.')
-				t = 0.
-			ret = None
-		else:
-			ret = 'Runtime error %d.(MLE will cause RE as well in linux)' % ret
-			t = 0.
-	return ret, t
-
-def runner_mac(name, que, ml, input = None, output = None, vm = None):
-	pro = subprocess.Popen(
-		'ulimit -v %d; (time -p %s %s %s) 2> timer' % (
-			int(base.Memory(ml).KB),
-			vm(name, ml) if vm else './%s' % name,
-			'< %s' % input if input else '',
-			'> %s' % output if output else '',
-		),
-		shell = True,
-		preexec_fn = os.setsid
-	)
-	que.put(pro.pid)
-	ret = pro.wait()
-	que.put(ret)
-
-def run_mac(name, tl, ml, input = None, output = None, vm = None):
-	que = Queue()
-	pro = Process(target = runner_mac, args = (name, que, ml, input, output, vm))
-	pro.start()
-	pro.join(tl * base.time_multiplier)
-	if que.empty():
-		log.error('Runner broken.')
-	else:
-		pid = que.get()
-		if que.empty():
-			ret = 'Time out.'
-			os.killpg(os.getpgid(pid), signal.SIGTERM)
-			t = 0.
-		else:
-			ret = que.get()
-			if ret == 0:
-				try:
-					with open('timer') as f:
-						for i in range(2 if base.user_time else 1):
-							line = f.readline()
-						t = time2float(line.strip().split()[-1])
-				except:
-					base.warning('Timer broken.')
-					t = 0.
-				ret = None
-			else:
-				ret = 'Runtime error %d.' % ret
-				t = 0.
-	return ret, t
-
-if base.system == 'Linux':
-	run = run_linux
-elif base.system == 'Windows':
-	run = run_windows
-elif base.system == 'Darwin':
-	run = run_mac
-else:
-	run = run_linux
-	log.warning(u'未知的操作系统，尝试当做Linux运行。')
-	
-def compile(prob, name):
-	for lang, args in prob['compile'].items():
-		if os.path.exists(pjoin('tmp', name + '.' + lang)):
-			base.check_install(lang)
-			os.chdir('tmp')
-			try:
-				ret = subprocess.call(
-					base.compilers[lang](name, args, base.macros[base.work], ml = prob.ml()),
-					shell = True,
-					stdout = open('stdout', 'w'),
-					stderr = open('stderr', 'w')
-				)
-			except Exception as e:
-				with open('stderr', 'a') as f:
-					f.write(str(e))
-				ret = -1
-			os.chdir('..')
-			if ret:
-				log.info('`' + name + '.' + lang + u'`编译失败，详情见`compile.log`。')
-				with open('compile.log', 'a') as f:
-					import __main__
-					f.write(u'## 脚本%s/，工程路径%s，参数%s，开始于%s。\n' % (__main__.__file__, os.getcwd(), str(sys.argv[1:]), str(datetime.datetime.now())))
-					f.write(u'## 测试题目`%s`，编译失败代码名称`%s.%s`\n' % (prob['name'], name, lang))
-					try:
-						f.write(u'编译器输出的stdout为：\n')
-						f.write(open('tmp/stdout').read())
-					except Exception as e:
-						f.write(u'编译器没有输出stdout，具体错误为：\n')
-						f.write(str(e) + '\n')
-					try:
-						f.write(u'编译器输出的stderr为：\n')
-						f.write(open('tmp/stderr').read())
-					except Exception as e:
-						f.write(u'编译器没有输出stderr，具体错误为：\n')
-						f.write(str(e) + '\n')
-				raise Exception('`' + name + '.' + lang + '` compile failed.')
-			return lang
-	else:
-		raise Exception('Can\'t find source file.')
-
-def test(prob, name):
-	scores = []
-	times = []
-	reports = []
-	if prob['type'] == 'program':
-		try:
-			lang = compile(prob, name)
-		except Exception as e:
-			for i in range(len(prob.test_cases) + len(prob.sample_cases)):
-				scores.append(0.0)
-				times.append(0.0)
-				reports.append(str(e))
-			return scores, times, reports
-	all_cases = prob.test_cases + prob.sample_cases + prob.pre_cases
-	for case in all_cases:
-		print('Case %s:%s  ' % (case['key'], case), end = '\r')
-		sys.stdout.flush()
-		shutil.copy(case.full() + '.in', pjoin('tmp', 'in'))
-		shutil.copy(case.full() + '.ans', pjoin('tmp', 'ans'))
-		for fname in ('in', 'ans'):
-			if base.system == 'Windows':
-				base.unix2dos(pjoin('tmp', fname))
-			else:
-				base.dos2unix(pjoin('tmp', fname))
-		if prob['type'] == 'program':
-			os.chdir('tmp')
-			ret, time = run(name, prob['time limit'], prob['memory limit'], 'in', 'out', base.runners[lang])
-			os.chdir('..')
-		elif prob['type'] == 'output':
-			if os.path.exists(pjoin('tmp', case['case'] + '.out')):
-				shutil.copy(pjoin('tmp', case['case'] + '.out'), pjoin('tmp', 'out'))
-				ret = None
-				time = 0.0
-			else:
-				ret = 'Output file does not exist.'
-				time = 0.0
-		else:
-			log.error(u'错误的题目类型`%s`。' % prob['type'])
-			raise Exception('problem type error.')
-		if not ret:
-			if not os.path.exists(pjoin('tmp', 'out')):
-				ret = 'Output file does not exist.'
-				time = 0.0
-				score = 0.0
-			elif prob.chk:
-				shutil.copy(pjoin('bin', prob.route), pjoin('tmp', 'chk' + base.elf_suffix))
-				open('100.0', 'w').write('100.0\n')
-				os.system('%s %s %s %s 100.0 tmp/score tmp/info' % (
-					pjoin('tmp', 'chk' + base.elf_suffix),
-					pjoin('tmp', 'in'),
-					pjoin('tmp', 'out'),
-					pjoin('tmp', 'ans')
-				))
-				os.remove('100.0')
-				try:
-					arbiter_out = ('/' if base.system != 'Windows' else '') + 'tmp/_eval.score'
-					f = open(arbiter_out)
-					report = f.readline().strip()
-					score = float(f.readline()) * 0.1
-					f.close()
-					shutil.remove(arbiter_out)
-				except Exception as e:
-					try:
-						report = open('tmp/info').read().strip()
-					except Exception as e:
-						report = ''
-					score = float(open('tmp/score').readline()) * .01
-			else:
-				ret = os.system('%s %s %s > log' % (
-					base.diff_tool,
-					pjoin('tmp', 'ans'),
-					pjoin('tmp', 'out')
-				))
-				if ret == 0:
-					score = 1.0
-					report = 'ok'
-					if prob['type'] != 'output' and time > prob['time limit']:
-						score = 0.0
-						report += '(but time out)'
-				else:
-					score = 0.0
-					report = 'wa'
-					if prob['type'] != 'output' and time > prob['time limit']:
-						report += '(and time out)'
-		else:
-			score = 0.0
-			report = ret
-		while os.path.exists(pjoin('tmp', prob['name'] + '.out')):
-			try:
-				os.remove(pjoin('tmp', prob['name'] + '.out'))
-			except:
-				pass
-		scores.append(score)
-		times.append(time)
-		reports.append(report)
-	return scores, times, reports
-
-def packed_score(scores, times, reports, score_map, prob):
-	pscore = []
-	ptime = []
-	preport = []
-	for datum in prob.data:
-		pscore.append(datum.score * min((scores[score_map[i]] for i in datum['cases'])))
-		ptime.append(sum((times[score_map[i]] for i in datum['cases'] if scores[score_map[i]] > 0)))
-		preport.append('Total %.1f' % datum.score)
-	pscore.append(sum(pscore))
-	ptime.append(sum(ptime))
-	preport.append('')
-	return (pscore, ptime, preport)
-	
-def test_problem(prob):
-	log.info(u'尝试评测题目`%s`。' % prob.route)
-	if 'users' not in prob:
-		log.warning(u'题目`%s`缺少`users`字段，没有找到出题人的程序。' % prob.route)
-		log.info(u'你需要在工程中放置你的代码，然后使用`python -m tuack.gen code`搜索源代码，或直接配置`users`字段。')
-		return
-	if 'data' not in prob or len(prob.test_cases) == 0:
-		log.warning(u'题目`%s`缺少`data`字段，找不到测试数据。' % prob.route)
-		log.info(u'你需要在文件夹`%s`下按*.in和*.ans格式存放测试数据，' % pjoin(prob.path, 'data'))
-		log.info(u'然后使用`python -m tuack.gen data`添加它们或直接配置`data`字段。')
-	if 'samples' not in prob or len(prob.sample_cases) == 0:
-		log.warning(u'题目`%s`缺少`samples`字段，找不到样例数据。' % prob.route)
-		log.info(u'你需要在文件夹`%s`下按*.in和*.ans格式存放样例数据，' % pjoin(prob.path, 'down'))
-		log.info(u'然后使用`python -m tuack.gen samples`添加它们或直接配置`samples`字段。')
-	if 'pre' in prob and len(prob.pre_cases) == 0:
-		log.warning(u'题目`%s`的`pre`字段为空，找不到预测试数据。' % prob.route)
-		log.info(u'如果这道题目有预测试数据，你需要在文件夹`%s`下按*.in和*.ans格式存放预测试数据，' % pjoin(prob.path, 'pre'))
-		log.info(u'然后使用`python -m tuack.gen pre`在文件夹`%s`下搜索预测试数据。' % (pjoin(prob.path, 'pre')))
-		log.info(u'如果这道题目没有预测试数据，你需要删除`conf.*`中的`pre`字段。')
-	if len(prob.data) == 1 and prob.data[0].get('score') != 100:
-		log.warning(u'题目`%s`的`data`字段只有一个元素，可能没有正确配置数据。' % prob.route)
-		log.info(u'如果是一个包的CPC赛制，需要在这个元素中配置`score`项为100。')
-		log.info(u'如果是多点或多子任务的赛制，需要将每类数据分类配置或打包配置。')
-		log.info(u'详情请见%s。' % base.wiki(u'配置题目#数据'))
-	log.info(u'共%d组样例，%d个预测试点，%d个测试点，%s打包评测%s。' % (
-		len(prob.sample_cases),
-		len(prob.pre_cases),
-		len(prob.test_cases),
-		u'是' if prob.packed else u'不是',
-		(u'（共%d个包）' % len(prob.data) if len(prob.data) != 1 else u'（看样子是一个包的CPC赛制）') if prob.packed else ''
-	))
-
-	prob_failed = False
-
-	case_features = [[] for i in range(len(prob.data))]
-
-	with open(pjoin('result', prob.route) + '.csv', 'w') as fres:
-		fres.write('%s,%s%s,summary,sample%s,pre%s\n' % (
-			prob['name'],
-			','.join(prob.test_cases),
-			',' + ','.join(map(lambda datum : '{' + ';'.join(map(str, datum['cases'])) + '}', prob.data)) \
-				if prob.packed else '',
-			','.join(prob.sample_cases),
-			','.join(prob.pre_cases)
-		))
-		for user, algos in prob.users().items():
-			if not prob.all:
-				match = base.any_prefix(rjoin(prob.route, user))
-				if not match:
-					continue
-			for algo, algo_obj in algos.items():
-				path = algo_obj['path']
-				expe = algo_obj.get('expected')
-				if not expe or len(expe) == 0:
-					log.warning(u'程序`%s/%s`没有设置期望得分。' % (user, algo))
-					log.info(u'如果该程序是标程、部分分程序或骗分程序等，需要设置它的`expected`字段。')
-					log.info(u'有多种设置的格式，例如：`== 60`表示该程序应该得到60分。')
-					log.info(u'如果该程序是其他功能程序，例如数据生成器，请将该程序从配置文件中移除。')
-				if (not prob.all and match != 1 and not base.any_prefix(rjoin(prob.route, user, algo))):
-					continue
-				while os.path.exists('tmp'):
-					try:
-						shutil.rmtree('tmp')
-					except:
-						time.sleep(1e-2)
-				if prob['type'] == 'program':
-					while True:
-						try:
-							os.makedirs('tmp')
-						except:
-							time.sleep(1e-2)
-						else:
-							break
-					try:
-						shutil.copy(path, pjoin('tmp', path.split('/')[-1]))
-					except Exception as e:
-						log.error(u'程序`%s`没有找到。' % path)
-						log.info(e)
-						log.info(u'如果该程序是测试程序，请确保该程序存在；如果不是，请将其从`conf.*`中移除。')
-						continue
-				elif prob['type'] == 'output':
-					for i in range(20):
-						try:
-							shutil.copytree(path, 'tmp')
-						except Exception as e:
-							time.sleep(1e-2)
-							log.error(u'测试输出文件包`%s`没有找到或复制失败，正在重试 %d / 20。' % (path, i + 1))
-							log.info(e)
-						else:
-							break
-					else:
-						log.error(u'跳过该输出文件包。')
-						log.info(u'如果该文件包是测试输出，请确保该文件包存在；如果不是，请将其从`conf.*`中移除。')
-				log.info(u'测试程序 %s:%s:%s' % (prob['name'], user, algo))
-				scores, times, reports = test(prob, path.split('/')[-1].split('.')[0])
-				while os.path.exists('tmp'):
-					try:
-						shutil.rmtree('tmp')
-					except:
-						pass
-				tc = len(prob.test_cases)
-				score_map = {}
-				for i in range(tc):
-					score_map[prob.test_cases[i]] = i
-				if prob.packed:
-					packed = packed_score(scores[:tc], times[:tc], reports[:tc], score_map, prob)
-					tot = sum(packed[0][:-1])
-					scores = scores[:tc] + packed[0] + scores[tc:]
-					times = times[:tc] + packed[1] + times[tc:]
-					reports = reports[:tc] + packed[2] + reports[tc:]
-					for i, s in enumerate(packed[0][:-1]):
-						case_features[i].append(s)
-				elif tc > 0:
-					ratio = 100. / tc
-					scores = [score * ratio for score in scores[:tc] + [sum(scores[:tc])] + scores[tc:]]
-					packed = packed_score(scores[:tc], times[:tc], reports[:tc], score_map, prob)
-					tot = sum(scores[:tc])
-					times = times[:tc] + [sum((val for idx, val in enumerate(times[:tc]) if scores[idx] > 0))] + times[tc:]
-					reports = reports[:tc] + [''] + reports[tc:]
-					for i, s in enumerate(packed[0][:-1]):
-						case_features[i].append(s)
-				else:
-					# FIXME: Do I do this?
-					tot = sum(scores)
-					scores = [0.0, 0.0] + scores
-					times = [0.0, 0.0] + times
-					reports = ['', ''] + reports
-
-				if not prob.expect(user, algo, tot):
-					log.error(u'未达到预期。预期分数 %s ，实际得分 %.2f' % (algo_obj['expected'], tot))
-					prob_failed = True
-
-				scores = map(lambda i : '%.2f' % i, scores)
-				times = map(lambda i : '%.3f' % i, times)
-				reports = map(lambda i : i.replace('\n', '\\n').replace(',', ';').replace('\r', ''), reports)
-				for title, line in [(user, scores), (algo, times), ('', reports)]:
-					fres.write('%s,%s\n' % (title, ','.join(line)))
-	used_features = {}
-	for i, f in enumerate(case_features):
-		tf = tuple(f)
-		if tf in used_features:
-			log.warning(u'没有程序区分数据包%s和%s。' % (prob.data[used_features[tf]]['cases'], prob.data[i]['cases']))
-			log.info(u'对每种不同类型的数据，都应当有程序可以被这些数据区分。')
-		else:
-			used_features[tf] = i
-	if base.start_file:
-		base.xopen_file(pjoin('result', prob.route) + '.csv')
-	return not prob_failed
-
-def test_progs():
-	test_failed = False
-	if base.conf.folder != 'problem' and not os.path.exists('result'):
-		os.makedirs('result')
-	for day in base.days():
-		path = pjoin('result', day.route)
-		if not os.path.exists(path):
-			os.makedirs(path)
-	for prob in base.probs():
-		try:
-			if not test_problem(prob):
-				test_failed = True
-		except Exception as e:
-			log.error(traceback.format_exc())
-	return not test_failed
-
-if __name__ == '__main__':
-	try:
-		if base.init():
-			base.work = 'test'
-			if base.do_pack:
-				from . import packer
-				base.run_exc(packer.test)
-			ex, success = base.run_exc(test_progs)
-			if ex or not success:
-				sys.exit(1)
-		else:
-			log.info(u'这是测试出题人数据和程序的测试器，测试器没有细分的工作。')
-			sys.exit(1)
-	except base.NoFileException as e:
-		log.error(e)
-		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
-		sys.exit(1)
+# -*- coding: utf-8 -*-
+
+from __future__ import print_function
+import os
+import re
+import sys
+import json
+import datetime
+import shutil
+import subprocess
+import time
+import signal
+import zipfile
+from multiprocessing import Process, Queue
+from functools import wraps
+from threading import Timer
+import platform
+from . import base
+from .base import log, pjoin, rjoin
+import traceback
+
+def time2float(inp):
+	m = re.match(r'(\d*)(:|h)(\d*)(:|m)(\d*\.?\d*)s?', inp)
+	if m:
+		return float(m.group(1)) * 3600 + float(m.group(3)) * 60 + float(m.group(5))
+	m = re.match(r'(\d*)(:|m)(\d*\.?\d*)s?', inp)
+	if m:
+		return float(m.group(1)) * 60 + float(m.group(3))
+	m = re.match(r'(\d*\.?\d*)s?', inp)
+	if m:
+		return float(m.group(1))
+	raise Exception('Timer broken')
+
+def run_windows(name, tl, ml, input = None, output = None, vm = None):
+	'''
+	On windows, memory limit is not considered.
+	'''
+	timer = time.perf_counter if base.python_version >= (3, 3) else time.clock
+	try:
+		fin = (open(input) if input else None)
+		fout = (open(output, 'w') if output else None)
+		t = timer()
+		pro = subprocess.Popen(vm(name, ml) if vm else name, stdin = fin, stdout = fout)
+		if fout:
+			fout.close()
+		if fin:
+			fin.close()
+	except:
+		return 'Can\'t run program.', 0.0
+	while True:
+		ret = pro.poll()
+		if ret != None:
+			t = timer() - t
+			if ret == 0:
+				ret = None
+			else:
+				ret = 'Runtime error %d.' % ret
+			break
+		if (timer() - t) >= tl * base.time_multiplier:
+			pro.kill()
+			t = 0.0
+			ret = 'Time out.'
+			break
+		time.sleep(1e-2)
+	time.sleep(1e-2)
+	return ret, t
+
+def runner_linux(name, que, ml, input = None, output = None, vm = None):
+	pro = subprocess.Popen(
+		'%s time -f "%%%s" -o timer %s %s %s' % (
+			'ulimit -v %d;' % int(base.Memory(ml).KB) if vm != base.runners['java'] else '',
+			'U' if base.user_time else 'E',
+			vm(name, ml) if vm else './%s' % name,
+			'< %s' % input if input else '',
+			'> %s' % output if output else '',
+		),
+		shell = True,
+		preexec_fn = os.setsid
+	)
+	que.put(pro.pid)
+	ret = pro.wait()
+	que.put(ret)
+	
+def run_linux(name, tl, ml, input = None, output = None, vm = None):
+	que = Queue()
+	pro = Process(target = runner_linux, args = (name, que, ml, input, output, vm))
+	pro.start()
+	pro.join(tl * base.time_multiplier)
+	if que.qsize() == 0:
+		log.error('Runner broken.')
+	elif que.qsize() == 1:
+		ret = 'Time out.'
+		pid = que.get()
+		os.killpg(os.getpgid(pid), signal.SIGTERM)
+		t = 0.
+	else:
+		pid = que.get()
+		ret = que.get()
+		if ret == 0:
+			try:
+				t = time2float(open('timer').readline())
+			except Exception as e:
+				log.warning('Timer broken.')
+				t = 0.
+			ret = None
+		else:
+			ret = 'Runtime error %d.(MLE will cause RE as well in linux)' % ret
+			t = 0.
+	return ret, t
+
+def runner_mac(name, que, ml, input = None, output = None, vm = None):
+	pro = subprocess.Popen(
+		'ulimit -n %d; (time -p %s %s %s) 2> timer' % (
+			int(base.Memory(ml).KB),
+			vm(name, ml) if vm else './%s' % name,
+			'< %s' % input if input else '',
+			'> %s' % output if output else '',
+		),
+		shell = True,
+		preexec_fn = os.setsid
+	)
+	que.put(pro.pid)
+	ret = pro.wait()
+	que.put(ret)
+
+def run_mac(name, tl, ml, input = None, output = None, vm = None):
+	que = Queue()
+	pro = Process(target = runner_mac, args = (name, que, ml, input, output, vm))
+	pro.start()
+	pro.join(tl * base.time_multiplier)
+	if que.empty():
+		log.error('Runner broken.')
+	else:
+		pid = que.get()
+		if que.empty():
+			ret = 'Time out.'
+			os.killpg(os.getpgid(pid), signal.SIGTERM)
+			t = 0.
+		else:
+			ret = que.get()
+			if ret == 0:
+				try:
+					with open('timer') as f:
+						for i in range(2 if base.user_time else 1):
+							line = f.readline()
+						t = time2float(line.strip().split()[-1])
+				except:
+					base.warning('Timer broken.')
+					t = 0.
+				ret = None
+			else:
+				ret = 'Runtime error %d.' % ret
+				t = 0.
+	return ret, t
+
+if base.system == 'Linux':
+	base.check_install('time')
+	run = run_linux
+elif base.system == 'Windows':
+	run = run_windows
+elif base.system == 'Darwin':
+	run = run_mac
+else:
+	run = run_linux
+	log.warning(u'未知的操作系统，尝试当做Linux运行。')
+	
+def compile(prob, name):
+	for lang, args in prob['compile'].items():
+		if os.path.exists(pjoin('tmp', name + '.' + lang)):
+			base.check_install(lang)
+			os.chdir('tmp')
+			try:
+				ret = subprocess.call(
+					base.compilers[lang](name, args, base.macros[base.work], ml = prob.ml()),
+					shell = True,
+					stdout = open('stdout', 'w'),
+					stderr = open('stderr', 'w')
+				)
+			except Exception as e:
+				with open('stderr', 'a') as f:
+					f.write(str(e))
+				ret = -1
+			os.chdir('..')
+			if ret:
+				log.info('`' + name + '.' + lang + u'`编译失败，详情见`compile.log`。')
+				with open('compile.log', 'a') as f:
+					import __main__
+					f.write(u'## 脚本%s/，工程路径%s，参数%s，开始于%s。\n' % (__main__.__file__, os.getcwd(), str(sys.argv[1:]), str(datetime.datetime.now())))
+					f.write(u'## 测试题目`%s`，编译失败代码名称`%s.%s`\n' % (prob['name'], name, lang))
+					try:
+						f.write(u'编译器输出的stdout为：\n')
+						f.write(open('tmp/stdout').read())
+					except Exception as e:
+						f.write(u'编译器没有输出stdout，具体错误为：\n')
+						f.write(str(e) + '\n')
+					try:
+						f.write(u'编译器输出的stderr为：\n')
+						f.write(open('tmp/stderr').read())
+					except Exception as e:
+						f.write(u'编译器没有输出stderr，具体错误为：\n')
+						f.write(str(e) + '\n')
+				raise Exception('`' + name + '.' + lang + '` compile failed.')
+			return lang
+	else:
+		raise Exception('Can\'t find source file.')
+
+def test(prob, name):
+	scores = []
+	times = []
+	reports = []
+	if prob['type'] == 'program':
+		try:
+			lang = compile(prob, name)
+		except Exception as e:
+			for i in range(len(prob.test_cases) + len(prob.sample_cases)):
+				scores.append(0.0)
+				times.append(0.0)
+				reports.append(str(e))
+			return scores, times, reports
+	all_cases = prob.test_cases + prob.sample_cases + prob.pre_cases
+	for case in all_cases:
+		print('Case %s:%s  ' % (case['key'], case), end = '\r')
+		sys.stdout.flush()
+		shutil.copy(case.full() + '.in', pjoin('tmp', 'in'))
+		shutil.copy(case.full() + '.ans', pjoin('tmp', 'ans'))
+		for fname in ('in', 'ans'):
+			if not ('binary data' in prob and prob['binary data'] == True):
+				if base.system == 'Windows':
+					base.unix2dos(pjoin('tmp', fname))
+				else:
+					base.dos2unix(pjoin('tmp', fname))
+		if prob['type'] == 'program':
+			os.chdir('tmp')
+			ret, time = run(name, prob['time limit'], prob['memory limit'], 'in', 'out', base.runners[lang])
+			os.chdir('..')
+		elif prob['type'] == 'output':
+			if os.path.exists(pjoin('tmp', case['case'] + '.out')):
+				shutil.copy(pjoin('tmp', case['case'] + '.out'), pjoin('tmp', 'out'))
+				ret = None
+				time = 0.0
+			else:
+				ret = 'Output file does not exist.'
+				time = 0.0
+		else:
+			log.error(u'错误的题目类型`%s`。' % prob['type'])
+			raise Exception('problem type error.')
+		if not ret:
+			if not os.path.exists(pjoin('tmp', 'out')):
+				ret = 'Output file does not exist.'
+				time = 0.0
+				score = 0.0
+			elif prob.chk:
+				shutil.copy(pjoin('bin', prob.route), pjoin('tmp', 'chk' + base.elf_suffix))
+				open('100.0', 'w').write('100.0\n')
+				os.system('%s %s %s %s 100.0 tmp/score tmp/info' % (
+					pjoin('tmp', 'chk' + base.elf_suffix),
+					pjoin('tmp', 'in'),
+					pjoin('tmp', 'out'),
+					pjoin('tmp', 'ans')
+				))
+				os.remove('100.0')
+				try:
+					arbiter_out = ('/' if base.system != 'Windows' else '') + 'tmp/_eval.score'
+					f = open(arbiter_out)
+					report = f.readline().strip()
+					score = float(f.readline()) * 0.1
+					f.close()
+					shutil.remove(arbiter_out)
+				except Exception as e:
+					try:
+						report = open('tmp/info').read().strip()
+					except Exception as e:
+						report = ''
+					score = float(open('tmp/score').readline()) * .01
+				if time > prob['time limit']:
+					score = 0.0
+					report += '(but time out)'
+			else:
+				ret = os.system('%s %s %s > log' % (
+					base.diff_tool,
+					pjoin('tmp', 'ans'),
+					pjoin('tmp', 'out')
+				))
+				if ret == 0:
+					score = 1.0
+					report = 'ok'
+					if prob['type'] != 'output' and time > prob['time limit']:
+						score = 0.0
+						report += '(but time out)'
+				else:
+					score = 0.0
+					report = 'wa'
+					if prob['type'] != 'output' and time > prob['time limit']:
+						report += '(and time out)'
+		else:
+			score = 0.0
+			report = ret
+		while os.path.exists(pjoin('tmp', prob['name'] + '.out')):
+			try:
+				os.remove(pjoin('tmp', prob['name'] + '.out'))
+			except:
+				pass
+		scores.append(score)
+		times.append(time)
+		reports.append(report)
+	return scores, times, reports
+
+def packed_score(scores, times, reports, score_map, prob):
+	pscore = []
+	ptime = []
+	preport = []
+	for datum in prob.data:
+		pscore.append(datum.score * min((scores[score_map[i]] for i in datum['cases'])))
+		ptime.append(sum((times[score_map[i]] for i in datum['cases'] if scores[score_map[i]] > 0)))
+		preport.append('Total %.1f' % datum.score)
+	pscore.append(sum(pscore))
+	ptime.append(sum(ptime))
+	preport.append('')
+	return (pscore, ptime, preport)
+	
+def test_problem(prob):
+	log.info(u'尝试评测题目`%s`。' % prob.route)
+	if 'users' not in prob:
+		log.warning(u'题目`%s`缺少`users`字段，没有找到出题人的程序。' % prob.route)
+		log.info(u'你需要在工程中放置你的代码，然后使用`python -m tuack.gen code`搜索源代码，或直接配置`users`字段。')
+		return
+	if 'data' not in prob or len(prob.test_cases) == 0:
+		log.warning(u'题目`%s`缺少`data`字段，找不到测试数据。' % prob.route)
+		log.info(u'你需要在文件夹`%s`下按*.in和*.ans格式存放测试数据，' % pjoin(prob.path, 'data'))
+		log.info(u'然后使用`python -m tuack.gen data`添加它们或直接配置`data`字段。')
+	if 'samples' not in prob or len(prob.sample_cases) == 0:
+		log.warning(u'题目`%s`缺少`samples`字段，找不到样例数据。' % prob.route)
+		log.info(u'你需要在文件夹`%s`下按*.in和*.ans格式存放样例数据，' % pjoin(prob.path, 'down'))
+		log.info(u'然后使用`python -m tuack.gen samples`添加它们或直接配置`samples`字段。')
+	if 'pre' in prob and len(prob.pre_cases) == 0:
+		log.warning(u'题目`%s`的`pre`字段为空，找不到预测试数据。' % prob.route)
+		log.info(u'如果这道题目有预测试数据，你需要在文件夹`%s`下按*.in和*.ans格式存放预测试数据，' % pjoin(prob.path, 'pre'))
+		log.info(u'然后使用`python -m tuack.gen pre`在文件夹`%s`下搜索预测试数据。' % (pjoin(prob.path, 'pre')))
+		log.info(u'如果这道题目没有预测试数据，你需要删除`conf.*`中的`pre`字段。')
+	if len(prob.data) == 1 and prob.data[0].get('score') != 100:
+		log.warning(u'题目`%s`的`data`字段只有一个元素，可能没有正确配置数据。' % prob.route)
+		log.info(u'如果是一个包的CPC赛制，需要在这个元素中配置`score`项为100。')
+		log.info(u'如果是多点或多子任务的赛制，需要将每类数据分类配置或打包配置。')
+		log.info(u'详情请见%s。' % base.wiki(u'配置题目#数据'))
+	if 'binary data' in prob and prob['binary data'] == True:
+		log.info(u'本题数据为二进制文件，测试时不进行换行符转换')
+	log.info(u'共%d组样例，%d个预测试点，%d个测试点，%s打包评测%s。' % (
+		len(prob.sample_cases),
+		len(prob.pre_cases),
+		len(prob.test_cases),
+		u'是' if prob.packed else u'不是',
+		(u'（共%d个包）' % len(prob.data) if len(prob.data) != 1 else u'（看样子是一个包的CPC赛制）') if prob.packed else ''
+	))
+
+	prob_failed = False
+
+	case_features = [[] for i in range(len(prob.data))]
+
+	with open(pjoin('result', prob.route) + '.csv', 'w') as fres:
+		fres.write('%s,%s%s,summary,sample%s,pre%s\n' % (
+			prob['name'],
+			','.join(prob.test_cases),
+			',' + ','.join(map(lambda datum : '{' + ';'.join(map(str, datum['cases'])) + '}', prob.data)) \
+				if prob.packed else '',
+			','.join(prob.sample_cases),
+			','.join(prob.pre_cases)
+		))
+		for user, algos in prob.users().items():
+			if not prob.all:
+				match = base.any_prefix(rjoin(prob.route, user))
+				if not match:
+					continue
+			for algo, algo_obj in algos.items():
+				path = algo_obj['path']
+				expe = algo_obj.get('expected')
+				if not expe or len(expe) == 0:
+					log.warning(u'程序`%s/%s`没有设置期望得分。' % (user, algo))
+					log.info(u'如果该程序是标程、部分分程序或骗分程序等，需要设置它的`expected`字段。')
+					log.info(u'有多种设置的格式，例如：`== 60`表示该程序应该得到60分。')
+					log.info(u'如果该程序是其他功能程序，例如数据生成器，请将该程序从配置文件中移除。')
+				if (not prob.all and match != 1 and not base.any_prefix(rjoin(prob.route, user, algo))):
+					continue
+				while os.path.exists('tmp'):
+					try:
+						shutil.rmtree('tmp')
+					except:
+						time.sleep(1e-2)
+				if prob['type'] == 'program':
+					while True:
+						try:
+							os.makedirs('tmp')
+						except:
+							time.sleep(1e-2)
+						else:
+							break
+					try:
+						shutil.copy(path, pjoin('tmp', path.split('/')[-1]))
+					except Exception as e:
+						log.error(u'程序`%s`没有找到。' % path)
+						log.info(e)
+						log.info(u'如果该程序是测试程序，请确保该程序存在；如果不是，请将其从`conf.*`中移除。')
+						continue
+				elif prob['type'] == 'output':
+					for i in range(20):
+						try:
+							shutil.copytree(path, 'tmp')
+						except Exception as e:
+							time.sleep(1e-2)
+							log.error(u'测试输出文件包`%s`没有找到或复制失败，正在重试 %d / 20。' % (path, i + 1))
+							log.info(e)
+						else:
+							break
+					else:
+						log.error(u'跳过该输出文件包。')
+						log.info(u'如果该文件包是测试输出，请确保该文件包存在；如果不是，请将其从`conf.*`中移除。')
+				log.info(u'测试程序 %s:%s:%s' % (prob['name'], user, algo))
+				scores, times, reports = test(prob, path.split('/')[-1].split('.')[0])
+				while os.path.exists('tmp'):
+					try:
+						shutil.rmtree('tmp')
+					except:
+						pass
+				tc = len(prob.test_cases)
+				score_map = {}
+				for i in range(tc):
+					score_map[prob.test_cases[i]] = i
+				if prob.packed:
+					packed = packed_score(scores[:tc], times[:tc], reports[:tc], score_map, prob)
+					tot = sum(packed[0][:-1])
+					scores = scores[:tc] + packed[0] + scores[tc:]
+					times = times[:tc] + packed[1] + times[tc:]
+					reports = reports[:tc] + packed[2] + reports[tc:]
+					for i, s in enumerate(packed[0][:-1]):
+						case_features[i].append(s)
+				elif tc > 0:
+					ratio = 100. / tc
+					scores = [score * ratio for score in scores[:tc] + [sum(scores[:tc])] + scores[tc:]]
+					packed = packed_score(scores[:tc], times[:tc], reports[:tc], score_map, prob)
+					tot = sum(scores[:tc])
+					times = times[:tc] + [sum((val for idx, val in enumerate(times[:tc]) if scores[idx] > 0))] + times[tc:]
+					reports = reports[:tc] + [''] + reports[tc:]
+					for i, s in enumerate(packed[0][:-1]):
+						case_features[i].append(s)
+				else:
+					# FIXME: Do I do this?
+					tot = sum(scores)
+					scores = [0.0, 0.0] + scores
+					times = [0.0, 0.0] + times
+					reports = ['', ''] + reports
+
+				if not prob.expect(user, algo, tot):
+					log.error(u'未达到预期。预期分数 %s ，实际得分 %.2f' % (algo_obj['expected'], tot))
+					prob_failed = True
+
+				scores = map(lambda i : '%.2f' % i, scores)
+				times = map(lambda i : '%.3f' % i, times)
+				reports = map(lambda i : i.replace('\n', '\\n').replace(',', ';').replace('\r', ''), reports)
+				for title, line in [(user, scores), (algo, times), ('', reports)]:
+					fres.write('%s,%s\n' % (title, ','.join(line)))
+	used_features = {}
+	for i, f in enumerate(case_features):
+		tf = tuple(f)
+		if tf in used_features:
+			log.warning(u'没有程序区分数据包%s和%s。' % (prob.data[used_features[tf]]['cases'], prob.data[i]['cases']))
+			log.info(u'对每种不同类型的数据，都应当有程序可以被这些数据区分。')
+		else:
+			used_features[tf] = i
+	if base.start_file:
+		base.xopen_file(pjoin('result', prob.route) + '.csv')
+	return not prob_failed
+
+def test_progs():
+	test_failed = False
+	if base.conf.folder != 'problem' and not os.path.exists('result'):
+		os.makedirs('result')
+	for day in base.days():
+		path = pjoin('result', day.route)
+		if not os.path.exists(path):
+			os.makedirs(path)
+	for prob in base.probs():
+		try:
+			if not test_problem(prob):
+				test_failed = True
+		except Exception as e:
+			log.error(traceback.format_exc())
+	return not test_failed
+
+if __name__ == '__main__':
+	try:
+		if base.init():
+			base.work = 'test'
+			if base.do_pack:
+				from . import packer
+				base.run_exc(packer.test)
+			ex, success = base.run_exc(test_progs)
+			if ex or not success:
+				sys.exit(1)
+		else:
+			log.info(u'这是测试出题人数据和程序的测试器，测试器没有细分的工作。')
+			sys.exit(1)
+	except base.NoFileException as e:
+		log.error(e)
+		log.info(u'尝试使用`python -m tuack.gen -h`获取如何生成一个工程。')
+		sys.exit(1)
```

### Comparing `tuack-0.1.4.9.2/tuack.egg-info/SOURCES.txt` & `tuack-0.1.5/tuack.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+LICENSE
 MANIFEST.in
 README.md
 setup.py
 tuack/__init__.py
 tuack/base.py
 tuack/doc.py
 tuack/dump.py
@@ -28,14 +29,15 @@
 tuack/lex/lex.yy.c
 tuack/lex/lex.yy.o
 tuack/lex/main.h
 tuack/lex/yacc.tab.c
 tuack/lex/yacc.tab.h
 tuack/lex/yacc.tab.o
 tuack/lex/yacc.y
+tuack/sample/arbiter_e.noi_linux1.sample
 tuack/sample/arbiter_e.sample
 tuack/sample/chk.cpp
 tuack/sample/contest.gitignore
 tuack/sample/contest.json
 tuack/sample/day.gitignore
 tuack/sample/day.json
 tuack/sample/empty.gitattributes
```

