# Comparing `tmp/GMMA-1.1.8.tar.gz` & `tmp/GMMA-1.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "GMMA-1.1.8.tar", last modified: Fri Mar 17 03:30:28 2023, max compression
+gzip compressed data, was "GMMA-1.1.9.tar", last modified: Tue Mar 28 00:25:56 2023, max compression
```

## Comparing `GMMA-1.1.8.tar` & `GMMA-1.1.9.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-17 03:30:28.620565 GMMA-1.1.8/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-17 03:30:28.620565 GMMA-1.1.8/GMMA.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-17 03:30:28.000000 GMMA-1.1.8/GMMA.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      317 2023-03-17 03:30:28.000000 GMMA-1.1.8/GMMA.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-17 03:30:28.000000 GMMA-1.1.8/GMMA.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       37 2023-03-17 03:30:28.000000 GMMA-1.1.8/GMMA.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-03-17 03:30:28.000000 GMMA-1.1.8/GMMA.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-03-17 03:30:19.000000 GMMA-1.1.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-17 03:30:28.620565 GMMA-1.1.8/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-17 03:30:28.620565 GMMA-1.1.8/gamma/
--rw-r--r--   0 runner    (1001) docker     (123)      330 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    19123 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/_base.py
--rw-r--r--   0 runner    (1001) docker     (123)    37223 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/_bayesian_mixture.py
--rw-r--r--   0 runner    (1001) docker     (123)    33646 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/_gaussian_mixture.py
--rw-r--r--   0 runner    (1001) docker     (123)     7104 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/app.py
--rw-r--r--   0 runner    (1001) docker     (123)    16399 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/seismic_ops.py
--rw-r--r--   0 runner    (1001) docker     (123)    15345 2023-03-17 03:30:19.000000 GMMA-1.1.8/gamma/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-17 03:30:28.620565 GMMA-1.1.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      349 2023-03-17 03:30:19.000000 GMMA-1.1.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-17 03:30:28.620565 GMMA-1.1.8/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     3752 2023-03-17 03:30:19.000000 GMMA-1.1.8/tests/test_seismoc_ops.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-28 00:25:56.970907 GMMA-1.1.9/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-28 00:25:56.966907 GMMA-1.1.9/GMMA.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-28 00:25:56.000000 GMMA-1.1.9/GMMA.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      317 2023-03-28 00:25:56.000000 GMMA-1.1.9/GMMA.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-28 00:25:56.000000 GMMA-1.1.9/GMMA.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       37 2023-03-28 00:25:56.000000 GMMA-1.1.9/GMMA.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-03-28 00:25:56.000000 GMMA-1.1.9/GMMA.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-03-28 00:25:48.000000 GMMA-1.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-28 00:25:56.970907 GMMA-1.1.9/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-28 00:25:56.970907 GMMA-1.1.9/gamma/
+-rw-r--r--   0 runner    (1001) docker     (123)      330 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19123 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37223 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/_bayesian_mixture.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33646 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/_gaussian_mixture.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7104 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16699 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/seismic_ops.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16059 2023-03-28 00:25:48.000000 GMMA-1.1.9/gamma/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-28 00:25:56.970907 GMMA-1.1.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      349 2023-03-28 00:25:48.000000 GMMA-1.1.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-28 00:25:56.970907 GMMA-1.1.9/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     3752 2023-03-28 00:25:48.000000 GMMA-1.1.9/tests/test_seismoc_ops.py
```

### Comparing `GMMA-1.1.8/LICENSE` & `GMMA-1.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `GMMA-1.1.8/gamma/_base.py` & `GMMA-1.1.9/gamma/_base.py`

 * *Files identical despite different names*

### Comparing `GMMA-1.1.8/gamma/_bayesian_mixture.py` & `GMMA-1.1.9/gamma/_bayesian_mixture.py`

 * *Files identical despite different names*

### Comparing `GMMA-1.1.8/gamma/_gaussian_mixture.py` & `GMMA-1.1.9/gamma/_gaussian_mixture.py`

 * *Files identical despite different names*

### Comparing `GMMA-1.1.8/gamma/app.py` & `GMMA-1.1.9/gamma/app.py`

 * *Files identical despite different names*

### Comparing `GMMA-1.1.8/gamma/seismic_ops.py` & `GMMA-1.1.9/gamma/seismic_ops.py`

 * *Files 2% similar despite different names*

