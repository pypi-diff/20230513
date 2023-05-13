# Comparing `tmp/spotON_sdk-0.0.3.8.tar.gz` & `tmp/spotON_sdk-0.0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spotON_sdk-0.0.3.8.tar", last modified: Thu May 11 10:37:12 2023, max compression
+gzip compressed data, was "spotON_sdk-0.0.4.0.tar", last modified: Sat May 13 13:05:49 2023, max compression
```

## Comparing `spotON_sdk-0.0.3.8.tar` & `spotON_sdk-0.0.4.0.tar`

### file list

```diff
@@ -1,13 +1,22 @@
--rw-r--r--   0        0        0     6178 2023-05-08 22:34:46.754824 spotON_sdk-0.0.3.8/.gitignore
--rw-r--r--   0        0        0     1085 2023-05-06 14:04:24.538041 spotON_sdk-0.0.3.8/LICENSE
--rw-r--r--   0        0        0      317 2023-05-09 09:46:50.739083 spotON_sdk-0.0.3.8/pyproject.toml
--rw-r--r--   0        0        0      447 2023-05-11 10:36:58.899925 spotON_sdk-0.0.3.8/spotON_sdk/__init__.py
--rw-r--r--   0        0        0      745 2023-05-08 10:18:24.622068 spotON_sdk-0.0.3.8/spotON_sdk/constants/bidding_zones.py
--rw-r--r--   0        0        0     4640 2023-05-11 09:12:50.539688 spotON_sdk-0.0.3.8/spotON_sdk/constants/countries.py
--rw-r--r--   0        0        0     2309 2023-05-11 09:13:15.250068 spotON_sdk-0.0.3.8/spotON_sdk/constants/markets.py
--rw-r--r--   0        0        0      714 2023-05-09 15:29:09.049429 spotON_sdk-0.0.3.8/spotON_sdk/logic/BestHour.py
--rw-r--r--   0        0        0     2880 2023-05-11 10:37:03.013307 spotON_sdk-0.0.3.8/spotON_sdk/logic/Config.py
--rw-r--r--   0        0        0     3480 2023-05-09 10:03:04.606749 spotON_sdk-0.0.3.8/spotON_sdk/logic/Entsoe_query.py
--rw-r--r--   0        0        0     1395 2023-05-09 09:59:06.668329 spotON_sdk-0.0.3.8/spotON_sdk/logic/dataframe_modifier.py
--rw-r--r--   0        0        0       94 2023-05-09 21:55:38.975092 spotON_sdk-0.0.3.8/tests/test.py
--rw-r--r--   0        0        0      250 1970-01-01 00:00:00.000000 spotON_sdk-0.0.3.8/PKG-INFO
+-rw-r--r--   0        0        0     6178 2023-05-08 22:34:46.754824 spotON_sdk-0.0.4.0/.gitignore
+-rw-r--r--   0        0        0     1085 2023-05-06 14:04:24.538041 spotON_sdk-0.0.4.0/LICENSE
+-rw-r--r--   0        0        0      317 2023-05-09 09:46:50.739083 spotON_sdk-0.0.4.0/pyproject.toml
+-rw-r--r--   0        0        0      471 2023-05-13 12:21:23.587076 spotON_sdk-0.0.4.0/spotON_sdk/__init__.py
+-rw-r--r--   0        0        0      714 2023-05-09 15:29:09.049429 spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/BestHour.py
+-rw-r--r--   0        0        0      150 2023-05-13 09:50:24.206287 spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/__init__.py
+-rw-r--r--   0        0        0     1395 2023-05-09 09:59:06.668329 spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/dataframe_modifier.py
+-rw-r--r--   0        0        0     3477 2023-05-13 09:52:05.827466 spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/entsoe_query.py
+-rw-r--r--   0        0        0     2643 2023-05-13 12:17:11.591288 spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/Config.py
+-rw-r--r--   0        0        0      163 2023-05-13 12:09:52.903536 spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/__init__.py
+-rw-r--r--   0        0        0      745 2023-05-08 10:18:24.622068 spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/bidding_zones.py
+-rw-r--r--   0        0        0     4783 2023-05-13 09:44:54.918595 spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/countries.py
+-rw-r--r--   0        0        0     2289 2023-05-13 11:25:11.404195 spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/markets.py
+-rw-r--r--   0        0        0      424 2023-05-13 12:13:49.881633 spotON_sdk-0.0.4.0/spotON_sdk/settings/Feedback/Feedback.py
+-rw-r--r--   0        0        0      122 2023-05-13 12:18:00.893425 spotON_sdk-0.0.4.0/spotON_sdk/settings/Feedback/Sensors.py
+-rw-r--r--   0        0        0      429 2023-05-13 11:38:31.810517 spotON_sdk-0.0.4.0/spotON_sdk/settings/Feedback/Units.py
+-rw-r--r--   0        0        0      132 2023-05-13 12:05:25.975505 spotON_sdk-0.0.4.0/spotON_sdk/settings/Feedback/__init__.py
+-rw-r--r--   0        0        0       64 2023-05-13 12:09:44.848658 spotON_sdk-0.0.4.0/spotON_sdk/settings/Switchtypes/Switchtypes.py
+-rw-r--r--   0        0        0       91 2023-05-13 12:09:16.378665 spotON_sdk-0.0.4.0/spotON_sdk/settings/Switchtypes/__init__.py
+-rw-r--r--   0        0        0      137 2023-05-13 12:11:13.611869 spotON_sdk-0.0.4.0/spotON_sdk/settings/__init__.py
+-rw-r--r--   0        0        0      342 2023-05-13 12:13:23.297526 spotON_sdk-0.0.4.0/spotON_sdk/spotON_controller.py
+-rw-r--r--   0        0        0      250 1970-01-01 00:00:00.000000 spotON_sdk-0.0.4.0/PKG-INFO
```

### Comparing `spotON_sdk-0.0.3.8/.gitignore` & `spotON_sdk-0.0.4.0/.gitignore`

 * *Files identical despite different names*

### Comparing `spotON_sdk-0.0.3.8/LICENSE` & `spotON_sdk-0.0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/constants/bidding_zones.py` & `spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/bidding_zones.py`

 * *Files identical despite different names*

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/constants/countries.py` & `spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/countries.py`

 * *Files 4% similar despite different names*

