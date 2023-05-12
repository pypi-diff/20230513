# Comparing `tmp/cocoder-0.1.0.tar.gz` & `tmp/cocoder-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cocoder-0.1.0.tar", last modified: Fri May 12 20:29:09 2023, max compression
+gzip compressed data, was "cocoder-0.1.1.tar", last modified: Fri May 12 22:41:10 2023, max compression
```

## Comparing `cocoder-0.1.0.tar` & `cocoder-0.1.1.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.105039 cocoder-0.1.0/
--rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.0/LICENSE
--rw-rw-rw-   0        0        0     1018 2023-05-12 20:29:09.103862 cocoder-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.050907 cocoder-0.1.0/cocoder/
--rw-rw-rw-   0        0        0      508 2023-05-12 20:19:27.000000 cocoder-0.1.0/cocoder/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.080667 cocoder-0.1.0/cocoder/chatbase/
--rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.0/cocoder/chatbase/__init__.py
--rw-rw-rw-   0        0        0     1855 2023-05-12 20:27:36.000000 cocoder-0.1.0/cocoder/chatbase/bard_receiver.py
--rw-rw-rw-   0        0        0     2439 2023-05-12 20:27:44.000000 cocoder-0.1.0/cocoder/chatbase/openai_receiver.py
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.086153 cocoder-0.1.0/cocoder/ipy/
--rw-rw-rw-   0        0        0      508 2023-05-12 20:28:49.000000 cocoder-0.1.0/cocoder/ipy/__init__.py
--rw-rw-rw-   0        0        0     1820 2023-05-12 19:52:24.000000 cocoder-0.1.0/cocoder/ipy/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.101867 cocoder-0.1.0/cocoder/py/
--rw-rw-rw-   0        0        0      486 2023-05-12 20:19:20.000000 cocoder-0.1.0/cocoder/py/__init__.py
--rw-rw-rw-   0        0        0     3657 2023-05-12 19:58:37.000000 cocoder-0.1.0/cocoder/py/core.py
-drwxrwxrwx   0        0        0        0 2023-05-12 20:29:09.072471 cocoder-0.1.0/cocoder.egg-info/
--rw-rw-rw-   0        0        0     1018 2023-05-12 20:29:08.000000 cocoder-0.1.0/cocoder.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      419 2023-05-12 20:29:09.000000 cocoder-0.1.0/cocoder.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 20:29:08.000000 cocoder-0.1.0/cocoder.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2023-05-12 20:29:08.000000 cocoder-0.1.0/cocoder.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       15 2023-05-12 20:29:09.000000 cocoder-0.1.0/cocoder.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-05-12 20:29:09.000000 cocoder-0.1.0/cocoder.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-12 20:29:09.105039 cocoder-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0     1775 2023-05-12 20:28:32.000000 cocoder-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.258509 cocoder-0.1.1/
+-rw-rw-rw-   0        0        0     1089 2023-05-12 15:23:47.000000 cocoder-0.1.1/LICENSE
+-rw-rw-rw-   0        0        0     1018 2023-05-12 22:41:10.257510 cocoder-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0      121 2023-05-12 15:23:47.000000 cocoder-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.205744 cocoder-0.1.1/cocoder/
+-rw-rw-rw-   0        0        0      504 2023-05-12 22:40:21.000000 cocoder-0.1.1/cocoder/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.232977 cocoder-0.1.1/cocoder/chatbase/
+-rw-rw-rw-   0        0        0        0 2023-05-12 20:28:43.000000 cocoder-0.1.1/cocoder/chatbase/__init__.py
+-rw-rw-rw-   0        0        0     2146 2023-05-12 22:39:53.000000 cocoder-0.1.1/cocoder/chatbase/bard_receiver.py
+-rw-rw-rw-   0        0        0     2439 2023-05-12 22:39:58.000000 cocoder-0.1.1/cocoder/chatbase/openai_receiver.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.242998 cocoder-0.1.1/cocoder/ipython/
+-rw-rw-rw-   0        0        0      554 2023-05-12 22:40:24.000000 cocoder-0.1.1/cocoder/ipython/__init__.py
+-rw-rw-rw-   0        0        0     1881 2023-05-12 21:26:00.000000 cocoder-0.1.1/cocoder/ipython/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.254502 cocoder-0.1.1/cocoder/python/
+-rw-rw-rw-   0        0        0      544 2023-05-12 22:40:26.000000 cocoder-0.1.1/cocoder/python/__init__.py
+-rw-rw-rw-   0        0        0     3047 2023-05-12 22:39:18.000000 cocoder-0.1.1/cocoder/python/core.py
+drwxrwxrwx   0        0        0        0 2023-05-12 22:41:10.227163 cocoder-0.1.1/cocoder.egg-info/
+-rw-rw-rw-   0        0        0     1018 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      435 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       15 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-12 22:41:10.000000 cocoder-0.1.1/cocoder.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-12 22:41:10.258509 cocoder-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0     1775 2023-05-12 22:40:18.000000 cocoder-0.1.1/setup.py
```

### Comparing `cocoder-0.1.0/LICENSE` & `cocoder-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.0/PKG-INFO` & `cocoder-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.0
+Version: 0.1.1
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.0/cocoder/chatbase/bard_receiver.py` & `cocoder-0.1.1/cocoder/chatbase/bard_receiver.py`

 * *Files 21% similar despite different names*

```diff
@@ -10,29 +10,27 @@
     :type _OPEN_AI_API: str
     :param error_message: Error message
     :type error_message: str
     :return: Returns a description and example of the code, the location of the error, and a debugging code example.
     :rtype: str
     """
     environ["_BARD_API_KEY"] = _BARD_API_KEY
+
     if environ.get("_PROMPT_COMMAND") is None:
-        if environ["_BARD_ADVICE_LANG"]=='ko':
-            input_text = f"이 오류를 어떻게 수정할 수 있나요? 디버깅을 위한 코드 예시와 이 문제와 관련된 Stack Overflow 링크를 제공해 주세요. error=={error_message}"
-        elif environ["_BARD_ADVICE_LANG"]=='jp':
-            input_text = f"このエラーを修正するにはどうすればよいですか？デバッグのためのコード例を提供し、この問題に関連するStack Overflowリンクを教えてください。 error=={error_message}"
+        if environ.get("_BARD_ADVICE_LANG") is None:
+            input_text = f"Give me more explanation for the following error. And if you have a code example and a way to solve it, please suggest it. Please provide as much information as possible. error is {error_message}."
         else:
-            input_text = f"How can I fix this error? Please provide a code example for debugging, and Stack Overflow links related to this issue. error=={error_message}"
+            if environ["_BARD_ADVICE_LANG"]=='ko':
+                input_text = f"다음 에러와 관련된 더 많은 설명을 알려줘. 그리고 만약 이 오류와 관련된 코드 예제 및 유용한 자료가 있다면 가능한 많이 알려줘. 오류는 {error_message} 입니다."
+            elif environ["_BARD_ADVICE_LANG"]=='jp':
+                input_text = f"次のエラーに関連するできるだけ多くの情報を教えてください。エラーを解決するサンプルコードや情報があればそれも教えてください。 エラーは {error_message} です。"
+            else:
+                print('You can only use ko or jp for the _BARD_ADVICE_LANG variable. Hence, answers will be provided in English.')
+                input_text = f"Give me more explanation for the following error. And if you have a code example and a way to solve it, please suggest it. Please provide as much information as possible. error is {error_message}."
     else:
         input_text = f"{environ['_PROMPT_COMMAND']} error=={error_message}" 
 
     response = bardapi.core.Bard().get_answer(input_text)
-    advice_msg = response["content"]
+    advice_msg = response['content']
 
     return advice_msg
 
-
-# if __name__ == "__main__":
-#     _BARD_API_KEY = "xxxxxxxxxxxxxx."
-#     error_message = " Cell 3 in ()----> 1 1/0 ZeroDivisionError: division by zero"
-#     advice_msg = receive_bard_advice(_BARD_API_KEY, error_message)
-
-#     print(advice_msg)
```

### Comparing `cocoder-0.1.0/cocoder/chatbase/openai_receiver.py` & `cocoder-0.1.1/cocoder/chatbase/openai_receiver.py`

 * *Files identical despite different names*

### Comparing `cocoder-0.1.0/cocoder/ipy/core.py` & `cocoder-0.1.1/cocoder/ipython/core.py`

 * *Files 10% similar despite different names*

```diff
@@ -22,29 +22,29 @@
     :type tb_offset: int, optional
     """
     itb = AutoFormattedTB(mode="Plain", tb_offset=1)
     shell.showtraceback((etype, evalue, tb), tb_offset=tb_offset)
     stb = itb.structured_traceback(etype, evalue, tb)
     sstb = itb.stb2text(stb)
 
