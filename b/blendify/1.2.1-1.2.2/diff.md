# Comparing `tmp/blendify-1.2.1.tar.gz` & `tmp/blendify-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/blendify-1.2.1.tar", last modified: Wed May 10 12:12:42 2023, max compression
+gzip compressed data, was "dist/blendify-1.2.2.tar", last modified: Sat May 13 14:03:22 2023, max compression
```

## Comparing `blendify-1.2.1.tar` & `blendify-1.2.2.tar`

### file list

```diff
@@ -1,55 +1,55 @@
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/
--rw-r--r--   0 vguzov     (502) staff       (20)     5888 2023-05-10 12:12:42.000000 blendify-1.2.1/PKG-INFO
--rw-r--r--   0 vguzov     (502) staff       (20)     5516 2023-05-10 12:07:39.000000 blendify-1.2.1/README.md
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/
--rw-r--r--   0 vguzov     (502) staff       (20)      302 2023-05-10 12:07:11.000000 blendify-1.2.1/blendify/__init__.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/cameras/
--rw-r--r--   0 vguzov     (502) staff       (20)       58 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/cameras/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)     3071 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/cameras/base.py
--rw-r--r--   0 vguzov     (502) staff       (20)     5470 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/cameras/common.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/colors/
--rw-r--r--   0 vguzov     (502) staff       (20)      121 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/colors/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)      718 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/colors/base.py
--rw-r--r--   0 vguzov     (502) staff       (20)     2604 2023-05-03 18:18:43.000000 blendify-1.2.1/blendify/colors/common.py
--rw-r--r--   0 vguzov     (502) staff       (20)     3838 2023-04-24 18:05:40.000000 blendify-1.2.1/blendify/colors/texture.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/internal/
--rw-r--r--   0 vguzov     (502) staff       (20)       32 2021-12-06 17:55:11.000000 blendify-1.2.1/blendify/internal/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)     1886 2023-05-01 16:57:41.000000 blendify-1.2.1/blendify/internal/io.py
--rw-r--r--   0 vguzov     (502) staff       (20)     3925 2023-04-24 18:05:40.000000 blendify-1.2.1/blendify/internal/parser.py
--rw-r--r--   0 vguzov     (502) staff       (20)     3068 2023-05-01 15:22:56.000000 blendify-1.2.1/blendify/internal/positionable.py
--rw-r--r--   0 vguzov     (502) staff       (20)      575 2022-03-31 07:59:42.000000 blendify-1.2.1/blendify/internal/singleton.py
--rw-r--r--   0 vguzov     (502) staff       (20)     2434 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/internal/texture.py
--rw-r--r--   0 vguzov     (502) staff       (20)      395 2022-03-28 15:22:56.000000 blendify-1.2.1/blendify/internal/types.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/lights/
--rw-r--r--   0 vguzov     (502) staff       (20)      190 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/lights/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)     6083 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/lights/area.py
--rw-r--r--   0 vguzov     (502) staff       (20)     2112 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/lights/base.py
--rw-r--r--   0 vguzov     (502) staff       (20)    10174 2023-05-01 19:24:08.000000 blendify-1.2.1/blendify/lights/collection.py
--rw-r--r--   0 vguzov     (502) staff       (20)     5412 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/lights/common.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/materials/
--rw-r--r--   0 vguzov     (502) staff       (20)       63 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/materials/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)      665 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/materials/base.py
--rw-r--r--   0 vguzov     (502) staff       (20)     4853 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/materials/common.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/renderables/
--rw-r--r--   0 vguzov     (502) staff       (20)      249 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/renderables/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)     9851 2023-05-03 16:18:59.000000 blendify-1.2.1/blendify/renderables/base.py
--rw-r--r--   0 vguzov     (502) staff       (20)    14942 2023-05-03 15:27:36.000000 blendify-1.2.1/blendify/renderables/collection.py
--rw-r--r--   0 vguzov     (502) staff       (20)     5355 2023-05-03 18:18:39.000000 blendify-1.2.1/blendify/renderables/mesh.py
--rw-r--r--   0 vguzov     (502) staff       (20)    24366 2023-05-01 16:03:16.000000 blendify-1.2.1/blendify/renderables/pointcloud.py
--rw-r--r--   0 vguzov     (502) staff       (20)    14788 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/renderables/primitives.py
--rw-r--r--   0 vguzov     (502) staff       (20)    21860 2023-05-10 11:14:58.000000 blendify-1.2.1/blendify/scene.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify/utils/
--rw-r--r--   0 vguzov     (502) staff       (20)        0 2021-12-06 13:26:58.000000 blendify-1.2.1/blendify/utils/__init__.py
--rw-r--r--   0 vguzov     (502) staff       (20)     4899 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/utils/camera_trajectory.py
--rw-r--r--   0 vguzov     (502) staff       (20)      870 2022-03-31 07:59:42.000000 blendify-1.2.1/blendify/utils/image.py
--rw-r--r--   0 vguzov     (502) staff       (20)     4767 2023-04-24 17:47:43.000000 blendify-1.2.1/blendify/utils/pointcloud.py
--rw-r--r--   0 vguzov     (502) staff       (20)     1127 2023-04-24 18:05:40.000000 blendify-1.2.1/blendify/utils/shadow_catcher.py
--rw-r--r--   0 vguzov     (502) staff       (20)     2543 2023-04-24 18:05:40.000000 blendify-1.2.1/blendify/utils/smpl_wrapper.py
-drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/
--rw-r--r--   0 vguzov     (502) staff       (20)     5888 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/PKG-INFO
--rw-r--r--   0 vguzov     (502) staff       (20)     1200 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/SOURCES.txt
--rw-r--r--   0 vguzov     (502) staff       (20)        1 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/dependency_links.txt
--rw-r--r--   0 vguzov     (502) staff       (20)      273 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/requires.txt
--rw-r--r--   0 vguzov     (502) staff       (20)        9 2023-05-10 12:12:42.000000 blendify-1.2.1/blendify.egg-info/top_level.txt
--rw-r--r--   0 vguzov     (502) staff       (20)       38 2023-05-10 12:12:42.000000 blendify-1.2.1/setup.cfg
--rw-r--r--   0 vguzov     (502) staff       (20)     2214 2023-05-10 12:07:11.000000 blendify-1.2.1/setup.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/
+-rw-r--r--   0 vguzov     (502) staff       (20)     5888 2023-05-13 14:03:22.000000 blendify-1.2.2/PKG-INFO
+-rw-r--r--   0 vguzov     (502) staff       (20)     5528 2023-05-13 13:57:46.000000 blendify-1.2.2/README.md
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/
+-rw-r--r--   0 vguzov     (502) staff       (20)      302 2023-05-13 13:59:05.000000 blendify-1.2.2/blendify/__init__.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/cameras/
+-rw-r--r--   0 vguzov     (502) staff       (20)       58 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/cameras/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     3071 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/cameras/base.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     5470 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/cameras/common.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/colors/
+-rw-r--r--   0 vguzov     (502) staff       (20)      121 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/colors/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)      718 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/colors/base.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     2604 2023-05-03 18:18:43.000000 blendify-1.2.2/blendify/colors/common.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     3838 2023-04-24 18:05:40.000000 blendify-1.2.2/blendify/colors/texture.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/internal/
+-rw-r--r--   0 vguzov     (502) staff       (20)       32 2021-12-06 17:55:11.000000 blendify-1.2.2/blendify/internal/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     1886 2023-05-01 16:57:41.000000 blendify-1.2.2/blendify/internal/io.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     3925 2023-04-24 18:05:40.000000 blendify-1.2.2/blendify/internal/parser.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     3068 2023-05-01 15:22:56.000000 blendify-1.2.2/blendify/internal/positionable.py
+-rw-r--r--   0 vguzov     (502) staff       (20)      575 2022-03-31 07:59:42.000000 blendify-1.2.2/blendify/internal/singleton.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     2434 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/internal/texture.py
+-rw-r--r--   0 vguzov     (502) staff       (20)      395 2022-03-28 15:22:56.000000 blendify-1.2.2/blendify/internal/types.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/lights/
+-rw-r--r--   0 vguzov     (502) staff       (20)      190 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/lights/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     6083 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/lights/area.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     2112 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/lights/base.py
+-rw-r--r--   0 vguzov     (502) staff       (20)    10174 2023-05-01 19:24:08.000000 blendify-1.2.2/blendify/lights/collection.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     5412 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/lights/common.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/materials/
+-rw-r--r--   0 vguzov     (502) staff       (20)       87 2023-05-13 14:00:45.000000 blendify-1.2.2/blendify/materials/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)      665 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/materials/base.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     4938 2023-05-13 13:57:58.000000 blendify-1.2.2/blendify/materials/common.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/renderables/
+-rw-r--r--   0 vguzov     (502) staff       (20)      249 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/renderables/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     9851 2023-05-03 16:18:59.000000 blendify-1.2.2/blendify/renderables/base.py
+-rw-r--r--   0 vguzov     (502) staff       (20)    14942 2023-05-03 15:27:36.000000 blendify-1.2.2/blendify/renderables/collection.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     5355 2023-05-03 18:18:39.000000 blendify-1.2.2/blendify/renderables/mesh.py
+-rw-r--r--   0 vguzov     (502) staff       (20)    24366 2023-05-01 16:03:16.000000 blendify-1.2.2/blendify/renderables/pointcloud.py
+-rw-r--r--   0 vguzov     (502) staff       (20)    14788 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/renderables/primitives.py
+-rw-r--r--   0 vguzov     (502) staff       (20)    21860 2023-05-10 11:14:58.000000 blendify-1.2.2/blendify/scene.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify/utils/
+-rw-r--r--   0 vguzov     (502) staff       (20)        0 2021-12-06 13:26:58.000000 blendify-1.2.2/blendify/utils/__init__.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     4899 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/utils/camera_trajectory.py
+-rw-r--r--   0 vguzov     (502) staff       (20)      870 2022-03-31 07:59:42.000000 blendify-1.2.2/blendify/utils/image.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     4767 2023-04-24 17:47:43.000000 blendify-1.2.2/blendify/utils/pointcloud.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     1127 2023-04-24 18:05:40.000000 blendify-1.2.2/blendify/utils/shadow_catcher.py
+-rw-r--r--   0 vguzov     (502) staff       (20)     2543 2023-04-24 18:05:40.000000 blendify-1.2.2/blendify/utils/smpl_wrapper.py
+drwxr-xr-x   0 vguzov     (502) staff       (20)        0 2023-05-13 14:03:22.000000 blendify-1.2.2/blendify.egg-info/
+-rw-r--r--   0 vguzov     (502) staff       (20)     5888 2023-05-13 14:03:21.000000 blendify-1.2.2/blendify.egg-info/PKG-INFO
+-rw-r--r--   0 vguzov     (502) staff       (20)     1200 2023-05-13 14:03:21.000000 blendify-1.2.2/blendify.egg-info/SOURCES.txt
+-rw-r--r--   0 vguzov     (502) staff       (20)        1 2023-05-13 14:03:21.000000 blendify-1.2.2/blendify.egg-info/dependency_links.txt
+-rw-r--r--   0 vguzov     (502) staff       (20)      273 2023-05-13 14:03:21.000000 blendify-1.2.2/blendify.egg-info/requires.txt
+-rw-r--r--   0 vguzov     (502) staff       (20)        9 2023-05-13 14:03:21.000000 blendify-1.2.2/blendify.egg-info/top_level.txt
+-rw-r--r--   0 vguzov     (502) staff       (20)       38 2023-05-13 14:03:22.000000 blendify-1.2.2/setup.cfg
+-rw-r--r--   0 vguzov     (502) staff       (20)     2214 2023-05-13 13:58:44.000000 blendify-1.2.2/setup.py
```

### Comparing `blendify-1.2.1/PKG-INFO` & `blendify-1.2.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: blendify
-Version: 1.2.1
+Version: 1.2.2
 Summary: Python rendering framework for Blender
 Home-page: https://github.com/ptrvilya/blendify
 Author: Vladimir Guzov, Ilya Petrov
 Author-email: vguzov@mpi-inf.mpg.de, i.petrov@uni-tuebingen.de
 License: UNKNOWN
 Description: ![blendify Logo](https://github.com/ptrvilya/blendify/blob/main/.github/blendify_logo_light_bg.png?raw=true)
         
@@ -43,22 +43,22 @@
         [README](https://github.com/vchoutas/smplx#downloading-the-model).
         
         
         ## Quick Start
         ```python
         # Script to render cube
         from blendify import scene
-        from blendify.materials import PrinsipledBSDFMaterial
+        from blendify.materials import PrincipledBSDFMaterial
         from blendify.colors import UniformColors
         # Add light
         scene.lights.add_point(strength=1000, translation=(4, -2, 4))
         # Add camera
         scene.set_perspective_camera((512, 512), fov_x=0.7, quaternion=(0.82, 0.42, 0.18, 0.34), translation=(5, -5, 5))
         # Create material
-        material = PrinsipledBSDFMaterial()
+        material = PrincipledBSDFMaterial()
         # Create color
         color = UniformColors((0.0, 1.0, 0.0))
         # Add cube mesh
         scene.renderables.add_cube_mesh(1.0, material, color)
         # Render scene
         scene.render(filepath="cube.png")
         ```
```

### Comparing `blendify-1.2.1/README.md` & `blendify-1.2.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -3,26 +3,26 @@
 ![blendify Logo](.github/blendify_logo_light_bg.png)
 
 ## Introduction
 Blendify is a lightweight Python framework that provides a high-level API for creating and rendering scenes with Blender. Developed with a focus on 3D computer vision visualization, Blendify simplifies access to selected Blender functions and objects.
 
 Key features of Blendify:
 
-1. Simple interface: Blendify provides a user-friendly interface for performing common visualization tasks without having to dive into the complicated Blender API.
+1. **Simple interface:** Blendify provides a user-friendly interface for performing common visualization tasks without having to dive into the complicated Blender API.
 
-2. Easy integration: Blendify seamlessly integrates with development scripts, implementing
+2. **Easy integration:** Blendify seamlessly integrates with development scripts, implementing
 commonly used routines and functions:
     * native support of point clouds, meshes, and primitives;
     * support of per-vertex colors and textures;
     * advanced shadows with shadow catcher objects;
     * video rendering with smooth camera trajectories;
     * support for common camera models;
     * import and export of .blend files for deeper integration with Blender.
 
-3. Quick start: Blendify is easy to get started with and does not require a standalone Blender installation. All you need to do is run `pip install blendify`.
+3. **Quick start:** Blendify is easy to get started with and does not require a standalone Blender installation. All you need to do is run `pip install blendify`.
 
 
 ## Installation instructions
 ### Install from pip
 ```bash
 pip install blendify
 ```
@@ -37,22 +37,22 @@
 [README](https://github.com/vchoutas/smplx#downloading-the-model).
 
 
 ## Quick Start
 ```python
 # Script to render cube
 from blendify import scene
-from blendify.materials import PrinsipledBSDFMaterial
+from blendify.materials import PrincipledBSDFMaterial
 from blendify.colors import UniformColors
 # Add light
 scene.lights.add_point(strength=1000, translation=(4, -2, 4))
 # Add camera
 scene.set_perspective_camera((512, 512), fov_x=0.7, quaternion=(0.82, 0.42, 0.18, 0.34), translation=(5, -5, 5))
 # Create material
-material = PrinsipledBSDFMaterial()
+material = PrincipledBSDFMaterial()
 # Create color
 color = UniformColors((0.0, 1.0, 0.0))
 # Add cube mesh
 scene.renderables.add_cube_mesh(1.0, material, color)
 # Render scene
 scene.render(filepath="cube.png")
 ```
```

#### html2text {}

```diff
@@ -1,35 +1,35 @@
   ![blendify Logo](.github/blendify_logo_light_bg.png) ## Introduction Blendify
 is a lightweight Python framework that provides a high-level API for creating
 and rendering scenes with Blender. Developed with a focus on 3D computer vision
 visualization, Blendify simplifies access to selected Blender functions and
-objects. Key features of Blendify: 1. Simple interface: Blendify provides a
+objects. Key features of Blendify: 1. **Simple interface:** Blendify provides a
 user-friendly interface for performing common visualization tasks without
-having to dive into the complicated Blender API. 2. Easy integration: Blendify
-seamlessly integrates with development scripts, implementing commonly used
-routines and functions: * native support of point clouds, meshes, and
+having to dive into the complicated Blender API. 2. **Easy integration:**
+Blendify seamlessly integrates with development scripts, implementing commonly
+used routines and functions: * native support of point clouds, meshes, and
 primitives; * support of per-vertex colors and textures; * advanced shadows
 with shadow catcher objects; * video rendering with smooth camera trajectories;
 * support for common camera models; * import and export of .blend files for
-deeper integration with Blender. 3. Quick start: Blendify is easy to get
+deeper integration with Blender. 3. **Quick start:** Blendify is easy to get
 started with and does not require a standalone Blender installation. All you
 need to do is run `pip install blendify`. ## Installation instructions ###
 Install from pip ```bash pip install blendify ``` ### Optional requirements
 ```bash pip install blendify[utils / examples / docs / all] ``` Running
 examples 4 and 5 requires [PyTorch](https://pytorch.org/) with [PyTorch3D]
 (https://github.com/facebookresearch/pytorch3d/blob/main/INSTALL.md). Running
 example 5 requires SMPL model files, please refer to the installation
 instructions in [README](https://github.com/vchoutas/smplx#downloading-the-
 model). ## Quick Start ```python # Script to render cube from blendify import
-scene from blendify.materials import PrinsipledBSDFMaterial from
+scene from blendify.materials import PrincipledBSDFMaterial from
 blendify.colors import UniformColors # Add light scene.lights.add_point
 (strength=1000, translation=(4, -2, 4)) # Add camera
 scene.set_perspective_camera((512, 512), fov_x=0.7, quaternion=(0.82, 0.42,
 0.18, 0.34), translation=(5, -5, 5)) # Create material material =
-PrinsipledBSDFMaterial() # Create color color = UniformColors((0.0, 1.0, 0.0))
+PrincipledBSDFMaterial() # Create color color = UniformColors((0.0, 1.0, 0.0))
 # Add cube mesh scene.renderables.add_cube_mesh(1.0, material, color) # Render
 scene scene.render(filepath="cube.png") ``` ## Examples
                  Cornell_Box                      Color,_albedo_and_depth
     [.github/01_cornell_box.jpg]         [.github/02_color_albedo_depth.jpg]
             Mesh_with_texture                  Camera_colored_point_cloud
 [.github/03_mesh_with_texture.jpg] [.github/04_camera_colored_point_cloud.gif]
                SMPL_movement                           NURBS_trajectory
```

### Comparing `blendify-1.2.1/blendify/cameras/base.py` & `blendify-1.2.2/blendify/cameras/base.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/cameras/common.py` & `blendify-1.2.2/blendify/cameras/common.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/colors/base.py` & `blendify-1.2.2/blendify/colors/base.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/colors/common.py` & `blendify-1.2.2/blendify/colors/common.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/colors/texture.py` & `blendify-1.2.2/blendify/colors/texture.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/internal/io.py` & `blendify-1.2.2/blendify/internal/io.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/internal/parser.py` & `blendify-1.2.2/blendify/internal/parser.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/internal/positionable.py` & `blendify-1.2.2/blendify/internal/positionable.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/internal/singleton.py` & `blendify-1.2.2/blendify/internal/singleton.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/internal/texture.py` & `blendify-1.2.2/blendify/internal/texture.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/lights/area.py` & `blendify-1.2.2/blendify/lights/area.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/lights/base.py` & `blendify-1.2.2/blendify/lights/base.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/lights/collection.py` & `blendify-1.2.2/blendify/lights/collection.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/lights/common.py` & `blendify-1.2.2/blendify/lights/common.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/materials/base.py` & `blendify-1.2.2/blendify/materials/base.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/materials/common.py` & `blendify-1.2.2/blendify/materials/common.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Tuple
 
 import bpy
 
 from .base import Material, material_property
 
 
-class PrinsipledBSDFMaterial(Material):
-    """A class which manages the parameters of PrinsipledBSDF Blender material.
+class PrincipledBSDFMaterial(Material):
+    """A class which manages the parameters of PrincipledBSDF Blender material.
     Full docs: https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html
     """
 
     def __init__(
             self, metallic=0.0, specular=0.3, specular_tint=0.0, roughness=0.4, anisotropic=0.0,
             anisotropic_rotation=0.0,
             sheen=0.0, sheen_tint=0.5, clearcoat=0.0, clearcoat_roughness=0.0, ior=1.45, transmission=0.0,
@@ -54,14 +54,18 @@
         # Set material properties
         for property_name, blender_name in self._property2blender_mapping.items():
             self._bsdf_node.inputs[blender_name].default_value = self.__getattribute__("_" + property_name)
 
         return self._object_material, self._bsdf_node
 
 
+# Alias for backward compatibility
+PrinsipledBSDFMaterial = PrincipledBSDFMaterial
+
+
 class GlossyBSDFMaterial(Material):
     """A class which manages the parameters of GlossyBSDF Blender material.
     Full docs: https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/glossy.html
     """
 
     def __init__(self, roughness=0.4, distribution="GGX"):
         super().__init__()
```

### Comparing `blendify-1.2.1/blendify/renderables/base.py` & `blendify-1.2.2/blendify/renderables/base.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/renderables/collection.py` & `blendify-1.2.2/blendify/renderables/collection.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/renderables/mesh.py` & `blendify-1.2.2/blendify/renderables/mesh.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/renderables/pointcloud.py` & `blendify-1.2.2/blendify/renderables/pointcloud.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/renderables/primitives.py` & `blendify-1.2.2/blendify/renderables/primitives.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/scene.py` & `blendify-1.2.2/blendify/scene.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/utils/camera_trajectory.py` & `blendify-1.2.2/blendify/utils/camera_trajectory.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/utils/image.py` & `blendify-1.2.2/blendify/utils/image.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/utils/pointcloud.py` & `blendify-1.2.2/blendify/utils/pointcloud.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/utils/shadow_catcher.py` & `blendify-1.2.2/blendify/utils/shadow_catcher.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify/utils/smpl_wrapper.py` & `blendify-1.2.2/blendify/utils/smpl_wrapper.py`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/blendify.egg-info/PKG-INFO` & `blendify-1.2.2/blendify.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: blendify
-Version: 1.2.1
+Version: 1.2.2
 Summary: Python rendering framework for Blender
 Home-page: https://github.com/ptrvilya/blendify
 Author: Vladimir Guzov, Ilya Petrov
 Author-email: vguzov@mpi-inf.mpg.de, i.petrov@uni-tuebingen.de
 License: UNKNOWN
 Description: ![blendify Logo](https://github.com/ptrvilya/blendify/blob/main/.github/blendify_logo_light_bg.png?raw=true)
         
@@ -43,22 +43,22 @@
         [README](https://github.com/vchoutas/smplx#downloading-the-model).
         
         
         ## Quick Start
         ```python
         # Script to render cube
         from blendify import scene
-        from blendify.materials import PrinsipledBSDFMaterial
+        from blendify.materials import PrincipledBSDFMaterial
         from blendify.colors import UniformColors
         # Add light
         scene.lights.add_point(strength=1000, translation=(4, -2, 4))
         # Add camera
         scene.set_perspective_camera((512, 512), fov_x=0.7, quaternion=(0.82, 0.42, 0.18, 0.34), translation=(5, -5, 5))
         # Create material
-        material = PrinsipledBSDFMaterial()
+        material = PrincipledBSDFMaterial()
         # Create color
         color = UniformColors((0.0, 1.0, 0.0))
         # Add cube mesh
         scene.renderables.add_cube_mesh(1.0, material, color)
         # Render scene
         scene.render(filepath="cube.png")
         ```
```

### Comparing `blendify-1.2.1/blendify.egg-info/SOURCES.txt` & `blendify-1.2.2/blendify.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `blendify-1.2.1/setup.py` & `blendify-1.2.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from pkg_resources import DistributionNotFound, get_distribution
 from setuptools import setup, find_packages
-version = '1.2.1'
+version = '1.2.2'
 
 with open("docs/pip_readme.md", "r") as fi:
     long_description = fi.read()
 
 keywords = ["rendering", "pointcloud", "blender", "mesh"]
 
 classifiers = [
```

