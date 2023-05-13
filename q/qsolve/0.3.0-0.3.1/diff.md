# Comparing `tmp/qsolve-0.3.0.tar.gz` & `tmp/qsolve-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "qsolve-0.3.0.tar", last modified: Wed May 10 14:39:00 2023, max compression
+gzip compressed data, was "qsolve-0.3.1.tar", last modified: Sat May 13 18:00:43 2023, max compression
```

## Comparing `qsolve-0.3.0.tar` & `qsolve-0.3.1.tar`

### file list

```diff
@@ -1,130 +1,114 @@
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       31 2023-05-10 12:21:00.000000 qsolve-0.3.0/MANIFEST.in
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      807 2023-05-10 14:39:00.618233 qsolve-0.3.0/PKG-INFO
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      306 2023-05-04 13:53:12.000000 qsolve-0.3.0/README.md
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       38 2023-05-10 14:39:00.618233 qsolve-0.3.0/setup.cfg
--rwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)     1095 2023-05-10 14:38:57.000000 qsolve-0.3.0/setup.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.610233 qsolve-0.3.0/src/
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.610233 qsolve-0.3.0/src/qsolve/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       33 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      403 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/constants.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.610233 qsolve-0.3.0/src/qsolve/core/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      258 2023-05-10 13:39:58.000000 qsolve-0.3.0/src/qsolve/core/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2755 2023-05-10 14:00:41.000000 qsolve-0.3.0/src/qsolve/core/fourier.pyc
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     5904 2023-05-10 14:00:41.000000 qsolve-0.3.0/src/qsolve/core/qsolve_core_gpe_1d.pyc
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     6904 2023-05-10 14:00:41.000000 qsolve-0.3.0/src/qsolve/core/qsolve_core_gpe_2d.pyc
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)    15510 2023-05-10 14:00:41.000000 qsolve-0.3.0/src/qsolve/core/qsolve_core_gpe_3d.pyc
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.610233 qsolve-0.3.0/src/qsolve/figures/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       41 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       41 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1868 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_control_inputs.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2267 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_psi_abs_squared_1d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2607 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_psi_re_im_1d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     5507 2023-05-10 13:07:49.000000 qsolve-0.3.0/src/qsolve/figures/figure_main_1d/figure_main_1d.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/figures/style/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4284 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/colors.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      225 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/hex2rgb.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1502 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/make_cmap.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1279 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/mpl_settings.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4727 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/figures/style/mystyle.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      124 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/parameter.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/potentials/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/potentials/components_1d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/box_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      285 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/gaussian_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      126 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/gaussian_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      192 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/harmonic_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/harmonic_x_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/harmonic_y_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/harmonic_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/lattice_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2746 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/lesanovsky_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3134 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/lesanovsky_xy_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       64 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/potentials/components_1d/tilt_x_3d.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/potentials/components_2d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/box_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      213 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/gaussian_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       16 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/gaussian_y_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      154 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/harmonic_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        1 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/harmonic_x_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/harmonic_y_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/harmonic_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_2d/lattice_z_3d.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/potentials/components_3d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/box_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      285 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/gaussian_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      126 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/gaussian_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      192 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/harmonic_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/harmonic_x_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/harmonic_y_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/harmonic_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/lattice_z_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2746 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/lesanovsky_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3134 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/lesanovsky_xy_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       64 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/potentials/components_3d/tilt_x_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      843 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/primes.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/solvers/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      108 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/solvers/solvers_1d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       39 2023-05-08 10:00:10.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_1d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     7683 2023-05-10 12:15:09.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_1d/solver_gpe_1d.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.614233 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       53 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      997 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/chemical_potential.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      860 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/compute_ground_state_solution.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1985 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/densities.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3251 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/energies.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4044 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/getter_functions.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      537 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_device.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1350 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_grid_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      587 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_potential.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      461 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_time_evolution.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      471 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/n_atoms.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       83 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/set_V.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      374 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/set_psi.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     5486 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/solver_gpe_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1525 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/spectrum.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1248 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/units.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       53 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      398 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/check_python_version.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1039 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/chemical_potential.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      877 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/compute_ground_state_solution.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1985 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/densities.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3937 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/energies.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     6584 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/getter_functions.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      537 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_device.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1974 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_grid_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      637 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_potential.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      159 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_seed.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      461 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_time_evolution.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1897 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_units.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      489 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/n_atoms.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       83 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/set_V.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      374 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/set_psi.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3308 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/solver_gpe_3d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1525 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/spectrum.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1110 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/units.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2683 2023-05-08 08:28:31.000000 qsolve-0.3.0/src/qsolve/units.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/src/qsolve/units_backup/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       30 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/units_backup/__init__.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1680 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/units_backup/units_1d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      899 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/units_backup/units_2d.py
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1156 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/units_backup/units_3d.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.618233 qsolve-0.3.0/src/qsolve/utils/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-04 13:53:12.000000 qsolve-0.3.0/src/qsolve/utils/__init__.py
-drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-10 14:39:00.610233 qsolve-0.3.0/src/qsolve.egg-info/
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      807 2023-05-10 14:39:00.000000 qsolve-0.3.0/src/qsolve.egg-info/PKG-INFO
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     5183 2023-05-10 14:39:00.000000 qsolve-0.3.0/src/qsolve.egg-info/SOURCES.txt
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        1 2023-05-10 14:39:00.000000 qsolve-0.3.0/src/qsolve.egg-info/dependency_links.txt
--rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        7 2023-05-10 14:39:00.000000 qsolve-0.3.0/src/qsolve.egg-info/top_level.txt
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.779208 qsolve-0.3.1/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       30 2023-05-13 17:20:39.000000 qsolve-0.3.1/MANIFEST.in
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      603 2023-05-13 18:00:43.779208 qsolve-0.3.1/PKG-INFO
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      344 2023-05-13 17:26:07.000000 qsolve-0.3.1/README.md
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       38 2023-05-13 18:00:43.779208 qsolve-0.3.1/setup.cfg
+-rwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)     1038 2023-05-13 18:00:19.000000 qsolve-0.3.1/setup.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.763208 qsolve-0.3.1/src/
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.763208 qsolve-0.3.1/src/qsolve/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       33 2023-05-06 14:25:43.000000 qsolve-0.3.1/src/qsolve/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      403 2023-05-04 16:16:02.000000 qsolve-0.3.1/src/qsolve/constants.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.767208 qsolve-0.3.1/src/qsolve/core/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      258 2023-05-13 17:17:51.000000 qsolve-0.3.1/src/qsolve/core/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)   778016 2023-05-13 17:16:25.000000 qsolve-0.3.1/src/qsolve/core/fourier.cpython-310-x86_64-linux-gnu.so
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)   823104 2023-05-13 17:16:37.000000 qsolve-0.3.1/src/qsolve/core/qsolve_core_gpe_1d.cpython-310-x86_64-linux-gnu.so
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)   831296 2023-05-13 17:16:49.000000 qsolve-0.3.1/src/qsolve/core/qsolve_core_gpe_2d.cpython-310-x86_64-linux-gnu.so
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)  1048384 2023-05-13 17:17:02.000000 qsolve-0.3.1/src/qsolve/core/qsolve_core_gpe_3d.cpython-310-x86_64-linux-gnu.so
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.767208 qsolve-0.3.1/src/qsolve/figures/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       41 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/__init__.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.767208 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       41 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1868 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_control_inputs.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2267 2023-05-06 15:45:28.000000 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_psi_abs_squared_1d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2607 2023-05-06 15:44:58.000000 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_psi_re_im_1d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     5507 2023-05-10 16:00:22.000000 qsolve-0.3.1/src/qsolve/figures/figure_main_1d/figure_main_1d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.771208 qsolve-0.3.1/src/qsolve/figures/style/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4284 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/colors.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      225 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/hex2rgb.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1502 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/make_cmap.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1279 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/mpl_settings.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4727 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/figures/style/mystyle.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      124 2023-05-06 14:31:31.000000 qsolve-0.3.1/src/qsolve/parameter.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.771208 qsolve-0.3.1/src/qsolve/potentials/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/__init__.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.771208 qsolve-0.3.1/src/qsolve/potentials/components_1d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/box_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      285 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/gaussian_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      126 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/gaussian_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      192 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/harmonic_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/harmonic_x_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/harmonic_y_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/harmonic_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/lattice_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2746 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/lesanovsky_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3134 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/lesanovsky_xy_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       64 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_1d/tilt_x_3d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.771208 qsolve-0.3.1/src/qsolve/potentials/components_2d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/box_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      213 2023-04-27 13:56:24.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/gaussian_2d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       16 2023-04-27 14:02:09.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/gaussian_y_2d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      154 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/harmonic_2d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        1 2023-04-27 14:01:12.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/harmonic_x_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/harmonic_y_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/harmonic_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/potentials/components_2d/lattice_z_3d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.775208 qsolve-0.3.1/src/qsolve/potentials/components_3d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      194 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/box_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      285 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/gaussian_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      126 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/gaussian_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      192 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/harmonic_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/harmonic_x_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/harmonic_y_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      116 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/harmonic_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      160 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/lattice_z_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2746 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/lesanovsky_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3134 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/lesanovsky_xy_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       64 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/potentials/components_3d/tilt_x_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      843 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/primes.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.775208 qsolve-0.3.1/src/qsolve/solvers/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      108 2023-05-02 19:44:05.000000 qsolve-0.3.1/src/qsolve/solvers/__init__.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.775208 qsolve-0.3.1/src/qsolve/solvers/solvers_1d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       39 2023-05-08 16:18:07.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_1d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     7690 2023-05-12 17:16:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_1d/solver_gpe_1d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.775208 qsolve-0.3.1/src/qsolve/solvers/solvers_2d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       39 2023-05-11 15:20:46.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_2d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     9054 2023-05-12 17:40:19.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_2d/solver_gpe_2d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.775208 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       53 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/__init__.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.779208 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      398 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/check_python_version.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1039 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/chemical_potential.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      877 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/compute_ground_state_solution.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1985 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/densities.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3937 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/energies.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     6584 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/getter_functions.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      537 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_device.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1974 2023-05-06 11:59:46.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_grid_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      637 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_potential.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      159 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_seed.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      461 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_time_evolution.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1897 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_units.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      489 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/n_atoms.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       83 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/set_V.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      374 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/set_psi.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     3308 2023-04-22 11:03:47.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/solver_gpe_3d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1525 2023-04-26 16:21:29.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/spectrum.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1110 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/units.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     2683 2023-05-06 12:00:25.000000 qsolve-0.3.1/src/qsolve/units.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.779208 qsolve-0.3.1/src/qsolve/units_backup/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)       30 2023-05-04 16:16:02.000000 qsolve-0.3.1/src/qsolve/units_backup/__init__.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1680 2023-05-04 16:16:02.000000 qsolve-0.3.1/src/qsolve/units_backup/units_1d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      899 2023-05-04 16:16:02.000000 qsolve-0.3.1/src/qsolve/units_backup/units_2d.py
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     1156 2023-05-04 16:16:02.000000 qsolve-0.3.1/src/qsolve/units_backup/units_3d.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.779208 qsolve-0.3.1/src/qsolve/utils/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-04-06 18:09:05.000000 qsolve-0.3.1/src/qsolve/utils/__init__.py
+drwxrwxr-x   0 jfmennemann  (1000) jfmennemann  (1000)        0 2023-05-13 18:00:43.763208 qsolve-0.3.1/src/qsolve.egg-info/
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)      603 2023-05-13 18:00:43.000000 qsolve-0.3.1/src/qsolve.egg-info/PKG-INFO
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)     4385 2023-05-13 18:00:43.000000 qsolve-0.3.1/src/qsolve.egg-info/SOURCES.txt
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        1 2023-05-13 18:00:43.000000 qsolve-0.3.1/src/qsolve.egg-info/dependency_links.txt
+-rw-rw-r--   0 jfmennemann  (1000) jfmennemann  (1000)        7 2023-05-13 18:00:43.000000 qsolve-0.3.1/src/qsolve.egg-info/top_level.txt
```

### Comparing `qsolve-0.3.0/setup.py` & `qsolve-0.3.1/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -6,30 +6,28 @@
 with open("README.md", "r", encoding="utf-8") as fh:
     
     long_description = fh.read()
 
 
 setuptools.setup(
     name="qsolve",
-    version="0.3.0",
+    version="0.3.1",
     url = "https://github.com/jfmennemann/qsolve",
     author="Jan-Frederik Mennemann",
     author_email="jfmennemann@gmx.de",
-    description="Numerical methods for the simulation of ultracold atom experiments",
+    description="Numerical framework for the simulation and optimization of ultracold atom experiments",
     # long_description=read('README.md'),
     long_description=long_description,
-    # long_description_content_type='text/markdown',
     packages=find_packages(where="src"),
     package_dir={"": "src"},
-    # package_dir={"": "qsolve"},
     include_package_data=True,
-    install_requires=[],
-    classifiers=[
-        'Programming Language :: Python',
-        'Programming Language :: Python :: 3',
-        'Programming Language :: Python :: 3.10',
-    ],
+    install_requires=[]
+    # classifiers=[
+    #     'Programming Language :: Python',
+    #     'Programming Language :: Python :: 3',
+    #     'Programming Language :: Python :: 3.10',
+    # ],
     # package_data={'': ['/qsolve/qsolve/core/*.pyc']},
     # license="MIT",
-    keywords="ultracold atoms, classical fields simulations, Gross-Pitaevskii equation, thermal state sampling, time of flight"
+    # keywords="ultracold atoms, classical fields simulations, Gross-Pitaevskii equation, thermal state sampling, time of flight"
 )
