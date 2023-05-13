# Comparing `tmp/librenv-0.1-py3.11.egg` & `tmp/librenv-0.1.1-py3.11.egg`

## zipinfo {}

```diff
@@ -1,24 +1,28 @@
-Zip file size: 12681 bytes, number of entries: 22
--rw-r--r--  2.0 unx      760 b- defN 23-May-13 12:50 EGG-INFO/PKG-INFO
--rw-r--r--  2.0 unx      352 b- defN 23-May-13 12:50 EGG-INFO/SOURCES.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-13 12:50 EGG-INFO/dependency_links.txt
--rw-r--r--  2.0 unx       50 b- defN 23-May-13 12:50 EGG-INFO/entry_points.txt
--rw-r--r--  2.0 unx        8 b- defN 23-May-13 12:50 EGG-INFO/top_level.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-13 12:50 EGG-INFO/zip-safe
--rw-r--r--  2.0 unx       81 b- defN 23-May-13 10:44 librenv/__init__.py
+Zip file size: 15763 bytes, number of entries: 26
+-rw-r--r--  2.0 unx      762 b- defN 23-May-13 14:45 EGG-INFO/PKG-INFO
+-rw-r--r--  2.0 unx      396 b- defN 23-May-13 14:45 EGG-INFO/SOURCES.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 14:45 EGG-INFO/dependency_links.txt
+-rw-r--r--  2.0 unx       50 b- defN 23-May-13 14:45 EGG-INFO/entry_points.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-May-13 14:45 EGG-INFO/top_level.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-May-13 14:45 EGG-INFO/zip-safe
+-rw-r--r--  2.0 unx       83 b- defN 23-May-13 13:38 librenv/__init__.py
 -rw-r--r--  2.0 unx      258 b- defN 23-May-13 12:35 librenv/__main__.py
--rw-r--r--  2.0 unx     2117 b- defN 23-May-13 12:33 librenv/librenv.py
+-rw-r--r--  2.0 unx     2225 b- defN 23-May-13 14:41 librenv/librenv.py
 -rw-r--r--  2.0 unx     1751 b- defN 23-May-13 10:31 librenv/project.py
--rw-r--r--  2.0 unx      256 b- defN 23-May-13 12:50 librenv/__pycache__/__init__.cpython-311.pyc
--rw-r--r--  2.0 unx      866 b- defN 23-May-13 12:50 librenv/__pycache__/__main__.cpython-311.pyc
--rw-r--r--  2.0 unx     4501 b- defN 23-May-13 12:50 librenv/__pycache__/librenv.cpython-311.pyc
--rw-r--r--  2.0 unx     3210 b- defN 23-May-13 12:50 librenv/__pycache__/project.cpython-311.pyc
--rw-r--r--  2.0 unx       82 b- defN 23-May-13 10:57 librenv/api/__init__.py
+-rw-r--r--  2.0 unx      258 b- defN 23-May-13 14:45 librenv/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--  2.0 unx      866 b- defN 23-May-13 14:45 librenv/__pycache__/__main__.cpython-311.pyc
+-rw-r--r--  2.0 unx     4860 b- defN 23-May-13 14:45 librenv/__pycache__/librenv.cpython-311.pyc
+-rw-r--r--  2.0 unx     3210 b- defN 23-May-13 14:45 librenv/__pycache__/project.cpython-311.pyc
+-rw-r--r--  2.0 unx      136 b- defN 23-May-13 13:38 librenv/api/__init__.py
 -rw-r--r--  2.0 unx      349 b- defN 23-May-11 10:42 librenv/api/color.py
--rw-r--r--  2.0 unx      490 b- defN 23-May-13 12:38 librenv/api/sprite.py
+-rw-r--r--  2.0 unx      324 b- defN 23-May-13 14:42 librenv/api/drawable.py
+-rw-r--r--  2.0 unx      539 b- defN 23-May-13 14:42 librenv/api/sprite.py
+-rw-r--r--  2.0 unx      641 b- defN 23-May-13 14:40 librenv/api/text.py
 -rw-r--r--  2.0 unx      445 b- defN 23-May-13 12:45 librenv/api/vector2.py
--rw-r--r--  2.0 unx      318 b- defN 23-May-13 12:50 librenv/api/__pycache__/__init__.cpython-311.pyc
--rw-r--r--  2.0 unx     1369 b- defN 23-May-13 12:50 librenv/api/__pycache__/color.cpython-311.pyc
--rw-r--r--  2.0 unx     1439 b- defN 23-May-13 12:50 librenv/api/__pycache__/sprite.cpython-311.pyc
--rw-r--r--  2.0 unx     1173 b- defN 23-May-13 12:50 librenv/api/__pycache__/vector2.cpython-311.pyc
-22 files, 19877 bytes uncompressed, 9687 bytes compressed:  51.3%
+-rw-r--r--  2.0 unx      424 b- defN 23-May-13 14:45 librenv/api/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--  2.0 unx     1369 b- defN 23-May-13 14:45 librenv/api/__pycache__/color.cpython-311.pyc
+-rw-r--r--  2.0 unx     1187 b- defN 23-May-13 14:45 librenv/api/__pycache__/drawable.cpython-311.pyc
+-rw-r--r--  2.0 unx     1617 b- defN 23-May-13 14:45 librenv/api/__pycache__/sprite.cpython-311.pyc
+-rw-r--r--  2.0 unx     1786 b- defN 23-May-13 14:45 librenv/api/__pycache__/text.cpython-311.pyc
+-rw-r--r--  2.0 unx     1173 b- defN 23-May-13 14:45 librenv/api/__pycache__/vector2.cpython-311.pyc
+26 files, 24719 bytes uncompressed, 12197 bytes compressed:  50.7%
```

## zipnote «TEMP»/diffoscope_jdnt50yt_/tmp5rgcwwi4_.zip

```diff
@@ -42,26 +42,38 @@
 
 Filename: librenv/api/__init__.py
 Comment: 
 
 Filename: librenv/api/color.py
 Comment: 
 
+Filename: librenv/api/drawable.py
+Comment: 
+
 Filename: librenv/api/sprite.py
 Comment: 
 
+Filename: librenv/api/text.py
+Comment: 
+
 Filename: librenv/api/vector2.py
 Comment: 
 
 Filename: librenv/api/__pycache__/__init__.cpython-311.pyc
 Comment: 
 
 Filename: librenv/api/__pycache__/color.cpython-311.pyc
 Comment: 
 
+Filename: librenv/api/__pycache__/drawable.cpython-311.pyc
+Comment: 
+
 Filename: librenv/api/__pycache__/sprite.cpython-311.pyc
 Comment: 
 
+Filename: librenv/api/__pycache__/text.cpython-311.pyc
+Comment: 
+
 Filename: librenv/api/__pycache__/vector2.cpython-311.pyc
 Comment: 
 
 Zip file comment:
```

## EGG-INFO/PKG-INFO

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: librenv
-Version: 0.1
+Version: 0.1.1
 Summary: Simple visual novel engine, written on Python3+SDL2.
 Home-page: https://notabug.org/loliconshik3/librenv
 Author: loliconshik3
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # librenv
```

## EGG-INFO/SOURCES.txt

```diff
@@ -8,9 +8,11 @@
 librenv.egg-info/PKG-INFO
 librenv.egg-info/SOURCES.txt
 librenv.egg-info/dependency_links.txt
 librenv.egg-info/entry_points.txt
 librenv.egg-info/top_level.txt
 librenv/api/__init__.py
 librenv/api/color.py
+librenv/api/drawable.py
 librenv/api/sprite.py
+librenv/api/text.py
 librenv/api/vector2.py
```

## librenv/__init__.py

```diff
@@ -1,4 +1,4 @@
 """
 Simple visual novel engine, written on Python3+SDL2.
 """
-__version__ = "0.1"
+__version__ = "0.1.1"
```

## librenv/librenv.py

```diff
@@ -1,67 +1,70 @@
 from threading import Thread
 from sdl2.sdlimage import IMG_INIT_JPG, IMG_INIT_PNG, IMG_INIT_WEBP, IMG_Init
-from sdl2.ext import fill
+from sdl2.sdlttf import TTF_Init
+from sdl2.ext import Renderer, init
 from sdl2 import *
 import ctypes
 import time
 import os
 
+from .api.drawable import Drawable
 from .project import Project
-from .api.sprite import Sprite
 
 class LibreNV:
 
     def __init__(self):
-        # Initialize video
+        # Initialize SDL 
+        init()
         SDL_Init(SDL_INIT_EVERYTHING)
         IMG_Init(IMG_INIT_JPG | IMG_INIT_PNG | IMG_INIT_WEBP)
-        
+        TTF_Init()
+
         # Make window
         self.window = SDL_CreateWindow(b"LibreNV",
                                        SDL_WINDOWPOS_CENTERED, SDL_WINDOWPOS_CENTERED,
                                        800, 600, SDL_WINDOW_SHOWN)
         self.windowsurface = SDL_GetWindowSurface(self.window)
