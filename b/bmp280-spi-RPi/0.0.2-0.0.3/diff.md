# Comparing `tmp/bmp280-spi-RPi-0.0.2.tar.gz` & `tmp/bmp280-spi-RPi-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bmp280-spi-RPi-0.0.2.tar", last modified: Sat May 13 06:38:24 2023, max compression
+gzip compressed data, was "bmp280-spi-RPi-0.0.3.tar", last modified: Sat May 13 07:09:40 2023, max compression
```

## Comparing `bmp280-spi-RPi-0.0.2.tar` & `bmp280-spi-RPi-0.0.3.tar`

### file list

```diff
@@ -1,20 +1,21 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 06:38:24.845747 bmp280-spi-RPi-0.0.2/
--rw-rw-rw-   0        0        0      318 2023-05-13 06:38:24.844748 bmp280-spi-RPi-0.0.2/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-05-13 06:36:29.000000 bmp280-spi-RPi-0.0.2/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 06:38:24.818842 bmp280-spi-RPi-0.0.2/bmp280/
--rw-rw-rw-   0        0        0        0 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/__init__.py
--rw-rw-rw-   0        0        0     3502 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/bmp280.py
--rw-rw-rw-   0        0        0       73 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/filter.py
--rw-rw-rw-   0        0        0       91 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/pressure_oversampling.py
--rw-rw-rw-   0        0        0      132 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/sampling_interval.py
--rw-rw-rw-   0        0        0       91 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.2/bmp280/temperature_oversampling.py
-drwxrwxrwx   0        0        0        0 2023-05-13 06:38:24.843761 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/
--rw-rw-rw-   0        0        0      318 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      407 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0        7 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-05-13 06:38:24.000000 bmp280-spi-RPi-0.0.2/bmp280_spi_RPi.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      382 2023-05-13 06:38:22.000000 bmp280-spi-RPi-0.0.2/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-13 06:38:24.845747 bmp280-spi-RPi-0.0.2/setup.cfg
--rw-rw-rw-   0        0        0      864 2023-05-13 06:38:22.000000 bmp280-spi-RPi-0.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:09:40.780548 bmp280-spi-RPi-0.0.3/
+-rw-rw-rw-   0        0        0     1094 2023-05-13 06:56:32.000000 bmp280-spi-RPi-0.0.3/LICENSE.md
+-rw-rw-rw-   0        0        0     2201 2023-05-13 07:09:40.779548 bmp280-spi-RPi-0.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0      684 2023-05-13 07:06:10.000000 bmp280-spi-RPi-0.0.3/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 07:09:40.757547 bmp280-spi-RPi-0.0.3/bmp280/
+-rw-rw-rw-   0        0        0        0 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/__init__.py
+-rw-rw-rw-   0        0        0     3502 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/bmp280.py
+-rw-rw-rw-   0        0        0       73 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/filter.py
+-rw-rw-rw-   0        0        0       91 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/pressure_oversampling.py
+-rw-rw-rw-   0        0        0      132 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/sampling_interval.py
+-rw-rw-rw-   0        0        0       91 2023-05-12 18:42:01.000000 bmp280-spi-RPi-0.0.3/bmp280/temperature_oversampling.py
+drwxrwxrwx   0        0        0        0 2023-05-13 07:09:40.778551 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/
+-rw-rw-rw-   0        0        0     2201 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      418 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0        7 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 07:09:40.000000 bmp280-spi-RPi-0.0.3/bmp280_spi_RPi.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      415 2023-05-13 07:09:38.000000 bmp280-spi-RPi-0.0.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 07:09:40.780548 bmp280-spi-RPi-0.0.3/setup.cfg
+-rw-rw-rw-   0        0        0      864 2023-05-13 06:41:48.000000 bmp280-spi-RPi-0.0.3/setup.py
```

### Comparing `bmp280-spi-RPi-0.0.2/bmp280/bmp280.py` & `bmp280-spi-RPi-0.0.3/bmp280/bmp280.py`

 * *Files identical despite different names*

### Comparing `bmp280-spi-RPi-0.0.2/setup.py` & `bmp280-spi-RPi-0.0.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='bmp280-spi-RPi',
-    version='0.0.2',
+    version='0.0.3',
     author="Michal Tomek",
     description="BMP280 package for Raspberry Pi using SPI interface provided by spidev library",
     long_description="BMP280 package for Raspberry Pi. Provides option for BMP280 configuration and data read. "
                      "Doesn't need linux device tree patch like other BMP280 SPI linux packages. "
                      "Performs raw data processing with calibration data, like specified in BMP280 datasheet. "
                      "Does support single reads, does not support callbacks for fast data sampling yet. ",
     install_requires=[
```

