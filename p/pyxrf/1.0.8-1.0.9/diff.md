# Comparing `tmp/pyxrf-1.0.8.tar.gz` & `tmp/pyxrf-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyxrf-1.0.8.tar", last modified: Fri Oct  1 20:11:54 2021, max compression
+gzip compressed data, was "pyxrf-1.0.9.tar", last modified: Wed Oct 20 17:42:17 2021, max compression
```

## Comparing `pyxrf-1.0.8.tar` & `pyxrf-1.0.9.tar`

### file list

```diff
@@ -1,147 +1,147 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1538 2021-10-01 20:11:42.000000 pyxrf-1.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)      345 2021-10-01 20:11:42.000000 pyxrf-1.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)      535 2021-10-01 20:11:54.066418 pyxrf-1.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1177 2021-10-01 20:11:42.000000 pyxrf-1.0.8/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.046418 pyxrf-1.0.8/configs/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      455 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/hxn_pv_config.json
--rw-r--r--   0 runner    (1001) docker     (121)      306 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/pv_config.json
--rw-r--r--   0 runner    (1001) docker     (121)      330 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/srx_pv_config-original.json
--rw-r--r--   0 runner    (1001) docker     (121)      436 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/srx_pv_config.json
--rw-r--r--   0 runner    (1001) docker     (121)      230 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/tes_pv_config.json
--rw-r--r--   0 runner    (1001) docker     (121)      195 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/xfm_pv_config.json
--rw-r--r--   0 runner    (1001) docker     (121)     7375 2021-10-01 20:11:42.000000 pyxrf-1.0.8/configs/xrf_parameter.json
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.050418 pyxrf-1.0.8/docs/
--rw-r--r--   0 runner    (1001) docker     (121)      602 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.050418 pyxrf-1.0.8/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (121)   117863 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/define_h5file.jpg
--rw-r--r--   0 runner    (1001) docker     (121)   203384 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/define_h5file.pdf
--rw-r--r--   0 runner    (1001) docker     (121)   645824 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/define_h5file.png
--rw-r--r--   0 runner    (1001) docker     (121)   687410 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/load_parameter_file.png
--rw-r--r--   0 runner    (1001) docker     (121)   351569 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/more_datasets.png
--rw-r--r--   0 runner    (1001) docker     (121)   148489 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/select_data_plot.png
--rw-r--r--   0 runner    (1001) docker     (121)   979052 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/_static/zoomin_plot.png
--rw-r--r--   0 runner    (1001) docker     (121)     4664 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (121)      420 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/credits.rst
--rw-r--r--   0 runner    (1001) docker     (121)     2441 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/data_input.rst
--rw-r--r--   0 runner    (1001) docker     (121)      285 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/data_output.rst
--rw-r--r--   0 runner    (1001) docker     (121)     1701 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (121)     3298 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/installation.rst
--rw-r--r--   0 runner    (1001) docker     (121)      808 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (121)      912 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/questions.rst
--rw-r--r--   0 runner    (1001) docker     (121)     3616 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/summed_spectrum_fit.rst
--rw-r--r--   0 runner    (1001) docker     (121)     3625 2021-10-01 20:11:42.000000 pyxrf-1.0.8/docs/work_at_beamlines.rst
--rw-r--r--   0 runner    (1001) docker     (121)      372 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.070418 pyxrf-1.0.8/pyxrf/
--rw-r--r--   0 runner    (1001) docker     (121)      210 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      471 2021-10-01 20:11:54.070418 pyxrf-1.0.8/pyxrf/_version.py
--rw-r--r--   0 runner    (1001) docker     (121)     1216 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/api.py
--rw-r--r--   0 runner    (1001) docker     (121)     1937 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/api_dev.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.054417 pyxrf-1.0.8/pyxrf/core/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    15011 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/fitting.py
--rw-r--r--   0 runner    (1001) docker     (121)    46348 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/map_processing.py
--rw-r--r--   0 runner    (1001) docker     (121)    77442 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/quant_analysis.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.058418 pyxrf-1.0.8/pyxrf/core/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    23140 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/test_fitting.py
--rw-r--r--   0 runner    (1001) docker     (121)    49145 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/test_map_processing.py
--rw-r--r--   0 runner    (1001) docker     (121)    47273 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/test_quant_analysis.py
--rw-r--r--   0 runner    (1001) docker     (121)     7919 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/test_xrf_utils.py
--rw-r--r--   0 runner    (1001) docker     (121)    16245 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/tests/test_yaml_param_files.py
--rw-r--r--   0 runner    (1001) docker     (121)    10665 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/utils.py
--rw-r--r--   0 runner    (1001) docker     (121)     7280 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/xrf_quant_standards.yaml
--rw-r--r--   0 runner    (1001) docker     (121)    11609 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/xrf_utils.py
--rw-r--r--   0 runner    (1001) docker     (121)    15002 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/core/yaml_param_files.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.058418 pyxrf-1.0.8/pyxrf/db_config/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/db_config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      482 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/db_config/hxn_db_config.py
--rw-r--r--   0 runner    (1001) docker     (121)     2041 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/db_config/srx_db_config.py
--rw-r--r--   0 runner    (1001) docker     (121)      871 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/db_config/tes_db_config.py
--rw-r--r--   0 runner    (1001) docker     (121)     1477 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/db_config/xfm_db_config.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.062418 pyxrf-1.0.8/pyxrf/gui_module/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1840 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/central_widget.py
--rw-r--r--   0 runner    (1001) docker     (121)     5137 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_edit_user_peak_parameters.py
--rw-r--r--   0 runner    (1001) docker     (121)    11868 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_export_to_tiff_and_txt.py
--rw-r--r--   0 runner    (1001) docker     (121)    16486 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_find_elements.py
--rw-r--r--   0 runner    (1001) docker     (121)    15522 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_load_mask.py
--rw-r--r--   0 runner    (1001) docker     (121)     1626 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_new_user_peak.py
--rw-r--r--   0 runner    (1001) docker     (121)     6189 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_pileup_peak_parameters.py
--rw-r--r--   0 runner    (1001) docker     (121)     2507 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_plot_escape_peak.py
--rw-r--r--   0 runner    (1001) docker     (121)     7411 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_save_calibration.py
--rw-r--r--   0 runner    (1001) docker     (121)     6118 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_select_quant_standard.py
--rw-r--r--   0 runner    (1001) docker     (121)     5190 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_select_scan.py
--rw-r--r--   0 runner    (1001) docker     (121)     1266 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_view_calib_standard.py
--rw-r--r--   0 runner    (1001) docker     (121)      756 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/dlg_view_metadata.py
--rw-r--r--   0 runner    (1001) docker     (121)      313 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/form_base_widget.py
--rw-r--r--   0 runner    (1001) docker     (121)     2012 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/left_panel.py
--rw-r--r--   0 runner    (1001) docker     (121)    28005 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/main_window.py
--rw-r--r--   0 runner    (1001) docker     (121)     2837 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/right_panel.py
--rw-r--r--   0 runner    (1001) docker     (121)    22375 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_fit_maps.py
--rw-r--r--   0 runner    (1001) docker     (121)    24591 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_load_data.py
--rw-r--r--   0 runner    (1001) docker     (121)    26338 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_model.py
--rw-r--r--   0 runner    (1001) docker     (121)     9131 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_fitting_model.py
--rw-r--r--   0 runner    (1001) docker     (121)     1248 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_preview.py
--rw-r--r--   0 runner    (1001) docker     (121)     8557 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_rgb_maps.py
--rw-r--r--   0 runner    (1001) docker     (121)     9016 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_xrf_maps.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.062418 pyxrf-1.0.8/pyxrf/gui_module/tests/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      801 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_main_window.py
--rw-r--r--   0 runner    (1001) docker     (121)    26978 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_useful_widgets.py
--rw-r--r--   0 runner    (1001) docker     (121)     2232 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_wd_image_wizard.py
--rw-r--r--   0 runner    (1001) docker     (121)    12574 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_wd_load_data.py
--rw-r--r--   0 runner    (1001) docker     (121)     3994 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_wnd_load_quant_calibration.py
--rw-r--r--   0 runner    (1001) docker     (121)      696 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/tests/test_wnd_manage_emission_lines.py
--rw-r--r--   0 runner    (1001) docker     (121)    39683 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/useful_widgets.py
--rw-r--r--   0 runner    (1001) docker     (121)     5829 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wd_preview_plot_count.py
--rw-r--r--   0 runner    (1001) docker     (121)     5082 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wd_preview_plot_spectrum.py
--rw-r--r--   0 runner    (1001) docker     (121)    13746 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wd_rgb_selection.py
--rw-r--r--   0 runner    (1001) docker     (121)    18104 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_compute_roi_maps.py
--rw-r--r--   0 runner    (1001) docker     (121)    18066 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_detailed_fitting_params.py
--rw-r--r--   0 runner    (1001) docker     (121)    21275 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_general_settings_for_fitting.py
--rw-r--r--   0 runner    (1001) docker     (121)    12287 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_image_wizard.py
--rw-r--r--   0 runner    (1001) docker     (121)    21729 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_load_quant_calibration.py
--rw-r--r--   0 runner    (1001) docker     (121)    32675 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_module/wnd_manage_emission_lines.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.062418 pyxrf-1.0.8/pyxrf/gui_support/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_support/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    82188 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_support/gpc_class.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/pyxrf/gui_support/tests/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_support/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     4020 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/gui_support/tests/test_gpc_class.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/pyxrf/model/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    36735 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/command_tools.py
--rw-r--r--   0 runner    (1001) docker     (121)     5228 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/data_to_analysis_store.py
--rw-r--r--   0 runner    (1001) docker     (121)    33762 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/draw_image.py
--rw-r--r--   0 runner    (1001) docker     (121)    31070 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/draw_image_rgb.py
--rw-r--r--   0 runner    (1001) docker     (121)    91374 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/fileio.py
--rw-r--r--   0 runner    (1001) docker     (121)    77535 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/fit_spectrum.py
--rw-r--r--   0 runner    (1001) docker     (121)    78757 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/lineplot.py
--rw-r--r--   0 runner    (1001) docker     (121)    97330 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/load_data_from_db.py
--rw-r--r--   0 runner    (1001) docker     (121)     6943 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/param_data.py
--rw-r--r--   0 runner    (1001) docker     (121)    57227 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/parameters.py
--rw-r--r--   0 runner    (1001) docker     (121)    13148 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/roi_model.py
--rw-r--r--   0 runner    (1001) docker     (121)     8538 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/scan_metadata.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/pyxrf/model/tests/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5983 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/model/tests/test_hdf5_file_operations.py
--rw-r--r--   0 runner    (1001) docker     (121)     4613 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/pyxrf_run.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/pyxrf/simulation/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/simulation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    27002 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/simulation/sim_xrf_scan_data.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.066418 pyxrf-1.0.8/pyxrf/xanes_maps/
--rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/xanes_maps/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)   149281 2021-10-01 20:11:42.000000 pyxrf-1.0.8/pyxrf/xanes_maps/xanes_maps_api.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-01 20:11:54.054417 pyxrf-1.0.8/pyxrf.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)      535 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     4040 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       47 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)      181 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       14 2021-10-01 20:11:53.000000 pyxrf-1.0.8/pyxrf.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)      170 2021-10-01 20:11:42.000000 pyxrf-1.0.8/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (121)      169 2021-10-01 20:11:54.066418 pyxrf-1.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      984 2021-10-01 20:11:42.000000 pyxrf-1.0.8/setup.py
--rw-r--r--   0 runner    (1001) docker     (121)    62474 2021-10-01 20:11:42.000000 pyxrf-1.0.8/versioneer.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     1538 2021-10-20 17:42:05.000000 pyxrf-1.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)      345 2021-10-20 17:42:05.000000 pyxrf-1.0.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)      535 2021-10-20 17:42:17.724420 pyxrf-1.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     1177 2021-10-20 17:42:05.000000 pyxrf-1.0.9/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.708420 pyxrf-1.0.9/configs/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      455 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/hxn_pv_config.json
+-rw-r--r--   0 runner    (1001) docker     (121)      306 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/pv_config.json
+-rw-r--r--   0 runner    (1001) docker     (121)      330 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/srx_pv_config-original.json
+-rw-r--r--   0 runner    (1001) docker     (121)      436 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/srx_pv_config.json
+-rw-r--r--   0 runner    (1001) docker     (121)      230 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/tes_pv_config.json
+-rw-r--r--   0 runner    (1001) docker     (121)      195 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/xfm_pv_config.json
+-rw-r--r--   0 runner    (1001) docker     (121)     7375 2021-10-20 17:42:05.000000 pyxrf-1.0.9/configs/xrf_parameter.json
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.708420 pyxrf-1.0.9/docs/
+-rw-r--r--   0 runner    (1001) docker     (121)      602 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.712420 pyxrf-1.0.9/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (121)   117863 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/define_h5file.jpg
+-rw-r--r--   0 runner    (1001) docker     (121)   203384 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/define_h5file.pdf
+-rw-r--r--   0 runner    (1001) docker     (121)   645824 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/define_h5file.png
+-rw-r--r--   0 runner    (1001) docker     (121)   687410 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/load_parameter_file.png
+-rw-r--r--   0 runner    (1001) docker     (121)   351569 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/more_datasets.png
+-rw-r--r--   0 runner    (1001) docker     (121)   148489 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/select_data_plot.png
+-rw-r--r--   0 runner    (1001) docker     (121)   979052 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/_static/zoomin_plot.png
+-rw-r--r--   0 runner    (1001) docker     (121)     4664 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (121)      420 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/credits.rst
+-rw-r--r--   0 runner    (1001) docker     (121)     2441 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/data_input.rst
+-rw-r--r--   0 runner    (1001) docker     (121)      285 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/data_output.rst
+-rw-r--r--   0 runner    (1001) docker     (121)     1701 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (121)     3298 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/installation.rst
+-rw-r--r--   0 runner    (1001) docker     (121)      808 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (121)      912 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/questions.rst
+-rw-r--r--   0 runner    (1001) docker     (121)     3616 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/summed_spectrum_fit.rst
+-rw-r--r--   0 runner    (1001) docker     (121)     3625 2021-10-20 17:42:05.000000 pyxrf-1.0.9/docs/work_at_beamlines.rst
+-rw-r--r--   0 runner    (1001) docker     (121)      372 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/
+-rw-r--r--   0 runner    (1001) docker     (121)      210 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      471 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/_version.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1216 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/api.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1937 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/api_dev.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.716420 pyxrf-1.0.9/pyxrf/core/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    15011 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/fitting.py
+-rw-r--r--   0 runner    (1001) docker     (121)    46348 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/map_processing.py
+-rw-r--r--   0 runner    (1001) docker     (121)    77442 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/quant_analysis.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.716420 pyxrf-1.0.9/pyxrf/core/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23140 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/test_fitting.py
+-rw-r--r--   0 runner    (1001) docker     (121)    49145 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/test_map_processing.py
+-rw-r--r--   0 runner    (1001) docker     (121)    47273 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/test_quant_analysis.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7919 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/test_xrf_utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)    16245 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/tests/test_yaml_param_files.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10665 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7280 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/xrf_quant_standards.yaml
+-rw-r--r--   0 runner    (1001) docker     (121)    11609 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/xrf_utils.py
+-rw-r--r--   0 runner    (1001) docker     (121)    15002 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/core/yaml_param_files.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.716420 pyxrf-1.0.9/pyxrf/db_config/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/db_config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      482 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/db_config/hxn_db_config.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2041 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/db_config/srx_db_config.py
+-rw-r--r--   0 runner    (1001) docker     (121)      871 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/db_config/tes_db_config.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1477 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/db_config/xfm_db_config.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.720420 pyxrf-1.0.9/pyxrf/gui_module/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1840 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/central_widget.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5137 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_edit_user_peak_parameters.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11868 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_export_to_tiff_and_txt.py
+-rw-r--r--   0 runner    (1001) docker     (121)    16486 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_find_elements.py
+-rw-r--r--   0 runner    (1001) docker     (121)    15522 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_load_mask.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1626 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_new_user_peak.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6189 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_pileup_peak_parameters.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2507 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_plot_escape_peak.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7411 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_save_calibration.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6118 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_select_quant_standard.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5190 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_select_scan.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1266 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_view_calib_standard.py
+-rw-r--r--   0 runner    (1001) docker     (121)      756 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/dlg_view_metadata.py
+-rw-r--r--   0 runner    (1001) docker     (121)      313 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/form_base_widget.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2012 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/left_panel.py
+-rw-r--r--   0 runner    (1001) docker     (121)    28005 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/main_window.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2837 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/right_panel.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22375 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_fit_maps.py
+-rw-r--r--   0 runner    (1001) docker     (121)    24591 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_load_data.py
+-rw-r--r--   0 runner    (1001) docker     (121)    26338 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_model.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9131 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_fitting_model.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1248 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_preview.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8557 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_rgb_maps.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9016 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_xrf_maps.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.720420 pyxrf-1.0.9/pyxrf/gui_module/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      801 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_main_window.py
+-rw-r--r--   0 runner    (1001) docker     (121)    26978 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_useful_widgets.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2232 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_wd_image_wizard.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12574 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_wd_load_data.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3994 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_wnd_load_quant_calibration.py
+-rw-r--r--   0 runner    (1001) docker     (121)      696 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/tests/test_wnd_manage_emission_lines.py
+-rw-r--r--   0 runner    (1001) docker     (121)    39683 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/useful_widgets.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5829 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wd_preview_plot_count.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5082 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wd_preview_plot_spectrum.py
+-rw-r--r--   0 runner    (1001) docker     (121)    13746 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wd_rgb_selection.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18104 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_compute_roi_maps.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18066 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_detailed_fitting_params.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21275 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_general_settings_for_fitting.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12287 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_image_wizard.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21729 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_load_quant_calibration.py
+-rw-r--r--   0 runner    (1001) docker     (121)    32675 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_module/wnd_manage_emission_lines.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.720420 pyxrf-1.0.9/pyxrf/gui_support/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_support/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    82188 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_support/gpc_class.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.720420 pyxrf-1.0.9/pyxrf/gui_support/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_support/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4020 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/gui_support/tests/test_gpc_class.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/model/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    36735 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/command_tools.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5228 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/data_to_analysis_store.py
+-rw-r--r--   0 runner    (1001) docker     (121)    33762 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/draw_image.py
+-rw-r--r--   0 runner    (1001) docker     (121)    31070 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/draw_image_rgb.py
+-rw-r--r--   0 runner    (1001) docker     (121)    91374 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/fileio.py
+-rw-r--r--   0 runner    (1001) docker     (121)    77535 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/fit_spectrum.py
+-rw-r--r--   0 runner    (1001) docker     (121)    78757 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/lineplot.py
+-rw-r--r--   0 runner    (1001) docker     (121)    97330 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/load_data_from_db.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6943 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/param_data.py
+-rw-r--r--   0 runner    (1001) docker     (121)    57227 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/parameters.py
+-rw-r--r--   0 runner    (1001) docker     (121)    13148 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/roi_model.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8538 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/scan_metadata.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/model/tests/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5983 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/model/tests/test_hdf5_file_operations.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4613 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/pyxrf_run.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/simulation/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/simulation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    27002 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/simulation/sim_xrf_scan_data.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.724420 pyxrf-1.0.9/pyxrf/xanes_maps/
+-rw-r--r--   0 runner    (1001) docker     (121)       53 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/xanes_maps/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)   149330 2021-10-20 17:42:05.000000 pyxrf-1.0.9/pyxrf/xanes_maps/xanes_maps_api.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-10-20 17:42:17.712420 pyxrf-1.0.9/pyxrf.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)      535 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     4040 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       47 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (121)      201 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       14 2021-10-20 17:42:17.000000 pyxrf-1.0.9/pyxrf.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)      190 2021-10-20 17:42:05.000000 pyxrf-1.0.9/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (121)      169 2021-10-20 17:42:17.724420 pyxrf-1.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)      984 2021-10-20 17:42:05.000000 pyxrf-1.0.9/setup.py
+-rw-r--r--   0 runner    (1001) docker     (121)    62474 2021-10-20 17:42:05.000000 pyxrf-1.0.9/versioneer.py
```

### Comparing `pyxrf-1.0.8/LICENSE` & `pyxrf-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/PKG-INFO` & `pyxrf-1.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyxrf
-Version: 1.0.8
+Version: 1.0.9
 Summary: UNKNOWN
 Home-page: https://github.com/NSLS-II/PyXRF
 Author: Brookhaven National Laboratory
 License: BSD
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `pyxrf-1.0.8/README.rst` & `pyxrf-1.0.9/README.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/configs/xrf_parameter.json` & `pyxrf-1.0.9/configs/xrf_parameter.json`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/Makefile` & `pyxrf-1.0.9/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/define_h5file.jpg` & `pyxrf-1.0.9/docs/_static/define_h5file.jpg`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/define_h5file.pdf` & `pyxrf-1.0.9/docs/_static/define_h5file.pdf`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/define_h5file.png` & `pyxrf-1.0.9/docs/_static/define_h5file.png`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/load_parameter_file.png` & `pyxrf-1.0.9/docs/_static/load_parameter_file.png`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/more_datasets.png` & `pyxrf-1.0.9/docs/_static/more_datasets.png`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/select_data_plot.png` & `pyxrf-1.0.9/docs/_static/select_data_plot.png`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/_static/zoomin_plot.png` & `pyxrf-1.0.9/docs/_static/zoomin_plot.png`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/conf.py` & `pyxrf-1.0.9/docs/conf.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/data_input.rst` & `pyxrf-1.0.9/docs/data_input.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/index.rst` & `pyxrf-1.0.9/docs/index.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/installation.rst` & `pyxrf-1.0.9/docs/installation.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/make.bat` & `pyxrf-1.0.9/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/questions.rst` & `pyxrf-1.0.9/docs/questions.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/summed_spectrum_fit.rst` & `pyxrf-1.0.9/docs/summed_spectrum_fit.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/docs/work_at_beamlines.rst` & `pyxrf-1.0.9/docs/work_at_beamlines.rst`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/api.py` & `pyxrf-1.0.9/pyxrf/api.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/api_dev.py` & `pyxrf-1.0.9/pyxrf/api_dev.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/fitting.py` & `pyxrf-1.0.9/pyxrf/core/fitting.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/map_processing.py` & `pyxrf-1.0.9/pyxrf/core/map_processing.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/quant_analysis.py` & `pyxrf-1.0.9/pyxrf/core/quant_analysis.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/tests/test_fitting.py` & `pyxrf-1.0.9/pyxrf/core/tests/test_fitting.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/tests/test_map_processing.py` & `pyxrf-1.0.9/pyxrf/core/tests/test_map_processing.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/tests/test_quant_analysis.py` & `pyxrf-1.0.9/pyxrf/core/tests/test_quant_analysis.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/tests/test_xrf_utils.py` & `pyxrf-1.0.9/pyxrf/core/tests/test_xrf_utils.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/tests/test_yaml_param_files.py` & `pyxrf-1.0.9/pyxrf/core/tests/test_yaml_param_files.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/utils.py` & `pyxrf-1.0.9/pyxrf/core/utils.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/xrf_quant_standards.yaml` & `pyxrf-1.0.9/pyxrf/core/xrf_quant_standards.yaml`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/xrf_utils.py` & `pyxrf-1.0.9/pyxrf/core/xrf_utils.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/core/yaml_param_files.py` & `pyxrf-1.0.9/pyxrf/core/yaml_param_files.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/db_config/srx_db_config.py` & `pyxrf-1.0.9/pyxrf/db_config/srx_db_config.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/db_config/tes_db_config.py` & `pyxrf-1.0.9/pyxrf/db_config/tes_db_config.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/db_config/xfm_db_config.py` & `pyxrf-1.0.9/pyxrf/db_config/xfm_db_config.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/central_widget.py` & `pyxrf-1.0.9/pyxrf/gui_module/central_widget.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_edit_user_peak_parameters.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_edit_user_peak_parameters.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_export_to_tiff_and_txt.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_export_to_tiff_and_txt.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_find_elements.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_find_elements.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_load_mask.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_load_mask.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_new_user_peak.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_new_user_peak.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_pileup_peak_parameters.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_pileup_peak_parameters.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_plot_escape_peak.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_plot_escape_peak.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_save_calibration.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_save_calibration.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_select_quant_standard.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_select_quant_standard.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_select_scan.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_select_scan.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_view_calib_standard.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_view_calib_standard.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/dlg_view_metadata.py` & `pyxrf-1.0.9/pyxrf/gui_module/dlg_view_metadata.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/left_panel.py` & `pyxrf-1.0.9/pyxrf/gui_module/left_panel.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/main_window.py` & `pyxrf-1.0.9/pyxrf/gui_module/main_window.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/right_panel.py` & `pyxrf-1.0.9/pyxrf/gui_module/right_panel.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_fit_maps.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_fit_maps.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_load_data.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_load_data.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_model.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_model.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_fitting_model.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_fitting_model.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_preview.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_preview.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_rgb_maps.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_rgb_maps.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tab_wd_plots_xrf_maps.py` & `pyxrf-1.0.9/pyxrf/gui_module/tab_wd_plots_xrf_maps.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_main_window.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_main_window.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_useful_widgets.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_useful_widgets.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_wd_image_wizard.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_wd_image_wizard.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_wd_load_data.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_wd_load_data.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_wnd_load_quant_calibration.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_wnd_load_quant_calibration.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/tests/test_wnd_manage_emission_lines.py` & `pyxrf-1.0.9/pyxrf/gui_module/tests/test_wnd_manage_emission_lines.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/useful_widgets.py` & `pyxrf-1.0.9/pyxrf/gui_module/useful_widgets.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wd_preview_plot_count.py` & `pyxrf-1.0.9/pyxrf/gui_module/wd_preview_plot_count.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wd_preview_plot_spectrum.py` & `pyxrf-1.0.9/pyxrf/gui_module/wd_preview_plot_spectrum.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wd_rgb_selection.py` & `pyxrf-1.0.9/pyxrf/gui_module/wd_rgb_selection.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_compute_roi_maps.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_compute_roi_maps.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_detailed_fitting_params.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_detailed_fitting_params.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_general_settings_for_fitting.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_general_settings_for_fitting.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_image_wizard.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_image_wizard.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_load_quant_calibration.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_load_quant_calibration.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_module/wnd_manage_emission_lines.py` & `pyxrf-1.0.9/pyxrf/gui_module/wnd_manage_emission_lines.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_support/gpc_class.py` & `pyxrf-1.0.9/pyxrf/gui_support/gpc_class.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/gui_support/tests/test_gpc_class.py` & `pyxrf-1.0.9/pyxrf/gui_support/tests/test_gpc_class.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/command_tools.py` & `pyxrf-1.0.9/pyxrf/model/command_tools.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/data_to_analysis_store.py` & `pyxrf-1.0.9/pyxrf/model/data_to_analysis_store.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/draw_image.py` & `pyxrf-1.0.9/pyxrf/model/draw_image.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/draw_image_rgb.py` & `pyxrf-1.0.9/pyxrf/model/draw_image_rgb.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/fileio.py` & `pyxrf-1.0.9/pyxrf/model/fileio.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/fit_spectrum.py` & `pyxrf-1.0.9/pyxrf/model/fit_spectrum.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/lineplot.py` & `pyxrf-1.0.9/pyxrf/model/lineplot.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/load_data_from_db.py` & `pyxrf-1.0.9/pyxrf/model/load_data_from_db.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/param_data.py` & `pyxrf-1.0.9/pyxrf/model/param_data.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/parameters.py` & `pyxrf-1.0.9/pyxrf/model/parameters.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/roi_model.py` & `pyxrf-1.0.9/pyxrf/model/roi_model.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/scan_metadata.py` & `pyxrf-1.0.9/pyxrf/model/scan_metadata.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/model/tests/test_hdf5_file_operations.py` & `pyxrf-1.0.9/pyxrf/model/tests/test_hdf5_file_operations.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/pyxrf_run.py` & `pyxrf-1.0.9/pyxrf/pyxrf_run.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/simulation/sim_xrf_scan_data.py` & `pyxrf-1.0.9/pyxrf/simulation/sim_xrf_scan_data.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/pyxrf/xanes_maps/xanes_maps_api.py` & `pyxrf-1.0.9/pyxrf/xanes_maps/xanes_maps_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -2506,16 +2506,16 @@
             self.ax_img_stack = plt.axes([0.07, 0.25, 0.35, 0.65])
             self.ax_img_cbar = plt.axes([0.425, 0.26, 0.013, 0.63])
             self.ax_fluor_plot = plt.axes([0.55, 0.25, 0.4, 0.65])
             self.fig.subplots_adjust(left=0.07, right=0.95, bottom=0.25)
 
             self.t_bar = plt.get_current_fig_manager().toolbar
 
-            x_label = "X, {axes_units}" if axes_units else "X"
-            y_label = "Y, {axes_units}" if axes_units else "Y"
+            x_label = f"X, {axes_units}" if axes_units else "X"
+            y_label = f"Y, {axes_units}" if axes_units else "Y"
             self.ax_img_stack.set_xlabel(x_label, fontsize=self.label_fontsize)
             self.ax_img_stack.set_ylabel(y_label, fontsize=self.label_fontsize)
 
             # Compute parameters of the arrow (width and length), used to mark
             #   selected point on the image plot
             max_dim = max(abs(self.pos_x_max - self.pos_x_min), abs(self.pos_y_max - self.pos_y_min))
             self.arr_width = max_dim / 200
@@ -2998,16 +2998,16 @@
     if (positions_x is None) or (positions_y is None):
         positions_x = range(nx)
         positions_y = range(ny)
         axes_units = "pixels"
     else:
         axes_units = axes_units if axes_units else ""
 
-    x_label = "X, {axes_units}" if axes_units else "X"
-    y_label = "Y, {axes_units}" if axes_units else "Y"
+    x_label = f"X, {axes_units}" if axes_units else "X"
+    y_label = f"Y, {axes_units}" if axes_units else "Y"
 
     # Find max and min values. The margins are likely to contain strong artifacts that distort images.
     c = max(map_margin / 100.0, 0)  # Make sure it is positive
     x_margin, y_margin = int(nx * c), int(ny * c)
     vmin = np.min(map_data[y_margin : ny - y_margin, x_margin : nx - x_margin])
     vmax = np.max(map_data[y_margin : ny - y_margin, x_margin : nx - x_margin])
 
@@ -3017,21 +3017,22 @@
     label_fig_title = label_fig_title.replace("_", "")
 
     if label:
         fig_title = f"XANES map: {label_fig_title}"
         img_title = f"XANES map: {label}"
 
     fig = plt.figure(figsize=(6, 6), num=fig_title)
+    ax = fig.subplots()
 
     # display image
     extent = [positions_x[0], positions_x[-1], positions_y[-1], positions_y[0]]
-    img_plot = plt.imshow(map_data, vmin=vmin, vmax=vmax, origin="upper", extent=extent)
+    img_plot = ax.imshow(map_data, vmin=vmin, vmax=vmax, origin="upper", extent=extent)
     plt.colorbar(img_plot, orientation="vertical")
-    plt.axes().set_xlabel(x_label, fontsize=15)
-    plt.axes().set_ylabel(y_label, fontsize=15)
+    ax.get_xaxis().set_label_text(x_label, fontsize=15)
+    ax.get_yaxis().set_label_text(y_label, fontsize=15)
     fig.suptitle(img_title, fontsize=20)
     plt.show(block=block)
     return fig
 
 
 def plot_absorption_references(
     *, ref_energy, ref_data, scan_energies, scan_absorption_refs, ref_labels=None, block=True
@@ -3070,23 +3071,24 @@
 
     if ref_labels:
         labels = ref_labels
     else:
         labels = [""] * n_refs
 
     fig = plt.figure(figsize=(6, 6), num="Element References")
+    ax = fig.subplots()
 
     for n in range(n_refs):
-        plt.plot(ref_energy, ref_data[:, n], label=labels[n])
+        ax.plot(ref_energy, ref_data[:, n], label=labels[n])
 
     for n in range(n_refs):
-        plt.plot(scan_energies, scan_absorption_refs[:, n], "o", label=labels[n])
+        ax.plot(scan_energies, scan_absorption_refs[:, n], "o", label=labels[n])
 
-    plt.axes().set_xlabel("Energy, keV", fontsize=15)
-    plt.axes().set_ylabel("Absorption", fontsize=15)
+    ax.set_xlabel("Energy, keV", fontsize=15)
+    ax.set_ylabel("Absorption", fontsize=15)
     plt.grid(True)
     fig.suptitle("Element References", fontsize=20)
     if ref_labels:
         plt.legend(loc="upper right")
     plt.show(block=block)
     return fig
```

### Comparing `pyxrf-1.0.8/pyxrf.egg-info/PKG-INFO` & `pyxrf-1.0.9/pyxrf.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyxrf
-Version: 1.0.8
+Version: 1.0.9
 Summary: UNKNOWN
 Home-page: https://github.com/NSLS-II/PyXRF
 Author: Brookhaven National Laboratory
 License: BSD
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `pyxrf-1.0.8/pyxrf.egg-info/SOURCES.txt` & `pyxrf-1.0.9/pyxrf.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/setup.py` & `pyxrf-1.0.9/setup.py`

 * *Files identical despite different names*

### Comparing `pyxrf-1.0.8/versioneer.py` & `pyxrf-1.0.9/versioneer.py`

 * *Files identical despite different names*

