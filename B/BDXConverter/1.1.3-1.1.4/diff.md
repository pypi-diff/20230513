# Comparing `tmp/BDXConverter-1.1.3.tar.gz` & `tmp/BDXConverter-1.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BDXConverter-1.1.3.tar", last modified: Sat May 13 14:01:17 2023, max compression
+gzip compressed data, was "BDXConverter-1.1.4.tar", last modified: Sat May 13 14:04:56 2023, max compression
```

## Comparing `BDXConverter-1.1.3.tar` & `BDXConverter-1.1.4.tar`

### file list

```diff
@@ -1,72 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.586998 BDXConverter-1.1.3/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.578997 BDXConverter-1.1.3/BDXConverter/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.578997 BDXConverter-1.1.3/BDXConverter/Converter/
--rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Converter/Converter.py
--rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Converter/ErrorClassDefine.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Converter/FileOperation.py
--rw-r--r--   0 runner    (1001) docker     (123)    10941 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Converter/Signature.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.582997 BDXConverter-1.1.3/BDXConverter/General/
--rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/General/GeneralClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/General/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/General/Pool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/General/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.586998 BDXConverter-1.1.3/BDXConverter/Operation/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt16XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt16YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt16ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt16ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt32XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt32YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt32ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt32ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt8XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt8YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddInt8ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AddZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/AssignDebugData.py
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/CreateConstantString.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/NOP.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithBlockStates.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithNBTData.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/SetCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/SubtractXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/SubtractYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/SubtractZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/UseRuntimeIDPool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/Operation/structOfChest.py
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.586998 BDXConverter-1.1.3/BDXConverter/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/getByte.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/getString.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/marshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/marshalNBT_OldVersion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/unmarshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/BDXConverter/utils/unmarshalNBT_OldVersion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:01:17.578997 BDXConverter-1.1.3/BDXConverter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 14:01:17.000000 BDXConverter-1.1.3/BDXConverter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 14:01:17.000000 BDXConverter-1.1.3/BDXConverter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:01:17.000000 BDXConverter-1.1.3/BDXConverter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:01:17.000000 BDXConverter-1.1.3/BDXConverter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 14:01:17.000000 BDXConverter-1.1.3/BDXConverter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 14:01:17.586998 BDXConverter-1.1.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5448 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:01:17.586998 BDXConverter-1.1.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 14:01:05.000000 BDXConverter-1.1.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.651532 BDXConverter-1.1.4/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.639531 BDXConverter-1.1.4/BDXConverter/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.643531 BDXConverter-1.1.4/BDXConverter/Converter/
+-rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Converter/Converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Converter/ErrorClassDefine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Converter/FileOperation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10968 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Converter/Signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.643531 BDXConverter-1.1.4/BDXConverter/General/
+-rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/General/GeneralClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/General/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/General/Pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/General/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.651532 BDXConverter-1.1.4/BDXConverter/Operation/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt16XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt16YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt16ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt16ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt32XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt32YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt32ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt32ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt8XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt8YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddInt8ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AddZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/AssignDebugData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/CreateConstantString.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/NOP.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithBlockStates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithNBTData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/SetCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/SubtractXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/SubtractYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/SubtractZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/UseRuntimeIDPool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/Operation/structOfChest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.651532 BDXConverter-1.1.4/BDXConverter/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/getByte.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/getString.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/marshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/marshalNBT_OldVersion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/unmarshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/BDXConverter/utils/unmarshalNBT_OldVersion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:04:56.643531 BDXConverter-1.1.4/BDXConverter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 14:04:56.000000 BDXConverter-1.1.4/BDXConverter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 14:04:56.000000 BDXConverter-1.1.4/BDXConverter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:04:56.000000 BDXConverter-1.1.4/BDXConverter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:04:56.000000 BDXConverter-1.1.4/BDXConverter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 14:04:56.000000 BDXConverter-1.1.4/BDXConverter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 14:04:56.651532 BDXConverter-1.1.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5448 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:04:56.651532 BDXConverter-1.1.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 14:04:43.000000 BDXConverter-1.1.4/setup.py
```

### Comparing `BDXConverter-1.1.3/BDXConverter/Converter/Converter.py` & `BDXConverter-1.1.4/BDXConverter/Converter/Converter.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Converter/ErrorClassDefine.py` & `BDXConverter-1.1.4/BDXConverter/Converter/ErrorClassDefine.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Converter/FileOperation.py` & `BDXConverter-1.1.4/BDXConverter/Converter/FileOperation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Converter/Signature.py` & `BDXConverter-1.1.4/BDXConverter/Converter/Signature.py`

 * *Files 0% similar despite different names*

```diff
@@ -263,14 +263,14 @@
         if 'Outdated' in jsonDict:
             if jsonDict['Outdated'] != None:
                 self.isLegacy = jsonDict['Outdated']
         self.signedOrNeedToSign = jsonDict['Signed'] if 'Signed' in jsonDict else False
 
     def Dumps(self) -> dict:
         return {
-            'Signer': self.signer if self.signedOrNeedToSign == True else None,
+            'Signer': self.signer if self.isLegacy == False and self.signedOrNeedToSign == True else None,
             'Prove': self.prove if self.prove != '' else None,
             'Signature': self.signature.hex() if self.isLegacy == False and self.signedOrNeedToSign == True else None,
             'LegacySignBuffer': self.legacySignBuffer.hex() if self.isLegacy == True and self.signedOrNeedToSign == True else None,
             'Signed': self.signedOrNeedToSign,
             'Outdated': self.isLegacy if self.signedOrNeedToSign == True else None
         }
