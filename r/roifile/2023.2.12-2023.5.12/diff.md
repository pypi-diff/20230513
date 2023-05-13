# Comparing `tmp/roifile-2023.2.12.tar.gz` & `tmp/roifile-2023.5.12.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "roifile-2023.2.12.tar", last modified: Sun Feb 12 22:21:53 2023, max compression
+gzip compressed data, was "roifile-2023.5.12.tar", last modified: Sat May 13 05:51:34 2023, max compression
```

## Comparing `roifile-2023.2.12.tar` & `roifile-2023.5.12.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-02-12 22:21:53.937326 roifile-2023.2.12/
--rw-rw-rw-   0        0        0     1559 2023-02-12 22:21:51.000000 roifile-2023.2.12/LICENSE
--rw-rw-rw-   0        0        0      276 2022-12-09 00:08:23.000000 roifile-2023.2.12/MANIFEST.in
--rw-rw-rw-   0        0        0     4800 2023-02-12 22:21:53.937326 roifile-2023.2.12/PKG-INFO
--rw-rw-rw-   0        0        0     3869 2023-02-12 22:21:51.000000 roifile-2023.2.12/README.rst
-drwxrwxrwx   0        0        0        0 2023-02-12 22:21:53.927141 roifile-2023.2.12/roifile/
--rw-rw-rw-   0        0        0      101 2020-02-14 04:28:42.000000 roifile-2023.2.12/roifile/__init__.py
--rw-rw-rw-   0        0        0      132 2020-02-14 04:32:59.000000 roifile-2023.2.12/roifile/__main__.py
--rw-rw-rw-   0        0        0    42633 2023-02-12 22:07:53.000000 roifile-2023.2.12/roifile/roifile.py
-drwxrwxrwx   0        0        0        0 2023-02-12 22:21:53.932191 roifile-2023.2.12/roifile.egg-info/
--rw-rw-rw-   0        0        0     4800 2023-02-12 22:21:52.000000 roifile-2023.2.12/roifile.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      302 2023-02-12 22:21:53.000000 roifile-2023.2.12/roifile.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-12 22:21:52.000000 roifile-2023.2.12/roifile.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       49 2023-02-12 22:21:52.000000 roifile-2023.2.12/roifile.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       57 2023-02-12 22:21:52.000000 roifile-2023.2.12/roifile.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-02-12 22:21:52.000000 roifile-2023.2.12/roifile.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1777 2023-02-12 21:52:27.000000 roifile-2023.2.12/roifile_demo.py
--rw-rw-rw-   0        0        0       42 2023-02-12 22:21:53.937326 roifile-2023.2.12/setup.cfg
--rw-rw-rw-   0        0        0     2381 2022-10-03 18:24:00.000000 roifile-2023.2.12/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:34.089789 roifile-2023.5.12/
+-rw-rw-rw-   0        0        0     1559 2023-05-13 05:51:28.000000 roifile-2023.5.12/LICENSE
+-rw-rw-rw-   0        0        0      276 2022-12-09 00:08:23.000000 roifile-2023.5.12/MANIFEST.in
+-rw-rw-rw-   0        0        0     4851 2023-05-13 05:51:34.089789 roifile-2023.5.12/PKG-INFO
+-rw-rw-rw-   0        0        0     3971 2023-05-13 05:51:28.000000 roifile-2023.5.12/README.rst
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:34.084665 roifile-2023.5.12/roifile/
+-rw-rw-rw-   0        0        0      101 2020-02-14 04:28:42.000000 roifile-2023.5.12/roifile/__init__.py
+-rw-rw-rw-   0        0        0      132 2020-02-14 04:32:59.000000 roifile-2023.5.12/roifile/__main__.py
+-rw-rw-rw-   0        0        0    44333 2023-05-13 05:47:12.000000 roifile-2023.5.12/roifile/roifile.py
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:34.089789 roifile-2023.5.12/roifile.egg-info/
+-rw-rw-rw-   0        0        0     4851 2023-05-13 05:51:32.000000 roifile-2023.5.12/roifile.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      302 2023-05-13 05:51:33.000000 roifile-2023.5.12/roifile.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 05:51:32.000000 roifile-2023.5.12/roifile.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       49 2023-05-13 05:51:32.000000 roifile-2023.5.12/roifile.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       33 2023-05-13 05:51:32.000000 roifile-2023.5.12/roifile.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 05:51:32.000000 roifile-2023.5.12/roifile.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1775 2023-05-13 05:48:29.000000 roifile-2023.5.12/roifile_demo.py
+-rw-rw-rw-   0        0        0       42 2023-05-13 05:51:34.089789 roifile-2023.5.12/setup.cfg
+-rw-rw-rw-   0        0        0     2307 2023-05-01 15:10:59.000000 roifile-2023.5.12/setup.py
```

### Comparing `roifile-2023.2.12/LICENSE` & `roifile-2023.5.12/LICENSE`

 * *Files identical despite different names*

### Comparing `roifile-2023.2.12/PKG-INFO` & `roifile-2023.5.12/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,25 +1,24 @@
 Metadata-Version: 2.1
 Name: roifile
