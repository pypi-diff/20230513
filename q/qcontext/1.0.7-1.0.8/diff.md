# Comparing `tmp/qcontext-1.0.7.tar.gz` & `tmp/qcontext-1.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "qcontext-1.0.7.tar", last modified: Fri May 12 03:11:51 2023, max compression
+gzip compressed data, was "qcontext-1.0.8.tar", last modified: Sat May 13 19:41:19 2023, max compression
```

## Comparing `qcontext-1.0.7.tar` & `qcontext-1.0.8.tar`

### file list

```diff
@@ -1,354 +1,355 @@
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.285561 qcontext-1.0.7/
--rw-rw-rw-   0        0        0     1093 2023-02-26 16:41:50.000000 qcontext-1.0.7/LICENSE.txt
--rw-rw-rw-   0        0        0     2788 2023-05-12 03:11:51.285561 qcontext-1.0.7/PKG-INFO
--rw-rw-rw-   0        0        0      545 2023-05-11 02:27:47.000000 qcontext-1.0.7/README.md
--rw-rw-rw-   0        0        0     1577 2023-05-12 03:11:17.000000 qcontext-1.0.7/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-12 03:11:51.285561 qcontext-1.0.7/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:50.985561 qcontext-1.0.7/src/
--rw-rw-rw-   0        0        0        0 2023-03-20 19:19:08.000000 qcontext-1.0.7/src/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:50.988566 qcontext-1.0.7/src/qcontext/
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.250561 qcontext-1.0.7/src/qcontext/.assets/
--rw-rw-rw-   0        0        0      277 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/activity.svg
--rw-rw-rw-   0        0        0      357 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/airplay.svg
--rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/alert-circle.svg
--rw-rw-rw-   0        0        0      411 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/alert-octagon.svg
--rw-rw-rw-   0        0        0      419 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/alert-triangle.svg
--rw-rw-rw-   0        0        0      393 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/align-center.svg
--rw-rw-rw-   0        0        0      394 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/align-justify.svg
--rw-rw-rw-   0        0        0      391 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/align-left.svg
--rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/align-right.svg
--rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/anchor.svg
--rw-rw-rw-   0        0        0      563 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/aperture.svg
--rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/archive.svg
--rw-rw-rw-   0        0        0      355 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-down-circle.svg
--rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-down-left.svg
--rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-down-right.svg
--rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-down.svg
--rw-rw-rw-   0        0        0      354 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-left-circle.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-left.svg
--rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-right-circle.svg
--rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-right.svg
--rw-rw-rw-   0        0        0      352 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-up-circle.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-up-left.svg
--rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-up-right.svg
--rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/arrow-up.svg
--rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/at-sign.svg
--rw-rw-rw-   0        0        0      320 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/award.svg
--rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bar-chart-2.svg
--rw-rw-rw-   0        0        0      348 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bar-chart.svg
--rw-rw-rw-   0        0        0      422 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/battery-charging.svg
--rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/battery.svg
--rw-rw-rw-   0        0        0      455 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bell-off.svg
--rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bell.svg
--rw-rw-rw-   0        0        0      293 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bluetooth.svg
--rw-rw-rw-   0        0        0      322 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bold.svg
--rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/book-open.svg
--rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/book.svg
--rw-rw-rw-   0        0        0      282 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/bookmark.svg
--rw-rw-rw-   0        0        0      457 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/box.svg
--rw-rw-rw-   0        0        0      338 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/briefcase.svg
--rw-rw-rw-   0        0        0      405 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/calendar.svg
--rw-rw-rw-   0        0        0      380 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/camera-off.svg
--rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/camera.svg
--rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cast.svg
--rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/check-circle.svg
--rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/check-square.svg
--rw-rw-rw-   0        0        0      257 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/check.svg
--rw-rw-rw-   0        0        0      264 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevron-down.svg
--rw-rw-rw-   0        0        0      265 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevron-left.svg
--rw-rw-rw-   0        0        0      265 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevron-right.svg
--rw-rw-rw-   0        0        0      263 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevron-up.svg
--rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevrons-down.svg
--rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevrons-left.svg
--rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevrons-right.svg
--rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chevrons-up.svg
--rw-rw-rw-   0        0        0      443 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/chrome.svg
--rw-rw-rw-   0        0        0      253 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/circle.svg
--rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/clipboard.svg
--rw-rw-rw-   0        0        0      299 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/clock.svg
--rw-rw-rw-   0        0        0      552 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud-drizzle.svg
--rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud-lightning.svg
--rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud-off.svg
--rw-rw-rw-   0        0        0      416 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud-rain.svg
--rw-rw-rw-   0        0        0      567 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud-snow.svg
--rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cloud.svg
--rw-rw-rw-   0        0        0      302 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/code.svg
--rw-rw-rw-   0        0        0      481 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/codepen.svg
--rw-rw-rw-   0        0        0      633 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/codesandbox.svg
--rw-rw-rw-   0        0        0      442 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/coffee.svg
--rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/columns.svg
--rw-rw-rw-   0        0        0      416 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/command.svg
--rw-rw-rw-   0        0        0      337 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/compass.svg
--rw-rw-rw-   0        0        0      346 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/copy.svg
--rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-down-left.svg
--rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-down-right.svg
--rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-left-down.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-left-up.svg
--rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-right-down.svg
--rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-right-up.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-up-left.svg
--rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/corner-up-right.svg
--rw-rw-rw-   0        0        0      662 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/cpu.svg
--rw-rw-rw-   0        0        0      324 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/credit-card.svg
--rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/crop.svg
--rw-rw-rw-   0        0        0      432 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/crosshair.svg
--rw-rw-rw-   0        0        0      367 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/database.svg
--rw-rw-rw-   0        0        0      369 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/delete.svg
--rw-rw-rw-   0        0        0      290 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/disc.svg
--rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/divide-circle.svg
--rw-rw-rw-   0        0        0      414 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/divide-square.svg
--rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/divide.svg
--rw-rw-rw-   0        0        0      329 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/dollar-sign.svg
--rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/download-cloud.svg
--rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/download.svg
--rw-rw-rw-   0        0        0      419 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/dribbble.svg
--rw-rw-rw-   0        0        0      269 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/droplet.svg
--rw-rw-rw-   0        0        0      286 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/edit-2.svg
--rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/edit-3.svg
--rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/edit.svg
--rw-rw-rw-   0        0        0      383 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/external-link.svg
--rw-rw-rw-   0        0        0      455 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/eye-off.svg
--rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/eye.svg
--rw-rw-rw-   0        0        0      298 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/facebook.svg
--rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/fast-forward.svg
--rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/feather.svg
--rw-rw-rw-   0        0        0      548 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/figma.svg
--rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/file-minus.svg
--rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/file-plus.svg
--rw-rw-rw-   0        0        0      468 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/file-text.svg
--rw-rw-rw-   0        0        0      332 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/file.svg
--rw-rw-rw-   0        0        0      581 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/film.svg
--rw-rw-rw-   0        0        0      285 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/filter.svg
--rw-rw-rw-   0        0        0      329 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/flag.svg
--rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/folder-minus.svg
--rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/folder-plus.svg
--rw-rw-rw-   0        0        0      306 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/folder.svg
--rw-rw-rw-   0        0        0      273 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/framer.svg
--rw-rw-rw-   0        0        0      385 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/frown.svg
--rw-rw-rw-   0        0        0      476 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/gift.svg
--rw-rw-rw-   0        0        0      372 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/git-branch.svg
--rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/git-commit.svg
--rw-rw-rw-   0        0        0      331 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/git-merge.svg
--rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/git-pull-request.svg
--rw-rw-rw-   0        0        0      522 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/github.svg
--rw-rw-rw-   0        0        0      485 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/gitlab.svg
--rw-rw-rw-   0        0        0      404 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/globe.svg
--rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/grid.svg
--rw-rw-rw-   0        0        0      479 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/hard-drive.svg
--rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/hash.svg
--rw-rw-rw-   0        0        0      390 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/headphones.svg
--rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/heart.svg
--rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/help-circle.svg
--rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/hexagon.svg
--rw-rw-rw-   0        0        0      327 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/home.svg
--rw-rw-rw-   0        0        0      364 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/image.svg
--rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/inbox.svg
--rw-rw-rw-   0        0        0      342 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/info.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/instagram.svg
--rw-rw-rw-   0        0        0      343 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/italic.svg
--rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/key.svg
--rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/layers.svg
--rw-rw-rw-   0        0        0      359 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/layout.svg
--rw-rw-rw-   0        0        0      570 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/life-buoy.svg
--rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/link-2.svg
--rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/link.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/linkedin.svg
--rw-rw-rw-   0        0        0      477 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/list.svg
--rw-rw-rw-   0        0        0      609 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/loader.svg
--rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/lock.svg
--rw-rw-rw-   0        0        0      363 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/log-in.svg
--rw-rw-rw-   0        0        0      362 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/log-out.svg
--rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/mail.svg
--rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/map-pin.svg
--rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/map.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/maximize-2.svg
--rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/maximize.svg
--rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/meh.svg
--rw-rw-rw-   0        0        0      341 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/menu.svg
--rw-rw-rw-   0        0        0      423 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/message-circle.svg
--rw-rw-rw-   0        0        0      300 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/message-square.svg
--rw-rw-rw-   0        0        0      489 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/mic-off.svg
--rw-rw-rw-   0        0        0      413 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/mic.svg
--rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/minimize-2.svg
--rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/minimize.svg
--rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/minus-circle.svg
--rw-rw-rw-   0        0        0      325 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/minus-square.svg
--rw-rw-rw-   0        0        0      256 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/minus.svg
--rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/monitor.svg
--rw-rw-rw-   0        0        0      276 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/moon.svg
--rw-rw-rw-   0        0        0      338 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/more-horizontal.svg
--rw-rw-rw-   0        0        0      336 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/more-vertical.svg
--rw-rw-rw-   0        0        0      306 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/mouse-pointer.svg
--rw-rw-rw-   0        0        0      481 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/move.svg
--rw-rw-rw-   0        0        0      322 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/music.svg
--rw-rw-rw-   0        0        0      274 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/navigation-2.svg
--rw-rw-rw-   0        0        0      272 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/navigation.svg
--rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/octagon.svg
--rw-rw-rw-   0        0        0      512 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/package.svg
--rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/paperclip.svg
--rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/pause-circle.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/pause.svg
--rw-rw-rw-   0        0        0      386 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/pen-tool.svg
--rw-rw-rw-   0        0        0      345 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/percent.svg
--rw-rw-rw-   0        0        0      571 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-call.svg
--rw-rw-rw-   0        0        0      613 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-forwarded.svg
--rw-rw-rw-   0        0        0      612 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-incoming.svg
--rw-rw-rw-   0        0        0      608 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-missed.svg
--rw-rw-rw-   0        0        0      586 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-off.svg
--rw-rw-rw-   0        0        0      612 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone-outgoing.svg
--rw-rw-rw-   0        0        0      515 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/phone.svg
--rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/pie-chart.svg
--rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/play-circle.svg
--rw-rw-rw-   0        0        0      258 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/play.svg
--rw-rw-rw-   0        0        0      345 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/plus-circle-gray.svg
--rw-rw-rw-   0        0        0      346 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/plus-circle.svg
--rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/plus-square.svg
--rw-rw-rw-   0        0        0      299 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/plus.svg
--rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/pocket.svg
--rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/power.svg
--rw-rw-rw-   0        0        0      402 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/printer.svg
--rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/radio.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/refresh-ccw.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/refresh-cw.svg
--rw-rw-rw-   0        0        0      387 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/repeat.svg
--rw-rw-rw-   0        0        0      314 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/rewind.svg
--rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/rotate-ccw.svg
--rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/rotate-cw.svg
--rw-rw-rw-   0        0        0      325 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/rss.svg
--rw-rw-rw-   0        0        0      387 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/save.svg
--rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/schedule.svg
--rw-rw-rw-   0        0        0      439 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/scissors.svg
--rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/search.svg
--rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/send.svg
--rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/server.svg
--rw-rw-rw-   0        0        0     1006 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/settings.svg
--rw-rw-rw-   0        0        0      440 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/share-2.svg
--rw-rw-rw-   0        0        0      359 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/share.svg
--rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/shield-off.svg
--rw-rw-rw-   0        0        0      274 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/shield.svg
--rw-rw-rw-   0        0        0      367 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/shopping-bag.svg
--rw-rw-rw-   0        0        0      378 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/shopping-cart.svg
--rw-rw-rw-   0        0        0      436 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/shuffle.svg
--rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/sidebar.svg
--rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/skip-back.svg
--rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/skip-forward.svg
--rw-rw-rw-   0        0        0      994 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/slack.svg
--rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/slash.svg
--rw-rw-rw-   0        0        0      606 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/sliders.svg
--rw-rw-rw-   0        0        0      327 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/smartphone.svg
--rw-rw-rw-   0        0        0      383 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/smile.svg
--rw-rw-rw-   0        0        0      361 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/speaker.svg
--rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/square.svg
--rw-rw-rw-   0        0        0      391 2023-04-06 21:10:35.000000 qcontext-1.0.7/src/qcontext/.assets/star-fill.svg
--rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/star.svg
--rw-rw-rw-   0        0        0      304 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/stop-circle.svg
--rw-rw-rw-   0        0        0      645 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/sun.svg
--rw-rw-rw-   0        0        0      584 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/sunrise.svg
--rw-rw-rw-   0        0        0      583 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/sunset.svg
--rw-rw-rw-   0        0        0      335 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/table.svg
--rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/tablet.svg
--rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/tag.svg
--rw-rw-rw-   0        0        0      331 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/target.svg
--rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/terminal.svg
--rw-rw-rw-   0        0        0      292 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/thermometer.svg
--rw-rw-rw-   0        0        0      369 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/thumbs-down.svg
--rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/thumbs-up.svg
--rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/toggle-left.svg
--rw-rw-rw-   0        0        0      320 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/toggle-right.svg
--rw-rw-rw-   0        0        0      381 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/tool.svg
--rw-rw-rw-   0        0        0      443 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/trash-2.svg
--rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/trash.svg
--rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/trello.svg
--rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/trending-down.svg
--rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/trending-up.svg
--rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/triangle.svg
--rw-rw-rw-   0        0        0      410 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/truck.svg
--rw-rw-rw-   0        0        0      315 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/tv.svg
--rw-rw-rw-   0        0        0      272 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/twitch.svg
--rw-rw-rw-   0        0        0      403 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/twitter.svg
--rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/type.svg
--rw-rw-rw-   0        0        0      285 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/umbrella.svg
--rw-rw-rw-   0        0        0      314 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/underline.svg
--rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/unlock.svg
--rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/upload-cloud.svg
--rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/upload.svg
--rw-rw-rw-   0        0        0      362 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/user-check.svg
--rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/user-minus.svg
--rw-rw-rw-   0        0        0      403 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/user-plus.svg
--rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/user-x.svg
--rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/user.svg
--rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/users.svg
--rw-rw-rw-   0        0        0      374 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/video-off.svg
--rw-rw-rw-   0        0        0      324 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/video.svg
--rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/voicemail.svg
--rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/volume-1.svg
--rw-rw-rw-   0        0        0      354 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/volume-2.svg
--rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/volume-x.svg
--rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/volume.svg
--rw-rw-rw-   0        0        0      457 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/watch.svg
--rw-rw-rw-   0        0        0      564 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/wifi-off.svg
--rw-rw-rw-   0        0        0      396 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/wifi.svg
--rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/wind.svg
--rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/x-circle-gray.svg
--rw-rw-rw-   0        0        0      341 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/x-circle.svg
--rw-rw-rw-   0        0        0      401 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/x-octagon.svg
--rw-rw-rw-   0        0        0      363 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/x-square.svg
--rw-rw-rw-   0        0        0      294 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/x.svg
--rw-rw-rw-   0        0        0      560 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/youtube.svg
--rw-rw-rw-   0        0        0      428 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/zap-off.svg
--rw-rw-rw-   0        0        0      277 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/zap.svg
--rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/zoom-in.svg
--rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.7/src/qcontext/.assets/zoom-out.svg
--rw-rw-rw-   0        0        0       62 2023-05-11 03:03:55.000000 qcontext-1.0.7/src/qcontext/__init__.py
--rw-rw-rw-   0        0        0      426 2023-05-09 13:48:36.000000 qcontext-1.0.7/src/qcontext/contextapi.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.257561 qcontext-1.0.7/src/qcontext/misc/
--rw-rw-rw-   0        0        0      217 2023-05-02 22:09:11.000000 qcontext-1.0.7/src/qcontext/misc/__init__.py
--rw-rw-rw-   0        0        0     1865 2023-05-12 03:11:10.000000 qcontext-1.0.7/src/qcontext/misc/aiorequest.py
--rw-rw-rw-   0        0        0     1062 2023-05-02 22:09:01.000000 qcontext-1.0.7/src/qcontext/misc/conditional_thread_queue.py
--rw-rw-rw-   0        0        0     3533 2023-05-11 07:05:58.000000 qcontext-1.0.7/src/qcontext/misc/icon.py
--rw-rw-rw-   0        0        0      274 2023-04-20 15:54:13.000000 qcontext-1.0.7/src/qcontext/misc/size.py
--rw-rw-rw-   0        0        0     2181 2023-05-09 19:37:01.000000 qcontext-1.0.7/src/qcontext/misc/stylesheet_parser.py
--rw-rw-rw-   0        0        0      959 2023-05-11 02:43:57.000000 qcontext-1.0.7/src/qcontext/misc/utils.py
--rw-rw-rw-   0        0        0      509 2023-05-11 00:19:53.000000 qcontext-1.0.7/src/qcontext/misc/uvicorn_threaded_server.py
--rw-rw-rw-   0        0        0      884 2023-05-11 03:44:11.000000 qcontext-1.0.7/src/qcontext/qasyncio.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.270561 qcontext-1.0.7/src/qcontext/widgets/
--rw-rw-rw-   0        0        0      541 2023-05-11 05:20:54.000000 qcontext-1.0.7/src/qcontext/widgets/__init__.py
--rw-rw-rw-   0        0        0     1141 2023-05-11 02:59:52.000000 qcontext-1.0.7/src/qcontext/widgets/button.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.276560 qcontext-1.0.7/src/qcontext/widgets/custom/
--rw-rw-rw-   0        0        0      279 2023-05-02 20:21:51.000000 qcontext-1.0.7/src/qcontext/widgets/custom/__init__.py
--rw-rw-rw-   0        0        0     5580 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/custom/date_picker.py
--rw-rw-rw-   0        0        0     1930 2023-05-11 03:02:05.000000 qcontext-1.0.7/src/qcontext/widgets/custom/error_label.py
--rw-rw-rw-   0        0        0     2018 2023-05-11 04:47:21.000000 qcontext-1.0.7/src/qcontext/widgets/custom/favourite_button.py
--rw-rw-rw-   0        0        0     2676 2023-05-11 03:02:25.000000 qcontext-1.0.7/src/qcontext/widgets/custom/image_button.py
--rw-rw-rw-   0        0        0     1319 2023-05-11 03:03:19.000000 qcontext-1.0.7/src/qcontext/widgets/custom/label_extended.py
--rw-rw-rw-   0        0        0     1460 2023-05-11 03:03:19.000000 qcontext-1.0.7/src/qcontext/widgets/custom/menu_button.py
--rw-rw-rw-   0        0        0     1004 2023-05-11 03:03:19.000000 qcontext-1.0.7/src/qcontext/widgets/custom/search_bar.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.284561 qcontext-1.0.7/src/qcontext/widgets/extensions/
--rw-rw-rw-   0        0        0      298 2023-05-11 03:10:19.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/__init__.py
--rw-rw-rw-   0        0        0      652 2023-05-11 03:08:55.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/alignment_ext.py
--rw-rw-rw-   0        0        0     2130 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/context_object_ext.py
--rw-rw-rw-   0        0        0     1895 2023-05-10 02:24:48.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/layout_ext.py
--rw-rw-rw-   0        0        0      116 2023-05-11 03:10:19.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/orientation_ext.py
--rw-rw-rw-   0        0        0      225 2023-05-11 03:09:33.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/policy_ext.py
--rw-rw-rw-   0        0        0      674 2023-04-20 15:21:35.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/side_menu_ext.py
--rw-rw-rw-   0        0        0     1897 2023-04-27 03:54:17.000000 qcontext-1.0.7/src/qcontext/widgets/extensions/splitter_widget_ext.py
--rw-rw-rw-   0        0        0      778 2023-05-11 03:00:02.000000 qcontext-1.0.7/src/qcontext/widgets/frame.py
--rw-rw-rw-   0        0        0     1701 2023-05-11 03:11:47.000000 qcontext-1.0.7/src/qcontext/widgets/label.py
--rw-rw-rw-   0        0        0     1305 2023-05-11 03:10:28.000000 qcontext-1.0.7/src/qcontext/widgets/layout.py
--rw-rw-rw-   0        0        0     1118 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/line_input.py
--rw-rw-rw-   0        0        0     3945 2023-05-10 23:37:34.000000 qcontext-1.0.7/src/qcontext/widgets/popup.py
--rw-rw-rw-   0        0        0     1687 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/scroll_area.py
--rw-rw-rw-   0        0        0     1328 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/selector.py
--rw-rw-rw-   0        0        0      369 2023-04-08 19:53:22.000000 qcontext-1.0.7/src/qcontext/widgets/spacer.py
--rw-rw-rw-   0        0        0     1741 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/splitter.py
--rw-rw-rw-   0        0        0     1062 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/stacked_widget.py
--rw-rw-rw-   0        0        0      392 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/statusbar.py
--rw-rw-rw-   0        0        0      779 2023-05-11 03:01:38.000000 qcontext-1.0.7/src/qcontext/widgets/text_input.py
--rw-rw-rw-   0        0        0      675 2023-05-11 02:59:52.000000 qcontext-1.0.7/src/qcontext/widgets/widget.py
--rw-rw-rw-   0        0        0      335 2023-05-10 00:56:17.000000 qcontext-1.0.7/src/qcontext/widgets/window.py
-drwxrwxrwx   0        0        0        0 2023-05-12 03:11:51.005583 qcontext-1.0.7/src/qcontext.egg-info/
--rw-rw-rw-   0        0        0     2788 2023-05-12 03:11:50.000000 qcontext-1.0.7/src/qcontext.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0    11822 2023-05-12 03:11:50.000000 qcontext-1.0.7/src/qcontext.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-12 03:11:50.000000 qcontext-1.0.7/src/qcontext.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       65 2023-05-12 03:11:50.000000 qcontext-1.0.7/src/qcontext.egg-info/requires.txt
--rw-rw-rw-   0        0        0       18 2023-05-12 03:11:50.000000 qcontext-1.0.7/src/qcontext.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.324772 qcontext-1.0.8/
+-rw-rw-rw-   0        0        0     1093 2023-02-26 16:41:50.000000 qcontext-1.0.8/LICENSE.txt
+-rw-rw-rw-   0        0        0     2788 2023-05-13 19:41:19.324772 qcontext-1.0.8/PKG-INFO
+-rw-rw-rw-   0        0        0      545 2023-05-11 02:27:47.000000 qcontext-1.0.8/README.md
+-rw-rw-rw-   0        0        0     1577 2023-05-13 19:41:02.000000 qcontext-1.0.8/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 19:41:19.325771 qcontext-1.0.8/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:17.295608 qcontext-1.0.8/src/
+-rw-rw-rw-   0        0        0        0 2023-03-20 19:19:08.000000 qcontext-1.0.8/src/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:17.313609 qcontext-1.0.8/src/qcontext/
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.070772 qcontext-1.0.8/src/qcontext/.assets/
+-rw-rw-rw-   0        0        0      277 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/activity.svg
+-rw-rw-rw-   0        0        0      357 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/airplay.svg
+-rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/alert-circle.svg
+-rw-rw-rw-   0        0        0      411 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/alert-octagon.svg
+-rw-rw-rw-   0        0        0      419 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/alert-triangle.svg
+-rw-rw-rw-   0        0        0      393 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/align-center.svg
+-rw-rw-rw-   0        0        0      394 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/align-justify.svg
+-rw-rw-rw-   0        0        0      391 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/align-left.svg
+-rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/align-right.svg
+-rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/anchor.svg
+-rw-rw-rw-   0        0        0      563 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/aperture.svg
+-rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/archive.svg
+-rw-rw-rw-   0        0        0      355 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-down-circle.svg
+-rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-down-left.svg
+-rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-down-right.svg
+-rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-down.svg
+-rw-rw-rw-   0        0        0      354 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-left-circle.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-left.svg
+-rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-right-circle.svg
+-rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-right.svg
+-rw-rw-rw-   0        0        0      352 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-up-circle.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-up-left.svg
+-rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-up-right.svg
+-rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/arrow-up.svg
+-rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/at-sign.svg
+-rw-rw-rw-   0        0        0      320 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/award.svg
+-rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bar-chart-2.svg
+-rw-rw-rw-   0        0        0      348 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bar-chart.svg
+-rw-rw-rw-   0        0        0      422 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/battery-charging.svg
+-rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/battery.svg
+-rw-rw-rw-   0        0        0      455 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bell-off.svg
+-rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bell.svg
+-rw-rw-rw-   0        0        0      293 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bluetooth.svg
+-rw-rw-rw-   0        0        0      322 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bold.svg
+-rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/book-open.svg
+-rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/book.svg
+-rw-rw-rw-   0        0        0      282 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/bookmark.svg
+-rw-rw-rw-   0        0        0      457 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/box.svg
+-rw-rw-rw-   0        0        0      338 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/briefcase.svg
+-rw-rw-rw-   0        0        0      405 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/calendar.svg
+-rw-rw-rw-   0        0        0      380 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/camera-off.svg
+-rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/camera.svg
+-rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cast.svg
+-rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/check-circle.svg
+-rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/check-square.svg
+-rw-rw-rw-   0        0        0      257 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/check.svg
+-rw-rw-rw-   0        0        0      264 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevron-down.svg
+-rw-rw-rw-   0        0        0      265 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevron-left.svg
+-rw-rw-rw-   0        0        0      265 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevron-right.svg
+-rw-rw-rw-   0        0        0      263 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevron-up.svg
+-rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevrons-down.svg
+-rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevrons-left.svg
+-rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevrons-right.svg
+-rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chevrons-up.svg
+-rw-rw-rw-   0        0        0      443 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/chrome.svg
+-rw-rw-rw-   0        0        0      253 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/circle.svg
+-rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/clipboard.svg
+-rw-rw-rw-   0        0        0      299 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/clock.svg
+-rw-rw-rw-   0        0        0      552 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud-drizzle.svg
+-rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud-lightning.svg
+-rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud-off.svg
+-rw-rw-rw-   0        0        0      416 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud-rain.svg
+-rw-rw-rw-   0        0        0      567 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud-snow.svg
+-rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cloud.svg
+-rw-rw-rw-   0        0        0      302 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/code.svg
+-rw-rw-rw-   0        0        0      481 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/codepen.svg
+-rw-rw-rw-   0        0        0      633 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/codesandbox.svg
+-rw-rw-rw-   0        0        0      442 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/coffee.svg
+-rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/columns.svg
+-rw-rw-rw-   0        0        0      416 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/command.svg
+-rw-rw-rw-   0        0        0      337 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/compass.svg
+-rw-rw-rw-   0        0        0      346 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/copy.svg
+-rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-down-left.svg
+-rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-down-right.svg
+-rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-left-down.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-left-up.svg
+-rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-right-down.svg
+-rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-right-up.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-up-left.svg
+-rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/corner-up-right.svg
+-rw-rw-rw-   0        0        0      662 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/cpu.svg
+-rw-rw-rw-   0        0        0      324 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/credit-card.svg
+-rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/crop.svg
+-rw-rw-rw-   0        0        0      432 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/crosshair.svg
+-rw-rw-rw-   0        0        0      367 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/database.svg
+-rw-rw-rw-   0        0        0      369 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/delete.svg
+-rw-rw-rw-   0        0        0      290 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/disc.svg
+-rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/divide-circle.svg
+-rw-rw-rw-   0        0        0      414 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/divide-square.svg
+-rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/divide.svg
+-rw-rw-rw-   0        0        0      329 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/dollar-sign.svg
+-rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/download-cloud.svg
+-rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/download.svg
+-rw-rw-rw-   0        0        0      419 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/dribbble.svg
+-rw-rw-rw-   0        0        0      269 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/droplet.svg
+-rw-rw-rw-   0        0        0      286 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/edit-2.svg
+-rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/edit-3.svg
+-rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/edit.svg
+-rw-rw-rw-   0        0        0      383 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/external-link.svg
+-rw-rw-rw-   0        0        0      455 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/eye-off.svg
+-rw-rw-rw-   0        0        0      311 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/eye.svg
+-rw-rw-rw-   0        0        0      298 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/facebook.svg
+-rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/fast-forward.svg
+-rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/feather.svg
+-rw-rw-rw-   0        0        0      548 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/figma.svg
+-rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/file-minus.svg
+-rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/file-plus.svg
+-rw-rw-rw-   0        0        0      468 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/file-text.svg
+-rw-rw-rw-   0        0        0      332 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/file.svg
+-rw-rw-rw-   0        0        0      581 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/film.svg
+-rw-rw-rw-   0        0        0      285 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/filter.svg
+-rw-rw-rw-   0        0        0      329 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/flag.svg
+-rw-rw-rw-   0        0        0      356 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/folder-minus.svg
+-rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/folder-plus.svg
+-rw-rw-rw-   0        0        0      306 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/folder.svg
+-rw-rw-rw-   0        0        0      273 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/framer.svg
+-rw-rw-rw-   0        0        0      385 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/frown.svg
+-rw-rw-rw-   0        0        0      476 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/gift.svg
+-rw-rw-rw-   0        0        0      372 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/git-branch.svg
+-rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/git-commit.svg
+-rw-rw-rw-   0        0        0      331 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/git-merge.svg
+-rw-rw-rw-   0        0        0      382 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/git-pull-request.svg
+-rw-rw-rw-   0        0        0      522 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/github.svg
+-rw-rw-rw-   0        0        0      485 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/gitlab.svg
+-rw-rw-rw-   0        0        0      404 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/globe.svg
+-rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/grid.svg
+-rw-rw-rw-   0        0        0      479 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/hard-drive.svg
+-rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/hash.svg
+-rw-rw-rw-   0        0        0      390 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/headphones.svg
+-rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/heart.svg
+-rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/help-circle.svg
+-rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/hexagon.svg
+-rw-rw-rw-   0        0        0      327 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/home.svg
+-rw-rw-rw-   0        0        0      364 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/image.svg
+-rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/inbox.svg
+-rw-rw-rw-   0        0        0      342 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/info.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/instagram.svg
+-rw-rw-rw-   0        0        0      343 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/italic.svg
+-rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/key.svg
+-rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/layers.svg
+-rw-rw-rw-   0        0        0      359 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/layout.svg
+-rw-rw-rw-   0        0        0      570 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/life-buoy.svg
+-rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/link-2.svg
+-rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/link.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/linkedin.svg
+-rw-rw-rw-   0        0        0      477 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/list.svg
+-rw-rw-rw-   0        0        0      609 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/loader.svg
+-rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/lock.svg
+-rw-rw-rw-   0        0        0      363 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/log-in.svg
+-rw-rw-rw-   0        0        0      362 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/log-out.svg
+-rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/mail.svg
+-rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/map-pin.svg
+-rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/map.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/maximize-2.svg
+-rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/maximize.svg
+-rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/meh.svg
+-rw-rw-rw-   0        0        0      341 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/menu.svg
+-rw-rw-rw-   0        0        0      423 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/message-circle.svg
+-rw-rw-rw-   0        0        0      300 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/message-square.svg
+-rw-rw-rw-   0        0        0      489 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/mic-off.svg
+-rw-rw-rw-   0        0        0      413 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/mic.svg
+-rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/minimize-2.svg
+-rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/minimize.svg
+-rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/minus-circle.svg
+-rw-rw-rw-   0        0        0      325 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/minus-square.svg
+-rw-rw-rw-   0        0        0      256 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/minus.svg
+-rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/monitor.svg
+-rw-rw-rw-   0        0        0      276 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/moon.svg
+-rw-rw-rw-   0        0        0      338 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/more-horizontal.svg
+-rw-rw-rw-   0        0        0      336 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/more-vertical.svg
+-rw-rw-rw-   0        0        0      306 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/mouse-pointer.svg
+-rw-rw-rw-   0        0        0      481 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/move.svg
+-rw-rw-rw-   0        0        0      322 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/music.svg
+-rw-rw-rw-   0        0        0      274 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/navigation-2.svg
+-rw-rw-rw-   0        0        0      272 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/navigation.svg
+-rw-rw-rw-   0        0        0      313 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/octagon.svg
+-rw-rw-rw-   0        0        0      512 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/package.svg
+-rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/paperclip.svg
+-rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/pause-circle.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/pause.svg
+-rw-rw-rw-   0        0        0      386 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/pen-tool.svg
+-rw-rw-rw-   0        0        0      345 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/percent.svg
+-rw-rw-rw-   0        0        0      571 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-call.svg
+-rw-rw-rw-   0        0        0      613 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-forwarded.svg
+-rw-rw-rw-   0        0        0      612 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-incoming.svg
+-rw-rw-rw-   0        0        0      608 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-missed.svg
+-rw-rw-rw-   0        0        0      586 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-off.svg
+-rw-rw-rw-   0        0        0      612 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone-outgoing.svg
+-rw-rw-rw-   0        0        0      515 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/phone.svg
+-rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/pie-chart.svg
+-rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/play-circle.svg
+-rw-rw-rw-   0        0        0      258 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/play.svg
+-rw-rw-rw-   0        0        0      345 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/plus-circle-gray.svg
+-rw-rw-rw-   0        0        0      346 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/plus-circle.svg
+-rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/plus-square.svg
+-rw-rw-rw-   0        0        0      299 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/plus.svg
+-rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/pocket.svg
+-rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/power.svg
+-rw-rw-rw-   0        0        0      402 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/printer.svg
+-rw-rw-rw-   0        0        0      384 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/radio.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/refresh-ccw.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/refresh-cw.svg
+-rw-rw-rw-   0        0        0      387 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/repeat.svg
+-rw-rw-rw-   0        0        0      314 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/rewind.svg
+-rw-rw-rw-   0        0        0      312 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/rotate-ccw.svg
+-rw-rw-rw-   0        0        0      316 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/rotate-cw.svg
+-rw-rw-rw-   0        0        0      325 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/rss.svg
+-rw-rw-rw-   0        0        0      387 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/save.svg
+-rw-rw-rw-   0        0        0      366 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/schedule.svg
+-rw-rw-rw-   0        0        0      439 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/scissors.svg
+-rw-rw-rw-   0        0        0      303 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/search.svg
+-rw-rw-rw-   0        0        0      309 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/send.svg
+-rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/server.svg
+-rw-rw-rw-   0        0        0     1006 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/settings.svg
+-rw-rw-rw-   0        0        0      440 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/share-2.svg
+-rw-rw-rw-   0        0        0      359 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/share.svg
+-rw-rw-rw-   0        0        0      400 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/shield-off.svg
+-rw-rw-rw-   0        0        0      274 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/shield.svg
+-rw-rw-rw-   0        0        0      367 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/shopping-bag.svg
+-rw-rw-rw-   0        0        0      378 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/shopping-cart.svg
+-rw-rw-rw-   0        0        0      436 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/shuffle.svg
+-rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/sidebar.svg
+-rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/skip-back.svg
+-rw-rw-rw-   0        0        0      310 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/skip-forward.svg
+-rw-rw-rw-   0        0        0      994 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/slack.svg
+-rw-rw-rw-   0        0        0      307 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/slash.svg
+-rw-rw-rw-   0        0        0      606 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/sliders.svg
+-rw-rw-rw-   0        0        0      327 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/smartphone.svg
+-rw-rw-rw-   0        0        0      383 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/smile.svg
+-rw-rw-rw-   0        0        0      361 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/speaker.svg
+-rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/square.svg
+-rw-rw-rw-   0        0        0      391 2023-04-06 21:10:35.000000 qcontext-1.0.8/src/qcontext/.assets/star-fill.svg
+-rw-rw-rw-   0        0        0      334 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/star.svg
+-rw-rw-rw-   0        0        0      304 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/stop-circle.svg
+-rw-rw-rw-   0        0        0      645 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/sun.svg
+-rw-rw-rw-   0        0        0      584 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/sunrise.svg
+-rw-rw-rw-   0        0        0      583 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/sunset.svg
+-rw-rw-rw-   0        0        0      335 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/table.svg
+-rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/tablet.svg
+-rw-rw-rw-   0        0        0      350 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/tag.svg
+-rw-rw-rw-   0        0        0      331 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/target.svg
+-rw-rw-rw-   0        0        0      305 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/terminal.svg
+-rw-rw-rw-   0        0        0      292 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/thermometer.svg
+-rw-rw-rw-   0        0        0      369 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/thumbs-down.svg
+-rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/thumbs-up.svg
+-rw-rw-rw-   0        0        0      318 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/toggle-left.svg
+-rw-rw-rw-   0        0        0      320 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/toggle-right.svg
+-rw-rw-rw-   0        0        0      381 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/tool.svg
+-rw-rw-rw-   0        0        0      443 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/trash-2.svg
+-rw-rw-rw-   0        0        0      351 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/trash.svg
+-rw-rw-rw-   0        0        0      368 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/trello.svg
+-rw-rw-rw-   0        0        0      326 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/trending-down.svg
+-rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/trending-up.svg
+-rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/triangle.svg
+-rw-rw-rw-   0        0        0      410 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/truck.svg
+-rw-rw-rw-   0        0        0      315 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/tv.svg
+-rw-rw-rw-   0        0        0      272 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/twitch.svg
+-rw-rw-rw-   0        0        0      403 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/twitter.svg
+-rw-rw-rw-   0        0        0      347 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/type.svg
+-rw-rw-rw-   0        0        0      285 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/umbrella.svg
+-rw-rw-rw-   0        0        0      314 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/underline.svg
+-rw-rw-rw-   0        0        0      317 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/unlock.svg
+-rw-rw-rw-   0        0        0      426 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/upload-cloud.svg
+-rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/upload.svg
+-rw-rw-rw-   0        0        0      362 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/user-check.svg
+-rw-rw-rw-   0        0        0      360 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/user-minus.svg
+-rw-rw-rw-   0        0        0      403 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/user-plus.svg
+-rw-rw-rw-   0        0        0      399 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/user-x.svg
+-rw-rw-rw-   0        0        0      308 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/user.svg
+-rw-rw-rw-   0        0        0      395 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/users.svg
+-rw-rw-rw-   0        0        0      374 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/video-off.svg
+-rw-rw-rw-   0        0        0      324 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/video.svg
+-rw-rw-rw-   0        0        0      353 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/voicemail.svg
+-rw-rw-rw-   0        0        0      323 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/volume-1.svg
+-rw-rw-rw-   0        0        0      354 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/volume-2.svg
+-rw-rw-rw-   0        0        0      365 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/volume-x.svg
+-rw-rw-rw-   0        0        0      275 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/volume.svg
+-rw-rw-rw-   0        0        0      457 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/watch.svg
+-rw-rw-rw-   0        0        0      564 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/wifi-off.svg
+-rw-rw-rw-   0        0        0      396 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/wifi.svg
+-rw-rw-rw-   0        0        0      321 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/wind.svg
+-rw-rw-rw-   0        0        0      340 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/x-circle-gray.svg
+-rw-rw-rw-   0        0        0      341 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/x-circle.svg
+-rw-rw-rw-   0        0        0      401 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/x-octagon.svg
+-rw-rw-rw-   0        0        0      363 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/x-square.svg
+-rw-rw-rw-   0        0        0      294 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/x.svg
+-rw-rw-rw-   0        0        0      560 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/youtube.svg
+-rw-rw-rw-   0        0        0      428 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/zap-off.svg
+-rw-rw-rw-   0        0        0      277 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/zap.svg
+-rw-rw-rw-   0        0        0      392 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/zoom-in.svg
+-rw-rw-rw-   0        0        0      349 2023-03-18 18:50:21.000000 qcontext-1.0.8/src/qcontext/.assets/zoom-out.svg
+-rw-rw-rw-   0        0        0       62 2023-05-11 03:03:55.000000 qcontext-1.0.8/src/qcontext/__init__.py
+-rw-rw-rw-   0        0        0      426 2023-05-09 13:48:36.000000 qcontext-1.0.8/src/qcontext/contextapi.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.125772 qcontext-1.0.8/src/qcontext/misc/
+-rw-rw-rw-   0        0        0      217 2023-05-02 22:09:11.000000 qcontext-1.0.8/src/qcontext/misc/__init__.py
+-rw-rw-rw-   0        0        0     1931 2023-05-12 16:41:32.000000 qcontext-1.0.8/src/qcontext/misc/aiorequest.py
+-rw-rw-rw-   0        0        0     1062 2023-05-02 22:09:01.000000 qcontext-1.0.8/src/qcontext/misc/conditional_thread_queue.py
+-rw-rw-rw-   0        0        0     3533 2023-05-11 07:05:58.000000 qcontext-1.0.8/src/qcontext/misc/icon.py
+-rw-rw-rw-   0        0        0      274 2023-04-20 15:54:13.000000 qcontext-1.0.8/src/qcontext/misc/size.py
+-rw-rw-rw-   0        0        0     2181 2023-05-09 19:37:01.000000 qcontext-1.0.8/src/qcontext/misc/stylesheet_parser.py
+-rw-rw-rw-   0        0        0      959 2023-05-11 02:43:57.000000 qcontext-1.0.8/src/qcontext/misc/utils.py
+-rw-rw-rw-   0        0        0      642 2023-05-13 19:40:41.000000 qcontext-1.0.8/src/qcontext/misc/uvicorn_threaded_server.py
+-rw-rw-rw-   0        0        0      884 2023-05-11 03:44:11.000000 qcontext-1.0.8/src/qcontext/qasyncio.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.231807 qcontext-1.0.8/src/qcontext/widgets/
+-rw-rw-rw-   0        0        0      569 2023-05-13 19:40:41.000000 qcontext-1.0.8/src/qcontext/widgets/__init__.py
+-rw-rw-rw-   0        0        0     1141 2023-05-11 02:59:52.000000 qcontext-1.0.8/src/qcontext/widgets/button.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.277773 qcontext-1.0.8/src/qcontext/widgets/custom/
+-rw-rw-rw-   0        0        0      279 2023-05-02 20:21:51.000000 qcontext-1.0.8/src/qcontext/widgets/custom/__init__.py
+-rw-rw-rw-   0        0        0     5580 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/custom/date_picker.py
+-rw-rw-rw-   0        0        0     1930 2023-05-11 03:02:05.000000 qcontext-1.0.8/src/qcontext/widgets/custom/error_label.py
+-rw-rw-rw-   0        0        0     2018 2023-05-11 04:47:21.000000 qcontext-1.0.8/src/qcontext/widgets/custom/favourite_button.py
+-rw-rw-rw-   0        0        0     2676 2023-05-11 03:02:25.000000 qcontext-1.0.8/src/qcontext/widgets/custom/image_button.py
+-rw-rw-rw-   0        0        0     1319 2023-05-11 03:03:19.000000 qcontext-1.0.8/src/qcontext/widgets/custom/label_extended.py
+-rw-rw-rw-   0        0        0     1460 2023-05-11 03:03:19.000000 qcontext-1.0.8/src/qcontext/widgets/custom/menu_button.py
+-rw-rw-rw-   0        0        0     1004 2023-05-11 03:03:19.000000 qcontext-1.0.8/src/qcontext/widgets/custom/search_bar.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:19.323772 qcontext-1.0.8/src/qcontext/widgets/extensions/
+-rw-rw-rw-   0        0        0      298 2023-05-11 03:10:19.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/__init__.py
+-rw-rw-rw-   0        0        0      652 2023-05-11 03:08:55.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/alignment_ext.py
+-rw-rw-rw-   0        0        0     2130 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/context_object_ext.py
+-rw-rw-rw-   0        0        0     1895 2023-05-10 02:24:48.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/layout_ext.py
+-rw-rw-rw-   0        0        0      150 2023-05-13 09:08:57.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/orientation_ext.py
+-rw-rw-rw-   0        0        0      225 2023-05-11 03:09:33.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/policy_ext.py
+-rw-rw-rw-   0        0        0      674 2023-04-20 15:21:35.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/side_menu_ext.py
+-rw-rw-rw-   0        0        0     1897 2023-04-27 03:54:17.000000 qcontext-1.0.8/src/qcontext/widgets/extensions/splitter_widget_ext.py
+-rw-rw-rw-   0        0        0      778 2023-05-11 03:00:02.000000 qcontext-1.0.8/src/qcontext/widgets/frame.py
+-rw-rw-rw-   0        0        0     1701 2023-05-11 03:11:47.000000 qcontext-1.0.8/src/qcontext/widgets/label.py
+-rw-rw-rw-   0        0        0     1305 2023-05-11 03:10:28.000000 qcontext-1.0.8/src/qcontext/widgets/layout.py
+-rw-rw-rw-   0        0        0     1118 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/line_input.py
+-rw-rw-rw-   0        0        0     3945 2023-05-10 23:37:34.000000 qcontext-1.0.8/src/qcontext/widgets/popup.py
+-rw-rw-rw-   0        0        0     1687 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/scroll_area.py
+-rw-rw-rw-   0        0        0     1328 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/selector.py
+-rw-rw-rw-   0        0        0      925 2023-05-13 19:40:16.000000 qcontext-1.0.8/src/qcontext/widgets/slider.py
+-rw-rw-rw-   0        0        0      369 2023-04-08 19:53:22.000000 qcontext-1.0.8/src/qcontext/widgets/spacer.py
+-rw-rw-rw-   0        0        0     1741 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/splitter.py
+-rw-rw-rw-   0        0        0     1062 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/stacked_widget.py
+-rw-rw-rw-   0        0        0      392 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/statusbar.py
+-rw-rw-rw-   0        0        0      779 2023-05-11 03:01:38.000000 qcontext-1.0.8/src/qcontext/widgets/text_input.py
+-rw-rw-rw-   0        0        0      675 2023-05-11 02:59:52.000000 qcontext-1.0.8/src/qcontext/widgets/widget.py
+-rw-rw-rw-   0        0        0      335 2023-05-10 00:56:17.000000 qcontext-1.0.8/src/qcontext/widgets/window.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:41:17.336609 qcontext-1.0.8/src/qcontext.egg-info/
+-rw-rw-rw-   0        0        0     2788 2023-05-13 19:41:17.000000 qcontext-1.0.8/src/qcontext.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0    11853 2023-05-13 19:41:17.000000 qcontext-1.0.8/src/qcontext.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:41:17.000000 qcontext-1.0.8/src/qcontext.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       65 2023-05-13 19:41:17.000000 qcontext-1.0.8/src/qcontext.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       18 2023-05-13 19:41:17.000000 qcontext-1.0.8/src/qcontext.egg-info/top_level.txt
```

### Comparing `qcontext-1.0.7/LICENSE.txt` & `qcontext-1.0.8/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/PKG-INFO` & `qcontext-1.0.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: qcontext
-Version: 1.0.7
+Version: 1.0.8
 Summary: One of the most controversial things
 Author-email: cxllmerichie <cxllmerichie@gmail.com>
 Maintainer-email: cxllmerichie <cxllmerichie@gmail.com>
 License: MIT License
         
         Copyright (c) 2022-2023 cxllmerichie
