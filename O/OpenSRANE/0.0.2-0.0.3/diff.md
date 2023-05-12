# Comparing `tmp/OpenSRANE-0.0.2.tar.gz` & `tmp/OpenSRANE-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OpenSRANE-0.0.2.tar", last modified: Fri May  5 18:30:38 2023, max compression
+gzip compressed data, was "OpenSRANE-0.0.3.tar", last modified: Fri May 12 22:41:43 2023, max compression
```

## Comparing `OpenSRANE-0.0.2.tar` & `OpenSRANE-0.0.3.tar`

### file list

```diff
@@ -1,139 +1,139 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.024228 OpenSRANE-0.0.2/OpenSRANE.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      551 2023-05-05 18:30:37.000000 OpenSRANE-0.0.2/OpenSRANE.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3966 2023-05-05 18:30:37.000000 OpenSRANE-0.0.2/OpenSRANE.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-05 18:30:37.000000 OpenSRANE-0.0.2/OpenSRANE.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       39 2023-05-05 18:30:37.000000 OpenSRANE-0.0.2/OpenSRANE.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-05 18:30:37.000000 OpenSRANE-0.0.2/OpenSRANE.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      551 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/All/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/All/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4098 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/All/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/All/empty.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/Analyze/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     9632 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/ScenarioAnalyze.py
--rw-r--r--   0 runner    (1001) docker     (123)     4891 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_DispSprd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4923 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_Frag_OutFlow.py
--rw-r--r--   0 runner    (1001) docker     (123)    17005 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_NodesGroupsVulnerability.py
--rw-r--r--   0 runner    (1001) docker     (123)     5718 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_PhysicalAssign.py
--rw-r--r--   0 runner    (1001) docker     (123)     9235 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_PhysicalEffects.py
--rw-r--r--   0 runner    (1001) docker     (123)     4954 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_Prob_OutFlow.py
--rw-r--r--   0 runner    (1001) docker     (123)     2882 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_Sampling.py
--rw-r--r--   0 runner    (1001) docker     (123)     4597 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/_ZeroLevel.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Analyze/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/Connectors/
--rw-r--r--   0 runner    (1001) docker     (123)     4679 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Connectors/DS_LOC.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Connectors/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     5190 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Connectors/Out_Physic.py
--rw-r--r--   0 runner    (1001) docker     (123)     4931 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Connectors/Pb_LOC.py
--rw-r--r--   0 runner    (1001) docker     (123)     2509 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Connectors/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/DateAndTime/
--rw-r--r--   0 runner    (1001) docker     (123)     2701 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DateAndTime/DateTime.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DateAndTime/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DateAndTime/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.028228 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/
--rw-r--r--   0 runner    (1001) docker     (123)    21663 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/BritterMcQuaid.py
--rw-r--r--   0 runner    (1001) docker     (123)    29223 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/GasGaussian.py
--rw-r--r--   0 runner    (1001) docker     (123)     8244 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/LiquidSpread.py
--rw-r--r--   0 runner    (1001) docker     (123)    38372 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/LqdSprdGaussianGasDisp.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     9589 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.032228 OpenSRANE-0.0.2/opensrane/Fragilities/
--rw-r--r--   0 runner    (1001) docker     (123)     4525 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Fragilities/Fragility.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Fragilities/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4422 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Fragilities/Probit.py
--rw-r--r--   0 runner    (1001) docker     (123)     2083 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Fragilities/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Fragilities/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.032228 OpenSRANE-0.0.2/opensrane/Hazard/
--rw-r--r--   0 runner    (1001) docker     (123)     3388 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Hazard/Earthquake.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Hazard/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Hazard/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Hazard/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.032228 OpenSRANE-0.0.2/opensrane/Misc/
--rw-r--r--   0 runner    (1001) docker     (123)     7112 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Misc/MiscFuncs.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Misc/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Misc/WarningRecorder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2393 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Misc/_NewClass.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Misc/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.032228 OpenSRANE-0.0.2/opensrane/NodesGroups/
--rw-r--r--   0 runner    (1001) docker     (123)     4796 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/NodesGroups/Nodes.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/NodesGroups/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4567 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/NodesGroups/RectangNodes.py
--rw-r--r--   0 runner    (1001) docker     (123)     4548 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/NodesGroups/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/NodesGroups/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.032228 OpenSRANE-0.0.2/opensrane/OutFlowModel/
--rw-r--r--   0 runner    (1001) docker     (123)     7945 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/GasUnitHole.py
--rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/Liquid10min.py
--rw-r--r--   0 runner    (1001) docker     (123)     4056 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/NoOutFlow.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4621 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/SimultaniousGas.py
--rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/SimultaniousLiquid.py
--rw-r--r--   0 runner    (1001) docker     (123)     7586 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHole.py
--rw-r--r--   0 runner    (1001) docker     (123)     7978 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleDuration.py
--rw-r--r--   0 runner    (1001) docker     (123)     7949 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleFixStep.py
--rw-r--r--   0 runner    (1001) docker     (123)     7516 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleInitRate.py
--rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/OutFlowModel/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/PhysicalEffect/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2982 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/SAFE.py
--rw-r--r--   0 runner    (1001) docker     (123)    21265 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/Simple_fire_point_source.py
--rw-r--r--   0 runner    (1001) docker     (123)    12111 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/VCE_TNT.py
--rw-r--r--   0 runner    (1001) docker     (123)     7073 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21276 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PhysicalEffect/fire_point_source.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/PlantUnits/
--rw-r--r--   0 runner    (1001) docker     (123)     6044 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PlantUnits/ONGStorage.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PlantUnits/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     6455 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PlantUnits/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2901 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PlantUnits/_Position.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PlantUnits/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/Plot/
--rw-r--r--   0 runner    (1001) docker     (123)     7411 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Plot/Matplot.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Plot/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)    42461 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Plot/Plotly.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Plot/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/PostProcess/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PostProcess/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)    16740 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PostProcess/ObjsRecorderPP.py
--rw-r--r--   0 runner    (1001) docker     (123)    11762 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PostProcess/PlotPP.py
--rw-r--r--   0 runner    (1001) docker     (123)    20168 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PostProcess/RecorderPP.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/PostProcess/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/Recorders/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Recorders/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     9650 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Recorders/Objs_recorder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Recorders/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    19280 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Recorders/recorder.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/Safety/
--rw-r--r--   0 runner    (1001) docker     (123)     2854 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Safety/Dike.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Safety/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Safety/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Safety/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.036228 OpenSRANE-0.0.2/opensrane/Sites/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Sites/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3284 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Sites/Site.py
--rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Sites/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Sites/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/opensrane/Substance/
--rw-r--r--   0 runner    (1001) docker     (123)    13361 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Substance/DataBank.py
--rw-r--r--   0 runner    (1001) docker     (123)     6690 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Substance/Material.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Substance/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Substance/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/Substance/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/opensrane/WindData/
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/WindData/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     9303 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/WindData/WindRose.py
--rw-r--r--   0 runner    (1001) docker     (123)     2787 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/WindData/_GlobalParameters.py
--rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/WindData/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/opensrane/_New_module/
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/_New_module/New_class.py
--rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/_New_module/ObjManager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2507 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/_New_module/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2949 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2012 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/opensrane/version.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-05 18:30:38.040228 OpenSRANE-0.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2889 2023-05-05 18:30:25.000000 OpenSRANE-0.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.021426 OpenSRANE-0.0.3/OpenSRANE.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-12 22:41:42.000000 OpenSRANE-0.0.3/OpenSRANE.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3966 2023-05-12 22:41:42.000000 OpenSRANE-0.0.3/OpenSRANE.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-12 22:41:42.000000 OpenSRANE-0.0.3/OpenSRANE.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       39 2023-05-12 22:41:42.000000 OpenSRANE-0.0.3/OpenSRANE.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-05-12 22:41:42.000000 OpenSRANE-0.0.3/OpenSRANE.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      620 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      140 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.021426 OpenSRANE-0.0.3/opensrane/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.021426 OpenSRANE-0.0.3/opensrane/All/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/All/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4098 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/All/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/All/empty.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.021426 OpenSRANE-0.0.3/opensrane/Analyze/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9632 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/ScenarioAnalyze.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4891 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_DispSprd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4923 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_Frag_OutFlow.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17005 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_NodesGroupsVulnerability.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5718 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_PhysicalAssign.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9235 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_PhysicalEffects.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4954 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_Prob_OutFlow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2882 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_Sampling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4597 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/_ZeroLevel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Analyze/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.021426 OpenSRANE-0.0.3/opensrane/Connectors/
+-rw-r--r--   0 runner    (1001) docker     (123)     4679 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Connectors/DS_LOC.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Connectors/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5190 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Connectors/Out_Physic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4931 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Connectors/Pb_LOC.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2509 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Connectors/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/DateAndTime/
+-rw-r--r--   0 runner    (1001) docker     (123)     2701 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DateAndTime/DateTime.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DateAndTime/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DateAndTime/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/
+-rw-r--r--   0 runner    (1001) docker     (123)    21663 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/BritterMcQuaid.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29223 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/GasGaussian.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8244 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/LiquidSpread.py
+-rw-r--r--   0 runner    (1001) docker     (123)    38372 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/LqdSprdGaussianGasDisp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9589 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/Fragilities/
+-rw-r--r--   0 runner    (1001) docker     (123)     4525 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Fragilities/Fragility.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Fragilities/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4422 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Fragilities/Probit.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2083 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Fragilities/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Fragilities/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/Hazard/
+-rw-r--r--   0 runner    (1001) docker     (123)     3388 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Hazard/Earthquake.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Hazard/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Hazard/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Hazard/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/Misc/
+-rw-r--r--   0 runner    (1001) docker     (123)     7112 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Misc/MiscFuncs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Misc/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Misc/WarningRecorder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2393 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Misc/_NewClass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Misc/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/NodesGroups/
+-rw-r--r--   0 runner    (1001) docker     (123)     4796 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/NodesGroups/Nodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/NodesGroups/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4567 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/NodesGroups/RectangNodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4548 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/NodesGroups/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/NodesGroups/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/OutFlowModel/
+-rw-r--r--   0 runner    (1001) docker     (123)     7945 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/GasUnitHole.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3870 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/Liquid10min.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4056 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/NoOutFlow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4621 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/SimultaniousGas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4638 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/SimultaniousLiquid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7586 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHole.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7978 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleDuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7949 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleFixStep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7516 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleInitRate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/OutFlowModel/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.025426 OpenSRANE-0.0.3/opensrane/PhysicalEffect/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2982 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/SAFE.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21265 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/Simple_fire_point_source.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12111 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/VCE_TNT.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7073 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21276 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PhysicalEffect/fire_point_source.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/PlantUnits/
+-rw-r--r--   0 runner    (1001) docker     (123)     6044 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PlantUnits/ONGStorage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PlantUnits/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6455 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PlantUnits/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2901 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PlantUnits/_Position.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PlantUnits/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/Plot/
+-rw-r--r--   0 runner    (1001) docker     (123)     7411 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Plot/Matplot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Plot/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)    45542 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Plot/Plotly.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Plot/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/PostProcess/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PostProcess/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16740 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PostProcess/ObjsRecorderPP.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13639 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PostProcess/PlotPP.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20168 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PostProcess/RecorderPP.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/PostProcess/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/Recorders/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Recorders/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9650 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Recorders/Objs_recorder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Recorders/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19280 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Recorders/recorder.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/Safety/
+-rw-r--r--   0 runner    (1001) docker     (123)     2854 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Safety/Dike.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Safety/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Safety/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Safety/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/Sites/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Sites/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3284 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Sites/Site.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Sites/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Sites/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/Substance/
+-rw-r--r--   0 runner    (1001) docker     (123)    13361 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Substance/DataBank.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6599 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Substance/Material.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Substance/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2135 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Substance/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/Substance/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/WindData/
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/WindData/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9303 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/WindData/WindRose.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2787 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/WindData/_GlobalParameters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2508 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/WindData/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/opensrane/_New_module/
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/_New_module/New_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4281 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/_New_module/ObjManager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2507 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/_New_module/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2949 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2012 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/opensrane/version.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-12 22:41:43.029426 OpenSRANE-0.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2889 2023-05-12 22:41:32.000000 OpenSRANE-0.0.3/setup.py
```

### Comparing `OpenSRANE-0.0.2/OpenSRANE.egg-info/PKG-INFO` & `OpenSRANE-0.0.3/OpenSRANE.egg-info/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 Metadata-Version: 2.1
 Name: OpenSRANE
