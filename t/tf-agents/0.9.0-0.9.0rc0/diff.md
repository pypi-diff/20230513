# Comparing `tmp/tf_agents-0.9.0-py3-none-any.whl.zip` & `tmp/tf_agents-0.9.0rc0-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 1263395 bytes, number of entries: 527
+Zip file size: 1263438 bytes, number of entries: 527
 -rw-r--r--  2.0 unx     3347 b- defN 21-Aug-06 20:54 tf_agents/__init__.py
 -rw-r--r--  2.0 unx     1210 b- defN 21-Aug-06 20:54 tf_agents/tf_agents_api_test.py
--rw-r--r--  2.0 unx     1373 b- defN 21-Aug-12 16:34 tf_agents/version.py
+-rw-r--r--  2.0 unx     1376 b- defN 21-Aug-06 20:54 tf_agents/version.py
 -rw-r--r--  2.0 unx     1806 b- defN 21-Aug-06 20:54 tf_agents/agents/__init__.py
 -rw-r--r--  2.0 unx    17268 b- defN 21-Aug-06 20:54 tf_agents/agents/data_converter.py
 -rw-r--r--  2.0 unx    10424 b- defN 21-Aug-06 20:54 tf_agents/agents/data_converter_test.py
 -rw-r--r--  2.0 unx     3397 b- defN 21-Aug-06 20:54 tf_agents/agents/test_util.py
 -rw-r--r--  2.0 unx    25499 b- defN 21-Aug-06 20:54 tf_agents/agents/tf_agent.py
 -rw-r--r--  2.0 unx     6832 b- defN 21-Aug-06 20:54 tf_agents/agents/tf_agent_test.py
 -rw-r--r--  2.0 unx      710 b- defN 21-Aug-06 20:54 tf_agents/agents/behavioral_cloning/__init__.py
@@ -517,13 +517,13 @@
 -rw-r--r--  2.0 unx     2720 b- defN 21-Aug-06 20:54 tf_agents/utils/test_utils.py
 -rw-r--r--  2.0 unx     1614 b- defN 21-Aug-06 20:54 tf_agents/utils/test_utils_test.py
 -rw-r--r--  2.0 unx     1204 b- defN 21-Aug-06 20:54 tf_agents/utils/timer.py
 -rw-r--r--  2.0 unx     5854 b- defN 21-Aug-06 20:54 tf_agents/utils/value_ops.py
 -rw-r--r--  2.0 unx     8908 b- defN 21-Aug-06 20:54 tf_agents/utils/value_ops_test.py
 -rw-r--r--  2.0 unx     3895 b- defN 21-Aug-06 20:54 tf_agents/utils/xla.py
 -rw-r--r--  2.0 unx     2415 b- defN 21-Aug-06 20:54 tf_agents/utils/xla_test.py
--rw-r-----  2.0 unx    11414 b- defN 21-Aug-12 16:57 tf_agents-0.9.0.dist-info/LICENSE
--rw-r--r--  2.0 unx    10712 b- defN 21-Aug-12 16:57 tf_agents-0.9.0.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 21-Aug-12 16:57 tf_agents-0.9.0.dist-info/WHEEL
--rw-r--r--  2.0 unx       10 b- defN 21-Aug-12 16:57 tf_agents-0.9.0.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx    53535 b- defN 21-Aug-12 16:57 tf_agents-0.9.0.dist-info/RECORD
-527 files, 4407087 bytes uncompressed, 1176311 bytes compressed:  73.3%
+-rw-r-----  2.0 unx    11414 b- defN 21-Aug-10 13:59 tf_agents-0.9.0rc0.dist-info/LICENSE
+-rw-r--r--  2.0 unx    10721 b- defN 21-Aug-10 13:59 tf_agents-0.9.0rc0.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 21-Aug-10 13:59 tf_agents-0.9.0rc0.dist-info/WHEEL
+-rw-r--r--  2.0 unx       10 b- defN 21-Aug-10 13:59 tf_agents-0.9.0rc0.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx    53550 b- defN 21-Aug-10 13:59 tf_agents-0.9.0rc0.dist-info/RECORD
+527 files, 4407114 bytes uncompressed, 1176324 bytes compressed:  73.3%
```

## zipnote {}

```diff
@@ -1560,23 +1560,23 @@
 
 Filename: tf_agents/utils/xla.py
 Comment: 
 
 Filename: tf_agents/utils/xla_test.py
 Comment: 
 
