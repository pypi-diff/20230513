# Comparing `tmp/pymininec-0.3.0.tar.gz` & `tmp/pymininec-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymininec-0.3.0.tar", last modified: Tue Aug  9 08:33:08 2022, max compression
+gzip compressed data, was "pymininec-0.4.0.tar", last modified: Sat May 13 11:10:19 2023, max compression
```

## Comparing `pymininec-0.3.0.tar` & `pymininec-0.4.0.tar`

### file list

```diff
@@ -1,20 +1,18 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-08-09 08:33:08.001932 pymininec-0.3.0/
--rw-r--r--   0 ralf      (1000) priv      (1011)    24539 2022-08-09 08:33:07.997932 pymininec-0.3.0/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)    20735 2022-08-09 08:26:53.000000 pymininec-0.3.0/README.rst
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-08-09 08:33:07.961932 pymininec-0.3.0/mininec/
--rw-r--r--   0 ralf      (1000) priv      (1011)       16 2022-08-09 08:32:01.000000 pymininec-0.3.0/mininec/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2022-07-18 18:56:28.000000 pymininec-0.3.0/mininec/__init__.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)   136911 2022-08-06 18:44:21.000000 pymininec-0.3.0/mininec/mininec.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    22470 2022-08-06 18:44:21.000000 pymininec-0.3.0/mininec/plot_antenna.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-08-09 08:33:07.985932 pymininec-0.3.0/pymininec.egg-info/
--rw-r--r--   0 ralf      (1000) priv      (1011)    24539 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)      340 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/SOURCES.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        1 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/dependency_links.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       93 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/entry_points.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       23 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/requires.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        8 2022-08-09 08:33:07.000000 pymininec-0.3.0/pymininec.egg-info/top_level.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       38 2022-08-09 08:33:08.001932 pymininec-0.3.0/setup.cfg
--rw-r--r--   0 ralf      (1000) priv      (1011)     2893 2022-07-23 06:49:59.000000 pymininec-0.3.0/setup.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-08-09 08:33:07.993932 pymininec-0.3.0/test/
--rw-r--r--   0 ralf      (1000) priv      (1011)    27119 2022-08-06 18:44:21.000000 pymininec-0.3.0/test/test_mininec.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     7220 2022-07-23 06:50:00.000000 pymininec-0.3.0/test/test_plot.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 11:10:19.981212 pymininec-0.4.0/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    24708 2023-05-13 11:10:19.977212 pymininec-0.4.0/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)    20856 2023-05-13 11:05:34.000000 pymininec-0.4.0/README.rst
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 11:10:19.933212 pymininec-0.4.0/mininec/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       16 2023-05-13 11:09:22.000000 pymininec-0.4.0/mininec/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2022-07-18 18:56:28.000000 pymininec-0.4.0/mininec/__init__.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)   140072 2023-05-13 10:41:36.000000 pymininec-0.4.0/mininec/mininec.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 11:10:19.965212 pymininec-0.4.0/pymininec.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    24708 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      298 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       52 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       23 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/requires.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        8 2023-05-13 11:10:19.000000 pymininec-0.4.0/pymininec.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-05-13 11:10:19.981212 pymininec-0.4.0/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2838 2022-09-13 14:25:55.000000 pymininec-0.4.0/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-05-13 11:10:19.969212 pymininec-0.4.0/test/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    28959 2023-05-13 10:42:27.000000 pymininec-0.4.0/test/test_mininec.py
```

### Comparing `pymininec-0.3.0/PKG-INFO` & `pymininec-0.4.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pymininec
-Version: 0.3.0
+Version: 0.4.0
 Summary: Python version of the original MININEC Antenna Optimization code
 Home-page: https://github.com/schlatterbeck/pymininec
 Author: Ralf Schlatterbeck
 Author-email: rsc@runtux.com
 License: MIT License
 Description: MININEC in Python
         =================
@@ -15,14 +15,16 @@
         .. |__| unicode:: U+2013   .. en dash without spaces
             :trim:
         .. |_| unicode:: U+00A0 .. Non-breaking space
             :trim:
         .. |-| unicode:: U+202F .. Thin non-breaking space
             :trim:
         .. |numpy.linalg.solve| replace:: ``numpy.linalg.solve``
+        .. |scipy.integrate| replace:: ``scipy.integrate``
+        .. |scipy.special.ellipk| replace:: ``scipy.special.ellipk``
         
         This is an attempt to rewrite the original MININEC3 basic sources in
         Python. Standard use-case like computation of feed impedance and far
         field are implemented and are quite well tested. There is only a command
         line interface.
         
         An example of using the command-line interface uses the following
@@ -61,66 +63,38 @@
         the format of the original Basic implementation of Mininec.
         
         Plotting
         --------
         
         The output tables produced by ``pymininec``
         are not very useful to get an idea of the far field behaviour of
-        an antenna. Therefore there is a small companion program ``plot-antenna``
-        that can plot the antenna pattern. The default is to plot all available
-        graphics, including an interactive 3d view. In addition with the
-        ``--azimuth`` or ``--elevation`` options you can get an Azimuth
-        diagram::
-        
-            plot-antenna --azimuth test/12-el-1deg.pout
-        
-        .. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-azimuth.png
-            :align: center
-        
-        or an elevation diagram::
-        
-            plot-antenna --elevation test/12-el-1deg.pout
-        
-        .. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-elevation.png
-            :align: center
-        
-        respectively. Note that I used an output file with 1-degree resolution
-        in elevation and azimuth angles not with 5 degrees as in the example
-        above. The pattern look smoother but a 3D-view will be very slow due to
-        the large number of points. The plot program also has a ``--help``
-        option for further information. In particular the scaling of the antenna
-        plot can be ``linear``, ``linear_db``, and ``linear_voltage`` in
-        addition to the default of ``arrl`` scaling. You may consult Cebik's [6]_
-        article for explanation of the different diagrams.
-        
-        The latest version accepts several plot parameters, ``--elevation``,
-        ``--azimuth``, ``--plot3d``, ``--plot-vswr`` which are plotted into one
-        diagram. The default is to plot all four graphs. With the ``--output``
-        option pictures can directly be saved without displaying the graphics on
-        the screen.
-        
-        The plot program can also display output files of ``nec2c``, not only
-        from ``pymininec``.
-        
-        The latest version has key-bindings for scrolling through the
-        frequencies of an antenna simulation. So if you have an output file with
-        a simulation of multiple frequencies (either with ``pymininec`` or
-        ``nec2c``) you can display diagrams for the next frequency by typing
-        ``+``, and to the previous frequency by typing ``-``. For newer versions
-        of ``matplotlib`` you can display a scrollbar for the frequencies with
-        the ``--with-slider`` option.
-        
-        Other keybindings switch the scaling for the antenna plots, ``a``
-        switches to ``arrl`` scaling, ``l`` switches to linear scaling, ``d``
-        switches to linear dB scaling, and ``v`` switches to linear voltage
-        scaling.
-        
-        Finally the ``w`` option toggles display of the 3d diagram from/to
-        wireframe display. Note that the wireframe display may not be supported
-        on all versions of ``matplotlib`` and/or graphics cards.
+        an antenna. The companion program `plot-antenna`_ used to be bundled
+        with ``pymininec`` but was moved to its own project. You can currently
+        plot elevation and azimuth diagram of an antenna, a 3D-plot, the
+        geometry and VSWR. All either as a standalone program (using matplotlib)
+        or exported as HTML to the browser (using plotly).
+        
+        Ground (Media)
+        --------------
+        
+        The latest version implements the option parsing for the mininec ground
+        model for more than one medium. You also need to specify the
+        ``--boundary`` option to set the type of boundary between media: The
+        default ``linear`` boundary appends grounds in X-direction with the
+        distance in the 4th parameter of the ``--medium`` option. The
+        ``circular`` boundary has concentric media with the radius of each
+        medium given in the 4th parameter of the ``--medium`` option. The third
+        parameter of the ``--medium`` option is the height. Note that you
+        typically want *negative* heights for media further out, this allows
+        modelling of summits. Mininec *allows* the specification of *higher*
+        grounds but the results will be questionable as no reflection at the
+        higher ground is modelled. The ground implementation was not yet tested
+        against the originally basic code (or any other modelling program
+        implementing the mininec engine).
+        
         
         Test coverage: Making sure it is consistent with original Mininec
         -----------------------------------------------------------------
         
         There are several tests against the `original Basic source code`_, for
         the test cases see the subdirectory ``test``. One of the test cases is
         a simple 7MHz wire dipole with half the wavelength and 10 segments.
@@ -212,21 +186,22 @@
         on my PC (this has 264 segments, more than the original Mininec ever
         supported) when I'm using 5 degree increments for theta and phi angles
         and about 11 minutes (!) for 1 degree angles. The reason is that
         everything currently is implemented (like in Basic) as nested loops.
         This could (and should) be changed to use vector and matrix operations
         in `numpy`_. In the inner loop of the matrix fill operation there are
         several integrals computed using `gaussian quadrature`_ or a numeric
-        solution to an `elliptic integral`_. These could be implemented by
-        scipy_ library functions.
+        solution to an `elliptic integral`_. These are now implemented using
+        methods (or at least constants in the case of `gaussian quadrature`_)
+        from |scipy.integrate|_ and |scipy.special.ellipk|_.
         
         Notes on Elliptic Integral Parameters
         -------------------------------------
         