-Version: 0.0.2
+Version: 0.0.3
 Summary: Open Software for Risk Assessment of Natech Events
 Home-page: https://github.com/OpenSRANE/OpenSRANE
 Author: Bijan Sayyafzadeh
 Author-email: <OpenSRANE@Gmail.com>
 Keywords: python,NaTech,Modeling,Risk
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Operating System :: Microsoft :: Windows
 Description-Content-Type: text/markdown
 
 ## OpenSRANE
 
 ### Open Software for Risk Assessment of Natech Events
 
+Documentation: https://github.com/OpenSRANE/OpenSRANE_Documentation
+
```

### Comparing `OpenSRANE-0.0.2/OpenSRANE.egg-info/SOURCES.txt` & `OpenSRANE-0.0.3/OpenSRANE.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/PKG-INFO` & `OpenSRANE-0.0.3/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 Metadata-Version: 2.1
 Name: OpenSRANE
-Version: 0.0.2
+Version: 0.0.3
 Summary: Open Software for Risk Assessment of Natech Events
 Home-page: https://github.com/OpenSRANE/OpenSRANE
 Author: Bijan Sayyafzadeh
 Author-email: <OpenSRANE@Gmail.com>
 Keywords: python,NaTech,Modeling,Risk
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Operating System :: Microsoft :: Windows
 Description-Content-Type: text/markdown
 
 ## OpenSRANE
 
 ### Open Software for Risk Assessment of Natech Events
 