+        self.renderer = Renderer(self.windowsurface)
         self.running = True
         self.thread = None
 
     def load_game(self, game_path):
         project_path = game_path + "/project.json"
         if not os.path.exists(project_path):
             return print("project.json not found!")
         project = Project.from_file(project_path)     
         SDL_SetWindowTitle(self.window, bytes(project.name, 'utf-8'))
         self.thread = Thread(target=project.run)
         self.thread.start()
         return self.loop()
 
-    def get_drawables(self):
-        return Sprite.SPRITES
+    def get_drawables(self) -> list:
+        return Drawable.DRAWABLES
 
-    def draw_background(self):
-        fill(self.windowsurface, 0)
+    def draw_background(self) -> None:
+        self.renderer.clear(SDL_Color(0,0,0))
 
-    def draw(self):
+    def draw(self) -> None:
         self.draw_background()
         drawables = self.get_drawables()
         for drawable in drawables:
             if drawable.is_hidden: continue
-            SDL_BlitSurface(drawable.image, None, self.windowsurface, 
-                            SDL_Rect(drawable.position.x, drawable.position.y)
-            )
+            drawable._draw(self.renderer, self.windowsurface)
+        self.renderer.present()
         SDL_UpdateWindowSurface(self.window)
 
-    def check_events(self):
+    def check_events(self) -> None:
         event = SDL_Event()
         while SDL_PollEvent(ctypes.byref(event)) != 0:
             if event.type == SDL_QUIT:
                 self.running = False
                 break
 
-    def loop(self):
+    def loop(self) -> int:
         while self.running:
             self.check_events()
             self.draw()
             time.sleep(0.016)
 
         SDL_DestroyWindow(self.window)
         SDL_Quit()
```

## librenv/__pycache__/__init__.cpython-311.pyc

### Python bytecode

```diff
@@ -1,28 +1,28 @@
 magic:    0xa70d0d0a
-moddate:  0xe23f5f64 (Sat May 13 07:44:34 2023 UTC)
-files sz: 81
+moddate:  0xac685f64 (Sat May 13 10:38:36 2023 UTC)
+files sz: 83
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 1
    flags     : 0
    code 0x970064005a0064015a0164025300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 ('\nSimple visual novel engine, written on Python3+SDL2.\n')
                  4 STORE_NAME               0 (__doc__)
    
-     4           6 LOAD_CONST               1 ('0.1')
+     4           6 LOAD_CONST               1 ('0.1.1')
                  8 STORE_NAME               1 (__version__)
                 10 LOAD_CONST               2 (None)
                 12 RETURN_VALUE
    consts
       '\nSimple visual novel engine, written on Python3+SDL2.\n'
-      '0.1'
+      '0.1.1'
       None
    names      ('__doc__', '__version__')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   'build/bdist.linux-x86_64/egg/librenv/__init__.py'
    name       '<module>'
```

## librenv/__pycache__/librenv.cpython-311.pyc

### Python bytecode

```diff
@@ -1,21 +1,22 @@
 magic:    0xa70d0d0a
-moddate:  0x87595f64 (Sat May 13 09:33:59 2023 UTC)
-files sz: 2117
+moddate:  0x80775f64 (Sat May 13 11:41:52 2023 UTC)
+files sz: 2225
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 0
    code
       0x9700640064016c006d015a010100640064026c026d035a036d045a046d
-      055a056d065a060100640064036c076d085a080100640064046c09540064
-      0064056c0a5a0a640064056c0b5a0b640064056c0c5a0c640664076c0d6d
-      0e5a0e0100640664086c0f6d105a1001000200470064098400640aa60200
-      00ab0200000000000000005a1164055300
+      055a056d065a060100640064036c076d085a080100640064046c096d0a5a
+      0a6d0b5a0b0100640064056c0c5400640064066c0d5a0d640064066c0e5a
+      0e640064066c0f5a0f640764086c106d115a110100640764096c126d135a
+      13010002004700640a8400640ba6020000ab0200000000000000005a1464
+      065300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
                  4 LOAD_CONST               1 (('Thread',))
                  6 IMPORT_NAME              0 (threading)
                  8 IMPORT_FROM              1 (Thread)
                 10 STORE_NAME               1 (Thread)
@@ -31,199 +32,240 @@
                 28 IMPORT_FROM              5 (IMG_INIT_WEBP)
                 30 STORE_NAME               5 (IMG_INIT_WEBP)
                 32 IMPORT_FROM              6 (IMG_Init)
                 34 STORE_NAME               6 (IMG_Init)
                 36 POP_TOP
    
      3          38 LOAD_CONST               0 (0)
-                40 LOAD_CONST               3 (('fill',))
-                42 IMPORT_NAME              7 (sdl2.ext)
-                44 IMPORT_FROM              8 (fill)
-                46 STORE_NAME               8 (fill)
+                40 LOAD_CONST               3 (('TTF_Init',))
+                42 IMPORT_NAME              7 (sdl2.sdlttf)
+                44 IMPORT_FROM              8 (TTF_Init)
+                46 STORE_NAME               8 (TTF_Init)
                 48 POP_TOP
    
      4          50 LOAD_CONST               0 (0)
-                52 LOAD_CONST               4 (('*',))
-                54 IMPORT_NAME              9 (sdl2)
-                56 IMPORT_STAR
-   
-     5          58 LOAD_CONST               0 (0)
-                60 LOAD_CONST               5 (None)
-                62 IMPORT_NAME             10 (ctypes)
-                64 STORE_NAME              10 (ctypes)
-   
-     6          66 LOAD_CONST               0 (0)
-                68 LOAD_CONST               5 (None)
-                70 IMPORT_NAME             11 (time)
-                72 STORE_NAME              11 (time)
-   
-     7          74 LOAD_CONST               0 (0)
-                76 LOAD_CONST               5 (None)
-                78 IMPORT_NAME             12 (os)
-                80 STORE_NAME              12 (os)
-   
-     9          82 LOAD_CONST               6 (1)
-                84 LOAD_CONST               7 (('Project',))
-                86 IMPORT_NAME             13 (project)
-                88 IMPORT_FROM             14 (Project)
-                90 STORE_NAME              14 (Project)
-                92 POP_TOP
-   
-    10          94 LOAD_CONST               6 (1)
-                96 LOAD_CONST               8 (('Sprite',))
-                98 IMPORT_NAME             15 (api.sprite)
-               100 IMPORT_FROM             16 (Sprite)
-               102 STORE_NAME              16 (Sprite)
-               104 POP_TOP
-   
-    12         106 PUSH_NULL
-               108 LOAD_BUILD_CLASS
-               110 LOAD_CONST               9 (<code object LibreNV, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 12>)
-               112 MAKE_FUNCTION            0
-               114 LOAD_CONST              10 ('LibreNV')
-               116 PRECALL                  2
-               120 CALL                     2
-               130 STORE_NAME              17 (LibreNV)
-               132 LOAD_CONST               5 (None)
-               134 RETURN_VALUE
+                52 LOAD_CONST               4 (('Renderer', 'init'))
+                54 IMPORT_NAME              9 (sdl2.ext)
+                56 IMPORT_FROM             10 (Renderer)
+                58 STORE_NAME              10 (Renderer)
+                60 IMPORT_FROM             11 (init)
+                62 STORE_NAME              11 (init)
+                64 POP_TOP
+   
+     5          66 LOAD_CONST               0 (0)
+                68 LOAD_CONST               5 (('*',))
+                70 IMPORT_NAME             12 (sdl2)
+                72 IMPORT_STAR
+   
+     6          74 LOAD_CONST               0 (0)
+                76 LOAD_CONST               6 (None)
+                78 IMPORT_NAME             13 (ctypes)
+                80 STORE_NAME              13 (ctypes)
+   
+     7          82 LOAD_CONST               0 (0)
+                84 LOAD_CONST               6 (None)
+                86 IMPORT_NAME             14 (time)
+                88 STORE_NAME              14 (time)
+   
+     8          90 LOAD_CONST               0 (0)
+                92 LOAD_CONST               6 (None)
+                94 IMPORT_NAME             15 (os)
+                96 STORE_NAME              15 (os)
+   
+    10          98 LOAD_CONST               7 (1)
+               100 LOAD_CONST               8 (('Drawable',))
+               102 IMPORT_NAME             16 (api.drawable)
+               104 IMPORT_FROM             17 (Drawable)
+               106 STORE_NAME              17 (Drawable)
+               108 POP_TOP
+   
+    11         110 LOAD_CONST               7 (1)
+               112 LOAD_CONST               9 (('Project',))
+               114 IMPORT_NAME             18 (project)
+               116 IMPORT_FROM             19 (Project)
+               118 STORE_NAME              19 (Project)
+               120 POP_TOP
+   
+    13         122 PUSH_NULL
+               124 LOAD_BUILD_CLASS
+               126 LOAD_CONST              10 (<code object LibreNV, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 13>)
+               128 MAKE_FUNCTION            0
+               130 LOAD_CONST              11 ('LibreNV')
+               132 PRECALL                  2
+               136 CALL                     2
+               146 STORE_NAME              20 (LibreNV)
+               148 LOAD_CONST               6 (None)
+               150 RETURN_VALUE
    consts
       0
       ('Thread',)
       ('IMG_INIT_JPG', 'IMG_INIT_PNG', 'IMG_INIT_WEBP', 'IMG_Init')