-        The Mininec code uses the implementation of an elliptic integral when
+        The Mininec code uses the implementation of an `elliptic integral`_ when
         computing the impedance matrix and in several other places. The integral
         uses a set of E-vector coefficients that are cited differently in
         different places. In the latest version of the open source Basic code
         these parameters are in lines 1510 |__| 1512. They are also
         reprinted in the publication [2]_ about that version of Mininec which
         has a listing of the Basic source code (slightly different from the
         version available online) where it is on p. |-| C-31 in lines
@@ -265,28 +240,28 @@
         but notice how in the *b* parameters (2nd line) the current Basic code
         has one more *3* in the second column. The rounding of the earlier Basic
         code suggests that the second *3* is a typo in the later Basic version.
         Also notice that in the 4th column the later Basic code has a *5* less
         than the version in the papers. The rounding in the earlier Basic code
         also suggests that the later Basic code is in error.
         
-        The errors in the elliptic integral parameters do not have much effect
+        The errors in the `elliptic integral`_ parameters do not have much effect
         on the computed values of the Mininec code. There are some minor
         differences but these are below the differences between Basic and Python
         implementation (single vs. double precision arithmetics). I had hoped
         that this has something to do with the well known fact that Mininec
         finds a resonance point of an antenna some percent too high which means
         that usually in practice the computed wire lengths are a little too
         long. This is apparently not the case. The resonance point is also wrong
         for very thin wires below the *small radius modification condition*
         which happens when the wire radius is below 1e-4 of the wavelength.
-        Even in that case --  where the elliptic integral is not used -- the
+        Even in that case --  where the `elliptic integral`_ is not used -- the
         resonance is slightly wrong.
         
-        The reference for the elliptic integral parameters [3]_ cited in both
+        The reference for the `elliptic integral`_ parameters [3]_ cited in both
         reports lists the following table on p. |-| 591:
         
         +---------------+--------------+--------------+--------------+--------------+
         | 1.38629436112 | .09666344259 | .03590092383 | .03742563713 | .01451196212 |
         +---------------+--------------+--------------+--------------+--------------+
         |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
         +---------------+--------------+--------------+--------------+--------------+
@@ -310,14 +285,20 @@
         +---------------+--------------+--------------+--------------+--------------+
         |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
         +---------------+--------------+--------------+--------------+--------------+
         
         So apparently the handbook [3]_ is correct. And the Basic version and
         *both* Mininec reports have at least one typo.
         
+        Since this paragraph was written the implementation of the `elliptic
+        integral`_ was removed and replace with a call to |scipy.special.ellipk|_.
+        The resulting differences in computed outputs were smaller than the
+        differences between the Basic (single precision) and the Python (double
+        precision) implementation.
+        
         Running examples in Basic
         -------------------------
         
         The original Basic source code can still be run today, thanks to Rob
         Hagemans `pcbasic`_ project. It is written in Python and can be
         installed with pip. It is also packaged in some Linux distributions,
         e.g. in Debian_.
@@ -345,14 +326,35 @@
         cut&paste buffer.
         
         The `original basic source code`_ can be obtained from the `unofficial
         NEC archive`_ by PA3KJ or from a `Mininec github project`_, I'm using
         the version from the `unofficial NEC archive`_ and have not verified if
         the two links I've given contain the same code.
         
+        Release Notes
+        -------------
+        
+        v0.4.0: Split `plot-antenna`_ into own project
+        
+        - Own project `plot-antenna`_
+        - Fix parsing of several medium options, mention ground in documentation
+        
+        v0.3.0: Laplace loads correctly implemented
+        
+        - Use scipy.special.ellipk for elliptic integral
+        - Use gaussian quadrature coefficients from scipy.integrate
+        - Test resonance (NEC vs. mininec)
+        
+        v0.2.0: Add short paragraph on new plotting program
+        
+        - Test coverage
+        - Expression simplification
+        
+        v0.1.0: Initial release
+        
         .. _`original basic source code`: http://nec-archives.pa3kj.com/mininec3.zip
         .. _`unofficial NEC archive`: http://nec-archives.pa3kj.com/
         .. _`Mininec github project`: https://github.com/Kees-PA3KJ/MiniNec
         .. _`numpy`: https://numpy.org/
         .. _`pcbasic`: https://github.com/robhagemans/pcbasic
         .. _`Debian`: https://packages.debian.org/stable/python3-pcbasic
         .. _`contribution to pcbasic`: https://github.com/robhagemans/pcbasic/pull/183
@@ -386,27 +388,31 @@
             Magazine, 2003. Available with antenna models from the `Cebik
             collection`_.
         
         .. _ADA121535: https://apps.dtic.mil/sti/pdfs/ADA121535.pdf
         .. _ADA181682: https://apps.dtic.mil/sti/pdfs/ADA181682.pdf
         .. _`numpy.linalg.solve`:
             https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html
+        .. _`scipy.integrate`: https://docs.scipy.org/doc/scipy/tutorial/integrate.html
+        .. _`scipy.special.ellipk`:
+            https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.ellipk.html
         .. _`OhioLINK Electronic Theses & Dissertations Center`:
             https://etd.ohiolink.edu/apexprod/rws_etd/send_file/send?accession=ohiou1176315682
         .. _`reported this as a bug in the pytest project`:
             https://github.com/pytest-dev/pytest/issues/10152
         .. _`as a bug in python`:
             https://github.com/python/cpython/issues/94974
         .. _`Cebik collection`:
             http://on5au.be/Books/allmodnotes.zip
         .. _`Antenna modelling notes episode 48`:
             http://on5au.be/content/amod/amod48.html
         .. _`gaussian quadrature`: https://en.wikipedia.org/wiki/Gaussian_quadrature
         .. _`elliptic integral`: https://en.wikipedia.org/wiki/Elliptic_integral
         .. _`scipy`: https://scipy.org/
+        .. _`plot-antenna`: https://github.com/schlatterbeck/plot-antenna
         
 Platform: Any
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Intended Audience :: Science/Research
```

### Comparing `pymininec-0.3.0/README.rst` & `pymininec-0.4.0/README.rst`

 * *Files 6% similar despite different names*

```diff
@@ -7,14 +7,16 @@
 .. |__| unicode:: U+2013   .. en dash without spaces
     :trim:
 .. |_| unicode:: U+00A0 .. Non-breaking space
     :trim:
 .. |-| unicode:: U+202F .. Thin non-breaking space
     :trim:
 .. |numpy.linalg.solve| replace:: ``numpy.linalg.solve``
+.. |scipy.integrate| replace:: ``scipy.integrate``
+.. |scipy.special.ellipk| replace:: ``scipy.special.ellipk``
 
 This is an attempt to rewrite the original MININEC3 basic sources in
 Python. Standard use-case like computation of feed impedance and far
 field are implemented and are quite well tested. There is only a command
 line interface.
 
 An example of using the command-line interface uses the following
@@ -53,66 +55,38 @@
 the format of the original Basic implementation of Mininec.
 
 Plotting
 --------
 
 The output tables produced by ``pymininec``
 are not very useful to get an idea of the far field behaviour of
-an antenna. Therefore there is a small companion program ``plot-antenna``
-that can plot the antenna pattern. The default is to plot all available
-graphics, including an interactive 3d view. In addition with the
-``--azimuth`` or ``--elevation`` options you can get an Azimuth
-diagram::
-
-    plot-antenna --azimuth test/12-el-1deg.pout
-
-.. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-azimuth.png
-    :align: center
-
-or an elevation diagram::
-
-    plot-antenna --elevation test/12-el-1deg.pout
-
-.. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-elevation.png
-    :align: center
-
-respectively. Note that I used an output file with 1-degree resolution
-in elevation and azimuth angles not with 5 degrees as in the example
-above. The pattern look smoother but a 3D-view will be very slow due to
-the large number of points. The plot program also has a ``--help``
-option for further information. In particular the scaling of the antenna
-plot can be ``linear``, ``linear_db``, and ``linear_voltage`` in
-addition to the default of ``arrl`` scaling. You may consult Cebik's [6]_
-article for explanation of the different diagrams.
-
-The latest version accepts several plot parameters, ``--elevation``,
-``--azimuth``, ``--plot3d``, ``--plot-vswr`` which are plotted into one
-diagram. The default is to plot all four graphs. With the ``--output``
-option pictures can directly be saved without displaying the graphics on
-the screen.
-
-The plot program can also display output files of ``nec2c``, not only
-from ``pymininec``.
-
-The latest version has key-bindings for scrolling through the
-frequencies of an antenna simulation. So if you have an output file with
-a simulation of multiple frequencies (either with ``pymininec`` or
-``nec2c``) you can display diagrams for the next frequency by typing
-``+``, and to the previous frequency by typing ``-``. For newer versions
-of ``matplotlib`` you can display a scrollbar for the frequencies with
-the ``--with-slider`` option.
-
-Other keybindings switch the scaling for the antenna plots, ``a``
-switches to ``arrl`` scaling, ``l`` switches to linear scaling, ``d``
-switches to linear dB scaling, and ``v`` switches to linear voltage
-scaling.
-
-Finally the ``w`` option toggles display of the 3d diagram from/to
-wireframe display. Note that the wireframe display may not be supported
-on all versions of ``matplotlib`` and/or graphics cards.
+an antenna. The companion program `plot-antenna`_ used to be bundled
+with ``pymininec`` but was moved to its own project. You can currently
+plot elevation and azimuth diagram of an antenna, a 3D-plot, the
+geometry and VSWR. All either as a standalone program (using matplotlib)
+or exported as HTML to the browser (using plotly).
+
+Ground (Media)
+--------------
+
+The latest version implements the option parsing for the mininec ground
+model for more than one medium. You also need to specify the
+``--boundary`` option to set the type of boundary between media: The
+default ``linear`` boundary appends grounds in X-direction with the
+distance in the 4th parameter of the ``--medium`` option. The
+``circular`` boundary has concentric media with the radius of each
+medium given in the 4th parameter of the ``--medium`` option. The third
+parameter of the ``--medium`` option is the height. Note that you
+typically want *negative* heights for media further out, this allows
+modelling of summits. Mininec *allows* the specification of *higher*
+grounds but the results will be questionable as no reflection at the
+higher ground is modelled. The ground implementation was not yet tested
+against the originally basic code (or any other modelling program
+implementing the mininec engine).
+
 
 Test coverage: Making sure it is consistent with original Mininec
 -----------------------------------------------------------------
 
 There are several tests against the `original Basic source code`_, for
 the test cases see the subdirectory ``test``. One of the test cases is
 a simple 7MHz wire dipole with half the wavelength and 10 segments.