-    error_message = f"error sheel=={shell}, error_type_document=={etype.__doc__}, error_value=={evalue}, error message in ipython cell=={sstb}"
-    
+    error_message = f"error_type_document=={etype.__doc__}, error_value=={evalue}, error message in ipython cell=={sstb}"
     if environ.get("_BARD_API_KEY") is not None:
         try:
             advice_msg = receive_bard_advice(environ["_BARD_API_KEY"], error_message)
             print(advice_msg)
         except Exception as e:
+            print(f'Cocoder not worked: {e}')
             pass
 
     elif environ.get("_OPEN_AI_API") is not None:
         try:
             advice_msg = receive_openai_advice(
                 environ["_OPEN_AI_MODEL"], environ["_OPEN_AI_API"], error_message
             )
             print(advice_msg)
-            
         except Exception as e:
+            print(f'Cocoder not worked: {e}')
             pass
 
     else:
-        print("There is no system variable for AI inference.")
+        print("There is no system variable available for AI inference")
```

### Comparing `cocoder-0.1.0/cocoder/py/core.py` & `cocoder-0.1.1/cocoder/python/core.py`

 * *Files 26% similar despite different names*

```diff
@@ -57,38 +57,28 @@
                 try:
                     cocoder["traced_error"] += str(val)
                 except:
                     cocoder["traced_error"] += "<traced_error WHILE PRINTING VALUE>"
 
         if environ.get("_OPEN_AI_API") is not None:
             try:
