# Comparing `tmp/IMDbTraktSyncer-1.0.9.tar.gz` & `tmp/IMDbTraktSyncer-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IMDbTraktSyncer-1.0.9.tar", last modified: Sun May  7 03:06:22 2023, max compression
+gzip compressed data, was "IMDbTraktSyncer-1.1.0.tar", last modified: Sat May 13 08:17:30 2023, max compression
```

## Comparing `IMDbTraktSyncer-1.0.9.tar` & `IMDbTraktSyncer-1.1.0.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxrwxrwx   0        0        0        0 2023-05-07 03:06:22.619098 IMDbTraktSyncer-1.0.9/
-drwxrwxrwx   0        0        0        0 2023-05-07 03:06:22.598310 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/
--rw-rw-rw-   0        0        0     7944 2023-05-07 03:02:56.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/IMDbTraktSyncer.py
--rw-rw-rw-   0        0        0        0 2023-04-29 22:05:24.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/__init__.py
--rw-rw-rw-   0        0        0     1805 2023-05-06 06:40:54.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/authTrakt.py
--rw-rw-rw-   0        0        0      642 2023-05-06 06:40:54.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/checkChromedriver.py
--rw-rw-rw-   0        0        0     2038 2023-05-06 06:40:54.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/imdbRatings.py
--rw-rw-rw-   0        0        0     1408 2023-05-06 06:40:54.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/traktRatings.py
--rw-rw-rw-   0        0        0     2516 2023-05-06 06:40:54.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/verifyCredentials.py
-drwxrwxrwx   0        0        0        0 2023-05-07 03:06:22.616611 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/
--rw-rw-rw-   0        0        0     5959 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      491 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       73 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       29 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/requires.txt
--rw-rw-rw-   0        0        0       16 2023-05-07 03:06:22.000000 IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1079 2023-04-26 18:19:27.000000 IMDbTraktSyncer-1.0.9/LICENSE
--rw-rw-rw-   0        0        0     5959 2023-05-07 03:06:22.618599 IMDbTraktSyncer-1.0.9/PKG-INFO
--rw-rw-rw-   0        0        0     5342 2023-05-07 03:05:58.000000 IMDbTraktSyncer-1.0.9/README.md
--rw-rw-rw-   0        0        0       42 2023-05-07 03:06:22.619606 IMDbTraktSyncer-1.0.9/setup.cfg
--rw-rw-rw-   0        0        0     1287 2023-05-07 03:05:11.000000 IMDbTraktSyncer-1.0.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.402412 IMDbTraktSyncer-1.1.0/
+drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.366967 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/
+-rw-rw-rw-   0        0        0    10477 2023-05-13 08:14:40.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/IMDbTraktSyncer.py
+-rw-rw-rw-   0        0        0        0 2023-04-29 22:05:24.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/__init__.py
+-rw-rw-rw-   0        0        0     1805 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/authTrakt.py
+-rw-rw-rw-   0        0        0      642 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/checkChromedriver.py
+-rw-rw-rw-   0        0        0     2038 2023-05-13 08:07:22.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/imdbRatings.py
+-rw-rw-rw-   0        0        0     1408 2023-05-13 08:07:19.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/traktRatings.py
+-rw-rw-rw-   0        0        0     2516 2023-05-07 03:12:27.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/verifyCredentials.py
+drwxrwxrwx   0        0        0        0 2023-05-13 08:17:30.399414 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/
+-rw-rw-rw-   0        0        0     6624 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      491 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       73 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       29 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       16 2023-05-13 08:17:30.000000 IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1079 2023-04-26 18:19:27.000000 IMDbTraktSyncer-1.1.0/LICENSE
+-rw-rw-rw-   0        0        0     6624 2023-05-13 08:17:30.401414 IMDbTraktSyncer-1.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     6004 2023-05-13 08:16:25.000000 IMDbTraktSyncer-1.1.0/README.md
+-rw-rw-rw-   0        0        0       42 2023-05-13 08:17:30.402412 IMDbTraktSyncer-1.1.0/setup.cfg
+-rw-rw-rw-   0        0        0     1287 2023-05-13 08:17:03.000000 IMDbTraktSyncer-1.1.0/setup.py
```

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/IMDbTraktSyncer.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/IMDbTraktSyncer.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,19 +1,21 @@
 import os
 import json
 import subprocess
 import requests
 import time
+import logging
 from selenium import webdriver
 from selenium.webdriver.chrome.service import Service
 from selenium.webdriver.common.by import By
 from selenium.common.exceptions import StaleElementReferenceException
 from selenium.webdriver.chrome.options import Options
 from selenium.webdriver.support.ui import WebDriverWait
 from selenium.webdriver.support import expected_conditions as EC
+from selenium.common.exceptions import SessionNotCreatedException
 try:
     from IMDbTraktSyncer import checkChromedriver
     from IMDbTraktSyncer import verifyCredentials
     from IMDbTraktSyncer import traktRatings
     from IMDbTraktSyncer import imdbRatings
 except:
     import checkChromedriver
@@ -30,41 +32,54 @@
     trakt_client_secret = verifyCredentials.trakt_client_secret
     trakt_access_token = verifyCredentials.trakt_access_token
     imdb_username = verifyCredentials.imdb_username
     imdb_password = verifyCredentials.imdb_password
     
     directory = os.path.dirname(os.path.realpath(__file__))
     
+    logging.getLogger('selenium.webdriver').setLevel(logging.WARNING)
+    
     #Start web driver
-    print('Starting webdriver')
+    print('Starting webdriver...')
     options = Options()
     options.add_argument("--headless=new")
     options.add_argument('--user-agent=Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3')
     options.add_experimental_option("prefs", {"download.default_directory": directory, "download.directory_upgrade": True, "download.prompt_for_download": False, "credentials_enable_service": False, "profile.password_manager_enabled": False})
     options.add_argument("--disable-save-password-bubble")
+    options.add_argument("--disable-infobars")
     options.add_argument("--disable-autofill-for-password-fields")
     options.add_argument('--disable-notifications')
     options.add_argument("--disable-third-party-cookies")
     options.add_argument("--disable-dev-shm-usage")
     options.add_argument("--no-sandbox")
     options.add_argument("--disable-extensions")
-    options.add_experimental_option("excludeSwitches", ["enable-automation"])
+    options.add_experimental_option("excludeSwitches", ["enable-automation", "enable-logging"])
     options.add_experimental_option("useAutomationExtension", False)
     options.add_argument('--log-level=3')
 
     service = Service(executable_path=binary_path)
-    driver = webdriver.Chrome(service=service, options=options)
+    try:
+        driver = webdriver.Chrome(service=service, options=options)
+    except SessionNotCreatedException as e:
+        error_message = str(e)
+        if "This version of ChromeDriver only supports Chrome version" in error_message:
+            extract_message = error_message.split("Stacktrace:")[0].replace("Message: session not created:", "").strip()
+            print(f"Error: {extract_message}")
+            print("See this link for details on how to fix: https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/16")
+            raise SystemExit
+        else:
+            raise
 
     wait = WebDriverWait(driver, 20)
 
     driver.get('https://www.imdb.com/registration/signin')
 
     # wait for sign in link to appear and then click it
-    sign_in_link = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, '.auth-provider-text')))
-    if sign_in_link.text == 'Sign in with IMDb':
+    sign_in_link = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, 'a.list-group-item > .auth-provider-text')))
+    if 'IMDb' in sign_in_link.text:
         sign_in_link.click()
 
     # wait for email input field and password input field to appear, then enter credentials and submit
     email_input = wait.until(EC.presence_of_all_elements_located((By.CSS_SELECTOR, "input[type='email']")))[0]
     password_input = wait.until(EC.presence_of_all_elements_located((By.CSS_SELECTOR, "input[type='password']")))[0]
     email_input.send_keys(imdb_username)
     password_input.send_keys(imdb_password)
@@ -76,106 +91,125 @@
     # go to IMDb homepage
     driver.get('https://www.imdb.com/')
 
     time.sleep(2)
 
     # Check if signed in
     element = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".nav__userMenu.navbar__user")))
-    if "Sign In" in element.text:
-        print("Not signed in")
+    if element.find_elements(By.CSS_SELECTOR, ".imdb-header__account-toggle--logged-in"):
+        print("Successfully signed in to IMDb")
     else:
-        print("Signed in")
+        print("Error: Not signed in to IMDb")
+        print("\nPossible IMDb captcha check or IMDb login incorrect.")
+        print("\nIf your login is correct then an IMDb captcha check likely the cause of this error. To fix this, simply login to the IMDb website in your browser, preferably Chrome, and from the same computer. If logged in, log out and log back in. It may ask you to fill in a captcha; complete it and finish logging in. After logging in successfully on your browser, run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues.")
+        print("\nIf your IMDb login is incorrect, simply edit the credentials.txt file with the correct login or delete the credentials file and run the script again.")
+        print("\nSee this GitHub link for more details: https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/2")
+        print("\nStopping script...")
+        raise SystemExit
     
     trakt_ratings = traktRatings.getTraktRatings(trakt_client_id, trakt_access_token)
     imdb_ratings = imdbRatings.getImdbRatings(imdb_username, imdb_password, driver, directory, wait)
-    
-    print('Setting IMDB Ratings')
-        
+
     #Get trakt and imdb ratings and filter out trakt ratings wish missing imbd id
     trakt_ratings = [rating for rating in trakt_ratings if rating['ID'] is not None]
     imdb_ratings = [rating for rating in imdb_ratings if rating['ID'] is not None]
     #Filter out ratings already set
     imdb_ratings_to_set = [rating for rating in trakt_ratings if rating['ID'] not in [imdb_rating['ID'] for imdb_rating in imdb_ratings]]
     trakt_ratings_to_set = [rating for rating in imdb_ratings if rating['ID'] not in [trakt_rating['ID'] for trakt_rating in trakt_ratings]]
 
-    # loop through each movie and TV show rating and submit rating on IMDb website
-    for i, item in enumerate(imdb_ratings_to_set, 1):
-        print(f'Rating {item["Type"]}: ({i} of {len(imdb_ratings_to_set)}) {item["Title"]} ({item["Year"]}): {item["Rating"]}/10 on IMDb')
-        driver.get(f'https://www.imdb.com/title/{item["ID"]}/')
-        time.sleep(2)
-
-        # click on "Rate" button and select rating option, then submit rating
-        buttons = wait.until(EC.presence_of_all_elements_located((By.CSS_SELECTOR, 'button.ipc-btn span')))
-        found_rate_button = False
-        for button in buttons:
-            if "Rate" in button.text:
-                driver.execute_script("arguments[0].click();", button)
-                rating_option_element = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, f'button[aria-label="Rate {item["Rating"]}"]')))
-                driver.execute_script("arguments[0].click();", rating_option_element)
-                submit_element = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, 'button.ipc-rating-prompt__rate-button')))
-                submit_element.click()
-                found_rate_button = True
-                break
-
-        if not found_rate_button:
-            continue
-            
-    print('Setting Trakt Ratings')
-
-    # Set the API endpoints
-    oauth_url = "https://api.trakt.tv/oauth/token"
-    rate_url = "https://api.trakt.tv/sync/ratings"
-
-    # Set the headers
-    headers = {
-        "Content-Type": "application/json",
-        "trakt-api-version": "2",
-        "trakt-api-key": trakt_client_id,
-        "Authorization": f"Bearer {trakt_access_token}"
-    }
-    
-    # Count the total number of items to rate
-    num_items = len(trakt_ratings_to_set)
-    item_count = 0
-            
-    # Loop through your data table and rate each item on Trakt
-    for item in trakt_ratings_to_set:
-        item_count += 1
-        if item["Type"] == "show":
-            # This is a TV show
-            data = {
-                "shows": [{
-                    "ids": {
-                        "imdb": item["ID"]
-                    },
-                    "rating": item["Rating"]
-                }]
-            }
-            print(f"Rating TV show ({item_count} of {num_items}): {item['Title']} ({item['Year']}) with rating {item['Rating']}/10 on Trakt")
-        elif item["Type"] == "movie":
-            # This is a movie
-            data = {
-                "movies": [{
-                    "ids": {
-                        "imdb": item["ID"]
-                    },
-                    "rating": item["Rating"]
-                }]
-            }
-            print(f"Rating movie ({item_count} of {num_items}): {item['Title']} ({item['Year']}) with rating {item['Rating']}/10 on Trakt")
-
-        # Make the API call to rate the item
-        response = requests.post(rate_url, headers=headers, json=data)
-        time.sleep(1)
-        while response.status_code == 429:
-            print("Rate limit exceeded. Waiting for 1 second...")
-            time.sleep(1)
+    if imdb_ratings_to_set:
+        print('Setting IMDB Ratings')
+
+        # loop through each movie and TV show rating and submit rating on IMDb website
+        for i, item in enumerate(imdb_ratings_to_set, 1):
+            print(f'Rating {item["Type"]}: ({i} of {len(imdb_ratings_to_set)}) {item["Title"]} ({item["Year"]}): {item["Rating"]}/10 on IMDb')
+            driver.get(f'https://www.imdb.com/title/{item["ID"]}/')
+            time.sleep(2)
+
+            # click on "Rate" button and select rating option, then submit rating
+            buttons = wait.until(EC.presence_of_all_elements_located((By.CSS_SELECTOR, 'button.ipc-btn span')))
+            found_rate_button = False
+            for button in buttons:
+                try:
+                    element_rating_bar = button.find_element(By.CSS_SELECTOR, '[data-testid="hero-rating-bar__user-rating__unrated"]')
+                    if element_rating_bar:
+                        driver.execute_script("arguments[0].click();", button)
+                        rating_option_element = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, f'button[aria-label="Rate {item["Rating"]}"]')))
+                        driver.execute_script("arguments[0].click();", rating_option_element)
+                        submit_element = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, 'button.ipc-rating-prompt__rate-button')))
+                        submit_element.click()
+                        found_rate_button = True
+                        break
+                except:
+                    continue
+
+            if not found_rate_button:
+                continue
+        print('Setting IMDb Ratings Complete')
+    else:
+        print('No IMDb Ratings To Set')
+
+    if trakt_ratings_to_set:
+        print('Setting Trakt Ratings')
+
+        # Set the API endpoints
+        oauth_url = "https://api.trakt.tv/oauth/token"
+        rate_url = "https://api.trakt.tv/sync/ratings"
+
+        # Set the headers
+        headers = {
+            "Content-Type": "application/json",
+            "trakt-api-version": "2",
+            "trakt-api-key": trakt_client_id,
+            "Authorization": f"Bearer {trakt_access_token}"
+        }
+        
+        # Count the total number of items to rate
+        num_items = len(trakt_ratings_to_set)
+        item_count = 0
+                
+        # Loop through your data table and rate each item on Trakt
+        for item in trakt_ratings_to_set:
+            item_count += 1
+            if item["Type"] == "show":
+                # This is a TV show
+                data = {
+                    "shows": [{
+                        "ids": {
+                            "imdb": item["ID"]
+                        },
+                        "rating": item["Rating"]
+                    }]
+                }
+                print(f"Rating TV show ({item_count} of {num_items}): {item['Title']} ({item['Year']}) with rating {item['Rating']}/10 on Trakt")
+            elif item["Type"] == "movie":
+                # This is a movie
+                data = {
+                    "movies": [{
+                        "ids": {
+                            "imdb": item["ID"]
+                        },
+                        "rating": item["Rating"]
+                    }]
+                }
+                print(f"Rating movie ({item_count} of {num_items}): {item['Title']} ({item['Year']}) with rating {item['Rating']}/10 on Trakt")
+
+            # Make the API call to rate the item
             response = requests.post(rate_url, headers=headers, json=data)
-        if response.status_code != 201:
-            print(f"Error rating {item}: {response.content}")
+            time.sleep(1)
+            while response.status_code == 429:
+                print("Rate limit exceeded. Waiting for 1 second...")
+                time.sleep(1)
+                response = requests.post(rate_url, headers=headers, json=data)
+            if response.status_code != 201:
+                print(f"Error rating {item}: {response.content}")
+
+        print('Setting Trakt Ratings Complete')
+    else:
+        print('No Trakt Ratings To Set')
 
     #Close web driver
     print("Closing webdriver...")
     driver.quit()
     service.stop()
 
 if __name__ == '__main__':
```

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/authTrakt.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/authTrakt.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/checkChromedriver.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/checkChromedriver.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/imdbRatings.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/imdbRatings.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/traktRatings.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/traktRatings.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer/verifyCredentials.py` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer/verifyCredentials.py`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/IMDbTraktSyncer.egg-info/PKG-INFO` & `IMDbTraktSyncer-1.1.0/IMDbTraktSyncer.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IMDbTraktSyncer
-Version: 1.0.9
+Version: 1.1.0
 Summary: This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.
 Home-page: https://github.com/RileyXX/IMDb-Trakt-Syncer
 Keywords: python,video,trakt,imdb,ratings,sync,movies,tv shows
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
@@ -27,23 +27,25 @@
 
 ## Update:
 `python -m pip install IMDbTraktSyncer --upgrade` in command line.
 
 ## Uninstall:
 `python -m pip uninstall IMDbTraktSyncer` in command line.
 