@@ -204,21 +178,22 @@
 on my PC (this has 264 segments, more than the original Mininec ever
 supported) when I'm using 5 degree increments for theta and phi angles
 and about 11 minutes (!) for 1 degree angles. The reason is that
 everything currently is implemented (like in Basic) as nested loops.
 This could (and should) be changed to use vector and matrix operations
 in `numpy`_. In the inner loop of the matrix fill operation there are
 several integrals computed using `gaussian quadrature`_ or a numeric
-solution to an `elliptic integral`_. These could be implemented by
-scipy_ library functions.
+solution to an `elliptic integral`_. These are now implemented using
+methods (or at least constants in the case of `gaussian quadrature`_)
+from |scipy.integrate|_ and |scipy.special.ellipk|_.
 
 Notes on Elliptic Integral Parameters
 -------------------------------------
 
-The Mininec code uses the implementation of an elliptic integral when
+The Mininec code uses the implementation of an `elliptic integral`_ when
 computing the impedance matrix and in several other places. The integral
 uses a set of E-vector coefficients that are cited differently in
 different places. In the latest version of the open source Basic code
 these parameters are in lines 1510 |__| 1512. They are also
 reprinted in the publication [2]_ about that version of Mininec which
 has a listing of the Basic source code (slightly different from the
 version available online) where it is on p. |-| C-31 in lines
@@ -257,28 +232,28 @@
 but notice how in the *b* parameters (2nd line) the current Basic code
 has one more *3* in the second column. The rounding of the earlier Basic
 code suggests that the second *3* is a typo in the later Basic version.
 Also notice that in the 4th column the later Basic code has a *5* less
 than the version in the papers. The rounding in the earlier Basic code
 also suggests that the later Basic code is in error.
 
-The errors in the elliptic integral parameters do not have much effect
+The errors in the `elliptic integral`_ parameters do not have much effect
 on the computed values of the Mininec code. There are some minor
 differences but these are below the differences between Basic and Python
 implementation (single vs. double precision arithmetics). I had hoped
 that this has something to do with the well known fact that Mininec
 finds a resonance point of an antenna some percent too high which means
 that usually in practice the computed wire lengths are a little too
 long. This is apparently not the case. The resonance point is also wrong
 for very thin wires below the *small radius modification condition*
 which happens when the wire radius is below 1e-4 of the wavelength.
-Even in that case --  where the elliptic integral is not used -- the
+Even in that case --  where the `elliptic integral`_ is not used -- the
 resonance is slightly wrong.
 
-The reference for the elliptic integral parameters [3]_ cited in both
+The reference for the `elliptic integral`_ parameters [3]_ cited in both
 reports lists the following table on p. |-| 591:
 
 +---------------+--------------+--------------+--------------+--------------+
 | 1.38629436112 | .09666344259 | .03590092383 | .03742563713 | .01451196212 |
 +---------------+--------------+--------------+--------------+--------------+
 |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
 +---------------+--------------+--------------+--------------+--------------+
@@ -302,14 +277,20 @@
 +---------------+--------------+--------------+--------------+--------------+
 |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
 +---------------+--------------+--------------+--------------+--------------+
 
 So apparently the handbook [3]_ is correct. And the Basic version and
 *both* Mininec reports have at least one typo.
 
+Since this paragraph was written the implementation of the `elliptic
+integral`_ was removed and replace with a call to |scipy.special.ellipk|_.
+The resulting differences in computed outputs were smaller than the
+differences between the Basic (single precision) and the Python (double
+precision) implementation.
+
 Running examples in Basic
 -------------------------
 
 The original Basic source code can still be run today, thanks to Rob
 Hagemans `pcbasic`_ project. It is written in Python and can be
 installed with pip. It is also packaged in some Linux distributions,
 e.g. in Debian_.
@@ -337,14 +318,35 @@
 cut&paste buffer.
 
 The `original basic source code`_ can be obtained from the `unofficial
 NEC archive`_ by PA3KJ or from a `Mininec github project`_, I'm using
 the version from the `unofficial NEC archive`_ and have not verified if
 the two links I've given contain the same code.
 
+Release Notes
+-------------
+
+v0.4.0: Split `plot-antenna`_ into own project
+
+- Own project `plot-antenna`_
+- Fix parsing of several medium options, mention ground in documentation
+
+v0.3.0: Laplace loads correctly implemented
+
+- Use scipy.special.ellipk for elliptic integral
+- Use gaussian quadrature coefficients from scipy.integrate
+- Test resonance (NEC vs. mininec)
+
+v0.2.0: Add short paragraph on new plotting program
+
+- Test coverage
+- Expression simplification
+
+v0.1.0: Initial release
+
 .. _`original basic source code`: http://nec-archives.pa3kj.com/mininec3.zip
 .. _`unofficial NEC archive`: http://nec-archives.pa3kj.com/
 .. _`Mininec github project`: https://github.com/Kees-PA3KJ/MiniNec
 .. _`numpy`: https://numpy.org/
 .. _`pcbasic`: https://github.com/robhagemans/pcbasic
 .. _`Debian`: https://packages.debian.org/stable/python3-pcbasic
 .. _`contribution to pcbasic`: https://github.com/robhagemans/pcbasic/pull/183
@@ -378,20 +380,24 @@
     Magazine, 2003. Available with antenna models from the `Cebik
     collection`_.
 
 .. _ADA121535: https://apps.dtic.mil/sti/pdfs/ADA121535.pdf
 .. _ADA181682: https://apps.dtic.mil/sti/pdfs/ADA181682.pdf
 .. _`numpy.linalg.solve`:
     https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html
+.. _`scipy.integrate`: https://docs.scipy.org/doc/scipy/tutorial/integrate.html
+.. _`scipy.special.ellipk`:
+    https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.ellipk.html
 .. _`OhioLINK Electronic Theses & Dissertations Center`:
     https://etd.ohiolink.edu/apexprod/rws_etd/send_file/send?accession=ohiou1176315682
 .. _`reported this as a bug in the pytest project`:
     https://github.com/pytest-dev/pytest/issues/10152
 .. _`as a bug in python`:
     https://github.com/python/cpython/issues/94974
 .. _`Cebik collection`:
     http://on5au.be/Books/allmodnotes.zip
 .. _`Antenna modelling notes episode 48`:
     http://on5au.be/content/amod/amod48.html
 .. _`gaussian quadrature`: https://en.wikipedia.org/wiki/Gaussian_quadrature
 .. _`elliptic integral`: https://en.wikipedia.org/wiki/Elliptic_integral
 .. _`scipy`: https://scipy.org/
+.. _`plot-antenna`: https://github.com/schlatterbeck/plot-antenna
```

### Comparing `pymininec-0.3.0/mininec/mininec.py` & `pymininec-0.4.0/mininec/mininec.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python3
-# Copyright (C) 2022 Ralf Schlatterbeck. All rights reserved
+# Copyright (C) 2022-23 Ralf Schlatterbeck. All rights reserved
 # Reichergasse 131, A-3411 Weidling
 # ****************************************************************************
 #
 # Permission is hereby granted, free of charge, to any person obtaining a copy
 # of this software and associated documentation files (the "Software"), to deal
 # in the Software without restriction, including without limitation the rights
 # to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
@@ -92,38 +92,72 @@
 
 class Connected_Wires:
     """ This is used to store a set of connected wires *and* the
         corresponding segments in one data structure.
     """
 
     def __init__ (self):
-        self.pulses = set ()
-        self.wires  = set ()
-        self.list   = []
+        self.wires         = set ()
+        self.list          = []
+        self.cached_pulses = None
+        self.sgn_by_wire   = {}
     # end def __init__
 
-    def add (self, wire, pulse_idx, sign):
+    @property
+    def pulses (self):
+        if self.cached_pulses is None:
+            self.cached_pulses = set (x [0] for x in self.pulse_iter ())
+        return self.cached_pulses
+    # end def pulses
+
+    def add (self, wire, other_wire, end_idx, sign, sign2):
         assert wire not in self.wires
-        assert pulse_idx not in self.pulses
-        self.pulses.add (pulse_idx)
         self.wires.add (wire)
-        self.list.append ((wire, pulse_idx, sign))
+        self.list.append ((wire, other_wire, end_idx, sign))
+        self.sgn_by_wire [other_wire] = sign2
     # end def add
 
