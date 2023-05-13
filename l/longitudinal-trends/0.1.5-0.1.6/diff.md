# Comparing `tmp/longitudinal_trends-0.1.5.tar.gz` & `tmp/longitudinal_trends-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "longitudinal_trends-0.1.5.tar", last modified: Fri May  5 12:48:29 2023, max compression
+gzip compressed data, was "longitudinal_trends-0.1.6.tar", last modified: Sat May 13 10:28:05 2023, max compression
```

## Comparing `longitudinal_trends-0.1.5.tar` & `longitudinal_trends-0.1.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-05 12:48:29.638960 longitudinal_trends-0.1.5/
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)     1104 2023-03-18 15:04:53.000000 longitudinal_trends-0.1.5/LICENSE
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)       34 2023-03-18 16:38:44.000000 longitudinal_trends-0.1.5/MANIFEST.in
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)    10290 2023-05-05 12:48:29.638960 longitudinal_trends-0.1.5/PKG-INFO
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)     9719 2023-05-05 08:12:31.000000 longitudinal_trends-0.1.5/README.md
-drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-05 12:48:29.328949 longitudinal_trends-0.1.5/longitudinal_trends/
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)    17391 2023-05-05 12:47:53.000000 longitudinal_trends-0.1.5/longitudinal_trends/__init__.py
-drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-05 12:48:29.576063 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)    10290 2023-05-05 12:48:28.000000 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/PKG-INFO
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)      307 2023-05-05 12:48:29.000000 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/SOURCES.txt
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)        1 2023-05-05 12:48:28.000000 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/dependency_links.txt
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)       45 2023-05-05 12:48:28.000000 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/requires.txt
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)       20 2023-05-05 12:48:28.000000 longitudinal_trends-0.1.5/longitudinal_trends.egg-info/top_level.txt
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)     1141 2023-05-05 12:48:06.000000 longitudinal_trends-0.1.5/pyproject.toml
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)       44 2023-04-15 18:04:14.000000 longitudinal_trends-0.1.5/requirements.txt
--rwxrwxrwx   0 msakir    (1000) msakir    (1000)       38 2023-05-05 12:48:29.638960 longitudinal_trends-0.1.5/setup.cfg
+drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-13 10:28:05.799192 longitudinal_trends-0.1.6/
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)     1104 2023-03-18 15:04:53.000000 longitudinal_trends-0.1.6/LICENSE
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)       34 2023-03-18 16:38:44.000000 longitudinal_trends-0.1.6/MANIFEST.in
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)    10290 2023-05-13 10:28:05.792192 longitudinal_trends-0.1.6/PKG-INFO
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)     9719 2023-05-05 08:12:31.000000 longitudinal_trends-0.1.6/README.md
+drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-13 10:28:05.445888 longitudinal_trends-0.1.6/longitudinal_trends/
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)    17774 2023-05-13 10:20:57.000000 longitudinal_trends-0.1.6/longitudinal_trends/__init__.py
+drwxrwxrwx   0 msakir    (1000) msakir    (1000)        0 2023-05-13 10:28:05.725513 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)    10290 2023-05-13 10:28:04.000000 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/PKG-INFO
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)      307 2023-05-13 10:28:05.000000 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/SOURCES.txt
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)        1 2023-05-13 10:28:04.000000 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/dependency_links.txt
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)       45 2023-05-13 10:28:04.000000 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/requires.txt
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)       20 2023-05-13 10:28:04.000000 longitudinal_trends-0.1.6/longitudinal_trends.egg-info/top_level.txt
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)     1141 2023-05-13 10:26:02.000000 longitudinal_trends-0.1.6/pyproject.toml
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)       44 2023-04-15 18:04:14.000000 longitudinal_trends-0.1.6/requirements.txt
+-rwxrwxrwx   0 msakir    (1000) msakir    (1000)       38 2023-05-13 10:28:05.802196 longitudinal_trends-0.1.6/setup.cfg
```

### Comparing `longitudinal_trends-0.1.5/LICENSE` & `longitudinal_trends-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `longitudinal_trends-0.1.5/PKG-INFO` & `longitudinal_trends-0.1.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: longitudinal_trends
-Version: 0.1.5
+Version: 0.1.6
 Summary: Generate long-term longitudinal Google Trends Data
 Author: Mohammad Saleh Ahsan Sakir, Taeyong Park
 Author-email: ahsansakir506@gmail.com, taeyongp@andrew.cmu.edu
 License: MIT
 Project-URL: homepage, https://github.com/Mohammad-sakir/longitudinalTrends
 Keywords: longitudinal-trends longitudinal data python google-trends-api google-trends search-data
 Classifier: Programming Language :: Python :: 3
```