+Documentation: https://github.com/OpenSRANE/OpenSRANE_Documentation
+
```

### Comparing `OpenSRANE-0.0.2/opensrane/All/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/All/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/All/__init__.py` & `OpenSRANE-0.0.3/opensrane/All/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/All/empty.py` & `OpenSRANE-0.0.3/opensrane/All/empty.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Analyze/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/ScenarioAnalyze.py` & `OpenSRANE-0.0.3/opensrane/Analyze/ScenarioAnalyze.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_DispSprd.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_DispSprd.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_Frag_OutFlow.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_Frag_OutFlow.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_NodesGroupsVulnerability.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_NodesGroupsVulnerability.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_PhysicalAssign.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_PhysicalAssign.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_PhysicalEffects.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_PhysicalEffects.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_Prob_OutFlow.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_Prob_OutFlow.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_Sampling.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_Sampling.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/_ZeroLevel.py` & `OpenSRANE-0.0.3/opensrane/Analyze/_ZeroLevel.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Analyze/__init__.py` & `OpenSRANE-0.0.3/opensrane/Analyze/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Connectors/DS_LOC.py` & `OpenSRANE-0.0.3/opensrane/Connectors/DS_LOC.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Connectors/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Connectors/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Connectors/Out_Physic.py` & `OpenSRANE-0.0.3/opensrane/Connectors/Out_Physic.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Connectors/Pb_LOC.py` & `OpenSRANE-0.0.3/opensrane/Connectors/Pb_LOC.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Connectors/__init__.py` & `OpenSRANE-0.0.3/opensrane/Connectors/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DateAndTime/DateTime.py` & `OpenSRANE-0.0.3/opensrane/DateAndTime/DateTime.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DateAndTime/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/DateAndTime/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DateAndTime/__init__.py` & `OpenSRANE-0.0.3/opensrane/DateAndTime/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/BritterMcQuaid.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/BritterMcQuaid.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/GasGaussian.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/GasGaussian.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/LiquidSpread.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/LiquidSpread.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/LqdSprdGaussianGasDisp.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/LqdSprdGaussianGasDisp.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/DispersionSpreadModels/__init__.py` & `OpenSRANE-0.0.3/opensrane/DispersionSpreadModels/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Fragilities/Fragility.py` & `OpenSRANE-0.0.3/opensrane/Fragilities/Fragility.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Fragilities/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Fragilities/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Fragilities/Probit.py` & `OpenSRANE-0.0.3/opensrane/Fragilities/Probit.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Fragilities/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/Fragilities/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Fragilities/__init__.py` & `OpenSRANE-0.0.3/opensrane/Fragilities/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Hazard/Earthquake.py` & `OpenSRANE-0.0.3/opensrane/Hazard/Earthquake.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Hazard/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Hazard/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Hazard/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/Hazard/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Hazard/__init__.py` & `OpenSRANE-0.0.3/opensrane/Hazard/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Misc/MiscFuncs.py` & `OpenSRANE-0.0.3/opensrane/Misc/MiscFuncs.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Misc/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Misc/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Misc/WarningRecorder.py` & `OpenSRANE-0.0.3/opensrane/Misc/WarningRecorder.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Misc/_NewClass.py` & `OpenSRANE-0.0.3/opensrane/Misc/_NewClass.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Misc/__init__.py` & `OpenSRANE-0.0.3/opensrane/Misc/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/NodesGroups/Nodes.py` & `OpenSRANE-0.0.3/opensrane/NodesGroups/Nodes.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/NodesGroups/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/NodesGroups/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/NodesGroups/RectangNodes.py` & `OpenSRANE-0.0.3/opensrane/NodesGroups/RectangNodes.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/NodesGroups/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/NodesGroups/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/NodesGroups/__init__.py` & `OpenSRANE-0.0.3/opensrane/NodesGroups/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/GasUnitHole.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/GasUnitHole.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/Liquid10min.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/Liquid10min.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/NoOutFlow.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/NoOutFlow.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/SimultaniousGas.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/SimultaniousGas.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/SimultaniousLiquid.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/SimultaniousLiquid.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHole.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHole.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleDuration.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleDuration.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleFixStep.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleFixStep.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/TankHoleInitRate.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/TankHoleInitRate.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/OutFlowModel/__init__.py` & `OpenSRANE-0.0.3/opensrane/OutFlowModel/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/SAFE.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/SAFE.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/Simple_fire_point_source.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/Simple_fire_point_source.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/VCE_TNT.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/VCE_TNT.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/__init__.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PhysicalEffect/fire_point_source.py` & `OpenSRANE-0.0.3/opensrane/PhysicalEffect/fire_point_source.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PlantUnits/ONGStorage.py` & `OpenSRANE-0.0.3/opensrane/PlantUnits/ONGStorage.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PlantUnits/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/PlantUnits/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PlantUnits/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/PlantUnits/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PlantUnits/_Position.py` & `OpenSRANE-0.0.3/opensrane/PlantUnits/_Position.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PlantUnits/__init__.py` & `OpenSRANE-0.0.3/opensrane/PlantUnits/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Plot/Matplot.py` & `OpenSRANE-0.0.3/opensrane/Plot/Matplot.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Plot/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Plot/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Plot/Plotly.py` & `OpenSRANE-0.0.3/opensrane/Plot/Plotly.py`

 * *Files 2% similar despite different names*

```diff
@@ -38,14 +38,15 @@
 import random as _rnd
 import pandas as _pd
 import numpy as _np
 import math as _math
 import plotly.figure_factory as _ff
 # from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot
 from plotly.offline import iplot as _iplot