-      ('fill',)
+      ('TTF_Init',)
+      ('Renderer', 'init')
       ('*',)
       None
       1
+      ('Drawable',)
       ('Project',)
-      ('Sprite',)
       code
          argcount  : 0
          nlocals   : 0
-         stacksize : 1
+         stacksize : 2
          flags     : 0
          code
-            0x970065005a0164005a02640184005a03640284005a04640384005a0564
-            0484005a06640584005a07640684005a08640784005a0964085300
-          12           0 RESUME                   0
+            0x970065005a0164005a02640184005a03640284005a0464036505660264
+            0484045a06640a640684045a07640a640784045a08640a640884045a0964
+            03650a6602640984045a0b64055300
+          13           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('LibreNV')
                        8 STORE_NAME               2 (__qualname__)
          
-          14          10 LOAD_CONST               1 (<code object __init__, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 14>)
+          15          10 LOAD_CONST               1 (<code object __init__, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 15>)
                       12 MAKE_FUNCTION            0
                       14 STORE_NAME               3 (__init__)
          
-          27          16 LOAD_CONST               2 (<code object load_game, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 27>)
+          31          16 LOAD_CONST               2 (<code object load_game, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 31>)
                       18 MAKE_FUNCTION            0
                       20 STORE_NAME               4 (load_game)
          
-          37          22 LOAD_CONST               3 (<code object get_drawables, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 37>)
-                      24 MAKE_FUNCTION            0
-                      26 STORE_NAME               5 (get_drawables)
+          41          22 LOAD_CONST               3 ('return')
+                      24 LOAD_NAME                5 (list)
+                      26 BUILD_TUPLE              2
+                      28 LOAD_CONST               4 (<code object get_drawables, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 41>)
+                      30 MAKE_FUNCTION            4 (annotations)
+                      32 STORE_NAME               6 (get_drawables)
          
-          40          28 LOAD_CONST               4 (<code object draw_background, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 40>)
-                      30 MAKE_FUNCTION            0
-                      32 STORE_NAME               6 (draw_background)
+          44          34 LOAD_CONST              10 (('return', None))
+                      36 LOAD_CONST               6 (<code object draw_background, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 44>)
+                      38 MAKE_FUNCTION            4 (annotations)
+                      40 STORE_NAME               7 (draw_background)
          
-          43          34 LOAD_CONST               5 (<code object draw, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 43>)
-                      36 MAKE_FUNCTION            0
-                      38 STORE_NAME               7 (draw)
+          47          42 LOAD_CONST              10 (('return', None))
+                      44 LOAD_CONST               7 (<code object draw, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 47>)
+                      46 MAKE_FUNCTION            4 (annotations)
+                      48 STORE_NAME               8 (draw)
          
-          53          40 LOAD_CONST               6 (<code object check_events, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 53>)
-                      42 MAKE_FUNCTION            0
-                      44 STORE_NAME               8 (check_events)
+          56          50 LOAD_CONST              10 (('return', None))
+                      52 LOAD_CONST               8 (<code object check_events, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 56>)
+                      54 MAKE_FUNCTION            4 (annotations)
+                      56 STORE_NAME               9 (check_events)
          
-          60          46 LOAD_CONST               7 (<code object loop, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 60>)
-                      48 MAKE_FUNCTION            0
-                      50 STORE_NAME               9 (loop)
-                      52 LOAD_CONST               8 (None)
-                      54 RETURN_VALUE
+          63          58 LOAD_CONST               3 ('return')
+                      60 LOAD_NAME               10 (int)
+                      62 BUILD_TUPLE              2
+                      64 LOAD_CONST               9 (<code object loop, file "build/bdist.linux-x86_64/egg/librenv/librenv.py", line 63>)
+                      66 MAKE_FUNCTION            4 (annotations)
+                      68 STORE_NAME              11 (loop)
+                      70 LOAD_CONST               5 (None)
+                      72 RETURN_VALUE
          consts
             'LibreNV'
             code
                argcount  : 1
                nlocals   : 1
                stacksize : 8
                flags     : 3
                code
-                  0x9700740100000000000000000000740200000000000000000000a60100
-                  00ab01000000000000000001007405000000000000000000007406000000
-                  000000000000007408000000000000000000007a070000740a0000000000
-                  00000000007a070000a6010000ab0100000000000000000100740d000000
-                  000000000000006401740e00000000000000000000740e00000000000000
-                  00000064026403741000000000000000000000a6060000ab060000000000
-                  0000007c005f0900000000000000007415000000000000000000007c006a
-                  090000000000000000a6010000ab0100000000000000007c005f0b000000
-                  000000000064047c005f0c000000000000000064007c005f0d0000000000
-                  00000064005300
-                14           0 RESUME                   0
-               
-                16           2 LOAD_GLOBAL              1 (NULL + SDL_Init)
-                            14 LOAD_GLOBAL              2 (SDL_INIT_EVERYTHING)
-                            26 PRECALL                  1
-                            30 CALL                     1
-                            40 POP_TOP
+                  0x9700740100000000000000000000a6000000ab00000000000000000001
+                  00740300000000000000000000740400000000000000000000a6010000ab
+                  010000000000000000010074070000000000000000000074080000000000
+                  0000000000740a000000000000000000007a070000740c00000000000000
+                  0000007a070000a6010000ab0100000000000000000100740f0000000000
+                  0000000000a6000000ab0000000000000000000100741100000000000000
+                  000000640174120000000000000000000074120000000000000000000064
+                  026403741400000000000000000000a6060000ab0600000000000000007c
+                  005f0b00000000000000007419000000000000000000007c006a0b000000
+                  0000000000a6010000ab0100000000000000007c005f0d00000000000000
+                  00741d000000000000000000007c006a0d0000000000000000a6010000ab
+                  0100000000000000007c005f0f000000000000000064047c005f10000000
+                  000000000064007c005f11000000000000000064005300
+                15           0 RESUME                   0
                
-                17          42 LOAD_GLOBAL              5 (NULL + IMG_Init)
-                            54 LOAD_GLOBAL              6 (IMG_INIT_JPG)
-                            66 LOAD_GLOBAL              8 (IMG_INIT_PNG)
-                            78 BINARY_OP                7 (|)
-                            82 LOAD_GLOBAL             10 (IMG_INIT_WEBP)
-                            94 BINARY_OP                7 (|)
-                            98 PRECALL                  1
-                           102 CALL                     1
-                           112 POP_TOP
-               
-                20         114 LOAD_GLOBAL             13 (NULL + SDL_CreateWindow)
-                           126 LOAD_CONST               1 (b'LibreNV')
-               
-                21         128 LOAD_GLOBAL             14 (SDL_WINDOWPOS_CENTERED)
-                           140 LOAD_GLOBAL             14 (SDL_WINDOWPOS_CENTERED)
-               
-                22         152 LOAD_CONST               2 (800)
-                           154 LOAD_CONST               3 (600)
-                           156 LOAD_GLOBAL             16 (SDL_WINDOW_SHOWN)
-               
-                20         168 PRECALL                  6
-                           172 CALL                     6
-                           182 LOAD_FAST                0 (self)
-                           184 STORE_ATTR               9 (window)
-               
-                23         194 LOAD_GLOBAL             21 (NULL + SDL_GetWindowSurface)
-                           206 LOAD_FAST                0 (self)
-                           208 LOAD_ATTR                9 (window)
-                           218 PRECALL                  1
-                           222 CALL                     1
-                           232 LOAD_FAST                0 (self)
-                           234 STORE_ATTR              11 (windowsurface)
-               
-                24         244 LOAD_CONST               4 (True)
-                           246 LOAD_FAST                0 (self)
-                           248 STORE_ATTR              12 (running)
-               
-                25         258 LOAD_CONST               0 (None)
-                           260 LOAD_FAST                0 (self)
-                           262 STORE_ATTR              13 (thread)
-                           272 LOAD_CONST               0 (None)
-                           274 RETURN_VALUE
+                17           2 LOAD_GLOBAL              1 (NULL + init)
+                            14 PRECALL                  0
+                            18 CALL                     0
+                            28 POP_TOP
+               
+                18          30 LOAD_GLOBAL              3 (NULL + SDL_Init)
+                            42 LOAD_GLOBAL              4 (SDL_INIT_EVERYTHING)
+                            54 PRECALL                  1
+                            58 CALL                     1
+                            68 POP_TOP
+               
+                19          70 LOAD_GLOBAL              7 (NULL + IMG_Init)
+                            82 LOAD_GLOBAL              8 (IMG_INIT_JPG)
+                            94 LOAD_GLOBAL             10 (IMG_INIT_PNG)
+                           106 BINARY_OP                7 (|)
+                           110 LOAD_GLOBAL             12 (IMG_INIT_WEBP)
+                           122 BINARY_OP                7 (|)
+                           126 PRECALL                  1
+                           130 CALL                     1
+                           140 POP_TOP
+               
+                20         142 LOAD_GLOBAL             15 (NULL + TTF_Init)
+                           154 PRECALL                  0
+                           158 CALL                     0
+                           168 POP_TOP
+               
+                23         170 LOAD_GLOBAL             17 (NULL + SDL_CreateWindow)
+                           182 LOAD_CONST               1 (b'LibreNV')
+               
+                24         184 LOAD_GLOBAL             18 (SDL_WINDOWPOS_CENTERED)
+                           196 LOAD_GLOBAL             18 (SDL_WINDOWPOS_CENTERED)
+               
+                25         208 LOAD_CONST               2 (800)
+                           210 LOAD_CONST               3 (600)
+                           212 LOAD_GLOBAL             20 (SDL_WINDOW_SHOWN)
+               
+                23         224 PRECALL                  6
+                           228 CALL                     6
+                           238 LOAD_FAST                0 (self)
+                           240 STORE_ATTR              11 (window)
+               
+                26         250 LOAD_GLOBAL             25 (NULL + SDL_GetWindowSurface)
+                           262 LOAD_FAST                0 (self)
+                           264 LOAD_ATTR               11 (window)
+                           274 PRECALL                  1
+                           278 CALL                     1
+                           288 LOAD_FAST                0 (self)
+                           290 STORE_ATTR              13 (windowsurface)
+               
+                27         300 LOAD_GLOBAL             29 (NULL + Renderer)
+                           312 LOAD_FAST                0 (self)
+                           314 LOAD_ATTR               13 (windowsurface)
+                           324 PRECALL                  1
+                           328 CALL                     1
+                           338 LOAD_FAST                0 (self)
+                           340 STORE_ATTR              15 (renderer)
+               
+                28         350 LOAD_CONST               4 (True)
+                           352 LOAD_FAST                0 (self)
+                           354 STORE_ATTR              16 (running)
+               
+                29         364 LOAD_CONST               0 (None)
+                           366 LOAD_FAST                0 (self)
+                           368 STORE_ATTR              17 (thread)
+                           378 LOAD_CONST               0 (None)
+                           380 RETURN_VALUE
                consts
                   None
                   b'LibreNV'
                   800
                   600
                   True