-## Alternative manual no install method:
-1. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and move it to the file directory of your choice.
-2. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
-3. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
-4. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
+## Alternative manual no pip install method:
+1. Install [Python](https://www.python.org/downloads/) and [Google Chrome](https://www.google.com/chrome/). _If these are already installed on your machine you can ignore this step. Please note this script does not effect Chrome in anyway it is simply required in order for chromedriver to work._
+2. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and extract it to the file directory of your choice.
+3. Login to [Trakt](https://trakt.tv/oauth/applications) and create a new API application. We will name it `IMDbTraktSyncer`. In the Redirect uri field enter `urn:ietf:wg:oauth:2.0:oob` then Save. 
+4. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
+5. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
+6. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
 
 ## Troubleshooting, known issues, workarounds & future outlook:
-* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. 
-* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work.
+* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/2
+* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/16
 * Due to IMDb's lack of API and lack of rating import ability, this script uses a rather unconventional method that mimics using a web browser to set ratings on IMDB. So there are many points of failure that could arise. I will try my best to keep the script updated as best possible.
 * If any of your details change, passwords, logins, api keys etc, just delete credentials.txt and that will reset the script. It will prompt you to enter your new details on next run.
 
 ## Screenshot:
 ![Demo](https://i.imgur.com/uydTDcg.png)
 
 
@@ -53,12 +55,13 @@
 #### More donation options:
 - Cashapp: `$rileyxx`
 - Venmo: `@rileyxx`
 - Bitcoin: `bc1qrjevwqv49z8y77len3azqfghxrjmrjvhy5zqau`
 - Amazon Wishlist: [Link ↗](https://www.amazon.com/hz/wishlist/ls/WURF5NWZ843U)
 
 ## Also posted on:
+* [PyPi](https://pypi.org/project/IMDbTraktSyncer/)
 * [Reddit](https://www.reddit.com/r/trakt/comments/132heo0/imdb_trakt_rating_syncer_tool_sync_both_ways/)
 
 <br>
 
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
```

### Comparing `IMDbTraktSyncer-1.0.9/LICENSE` & `IMDbTraktSyncer-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `IMDbTraktSyncer-1.0.9/PKG-INFO` & `IMDbTraktSyncer-1.1.0/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IMDbTraktSyncer
-Version: 1.0.9
+Version: 1.1.0
 Summary: This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.
 Home-page: https://github.com/RileyXX/IMDb-Trakt-Syncer
 Keywords: python,video,trakt,imdb,ratings,sync,movies,tv shows
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: End Users/Desktop
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
@@ -27,23 +27,25 @@
 
 ## Update:
 `python -m pip install IMDbTraktSyncer --upgrade` in command line.
 
 ## Uninstall:
 `python -m pip uninstall IMDbTraktSyncer` in command line.
 
-## Alternative manual no install method:
-1. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and move it to the file directory of your choice.
-2. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
-3. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
-4. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
+## Alternative manual no pip install method:
+1. Install [Python](https://www.python.org/downloads/) and [Google Chrome](https://www.google.com/chrome/). _If these are already installed on your machine you can ignore this step. Please note this script does not effect Chrome in anyway it is simply required in order for chromedriver to work._
+2. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and extract it to the file directory of your choice.
+3. Login to [Trakt](https://trakt.tv/oauth/applications) and create a new API application. We will name it `IMDbTraktSyncer`. In the Redirect uri field enter `urn:ietf:wg:oauth:2.0:oob` then Save. 
+4. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
+5. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
+6. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
 
 ## Troubleshooting, known issues, workarounds & future outlook:
-* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. 
-* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work.
+* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/2
+* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/16
 * Due to IMDb's lack of API and lack of rating import ability, this script uses a rather unconventional method that mimics using a web browser to set ratings on IMDB. So there are many points of failure that could arise. I will try my best to keep the script updated as best possible.
 * If any of your details change, passwords, logins, api keys etc, just delete credentials.txt and that will reset the script. It will prompt you to enter your new details on next run.
 
 ## Screenshot:
 ![Demo](https://i.imgur.com/uydTDcg.png)
 
 
@@ -53,12 +55,13 @@
 #### More donation options:
 - Cashapp: `$rileyxx`
 - Venmo: `@rileyxx`
 - Bitcoin: `bc1qrjevwqv49z8y77len3azqfghxrjmrjvhy5zqau`
 - Amazon Wishlist: [Link ↗](https://www.amazon.com/hz/wishlist/ls/WURF5NWZ843U)
 
 ## Also posted on:
+* [PyPi](https://pypi.org/project/IMDbTraktSyncer/)
 * [Reddit](https://www.reddit.com/r/trakt/comments/132heo0/imdb_trakt_rating_syncer_tool_sync_both_ways/)
 
 <br>
 
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
```

### Comparing `IMDbTraktSyncer-1.0.9/README.md` & `IMDbTraktSyncer-1.1.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -13,23 +13,25 @@
 
 ## Update:
 `python -m pip install IMDbTraktSyncer --upgrade` in command line.
 
 ## Uninstall:
 `python -m pip uninstall IMDbTraktSyncer` in command line.
 
-## Alternative manual no install method:
-1. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and move it to the file directory of your choice.
-2. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
-3. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
-4. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
+## Alternative manual no pip install method:
+1. Install [Python](https://www.python.org/downloads/) and [Google Chrome](https://www.google.com/chrome/). _If these are already installed on your machine you can ignore this step. Please note this script does not effect Chrome in anyway it is simply required in order for chromedriver to work._
+2. Download the latest .zip from the [releases page](https://github.com/RileyXX/IMDb-Trakt-Syncer/releases) and extract it to the file directory of your choice.
+3. Login to [Trakt](https://trakt.tv/oauth/applications) and create a new API application. We will name it `IMDbTraktSyncer`. In the Redirect uri field enter `urn:ietf:wg:oauth:2.0:oob` then Save. 
+4. Run `IMDbTraktSyncer.py` OR open terminal and navigate to folder where `IMDbTraktSyncer.py` is located. Run `IMDbTraktSyncer.py` in terminal. 
+5. Follow the prompts on first run. It will ask you to fill in your Trakt client id and client secret from step 3. It will also ask you to enter your IMDb username and password. Please note that these details are saved insecurely as credentials.txt in the same folder as the script. Recommended to change your password to something unique beforehand.
+6. Done. The script will continue to run and sync your ratings. This may take some time, you can follow its progress in the command line.
 
 ## Troubleshooting, known issues, workarounds & future outlook:
-* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. 
-* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work.
+* IMDb may require a captcha on login. If you see "Not signed in" appear in the script then the script will fail and the captcha is likely to be the cause. To fix this, navigate to IMDb website in your browser, preferably Chrome and from the same computer. If logged in, logout, and log back in. It may ask you to fill in a captch, complete it and finish logging in. After logging in succesfully on your browser run the script again and it should work. You may need to repeat this step once or twice if it still gives you issues. I'm looking into adding a captcha solver into the script to solve this problem, but it is currently not implemented. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/2
+* If you see an error about having the incorrect version of Chrome driver. Uninstall it by running `python -m pip uninstall chromedriver-py` in command line. In your Chrome browser navigate to Settings > About Chrome and check your version (112... or 111 etc). This would indicate you are on Chrome version 112. Navigate to [chromedriver-py releases page](https://pypi.org/project/chromedriver-py/#history) and find the latest version that is the same Chrome version (112) already on your machine. Copy the version number you need. Then in command line run `python -m pip install chromedriver-py==VERSION_NUMBER`. Replace `VERSION_NUMBER` with the version you copied and press enter. This will install the correct chromedriver version. Run the script again and it should work. https://github.com/RileyXX/IMDb-Trakt-Syncer/issues/16
 * Due to IMDb's lack of API and lack of rating import ability, this script uses a rather unconventional method that mimics using a web browser to set ratings on IMDB. So there are many points of failure that could arise. I will try my best to keep the script updated as best possible.
 * If any of your details change, passwords, logins, api keys etc, just delete credentials.txt and that will reset the script. It will prompt you to enter your new details on next run.
 
 ## Screenshot:
 ![Demo](https://i.imgur.com/uydTDcg.png)
 
 
@@ -39,12 +41,13 @@
 #### More donation options:
 - Cashapp: `$rileyxx`
 - Venmo: `@rileyxx`
 - Bitcoin: `bc1qrjevwqv49z8y77len3azqfghxrjmrjvhy5zqau`
 - Amazon Wishlist: [Link ↗](https://www.amazon.com/hz/wishlist/ls/WURF5NWZ843U)
 
 ## Also posted on:
+* [PyPi](https://pypi.org/project/IMDbTraktSyncer/)
 * [Reddit](https://www.reddit.com/r/trakt/comments/132heo0/imdb_trakt_rating_syncer_tool_sync_both_ways/)
 
 <br>
 
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
```

### Comparing `IMDbTraktSyncer-1.0.9/setup.py` & `IMDbTraktSyncer-1.1.0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 #To upload package: twine upload dist/*
 
 here = os.path.abspath(os.path.dirname(__file__))
 
 with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
     long_description = "\n" + fh.read()
 
-VERSION = '1.0.9'
+VERSION = '1.1.0'
 DESCRIPTION = 'This python script will sync user ratings for Movies and TV Shows both ways between Trakt and IMDb.'
 
 # Setting up
 setup(
     name="IMDbTraktSyncer",
     version=VERSION,
     description=DESCRIPTION,
```