+from plotly.offline import plot as _plot
 from tqdm import tqdm as _tqdm
 
 '''
 
             # Get Geometry and Location Data and the Other required data
             xc=Unit.Hlocalcoord
             yc=Unit.Vlocalcoord
@@ -96,15 +97,15 @@
                                                                 ),
                                      )
                          )
                          
 '''
 
 
-def PlotWindRose(WindRoseTag,Draw_For_Day=True):
+def PlotWindRose(WindRoseTag,Draw_For_Day=True,PlotMode=1, width=None, height=None):
     #Figure Settings -------------------------------------------------------- 
     fig = _go.Figure()
     
     
     #Get WindRose Object
     obj=_opr.WindData.ObjManager.TagObjDict[WindRoseTag]
     
@@ -146,36 +147,52 @@
     #Plotly Settings ---------------------------------------------------------------------------------------------------------------------------------------
     fig.update_layout(
         title=title,
         font_size=16, legend_font_size=16,
         #polar_radialaxis_ticksuffix='%',
         polar_angularaxis_rotation=90,)
     
+    if height!=None:
+        fig.update_layout(height=height)
+    if width!=None:
+        fig.update_layout(width=width)
+
+
+    if PlotMode==3:
+        
+        return _iplot(fig)
+        
+    elif PlotMode==2:
+        
+        image_filename='WindDay.html' if Draw_For_Day==True else 'Windnight.html'
+        _plot(fig,filename=image_filename,config = dict({'scrollZoom': True}))
+        
+    else:
+        fig.show()
     
-    return _iplot(fig)
 
 
 def PlotUnits2D(PlotMode=1,OverPressureList=[],OverPressureHeight=2, OverPressurePointNumber=20,
                 RadiationList=[],RadiationHeight=2,RadiationPointNumber=20, 
-                GasConcentrationlist=[],GasConcentrationHeght=2,ConcentrationPointNumber=10,
-                ):
+                GasConcentrationlist=[],GasConcentrationHeght=2,ConcentrationPointNumber=10
+                ,raw=False, width=None, height=None):
     '''
     RadiationList: list of desired radiation values to be plotted 
     RadiationHeight: height of radiation calculations
     RadiationPointNumber: Radiation Boundary Points number To plot for
 
     OverPressureList: list of desired OverPressure values to be plotted 
     OverPressureHeight: height of OverPressure calculations
     OverPressurePointNumber: OverPressure Boundary Points number To plot for
     
     GasConcentrationlist: list of desired Concentration values to be plotted 
     GasConcentrationHeght: heght of Concentration calculations
     ConcentrationPointNumber: Concentration Points number for numeric calculations
     
-    
+    raw: Boolean that if consider as True means that just only plot the plant without showing any damages or other events.
     '''
     
     Plcollist=_PLcols.DEFAULT_PLOTLY_COLORS*20 #List of plotly Colors
     Plcollist=['rgb(255, 0, 5)']+Plcollist[1:3]+Plcollist[4:]
     
     #Initial Figure Settings
     fig = _go.Figure()
@@ -194,15 +211,15 @@
     maxx=None
     miny=None
     maxy=None
     
     ArrowsDict={} #Dictionary that Stores the Damage level arrows
     
     #Plot Tanks
-    minx,maxx,miny,maxy=_PlotTanks(fig,PlotDamagedColor=True)
+    minx,maxx,miny,maxy=_PlotTanks(fig,PlotDamagedColor=True,raw=raw)
 
     
     for Unit in _tqdm(UnitObj,desc='Adding Units Data'):
         
         # Onground Tanks
         if Unit.__class__==_opr.PlantUnits.ONGStorage:
 
@@ -219,15 +236,15 @@
             
             PhysicalObjname=Unit.PhysicalEffectModelname
             PhysicalObj=Unit.PhysicalEffectObject
             
 
             
             #Draw Liquid Dispersion
-            if DispSprdModelname!=None:
+            if DispSprdModelname!=None and raw==False:
                 if LiquidCenter!=None:
                     
                     x0=LiquidCenter[0]
                     y0=LiquidCenter[1]
                     R=LiquidRadios
                     Phi=[i/20*2*_math.pi for i in range(20)]
                     x=[x0+R*_math.cos(phi) for phi in Phi]
@@ -251,15 +268,15 @@
                         if x0-R<minx: minx=x0-R
                         if x0+R>maxx: maxx=x0+R
                         if y0-R<miny: miny=y0-R
                         if y0+R>maxy: maxy=y0+R
                         
             
             #Draw Gas Dispersion for BritterMcQuaid Model (Should Be Modify for Specific Entered Concentrations in the list)
-            if DispSprdObj!=None and DispSprdObj.Title=='BritterMcQuaid' and GasConcentrationlist!=[]:
+            if DispSprdObj!=None and DispSprdObj.Title=='BritterMcQuaid' and GasConcentrationlist!=[] and raw==False:
                 CC0=[1,0.8,0.7,0.5,0.4,0.2,0.1,0.05,0.02,0.01,0.005,0.002]
                 P1s=[]
                 P2s=[]
                 Lvs=[]
                 for c in CC0:
                     P1,P2,Lv,Lu=DispSprdObj.GiveBoundary(c)
                     P1s.append(P1)