```

### Comparing `qcontext-1.0.7/README.md` & `qcontext-1.0.8/README.md`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/pyproject.toml` & `qcontext-1.0.8/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=63.2"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "qcontext"
-version = "1.0.7"
+version = "1.0.8"
 authors = [
     { name="cxllmerichie", email="cxllmerichie@gmail.com" },
 ]
 maintainers = [
     { name="cxllmerichie", email="cxllmerichie@gmail.com" },
 ]
 description = "One of the most controversial things"
```

### Comparing `qcontext-1.0.7/src/qcontext/.assets/aperture.svg` & `qcontext-1.0.8/src/qcontext/.assets/aperture.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/cloud-drizzle.svg` & `qcontext-1.0.8/src/qcontext/.assets/cloud-drizzle.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/cloud-snow.svg` & `qcontext-1.0.8/src/qcontext/.assets/cloud-snow.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/codesandbox.svg` & `qcontext-1.0.8/src/qcontext/.assets/codesandbox.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/cpu.svg` & `qcontext-1.0.8/src/qcontext/.assets/cpu.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/figma.svg` & `qcontext-1.0.8/src/qcontext/.assets/figma.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/film.svg` & `qcontext-1.0.8/src/qcontext/.assets/film.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/github.svg` & `qcontext-1.0.8/src/qcontext/.assets/github.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/life-buoy.svg` & `qcontext-1.0.8/src/qcontext/.assets/life-buoy.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/loader.svg` & `qcontext-1.0.8/src/qcontext/.assets/loader.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/package.svg` & `qcontext-1.0.8/src/qcontext/.assets/package.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-call.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-call.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-forwarded.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-forwarded.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-incoming.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-incoming.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-missed.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-missed.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-off.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-off.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone-outgoing.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone-outgoing.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/phone.svg` & `qcontext-1.0.8/src/qcontext/.assets/phone.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/settings.svg` & `qcontext-1.0.8/src/qcontext/.assets/settings.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/slack.svg` & `qcontext-1.0.8/src/qcontext/.assets/slack.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/sliders.svg` & `qcontext-1.0.8/src/qcontext/.assets/sliders.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/sun.svg` & `qcontext-1.0.8/src/qcontext/.assets/sun.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/sunrise.svg` & `qcontext-1.0.8/src/qcontext/.assets/sunrise.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/sunset.svg` & `qcontext-1.0.8/src/qcontext/.assets/sunset.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/wifi-off.svg` & `qcontext-1.0.8/src/qcontext/.assets/wifi-off.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/.assets/youtube.svg` & `qcontext-1.0.8/src/qcontext/.assets/youtube.svg`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/misc/aiorequest.py` & `qcontext-1.0.8/src/qcontext/misc/aiorequest.py`

 * *Files 6% similar despite different names*

