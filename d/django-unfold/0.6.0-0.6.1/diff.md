# Comparing `tmp/django_unfold-0.6.0.tar.gz` & `tmp/django_unfold-0.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_unfold-0.6.0.tar", max compression
+gzip compressed data, was "django_unfold-0.6.1.tar", max compression
```

## Comparing `django_unfold-0.6.0.tar` & `django_unfold-0.6.1.tar`

### file list

```diff
@@ -1,133 +1,133 @@
--rw-r--r--   0        0        0     1082 2023-01-13 08:15:39.294988 django_unfold-0.6.0/LICENSE
--rw-r--r--   0        0        0    25346 2023-05-12 17:59:11.443851 django_unfold-0.6.0/README.md
--rw-r--r--   0        0        0     1273 2023-05-12 18:08:32.293031 django_unfold-0.6.0/pyproject.toml
--rw-r--r--   0        0        0        0 2023-04-25 16:53:58.827841 django_unfold-0.6.0/src/unfold/__init__.py
--rw-r--r--   0        0        0    22083 2023-04-29 14:53:25.025426 django_unfold-0.6.0/src/unfold/admin.py
--rw-r--r--   0        0        0      307 2023-04-25 16:53:58.828269 django_unfold-0.6.0/src/unfold/apps.py
--rw-r--r--   0        0        0     1835 2023-04-29 14:48:57.720570 django_unfold-0.6.0/src/unfold/checks.py
--rw-r--r--   0        0        0        0 2023-04-25 16:53:58.828366 django_unfold-0.6.0/src/unfold/contrib/__init__.py
--rw-r--r--   0        0        0        0 2023-04-25 16:53:58.828468 django_unfold-0.6.0/src/unfold/contrib/filters/__init__.py
--rw-r--r--   0        0        0    16034 2023-04-29 14:54:36.705530 django_unfold-0.6.0/src/unfold/contrib/filters/admin.py
--rw-r--r--   0        0        0      107 2023-04-25 16:53:58.828782 django_unfold-0.6.0/src/unfold/contrib/filters/apps.py
--rw-r--r--   0        0        0     4055 2023-04-25 16:53:58.828924 django_unfold-0.6.0/src/unfold/contrib/filters/forms.py
--rw-r--r--   0        0        0     4221 2023-04-25 16:53:58.829091 django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css
--rw-r--r--   0        0        0    19332 2023-04-25 16:53:58.829291 django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js
--rw-r--r--   0        0        0     1668 2023-04-25 16:53:58.829456 django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js
--rw-r--r--   0        0        0    26683 2023-04-25 16:53:58.829680 django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js
--rw-r--r--   0        0        0     2236 2023-04-25 16:53:58.829830 django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js
--rw-r--r--   0        0        0      470 2023-04-25 16:53:58.829970 django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_date_range.html
--rw-r--r--   0        0        0      470 2023-04-25 16:53:58.830145 django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_datetime_range.html
--rw-r--r--   0        0        0      338 2023-04-25 16:53:58.830286 django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_range.html
--rw-r--r--   0        0        0      273 2023-04-25 16:53:58.830426 django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_single.html
--rw-r--r--   0        0        0     1648 2023-04-25 16:53:58.830578 django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html
--rw-r--r--   0        0        0        0 2023-04-25 16:53:58.830668 django_unfold-0.6.0/src/unfold/contrib/forms/__init__.py
--rw-r--r--   0        0        0      105 2023-04-25 16:53:58.830813 django_unfold-0.6.0/src/unfold/contrib/forms/apps.py
--rw-r--r--   0        0        0    20007 2023-04-25 16:53:58.830992 django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/css/trix.css
--rw-r--r--   0        0        0      858 2023-04-25 16:53:58.831136 django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js
--rw-r--r--   0        0        0   172634 2023-04-25 16:53:58.831717 django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/js/trix.js
--rw-r--r--   0        0        0     9558 2023-04-25 16:53:58.831938 django_unfold-0.6.0/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html
--rw-r--r--   0        0        0      351 2023-04-25 16:53:58.832097 django_unfold-0.6.0/src/unfold/contrib/forms/templates/unfold/forms/wysiwyg.html
--rw-r--r--   0        0        0      962 2023-04-29 14:41:34.283805 django_unfold-0.6.0/src/unfold/contrib/forms/widgets.py
--rw-r--r--   0        0        0        0 2023-05-12 17:59:11.446021 django_unfold-0.6.0/src/unfold/contrib/import_export/__init__.py
--rw-r--r--   0        0        0      142 2023-05-12 17:59:11.446213 django_unfold-0.6.0/src/unfold/contrib/import_export/apps.py
--rw-r--r--   0        0        0      672 2023-05-12 17:59:11.446368 django_unfold-0.6.0/src/unfold/contrib/import_export/forms.py
--rw-r--r--   0        0        0      357 2023-05-12 17:59:11.446801 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/base.html
--rw-r--r--   0        0        0      412 2023-05-12 17:59:11.446954 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/change_list_export_item.html
--rw-r--r--   0        0        0      229 2023-05-12 17:59:11.447087 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_export.html
--rw-r--r--   0        0        0      387 2023-05-12 17:59:11.447460 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_item.html
--rw-r--r--   0        0        0     1791 2023-05-12 17:59:11.447700 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/export.html
--rw-r--r--   0        0        0     2075 2023-05-12 17:59:11.448059 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import.html
--rw-r--r--   0        0        0      867 2023-05-12 17:59:11.448210 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html
--rw-r--r--   0        0        0     1422 2023-05-12 17:59:11.448490 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html
--rw-r--r--   0        0        0     1312 2023-05-12 17:59:11.448646 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html
--rw-r--r--   0        0        0     2413 2023-05-12 17:59:11.448800 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html
--rw-r--r--   0        0        0     4880 2023-05-12 17:59:11.448961 django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html
--rw-r--r--   0        0        0      199 2023-04-29 14:24:13.252315 django_unfold-0.6.0/src/unfold/dataclasses.py
--rw-r--r--   0        0        0     3277 2023-04-29 14:41:34.283979 django_unfold-0.6.0/src/unfold/decorators.py
--rw-r--r--   0        0        0       43 2023-04-25 16:53:58.832547 django_unfold-0.6.0/src/unfold/exceptions.py
--rw-r--r--   0        0        0     3281 2023-04-29 14:41:34.284117 django_unfold-0.6.0/src/unfold/forms.py
--rw-r--r--   0        0        0     1116 2023-04-25 16:53:58.832819 django_unfold-0.6.0/src/unfold/settings.py
--rw-r--r--   0        0        0     9000 2023-04-29 14:41:34.284275 django_unfold-0.6.0/src/unfold/sites.py
--rw-r--r--   0        0        0     3890 2023-04-25 16:53:58.833130 django_unfold-0.6.0/src/unfold/static/unfold/css/simplebar.css
--rw-r--r--   0        0        0    71987 2023-05-12 17:59:11.449470 django_unfold-0.6.0/src/unfold/static/unfold/css/styles.css
--rw-r--r--   0        0        0    41071 2023-04-29 14:24:13.253109 django_unfold-0.6.0/src/unfold/static/unfold/js/alpine.js
--rw-r--r--   0        0        0      626 2023-05-12 17:59:11.449806 django_unfold-0.6.0/src/unfold/static/unfold/js/alpine.persist.js
--rw-r--r--   0        0        0     1628 2023-04-25 16:53:58.834027 django_unfold-0.6.0/src/unfold/static/unfold/js/app.js
--rw-r--r--   0        0        0    42820 2023-04-29 14:24:13.253449 django_unfold-0.6.0/src/unfold/static/unfold/js/htmx.js
--rw-r--r--   0        0        0    65855 2023-04-25 16:53:58.834621 django_unfold-0.6.0/src/unfold/static/unfold/js/simplebar.js
--rw-r--r--   0        0        0     2519 2023-04-25 16:53:58.834775 django_unfold-0.6.0/src/unfold/templates/admin/actions.html
--rw-r--r--   0        0        0      802 2023-04-25 16:53:58.834928 django_unfold-0.6.0/src/unfold/templates/admin/app_index.html
--rw-r--r--   0        0        0     3594 2023-04-25 16:53:58.835073 django_unfold-0.6.0/src/unfold/templates/admin/app_list.html
--rw-r--r--   0        0        0      478 2023-04-25 16:53:58.835211 django_unfold-0.6.0/src/unfold/templates/admin/auth/user/add_form.html
--rw-r--r--   0        0        0     2892 2023-05-12 17:59:11.450055 django_unfold-0.6.0/src/unfold/templates/admin/auth/user/change_password.html
--rw-r--r--   0        0        0     3503 2023-04-25 16:53:58.835525 django_unfold-0.6.0/src/unfold/templates/admin/base.html
--rw-r--r--   0        0        0      361 2023-04-25 16:53:58.835682 django_unfold-0.6.0/src/unfold/templates/admin/base_site.html
--rw-r--r--   0        0        0     5001 2023-04-25 16:53:58.835845 django_unfold-0.6.0/src/unfold/templates/admin/change_form.html
--rw-r--r--   0        0        0      686 2023-04-25 16:53:58.835984 django_unfold-0.6.0/src/unfold/templates/admin/change_form_object_tools.html
--rw-r--r--   0        0        0     8376 2023-04-25 16:53:58.836131 django_unfold-0.6.0/src/unfold/templates/admin/change_list.html
--rw-r--r--   0        0        0      699 2023-04-25 16:53:58.836285 django_unfold-0.6.0/src/unfold/templates/admin/change_list_object_tools.html
--rw-r--r--   0        0        0     4206 2023-04-29 14:24:13.253582 django_unfold-0.6.0/src/unfold/templates/admin/change_list_results.html
--rw-r--r--   0        0        0     1306 2023-04-25 16:53:58.836586 django_unfold-0.6.0/src/unfold/templates/admin/date_hierarchy.html
--rw-r--r--   0        0        0     5166 2023-05-12 17:59:11.450271 django_unfold-0.6.0/src/unfold/templates/admin/delete_confirmation.html
--rw-r--r--   0        0        0     4941 2023-04-25 16:53:58.836907 django_unfold-0.6.0/src/unfold/templates/admin/delete_selected_confirmation.html
--rw-r--r--   0        0        0     4372 2023-04-25 16:53:58.837062 django_unfold-0.6.0/src/unfold/templates/admin/edit_inline/stacked.html
--rw-r--r--   0        0        0    12199 2023-04-25 16:53:58.837259 django_unfold-0.6.0/src/unfold/templates/admin/edit_inline/tabular.html
--rw-r--r--   0        0        0     1479 2023-04-25 16:53:58.837505 django_unfold-0.6.0/src/unfold/templates/admin/filter.html
--rw-r--r--   0        0        0     3047 2023-04-25 16:53:58.837678 django_unfold-0.6.0/src/unfold/templates/admin/includes/fieldset.html
--rw-r--r--   0        0        0      468 2023-04-25 16:53:58.837840 django_unfold-0.6.0/src/unfold/templates/admin/includes/object_delete_summary.html
--rw-r--r--   0        0        0      674 2023-04-25 16:53:58.837997 django_unfold-0.6.0/src/unfold/templates/admin/index.html
--rw-r--r--   0        0        0     3494 2023-04-25 16:53:58.838180 django_unfold-0.6.0/src/unfold/templates/admin/login.html
--rw-r--r--   0        0        0     1178 2023-04-25 16:53:58.838335 django_unfold-0.6.0/src/unfold/templates/admin/nav_sidebar.html
--rw-r--r--   0        0        0     3951 2023-04-25 16:53:58.838481 django_unfold-0.6.0/src/unfold/templates/admin/object_history.html
--rw-r--r--   0        0        0     1173 2023-04-25 16:53:58.838617 django_unfold-0.6.0/src/unfold/templates/admin/pagination.html
--rw-r--r--   0        0        0     1143 2023-04-25 16:53:58.839211 django_unfold-0.6.0/src/unfold/templates/admin/search_form.html
--rw-r--r--   0        0        0     4306 2023-04-25 16:53:58.839427 django_unfold-0.6.0/src/unfold/templates/admin/submit_line.html
--rw-r--r--   0        0        0     1751 2023-04-25 16:53:58.839617 django_unfold-0.6.0/src/unfold/templates/admin/widgets/clearable_file_input.html
--rw-r--r--   0        0        0     3888 2023-04-25 16:53:58.839816 django_unfold-0.6.0/src/unfold/templates/admin/widgets/related_widget_wrapper.html
--rw-r--r--   0        0        0      848 2023-04-25 16:53:58.839974 django_unfold-0.6.0/src/unfold/templates/admin/widgets/split_datetime.html
--rw-r--r--   0        0        0      785 2023-04-25 16:53:58.840124 django_unfold-0.6.0/src/unfold/templates/auth/widgets/read_only_password_hash.html
--rw-r--r--   0        0        0     1028 2023-04-25 16:53:58.840286 django_unfold-0.6.0/src/unfold/templates/registration/logged_out.html
--rw-r--r--   0        0        0     1062 2023-04-25 16:53:58.840449 django_unfold-0.6.0/src/unfold/templates/registration/password_change_done.html
--rw-r--r--   0        0        0     2225 2023-04-25 16:53:58.840609 django_unfold-0.6.0/src/unfold/templates/registration/password_change_form.html
--rw-r--r--   0        0        0     1461 2023-04-29 14:24:13.253731 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/actions_row.html
--rw-r--r--   0        0        0     3908 2023-04-25 16:53:58.840917 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/app_list.html
--rw-r--r--   0        0        0     3302 2023-04-25 16:53:58.841436 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/app_list_default.html
--rw-r--r--   0        0        0      466 2023-04-25 16:53:58.841593 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/boolean.html
--rw-r--r--   0        0        0      234 2023-04-25 16:53:58.841751 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/breadcrumb_item.html
--rw-r--r--   0        0        0      248 2023-04-25 16:53:58.841920 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/display_header.html
--rw-r--r--   0        0        0     2072 2023-04-25 16:53:58.842071 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/display_label.html
--rw-r--r--   0        0        0      335 2023-05-12 17:59:11.450462 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/field.html
--rw-r--r--   0        0        0      266 2023-04-25 16:53:58.842332 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/form_errors.html
--rw-r--r--   0        0        0      151 2023-04-25 16:53:58.842459 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/help_text.html
--rw-r--r--   0        0        0     1995 2023-04-25 16:53:58.842615 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/history.html
--rw-r--r--   0        0        0      237 2023-04-25 16:53:58.842754 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/label.html
--rw-r--r--   0        0        0      557 2023-04-25 16:53:58.842902 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages/error.html
--rw-r--r--   0        0        0      404 2023-04-25 16:53:58.843034 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages/errornote.html
--rw-r--r--   0        0        0      143 2023-04-25 16:53:58.843183 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages/info.html
--rw-r--r--   0        0        0      595 2023-04-25 16:53:58.843319 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages.html
--rw-r--r--   0        0        0     1101 2023-04-29 08:17:13.737125 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/navigation.html
--rw-r--r--   0        0        0       69 2023-04-25 16:53:58.843716 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/pagination_current_item.html
--rw-r--r--   0        0        0       56 2023-04-25 16:53:58.843850 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/pagination_ellipsis.html
--rw-r--r--   0        0        0     1314 2023-04-25 16:53:58.843984 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/search.html
--rw-r--r--   0        0        0      725 2023-04-25 16:53:58.844119 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/search_results.html
--rw-r--r--   0        0        0      442 2023-04-25 16:53:58.844252 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/site_icon.html
--rw-r--r--   0        0        0     2038 2023-05-12 17:59:11.450664 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/tab_list.html
--rw-r--r--   0        0        0     4895 2023-04-25 16:53:58.844537 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/userlinks.html
--rw-r--r--   0        0        0     1120 2023-04-25 16:53:58.844676 django_unfold-0.6.0/src/unfold/templates/unfold/helpers/welcomemsg.html
--rw-r--r--   0        0        0      859 2023-04-25 16:53:58.844811 django_unfold-0.6.0/src/unfold/templates/unfold/layouts/base_simple.html
--rw-r--r--   0        0        0     3149 2023-05-12 17:59:11.450883 django_unfold-0.6.0/src/unfold/templates/unfold/layouts/skeleton.html
--rw-r--r--   0        0        0     2218 2023-05-12 17:59:11.451078 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/clearable_file_input_small.html
--rw-r--r--   0        0        0       88 2023-04-25 16:53:58.845218 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/date.html
--rw-r--r--   0        0        0      262 2023-04-25 16:53:58.845347 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/range.html
--rw-r--r--   0        0        0      881 2023-04-25 16:53:58.845482 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/split_datetime_vertical.html
--rw-r--r--   0        0        0      459 2023-04-25 16:53:58.845611 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/textarea.html
--rw-r--r--   0        0        0       88 2023-04-25 16:53:58.845754 django_unfold-0.6.0/src/unfold/templates/unfold/widgets/time.html
--rw-r--r--   0        0        0        0 2023-04-25 16:53:58.845896 django_unfold-0.6.0/src/unfold/templatetags/__init__.py
--rw-r--r--   0        0        0     3559 2023-05-12 17:59:11.451293 django_unfold-0.6.0/src/unfold/templatetags/unfold.py
--rw-r--r--   0        0        0    10012 2023-04-29 14:41:34.284613 django_unfold-0.6.0/src/unfold/templatetags/unfold_list.py
--rw-r--r--   0        0        0      576 2023-04-29 14:41:34.284745 django_unfold-0.6.0/src/unfold/typing.py
--rw-r--r--   0        0        0     3878 2023-04-29 14:41:34.285023 django_unfold-0.6.0/src/unfold/utils.py
--rw-r--r--   0        0        0      708 2023-04-29 14:41:34.285153 django_unfold-0.6.0/src/unfold/views.py
--rw-r--r--   0        0        0     8150 2023-05-12 17:59:11.451628 django_unfold-0.6.0/src/unfold/widgets.py
--rw-r--r--   0        0        0    27827 1970-01-01 00:00:00.000000 django_unfold-0.6.0/setup.py
--rw-r--r--   0        0        0    26377 1970-01-01 00:00:00.000000 django_unfold-0.6.0/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-13 10:12:56.719117 django_unfold-0.6.1/LICENSE
+-rw-r--r--   0        0        0    25292 2023-05-13 10:13:27.829399 django_unfold-0.6.1/README.md
+-rw-r--r--   0        0        0     1277 2023-05-13 10:13:47.172513 django_unfold-0.6.1/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.598781 django_unfold-0.6.1/src/unfold/__init__.py
+-rw-r--r--   0        0        0    22083 2023-05-12 18:20:54.599253 django_unfold-0.6.1/src/unfold/admin.py
+-rw-r--r--   0        0        0      307 2023-05-12 18:20:54.599876 django_unfold-0.6.1/src/unfold/apps.py
+-rw-r--r--   0        0        0     1835 2023-05-12 18:20:54.600089 django_unfold-0.6.1/src/unfold/checks.py
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.600203 django_unfold-0.6.1/src/unfold/contrib/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.600335 django_unfold-0.6.1/src/unfold/contrib/filters/__init__.py
+-rw-r--r--   0        0        0    16034 2023-05-12 18:20:54.600718 django_unfold-0.6.1/src/unfold/contrib/filters/admin.py
+-rw-r--r--   0        0        0      107 2023-05-12 18:20:54.600880 django_unfold-0.6.1/src/unfold/contrib/filters/apps.py
+-rw-r--r--   0        0        0     4055 2023-05-12 18:20:54.601060 django_unfold-0.6.1/src/unfold/contrib/filters/forms.py
+-rw-r--r--   0        0        0     4221 2023-05-12 18:20:54.601236 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css
+-rw-r--r--   0        0        0    19332 2023-05-12 18:20:54.601420 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js
+-rw-r--r--   0        0        0     1668 2023-05-12 18:20:54.601576 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js
+-rw-r--r--   0        0        0    26683 2023-05-12 18:20:54.601864 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js
+-rw-r--r--   0        0        0     2236 2023-05-12 18:20:54.602017 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js
+-rw-r--r--   0        0        0      470 2023-05-12 18:20:54.602162 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_date_range.html
+-rw-r--r--   0        0        0      470 2023-05-12 18:20:54.602300 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_datetime_range.html
+-rw-r--r--   0        0        0      338 2023-05-12 18:20:54.602434 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_range.html
+-rw-r--r--   0        0        0      273 2023-05-12 18:20:54.602579 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_single.html
+-rw-r--r--   0        0        0     1648 2023-05-12 18:20:54.602723 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.602815 django_unfold-0.6.1/src/unfold/contrib/forms/__init__.py
+-rw-r--r--   0        0        0      105 2023-05-12 18:20:54.602973 django_unfold-0.6.1/src/unfold/contrib/forms/apps.py
+-rw-r--r--   0        0        0    20007 2023-05-12 18:20:54.603172 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/css/trix.css
+-rw-r--r--   0        0        0      858 2023-05-12 18:20:54.603349 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js
+-rw-r--r--   0        0        0   172634 2023-05-12 18:20:54.603957 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.js
+-rw-r--r--   0        0        0     9558 2023-05-12 18:20:54.604145 django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html
+-rw-r--r--   0        0        0      351 2023-05-12 18:20:54.604341 django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/wysiwyg.html
+-rw-r--r--   0        0        0      962 2023-05-12 18:20:54.604771 django_unfold-0.6.1/src/unfold/contrib/forms/widgets.py
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.604888 django_unfold-0.6.1/src/unfold/contrib/import_export/__init__.py
+-rw-r--r--   0        0        0      142 2023-05-12 18:20:54.605086 django_unfold-0.6.1/src/unfold/contrib/import_export/apps.py
+-rw-r--r--   0        0        0      672 2023-05-12 18:20:54.605258 django_unfold-0.6.1/src/unfold/contrib/import_export/forms.py
+-rw-r--r--   0        0        0      357 2023-05-12 18:20:54.605425 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/base.html
+-rw-r--r--   0        0        0      412 2023-05-12 18:20:54.605579 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_export_item.html
+-rw-r--r--   0        0        0      229 2023-05-12 18:20:54.605725 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_export.html
+-rw-r--r--   0        0        0      387 2023-05-12 18:20:54.605864 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_item.html
+-rw-r--r--   0        0        0     1791 2023-05-12 18:20:54.606013 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/export.html
+-rw-r--r--   0        0        0     2075 2023-05-12 18:20:54.606159 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import.html
+-rw-r--r--   0        0        0      867 2023-05-12 18:20:54.606318 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html
+-rw-r--r--   0        0        0     1422 2023-05-12 18:20:54.606457 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html
+-rw-r--r--   0        0        0     1312 2023-05-12 18:20:54.606598 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html
+-rw-r--r--   0        0        0     2413 2023-05-12 18:20:54.606738 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html
+-rw-r--r--   0        0        0     4880 2023-05-12 18:20:54.606939 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html
+-rw-r--r--   0        0        0      199 2023-05-12 18:20:54.607385 django_unfold-0.6.1/src/unfold/dataclasses.py
+-rw-r--r--   0        0        0     3277 2023-05-12 18:20:54.607661 django_unfold-0.6.1/src/unfold/decorators.py
+-rw-r--r--   0        0        0       43 2023-05-12 18:20:54.607837 django_unfold-0.6.1/src/unfold/exceptions.py
+-rw-r--r--   0        0        0     3281 2023-05-12 18:20:54.608016 django_unfold-0.6.1/src/unfold/forms.py
+-rw-r--r--   0        0        0     1116 2023-05-12 18:20:54.608156 django_unfold-0.6.1/src/unfold/settings.py
+-rw-r--r--   0        0        0     9000 2023-05-12 18:20:54.608315 django_unfold-0.6.1/src/unfold/sites.py
+-rw-r--r--   0        0        0     3890 2023-05-12 18:20:54.608495 django_unfold-0.6.1/src/unfold/static/unfold/css/simplebar.css
+-rw-r--r--   0        0        0    71987 2023-05-12 18:20:54.608770 django_unfold-0.6.1/src/unfold/static/unfold/css/styles.css
+-rw-r--r--   0        0        0    41071 2023-05-12 18:20:54.609088 django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.js
+-rw-r--r--   0        0        0      626 2023-05-12 18:20:54.609260 django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.persist.js
+-rw-r--r--   0        0        0     1628 2023-05-12 18:20:54.609421 django_unfold-0.6.1/src/unfold/static/unfold/js/app.js
+-rw-r--r--   0        0        0    42820 2023-05-12 18:20:54.609691 django_unfold-0.6.1/src/unfold/static/unfold/js/htmx.js
+-rw-r--r--   0        0        0    65855 2023-05-12 18:20:54.610054 django_unfold-0.6.1/src/unfold/static/unfold/js/simplebar.js
+-rw-r--r--   0        0        0     2519 2023-05-12 18:20:54.610231 django_unfold-0.6.1/src/unfold/templates/admin/actions.html
+-rw-r--r--   0        0        0      802 2023-05-12 18:20:54.610384 django_unfold-0.6.1/src/unfold/templates/admin/app_index.html
+-rw-r--r--   0        0        0     3594 2023-05-12 18:20:54.610605 django_unfold-0.6.1/src/unfold/templates/admin/app_list.html
+-rw-r--r--   0        0        0      478 2023-05-12 18:20:54.610762 django_unfold-0.6.1/src/unfold/templates/admin/auth/user/add_form.html
+-rw-r--r--   0        0        0     2892 2023-05-12 18:20:54.610908 django_unfold-0.6.1/src/unfold/templates/admin/auth/user/change_password.html
+-rw-r--r--   0        0        0     3503 2023-05-12 18:20:54.611288 django_unfold-0.6.1/src/unfold/templates/admin/base.html
+-rw-r--r--   0        0        0      361 2023-05-12 18:20:54.611499 django_unfold-0.6.1/src/unfold/templates/admin/base_site.html
+-rw-r--r--   0        0        0     5001 2023-05-12 18:20:54.611702 django_unfold-0.6.1/src/unfold/templates/admin/change_form.html
+-rw-r--r--   0        0        0      686 2023-05-12 18:20:54.611928 django_unfold-0.6.1/src/unfold/templates/admin/change_form_object_tools.html
+-rw-r--r--   0        0        0     8376 2023-05-12 18:20:54.612096 django_unfold-0.6.1/src/unfold/templates/admin/change_list.html
+-rw-r--r--   0        0        0      699 2023-05-12 18:20:54.612241 django_unfold-0.6.1/src/unfold/templates/admin/change_list_object_tools.html
+-rw-r--r--   0        0        0     4206 2023-05-12 18:20:54.612387 django_unfold-0.6.1/src/unfold/templates/admin/change_list_results.html
+-rw-r--r--   0        0        0     1306 2023-05-12 18:20:54.612538 django_unfold-0.6.1/src/unfold/templates/admin/date_hierarchy.html
+-rw-r--r--   0        0        0     5166 2023-05-12 18:20:54.612692 django_unfold-0.6.1/src/unfold/templates/admin/delete_confirmation.html
+-rw-r--r--   0        0        0     4941 2023-05-12 18:20:54.612842 django_unfold-0.6.1/src/unfold/templates/admin/delete_selected_confirmation.html
+-rw-r--r--   0        0        0     4372 2023-05-12 18:20:54.612989 django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/stacked.html
+-rw-r--r--   0        0        0    12199 2023-05-12 18:20:54.613137 django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/tabular.html
+-rw-r--r--   0        0        0     1479 2023-05-12 18:20:54.613269 django_unfold-0.6.1/src/unfold/templates/admin/filter.html
+-rw-r--r--   0        0        0     3047 2023-05-12 18:20:54.613405 django_unfold-0.6.1/src/unfold/templates/admin/includes/fieldset.html
+-rw-r--r--   0        0        0      468 2023-05-12 18:20:54.613548 django_unfold-0.6.1/src/unfold/templates/admin/includes/object_delete_summary.html
+-rw-r--r--   0        0        0      674 2023-05-12 18:20:54.613684 django_unfold-0.6.1/src/unfold/templates/admin/index.html
+-rw-r--r--   0        0        0     3494 2023-05-12 18:20:54.613824 django_unfold-0.6.1/src/unfold/templates/admin/login.html
+-rw-r--r--   0        0        0     1178 2023-05-12 18:20:54.613956 django_unfold-0.6.1/src/unfold/templates/admin/nav_sidebar.html
+-rw-r--r--   0        0        0     3951 2023-05-12 18:20:54.614095 django_unfold-0.6.1/src/unfold/templates/admin/object_history.html
+-rw-r--r--   0        0        0     1173 2023-05-12 18:20:54.614240 django_unfold-0.6.1/src/unfold/templates/admin/pagination.html
+-rw-r--r--   0        0        0     1143 2023-05-12 18:20:54.614378 django_unfold-0.6.1/src/unfold/templates/admin/search_form.html
+-rw-r--r--   0        0        0     4306 2023-05-12 18:20:54.614530 django_unfold-0.6.1/src/unfold/templates/admin/submit_line.html
+-rw-r--r--   0        0        0     1751 2023-05-12 18:20:54.614674 django_unfold-0.6.1/src/unfold/templates/admin/widgets/clearable_file_input.html
+-rw-r--r--   0        0        0     3888 2023-05-12 18:20:54.614822 django_unfold-0.6.1/src/unfold/templates/admin/widgets/related_widget_wrapper.html
+-rw-r--r--   0        0        0      848 2023-05-12 18:20:54.615101 django_unfold-0.6.1/src/unfold/templates/admin/widgets/split_datetime.html
+-rw-r--r--   0        0        0      785 2023-05-12 18:20:54.615265 django_unfold-0.6.1/src/unfold/templates/auth/widgets/read_only_password_hash.html
+-rw-r--r--   0        0        0     1028 2023-05-12 18:20:54.615426 django_unfold-0.6.1/src/unfold/templates/registration/logged_out.html
+-rw-r--r--   0        0        0     1062 2023-05-12 18:20:54.615582 django_unfold-0.6.1/src/unfold/templates/registration/password_change_done.html
+-rw-r--r--   0        0        0     2225 2023-05-12 18:20:54.615724 django_unfold-0.6.1/src/unfold/templates/registration/password_change_form.html
+-rw-r--r--   0        0        0     1461 2023-05-12 18:20:54.615872 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/actions_row.html
+-rw-r--r--   0        0        0     3908 2023-05-12 18:20:54.616067 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list.html
+-rw-r--r--   0        0        0     3302 2023-05-12 18:20:54.616262 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list_default.html
+-rw-r--r--   0        0        0      466 2023-05-12 18:20:54.616448 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/boolean.html
+-rw-r--r--   0        0        0      234 2023-05-12 18:20:54.616621 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/breadcrumb_item.html
+-rw-r--r--   0        0        0      248 2023-05-12 18:20:54.616796 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_header.html
+-rw-r--r--   0        0        0     2072 2023-05-12 18:20:54.616979 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_label.html
+-rw-r--r--   0        0        0      335 2023-05-12 18:20:54.617143 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/field.html
+-rw-r--r--   0        0        0      266 2023-05-12 18:20:54.617297 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/form_errors.html
+-rw-r--r--   0        0        0      151 2023-05-12 18:20:54.617435 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/help_text.html
+-rw-r--r--   0        0        0     1995 2023-05-12 18:20:54.617571 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/history.html
+-rw-r--r--   0        0        0      237 2023-05-12 18:20:54.617700 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/label.html
+-rw-r--r--   0        0        0      557 2023-05-12 18:20:54.617864 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/error.html
+-rw-r--r--   0        0        0      404 2023-05-12 18:20:54.618038 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/errornote.html
+-rw-r--r--   0        0        0      143 2023-05-12 18:20:54.618223 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/info.html
+-rw-r--r--   0        0        0      595 2023-05-12 18:20:54.618403 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages.html
+-rw-r--r--   0        0        0     1101 2023-05-12 18:20:54.618729 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/navigation.html
+-rw-r--r--   0        0        0       69 2023-05-12 18:20:54.618910 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/pagination_current_item.html
+-rw-r--r--   0        0        0       56 2023-05-12 18:20:54.619087 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/pagination_ellipsis.html
+-rw-r--r--   0        0        0     1314 2023-05-12 18:20:54.619231 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search.html
+-rw-r--r--   0        0        0      725 2023-05-12 18:20:54.619389 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search_results.html
+-rw-r--r--   0        0        0      442 2023-05-12 18:20:54.619541 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/site_icon.html
+-rw-r--r--   0        0        0     2038 2023-05-12 18:20:54.619703 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/tab_list.html
+-rw-r--r--   0        0        0     4895 2023-05-12 18:20:54.619870 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/userlinks.html
+-rw-r--r--   0        0        0     1120 2023-05-12 18:20:54.620020 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/welcomemsg.html
+-rw-r--r--   0        0        0      859 2023-05-12 18:20:54.620180 django_unfold-0.6.1/src/unfold/templates/unfold/layouts/base_simple.html
+-rw-r--r--   0        0        0     3149 2023-05-12 18:20:54.620363 django_unfold-0.6.1/src/unfold/templates/unfold/layouts/skeleton.html
+-rw-r--r--   0        0        0     2218 2023-05-12 18:20:54.620539 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/clearable_file_input_small.html
+-rw-r--r--   0        0        0       88 2023-05-12 18:20:54.620735 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/date.html
+-rw-r--r--   0        0        0      262 2023-05-12 18:20:54.620945 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/range.html
+-rw-r--r--   0        0        0      881 2023-05-12 18:20:54.621116 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/split_datetime_vertical.html
+-rw-r--r--   0        0        0      459 2023-05-12 18:20:54.621287 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/textarea.html
+-rw-r--r--   0        0        0       88 2023-05-12 18:20:54.621454 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/time.html
+-rw-r--r--   0        0        0        0 2023-05-12 18:20:54.621577 django_unfold-0.6.1/src/unfold/templatetags/__init__.py
+-rw-r--r--   0        0        0     3559 2023-05-12 18:20:54.621781 django_unfold-0.6.1/src/unfold/templatetags/unfold.py
+-rw-r--r--   0        0        0    10012 2023-05-12 18:20:54.621974 django_unfold-0.6.1/src/unfold/templatetags/unfold_list.py
+-rw-r--r--   0        0        0      576 2023-05-12 18:20:54.622129 django_unfold-0.6.1/src/unfold/typing.py
+-rw-r--r--   0        0        0     3878 2023-05-12 18:20:54.622285 django_unfold-0.6.1/src/unfold/utils.py
+-rw-r--r--   0        0        0      708 2023-05-12 18:20:54.622428 django_unfold-0.6.1/src/unfold/views.py
+-rw-r--r--   0        0        0     8150 2023-05-12 18:20:54.622598 django_unfold-0.6.1/src/unfold/widgets.py
+-rw-r--r--   0        0        0    27771 1970-01-01 00:00:00.000000 django_unfold-0.6.1/setup.py
+-rw-r--r--   0        0        0    26327 1970-01-01 00:00:00.000000 django_unfold-0.6.1/PKG-INFO
```

### Comparing `django_unfold-0.6.0/LICENSE` & `django_unfold-0.6.1/LICENSE`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2023 Remaster Solutions s.r.o.
+Copyright (c) 2023 Unfold Admin
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `django_unfold-0.6.0/README.md` & `django_unfold-0.6.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-![Screenshot - Objects Listing](https://github.com/remastr/django-unfold/raw/main/screenshot-1.jpg)
+![Screenshot - Objects Listing](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-1.jpg)
 
-![Screenshot - Login Page](https://github.com/remastr/django-unfold/raw/main/screenshot-2.jpg)
+![Screenshot - Login Page](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-2.jpg)
 
 ## Unfold Django Admin Theme
 
 Unfold is a new theme for Django Admin incorporating some most common practises for building full-fledged admin areas.
 
 - **Visual**: provides new user interface based on Tailwind CSS framework
 - **Sidebar:** simplifies definition of custom sidebar navigation
@@ -112,14 +112,15 @@
 class UserAdmin(BaseUserAdmin, ModelAdmin):
     pass
 ```
 
 ## Configuration
 
 ### Available settings.py options
+
 ```python
 # settings.py
 
 from django.templatetags.static import static
 from django.urls import reverse_lazy
 from django.utils.translation import gettext_lazy as _
 
@@ -314,24 +315,25 @@
 
 ### Actions overview
 
 Besides traditional actions selected from dropdown, Unfold supports several other types of actions. Following table
 gives overview of all available actions together with their recommended usage:
 
 | Type of action | Appearance                               | Usage                                                                                      | Examples of usage                      |
-|----------------|------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------|
+| -------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------- |
 | Default        | List view - top of listing (in dropdown) | Actions, where you want to select specific subset of instances to perform this action upon | Bulk deleting, bulk activation         |
 | Global         | List view - top of listing (as buttons)  | General actions for model, without selecting specific instances                            | Import, export                         |
 | Row            | List view - in each row                  | Action for one specific instance, executable from listing                                  | Activation, sync with external service |
 | Detail         | Detail view - top of detail              | Action for one specific instance, executable from detail                                   | Activation, sync with external service |
 | Submit line    | Detail view - near submit button         | Action performed during form submit (instance save)                                        | Publishing article together with save  |
 
 ### Custom unfold @action decorator
 
 Unfold also uses custom `@action` decorator, supporting 2 more parameters in comparison to base `@action` decorator:
+
 - `url_path`: Action path name, used to override the path under which the action will be available
   (if not provided, URL path will be generated by Unfold)
 - `attrs`: Dictionary of the additional attributes added to the `<a>` element, used for e.g. opening action in new tab (`{"target": "_blank"}`)
 
 ### Action handler functions
 
 This section provides explanation of how the action handler functions should be constructed for Unfold actions.
@@ -483,18 +485,16 @@
         CustomRangeNumericListFilter,  # Numeric range search not restricted to a model field
     )
 
     def get_queryset(self, request):
         return super().get_queryset().annotate(items_count=Count("item", distinct=True))
 ```
 
-
 ## Third party packages
 
-
 ### django-import-export
 
 To get proper visual appearance for django-import-export, two things are needed
 
 1. Add `unfold.contrib.import_export` to `INSTALLED_APPS` at the begging of the file. This action will override all templates coming from the plugin.
 2. Change `import_form_class` and `export_form_class` in ModelAdmin which is inheriting from `ImportExportModelAdmin`. This chunk of code is responsible for adding proper styling to form elements.
 
@@ -552,32 +552,30 @@
 
 When creating custom dashboard or adding custom components, it is needed to add own styles. Adding custom styles is described above. Most of the time, it is supposed that new elements are going to match with the rest of the administration panel. First of all, create tailwind.config.js in your application. Below is located minimal configuration for this file.
 
 ```javascript
 // tailwind.config.js
 
 module.exports = {
-    content: [
-        "./your_project/**/*.{html,py,js}"
-    ],
-    // In case custom colors are defined in UNFOLD["COLORS"]
-    colors: {
-        primary: {
-          100: "rgb(var(--color-primary-100) / <alpha-value>)",
-          200: "rgb(var(--color-primary-200) / <alpha-value>)",
-          300: "rgb(var(--color-primary-300) / <alpha-value>)",
-          400: "rgb(var(--color-primary-400) / <alpha-value>)",
-          500: "rgb(var(--color-primary-500) / <alpha-value>)",
-          600: "rgb(var(--color-primary-600) / <alpha-value>)",
-          700: "rgb(var(--color-primary-700) / <alpha-value>)",
-          800: "rgb(var(--color-primary-800) / <alpha-value>)",
-          900: "rgb(var(--color-primary-900) / <alpha-value>)"
-        }
-    }
-}
+  content: ["./your_project/**/*.{html,py,js}"],
+  // In case custom colors are defined in UNFOLD["COLORS"]
+  colors: {
+    primary: {
+      100: "rgb(var(--color-primary-100) / <alpha-value>)",
+      200: "rgb(var(--color-primary-200) / <alpha-value>)",
+      300: "rgb(var(--color-primary-300) / <alpha-value>)",
+      400: "rgb(var(--color-primary-400) / <alpha-value>)",
+      500: "rgb(var(--color-primary-500) / <alpha-value>)",
+      600: "rgb(var(--color-primary-600) / <alpha-value>)",
+      700: "rgb(var(--color-primary-700) / <alpha-value>)",
+      800: "rgb(var(--color-primary-800) / <alpha-value>)",
+      900: "rgb(var(--color-primary-900) / <alpha-value>)",
+    },
+  },
+};
 ```
 
 Once the configuration file is set, it is possible to compile new styles which can be loaded into admin by using **STYLES** key in **UNFOLD** dict.
 
 ```bash
 npx tailwindcss  -o your_project/static/css/styles.css --watch --minify
 ```
@@ -622,15 +620,15 @@
 
 ### Poetry Configuration
 
 To add a new feature or fix the easiest approach is to use django-unfold in combination with Poetry. The process looks like:
 
 - Install django-unfold via `poetry add django-unfold`
 - After that it is needed to git clone the repository somewhere on local computer.
-- Edit *pyproject.toml* and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`
+- Edit _pyproject.toml_ and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`
 - Lock and update via `poetry lock && poetry update`
 
 ### Compiling Tailwind
 
 At the moment project contains package.json with all dependencies required to compile new CSS file. Tailwind configuration file is set to check all html, js and py files for Tailwind's classeses occurrences.
 
 ```bash