@@ -287,15 +304,15 @@
                     if min(min(L1x,L2x))<minx: minx=min(min(L1x,L2x))
                     if max(max(L1x,L2x))>maxx: maxx=max(max(L1x,L2x))
                     if min(min(L1y,L2y))<miny: miny=min(min(L1y,L2y))
                     if max(max(L1y,L2y))>maxy: maxy=max(max(L1y,L2y))   
             
             #Draw Gas Dispersion for LqdSprdGaussianGasDisp
 
-            if DispSprdObj!=None and (DispSprdObj.Title=='LqdSprdGaussianGasDisp' or DispSprdObj.Title=='GasGaussian') and GasConcentrationlist!=[]:
+            if DispSprdObj!=None and (DispSprdObj.Title=='LqdSprdGaussianGasDisp' or DispSprdObj.Title=='GasGaussian') and GasConcentrationlist!=[] and raw==False:
                 for C in GasConcentrationlist:
                     points=DispSprdObj.GiveBoundary(C=C,z=GasConcentrationHeght,SegmentNumbers=ConcentrationPointNumber,errpercent=1)
                     fillc=f'rgba(250, 250, 5,0.2)'
                     x=[p[0] for p in points]
                     y=[p[1] for p in points]
                     fig.add_scatter(x=x, y=y,mode='lines',line=dict(color=f'rgba(250, 250, 5,1)'),fill='toself',fillcolor=fillc,hoverinfo='none',name='GasDispersions',showlegend=False,legendgroup='GasDispersions', visible='legendonly')
                     
@@ -311,15 +328,15 @@
                         if max(x)>maxx: maxx=max(x)
                         if min(y)<miny: miny=min(y)
                         if max(y)>maxy: maxy=max(y)   
                            
       
             
             #Draw Radiation Boundary
-            if PhysicalObj!=None and RadiationList!=[]:
+            if PhysicalObj!=None and RadiationList!=[] and raw==False:
                 # print(f'start of radiation for unit {Unit.tag}')
                 
                 for Rad in RadiationList:
                     Results=PhysicalObj.RadiationBoundary(Rad,RadiationHeight,RadiationPointNumber)
                     if Results!=None:
                         points=Results.values()
                         x=[i[0] for i in points if i!=None]
@@ -337,15 +354,15 @@
                         if max(x)>maxx: maxx=max(x)
                         if min(y)<miny: miny=min(y)
                         if max(y)>maxy: maxy=max(y)
                 # print('end of radiation')    
         
         
             #Draw OverPressure boundary
-            if PhysicalObj!=None and OverPressureList!=[]:
+            if PhysicalObj!=None and OverPressureList!=[] and raw==False:
                 # print(f'start of OverPressure for unit {Unit.tag}')            
             
                 for OverP in OverPressureList:
                     Results=PhysicalObj.OverPressureBoundary(OverP, OverPressureHeight, OverPressurePointNumber)
                     if Results!=None and Results!=0 :
                         points=Results.values()
                         x=[i[0] for i in points if i!=None]
@@ -366,15 +383,15 @@
                         
                 # print('end of OverPressure') 
 
                 
         #Get DamageLevels Arrows Data
         
         
-        if Unit.DamageLevel!=None and Unit.DamageLevel>0:
+        if Unit.DamageLevel!=None and Unit.DamageLevel>0 and raw==False:
             
             #To consider multi damage sources (For radiations)
             DmSources=Unit.DamageSourceTag if type(Unit.DamageSourceTag)==list else [Unit.DamageSourceTag] 
             for dm in DmSources:
                 SourceUnitObj=_opr.PlantUnits.ObjManager[dm]
                 x,y=SourceUnitObj.Hlocalcoord, SourceUnitObj.Vlocalcoord
                 ax,ay=Unit.Hlocalcoord, Unit.Vlocalcoord
@@ -424,15 +441,15 @@
 
             Phi=[i/20*2*_math.pi for i in range(20)]
             x=[x0+R*_math.cos(phi) for phi in Phi]
             y=[y0+R*_math.sin(phi) for phi in Phi]
             
             fillDam=f'rgba(255, 0, 0,0.5)'
             fillUnDam=f'rgba(127, 127, 127,0.05)'
-            fig.add_scatter(x=x,y=y,fill='toself',fillcolor=fillDam if dam==True else fillUnDam,mode='lines',
+            fig.add_scatter(x=x,y=y,fill='toself',fillcolor=fillDam if (dam==True and raw==False) else fillUnDam,mode='lines',
                             line=dict(color=NodeGcol,width=1,
                             shape='spline',smoothing=0.9,simplify=False,),
                             hoverinfo='none',name='Vulnerable Object',showlegend=False,legendgroup=Type, visible='legendonly')
             
             fig.add_trace(_go.Scatter(x=[x0], y=[y0], mode='markers', name='Vulnerable Object',showlegend=False,legendgroup=Type,
                                       marker=dict(color=NodeGcol,size=2),
                                     
@@ -465,48 +482,52 @@
         
     # Add single TanksData for legend
     fig.add_trace(_go.Scatter(x=[None], y=[None], mode='markers',
                               marker=dict(size=8, color=ColBound),
                               name='TanksData',showlegend=True,legendgroup='TanksData',))
                               
     # Add single liquid dispersion for legend
-    fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+    if raw==False: fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
                               line=dict(color=f'rgba(1, 1, 1,0.01)'),
                               name='Liquid Dispersion',showlegend=True,legendgroup='Liquid Dispersion', visible='legendonly'))
                               
     # Add single GasDispersions for legend
-    fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+    if raw==False: fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
                               line=dict(color=f'rgba(250, 250, 5,1)'),
                               name='GasDispersions',showlegend=True,legendgroup='GasDispersions', visible='legendonly'))
     
     # Add single Radiation for legend
