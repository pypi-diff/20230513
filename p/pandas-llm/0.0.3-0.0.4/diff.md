# Comparing `tmp/pandas_llm-0.0.3.tar.gz` & `tmp/pandas_llm-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pandas_llm-0.0.3.tar", last modified: Fri May 12 08:48:26 2023, max compression
+gzip compressed data, was "pandas_llm-0.0.4.tar", last modified: Sat May 13 14:56:54 2023, max compression
```

## Comparing `pandas_llm-0.0.3.tar` & `pandas_llm-0.0.4.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-12 08:48:26.398585 pandas_llm-0.0.3/
--rw-r--r--   0 alessioricco   (501) staff       (20)     1068 2023-05-11 12:07:22.000000 pandas_llm-0.0.3/LICENSE
--rw-r--r--   0 alessioricco   (501) staff       (20)     2552 2023-05-12 08:48:26.398689 pandas_llm-0.0.3/PKG-INFO
--rw-r--r--   0 alessioricco   (501) staff       (20)     1735 2023-05-12 08:44:14.000000 pandas_llm-0.0.3/README.md
-drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-12 08:48:26.397087 pandas_llm-0.0.3/pandas_llm/
--rw-r--r--   0 alessioricco   (501) staff       (20)       32 2023-05-11 15:03:14.000000 pandas_llm-0.0.3/pandas_llm/__init__.py
--rw-r--r--   0 alessioricco   (501) staff       (20)     2511 2023-05-11 15:38:43.000000 pandas_llm-0.0.3/pandas_llm/example-chatbot.py
--rw-r--r--   0 alessioricco   (501) staff       (20)      902 2023-05-11 16:51:08.000000 pandas_llm-0.0.3/pandas_llm/example.py
--rw-r--r--   0 alessioricco   (501) staff       (20)     7081 2023-05-11 21:57:26.000000 pandas_llm-0.0.3/pandas_llm/pandas_llm.py
--rw-r--r--   0 alessioricco   (501) staff       (20)     1967 2023-05-11 12:28:50.000000 pandas_llm-0.0.3/pandas_llm/sandbox.py
-drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-12 08:48:26.398443 pandas_llm-0.0.3/pandas_llm.egg-info/
--rw-r--r--   0 alessioricco   (501) staff       (20)     2552 2023-05-12 08:48:26.000000 pandas_llm-0.0.3/pandas_llm.egg-info/PKG-INFO
--rw-r--r--   0 alessioricco   (501) staff       (20)      327 2023-05-12 08:48:26.000000 pandas_llm-0.0.3/pandas_llm.egg-info/SOURCES.txt
--rw-r--r--   0 alessioricco   (501) staff       (20)        1 2023-05-12 08:48:26.000000 pandas_llm-0.0.3/pandas_llm.egg-info/dependency_links.txt
--rw-r--r--   0 alessioricco   (501) staff       (20)      187 2023-05-12 08:48:26.000000 pandas_llm-0.0.3/pandas_llm.egg-info/requires.txt
--rw-r--r--   0 alessioricco   (501) staff       (20)       11 2023-05-12 08:48:26.000000 pandas_llm-0.0.3/pandas_llm.egg-info/top_level.txt
--rw-r--r--   0 alessioricco   (501) staff       (20)       79 2023-05-12 08:48:26.399041 pandas_llm-0.0.3/setup.cfg
--rw-r--r--   0 alessioricco   (501) staff       (20)     2035 2023-05-12 08:46:42.000000 pandas_llm-0.0.3/setup.py
+drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-13 14:56:54.140380 pandas_llm-0.0.4/
+-rw-r--r--   0 alessioricco   (501) staff       (20)     1068 2023-05-11 12:07:22.000000 pandas_llm-0.0.4/LICENSE
+-rw-r--r--   0 alessioricco   (501) staff       (20)     2542 2023-05-13 14:56:54.140472 pandas_llm-0.0.4/PKG-INFO
+-rw-r--r--   0 alessioricco   (501) staff       (20)     1725 2023-05-13 14:31:01.000000 pandas_llm-0.0.4/README.md
+drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-13 14:56:54.139183 pandas_llm-0.0.4/pandas_llm/
+-rw-r--r--   0 alessioricco   (501) staff       (20)       32 2023-05-11 15:03:14.000000 pandas_llm-0.0.4/pandas_llm/__init__.py
+-rw-r--r--   0 alessioricco   (501) staff       (20)     2600 2023-05-13 14:31:01.000000 pandas_llm-0.0.4/pandas_llm/example-chatbot.py
+-rw-r--r--   0 alessioricco   (501) staff       (20)      888 2023-05-13 14:31:01.000000 pandas_llm-0.0.4/pandas_llm/example.py
+-rw-r--r--   0 alessioricco   (501) staff       (20)    11178 2023-05-13 14:31:01.000000 pandas_llm-0.0.4/pandas_llm/pandas_llm.py
+-rw-r--r--   0 alessioricco   (501) staff       (20)     1967 2023-05-11 12:28:50.000000 pandas_llm-0.0.4/pandas_llm/sandbox.py
+drwxr-xr-x   0 alessioricco   (501) staff       (20)        0 2023-05-13 14:56:54.140238 pandas_llm-0.0.4/pandas_llm.egg-info/
+-rw-r--r--   0 alessioricco   (501) staff       (20)     2542 2023-05-13 14:56:54.000000 pandas_llm-0.0.4/pandas_llm.egg-info/PKG-INFO
+-rw-r--r--   0 alessioricco   (501) staff       (20)      327 2023-05-13 14:56:54.000000 pandas_llm-0.0.4/pandas_llm.egg-info/SOURCES.txt
+-rw-r--r--   0 alessioricco   (501) staff       (20)        1 2023-05-13 14:56:54.000000 pandas_llm-0.0.4/pandas_llm.egg-info/dependency_links.txt
+-rw-r--r--   0 alessioricco   (501) staff       (20)      187 2023-05-13 14:56:54.000000 pandas_llm-0.0.4/pandas_llm.egg-info/requires.txt
+-rw-r--r--   0 alessioricco   (501) staff       (20)       11 2023-05-13 14:56:54.000000 pandas_llm-0.0.4/pandas_llm.egg-info/top_level.txt
+-rw-r--r--   0 alessioricco   (501) staff       (20)       79 2023-05-13 14:56:54.140800 pandas_llm-0.0.4/setup.cfg
+-rw-r--r--   0 alessioricco   (501) staff       (20)     2035 2023-05-13 14:31:01.000000 pandas_llm-0.0.4/setup.py
```

### Comparing `pandas_llm-0.0.3/LICENSE` & `pandas_llm-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pandas_llm-0.0.3/PKG-INFO` & `pandas_llm-0.0.4/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pandas_llm
-Version: 0.0.3
+Version: 0.0.4
 Summary: Conversational Pandas Dataframes
 Home-page: https://github.com/DashyDashOrg/pandas-llm