```

### Comparing `qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_control_inputs.py` & `qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_control_inputs.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_psi_abs_squared_1d.py` & `qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_psi_abs_squared_1d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/figure_main_1d/fig_psi_re_im_1d.py` & `qsolve-0.3.1/src/qsolve/figures/figure_main_1d/fig_psi_re_im_1d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/figure_main_1d/figure_main_1d.py` & `qsolve-0.3.1/src/qsolve/figures/figure_main_1d/figure_main_1d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/style/colors.py` & `qsolve-0.3.1/src/qsolve/figures/style/colors.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/style/make_cmap.py` & `qsolve-0.3.1/src/qsolve/figures/style/make_cmap.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/style/mpl_settings.py` & `qsolve-0.3.1/src/qsolve/figures/style/mpl_settings.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/figures/style/mystyle.py` & `qsolve-0.3.1/src/qsolve/figures/style/mystyle.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/potentials/components_1d/lesanovsky_3d.py` & `qsolve-0.3.1/src/qsolve/potentials/components_1d/lesanovsky_3d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/potentials/components_1d/lesanovsky_xy_3d.py` & `qsolve-0.3.1/src/qsolve/potentials/components_1d/lesanovsky_xy_3d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/potentials/components_3d/lesanovsky_3d.py` & `qsolve-0.3.1/src/qsolve/potentials/components_3d/lesanovsky_3d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/potentials/components_3d/lesanovsky_xy_3d.py` & `qsolve-0.3.1/src/qsolve/potentials/components_3d/lesanovsky_xy_3d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/primes.py` & `qsolve-0.3.1/src/qsolve/primes.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_1d/solver_gpe_1d.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_1d/solver_gpe_1d.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 import sys
 
 import math
 
 from qsolve.core import qsolve_core_gpe_1d
 
 from qsolve.primes import get_prime_factors
