# Comparing `tmp/kektris-0.0.1.tar.gz` & `tmp/kektris-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kektris-0.0.1.tar", last modified: Fri May  5 21:51:48 2023, max compression
+gzip compressed data, was "kektris-0.0.2.tar", last modified: Sat May 13 00:36:09 2023, max compression
```

## Comparing `kektris-0.0.1.tar` & `kektris-0.0.2.tar`

### file list

```diff
@@ -1,20 +1,21 @@
-drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-05 21:51:48.961823 kektris-0.0.1/
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1076 2023-05-04 20:42:52.000000 kektris-0.0.1/LICENSE
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)       45 2023-05-05 21:22:56.000000 kektris-0.0.1/MANIFEST.in
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      476 2023-05-05 21:49:35.000000 kektris-0.0.1/Makefile
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1295 2023-05-05 21:51:48.961823 kektris-0.0.1/PKG-INFO
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      801 2023-05-05 21:51:26.000000 kektris-0.0.1/README.md
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      683 2023-05-05 21:43:16.000000 kektris-0.0.1/requirements-dev.txt
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      208 2023-05-05 21:51:48.961823 kektris-0.0.1/setup.cfg
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1607 2023-05-05 21:28:52.000000 kektris-0.0.1/setup.py
-drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-05 21:51:48.961823 kektris-0.0.1/src/
-drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-05 21:51:48.961823 kektris-0.0.1/src/kektris.egg-info/
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1295 2023-05-05 21:51:48.000000 kektris-0.0.1/src/kektris.egg-info/PKG-INFO
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      321 2023-05-05 21:51:48.000000 kektris-0.0.1/src/kektris.egg-info/SOURCES.txt
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)        1 2023-05-05 21:51:48.000000 kektris-0.0.1/src/kektris.egg-info/dependency_links.txt
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      704 2023-05-05 21:51:48.000000 kektris-0.0.1/src/kektris.egg-info/requires.txt
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)        1 2023-05-05 21:51:48.000000 kektris-0.0.1/src/kektris.egg-info/top_level.txt
-drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-05 21:51:48.961823 kektris-0.0.1/tests/
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)    15315 2023-05-05 16:24:59.000000 kektris-0.0.1/tests/test_blocks.py
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      337 2023-05-05 15:30:38.000000 kektris-0.0.1/tests/test_constraints.py
--rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     9759 2023-05-05 16:24:59.000000 kektris-0.0.1/tests/test_kektris.py
+drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-13 00:36:09.273082 kektris-0.0.2/
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1076 2023-05-04 20:42:52.000000 kektris-0.0.2/LICENSE
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)       85 2023-05-13 00:36:02.000000 kektris-0.0.2/MANIFEST.in
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      476 2023-05-05 22:22:44.000000 kektris-0.0.2/Makefile
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1520 2023-05-13 00:36:09.273082 kektris-0.0.2/PKG-INFO
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)    13885 2023-05-13 00:34:58.000000 kektris-0.0.2/Q-tris.png
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1026 2023-05-13 00:34:58.000000 kektris-0.0.2/README.md
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      683 2023-05-05 22:22:44.000000 kektris-0.0.2/requirements-dev.txt
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      208 2023-05-13 00:36:09.273082 kektris-0.0.2/setup.cfg
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1607 2023-05-13 00:34:58.000000 kektris-0.0.2/setup.py
+drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-13 00:36:09.273082 kektris-0.0.2/src/
+drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-13 00:36:09.273082 kektris-0.0.2/src/kektris.egg-info/
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     1520 2023-05-13 00:36:09.000000 kektris-0.0.2/src/kektris.egg-info/PKG-INFO
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      332 2023-05-13 00:36:09.000000 kektris-0.0.2/src/kektris.egg-info/SOURCES.txt
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)        1 2023-05-13 00:36:09.000000 kektris-0.0.2/src/kektris.egg-info/dependency_links.txt
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      704 2023-05-13 00:36:09.000000 kektris-0.0.2/src/kektris.egg-info/requires.txt
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)        1 2023-05-13 00:36:09.000000 kektris-0.0.2/src/kektris.egg-info/top_level.txt
+drwxrwxr-x   0 kklepikov  (1000) kklepikov  (1000)        0 2023-05-13 00:36:09.273082 kektris-0.0.2/tests/
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)    16098 2023-05-11 21:58:51.000000 kektris-0.0.2/tests/test_blocks.py
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)      684 2023-05-11 22:38:12.000000 kektris-0.0.2/tests/test_constraints.py
+-rw-rw-r--   0 kklepikov  (1000) kklepikov  (1000)     9950 2023-05-12 22:50:14.000000 kektris-0.0.2/tests/test_kektris.py
```

### Comparing `kektris-0.0.1/LICENSE` & `kektris-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `kektris-0.0.1/PKG-INFO` & `kektris-0.0.2/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kektris
-Version: 0.0.1
+Version: 0.0.2
 Summary: 4-quarter tetris created by Pyxel
 Home-page: https://github.com/KonstantinKlepikov/kektris
 Author: Konstantin Klepikov
 Author-email: oformleno@gmail.com
 License: MIT
 Keywords: game
 Classifier: Programming Language :: Python :: 3
@@ -15,24 +15,26 @@
 Provides-Extra: dev
 License-File: LICENSE
 
 # kektris
 
 4-quarter tetris created by [Pyxel](https://github.com/kitao/pyxel)
 
+![Q-tris](Q-tris.png "Q-tris")
+
 ## Development and destribution
 
 Typicaly: `pip install -e .[dev]`
 
 Available make cli:
 
 ```sh
 make test
 make run
