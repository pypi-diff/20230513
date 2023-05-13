# Comparing `tmp/gmltools-0.0.62.tar.gz` & `tmp/gmltools-0.0.63.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gmltools-0.0.62.tar", last modified: Fri May 12 09:22:20 2023, max compression
+gzip compressed data, was "gmltools-0.0.63.tar", last modified: Sat May 13 10:13:14 2023, max compression
```

## Comparing `gmltools-0.0.62.tar` & `gmltools-0.0.63.tar`

### file list

```diff
@@ -1,42 +1,42 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.317404 gmltools-0.0.62/
--rw-rw-rw-   0        0        0    35782 2023-03-08 11:55:03.000000 gmltools-0.0.62/LICENSE
--rw-rw-rw-   0        0        0    10875 2023-03-07 08:36:17.000000 gmltools-0.0.62/Models.ipynb
--rw-rw-rw-   0        0        0     1021 2023-05-12 09:22:20.317404 gmltools-0.0.62/PKG-INFO
--rw-rw-rw-   0        0        0      755 2023-03-09 09:37:42.000000 gmltools-0.0.62/README.md
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.092622 gmltools-0.0.62/dist/
--rw-rw-rw-   0        0        0    74791 2023-04-14 10:52:54.000000 gmltools-0.0.62/dist/gmltools-0.0.59.tar.gz
--rw-rw-rw-   0        0        0    17876 2023-03-16 08:30:12.000000 gmltools-0.0.62/gmltools.yml
--rw-rw-rw-   0        0        0    17555 2023-03-06 11:09:12.000000 gmltools-0.0.62/mltools.yml
--rw-rw-rw-   0        0        0      546 2023-05-12 09:21:23.000000 gmltools-0.0.62/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-12 09:22:20.317404 gmltools-0.0.62/setup.cfg
--rw-rw-rw-   0        0        0     1682 2023-05-12 09:21:04.000000 gmltools-0.0.62/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.043668 gmltools-0.0.62/src/
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.099603 gmltools-0.0.62/src/gmltools/
--rw-rw-rw-   0        0        0      879 2023-03-14 15:28:10.000000 gmltools-0.0.62/src/gmltools/To_Do.txt
--rw-rw-rw-   0        0        0      327 2023-03-08 11:50:28.000000 gmltools-0.0.62/src/gmltools/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.138515 gmltools-0.0.62/src/gmltools/eda/
--rw-rw-rw-   0        0        0      327 2023-03-08 11:50:28.000000 gmltools-0.0.62/src/gmltools/eda/__init__.py
--rw-rw-rw-   0        0        0    40126 2023-04-17 07:50:02.000000 gmltools-0.0.62/src/gmltools/eda/eda.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.258306 gmltools-0.0.62/src/gmltools/models/
--rw-rw-rw-   0        0        0      327 2023-03-08 11:51:09.000000 gmltools-0.0.62/src/gmltools/models/__init__.py
--rw-rw-rw-   0        0        0     4893 2023-03-13 11:20:44.000000 gmltools-0.0.62/src/gmltools/models/bayes.py
--rw-rw-rw-   0        0        0     1983 2023-03-16 08:43:00.000000 gmltools-0.0.62/src/gmltools/models/custom_scorings.py
--rw-rw-rw-   0        0        0     5143 2023-04-14 11:04:34.000000 gmltools-0.0.62/src/gmltools/models/dummy_model.py
--rw-rw-rw-   0        0        0   119114 2023-05-09 11:31:39.000000 gmltools-0.0.62/src/gmltools/models/model.py
--rw-rw-rw-   0        0        0     5803 2023-03-07 12:45:49.000000 gmltools-0.0.62/src/gmltools/models/models_info.py
--rw-rw-rw-   0        0        0    13212 2023-05-12 09:20:42.000000 gmltools-0.0.62/src/gmltools/models/timeseriesplit.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.292445 gmltools-0.0.62/src/gmltools/models_analysis/
--rw-rw-rw-   0        0        0      327 2023-03-08 11:50:54.000000 gmltools-0.0.62/src/gmltools/models_analysis/__init__.py
--rw-rw-rw-   0        0        0    73636 2023-04-30 15:51:16.000000 gmltools-0.0.62/src/gmltools/models_analysis/classification_analysis.py
--rw-rw-rw-   0        0        0     5653 2023-04-30 15:57:34.000000 gmltools-0.0.62/src/gmltools/models_analysis/xai.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.316401 gmltools-0.0.62/src/gmltools/preprocess/
--rw-rw-rw-   0        0        0      327 2023-03-08 11:50:40.000000 gmltools-0.0.62/src/gmltools/preprocess/__init__.py
--rw-rw-rw-   0        0        0    18728 2023-03-06 08:35:56.000000 gmltools-0.0.62/src/gmltools/preprocess/autoregressive_features.py
--rw-rw-rw-   0        0        0     8133 2023-02-23 12:30:28.000000 gmltools-0.0.62/src/gmltools/preprocess/manage_holidays.py
--rw-rw-rw-   0        0        0     4045 2023-03-30 08:41:18.000000 gmltools-0.0.62/src/gmltools/preprocess/preprocess.py
-drwxrwxrwx   0        0        0        0 2023-05-12 09:22:20.123408 gmltools-0.0.62/src/gmltools.egg-info/
--rw-rw-rw-   0        0        0     1021 2023-05-12 09:22:19.000000 gmltools-0.0.62/src/gmltools.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      934 2023-05-12 09:22:19.000000 gmltools-0.0.62/src/gmltools.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 09:22:19.000000 gmltools-0.0.62/src/gmltools.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       82 2023-05-12 09:22:19.000000 gmltools-0.0.62/src/gmltools.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-12 09:22:19.000000 gmltools-0.0.62/src/gmltools.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.403435 gmltools-0.0.63/
+-rw-rw-rw-   0        0        0    35782 2023-03-08 11:55:03.000000 gmltools-0.0.63/LICENSE
+-rw-rw-rw-   0        0        0    10875 2023-03-07 08:36:17.000000 gmltools-0.0.63/Models.ipynb
+-rw-rw-rw-   0        0        0     1021 2023-05-13 10:13:14.401296 gmltools-0.0.63/PKG-INFO
+-rw-rw-rw-   0        0        0      755 2023-03-09 09:37:42.000000 gmltools-0.0.63/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.055795 gmltools-0.0.63/dist/
+-rw-rw-rw-   0        0        0    74791 2023-04-14 10:52:54.000000 gmltools-0.0.63/dist/gmltools-0.0.59.tar.gz
+-rw-rw-rw-   0        0        0    17876 2023-03-16 08:30:12.000000 gmltools-0.0.63/gmltools.yml
+-rw-rw-rw-   0        0        0    17555 2023-03-06 11:09:12.000000 gmltools-0.0.63/mltools.yml
+-rw-rw-rw-   0        0        0      546 2023-05-13 10:12:29.000000 gmltools-0.0.63/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 10:13:14.403435 gmltools-0.0.63/setup.cfg
+-rw-rw-rw-   0        0        0     1682 2023-05-13 10:12:19.000000 gmltools-0.0.63/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:13.943063 gmltools-0.0.63/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.089362 gmltools-0.0.63/src/gmltools/
+-rw-rw-rw-   0        0        0      879 2023-03-14 15:28:10.000000 gmltools-0.0.63/src/gmltools/To_Do.txt
+-rw-rw-rw-   0        0        0      327 2023-03-08 11:50:28.000000 gmltools-0.0.63/src/gmltools/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.181881 gmltools-0.0.63/src/gmltools/eda/
+-rw-rw-rw-   0        0        0      327 2023-03-08 11:50:28.000000 gmltools-0.0.63/src/gmltools/eda/__init__.py
+-rw-rw-rw-   0        0        0    40126 2023-04-17 07:50:02.000000 gmltools-0.0.63/src/gmltools/eda/eda.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.288147 gmltools-0.0.63/src/gmltools/models/
+-rw-rw-rw-   0        0        0      327 2023-03-08 11:51:09.000000 gmltools-0.0.63/src/gmltools/models/__init__.py
+-rw-rw-rw-   0        0        0     4893 2023-03-13 11:20:44.000000 gmltools-0.0.63/src/gmltools/models/bayes.py
+-rw-rw-rw-   0        0        0     1983 2023-03-16 08:43:00.000000 gmltools-0.0.63/src/gmltools/models/custom_scorings.py
+-rw-rw-rw-   0        0        0     5143 2023-04-14 11:04:34.000000 gmltools-0.0.63/src/gmltools/models/dummy_model.py
+-rw-rw-rw-   0        0        0   119146 2023-05-13 10:11:58.000000 gmltools-0.0.63/src/gmltools/models/model.py
+-rw-rw-rw-   0        0        0     5803 2023-03-07 12:45:49.000000 gmltools-0.0.63/src/gmltools/models/models_info.py
+-rw-rw-rw-   0        0        0    13212 2023-05-12 09:20:42.000000 gmltools-0.0.63/src/gmltools/models/timeseriesplit.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.333257 gmltools-0.0.63/src/gmltools/models_analysis/
+-rw-rw-rw-   0        0        0      327 2023-03-08 11:50:54.000000 gmltools-0.0.63/src/gmltools/models_analysis/__init__.py
+-rw-rw-rw-   0        0        0    73636 2023-04-30 15:51:16.000000 gmltools-0.0.63/src/gmltools/models_analysis/classification_analysis.py
+-rw-rw-rw-   0        0        0     5653 2023-04-30 15:57:34.000000 gmltools-0.0.63/src/gmltools/models_analysis/xai.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.396121 gmltools-0.0.63/src/gmltools/preprocess/
+-rw-rw-rw-   0        0        0      327 2023-03-08 11:50:40.000000 gmltools-0.0.63/src/gmltools/preprocess/__init__.py
+-rw-rw-rw-   0        0        0    18728 2023-03-06 08:35:56.000000 gmltools-0.0.63/src/gmltools/preprocess/autoregressive_features.py
+-rw-rw-rw-   0        0        0     8133 2023-02-23 12:30:28.000000 gmltools-0.0.63/src/gmltools/preprocess/manage_holidays.py
+-rw-rw-rw-   0        0        0     4045 2023-03-30 08:41:18.000000 gmltools-0.0.63/src/gmltools/preprocess/preprocess.py
+drwxrwxrwx   0        0        0        0 2023-05-13 10:13:14.153269 gmltools-0.0.63/src/gmltools.egg-info/
+-rw-rw-rw-   0        0        0     1021 2023-05-13 10:13:13.000000 gmltools-0.0.63/src/gmltools.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      934 2023-05-13 10:13:13.000000 gmltools-0.0.63/src/gmltools.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 10:13:13.000000 gmltools-0.0.63/src/gmltools.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       82 2023-05-13 10:13:13.000000 gmltools-0.0.63/src/gmltools.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 10:13:13.000000 gmltools-0.0.63/src/gmltools.egg-info/top_level.txt
```

### Comparing `gmltools-0.0.62/LICENSE` & `gmltools-0.0.63/LICENSE`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/Models.ipynb` & `gmltools-0.0.63/Models.ipynb`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/PKG-INFO` & `gmltools-0.0.63/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gmltools
-Version: 0.0.62
+Version: 0.0.63
 Summary: Machine Learning library aiming for a higher level programming, organizing best tools
 Author: Diego Sanz-Gadea Sánchez
 Author-email: dsanzgadeasanchez@gmail.com
 Requires-Python: >=3.9,<4.0
 License-File: LICENSE
 
 # gmltools
