# Comparing `tmp/BDXConverter-1.0.16.tar.gz` & `tmp/BDXConverter-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BDXConverter-1.0.16.tar", last modified: Sat May  6 14:15:29 2023, max compression
+gzip compressed data, was "BDXConverter-1.1.0.tar", last modified: Sat May 13 08:33:05 2023, max compression
```

## Comparing `BDXConverter-1.0.16.tar` & `BDXConverter-1.1.0.tar`

### file list

```diff
@@ -1,71 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.594804 BDXConverter-1.0.16/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.578803 BDXConverter-1.0.16/BDXConverter/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.578803 BDXConverter-1.0.16/BDXConverter/Converter/
--rw-r--r--   0 runner    (1001) docker     (123)      781 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Converter/ConvertErrorDefine.py
--rw-r--r--   0 runner    (1001) docker     (123)     4536 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Converter/Converter.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.582803 BDXConverter-1.0.16/BDXConverter/General/
--rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/General/GeneralClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2648 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/General/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1515 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/General/Pool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/General/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.590803 BDXConverter-1.0.16/BDXConverter/Operation/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt16XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt16YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt16ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt16ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt32XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt32YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt32ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt32ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt8XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt8YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddInt8ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AddZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/AssignDebugData.py
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/CreateConstantString.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/NOP.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithBlockStates.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithNBTData.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/SetCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/SubtractXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/SubtractYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/SubtractZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      477 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/Terminate.py
--rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/UseRuntimeIDPool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/Operation/structOfChest.py
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.594804 BDXConverter-1.0.16/BDXConverter/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/getByte.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/getString.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/marshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/marshalNBT_OldVersion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/unmarshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/BDXConverter/utils/unmarshalNBT_OldVersion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-06 14:15:29.578803 BDXConverter-1.0.16/BDXConverter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5725 2023-05-06 14:15:29.000000 BDXConverter-1.0.16/BDXConverter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2509 2023-05-06 14:15:29.000000 BDXConverter-1.0.16/BDXConverter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-06 14:15:29.000000 BDXConverter-1.0.16/BDXConverter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-05-06 14:15:29.000000 BDXConverter-1.0.16/BDXConverter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-06 14:15:29.000000 BDXConverter-1.0.16/BDXConverter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5725 2023-05-06 14:15:29.594804 BDXConverter-1.0.16/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5196 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-06 14:15:29.594804 BDXConverter-1.0.16/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-06 14:15:18.000000 BDXConverter-1.0.16/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.482476 BDXConverter-1.1.0/BDXConverter/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter/Converter/
+-rw-r--r--   0 runner    (1001) docker     (123)     4437 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/Converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/ErrorClassDefine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/FileOperation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9232 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/Signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter/General/
+-rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/GeneralClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/Pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/General/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.498476 BDXConverter-1.1.0/BDXConverter/Operation/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddInt8ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AddZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/AssignDebugData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/CreateConstantString.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/NOP.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithNBTData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SetCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/SubtractZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/UseRuntimeIDPool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/Operation/structOfChest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.498476 BDXConverter-1.1.0/BDXConverter/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/getByte.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/getString.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/marshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/marshalNBT_OldVersion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT_OldVersion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 08:33:05.486476 BDXConverter-1.1.0/BDXConverter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 08:33:05.000000 BDXConverter-1.1.0/BDXConverter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5252 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 08:33:05.502477 BDXConverter-1.1.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 08:32:54.000000 BDXConverter-1.1.0/setup.py
```

### Comparing `BDXConverter-1.0.16/BDXConverter/Converter/ConvertErrorDefine.py` & `BDXConverter-1.1.0/BDXConverter/Converter/ErrorClassDefine.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-class notAcorrectBDXFileError(Exception):
+class headerError(Exception):
     """
-    Not a correct BDX file error
+    header error occurred while reading header in BDX file
     """
 
-    def __init__(self, path: str):
-        Exception.__init__(self, f'"{path}" is not a correct BDX file')
+    def __init__(self, header: bytes):
+        Exception.__init__(self, f'find invalid file header "{header}"')
 
 
 class readError(Exception):
     """
     BDX file read error
     """
 
@@ -21,7 +21,16 @@
     """
     Find unknown operation error
     """
 
     def __init__(self, operationId: int, errorOccurredPosition: int):
         Exception.__init__(
             self, f'an unknown operation {operationId} was found, and the error occurred at position {errorOccurredPosition}')