-make pypi-test
+make test-pypi
 make pypi
 make build-example
 ```
 
 When `build-example` - result is propogated to folder example - here is html-launcher and application file (.pyxapp).
 
 Pyxel cli:
@@ -46,7 +48,11 @@
 pyxel app2exe PYXEL_APP_FILE(.pyxapp)
 pyxel app2html PYXEL_APP_FILE(.pyxapp)
 ```
 
 ## Play the game in web
 
 [wasm launcher](https://kitao.github.io/pyxel/wasm/launcher/?play=KonstantinKlepikov.kektris.example.kektris)
+
+## Reference
+
+A little of code idea is get from [this](https://github.com/shivanju/pyxel-games/tree/master) tetris repo. Music is copypasted from [pyxel](https://github.com/kitao/pyxel) demo.
```

### Comparing `kektris-0.0.1/README.md` & `kektris-0.0.2/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 # kektris
 
 4-quarter tetris created by [Pyxel](https://github.com/kitao/pyxel)
 
+![Q-tris](Q-tris.png "Q-tris")
+
 ## Development and destribution
 
 Typicaly: `pip install -e .[dev]`
 
 Available make cli:
 
 ```sh
 make test
 make run
-make pypi-test
+make test-pypi
 make pypi
 make build-example
 ```
 
 When `build-example` - result is propogated to folder example - here is html-launcher and application file (.pyxapp).
 
 Pyxel cli:
@@ -29,7 +31,11 @@
 pyxel app2exe PYXEL_APP_FILE(.pyxapp)
 pyxel app2html PYXEL_APP_FILE(.pyxapp)
 ```
 
 ## Play the game in web
 
 [wasm launcher](https://kitao.github.io/pyxel/wasm/launcher/?play=KonstantinKlepikov.kektris.example.kektris)
+
+## Reference
+
+A little of code idea is get from [this](https://github.com/shivanju/pyxel-games/tree/master) tetris repo. Music is copypasted from [pyxel](https://github.com/kitao/pyxel) demo.
```

### Comparing `kektris-0.0.1/requirements-dev.txt` & `kektris-0.0.2/requirements-dev.txt`

 * *Files identical despite different names*

### Comparing `kektris-0.0.1/setup.py` & `kektris-0.0.2/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 EMAIL = 'oformleno@gmail.com'
 DESCRIPTION = '4-quarter tetris created by Pyxel'
 LONG_DESCRIPTION = (here / "README.md").read_text(encoding="utf-8")
 SOURCE_URL = 'https://github.com/KonstantinKlepikov/kektris'
 
 setup(
     name=NAME,
-    version='0.0.1',
+    version='0.0.2',
     install_requires=get_dependencies('requirements.txt'),
     extras_require={
         "dev": get_dependencies('requirements-dev.txt'),
     },
     description=DESCRIPTION,
     long_description=LONG_DESCRIPTION,
     long_description_content_type='text/markdown',
```

### Comparing `kektris-0.0.1/src/kektris.egg-info/PKG-INFO` & `kektris-0.0.2/src/kektris.egg-info/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kektris
-Version: 0.0.1
+Version: 0.0.2
 Summary: 4-quarter tetris created by Pyxel
 Home-page: https://github.com/KonstantinKlepikov/kektris
 Author: Konstantin Klepikov
 Author-email: oformleno@gmail.com
 License: MIT
 Keywords: game
 Classifier: Programming Language :: Python :: 3
@@ -15,24 +15,26 @@
 Provides-Extra: dev
 License-File: LICENSE
 
 # kektris
 
 4-quarter tetris created by [Pyxel](https://github.com/kitao/pyxel)
 
+![Q-tris](Q-tris.png "Q-tris")
+
 ## Development and destribution
 
 Typicaly: `pip install -e .[dev]`
 
 Available make cli:
 
 ```sh
 make test
 make run
-make pypi-test
+make test-pypi
 make pypi
 make build-example
 ```
 
 When `build-example` - result is propogated to folder example - here is html-launcher and application file (.pyxapp).
 
 Pyxel cli:
@@ -46,7 +48,11 @@
 pyxel app2exe PYXEL_APP_FILE(.pyxapp)
 pyxel app2html PYXEL_APP_FILE(.pyxapp)
 ```
 
 ## Play the game in web
 
 [wasm launcher](https://kitao.github.io/pyxel/wasm/launcher/?play=KonstantinKlepikov.kektris.example.kektris)
+
+## Reference
+
+A little of code idea is get from [this](https://github.com/shivanju/pyxel-games/tree/master) tetris repo. Music is copypasted from [pyxel](https://github.com/kitao/pyxel) demo.
```

### Comparing `kektris-0.0.1/src/kektris.egg-info/requires.txt` & `kektris-0.0.2/src/kektris.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `kektris-0.0.1/tests/test_blocks.py` & `kektris-0.0.2/tests/test_blocks.py`

 * *Files 2% similar despite different names*

```diff
@@ -131,14 +131,22 @@
         assert len(grid.get_frozen) == 1, 'wrong frozen cells len'
 
 
 class TestWindow:
     """Test FigureWinfow class
     """
 
+    @pytest.fixture(scope='function', params=FigureOrientation.get_includes())
+    def window(self, grid: Grid, request) -> Window:
+        """Make window
+        """
+        window = Window((0, 0), request.param, grid, Direction.LEFT)
+        window.param = request.param
+        return window
+
     @pytest.mark.parametrize(
         'direction,arrive_pos', [
             (Direction.RIGHT, (-4, 0)),
             (Direction.LEFT, (34, 0)),
             (Direction.UP, (0, 34)),
             (Direction.DOWN, (0, -4))
                 ]
@@ -215,14 +223,25 @@
         """Test msp window return cells with ofboard from ищеещь кшпре
         """
         window = Window((33, 31), FigureOrientation.I_U, grid, Direction.LEFT)
         m = window.map_window
         assert len(m) == 1, 'wrong result len'
         assert m[0].pos == grid.grid[33][32].pos, 'wrong figure'
 
+    def test_window_figure_pos(self, window: Window) -> None:
+        """Test window figure position returns positions on grid
+        """
+        assert len(window.window_figure_pos) == 4, 'wrong figure positions'
+
+    def test_window_figure_pos_dont_return_offgrid(self, window: Window) -> None:
+        """Test window figure position returns positions offgrid
+        """
+        window.top_left = (-4, -4)
+        assert len(window.window_figure_pos) == 4, 'wrong figure positions'
+
     def test_has_frozen(self, grid: Grid) -> None:
         """Test has frozen mapped window
         """
         window = Window((0, 0), FigureOrientation.I_L, grid, Direction.LEFT)
         assert not window.has_frozen(), 'has frozen'
         window = Window((0, 0), FigureOrientation.I_U, grid, Direction.LEFT)
         window.grid.grid[1][1].freeze()
```

### Comparing `kektris-0.0.1/tests/test_kektris.py` & `kektris-0.0.2/tests/test_kektris.py`

 * *Files 11% similar despite different names*

```diff
@@ -19,34 +19,34 @@
         assert isinstance(make_app.grid, Grid), 'wrong grid'
         assert not make_app.grid_higlight, 'grid highlited'
 
     def test_generate_figure_start_position(self, make_app: Game) -> None:
         """Test random figure generation
         """
         with FixedSeed(42):
-            top_left, orientation = make_app._generate_figure_start_position()
+            top_left, orientation = make_app.generate_figure_start_position()
             assert isinstance(top_left, tuple), 'wrong result'
             assert top_left == (-4, 21), 'wrong top left position'
             assert orientation == FigureOrientation.I_R, 'wrong orientation'
 
     def test_generate_figure_start_position_probability(self, make_app: Game) -> None:
         """Test generate_figure_start_position probabilitie
         """
         figures = {name: 0 for name in FigureOrientation.get_names()}
         with FixedSeed(42):
             for _ in range(1000):
-                figures[make_app._generate_figure_start_position()[1].name] += 1
+                figures[make_app.generate_figure_start_position()[1].name] += 1
             assert figures['O'] == 144, 'wrong sample'
             assert figures['I_U'] == 24, 'wrong sample'
 
     def test_arrive_figure(self, make_app: Game) -> None:
         """Test arrive figure
         """
         with FixedSeed(42):
-            figure = make_app._arrive_figure()
+            figure = make_app.arrive_figure()
             assert isinstance(figure, Figure), 'wrong figure move_direction'
             assert figure.window.top_left == (-4, 21), \
                 'wrong top left position'
             assert figure.window.orientation == FigureOrientation.I_R, \
                 'wrong orientation'
 
     def test_get_chunked(self, make_app: Game) -> None:
@@ -102,15 +102,15 @@
         ) -> None:
         """Test is line is ready to clear
         """
         for p in frozen:
             make_app.grid.grid[p[0]][p[1]].freeze()
         frozen_pos = [p.pos for p in make_app.grid.get_frozen]
         assert len(make_app.grid.get_frozen) == len(frozen), 'wrong frozen'
-        line = make_app._check_line(1, frozen_pos)
+        line = make_app.check_line(1, frozen_pos)
         assert isinstance(line, list), 'wrong line type'
         assert isinstance(line[0], tuple), 'wrong pos'
         assert line == result, 'wrong comparison'
         if ost:
             for p in ost:
                 assert make_app.grid.grid[p[0]][p[1]].is_frozen, 'unfrozen'
 
@@ -119,33 +119,33 @@
         """
         for p in range(12):
             make_app.grid.grid[p][0].freeze()
         for p in range(14, 17):
             make_app.grid.grid[p][0].freeze()
         frozen_pos = [p.pos for p in make_app.grid.get_frozen]
         assert len(make_app.grid.get_frozen) == 15, 'wrong frozen'
-        line = make_app._check_line(1, frozen_pos)
+        line = make_app.check_line(1, frozen_pos)
         assert isinstance(line, list), 'wrong line type'
         assert isinstance(line[0], tuple), 'wrong pos'
         assert len(line) == 12, 'wrong line lenght'
         assert frozen_pos[0:12] == line, 'wrong comparison'
 
     def test_get_shift(self, make_app: Game) -> None:
         """Test get shift for frozen cells
         """
         make_app.figure.window.move_direction = Direction.LEFT
-        assert make_app._get_shift(0, 0) == (1, 0), 'wrong left shift'
-        assert make_app._get_shift(12, 0) == (13, 0), 'wrong colossal shift'
+        assert make_app.get_shift(0, 0) == (1, 0), 'wrong left shift'
+        assert make_app.get_shift(12, 0) == (13, 0), 'wrong colossal shift'
         make_app.figure.window.move_direction = Direction.RIGHT
-        assert make_app._get_shift(0, 0) == (-1, 0), 'wrong right shift'
-        assert make_app._get_shift(12, 0) == (11, 0), 'wrong colossal shift'
+        assert make_app.get_shift(0, 0) == (-1, 0), 'wrong right shift'
+        assert make_app.get_shift(12, 0) == (11, 0), 'wrong colossal shift'
         make_app.figure.window.move_direction = Direction.UP
-        assert make_app._get_shift(0, 0) == (0, 1), 'wrong up shift'
+        assert make_app.get_shift(0, 0) == (0, 1), 'wrong up shift'
         make_app.figure.window.move_direction = Direction.DOWN
-        assert make_app._get_shift(0, 0) == (0, -1), 'wrong down shift'
+        assert make_app.get_shift(0, 0) == (0, -1), 'wrong down shift'
 
     @pytest.mark.parametrize(
         'frozen,line,result,direction', [
             (
                 [(31,0), (31,1), (31,2), (32,0), (33,5)],
                 [(30,n) for n in range(7)] ,
                 [(31,0), (31,1), (31,2), (32,0)],
@@ -169,15 +169,15 @@
             ) -> None:
         """Test frozen can be shifted
         """
         make_app.figure.window.move_direction = direction
         quarter = make_app.figure.window.quarter
         for pos in frozen:
             make_app.grid.grid[pos[0]][pos[1]].freeze()
-        shifted = make_app._get_shifted_frozen(line)
+        shifted = make_app.get_shifted_frozen(line)
         assert shifted == result, 'wrong shifted'
         for pos in shifted:
             assert pos in quarter, 'not in quarter'
 
     @pytest.mark.parametrize(
         'shifted,result,direction', [
             (
@@ -206,52 +206,48 @@
             ) -> None:
         """Test move shifted frozen
         """
         make_app.figure.window.move_direction = direction
         quarter = make_app.figure.window.quarter
         for pos in shifted:
             make_app.grid.grid[pos[0]][pos[1]].freeze()
-        make_app._move_shifted_frozen(shifted)
+        make_app.move_shifted_frozen(shifted)
         assert {cell.pos for cell in make_app.grid.get_frozen} == result, 'wrong result'
 
     def test_change_speed(self, make_app: Game) -> None:
         """Test change speed
         """
-        make_app._change_speed()
+        make_app.change_speed()
         assert make_app.speed == 0, 'mistaken grown'
 
         make_app.score = const.SPEED_MODIFICATOR
-        make_app._change_speed()
+        make_app.change_speed()
         assert make_app.speed == 1, 'not grown'
         assert make_app.speed_color_timeout == const.COLOR_TIMOUT, 'wrong timout'
 
-        make_app.score = const.SPEED_MODIFICATOR*const.GAME_SPEED
-        make_app.speed = const.GAME_SPEED-1
-        make_app._change_speed()
-        assert make_app.speed == const.GAME_SPEED, 'not grown'
+        make_app.score = const.SPEED_MODIFICATOR*const.MAX_GAME_SPEED
+        make_app.speed = const.MAX_GAME_SPEED-1
+        make_app.change_speed()
+        assert make_app.speed == const.MAX_GAME_SPEED, 'not grown'
 
         make_app.score = const.SPEED_MODIFICATOR*100000
-        make_app._change_speed()
-        assert make_app.speed == const.GAME_SPEED, 'wrong grown'
+        make_app.change_speed()
+        assert make_app.speed == const.MAX_GAME_SPEED, 'wrong grown'
 
-    @pytest.mark.parametrize(
-        'positions,result', [
-        ([(0,0),], True),
-        ([(1,1),], False),
-        ([(1,1),(0,0)], True),
-        ([(33,33),], True),
-        ([(33,0),], True),
-        ([(0,33),], True),
-            ]
-        )
-    def test_is_game_over(
-        self,
-        make_app: Game,
-        positions: list[tuple[int, int]],
-        result: bool,
-            ) -> None:
-        """Test game is over
+    def test_change_clear_line_lenght(self, make_app: Game) -> None:
+        """Test change clear line lenght
         """
-        assert not make_app.is_over, 'game over'
-        for pos in positions:
-            make_app.grid.grid[pos[0]][pos[1]].freeze()
-        assert make_app._is_game_over() == result, 'wrong result'
+        make_app.change_line_lenght()
+        assert make_app.line_lenght == const.START_CLEAR_LENGTH, 'mistaken grown'
+
+        make_app.score = const.LENGHT_MODIFICATOR
+        make_app.change_line_lenght()
+        assert make_app.line_lenght == const.START_CLEAR_LENGTH + 1, 'not grown'
+        assert make_app.line_color_timeout == const.COLOR_TIMOUT, 'wrong timout'
+
+        make_app.score = const.LENGHT_MODIFICATOR*100000
+        make_app.line_lenght = const.MAX_CLEAR_LENGHT-1
+        make_app.change_line_lenght()
+        assert make_app.line_lenght == const.MAX_CLEAR_LENGHT, 'not grown'
+
+        make_app.change_line_lenght()
+        assert make_app.line_lenght == const.MAX_CLEAR_LENGHT, 'wrong grown'
```

