# Comparing `tmp/BlueBrain-0.1.1.tar.gz` & `tmp/BlueBrain-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BlueBrain-0.1.1.tar", last modified: Wed May  3 15:55:06 2023, max compression
+gzip compressed data, was "BlueBrain-0.1.2.tar", last modified: Sat May 13 12:32:26 2023, max compression
```

## Comparing `BlueBrain-0.1.1.tar` & `BlueBrain-0.1.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-05-03 15:55:06.962013 BlueBrain-0.1.1/
-drwxrwxrwx   0        0        0        0 2023-05-03 15:55:06.955013 BlueBrain-0.1.1/BlueBrain/
--rw-rw-rw-   0        0        0     9533 2023-05-03 15:54:07.000000 BlueBrain-0.1.1/BlueBrain/AITONeuralNetwork.py
--rw-rw-rw-   0        0        0       49 2023-05-03 15:50:51.000000 BlueBrain-0.1.1/BlueBrain/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-03 15:55:06.961017 BlueBrain-0.1.1/BlueBrain.egg-info/
--rw-rw-rw-   0        0        0      748 2023-05-03 15:55:06.000000 BlueBrain-0.1.1/BlueBrain.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      225 2023-05-03 15:55:06.000000 BlueBrain-0.1.1/BlueBrain.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-03 15:55:06.000000 BlueBrain-0.1.1/BlueBrain.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       19 2023-05-03 15:55:06.000000 BlueBrain-0.1.1/BlueBrain.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-05-03 15:55:06.000000 BlueBrain-0.1.1/BlueBrain.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      748 2023-05-03 15:55:06.962013 BlueBrain-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0       42 2023-05-03 15:55:06.962013 BlueBrain-0.1.1/setup.cfg
--rw-rw-rw-   0        0        0     1058 2023-05-03 15:52:55.000000 BlueBrain-0.1.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:32:26.769075 BlueBrain-0.1.2/
+drwxrwxrwx   0        0        0        0 2023-05-13 12:32:26.751086 BlueBrain-0.1.2/BlueBrain/
+-rw-rw-rw-   0        0        0     9346 2023-05-13 12:27:27.000000 BlueBrain-0.1.2/BlueBrain/NeuralNetwork.py
+-rw-rw-rw-   0        0        0       49 2023-05-03 15:50:51.000000 BlueBrain-0.1.2/BlueBrain/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 12:32:26.768108 BlueBrain-0.1.2/BlueBrain.egg-info/
+-rw-rw-rw-   0        0        0      748 2023-05-13 12:32:26.000000 BlueBrain-0.1.2/BlueBrain.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      221 2023-05-13 12:32:26.000000 BlueBrain-0.1.2/BlueBrain.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 12:32:26.000000 BlueBrain-0.1.2/BlueBrain.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       19 2023-05-13 12:32:26.000000 BlueBrain-0.1.2/BlueBrain.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-05-13 12:32:26.000000 BlueBrain-0.1.2/BlueBrain.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      748 2023-05-13 12:32:26.769075 BlueBrain-0.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0       42 2023-05-13 12:32:26.769075 BlueBrain-0.1.2/setup.cfg
+-rw-rw-rw-   0        0        0     1058 2023-05-13 12:31:42.000000 BlueBrain-0.1.2/setup.py
```

### Comparing `BlueBrain-0.1.1/BlueBrain/AITONeuralNetwork.py` & `BlueBrain-0.1.2/BlueBrain/NeuralNetwork.py`

 * *Files 10% similar despite different names*

```diff
@@ -19,84 +19,108 @@
     block = int(round(barLength * progress))
     text = "\r[{}] {:.0f}% {}".format(
         "#" * block + "-" * (barLength - block), round(progress * 100, 0),
         status)
     sys.stdout.write(text)
     sys.stdout.flush()
 
+
 def sigmoid_function(x):
     return 1 / (1 + e * (1 / x))
 
 
-class AITONeuralNetwork:
-    generation_weight = []
-
+class NeuralNetwork:
+    # Setting neural network values.
     def __init__(self, input_layer_size, secret_layer_size, secret_layer_count, generation_count):
         self.secret_layer_count = secret_layer_count
         self.secret_layer_size = secret_layer_size
         self.input_layer_size = input_layer_size
         self.network_weight = []
         self.generation_count = generation_count
         self.generation_weight = secret_layer_size * secret_layer_size * (
                 secret_layer_count - 1) + input_layer_size * secret_layer_size
         self.model_path = os.getcwd()
 
