# Comparing `tmp/BDXConverter-1.1.1.tar.gz` & `tmp/BDXConverter-1.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BDXConverter-1.1.1.tar", last modified: Sat May 13 08:56:31 2023, max compression
+gzip compressed data, was "BDXConverter-1.1.2.tar", last modified: Sat May 13 13:54:43 2023, max compression
```

## Comparing `BDXConverter-1.1.1.tar` & `BDXConverter-1.1.2.tar`

### file list

```diff
@@ -1,72 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/Converter/
--rw-r--r--   0 runner    (1001) docker     (123)     4437 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/Converter.py
--rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/ErrorClassDefine.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/FileOperation.py
--rw-r--r--   0 runner    (1001) docker     (123)     9454 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/Signature.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/General/
--rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/GeneralClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/Pool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/BDXConverter/Operation/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AssignDebugData.py
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/CreateConstantString.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/NOP.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStates.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithNBTData.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SetCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/UseRuntimeIDPool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/structOfChest.py
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/BDXConverter/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/getByte.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/getString.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/marshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/marshalNBT_OldVersion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT_OldVersion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5448 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.066960 BDXConverter-1.1.2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.054959 BDXConverter-1.1.2/BDXConverter/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.058959 BDXConverter-1.1.2/BDXConverter/Converter/
+-rw-r--r--   0 runner    (1001) docker     (123)     4581 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Converter/Converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Converter/ErrorClassDefine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Converter/FileOperation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10941 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Converter/Signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.058959 BDXConverter-1.1.2/BDXConverter/General/
+-rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/General/GeneralClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/General/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/General/Pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/General/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.062959 BDXConverter-1.1.2/BDXConverter/Operation/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt16XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt16YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt16ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt16ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt32XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt32YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt32ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt32ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt8XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt8YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddInt8ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AddZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/AssignDebugData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/CreateConstantString.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/NOP.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithBlockStates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithNBTData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/SetCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/SubtractXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/SubtractYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/SubtractZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/UseRuntimeIDPool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/Operation/structOfChest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.062959 BDXConverter-1.1.2/BDXConverter/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/getByte.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/getString.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/marshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/marshalNBT_OldVersion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/unmarshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/BDXConverter/utils/unmarshalNBT_OldVersion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:54:43.054959 BDXConverter-1.1.2/BDXConverter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 13:54:43.000000 BDXConverter-1.1.2/BDXConverter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 13:54:43.000000 BDXConverter-1.1.2/BDXConverter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:54:43.000000 BDXConverter-1.1.2/BDXConverter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 13:54:43.000000 BDXConverter-1.1.2/BDXConverter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 13:54:43.000000 BDXConverter-1.1.2/BDXConverter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 13:54:43.066960 BDXConverter-1.1.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5448 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:54:43.066960 BDXConverter-1.1.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 13:54:30.000000 BDXConverter-1.1.2/setup.py
```

### Comparing `BDXConverter-1.1.1/BDXConverter/Converter/Converter.py` & `BDXConverter-1.1.2/BDXConverter/Converter/Converter.py`

 * *Files 3% similar despite different names*

```diff
@@ -81,14 +81,17 @@
                 elif errorType == 2:
                     raise readError(reader.seek(0, 1))
                 # if meet error
                 self.BDXContent.append(struct)
                 # submit single datas
         # read datas from reader
         self.Signature.UnMarshal(reader)
+        reader.truncate(reader.seek(-1, 1))
+        self.Signature.BDXContentWithInsideHeader = reader
+        self.Signature.verifySignature()
         # signature
 
     def Loads(self, jsonDict: dict) -> None:
         BDXCommandPool: dict[int, GeneralClass] = GetBDXCommandPool()
 
         self.AuthorName = jsonDict['AuthorName'] if 'AuthorName' in jsonDict else ''
         if 'Signature' in jsonDict:
```

### Comparing `BDXConverter-1.1.1/BDXConverter/Converter/ErrorClassDefine.py` & `BDXConverter-1.1.2/BDXConverter/Converter/ErrorClassDefine.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Converter/FileOperation.py` & `BDXConverter-1.1.2/BDXConverter/Converter/FileOperation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Converter/Signature.py` & `BDXConverter-1.1.2/BDXConverter/Converter/Signature.py`

 * *Files 14% similar despite different names*

```diff
@@ -74,49 +74,52 @@
             Prove provided by the PhoenixBuilder Auth server.
                 Note: You don't know what "Prove: str" is?
                 If you go to the beginning of this file, 
                 there's a comment there, then you will get 
                 what you want. Same as follow
         `signer: str`
             Signer of this BDX file
+        `legacySignBuffer: bytes`
+            Binary signature datas on legacy signing method
         `signature: bytes`
-            Binary signature data
+            Binary signature datas
         `signedOrNeedToSign: bool` [You need to provide this while signing]
             If this file is signed, we will set it as True.
             Or, if you want to sign the changed BDX file,
             please set it as True
         `isLegacy: bool`
             It is true if the old signature method is used.
             The old signing method is deprecated,
             so we cannot support signing with this method
         `privateSigningKeyString: str` [You need to provide this while signing]
             The private key which used to sign BDX file
             provided by the PhoenixBuilder Auth server
         `BDXContentWithInsideHeader: io.BytesIO` [You need to provide this while only used to signing]
             The content of BDX file with inside file header
         """
-        self.prove: str | None = None
+        self.prove: str = ''
         self.signer: str = ''
+        self.legacySignBuffer: bytes = b''
         self.signature: bytes = b''
 
         self.signedOrNeedToSign: bool = False
         self.isLegacy: bool = False
 
         self.privateSigningKeyString: str = ''
         self.BDXContentWithInsideHeader: BytesIO = BytesIO(b'')
 
-    def verificationProve(self) -> str:
+    def verifyProve(self) -> str:
         """
