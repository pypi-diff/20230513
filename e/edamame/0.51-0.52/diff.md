# Comparing `tmp/edamame-0.51.tar.gz` & `tmp/edamame-0.52.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "edamame-0.51.tar", last modified: Sat May  6 16:08:18 2023, max compression
+gzip compressed data, was "edamame-0.52.tar", last modified: Sat May 13 13:15:46 2023, max compression
```

## Comparing `edamame-0.51.tar` & `edamame-0.52.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.094311 edamame-0.51/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     1073 2022-11-30 14:22:32.000000 edamame-0.51/LICENSE
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    11935 2023-05-06 16:08:18.093775 edamame-0.51/PKG-INFO
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    10181 2023-05-06 16:05:55.000000 edamame-0.51/README.md
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.083884 edamame-0.51/edamame/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       21 2023-05-06 16:04:41.000000 edamame-0.51/edamame/__init__.py
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.088978 edamame-0.51/edamame/classifier/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      194 2023-05-04 19:56:56.000000 edamame-0.51/edamame/classifier/__init__.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    21566 2023-05-03 19:38:54.000000 edamame-0.51/edamame/classifier/classification.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     6106 2023-05-06 15:22:05.000000 edamame-0.51/edamame/classifier/diagnose.py
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.091110 edamame-0.51/edamame/eda/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      876 2023-05-06 16:04:28.000000 edamame-0.51/edamame/eda/__init__.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    32458 2023-03-25 15:28:28.000000 edamame-0.51/edamame/eda/eda.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     4460 2023-05-06 14:05:21.000000 edamame-0.51/edamame/eda/tools.py
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.093109 edamame-0.51/edamame/regressor/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      189 2023-04-06 20:53:01.000000 edamame-0.51/edamame/regressor/__init__.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     8347 2023-05-04 19:55:27.000000 edamame-0.51/edamame/regressor/diagnose.py
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    21361 2023-04-21 08:55:27.000000 edamame-0.51/edamame/regressor/regression.py
-drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-06 16:08:18.086734 edamame-0.51/edamame.egg-info/
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    11935 2023-05-06 16:08:18.000000 edamame-0.51/edamame.egg-info/PKG-INFO
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      461 2023-05-06 16:08:18.000000 edamame-0.51/edamame.egg-info/SOURCES.txt
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)        1 2023-05-06 16:08:18.000000 edamame-0.51/edamame.egg-info/dependency_links.txt
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       83 2023-05-06 16:08:18.000000 edamame-0.51/edamame.egg-info/requires.txt
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)        8 2023-05-06 16:08:18.000000 edamame-0.51/edamame.egg-info/top_level.txt
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      803 2023-05-06 16:04:37.000000 edamame-0.51/pyproject.toml
--rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       38 2023-05-06 16:08:18.094421 edamame-0.51/setup.cfg
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.075268 edamame-0.52/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     1073 2022-11-30 14:22:32.000000 edamame-0.52/LICENSE
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    11935 2023-05-13 13:15:46.074796 edamame-0.52/PKG-INFO
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    10181 2023-05-06 16:05:55.000000 edamame-0.52/README.md
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.066016 edamame-0.52/edamame/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       21 2023-05-13 12:08:29.000000 edamame-0.52/edamame/__init__.py
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.069674 edamame-0.52/edamame/classifier/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      194 2023-05-04 19:56:56.000000 edamame-0.52/edamame/classifier/__init__.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    22267 2023-05-13 12:08:26.000000 edamame-0.52/edamame/classifier/classification.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     6106 2023-05-06 15:22:05.000000 edamame-0.52/edamame/classifier/diagnose.py
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.072200 edamame-0.52/edamame/eda/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      876 2023-05-06 16:04:28.000000 edamame-0.52/edamame/eda/__init__.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    32458 2023-03-25 15:28:28.000000 edamame-0.52/edamame/eda/eda.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     4460 2023-05-06 14:05:21.000000 edamame-0.52/edamame/eda/tools.py
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.073908 edamame-0.52/edamame/regressor/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      189 2023-04-06 20:53:01.000000 edamame-0.52/edamame/regressor/__init__.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)     8347 2023-05-04 19:55:27.000000 edamame-0.52/edamame/regressor/diagnose.py
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    22034 2023-05-13 12:08:20.000000 edamame-0.52/edamame/regressor/regression.py
+drwxr-xr-x   0 marcosalvalaggio   (501) staff       (20)        0 2023-05-13 13:15:46.067921 edamame-0.52/edamame.egg-info/
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)    11935 2023-05-13 13:15:46.000000 edamame-0.52/edamame.egg-info/PKG-INFO
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      461 2023-05-13 13:15:46.000000 edamame-0.52/edamame.egg-info/SOURCES.txt
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)        1 2023-05-13 13:15:46.000000 edamame-0.52/edamame.egg-info/dependency_links.txt
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       83 2023-05-13 13:15:46.000000 edamame-0.52/edamame.egg-info/requires.txt
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)        8 2023-05-13 13:15:46.000000 edamame-0.52/edamame.egg-info/top_level.txt
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)      803 2023-05-13 12:08:12.000000 edamame-0.52/pyproject.toml
+-rw-r--r--   0 marcosalvalaggio   (501) staff       (20)       38 2023-05-13 13:15:46.075361 edamame-0.52/setup.cfg
```

### Comparing `edamame-0.51/LICENSE` & `edamame-0.52/LICENSE`

 * *Files identical despite different names*

### Comparing `edamame-0.51/PKG-INFO` & `edamame-0.52/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: edamame
-Version: 0.51
+Version: 0.52
 Summary: Exploratory data analysis tools
 Author-email: Marco Salvalaggio <mar.salvalaggio@gmail.com>
 License: Copyright (c) 2018 The Python Packaging Authority
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
         in the Software without restriction, including without limitation the rights
