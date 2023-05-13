# Comparing `tmp/netext-0.1.0.tar.gz` & `tmp/netext-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "netext-0.1.0.tar", max compression
+gzip compressed data, was "netext-0.1.1.tar", max compression
```

## Comparing `netext-0.1.0.tar` & `netext-0.1.1.tar`

### file list

```diff
@@ -1,33 +1,34 @@
--rw-r--r--   0        0        0     1068 2022-07-21 11:10:54.728351 netext-0.1.0/LICENSE
--rw-r--r--   0        0        0      121 2022-07-28 09:14:58.912740 netext-0.1.0/netext/__init__.py
--rw-r--r--   0        0        0     6931 2023-04-14 17:49:22.938221 netext-0.1.0/netext/buffer_renderer.py
--rw-r--r--   0        0        0     5408 2023-04-27 19:31:08.534822 netext-0.1.0/netext/edge_rasterizer.py
--rw-r--r--   0        0        0        0 2023-04-14 17:49:22.938888 netext-0.1.0/netext/edge_rendering/__init__.py
--rw-r--r--   0        0        0     3633 2023-04-27 19:13:41.537169 netext-0.1.0/netext/edge_rendering/arrow_tips.py
--rw-r--r--   0        0        0     5541 2023-04-27 18:56:44.440021 netext-0.1.0/netext/edge_rendering/bitmap.py
--rw-r--r--   0        0        0     6395 2023-04-28 17:44:32.792145 netext-0.1.0/netext/edge_rendering/box.py
--rw-r--r--   0        0        0     3029 2023-04-14 17:49:22.940244 netext-0.1.0/netext/edge_rendering/bresenham.py
--rw-r--r--   0        0        0      799 2023-04-14 17:49:22.940513 netext-0.1.0/netext/edge_rendering/buffer.py
--rw-r--r--   0        0        0      270 2023-04-28 17:44:32.792632 netext-0.1.0/netext/edge_rendering/modes.py
--rw-r--r--   0        0        0        0 2023-01-19 19:24:14.666622 netext-0.1.0/netext/edge_routing/__init__.py
--rw-r--r--   0        0        0     6961 2023-04-27 18:56:44.441702 netext-0.1.0/netext/edge_routing/edge.py
--rw-r--r--   0        0        0      109 2023-04-27 18:56:44.442196 netext-0.1.0/netext/edge_routing/modes.py
--rw-r--r--   0        0        0     3179 2023-04-21 18:09:16.081957 netext-0.1.0/netext/edge_routing/orthogonal.py
--rw-r--r--   0        0        0     1445 2023-04-27 18:56:44.442779 netext-0.1.0/netext/edge_routing/route.py
--rw-r--r--   0        0        0      113 2023-04-14 17:49:22.942247 netext-0.1.0/netext/geometry/__init__.py
--rw-r--r--   0        0        0     2658 2023-04-15 11:55:40.807331 netext-0.1.0/netext/geometry/line_segment.py
--rw-r--r--   0        0        0      129 2023-04-14 17:49:22.943043 netext-0.1.0/netext/geometry/magnet.py
--rw-r--r--   0        0        0     1720 2023-04-15 11:55:34.747534 netext-0.1.0/netext/geometry/point.py
--rw-r--r--   0        0        0        0 2022-07-28 09:14:58.912939 netext-0.1.0/netext/layout_engines/__init__.py
--rw-r--r--   0        0        0      301 2023-02-19 13:46:26.585243 netext-0.1.0/netext/layout_engines/engine.py
--rw-r--r--   0        0        0     1922 2023-04-28 19:06:54.382788 netext-0.1.0/netext/layout_engines/grandalf.py
--rw-r--r--   0        0        0      394 2023-04-28 19:06:54.367866 netext-0.1.0/netext/layout_engines/static.py
--rw-r--r--   0        0        0     6863 2023-04-23 18:19:19.715474 netext-0.1.0/netext/node_rasterizer.py
--rw-r--r--   0        0        0        0 2023-04-14 17:49:22.945675 netext-0.1.0/netext/rendering/__init__.py
--rw-r--r--   0        0        0      580 2023-04-14 17:49:22.945860 netext-0.1.0/netext/rendering/bitmap_buffer.py
--rw-r--r--   0        0        0     1369 2023-04-15 06:27:35.991709 netext-0.1.0/netext/rendering/segment_buffer.py
--rw-r--r--   0        0        0        0 2023-04-14 17:49:22.946251 netext-0.1.0/netext/shapes/__init__.py
--rw-r--r--   0        0        0     9540 2023-04-28 18:14:56.042355 netext-0.1.0/netext/terminal_graph.py
--rw-r--r--   0        0        0     1175 2023-05-05 18:25:00.328706 netext-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1001 1970-01-01 00:00:00.000000 netext-0.1.0/setup.py
--rw-r--r--   0        0        0      785 1970-01-01 00:00:00.000000 netext-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1068 2022-07-21 11:10:54.728351 netext-0.1.1/LICENSE
+-rw-r--r--   0        0        0     1323 2023-05-05 18:46:20.213875 netext-0.1.1/README.md
+-rw-r--r--   0        0        0      121 2022-07-28 09:14:58.912740 netext-0.1.1/netext/__init__.py
+-rw-r--r--   0        0        0     6931 2023-04-14 17:49:22.938221 netext-0.1.1/netext/buffer_renderer.py
+-rw-r--r--   0        0        0     5537 2023-05-07 18:41:05.976385 netext-0.1.1/netext/edge_rasterizer.py
+-rw-r--r--   0        0        0        0 2023-04-14 17:49:22.938888 netext-0.1.1/netext/edge_rendering/__init__.py
+-rw-r--r--   0        0        0     4290 2023-05-07 18:42:19.410412 netext-0.1.1/netext/edge_rendering/arrow_tips.py
+-rw-r--r--   0        0        0     5541 2023-04-27 18:56:44.440021 netext-0.1.1/netext/edge_rendering/bitmap.py
+-rw-r--r--   0        0        0     6723 2023-05-07 18:41:52.158005 netext-0.1.1/netext/edge_rendering/box.py
+-rw-r--r--   0        0        0     3029 2023-04-14 17:49:22.940244 netext-0.1.1/netext/edge_rendering/bresenham.py
+-rw-r--r--   0        0        0      799 2023-04-14 17:49:22.940513 netext-0.1.1/netext/edge_rendering/buffer.py
+-rw-r--r--   0        0        0      270 2023-04-28 17:44:32.792632 netext-0.1.1/netext/edge_rendering/modes.py
+-rw-r--r--   0        0        0        0 2023-01-19 19:24:14.666622 netext-0.1.1/netext/edge_routing/__init__.py
+-rw-r--r--   0        0        0     6961 2023-04-27 18:56:44.441702 netext-0.1.1/netext/edge_routing/edge.py
+-rw-r--r--   0        0        0      109 2023-04-27 18:56:44.442196 netext-0.1.1/netext/edge_routing/modes.py
+-rw-r--r--   0        0        0     3179 2023-04-21 18:09:16.081957 netext-0.1.1/netext/edge_routing/orthogonal.py
+-rw-r--r--   0        0        0     1445 2023-04-27 18:56:44.442779 netext-0.1.1/netext/edge_routing/route.py
+-rw-r--r--   0        0        0      113 2023-04-14 17:49:22.942247 netext-0.1.1/netext/geometry/__init__.py
+-rw-r--r--   0        0        0     2658 2023-04-15 11:55:40.807331 netext-0.1.1/netext/geometry/line_segment.py
+-rw-r--r--   0        0        0      129 2023-04-14 17:49:22.943043 netext-0.1.1/netext/geometry/magnet.py
+-rw-r--r--   0        0        0     1720 2023-04-15 11:55:34.747534 netext-0.1.1/netext/geometry/point.py
+-rw-r--r--   0        0        0        0 2022-07-28 09:14:58.912939 netext-0.1.1/netext/layout_engines/__init__.py
+-rw-r--r--   0        0        0      301 2023-02-19 13:46:26.585243 netext-0.1.1/netext/layout_engines/engine.py
+-rw-r--r--   0        0        0     1922 2023-04-28 19:06:54.382788 netext-0.1.1/netext/layout_engines/grandalf.py
+-rw-r--r--   0        0        0      394 2023-04-28 19:06:54.367866 netext-0.1.1/netext/layout_engines/static.py
+-rw-r--r--   0        0        0     6863 2023-04-23 18:19:19.715474 netext-0.1.1/netext/node_rasterizer.py
+-rw-r--r--   0        0        0        0 2023-04-14 17:49:22.945675 netext-0.1.1/netext/rendering/__init__.py
+-rw-r--r--   0        0        0      580 2023-04-14 17:49:22.945860 netext-0.1.1/netext/rendering/bitmap_buffer.py
+-rw-r--r--   0        0        0     1369 2023-04-15 06:27:35.991709 netext-0.1.1/netext/rendering/segment_buffer.py
+-rw-r--r--   0        0        0        0 2023-04-14 17:49:22.946251 netext-0.1.1/netext/shapes/__init__.py
+-rw-r--r--   0        0        0     9540 2023-04-28 18:14:56.042355 netext-0.1.1/netext/terminal_graph.py
+-rw-r--r--   0        0        0     1297 2023-05-13 12:13:18.387643 netext-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     2363 1970-01-01 00:00:00.000000 netext-0.1.1/setup.py
+-rw-r--r--   0        0        0     2292 1970-01-01 00:00:00.000000 netext-0.1.1/PKG-INFO
```

### Comparing `netext-0.1.0/LICENSE` & `netext-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/buffer_renderer.py` & `netext-0.1.1/netext/buffer_renderer.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_rasterizer.py` & `netext-0.1.1/netext/edge_rasterizer.py`

 * *Files 3% similar despite different names*

```diff
@@ -97,14 +97,17 @@
     edge_segments = edge_segments.cut_with_nodes([u_buffer, v_buffer])
 
     if not edge_segments.segments:
         return None
 
     if edge_segment_drawing_mode in [
         EdgeSegmentDrawingMode.BOX,
+        EdgeSegmentDrawingMode.BOX_ROUNDED,
+        EdgeSegmentDrawingMode.BOX_HEAVY,
+        EdgeSegmentDrawingMode.BOX_DOUBLE,
         EdgeSegmentDrawingMode.ASCII,
     ]:
         assert (
             routing_mode == EdgeRoutingMode.ORTHOGONAL
         ), "Box characters are only supported on orthogonal lines"
         strips = orthogonal_segments_to_strips_with_box_characters(
             edge_segments.segments, edge_segment_drawing_mode, style=style
```

### Comparing `netext-0.1.0/netext/edge_rendering/arrow_tips.py` & `netext-0.1.1/netext/edge_rendering/arrow_tips.py`

 * *Files 13% similar despite different names*

```diff
@@ -23,14 +23,32 @@
     ArrowTip.ARROW: {
         EdgeSegmentDrawingMode.BOX: {
             ArrowDirections.LEFT: "◀",
             ArrowDirections.RIGHT: "▶",
             ArrowDirections.UP: "▲",
             ArrowDirections.DOWN: "▼",
         },
+        EdgeSegmentDrawingMode.BOX_ROUNDED: {
+            ArrowDirections.LEFT: "◀",
+            ArrowDirections.RIGHT: "▶",
+            ArrowDirections.UP: "▲",
+            ArrowDirections.DOWN: "▼",
+        },
+        EdgeSegmentDrawingMode.BOX_HEAVY: {
+            ArrowDirections.LEFT: "◀",
+            ArrowDirections.RIGHT: "▶",
+            ArrowDirections.UP: "▲",
+            ArrowDirections.DOWN: "▼",
+        },
+        EdgeSegmentDrawingMode.BOX_DOUBLE: {
+            ArrowDirections.LEFT: "◀",
+            ArrowDirections.RIGHT: "▶",
+            ArrowDirections.UP: "▲",
+            ArrowDirections.DOWN: "▼",
+        },
         EdgeSegmentDrawingMode.SINGLE_CHARACTER: {
             ArrowDirections.LEFT: "<",
             ArrowDirections.RIGHT: ">",
             ArrowDirections.UP: "^",
             ArrowDirections.DOWN: "v",
         },
         EdgeSegmentDrawingMode.ASCII: {
```

### Comparing `netext-0.1.0/netext/edge_rendering/bitmap.py` & `netext-0.1.1/netext/edge_rendering/bitmap.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_rendering/box.py` & `netext-0.1.1/netext/edge_rendering/box.py`

 * *Files 8% similar despite different names*

```diff
@@ -39,14 +39,22 @@
         EdgeCharacters.HORIZONTAL: "━",
         EdgeCharacters.VERTICAL: "┃",
         EdgeCharacters.CORNER_UPPER_LEFT: "┏",
         EdgeCharacters.CORNER_UPPER_RIGHT: "┓",
         EdgeCharacters.CORNER_LOWER_LEFT: "┗",
         EdgeCharacters.CORNER_LOWER_RIGHT: "┛",
     },
+    EdgeSegmentDrawingMode.BOX_DOUBLE: {
+        EdgeCharacters.HORIZONTAL: "═",
+        EdgeCharacters.VERTICAL: "║",
+        EdgeCharacters.CORNER_UPPER_LEFT: "╔",
+        EdgeCharacters.CORNER_UPPER_RIGHT: "╗",
+        EdgeCharacters.CORNER_LOWER_LEFT: "╚",
+        EdgeCharacters.CORNER_LOWER_RIGHT: "╝",
+    },
     EdgeSegmentDrawingMode.ASCII: {
         EdgeCharacters.HORIZONTAL: "-",
         EdgeCharacters.VERTICAL: "|",
         EdgeCharacters.CORNER_LOWER_LEFT: "+",
         EdgeCharacters.CORNER_LOWER_RIGHT: "+",
         EdgeCharacters.CORNER_UPPER_LEFT: "+",
         EdgeCharacters.CORNER_UPPER_RIGHT: "+",
```

### Comparing `netext-0.1.0/netext/edge_rendering/bresenham.py` & `netext-0.1.1/netext/edge_rendering/bresenham.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_rendering/buffer.py` & `netext-0.1.1/netext/edge_rendering/buffer.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_routing/edge.py` & `netext-0.1.1/netext/edge_routing/edge.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_routing/orthogonal.py` & `netext-0.1.1/netext/edge_routing/orthogonal.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/edge_routing/route.py` & `netext-0.1.1/netext/edge_routing/route.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/geometry/line_segment.py` & `netext-0.1.1/netext/geometry/line_segment.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/geometry/point.py` & `netext-0.1.1/netext/geometry/point.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/layout_engines/grandalf.py` & `netext-0.1.1/netext/layout_engines/grandalf.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/node_rasterizer.py` & `netext-0.1.1/netext/node_rasterizer.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/rendering/bitmap_buffer.py` & `netext-0.1.1/netext/rendering/bitmap_buffer.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/rendering/segment_buffer.py` & `netext-0.1.1/netext/rendering/segment_buffer.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/netext/terminal_graph.py` & `netext-0.1.1/netext/terminal_graph.py`

 * *Files identical despite different names*

### Comparing `netext-0.1.0/pyproject.toml` & `netext-0.1.1/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,13 +1,16 @@
 [tool.poetry]
 name = "netext"
-version = "0.1.0"
+version = "0.1.1"
 description = "A graph (network) rendering library for the terminal."
 authors = ["Malte Klemm <me@malteklemm.de>"]
 license = "MIT"
+repository = 'https://github.com/mahrz24/netext'
+readme = 'README.md'
+keywords = ['network', 'graph', 'terminal', 'rich']
 
 [tool.poetry.dependencies]
 python = "^3.10"
 rich = "^13"
 networkx = {extras = ["default"], version="^3.0"}
 grandalf = "^0.7"
 bitarray = "^2.6.2"
```

