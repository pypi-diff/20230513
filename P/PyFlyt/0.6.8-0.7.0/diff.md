# Comparing `tmp/PyFlyt-0.6.8.tar.gz` & `tmp/PyFlyt-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyFlyt-0.6.8.tar", last modified: Fri May 12 21:54:19 2023, max compression
+gzip compressed data, was "PyFlyt-0.7.0.tar", last modified: Fri May 12 22:23:11 2023, max compression
```

## Comparing `PyFlyt-0.6.8.tar` & `PyFlyt-0.7.0.tar`

### file list

```diff
@@ -1,76 +1,76 @@
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/
--rw-rw-r--   0 jet       (1000) jet       (1000)     1036 2022-11-23 13:24:51.000000 PyFlyt-0.6.8/LICENSE.txt
--rw-rw-r--   0 jet       (1000) jet       (1000)     4098 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PKG-INFO
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/
--rw-rw-r--   0 jet       (1000) jet       (1000)       85 2023-03-01 18:16:37.000000 PyFlyt-0.6.8/PyFlyt/__init__.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/core/
--rw-rw-r--   0 jet       (1000) jet       (1000)      178 2023-03-06 19:51:22.000000 PyFlyt-0.6.8/PyFlyt/core/__init__.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/core/abstractions/
--rw-rw-r--   0 jet       (1000) jet       (1000)      396 2023-05-12 20:44:00.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/__init__.py
--rw-rw-r--   0 jet       (1000) jet       (1000)      601 2023-05-12 19:45:35.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/base_controller.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    12406 2023-05-12 20:30:07.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/base_drone.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     2799 2023-05-12 21:50:26.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/base_wind_field.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    11845 2023-04-12 15:29:31.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/boosters.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     4454 2023-05-12 21:50:10.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/boring_bodies.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     7695 2023-04-12 15:30:11.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/camera.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     7376 2023-04-27 19:26:46.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/gimbals.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    15316 2023-05-12 20:44:00.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/lifting_surfaces.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     6757 2023-04-12 15:30:45.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/motors.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     1832 2023-03-10 22:15:27.000000 PyFlyt-0.6.8/PyFlyt/core/abstractions/pid.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    17933 2023-05-12 21:21:01.000000 PyFlyt-0.6.8/PyFlyt/core/aviary.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/core/drones/
--rw-rw-r--   0 jet       (1000) jet       (1000)      132 2023-04-07 22:16:41.000000 PyFlyt-0.6.8/PyFlyt/core/drones/__init__.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     9440 2023-04-12 14:34:17.000000 PyFlyt-0.6.8/PyFlyt/core/drones/fixedwing.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    18407 2023-05-12 21:51:00.000000 PyFlyt-0.6.8/PyFlyt/core/drones/quadx.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    11574 2023-05-12 21:46:35.000000 PyFlyt-0.6.8/PyFlyt/core/drones/rocket.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     2254 2023-03-01 18:23:35.000000 PyFlyt-0.6.8/PyFlyt/core/load_objs.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/core/wind/
--rw-rw-r--   0 jet       (1000) jet       (1000)       46 2023-05-12 21:08:07.000000 PyFlyt-0.6.8/PyFlyt/core/wind/__init__.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/gym_envs/
--rw-rw-r--   0 jet       (1000) jet       (1000)      798 2023-03-08 22:30:13.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/__init__.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/gym_envs/fixedwing_envs/
--rw-rw-r--   0 jet       (1000) jet       (1000)     9211 2023-04-07 18:01:10.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/fixedwing_envs/fixedwing_base_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     6228 2023-04-12 17:52:29.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/fixedwing_envs/fixedwing_waypoints_env.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/
--rw-rw-r--   0 jet       (1000) jet       (1000)     8945 2023-04-07 18:01:10.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_base_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)    10073 2023-03-13 17:50:38.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_gates_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     3973 2023-04-12 15:34:33.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_hover_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     6877 2023-04-12 17:52:31.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_waypoints_env.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/gym_envs/rocket_envs/
--rw-rw-r--   0 jet       (1000) jet       (1000)    11585 2023-04-08 01:12:26.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/rocket_envs/rocket_base_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     9736 2023-04-18 14:26:29.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/rocket_envs/rocket_landing_env.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     6306 2023-04-06 11:28:39.000000 PyFlyt-0.6.8/PyFlyt/gym_envs/waypoint_handler.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/
--rw-rw-r--   0 jet       (1000) jet       (1000)      441 2023-02-26 21:57:19.000000 PyFlyt-0.6.8/PyFlyt/models/landing_pad.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)     2533 2022-11-23 13:24:51.000000 PyFlyt-0.6.8/PyFlyt/models/race_gate.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)      452 2023-02-24 22:55:32.000000 PyFlyt-0.6.8/PyFlyt/models/target.urdf
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.118028 PyFlyt-0.6.8/PyFlyt/models/vehicles/
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/
--rw-rw-r--   0 jet       (1000) jet       (1000)   529735 2022-11-23 13:24:51.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2.dae
--rw-rw-r--   0 jet       (1000) jet       (1000)     2580 2023-03-10 23:54:13.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2x.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)     1265 2023-05-12 21:48:51.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2x.yaml
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/vehicles/fixedwing/
--rw-rw-r--   0 jet       (1000) jet       (1000)     4711 2023-03-10 23:51:03.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/fixedwing/fixedwing.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)     2558 2023-03-08 21:54:50.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/fixedwing/fixedwing.yaml
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/
--rw-rw-r--   0 jet       (1000) jet       (1000)     3501 2023-03-10 23:52:15.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)     1238 2023-03-10 23:21:42.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/primitive_drone.yaml
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/vehicles/quadplane/
--rw-rw-r--   0 jet       (1000) jet       (1000)     5907 2023-02-11 08:07:00.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/quadplane/quadplane.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)     2618 2023-02-11 08:07:00.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/quadplane/quadplane.yaml
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt/models/vehicles/rocket/
--rw-rw-r--   0 jet       (1000) jet       (1000)     7191 2023-04-02 23:10:49.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/rocket/rocket.urdf
--rw-rw-r--   0 jet       (1000) jet       (1000)      976 2023-04-12 14:42:21.000000 PyFlyt-0.6.8/PyFlyt/models/vehicles/rocket/rocket.yaml
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/PyFlyt.egg-info/
--rw-rw-r--   0 jet       (1000) jet       (1000)     4098 2023-05-12 21:54:19.000000 PyFlyt-0.6.8/PyFlyt.egg-info/PKG-INFO
--rw-rw-r--   0 jet       (1000) jet       (1000)     1968 2023-05-12 21:54:19.000000 PyFlyt-0.6.8/PyFlyt.egg-info/SOURCES.txt
--rw-rw-r--   0 jet       (1000) jet       (1000)        1 2023-05-12 21:54:19.000000 PyFlyt-0.6.8/PyFlyt.egg-info/dependency_links.txt
--rw-rw-r--   0 jet       (1000) jet       (1000)       43 2023-05-12 21:54:19.000000 PyFlyt-0.6.8/PyFlyt.egg-info/requires.txt
--rw-rw-r--   0 jet       (1000) jet       (1000)        7 2023-05-12 21:54:19.000000 PyFlyt-0.6.8/PyFlyt.egg-info/top_level.txt
--rw-rw-r--   0 jet       (1000) jet       (1000)     1162 2023-05-12 21:54:14.000000 PyFlyt-0.6.8/pyproject.toml
--rw-rw-r--   0 jet       (1000) jet       (1000)     2283 2023-04-27 19:14:33.000000 PyFlyt-0.6.8/readme.md
--rw-rw-r--   0 jet       (1000) jet       (1000)       38 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/setup.cfg
--rw-rw-r--   0 jet       (1000) jet       (1000)      462 2023-03-01 19:59:08.000000 PyFlyt-0.6.8/setup.py
-drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 21:54:19.122027 PyFlyt-0.6.8/tests/
--rw-rw-r--   0 jet       (1000) jet       (1000)     8567 2023-05-12 21:34:19.000000 PyFlyt-0.6.8/tests/test_core.py
--rw-rw-r--   0 jet       (1000) jet       (1000)     5300 2023-04-23 20:14:07.000000 PyFlyt-0.6.8/tests/test_gym_envs.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1036 2022-11-23 13:24:51.000000 PyFlyt-0.7.0/LICENSE.txt
+-rw-rw-r--   0 jet       (1000) jet       (1000)     4098 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PKG-INFO
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/
+-rw-rw-r--   0 jet       (1000) jet       (1000)       85 2023-03-01 18:16:37.000000 PyFlyt-0.7.0/PyFlyt/__init__.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/core/
+-rw-rw-r--   0 jet       (1000) jet       (1000)      178 2023-03-06 19:51:22.000000 PyFlyt-0.7.0/PyFlyt/core/__init__.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/core/abstractions/
+-rw-rw-r--   0 jet       (1000) jet       (1000)      396 2023-05-12 20:44:00.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/__init__.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)      601 2023-05-12 19:45:35.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/base_controller.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    12406 2023-05-12 20:30:07.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/base_drone.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2799 2023-05-12 21:50:26.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/base_wind_field.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    11845 2023-04-12 15:29:31.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/boosters.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     4454 2023-05-12 22:13:35.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/boring_bodies.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     7695 2023-04-12 15:30:11.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/camera.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     7376 2023-04-27 19:26:46.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/gimbals.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    15316 2023-05-12 22:13:14.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/lifting_surfaces.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     6757 2023-04-12 15:30:45.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/motors.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1832 2023-03-10 22:15:27.000000 PyFlyt-0.7.0/PyFlyt/core/abstractions/pid.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    17975 2023-05-12 22:20:50.000000 PyFlyt-0.7.0/PyFlyt/core/aviary.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/core/drones/
+-rw-rw-r--   0 jet       (1000) jet       (1000)      132 2023-04-07 22:16:41.000000 PyFlyt-0.7.0/PyFlyt/core/drones/__init__.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     9440 2023-04-12 14:34:17.000000 PyFlyt-0.7.0/PyFlyt/core/drones/fixedwing.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    18407 2023-05-12 22:08:36.000000 PyFlyt-0.7.0/PyFlyt/core/drones/quadx.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    11574 2023-05-12 21:46:35.000000 PyFlyt-0.7.0/PyFlyt/core/drones/rocket.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2254 2023-03-01 18:23:35.000000 PyFlyt-0.7.0/PyFlyt/core/load_objs.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/core/wind/
+-rw-rw-r--   0 jet       (1000) jet       (1000)       46 2023-05-12 21:08:07.000000 PyFlyt-0.7.0/PyFlyt/core/wind/__init__.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/gym_envs/
+-rw-rw-r--   0 jet       (1000) jet       (1000)      798 2023-03-08 22:30:13.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/__init__.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/gym_envs/fixedwing_envs/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     9211 2023-04-07 18:01:10.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/fixedwing_envs/fixedwing_base_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     6228 2023-04-12 17:52:29.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/fixedwing_envs/fixedwing_waypoints_env.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     8945 2023-04-07 18:01:10.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_base_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)    10073 2023-03-13 17:50:38.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_gates_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     3973 2023-04-12 15:34:33.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_hover_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     6877 2023-04-12 17:52:31.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_waypoints_env.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/gym_envs/rocket_envs/
+-rw-rw-r--   0 jet       (1000) jet       (1000)    11585 2023-04-08 01:12:26.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/rocket_envs/rocket_base_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     9736 2023-04-18 14:26:29.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/rocket_envs/rocket_landing_env.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     6306 2023-04-06 11:28:39.000000 PyFlyt-0.7.0/PyFlyt/gym_envs/waypoint_handler.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/
+-rw-rw-r--   0 jet       (1000) jet       (1000)      441 2023-02-26 21:57:19.000000 PyFlyt-0.7.0/PyFlyt/models/landing_pad.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2533 2022-11-23 13:24:51.000000 PyFlyt-0.7.0/PyFlyt/models/race_gate.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)      452 2023-02-24 22:55:32.000000 PyFlyt-0.7.0/PyFlyt/models/target.urdf
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt/models/vehicles/
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/
+-rw-rw-r--   0 jet       (1000) jet       (1000)   529735 2022-11-23 13:24:51.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2.dae
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2929 2023-05-12 22:15:04.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2x.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1262 2023-05-12 22:19:56.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2x.yaml
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/vehicles/fixedwing/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     4711 2023-03-10 23:51:03.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/fixedwing/fixedwing.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2558 2023-03-08 21:54:50.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/fixedwing/fixedwing.yaml
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     3850 2023-05-12 22:15:09.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1257 2023-05-12 22:17:02.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/primitive_drone.yaml
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/vehicles/quadplane/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     5907 2023-02-11 08:07:00.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/quadplane/quadplane.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2618 2023-02-11 08:07:00.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/quadplane/quadplane.yaml
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/PyFlyt/models/vehicles/rocket/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     7191 2023-04-02 23:10:49.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/rocket/rocket.urdf
+-rw-rw-r--   0 jet       (1000) jet       (1000)      976 2023-04-12 14:42:21.000000 PyFlyt-0.7.0/PyFlyt/models/vehicles/rocket/rocket.yaml
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.310949 PyFlyt-0.7.0/PyFlyt.egg-info/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     4098 2023-05-12 22:23:11.000000 PyFlyt-0.7.0/PyFlyt.egg-info/PKG-INFO
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1968 2023-05-12 22:23:11.000000 PyFlyt-0.7.0/PyFlyt.egg-info/SOURCES.txt
+-rw-rw-r--   0 jet       (1000) jet       (1000)        1 2023-05-12 22:23:11.000000 PyFlyt-0.7.0/PyFlyt.egg-info/dependency_links.txt
+-rw-rw-r--   0 jet       (1000) jet       (1000)       43 2023-05-12 22:23:11.000000 PyFlyt-0.7.0/PyFlyt.egg-info/requires.txt
+-rw-rw-r--   0 jet       (1000) jet       (1000)        7 2023-05-12 22:23:11.000000 PyFlyt-0.7.0/PyFlyt.egg-info/top_level.txt
+-rw-rw-r--   0 jet       (1000) jet       (1000)     1162 2023-05-12 22:23:04.000000 PyFlyt-0.7.0/pyproject.toml
+-rw-rw-r--   0 jet       (1000) jet       (1000)     2283 2023-04-27 19:14:33.000000 PyFlyt-0.7.0/readme.md
+-rw-rw-r--   0 jet       (1000) jet       (1000)       38 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/setup.cfg
+-rw-rw-r--   0 jet       (1000) jet       (1000)      462 2023-03-01 19:59:08.000000 PyFlyt-0.7.0/setup.py
+drwxrwxr-x   0 jet       (1000) jet       (1000)        0 2023-05-12 22:23:11.314949 PyFlyt-0.7.0/tests/
+-rw-rw-r--   0 jet       (1000) jet       (1000)     8567 2023-05-12 21:34:19.000000 PyFlyt-0.7.0/tests/test_core.py
+-rw-rw-r--   0 jet       (1000) jet       (1000)     5300 2023-04-23 20:14:07.000000 PyFlyt-0.7.0/tests/test_gym_envs.py
```

### Comparing `PyFlyt-0.6.8/LICENSE.txt` & `PyFlyt-0.7.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PKG-INFO` & `PyFlyt-0.7.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyFlyt
-Version: 0.6.8
+Version: 0.7.0
 Summary: UAV Flight Simulator Gymnasium Environments for Reinforcement Learning Research.
 Author-email: Jet <taijunjet@hotmail.com>
 License: MIT License
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
         in the Software without restriction, including without limitation the rights
