# Comparing `tmp/django_unfold-0.6.1.tar.gz` & `tmp/django_unfold-0.6.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_unfold-0.6.1.tar", max compression
+gzip compressed data, was "django_unfold-0.6.2.tar", max compression
```

## Comparing `django_unfold-0.6.1.tar` & `django_unfold-0.6.2.tar`

### file list

```diff
@@ -1,133 +1,133 @@
--rw-r--r--   0        0        0     1069 2023-05-13 10:12:56.719117 django_unfold-0.6.1/LICENSE
--rw-r--r--   0        0        0    25292 2023-05-13 10:13:27.829399 django_unfold-0.6.1/README.md
--rw-r--r--   0        0        0     1277 2023-05-13 10:13:47.172513 django_unfold-0.6.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.598781 django_unfold-0.6.1/src/unfold/__init__.py
--rw-r--r--   0        0        0    22083 2023-05-12 18:20:54.599253 django_unfold-0.6.1/src/unfold/admin.py
--rw-r--r--   0        0        0      307 2023-05-12 18:20:54.599876 django_unfold-0.6.1/src/unfold/apps.py
--rw-r--r--   0        0        0     1835 2023-05-12 18:20:54.600089 django_unfold-0.6.1/src/unfold/checks.py
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.600203 django_unfold-0.6.1/src/unfold/contrib/__init__.py
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.600335 django_unfold-0.6.1/src/unfold/contrib/filters/__init__.py
--rw-r--r--   0        0        0    16034 2023-05-12 18:20:54.600718 django_unfold-0.6.1/src/unfold/contrib/filters/admin.py
--rw-r--r--   0        0        0      107 2023-05-12 18:20:54.600880 django_unfold-0.6.1/src/unfold/contrib/filters/apps.py
--rw-r--r--   0        0        0     4055 2023-05-12 18:20:54.601060 django_unfold-0.6.1/src/unfold/contrib/filters/forms.py
--rw-r--r--   0        0        0     4221 2023-05-12 18:20:54.601236 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css
--rw-r--r--   0        0        0    19332 2023-05-12 18:20:54.601420 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js
--rw-r--r--   0        0        0     1668 2023-05-12 18:20:54.601576 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js
--rw-r--r--   0        0        0    26683 2023-05-12 18:20:54.601864 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js
--rw-r--r--   0        0        0     2236 2023-05-12 18:20:54.602017 django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js
--rw-r--r--   0        0        0      470 2023-05-12 18:20:54.602162 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_date_range.html
--rw-r--r--   0        0        0      470 2023-05-12 18:20:54.602300 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_datetime_range.html
--rw-r--r--   0        0        0      338 2023-05-12 18:20:54.602434 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_range.html
--rw-r--r--   0        0        0      273 2023-05-12 18:20:54.602579 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_single.html
--rw-r--r--   0        0        0     1648 2023-05-12 18:20:54.602723 django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.602815 django_unfold-0.6.1/src/unfold/contrib/forms/__init__.py
--rw-r--r--   0        0        0      105 2023-05-12 18:20:54.602973 django_unfold-0.6.1/src/unfold/contrib/forms/apps.py
--rw-r--r--   0        0        0    20007 2023-05-12 18:20:54.603172 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/css/trix.css
--rw-r--r--   0        0        0      858 2023-05-12 18:20:54.603349 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js
--rw-r--r--   0        0        0   172634 2023-05-12 18:20:54.603957 django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.js
--rw-r--r--   0        0        0     9558 2023-05-12 18:20:54.604145 django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html
--rw-r--r--   0        0        0      351 2023-05-12 18:20:54.604341 django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/wysiwyg.html
--rw-r--r--   0        0        0      962 2023-05-12 18:20:54.604771 django_unfold-0.6.1/src/unfold/contrib/forms/widgets.py
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.604888 django_unfold-0.6.1/src/unfold/contrib/import_export/__init__.py
--rw-r--r--   0        0        0      142 2023-05-12 18:20:54.605086 django_unfold-0.6.1/src/unfold/contrib/import_export/apps.py
--rw-r--r--   0        0        0      672 2023-05-12 18:20:54.605258 django_unfold-0.6.1/src/unfold/contrib/import_export/forms.py
--rw-r--r--   0        0        0      357 2023-05-12 18:20:54.605425 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/base.html
--rw-r--r--   0        0        0      412 2023-05-12 18:20:54.605579 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_export_item.html
--rw-r--r--   0        0        0      229 2023-05-12 18:20:54.605725 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_export.html
--rw-r--r--   0        0        0      387 2023-05-12 18:20:54.605864 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_item.html
--rw-r--r--   0        0        0     1791 2023-05-12 18:20:54.606013 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/export.html
--rw-r--r--   0        0        0     2075 2023-05-12 18:20:54.606159 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import.html
--rw-r--r--   0        0        0      867 2023-05-12 18:20:54.606318 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html
--rw-r--r--   0        0        0     1422 2023-05-12 18:20:54.606457 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html
--rw-r--r--   0        0        0     1312 2023-05-12 18:20:54.606598 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html
--rw-r--r--   0        0        0     2413 2023-05-12 18:20:54.606738 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html
--rw-r--r--   0        0        0     4880 2023-05-12 18:20:54.606939 django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html
--rw-r--r--   0        0        0      199 2023-05-12 18:20:54.607385 django_unfold-0.6.1/src/unfold/dataclasses.py
--rw-r--r--   0        0        0     3277 2023-05-12 18:20:54.607661 django_unfold-0.6.1/src/unfold/decorators.py
--rw-r--r--   0        0        0       43 2023-05-12 18:20:54.607837 django_unfold-0.6.1/src/unfold/exceptions.py
--rw-r--r--   0        0        0     3281 2023-05-12 18:20:54.608016 django_unfold-0.6.1/src/unfold/forms.py
--rw-r--r--   0        0        0     1116 2023-05-12 18:20:54.608156 django_unfold-0.6.1/src/unfold/settings.py
--rw-r--r--   0        0        0     9000 2023-05-12 18:20:54.608315 django_unfold-0.6.1/src/unfold/sites.py
--rw-r--r--   0        0        0     3890 2023-05-12 18:20:54.608495 django_unfold-0.6.1/src/unfold/static/unfold/css/simplebar.css
--rw-r--r--   0        0        0    71987 2023-05-12 18:20:54.608770 django_unfold-0.6.1/src/unfold/static/unfold/css/styles.css
--rw-r--r--   0        0        0    41071 2023-05-12 18:20:54.609088 django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.js
--rw-r--r--   0        0        0      626 2023-05-12 18:20:54.609260 django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.persist.js
--rw-r--r--   0        0        0     1628 2023-05-12 18:20:54.609421 django_unfold-0.6.1/src/unfold/static/unfold/js/app.js
--rw-r--r--   0        0        0    42820 2023-05-12 18:20:54.609691 django_unfold-0.6.1/src/unfold/static/unfold/js/htmx.js
--rw-r--r--   0        0        0    65855 2023-05-12 18:20:54.610054 django_unfold-0.6.1/src/unfold/static/unfold/js/simplebar.js
--rw-r--r--   0        0        0     2519 2023-05-12 18:20:54.610231 django_unfold-0.6.1/src/unfold/templates/admin/actions.html
--rw-r--r--   0        0        0      802 2023-05-12 18:20:54.610384 django_unfold-0.6.1/src/unfold/templates/admin/app_index.html
--rw-r--r--   0        0        0     3594 2023-05-12 18:20:54.610605 django_unfold-0.6.1/src/unfold/templates/admin/app_list.html
--rw-r--r--   0        0        0      478 2023-05-12 18:20:54.610762 django_unfold-0.6.1/src/unfold/templates/admin/auth/user/add_form.html
--rw-r--r--   0        0        0     2892 2023-05-12 18:20:54.610908 django_unfold-0.6.1/src/unfold/templates/admin/auth/user/change_password.html
--rw-r--r--   0        0        0     3503 2023-05-12 18:20:54.611288 django_unfold-0.6.1/src/unfold/templates/admin/base.html
--rw-r--r--   0        0        0      361 2023-05-12 18:20:54.611499 django_unfold-0.6.1/src/unfold/templates/admin/base_site.html
--rw-r--r--   0        0        0     5001 2023-05-12 18:20:54.611702 django_unfold-0.6.1/src/unfold/templates/admin/change_form.html
--rw-r--r--   0        0        0      686 2023-05-12 18:20:54.611928 django_unfold-0.6.1/src/unfold/templates/admin/change_form_object_tools.html
--rw-r--r--   0        0        0     8376 2023-05-12 18:20:54.612096 django_unfold-0.6.1/src/unfold/templates/admin/change_list.html
--rw-r--r--   0        0        0      699 2023-05-12 18:20:54.612241 django_unfold-0.6.1/src/unfold/templates/admin/change_list_object_tools.html
--rw-r--r--   0        0        0     4206 2023-05-12 18:20:54.612387 django_unfold-0.6.1/src/unfold/templates/admin/change_list_results.html
--rw-r--r--   0        0        0     1306 2023-05-12 18:20:54.612538 django_unfold-0.6.1/src/unfold/templates/admin/date_hierarchy.html
--rw-r--r--   0        0        0     5166 2023-05-12 18:20:54.612692 django_unfold-0.6.1/src/unfold/templates/admin/delete_confirmation.html
--rw-r--r--   0        0        0     4941 2023-05-12 18:20:54.612842 django_unfold-0.6.1/src/unfold/templates/admin/delete_selected_confirmation.html
--rw-r--r--   0        0        0     4372 2023-05-12 18:20:54.612989 django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/stacked.html
--rw-r--r--   0        0        0    12199 2023-05-12 18:20:54.613137 django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/tabular.html
--rw-r--r--   0        0        0     1479 2023-05-12 18:20:54.613269 django_unfold-0.6.1/src/unfold/templates/admin/filter.html
--rw-r--r--   0        0        0     3047 2023-05-12 18:20:54.613405 django_unfold-0.6.1/src/unfold/templates/admin/includes/fieldset.html
--rw-r--r--   0        0        0      468 2023-05-12 18:20:54.613548 django_unfold-0.6.1/src/unfold/templates/admin/includes/object_delete_summary.html
--rw-r--r--   0        0        0      674 2023-05-12 18:20:54.613684 django_unfold-0.6.1/src/unfold/templates/admin/index.html
--rw-r--r--   0        0        0     3494 2023-05-12 18:20:54.613824 django_unfold-0.6.1/src/unfold/templates/admin/login.html
--rw-r--r--   0        0        0     1178 2023-05-12 18:20:54.613956 django_unfold-0.6.1/src/unfold/templates/admin/nav_sidebar.html
--rw-r--r--   0        0        0     3951 2023-05-12 18:20:54.614095 django_unfold-0.6.1/src/unfold/templates/admin/object_history.html
--rw-r--r--   0        0        0     1173 2023-05-12 18:20:54.614240 django_unfold-0.6.1/src/unfold/templates/admin/pagination.html
--rw-r--r--   0        0        0     1143 2023-05-12 18:20:54.614378 django_unfold-0.6.1/src/unfold/templates/admin/search_form.html
--rw-r--r--   0        0        0     4306 2023-05-12 18:20:54.614530 django_unfold-0.6.1/src/unfold/templates/admin/submit_line.html
--rw-r--r--   0        0        0     1751 2023-05-12 18:20:54.614674 django_unfold-0.6.1/src/unfold/templates/admin/widgets/clearable_file_input.html
--rw-r--r--   0        0        0     3888 2023-05-12 18:20:54.614822 django_unfold-0.6.1/src/unfold/templates/admin/widgets/related_widget_wrapper.html
--rw-r--r--   0        0        0      848 2023-05-12 18:20:54.615101 django_unfold-0.6.1/src/unfold/templates/admin/widgets/split_datetime.html
--rw-r--r--   0        0        0      785 2023-05-12 18:20:54.615265 django_unfold-0.6.1/src/unfold/templates/auth/widgets/read_only_password_hash.html
--rw-r--r--   0        0        0     1028 2023-05-12 18:20:54.615426 django_unfold-0.6.1/src/unfold/templates/registration/logged_out.html
--rw-r--r--   0        0        0     1062 2023-05-12 18:20:54.615582 django_unfold-0.6.1/src/unfold/templates/registration/password_change_done.html
--rw-r--r--   0        0        0     2225 2023-05-12 18:20:54.615724 django_unfold-0.6.1/src/unfold/templates/registration/password_change_form.html
--rw-r--r--   0        0        0     1461 2023-05-12 18:20:54.615872 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/actions_row.html
--rw-r--r--   0        0        0     3908 2023-05-12 18:20:54.616067 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list.html
--rw-r--r--   0        0        0     3302 2023-05-12 18:20:54.616262 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list_default.html
--rw-r--r--   0        0        0      466 2023-05-12 18:20:54.616448 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/boolean.html
--rw-r--r--   0        0        0      234 2023-05-12 18:20:54.616621 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/breadcrumb_item.html
--rw-r--r--   0        0        0      248 2023-05-12 18:20:54.616796 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_header.html
--rw-r--r--   0        0        0     2072 2023-05-12 18:20:54.616979 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_label.html
--rw-r--r--   0        0        0      335 2023-05-12 18:20:54.617143 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/field.html
--rw-r--r--   0        0        0      266 2023-05-12 18:20:54.617297 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/form_errors.html
--rw-r--r--   0        0        0      151 2023-05-12 18:20:54.617435 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/help_text.html
--rw-r--r--   0        0        0     1995 2023-05-12 18:20:54.617571 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/history.html
--rw-r--r--   0        0        0      237 2023-05-12 18:20:54.617700 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/label.html
--rw-r--r--   0        0        0      557 2023-05-12 18:20:54.617864 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/error.html
--rw-r--r--   0        0        0      404 2023-05-12 18:20:54.618038 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/errornote.html
--rw-r--r--   0        0        0      143 2023-05-12 18:20:54.618223 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/info.html
--rw-r--r--   0        0        0      595 2023-05-12 18:20:54.618403 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages.html
--rw-r--r--   0        0        0     1101 2023-05-12 18:20:54.618729 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/navigation.html
--rw-r--r--   0        0        0       69 2023-05-12 18:20:54.618910 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/pagination_current_item.html
--rw-r--r--   0        0        0       56 2023-05-12 18:20:54.619087 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/pagination_ellipsis.html
--rw-r--r--   0        0        0     1314 2023-05-12 18:20:54.619231 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search.html
--rw-r--r--   0        0        0      725 2023-05-12 18:20:54.619389 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search_results.html
--rw-r--r--   0        0        0      442 2023-05-12 18:20:54.619541 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/site_icon.html
--rw-r--r--   0        0        0     2038 2023-05-12 18:20:54.619703 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/tab_list.html
--rw-r--r--   0        0        0     4895 2023-05-12 18:20:54.619870 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/userlinks.html
--rw-r--r--   0        0        0     1120 2023-05-12 18:20:54.620020 django_unfold-0.6.1/src/unfold/templates/unfold/helpers/welcomemsg.html
--rw-r--r--   0        0        0      859 2023-05-12 18:20:54.620180 django_unfold-0.6.1/src/unfold/templates/unfold/layouts/base_simple.html
--rw-r--r--   0        0        0     3149 2023-05-12 18:20:54.620363 django_unfold-0.6.1/src/unfold/templates/unfold/layouts/skeleton.html
--rw-r--r--   0        0        0     2218 2023-05-12 18:20:54.620539 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/clearable_file_input_small.html
--rw-r--r--   0        0        0       88 2023-05-12 18:20:54.620735 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/date.html
--rw-r--r--   0        0        0      262 2023-05-12 18:20:54.620945 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/range.html
--rw-r--r--   0        0        0      881 2023-05-12 18:20:54.621116 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/split_datetime_vertical.html
--rw-r--r--   0        0        0      459 2023-05-12 18:20:54.621287 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/textarea.html
--rw-r--r--   0        0        0       88 2023-05-12 18:20:54.621454 django_unfold-0.6.1/src/unfold/templates/unfold/widgets/time.html
--rw-r--r--   0        0        0        0 2023-05-12 18:20:54.621577 django_unfold-0.6.1/src/unfold/templatetags/__init__.py
--rw-r--r--   0        0        0     3559 2023-05-12 18:20:54.621781 django_unfold-0.6.1/src/unfold/templatetags/unfold.py
--rw-r--r--   0        0        0    10012 2023-05-12 18:20:54.621974 django_unfold-0.6.1/src/unfold/templatetags/unfold_list.py
--rw-r--r--   0        0        0      576 2023-05-12 18:20:54.622129 django_unfold-0.6.1/src/unfold/typing.py
--rw-r--r--   0        0        0     3878 2023-05-12 18:20:54.622285 django_unfold-0.6.1/src/unfold/utils.py
--rw-r--r--   0        0        0      708 2023-05-12 18:20:54.622428 django_unfold-0.6.1/src/unfold/views.py
--rw-r--r--   0        0        0     8150 2023-05-12 18:20:54.622598 django_unfold-0.6.1/src/unfold/widgets.py
--rw-r--r--   0        0        0    27771 1970-01-01 00:00:00.000000 django_unfold-0.6.1/setup.py
--rw-r--r--   0        0        0    26327 1970-01-01 00:00:00.000000 django_unfold-0.6.1/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-13 10:12:56.719117 django_unfold-0.6.2/LICENSE
+-rw-r--r--   0        0        0    25292 2023-05-13 10:13:27.829399 django_unfold-0.6.2/README.md
+-rw-r--r--   0        0        0     1277 2023-05-13 16:56:13.925305 django_unfold-0.6.2/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.727345 django_unfold-0.6.2/src/unfold/__init__.py
+-rw-r--r--   0        0        0    22083 2023-05-13 16:52:54.544597 django_unfold-0.6.2/src/unfold/admin.py
+-rw-r--r--   0        0        0      307 2023-05-13 10:21:01.728211 django_unfold-0.6.2/src/unfold/apps.py
+-rw-r--r--   0        0        0     1835 2023-05-13 10:21:01.728376 django_unfold-0.6.2/src/unfold/checks.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.728475 django_unfold-0.6.2/src/unfold/contrib/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.728585 django_unfold-0.6.2/src/unfold/contrib/filters/__init__.py
+-rw-r--r--   0        0        0    16034 2023-05-13 10:21:01.728762 django_unfold-0.6.2/src/unfold/contrib/filters/admin.py
+-rw-r--r--   0        0        0      107 2023-05-13 10:21:01.728902 django_unfold-0.6.2/src/unfold/contrib/filters/apps.py
+-rw-r--r--   0        0        0     4055 2023-05-13 10:21:01.729050 django_unfold-0.6.2/src/unfold/contrib/filters/forms.py
+-rw-r--r--   0        0        0     4221 2023-05-13 10:21:01.729226 django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css
+-rw-r--r--   0        0        0    19332 2023-05-13 10:21:01.729407 django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js
+-rw-r--r--   0        0        0     1668 2023-05-13 10:21:01.729575 django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js
+-rw-r--r--   0        0        0    26683 2023-05-13 10:21:01.729796 django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js
+-rw-r--r--   0        0        0     2236 2023-05-13 10:21:01.729940 django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js
+-rw-r--r--   0        0        0      470 2023-05-13 10:21:01.730196 django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_date_range.html
+-rw-r--r--   0        0        0      470 2023-05-13 10:21:01.730358 django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_datetime_range.html
+-rw-r--r--   0        0        0      338 2023-05-13 10:21:01.730500 django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_range.html
+-rw-r--r--   0        0        0      273 2023-05-13 10:21:01.730647 django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_single.html
+-rw-r--r--   0        0        0     1648 2023-05-13 10:21:01.730791 django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.730880 django_unfold-0.6.2/src/unfold/contrib/forms/__init__.py
+-rw-r--r--   0        0        0      105 2023-05-13 10:21:01.731028 django_unfold-0.6.2/src/unfold/contrib/forms/apps.py
+-rw-r--r--   0        0        0    20007 2023-05-13 10:21:01.731207 django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/css/trix.css
+-rw-r--r--   0        0        0      858 2023-05-13 10:21:01.731352 django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js
+-rw-r--r--   0        0        0   172634 2023-05-13 10:21:01.731965 django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/js/trix.js
+-rw-r--r--   0        0        0     9558 2023-05-13 10:21:01.732147 django_unfold-0.6.2/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html
+-rw-r--r--   0        0        0      351 2023-05-13 10:21:01.732295 django_unfold-0.6.2/src/unfold/contrib/forms/templates/unfold/forms/wysiwyg.html
+-rw-r--r--   0        0        0      962 2023-05-13 10:21:01.732430 django_unfold-0.6.2/src/unfold/contrib/forms/widgets.py
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.732518 django_unfold-0.6.2/src/unfold/contrib/import_export/__init__.py
+-rw-r--r--   0        0        0      142 2023-05-13 10:21:01.732682 django_unfold-0.6.2/src/unfold/contrib/import_export/apps.py
+-rw-r--r--   0        0        0      672 2023-05-13 10:21:01.732855 django_unfold-0.6.2/src/unfold/contrib/import_export/forms.py
+-rw-r--r--   0        0        0      357 2023-05-13 10:21:01.733021 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/base.html
+-rw-r--r--   0        0        0      412 2023-05-13 10:21:01.733224 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/change_list_export_item.html
+-rw-r--r--   0        0        0      229 2023-05-13 10:21:01.733388 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_export.html
+-rw-r--r--   0        0        0      387 2023-05-13 10:21:01.733550 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/change_list_import_item.html
+-rw-r--r--   0        0        0     1791 2023-05-13 10:21:01.733708 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/export.html
+-rw-r--r--   0        0        0     2075 2023-05-13 10:21:01.733862 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import.html
+-rw-r--r--   0        0        0      867 2023-05-13 10:21:01.734027 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html
+-rw-r--r--   0        0        0     1422 2023-05-13 10:21:01.734315 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html
+-rw-r--r--   0        0        0     1312 2023-05-13 10:21:01.734488 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html
+-rw-r--r--   0        0        0     2413 2023-05-13 10:21:01.734667 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html
+-rw-r--r--   0        0        0     4880 2023-05-13 10:21:01.734852 django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html
+-rw-r--r--   0        0        0      199 2023-05-13 10:21:01.735015 django_unfold-0.6.2/src/unfold/dataclasses.py
+-rw-r--r--   0        0        0     3272 2023-05-13 16:17:57.016841 django_unfold-0.6.2/src/unfold/decorators.py
+-rw-r--r--   0        0        0       43 2023-05-13 10:21:01.735307 django_unfold-0.6.2/src/unfold/exceptions.py
+-rw-r--r--   0        0        0     3281 2023-05-13 10:21:01.735454 django_unfold-0.6.2/src/unfold/forms.py
+-rw-r--r--   0        0        0     1116 2023-05-13 10:21:01.735597 django_unfold-0.6.2/src/unfold/settings.py
+-rw-r--r--   0        0        0     9000 2023-05-13 10:21:01.735755 django_unfold-0.6.2/src/unfold/sites.py
+-rw-r--r--   0        0        0     3890 2023-05-13 10:21:01.735925 django_unfold-0.6.2/src/unfold/static/unfold/css/simplebar.css
+-rw-r--r--   0        0        0    71987 2023-05-13 10:21:01.736233 django_unfold-0.6.2/src/unfold/static/unfold/css/styles.css
+-rw-r--r--   0        0        0    41071 2023-05-13 10:21:01.736551 django_unfold-0.6.2/src/unfold/static/unfold/js/alpine.js
+-rw-r--r--   0        0        0      626 2023-05-13 10:21:01.736712 django_unfold-0.6.2/src/unfold/static/unfold/js/alpine.persist.js
+-rw-r--r--   0        0        0     1628 2023-05-13 10:21:01.736875 django_unfold-0.6.2/src/unfold/static/unfold/js/app.js
+-rw-r--r--   0        0        0    42820 2023-05-13 10:21:01.737160 django_unfold-0.6.2/src/unfold/static/unfold/js/htmx.js
+-rw-r--r--   0        0        0    65855 2023-05-13 10:21:01.737510 django_unfold-0.6.2/src/unfold/static/unfold/js/simplebar.js
+-rw-r--r--   0        0        0     2519 2023-05-13 10:21:01.737669 django_unfold-0.6.2/src/unfold/templates/admin/actions.html
+-rw-r--r--   0        0        0      802 2023-05-13 10:21:01.737808 django_unfold-0.6.2/src/unfold/templates/admin/app_index.html
+-rw-r--r--   0        0        0     3594 2023-05-13 10:21:01.737961 django_unfold-0.6.2/src/unfold/templates/admin/app_list.html
+-rw-r--r--   0        0        0      478 2023-05-13 10:21:01.738123 django_unfold-0.6.2/src/unfold/templates/admin/auth/user/add_form.html
+-rw-r--r--   0        0        0     2892 2023-05-13 10:21:01.738288 django_unfold-0.6.2/src/unfold/templates/admin/auth/user/change_password.html
+-rw-r--r--   0        0        0     3503 2023-05-13 10:21:01.738451 django_unfold-0.6.2/src/unfold/templates/admin/base.html
+-rw-r--r--   0        0        0      361 2023-05-13 10:21:01.738610 django_unfold-0.6.2/src/unfold/templates/admin/base_site.html
+-rw-r--r--   0        0        0     5001 2023-05-13 10:21:01.738755 django_unfold-0.6.2/src/unfold/templates/admin/change_form.html
+-rw-r--r--   0        0        0      686 2023-05-13 10:21:01.738895 django_unfold-0.6.2/src/unfold/templates/admin/change_form_object_tools.html
+-rw-r--r--   0        0        0     8376 2023-05-13 10:21:01.739065 django_unfold-0.6.2/src/unfold/templates/admin/change_list.html
+-rw-r--r--   0        0        0      699 2023-05-13 10:21:01.739226 django_unfold-0.6.2/src/unfold/templates/admin/change_list_object_tools.html
+-rw-r--r--   0        0        0     4206 2023-05-13 10:21:01.739365 django_unfold-0.6.2/src/unfold/templates/admin/change_list_results.html
+-rw-r--r--   0        0        0     1306 2023-05-13 10:21:01.739510 django_unfold-0.6.2/src/unfold/templates/admin/date_hierarchy.html
+-rw-r--r--   0        0        0     5166 2023-05-13 10:21:01.739658 django_unfold-0.6.2/src/unfold/templates/admin/delete_confirmation.html
+-rw-r--r--   0        0        0     4941 2023-05-13 10:21:01.739813 django_unfold-0.6.2/src/unfold/templates/admin/delete_selected_confirmation.html
+-rw-r--r--   0        0        0     4372 2023-05-13 10:21:01.739959 django_unfold-0.6.2/src/unfold/templates/admin/edit_inline/stacked.html
+-rw-r--r--   0        0        0    12199 2023-05-13 10:21:01.740109 django_unfold-0.6.2/src/unfold/templates/admin/edit_inline/tabular.html
+-rw-r--r--   0        0        0     1479 2023-05-13 10:21:01.740242 django_unfold-0.6.2/src/unfold/templates/admin/filter.html
+-rw-r--r--   0        0        0     3047 2023-05-13 10:21:01.740388 django_unfold-0.6.2/src/unfold/templates/admin/includes/fieldset.html
+-rw-r--r--   0        0        0      468 2023-05-13 10:21:01.740522 django_unfold-0.6.2/src/unfold/templates/admin/includes/object_delete_summary.html
+-rw-r--r--   0        0        0      674 2023-05-13 10:21:01.740655 django_unfold-0.6.2/src/unfold/templates/admin/index.html
+-rw-r--r--   0        0        0     3494 2023-05-13 10:21:01.740800 django_unfold-0.6.2/src/unfold/templates/admin/login.html
+-rw-r--r--   0        0        0     1178 2023-05-13 10:21:01.740932 django_unfold-0.6.2/src/unfold/templates/admin/nav_sidebar.html
+-rw-r--r--   0        0        0     3951 2023-05-13 10:21:01.741071 django_unfold-0.6.2/src/unfold/templates/admin/object_history.html
+-rw-r--r--   0        0        0     1173 2023-05-13 10:21:01.741206 django_unfold-0.6.2/src/unfold/templates/admin/pagination.html
+-rw-r--r--   0        0        0     1143 2023-05-13 10:21:01.741347 django_unfold-0.6.2/src/unfold/templates/admin/search_form.html
+-rw-r--r--   0        0        0     4306 2023-05-13 10:21:01.741494 django_unfold-0.6.2/src/unfold/templates/admin/submit_line.html
+-rw-r--r--   0        0        0     1751 2023-05-13 10:21:01.741647 django_unfold-0.6.2/src/unfold/templates/admin/widgets/clearable_file_input.html
+-rw-r--r--   0        0        0     3888 2023-05-13 10:21:01.741809 django_unfold-0.6.2/src/unfold/templates/admin/widgets/related_widget_wrapper.html
+-rw-r--r--   0        0        0      848 2023-05-13 10:21:01.741973 django_unfold-0.6.2/src/unfold/templates/admin/widgets/split_datetime.html
+-rw-r--r--   0        0        0      785 2023-05-13 10:21:01.742129 django_unfold-0.6.2/src/unfold/templates/auth/widgets/read_only_password_hash.html
+-rw-r--r--   0        0        0     1028 2023-05-13 10:21:01.742442 django_unfold-0.6.2/src/unfold/templates/registration/logged_out.html
+-rw-r--r--   0        0        0     1062 2023-05-13 10:21:01.742605 django_unfold-0.6.2/src/unfold/templates/registration/password_change_done.html
+-rw-r--r--   0        0        0     2225 2023-05-13 10:21:01.742767 django_unfold-0.6.2/src/unfold/templates/registration/password_change_form.html
+-rw-r--r--   0        0        0     1461 2023-05-13 10:21:01.742924 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/actions_row.html
+-rw-r--r--   0        0        0     3908 2023-05-13 10:21:01.743087 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/app_list.html
+-rw-r--r--   0        0        0     3302 2023-05-13 10:21:01.743236 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/app_list_default.html
+-rw-r--r--   0        0        0      466 2023-05-13 10:21:01.743380 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/boolean.html
+-rw-r--r--   0        0        0      234 2023-05-13 10:21:01.743536 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/breadcrumb_item.html
+-rw-r--r--   0        0        0      248 2023-05-13 10:21:01.743673 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/display_header.html
+-rw-r--r--   0        0        0     2072 2023-05-13 10:21:01.743934 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/display_label.html
+-rw-r--r--   0        0        0      335 2023-05-13 10:21:01.744073 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/field.html
+-rw-r--r--   0        0        0      266 2023-05-13 10:21:01.744211 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/form_errors.html
+-rw-r--r--   0        0        0      151 2023-05-13 10:21:01.744340 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/help_text.html
+-rw-r--r--   0        0        0     1995 2023-05-13 10:21:01.744474 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/history.html
+-rw-r--r--   0        0        0      237 2023-05-13 10:21:01.744606 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/label.html
+-rw-r--r--   0        0        0      557 2023-05-13 10:21:01.744746 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages/error.html
+-rw-r--r--   0        0        0      404 2023-05-13 10:21:01.744880 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages/errornote.html
+-rw-r--r--   0        0        0      143 2023-05-13 10:21:01.745021 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages/info.html
+-rw-r--r--   0        0        0      595 2023-05-13 10:21:01.745153 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages.html
+-rw-r--r--   0        0        0     1101 2023-05-13 10:21:01.745288 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/navigation.html
+-rw-r--r--   0        0        0       69 2023-05-13 10:21:01.745416 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/pagination_current_item.html
+-rw-r--r--   0        0        0       56 2023-05-13 10:21:01.745547 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/pagination_ellipsis.html
+-rw-r--r--   0        0        0     1314 2023-05-13 10:21:01.745680 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/search.html
+-rw-r--r--   0        0        0      725 2023-05-13 10:21:01.745816 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/search_results.html
+-rw-r--r--   0        0        0      442 2023-05-13 10:21:01.745946 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/site_icon.html
+-rw-r--r--   0        0        0     2038 2023-05-13 10:21:01.746080 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/tab_list.html
+-rw-r--r--   0        0        0     4895 2023-05-13 10:21:01.746219 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/userlinks.html
+-rw-r--r--   0        0        0     1120 2023-05-13 10:21:01.746366 django_unfold-0.6.2/src/unfold/templates/unfold/helpers/welcomemsg.html
+-rw-r--r--   0        0        0      859 2023-05-13 10:21:01.746507 django_unfold-0.6.2/src/unfold/templates/unfold/layouts/base_simple.html
+-rw-r--r--   0        0        0     3149 2023-05-13 10:21:01.746646 django_unfold-0.6.2/src/unfold/templates/unfold/layouts/skeleton.html
+-rw-r--r--   0        0        0     2218 2023-05-13 10:21:01.746785 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/clearable_file_input_small.html
+-rw-r--r--   0        0        0       88 2023-05-13 10:21:01.746918 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/date.html
+-rw-r--r--   0        0        0      262 2023-05-13 10:21:01.747065 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/range.html
+-rw-r--r--   0        0        0      881 2023-05-13 10:21:01.747227 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/split_datetime_vertical.html
+-rw-r--r--   0        0        0      459 2023-05-13 10:21:01.747399 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/textarea.html
+-rw-r--r--   0        0        0       88 2023-05-13 10:21:01.747528 django_unfold-0.6.2/src/unfold/templates/unfold/widgets/time.html
+-rw-r--r--   0        0        0        0 2023-05-13 10:21:01.747617 django_unfold-0.6.2/src/unfold/templatetags/__init__.py
+-rw-r--r--   0        0        0     3559 2023-05-13 10:21:01.747806 django_unfold-0.6.2/src/unfold/templatetags/unfold.py
+-rw-r--r--   0        0        0    10012 2023-05-13 10:21:01.747989 django_unfold-0.6.2/src/unfold/templatetags/unfold_list.py
+-rw-r--r--   0        0        0      576 2023-05-13 10:21:01.748144 django_unfold-0.6.2/src/unfold/typing.py
+-rw-r--r--   0        0        0     3878 2023-05-13 10:21:01.748551 django_unfold-0.6.2/src/unfold/utils.py
+-rw-r--r--   0        0        0      708 2023-05-13 10:21:01.748709 django_unfold-0.6.2/src/unfold/views.py
+-rw-r--r--   0        0        0     8150 2023-05-13 10:21:01.748887 django_unfold-0.6.2/src/unfold/widgets.py
+-rw-r--r--   0        0        0    27771 1970-01-01 00:00:00.000000 django_unfold-0.6.2/setup.py
+-rw-r--r--   0        0        0    26327 1970-01-01 00:00:00.000000 django_unfold-0.6.2/PKG-INFO
```

### Comparing `django_unfold-0.6.1/LICENSE` & `django_unfold-0.6.2/LICENSE`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/README.md` & `django_unfold-0.6.2/README.md`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/pyproject.toml` & `django_unfold-0.6.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "django-unfold"
-version = "0.6.1"
+version = "0.6.2"
 description = "Clean & minimal Django admin theme based on Tailwind CSS"
 license = "MIT"
 readme = "README.md"
 authors = []
 homepage = "https://unfoldadmin.com"
 repository = "https://github.com/unfoldadmin/django-unfold"
 packages = [
```

### Comparing `django_unfold-0.6.1/src/unfold/admin.py` & `django_unfold-0.6.2/src/unfold/admin.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/checks.py` & `django_unfold-0.6.2/src/unfold/checks.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/admin.py` & `django_unfold-0.6.2/src/unfold/contrib/filters/admin.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/forms.py` & `django_unfold-0.6.2/src/unfold/contrib/filters/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css` & `django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/css/nouislider.min.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js` & `django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/DateTimeShortcuts.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js` & `django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/admin-numeric-filter.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js` & `django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/nouislider.min.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js` & `django_unfold-0.6.2/src/unfold/contrib/filters/static/unfold/filters/js/wNumb.min.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html` & `django_unfold-0.6.2/src/unfold/contrib/filters/templates/unfold/filters/filters_numeric_slider.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/css/trix.css` & `django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/css/trix.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js` & `django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/js/trix.config.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/forms/static/unfold/forms/js/trix.js` & `django_unfold-0.6.2/src/unfold/contrib/forms/static/unfold/forms/js/trix.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html` & `django_unfold-0.6.2/src/unfold/contrib/forms/templates/unfold/forms/helpers/toolbar.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/forms/widgets.py` & `django_unfold-0.6.2/src/unfold/contrib/forms/widgets.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/forms.py` & `django_unfold-0.6.2/src/unfold/contrib/import_export/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/export.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/export.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_confirm.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_errors.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_preview.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html` & `django_unfold-0.6.2/src/unfold/contrib/import_export/templates/admin/import_export/import_validation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/decorators.py` & `django_unfold-0.6.2/src/unfold/decorators.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from typing import Any, Callable, Dict, Iterable, Optional, Union
 
 from django.contrib.admin.options import BaseModelAdmin
 from django.core.exceptions import PermissionDenied
-from django.db.models import Combinable, Model
-from django.db.models.expressions import BaseExpression
+from django.db.models import Model
+from django.db.models.expressions import BaseExpression, Combinable
 from django.http import HttpRequest, HttpResponse
 
 from .typing import ActionFunction
 
 
 def action(
     function: Optional[Callable] = None,
@@ -15,15 +15,15 @@
     permissions: Optional[Iterable[str]] = None,
     description: Optional[str] = None,
     url_path: Optional[str] = None,
     attrs: Optional[Dict[str, Any]] = None,
 ) -> ActionFunction:
     def decorator(func: Callable) -> ActionFunction:
         def inner(
-            model_admin: BaseModelAdmin[Any],
+            model_admin: BaseModelAdmin,
             request: HttpRequest,
             *args: Any,
             **kwargs,
         ) -> Optional[HttpResponse]:
             if permissions:
                 permission_checks = (
                     getattr(model_admin, f"has_{permission}_permission")
```

### Comparing `django_unfold-0.6.1/src/unfold/forms.py` & `django_unfold-0.6.2/src/unfold/forms.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/settings.py` & `django_unfold-0.6.2/src/unfold/settings.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/sites.py` & `django_unfold-0.6.2/src/unfold/sites.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/css/simplebar.css` & `django_unfold-0.6.2/src/unfold/static/unfold/css/simplebar.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/css/styles.css` & `django_unfold-0.6.2/src/unfold/static/unfold/css/styles.css`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.js` & `django_unfold-0.6.2/src/unfold/static/unfold/js/alpine.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/js/alpine.persist.js` & `django_unfold-0.6.2/src/unfold/static/unfold/js/alpine.persist.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/js/app.js` & `django_unfold-0.6.2/src/unfold/static/unfold/js/app.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/js/htmx.js` & `django_unfold-0.6.2/src/unfold/static/unfold/js/htmx.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/static/unfold/js/simplebar.js` & `django_unfold-0.6.2/src/unfold/static/unfold/js/simplebar.js`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/actions.html` & `django_unfold-0.6.2/src/unfold/templates/admin/actions.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/app_index.html` & `django_unfold-0.6.2/src/unfold/templates/admin/app_index.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/app_list.html` & `django_unfold-0.6.2/src/unfold/templates/admin/app_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/auth/user/change_password.html` & `django_unfold-0.6.2/src/unfold/templates/admin/auth/user/change_password.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/base.html` & `django_unfold-0.6.2/src/unfold/templates/admin/base.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/change_form.html` & `django_unfold-0.6.2/src/unfold/templates/admin/change_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/change_form_object_tools.html` & `django_unfold-0.6.2/src/unfold/templates/admin/change_form_object_tools.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/change_list.html` & `django_unfold-0.6.2/src/unfold/templates/admin/change_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/change_list_object_tools.html` & `django_unfold-0.6.2/src/unfold/templates/admin/change_list_object_tools.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/change_list_results.html` & `django_unfold-0.6.2/src/unfold/templates/admin/change_list_results.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/date_hierarchy.html` & `django_unfold-0.6.2/src/unfold/templates/admin/date_hierarchy.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/delete_confirmation.html` & `django_unfold-0.6.2/src/unfold/templates/admin/delete_confirmation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/delete_selected_confirmation.html` & `django_unfold-0.6.2/src/unfold/templates/admin/delete_selected_confirmation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/stacked.html` & `django_unfold-0.6.2/src/unfold/templates/admin/edit_inline/stacked.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/edit_inline/tabular.html` & `django_unfold-0.6.2/src/unfold/templates/admin/edit_inline/tabular.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/filter.html` & `django_unfold-0.6.2/src/unfold/templates/admin/filter.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/includes/fieldset.html` & `django_unfold-0.6.2/src/unfold/templates/admin/includes/fieldset.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/index.html` & `django_unfold-0.6.2/src/unfold/templates/admin/index.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/login.html` & `django_unfold-0.6.2/src/unfold/templates/admin/login.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/nav_sidebar.html` & `django_unfold-0.6.2/src/unfold/templates/admin/nav_sidebar.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/object_history.html` & `django_unfold-0.6.2/src/unfold/templates/admin/object_history.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/pagination.html` & `django_unfold-0.6.2/src/unfold/templates/admin/pagination.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/search_form.html` & `django_unfold-0.6.2/src/unfold/templates/admin/search_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/submit_line.html` & `django_unfold-0.6.2/src/unfold/templates/admin/submit_line.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/widgets/clearable_file_input.html` & `django_unfold-0.6.2/src/unfold/templates/admin/widgets/clearable_file_input.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/widgets/related_widget_wrapper.html` & `django_unfold-0.6.2/src/unfold/templates/admin/widgets/related_widget_wrapper.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/admin/widgets/split_datetime.html` & `django_unfold-0.6.2/src/unfold/templates/admin/widgets/split_datetime.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/auth/widgets/read_only_password_hash.html` & `django_unfold-0.6.2/src/unfold/templates/auth/widgets/read_only_password_hash.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/registration/logged_out.html` & `django_unfold-0.6.2/src/unfold/templates/registration/logged_out.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/registration/password_change_done.html` & `django_unfold-0.6.2/src/unfold/templates/registration/password_change_done.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/registration/password_change_form.html` & `django_unfold-0.6.2/src/unfold/templates/registration/password_change_form.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/actions_row.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/actions_row.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/app_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/app_list_default.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/app_list_default.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/display_label.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/display_label.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/history.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/history.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages/error.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages/error.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/messages.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/messages.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/navigation.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/navigation.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/search.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/search_results.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/search_results.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/tab_list.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/tab_list.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/userlinks.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/userlinks.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/helpers/welcomemsg.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/helpers/welcomemsg.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/layouts/base_simple.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/layouts/base_simple.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/layouts/skeleton.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/layouts/skeleton.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/widgets/clearable_file_input_small.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/widgets/clearable_file_input_small.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templates/unfold/widgets/split_datetime_vertical.html` & `django_unfold-0.6.2/src/unfold/templates/unfold/widgets/split_datetime_vertical.html`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templatetags/unfold.py` & `django_unfold-0.6.2/src/unfold/templatetags/unfold.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/templatetags/unfold_list.py` & `django_unfold-0.6.2/src/unfold/templatetags/unfold_list.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/typing.py` & `django_unfold-0.6.2/src/unfold/typing.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/utils.py` & `django_unfold-0.6.2/src/unfold/utils.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/views.py` & `django_unfold-0.6.2/src/unfold/views.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/src/unfold/widgets.py` & `django_unfold-0.6.2/src/unfold/widgets.py`

 * *Files identical despite different names*

### Comparing `django_unfold-0.6.1/setup.py` & `django_unfold-0.6.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
  'unfold.contrib.import_export': ['templates/admin/import_export/*']}
 
 install_requires = \
 ['django>=3.2']
 
 setup_kwargs = {
     'name': 'django-unfold',
-    'version': '0.6.1',
+    'version': '0.6.2',
     'description': 'Clean & minimal Django admin theme based on Tailwind CSS',
     'long_description': '![Screenshot - Objects Listing](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-1.jpg)\n\n![Screenshot - Login Page](https://github.com/unfoldadmin/django-unfold/raw/main/screenshot-2.jpg)\n\n## Unfold Django Admin Theme\n\nUnfold is a new theme for Django Admin incorporating some most common practises for building full-fledged admin areas.\n\n- **Visual**: provides new user interface based on Tailwind CSS framework\n- **Sidebar:** simplifies definition of custom sidebar navigation\n- **Dark mode:** supports both light and dark mode versions\n- **Configuration:** most of the basic options can be changed in settings.py\n- **Dependencies:** completely based only on `django.contrib.admin`\n- **Filters:** custom widgets for filters (e.g. numeric filter)\n- **Actions:** multiple ways how to define actions within different parts of admin\n\n## Table of Contents\n\n- [Unfold Django Admin Theme](#unfold-django-admin-theme)\n- [Table of Contents](#table-of-contents)\n- [Installation](#installation)\n- [Configuration](#configuration)\n  - [Available settings.py options](#available-settingspy-options)\n  - [Available unfold.admin.ModelAdmin options](#available-unfoldadminmodeladmin-options)\n- [Decorators](#decorators)\n  - [@display](#display)\n- [Actions](#actions)\n  - [Actions overview](#actions-overview)\n  - [Custom unfold @action decorator](#custom-unfold-action-decorator)\n  - [Action handler functions](#action-handler-functions)\n    - [For submit row action](#for-submit-row-action)\n    - [For global, row and detail action](#for-global-row-and-detail-action)\n  - [Action examples](#action-examples)\n- [Filters](#filters)\n- [Third party packages](#third-party-packages)\n  - [django-import-export](#django-import-export)\n- [User Admin Form](#user-admin-form)\n- [Adding Custom Styles and Scripts](#adding-custom-styles-and-scripts)\n- [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet)\n- [Custom Admin Dashboard](#custom-admin-dashboard)\n- [Unfold Development](#unfold-development)\n  - [Pre-commit](#pre-commit)\n  - [Poetry Configuration](#poetry-configuration)\n  - [Compiling Tailwind](#compiling-tailwind)\n\n## Installation\n\nThe installation process is minimal. Everything what is needed after installation is to put new application at the beginning of **INSTALLED_APPS**. Default admin configuration in urls.py can stay as it is and there are no changes required.\n\n```python\n# settings.py\n\nINSTALLED_APPS = [\n    "unfold",  # before django.contrib.admin\n    "unfold.contrib.filters",  # optional, if special filters are needed\n    "unfold.contrib.forms",  # optional, if special form elements are needed\n    "unfold.contrib.import_export",  # optional, if django-import-export package is used\n    "django.contrib.admin",  # required\n]\n```\n\nIn case you need installation command below are the versions for `pip` and `poetry` which needs to be executed in shell.\n\n```bash\npip install django-unfold\npoetry add django-unfold\n```\n\nJust for an example below is the minimal admin configuration in terms of adding Unfold into URL paths.\n\n```python\n# urls.py\n\nfrom django.contrib import admin\nfrom django.urls import path\n\nurlpatterns = [\n    path("admin/", admin.site.urls),\n    # Other URL paths\n]\n```\n\nAfter installation, it is required that admin classes are going to inherit from custom `ModelAdmin` available in `unfold.admin`.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom unfold.admin import ModelAdmin\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    pass\n```\n\n**Note:** Registered admin models coming from third party packages are not going to properly work with Unfold because of parent class. By default, these models are registered by using `django.contrib.admin.ModelAdmin` but it is needed to use `unfold.admin.ModelAdmin`. Solution for this problem is to unregister model and then again register it back by using `unfold.admin.ModelAdmin`.\n\n```python\n# admin.py\nfrom django.contrib import admin\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\n\n\nadmin.site.unregister(User)\n\n\n@admin.register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    pass\n```\n\n## Configuration\n\n### Available settings.py options\n\n```python\n# settings.py\n\nfrom django.templatetags.static import static\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\n\nUNFOLD = {\n    "SITE_TITLE": None,\n    "SITE_HEADER": None,\n    "SITE_URL": "/",\n    "SITE_ICON": lambda request: static("logo.svg"),\n    "SITE_SYMBOL": "speed",  # symbol from icon set\n    "DASHBOARD_CALLBACK": "sample_app.dashboard_callback",\n    "LOGIN": {\n        "image": lambda r: static("sample/login-bg.jpg"),\n        "redirect_after": lambda r: reverse_lazy("admin:APP_MODEL_changelist"),\n    },\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n    "COLORS": {\n        "primary": {\n            "50": "250 245 255",\n            "100": "243 232 255",\n            "200": "233 213 255",\n            "300": "216 180 254",\n            "400": "192 132 252",\n            "500": "168 85 247",\n            "600": "147 51 234",\n            "700": "126 34 206",\n            "800": "107 33 168",\n            "900": "88 28 135",\n        },\n    },\n    "EXTENSIONS": {\n        "modeltranslation": {\n            "flags": {\n                "en": "🇬🇧",\n                "fr": "🇫🇷",\n                "nl": "🇧🇪",\n            },\n        },\n    },\n    "SIDEBAR": {\n        "show_search": False,  # Search in applications and models names\n        "show_all_applications": False,  # Dropdown with all applications and models\n        "navigation": [\n            {\n                "title": _("Navigation"),\n                "separator": True,  # Top border\n                "items": [\n                    {\n                        "title": _("Dashboard"),\n                        "icon": "dashboard",  # Supported icon set: https://fonts.google.com/icons\n                        "link": reverse_lazy("admin:index"),\n                        "badge": "sample_app.badge_callback",\n                    },\n                    {\n                        "title": _("Users"),\n                        "icon": "people",\n                        "link": reverse_lazy("admin:users_user_changelist"),\n                    },\n                ],\n            },\n        ],\n    },\n    "TABS": [\n        {\n            "models": [\n                "app_label.model_name_in_lowercase",\n            ],\n            "items": [\n                {\n                    "title": _("Your custom title"),\n                    "link": reverse_lazy("admin:app_label_model_name_changelist"),\n                },\n            ],\n        },\n    ],\n}\n\n\ndef dashboard_callback(request, context):\n    """\n    Callback to prepare custom variables for index template which is used as dashboard\n    template. It can be overridden in application by creating custom admin/index.html.\n    """\n    context.update(\n        {\n            "sample": "example",  # this will be injected into templates/admin/index.html\n        }\n    )\n    return context\n\n\ndef badge_callback(request):\n    return 3\n```\n\n### Available unfold.admin.ModelAdmin options\n\n```python\nfrom django import models\nfrom django.contrib import admin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.forms.widgets import WysiwygWidget\n\n\n@admin.register(MyModel)\nclass CustomAdminClass(ModelAdmin):\n    # Preprocess content of readonly fields before render\n    readonly_preprocess_fields = {\n        "model_field_name": "html.unescape",\n        "other_field_name": lambda content: content.strip(),\n    }\n\n    # Display submit button in filters\n    list_filter_submit = False\n\n    # Custom actions\n    actions_list = []  # Displayed above the results list\n    actions_row = []  # Displayed in a table row in results list\n    actions_detail = []  # Displayed at the top of for in object detail\n    actions_submit_line = []  # Displayed near save in object detail\n\n    formfield_overrides = {\n        models.TextField: WysiwygWidget,\n    }\n```\n\n## Decorators\n\n### @display\n\nUnfold introduces it\'s own `unfold.decorators.display` decorator. By default it has exactly same behavior as native `django.contrib.admin.decorators.display` but it adds same customizations which helps to extends default logic.\n\n`@display(label=True)`, `@display(label={"value1": "success"})` displays a result as a label. This option fits for different types of statuses. Label can be either boolean indicating we want to use label with default color or dict where the dict is responsible for displaying labels in different colors. At the moment these color combinations are supported: success(green), info(blue), danger(red) and warning(orange).\n\n`@display(header=True)` displays in results list two information in one table cell. Good example is when we want to display customer information, first line is going to be customer\'s name and right below the name display corresponding email address. Method with such a decorator is supposed to return a list with two elements `return "Full name", "E-mail address"`.\n\n```python\n# models.py\n\nfrom django.db.models import TextChoices\nfrom django.utils.translation import gettext_lazy as _\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import display\n\n\nclass UserStatus(TextChoices):\n    ACTIVE = "ACTIVE", _("Active")\n    PENDING = "PENDING", _("Pending")\n    INACTIVE = "INACTIVE", _("Inactive")\n    CANCELLED = "CANCELLED", _("Cancelled")\n\n\nclass UserAdmin(ModelAdmin):\n    list_display = [\n        "display_as_two_line_heading",\n        "show_status",\n        "show_status_with_custom_label",\n    ]\n\n    @display(\n        description=_("Status"),\n        ordering="status",\n        label=True,\n        mapping={\n            UserStatus.ACTIVE: "success",\n            UserStatus.PENDING: "info",\n            UserStatus.INACTIVE: "warning",\n            UserStatus.CANCELLED: "danger",\n        },\n    )\n    def show_status(self, obj):\n        return obj.status\n\n    @display(description=_("Status with label"), ordering="status", label=True)\n    def show_status_with_custom_label(self, obj):\n        return obj.status, obj.get_status_display()\n\n    @display(header=True)\n    def display_as_two_line_heading(self, obj):\n        return "First main heading", "Smaller additional description"\n```\n\n## Actions\n\nIt is highly recommended to read the base [Django actions documentation](https://docs.djangoproject.com/en/4.2/ref/contrib/admin/actions/) before reading this section, since Unfold actions are derived from Django actions.\n\n### Actions overview\n\nBesides traditional actions selected from dropdown, Unfold supports several other types of actions. Following table\ngives overview of all available actions together with their recommended usage:\n\n| Type of action | Appearance                               | Usage                                                                                      | Examples of usage                      |\n| -------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------- |\n| Default        | List view - top of listing (in dropdown) | Actions, where you want to select specific subset of instances to perform this action upon | Bulk deleting, bulk activation         |\n| Global         | List view - top of listing (as buttons)  | General actions for model, without selecting specific instances                            | Import, export                         |\n| Row            | List view - in each row                  | Action for one specific instance, executable from listing                                  | Activation, sync with external service |\n| Detail         | Detail view - top of detail              | Action for one specific instance, executable from detail                                   | Activation, sync with external service |\n| Submit line    | Detail view - near submit button         | Action performed during form submit (instance save)                                        | Publishing article together with save  |\n\n### Custom unfold @action decorator\n\nUnfold also uses custom `@action` decorator, supporting 2 more parameters in comparison to base `@action` decorator:\n\n- `url_path`: Action path name, used to override the path under which the action will be available\n  (if not provided, URL path will be generated by Unfold)\n- `attrs`: Dictionary of the additional attributes added to the `<a>` element, used for e.g. opening action in new tab (`{"target": "_blank"}`)\n\n### Action handler functions\n\nThis section provides explanation of how the action handler functions should be constructed for Unfold actions.\nFor default actions, follow official Django admin documentation.\n\n#### For submit row action\n\nSubmit row actions work a bit differently when compared to other custom Unfold actions.\nThese actions first invoke form save (same as if you hit `Save` button) and then lets you\nperform additional logic on already saved instance.\n\n#### For global, row and detail action\n\nAll these actions are based on custom URLs generated for each of them. Handler function for these views is\nbasically function based view.\n\nFor actions without intermediate steps, you can write all the logic inside handler directly. Request and object ID\nare both passed to these action handler functions, so you are free to fetch the instance from database and perform any\noperations with it. In the end, it is recommended to return redirect back to either detail or listing, based on where\nthe action was triggered from.\n\nFor actions with intermediate steps, it is recommended to use handler function only to redirect to custom URL with custom\nview. This view can be extended from base Unfold view, to have unified experience.\n\nIf that\'s confusing, there are examples for both these actions in next section.\n\n### Action examples\n\n```python\n# admin.py\n\nfrom django.db.models import Model\nfrom django.contrib.admin import register\nfrom django.shortcuts import redirect\nfrom django.urls import reverse_lazy\nfrom django.utils.translation import gettext_lazy as _\nfrom django.http import HttpRequest\nfrom unfold.admin import ModelAdmin\nfrom unfold.decorators import action\n\n\nclass User(Model):\n    pass\n\n\n@register(User)\nclass UserAdmin(ModelAdmin):\n    actions_list = ["changelist_global_action_import"]\n    actions_row = ["changelist_row_action_view_on_website"]\n    actions_detail = ["change_detail_action_block"]\n    actions_submit_line = ["submit_line_action_activate"]\n\n    @action(description=_("Save & Activate"))\n    def submit_line_action_activate(self, request: HttpRequest, obj: User):\n        """\n        If instance is modified in any way, it also needs to be saved,\n        since this handler is invoked after instance is saved.\n        :param request:\n        :param obj: Model instance that was manipulated, with changes already saved to database\n        :return: None, this handler should not return anything\n        """\n        obj.is_active = True\n        obj.save()\n\n    @action(description=_("Import"), url_path="import")\n    def changelist_global_action_import(self, request: HttpRequest):\n        """\n        Handler for global actions does not receive any queryset or object ids, because it is\n        meant to be used for general actions for given model.\n        :param request:\n        :return: View, as described in section above\n        """\n        # This is example of action redirecting to custom page, where the action will be handled\n        # (with intermediate steps)\n        return redirect(\n          reverse_lazy("view-where-import-will-be-handled")\n        )\n\n    @action(description=_("Row"), url_path="row-action", attrs={"target": "_blank"})\n    def changelist_row_action_view_on_website(self, request: HttpRequest, object_id: int):\n        """\n        Handler for list row action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        return redirect(f"https://example.com/{object_id}")\n\n    @action(description=_("Detail"), url_path="detail-action", attrs={"target": "_blank"})\n    def change_detail_action_block(self, request: HttpRequest, object_id: int):\n        """\n        Handler for detail action.\n        :param request:\n        :param object_id: ID of instance that this action was invoked for\n        :return: View, as described in section above\n        """\n        # This is example of action that handled whole logic inside handler\n        # function and redirects back to object detail\n        user = User.objects.get(pk=object_id)\n        user.block()\n        return redirect(\n            reverse_lazy("admin:users_user_change", args=(object_id,))\n        )\n```\n\n## Filters\n\nBy default, Django admin handles all filters as regular HTML links pointing at the same URL with different query parameters. This approach is for basic filtering more than enough. In the case of more advanced filtering by incorporating input fields, it is not going to work.\n\nCurrently, Unfold implements numeric filters inside `unfold.contrib.filters` application. In order to use these filters, it is required to add this application into `INSTALLED_APPS` in `settings.py` right after `unfold` application.\n\n```python\n# admin.py\n\nfrom django.contrib import admin\nfrom django.contrib.auth.models import User\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.filters.admin import (\n    RangeNumericListFilter,\n    RangeNumericFilter,\n    SingleNumericFilter,\n    SliderNumericFilter,\n    RangeDateFilter,\n    RangeDateTimeFilter,\n)\n\n\nclass CustomSliderNumericFilter(SliderNumericFilter):\n    MAX_DECIMALS = 2\n    STEP = 10\n\n\nclass CustomRangeNumericListFilter(RangeNumericListFilter):\n    parameter_name = "items_count"\n    title = "items"\n\n\n@admin.register(User)\nclass YourModelAdmin(ModelAdmin):\n    list_filter_submit = True  # Submit button at the bottom of the filter\n    list_filter = (\n        ("field_A", SingleNumericFilter),  # Numeric single field search, __gte lookup\n        ("field_B", RangeNumericFilter),  # Numeric range search, __gte and __lte lookup\n        ("field_C", SliderNumericFilter),  # Numeric range filter but with slider\n        ("field_D", CustomSliderNumericFilter),  # Numeric filter with custom attributes\n        ("field_E", RangeDateFilter),  # Date filter\n        ("field_F", RangeDateTimeFilter),  # Datetime filter\n        CustomRangeNumericListFilter,  # Numeric range search not restricted to a model field\n    )\n\n    def get_queryset(self, request):\n        return super().get_queryset().annotate(items_count=Count("item", distinct=True))\n```\n\n## Third party packages\n\n### django-import-export\n\nTo get proper visual appearance for django-import-export, two things are needed\n\n1. Add `unfold.contrib.import_export` to `INSTALLED_APPS` at the begging of the file. This action will override all templates coming from the plugin.\n2. Change `import_form_class` and `export_form_class` in ModelAdmin which is inheriting from `ImportExportModelAdmin`. This chunk of code is responsible for adding proper styling to form elements.\n\n```python\nfrom unfold.admin import ModelAdmin\nfrom unfold.contrib.import_export.forms import ExportForm, ImportForm\n\nclass ExampleAdmin(ModelAdmin, ImportExportModelAdmin):\n    import_form_class = ImportForm\n    export_form_class = ExportForm\n```\n\n## User Admin Form\n\nUser\'s admin in Django is specific as it contains several forms which are requiring custom styling. All of these forms has been inherited and accordingly adjusted. In user admin class it is needed to use these inherited form classes to enable custom styling matching rest of the website.\n\n```python\n# models.py\n\nfrom django.contrib.admin import register\nfrom django.contrib.auth.models import User\nfrom django.contrib.auth.admin import UserAdmin as BaseUserAdmin\n\nfrom unfold.admin import ModelAdmin\nfrom unfold.forms import AdminPasswordChangeForm, UserChangeForm, UserCreationForm\n\n\n@register(User)\nclass UserAdmin(BaseUserAdmin, ModelAdmin):\n    form = UserChangeForm\n    add_form = UserCreationForm\n    change_password_form = AdminPasswordChangeForm\n```\n\n## Adding Custom Styles and Scripts\n\nTo add new custom styles, for example for custom dashboard, it is possible to load them via **STYLES** key in **UNFOLD** dict. This key accepts a list of strings or lambda functions which will be loaded on all pages. JavaScript files can be loaded by using similar apprach, but **SCRIPTS** is used.\n\n```python\n# settings.py\n\nfrom django.templatetags.static import static\n\nUNFOLD = {\n    "STYLES": [\n        lambda request: static("css/style.css"),\n    ],\n    "SCRIPTS": [\n        lambda request: static("js/script.js"),\n    ],\n}\n```\n\n## Project Level Tailwind Stylesheet\n\nWhen creating custom dashboard or adding custom components, it is needed to add own styles. Adding custom styles is described above. Most of the time, it is supposed that new elements are going to match with the rest of the administration panel. First of all, create tailwind.config.js in your application. Below is located minimal configuration for this file.\n\n```javascript\n// tailwind.config.js\n\nmodule.exports = {\n  content: ["./your_project/**/*.{html,py,js}"],\n  // In case custom colors are defined in UNFOLD["COLORS"]\n  colors: {\n    primary: {\n      100: "rgb(var(--color-primary-100) / <alpha-value>)",\n      200: "rgb(var(--color-primary-200) / <alpha-value>)",\n      300: "rgb(var(--color-primary-300) / <alpha-value>)",\n      400: "rgb(var(--color-primary-400) / <alpha-value>)",\n      500: "rgb(var(--color-primary-500) / <alpha-value>)",\n      600: "rgb(var(--color-primary-600) / <alpha-value>)",\n      700: "rgb(var(--color-primary-700) / <alpha-value>)",\n      800: "rgb(var(--color-primary-800) / <alpha-value>)",\n      900: "rgb(var(--color-primary-900) / <alpha-value>)",\n    },\n  },\n};\n```\n\nOnce the configuration file is set, it is possible to compile new styles which can be loaded into admin by using **STYLES** key in **UNFOLD** dict.\n\n```bash\nnpx tailwindcss  -o your_project/static/css/styles.css --watch --minify\n```\n\n## Custom Admin Dashboard\n\nThe most common thing which needs to be adjusted for each project in admin is the dashboard. By default Unfold does not provide any dashboard components. The default dashboard experience with list of all applications and models is kept with proper styling matching rest of the components but thats it. Anyway, Unfold was created that creation of custom dashboard will be streamlined.\n\nCreate `templates/admin/index.html` in your project and paste the base template below into it. By default, all your custom styles here are not compiled because CSS classes are located in your specific project. Here it is needed to set up the Tailwind for your project and all requried instructions are located in [Project Level Tailwind Stylesheet](#project-level-tailwind-stylesheet) chapter.\n\n```\n{% extends \'unfold/layouts/base_simple.html\' %}\n\n{% load cache humanize i18n %}\n\n{% block breadcrumbs %}{% endblock %}\n\n{% block title %}{% if subtitle %}{{ subtitle }} | {% endif %}{{ title }} | {{ site_title|default:_(\'Django site admin\') }}{% endblock %}\n\n{% block branding %}\n    <h1 id="site-name"><a href="{% url \'admin:index\' %}">{{ site_header|default:_(\'Django administration\') }}</a></h1>\n{% endblock %}\n\n{% block content %}\n    Start creating your own Tailwind components here\n{% endblock %}\n```\n\nNote: In case that it is needed to pass custom variables into dashboard tamplate, check **DASHOARD_CALLBACK** in **UNFOLD** dict.\n\n## Unfold Development\n\n### Pre-commit\n\nBefore adding any source code, it is recommended to have pre-commit installed on your local computer to check for all potential issues when comitting the code.\n\n```bash\npip install pre-commit\npre-commit install\npre-commit install --hook-type commit-msg\n```\n\n### Poetry Configuration\n\nTo add a new feature or fix the easiest approach is to use django-unfold in combination with Poetry. The process looks like:\n\n- Install django-unfold via `poetry add django-unfold`\n- After that it is needed to git clone the repository somewhere on local computer.\n- Edit _pyproject.toml_ and update django-unfold line `django-unfold = { path = "../django-unfold", develop = true}`\n- Lock and update via `poetry lock && poetry update`\n\n### Compiling Tailwind\n\nAt the moment project contains package.json with all dependencies required to compile new CSS file. Tailwind configuration file is set to check all html, js and py files for Tailwind\'s classeses occurrences.\n\n```bash\nnpm install\nnpx tailwindcss -i styles.css -o src/unfold/static/unfold/css/styles.css --watch --minify\n\nnpm run tailwind:watch # run after each change in code\nnpm run tailwind:build # run once\n```\n\nSome components like datepickers, calendars or selectors in admin was not possible to style by overriding html templates so their default styles are overriden in **styles.css**.\n\nNone: most of the custom styles localted in style.css are created via `@apply some-tailwind-class;`.\n',
     'author': 'None',
     'author_email': 'None',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://unfoldadmin.com',
```

### Comparing `django_unfold-0.6.1/PKG-INFO` & `django_unfold-0.6.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-unfold
-Version: 0.6.1
+Version: 0.6.2
 Summary: Clean & minimal Django admin theme based on Tailwind CSS
 Home-page: https://unfoldadmin.com
 License: MIT
 Keywords: django,admin,tailwind,theme
 Requires-Python: >=3.8
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
```