-                traced_error_message = f"traced_error_type=={excType} traced_error_type_document=={etype.__doc__} traced_error_value=={value} stack infomation=={stack} code name=={frame.f_code.co_name}file name=={frame.f_code.co_filename} file_number=={frame.f_lineno}"
-                advice_msg = '\tFile: "%s"\n\t\t%s %s: %s\n' % (
-                    line[0],
-                    line[2],
-                    line[1],
-                    line[3],
-                )
-                advice_msg += receive_openai_advice(
+                traced_error_message = f"traced_error_type=={excType} traced_error_type_document=={etype.__doc__} traced_error_value=={value} stack infomation=={stack}"
+
+                advice_msg = receive_openai_advice(
                     environ["_OPEN_AI_MODEL"], environ["_OPEN_AI_API"], traced_error_message
                 )  
                 print(advice_msg)
             except Exception as e:
                 print(f'Cocoder not worked: {e}')
                 pass
 
         if environ.get("_BARD_API_KEY") is not None:
             try:
-                traced_error_message = f"traced_error_type=={excType} traced_error_type_document=={etype.__doc__} traced_error_value=={value} stack infomation=={stack} code name=={frame.f_code.co_name}file name=={frame.f_code.co_filename} file_number=={frame.f_lineno}"
-                advice_msg = '\tFile: "%s"\n\t\t%s %s: %s\n' % (
-                    line[0],
-                    line[2],
-                    line[1],
-                    line[3],
-                )
-                advice_msg += receive_bard_advice(
+                traced_error_message = f"traced_error_type=={excType} traced_error_type_document=={etype.__doc__} traced_error_value=={value} stack infomation=={stack}"
+
+                advice_msg = receive_bard_advice(
                     environ["_BARD_API_KEY"], traced_error_message
                 )  
                 print(advice_msg)
             except Exception as e:
                 print(f'Cocoder not worked: {e}')
                 pass
```

### Comparing `cocoder-0.1.0/cocoder.egg-info/PKG-INFO` & `cocoder-0.1.1/cocoder.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cocoder
-Version: 0.1.0
+Version: 0.1.1
 Home-page: https://github.com/dsdanielpark/Co-Coder
 Author: daniel park
 Author-email: parkminwoo1991@gmail.com
 Keywords: Python Debuger,Python AI Debug,Realtime Debuger,Search,Find Debug Infomation,Bard,ChatGPT,GoogleBard,OpenAIchatGPT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Science/Research
 Classifier: Natural Language :: English
```

### Comparing `cocoder-0.1.0/setup.py` & `cocoder-0.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
 
 version = get_version()
 
 
 setup(
     name="cocoder",
-    version="0.1.0",
+    version="0.1.1",
     author="daniel park",
     author_email="parkminwoo1991@gmail.com",
     description="",
     long_description=get_long_description(),
     long_description_content_type="text/markdown",
     url="https://github.com/dsdanielpark/Co-Coder",
     packages=find_packages(exclude=[]),
```