-Filename: tf_agents-0.9.0.dist-info/LICENSE
+Filename: tf_agents-0.9.0rc0.dist-info/LICENSE
 Comment: 
 
-Filename: tf_agents-0.9.0.dist-info/METADATA
+Filename: tf_agents-0.9.0rc0.dist-info/METADATA
 Comment: 
 
-Filename: tf_agents-0.9.0.dist-info/WHEEL
+Filename: tf_agents-0.9.0rc0.dist-info/WHEEL
 Comment: 
 
-Filename: tf_agents-0.9.0.dist-info/top_level.txt
+Filename: tf_agents-0.9.0rc0.dist-info/top_level.txt
 Comment: 
 
-Filename: tf_agents-0.9.0.dist-info/RECORD
+Filename: tf_agents-0.9.0rc0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## tf_agents/version.py

```diff
@@ -22,15 +22,15 @@
 
 # When building releases, we can update this value on the release branch to
 # reflect the current release candidate ('rc0', 'rc1') or, finally, the official
 # stable release (indicated by `_REL_SUFFIX = ''`). Outside the context of a
 # release branch, the current version is by default assumed to be a
 # 'development' version, labeled 'dev'.
 _DEV_SUFFIX = 'dev'
-_REL_SUFFIX = ''
+_REL_SUFFIX = 'rc0'
 
 # Example, '0.9.0rc0'
 __version__ = '.'.join([
     _MAJOR_VERSION,
     _MINOR_VERSION,
     _PATCH_VERSION,
 ])
```

## Comparing `tf_agents-0.9.0.dist-info/LICENSE` & `tf_agents-0.9.0rc0.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `tf_agents-0.9.0.dist-info/METADATA` & `tf_agents-0.9.0rc0.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tf-agents
-Version: 0.9.0
+Version: 0.9.0rc0
 Summary: TF-Agents: A Reinforcement Learning Library for TensorFlow
 Home-page: https://github.com/tensorflow/agents
 Author: Google LLC
 Author-email: no-reply@google.com
 License: Apache 2.0
 Keywords: tensorflow agents reinforcement learning machine bandits
 Platform: UNKNOWN
@@ -31,18 +31,18 @@
 Requires-Dist: gin-config (>=0.4.0)
 Requires-Dist: gym (>=0.17.0)
 Requires-Dist: numpy (>=1.13.3)
 Requires-Dist: six (>=1.10.0)
 Requires-Dist: protobuf (>=3.11.3)
 Requires-Dist: wrapt (>=1.11.1)
 Requires-Dist: typing-extensions (>=3.7.4.3)
-Requires-Dist: tensorflow-probability (>=0.13.0)
+Requires-Dist: tensorflow-probability (==0.13.0)
 Provides-Extra: reverb
-Requires-Dist: dm-reverb (~=0.4.0) ; extra == 'reverb'
-Requires-Dist: tensorflow (~=2.6.0) ; extra == 'reverb'
+Requires-Dist: dm-reverb (==0.4.0rc0) ; extra == 'reverb'
+Requires-Dist: tensorflow (==2.6.0rc2) ; extra == 'reverb'
 Provides-Extra: tests
 Requires-Dist: atari-py (==0.1.7) ; extra == 'tests'
 Requires-Dist: mock (>=2.0.0) ; extra == 'tests'
 Requires-Dist: opencv-python (>=3.4.1.15) ; extra == 'tests'
 Requires-Dist: pybullet ; extra == 'tests'
 Requires-Dist: scipy (==1.1.0) ; extra == 'tests'