-Version: 2023.2.12
+Version: 2023.5.12
 Summary: Read and write ImageJ ROI format
 Home-page: https://www.cgohlke.com
 Author: Christoph Gohlke
 Author-email: cgohlke@cgohlke.com
 License: BSD
 Project-URL: Bug Tracker, https://github.com/cgohlke/roifile/issues
 Project-URL: Source Code, https://github.com/cgohlke/roifile
 Platform: any
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Science/Research
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.8
 Provides-Extra: all
 License-File: LICENSE
 
@@ -30,15 +29,15 @@
 an undocumented and ImageJ application specific format to store regions of
 interest, geometric shapes, paths, text, and whatnot for image overlays.
 
 .. _ImageJ: https://imagej.net
 
 :Author: `Christoph Gohlke <https://www.cgohlke.com>`_
 :License: BSD 3-Clause
-:Version: 2023.2.12
+:Version: 2023.5.12
 :DOI: `10.5281/zenodo.6941603 <https://doi.org/10.5281/zenodo.6941603>`_
 
 Quickstart
 ----------
 
 Install the roifile package and all dependencies from the
 `Python Package Index <https://pypi.org/project/roifile/>`_::
@@ -56,22 +55,27 @@
 
 Requirements
 ------------
 
 This revision was tested with the following requirements and dependencies
 (other versions may work):
 
-- `CPython 3.8.10, 3.9.13, 3.10.10, 3.11.2 <https://www.python.org>`_
-- `Numpy 1.23.5 <https://pypi.org/project/numpy/>`_
-- `Tifffile 2023.2.3 <https://pypi.org/project/tifffile/>`_  (optional)
-- `Matplotlib 3.6.3 <https://pypi.org/project/matplotlib/>`_  (optional)
+- `CPython <https://www.python.org>`_ 3.9.13, 3.10.11, 3.11.3
+- `Numpy <https://pypi.org/project/numpy/>`_ 1.23.5
+- `Tifffile <https://pypi.org/project/tifffile/>`_ 2023.4.12 (optional)
+- `Matplotlib <https://pypi.org/project/matplotlib/>`_ 3.7.1 (optional)
 
 Revisions
 ---------
 
+2023.5.12
+
+- Improve object repr and type hints.
+- Drop support for Python 3.8 and numpy < 1.21 (NEP29).
+
 2023.2.12
 
 - Delay import of zipfile.
 - Verify shape of coordinates on write.
 
 2022.9.19
```

### Comparing `roifile-2023.2.12/README.rst` & `roifile-2023.5.12/README.rst`

 * *Files 4% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 an undocumented and ImageJ application specific format to store regions of
 interest, geometric shapes, paths, text, and whatnot for image overlays.
 
 .. _ImageJ: https://imagej.net
 
 :Author: `Christoph Gohlke <https://www.cgohlke.com>`_
 :License: BSD 3-Clause
-:Version: 2023.2.12
+:Version: 2023.5.12
 :DOI: `10.5281/zenodo.6941603 <https://doi.org/10.5281/zenodo.6941603>`_
 
 Quickstart
 ----------
 
 Install the roifile package and all dependencies from the
 `Python Package Index <https://pypi.org/project/roifile/>`_::
@@ -31,22 +31,27 @@
 
 Requirements
 ------------
 
 This revision was tested with the following requirements and dependencies
 (other versions may work):
 