```diff
@@ -339,16 +339,16 @@
     phase_type,
     station_loc,
     weight,
     event_loc0,
     eikonal=None,
     vel={"p": 6.0, "s": 6.0 / 1.75},
     bounds=None,
-    max_iter=10,
-    convergence=1e-3,
+    max_iter=100,
+    convergence=1e-6,
 ):
     if eikonal is None:
         event_loc, loss = linloc(
             event_loc0,
             phase_time,
             phase_type,
             station_loc,
@@ -438,19 +438,24 @@
     ## performance is ok
     # sigma = np.array([1.0,1.0])
     # prob = np.sum(1.0/sigma * np.exp( - (means - X) ** 2 / (2 * sigma**2)), axis=-1).T # (n_components, n_samples, n_features) -> (n_samples, n_components)
     # prob_sum = np.sum(prob, axis=1, keepdims=True)
     # prob_sum[prob_sum == 0] = 1.0
     # resp = prob / prob_sum
 
-    dist = np.linalg.norm(means - X, axis=-1).T  # (n_components, n_samples, n_features) -> (n_samples, n_components)
-    resp = np.exp(-dist)
-    resp_sum = resp.sum(axis=1, keepdims=True)
-    resp_sum[resp_sum == 0] = 1.0
-    resp = resp / resp_sum
+    # dist = np.linalg.norm(means - X, axis=-1).T  # (n_components, n_samples, n_features) -> (n_samples, n_components)
+    # resp = np.exp(-dist)
+    # resp_sum = resp.sum(axis=1, keepdims=True)
+    # resp_sum[resp_sum == 0] = 1.0
+    # resp = resp / resp_sum
+
+    # proposed by Yaqi
+    dist = np.linalg.norm(means - X, axis=-1) # (n_components, n_samples, n_features) -> (n_components, n_samples)
+    resp = np.exp(-dist/(np.median(dist, axis=0, keepdims=True)/10.0)).T 
+    resp /= np.sum(resp, axis=1, keepdims=True) # (n_components, n_samples)
 
     if n_features == 2:
         for i in range(n_components):
             centers[i, -1:] = calc_mag(X[:, 1:2], centers_init[i : i + 1, :-1], station_locs, resp[:, i : i + 1])
 
     return resp, centers, means
```

### Comparing `GMMA-1.1.8/gamma/utils.py` & `GMMA-1.1.9/gamma/utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 import multiprocessing as mp
+from collections import Counter
 from datetime import datetime
+
 import numpy as np
 import pandas as pd
 from sklearn.cluster import DBSCAN
 
 from ._bayesian_mixture import BayesianGaussianMixture
 from ._gaussian_mixture import GaussianMixture
 from .seismic_ops import calc_amp, calc_time, initialize_eikonal
@@ -62,99 +64,112 @@
     if ("use_dbscan" in config) and config["use_dbscan"]:
         # db = DBSCAN(eps=config["dbscan_eps"], min_samples=config["dbscan_min_samples"]).fit(data[:, 0:1])
         db = DBSCAN(eps=config["dbscan_eps"], min_samples=config["dbscan_min_samples"]).fit(
             np.hstack([data[:, 0:1], locs[:, :2] / np.average(vel["p"])])
         )
         labels = db.labels_
         unique_labels = set(labels)
