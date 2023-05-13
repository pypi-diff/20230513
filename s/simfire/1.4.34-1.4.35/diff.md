# Comparing `tmp/simfire-1.4.34.tar.gz` & `tmp/simfire-1.4.35.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simfire-1.4.34.tar", max compression
+gzip compressed data, was "simfire-1.4.35.tar", max compression
```

## Comparing `simfire-1.4.34.tar` & `simfire-1.4.35.tar`

### file list

```diff
@@ -1,65 +1,65 @@
--rw-r--r--   0        0        0    10789 2023-05-09 00:16:40.286229 simfire-1.4.34/LICENSE
--rw-r--r--   0        0        0     2688 2023-05-09 00:16:40.286229 simfire-1.4.34/README.md
--rw-r--r--   0        0        0     1852 2023-05-09 00:16:40.466230 simfire-1.4.34/pyproject.toml
--rw-r--r--   0        0        0     1111 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/__init__.py
--rw-r--r--   0        0        0    10729 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/enums.py
--rw-r--r--   0        0        0       37 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/__init__.py
--rw-r--r--   0        0        0      874 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/_tests/__init__.py
--rw-r--r--   0        0        0    15523 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/_tests/test_game.py
--rw-r--r--   0        0        0     9928 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/_tests/test_sprites.py
--rw-r--r--   0        0        0    14937 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/game.py
--rw-r--r--   0        0        0     1318 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/image.py
--rw-r--r--   0        0        0      379 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/managers/__init__.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/managers/_tests/__init__.py
--rw-r--r--   0        0        0    18385 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/managers/_tests/test_fire.py
--rw-r--r--   0        0        0     8301 2023-05-09 00:16:40.466230 simfire-1.4.34/simfire/game/managers/_tests/test_mitigation.py
--rw-r--r--   0        0        0    29762 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/game/managers/fire.py
--rw-r--r--   0        0        0     7321 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/game/managers/mitigation.py
--rw-r--r--   0        0        0    15972 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/game/sprites.py
--rw-r--r--   0        0        0       49 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/sim/__init__.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/sim/_tests/__init__.py
--rw-r--r--   0        0        0    14392 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/sim/_tests/test_simulation.py
--rw-r--r--   0        0        0    37815 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/sim/simulation.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/__init__.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/__init__.py
--rw-r--r--   0        0        0     2771 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_config.py
--rw-r--r--   0        0        0     1925 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_configs/test_config.yml
--rw-r--r--   0        0        0       47 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_bad.yml
--rw-r--r--   0        0        0     1874 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_flat_simple.yml
--rw-r--r--   0        0        0     1876 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_gaussian.yml
--rw-r--r--   0        0        0     1851 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_rothermel_manager.yml
--rw-r--r--   0        0        0     4693 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_graph.py
--rw-r--r--   0        0        0    17172 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_layers.py
--rw-r--r--   0        0        0      622 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_log.py
--rw-r--r--   0        0        0     4495 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_terrain.py
--rw-r--r--   0        0        0     1472 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/_tests/test_units.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/assets/__init__.py
--rw-r--r--   0        0        0     1854 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/assets/fireline_logo.png
--rw-r--r--   0        0        0    38910 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/config.py
--rw-r--r--   0        0        0      499 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/decorators.py
--rw-r--r--   0        0        0     4153 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/generate_cfd_wind_layer.py
--rw-r--r--   0        0        0    10189 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/graph.py
--rw-r--r--   0        0        0    51105 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/layers.py
--rw-r--r--   0        0        0     2030 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/log.py
--rw-r--r--   0        0        0   143776 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/pregenerated_wind_files/generated_wind_directions.npy
--rw-r--r--   0        0        0   143776 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/pregenerated_wind_files/generated_wind_magnitudes.npy
--rw-r--r--   0        0        0     3647 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/terrain.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/textures/__init__.py
--rw-r--r--   0        0        0   204702 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/textures/terrain.jpg
--rw-r--r--   0        0        0     2555 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/utils/units.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/__init__.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/_tests/__init__.py
--rw-r--r--   0        0        0     2184 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/_tests/test_cfd_wind.py
--rw-r--r--   0        0        0     2423 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/_tests/test_elevation_functions.py
--rw-r--r--   0        0        0     2821 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/_tests/test_rothermel.py
--rw-r--r--   0        0        0     1466 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/_tests/test_wind.py
--rw-r--r--   0        0        0     3703 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/elevation_functions.py
--rw-r--r--   0        0        0     1054 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/fuel_array_functions.py
--rw-r--r--   0        0        0     2306 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/parameters.py
--rw-r--r--   0        0        0     2083 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/presets.py
--rw-r--r--   0        0        0     4306 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/rothermel.py
--rw-r--r--   0        0        0        0 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/wind_mechanics/__init__.py
--rw-r--r--   0        0        0     8781 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/wind_mechanics/cfd_wind.py
--rw-r--r--   0        0        0     3132 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/wind_mechanics/perlin_wind.py
--rw-r--r--   0        0        0     6578 2023-05-09 00:16:40.470231 simfire-1.4.34/simfire/world/wind_mechanics/wind_controller.py
--rw-r--r--   0        0        0     3862 1970-01-01 00:00:00.000000 simfire-1.4.34/PKG-INFO
+-rw-r--r--   0        0        0    10789 2023-05-13 00:23:54.660832 simfire-1.4.35/LICENSE
+-rw-r--r--   0        0        0     2662 2023-05-13 00:23:54.660832 simfire-1.4.35/README.md
+-rw-r--r--   0        0        0     1852 2023-05-13 00:23:54.892849 simfire-1.4.35/pyproject.toml
+-rw-r--r--   0        0        0     1111 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/__init__.py
+-rw-r--r--   0        0        0    10729 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/enums.py
+-rw-r--r--   0        0        0       37 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/__init__.py
+-rw-r--r--   0        0        0      874 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/_tests/__init__.py
+-rw-r--r--   0        0        0    15523 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/_tests/test_game.py
+-rw-r--r--   0        0        0     9928 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/_tests/test_sprites.py
+-rw-r--r--   0        0        0    14937 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/game.py
+-rw-r--r--   0        0        0     1318 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/image.py
+-rw-r--r--   0        0        0      379 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/managers/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/managers/_tests/__init__.py
+-rw-r--r--   0        0        0    18385 2023-05-13 00:23:54.892849 simfire-1.4.35/simfire/game/managers/_tests/test_fire.py
+-rw-r--r--   0        0        0     8301 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/game/managers/_tests/test_mitigation.py
+-rw-r--r--   0        0        0    29762 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/game/managers/fire.py
+-rw-r--r--   0        0        0     7321 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/game/managers/mitigation.py
+-rw-r--r--   0        0        0    15972 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/game/sprites.py
+-rw-r--r--   0        0        0       49 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/sim/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/sim/_tests/__init__.py
+-rw-r--r--   0        0        0    14392 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/sim/_tests/test_simulation.py
+-rw-r--r--   0        0        0    37815 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/sim/simulation.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/__init__.py
+-rw-r--r--   0        0        0     2771 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_config.py
+-rw-r--r--   0        0        0     1925 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_configs/test_config.yml
+-rw-r--r--   0        0        0       47 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_bad.yml
+-rw-r--r--   0        0        0     1874 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_flat_simple.yml
+-rw-r--r--   0        0        0     1876 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_gaussian.yml
+-rw-r--r--   0        0        0     1851 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_rothermel_manager.yml
+-rw-r--r--   0        0        0     4693 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_graph.py
+-rw-r--r--   0        0        0    17172 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_layers.py
+-rw-r--r--   0        0        0      622 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_log.py
+-rw-r--r--   0        0        0     4495 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_terrain.py
+-rw-r--r--   0        0        0     1472 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/_tests/test_units.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/assets/__init__.py
+-rw-r--r--   0        0        0     1854 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/assets/fireline_logo.png
+-rw-r--r--   0        0        0    38910 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/config.py
+-rw-r--r--   0        0        0      499 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/decorators.py
+-rw-r--r--   0        0        0     4153 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/generate_cfd_wind_layer.py
+-rw-r--r--   0        0        0    10189 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/graph.py
+-rw-r--r--   0        0        0    51105 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/layers.py
+-rw-r--r--   0        0        0     2030 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/log.py
+-rw-r--r--   0        0        0   143776 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/pregenerated_wind_files/generated_wind_directions.npy
+-rw-r--r--   0        0        0   143776 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/pregenerated_wind_files/generated_wind_magnitudes.npy
+-rw-r--r--   0        0        0     3647 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/terrain.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.896849 simfire-1.4.35/simfire/utils/textures/__init__.py
+-rw-r--r--   0        0        0   204702 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/utils/textures/terrain.jpg
+-rw-r--r--   0        0        0     2555 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/utils/units.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/_tests/__init__.py
+-rw-r--r--   0        0        0     2184 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/_tests/test_cfd_wind.py
+-rw-r--r--   0        0        0     2423 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/_tests/test_elevation_functions.py
+-rw-r--r--   0        0        0     2821 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/_tests/test_rothermel.py
+-rw-r--r--   0        0        0     1466 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/_tests/test_wind.py
+-rw-r--r--   0        0        0     3703 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/elevation_functions.py
+-rw-r--r--   0        0        0     1054 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/fuel_array_functions.py
+-rw-r--r--   0        0        0     2306 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/parameters.py
+-rw-r--r--   0        0        0     2083 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/presets.py
+-rw-r--r--   0        0        0     4306 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/rothermel.py
+-rw-r--r--   0        0        0        0 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/wind_mechanics/__init__.py
+-rw-r--r--   0        0        0     8781 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/wind_mechanics/cfd_wind.py
+-rw-r--r--   0        0        0     3132 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/wind_mechanics/perlin_wind.py
+-rw-r--r--   0        0        0     6578 2023-05-13 00:23:54.900849 simfire-1.4.35/simfire/world/wind_mechanics/wind_controller.py
+-rw-r--r--   0        0        0     3836 1970-01-01 00:00:00.000000 simfire-1.4.35/PKG-INFO
```

### Comparing `simfire-1.4.34/LICENSE` & `simfire-1.4.35/LICENSE`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/README.md` & `simfire-1.4.35/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -2,28 +2,28 @@
 
 <p align="center">
     <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/icons/rl_logo_horizontal.png">
 </p>
 
 ## Introduction
 
-SimFire uses [PyGame](https://www.pygame.org/wiki/about) to display and simulate different fire spread models, including the Rothermel Surface fire spread model described in [this](https://www.fs.fed.us/rm/pubs_series/rmrs/gtr/rmrs_gtr371.pdf) paper.
+SimFire uses [PyGame](https://www.pygame.org/wiki/about) to display and simulate different fire spread models, including the Rothermel Surface fire spread model described in [this](https://www.fs.usda.gov/rm/pubs_series/rmrs/gtr/rmrs_gtr371.pdf) paper.
 
 For more comprehensive documentation, go to our [docs page](https://mitrefireline.github.io/simfire).
 
 
 ## Running the Simulation
 <figure>
     <p align="center">
         <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/gifs/simulation_33.06N_116.58W.gif" width="225" />
         <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/gifs/simulation_39.67N_119.80W.gif" width="225" />
+        <br><b>Left: Fire simulated near Julian, CA. Right: Fire simulated near Reno, NV.
+        <br>Both fires have winds from the east at 20mph<b>
     </p>
-    <figcaption align = "center"><b>Left: Fire simulated near Julian, CA. Right: Fire simulated near Reno, NV.
-                                    <br>Both fires have winds from the east at 20mph<b></figcaption>
-</figure>
+ </figure>
 
 Install `simfire` by following the [installation instructions](#installing-the-package). Then run the `run_game.py` script:
 
 ```shell
 python run_game.py
 ```
 
@@ -73,11 +73,14 @@
 
 # Turn off rendering so the display disappears and the simulation continues to run in the background
 sim.rendering = False
 ```
 
 ## Installing the Package
 
