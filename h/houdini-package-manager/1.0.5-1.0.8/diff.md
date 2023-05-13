# Comparing `tmp/houdini_package_manager-1.0.5.tar.gz` & `tmp/houdini_package_manager-1.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "houdini_package_manager-1.0.5.tar", max compression
+gzip compressed data, was "houdini_package_manager-1.0.8.tar", max compression
```

## Comparing `houdini_package_manager-1.0.5.tar` & `houdini_package_manager-1.0.8.tar`

### file list

```diff
@@ -1,70 +1,72 @@
--rw-r--r--   0        0        0    34523 2023-05-11 17:18:54.695961 houdini_package_manager-1.0.5/LICENSE
--rw-r--r--   0        0        0     2658 2023-05-11 17:18:54.695961 houdini_package_manager-1.0.5/README.md
--rw-r--r--   0        0        0       22 2023-05-11 17:18:54.699961 houdini_package_manager-1.0.5/houdini_package_manager/__init__.py
--rw-r--r--   0        0        0     1149 2023-05-11 17:18:54.699961 houdini_package_manager-1.0.5/houdini_package_manager/main.py
--rw-r--r--   0        0        0     1975 2023-05-11 17:18:54.699961 houdini_package_manager-1.0.5/houdini_package_manager/meta/meta_tools.py
--rw-r--r--   0        0        0   614544 2023-05-11 17:18:54.703961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Black.ttf
--rw-r--r--   0        0        0   672480 2023-05-11 17:18:54.707961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-BlackItalic.ttf
--rw-r--r--   0        0        0   657188 2023-05-11 17:18:54.715961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Bold.ttf
--rw-r--r--   0        0        0   699008 2023-05-11 17:18:54.719961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-BoldItalic.ttf
--rw-r--r--   0        0        0   723544 2023-05-11 17:18:54.723961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Italic.ttf
--rw-r--r--   0        0        0   644556 2023-05-11 17:18:54.727961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Light.ttf
--rw-r--r--   0        0        0   658212 2023-05-11 17:18:54.731961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-LightItalic.ttf
--rw-r--r--   0        0        0   637068 2023-05-11 17:18:54.739961 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Medium.ttf
--rw-r--r--   0        0        0   695588 2023-05-11 17:18:54.743960 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-MediumItalic.ttf
--rw-r--r--   0        0        0   657212 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Regular.ttf
--rw-r--r--   0        0        0      332 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add.svg
--rw-r--r--   0        0        0      329 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_hover.svg
--rw-r--r--   0        0        0    10421 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages.svg
--rw-r--r--   0        0        0    10472 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_confirm.svg
--rw-r--r--   0        0        0    10475 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_confirm_hover.svg
--rw-r--r--   0        0        0    10424 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_hover.svg
--rw-r--r--   0        0        0     1991 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/bug.svg
--rw-r--r--   0        0        0     1988 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/bug_hover.svg
--rw-r--r--   0        0        0      803 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/clear_selection.svg
--rw-r--r--   0        0        0      800 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/clear_selection_hover.svg
--rw-r--r--   0        0        0      427 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/delete.svg
--rw-r--r--   0        0        0      424 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/delete_hover.svg
--rw-r--r--   0        0        0      505 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/docs.svg
--rw-r--r--   0        0        0      502 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/docs_hover.svg
--rw-r--r--   0        0        0      455 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/file.svg
--rw-r--r--   0        0        0      452 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/file_hover.svg
--rw-r--r--   0        0        0      382 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/folder.svg
--rw-r--r--   0        0        0      379 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/folder_hover.svg
--rw-r--r--   0        0        0     4286 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm.ico
--rw-r--r--   0        0        0      566 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm.svg
--rw-r--r--   0        0        0      598 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_ICO.svg
--rw-r--r--   0        0        0      569 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_hover.svg
--rw-r--r--   0        0        0      571 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_icon.svg
--rw-r--r--   0        0        0      696 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/invert_selection.svg
--rw-r--r--   0        0        0      693 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/invert_selection_hover.svg
--rw-r--r--   0        0        0      323 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/migrate.svg
--rw-r--r--   0        0        0      320 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/migrate_hover.svg
--rw-r--r--   0        0        0     1455 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh.svg
--rw-r--r--   0        0        0     1625 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_all.svg
--rw-r--r--   0        0        0     1622 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_all_hover.svg
--rw-r--r--   0        0        0     1452 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_hover.svg
--rw-r--r--   0        0        0      484 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/remove.svg
--rw-r--r--   0        0        0      390 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/remove_all_items.svg
--rw-r--r--   0        0        0      387 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/remove_all_items_hover.svg
--rw-r--r--   0        0        0      502 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/remove_hover.svg
--rw-r--r--   0        0        0      837 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/repo.svg
--rw-r--r--   0        0        0      834 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/repo_hover.svg
--rw-r--r--   0        0        0      224 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/toggle_off.svg
--rw-r--r--   0        0        0      221 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/toggle_off_hover.svg
--rw-r--r--   0        0        0      334 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/toggle_on.svg
--rw-r--r--   0        0        0      331 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/toggle_on_hover.svg
--rw-r--r--   0        0        0      677 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/warning.svg
--rw-r--r--   0        0        0      680 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/warning_hover.svg
--rw-r--r--   0        0        0     2936 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/update.py
--rw-r--r--   0        0        0      868 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/utils.py
--rw-r--r--   0        0        0      655 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/widgets/actions.py
--rw-r--r--   0        0        0    22228 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/widgets/add_packages_layout.py
--rw-r--r--   0        0        0     3574 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/widgets/custom_widgets.py
--rw-r--r--   0        0        0     6818 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/widgets/main_window.py
--rw-r--r--   0        0        0    21983 2023-05-11 17:18:54.747960 houdini_package_manager-1.0.5/houdini_package_manager/widgets/packages_layout.py
--rw-r--r--   0        0        0    12686 2023-05-11 17:18:54.751961 houdini_package_manager-1.0.5/houdini_package_manager/widgets/packages_table.py
--rw-r--r--   0        0        0    28576 2023-05-11 17:18:54.751961 houdini_package_manager-1.0.5/houdini_package_manager/wrangle/config_control.py
--rw-r--r--   0        0        0     1079 2023-05-11 17:18:54.751961 houdini_package_manager-1.0.5/houdini_package_manager/wrangle/package_templates.py
--rw-r--r--   0        0        0     2105 2023-05-11 17:19:22.559861 houdini_package_manager-1.0.5/pyproject.toml
--rw-r--r--   0        0        0     3487 1970-01-01 00:00:00.000000 houdini_package_manager-1.0.5/PKG-INFO
+-rw-r--r--   0        0        0    34523 2023-05-13 05:18:26.037374 houdini_package_manager-1.0.8/LICENSE
+-rw-r--r--   0        0        0     3842 2023-05-13 05:18:26.037374 houdini_package_manager-1.0.8/README.md
+-rw-r--r--   0        0        0       22 2023-05-13 05:18:26.041374 houdini_package_manager-1.0.8/houdini_package_manager/__init__.py
+-rw-r--r--   0        0        0     1149 2023-05-13 05:18:26.041374 houdini_package_manager-1.0.8/houdini_package_manager/main.py
+-rw-r--r--   0        0        0     1975 2023-05-13 05:18:26.041374 houdini_package_manager-1.0.8/houdini_package_manager/meta/meta_tools.py
+-rw-r--r--   0        0        0   614544 2023-05-13 05:18:26.045374 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Black.ttf
+-rw-r--r--   0        0        0   672480 2023-05-13 05:18:26.053375 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-BlackItalic.ttf
+-rw-r--r--   0        0        0   657188 2023-05-13 05:18:26.057375 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Bold.ttf
+-rw-r--r--   0        0        0   699008 2023-05-13 05:18:26.061375 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-BoldItalic.ttf
+-rw-r--r--   0        0        0   723544 2023-05-13 05:18:26.069376 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Italic.ttf
+-rw-r--r--   0        0        0   644556 2023-05-13 05:18:26.073376 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Light.ttf
+-rw-r--r--   0        0        0   658212 2023-05-13 05:18:26.081377 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-LightItalic.ttf
+-rw-r--r--   0        0        0   637068 2023-05-13 05:18:26.085377 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Medium.ttf
+-rw-r--r--   0        0        0   695588 2023-05-13 05:18:26.089377 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-MediumItalic.ttf
+-rw-r--r--   0        0        0   657212 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Regular.ttf
+-rw-r--r--   0        0        0      332 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add.svg
+-rw-r--r--   0        0        0      329 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_hover.svg
+-rw-r--r--   0        0        0    10421 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages.svg
+-rw-r--r--   0        0        0    10472 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_confirm.svg
+-rw-r--r--   0        0        0    10475 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_confirm_hover.svg
+-rw-r--r--   0        0        0    10424 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_hover.svg
+-rw-r--r--   0        0        0     1991 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/bug.svg
+-rw-r--r--   0        0        0     1988 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/bug_hover.svg
+-rw-r--r--   0        0        0      803 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/clear_selection.svg
+-rw-r--r--   0        0        0      800 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/clear_selection_hover.svg
+-rw-r--r--   0        0        0      427 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/delete.svg
+-rw-r--r--   0        0        0      424 2023-05-13 05:18:26.093377 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/delete_hover.svg
+-rw-r--r--   0        0        0      505 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/docs.svg
+-rw-r--r--   0        0        0      502 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/docs_hover.svg
+-rw-r--r--   0        0        0      455 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/file.svg
+-rw-r--r--   0        0        0      452 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/file_hover.svg
+-rw-r--r--   0        0        0      382 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/folder.svg
+-rw-r--r--   0        0        0      379 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/folder_hover.svg
+-rw-r--r--   0        0        0     4286 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm.ico
+-rw-r--r--   0        0        0      566 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm.svg
+-rw-r--r--   0        0        0      598 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_ICO.svg
+-rw-r--r--   0        0        0      591 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_grey.svg
+-rw-r--r--   0        0        0      588 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_grey_hover.svg
+-rw-r--r--   0        0        0      569 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_hover.svg
+-rw-r--r--   0        0        0      571 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_icon.svg
+-rw-r--r--   0        0        0      696 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/invert_selection.svg
+-rw-r--r--   0        0        0      693 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/invert_selection_hover.svg
+-rw-r--r--   0        0        0      323 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/migrate.svg
+-rw-r--r--   0        0        0      320 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/migrate_hover.svg
+-rw-r--r--   0        0        0     1455 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh.svg
+-rw-r--r--   0        0        0     1625 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_all.svg
+-rw-r--r--   0        0        0     1622 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_all_hover.svg
+-rw-r--r--   0        0        0     1452 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_hover.svg
+-rw-r--r--   0        0        0      484 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/remove.svg
+-rw-r--r--   0        0        0      390 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/remove_all_items.svg
+-rw-r--r--   0        0        0      387 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/remove_all_items_hover.svg
+-rw-r--r--   0        0        0      502 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/remove_hover.svg
+-rw-r--r--   0        0        0      837 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/repo.svg
+-rw-r--r--   0        0        0      834 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/repo_hover.svg
+-rw-r--r--   0        0        0      224 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/toggle_off.svg
+-rw-r--r--   0        0        0      221 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/toggle_off_hover.svg
+-rw-r--r--   0        0        0      334 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/toggle_on.svg
+-rw-r--r--   0        0        0      331 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/toggle_on_hover.svg
+-rw-r--r--   0        0        0      677 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/warning.svg
+-rw-r--r--   0        0        0      680 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/warning_hover.svg
+-rw-r--r--   0        0        0     2936 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/update.py
+-rw-r--r--   0        0        0      868 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/utils.py
+-rw-r--r--   0        0        0      655 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/actions.py
+-rw-r--r--   0        0        0    22508 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/add_packages_layout.py
+-rw-r--r--   0        0        0     3574 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/custom_widgets.py
+-rw-r--r--   0        0        0     7351 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/main_window.py
+-rw-r--r--   0        0        0    21983 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/packages_layout.py
+-rw-r--r--   0        0        0    12686 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/widgets/packages_table.py
+-rw-r--r--   0        0        0    28576 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/wrangle/config_control.py
+-rw-r--r--   0        0        0     1079 2023-05-13 05:18:26.097378 houdini_package_manager-1.0.8/houdini_package_manager/wrangle/package_templates.py
+-rw-r--r--   0        0        0     2104 2023-05-13 05:19:00.315457 houdini_package_manager-1.0.8/pyproject.toml
+-rw-r--r--   0        0        0     4670 1970-01-01 00:00:00.000000 houdini_package_manager-1.0.8/PKG-INFO
```

### Comparing `houdini_package_manager-1.0.5/LICENSE` & `houdini_package_manager-1.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/main.py` & `houdini_package_manager-1.0.8/houdini_package_manager/main.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/meta/meta_tools.py` & `houdini_package_manager-1.0.8/houdini_package_manager/meta/meta_tools.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Black.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Black.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-BlackItalic.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-BlackItalic.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Bold.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Bold.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-BoldItalic.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-BoldItalic.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Italic.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Italic.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Light.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Light.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-LightItalic.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-LightItalic.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Medium.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Medium.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-MediumItalic.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-MediumItalic.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/fonts/Lato-Regular.ttf` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/fonts/Lato-Regular.ttf`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_confirm.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_confirm.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_confirm_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_confirm_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/add_packages_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/add_packages_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/bug.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/bug.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/bug_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/bug_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/clear_selection.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/clear_selection.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/clear_selection_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/clear_selection_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm.ico` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm.ico`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_ICO.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_ICO.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/hpm_icon.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/hpm_icon.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/invert_selection.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/invert_selection.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/invert_selection_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/invert_selection_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_all.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_all.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_all_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_all_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/refresh_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/refresh_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/repo.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/repo.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/repo_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/repo_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/warning.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/warning.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/resources/icons/warning_hover.svg` & `houdini_package_manager-1.0.8/houdini_package_manager/resources/icons/warning_hover.svg`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/update.py` & `houdini_package_manager-1.0.8/houdini_package_manager/update.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/utils.py` & `houdini_package_manager-1.0.8/houdini_package_manager/utils.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/actions.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/actions.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/add_packages_layout.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/add_packages_layout.py`

 * *Files 1% similar despite different names*