```

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/base_controller.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/base_controller.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/base_drone.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/base_drone.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/base_wind_field.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/base_wind_field.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/boosters.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/boosters.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/boring_bodies.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/boring_bodies.py`

 * *Files 0% similar despite different names*

```diff
@@ -85,15 +85,15 @@
 
         # get all the velocities
         body_velocities = np.array([item[-2] for item in link_states])
 
         # query for wind if available and add to surface velocities
         if self.p.wind_field is not None:
             body_positions = np.array([item[0] for item in link_states])
-            body_velocities += self.p.wind_field(self.p.elapsed_time, body_positions)
+            body_velocities -= self.p.wind_field(self.p.elapsed_time, body_positions)
 
         # rotate all velocities to be in local frame
         body_velocities = np.matmul(rotation_matrix, body_velocities.T).T
 
         # update the variable
         self.local_body_velocities = body_velocities
```

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/camera.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/camera.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/gimbals.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/gimbals.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/lifting_surfaces.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/lifting_surfaces.py`

 * *Files 1% similar despite different names*

```diff
@@ -78,15 +78,15 @@
 
         # get all the velocities
         surface_velocities = np.array([item[-2] for item in link_states])
 
         # query for wind if available and add to surface velocities
         if self.p.wind_field is not None:
             surface_positions = np.array([item[0] for item in link_states])