-               names      ('SDL_Init', 'SDL_INIT_EVERYTHING', 'IMG_Init', 'IMG_INIT_JPG', 'IMG_INIT_PNG', 'IMG_INIT_WEBP', 'SDL_CreateWindow', 'SDL_WINDOWPOS_CENTERED', 'SDL_WINDOW_SHOWN', 'window', 'SDL_GetWindowSurface', 'windowsurface', 'running', 'thread')
+               names      ('init', 'SDL_Init', 'SDL_INIT_EVERYTHING', 'IMG_Init', 'IMG_INIT_JPG', 'IMG_INIT_PNG', 'IMG_INIT_WEBP', 'TTF_Init', 'SDL_CreateWindow', 'SDL_WINDOWPOS_CENTERED', 'SDL_WINDOW_SHOWN', 'window', 'SDL_GetWindowSurface', 'windowsurface', 'Renderer', 'renderer', 'running', 'thread')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       '__init__'
-               firstlineno 14
-               lnotab 0x0202280148030e01180110fe1a0332010e01
+               firstlineno 15
+               lnotab 0x02021c01280148011c030e01180110fe1a03320132010e01
             code
                argcount  : 2
                nlocals   : 4
                stacksize : 7
                flags     : 3
                code
                   0x97007c0164017a0000007d027400000000000000000000006a01000000
@@ -235,72 +277,72 @@
                   007c036a0900000000000000006403a6020000ab020000000000000000a6
                   020000ab02000000000000000001007415000000000000000000007c036a
                   0b0000000000000000ac04a6010000ab0100000000000000007c005f0c00
                   000000000000007c006a0c0000000000000000a00d000000000000000000
                   0000000000000000000000a6000000ab00000000000000000001007c00a0
                   0e0000000000000000000000000000000000000000a6000000ab00000000
                   00000000005300
-                27           0 RESUME                   0
+                31           0 RESUME                   0
                
-                28           2 LOAD_FAST                1 (game_path)
+                32           2 LOAD_FAST                1 (game_path)
                              4 LOAD_CONST               1 ('/project.json')
                              6 BINARY_OP                0 (+)
                             10 STORE_FAST               2 (project_path)
                
-                29          12 LOAD_GLOBAL              0 (os)
+                33          12 LOAD_GLOBAL              0 (os)
                             24 LOAD_ATTR                1 (path)
                             34 LOAD_METHOD              2 (exists)
                             56 LOAD_FAST                2 (project_path)
                             58 PRECALL                  1
                             62 CALL                     1
                             72 POP_JUMP_FORWARD_IF_TRUE    15 (to 104)
                
-                30          74 LOAD_GLOBAL              7 (NULL + print)
+                34          74 LOAD_GLOBAL              7 (NULL + print)
                             86 LOAD_CONST               2 ('project.json not found!')
                             88 PRECALL                  1
                             92 CALL                     1
                            102 RETURN_VALUE
                
-                31     >>  104 LOAD_GLOBAL              9 (NULL + Project)
+                35     >>  104 LOAD_GLOBAL              9 (NULL + Project)
                            116 LOAD_ATTR                5 (from_file)
                            126 LOAD_FAST                2 (project_path)
                            128 PRECALL                  1
                            132 CALL                     1
                            142 STORE_FAST               3 (project)
                
-                32         144 LOAD_GLOBAL             13 (NULL + SDL_SetWindowTitle)
+                36         144 LOAD_GLOBAL             13 (NULL + SDL_SetWindowTitle)
                            156 LOAD_FAST                0 (self)
                            158 LOAD_ATTR                7 (window)
                            168 LOAD_GLOBAL             17 (NULL + bytes)
                            180 LOAD_FAST                3 (project)
                            182 LOAD_ATTR                9 (name)
                            192 LOAD_CONST               3 ('utf-8')
                            194 PRECALL                  2
                            198 CALL                     2
                            208 PRECALL                  2
                            212 CALL                     2
                            222 POP_TOP
                
-                33         224 LOAD_GLOBAL             21 (NULL + Thread)
+                37         224 LOAD_GLOBAL             21 (NULL + Thread)
                            236 LOAD_FAST                3 (project)
                            238 LOAD_ATTR               11 (run)
                            248 KW_NAMES                 4
                            250 PRECALL                  1
                            254 CALL                     1
                            264 LOAD_FAST                0 (self)
                            266 STORE_ATTR              12 (thread)
                
-                34         276 LOAD_FAST                0 (self)
+                38         276 LOAD_FAST                0 (self)
                            278 LOAD_ATTR               12 (thread)
                            288 LOAD_METHOD             13 (start)
                            310 PRECALL                  0
                            314 CALL                     0
                            324 POP_TOP
                
-                35         326 LOAD_FAST                0 (self)
+                39         326 LOAD_FAST                0 (self)
                            328 LOAD_METHOD             14 (loop)
                            350 PRECALL                  0
                            354 CALL                     0
                            364 RETURN_VALUE
                consts
                   None
                   '/project.json'
@@ -309,194 +351,197 @@
                   ('target',)
                names      ('os', 'path', 'exists', 'print', 'Project', 'from_file', 'SDL_SetWindowTitle', 'window', 'bytes', 'name', 'Thread', 'run', 'thread', 'start', 'loop')
                varnames   ('self', 'game_path', 'project_path', 'project')
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'load_game'
-               firstlineno 27
+               firstlineno 31
                lnotab 0x02010a013e011e012801500134013201
+            'return'
             code
                argcount  : 1
                nlocals   : 1
                stacksize : 1
                flags     : 3
                code 0x97007400000000000000000000006a0100000000000000005300
-                37           0 RESUME                   0
+                41           0 RESUME                   0
                
-                38           2 LOAD_GLOBAL              0 (Sprite)
-                            14 LOAD_ATTR                1 (SPRITES)
+                42           2 LOAD_GLOBAL              0 (Drawable)
+                            14 LOAD_ATTR                1 (DRAWABLES)
                             24 RETURN_VALUE
                consts
                   None
-               names      ('Sprite', 'SPRITES')
+               names      ('Drawable', 'DRAWABLES')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'get_drawables'
-               firstlineno 37
+               firstlineno 41
                lnotab 0x0201
+            None
             code
                argcount  : 1
                nlocals   : 1
-               stacksize : 4
+               stacksize : 7
                flags     : 3
                code