```diff
@@ -471,20 +471,21 @@
 
 class PluginListItem(QWidget):
     """
     A plugin row for the plugins list.
     Includes a checkbox (with the path name), the path, and a remove-item button.
     """
 
-    def __init__(self, parent: QWidget, path: Path, label_file_overwrite: QLabel) -> None:
-        super().__init__(parent)
+    def __init__(self, listbox: PluginListBox, path: Path, label_file_overwrite: QLabel) -> None:
+        super().__init__(listbox)
 
         if not isinstance(path, Path):
             raise TypeError("path must be a pathlib Path.")
 
+        self.listbox = listbox
         self.label_file_overwrite = label_file_overwrite
 
         self.button_remove = SvgPushButton(
             self,
             16,
             16,
             epath("resources/icons/remove.svg"),
@@ -524,14 +525,19 @@
         self.deleteLater()
 
         # since the delete happens later and we need to update the file overwrite conflict check now,
         # manually disable the toggle instead, which has the same effect in this case.
         self.checkbox.setChecked(False)
         self.label_file_overwrite.property("update")()
 
+        # if there's only one item left, then it must be this one (self) that's getting deleted,
+        # so change stack back to default
+        if self.listbox.layout_plugin_list.count() == 1:
+            self.listbox.setCurrentIndex(0)
+
 
 class SelectPluginsButton(QPushButton):
     """
     The default button that prompts the user to open a file/folder dialog and select files/folders.
     This is meant to be displayed when the plugins list box has no items yet.
     """
```

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/custom_widgets.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/custom_widgets.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/main_window.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/main_window.py`

 * *Files 4% similar despite different names*

```diff
@@ -110,18 +110,30 @@
 
             QTabBar::tab:hover { background-color: #666666; }
             QTabBar::tab:selected { background-color: #4d4d4d; }
         """
         )
 
         # SETTINGS BUTTONS
+        self.DOWNLOAD_URL = "https://houpm.com"
         self.REPOSITORY_URL = "https://github.com/ariffjeff/houdini-package-manager"
         self.REPOSITORY_ISSUES_URL = "https://github.com/ariffjeff/houdini-package-manager/issues"
         self.PACKAGES_DOCS_URL = "https://www.sidefx.com/docs/houdini/ref/plugins.html"
 
+        button_houpm = SvgPushButton(
+            self,
+            56,
+            28,
+            epath("resources/icons/hpm_grey.svg"),
+            epath("resources/icons/hpm_grey_hover.svg"),
+        )
+        button_houpm.clicked.connect(lambda: self.open_url(self.DOWNLOAD_URL))
+        button_houpm.set_hover_status_message(f"Open project download site: {self.DOWNLOAD_URL}")
+        button_houpm.setToolTip("Project download site")
+
         button_repo = SvgPushButton(
             self,
             28,
             28,
             epath("resources/icons/repo.svg"),
             epath("resources/icons/repo_hover.svg"),
         )
@@ -165,14 +177,15 @@
 
         # SET LAYOUTS
         central_widget.setLayout(layout_main_vertical)
 
         layout_main_vertical.addLayout(layout_main_header)
         layout_main_header.addWidget(logo)
         layout_main_header.addLayout(layout_urls)
+        layout_urls.addWidget(button_houpm)
         layout_urls.addWidget(button_repo)
         layout_urls.addWidget(button_bug_report)
         layout_urls.addWidget(button_pkg_docs)
         layout_urls.setAlignment(Qt.AlignRight)
         layout_main_vertical.addWidget(self.tabs)
 
         tab_packages.setLayout(packages.layout_main)
```

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/packages_layout.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/packages_layout.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/widgets/packages_table.py` & `houdini_package_manager-1.0.8/houdini_package_manager/widgets/packages_table.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/wrangle/config_control.py` & `houdini_package_manager-1.0.8/houdini_package_manager/wrangle/config_control.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/houdini_package_manager/wrangle/package_templates.py` & `houdini_package_manager-1.0.8/houdini_package_manager/wrangle/package_templates.py`

 * *Files identical despite different names*

### Comparing `houdini_package_manager-1.0.5/pyproject.toml` & `houdini_package_manager-1.0.8/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 [tool.poetry]
 name = "houdini_package_manager"
-version = "1.0.5"
+version = "1.0.8"
 description = "GUI package manager for Houdini"
-authors = ["Ariff Jeff <fariffjeff@icloud.com>"]
+authors = ["Ariff Jeff <ariffjeff@icloud.com>"]
 repository = "https://github.com/ariffjeff/houdini-package-manager"
 documentation = "https://ariffjeff.github.io/houdini-package-manager/"
 readme = "README.md"
 packages = [
   {include = "houdini_package_manager"}
 ]
```