-- `CPython 3.8.10, 3.9.13, 3.10.10, 3.11.2 <https://www.python.org>`_
-- `Numpy 1.23.5 <https://pypi.org/project/numpy/>`_
-- `Tifffile 2023.2.3 <https://pypi.org/project/tifffile/>`_  (optional)
-- `Matplotlib 3.6.3 <https://pypi.org/project/matplotlib/>`_  (optional)
+- `CPython <https://www.python.org>`_ 3.9.13, 3.10.11, 3.11.3
+- `Numpy <https://pypi.org/project/numpy/>`_ 1.23.5
+- `Tifffile <https://pypi.org/project/tifffile/>`_ 2023.4.12 (optional)
+- `Matplotlib <https://pypi.org/project/matplotlib/>`_ 3.7.1 (optional)
 
 Revisions
 ---------
 
+2023.5.12
+
+- Improve object repr and type hints.
+- Drop support for Python 3.8 and numpy < 1.21 (NEP29).
+
 2023.2.12
 
 - Delay import of zipfile.
 - Verify shape of coordinates on write.
 
 2022.9.19
```

### Comparing `roifile-2023.2.12/roifile/roifile.py` & `roifile-2023.5.12/roifile/roifile.py`

 * *Files 5% similar despite different names*

```diff
@@ -35,15 +35,15 @@
 an undocumented and ImageJ application specific format to store regions of
 interest, geometric shapes, paths, text, and whatnot for image overlays.
 
 .. _ImageJ: https://imagej.net
 
 :Author: `Christoph Gohlke <https://www.cgohlke.com>`_
 :License: BSD 3-Clause
-:Version: 2023.2.12
+:Version: 2023.5.12
 :DOI: `10.5281/zenodo.6941603 <https://doi.org/10.5281/zenodo.6941603>`_
 
 Quickstart
 ----------
 
 Install the roifile package and all dependencies from the
 `Python Package Index <https://pypi.org/project/roifile/>`_::
@@ -61,22 +61,27 @@
 
 Requirements
 ------------
 
 This revision was tested with the following requirements and dependencies
 (other versions may work):
 
-- `CPython 3.8.10, 3.9.13, 3.10.10, 3.11.2 <https://www.python.org>`_
-- `Numpy 1.23.5 <https://pypi.org/project/numpy/>`_
-- `Tifffile 2023.2.3 <https://pypi.org/project/tifffile/>`_  (optional)
-- `Matplotlib 3.6.3 <https://pypi.org/project/matplotlib/>`_  (optional)
+- `CPython <https://www.python.org>`_ 3.9.13, 3.10.11, 3.11.3
+- `Numpy <https://pypi.org/project/numpy/>`_ 1.23.5
+- `Tifffile <https://pypi.org/project/tifffile/>`_ 2023.4.12 (optional)
+- `Matplotlib <https://pypi.org/project/matplotlib/>`_ 3.7.1 (optional)
 
 Revisions
 ---------
 
+2023.5.12
+
+- Improve object repr and type hints.
+- Drop support for Python 3.8 and numpy < 1.21 (NEP29).
+
 2023.2.12
 
 - Delay import of zipfile.
 - Verify shape of coordinates on write.
 
 2022.9.19
 
@@ -183,58 +188,59 @@
 
     python -m roifile _test.roi
 
 """
 
 from __future__ import annotations
 
-__version__ = '2023.2.12'
+__version__ = '2023.5.12'
 
 __all__ = [
     'roiread',
     'roiwrite',
     'ImagejRoi',
     'ROI_TYPE',
     'ROI_SUBTYPE',
     'ROI_OPTIONS',
     'ROI_POINT_TYPE',
     'ROI_POINT_SIZE',
+    'ROI_COLOR_NONE',
 ]
 
 import enum
 import os
 import struct
 import sys
 import dataclasses
 
-from typing import Any, Iterable, Literal, Union
 import numpy
 
-try:
-    from numpy.typing import ArrayLike
-except ImportError:
-    # numpy < 1.20
-    from numpy import ndarray as ArrayLike
+from typing import TYPE_CHECKING
+
+if TYPE_CHECKING:
+    from typing import Any, Literal, Union
+    from collections.abc import Iterable
+    from numpy.typing import ArrayLike, NDArray
 
-ZipFileMode = Union[Literal['r'], Literal['w'], Literal['x'], Literal['a']]
+    ZipFileMode = Union[Literal['r'], Literal['w'], Literal['x'], Literal['a']]
 
 
 def roiread(
-    filename: os.PathLike | str, /, *, min_int_coord: int | None = None
+    filename: os.PathLike[Any] | str, /, *, min_int_coord: int | None = None
 ) -> ImagejRoi | list[ImagejRoi]:
     """Return ImagejRoi instance(s) from ROI, ZIP, or TIFF file.
 
     For ZIP or TIFF files, return a list of ImagejRoi.
 
     """
     return ImagejRoi.fromfile(filename, min_int_coord=min_int_coord)
 
 
 def roiwrite(
-    filename: os.PathLike | str,
+    filename: os.PathLike[Any] | str,
     roi: ImagejRoi | Iterable[ImagejRoi],
     /,
     *,
     name: str | Iterable[str] | None = None,
     mode: ZipFileMode | None = None,
 ) -> None:
     """Write ImagejRoi instance(s) to ROI or ZIP file.
