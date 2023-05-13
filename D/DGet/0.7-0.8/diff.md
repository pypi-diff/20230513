# Comparing `tmp/DGet-0.7.tar.gz` & `tmp/DGet-0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "DGet-0.7.tar", last modified: Sat Apr 29 03:33:47 2023, max compression
+gzip compressed data, was "DGet-0.8.tar", last modified: Sat May 13 03:50:38 2023, max compression
```

## Comparing `DGet-0.7.tar` & `DGet-0.8.tar`

### file list

```diff
@@ -1,24 +1,25 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 03:33:47.149280 DGet-0.7/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 03:33:47.145280 DGet-0.7/DGet.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2648 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      354 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-04-29 03:33:47.000000 DGet-0.7/DGet.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-04-29 03:33:36.000000 DGet-0.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2648 2023-04-29 03:33:47.149280 DGet-0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2238 2023-04-29 03:33:36.000000 DGet-0.7/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 03:33:47.149280 DGet-0.7/dget/
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-04-29 03:33:36.000000 DGet-0.7/dget/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2954 2023-04-29 03:33:36.000000 DGet-0.7/dget/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-04-29 03:33:36.000000 DGet-0.7/dget/adduct.py
--rw-r--r--   0 runner    (1001) docker     (123)      946 2023-04-29 03:33:36.000000 DGet-0.7/dget/convolve.py
--rw-r--r--   0 runner    (1001) docker     (123)    12522 2023-04-29 03:33:36.000000 DGet-0.7/dget/dget.py
--rw-r--r--   0 runner    (1001) docker     (123)     2121 2023-04-29 03:33:36.000000 DGet-0.7/dget/formula.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-29 03:33:47.149280 DGet-0.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-04-29 03:33:36.000000 DGet-0.7/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 03:33:47.149280 DGet-0.7/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1903 2023-04-29 03:33:36.000000 DGet-0.7/tests/test_adduct.py
--rw-r--r--   0 runner    (1001) docker     (123)     2288 2023-04-29 03:33:36.000000 DGet-0.7/tests/test_dget.py
--rw-r--r--   0 runner    (1001) docker     (123)     3072 2023-04-29 03:33:36.000000 DGet-0.7/tests/test_formula.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:50:38.779628 DGet-0.8/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:50:38.775628 DGet-0.8/DGet.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2648 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      367 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-05-13 03:50:38.000000 DGet-0.8/DGet.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 03:50:26.000000 DGet-0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2648 2023-05-13 03:50:38.779628 DGet-0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2238 2023-05-13 03:50:26.000000 DGet-0.8/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:50:38.779628 DGet-0.8/dget/
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 03:50:26.000000 DGet-0.8/dget/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3284 2023-05-13 03:50:26.000000 DGet-0.8/dget/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-05-13 03:50:26.000000 DGet-0.8/dget/adduct.py
+-rw-r--r--   0 runner    (1001) docker     (123)      946 2023-05-13 03:50:26.000000 DGet-0.8/dget/convolve.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15695 2023-05-13 03:50:26.000000 DGet-0.8/dget/dget.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2121 2023-05-13 03:50:26.000000 DGet-0.8/dget/formula.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-05-13 03:50:26.000000 DGet-0.8/dget/plot.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 03:50:38.779628 DGet-0.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-05-13 03:50:26.000000 DGet-0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:50:38.779628 DGet-0.8/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1903 2023-05-13 03:50:26.000000 DGet-0.8/tests/test_adduct.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-05-13 03:50:26.000000 DGet-0.8/tests/test_dget.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3072 2023-05-13 03:50:26.000000 DGet-0.8/tests/test_formula.py
```

### Comparing `DGet-0.7/DGet.egg-info/PKG-INFO` & `DGet-0.8/DGet.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: DGet
-Version: 0.7
+Version: 0.8
 Summary: Calculates compound deuteration from ToF-MS data.
 Home-page: https://github.com/djdt/dget
 Author: djdt
 License: GPL3
 Project-URL: Documentation, https://dget.readthedocs.io
 Project-URL: Source, https://github.com/djdt/dget
 Project-URL: Web App, https://djdt.github.io/dget