+    def idx (self, wire):
+        """ This computes I1 or I2 from the Basic code, respectively
+        """
+        if self.list:
+            # Forward linked segments are printed as 0
+            if wire.n < self.list [0][0].n:
+                return 0
+            return (1 + self.list [0][0].n) * self.sgn_by_wire [wire]
+        return 0
+    # end def idx
+
+    def is_connected (self, other):
+        return other in self.wires
+    # end def is_connected
+
     def pulse_iter (self):
         """ Yield pulse indeces sorted by wire index
         """
-        for wire, idx, s in sorted (self.list, key = lambda x: x [0].n):
-            yield (idx, s)
+        for wire, ow, idx, s in self._iter ():
+            yield (ow.end_segs [idx], s)
     # end def pulse_iter
 
+    def _iter (self):
+        for wire, ow, idx, s in sorted (self.list, key = lambda x: x [0].n):
+            yield (wire, ow, idx, s)
+    # end def _iter
+
     def __bool__ (self):
         return bool (self.list)
     # end def __bool__
 
+    def __str__ (self):
+        r = []
+        for wire, ow, idx, s in self._iter ():
+            r.append ('w: %d idx: %d s:%d' % (wire.n, ow.end_segs [idx], s))
+        return '\n'.join (r)
+    __repr__ = __str__
+
 # end class Connected_Wires
 
 class Excitation:
     """ This is the pulse source definition in mininec.
         For convenience phase is in degrees (and converted internally)
         Magnitude is in volts, constructor can either directly give a
         complex number for the voltage *or* floating point voltage
@@ -357,72 +391,74 @@
         return u / d
     # end def impedance
 
 # end class Laplace_Load
 
 class Medium:
     """ This encapsulates the media (e.g. ground screen etc.)
-        With diel and cond zero we asume ideal ground.
+        With permittivity and conductivity zero we asume ideal ground.
         Note that it seems only the first medium can have a
-        ground screen of radials
+        ground screen of radials.
         The boundary is the type of boundary between different media (if
-        there is more than one). It is 1 for linear (X-coordinate it
-        seems) or circular. If there is more than one medium we need the
-        coordinate (distance X for linear and radius R for circular
+        there is more than one). It is either 'linear' (X-coordinate it
+        seems) or 'circular'. If there is more than one medium we need
+        the coordinate (distance X for linear and radius R for circular
         boundary) of the *next* medium, in the original code U(I).
     >>> med = Medium (3, 4)
     >>> imp = med.impedance (30)
     >>> print ('%.4f%+.4fj' % (imp.real, imp.imag))
     0.0144+0.0144j
     >>> med = Medium (0, 0)
     >>> med.impedance (7)
     0j
     """
     def __init__ \
         ( self
-        , diel, cond, height = 0
+        , permittivity, conductivity, height = 0
         , nradials = 0, radius = 0, dist = 0
-        , boundary = 1, coord = 1e6
+        , boundary = 'linear', coord = 1e6
         ):
-        self.diel     = diel     # dielectric constant T(I)
-        self.cond     = cond     # conductivity        V(I)
+        self.permittivity = permittivity  # (dielectric constant) T(I)
+        self.conductivity = conductivity  # V(I)
         self.nradials = nradials # number of radials   NR
         self.radius   = radius   # radial wire radius  RR
         self.coord    = coord    # U(I)
         self.height   = height   # H(I)
         self.boundary = boundary
         self.next     = None     # next medium
         self.prev     = None     # previous medium
         self.is_ideal = False
-        if diel == 0 and cond == 0:
+        if permittivity == 0 and conductivity == 0:
             self.is_ideal = True
             self.coord    = 0
             if self.nradials:
                 raise ValueError ("Ideal ground may not use radials")
             if self.height != 0:
                 raise ValueError ("Ideal ground must have height 0")
         if self.nradials:
-            self.boundary = 2
+            self.boundary = 'circular'
             # Radials extend to boundary of next medium
             if self.radius <= 0:
                 raise ValueError ("Radius must be >0")
         else:
             self.radius = 0.0
         # Code from Line 628-633 in far field calculation
-        if diel:
-            if not self.cond:
+        if permittivity:
+            if not self.conductivity:
                 raise ValueError \
                     ("Non-ideal ground must have non-zero ground parameters")
     # end def __init__
 
     def as_mininec (self):
         r = []
         if not self.is_ideal:
             p = tuple \
-                (x.strip () for x in format_float ((self.diel, self.cond)))
+                ( x.strip ()
+                  for x in format_float ((self.permittivity, self.conductivity))
+                )
             r.append \
                 ( ' RELATIVE DIELECTRIC CONSTANT, CONDUCTIVITY:'
                   '  %s , %s'
                 % p
                 )
         if self.nradials:
             r.append \
@@ -446,15 +482,15 @@
         return '\n'.join (r)
     # end def as_mininec
 
     def impedance (self, f):
         if self.is_ideal:
             return 0+0j
         t = 2 * np.pi * f * 8.85e-6
-        return 1 / np.sqrt (self.diel + -1j * self.cond / t)
+        return 1 / np.sqrt (self.permittivity + -1j * self.conductivity / t)
     # end def impedance
 
     def set_next (self, next):
         self.next = next
         if next is None:
             if self.nradials:
                 raise ValueError \
@@ -503,26 +539,36 @@
         if (diff == 0).all ():
             raise ValueError ("Zero length wire: %s %s" % (self.p1, self.p2))
         self.wire_len = np.linalg.norm (diff)
         self.seg_len  = self.wire_len / self.n_segments
         # Original comment: compute direction cosines
         self.dirs = diff / self.wire_len
         self.end_segs = [None, None]
-        self.j2 = [None, None]
-        self.i1 = self.i2 = 0
         # Links to previous/next connected wire (at start/end)
+        # conn [0] contains wires that link to our first end
+        # while conn [1] contains wires that link to our second end.
         self.conn = (Connected_Wires (), Connected_Wires ())
         self.n = None
         # This is Integral I1 in the paper(s), in the implementation
         # used in Basic this boils down to only wire-dependent
         # Parameters. So we can avoid re-computing this for each
         # combination of segments.
         self.i6 = (1 + np.log (16 * r / self.seg_len)) / np.pi / r
     # end def __init__
 
+    @property
+    def idx_1 (self):
+        return self.idx (0)
+    # end def idx_1
+
+    @property
+    def idx_2 (self):
+        return self.idx (1)
+    # end def idx_2
+
     def compute_ground (self, n, media):
         self.n = n
         # If we are in free space, nothing to do here
         if media is None:
             self.is_ground = (False, False)
             return
         # Wire end is grounded if Z coordinate is 0
@@ -531,35 +577,73 @@
         self.is_ground = ((self.p1 [-1] == 0), (self.p2 [-1] == 0))
         if self.is_ground [0] and self.is_ground [1]:
             raise ValueError ("Both ends of a wire may not be grounded")
         if self.p1 [-1] < 0 or self.p2 [-1] < 0:
             raise ValueError ("height cannot not be negative with ground")
     # end def compute_ground
 
-    def compute_connections (self, media):
-        """ Compute links to connected wires self.conn [0] contains
-            wires that link to our first end while conn [1] contains wires
-            that link to our second end.
+    def compute_connections (self, end_dicts):
+        """ Compute links to connected wires
             Also compute sets of indeces of pulses.
-        """
-        for n, j in enumerate (self.j2):
-            if j <= 0:
-                continue
-            if not self.is_ground [n] and j != self.n + 1:
-                other = media [j - 1]
-                self.conn [n].add (other, self.end_segs [n], 1)
-                if (other.p1 == self.endpoints [n]).all ():
-                    s = 1 if n == 1 else -1
-                    other.conn [0].add (self, self.end_segs [n], s)
-                else:
-                    assert (other.p2 == self.endpoints [n]).all ()
-                    s = 1 if n == 0 else -1
-                    other.conn [1].add (self, self.end_segs [n], s)
+            Note that we're using dictionaries for matching endpoints,
+            this reduces two nested loops over the wires which is O(N**2)
+            to a single loop O(N).
+        """
+
+        # These are two loops of two elements each. This rolls the
+        # end-matching computation of 4 explicitly-programmed cases in
+        # the Basic program lines 1325-1356 into a few statements.
+        # The idea is to use two dictionaries of end-point coordinates.
+        for n1, current_end in enumerate (self.endpoints):
+            ep_tuple = tuple (current_end)
+            for n2, other_end_dict in enumerate (end_dicts):
+                if not self.is_ground [n1] and ep_tuple in other_end_dict:
+                    other = other_end_dict [ep_tuple]
+                    s = -1 if (n2 == n1) else 1
+                    other.conn [n2].add (self,  self, n1, s, s)
+                    self.conn  [n1].add (other, self, n1, 1, s)
+            if ep_tuple not in end_dicts [n1]:
+                end_dicts [n1][ep_tuple] = self
     # end def compute_connections
 
+    def connections (self):
+        return self.conn [0].wires.union (self.conn [1].wires)
+    # end def connections
+
+    def idx (self, end_idx):
+        """ The indeces I1, I2 from the Basic code, this is -self.n when
+            the end is grounded, the index of a connected wire (negative
+            if the direction of the wire is reversed) if connected and 0
+            otherwise. Used mainly when printing wires in mininec format.
+        """
+        if self.is_ground [end_idx]:
+            return -(self.n + 1)
+        return self.conn [end_idx].idx (self)
+    # end def idx
+
+    def is_connected (self, other):
+        if other is self:
+            return True
+        for c in self.conn:
+            if c.is_connected (other):
+                return True
+        return bool (self.connections ().intersection (other.connections ()))
+    # end def is_connected
+
+    def conn_as_str (self):
+        """ Mostly for debugging connections
+        """
+        r = []
+        r.append ('W: %d' % self.n)
+        for n, c in enumerate (self.conn):
+            r.append ('conn %s:' % 'lr' [n])
+            r.append (str (c))
+        return '\n'.join (r)
+    # end def conn_as_str
+
     def segment_iter (self, yield_ends = True):
         if self.end_segs [0] is not None or self.end_segs [1] is not None:
             if self.end_segs [1] is None:
                 if yield_ends or self.end_segs [0] not in self.conn [0].pulses:
                     yield self.end_segs [0]
             elif self.end_segs [0] is None:
                 if yield_ends or self.end_segs [1] not in self.conn [1].pulses:
@@ -673,15 +757,15 @@
                  - list of Medium object otherwise
             nm:  Number of media (NM)
                  0: perfectly conducting ground
                  See class Medium above
             boundary:  Type of boundary (1: linear, 2: circular) (TB)
                  only if nm > 1
                  See class Medium above, if we have radials it's
-                 circular
+                 forced to circular
             Computed:
             w:   Wavelength in m, (W)
             s0:  virtual dipole lenght for near field calculation (S0)
             m:   ?  Comment: 1 / (4 * PI * OMEGA * EPSILON)
             srm: SMALL RADIUS MODIFICATION CONDITION
         >>> w = []
         >>> w.append (Wire (10, 0, 0, 0, 21.414285, 0, 0, 0.001))
@@ -694,24 +778,40 @@
          [1 1]
          [1 1]
          [1 1]
          [1 1]
          [1 1]
          [1 1]
          [1 1]]
+        >>> w = []
+        >>> w.append (Wire (10, 0,          0, 0, 21.414285, 0, 0, 0.001))
+        >>> w.append (Wire (10, 21.4142850, 0, 0, 33.      , 0, 0, 0.001))
+        >>> s = Excitation (1, 0)
+        >>> m = Mininec (7, w)
+        >>> print (m.geo_as_str ())
+        W: 0
+        conn l:
+        <BLANKLINE>
+        conn r:
+        w: 1 idx: 9 s:1
+        W: 1
+        conn l:
+        w: 0 idx: 9 s:1
+        conn r:
+        <BLANKLINE>
         """
         self.f          = f
         self.media      = media
         self.loads      = []
         self.check_ground ()
         self.sources    = []
         self.geo        = geo
         self.print_opts = print_opts or set (('far-field',))
         if not self.media or len (self.media) == 1:
-            self.boundary = 1
+            self.boundary = 'linear'
         self.check_geo ()
         self.compute_connectivity ()
         self.output_date = False
     # end __init__
 
     @property
     def f (self):
@@ -741,15 +841,15 @@
                 if n == 0:
                     if len (self.media) == 1:
                         m.set_next (None)
                     self.boundary = m.boundary
                 else:
                     self.media [n - 1].set_next (m)
         else:
-            self.boundary = 1
+            self.boundary = 'linear'
     # end def check_ground
 
     def check_geo (self):
         for n, wire in enumerate (self.geo):
             wire.compute_ground (n, self.media)
     # end def check_geo
 
@@ -804,79 +904,46 @@
             Then the segments are computed.
             In the original code this starts on line 1198 with the
             comment "compute connectivity data (pulses N1 to N)"
             The variable seg replaces the X, Y, Z arrays in the original
             code, it has consequently dimension 3.
             Looks like index n1 is the index of the next start segment.
             And n is the index of the next end segment.
+
+            Note that we do not use a second loop but instead put each
+            wire end into a dictionary linking to the wire. That way the
+            algorithm is O(N) not O(N^2). The dictionaries for the wire
+            ends is end_dicts, this is a list of two dictionaries, one
+            for each end.
         """
         n = 0
         self.c_per = c_per = {}
         self.w_per = w_per = {}
         self.seg   = seg   = {}
+        end_dicts  = [{}, {}]
         for i, w in enumerate (self.geo):
             # This part starts at 1298 comment "connections"
             # We do not use the E, L, M array with the X, Y, Z
             # coordinates of the start of the wires and the second half
             # with the end of the wires, we use the Wire objects
             # instead.
-            gflag = False
-            i1 = i2 = 0
-            w.j2 [:] = (-(i + 1), -(i + 1))
-            # check for ground connection
-            if self.media:
-                if w.is_ground [0]:
-                    i1   = -(i + 1)
-                if w.is_ground [1]:
-                    i2   = -(i + 1)
-                    # Why is the gflag only set for the second ground case??
-                    gflag = True
-            for j in range (i):
-                # Check start -> start
-                # Original comment: check for end1 to end1
-                if (w.p1 == self.geo [j].p1).all ():
-                    #print ("p1 p1 %d %d" % (i, j))
-                    i1 = -(j + 1)
-                    w.j2 [0] = j + 1
-                    if self.geo [j].j2 [0] == -(j + 1):
-                        self.geo [j].j2 [0] = j + 1
-                    break
-                # Check start -> end
-                # Original comment: check for end1 to end2
-                if (w.p1 == self.geo [j].p2).all ():
-                    #print ("p1 p2 %d %d" % (i, j))
-                    i1 = (j + 1)
-                    w.j2 [0] = j + 1
-                    if self.geo [j].j2 [1] == -(j + 1):
-                        self.geo [j].j2 [1] = j + 1
-                    break
-            if not gflag:
-                for j in range (i):
-                    # Check end -> end
-                    # Original comment: check end2 to end2
-                    if (w.p2 == self.geo [j].p2).all ():
-                        #print ("p2 p2 %d %d" % (i, j))
-                        i2 = -(j + 1)
-                        w.j2 [1] = j + 1
-                        if self.geo [j].j2 [1] == -(j + 1):
-                            self.geo [j].j2 [1] = j + 1
-                        break
-                    # Check end -> start
-                    # Original comment: check for end2 to end1
-                    if (w.p2 == self.geo [j].p1).all ():
-                        #print ("p2 p1 %d %d" % (i, j))
-                        i2 = (j + 1)
-                        w.j2 [1] = j + 1
-                        if self.geo [j].j2 [0] == -(j + 1):
-                            self.geo [j].j2 [0] = j + 1
-                        break
-            w.i1 = i1
-            w.i2 = i2
-            # Here we used to print the geometry, we do this separately.
 
+            # Try to match existing wire endpoints
+            w.compute_connections (end_dicts)
+
+            # i1 and i2 are the indeces of the previous/next wire.
+            # This is 0 when there is no prev/next wire. It is -n
+            # (where n is the wire.n) if the end is grounded. The index
+            # is negative if the polarity changes, i.e. when we have a
+            # connection from end1 to end1 of the other wire or end2 to
+            # end2 of the other wire.
+
+            # n is the segment index.
+            i1 = w.idx_1
+            i2 = w.idx_2
             # This part starts at 1198
             # compute connectivity data (pulses n1 to n)
             # We make end_segs 0-based and use None instead of 0
             n1 = n + 1
             self.geo [i].end_segs [0] = n1 - 1
             if w.n_segments == 1 and i1 == 0:
                 self.geo [i].end_segs [0] = None
@@ -947,16 +1014,14 @@
         self.seg_idx = copy.deepcopy (self.c_per)
         # Fill 0s with values from w_per
         for idx in range (2):
             cnull = self.c_per.T [idx] == 0
             self.seg_idx.T [idx][cnull] = self.w_per [cnull]
         # make indeces 0-based
         self.w_per   -= 1
-        for wire in self.geo:
-            wire.compute_connections (self.geo)
     # end def compute_connectivity
 
     def compute_far_field \
         (self, zenith_angle, azimuth_angle, pwr = None, dist = 0):
         """ Compute far field
             Original code starts at 620 (and is called at 621)
             The angles are instances of Angle.
@@ -1034,15 +1099,15 @@
                                 nr  = med.nradials
                                 rr  = med.radius
                                 # begin by finding specular distance
                                 t4 = 1e5
                                 if rt3.real != 0:
                                     t4 = -self.seg [j][2] * rt3.imag / rt3.real
                                 b9 = t4 * v21.real + self.seg [j][0]
-                                if self.boundary != 1:
+                                if self.boundary != 'linear':
                                     # Hmm this is pythagoras?
                                     b9 *= b9
                                     b9 += (self.seg [j][1] - t4 * v21.imag) ** 2
                                     b9 = np.sqrt (b9)
                                 # search for the corresponding medium
                                 # Find minimum index where b9 > coord
                                 coord = [m.coord for m in self.media]
@@ -1422,14 +1487,21 @@
                     f2 *= 2
                 # Weird, the imag part goes to the real Z component and
                 # vice-versa, the contribution to the real part is
                 # negated, the contribution to the imag part not
                 self.Z [j][j] += -f2 * l.impedance (self.f) * 1j
     # end def compute_impedance_matrix_loads
 
+    def geo_as_str (self):
+        r = []
+        for g in self.geo:
+            r.append (g.conn_as_str ())
+        return '\n'.join (r)
+    # end def geo_as_str
+
     def nf_helper (self, cp, j, k, v, j12, wj, f67, f45):
         v6  = np.array ([1, 1, f67 [0]])
         v7  = np.array ([1, 1, f67 [1]])
         dir = [w.dirs for w in wj]
         j3  = np.max (j12)
         # compute psi(0,J,J+.5)
         p2  = 2 * j3 + j + 1
