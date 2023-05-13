# Comparing `tmp/rubik-cube-0.0.1.tar.gz` & `tmp/rubik-cube-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/rubik-cube-0.0.1.tar", last modified: Sat Jan  4 07:53:11 2020, max compression
+gzip compressed data, was "rubik-cube-0.0.2.tar", last modified: Sat May 13 20:22:13 2023, max compression
```

## Comparing `rubik-cube-0.0.1.tar` & `rubik-cube-0.0.2.tar`

### file list

```diff
@@ -1,16 +1,19 @@
-drwxr-xr-x   0 pglass     (501) staff       (20)        0 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/
--rw-r--r--   0 pglass     (501) staff       (20)     6232 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/PKG-INFO
-drwxr-xr-x   0 pglass     (501) staff       (20)        0 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik_cube.egg-info/
--rw-r--r--   0 pglass     (501) staff       (20)     6232 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik_cube.egg-info/PKG-INFO
--rw-r--r--   0 pglass     (501) staff       (20)      234 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik_cube.egg-info/SOURCES.txt
--rw-r--r--   0 pglass     (501) staff       (20)        6 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik_cube.egg-info/top_level.txt
--rw-r--r--   0 pglass     (501) staff       (20)        1 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik_cube.egg-info/dependency_links.txt
--rw-r--r--   0 pglass     (501) staff       (20)     4576 2020-01-04 07:51:53.000000 rubik-cube-0.0.1/README.md
--rw-r--r--   0 pglass     (501) staff       (20)     1043 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/setup.py
-drwxr-xr-x   0 pglass     (501) staff       (20)        0 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/rubik/
--rw-r--r--   0 pglass     (501) staff       (20)     4081 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/rubik/optimize.py
--rw-r--r--   0 pglass     (501) staff       (20)        0 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/rubik/__init__.py
--rw-r--r--   0 pglass     (501) staff       (20)    13756 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/rubik/cube.py
--rw-r--r--   0 pglass     (501) staff       (20)    21650 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/rubik/solve.py
--rw-r--r--   0 pglass     (501) staff       (20)     4374 2020-01-04 07:51:43.000000 rubik-cube-0.0.1/rubik/maths.py
--rw-r--r--   0 pglass     (501) staff       (20)       38 2020-01-04 07:53:11.000000 rubik-cube-0.0.1/setup.cfg
+drwxr-xr-x   0 pglass     (501) staff       (20)        0 2023-05-13 20:22:13.456637 rubik-cube-0.0.2/
+-rw-r--r--   0 pglass     (501) staff       (20)     1056 2020-01-04 07:51:43.000000 rubik-cube-0.0.2/LICENSE
+-rw-r--r--   0 pglass     (501) staff       (20)     5407 2023-05-13 20:22:13.456285 rubik-cube-0.0.2/PKG-INFO
+-rw-r--r--   0 pglass     (501) staff       (20)     4634 2023-05-12 04:56:00.000000 rubik-cube-0.0.2/README.md
+drwxr-xr-x   0 pglass     (501) staff       (20)        0 2023-05-13 20:22:13.453918 rubik-cube-0.0.2/rubik/
+-rw-r--r--   0 pglass     (501) staff       (20)        0 2020-01-04 07:51:43.000000 rubik-cube-0.0.2/rubik/__init__.py
+-rw-r--r--   0 pglass     (501) staff       (20)    13740 2023-05-13 20:05:14.000000 rubik-cube-0.0.2/rubik/cube.py
+-rw-r--r--   0 pglass     (501) staff       (20)     4384 2023-05-13 20:05:14.000000 rubik-cube-0.0.2/rubik/maths.py
+-rw-r--r--   0 pglass     (501) staff       (20)     4081 2020-01-04 07:51:43.000000 rubik-cube-0.0.2/rubik/optimize.py
+-rw-r--r--   0 pglass     (501) staff       (20)    21993 2023-05-13 20:05:14.000000 rubik-cube-0.0.2/rubik/solve.py
+drwxr-xr-x   0 pglass     (501) staff       (20)        0 2023-05-13 20:22:13.455493 rubik-cube-0.0.2/rubik_cube.egg-info/
+-rw-r--r--   0 pglass     (501) staff       (20)     5407 2023-05-13 20:22:13.000000 rubik-cube-0.0.2/rubik_cube.egg-info/PKG-INFO
+-rw-r--r--   0 pglass     (501) staff       (20)      256 2023-05-13 20:22:13.000000 rubik-cube-0.0.2/rubik_cube.egg-info/SOURCES.txt
+-rw-r--r--   0 pglass     (501) staff       (20)        1 2023-05-13 20:22:13.000000 rubik-cube-0.0.2/rubik_cube.egg-info/dependency_links.txt
+-rw-r--r--   0 pglass     (501) staff       (20)        6 2023-05-13 20:22:13.000000 rubik-cube-0.0.2/rubik_cube.egg-info/top_level.txt
+-rw-r--r--   0 pglass     (501) staff       (20)       38 2023-05-13 20:22:13.456718 rubik-cube-0.0.2/setup.cfg
+-rw-r--r--   0 pglass     (501) staff       (20)     1143 2023-05-13 20:05:22.000000 rubik-cube-0.0.2/setup.py
+drwxr-xr-x   0 pglass     (501) staff       (20)        0 2023-05-13 20:22:13.455828 rubik-cube-0.0.2/tests/
+-rw-r--r--   0 pglass     (501) staff       (20)    26120 2023-05-13 20:05:14.000000 rubik-cube-0.0.2/tests/test.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `rubik-cube-0.0.1/PKG-INFO` & `rubik-cube-0.0.2/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,142 +1,146 @@
 Metadata-Version: 2.1
 Name: rubik-cube
-Version: 0.0.1
+Version: 0.0.2
 Summary: A basic, pure-Python Rubik's cube solver
 Home-page: https://github.com/pglass/cube
 Author: Paul Glass
 Author-email: pnglass@gmail.com
 License: MIT
-Description: # Overview
-        
-        This is a Python 3 implementation of a (3x3) Rubik's Cube solver.
-        
-        It contains:
-        
-        - A simple implementation of the cube
-        - A solver that follows a fixed algorithm
-        - An unintelligent solution sequence optimizer
-        - A decent set of test cases
-        
-        ## Installation
-        
-        The package is hosted on PyPI.
-        
-        ```
-        pip install rubik-cube
-        ```
-        
-        Import from the `rubik` package,
-        
-        ```python
-        >>> from rubik.cube import Cube
-        >>> c = Cube("OOOOOOOOOYYYWWWGGGBBBYYYWWWGGGBBBYYYWWWGGGBBBRRRRRRRRR")
-        >>> print(c)
-            OOO
-            OOO
-            OOO
-        YYY WWW GGG BBB
-        YYY WWW GGG BBB
-        YYY WWW GGG BBB
-            RRR
-            RRR
-            RRR
-        ```
-        
-        ## Implementation
-        
-        ### Piece
-        
-        The cornerstone of this implementation is the Piece class. A Piece stores two
-        pieces of information:
-        
-        1. An integer `position` vector `(x, y, z)` where each component is in {-1, 0,
-        1}:
-            - `(0, 0, 0)` is the center of the cube
-            - the positive x-axis points to the right face
-            - the positive y-axis points to the up face
-            - the positive z-axis points to the front face
-        
-        2. A `colors` vector `(cx, cy, cz)`, giving the color of the sticker along each
-        axis. Null values are place whenever that Piece has less than three sides. For
-        example, a Piece with `colors=('Orange', None, 'Red')` is an edge piece with an
-        `'Orange'` sticker facing the x-direction and a `'Red'` sticker facing the
-        z-direction. The Piece doesn't know or care which direction along the x-axis
-        the `'Orange'` sticker is facing, just that it is facing in the x-direction and
-        not the y- or z- directions.
-        
-        Using the combination of `position` and `color` vectors makes it easy to
-        identify any Piece by its absolute position or by its unique combination of
-        colors.
-        
-        A Piece provides a method `Piece.rotate(matrix)`, which accepts a (90 degree)
-        rotation matrix. A matrix-vector multiplication is done to update the Piece's
-        `position` vector. Then we update the `colors` vector, by swapping exactly two
-        entries in the `colors` vector:
-        
-        - For example, a corner Piece has three stickers of different colors. After a
-          90 degree rotation of the Piece, one sticker remains facing down the same
-          axis, while the other two stickers swap axes. This corresponds to swapping the
-          positions of two entries in the Piece’s `colors` vector.
-        - For an edge or face piece, the argument is the same as above, although we may
-          swap around one or more null entries.
-        
-        ### Cube
-        
-        The Cube class is built on top of the Piece class. The Cube stores a list of
-        Pieces and provides nice methods for flipping slices of the cube, as well as
-        methods for querying the current state. (I followed standard [Rubik's Cube
-        notation](http://ruwix.com/the-rubiks-cube/notation/))
-        
-        Because the Piece class encapsulates all of the rotation logic, implementing
-        rotations in the Cube class is dead simple - just apply the appropriate
-        rotation matrix to all Pieces involved in the rotation. An example: To
-        implement `Cube.L()` - a clockwise rotation of the left face - do the
-        following:
-        
-        1. Construct the appropriate [rotation matrix](
-        http://en.wikipedia.org/wiki/Rotation_matrix) for a 90 degree rotation in the
-        `x = -1` plane.
-        2. Select all Pieces satisfying `position.x == -1`.
-        3. Apply the rotation matrix to each of these Pieces.
-        
-        To implement `Cube.X()` - a clockwise rotation of the entire cube around the
-        positive x-axis - just apply a rotation matrix to all Pieces stored in the
-        Cube.
-        
-        ### Solver
-        
-        The solver implements the algorithm described
-        [here](http://peter.stillhq.com/jasmine/rubikscubesolution.html) and
-        [here](http://www.chessandpoker.com/rubiks-cube-solution.html). It is a
-        layer-by-layer solution. First the front-face (the `z = 1` plane) is solved,
-        then the middle layer (`z = 0`), and finally the back layer (`z = -1`). When
-        the solver is done, `Solver.moves` is a list representing the solution
-        sequence.
-        
-        My first correct-looking implementation of the solver average 252.5 moves per
-        solution sequence on 135000 randomly-generated cubes (with no failures).
-        Implementing a dumb optimizer reduced the average number of moves to 192.7 on
-        67000 randomly-generated cubes. The optimizer does the following:
-        
-        1. Eliminate full-cube rotations by "unrotating" the moves (Z U L D Zi becomes
-        L D R)
-        2. Eliminate moves followed by their inverse (R R Ri Ri is gone)
-        3. Replace moves repeated three times with a single turn in the opposite
-        direction (R R R becomes Ri)
-        
-        The solver is not particularly fast. On my machine (a 4.0 Ghz i7), it takes
-        about 0.06 seconds per solve on CPython, which is roughly 16.7 solves/second.
-        On PyPy, this is reduced to about 0.013 seconds per solve, or about 76
-        solves/second.
-        
 Keywords: rubik cube solver
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+![PyPI](https://img.shields.io/pypi/v/rubik-cube)
+![PyPI - Python Version](https://img.shields.io/pypi/pyversions/rubik-cube)
+
+# Overview
+
+This is a Python 3 implementation of a (3x3) Rubik's Cube solver.
+
+It contains:
+
+- A simple implementation of the cube
+- A solver that follows a fixed algorithm
+- An unintelligent solution sequence optimizer
+- A decent set of test cases
+
+## Installation
+
+The package is hosted on PyPI.
+
+```
+pip install rubik-cube
+```
+
+Import from the `rubik` package,
+
+```python
+>>> from rubik.cube import Cube
+>>> c = Cube("OOOOOOOOOYYYWWWGGGBBBYYYWWWGGGBBBYYYWWWGGGBBBRRRRRRRRR")
+>>> print(c)
+    OOO
+    OOO
+    OOO
+YYY WWW GGG BBB
+YYY WWW GGG BBB
+YYY WWW GGG BBB
+    RRR
+    RRR
+    RRR
+```
+
+## Implementation
+
+### Piece
+
+The cornerstone of this implementation is the Piece class. A Piece stores two
+pieces of information:
+
+1. An integer `position` vector `(x, y, z)` where each component is in {-1, 0,
+1}:
+    - `(0, 0, 0)` is the center of the cube
+    - the positive x-axis points to the right face
+    - the positive y-axis points to the up face
+    - the positive z-axis points to the front face
+
+2. A `colors` vector `(cx, cy, cz)`, giving the color of the sticker along each
+axis. Null values are place whenever that Piece has less than three sides. For
+example, a Piece with `colors=('Orange', None, 'Red')` is an edge piece with an
+`'Orange'` sticker facing the x-direction and a `'Red'` sticker facing the
+z-direction. The Piece doesn't know or care which direction along the x-axis
+the `'Orange'` sticker is facing, just that it is facing in the x-direction and
+not the y- or z- directions.
+
+Using the combination of `position` and `color` vectors makes it easy to
+identify any Piece by its absolute position or by its unique combination of
+colors.
+
+A Piece provides a method `Piece.rotate(matrix)`, which accepts a (90 degree)
+rotation matrix. A matrix-vector multiplication is done to update the Piece's
+`position` vector. Then we update the `colors` vector, by swapping exactly two
+entries in the `colors` vector:
+
+- For example, a corner Piece has three stickers of different colors. After a
+  90 degree rotation of the Piece, one sticker remains facing down the same
+  axis, while the other two stickers swap axes. This corresponds to swapping the
+  positions of two entries in the Piece’s `colors` vector.
+- For an edge or face piece, the argument is the same as above, although we may
+  swap around one or more null entries.
+
+### Cube
+
+The Cube class is built on top of the Piece class. The Cube stores a list of
+Pieces and provides nice methods for flipping slices of the cube, as well as
+methods for querying the current state. (I followed standard [Rubik's Cube
+notation](http://ruwix.com/the-rubiks-cube/notation/))
+
+Because the Piece class encapsulates all of the rotation logic, implementing
+rotations in the Cube class is dead simple - just apply the appropriate
+rotation matrix to all Pieces involved in the rotation. An example: To
+implement `Cube.L()` - a clockwise rotation of the left face - do the
+following:
+
+1. Construct the appropriate [rotation matrix](
+http://en.wikipedia.org/wiki/Rotation_matrix) for a 90 degree rotation in the
+`x = -1` plane.
+2. Select all Pieces satisfying `position.x == -1`.
+3. Apply the rotation matrix to each of these Pieces.
+
+To implement `Cube.X()` - a clockwise rotation of the entire cube around the
+positive x-axis - just apply a rotation matrix to all Pieces stored in the
+Cube.
+
+### Solver
+
+The solver implements the algorithm described
+[here](http://www.chessandpoker.com/rubiks-cube-solution.html). It is a
+layer-by-layer solution. First the front-face (the `z = 1` plane) is solved,
+then the middle layer (`z = 0`), and finally the back layer (`z = -1`). When
+the solver is done, `Solver.moves` is a list representing the solution
+sequence.
+
+My first correct-looking implementation of the solver average 252.5 moves per
+solution sequence on 135000 randomly-generated cubes (with no failures).
+Implementing a dumb optimizer reduced the average number of moves to 192.7 on
+67000 randomly-generated cubes. The optimizer does the following:
+
+1. Eliminate full-cube rotations by "unrotating" the moves (Z U L D Zi becomes
+L D R)
+2. Eliminate moves followed by their inverse (R R Ri Ri is gone)
+3. Replace moves repeated three times with a single turn in the opposite
+direction (R R R becomes Ri)
+
+The solver is not particularly fast. On my machine (a 4.0 Ghz i7), it takes
+about 0.06 seconds per solve on CPython, which is roughly 16.7 solves/second.
+On PyPy, this is reduced to about 0.013 seconds per solve, or about 76
+solves/second.
```