+    # create network weights and prepare training data
     def set_up(self):
         self.create_network_weight()
         self.split_data()
 
+    # load saved model from folder
     def load_model(self, path=None):
-
-        if path is None:
-            with open('AITO.dat', 'rb') as f:
-                self = pickle.load(f)
-                return self
         with open(path, 'rb') as f:
             self = pickle.load(f)
             return self
 
+    # save trained model on folder.
     def save_model(self, path=None):
-
         if path is None:
             with open('../Models/AITO.dat', 'wb') as f:
                 pickle.dump(self, f)
-
         else:
             with open(path, 'wb') as f:
                 pickle.dump(self, f)
 
+    # create network weight for training model.
     def create_network_weight(self):
         for generation in range(self.generation_count):
             self.network_weight.append([])
             for i in range(self.generation_weight):
                 self.network_weight[generation].append(round(random.uniform(-1.0, 1.0),
                                                              5) / 50)
 
-    def split_data(self):
-        for generation in range(self.generation_count):
-            temp_list = [[]]
-            for k in self.network_weight[generation]:
-                last_param = len(temp_list[len(temp_list) - 1])
-                if last_param == self.secret_layer_size:
-                    temp_list.append([])
-                temp_list[len(temp_list) - 1].append(k)
-            self.network_weight[generation] = temp_list.copy()
-
+    # generate new weights to compare old weights.
     def create_new_weights(self):
         new_data = []
         for i in range(len(self.network_weight)):
             new_data.append([])
             for j in range(len(self.network_weight[i])):
                 new_data[i].append([])
                 for t in range(len(self.network_weight[i][j])):
                     new_data[i][j].append(self.network_weight[i][j][t] + round(random.uniform(-1.0, 1.0),
                                                                                5) / 100)
 
         return new_data
 
+    # parse train data for train ML model.
+    def split_data(self):
+        for generation in range(self.generation_count):
+            temp_list = [[]]
+            for k in self.network_weight[generation]:
+                last_param = len(temp_list[len(temp_list) - 1])
+                if last_param == self.secret_layer_size:
+                    temp_list.append([])
+                temp_list[len(temp_list) - 1].append(k)
+            self.network_weight[generation] = temp_list.copy()
+
+    # predict a estimation according to ML model.
+    def predict(self, input_x):
+        if self.inputIsNotValid(input_x):
+            print('\033[1;31m' + "Invalid input, shape of data doesn't fit model.")
+            print('\033[1;31m' + "Check predict function.")
+            return []
+        t = 0
+
+        y = (np.dot(input_x, self.network_weight[0][0:self.input_layer_size]))
+
+        index = 0
+        for j in range(len(self.network_weight[0])):
+
+            if j == self.input_layer_size + index * self.secret_layer_size:
+                y = (
+                    np.dot(
+                        y,
+                        self.network_weight[0][
+                        self.input_layer_size + self.secret_layer_size * index: self.input_layer_size + self.secret_layer_size * index + self.secret_layer_size]))
+                index = index + 1
+                t = t + 1
+
+        return y
+
+    #
     def predict_with_current_weight(self, input_x, current_y):
 
         for i in range(self.generation_count):
             t = 0
             for x in input_x:
                 if len(current_y[i]) < len(input_x):
                     current_y[i].append([])
@@ -112,34 +136,35 @@
                                 self.input_layer_size + self.secret_layer_size * index: self.input_layer_size + self.secret_layer_size * index + self.secret_layer_size]))
                         index = index + 1
                 t = t + 1
         return current_y
 
     # *--------------------------------------------------------------------------------------------------------------*
 
-    def predict_with_new_weight(self, input_x, new_y, new_weights):
-
+    def predict_for_Training(self, input_x, new_y, new_weights):
+        y = []
         for i in range(self.generation_count):
             t = 0
+            y.append([])
             for x in input_x:
-                if len(new_y[i]) < len(input_x):
-                    new_y[i].append([])
-                new_y[i][t] = (np.dot(x, new_weights[i][0:self.input_layer_size]))
+                # if len(y[i]) < len(input_x):
+                y[i].append([])
+                y[i][t] = (np.dot(x, new_weights[i][0:self.input_layer_size]))
 
                 index = 0
                 for j in range(len(new_weights[i])):
                     if j == self.input_layer_size + index * self.secret_layer_size:
-                        new_y[i][t] = (
+                        y[i][t] = (
                             np.dot(
-                                new_y[i][t],
+                                y[i][t],
                                 new_weights[i][
                                 self.input_layer_size + self.secret_layer_size * index: self.input_layer_size + self.secret_layer_size * index + self.secret_layer_size]))
                         index = index + 1
                 t = t + 1
-        return new_y
+        return y
 
     def generate_new_population(self, output_y, current_result):
 
         total_current = []
         for i in range(self.generation_count):
             total_current.append([0])
 
@@ -184,62 +209,33 @@
             current_y.append([])
             new_y.append([])
 
         for generation in range(genetic_iteration):
             for rep in range(iteration):
                 updt(iteration * genetic_iteration, (generation * rep + rep))
 
-                # print("================================== Generation: " + str(generation + 1) + " Iteration : " + str(
-                #     int(rep + 1)) +  " =======================================")
-                # print(
-                #     "- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -")
                 new_weights = self.create_new_weights()
 
-                current_result = self.predict_with_current_weight(input_x, current_y)
+                current_result = self.predict_for_Training(input_x, current_y,self.network_weight)
 
-                new_result = self.predict_with_new_weight(input_x, new_y, new_weights)
+                new_result = self.predict_for_Training(input_x, new_y, new_weights)
 
                 # find best network weight on self.network_weight generations
                 self.comparing_weights(current_result, new_result, output_y, new_weights)
 
             self.generate_new_population(output_y, current_result)
 
-    def predict(self, input_x):
-        if self.inputIsNotValid(input_x):
-            print('\033[1;31m' + "Invalid input, shape of data doesn't fit model.")
-            print('\033[1;31m' + "Check predict function.")
-            return []
-        y = []
-
-        t = 0
-
-        y = (np.dot(input_x, self.network_weight[0][0:self.input_layer_size]))
 
-        index = 0
-        for j in range(len(self.network_weight[0])):
-
-            if j == self.input_layer_size + index * self.secret_layer_size:
-                y = (
-                    np.dot(
-                        y,
-                        self.network_weight[0][
-                        self.input_layer_size + self.secret_layer_size * index: self.input_layer_size + self.secret_layer_size * index + self.secret_layer_size]))
-                index = index + 1
-                t = t + 1
-
-        return y
 
     def inputIsNotValid(self, input_x):
 
         if type(input_x[0]) is int:
             if self.input_layer_size != len(input_x):
                 return True
             return False
 
         else:
 
             if self.input_layer_size != len(input_x[0]):
                 return True
             return False
 
-
-print("everything is okey")
```

### Comparing `BlueBrain-0.1.1/BlueBrain.egg-info/PKG-INFO` & `BlueBrain-0.1.2/BlueBrain.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BlueBrain
-Version: 0.1.1
+Version: 0.1.2
 Summary: Special AI/ML library for autonomous vehicles and underwater systems
 Home-page: UNKNOWN
 Author: Uranyum (Mustafa Gülsoy)
 Author-email: <mustafagulsoy05@gmail.com>
 License: UNKNOWN
 Keywords: python,AI,ML,BlueBrain,Self-Drive
 Platform: UNKNOWN
```

### Comparing `BlueBrain-0.1.1/PKG-INFO` & `BlueBrain-0.1.2/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BlueBrain
-Version: 0.1.1
+Version: 0.1.2
 Summary: Special AI/ML library for autonomous vehicles and underwater systems
 Home-page: UNKNOWN
 Author: Uranyum (Mustafa Gülsoy)
 Author-email: <mustafagulsoy05@gmail.com>
 License: UNKNOWN
 Keywords: python,AI,ML,BlueBrain,Self-Drive
 Platform: UNKNOWN
```

### Comparing `BlueBrain-0.1.1/setup.py` & `BlueBrain-0.1.2/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 import codecs
 import os
 
 
-VERSION = '0.1.1'
+VERSION = '0.1.2'
 DESCRIPTION = 'Special AI/ML library for autonomous vehicles and underwater systems'
 LONG_DESCRIPTION = 'A package that allows to build AI/ML models for manage self-driving cars' \
                    ' and images processing tools.'
 
 # Setting up
 setup(
     name="BlueBrain",
```