+
 from qsolve.units import Units
 
 
 class SolverGPE1D(object):
 
     def __init__(self, *, m_atom, a_s, omega_perp, seed=0, device='cpu', num_threads_cpu=1):
 
@@ -27,15 +28,15 @@
         print()
         # -----------------------------------------------------------------------------------------
 
         torch.manual_seed(seed)
 
         torch.set_num_threads(num_threads_cpu)
 
-        self.device = torch.device(device)
+        self._device = torch.device(device)
 
         self._units = Units.solver_units(m_atom, dim=1)
 
         # -----------------------------------------------------------------------------------------
         self._hbar = scipy.constants.hbar / self._units.unit_hbar
         self._mu_B = scipy.constants.physical_constants['Bohr magneton'][0] / self._units.unit_bohr_magneton
         self._k_B = scipy.constants.Boltzmann / self._units.unit_k_B
@@ -100,15 +101,15 @@
 
         _x = np.linspace(self._x_min, self._x_max, self._Jx, endpoint=False)
 
         self._dx = _x[1] - _x[0]
 
         self._Lx = self._Jx * self._dx
 
-        self._x = torch.tensor(_x, dtype=torch.float64, device=self.device)
+        self._x = torch.tensor(_x, dtype=torch.float64, device=self._device)
 
     def init_external_potential(self, compute_external_potential, parameters_potential):
 
         self._compute_external_potential = compute_external_potential
 
         for key, p in parameters_potential.items():
 