@@ -2064,15 +2136,15 @@
             or wire.r > self.srm
             or p3 != p2 + 1
             or p1 != (p2 + p3) / 2
             ):
             i4 = int (p1)
             i5 = i4 + 1
             vec1 = (self.seg [i4] + self.seg [i5]) / 2
-            wd   = self.wires_differ (i, j)
+            wd   = self.wires_unconnected (i, j)
             vec2, vecv = self.psi_common_vec1_vecv (vec1, k, p2, p3)
             return self.psi (vec2, vecv, k, p2, p3, p4, fvs = 1, exact = not wd)
         t1 = 2 * np.log (wire.seg_len / wire.r)
         t2 = -self.w * wire.seg_len
         return t1 + t2 * 1j
     # end def scalar_potential
 
@@ -2105,34 +2177,32 @@
         >>> print ("%.7f %.7fj" % (r.real, r.imag))
         0.6747199 -0.1555773j
         """
         wire = self.geo [p4]
         if k < 1 or wire.r >= self.srm or i != j or p3 != p2 + .5:
             vec1 = self.seg [p1]
             vec2, vecv = self.psi_common_vec1_vecv (vec1, k, p2, p3)
-            wd = self.wires_differ (i, j)
+            wd = self.wires_unconnected (i, j)
             return self.psi (vec2, vecv, k, p2, p3, p4, fvs = 0, exact = not wd)
         t1 = np.log (wire.seg_len / wire.r)
         t2 = -self.w * wire.seg_len / 2
         return t1 + t2 * 1j
     # end def vector_potential
 
-    def wires_differ (self, i, j):
+    def wires_unconnected (self, i, j):
+        """ Check if the wires to which the given segment indeces belong
+            are *not* connected.
+        """
         assert self.w_per [i] >= 0
         assert self.w_per [j] >= 0
-        wire_i_j2 = self.geo [self.w_per [i]].j2
-        wire_j_j2 = self.geo [self.w_per [j]].j2
-        r = \
-            (   wire_i_j2 [0] != wire_j_j2 [0]
-            and wire_i_j2 [0] != wire_j_j2 [1]
-            and wire_i_j2 [1] != wire_j_j2 [0]
-            and wire_i_j2 [1] != wire_j_j2 [1]
-            )
-        return r
-    # end def wires_differ
+        w1 = self.geo [self.w_per [i]]
+        w2 = self.geo [self.w_per [j]]
+        # Well this should really be symmetric, so one should be enough :-)
+        return not w1.is_connected (w2) and not w2.is_connected (w1)
+    # end def wires_unconnected
 
     # All the *as_mininec methods
 
     def _options (self, options):
         if options is None:
             options = self.print_opts
         return options
@@ -2175,14 +2245,15 @@
             fmt = ''.join (['%s ' * 2] * 2)
             if not wire.is_ground [0]:
                 if not wire.conn [0]:
                     r.append ((' ' * 13).join (['E '] + ['0'] * 4))
                 else:
                     c = 0+0j
                     for p, s in wire.conn [0].pulse_iter ():
+                        assert p is not None
                         c = s * self.current [p]
                     a = np.angle (c) / np.pi * 180
                     r.append \
                         ( ('J ' + ' ' * 12 + fmt)
                         % format_float
                             ((c.real, c.imag, np.abs (c), a), use_e = True)
                         )
@@ -2196,14 +2267,15 @@
                     )
             if not wire.is_ground [1]:
                 if not wire.conn [1]:
                     r.append ((' ' * 13).join (['E '] + ['0'] * 4))
                 else:
                     c = 0+0j
                     for p, s in wire.conn [1].pulse_iter ():
+                        assert p is not None
                         c += s * self.current [p]
                     a = np.angle (c) / np.pi * 180
                     r.append \
                         ( ('J ' + ' ' * 12 + fmt)
                         % format_float
                             ((c.real, c.imag, np.abs (c), a), use_e = True)
                         )
@@ -2225,18 +2297,18 @@
             ('ENVIRONMENT (+1 FOR FREE SPACE, -1 FOR GROUND PLANE): %+d' % e)
         if self.media:
             r.append \
                 ( ' NUMBER OF MEDIA (0 FOR PERFECTLY CONDUCTING GROUND): %2d'
                 % l
                 )
             if len (self.media) > 1:
-                r.append \
-                    ( ' TYPE OF BOUNDARY (1-LINEAR, 2-CIRCULAR):  %d'
-                    % self.boundary
-                    )
+                b = 1
+                if self.boundary != 'linear':
+                    b = 2
+                r.append (' TYPE OF BOUNDARY (1-LINEAR, 2-CIRCULAR):  %d' % b)
             if l:
                 for n, m in enumerate (self.media):
                     r.append (m.as_mininec ())
         return '\n'.join (r)
     # end def environment_as_mininec
 
     def far_field_absolute_as_mininec (self):
@@ -2549,20 +2621,20 @@
                 )
             r.append \
                 ( '   X%sY%sZ%sRADIUS%sCONNECTION%sSEGMENTS'
                 % (' ' * 13, ' ' * 13, ' ' * 10, ' ' * 5, ' ' * 5)
                 )
             l = []
             l.append (('%-13s ' * 3) % format_float (wire.p1))
-            l.append ('%s%3d' % (' ' * 12, wire.i1))
+            l.append ('%s%3d' % (' ' * 12, wire.idx_1))
             r.append (''.join (l))
             l = []
             l.append (('%-13s ' * 3) % format_float (wire.p2))
             l.append ('%-13s' % format_float ([wire.r]))
-            l.append ('%2d%15d' % (wire.i2, wire.n_segments))
+            l.append ('%2d%15d' % (wire.idx_2, wire.n_segments))
             r.append (''.join (l))
             r.append ('')
         r.append (' ' * 18 + '**** ANTENNA GEOMETRY ****')
         k = 1
         j = 0
         for wire in self.geo:
             r.append ('')
@@ -2870,14 +2942,21 @@
 
     >>> args = ['-f', '7.15', '-w', '5,0,0,0,0,0,10.0838,0.0127,extra']
     >>> r = main (args, sys.stdout)
     Invalid number of parameters for wire 1
     >>> r
     23
 
+    >>> args = ['-f', '7.15', '-w', '5,0,0,0,0,0,10.0838,0.0127']
+    >>> args.extend (['--boundary', 'unknown'])
+    >>> r = main (args, sys.stdout)
+    Invalid boundary: unknown, must be one of "linear", "circular"
+    >>> r
+    23
+
     >>> args = ['-f', '7.15', '-w', '5,0,0,0,0,0,10.0838,extra']
     >>> r = main (args, sys.stdout)
     Invalid wire 1: could not convert string to float: 'extra'
     >>> r
     23
 
     >>> args = ['-f', '7.15', '-w', '5,0,0,0,0,0,10.0838,0.0127']
@@ -3060,27 +3139,34 @@
     >>> args.extend (['--excitation-segment=1'])
     >>> args.extend (['--theta=0,45,nonint', '--phi=0,180,3'])
     >>> r = main (args, sys.stdout)
     Invalid theta angle, need float, float, int
     >>> r
     23
     """
+    boundaries = ('linear', 'circular')
     from argparse import ArgumentParser
     cmd = ArgumentParser ()
     cmd.add_argument \
         ( '--attach-load'
         , help    = 'Attach load with given index to pulse, needs '
                     'load-index, pulse-index, optional wire index. If '
                     'wire index is given, pulse index is relative to '
                     'wire. To attach a load to all pulses use "all" for '
                     'the pulse index (and leave the wire index blank).'
         , action  = 'append'
         , default = []
         )
     cmd.add_argument \
+        ( '--boundary'
+        , help    = 'Boundary between different media, one of %s'
+                  % ','.join ('"%s"' % b for b in boundaries)
+        , default = 'linear'
+        )
+    cmd.add_argument \
         (  '--excitation-segment'
         , help    = "Segment number for excitation, can be specified "
                     "more than once, default is the single segment 5"
         , type    = int
         , action  = 'append'
         , default = []
         , 
@@ -3142,20 +3228,23 @@
         , help    = 'Complex load'
         , action  = 'append'
         , default = []
         )
     cmd.add_argument \
         ( '--medium'
         , help    = "Media (ground), free space if not given, "
-                    "specify dielectricum, condition, height, if all are "
+                    "specify permittivity (dielectric constant), "
+                    "conductivity, height, if all are "
                     "zero, ideal ground is asumed, if radials are "
                     "specified they apply to the first ground (which "
                     "cannot be ideal with radials), several media can be "
                     "specified. If more than one medium is given, the "
-                    "circular or linear coordinate of medium must be given."
+                    "circular or linear coordinate of medium must be "
+                    "given as the fourth parameter, this is the distance "
+                    "to the next medium."
         , action  = 'append'
         , default = []
         )
     cmd.add_argument \
         ( '--near-field'
         , help    = "Near-field definition, give three comma-separated "
                     "start values, then three comma-separated "
@@ -3212,14 +3301,21 @@
                     " x,y,z coordinates of wire endpoints plus wire radius, "
                     "can be specified more than once, default is a "
                     "single wire with length 21.414285"
         , action  = 'append'
         , default = []
         )
     args = cmd.parse_args (argv)
