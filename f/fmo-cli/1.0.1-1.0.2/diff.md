# Comparing `tmp/fmo-cli-1.0.1.tar.gz` & `tmp/fmo-cli-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fmo-cli-1.0.1.tar", last modified: Fri May 12 20:38:16 2023, max compression
+gzip compressed data, was "fmo-cli-1.0.2.tar", last modified: Sat May 13 02:12:05 2023, max compression
```

## Comparing `fmo-cli-1.0.1.tar` & `fmo-cli-1.0.2.tar`

### file list

```diff
@@ -1,16 +1,17 @@
-drwxr-xr-x   0 gudjon     (501) staff       (20)        0 2023-05-12 20:38:16.340014 fmo-cli-1.0.1/
--rw-r--r--   0 gudjon     (501) staff       (20)     1872 2023-05-12 20:38:16.339859 fmo-cli-1.0.1/PKG-INFO
--rw-r--r--   0 gudjon     (501) staff       (20)     1589 2023-05-12 20:35:59.000000 fmo-cli-1.0.1/README.md
-drwxr-xr-x   0 gudjon     (501) staff       (20)        0 2023-05-12 20:38:16.338426 fmo-cli-1.0.1/fmo/
--rw-r--r--   0 gudjon     (501) staff       (20)        0 2023-05-12 19:03:23.000000 fmo-cli-1.0.1/fmo/__init__.py
--rw-r--r--   0 gudjon     (501) staff       (20)     2633 2023-05-12 19:38:22.000000 fmo-cli-1.0.1/fmo/cli.py
--rw-r--r--   0 gudjon     (501) staff       (20)     1732 2023-05-12 19:05:55.000000 fmo-cli-1.0.1/fmo/fmo.py
-drwxr-xr-x   0 gudjon     (501) staff       (20)        0 2023-05-12 20:38:16.339664 fmo-cli-1.0.1/fmo_cli.egg-info/
--rw-r--r--   0 gudjon     (501) staff       (20)     1872 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/PKG-INFO
--rw-r--r--   0 gudjon     (501) staff       (20)      244 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/SOURCES.txt
--rw-r--r--   0 gudjon     (501) staff       (20)        1 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/dependency_links.txt
--rw-r--r--   0 gudjon     (501) staff       (20)       36 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/entry_points.txt
--rw-r--r--   0 gudjon     (501) staff       (20)       65 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/requires.txt
--rw-r--r--   0 gudjon     (501) staff       (20)        4 2023-05-12 20:38:16.000000 fmo-cli-1.0.1/fmo_cli.egg-info/top_level.txt
--rw-r--r--   0 gudjon     (501) staff       (20)       38 2023-05-12 20:38:16.340056 fmo-cli-1.0.1/setup.cfg
--rw-r--r--   0 gudjon     (501) staff       (20)      824 2023-05-12 20:36:19.000000 fmo-cli-1.0.1/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:12:05.426279 fmo-cli-1.0.2/
+-rw-r--r--   0 root         (0) root         (0)     1871 2023-05-13 02:12:05.426279 fmo-cli-1.0.2/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     1588 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:12:05.426279 fmo-cli-1.0.2/fmo/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/fmo/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1693 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/fmo/cli.py
+-rw-rw-rw-   0 root         (0) root         (0)     1730 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/fmo/fmo.py
+-rw-rw-rw-   0 root         (0) root         (0)     1106 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/fmo/nmea.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 02:12:05.426279 fmo-cli-1.0.2/fmo_cli.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     1871 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      256 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       36 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/entry_points.txt
+-rw-r--r--   0 root         (0) root         (0)       65 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        4 2023-05-13 02:12:05.000000 fmo-cli-1.0.2/fmo_cli.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 02:12:05.426279 fmo-cli-1.0.2/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)      880 2023-05-13 02:11:37.000000 fmo-cli-1.0.2/setup.py
```

### Comparing `fmo-cli-1.0.1/PKG-INFO` & `fmo-cli-1.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fmo-cli
-Version: 1.0.1
+Version: 1.0.2
 Summary: Command Line Interface to access and upload FindMyOyster data
 Author: Gudjon Magnusson
 Author-email: gmagnusson@fraunhofer.org
 Keywords: FindMyOyster,CLI
 Requires-Python: >=3.7, <4
 Description-Content-Type: text/markdown
 
@@ -34,15 +34,15 @@
 - Password: The password you would use in the app
 
 If authentication is successful, then a token will be saved in a `.env` file. FMO will look for the token there for all subsequent request. 
 
 If you already have a token, you are welcome to create the file by hand and skip the authentication step. The file should look like this:
 ```
 FMO_TOKEN=<my-token>
-FMO_API_URL=https://api.findmyoyster.com/dev
+FMO_API_URL=https://api.findmyoyster.com/v1
 ```
 
 ## Upload a GPS path
 
 GPS path are one of the primary types of data we deal with. Here how you might upload a path from a CSV file
 
 ```
```

### Comparing `fmo-cli-1.0.1/README.md` & `fmo-cli-1.0.2/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 - Password: The password you would use in the app
 
 If authentication is successful, then a token will be saved in a `.env` file. FMO will look for the token there for all subsequent request. 
 
 If you already have a token, you are welcome to create the file by hand and skip the authentication step. The file should look like this:
 ```
 FMO_TOKEN=<my-token>
-FMO_API_URL=https://api.findmyoyster.com/dev
+FMO_API_URL=https://api.findmyoyster.com/v1
 ```
 
 ## Upload a GPS path
 
 GPS path are one of the primary types of data we deal with. Here how you might upload a path from a CSV file
 
 ```
```

