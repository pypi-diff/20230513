# Comparing `tmp/atuin_graph-1.0.2.tar.gz` & `tmp/atuin_graph-1.1.0.tar.gz`

## Comparing `atuin_graph-1.0.2.tar` & `atuin_graph-1.1.0.tar`

### file list

```diff
@@ -1,14 +1,13 @@
--rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/.python-version
--rw-r--r--   0        0        0     2242 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/requirements.txt
--rw-r--r--   0        0        0      682 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/.github/workflows/release.yaml
--rw-r--r--   0        0        0      328 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/.github/workflows/ruff.yaml
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/atuin_graph/__init__.py
--rw-r--r--   0        0        0     1025 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/atuin_graph/cli.py
--rwxr-xr-x   0        0        0     2740 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/atuin_graph/generate_calendar.py
--rw-r--r--   0        0        0      792 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/atuin_graph/web.py
--rw-r--r--   0        0        0  2038139 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/img/shell.history.gif
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/.gitignore
--rw-r--r--   0        0        0     1069 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/LICENSE
--rw-r--r--   0        0        0     1437 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/README.md
--rw-r--r--   0        0        0     1158 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/pyproject.toml
--rw-r--r--   0        0        0     2626 2020-02-02 00:00:00.000000 atuin_graph-1.0.2/PKG-INFO
+-rw-r--r--   0        0        0        7 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/.python-version
+-rw-r--r--   0        0        0      682 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/.github/workflows/release.yaml
+-rw-r--r--   0        0        0      328 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/.github/workflows/ruff.yaml
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/atuin_graph/__init__.py
+-rw-r--r--   0        0        0     1155 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/atuin_graph/cli.py
+-rw-r--r--   0        0        0     2866 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/atuin_graph/generate_calendar.py
+-rw-r--r--   0        0        0      939 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/atuin_graph/web.py
+-rw-r--r--   0        0        0  2038139 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/img/shell.history.gif
+-rw-r--r--   0        0        0       88 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/.gitignore
+-rw-r--r--   0        0        0     1069 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/LICENSE
+-rw-r--r--   0        0        0     1711 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/README.md
+-rw-r--r--   0        0        0     1158 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/pyproject.toml
+-rw-r--r--   0        0        0     2900 2020-02-02 00:00:00.000000 atuin_graph-1.1.0/PKG-INFO
```

### Comparing `atuin_graph-1.0.2/.github/workflows/release.yaml` & `atuin_graph-1.1.0/.github/workflows/release.yaml`

 * *Files identical despite different names*

### Comparing `atuin_graph-1.0.2/atuin_graph/cli.py` & `atuin_graph-1.1.0/atuin_graph/cli.py`

 * *Files 21% similar despite different names*

```diff
@@ -7,29 +7,36 @@
 from atuin_graph.generate_calendar import generate_calendar
 
 
 def main():
     parser = argparse.ArgumentParser()
     parser.add_argument("--user", help="user to draw the graph for", required=True)
     parser.add_argument(
+        "--from",
+        dest="from_",
+        metavar="FROM",
+        help="day (yyyy-mm-dd) to query from",
+    )
+    parser.add_argument(
         "--until",
-        help="day (yyyy-mm-dd) to query until, used for gif generation",
+        help="day (yyyy-mm-dd) to query until",
     )
     parser.add_argument("--atuin_server_config", help="atuin server config path")
     args = parser.parse_args()
 
     if args.atuin_server_config:
         config = args.atuin_server_config
     else:
         config = os.environ["HOME"] + "/.config/atuin/server.toml"
 
-    generate_calendar(config, args.user, args.until)
+    generate_calendar(config, args.user, args.from_, args.until)
 
     if args.until:
         plt.savefig(f"atuin-{args.user}-{args.until}.png", bbox_inches="tight")
     else:
         plt.savefig(f"atuin-{args.user}.png", bbox_inches="tight")
+
     plt.close()
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `atuin_graph-1.0.2/atuin_graph/generate_calendar.py` & `atuin_graph-1.1.0/atuin_graph/generate_calendar.py`

 * *Files 4% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import matplotlib.pyplot as plt
 import calplot
 import numpy as np
 import pandas as pd
 from sqlalchemy import create_engine
 
 
-def generate_calendar(config, user, until):
+def generate_calendar(config, user, from_, until):
     """get the data from pg and generate the calendar"""
     with open(config, "rb") as f:
         serverconf = tomllib.load(f)
 
     # for it to work db_uri in server.toml has to start with postgresql://
     # sqlalchemy will fail with the postgres:// prefix
     engine = create_engine(serverconf["db_uri"])
@@ -21,29 +21,32 @@
     params = {"user": user}
     sql_query = (
         "select h.timestamp::date as timestamp, count(h.timestamp) as activity "
         "from history h "
         "inner join users u on h.user_id=u.id "
         "where u.username = %(user)s"
     )
+    if from_:
+        params["from"] = from_
+        sql_query += " and h.timestamp::date >= %(from)s"
 
     if until:
         params["until"] = until
         sql_query += " and h.timestamp::date <= %(until)s"
 
     sql_query += " group by timestamp::date order by timestamp"
 
     try:
         df = pd.read_sql_query(sql_query, con=engine, params=params)
     except Exception as e:
         print(e)
         return False
 
     if df.empty:
-        print(f"no data found for user: {user} / until: {until}")
+        print(f"no data found for user: {user} / from: {from_} / until: {until}")
         return False
     df["timestamp"] = pd.to_datetime(df["timestamp"])
     df.set_index("timestamp", inplace=True)
 
     # get longest streak
     # taken from https://stackoverflow.com/q/23514336
     df = df.resample("D").sum()  # add missing dates to df
```

### Comparing `atuin_graph-1.0.2/img/shell.history.gif` & `atuin_graph-1.1.0/img/shell.history.gif`

 * *Files identical despite different names*

### Comparing `atuin_graph-1.0.2/LICENSE` & `atuin_graph-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `atuin_graph-1.0.2/pyproject.toml` & `atuin_graph-1.1.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `atuin_graph-1.0.2/PKG-INFO` & `atuin_graph-1.1.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: atuin-graph
-Version: 1.0.2
+Version: 1.1.0
 Summary: activity graph for atuin
 Project-URL: Homepage, https://github.com/tieum/atuin-graph
 Project-URL: Bug Tracker, https://github.com/tieum/atuin-graph/issues
 Author-email: matthieu@bluegreen.sh
 License-Expression: MIT
 License-File: LICENSE
 Requires-Python: >=3.11
@@ -60,18 +60,22 @@
 
 ```bash
 usage: atuin-graph [-h] --user USER [--until UNTIL]
 
                       [--atuin_server_config ATUIN_SERVER_CONFIG]
 ```
 ##  web app
-This package also ships a `Flask`app which dynamically serves a png for a given user and optional date
-```bash
-https://my-atuin-server/graph/username[/yyyy-mm-dd]
-```
+This package also ships a Flask app which dynamically serves a png for a given user and optional dates
+
+ |📅️ | |
+|--------------- | --------------- |
+|from a date| `https://my-atuin-server/graph/username/from/yyyy-mm-dd`|
+|until a date| `https://my-atuin-server/graph/username/until/yyyy-mm-dd` <br/> `https://my-atuin-server/graph/username/yyyy-mm-dd` |
+|between dates| `https://my-atuin-server/graph/username/yyyy-mm-dd/yyyy-mm-dd`|
+
 
 one way to run it:
 
 ```bash
 GUNICORN_CMD_ARGS="--bind=127.0.0.1:8889" SCRIPT_NAME=/graph gunicorn atuin_graph.web:app
 ```
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