-                  0x97007401000000000000000000007c006a0100000000000000006401a6
-                  020000ab020000000000000000010064005300
-                40           0 RESUME                   0
-               
-                41           2 LOAD_GLOBAL              1 (NULL + fill)
-                            14 LOAD_FAST                0 (self)
-                            16 LOAD_ATTR                1 (windowsurface)
-                            26 LOAD_CONST               1 (0)
-                            28 PRECALL                  2
-                            32 CALL                     2
-                            42 POP_TOP
-                            44 LOAD_CONST               0 (None)
-                            46 RETURN_VALUE
+                  0x97007c006a000000000000000000a00100000000000000000000000000
+                  00000000000000740500000000000000000000640164016401a6030000ab
+                  030000000000000000a6010000ab010000000000000000010064005300
+                44           0 RESUME                   0
+               
+                45           2 LOAD_FAST                0 (self)
+                             4 LOAD_ATTR                0 (renderer)
+                            14 LOAD_METHOD              1 (clear)
+                            36 LOAD_GLOBAL              5 (NULL + SDL_Color)
+                            48 LOAD_CONST               1 (0)
+                            50 LOAD_CONST               1 (0)
+                            52 LOAD_CONST               1 (0)
+                            54 PRECALL                  3
+                            58 CALL                     3
+                            68 PRECALL                  1
+                            72 CALL                     1
+                            82 POP_TOP
+                            84 LOAD_CONST               0 (None)
+                            86 RETURN_VALUE
                consts
                   None
                   0
-               names      ('fill', 'windowsurface')
+               names      ('renderer', 'clear', 'SDL_Color')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'draw_background'
-               firstlineno 40
+               firstlineno 44
                lnotab 0x0201
             code
                argcount  : 1
                nlocals   : 3
-               stacksize : 10
+               stacksize : 5
                flags     : 3
                code
                   0x97007c00a0000000000000000000000000000000000000000000a60000
                   00ab00000000000000000001007c00a00100000000000000000000000000
-                  00000000000000a6000000ab0000000000000000007d017c0144005d487d
-                  027c026a02000000000000000072018c0a7407000000000000000000007c
-                  026a04000000000000000064007c006a050000000000000000740d000000
-                  000000000000007c026a0700000000000000006a0800000000000000007c
-                  026a0700000000000000006a090000000000000000a6020000ab02000000
-                  0000000000a6040000ab04000000000000000001008c4974150000000000
-                  00000000007c006a0b0000000000000000a6010000ab0100000000000000
-                  00010064005300
-                43           0 RESUME                   0
+                  00000000000000a6000000ab0000000000000000007d017c0144005d2a7d
+                  027c026a02000000000000000072018c0a7c02a003000000000000000000
+                  00000000000000000000007c006a0400000000000000007c006a05000000
+                  0000000000a6020000ab02000000000000000001008c2b7c006a04000000
+                  0000000000a0060000000000000000000000000000000000000000a60000
+                  00ab0000000000000000000100740f000000000000000000007c006a0800
+                  00000000000000a6010000ab010000000000000000010064005300
+                47           0 RESUME                   0
                
-                44           2 LOAD_FAST                0 (self)
+                48           2 LOAD_FAST                0 (self)
                              4 LOAD_METHOD              0 (draw_background)
                             26 PRECALL                  0
                             30 CALL                     0
                             40 POP_TOP
                
-                45          42 LOAD_FAST                0 (self)
+                49          42 LOAD_FAST                0 (self)
                             44 LOAD_METHOD              1 (get_drawables)
                             66 PRECALL                  0
                             70 CALL                     0
                             80 STORE_FAST               1 (drawables)
                
-                46          82 LOAD_FAST                1 (drawables)
+                50          82 LOAD_FAST                1 (drawables)
                             84 GET_ITER
-                       >>   86 FOR_ITER                72 (to 232)
+                       >>   86 FOR_ITER                42 (to 172)
                             88 STORE_FAST               2 (drawable)
                
-                47          90 LOAD_FAST                2 (drawable)
+                51          90 LOAD_FAST                2 (drawable)
                             92 LOAD_ATTR                2 (is_hidden)
                            102 POP_JUMP_FORWARD_IF_FALSE     1 (to 106)
                            104 JUMP_BACKWARD           10 (to 86)
                
-                48     >>  106 LOAD_GLOBAL              7 (NULL + SDL_BlitSurface)
-                           118 LOAD_FAST                2 (drawable)
-                           120 LOAD_ATTR                4 (image)
-                           130 LOAD_CONST               0 (None)
-                           132 LOAD_FAST                0 (self)
-                           134 LOAD_ATTR                5 (windowsurface)
-               
-                49         144 LOAD_GLOBAL             13 (NULL + SDL_Rect)
-                           156 LOAD_FAST                2 (drawable)
-                           158 LOAD_ATTR                7 (position)
-                           168 LOAD_ATTR                8 (x)
-                           178 LOAD_FAST                2 (drawable)
-                           180 LOAD_ATTR                7 (position)
-                           190 LOAD_ATTR                9 (y)
-                           200 PRECALL                  2
-                           204 CALL                     2
-               
-                48         214 PRECALL                  4
-                           218 CALL                     4
-                           228 POP_TOP
-                           230 JUMP_BACKWARD           73 (to 86)
-               
-                51     >>  232 LOAD_GLOBAL             21 (NULL + SDL_UpdateWindowSurface)
-                           244 LOAD_FAST                0 (self)
-                           246 LOAD_ATTR               11 (window)
-                           256 PRECALL                  1
-                           260 CALL                     1
-                           270 POP_TOP
-                           272 LOAD_CONST               0 (None)
-                           274 RETURN_VALUE
+                52     >>  106 LOAD_FAST                2 (drawable)
+                           108 LOAD_METHOD              3 (_draw)
+                           130 LOAD_FAST                0 (self)
+                           132 LOAD_ATTR                4 (renderer)
+                           142 LOAD_FAST                0 (self)
+                           144 LOAD_ATTR                5 (windowsurface)
+                           154 PRECALL                  2
+                           158 CALL                     2
+                           168 POP_TOP
+                           170 JUMP_BACKWARD           43 (to 86)
+               
+                53     >>  172 LOAD_FAST                0 (self)
+                           174 LOAD_ATTR                4 (renderer)
+                           184 LOAD_METHOD              6 (present)
+                           206 PRECALL                  0
+                           210 CALL                     0
+                           220 POP_TOP
+               
+                54         222 LOAD_GLOBAL             15 (NULL + SDL_UpdateWindowSurface)
+                           234 LOAD_FAST                0 (self)
+                           236 LOAD_ATTR                8 (window)
+                           246 PRECALL                  1
+                           250 CALL                     1
+                           260 POP_TOP
+                           262 LOAD_CONST               0 (None)
+                           264 RETURN_VALUE
                consts
                   None
-               names      ('draw_background', 'get_drawables', 'is_hidden', 'SDL_BlitSurface', 'image', 'windowsurface', 'SDL_Rect', 'position', 'x', 'y', 'SDL_UpdateWindowSurface', 'window')
+               names      ('draw_background', 'get_drawables', 'is_hidden', '_draw', 'renderer', 'windowsurface', 'present', 'SDL_UpdateWindowSurface', 'window')
                varnames   ('self', 'drawables', 'drawable')
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'draw'
-               firstlineno 43
-               lnotab 0x02012801280108011001260146ff1203
+               firstlineno 47
+               lnotab 0x0201280128010801100142013201
             code
                argcount  : 1
                nlocals   : 2
                stacksize : 5
                flags     : 3
                code
                   0x9700740100000000000000000000a6000000ab0000000000000000007d
                   017403000000000000000000007405000000000000000000006a03000000
                   00000000007c01a6010000ab010000000000000000a6010000ab01000000
                   000000000064016b030000000072407c016a040000000000000000740a00
                   0000000000000000006b0200000000720964027c005f0600000000000000
                   00640053007403000000000000000000007405000000000000000000006a
                   0300000000000000007c01a6010000ab010000000000000000a6010000ab
                   01000000000000000064016b0300000000b03e6400530064005300
-                53           0 RESUME                   0
+                56           0 RESUME                   0
                
-                54           2 LOAD_GLOBAL              1 (NULL + SDL_Event)
+                57           2 LOAD_GLOBAL              1 (NULL + SDL_Event)
                             14 PRECALL                  0
                             18 CALL                     0
                             28 STORE_FAST               1 (event)
                
-                55          30 LOAD_GLOBAL              3 (NULL + SDL_PollEvent)
+                58          30 LOAD_GLOBAL              3 (NULL + SDL_PollEvent)
                             42 LOAD_GLOBAL              5 (NULL + ctypes)
                             54 LOAD_ATTR                3 (byref)
                             64 LOAD_FAST                1 (event)
                             66 PRECALL                  1
                             70 CALL                     1
                             80 PRECALL                  1
                             84 CALL                     1
                             94 LOAD_CONST               1 (0)
                             96 COMPARE_OP               3 (!=)
                            102 POP_JUMP_FORWARD_IF_FALSE    64 (to 232)
                
-                56     >>  104 LOAD_FAST                1 (event)
+                59     >>  104 LOAD_FAST                1 (event)
                            106 LOAD_ATTR                4 (type)
                            116 LOAD_GLOBAL             10 (SDL_QUIT)
                            128 COMPARE_OP               2 (==)
                            134 POP_JUMP_FORWARD_IF_FALSE     9 (to 154)
                
-                57         136 LOAD_CONST               2 (False)
+                60         136 LOAD_CONST               2 (False)
                            138 LOAD_FAST                0 (self)
                            140 STORE_ATTR               6 (running)
                