### Comparing `longitudinal_trends-0.1.5/README.md` & `longitudinal_trends-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `longitudinal_trends-0.1.5/longitudinal_trends/__init__.py` & `longitudinal_trends-0.1.6/longitudinal_trends/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -108,29 +108,30 @@
         
 
     # This method is intended to create necessary directories at each discretion
     def __create_required_directory(self, folder):
         if not os.path.exists(folder):
             os.mkdir(folder)
 
+
     # This method provides list of time periods to fetch data for
     def __determine_time_periods(self):
         timeperiod = ceil(self.__num_of_days/self.TIME_WINDOW)
 
         self.__times = [self.start_date + dt.timedelta(days=x*self.TIME_WINDOW) for x in range(0, timeperiod+1)]
         self.__times[-1] = self.end_date
 
 
-    def cross_section(self, geo="", resolution="COUNTRY"):
+    def cross_section(self, geo: str="", resolution: str="COUNTRY"):
         self.__logger.info("Collecting Cross Section Data now")
 
         res = ["COUNTRY", "REGION", "CITY"]
-        if not geo.strip() or resolution not in res:
+        if (not geo.strip() and resolution != "COUNTRY") or (geo.strip() and resolution not in res):
             self.__logger.info("Incorrect Resolution Provided. Defaulting to 'COUNTRY'")
-            resolution = "COUNTRY"
+            resolution = "COUNTRY"    
 
         self.__create_required_directory("{}/{}/by_region".format(self.folder_name, self.data_format))
 
         if self.data_format == 'daily':
             chng_delta = relativedelta(days=1)
             end_delta = relativedelta(days=0)
             form = 'day'
@@ -152,28 +153,30 @@
         with console.status("Collecting Data...") as stats:
             while True:
                 if (self.data_format == 'weekly' and current_time >= self.end_date) or (self.data_format != 'weekly' and current_time > self.end_date):
                     stats.stop()
                     break
 
                 current_end_time = current_time + end_delta
-                if os.path.exists("{}/{}/by_region/{}-{}-{}_{}.csv".format(self.folder_name, self.data_format, current_time.strftime("%Y%m%d"), current_end_time.strftime("%Y%m%d"), form, i)):
+                # print("{}/{}/by_region/{}_{}-{}-{}.csv".format(self.folder_name, self.data_format,  form, i+1, current_time.strftime("%Y%m%d"), current_end_time.strftime("%Y%m%d")))
+                if os.path.exists("{}/{}/by_region/{}_{}-{}-{}.csv".format(self.folder_name, self.data_format,  form, i+1, current_time.strftime("%Y%m%d"), current_end_time.strftime("%Y%m%d"))):
                         self.__logger.info("Data for {}-{} already collected. Moving to next date...".format(current_time.strftime("%#d/%m/%#Y"), current_end_time.strftime("%#d/%m/%#Y")), extra={"markup": True})
                         current_time += chng_delta
                         i += 1
                 else:
                     try:
                         self.__pytrend.build_payload(kw_list=[self.topic], geo=geo, 
                                                         timeframe='%s %s' % (current_time.strftime("%Y-%m-%d"), current_end_time.strftime("%Y-%m-%d"))) 
                         time.sleep(5)
                         df = self.__pytrend.interest_by_region(resolution=resolution, inc_geo_code=True, inc_low_vol=True)
                         df = df.rename(columns={self.topic:self.keyword})
                         i += 1
                     except ResponseError as e:
-
+                        #TODO: Throw error for status code 500
+                        #TODO: Save errors in a file
                         self.__logger.info("Please have patience as we reset rate limit ... ", extra={"markup": True})
                         time.sleep(5)
                         continue
                     except:
                         stats.stop() # Stop the animation
                         if not self.__in_notebook():
                             self.__logger.error("[bold red]Whoops![/]", exc_info=1, extra={"markup": True})