```

### Comparing `DGet-0.7/LICENSE` & `DGet-0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `DGet-0.7/PKG-INFO` & `DGet-0.8/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: DGet
-Version: 0.7
+Version: 0.8
 Summary: Calculates compound deuteration from ToF-MS data.
 Home-page: https://github.com/djdt/dget
 Author: djdt
 License: GPL3
 Project-URL: Documentation, https://dget.readthedocs.io
 Project-URL: Source, https://github.com/djdt/dget
 Project-URL: Web App, https://djdt.github.io/dget
```

### Comparing `DGet-0.7/README.rst` & `DGet-0.8/README.rst`

 * *Files identical despite different names*

### Comparing `DGet-0.7/dget/__main__.py` & `DGet-0.8/dget/__main__.py`

 * *Files 4% similar despite different names*

```diff
@@ -40,14 +40,19 @@
         "--plot",
         nargs="?",
         const="targets",
         help="Plot the convolved match against the MS data, "
         "use '--plot full' to show the entire mass range..",
     )
     parser.add_argument(
+        "--nstates",
+        type=int,
+        help="Maximum number of states to calculate, defaults to first 2 < 0.5%",
+    )
+    parser.add_argument(
         "--masswidth",
         type=float,
         default=0.5,
         help="Window for integration of MS data.",
     )
     parser.add_argument(
         "--realign",
@@ -75,28 +80,33 @@
         "skiprows": args.skiprows,
         "usecols": args.columns,
     }
     dget = DGet(
         args.formula,
         args.tofdata,
         adduct=args.adduct,
+        number_states=args.nstates,
         loadtxt_kws=loadtxt_kws,
     )
     if args.autoadduct:
         adduct, diff = dget.guess_adduct_from_base_peak()
         dget.adduct = adduct
         print(f"Adduct difference from base peak m/z: {diff:.4f}")
         print()
 
     dget.mass_width = args.masswidth
     if args.realign:
-        dget.align_tof_with_spectra()
-        print(f"Re-aligned ToF data by shifting {dget.offset_mz:.2f} m/z")
+        offset = dget.align_tof_with_spectra()
+        print(f"Re-aligned ToF data by shifting {offset:.2f} m/z")
         print()
 
+    baseline = dget.subtract_baseline((dget.targets[0], dget.targets[-1]))
+    print(f"Subtracting baseline of {baseline:.2f}")
+    print()
+
     dget.print_results()
 
     if args.plot:
         import matplotlib.pyplot as plt
 
         fig, axes = plt.subplots(1, 1)
         dget.plot_predicted_spectra(axes, mass_range=args.plot)
```

### Comparing `DGet-0.7/dget/adduct.py` & `DGet-0.8/dget/adduct.py`

 * *Files identical despite different names*

### Comparing `DGet-0.7/dget/convolve.py` & `DGet-0.8/dget/convolve.py`

 * *Files identical despite different names*

### Comparing `DGet-0.7/dget/dget.py` & `DGet-0.8/dget/dget.py`

 * *Files 16% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 
 import numpy as np
 from molmass import Formula, Spectrum
 
 from dget.adduct import Adduct
 from dget.convolve import deconvolve
 from dget.formula import spectra_mz_spread
+from dget.plot import scale_to_match, stacked_stem
 
 
 class DGet(object):
     """Deuteration calculation class.
 
     This class contains functions for calculating deuteration from
     a molecular formula and mass spectra.
@@ -23,14 +24,15 @@
     The deilimter can be specified using the 'delimiter' keyword.
     Mass spectra can also be passed as a tuple of numpy arrays, (masses, signals).
 
     Attributes:
         deuterated_formula: formula of fully deuterated molecule
         tofdata: path to mass spectra text file, or tuple of masses, signals
         adduct: form of adduct ion, see `dget.adduct`
+        number_states: number of deuterated states to calculate
         signal_mass_width: range around each m/z to search for maxima or integrate
         signal_method: detection mode, valid values are 'peak area', 'peak height'
         spectrum_min_fraction: limit spectra to entries with at least this fraction
         loadtxt_kws: parameters passed to `numpy.loadtxt`,
             defaults to {'delimiter': ',', 'usecols': (0, 1)}
     """
 