### Comparing `fmo-cli-1.0.1/fmo/cli.py` & `fmo-cli-1.0.2/fmo/cli.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,51 +1,18 @@
 
 
 import os
-from datetime import datetime
 import click
-import pandas
 from dotenv import load_dotenv
 
-from .fmo import FMO, GPSPath, login_to_get_token, FMO_API_URL
+from .nmea import parse_nmea_file
+from .fmo import FMO, login_to_get_token, FMO_API_URL
 
 load_dotenv()
 
-# Convert DMS coordinates to decimal degrees
-def nmea_latitude(dms, direction):
-    decimal = float(dms[:2]) + float(dms[2:])/60
-    if direction == 'S':
-        decimal = -decimal
-    return decimal
-
-def nmea_longitude(dms, direction):
-    decimal = float(dms[:3]) + float(dms[3:])/60
-    if direction == 'W':
-        decimal = -decimal
-    return decimal
-
-def parse_nmea_file(file) -> GPSPath:
-    # https://www.gpsworld.com/what-exactly-is-gps-nmea-data/
-
-    if not file.endswith(".csv"):
-        raise Exception("Not a CSV file")
-    
-    # Read the CSV file into a list of dictionaries
-    df = pandas.read_csv(file, dtype = str)
-
-    # Parse the latitude and longitude fields and convert them to decimal degrees
-    values = []
-    for _, row in df.iterrows():
-        lat = nmea_latitude(row[2], row[3])
-        lng = nmea_longitude(row[4], row[5])
-        timestamp = datetime.combine(datetime.today(), datetime.strptime(row[1], '%H%M%S.%f').time())
-        values.append((timestamp, lat, lng))
-
-    return GPSPath(values)
-
 
 @click.group()
 def cli():
     pass
 
 @cli.command()
 @click.argument('file')
@@ -60,15 +27,19 @@
 
 @cli.command()
 @click.option("--url", prompt=True, default=FMO_API_URL)
 @click.option("--farm", prompt=True, default="demo")
 @click.option("--user", prompt=True)
 @click.option("--password", prompt=True, hide_input=True)
 def authenticate(url, farm, user, password):
-    token = login_to_get_token(farm, user, password)
+    try:
+        token = login_to_get_token(url, farm, user, password)
+    except Exception as ex:
+        click.echo(f"Authentication failed: {ex}")
+        return
 
     # Write the token to the .env file
     with open(".env", "w") as f:
         f.write(f"FMO_TOKEN={token}\n")
         f.write(f"FMO_API_URL={url}\n")
 
     click.echo("Authentication successful. Token written to .env file.")
```

### Comparing `fmo-cli-1.0.1/fmo/fmo.py` & `fmo-cli-1.0.2/fmo/fmo.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import requests
 import pandas
 import datetime
 
-FMO_API_URL = "https://api.findmyoyster.com/dev"
+FMO_API_URL = "https://api.findmyoyster.com/v1"
 
 
 def any_to_unix_time(any):
     if isinstance(any, datetime.datetime):
         return int(datetime.datetime.timestamp(any))
 
     if isinstance(any, str):
@@ -47,15 +47,15 @@
         }
 
     def dataframe(self):
         return pandas.DataFrame(self._coords, columns=["Time", "Latitude", "Longitude"])
 
 
 class FMO:
-    def __init__(self, token, url="api.findmyoyster.com/dev"):
+    def __init__(self, token, url="api.findmyoyster.com/v1"):
         self._url = url
         self._token = token
 
     def upload_path(self, path: GPSPath):
         response = requests.post(
             f"{self._url}/paths",
             json=path.fmo_path_json(),
```

### Comparing `fmo-cli-1.0.1/fmo_cli.egg-info/PKG-INFO` & `fmo-cli-1.0.2/fmo_cli.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fmo-cli
-Version: 1.0.1
+Version: 1.0.2
 Summary: Command Line Interface to access and upload FindMyOyster data
 Author: Gudjon Magnusson
 Author-email: gmagnusson@fraunhofer.org
 Keywords: FindMyOyster,CLI
 Requires-Python: >=3.7, <4
 Description-Content-Type: text/markdown
 
@@ -34,15 +34,15 @@
 - Password: The password you would use in the app
 
 If authentication is successful, then a token will be saved in a `.env` file. FMO will look for the token there for all subsequent request. 
 
 If you already have a token, you are welcome to create the file by hand and skip the authentication step. The file should look like this:
 ```
 FMO_TOKEN=<my-token>
-FMO_API_URL=https://api.findmyoyster.com/dev
+FMO_API_URL=https://api.findmyoyster.com/v1
 ```
 
 ## Upload a GPS path
 
 GPS path are one of the primary types of data we deal with. Here how you might upload a path from a CSV file
 
 ```
```

### Comparing `fmo-cli-1.0.1/setup.py` & `fmo-cli-1.0.2/setup.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,18 +1,20 @@
+import os
 from setuptools import setup
 
 # read the contents of your README file
 from pathlib import Path
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
+VERSION = os.getenv("CI_COMMIT_TAG", "0.0.0")
 
 setup(
     name="fmo-cli",
-    version="1.0.1",
+    version=VERSION,
     author="Gudjon Magnusson",
     author_email="gmagnusson@fraunhofer.org",
     description="Command Line Interface to access and upload FindMyOyster data",
     long_description=long_description,
     long_description_content_type='text/markdown',
     packages=["fmo"],
     keywords=["FindMyOyster", "CLI"],
```