-        if -1 in unique_labels:
-            unique_labels.remove(-1)
+        unique_labels = unique_labels.difference([-1])
     else:
         labels = np.zeros(len(data))
         unique_labels = [0]
 
     if "ncpu" not in config:
         config["ncpu"] = max(1, min(len(unique_labels)//4, mp.cpu_count() - 1))
 
     if len(unique_labels) == 1:
-        events = []
-        assignment = []
         event_idx = 0
         print(f"Associating {len(data)} picks with {config['ncpu']} CPUs")
         events, assignment = associate(
+            list(unique_labels)[0],
+            labels,
             data,
             locs,
             phase_type,
             phase_weight,
             pick_idx,
             pick_station_id,
             config,
             timestamp0,
             vel,
             method,
-            events,
-            assignment,
             event_idx,
         )
     else:
-        # manager = mp.Manager()
-        with mp.Manager() as manager:
-            events = manager.list([])
-            assignment = manager.list([])  ## from picks to events
-            lock = manager.Lock()
-            event_idx = manager.Value("i", event_idx0)
-
-            print(f"Associating {len(unique_labels)} clusters with {config['ncpu']} CPUs")
-            with mp.Pool(config["ncpu"]) as p:
-                p.starmap(
-                    associate,
+        manager = mp.Manager()
+        lock = manager.Lock()
+        # event_idx0 - 1 as event_idx is increased before use
+        event_idx = manager.Value("i", event_idx0 - 1)
+
+        print(f"Associating {len(unique_labels)} clusters with {config['ncpu']} CPUs")
+
+        # the following sort and shuffle is to make sure jobs are distributed evenly
+        counter=Counter(labels)
+        unique_labels = sorted(unique_labels, key=lambda x: counter[x], reverse=True)
+        np.random.shuffle(unique_labels)
+
+        # the default chunk_size is len(unique_labels)//(config["ncpu"]*4), which makes some jobs very heavy
+        chunk_size = max(len(unique_labels)//(config["ncpu"]*20), 1)
+        with mp.get_context('spawn').Pool(config["ncpu"]) as p:
+            results = p.starmap(
+                associate,
+                [
                     [
-                        [
-                            data[labels == k],
-                            locs[labels == k],
-                            phase_type[labels == k],
-                            phase_weight[labels == k],
-                            pick_idx[labels == k],
-                            pick_station_id[labels == k],
-                            config,
-                            timestamp0,
-                            vel,
-                            method,
-                            events,
-                            assignment,
-                            event_idx,
-                            lock,
-                        ]
-                        for k in unique_labels
-                    ],
-                )
-            
-            events = list(events)
-            assignment = list(assignment)
-
-    return events, assignment  # , event_idx.value
+                        k,
+                        labels,
+                        data,
+                        locs,
+                        phase_type,
+                        phase_weight,
+                        pick_idx,
+                        pick_station_id,
+                        config,
+                        timestamp0,
+                        vel,
+                        method,
+                        event_idx,
+                        lock,
+                    ]
+                    for k in unique_labels
+                ],
+                chunksize=chunk_size,
+            )
+            # resuts is a list of tuples, each tuple contains two lists events and assignment
+            # here we flatten the list of tuples into two lists
+            events, assignment = [],[]
+            for each_events, each_assignment in results:
+                events.extend(each_events)
+                assignment.extend(each_assignment)
 
+    return events, assignment # , event_idx.value
 
 def associate(
-    data_,
-    locs_,
-    phase_type_,
-    phase_weight_,
-    pick_idx_,
-    pick_station_id_,
+    k,
+    labels,
+    data,
+    locs,
+    phase_type,
+    phase_weight,
+    pick_idx,
+    pick_station_id,
     config,
     timestamp0,
     vel,
     method,
-    events,
-    assignment,
     event_idx,
     lock=None,
 ):
     print(".", end="")
+    
+    data_=data[labels==k]
+    locs_=locs[labels==k]
+    phase_type_=phase_type[labels==k]
+    phase_weight_=phase_weight[labels==k]
+    pick_idx_=pick_idx[labels==k]
+    pick_station_id_=pick_station_id[labels==k]
 
     if len(pick_idx_) < max(3, config["min_picks_per_eq"]):
         return [], []
 
     time_range = max(data_[:, 0].max() - data_[:, 0].min(), 1)
 
     ## initialization with 5 horizontal points and N//5 time points
@@ -211,14 +226,17 @@
     prob_matrix = gmm.predict_proba(data_)
     prob_eq = prob_matrix.sum(axis=0)
     #  prob = prob_matrix[range(len(data_)), pred]
     #  score = gmm.score(data_)
     #  score_sample = gmm.score_samples(data_)
 
     ## filtering
+    events = []
+    assignment = []
+
     for i in range(len(centers_init)):
         tmp_data = data_[pred == i]
         tmp_locs = locs_[pred == i]
         tmp_pick_station_id = pick_station_id_[pred == i]
         tmp_phase_type = phase_type_[pred == i]
         if (len(tmp_data) == 0) or (len(tmp_data) < config["min_picks_per_eq"]):
             continue
@@ -275,57 +293,54 @@
             if len(tmp_data[idx_filter & (tmp_phase_type == "p")]) < config["min_p_picks_per_eq"]:
                 continue
         if "min_s_picks_per_eq" in config:
             if len(tmp_data[idx_filter & (tmp_phase_type == "s")]) < config["min_s_picks_per_eq"]:
                 continue
 
         if lock is not None:
-            lock.acquire()
-        
-        try:
+            with lock:
+                if not isinstance(event_idx, int):
+                    event_idx.value += 1
+                    event_idx_value = event_idx.value
+                else:
+                    event_idx += 1
+                    event_idx_value = event_idx
+        else:
             if not isinstance(event_idx, int):
+                event_idx.value += 1
                 event_idx_value = event_idx.value
             else:
+                event_idx += 1
                 event_idx_value = event_idx
 
-            event = {
-                # "time": from_seconds(gmm.centers_[i, len(config["dims"])]),
-                "time": datetime.utcfromtimestamp(gmm.centers_[i, len(config["dims"])] + timestamp0).isoformat(
-                    timespec="milliseconds"
-                ),
-                # "time(s)": gmm.centers_[i, len(config["dims"])],
-                "magnitude": gmm.centers_[i, len(config["dims"]) + 1] if config["use_amplitude"] else 999,
-                "sigma_time": np.sqrt(gmm.covariances_[i, 0, 0]),
-                "sigma_amp": np.sqrt(gmm.covariances_[i, 1, 1]) if config["use_amplitude"] else 0,
-                "cov_time_amp": gmm.covariances_[i, 0, 1] if config["use_amplitude"] else 0,
-                "gamma_score": prob_eq[i],
-                "number_picks": len(tmp_data[idx_filter]),
-                "number_p_picks": len(tmp_data[idx_filter & (tmp_phase_type == "p")]),
-                "number_s_picks": len(tmp_data[idx_filter & (tmp_phase_type == "s")]),
-                "event_index": event_idx_value,
-            }
-            for j, k in enumerate(config["dims"]):  ## add location
-                event[k] = gmm.centers_[i, j]
-            events.append(event)
+        event = {
+            # "time": from_seconds(gmm.centers_[i, len(config["dims"])]),
+            "time": datetime.utcfromtimestamp(gmm.centers_[i, len(config["dims"])] + timestamp0).isoformat(
+                timespec="milliseconds"
+            ),
+            # "time(s)": gmm.centers_[i, len(config["dims"])],
+            "magnitude": gmm.centers_[i, len(config["dims"]) + 1] if config["use_amplitude"] else 999,
+            "sigma_time": np.sqrt(gmm.covariances_[i, 0, 0]),
+            "sigma_amp": np.sqrt(gmm.covariances_[i, 1, 1]) if config["use_amplitude"] else 0,
+            "cov_time_amp": gmm.covariances_[i, 0, 1] if config["use_amplitude"] else 0,
+            "gamma_score": prob_eq[i],
+            "number_picks": len(tmp_data[idx_filter]),
+            "number_p_picks": len(tmp_data[idx_filter & (tmp_phase_type == "p")]),
+            "number_s_picks": len(tmp_data[idx_filter & (tmp_phase_type == "s")]),
+            "event_index": event_idx_value,
+        }
+        for j, k in enumerate(config["dims"]):  ## add location
+            event[k] = gmm.centers_[i, j]
+        events.append(event)
 
-            for pi, pr in zip(pick_idx_[pred == i][idx_filter], prob):
-                assignment.append((pi, event_idx_value, pr))
-
-            if not isinstance(event_idx, int):
-                event_idx.value += 1
-            else:
-                event_idx += 1
-
-        finally:
-            if lock is not None:
-                lock.release()
+        for pi, pr in zip(pick_idx_[pred == i][idx_filter], prob):
+            assignment.append((pi, event_idx_value, pr))
 
         if (event_idx_value + 1) % 100 == 0:
             print(f"\nFinish {event_idx_value} events")
-
     return events, assignment
 
 
 def init_centers(config, data_, locs_, time_range):
     if "initial_points" in config:
         initial_points = config["initial_points"]
         if not isinstance(initial_points, list):
```

### Comparing `GMMA-1.1.8/tests/test_seismoc_ops.py` & `GMMA-1.1.9/tests/test_seismoc_ops.py`

 * *Files identical despite different names*