```diff
@@ -21,27 +21,29 @@
         self.__base_url = base_url
 
     async def __call__(
             self,
             method: str, url: str,
             *,
             params: dict[str, Any] = None, body: dict[str, Any] = None, headers: dict[str, Any] = None,
-            data: dict[str, Any] = None
+            data: dict[str, Any] = None,
+            nobase: bool = False
     ) -> Any:
         assert (method := method.lower()) in ('get', 'post', 'put', 'delete')
         async with aiohttp.ClientSession(json_serialize=ujson.dumps) as session:
             # convert params values to str
             for key, value in params.items() if params else {}:
                 params[key] = str(value)
-            request_method = getattr(session, method)
-            async with request_method(await self.__url(url), json=body, params=params, headers=headers, data=data) as response:
+            async with getattr(session, method)(
+                    await self.__url(url, nobase), json=body, params=params, headers=headers, data=data
+            ) as response:
                 return await response.json()
 
-    async def __url(self, url: str):
-        if not (base := await self.base_url):
+    async def __url(self, url: str, nobase: bool = False):
+        if not (base := await self.base_url) or nobase:
             return url
         if base.endswith('/') and url.startswith('/'):
             return base[:-1] + url
         elif base.endswith('/') and not url.startswith('/'):
             return base + url
         elif not base.endswith('/') and url.startswith('/'):
             return base + url
```

