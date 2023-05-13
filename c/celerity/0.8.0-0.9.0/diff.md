# Comparing `tmp/celerity-0.8.0.tar.gz` & `tmp/celerity-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "celerity-0.8.0.tar", max compression
+gzip compressed data, was "celerity-0.9.0.tar", max compression
```

## Comparing `celerity-0.8.0.tar` & `celerity-0.9.0.tar`

### file list

```diff
@@ -1,16 +1,17 @@
--rw-r--r--   0        0        0     1075 2023-05-09 15:28:31.467559 celerity-0.8.0/LICENSE
--rw-r--r--   0        0        0     5469 2023-05-09 15:28:31.467559 celerity-0.8.0/README.md
--rw-r--r--   0        0        0     1846 2023-05-09 15:28:31.471561 celerity-0.8.0/pyproject.toml
--rw-r--r--   0        0        0      133 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/__init__.py
--rw-r--r--   0        0        0     2418 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/astrometry.py
--rw-r--r--   0        0        0      240 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/common.py
--rw-r--r--   0        0        0      997 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/constants.py
--rw-r--r--   0        0        0     1354 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/coordinates.py
--rw-r--r--   0        0        0      632 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/earth.py
--rw-r--r--   0        0        0      468 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/epoch.py
--rw-r--r--   0        0        0     4394 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/moon.py
--rw-r--r--   0        0        0     2049 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/seeing.py
--rw-r--r--   0        0        0     4066 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/sun.py
--rw-r--r--   0        0        0     4125 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/temporal.py
--rw-r--r--   0        0        0      961 2023-05-09 15:28:31.471561 celerity-0.8.0/src/celerity/utilities.py
--rw-r--r--   0        0        0     6102 1970-01-01 00:00:00.000000 celerity-0.8.0/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-05-10 14:08:31.794523 celerity-0.9.0/LICENSE
+-rw-r--r--   0        0        0     5469 2023-05-10 14:08:31.794523 celerity-0.9.0/README.md
+-rw-r--r--   0        0        0     1846 2023-05-10 14:08:31.794523 celerity-0.9.0/pyproject.toml
+-rw-r--r--   0        0        0      133 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/__init__.py
+-rw-r--r--   0        0        0     3274 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/astrometry.py
+-rw-r--r--   0        0        0     1096 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/common.py
+-rw-r--r--   0        0        0     1733 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/constants.py
+-rw-r--r--   0        0        0     1974 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/coordinates.py
+-rw-r--r--   0        0        0     1252 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/earth.py
+-rw-r--r--   0        0        0     1088 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/epoch.py
+-rw-r--r--   0        0        0     7609 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/moon.py
+-rw-r--r--   0        0        0     2905 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/seeing.py
+-rw-r--r--   0        0        0     6599 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/sun.py
+-rw-r--r--   0        0        0     5217 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/temporal.py
+-rw-r--r--   0        0        0     1796 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/transit.py
+-rw-r--r--   0        0        0     1583 2023-05-10 14:08:31.794523 celerity-0.9.0/src/celerity/utilities.py
+-rw-r--r--   0        0        0     6102 1970-01-01 00:00:00.000000 celerity-0.9.0/PKG-INFO
```

### Comparing `celerity-0.8.0/LICENSE` & `celerity-0.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `celerity-0.8.0/README.md` & `celerity-0.9.0/README.md`

 * *Files identical despite different names*

### Comparing `celerity-0.8.0/pyproject.toml` & `celerity-0.9.0/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "celerity"
-version = "0.8.0"
+version = "0.9.0"
 description = "Celerity is a lightweight, zero-dependency and type-safe Python library for astronomical calculations."
 authors = [
     "Michael J. Roberts <michael@observerly.com>"
 ]
 maintainers = [
     "Michael J. Roberts <michael@observerly.com>"
 ]
```

### Comparing `celerity-0.8.0/src/celerity/astrometry.py` & `celerity-0.9.0/src/celerity/astrometry.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,13 +1,23 @@
+# *****************************************************************************************************************
+
+# @author         Michael Roberts <michael@observerly.com>
+# @package        @observerly/celerity
+# @license        Copyright © 2021-2023 observerly
+
+# *****************************************************************************************************************
+
 from datetime import datetime
 from math import atan2, cos, degrees, pow, radians, sin, tan
 
 from .common import EquatorialCoordinate, GeographicCoordinate
 from .temporal import get_julian_date, get_local_sidereal_time
 
