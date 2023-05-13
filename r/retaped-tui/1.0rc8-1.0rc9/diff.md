# Comparing `tmp/retaped_tui-1.0rc8.tar.gz` & `tmp/retaped_tui-1.0rc9.tar.gz`

## Comparing `retaped_tui-1.0rc8.tar` & `retaped_tui-1.0rc9.tar`

### file list

```diff
@@ -1,76 +1,76 @@
--rw-r--r--   0        0        0      510 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/.vscode/launch.json
--rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/__init__.py
--rw-r--r--   0        0        0      434 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/aboutRT-tui.txt
--rw-r--r--   0        0        0      841 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/globals.py
--rw-r--r--   0        0        0     1199 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/login.py
--rw-r--r--   0        0        0     9508 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/main.py
--rw-r--r--   0        0        0      406 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/structures.py
--rw-r--r--   0        0        0     8276 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/widgets.py
--rw-r--r--   0        0        0     5950 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/__init__.py
--rw-r--r--   0        0        0      826 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplication.py
--rw-r--r--   0        0        0      410 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplicationAdvanced.py
--rw-r--r--   0        0        0     2927 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplicationEvents.py
--rw-r--r--   0        0        0     8320 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplicationManaged.py
--rw-r--r--   0        0        0    10257 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apOptions.py
--rw-r--r--   0        0        0     2183 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/eveventhandler.py
--rw-r--r--   0        0        0     4273 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmActionForm.py
--rw-r--r--   0        0        0     3791 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmActionFormV2.py
--rw-r--r--   0        0        0     8371 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFileSelector.py
--rw-r--r--   0        0        0    16155 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmForm.py
--rw-r--r--   0        0        0     8245 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMultiPage.py
--rw-r--r--   0        0        0     3638 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMutt.py
--rw-r--r--   0        0        0     8938 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMuttActive.py
--rw-r--r--   0        0        0     3293 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormWithMenus.py
--rw-r--r--   0        0        0     1031 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmPopup.py
--rw-r--r--   0        0        0     3987 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fm_form_edit_loop.py
--rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/globals.py
--rw-r--r--   0        0        0     1985 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/muMenu.py
--rw-r--r--   0        0        0     2379 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/muNewMenu.py
--rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysGlobalOptions.py
--rw-r--r--   0        0        0     1119 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysNPSFilteredData.py
--rw-r--r--   0        0        0     5407 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysThemeManagers.py
--rw-r--r--   0        0        0     6161 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysThemes.py
--rw-r--r--   0        0        0     6877 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysTree.py
--rw-r--r--   0        0        0      836 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npyspmfuncs.py
--rw-r--r--   0        0        0     2609 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npyssafewrapper.py
--rw-r--r--   0        0        0     5124 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/proto_fm_screen_area.py
--rw-r--r--   0        0        0     9374 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/stdfmemail.py
--rw-r--r--   0        0        0     2856 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/utilNotify.py
--rw-r--r--   0        0        0      618 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/util_viewhelp.py
--rw-r--r--   0        0        0     1746 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgFormControlCheckbox.py
--rw-r--r--   0        0        0     7840 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgNMenuDisplay.py
--rw-r--r--   0        0        0     3116 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgannotatetextbox.py
--rw-r--r--   0        0        0     4057 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgautocomplete.py
--rw-r--r--   0        0        0     8445 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgboxwidget.py
--rw-r--r--   0        0        0     3902 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgbutton.py
--rw-r--r--   0        0        0     5860 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgcheckbox.py
--rw-r--r--   0        0        0     3280 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgcombobox.py
--rw-r--r--   0        0        0     3507 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgdatecombo.py
--rw-r--r--   0        0        0    15673 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgeditmultiline.py
--rw-r--r--   0        0        0     1667 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgfilenamecombo.py
--rw-r--r--   0        0        0    12412 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wggrid.py
--rw-r--r--   0        0        0     1569 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wggridcoltitles.py
--rw-r--r--   0        0        0    10265 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmonthbox.py
--rw-r--r--   0        0        0    31961 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiline.py
--rw-r--r--   0        0        0     4413 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilineeditable.py
--rw-r--r--   0        0        0    15458 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilinetree.py
--rw-r--r--   0        0        0     4118 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilinetreeselectable.py
--rw-r--r--   0        0        0     3360 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiselect.py
--rw-r--r--   0        0        0     1474 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiselecttree.py
--rw-r--r--   0        0        0      680 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgpassword.py
--rw-r--r--   0        0        0     2011 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgselectone.py
--rw-r--r--   0        0        0     6241 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgslider.py
--rw-r--r--   0        0        0    21858 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextbox.py
--rw-r--r--   0        0        0      933 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextbox_controlchrs.py
--rw-r--r--   0        0        0      971 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextboxunicode.py
--rw-r--r--   0        0        0     7232 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtexttokens.py
--rw-r--r--   0        0        0     6797 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtitlefield.py
--rw-r--r--   0        0        0    31166 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgwidget.py
--rw-r--r--   0        0        0     2564 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgwidget_proto.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/compatibility_code/__init__.py
--rw-r--r--   0        0        0     7343 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/compatibility_code/npysNPSTree.py
--rw-r--r--   0        0        0    11261 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/src/retaped_tui/npyscreen/compatibility_code/oldtreeclasses.py
--rw-r--r--   0        0        0    35149 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/LICENSE
--rw-r--r--   0        0        0       91 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/README.md
--rw-r--r--   0        0        0      676 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/pyproject.toml
--rw-r--r--   0        0        0      659 2020-02-02 00:00:00.000000 retaped_tui-1.0rc8/PKG-INFO
+-rw-r--r--   0        0        0      521 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/.vscode/launch.json
+-rw-r--r--   0        0        0       33 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/__init__.py
+-rw-r--r--   0        0        0      434 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/aboutRT-tui.txt
+-rw-r--r--   0        0        0      841 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/globals.py
+-rw-r--r--   0        0        0     1199 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/login.py
+-rw-r--r--   0        0        0    10426 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/main.py
+-rw-r--r--   0        0        0      406 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/structures.py
+-rw-r--r--   0        0        0     8458 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/widgets.py
+-rw-r--r--   0        0        0     5950 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/__init__.py
+-rw-r--r--   0        0        0      826 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplication.py
+-rw-r--r--   0        0        0      410 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplicationAdvanced.py
+-rw-r--r--   0        0        0     2927 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplicationEvents.py
+-rw-r--r--   0        0        0     8320 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplicationManaged.py
+-rw-r--r--   0        0        0    10257 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apOptions.py
+-rw-r--r--   0        0        0     2183 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/eveventhandler.py
+-rw-r--r--   0        0        0     4273 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmActionForm.py
+-rw-r--r--   0        0        0     3791 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmActionFormV2.py
+-rw-r--r--   0        0        0     8371 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFileSelector.py
+-rw-r--r--   0        0        0    16155 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmForm.py
+-rw-r--r--   0        0        0     8245 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMultiPage.py
+-rw-r--r--   0        0        0     3638 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMutt.py
+-rw-r--r--   0        0        0     8938 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMuttActive.py
+-rw-r--r--   0        0        0     3293 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormWithMenus.py
+-rw-r--r--   0        0        0     1031 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmPopup.py
+-rw-r--r--   0        0        0     3987 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fm_form_edit_loop.py
+-rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/globals.py
+-rw-r--r--   0        0        0     1985 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/muMenu.py
+-rw-r--r--   0        0        0     2379 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/muNewMenu.py
+-rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysGlobalOptions.py
+-rw-r--r--   0        0        0     1119 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysNPSFilteredData.py
+-rw-r--r--   0        0        0     5407 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysThemeManagers.py
+-rw-r--r--   0        0        0     6161 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysThemes.py
+-rw-r--r--   0        0        0     6877 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysTree.py
+-rw-r--r--   0        0        0      836 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npyspmfuncs.py
+-rw-r--r--   0        0        0     2609 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npyssafewrapper.py
+-rw-r--r--   0        0        0     5124 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/proto_fm_screen_area.py
+-rw-r--r--   0        0        0     9374 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/stdfmemail.py
+-rw-r--r--   0        0        0     2856 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/utilNotify.py
+-rw-r--r--   0        0        0      618 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/util_viewhelp.py
+-rw-r--r--   0        0        0     1746 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgFormControlCheckbox.py
+-rw-r--r--   0        0        0     7840 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgNMenuDisplay.py
+-rw-r--r--   0        0        0     3116 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgannotatetextbox.py
+-rw-r--r--   0        0        0     4057 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgautocomplete.py
+-rw-r--r--   0        0        0     8445 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgboxwidget.py
+-rw-r--r--   0        0        0     3902 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgbutton.py
+-rw-r--r--   0        0        0     5860 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgcheckbox.py
+-rw-r--r--   0        0        0     3280 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgcombobox.py
+-rw-r--r--   0        0        0     3507 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgdatecombo.py
+-rw-r--r--   0        0        0    15673 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgeditmultiline.py
+-rw-r--r--   0        0        0     1667 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgfilenamecombo.py
+-rw-r--r--   0        0        0    12412 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wggrid.py
+-rw-r--r--   0        0        0     1569 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wggridcoltitles.py
+-rw-r--r--   0        0        0    10265 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmonthbox.py
+-rw-r--r--   0        0        0    31961 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiline.py
+-rw-r--r--   0        0        0     4413 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilineeditable.py
+-rw-r--r--   0        0        0    15458 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilinetree.py
+-rw-r--r--   0        0        0     4118 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilinetreeselectable.py
+-rw-r--r--   0        0        0     3360 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiselect.py
+-rw-r--r--   0        0        0     1474 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiselecttree.py
+-rw-r--r--   0        0        0      680 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgpassword.py
+-rw-r--r--   0        0        0     2011 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgselectone.py
+-rw-r--r--   0        0        0     6241 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgslider.py
+-rw-r--r--   0        0        0    21858 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextbox.py
+-rw-r--r--   0        0        0      933 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextbox_controlchrs.py
+-rw-r--r--   0        0        0      971 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextboxunicode.py
+-rw-r--r--   0        0        0     7232 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtexttokens.py
+-rw-r--r--   0        0        0     6797 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtitlefield.py
+-rw-r--r--   0        0        0    31166 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgwidget.py
+-rw-r--r--   0        0        0     2564 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgwidget_proto.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/compatibility_code/__init__.py
+-rw-r--r--   0        0        0     7343 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/compatibility_code/npysNPSTree.py
+-rw-r--r--   0        0        0    11261 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/src/retaped_tui/npyscreen/compatibility_code/oldtreeclasses.py
+-rw-r--r--   0        0        0    35149 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/LICENSE
+-rw-r--r--   0        0        0       91 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/README.md
+-rw-r--r--   0        0        0      676 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/pyproject.toml
+-rw-r--r--   0        0        0      659 2020-02-02 00:00:00.000000 retaped_tui-1.0rc9/PKG-INFO
```

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/globals.py` & `retaped_tui-1.0rc9/src/retaped_tui/globals.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/login.py` & `retaped_tui-1.0rc9/src/retaped_tui/login.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/main.py` & `retaped_tui-1.0rc9/src/retaped_tui/main.py`

 * *Files 15% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 import asyncio
 
 import json
 import yaml
 from yaml import Loader
 import os
 import time
+import sys
 
 from . import login
 from . import globals
 
 globals.init()
 from . import structures, widgets
 
@@ -51,66 +52,63 @@
         tmpChannel.name = i['name'] if 'name' in i.keys() else False
         tmpChannel.desc = i['description'] if 'description' in i.keys() else False
         tmpChannel.server = i['server'] if 'server' in i.keys() else False
         tmpChannel.type = i['channel_type']
         globals.cache['channels'].update({i['_id']: tmpChannel})
 
 
-
-def boilerplate():
-    try:
-        asyncio.run(ws())
-    except KeyboardInterrupt:
-        exit(0)
-
+def _exit():
+    exit()
 def wsInit():
     globals.websocket = connect(globals.wsEndpoint)
     globals.websocket.send(json.dumps({"type": "Authenticate", "token": globals.token}))
 
-
-async def ws():
-    try:
-        wsInit()
-    except:
-        npyscreen.notify('WS failed to connect', title='Connection failed')
-        time.sleep(1)
-        exit()
-    while True:
+class wsThread(threading.Thread):
+    def run(self):
         try:
-            message = globals.websocket.recv()
-        except KeyboardInterrupt:
-            exit()
+            wsInit()
         except:
-            npyscreen.notify('Reconnecting', title='Disconnected')
-            failed=True
-            while failed==True:
-                try:
-                    wsInit()
-                except TimeoutError:
-                    failed=True
-
-        message = json.loads(message)
-        match(message['type']):
-            case 'Message':
-                if message['channel'] == globals.currentChannel:
-                    globals.messageBox.renderMessage(message)
-                    globals.messageBox.update(globals.messageBox)
-            case 'MessageUpdate':
-                if message['channel'] == globals.currentChannel:
-                    globals.messageBox.updateMessage(message)
-                    globals.messageBox.update(globals.messageBox)
-            case 'Ready':
-                buildUserCache(message['users'])
-                buildServerCache(message['servers'])
-                buildChannelCache(message['channels'])
-                globals.serverList.values = []
-                for i in message['servers']:
-                    globals.serverList.values.append(i['name'])
-                globals.serverList.name = globals.localUser.username
-                globals.serverList.edit()
+            npyscreen.notify('WS failed to connect', title='Connection failed')
+            time.sleep(1)
+            _exit()
+        while True:
+            try:
+                message = globals.websocket.recv()
+            except KeyboardInterrupt:
+                _exit()
+            except:
+                npyscreen.notify('Reconnecting', title='Disconnected')
+                failed=True
+                while failed==True:
+                    try:
+                        wsInit()
+                    except TimeoutError:
+                        failed=True
+
+            message = json.loads(message)
+            match(message['type']):
+                case 'Message':
+                    if message['channel'] == globals.currentChannel:
+                        globals.messageBox.renderMessage(message)
+                        globals.messageBox.update(globals.messageBox)
+                case 'MessageUpdate':
+                    if message['channel'] == globals.currentChannel:
+                        globals.messageBox.updateMessage(message)
+                        globals.messageBox.update(globals.messageBox)
+                case 'Ready':
+                    buildUserCache(message['users'])
+                    buildServerCache(message['servers'])
+                    buildChannelCache(message['channels'])
+                    globals.serverList.values = []
+                    for i in message['servers']:
+                        globals.serverList.values.append(i['name'])
+                    globals.serverList.name = globals.localUser.username
+                    globals.serverList.edit()
+    def raiseException(self):
+        self.killed=True
 
 
 
 
 
 
 def sendMessage(totallyanargument):
@@ -134,15 +132,15 @@
         globals.inputBox.value=''
         globals.editingMessage=False
     globals.replies=[]
     globals.inputBox.name = ''
     globals.inputBox.update()
 
 def addReply(totallyanargument):
-    if not globals.editingMessage:
+    if not globals.editingMessage and (message:=globals.messageBox.values[globals.highlightedIndex]).id!='':
         message = globals.messageBox.values[globals.highlightedIndex]
         globals.replies.append({'id': message.id, 'mention': False})
         globals.inputBox.name+="> "+message.content+"\n"
         globals.inputBox.update()
 
 def editMessage(totallyanargument):
     message = globals.messageBox.values[globals.highlightedIndex]
@@ -154,71 +152,67 @@
         globals.inputBox.edit()
     else:
         npyscreen.notify('Not your message', title='Failed to edit')
         time.sleep(2)
 
 class TestApp(npyscreen.NPSAppManaged):
     def onStart(self):
-        npyscreen.setTheme(npyscreen.Themes.ElegantTheme)
         globals.app=self
         try:
             if "XDG_CONFIG_DIR" in os.environ:
                 globals.configPath = os.environ['XDG_CONFIG_HOME']
             else:
                 globals.configPath = f'{os.environ["HOME"]}/.config'
             if os.path.exists(f'{globals.configPath}/Retaped.yaml'):
                 self.registerForm("MAIN", MainForm())
             else:
                 self.registerForm("LOGIN", login.LoginForm())
                 self.setNextForm("MAIN", MainForm())
         except KeyboardInterrupt:
-            exit(0)
-
+            _exit()
 class MainForm(npyscreen.FormBaseNew):
     def create(self):
         config = open(f'{globals.configPath}/Retaped.yaml', 'r')
         config = yaml.load(config, Loader=Loader)
         globals.token=config['token']
         globals.apiEndpoint=config['api-endpoint']
         globals.wsEndpoint=config['ws-endpoint']
         globals.form=self
         self.name = 'Retaped TUI'
         self.FIX_MINIMUM_SIZE_WHEN_CREATED = True
-        globals.serverList = self.add(widgets.serverBox, relx=1, rely=1, width=floor(
-            self.max_x/6), height=floor(self.max_y/2)-1)
-        globals.channelList = self.add(widgets.channelBox, relx=1, width=floor(
-            self.max_x/6), height=floor(self.max_y/2))
-        globals.messageBox = self.add(widgets.messageBox, relx=floor(self.max_x/6)+1, rely=1,
-                              height=floor(self.max_y)-6, width=self.max_x-floor(self.max_x/6)-2)
-        globals.inputBox = self.add(widgets.inputTextBox,relx=floor(
-            self.max_x/6)+1, name='', rely=-5, height=4, width=self.max_x-floor(self.max_x/6)-2)
+        globals.serverList = self.add(widgets.serverBox, relx=1, rely=1, width=self.max_x//6, height=self.max_y//2)
+        globals.channelList = self.add(widgets.channelBox, relx=1, width=self.max_x//6, height=self.max_y//2-1)
+        globals.messageBox = self.add(widgets.messageBox, relx=self.max_x//6+1, rely=1,height=self.max_y-6, width=self.max_x-self.max_x//6-2)
+        globals.inputBox = self.add(widgets.inputTextBox,relx=self.max_x//6+1, name='', rely=-5, height=4, width=self.max_x-self.max_x//6-2)
         globals.inputBox.add_handlers({"!s": sendMessage, curses.ascii.ESC: clearReplies})
         globals.messageBox.add_handlers({"r": addReply})
         globals.messageBox.add_handlers({"e": editMessage})
 
         try:
             tmpUser = requests.get(
                     f'{globals.apiEndpoint}/users/@me', headers={'x-session-token': globals.token})
             if tmpUser.status_code == 401:
                 os.remove(f'{globals.configPath}/Retaped.yaml')
                 self.notify('Invalid token')
                 time.sleep(1)
-                exit(1)
+                _exit()
         except KeyboardInterrupt:
-            exit(0)
+            _exit()
         except:
             npyscreen.notify('Failed to request user profile', title='Failed to connect')
             time.sleep(1)
-            exit(1)
+            _exit
         tmpUser=tmpUser.json()
         globals.localUser = structures.user()
         globals.localUser.id = tmpUser['_id']
         globals.localUser.username = tmpUser['username']
         
-        threading.Thread(target=boilerplate).start()
+        globals.wsThread = wsThread()
+        globals.wsThread.daemon=True
+        globals.wsThread.start()
         script_dir = os.path.dirname(__file__)
         for i in open(f'{script_dir}/aboutRT-tui.txt', 'r'):
             tmpFakeMessage = structures.message()
             tmpFakeMessage.content = i
             tmpFakeMessage.replies = []
             tmpFakeMessage.author = ''
             tmpFakeMessage.mentions = []
@@ -230,30 +224,42 @@
             while failed:
                 try:
                     self.edit()
                     failed=False
                 except npyscreen.NotEnoughSpaceForWidget:
                     pass
                 except KeyboardInterrupt:
-                    exit(0)
-
+                    globals.wsThread._is_running=False
+            
+        except KeyboardInterrupt:
+            _exit
     def resize(self):
-        self.refresh()
-        globals.serverList.height, globals.serverList.width = floor(
-            self.max_y/2)-1, floor(self.max_x/6)
-        globals.channelList.height, globals.channelList.width = floor(
-            self.max_y/2), floor(self.max_x/6)
-
-        globals.messageBox.relx, globals.messageBox.height, globals.messageBox.width = floor(
-            self.max_x/6)+1, floor(self.max_y)-6, self.max_x-floor(self.max_x/6)-2
-        globals.inputBox.relx, globals.inputBox.width = floor(
-            self.max_x/6)+1, self.max_x-floor(self.max_x/6)-2
-        self.display()
+        serverList = globals.serverList.entry_widget
+        channelList = globals.channelList.entry_widget
+        messageBox = globals.messageBox.entry_widget
+        inputBox = globals.inputBox.entry_widget
+        
+        serverList.width, serverList.width =  self.max_x//6-2, self.max_y//2-3
+        channelList.width, channelList.max_height = self.max_x//6-2, self.max_y//2-3
+        messageBox.relx, messageBox.height, messageBox.width = self.max_x//6+1, self.max_y-8, self.max_x-self.max_x//6-4
+        inputBox.relx, inputBox.width=self.max_x//6+1, self.max_x-self.max_x//6-4
+        
+        globals.serverList.width, globals.serverList.width =  self.max_x//6, self.max_y//2-1
+        globals.channelList.width, globals.channelList.max_height = self.max_x//6, self.max_y//2-1
+        globals.messageBox.relx, globals.messageBox.height, globals.messageBox.width = self.max_x//6+1, self.max_y-6, self.max_x-self.max_x//6-2
+        globals.inputBox.relx, globals.inputBox.width=self.max_x//6+1, self.max_x-self.max_x//6-2
+        globals.serverList._resize()
+        globals.channelList._resize()
+        globals.messageBox._resize()
+        globals.inputBox._resize()
+        
+        serverList.update(clear=True)
+        channelList.update(clear=True)
+        messageBox.update(clear=True)
+        inputBox.update(clear=True)
+
 
 try:
     TestApp().run()
 except KeyboardInterrupt:
-    exit(0)
-except Exception as e:
-    print(e)
-    exit()
+    _exit()
 # asyncio.run(ws())
```

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/widgets.py` & `retaped_tui-1.0rc9/src/retaped_tui/widgets.py`

 * *Files 2% similar despite different names*

```diff
@@ -91,19 +91,15 @@
         self._contained_widgets.True_box = ''
         super().__init__(screen, values, value, slow_scroll, scroll_exit, return_exit, select_exit,
                          exit_left, exit_right, widgets_inherit_color, always_show_cursor, allow_filtering, **keywords)
 
     def display_value(self, vl: structures.message):
         output = ''
         mentioned = False