```

### Comparing `gmltools-0.0.62/README.md` & `gmltools-0.0.63/README.md`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/dist/gmltools-0.0.59.tar.gz` & `gmltools-0.0.63/dist/gmltools-0.0.59.tar.gz`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/gmltools.yml` & `gmltools-0.0.63/gmltools.yml`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/mltools.yml` & `gmltools-0.0.63/mltools.yml`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/pyproject.toml` & `gmltools-0.0.63/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "gmltools"
-version = "0.0.62"
+version = "0.0.63"
 description = "Machine Learning library aiming for a higher level programming, organizing best tools"
 authors = ["Diego Sanz-Gadea Sánchez"]
 license = "GNU General Public License v3.0"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
```

### Comparing `gmltools-0.0.62/setup.py` & `gmltools-0.0.63/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 {'': ['*']}
 
 install_requires = \
 ['matplotlib>=3.6.3,<4.0.0', 'numpy>=1.21.6,<2.0.0', 'pandas>=1.5.0,<2.0.0', 'xgboost==1.5.0']
 
 setup_kwargs = {
     'name': 'gmltools',
-    'version': '0.0.62',
+    'version': '0.0.63',
     'description': 'Machine Learning library aiming for a higher level programming, organizing best tools',
     'long_description': '# gmltools\n\nMachine Learning library aiming for a higher level programming, organizing best tools\n\n```bash\n$ pip install gmltools\n```\n\n## Usage\n\n- TODO\n\n## Contributing\n\nInterested in contributing? Check out the contributing guidelines. Please note that this project is released with a Code of Conduct. By contributing to this project, you agree to abide by its terms.\n\n## License\n\n`gmltutils` was created by Diego Sanz-Gadea Sánchez. It is licensed under the terms of the GNU General Public License v3.0 license.\n\n## Credits\n\n`gmltutils` was created with [`cookiecutter`](https://cookiecutter.readthedocs.io/en/latest/) and the `py-pkgs-cookiecutter` [template](https://github.com/py-pkgs/py-pkgs-cookiecutter).\n',
     'author': 'Diego Sanz-Gadea Sánchez',
     'author_email': 'dsanzgadeasanchez@gmail.com',
     'maintainer': None,
     'maintainer_email': None,
     'url': None,
```

### Comparing `gmltools-0.0.62/src/gmltools/To_Do.txt` & `gmltools-0.0.63/src/gmltools/To_Do.txt`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/eda/eda.py` & `gmltools-0.0.63/src/gmltools/eda/eda.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models/bayes.py` & `gmltools-0.0.63/src/gmltools/models/bayes.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models/custom_scorings.py` & `gmltools-0.0.63/src/gmltools/models/custom_scorings.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models/dummy_model.py` & `gmltools-0.0.63/src/gmltools/models/dummy_model.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models/model.py` & `gmltools-0.0.63/src/gmltools/models/model.py`

 * *Files 0% similar despite different names*

```diff
@@ -1269,15 +1269,15 @@
                             grid_params={'XGB__n_estimators': [100, 200, 300, 400, 500],
                                 'XGB__max_depth': [3,5,7,10],
                                 'XGB__learning_rate': [0.01,0.05,0.1,0.15,0.2],
                                 'XGB__min_child_weight': [1,3,5,7],
                                 'XGB__gamma': [0.0,0.1,0.2,0.3,0.4],
                                 'XGB__colsample_bytree': [0.3,0.4,0.5,0.7]}, 
                             random_params=None, random_n_iter=10, bayes_pbounds=None, bayes_int_params=None,
-                            bayes_n_iter=30, sample_weight=None, random_state=None, n_jobs=-1,
+                            bayes_n_iter=30, sample_weight=None, random_state=None,verbosity=1, n_jobs=-1,
                             columns_lags=None, column_rolled_lags=None,lags=None,rolled_lags=None, rolled_metrics=None, column_rolled_lags_initial=None):
             
             """
             This method performs a XGBoost regression model with grid search or bayesian optimization.
     
             Parameters
             ----------
@@ -1348,15 +1348,15 @@
                 assert all('XGB__' in s for s in bayes_pbounds.keys()), "In case of bayesian optimization, bayes_pbounds must start with 'XGB__'"
                 assert all('XGB__' in s for s in bayes_int_params), "In case of bayesian optimization, bayes_int_params must start with 'XGB__'"
             
 
             #Preprocess the data automatically
             preprocessor=self._automatic_preprocessor(self.X_train,ordinal_cat_cols)
             pipe = Pipeline(steps=[('Prep', preprocessor),
-                                ('XGB', XGBRegressor(random_state=random_state,n_jobs=n_jobs))]) # Model always the last step
+                                ('XGB', XGBRegressor(random_state=random_state,n_jobs=n_jobs,verbosity=verbosity))]) # Model always the last step
             #Select Grid Search, Random Search or Bayesian Optimization
             select_searchcv=SelectSearchCV(self.X_train, self.y_train, pipe, scoring, sample_weight=sample_weight,cv=self.cv,n_jobs=n_jobs)
             select_searchcv.select_automatic(grid_params, random_params, random_n_iter, bayes_pbounds, bayes_int_params, bayes_n_iter)
             self.model=select_searchcv.fit(X_prev=self.X_prev, columns_lags=columns_lags, column_rolled_lags=column_rolled_lags,lags=lags,rolled_lags=rolled_lags, rolled_metrics=rolled_metrics, column_rolled_lags_initial=column_rolled_lags_initial)
             
             #generate a dictionary with all the parameters used in the model
             self._search_not_none_params = self._not_none_search(grid_params, random_params, random_n_iter, bayes_pbounds, bayes_int_params, bayes_n_iter)
```

### Comparing `gmltools-0.0.62/src/gmltools/models/models_info.py` & `gmltools-0.0.63/src/gmltools/models/models_info.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models/timeseriesplit.py` & `gmltools-0.0.63/src/gmltools/models/timeseriesplit.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models_analysis/classification_analysis.py` & `gmltools-0.0.63/src/gmltools/models_analysis/classification_analysis.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/models_analysis/xai.py` & `gmltools-0.0.63/src/gmltools/models_analysis/xai.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/preprocess/autoregressive_features.py` & `gmltools-0.0.63/src/gmltools/preprocess/autoregressive_features.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/preprocess/manage_holidays.py` & `gmltools-0.0.63/src/gmltools/preprocess/manage_holidays.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools/preprocess/preprocess.py` & `gmltools-0.0.63/src/gmltools/preprocess/preprocess.py`

 * *Files identical despite different names*

### Comparing `gmltools-0.0.62/src/gmltools.egg-info/PKG-INFO` & `gmltools-0.0.63/src/gmltools.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gmltools
-Version: 0.0.62
+Version: 0.0.63
 Summary: Machine Learning library aiming for a higher level programming, organizing best tools
 Author: Diego Sanz-Gadea Sánchez
 Author-email: dsanzgadeasanchez@gmail.com
 Requires-Python: >=3.9,<4.0
 License-File: LICENSE
 
 # gmltools
```

### Comparing `gmltools-0.0.62/src/gmltools.egg-info/SOURCES.txt` & `gmltools-0.0.63/src/gmltools.egg-info/SOURCES.txt`

 * *Files identical despite different names*

