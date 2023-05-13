# Comparing `tmp/auptitcafe-0.1.6.tar.gz` & `tmp/auptitcafe-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "auptitcafe-0.1.6.tar", max compression
+gzip compressed data, was "auptitcafe-0.1.7.tar", max compression
```

## Comparing `auptitcafe-0.1.6.tar` & `auptitcafe-0.1.7.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0      703 2023-05-11 10:11:14.145038 auptitcafe-0.1.6/README.md
--rw-r--r--   0        0        0        0 2023-05-11 10:11:51.953313 auptitcafe-0.1.6/auptitcafe/__init__.py
--rw-r--r--   0        0        0     2280 2023-05-11 10:11:14.145038 auptitcafe-0.1.6/auptitcafe/menus.py
--rw-r--r--   0        0        0      502 2023-05-11 10:11:14.145038 auptitcafe-0.1.6/auptitcafe/plat.py
--rw-r--r--   0        0        0      443 2023-05-11 10:11:14.145038 auptitcafe-0.1.6/pyproject.toml
--rw-r--r--   0        0        0     1193 1970-01-01 00:00:00.000000 auptitcafe-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0      703 2023-05-13 06:57:43.061927 auptitcafe-0.1.7/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 06:58:27.626995 auptitcafe-0.1.7/auptitcafe/__init__.py
+-rw-r--r--   0        0        0     2288 2023-05-13 06:57:43.061927 auptitcafe-0.1.7/auptitcafe/menus.py
+-rw-r--r--   0        0        0      503 2023-05-13 06:57:43.061927 auptitcafe-0.1.7/auptitcafe/plat.py
+-rw-r--r--   0        0        0      443 2023-05-13 06:57:43.061927 auptitcafe-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     1193 1970-01-01 00:00:00.000000 auptitcafe-0.1.7/PKG-INFO
```

### Comparing `auptitcafe-0.1.6/README.md` & `auptitcafe-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `auptitcafe-0.1.6/auptitcafe/menus.py` & `auptitcafe-0.1.7/auptitcafe/menus.py`

 * *Files 3% similar despite different names*

```diff
@@ -12,44 +12,44 @@
 
 
     def get_all(self):
         out = []
         response = requests.get(self.menus_url )
         soup = BeautifulSoup(response.text, 'html.parser')
         title = soup.find('h2', class_='elementor-heading-title elementor-size-default')
-        print('title : <' + title.text.strip() + '>')
+        #print('title : <' + title.text.strip() + '>')
         # Plats
 
         menus = soup.find_all('div', class_='col-sm-6 col-md-6 mb-4 selfer-contact-info')
 
         for menu in menus:
             name = menu.find('h5').text.strip()
             image = menu.find('img')['src']
             recette = menu.find('div').text.strip()
-            print('name : <' + name + '>')
+            #print('name : <' + name + '>')
             titre_plat = name.split("-")[0].strip()
-            print('Titre plat : <' + titre_plat + '>')
-            print('url image : <' + image + '>')
-            print('recette : <' + recette + '>')
+            #print('Titre plat : <' + titre_plat + '>')
+            #print('url image : <' + image + '>')
+            #print('recette : <' + recette + '>')
             #image_url = menu.find('img')['src']
             #print(name + " : " + image_url)
             numbers = [int(s) for s in re.findall(r'\d+\.\d+|\d+', name)]
-            print('Prix : <' + str(numbers[0]) + '>')
+            #print('Prix : <' + str(numbers[0]) + '>')
             prix = numbers[0]
             if prix < 1500:
                 category = 'DESSERT'
             else:
                 category = 'PLAT'
-            print("Catgory : <" + category + '>')
+            #print("Catgory : <" + category + '>')
             plat = Plat(title = titre_plat,
                         price = prix,
                         cat = category,
                         details = recette,
                         img_url = image)
-            print("================================================================")
+            #print("================================================================")
             out.append(plat)
         return out
     
     def to_csv(self, csv_filename='menus.csv', header=True):
         menu_instance = Menus()
         plats = []
         plats = menu_instance.get_all()
```

### Comparing `auptitcafe-0.1.6/PKG-INFO` & `auptitcafe-0.1.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: auptitcafe
-Version: 0.1.6
+Version: 0.1.7
 Summary: SDK pour interagir avec http://auptitcafe.nc/menu/
 Author: Adrien SALES
 Author-email: Adrien.Sales@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