```

### Comparing `django_unfold-0.6.0/pyproject.toml` & `django_unfold-0.6.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 [tool.poetry]
 name = "django-unfold"
-version = "0.6.0"
+version = "0.6.1"
 description = "Clean & minimal Django admin theme based on Tailwind CSS"
 license = "MIT"
 readme = "README.md"
 authors = []
 homepage = "https://unfoldadmin.com"
-repository = "https://github.com/remastr/django-unfold"
+repository = "https://github.com/unfoldadmin/django-unfold"
 packages = [
     { include = "unfold", from = "src" },
 ]
 keywords = [
     "django",
     "admin",
     "tailwind",
```

### Comparing `django_unfold-0.6.0/src/unfold/admin.py` & `django_unfold-0.6.1/src/unfold/admin.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/checks.py` & `django_unfold-0.6.1/src/unfold/checks.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/admin.py` & `django_unfold-0.6.1/src/unfold/contrib/filters/admin.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/forms.py` & `django_unfold-0.6.1/src/unfold/contrib/filters/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css` & `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js` & `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js` & `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js` & `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js` & `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html` & `django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/css/trix.css` & `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/css/trix.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js` & `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/forms/static/unfold/forms/js/trix.js` & `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html` & `django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/forms/widgets.py` & `django_unfold-0.6.1/src/unfold/contrib/forms/widgets.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/forms.py` & `django_unfold-0.6.1/src/unfold/contrib/import_export/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/export.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/export.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html` & `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/decorators.py` & `django_unfold-0.6.1/src/unfold/decorators.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/forms.py` & `django_unfold-0.6.1/src/unfold/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/settings.py` & `django_unfold-0.6.1/src/unfold/settings.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/sites.py` & `django_unfold-0.6.1/src/unfold/sites.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/css/simplebar.css` & `django_unfold-0.6.1/src/unfold/static/unfold/css/simplebar.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/css/styles.css` & `django_unfold-0.6.1/src/unfold/static/unfold/css/styles.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/js/alpine.js` & `django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/js/alpine.persist.js` & `django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.persist.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/js/app.js` & `django_unfold-0.6.1/src/unfold/static/unfold/js/app.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/js/htmx.js` & `django_unfold-0.6.1/src/unfold/static/unfold/js/htmx.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/static/unfold/js/simplebar.js` & `django_unfold-0.6.1/src/unfold/static/unfold/js/simplebar.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/actions.html` & `django_unfold-0.6.1/src/unfold/templates/admin/actions.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/app_index.html` & `django_unfold-0.6.1/src/unfold/templates/admin/app_index.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/app_list.html` & `django_unfold-0.6.1/src/unfold/templates/admin/app_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/auth/user/change_password.html` & `django_unfold-0.6.1/src/unfold/templates/admin/auth/user/change_password.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/base.html` & `django_unfold-0.6.1/src/unfold/templates/admin/base.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/change_form.html` & `django_unfold-0.6.1/src/unfold/templates/admin/change_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/change_form_object_tools.html` & `django_unfold-0.6.1/src/unfold/templates/admin/change_form_object_tools.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/change_list.html` & `django_unfold-0.6.1/src/unfold/templates/admin/change_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/change_list_object_tools.html` & `django_unfold-0.6.1/src/unfold/templates/admin/change_list_object_tools.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/change_list_results.html` & `django_unfold-0.6.1/src/unfold/templates/admin/change_list_results.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/date_hierarchy.html` & `django_unfold-0.6.1/src/unfold/templates/admin/date_hierarchy.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/delete_confirmation.html` & `django_unfold-0.6.1/src/unfold/templates/admin/delete_confirmation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/delete_selected_confirmation.html` & `django_unfold-0.6.1/src/unfold/templates/admin/delete_selected_confirmation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/edit_inline/stacked.html` & `django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/stacked.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/edit_inline/tabular.html` & `django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/tabular.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/filter.html` & `django_unfold-0.6.1/src/unfold/templates/admin/filter.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/includes/fieldset.html` & `django_unfold-0.6.1/src/unfold/templates/admin/includes/fieldset.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/index.html` & `django_unfold-0.6.1/src/unfold/templates/admin/index.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/login.html` & `django_unfold-0.6.1/src/unfold/templates/admin/login.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/nav_sidebar.html` & `django_unfold-0.6.1/src/unfold/templates/admin/nav_sidebar.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/object_history.html` & `django_unfold-0.6.1/src/unfold/templates/admin/object_history.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/pagination.html` & `django_unfold-0.6.1/src/unfold/templates/admin/pagination.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/search_form.html` & `django_unfold-0.6.1/src/unfold/templates/admin/search_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/submit_line.html` & `django_unfold-0.6.1/src/unfold/templates/admin/submit_line.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/widgets/clearable_file_input.html` & `django_unfold-0.6.1/src/unfold/templates/admin/widgets/clearable_file_input.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/widgets/related_widget_wrapper.html` & `django_unfold-0.6.1/src/unfold/templates/admin/widgets/related_widget_wrapper.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/admin/widgets/split_datetime.html` & `django_unfold-0.6.1/src/unfold/templates/admin/widgets/split_datetime.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/auth/widgets/read_only_password_hash.html` & `django_unfold-0.6.1/src/unfold/templates/auth/widgets/read_only_password_hash.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/registration/logged_out.html` & `django_unfold-0.6.1/src/unfold/templates/registration/logged_out.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/registration/password_change_done.html` & `django_unfold-0.6.1/src/unfold/templates/registration/password_change_done.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/registration/password_change_form.html` & `django_unfold-0.6.1/src/unfold/templates/registration/password_change_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/actions_row.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/actions_row.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/app_list.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/app_list_default.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list_default.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/display_label.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_label.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/history.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/history.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages/error.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/error.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/messages.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/navigation.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/navigation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/search.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/search_results.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search_results.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/tab_list.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/tab_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/userlinks.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/userlinks.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/helpers/welcomemsg.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/welcomemsg.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/layouts/base_simple.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/layouts/base_simple.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/layouts/skeleton.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/layouts/skeleton.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/widgets/clearable_file_input_small.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/widgets/clearable_file_input_small.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templates/unfold/widgets/split_datetime_vertical.html` & `django_unfold-0.6.1/src/unfold/templates/unfold/widgets/split_datetime_vertical.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templatetags/unfold.py` & `django_unfold-0.6.1/src/unfold/templatetags/unfold.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/templatetags/unfold_list.py` & `django_unfold-0.6.1/src/unfold/templatetags/unfold_list.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/typing.py` & `django_unfold-0.6.1/src/unfold/typing.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/utils.py` & `django_unfold-0.6.1/src/unfold/utils.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/views.py` & `django_unfold-0.6.1/src/unfold/views.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/src/unfold/widgets.py` & `django_unfold-0.6.1/src/unfold/widgets.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.0/setup.py` & `django_unfold-0.6.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -37,17 +37,17 @@
  'unfold.contrib.import_export': ['templates/admin/import_export/*']}
 
 install_requires = \
 ['django>=3.2']
 
 setup_kwargs = {
     'name': 'django-unfold',
-    'version': '0.6.0',
+    'version': '0.6.1',
     'description': 'Clean & minimal Django admin theme based on Tailwind CSS',
-    'long_description': '![Screenshot - Objects Listing](https://github.com/remastr/django-unfold/raw/main/screenshot-1.jpg)\n\n![Screenshot - Login Page](https://github.com/remastr/django-unfold/raw/main/screenshot-2.jpg)\n\n## Unfold Django Admin Theme\n\nUnfold is a new theme for Django Admin incorporating some most common practises for building full-fledged admin areas.\n\n- **Visual**: provides new user interface based on Tailwind CSS framework\n- **Sidebar:** simplifies definition of custom sidebar navigation\n- **Dark mode:** supports both light and dark mode versions\n- **Configuration:** most of the basic options can be changed in settings.py\n- **Dependencies:** completely based only on `django.contrib.admin`\n- **Filters:** custom widgets for filters (e.g. numeric filter)\n- **Actions:** multiple ways how to define actions within different parts of admin\n\n## Table of Contents\n\n- [Unfold Django Admin Theme](#unfold-django-admin-theme)\n- [Table of Contents](#table-of-contents)\n- [Installation](#installation)\n- [Configuration](#configuration)\n  - [Available settings.py options](#available-settingspy-options)\n  - [Available unfold.admin.ModelAdmin options](#available-unfoldadminmodeladmin-options)\n- [Decorators](#decorators)\n  - [@display](#display)\n- [Actions](#actions)\n  - [Actions overview](#actions-overview)\n  - [Custom unfold @action decorator](#custom-unfold-action-decorator)\n  - [Action handler functions](#action-handler-functions)\n    - [For submit row action](#for-submit-row-action)\n    - [For global, row and detail action](#for-global-row-and-detail-action)\n  - [Action examples](#action-examples)\n- [Filters](#filters)\n- [Third party packages](#third-party-packages)\n  - [django-import-export](#django-import-export)\n- [User Admin Form](#user-admin-form)\n- [Adding Custom Styles and Scripts](#adding-custom-styles-and-scripts)\n- [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet)\n- [Custom Admin Dashboard](#custom-admin-dashboard)\n- [Unfold Development](#unfold-development)\n  - [Pre-commit](#pre-commit)\n  - [Poetry Configuration](#poetry-configuration)\n  - [Compiling Tailwind](#compiling-tailwind)\n\n## Installation\n\nThe installation process is minimal. Everything what is needed after installation is to put new application at the beginning of **INSTALLED_APPS**. Default admin configuration in urls.py can stay as it is and there are no changes required.\n\n```python\n# settings.py\n\nINSTALLED_APPS = [\n    "unfold",  # before django.contrib.admin\n    "unfold.contrib.filters",  # optional, if special filters are needed\n    "unfold.contrib.forms",  # optional, if special form elements are needed\n    "unfold.contrib.import_export",  # optional, if django-import-export package is used\n    "django.contrib.admin",  # required\n]\n```\n\nIn case you need installation command below are the versions for `pip` and `poetry` which needs to be executed in shell.\n\n```bash\npip install django-unfold\npoetry add django-unfold\n```\n\nJust for an example below is the minimal admin configuration in terms of adding Unfold into URL paths.\n\n```python\n# urls.py\n\nfrom django.contrib import admin\nfrom django.urls import path\n\nurlpatterns = [\n    path("admin/", admin.site.urls),\n    # Other URL paths\n]\n```\n\nAfter installation, it is required that admin classes are going to inherit from custom `ModelAdmin` available in `unfold.admin`.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom unfold.admin import ModelAdmin\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    pass\n```\n\n**Note:** Registered admin models coming from third party packages are not going to properly work with Unfold because of parent class. By default, these models are registered by using `django.contrib.admin.ModelAdmin` but it is needed to use `unfold.admin.ModelAdmin`. Solution for this problem is to unregister model and then again register it back by using `unfold.admin.ModelAdmin`.\n\n```python\n# admin.py\nfrom django.contrib import admin\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\n\n\nadmin.site.unregister(User)\n\n\n@admin.register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    pass\n```\n\n## Configuration\n\n### Available settings.py options\n```python\n# settings.py\n\nfrom django.templatetags.static import static\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\n\nUNFOLD = {\n    "SITE_TITLE": None,\n    "SITE_HEADER": None,\n    "SITE_URL": "/",\n    "SITE_ICON": lambda request: static("logo.svg"),\n    "SITE_SYMBOL": "speed",  # symbol from icon set\n    "DASHBOARD_CALLBACK": "sample_app.dashboard_callback",\n    "LOGIN": {\n        "image": lambda r: static("sample/login-bg.jpg"),\n        "redirect_after": lambda r: reverse_lazy("admin:APP_MODEL_changelist"),\n    },\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n    "COLORS": {\n        "primary": {\n            "50": "250 245 255",\n            "100": "243 232 255",\n            "200": "233 213 255",\n            "300": "216 180 254",\n            "400": "192 132 252",\n            "500": "168 85 247",\n            "600": "147 51 234",\n            "700": "126 34 206",\n            "800": "107 33 168",\n            "900": "88 28 135",\n        },\n    },\n    "EXTENSIONS": {\n        "modeltranslation": {\n            "flags": {\n                "en": "🇬🇧",\n                "fr": "🇫🇷",\n                "nl": "🇧🇪",\n            },\n        },\n    },\n    "SIDEBAR": {\n        "show_search": False,  # Search in applications and models names\n        "show_all_applications": False,  # Dropdown with all applications and models\n        "navigation": [\n            {\n                "title": _("Navigation"),\n                "separator": True,  # Top border\n                "items": [\n                    {\n                        "title": _("Dashboard"),\n                        "icon": "dashboard",  # Supported icon set: https://fonts.google.com/icons\n                        "link": reverse_lazy("admin:index"),\n                        "badge": "sample_app.badge_callback",\n                    },\n                    {\n                        "title": _("Users"),\n                        "icon": "people",\n                        "link": reverse_lazy("admin:users_user_changelist"),\n                    },\n                ],\n            },\n        ],\n    },\n    "TABS": [\n        {\n            "models": [\n                "app_label.model_name_in_lowercase",\n            ],\n            "items": [\n                {\n                    "title": _("Your custom title"),\n                    "link": reverse_lazy("admin:app_label_model_name_changelist"),\n                },\n            ],\n        },\n    ],\n}\n\n\ndef dashboard_callback(request, context):\n    """\n    Callback to prepare custom variables for index template which is used as dashboard\n    template. It can be overridden in application by creating custom admin/index.html.\n    """\n    context.update(\n        {\n            "sample": "example",  # this will be injected into templates/admin/index.html\n        }\n    )\n    return context\n\n\ndef badge_callback(request):\n    return 3\n```\n\n### Available unfold.admin.ModelAdmin options\n\n```python\nfrom django import models\nfrom django.contrib import admin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.forms.widgets import WysiwygWidget\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    # Preprocess content of readonly fields before render\n    readonly_preprocess_fields = {\n        "model_field_name": "html.unescape",\n        "other_field_name": lambda content: content.strip(),\n    }\n\n    # Display submit button in filters\n    list_filter_submit = False\n\n    # Custom actions\n    actions_list = []  # Displayed above the results list\n    actions_row = []  # Displayed in a table row in results list\n    actions_detail = []  # Displayed at the top of for in object detail\n    actions_submit_line = []  # Displayed near save in object detail\n\n    formfield_overrides = {\n        models.TextField: WysiwygWidget,\n    }\n```\n\n## Decorators\n\n### @display\n\nUnfold introduces it\'s own `unfold.decorators.display` decorator. By default it has exactly same behavior as native `django.contrib.admin.decorators.display` but it adds same customizations which helps to extends default logic.\n\n`@display(label=True)`, `@display(label={"value1": "success"})` displays a result as a label. This option fits for different types of statuses. Label can be either boolean indicating we want to use label with default color or dict where the dict is responsible for displaying labels in different colors. At the moment these color combinations are supported: success(green), info(blue), danger(red) and warning(orange).\n\n`@display(header=True)` displays in results list two information in one table cell. Good example is when we want to display customer information, first line is going to be customer\'s name and right below the name display corresponding email address. Method with such a decorator is supposed to return a list with two elements `return "Full name", "E-mail address"`.\n\n```python\n# models.py\n\nfrom django.db.models import TextChoices\nfrom django.utils.translation import gettext_lazy as _\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import display\n\n\nclass UserStatus(TextChoices):\n    ACTIVE = "ACTIVE", _("Active")\n    PENDING = "PENDING", _("Pending")\n    INACTIVE = "INACTIVE", _("Inactive")\n    CANCELLED = "CANCELLED", _("Cancelled")\n\n\nclass UserAdmin(ModelAdmin):\n    list_display = [\n        "display_as_two_line_heading",\n        "show_status",\n        "show_status_with_custom_label",\n    ]\n\n    @display(\n        description=_("Status"),\n        ordering="status",\n        label=True,\n        mapping={\n            UserStatus.ACTIVE: "success",\n            UserStatus.PENDING: "info",\n            UserStatus.INACTIVE: "warning",\n            UserStatus.CANCELLED: "danger",\n        },\n    )\n    def show_status(self, obj):\n        return obj.status\n\n    @display(description=_("Status with label"), ordering="status", label=True)\n    def show_status_with_custom_label(self, obj):\n        return obj.status, obj.get_status_display()\n\n    @display(header=True)\n    def display_as_two_line_heading(self, obj):\n        return "First main heading", "Smaller additional description"\n```\n\n## Actions\n\nIt is highly recommended to read the base [Django actions documentation](https://docs.djangoproject.com/en/4.2/ref/contrib/admin/actions/) before reading this section, since Unfold actions are derived from Django actions.\n\n### Actions overview\n\nBesides traditional actions selected from dropdown, Unfold supports several other types of actions. Following table\ngives overview of all available actions together with their recommended usage:\n\n| Type of action | Appearance                               | Usage                                                                                      | Examples of usage                      |\n|----------------|------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------|\n| Default        | List view - top of listing (in dropdown) | Actions, where you want to select specific subset of instances to perform this action upon | Bulk deleting, bulk activation         |\n| Global         | List view - top of listing (as buttons)  | General actions for model, without selecting specific instances                            | Import, export                         |\n| Row            | List view - in each row                  | Action for one specific instance, executable from listing                                  | Activation, sync with external service |\n| Detail         | Detail view - top of detail              | Action for one specific instance, executable from detail                                   | Activation, sync with external service |\n| Submit line    | Detail view - near submit button         | Action performed during form submit (instance save)                                        | Publishing article together with save  |\n\n### Custom unfold @action decorator\n\nUnfold also uses custom `@action` decorator, supporting 2 more parameters in comparison to base `@action` decorator:\n- `url_path`: Action path name, used to override the path under which the action will be available\n  (if not provided, URL path will be generated by Unfold)\n- `attrs`: Dictionary of the additional attributes added to the `<a>` element, used for e.g. opening action in new tab (`{"target": "_blank"}`)\n\n### Action handler functions\n\nThis section provides explanation of how the action handler functions should be constructed for Unfold actions.\nFor default actions, follow official Django admin documentation.\n\n#### For submit row action\n\nSubmit row actions work a bit differently when compared to other custom Unfold actions.\nThese actions first invoke form save (same as if you hit `Save` button) and then lets you\nperform additional logic on already saved instance.\n\n#### For global, row and detail action\n\nAll these actions are based on custom URLs generated for each of them. Handler function for these views is\nbasically function based view.\n\nFor actions without intermediate steps, you can write all the logic inside handler directly. Request and object ID\nare both passed to these action handler functions, so you are free to fetch the instance from database and perform any\noperations with it. In the end, it is recommended to return redirect back to either detail or listing, based on where\nthe action was triggered from.\n\nFor actions with intermediate steps, it is recommended to use handler function only to redirect to custom URL with custom\nview. This view can be extended from base Unfold view, to have unified experience.\n\nIf that\'s confusing, there are examples for both these actions in next section.\n\n### Action examples\n\n```python\n# admin.py\n\nfrom django.db.models import Model\nfrom django.contrib.admin import register\nfrom django.shortcuts import redirect\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\nfrom django.http import HttpRequest\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import action\n\n\nclass User(Model):\n    pass\n\n\n@register(User)\nclass UserAdmin(ModelAdmin):\n    actions_list = ["changelist_global_action_import"]\n    actions_row = ["changelist_row_action_view_on_website"]\n    actions_detail = ["change_detail_action_block"]\n    actions_submit_line = ["submit_line_action_activate"]\n\n    @action(description=_("Save & Activate"))\n    def submit_line_action_activate(self, request: HttpRequest, obj: User):\n        """\n        If instance is modified in any way, it also needs to be saved,\n        since this handler is invoked after instance is saved.\n        :param request:\n        :param obj: Model instance that was manipulated, with changes already saved to database\n        :return: None, this handler should not return anything\n        """\n        obj.is_active = True\n        obj.save()\n\n    @action(description=_("Import"), url_path="import")\n    def changelist_global_action_import(self, request: HttpRequest):\n        """\n        Handler for global actions does not receive any queryset or object ids, because it is\n        meant to be used for general actions for given model.\n        :param request:\n        :return: View, as described in section above\n        """\n        # This is example of action redirecting to custom page, where the action will be handled\n        # (with intermediate steps)\n        return redirect(\n          reverse_lazy("view-where-import-will-be-handled")\n        )\n\n    @action(description=_("Row"), url_path="row-action", attrs={"target": "_blank"})\n    def changelist_row_action_view_on_website(self, request: HttpRequest, object_id: int):\n        """\n        Handler for list row action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        return redirect(f"https://example.com/{object_id}")\n\n    @action(description=_("Detail"), url_path="detail-action", attrs={"target": "_blank"})\n    def change_detail_action_block(self, request: HttpRequest, object_id: int):\n        """\n        Handler for detail action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        # This is example of action that handled whole logic inside handler\n        # function and redirects back to object detail\n        user = User.objects.get(pk=object_id)\n        user.block()\n        return redirect(\n            reverse_lazy("admin:users_user_change", args=(object_id,))\n        )\n```\n\n## Filters\n\nBy default, Django admin handles all filters as regular HTML links pointing at the same URL with different query parameters. This approach is for basic filtering more than enough. In the case of more advanced filtering by incorporating input fields, it is not going to work.\n\nCurrently, Unfold implements numeric filters inside `unfold.contrib.filters` application. In order to use these filters, it is required to add this application into `INSTALLED_APPS` in `settings.py` right after `unfold` application.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.filters.admin import (\n    RangeNumericListFilter,\n    RangeNumericFilter,\n    SingleNumericFilter,\n    SliderNumericFilter,\n    RangeDateFilter,\n    RangeDateTimeFilter,\n)\n\n\nclass CustomSliderNumericFilter(SliderNumericFilter):\n    MAX_DECIMALS = 2\n    STEP = 10\n\n\nclass CustomRangeNumericListFilter(RangeNumericListFilter):\n    parameter_name = "items_count"\n    title = "items"\n\n\n@admin.register(User)\nclass YourModelAdmin(ModelAdmin):\n    list_filter_submit = True  # Submit button at the bottom of the filter\n    list_filter = (\n        ("field_A", SingleNumericFilter),  # Numeric single field search, __gte lookup\n        ("field_B", RangeNumericFilter),  # Numeric range search, __gte and __lte lookup\n        ("field_C", SliderNumericFilter),  # Numeric range filter but with slider\n        ("field_D", CustomSliderNumericFilter),  # Numeric filter with custom attributes\n        ("field_E", RangeDateFilter),  # Date filter\n        ("field_F", RangeDateTimeFilter),  # Datetime filter\n        CustomRangeNumericListFilter,  # Numeric range search not restricted to a model field\n    )\n\n    def get_queryset(self, request):\n        return super().get_queryset().annotate(items_count=Count("item", distinct=True))\n```\n\n\n## Third party packages\n\n\n### django-import-export\n\nTo get proper visual appearance for django-import-export, two things are needed\n\n1. Add `unfold.contrib.import_export` to `INSTALLED_APPS` at the begging of the file. This action will override all templates coming from the plugin.\n2. Change `import_form_class` and `export_form_class` in ModelAdmin which is inheriting from `ImportExportModelAdmin`. This chunk of code is responsible for adding proper styling to form elements.\n\n```python\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.import_export.forms import ExportForm, ImportForm\n\nclass ExampleAdmin(ModelAdmin, ImportExportModelAdmin):\n    import_form_class = ImportForm\n    export_form_class = ExportForm\n```\n\n## User Admin Form\n\nUser\'s admin in Django is specific as it contains several forms which are requiring custom styling. All of these forms has been inherited and accordingly adjusted. In user admin class it is needed to use these inherited form classes to enable custom styling matching rest of the website.\n\n```python\n# models.py\n\nfrom django.contrib.admin import register\nfrom django.contrib.auth.models import User\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.forms import AdminPasswordChangeForm, UserChangeForm, UserCreationForm\n\n\n@register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    form = UserChangeForm\n    add_form = UserCreationForm\n    change_password_form = AdminPasswordChangeForm\n```\n\n## Adding Custom Styles and Scripts\n\nTo add new custom styles, for example for custom dashboard, it is possible to load them via **STYLES** key in **UNFOLD** dict. This key accepts a list of strings or lambda functions which will be loaded on all pages. JavaScript files can be loaded by using similar apprach, but **SCRIPTS** is used.\n\n```python\n# settings.py\n\nfrom django.templatetags.static import static\n\nUNFOLD = {\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n}\n```\n\n## Project Level Tailwind Stylesheet\n\nWhen creating custom dashboard or adding custom components, it is needed to add own styles. Adding custom styles is described above. Most of the time, it is supposed that new elements are going to match with the rest of the administration panel. First of all, create tailwind.config.js in your application. Below is located minimal configuration for this file.\n\n```javascript\n// tailwind.config.js\n\nmodule.exports = {\n    content: [\n        "./your_project/**/*.{html,py,js}"\n    ],\n    // In case custom colors are defined in UNFOLD["COLORS"]\n    colors: {\n        primary: {\n          100: "rgb(var(--color-primary-100) / <alpha-value>)",\n          200: "rgb(var(--color-primary-200) / <alpha-value>)",\n          300: "rgb(var(--color-primary-300) / <alpha-value>)",\n          400: "rgb(var(--color-primary-400) / <alpha-value>)",\n          500: "rgb(var(--color-primary-500) / <alpha-value>)",\n          600: "rgb(var(--color-primary-600) / <alpha-value>)",\n          700: "rgb(var(--color-primary-700) / <alpha-value>)",\n          800: "rgb(var(--color-primary-800) / <alpha-value>)",\n          900: "rgb(var(--color-primary-900) / <alpha-value>)"\n        }\n    }\n}\n```\n\nOnce the configuration file is set, it is possible to compile new styles which can be loaded into admin by using **STYLES** key in **UNFOLD** dict.\n\n```bash\nnpx tailwindcss  -o your_project/static/css/styles.css --watch --minify\n```\n\n## Custom Admin Dashboard\n\nThe most common thing which needs to be adjusted for each project in admin is the dashboard. By default Unfold does not provide any dashboard components. The default dashboard experience with list of all applications and models is kept with proper styling matching rest of the components but thats it. Anyway, Unfold was created that creation of custom dashboard will be streamlined.\n\nCreate `templates/admin/index.html` in your project and paste the base template below into it. By default, all your custom styles here are not compiled because CSS classes are located in your specific project. Here it is needed to set up the Tailwind for your project and all requried instructions are located in [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet) chapter.\n\n```\n{% extends \'unfold/layouts/base_simple.html\' %}\n\n{% load cache humanize i18n %}\n\n{% block breadcrumbs %}{% endblock %}\n\n{% block title %}{% if subtitle %}{{ subtitle }} | {% endif %}{{ title }} | {{ site_title|default:_(\'Django site admin\') }}{% endblock %}\n\n{% block branding %}\n    <h1 id="site-name"><a href="{% url \'admin:index\' %}">{{ site_header|default:_(\'Django administration\') }}</a></h1>\n{% endblock %}\n\n{% block content %}\n    Start creating your own Tailwind components here\n{% endblock %}\n```\n\nNote: In case that it is needed to pass custom variables into dashboard tamplate, check **DASHOARD_CALLBACK** in **UNFOLD** dict.\n\n## Unfold Development\n\n### Pre-commit\n\nBefore adding any source code, it is recommended to have pre-commit installed on your local computer to check for all potential issues when comitting the code.\n\n```bash\npip install pre-commit\npre-commit install\npre-commit install --hook-type commit-msg\n```\n\n### Poetry Configuration\n\nTo add a new feature or fix the easiest approach is to use django-unfold in combination with Poetry. The process looks like:\n\n- Install django-unfold via `poetry add django-unfold`\n- After that it is needed to git clone the repository somewhere on local computer.\n- Edit *pyproject.toml* and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`\n- Lock and update via `poetry lock && poetry update`\n\n### Compiling Tailwind\n\nAt the moment project contains package.json with all dependencies required to compile new CSS file. Tailwind configuration file is set to check all html, js and py files for Tailwind\'s classeses occurrences.\n\n```bash\nnpm install\nnpx tailwindcss -i styles.css -o src/unfold/static/unfold/css/styles.css --watch --minify\n\nnpm run tailwind:watch # run after each change in code\nnpm run tailwind:build # run once\n```\n\nSome components like datepickers, calendars or selectors in admin was not possible to style by overriding html templates so their default styles are overriden in **styles.css**.\n\nNone: most of the custom styles localted in style.css are created via `@apply some-tailwind-class;`.\n',
+    'long_description': '![Screenshot - Objects Listing](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-1.jpg)\n\n![Screenshot - Login Page](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-2.jpg)\n\n## Unfold Django Admin Theme\n\nUnfold is a new theme for Django Admin incorporating some most common practises for building full-fledged admin areas.\n\n- **Visual**: provides new user interface based on Tailwind CSS framework\n- **Sidebar:** simplifies definition of custom sidebar navigation\n- **Dark mode:** supports both light and dark mode versions\n- **Configuration:** most of the basic options can be changed in settings.py\n- **Dependencies:** completely based only on `django.contrib.admin`\n- **Filters:** custom widgets for filters (e.g. numeric filter)\n- **Actions:** multiple ways how to define actions within different parts of admin\n\n## Table of Contents\n\n- [Unfold Django Admin Theme](#unfold-django-admin-theme)\n- [Table of Contents](#table-of-contents)\n- [Installation](#installation)\n- [Configuration](#configuration)\n  - [Available settings.py options](#available-settingspy-options)\n  - [Available unfold.admin.ModelAdmin options](#available-unfoldadminmodeladmin-options)\n- [Decorators](#decorators)\n  - [@display](#display)\n- [Actions](#actions)\n  - [Actions overview](#actions-overview)\n  - [Custom unfold @action decorator](#custom-unfold-action-decorator)\n  - [Action handler functions](#action-handler-functions)\n    - [For submit row action](#for-submit-row-action)\n    - [For global, row and detail action](#for-global-row-and-detail-action)\n  - [Action examples](#action-examples)\n- [Filters](#filters)\n- [Third party packages](#third-party-packages)\n  - [django-import-export](#django-import-export)\n- [User Admin Form](#user-admin-form)\n- [Adding Custom Styles and Scripts](#adding-custom-styles-and-scripts)\n- [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet)\n- [Custom Admin Dashboard](#custom-admin-dashboard)\n- [Unfold Development](#unfold-development)\n  - [Pre-commit](#pre-commit)\n  - [Poetry Configuration](#poetry-configuration)\n  - [Compiling Tailwind](#compiling-tailwind)\n\n## Installation\n\nThe installation process is minimal. Everything what is needed after installation is to put new application at the beginning of **INSTALLED_APPS**. Default admin configuration in urls.py can stay as it is and there are no changes required.\n\n```python\n# settings.py\n\nINSTALLED_APPS = [\n    "unfold",  # before django.contrib.admin\n    "unfold.contrib.filters",  # optional, if special filters are needed\n    "unfold.contrib.forms",  # optional, if special form elements are needed\n    "unfold.contrib.import_export",  # optional, if django-import-export package is used\n    "django.contrib.admin",  # required\n]\n```\n\nIn case you need installation command below are the versions for `pip` and `poetry` which needs to be executed in shell.\n\n```bash\npip install django-unfold\npoetry add django-unfold\n```\n\nJust for an example below is the minimal admin configuration in terms of adding Unfold into URL paths.\n\n```python\n# urls.py\n\nfrom django.contrib import admin\nfrom django.urls import path\n\nurlpatterns = [\n    path("admin/", admin.site.urls),\n    # Other URL paths\n]\n```\n\nAfter installation, it is required that admin classes are going to inherit from custom `ModelAdmin` available in `unfold.admin`.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom unfold.admin import ModelAdmin\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    pass\n```\n\n**Note:** Registered admin models coming from third party packages are not going to properly work with Unfold because of parent class. By default, these models are registered by using `django.contrib.admin.ModelAdmin` but it is needed to use `unfold.admin.ModelAdmin`. Solution for this problem is to unregister model and then again register it back by using `unfold.admin.ModelAdmin`.\n\n```python\n# admin.py\nfrom django.contrib import admin\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\n\n\nadmin.site.unregister(User)\n\n\n@admin.register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    pass\n```\n\n## Configuration\n\n### Available settings.py options\n\n```python\n# settings.py\n\nfrom django.templatetags.static import static\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\n\nUNFOLD = {\n    "SITE_TITLE": None,\n    "SITE_HEADER": None,\n    "SITE_URL": "/",\n    "SITE_ICON": lambda request: static("logo.svg"),\n    "SITE_SYMBOL": "speed",  # symbol from icon set\n    "DASHBOARD_CALLBACK": "sample_app.dashboard_callback",\n    "LOGIN": {\n        "image": lambda r: static("sample/login-bg.jpg"),\n        "redirect_after": lambda r: reverse_lazy("admin:APP_MODEL_changelist"),\n    },\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n    "COLORS": {\n        "primary": {\n            "50": "250 245 255",\n            "100": "243 232 255",\n            "200": "233 213 255",\n            "300": "216 180 254",\n            "400": "192 132 252",\n            "500": "168 85 247",\n            "600": "147 51 234",\n            "700": "126 34 206",\n            "800": "107 33 168",\n            "900": "88 28 135",\n        },\n    },\n    "EXTENSIONS": {\n        "modeltranslation": {\n            "flags": {\n                "en": "🇬🇧",\n                "fr": "🇫🇷",\n                "nl": "🇧🇪",\n            },\n        },\n    },\n    "SIDEBAR": {\n        "show_search": False,  # Search in applications and models names\n        "show_all_applications": False,  # Dropdown with all applications and models\n        "navigation": [\n            {\n                "title": _("Navigation"),\n                "separator": True,  # Top border\n                "items": [\n                    {\n                        "title": _("Dashboard"),\n                        "icon": "dashboard",  # Supported icon set: https://fonts.google.com/icons\n                        "link": reverse_lazy("admin:index"),\n                        "badge": "sample_app.badge_callback",\n                    },\n                    {\n                        "title": _("Users"),\n                        "icon": "people",\n                        "link": reverse_lazy("admin:users_user_changelist"),\n                    },\n                ],\n            },\n        ],\n    },\n    "TABS": [\n        {\n            "models": [\n                "app_label.model_name_in_lowercase",\n            ],\n            "items": [\n                {\n                    "title": _("Your custom title"),\n                    "link": reverse_lazy("admin:app_label_model_name_changelist"),\n                },\n            ],\n        },\n    ],\n}\n\n\ndef dashboard_callback(request, context):\n    """\n    Callback to prepare custom variables for index template which is used as dashboard\n    template. It can be overridden in application by creating custom admin/index.html.\n    """\n    context.update(\n        {\n            "sample": "example",  # this will be injected into templates/admin/index.html\n        }\n    )\n    return context\n\n\ndef badge_callback(request):\n    return 3\n```\n\n### Available unfold.admin.ModelAdmin options\n\n```python\nfrom django import models\nfrom django.contrib import admin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.forms.widgets import WysiwygWidget\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    # Preprocess content of readonly fields before render\n    readonly_preprocess_fields = {\n        "model_field_name": "html.unescape",\n        "other_field_name": lambda content: content.strip(),\n    }\n\n    # Display submit button in filters\n    list_filter_submit = False\n\n    # Custom actions\n    actions_list = []  # Displayed above the results list\n    actions_row = []  # Displayed in a table row in results list\n    actions_detail = []  # Displayed at the top of for in object detail\n    actions_submit_line = []  # Displayed near save in object detail\n\n    formfield_overrides = {\n        models.TextField: WysiwygWidget,\n    }\n```\n\n## Decorators\n\n### @display\n\nUnfold introduces it\'s own `unfold.decorators.display` decorator. By default it has exactly same behavior as native `django.contrib.admin.decorators.display` but it adds same customizations which helps to extends default logic.\n\n`@display(label=True)`, `@display(label={"value1": "success"})` displays a result as a label. This option fits for different types of statuses. Label can be either boolean indicating we want to use label with default color or dict where the dict is responsible for displaying labels in different colors. At the moment these color combinations are supported: success(green), info(blue), danger(red) and warning(orange).\n\n`@display(header=True)` displays in results list two information in one table cell. Good example is when we want to display customer information, first line is going to be customer\'s name and right below the name display corresponding email address. Method with such a decorator is supposed to return a list with two elements `return "Full name", "E-mail address"`.\n\n```python\n# models.py\n\nfrom django.db.models import TextChoices\nfrom django.utils.translation import gettext_lazy as _\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import display\n\n\nclass UserStatus(TextChoices):\n    ACTIVE = "ACTIVE", _("Active")\n    PENDING = "PENDING", _("Pending")\n    INACTIVE = "INACTIVE", _("Inactive")\n    CANCELLED = "CANCELLED", _("Cancelled")\n\n\nclass UserAdmin(ModelAdmin):\n    list_display = [\n        "display_as_two_line_heading",\n        "show_status",\n        "show_status_with_custom_label",\n    ]\n\n    @display(\n        description=_("Status"),\n        ordering="status",\n        label=True,\n        mapping={\n            UserStatus.ACTIVE: "success",\n            UserStatus.PENDING: "info",\n            UserStatus.INACTIVE: "warning",\n            UserStatus.CANCELLED: "danger",\n        },\n    )\n    def show_status(self, obj):\n        return obj.status\n\n    @display(description=_("Status with label"), ordering="status", label=True)\n    def show_status_with_custom_label(self, obj):\n        return obj.status, obj.get_status_display()\n\n    @display(header=True)\n    def display_as_two_line_heading(self, obj):\n        return "First main heading", "Smaller additional description"\n```\n\n## Actions\n\nIt is highly recommended to read the base [Django actions documentation](https://docs.djangoproject.com/en/4.2/ref/contrib/admin/actions/) before reading this section, since Unfold actions are derived from Django actions.\n\n### Actions overview\n\nBesides traditional actions selected from dropdown, Unfold supports several other types of actions. Following table\ngives overview of all available actions together with their recommended usage:\n\n| Type of action | Appearance                               | Usage                                                                                      | Examples of usage                      |\n| -------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------- |\n| Default        | List view - top of listing (in dropdown) | Actions, where you want to select specific subset of instances to perform this action upon | Bulk deleting, bulk activation         |\n| Global         | List view - top of listing (as buttons)  | General actions for model, without selecting specific instances                            | Import, export                         |\n| Row            | List view - in each row                  | Action for one specific instance, executable from listing                                  | Activation, sync with external service |\n| Detail         | Detail view - top of detail              | Action for one specific instance, executable from detail                                   | Activation, sync with external service |\n| Submit line    | Detail view - near submit button         | Action performed during form submit (instance save)                                        | Publishing article together with save  |\n\n### Custom unfold @action decorator\n\nUnfold also uses custom `@action` decorator, supporting 2 more parameters in comparison to base `@action` decorator:\n\n- `url_path`: Action path name, used to override the path under which the action will be available\n  (if not provided, URL path will be generated by Unfold)\n- `attrs`: Dictionary of the additional attributes added to the `<a>` element, used for e.g. opening action in new tab (`{"target": "_blank"}`)\n\n### Action handler functions\n\nThis section provides explanation of how the action handler functions should be constructed for Unfold actions.\nFor default actions, follow official Django admin documentation.\n\n#### For submit row action\n\nSubmit row actions work a bit differently when compared to other custom Unfold actions.\nThese actions first invoke form save (same as if you hit `Save` button) and then lets you\nperform additional logic on already saved instance.\n\n#### For global, row and detail action\n\nAll these actions are based on custom URLs generated for each of them. Handler function for these views is\nbasically function based view.\n\nFor actions without intermediate steps, you can write all the logic inside handler directly. Request and object ID\nare both passed to these action handler functions, so you are free to fetch the instance from database and perform any\noperations with it. In the end, it is recommended to return redirect back to either detail or listing, based on where\nthe action was triggered from.\n\nFor actions with intermediate steps, it is recommended to use handler function only to redirect to custom URL with custom\nview. This view can be extended from base Unfold view, to have unified experience.\n\nIf that\'s confusing, there are examples for both these actions in next section.\n\n### Action examples\n\n```python\n# admin.py\n\nfrom django.db.models import Model\nfrom django.contrib.admin import register\nfrom django.shortcuts import redirect\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\nfrom django.http import HttpRequest\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import action\n\n\nclass User(Model):\n    pass\n\n\n@register(User)\nclass UserAdmin(ModelAdmin):\n    actions_list = ["changelist_global_action_import"]\n    actions_row = ["changelist_row_action_view_on_website"]\n    actions_detail = ["change_detail_action_block"]\n    actions_submit_line = ["submit_line_action_activate"]\n\n    @action(description=_("Save & Activate"))\n    def submit_line_action_activate(self, request: HttpRequest, obj: User):\n        """\n        If instance is modified in any way, it also needs to be saved,\n        since this handler is invoked after instance is saved.\n        :param request:\n        :param obj: Model instance that was manipulated, with changes already saved to database\n        :return: None, this handler should not return anything\n        """\n        obj.is_active = True\n        obj.save()\n\n    @action(description=_("Import"), url_path="import")\n    def changelist_global_action_import(self, request: HttpRequest):\n        """\n        Handler for global actions does not receive any queryset or object ids, because it is\n        meant to be used for general actions for given model.\n        :param request:\n        :return: View, as described in section above\n        """\n        # This is example of action redirecting to custom page, where the action will be handled\n        # (with intermediate steps)\n        return redirect(\n          reverse_lazy("view-where-import-will-be-handled")\n        )\n\n    @action(description=_("Row"), url_path="row-action", attrs={"target": "_blank"})\n    def changelist_row_action_view_on_website(self, request: HttpRequest, object_id: int):\n        """\n        Handler for list row action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        return redirect(f"https://example.com/{object_id}")\n\n    @action(description=_("Detail"), url_path="detail-action", attrs={"target": "_blank"})\n    def change_detail_action_block(self, request: HttpRequest, object_id: int):\n        """\n        Handler for detail action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        # This is example of action that handled whole logic inside handler\n        # function and redirects back to object detail\n        user = User.objects.get(pk=object_id)\n        user.block()\n        return redirect(\n            reverse_lazy("admin:users_user_change", args=(object_id,))\n        )\n```\n\n## Filters\n\nBy default, Django admin handles all filters as regular HTML links pointing at the same URL with different query parameters. This approach is for basic filtering more than enough. In the case of more advanced filtering by incorporating input fields, it is not going to work.\n\nCurrently, Unfold implements numeric filters inside `unfold.contrib.filters` application. In order to use these filters, it is required to add this application into `INSTALLED_APPS` in `settings.py` right after `unfold` application.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.filters.admin import (\n    RangeNumericListFilter,\n    RangeNumericFilter,\n    SingleNumericFilter,\n    SliderNumericFilter,\n    RangeDateFilter,\n    RangeDateTimeFilter,\n)\n\n\nclass CustomSliderNumericFilter(SliderNumericFilter):\n    MAX_DECIMALS = 2\n    STEP = 10\n\n\nclass CustomRangeNumericListFilter(RangeNumericListFilter):\n    parameter_name = "items_count"\n    title = "items"\n\n\n@admin.register(User)\nclass YourModelAdmin(ModelAdmin):\n    list_filter_submit = True  # Submit button at the bottom of the filter\n    list_filter = (\n        ("field_A", SingleNumericFilter),  # Numeric single field search, __gte lookup\n        ("field_B", RangeNumericFilter),  # Numeric range search, __gte and __lte lookup\n        ("field_C", SliderNumericFilter),  # Numeric range filter but with slider\n        ("field_D", CustomSliderNumericFilter),  # Numeric filter with custom attributes\n        ("field_E", RangeDateFilter),  # Date filter\n        ("field_F", RangeDateTimeFilter),  # Datetime filter\n        CustomRangeNumericListFilter,  # Numeric range search not restricted to a model field\n    )\n\n    def get_queryset(self, request):\n        return super().get_queryset().annotate(items_count=Count("item", distinct=True))\n```\n\n## Third party packages\n\n### django-import-export\n\nTo get proper visual appearance for django-import-export, two things are needed\n\n1. Add `unfold.contrib.import_export` to `INSTALLED_APPS` at the begging of the file. This action will override all templates coming from the plugin.\n2. Change `import_form_class` and `export_form_class` in ModelAdmin which is inheriting from `ImportExportModelAdmin`. This chunk of code is responsible for adding proper styling to form elements.\n\n```python\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.import_export.forms import ExportForm, ImportForm\n\nclass ExampleAdmin(ModelAdmin, ImportExportModelAdmin):\n    import_form_class = ImportForm\n    export_form_class = ExportForm\n```\n\n## User Admin Form\n\nUser\'s admin in Django is specific as it contains several forms which are requiring custom styling. All of these forms has been inherited and accordingly adjusted. In user admin class it is needed to use these inherited form classes to enable custom styling matching rest of the website.\n\n```python\n# models.py\n\nfrom django.contrib.admin import register\nfrom django.contrib.auth.models import User\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.forms import AdminPasswordChangeForm, UserChangeForm, UserCreationForm\n\n\n@register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    form = UserChangeForm\n    add_form = UserCreationForm\n    change_password_form = AdminPasswordChangeForm\n```\n\n## Adding Custom Styles and Scripts\n\nTo add new custom styles, for example for custom dashboard, it is possible to load them via **STYLES** key in **UNFOLD** dict. This key accepts a list of strings or lambda functions which will be loaded on all pages. JavaScript files can be loaded by using similar apprach, but **SCRIPTS** is used.\n\n```python\n# settings.py\n\nfrom django.templatetags.static import static\n\nUNFOLD = {\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n}\n```\n\n## Project Level Tailwind Stylesheet\n\nWhen creating custom dashboard or adding custom components, it is needed to add own styles. Adding custom styles is described above. Most of the time, it is supposed that new elements are going to match with the rest of the administration panel. First of all, create tailwind.config.js in your application. Below is located minimal configuration for this file.\n\n```javascript\n// tailwind.config.js\n\nmodule.exports = {\n  content: ["./your_project/**/*.{html,py,js}"],\n  // In case custom colors are defined in UNFOLD["COLORS"]\n  colors: {\n    primary: {\n      100: "rgb(var(--color-primary-100) / <alpha-value>)",\n      200: "rgb(var(--color-primary-200) / <alpha-value>)",\n      300: "rgb(var(--color-primary-300) / <alpha-value>)",\n      400: "rgb(var(--color-primary-400) / <alpha-value>)",\n      500: "rgb(var(--color-primary-500) / <alpha-value>)",\n      600: "rgb(var(--color-primary-600) / <alpha-value>)",\n      700: "rgb(var(--color-primary-700) / <alpha-value>)",\n      800: "rgb(var(--color-primary-800) / <alpha-value>)",\n      900: "rgb(var(--color-primary-900) / <alpha-value>)",\n    },\n  },\n};\n```\n\nOnce the configuration file is set, it is possible to compile new styles which can be loaded into admin by using **STYLES** key in **UNFOLD** dict.\n\n```bash\nnpx tailwindcss  -o your_project/static/css/styles.css --watch --minify\n```\n\n## Custom Admin Dashboard\n\nThe most common thing which needs to be adjusted for each project in admin is the dashboard. By default Unfold does not provide any dashboard components. The default dashboard experience with list of all applications and models is kept with proper styling matching rest of the components but thats it. Anyway, Unfold was created that creation of custom dashboard will be streamlined.\n\nCreate `templates/admin/index.html` in your project and paste the base template below into it. By default, all your custom styles here are not compiled because CSS classes are located in your specific project. Here it is needed to set up the Tailwind for your project and all requried instructions are located in [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet) chapter.\n\n```\n{% extends \'unfold/layouts/base_simple.html\' %}\n\n{% load cache humanize i18n %}\n\n{% block breadcrumbs %}{% endblock %}\n\n{% block title %}{% if subtitle %}{{ subtitle }} | {% endif %}{{ title }} | {{ site_title|default:_(\'Django site admin\') }}{% endblock %}\n\n{% block branding %}\n    <h1 id="site-name"><a href="{% url \'admin:index\' %}">{{ site_header|default:_(\'Django administration\') }}</a></h1>\n{% endblock %}\n\n{% block content %}\n    Start creating your own Tailwind components here\n{% endblock %}\n```\n\nNote: In case that it is needed to pass custom variables into dashboard tamplate, check **DASHOARD_CALLBACK** in **UNFOLD** dict.\n\n## Unfold Development\n\n### Pre-commit\n\nBefore adding any source code, it is recommended to have pre-commit installed on your local computer to check for all potential issues when comitting the code.\n\n```bash\npip install pre-commit\npre-commit install\npre-commit install --hook-type commit-msg\n```\n\n### Poetry Configuration\n\nTo add a new feature or fix the easiest approach is to use django-unfold in combination with Poetry. The process looks like:\n\n- Install django-unfold via `poetry add django-unfold`\n- After that it is needed to git clone the repository somewhere on local computer.\n- Edit _pyproject.toml_ and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`\n- Lock and update via `poetry lock && poetry update`\n\n### Compiling Tailwind\n\nAt the moment project contains package.json with all dependencies required to compile new CSS file. Tailwind configuration file is set to check all html, js and py files for Tailwind\'s classeses occurrences.\n\n```bash\nnpm install\nnpx tailwindcss -i styles.css -o src/unfold/static/unfold/css/styles.css --watch --minify\n\nnpm run tailwind:watch # run after each change in code\nnpm run tailwind:build # run once\n```\n\nSome components like datepickers, calendars or selectors in admin was not possible to style by overriding html templates so their default styles are overriden in **styles.css**.\n\nNone: most of the custom styles localted in style.css are created via `@apply some-tailwind-class;`.\n',
     'author': 'None',
     'author_email': 'None',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://unfoldadmin.com',
     'package_dir': package_dir,
     'packages': packages,
```

### Comparing `django_unfold-0.6.0/PKG-INFO` & `django_unfold-0.6.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-unfold
-Version: 0.6.0
+Version: 0.6.1
 Summary: Clean & minimal Django admin theme based on Tailwind CSS
 Home-page: https://unfoldadmin.com
 License: MIT
 Keywords: django,admin,tailwind,theme
 Requires-Python: >=3.8
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
@@ -17,20 +17,20 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Dist: django (>=3.2)
-Project-URL: Repository, https://github.com/remastr/django-unfold
+Project-URL: Repository, https://github.com/unfoldadmin/django-unfold
 Description-Content-Type: text/markdown
 
-![Screenshot - Objects Listing](https://github.com/remastr/django-unfold/raw/main/screenshot-1.jpg)
+![Screenshot - Objects Listing](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-1.jpg)
 
-![Screenshot - Login Page](https://github.com/remastr/django-unfold/raw/main/screenshot-2.jpg)
+![Screenshot - Login Page](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-2.jpg)
 
 ## Unfold Django Admin Theme
 
 Unfold is a new theme for Django Admin incorporating some most common practises for building full-fledged admin areas.
 
 - **Visual**: provides new user interface based on Tailwind CSS framework
 - **Sidebar:** simplifies definition of custom sidebar navigation
@@ -138,14 +138,15 @@
 class UserAdmin(BaseUserAdmin, ModelAdmin):
     pass
 ```
 
 ## Configuration
 
 ### Available settings.py options
+
 ```python
 # settings.py
 
 from django.templatetags.static import static
 from django.urls import reverse_lazy
 from django.utils.translation import gettext_lazy as _
 
@@ -340,24 +341,25 @@
 
 ### Actions overview
 
 Besides traditional actions selected from dropdown, Unfold supports several other types of actions. Following table
 gives overview of all available actions together with their recommended usage:
 
 | Type of action | Appearance                               | Usage                                                                                      | Examples of usage                      |
-|----------------|------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------|
+| -------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------- |
 | Default        | List view - top of listing (in dropdown) | Actions, where you want to select specific subset of instances to perform this action upon | Bulk deleting, bulk activation         |
 | Global         | List view - top of listing (as buttons)  | General actions for model, without selecting specific instances                            | Import, export                         |
 | Row            | List view - in each row                  | Action for one specific instance, executable from listing                                  | Activation, sync with external service |
 | Detail         | Detail view - top of detail              | Action for one specific instance, executable from detail                                   | Activation, sync with external service |
 | Submit line    | Detail view - near submit button         | Action performed during form submit (instance save)                                        | Publishing article together with save  |
 
 ### Custom unfold @action decorator
 
 Unfold also uses custom `@action` decorator, supporting 2 more parameters in comparison to base `@action` decorator:
+
 - `url_path`: Action path name, used to override the path under which the action will be available
   (if not provided, URL path will be generated by Unfold)
 - `attrs`: Dictionary of the additional attributes added to the `<a>` element, used for e.g. opening action in new tab (`{"target": "_blank"}`)
 
 ### Action handler functions
 
 This section provides explanation of how the action handler functions should be constructed for Unfold actions.
@@ -509,18 +511,16 @@
         CustomRangeNumericListFilter,  # Numeric range search not restricted to a model field
     )
 
     def get_queryset(self, request):
         return super().get_queryset().annotate(items_count=Count("item", distinct=True))
 ```
 
-
 ## Third party packages
 
-
 ### django-import-export
 
 To get proper visual appearance for django-import-export, two things are needed
 
 1. Add `unfold.contrib.import_export` to `INSTALLED_APPS` at the begging of the file. This action will override all templates coming from the plugin.
 2. Change `import_form_class` and `export_form_class` in ModelAdmin which is inheriting from `ImportExportModelAdmin`. This chunk of code is responsible for adding proper styling to form elements.
 
@@ -578,32 +578,30 @@
 
 When creating custom dashboard or adding custom components, it is needed to add own styles. Adding custom styles is described above. Most of the time, it is supposed that new elements are going to match with the rest of the administration panel. First of all, create tailwind.config.js in your application. Below is located minimal configuration for this file.
 
 ```javascript
 // tailwind.config.js
 
 module.exports = {
-    content: [
-        "./your_project/**/*.{html,py,js}"
-    ],
-    // In case custom colors are defined in UNFOLD["COLORS"]
-    colors: {
-        primary: {
-          100: "rgb(var(--color-primary-100) / <alpha-value>)",
-          200: "rgb(var(--color-primary-200) / <alpha-value>)",
-          300: "rgb(var(--color-primary-300) / <alpha-value>)",
-          400: "rgb(var(--color-primary-400) / <alpha-value>)",
-          500: "rgb(var(--color-primary-500) / <alpha-value>)",
-          600: "rgb(var(--color-primary-600) / <alpha-value>)",
-          700: "rgb(var(--color-primary-700) / <alpha-value>)",
-          800: "rgb(var(--color-primary-800) / <alpha-value>)",
-          900: "rgb(var(--color-primary-900) / <alpha-value>)"
-        }
-    }
-}
+  content: ["./your_project/**/*.{html,py,js}"],
+  // In case custom colors are defined in UNFOLD["COLORS"]
+  colors: {
+    primary: {
+      100: "rgb(var(--color-primary-100) / <alpha-value>)",
+      200: "rgb(var(--color-primary-200) / <alpha-value>)",
+      300: "rgb(var(--color-primary-300) / <alpha-value>)",
+      400: "rgb(var(--color-primary-400) / <alpha-value>)",
+      500: "rgb(var(--color-primary-500) / <alpha-value>)",
+      600: "rgb(var(--color-primary-600) / <alpha-value>)",
+      700: "rgb(var(--color-primary-700) / <alpha-value>)",
+      800: "rgb(var(--color-primary-800) / <alpha-value>)",
+      900: "rgb(var(--color-primary-900) / <alpha-value>)",
+    },
+  },
+};
 ```
 
 Once the configuration file is set, it is possible to compile new styles which can be loaded into admin by using **STYLES** key in **UNFOLD** dict.
 
 ```bash
 npx tailwindcss  -o your_project/static/css/styles.css --watch --minify
 ```
@@ -648,15 +646,15 @@
 
 ### Poetry Configuration
 
 To add a new feature or fix the easiest approach is to use django-unfold in combination with Poetry. The process looks like:
 
 - Install django-unfold via `poetry add django-unfold`
 - After that it is needed to git clone the repository somewhere on local computer.
-- Edit *pyproject.toml* and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`
+- Edit _pyproject.toml_ and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`
 - Lock and update via `poetry lock && poetry update`
 
 ### Compiling Tailwind
 
 At the moment project contains package.json with all dependencies required to compile new CSS file. Tailwind configuration file is set to check all html, js and py files for Tailwind's classeses occurrences.
 
 ```bash
```