-    for Rad in RadiationList:
-        RadColor=f'rgba(250,50,0,{Rad/max(RadiationList)})'
-        fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
-                                  line=dict(color=RadColor),
-                                  name=f'Radiation{Rad}',showlegend=True,legendgroup=f'Radiation{Rad}', visible='legendonly'))
+    if raw==False: 
+        for Rad in RadiationList:
+            RadColor=f'rgba(250,50,0,{Rad/max(RadiationList)})'
+            fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+                                    line=dict(color=RadColor),
+                                    name=f'Radiation{Rad}',showlegend=True,legendgroup=f'Radiation{Rad}', visible='legendonly'))
 
     # Add single OverPressure for legend
-    for OverP in OverPressureList:
-        OverPColor=f'rgba(50,250,0,{OverP/max(OverPressureList)})'
-        fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
-                                  line=dict(color=OverPColor),
-                                  name=f'OverPressure{OverP}',showlegend=True,legendgroup=f'OverPressure{OverP}', visible='legendonly'))
+    if raw==False: 
+        for OverP in OverPressureList:
+            OverPColor=f'rgba(50,250,0,{OverP/max(OverPressureList)})'
+            fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+                                    line=dict(color=OverPColor),
+                                    name=f'OverPressure{OverP}',showlegend=True,legendgroup=f'OverPressure{OverP}', visible='legendonly'))
                                   
     # Add single Damage Level Arrows for legend
     #DamageLevel 0
-    if ArrowsDict!={}:
-        fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
-                                  line=dict(color='rgba'+Plcollist[0][3:-1]+', 0.3)'),
-                                  name=f'DamageLevel {0}',showlegend=True,legendgroup=f'DamageLevel {0}', visible='legendonly'))
+    if raw==False: 
+        if ArrowsDict!={}:
+            fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+                                    line=dict(color='rgba'+Plcollist[0][3:-1]+', 0.3)'),
+                                    name=f'DamageLevel {0}',showlegend=True,legendgroup=f'DamageLevel {0}', visible='legendonly'))
     #Other Damage Lavels
-    for dmlevel,values in ArrowsDict.items():
-        fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
-                                  line=dict(color='rgba'+Plcollist[dmlevel][3:-1]+', 0.3)'),
-                                  name=f'DamageLevel {dmlevel}',showlegend=True,legendgroup=f'DamageLevel {dmlevel}', visible='legendonly'))
+    if raw==False: 
+        for dmlevel,values in ArrowsDict.items():
+            fig.add_trace(_go.Scatter(x=[None], y=[None], mode='lines',
+                                    line=dict(color='rgba'+Plcollist[dmlevel][3:-1]+', 0.3)'),
+                                    name=f'DamageLevel {dmlevel}',showlegend=True,legendgroup=f'DamageLevel {dmlevel}', visible='legendonly'))
 
     # Add single NodesGroups for legend
     TypeSet=set()
     
     for node in NodesObjects:
         TypeSet.add(node.Type)
     
@@ -540,21 +561,32 @@
         miny=yc-L2/2
         maxy=yc+L2/2
             
             
     fig.update_xaxes(title_text='x',showline=True,linewidth=2, linecolor='black',range=[minx-0.05*L1, maxx+0.05*L1],title_font=dict(size=18, family='Courier', color='black')) #mirror=True
     fig.update_yaxes(title_text='y',showline=True,linewidth=2, linecolor='black',range=[miny-0.05*L2, maxy+0.05*L2],title_font=dict(size=18, family='Courier', color='black'))#,mirror=True
     
-    
-    if PlotMode==1:
-        fig.show(config = dict({'scrollZoom': True})) 
-    else:
+    if height!=None:
+        fig.update_layout(height=height)
+    if width!=None:
+        fig.update_layout(width=width)
+
+    if PlotMode==3:
+        
         return _iplot(fig)
+        
+    elif PlotMode==2:
+        
+        image_filename='PlotUnits2D.html'
+        _plot(fig,filename=image_filename, config = dict({'scrollZoom': True}))
+        
+    else:
+        fig.show(config = dict({'scrollZoom': True}))
 
-def PlotIndividualRisk( PlotMode=1, NodesGroupTag=1, NodesProbabilityList=[], ContorList=[]):
+def PlotIndividualRisk( PlotMode=1, NodesGroupTag=1, NodesProbabilityList=[], ContorList=[], width=None, height=None):
     '''
     NodesGroupTag: Tag of the nodesgroup that want to see its damage probability
     NodesProbabilityList: list of the nodes damage probability values. 
     ContorList: list of contor values
     
     
     '''
@@ -648,22 +680,36 @@
         L2=L1*Ratio
         miny=yc-L2/2
         maxy=yc+L2/2
             
             
     fig.update_xaxes(title_text='x',showline=True,linewidth=2, linecolor='black',range=[minx-0.05*L1, maxx+0.05*L1],title_font=dict(size=18, family='Courier', color='black')) #mirror=True
     fig.update_yaxes(title_text='y',showline=True,linewidth=2, linecolor='black',range=[miny-0.05*L2, maxy+0.05*L2],title_font=dict(size=18, family='Courier', color='black'))#,mirror=True
-      
+
+    if height!=None:
+        fig.update_layout(height=height)
+    if width!=None:
+        fig.update_layout(width=width)    
     
-    if PlotMode==1:
-        fig.show(config = dict({'scrollZoom': True})) 
+
+    if PlotMode==3:
+        
+        return _iplot(fig)
+        
+    elif PlotMode==2:
+        
+        image_filename='PlotIndividualRisk.html'
+        _plot(fig,filename=image_filename,config = dict({'scrollZoom': True}))
+        
     else:
-        return _iplot(fig)   
+        fig.show(config = dict({'scrollZoom': True}))
 
-def _PlotTanks(fig,PlotDamagedColor=True):
+def _PlotTanks(fig,PlotDamagedColor=True,raw=False):
+    
+    #raw: Boolean that if consider as True means that just only plot the plant without showing any damages or other events.
 
     Plcollist=_PLcols.DEFAULT_PLOTLY_COLORS*20 #List of plotly Colors
     Plcollist=['rgb(255, 0, 5)']+Plcollist[1:3]+Plcollist[4:]
 
     ColBound=f'rgba(0, 0, 0,1)' # Boundary Colors
     ColNodamage=f'rgba(250, 250, 250,0.2)' #Undamaged Colors
     ColDamaged=f'rgba(255, 0, 5,0.2 )' #Damaged Colors