-                58         150 LOAD_CONST               0 (None)
+                61         150 LOAD_CONST               0 (None)
                            152 RETURN_VALUE
                
-                55     >>  154 LOAD_GLOBAL              3 (NULL + SDL_PollEvent)
+                58     >>  154 LOAD_GLOBAL              3 (NULL + SDL_PollEvent)
                            166 LOAD_GLOBAL              5 (NULL + ctypes)
                            178 LOAD_ATTR                3 (byref)
                            188 LOAD_FAST                1 (event)
                            190 PRECALL                  1
                            194 CALL                     1
                            204 PRECALL                  1
                            208 CALL                     1
@@ -513,15 +558,15 @@
                   False
                names      ('SDL_Event', 'SDL_PollEvent', 'ctypes', 'byref', 'type', 'SDL_QUIT', 'running')
                varnames   ('self', 'event')
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'check_events'
-               firstlineno 53
+               firstlineno 56
                lnotab 0x02011c014a0120010e0104fd
             code
                argcount  : 1
                nlocals   : 1
                stacksize : 3
                flags     : 3
                code
@@ -529,80 +574,80 @@
                   0000000000000000000000a6000000ab00000000000000000001007c00a0
                   020000000000000000000000000000000000000000a6000000ab00000000
                   000000000001007407000000000000000000006a04000000000000000064
                   01a6010000ab01000000000000000001007c006a000000000000000000b0
                   43740b000000000000000000007c006a060000000000000000a6010000ab
                   0100000000000000000100740f00000000000000000000a6000000ab0000
                   00000000000000010064025300
-                60           0 RESUME                   0
+                63           0 RESUME                   0
                
-                61           2 LOAD_FAST                0 (self)
+                64           2 LOAD_FAST                0 (self)
                              4 LOAD_ATTR                0 (running)
                             14 POP_JUMP_FORWARD_IF_FALSE    67 (to 150)
                
-                62     >>   16 LOAD_FAST                0 (self)
+                65     >>   16 LOAD_FAST                0 (self)
                             18 LOAD_METHOD              1 (check_events)
                             40 PRECALL                  0
                             44 CALL                     0
                             54 POP_TOP
                
-                63          56 LOAD_FAST                0 (self)
+                66          56 LOAD_FAST                0 (self)
                             58 LOAD_METHOD              2 (draw)
                             80 PRECALL                  0
                             84 CALL                     0
                             94 POP_TOP
                
-                64          96 LOAD_GLOBAL              7 (NULL + time)
+                67          96 LOAD_GLOBAL              7 (NULL + time)
                            108 LOAD_ATTR                4 (sleep)
                            118 LOAD_CONST               1 (0.016)
                            120 PRECALL                  1
                            124 CALL                     1
                            134 POP_TOP
                
-                61         136 LOAD_FAST                0 (self)
+                64         136 LOAD_FAST                0 (self)
                            138 LOAD_ATTR                0 (running)
                            148 POP_JUMP_BACKWARD_IF_TRUE    67 (to 16)
                
-                66     >>  150 LOAD_GLOBAL             11 (NULL + SDL_DestroyWindow)
+                69     >>  150 LOAD_GLOBAL             11 (NULL + SDL_DestroyWindow)
                            162 LOAD_FAST                0 (self)
                            164 LOAD_ATTR                6 (window)
                            174 PRECALL                  1
                            178 CALL                     1
                            188 POP_TOP
                
-                67         190 LOAD_GLOBAL             15 (NULL + SDL_Quit)
+                70         190 LOAD_GLOBAL             15 (NULL + SDL_Quit)
                            202 PRECALL                  0
                            206 CALL                     0
                            216 POP_TOP
                
-                68         218 LOAD_CONST               2 (0)
+                71         218 LOAD_CONST               2 (0)
                            220 RETURN_VALUE
                consts
                   None
                   0.016
                   0
                names      ('running', 'check_events', 'draw', 'time', 'sleep', 'SDL_DestroyWindow', 'window', 'SDL_Quit')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
                name       'loop'
-               firstlineno 60
+               firstlineno 63
                lnotab 0x02010e012801280128fd0e0528011c01
-            None
-         names      ('__name__', '__module__', '__qualname__', '__init__', 'load_game', 'get_drawables', 'draw_background', 'draw', 'check_events', 'loop')
+            ('return', None)
+         names      ('__name__', '__module__', '__qualname__', '__init__', 'load_game', 'list', 'get_drawables', 'draw_background', 'draw', 'check_events', 'int', 'loop')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
          name       'LibreNV'
-         firstlineno 12
-         lnotab 0x0a02060d060a06030603060a0607
+         firstlineno 13
+         lnotab 0x0a020610060a0c03080308090807
       'LibreNV'
-   names      ('threading', 'Thread', 'sdl2.sdlimage', 'IMG_INIT_JPG', 'IMG_INIT_PNG', 'IMG_INIT_WEBP', 'IMG_Init', 'sdl2.ext', 'fill', 'sdl2', 'ctypes', 'time', 'os', 'project', 'Project', 'api.sprite', 'Sprite', 'LibreNV')
+   names      ('threading', 'Thread', 'sdl2.sdlimage', 'IMG_INIT_JPG', 'IMG_INIT_PNG', 'IMG_INIT_WEBP', 'IMG_Init', 'sdl2.sdlttf', 'TTF_Init', 'sdl2.ext', 'Renderer', 'init', 'sdl2', 'ctypes', 'time', 'os', 'api.drawable', 'Drawable', 'project', 'Project', 'LibreNV')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   'build/bdist.linux-x86_64/egg/librenv/librenv.py'
    name       '<module>'
    firstlineno 1
-   lnotab 0x00ff02010c0118010c0108010801080108020c010c02
+   lnotab 0x00ff02010c0118010c01100108010801080108020c010c02
```

## librenv/api/__init__.py

```diff
@@ -1,4 +1,6 @@
+from .drawable import Drawable
 from .vector2 import Vector2
 from .color import Color
 from .sprite import Sprite
+from .text import Text
```

## librenv/api/sprite.py

```diff
@@ -1,22 +1,18 @@
+from sdl2.ext import Texture
 from sdl2.sdlimage import IMG_Load
 from sdl2 import *
 
+from .drawable import Drawable
 from .vector2 import Vector2
 
-class Sprite:
-
-    SPRITES = list()
+class Sprite(Drawable):
 
     def __init__(self, image_path: str="", position: Vector2=Vector2()) -> None:
         self.image      = IMG_Load(bytes(image_path, 'utf-8'))
         self.position   = position
-        self.is_hidden  = False
-        Sprite.SPRITES.append(self)
-
-    def show(self) -> None:
-        self.is_hidden = False
-
-    def hide(self) -> None:
-        self.is_hidden = True
+        super().__init__(self)
 
+    def _draw(self, renderer, _):
+        texture = Texture(renderer, self.image)
+        renderer.copy(texture, dstrect=(self.position.x, self.position.y))
```

## librenv/api/__pycache__/__init__.cpython-311.pyc

### Python bytecode

```diff
@@ -1,49 +1,66 @@
 magic:    0xa70d0d0a
-moddate:  0x00435f64 (Sat May 13 07:57:52 2023 UTC)
-files sz: 82
+moddate:  0xa4685f64 (Sat May 13 10:38:28 2023 UTC)
+files sz: 136
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
       0x9700640064016c006d015a010100640064026c026d035a030100640064
-      036c046d055a05010064045300
+      036c046d055a050100640064046c066d075a070100640064056c086d095a
+      09010064065300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (1)
-                 4 LOAD_CONST               1 (('Vector2',))
-                 6 IMPORT_NAME              0 (vector2)
-                 8 IMPORT_FROM              1 (Vector2)
-                10 STORE_NAME               1 (Vector2)
+                 4 LOAD_CONST               1 (('Drawable',))
+                 6 IMPORT_NAME              0 (drawable)
+                 8 IMPORT_FROM              1 (Drawable)
+                10 STORE_NAME               1 (Drawable)
                 12 POP_TOP
    
      2          14 LOAD_CONST               0 (1)
-                16 LOAD_CONST               2 (('Color',))
-                18 IMPORT_NAME              2 (color)
-                20 IMPORT_FROM              3 (Color)
-                22 STORE_NAME               3 (Color)
+                16 LOAD_CONST               2 (('Vector2',))
+                18 IMPORT_NAME              2 (vector2)
+                20 IMPORT_FROM              3 (Vector2)
+                22 STORE_NAME               3 (Vector2)
                 24 POP_TOP
    
      3          26 LOAD_CONST               0 (1)
-                28 LOAD_CONST               3 (('Sprite',))
-                30 IMPORT_NAME              4 (sprite)
-                32 IMPORT_FROM              5 (Sprite)
-                34 STORE_NAME               5 (Sprite)
+                28 LOAD_CONST               3 (('Color',))
+                30 IMPORT_NAME              4 (color)
+                32 IMPORT_FROM              5 (Color)
+                34 STORE_NAME               5 (Color)
                 36 POP_TOP
