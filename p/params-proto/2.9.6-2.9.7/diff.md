# Comparing `tmp/params_proto-2.9.6-py3-none-any.whl.zip` & `tmp/params_proto-2.9.7-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,20 +1,20 @@
-Zip file size: 37357 bytes, number of entries: 18
+Zip file size: 37387 bytes, number of entries: 18
 -rw-r--r--  2.0 unx      117 b- defN 20-Aug-05 00:59 params_proto/__init__.py
 -rw-r--r--  2.0 unx     3163 b- defN 20-Aug-05 00:59 params_proto/hyper.py
--rw-r--r--  2.0 unx    12833 b- defN 21-Nov-17 14:58 params_proto/neo_hyper.py
+-rw-r--r--  2.0 unx    12867 b- defN 22-Jun-25 15:38 params_proto/neo_hyper.py
 -rw-r--r--  2.0 unx     1125 b- defN 20-Aug-05 07:27 params_proto/neo_partial.py
--rw-r--r--  2.0 unx    14629 b- defN 21-Nov-08 19:01 params_proto/neo_proto.py
+-rw-r--r--  2.0 unx    14629 b- defN 22-Feb-14 14:04 params_proto/neo_proto.py
 -rw-r--r--  2.0 unx     9292 b- defN 21-Mar-04 01:07 params_proto/params_proto.py
 -rw-r--r--  2.0 unx     1530 b- defN 19-Dec-11 12:38 params_proto/utils.py
 -rw-r--r--  2.0 unx      309 b- defN 21-Jan-20 06:22 params_proto/__pycache__/__init__.cpython-36.pyc
 -rw-r--r--  2.0 unx     4430 b- defN 21-Jan-20 06:22 params_proto/__pycache__/hyper.cpython-36.pyc
 -rw-r--r--  2.0 unx     8330 b- defN 21-Jan-20 06:22 params_proto/__pycache__/neo_hyper.cpython-36.pyc
 -rw-r--r--  2.0 unx    12285 b- defN 21-Jan-20 06:35 params_proto/__pycache__/neo_proto.cpython-36.pyc
 -rw-r--r--  2.0 unx     9149 b- defN 21-Jan-20 06:22 params_proto/__pycache__/params_proto.cpython-36.pyc
 -rw-r--r--  2.0 unx     1257 b- defN 21-Jan-20 06:22 params_proto/__pycache__/utils.cpython-36.pyc
--rw-r--r--  2.0 unx     1526 b- defN 21-Nov-17 15:00 params_proto-2.9.6.dist-info/LICENSE.md
--rw-r--r--  2.0 unx     8443 b- defN 21-Nov-17 15:00 params_proto-2.9.6.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 21-Nov-17 15:00 params_proto-2.9.6.dist-info/WHEEL
--rw-r--r--  2.0 unx       13 b- defN 21-Nov-17 15:00 params_proto-2.9.6.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1615 b- defN 21-Nov-17 15:00 params_proto-2.9.6.dist-info/RECORD
-18 files, 90138 bytes uncompressed, 34675 bytes compressed:  61.5%
+-rw-r--r--  2.0 unx     1526 b- defN 22-Jun-25 15:41 params_proto-2.9.7.dist-info/LICENSE.md
+-rw-r--r--  2.0 unx     8486 b- defN 22-Jun-25 15:41 params_proto-2.9.7.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 22-Jun-25 15:41 params_proto-2.9.7.dist-info/WHEEL
+-rw-r--r--  2.0 unx       13 b- defN 22-Jun-25 15:41 params_proto-2.9.7.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1615 b- defN 22-Jun-25 15:41 params_proto-2.9.7.dist-info/RECORD
+18 files, 90215 bytes uncompressed, 34705 bytes compressed:  61.5%
```

## zipnote {}

```diff
@@ -33,23 +33,23 @@
 
 Filename: params_proto/__pycache__/params_proto.cpython-36.pyc
 Comment: 
 
 Filename: params_proto/__pycache__/utils.cpython-36.pyc
 Comment: 
 
-Filename: params_proto-2.9.6.dist-info/LICENSE.md
+Filename: params_proto-2.9.7.dist-info/LICENSE.md
 Comment: 
 
-Filename: params_proto-2.9.6.dist-info/METADATA
+Filename: params_proto-2.9.7.dist-info/METADATA
 Comment: 
 