```

### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: tf-agents Version: 0.9.0 Summary: TF-Agents: A
+Metadata-Version: 2.1 Name: tf-agents Version: 0.9.0rc0 Summary: TF-Agents: A
 Reinforcement Learning Library for TensorFlow Home-page: https://github.com/
 tensorflow/agents Author: Google LLC Author-email: no-reply@google.com License:
 Apache 2.0 Keywords: tensorflow agents reinforcement learning machine bandits
 Platform: UNKNOWN Classifier: Development Status :: 3 - Alpha Classifier:
 Intended Audience :: Developers Classifier: Intended Audience :: Education
 Classifier: Intended Audience :: Science/Research Classifier: License :: OSI
 Approved :: Apache Software License Classifier: Programming Language :: Python
@@ -14,17 +14,17 @@
 Topic :: Software Development :: Libraries Classifier: Topic :: Software
 Development :: Libraries :: Python Modules Requires-Python: >=3 Description-
 Content-Type: text/markdown License-File: LICENSE Requires-Dist: absl-py
 (>=0.6.1) Requires-Dist: cloudpickle (>=1.3) Requires-Dist: gin-config
 (>=0.4.0) Requires-Dist: gym (>=0.17.0) Requires-Dist: numpy (>=1.13.3)
 Requires-Dist: six (>=1.10.0) Requires-Dist: protobuf (>=3.11.3) Requires-Dist:
 wrapt (>=1.11.1) Requires-Dist: typing-extensions (>=3.7.4.3) Requires-Dist:
-tensorflow-probability (>=0.13.0) Provides-Extra: reverb Requires-Dist: dm-
-reverb (~=0.4.0) ; extra == 'reverb' Requires-Dist: tensorflow (~=2.6.0) ;
-extra == 'reverb' Provides-Extra: tests Requires-Dist: atari-py (==0.1.7) ;
+tensorflow-probability (==0.13.0) Provides-Extra: reverb Requires-Dist: dm-
+reverb (==0.4.0rc0) ; extra == 'reverb' Requires-Dist: tensorflow (==2.6.0rc2)
+; extra == 'reverb' Provides-Extra: tests Requires-Dist: atari-py (==0.1.7) ;
 extra == 'tests' Requires-Dist: mock (>=2.0.0) ; extra == 'tests' Requires-
 Dist: opencv-python (>=3.4.1.15) ; extra == 'tests' Requires-Dist: pybullet ;
 extra == 'tests' Requires-Dist: scipy (==1.1.0) ; extra == 'tests' # TF-Agents:
 A reliable, scalable and easy to use TensorFlow library for Contextual Bandits
 and Reinforcement Learning. [![PyPI tf-agents](https://badge.fury.io/py/tf-
 agents.svg)](https://badge.fury.io/py/tf-agents) [TF-Agents](https://
 github.com/tensorflow/agents) makes implementing, deploying, and testing new
```

## Comparing `tf_agents-0.9.0.dist-info/RECORD` & `tf_agents-0.9.0rc0.dist-info/RECORD`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 tf_agents/__init__.py,sha256=EgFc5E7r7iX7NDdvLDQKUDsATy_vQ_gmkkMl3vG_E5A,3347
 tf_agents/tf_agents_api_test.py,sha256=3WMUhEQPxgM33uyETC6AYtdltdMjR0lpLb3Oua_9opk,1210
