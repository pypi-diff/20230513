# Comparing `tmp/tiivad-0.0.8.tar.gz` & `tmp/tiivad-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tiivad-0.0.8.tar", last modified: Sun Mar 26 20:23:51 2023, max compression
+gzip compressed data, was "tiivad-0.0.9.tar", last modified: Thu Mar 30 19:03:04 2023, max compression
```

## Comparing `tiivad-0.0.8.tar` & `tiivad-0.0.9.tar`

### file list

```diff
@@ -1,33 +1,33 @@
-drwxrwxrwx   0        0        0        0 2023-03-26 20:23:51.242812 tiivad-0.0.8/
--rw-rw-rw-   0        0        0     1087 2023-03-26 20:19:39.000000 tiivad-0.0.8/LICENSE.txt
--rw-rw-rw-   0        0        0      251 2023-03-26 20:23:51.241812 tiivad-0.0.8/PKG-INFO
--rw-rw-rw-   0        0        0      842 2023-03-26 20:19:39.000000 tiivad-0.0.8/README.md
-drwxrwxrwx   0        0        0        0 2023-03-26 20:23:51.198701 tiivad-0.0.8/docker/
--rw-rw-rw-   0        0        0    14146 2023-03-26 20:19:39.000000 tiivad-0.0.8/docker/assessment_code.py
--rw-rw-rw-   0        0        0     1048 2023-03-26 20:19:39.000000 tiivad-0.0.8/docker/kodu1.py
--rw-rw-rw-   0        0        0       42 2023-03-26 20:23:51.242812 tiivad-0.0.8/setup.cfg
--rw-rw-rw-   0        0        0      324 2023-03-26 20:22:22.000000 tiivad-0.0.8/setup.py
-drwxrwxrwx   0        0        0        0 2023-03-26 20:23:51.227844 tiivad-0.0.8/tiivad/
--rw-rw-rw-   0        0        0     1049 2023-03-13 19:20:53.000000 tiivad-0.0.8/tiivad/__init__.py
--rw-rw-rw-   0        0        0    23670 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/edutest.py
--rw-rw-rw-   0        0        0     3368 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/file.py
--rw-rw-rw-   0        0        0    21498 2023-03-13 19:37:23.000000 tiivad-0.0.8/tiivad/function.py
--rw-rw-rw-   0        0        0     9872 2023-03-13 19:20:53.000000 tiivad-0.0.8/tiivad/function_execution.py
--rw-rw-rw-   0        0        0    19331 2023-03-26 20:19:40.000000 tiivad-0.0.8/tiivad/functions.py
--rw-rw-rw-   0        0        0    19331 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/functions_OLD.py
--rw-rw-rw-   0        0        0     4076 2023-03-13 19:41:15.000000 tiivad-0.0.8/tiivad/help_structures.py
--rw-rw-rw-   0        0        0    12503 2023-03-26 20:19:40.000000 tiivad-0.0.8/tiivad/prog_kontroll.py
--rw-rw-rw-   0        0        0    12503 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/prog_kontroll_OLD.py
--rw-rw-rw-   0        0        0    12503 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/progkontroll.py
--rw-rw-rw-   0        0        0    20189 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/program.py
--rw-rw-rw-   0        0        0     5455 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/program_execution.py
--rw-rw-rw-   0        0        0     3117 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/results.py
--rw-rw-rw-   0        0        0     1059 2023-03-26 20:19:40.000000 tiivad-0.0.8/tiivad/solution.py
--rw-rw-rw-   0        0        0      254 2023-03-13 16:08:47.000000 tiivad-0.0.8/tiivad/t.py
--rw-rw-rw-   0        0        0    23028 2023-03-26 20:06:24.000000 tiivad-0.0.8/tiivad/tests.py
--rw-rw-rw-   0        0        0    13477 2023-03-13 19:37:23.000000 tiivad-0.0.8/tiivad/utils.py
-drwxrwxrwx   0        0        0        0 2023-03-26 20:23:51.240804 tiivad-0.0.8/tiivad.egg-info/
--rw-rw-rw-   0        0        0      251 2023-03-26 20:23:51.000000 tiivad-0.0.8/tiivad.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      564 2023-03-26 20:23:51.000000 tiivad-0.0.8/tiivad.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-03-26 20:23:51.000000 tiivad-0.0.8/tiivad.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       19 2023-03-26 20:23:51.000000 tiivad-0.0.8/tiivad.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-03-30 19:03:04.229617 tiivad-0.0.9/
+-rw-rw-rw-   0        0        0     1087 2023-03-26 20:19:39.000000 tiivad-0.0.9/LICENSE.txt
+-rw-rw-rw-   0        0        0      251 2023-03-30 19:03:04.227944 tiivad-0.0.9/PKG-INFO
+-rw-rw-rw-   0        0        0      842 2023-03-26 20:19:39.000000 tiivad-0.0.9/README.md
+drwxrwxrwx   0        0        0        0 2023-03-30 19:03:04.144781 tiivad-0.0.9/docker/
+-rw-rw-rw-   0        0        0    13796 2023-03-26 20:27:12.000000 tiivad-0.0.9/docker/assessment_code.py
+-rw-rw-rw-   0        0        0     1048 2023-03-26 20:19:39.000000 tiivad-0.0.9/docker/submission.py
+-rw-rw-rw-   0        0        0       42 2023-03-30 19:03:04.229617 tiivad-0.0.9/setup.cfg
+-rw-rw-rw-   0        0        0      324 2023-03-30 19:02:47.000000 tiivad-0.0.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-03-30 19:03:04.203240 tiivad-0.0.9/tiivad/
+-rw-rw-rw-   0        0        0     1049 2023-03-13 19:20:53.000000 tiivad-0.0.9/tiivad/__init__.py
+-rw-rw-rw-   0        0        0    23670 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/edutest.py
+-rw-rw-rw-   0        0        0     3368 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/file.py
+-rw-rw-rw-   0        0        0    21498 2023-03-13 19:37:23.000000 tiivad-0.0.9/tiivad/function.py
+-rw-rw-rw-   0        0        0     9872 2023-03-13 19:20:53.000000 tiivad-0.0.9/tiivad/function_execution.py
+-rw-rw-rw-   0        0        0    19331 2023-03-26 20:19:40.000000 tiivad-0.0.9/tiivad/functions.py
+-rw-rw-rw-   0        0        0    19331 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/functions_OLD.py
+-rw-rw-rw-   0        0        0     4076 2023-03-13 19:41:15.000000 tiivad-0.0.9/tiivad/help_structures.py
+-rw-rw-rw-   0        0        0    12503 2023-03-26 20:19:40.000000 tiivad-0.0.9/tiivad/prog_kontroll.py
+-rw-rw-rw-   0        0        0    12503 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/prog_kontroll_OLD.py
+-rw-rw-rw-   0        0        0    12503 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/progkontroll.py
+-rw-rw-rw-   0        0        0    20189 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/program.py
+-rw-rw-rw-   0        0        0     5455 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/program_execution.py
+-rw-rw-rw-   0        0        0     3117 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/results.py
+-rw-rw-rw-   0        0        0     1059 2023-03-26 20:19:40.000000 tiivad-0.0.9/tiivad/solution.py
+-rw-rw-rw-   0        0        0      254 2023-03-13 16:08:47.000000 tiivad-0.0.9/tiivad/t.py
+-rw-rw-rw-   0        0        0    23275 2023-03-29 14:58:12.000000 tiivad-0.0.9/tiivad/tests.py
+-rw-rw-rw-   0        0        0    13477 2023-03-13 19:37:23.000000 tiivad-0.0.9/tiivad/utils.py
+drwxrwxrwx   0        0        0        0 2023-03-30 19:03:04.226950 tiivad-0.0.9/tiivad.egg-info/
+-rw-rw-rw-   0        0        0      251 2023-03-30 19:03:04.000000 tiivad-0.0.9/tiivad.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      569 2023-03-30 19:03:04.000000 tiivad-0.0.9/tiivad.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-03-30 19:03:04.000000 tiivad-0.0.9/tiivad.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       19 2023-03-30 19:03:04.000000 tiivad-0.0.9/tiivad.egg-info/top_level.txt
```

### Comparing `tiivad-0.0.8/LICENSE.txt` & `tiivad-0.0.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/README.md` & `tiivad-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/docker/assessment_code.py` & `tiivad-0.0.9/docker/assessment_code.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,151 +1,150 @@
 from tiivad import *
 