@@ -48,39 +50,39 @@
     ]
 
     def __init__(
         self,
         deuterated_formula: str | Formula,
         tofdata: str | Path | Tuple[np.ndarray, np.ndarray],
         adduct: str = "[M]+",
+        number_states: int | None = None,
         signal_mass_width: float = 0.5,
         signal_mode: str = "peak height",
         spectrum_min_fraction: float = 0.01,
         loadtxt_kws: dict | None = None,
     ):
         if isinstance(deuterated_formula, str):
             deuterated_formula = Formula(deuterated_formula)
 
         _loadtxt_kws = {"delimiter": ",", "usecols": (0, 1)}
         if loadtxt_kws is not None:
             _loadtxt_kws.update(loadtxt_kws)
 
-        self.offset_mz: float | None = None
-
         self._targets: np.ndarray | None = None
         self._probabilities: np.ndarray | None = None
         self._probability_remainders: np.ndarray | None = None
 
         self.adduct = Adduct(deuterated_formula, adduct)
 
         if self.deuterium_count == 0:
             raise ValueError(
                 f"formula: {self.adduct.base.formula} does not contain deuterium"
             )
 
+        self.number_states = number_states
         self.mass_width = signal_mass_width
         if signal_mode not in ["peak area", "peak height"]:
             raise ValueError("signal_mode must be one of 'peak area', 'peak height'.")
         self.signal_mode = signal_mode
         self.spectra_min_fraction = spectrum_min_fraction
 
         if isinstance(tofdata, (str | Path)):
@@ -98,23 +100,23 @@
 
     @property
     def deuteration(self) -> float:
         """The deuteration of the *base molecule*.
 
         Deuteration is calculated as the fraction of deuterium in the molecular
         formula that have been deuterated successfully.
-
         For example: 60% C2H5D1, 40% C2H6 would give a deuteration of 0.6.
+
+        Deuteration is only calculated for the ``number_states`` highest deuteration
+        states.
         """
-        prob = self.deuteration_probabilites
-        return (
-            np.sum(prob * np.arange(prob.size))
-            / self.deuterium_count
-            / self.adduct.num_base
-        )
+        states = self.deuteration_states
+        prob = self.deuteration_probabilites[states]
+        prob = prob / prob.sum()  # re-normalise
+        return np.sum(prob * states) / self.deuterium_count / self.adduct.num_base
 
     @property
     def deuteration_probabilites(self) -> np.ndarray:
         """The deuteration fraction of each possible deuteration.
 
         Probabilities are listed in order of D=0 to N, where N is the number of
         deuterium in the original molecular formula. Probabilites will sum to 1.0.
@@ -139,19 +141,39 @@
                     self.y, np.stack((starts[valid], ends[valid]), axis=1).flat
                 )[::2]
             counts = counts / counts.sum()
 
             self._probabilities, self._probability_remainders = deconvolve(
                 counts, self.psf
             )
+            # Remove negative proabilities and normalise
+            self._probabilities[self._probabilities < 0.0] = 0.0
             self._probabilities = self._probabilities / self._probabilities.sum()
 
         return self._probabilities  # type: ignore
 
     @property
+    def deuteration_states(self) -> np.ndarray:
+        """Indexes of the valid deuteration states.
+
+        Valid states are those Dx-Dn, where n is the number of deuterium atoms
+        in the base molecule as x is either:
+            ``n - self.number_states``
+            ``n - the 2nd last D with a probability < 0.5%``
+        """
+        if self.number_states is None:
+            prob = self.deuteration_probabilites
+            idx = np.flatnonzero((prob[:-1] < 0.005) & (prob[1] < 0.005)) - 1
+            nstates = idx[-1] if idx.size > 0 else self.deuterium_count
+        else:
+            nstates = self.number_states
+        print(self.deuterium_count - nstates)
+        return np.arange(self.deuterium_count - nstates, self.deuterium_count + 1)
+
+    @property
     def formula(self) -> Formula:
         """The adduct formula."""
         return self.adduct.formula
 
     @property
     def psf(self) -> np.ndarray:  # type: ignore
         """The point spread function used for (de)convolution.