@@ -713,15 +759,15 @@
                 if yc+D/2>maxy: maxy=yc+D/2
                 
            
             # Add Tank Shape
             fig.add_shape(type="circle", xref="x", yref="y", name=name,
                 x0=xc-D/2, y0=yc-D/2, x1=xc+D/2, y1=yc+D/2,
                 
-                line_color=ColBound ,fillcolor='rgba'+Plcollist[Unit.DamageLevel][3:-1]+', 0.3)' if (Unit.isdamaged==True and PlotDamagedColor==True and Unit.DamageLevel!=None) else ColNodamage,)
+                line_color=ColBound ,fillcolor='rgba'+Plcollist[Unit.DamageLevel][3:-1]+', 0.3)' if (Unit.isdamaged==True and PlotDamagedColor==True and Unit.DamageLevel!=None and raw==False) else ColNodamage,)
                 # 'rgba'+Plcollist[Unit.DamageLevel][3:-1]+', 0.1)' if (Unit.DamageLevel!=None and Unit.DamageLevel!=0) else
 
             #Add Tanks Center Point and Data                
             fig.add_trace(_go.Scatter(x=[xc], y=[yc], mode='markers', name='TanksData',showlegend=False,legendgroup='TanksData',
                                       marker=dict(color=ColBound),
                                      
                                       hoverinfo='text',
@@ -736,15 +782,15 @@
                                                 size=14,                            #or other size
                                                 color=f'rgba(255, 255, 255, 1)')
                                                                 ),
                                      )
                          )
     return minx,maxx,miny,maxy
     
-def PlotFragilities(StdNumber=3,NPoints=100, FragilityTagList=[]):
+def PlotFragilities(StdNumber=3,NPoints=100, FragilityTagList=[],PlotMode=1, width=None, height=None):
     '''
     All Fragilities that are defined by the user, Are drawn using This Function
     FragilityTagList = list of fragilities tag that user want to plot
     '''
 
     stdN=StdNumber
     N=NPoints
@@ -797,24 +843,40 @@
     if x!=[]: #Means that we have Fragilities
     
         #Plotly Settings ---------------------------------------------------------------------------------------------------------------------------------------
         fig.update_xaxes(title_text='Random Variables',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, max(x)],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
         fig.update_yaxes(title_text='Probability',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, 1.05],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
         fig.update_layout(title={'text': "Fragilities",'y':0.9,'x':0.13,'xanchor': 'center', 'yanchor': 'top'},height=800)
         fig.update_layout(legend=dict(yanchor="top",y=0.99,xanchor="left",x=0.01,bordercolor="Black", borderwidth=2))
+        
+        if height!=None:
+            fig.update_layout(height=height)
+        if width!=None:
+            fig.update_layout(width=width)
         #fig.update_traces(hovertemplate="<b>%{text}</b><br><br>" +"Random Variable: %{x}<br>" +"Probability: %{y}<br>" +"<extra></extra>",)
         
     
-        return _iplot(fig)
+        if PlotMode==3:
+        
+            return _iplot(fig)
+            
+        elif PlotMode==2:
+            
+            image_filename='PlotFragilities.html'
+            _plot(fig,filename=image_filename,config = dict({'scrollZoom': True}))
+            
+        else:
+            fig.show(config = dict({'scrollZoom': True}))
+
     else:
         print('There is No fragility function to Draw!')
 
 
 
-def PlotProbits(StdNumber=3,NPoints=100,ProbitTag=None):
+def PlotProbits(StdNumber=3,NPoints=100,ProbitTag=None,PlotMode=1,  width=None, height=None):
     '''
     All Fragilities that are defined by the user, Are drawn using This Function
     '''
 
     stdN=StdNumber
     N=NPoints
     
@@ -885,27 +947,42 @@
             
 
     if x!=[]: #Means that we have Fragilities
     
         #Plotly Settings ---------------------------------------------------------------------------------------------------------------------------------------
         fig.update_xaxes(title_text='Random Variables',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, max(x)],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
         fig.update_yaxes(title_text='Probability',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, 1.05],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
-        fig.update_layout(title={'text': "Probits",'y':0.9,'x':0.13,'xanchor': 'center', 'yanchor': 'top'},height=800)
+        fig.update_layout(title={'text': "Probits",'y':0.9,'x':0.13,'xanchor': 'center', 'yanchor': 'top'})
         fig.update_layout(legend=dict(yanchor="top",y=0.99,xanchor="left",x=0.01,bordercolor="Black", borderwidth=2))
+        if height!=None:
+            fig.update_layout(height=height)
+        if width!=None:
+            fig.update_layout(width=width)
         #fig.update_traces(hovertemplate="<b>%{text}</b><br><br>" +"Random Variable: %{x}<br>" +"Probability: %{y}<br>" +"<extra></extra>",)
         
     
-        return _iplot(fig)
+        if PlotMode==3:
+        
+            return _iplot(fig)
+            
+        elif PlotMode==2:
+            
+            image_filename='PlotProbits.html'
+            _plot(fig,filename=image_filename,config = dict({'scrollZoom': True}))
+            
+        else:
+            fig.show(config = dict({'scrollZoom': True}))
+        
     else:
         print('There is No fragility function to Draw!')
 
 
 
 
-def PlotHazard():
+def PlotHazard(PlotMode=1, width=None, height=None):
     '''
     The First Hazard Object that are defined by the user, is drawn using This Function
     '''
 
     
     #Get The first Hazard Object
     HazarbObj=_opr.Hazard.ObjManager.Objlst[0]
@@ -930,10 +1007,24 @@
 
 
     #Plotly Settings ---------------------------------------------------------------------------------------------------------------------------------------
     fig.update_xaxes(title_text='Magnitude',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, max(x)],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
     fig.update_yaxes(title_text='Probability',showline=True,linewidth=2, linecolor='black',mirror=True,range=[0, 1.05],title_font=dict(size=18, family='Courier', color='black'),showspikes=True)
     fig.update_layout(title={'text': "Hazard Curve",'y':0.92,'x':0.16,'xanchor': 'center', 'yanchor': 'top'},height=800,title_font=dict(size=22,  color='black'))
     fig.update_layout(legend=dict(yanchor="top",y=0.99,xanchor="right",x=0.99,bordercolor="Black", borderwidth=2))