-validate_files(['''kodu1.py'''])
-execute_test(file_name='''kodu1.py''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ALL_OF_THESE''', nothing_else=None, expected_output=['''turtle'''],
-                         before_message='''Kontrollib, kas programm impordib mooduli.''',
-                         passed_message='''Programm importis mooduli.''',
-                         failed_message='''Programm ei importinud moodulit.''')],
-             type='''program_imports_module_test''', points=10.0, id=None, name='''Programm importib mooduli turtle.''',
-             inputs=None, passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                         expected_output=['''down''', '''up''', '''forward''', '''left''', '''right''', '''fd''',
-                                          '''rt''', '''lt''', '''bk''', '''goto'''],
-                         before_message='''Kontrollib, kas programm kutsub välja turtle funktsiooni.''',
-                         passed_message='''Programm kutsus välja vähemalt ühe turtle funktsiooni.''',
-                         failed_message='''Programm ei kutsnud välja ühtegi turtle funktsiooni.''')],
+validate_files(['''submission.py'''])
+execute_test(file_name='''submission.py''', standard_input_data=['''Kasutajasisend'''],
+             input_files=[('''sisendfail.txt''', '''Sisendfaili sisu.''')], generic_checks=[
+        GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None, expected_value=['''down''', '''up'''],
+                      consider_elements_order=False, before_message='''Kontrollib, kas väljund sisaldab võtmesõna.''',
+                      passed_message='''Programmi väljund sisaldab antud võtmesõna.''',
+                      failed_message='''Programmi väljund ei sisalda antud võtmesõna.''')], output_file_checks=[
+        OutputFileChecks(file_name='''valjundfail.txt''', check_type='''ALL_OF_THESE''', nothing_else=None,
+                         expected_value=['''Väljundfaili eeldatav sisu'''], consider_elements_order=False,
+                         before_message='''Kontrollib, kas väljundfail sisaldab võtmesõna.''',
+                         passed_message='''Programmi väljundfail sisaldab antud võtmesõna.''',
+                         failed_message='''Programmi väljundfail ei sisalda antud võtmesõna.''')], exception_check=True,
+             before_message=None, passed_message=None, failed_message=None, type='''program_execution_test''',
+             points=1.0, id=None, name='''Programmi käivituse test.''', inputs=None, passed_next=None, failed_next=None,
+             visible_to_user=None)
+execute_test(file_name='''submission.py''', generic_checks=[
+    GenericChecks(check_type='''ALL_OF_THESE''', nothing_else=None, expected_value=['''turtle'''],
+                  before_message='''Kontrollib, kas programm impordib mooduli.''',
+                  passed_message='''Programm importis mooduli.''',
+                  failed_message='''Programm ei importinud moodulit.''')], type='''program_imports_module_test''',
+             points=10.0, id=None, name='''Programm impordib mooduli''', inputs=None, passed_next=None,
+             failed_next=None, visible_to_user=None)
+execute_test(file_name='''submission.py''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None, expected_value=['''close'''],
+                  before_message='''Kontrollib, kas programm kutsub välja turtle funktsiooni.''',
+                  passed_message='''Programm kutsus välja vähemalt ühe turtle funktsiooni.''',
+                  failed_message='''Programm ei kutsnud välja ühtegi turtle funktsiooni.''')],
              type='''program_calls_function_test''', points=1.0, id=None,
              name='''Programm kutsub välja turtle funktsiooni.''', inputs=None, passed_next=None, failed_next=None,
              visible_to_user=None)
-execute_test(file_name='''kodu1.py''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', contains_check=False,
              before_message='''Kontrollib, kas programmis esineb tsükkel.''',
              passed_message='''Programmis esines tsükkel.''', failed_message='''Programmis ei esine ühtegi tsüklit.''',
              type='''program_contains_loop_test''', points=1.0, id=None, name='''Programmis esineb tsükkel.''',
              inputs=None, passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', contains_check=(False, True),
+execute_test(file_name='''submission.py''', contains_check=True,
              before_message='''Kontrollib, kas programmis esineb try/except plokk.''',
              passed_message='''Programmis ei esine try/except plokki.''',
              failed_message='''Programmis esines try/except plokk.''', type='''program_contains_try_except_test''',
              points=1.0, id=None, name='''Programmis ei tohi olla try/except plokki.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', contains_check=False,
              before_message='''Kontrollib, kas programm kutsub välja 'print' käsu.''',
              passed_message='''Programm kutsus välja 'print' käsu.''',
              failed_message='''Programm ei kutsunud välja 'print' käsku.''', type='''program_calls_print_test''',
              points=1.0, id=None, name='''Programm peab välja kutsuma 'print' käsu.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                         expected_output=['''down''', '''up''', '''seosta_lapsed_ja_vanemad'''],
-                         before_message='''Kontrollib, kas programm defineerib vähemalt ühe antud funktsioonidest.''',
-                         passed_message='''Programm defineeris vähemalt ühe antud funktsioonidest.''',
-                         failed_message='''Programm ei defineerinud välja ühtegi antud funktsioonidest.''')],
+execute_test(file_name='''submission.py''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None,
+                  expected_value=['''down''', '''up''', '''seosta_lapsed_ja_vanemad'''],
+                  before_message='''Kontrollib, kas programm defineerib vähemalt ühe antud funktsioonidest.''',
+                  passed_message='''Programm defineeris vähemalt ühe antud funktsioonidest.''',
+                  failed_message='''Programm ei defineerinud välja ühtegi antud funktsioonidest.''')],
              type='''program_defines_function_test''', points=1.0, id=None,
              name='''Programm defineerib vähemalt ühe antud funktsioonidest.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                         expected_output=['''seosta_lapsed_ja_vanemad''', '''yes''', '''no'''],
-                         consider_elements_order=None,
-                         before_message='''Kontrollib, kas programm sisaldab võtmesõna.''',
-                         passed_message='''Programm sisaldab võtmesõna.''',
-                         failed_message='''Programm ei sisalda võtmesõna.''')],
-             type='''program_contains_keyword_test''', points=1.0, id=None, name='''Programm sisaldab võtmesõna.''',
-             inputs=None, passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', standard_input_data=['''Kasutajasisend'''],
-             input_files=[('''sisendfail.txt''', '''Sisendfaili sisu.''')], standard_output_checks=[
-        StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                             expected_output=['''down''', '''up'''], consider_elements_order=False,
-                             before_message='''Kontrollib, kas väljund sisaldab võtmesõna.''',
-                             passed_message='''Programmi väljund sisaldab antud võtmesõna.''',
-                             failed_message='''Programmi väljund ei sisalda antud võtmesõna.''')], output_file_checks=[
-        OutputFileChecks(file_name='''valjundfail.txt''', string_check_type='''ALL_OF_THESE''', nothing_else=None,
-                         expected_output=['''Väljundfaili eeldatav sisu'''], consider_elements_order=False,
-                         before_message='''Kontrollib, kas väljundfail sisaldab võtmesõna.''',
-                         passed_message='''Programmi väljundfail sisaldab antud võtmesõna.''',
-                         failed_message='''Programmi väljundfail ei sisalda antud võtmesõna.''')],
-             exception_check=(False, True), before_message=None, passed_message=None, failed_message=None,
-             type='''program_execution_test''', points=1.0, id=None, name='''Programmi käivituse test.''', inputs=None,
-             passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None,
+                  expected_value=['''seosta_lapsed_ja_vanemad''', '''yes''', '''no'''], consider_elements_order=False,
+                  before_message='''Kontrollib, kas programm sisaldab võtmesõna.''',
+                  passed_message='''Programm sisaldab võtmesõna.''',
+                  failed_message='''Programm ei sisalda võtmesõna.''')], type='''program_contains_keyword_test''',
+             points=1.0, id=None, name='''Programm sisaldab võtmesõna.''', inputs=None, passed_next=None,
+             failed_next=None, visible_to_user=None)
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=False,
              before_message='''Kontrollib, kas funktsioonis esineb tsükkel.''',
              passed_message='''Funktsioonis esines tsükkel.''',
              failed_message='''Funktsioonis ei esine ühtegi tsüklit.''', type='''function_contains_loop_test''',
              points=1.0, id=None, name='''Funktsioonis esineb tsükkel.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None, expected_value=['''ff.close()''', '''no'''],