```

### Comparing `edamame-0.51/README.md` & `edamame-0.52/README.md`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/classifier/classification.py` & `edamame-0.52/edamame/classifier/classification.py`

 * *Files 4% similar despite different names*

```diff
@@ -66,158 +66,170 @@
         self.__knn_fit = {}
         self.__tree_fit = {}
         self.__random_forest_fit = {}
         self.__xgb_fit = {}
         self.__svm_fit = {}
 
 
-    def logistic(self) -> LogisticRegression:
+    def logistic(self, **kwargs) -> LogisticRegression:
         """
         Trains a logistic regression model using the training data and returns the fitted model.
 
+        Args:
+            **kwargs: Arbitrary keyword arguments to be passed to the `logistic` constructor.
+
         Returns:
             LogisticRegression: The trained logistic regression model.
 
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> logistic = classifier.logistic()
         """
-        logistic = LogisticRegression()
+        logistic = LogisticRegression(**kwargs)
         logistic.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__logistic_fit = logistic
         return self.__logistic_fit
 
 
-    def gaussian_nb(self) -> GaussianNB:
+    def gaussian_nb(self, **kwargs) -> GaussianNB:
         """
         Trains a Gaussian Naive Bayes classifier using the training data and returns the fitted model.
 
+        Args:
+            **kwargs: Arbitrary keyword arguments to be passed to the `Gaussian NB` constructor.
+
         Returns:
             GaussianNB: The trained Gaussian Naive Bayes classifier.
         
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> nb = classifier.gaussian_nb()
         """
-        gauss_nb = GaussianNB()
+        gauss_nb = GaussianNB(**kwargs)
         gauss_nb.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__gaussian_nb_fit = gauss_nb
         return self.__gaussian_nb_fit
 
 
     # ------------ #
     # KNN
     # ------------ #
-    def knn(self, n_neighbors: Tuple[int, int, int] = (1, 50, 50), n_folds: int = 5) -> KNeighborsClassifier:
+    def knn(self, n_neighbors: Tuple[int, int, int] = (1, 50, 50), n_folds: int = 5, **kwargs) -> KNeighborsClassifier:
         """
         Train a k-Nearest Neighbors classification model using the training data, and perform a grid search to find the
-        best value of 'n_neighbors' hyperparameter. 
+    best value of 'n_neighbors' hyperparameter. 
 
         Args:
             n_neighbors (Tuple[int, int, int]): A tuple with three integers. The first and second integers are the range of the 
                 'n_neighbors' hyperparameter that will be searched by the grid search, and the third integer is the 
                 number of values to generate in the interval [n_neighbors[0], n_neighbors[1]]. Default is [1, 50, 50].
             n_folds (int): The number of cross-validation folds to use for the grid search. Default is 5.
+            **kwargs: Arbitrary keyword arguments to be passed to the `KNN` constructor.
+
 
         Returns:
             KNeighborsClassifier: The trained k-Nearest Neighbors classification model with the best 'n_neighbors' 
                 hyperparameter found by the grid search. 
         
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> knn = classifier.knn(n_neighbors=(1,50,50), n_folds=3) 
         """
         n_n = np.linspace(n_neighbors[0], n_neighbors[1], n_neighbors[2]).astype(np.int32)
-        knn = KNeighborsClassifier()
+        knn = KNeighborsClassifier(**kwargs)
         tuned_parameters = [{"n_neighbors": n_n}]
         grid_knn = GridSearchCV(knn, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='accuracy')
         grid_knn.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__knn_fit = grid_knn.best_estimator_
         return self.__knn_fit
 
 
-    def tree(self, alpha: Tuple[float, float, int] = (0., 0.001, 5), impurity: Tuple[float, float, int] = (0., 0.00001, 5), n_folds: int = 5) -> DecisionTreeClassifier:
+    def tree(self, alpha: Tuple[float, float, int] = (0., 0.001, 5), impurity: Tuple[float, float, int] = (0., 0.00001, 5), n_folds: int = 5, **kwargs) -> DecisionTreeClassifier:
         """
         Trains a decision tree classifier using the training data and returns the fitted model.
     
         Args:
             alpha (Tuple[float, float, int]): A tuple containing the minimum and maximum values of ccp_alpha and the number of values to try (default: (0., 0.001, 5)).
             impurity (Tuple[float, float, int]): A tuple containing the minimum and maximum values of min_impurity_decrease and the number of values to try (default: (0., 0.00001, 5)).
             n_folds (int): The number of cross-validation folds to use for grid search (default: 5).
+            **kwargs: Arbitrary keyword arguments to be passed to the `tree` constructor.
+
 
         Returns:
             DecisionTreeClassifier: The trained decision tree classifier model.
 
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> tree = classifier.tree(alpha=(0., 0.001, 5), impurity=(0., 0.00001, 5), n_folds=3) 
         """
         alphas = np.linspace(alpha[0], alpha[1], alpha[2])
         impurities = np.linspace(impurity[0], impurity[1], impurity[2])
         tuned_parameters = [{"ccp_alpha": alphas, 'min_impurity_decrease': impurities}]
-        tree = DecisionTreeClassifier() 
+        tree = DecisionTreeClassifier(**kwargs) 
         grid_tree = GridSearchCV(tree, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='accuracy')
         grid_tree.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__tree_fit = grid_tree.best_estimator_
         return self.__tree_fit
 
 
-    def random_forest(self, n_estimators: Tuple[int, int, int] = (50, 1000, 5), n_folds: int = 2) -> RandomForestClassifier:
+    def random_forest(self, n_estimators: Tuple[int, int, int] = (50, 1000, 5), n_folds: int = 2, **kwargs) -> RandomForestClassifier:
         """
         Train a Random Forest classifier using the training data and return the fitted model.
 
         Args:
             n_estimators (Tuple[int, int, int]): The range of the number of trees in the forest. Default is (50, 1000, 5).
             n_folds (int): The number of folds in cross-validation. Default is 2.
+            **kwargs: Arbitrary keyword arguments to be passed to the `random forest` constructor.
 
         Returns:
             RandomForestClassifier: The trained Random Forest classifier.
 
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> rf = classifier.random_forest(n_estimators=(50, 1000, 5), n_folds=2) 
         """
         n_estimators = np.linspace(n_estimators[0], n_estimators[1], n_estimators[2]).astype(np.int16)
         tuned_parameters = [{"n_estimators": n_estimators}]
-        random_forest = RandomForestClassifier(warm_start=True, n_jobs=-1)
+        random_forest = RandomForestClassifier(warm_start=True, n_jobs=-1, **kwargs)
         grid_random_forest = GridSearchCV(random_forest, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='accuracy')
         grid_random_forest.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__random_forest_fit = grid_random_forest.best_estimator_
         return self.__random_forest_fit
 
 
-    def xgboost(self, n_estimators: Tuple[int, int, int] = (10, 100, 5), n_folds: int = 2) -> XGBClassifier:
+    def xgboost(self, n_estimators: Tuple[int, int, int] = (10, 100, 5), n_folds: int = 2, **kwargs) -> XGBClassifier:
         """
         Train an XGBoost classifier using the training data and return the fitted model.
 
         Args:
             n_estimators (Tuple[int, int, int]): The range of the number of boosting rounds. Default is (10, 100, 5).
             n_folds (int): The number of folds in cross-validation. Default is 2.
+            **kwargs: Arbitrary keyword arguments to be passed to the `xgboost` constructor.
 
         Returns:
             XGBClassifier: The trained XGBoost classifier.
 
         Example:
             >>> from edamame.classifier import TrainClassifier
             >>> classifier = TrainClassifier(X_train=X_train, y_train=y_train, X_test=X_test, y_test=y_test)
             >>> xgboost = classifier.xgboost(n_estimators=(10, 100, 5), n_folds=2) 
         """
         n_est = np.linspace(n_estimators[0], n_estimators[1], n_estimators[2]).astype(np.int16)
         tuned_parameters = {"n_estimators": n_est}
-        xgb_m = XGBClassifier()
+        xgb_m = XGBClassifier(**kwargs)
         grid_xgb = GridSearchCV(xgb_m, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='accuracy')
         grid_xgb.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__xgb_fit = grid_xgb.best_estimator_
         return self.__xgb_fit
     
 
@@ -437,8 +449,8 @@
     y_pred = model.predict(X)
     title = f'#### Model metrics:'
     display(Markdown(title))
     sns.heatmap(confusion_matrix(y, y_pred), annot=True, fmt="2.0f")
     plt.show()
     print(classification_report(y, y_pred))
 
-        
+
```