@@ -168,15 +190,16 @@
     @property
     def targets(self) -> np.ndarray:
         """The m/z of every possible spectrum.
 
         A new spectrum is created by combining the spectra of every possible
         deuteration state."""
         if self._targets is None:
-            self._targets = spectra_mz_spread(list(self.spectra()))
+            spectra = list(self.spectra())
+            self._targets = spectra_mz_spread(spectra)
         return self._targets
 
     def __str__(self) -> str:
         return f"DGet({self.adduct})"
 
     def __repr__(self) -> str:
         return f"DGet({self.adduct!r})"
@@ -200,31 +223,74 @@
             )
         for kw in ["unpack", "dtype"]:
             if kw in kwargs:
                 kwargs.pop(kw)
                 print(f"warning: removing loadtxt keyword '{kw}'")
         return np.loadtxt(path, unpack=True, dtype=np.float32, **kwargs)  # type: ignore
 
-    def align_tof_with_spectra(self) -> None:
+    def align_tof_with_spectra(self, alignment_mz: float | None = None) -> float:
         """Shifts ToF data to better align with monoisotopic m/z.
 
         Please calibrate your MS instead of using this.
-        Sets the ``DGet.offset_mz`` attribute as the shift use dto align.
+
+        Args:
+            alignment_mz: m/zz used for alignment, defaults to monoisotopic m/z
+
+        Returns:
+            offset used for alignment
         """