+                  consider_elements_order=False, before_message='''Kontrollib, kas funktsioon sisaldab võtmesõna.''',
+                  passed_message='''Funktsioon sisaldab võtmesõna.''',
+                  failed_message='''Funktsioon ei sisalda võtmesõna.''')], type='''function_contains_keyword_test''',
+             points=1.0, id=None, name='''Funktsioon sisaldab võtmesõna.''', inputs=None, passed_next=None,
+             failed_next=None, visible_to_user=None)
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=False,
              before_message='''Kontrollib, kas funktsioonis esineb return.''',
              passed_message='''Funktsioonis esines return.''',
              failed_message='''Funktsioonis ei esine ühtegi return'i.''', type='''function_contains_return_test''',
              points=1.0, id=None, name='''Funktsioonis esineb return.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                         expected_output=['''down''', '''up''', '''forward''', '''left''', '''right''', '''fd''',
-                                          '''rt''', '''lt''', '''bk''', '''goto'''],
-                         before_message='''Kontrollib, kas funktsioon kutsub välja turtle funktsiooni.''',
-                         passed_message='''Funktsioon kutsus välja vähemalt ühe turtle funktsiooni.''',
-                         failed_message='''Funktsioon ei kutsnud välja ühtegi turtle funktsiooni.''')],
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None,
+                  expected_value=['''down''', '''up''', '''forward''', '''left''', '''right''', '''fd''', '''rt''',
+                                  '''lt''', '''bk''', '''goto'''],
+                  before_message='''Kontrollib, kas funktsioon kutsub välja turtle funktsiooni.''',
+                  passed_message='''Funktsioon kutsus välja vähemalt ühe turtle funktsiooni.''',
+                  failed_message='''Funktsioon ei kutsnud välja ühtegi turtle funktsiooni.''')],
              type='''function_calls_function_test''', points=1.0, id=None,
              name='''Funktsioon kutsub välja turtle funktsiooni.''', inputs=None, passed_next=None, failed_next=None,
              visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=False,
              before_message='''Kontrollib, kas funktsioon kutsub välja print käsu.''',
              passed_message='''Funktsioon kutsub välja print käsu.''',
              failed_message='''Funktsioon ei kutsu välja print käsku.''', type='''function_calls_print_test''',
              points=1.0, id=None, name='''Funktsioon kutsub välja print käsu.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=False,
              before_message='''Kontrollib, kas funktsioon on rekursiivne.''',
              passed_message='''Funktsioonis on rekursiivne.''', failed_message='''Funktsioonis ei ole rekursiivne.''',
              type='''function_is_recursive_test''', points=1.0, id=None, name='''Funktsioonis on rekursiivne.''',
              inputs=None, passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                         expected_output=['''down''', '''up''', '''seosta_lapsed_ja_vanemad2'''],
