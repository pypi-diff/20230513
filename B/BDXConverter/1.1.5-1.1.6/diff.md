# Comparing `tmp/BDXConverter-1.1.5.tar.gz` & `tmp/BDXConverter-1.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BDXConverter-1.1.5.tar", last modified: Sat May 13 14:34:35 2023, max compression
+gzip compressed data, was "BDXConverter-1.1.6.tar", last modified: Sat May 13 14:43:45 2023, max compression
```

## Comparing `BDXConverter-1.1.5.tar` & `BDXConverter-1.1.6.tar`

### file list

```diff
@@ -1,72 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.383227 BDXConverter-1.1.5/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.359227 BDXConverter-1.1.5/BDXConverter/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.363227 BDXConverter-1.1.5/BDXConverter/Converter/
--rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Converter/Converter.py
--rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Converter/ErrorClassDefine.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Converter/FileOperation.py
--rw-r--r--   0 runner    (1001) docker     (123)    10968 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Converter/Signature.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.367227 BDXConverter-1.1.5/BDXConverter/General/
--rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/General/GeneralClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/General/Operation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/General/Pool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/General/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.379227 BDXConverter-1.1.5/BDXConverter/Operation/
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt16XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt16YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt16ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt16ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt32XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt32YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt32ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt32ZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt8XValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt8YValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddInt8ZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AddZValue0.py
--rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/AssignDebugData.py
--rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/CreateConstantString.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/NOP.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithBlockStates.py
--rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithNBTData.py
--rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/SetCommandBlockData.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/SubtractXValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/SubtractYValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/SubtractZValue.py
--rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/UseRuntimeIDPool.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/Operation/structOfChest.py
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.383227 BDXConverter-1.1.5/BDXConverter/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/getByte.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/getString.py
--rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/marshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/marshalNBT_OldVersion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/unmarshalNBT.py
--rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/BDXConverter/utils/unmarshalNBT_OldVersion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:34:35.359227 BDXConverter-1.1.5/BDXConverter.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6010 2023-05-13 14:34:35.000000 BDXConverter-1.1.5/BDXConverter.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 14:34:35.000000 BDXConverter-1.1.5/BDXConverter.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:34:35.000000 BDXConverter-1.1.5/BDXConverter.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:34:35.000000 BDXConverter-1.1.5/BDXConverter.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 14:34:35.000000 BDXConverter-1.1.5/BDXConverter.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1090 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6010 2023-05-13 14:34:35.383227 BDXConverter-1.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5482 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:34:35.383227 BDXConverter-1.1.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 14:34:19.000000 BDXConverter-1.1.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.258452 BDXConverter-1.1.6/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.226451 BDXConverter-1.1.6/BDXConverter/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.234451 BDXConverter-1.1.6/BDXConverter/Converter/
+-rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Converter/Converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Converter/ErrorClassDefine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Converter/FileOperation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10968 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Converter/Signature.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.234451 BDXConverter-1.1.6/BDXConverter/General/
+-rw-r--r--   0 runner    (1001) docker     (123)     1684 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/General/GeneralClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2604 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/General/Operation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/General/Pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/General/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.250451 BDXConverter-1.1.6/BDXConverter/Operation/
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt16XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt16YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt16ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      530 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt16ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt32XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt32YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      529 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt32ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      531 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt32ZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt8XValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt8YValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddInt8ZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AddZValue0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1379 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/AssignDebugData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      545 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/CreateConstantString.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/NOP.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithBlockStates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      805 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2536 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithNBTData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithRuntimeId.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1798 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/SetCommandBlockData.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/SubtractXValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/SubtractYValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/SubtractZValue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      541 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/UseRuntimeIDPool.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/Operation/structOfChest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.254451 BDXConverter-1.1.6/BDXConverter/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/getByte.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/getString.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3204 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/marshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3201 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/marshalNBT_OldVersion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/unmarshalNBT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3075 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/BDXConverter/utils/unmarshalNBT_OldVersion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 14:43:45.230451 BDXConverter-1.1.6/BDXConverter.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6015 2023-05-13 14:43:45.000000 BDXConverter-1.1.6/BDXConverter.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2547 2023-05-13 14:43:45.000000 BDXConverter-1.1.6/BDXConverter.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 14:43:45.000000 BDXConverter-1.1.6/BDXConverter.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-05-13 14:43:45.000000 BDXConverter-1.1.6/BDXConverter.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-05-13 14:43:45.000000 BDXConverter-1.1.6/BDXConverter.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     6015 2023-05-13 14:43:45.254451 BDXConverter-1.1.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5487 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 14:43:45.258452 BDXConverter-1.1.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1004 2023-05-13 14:43:32.000000 BDXConverter-1.1.6/setup.py
```

### Comparing `BDXConverter-1.1.5/BDXConverter/Converter/Converter.py` & `BDXConverter-1.1.6/BDXConverter/Converter/Converter.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Converter/ErrorClassDefine.py` & `BDXConverter-1.1.6/BDXConverter/Converter/ErrorClassDefine.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Converter/FileOperation.py` & `BDXConverter-1.1.6/BDXConverter/Converter/FileOperation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Converter/Signature.py` & `BDXConverter-1.1.6/BDXConverter/Converter/Signature.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/General/GeneralClass.py` & `BDXConverter-1.1.6/BDXConverter/General/GeneralClass.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/General/Operation.py` & `BDXConverter-1.1.6/BDXConverter/General/Operation.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/General/Pool.py` & `BDXConverter-1.1.6/BDXConverter/General/Pool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt16XValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt16XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt16YValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt16YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt16ZValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt16ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt16ZValue0.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt16ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt32XValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt32XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt32YValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt32YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt32ZValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt32ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt32ZValue0.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt32ZValue0.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt8XValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt8XValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt8YValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt8YValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AddInt8ZValue.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AddInt8ZValue.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/AssignDebugData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/AssignDebugData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/CreateConstantString.py` & `BDXConverter-1.1.6/BDXConverter/Operation/CreateConstantString.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlock.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithBlockStates.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithBlockStates.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithBlockStatesDeprecated.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithChestData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithNBTData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithNBTData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceBlockWithRuntimeId.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceBlockWithRuntimeId.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceCommandBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlock.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlock.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithChestData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithChestDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py` & `BDXConverter-1.1.6/BDXConverter/Operation/PlaceRuntimeBlockWithCommandBlockDataAndUint32RuntimeID.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/SetCommandBlockData.py` & `BDXConverter-1.1.6/BDXConverter/Operation/SetCommandBlockData.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/UseRuntimeIDPool.py` & `BDXConverter-1.1.6/BDXConverter/Operation/UseRuntimeIDPool.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/Operation/structOfChest.py` & `BDXConverter-1.1.6/BDXConverter/Operation/structOfChest.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/utils/marshalNBT.py` & `BDXConverter-1.1.6/BDXConverter/utils/marshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/utils/marshalNBT_OldVersion.py` & `BDXConverter-1.1.6/BDXConverter/utils/marshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/utils/unmarshalNBT.py` & `BDXConverter-1.1.6/BDXConverter/utils/unmarshalNBT.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter/utils/unmarshalNBT_OldVersion.py` & `BDXConverter-1.1.6/BDXConverter/utils/unmarshalNBT_OldVersion.py`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/BDXConverter.egg-info/PKG-INFO` & `BDXConverter-1.1.6/BDXConverter.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.5
+Version: 1.1.6
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -85,15 +85,15 @@
 我们配置了自动化 `CD/CI 工作流` ，因此如果您是本项目的 `协作者` ，您可以通过更改 `version` 文件或通过手动触发的方式启动工作流，它会自动编译本项目并将将其上载到 `Pypi` 中。
 
 _[注：我们建议您在 `Python 3.10` 及以上的版本使用本项目，`3.7` 及以下的版本已不再受到 `Python` 的维护和更新]_
 
 
 
 # 第三方依赖
-本项目使用了 `brotli, nbtlib, pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
+本项目使用了 `brotli, nbtlib` 和 `pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
 
 ```
 pip install brotli
 pip install nbtlib
 pip install pycryptodome
 ```
```