+```shell
+pip install simfire
+```
 
 ## Contributing
 
 For contributing, see the [Contribution Page](https://mitrefireline.github.io/simfire/contributing.html) in our [docs](https://mitrefireline.github.io/simfire).
```

### Comparing `simfire-1.4.34/pyproject.toml` & `simfire-1.4.35/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "simfire"
-version = "1.4.34"
+version = "1.4.35"
 description = "Fire simulator built in Python"
 authors = ["Tim Welsh <twelsh@mitre.org>", "Marissa Dotter <mdotter@mitre.org>",
            "Michael Doyle <mdoyle@mitre.org>", "Dhanuj Gandikota <dgandikota@mitre.org>",
            "Chris Kempis <ckempis@mitre.org>", "Lauren Schambach <lschambach@mitre.org>",
            "Alex Tapley <atapley@mitre.org>", "Michael Threet <mthreet@mitre.org>"]
 readme = "README.md"
 include = ["simfire/utils/textures/terrain.jpg", "simfire/utils/assets/fireline_logo.png"]
```

### Comparing `simfire-1.4.34/simfire/__init__.py` & `simfire-1.4.35/simfire/__init__.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/enums.py` & `simfire-1.4.35/simfire/enums.py`

 * *Files 0% similar despite different names*

```diff
@@ -127,15 +127,15 @@
         SIGMA: Surface-area-to-volume ratio (ft^2/ft^3) min and max.
     """
 
     W_0_MIN: float = 0.0
     W_0_MAX: float = 1.0
     DELTA_MIN: float = 0.2
     DELTA_MAX: float = 6.0
-    M_X_MIN: float = 0.15
+    M_X_MIN: float = 0.12
     M_X_MAX: float = 1.0
     SIGMA_MIN: int = 1
     SIGMA_MAX: int = 3500
 
 
 @dataclass
 class ElevationConstants:
```

### Comparing `simfire-1.4.34/simfire/game/_tests/__init__.py` & `simfire-1.4.35/simfire/game/_tests/__init__.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/_tests/test_game.py` & `simfire-1.4.35/simfire/game/_tests/test_game.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/_tests/test_sprites.py` & `simfire-1.4.35/simfire/game/_tests/test_sprites.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/game.py` & `simfire-1.4.35/simfire/game/game.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/image.py` & `simfire-1.4.35/simfire/game/image.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/managers/_tests/test_fire.py` & `simfire-1.4.35/simfire/game/managers/_tests/test_fire.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/managers/_tests/test_mitigation.py` & `simfire-1.4.35/simfire/game/managers/_tests/test_mitigation.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/managers/fire.py` & `simfire-1.4.35/simfire/game/managers/fire.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/managers/mitigation.py` & `simfire-1.4.35/simfire/game/managers/mitigation.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/game/sprites.py` & `simfire-1.4.35/simfire/game/sprites.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/sim/_tests/test_simulation.py` & `simfire-1.4.35/simfire/sim/_tests/test_simulation.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/sim/simulation.py` & `simfire-1.4.35/simfire/sim/simulation.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_config.py` & `simfire-1.4.35/simfire/utils/_tests/test_config.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_configs/test_config.yml` & `simfire-1.4.35/simfire/utils/_tests/test_configs/test_config.yml`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_flat_simple.yml` & `simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_flat_simple.yml`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_gaussian.yml` & `simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_gaussian.yml`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_configs/test_config_rothermel_manager.yml` & `simfire-1.4.35/simfire/utils/_tests/test_configs/test_config_rothermel_manager.yml`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_graph.py` & `simfire-1.4.35/simfire/utils/_tests/test_graph.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_layers.py` & `simfire-1.4.35/simfire/utils/_tests/test_layers.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_log.py` & `simfire-1.4.35/simfire/utils/_tests/test_log.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_terrain.py` & `simfire-1.4.35/simfire/utils/_tests/test_terrain.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/_tests/test_units.py` & `simfire-1.4.35/simfire/utils/_tests/test_units.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/assets/fireline_logo.png` & `simfire-1.4.35/simfire/utils/assets/fireline_logo.png`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/config.py` & `simfire-1.4.35/simfire/utils/config.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/generate_cfd_wind_layer.py` & `simfire-1.4.35/simfire/utils/generate_cfd_wind_layer.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/graph.py` & `simfire-1.4.35/simfire/utils/graph.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/layers.py` & `simfire-1.4.35/simfire/utils/layers.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/log.py` & `simfire-1.4.35/simfire/utils/log.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/pregenerated_wind_files/generated_wind_directions.npy` & `simfire-1.4.35/simfire/utils/pregenerated_wind_files/generated_wind_directions.npy`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/pregenerated_wind_files/generated_wind_magnitudes.npy` & `simfire-1.4.35/simfire/utils/pregenerated_wind_files/generated_wind_magnitudes.npy`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/terrain.py` & `simfire-1.4.35/simfire/utils/terrain.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/textures/terrain.jpg` & `simfire-1.4.35/simfire/utils/textures/terrain.jpg`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/utils/units.py` & `simfire-1.4.35/simfire/utils/units.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/_tests/test_cfd_wind.py` & `simfire-1.4.35/simfire/world/_tests/test_cfd_wind.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/_tests/test_elevation_functions.py` & `simfire-1.4.35/simfire/world/_tests/test_elevation_functions.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/_tests/test_rothermel.py` & `simfire-1.4.35/simfire/world/_tests/test_rothermel.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/_tests/test_wind.py` & `simfire-1.4.35/simfire/world/_tests/test_wind.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/elevation_functions.py` & `simfire-1.4.35/simfire/world/elevation_functions.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/fuel_array_functions.py` & `simfire-1.4.35/simfire/world/fuel_array_functions.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/parameters.py` & `simfire-1.4.35/simfire/world/parameters.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/presets.py` & `simfire-1.4.35/simfire/world/presets.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/rothermel.py` & `simfire-1.4.35/simfire/world/rothermel.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/wind_mechanics/cfd_wind.py` & `simfire-1.4.35/simfire/world/wind_mechanics/cfd_wind.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/wind_mechanics/perlin_wind.py` & `simfire-1.4.35/simfire/world/wind_mechanics/perlin_wind.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/simfire/world/wind_mechanics/wind_controller.py` & `simfire-1.4.35/simfire/world/wind_mechanics/wind_controller.py`

 * *Files identical despite different names*

### Comparing `simfire-1.4.34/PKG-INFO` & `simfire-1.4.35/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simfire
-Version: 1.4.34
+Version: 1.4.35
 Summary: Fire simulator built in Python
 Home-page: https://gitlab.mitre.org/fireline/simfire
 Keywords: python,reinforcement learning,simulation,fire
 Author: Tim Welsh
 Author-email: twelsh@mitre.org
 Requires-Python: >=3.9,<3.10
 Classifier: Programming Language :: Python :: 3
@@ -32,28 +32,28 @@
 
 <p align="center">
     <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/icons/rl_logo_horizontal.png">
 </p>
 
 ## Introduction
 
-SimFire uses [PyGame](https://www.pygame.org/wiki/about) to display and simulate different fire spread models, including the Rothermel Surface fire spread model described in [this](https://www.fs.fed.us/rm/pubs_series/rmrs/gtr/rmrs_gtr371.pdf) paper.
+SimFire uses [PyGame](https://www.pygame.org/wiki/about) to display and simulate different fire spread models, including the Rothermel Surface fire spread model described in [this](https://www.fs.usda.gov/rm/pubs_series/rmrs/gtr/rmrs_gtr371.pdf) paper.
 
 For more comprehensive documentation, go to our [docs page](https://mitrefireline.github.io/simfire).
 
 
 ## Running the Simulation
 <figure>
     <p align="center">
         <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/gifs/simulation_33.06N_116.58W.gif" width="225" />
         <img src="https://raw.githubusercontent.com/mitrefireline/simfire/main/assets/gifs/simulation_39.67N_119.80W.gif" width="225" />
+        <br><b>Left: Fire simulated near Julian, CA. Right: Fire simulated near Reno, NV.
+        <br>Both fires have winds from the east at 20mph<b>
     </p>
-    <figcaption align = "center"><b>Left: Fire simulated near Julian, CA. Right: Fire simulated near Reno, NV.
-                                    <br>Both fires have winds from the east at 20mph<b></figcaption>
-</figure>
+ </figure>
 
 Install `simfire` by following the [installation instructions](#installing-the-package). Then run the `run_game.py` script:
 
 ```shell
 python run_game.py
 ```
 
@@ -103,12 +103,15 @@
 
 # Turn off rendering so the display disappears and the simulation continues to run in the background
 sim.rendering = False
 ```
 
 ## Installing the Package
 
+```shell
+pip install simfire
+```
 
 ## Contributing
 
 For contributing, see the [Contribution Page](https://mitrefireline.github.io/simfire/contributing.html) in our [docs](https://mitrefireline.github.io/simfire).
```