### Comparing `rubik-cube-0.0.1/rubik_cube.egg-info/PKG-INFO` & `rubik-cube-0.0.2/rubik_cube.egg-info/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,142 +1,146 @@
 Metadata-Version: 2.1
 Name: rubik-cube
-Version: 0.0.1
+Version: 0.0.2
 Summary: A basic, pure-Python Rubik's cube solver
 Home-page: https://github.com/pglass/cube
 Author: Paul Glass
 Author-email: pnglass@gmail.com
 License: MIT
-Description: # Overview
-        
-        This is a Python 3 implementation of a (3x3) Rubik's Cube solver.
-        
-        It contains:
-        
-        - A simple implementation of the cube
-        - A solver that follows a fixed algorithm
-        - An unintelligent solution sequence optimizer
-        - A decent set of test cases
-        
-        ## Installation
-        
-        The package is hosted on PyPI.
-        
-        ```
-        pip install rubik-cube
-        ```
-        
-        Import from the `rubik` package,
-        
-        ```python
-        >>> from rubik.cube import Cube
-        >>> c = Cube("OOOOOOOOOYYYWWWGGGBBBYYYWWWGGGBBBYYYWWWGGGBBBRRRRRRRRR")
-        >>> print(c)
-            OOO
-            OOO
-            OOO
-        YYY WWW GGG BBB
-        YYY WWW GGG BBB
-        YYY WWW GGG BBB
-            RRR
-            RRR
-            RRR
-        ```
-        
-        ## Implementation
-        
-        ### Piece
-        
-        The cornerstone of this implementation is the Piece class. A Piece stores two
-        pieces of information:
-        
-        1. An integer `position` vector `(x, y, z)` where each component is in {-1, 0,
-        1}:
-            - `(0, 0, 0)` is the center of the cube
-            - the positive x-axis points to the right face
-            - the positive y-axis points to the up face
-            - the positive z-axis points to the front face
-        
-        2. A `colors` vector `(cx, cy, cz)`, giving the color of the sticker along each
-        axis. Null values are place whenever that Piece has less than three sides. For
-        example, a Piece with `colors=('Orange', None, 'Red')` is an edge piece with an
-        `'Orange'` sticker facing the x-direction and a `'Red'` sticker facing the
-        z-direction. The Piece doesn't know or care which direction along the x-axis
-        the `'Orange'` sticker is facing, just that it is facing in the x-direction and
-        not the y- or z- directions.
-        
-        Using the combination of `position` and `color` vectors makes it easy to
-        identify any Piece by its absolute position or by its unique combination of
-        colors.
-        
-        A Piece provides a method `Piece.rotate(matrix)`, which accepts a (90 degree)
-        rotation matrix. A matrix-vector multiplication is done to update the Piece's
-        `position` vector. Then we update the `colors` vector, by swapping exactly two
-        entries in the `colors` vector:
-        
-        - For example, a corner Piece has three stickers of different colors. After a
-          90 degree rotation of the Piece, one sticker remains facing down the same
-          axis, while the other two stickers swap axes. This corresponds to swapping the
-          positions of two entries in the Piece’s `colors` vector.
-        - For an edge or face piece, the argument is the same as above, although we may
-          swap around one or more null entries.
-        
-        ### Cube
-        
-        The Cube class is built on top of the Piece class. The Cube stores a list of
-        Pieces and provides nice methods for flipping slices of the cube, as well as
-        methods for querying the current state. (I followed standard [Rubik's Cube
-        notation](http://ruwix.com/the-rubiks-cube/notation/))
-        
-        Because the Piece class encapsulates all of the rotation logic, implementing
-        rotations in the Cube class is dead simple - just apply the appropriate
-        rotation matrix to all Pieces involved in the rotation. An example: To
-        implement `Cube.L()` - a clockwise rotation of the left face - do the
-        following:
-        
-        1. Construct the appropriate [rotation matrix](
-        http://en.wikipedia.org/wiki/Rotation_matrix) for a 90 degree rotation in the
-        `x = -1` plane.
-        2. Select all Pieces satisfying `position.x == -1`.
-        3. Apply the rotation matrix to each of these Pieces.
-        
-        To implement `Cube.X()` - a clockwise rotation of the entire cube around the
-        positive x-axis - just apply a rotation matrix to all Pieces stored in the
-        Cube.
-        
-        ### Solver
-        
-        The solver implements the algorithm described
-        [here](http://peter.stillhq.com/jasmine/rubikscubesolution.html) and
-        [here](http://www.chessandpoker.com/rubiks-cube-solution.html). It is a
-        layer-by-layer solution. First the front-face (the `z = 1` plane) is solved,
-        then the middle layer (`z = 0`), and finally the back layer (`z = -1`). When
-        the solver is done, `Solver.moves` is a list representing the solution
-        sequence.
-        
-        My first correct-looking implementation of the solver average 252.5 moves per
-        solution sequence on 135000 randomly-generated cubes (with no failures).
-        Implementing a dumb optimizer reduced the average number of moves to 192.7 on
-        67000 randomly-generated cubes. The optimizer does the following:
-        
-        1. Eliminate full-cube rotations by "unrotating" the moves (Z U L D Zi becomes
-        L D R)
-        2. Eliminate moves followed by their inverse (R R Ri Ri is gone)
-        3. Replace moves repeated three times with a single turn in the opposite
-        direction (R R R becomes Ri)
-        
-        The solver is not particularly fast. On my machine (a 4.0 Ghz i7), it takes
-        about 0.06 seconds per solve on CPython, which is roughly 16.7 solves/second.
-        On PyPy, this is reduced to about 0.013 seconds per solve, or about 76
-        solves/second.
-        
 Keywords: rubik cube solver
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+![PyPI](https://img.shields.io/pypi/v/rubik-cube)
+![PyPI - Python Version](https://img.shields.io/pypi/pyversions/rubik-cube)
+
+# Overview
+
+This is a Python 3 implementation of a (3x3) Rubik's Cube solver.
+
+It contains:
+
+- A simple implementation of the cube
+- A solver that follows a fixed algorithm
+- An unintelligent solution sequence optimizer
+- A decent set of test cases
+
+## Installation
+
+The package is hosted on PyPI.
+
+```
+pip install rubik-cube
+```
+
+Import from the `rubik` package,
+
+```python
+>>> from rubik.cube import Cube
+>>> c = Cube("OOOOOOOOOYYYWWWGGGBBBYYYWWWGGGBBBYYYWWWGGGBBBRRRRRRRRR")
+>>> print(c)
+    OOO
+    OOO
+    OOO
+YYY WWW GGG BBB
+YYY WWW GGG BBB
+YYY WWW GGG BBB
+    RRR
+    RRR
+    RRR
+```
+
+## Implementation
+
+### Piece
+
+The cornerstone of this implementation is the Piece class. A Piece stores two
+pieces of information:
+
+1. An integer `position` vector `(x, y, z)` where each component is in {-1, 0,
+1}:
+    - `(0, 0, 0)` is the center of the cube
+    - the positive x-axis points to the right face
+    - the positive y-axis points to the up face
+    - the positive z-axis points to the front face
+
+2. A `colors` vector `(cx, cy, cz)`, giving the color of the sticker along each
+axis. Null values are place whenever that Piece has less than three sides. For
+example, a Piece with `colors=('Orange', None, 'Red')` is an edge piece with an
+`'Orange'` sticker facing the x-direction and a `'Red'` sticker facing the
+z-direction. The Piece doesn't know or care which direction along the x-axis
+the `'Orange'` sticker is facing, just that it is facing in the x-direction and
+not the y- or z- directions.
+
+Using the combination of `position` and `color` vectors makes it easy to
+identify any Piece by its absolute position or by its unique combination of
+colors.
+
+A Piece provides a method `Piece.rotate(matrix)`, which accepts a (90 degree)
+rotation matrix. A matrix-vector multiplication is done to update the Piece's
+`position` vector. Then we update the `colors` vector, by swapping exactly two
+entries in the `colors` vector:
+
+- For example, a corner Piece has three stickers of different colors. After a
+  90 degree rotation of the Piece, one sticker remains facing down the same
+  axis, while the other two stickers swap axes. This corresponds to swapping the
+  positions of two entries in the Piece’s `colors` vector.
+- For an edge or face piece, the argument is the same as above, although we may
+  swap around one or more null entries.
+
+### Cube
+
+The Cube class is built on top of the Piece class. The Cube stores a list of
+Pieces and provides nice methods for flipping slices of the cube, as well as
+methods for querying the current state. (I followed standard [Rubik's Cube
+notation](http://ruwix.com/the-rubiks-cube/notation/))
+
+Because the Piece class encapsulates all of the rotation logic, implementing
+rotations in the Cube class is dead simple - just apply the appropriate
+rotation matrix to all Pieces involved in the rotation. An example: To
+implement `Cube.L()` - a clockwise rotation of the left face - do the
+following:
+
+1. Construct the appropriate [rotation matrix](
+http://en.wikipedia.org/wiki/Rotation_matrix) for a 90 degree rotation in the
+`x = -1` plane.
+2. Select all Pieces satisfying `position.x == -1`.
+3. Apply the rotation matrix to each of these Pieces.
+
+To implement `Cube.X()` - a clockwise rotation of the entire cube around the
+positive x-axis - just apply a rotation matrix to all Pieces stored in the
+Cube.
+
+### Solver
+
+The solver implements the algorithm described
+[here](http://www.chessandpoker.com/rubiks-cube-solution.html). It is a
+layer-by-layer solution. First the front-face (the `z = 1` plane) is solved,
+then the middle layer (`z = 0`), and finally the back layer (`z = -1`). When
+the solver is done, `Solver.moves` is a list representing the solution
+sequence.
+
+My first correct-looking implementation of the solver average 252.5 moves per
+solution sequence on 135000 randomly-generated cubes (with no failures).
+Implementing a dumb optimizer reduced the average number of moves to 192.7 on
+67000 randomly-generated cubes. The optimizer does the following:
+
+1. Eliminate full-cube rotations by "unrotating" the moves (Z U L D Zi becomes
+L D R)
+2. Eliminate moves followed by their inverse (R R Ri Ri is gone)
+3. Replace moves repeated three times with a single turn in the opposite
+direction (R R R becomes Ri)
+
+The solver is not particularly fast. On my machine (a 4.0 Ghz i7), it takes
+about 0.06 seconds per solve on CPython, which is roughly 16.7 solves/second.
+On PyPy, this is reduced to about 0.013 seconds per solve, or about 76
+solves/second.
```

### Comparing `rubik-cube-0.0.1/README.md` & `rubik-cube-0.0.2/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,10 @@
+![PyPI](https://img.shields.io/pypi/v/rubik-cube)
+![PyPI - Python Version](https://img.shields.io/pypi/pyversions/rubik-cube)
+
 # Overview
 
 This is a Python 3 implementation of a (3x3) Rubik's Cube solver.
 
 It contains:
 
 - A simple implementation of the cube
@@ -94,15 +97,14 @@
 To implement `Cube.X()` - a clockwise rotation of the entire cube around the
 positive x-axis - just apply a rotation matrix to all Pieces stored in the
 Cube.
 
 ### Solver
 
 The solver implements the algorithm described
-[here](http://peter.stillhq.com/jasmine/rubikscubesolution.html) and
 [here](http://www.chessandpoker.com/rubiks-cube-solution.html). It is a
 layer-by-layer solution. First the front-face (the `z = 1` plane) is solved,
 then the middle layer (`z = 0`), and finally the back layer (`z = -1`). When
 the solver is done, `Solver.moves` is a list representing the solution
 sequence.
 
 My first correct-looking implementation of the solver average 252.5 moves per
```

### Comparing `rubik-cube-0.0.1/setup.py` & `rubik-cube-0.0.2/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import setuptools
 
 long_description = open("README.md").read()
 
 setup_params = dict(
     name="rubik-cube",
-    version="0.0.1",
+    version="0.0.2",
     license="MIT",
     author="Paul Glass",
     author_email="pnglass@gmail.com",
     url="https://github.com/pglass/cube",
     keywords="rubik cube solver",
     packages=["rubik"],
     package_data={"": ["LICENSE"]},
@@ -20,15 +20,17 @@
     install_requires=[],
     classifiers=[
         "Development Status :: 4 - Beta",
         "Environment :: Console",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
-        "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
+        "Programming Language :: Python :: 3.9",
+        "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
     ],
 )
 
 if __name__ == "__main__":
     setuptools.setup(**setup_params)
```

### Comparing `rubik-cube-0.0.1/rubik/optimize.py` & `rubik-cube-0.0.2/rubik/optimize.py`

 * *Files identical despite different names*

### Comparing `rubik-cube-0.0.1/rubik/cube.py` & `rubik-cube-0.0.2/rubik/cube.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 import string
-import textwrap
 
 from rubik.maths import Point, Matrix
 
 RIGHT = X_AXIS = Point(1, 0, 0)
 LEFT           = Point(-1, 0, 0)
 UP    = Y_AXIS = Point(0, 1, 0)
 DOWN           = Point(0, -1, 0)
```

### Comparing `rubik-cube-0.0.1/rubik/solve.py` & `rubik-cube-0.0.2/rubik/solve.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,7 @@
-import sys
-import time
 from rubik import cube
 from rubik.maths import Point
 
 DEBUG = False
 
 
 class Solver:
@@ -14,14 +12,16 @@
         self.moves = []
 
         self.left_piece  = self.cube.find_piece(self.cube.left_color())
         self.right_piece = self.cube.find_piece(self.cube.right_color())
         self.up_piece    = self.cube.find_piece(self.cube.up_color())
         self.down_piece  = self.cube.find_piece(self.cube.down_color())
 
+        self.inifinite_loop_max_iterations = 12
+
     def solve(self):
         if DEBUG: print(self.cube)
         self.cross()
         if DEBUG: print('Cross:\n', self.cube)
         self.cross_corners()
         if DEBUG: print('Corners:\n', self.cube)
         self.second_layer()
@@ -87,15 +87,15 @@
         assert edge_piece.pos.z == -1
 
         # piece is at z = -1, rotate to correct face (LEFT or RIGHT)
         count = 0
         while (edge_piece.pos.x, edge_piece.pos.y) != (face_piece.pos.x, face_piece.pos.y):
             self.move("B")
             count += 1
-            if count == 10:
+            if count >= self.inifinite_loop_max_iterations:
                 raise Exception("Stuck in loop - unsolvable cube?\n" + str(self.cube))
 
         # if we moved a correctly-placed piece, restore it
         if undo_move:
             self.move(undo_move)
 
         # the piece is on the correct face on plane z = -1, but has two orientations
@@ -237,15 +237,15 @@
             if state4() or state2():
                 self.move("D F R Fi Ri Di")
             elif state3():
                 self.move("D R F Ri Fi Di")
             else:
                 self.move("F")
             count += 1
-            if count == 10:
+            if count >= self.inifinite_loop_max_iterations:
                 raise Exception("Stuck in loop - unsolvable cube\n" + str(self.cube))
 
         self.move("Xi Xi")
 
     def last_layer_corners_position(self):
         self.move("X X")
         # UP face:
@@ -336,25 +336,30 @@
                     self.cube[ 1, -1, 1].colors[2] == self.cube.front_color() and
                     self.cube[-1, -1, 1].colors[2] == self.cube.front_color() and
                     self.cube[-1,  1, 1].colors[2] == self.cube.front_color())
 
         move_1 = "Ri Fi R Fi Ri F F R F F "
         move_2 = "R F Ri F R F F Ri F F "
 
+        count = 0
         while not state8():
             if state1(): self.move(move_1)
             elif state2(): self.move(move_2)
             elif state3(): self.move(move_2 + "F F " + move_1)
             elif state4(): self.move(move_2 + move_1)
             elif state5(): self.move(move_1 + "F " + move_2)
             elif state6(): self.move(move_1 + "Fi " + move_1)
             elif state7(): self.move(move_1 + "F F " + move_1)
             else:
                 self.move("F")
 
+            count += 1
+            if count >= self.inifinite_loop_max_iterations:
+                raise Exception("Stuck in loop - unsolvable cube:\n" + str(self.cube))
+
         # rotate corners into correct locations (cube is inverted, so swap up and down colors)
         bru_corner = self.cube.find_piece(self.cube.front_color(), self.cube.right_color(), self.cube.up_color())
         while bru_corner.pos != Point(1, 1, 1):
             self.move("F")
 
         self.move("Xi Xi")
 
@@ -432,15 +437,15 @@
             if h_pattern1():
                 self.move(h_pattern_move)
             elif h_pattern2():
                 self.move("Z " + h_pattern_move + "Zi")
             else:
                 self.move(cycle_move)
             count += 1
-            if count == 10:
+            if count >= self.inifinite_loop_max_iterations:
                 raise Exception("Stuck in loop - unsolvable cube:\n" + str(self.cube))
 
         self.move("Xi Xi")
 
 
     def _handle_last_layer_state1(self, br_edge, bl_edge, bu_edge, bd_edge, cycle_move, h_move):
         if DEBUG: print("_handle_last_layer_state1")
@@ -475,25 +480,25 @@
             piece = self.cube[cube.DOWN + cube.FRONT]
             if piece.colors[2] == self.cube.front_color() and piece.colors[1] == self.cube.down_color():
                 return piece
 
         count = 0
         while True:
             edge = correct_edge()
-            if edge == None:
+            if edge is None:
                 self.move(cycle_move)
             else:
                 break
 
             count += 1
 
             if count % 3 == 0:
                 self.move("Z")
 
-            if count == 12:
+            if count >= self.inifinite_loop_max_iterations:
                 raise Exception("Stuck in loop - unsolvable cube:\n" + str(self.cube))
 
         while edge.pos != Point(-1, 0, 1):
             self.move("Z")
 
         assert self.cube[cube.LEFT + cube.FRONT].colors[2] == self.cube.front_color() and \
                self.cube[cube.LEFT + cube.FRONT].colors[0] == self.cube.left_color()
```

### Comparing `rubik-cube-0.0.1/rubik/maths.py` & `rubik-cube-0.0.2/rubik/maths.py`

 * *Files 1% similar despite different names*

```diff
@@ -91,15 +91,15 @@
         Matrix(x for x in range(1, 10))
         """
         if len(args) == 9:
             self.vals = list(args)
         elif len(args) == 3:
             try:
                 self.vals = [x for y in args for x in y]
-            except:
+            except Exception:
                 self.vals = []
         else:
             self.__init__(*args[0])
 
         if len(self.vals) != 9:
             raise ValueError(f"Matrix requires 9 items, got {args}")
```