+    if args.boundary not in boundaries:
+        print \
+            ( 'Invalid boundary: %s, must be one of %s'
+            % (args.boundary, ', '.join ('"%s"' % b for b in boundaries))
+            , file = f_err
+            )
+        return 23
     if not args.wire:
         args.wire = ['10, 0, 0, 0, 21.414285, 0, 0, 0.001']
     if not args.excitation_segment:
         args.excitation_segment = [5]
     if not args.excitation_voltage:
         args.excitation_voltage = [1]
     wires = []
@@ -3260,16 +3356,17 @@
             p = [float (x) for x in p]
         except ValueError as err:
             print ("Invalid medium %d: %s" % (n + 1, str (err)), file = f_err)
             return 23
         d = {}
         if n == 0:
             d = dict (rad)
+        d.update (boundary = args.boundary)
         if len (p) > 3:
-            d ['coord'] = p [3]
+            d.update (coord = p [3])
         p = p [:3]
         media.append (Medium (*p, **d))
     media = media or None
     m = Mininec (args.frequency, wires, media = media)
     for i, v in zip (args.excitation_segment, args.excitation_voltage):
         s = Excitation (cvolt = v)
         m.register_source (s, i - 1)
```

### Comparing `pymininec-0.3.0/pymininec.egg-info/PKG-INFO` & `pymininec-0.4.0/pymininec.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pymininec
-Version: 0.3.0
+Version: 0.4.0
 Summary: Python version of the original MININEC Antenna Optimization code
 Home-page: https://github.com/schlatterbeck/pymininec
 Author: Ralf Schlatterbeck
 Author-email: rsc@runtux.com
 License: MIT License
 Description: MININEC in Python
         =================
@@ -15,14 +15,16 @@
         .. |__| unicode:: U+2013   .. en dash without spaces
             :trim:
         .. |_| unicode:: U+00A0 .. Non-breaking space
             :trim:
         .. |-| unicode:: U+202F .. Thin non-breaking space
             :trim:
         .. |numpy.linalg.solve| replace:: ``numpy.linalg.solve``
+        .. |scipy.integrate| replace:: ``scipy.integrate``
+        .. |scipy.special.ellipk| replace:: ``scipy.special.ellipk``
         
         This is an attempt to rewrite the original MININEC3 basic sources in
         Python. Standard use-case like computation of feed impedance and far
         field are implemented and are quite well tested. There is only a command
         line interface.
         
         An example of using the command-line interface uses the following
@@ -61,66 +63,38 @@
         the format of the original Basic implementation of Mininec.
         
         Plotting
         --------
         
         The output tables produced by ``pymininec``
         are not very useful to get an idea of the far field behaviour of
-        an antenna. Therefore there is a small companion program ``plot-antenna``
-        that can plot the antenna pattern. The default is to plot all available
-        graphics, including an interactive 3d view. In addition with the
-        ``--azimuth`` or ``--elevation`` options you can get an Azimuth
-        diagram::
-        
-            plot-antenna --azimuth test/12-el-1deg.pout
-        
-        .. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-azimuth.png
-            :align: center
-        
-        or an elevation diagram::
-        
-            plot-antenna --elevation test/12-el-1deg.pout
-        
-        .. figure:: https://raw.githubusercontent.com/schlatterbeck/pymininec/master/test/12-el-elevation.png
-            :align: center
-        
-        respectively. Note that I used an output file with 1-degree resolution
-        in elevation and azimuth angles not with 5 degrees as in the example
-        above. The pattern look smoother but a 3D-view will be very slow due to
-        the large number of points. The plot program also has a ``--help``
-        option for further information. In particular the scaling of the antenna
-        plot can be ``linear``, ``linear_db``, and ``linear_voltage`` in
-        addition to the default of ``arrl`` scaling. You may consult Cebik's [6]_
-        article for explanation of the different diagrams.
-        
-        The latest version accepts several plot parameters, ``--elevation``,
-        ``--azimuth``, ``--plot3d``, ``--plot-vswr`` which are plotted into one
-        diagram. The default is to plot all four graphs. With the ``--output``
-        option pictures can directly be saved without displaying the graphics on
-        the screen.
-        
-        The plot program can also display output files of ``nec2c``, not only
-        from ``pymininec``.
-        
-        The latest version has key-bindings for scrolling through the
-        frequencies of an antenna simulation. So if you have an output file with
-        a simulation of multiple frequencies (either with ``pymininec`` or
-        ``nec2c``) you can display diagrams for the next frequency by typing
-        ``+``, and to the previous frequency by typing ``-``. For newer versions
-        of ``matplotlib`` you can display a scrollbar for the frequencies with
-        the ``--with-slider`` option.
-        
-        Other keybindings switch the scaling for the antenna plots, ``a``
-        switches to ``arrl`` scaling, ``l`` switches to linear scaling, ``d``
-        switches to linear dB scaling, and ``v`` switches to linear voltage
-        scaling.
-        
-        Finally the ``w`` option toggles display of the 3d diagram from/to
-        wireframe display. Note that the wireframe display may not be supported
-        on all versions of ``matplotlib`` and/or graphics cards.
+        an antenna. The companion program `plot-antenna`_ used to be bundled
+        with ``pymininec`` but was moved to its own project. You can currently
+        plot elevation and azimuth diagram of an antenna, a 3D-plot, the
+        geometry and VSWR. All either as a standalone program (using matplotlib)
+        or exported as HTML to the browser (using plotly).
+        
+        Ground (Media)
+        --------------
+        
+        The latest version implements the option parsing for the mininec ground
+        model for more than one medium. You also need to specify the
+        ``--boundary`` option to set the type of boundary between media: The
+        default ``linear`` boundary appends grounds in X-direction with the
+        distance in the 4th parameter of the ``--medium`` option. The
+        ``circular`` boundary has concentric media with the radius of each
+        medium given in the 4th parameter of the ``--medium`` option. The third
+        parameter of the ``--medium`` option is the height. Note that you
+        typically want *negative* heights for media further out, this allows
+        modelling of summits. Mininec *allows* the specification of *higher*
+        grounds but the results will be questionable as no reflection at the
+        higher ground is modelled. The ground implementation was not yet tested
+        against the originally basic code (or any other modelling program
+        implementing the mininec engine).
+        
         
         Test coverage: Making sure it is consistent with original Mininec
         -----------------------------------------------------------------
         
         There are several tests against the `original Basic source code`_, for
         the test cases see the subdirectory ``test``. One of the test cases is
         a simple 7MHz wire dipole with half the wavelength and 10 segments.
@@ -212,21 +186,22 @@
         on my PC (this has 264 segments, more than the original Mininec ever
         supported) when I'm using 5 degree increments for theta and phi angles
         and about 11 minutes (!) for 1 degree angles. The reason is that
         everything currently is implemented (like in Basic) as nested loops.
         This could (and should) be changed to use vector and matrix operations
         in `numpy`_. In the inner loop of the matrix fill operation there are
         several integrals computed using `gaussian quadrature`_ or a numeric
-        solution to an `elliptic integral`_. These could be implemented by
-        scipy_ library functions.
+        solution to an `elliptic integral`_. These are now implemented using
+        methods (or at least constants in the case of `gaussian quadrature`_)
+        from |scipy.integrate|_ and |scipy.special.ellipk|_.
         
         Notes on Elliptic Integral Parameters
         -------------------------------------
         
-        The Mininec code uses the implementation of an elliptic integral when
+        The Mininec code uses the implementation of an `elliptic integral`_ when
         computing the impedance matrix and in several other places. The integral
         uses a set of E-vector coefficients that are cited differently in
         different places. In the latest version of the open source Basic code
         these parameters are in lines 1510 |__| 1512. They are also
         reprinted in the publication [2]_ about that version of Mininec which
         has a listing of the Basic source code (slightly different from the
         version available online) where it is on p. |-| C-31 in lines
@@ -265,28 +240,28 @@
         but notice how in the *b* parameters (2nd line) the current Basic code
         has one more *3* in the second column. The rounding of the earlier Basic
         code suggests that the second *3* is a typo in the later Basic version.
         Also notice that in the 4th column the later Basic code has a *5* less
         than the version in the papers. The rounding in the earlier Basic code
         also suggests that the later Basic code is in error.
         
-        The errors in the elliptic integral parameters do not have much effect
+        The errors in the `elliptic integral`_ parameters do not have much effect
         on the computed values of the Mininec code. There are some minor
         differences but these are below the differences between Basic and Python
         implementation (single vs. double precision arithmetics). I had hoped
         that this has something to do with the well known fact that Mininec
         finds a resonance point of an antenna some percent too high which means
         that usually in practice the computed wire lengths are a little too
         long. This is apparently not the case. The resonance point is also wrong
         for very thin wires below the *small radius modification condition*
         which happens when the wire radius is below 1e-4 of the wavelength.
-        Even in that case --  where the elliptic integral is not used -- the
+        Even in that case --  where the `elliptic integral`_ is not used -- the
         resonance is slightly wrong.
         
-        The reference for the elliptic integral parameters [3]_ cited in both
+        The reference for the `elliptic integral`_ parameters [3]_ cited in both
         reports lists the following table on p. |-| 591:
         
         +---------------+--------------+--------------+--------------+--------------+
         | 1.38629436112 | .09666344259 | .03590092383 | .03742563713 | .01451196212 |
         +---------------+--------------+--------------+--------------+--------------+
         |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
         +---------------+--------------+--------------+--------------+--------------+