-        for i in vl.replies:
-            if i in globals.cache['messages']:
-                output += f'> {globals.cache["messages"][i].content}\n'
-            else:
-                output += f'>Unloaded Message'
+
         if globals.localUser.id in vl.mentions:
             mentioned = True
         if vl.author:
             output += f'[{vl.author}] '
         output += f'{vl.content}'
         return [output, mentioned]
 
@@ -119,15 +115,24 @@
     _contained_widget = multiLineMessages
     def renderMessage(self, messageData):
         reply = []
         mentions=[]
         author = ''
         if 'replies' in messageData.keys():
             for i in messageData['replies']:
-                reply.append(i)
+                if i in globals.cache['messages']:
+                    replyContent=f'> {globals.cache["messages"][i].content}'
+                else:
+                    replyContent=f'>Unloaded Message'
+                reply=structures.message()
+                reply.content=replyContent
+                reply.author=''
+                reply.id=''
+                reply.mentions=[]
+                self.values.append(reply)
         if 'mentions' in messageData.keys():
             for i in messageData['mentions']:
                 mentions.append(i)
         if 'masquerade' in messageData.keys():
             author = messageData['masquerade']['name']
         else:
             if messageData['author'] in globals.cache['users'].keys():
```

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/__init__.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/__init__.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplication.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplication.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplicationEvents.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplicationEvents.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apNPSApplicationManaged.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apNPSApplicationManaged.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/apOptions.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/apOptions.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/eveventhandler.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/eveventhandler.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmActionForm.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmActionForm.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmActionFormV2.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmActionFormV2.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFileSelector.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFileSelector.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmForm.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmForm.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMultiPage.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMultiPage.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMutt.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMutt.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormMuttActive.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormMuttActive.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmFormWithMenus.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmFormWithMenus.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fmPopup.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fmPopup.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/fm_form_edit_loop.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/fm_form_edit_loop.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/muMenu.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/muMenu.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/muNewMenu.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/muNewMenu.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysNPSFilteredData.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysNPSFilteredData.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysThemeManagers.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysThemeManagers.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysThemes.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysThemes.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npysTree.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npysTree.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npyspmfuncs.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npyspmfuncs.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/npyssafewrapper.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/npyssafewrapper.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/proto_fm_screen_area.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/proto_fm_screen_area.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/stdfmemail.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/stdfmemail.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/utilNotify.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/utilNotify.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/util_viewhelp.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/util_viewhelp.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgFormControlCheckbox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgFormControlCheckbox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgNMenuDisplay.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgNMenuDisplay.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgannotatetextbox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgannotatetextbox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgautocomplete.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgautocomplete.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgboxwidget.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgboxwidget.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgbutton.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgbutton.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgcheckbox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgcheckbox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgcombobox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgcombobox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgdatecombo.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgdatecombo.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgeditmultiline.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgeditmultiline.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgfilenamecombo.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgfilenamecombo.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wggrid.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wggrid.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wggridcoltitles.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wggridcoltitles.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmonthbox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmonthbox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiline.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiline.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilineeditable.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilineeditable.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilinetree.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilinetree.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultilinetreeselectable.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultilinetreeselectable.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiselect.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiselect.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgmultiselecttree.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgmultiselecttree.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgpassword.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgpassword.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgselectone.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgselectone.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgslider.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgslider.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextbox.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextbox.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextbox_controlchrs.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextbox_controlchrs.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtextboxunicode.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtextboxunicode.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtexttokens.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtexttokens.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgtitlefield.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgtitlefield.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgwidget.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgwidget.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/wgwidget_proto.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/wgwidget_proto.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/compatibility_code/npysNPSTree.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/compatibility_code/npysNPSTree.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/src/retaped_tui/npyscreen/compatibility_code/oldtreeclasses.py` & `retaped_tui-1.0rc9/src/retaped_tui/npyscreen/compatibility_code/oldtreeclasses.py`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/LICENSE` & `retaped_tui-1.0rc9/LICENSE`

 * *Files identical despite different names*

### Comparing `retaped_tui-1.0rc8/pyproject.toml` & `retaped_tui-1.0rc9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 [project]
 name = "retaped_tui"
-version = "1.0-rc8"
+version = "1.0-rc9"
 authors = [
   { name="Tetra Green", email="giggabyte6@gmail.com" },
 ]
 description = "A Revolt client for the terminal"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `retaped_tui-1.0rc8/PKG-INFO` & `retaped_tui-1.0rc9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: retaped_tui
-Version: 1.0rc8
+Version: 1.0rc9
 Summary: A Revolt client for the terminal
 Project-URL: Homepage, https://github.com/error-404-null-not-found/Retaped-tui
 Project-URL: Bug Tracker, https://github.com/error-404-null-not-found/Retaped-tui/issues
 Author-email: Tetra Green <giggabyte6@gmail.com>
 License-File: LICENSE
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
```