@@ -261,37 +267,43 @@
     with zipfile.ZipFile(filename, mode) as zf:
         for n, r in zip(name, roi):
             with zf.open(n, 'w') as fh:
                 fh.write(r.tobytes())
 
 
 class ROI_TYPE(enum.IntEnum):
+    """ImageJ ROI types."""
+
     POLYGON = 0
     RECT = 1
     OVAL = 2
     LINE = 3
     FREELINE = 4
     POLYLINE = 5
     NOROI = 6
     FREEHAND = 7
     TRACED = 8
     ANGLE = 9
     POINT = 10
 
 
 class ROI_SUBTYPE(enum.IntEnum):
+    """ImageJ ROI subtypes."""
+
     UNDEFINED = 0
     TEXT = 1
     ARROW = 2
     ELLIPSE = 3
     IMAGE = 4
     ROTATED_RECT = 5
 
 
 class ROI_OPTIONS(enum.IntFlag):
+    """ImageJ ROI options."""
+
     SPLINE_FIT = 1
     DOUBLE_HEADED = 2
     OUTLINE = 4
     OVERLAY_LABELS = 8
     OVERLAY_NAMES = 16
     OVERLAY_BACKGROUNDS = 32
     OVERLAY_BOLD = 64
@@ -300,32 +312,37 @@
     ZERO_TRANSPARENT = 512
     SHOW_LABELS = 1024
     SCALE_LABELS = 2048
     PROMPT_BEFORE_DELETING = 4096
 
 
 class ROI_POINT_TYPE(enum.IntEnum):
+    """ImageJ ROI point types."""
+
     HYBRID = 0
     CROSS = 1
     # CROSSHAIR = 1
     DOT = 2
     CIRCLE = 3
 
 
 class ROI_POINT_SIZE(enum.IntEnum):
+    """ImageJ ROI point sizes."""
+
     TINY = 1
     SMALL = 3
     MEDIUM = 5
     LARGE = 7
     EXTRA_LARGE = 11
     XXL = 17
     XXXL = 25
 
 
 ROI_COLOR_NONE = b'\x00\x00\x00\x00'
+"""No color or Black."""
 
 
 @dataclasses.dataclass
 class ImagejRoi:
     """Read and write ImageJ ROI format."""
 
     byteorder: Literal['>'] | Literal['<'] = '>'
@@ -361,24 +378,24 @@
     heightd: float = 0.0
     overlay_label_color: bytes = ROI_COLOR_NONE
     overlay_font_size: int = 0
     group: int = 0
     image_opacity: int = 0
     image_size: int = 0
     float_stroke_width: float = 0.0
-    integer_coordinates: numpy.ndarray | None = None
-    subpixel_coordinates: numpy.ndarray | None = None
-    multi_coordinates: numpy.ndarray | None = None
-    counters: numpy.ndarray | None = None
-    counter_positions: numpy.ndarray | None = None  # flat indices to TZC array
     text_size: int = 0
     text_style: int = 0
     text_justification: int = 0
     text_name: str = ''
     text: str = ''