-                38 LOAD_CONST               4 (None)
-                40 RETURN_VALUE
+   
+     4          38 LOAD_CONST               0 (1)
+                40 LOAD_CONST               4 (('Sprite',))
+                42 IMPORT_NAME              6 (sprite)
+                44 IMPORT_FROM              7 (Sprite)
+                46 STORE_NAME               7 (Sprite)
+                48 POP_TOP
+   
+     5          50 LOAD_CONST               0 (1)
+                52 LOAD_CONST               5 (('Text',))
+                54 IMPORT_NAME              8 (text)
+                56 IMPORT_FROM              9 (Text)
+                58 STORE_NAME               9 (Text)
+                60 POP_TOP
+                62 LOAD_CONST               6 (None)
+                64 RETURN_VALUE
    consts
       1
+      ('Drawable',)
       ('Vector2',)
       ('Color',)
       ('Sprite',)
+      ('Text',)
       None
-   names      ('vector2', 'Vector2', 'color', 'Color', 'sprite', 'Sprite')
+   names      ('drawable', 'Drawable', 'vector2', 'Vector2', 'color', 'Color', 'sprite', 'Sprite', 'text', 'Text')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   'build/bdist.linux-x86_64/egg/librenv/api/__init__.py'
    name       '<module>'
    firstlineno 1
-   lnotab 0x00ff02010c010c01
+   lnotab 0x00ff02010c010c010c010c01
```

## librenv/api/__pycache__/sprite.cpython-311.pyc

### Python bytecode

```diff
@@ -1,227 +1,235 @@
 magic:    0xa70d0d0a
-moddate:  0x7c5a5f64 (Sat May 13 09:38:04 2023 UTC)
-files sz: 490
+moddate:  0xaf775f64 (Sat May 13 11:42:39 2023 UTC)
+files sz: 539
 code
    argcount  : 0
    nlocals   : 0
-   stacksize : 4
+   stacksize : 5
    flags     : 0
    code
-      0x9700640064016c006d015a010100640064026c025400640364046c036d
-      045a04010002004700640584006406a6020000ab0200000000000000005a
-      0564075300
+      0x9700640064016c006d015a010100640064026c026d035a030100640064
+      036c045400640464056c056d065a060100640464066c076d085a08010002
+      0047006407840064086506a6030000ab0300000000000000005a09640953
+      00
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
-                 4 LOAD_CONST               1 (('IMG_Load',))
-                 6 IMPORT_NAME              0 (sdl2.sdlimage)
-                 8 IMPORT_FROM              1 (IMG_Load)
-                10 STORE_NAME               1 (IMG_Load)
+                 4 LOAD_CONST               1 (('Texture',))
+                 6 IMPORT_NAME              0 (sdl2.ext)
+                 8 IMPORT_FROM              1 (Texture)
+                10 STORE_NAME               1 (Texture)
                 12 POP_TOP
    
      2          14 LOAD_CONST               0 (0)
-                16 LOAD_CONST               2 (('*',))
-                18 IMPORT_NAME              2 (sdl2)
-                20 IMPORT_STAR
-   
-     4          22 LOAD_CONST               3 (1)
-                24 LOAD_CONST               4 (('Vector2',))
-                26 IMPORT_NAME              3 (vector2)
-                28 IMPORT_FROM              4 (Vector2)
-                30 STORE_NAME               4 (Vector2)
-                32 POP_TOP
-   
-     6          34 PUSH_NULL
-                36 LOAD_BUILD_CLASS
-                38 LOAD_CONST               5 (<code object Sprite, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 6>)
-                40 MAKE_FUNCTION            0
-                42 LOAD_CONST               6 ('Sprite')
-                44 PRECALL                  2
-                48 CALL                     2
-                58 STORE_NAME               5 (Sprite)
-                60 LOAD_CONST               7 (None)
-                62 RETURN_VALUE
+                16 LOAD_CONST               2 (('IMG_Load',))
+                18 IMPORT_NAME              2 (sdl2.sdlimage)
+                20 IMPORT_FROM              3 (IMG_Load)
+                22 STORE_NAME               3 (IMG_Load)
+                24 POP_TOP
+   
+     3          26 LOAD_CONST               0 (0)
+                28 LOAD_CONST               3 (('*',))
+                30 IMPORT_NAME              4 (sdl2)
+                32 IMPORT_STAR
+   
+     5          34 LOAD_CONST               4 (1)
+                36 LOAD_CONST               5 (('Drawable',))
+                38 IMPORT_NAME              5 (drawable)
+                40 IMPORT_FROM              6 (Drawable)
+                42 STORE_NAME               6 (Drawable)
+                44 POP_TOP
+   
+     6          46 LOAD_CONST               4 (1)
+                48 LOAD_CONST               6 (('Vector2',))
+                50 IMPORT_NAME              7 (vector2)
+                52 IMPORT_FROM              8 (Vector2)
+                54 STORE_NAME               8 (Vector2)
+                56 POP_TOP
+   
+     8          58 PUSH_NULL
+                60 LOAD_BUILD_CLASS
+                62 LOAD_CONST               7 (<code object Sprite, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 8>)
+                64 MAKE_FUNCTION            0
+                66 LOAD_CONST               8 ('Sprite')
+                68 LOAD_NAME                6 (Drawable)
+                70 PRECALL                  3
+                74 CALL                     3
+                84 STORE_NAME               9 (Sprite)
+                86 LOAD_CONST               9 (None)
+                88 RETURN_VALUE
    consts
       0
+      ('Texture',)
       ('IMG_Load',)
       ('*',)
       1
+      ('Drawable',)
       ('Vector2',)
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 7
          flags     : 0
          code
-            0x970065005a0164005a0202006503a6000000ab0000000000000000005a
-            04640102006505a6000000ab000000000000000000660264026506640365
-            05640464056606640684055a076409640784045a086409640884045a0964
-            055300
-           6           0 RESUME                   0
-                       2 LOAD_NAME                0 (__name__)
-                       4 STORE_NAME               1 (__module__)
-                       6 LOAD_CONST               0 ('Sprite')
-                       8 STORE_NAME               2 (__qualname__)
-         
-           8          10 PUSH_NULL
-                      12 LOAD_NAME                3 (list)
-                      14 PRECALL                  0
-                      18 CALL                     0
-                      28 STORE_NAME               4 (SPRITES)
+            0x8700970065005a0164005a02640102006503a6000000ab000000000000
+            00000066026402650464036503640464056606880066016406840d5a0564
+            0784005a06880078015a075300
+                       0 MAKE_CELL                0 (__class__)
          
-          10          30 LOAD_CONST               1 ('')
-                      32 PUSH_NULL
-                      34 LOAD_NAME                5 (Vector2)
-                      36 PRECALL                  0
-                      40 CALL                     0
-                      50 BUILD_TUPLE              2
-                      52 LOAD_CONST               2 ('image_path')
-                      54 LOAD_NAME                6 (str)
-                      56 LOAD_CONST               3 ('position')
-                      58 LOAD_NAME                5 (Vector2)
-                      60 LOAD_CONST               4 ('return')
-                      62 LOAD_CONST               5 (None)
-                      64 BUILD_TUPLE              6
-                      66 LOAD_CONST               6 (<code object __init__, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 10>)
-                      68 MAKE_FUNCTION            5 (defaults, annotations)
-                      70 STORE_NAME               7 (__init__)
+           8           2 RESUME                   0
+                       4 LOAD_NAME                0 (__name__)
+                       6 STORE_NAME               1 (__module__)
+                       8 LOAD_CONST               0 ('Sprite')
+                      10 STORE_NAME               2 (__qualname__)
          
-          16          72 LOAD_CONST               9 (('return', None))
-                      74 LOAD_CONST               7 (<code object show, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 16>)
-                      76 MAKE_FUNCTION            4 (annotations)
-                      78 STORE_NAME               8 (show)
+          10          12 LOAD_CONST               1 ('')
+                      14 PUSH_NULL
+                      16 LOAD_NAME                3 (Vector2)
+                      18 PRECALL                  0
+                      22 CALL                     0
+                      32 BUILD_TUPLE              2
+                      34 LOAD_CONST               2 ('image_path')
+                      36 LOAD_NAME                4 (str)
+                      38 LOAD_CONST               3 ('position')
+                      40 LOAD_NAME                3 (Vector2)
+                      42 LOAD_CONST               4 ('return')
+                      44 LOAD_CONST               5 (None)
+                      46 BUILD_TUPLE              6
+                      48 LOAD_CLOSURE             0 (__class__)
+                      50 BUILD_TUPLE              1
+                      52 LOAD_CONST               6 (<code object __init__, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 10>)
+                      54 MAKE_FUNCTION           13 (defaults, annotations, closure)
+                      56 STORE_NAME               5 (__init__)
          