-            surface_velocities += self.p.wind_field(
+            surface_velocities -= self.p.wind_field(
                 self.p.elapsed_time, surface_positions
             )
 
         # convert all to local velocities
         surface_velocities = np.matmul(rotation_matrix, surface_velocities.T).T
 
         # update the velocities of all surfaces
```

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/motors.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/motors.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/abstractions/pid.py` & `PyFlyt-0.7.0/PyFlyt/core/abstractions/pid.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/aviary.py` & `PyFlyt-0.7.0/PyFlyt/core/aviary.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 """The Aviary class, the core of how PyFlyt handles UAVs in the PyBullet simulation environment."""
 from __future__ import annotations
 
 import time
 from itertools import repeat
-from typing import Any, Callable, Sequence, Type
+from typing import Any, Callable, Sequence
 from warnings import warn
 
 import numpy as np
 import pybullet as p
 import pybullet_data
 from pybullet_utils import bullet_client
 
@@ -199,15 +199,15 @@
                     physics_hz=self.physics_hz,
                     np_random=self.np_random,
                     **drone_options,
                 )
             )
 
         # initialize the wind field
-        self.wind_field: None | WindFieldClass
+        self.wind_field: None | WindFieldClass | Callable
         if self.wind_type is None:
             # no wind field
             self.wind_field = None
         elif isinstance(self.wind_type, str):
             # default wind fields
             assert self.wind_type in [], f"Unknown wind field model {self.wind_type}."
             self.wind_field = None
@@ -265,14 +265,15 @@
         """For less complicated wind field models (time invariant models), this allows the registration of a normal function as a wind field model.
 
         Args:
             wind_field (Callable): given the time float and a position as an (n, 3) array, must return a (n, 3) array representing the local wind velocity.
         """
         assert callable(wind_field), "`wind_field` function must be callable."
         WindFieldClass._check_wind_field_validity(wind_field)
+        self.wind_field = wind_field
 
     def state(self, index: DroneIndex) -> np.ndarray:
         """Returns the state for the indexed drone.
 
         Args:
             index (DRONE_INDEX): index
```

### Comparing `PyFlyt-0.6.8/PyFlyt/core/drones/fixedwing.py` & `PyFlyt-0.7.0/PyFlyt/core/drones/fixedwing.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/drones/quadx.py` & `PyFlyt-0.7.0/PyFlyt/core/drones/quadx.py`

 * *Files 0% similar despite different names*

```diff
@@ -135,15 +135,15 @@
 
             # simulate the drag on the main body
             self.body = BoringBodies(
                 p=self.p,
                 physics_period=self.physics_period,
                 np_random=self.np_random,
                 uav_id=self.Id,
-                body_ids=np.array([0]),
+                body_ids=np.array([4]),
                 drag_coefs=np.array([[drag_params["drag_coef_xyz"]] * 3]),
                 normal_areas=np.array([[drag_params["drag_area_xyz"]] * 3]),
             )
 
             self.Kp_ang_vel = np.array(ctrl_params["ang_vel"]["kp"])
             self.Ki_ang_vel = np.array(ctrl_params["ang_vel"]["ki"])
             self.Kd_ang_vel = np.array(ctrl_params["ang_vel"]["kd"])
```

### Comparing `PyFlyt-0.6.8/PyFlyt/core/drones/rocket.py` & `PyFlyt-0.7.0/PyFlyt/core/drones/rocket.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/core/load_objs.py` & `PyFlyt-0.7.0/PyFlyt/core/load_objs.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/__init__.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/__init__.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/fixedwing_envs/fixedwing_base_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/fixedwing_envs/fixedwing_base_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/fixedwing_envs/fixedwing_waypoints_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/fixedwing_envs/fixedwing_waypoints_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_base_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_base_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_gates_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_gates_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_hover_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_hover_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/quadx_envs/quadx_waypoints_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/quadx_envs/quadx_waypoints_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/rocket_envs/rocket_base_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/rocket_envs/rocket_base_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/rocket_envs/rocket_landing_env.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/rocket_envs/rocket_landing_env.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/gym_envs/waypoint_handler.py` & `PyFlyt-0.7.0/PyFlyt/gym_envs/waypoint_handler.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/race_gate.urdf` & `PyFlyt-0.7.0/PyFlyt/models/race_gate.urdf`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2.dae` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2.dae`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2x.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2x.urdf`

 * *Files 3% similar despite different names*

#### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2x.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2x.urdf`

```diff
@@ -79,8 +79,21 @@
       <inertia ixx="0" ixy="0" ixz="0" iyy="0" iyz="0" izz="0"/>
     </inertial>
   </link>
   <joint name="center_of_mass_joint" type="fixed">
     <parent link="base_link"/>
     <child link="center_of_mass_link"/>
   </joint>
+  <link name="body">
+    <inertial>
+      <origin rpy="0 0 0" xyz="0 0 0"/>
+      <mass value="0"/>
+      <inertia ixx="0" ixy="0" ixz="0" iyy="0" iyz="0" izz="0"/>
+    </inertial>
+  </link>
+  <joint name="body_link" type="fixed">
+    <parent link="base_link"/>
+    <child link="body"/>
+    <origin xyz="0 0 0"/>
+    <axis xyz="0 0 0"/>
+  </joint>
 </robot>
```

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/cf2x/cf2x.yaml` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/cf2x/cf2x.yaml`

 * *Files 1% similar despite different names*

```diff
@@ -2,16 +2,16 @@
   total_thrust: 2.0
   thrust_coef: 3.16e-10
   torque_coef: 7.94e-12
   noise_ratio: 0.02
   tau: 0.01
 
 drag_params:
-  drag_coef_xyz: 1.0e-3
-  drag_area_xyz: 8.0e-6
+  drag_coef_xyz: 3.0
+  drag_area_xyz: 4.0e-4
   drag_coef_pqr: 1.0e-4
 
 control_params:
   ang_vel:
     description: "input: angular velocity command | output: normalized angular torque command"
     kp: [4.0e-2, 4.0e-2, 8.0e-2]
     ki: [5.0e-7, 5.0e-7, 2.7e-4]
```

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/fixedwing/fixedwing.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/fixedwing/fixedwing.urdf`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/fixedwing/fixedwing.yaml` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/fixedwing/fixedwing.yaml`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf`

 * *Files 12% similar despite different names*

#### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/primitive_drone.urdf`

```diff
@@ -122,8 +122,21 @@
   <joint name="base_to_back_right_prop" type="fixed">
     <parent link="base_link"/>
     <child link="back_right_prop"/>
     <!-- joint of child is xyz away from parent -->
     <origin xyz="-0.16 -0.16 0"/>
     <axis xyz="1 0 0"/>
   </joint>
+  <link name="body">
+    <inertial>
+      <origin rpy="0 0 0" xyz="0 0 0"/>
+      <mass value="0"/>
+      <inertia ixx="0" ixy="0" ixz="0" iyy="0" iyz="0" izz="0"/>
+    </inertial>
+  </link>
+  <joint name="body_link" type="fixed">
+    <parent link="base_link"/>
+    <child link="body"/>
+    <origin xyz="0 0 0"/>
+    <axis xyz="0 0 0"/>
+  </joint>
 </robot>
```

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/primitive_drone/primitive_drone.yaml` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/primitive_drone/primitive_drone.yaml`

 * *Files 8% similar despite different names*

```diff
@@ -2,15 +2,16 @@
   total_thrust: 40
   thrust_coef: 3.0e-7
   torque_coef: 3.0e-7
   noise_ratio: 0.003
   tau: 0.01
 
 drag_params:
-  drag_coef_xyz: 1.0e-3
+  drag_coef_xyz: 2.0
+  drag_area_xyz: 0.08
   drag_coef_pqr: 1.0e-4
 
 control_params:
   ang_vel:
     description: "input: angular velocity command | output: normalized angular torque command"
     kp: [5.0e-3, 5.0e-3, 1.8e-3]
     ki: [1.0e-5, 1.0e-5, 2.0e-6]
```

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/quadplane/quadplane.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/quadplane/quadplane.urdf`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/quadplane/quadplane.yaml` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/quadplane/quadplane.yaml`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/rocket/rocket.urdf` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/rocket/rocket.urdf`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt/models/vehicles/rocket/rocket.yaml` & `PyFlyt-0.7.0/PyFlyt/models/vehicles/rocket/rocket.yaml`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/PyFlyt.egg-info/PKG-INFO` & `PyFlyt-0.7.0/PyFlyt.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyFlyt
-Version: 0.6.8
+Version: 0.7.0
 Summary: UAV Flight Simulator Gymnasium Environments for Reinforcement Learning Research.
 Author-email: Jet <taijunjet@hotmail.com>
 License: MIT License
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
         of this software and associated documentation files (the "Software"), to deal
         in the Software without restriction, including without limitation the rights
```

### Comparing `PyFlyt-0.6.8/PyFlyt.egg-info/SOURCES.txt` & `PyFlyt-0.7.0/PyFlyt.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/pyproject.toml` & `PyFlyt-0.7.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "PyFlyt"
-version = "0.6.8"
+version = "0.7.0"
 authors = [
   { name="Jet", email="taijunjet@hotmail.com" },
 ]
 description = "UAV Flight Simulator Gymnasium Environments for Reinforcement Learning Research."
 readme = "readme.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `PyFlyt-0.6.8/readme.md` & `PyFlyt-0.7.0/readme.md`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/tests/test_core.py` & `PyFlyt-0.7.0/tests/test_core.py`

 * *Files identical despite different names*

### Comparing `PyFlyt-0.6.8/tests/test_gym_envs.py` & `PyFlyt-0.7.0/tests/test_gym_envs.py`

 * *Files identical despite different names*