### Comparing `BDXConverter-1.1.5/BDXConverter.egg-info/SOURCES.txt` & `BDXConverter-1.1.6/BDXConverter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `BDXConverter-1.1.5/LICENSE` & `BDXConverter-1.1.6/LICENSE`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 MIT License
 
 Copyright (c) 2023 Minecraft Muti-Media Organization
+Copyright (c) 2023 All the contributors of TriM-Organization/BDXConverter <https://github.com/TriM-Organization/BDXConverter>
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `BDXConverter-1.1.5/PKG-INFO` & `BDXConverter-1.1.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BDXConverter
-Version: 1.1.5
+Version: 1.1.6
 Summary: A code library to marshal, unmarshal, visual and reverse visualization of BDX files
 Home-page: https://github.com/TriM-Organization/BDXConverter
 Author: Minecraft Muti-Media Organization
 Author-email: TriM-Organization@hotmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -85,15 +85,15 @@
 我们配置了自动化 `CD/CI 工作流` ，因此如果您是本项目的 `协作者` ，您可以通过更改 `version` 文件或通过手动触发的方式启动工作流，它会自动编译本项目并将将其上载到 `Pypi` 中。
 
 _[注：我们建议您在 `Python 3.10` 及以上的版本使用本项目，`3.7` 及以下的版本已不再受到 `Python` 的维护和更新]_
 
 
 
 # 第三方依赖
-本项目使用了 `brotli, nbtlib, pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
+本项目使用了 `brotli, nbtlib` 和 `pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
 
 ```
 pip install brotli
 pip install nbtlib
 pip install pycryptodome
 ```
```

### Comparing `BDXConverter-1.1.5/README.md` & `BDXConverter-1.1.6/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -71,15 +71,15 @@
 我们配置了自动化 `CD/CI 工作流` ，因此如果您是本项目的 `协作者` ，您可以通过更改 `version` 文件或通过手动触发的方式启动工作流，它会自动编译本项目并将将其上载到 `Pypi` 中。
 
 _[注：我们建议您在 `Python 3.10` 及以上的版本使用本项目，`3.7` 及以下的版本已不再受到 `Python` 的维护和更新]_
 
 
 
 # 第三方依赖
-本项目使用了 `brotli, nbtlib, pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
+本项目使用了 `brotli, nbtlib` 和 `pycryptodome` 总计 `3` 个第三方库，您可以通过在 `终端` 逐一地执行以下命令以安装它们。
 
 ```
 pip install brotli
 pip install nbtlib
 pip install pycryptodome
 ```
```

### Comparing `BDXConverter-1.1.5/setup.py` & `BDXConverter-1.1.6/setup.py`

 * *Files identical despite different names*