### Comparing `qcontext-1.0.7/src/qcontext/misc/conditional_thread_queue.py` & `qcontext-1.0.8/src/qcontext/misc/conditional_thread_queue.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/misc/icon.py` & `qcontext-1.0.8/src/qcontext/misc/icon.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/misc/stylesheet_parser.py` & `qcontext-1.0.8/src/qcontext/misc/stylesheet_parser.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/misc/utils.py` & `qcontext-1.0.8/src/qcontext/misc/utils.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/qasyncio.py` & `qcontext-1.0.8/src/qcontext/qasyncio.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/__init__.py` & `qcontext-1.0.8/src/qcontext/widgets/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -8,12 +8,13 @@
 from .label import Label
 from .line_input import LineInput
 from .text_input import TextInput
 from .selector import Selector
 from .popup import Popup
 from .statusbar import StatusBar
 from .window import Window
+from .slider import Slider
 
 from .layout import Layout
 from .spacer import Spacer
 
 from PyQt5.QtWidgets import QWidget
```

### Comparing `qcontext-1.0.7/src/qcontext/widgets/button.py` & `qcontext-1.0.8/src/qcontext/widgets/button.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/date_picker.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/date_picker.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/error_label.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/error_label.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/favourite_button.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/favourite_button.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/image_button.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/image_button.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/label_extended.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/label_extended.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/menu_button.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/menu_button.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/custom/search_bar.py` & `qcontext-1.0.8/src/qcontext/widgets/custom/search_bar.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/extensions/alignment_ext.py` & `qcontext-1.0.8/src/qcontext/widgets/extensions/alignment_ext.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/extensions/context_object_ext.py` & `qcontext-1.0.8/src/qcontext/widgets/extensions/context_object_ext.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/extensions/layout_ext.py` & `qcontext-1.0.8/src/qcontext/widgets/extensions/layout_ext.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/extensions/side_menu_ext.py` & `qcontext-1.0.8/src/qcontext/widgets/extensions/side_menu_ext.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/extensions/splitter_widget_ext.py` & `qcontext-1.0.8/src/qcontext/widgets/extensions/splitter_widget_ext.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/frame.py` & `qcontext-1.0.8/src/qcontext/widgets/frame.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/label.py` & `qcontext-1.0.8/src/qcontext/widgets/label.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/layout.py` & `qcontext-1.0.8/src/qcontext/widgets/layout.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/line_input.py` & `qcontext-1.0.8/src/qcontext/widgets/line_input.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/popup.py` & `qcontext-1.0.8/src/qcontext/widgets/popup.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/scroll_area.py` & `qcontext-1.0.8/src/qcontext/widgets/scroll_area.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/selector.py` & `qcontext-1.0.8/src/qcontext/widgets/selector.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/splitter.py` & `qcontext-1.0.8/src/qcontext/widgets/splitter.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/stacked_widget.py` & `qcontext-1.0.8/src/qcontext/widgets/stacked_widget.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/text_input.py` & `qcontext-1.0.8/src/qcontext/widgets/text_input.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext/widgets/widget.py` & `qcontext-1.0.8/src/qcontext/widgets/widget.py`

 * *Files identical despite different names*

### Comparing `qcontext-1.0.7/src/qcontext.egg-info/PKG-INFO` & `qcontext-1.0.8/src/qcontext.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: qcontext
-Version: 1.0.7
+Version: 1.0.8
 Summary: One of the most controversial things
 Author-email: cxllmerichie <cxllmerichie@gmail.com>
 Maintainer-email: cxllmerichie <cxllmerichie@gmail.com>
 License: MIT License
         
         Copyright (c) 2022-2023 cxllmerichie
```

### Comparing `qcontext-1.0.7/src/qcontext.egg-info/SOURCES.txt` & `qcontext-1.0.8/src/qcontext.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -314,14 +314,15 @@
 src/qcontext/widgets/frame.py
 src/qcontext/widgets/label.py
 src/qcontext/widgets/layout.py
 src/qcontext/widgets/line_input.py
 src/qcontext/widgets/popup.py
 src/qcontext/widgets/scroll_area.py
 src/qcontext/widgets/selector.py
+src/qcontext/widgets/slider.py
 src/qcontext/widgets/spacer.py
 src/qcontext/widgets/splitter.py
 src/qcontext/widgets/stacked_widget.py
 src/qcontext/widgets/statusbar.py
 src/qcontext/widgets/text_input.py
 src/qcontext/widgets/widget.py
 src/qcontext/widgets/window.py
```