+    counters: NDArray[numpy.uint8] | None = None
+    counter_positions: NDArray[numpy.uint32] | None = None
+    integer_coordinates: NDArray[numpy.int32] | None = None
+    subpixel_coordinates: NDArray[numpy.float32] | None = None
+    multi_coordinates: NDArray[numpy.float32] | None = None
 
     @classmethod
     def frompoints(
         cls,
         points: ArrayLike | None = None,
         /,
         *,
@@ -448,15 +465,15 @@
         self.bottom = int(right_bottom[1])
 
         return self
 
     @classmethod
     def fromfile(
         cls,
-        filename: os.PathLike | str,
+        filename: os.PathLike[Any] | str,
         /,
         *,
         min_int_coord: int | None = None,
     ) -> ImagejRoi | list[ImagejRoi]:
         """Return ImagejRoi instance from ROI, ZIP, or TIFF file.
 
         For ZIP or TIFF files, return a list of ImagejRoi.
@@ -608,22 +625,22 @@
             if roi_props_offset > 0 and roi_props_length > 0:
                 props = data[
                     roi_props_offset : name_offset + roi_props_length * 2
                 ]
                 self.props = props.decode(self.utf16)
 
             if counters_offset > 0:
-                counters: numpy.ndarray = numpy.ndarray(
+                counters: NDArray[numpy.uint32] = numpy.ndarray(
                     shape=self.n_coordinates,
                     dtype=self.byteorder + 'u4',
                     buffer=data,
                     offset=counters_offset,
                 )
                 self.counters = (counters & 0xFF).astype('u1')
-                self.counter_positions = counters >> 8
+                self.counter_positions = (counters >> 8).astype('u4')
 
         if self.version >= 218 and self.subtype == ROI_SUBTYPE.TEXT:
             (
                 self.text_size,
                 style_and_justification,
                 name_length,
                 text_length,
@@ -677,15 +694,15 @@
         elif self.roitype not in (ROI_TYPE.RECT, ROI_TYPE.LINE, ROI_TYPE.OVAL):
             log_warning(f'cannot handle ImagejRoi type {self.roitype!r}')
 
         return self
 
     def tofile(
         self,
-        filename: os.PathLike | str,
+        filename: os.PathLike[Any] | str,
         name: str | None = None,
         mode: ZipFileMode | None = None,
     ) -> None:
         """Write ImagejRoi to ROI or ZIP file.
 
         Existing ZIP files are opened for append.
 
@@ -866,15 +883,15 @@
                 )
                 counters = counters & 0xFF | indices << 8
                 counters = counters.astype(self.byteorder + 'u4')
             result.append(counters.tobytes())
 
         return b''.join(result)
 