```diff
@@ -54,42 +54,44 @@
     If no such object is found, returns None.
     """
     for country in countries:
         if country.country_name == country_name:
             return country
     return None
 
-Austria = Country(capital="Vienna", country_code="AT", country_name="Austria")
-Belgium = Country(capital="Brussels", country_code="BE", country_name="Belgium")
-Bulgaria = Country(capital="Sofia", country_code="BG", country_name="Bulgaria")
-Croatia = Country(capital="Zagreb", country_code="HR", country_name="Croatia")
-Cyprus = Country(capital="Nicosia", country_code="CY", country_name="Cyprus")
-Czech_republic = Country(capital="Prague", country_code="CZ", country_name="Czech Republic")
-Denmark = Country(capital="Copenhagen", country_code="DK", country_name="Denmark")
-Estonia = Country(capital="Tallinn", country_code="EE", country_name="Estonia")
-Finland = Country(capital="Helsinki", country_code="FI", country_name="Finland")
-France = Country(capital="Paris", country_code="FR", country_name="France")
-Germany = Country(capital="Berlin", country_code="DE", country_name="Germany")
-Greece = Country(capital="Athens", country_code="GR", country_name="Greece")
-Hungary = Country(capital="Budapest", country_code="HU", country_name="Hungary")
-Ireland = Country(capital="Dublin", country_code="IE", country_name="Ireland")
-Italy = Country(capital="Rome", country_code="IT", country_name="Italy")
-Latvia = Country(capital="Riga", country_code="LV", country_name="Latvia")
-Lithuania = Country(capital="Vilnius", country_code="LT", country_name="Lithuania")
-Luxembourg = Country(capital="Luxembourg", country_code="LU", country_name="Luxembourg")
-Netherlands = Country(capital="Amsterdam", country_code="NL", country_name="Netherlands")
-Poland = Country(capital="Warsaw", country_code="PL", country_name="Poland")
-Portugal = Country(capital="Lisbon", country_code="PT", country_name="Portugal")
-Romania = Country(capital="Bucharest", country_code="RO", country_name="Romania")
-Slovakia = Country(capital="Bratislava", country_code="SK", country_name="Slovakia")
-Slovenia = Country(capital="Ljubljana", country_code="SI", country_name="Slovenia")
-Spain = Country(capital="Madrid", country_code="ES", country_name="Spain")
-Sweden = Country(capital="Stockholm", country_code="SE", country_name="Sweden")
+@dataclass
+class all_Countries():
+    Austria = Country(capital="Vienna", country_code="AT", country_name="Austria")
+    Belgium = Country(capital="Brussels", country_code="BE", country_name="Belgium")
+    Bulgaria = Country(capital="Sofia", country_code="BG", country_name="Bulgaria")
+    Croatia = Country(capital="Zagreb", country_code="HR", country_name="Croatia")
+    Cyprus = Country(capital="Nicosia", country_code="CY", country_name="Cyprus")
+    Czech_republic = Country(capital="Prague", country_code="CZ", country_name="Czech Republic")
+    Denmark = Country(capital="Copenhagen", country_code="DK", country_name="Denmark")
+    Estonia = Country(capital="Tallinn", country_code="EE", country_name="Estonia")
+    Finland = Country(capital="Helsinki", country_code="FI", country_name="Finland")
+    France = Country(capital="Paris", country_code="FR", country_name="France")
+    Germany = Country(capital="Berlin", country_code="DE", country_name="Germany")
+    Greece = Country(capital="Athens", country_code="GR", country_name="Greece")
+    Hungary = Country(capital="Budapest", country_code="HU", country_name="Hungary")
+    Ireland = Country(capital="Dublin", country_code="IE", country_name="Ireland")
+    Italy = Country(capital="Rome", country_code="IT", country_name="Italy")
+    Latvia = Country(capital="Riga", country_code="LV", country_name="Latvia")
+    Lithuania = Country(capital="Vilnius", country_code="LT", country_name="Lithuania")
+    Luxembourg = Country(capital="Luxembourg", country_code="LU", country_name="Luxembourg")
+    Netherlands = Country(capital="Amsterdam", country_code="NL", country_name="Netherlands")
+    Poland = Country(capital="Warsaw", country_code="PL", country_name="Poland")
+    Portugal = Country(capital="Lisbon", country_code="PT", country_name="Portugal")
+    Romania = Country(capital="Bucharest", country_code="RO", country_name="Romania")
+    Slovakia = Country(capital="Bratislava", country_code="SK", country_name="Slovakia")
+    Slovenia = Country(capital="Ljubljana", country_code="SI", country_name="Slovenia")
+    Spain = Country(capital="Madrid", country_code="ES", country_name="Spain")
+    Sweden = Country(capital="Stockholm", country_code="SE", country_name="Sweden")
 
-countries = [Austria, Belgium, Bulgaria, Croatia, Cyprus, Czech_republic, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Italy, Latvia, Lithuania, Luxembourg, Netherlands, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden]
+    return_List= [Austria, Belgium, Bulgaria, Croatia, Cyprus, Czech_republic, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Italy, Latvia, Lithuania, Luxembourg, Netherlands, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden]
 
 
 
 
 def return_All_Areas(filterstring:str ="MBA"):
         
     result = []
```

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/constants/markets.py` & `spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/markets.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,13 @@
 from dataclasses import dataclass
 from entsoe import Area