-        Verify the validity of self.prove and return signer's name
+        Verify self.prove and return signer's name
         """
         constantServerKey = RSA.import_key('-----BEGIN RSA PUBLIC KEY-----\nMIIBCgKCAQEAzOoZfky1sYQXkTXWuYqf7HZ+tDSLyyuYOvyqt/dO4xahyNqvXcL5\n1A+eNFhsk6S5u84RuwsUk7oeNDpg/I0hbiRuJwCxFPJKNxDdj5Q5P5O0NTLR0TAT\nNBP7AjX6+XtNB/J6cV3fPcduqBbN4NjkNZxP4I1lgbupIR2lMKU9lXEn58nFSqSZ\nvG4BZfYLKUiu89IHaZOG5wgyDwwQrejxqkLUftmXibUO4s4gf8qAiLp3ukeIPYRj\nwGhGNlUfdU0foCxf2QwAoBV2xREL8/Sx1AIvmoVUg1SqCiIVMvbBkDoFfkzPZCgC\nLtmbkmqZJnpoBVHcBhBdUYsfyM6QwtWBNQIDAQAB\n-----END RSA PUBLIC KEY-----')
         verifier = PKCS1_v1_5.new(constantServerKey)
         # get publick key and verifier
         # note: this public key is provided from PhoenixBuilder code library
-        splitResult: list[str] = self.prove.split('::')  # type: ignore
+        splitResult: list[str] = self.prove.split('::')
         if len(splitResult) != 2:
             raise signatureError(
                 f'failed to parse prove datas; self.prove = "{self.prove}"')
         # split prove into list
         # example:
         # splitResult: list[str] = [rsaPublicKeyWithHolder: str, signature: str]
         # note: rsaPublicKey is used to sign the BDX file
@@ -129,15 +132,15 @@
         result = verifier.verify(
             new(splitResult[0].encode()),
             bytes.fromhex(splitResult[1])
         )
         if result == False:
             raise signatureError(
                 f'the prove provided has not been verified and may be invalid; self.prove = "{self.prove}"')
-        # verification the prove
+        # verify the prove
         return signer
         # return
 
     def loadPrivateKey(self) -> RSA.RsaKey:
         """
         Load privateKeyString:str into RSA.RsaKey and return it
         """
@@ -146,44 +149,58 @@
             return RSA.import_key(self.privateSigningKeyString)
         except:
             successStates = False
         if successStates == False:
             raise signatureError(
                 f'the privateSigningKeyString provided is invalid; self.privateSigningKeyString = "{self.privateSigningKeyString}"')
 
+    def verifySignature(self) -> None:
+        splitResult: list[str] = self.prove.split('|')
+        if len(splitResult) != 2:
+            raise signatureError(
+                f'failed to parse prove datas; self.prove = "{self.prove}"')
+        # split prove into list
+        rsaPublicKey = RSA.import_key(splitResult[0])
+        # load rsa public key
+        verifier = PKCS1_v1_5.new(rsaPublicKey)
+        # get verifier
+        result = verifier.verify(
+            new(self.BDXContentWithInsideHeader.getvalue()),
+            self.signature
+        )
+        if result == False:
+            raise signatureError(
+                f'the signature provided has not been validated, and it may be invalid; self.signature.hex() = "{self.signature.hex()}"')
+        # verify the signature
+
     def Marshal(self, writer: BytesIO) -> None:
         if self.signedOrNeedToSign == False or self.isLegacy == True:
             return
         # check if need to sign this file or this is a legacy method
         # note: legacy method is officially deprecated so we cannot support this
-        if self.prove == None:
+        if self.prove == '':
             raise signatureError('self.prove is not assigned')
         # check the states of self.prove
         if not 'privateSigningKeyString' in self.__dict__:
             raise signatureError('self.privateSigningKeyString is not existed')
         # check the states of self.privateSigningKeyString
-        self.signer = self.verificationProve()
+        self.signer = self.verifyProve()
         # verification the prove
         newWriter: BytesIO = BytesIO(b'')
         newWriter.write(b'\x00\x8b')
-        newWriter.write(pack('<H', len(self.prove)))  # type: ignore
-        newWriter.write(self.prove.encode(encoding='utf-8'))  # type: ignore
-        newWriter.write(
-            PKCS1_v1_5.new(
-                self.loadPrivateKey()
-            ).sign(
-                new(
-                    self.BDXContentWithInsideHeader.getvalue()
-                )
-            )
-        )
-        self.signature = newWriter.getvalue()
+        newWriter.write(pack('<H', len(self.prove)))
+        newWriter.write(self.prove.encode(encoding='utf-8'))
+        signatureDatas = PKCS1_v1_5.new(self.loadPrivateKey()).sign(
+            new(self.BDXContentWithInsideHeader.getvalue()))
+        newWriter.write(signatureDatas)
+        self.signature = signatureDatas
+        self.verifySignature()
         # get sign content and sync datas
         writer.write(b'X')
-        writer.write(self.signature)
+        writer.write(newWriter.getvalue())
         # write Terminate and sign content
         if newWriter.seek(0, 1) >= 255:
             writer.write(pack('>H', newWriter.seek(0, 1)))
             writer.write(b'\xff')
         else:
             writer.write(newWriter.seek(0, 1).to_bytes(
                 length=1, byteorder='little', signed=False))
@@ -210,40 +227,50 @@
             signLength: int = unpack('>H', getByte(buffer, 2))[0]
             buffer.seek(-4-signLength, 2)
         else:
             buffer.seek(-2, 2)
             signLength: int = unpack('>B', getByte(buffer, 1))[0]
             buffer.seek(-2-signLength, 2)
         signContent = BytesIO(getByte(buffer, signLength))
-        # get sign content
+        # get sign content ans sync datas
         if getByte(signContent, 2) != b'\x00\x8b':
             self.isLegacy = True
-            self.prove = None
-            self.signature = signContent.getvalue()
+            self.legacySignBuffer = signContent.getvalue()
             return
         else:
             proveLength: int = unpack('<H', getByte(signContent, 2))[0]
             self.prove = getByte(
                 signContent, proveLength).decode(encoding='utf-8')
-            self.signer = self.verificationProve()
+            self.signer = self.verifyProve()
             self.signature = getByte(signContent, signLength-proveLength-4)
         # sync datas
         buffer.seek(nowSeek, 0)
         # revert the pointer
 
     def Loads(self, jsonDict: dict) -> None:
-        self.signer = jsonDict['Signer'] if 'Signer' in jsonDict else ''
         self.prove = jsonDict['Prove'] if 'Prove' in jsonDict else ''
+        self.prove = '' if self.prove == None else self.prove
+        if 'Signer' in jsonDict:
+            if jsonDict['Signer'] != None:
+                self.signer = jsonDict['Signer']
         if 'Signature' in jsonDict:
-            signBinaryContent: str = jsonDict['Signature']
-            self.signature = bytes.fromhex(signBinaryContent)
+            if jsonDict['Signature'] != None:
+                self.signature = bytes.fromhex(jsonDict['Signature'])
+        if 'LegacySignBuffer' in jsonDict:
+            if jsonDict['LegacySignBuffer'] != None:
+                self.legacySignBuffer = bytes.fromhex(
+                    jsonDict['LegacySignBuffer']
+                )
+        if 'Outdated' in jsonDict:
+            if jsonDict['Outdated'] != None:
+                self.isLegacy = jsonDict['Outdated']
         self.signedOrNeedToSign = jsonDict['Signed'] if 'Signed' in jsonDict else False
-        self.isLegacy = jsonDict['Outdated'] if 'Outdated' in jsonDict else False
 
     def Dumps(self) -> dict:
         return {
-            'Signer': self.signer,
-            'Prove': self.prove,
-            'Signature': self.signature.hex(),
+            'Signer': self.signer if self.signedOrNeedToSign == True else None,
+            'Prove': self.prove if self.prove != '' else None,
+            'Signature': self.signature.hex() if self.isLegacy == False and self.signedOrNeedToSign == True else None,
+            'LegacySignBuffer': self.legacySignBuffer.hex() if self.isLegacy == True and self.signedOrNeedToSign == True else None,
             'Signed': self.signedOrNeedToSign,
-            'Outdated': self.isLegacy
+            'Outdated': self.isLegacy if self.signedOrNeedToSign == True else None
         }
```

### Comparing `BDXConverter-1.1.1/BDXConverter/General/GeneralClass.py` & `BDXConverter-1.1.2/BDXConverter/General/GeneralClass.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/General/Operation.py` & `BDXConverter-1.1.2/BDXConverter/General/Operation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/General/Pool.py` & `BDXConverter-1.1.2/BDXConverter/General/Pool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16XValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt16XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16YValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt16YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt16ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue0.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt16ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32XValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt32XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32YValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt32YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt32ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue0.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt32ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8XValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt8XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8YValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt8YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8ZValue.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AddInt8ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/AssignDebugData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/AssignDebugData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/CreateConstantString.py` & `BDXConverter-1.1.2/BDXConverter/Operation/CreateConstantString.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlock.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStates.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithBlockStates.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithChestData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithNBTData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithNBTData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithRuntimeId.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceBlockWithRuntimeId.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlock.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py` & `BDXConverter-1.1.2/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/SetCommandBlockData.py` & `BDXConverter-1.1.2/BDXConverter/Operation/SetCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/UseRuntimeIDPool.py` & `BDXConverter-1.1.2/BDXConverter/Operation/UseRuntimeIDPool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/Operation/structOfChest.py` & `BDXConverter-1.1.2/BDXConverter/Operation/structOfChest.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/utils/marshalNBT.py` & `BDXConverter-1.1.2/BDXConverter/utils/marshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/utils/marshalNBT_OldVersion.py` & `BDXConverter-1.1.2/BDXConverter/utils/marshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT.py` & `BDXConverter-1.1.2/BDXConverter/utils/unmarshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT_OldVersion.py` & `BDXConverter-1.1.2/BDXConverter/utils/unmarshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/BDXConverter.egg-info/PKG-INFO` & `BDXConverter-1.1.2/BDXConverter.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.1
+Version: 1.1.2
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `BDXConverter-1.1.1/BDXConverter.egg-info/SOURCES.txt` & `BDXConverter-1.1.2/BDXConverter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/LICENSE` & `BDXConverter-1.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/PKG-INFO` & `BDXConverter-1.1.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.1
+Version: 1.1.2
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `BDXConverter-1.1.1/README.md` & `BDXConverter-1.1.2/README.md`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.1/setup.py` & `BDXConverter-1.1.2/setup.py`

 * *Files identical despite different names*