-    def plot(
+    def plot(  # type: ignore
         self,
         ax: Any | None = None,
         *,
         rois: Iterable[ImagejRoi] | None = None,
         title: str | None = None,
         bounds: bool = False,
         invert_yaxis: bool | None = None,
@@ -978,16 +995,17 @@
             ax.invert_yaxis()
 
         if fig is not None:
             pyplot.show()
 
     def coordinates(
         self, multi: bool = False
-    ) -> numpy.ndarray | list[numpy.ndarray]:
+    ) -> NDArray[Any] | list[NDArray[Any]]:
         """Return x, y coordinates as numpy array for display."""
+        coords: Any
         if self.subpixel_coordinates is not None:
             coords = self.subpixel_coordinates.copy()
         elif self.integer_coordinates is not None:
             coords = self.integer_coordinates + [self.left, self.top]
         elif self.multi_coordinates is not None:
             coordslist = self.path2coords(self.multi_coordinates)
             if not multi:
@@ -1019,26 +1037,29 @@
         if b == ROI_COLOR_NONE:
             return default
         if self.byteorder == '>':
             return f'#{b[1]:02x}{b[2]:02x}{b[3]:02x}'
         return f'#{b[3]:02x}{b[2]:02x}{b[1]:02x}'
 
     @staticmethod
-    def path2coords(path: numpy.ndarray, /) -> list[numpy.ndarray]:
+    def path2coords(
+        multi_coordinates: NDArray[numpy.float32], /
+    ) -> list[NDArray[numpy.float32]]:
         """Return list of coordinate arrays from 2D geometric path."""
         coordinates = []
-        points: list[list[int | float]] = []
+        points: list[list[float]] = []
+        path: list[float] = multi_coordinates.tolist()
         n = 0
         m = 0
         while n < len(path):
             op = int(path[n])
             if op == 0:
                 # MOVETO
                 if n > 0:
-                    coordinates.append(numpy.array(points))
+                    coordinates.append(numpy.array(points, dtype='f4'))
                     points = []
                 points.append([path[n + 1], path[n + 2]])
                 m = len(points) - 1
                 n += 3
             elif op == 1:
                 # LINETO
                 points.append([path[n + 1], path[n + 2]])
@@ -1051,15 +1072,15 @@
                 # QUADTO or CUBICTO
                 raise NotImplementedError(
                     f'PathIterator command {op!r} not supported'
                 )
             else:
                 raise RuntimeError(f'invalid PathIterator command {op!r}')
 
-        coordinates.append(numpy.array(points))
+        coordinates.append(numpy.array(points, dtype='f4'))
         return coordinates
 
     @staticmethod
     def min_int_coord(value: int | None = None) -> int:
         """Return minimum integer coordinate value.
 
         The default, -5000, is used by ImageJ.
@@ -1123,44 +1144,75 @@
             and self.left == other.left
             and self.top == other.top
             and self.right == other.right
             and self.bottom == other.bottom
         )
 
     def __repr__(self) -> str:
-        return f'<{self.__class__.__name__} {self.name!r}>'
-
-    def __str__(self) -> str:
-        return indent(
-            repr(self),
-            *(f'{name} = {value!r}' for name, value in self.__dict__.items()),
-        )
+        info = [f'{self.__class__.__name__}(']
+        for name, value in self.__dict__.items():
+            if isinstance(value, numpy.ndarray):
+                value = repr(value).replace('    ', ' ')
+                value = value.replace('([[', '([\n    [')
+                info.append(f'{name}=numpy.{value},')
+            elif value == getattr(ImagejRoi, name):
+                pass
+            elif isinstance(value, enum.Enum):
+                info.append(f'{name}={enumstr(value)},')
+            else:
+                info.append(f'{name}={value!r},')
+        return indent(*info, end='\n)')
 
 
-def oval(rect: ArrayLike, /, points: int = 33) -> numpy.ndarray:
+def oval(rect: ArrayLike, /, points: int = 33) -> NDArray[numpy.float32]:
     """Return coordinates of oval from rectangle corners."""
     arr = numpy.array(rect, dtype=numpy.float32)
     c = numpy.linspace(0.0, 2.0 * numpy.pi, num=points, dtype=numpy.float32)
     c = numpy.array([numpy.cos(c), numpy.sin(c)]).T
     r = arr[1] - arr[0]
     r /= 2.0
     c *= r
     c += arr[0] + r
     return c
 
 
-def indent(*args) -> str:
-    """Return joined string representations of objects with lines indented."""
-    text = '\n'.join(str(arg) for arg in args)
-    return '\n'.join(
-        ('  ' + line if line else line) for line in text.splitlines() if line
-    )[2:]
+def indent(*args: Any, sep='', end='') -> str:
+    """Return joined string representations of objects with indented lines."""
+    text = (sep + '\n').join(
+        arg if isinstance(arg, str) else repr(arg) for arg in args
+    )
+    return (
+        '\n'.join(
+            ('    ' + line if line else line)
+            for line in text.splitlines()
+            if line
+        )[4:]
+        + end
+    )
+
+
+def enumstr(v: enum.Enum | None, /) -> str:
+    """Return IntEnum or IntFlag as str."""
+    # repr() and str() of enums are type, value, and version dependent
+    if v is None:
+        return 'None'
+    # return f'{v.__class__.__name__}({v.value})'
+    s = repr(v)
+    s = s[1:].split(':', 1)[0]
+    if 'UNKNOWN' in s:
+        s = f'{v.__class__.__name__}({v.value})'
+    elif '|' in s:
+        # IntFlag combination
+        s = s.replace('|', ' | ' + v.__class__.__name__ + '.')
+    elif not hasattr(v, 'name') or v.name is None:
+        s = f'{v.__class__.__name__}({v.value})'
+    return s
 
 
-def log_warning(msg: object, *args: object, **kwargs) -> None:
+def log_warning(msg: object, *args: object, **kwargs: Any) -> None:
     """Log message with level WARNING."""
     import logging
 
     logging.getLogger(__name__).warning(msg, *args, **kwargs)
 
 
 def test(verbose: bool = False) -> None:
```

### Comparing `roifile-2023.2.12/roifile.egg-info/PKG-INFO` & `roifile-2023.5.12/roifile.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,25 +1,24 @@
 Metadata-Version: 2.1
 Name: roifile
-Version: 2023.2.12
+Version: 2023.5.12
 Summary: Read and write ImageJ ROI format
 Home-page: https://www.cgohlke.com
 Author: Christoph Gohlke
 Author-email: cgohlke@cgohlke.com
 License: BSD
 Project-URL: Bug Tracker, https://github.com/cgohlke/roifile/issues
 Project-URL: Source Code, https://github.com/cgohlke/roifile
 Platform: any
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Science/Research
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.8
 Provides-Extra: all
 License-File: LICENSE
 
@@ -30,15 +29,15 @@
 an undocumented and ImageJ application specific format to store regions of
 interest, geometric shapes, paths, text, and whatnot for image overlays.
 
 .. _ImageJ: https://imagej.net
 
 :Author: `Christoph Gohlke <https://www.cgohlke.com>`_
 :License: BSD 3-Clause
-:Version: 2023.2.12
+:Version: 2023.5.12
 :DOI: `10.5281/zenodo.6941603 <https://doi.org/10.5281/zenodo.6941603>`_
 
 Quickstart
 ----------
 
 Install the roifile package and all dependencies from the
 `Python Package Index <https://pypi.org/project/roifile/>`_::
@@ -56,22 +55,27 @@
 
 Requirements
 ------------
 
 This revision was tested with the following requirements and dependencies
 (other versions may work):
 
-- `CPython 3.8.10, 3.9.13, 3.10.10, 3.11.2 <https://www.python.org>`_
-- `Numpy 1.23.5 <https://pypi.org/project/numpy/>`_
-- `Tifffile 2023.2.3 <https://pypi.org/project/tifffile/>`_  (optional)
-- `Matplotlib 3.6.3 <https://pypi.org/project/matplotlib/>`_  (optional)
+- `CPython <https://www.python.org>`_ 3.9.13, 3.10.11, 3.11.3
+- `Numpy <https://pypi.org/project/numpy/>`_ 1.23.5
+- `Tifffile <https://pypi.org/project/tifffile/>`_ 2023.4.12 (optional)
+- `Matplotlib <https://pypi.org/project/matplotlib/>`_ 3.7.1 (optional)
 
 Revisions
 ---------
 
+2023.5.12
+
+- Improve object repr and type hints.
+- Drop support for Python 3.8 and numpy < 1.21 (NEP29).
+
 2023.2.12
 
 - Delay import of zipfile.
 - Verify shape of coordinates on write.
 
 2022.9.19
```

### Comparing `roifile-2023.2.12/roifile_demo.py` & `roifile-2023.5.12/roifile_demo.py`

 * *Files 8% similar despite different names*

```diff
@@ -7,15 +7,14 @@
 
 """
 
 import numpy
 from matplotlib import pyplot
 from skimage.measure import find_contours, label, regionprops
 from tifffile import TiffFile, imwrite
-
 from roifile import ImagejRoi
 
 
 def plot_image_overlays(image, overlays, **kwargs):
     """Plot image and overlays (bytes) using matplotlib."""
     fig, ax = pyplot.subplots()
     ax.imshow(image, cmap='gray')
```

### Comparing `roifile-2023.2.12/setup.py` & `roifile-2023.5.12/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -61,23 +61,22 @@
         'Bug Tracker': 'https://github.com/cgohlke/roifile/issues',
         'Source Code': 'https://github.com/cgohlke/roifile',
         # 'Documentation': 'https://',
     },
     packages=['roifile'],
     entry_points={'console_scripts': ['roifile = roifile.roifile:main']},
     python_requires='>=3.8',
-    install_requires=['numpy>=1.19.2'],
-    extras_require={'all': ['matplotlib>=3.3', 'tifffile>=2021.11.2']},
+    install_requires=['numpy'],
+    extras_require={'all': ['matplotlib', 'tifffile']},
     platforms=['any'],
     classifiers=[
         'Development Status :: 4 - Beta',
         'License :: OSI Approved :: BSD License',
         'Intended Audience :: Science/Research',
         'Intended Audience :: Developers',
         'Operating System :: OS Independent',
         'Programming Language :: Python :: 3 :: Only',
-        'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
         'Programming Language :: Python :: 3.11',
     ],
 )
```