-import pandas as pd
 
 import pandas as pd
 from dataclasses import dataclass, field
 from typing import Optional, Dict,Any
-import pytz
 
 from typing import List
 from .countries import *
 from .bidding_zones import bidding_zones
 
 @dataclass
 class Market():
@@ -23,15 +21,15 @@
 
     def __post_init__(self):
         self.area_code = self.area.name
         country_region = self.area_code.split("_")
         self.country_code = country_region[0]
         if len(country_region) >=2:
             self.region_code = country_region[1]
-        print (self.area_code)
+
         try:
             city_List = bidding_zones[self.area_code]["cities"]
             my_string = ', '.join(city_List)
             self.cities = my_string
         except:
             self.cities = ""
 
@@ -39,18 +37,18 @@
         self.name = f"{self.country.emoji} {self.country.country_name} {self.area_code} {self.cities}"
         self.name = f"{self.country.emoji} {self.country.country_name}"
 
         #self.get_Market_by_area_code(self.area.name)
 
 dataclass
 class Markets():
-    austria = Market(Area.AT,Austria)
-    germany = Market(Area.DE_LU,Germany,alias="DE_LU")
+    austria = Market(Area.AT,all_Countries.Austria)
+    germany = Market(Area.DE_LU,all_Countries.Germany,alias="DE_LU")
     #luxembourg = Market(Area.DE_LU,Luxembourg)