```

### Comparing `BDXConverter-1.1.3/BDXConverter/General/GeneralClass.py` & `BDXConverter-1.1.4/BDXConverter/General/GeneralClass.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/General/Operation.py` & `BDXConverter-1.1.4/BDXConverter/General/Operation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/General/Pool.py` & `BDXConverter-1.1.4/BDXConverter/General/Pool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt16XValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt16XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt16YValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt16YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt16ZValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt16ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt16ZValue0.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt16ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt32XValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt32XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt32YValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt32YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt32ZValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt32ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt32ZValue0.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt32ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt8XValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt8XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt8YValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt8YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AddInt8ZValue.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AddInt8ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/AssignDebugData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/AssignDebugData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/CreateConstantString.py` & `BDXConverter-1.1.4/BDXConverter/Operation/CreateConstantString.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlock.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithBlockStates.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithBlockStates.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithChestData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithNBTData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithNBTData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceBlockWithRuntimeId.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceBlockWithRuntimeId.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlock.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py` & `BDXConverter-1.1.4/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/SetCommandBlockData.py` & `BDXConverter-1.1.4/BDXConverter/Operation/SetCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/UseRuntimeIDPool.py` & `BDXConverter-1.1.4/BDXConverter/Operation/UseRuntimeIDPool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/Operation/structOfChest.py` & `BDXConverter-1.1.4/BDXConverter/Operation/structOfChest.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/utils/marshalNBT.py` & `BDXConverter-1.1.4/BDXConverter/utils/marshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/utils/marshalNBT_OldVersion.py` & `BDXConverter-1.1.4/BDXConverter/utils/marshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/utils/unmarshalNBT.py` & `BDXConverter-1.1.4/BDXConverter/utils/unmarshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter/utils/unmarshalNBT_OldVersion.py` & `BDXConverter-1.1.4/BDXConverter/utils/unmarshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/BDXConverter.egg-info/PKG-INFO` & `BDXConverter-1.1.4/BDXConverter.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.3
+Version: 1.1.4
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `BDXConverter-1.1.3/BDXConverter.egg-info/SOURCES.txt` & `BDXConverter-1.1.4/BDXConverter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/LICENSE` & `BDXConverter-1.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/PKG-INFO` & `BDXConverter-1.1.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.3
+Version: 1.1.4
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `BDXConverter-1.1.3/README.md` & `BDXConverter-1.1.4/README.md`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.3/setup.py` & `BDXConverter-1.1.4/setup.py`

 * *Files identical despite different names*