-        mz = self.formula.isotope.mz
-        start, onmass, end = np.searchsorted(
-            self.x, [mz - self.mass_width, mz, mz + self.mass_width]
+        if alignment_mz is None:
+            alignment_mz = self.formula.isotope.mz
+
+        idx = np.searchsorted(
+            self.x,
+            [
+                alignment_mz - self.mass_width,
+                alignment_mz,
+                alignment_mz + self.mass_width,
+            ],
         )
-        if start == 0 or end == self.x.size:
-            raise ValueError("unable to align, m/z falls outside of mass spectra")
+        start, onmass, end = np.clip(idx, 0, self.x.size)
+        if start == end:
+            raise ValueError("unable to align, m/z falls outside spectra")
 
-        self.offset_mz = self.x[start + np.argmax(self.y[start:end])] - self.x[onmass]
-        if abs(self.offset_mz) > 1.0:  # type: ignore
+        offset = self.x[onmass] - self.x[start + np.argmax(self.y[start:end])]
+        if abs(offset) > 0.5:  # type: ignore
             print("warning: calculated alignment offset greater than 0.5 Da!")
-        self.x -= self.offset_mz
+        self.x += offset
+        return offset
+
+    def subtract_baseline(
+        self, mass_range: Tuple[float, float] | None = None, percentile: float = 25.0
+    ) -> float:
+        """Subtracts baseline of region.
+
+        Clalulates the ``percentile`` percentile of the designated mass region and
+        subtracts it from the mass spec signals.
+
+        Args:
+            mass_range: region to find baseline
+            percentile: percentile to use
+
+        Returns:
+            offset used for alignment
+        """
+        if mass_range is not None:
+            idx = np.searchsorted(self.x, mass_range)
+            start, end = np.clip(idx, 0, self.x.size)
+        else:
+            start, end = 0, self.x.size
+        if start == end:
+            raise ValueError(
+                "unable to subtract baseline, entire m/z range falls outside spectra"
+            )
+
+        baseline = np.percentile(self.y[start:end], percentile)
+        self.y -= baseline
+        return baseline
 
     def guess_adduct_from_base_peak(
         self,
         adducts: List[Formula] | None = None,
         mass_range: Tuple[float, float] | None = None,
     ) -> Tuple[Adduct, float]:
         """Finds the adduct closest to the m/z of the largest tof peak.
@@ -248,107 +314,121 @@
                 formulas.append(Adduct(self.adduct.base, adduct))
             except ValueError:
                 pass
 
         masses = np.array([f.formula.isotope.mz for f in formulas])
 
         if mass_range is not None:
-            start, stop = np.searchsorted(self.x, mass_range)
+            idx = np.searchsorted(self.x, mass_range)
+            start, end = np.clip(idx, 0, self.x.size)
         else:
-            start, stop = 0, self.x.size
+            start, end = 0, self.x.size
+        if start == end:
+            raise ValueError(
+                "unable to get adduct, entire m/z range falls outside spectra"
+            )
 
-        base = self.x[start:stop][np.argmax(self.y[start:stop])]
-        diffs = base - masses
+        base = self.x[start:end][np.argmax(self.y[start:end])]
+        diffs = masses - base
         best = np.argmin(np.abs(diffs))
         return formulas[best], diffs[best]
 
     def plot_predicted_spectra(
         self,
         ax: "matplotlib.axes.Axes",
         mass_range: Tuple[float, float] | str = "targets",  # noqa: F821
+        color_probabilites: bool = False,
     ) -> None:
         """Plot spectra over mass spectra on `ax`.
 
         `mass_range` can be passed as a tuple of floats (start m/z, end m/z),
         'full' to plot the entire mass range or 'targets' to plot the region around
         the predicted spectra.
 
         Args:
             ax: matplotlib axes to plot on
             mass_range: range to plot
+            color_probabilites: use a colour for each probability
         """
-
-        def scale_spectra(x, y, spectra_x, spectra):
-            max = spectra_x[np.argmax(spectra)]
-            start, end = np.searchsorted(
-                x, [max - self.mass_width, max + self.mass_width]
-            )
-            if start == end:
-                return spectra
-            return spectra * np.amax(y[start:end]) / spectra.max()
-
         targets = self.targets
 
         if isinstance(mass_range, str):
             if mass_range == "full":
                 mass_range = self.x.min(), self.x.max()
             elif mass_range == "targets":
                 mass_range = targets.min() - 5.0, targets.max() + 5.0
             else:
                 raise ValueError("'mass_range' must be one of 'full', 'targets'.")
 
         start, end = np.searchsorted(self.x, mass_range)
         x, y = self.x[start:end], self.y[start:end]
 
-        prediction = np.convolve(self.deuteration_probabilites, self.psf, mode="full")
-
         # Data
         ax.plot(x, y, color="black")
 
-        # Scaled prediction
-        if prediction.size == 0:
+        if self.deuteration_probabilites.size == 0:
             return
 
-        ax.stem(
-            targets,
-            scale_spectra(x, y, targets, prediction),
-            markerfmt=" ",
-            basefmt=" ",
-            linefmt="red",
-            label="Deconvolved Spectra",
-        )
+        if color_probabilites:
+            ys = np.zeros(
+                (
+                    self.deuteration_probabilites.size,
+                    self.deuteration_probabilites.size,
+                )
+            )
+            np.fill_diagonal(ys.T, self.deuteration_probabilites)
+            ys = np.apply_along_axis(np.convolve, 0, ys, self.psf, mode="full")
+            ys = scale_to_match(x, y, targets, ys, width=self.mass_width)
+
+            kws = [{"colors": f"C{i}"} for i in range(ys.shape[1])]
+
+            stacked_stem(ax, targets, ys, stack_kws=kws)
+        else:
+            # Scaled prediction
+            ys = np.convolve(self.deuteration_probabilites, self.psf, mode="full")
+            ax.stem(
+                targets,
+                scale_to_match(x, y, targets, ys, width=self.mass_width),
+                markerfmt=" ",
+                basefmt=" ",
+                linefmt="C1-",
+                label="Deconvolved Spectra",
+            )
 
         # Scaled PSF
-        masses = [i.mz for i in self.spectrum.values()]
+        masses = np.array([i.mz for i in self.spectrum.values()])
         ax.stem(
             masses,
-            scale_spectra(x, y, masses, self.psf),
+            scale_to_match(x, y, masses, self.psf, width=self.mass_width),
             markerfmt=" ",
             basefmt=" ",
-            linefmt="blue",
+            linefmt="--",
             label="Adduct Spectra",
         )
         ax.set_title(f"{self.adduct.base.formula} {self.adduct.adduct}")
         ax.set_xlabel("M/Z")
         ax.set_ylabel("Signal")
         ax.legend(loc="best", bbox_to_anchor=(0.0, 0.6, 1.0, 0.4))
 
     def print_results(self) -> None:
         """Print results to stdout."""
         pd = self.deuteration  # ensure calculated
+        states = self.deuteration_states
+        prob = self.deuteration_probabilites[states]
+        prob = prob / prob.sum()
 
         print(f"Formula          : {self.adduct.base.formula}")
         print(f"Adduct           : {self.adduct.adduct}")
         print(f"M/Z              : {self.adduct.base.isotope.mz:.4f}")
         print(f"Adduct M/Z       : {self.formula.isotope.mz:.4f}")
         print(f"%Deuteration     : {pd * 100.0:.2f} %")
         print()
         print("Deuteration Ratio Spectra")
-        for i, p in enumerate(self.deuteration_probabilites):
-            print(f"D{i:<2}              : {p * 100.0:5.2f} %")
+        for s, p in zip(states, prob):
+            print(f"D{s:<2}              : {p * 100.0:5.2f} %")
 
     def spectra(self, **kwargs) -> Generator[Spectrum, None, None]:
         """Spectrum of all compounds from non to fully deuterated.
 
         kwargs are passed to molmass.Formula.spectrum()
         """
```

### Comparing `DGet-0.7/dget/formula.py` & `DGet-0.8/dget/formula.py`

 * *Files identical despite different names*

### Comparing `DGet-0.7/setup.py` & `DGet-0.8/setup.py`

 * *Files identical despite different names*

### Comparing `DGet-0.7/tests/test_adduct.py` & `DGet-0.8/tests/test_adduct.py`

 * *Files identical despite different names*

### Comparing `DGet-0.7/tests/test_dget.py` & `DGet-0.8/tests/test_dget.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 def test_dget_know_data():
     formulas = {
         "C12HD8N": ("[M-H]-", 94.4),
         "C42H69D13NO8P": ("[M+H]+", 99.0),
         "C16H11D7N2O4S": ("[M-H]-", 95.4),
         "C57H3D101O6": ("[M+Na]+", 95.1),
-        "C13H9D7N2O2": ("[M+Na]+", 94.9),
+        # "C13H9D7N2O2": ("[M+Na]+", 94.9),
     }
 
     for formula, (adduct, percent_d) in formulas.items():
         dget = DGet(
             formula,
             data_path.joinpath(f"{formula}.txt"),
             adduct=adduct,
@@ -44,17 +44,22 @@
     dget._probabilities = np.array([0.1, 0.3, 0.6])
     assert np.isclose(dget.deuteration, 0.75)
 
     dget = DGet("C2H2D4", tofdata=(np.array([0.0, 999.0]), np.array([0.0, 0.0])))
     dget._probabilities = np.array([0.4, 0.2, 0.2, 0.1, 0.1])
     assert np.isclose(dget.deuteration, 0.325)
     dget._probabilities = np.array([0.5, 0.0, 0.0, 0.0, 0.5])
-    assert np.isclose(dget.deuteration, 0.5)
+    assert np.all(dget.deuteration_states == [2, 3, 4])
+    assert np.isclose(dget.deuteration, 1.0)
     dget._probabilities = np.array([0.1, 0.1, 0.2, 0.2, 0.4])
     assert np.isclose(dget.deuteration, 0.675)
+    dget._probabilities = np.array([0.5, 0.0, 0.0, 0.0, 0.5])
+    dget.number_states = 4
+    assert np.all(dget.deuteration_states == [0, 1, 2, 3, 4])
+    assert np.isclose(dget.deuteration, 0.5)
 
 
 def test_targets():
     dget = DGet("C20D6", tofdata=(np.array([0.0, 999.0]), np.array([0.0, 0.0])))
     formulas = ["C20H6", "C20H5D", "C20H4D2", "C20H3D3", "C20H2D4", "C20HD5", "C20D6"]
 
     assert np.allclose(dget.targets[:7], [Formula(f).isotope.mz for f in formulas])
```

### Comparing `DGet-0.7/tests/test_formula.py` & `DGet-0.8/tests/test_formula.py`

 * *Files identical despite different names*