-tf_agents/version.py,sha256=24i7NsLtg_z-oAi6juUzuYTG6_aKAQJsWpaytSMjoRc,1373
+tf_agents/version.py,sha256=kHRe11XJLegXvQLseVtEvfIkm1AqBBLx3QkMPGy25Uw,1376
 tf_agents/agents/__init__.py,sha256=eDcntert6i__qmGd_cPRpii3QWSs0xdRkWhvTitt9FA,1806
 tf_agents/agents/data_converter.py,sha256=UZeCMVWyfN6EGxMR43_9up_3xxDjDuXIqpYkP0moVUk,17268
 tf_agents/agents/data_converter_test.py,sha256=ryvNuRhtkA9q0mM1MW3-Mvys1OjAmoAz1Bv-aeFrwgk,10424
 tf_agents/agents/test_util.py,sha256=qqJ33vlWsgNEahJuEmFovaMjGErFhHleM8Y05ZZTMP0,3397
 tf_agents/agents/tf_agent.py,sha256=o3TZ0E5X5KImrGeblh3KuD8ZqJJ9yIrYxXFXg7iqEgE,25499
 tf_agents/agents/tf_agent_test.py,sha256=AOzJ_b5KykR8KZVkc92IMRKWtO-jBVoE7I6D-_J6GCI,6832
 tf_agents/agents/behavioral_cloning/__init__.py,sha256=w8wtjAcyQmYSuP3B1-s14zc1Gvywia7E56cCooJZdzQ,710
@@ -516,12 +516,12 @@
 tf_agents/utils/test_utils.py,sha256=c3R7UEimAe7SA4MwmETK1QK789vU0ShPoJW6oEp1SGg,2720
 tf_agents/utils/test_utils_test.py,sha256=YCAhfBcH7Bs0R5zzKoRkyAVLdLGybG84ub7ohj060TU,1614
 tf_agents/utils/timer.py,sha256=RDgMCdIy9dOXd3kxgXM64NcgqiS8jk1YqbH7q-XUswA,1204
 tf_agents/utils/value_ops.py,sha256=7sSx82o-CGJvbkQ2z3d5O2GeGxmX-JFtU-wolkEAvTc,5854
 tf_agents/utils/value_ops_test.py,sha256=vjfcVPws3YCTEHJfCPzZgrpW2uNlQdfhqyBNrhDFyTM,8908
 tf_agents/utils/xla.py,sha256=3a-7PgW_g9540_rxX7rbX0IlnRd67K5Sbice8xbmSM8,3895
 tf_agents/utils/xla_test.py,sha256=SqC3G8vTe6X4NEcqmTyvgjYiXwhQ-KvqNAbAMhpEtKo,2415
-tf_agents-0.9.0.dist-info/LICENSE,sha256=mWN7znMvTQlt7mTAQO_wG0aiSDBN56ILpR8299cINUA,11414
-tf_agents-0.9.0.dist-info/METADATA,sha256=rFiB7gCMNUwsw9vMAFOctqjcbKI-D1FCqpkHvB0x6ps,10712
-tf_agents-0.9.0.dist-info/WHEEL,sha256=ewwEueio1C2XeHTvT17n8dZUJgOvyCWCt0WVNLClP9o,92
-tf_agents-0.9.0.dist-info/top_level.txt,sha256=ufuDpxU8MB5MMU3IZnWApNkJ7vOsRbDKu6GOwzv_vdQ,10
-tf_agents-0.9.0.dist-info/RECORD,,
+tf_agents-0.9.0rc0.dist-info/LICENSE,sha256=mWN7znMvTQlt7mTAQO_wG0aiSDBN56ILpR8299cINUA,11414
+tf_agents-0.9.0rc0.dist-info/METADATA,sha256=9gg3DrUTaw-K7UedlBDqkWx57JDJTRx2W_7eqO7VZFU,10721
+tf_agents-0.9.0rc0.dist-info/WHEEL,sha256=OqRkF0eY5GHssMorFjlbTIq072vpHpF60fIQA6lS9xA,92
+tf_agents-0.9.0rc0.dist-info/top_level.txt,sha256=ufuDpxU8MB5MMU3IZnWApNkJ7vOsRbDKu6GOwzv_vdQ,10
+tf_agents-0.9.0rc0.dist-info/RECORD,,
```

