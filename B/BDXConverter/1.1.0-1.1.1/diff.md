# Comparing `tmp/BDXConverter-1.1.0.tar.gz` & `tmp/BDXConverter-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BDXConverter-1.1.0.tar", last modified: Sat May 13 08:33:05 2023, max compression
+gzip compressed data, was "BDXConverter-1.1.1.tar", last modified: Sat May 13 08:56:31 2023, max compression
```

## Comparing `BDXConverter-1.1.0.tar` & `BDXConverter-1.1.1.tar`

### file list

```diff
@@ -1,72 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.482476 BDXConverter-1.1.0/BDXConverter/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter/Converter/
--rw-r--r--   0 runner    (1001) docker     (123)     4437 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/Converter.py
--rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/ErrorClassDefine.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/FileOperation.py
--rw-r--r--   0 runner    (1001) docker     (123)     9232 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/Signature.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter/General/
--rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/GeneralClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/Pool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.498476 BDXConverter-1.1.0/BDXConverter/Operation/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AssignDebugData.py
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/CreateConstantString.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/NOP.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStates.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithNBTData.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SetCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/UseRuntimeIDPool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/structOfChest.py
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.498476 BDXConverter-1.1.0/BDXConverter/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/getByte.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/getString.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/marshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/marshalNBT_OldVersion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT_OldVersion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5252 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/Converter/
+-rw-r--r--   0 runner    (1001) docker     (123)     4437 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/Converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/ErrorClassDefine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/FileOperation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9454 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/Signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter/General/
+-rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/GeneralClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/Pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/General/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/BDXConverter/Operation/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddInt8ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AddZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/AssignDebugData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/CreateConstantString.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/NOP.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithNBTData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SetCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/SubtractZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/UseRuntimeIDPool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/Operation/structOfChest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/BDXConverter/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/getByte.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/getString.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/marshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/marshalNBT_OldVersion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT_OldVersion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:56:31.368963 BDXConverter-1.1.1/BDXConverter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 08:56:31.000000 BDXConverter-1.1.1/BDXConverter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5976 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5448 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:56:31.376963 BDXConverter-1.1.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 08:56:18.000000 BDXConverter-1.1.1/setup.py
```

### Comparing `BDXConverter-1.1.0/BDXConverter/Converter/Converter.py` & `BDXConverter-1.1.1/BDXConverter/Converter/Converter.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Converter/ErrorClassDefine.py` & `BDXConverter-1.1.1/BDXConverter/Converter/ErrorClassDefine.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Converter/FileOperation.py` & `BDXConverter-1.1.1/BDXConverter/Converter/FileOperation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Converter/Signature.py` & `BDXConverter-1.1.1/BDXConverter/Converter/Signature.py`

 * *Files 8% similar despite different names*

```diff
@@ -90,15 +90,15 @@
             so we cannot support signing with this method
         `privateSigningKeyString: str` [You need to provide this while signing]
             The private key which used to sign BDX file
             provided by the PhoenixBuilder Auth server
         `BDXContentWithInsideHeader: io.BytesIO` [You need to provide this while only used to signing]
             The content of BDX file with inside file header
         """
-        self.prove: str = ''
+        self.prove: str | None = None
         self.signer: str = ''
         self.signature: bytes = b''
 
         self.signedOrNeedToSign: bool = False
         self.isLegacy: bool = False
 
         self.privateSigningKeyString: str = ''
@@ -108,15 +108,15 @@
         """
         Verify the validity of self.prove and return signer's name
         """
         constantServerKey = RSA.import_key('-----BEGIN RSA PUBLIC KEY-----\nMIIBCgKCAQEAzOoZfky1sYQXkTXWuYqf7HZ+tDSLyyuYOvyqt/dO4xahyNqvXcL5\n1A+eNFhsk6S5u84RuwsUk7oeNDpg/I0hbiRuJwCxFPJKNxDdj5Q5P5O0NTLR0TAT\nNBP7AjX6+XtNB/J6cV3fPcduqBbN4NjkNZxP4I1lgbupIR2lMKU9lXEn58nFSqSZ\nvG4BZfYLKUiu89IHaZOG5wgyDwwQrejxqkLUftmXibUO4s4gf8qAiLp3ukeIPYRj\nwGhGNlUfdU0foCxf2QwAoBV2xREL8/Sx1AIvmoVUg1SqCiIVMvbBkDoFfkzPZCgC\nLtmbkmqZJnpoBVHcBhBdUYsfyM6QwtWBNQIDAQAB\n-----END RSA PUBLIC KEY-----')
         verifier = PKCS1_v1_5.new(constantServerKey)
         # get publick key and verifier
         # note: this public key is provided from PhoenixBuilder code library
-        splitResult: list[str] = self.prove.split('::')
+        splitResult: list[str] = self.prove.split('::')  # type: ignore
         if len(splitResult) != 2:
             raise signatureError(
                 f'failed to parse prove datas; self.prove = "{self.prove}"')
         # split prove into list
         # example:
         # splitResult: list[str] = [rsaPublicKeyWithHolder: str, signature: str]
         # note: rsaPublicKey is used to sign the BDX file
@@ -151,23 +151,26 @@
                 f'the privateSigningKeyString provided is invalid; self.privateSigningKeyString = "{self.privateSigningKeyString}"')
 
     def Marshal(self, writer: BytesIO) -> None:
         if self.signedOrNeedToSign == False or self.isLegacy == True:
             return
         # check if need to sign this file or this is a legacy method
         # note: legacy method is officially deprecated so we cannot support this
+        if self.prove == None:
+            raise signatureError('self.prove is not assigned')
+        # check the states of self.prove
         if not 'privateSigningKeyString' in self.__dict__:
             raise signatureError('self.privateSigningKeyString is not existed')
         # check the states of self.privateSigningKeyString
         self.signer = self.verificationProve()
         # verification the prove
         newWriter: BytesIO = BytesIO(b'')
         newWriter.write(b'\x00\x8b')
-        newWriter.write(pack('<H', len(self.prove)))
-        newWriter.write(self.prove.encode(encoding='utf-8'))
+        newWriter.write(pack('<H', len(self.prove)))  # type: ignore
+        newWriter.write(self.prove.encode(encoding='utf-8'))  # type: ignore
         newWriter.write(
             PKCS1_v1_5.new(
                 self.loadPrivateKey()
             ).sign(
                 new(
                     self.BDXContentWithInsideHeader.getvalue()
                 )
@@ -210,14 +213,15 @@
             buffer.seek(-2, 2)
             signLength: int = unpack('>B', getByte(buffer, 1))[0]
             buffer.seek(-2-signLength, 2)
         signContent = BytesIO(getByte(buffer, signLength))
         # get sign content
         if getByte(signContent, 2) != b'\x00\x8b':
             self.isLegacy = True
+            self.prove = None
             self.signature = signContent.getvalue()
             return
         else:
             proveLength: int = unpack('<H', getByte(signContent, 2))[0]
             self.prove = getByte(
                 signContent, proveLength).decode(encoding='utf-8')
             self.signer = self.verificationProve()
```

### Comparing `BDXConverter-1.1.0/BDXConverter/General/GeneralClass.py` & `BDXConverter-1.1.1/BDXConverter/General/GeneralClass.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/General/Operation.py` & `BDXConverter-1.1.1/BDXConverter/General/Operation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/General/Pool.py` & `BDXConverter-1.1.1/BDXConverter/General/Pool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16XValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16YValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue0.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt16ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32XValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32YValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue0.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt32ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8XValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8YValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8ZValue.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AddInt8ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/AssignDebugData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/AssignDebugData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/CreateConstantString.py` & `BDXConverter-1.1.1/BDXConverter/Operation/CreateConstantString.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlock.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStates.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStates.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithChestData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithNBTData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithNBTData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithRuntimeId.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceBlockWithRuntimeId.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlock.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py` & `BDXConverter-1.1.1/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/SetCommandBlockData.py` & `BDXConverter-1.1.1/BDXConverter/Operation/SetCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/UseRuntimeIDPool.py` & `BDXConverter-1.1.1/BDXConverter/Operation/UseRuntimeIDPool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/Operation/structOfChest.py` & `BDXConverter-1.1.1/BDXConverter/Operation/structOfChest.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/utils/marshalNBT.py` & `BDXConverter-1.1.1/BDXConverter/utils/marshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/utils/marshalNBT_OldVersion.py` & `BDXConverter-1.1.1/BDXConverter/utils/marshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT.py` & `BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT_OldVersion.py` & `BDXConverter-1.1.1/BDXConverter/utils/unmarshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/BDXConverter.egg-info/PKG-INFO` & `BDXConverter-1.1.1/BDXConverter.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.0
+Version: 1.1.1
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,20 +17,22 @@
 <br/>
 <p align="center">
 <img src="https://forthebadge.com/images/badges/built-with-love.svg">
 <p>
 
 [GitHub: Happy2018new]: https://img.shields.io/badge/GitHub-Happy2018new-00A1E7?style=for-the-badge
 [GitHub: Inotart]: https://img.shields.io/badge/GitHub-Inotart-00A1E7?style=for-the-badge
+[Bilibili: EillesWan]: https://img.shields.io/badge/Bilibili-%E5%87%8C%E4%BA%91%E9%87%91%E7%BE%BF-00A1E7?style=for-the-badge
 [python]: https://img.shields.io/badge/python-3.9-AB70FF?style=for-the-badge
 [release]: https://img.shields.io/github/v/release/EillesWan/Musicreater?style=for-the-badge
 [license]: https://img.shields.io/badge/LICENSE-MIT-228B22?style=for-the-badge
 
 [![][GitHub: Happy2018new]](https://github.com/Happy2018new)<br/>
 [![][GitHub: Inotart]](https://github.com/Inotart)<br/>
+[![][Bilibili: EillesWan]](https://space.bilibili.com/397369002/)<br/>
 [![][python]](https://www.python.org/)<br/>
 [![][license]](LICENSE)<br/>
```

### Comparing `BDXConverter-1.1.0/BDXConverter.egg-info/SOURCES.txt` & `BDXConverter-1.1.1/BDXConverter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/LICENSE` & `BDXConverter-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.0/PKG-INFO` & `BDXConverter-1.1.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.0
+Version: 1.1.1
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,20 +17,22 @@
 <br/>
 <p align="center">
 <img src="https://forthebadge.com/images/badges/built-with-love.svg">
 <p>
 
 [GitHub: Happy2018new]: https://img.shields.io/badge/GitHub-Happy2018new-00A1E7?style=for-the-badge
 [GitHub: Inotart]: https://img.shields.io/badge/GitHub-Inotart-00A1E7?style=for-the-badge
+[Bilibili: EillesWan]: https://img.shields.io/badge/Bilibili-%E5%87%8C%E4%BA%91%E9%87%91%E7%BE%BF-00A1E7?style=for-the-badge
 [python]: https://img.shields.io/badge/python-3.9-AB70FF?style=for-the-badge
 [release]: https://img.shields.io/github/v/release/EillesWan/Musicreater?style=for-the-badge
 [license]: https://img.shields.io/badge/LICENSE-MIT-228B22?style=for-the-badge
 
 [![][GitHub: Happy2018new]](https://github.com/Happy2018new)<br/>
 [![][GitHub: Inotart]](https://github.com/Inotart)<br/>
+[![][Bilibili: EillesWan]](https://space.bilibili.com/397369002/)<br/>
 [![][python]](https://www.python.org/)<br/>
 [![][license]](LICENSE)<br/>
```

### Comparing `BDXConverter-1.1.0/README.md` & `BDXConverter-1.1.1/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -3,20 +3,22 @@
 <br/>
 <p align="center">
 <img src="https://forthebadge.com/images/badges/built-with-love.svg">
 <p>
 
 [GitHub: Happy2018new]: https://img.shields.io/badge/GitHub-Happy2018new-00A1E7?style=for-the-badge
 [GitHub: Inotart]: https://img.shields.io/badge/GitHub-Inotart-00A1E7?style=for-the-badge
+[Bilibili: EillesWan]: https://img.shields.io/badge/Bilibili-%E5%87%8C%E4%BA%91%E9%87%91%E7%BE%BF-00A1E7?style=for-the-badge
 [python]: https://img.shields.io/badge/python-3.9-AB70FF?style=for-the-badge
 [release]: https://img.shields.io/github/v/release/EillesWan/Musicreater?style=for-the-badge
 [license]: https://img.shields.io/badge/LICENSE-MIT-228B22?style=for-the-badge
 
 [![][GitHub: Happy2018new]](https://github.com/Happy2018new)<br/>
 [![][GitHub: Inotart]](https://github.com/Inotart)<br/>
+[![][Bilibili: EillesWan]](https://space.bilibili.com/397369002/)<br/>
 [![][python]](https://www.python.org/)<br/>
 [![][license]](LICENSE)<br/>
```

### Comparing `BDXConverter-1.1.0/setup.py` & `BDXConverter-1.1.1/setup.py`

 * *Files identical despite different names*