+# *****************************************************************************************************************
+
 
 def get_hour_angle(date: datetime, ra: float, longitude: float) -> float:
     """
     Gets the hour angle for a particular object for a particular observer at a given datetime
 
     :param date: The datetime object to convert.
     :param ra: The right ascension of the observed object's equatorial coordinate in degrees.
@@ -21,14 +31,17 @@
     # If the hour angle is less than zero, ensure we rotate by 2π radians (360 degrees)
     if ha < 0:
         ha += 360
 
     return ha
 
 
+# *****************************************************************************************************************
+
+
 def get_obliquity_of_the_ecliptic(date: datetime) -> float:
     """
     Gets the obliquity of the ecliptic for a particular datetime
 
     The obliquity of the ecliptic is the angle between the ecliptic and the celestial equator, and is used to
     convert between ecliptic and equatorial coordinates.
 
@@ -41,14 +54,17 @@
     # Calculate the number of centuries since J2000.0:
     T = (JD - 2451545.0) / 36525
 
     # Calculate the obliquity of the ecliptic:
     return 23.439292 - (46.845 * T + 0.00059 * pow(T, 2) + 0.001813 * pow(T, 3)) / 3600
 
 
+# *****************************************************************************************************************
+
+
 def get_parallactic_angle(
     date: datetime,
     observer: GeographicCoordinate,
     target: EquatorialCoordinate,
 ) -> float:
     """
     Gets the parallactic angle for a particular object for a particular observer at a given datetime
@@ -68,7 +84,10 @@
     # Calculate the parallactic angle and return in degrees:
     return degrees(
         atan2(
             sin(ha),
             tan(lat) * cos(dec) - sin(dec) * cos(ha),
         )
     )
+
+
+# *****************************************************************************************************************
```

### Comparing `celerity-0.8.0/src/celerity/coordinates.py` & `celerity-0.9.0/src/celerity/coordinates.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,13 +1,23 @@
+# *****************************************************************************************************************
+
+# @author         Michael Roberts <michael@observerly.com>
+# @package        @observerly/celerity
+# @license        Copyright © 2021-2023 observerly
+
+# *****************************************************************************************************************
+
 from datetime import datetime
 from math import acos, asin, cos, degrees, radians, sin
 
 from .astrometry import get_hour_angle
 from .common import EquatorialCoordinate, GeographicCoordinate, HorizontalCoordinate
 
+# *****************************************************************************************************************
+
 
 def convert_equatorial_to_horizontal(
     date: datetime,
     observer: GeographicCoordinate,
     target: EquatorialCoordinate,
 ) -> HorizontalCoordinate:
     """
@@ -35,7 +45,10 @@
 
     az = acos((sin(dec) - sin(alt) * sin(lat)) / (cos(alt) * cos(lat)))
 
     return {
         "az": 360 - degrees(az) if sin(ha) > 0 else degrees(az),
         "alt": degrees(alt),
     }
+
+
+# *****************************************************************************************************************
```

### Comparing `celerity-0.8.0/src/celerity/seeing.py` & `celerity-0.9.0/src/celerity/seeing.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,9 +1,19 @@
+# *****************************************************************************************************************
+
+# @author         Michael Roberts <michael@observerly.com>
+# @package        @observerly/celerity
+# @license        Copyright © 2021-2023 observerly
+
+# *****************************************************************************************************************
+
 from math import pow, radians, sin
 
+# *****************************************************************************************************************
+
 
 def get_airmass(altitude: float) -> float:
     """
     Gets the airmass of an object at a given altitude using Pickering's formula.
 
     Airmass is a measure of the amount of air along the line of sight when observing a star
     or other celestial source from below Earth's atmosphere. It is formulated
@@ -12,14 +22,17 @@
     :see: Pickering, K. A. (2002). "The Southern Limits of the Ancient Star Catalog" (PDF). DIO. 12 (1): 20-39.
     :param: altitude: The altitude of the object in degrees.
     :return: The airmass of the object.
     """
     return get_airmass_pickering(altitude)
 
 
+# *****************************************************************************************************************
+
+
 def get_airmass_pickering(altitude: float) -> float:
     """
     Gets the airmass of an object at a given altitude using Pickering's formula.
 
     Airmass is a measure of the amount of air along the line of sight when observing a star
     or other celestial source from below Earth's atmosphere. It is formulated
     as the integral of air density along the light ray.
@@ -27,20 +40,26 @@
     :see: Pickering, K. A. (2002). "The Southern Limits of the Ancient Star Catalog" (PDF). DIO. 12 (1): 20-39.
     :param: altitude: The altitude of the object in degrees.
     :return: The airmass of the object.
     """
     return 1 / sin(radians(altitude + 244 / (165 + (47 * pow(altitude, 1.1)))))
 
 