+
+
+class signatureError(Exception):
+    """
+    Error occurred while signing
+    """
+
+    def __init__(self, errorContent: str):
+        Exception.__init__(self, errorContent)
```

### Comparing `BDXConverter-1.0.16/BDXConverter/Converter/Converter.py` & `BDXConverter-1.1.0/BDXConverter/Converter/Converter.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,132 +1,113 @@
 from ..General.GeneralClass import GeneralClass
 from ..General.Pool import GetBDXCommandPool
 from ..utils.getString import getByte, getString
-from .ConvertErrorDefine import notAcorrectBDXFileError
-from .ConvertErrorDefine import readError, unknownOperationError
+from .Signature import Signature
+from .ErrorClassDefine import headerError
+from .ErrorClassDefine import readError, unknownOperationError
 from brotli import compress, decompress
 from io import BytesIO
-from json import loads, dumps
 from copy import deepcopy
 
 
-def ReadBDXFile(path: str) -> tuple[list[GeneralClass], str]:
-    """
-    Convert BDX file into list[GeneralClass] and return the author's name
-    """
-    with open(path, "r+b") as file:
-        fileContext: bytes = file.read()
-    # get the context of this bdx file
-    if fileContext[0:3] != b'BD@':
-        raise notAcorrectBDXFileError(path)
-    buffer = BytesIO(decompress(fileContext[3:]))
-    if getByte(buffer, 3) != b'BDX':
-        raise notAcorrectBDXFileError(path)
-    # check header and create new buffer
-    result: list[GeneralClass] = []
-    bdxCommandPool: dict[int, GeneralClass] = GetBDXCommandPool()
-    # prepare
-    getByte(buffer, 1)
-    authorName = getString(buffer)
-    # get author's information
-    while True:
-        commandId = getByte(buffer, 1)
-        if commandId[0] in bdxCommandPool:
-            struct: GeneralClass = deepcopy(bdxCommandPool[commandId[0]])
-            # get struct(operation) from the pool
-            try:
-                struct.UnMarshal(buffer)
-            except EOFError:
-                raise EOFError
-            except:
-                raise readError(buffer.seek(0, 1))
-            # unmarshal bytes into python object(GeneralClass)
-            result.append(struct)
-            # submit single datas
-            if struct.operationNumber == 88:
-                break
-            # if meet operation Terminate(88)
+class BDX(GeneralClass):
+    def __init__(self) -> None:
+        """
+        `AuthorName: str`
+            The author of this BDX file
+                Note: The default value is "TriM-Organization/BDXConverter"
+        `BDXContent: list[GeneralClass]`
+            The valid contents of the BDX file
+        `Signature: Signature`
+            The signature data of the BDX file
+        """
+        self.AuthorName: str = 'TriM-Organization/BDXConverter'
+        self.BDXContent: list[GeneralClass] = []
+        self.Signature: Signature = Signature()
+
+    def Marshal(self, writer: BytesIO) -> None:
+        newWriter = BytesIO(
+            b'BDX\x00'+self.AuthorName.encode(encoding='utf-8')+b'\x00')
+        newWriter.seek(0, 2)
+        # inside header with author's name
+        for i in self.BDXContent:
+            newWriter.write(i.operationNumber.to_bytes(
+                length=1, byteorder='big', signed=False))
+            i.Marshal(newWriter)
+        # valid contents
+        if self.Signature.signedOrNeedToSign == True and self.Signature.isLegacy == False:
+            self.Signature.BDXContentWithInsideHeader = newWriter
+            self.Signature.Marshal(newWriter)
         else:
-            raise unknownOperationError(commandId[0], buffer.seek(0, 1))
-            # if we can not find the operation from the command pool
-    # read bdx file
-    return result, authorName
-    # return
-
-
-def DumpStructs(
-        structs: list[GeneralClass],
-        outputPath: str,
-        authorName: str = 'KazamataNeri/MCConvertExecute-bdx'
-) -> None:
-    """
-    Convert list[GeneralClass] into bytes and write it into a bdx file(outputPath:str).
-
-    Note:
-        - Author's name is no need to write,
-        because this field has been officially deprecated.
-        But we still put the names into this place as symbolically
-    """
-    writer: BytesIO = BytesIO(b'')
-    # request a new writer
-    writer.write(b'BDX\x00'+authorName.encode(encoding='utf-8')+b'\x00')
-    # write inside header(BDX) and author's name
-    for i in structs:
-        writer.write(i.operationNumber.to_bytes(
-            length=1, byteorder='big', signed=False))
-        i.Marshal(writer)
-    # marshal python object into the writer
-    result = b'BD@' + compress(writer.getvalue())
-    # compress writer into bytes and set outside header which named "BD@"
-    with open(outputPath, 'w+b') as file:
-        file.write(result)
-    # write bytes into a bdx file
-
-
-def VisualStructs(structs: list[GeneralClass], outputPath: str) -> None:
-    """
-    Convert list[GeneralClass] into json data and write it into outputPath:str
-    """
-    new: list = []
-    for i in structs:
-        new.append(i.Dumps())
-    # convert bdx file in to basic datas
-    result: str = dumps(
-        new,
-        sort_keys=True,
-        indent=4,
-        separators=(', ', ': '),
-        ensure_ascii=False
-    )
-    # get string
-    with open(outputPath, 'w+', encoding='utf-8') as file:
-        file.write(result)
-    # write json datas
-
-
-def ConvertJSONFileIntoStructs(path: str) -> list[GeneralClass]:
-    """
-    Read json datas from path:str and convert it into list[GeneralClass]
-    """
-    with open(path, 'r+', encoding='utf-8') as file:
-        fileContext: str = file.read()
-    jsonDatas: list[dict] = loads(fileContext)
-    # load json datas from file
-    result: list[GeneralClass] = []
-    bdxCommandPool: dict[int, GeneralClass] = GetBDXCommandPool()
-    # prepare
-    for i in jsonDatas:
-        if not 'operationNumber' in i:
-            continue
-        operationNumber: int = i['operationNumber']
-        if not operationNumber in bdxCommandPool:
-            continue
-        # get operation number
-        struct: GeneralClass = deepcopy(bdxCommandPool[operationNumber])
-        # request a new struct
-        struct.Loads(i)
-        # load datas
-        result.append(struct)
-        # submit single struct
-    # load datas from json dict
-    return result
-    # return
+            newWriter.write(b'XE')
+        # signature
+        writer.write(b'BD@'+compress(newWriter.getvalue()))
+        # write BDX datas
+
+    def UnMarshal(self, binaryDatas: bytes) -> None:
+        if binaryDatas[0:3] != b'BD@':
+            raise headerError(binaryDatas[:3])
+        # check outside header
+        reader = BytesIO(decompress(binaryDatas[3:]))
+        # get reader to read valid contents
+        insideHeader = getByte(reader, 3)
+        if insideHeader != b'BDX':
+            raise headerError(insideHeader)
+        # check inside header
+        firstOperation = getByte(reader, 1)
+        if firstOperation != b'\x00':
+            raise unknownOperationError(firstOperation[0], reader.seek(-1, 1))
+        self.AuthorName = getString(reader)
+        # get author's name
+        BDXCommandPool: dict[int, GeneralClass] = GetBDXCommandPool()
+        # get bdx command(operation) pool
+        while True:
+            commandId = getByte(reader, 1)[0]
+            if commandId == 88:
+                break
+            elif commandId in BDXCommandPool:
+                struct: GeneralClass = deepcopy(BDXCommandPool[commandId])
+                # get struct(operation) from the pool
+                errorType = 0
+                # prepare
+                try:
+                    struct.UnMarshal(reader)
+                except EOFError:
+                    errorType = 1
+                except:
+                    errorType = 2
+                # unmarshal bytes into the struct
+                if errorType == 1:
+                    raise EOFError
+                elif errorType == 2:
+                    raise readError(reader.seek(0, 1))
+                # if meet error
+                self.BDXContent.append(struct)
+                # submit single datas
+        # read datas from reader
+        self.Signature.UnMarshal(reader)
+        # signature
+
+    def Loads(self, jsonDict: dict) -> None:
+        BDXCommandPool: dict[int, GeneralClass] = GetBDXCommandPool()
+
+        self.AuthorName = jsonDict['AuthorName'] if 'AuthorName' in jsonDict else ''
+        if 'Signature' in jsonDict:
+            self.Signature.Loads(jsonDict['Signature'])
+        if 'BDXContent' in jsonDict:
+            tmp: list[dict] = jsonDict['BDXContent']
+            for i in tmp:
+                if not 'operationNumber' in i:
+                    continue
+                if not 'operationDatas' in i:
+                    continue
+                commandId: int = i['operationNumber']
+                struct: GeneralClass = deepcopy(BDXCommandPool[commandId])
+                struct.Loads(i['operationDatas'])
+                self.BDXContent.append(struct)
+
+    def Dumps(self) -> dict:
+        return {
+            'AuthorName': self.AuthorName,
+            'BDXContent': [i.Dumps() for i in self.BDXContent],
+            'Signature': self.Signature.Dumps()
+        }
```

### Comparing `BDXConverter-1.0.16/BDXConverter/General/GeneralClass.py` & `BDXConverter-1.1.0/BDXConverter/General/GeneralClass.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/General/Operation.py` & `BDXConverter-1.1.0/BDXConverter/General/Operation.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,10 +34,9 @@
 from ..Operation.PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID import PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID
 from ..Operation.PlaceCommandBlockWithCommandBlockData import PlaceCommandBlockWithCommandBlockData
 from ..Operation.PlaceRuntimeBlockWithChestData import PlaceRuntimeBlockWithChestData
 from ..Operation.PlaceRuntimeBlockWithChestDataAndUint32RuntimeID import PlaceRuntimeBlockWithChestDataAndUint32RuntimeID
 from ..Operation.AssignDebugData import AssignDebugData
 from ..Operation.PlaceBlockWithChestData import PlaceBlockWithChestData
 from ..Operation.PlaceBlockWithNBTData import PlaceBlockWithNBTData