@@ -157,14 +158,29 @@
 
             return self._units.unit_wave_function * _psi_0.cpu().numpy(), vec_res, vec_iter
 
         else:
 
             return self._units.unit_wave_function * _psi_0.cpu().numpy()
 
+    def init_time_evolution(self, *, t_final, dt):
+
+        self._t_final = t_final / self._units.unit_time
+        self._dt = dt / self._units.unit_time
+
+        self._n_time_steps = int(np.round(self._t_final / self._dt))
+
+        self._n_times = self._n_time_steps + 1
+
+        assert (np.abs(self._n_time_steps * self._dt - self._t_final)) < 1e-14
+
+        self._times = self._dt * np.arange(self._n_times)
+
+        assert (np.abs(self._times[-1] - self._t_final)) < 1e-14
+
     def propagate_gpe(self, *, u_of_times, n_start, n_inc, mue_shift=0.0):
 
         _mue_shift = mue_shift / self._units.unit_energy
 
         n_local = 0
 
         while n_local < n_inc:
@@ -191,29 +207,14 @@
                 _mue_shift,
                 self._hbar,
                 self._m_atom,
                 self._g)
 
             n_local = n_local + 1
 
-    def init_time_evolution(self, t_final, dt):
-
-        self._t_final = t_final / self._units.unit_time
-        self._dt = dt / self._units.unit_time
-
-        self._n_time_steps = int(np.round(self._t_final / self._dt))
-
-        self._n_times = self._n_time_steps + 1
-
-        assert (np.abs(self._n_time_steps * self._dt - self._t_final)) < 1e-14
-
-        self._times = self._dt * np.arange(self._n_times)
-
-        assert (np.abs(self._times[-1] - self._t_final)) < 1e-14
-
     @property
     def x(self):
         return self._units.unit_length * self._x.cpu().numpy()
 
     @property
     def dx(self):
         return self._units.unit_length * self._dx