-Filename: params_proto-2.9.6.dist-info/WHEEL
+Filename: params_proto-2.9.7.dist-info/WHEEL
 Comment: 
 
-Filename: params_proto-2.9.6.dist-info/top_level.txt
+Filename: params_proto-2.9.7.dist-info/top_level.txt
 Comment: 
 
-Filename: params_proto-2.9.6.dist-info/RECORD
+Filename: params_proto-2.9.7.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## params_proto/neo_hyper.py

```diff
@@ -284,15 +284,17 @@
             line = f.readline().strip()
             while line:  # need to handle end of line
                 if not line.startswith("//"):
                     sweep.append(json.loads(line.strip()))
                 line = f.readline().strip()
         return sweep
 
-    def load(self, sweep="sweep.jsonl", strict=True, silent=False):
+    file = None
+
+    def load(self, file="sweep.jsonl", strict=True, silent=False):
         """
         Loading sweep state from a jsonl file:
 
         Note: **Important Caveat** When multiple prefix-free ParamsProto objects are present,
             We sweep through all of the proto objects and sets the attribute to the first
             proto with the correct key. This first-attr approach works because the ParamsProto
             object also generates argparse parameters, which means repetitive arguments are
@@ -316,22 +318,24 @@
             for i, deps in enumerate(sweep):
                 assert RUN.job_id == i + 1, "the job_id in that sweep.json should be 1-based."
 
         """
         import pandas as pd
         from termcolor import colored
 
-        if isinstance(sweep, str):
-            sweep = self.read(sweep)
-        if isinstance(sweep, list):
-            df = pd.DataFrame(sweep)
-        elif isinstance(sweep, pd.DataFrame):
-            df = sweep
+        self.file = file
+
+        if isinstance(file, str):
+            file = self.read(file)
+        if isinstance(file, list):
+            df = pd.DataFrame(file)
+        elif isinstance(file, pd.DataFrame):
+            df = file
         else:
-            raise TypeError(f"{type(sweep)} is not supported")
+            raise TypeError(f"{type(file)} is not supported")
 
         with self.zip:
             for full_key in df:
                 prefix, *keys = full_key.split('.')
                 if prefix in self.root:
                     proto = self.root[prefix]
                     if not hasattr(proto, keys[0]):
```

## Comparing `params_proto-2.9.6.dist-info/LICENSE.md` & `params_proto-2.9.7.dist-info/LICENSE.md`

 * *Files identical despite different names*

## Comparing `params_proto-2.9.6.dist-info/METADATA` & `params_proto-2.9.7.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 Metadata-Version: 2.1
 Name: params-proto
-Version: 2.9.6
+Version: 2.9.7
 Summary: A command line argument parsing utility using python class-based namespace for better IDE static auto-completion
 Home-page: https://github.com/episodeyang/params_proto
 Author: Ge Yang
 Author-email: yangge1987@gmail.com
 License: UNKNOWN
 Keywords: params_proto,decorator,argparse,argcomplete,auto-completion,autocomplete,shell arguments,argument parser
 Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Science/Research
 Classifier: Programming Language :: Python :: 3
+License-File: LICENSE.md
 Requires-Dist: waterbear (>=2.6.5)
 Requires-Dist: argparse
 Requires-Dist: argcomplete
 Requires-Dist: typing
 Requires-Dist: expandvars
 
 ``params-proto``, A Python Decorator That Gives Your Model Parameters Super-power
@@ -114,30 +115,30 @@
    if __name__ == '__main__':
        from lp_analysis import instr
 
        with Sweep(Args, LfGR) as sweep:
            # override the default
            Args.pi_lr = 3e-3
            Args.clip_inputs = True # this was a flag
-
+           
            # override the second config object
            LfGR.visualization_interval = 40
 
            # product between the zipped and the seed
            with sweep.product:
 
                # similar to python zip, unpacks a list of values.
                with sweep.zip:
                    Args.env_name = ['FetchReach-v1', 'FetchPush-v1', 'FetchPickAndPlace-v1', 'FetchSlide-v1']
                    Args.n_epochs = [4, 12, 12, 20]
                    Args.n_workers = [5, 150, 200, 500]
 
                # the seed is sweeped at last
                Args.seed = [100, 200, 300, 400, 500, 600]