+# *****************************************************************************************************************
+
+
 def get_airmass_karstenyoung(altitude: float) -> float:
     """
     Gets the airmass of an object at a given altitude using Karsten & Young's formula.
 
     Airmass is a measure of the amount of air along the line of sight when observing a star
     or other celestial source from below Earth's atmosphere. It is formulated
     as the integral of air density along the light ray.
 
     :see: Kasten, F.; Young, A. T. (1989). "Revised optical air mass tables and approximation formula". Applied Optics. 28 (22): 4735-4738.
     :param: altitude: The altitude of the object in degrees.
     :return: The airmass of the object.
     """
     return 1 / (sin(radians(altitude)) + 0.50572 * pow(altitude + 6.07995, -1.6364))
+
+
+# *****************************************************************************************************************
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `celerity-0.8.0/src/celerity/sun.py` & `celerity-0.9.0/src/celerity/sun.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,12 +1,24 @@
+# *****************************************************************************************************************
+
+# @author         Michael Roberts <michael@observerly.com>
+# @package        @observerly/celerity
+# @license        Copyright © 2021-2023 observerly
+
+# *****************************************************************************************************************
+
 from datetime import datetime
-from math import pow, radians, sin
+from math import asin, atan2, cos, degrees, pow, radians, sin
 
+from .astrometry import get_obliquity_of_the_ecliptic
+from .common import EquatorialCoordinate
 from .temporal import get_julian_date
 
+# *****************************************************************************************************************
+
 
 def get_equation_of_center(date) -> float:
     """
     The equation of center is the difference between the mean geometric longitude
     and the mean anomaly.
 
     :param date: The datetime object to convert.
@@ -27,14 +39,17 @@
         + (0.019993 - 0.000101 * pow(T, 2)) * sin(radians(2 * M))
         + 0.000289 * sin(radians(3 * M))
     )
 
     return C
 
 
+# *****************************************************************************************************************
+
+
 def get_mean_anomaly(date: datetime) -> float:
     """
     The mean anomaly is the angle between the perihelion and the current position
     of the planet, as seen from the Sun.
 
     :param date: The datetime object to convert.
     :return: The mean anomaly in degrees.
@@ -51,14 +66,17 @@
     # Correct for negative angles
     if M < 0:
         M += 360
 
     return M
 
 
+# *****************************************************************************************************************
+
+
 def get_mean_geometric_longitude(date: datetime) -> float:
     """
     The mean geometric longitude for the Sun is the angle between the perihelion
     and the current position of the Sun, as seen from the centre of the Earth.
 
     :param date: The datetime object to convert.
     :return: The mean geometric longitude in degrees.
@@ -75,14 +93,17 @@
     # Correct for negative angles
     if L < 0:
         L += 360
 
     return L
 
 
+# *****************************************************************************************************************
+
+
 def get_true_anomaly(date: datetime) -> float:
     """
     The true anomaly for the Sun is the angle between the perihelion and the
     current position of the Sun, as seen from the centre of the Earth, corrected
     for the equation of center.
 
     :param date: The datetime object to convert.
@@ -94,14 +115,17 @@
     # Get the equation of center:
     C = get_equation_of_center(date)
 
     # Correct the mean anomaly for the equation of center:
     return (M + C) % 360
 
 
+# *****************************************************************************************************************
+
+
 def get_true_geometric_longitude(date: datetime) -> float:
     """
     The true geometric longitude for the Sun is the angle between the perihelion
     and the current position of the Sun, as seen from the centre of the Earth,
     corrected for the equation of center.
 
     :param date: The datetime object to convert.
@@ -113,14 +137,17 @@
     # Get the equation of center:
     C = get_equation_of_center(date)
 
     # Correct the mean geometric longitude for the equation of center:
     return (L + C) % 360
 
 
+# *****************************************************************************************************************
+
+
 def get_ecliptic_longitude(date: datetime) -> float:
     """
     The ecliptic longitude for the Sun is the angle between the perihelion and
     the current position of the Sun, as seen from the centre of the Earth,
     corrected for the equation of center and the Sun's ecliptic longitude at
     perigee at the epoch.
 
@@ -135,7 +162,46 @@
     λ = ν + 282.938346 % 360
 
     # Correct for negative angles
     if λ < 0:
         λ += 360
 
     return λ
+
+
+# *****************************************************************************************************************
+
+
+def get_equatorial_coordinate(date: datetime) -> EquatorialCoordinate:
+    """
+    The equatorial coordinate of the Sun is the standard equatorial coordinate
+    of the Sun, as seen from the centre of the Earth, corrected for the equation
+    of center and the Sun's ecliptic longitude at perigee at the epoch.
+
+    :param date: The datetime object to convert.
+    :return: The equatorial coordinate in degrees.
+    """
+    # Get the ecliptic longitude:
+    λ = radians(get_ecliptic_longitude(date))
+
+    # Get the ecliptic latitude:
+    # This term is zero for the Sun, so we can largely ignore it by refactoring
+    # the standard equations for the conversion between ecliptic and equatorial
+    # coordinates.
+    # β = 0
+
+    # Get the obliquity of the ecliptic:
+    ε = radians(get_obliquity_of_the_ecliptic(date))
+
+    # Get the corresponding Right Ascension, α:
+    ra = degrees(atan2(sin(λ) * cos(ε), cos(λ))) % 360
+
+    # Correct ra for negative angles
+    if ra < 0:
+        ra += 360
+
+    dec = degrees(asin(sin(ε) * sin(λ)))
+
+    return {"ra": ra, "dec": dec}
+
+
+# *****************************************************************************************************************
```