-Download-URL: https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.3
+Download-URL: https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.4
 Author: DashyDash
 Author-email: alessio@dashydash.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/DashyDashOrg/pandas-llm/issues
 Keywords: pypi,pandas-llm,pandas,llm,ai,openai,chatgpt
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -40,17 +40,14 @@
 Here's a quick example of how to use pandas-llm:
 
 ```python
 import os
 import pandas as pd
 from pandas_llm import PandasLLM
 
-# your key
-OPENAI_API_KEY = os.environ.get("OPENAI_API_KEY")
-
 # Data
 # Please note that these names, ages, and donations are randomly generated 
 # and do not correspond to real individuals or their donations.
 data = [('John Doe', 25, 50), 
         ('Jane Smith', 38, 70),
         ('Alex Johnson', 45, 80),
         ('Jessica Brown', 60, 40),
@@ -58,18 +55,20 @@
         ('Emily Wilson', 30, 60),
         ('Daniel Taylor', 35, 75),
         ('Sophia Moore', 40, 85),
         ('David Thomas', 50, 65),
         ('Olivia Jackson', 29, 55)]
 df = pd.DataFrame(data, columns=['name', 'age', 'donation'])
 
-conv_df = PandasLLM(data=df, config={ "openai_api_key":OPENAI_API_KEY})
+conv_df = PandasLLM(data=df, openai_api_key = os.environ.get("OPENAI_API_KEY"))
 result = conv_df.prompt("What is the average donation of people older than 30 who donated more than $50?")
 
 print(f"Result ({type(result)}):\n {result}")
+# Result (<class 'numpy.float64'>):
+#  75.0
 ```
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate.
 
 ## License
 MIT