-
+       
        # You can save the sweep into a `jsonl` file
        sweep.save('sweep.jsonl')
 
        for i, deps in sweep.items():
            thunk = instr(main, deps, _job_postfix=f"{Args.env_name}")
            print(deps)
```

## Comparing `params_proto-2.9.6.dist-info/RECORD` & `params_proto-2.9.7.dist-info/RECORD`

 * *Files 10% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 params_proto/__init__.py,sha256=yHzaOshHfDNxniQ5zV1HrVbXUfaEwdLXKPjoDoaas88,117
 params_proto/hyper.py,sha256=zFEE5Xbl5m8XJ1j92mfoCpHHkVettQk4gBgEaUqRZV8,3163
-params_proto/neo_hyper.py,sha256=5g-wodyKNQQfYl1rs5OYTc0Pn6O2-T48NdDlN0YYCOU,12833
+params_proto/neo_hyper.py,sha256=o9cbix5j1GqafYJFCBncz2tRz_QhKR-vrARcofiyQJQ,12867
 params_proto/neo_partial.py,sha256=4DUoRvpniDS9AzfaDt6ufjYGRudIBKCnwRyn17XfsmM,1125
 params_proto/neo_proto.py,sha256=nJPZuh-U4Bs7L_ZRD3eO2x5yUmRrOnSmS4SID-URv9U,14629
 params_proto/params_proto.py,sha256=saPuNEyfgWq2GXAMDwbFb01_1YRpQ0Puht-aoZX4zl8,9292
 params_proto/utils.py,sha256=CVjjx_ynou2EdpOBRuRPwEqOwtiGxvvOTbGualDhBAg,1530
 params_proto/__pycache__/__init__.cpython-36.pyc,sha256=6tP793uVPW1mt0QG_3urXr_i8oytoA1nZG-kHp97Rx4,309
 params_proto/__pycache__/hyper.cpython-36.pyc,sha256=Lr8cxIEwOs1diXpONLCnxVDlcp6GUSZBAK3QfxyYO5w,4430
 params_proto/__pycache__/neo_hyper.cpython-36.pyc,sha256=TmJJm9fltC10kQHXvlfNTHdN_6AWaTWQ9sixIqT9gUk,8330
 params_proto/__pycache__/neo_proto.cpython-36.pyc,sha256=v4O_Dl6vOnh368_LWY_IDjkjuu2WCs7tvrZ_YlNBUJI,12285
 params_proto/__pycache__/params_proto.cpython-36.pyc,sha256=XPbbZo2jQ7rSy6V-Txqivv-0knAoWcPZTrgH5JByZhU,9149
 params_proto/__pycache__/utils.cpython-36.pyc,sha256=gDOtrNoWIubpgHovQE9kukWZrlXmqA68ljdnzst19W0,1257
-params_proto-2.9.6.dist-info/LICENSE.md,sha256=c2qSYi9tUMZtzj9SEsMeKhub5LJUmHwBtDLiIMM5b6U,1526
-params_proto-2.9.6.dist-info/METADATA,sha256=NghZkPmsPmE_62ODcW9i7glB4hIw_A0ies_YSv20CO8,8443
-params_proto-2.9.6.dist-info/WHEEL,sha256=OqRkF0eY5GHssMorFjlbTIq072vpHpF60fIQA6lS9xA,92
-params_proto-2.9.6.dist-info/top_level.txt,sha256=WrUs3p5VrdGRpHUDLBBAx6fkb25RS4F9qC8oGc4qCxA,13
-params_proto-2.9.6.dist-info/RECORD,,
+params_proto-2.9.7.dist-info/LICENSE.md,sha256=c2qSYi9tUMZtzj9SEsMeKhub5LJUmHwBtDLiIMM5b6U,1526
+params_proto-2.9.7.dist-info/METADATA,sha256=zm5UNVv9gjVsj3NXkuRwiZi-p0GpGNDGQGXv7cHuJuc,8486
+params_proto-2.9.7.dist-info/WHEEL,sha256=G16H4A3IeoQmnOrYV4ueZGKSjhipXx8zc8nu9FGlvMA,92
+params_proto-2.9.7.dist-info/top_level.txt,sha256=WrUs3p5VrdGRpHUDLBBAx6fkb25RS4F9qC8oGc4qCxA,13
+params_proto-2.9.7.dist-info/RECORD,,
```