### Comparing `celerity-0.8.0/src/celerity/temporal.py` & `celerity-0.9.0/src/celerity/temporal.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,22 @@
+# *****************************************************************************************************************
+
+# @author         Michael Roberts <michael@observerly.com>
+# @package        @observerly/celerity
+# @license        Copyright © 2021-2023 observerly
+
+# *****************************************************************************************************************
+
 from datetime import datetime, timezone
 from math import floor, pow
 
 from .constants import J1900, J2000
 
+# *****************************************************************************************************************
+
 
 def get_julian_date(date: datetime) -> float:
     """
     The Julian date (JD) of any instant is the Julian day number
     plus the fraction of a day since the preceding noon in Universal
     Time (UT).
 
@@ -21,25 +31,31 @@
             ).total_seconds()
             * 1000
         )
         / 86400000.0
     ) + 2440587.5
 
 
+# *****************************************************************************************************************
+
+
 def get_modified_julian_date(date: datetime) -> float:
     """
     The Modified Julian Date (MJD) is the number of fractional days since midnight
     on November 17, 1858.
 
     :param date: The datetime object to convert.
     :return: The Modified Julian Date (MJD) of the given date normalised to UTC.
     """
     return get_julian_date(date) - 2400000.5
 
 
+# *****************************************************************************************************************
+
+
 def get_greenwhich_sidereal_time(date: datetime) -> float:
     """
     The Greenwich Sidereal Time (GST) is the hour angle of the vernal
     equinox, the ascending node of the ecliptic on the celestial equator.
 
     :param date: The datetime object to convert.
     :return: The Greenwich Sidereal Time (GST) of the given date normalised to UTC.
@@ -68,14 +84,17 @@
     T_0 += A
 
     GST = T_0 % 24
 
     return GST + 24 if GST < 0 else GST
 
 
+# *****************************************************************************************************************
+
+
 def get_local_sidereal_time(date: datetime, longitude: float) -> float:
     """
     The Local Sidereal Time (LST) is the hour angle of the vernal
     equinox, the ascending node of the ecliptic on the celestial equator.
 
     :param date: The datetime object to convert.
     :param longitude: The longitude of the observer.
@@ -89,14 +108,17 @@
 
     if d < 0:
         d += 1
 
     return 24.0 * d
 
 
+# *****************************************************************************************************************
+
+
 def get_universal_time(date: datetime) -> float:
     """
     Universal Time (UT or UT1) is a time standard based on Earth's
     rotation. While originally it was mean solar time at 0° longitude,
     precise measurements of the Sun are difficult. Therefore, UT1 is
     computed from a measure of the Earth's angle with respect to the
     International Celestial Reference Frame (ICRF), called the Earth
@@ -144,7 +166,10 @@
 
     A = GST - T_0
 
     if A < 0:
         A += 24
 
     return 0.99727 * A
+
+
+# *****************************************************************************************************************
```

### Comparing `celerity-0.8.0/PKG-INFO` & `celerity-0.9.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: celerity
-Version: 0.8.0
+Version: 0.9.0
 Summary: Celerity is a lightweight, zero-dependency and type-safe Python library for astronomical calculations.
 Home-page: https://github.com/michaelroberts/celerity
 Keywords: astronomy,astrometry,ephemeris
 Author: Michael J. Roberts
 Author-email: michael@observerly.com
 Maintainer: Michael J. Roberts
 Maintainer-email: michael@observerly.com
```