```

### Comparing `pandas_llm-0.0.3/README.md` & `pandas_llm-0.0.4/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -19,17 +19,14 @@
 Here's a quick example of how to use pandas-llm:
 
 ```python
 import os
 import pandas as pd
 from pandas_llm import PandasLLM
 
-# your key
-OPENAI_API_KEY = os.environ.get("OPENAI_API_KEY")
-
 # Data
 # Please note that these names, ages, and donations are randomly generated 
 # and do not correspond to real individuals or their donations.
 data = [('John Doe', 25, 50), 
         ('Jane Smith', 38, 70),
         ('Alex Johnson', 45, 80),
         ('Jessica Brown', 60, 40),
@@ -37,18 +34,20 @@
         ('Emily Wilson', 30, 60),
         ('Daniel Taylor', 35, 75),
         ('Sophia Moore', 40, 85),
         ('David Thomas', 50, 65),
         ('Olivia Jackson', 29, 55)]
 df = pd.DataFrame(data, columns=['name', 'age', 'donation'])
 
-conv_df = PandasLLM(data=df, config={ "openai_api_key":OPENAI_API_KEY})
+conv_df = PandasLLM(data=df, openai_api_key = os.environ.get("OPENAI_API_KEY"))
 result = conv_df.prompt("What is the average donation of people older than 30 who donated more than $50?")
 
 print(f"Result ({type(result)}):\n {result}")
+# Result (<class 'numpy.float64'>):
+#  75.0
 ```
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate.
 
 ## License
 MIT
```

### Comparing `pandas_llm-0.0.3/pandas_llm/example-chatbot.py` & `pandas_llm-0.0.4/pandas_llm/example-chatbot.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 import sys
 from pathlib import Path
 sys.path.append(str(Path(__file__).resolve().parent.parent))
 
 from pandas_llm import PandasLLM
 
 # Data