@@ -310,14 +285,20 @@
         +---------------+--------------+--------------+--------------+--------------+
         |            .5 | .12498593597 | .06880248576 | .03328355346 | .00441787012 |
         +---------------+--------------+--------------+--------------+--------------+
         
         So apparently the handbook [3]_ is correct. And the Basic version and
         *both* Mininec reports have at least one typo.
         
+        Since this paragraph was written the implementation of the `elliptic
+        integral`_ was removed and replace with a call to |scipy.special.ellipk|_.
+        The resulting differences in computed outputs were smaller than the
+        differences between the Basic (single precision) and the Python (double
+        precision) implementation.
+        
         Running examples in Basic
         -------------------------
         
         The original Basic source code can still be run today, thanks to Rob
         Hagemans `pcbasic`_ project. It is written in Python and can be
         installed with pip. It is also packaged in some Linux distributions,
         e.g. in Debian_.
@@ -345,14 +326,35 @@
         cut&paste buffer.
         
         The `original basic source code`_ can be obtained from the `unofficial
         NEC archive`_ by PA3KJ or from a `Mininec github project`_, I'm using
         the version from the `unofficial NEC archive`_ and have not verified if
         the two links I've given contain the same code.
         
+        Release Notes
+        -------------
+        
+        v0.4.0: Split `plot-antenna`_ into own project
+        
+        - Own project `plot-antenna`_
+        - Fix parsing of several medium options, mention ground in documentation
+        
+        v0.3.0: Laplace loads correctly implemented
+        
+        - Use scipy.special.ellipk for elliptic integral
+        - Use gaussian quadrature coefficients from scipy.integrate
+        - Test resonance (NEC vs. mininec)
+        
+        v0.2.0: Add short paragraph on new plotting program
+        
+        - Test coverage
+        - Expression simplification
+        
+        v0.1.0: Initial release
+        
         .. _`original basic source code`: http://nec-archives.pa3kj.com/mininec3.zip
         .. _`unofficial NEC archive`: http://nec-archives.pa3kj.com/
         .. _`Mininec github project`: https://github.com/Kees-PA3KJ/MiniNec
         .. _`numpy`: https://numpy.org/
         .. _`pcbasic`: https://github.com/robhagemans/pcbasic
         .. _`Debian`: https://packages.debian.org/stable/python3-pcbasic
         .. _`contribution to pcbasic`: https://github.com/robhagemans/pcbasic/pull/183
@@ -386,27 +388,31 @@
             Magazine, 2003. Available with antenna models from the `Cebik
             collection`_.
         
         .. _ADA121535: https://apps.dtic.mil/sti/pdfs/ADA121535.pdf
         .. _ADA181682: https://apps.dtic.mil/sti/pdfs/ADA181682.pdf
         .. _`numpy.linalg.solve`:
             https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html
+        .. _`scipy.integrate`: https://docs.scipy.org/doc/scipy/tutorial/integrate.html
+        .. _`scipy.special.ellipk`:
+            https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.ellipk.html
         .. _`OhioLINK Electronic Theses & Dissertations Center`:
             https://etd.ohiolink.edu/apexprod/rws_etd/send_file/send?accession=ohiou1176315682
         .. _`reported this as a bug in the pytest project`:
             https://github.com/pytest-dev/pytest/issues/10152
         .. _`as a bug in python`:
             https://github.com/python/cpython/issues/94974
         .. _`Cebik collection`:
             http://on5au.be/Books/allmodnotes.zip
         .. _`Antenna modelling notes episode 48`:
             http://on5au.be/content/amod/amod48.html
         .. _`gaussian quadrature`: https://en.wikipedia.org/wiki/Gaussian_quadrature
         .. _`elliptic integral`: https://en.wikipedia.org/wiki/Elliptic_integral
         .. _`scipy`: https://scipy.org/
+        .. _`plot-antenna`: https://github.com/schlatterbeck/plot-antenna
         
 Platform: Any
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Intended Audience :: Science/Research
```

### Comparing `pymininec-0.3.0/setup.py` & `pymininec-0.4.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,15 +54,14 @@
     , packages         = ['mininec']
     , platforms        = 'Any'
     , url              = "https://github.com/schlatterbeck/pymininec"
     , python_requires  = rq
     , entry_points     = dict
         ( console_scripts =
             [ 'pymininec=mininec.mininec:main'
-            , 'plot-antenna=mininec.plot_antenna:main'
             ]
         )
     , classifiers      = \
         [ 'Development Status :: 4 - Beta'
         , 'License :: OSI Approved :: ' + license
         , 'Operating System :: OS Independent'
         , 'Programming Language :: Python'
```

### Comparing `pymininec-0.3.0/test/test_mininec.py` & `pymininec-0.4.0/test/test_mininec.py`

 * *Files 2% similar despite different names*

```diff
@@ -240,26 +240,69 @@
                         self.assertEqual (ef [:-1], af [:-1])
                     else:
                         self.assertEqual (ef, af)
                 else:
                     self.assertLess (aff, -200)
     # end def compare_far_field_data
 
+    def compare_currents (self, exs, acs):
+        """ This is used when the CURRENT line in the feed pulse is
+            slightly off on different architectures. In addition the
+            individual CURRENT DATA lines are also compared
+            approximately
+        """
+        ex  = exs.split ('\n')
+        ac  = acs.split ('\n')
+        idx = exs.find ('CURRENT')
+        l   = len (exs [:idx].split ('\n'))
+        off = l - 1
+        self.assertEqual (ex [:off], ac [:off])
+        exc = ex [off].strip ()
+        acc = ac [off].strip ()
+        assert acc.startswith ('CURRENT = ( ')
+        assert acc.endswith (' J)')
+        exc = [float (x) for x in exc [12:-3].split (',')]
+        acc = [float (x) for x in acc [12:-3].split (',')]
+        self.assertAlmostEqual (exc [0], acc [0], 12)
+        self.assertAlmostEqual (exc [1], acc [1], 12)
+        off += 1
+        state = 0
+        for l_ex, l_ac in zip (ex [off:], ac [off:]):
+            if state == 0 or state == 2:
+                self.assertEqual (l_ex, l_ac)
+            if '(DEGREES)' in l_ex:
+                state = 1
+                continue
+            if state == 1:
+                sp_ex = l_ex.strip ().split ()
+                sp_ac = l_ac.strip ().split ()
+                if len (sp_ex) != 5 or sp_ex [0] in 'JE':
+                    state = 2
+                    self.assertEqual (l_ex, l_ac)
+                    continue
+                num_ex = [float (x) for x in sp_ex]
+                num_ac = [float (x) for x in sp_ac]
+                self.assertEqual (num_ex [0], num_ac [0])
+                for a, b in zip (num_ex [1:-1], num_ac [1:-1]):
+                    self.assertAlmostEqual (a, b, 12)
+                self.assertAlmostEqual (num_ex [-1], num_ac [-1], 10)
+    # end def compare_currents
+
     def compare_near_field_data (self, m, opts = None):
         """ Near field data below absolute values of 1e-15 may be
             different on different architectures
         """
         if opts is None:
             opts = set (('near-field',))
         ex  = self.expected_output.rstrip ().split ('\n')
         ac  = m.as_mininec (opts).rstrip ().split ('\n')
         idx = self.expected_output.find ('FIELD POINT: X')
         l   = len (self.expected_output [:idx].split ('\n'))
         off = l - 2
-        self.assertEqual (ex [:off], ac [:off])
+        self.compare_currents ('\n'.join (ex [:off]), '\n'.join (ac [:off]))
         for e, a in zip (ex [off:], ac [off:]):
             el = e.strip ().split ()
             al = a.strip ().split ()
             if not el:
                 self.assertEqual (e, a)
                 continue
             if el [0] in 'XYZ':
@@ -460,15 +503,16 @@
                 self.assertAlmostEqual (mat [i][j].real, m.Z [i][j].real, 3-f)
                 f = int (np.log (abs (mat [i][j].imag)) / np.log (10))
                 self.assertAlmostEqual (mat [i][j].imag, m.Z [i][j].imag, 3-f)
     # end def test_matrix_fill_ohio_example
 
     def test_dipole_wiredia_01 (self):
         m = self.dipole_7mhz (wire_dia = 0.01, filename = 'dipole-01.pout')
-        self.assertEqual (self.expected_output, m.as_mininec ())
+        out = m.as_mininec ()
+        self.assertEqual (self.expected_output, out)
     # end def test_dipole_wiredia_01
 
     def test_dipole_wiredia_001 (self):
         m = self.dipole_7mhz (wire_dia = 0.001, filename = 'dipole-001.pout')
         self.assertEqual (self.expected_output, m.as_mininec ())
     # end def test_dipole_wiredia_001
 
@@ -607,15 +651,15 @@
 # end class Test_Case_Known_Structure
 
 class Test_Doctest (unittest.TestCase):
 
     flags = doctest.NORMALIZE_WHITESPACE
 
     def test_mininec (self):
-        num_tests = 297
+        num_tests = 307
         f, t  = doctest.testmod \
             (mininec.mininec, verbose = False, optionflags = self.flags)
         fn = os.path.basename (mininec.mininec.__file__)
         format_ok  = '%(fn)s passes all of %(t)s doc-tests'
         format_nok = '%(fn)s fails %(f)s of %(t)s doc-tests'
         if f:
             msg = format_nok % locals ()
```

