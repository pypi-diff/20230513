# Comparing `tmp/websiteclassificationapi-2.1.9.tar.gz` & `tmp/websiteclassificationapi-2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\websiteclassificationapi-2.1.9.tar", last modified: Sat Oct 15 12:33:00 2022, max compression
+gzip compressed data, was "dist\websiteclassificationapi-2.2.tar", last modified: Sat May 13 14:41:24 2023, max compression
```

## Comparing `websiteclassificationapi-2.1.9.tar` & `websiteclassificationapi-2.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/
--rw-rw-rw-   0        0        0    11766 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/PKG-INFO
--rw-rw-rw-   0        0        0     9029 2022-10-15 12:29:24.000000 websiteclassificationapi-2.1.9/README.md
--rw-rw-rw-   0        0        0       42 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/setup.cfg
--rw-rw-rw-   0        0        0     1381 2022-10-15 12:32:51.000000 websiteclassificationapi-2.1.9/setup.py
-drwxrwxrwx   0        0        0        0 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/test/
--rw-rw-rw-   0        0        0     2869 2022-08-29 10:19:49.000000 websiteclassificationapi-2.1.9/test/__init__.py
-drwxrwxrwx   0        0        0        0 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi/
--rw-rw-rw-   0        0        0     2869 2022-08-29 10:19:49.000000 websiteclassificationapi-2.1.9/websiteclassificationapi/__init__.py
-drwxrwxrwx   0        0        0        0 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/
--rw-rw-rw-   0        0        0    11766 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      264 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       30 2022-10-15 12:33:00.000000 websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/
+-rw-rw-rw-   0        0        0    14125 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/PKG-INFO
+-rw-rw-rw-   0        0        0    11262 2023-05-13 14:36:19.000000 websiteclassificationapi-2.2/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/setup.cfg
+-rw-rw-rw-   0        0        0     1379 2023-05-13 14:41:13.000000 websiteclassificationapi-2.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/test/
+-rw-rw-rw-   0        0        0     2869 2022-08-29 10:19:49.000000 websiteclassificationapi-2.2/test/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi/
+-rw-rw-rw-   0        0        0     2869 2022-08-29 10:19:49.000000 websiteclassificationapi-2.2/websiteclassificationapi/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi.egg-info/
+-rw-rw-rw-   0        0        0    14125 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      264 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       30 2023-05-13 14:41:24.000000 websiteclassificationapi-2.2/websiteclassificationapi.egg-info/top_level.txt
```

### Comparing `websiteclassificationapi-2.1.9/PKG-INFO` & `websiteclassificationapi-2.2/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -1,264 +1,262 @@
-Metadata-Version: 2.1
-Name: websiteclassificationapi
-Version: 2.1.9
-Summary: Website classification API
-Home-page: https://github.com/websitecategorization/websiteclassificationnapi
-Author-email: info@websitecategorizationapi.com
-License: UNKNOWN
-Description: # Website Classification API
-        
-        Python3 client library for [URL Classification](https://www.websitecategorizationapi.com). 
-        
-        Website classification API s a python library that allows to classify websites based on IAB and E-commerce taxonomies. 
-        
-        ## Installation 
-        ```
-        pip install websiteclassificationapi
-        ```
-        ## Requirements
-        
-        Only Python 3 is supported. You need an API key which you can obtain at . 
-        Python library requires only requests package. 
-        
-        ## Documentation 
-        
-        More detailed API documentation on URL Classification is [available here](https://www.websitecategorizationapi.com/api.php). 
-        
-        ## Examples 
-        
-        ```
-        from websiteclassificationapi import websiteclassificationapi
-        
-        api_key = 'h2XurA' # you can get API key from www.websitecategorizationapi.com
-        url = 'www.alpha-quantum.com' # can be set to any valid URL
-        classifier_type = 'iab1' # should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites
-        
-        # calling the API
-        print(websiteclassificationapi.get_categorization(url,api_key,classifier_type))
-        ```
-        
-        ## How to select classifiers of different taxonomies
-        
-        Classifier_type should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites. 
-        
-        IAB Tier 1 categorization returns probabilities of text being classified as one of 29 possible categories.
-        
-        IAB Tier 2 categorization returns probabilities of text being classified as one of 447 possible categories.
-        
-        Ecommerce Tier 1 categorization returns probabilities of text being classified as one of 21 possible categories.
-        
-        Ecommerce Tier 2 website categorization returns probabilities of text being classified as one of 182 possible categories.
-        
-        Ecommerce Tier 3 website categorization returns probabilities of text being classified as one of 1113 possible categories.
-        
-        ## Taxonomies
-        
-        The list of categories available by classifier is also known as Taxonomy. There are many taxonomies available, some are standard are well known, e.g. IAB taxonomy is well suited for ads and advertising in general, whereas Facebook product categories taxonomy 
-        is appropriate for ecommerce field. 
-        
-        Taxonomy also differ in how many tiers, levels, or depths do they support. E.g. taxonomy may only support 1 set of main categories, or it can further subcategories. 
-        
-        The categorization in the form of Tier 1/Tier 2/Tier 3/.... is also known as taxonomy path. 
-        
-        The classifiers can be either built in a way that they predict single Tier categories or they can return full taxonomy paths. It really depends on the use case what is most appropriate. 
-        
-        You can find more information about IAB taxonomy at this page: https://www.iab.com/guidelines/content-taxonomy/. 
-        
-        Taxonomy should be chosen in a way that it suits your use case. E.g. let us say you have an online store and currently you just list your products without any categorizations. 
-        
-        Then it may be very valuable if you could provide some kind of menus that categorize products in different verticals. 
-        
-        Why? Because your users may more easily find your products, you will have more subpages that can be indexed by search engines and thus provide you with more traffic and visits. 
-        
-        Having verticals set up may also mean better filtering and lead to higher conversions and thus lower cost of acquisition. There are a multitude of opportunities in adding categorization to an online store. 
-        
-        ## AI explainability
-        
-        One of the unique features of classifiers is that they provide machine learning interpretability or artificial intelligence explainability (XAI) in the form of words that most contribute to resulting classification. 
-        
-        Example 1 of explainability: 
-        ![Image1](https://www.websitecategorizationapi.com/product_categorization.png)
-        
-        Example 2 of explainability: 
-        ![Image1](https://www.websitecategorizationapi.com/productcategorizationnew1.jpg)
-        
-        Why the need of AI explainability? 
-        
-        AI models are increasingly being used in ways that affect humans. E.g. you may apply for a loan at the bank and get rejected, but even though a human may have sent or explained you this, the decision may have actually been made by a machine learning model. 
-        
-        Machine learning models making decisions is increasingly part of every day and because often these decisions are made by what could be termed black boxes, there is increasing desire for having ML decisions made in a way that are explainable. 
-        
-        There are also many regulations that demand this, e.g. GDPR. 
-        
-        ## Support for languages
-        
-        Classification service supports classifications of websites in 30+ major languages, including English, French, German, Italian, Spanish, Chinese and others.  
-        
-        ## Offline database of categorized domains
-        
-        We offer offline [URL database](https://www.websitecategorizationapi.com/url_database.php) of millions of categorized domains. It can be used web content filtering, AdTech marketing, cybersecurity, brand safety, contextual targeting. 
-        
-        It is ideal for those use cases where you require very low latency of requests, which can be achieved with pre-classified websites stored in database. 
-        
-        ## Handling websites with no texts
-        
-        When encountering websites that have no text and just images, our classifier relies on [online optical character recognition API service](https://ocrapi.io) to extract text (if any available) from images on the website. And then classify it. 
-        
-        To deal with potential duplicates we use the [reverse IP lookup of domains](https://reverseiplookupapi.com) to find similar domains that are hosted on the same IP. 
-        
-        ## Example classifications
-        
-        Example classification for website www.github.com:
-        ```
-        {
-          "classification": [
-            {
-              "category": "Technology & Computing",
-              "value": 0.7621352908406164
-            },
-            {
-              "category": "Business and Finance",
-              "value": 0.0785701408756428
-            },
-            {
-              "category": "Video Gaming",
-              "value": 0.06626958968249749
-            },
-            {
-              "category": "Fine Art",
-              "value": 0.017105357862223433
-            },
-            {
-              "category": "Hobbies & Interests",
-              "value": 0.016812511656388394
-            },
-            {
-              "category": "Sports",
-              "value": 0.011396157737341801
-            },
-            {
-              "category": "Home & Garden",
-              "value": 0.009099685741207822
-            },
-            {
-              "category": "Personal Finance",
-              "value": 0.0076400890345109055
-            },
-            {
-              "category": "News and Politics",
-              "value": 0.006692288300928684
-            },
-            {
-              "category": "Careers",
-              "value": 0.0039930258544077606
-            },
-            {
-              "category": "Automotive",
-              "value": 0.0029276292555247764
-            },
-            {
-              "category": "Events and Attractions",
-              "value": 0.0026449624402393084
-            },
-            {
-              "category": "Shopping",
-              "value": 0.0023606962223306537
-            },
-            {
-              "category": "Family and Relationships",
-              "value": 0.0023174171750800186
-            },
-            {
-              "category": "Music and Audio",
-              "value": 0.0020517145262615513
-            },
-            {
-              "category": "Movies",
-              "value": 0.0018936850100483473
-            },
-            {
-              "category": "Travel",
-              "value": 0.0009448942095545797
-            },
-            {
-              "category": "Science",
-              "value": 0.0008432696857311802
-            },
-            {
-              "category": "Pets",
-              "value": 0.0006956402098649299
-            },
-            {
-              "category": "Television",
-              "value": 0.0005261918310662409
-            },
-            {
-              "category": "Real Estate",
-              "value": 0.0005058920662560916
-            },
-            {
-              "category": "Religion & Spirituality",
-              "value": 0.000492253420442475
-            },
-            {
-              "category": "Healthy Living",
-              "value": 0.0004690261931844088
-            },
-            {
-              "category": "Medical Health",
-              "value": 0.0004467617749304944
-            },
-            {
-              "category": "Education",
-              "value": 0.00036333686743226124
-            },
-            {
-              "category": "Food & Drink",
-              "value": 0.0003463620639422737
-            },
-            {
-              "category": "Books and Literature",
-              "value": 0.00027078317064036986
-            },
-            {
-              "category": "Style & Fashion",
-              "value": 0.00011770141998920516
-            },
-            {
-              "category": "Pop Culture",
-              "value": 0.00006764487171529734
-            }
-          ],
-          "html": "29101",
-          "language": "en",
-          "status": 200
-        }
-        ```
-        
-        ## Useful resources used in development of website categorization
-        
-        - [Tensorflow](https://www.tensorflow.org/)
-        
-        - [Website categorization](https://medium.com/website-categorization/website-categorization-api-ca6c3e0f6c4d)
-        
-        - [Sklearn](https://scikit-learn.org/stable/)
-        
-        - [Physik nachhilfe muenchen](https://www.boplnachhilfe.de)
-        
-        - [Introduction to URL Categorization Database](https://www.alpha-quantum.com/blog/url-database/url-database/) 
-        
-        - [Top shopify stores](https://www.onlinestores.ai)
-        
-        
-        
-        
-Keywords: website categorization,classification,categorization
-Platform: UNKNOWN
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.3
-Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.0
-Classifier: Environment :: GPU :: NVIDIA CUDA
-Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.2
-Classifier: Environment :: GPU :: NVIDIA CUDA :: 10.1
-Classifier: Programming Language :: Python :: 3 :: Only
-Description-Content-Type: text/markdown
+# Website Classification API
+
+Python3 client library for [URL Classification](https://www.websitecategorizationapi.com). 
+
+Website classification API s a python library that allows to classify websites based on IAB and E-commerce taxonomies. 
+
+## Installation 
+```
+pip install websiteclassificationapi
+```
+## Requirements
+
+Only Python 3 is supported. You need an API key which you can obtain at . 
+Python library requires only requests package. 
+
+## Documentation 
+
+More detailed API documentation on URL Classification is [available here](https://www.websitecategorizationapi.com/api.php). 
+
+## Examples 
+
+```
+from websiteclassificationapi import websiteclassificationapi
+
+api_key = 'h2XurA' # you can get API key from www.websitecategorizationapi.com
+url = 'www.alpha-quantum.com' # can be set to any valid URL
+classifier_type = 'iab1' # should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites
+
+# calling the API
+print(websiteclassificationapi.get_categorization(url,api_key,classifier_type))
+```
+
+## How to select classifiers of different taxonomies
+
+Classifier_type should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites. 
+
+IAB Tier 1 categorization returns probabilities of text being classified as one of 29 possible categories.
+
+IAB Tier 2 categorization returns probabilities of text being classified as one of 447 possible categories.
+
+Ecommerce Tier 1 categorization returns probabilities of text being classified as one of 21 possible categories.
+
+Ecommerce Tier 2 website categorization returns probabilities of text being classified as one of 182 possible categories.
+
+Ecommerce Tier 3 website categorization returns probabilities of text being classified as one of 1113 possible categories.
+
+## Taxonomies
+
+The list of categories available by classifier is also known as Taxonomy. There are many taxonomies available, some are standard are well known, e.g. IAB taxonomy is well suited for ads and advertising in general, whereas Facebook product categories taxonomy 
+is appropriate for ecommerce field. 
+
+Taxonomy also differ in how many tiers, levels, or depths do they support. E.g. taxonomy may only support 1 set of main categories, or it can further subcategories. 
+
+The categorization in the form of Tier 1/Tier 2/Tier 3/.... is also known as taxonomy path. 
+
+The classifiers can be either built in a way that they predict single Tier categories or they can return full taxonomy paths. It really depends on the use case what is most appropriate. 
+
+You can find more information about IAB taxonomy at this page: https://www.iab.com/guidelines/content-taxonomy/. 
+
+Taxonomy should be chosen in a way that it suits your use case. E.g. let us say you have an online store and currently you just list your products without any categorizations. 
+
+Then it may be very valuable if you could provide some kind of menus that categorize products in different verticals. 
+
+Why? Because your users may more easily find your products, you will have more subpages that can be indexed by search engines and thus provide you with more traffic and visits. 
+
+Having verticals set up may also mean better filtering and lead to higher conversions and thus lower cost of acquisition. There are a multitude of opportunities in adding categorization to an online store. 
+
+## AI explainability
+
+One of the unique features of classifiers is that they provide machine learning interpretability or artificial intelligence explainability (XAI) in the form of words that most contribute to resulting classification. 
+
+Example 1 of explainability: 
+![Image1](https://www.websitecategorizationapi.com/product_categorization.png)
+
+Example 2 of explainability: 
+![Image1](https://www.websitecategorizationapi.com/productcategorizationnew1.jpg)
+
+Why the need of AI explainability? 
+
+AI models are increasingly being used in ways that affect humans. E.g. you may apply for a loan at the bank and get rejected, but even though a human may have sent or explained you this, the decision may have actually been made by a machine learning model. 
+
+Machine learning models making decisions is increasingly part of every day and because often these decisions are made by what could be termed black boxes, there is increasing desire for having ML decisions made in a way that are explainable. 
+
+There are also many regulations that demand this, e.g. GDPR. 
+
+## Support for languages
+
+Classification service supports classifications of websites in 30+ major languages, including English, French, German, Italian, Spanish, Chinese and others.  
+
+## Offline database of categorized domains
+
+We offer offline [URL database](https://www.websitecategorizationapi.com/url_database.php) of millions of categorized domains. It can be used web content filtering, AdTech marketing, cybersecurity, brand safety, contextual targeting. 
+
+It is ideal for those use cases where you require very low latency of requests, which can be achieved with pre-classified websites stored in database. 
+
+## Handling websites with no texts
+
+When encountering websites that have no text and just images, our classifier relies on [online optical character recognition API service](https://ocrapi.io) to extract text (if any available) from images on the website. And then classify it. 
+
+To deal with potential duplicates we use the [reverse IP lookup of domains](https://reverseiplookupapi.com) to find similar domains that are hosted on the same IP. 
+
+## Application of website categorization to technologies usage
+
+We have collected usage of technologies by millions of websites, by combining this with categorization, one can find interesting results. 
+
+Here is for example usage of Intercom across industry verticals: 
+
+![Image1](https://user-images.githubusercontent.com/58834207/238138013-d59d68b8-d7e3-42d2-bdda-100924669b72.png)
+
+Based on 50 millions of usage points we built an AI recommender which can predict which technologies for company using a set of technologies. 
+
+Here are e.g. recommendations for company using Mouse Flow: <table class="table" style="font-size:20px;line-height:30px"><thead><tr><th>Technology</th><th>AI Recommendation Score </th><th>Website</th></tr></thead><tbody><tr><td><a href="https://www.alpha-quantum.com/technologies/AppNexus">AppNexus</a></td><td>0.15</td><td>http://appnexus.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Microsoft Clarity">Microsoft Clarity</a></td><td>0.14</td><td>https://clarity.microsoft.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Osano">Osano</a></td><td>0.14</td><td>https://www.osano.com/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Jetpack">Jetpack</a></td><td>0.14</td><td>https://jetpack.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Raphael">Raphael</a></td><td>0.14</td><td>https://dmitrybaranovskiy.github.io/raphael/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Svelte">Svelte</a></td><td>0.13</td><td>https://svelte.dev</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/AWS Certificate Manager">AWS Certificate Manager</a></td><td>0.12</td><td>https://aws.amazon.com/certificate-manager/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Extendify">Extendify</a></td><td>0.11</td><td>https://extendify.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Kendo UI">Kendo UI</a></td><td>0.11</td><td>https://www.telerik.com/kendo-ui</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Flywheel">Flywheel</a></td><td>0.11</td><td>https://getflywheel.com</td></tr></tbody></table>
+
+
+
+
+
+## Example classifications
+
+Example classification for website www.github.com:
+```
+{
+  "classification": [
+    {
+      "category": "Technology & Computing",
+      "value": 0.7621352908406164
+    },
+    {
+      "category": "Business and Finance",
+      "value": 0.0785701408756428
+    },
+    {
+      "category": "Video Gaming",
+      "value": 0.06626958968249749
+    },
+    {
+      "category": "Fine Art",
+      "value": 0.017105357862223433
+    },
+    {
+      "category": "Hobbies & Interests",
+      "value": 0.016812511656388394
+    },
+    {
+      "category": "Sports",
+      "value": 0.011396157737341801
+    },
+    {
+      "category": "Home & Garden",
+      "value": 0.009099685741207822
+    },
+    {
+      "category": "Personal Finance",
+      "value": 0.0076400890345109055
+    },
+    {
+      "category": "News and Politics",
+      "value": 0.006692288300928684
+    },
+    {
+      "category": "Careers",
+      "value": 0.0039930258544077606
+    },
+    {
+      "category": "Automotive",
+      "value": 0.0029276292555247764
+    },
+    {
+      "category": "Events and Attractions",
+      "value": 0.0026449624402393084
+    },
+    {
+      "category": "Shopping",
+      "value": 0.0023606962223306537
+    },
+    {
+      "category": "Family and Relationships",
+      "value": 0.0023174171750800186
+    },
+    {
+      "category": "Music and Audio",
+      "value": 0.0020517145262615513
+    },
+    {
+      "category": "Movies",
+      "value": 0.0018936850100483473
+    },
+    {
+      "category": "Travel",
+      "value": 0.0009448942095545797
+    },
+    {
+      "category": "Science",
+      "value": 0.0008432696857311802
+    },
+    {
+      "category": "Pets",
+      "value": 0.0006956402098649299
+    },
+    {
+      "category": "Television",
+      "value": 0.0005261918310662409
+    },
+    {
+      "category": "Real Estate",
+      "value": 0.0005058920662560916
+    },
+    {
+      "category": "Religion & Spirituality",
+      "value": 0.000492253420442475
+    },
+    {
+      "category": "Healthy Living",
+      "value": 0.0004690261931844088
+    },
+    {
+      "category": "Medical Health",
+      "value": 0.0004467617749304944
+    },
+    {
+      "category": "Education",
+      "value": 0.00036333686743226124
+    },
+    {
+      "category": "Food & Drink",
+      "value": 0.0003463620639422737
+    },
+    {
+      "category": "Books and Literature",
+      "value": 0.00027078317064036986
+    },
+    {
+      "category": "Style & Fashion",
+      "value": 0.00011770141998920516
+    },
+    {
+      "category": "Pop Culture",
+      "value": 0.00006764487171529734
+    }
+  ],
+  "html": "29101",
+  "language": "en",
+  "status": 200
+}
+```
+
+## Useful resources used in development of website categorization
+
+- [Tensorflow](https://www.tensorflow.org/)
+
+- [Website categorization](https://medium.com/website-categorization/website-categorization-api-ca6c3e0f6c4d)
+
+- [Sklearn](https://scikit-learn.org/stable/)
+
+- [Physik nachhilfe muenchen](https://www.boplnachhilfe.de)
+
+- [Introduction to URL Categorization Database](https://www.alpha-quantum.com/blog/url-database/url-database/) 
+
+- [Top shopify stores](https://www.onlinestores.ai)
+
+
+
```

### Comparing `websiteclassificationapi-2.1.9/README.md` & `websiteclassificationapi-2.2/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,246 +1,280 @@
-# Website Classification API
-
-Python3 client library for [URL Classification](https://www.websitecategorizationapi.com). 
-
-Website classification API s a python library that allows to classify websites based on IAB and E-commerce taxonomies. 
-
-## Installation 
-```
-pip install websiteclassificationapi
-```
-## Requirements
-
-Only Python 3 is supported. You need an API key which you can obtain at . 
-Python library requires only requests package. 
-
-## Documentation 
-
-More detailed API documentation on URL Classification is [available here](https://www.websitecategorizationapi.com/api.php). 
-
-## Examples 
-
-```
-from websiteclassificationapi import websiteclassificationapi
-
-api_key = 'h2XurA' # you can get API key from www.websitecategorizationapi.com
-url = 'www.alpha-quantum.com' # can be set to any valid URL
-classifier_type = 'iab1' # should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites
-
-# calling the API
-print(websiteclassificationapi.get_categorization(url,api_key,classifier_type))
-```
-
-## How to select classifiers of different taxonomies
-
-Classifier_type should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites. 
-
-IAB Tier 1 categorization returns probabilities of text being classified as one of 29 possible categories.
-
-IAB Tier 2 categorization returns probabilities of text being classified as one of 447 possible categories.
-
-Ecommerce Tier 1 categorization returns probabilities of text being classified as one of 21 possible categories.
-
-Ecommerce Tier 2 website categorization returns probabilities of text being classified as one of 182 possible categories.
-
-Ecommerce Tier 3 website categorization returns probabilities of text being classified as one of 1113 possible categories.
-
-## Taxonomies
-
-The list of categories available by classifier is also known as Taxonomy. There are many taxonomies available, some are standard are well known, e.g. IAB taxonomy is well suited for ads and advertising in general, whereas Facebook product categories taxonomy 
-is appropriate for ecommerce field. 
-
-Taxonomy also differ in how many tiers, levels, or depths do they support. E.g. taxonomy may only support 1 set of main categories, or it can further subcategories. 
-
-The categorization in the form of Tier 1/Tier 2/Tier 3/.... is also known as taxonomy path. 
-
-The classifiers can be either built in a way that they predict single Tier categories or they can return full taxonomy paths. It really depends on the use case what is most appropriate. 
-
-You can find more information about IAB taxonomy at this page: https://www.iab.com/guidelines/content-taxonomy/. 
-
-Taxonomy should be chosen in a way that it suits your use case. E.g. let us say you have an online store and currently you just list your products without any categorizations. 
-
-Then it may be very valuable if you could provide some kind of menus that categorize products in different verticals. 
-
-Why? Because your users may more easily find your products, you will have more subpages that can be indexed by search engines and thus provide you with more traffic and visits. 
-
-Having verticals set up may also mean better filtering and lead to higher conversions and thus lower cost of acquisition. There are a multitude of opportunities in adding categorization to an online store. 
-
-## AI explainability
-
-One of the unique features of classifiers is that they provide machine learning interpretability or artificial intelligence explainability (XAI) in the form of words that most contribute to resulting classification. 
-
-Example 1 of explainability: 
-![Image1](https://www.websitecategorizationapi.com/product_categorization.png)
-
-Example 2 of explainability: 
-![Image1](https://www.websitecategorizationapi.com/productcategorizationnew1.jpg)
-
-Why the need of AI explainability? 
-
-AI models are increasingly being used in ways that affect humans. E.g. you may apply for a loan at the bank and get rejected, but even though a human may have sent or explained you this, the decision may have actually been made by a machine learning model. 
-
-Machine learning models making decisions is increasingly part of every day and because often these decisions are made by what could be termed black boxes, there is increasing desire for having ML decisions made in a way that are explainable. 
-
-There are also many regulations that demand this, e.g. GDPR. 
-
-## Support for languages
-
-Classification service supports classifications of websites in 30+ major languages, including English, French, German, Italian, Spanish, Chinese and others.  
-
-## Offline database of categorized domains
-
-We offer offline [URL database](https://www.websitecategorizationapi.com/url_database.php) of millions of categorized domains. It can be used web content filtering, AdTech marketing, cybersecurity, brand safety, contextual targeting. 
-
-It is ideal for those use cases where you require very low latency of requests, which can be achieved with pre-classified websites stored in database. 
-
-## Handling websites with no texts
-
-When encountering websites that have no text and just images, our classifier relies on [online optical character recognition API service](https://ocrapi.io) to extract text (if any available) from images on the website. And then classify it. 
-
-To deal with potential duplicates we use the [reverse IP lookup of domains](https://reverseiplookupapi.com) to find similar domains that are hosted on the same IP. 
-
-## Example classifications
-
-Example classification for website www.github.com:
-```
-{
-  "classification": [
-    {
-      "category": "Technology & Computing",
-      "value": 0.7621352908406164
-    },
-    {
-      "category": "Business and Finance",
-      "value": 0.0785701408756428
-    },
-    {
-      "category": "Video Gaming",
-      "value": 0.06626958968249749
-    },
-    {
-      "category": "Fine Art",
-      "value": 0.017105357862223433
-    },
-    {
-      "category": "Hobbies & Interests",
-      "value": 0.016812511656388394
-    },
-    {
-      "category": "Sports",
-      "value": 0.011396157737341801
-    },
-    {
-      "category": "Home & Garden",
-      "value": 0.009099685741207822
-    },
-    {
-      "category": "Personal Finance",
-      "value": 0.0076400890345109055
-    },
-    {
-      "category": "News and Politics",
-      "value": 0.006692288300928684
-    },
-    {
-      "category": "Careers",
-      "value": 0.0039930258544077606
-    },
-    {
-      "category": "Automotive",
-      "value": 0.0029276292555247764
-    },
-    {
-      "category": "Events and Attractions",
-      "value": 0.0026449624402393084
-    },
-    {
-      "category": "Shopping",
-      "value": 0.0023606962223306537
-    },
-    {
-      "category": "Family and Relationships",
-      "value": 0.0023174171750800186
-    },
-    {
-      "category": "Music and Audio",
-      "value": 0.0020517145262615513
-    },
-    {
-      "category": "Movies",
-      "value": 0.0018936850100483473
-    },
-    {
-      "category": "Travel",
-      "value": 0.0009448942095545797
-    },
-    {
-      "category": "Science",
-      "value": 0.0008432696857311802
-    },
-    {
-      "category": "Pets",
-      "value": 0.0006956402098649299
-    },
-    {
-      "category": "Television",
-      "value": 0.0005261918310662409
-    },
-    {
-      "category": "Real Estate",
-      "value": 0.0005058920662560916
-    },
-    {
-      "category": "Religion & Spirituality",
-      "value": 0.000492253420442475
-    },
-    {
-      "category": "Healthy Living",
-      "value": 0.0004690261931844088
-    },
-    {
-      "category": "Medical Health",
-      "value": 0.0004467617749304944
-    },
-    {
-      "category": "Education",
-      "value": 0.00036333686743226124
-    },
-    {
-      "category": "Food & Drink",
-      "value": 0.0003463620639422737
-    },
-    {
-      "category": "Books and Literature",
-      "value": 0.00027078317064036986
-    },
-    {
-      "category": "Style & Fashion",
-      "value": 0.00011770141998920516
-    },
-    {
-      "category": "Pop Culture",
-      "value": 0.00006764487171529734
-    }
-  ],
-  "html": "29101",
-  "language": "en",
-  "status": 200
-}
-```
-
-## Useful resources used in development of website categorization
-
-- [Tensorflow](https://www.tensorflow.org/)
-
-- [Website categorization](https://medium.com/website-categorization/website-categorization-api-ca6c3e0f6c4d)
-
-- [Sklearn](https://scikit-learn.org/stable/)
-
-- [Physik nachhilfe muenchen](https://www.boplnachhilfe.de)
-
-- [Introduction to URL Categorization Database](https://www.alpha-quantum.com/blog/url-database/url-database/) 
-
-- [Top shopify stores](https://www.onlinestores.ai)
-
-
-
+Metadata-Version: 2.1
+Name: websiteclassificationapi
+Version: 2.2
+Summary: Website classification API
+Home-page: https://github.com/websitecategorization/websiteclassificationnapi
+Author-email: info@websitecategorizationapi.com
+License: UNKNOWN
+Description: # Website Classification API
+        
+        Python3 client library for [URL Classification](https://www.websitecategorizationapi.com). 
+        
+        Website classification API s a python library that allows to classify websites based on IAB and E-commerce taxonomies. 
+        
+        ## Installation 
+        ```
+        pip install websiteclassificationapi
+        ```
+        ## Requirements
+        
+        Only Python 3 is supported. You need an API key which you can obtain at . 
+        Python library requires only requests package. 
+        
+        ## Documentation 
+        
+        More detailed API documentation on URL Classification is [available here](https://www.websitecategorizationapi.com/api.php). 
+        
+        ## Examples 
+        
+        ```
+        from websiteclassificationapi import websiteclassificationapi
+        
+        api_key = 'h2XurA' # you can get API key from www.websitecategorizationapi.com
+        url = 'www.alpha-quantum.com' # can be set to any valid URL
+        classifier_type = 'iab1' # should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites
+        
+        # calling the API
+        print(websiteclassificationapi.get_categorization(url,api_key,classifier_type))
+        ```
+        
+        ## How to select classifiers of different taxonomies
+        
+        Classifier_type should be set to either iab1 (Tier 1 categorization) or iab2 (Tier 2 categorization) for general websites or ecommerce1, ecommerce2 and ecommerce3 for E-commerce or product websites. 
+        
+        IAB Tier 1 categorization returns probabilities of text being classified as one of 29 possible categories.
+        
+        IAB Tier 2 categorization returns probabilities of text being classified as one of 447 possible categories.
+        
+        Ecommerce Tier 1 categorization returns probabilities of text being classified as one of 21 possible categories.
+        
+        Ecommerce Tier 2 website categorization returns probabilities of text being classified as one of 182 possible categories.
+        
+        Ecommerce Tier 3 website categorization returns probabilities of text being classified as one of 1113 possible categories.
+        
+        ## Taxonomies
+        
+        The list of categories available by classifier is also known as Taxonomy. There are many taxonomies available, some are standard are well known, e.g. IAB taxonomy is well suited for ads and advertising in general, whereas Facebook product categories taxonomy 
+        is appropriate for ecommerce field. 
+        
+        Taxonomy also differ in how many tiers, levels, or depths do they support. E.g. taxonomy may only support 1 set of main categories, or it can further subcategories. 
+        
+        The categorization in the form of Tier 1/Tier 2/Tier 3/.... is also known as taxonomy path. 
+        
+        The classifiers can be either built in a way that they predict single Tier categories or they can return full taxonomy paths. It really depends on the use case what is most appropriate. 
+        
+        You can find more information about IAB taxonomy at this page: https://www.iab.com/guidelines/content-taxonomy/. 
+        
+        Taxonomy should be chosen in a way that it suits your use case. E.g. let us say you have an online store and currently you just list your products without any categorizations. 
+        
+        Then it may be very valuable if you could provide some kind of menus that categorize products in different verticals. 
+        
+        Why? Because your users may more easily find your products, you will have more subpages that can be indexed by search engines and thus provide you with more traffic and visits. 
+        
+        Having verticals set up may also mean better filtering and lead to higher conversions and thus lower cost of acquisition. There are a multitude of opportunities in adding categorization to an online store. 
+        
+        ## AI explainability
+        
+        One of the unique features of classifiers is that they provide machine learning interpretability or artificial intelligence explainability (XAI) in the form of words that most contribute to resulting classification. 
+        
+        Example 1 of explainability: 
+        ![Image1](https://www.websitecategorizationapi.com/product_categorization.png)
+        
+        Example 2 of explainability: 
+        ![Image1](https://www.websitecategorizationapi.com/productcategorizationnew1.jpg)
+        
+        Why the need of AI explainability? 
+        
+        AI models are increasingly being used in ways that affect humans. E.g. you may apply for a loan at the bank and get rejected, but even though a human may have sent or explained you this, the decision may have actually been made by a machine learning model. 
+        
+        Machine learning models making decisions is increasingly part of every day and because often these decisions are made by what could be termed black boxes, there is increasing desire for having ML decisions made in a way that are explainable. 
+        
+        There are also many regulations that demand this, e.g. GDPR. 
+        
+        ## Support for languages
+        
+        Classification service supports classifications of websites in 30+ major languages, including English, French, German, Italian, Spanish, Chinese and others.  
+        
+        ## Offline database of categorized domains
+        
+        We offer offline [URL database](https://www.websitecategorizationapi.com/url_database.php) of millions of categorized domains. It can be used web content filtering, AdTech marketing, cybersecurity, brand safety, contextual targeting. 
+        
+        It is ideal for those use cases where you require very low latency of requests, which can be achieved with pre-classified websites stored in database. 
+        
+        ## Handling websites with no texts
+        
+        When encountering websites that have no text and just images, our classifier relies on [online optical character recognition API service](https://ocrapi.io) to extract text (if any available) from images on the website. And then classify it. 
+        
+        To deal with potential duplicates we use the [reverse IP lookup of domains](https://reverseiplookupapi.com) to find similar domains that are hosted on the same IP. 
+        
+        ## Application of website categorization to technologies usage
+        
+        We have collected usage of technologies by millions of websites, by combining this with categorization, one can find interesting results. 
+        
+        Here is for example usage of Intercom across industry verticals: 
+        
+        ![Image1](https://user-images.githubusercontent.com/58834207/238138013-d59d68b8-d7e3-42d2-bdda-100924669b72.png)
+        
+        Based on 50 millions of usage points we built an AI recommender which can predict which technologies for company using a set of technologies. 
+        
+        Here are e.g. recommendations for company using Mouse Flow: <table class="table" style="font-size:20px;line-height:30px"><thead><tr><th>Technology</th><th>AI Recommendation Score </th><th>Website</th></tr></thead><tbody><tr><td><a href="https://www.alpha-quantum.com/technologies/AppNexus">AppNexus</a></td><td>0.15</td><td>http://appnexus.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Microsoft Clarity">Microsoft Clarity</a></td><td>0.14</td><td>https://clarity.microsoft.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Osano">Osano</a></td><td>0.14</td><td>https://www.osano.com/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Jetpack">Jetpack</a></td><td>0.14</td><td>https://jetpack.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Raphael">Raphael</a></td><td>0.14</td><td>https://dmitrybaranovskiy.github.io/raphael/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Svelte">Svelte</a></td><td>0.13</td><td>https://svelte.dev</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/AWS Certificate Manager">AWS Certificate Manager</a></td><td>0.12</td><td>https://aws.amazon.com/certificate-manager/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Extendify">Extendify</a></td><td>0.11</td><td>https://extendify.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Kendo UI">Kendo UI</a></td><td>0.11</td><td>https://www.telerik.com/kendo-ui</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Flywheel">Flywheel</a></td><td>0.11</td><td>https://getflywheel.com</td></tr></tbody></table>
+        
+        
+        
+        
+        
+        ## Example classifications
+        
+        Example classification for website www.github.com:
+        ```
+        {
+          "classification": [
+            {
+              "category": "Technology & Computing",
+              "value": 0.7621352908406164
+            },
+            {
+              "category": "Business and Finance",
+              "value": 0.0785701408756428
+            },
+            {
+              "category": "Video Gaming",
+              "value": 0.06626958968249749
+            },
+            {
+              "category": "Fine Art",
+              "value": 0.017105357862223433
+            },
+            {
+              "category": "Hobbies & Interests",
+              "value": 0.016812511656388394
+            },
+            {
+              "category": "Sports",
+              "value": 0.011396157737341801
+            },
+            {
+              "category": "Home & Garden",
+              "value": 0.009099685741207822
+            },
+            {
+              "category": "Personal Finance",
+              "value": 0.0076400890345109055
+            },
+            {
+              "category": "News and Politics",
+              "value": 0.006692288300928684
+            },
+            {
+              "category": "Careers",
+              "value": 0.0039930258544077606
+            },
+            {
+              "category": "Automotive",
+              "value": 0.0029276292555247764
+            },
+            {
+              "category": "Events and Attractions",
+              "value": 0.0026449624402393084
+            },
+            {
+              "category": "Shopping",
+              "value": 0.0023606962223306537
+            },
+            {
+              "category": "Family and Relationships",
+              "value": 0.0023174171750800186
+            },
+            {
+              "category": "Music and Audio",
+              "value": 0.0020517145262615513
+            },
+            {
+              "category": "Movies",
+              "value": 0.0018936850100483473
+            },
+            {
+              "category": "Travel",
+              "value": 0.0009448942095545797
+            },
+            {
+              "category": "Science",
+              "value": 0.0008432696857311802
+            },
+            {
+              "category": "Pets",
+              "value": 0.0006956402098649299
+            },
+            {
+              "category": "Television",
+              "value": 0.0005261918310662409
+            },
+            {
+              "category": "Real Estate",
+              "value": 0.0005058920662560916
+            },
+            {
+              "category": "Religion & Spirituality",
+              "value": 0.000492253420442475
+            },
+            {
+              "category": "Healthy Living",
+              "value": 0.0004690261931844088
+            },
+            {
+              "category": "Medical Health",
+              "value": 0.0004467617749304944
+            },
+            {
+              "category": "Education",
+              "value": 0.00036333686743226124
+            },
+            {
+              "category": "Food & Drink",
+              "value": 0.0003463620639422737
+            },
+            {
+              "category": "Books and Literature",
+              "value": 0.00027078317064036986
+            },
+            {
+              "category": "Style & Fashion",
+              "value": 0.00011770141998920516
+            },
+            {
+              "category": "Pop Culture",
+              "value": 0.00006764487171529734
+            }
+          ],
+          "html": "29101",
+          "language": "en",
+          "status": 200
+        }
+        ```
+        
+        ## Useful resources used in development of website categorization
+        
+        - [Tensorflow](https://www.tensorflow.org/)
+        
+        - [Website categorization](https://medium.com/website-categorization/website-categorization-api-ca6c3e0f6c4d)
+        
+        - [Sklearn](https://scikit-learn.org/stable/)
+        
+        - [Physik nachhilfe muenchen](https://www.boplnachhilfe.de)
+        
+        - [Introduction to URL Categorization Database](https://www.alpha-quantum.com/blog/url-database/url-database/) 
+        
+        - [Top shopify stores](https://www.onlinestores.ai)
+        
+        
+        
+        
+Keywords: website categorization,classification,categorization
+Platform: UNKNOWN
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.3
+Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.0
+Classifier: Environment :: GPU :: NVIDIA CUDA
+Classifier: Environment :: GPU :: NVIDIA CUDA :: 11.2
+Classifier: Environment :: GPU :: NVIDIA CUDA :: 10.1
+Classifier: Programming Language :: Python :: 3 :: Only
+Description-Content-Type: text/markdown
```

### Comparing `websiteclassificationapi-2.1.9/setup.py` & `websiteclassificationapi-2.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 
 setup(
     # The name of project.
     # pip install websiteclassificationapi
     name="websiteclassificationapi",
 
     # The version of your project.
-    version="2.1.9",
+    version="2.2",
 
     packages=find_packages(exclude="tests"),
 
     description="Website classification API",
 
     long_description=README_MD,
```

### Comparing `websiteclassificationapi-2.1.9/test/__init__.py` & `websiteclassificationapi-2.2/test/__init__.py`

 * *Files identical despite different names*

### Comparing `websiteclassificationapi-2.1.9/websiteclassificationapi/__init__.py` & `websiteclassificationapi-2.2/websiteclassificationapi/__init__.py`

 * *Files identical despite different names*

### Comparing `websiteclassificationapi-2.1.9/websiteclassificationapi.egg-info/PKG-INFO` & `websiteclassificationapi-2.2/websiteclassificationapi.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: websiteclassificationapi
-Version: 2.1.9
+Version: 2.2
 Summary: Website classification API
 Home-page: https://github.com/websitecategorization/websiteclassificationnapi
 Author-email: info@websitecategorizationapi.com
 License: UNKNOWN
 Description: # Website Classification API
         
         Python3 client library for [URL Classification](https://www.websitecategorizationapi.com). 
@@ -102,14 +102,30 @@
         
         ## Handling websites with no texts
         
         When encountering websites that have no text and just images, our classifier relies on [online optical character recognition API service](https://ocrapi.io) to extract text (if any available) from images on the website. And then classify it. 
         
         To deal with potential duplicates we use the [reverse IP lookup of domains](https://reverseiplookupapi.com) to find similar domains that are hosted on the same IP. 
         
+        ## Application of website categorization to technologies usage
+        
+        We have collected usage of technologies by millions of websites, by combining this with categorization, one can find interesting results. 
+        
+        Here is for example usage of Intercom across industry verticals: 
+        
+        ![Image1](https://user-images.githubusercontent.com/58834207/238138013-d59d68b8-d7e3-42d2-bdda-100924669b72.png)
+        
+        Based on 50 millions of usage points we built an AI recommender which can predict which technologies for company using a set of technologies. 
+        
+        Here are e.g. recommendations for company using Mouse Flow: <table class="table" style="font-size:20px;line-height:30px"><thead><tr><th>Technology</th><th>AI Recommendation Score </th><th>Website</th></tr></thead><tbody><tr><td><a href="https://www.alpha-quantum.com/technologies/AppNexus">AppNexus</a></td><td>0.15</td><td>http://appnexus.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Microsoft Clarity">Microsoft Clarity</a></td><td>0.14</td><td>https://clarity.microsoft.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Osano">Osano</a></td><td>0.14</td><td>https://www.osano.com/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Jetpack">Jetpack</a></td><td>0.14</td><td>https://jetpack.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Raphael">Raphael</a></td><td>0.14</td><td>https://dmitrybaranovskiy.github.io/raphael/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Svelte">Svelte</a></td><td>0.13</td><td>https://svelte.dev</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/AWS Certificate Manager">AWS Certificate Manager</a></td><td>0.12</td><td>https://aws.amazon.com/certificate-manager/</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Extendify">Extendify</a></td><td>0.11</td><td>https://extendify.com</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Kendo UI">Kendo UI</a></td><td>0.11</td><td>https://www.telerik.com/kendo-ui</td></tr><tr><td><a href="https://www.alpha-quantum.com/technologies/Flywheel">Flywheel</a></td><td>0.11</td><td>https://getflywheel.com</td></tr></tbody></table>
+        
+        
+        
+        
+        
         ## Example classifications
         
         Example classification for website www.github.com:
         ```
         {
           "classification": [
             {
```