@@ -188,15 +191,15 @@
 
                     current_time += chng_delta
 
             self.__logger.info("[bold green]Successfully Collected Required Data![/]", extra={"markup": True})
 
 
     # Time Series Data collection method for 'monthly'
-    def __time_series_monthly(self, stats, reference_geo_code="US"):
+    def __time_series_monthly(self, stats, reference_geo_code: str="US"):
         if os.path.exists("{}/{}/over_time/{}/{}-{}.csv".format(self.folder_name, self.data_format, reference_geo_code, self.start_date.strftime("%Y%m%d"), self.end_date.strftime("%Y%m%d"))):
             stats.stop()
             self.__logger.info("All Data for current request is already collected", extra={"markup": True})
         else:
             try:
                 self.__pytrend.build_payload(kw_list=[self.topic], geo=reference_geo_code, 
                                     timeframe='%s %s' % (self.start_date.strftime("%Y-%m-%d"), self.end_date.strftime("%Y-%m-%d"))) 
@@ -211,15 +214,15 @@
                 time.sleep(5)
             except:
                 stats.stop()
                 self.__logger.error("[bold red]Whoops![/]", exc_info=1, extra={"markup": True})
 
 
     # Time Series Data collection method for 'weekly'/'daily'
-    def __time_series_nmonthly(self, stats, reference_geo_code="US"):
+    def __time_series_nmonthly(self, stats, reference_geo_code: str="US"):
         for period in range(len(self.__times)-1):
             start, end = self.__times[period], self.__times[period+1]
 
             if self.data_format == "weekly":
                 num_days = (end - start).days
                 if num_days < 270:
                     stats.stop()
@@ -248,15 +251,15 @@
                     self.__logger.info("No Data was returned for period: {} -> '{}' to '{}'".format(period+1, start.strftime("%#d/%m/%#Y"), end.strftime("%#d/%m/%#Y")), extra={"markup": True})
                 else:                    
                     df = df.rename(columns={self.topic:self.keyword})
                     df.drop('isPartial', axis=1, inplace=True)
                     df.to_csv("{}/{}/over_time/{}/{}-{}-{}.csv".format(self.folder_name, self.data_format, reference_geo_code, period+1, start.strftime("%Y%m%d"), end.strftime("%Y%m%d")))
 
 
-    def time_series(self, reference_geo_code="US"):
+    def time_series(self, reference_geo_code: str="US"):
         """
             reference_geo_code: Reference reference_geo_code code for Country/State/City. Eg, 'US-Al' for Alabama state of united states.
             *** If unsure of reference_geo_code, run 'cross_section' function as it will give the reference_geo_code Codes of the desired level ***
         """
         with console.status("Collecting Data...") as stats:
             self.__logger.info("Collecting Over Time Data now", extra={"markup": True})
```

### Comparing `longitudinal_trends-0.1.5/longitudinal_trends.egg-info/PKG-INFO` & `longitudinal_trends-0.1.6/longitudinal_trends.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: longitudinal-trends
-Version: 0.1.5
+Version: 0.1.6
 Summary: Generate long-term longitudinal Google Trends Data
 Author: Mohammad Saleh Ahsan Sakir, Taeyong Park
 Author-email: ahsansakir506@gmail.com, taeyongp@andrew.cmu.edu
 License: MIT
 Project-URL: homepage, https://github.com/Mohammad-sakir/longitudinalTrends
 Keywords: longitudinal-trends longitudinal data python google-trends-api google-trends search-data
 Classifier: Programming Language :: Python :: 3
```

### Comparing `longitudinal_trends-0.1.5/pyproject.toml` & `longitudinal_trends-0.1.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]#, "setuptools-scm"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "longitudinal_trends"
-version='0.1.5'
+version='0.1.6'
 description="Generate long-term longitudinal Google Trends Data"
 urls = {homepage = "https://github.com/Mohammad-sakir/longitudinalTrends"}
 requires-python = ">=3.7"
 authors = [
     {name = "Mohammad Saleh Ahsan Sakir"},
     {name = "Taeyong Park"}, 
     {email="ahsansakir506@gmail.com"},
```