-from ..Operation.Terminate import Terminate
 
 from ..Operation.structOfChest import ChestSlot, ChestData
```

### Comparing `BDXConverter-1.0.16/BDXConverter/General/Pool.py` & `BDXConverter-1.1.0/BDXConverter/General/Pool.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,10 +38,9 @@
         34: PlaceRuntimeBlockWithCommandBlockData(),
         35: PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID(),
         36: PlaceCommandBlockWithCommandBlockData(),
         37: PlaceRuntimeBlockWithChestData(),
         38: PlaceRuntimeBlockWithChestDataAndUint32RuntimeID(),
         39: AssignDebugData(),
         40: PlaceBlockWithChestData(),
-        41: PlaceBlockWithNBTData(),
-        88: Terminate()
+        41: PlaceBlockWithNBTData()
     }
```

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt16XValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt16YValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt16ZValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt16ZValue0.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt16ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt32XValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt32YValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt32ZValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt32ZValue0.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt32ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt8XValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt8YValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AddInt8ZValue.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AddInt8ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/AssignDebugData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/AssignDebugData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/CreateConstantString.py` & `BDXConverter-1.1.0/BDXConverter/Operation/CreateConstantString.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlock.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithBlockStates.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStates.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithChestData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithNBTData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithNBTData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceBlockWithRuntimeId.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceBlockWithRuntimeId.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlock.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py` & `BDXConverter-1.1.0/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/SetCommandBlockData.py` & `BDXConverter-1.1.0/BDXConverter/Operation/SetCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/UseRuntimeIDPool.py` & `BDXConverter-1.1.0/BDXConverter/Operation/UseRuntimeIDPool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/Operation/structOfChest.py` & `BDXConverter-1.1.0/BDXConverter/Operation/structOfChest.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/utils/marshalNBT.py` & `BDXConverter-1.1.0/BDXConverter/utils/marshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/utils/marshalNBT_OldVersion.py` & `BDXConverter-1.1.0/BDXConverter/utils/marshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/utils/unmarshalNBT.py` & `BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter/utils/unmarshalNBT_OldVersion.py` & `BDXConverter-1.1.0/BDXConverter/utils/unmarshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/BDXConverter.egg-info/PKG-INFO` & `BDXConverter-1.1.0/BDXConverter.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.0.16
+Version: 1.1.0
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -57,22 +57,23 @@
 `BDX Converter` 是一个轻量化的纯 `Python` 实现，它提供了基本的 `BDX` 解析、反解析、`JSON` 可视化和反可视化功能。 
 
 
 
 
 
 # 注意事项
+- 版本 `1.1.0` 不兼容之前的所有版本
 - 版本 `1.0.16` 在可视化和反可视化字典方面不兼容之前的版本
 
 
 
 
 
 # 快速上手
-您可以利用 [`BDXConverter/Converter/Converter.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/Converter.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
+您可以利用 [`BDXConverter/Converter/FileOperation.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/FileOperation.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
 
 
 
 
 
 # 🐍 Pypi Packages
 我们已将此存储库以 `BDXConverter` 的名字上载到 `Pypi` ，您可以通过 `pip install BDXConverter` 快速安装。
@@ -160,15 +161,15 @@
 
 
 
 
 
 # 待办列表
 - [ ] `API` 文档
-- [ ] 支持与 `签名` 有关的功能
+- [x] 支持与 `签名` 有关的功能
 - [ ] 可以将得到的 `Python Class` 进一步解析为建筑结构
 - [ ] 可以自由地转换 `BDX` 和其他建筑文件格式
```

### Comparing `BDXConverter-1.0.16/BDXConverter.egg-info/SOURCES.txt` & `BDXConverter-1.1.0/BDXConverter.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -3,16 +3,18 @@
 setup.py
 BDXConverter/__init__.py
 BDXConverter.egg-info/PKG-INFO
 BDXConverter.egg-info/SOURCES.txt
 BDXConverter.egg-info/dependency_links.txt
 BDXConverter.egg-info/requires.txt
 BDXConverter.egg-info/top_level.txt
-BDXConverter/Converter/ConvertErrorDefine.py
 BDXConverter/Converter/Converter.py
+BDXConverter/Converter/ErrorClassDefine.py
+BDXConverter/Converter/FileOperation.py
+BDXConverter/Converter/Signature.py
 BDXConverter/Converter/__init__.py
 BDXConverter/General/GeneralClass.py
 BDXConverter/General/Operation.py
 BDXConverter/General/Pool.py
 BDXConverter/General/__init__.py
 BDXConverter/Operation/AddInt16XValue.py
 BDXConverter/Operation/AddInt16YValue.py
@@ -45,15 +47,14 @@
 BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
 BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
 BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
 BDXConverter/Operation/SetCommandBlockData.py
 BDXConverter/Operation/SubtractXValue.py
 BDXConverter/Operation/SubtractYValue.py
 BDXConverter/Operation/SubtractZValue.py
-BDXConverter/Operation/Terminate.py
 BDXConverter/Operation/UseRuntimeIDPool.py
 BDXConverter/Operation/__init__.py
 BDXConverter/Operation/structOfChest.py
 BDXConverter/utils/__init__.py
 BDXConverter/utils/getByte.py
 BDXConverter/utils/getString.py
 BDXConverter/utils/marshalNBT.py
```

### Comparing `BDXConverter-1.0.16/LICENSE` & `BDXConverter-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.0.16/PKG-INFO` & `BDXConverter-1.1.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.0.16
+Version: 1.1.0
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -57,22 +57,23 @@
 `BDX Converter` 是一个轻量化的纯 `Python` 实现，它提供了基本的 `BDX` 解析、反解析、`JSON` 可视化和反可视化功能。 
 
 
 
 
 
 # 注意事项
+- 版本 `1.1.0` 不兼容之前的所有版本
 - 版本 `1.0.16` 在可视化和反可视化字典方面不兼容之前的版本
 
 
 
 
 
 # 快速上手
-您可以利用 [`BDXConverter/Converter/Converter.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/Converter.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
+您可以利用 [`BDXConverter/Converter/FileOperation.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/FileOperation.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
 
 
 
 
 
 # 🐍 Pypi Packages
 我们已将此存储库以 `BDXConverter` 的名字上载到 `Pypi` ，您可以通过 `pip install BDXConverter` 快速安装。
@@ -160,15 +161,15 @@
 
 
 
 
 
 # 待办列表
 - [ ] `API` 文档
-- [ ] 支持与 `签名` 有关的功能
+- [x] 支持与 `签名` 有关的功能
 - [ ] 可以将得到的 `Python Class` 进一步解析为建筑结构
 - [ ] 可以自由地转换 `BDX` 和其他建筑文件格式
```

### Comparing `BDXConverter-1.0.16/README.md` & `BDXConverter-1.1.0/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -43,22 +43,23 @@
 `BDX Converter` 是一个轻量化的纯 `Python` 实现，它提供了基本的 `BDX` 解析、反解析、`JSON` 可视化和反可视化功能。 
 
 
 
 
 
 # 注意事项
+- 版本 `1.1.0` 不兼容之前的所有版本
 - 版本 `1.0.16` 在可视化和反可视化字典方面不兼容之前的版本
 
 
 
 
 
 # 快速上手
-您可以利用 [`BDXConverter/Converter/Converter.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/Converter.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
+您可以利用 [`BDXConverter/Converter/FileOperation.py`](https://github.com/TriM-Organization/BDXConverter/blob/main/BDXConverter/Converter/FileOperation.py) 中已提供的 `4` 个函数来完成 `BDX` 文件和 `JSON` 文件的相关操作。 
 
 
 
 
 
 # 🐍 Pypi Packages
 我们已将此存储库以 `BDXConverter` 的名字上载到 `Pypi` ，您可以通过 `pip install BDXConverter` 快速安装。
@@ -146,15 +147,15 @@
 
 
 
 
 
 # 待办列表
 - [ ] `API` 文档
-- [ ] 支持与 `签名` 有关的功能
+- [x] 支持与 `签名` 有关的功能
 - [ ] 可以将得到的 `Python Class` 进一步解析为建筑结构
 - [ ] 可以自由地转换 `BDX` 和其他建筑文件格式
```

### Comparing `BDXConverter-1.0.16/setup.py` & `BDXConverter-1.1.0/setup.py`

 * *Files identical despite different names*