@@ -228,15 +229,15 @@
 
     @property
     def psi(self):
         return self._units.unit_wave_function * self._psi.cpu().numpy()
 
     @psi.setter
     def psi(self, value):
-        self._psi = torch.tensor(value / self._units.unit_wave_function, device=self.device)
+        self._psi = torch.tensor(value / self._units.unit_wave_function, device=self._device)
 
     @property
     def V(self):
         return self._units.unit_energy * self._V.cpu().numpy()
 
     def compute_n_atoms(self):
         return qsolve_core_gpe_1d.compute_n_atoms(self._psi, self._dx)
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/chemical_potential.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/chemical_potential.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,38 +1,40 @@
-from qsolve.core import qsolve_core_gpe_2d
+from qsolve.core import qsolve_core_gpe_3d
 
 
 def compute_chemical_potential(self, identifier, kwargs):
 
     if "units" in kwargs:
 
         units = kwargs["units"]
 
     else:
 
         units = "si_units"
 
     if identifier == "psi":
 
-        mue = qsolve_core_gpe_2d.compute_chemical_potential(
+        mue = qsolve_core_gpe_3d.compute_chemical_potential(
             self.psi,
             self.V,
             self.dx,
             self.dy,
+            self.dz,
             self.hbar,
             self.m_atom,
             self.g)
 
     elif identifier == "psi_0":
 
-        mue = qsolve_core_gpe_2d.compute_chemical_potential(
+        mue = qsolve_core_gpe_3d.compute_chemical_potential(
             self.psi_0,
             self.V,
             self.dx,
             self.dy,
+            self.dz,
             self.hbar,
             self.m_atom,
             self.g)
 
     else:
 
         message = 'compute_chemical_potential(self, identifier, **kwargs): ' \
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/compute_ground_state_solution.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/compute_ground_state_solution.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from qsolve.core import qsolve_core_gpe_2d
+from qsolve.core import qsolve_core_gpe_3d
 
 
 def compute_ground_state_solution(self, kwargs):
 
     tau = kwargs["tau"] / self.units.unit_time
 
     n_iter = kwargs["n_iter"]
@@ -19,18 +19,19 @@
 
     else:
 
         adaptive_tau = True
 
     N = kwargs["N"]
 
-    psi_0, vec_res, vec_iter = qsolve_core_gpe_2d.compute_ground_state_solution(
+    psi_0, vec_res, vec_iter = qsolve_core_gpe_3d.compute_ground_state_solution(
         self.V,
         self.dx,
         self.dy,
+        self.dz,
         tau,
         adaptive_tau,
         n_iter,
         N,
         self.hbar,
         self.m_atom,
         self.g)
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/densities.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/densities.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_device.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_device.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_grid_2d.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_grid_3d.py`

 * *Files 25% similar despite different names*

```diff
@@ -9,39 +9,53 @@
 
     self.x_min = kwargs['x_min'] / self.units.unit_length
     self.x_max = kwargs['x_max'] / self.units.unit_length
 
     self.y_min = kwargs['y_min'] / self.units.unit_length
     self.y_max = kwargs['y_max'] / self.units.unit_length
 
+    self.z_min = kwargs['z_min'] / self.units.unit_length
+    self.z_max = kwargs['z_max'] / self.units.unit_length
+
     self.Jx = kwargs['Jx']
     self.Jy = kwargs['Jy']
+    self.Jz = kwargs['Jz']
 
     prime_factors_Jx = get_prime_factors(self.Jx)
     prime_factors_Jy = get_prime_factors(self.Jy)
+    prime_factors_Jz = get_prime_factors(self.Jz)
 
     assert (np.max(prime_factors_Jx) < 11)
     assert (np.max(prime_factors_Jy) < 11)
+    assert (np.max(prime_factors_Jz) < 11)
 
     assert (self.Jx % 2 == 0)
     assert (self.Jy % 2 == 0)
+    assert (self.Jz % 2 == 0)
 
     x = np.linspace(self.x_min, self.x_max, self.Jx, endpoint=False)
     y = np.linspace(self.y_min, self.y_max, self.Jy, endpoint=False)
+    z = np.linspace(self.z_min, self.z_max, self.Jz, endpoint=False)
 
     self.index_center_x = np.argmin(np.abs(x))
     self.index_center_y = np.argmin(np.abs(y))
+    self.index_center_z = np.argmin(np.abs(z))
 
     assert (np.abs(x[self.index_center_x]) < 1e-14)
     assert (np.abs(y[self.index_center_y]) < 1e-14)
+    assert (np.abs(z[self.index_center_z]) < 1e-14)
 
     self.dx = x[1] - x[0]
     self.dy = y[1] - y[0]
+    self.dz = z[1] - z[0]
 
     self.Lx = self.Jx * self.dx
     self.Ly = self.Jy * self.dy
+    self.Lz = self.Jz * self.dz
 
     self.x = torch.tensor(x, dtype=torch.float64, device=self.device)
     self.y = torch.tensor(y, dtype=torch.float64, device=self.device)
+    self.z = torch.tensor(z, dtype=torch.float64, device=self.device)
 
-    self.x_2d = torch.reshape(self.x, (self.Jx, 1))
-    self.y_2d = torch.reshape(self.y, (1, self.Jy))
+    self.x_3d = torch.reshape(self.x, (self.Jx, 1, 1))
+    self.y_3d = torch.reshape(self.y, (1, self.Jy, 1))
+    self.z_3d = torch.reshape(self.z, (1, 1, self.Jz))
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_potential.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_potential.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 def init_potential(self, Potential, params_user):
 
     params_solver = {
-        "x_2d": self.x_2d,
-        "y_2d": self.y_2d,
+        "x_3d": self.x_3d,
+        "y_3d": self.y_3d,
+        "z_3d": self.z_3d,
         "Lx": self.Lx,
         "Ly": self.Ly,
+        "Lz": self.Lz,
         "hbar": self.hbar,
         "mu_B": self.mu_B,
         "m_atom": self.m_atom,
         "unit_length": self.units.unit_length,
         "unit_time": self.units.unit_time,
         "unit_mass": self.units.unit_mass,
         "unit_energy": self.units.unit_energy,
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/spectrum.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/spectrum.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_2d/solver_gpe_2d/units.py` & `qsolve-0.3.1/src/qsolve/units_backup/units_2d.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-from math import sqrt
+import math
 
 
-class Units(object):
+class Units2D(object):
 
     def __init__(self, unit_length, unit_time, unit_mass, unit_electric_current, unit_temperature):
 
         self.unit_length = unit_length
 
         self.unit_mass = unit_mass
 
@@ -15,21 +15,16 @@
 
         self.unit_temperature = unit_temperature
 
         self.unit_frequency = 1.0 / unit_time
 
         self.unit_energy = unit_mass * (unit_length * unit_length) / (unit_time * unit_time)
 
-        # self.unit_wave_function = 1.0 / sqrt(unit_length * unit_length * unit_length)
-        self.unit_wave_function = 1.0 / sqrt(unit_length * unit_length)
-
-        # self.unit_density = 1.0 / (unit_length * unit_length * unit_length)
         self.unit_density = 1.0 / (unit_length * unit_length)
 
+        self.unit_wave_function = math.sqrt(self.unit_density)
+
         self.unit_hbar = (unit_mass * unit_length * unit_length) / unit_time
 
         self.unit_bohr_magneton = unit_length * unit_length * unit_electric_current
 
         self.unit_k_B = unit_mass * unit_length * unit_length / (unit_time * unit_time * unit_temperature)
-
-        self.unit_g = unit_mass * (unit_length * unit_length * unit_length
-                                   * unit_length * unit_length) / (unit_time * unit_time)
```

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/energies.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/energies.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/getter_functions.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/getter_functions.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_units.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/init_units.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/solver_gpe_3d.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/solver_gpe_3d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/solvers/solvers_3d/solver_gpe_3d/units.py` & `qsolve-0.3.1/src/qsolve/solvers/solvers_3d/solver_gpe_3d/units.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/units.py` & `qsolve-0.3.1/src/qsolve/units.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/units_backup/units_1d.py` & `qsolve-0.3.1/src/qsolve/units_backup/units_1d.py`

 * *Files identical despite different names*

### Comparing `qsolve-0.3.0/src/qsolve/units_backup/units_2d.py` & `qsolve-0.3.1/src/qsolve/units_backup/units_3d.py`

 * *Files 14% similar despite different names*

```diff
@@ -15,16 +15,22 @@
 
         self.unit_temperature = unit_temperature
 
         self.unit_frequency = 1.0 / unit_time
 
         self.unit_energy = unit_mass * (unit_length * unit_length) / (unit_time * unit_time)
 
-        self.unit_density = 1.0 / (unit_length * unit_length)
+        self.unit_density = 1.0 / (unit_length * unit_length * unit_length)
 
         self.unit_wave_function = math.sqrt(self.unit_density)
 
         self.unit_hbar = (unit_mass * unit_length * unit_length) / unit_time
 
         self.unit_bohr_magneton = unit_length * unit_length * unit_electric_current
 
         self.unit_k_B = unit_mass * unit_length * unit_length / (unit_time * unit_time * unit_temperature)
+
+        self.unit_g = unit_mass * (unit_length * unit_length * unit_length
+                                   * unit_length * unit_length) / (unit_time * unit_time)
+
+        # d = 3
+        # self.unit_g = self.unit_energy * unit_length ** d
```

### Comparing `qsolve-0.3.0/src/qsolve.egg-info/SOURCES.txt` & `qsolve-0.3.1/src/qsolve.egg-info/SOURCES.txt`

 * *Files 25% similar despite different names*

```diff
@@ -7,18 +7,18 @@
 src/qsolve/primes.py
 src/qsolve/units.py
 src/qsolve.egg-info/PKG-INFO
 src/qsolve.egg-info/SOURCES.txt
 src/qsolve.egg-info/dependency_links.txt
 src/qsolve.egg-info/top_level.txt
 src/qsolve/core/__init__.py
-src/qsolve/core/fourier.pyc
-src/qsolve/core/qsolve_core_gpe_1d.pyc
-src/qsolve/core/qsolve_core_gpe_2d.pyc
-src/qsolve/core/qsolve_core_gpe_3d.pyc
+src/qsolve/core/fourier.cpython-310-x86_64-linux-gnu.so
+src/qsolve/core/qsolve_core_gpe_1d.cpython-310-x86_64-linux-gnu.so
+src/qsolve/core/qsolve_core_gpe_2d.cpython-310-x86_64-linux-gnu.so
+src/qsolve/core/qsolve_core_gpe_3d.cpython-310-x86_64-linux-gnu.so
 src/qsolve/figures/__init__.py
 src/qsolve/figures/figure_main_1d/__init__.py
 src/qsolve/figures/figure_main_1d/fig_control_inputs.py
 src/qsolve/figures/figure_main_1d/fig_psi_abs_squared_1d.py
 src/qsolve/figures/figure_main_1d/fig_psi_re_im_1d.py
 src/qsolve/figures/figure_main_1d/figure_main_1d.py
 src/qsolve/figures/style/__init__.py
@@ -61,30 +61,15 @@
 src/qsolve/potentials/components_3d/lesanovsky_3d.py
 src/qsolve/potentials/components_3d/lesanovsky_xy_3d.py
 src/qsolve/potentials/components_3d/tilt_x_3d.py
 src/qsolve/solvers/__init__.py
 src/qsolve/solvers/solvers_1d/__init__.py
 src/qsolve/solvers/solvers_1d/solver_gpe_1d.py
 src/qsolve/solvers/solvers_2d/__init__.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/__init__.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/chemical_potential.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/compute_ground_state_solution.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/densities.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/energies.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/getter_functions.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_device.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_grid_2d.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_potential.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/init_time_evolution.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/n_atoms.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/set_V.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/set_psi.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/solver_gpe_2d.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/spectrum.py
-src/qsolve/solvers/solvers_2d/solver_gpe_2d/units.py
+src/qsolve/solvers/solvers_2d/solver_gpe_2d.py
 src/qsolve/solvers/solvers_3d/__init__.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/__init__.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/check_python_version.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/chemical_potential.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/compute_ground_state_solution.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/densities.py
 src/qsolve/solvers/solvers_3d/solver_gpe_3d/energies.py
```