### Comparing `edamame-0.51/edamame/classifier/diagnose.py` & `edamame-0.52/edamame/classifier/diagnose.py`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/eda/__init__.py` & `edamame-0.52/edamame/eda/__init__.py`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/eda/eda.py` & `edamame-0.52/edamame/eda/eda.py`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/eda/tools.py` & `edamame-0.52/edamame/eda/tools.py`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/regressor/diagnose.py` & `edamame-0.52/edamame/regressor/diagnose.py`

 * *Files identical despite different names*

### Comparing `edamame-0.51/edamame/regressor/regression.py` & `edamame-0.52/edamame/regressor/regression.py`

 * *Files 6% similar despite different names*

```diff
@@ -64,172 +64,180 @@
         self.__lasso_fit = {}
         self.__ridge_fit = {}
         self.__tree_fit = {}
         self.__random_forest_fit = {}
         self.__xgb_fit = {}
 
 
-    def linear(self) -> LinearRegression:
+    def linear(self, **kwargs) -> LinearRegression:
         """
         Train a linear regression model using the training data and return the fitted model.
 
+        Args: 
+            **kwargs: Arbitrary keyword arguments to be passed to the `linear` constructor.
+
         Returns:
             LinearRegression: The trained linear regression model.
-        
-        Example:
+
+    Example:
             >>> from edamame.regressor import TrainRegressor
             >>> regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
             >>> linear = regressor.linear()
         """
-        linear = LinearRegression()
+        linear = LinearRegression(**kwargs)
         linear.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__linear_fit = linear
         # return step 
         return self.__linear_fit
 
 
-    def lasso(self, alpha: Tuple[float, float, int] = (0.0001, 10., 50), n_folds: int = 5) -> Lasso:
+    def lasso(self, alpha: Tuple[float, float, int] = (0.0001, 10., 50), n_folds: int = 5, **kwargs) -> Lasso:
         """
         Train a Lasso regression model using the training data and return the fitted model.
 
         Args:
             alpha (Tuple[float, float, int]): The range of alpha values to test for hyperparameter tuning. Default is (0.0001, 10., 50).
             n_folds (int): The number of cross-validation folds to use for hyperparameter tuning. Default is 5.
+            **kwargs: Arbitrary keyword arguments to be passed to the `lasso` constructor.
 
         Returns:
             Lasso: The trained Lasso regression model.
 
         Example:
             >>> from edamame.regressor import TrainRegressor
             >>> regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
             >>> lasso = regressor.lasso(alpha=(0.0001, 10., 50), n_folds=5)
         """
         # lasso hyperparameter 
         alphas = np.linspace(alpha[0], alpha[1], alpha[2])
         # hyperparameter gridsearch
-        lasso = Lasso()
+        lasso = Lasso(**kwargs)
         tuned_parameters = [{"alpha": alphas}]
         reg_lasso = GridSearchCV(lasso, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='r2')
         reg_lasso.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__lasso_fit = reg_lasso.best_estimator_
         # return step 
         return self.__lasso_fit
 
 
-    def ridge(self, alpha: Tuple[float, float, int] = (0.1, 50., 50), n_folds: int = 5) -> Ridge:
+    def ridge(self, alpha: Tuple[float, float, int] = (0.1, 50., 50), n_folds: int = 5, **kwargs) -> Ridge:
         """
         Train a Ridge regression model using the training data and return the fitted model.
 
         Args:
             alpha (Tuple[float, float, int]): The range of alpha values to test for hyperparameter tuning. Default is (0.1, 50, 50).
             n_folds (int): The number of cross-validation folds to use for hyperparameter tuning. Default is 5.
+            **kwargs: Arbitrary keyword arguments to be passed to the `ridge` constructor.
 
         Returns:
             Ridge: The trained Ridge regression model.
 
         Example:
             >>> from edamame.regressor import TrainRegressor
             >>> regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
             >>> ridge = regressor.ridge(alpha=((0.1, 50., 50), n_folds=5)
         """
         # ridge hyperparameter 
         alphas = np.linspace(alpha[0], alpha[1], alpha[2])
         # hyperparameter gridsearch
-        ridge = Ridge()
+        ridge = Ridge(**kwargs)
         tuned_parameters = [{"alpha": alphas}]
         reg_ridge = GridSearchCV(ridge, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='r2')
         reg_ridge.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__ridge_fit = reg_ridge.best_estimator_
         # return step 
         return self.__ridge_fit
     
     
     def tree(self, alpha: Tuple[float, float, int] = (0., 0.001, 5), impurity: Tuple[float, float, int] = (0., 0.00001, 5),
-            n_folds: int = 5) -> DecisionTreeRegressor:
+            n_folds: int = 5, **kwargs) -> DecisionTreeRegressor:
         """
         Fits a decision tree regression model using the provided training data and hyperparameters.
 
         Args:
             alpha (Tuple[float, float, int]): A tuple specifying the range of values to use for the ccp_alpha 
                 hyperparameter. The range is given as a tuple (start, stop, num), where `start` is the start
                 of the range, `stop` is the end of the range, and `num` is the number of values to generate
                 within the range. Defaults to (0., 0.001, 5).
             impurity (Tuple[float, float, int]): A tuple specifying the range of values to use for the 
                 min_impurity_decrease hyperparameter. The range is given as a tuple (start, stop, num), where 
                 `start` is the start of the range, `stop` is the end of the range, and `num` is the number of 
                 values to generate within the range. Defaults to (0., 0.00001, 5).
             n_folds (int): The number of folds to use for cross-validation. Defaults to 5.
+            **kwargs: Arbitrary keyword arguments to be passed to the `tree` constructor.
 
         Returns:
             DecisionTreeRegressor: The fitted decision tree regressor model.
 
         Example:
             >>> from edamame.regressor import TrainRegressor
             >>> regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
             >>> tree = regressor.tree(alpha=(0., 0.001, 5), impurity=(0., 0.00001, 5), n_folds=3)
         """
         # hyperparameters gridsearch
         alphas = np.linspace(alpha[0], alpha[1], alpha[2])
         impurities = np.linspace(impurity[0], impurity[1], impurity[2])
         tuned_parameters = [{"ccp_alpha": alphas, 'min_impurity_decrease': impurities}]
-        tree = DecisionTreeRegressor() 
+        tree = DecisionTreeRegressor(**kwargs) 
         reg_tree = GridSearchCV(tree, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='r2')
         reg_tree.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__tree_fit = reg_tree.best_estimator_
         # return step 
         return self.__tree_fit
 
 
-    def random_forest(self, n_estimators: Tuple[int, int, int] = (50, 1000, 5), n_folds: int = 2) -> RandomForestRegressor:
+    def random_forest(self, n_estimators: Tuple[int, int, int] = (50, 1000, 5), n_folds: int = 2, **kwargs) -> RandomForestRegressor:
         """
         Trains a Random Forest regression model on the training data and returns the best estimator found by GridSearchCV.
 
         Args:
             n_estimators (Tuple[int, int, int]): A tuple of integers specifying the minimum and maximum number of trees
                 to include in the forest, and the step size between them.
             n_folds (int): The number of cross-validation folds to use when evaluating models.
+            **kwargs: Arbitrary keyword arguments to be passed to the `random forest` constructor.
 
         Returns:
             RandomForestRegressor: The best Random Forest model found by GridSearchCV.
         """
         n_estimators = np.linspace(n_estimators[0], n_estimators[1], n_estimators[2]).astype(np.int16)
         tuned_parameters = [{"n_estimators": n_estimators}]
-        random_forest = RandomForestRegressor(warm_start=True, n_jobs=-1)
+        random_forest = RandomForestRegressor(warm_start=True, n_jobs=-1, **kwargs)
         reg_random_forest = GridSearchCV(random_forest, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='r2')
         reg_random_forest.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__random_forest_fit = reg_random_forest.best_estimator_
         # return step 
         return self.__random_forest_fit
 
 
-    def xgboost(self, n_estimators: Tuple[int, int, int] = (10, 100, 5), n_folds: int = 2) -> xgb.XGBRegressor:
+    def xgboost(self, n_estimators: Tuple[int, int, int] = (10, 100, 5), n_folds: int = 2, **kwargs) -> xgb.XGBRegressor:
         """
         Trains an XGBoost model using the specified hyperparameters.
 
         Args:
             n_estimators (Tuple[int, int, int]): A tuple containing the start, end and step values for number of estimators.
                 Default is (10, 100, 5).
             n_folds (int): The number of folds to use in the cross-validation process. Default is 2.
+            **kwargs: Arbitrary keyword arguments to be passed to the `xgboost` constructor.
 
         Returns:
             xgb.XGBRegressor: The trained XGBoost model.
 
         Example:
             >>> from edamame.regressor import TrainRegressor
             >>> regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
             >>> xgboost = regressor.xgboost(n_estimators=(10, 200, 10), n_folds=5)
         """
         n_est = np.linspace(n_estimators[0], n_estimators[1], n_estimators[2]).astype(np.int16)
         tuned_parameters = {"n_estimators": n_est}
-        xgb_m = xgb.XGBRegressor(objective ='reg:squarederror')
+        xgb_m = xgb.XGBRegressor(objective ='reg:squarederror', **kwargs)
         reg_xgb = GridSearchCV(xgb_m, tuned_parameters, cv=n_folds, refit=True, verbose=0, scoring='r2')
         reg_xgb.fit(self.X_train, self.y_train.squeeze())
         # save the model in the instance attributes
         self.__xgb_fit = reg_xgb.best_estimator_
         # return step 
         return self.__xgb_fit
 
@@ -443,8 +451,8 @@
     X = pd.read_csv('/Users/marcosalvalaggio/code/python/ds/data/melb_data/X.csv', sep = ';')
     y = pd.read_csv('/Users/marcosalvalaggio/code/python/ds/data/melb_data/y.csv', sep = ';')
     X_train, X_test, y_train, y_test = setup(X, y)
     regressor = TrainRegressor(X_train, np.log(y_train), X_test, np.log(y_test))
     regressor.linear()
     model_list = regressor.auto_ml()
     regressor.model_metrics()
-    regressor.save_model()
+    regressor.save_model()
```

### Comparing `edamame-0.51/edamame.egg-info/PKG-INFO` & `edamame-0.52/edamame.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: edamame
-Version: 0.51
+Version: 0.52
 Summary: Exploratory data analysis tools
 Author-email: Marco Salvalaggio <mar.salvalaggio@gmail.com>
 License: Copyright (c) 2018 The Python Packaging Authority
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
         in the Software without restriction, including without limitation the rights
```

### Comparing `edamame-0.51/pyproject.toml` & `edamame-0.52/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "edamame"
-version = "0.51"
+version = "0.52"
 authors = [
   { name="Marco Salvalaggio", email="mar.salvalaggio@gmail.com" },
 ]
 description = "Exploratory data analysis tools"
 readme = "README.md"
 license = { file="LICENSE" }
 requires-python = ">=3.7"
```

