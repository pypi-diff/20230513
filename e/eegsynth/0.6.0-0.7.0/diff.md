# Comparing `tmp/eegsynth-0.6.0.tar.gz` & `tmp/eegsynth-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/eegsynth-0.6.0.tar", last modified: Thu Oct 27 19:27:42 2022, max compression
+gzip compressed data, was "eegsynth-0.7.0.tar", last modified: Sat May 13 08:07:10 2023, max compression
```

## Comparing `eegsynth-0.6.0.tar` & `eegsynth-0.7.0.tar`

### file list

```diff
@@ -1,245 +1,268 @@
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/
--rw-r--r--   0 roboos     (503) staff       (20)     4524 2022-10-27 19:27:42.000000 eegsynth-0.6.0/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     2698 2020-01-01 15:23:09.000000 eegsynth-0.6.0/README.md
--rw-r--r--   0 roboos     (503) staff       (20)        0 2020-01-01 15:23:09.000000 eegsynth-0.6.0/__init__.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/bin/
--rw-r--r--   0 roboos     (503) staff       (20)        0 2020-01-01 15:23:09.000000 eegsynth-0.6.0/bin/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4386 2022-06-06 12:47:44.000000 eegsynth-0.6.0/bin/eegsynth.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/
--rw-r--r--   0 roboos     (503) staff       (20)     4524 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     5049 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/SOURCES.txt
--rw-r--r--   0 roboos     (503) staff       (20)        1 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/dependency_links.txt
--rw-r--r--   0 roboos     (503) staff       (20)       58 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/entry_points.txt
--rw-r--r--   0 roboos     (503) staff       (20)      233 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/requires.txt
--rw-r--r--   0 roboos     (503) staff       (20)        9 2022-10-27 19:27:42.000000 eegsynth-0.6.0/eegsynth.egg-info/top_level.txt
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/lib/
--rw-r--r--   0 roboos     (503) staff       (20)     1656 2020-04-14 21:17:23.000000 eegsynth-0.6.0/lib/ArtNet.py
--rw-r--r--   0 roboos     (503) staff       (20)    17162 2019-09-21 12:06:06.000000 eegsynth-0.6.0/lib/EDF.py
--rw-r--r--   0 roboos     (503) staff       (20)    25482 2022-10-08 19:02:31.000000 eegsynth-0.6.0/lib/EEGsynth.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    27634 2022-06-12 07:25:53.000000 eegsynth-0.6.0/lib/FieldTrip.py
--rw-r--r--   0 roboos     (503) staff       (20)      435 2022-06-06 12:39:55.000000 eegsynth-0.6.0/lib/FieldTrip_test_client.py
--rw-r--r--   0 roboos     (503) staff       (20)      301 2022-06-06 12:39:55.000000 eegsynth-0.6.0/lib/FieldTrip_test_server.py
--rw-r--r--   0 roboos     (503) staff       (20)     2193 2022-06-06 12:39:55.000000 eegsynth-0.6.0/lib/RingBuffer.py
--rw-r--r--   0 roboos     (503) staff       (20)        0 2020-01-01 15:23:09.000000 eegsynth-0.6.0/lib/__init__.py
--rw-r--r--   0 roboos     (503) staff       (20)    59022 2022-03-26 20:53:12.000000 eegsynth-0.6.0/lib/colormap.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/
--rw-r--r--   0 roboos     (503) staff       (20)        0 2020-04-13 12:07:00.000000 eegsynth-0.6.0/module/__init__.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/accelerometer/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/accelerometer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6310 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/accelerometer/accelerometer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/audio2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/audio2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7387 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/audio2ft/audio2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/audiomixer/
--rwxr-xr-x   0 roboos     (503) staff       (20)      654 2022-10-15 06:39:00.000000 eegsynth-0.6.0/module/audiomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8018 2022-10-16 07:54:25.000000 eegsynth-0.6.0/module/audiomixer/audiomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/bitalino2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/bitalino2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7183 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/bitalino2ft/bitalino2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/brainflow2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2022-02-20 14:18:46.000000 eegsynth-0.6.0/module/brainflow2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7040 2022-02-20 15:51:59.000000 eegsynth-0.6.0/module/brainflow2ft/brainflow2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/buffer/
--rw-r--r--   0 roboos     (503) staff       (20)      650 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/buffer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4053 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/buffer/buffer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/clockdivider/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/clockdivider/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6048 2022-10-09 06:53:43.000000 eegsynth-0.6.0/module/clockdivider/clockdivider.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/clockmultiplier/
--rw-r--r--   0 roboos     (503) staff       (20)      659 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/clockmultiplier/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7873 2022-10-09 06:53:58.000000 eegsynth-0.6.0/module/clockmultiplier/clockmultiplier.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/cogito/
--rw-r--r--   0 roboos     (503) staff       (20)      650 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/cogito/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13048 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/cogito/cogito.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2020-01-01 15:23:09.000000 eegsynth-0.6.0/module/cogito/gtec2wav.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/complexity/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/complexity/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9329 2022-06-12 15:55:42.000000 eegsynth-0.6.0/module/complexity/complexity.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/compressor/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/compressor/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5725 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/compressor/compressor.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/csp/
--rw-r--r--   0 roboos     (503) staff       (20)      647 2022-06-05 10:10:40.000000 eegsynth-0.6.0/module/csp/__init__.py
--rw-r--r--   0 roboos     (503) staff       (20)    13384 2022-06-05 10:10:40.000000 eegsynth-0.6.0/module/csp/csp.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/delaytrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2022-04-29 07:08:20.000000 eegsynth-0.6.0/module/delaytrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6351 2022-05-16 14:05:51.000000 eegsynth-0.6.0/module/delaytrigger/delaytrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/demodulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      658 2022-02-17 20:35:41.000000 eegsynth-0.6.0/module/demodulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10309 2022-02-20 10:39:48.000000 eegsynth-0.6.0/module/demodulatetone/demodulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/endorphines/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/endorphines/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10553 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/endorphines/endorphines.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/example/
--rw-r--r--   0 roboos     (503) staff       (20)      651 2022-07-04 07:20:07.000000 eegsynth-0.6.0/module/example/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4469 2022-10-08 19:02:31.000000 eegsynth-0.6.0/module/example/example.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/generateclock/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/generateclock/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12711 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/generateclock/generateclock.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/generatecontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      659 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/generatecontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8917 2022-10-19 07:17:06.000000 eegsynth-0.6.0/module/generatecontrol/generatecontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/generatesignal/
--rw-r--r--   0 roboos     (503) staff       (20)      682 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/generatesignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11409 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/generatesignal/generatesignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/generatetrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      659 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/generatetrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7379 2022-10-19 06:31:45.000000 eegsynth-0.6.0/module/generatetrigger/generatetrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/geomixer/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/geomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9273 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/geomixer/geomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/heartrate/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/heartrate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9114 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/heartrate/heartrate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/historycontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      658 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/historycontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9884 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/historycontrol/historycontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/historysignal/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/historysignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10115 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/historysignal/historysignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      387 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15985 2022-07-05 11:43:42.000000 eegsynth-0.6.0/module/inputcontrol/inputcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7159 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/inputlsl/inputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5864 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/inputmidi/inputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6562 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/inputmqtt/inputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8636 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/inputosc/inputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/inputzeromq/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/inputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6440 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/inputzeromq/inputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/keyboard/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/keyboard/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15199 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/keyboard/keyboard.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/launchcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/launchcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14605 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/launchcontrol/launchcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/launchpad/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/launchpad/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15154 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/launchpad/launchpad.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/lsl2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      650 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/lsl2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7318 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/lsl2ft/lsl2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/modulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2022-02-13 17:35:57.000000 eegsynth-0.6.0/module/modulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11269 2022-02-17 20:35:41.000000 eegsynth-0.6.0/module/modulatetone/modulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputartnet/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/outputartnet/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7166 2022-10-09 06:54:50.000000 eegsynth-0.6.0/module/outputartnet/outputartnet.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputaudio/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/outputaudio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12980 2022-07-31 14:07:50.000000 eegsynth-0.6.0/module/outputaudio/outputaudio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputcvgate/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-04-14 19:34:54.000000 eegsynth-0.6.0/module/outputcvgate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10713 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/outputcvgate/outputcvgate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputdmx/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-29 13:55:42.000000 eegsynth-0.6.0/module/outputdmx/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7557 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/outputdmx/outputdmx.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputgpio/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-03-29 13:26:24.000000 eegsynth-0.6.0/module/outputgpio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9057 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/outputgpio/outputgpio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-31 19:47:39.000000 eegsynth-0.6.0/module/outputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8428 2022-02-09 13:31:22.000000 eegsynth-0.6.0/module/outputlsl/outputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/outputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13841 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/outputmidi/outputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-03-31 19:50:53.000000 eegsynth-0.6.0/module/outputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7825 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/outputmqtt/outputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/outputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8154 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/outputosc/outputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/outputzeromq/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-03-31 19:50:36.000000 eegsynth-0.6.0/module/outputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7262 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/outputzeromq/outputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/playbackcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      659 2020-03-31 19:50:24.000000 eegsynth-0.6.0/module/playbackcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7030 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/playbackcontrol/playbackcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/playbacksignal/
--rw-r--r--   0 roboos     (503) staff       (20)      658 2020-03-31 19:50:12.000000 eegsynth-0.6.0/module/playbacksignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9620 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/playbacksignal/playbacksignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/plotcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      386 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/plotcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7050 2022-07-03 18:56:16.000000 eegsynth-0.6.0/module/plotcontrol/plotcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/plotimage/
--rw-r--r--   0 roboos     (503) staff       (20)      384 2022-07-02 13:09:02.000000 eegsynth-0.6.0/module/plotimage/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7147 2022-06-12 15:55:42.000000 eegsynth-0.6.0/module/plotimage/plotimage.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/plotsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      385 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/plotsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12125 2022-07-03 18:54:30.000000 eegsynth-0.6.0/module/plotsignal/plotsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/plotspectral/
--rw-r--r--   0 roboos     (503) staff       (20)      387 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/plotspectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    22919 2022-07-03 18:55:51.000000 eegsynth-0.6.0/module/plotspectral/plotspectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/plottrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      386 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/plottrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8687 2022-06-12 15:55:42.000000 eegsynth-0.6.0/module/plottrigger/plottrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/postprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      658 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/postprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7099 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/postprocessing/postprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/preprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/preprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15393 2022-10-13 20:34:27.000000 eegsynth-0.6.0/module/preprocessing/preprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/processtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      658 2020-03-31 19:49:36.000000 eegsynth-0.6.0/module/processtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10140 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/processtrigger/processtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/quantizer/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-31 19:49:24.000000 eegsynth-0.6.0/module/quantizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7127 2022-10-15 10:16:29.000000 eegsynth-0.6.0/module/quantizer/quantizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/recordcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-03-31 19:49:09.000000 eegsynth-0.6.0/module/recordcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9571 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/recordcontrol/recordcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/recordsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-03-31 19:48:51.000000 eegsynth-0.6.0/module/recordsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10846 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/recordsignal/recordsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/recordtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      657 2020-03-31 19:48:40.000000 eegsynth-0.6.0/module/recordtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8161 2022-07-02 14:23:26.000000 eegsynth-0.6.0/module/recordtrigger/recordtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/rms/
--rw-r--r--   0 roboos     (503) staff       (20)      647 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/rms/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7197 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/rms/rms.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/sampler/
--rw-r--r--   0 roboos     (503) staff       (20)      651 2020-03-31 19:48:28.000000 eegsynth-0.6.0/module/sampler/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14988 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/sampler/sampler.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/sequencer/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-31 19:48:18.000000 eegsynth-0.6.0/module/sequencer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10912 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/sequencer/sequencer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/slewlimiter/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/slewlimiter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5005 2020-04-14 18:43:23.000000 eegsynth-0.6.0/module/slewlimiter/slewlimiter.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/sonification/
--rw-r--r--   0 roboos     (503) staff       (20)      656 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/sonification/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15727 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/sonification/sonification.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/spectral/
--rw-r--r--   0 roboos     (503) staff       (20)      652 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/spectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2022-07-02 06:30:11.000000 eegsynth-0.6.0/module/spectral/spectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/synthesizer/
--rw-r--r--   0 roboos     (503) staff       (20)      655 2020-03-31 19:48:10.000000 eegsynth-0.6.0/module/synthesizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15638 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/synthesizer/synthesizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/threshold/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/threshold/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8393 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/threshold/threshold.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/unicorn2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2022-10-13 20:08:45.000000 eegsynth-0.6.0/module/unicorn2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8012 2022-10-09 08:57:45.000000 eegsynth-0.6.0/module/unicorn2ft/unicorn2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/volcabass/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-29 20:46:41.000000 eegsynth-0.6.0/module/volcabass/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10311 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/volcabass/volcabass.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/volcabeats/
--rw-r--r--   0 roboos     (503) staff       (20)      654 2020-03-29 20:46:51.000000 eegsynth-0.6.0/module/volcabeats/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9139 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/volcabeats/volcabeats.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/volcakeys/
--rw-r--r--   0 roboos     (503) staff       (20)      653 2020-03-29 20:48:42.000000 eegsynth-0.6.0/module/volcakeys/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10427 2022-06-06 12:39:55.000000 eegsynth-0.6.0/module/volcakeys/volcakeys.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2022-10-27 19:27:42.000000 eegsynth-0.6.0/module/vumeter/
--rw-r--r--   0 roboos     (503) staff       (20)      382 2020-02-15 14:46:30.000000 eegsynth-0.6.0/module/vumeter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7078 2022-06-12 15:55:42.000000 eegsynth-0.6.0/module/vumeter/vumeter.py
--rw-r--r--   0 roboos     (503) staff       (20)       38 2022-10-27 19:27:42.000000 eegsynth-0.6.0/setup.cfg
--rwxr-xr-x   0 roboos     (503) staff       (20)     3438 2022-10-27 19:26:04.000000 eegsynth-0.6.0/setup.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.360677 eegsynth-0.7.0/
+-rw-r--r--   0 roboos     (503) staff       (20)    32472 2023-03-21 19:58:52.000000 eegsynth-0.7.0/LICENSE
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 08:07:10.360183 eegsynth-0.7.0/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     2698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/README.md
+-rwxr-xr-x   0 roboos     (503) staff       (20)    16439 2023-05-13 08:01:31.000000 eegsynth-0.7.0/eegsynth-gui.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.232720 eegsynth-0.7.0/eegsynth.egg-info/
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     5482 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/SOURCES.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        1 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/dependency_links.txt
+-rw-r--r--   0 roboos     (503) staff       (20)       53 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/entry_points.txt
+-rw-r--r--   0 roboos     (503) staff       (20)      296 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/requires.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        9 2023-05-13 08:07:09.000000 eegsynth-0.7.0/eegsynth.egg-info/top_level.txt
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13354 2023-05-13 08:01:31.000000 eegsynth-0.7.0/eegsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1388 2023-05-04 12:16:58.000000 eegsynth-0.7.0/hook-pylsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.241782 eegsynth-0.7.0/lib/
+-rw-r--r--   0 roboos     (503) staff       (20)     1656 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/ArtNet.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1450 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/DummyRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)    17162 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/EDF.py
+-rw-r--r--   0 roboos     (503) staff       (20)    35670 2023-05-02 20:55:48.000000 eegsynth-0.7.0/lib/EEGsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1975 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/FakeRedis.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    27618 2023-04-30 19:35:59.000000 eegsynth-0.7.0/lib/FieldTrip.py
+-rw-r--r--   0 roboos     (503) staff       (20)      435 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/FieldTrip_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)      301 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/FieldTrip_test_server.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1131 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/Redis_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)     2193 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/RingBuffer.py
+-rw-r--r--   0 roboos     (503) staff       (20)     7184 2023-05-02 18:05:03.000000 eegsynth-0.7.0/lib/ZmqRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/__init__.py
+-rw-r--r--   0 roboos     (503) staff       (20)    59022 2023-03-21 19:58:52.000000 eegsynth-0.7.0/lib/colormap.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.243588 eegsynth-0.7.0/module/
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/__init__.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.244843 eegsynth-0.7.0/module/accelerometer/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/accelerometer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5707 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/accelerometer/accelerometer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.246233 eegsynth-0.7.0/module/audio2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/audio2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6708 2023-04-29 08:49:58.000000 eegsynth-0.7.0/module/audio2ft/audio2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.247460 eegsynth-0.7.0/module/audiomixer/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/audiomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7220 2023-04-29 09:10:40.000000 eegsynth-0.7.0/module/audiomixer/audiomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.248926 eegsynth-0.7.0/module/bitalino2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/bitalino2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6396 2023-04-29 09:15:26.000000 eegsynth-0.7.0/module/bitalino2ft/bitalino2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.250139 eegsynth-0.7.0/module/brainflow2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/brainflow2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6322 2023-04-29 08:15:56.000000 eegsynth-0.7.0/module/brainflow2ft/brainflow2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.251249 eegsynth-0.7.0/module/buffer/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/buffer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3468 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/buffer/buffer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.252503 eegsynth-0.7.0/module/clockdivider/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/clockdivider/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5433 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/clockdivider/clockdivider.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.254391 eegsynth-0.7.0/module/clockmultiplier/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/clockmultiplier/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7267 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/clockmultiplier/clockmultiplier.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.256953 eegsynth-0.7.0/module/cogito/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/cogito/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12302 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/cogito/cogito.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/cogito/gtec2wav.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.258540 eegsynth-0.7.0/module/complexity/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/complexity/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8635 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/complexity/complexity.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.259842 eegsynth-0.7.0/module/compressor/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/compressor/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5131 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/compressor/compressor.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.261240 eegsynth-0.7.0/module/csp/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/csp/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12865 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/csp/csp.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.263084 eegsynth-0.7.0/module/delaytrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/delaytrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5784 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/delaytrigger/delaytrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.264758 eegsynth-0.7.0/module/demodulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/demodulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9517 2023-04-29 09:15:47.000000 eegsynth-0.7.0/module/demodulatetone/demodulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.266160 eegsynth-0.7.0/module/endorphines/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/endorphines/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9952 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/endorphines/endorphines.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.267614 eegsynth-0.7.0/module/example/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/example/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4008 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/example/example.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.269017 eegsynth-0.7.0/module/generateclock/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/generateclock/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12009 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/generateclock/generateclock.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.270588 eegsynth-0.7.0/module/generatecontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/generatecontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8392 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/generatecontrol/generatecontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.271962 eegsynth-0.7.0/module/generatesignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/generatesignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10722 2023-05-02 20:11:22.000000 eegsynth-0.7.0/module/generatesignal/generatesignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.273596 eegsynth-0.7.0/module/generatetrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/generatetrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6763 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/generatetrigger/generatetrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.274852 eegsynth-0.7.0/module/geomixer/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/geomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8648 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/geomixer/geomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.276061 eegsynth-0.7.0/module/heartrate/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/heartrate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8413 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/heartrate/heartrate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.277993 eegsynth-0.7.0/module/historycontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/historycontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9494 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/historycontrol/historycontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.280925 eegsynth-0.7.0/module/historysignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/historysignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9401 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/historysignal/historysignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.283665 eegsynth-0.7.0/module/inputcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17279 2023-05-10 07:50:04.000000 eegsynth-0.7.0/module/inputcontrol/inputcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.285523 eegsynth-0.7.0/module/inputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6618 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/inputlsl/inputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.287274 eegsynth-0.7.0/module/inputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5264 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/inputmidi/inputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.289255 eegsynth-0.7.0/module/inputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5957 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/inputmqtt/inputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.291180 eegsynth-0.7.0/module/inputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/inputosc/inputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.292497 eegsynth-0.7.0/module/inputzeromq/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/inputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5740 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/inputzeromq/inputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.294092 eegsynth-0.7.0/module/keyboard/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/keyboard/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14634 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/keyboard/keyboard.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.295999 eegsynth-0.7.0/module/launchcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/launchcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13953 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/launchcontrol/launchcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.297607 eegsynth-0.7.0/module/launchpad/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/launchpad/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14601 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/launchpad/launchpad.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.299095 eegsynth-0.7.0/module/logging/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-04-30 07:48:46.000000 eegsynth-0.7.0/module/logging/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7275 2023-04-30 20:43:41.000000 eegsynth-0.7.0/module/logging/logging.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.300478 eegsynth-0.7.0/module/lsl2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/lsl2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6768 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/lsl2ft/lsl2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.301790 eegsynth-0.7.0/module/modulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/modulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10550 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/modulatetone/modulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.303131 eegsynth-0.7.0/module/outputartnet/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputartnet/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6639 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputartnet/outputartnet.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.304504 eegsynth-0.7.0/module/outputaudio/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputaudio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12350 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputaudio/outputaudio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.305834 eegsynth-0.7.0/module/outputcvgate/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputcvgate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10263 2023-05-07 13:53:03.000000 eegsynth-0.7.0/module/outputcvgate/outputcvgate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.307566 eegsynth-0.7.0/module/outputdmx/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputdmx/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6984 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputdmx/outputdmx.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.309048 eegsynth-0.7.0/module/outputgpio/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputgpio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8490 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputgpio/outputgpio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.310481 eegsynth-0.7.0/module/outputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7652 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputlsl/outputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.311859 eegsynth-0.7.0/module/outputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13389 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputmidi/outputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.313520 eegsynth-0.7.0/module/outputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7263 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputmqtt/outputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.315201 eegsynth-0.7.0/module/outputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7596 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputosc/outputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.316489 eegsynth-0.7.0/module/outputzeromq/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/outputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6590 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/outputzeromq/outputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.317548 eegsynth-0.7.0/module/pepipiaf/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/pepipiaf/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    25727 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/pepipiaf/pepipiaf.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.318554 eegsynth-0.7.0/module/playbackcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/playbackcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6454 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/playbackcontrol/playbackcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.319764 eegsynth-0.7.0/module/playbacksignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/playbacksignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9858 2023-05-02 20:53:32.000000 eegsynth-0.7.0/module/playbacksignal/playbacksignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.320963 eegsynth-0.7.0/module/plotcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/plotcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7058 2023-04-30 20:43:43.000000 eegsynth-0.7.0/module/plotcontrol/plotcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.322219 eegsynth-0.7.0/module/plotimage/
+-rw-r--r--   0 roboos     (503) staff       (20)      424 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/plotimage/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6780 2023-04-30 20:43:48.000000 eegsynth-0.7.0/module/plotimage/plotimage.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.323573 eegsynth-0.7.0/module/plotsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      425 2023-04-30 19:40:07.000000 eegsynth-0.7.0/module/plotsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11992 2023-04-30 20:43:51.000000 eegsynth-0.7.0/module/plotsignal/plotsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.325344 eegsynth-0.7.0/module/plotspectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/plotspectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    23337 2023-04-30 20:43:55.000000 eegsynth-0.7.0/module/plotspectral/plotspectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.327065 eegsynth-0.7.0/module/plottext/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/plottext/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7894 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/plottext/plottext.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.328116 eegsynth-0.7.0/module/plottopo/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/plottopo/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8637 2023-04-30 20:44:05.000000 eegsynth-0.7.0/module/plottopo/plottopo.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.329130 eegsynth-0.7.0/module/plottrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/plottrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8295 2023-04-30 20:44:08.000000 eegsynth-0.7.0/module/plottrigger/plottrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.330768 eegsynth-0.7.0/module/postprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/postprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6740 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/postprocessing/postprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.331952 eegsynth-0.7.0/module/preprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/preprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14798 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/preprocessing/preprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.333152 eegsynth-0.7.0/module/processtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/processtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9670 2023-05-02 19:32:40.000000 eegsynth-0.7.0/module/processtrigger/processtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.334339 eegsynth-0.7.0/module/quantizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/quantizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6181 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/quantizer/quantizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.335573 eegsynth-0.7.0/module/recordcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      701 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/recordcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10121 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/recordcontrol/recordcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.336598 eegsynth-0.7.0/module/recordsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/recordsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11451 2023-05-02 20:50:47.000000 eegsynth-0.7.0/module/recordsignal/recordsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.337930 eegsynth-0.7.0/module/recordtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/recordtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8005 2023-05-13 08:01:31.000000 eegsynth-0.7.0/module/recordtrigger/recordtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.338959 eegsynth-0.7.0/module/redis/
+-rw-r--r--   0 roboos     (503) staff       (20)      683 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/redis/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3599 2023-04-30 20:46:28.000000 eegsynth-0.7.0/module/redis/redis.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.340159 eegsynth-0.7.0/module/rms/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/rms/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6500 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/rms/rms.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.341719 eegsynth-0.7.0/module/sampler/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/sampler/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14409 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/sampler/sampler.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.343132 eegsynth-0.7.0/module/sequencer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/sequencer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10356 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/sequencer/sequencer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.344768 eegsynth-0.7.0/module/slewlimiter/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/slewlimiter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4470 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/slewlimiter/slewlimiter.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.346699 eegsynth-0.7.0/module/sonification/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/sonification/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15140 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/sonification/sonification.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.348220 eegsynth-0.7.0/module/spectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/spectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7528 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/spectral/spectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.349810 eegsynth-0.7.0/module/synthesizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/synthesizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15026 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/synthesizer/synthesizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.351073 eegsynth-0.7.0/module/threshold/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/threshold/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7690 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/threshold/threshold.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.352329 eegsynth-0.7.0/module/unicorn2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/unicorn2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7588 2023-05-07 13:53:03.000000 eegsynth-0.7.0/module/unicorn2ft/unicorn2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.353466 eegsynth-0.7.0/module/videoprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-25 11:03:23.000000 eegsynth-0.7.0/module/videoprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17749 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/videoprocessing/videoprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.354902 eegsynth-0.7.0/module/volcabass/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/volcabass/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9541 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/volcabass/volcabass.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.356154 eegsynth-0.7.0/module/volcabeats/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/volcabeats/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8370 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/volcabeats/volcabeats.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.357486 eegsynth-0.7.0/module/volcakeys/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/volcakeys/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9657 2023-04-30 15:10:12.000000 eegsynth-0.7.0/module/volcakeys/volcakeys.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 08:07:10.358970 eegsynth-0.7.0/module/vumeter/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-03-21 19:58:52.000000 eegsynth-0.7.0/module/vumeter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6651 2023-04-30 20:44:11.000000 eegsynth-0.7.0/module/vumeter/vumeter.py
+-rw-r--r--   0 roboos     (503) staff       (20)       38 2023-05-13 08:07:10.360843 eegsynth-0.7.0/setup.cfg
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3551 2023-04-22 08:08:45.000000 eegsynth-0.7.0/setup.py
+-rw-r--r--   0 roboos     (503) staff       (20)       20 2023-04-22 08:08:45.000000 eegsynth-0.7.0/version.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `eegsynth-0.6.0/PKG-INFO` & `eegsynth-0.7.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,56 +1,56 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.6.0
+Version: 0.7.0
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
 Project-URL: Tracker, https://github.com/eegsynth/eegsynth/issues
-Description: ![](https://github.com/eegsynth/eegsynth/raw/master/doc/figures/EEGsynth_logo.svg?sanitize=true)
-        
-        The EEGsynth is a [Python](https://www.python.org/) codebase released under the [GNU general public license]( https://en.wikipedia.org/wiki/GNU_General_Public_License) that provides a real-time interface between (open-hardware) devices for electrophysiological recordings (e.g. EEG, EMG and ECG) and analogue and digital devices (e.g. MIDI, lights, games and analogue synthesizers). The EEGsynth allows one to use electrical activity recorded from the brain or body to flexibly control devices in real-time, i.e. (re)active and passive brain-computer-interfaces (BCIs), biofeedback and neurofeedback.
-        
-        Since December 2018, the EEGsynth is registered as a legal _Association_ with the French authorities.
-        
-        ## Documentation
-        
-        The EEGsynth code and documentation are hosted on Github and organized as follows:
-        
-         * [bin](https://github.com/eegsynth/eegsynth/raw/master/bin) contains binaries for the buffer and for some EEG systems
-         * [doc](https://github.com/eegsynth/eegsynth/raw/master/doc) contains the documentation on the EEGsynth software
-         * [hardware](https://github.com/eegsynth/eegsynth/raw/master/hardware) contains the hardware documentation
-         * [lib](https://github.com/eegsynth/eegsynth/raw/master/lib) contains some libraries
-         * [module](https://github.com/eegsynth/eegsynth/raw/master/module) contains the EEGsynth modules
-         * [patches](https://github.com/eegsynth/eegsynth/raw/master/patches) contains patches for performances
-        
-        ## Disclaimer
-        
-        The EEGsynth does not allow diagnostic investigations or clinical applications. It also does not provide a graphical user interface for offline analysis. Rather, the EEGsynth is intended as a collaborative interdisciplinary [open-source](https://opensource.com/open-source-way) and [open-hardware](https://opensource.com/resources/what-open-hardware) project that brings together programmers, musicians, artists, neuroscientists and developers in scientific and artistic exploration.
-        
-        Although there are plans to make it more 'plug-and-play', the EEGsynth currently has to be run from the command line, using [Python](https://www.python.org/) and [Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) scripts, and is therefor not friendly for those not familiar with such an approach.
-        
-        ## Collaborate and get more information
-        
-        When you start an project with the EEGsynth, consider doing it together with in a group of people that have knowledge and experience complimentary to yours, such as in electrophysiology, neuroscience, psychology, programming, computer science or signal processing.
-        
-        More information can be found at [our website](https://www.eegsynth.org).  Follow us on [Facebook](https://www.facebook.com/EEGsynth/) and [Twitter](https://twitter.com/eegsynth), and check our past and upcoming events on [our calendar](http://www.eegsynth.org/?calendar=eegsynth-calendar). Please feel free to contact us via our [contact form](http://www.eegsynth.org/?page_id=233).
-        
 Keywords: EEG,EMG,ECG,BCI,brain,art,music,sound,sonification,brain-computer interface,real-time
-Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Topic :: Artistic Software
 Classifier: Topic :: Multimedia :: Sound/Audio
 Classifier: Topic :: Scientific/Engineering :: Human Machine Interfaces
 Classifier: Topic :: Scientific/Engineering :: Medical Science Apps.
 Requires-Python: >=2.7
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+![](https://github.com/eegsynth/eegsynth/raw/master/doc/figures/EEGsynth_logo.svg?sanitize=true)
+
+The EEGsynth is a [Python](https://www.python.org/) codebase released under the [GNU general public license]( https://en.wikipedia.org/wiki/GNU_General_Public_License) that provides a real-time interface between (open-hardware) devices for electrophysiological recordings (e.g. EEG, EMG and ECG) and analogue and digital devices (e.g. MIDI, lights, games and analogue synthesizers). The EEGsynth allows one to use electrical activity recorded from the brain or body to flexibly control devices in real-time, i.e. (re)active and passive brain-computer-interfaces (BCIs), biofeedback and neurofeedback.
+
+Since December 2018, the EEGsynth is registered as a legal _Association_ with the French authorities.
+
+## Documentation
+
+The EEGsynth code and documentation are hosted on Github and organized as follows:
+
+ * [bin](https://github.com/eegsynth/eegsynth/raw/master/bin) contains binaries for the buffer and for some EEG systems
+ * [doc](https://github.com/eegsynth/eegsynth/raw/master/doc) contains the documentation on the EEGsynth software
+ * [hardware](https://github.com/eegsynth/eegsynth/raw/master/hardware) contains the hardware documentation
+ * [lib](https://github.com/eegsynth/eegsynth/raw/master/lib) contains some libraries
+ * [module](https://github.com/eegsynth/eegsynth/raw/master/module) contains the EEGsynth modules
+ * [patches](https://github.com/eegsynth/eegsynth/raw/master/patches) contains patches for performances
+
+## Disclaimer
+
+The EEGsynth does not allow diagnostic investigations or clinical applications. It also does not provide a graphical user interface for offline analysis. Rather, the EEGsynth is intended as a collaborative interdisciplinary [open-source](https://opensource.com/open-source-way) and [open-hardware](https://opensource.com/resources/what-open-hardware) project that brings together programmers, musicians, artists, neuroscientists and developers in scientific and artistic exploration.
+
+Although there are plans to make it more 'plug-and-play', the EEGsynth currently has to be run from the command line, using [Python](https://www.python.org/) and [Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) scripts, and is therefor not friendly for those not familiar with such an approach.
+
+## Collaborate and get more information
+
+When you start an project with the EEGsynth, consider doing it together with in a group of people that have knowledge and experience complimentary to yours, such as in electrophysiology, neuroscience, psychology, programming, computer science or signal processing.
+
+More information can be found at [our website](https://www.eegsynth.org).  Follow us on [Facebook](https://www.facebook.com/EEGsynth/) and [Twitter](https://twitter.com/eegsynth), and check our past and upcoming events on [our calendar](http://www.eegsynth.org/?calendar=eegsynth-calendar). Please feel free to contact us via our [contact form](http://www.eegsynth.org/?page_id=233).
```

### Comparing `eegsynth-0.6.0/README.md` & `eegsynth-0.7.0/README.md`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/eegsynth.egg-info/PKG-INFO` & `eegsynth-0.7.0/eegsynth.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,56 +1,56 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.6.0
+Version: 0.7.0
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
 Project-URL: Tracker, https://github.com/eegsynth/eegsynth/issues
-Description: ![](https://github.com/eegsynth/eegsynth/raw/master/doc/figures/EEGsynth_logo.svg?sanitize=true)
-        
-        The EEGsynth is a [Python](https://www.python.org/) codebase released under the [GNU general public license]( https://en.wikipedia.org/wiki/GNU_General_Public_License) that provides a real-time interface between (open-hardware) devices for electrophysiological recordings (e.g. EEG, EMG and ECG) and analogue and digital devices (e.g. MIDI, lights, games and analogue synthesizers). The EEGsynth allows one to use electrical activity recorded from the brain or body to flexibly control devices in real-time, i.e. (re)active and passive brain-computer-interfaces (BCIs), biofeedback and neurofeedback.
-        
-        Since December 2018, the EEGsynth is registered as a legal _Association_ with the French authorities.
-        
-        ## Documentation
-        
-        The EEGsynth code and documentation are hosted on Github and organized as follows:
-        
-         * [bin](https://github.com/eegsynth/eegsynth/raw/master/bin) contains binaries for the buffer and for some EEG systems
-         * [doc](https://github.com/eegsynth/eegsynth/raw/master/doc) contains the documentation on the EEGsynth software
-         * [hardware](https://github.com/eegsynth/eegsynth/raw/master/hardware) contains the hardware documentation
-         * [lib](https://github.com/eegsynth/eegsynth/raw/master/lib) contains some libraries
-         * [module](https://github.com/eegsynth/eegsynth/raw/master/module) contains the EEGsynth modules
-         * [patches](https://github.com/eegsynth/eegsynth/raw/master/patches) contains patches for performances
-        
-        ## Disclaimer
-        
-        The EEGsynth does not allow diagnostic investigations or clinical applications. It also does not provide a graphical user interface for offline analysis. Rather, the EEGsynth is intended as a collaborative interdisciplinary [open-source](https://opensource.com/open-source-way) and [open-hardware](https://opensource.com/resources/what-open-hardware) project that brings together programmers, musicians, artists, neuroscientists and developers in scientific and artistic exploration.
-        
-        Although there are plans to make it more 'plug-and-play', the EEGsynth currently has to be run from the command line, using [Python](https://www.python.org/) and [Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) scripts, and is therefor not friendly for those not familiar with such an approach.
-        
-        ## Collaborate and get more information
-        
-        When you start an project with the EEGsynth, consider doing it together with in a group of people that have knowledge and experience complimentary to yours, such as in electrophysiology, neuroscience, psychology, programming, computer science or signal processing.
-        
-        More information can be found at [our website](https://www.eegsynth.org).  Follow us on [Facebook](https://www.facebook.com/EEGsynth/) and [Twitter](https://twitter.com/eegsynth), and check our past and upcoming events on [our calendar](http://www.eegsynth.org/?calendar=eegsynth-calendar). Please feel free to contact us via our [contact form](http://www.eegsynth.org/?page_id=233).
-        
 Keywords: EEG,EMG,ECG,BCI,brain,art,music,sound,sonification,brain-computer interface,real-time
-Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Topic :: Artistic Software
 Classifier: Topic :: Multimedia :: Sound/Audio
 Classifier: Topic :: Scientific/Engineering :: Human Machine Interfaces
 Classifier: Topic :: Scientific/Engineering :: Medical Science Apps.
 Requires-Python: >=2.7
 Description-Content-Type: text/markdown
+License-File: LICENSE
+
+![](https://github.com/eegsynth/eegsynth/raw/master/doc/figures/EEGsynth_logo.svg?sanitize=true)
+
+The EEGsynth is a [Python](https://www.python.org/) codebase released under the [GNU general public license]( https://en.wikipedia.org/wiki/GNU_General_Public_License) that provides a real-time interface between (open-hardware) devices for electrophysiological recordings (e.g. EEG, EMG and ECG) and analogue and digital devices (e.g. MIDI, lights, games and analogue synthesizers). The EEGsynth allows one to use electrical activity recorded from the brain or body to flexibly control devices in real-time, i.e. (re)active and passive brain-computer-interfaces (BCIs), biofeedback and neurofeedback.
+
+Since December 2018, the EEGsynth is registered as a legal _Association_ with the French authorities.
+
+## Documentation
+
+The EEGsynth code and documentation are hosted on Github and organized as follows:
+
+ * [bin](https://github.com/eegsynth/eegsynth/raw/master/bin) contains binaries for the buffer and for some EEG systems
+ * [doc](https://github.com/eegsynth/eegsynth/raw/master/doc) contains the documentation on the EEGsynth software
+ * [hardware](https://github.com/eegsynth/eegsynth/raw/master/hardware) contains the hardware documentation
+ * [lib](https://github.com/eegsynth/eegsynth/raw/master/lib) contains some libraries
+ * [module](https://github.com/eegsynth/eegsynth/raw/master/module) contains the EEGsynth modules
+ * [patches](https://github.com/eegsynth/eegsynth/raw/master/patches) contains patches for performances
+
+## Disclaimer
+
+The EEGsynth does not allow diagnostic investigations or clinical applications. It also does not provide a graphical user interface for offline analysis. Rather, the EEGsynth is intended as a collaborative interdisciplinary [open-source](https://opensource.com/open-source-way) and [open-hardware](https://opensource.com/resources/what-open-hardware) project that brings together programmers, musicians, artists, neuroscientists and developers in scientific and artistic exploration.
+
+Although there are plans to make it more 'plug-and-play', the EEGsynth currently has to be run from the command line, using [Python](https://www.python.org/) and [Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) scripts, and is therefor not friendly for those not familiar with such an approach.
+
+## Collaborate and get more information
+
+When you start an project with the EEGsynth, consider doing it together with in a group of people that have knowledge and experience complimentary to yours, such as in electrophysiology, neuroscience, psychology, programming, computer science or signal processing.
+
+More information can be found at [our website](https://www.eegsynth.org).  Follow us on [Facebook](https://www.facebook.com/EEGsynth/) and [Twitter](https://twitter.com/eegsynth), and check our past and upcoming events on [our calendar](http://www.eegsynth.org/?calendar=eegsynth-calendar). Please feel free to contact us via our [contact form](http://www.eegsynth.org/?page_id=233).
```

### Comparing `eegsynth-0.6.0/eegsynth.egg-info/SOURCES.txt` & `eegsynth-0.7.0/eegsynth.egg-info/SOURCES.txt`

 * *Files 7% similar despite different names*

```diff
@@ -1,26 +1,31 @@
+LICENSE
 README.md
 setup.py
-./__init__.py
-./setup.py
-bin/__init__.py
-bin/eegsynth.py
+./eegsynth-gui.py
+./eegsynth.py
+./hook-pylsl.py
+./version.py
 eegsynth.egg-info/PKG-INFO
 eegsynth.egg-info/SOURCES.txt
 eegsynth.egg-info/dependency_links.txt
 eegsynth.egg-info/entry_points.txt
 eegsynth.egg-info/requires.txt
 eegsynth.egg-info/top_level.txt
 lib/ArtNet.py
+lib/DummyRedis.py
 lib/EDF.py
 lib/EEGsynth.py
+lib/FakeRedis.py
 lib/FieldTrip.py
 lib/FieldTrip_test_client.py
 lib/FieldTrip_test_server.py
+lib/Redis_test_client.py
 lib/RingBuffer.py
+lib/ZmqRedis.py
 lib/__init__.py
 lib/colormap.py
 module/__init__.py
 module/accelerometer/__init__.py
 module/accelerometer/accelerometer.py
 module/audio2ft/__init__.py
 module/audio2ft/audio2ft.py
@@ -83,14 +88,16 @@
 module/inputzeromq/inputzeromq.py
 module/keyboard/__init__.py
 module/keyboard/keyboard.py
 module/launchcontrol/__init__.py
 module/launchcontrol/launchcontrol.py
 module/launchpad/__init__.py
 module/launchpad/launchpad.py
+module/logging/__init__.py
+module/logging/logging.py
 module/lsl2ft/__init__.py
 module/lsl2ft/lsl2ft.py
 module/modulatetone/__init__.py
 module/modulatetone/modulatetone.py
 module/outputartnet/__init__.py
 module/outputartnet/outputartnet.py
 module/outputaudio/__init__.py
@@ -107,26 +114,32 @@
 module/outputmidi/outputmidi.py
 module/outputmqtt/__init__.py
 module/outputmqtt/outputmqtt.py
 module/outputosc/__init__.py
 module/outputosc/outputosc.py
 module/outputzeromq/__init__.py
 module/outputzeromq/outputzeromq.py
+module/pepipiaf/__init__.py
+module/pepipiaf/pepipiaf.py
 module/playbackcontrol/__init__.py
 module/playbackcontrol/playbackcontrol.py
 module/playbacksignal/__init__.py
 module/playbacksignal/playbacksignal.py
 module/plotcontrol/__init__.py
 module/plotcontrol/plotcontrol.py
 module/plotimage/__init__.py
 module/plotimage/plotimage.py
 module/plotsignal/__init__.py
 module/plotsignal/plotsignal.py
 module/plotspectral/__init__.py
 module/plotspectral/plotspectral.py
+module/plottext/__init__.py
+module/plottext/plottext.py
+module/plottopo/__init__.py
+module/plottopo/plottopo.py
 module/plottrigger/__init__.py
 module/plottrigger/plottrigger.py
 module/postprocessing/__init__.py
 module/postprocessing/postprocessing.py
 module/preprocessing/__init__.py
 module/preprocessing/preprocessing.py
 module/processtrigger/__init__.py
@@ -135,14 +148,16 @@
 module/quantizer/quantizer.py
 module/recordcontrol/__init__.py
 module/recordcontrol/recordcontrol.py
 module/recordsignal/__init__.py
 module/recordsignal/recordsignal.py
 module/recordtrigger/__init__.py
 module/recordtrigger/recordtrigger.py
+module/redis/__init__.py
+module/redis/redis.py
 module/rms/__init__.py
 module/rms/rms.py
 module/sampler/__init__.py
 module/sampler/sampler.py
 module/sequencer/__init__.py
 module/sequencer/sequencer.py
 module/slewlimiter/__init__.py
@@ -153,14 +168,16 @@
 module/spectral/spectral.py
 module/synthesizer/__init__.py
 module/synthesizer/synthesizer.py
 module/threshold/__init__.py
 module/threshold/threshold.py
 module/unicorn2ft/__init__.py
 module/unicorn2ft/unicorn2ft.py
+module/videoprocessing/__init__.py
+module/videoprocessing/videoprocessing.py
 module/volcabass/__init__.py
 module/volcabass/volcabass.py
 module/volcabeats/__init__.py
 module/volcabeats/volcabeats.py
 module/volcakeys/__init__.py
 module/volcakeys/volcakeys.py
 module/vumeter/__init__.py
```

### Comparing `eegsynth-0.6.0/lib/ArtNet.py` & `eegsynth-0.7.0/lib/ArtNet.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/lib/EDF.py` & `eegsynth-0.7.0/lib/EDF.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/lib/EEGsynth.py` & `eegsynth-0.7.0/lib/EEGsynth.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,84 +1,397 @@
+# This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
+#
+# Copyright (C) 2023 EEGsynth project
+#
+# This program is free software: you can redistribute it and/or modify
+# it under the terms of the GNU General Public License as published by
+# the Free Software Foundation, either version 3 of the License, or
+# (at your option) any later version.
+#
+# This program is distributed in the hope that it will be useful,
+# but WITHOUT ANY WARRANTY; without even the implied warranty of
+# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
+# GNU General Public License for more details.
+#
+# You should have received a copy of the GNU General Public License
+# along with this program.  If not, see <http://www.gnu.org/licenses/>.
+
 from __future__ import print_function
 
+import os
 import sys
+
+# exclude some eegsynth/module directories from the path
+for i, dir in enumerate(sys.path):
+    if dir.endswith(os.path.join('module', 'redis')):
+        del sys.path[i]
+        continue
+    if dir.endswith(os.path.join('module', 'logging')):
+        del sys.path[i]
+        continue
+
+import configparser
+import argparse
 import time
 import threading
 import math
 import numpy as np
 from scipy.signal import firwin, butter, bessel, lfilter, lfiltic, iirnotch
 import logging
 from logging import Formatter
 import colorama
+import random
+import redis          # this is NOT eegsynth/module/redis
+import ZmqRedis       # this offers an alternative to a real redis server
+import FakeRedis      # this offers an alternative to a real redis server
+import DummyRedis     # this offers an alternative to a real redis server
+import string
 import termcolor
+import platform
+import ctypes
 from termcolor import colored
 
 ###################################################################################################
-def formatkeyval(key, val):
-    if sys.version_info < (3,0):
-        # this works in Python 2, but fails in Python 3
-        isstring = isinstance(val, basestring)
-    else:
-        # this works in Python 3, but fails for unicode strings in Python 2
-        isstring = isinstance(val, str)
-    if val is None:
-        output = "%s = None" % (key)
-    elif isinstance(val, list):
-        output = "%s = %s" % (key, str(val))
-    elif isstring:
-        output = "%s = %s" % (key, val)
-    else:
-        output = "%s = %g" % (key, val)
-    return output
+class patch():
+    """Class to provide a generalized interface for patching modules using
+    command-line arguments, configuration files and Redis.
 
-###################################################################################################
-def trimquotes(option):
-    # remove leading and trailing quotation marks
-    # this is needed to include leading or trailing spaces in an ini-file option
-    if option[0]=='"':
-        option = option[1:]
-    if option[0]=='\'':
-        option = option[1:]
-    if option[-1]=='"':
-        option = option[0:-1]
-    if option[-1]=='\'':
-        option = option[0:-1]
-    return option
+    The patch is initialized like this
+      patch = EEGsynth.patch(name=<name>, path=<path>)
+    where the name and path point to the ini file. You can also
+    pass the --inifile option on the command-line.
+
+    The following method sets and publishes the value to Redis
+      patch.setvalue(key, value)
+
+    The following method gets the value (as a string) from the command-line
+    arguments or from the ini file
+      patch.get(section, item, default=None)
+
+    The following methods get the values either from the command-line
+    arguments, from the ini file or from Redis
+      patch.getfloat(section, item, multiple=False, default=None)
+      patch.getint(section, item, multiple=False, default=None)
+      patch.getstring(section, item, multiple=False, default=None)
 
-###################################################################################################
-class ColoredFormatter(Formatter):
-    """Class to format logging messages
+    The formatting of options on the command-line should be like this
+      --section-item value
+
+    The formatting of options in the ini file should be like this
+      [section]
+      item=1            this returns 1
+      item=key          get the value of the key from Redis
+    or to return multiple items the formatting should be like this
+      [section]
+      item=1-20         this returns [1,20]
+      item=1,2,3        this returns [1,2,3]
+      item=1,2,3,5-9    this returns [1,2,3,5,9], not [1,2,3,5,6,7,8,9]
+      item=key1,key2    get the value of key1 and key2 from Redis
+      item=key1,5       get the value of key1 from Redis
+      item=0,key2       get the value of key2 from Redis
     """
 
-    def __init__(self, name=None):
-        self.name = name
-        colors = list(termcolor.COLORS.keys()) # prevent RuntimeError: dictionary changed size during iteration
-        # add reverse and bright color
-        for color in colors:
-            termcolor.COLORS['reverse_'+color] = termcolor.COLORS[color]+10
-            termcolor.COLORS['bright_'+color] = termcolor.COLORS[color]+60
-        # for color in termcolor.COLORS.keys():
-        #     print(colored(color, color))
+    def __init__(self, name=None, path=None, preservecase=False):
 
-    def format(self, record):
-        colors = {
-            'CRITICAL': 'reverse_red',
-            'ERROR': 'red',
-            'WARNING': 'yellow',
-            'SUCCESS': 'green',
-            'INFO': 'cyan',
-            'DEBUG': 'bright_grey',
-            'TRACE': 'reverse_white',
-        }
-        color = colors.get(record.levelname, 'white')
-        if self.name:
-            return colored(record.levelname, color) + ': ' + self.name + ': ' + record.getMessage()
+        if not name==None and not path==None:
+            inifile = os.path.join(path, name + '.ini')
+        elif not name==None:
+            inifile = name + '.ini'
+        else:
+            inifile = None
+
+        parser = argparse.ArgumentParser()
+        parser.add_argument("-i", "--inifile", default=inifile, help="name of the configuration file")
+        parser.add_argument("--general-broker", default=None, help="general broker")
+        parser.add_argument("--general-debug", default=None, help="general debug")
+        parser.add_argument("--general-delay", default=None, help="general delay")
+        parser.add_argument("--general-logging", default=None, help="general logging")
+        args = parser.parse_args()
+
+        config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
+        if preservecase:
+            # see https://docs.python.org/3/library/configparser.html#configparser.ConfigParser.optionxform
+            config.optionxform = str
+        if 'inifile' in args and not args.inifile==None:
+            config.read(args.inifile)
+
+        # convert the command-line arguments in a dict
+        args = vars(args)
+        # remove empty items
+        args = {k:v for k,v in args.items() if v}
+
+        if 'general_broker' in args:
+            broker = args['general_broker']
+        elif config.has_option('general', 'broker'):
+            broker = config.get('general', 'broker')
+        else:
+            # set the default broker
+            if config.has_section('redis'):
+                broker = 'redis'
+            elif config.has_section('zeromq'):
+                broker = 'zeromq'
+            else:
+                broker = 'dummy'
+
+        if broker=='redis':
+            if config.has_option('redis', 'hostname'):
+                hostname = config.get('redis', 'hostname')
+            else:
+                hostname = 'localhost'
+            if config.has_option('redis', 'port'):
+                port = config.getint('redis', 'port')
+            else:
+                port = 6379
+            try:
+                r = redis.StrictRedis(host=hostname, port=port, db=0, charset='utf-8', decode_responses=True)
+                response = r.client_list()
+            except redis.ConnectionError:
+                raise RuntimeError("cannot connect to Redis server")
+
+        elif broker=='zeromq':
+            # make a connection to the specified ZeroMQ server
+            # the combination of server and client emulate a subset of redis functionality
+            if config.has_option('zeromq', 'hostname'):
+                hostname = config.get('zeromq', 'hostname')
+            else:
+                hostname = 'localhost'
+            if config.has_option('zeromq', 'port'):
+                port = config.getint('zeromq', 'port')
+            else:
+                port = 5555
+            if config.has_option('zeromq', 'timeout'):
+                timeout = config.getint('zeromq', 'timeout')
+            else:
+                timeout = 5000
+            r = ZmqRedis.client(host=hostname, port=port, timeout=timeout)
+            if not name=='redis' and not r.connect():
+                raise RuntimeError("cannot connect to ZeroMQ server")
+
+        elif broker=='fake':
+            # the fake client stores all values in a dictionary
+            r = DummyRedis.client()
+
+        elif broker=='dummy':
+            # the dummy client has all functions but does not do anything
+            r = DummyRedis.client()
+
+        else:
+            raise RuntimeError("unknown broker")
+
+        # store the command-line arguments, the configuration object that maps the ini file, and the Redis connection
+        self.args = args
+        self.config = config
+        self.redis = r              # this can be redis, zeromq, fake or dummy
+
+    ####################################################################
+    def pubsub(self):
+        return self.redis.pubsub()
+
+    ####################################################################
+    def publish(self, channel, value):
+        return self.redis.publish(channel, value)
+
+    ####################################################################
+    def get(self, section, item, default=None):
+        if section + "_" + item in self.args:
+            return self.args[section + "_" + item]
+        elif self.config.has_option(section, item):
+            return self.config.get(section, item)
         else:
-            return colored(record.levelname, color) + ': ' + record.getMessage()
+            return default
+
+    ####################################################################
+    def getfloat(self, section, item, multiple=False, default=None):
+        if section + "_" + item in self.args:
+            # get it from the command-line arguments
+            return float(self.args[section + "_" + item])
+        elif self.config.has_option(section, item) and len(self.config.get(section, item))>0:
+            # get all items from the ini file, there might be one or multiple
+            items = self.config.get(section, item)
+
+            if multiple:
+                # convert the items to a list
+                if items.find(",") > -1:
+                    separator = ","
+                elif items.find("-") > -1:
+                    separator = "-"
+                elif items.find("\t") > -1:
+                    separator = "\t"
+                else:
+                    separator = " "
+                items = squeeze(' ', items)        # remove excess whitespace
+                items = squeeze(separator, items)  # remove double separators
+                items = items.split(separator)     # split on the separator
+            else:
+                # make a list with a single item
+                items = [items]
+
+            # set the default
+            if multiple and isinstance(default, list):
+                val = [float(x) for x in default]
+            elif default != None:
+                val = [float(default)] * len(items)
+            else:
+                val = [default] * len(items)
+
+            # convert the strings into floating point values
+            for i,item in enumerate(items):
+                try:
+                    # if it resembles a value, use that
+                    val[i] = float(item)
+                except ValueError:
+                    # if it is a string, get the value from Redis
+                    try:
+                        val[i] = float(self.redis.get(item))
+                    except TypeError:
+                        pass
+        else:
+            # the configuration file does not contain the item
+            if multiple and isinstance(default, list):
+                val = [float(x) for x in default]
+            elif multiple and default == None:
+                val = []
+            elif multiple and default != None:
+                val = [float(default)]
+            elif not multiple and default == None:
+                val = default
+            elif not multiple and default != None:
+                val = float(default)
+
+        if multiple and not isinstance(val, list):
+            # return a list
+            return [val]
+        elif not multiple and isinstance(val, list):
+            # return a single value
+            return val[0]
+        else:
+            return val
+
+    ####################################################################
+    def getint(self, section, item, multiple=False, default=None):
+        if section + "_" + item in self.args:
+            return int(self.args[section + "_" + item])
+        elif self.config.has_option(section, item) and len(self.config.get(section, item))>0:
+            # get all items from the ini file, there might be one or multiple
+            items = self.config.get(section, item)
+
+            if multiple:
+                # convert the items to a list
+                if items.find(",") > -1:
+                    separator = ","
+                elif items.find("-") > -1:
+                    separator = "-"
+                elif items.find("\t") > -1:
+                    separator = "\t"
+                else:
+                    separator = " "
+                items = squeeze(' ', items)        # remove excess whitespace
+                items = squeeze(separator, items)  # remove double separators
+                items = items.split(separator)     # split on the separator
+            else:
+                # make a list with a single item
+                items = [items]
+
+            # set the default
+            if multiple and isinstance(default, list):
+                val = [int(x) for x in default]
+            elif default != None:
+                val = [int(default)] * len(items)
+            else:
+                val = [default] * len(items)
+
+            # convert the strings into integer values
+            for i,item in enumerate(items):
+                try:
+                    # if it resembles a value, use that
+                    val[i] = int(item)
+                except ValueError:
+                    # if it is a string, get the value from Redis
+                    try:
+                        val[i] = int(round(float(self.redis.get(item))))
+                    except TypeError:
+                        pass
+        else:
+            # the configuration file does not contain the item
+            if multiple and isinstance(default, list):
+                val = [int(x) for x in default]
+            elif multiple and default == None:
+                val = []
+            elif multiple and default != None:
+                val = [int(default)]
+            elif not multiple and default == None:
+                val = default
+            elif not multiple and default != None:
+                val = int(default)
+
+        if multiple and not isinstance(val, list):
+            # return a list
+            return [val]
+        elif not multiple and isinstance(val, list):
+            # return a single value
+            return val[0]
+        else:
+            return val
+
+    ####################################################################
+    def getstring(self, section, item, multiple=False, default=None):
+        if section + "_" + item in self.args:
+            return self.args[section + "_" + item]
+        else:
+            # get all items from the ini file, there might be one or multiple
+            try:
+                val = self.config.get(section, item)
+                if self.redis.exists(val):
+                    # the ini file points to a Redis key, which contains the actual value
+                    val = self.redis.get(val)
+            except:
+                val = default
+
+        if multiple:
+            if val==None or len(val)==0:
+                # convert it to an empty list
+                val = []
+            else:
+                # convert the string with items to a list
+                if val.find(",") > -1:
+                    separator = ","
+                elif val.find("-") > -1:
+                    separator = "-"
+                elif val.find("\t") > -1:
+                    separator = "\t"
+                else:
+                    separator = " "
+
+                val = squeeze(separator, val)  # remove double separators
+                val = val.split(separator)     # split on the separator
+
+        if multiple and not isinstance(val, list):
+            # return a list
+            return [val]
+        elif not multiple and isinstance(val, list):
+            # return a single value
+            return val[0]
+        else:
+            return val
+
+    ####################################################################
+    def hasitem(self, section, item):
+        # check whether an item is present on the command line or in the ini file
+        if section + "_" + item in self.args:
+            return True
+        else:
+            return self.config.has_option(section, item)
 
+    ####################################################################
+    def setvalue(self, item, val, duration=0):
+        self.redis.set(item, val)      # set it as control channel
+        self.redis.publish(item, val)  # send it as trigger
+        if duration > 0:
+            # switch off after a certain amount of time
+            threading.Timer(duration, self.setvalue, args=[item, 0.]).start()
 
 ###################################################################################################
 class monitor():
     """Class to monitor control values and print them to screen when they have changed. It also
     prints a boilerplate license upon startup.
 
     monitor.loop()           - to be called on every iteration of the loop
@@ -89,57 +402,65 @@
     monitor.warning(...)   - shows always
     monitor.success(...)   - debug level 0
     monitor.info(...)      - debug level 1
     monitor.debug(...)     - debug level 2
     monitor.trace(...)     - debug level 3
     """
 
-    def __init__(self, name=None, debug=0):
+    def __init__(self, name=None, debug=0, patch=None, target=None):
         self.previous_value = {}
         self.loop_time = None
+        self.patch = patch
+        self.target = target
 
-        # If using Windows,this  will cause anything sent to stdout or stderr will have ANSI color codes converted to the Windows versions
+        # on Windows this will cause anything with ANSI color codes sent to stdout or stderr converted to the Windows versions
         colorama.init()
 
-        logger = logging.getLogger(__name__)
-        handler = logging.StreamHandler()
-        formatter = ColoredFormatter(name)
-        handler.setFormatter(formatter)
-        logger.addHandler(handler)
+        logger = logging.getLogger(name)
+
+        if target and patch:
+            redisHandler = RedisLogger(self.patch.redis, target)
+            redisHandler.setFormatter(logging.Formatter('%(levelname)s: %(name)s: %(message)s'))
+            # '%(asctime)s - %(name)s - %(levelname)s - %(message)s'
+            logger.addHandler(redisHandler)
+        else:
+            streamHandler = logging.StreamHandler()
+            streamHandler.setFormatter(ColoredFormatter(name))
+            logger.addHandler(streamHandler)
 
         # add a success level
         logging.SUCCESS = logging.INFO + 5
         logging.addLevelName(logging.SUCCESS, 'SUCCESS')
 
         # add a trace level
         logging.TRACE = logging.DEBUG - 5
         logging.addLevelName(logging.TRACE, 'TRACE')
 
-        # remember the logger
-        self.logger = logger
-
         if debug==0:
             logger.setLevel(logging.SUCCESS)
         elif debug==1:
             logger.setLevel(logging.INFO)
         elif debug==2:
             logger.setLevel(logging.DEBUG)
         elif debug==3:
             logger.setLevel(logging.TRACE)
 
+        # remember the logger
+        self.logger = logger
+
         if name == None:
             fullname = 'This software'
         else:
             fullname = 'The %s module' % (name)
 
         print("""
 ##############################################################################
 # %s is part of EEGsynth, see <http://www.eegsynth.org>.
 #
-# Copyright (C) 2017-2022 EEGsynth project
+# Copyright (C) 2017-2023 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -150,43 +471,74 @@
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 ##############################################################################
 
 Press Ctrl-C to stop this module.
         """ % (fullname))
 
-    def loop(self, duration=None):
+    def setTarget(self, target):
+        self.target = target
+
+    def setPatch(self, patch):
+        self.patch = patch
+
+    def setLevel(self, level):
+        if level==0:
+            self.logger.setLevel(logging.SUCCESS)
+        elif level==1:
+            self.logger.setLevel(logging.INFO)
+        elif level==2:
+            self.logger.setLevel(logging.DEBUG)
+        elif level==3:
+            self.logger.setLevel(logging.TRACE)
+
+    def loop(self, feedback=1.0, duration=None):
         now = time.time()
 
         if self.loop_time is None:
             self.success("starting loop...")
             self.loop_time = now
             self.loop_count = 0
             self.loop_start = time.time()
         else:
             self.loop_count += 1
         elapsed = now - self.loop_time
-        if elapsed>=1:
+        if feedback and elapsed>=feedback:
             self.info("looping with %d iterations in %g seconds" % (self.loop_count, elapsed))
             self.loop_time = now
             self.loop_count = 0
         if duration!=None and now-self.loop_start>duration:
             raise SystemExit
 
-    def update(self, key, val):
+    def update(self, key, val, level='info'):
         if (key not in self.previous_value) or (self.previous_value[key]!=val):
             try:
                 # the comparison returns false in case both are nan
                 a = math.isnan(self.previous_value[key])
                 b = math.isnan(val)
                 if (a and b):
                     return False
             except:
                 pass
-            self.info(formatkeyval(key, val))
+
+            if level == 'critical':
+                self.critical(formatkeyval(key, val))
+            elif level == 'error':
+                self.error(formatkeyval(key, val))
+            elif level == 'warning':
+                self.warning(formatkeyval(key, val))
+            elif level == 'success':
+                self.success(formatkeyval(key, val))
+            elif level == 'info':
+                self.info(formatkeyval(key, val))
+            elif level == 'debug':
+                self.debug(formatkeyval(key, val))
+            elif level == 'trace':
+                self.trace(formatkeyval(key, val))
+
             self.previous_value[key] = val
             return True
         else:
             return False
 
     def critical(self, *args):
         if len(args)==1:
@@ -226,209 +578,60 @@
 
     def trace(self, *args):
         if len(args)==1:
             self.logger.log(logging.TRACE, *args)
         else:
             self.logger.log(logging.TRACE, " ".join(map(format, args)))
 
-###################################################################################################
-class patch():
-    """Class to provide a generalized interface for patching modules using
-    configuration files and Redis.
 
-    The formatting of the item in the ini file should be like this
-      item=1            this returns 1
-      item=key          get the value of the key from Redis
-    or if multiple is True
-      item=1-20         this returns [1,20]
-      item=1,2,3        this returns [1,2,3]
-      item=1,2,3,5-9    this returns [1,2,3,5,9], not [1,2,3,4,5,6,7,8,9]
-      item=key1,key2    get the value of key1 and key2 from Redis
-      item=key1,5       get the value of key1 from Redis
-      item=0,key2       get the value of key2 from Redis
+###################################################################################################
+class RedisLogger(logging.Handler):
+    """Class to send logging messages to Redis
     """
 
-    def __init__(self, c, r):
-        self.config = c
-        self.redis  = r
-
-    ####################################################################
-    def getfloat(self, section, item, multiple=False, default=None):
-        if self.config.has_option(section, item) and len(self.config.get(section, item))>0:
-            # get all items from the ini file, there might be one or multiple
-            items = self.config.get(section, item)
-
-            if multiple:
-                # convert the items to a list
-                if items.find(",") > -1:
-                    separator = ","
-                elif items.find("-") > -1:
-                    separator = "-"
-                elif items.find("\t") > -1:
-                    separator = "\t"
-                else:
-                    separator = " "
-                items = squeeze(' ', items)        # remove excess whitespace
-                items = squeeze(separator, items)  # remove double separators
-                items = items.split(separator)     # split on the separator
-            else:
-                # make a list with a single item
-                items = [items]
-
-            # set the default
-            if default != None:
-                val = [float(default)] * len(items)
-            else:
-                val = [default] * len(items)
-
-            # convert the strings into floating point values
-            for i,item in enumerate(items):
-                try:
-                    # if it resembles a value, use that
-                    val[i] = float(item)
-                except ValueError:
-                    # if it is a string, get the value from Redis
-                    try:
-                        val[i] = float(self.redis.get(item))
-                    except TypeError:
-                        pass
-        else:
-            # the configuration file does not contain the item
-            if multiple == True and default == None:
-                val = []
-            elif multiple == True and default != None:
-                val = [float(x) for x in default]
-            elif multiple == False and default == None:
-                val = None
-            elif multiple == False and default != None:
-                val = float(default)
-
-        if multiple:
-            # return it as list
-            return val
-        else:
-            # return a single value
-            if isinstance(val, list):
-                return val[0]
-            else:
-                return val
+    def __init__(self, server, channel):
+        super().__init__()
+        self.redis = server
+        self.channel = channel
+
+    def emit(self, record):
+        msg = self.format(record)
+        self.redis.set(self.channel, msg)
+        self.redis.publish(self.channel, msg)
 
-    ####################################################################
-    def getint(self, section, item, multiple=False, default=None):
-        if self.config.has_option(section, item) and len(self.config.get(section, item))>0:
-            # get all items from the ini file, there might be one or multiple
-            items = self.config.get(section, item)
-
-            if multiple:
-                # convert the items to a list
-                if items.find(",") > -1:
-                    separator = ","
-                elif items.find("-") > -1:
-                    separator = "-"
-                elif items.find("\t") > -1:
-                    separator = "\t"
-                else:
-                    separator = " "
-                items = squeeze(' ', items)        # remove excess whitespace
-                items = squeeze(separator, items)  # remove double separators
-                items = items.split(separator)     # split on the separator
-            else:
-                # make a list with a single item
-                items = [items]
-
-            # set the default
-            if default != None:
-                val = [int(default)] * len(items)
-            else:
-                val = [default] * len(items)
-
-            # convert the strings into integer values
-            for i,item in enumerate(items):
-                try:
-                    # if it resembles a value, use that
-                    val[i] = int(item)
-                except ValueError:
-                    # if it is a string, get the value from Redis
-                    try:
-                        val[i] = int(round(float(self.redis.get(item))))
-                    except TypeError:
-                        pass
-        else:
-            # the configuration file does not contain the item
-            if multiple == True and default == None:
-                val = []
-            elif multiple == True and default != None:
-                val = [int(x) for x in default]
-            elif multiple == False and default == None:
-                val = None
-            elif multiple == False and default != None:
-                val = int(default)
-
-        if multiple:
-            # return it as list
-            return val
-        else:
-            # return a single value
-            if isinstance(val, list):
-                return val[0]
-            else:
-                return val
-
-    ####################################################################
-    def getstring(self, section, item, default=None, multiple=False):
-        # get all items from the ini file, there might be one or multiple
-        try:
-            val = self.config.get(section, item)
-            if self.redis.exists(val):
-                # the ini file points to a Redis key, which contains the actual value
-                val = self.redis.get(val)
-        except:
-            val = default
-
-        if multiple:
-            if val==None or len(val)==0:
-                # convert it to an empty list
-                val = []
-            else:
-                # convert the string with items to a list
-                if val.find(",") > -1:
-                    separator = ","
-                elif val.find("-") > -1:
-                    separator = "-"
-                elif val.find("\t") > -1:
-                    separator = "\t"
-                else:
-                    separator = " "
+###################################################################################################
+class ColoredFormatter(Formatter):
+    """Class to format logging messages
+    """
 
-                val = squeeze(separator, val)  # remove double separators
-                val = val.split(separator)     # split on the separator
+    def __init__(self, name=None):
+        self.name = name
+        colors = list(termcolor.COLORS.keys()) # prevent RuntimeError: dictionary changed size during iteration
+        # add reverse and bright color
+        for color in colors:
+            termcolor.COLORS['reverse_'+color] = termcolor.COLORS[color]+10
+            termcolor.COLORS['bright_'+color] = termcolor.COLORS[color]+60
+        # for color in termcolor.COLORS.keys():
+        #     print(colored(color, color))
 
-        if multiple:
-            # return it as list
-            return val
+    def format(self, record):
+        colors = {
+            'CRITICAL': 'reverse_red',
+            'ERROR': 'red',
+            'WARNING': 'yellow',
+            'SUCCESS': 'green',
+            'INFO': 'cyan',
+            'DEBUG': 'bright_grey',
+            'TRACE': 'reverse_white',
+        }
+        color = colors.get(record.levelname, 'white')
+        if self.name:
+            return colored(record.levelname, color) + ': ' + self.name + ': ' + record.getMessage()
         else:
-            # return a single value
-            if isinstance(val, list):
-                return val[0]
-            else:
-                return val
-
-    ####################################################################
-    def hasitem(self, section, item):
-        # check whether an item is present in the ini file
-        return self.config.has_option(section, item)
-
-    ####################################################################
-    def setvalue(self, item, val, duration=0):
-        self.redis.set(item, val)      # set it as control channel
-        self.redis.publish(item, val)  # send it as trigger
-        if duration > 0:
-            # switch off after a certain amount of time
-            threading.Timer(duration, self.setvalue, args=[item, 0.]).start()
-
+            return colored(record.levelname, color) + ': ' + record.getMessage()
 
 ####################################################################
 def rescale(xval, slope=None, offset=None, reverse=False):
     if hasattr(xval, "__iter__"):
         return [rescale(x, slope, offset) for x in xval]
     elif xval == None:
         return None
@@ -728,7 +931,49 @@
         y2 = np.flip(y2, 1)
         y2 = lfilter(b, a, y2)
         y2 = np.flip(y2, 1)
         y2 = lfilter(b, a, y2)
         # average
         y = (y1 + y2)/2
     return y
+
+###################################################################################################
+def formatkeyval(key, val):
+    if sys.version_info < (3,0):
+        # this works in Python 2, but fails in Python 3
+        isstring = isinstance(val, basestring)
+    else:
+        # this works in Python 3, but fails for unicode strings in Python 2
+        isstring = isinstance(val, str)
+    if val is None:
+        output = "%s = None" % (key)
+    elif isinstance(val, list):
+        output = "%s = %s" % (key, str(val))
+    elif isstring:
+        output = "%s = %s" % (key, val)
+    else:
+        output = "%s = %g" % (key, val)
+    return output
+
+###################################################################################################
+def trimquotes(option):
+    # remove leading and trailing quotation marks
+    # this is needed to include leading or trailing spaces in an ini-file option
+    if option[0]=='"':
+        option = option[1:]
+    if option[0]=='\'':
+        option = option[1:]
+    if option[-1]=='"':
+        option = option[0:-1]
+    if option[-1]=='\'':
+        option = option[0:-1]
+    return option
+
+###################################################################################################
+def uuid(length):
+    return ''.join(random.choice(string.hexdigits) for i in range(length))
+
+###################################################################################################
+def appid(myappid):
+    # the icon in the taskbar should not be the python interpreter but the EEGsynth logo
+    if platform.system() == 'Windows':
+        ctypes.windll.shell32.SetCurrentProcessExplicitAppUserModelID(myappid)
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `eegsynth-0.6.0/lib/FieldTrip.py` & `eegsynth-0.7.0/lib/FieldTrip.py`

 * *Files 0% similar despite different names*

```diff
@@ -783,15 +783,15 @@
     def loop(self):
         if not self.isConnected:
             if self.keepalive:
                 print('Not connected.')
                 return
             else:
                 raise RuntimeError('Not connected.')
-                
+
         # the timeout is used to return control to the main loop once in a while
         events = self.sel.select(timeout = self.timeout)
         for key, mask in events:
             if key.data is None:
                 self.accept_wrapper(key.fileobj)
             else:
                 self.service_request(key, mask)
```

### Comparing `eegsynth-0.6.0/lib/RingBuffer.py` & `eegsynth-0.7.0/lib/RingBuffer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/lib/colormap.py` & `eegsynth-0.7.0/lib/colormap.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/module/accelerometer/__init__.py` & `eegsynth-0.7.0/module/csp/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .accelerometer import _setup, _start, _loop_once, _loop_forever, _stop
+from .csp import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/accelerometer/accelerometer.py` & `eegsynth-0.7.0/module/accelerometer/accelerometer.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -50,53 +47,40 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError('cannot connect to Redis server')
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, window, channel_items, channel_name, channel_indx, item, begsample, endsample
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success("Connected to FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, window, channel_items, channel_name, channel_indx, item, begsample, endsample
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.success("Waiting for data to arrive...")
@@ -109,15 +93,15 @@
     monitor.info(hdr_input)
     monitor.info(hdr_input.labels)
 
     # get the processing parameters
     window = patch.getfloat('processing', 'window')
     window = int(window * hdr_input.fSample)  # expressed in samples
 
-    channel_items = config.items('input')
+    channel_items = patch.config.items('input')
     channel_name = []
     channel_indx = []
     for item in channel_items:
         # channel numbers are one-offset in the ini file, zero-offset in the code
         channel_name.append(item[0])                           # the channel name
         channel_indx.append(patch.getint('input', item[0]) - 1)  # the channel number
 
@@ -125,16 +109,16 @@
     endsample = -1
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, window, channel_items, channel_name, channel_indx, item, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, window, channel_items, channel_name, channel_indx, item, begsample, endsample
     global dat, channame, chanindx, key, val
 
     hdr_input = ft_input.getHeader()
     if (hdr_input.nSamples - 1) < endsample:
         raise RuntimeError("buffer reset detected")
     if hdr_input.nSamples < window:
         # there are not yet enough samples in the buffer
@@ -160,23 +144,22 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
-
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/audio2ft/__init__.py` & `eegsynth-0.7.0/module/volcabeats/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .audio2ft import _setup, _start, _loop_once, _loop_forever, _stop
+from .volcabeats import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/audio2ft/audio2ft.py` & `eegsynth-0.7.0/module/audio2ft/audio2ft.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import pyaudio
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -51,75 +48,50 @@
 import FieldTrip
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument(
-        "-i",
-        "--inifile",
-        default=os.path.join(path, name + ".ini"),
-        help="name of the configuration file",
-    )
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=("#", ";"))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(
-            host=config.get("redis", "hostname"),
-            port=config.getint("redis", "port"),
-            db=0,
-            charset="utf-8",
-            decode_responses=True,
-        )
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug", default=1))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, device, rate, blocksize, nchans, ft_host, ft_port, ft_output, p, info, i, devinfo, stream, startfeedback, countfeedback
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug"))
-
-    # get the options from the configuration file
-    debug = patch.getint("general", "debug")
-    device = patch.getint("audio", "device")
-    rate = patch.getint("audio", "rate", default=44100)
-    blocksize = patch.getint("audio", "blocksize", default=1024)
-    nchans = patch.getint("audio", "nchans", default=2)
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, device, rate, blocksize, nchans, p, info, i, devinfo, stream, startfeedback, countfeedback
 
     try:
         ft_host = patch.getstring("fieldtrip", "hostname")
         ft_port = patch.getint("fieldtrip", "port")
         monitor.success("Trying to connect to buffer on %s:%i ..." % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success("Connected to output FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
+    # get the options from the configuration file
+    device = patch.getint("audio", "device")
+    rate = patch.getint("audio", "rate", default=44100)
+    blocksize = patch.getint("audio", "blocksize", default=1024)
+    nchans = patch.getint("audio", "nchans", default=2)
+
     monitor.info("rate = %g" % rate)
     monitor.info("nchans = %g" % nchans)
     monitor.info("blocksize = %g" % blocksize)
 
     p = pyaudio.PyAudio()
 
     monitor.info("------------------------------------------------------------------")
@@ -156,16 +128,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global startfeedback, countfeedback
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, device, rate, blocksize, nchans, p, info, i, devinfo, stream, startfeedback, countfeedback
     global start, data
 
     # measure the time that it takes
     start = time.time()
 
     # read a block of data from the audio device
     data = stream.read(blocksize)
@@ -194,23 +166,23 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global stream, p
     stream.stop_stream()
     stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/audiomixer/__init__.py` & `eegsynth-0.7.0/module/rms/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .audiomixer import _setup, _start, _loop_once, _loop_forever, _stop
+from .rms import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/audiomixer/audiomixer.py` & `eegsynth-0.7.0/module/audiomixer/audiomixer.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import pyaudio
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -62,60 +59,35 @@
     return mix
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument(
-        "-i",
-        "--inifile",
-        default=os.path.join(path, name + ".ini"),
-        help="name of the configuration file",
-    )
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=("#", ";"))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(
-            host=config.get("redis", "hostname"),
-            port=config.getint("redis", "port"),
-            db=0,
-            charset="utf-8",
-            decode_responses=True,
-        )
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug", default=1))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, delay, p, input_device, output_device, rate, blocksize, input_nchans, output_nchans, input_stream, output_stream, mix, previous
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug"))
+    global patch, name, path, monitor
+    global delay, p, input_device, output_device, rate, blocksize, input_nchans, output_nchans, input_stream, output_stream, mix, previous
 
     # get the options from the configuration file
-    debug = patch.getint("general", "debug")
     delay = patch.getfloat("general", "delay", default=0.05)
     input_device = patch.getint("input", "device")
     input_nchans = patch.getint("input", "nchans", default=2)
     rate = patch.getint("input", "rate", default=44100)
     blocksize = patch.getint("input", "blocksize", default=1024)
     output_device = patch.getint("output", "device")
     output_nchans = patch.getint("output", "nchans", default=2)
@@ -176,32 +148,32 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, delay, blocksize, input_stream, output_stream, mix, previous
+    global patch, name, path, monitor
+    global delay, blocksize, input_stream, output_stream, mix, previous
 
     now = time.time()
     if (now-previous)>delay :
         # reconstruct the mixing matrix
         mix = update_mix()
         previous = now
 
     # read a block of data from the input audio device
     input_data = input_stream.read(blocksize, exception_on_overflow=False)
-    
+
     # convert raw buffer to numpy array
     input_data = np.reshape(np.frombuffer(input_data, dtype=np.float32), (blocksize, input_nchans))
-    
+
     # apply the mixing
     output_data = np.matmul(input_data, mix, dtype=np.float32)
-    
+
     # convert numpy array to raw buffer
     output_data = output_data.tobytes()
 
     # write the block of data to the output audio device
     output_stream.write(output_data, exception_on_underflow=False)
 
 
@@ -211,25 +183,25 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global stream, p
     input_stream.stop_stream()
     output_stream.stop_stream()
     input_stream.close()
     output_stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/bitalino2ft/__init__.py` & `eegsynth-0.7.0/module/outputartnet/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .bitalino2ft import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputartnet import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/bitalino2ft/bitalino2ft.py` & `eegsynth-0.7.0/module/bitalino2ft/bitalino2ft.py`

 * *Files 14% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 from scipy import signal as sp
 from bitalino import BITalino
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -52,60 +49,35 @@
 import FieldTrip
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument(
-        "-i",
-        "--inifile",
-        default=os.path.join(path, name + ".ini"),
-        help="name of the configuration file",
-    )
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=("#", ";"))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(
-            host=config.get("redis", "hostname"),
-            port=config.getint("redis", "port"),
-            db=0,
-            charset="utf-8",
-            decode_responses=True,
-        )
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug", default=1))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global  monitor, debug, device, fsample, blocksize, channels, batterythreshold, nchans, startfeedback, countfeedback, ft_host, ft_port, ft_output, datatype, digitalOutput
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug"))
+    global patch, name, path, monitor
+    global device, fsample, blocksize, channels, batterythreshold, nchans, startfeedback, countfeedback, ft_host, ft_port, ft_output, datatype, digitalOutput
 
     # get the options from the configuration file
-    debug = patch.getint("general", "debug")
     device = patch.getstring("bitalino", "device")
     fsample = patch.getfloat("bitalino", "fsample", default=1000)
     blocksize = patch.getint("bitalino", "blocksize", default=10)
     channels = patch.getint("bitalino", "channels", multiple=True)  # these should be one-offset
     batterythreshold = patch.getint("bitalino", "batterythreshold", default=30)
 
     # switch from one-offset to zero-offset
@@ -156,16 +128,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, device, fsample, blocksize, channels, batterythreshold, nchans, startfeedback, countfeedback, ft_host, ft_port, ft_output, datatype, digitalOutput
+    global patch, name, path, monitor
+    global device, fsample, blocksize, channels, batterythreshold, nchans, startfeedback, countfeedback, ft_host, ft_port, ft_output, datatype, digitalOutput
     global start, dat
 
     # measure the time that it takes
     start = time.time()
 
     # read the selected channels from the bitalino
     dat = device.read(blocksize)
@@ -194,23 +166,23 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global device
     # Stop acquisition and close connection
     device.stop()
     device.close()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/brainflow2ft/__init__.py` & `eegsynth-0.7.0/module/outputgpio/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .brainflow2ft import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputgpio import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/brainflow2ft/brainflow2ft.py` & `eegsynth-0.7.0/module/brainflow2ft/brainflow2ft.py`

 * *Files 9% similar despite different names*

```diff
@@ -15,29 +15,26 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
-import redis
 import os
 import sys
 import time
 
 import brainflow
 from brainflow.board_shim import BoardShim, BrainFlowInputParams
 from brainflow.data_filter import DataFilter, FilterTypes, AggOperations
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -53,72 +50,47 @@
 import EEGsynth
 import FieldTrip
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument(
-        "-i",
-        "--inifile",
-        default=os.path.join(path, name + ".ini"),
-        help="name of the configuration file",
-    )
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=("#", ";"))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(
-            host=config.get("redis", "hostname"),
-            port=config.getint("redis", "port"),
-            db=0,
-            charset="utf-8",
-            decode_responses=True,
-        )
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug", default=1))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, delay, ft_host, ft_port, ft_output, board_id, streamer_params, params, board
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug"))
-
-    # get the general options from the configuration file
-    debug = patch.getint("general", "debug")
-    delay = patch.getfloat("general", "delay")
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, delay, board_id, streamer_params, params, board
 
     try:
         ft_host = patch.getstring("fieldtrip", "hostname")
         ft_port = patch.getint("fieldtrip", "port")
         monitor.success("Trying to connect to buffer on %s:%i ..." % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success("Connected to output FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
+    # get the general options from the configuration file
+    delay = patch.getfloat("general", "delay")
+
     # get the options that are specific for BrainFlow
     board_id             = patch.getint("brainflow", "board_id", default=-1)
     streamer_params      = patch.getstring("brainflow", "streamer_params", default=None)
     params               = BrainFlowInputParams()
     params.ip_port       = patch.getint("brainflow", "ip_port", default=0)
     params.serial_port   = patch.getstring("brainflow", "serial_port", default="/dev/cu.usbmodem11")
     params.mac_address   = patch.getstring("brainflow", "mac_address", default="")
@@ -134,15 +106,15 @@
     BoardShim.disable_board_logger()
     # BoardShim.enable_board_logger()
     # BoardShim.enable_dev_board_logger()
 
     board = BoardShim(board_id, params)
     board.prepare_session()
     board.start_stream(45000, streamer_params)
-    
+
     # get all data and remove it from internal buffer
     board.get_board_data()
 
     monitor.success("Connected to " + board.get_device_name(board_id))
     monitor.info("fsample =", board.get_sampling_rate(board_id))
     monitor.info("nchans  =", board.get_num_rows(board_id))
 
@@ -153,17 +125,18 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, delay, ft_output, board, data
-    
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, delay, board_id, streamer_params, params, board
+    global data
+
     if board.get_board_data_count()>0:
         data = np.transpose(board.get_board_data())
         ft_output.putData(data.astype(np.float32))
         monitor.debug("wrote " + str(len(data[:,1])) + " samples")
     else:
         # wait for a short time before trying again
         time.sleep(delay)
@@ -179,22 +152,22 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global board
     board.stop_stream()
     board.release_session()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/buffer/__init__.py` & `eegsynth-0.7.0/module/buffer/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/buffer/buffer.py` & `eegsynth-0.7.0/module/buffer/buffer.py`

 * *Files 16% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import threading
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -50,57 +47,43 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, delay, port, server
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, port, server
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     delay = patch.getfloat('general', 'delay', default=0.010)
     port = patch.getint('fieldtrip', 'port', multiple=True)
-    
+
     server = []
     for p in port:
         monitor.info("starting server on %d" % p)
         s = FieldTrip.Server()
         s.connect(hostname='localhost', port=p)
         s.timeout = 0 # the server main loop should not wait, as it would block the other instances
         server.append(s);
     del p, s
-        
+
 
 def _loop_once():
     '''Run the main loop once
     '''
     global server
     for s in server:
         s.loop() # deal with new connections and incoming requests
@@ -113,22 +96,22 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(delay)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, server
     for s in server:
         s.disconnect()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/clockdivider/__init__.py` & `eegsynth-0.7.0/module/outputzeromq/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .clockdivider import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputzeromq import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/clockdivider/clockdivider.py` & `eegsynth-0.7.0/module/clockdivider/clockdivider.py`

 * *Files 11% similar despite different names*

```diff
@@ -13,25 +13,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -56,15 +53,15 @@
         self.count = 0
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         global count
         # this message unblocks the Redis listen command
         pubsub.subscribe('CLOCKDIVIDER_UNBLOCK')
         # this message triggers the event
         pubsub.subscribe(self.redischannel)
         while self.running:
             for item in pubsub.listen():
@@ -78,49 +75,35 @@
                         patch.setvalue(self.key, val)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, channels, dividers, count, triggers, channel, divider, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global channels, dividers, count, triggers, channel, divider, thread
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     channels = patch.getstring('clock', 'channel', multiple=True)
     dividers = patch.getint('clock', 'rate', multiple=True)
 
     # keep track of the number of received triggers
     count = 0
 
     triggers = []
@@ -138,16 +121,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, channels, dividers, count, triggers, channel, divider, thread
+    global patch, name, path, monitor
+    global channels, dividers, count, triggers, channel, divider, thread
 
     monitor.update("count", count / len(dividers))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
@@ -165,20 +148,20 @@
 def _stop():
     '''Stop and clean up and stop on SystemExit, KeyboardInterrupt
     '''
     global monitor, triggers, r
     monitor.success('Closing threads')
     for thread in triggers:
         thread.stop()
-    r.publish('CLOCKDIVIDER_UNBLOCK', 1)
+    patch.publish('CLOCKDIVIDER_UNBLOCK', 1)
     for thread in triggers:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/clockmultiplier/__init__.py` & `eegsynth-0.7.0/module/outputmqtt/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .clockmultiplier import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputmqtt import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/clockmultiplier/clockmultiplier.py` & `eegsynth-0.7.0/module/clockmultiplier/clockmultiplier.py`

 * *Files 10% similar despite different names*

```diff
@@ -13,25 +13,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -65,15 +62,15 @@
             t.cancel()
         self.timer = []
         self.running = False
 
     def run(self):
         global count
         global interval
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         # this message unblocks the Redis listen command
         pubsub.subscribe('CLOCKMULTIPLIER_UNBLOCK')
         # this message triggers the event
         pubsub.subscribe(self.redischannel)
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
@@ -114,49 +111,35 @@
                         self.timer.append(t)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, channels, multipliers, lrate, count, triggers, channel, multiplier, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global channels, multipliers, lrate, count, triggers, channel, multiplier, thread
 
     # get the options from the configuration file
-    debug       = patch.getint('general', 'debug')
     channels    = patch.getstring('clock', 'channel', multiple=True)
     multipliers = patch.getint('clock', 'rate',  multiple=True)
     lrate       = patch.getfloat('clock', 'learning_rate', default=1)
 
     # for keeping track of the number of received triggers
     count = 0
 
@@ -175,16 +158,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, channels, multipliers, lrate, count, triggers, channel, multiplier, thread
+    global patch, name, path, monitor
+    global channels, multipliers, lrate, count, triggers, channel, multiplier, thread
 
     monitor.update("count", count / len(multipliers))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
@@ -196,27 +179,27 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(1)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, triggers, r
 
     monitor.success('Closing threads')
     for thread in triggers:
         thread.stop()
-    r.publish('CLOCKMULTIPLIER_UNBLOCK', 1)
+    patch.publish('CLOCKMULTIPLIER_UNBLOCK', 1)
     for thread in triggers:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/cogito/__init__.py` & `eegsynth-0.7.0/module/demodulatetone/__init__.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .cogito import _setup, _start, _loop_once, _loop_forever, _stop
+from .demodulatetone import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/cogito/cogito.py` & `eegsynth-0.7.0/module/cogito/cogito.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,30 +17,27 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from __future__ import print_function
 
-import configparser
-import argparse
 import numpy as np
 import os
 import sys
 import time
-import redis
 from copy import copy
 
 # Pandas is a rather large Python package with a lot of extra dependencies.
 # It is only used inside this specific EEGsynth module, hence it might not be installed by default
 import pandas as pd
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -57,37 +54,29 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
-
-    # get the options from the configuration file
-    debug   = patch.getint('general', 'debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, input_number, input_channel, output_number, output_channel, nInputs, number, channel, nOutputs, tmp, sample_rate, window, f_min, f_max, f_offset, scaling, polyorder, profileMin, profileMax, profileCorrection, layout, definition, val, positions, inputscaling, outputscaling, begsample, endsample
 
     try:
         ft_host = patch.getstring('input_fieldtrip', 'hostname')
         ft_port = patch.getint('input_fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
@@ -101,22 +90,14 @@
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success('Connected to output FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output, name
-    global timeout, hdr_input, start, input_number, input_channel, output_number, output_channel, nInputs, number, channel, nOutputs, tmp, sample_rate, window, f_min, f_max, f_offset, scaling, polyorder, profileMin, profileMax, profileCorrection, layout, definition, val, positions, inputscaling, outputscaling, begsample, endsample
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('input_fieldtrip','timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
@@ -126,16 +107,16 @@
         hdr_input = ft_input.getHeader()
 
     monitor.info('Data arrived')
     monitor.debug(hdr_input)
     monitor.debug(hdr_input.labels)
 
     # get the input and output options
-    input_number, input_channel = list(map(list, list(zip(*config.items('input_channel')))))
-    output_number, output_channel = list(map(list, list(zip(*config.items('output_channel')))))
+    input_number, input_channel = list(map(list, list(zip(*patch.config.items('input_channel')))))
+    output_number, output_channel = list(map(list, list(zip(*patch.config.items('output_channel')))))
 
     # convert to integer and make the indices zero-offset
     input_number = [int(number)-1 for number in input_number]
     output_number = [int(number)-1 for number in output_number]
 
     # ensure that all input channels have a label
     nInputs = hdr_input.nChannels
@@ -157,21 +138,20 @@
     for number, channel in zip(output_number, output_channel):
         tmp[number] = channel
 
     # update the output channel specification
     output_number = list(range(nOutputs))
     output_channel = tmp
 
-    if debug > 0:
-        monitor.info('===== input channels =====')
-        for number, channel in zip(input_number, input_channel):
-            monitor.info(str(number) + ' = ' + channel)
-        monitor.info('===== output channels =====')
-        for number, channel in zip(output_number, output_channel):
-            monitor.info(str(number) + ' = ' + channel)
+    monitor.info('===== input channels =====')
+    for number, channel in zip(input_number, input_channel):
+        monitor.info(str(number) + ' = ' + channel)
+    monitor.info('===== output channels =====')
+    for number, channel in zip(output_number, output_channel):
+        monitor.info(str(number) + ' = ' + channel)
 
     sample_rate         = patch.getfloat('cogito', 'sample_rate')
     window              = patch.getfloat('cogito', 'window')
     f_min               = patch.getfloat('cogito', 'f_min')
     f_max               = patch.getfloat('cogito', 'f_max')
     f_offset            = patch.getfloat('cogito', 'f_offset')
     scaling             = patch.getfloat('cogito', 'scaling')
@@ -210,16 +190,16 @@
         endsample = hdr_input.nSamples-1
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
-    global timeout, hdr_input, start, input_number, input_channel, output_number, output_channel, nInputs, number, channel, nOutputs, tmp, sample_rate, window, f_min, f_max, f_offset, scaling, polyorder, profileMin, profileMax, profileCorrection, layout, definition, val, positions, inputscaling, outputscaling, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, input_number, input_channel, output_number, output_channel, nInputs, number, channel, nOutputs, tmp, sample_rate, window, f_min, f_max, f_offset, scaling, polyorder, profileMin, profileMax, profileCorrection, layout, definition, val, positions, inputscaling, outputscaling, begsample, endsample
     global dat_input, tmpvar, ch, chan_time, original, t, fourier, mask, convert, signal_time, signal, dat_output, write_time
 
     # determine when we start polling for available data
     start = time.time()
 
     while endsample>hdr_input.nSamples-1:
         # wait until there is enough data
@@ -319,24 +299,24 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input, ft_output
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
     ft_output.disconnect()
     monitor.success('Disconnected from output FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/cogito/gtec2wav.py` & `eegsynth-0.7.0/module/cogito/gtec2wav.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.6.0/module/complexity/__init__.py` & `eegsynth-0.7.0/module/slewlimiter/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .complexity import _setup, _start, _loop_once, _loop_forever, _stop
+from .slewlimiter import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/complexity/complexity.py` & `eegsynth-0.7.0/module/complexity/complexity.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,32 +15,29 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import math
 import multiprocessing
 import numpy as np
 import os
-import redis
 import sys
 import threading
 import time
 
 # Neurokit is a rather large Python package with a lot of extra dependencies.
 # It is only used inside this specific EEGsynth module, hence it might not be installed by default
 from neurokit.signal import complexity
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -57,56 +54,40 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
 
-    # get the options from the configuration file
-    debug = patch.getint('general','debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, shannon, sampen, multiscale, spectral, svd, correlation, higushi, petrosian, fisher, hurst, dfa, lyap_r, lyap_e, window, taper, begsample, endsample
 
     try:
-        ft_host = patch.getstring('fieldtrip','hostname')
-        ft_port = patch.getint('fieldtrip','port')
+        ft_host = patch.getstring('fieldtrip', 'hostname')
+        ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, shannon, sampen, multiscale, spectral, svd, correlation, higushi, petrosian, fisher, hurst, dfa, lyap_r, lyap_e, window, taper, begsample, endsample
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
@@ -115,15 +96,15 @@
         time.sleep(0.1)
         hdr_input = ft_input.getHeader()
 
     monitor.info('Data arrived')
     monitor.debug(hdr_input)
     monitor.debug(hdr_input.labels)
 
-    channel_items = config.items('input')
+    channel_items = patch.config.items('input')
     channame = []
     chanindx = []
     for item in channel_items:
         # channel numbers are one-offset in the ini file, zero-offset in the code
         channame.append(item[0])
         chanindx.append(patch.getint('input', item[0])-1)
 
@@ -153,16 +134,16 @@
     endsample = -1
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, shannon, sampen, multiscale, spectral, svd, correlation, higushi, petrosian, fisher, hurst, dfa, lyap_r, lyap_e, window, taper, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, shannon, sampen, multiscale, spectral, svd, correlation, higushi, petrosian, fisher, hurst, dfa, lyap_r, lyap_e, window, taper, begsample, endsample
     global dat, meandat, chan, sample, metrics, timeseries, metric_names, metric, shortmetric, key, val
 
     hdr_input = ft_input.getHeader()
     if (hdr_input.nSamples - 1) < endsample:
         raise RuntimeError("buffer reset detected")
     if hdr_input.nSamples < window:
         # there are not yet enough samples in the buffer
@@ -225,22 +206,22 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/compressor/__init__.py` & `eegsynth-0.7.0/module/launchcontrol/__init__.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .compressor import _setup, _start, _loop_once, _loop_forever, _stop
+from .launchcontrol import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/compressor/compressor.py` & `eegsynth-0.7.0/module/compressor/compressor.py`

 * *Files 7% similar despite different names*

```diff
@@ -15,24 +15,21 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -48,69 +45,55 @@
 import EEGsynth
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, delay, prefix, input_name, input_variable
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, prefix, input_name, input_variable
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     delay = patch.getfloat('general', 'delay')
     prefix = patch.getstring('output', 'prefix')
 
     # get the input options
-    input_name, input_variable = list(zip(*config.items('input')))
+    input_name, input_variable = list(zip(*patch.config.items('input')))
 
     for name, variable in zip(input_name, input_variable):
         monitor.info("%s = %s" % (name, variable))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, delay, prefix, input_name, input_variable
+    global patch, name, path, monitor
+    global delay, prefix, input_name, input_variable
 
     if patch.getint('processing', 'enable', default=1):
         # the compressor/expander applies to all channels and must exist as float or redis key
         scale = patch.getfloat('scale', 'lo', default=1.)
         offset = patch.getfloat('offset', 'lo', default=0.)
         lo = patch.getfloat('processing', 'lo')
         lo = EEGsynth.rescale(lo, slope=scale, offset=offset)
@@ -151,19 +134,20 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
-    sys.exit()
+    pass
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/csp/__init__.py` & `eegsynth-0.7.0/module/brainflow2ft/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .csp import _setup, _start, _loop_once, _loop_forever, _stop
+from .brainflow2ft import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/csp/csp.py` & `eegsynth-0.7.0/module/csp/csp.py`

 * *Files 6% similar despite different names*

```diff
@@ -21,34 +21,31 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import wave
 import struct
 import glob
 import scipy.linalg as la
 import scipy.signal as signal
 import matplotlib.pyplot as plt
 import matplotlib.colors as colors
 from matplotlib import cm
 from mpl_toolkits.axes_grid1 import make_axes_locatable # part of matplotlib
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -66,52 +63,39 @@
 import EDF
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument('-i', '--inifile', default=os.path.join(path, name + '.ini'), help='name of the configuration file')
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError('cannot connect to Redis server')
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, stepsize, filename, fileformat
+    global patch, name, path, monitor
+    global stepsize, filename, fileformat
     global data_A, filepath_A
     global data_B, filepath_B
     global scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filtorder, scale_notchquality, offset_filtorder, offset_notchquality
     global lpfreq, hpfreq, filtorder, hp, lp
     global filenames, indx, filenr, filename, f, data, chanindx, filters, cmap, fig, axes, i, ax, im, divider, cax, prefix, icomp, comp, iweight, weight, key
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
     # get the options from the configuration file
     stepsize   = patch.getfloat('general', 'delay')
     filepath_A = patch.getstring('data', 'conditionA')
     filepath_B = patch.getstring('data', 'conditionB')
     fileformat = patch.getstring('data', 'format')
 
     if fileformat is None:
@@ -128,16 +112,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, H, A
+    global patch, name, path, monitor
+    global H, A
     global D, stepsize
     global data_A, filepath_A
     global data_B, filepath_B
     global scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filtorder, scale_notchquality, offset_filtorder, offset_notchquality
     global nChannels, fSample, nSamples, labels
     global lpfreq, hpfreq, filtorder, hp, lp
     global filenames, indx, filenr, filename, f, data, chanindx, filters, cmap, fig, axes, i, ax, im, divider, cax, prefix, icomp, comp, iweight, weight, key
@@ -199,28 +183,28 @@
 
                 f.close()
 
     else:
         raise NotImplementedError('unsupported file format')
 
     # plot timecourses for debugging
-    if patch.getint('general', 'debug') == 3:
+    if patch.getint('general', 'debug', default=1) == 3:
         for filenr, filename in enumerate(filenames):
             fig = plt.figure(filenr+1)
             for chanindx in range(nChannels[0]):
                 print('file nr. %d channel nr. %d' % (filenr, chanindx))
                 plt.subplot(8, 1, chanindx+1)
                 plt.plot(data[filenr][chanindx, :])
             plt.show()
 
     # calculate CSP
     filters = CSP(data[indx==0], data[indx==1])
 
     # plot CSP when debugging
-    if patch.getint('general', 'debug') == 3:
+    if patch.getint('general', 'debug', default=1) == 3:
         cmap = cm.coolwarm
         fig, axes = plt.subplots(1,2, figsize=(8,8))
         for i, ax in enumerate(axes.flat):
             im = ax.imshow(filters[i], norm=colors.CenteredNorm(0), cmap = cmap)
             # pc = ax.imshow(filters[i])
             # plt.colorbar(pc, ax=ax)
             divider = make_axes_locatable(ax)
@@ -260,17 +244,17 @@
         elapsed = time.time() - start
         naptime = stepsize - elapsed
         if naptime > 0:
             # this approximates the real time streaming speed
             time.sleep(naptime)
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 def CSP(*tasks):
     if len(tasks) < 2:
         print("Must have at least 2 tasks for filtering.")
         return (None,) * len(tasks)
     else:
@@ -344,7 +328,8 @@
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/delaytrigger/__init__.py` & `eegsynth-0.7.0/module/recordcontrol/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .delaytrigger import _setup, _start, _loop_once, _loop_forever, _stop
+from .recordcontrol import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+    
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/delaytrigger/delaytrigger.py` & `eegsynth-0.7.0/module/delaytrigger/delaytrigger.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import threading
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -64,16 +61,16 @@
         monitor.debug('flushing %d timers' % len(self.timer))
         for t in self.timer:
             t.cancel()
         self.timer = []
         self.running = False
 
     def run(self):
-        global r, monitor, lock
-        pubsub = r.pubsub()
+        global patch, name, path, monitor, lock
+        pubsub = patch.pubsub()
         pubsub.subscribe('DELAYTRIGGER_UNBLOCK')   # this message unblocks the Redis listen command
         pubsub.subscribe(self.redischannel)        # this message triggers the event
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -89,54 +86,38 @@
                     self.timer.append(t)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, prefix, item, val, input_name, input_variable, output_name, output_variable, lock, trigger, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    global patch, name, path, monitor
+    global prefix, item, val, input_name, input_variable, output_name, output_variable, lock, trigger, thread
 
     # create the background threads that deal with the input triggers
     trigger = []
     monitor.debug("Setting up threads")
-    for item in config.items('input'):
+    for item in patch.config.items('input'):
         input = item[1]
         delay = patch.getfloat("delay", item[0])
         output = patch.getstring("output", item[0])
         value = patch.getfloat("value", item[0]) # when not specified this will return None
         monitor.info(input, '->', delay, '->', output)
         trigger.append(TriggerThread(input, delay, output, value))
 
@@ -154,32 +135,33 @@
     '''
     pass
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
+    global monitor, patch
     while True:
         monitor.loop()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('DELAYTRIGGER_UNBLOCK', 1)
+    patch.publish('DELAYTRIGGER_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/demodulatetone/__init__.py` & `eegsynth-0.7.0/module/outputdmx/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .demodulatetone import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputdmx import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/demodulatetone/demodulatetone.py` & `eegsynth-0.7.0/module/demodulatetone/demodulatetone.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import pyaudio
 
 if hasattr(sys, "frozen"):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__" and sys.argv[0] != "":
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == "__main__":
     path = os.path.abspath("")
@@ -51,60 +48,35 @@
 import FieldTrip
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument(
-        "-i",
-        "--inifile",
-        default=os.path.join(path, name + ".ini"),
-        help="name of the configuration file",
-    )
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=("#", ";"))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(
-            host=config.get("redis", "hostname"),
-            port=config.getint("redis", "port"),
-            db=0,
-            charset="utf-8",
-            decode_responses=True,
-        )
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug", default=1))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, device, rate, blocksize, modulation, nchans, frequencies, ntones, scale_amplitude, offset_amplitude, scale_frequency, offset_frequency,key, p, info, i, devinfo, stream, startfeedback, countfeedback, offset
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint("general", "debug"))
+    global patch, name, path, monitor
+    global device, rate, blocksize, modulation, nchans, frequencies, ntones, scale_amplitude, offset_amplitude, scale_frequency, offset_frequency,key, p, info, i, devinfo, stream, startfeedback, countfeedback, offset
 
     # get the options from the configuration file
-    debug = patch.getint("general", "debug")
     device = patch.getint("audio", "device")
     rate = patch.getint("audio", "rate", default=44100)
     nchans = patch.getint("audio", "nchans", default=2)
     blocksize = patch.getint("audio", "blocksize", default=1024)
     modulation = patch.getstring('audio', 'modulation', default='am')
     frequencies = patch.getfloat('audio', 'frequencies', multiple=True)
 
@@ -125,21 +97,21 @@
     channame = ['left', 'right', 'chan3', 'chan4', 'chan5', 'chan6', 'chan7', 'chan8']
     key = []
     for chan in range(0, nchans):
         key.append([])
         for tone in range(0, ntones):
             tonestr = "tone%d" % (tone + 1)
             if patch.hasitem(channame[chan], tonestr):
-                redischannel = patch.getstring(channame[chan], tonestr)
+                redischannel = patch.get(channame[chan], tonestr)
                 key[chan].append(redischannel)
                 monitor.info("configured " + channame[chan] + " " + tonestr + " as " + redischannel)
             else:
                 key[chan].append(None)
                 monitor.info("not configured " + channame[chan] + " " + tonestr)
-                
+
     p = pyaudio.PyAudio()
 
     monitor.info("------------------------------------------------------------------")
     info = p.get_host_api_info_by_index(0)
     monitor.info(info)
     monitor.info("------------------------------------------------------------------")
     for i in range(info.get("deviceCount")):
@@ -171,15 +143,15 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
     global rate, nchans, blocksize, frequencies, modulation, ntones, offset, startfeedback, countfeedback
     global start, data, chan, timeaxis, tone, phase, value, Fsin, Fcos, chanval
 
     # measure the time that it takes
     start = time.time()
 
     # read a block of data from the audio device and convert raw buffer to numpy array
@@ -236,23 +208,23 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global stream, p
     stream.stop_stream()
     stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/endorphines/__init__.py` & `eegsynth-0.7.0/module/cogito/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .endorphines import _setup, _start, _loop_once, _loop_forever, _stop
+from .cogito import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/endorphines/endorphines.py` & `eegsynth-0.7.0/module/endorphines/endorphines.py`

 * *Files 7% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -58,15 +55,15 @@
         self.midichannel = midichannel
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('ENDORPHINES_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)      # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -83,49 +80,35 @@
                     time.sleep(patch.getfloat('general', 'pulselength'))
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, mididevice, outputport, lock, trigger, port, channel, previous_val, previous_port_val
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global mididevice, outputport, lock, trigger, port, channel, previous_val, previous_port_val
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     mididevice = patch.getstring('midi', 'device')
     mididevice = EEGsynth.trimquotes(mididevice)
     mididevice = process.extractOne(mididevice, mido.get_output_names())[0]  # select the closest match
 
     # this is only for debugging, check which MIDI devices are accessible
     monitor.info('------ OUTPUT ------')
     for port in mido.get_output_names():
@@ -143,18 +126,18 @@
 
     # each of the gates that can be triggered is mapped onto a different message
     trigger = []
     for channel in range(0, 16):
 
         # channels are one-offset in the ini file, zero-offset in the code
         name = 'channel{}'.format(channel + 1)
-        if config.has_option('gate', name):
+        if patch.config.has_option('gate', name):
 
             # start the background thread that deals with this channel
-            this = TriggerThread(patch.getstring('gate', name), channel)
+            this = TriggerThread(patch.get('gate', name), channel)
             trigger.append(this)
             monitor.debug(name + ' trigger configured')
 
     # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
@@ -171,16 +154,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, mididevice, outputport, lock, trigger, port, channel, previous_val, previous_port_val
+    global patch, name, path, monitor
+    global mididevice, outputport, lock, trigger, port, channel, previous_val, previous_port_val
     global name, val, port_val, scale, offset, midichannel, msg
 
     # loop over the control values
     for channel in range(0, 16):
         # channels are one-offset in the ini file, zero-offset in the code
         name = 'channel{}'.format(channel + 1)
         val = patch.getfloat('control', name)
@@ -265,26 +248,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('ENDORPHINES_UNBLOCK', 1)
+    patch.publish('ENDORPHINES_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/example/__init__.py` & `eegsynth-0.7.0/module/example/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/example/example.py` & `eegsynth-0.7.0/module/example/example.py`

 * *Files 14% similar despite different names*

```diff
@@ -15,24 +15,21 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -48,91 +45,80 @@
 import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, prefix, param1, param2
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global prefix, param1, param2
 
     # get the options from the configuration file
     prefix = patch.getstring('output', 'prefix')
     param1 = patch.getfloat('input', 'param1', default=0)
     param2 = patch.getfloat('input', 'param2', default=0)
-    
+
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     '''
-    global parser, args, config, r, response, patch
-    global monitor, prefix
+    global patch, name, path, monitor
+    global prefix, param1, param2
 
     # update the value of input param1, copy it to the output
     param1 = patch.getfloat('input', 'param1', default=0)
     patch.setvalue(prefix + 'param1', param1)
 
     # update the value of input param2, copy it to the output
     param2 = patch.getfloat('input', 'param2', default=0)
     patch.setvalue(prefix + 'param2', param2)
 
     monitor.info('param1', param1)  # this is printed when debug>=1
     monitor.debug('param2', param2) # this is printed when debug>=2
+    monitor.trace('param2', param2) # this is printed when debug>=3
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/generateclock/__init__.py` & `eegsynth-0.7.0/module/inputosc/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .generateclock import _setup, _start, _loop_once, _loop_forever, _stop
+from .inputosc import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/generateclock/generateclock.py` & `eegsynth-0.7.0/module/generateclock/generateclock.py`

 * *Files 9% similar despite different names*

```diff
@@ -13,29 +13,26 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import math
 import mido
 from fuzzywuzzy import process
 import numpy as np
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -158,46 +155,33 @@
                 time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, stepsize, scale_rate, offset_rate, scale_shift, offset_shift, scale_ppqn, offset_ppqn, lock, clock, i, clockthread, midithread, redisthread, midiport, previous_midi_play, previous_midi_start, previous_redis_play
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global stepsize, scale_rate, offset_rate, scale_shift, offset_shift, scale_ppqn, offset_ppqn, lock, clock, i, clockthread, midithread, redisthread, midiport, previous_midi_play, previous_midi_start, previous_redis_play
 
     # get the options from the configuration file
     stepsize = patch.getfloat('general', 'delay')
 
     # the scale and offset are used to map the Redis values to internal values
     scale_rate = patch.getfloat('scale', 'rate')
     offset_rate = patch.getfloat('offset', 'rate')
@@ -238,16 +222,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, stepsize, scale_rate, offset_rate, scale_shift, offset_shift, scale_ppqn, offset_ppqn, lock, clock, i, clockthread, midithread, redisthread, midiport, previous_midi_play, previous_midi_start, previous_redis_play
+    global patch, name, path, monitor
+    global stepsize, scale_rate, offset_rate, scale_shift, offset_shift, scale_ppqn, offset_ppqn, lock, clock, i, clockthread, midithread, redisthread, midiport, previous_midi_play, previous_midi_start, previous_redis_play
     global start, redis_play, midi_play, midi_start, rate, shift, ppqn, elapsed, naptime
 
     redis_play = patch.getint('redis', 'play')
     midi_play = patch.getint('midi', 'play')
     midi_start = patch.getint('midi', 'start')
 
     if previous_redis_play is None and redis_play is not None:
@@ -261,15 +245,15 @@
 
     # the MIDI port should only be opened once, and only if needed
     if midi_play and midiport == None:
         mididevice = patch.getstring('midi', 'device')
         mididevice = EEGsynth.trimquotes(mididevice)
         mididevice = process.extractOne(mididevice, mido.get_output_names())[0]  # select the closest match
         try:
-            outputport = mido.open_output(mididevice)
+            midiport = mido.open_output(mididevice)
             monitor.success('Connected to MIDI output')
         except:
             raise RuntimeError("cannot connect to MIDI output")
 
     # do something whenever the value changes
     if redis_play and not previous_redis_play:
         redisthread.setEnabled(True)
@@ -317,23 +301,19 @@
     monitor.update("ppqn",          ppqn)
 
     # update the clock and redis
     clockthread.setRate(rate)
     redisthread.setShift(shift)
     redisthread.setPpqn(ppqn)
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print("LOCALS: " + ", ".join(locals().keys()))
-
 
 def _loop_forever():
     """Run the main loop forever
     """
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -342,28 +322,28 @@
         naptime = stepsize - elapsed
         if naptime > 0:
             monitor.trace("naptime = " + str(naptime))
             time.sleep(naptime)
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
     global monitor, midithread, redisthread, clockthread
     monitor.success('Closing threads')
     # the thread that manages the clock should be stopped the last
     midithread.stop()
     midithread.join()
     redisthread.stop()
     redisthread.join()
     clockthread.stop()
     clockthread.join()
-    sys.exit()
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/generatecontrol/__init__.py` & `eegsynth-0.7.0/module/historycontrol/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .generatecontrol import _setup, _start, _loop_once, _loop_forever, _stop
+from .historycontrol import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/generatecontrol/generatecontrol.py` & `eegsynth-0.7.0/module/generatecontrol/generatecontrol.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 from scipy import signal
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -49,46 +46,33 @@
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, stepsize, scale_frequency, scale_spread, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_spread, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, sample, phase
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global stepsize, scale_frequency, scale_spread, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_spread, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, sample, phase
 
     # get the options from the configuration file
     stepsize = patch.getfloat('generate', 'stepsize')  # in seconds
 
     # the scale and offset are used to map the Redis values to internal values
     scale_frequency = patch.getfloat('scale', 'frequency', default=1)
     scale_spread = patch.getfloat('scale', 'spread', default=1)
@@ -112,16 +96,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, stepsize, scale_frequency, scale_spread, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_spread, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, sample, phase
+    global patch, name, path, monitor
+    global stepsize, scale_frequency, scale_spread, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_spread, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, sample, phase
     global frequency, spread, amplitude, offset, noise, dutycycle, key, val, elapsed, naptime
 
     if patch.getint('signal', 'rewind', default=0):
         monitor.info("Rewind pressed, jumping back to start of signal")
         # the sample number and phase should be 0 upon the start of the signal
         sample = 0
         phase = 0
@@ -190,15 +174,15 @@
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_forever():
     """Run the main loop forever
     """
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -206,21 +190,20 @@
         elapsed = time.time() - start
         naptime = stepsize - elapsed
         if naptime > 0:
             # this approximates the real time streaming speed
             time.sleep(naptime)
 
 
-
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
-    sys.exit()
-
+    pass
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/generatesignal/__init__.py` & `eegsynth-0.7.0/module/inputmqtt/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .generatesignal import _setup, _start, _loop_once, _loop_forever, _stop
+from .inputmqtt import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -17,9 +17,11 @@
             try:
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
-                _stop()
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/generatesignal/generatesignal.py` & `eegsynth-0.7.0/module/generatesignal/generatesignal.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 from scipy import signal as sp
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -51,60 +48,44 @@
 import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_output
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print("LOCALS: " + ", ".join(locals().keys()))
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, nchannels, fsample, shape, scale_frequency, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, blocksize, datatype, block, begsample, endsample, stepsize, timevec, phasevec
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success('Connected to output FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print("LOCALS: " + ", ".join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_output, name
-    global nchannels, fsample, shape, scale_frequency, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, blocksize, datatype, block, begsample, endsample, stepsize, timevec, phasevec
-
     # get the options from the configuration file
     nchannels = patch.getint('generate', 'nchannels')
     fsample = patch.getfloat('generate', 'fsample')
     # sin, square, triangle, sawtooth or dc
     shape = patch.getstring('signal', 'shape')
 
     # the scale and offset are used to map the Redis values to internal values
@@ -157,16 +138,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_output
-    global nchannels, fsample, shape, scale_frequency, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, blocksize, datatype, block, begsample, endsample, stepsize, timevec, phasevec
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, nchannels, fsample, shape, scale_frequency, scale_amplitude, scale_offset, scale_noise, scale_dutycycle, offset_frequency, offset_amplitude, offset_offset, offset_noise, offset_dutycycle, blocksize, datatype, block, begsample, endsample, stepsize, timevec, phasevec
     global start, frequency, amplitude, offset, noise, dutycycle, signal, dat_output, chan, elapsed, naptime
 
     if patch.getint('signal', 'rewind', default=0):
         monitor.info("Rewind pressed, jumping back to start of signal")
         # the sample number and phase should be 0 upon the start of the signal
         sample = 0
         phase = 0
@@ -249,15 +230,15 @@
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -266,22 +247,22 @@
         naptime = stepsize - elapsed
         if naptime > 0:
             # this approximates the real time streaming speed
             time.sleep(naptime)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_output
     ft_output.disconnect()
     monitor.success('Disconnected from output FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/generatetrigger/__init__.py` & `eegsynth-0.7.0/module/modulatetone/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .generatetrigger import _setup, _start, _loop_once, _loop_forever, _stop
+from .modulatetone import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/generatetrigger/generatetrigger.py` & `eegsynth-0.7.0/module/generatetrigger/generatetrigger.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import threading
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -47,15 +44,15 @@
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
 def trigger(skip=False):
-    global monitor, debug, patch, lock, rate, spread, t
+    global patch, lock, rate, spread, t
 
     if skip:
         # this happens upon initialization and when the timing parameters change
         monitor.debug('skipping this trigger')
     elif patch.getint('general', 'enable', default=True):
         # send the current trigger
         key = patch.getstring('output', 'prefix') + '.note'
@@ -87,49 +84,35 @@
     t.start()
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, scale_rate, scale_spread, offset_rate, offset_spread, rate, spread, lock, t
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global scale_rate, scale_spread, offset_rate, offset_spread, rate, spread, lock, t
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
 
     # the scale and offset are used to map the Redis values to internal values
     scale_rate = patch.getfloat('scale', 'rate', default=1)
     scale_spread = patch.getfloat('scale', 'spread', default=1)
     offset_rate = patch.getfloat('offset', 'rate', default=0)
     offset_spread = patch.getfloat('offset', 'spread', default=0)
 
@@ -153,16 +136,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, scale_rate, scale_spread, offset_rate, offset_spread, rate, spread, lock, t
+    global patch, name, path, monitor
+    global scale_rate, scale_spread, offset_rate, offset_spread, rate, spread, lock, t
     global change
 
     with lock:
         rate = patch.getfloat('interval', 'rate', default=60)
         spread = patch.getfloat('interval', 'spread', default=10)
         rate = EEGsynth.rescale(rate, slope=scale_rate, offset=offset_rate)
         spread = EEGsynth.rescale(spread, slope=scale_spread, offset=offset_spread)
@@ -188,19 +171,20 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
-    sys.exit()
+    pass
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/geomixer/__init__.py` & `eegsynth-0.7.0/module/inputzeromq/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .geomixer import _setup, _start, _loop_once, _loop_forever, _stop
+from .inputzeromq import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/geomixer/geomixer.py` & `eegsynth-0.7.0/module/geomixer/geomixer.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import math
 import numpy as np
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -59,49 +56,35 @@
     return min(max(val, 0), 1)
 
 
 def _setup():
     """Initialize the module
     This adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     """Start the module
     This uses the global variables from setup and adds a set of global variables
     """
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, stepsize, number, prefix, scale_input, scale_time, scale_precision, offset_input, offset_time, offset_precision, channel_name, vertex, dwelltime, edge, previous
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global stepsize, number, prefix, scale_input, scale_time, scale_precision, offset_input, offset_time, offset_precision, channel_name, vertex, dwelltime, edge, previous
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     stepsize = patch.getfloat('general', 'delay')
     number = patch.getint('switch', 'number', default=3)
     prefix = patch.getstring('output', 'prefix')
 
     # the scale and offset are used to map the Redis values to internal values
     scale_input = patch.getfloat('scale', 'input', default=1.)
     scale_time = patch.getfloat('scale', 'time', default=1.)
@@ -125,16 +108,16 @@
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     """Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     """
-    global parser, args, config, r, response, patch
-    global monitor, debug, stepsize, number, prefix, scale_input, scale_time, scale_precision, offset_input, offset_time, offset_precision, channel_name, vertex, dwelltime, edge, previous
+    global patch, name, path, monitor
+    global stepsize, number, prefix, scale_input, scale_time, scale_precision, offset_input, offset_time, offset_precision, channel_name, vertex, dwelltime, edge, previous
     global switch_time, switch_precision, input, lower_treshold, upper_treshold, change, key, channel_val, this, next, val, desired, elapsed, naptime, s
 
     # these can change on the fly
     switch_time = patch.getfloat('switch', 'time', default=1.0)
     switch_time = EEGsynth.rescale(switch_time, slope=scale_time, offset=offset_time)
     switch_precision = patch.getfloat('switch', 'precision', default=0.1)
     switch_precision = EEGsynth.rescale(switch_precision, slope=scale_precision, offset=offset_precision)
@@ -208,30 +191,29 @@
                 channel_val[this] = 1. - clip01(input)
                 channel_val[next] = clip01(input)
             else:
                 channel_val[this] = clip01(input)
                 channel_val[next] = 1. - clip01(input)
         patch.setvalue(channel_name[this], channel_val[this])
 
-    if debug > 0:
-        # construct a string with all details on a single line
-        s = 'edge=%2d' % (edge)
-        for key, val in zip(channel_name, channel_val):
-            s += ' %s = %0.2f' % (key, val)
-        monitor.info(s)
+    # print all details on a single line for debugging
+    s = 'edge=%2d' % (edge)
+    for key, val in zip(channel_name, channel_val):
+        s += ' %s = %0.2f' % (key, val)
+    monitor.info(s)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_forever():
     """Run the main loop forever
     """
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -239,21 +221,21 @@
         elapsed = time.time() - start
         naptime = stepsize - elapsed
         if naptime > 0:
             monitor.trace("naptime = " + str(naptime))
             time.sleep(naptime)
 
 
-
 def _stop():
-    """Stop and clean up on SystemExit, KeyboardInterrupt
+    """Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     """
-    sys.exit()
+    pass
 
 
 if __name__ == "__main__":
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/heartrate/__init__.py` & `eegsynth-0.7.0/module/playbackcontrol/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .heartrate import _setup, _start, _loop_once, _loop_forever, _stop
+from .playbackcontrol import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/heartrate/heartrate.py` & `eegsynth-0.7.0/module/heartrate/heartrate.py`

 * *Files 11% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -50,63 +47,47 @@
 import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel, window, threshold, lrate, debounce, key_beat, key_rate, curvemin, curvemean, curvemax, prev, begsample, endsample
 
-    # get the options from the configuration file
-    debug = patch.getint('general','debug')
+    # this is the timeout for the FieldTrip buffer
+    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to input FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to input FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, channel, window, threshold, lrate, debounce, key_beat, key_rate, curvemin, curvemean, curvemax, prev, begsample, endsample
-
-    # this is the timeout for the FieldTrip buffer
-    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
-
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
         if (time.time()-start)>timeout:
             raise RuntimeError("timeout while waiting for data")
         time.sleep(0.1)
@@ -140,16 +121,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, channel, window, threshold, lrate, debounce, key_beat, key_rate, curvemin, curvemean, curvemax, prev, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel, window, threshold, lrate, debounce, key_beat, key_rate, curvemin, curvemean, curvemax, prev, begsample, endsample
     global dat, negrange, posrange, thresh, prevsample, sample, last, bpm, duration, duration_scale, duration_offset
 
     hdr_input = ft_input.getHeader()
     if (hdr_input.nSamples-1)<endsample:
         raise RuntimeError("buffer reset detected")
     if hdr_input.nSamples < window:
         # there are not yet enough samples in the buffer
@@ -226,26 +207,26 @@
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
-        time.sleep(patch.getfloat('general','delay'))
+        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/historycontrol/__init__.py` & `eegsynth-0.7.0/module/synthesizer/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .historycontrol import _setup, _start, _loop_once, _loop_forever, _stop
+from .synthesizer import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/historycontrol/historycontrol.py` & `eegsynth-0.7.0/module/historycontrol/historycontrol.py`

 * *Files 22% similar despite different names*

```diff
@@ -14,25 +14,22 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from numpy import log, log2, log10, exp, power, sqrt, mean, median, var, std
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -57,46 +54,33 @@
     return val
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, inputlist, enable, stepsize, window, metrics_iqr, metrics_mad, metrics_max, metrics_max_att, metrics_mean, metrics_median, metrics_min, metrics_min_att, metrics_p03, metrics_p16, metrics_p84, metrics_p97, metrics_range, metrics_std, numchannel, numhistory, history, historic
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global inputlist, enable, stepsize, window, metrics_iqr, metrics_mad, metrics_max, metrics_max_att, metrics_mean, metrics_median, metrics_min, metrics_min_att, metrics_p03, metrics_p16, metrics_p84, metrics_p97, metrics_range, metrics_std, numchannel, numhistory, historic_data, historic_stat
 
     # get the options from the configuration file
     inputlist   = patch.getstring('input', 'channels', multiple=True)
     enable      = patch.getint('history', 'enable', default=1)
     stepsize    = patch.getfloat('history', 'stepsize')                 # stepize in seconds
     window      = patch.getfloat('history', 'window')                   # length of sliding window in seconds
 
@@ -114,119 +98,111 @@
     metrics_p97     = patch.getint('metrics', 'p97',     default=1) != 0
     metrics_range   = patch.getint('metrics', 'range',   default=1) != 0
     metrics_std     = patch.getint('metrics', 'std',     default=1) != 0
 
     numchannel  = len(inputlist)
     numhistory  = int(round(window/stepsize))
 
-    # this will contain the full list of historic values
-    history = np.empty((numchannel, numhistory)) * np.NAN
+    # this will contain the full list of historic_stat values
+    historic_data = np.empty((numchannel, numhistory)) * np.NAN
 
-    # this will contain the statistics of the historic values
-    historic = {}
+    # this will contain the statistics of the historic_stat values
+    historic_stat = {}
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, inputlist, enable, stepsize, window, metrics_iqr, metrics_mad, metrics_max, metrics_max_att, metrics_mean, metrics_median, metrics_min, metrics_min_att, metrics_p03, metrics_p16, metrics_p84, metrics_p97, metrics_range, metrics_std, numchannel, numhistory, history, historic
-    global prev_enable, channel, history_att, operation, key, val
+    global patch, name, path, monitor
+    global inputlist, enable, stepsize, window, metrics_iqr, metrics_mad, metrics_max, metrics_max_att, metrics_mean, metrics_median, metrics_min, metrics_min_att, metrics_p03, metrics_p16, metrics_p84, metrics_p97, metrics_range, metrics_std, numchannel, numhistory, historic_data, historic_stat
+    global channel, historic_att, operation, key, val
 
-    # update the enable status
-    prev_enable = enable
+    # determine whether the historic_data should be updated or not
     enable = patch.getint('history', 'enable', default=1)
-
-    if enable and prev_enable:
-        monitor.info("Updating the history")
-    elif enable and not prev_enable:
-        monitor.info("Enabling the updating")
-    elif not enable and not prev_enable:
-        monitor.info("Not updating the history")
-    elif not enable and prev_enable:
-        monitor.info("Disabling the updating")
-
+    monitor.update("enable", enable)
     if not enable:
-        time.sleep(0.1)
         return
 
-    # shift data to next sample
-    history[:, :-1] = history[:, 1:]
+    # shift the data to next sample
+    historic_data[:, :-1] = historic_data[:, 1:]
 
-    # update with current data
+    # update with the current data
     for channel in range(numchannel):
-        history[channel, numhistory-1] = r.get(inputlist[channel])
+        try:
+            historic_data[channel, numhistory-1] = float(patch.redis.get(inputlist[channel]))
+        except:
+            historic_data[channel, numhistory-1] = np.NaN
 
     if metrics_mean or metrics_max_att or metrics_min_att:
-        historic['mean']    = np.nanmean(history, axis=1)
+        historic_stat['mean']    = np.nanmean(historic_data, axis=1)
     if metrics_min or metrics_range:
-        historic['min']     = np.nanmin(history, axis=1)
+        historic_stat['min']     = np.nanmin(historic_data, axis=1)
     if metrics_max or metrics_range:
-        historic['max']     = np.nanmax(history, axis=1)
+        historic_stat['max']     = np.nanmax(historic_data, axis=1)
 
     # use some robust estimators
     if metrics_median:
-        historic['median']  = np.nanmedian(history, axis=1)
+        historic_stat['median']  = np.nanmedian(historic_data, axis=1)
     if metrics_mad:
         # see https://en.wikipedia.org/wiki/Median_absolute_deviation
-        historic['mad']     = mad(history, axis=1)
+        historic_stat['mad']     = mad(historic_data, axis=1)
 
     # for a normal distribution the 16th and 84th percentile correspond to the mean plus-minus one standard deviation
     if metrics_p03:
-        historic['p03']     = np.percentile(history,  3, axis=1) # mean minus 2x standard deviation
+        historic_stat['p03']     = np.percentile(historic_data,  3, axis=1) # mean minus 2x standard deviation
     if metrics_p16 or metrics_iqr:
-        historic['p16']     = np.percentile(history, 16, axis=1) # mean minus 1x standard deviation
+        historic_stat['p16']     = np.percentile(historic_data, 16, axis=1) # mean minus 1x standard deviation
     if metrics_p84 or metrics_iqr:
-        historic['p84']     = np.percentile(history, 84, axis=1) # mean plus 1x standard deviation
+        historic_stat['p84']     = np.percentile(historic_data, 84, axis=1) # mean plus 1x standard deviation
     if metrics_p97:
-        historic['p97']     = np.percentile(history, 97, axis=1) # mean plus 2x standard deviation
+        historic_stat['p97']     = np.percentile(historic_data, 97, axis=1) # mean plus 2x standard deviation
 
     if metrics_iqr:
         # see https://en.wikipedia.org/wiki/Interquartile_range
-        historic['iqr']     = historic['p84'] - historic['p16']
+        historic_stat['iqr']     = historic_stat['p84'] - historic_stat['p16']
 
     if metrics_range:
-        historic['range']   = historic['max'] - historic['min']
+        historic_stat['range']   = historic_stat['max'] - historic_stat['min']
     if metrics_std:
-        historic['std']     = np.nanstd(history, axis=1)
+        historic_stat['std']     = np.nanstd(historic_data, axis=1)
 
     if metrics_max_att or metrics_min_att:
-        # Attenuated history over time, so to diminish max/min over time
+        # Attenuated historic_data over time, so to diminish max/min over time
         # NOTE: There is probably a way to do this without a for-loop:
-        history_att = history
+        historic_att = historic_data
         for channel in range(numchannel):
-            history_att[channel, :] = history_att[channel, :] - historic['mean'][channel]
-            history_att[channel, :] = history_att[channel, :] * np.linspace(0, 1, numhistory)
-            history_att[channel, :] = history_att[channel, :] + historic['mean'][channel]
+            historic_att[channel, :] = historic_att[channel, :] - historic_stat['mean'][channel]
+            historic_att[channel, :] = historic_att[channel, :] * np.linspace(0, 1, numhistory)
+            historic_att[channel, :] = historic_att[channel, :] + historic_stat['mean'][channel]
 
     if metrics_max_att or metrics_min_att:
-        historic['min_att'] = np.nanmin(history_att, axis=1)
-        historic['max_att'] = np.nanmax(history_att, axis=1)
+        historic_stat['min_att'] = np.nanmin(historic_att, axis=1)
+        historic_stat['max_att'] = np.nanmax(historic_att, axis=1)
 
-    for operation in list(historic.keys()):
+    for operation in list(historic_stat.keys()):
         for channel in range(numchannel):
             key = inputlist[channel] + "." + operation
-            val = historic[operation][channel]
+            val = historic_stat[operation][channel]
             patch.setvalue(key, val)
             monitor.debug('%s = %g' % (key, val))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, stepize
+    global monitor, stepize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -234,16 +210,20 @@
         elapsed = time.time() - start
         naptime = stepsize - elapsed
         if naptime>0:
             time.sleep(naptime)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
-    _loop_forever()
+    try:
+        _loop_forever()
+    except (SystemExit, KeyboardInterrupt, RuntimeError):
+        _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/historysignal/__init__.py` & `eegsynth-0.7.0/module/historysignal/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/historysignal/historysignal.py` & `eegsynth-0.7.0/module/historysignal/historysignal.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 from numpy import log, log2, log10, exp, power, sqrt, mean, median, var, std
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -60,63 +57,47 @@
     return val
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, inputlist, prefix, enable, stepsize, window, numhistory, numchannel, history, historic, begsample, endsample
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    # this is the timeout for the FieldTrip buffer
+    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to input FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to input FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, inputlist, prefix, enable, stepsize, window, numhistory, numchannel, history, historic, begsample, endsample
-
-    # this is the timeout for the FieldTrip buffer
-    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
-
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
         if (time.time()-start) > timeout:
             raise RuntimeError("timeout while waiting for data")
         time.sleep(0.1)
@@ -155,16 +136,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, inputlist, prefix, enable, stepsize, window, numhistory, numchannel, history, historic, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, inputlist, prefix, enable, stepsize, window, numhistory, numchannel, history, historic, begsample, endsample
     global prev_enable, dat_input, chanindx, operation, key, val
 
     # determine the start of the actual processing
     start = time.time()
 
     # update the enable status
     prev_enable = enable
@@ -225,15 +206,15 @@
         historic['p97']     = np.percentile(history.flatten(), 97, axis=0) # mean plus 2x standard deviation
         # see https://en.wikipedia.org/wiki/Interquartile_range
         historic['iqr']     = historic['p84'] - historic['p16']
 
     for operation in list(historic.keys()):
         key = prefix + "." + operation
         val = historic[operation]
-        patch.setvalue(key, val, debug > 1)
+        patch.setvalue(key, val)
 
     begsample += stepsize
     endsample += stepsize
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
@@ -245,22 +226,22 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/inputcontrol/inputcontrol.py` & `eegsynth-0.7.0/module/inputcontrol/inputcontrol.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 # This module allows the user to design a graphical interface with dials (knobs), sliders and buttons.
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
-# Copyright (C) 2019 EEGsynth project
+# Copyright (C) 2019-2023 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -17,25 +17,22 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from PyQt5 import QtGui, QtCore, QtWidgets
 from PyQt5.QtWidgets import QApplication, QWidget
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import signal
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -47,66 +44,102 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
+class QLineEditDrop(QtWidgets.QLineEdit):
+    ''' This is a QLineEdit widget that also supports dropping a filename on it
+    '''
+    def __init__(self):
+        super().__init__()
+        self.setAcceptDrops(True)
+
+    def dragEnterEvent(self, event):
+        if event.mimeData().hasUrls():
+            event.accept()
+        else:
+            event.ignore()
+
+    def dropEvent(self, event):
+        files = [u.toLocalFile() for u in event.mimeData().urls()]
+        self.setText(files[0])
+
+
 class Window(QWidget):
     def __init__(self):
         super(Window, self).__init__()
         self.setGeometry(winx, winy, winwidth, winheight)
         self.setStyleSheet('background-color:black;')
         self.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth inputcontrol'))
         self.drawmain()
 
     # each row or column with sliders/dials/buttons is a panel
     def drawpanel(self, panel, list):
         for item in list:
 
             try:
-                # read the previous value from Redis
+                # get the default or previous value from Redis
                 key = '%s.%s' % (prefix, item[0])
-                val = float(patch.redis.get(key))
-                # sliders and dials have an internal value between 0 and 127
-                val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset, reverse=True)
-                # buttons have an internal value of 0, 1, 2, 3, 4
-                if item[1] == 'slap' or item[1] == 'push':
-                    # these should always start as 0, see https://github.com/eegsynth/eegsynth/issues/375
-                    val = 0
-                elif item[1] == 'toggle1':
-                    val = int(1. * val / 127.)
-                elif item[1] == 'toggle2':
-                    val = int(2. * val / 127.)
-                elif item[1] == 'toggle3':
-                    val = int(3. * val / 127.)
-                elif item[1] == 'toggle4':
-                    val = int(4. * val / 127.)
-                elif item[1] == 'text':
-                    # text has an internal value identical to the external value
-                    val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset)
-                monitor.info('%s = %g' % (key, val))
+                val = patch.redis.get(key)
+                # the value can either be a number or a string
+                try:
+                    val = float(val)
+                    # apply the appropriate scaling
+                    if item[1] == 'slider' or item[1] == 'dial':
+                        # sliders and dials have an internal value between 0 and 127
+                        val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset, reverse=True)
+                    elif item[1] == 'slap' or item[1] == 'push':
+                        # buttons have an internal value of 0, 1, 2, 3, 4 and should always start as 0, see https://github.com/eegsynth/eegsynth/issues/375
+                        val = 0
+                    elif item[1] == 'toggle1':
+                        val = int(1. * val / 127.)
+                    elif item[1] == 'toggle2':
+                        val = int(2. * val / 127.)
+                    elif item[1] == 'toggle3':
+                        val = int(3. * val / 127.)
+                    elif item[1] == 'toggle4':
+                        val = int(4. * val / 127.)
+                    elif item[1] == 'text':
+                        # text has an internal value identical to the external value
+                        val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset)
+                    monitor.info('%s = %g' % (key, val))
+
+                except ValueError:
+                    val = val
+                    monitor.info('%s = %s' % (key, val))
+
             except:
-                # set the default initial value to 0
+                # set the default value to 0
                 val = 0
 
             if item[1] == 'label':
                 l = QtWidgets.QLabel(item[0])
                 l.setAlignment(QtCore.Qt.AlignHCenter)
                 l.setStyleSheet('color: rgb(200,200,200);')
                 panel.addWidget(l)
 
+            elif item[1] == 'placeholder':
+                l = QtWidgets.QLabel("")
+                panel.addWidget(l)
+
             elif item[1] == 'text':
-                t = QtWidgets.QLineEdit()
+                t = QLineEditDrop() # derived from QtWidgets.QLineEdit()
                 t.name = item[0]
                 t.type = item[1]
-                t.setText("%g" % val)
+                # the value can either be a number or a string
+                if isinstance(val, str):
+                    t.setText(val)
+                else:
+                    t.setText("%g" % val)
                 t.setAlignment(QtCore.Qt.AlignHCenter)
                 t.setStyleSheet('background-color: rgb(64,64,64); color: rgb(200,200,200);')
-                t.editingFinished.connect(self.changevalue)
+                t.editingFinished.connect(self.changevalue) # upon manual edit
+                t.textChanged.connect(self.changevalue)     # upon drag-and-drop
                 l = QtWidgets.QLabel(t.name)
                 l.setAlignment(QtCore.Qt.AlignHCenter)
                 l.setStyleSheet('color: rgb(200,200,200);')
                 # position the label under the slider
                 tl = QtWidgets.QVBoxLayout()
                 tl.addWidget(t)
                 tl.setAlignment(t, QtCore.Qt.AlignHCenter)
@@ -116,15 +149,15 @@
 
             elif item[1] == 'slider':
                 s = QtWidgets.QSlider(QtCore.Qt.Vertical)
                 s.name = item[0]
                 s.type = item[1]
                 s.setMinimum(0)
                 s.setMaximum(127)  # default is 100
-                s.setValue(val)
+                s.setValue(int(val))
                 s.setTickInterval(1)
                 s.setTickPosition(QtWidgets.QSlider.NoTicks)
                 s.setStyleSheet('background-color: rgb(64,64,64);')
                 s.valueChanged.connect(self.changevalue)
                 l = QtWidgets.QLabel(s.name)
                 l.setAlignment(QtCore.Qt.AlignHCenter)
                 l.setStyleSheet('color: rgb(200,200,200);')
@@ -178,56 +211,57 @@
         mainlayout.addLayout(leftlayout)
         mainlayout.addLayout(rightlayout)
         self.setLayout(mainlayout)
 
         # the section 'slider' is treated as the first row
         # this is only for backward compatibility
         section = 'slider'
-        if config.has_section(section):
+        if patch.config.has_section(section):
             sectionlayout = QtWidgets.QHBoxLayout()
-            self.drawpanel(sectionlayout, config.items(section))
+            self.drawpanel(sectionlayout, patch.config.items(section))
             leftlayout.addLayout(sectionlayout)
 
         for row in range(0, 16):
             section = 'row%d' % (row + 1)
-            if config.has_section(section):
+            if patch.config.has_section(section):
                 sectionlayout = QtWidgets.QHBoxLayout()
-                self.drawpanel(sectionlayout, config.items(section))
+                self.drawpanel(sectionlayout, patch.config.items(section))
                 leftlayout.addLayout(sectionlayout)
 
         # the section 'button' is treated as the first column
         # this is only for backward compatibility
         section = 'button'
-        if config.has_section(section):
+        if patch.config.has_section(section):
             sectionlayout = QtWidgets.QVBoxLayout()
-            self.drawpanel(sectionlayout, config.items(section))
+            self.drawpanel(sectionlayout, patch.config.items(section))
             rightlayout.addLayout(sectionlayout)
 
         for column in range(0, 16):
             section = 'column%d' % (column + 1)
-            if config.has_section(section):
+            if patch.config.has_section(section):
                 sectionlayout = QtWidgets.QVBoxLayout()
-                self.drawpanel(sectionlayout, config.items(section))
+                self.drawpanel(sectionlayout, patch.config.items(section))
                 rightlayout.addLayout(sectionlayout)
 
     def changecolor(self):
         target = self.sender()
         self.setcolor(target)
 
     def changevalue(self):
         target = self.sender()
         send = True
         if target.type == 'slider' or target.type == 'dial':
             val = target.value()
         elif target.type == 'text':
+            # it can either be a number or a string
             try:
-                val = float(target.text())  # convert the string into a scalar
+                val = float(target.text())  # convert the string into a number
                 target.setText('%g' % val)  # ensure that the displayed value is consistent
-            except:
-                val = target.text()
+            except ValueError:
+                val = target.text()         # keep it as a string
         elif target.type == 'slap':
             target.value = (target.value + 1) % 2
             val = target.value * 127 / 1
             send = val > 0  # only send the press, not the release
         elif target.type == 'push':
             target.value = (target.value + 1) % 2
             val = target.value * 127 / 1
@@ -251,18 +285,18 @@
                 val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset)
             patch.setvalue(key, val)
             monitor.update(key, val)
 
     def setcolor(self, target):
         # see https://www.w3schools.com/css/css3_buttons.asp
         grey = 'background-color: rgb(250,250,250); border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
-        red = 'background-color: rgb(255,0,0);     border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
-        yellow = 'background-color: rgb(250,250,60);  border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
-        green = 'background-color: rgb(60,200,60);   border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
-        amber = 'background-color: rgb(250,190,45);  border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
+        red = 'background-color: rgb(255,0,0); border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
+        yellow = 'background-color: rgb(250,250,60); border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
+        green = 'background-color: rgb(60,200,60); border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
+        amber = 'background-color: rgb(250,190,45); border: 1px solid gray; border-radius: 4px; padding: 4px 4px;'
 
         if target.type == 'slap':
             if target.value == 1:
                 target.setStyleSheet(amber)
             else:
                 target.setStyleSheet(grey)
 
@@ -306,96 +340,93 @@
             target.setStyleSheet(grey)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, prefix, winx, winy, winwidth, winheight, output_scale, output_offset
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global prefix, winx, winy, winwidth, winheight, output_scale, output_offset, app, timer
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     prefix = patch.getstring('output', 'prefix')
-    winx = patch.getfloat('display', 'xpos')
-    winy = patch.getfloat('display', 'ypos')
-    winwidth = patch.getfloat('display', 'width')
-    winheight = patch.getfloat('display', 'height')
+    winx = patch.getint('display', 'xpos')
+    winy = patch.getint('display', 'ypos')
+    winwidth = patch.getint('display', 'width')
+    winheight = patch.getint('display', 'height')
 
     # the scale and offset are used to map internal values to Redis values
     output_scale = patch.getfloat('output', 'scale', default=1. / 127)  # internal values are from 0 to 127
     output_offset = patch.getfloat('output', 'offset', default=0.)    # internal values are from 0 to 127
 
-    if 'initial' in config.sections():
+    if 'initial' in patch.config.sections():
         # assign the initial values
-        for item in config.items('initial'):
-            val = patch.getfloat('initial', item[0])
+        for item in patch.config.items('initial'):
+            # the value can either be a number or a string
+            val = patch.getstring('initial', item[0])
+            try:
+                # convert to number
+                val = float(val)
+            except ValueError:
+                # keep as string
+                val = val
             patch.setvalue(item[0], val)
             monitor.update(item[0], val)
 
     # start the graphical user interface
     app = QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
     app.aboutToQuit.connect(_stop)
     signal.signal(signal.SIGINT, _stop)
 
+    window = Window()
+    window.show()
+
     # Let the interpreter run every 200 ms
     # see https://stackoverflow.com/questions/4938723/what-is-the-correct-way-to-make-my-pyqt-application-quit-when-killed-from-the-co/6072360#6072360
     timer = QtCore.QTimer()
-    timer.start(400)
-    timer.timeout.connect(lambda: None)
+    timer.start(200)
+    timer.timeout.connect(_loop_once)
 
-    ex = Window()
-    ex.show()
     sys.exit(app.exec_())
 
 
 def _loop_once():
-    '''Updating the main figure is done through Qt events
+    '''Run the main loop once
     '''
-    pass
+    # Updating the main figure is done through Qt events
+    global monitor
+    monitor.loop()
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     QApplication.quit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
```

### Comparing `eegsynth-0.6.0/module/inputlsl/__init__.py` & `eegsynth-0.7.0/module/outputosc/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .inputlsl import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputosc import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/inputlsl/inputlsl.py` & `eegsynth-0.7.0/module/inputlsl/inputlsl.py`

 * *Files 11% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import pylsl as lsl
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -49,46 +46,33 @@
 import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, delay, timeout, lsl_name, lsl_type, lsl_format, output_prefix, start, selected, streams, stream, inlet, type, source_id, match, lsl_id
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, timeout, lsl_name, lsl_type, lsl_format, output_prefix, start, selected, streams, stream, inlet, type, source_id, match, lsl_id
 
     # get the options from the configuration file
     delay = patch.getfloat('general', 'delay')
     timeout = patch.getfloat('lsl', 'timeout', default=30)
     lsl_name = patch.getstring('lsl', 'name')
     lsl_type = patch.getstring('lsl', 'type')
     lsl_format = patch.getstring('lsl', 'format')
@@ -139,16 +123,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, delay, timeout, lsl_name, lsl_type, lsl_format, output_prefix, start, selected, streams, stream, inlet, type, source_id, match, lsl_id
+    global patch, name, path, monitor
+    global delay, timeout, lsl_name, lsl_type, lsl_format, output_prefix, start, selected, streams, stream, inlet, type, source_id, match, lsl_id
     global sample, timestamp
 
     sample, timestamp = inlet.pull_sample(timeout=delay)
     if not sample == None:
 
         if lsl_format == 'value':
             # interpret the LSL marker string as a numerical value
@@ -181,19 +165,20 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/inputmidi/__init__.py` & `eegsynth-0.7.0/module/outputmidi/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .inputmidi import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputmidi import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/inputmidi/inputmidi.py` & `eegsynth-0.7.0/module/inputmqtt/inputmqtt.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,40 +1,38 @@
 #!/usr/bin/env python
 
-# Inputmidi records MIDI data to Redis
+# This module translates MQTT messages to Redis controls.
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
-# Copyright (C) 2017-2022 EEGsynth project
+# Copyright (C) 2019 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
-import mido
-from fuzzywuzzy import process
 import os
-import redis
+import string
 import sys
+import threading
 import time
+import paho.mqtt.client as mqtt
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -46,103 +44,108 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
+# The callback for when the client receives a CONNACK response from the server
+def on_connect(client, userdata, flags, rc):
+    monitor.info("Connected with result code " + str(rc))
+    # Subscribing in on_connect() means that if we lose the connection and
+    # reconnect then subscriptions will be renewed.
+    client.subscribe("$SYS/#")
+
+
+# The callback for when a PUBLISH message is received from the server
+def on_message(client, userdata, msg):
+    if not msg.topic.startswith('$SYS'):
+        try:
+            key = msg.topic.replace('/', '.').lower()
+            if len(prefix):
+                # add the prefix
+                key = "%s.%s" % (prefix, key)
+            # assume that it is a single scalar value
+            val = EEGsynth.rescale(float(msg.payload), slope=output_scale, offset=output_offset)
+            monitor.update(key, val)
+            patch.setvalue(key, val)
+        except:
+            pass
+
+
+# The callback for when the client disconnects
+def on_disconnect(client, userdata, rc):
+    if rc != 0:
+        monitor.info("MQTT disconnected")
+
+
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor, client
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+        client = mqtt.Client()
+        client.connect(patch.get('mqtt', 'hostname'), patch.getint('mqtt', 'port'), patch.getint('mqtt', 'timeout'))
+    except:
+        raise RuntimeError("cannot connect to MQTT broker")
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, mididevice, output_scale, output_offset, port, inputport
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor, client, name
+    global prefix, output_scale, output_offset, input_channels, channel
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-    mididevice = patch.getstring('midi', 'device')
-    mididevice = EEGsynth.trimquotes(mididevice)
-
-    # the scale and offset are used to map MIDI values to Redis values
-    output_scale = patch.getfloat('output', 'scale', default=1. / 127)  # MIDI values are from 0 to 127
-    output_offset = patch.getfloat('output', 'offset', default=0.)    # MIDI values are from 0 to 127
-
-    # this is only for debugging, check which MIDI devices are accessible
-    monitor.info('------ INPUT ------')
-    for port in mido.get_input_names():
-        monitor.info(port)
-    monitor.info('-------------------------')
+    prefix = patch.getstring('output', 'prefix')
 
-    try:
-        inputport = mido.open_input(mididevice)
-        monitor.success('Connected to MIDI input')
-    except:
-        raise RuntimeError("Cannot connect to MIDI input")
+    # the scale and offset are used to map OSC values to Redis values
+    output_scale = patch.getfloat('output', 'scale', default=1)
+    output_offset = patch.getfloat('output', 'offset', default=0)
+
+    client.on_connect = on_connect
+    client.on_message = on_message
+    client.on_disconnect = on_disconnect
+
+    input_channels = patch.getstring('input', 'channels', default='#', multiple=True)
+    for channel in input_channels:
+        monitor.info('subscribed to ' + channel)
+        client.subscribe(channel)
+
+    client.loop_start()
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, mididevice, output_scale, output_offset, port, inputport
-
-    for msg in inputport.iter_pending():
-        monitor.debug(msg)
-
-        if hasattr(msg, "control"):
-            # prefix.control000=value
-            key = "{}.control{:0>3d}".format(patch.getstring('output', 'prefix'), msg.control)
-            val = msg.value
-            # map the MIDI values to Redis values between 0 and 1
-            val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset)
-            patch.setvalue(key, val)
-
-        elif hasattr(msg, "note"):
-            # prefix.noteXXX=value
-            key = "{}.note{:0>3d}".format(patch.getstring('output', 'prefix'), msg.note)
-            val = msg.velocity
-            patch.setvalue(key, val)
-            key = "{}.note".format(patch.getstring('output', 'prefix'))
-            val = msg.note
-            patch.setvalue(key, val)
+    global patch, name, path, monitor, client
+    global prefix, output_scale, output_offset, input_channels, channel
+    global output_scale, output_offset
+
+    # update the scale and offset
+    output_scale = patch.getfloat('output', 'scale', default=1)
+    output_offset = patch.getfloat('output', 'offset', default=0)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
@@ -152,19 +155,23 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    global monitor, client
+    monitor.success("Stopping module...")
+    client.loop_stop(force=False)
+    monitor.success("Done.")
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/inputmqtt/__init__.py` & `eegsynth-0.7.0/module/volcabass/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .inputmqtt import _setup, _start, _loop_once, _loop_forever, _stop
+from .volcabass import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/inputmqtt/inputmqtt.py` & `eegsynth-0.7.0/module/inputzeromq/inputzeromq.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# This module translates MQTT messages to Redis controls.
+# This module translates ZeroMQ messages to Redis controls.
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2019 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,27 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import string
 import sys
-import threading
 import time
-import paho.mqtt.client as mqtt
+import zmq
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -47,148 +43,126 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
-# The callback for when the client receives a CONNACK response from the server
-def on_connect(client, userdata, flags, rc):
-    monitor.info("Connected with result code " + str(rc))
-    # Subscribing in on_connect() means that if we lose the connection and
-    # reconnect then subscriptions will be renewed.
-    client.subscribe("$SYS/#")
-
-
-# The callback for when a PUBLISH message is received from the server
-def on_message(client, userdata, msg):
-    if not msg.topic.startswith('$SYS'):
-        try:
-            key = msg.topic.replace('/', '.').lower()
-            if len(prefix):
-                # add the prefix
-                key = "%s.%s" % (prefix, key)
-            # assume that it is a single scalar value
-            val = EEGsynth.rescale(float(msg.payload), slope=output_scale, offset=output_offset)
-            monitor.update(key, val)
-            patch.setvalue(key, val)
-        except:
-            pass
-
-
-# The callback for when the client disconnects
-def on_disconnect(client, userdata, rc):
-    if rc != 0:
-        monitor.info("MQTT disconnected")
-
-
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, client
+    global patch, name, path, monitor, context, socket, patch
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     try:
-        client = mqtt.Client()
-        client.connect(config.get('mqtt', 'hostname'), config.getint('mqtt', 'port'), config.getint('mqtt', 'timeout'))
+        context = zmq.Context()
+        socket = context.socket(zmq.SUB)
+        socket.connect("tcp://%s:%i" % (patch.get('zeromq', 'hostname'), patch.getint('zeromq', 'port')))
     except:
-        raise RuntimeError("cannot connect to MQTT broker")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+        raise RuntimeError("cannot connect to ZeroMQ")
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, client, name
-    global monitor, debug, prefix, output_scale, output_offset, input_channels, channel
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor, context, socket, patch
+    global prefix, output_scale, output_offset, input_channels
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     prefix = patch.getstring('output', 'prefix')
 
     # the scale and offset are used to map OSC values to Redis values
     output_scale = patch.getfloat('output', 'scale', default=1)
     output_offset = patch.getfloat('output', 'offset', default=0)
 
-    client.on_connect = on_connect
-    client.on_message = on_message
-    client.on_disconnect = on_disconnect
-
-    input_channels = patch.getstring('input', 'channels', default='#', multiple=True)
-    for channel in input_channels:
-        monitor.info('subscribed to ' + channel)
-        client.subscribe(channel)
+    input_channels = patch.getstring('input', 'channels', multiple=True)
+    if len(input_channels) == 0:
+        monitor.info('subscribed to everything')
+        socket.setsockopt_string(zmq.SUBSCRIBE, u'')
+    else:
+        for channel in input_channels:
+            monitor.info('subscribed to ' + channel)
+            socket.setsockopt_string(zmq.SUBSCRIBE, channel)
 
-    client.loop_start()
+    # set a timeout for receiving messages
+    socket.RCVTIMEO = int(1000 * patch.getfloat('general', 'delay'))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, client
-    global monitor, debug, prefix, output_scale, output_offset, input_channels, channel
-    global output_scale, output_offset
+    global patch, name, path, monitor, context, socket, patch
+    global prefix, output_scale, output_offset, input_channels
+    global start
 
-    # update the scale and offset
+    start = time.time()
+
+    # process all messages that are waiting
+    while (time.time() - start) < patch.getfloat('general', 'delay'):
+        try:
+            # this will timeout after the specified delay
+            message = socket.recv_string()
+        except zmq.error.Again:
+            # timeout, there are no messages
+            break
+        key, val = message.split()
+        key = key.replace('/', '.').lower()
+        if len(prefix):
+            # add the prefix
+            key = "%s.%s" % (prefix, key)
+        # assume that it is a single scalar value
+        val = EEGsynth.rescale(float(val), slope=output_scale, offset=output_offset)
+        monitor.update(key, val)
+        patch.setvalue(key, val)
+
+    # update the scale and offset, these values are updated after every delay
     output_scale = patch.getfloat('output', 'scale', default=1)
     output_offset = patch.getfloat('output', 'offset', default=0)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
-        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, client
-    monitor.success("Closing module...")
-    client.loop_stop(force=False)
+    global monitor, socket, context
+    monitor.success("Stopping module...")
+    socket.close()
+    context.destroy()
     monitor.success("Done.")
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/inputosc/__init__.py` & `eegsynth-0.7.0/module/heartrate/__init__.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .inputosc import _setup, _start, _loop_once, _loop_forever, _stop
+from .heartrate import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/inputosc/inputosc.py` & `eegsynth-0.7.0/module/inputosc/inputosc.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,18 +15,15 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import socket
 import sys
 import threading
 import time
 
 # The required package depends on the Python version, one works for older and the other for newer versions.
 # This cannot be handled easily by setup.py during installation, hence we only _try_ to load the module.
@@ -44,15 +41,15 @@
         use_old_version = False
     except ModuleNotFoundError:
         # give a warning, not an error, so that eegsynth.py does not fail as a whole
         print('Warning: pythonosc is required for the outputosc module, please install it with "pip install python-osc"')
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -107,50 +104,36 @@
     monitor.update(key, val)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
+    global patch, name, path, monitor
     global use_old_version, dispatcher, osc_server
-    global monitor, debug, osc_address, osc_port, prefix, output_scale, output_offset
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global osc_address, osc_port, prefix, output_scale, output_offset
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     osc_address = patch.getstring('osc', 'address', default=socket.gethostbyname(socket.gethostname()))
     osc_port = patch.getint('osc', 'port')
     prefix = patch.getstring('output', 'prefix')
 
     # the scale and offset are used to map OSC values to Redis values
     output_scale = patch.getfloat('output', 'scale', default=1)
     output_offset = patch.getfloat('output', 'offset', default=0)
@@ -185,15 +168,15 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
     global use_old_version, output_scale, output_offset
 
     # keep looping while incoming OSC messages are being handled
     if use_old_version:
         # update the scale and offset
         output_scale = patch.getfloat('output', 'scale', default=1)
         output_offset = patch.getfloat('output', 'offset', default=0)
@@ -209,26 +192,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global use_old_version, monitor, s, st
     if use_old_version:
-        monitor.success("Closing module...")
+        monitor.success("Stopping module...")
         s.close()
         monitor.info("Waiting for OSC server thread to finish.")
         st.join()
         monitor.success("Done.")
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/inputzeromq/__init__.py` & `eegsynth-0.7.0/module/sonification/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .inputzeromq import _setup, _start, _loop_once, _loop_forever, _stop
+from .sonification import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/inputzeromq/inputzeromq.py` & `eegsynth-0.7.0/module/outputzeromq/outputzeromq.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# This module translates ZeroMQ messages to Redis controls.
+# This module translates Redis controls to ZeroMQ messages.
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2019 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,26 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import string
 import sys
+import threading
 import time
 import zmq
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -46,143 +44,148 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
+class TriggerThread(threading.Thread):
+    def __init__(self, redischannel, name, zeromqtopic):
+        threading.Thread.__init__(self)
+        self.redischannel = redischannel
+        self.name = name
+        self.zeromqtopic = zeromqtopic
+        self.running = True
+
+    def stop(self):
+        self.running = False
+
+    def run(self):
+        global r, patch, monitor, socket
+        pubsub = patch.pubsub()
+        pubsub.subscribe('OUTPUTZEROMQ_UNBLOCK')  # this message unblocks the redis listen command
+        pubsub.subscribe(self.redischannel)       # this message contains the value of interest
+        while self.running:
+            for item in pubsub.listen():
+                if not self.running or not item['type'] == 'message':
+                    break
+                if item['channel'] == self.redischannel:
+                    # map the Redis values to ZeroMQ values
+                    val = float(item['data'])
+                    # the scale and offset options are channel specific
+                    scale = patch.getfloat('scale', self.name, default=1)
+                    offset = patch.getfloat('offset', self.name, default=0)
+                    # apply the scale and offset
+                    val = EEGsynth.rescale(val, slope=scale, offset=offset)
+
+                    monitor.update(self.zeromqtopic, val)
+                    with lock:
+                        # send it as a string with a space as separator
+                        socket.send_string("%s %f" % (self.zeromqtopic, val))
+
+
+
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, context, socket, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    if not 'general' in config:
-        raise RuntimeError("cannot read configuration from " + args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    try:
-        context = zmq.Context()
-        socket = context.socket(zmq.SUB)
-        socket.connect("tcp://%s:%i" % (config.get('zeromq', 'hostname'), config.getint('zeromq', 'port')))
-    except:
-        raise RuntimeError("cannot connect to ZeroMQ")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, context, socket, patch
-    global monitor, debug, prefix, output_scale, output_offset, input_channels
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread, context, socket
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-    prefix = patch.getstring('output', 'prefix')
 
-    # the scale and offset are used to map OSC values to Redis values
-    output_scale = patch.getfloat('output', 'scale', default=1)
-    output_offset = patch.getfloat('output', 'offset', default=0)
-
-    input_channels = patch.getstring('input', 'channels', multiple=True)
-    if len(input_channels) == 0:
-        monitor.info('subscribed to everything')
-        socket.setsockopt_string(zmq.SUBSCRIBE, u'')
-    else:
-        for channel in input_channels:
-            monitor.info('subscribed to ' + channel)
-            socket.setsockopt_string(zmq.SUBSCRIBE, channel)
+    # keys should be present in both the input and output section of the *.ini file
+    list_input = patch.config.items('input')
+    list_output = patch.config.items('output')
+
+    list1 = []  # the key name that matches in the input and output section of the *.ini file
+    list2 = []  # the key name in Redis
+    list3 = []  # the key name in ZeroMQ
+    for i in range(len(list_input)):
+        for j in range(len(list_output)):
+            if list_input[i][0] == list_output[j][0]:
+                list1.append(list_input[i][0])  # short name in the ini file
+                list2.append(list_input[i][1])  # redis channel
+                list3.append(list_output[j][1])  # zeromq topic
+
+    # this is to prevent two messages from being sent at the same time
+    lock = threading.Lock()
+
+    # each of the Redis messages is mapped onto a different ZeroMQ topic
+    trigger = []
+    for key1, key2, key3 in zip(list1, list2, list3):
+        this = TriggerThread(key2, key1, key3)
+        trigger.append(this)
+        monitor.debug(key1 + ' trigger configured')
+
+    # start the thread for each of the triggers
+    for thread in trigger:
+        thread.start()
 
-    # set a timeout for receiving messages
-    socket.RCVTIMEO = int(1000 * patch.getfloat('general', 'delay'))
+    # make the connection with ZeroMQ
+    try:
+        context = zmq.Context()
+        socket = context.socket(zmq.PUB)
+        socket.bind("tcp://*:%i" % config.getint('zeromq', 'port'))
+        socket.send_string('Hello')
+    except:
+        raise RuntimeError("cannot connect to ZeroMQ")
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
-    This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, context, socket, patch
-    global monitor, debug, prefix, output_scale, output_offset, input_channels
-    global start
-
-    start = time.time()
-
-    # process all messages that are waiting
-    while (time.time() - start) < patch.getfloat('general', 'delay'):
-        try:
-            # this will timeout after the specified delay
-            message = socket.recv_string()
-        except zmq.error.Again:
-            # timeout, there are no messages
-            break
-        key, val = message.split()
-        key = key.replace('/', '.').lower()
-        if len(prefix):
-            # add the prefix
-            key = "%s.%s" % (prefix, key)
-        # assume that it is a single scalar value
-        val = EEGsynth.rescale(float(val), slope=output_scale, offset=output_offset)
-        monitor.update(key, val)
-        patch.setvalue(key, val)
-
-    # update the scale and offset, these values are updated after every delay
-    output_scale = patch.getfloat('output', 'scale', default=1)
-    output_offset = patch.getfloat('output', 'offset', default=0)
-
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    pass
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
+        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, socket, context
-    monitor.success("Closing module...")
-    socket.close()
+    global monitor, trigger, context
+    monitor.success('Closing threads')
+    for thread in trigger:
+        thread.stop()
+    patch.publish('OUTPUTZEROMQ_UNBLOCK', 1)
+    for thread in trigger:
+        thread.join()
     context.destroy()
-    monitor.success("Done.")
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/keyboard/__init__.py` & `eegsynth-0.7.0/module/keyboard/__init__.py`

 * *Files 22% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/keyboard/keyboard.py` & `eegsynth-0.7.0/module/keyboard/keyboard.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -68,15 +65,15 @@
         self.duration = duration    # optional, this is a value to get
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('KEYBOARD_UNBLOCK')  # this message unblocks the Redis listen command
         pubsub.subscribe(self.onset)      # this message triggers the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.onset:
@@ -86,31 +83,31 @@
                     val = EEGsynth.limit(val, 0, 127)
                     val = int(val)
 
                     if self.velocity == None:
                         # use the value of the onset trigger
                         velocity = val
                     elif type(self.velocity) == str:
-                        velocity = float(r.get(self.velocity))
+                        velocity = float(patch.redis.get(self.velocity))
                         velocity = EEGsynth.rescale(velocity, slope=scale_velocity, offset=offset_velocity)
                         velocity = EEGsynth.limit(velocity, 0, 127)
                         velocity = int(velocity)
                     else:
                         velocity = self.velocity
 
                     if type(self.pitch) == str:
-                        pitch = float(r.get(self.pitch))
+                        pitch = float(patch.redis.get(self.pitch))
                         pitch = EEGsynth.rescale(pitch, slope=scale_pitch, offset=offset_pitch)
                         pitch = EEGsynth.limit(pitch, 0, 127)
                         pitch = int(pitch)
                     else:
                         pitch = self.pitch
 
                     if type(self.duration) == str:
-                        duration = float(r.get(self.duration))
+                        duration = float(patch.redis.get(self.duration))
                         duration = EEGsynth.rescale(duration, slope=scale_duration, offset=offset_duration)
                         # some minimal time is needed for the delay
                         duration = EEGsynth.limit(duration, 0.05, float('Inf'))
                     else:
                         duration = self.duration
 
                     monitor.debug('----------------------------------------------')
@@ -135,56 +132,42 @@
                         t.start()
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, note_name, note_code, debug, midichannel, mididevice, input_scale, input_offset, scale_velocity, scale_pitch, scale_duration, offset_velocity, offset_pitch, offset_duration, output_scale, output_offset, port, inputport, outputport, lock, trigger, code, onset, velocity, pitch, duration, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global note_name, note_code, midichannel, mididevice, input_scale, input_offset, scale_velocity, scale_pitch, scale_duration, offset_velocity, offset_pitch, offset_duration, output_scale, output_offset, port, inputport, outputport, lock, trigger, code, onset, velocity, pitch, duration, thread
 
     # the list of MIDI commands is specific to the implementation for a full-scale keyboard
     # see https://newt.phys.unsw.edu.au/jw/notes.html
     note_name = ['C0', 'Db0', 'D0', 'Eb0', 'E0', 'F0', 'Gb0', 'G0', 'Ab0', 'A0', 'Bb0', 'B0', 'C1', 'Db1', 'D1', 'Eb1', 'E1', 'F1', 'Gb1', 'G1', 'Ab1', 'A1', 'Bb1', 'B1', 'C2', 'Db2', 'D2', 'Eb2', 'E2', 'F2', 'Gb2', 'G2', 'Ab2', 'A2', 'Bb2', 'B2', 'C3', 'Db3', 'D3', 'Eb3', 'E3', 'F3', 'Gb3', 'G3', 'Ab3', 'A3', 'Bb3', 'B3', 'C4', 'Db4', 'D4', 'Eb4', 'E4', 'F4', 'Gb4', 'G4', 'Ab4', 'A4', 'Bb4', 'B4', 'C5', 'Db5', 'D5', 'Eb5', 'E5', 'F5',
                  'Gb5', 'G5', 'Ab5', 'A5', 'Bb5', 'B5', 'C6', 'Db6', 'D6', 'Eb6', 'E6', 'F6', 'Gb6', 'G6', 'Ab6', 'A6', 'Bb6', 'B6', 'C7', 'Db7', 'D7', 'Eb7', 'E7', 'F7', 'Gb7', 'G7', 'Ab7', 'A7', 'Bb7', 'B7', 'C8', 'Db8', 'D8', 'Eb8', 'E8', 'F8', 'Gb8', 'G8', 'Ab8', 'A8', 'Bb8', 'B8', 'C9', 'Db9', 'D9', 'Eb9', 'E9', 'F9', 'Gb9', 'G9', 'Ab9', 'A9', 'Bb9', 'B9', 'C10', 'Db10', 'D10', 'Eb10', 'E10', 'F10', 'Gb10', 'G10', 'Ab10', 'A10', 'Bb10', 'B10']
     note_code = [12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81,
                  82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143]
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     midichannel = patch.getint('midi', 'channel', default=None)
     mididevice = patch.getstring('midi', 'device')
     mididevice = EEGsynth.trimquotes(mididevice)
     mididevice = process.extractOne(mididevice, mido.get_input_names())[0]  # select the closest match
 
     # the input scale and offset are used to map Redis values to MIDI values
     input_scale = patch.getfloat('input', 'scale', default=127)
@@ -229,15 +212,15 @@
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     # the keyboard notes can be linked to separate triggers, where the trigger value corresponds to the velocity
     trigger = []
     for name, code in zip(note_name, note_code):
-        if config.has_option('input', name):
+        if patch.config.has_option('input', name):
             # start the background thread that deals with this note
             onset = patch.getstring('input', name)
             velocity = None  # use the value of the onset trigger
             pitch = code
             duration = None
             trigger.append(TriggerThread(onset, velocity, pitch, duration))
             monitor.debug(name + ' = OK')
@@ -262,16 +245,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, note_name, note_code, debug, midichannel, mididevice, input_scale, input_offset, scale_velocity, scale_pitch, scale_duration, offset_velocity, offset_pitch, offset_duration, output_scale, output_offset, port, inputport, outputport, lock, trigger, code, onset, velocity, pitch, duration, thread
+    global patch, name, path, monitor
+    global note_name, note_code, midichannel, mididevice, input_scale, input_offset, scale_velocity, scale_pitch, scale_duration, offset_velocity, offset_pitch, offset_duration, output_scale, output_offset, port, inputport, outputport, lock, trigger, code, onset, velocity, pitch, duration, thread
 
     for msg in inputport.iter_pending():
         if midichannel is None:
             try:
                 # specify the MIDI channel on the basis of the first incoming message
                 midichannel = int(msg.channel)
                 monitor.update('midichannel', midichannel)
@@ -316,26 +299,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('KEYBOARD_UNBLOCK', 1)
+    patch.publish('KEYBOARD_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/launchcontrol/__init__.py` & `eegsynth-0.7.0/module/spectral/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .launchcontrol import _setup, _start, _loop_once, _loop_forever, _stop
+from .spectral import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/launchcontrol/launchcontrol.py` & `eegsynth-0.7.0/module/launchcontrol/launchcontrol.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -55,49 +52,33 @@
     	outputport.send(mido.Message('note_on', note=int(note), velocity=color, channel=midichannel))
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    if not 'general' in config:
-        raise RuntimeError("cannot read configuration from " + args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, push, toggle1, toggle2, toggle3, toggle4, slap, scale_note, scale_control, offset_note, offset_control, mididevice_input, mididevice_output, port, inputport, Off, Red_Low, Red_Full, Amber_Low, Amber_Full, Yellow_Full, Green_Low, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global push, toggle1, toggle2, toggle3, toggle4, slap, scale_note, scale_control, offset_note, offset_control, mididevice_input, mididevice_output, port, inputport, Off, Red_Low, Red_Full, Amber_Low, Amber_Full, Yellow_Full, Green_Low, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
 
     # get the options from the configuration file
     push        = patch.getint('button', 'push',    multiple=True)      # push-release button
     toggle1     = patch.getint('button', 'toggle1', multiple=True)      # on-off button
     toggle2     = patch.getint('button', 'toggle2', multiple=True)      # on1-on2-off button
     toggle3     = patch.getint('button', 'toggle3', multiple=True)      # on1-on2-on3-off button
     toggle4     = patch.getint('button', 'toggle4', multiple=True)      # on1-on2-on3-on4-off button
@@ -211,16 +192,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, push, toggle1, toggle2, toggle3, toggle4, slap, scale_note, scale_control, offset_note, offset_control, mididevice_input, mididevice_output, port, inputport, Off, Red_Low, Red_Full, Amber_Low, Amber_Full, Yellow_Full, Green_Low, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
+    global patch, name, path, monitor
+    global push, toggle1, toggle2, toggle3, toggle4, slap, scale_note, scale_control, offset_note, offset_control, mididevice_input, mididevice_output, port, inputport, Off, Red_Low, Red_Full, Amber_Low, Amber_Full, Yellow_Full, Green_Low, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
 
     for msg in inputport.iter_pending():
         if midichannel is None:
             # specify the MIDI channel on the basis of the first incoming message
             try:
                 midichannel = int(msg.channel)
                 monitor.update('midichannel', midichannel)
@@ -313,19 +294,19 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
-
+    pass
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/launchpad/__init__.py` & `eegsynth-0.7.0/module/outputaudio/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .launchpad import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputaudio import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/launchpad/launchpad.py` & `eegsynth-0.7.0/module/launchpad/launchpad.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -55,46 +52,33 @@
         outputport.send(mido.Message('note_on', note=int(note), velocity=color, channel=midichannel))
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, push, toggle1, toggle2, toggle3, toggle4, slap, model, scale_note, scale_control, offset_note, offset_control, port, mididevice_input, mididevice_output, inputport, Off, Red_Full, Amber_Full, Yellow_Full, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global push, toggle1, toggle2, toggle3, toggle4, slap, model, scale_note, scale_control, offset_note, offset_control, port, mididevice_input, mididevice_output, inputport, Off, Red_Full, Amber_Full, Yellow_Full, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
 
     # get the options from the configuration file
     debug       = patch.getint('general','debug')
     push        = patch.getint('button', 'push',    multiple=True)    # push-release button
     toggle1     = patch.getint('button', 'toggle1', multiple=True)    # on-off button
     toggle2     = patch.getint('button', 'toggle2', multiple=True)    # on1-on2-off button
     toggle3     = patch.getint('button', 'toggle3', multiple=True)    # on1-on2-on3-off button
@@ -222,16 +206,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, push, toggle1, toggle2, toggle3, toggle4, slap, model, scale_note, scale_control, offset_note, offset_control, port, mididevice_input, mididevice_output, inputport, Off, Red_Full, Amber_Full, Yellow_Full, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
+    global patch, name, path, monitor
+    global push, toggle1, toggle2, toggle3, toggle4, slap, model, scale_note, scale_control, offset_note, offset_control, port, mididevice_input, mididevice_output, inputport, Off, Red_Full, Amber_Full, Yellow_Full, Green_Full, ledcolor, note_list, status_list, note, state0change, state0color, state0value, state1change, state1color, state1value, state2change, state2color, state2value, state3change, state3color, state3value, state4change, state4color, state4value, state5change, state5color, state5value, midichannel, outputport
 
     for msg in inputport.iter_pending():
         if midichannel is None:
             try:
                 # specify the MIDI channel on the basis of the first incoming message
                 midichannel = int(msg.channel)
                 monitor.update('midichannel', midichannel)
@@ -322,23 +306,24 @@
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
-        time.sleep(patch.getfloat('general','delay'))
+        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/lsl2ft/__init__.py` & `eegsynth-0.7.0/module/unicorn2ft/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .lsl2ft import _setup, _start, _loop_once, _loop_forever, _stop
+from .unicorn2ft import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/lsl2ft/lsl2ft.py` & `eegsynth-0.7.0/module/lsl2ft/lsl2ft.py`

 * *Files 9% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import pylsl as lsl
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -51,46 +48,33 @@
 import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, timeout, lsl_name, lsl_type, ft_host, ft_port, ft_output, start, selected, streams, stream, inlet, type, source_id, match, lsl_id, channel_count, channel_format, nominal_srate, samples, blocksize
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global timeout, lsl_name, lsl_type, ft_host, ft_port, ft_output, start, selected, streams, stream, inlet, type, source_id, match, lsl_id, channel_count, channel_format, nominal_srate, samples, blocksize
 
     # get the options from the configuration file
     timeout = patch.getfloat('lsl', 'timeout', default=30)
     lsl_name = patch.getstring('lsl', 'name')
     lsl_type = patch.getstring('lsl', 'type')
 
     try:
@@ -158,16 +142,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, timeout, lsl_name, lsl_type, ft_host, ft_port, ft_output, start, selected, streams, stream, inlet, type, source_id, match, lsl_id, channel_count, channel_format, nominal_srate, samples, blocksize
+    global patch, name, path, monitor
+    global timeout, lsl_name, lsl_type, ft_host, ft_port, ft_output, start, selected, streams, stream, inlet, type, source_id, match, lsl_id, channel_count, channel_format, nominal_srate, samples, blocksize
 
     chunk, timestamps = inlet.pull_chunk()
     if timestamps:
         dat = np.asarray(chunk, dtype=np.float32)
         ft_output.putData(dat)
         blocksize = dat.shape[0]
         samples += blocksize
@@ -184,22 +168,22 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_output
     ft_output.disconnect()
     monitor.success('Disconnected from output FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/modulatetone/__init__.py` & `eegsynth-0.7.0/module/outputcvgate/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .modulatetone import _setup, _start, _loop_once, _loop_forever, _stop
+from .outputcvgate import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/modulatetone/modulatetone.py` & `eegsynth-0.7.0/module/modulatetone/modulatetone.py`

 * *Files 13% similar despite different names*

```diff
@@ -15,28 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import signal
 import threading
 import pyaudio
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -61,15 +58,15 @@
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
         global modulation, frequencies, control, channame, scale_amplitude, offset_amplitude, scale_frequency, offset_frequency
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         # this message unblocks the Redis listen command
         pubsub.subscribe('MODULATETONE_UNBLOCK')
         # this message triggers the event
         pubsub.subscribe(self.redischannel)
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
@@ -124,50 +121,32 @@
     return buf, pyaudio.paContinue
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'),
-                        help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint(
-            'redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    global patch, name, path, monitor
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug
+    global patch, name, path, monitor
     global device, mode, rate, modulation, offset, control, scale_amplitude, offset_amplitude, scale_frequency, offset_frequency, nchans, channame, ntones, frequencies, lock, stream, trigger, thread, p
 
     # get the options from the configuration file
     device = patch.getint('audio', 'device')
     rate = patch.getint('audio', 'rate', default=22050)
     nchans = patch.getint("audio", "nchans", default=2)
     modulation = patch.getstring('audio', 'modulation', default='am')
@@ -199,15 +178,15 @@
     trigger = []
     # configure the trigger threads for the control signals
     channame = ['left', 'right', 'chan3', 'chan4', 'chan5', 'chan6', 'chan7', 'chan8']
     for chan in range(0, nchans):
         for tone in range(0, ntones):
             tonestr = "tone%d" % (tone + 1)
             if patch.hasitem(channame[chan], tonestr):
-                redischannel = patch.getstring(channame[chan], tonestr)
+                redischannel = patch.get(channame[chan], tonestr)
                 trigger.append(TriggerThread(redischannel, chan, tone))
                 monitor.info("configured " + channame[chan] + " " + tonestr + " as " + redischannel)
             else:
                 monitor.info("not configured " + channame[chan] + " " + tonestr)
 
     # start the thread for each of the triggers
     for thread in trigger:
@@ -238,16 +217,14 @@
                     output=True,
                     output_device_index=device,
                     stream_callback=callback)
 
     # start the output stream
     stream.start_stream()
 
-    signal.signal(signal.SIGINT, _stop)
-
     if scale_amplitude>1/ntones:
         monitor.warning('the amplitude scaling is too high, clipping might occur')
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
@@ -266,29 +243,29 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, trigger, r, stream, p
+    global monitor, trigger, stream, p
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('MODULATETONE_UNBLOCK', 1)
+    patch.publish('MODULATETONE_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
     stream.stop_stream()
     stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputartnet/__init__.py` & `eegsynth-0.7.0/module/redis/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputartnet import _setup, _start, _loop_once, _loop_forever, _stop
+from .redis import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -14,11 +14,14 @@
 
         while True:
             # keep running until KeyboardInterrupt
             try:
                 _start()
                 _loop_forever()
             except RuntimeError:
-                # restart after one second
-                time.sleep(1)
+                # do not restart
+                raise SystemExit
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `eegsynth-0.6.0/module/outputartnet/outputartnet.py` & `eegsynth-0.7.0/module/outputartnet/outputartnet.py`

 * *Files 10% similar despite different names*

```diff
@@ -15,24 +15,21 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -49,57 +46,44 @@
 import ArtNet
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, address, artnet, dmxsize, dmxframe, prevtime
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global address, artnet, dmxsize, dmxframe, prevtime
 
     # get the options from the configuration file
     debug = patch.getint('general','debug')
 
     # prepare the data for a single universe
     address = [0, 0, patch.getint('artnet','universe')]
     artnet = ArtNet.ArtNet(ip=patch.getstring('artnet','broadcast'), port=patch.getint('artnet','port'))
 
     # determine the size of the universe
     dmxsize = 0
-    chanlist, chanvals = list(map(list, list(zip(*config.items('input')))))
+    chanlist, chanvals = list(map(list, list(zip(*patch.config.items('input')))))
     for chanindx in range(0, 512):
         chanstr = "channel%03d" % (chanindx + 1)
         if chanstr in chanlist:
             # the last channel determines the size
             dmxsize = chanindx + 1
 
     # FIXME the artnet code fails if the size is smaller than 512
@@ -119,16 +103,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, address, artnet, dmxsize, dmxframe, prevtime
+    global patch, name, path, monitor
+    global address, artnet, dmxsize, dmxframe, prevtime
     global update, chanindx, chanstr, chanval, scale, offset
 
     update = False
 
     # loop over the control values, these are 1-offset in the ini file
     for chanindx in range(0, dmxsize):
         chanstr = "channel%03d" % (chanindx + 1)
@@ -175,18 +159,18 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, artnet
-    monitor.success("Closing module...")
+    monitor.success("Stopping module...")
     # blank out
     dmxframe = [0] * 512
     artnet.broadcastDMX(dmxframe,address)
     time.sleep(0.1) # this seems to take some time
     artnet.broadcastDMX(dmxframe,address)
     time.sleep(0.1) # this seems to take some time
     artnet.broadcastDMX(dmxframe,address)
@@ -194,17 +178,18 @@
     artnet.broadcastDMX(dmxframe,address)
     time.sleep(0.1) # this seems to take some time
     artnet.broadcastDMX(dmxframe,address)
     time.sleep(0.1) # this seems to take some time
     artnet.broadcastDMX(dmxframe,address)
     time.sleep(0.1) # this seems to take some time
     artnet.close()
-    sys.exit()
+    monitor.success("Done.")
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputaudio/__init__.py` & `eegsynth-0.7.0/module/postprocessing/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputaudio import _setup, _start, _loop_once, _loop_forever, _stop
+from .postprocessing import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputaudio/outputaudio.py` & `eegsynth-0.7.0/module/outputaudio/outputaudio.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,28 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import signal
 import threading
 import pyaudio
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -109,63 +106,47 @@
     return buf, pyaudio.paContinue
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, device, window, lrate, scaling_method, scaling, outputrate, scale_scaling, offset_scaling, nchans, inputrate, p, info, i, devinfo, lock, stack, firstsample, stretch, inputblock, outputblock, previnput, prevoutput, stream, begsample, endsample
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    # this is the timeout for the FieldTrip buffer
+    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to input FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to input FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, device, window, lrate, scaling_method, scaling, outputrate, scale_scaling, offset_scaling, nchans, inputrate, p, info, i, devinfo, lock, stack, firstsample, stretch, inputblock, outputblock, previnput, prevoutput, stream, begsample, endsample
-
-    # this is the timeout for the FieldTrip buffer
-    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
-
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
         if (time.time() - start) > timeout:
             raise RuntimeError("timeout while waiting for data")
         time.sleep(0.1)
@@ -230,16 +211,14 @@
                     output=True,
                     output_device_index=device,
                     stream_callback=callback)
 
     # it should not start playing immediately
     stream.stop_stream()
 
-    signal.signal(signal.SIGINT, _stop)
-
     # jump to the end of the input stream
     if hdr_input.nSamples - 1 < window:
         begsample = 0
         endsample = window - 1
     else:
         begsample = hdr_input.nSamples - window
         endsample = hdr_input.nSamples - 1
@@ -249,16 +228,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, device, window, lrate, scaling_method, scaling, outputrate, scale_scaling, offset_scaling, nchans, inputrate, p, info, i, devinfo, lock, stack, firstsample, stretch, inputblock, outputblock, previnput, prevoutput, stream, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, device, window, lrate, scaling_method, scaling, outputrate, scale_scaling, offset_scaling, nchans, inputrate, p, info, i, devinfo, lock, stack, firstsample, stretch, inputblock, outputblock, previnput, prevoutput, stream, begsample, endsample
     global dat, now, old, new, duration
 
     # measure the time that it takes
     start = time.time()
 
     # wait only shortly, update the header after waiting
     # this fails when the data streams is stalled or when the buffer resets
@@ -329,24 +308,26 @@
     '''
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
-def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+def _stop(*args):
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global stream, p
+    global monitor, ft_input, stream, p
+    ft_input.disconnect()
+    monitor.success('Disconnected from input FieldTrip buffer')
     stream.stop_stream()
     stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputcvgate/__init__.py` & `eegsynth-0.7.0/module/sampler/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputcvgate import _setup, _start, _loop_once, _loop_forever, _stop
+from .sampler import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputcvgate/outputcvgate.py` & `eegsynth-0.7.0/module/outputcvgate/outputcvgate.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,28 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import threading
 import time
 import serial
 import serial.tools.list_ports
 from fuzzywuzzy import process
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -72,15 +69,15 @@
         self.chanstr = chanstr
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         # this message unblocks the Redis listen command
         pubsub.subscribe('OUTPUTCVGATE_UNBLOCK')
         # this message triggers the event
         pubsub.subscribe(self.redischannel)
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
@@ -119,45 +116,33 @@
                             t.start()
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, duration_scale, duration_offset, serialdevice, s, lock, trigger, chanindx, chanstr, redischannel, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global duration_scale, duration_offset, serialdevice, s, lock, trigger, chanindx, chanstr, redischannel, thread
 
     # values between 0 and 1 work well for the duration
     duration_scale = patch.getfloat('duration', 'scale', default=1)
     duration_offset = patch.getfloat('duration', 'offset', default=0)
 
     # get the specified serial device, or the one that is the closest match
     serialdevice = patch.getstring('serial', 'device')
@@ -198,16 +183,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, duration_scale, duration_offset, serialdevice, s, lock, trigger, chanindx, chanstr, redischannel, thread
+    global patch, name, path, monitor
+    global duration_scale, duration_offset, serialdevice, s, lock, trigger, chanindx, chanstr, redischannel, thread
 
     # loop over the control voltages
     for chanindx in range(1, 5):
         chanstr = "cv%d" % chanindx
         # this returns None when the channel is not present
         chanval = patch.getfloat('input', chanstr)
 
@@ -257,26 +242,28 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, trigger, r
+    global monitor, trigger, s
     monitor.success("Closing threads")
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTCVGATE_UNBLOCK', 1)
+    patch.publish('OUTPUTCVGATE_UNBLOCK', 1)
     for thread in trigger:
             thread.join()
-    sys.exit()
+    monitor.success("Closing serial port")
+    s.close()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputdmx/__init__.py` & `eegsynth-0.7.0/module/lsl2ft/__init__.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputdmx import _setup, _start, _loop_once, _loop_forever, _stop
+from .lsl2ft import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputdmx/outputdmx.py` & `eegsynth-0.7.0/module/outputdmx/outputdmx.py`

 * *Files 9% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import serial
 import serial.tools.list_ports
 from fuzzywuzzy import process
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -60,64 +57,50 @@
     s.write(bytearray(packet))
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, serialdevice, s, dmxsize, chanlist, chanvals, chanindx, chanstr, dmxframe, prevtime, START_VAL, END_VAL, TX_DMX_PACKET, FRAME_PAD
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global serialdevice, s, dmxsize, chanlist, chanvals, chanindx, chanstr, dmxframe, prevtime, START_VAL, END_VAL, TX_DMX_PACKET, FRAME_PAD
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
 
     # get the specified serial device, or the one that is the closest match
     serialdevice = patch.getstring('serial', 'device')
     serialdevice = EEGsynth.trimquotes(serialdevice)
     serialdevice = process.extractOne(serialdevice, [comport.device for comport in serial.tools.list_ports.comports()])[0]  # select the closest match
 
     try:
         s = serial.Serial(serialdevice, patch.getint('serial', 'baudrate'), timeout=3.0)
         monitor.info("Connected to serial port")
     except:
         raise RuntimeError("cannot connect to serial port")
 
     # determine the size of the universe
     dmxsize = 0
-    chanlist, chanvals = list(map(list, list(zip(*config.items('input')))))
+    chanlist, chanvals = list(map(list, list(zip(*patch.config.items('input')))))
     for chanindx in range(0, 512):
         chanstr = "channel%03d" % (chanindx + 1)
         if chanstr in chanlist:
             # the last channel determines the size
             dmxsize = chanindx + 1
 
     # my fixture won't work if the frame size is too small
@@ -137,16 +120,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, serialdevice, s, dmxsize, chanlist, chanvals, chanindx, chanstr, dmxframe, prevtime
+    global patch, name, path, monitor
+    global serialdevice, s, dmxsize, chanlist, chanvals, chanindx, chanstr, dmxframe, prevtime
     global update, chanval, scale, offset
 
     update = False
 
     # loop over the control values, these are 1-offset in the ini file
     for chanindx in range(0, dmxsize):
         chanstr = "channel%03d" % (chanindx + 1)
@@ -193,24 +176,25 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, s
-    monitor.success("Closing module...")
+    monitor.success("Stopping module...")
     # blank out everything
     dmxframe = [0] * 512
     sendframe(s, dmxframe)
-    sys.exit()
+    monitor.success("Done.")
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputgpio/__init__.py` & `eegsynth-0.7.0/module/delaytrigger/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputgpio import _setup, _start, _loop_once, _loop_forever, _stop
+from .delaytrigger import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputgpio/outputgpio.py` & `eegsynth-0.7.0/module/outputgpio/outputgpio.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,29 +15,26 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 import threading
 
 # The wiringpi package only works on a Raspberry Pi
 # It is only used inside this specific EEGsynth module, hence it might not be installed by default
 import wiringpi
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -69,15 +66,15 @@
         self.duration = duration
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         # this message unblocks the Redis listen command
         pubsub.subscribe('OUTPUTGPIO_UNBLOCK')
         # this message triggers the event
         pubsub.subscribe(self.redischannel)
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
@@ -101,46 +98,33 @@
                         t.start()
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, pin, debug, delay, scale_duration, offset_duration, lock, trigger
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global pin, delay, scale_duration, offset_duration, lock, trigger
 
     # make a dictionary that maps GPIOs to the WiringPi number
     pin = {
         "gpio0": 0,
         "gpio1": 1,
         "gpio2": 2,
         "gpio3": 3,
@@ -156,38 +140,37 @@
         "gpio26": 26,
         "gpio27": 27,
         "gpio28": 28,
         "gpio29": 29,
     }
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     delay = patch.getfloat('general', 'delay')
 
     # values between 0 and 1 work well for the duration
     scale_duration = patch.getfloat('scale', 'duration', default=1)
     offset_duration = patch.getfloat('offset', 'duration', default=0)
 
     # this is to prevent two triggers from being activated at the same time
     lock = threading.Lock()
 
     # use the WiringPi numbering, see http://wiringpi.com/reference/setup/
     wiringpi.wiringPiSetup()
 
     # set up PWM for the control channels
     previous_val = {}
-    for gpio, channel in config.items('control'):
+    for gpio, channel in patch.config.items('control'):
         monitor.info("control " + channel + " " + gpio)
         wiringpi.softPwmCreate(pin[gpio], 0, 100)
         # control values are only relevant when different from the previous value
         previous_val[gpio] = None
 
     # create the threads that deal with the triggers
     trigger = []
-    for gpio, channel in config.items('trigger'):
+    for gpio, channel in patch.config.items('trigger'):
         wiringpi.pinMode(pin[gpio], 1)
         duration = patch.getstring('duration', gpio)
         trigger.append(TriggerThread(channel, gpio, duration))
         monitor.info("trigger " + channel + " " + gpio)
 
     # start the thread for each of the triggers
     for thread in trigger:
@@ -198,17 +181,17 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    for gpio, channel in config.items('control'):
+    for gpio, channel in patch.config.items('control'):
         val = patch.getfloat('control', gpio)
 
         if val == None:
             continue  # it should be skipped when not present
         if val == previous_val[gpio]:
             continue  # it should be skipped when identical to the previous value
         previous_val[gpio] = val
@@ -233,26 +216,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTGPIO_UNBLOCK', 1)
+    patch.publish('OUTPUTGPIO_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputlsl/__init__.py` & `eegsynth-0.7.0/module/outputlsl/__init__.py`

 * *Files 16% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputlsl/outputlsl.py` & `eegsynth-0.7.0/module/outputlsl/outputlsl.py`

 * *Files 14% similar despite different names*

```diff
@@ -15,28 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
 import random
-import redis
 import string
 import sys
 import threading
 import time
 from pylsl import StreamInfo, StreamOutlet
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -48,33 +45,27 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
-def randomStringDigits(stringLength=6):
-    """Generate a random string of digits """
-    letters = string.digits
-    return ''.join(random.choice(letters) for i in range(stringLength))
-
-
 class TriggerThread(threading.Thread):
     def __init__(self, redischannel, trigger):
         threading.Thread.__init__(self)
         self.redischannel = redischannel
         self.name = trigger
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
         global r, lsl_format, patch, lock, monitor, outlet
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('OUTPUTLSL_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)  # this message contains the trigger
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -94,94 +85,79 @@
                         outlet.push_sample([marker])
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, lsl_name, lsl_type, lsl_id, lsl_format, info, outlet, trigger, item, lock, thread, previous_val
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global lsl_name, lsl_type, lsl_id, lsl_format, info, outlet, trigger, item, lock, thread, previous_val
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-
     lsl_name = patch.getstring('lsl', 'name', default='eegsynth')
     lsl_type = patch.getstring('lsl', 'type', default='Markers')
-    lsl_id = patch.getstring('lsl', 'id', default=randomStringDigits())
+    lsl_id = patch.getstring('lsl', 'id', default=EEGsynth.uuid(6))
     lsl_format = patch.getstring('lsl', 'format')
 
     # create an outlet stream
     info = StreamInfo(lsl_name, lsl_type, 1, 0, 'string', lsl_id)
     outlet = StreamOutlet(info)
 
     # create the background threads that deal with the triggers
     trigger = []
     monitor.info("Setting up threads for each trigger")
-    for item in config.items('trigger'):
+    for item in patch.config.items('trigger'):
         trigger.append(TriggerThread(item[1], item[0]))
         monitor.debug(str(item[0]) + " " + str(item[1]) + " OK")
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     # start the thread for each of the triggers
     for thread in trigger:
         thread.start()
 
     previous_val = {}
-    for item in config.items('control'):
+    for item in patch.config.items('control'):
         key = item[0]
         previous_val[key] = None
 
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, lsl_name, lsl_type, lsl_id, lsl_format, info, outlet, trigger, item, lock, thread, previous_val
+    global patch, name, path, monitor
+    global lsl_name, lsl_type, lsl_id, lsl_format, info, outlet, trigger, item, lock, thread, previous_val
     global val, marker
 
     # loop over the control values
-    for item in config.items('control'):
+    for item in patch.config.items('control'):
         key = item[0]
 
         val = patch.getfloat('control', key)
         if val is None:
             continue  # it should be skipped when not present in the ini or Redis
         if val == previous_val[key]:
             continue  # it should be skipped when identical to the previous value
@@ -213,21 +189,21 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTLSL_UNBLOCK', 1)
+    patch.publish('OUTPUTLSL_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
     sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
```

### Comparing `eegsynth-0.6.0/module/outputmidi/__init__.py` & `eegsynth-0.7.0/module/compressor/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputmidi import _setup, _start, _loop_once, _loop_forever, _stop
+from .compressor import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputmidi/outputmidi.py` & `eegsynth-0.7.0/module/outputmidi/outputmidi.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,27 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
+import numpy as np
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -48,15 +46,15 @@
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path,'../../lib'))
 import EEGsynth
 
 
 def UpdateParameters():
-    global patch, velocity_note, scale_velocity, offset_velocity, duration_note, scale_duration, offset_duration
+    global patch, name, path, monitor, velocity_note, scale_velocity, offset_velocity, duration_note, scale_duration, offset_duration
     velocity_note = patch.getfloat('velocity', 'note', default=64)
     velocity_note = int(EEGsynth.rescale(velocity_note, slope=scale_velocity, offset=offset_velocity))
     duration_note = patch.getfloat('duration', 'note', default=None)
     if duration_note != None:
         duration_note = EEGsynth.rescale(duration_note, slope=scale_duration, offset=offset_duration)
         # some minimal time is needed for the duration
         duration_note = EEGsynth.limit(duration_note, 0.05, float('Inf'))
@@ -95,14 +93,18 @@
     outputport.send(msg)
 
 
 # send the MIDI message, different messages have slightly different parameters
 def sendMidi(name, code, val):
     global previous
 
+    if np.isnan(val):
+        # monitor.error('cannot send NaN as MIDI message')
+        return
+
     if name == 'pitchwheel':
         # the value should be limited between -8192 to 8191
         val = EEGsynth.limit(val, -8192, 8191)
         val = int(val)
     else:
         # the value should be limited between 0 and 127
         val = EEGsynth.limit(val, 0, 127)
@@ -158,15 +160,15 @@
         self.redischannel = redischannel
         self.name = name
         self.code = code
         self.running = True
     def stop(self):
         self.running = False
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('OUTPUTMIDI_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)     # this message contains the value of interest
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel']==self.redischannel:
@@ -181,49 +183,35 @@
                         sendMidi(self.name, self.code, val)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global debug, mididevice, port, previous_note, trigger_name, trigger_code, code, trigger, this, thread, control_name, control_code, previous_val, duration_note, lock, midichannel, monitor, monophonic, offset_duration, offset_velocity, outputport, scale_duration, scale_velocity, velocity_note
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global mididevice, port, previous_note, trigger_name, trigger_code, code, trigger, this, thread, control_name, control_code, previous_val, duration_note, lock, midichannel, monitor, monophonic, offset_duration, offset_velocity, outputport, scale_duration, scale_velocity, velocity_note
 
     # get the options from the configuration file
-    debug       = patch.getint('general', 'debug')
     monophonic  = patch.getint('general', 'monophonic', default=1)
     midichannel = patch.getint('midi', 'channel')-1  # channel 1-16 get mapped to 0-15
     mididevice  = patch.getstring('midi', 'device')
     mididevice  = EEGsynth.trimquotes(mididevice)
     mididevice  = process.extractOne(mididevice, mido.get_output_names())[0] # select the closest match
 
     # values between 0 and 1 work well for the note duration
@@ -270,17 +258,17 @@
     for name in ['note', 'aftertouch', 'pitchwheel', 'start', 'continue', 'stop', 'reset']:
         trigger_name.append(name)
         trigger_code.append(None)
 
     # each of the Redis messages is mapped onto a different MIDI message
     trigger = []
     for name, code in zip(trigger_name, trigger_code):
-        if config.has_option('trigger', name):
+        if patch.config.has_option('trigger', name):
             # start the background thread that deals with this note
-            this = TriggerThread(patch.getstring('trigger', name), name, code)
+            this = TriggerThread(patch.get('trigger', name), name, code)
             trigger.append(this)
             monitor.debug(name + ' trigger configured')
 
     # start the thread for each of the triggers
     for thread in trigger:
         thread.start()
 
@@ -307,16 +295,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global debug, mididevice, port, previous_note, trigger_name, trigger_code, code, trigger, this, thread, control_name, control_code, previous_val, duration_note, lock, midichannel, monitor, monophonic, offset_duration, offset_velocity, outputport, scale_duration, scale_velocity, velocity_note
+    global patch, name, path, monitor
+    global mididevice, port, previous_note, trigger_name, trigger_code, code, trigger, this, thread, control_name, control_code, previous_val, duration_note, lock, midichannel, monitor, monophonic, offset_duration, offset_velocity, outputport, scale_duration, scale_velocity, velocity_note
 
     UpdateParameters()
 
     for name, code in zip(control_name, control_code):
         # loop over the control values
         val = patch.getfloat('control', name)
         if val is None:
@@ -340,22 +328,21 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
-
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTMIDI_UNBLOCK', 1)
+    patch.publish('OUTPUTMIDI_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
```

### Comparing `eegsynth-0.6.0/module/outputmqtt/__init__.py` & `eegsynth-0.7.0/module/volcakeys/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputmqtt import _setup, _start, _loop_once, _loop_forever, _stop
+from .volcakeys import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputmqtt/outputmqtt.py` & `eegsynth-0.7.0/module/outputmqtt/outputmqtt.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import string
 import sys
 import threading
 import time
 import paho.mqtt.client as mqtt
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -59,15 +56,15 @@
         self.mqtttopic = mqtttopic
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('OUTPUTMQTT_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)     # this message contains the value of interest
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -104,53 +101,39 @@
         monitor.info("MQTT disconnected")
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread, client
+    global patch, name, path, monitor
+    global list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread, client
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
 
     # keys should be present in both the input and output section of the *.ini file
-    list_input = config.items('input')
-    list_output = config.items('output')
+    list_input = patch.config.items('input')
+    list_output = patch.config.items('output')
 
     list1 = []  # the key name that matches in the input and output section of the *.ini file
     list2 = []  # the key name in Redis
     list3 = []  # the key name in OSC
     for i in range(len(list_input)):
         for j in range(len(list_output)):
             if list_input[i][0] == list_output[j][0]:
@@ -171,15 +154,15 @@
     # start the thread for each of the triggers
     for thread in trigger:
         thread.start()
 
     # make the connection with the MQTT broker
     try:
         client = mqtt.Client()
-        client.connect(config.get('mqtt', 'hostname'), config.getint('mqtt', 'port'), config.getint('mqtt', 'timeout'))
+        client.connect(patch.get('mqtt', 'hostname'), patch.getint('mqtt', 'port'), patch.getint('mqtt', 'timeout'))
         client.on_connect = on_connect
         client.on_message = on_message
         client.on_disconnect = on_disconnect
     except:
         raise RuntimeError("Cannot connect to MQTT broker")
 
     # there should not be any local variables in this function, they should all be global
@@ -200,26 +183,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTMQTT_UNBLOCK', 1)
+    patch.publish('OUTPUTMQTT_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputosc/__init__.py` & `eegsynth-0.7.0/module/preprocessing/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputosc import _setup, _start, _loop_once, _loop_forever, _stop
+from .preprocessing import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputosc/outputosc.py` & `eegsynth-0.7.0/module/outputosc/outputosc.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,18 +15,15 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import threading
 import time
 
 # The required package depends on the Python version, one works for older and the other for newer versions.
 # This cannot be handled easily by setup.py during installation, hence we only _try_ to load the module.
 if sys.version_info < (3,5):
@@ -42,15 +39,15 @@
         use_old_version = False
     except ModuleNotFoundError:
         # give a warning, not an error, so that eegsynth.py does not fail as a whole
         print('Warning: pythonosc is required for the outputosc module, please install it with "pip install pythonosc"')
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -72,15 +69,15 @@
         self.redischannel = redischannel
         self.name = name
         self.osctopic = osctopic
         self.running = True
     def stop(self):
         self.running = False
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('OUTPUTOSC_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)     # this message contains the value of interest
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel']==self.redischannel:
@@ -103,63 +100,49 @@
                             s.send_message(self.osctopic, val)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, s, list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    global patch, name, path, monitor
+    global s, list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread
 
     try:
         if use_old_version:
             s = OSC.OSCClient()
             s.connect((patch.getstring('osc','hostname'), patch.getint('osc','port')))
         else:
             s = udp_client.SimpleUDPClient(patch.getstring('osc','hostname'), patch.getint('osc','port'))
         monitor.success('Connected to OSC server')
     except:
         raise RuntimeError("Cannot connect to OSC server")
 
+    # get the options from the configuration file
+
     # keys should be present in both the input and output section of the *.ini file
-    list_input  = config.items('input')
-    list_output = config.items('output')
+    list_input  = patch.config.items('input')
+    list_output = patch.config.items('output')
 
     list1 = [] # the key name that matches in the input and output section of the *.ini file
     list2 = [] # the key name in Redis
     list3 = [] # the key name in OSC
     for i in range(len(list_input)):
         for j in range(len(list_output)):
             if list_input[i][0]==list_output[j][0]:
@@ -199,26 +182,26 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTOSC_UNBLOCK', 1)
+    patch.publish('OUTPUTOSC_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/outputzeromq/__init__.py` & `eegsynth-0.7.0/module/endorphines/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .outputzeromq import _setup, _start, _loop_once, _loop_forever, _stop
+from .endorphines import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/outputzeromq/outputzeromq.py` & `eegsynth-0.7.0/module/recordtrigger/recordtrigger.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,41 +1,38 @@
 #!/usr/bin/env python
 
-# This module translates Redis controls to ZeroMQ messages.
+# This module records Redis messages (i.e. triggers) to a TSV file
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
-# Copyright (C) 2019 EEGsynth project
+# Copyright (C) 2018-2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
+import datetime
 import os
-import redis
-import string
 import sys
-import threading
 import time
-import zmq
+import threading
+import tempfile
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -48,164 +45,178 @@
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
 class TriggerThread(threading.Thread):
-    def __init__(self, redischannel, name, zeromqtopic):
+    def __init__(self, redischannel):
         threading.Thread.__init__(self)
         self.redischannel = redischannel
-        self.name = name
-        self.zeromqtopic = zeromqtopic
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        global r, patch, monitor, socket
-        pubsub = r.pubsub()
-        pubsub.subscribe('OUTPUTZEROMQ_UNBLOCK')  # this message unblocks the redis listen command
-        pubsub.subscribe(self.redischannel)       # this message contains the value of interest
+        global r, monitor, lock
+        global f, csvwriter
+        pubsub = patch.pubsub()
+        pubsub.subscribe('RECORDTRIGGER_UNBLOCK')  # this message unblocks the Redis listen command
+        pubsub.subscribe(self.redischannel)        # this message triggers the event
         while self.running:
             for item in pubsub.listen():
+                timestamp = datetime.datetime.now().isoformat()
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
-                    # map the Redis values to ZeroMQ values
-                    val = float(item['data'])
-                    # the scale and offset options are channel specific
-                    scale = patch.getfloat('scale', self.name, default=1)
-                    offset = patch.getfloat('offset', self.name, default=0)
-                    # apply the scale and offset
-                    val = EEGsynth.rescale(val, slope=scale, offset=offset)
-
-                    monitor.update(self.zeromqtopic, val)
-                    with lock:
-                        # send it as a string with a space as separator
-                        socket.send_string("%s %f" % (self.zeromqtopic, val))
-
+                    val = item["data"]
+                    # the trigger value should be saved
+                    if input_scale != None or input_offset != None:
+                        try:
+                            # convert it to a number and apply the scaling and the offset
+                            val = float(val)
+                            val = EEGsynth.rescale(val, slope=input_scale, offset=input_offset)
+                        except ValueError:
+                            # keep it as a string
+                            monitor.info(("cannot apply scaling, writing %s as string" % (self.redischannel)))
+                    if f and not f.closed:
+                        # write the value, it can be either a number or a string
+                        with lock:
+                            csvwriter.writerow([self.redischannel, val, timestamp])
+                        monitor.info(("%s\t%s\t%s" % (self.redischannel, val, timestamp)))
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    if not 'general' in config:
-        raise RuntimeError("cannot read configuration from " + args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, list_input, list_output, list1, list2, list3, i, j, lock, trigger, key1, key2, key3, this, thread, context, socket
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, input_scale, input_offset, filename, fileformat, f, recording, filenumber, lock, trigger, item, thread
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    delay = patch.getfloat('general', 'delay')
+    input_scale = patch.getfloat('input', 'scale', default=None)
+    input_offset = patch.getfloat('input', 'offset', default=None)
+    filename = patch.getstring('recording', 'file')
+    fileformat = patch.getstring('recording', 'format')
+
+    if fileformat is None:
+        # determine the file format from the file name
+        name, ext = os.path.splitext(filename)
+        fileformat = ext[1:]
+
+    # start with a temporary file which is immediately closed
+    f = tempfile.TemporaryFile().close()
+    recording = False
+    filenumber = 0
 
-    # keys should be present in both the input and output section of the *.ini file
-    list_input = config.items('input')
-    list_output = config.items('output')
-
-    list1 = []  # the key name that matches in the input and output section of the *.ini file
-    list2 = []  # the key name in Redis
-    list3 = []  # the key name in ZeroMQ
-    for i in range(len(list_input)):
-        for j in range(len(list_output)):
-            if list_input[i][0] == list_output[j][0]:
-                list1.append(list_input[i][0])  # short name in the ini file
-                list2.append(list_input[i][1])  # redis channel
-                list3.append(list_output[j][1])  # zeromq topic
-
-    # this is to prevent two messages from being sent at the same time
+    # this is to prevent two triggers from being saved at the same time
     lock = threading.Lock()
 
-    # each of the Redis messages is mapped onto a different ZeroMQ topic
+    # create the background threads that deal with the triggers
     trigger = []
-    for key1, key2, key3 in zip(list1, list2, list3):
-        this = TriggerThread(key2, key1, key3)
-        trigger.append(this)
-        monitor.debug(key1 + ' trigger configured')
+    monitor.info("Setting up threads for each trigger")
+    for item in patch.config.items('trigger'):
+        trigger.append(TriggerThread(item[0]))
+        monitor.debug(item[0] + ' = OK')
 
     # start the thread for each of the triggers
     for thread in trigger:
         thread.start()
 
-    # make the connection with ZeroMQ
-    try:
-        context = zmq.Context()
-        socket = context.socket(zmq.PUB)
-        socket.bind("tcp://*:%i" % config.getint('zeromq', 'port'))
-        socket.send_string('Hello')
-    except:
-        raise RuntimeError("cannot connect to ZeroMQ")
-
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
+    This uses the global variables from setup and start, and adds a set of global variables
     '''
-    pass
+    global patch, name, path, monitor
+    global delay, input_scale, input_offset, filename, fileformat, recording, filenumber, lock, trigger, item, thread
+    global fname, ext, f, csvwriter
+
+    if recording and not patch.getint('recording', 'record'):
+        monitor.info("Recording disabled - closing " + fname)
+        f.close()
+        recording = False
+        return
+
+    if not recording and not patch.getint('recording', 'record'):
+        monitor.info("Recording is not enabled")
+        time.sleep(1)
+
+    if not recording and patch.getint('recording', 'record'):
+        recording = True
+        # open a new file
+        name, ext = os.path.splitext(filename)
+        if len(ext) == 0:
+            ext = '.' + fileformat
+        fname = name + '_' + datetime.datetime.now().strftime("%Y.%m.%d_%H.%M.%S") + ext
+        monitor.info("Recording enabled - opening " + fname)
+        
+        f = open(fname, 'w')
+        if fileformat == 'csv':
+            csvwriter = csv.writer(f, delimiter=',')
+        elif fileformat == 'tsv':
+            csvwriter = csv.writer(f, delimiter='\t')
+        csvwriter.writeheader(["event", "value", "timestamp"])
+        f.flush()
+
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
-def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+def _stop(*args):
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, trigger, r, context
+    global monitor, patch, trigger, recording, fname, f
+    if recording:
+        recording = False
+        monitor.info("Closing " + fname)
+        f.close()
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('OUTPUTZEROMQ_UNBLOCK', 1)
+    patch.publish('RECORDTRIGGER_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    context.destroy()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/playbackcontrol/__init__.py` & `eegsynth-0.7.0/module/playbacksignal/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .playbackcontrol import _setup, _start, _loop_once, _loop_forever, _stop
+from .playbacksignal import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/playbackcontrol/playbackcontrol.py` & `eegsynth-0.7.0/module/playbackcontrol/playbackcontrol.py`

 * *Files 8% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -50,49 +47,35 @@
 import EDF
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, filename, f, chanindx, channels, channelz, fSample, nSamples, replace, i, s, z, blocksize, begsample, endsample, block
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global filename, f, chanindx, channels, channelz, fSample, nSamples, replace, i, s, z, blocksize, begsample, endsample, block
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     filename = patch.getstring('playback', 'file')
 
     monitor.info("Reading data from " + filename)
 
     f = EDF.EDFReader()
     f.open(filename)
 
@@ -110,15 +93,15 @@
     channels = f.getSignalTextLabels()
     channelz = f.getSignalTextLabels()
 
     fSample = f.getSignalFreqs()[0]
     nSamples = f.getNSamples()[0]
 
     # search-and-replace to reduce the length of the channel labels
-    for replace in config.items('replace'):
+    for replace in patch.config.items('replace'):
         monitor.debug(replace)
         for i in range(len(channelz)):
             channelz[i] = channelz[i].replace(replace[0], replace[1])
     for s, z in zip(channels, channelz):
         monitor.info("Writing channel " + s + " as control value " + z)
 
     # this should write data in one-sample blocks
@@ -132,16 +115,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, filename, f, chanindx, channels, channelz, fSample, nSamples, replace, i, s, z, blocksize, begsample, endsample, block
+    global patch, name, path, monitor
+    global filename, f, chanindx, channels, channelz, fSample, nSamples, replace, i, s, z, blocksize, begsample, endsample, block
     global indx, val, stepsize, elapsed, naptime
 
     if endsample > nSamples - 1:
         monitor.info("End of file reached, jumping back to start")
         begsample = 0
         endsample = blocksize - 1
         block = 0
@@ -178,15 +161,15 @@
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -194,19 +177,20 @@
         naptime = stepsize - elapsed
         if naptime > 0:
             # this approximates the real time streaming speed
             time.sleep(naptime)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/playbacksignal/__init__.py` & `eegsynth-0.7.0/module/pepipiaf/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .playbacksignal import _setup, _start, _loop_once, _loop_forever, _stop
+from .pepipiaf import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/playbacksignal/playbacksignal.py` & `eegsynth-0.7.0/module/playbacksignal/playbacksignal.py`

 * *Files 7% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import wave
 import struct
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -53,207 +50,205 @@
 import EDF
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument('-i', '--inifile', default=os.path.join(path, name + '.ini'), help='name of the configuration file')
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError('cannot connect to Redis server')
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, filename, fileformat, ext, ft_host, ft_port, ft_output, H, MININT8, MAXINT8, MININT16, MAXINT16, MININT32, MAXINT32, f, chanindx, labels, A, blocksize, begsample, endsample, block
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # get the options from the configuration file
-    filename = patch.getstring('playback', 'file')
-    fileformat = patch.getstring('playback', 'format')
-
-    if fileformat is None:
-        # determine the file format from the file name
-        name, ext = os.path.splitext(filename)
-        fileformat = ext[1:]
-
-    monitor.info('Reading data from ' + filename)
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, filename, fileformat, MININT8, MAXINT8, MININT16, MAXINT16, MININT32, MAXINT32, stepsize, playback
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success('Connected to FieldTrip buffer')
     except:
         raise RuntimeError('cannot connect to FieldTrip buffer')
 
-    H = FieldTrip.Header()
+    # get the options from the configuration file
+    filename = patch.getstring('playback', 'file')
+    fileformat = patch.getstring('playback', 'format')
+
+    if fileformat is None:
+        # determine the file format from the file name
+        name, ext = os.path.splitext(filename)
+        fileformat = ext[1:]
 
     MININT8 = -np.power(2., 7)
     MAXINT8 = np.power(2., 7) - 1
     MININT16 = -np.power(2., 15)
     MAXINT16 = np.power(2., 15) - 1
     MININT32 = -np.power(2., 31)
     MAXINT32 = np.power(2., 31) - 1
 
-    if fileformat == 'edf':
-        f = EDF.EDFReader()
-        f.open(filename)
-        for chanindx in range(f.getNSignals()):
-            if f.getSignalFreqs()[chanindx] != f.getSignalFreqs()[0]:
-                raise AssertionError('unequal SignalFreqs')
-            if f.getNSamples()[chanindx] != f.getNSamples()[0]:
-                raise AssertionError('unequal NSamples')
-        H.nChannels = len(f.getSignalFreqs())
-        H.fSample = f.getSignalFreqs()[0]
-        H.nSamples = f.getNSamples()[0]
-        H.nEvents = 0
-        H.dataType = FieldTrip.DATATYPE_FLOAT32
-        # the channel labels will be written to the buffer
-        labels = f.getSignalTextLabels()
-        # read all the data from the file
-        A = np.ndarray(shape=(H.nSamples, H.nChannels), dtype=np.float32)
-        for chanindx in range(H.nChannels):
-            monitor.info('reading channel ' + str(chanindx))
-            A[:, chanindx] = f.readSignal(chanindx)
-        f.close()
-
-    elif fileformat == 'wav':
-        try:
-            physical_min = patch.getfloat('playback', 'physical_min')
-        except:
-            physical_min = -1
-        try:
-            physical_max = patch.getfloat('playback', 'physical_max')
-        except:
-            physical_max = 1
-        f = wave.open(filename, 'r')
-        resolution = f.getsampwidth()  # 1, 2 or 4
-        # 8-bit samples are stored as unsigned bytes, ranging from 0 to 255.
-        # 16-bit samples are stored as signed integers in 2's-complement.
-        H.nChannels = f.getnchannels()
-        H.fSample = f.getframerate()
-        H.nSamples = f.getnframes()
-        H.nEvents = 0
-        H.dataType = FieldTrip.DATATYPE_FLOAT32
-        # there are no channel labels
-        labels = None
-        # read all the data from the file
-        x = f.readframes(f.getnframes() * f.getnchannels())
-        f.close()
-        # convert and calibrate
-        if resolution == 2:
-            x = struct.unpack_from('%dh' % f.getnframes() * f.getnchannels(), x)
-            x = np.asarray(x).astype(np.float32).reshape(f.getnframes(), f.getnchannels())
-            y = x / float(MAXINT16)
-        elif resolution == 4:
-            x = struct.unpack_from('%di' % f.getnframes() * f.getnchannels(), x)
-            x = np.asarray(x).astype(np.float32).reshape(f.getnframes(), f.getnchannels())
-            y = x / float(MAXINT32)
-        else:
-            raise NotImplementedError('unsupported resolution')
-        A = y * ((physical_max - physical_min) / 2)
-
-    else:
-        raise NotImplementedError('unsupported file format')
-
-    monitor.debug('nChannels = ' + str(H.nChannels))
-    monitor.debug('nSamples = ' + str(H.nSamples))
-    monitor.debug('fSample = ' + str(H.fSample))
-    monitor.debug('labels = ' + str(labels))
-
-    ft_output.putHeader(H.nChannels, H.fSample, H.dataType, labels=labels)
-
-    blocksize = int(patch.getfloat('playback', 'blocksize') * H.fSample)
-    begsample = 0
-    endsample = blocksize - 1
-    block = 0
+    # this value will be updated later
+    stepsize = patch.getfloat('playback', 'blocksize') / patch.getfloat('playback', 'speed')
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    # the playback will start in _loop_once()
+    playback = False
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, H, A, ft_output, blocksize, begsample, endsample, block
-    global D, stepsize
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_output, filename, fileformat, ext, MININT8, MAXINT8, MININT16, MAXINT16, MININT32, MAXINT32, stepsize, playback
+    global f, H, chanindx, labels, A, blocksize, begsample, endsample, block, D
 
-    if endsample > H.nSamples - 1:
+    if playback and endsample > H.nSamples - 1:
         monitor.info('End of file reached, jumping back to start')
         begsample = 0
         endsample = blocksize - 1
         block = 0
 
-    if patch.getint('playback', 'rewind', default=0):
+    if playback and patch.getint('playback', 'rewind', default=0):
         monitor.info('Rewind pressed, jumping back to start of file')
         begsample = 0
         endsample = blocksize - 1
         block = 0
 
-    if not patch.getint('playback', 'play', default=1):
-        monitor.info('Stopped')
+    if patch.getint('playback', 'pause', default=0):
+        monitor.info('Paused')
+        playback = False
         time.sleep(0.1)
         return
 
-    if patch.getint('playback', 'pause', default=0):
-        monitor.info('Paused')
+    if not patch.getint('playback', 'play', default=1):
+        monitor.info('Stopped')
+        playback = False
         time.sleep(0.1)
         return
 
-    monitor.info('Playing block ' + str(block) + ' from ' + str(begsample) + ' to ' + str(endsample))
+    if not playback and patch.getint('playback', 'play'):
+        monitor.info('Reading data from ' + filename)
+        playback = True
+
+        # determine the filename, it may have changed
+        filename = patch.getstring('playback', 'file')
+
+        # construct the corresponding EEG header
+        H = FieldTrip.Header()
+
+        if fileformat == 'edf':
+            f = EDF.EDFReader()
+            f.open(filename)
+            for chanindx in range(f.getNSignals()):
+                if f.getSignalFreqs()[chanindx] != f.getSignalFreqs()[0]:
+                    raise AssertionError('unequal SignalFreqs')
+                if f.getNSamples()[chanindx] != f.getNSamples()[0]:
+                    raise AssertionError('unequal NSamples')
+            H.nChannels = len(f.getSignalFreqs())
+            H.fSample = f.getSignalFreqs()[0]
+            H.nSamples = f.getNSamples()[0]
+            H.nEvents = 0
+            H.dataType = FieldTrip.DATATYPE_FLOAT32
+            # the channel labels will be written to the buffer
+            labels = f.getSignalTextLabels()
+            # read all the data from the file
+            A = np.ndarray(shape=(H.nSamples, H.nChannels), dtype=np.float32)
+            for chanindx in range(H.nChannels):
+                monitor.info('reading channel ' + str(chanindx))
+                A[:, chanindx] = f.readSignal(chanindx)
+            f.close()
+
+        elif fileformat == 'wav':
+            try:
+                physical_min = patch.getfloat('playback', 'physical_min')
+            except:
+                physical_min = -1
+            try:
+                physical_max = patch.getfloat('playback', 'physical_max')
+            except:
+                physical_max = 1
+            f = wave.open(filename, 'r')
+            resolution = f.getsampwidth()  # 1, 2 or 4
+            # 8-bit samples are stored as unsigned bytes, ranging from 0 to 255.
+            # 16-bit samples are stored as signed integers in 2's-complement.
+            H.nChannels = f.getnchannels()
+            H.fSample = f.getframerate()
+            H.nSamples = f.getnframes()
+            H.nEvents = 0
+            H.dataType = FieldTrip.DATATYPE_FLOAT32
+            # there are no channel labels
+            labels = None
+            # read all the data from the file
+            x = f.readframes(f.getnframes() * f.getnchannels())
+            f.close()
+            # convert and calibrate
+            if resolution == 2:
+                x = struct.unpack_from('%dh' % f.getnframes() * f.getnchannels(), x)
+                x = np.asarray(x).astype(np.float32).reshape(f.getnframes(), f.getnchannels())
+                y = x / float(MAXINT16)
+            elif resolution == 4:
+                x = struct.unpack_from('%di' % f.getnframes() * f.getnchannels(), x)
+                x = np.asarray(x).astype(np.float32).reshape(f.getnframes(), f.getnchannels())
+                y = x / float(MAXINT32)
+            else:
+                raise NotImplementedError('unsupported resolution')
+            A = y * ((physical_max - physical_min) / 2)
+
+        else:
+            raise NotImplementedError('unsupported file format')
+
+        monitor.debug('nChannels = ' + str(H.nChannels))
+        monitor.debug('nSamples = ' + str(H.nSamples))
+        monitor.debug('fSample = ' + str(H.fSample))
+        monitor.debug('labels = ' + str(labels))
+
+        ft_output.putHeader(H.nChannels, H.fSample, H.dataType, labels=labels)
+
+        blocksize = int(patch.getfloat('playback', 'blocksize') * H.fSample)
+        stepsize = blocksize / (H.fSample * patch.getfloat('playback', 'speed'))
+        begsample = 0
+        endsample = blocksize - 1
+        block = 0
 
-    # copy the selected samples from the in-memory data
-    D = A[begsample:endsample + 1, :]
+    if playback:
+        monitor.info('Playing block ' + str(block) + ' from ' + str(begsample) + ' to ' + str(endsample))
 
-    # write the data to the output buffer
-    ft_output.putData(D)
+        # copy the selected samples from the in-memory data
+        D = A[begsample:endsample + 1, :]
 
-    stepsize = blocksize / (H.fSample * patch.getfloat('playback', 'speed'))
-    begsample += blocksize
-    endsample += blocksize
-    block += 1
+        # write the data to the output buffer
+        ft_output.putData(D)
+
+        begsample += blocksize
+        endsample += blocksize
+        block += 1
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, stepsize
+    global monitor, stepsize, elapsed, naptime
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -261,19 +256,20 @@
         naptime = stepsize - elapsed
         if naptime > 0:
             # this approximates the real time streaming speed
             time.sleep(naptime)
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/plotcontrol/plotcontrol.py` & `eegsynth-0.7.0/module/plotcontrol/plotcontrol.py`

 * *Files 16% similar despite different names*

```diff
@@ -16,26 +16,25 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from pyqtgraph.Qt import QtGui, QtCore
-import configparser
-import redis
-import argparse
 import numpy as np
 import os
 import pyqtgraph as pg
+import signal
 import sys
 import signal
+import traceback
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -50,65 +49,59 @@
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, delay, historysize, window, winx, winy, winwidth, winheight, input_name, input_variable, ylim_name, ylim_value, counter, app, win, inputhistory, inputplot, inputcurve, iplot, name, ylim, variable, linecolor, icurve, timer, timeaxis
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, historysize, window, winx, winy, winwidth, winheight, input_name, input_variable, ylim_name, ylim_value, counter, app, win, inputhistory, inputplot, inputcurve, iplot, name, ylim, variable, linecolor, icurve, timer, timeaxis
 
     # get the options from the configuration file
     delay       = patch.getfloat('general', 'delay')
     window      = patch.getfloat('general', 'window') # in seconds
-    winx        = patch.getfloat('display', 'xpos')
-    winy        = patch.getfloat('display', 'ypos')
-    winwidth    = patch.getfloat('display', 'width')
-    winheight   = patch.getfloat('display', 'height')
+    winx        = patch.getint('display', 'xpos')
+    winy        = patch.getint('display', 'ypos')
+    winwidth    = patch.getint('display', 'width')
+    winheight   = patch.getint('display', 'height')
 
     historysize = int(window/delay) # in steps
     timeaxis = np.linspace(-window, 0, historysize)
 
-    input_name, input_variable = list(zip(*config.items('input')))
-    ylim_name, ylim_value = list(zip(*config.items('ylim')))
+    input_name, input_variable = list(zip(*patch.config.items('input')))
+    ylim_name, ylim_value = list(zip(*patch.config.items('ylim')))
 
     # count the total number of curves to be drawm
     counter = 0
     for iplot, name in enumerate(input_name):
         for control in input_variable[iplot].split(','):
             counter += 1
 
-    # initialize graphical window
+    # start the graphical user interface
     app = QtGui.QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
+    signal.signal(signal.SIGINT, _stop)
+
+    # deal with uncaught exceptions
+    sys.excepthook = _exception_hook
+
     win = pg.GraphicsWindow(title=patch.getstring('display', 'title', default='EEGsynth plotcontrol'))
     win.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth plotcontrol'))
     win.setGeometry(winx, winy, winwidth, winheight)
 
     # Enable antialiasing for prettier plots
     pg.setConfigOptions(antialias=True)
 
@@ -134,32 +127,30 @@
         variable = input_variable[iplot].split(",")
         linecolor = patch.getstring('linecolor', name, multiple=True, default='w,'*len(variable))
         for icurve in range(len(variable)):
             inputcurve.append(inputplot[iplot].plot(pen=linecolor[icurve]))
 
         win.nextRow()
 
-        signal.signal(signal.SIGINT, _stop)
-
-        # Set timer for update
-        timer = QtCore.QTimer()
-        timer.timeout.connect(_loop_once)
-        timer.setInterval(10)            # timeout in milliseconds
-        timer.start(int(delay * 1000))   # in milliseconds
+    # Set timer for update
+    timer = QtCore.QTimer()
+    timer.timeout.connect(_loop_once)
+    timer.setInterval(10)            # timeout in milliseconds
+    timer.start(int(delay * 1000))   # in milliseconds
 
 
 def _loop_once():
     '''Update the main figure once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, delay, historysize, window, winx, winy, winwidth, winheight, input_name, input_variable, ylim_name, ylim_value, counter, app, win, inputhistory, inputplot, inputcurve, iplot, name, ylim, variable, linecolor, icurve, timer, timeaxis
+    global patch, name, path, monitor
+    global delay, historysize, window, winx, winy, winwidth, winheight, input_name, input_variable, ylim_name, ylim_value, counter, app, win, inputhistory, inputplot, inputcurve, iplot, name, ylim, variable, linecolor, icurve, timer, timeaxis
 
     monitor.loop()
-    
+
     if not patch.getint('general', 'enable', default=True):
         # do not read data and do not plot anything
         return
 
     # shift all historic data with one sample
     inputhistory = np.roll(inputhistory, -1, axis=1)
 
@@ -176,19 +167,29 @@
 def _loop_forever():
     '''Run the main loop forever
     '''
     QtGui.QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     QtGui.QApplication.quit()
 
 
+def _exception_hook(type, value, tb):
+    '''Stop and clean up the PyQt application on uncaught exception
+    '''
+    traceback_formated = traceback.format_exception(type, value, tb)
+    traceback_string = "".join(traceback_formated)
+    print(traceback_string, file=sys.stderr)
+    monitor.error('uncaught exception, stopping...')
+    _stop()
+
+
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
```

### Comparing `eegsynth-0.6.0/module/plotimage/plotimage.py` & `eegsynth-0.7.0/module/plotimage/plotimage.py`

 * *Files 7% similar despite different names*

```diff
@@ -17,26 +17,23 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from PyQt5 import QtGui, QtCore, QtWidgets
 from PyQt5.QtWidgets import QApplication, QWidget
-import configparser
-import redis
-import argparse
 import os
 import sys
 import time
 import threading
 import signal
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -62,25 +59,25 @@
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
         global r, patch, lock, monitor
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('PLOTIMAGE_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)  # this message contains the trigger
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
                     window.setImage(self.image)
                     window.paintEvent(None)
-                        
+
 
 class Window(QWidget):
     def __init__(self):
         super(Window, self).__init__()
         self.setGeometry(winx, winy, winwidth, winheight)
         # self.setFixedSize(winwidth, winheight)
         self.setStyleSheet('background-color:black;');
@@ -93,116 +90,106 @@
         g = QtWidgets.QGridLayout()
         g.setContentsMargins(0,0,0,0)
         g.addWidget(self.label,0,1)
         self.setLayout(g)
 
     def setImage(self, image):
         self.image = image
-        
+
     def paintEvent(self, e):
         if not self.image == None:
             self.label.setPixmap(self.image)
         self.show()
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, delay, winx, winy, winwidth, winheight, input_channel, input_image, app, window, triggers, timer
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, winx, winy, winwidth, winheight, input_channel, input_image, app, timer, window, triggers, channel, image, thread
 
     # get the options from the configuration file
     delay           = patch.getfloat('general', 'delay')
-    winx            = patch.getfloat('display', 'xpos')
-    winy            = patch.getfloat('display', 'ypos')
-    winwidth        = patch.getfloat('display', 'width')
-    winheight       = patch.getfloat('display', 'height')
+    winx            = patch.getint('display', 'xpos')
+    winy            = patch.getint('display', 'ypos')
+    winwidth        = patch.getint('display', 'width')
+    winheight       = patch.getint('display', 'height')
 
     # get the input options
-    input_channel, input_image = list(zip(*config.items('input')))
+    input_channel, input_image = list(zip(*patch.config.items('input')))
 
     # start the graphical user interface
     app = QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
     app.aboutToQuit.connect(_stop)
     signal.signal(signal.SIGINT, _stop)
 
-    # Let the interpreter run every 400 ms
-    # see https://stackoverflow.com/questions/4938723/what-is-the-correct-way-to-make-my-pyqt-application-quit-when-killed-from-the-co/6072360#6072360
-    timer = QtCore.QTimer()
-    timer.start(400)
-    timer.timeout.connect(lambda: None)
-
     window = Window()
     window.show()
 
+    # Let the interpreter run every 200 ms
+    # see https://stackoverflow.com/questions/4938723/what-is-the-correct-way-to-make-my-pyqt-application-quit-when-killed-from-the-co/6072360#6072360
+    timer = QtCore.QTimer()
+    timer.start(200)
+    timer.timeout.connect(_loop_once)
+
     triggers = []
     # make a trigger thread for each image
     for channel, image in zip(input_channel, input_image):
         triggers.append(TriggerThread(channel, image))
-        
+
     # start the thread for each of the triggers
     for thread in triggers:
         thread.start()
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     '''
-    pass
+    # Updating the main figure is done through Qt events
+    global monitor
+    monitor.loop()
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, r, triggers
+    global monitor, triggers
     monitor.success('Closing threads')
     for thread in triggers:
         thread.stop()
-    r.publish('PLOTIMAGE_UNBLOCK', 1)
+    patch.publish('PLOTIMAGE_UNBLOCK', 1)
     for thread in triggers:
         thread.join()
     QApplication.quit()
 
 
 if __name__ == '__main__':
     _setup()
```

### Comparing `eegsynth-0.6.0/module/plotsignal/plotsignal.py` & `eegsynth-0.7.0/module/plotsignal/plotsignal.py`

 * *Files 7% similar despite different names*

```diff
@@ -16,28 +16,26 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from pyqtgraph.Qt import QtGui, QtCore
-import configparser
-import redis
-import argparse
 import numpy as np
 import os
 import pyqtgraph as pg
+import signal
 import sys
 import time
-import signal
+import traceback
 from scipy.signal import detrend
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -54,62 +52,46 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, channels, winx, winy, winwidth, winheight, window, clipsize, clipside, stepsize, lrate, ylim, hdr_input, start, filterorder, filter, notchquality, notch, app, win, timeplot, curve, curvemax, plotnr, channr, timer, begsample, endsample
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to input FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to input FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global channels, winx, winy, winwidth, winheight, window, clipsize, clipside, stepsize, lrate, ylim, timeout, hdr_input, start, filterorder, filter, notchquality, notch, app, win, timeplot, curve, curvemax, plotnr, channr, timer, begsample, endsample
-
-    # read variables from ini/redis
+    # get the options from the configuration file
     channels    = patch.getint('arguments', 'channels', multiple=True)
-    winx        = patch.getfloat('display', 'xpos')
-    winy        = patch.getfloat('display', 'ypos')
-    winwidth    = patch.getfloat('display', 'width')
-    winheight   = patch.getfloat('display', 'height')
+    winx        = patch.getint('display', 'xpos')
+    winy        = patch.getint('display', 'ypos')
+    winwidth    = patch.getint('display', 'width')
+    winheight   = patch.getint('display', 'height')
     window      = patch.getfloat('arguments', 'window', default=5.0)        # in seconds
     clipsize    = patch.getfloat('arguments', 'clipsize', default=0.0)      # in seconds
     clipside    = patch.getstring('arguments', 'clipside', default='left')  # left is in the past, right is in the future
     stepsize    = patch.getfloat('arguments', 'stepsize', default=0.1)      # in seconds
     lrate       = patch.getfloat('arguments', 'learning_rate', default=0.2)
     ylim        = patch.getfloat('arguments', 'ylim', multiple=True, default=None)
 
@@ -153,16 +135,23 @@
     while begsample < 0:
         time.sleep(0.1)
         hdr_input = ft_input.getHeader()
         if hdr_input != None:
             begsample = hdr_input.nSamples - window
             endsample = hdr_input.nSamples - 1
 
-    # initialize graphical window
+    # start the graphical user interface
     app = QtGui.QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
+    signal.signal(signal.SIGINT, _stop)
+
+    # deal with uncaught exceptions
+    sys.excepthook = _exception_hook
+
     win = pg.GraphicsWindow(title=patch.getstring('display', 'title', default='EEGsynth plotsignal'))
     win.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth plotsignal'))
     win.setGeometry(winx, winy, winwidth, winheight)
 
     # Enable antialiasing for prettier plots
     pg.setConfigOptions(antialias=True)
 
@@ -176,33 +165,31 @@
 
         timeplot.append(win.addPlot(title="%s%s" % ('Channel ', channr)))
         timeplot[plotnr].setLabel('left', text='Amplitude')
         timeplot[plotnr].setLabel('bottom', text='Time (s)')
         curve.append(timeplot[plotnr].plot(pen='w'))
         win.nextRow()
 
-    signal.signal(signal.SIGINT, _stop)
-
     # Set timer for update
     timer = QtCore.QTimer()
     timer.timeout.connect(_loop_once)
     timer.setInterval(10)                       # timeout in milliseconds
     timer.start(int(round(stepsize * 1000)))    # stepsize in milliseconds
 
 
 def _loop_once():
     '''Update the main figure once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global channels, winx, winy, winwidth, winheight, window, clipsize, clipside, stepsize, lrate, ylim, timeout, hdr_input, start, filterorder, filter, notchquality, notch, app, win, timeplot, curve, curvemax, plotnr, channr, timer, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, channels, winx, winy, winwidth, winheight, window, clipsize, clipside, stepsize, lrate, ylim, hdr_input, start, filterorder, filter, notchquality, notch, app, win, timeplot, curve, curvemax, plotnr, channr, timer, begsample, endsample
     global dat, timeaxis
 
     monitor.loop()
-    
+
     if not patch.getint('general', 'enable', default=True):
         # do not read data and do not plot anything
         return
 
     hdr_input = ft_input.getHeader()
     if (hdr_input.nSamples-1)<endsample:
         monitor.info("buffer reset detected")
@@ -282,19 +269,29 @@
 def _loop_forever():
     '''Run the main loop forever
     '''
     QtGui.QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     QtGui.QApplication.quit()
 
 
+def _exception_hook(type, value, tb):
+    '''Stop and clean up the PyQt application on uncaught exception
+    '''
+    traceback_formated = traceback.format_exception(type, value, tb)
+    traceback_string = "".join(traceback_formated)
+    print(traceback_string, file=sys.stderr)
+    monitor.error('uncaught exception, stopping...')
+    _stop()
+
+
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
```

### Comparing `eegsynth-0.6.0/module/plotspectral/plotspectral.py` & `eegsynth-0.7.0/module/plotspectral/plotspectral.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,28 +17,26 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from pyqtgraph.Qt import QtGui, QtCore
-import configparser
-import redis
-import argparse
 import numpy as np
 import os
 import pyqtgraph as pg
+import signal
 import sys
 import time
-import signal
+import traceback
 from scipy.signal import detrend
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -55,53 +53,40 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor, ft_host, ft_port, ft_input
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channels, window, output, clipsize, clipside, stepsize, historysize, lrate, ylim, scale_red, scale_blue, offset_red, offset_blue, winx, winy, winwidth, winheight, prefix, numhistory, freqaxis, history, showred, showblue, filterorder, filter, notchquality, notch, freqrange, app, win, text_redleft_curr, text_redright_curr, text_blueleft_curr, text_blueright_curr, text_redleft_hist, text_redright_hist, text_blueleft_hist, text_blueright_hist, freqplot_curr, freqplot_hist, spect_curr, spect_hist, redleft_curr, redright_curr, blueleft_curr, blueright_curr, redleft_hist, redright_hist, blueleft_hist, blueright_hist, fft_curr, fft_hist, specmax_curr, specmin_curr, specmax_hist, specmin_hist, plotnr, channr, timer, begsample, endsample, taper
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.info('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.info("Connected to input FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to input FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, channels, window, output, clipsize, clipside, stepsize, historysize, lrate, ylim, scale_red, scale_blue, offset_red, offset_blue, winx, winy, winwidth, winheight, prefix, numhistory, freqaxis, history, showred, showblue, filterorder, filter, notchquality, notch, freqrange, app, win, text_redleft_curr, text_redright_curr, text_blueleft_curr, text_blueright_curr, text_redleft_hist, text_redright_hist, text_blueleft_hist, text_blueright_hist, freqplot_curr, freqplot_hist, spect_curr, spect_hist, redleft_curr, redright_curr, blueleft_curr, blueright_curr, redleft_hist, redright_hist, blueleft_hist, blueright_hist, fft_curr, fft_hist, specmax_curr, specmin_curr, specmax_hist, specmin_hist, plotnr, channr, timer, begsample, endsample, taper
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info("Waiting for data to arrive...")
@@ -122,21 +107,21 @@
     stepsize    = patch.getfloat('arguments', 'stepsize', default=0.1)      # in seconds
     historysize = patch.getfloat('arguments', 'historysize', default=10)    # in seconds
     lrate       = patch.getfloat('arguments', 'learning_rate', default=0.2)
     scale_red   = patch.getfloat('scale', 'red')
     scale_blue  = patch.getfloat('scale', 'blue')
     offset_red  = patch.getfloat('offset', 'red')
     offset_blue = patch.getfloat('offset', 'blue')
-    winx        = patch.getfloat('display', 'xpos')
-    winy        = patch.getfloat('display', 'ypos')
-    winwidth    = patch.getfloat('display', 'width')
-    winheight   = patch.getfloat('display', 'height')
+    winx        = patch.getint('display', 'xpos')
+    winy        = patch.getint('display', 'ypos')
+    winwidth    = patch.getint('display', 'width')
+    winheight   = patch.getint('display', 'height')
     prefix      = patch.getstring('output', 'prefix')
     ylim        = patch.getfloat('arguments', 'ylim', multiple=True, default=None)
-    output      = patch.getstring('arguments', 'output', default='amplitude')  # amplitude or power
+    output      = patch.getstring('arguments', 'output', default='amplitude')  # amplitude, power or db
 
     window      = int(round(window * hdr_input.fSample))       # in samples
     clipsize    = int(round(clipsize * hdr_input.fSample))     # in samples
     if clipside == 'left' or clipside == 'right':
         freqaxis = np.fft.fftfreq((window-clipsize), 1. / hdr_input.fSample)
     elif clipside == 'both':
         freqaxis = np.fft.fftfreq((window-2*clipsize), 1. / hdr_input.fSample)
@@ -174,16 +159,23 @@
     while begsample < 0:
         time.sleep(0.1)
         hdr_input = ft_input.getHeader()
         if hdr_input != None:
             begsample = hdr_input.nSamples - window
             endsample = hdr_input.nSamples - 1
 
-    # initialize graphical window
+    # start the graphical user interface
     app = QtGui.QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
+    signal.signal(signal.SIGINT, _stop)
+
+    # deal with uncaught exceptions
+    sys.excepthook = _exception_hook
+
     win = pg.GraphicsWindow(title=patch.getstring('display', 'title', default='EEGsynth plotspectral'))
     win.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth plotspectral'))
     win.setGeometry(winx, winy, winwidth, winheight)
 
     # initialize graphical elements
     text_redleft_curr   = pg.TextItem("", anchor=( 1,  0), color='r')
     text_redright_curr  = pg.TextItem("", anchor=( 0,  0), color='r')
@@ -226,29 +218,37 @@
         plot.setYRange(0,1)
 
         freqplot_curr.append(plot)
         if output=='amplitude':
             freqplot_curr[plotnr].setLabel('left', text='Amplitude')
         elif output=='power':
             freqplot_curr[plotnr].setLabel('left', text='Power')
+        elif output=='db':
+            freqplot_curr[plotnr].setLabel('left', text='dB')
         freqplot_curr[plotnr].setLabel('bottom', text='Frequency (Hz)')
 
         spect_curr.append(freqplot_curr[plotnr].plot(pen='w'))
         redleft_curr.append(freqplot_curr[plotnr].plot(pen='r'))
         redright_curr.append(freqplot_curr[plotnr].plot(pen='r'))
         blueleft_curr.append(freqplot_curr[plotnr].plot(pen='b'))
         blueright_curr.append(freqplot_curr[plotnr].plot(pen='b'))
 
         plot = win.addPlot(title="%s%s%s%s%s" % ('Averaged spectrum channel ', channr, ' (', historysize, 's)'))
         # speeds up the initial axis scaling set the range to something different than [0, 0]
         plot.setXRange(0,1)
         plot.setYRange(0,1)
 
         freqplot_hist.append(plot)
-        freqplot_hist[plotnr].setLabel('left', text='Power')
+
+        if output=='amplitude':
+            freqplot_hist[plotnr].setLabel('left', text='Amplitude')
+        elif output=='power':
+            freqplot_hist[plotnr].setLabel('left', text='Power')
+        elif output=='db':
+            freqplot_hist[plotnr].setLabel('left', text='dB')
         freqplot_hist[plotnr].setLabel('bottom', text='Frequency (Hz)')
 
         spect_hist.append(freqplot_hist[plotnr].plot(pen='w'))
         redleft_hist.append(freqplot_hist[plotnr].plot(pen='r'))
         redright_hist.append(freqplot_hist[plotnr].plot(pen='r'))
         blueleft_hist.append(freqplot_hist[plotnr].plot(pen='b'))
         blueright_hist.append(freqplot_hist[plotnr].plot(pen='b'))
@@ -268,29 +268,27 @@
     freqplot_curr[0].addItem(text_blueleft_curr)
     freqplot_curr[0].addItem(text_blueright_curr)
     freqplot_hist[0].addItem(text_redleft_hist)
     freqplot_hist[0].addItem(text_redright_hist)
     freqplot_hist[0].addItem(text_blueleft_hist)
     freqplot_hist[0].addItem(text_blueright_hist)
 
-    signal.signal(signal.SIGINT, _stop)
-
     # Set timer for update
     timer = QtCore.QTimer()
     timer.timeout.connect(_loop_once)
     timer.setInterval(10)                     # timeout in milliseconds
     timer.start(int(round(stepsize * 1000)))  # in milliseconds
 
 
 def _loop_once():
     '''Update the main figure once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, channels, window, output, clipsize, clipside, stepsize, historysize, lrate, ylim, scale_red, scale_blue, offset_red, offset_blue, winx, winy, winwidth, winheight, prefix, numhistory, freqaxis, history, showred, showblue, filterorder, filter, notchquality, notch, app, win, text_redleft_curr, text_redright_curr, text_blueleft_curr, text_blueright_curr, text_redleft_hist, text_redright_hist, text_blueleft_hist, text_blueright_hist, freqplot_curr, freqplot_hist, spect_curr, spect_hist, redleft_curr, redright_curr, blueleft_curr, blueright_curr, redleft_hist, redright_hist, blueleft_hist, blueright_hist, fft_curr, fft_hist, specmax_curr, specmin_curr, specmax_hist, specmin_hist, plotnr, channr, timer, begsample, endsample, taper
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channels, window, output, clipsize, clipside, stepsize, historysize, lrate, ylim, scale_red, scale_blue, offset_red, offset_blue, winx, winy, winwidth, winheight, prefix, numhistory, freqaxis, history, showred, showblue, filterorder, filter, notchquality, notch, app, win, text_redleft_curr, text_redright_curr, text_blueleft_curr, text_blueright_curr, text_redleft_hist, text_redright_hist, text_blueleft_hist, text_blueright_hist, freqplot_curr, freqplot_hist, spect_curr, spect_hist, redleft_curr, redright_curr, blueleft_curr, blueright_curr, redleft_hist, redright_hist, blueleft_hist, blueright_hist, fft_curr, fft_hist, specmax_curr, specmin_curr, specmax_hist, specmin_hist, plotnr, channr, timer, begsample, endsample, taper
     global dat, arguments_freqrange, freqrange, redfreq, redwidth, bluefreq, bluewidth
 
     monitor.loop()
 
     if not patch.getint('general', 'enable', default=True):
         # do not read data and do not plot anything
         return
@@ -332,15 +330,15 @@
     # apply the notch filtering
     if not np.isnan(notch) and notch<(hdr_input.fSample/2):
         dat = EEGsynth.notch_filter(dat.T, notch, hdr_input.fSample, notchquality).T # remove the line noise
     if not np.isnan(notch) and 2*notch<(hdr_input.fSample/2):
         dat = EEGsynth.notch_filter(dat.T, 2*notch, hdr_input.fSample, notchquality).T # remove the first harmonic
     if not np.isnan(notch) and 3*notch<(hdr_input.fSample/2):
         dat = EEGsynth.notch_filter(dat.T, 3*notch, hdr_input.fSample, notchquality).T # remove the second harmonic
-        
+
     # remove the filter padding
     if clipsize > 0:
         if clipside == 'left':
             dat = dat[clipsize:,:]
         elif clipside == 'right':
             dat = dat[:-clipsize,:]
         elif clipside == 'both':
@@ -355,14 +353,16 @@
     for plotnr, channr in enumerate(channels):
 
         # estimate the absolute FFT at the current moment
         if output == 'amplitude':
             fft_curr[plotnr] = abs(np.fft.fft(dat[:, channr-1]))
         elif output == 'power':
             fft_curr[plotnr] = abs(np.fft.fft(dat[:, channr-1]))**2
+        elif output == 'db':
+            fft_curr[plotnr] = 10*np.log10(abs(np.fft.fft(dat[:, channr-1])))
 
         # update the FFT history with the current estimate
         history[plotnr, :, numhistory - 1] = fft_curr[plotnr]
         fft_hist = np.mean(history, axis=2)
 
         # user-selected frequency band
         arguments_freqrange = patch.getfloat('arguments', 'freqrange', multiple=True)
@@ -454,19 +454,29 @@
 def _loop_forever():
     '''Run the main loop forever
     '''
     QtGui.QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     QtGui.QApplication.quit()
 
 
+def _exception_hook(type, value, tb):
+    '''Stop and clean up the PyQt application on uncaught exception
+    '''
+    traceback_formated = traceback.format_exception(type, value, tb)
+    traceback_string = "".join(traceback_formated)
+    print(traceback_string, file=sys.stderr)
+    monitor.error('uncaught exception, stopping...')
+    _stop()
+
+
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
```

### Comparing `eegsynth-0.6.0/module/plottrigger/plottrigger.py` & `eegsynth-0.7.0/module/plottrigger/plottrigger.py`

 * *Files 9% similar despite different names*

```diff
@@ -16,28 +16,26 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from pyqtgraph.Qt import QtGui, QtCore
-import configparser
-import redis
-import argparse
 import numpy as np
 import os
 import pyqtgraph as pg
+import signal
 import sys
 import time
 import threading
-import signal
+import traceback
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -58,128 +56,123 @@
         threading.Thread.__init__(self)
         self.redischannel = redischannel
         self.number = number
         self.running = True
     def stop(self):
         self.running = False
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('PLOTTRIGGER_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)      # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel']==self.redischannel:
-                    monitor.info(item)
+                    monitor.debug(item)
                     now = time.time()
                     val = float(item['data'])
                     with lock:
                         # append the time and value as a tuple
                         data[self.number].append((now, val))
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, delay, window, value, winx, winy, winwidth, winheight, data, lock, trigger, number, i, this, thread, app, win, plot
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+    global patch, name, path, monitor
+    global delay, window, value, winx, winy, winwidth, winheight, data, lock, trigger, number, i, this, thread, app, win, timer, plot
 
     # get the options from the configuration file
-    debug       = patch.getint('general', 'debug')
     delay       = patch.getfloat('general', 'delay')            # in seconds
     window      = patch.getfloat('general', 'window')           # in seconds
     value       = patch.getint('general', 'value', default=0)   # boolean
-    winx        = patch.getfloat('display', 'xpos')
-    winy        = patch.getfloat('display', 'ypos')
-    winwidth    = patch.getfloat('display', 'width')
-    winheight   = patch.getfloat('display', 'height')
+    winx        = patch.getint('display', 'xpos')
+    winy        = patch.getint('display', 'ypos')
+    winwidth    = patch.getint('display', 'width')
+    winheight   = patch.getint('display', 'height')
 
     # Initialize variables
     data = {}
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     trigger = []
     number = []
-    # each of the gates that can be triggered is mapped onto a different message
+    # each of the gates is mapped onto a different message
     for i in range(1, 17):
         name = 'channel{}'.format(i)
-        if config.has_option('gate', name):
+        if patch.config.has_option('gate', name):
             number.append(i)
             data[i] = []
             # start the background thread that deals with this channel
-            this = TriggerThread(patch.getstring('gate', name), i)
+            this = TriggerThread(patch.get('gate', name), i)
             trigger.append(this)
             monitor.info(name + ' trigger configured')
     if len(trigger)==0:
         monitor.warning('no gates were specified in the ini file')
 
     # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
-    # initialize graphical window
+    # start the graphical user interface
     app = QtGui.QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
+    signal.signal(signal.SIGINT, _stop)
+
+    # deal with uncaught exceptions
+    sys.excepthook = _exception_hook
+
     win = pg.GraphicsWindow(title=patch.getstring('display', 'title', default='EEGsynth plottrigger'))
     win.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth plottrigger'))
     win.setGeometry(winx, winy, winwidth, winheight)
 
     # Enable antialiasing for prettier plots
     pg.setConfigOptions(antialias=True)
 
     plot = win.addPlot()
     plot.setLabel('left', text='Channel')
     plot.setLabel('bottom', text='Time (s)')
     plot.setXRange(-window, 0)
     plot.setYRange(0.5, len(trigger)+0.5)
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    # Set timer for update
+    timer = QtCore.QTimer()
+    timer.timeout.connect(_loop_once)
+    timer.setInterval(10)                     # timeout in milliseconds
+    timer.start(int(round(delay * 1000)))     # in milliseconds
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, delay, window, value, winx, winy, winwidth, winheight, data, lock, trigger, number, i, this, thread, app, win, plot
+    global patch, name, path, monitor
+    global delay, window, value, winx, winy, winwidth, winheight, data, lock, trigger, number, i, this, thread, app, win, timer, plot
 
     monitor.loop()
 
     now = time.time()
     plot.clear()
     for y in number:
         for event in data[y]:
@@ -205,46 +198,44 @@
                     # print it as floating point value
                     s = '%2.1f' % v
 
                 text = pg.TextItem(s, anchor=(0,0))
                 text.setPos(x, y)
                 plot.addItem(text)
 
-    signal.signal(signal.SIGINT, _stop)
-
-    # Set timer for update
-    timer = QtCore.QTimer()
-    timer.timeout.connect(_loop_once)
-    timer.setInterval(10)                     # timeout in milliseconds
-    timer.start(int(round(delay * 1000)))     # in milliseconds
-
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     QtGui.QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, trigger, r
+    global monitor, trigger
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('PLOTTRIGGER_UNBLOCK', 1)
+    patch.publish('PLOTTRIGGER_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
     QtGui.QApplication.quit()
 
 
+def _exception_hook(type, value, tb):
+    '''Stop and clean up the PyQt application on uncaught exception
+    '''
+    traceback_formated = traceback.format_exception(type, value, tb)
+    traceback_string = "".join(traceback_formated)
+    print(traceback_string, file=sys.stderr)
+    monitor.error('uncaught exception, stopping...')
+    _stop()
+
+
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
```

### Comparing `eegsynth-0.6.0/module/postprocessing/__init__.py` & `eegsynth-0.7.0/module/videoprocessing/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .postprocessing import _setup, _start, _loop_once, _loop_forever, _stop
+from .videoprocessing import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/postprocessing/postprocessing.py` & `eegsynth-0.7.0/module/postprocessing/postprocessing.py`

 * *Files 7% similar despite different names*

```diff
@@ -16,25 +16,22 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from numpy import log, log2, log10, exp, power, sqrt, mean, median, var, std, mod, random
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -78,61 +75,48 @@
     return equation
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, input_name, input_variable, output_name, output_equation, variable, equation
+    global patch, name, path, monitor
+    global input_name, input_variable, output_name, output_equation, variable, equation
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    if 'initial' in config.sections():
+    if 'initial' in patch.config.sections():
         # assign the initial values
-        for item in config.items('initial'):
-            val = patch.getfloat('initial', item[0])
+        for item in patch.config.items('initial'):
+            val = patch.getfloat('initial', item[0], default=np.nan)
             patch.setvalue(item[0], val)
             monitor.update(item[0], val)
 
     # get the input and output options
-    if len(config.items('input')):
-        input_name, input_variable = list(zip(*config.items('input')))
+    if len(patch.config.items('input')):
+        input_name, input_variable = list(zip(*patch.config.items('input')))
     else:
         input_name, input_variable = ([], [])
-    if len(config.items('output')):
-        output_name, output_equation = list(zip(*config.items('output')))
+    if len(patch.config.items('output')):
+        output_name, output_equation = list(zip(*patch.config.items('output')))
     else:
         output_name, output_equation = ([], [])
 
     # make the equations robust against sub-string replacements
     output_equation = [sanitize(equation) for equation in output_equation]
 
     monitor.info('===== input variables =====')
@@ -148,34 +132,36 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, input_name, input_variable, output_name, output_equation, variable, equation
+    global patch, name, path, monitor
+    global input_name, input_variable, output_name, output_equation, variable, equation
 
     monitor.debug('============================')
 
     input_value = []
     for name in input_name:
-        val = patch.getfloat('input', name)
+        val = patch.getfloat('input', name, default=np.nan)
         input_value.append(val)
 
     for key, equation in zip(output_name, output_equation):
         # replace the variable names in the equation by the values
         for name, value in zip(input_name, input_value):
             if value is None and equation.count(name)>0:
                 monitor.error('Undefined value: %s' % (name))
             else:
                 equation = equation.replace(name, str(value))
 
         # try to evaluate the equation
         try:
+            equation = equation.replace('nan', 'np.nan')
+            equation = equation.replace('inf', 'np.inf')
             val = eval(equation)
             val = float(val) # deal with True/False
             monitor.debug('%s = %s = %g' % (key, equation, val))
             patch.setvalue(key, val)
         except ZeroDivisionError:
             # division by zero is not a serious error
             patch.setvalue(equation[0], np.NaN)
@@ -190,19 +176,20 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/preprocessing/__init__.py` & `eegsynth-0.7.0/module/generateclock/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .preprocessing import _setup, _start, _loop_once, _loop_forever, _stop
+from .generateclock import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/preprocessing/preprocessing.py` & `eegsynth-0.7.0/module/preprocessing/preprocessing.py`

 * *Files 4% similar despite different names*

```diff
@@ -16,27 +16,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import redis
-import argparse
 import os
 import sys
 import time
 import numpy as np
 from copy import copy
 from numpy.matlib import repmat
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -48,38 +45,35 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path,'../../lib'))
 import EEGsynth
 import FieldTrip
 
+
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, window, downsample, differentiate, integrate, rectify, smoothing, reference, default_scale, scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filterorder, scale_notchquality, offset_filterorder, offset_notchquality, previous, differentiate_zi, integrate_zi, begsample, endsample
+    global montage_in, montage_out
 
     try:
         ft_host = patch.getstring('input_fieldtrip','hostname')
         ft_port = patch.getint('input_fieldtrip','port')
         monitor.info('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
@@ -93,23 +87,14 @@
         monitor.info('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.info("Connected to output FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output, name
-    global timeout, hdr_input, start, window, downsample, differentiate, integrate, rectify, smoothing, reference, default_scale, scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filterorder, scale_notchquality, offset_filterorder, offset_notchquality, previous, differentiate_zi, integrate_zi, begsample, endsample
-    global montage_in, montage_out
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('input_fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info("Waiting for data to arrive...")
@@ -131,28 +116,28 @@
     integrate       = patch.getint('processing', 'integrate', default=0)
     rectify         = patch.getint('processing', 'rectify', default=0)
     downsample      = patch.getint('processing', 'downsample', default=None)
     smoothing       = patch.getfloat('processing', 'smoothing', default=None)
     reference       = patch.getstring('processing', 'reference')
 
     if reference == 'montage':
-        montage_out, montage_in = list(map(list, list(zip(*config.items('montage')))))
+        montage_out, montage_in = list(map(list, list(zip(*patch.config.items('montage')))))
         nChannels_out = len(montage_out)
         # construct the montage matrix once to give feedback, it will later be recomputed on the fly
         for i, name in enumerate(montage_out):
             montage_in[i] = patch.getfloat('montage', name, multiple=True)
         montage = np.transpose(np.array(montage_in), (1, 0))
         monitor.info("montage =", montage.shape)
     else:
         nChannels_out = hdr_input.nChannels
 
     try:
-        float(config.get('processing', 'highpassfilter'))
-        float(config.get('processing', 'lowpassfilter'))
-        float(config.get('processing', 'notchfilter'))
+        float(patch.config.get('processing', 'highpassfilter'))
+        float(patch.config.get('processing', 'lowpassfilter'))
+        float(patch.config.get('processing', 'notchfilter'))
         # the filter frequencies are specified as numbers, assume they are in Hz
         default_scale = 1.
     except:
         # the filter frequencies are specified as Redis channels, scale them to the Nyquist frequency
         default_scale = hdr_input.fSample/2
 
     monitor.info('default scale for filter settings is %.0f' % (default_scale))
@@ -190,16 +175,16 @@
         endsample = hdr_input.nSamples-1
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
-    global timeout, hdr_input, start, window, downsample, differentiate, integrate, rectify, smoothing, reference, default_scale, scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filterorder, scale_notchquality, offset_filterorder, offset_notchquality, previous, differentiate_zi, integrate_zi, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, window, downsample, differentiate, integrate, rectify, smoothing, reference, default_scale, scale_lowpass, scale_highpass, scale_notchfilter, offset_lowpass, offset_highpass, offset_notchfilter, scale_filterorder, scale_notchquality, offset_filterorder, offset_notchquality, previous, differentiate_zi, integrate_zi, begsample, endsample
     global dat_input, dat_output, highpassfilter, lowpassfilter, filterorder, change, b, a, zi, notchfilter, notchquality, nb, na, nzi, window_new, t
     global montage_in, montage_out
 
     monitor.loop()
 
     # determine when we start polling for available data
     start = time.time()
@@ -325,25 +310,24 @@
     '''Run the main loop forever
     '''
     while True:
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input, ft_output
-
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
     ft_output.disconnect()
     monitor.success('Disconnected from output FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/processtrigger/__init__.py` & `eegsynth-0.7.0/module/processtrigger/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/processtrigger/processtrigger.py` & `eegsynth-0.7.0/module/processtrigger/processtrigger.py`

 * *Files 7% similar despite different names*

```diff
@@ -17,26 +17,23 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from numpy import log, log2, log10, exp, power, sqrt, mean, median, var, std, mod
 from numpy import random
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 import threading
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -87,15 +84,15 @@
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
         global r, monitor, patch
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('PROCESSTRIGGER_UNBLOCK')  # this message unblocks the Redis listen command
         pubsub.subscribe(self.redischannel)        # this message triggers the event
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -146,87 +143,74 @@
                         patch.setvalue(key, val)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, prefix, item, val, input_name, input_variable, output_name, output_equation, variable, equation, lock, trigger, thread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global prefix, item, val, input_name, input_variable, output_name, output_equation, variable, equation, lock, trigger, thread
 
     # get the options from the configuration file
     prefix = patch.getstring('output', 'prefix')
 
-    if 'initial' in config.sections():
+    if 'initial' in patch.config.sections():
         # assign the initial values
-        for item in config.items('initial'):
+        for item in patch.config.items('initial'):
             val = patch.getfloat('initial', item[0])
             patch.setvalue(item[0], val)
             monitor.update(item[0], val)
 
     # get the input variables
-    if len(config.items('input')):
-        input_name, input_variable = list(zip(*config.items('input')))
+    if len(patch.config.items('input')):
+        input_name, input_variable = list(zip(*patch.config.items('input')))
     else:
         input_name, input_variable = ([], [])
 
     # get the output equations for each trigger
     output_name = {}
     output_equation = {}
-    for item in config.items('trigger'):
-        output_name[item[0]], output_equation[item[0]] = list(zip(*config.items(item[0])))
+    for item in patch.config.items('trigger'):
+        output_name[item[0]], output_equation[item[0]] = list(zip(*patch.config.items(item[0])))
         # make the equations robust against sub-string replacements
         output_equation[item[0]] = [sanitize(equation) for equation in output_equation[item[0]]]
 
     monitor.info('===== input variables =====')
     for name, variable in zip(input_name, input_variable):
         monitor.info(name + ' = ' + variable)
-    for item in config.items('trigger'):
+    for item in patch.config.items('trigger'):
         monitor.info('===== output equations for %s =====' % item[0])
         for name, equation in zip(output_name[item[0]], output_equation[item[0]]):
             monitor.info(name + ' = ' + equation)
     monitor.info('============================')
 
     # this is to prevent two triggers from being processed at the same time
     lock = threading.Lock()
 
     # create the background threads that deal with the triggers
     trigger = []
     monitor.debug("Setting up threads for each trigger")
-    for item in config.items('trigger'):
+    for item in patch.config.items('trigger'):
         trigger.append(TriggerThread(item[1], item[0]))
         monitor.debug(item[0] + " " + item[1] + " OK")
 
     # start the thread for each of the triggers
     for thread in trigger:
         thread.start()
 
@@ -246,26 +230,26 @@
     '''
     while True:
         monitor.loop()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('PROCESSTRIGGER_UNBLOCK', 1)
+    patch.publish('PROCESSTRIGGER_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
-        _stop()
+        _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/quantizer/__init__.py` & `eegsynth-0.7.0/module/quantizer/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/quantizer/quantizer.py` & `eegsynth-0.7.0/module/rms/rms.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# Quantizer does chromatic quantification of Redis values for musical interfaces
+# This module calculates a sliding-window RMS value of a signal
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2017-2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,155 +15,149 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
+import math
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
-elif __name__ == '__main__' and sys.argv[0] != '':
+elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
-elif __name__ == '__main__':
+elif __name__=='__main__':
     path = os.path.abspath('')
     file = os.path.split(path)[-1] + '.py'
     name = os.path.splitext(file)[0]
 else:
     path = os.path.split(__file__)[0]
     file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
-
-
-def find_nearest_idx(array, value):
-    # find the index of the array element that is the nearest to the value
-    idx = (np.abs(np.asarray(array) - value)).argmin()
-    return idx
+import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, input_scale, input_offset, output_scale, output_offset, input_channel, input_name, output_name, output_value, index, input_value
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, window, begsample, endsample
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    try:
+        ft_host = patch.getstring('fieldtrip', 'hostname')
+        ft_port = patch.getint('fieldtrip', 'port')
+        monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
+        ft_input = FieldTrip.Client()
+        ft_input.connect(ft_host, ft_port)
+        monitor.success('Connected to FieldTrip buffer')
+    except:
+        raise RuntimeError("cannot connect to FieldTrip buffer")
+
+    # this is the timeout for the FieldTrip buffer
+    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
+
+    hdr_input = None
+    start = time.time()
+    while hdr_input is None:
+        monitor.info('Waiting for data to arrive...')
+        if (time.time() - start) > timeout:
+            raise RuntimeError("timeout while waiting for data")
+        time.sleep(0.1)
+        hdr_input = ft_input.getHeader()
+
+    monitor.info('Data arrived')
+    monitor.debug(hdr_input)
+    monitor.debug(hdr_input.labels)
+
+    channel_items = patch.config.items('input')
+    channame = []
+    chanindx = []
+    for item in channel_items:
+        # channel numbers are one-offset in the ini file, zero-offset in the code
+        channame.append(item[0])                             # the channel name
+        chanindx.append(patch.getint('input', item[0]) - 1)  # the channel number
+
+    prefix = patch.getstring('output', 'prefix')
+    window = patch.getfloat('processing', 'window')     # in seconds
+    window = int(window * hdr_input.fSample)            # in samples
 
-    # the input scale and offset are used to map Redis values to internal values
-    input_scale = patch.getfloat('input', 'scale', default=127)
-    input_offset = patch.getfloat('input', 'offset', default=0)
-    # the output scale and offset are used to map internal values to Redis values
-    output_scale = patch.getfloat('output', 'scale', default=1. / 127)
-    output_offset = patch.getfloat('output', 'offset', default=0)
-
-    # get the input and output options
-    input_channel, input_name = list(map(list, list(zip(*config.items('input')))))
-    output_name, output_value = list(map(list, list(zip(*config.items('quantization')))))
-
-    # remove the scale and offset from the input list
-    del input_channel[input_channel.index('scale')]
-    del input_channel[input_channel.index('offset')]
-
-    # get the list of values for each of the input values for quantization
-    for i, name in enumerate(output_name):
-        output_value[i] = patch.getfloat('quantization', name, multiple=True)
-
-    # find the input value to which the data is to be quantized
-    index = output_name.index('value')
-    input_value = output_value[index]
-    # remove the value from the output list
-    del output_name[index]
-    del output_value[index]
+    begsample = -1
+    endsample = -1
 
     # there should not be any local variables in this function, they should all be global
-    del i, name
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, input_scale, input_offset, output_scale, output_offset, input_channel, input_name, output_name, output_value, i, index, input_value
-    global channel, val, idx, qname, qvalue, key
-
-    monitor.info('----------------------------------------')
-
-    for channel, name in zip(input_channel, input_name):
-        val = patch.getfloat('input', channel)
-        if val is None:
-            monitor.info(name + ' not found')
-            pass
-        else:
-            # map the Redis values to the internally used values
-            val = EEGsynth.rescale(val, slope=input_scale, offset=input_offset)
-            # look up the nearest index of the input_value vector
-            monitor.info('%s = %g' % (name, val))
-            idx = find_nearest_idx(input_value, val)
-            for qname, qvalue in zip(output_name, output_value):
-                key = '{}.{}'.format(name, qname)
-                if idx < len(qvalue):
-                    # look up the corresponding output value
-                    val = qvalue[idx]
-                else:
-                    # take the last value from the output list
-                    val = qvalue[-1]
-                monitor.info('%s = %g' % (key, val))
-                # map the internally used values to Redis values
-                val = EEGsynth.rescale(val, slope=output_scale, offset=output_offset)
-                patch.setvalue(key, val)
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, window, begsample, endsample
+    global dat, rms, i, chanvec, chanval, name, val, key
+
+    hdr_input = ft_input.getHeader()
+    if (hdr_input.nSamples - 1) < endsample:
+        raise RuntimeError("buffer reset detected")
+    if hdr_input.nSamples < window:
+        # there are not yet enough samples in the buffer
+        monitor.info('Waiting for data to arrive...')
+        return
+
+    # get the most recent data segment
+    begsample = hdr_input.nSamples - window
+    endsample = hdr_input.nSamples - 1
+    dat = ft_input.getData([begsample, endsample]).astype(np.double)
+    dat = dat[:, chanindx]
+
+    rms = [0.] * len(chanindx)
+    for i, chanvec in enumerate(dat.transpose()):
+        for chanval in chanvec:
+            rms[i] += chanval * chanval
+        if rms[i]>0:
+            # this avoids an occasional "ValueError: math domain error"
+            rms[i] = math.sqrt(rms[i] / window)
+
+    monitor.update("rms", rms)
+
+    for name, val in zip(channame, rms):
+        # send it as control value: prefix.channelX=val
+        key = "%s.%s" % (prefix, name)
+        patch.setvalue(key, val)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
@@ -172,20 +166,23 @@
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
-def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+def _stop():
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    global monitor, ft_input
+    ft_input.disconnect()
+    monitor.success('Disconnected from input FieldTrip buffer')
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/recordcontrol/__init__.py` & `eegsynth-0.7.0/module/generatecontrol/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .recordcontrol import _setup, _start, _loop_once, _loop_forever, _stop
+from .generatecontrol import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/recordcontrol/recordcontrol.py` & `eegsynth-0.7.0/module/recordcontrol/recordcontrol.py`

 * *Files 15% similar despite different names*

```diff
@@ -15,27 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import datetime
 import numpy as np
 import os
-import redis
 import sys
 import time
 import wave
+import csv
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -52,79 +50,66 @@
 import EDF
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, MININT16, MAXINT16, MININT32, MAXINT32, debug, delay, filename, fileformat, filenumber, recording, adjust
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global MININT16, MAXINT16, MININT32, MAXINT32, delay, filename, fileformat, filenumber, recording, adjust, maxabs
 
     MININT16 = -np.power(2., 15)
     MAXINT16 = np.power(2., 15) - 1
     MININT32 = -np.power(2., 31)
     MAXINT32 = np.power(2., 31) - 1
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     delay = patch.getfloat('general', 'delay')
     filename = patch.getstring('recording', 'file')
     fileformat = patch.getstring('recording', 'format')
 
     if fileformat is None:
         # determine the file format from the file name
         name, ext = os.path.splitext(filename)
         fileformat = ext[1:]
 
     filenumber = 0
     recording = False
     adjust = 1
+    maxabs = 0
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, MININT16, MAXINT16, MININT32, MAXINT32, debug, delay, filename, fileformat, filenumber, recording, adjust
-    global start, fname, f, ext, blocksize, synchronize, channels, channelz, nchans, sample, replace, i, s, z, physical_min, physical_max, meas_info, chan_info, recstart, D, chan, xval, elapsed
+    global patch, name, path, monitor
+    global MININT16, MAXINT16, MININT32, MAXINT32, delay, filename, fileformat, filenumber, recording, adjust, maxabs
+    global start, fname, f, ext, blocksize, synchronize, csvwriter, channels, channelz, nchans, sample, replace, i, s, z, physical_min, physical_max, meas_info, chan_info, recstart, D, chan, xval, elapsed
 
     # measure the time to correct for the slip
     start = time.time()
 
     if recording and not patch.getint('recording', 'record'):
         monitor.info("Recording disabled - closing " + fname)
         f.close()
@@ -133,33 +118,34 @@
 
     if not recording and not patch.getint('recording', 'record'):
         monitor.info("Recording is not enabled")
         time.sleep(1)
 
     if not recording and patch.getint('recording', 'record'):
         recording = True
+        maxabs = 0
         # open a new file
         name, ext = os.path.splitext(filename)
         if len(ext) == 0:
             ext = '.' + fileformat
         fname = name + '_' + datetime.datetime.now().strftime("%Y.%m.%d_%H.%M.%S") + ext
         # the blocksize is always 1
         blocksize = 1
         synchronize = int(patch.getfloat('recording', 'synchronize') / delay)
         assert (synchronize % blocksize) == 0, "synchronize should be multiple of blocksize"
 
         # get the details from Redis
-        channels = sorted(r.keys('*'))
-        channelz = sorted(r.keys('*'))
+        channels = sorted(patch.redis.keys('*'))
+        channelz = sorted(patch.redis.keys('*'))
         nchans = len(channels)
         # this is to keep track of the number of samples written so far
         sample = 0
 
         # search-and-replace to reduce the length of the channel labels
-        for replace in config.items('replace'):
+        for replace in patch.config.items('replace'):
             monitor.debug(replace)
             for i in range(len(channelz)):
                 channelz[i] = channelz[i].replace(replace[0], replace[1])
         for s, z in zip(channels, channelz):
             monitor.info("Writing control value " + s + " as channel " + z)
 
         # these are required for mapping floating point values onto 16 bit integers
@@ -191,47 +177,65 @@
             f.writeHeader((meas_info, chan_info))
         elif fileformat == 'wav':
             f = wave.open(fname, 'w')
             f.setnchannels(nchans)
             f.setnframes(0)
             f.setsampwidth(4)  # 1, 2 or 4
             f.setframerate(1. / delay)
+        elif fileformat == 'csv':
+            f = open(fname, 'w')
+            csvwriter = csv.writer(f, delimiter=',')
+            csvwriter.writerow(channelz)
+        elif fileformat == 'tsv':
+            f = open(fname, 'w')
+            csvwriter = csv.writer(f, delimiter='\t')
+            csvwriter.writerow(channelz)
         else:
             raise NotImplementedError('unsupported file format')
 
     if recording:
         D = []
         for chan in channels:
-            xval = r.get(chan)
             try:
-                xval = float(xval)
-            except ValueError:
+                xval = float(patch.redis.get(chan))
+            except:
                 xval = 0.
             xval = EEGsynth.limit(xval, physical_min, physical_max)
             D.append([xval])
         sample += 1
 
         if (sample % synchronize) == 0:
             key = "{}.synchronize".format(patch.getstring('prefix', 'synchronize'))
             patch.setvalue(key, sample)
 
         monitor.info("Writing sample " + str(sample) + " as " + str(np.shape(D)))
 
         if fileformat == 'edf':
             f.writeBlock(D)
         elif fileformat == 'wav':
-            D = np.asarray(D)
+            # the blocksize is always 1
+            D = np.array(D, ndmin=2).transpose()
             for x in D:
+                maxabs = max(max(abs(x)), maxabs)
+                if monitor.update('maxabs', maxabs) and maxabs>1:
+                    monitor.warning('the signal is clipping')
                 # scale the floating point values between -1 and 1
                 y = x / ((physical_max - physical_min) / 2.)
+                # the values cannot exceed the range from -1 to +1 in an int32 wav file
+                y = np.clip(y, -1.0, 1.0)
                 # scale the floating point values between MININT32 and MAXINT32
                 y = y * ((float(MAXINT32) - float(MININT32)) / 2.)
-                # convert them to packed binary data
-                z = "".join((wave.struct.pack('i', item) for item in y))
-                f.writeframesraw(z)
+                # convert them to packed binary int32 data
+                z = [int(item) for item in y]
+                f.writeframesraw(wave.struct.pack('i' * len(z), *z))
+                del x, y, z
+        elif fileformat == 'csv':
+            csvwriter.writerow([item for sublist in D for item in sublist])
+        elif fileformat == 'tsv':
+            csvwriter.writerow([item for sublist in D for item in sublist])
 
         time.sleep(adjust * delay)
 
         elapsed = time.time() - start
         # adjust the relative delay for the next iteration
         # the adjustment factor should only change a little per iteration
         adjust = 0.1 * delay / elapsed + 0.9 * adjust
@@ -240,26 +244,31 @@
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    global monitor, recording, fname, f
+    if recording:
+        recording = False
+        monitor.info("Closing " + fname)
+        f.close()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/recordsignal/__init__.py` & `eegsynth-0.7.0/module/recordsignal/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/recordsignal/recordsignal.py` & `eegsynth-0.7.0/module/recordsignal/recordsignal.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,28 +15,26 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import datetime
 import numpy as np
 import os
-import redis
 import sys
 import time
 import wave
 import struct
+import csv
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -54,54 +52,40 @@
 import EDF
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, MININT16, MAXINT16, MININT32, MAXINT32, debug, timeout, filename, fileformat, ft_host, ft_port, ft_input, hdr_input, start, recording
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global MININT16, MAXINT16, MININT32, MAXINT32, timeout, filename, fileformat, ft_host, ft_port, ft_input, hdr_input, start, recording, maxabs
 
     MININT16 = -np.power(2, 15)
     MAXINT16 = np.power(2, 15) - 1
     MININT32 = -np.power(2., 31)
     MAXINT32 = np.power(2., 31) - 1
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
     filename = patch.getstring('recording', 'file')
     fileformat = patch.getstring('recording', 'format')
 
     if fileformat is None:
         # determine the file format from the file name
         name, ext = os.path.splitext(filename)
@@ -127,27 +111,28 @@
         hdr_input = ft_input.getHeader()
 
     monitor.info('Data arrived')
     monitor.debug(hdr_input)
     monitor.debug(hdr_input.labels)
 
     recording = False
+    maxabs = 0
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, MININT16, MAXINT16, MININT32, MAXINT32, debug, timeout, filename, fileformat, ft_host, ft_port, ft_input, hdr_input, start, recording
-    global fname, f, ext, blocksize, synchronize, physical_min, physical_max, meas_info, chan_info, now, begsample, endsample, startsample, dat, key
+    global patch, name, path, monitor
+    global MININT16, MAXINT16, MININT32, MAXINT32, timeout, filename, fileformat, ft_host, ft_port, ft_input, hdr_input, start, recording, maxabs
+    global fname, f, ext, blocksize, synchronize, csvwriter, physical_min, physical_max, meas_info, chan_info, now, sample, begsample, endsample, startsample, dat, key
 
     hdr_input = ft_input.getHeader()
 
     if recording and hdr_input is None:
         monitor.info("Header is empty - closing " + fname)
         f.close()
         recording = False
@@ -161,14 +146,17 @@
 
     if not recording and not patch.getint('recording', 'record'):
         monitor.info("Recording is not enabled")
         time.sleep(1)
 
     if not recording and patch.getint('recording', 'record'):
         recording = True
+        maxabs = 0
+        # determine the filename, it may have changed
+        filename = patch.getstring('recording', 'file')
         # open a new file
         name, ext = os.path.splitext(filename)
         if len(ext) == 0:
             ext = '.' + fileformat
         fname = name + '_' + datetime.datetime.now().strftime("%Y.%m.%d_%H.%M.%S") + ext
         # the blocksize depends on the sampling rate, which may have changed
         blocksize = int(patch.getfloat('recording', 'blocksize') * hdr_input.fSample)
@@ -205,14 +193,20 @@
             f.writeHeader((meas_info, chan_info))
         elif fileformat == 'wav':
             f = wave.open(fname, 'w')
             f.setnchannels(hdr_input.nChannels)
             f.setnframes(0)
             f.setsampwidth(4)  # 1, 2 or 4
             f.setframerate(hdr_input.fSample)
+        elif fileformat == 'csv':
+            f = open(fname, 'w')
+            csvwriter = csv.writer(f, delimiter=',')
+        elif fileformat == 'tsv':
+            f = open(fname, 'w')
+            csvwriter = csv.writer(f, delimiter='\t')
         else:
             raise NotImplementedError('unsupported file format')
 
         # determine the starting point for recording
         if hdr_input.nSamples < blocksize:
             begsample = 0
             endsample = blocksize - 1
@@ -241,46 +235,64 @@
             patch.setvalue(key, endsample - startsample + 1)
         dat = ft_input.getData([begsample, endsample]).astype(np.float64)
         monitor.info("Writing sample " + str(begsample) + " to " + str(endsample) + " as " + str(np.shape(dat)))
         if fileformat == 'edf':
             # the scaling is done in the EDF writer
             f.writeBlock(np.transpose(dat))
         elif fileformat == 'wav':
-            for sample in range(len(dat)):
-                x = dat[sample, :]
+            for x in dat:
+                maxabs = max(max(abs(x)), maxabs)
+                if monitor.update('maxabs', maxabs) and maxabs>1:
+                    monitor.warning('the signal is clipping')
                 # scale the floating point values between -1 and 1
-                y = x / ((physical_max - physical_min) / 2)
+                y = x / ((physical_max - physical_min) / 2.)
+                # the values cannot exceed the range from -1 to +1 in an int32 wav file
+                y = np.clip(y, -1.0, 1.0)
                 # scale the floating point values between MININT32 and MAXINT32
                 y = y * ((float(MAXINT32) - float(MININT32)) / 2)
-                # convert them to packed binary data
+                # convert them to packed binary int32 data
                 z = [int(item) for item in y]
                 f.writeframesraw(wave.struct.pack('i' * len(z), *z))
+                del x, y, z
+        elif fileformat == 'csv':
+            for sample in range(len(dat)):
+                csvwriter.writerow(dat[sample, :])
+        elif fileformat == 'tsv':
+            for sample in range(len(dat)):
+                csvwriter.writerow(dat[sample, :])
         begsample += blocksize
         endsample += blocksize
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    global monitor, ft_input, recording, fname, f
+    ft_input.disconnect()
+    monitor.success('Disconnected from input FieldTrip buffer')
+    if recording:
+        recording = False
+        monitor.info("Closing " + fname)
+        f.close()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/recordtrigger/__init__.py` & `eegsynth-0.7.0/module/generatetrigger/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .recordtrigger import _setup, _start, _loop_once, _loop_forever, _stop
+from .generatetrigger import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/recordtrigger/recordtrigger.py` & `eegsynth-0.7.0/module/logging/logging.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,41 +1,49 @@
 #!/usr/bin/env python
 
-# This module records Redis messages (i.e. triggers) to a TSV file
+# Graphical dialog that can receive and display logging information
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
-# Copyright (C) 2018-2022 EEGsynth project
+# Copyright (C) 2023 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
-import datetime
 import os
-import redis
 import sys
+
+# exclude the eegsynth/module/logging directory from the path
+for i, dir in enumerate(sys.path):
+    if dir.endswith(os.path.join('module', 'logging')):
+        del sys.path[i]
+        continue
+
+from PyQt5 import QtGui, QtCore, QtWidgets
+from PyQt5.QtWidgets import QApplication, QWidget
+from PyQt5.QtCore import QObject, pyqtSignal
+
 import time
 import threading
-import tempfile
+import signal
+import logging
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -47,182 +55,171 @@
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
-class TriggerThread(threading.Thread):
-    def __init__(self, redischannel):
+class TriggerThread(threading.Thread, QObject):
+    signal = pyqtSignal(str)
+    def __init__(self, redischannel, callback):
         threading.Thread.__init__(self)
+        QObject.__init__(self)
         self.redischannel = redischannel
         self.running = True
-
+        # connect a Qt signal to the append function
+        self.signal.connect(callback)
     def stop(self):
         self.running = False
-
     def run(self):
-        global r, monitor, lock
-        pubsub = r.pubsub()
-        pubsub.subscribe('RECORDTRIGGER_UNBLOCK')  # this message unblocks the Redis listen command
-        pubsub.subscribe(self.redischannel)        # this message triggers the event
+        pubsub = patch.pubsub()
+        pubsub.subscribe('LOGGING_UNBLOCK')  # this message unblocks the redis listen command
+        pubsub.subscribe(self.redischannel)  # this message contains the note
         while self.running:
             for item in pubsub.listen():
-                timestamp = datetime.datetime.now().isoformat()
                 if not self.running or not item['type'] == 'message':
                     break
-                if item['channel'] == self.redischannel:
-                    val = item["data"]
-                    # the trigger value should be saved
-                    if input_scale != None or input_offset != None:
-                        try:
-                            # convert it to a number and apply the scaling and the offset
-                            val = float(val)
-                            val = EEGsynth.rescale(val, slope=input_scale, offset=input_offset)
-                        except ValueError:
-                            # keep it as a string
-                            monitor.info(("cannot apply scaling, writing %s as string" % (self.redischannel)))
-                    if f and not f.closed:
-                        # write the value, it can be either a number or a string
-                        with lock:
-                            f.write("%s\t%s\t%s\n" % (self.redischannel, val, timestamp))
-                        monitor.info(("%s\t%s\t%s" % (self.redischannel, val, timestamp)))
+                if item['channel']==self.redischannel:
+                    msg = item['data']
+                    self.signal.emit(msg)
+
+
+class QTextEditLogger_v1(logging.Handler):
+    """Class that implements a graphical window with full logging capabilities
+    """
+    def __init__(self, parent):
+        super().__init__()
+        self.widget = QtWidgets.QPlainTextEdit(parent)
+        self.widget.setReadOnly(True)
+
+    def emit(self, record):
+        msg = self.format(record)
+        self.widget.appendPlainText(msg)
+
+
+class QTextEditLogger_v2():
+    """Class that implements a graphical window with a simple append function
+    """
+    def __init__(self, parent):
+        super().__init__()
+        self.widget = QtWidgets.QPlainTextEdit(parent)
+        self.widget.setReadOnly(True)
+
+    def append(self, msg):
+        self.widget.appendPlainText(msg)
+
+
+class Window(QtWidgets.QDialog, QtWidgets.QPlainTextEdit):
+    def __init__(self, parent=None):
+        super().__init__(parent)
+        self.setGeometry(winx, winy, winwidth, winheight)
+        self.setWindowTitle(patch.getstring('display', 'title', default='EEGsynth logging'))
+
+        layout = QtWidgets.QVBoxLayout()
+
+        # logTextBox = QTextEditLogger_v1(self)
+        # logTextBox.setFormatter(logging.Formatter('%(message)s'))
+        # logTextBox.setFormatter(logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s'))
+        # logTextBox.setFormatter(logging.Formatter('%(levelname)s: %(name)s: %(message)s'))
+        # logging.getLogger().addHandler(logTextBox)
+        # logging.getLogger().setLevel(logging.DEBUG)
+        # layout.addWidget(logTextBox.widget)
+
+        logTextBox = QTextEditLogger_v2(self)
+        layout.addWidget(logTextBox.widget)
+        self.append = logTextBox.append
+
+        self.setLayout(layout)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.optionxform = str
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
-
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, delay, input_scale, input_offset, filename, fileformat, f, recording, filenumber, lock, trigger, item, thread
+    global patch, name, path, monitor
+    global delay, winx, winy, winwidth, winheight, lock, trigger, app, window, timer
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    trigger = []
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-    delay = patch.getfloat('general', 'delay')
-    input_scale = patch.getfloat('input', 'scale', default=None)
-    input_offset = patch.getfloat('input', 'offset', default=None)
-    filename = patch.getstring('recording', 'file')
-    fileformat = 'tsv'
-
-    # start with a temporary file which is immediately closed
-    f = tempfile.TemporaryFile().close()
-    recording = False
-    filenumber = 0
+    delay       = patch.getfloat('general', 'delay')
+    winx        = patch.getint('display', 'xpos')
+    winy        = patch.getint('display', 'ypos')
+    winwidth    = patch.getint('display', 'width')
+    winheight   = patch.getint('display', 'height')
+
+    # start the graphical user interface
+    app = QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
+    signal.signal(signal.SIGINT, _stop)
+
+    window = Window()
+    window.show()
+
+    # Set timer for update
+    timer = QtCore.QTimer()
+    timer.timeout.connect(_loop_once)
+    timer.setInterval(10)            # timeout in milliseconds
+    timer.start(int(delay * 1000))   # in milliseconds
 
-    # this is to prevent two triggers from being saved at the same time
     lock = threading.Lock()
 
-    # create the background threads that deal with the triggers
-    trigger = []
-    monitor.info("Setting up threads for each trigger")
-    for item in config.items('trigger'):
-        trigger.append(TriggerThread(item[0]))
-        monitor.debug(item[0] + ' = OK')
+    input = patch.get('input', 'logging')
+    for redischannel in input.split(','):
+        monitor.info('setting up logging for "%s"' %(redischannel))
+        thread = TriggerThread(redischannel, window.append)
+        trigger.append(thread)
 
-    # start the thread for each of the triggers
+    # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
 
 def _loop_once():
     '''Run the main loop once
-    This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, delay, input_scale, input_offset, filename, fileformat, f, recording, filenumber, lock, trigger, item, thread
-    global fname, ext
-
-    if recording and not patch.getint('recording', 'record'):
-        monitor.info("Recording disabled - closing " + fname)
-        f.close()
-        recording = False
-        return
-
-    if not recording and not patch.getint('recording', 'record'):
-        monitor.info("Recording is not enabled")
-        time.sleep(1)
-
-    if not recording and patch.getint('recording', 'record'):
-        recording = True
-        # open a new file
-        name, ext = os.path.splitext(filename)
-        if len(ext) == 0:
-            ext = '.' + fileformat
-        fname = name + '_' + datetime.datetime.now().strftime("%Y.%m.%d_%H.%M.%S") + ext
-        monitor.info("Recording enabled - opening " + fname)
-        f = open(fname, 'w')
-        f.write("event\tvalue\ttimestamp\n")
-        f.flush()
-
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    global monitor, window
+    monitor.loop()
+    window.update()
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
-    while True:
-        monitor.loop()
-        _loop_once()
-        time.sleep(patch.getfloat('general', 'delay'))
+    QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global f, monitor, trigger, r
-    if not f.closed:
-        monitor.info('Closing file')
-        f.close()
+    global monitor, trigger
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('RECORDTRIGGER_UNBLOCK', 1)
+    patch.publish('LOGGING_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
+    QApplication.quit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/rms/__init__.py` & `eegsynth-0.7.0/module/audio2ft/__init__.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .rms import _setup, _start, _loop_once, _loop_forever, _stop
+from .audio2ft import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/rms/rms.py` & `eegsynth-0.7.0/module/threshold/threshold.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# This module calculates a sliding-window RMS value of a signal
+# This module detects whether a signal exceeds a specified threshold
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2017-2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,26 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
-import math
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -51,60 +47,44 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, rectify, invert, prefix, window, scale_threshold, offset_threshold, scale_interval, offset_interval, channels, previous, begsample, endsample
 
     try:
         ft_host = patch.getstring('fieldtrip', 'hostname')
         ft_port = patch.getint('fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.success('Connected to FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, window, begsample, endsample
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
@@ -113,95 +93,118 @@
         time.sleep(0.1)
         hdr_input = ft_input.getHeader()
 
     monitor.info('Data arrived')
     monitor.debug(hdr_input)
     monitor.debug(hdr_input.labels)
 
-    channel_items = config.items('input')
-    channame = []
-    chanindx = []
-    for item in channel_items:
-        # channel numbers are one-offset in the ini file, zero-offset in the code
-        channame.append(item[0])                             # the channel name
-        chanindx.append(patch.getint('input', item[0]) - 1)  # the channel number
-
-    prefix = patch.getstring('output', 'prefix')
-    window = patch.getfloat('processing', 'window')     # in seconds
-    window = int(window * hdr_input.fSample)            # in samples
-
-    begsample = -1
-    endsample = -1
+    # get the options from the configuration file
+    rectify = patch.getint('processing', 'rectify', default=0)
+    invert  = patch.getint('processing', 'invert', default=0)
+    prefix  = patch.getstring('output', 'prefix')
+    window  = patch.getfloat('processing', 'window')     # in seconds
+    window  = round(window * hdr_input.fSample)          # in samples
+
+    scale_threshold   = patch.getfloat('scale', 'threshold', default=1)
+    offset_threshold  = patch.getfloat('offset', 'threshold', default=0)
+    scale_interval    = patch.getfloat('scale', 'interval', default=1)
+    offset_interval   = patch.getfloat('offset', 'interval', default=0)
+
+    channels = patch.getint('input', 'channels', multiple=True)
+    channels = [chan - 1 for chan in channels] # since python using indexing from 0 instead of 1
+
+    previous = [-np.Inf] * len(channels)
+
+    # jump to the end of the input stream
+    if hdr_input.nSamples<window:
+        begsample = 0
+        endsample = window-1
+    else:
+        begsample = hdr_input.nSamples-window
+        endsample = hdr_input.nSamples-1
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, window, begsample, endsample
-    global dat, rms, i, chanvec, chanval, name, val, key
-
-    hdr_input = ft_input.getHeader()
-    if (hdr_input.nSamples - 1) < endsample:
-        raise RuntimeError("buffer reset detected")
-    if hdr_input.nSamples < window:
-        # there are not yet enough samples in the buffer
-        monitor.info('Waiting for data to arrive...')
-        return
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, rectify, invert, prefix, window, scale_threshold, offset_threshold, scale_interval, offset_interval, channels, previous, begsample, endsample
+    global dat_input, threshold, interval, channel, maxind, maxval, sample, key
 
-    # get the most recent data segment
-    begsample = hdr_input.nSamples - window
-    endsample = hdr_input.nSamples - 1
-    dat = ft_input.getData([begsample, endsample]).astype(np.double)
-    dat = dat[:, chanindx]
-
-    rms = [0.] * len(chanindx)
-    for i, chanvec in enumerate(dat.transpose()):
-        for chanval in chanvec:
-            rms[i] += chanval * chanval
-        if rms[i]>0:
-            # this avoids an occasional "ValueError: math domain error"
-            rms[i] = math.sqrt(rms[i] / window)
-
-    monitor.update("rms", rms)
-
-    for name, val in zip(channame, rms):
-        # send it as control value: prefix.channelX=val
-        key = "%s.%s" % (prefix, name)
-        patch.setvalue(key, val)
+    # determine when we start polling for available data
+    start = time.time()
+
+    while endsample>hdr_input.nSamples-1:
+        # wait until there is enough data
+        time.sleep(patch.getfloat('general', 'delay'))
+        hdr_input = ft_input.getHeader()
+        if (hdr_input.nSamples-1)<(endsample-window):
+            raise RuntimeError("buffer reset detected")
+        if (time.time()-start)>timeout:
+            raise RuntimeError("timeout while waiting for data")
+
+    # get the input data
+    dat_input = ft_input.getData([begsample, endsample]).astype(np.double)
+
+    monitor.debug("read from sample %d to %d" % (begsample, endsample))
+
+    # rectify the data
+    if rectify:
+        dat_input = np.absolute(dat_input)
+
+    # invert the data
+    if invert:
+        dat_input = -dat_input
+
+    threshold = patch.getfloat('processing', 'threshold')
+    threshold = EEGsynth.rescale(threshold, slope=scale_threshold, offset=offset_threshold)
+    interval  = patch.getfloat('processing', 'interval', default=0)
+    interval  = EEGsynth.rescale(interval, slope=scale_interval, offset=offset_interval)
+
+    for channel in channels:
+        maxind = np.argmax(dat_input[:,channel])
+        maxval = dat_input[maxind,channel]
+        sample = maxind+begsample
+        if maxval>=threshold and (sample-previous[channel])>=(interval*hdr_input.fSample):
+            key = "%s.channel%d" % (patch.getstring('output','prefix'), channel+1)
+            patch.setvalue(key, float(maxval))
+            previous[channel] = sample
+
+    # increment the counters for the next loop
+    begsample += window
+    endsample += window
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
-        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/sampler/__init__.py` & `eegsynth-0.7.0/module/sequencer/__init__.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .sampler import _setup, _start, _loop_once, _loop_forever, _stop
+from .sequencer import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/sampler/sampler.py` & `eegsynth-0.7.0/module/sampler/sampler.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,29 +15,26 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import scipy.io
 from scipy.io import wavfile
 import os
-import redis
 import sys
 import time
 import pyaudio
 import threading
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -50,15 +47,15 @@
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 
 def callback(in_data, frame_count, time_info, status):
-    global lock, debug, stack, channels, prefix, current_channel, current_value
+    global lock, stack, channels, prefix, current_channel, current_value
 
     with lock:
         begsample = 0
         endsample = min(frame_count, stack.shape[0])
         dat = stack[begsample:endsample]
         # add zero-padding if required
         pad = np.zeros((frame_count - endsample, channels), dtype=np.float32)
@@ -90,15 +87,15 @@
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
         global r, monitor, patch, stack, current_channel, current_value
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('SAMPLER_UNBLOCK')  # this message unblocks the Redis listen command
         pubsub.subscribe(self.redischannel)  # this message triggers the event
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -197,49 +194,35 @@
                             patch.setvalue("%s.%s" % (started, current_channel), current_value)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, device, scaling_method, scaling, speed, onset, offset, taper, scale_scaling, scale_speed, scale_onset, scale_offset, scale_taper, offset_scaling, offset_speed, offset_onset, offset_offset, offset_taper, started, finished, p, info, i, devinfo, lock, input_channel, input_sample, rate, dat, channels, stack, current_channel, current_value, trigger, channel, sample, thread, stream
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global device, scaling_method, scaling, speed, onset, offset, taper, scale_scaling, scale_speed, scale_onset, scale_offset, scale_taper, offset_scaling, offset_speed, offset_onset, offset_offset, offset_taper, started, finished, p, info, i, devinfo, lock, input_channel, input_sample, rate, dat, channels, stack, current_channel, current_value, trigger, channel, sample, thread, stream
 
     # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
     device = patch.getint('audio', 'device')
     scaling_method = patch.getstring('audio', 'scaling_method')
     scaling = patch.getfloat('audio', 'scaling', default=1)
     speed = patch.getfloat('audio', 'scaling', default=1)
     onset = patch.getfloat('audio', 'scaling', default=0)
     offset = patch.getfloat('audio', 'scaling', default=1)
     taper = patch.getfloat('audio', 'taper', default=0)
@@ -272,15 +255,15 @@
     monitor.info("Selected device is " + devinfo['name'])
     monitor.info(devinfo)
     monitor.info('------------------------------------------------------------------')
 
     # this is to prevent concurrency problems
     lock = threading.Lock()
 
-    input_channel, input_sample = list(zip(*config.items('input')))
+    input_channel, input_sample = list(zip(*patch.config.items('input')))
     input_sample = [x.split(',') for x in input_sample]
 
     # open first file to determine the format
     rate, dat = wavfile.read(input_sample[0][0])
 
     if len(dat.shape) == 1:
         channels = 1
@@ -323,37 +306,37 @@
     '''
     pass
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, stream, p, trigger
     monitor.success("Closing stream")
     stream.stop_stream()
     stream.close()
     p.terminate()
     monitor.success("Closing threads")
     for thread in trigger:
         thread.stop()
-    r.publish('SAMPLER_UNBLOCK', 1)
+    patch.publish('SAMPLER_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/sequencer/__init__.py` & `eegsynth-0.7.0/module/complexity/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .sequencer import _setup, _start, _loop_once, _loop_forever, _stop
+from .complexity import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/sequencer/sequencer.py` & `eegsynth-0.7.0/module/sequencer/sequencer.py`

 * *Files 7% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import math
 import numpy as np
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -77,97 +74,84 @@
             self.duration = duration
 
     def stop(self):
         self.running = False
 
     def run(self):
         global r, monitor, patch
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('SEQUENCER_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)    # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
+                    monitor.debug(item)
                     now = time.time()
                     if self.prevtime != None:
                         self.steptime = now - self.prevtime
                     self.prevtime = now
                     if len(self.sequence) > 0:
                         # the sequence can consist of a list of values or a list of Redis channels
                         val = self.sequence[self.step % len(self.sequence)]
 
-                        try:
-                            # convert the string from the ini to floating point
-                            val = float(val)
-                        except:
-                            # get the value from Redis
-                            val = r.get(val)
-                            if val == None:
+                        if val[0].isalpha():
+                            # get the value directly from Redis
+                            try:
+                                val = float(patch.redis.get(val))
+                            except:
                                 val = 0.
-                            else:
-                                # convert the string from Redis to floating point
+                        else:
+                            try:
                                 val = float(val)
+                            except ValueError:
+                                val = 0.
 
                         # apply the scaling, offset and transpose the note
                         val = EEGsynth.rescale(val, slope=scale_note, offset=offset_note)
                         val += self.transpose
+
                         # send it as sequencer.note with the note as value
                         patch.setvalue(self.key, val, duration=self.duration * self.steptime)
                         if val >= 1.:
                             # send it also as sequencer.noteXXX with value 1.0
-                            key = '%s%03d' % (self.key, val)
+                            key = '%s%03d' % (self.key, round(val))
                             patch.setvalue(key, 1., duration=self.duration * self.steptime)
                         monitor.info("step %2d : %s = %g" % (self.step + 1, self.key, val))
                         # increment to the next step
                         self.step = (self.step + 1) % len(self.sequence)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    global patch, name, path, monitor
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
-
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, stepsize, clock, prefix, scale_active, scale_transpose, scale_note, scale_duration, offset_active, offset_transpose, offset_note, offset_duration, lock, key, sequencethread
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global stepsize, clock, prefix, scale_active, scale_transpose, scale_note, scale_duration, offset_active, offset_transpose, offset_note, offset_duration, lock, key, sequencethread
 
     # get the options from the configuration file
     stepsize = patch.getfloat('general', 'delay')
-    clock = patch.getstring('sequence', 'clock')  # the clock signal for the sequence
     prefix = patch.getstring('output', 'prefix')
 
     # these scale and offset parameters are used to map between Redis and internal values
     scale_active = patch.getfloat('scale', 'active',     default=127)
     scale_transpose = patch.getfloat('scale', 'transpose',  default=127)
     scale_note = patch.getfloat('scale', 'note',       default=1)
     scale_duration = patch.getfloat('scale', 'duration',   default=1)
@@ -175,14 +159,16 @@
     offset_transpose = patch.getfloat('offset', 'transpose', default=0)
     offset_note = patch.getfloat('offset', 'note',      default=0)
     offset_duration = patch.getfloat('offset', 'duration',  default=0)
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
+    # the clock signal for the sequence
+    clock = patch.get('sequence', 'clock')
     # the notes will be sent to Redis using this key
     key = "{}.note".format(prefix)
 
     # create and start the thread for the output
     sequencethread = SequenceThread(clock, key)
     sequencethread.start()
 
@@ -200,16 +186,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, stepsize, clock, prefix, scale_active, scale_transpose, scale_note, scale_duration, offset_active, offset_transpose, offset_note, offset_duration, lock, key, sequencethread
+    global patch, name, path, monitor
+    global stepsize, clock, prefix, scale_active, scale_transpose, scale_note, scale_duration, offset_active, offset_transpose, offset_note, offset_duration, lock, key, sequencethread
     global active, sequence, transpose, duration, elapsed, naptime
 
     # the active sequence is specified as an integer between 0 and 127
     active = patch.getfloat('sequence', 'active', default=0)
     active = EEGsynth.rescale(active, slope=scale_active, offset=offset_active)
     active = int(active)
 
@@ -241,15 +227,15 @@
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         # measure the time to correct for the slip
         start = time.time()
 
         monitor.loop()
         _loop_once()
 
@@ -258,29 +244,29 @@
         naptime = stepsize - elapsed
         if naptime > 0:
             monitor.trace("naptime = " + str(naptime))
             time.sleep(naptime)
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, patch, sequencethread, r
     try:
         monitor.success("Disabling last note")
         patch.setvalue(key, 0.)
     except:
         pass
     monitor.success('Closing threads')
     sequencethread.stop()
-    r.publish('SEQUENCER_UNBLOCK', 1)
+    patch.publish('SEQUENCER_UNBLOCK', 1)
     sequencethread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/slewlimiter/__init__.py` & `eegsynth-0.7.0/module/clockmultiplier/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .slewlimiter import _setup, _start, _loop_once, _loop_forever, _stop
+from .clockmultiplier import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/slewlimiter/slewlimiter.py` & `eegsynth-0.7.0/module/slewlimiter/slewlimiter.py`

 * *Files 15% similar despite different names*

```diff
@@ -15,24 +15,21 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -47,68 +44,55 @@
 sys.path.insert(0, os.path.join(path, '../../lib'))
 import EEGsynth
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, prefix, input_name, input_variable, previous_val
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global prefix, input_name, input_variable, previous_val
 
     # get the options from the configuration file
     prefix = patch.getstring('output', 'prefix')
 
     # get the list of input variables
-    input_name, input_variable = list(map(list, list(zip(*config.items('input')))))
+    input_name, input_variable = list(map(list, list(zip(*patch.config.items('input')))))
 
     previous_val = {}
     for name in input_name:
         previous_val[name] = None
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, prefix, input_name, input_variable, previous_val
+    global patch, name, path, monitor
+    global prefix, input_name, input_variable, previous_val
 
     lrate = patch.getfloat('processing', 'learning_rate', default=1)
 
     for name, variable in zip(input_name, input_variable):
         key = '%s.%s' % (prefix, variable)
         val = patch.getfloat('input', name)
         if val is None:
@@ -132,19 +116,20 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    pass
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/sonification/__init__.py` & `eegsynth-0.7.0/module/bitalino2ft/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .sonification import _setup, _start, _loop_once, _loop_forever, _stop
+from .bitalino2ft import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/sonification/sonification.py` & `eegsynth-0.7.0/module/sonification/sonification.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,25 +15,22 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -50,37 +47,33 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # there should not be any local variables in this function, they should all be global
+    if len(locals()):
+        print('LOCALS: ' + ', '.join(locals().keys()))
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, sample_rate, f_shift, f_offset, f_order, window, sideband, left, right, scaling, scaling_method, scale_scaling, offset_scaling, default_scale, scale_lowpass, scale_highpass, offset_lowpass, offset_highpass, scale_filterorder, offset_filterorder, hdr_output, nInput, nOutput, begsample, endsample, dat_output, left_f, left_b, left_a, left_zi, right_f, right_b, right_a, right_zi, i, highpass, lowpass
 
     try:
         ft_host = patch.getstring('input_fieldtrip', 'hostname')
         ft_port = patch.getint('input_fieldtrip', 'port')
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
@@ -94,28 +87,16 @@
         monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_output = FieldTrip.Client()
         ft_output.connect(ft_host, ft_port)
         monitor.success('Connected to output FieldTrip buffer')
     except:
         raise RuntimeError("cannot connect to output FieldTrip buffer")
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output, name
-    global timeout, hdr_input, start, sample_rate, f_shift, f_offset, f_order, window, sideband, left, right, scaling, scaling_method, scale_scaling, offset_scaling, default_scale, scale_lowpass, scale_highpass, offset_lowpass, offset_highpass, scale_filterorder, offset_filterorder, hdr_output, nInput, nOutput, begsample, endsample, dat_output, left_f, left_b, left_a, left_zi, right_f, right_b, right_a, right_zi, i, highpass, lowpass
-
     # this is the timeout for the FieldTrip buffer
-    timeout     = patch.getfloat('input_fieldtrip', 'timeout', default=30)
+    timeout = patch.getfloat('input_fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info('Waiting for data to arrive...')
         if (time.time()-start) > timeout:
             raise RuntimeError("timeout while waiting for data")
@@ -139,16 +120,16 @@
     # these are for multiplying/attenuating the output signal
     scaling        = patch.getfloat('sonification', 'scaling')
     scaling_method = patch.getstring('sonification', 'scaling_method')
     scale_scaling  = patch.getfloat('scale', 'scaling', default=1)
     offset_scaling = patch.getfloat('offset', 'scaling', default=0)
 
     try:
-        float(config.get('processing', 'highpassfilter'))
-        float(config.get('processing', 'lowpassfilter'))
+        float(patch.config.get('processing', 'highpassfilter'))
+        float(patch.config.get('processing', 'lowpassfilter'))
         # the filter frequencies are specified as numbers
         default_scale = 1.
     except:
         # the filter frequencies are specified as Redis channels
         # scale them to the Nyquist frequency
         default_scale = sample_rate/2
 
@@ -241,16 +222,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, ft_output
-    global timeout, hdr_input, start, sample_rate, f_shift, f_offset, f_order, window, sideband, left, right, scaling, scaling_method, scale_scaling, offset_scaling, default_scale, scale_lowpass, scale_highpass, offset_lowpass, offset_highpass, scale_filterorder, offset_filterorder, hdr_output, nInput, nOutput, begsample, endsample, dat_output, left_f, left_b, left_a, left_zi, right_f, right_b, right_a, right_zi, i, highpass, lowpass
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, ft_output, timeout, hdr_input, start, sample_rate, f_shift, f_offset, f_order, window, sideband, left, right, scaling, scaling_method, scale_scaling, offset_scaling, default_scale, scale_lowpass, scale_highpass, offset_lowpass, offset_highpass, scale_filterorder, offset_filterorder, hdr_output, nInput, nOutput, begsample, endsample, dat_output, left_f, left_b, left_a, left_zi, right_f, right_b, right_a, right_zi, i, highpass, lowpass
     global dat_input, begtime, endtime, tim_input, tim_output, chan, vec_output, highpassfilter, lowpassfilter, filterorder, change, b, a, zi, duration, desired
 
     # determine when we start polling for available data
     start = time.time()
 
     while endsample > hdr_input.nSamples-1:
         # wait until there is enough data
@@ -361,19 +342,22 @@
     global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    sys.exit()
+    global monitor, ft_input
+    ft_input.disconnect()
+    monitor.success('Disconnected from input FieldTrip buffer')
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/spectral/__init__.py` & `eegsynth-0.7.0/module/inputlsl/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .spectral import _setup, _start, _loop_once, _loop_forever, _stop
+from .inputlsl import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/spectral/spectral.py` & `eegsynth-0.7.0/module/spectral/spectral.py`

 * *Files 9% similar despite different names*

```diff
@@ -15,26 +15,23 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import numpy as np
 import os
-import redis
 import sys
 import time
 from scipy.signal import detrend
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -51,53 +48,40 @@
 import FieldTrip
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
+def _start():
+    '''Start the module
+    This uses the global variables from setup and adds a set of global variables
+    '''
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, output, begsample, endsample
 
     try:
         ft_host = patch.getstring('fieldtrip','hostname')
         ft_port = patch.getint('fieldtrip','port')
         monitor.info('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
         ft_input = FieldTrip.Client()
         ft_input.connect(ft_host, ft_port)
         monitor.info("Connected to FieldTrip buffer")
     except:
         raise RuntimeError("cannot connect to FieldTrip buffer")
 
-
-def _start():
-    '''Start the module
-    This uses the global variables from setup and adds a set of global variables
-    '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, output, begsample, endsample
-
     # this is the timeout for the FieldTrip buffer
     timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
 
     hdr_input = None
     start = time.time()
     while hdr_input is None:
         monitor.info("Waiting for data to arrive...")
@@ -106,57 +90,57 @@
         time.sleep(0.1)
         hdr_input = ft_input.getHeader()
 
     monitor.info("Data arrived")
     monitor.debug(hdr_input)
     monitor.debug(hdr_input.labels)
 
-    channel_items = config.items('input')
+    channel_items = patch.config.items('input')
     channame = []
     chanindx = []
     for item in channel_items:
         # channel numbers are one-offset in the ini file, zero-offset in the code
         channame.append(item[0])
         chanindx.append(patch.getint('input', item[0])-1)
 
     monitor.info(str(channame) + " " + str(chanindx))
 
     prefix = patch.getstring('output', 'prefix')
-    output = patch.getstring('processing', 'output', default='power')  # amplitude or power
+    output = patch.getstring('processing', 'output', default='amplitude')  # amplitude, power or db
 
     begsample = -1
     endsample = -1
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, output, begsample, endsample
+    global patch, name, path, monitor
+    global ft_host, ft_port, ft_input, timeout, hdr_input, start, channel_items, channame, chanindx, item, prefix, output, begsample, endsample
     global scale_window, offset_window, window, taper, frequency, band_items, bandname, bandlo, bandhi, lohi, dat, power, chan, band, meandat, sample, F, i, lo, hi, count, key
 
     scale_window = patch.getfloat('scale', 'window', default=1.)
     offset_window = patch.getfloat('offset', 'window', default=0.)
     window = patch.getfloat('processing', 'window', default=2)
     window = EEGsynth.rescale(window, slope=scale_window, offset=offset_window)
 
     monitor.update('window', window)
 
     window = int(round(window * hdr_input.fSample))  # in samples
     taper = np.hanning(window)
     frequency = np.fft.fftfreq(window, 1.0 / hdr_input.fSample)
 
-    band_items = config.items('band')
+    band_items = patch.config.items('band')
     bandname = []
     bandlo   = []
     bandhi   = []
     for item in band_items:
         # channel numbers are one-offset in the ini file, zero-offset in the code
-        lohi = patch.getfloat('band', item[0], multiple=True)
+        lohi = patch.getfloat('band', item[0], multiple=True, default=[0,hdr_input.fSample/2])
         bandname.append(item[0])
         bandlo.append(lohi[0])
         bandhi.append(lohi[1])
 
     monitor.debug(bandname, bandlo, bandhi)
 
     hdr_input = ft_input.getHeader()
@@ -180,34 +164,33 @@
     dat = dat * taper[:, np.newaxis]
 
     # compute the FFT over the sample direction
     if output == 'amplitude':
         F = abs(np.fft.fft(dat, axis=0))
     elif output == 'power':
         F = abs(np.fft.fft(dat, axis=0))**2
+    elif output == 'db':
+        F = 10*np.log10(abs(np.fft.fft(dat, axis=0)))
+
+    # this vector contains the spectral estimate for each channel and frequency band
+    value = [np.nan] * len(channame) * len(bandname)
 
-    value = [0] * len(channame) * len(bandname)
     i = 0
-    for chan in range(F.shape[1]):
-        for lo,hi in zip(bandlo,bandhi):
-            value[i] = 0
-            count = 0
-            for sample in range(len(frequency)):
-                if frequency[sample]>=lo and frequency[sample]<=hi:
-                    value[i] += F[sample, chan]
-                    count        += 1
-            if count>0:
-                value[i] /= count
+    for lo,hi in zip(bandlo,bandhi):
+        freqindx = np.logical_and(frequency>=lo, frequency<=hi)
+        for chan in range(F.shape[1]):
+            if freqindx.sum()>0:
+                value[i] = np.mean(F[freqindx, chan])
             i+=1
-
+    
     monitor.debug(np.around(value))
 
     i = 0
-    for chan in channame:
-        for band in bandname:
+    for band in bandname:
+        for chan in channame:
             key = "%s.%s.%s" % (prefix, chan, band)
             patch.setvalue(key, value[i])
             i+=1
 
 
 def _loop_forever():
     '''Run the main loop forever
@@ -216,22 +199,22 @@
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, ft_input
     ft_input.disconnect()
     monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/synthesizer/__init__.py` & `eegsynth-0.7.0/module/accelerometer/__init__.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .synthesizer import _setup, _start, _loop_once, _loop_forever, _stop
+from .accelerometer import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/synthesizer/synthesizer.py` & `eegsynth-0.7.0/module/synthesizer/synthesizer.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,28 +15,25 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import math
 import multiprocessing
 import os
 import pyaudio
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -60,15 +57,15 @@
             self.time = 0
             self.last = 0
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('SYNTHESIZER_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(patch.getstring('control', 'adsr_gate'))
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 monitor.trace(item)
@@ -185,52 +182,37 @@
             monitor.update('adsr_release ', adsr_release)
             monitor.update('vca_envelope ', vca_envelope)
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    global patch, name, path, monitor
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, debug, p, device, rate, blocksize, nchans, format, info, stream, lock, control, trigger, devinfo, block, offset, autoscale
+    global patch, name, path, monitor
+    global p, device, rate, blocksize, nchans, format, info, stream, lock, control, trigger, devinfo, block, offset, autoscale
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     p = pyaudio.PyAudio()
 
+    # get the options from the configuration file
     device = patch.getint('audio', 'device')
     rate = patch.getint('audio', 'rate')
     blocksize = patch.getint('audio', 'blocksize')
     nchans = 1
     format = p.get_format_from_width(2)  # the desired sample width in bytes (1, 2, 3, or 4)
 
     monitor.info('------------------------------------------------------------------')
@@ -274,16 +256,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, debug, p, device, rate, blocksize, nchans, format, info, stream, lock, control, trigger, devinfo, block, offset, autoscale
+    global patch, name, path, monitor
+    global p, device, rate, blocksize, nchans, format, info, stream, lock, control, trigger, devinfo, block, offset, autoscale
     global BUFFER, t, last, vco_pitch, vco_sin, vco_tri, vco_saw, vco_sqr, lfo_depth, lfo_frequency, adsr_attack, adsr_decay, adsr_sustain, adsr_release, vca_envelope, frequency, period, wave_sin, wave_tri, wave_saw, wave_sqr, waveform, lfo_envelope, adsr_envelope
 
     ################################################################################
     # this is constantly generating the output signal
     ################################################################################
     BUFFER = ''
 
@@ -352,36 +334,36 @@
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor, patch
+    global monitor
     while True:
         monitor.loop()
         _loop_once()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global monitor, control, trigger, r, stream, p
+    global monitor, control, trigger, stream, p
     monitor.success('Closing threads')
     control.stop()
     trigger.stop()
-    r.publish('SYNTHESIZER_UNBLOCK', 1)
+    patch.publish('SYNTHESIZER_UNBLOCK', 1)
     control.join()
     trigger.join()
     stream.stop_stream()
     stream.close()
     p.terminate()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/threshold/__init__.py` & `eegsynth-0.7.0/module/threshold/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/threshold/threshold.py` & `eegsynth-0.7.0/module/unicorn2ft/unicorn2ft.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,229 +1,212 @@
 #!/usr/bin/env python
 
-# This module detects whether a signal exceeds a specified threshold
+# Unicorn2ft module that streams data from a Unicorn Hybrid Black EEG system
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
-# Copyright (C) 2017-2022 EEGsynth project
+# Copyright (C) 2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
-import numpy as np
 import os
-import redis
 import sys
 import time
+import serial
+import struct
+import numpy as np
+import serial.tools.list_ports
+from fuzzywuzzy import process
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
-elif __name__=='__main__' and sys.argv[0] != '':
+elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
-elif __name__=='__main__':
+elif __name__ == '__main__':
     path = os.path.abspath('')
     file = os.path.split(path)[-1] + '.py'
     name = os.path.splitext(file)[0]
 else:
     path = os.path.split(__file__)[0]
     file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, '../../lib'))
-import EEGsynth
 import FieldTrip
+import EEGsynth
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    global patch, name, path, monitor
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general','debug'))
-
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-
-    try:
-        ft_host = patch.getstring('fieldtrip', 'hostname')
-        ft_port = patch.getint('fieldtrip', 'port')
-        monitor.success('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
-        ft_input = FieldTrip.Client()
-        ft_input.connect(ft_host, ft_port)
-        monitor.success('Connected to FieldTrip buffer')
-    except:
-        raise RuntimeError("cannot connect to FieldTrip buffer")
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input, name
-    global timeout, hdr_input, start, rectify, invert, prefix, window, scale_threshold, offset_threshold, scale_interval, offset_interval, channels, previous, begsample, endsample
+    global patch, name, path, monitor
+    global prefix, ft_host, ft_port, ft_output, timeout, blocksize, nchan, fsample, serialdevice, start_acq, stop_acq, start_sequence, stop_sequence, s, response
 
-    # this is the timeout for the FieldTrip buffer
-    timeout = patch.getfloat('fieldtrip', 'timeout', default=30)
-
-    hdr_input = None
-    start = time.time()
-    while hdr_input is None:
-        monitor.info('Waiting for data to arrive...')
-        if (time.time() - start) > timeout:
-            raise RuntimeError("timeout while waiting for data")
-        time.sleep(0.1)
-        hdr_input = ft_input.getHeader()
-
-    monitor.info('Data arrived')
-    monitor.debug(hdr_input)
-    monitor.debug(hdr_input.labels)
+    try:
+        ft_host = patch.getstring('fieldtrip', 'hostname')
+        ft_port = patch.getint('fieldtrip', 'port')
+        monitor.info('Trying to connect to buffer on %s:%i ...' % (ft_host, ft_port))
+        ft_output = FieldTrip.Client()
+        ft_output.connect(ft_host, ft_port)
+        monitor.info("Connected to output FieldTrip buffer")
+    except:
+        raise RuntimeError("cannot connect to output FieldTrip buffer")
 
     # get the options from the configuration file
-    rectify = patch.getint('processing', 'rectify', default=0)
-    invert  = patch.getint('processing', 'invert', default=0)
-    prefix  = patch.getstring('output', 'prefix')
-    window  = patch.getfloat('processing', 'window')     # in seconds
-    window  = round(window * hdr_input.fSample)          # in samples
-
-    scale_threshold   = patch.getfloat('scale', 'threshold', default=1)
-    offset_threshold  = patch.getfloat('offset', 'threshold', default=0)
-    scale_interval    = patch.getfloat('scale', 'interval', default=1)
-    offset_interval   = patch.getfloat('offset', 'interval', default=0)
-
-    channels = patch.getint('input', 'channels', multiple=True)
-    channels = [chan - 1 for chan in channels] # since python using indexing from 0 instead of 1
-
-    previous = [-np.Inf] * len(channels)
-
-    # jump to the end of the input stream
-    if hdr_input.nSamples<window:
-        begsample = 0
-        endsample = window-1
-    else:
-        begsample = hdr_input.nSamples-window
-        endsample = hdr_input.nSamples-1
+    timeout = patch.getfloat('unicorn', 'timeout', default=5)
+    blocksize = patch.getfloat('unicorn', 'blocksize', default=0.2) # write blocks of 0.2 seconds, i.e., 50 samples
+
+    # write the header information to the FieldTrip buffer
+    nchan = 16
+    fsample = 250
+    ft_output.putHeader(nchan, fsample, FieldTrip.DATATYPE_FLOAT32)
+
+    monitor.success("connecting to Unicorn...")
+
+    # get the specified serial device, or the one that is the closest match
+    serialdevice = patch.getstring('unicorn', 'device')
+    serialdevice = EEGsynth.trimquotes(serialdevice)
+    serialdevice = process.extractOne(serialdevice, [comport.device for comport in serial.tools.list_ports.comports()])[0] # select the closest match
+
+    start_acq      = [0x61, 0x7C, 0x87]
+    stop_acq       = [0x63, 0x5C, 0xC5]
+    start_response = [0x00, 0x00, 0x00]
+    stop_response  = [0x00, 0x00, 0x00]
+    start_sequence = [0xC0, 0x00]
+    stop_sequence  = [0x0D, 0x0A]
+
+    try:
+        s = serial.Serial(serialdevice, 115200, timeout=timeout)
+        monitor.success("connected to serial port " + serialdevice)
+    except:
+        raise RuntimeError("cannot connect to serial port " + serialdevice)
+
+    # start the data stream
+    s.write(start_acq)
+
+    response = s.read(3)
+    if response != b'\x00\x00\x00':
+        raise RuntimeError("cannot start data stream")
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+        print("LOCALS: " + ", ".join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
-    This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, monitor, debug, ft_host, ft_port, ft_input
-    global timeout, hdr_input, start, rectify, invert, prefix, window, scale_threshold, offset_threshold, scale_interval, offset_interval, channels, previous, begsample, endsample
-    global dat_input, threshold, interval, channel, maxind, maxval, sample, key
+    global patch, name, path, monitor
+    global prefix, ft_host, ft_port, ft_output, timeout, blocksize, nchan, fsample, serialdevice, start_acq, stop_acq, start_sequence, stop_sequence, s, response
 
-    # determine when we start polling for available data
-    start = time.time()
+    nsample = int(blocksize*fsample)
+    dat = np.zeros((nsample,nchan))
 
-    while endsample>hdr_input.nSamples-1:
-        # wait until there is enough data
-        time.sleep(patch.getfloat('general', 'delay'))
-        hdr_input = ft_input.getHeader()
-        if (hdr_input.nSamples-1)<(endsample-window):
-            raise RuntimeError("buffer reset detected")
-        if (time.time()-start)>timeout:
-            raise RuntimeError("timeout while waiting for data")
-
-    # get the input data
-    dat_input = ft_input.getData([begsample, endsample]).astype(np.double)
-
-    monitor.debug("read from sample %d to %d" % (begsample, endsample))
-
-    # rectify the data
-    if rectify:
-        dat_input = np.absolute(dat_input)
-
-    # invert the data
-    if invert:
-        dat_input = -dat_input
-
-    threshold = patch.getfloat('processing', 'threshold')
-    threshold = EEGsynth.rescale(threshold, slope=scale_threshold, offset=offset_threshold)
-    interval  = patch.getfloat('processing', 'interval', default=0)
-    interval  = EEGsynth.rescale(interval, slope=scale_interval, offset=offset_interval)
-
-    for channel in channels:
-        maxind = np.argmax(dat_input[:,channel])
-        maxval = dat_input[maxind,channel]
-        sample = maxind+begsample
-        if maxval>=threshold and (sample-previous[channel])>=(interval*hdr_input.fSample):
-            key = "%s.channel%d" % (patch.getstring('output','prefix'), channel+1)
-            patch.setvalue(key, float(maxval))
-            previous[channel] = sample
-
-    # increment the counters for the next loop
-    begsample += window
-    endsample += window
-
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
+    for sample in range(0,nsample):
+        # read one block of data from the serial port
+        payload = s.read(45)
+
+        # check the start and end bytes
+        if payload[0:2] != b'\xC0\x00':
+            raise RuntimeError("invalid packet")
+        if payload[43:45] != b'\x0D\x0A':
+            raise RuntimeError("invalid packet")
+
+        battery = 100*float(payload[2] & 0x0F)/15
+
+        eeg = np.zeros(8)
+        for ch in range(0,8):
+            # unpack as a big-endian 32 bit signed integer
+            eegv = struct.unpack('>i', b'\x00' + payload[(3+ch*3):(6+ch*3)])[0]
+            # apply two’s complement to the 32-bit signed integral value if the sign bit is set
+            if (eegv & 0x00800000):
+                eegv = eegv | 0xFF000000
+            eeg[ch] = float(eegv) * 4500000. / 50331642.
+
+        accel = np.zeros(3)
+        # unpack as a little-endian 16 bit signed integer
+        accel[0] = float(struct.unpack('<h', payload[27:29])[0]) / 4096.
+        accel[1] = float(struct.unpack('<h', payload[29:31])[0]) / 4096.
+        accel[2] = float(struct.unpack('<h', payload[31:33])[0]) / 4096.
+
+        gyro = np.zeros(3)
+        # unpack as a little-endian 16 bit signed integer
+        gyro[0] = float(struct.unpack('<h', payload[27:29])[0]) / 32.8
+        gyro[1] = float(struct.unpack('<h', payload[29:31])[0]) / 32.8
+        gyro[2] = float(struct.unpack('<h', payload[31:33])[0]) / 32.8
+
+        counter = struct.unpack('<L', payload[39:43])[0]
+
+        # collect the data that will be sent to the FieldTrip buffer
+        dat[sample,0:8]   = eeg
+        dat[sample,8:11]  = accel
+        dat[sample,11:14] = gyro
+        dat[sample,14]    = battery
+        dat[sample,15]    = counter
+
+    # write the segment of data to the FieldTrip buffer
+    ft_output.putData(dat.astype(np.float32))
+    monitor.info('wrote samples %d' % counter)
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
-    global monitor
+    global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
+        time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop():
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
-    global ft_input, monitor
-    ft_input.disconnect()
-    monitor.success('Disconnected from input FieldTrip buffer')
-    sys.exit()
+    global s, stop_acq
+    # stop the data stream and close the serial port
+    s.write(stop_acq)
+    monitor.success("Closing serial port")
+    s.close()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `eegsynth-0.6.0/module/unicorn2ft/__init__.py` & `eegsynth-0.7.0/module/geomixer/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .unicorn2ft import _setup, _start, _loop_once, _loop_forever, _stop
+from .geomixer import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/volcabass/__init__.py` & `eegsynth-0.7.0/module/generatesignal/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .volcabass import _setup, _start, _loop_once, _loop_forever, _stop
+from .generatesignal import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/volcabass/volcabass.py` & `eegsynth-0.7.0/module/volcakeys/volcakeys.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# Volcabass outputs Redis data via MIDI to the Korg Volca Bass synthesizer
+# Volcakeys outputs Redis data via MIDI to the Korg Volca Keys synthesizer
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2017-2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -58,16 +55,17 @@
         self.note = note
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
-        pubsub.subscribe('VOLCABASS_UNBLOCK')  # this message unblocks the redis listen command
+        global monitor, scale, offset
+        pubsub = patch.pubsub()
+        pubsub.subscribe('VOLCAKEYS_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)    # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
                     monitor.trace(item)
@@ -81,66 +79,51 @@
                         outputport.send(msg)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # the list of MIDI commands is the only aspect that is specific to the Volca Bass
-    # see http://media.aadl.org/files/catalog_guides/1444141_chart.pdf
-    control_name = ['slide_time', 'expression', 'octave', 'lfo_rate', 'lfo_int', 'vco_pitch1',
-                    'vco_pitch2', 'vco_pitch3', 'attack', 'decay_release', 'cutoff_intensity', 'gate_time']
-    control_code = [5, 11, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49]
+    # the list of MIDI commands is the only aspect that is specific to the Volca Keys
+    # see http://media.aadl.org/files/catalog_guides/1444140_chart.pdf
+    control_name = ['portamento', 'expression', 'voice', 'octave', 'detune', 'vco_eg_int', 'vcf_cutoff', 'vcf_eg_int', 'lfo_rate',
+                    'lfo_pitch_int', 'lfo_cutoff_int', 'eg_attack', 'eg_decay_release', 'eg_sustain', 'delay_time', 'delay_feedback']
+    control_code = [5, 11, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53]
     note_name = ['C0', 'Db0', 'D0', 'Eb0', 'E0', 'F0', 'Gb0', 'G0', 'Ab0', 'A0', 'Bb0', 'B0', 'C1', 'Db1', 'D1', 'Eb1', 'E1', 'F1', 'Gb1', 'G1', 'Ab1', 'A1', 'Bb1', 'B1', 'C2', 'Db2', 'D2', 'Eb2', 'E2', 'F2', 'Gb2', 'G2', 'Ab2', 'A2', 'Bb2', 'B2', 'C3', 'Db3', 'D3', 'Eb3', 'E3', 'F3', 'Gb3', 'G3', 'Ab3', 'A3', 'Bb3', 'B3', 'C4', 'Db4', 'D4', 'Eb4', 'E4', 'F4', 'Gb4', 'G4', 'Ab4', 'A4', 'Bb4', 'B4', 'C5', 'Db5', 'D5', 'Eb5', 'E5', 'F5',
                  'Gb5', 'G5', 'Ab5', 'A5', 'Bb5', 'B5', 'C6', 'Db6', 'D6', 'Eb6', 'E6', 'F6', 'Gb6', 'G6', 'Ab6', 'A6', 'Bb6', 'B6', 'C7', 'Db7', 'D7', 'Eb7', 'E7', 'F7', 'Gb7', 'G7', 'Ab7', 'A7', 'Bb7', 'B7', 'C8', 'Db8', 'D8', 'Eb8', 'E8', 'F8', 'Gb8', 'G8', 'Ab8', 'A8', 'Bb8', 'B8', 'C9', 'Db9', 'D9', 'Eb9', 'E9', 'F9', 'Gb9', 'G9', 'Ab9', 'A9', 'Bb9', 'B9', 'C10', 'Db10', 'D10', 'Eb10', 'E10', 'F10', 'Gb10', 'G10', 'Ab10', 'A10', 'Bb10', 'B10']
     note_code = [12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81,
                  82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143]
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-
     # this is only for debugging, check which MIDI devices are accessible
     monitor.info('------ OUTPUT ------')
     for port in mido.get_output_names():
         monitor.info(port)
     monitor.info('-------------------------')
 
+    # get the options from the configuration file
     midichannel = patch.getint('midi', 'channel') - 1  # channel 1-16 get mapped to 0-15
     mididevice = patch.getstring('midi', 'device')
     mididevice = EEGsynth.trimquotes(mididevice)
     mididevice = process.extractOne(mididevice, mido.get_output_names())[0]  # select the closest match
 
     try:
         outputport = mido.open_output(mididevice)
@@ -154,17 +137,17 @@
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     # each of the notes that can be played is mapped onto a different trigger
     trigger = []
     for name, code in zip(note_name, note_code):
-        if config.has_option('note', name):
+        if patch.config.has_option('note', name):
             # start the background thread that deals with this note
-            this = TriggerThread(patch.getstring('note', name), code)
+            this = TriggerThread(patch.get('note', name), code)
             trigger.append(this)
             monitor.debug(name + ' trigger configured')
 
     # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
@@ -178,16 +161,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
     global cmd, val, msg
 
     for name, cmd in zip(control_name, control_code):
         # loop over the control values
         val = patch.getfloat('control', name)
         if val == None:
             continue  # it should be skipped when not present
@@ -199,42 +182,38 @@
         val = EEGsynth.limit(val, 0, 127)
         val = int(val)
         msg = mido.Message('control_change', control=cmd, value=val, channel=midichannel)
         monitor.debug(cmd, val, name)
         with lock:
             outputport.send(msg)
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('VOLCABASS_UNBLOCK', 1)
+    patch.publish('VOLCAKEYS_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/volcabeats/volcabeats.py` & `eegsynth-0.7.0/module/volcabeats/volcabeats.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -58,15 +55,15 @@
         self.note = note
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        pubsub = r.pubsub()
+        pubsub = patch.pubsub()
         pubsub.subscribe('VOLCABEATS_UNBLOCK') # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)    # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
@@ -81,64 +78,50 @@
                         outputport.send(msg)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
 
     # the list of MIDI commands is the only aspect that is specific to the Volca Beats
     # see http://media.aadl.org/files/catalog_guides/1445131_chart.pdf
     control_name = ['kick_level', 'snare_level', 'lo_tom_level', 'hi_tom_level', 'closed_hat_level', 'open_hat_level', 'clap_level', 'claves_level', 'agogo_level', 'crash_level',
                     'clap_speed', 'claves_speed', 'agogo_speed', 'crash_speed', 'stutter_time', 'stutter_depth', 'tom_decay', 'closed_hat_decay', 'open_hat_decay', 'hat_gra    in']
     control_code = [40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59]
     note_name = ['kick', 'snare', 'lo_tom', 'hi_tom', 'closed_hat', 'open_hat', 'clap']
     note_code = [36, 38, 43, 50, 42, 46, 39]
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
 
     # this is only for debugging, check which MIDI devices are accessible
     monitor.info('------ OUTPUT ------')
     for port in mido.get_output_names():
         monitor.info(port)
     monitor.info('-------------------------')
 
+    # get the options from the configuration file
     midichannel = patch.getint('midi', 'channel') - 1  # channel 1-16 get mapped to 0-15
     mididevice = patch.getstring('midi', 'device')
     mididevice = EEGsynth.trimquotes(mididevice)
     mididevice = process.extractOne(mididevice, mido.get_output_names())[0]  # select the closest match
 
     try:
         outputport = mido.open_output(mididevice)
@@ -152,17 +135,17 @@
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     # each of the notes that can be played is mapped onto a different trigger
     trigger = []
     for name, code in zip(note_name, note_code):
-        if config.has_option('note', name):
+        if patch.config.has_option('note', name):
             # start the background thread that deals with this note
-            this = TriggerThread(patch.getstring('note', name), code)
+            this = TriggerThread(patch.get('note', name), code)
             trigger.append(this)
             monitor.debug(name + ' trigger configured')
 
     # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
@@ -176,16 +159,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
     global cmd, val, msg
 
     for name, cmd in zip(control_name, control_code):
         # loop over the control values
         val = patch.getfloat('control', name)
         if val == None:
             continue  # it should be skipped when not present
@@ -197,42 +180,38 @@
         val = EEGsynth.limit(val, 0, 127)
         val = int(val)
         msg = mido.Message('control_change', control=cmd, value=val, channel=midichannel)
         monitor.debug(cmd, val, name)
         with lock:
             outputport.send(msg)
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('VOLCABEATS_UNBLOCK', 1)
+    patch.publish('VOLCABEATS_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/volcakeys/__init__.py` & `eegsynth-0.7.0/module/clockdivider/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import sys
 import time
 
-from .volcakeys import _setup, _start, _loop_once, _loop_forever, _stop
+from .clockdivider import _setup, _start, _loop_once, _loop_forever, _stop
 
 class Executable:
     def __init__(self, args=None):
         if args!=None:
             # override the command line arguments
             sys.argv = [sys.argv[0]] + args
 
@@ -18,7 +18,10 @@
                 _start()
                 _loop_forever()
             except RuntimeError:
                 # restart after one second
                 time.sleep(1)
             except KeyboardInterrupt:
                 raise SystemExit
+
+    def __del__(self):
+        _stop()
```

### Comparing `eegsynth-0.6.0/module/volcakeys/volcakeys.py` & `eegsynth-0.7.0/module/volcabass/volcabass.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python
 
-# Volcakeys outputs Redis data via MIDI to the Korg Volca Keys synthesizer
+# Volcabass outputs Redis data via MIDI to the Korg Volca Bass synthesizer
 #
 # This software is part of the EEGsynth project, see <https://github.com/eegsynth/eegsynth>.
 #
 # Copyright (C) 2017-2022 EEGsynth project
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
@@ -15,27 +15,24 @@
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
-import configparser
-import argparse
 import mido
 from fuzzywuzzy import process
 import os
-import redis
 import sys
 import threading
 import time
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__ == '__main__':
     path = os.path.abspath('')
@@ -58,17 +55,16 @@
         self.note = note
         self.running = True
 
     def stop(self):
         self.running = False
 
     def run(self):
-        global monitor, scale, offset
-        pubsub = r.pubsub()
-        pubsub.subscribe('VOLCAKEYS_UNBLOCK')  # this message unblocks the redis listen command
+        pubsub = patch.pubsub()
+        pubsub.subscribe('VOLCABASS_UNBLOCK')  # this message unblocks the redis listen command
         pubsub.subscribe(self.redischannel)    # this message contains the note
         while self.running:
             for item in pubsub.listen():
                 if not self.running or not item['type'] == 'message':
                     break
                 if item['channel'] == self.redischannel:
                     monitor.trace(item)
@@ -82,66 +78,51 @@
                         outputport.send(msg)
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
+    global patch, name, path, monitor
 
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
 
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
-
-    # the list of MIDI commands is the only aspect that is specific to the Volca Keys
-    # see http://media.aadl.org/files/catalog_guides/1444140_chart.pdf
-    control_name = ['portamento', 'expression', 'voice', 'octave', 'detune', 'vco_eg_int', 'vcf_cutoff', 'vcf_eg_int', 'lfo_rate',
-                    'lfo_pitch_int', 'lfo_cutoff_int', 'eg_attack', 'eg_decay_release', 'eg_sustain', 'delay_time', 'delay_feedback']
-    control_code = [5, 11, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53]
+    # the list of MIDI commands is the only aspect that is specific to the Volca Bass
+    # see http://media.aadl.org/files/catalog_guides/1444141_chart.pdf
+    control_name = ['slide_time', 'expression', 'octave', 'lfo_rate', 'lfo_int', 'vco_pitch1',
+                    'vco_pitch2', 'vco_pitch3', 'attack', 'decay_release', 'cutoff_intensity', 'gate_time']
+    control_code = [5, 11, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49]
     note_name = ['C0', 'Db0', 'D0', 'Eb0', 'E0', 'F0', 'Gb0', 'G0', 'Ab0', 'A0', 'Bb0', 'B0', 'C1', 'Db1', 'D1', 'Eb1', 'E1', 'F1', 'Gb1', 'G1', 'Ab1', 'A1', 'Bb1', 'B1', 'C2', 'Db2', 'D2', 'Eb2', 'E2', 'F2', 'Gb2', 'G2', 'Ab2', 'A2', 'Bb2', 'B2', 'C3', 'Db3', 'D3', 'Eb3', 'E3', 'F3', 'Gb3', 'G3', 'Ab3', 'A3', 'Bb3', 'B3', 'C4', 'Db4', 'D4', 'Eb4', 'E4', 'F4', 'Gb4', 'G4', 'Ab4', 'A4', 'Bb4', 'B4', 'C5', 'Db5', 'D5', 'Eb5', 'E5', 'F5',
                  'Gb5', 'G5', 'Ab5', 'A5', 'Bb5', 'B5', 'C6', 'Db6', 'D6', 'Eb6', 'E6', 'F6', 'Gb6', 'G6', 'Ab6', 'A6', 'Bb6', 'B6', 'C7', 'Db7', 'D7', 'Eb7', 'E7', 'F7', 'Gb7', 'G7', 'Ab7', 'A7', 'Bb7', 'B7', 'C8', 'Db8', 'D8', 'Eb8', 'E8', 'F8', 'Gb8', 'G8', 'Ab8', 'A8', 'Bb8', 'B8', 'C9', 'Db9', 'D9', 'Eb9', 'E9', 'F9', 'Gb9', 'G9', 'Ab9', 'A9', 'Bb9', 'B9', 'C10', 'Db10', 'D10', 'Eb10', 'E10', 'F10', 'Gb10', 'G10', 'Ab10', 'A10', 'Bb10', 'B10']
     note_code = [12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81,
                  82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143]
 
-    # get the options from the configuration file
-    debug = patch.getint('general', 'debug')
-
     # this is only for debugging, check which MIDI devices are accessible
     monitor.info('------ OUTPUT ------')
     for port in mido.get_output_names():
         monitor.info(port)
     monitor.info('-------------------------')
 
+    # get the options from the configuration file
     midichannel = patch.getint('midi', 'channel') - 1  # channel 1-16 get mapped to 0-15
     mididevice = patch.getstring('midi', 'device')
     mididevice = EEGsynth.trimquotes(mididevice)
     mididevice = process.extractOne(mididevice, mido.get_output_names())[0]  # select the closest match
 
     try:
         outputport = mido.open_output(mididevice)
@@ -155,17 +136,17 @@
 
     # this is to prevent two messages from being sent at the same time
     lock = threading.Lock()
 
     # each of the notes that can be played is mapped onto a different trigger
     trigger = []
     for name, code in zip(note_name, note_code):
-        if config.has_option('note', name):
+        if patch.config.has_option('note', name):
             # start the background thread that deals with this note
-            this = TriggerThread(patch.getstring('note', name), code)
+            this = TriggerThread(patch.get('note', name), code)
             trigger.append(this)
             monitor.debug(name + ' trigger configured')
 
     # start the thread for each of the notes
     for thread in trigger:
         thread.start()
 
@@ -179,16 +160,16 @@
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
     This uses the global variables from setup and start, and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
-    global monitor, control_name, control_code, note_name, note_code, debug, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
+    global patch, name, path, monitor
+    global control_name, control_code, note_name, note_code, port, midichannel, mididevice, outputport, scale, offset, lock, trigger, code, this, thread, previous_val
     global cmd, val, msg
 
     for name, cmd in zip(control_name, control_code):
         # loop over the control values
         val = patch.getfloat('control', name)
         if val == None:
             continue  # it should be skipped when not present
@@ -200,42 +181,38 @@
         val = EEGsynth.limit(val, 0, 127)
         val = int(val)
         msg = mido.Message('control_change', control=cmd, value=val, channel=midichannel)
         monitor.debug(cmd, val, name)
         with lock:
             outputport.send(msg)
 
-    # there should not be any local variables in this function, they should all be global
-    if len(locals()):
-        print('LOCALS: ' + ', '.join(locals().keys()))
-
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     global monitor, patch
     while True:
         monitor.loop()
         _loop_once()
         time.sleep(patch.getfloat('general', 'delay'))
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     global monitor, trigger, r
     monitor.success('Closing threads')
     for thread in trigger:
         thread.stop()
-    r.publish('VOLCAKEYS_UNBLOCK', 1)
+    patch.publish('VOLCABASS_UNBLOCK', 1)
     for thread in trigger:
         thread.join()
-    sys.exit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
     try:
         _loop_forever()
     except (SystemExit, KeyboardInterrupt, RuntimeError):
         _stop()
+    sys.exit()
```

### Comparing `eegsynth-0.6.0/module/vumeter/vumeter.py` & `eegsynth-0.7.0/module/vumeter/vumeter.py`

 * *Files 8% similar despite different names*

```diff
@@ -17,26 +17,23 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 
 from PyQt5 import QtGui, QtCore, QtWidgets
 from PyQt5.QtWidgets import QApplication, QWidget
-import configparser
-import redis
-import argparse
 import os
 import sys
 import time
 import signal
 import numpy as np
 
 if hasattr(sys, 'frozen'):
     path = os.path.split(sys.executable)[0]
-    file = os.path.split(sys.executable)[-1]
+    file = os.path.split(__file__)[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__' and sys.argv[0] != '':
     path = os.path.split(sys.argv[0])[0]
     file = os.path.split(sys.argv[0])[-1]
     name = os.path.splitext(file)[0]
 elif __name__=='__main__':
     path = os.path.abspath('')
@@ -83,100 +80,89 @@
 
         for name in input_name:
             scale = patch.getfloat('scale', name, default=1)
             offset = patch.getfloat('offset', name, default=0)
             val = patch.getfloat('input', name, default=np.nan)
             val = EEGsynth.rescale(val, slope=scale, offset=offset)
 
-            monitor.update(name, val)
+            monitor.update(name, val, level='debug')
 
             threshold = patch.getfloat('threshold', name, default=1)
             threshold = EEGsynth.rescale(threshold, slope=scale, offset=offset)
 
             if val>=0 and val<=threshold:
                 qp.setBrush(green)
                 qp.setPen(green)
             else:
                 qp.setBrush(red)
                 qp.setPen(red)
 
             if not np.isnan(val):
                 val = EEGsynth.limit(val, 0, 1)
-                r = QtCore.QRect(x, pady + (1-val)*bary, barx, val*bary)
+                r = QtCore.QRect(int(x), int(pady + (1-val)*bary), int(barx), int(val*bary))
                 qp.drawRect(r)
 
-            r = QtCore.QRect(x, pady, barx, bary)
+            r = QtCore.QRect(int(x), int(pady), int(barx), int(bary))
             qp.setPen(QtGui.QColor('white'))
             qp.drawText(r, QtCore.Qt.AlignCenter | QtCore.Qt.AlignBottom, name)
 
             # update the position for the next bar
             x += 2*padx + barx
 
         # add horizontal lines every 10%
         for i in range(1,10):
             qp.setPen(QtGui.QColor('black'))
             y = h - pady - float(i)/10 * bary
-            qp.drawLine(0, y, w, y)
+            qp.drawLine(0, int(y), int(w), int(y))
 
         qp.end()
         self.show()
 
 
 def _setup():
     '''Initialize the module
     This adds a set of global variables
     '''
-    global parser, args, config, r, response, patch
+    global patch, name, path, monitor
 
-    parser = argparse.ArgumentParser()
-    parser.add_argument("-i", "--inifile", default=os.path.join(path, name + '.ini'), help="name of the configuration file")
-    args = parser.parse_args()
-
-    config = configparser.ConfigParser(inline_comment_prefixes=('#', ';'))
-    config.read(args.inifile)
-
-    try:
-        r = redis.StrictRedis(host=config.get('redis', 'hostname'), port=config.getint('redis', 'port'), db=0, charset='utf-8', decode_responses=True)
-        response = r.client_list()
-    except redis.ConnectionError:
-        raise RuntimeError("cannot connect to Redis server")
+    # configure and start the patch, this will parse the command-line arguments and the ini file
+    patch = EEGsynth.patch(name=name, path=path)
 
-    # combine the patching from the configuration file and Redis
-    patch = EEGsynth.patch(config, r)
+    # this shows the splash screen and can be used to track parameters that have changed
+    monitor = EEGsynth.monitor(name=name, patch=patch, debug=patch.getint('general', 'debug', default=1), target=patch.get('general', 'logging', default=None))
 
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _start():
     '''Start the module
     This uses the global variables from setup and adds a set of global variables
     '''
-    global parser, args, config, r, response, patch, name
-    global monitor, delay, winx, winy, winwidth, winheight, input_name, input_variable, variable, app, window, timer
-
-    # this can be used to show parameters that have changed
-    monitor = EEGsynth.monitor(name=name, debug=patch.getint('general', 'debug'))
+    global patch, name, path, monitor
+    global delay, winx, winy, winwidth, winheight, input_name, input_variable, variable, app, window, timer
 
     # get the options from the configuration file
     delay           = patch.getfloat('general', 'delay')
-    winx            = patch.getfloat('display', 'xpos')
-    winy            = patch.getfloat('display', 'ypos')
-    winwidth        = patch.getfloat('display', 'width')
-    winheight       = patch.getfloat('display', 'height')
+    winx            = patch.getint('display', 'xpos')
+    winy            = patch.getint('display', 'ypos')
+    winwidth        = patch.getint('display', 'width')
+    winheight       = patch.getint('display', 'height')
 
     # get the input options
-    input_name, input_variable = list(zip(*config.items('input')))
+    input_name, input_variable = list(zip(*patch.config.items('input')))
 
     for name,variable in zip(input_name, input_variable):
         monitor.info("%s = %s" % (name, variable))
 
     # start the graphical user interface
     app = QApplication(sys.argv)
+    app.setWindowIcon(QtGui.QIcon(os.path.join(path, '../../doc/figures/logo-128.ico')))
+    app.aboutToQuit.connect(_stop)
     signal.signal(signal.SIGINT, _stop)
 
     window = Window()
     window.show()
 
     # Set timer for update
     timer = QtCore.QTimer()
@@ -187,29 +173,28 @@
     # there should not be any local variables in this function, they should all be global
     if len(locals()):
         print('LOCALS: ' + ', '.join(locals().keys()))
 
 
 def _loop_once():
     '''Run the main loop once
-    This uses the global variables from setup and start, and adds a set of global variables
     '''
     global monitor, window
     monitor.loop()
     window.update()
 
 
 def _loop_forever():
     '''Run the main loop forever
     '''
     QApplication.instance().exec_()
 
 
 def _stop(*args):
-    '''Stop and clean up on SystemExit, KeyboardInterrupt
+    '''Stop and clean up on SystemExit, KeyboardInterrupt, RuntimeError
     '''
     QApplication.quit()
 
 
 if __name__ == '__main__':
     _setup()
     _start()
```

### Comparing `eegsynth-0.6.0/setup.py` & `eegsynth-0.7.0/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 #!/usr/bin/env python
 
 import setuptools
+from version import __version__
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 # update the local links, so that the documentation on PyPi points to Github
 long_description = long_description.replace(
     "](bin",      "](https://github.com/eegsynth/eegsynth/raw/master/bin")
@@ -20,15 +21,15 @@
     "](patches",  "](https://github.com/eegsynth/eegsynth/raw/master/patches")
 
 # The organization of the Python code is non-standard, hence a custom
 # package_dir and packages specification is needed.
 
 setuptools.setup(
     name="eegsynth",
-    version="0.6.0",
+    version=__version__,
     description="Converting real-time EEG into sounds, music and visual effects",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="http://www.eegsynth.org",
     author="Robert Oostenveld",
     author_email="r.oostenveld@gmail.com",
     license="GPLv3",
@@ -63,39 +64,41 @@
         "Documentation": "https://github.com/eegsynth/eegsynth/blob/master/doc/README.md",
         "Source": "https://github.com/eegsynth/eegsynth/",
         "Tracker": "https://github.com/eegsynth/eegsynth/issues",
     },
     package_dir={"eegsynth": ".", "eegsynth.bin": "bin", "eegsynth.lib": "lib", "eegsynth.module": "module"},
     packages=["eegsynth"] + ["eegsynth." + s for s in setuptools.find_packages(".")],
     install_requires=[
+        "bleak",
         "bitalino",
         "colorama",
         "configparser",
         "fuzzywuzzy[speedup]",
         "matplotlib",
         "mido",
-        "mido",
         "nilearn",
         "numpy",
+        "opencv-python",
         "paho-mqtt",
         "pyaudio",
         "pylsl",
-        "pyqtgraph",
+        "pyqtgraph==0.11",
         "pyserial",
+        "pyzmq",
         "redis",
         "scipy",
         "sklearn",
         "termcolor",
-        "pyzmq",
+        "wiringpi; platform_machine == 'armv7l'"
     ],
     python_requires=">=2.7",
     extras_require={
         ":python_version<'3.5'": ["pyOSC"],
         ":python_version>='3.5'": ["python-rtmidi"],
         ":python_version>='3.5'": ["python-osc"]
     },
     entry_points={
         'console_scripts': [
-            'eegsynth = eegsynth.bin.eegsynth:_main',
+            'eegsynth = eegsynth.eegsynth:_main',
         ],
     },
 )
```