+#  Please note that these names, ages, and donations are randomly generated and do not correspond to real individuals or their donations.
 data = [('John Doe', 25, 50), 
         ('Jane Smith', 38, 70),
         ('Alex Johnson', 45, 80),
         ('Jessica Brown', 60, 40),
         ('Michael Davis', 22, 90),
         ('Emily Wilson', 30, 60),
         ('Daniel Taylor', 35, 75),
@@ -50,27 +51,23 @@
 
     # Set the OpenAI API key
     openai_key = os.environ.get("OPENAI_API_KEY")
     if openai_key is None:
         print("No OpenAI API key provided. Exiting.")
         return
 
-    config = {
-        "openai_api_key":openai_key
-    }
-
-    conv_df = PandasLLM(data=df, config=config)
+    conv_df = PandasLLM(data=df, llm_api_key = openai_key)
     print()
     banner = """
     Welcome to the Donation Data CLI.
     The donation dataset has three columns (name, age, donation)
     Please note that these names, ages, and donations are randomly generated and do not correspond to real individuals or their donations.
     
     You can ask questions like:
-    - show me the name of donators
+    - show me the name of donors
     - What is the average age of people who donated?
     - What is the average donation amount?
     - What is the average donation of people older than 30?
     - What is the average donation of people older than 30 who donated more than $50?
     """
     print(banner)
```

### Comparing `pandas_llm-0.0.3/pandas_llm/example.py` & `pandas_llm-0.0.4/pandas_llm/example.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,14 +1,11 @@
 import os
 import pandas as pd
 from pandas_llm import PandasLLM
 
-# your key
-OPENAI_API_KEY = os.environ.get("OPENAI_API_KEY")
-
 # Data
 # Please note that these names, ages, and donations are randomly generated 
 # and do not correspond to real individuals or their donations.
 data = [('John Doe', 25, 50), 
         ('Jane Smith', 38, 70),
         ('Alex Johnson', 45, 80),
         ('Jessica Brown', 60, 40),
@@ -16,12 +13,13 @@
         ('Emily Wilson', 30, 60),
         ('Daniel Taylor', 35, 75),
         ('Sophia Moore', 40, 85),
         ('David Thomas', 50, 65),
         ('Olivia Jackson', 29, 55)]
 df = pd.DataFrame(data, columns=['name', 'age', 'donation'])
 
-conv_df = PandasLLM(data=df, config={ "openai_api_key":OPENAI_API_KEY})
+conv_df = PandasLLM(data=df, llm_api_key = os.environ.get("OPENAI_API_KEY"))
 result = conv_df.prompt("What is the average donation of people older than 30 who donated more than $50?")
 
 print(f"Result ({type(result)}):\n {result}")
-
+# Result (<class 'numpy.float64'>):
+#  75.0
```

### Comparing `pandas_llm-0.0.3/pandas_llm/sandbox.py` & `pandas_llm-0.0.4/pandas_llm/sandbox.py`

 * *Files identical despite different names*

### Comparing `pandas_llm-0.0.3/pandas_llm.egg-info/PKG-INFO` & `pandas_llm-0.0.4/pandas_llm.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pandas-llm
-Version: 0.0.3
+Version: 0.0.4
 Summary: Conversational Pandas Dataframes
 Home-page: https://github.com/DashyDashOrg/pandas-llm
-Download-URL: https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.3
+Download-URL: https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.4
 Author: DashyDash
 Author-email: alessio@dashydash.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/DashyDashOrg/pandas-llm/issues
 Keywords: pypi,pandas-llm,pandas,llm,ai,openai,chatgpt
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -40,17 +40,14 @@
 Here's a quick example of how to use pandas-llm:
 
 ```python
 import os
 import pandas as pd
 from pandas_llm import PandasLLM
 
-# your key
-OPENAI_API_KEY = os.environ.get("OPENAI_API_KEY")
-
 # Data
 # Please note that these names, ages, and donations are randomly generated 
 # and do not correspond to real individuals or their donations.
 data = [('John Doe', 25, 50), 
         ('Jane Smith', 38, 70),
         ('Alex Johnson', 45, 80),
         ('Jessica Brown', 60, 40),
@@ -58,18 +55,20 @@
         ('Emily Wilson', 30, 60),
         ('Daniel Taylor', 35, 75),
         ('Sophia Moore', 40, 85),
         ('David Thomas', 50, 65),
         ('Olivia Jackson', 29, 55)]
 df = pd.DataFrame(data, columns=['name', 'age', 'donation'])
 
-conv_df = PandasLLM(data=df, config={ "openai_api_key":OPENAI_API_KEY})
+conv_df = PandasLLM(data=df, openai_api_key = os.environ.get("OPENAI_API_KEY"))
 result = conv_df.prompt("What is the average donation of people older than 30 who donated more than $50?")
 
 print(f"Result ({type(result)}):\n {result}")
+# Result (<class 'numpy.float64'>):
+#  75.0
 ```
 
 ## Contributing
 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate.
 
 ## License
 MIT
```

### Comparing `pandas_llm-0.0.3/setup.py` & `pandas_llm-0.0.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 # Reads the content of your README.md into a variable to be used in the setup below
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setup(
     name='pandas_llm',                           # should match the package folder
-    version='0.0.3',                                # important for updates
+    version='0.0.4',                                # important for updates
     license='MIT',                                  # should match your chosen license
     description='Conversational Pandas Dataframes',
     long_description=long_description,              # loads your README.md
     long_description_content_type="text/markdown",  # README.md is of type 'markdown'
     author='DashyDash',
     author_email='alessio@dashydash.com',
     url='https://github.com/DashyDashOrg/pandas-llm', 
@@ -47,9 +47,9 @@
         "RestrictedPython",
         "six",
         "tqdm",
         "tzdata",
         "urllib3",
         "yarl",
     ],   
-    download_url="https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.3",
+    download_url="https://github.com/DashyDashOrg/pandas-llm/releases/tag/v0.0.4",
 )
```