-    sweden1 = Market(Area.SE_1,Sweden)
+    sweden1 = Market(Area.SE_1,all_Countries.Sweden)
     #sweden2 = Market(Area.SE_2,Sweden)
     #sweden3 = Market(Area.SE_3,Sweden)
     #sweden4 = Market(Area.SE_4,Sweden)
     markets_List = [value for key, value in vars().items() if isinstance(value, Market)]
     merged_Markets = []
 
     @staticmethod
```

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/logic/BestHour.py` & `spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/BestHour.py`

 * *Files identical despite different names*

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/logic/Config.py` & `spotON_sdk-0.0.4.0/spotON_sdk/settings/Config/Config.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,14 +1,11 @@
 from dataclasses import dataclass,field
 from typing import List
 
-from ..constants.markets import Market
-class Switchtypes():
-    switch = "Switch"
-    dimmer = "Dimmer"
+from .markets import Market
 
 
 class PeriodTypes():
     wholeDay :str = "24h Hour Period"
     timeFrame :str = "Timeframe"
 
 @dataclass
@@ -19,20 +16,20 @@
             return "<br> 🚨 <mark> Your Timeframe is SHORTER than your desired ON Time</mark> "
         else:
             return ""
 
 
 @dataclass
 class Config():
-    switchtype :Switchtypes
     nr_of_Hours_On :int
     uninterrupted :bool
     market : Market 
     timeframe :List[List[int]] 
     periodType : PeriodTypes| str = field(default="")
+    dayframe: List[int] | None = field(default=None,init=False) 
     bestHour :str = ""
     week: int = 100
     timeFrameValidation = TimeFrameValidation(False)
 
     def __post_init__(self):
         def check_nr_of_Hours_not_0():
             if self.nr_of_Hours_On < 1:
@@ -40,31 +37,30 @@
 
         def check_TimeFrame_is_large_enogh():
             if len(self.find_Possible_Hours()) > self.nr_of_Hours_On:
                 self.timeFrameValidation = TimeFrameValidation(True)
             else:
                 self.timeFrameValidation = TimeFrameValidation(False)
         
-        def checkLogic():
+        def checkConfig():
             if self.uninterrupted:
                 if len(self.timeframe) > 1:
                     raise ValueError(f"Hey your Timeframe has the Attribute of Beeing uninterruped means you can't have multiple timeframes")
-            if self.switchtype == Switchtypes.switch and self.nr_of_Hours_On == 24:
-                raise ValueError(f"Hey if it Should be on for {self.nr_of_Hours_On} there is no need for switching")
+
 
 
         def check_Overlapping_Arrays():
             possible_Hours = self.find_Possible_Hours()
             if(len(set(possible_Hours)) != len(possible_Hours)):
                 raise ValueError(f"Hey your Timeframes {self.timeframe} have overlapping Hours. Reduce it to one")
             
         
         check_nr_of_Hours_not_0()
         check_TimeFrame_is_large_enogh()
-        checkLogic()
+        checkConfig()
         #check_Overlapping_Arrays()
         
     def find_Possible_Hours(self):
         possible_Hours = []
         for timeframe in self.timeframe:
             start,end = timeframe[0],timeframe[1]
             def loop_Hours(_start,_end):
```

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/logic/Entsoe_query.py` & `spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/entsoe_query.py`

 * *Files 0% similar despite different names*

```diff
@@ -94,15 +94,15 @@
     start,end,CET_Difference = getTimeStamps(country_code,tomorrow,overrideTime,query_Month)
     
     print (f"{start=}   {end=}  {CET_Difference=}")
     try:
         series = client.query_day_ahead_prices(country_code,start=start,end=end)
         return series,CET_Difference
     except NoMatchingDataError as e:
-        print(f"No Values to fetch is {start=}   {end=}  {CET_Difference=} \n Is it before 13:30 UTC?","NoMatchingDataError occurred:", str(e))
+        print(f"No Values to fetch {start=}   {end=}  {CET_Difference=} \n Is it before 13:30 UTC?","NoMatchingDataError occurred:", str(e))
         
 
 
 def create_Dataframe(s:pd.Series,market:Market):
 
     # Convert series to dataframe
     df = s.to_frame()
```

### Comparing `spotON_sdk-0.0.3.8/spotON_sdk/logic/dataframe_modifier.py` & `spotON_sdk-0.0.4.0/spotON_sdk/data_helpers/dataframe_modifier.py`

 * *Files identical despite different names*