-                         before_message='''Kontrollib, kas funktsioon defineerib vähemalt ühe antud funktsioonidest.''',
-                         passed_message='''Funktsioon defineeris vähemalt ühe antud funktsioonidest.''',
-                         failed_message='''Funktsioon ei defineerinud ühtegi antud funktsioonidest.''')],
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', generic_checks=[
+    GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None,
+                  expected_value=['''down''', '''up''', '''seosta_lapsed_ja_vanemad2'''],
+                  before_message='''Kontrollib, kas funktsioon defineerib vähemalt ühe antud funktsioonidest.''',
+                  passed_message='''Funktsioon defineeris vähemalt ühe antud funktsioonidest.''',
+                  failed_message='''Funktsioon ei defineerinud ühtegi antud funktsioonidest.''')],
              type='''function_defines_function_test''', points=1.0, id=None,
              name='''Funktsioon defineerib vähemalt ühe antud funktsioonidest.''', inputs=None, passed_next=None,
              failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', standard_output_checks=[
-    StandardOutputChecks(string_check_type='''ALL_OF_THESE''', nothing_else=None, expected_output=['''turtle'''],
-                         before_message='''Kontrollib, kas funktsioon impordib mooduli.''',
-                         passed_message='''Funktsioon importis mooduli.''',
-                         failed_message='''Funktsioon ei importinud moodulit.''')],
-             type='''function_imports_module_test''', points=1.0, id=None,
-             name='''Funktsioon importib mooduli turtle.''', inputs=None, passed_next=None, failed_next=None,
-             visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(False, True),
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', generic_checks=[
+    GenericChecks(check_type='''ALL_OF_THESE''', nothing_else=None, expected_value=['''turtle'''],
+                  before_message='''Kontrollib, kas funktsioon impordib mooduli.''',
+                  passed_message='''Funktsioon importis mooduli.''',
+                  failed_message='''Funktsioon ei importinud moodulit.''')], type='''function_imports_module_test''',
+             points=1.0, id=None, name='''Funktsioon importib mooduli turtle.''', inputs=None, passed_next=None,
+             failed_next=None, visible_to_user=None)
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=True,
              before_message='''Kontrollib, kas funktsioonis esineb try/except plokk.''',
              passed_message='''Funktsioonis ei esine try/except plokki.''',
              failed_message='''Funktsioonis esines try/except plokk.''', type='''function_contains_try_except_test''',
              points=1.0, id=None, name='''Funktsioonis ei tohi olla try/except plokki.''', inputs=None,
              passed_next=None, failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=(True, False),
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''', contains_check=False,
              before_message='''Kontrollib, kas funktsioon kasutab ainult lokaalseid muutujaid.''',
              passed_message='''Funktsioon kasutab ainult lokaalseid muutujaid.''',
-             failed_message='''Funktsioon ei kasuta ainult lokaalseid muutujaid.''',
-             type='''function_uses_only_local_vars_test''', points=1.0, id=None,
-             name='''Funktsioon kasutab ainult lokaalseid muutujaid.''', inputs=None, passed_next=None,
-             failed_next=None, visible_to_user=None)
-execute_test(file_name='''kodu1.py''', function_name='''seosta_lapsed_ja_vanemad''',
+             failed_message='''Funktsioon ei kasuta ainult lokaalseid muutujaid.''', type='''function_is_pure_test''',
+             points=1.0, id=None, name='''Funktsioon kasutab ainult lokaalseid muutujaid.''', inputs=None,
+             passed_next=None, failed_next=None, visible_to_user=None)
+execute_test(file_name='''submission.py''', function_name='''seosta_lapsed_ja_vanemad''',
              arguments=['''lapsed.txt''', '''nimed.txt'''], standard_input_data=['''Kasutajasisend'''],
-             input_files=[('''sisendfail.txt''', '''Sisendfaili sisu.''')], return_value='''{}''',
-             standard_output_checks=[StandardOutputChecks(string_check_type='''ANY_OF_THESE''', nothing_else=None,
-                                                          expected_output=['''down''', '''up'''],
-                                                          consider_elements_order=False,
-                                                          before_message='''Kontrollib, kas funktsiooni väljund sisaldab võtmesõna.''',
-                                                          passed_message='''Funktsiooni väljund sisaldab antud võtmesõna.''',
-                                                          failed_message='''Funktsiooni väljund ei sisalda antud võtmesõna.''')],
-             output_file_checks=[OutputFileChecks(file_name='''valjundfail.txt''', string_check_type='''ALL_OF_THESE''',
-                                                  nothing_else=None, expected_output=['''Väljundfaili eeldatav sisu'''],
-                                                  consider_elements_order=False,
-                                                  before_message='''Kontrollib, kas funktsiooni väljundfail sisaldab võtmesõna.''',
-                                                  passed_message='''Funktsiooni väljundfail sisaldab antud võtmesõna.''',
-                                                  failed_message='''Funktsiooni väljundfail ei sisalda antud võtmesõna.''')],
+             input_files=[('''sisendfail.txt''', '''Sisendfaili sisu.''')], return_value='''3''', generic_checks=[
+        GenericChecks(check_type='''ANY_OF_THESE''', nothing_else=None, expected_value=['''down''', '''up'''],
+                      consider_elements_order=False,
+                      before_message='''Kontrollib, kas funktsiooni väljund sisaldab võtmesõna.''',
+                      passed_message='''Funktsiooni väljund sisaldab antud võtmesõna.''',
+                      failed_message='''Funktsiooni väljund ei sisalda antud võtmesõna.''')], output_file_checks=[
+        OutputFileChecks(file_name='''valjundfail.txt''', check_type='''ALL_OF_THESE''', nothing_else=None,
+                         expected_value=['''Väljundfaili eeldatav sisu'''], consider_elements_order=True,
+                         before_message='''Kontrollib, kas funktsiooni väljundfail sisaldab võtmesõna.''',
+                         passed_message='''Funktsiooni väljundfail sisaldab antud võtmesõna.''',
+                         failed_message='''Funktsiooni väljundfail ei sisalda antud võtmesõna.''')],
              type='''function_execution_test''', points=1.0, id=None, name='''Funktsiooni käivituse test.''',
              inputs=None, passed_next=None, failed_next=None, visible_to_user=None)
 print(json.dumps(Results(None).format_result(), cls=ComplexEncoder, ensure_ascii=False))
```

### Comparing `tiivad-0.0.8/docker/kodu1.py` & `tiivad-0.0.9/docker/submission.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/__init__.py` & `tiivad-0.0.9/tiivad/__init__.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/edutest.py` & `tiivad-0.0.9/tiivad/edutest.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/file.py` & `tiivad-0.0.9/tiivad/file.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/function.py` & `tiivad-0.0.9/tiivad/function.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/function_execution.py` & `tiivad-0.0.9/tiivad/function_execution.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/functions.py` & `tiivad-0.0.9/tiivad/functions.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/functions_OLD.py` & `tiivad-0.0.9/tiivad/functions_OLD.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/help_structures.py` & `tiivad-0.0.9/tiivad/help_structures.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/prog_kontroll.py` & `tiivad-0.0.9/tiivad/prog_kontroll.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/prog_kontroll_OLD.py` & `tiivad-0.0.9/tiivad/prog_kontroll_OLD.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/progkontroll.py` & `tiivad-0.0.9/tiivad/progkontroll.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/program.py` & `tiivad-0.0.9/tiivad/program.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/program_execution.py` & `tiivad-0.0.9/tiivad/program_execution.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/results.py` & `tiivad-0.0.9/tiivad/results.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/solution.py` & `tiivad-0.0.9/tiivad/solution.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad/tests.py` & `tiivad-0.0.9/tiivad/tests.py`

 * *Files 1% similar despite different names*

```diff
@@ -257,23 +257,24 @@
             check.check_status = TestResult.FAIL.name
             kwargs["test_status"] = TestResult.FAIL.name
             kwargs["checks"] += kwargs["output_file_checks"]
             return kwargs
         else:
             check.check_status = TestResult.PASS.name
 
-    kwargs["checks"] += (kwargs["output_file_checks"])
+    kwargs["checks"] += kwargs["output_file_checks"]
 
     threw_error = pe.program_threw_error
     must_not_throw = kwargs["exception_check"]
 
+    # Default check for the case when program executed successfully
     check = Check()
-    check.before_message = kwargs["before_message"]
-    check.passed_message = kwargs["passed_message"]
-    check.failed_message = kwargs["failed_message"]
+    check.before_message = kwargs["name"]
+    check.passed_message = "Programmi käivitus õnnestus"  # TODO: Set as default
+    check.failed_message = "Programmi käivitus ebaõnnestus"  # TODO: Set as default
 
     if not must_not_throw and not threw_error or must_not_throw and threw_error:
         kwargs["test_status"] = TestResult.FAIL.name
         check.error_message = pe.program_error_message
         check.check_status = TestResult.FAIL.name
     else:
         check.check_status = TestResult.PASS.name
@@ -557,26 +558,28 @@
         return kwargs
 
     f_obj = pe.globals_dict.get(f_name, None)
     user_inputs_fun = kwargs["arguments"]
     fe = FunctionExecution(f_obj, user_inputs_fun, user_inputs_prog, kwargs["return_value"])
 
     try:
-        execution_result, nr_of_user_inputs = fe.function_execution_and_input_count()
+        fe.function_execution_and_input_count()
     except:
+        # TODO: Think about this logic here
         pass
 
     check = Check()
-    check.before_message = kwargs.get("before_message", "")
+    check.before_message = kwargs.get("before_message", kwargs.get("name", ""))
     check.passed_message = kwargs.get("passed_message", "")
     check.failed_message = kwargs.get("failed_message", "")
     test_result, error_msg = fe.function_return_value_correct()
     if test_result is False:
         kwargs["test_status"] = TestResult.FAIL.name
         check.error_message = error_msg
+        check.failed_message = error_msg if check.failed_message == "" else check.failed_message
         check.check_status = TestResult.FAIL.name
         kwargs["checks"] += [check]
         return kwargs
     else:
         check.check_status = TestResult.PASS.name
 
     kwargs["checks"] += [check]
```

### Comparing `tiivad-0.0.8/tiivad/utils.py` & `tiivad-0.0.9/tiivad/utils.py`

 * *Files identical despite different names*

### Comparing `tiivad-0.0.8/tiivad.egg-info/SOURCES.txt` & `tiivad-0.0.9/tiivad.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 LICENSE.txt
 README.md
 setup.py
 docker/assessment_code.py
-docker/kodu1.py
+docker/submission.py
 tiivad/__init__.py
 tiivad/edutest.py
 tiivad/file.py
 tiivad/function.py
 tiivad/function_execution.py
 tiivad/functions.py
 tiivad/functions_OLD.py
```