-          19          80 LOAD_CONST               9 (('return', None))
-                      82 LOAD_CONST               8 (<code object hide, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 19>)
-                      84 MAKE_FUNCTION            4 (annotations)
-                      86 STORE_NAME               9 (hide)
-                      88 LOAD_CONST               5 (None)
-                      90 RETURN_VALUE
+          15          58 LOAD_CONST               7 (<code object _draw, file "build/bdist.linux-x86_64/egg/librenv/api/sprite.py", line 15>)
+                      60 MAKE_FUNCTION            0
+                      62 STORE_NAME               6 (_draw)
+                      64 LOAD_CLOSURE             0 (__class__)
+                      66 COPY                     1
+                      68 STORE_NAME               7 (__classcell__)
+                      70 RETURN_VALUE
          consts
             'Sprite'
             ''
             'image_path'
             'position'
             'return'
             None
             code
                argcount  : 3
                nlocals   : 3
                stacksize : 6
                flags     : 3
                code
-                  0x97007401000000000000000000007403000000000000000000007c0164
-                  01a6020000ab020000000000000000a6010000ab0100000000000000007c
-                  005f0200000000000000007c027c005f03000000000000000064027c005f
-                  040000000000000000740a000000000000000000006a0600000000000000
-                  00a00700000000000000000000000000000000000000007c00a6010000ab
-                  010000000000000000010064005300
-                10           0 RESUME                   0
-               
-                11           2 LOAD_GLOBAL              1 (NULL + IMG_Load)
-                            14 LOAD_GLOBAL              3 (NULL + bytes)
-                            26 LOAD_FAST                1 (image_path)
-                            28 LOAD_CONST               1 ('utf-8')
-                            30 PRECALL                  2
-                            34 CALL                     2
-                            44 PRECALL                  1
-                            48 CALL                     1
-                            58 LOAD_FAST                0 (self)
-                            60 STORE_ATTR               2 (image)
-               
-                12          70 LOAD_FAST                2 (position)
-                            72 LOAD_FAST                0 (self)
-                            74 STORE_ATTR               3 (position)
-               
-                13          84 LOAD_CONST               2 (False)
-                            86 LOAD_FAST                0 (self)
-                            88 STORE_ATTR               4 (is_hidden)
-               
-                14          98 LOAD_GLOBAL             10 (Sprite)
-                           110 LOAD_ATTR                6 (SPRITES)
-                           120 LOAD_METHOD              7 (append)
-                           142 LOAD_FAST                0 (self)
-                           144 PRECALL                  1
-                           148 CALL                     1
-                           158 POP_TOP
-                           160 LOAD_CONST               0 (None)
-                           162 RETURN_VALUE
+                  0x950197007401000000000000000000007403000000000000000000007c
+                  016401a6020000ab020000000000000000a6010000ab0100000000000000
+                  007c005f0200000000000000007c027c005f030000000000000000740900
+                  000000000000000000a6000000ab000000000000000000a0050000000000
+                  0000000000000000000000000000007c00a6010000ab0100000000000000
+                  00010064005300
+                             0 COPY_FREE_VARS           1
+               
+                10           2 RESUME                   0
+               
+                11           4 LOAD_GLOBAL              1 (NULL + IMG_Load)
+                            16 LOAD_GLOBAL              3 (NULL + bytes)
+                            28 LOAD_FAST                1 (image_path)
+                            30 LOAD_CONST               1 ('utf-8')
+                            32 PRECALL                  2
+                            36 CALL                     2
+                            46 PRECALL                  1
+                            50 CALL                     1
+                            60 LOAD_FAST                0 (self)
+                            62 STORE_ATTR               2 (image)
+               
+                12          72 LOAD_FAST                2 (position)
+                            74 LOAD_FAST                0 (self)
+                            76 STORE_ATTR               3 (position)
+               
+                13          86 LOAD_GLOBAL              9 (NULL + super)
+                            98 PRECALL                  0
+                           102 CALL                     0
+                           112 LOAD_METHOD              5 (__init__)
+                           134 LOAD_FAST                0 (self)
+                           136 PRECALL                  1
+                           140 CALL                     1
+                           150 POP_TOP
+                           152 LOAD_CONST               0 (None)
+                           154 RETURN_VALUE
                consts
                   None
                   'utf-8'
-                  False
-               names      ('IMG_Load', 'bytes', 'image', 'position', 'is_hidden', 'Sprite', 'SPRITES', 'append')
+               names      ('IMG_Load', 'bytes', 'image', 'position', 'super', '__init__')
                varnames   ('self', 'image_path', 'position')
-               freevars   ()
+               freevars   ('__class__',)
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/api/sprite.py'
                name       '__init__'
                firstlineno 10
-               lnotab 0x020144010e010e01
+               lnotab 0x040144010e01
             code
-               argcount  : 1
-               nlocals   : 1
-               stacksize : 2
-               flags     : 3
-               code 0x970064017c005f00000000000000000064005300
-                16           0 RESUME                   0
-               
-                17           2 LOAD_CONST               1 (False)
-                             4 LOAD_FAST                0 (self)
-                             6 STORE_ATTR               0 (is_hidden)
-                            16 LOAD_CONST               0 (None)
-                            18 RETURN_VALUE
-               consts
-                  None
-                  False
-               names      ('is_hidden',)
-               varnames   ('self',)
-               freevars   ()
-               cellvars   ()
-               filename   'build/bdist.linux-x86_64/egg/librenv/api/sprite.py'
-               name       'show'
-               firstlineno 16
-               lnotab 0x0201
-            code
-               argcount  : 1
-               nlocals   : 1
-               stacksize : 2
+               argcount  : 3
+               nlocals   : 4
+               stacksize : 5
                flags     : 3
-               code 0x970064017c005f00000000000000000064005300
-                19           0 RESUME                   0
-               
-                20           2 LOAD_CONST               1 (True)
-                             4 LOAD_FAST                0 (self)
-                             6 STORE_ATTR               0 (is_hidden)
-                            16 LOAD_CONST               0 (None)
-                            18 RETURN_VALUE
+               code
+                  0x97007401000000000000000000007c017c006a010000000000000000a6
+                  020000ab0200000000000000007d037c01a0020000000000000000000000
+                  0000000000000000007c037c006a0300000000000000006a040000000000
+                  0000007c006a0300000000000000006a0500000000000000006602ac01a6
+                  020000ab020000000000000000010064005300
+                15           0 RESUME                   0
+               
+                16           2 LOAD_GLOBAL              1 (NULL + Texture)
+                            14 LOAD_FAST                1 (renderer)
+                            16 LOAD_FAST                0 (self)
+                            18 LOAD_ATTR                1 (image)
+                            28 PRECALL                  2
+                            32 CALL                     2
+                            42 STORE_FAST               3 (texture)
+               
+                17          44 LOAD_FAST                1 (renderer)
+                            46 LOAD_METHOD              2 (copy)
+                            68 LOAD_FAST                3 (texture)
+                            70 LOAD_FAST                0 (self)
+                            72 LOAD_ATTR                3 (position)
+                            82 LOAD_ATTR                4 (x)
+                            92 LOAD_FAST                0 (self)
+                            94 LOAD_ATTR                3 (position)
+                           104 LOAD_ATTR                5 (y)
+                           114 BUILD_TUPLE              2
+                           116 KW_NAMES                 1
+                           118 PRECALL                  2
+                           122 CALL                     2
+                           132 POP_TOP
+                           134 LOAD_CONST               0 (None)
+                           136 RETURN_VALUE
                consts
                   None
-                  True
-               names      ('is_hidden',)
-               varnames   ('self',)
+                  ('dstrect',)
+               names      ('Texture', 'image', 'copy', 'position', 'x', 'y')
+               varnames   ('self', 'renderer', '_', 'texture')
                freevars   ()
                cellvars   ()
                filename   'build/bdist.linux-x86_64/egg/librenv/api/sprite.py'
-               name       'hide'
-               firstlineno 19
-               lnotab 0x0201
-            ('return', None)
-         names      ('__name__', '__module__', '__qualname__', 'list', 'SPRITES', 'Vector2', 'str', '__init__', 'show', 'hide')
+               name       '_draw'
+               firstlineno 15
+               lnotab 0x02012a01
+         names      ('__name__', '__module__', '__qualname__', 'Vector2', 'str', '__init__', '_draw', '__classcell__')
          varnames   ()
          freevars   ()
-         cellvars   ()
+         cellvars   ('__class__',)
          filename   'build/bdist.linux-x86_64/egg/librenv/api/sprite.py'
          name       'Sprite'
-         firstlineno 6
-         lnotab 0x0a0214022a060803
+         firstlineno 8
+         lnotab 0x0c022e05
       'Sprite'
       None
-   names      ('sdl2.sdlimage', 'IMG_Load', 'sdl2', 'vector2', 'Vector2', 'Sprite')
+   names      ('sdl2.ext', 'Texture', 'sdl2.sdlimage', 'IMG_Load', 'sdl2', 'drawable', 'Drawable', 'vector2', 'Vector2', 'Sprite')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   'build/bdist.linux-x86_64/egg/librenv/api/sprite.py'
    name       '<module>'
    firstlineno 1
-   lnotab 0x00ff02010c0108020c02
+   lnotab 0x00ff02010c010c0108020c010c02
```