+    if height!=None:
+        fig.update_layout(height=height)
+    if width!=None:
+        fig.update_layout(width=width)
+        
     
-    
-    return _iplot(fig)
+    if PlotMode==3:
+        
+            return _iplot(fig)
+            
+    elif PlotMode==2:
+        
+        image_filename='PlotHazard.html'
+        _plot(fig,filename=image_filename,config = dict({'scrollZoom': True}))
+        
+    else:
+        fig.show(config = dict({'scrollZoom': True}))
```

### Comparing `OpenSRANE-0.0.2/opensrane/Plot/__init__.py` & `OpenSRANE-0.0.3/opensrane/Plot/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PostProcess/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/PostProcess/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PostProcess/ObjsRecorderPP.py` & `OpenSRANE-0.0.3/opensrane/PostProcess/ObjsRecorderPP.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PostProcess/RecorderPP.py` & `OpenSRANE-0.0.3/opensrane/PostProcess/RecorderPP.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/PostProcess/__init__.py` & `OpenSRANE-0.0.3/opensrane/PostProcess/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Recorders/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Recorders/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Recorders/Objs_recorder.py` & `OpenSRANE-0.0.3/opensrane/Recorders/Objs_recorder.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Recorders/__init__.py` & `OpenSRANE-0.0.3/opensrane/Recorders/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Recorders/recorder.py` & `OpenSRANE-0.0.3/opensrane/Recorders/recorder.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Safety/Dike.py` & `OpenSRANE-0.0.3/opensrane/Safety/Dike.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Safety/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Safety/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Safety/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/Safety/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Safety/__init__.py` & `OpenSRANE-0.0.3/opensrane/Safety/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Sites/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Sites/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Sites/Site.py` & `OpenSRANE-0.0.3/opensrane/Sites/Site.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Sites/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/Sites/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Sites/__init__.py` & `OpenSRANE-0.0.3/opensrane/Sites/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Substance/DataBank.py` & `OpenSRANE-0.0.3/opensrane/Substance/DataBank.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Substance/Material.py` & `OpenSRANE-0.0.3/opensrane/Substance/Material.py`

 * *Files 1% similar despite different names*

```diff
@@ -34,22 +34,18 @@
 from .ObjManager import *
 from copy import deepcopy as _deepcopy
 from ._GlobalParameters import _GlobalParameters
 
 class Material(_NewClass, _GlobalParameters):
     
     
-    def __init__(self,tag,name='No name',isLiquidBooleanFunction=None,Density=None, GasDensity=None, BoilingPointGasDensity=None, LiquidPhaseSpreadModelTag=None, GasPhaseDispModelTag=None,
-        Dynamic_Viscousity=None,Molar_Heat_of_Combustion=None,Stoichiometric_Concentration=None,
-        Vapour_Density=None,Volumetric_Heat_Capacity=None,Molecular_Weight=None,Molar_Volume=None,
-        Boiling_Point=None,Critical_Pressure=None,Critical_Temperature=None,Melting_Point=None,Standard_Enthalpy_of_Formation=None,
-        Vapour_Pressure=None,Molar_Enthalpy_of_Vaporization=None,Specific_Heat_of_Vaporization=None,Molar_Heat_Capacity=None,
-        Specific_Heat_Capacity=None,Specific_Heat_Ratio=None,Autoignition_Temperature=None,Flash_Point=None,Specific_Heat_of_Combustion=None,
-        Lower_Flammability_Limit=None,Upper_Flammability_Limit=None, Bioconcentration_Factor=None,Liquid_Partial_Pressure_in_Atmosphere=None,
-        ):
+    def __init__(self,tag,name='No name', Density=None, GasDensity=None, BoilingPointGasDensity=None, 
+                 Dynamic_Viscousity=None,Molar_Heat_of_Combustion=None,Stoichiometric_Concentration=None,
+                 Vapour_Density=None,Volumetric_Heat_Capacity=None,Molecular_Weight=None,Molar_Volume=None,
+                 Boiling_Point=None,Critical_Pressure=None,Critical_Temperature=None,Melting_Point=None,Standard_Enthalpy_of_Formation=None, Vapour_Pressure=None,Molar_Enthalpy_of_Vaporization=None,Specific_Heat_of_Vaporization=None,Molar_Heat_Capacity=None, Specific_Heat_Capacity=None,Specific_Heat_Ratio=None,Autoignition_Temperature=None,Flash_Point=None,Specific_Heat_of_Combustion=None, Lower_Flammability_Limit=None,Upper_Flammability_Limit=None, Bioconcentration_Factor=None,Liquid_Partial_Pressure_in_Atmosphere=None, ):
          
         #---- Fix Part for each class __init__ ----
         ObjManager.Add(tag,self)
         _NewClass.__init__(self,tag)
         #------------------------------------------
 
         _GlobalParameters.__init__(self)
```

### Comparing `OpenSRANE-0.0.2/opensrane/Substance/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/Substance/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Substance/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/Substance/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/Substance/__init__.py` & `OpenSRANE-0.0.3/opensrane/Substance/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/WindData/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/WindData/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/WindData/WindRose.py` & `OpenSRANE-0.0.3/opensrane/WindData/WindRose.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/WindData/_GlobalParameters.py` & `OpenSRANE-0.0.3/opensrane/WindData/_GlobalParameters.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/WindData/__init__.py` & `OpenSRANE-0.0.3/opensrane/WindData/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/_New_module/New_class.py` & `OpenSRANE-0.0.3/opensrane/_New_module/New_class.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/_New_module/ObjManager.py` & `OpenSRANE-0.0.3/opensrane/_New_module/ObjManager.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/_New_module/__init__.py` & `OpenSRANE-0.0.3/opensrane/_New_module/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/__init__.py` & `OpenSRANE-0.0.3/opensrane/__init__.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/opensrane/version.py` & `OpenSRANE-0.0.3/opensrane/version.py`

 * *Files identical despite different names*

### Comparing `OpenSRANE-0.0.2/setup.py` & `OpenSRANE-0.0.3/setup.py`

 * *Files identical despite different names*

