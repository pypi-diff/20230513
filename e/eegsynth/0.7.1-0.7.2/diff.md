# Comparing `tmp/eegsynth-0.7.1.tar.gz` & `tmp/eegsynth-0.7.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eegsynth-0.7.1.tar", last modified: Sat May 13 09:16:51 2023, max compression
+gzip compressed data, was "eegsynth-0.7.2.tar", last modified: Sat May 13 13:05:59 2023, max compression
```

## Comparing `eegsynth-0.7.1.tar` & `eegsynth-0.7.2.tar`

### file list

```diff
@@ -1,268 +1,268 @@
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.405166 eegsynth-0.7.1/
--rw-r--r--   0 roboos     (503) staff       (20)    32472 2023-03-21 19:58:52.000000 eegsynth-0.7.1/LICENSE
--rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 09:16:51.404764 eegsynth-0.7.1/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     2698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/README.md
--rwxr-xr-x   0 roboos     (503) staff       (20)    16510 2023-05-13 08:17:47.000000 eegsynth-0.7.1/eegsynth-gui.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.212491 eegsynth-0.7.1/eegsynth.egg-info/
--rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 09:16:50.000000 eegsynth-0.7.1/eegsynth.egg-info/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     5482 2023-05-13 09:16:51.000000 eegsynth-0.7.1/eegsynth.egg-info/SOURCES.txt
--rw-r--r--   0 roboos     (503) staff       (20)        1 2023-05-13 09:16:50.000000 eegsynth-0.7.1/eegsynth.egg-info/dependency_links.txt
--rw-r--r--   0 roboos     (503) staff       (20)       53 2023-05-13 09:16:50.000000 eegsynth-0.7.1/eegsynth.egg-info/entry_points.txt
--rw-r--r--   0 roboos     (503) staff       (20)      296 2023-05-13 09:16:50.000000 eegsynth-0.7.1/eegsynth.egg-info/requires.txt
--rw-r--r--   0 roboos     (503) staff       (20)        9 2023-05-13 09:16:50.000000 eegsynth-0.7.1/eegsynth.egg-info/top_level.txt
--rwxr-xr-x   0 roboos     (503) staff       (20)    13425 2023-05-13 09:13:24.000000 eegsynth-0.7.1/eegsynth.py
--rw-r--r--   0 roboos     (503) staff       (20)     1388 2023-05-04 12:16:58.000000 eegsynth-0.7.1/hook-pylsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.222717 eegsynth-0.7.1/lib/
--rw-r--r--   0 roboos     (503) staff       (20)     1656 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/ArtNet.py
--rw-r--r--   0 roboos     (503) staff       (20)     1450 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/DummyRedis.py
--rw-r--r--   0 roboos     (503) staff       (20)    17162 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/EDF.py
--rw-r--r--   0 roboos     (503) staff       (20)    35670 2023-05-02 20:55:48.000000 eegsynth-0.7.1/lib/EEGsynth.py
--rw-r--r--   0 roboos     (503) staff       (20)     1975 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/FakeRedis.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    27618 2023-04-30 19:35:59.000000 eegsynth-0.7.1/lib/FieldTrip.py
--rw-r--r--   0 roboos     (503) staff       (20)      435 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/FieldTrip_test_client.py
--rw-r--r--   0 roboos     (503) staff       (20)      301 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/FieldTrip_test_server.py
--rw-r--r--   0 roboos     (503) staff       (20)     1131 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/Redis_test_client.py
--rw-r--r--   0 roboos     (503) staff       (20)     2193 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/RingBuffer.py
--rw-r--r--   0 roboos     (503) staff       (20)     7184 2023-05-02 18:05:03.000000 eegsynth-0.7.1/lib/ZmqRedis.py
--rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/__init__.py
--rw-r--r--   0 roboos     (503) staff       (20)    59022 2023-03-21 19:58:52.000000 eegsynth-0.7.1/lib/colormap.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.223820 eegsynth-0.7.1/module/
--rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/__init__.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.224962 eegsynth-0.7.1/module/accelerometer/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/accelerometer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5707 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/accelerometer/accelerometer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.226345 eegsynth-0.7.1/module/audio2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/audio2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6708 2023-04-29 08:49:58.000000 eegsynth-0.7.1/module/audio2ft/audio2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.227755 eegsynth-0.7.1/module/audiomixer/
--rwxr-xr-x   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/audiomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7220 2023-04-29 09:10:40.000000 eegsynth-0.7.1/module/audiomixer/audiomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.229273 eegsynth-0.7.1/module/bitalino2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/bitalino2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6396 2023-04-29 09:15:26.000000 eegsynth-0.7.1/module/bitalino2ft/bitalino2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.230753 eegsynth-0.7.1/module/brainflow2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/brainflow2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6322 2023-04-29 08:15:56.000000 eegsynth-0.7.1/module/brainflow2ft/brainflow2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.232059 eegsynth-0.7.1/module/buffer/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/buffer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     3468 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/buffer/buffer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.233574 eegsynth-0.7.1/module/clockdivider/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/clockdivider/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5433 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/clockdivider/clockdivider.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.235099 eegsynth-0.7.1/module/clockmultiplier/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/clockmultiplier/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7267 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/clockmultiplier/clockmultiplier.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.237482 eegsynth-0.7.1/module/cogito/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/cogito/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12302 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/cogito/cogito.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/cogito/gtec2wav.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.238516 eegsynth-0.7.1/module/complexity/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/complexity/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8635 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/complexity/complexity.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.239876 eegsynth-0.7.1/module/compressor/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/compressor/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5131 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/compressor/compressor.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.241879 eegsynth-0.7.1/module/csp/
--rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/csp/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12865 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/csp/csp.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.244262 eegsynth-0.7.1/module/delaytrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/delaytrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5784 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/delaytrigger/delaytrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.246469 eegsynth-0.7.1/module/demodulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/demodulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9517 2023-04-29 09:15:47.000000 eegsynth-0.7.1/module/demodulatetone/demodulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.249280 eegsynth-0.7.1/module/endorphines/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/endorphines/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9952 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/endorphines/endorphines.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.250665 eegsynth-0.7.1/module/example/
--rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/example/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4008 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/example/example.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.252155 eegsynth-0.7.1/module/generateclock/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/generateclock/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12009 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/generateclock/generateclock.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.253521 eegsynth-0.7.1/module/generatecontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/generatecontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8392 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/generatecontrol/generatecontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.254822 eegsynth-0.7.1/module/generatesignal/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/generatesignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10722 2023-05-02 20:11:22.000000 eegsynth-0.7.1/module/generatesignal/generatesignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.256459 eegsynth-0.7.1/module/generatetrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/generatetrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6763 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/generatetrigger/generatetrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.258982 eegsynth-0.7.1/module/geomixer/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/geomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8648 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/geomixer/geomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.265897 eegsynth-0.7.1/module/heartrate/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/heartrate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8413 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/heartrate/heartrate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.270585 eegsynth-0.7.1/module/historycontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/historycontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9494 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/historycontrol/historycontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.272803 eegsynth-0.7.1/module/historysignal/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/historysignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9401 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/historysignal/historysignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.274751 eegsynth-0.7.1/module/inputcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    17279 2023-05-10 07:50:04.000000 eegsynth-0.7.1/module/inputcontrol/inputcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.277067 eegsynth-0.7.1/module/inputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6618 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/inputlsl/inputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.280647 eegsynth-0.7.1/module/inputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5264 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/inputmidi/inputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.283436 eegsynth-0.7.1/module/inputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5957 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/inputmqtt/inputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.285594 eegsynth-0.7.1/module/inputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/inputosc/inputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.288536 eegsynth-0.7.1/module/inputzeromq/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/inputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5740 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/inputzeromq/inputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.293332 eegsynth-0.7.1/module/keyboard/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/keyboard/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14634 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/keyboard/keyboard.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.295225 eegsynth-0.7.1/module/launchcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/launchcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13953 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/launchcontrol/launchcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.296872 eegsynth-0.7.1/module/launchpad/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/launchpad/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14601 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/launchpad/launchpad.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.298506 eegsynth-0.7.1/module/logging/
--rw-r--r--   0 roboos     (503) staff       (20)      422 2023-04-30 07:48:46.000000 eegsynth-0.7.1/module/logging/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7275 2023-04-30 20:43:41.000000 eegsynth-0.7.1/module/logging/logging.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.300197 eegsynth-0.7.1/module/lsl2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/lsl2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6768 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/lsl2ft/lsl2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.302991 eegsynth-0.7.1/module/modulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/modulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10550 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/modulatetone/modulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.306479 eegsynth-0.7.1/module/outputartnet/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputartnet/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6639 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputartnet/outputartnet.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.309090 eegsynth-0.7.1/module/outputaudio/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputaudio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12350 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputaudio/outputaudio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.312106 eegsynth-0.7.1/module/outputcvgate/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputcvgate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10263 2023-05-07 13:53:03.000000 eegsynth-0.7.1/module/outputcvgate/outputcvgate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.314250 eegsynth-0.7.1/module/outputdmx/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputdmx/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6984 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputdmx/outputdmx.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.315638 eegsynth-0.7.1/module/outputgpio/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputgpio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8490 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputgpio/outputgpio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.317113 eegsynth-0.7.1/module/outputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7652 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputlsl/outputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.318374 eegsynth-0.7.1/module/outputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13389 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputmidi/outputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.319906 eegsynth-0.7.1/module/outputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7263 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputmqtt/outputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.321438 eegsynth-0.7.1/module/outputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7596 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputosc/outputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.324968 eegsynth-0.7.1/module/outputzeromq/
--rwxr-xr-x   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/outputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6590 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/outputzeromq/outputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.326943 eegsynth-0.7.1/module/pepipiaf/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/pepipiaf/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    25727 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/pepipiaf/pepipiaf.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.332003 eegsynth-0.7.1/module/playbackcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/playbackcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6454 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/playbackcontrol/playbackcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.335797 eegsynth-0.7.1/module/playbacksignal/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/playbacksignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9858 2023-05-02 20:53:32.000000 eegsynth-0.7.1/module/playbacksignal/playbacksignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.337534 eegsynth-0.7.1/module/plotcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/plotcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7058 2023-04-30 20:43:43.000000 eegsynth-0.7.1/module/plotcontrol/plotcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.339223 eegsynth-0.7.1/module/plotimage/
--rw-r--r--   0 roboos     (503) staff       (20)      424 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/plotimage/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6780 2023-04-30 20:43:48.000000 eegsynth-0.7.1/module/plotimage/plotimage.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.341935 eegsynth-0.7.1/module/plotsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      425 2023-04-30 19:40:07.000000 eegsynth-0.7.1/module/plotsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11992 2023-04-30 20:43:51.000000 eegsynth-0.7.1/module/plotsignal/plotsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.346409 eegsynth-0.7.1/module/plotspectral/
--rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/plotspectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    23337 2023-04-30 20:43:55.000000 eegsynth-0.7.1/module/plotspectral/plotspectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.347948 eegsynth-0.7.1/module/plottext/
--rw-r--r--   0 roboos     (503) staff       (20)      423 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/plottext/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7894 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/plottext/plottext.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.349688 eegsynth-0.7.1/module/plottopo/
--rw-r--r--   0 roboos     (503) staff       (20)      423 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/plottopo/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8637 2023-04-30 20:44:05.000000 eegsynth-0.7.1/module/plottopo/plottopo.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.351737 eegsynth-0.7.1/module/plottrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/plottrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8295 2023-04-30 20:44:08.000000 eegsynth-0.7.1/module/plottrigger/plottrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.353975 eegsynth-0.7.1/module/postprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/postprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6740 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/postprocessing/postprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.356169 eegsynth-0.7.1/module/preprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/preprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14798 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/preprocessing/preprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.359466 eegsynth-0.7.1/module/processtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/processtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9670 2023-05-02 19:32:40.000000 eegsynth-0.7.1/module/processtrigger/processtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.363908 eegsynth-0.7.1/module/quantizer/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/quantizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6181 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/quantizer/quantizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.368107 eegsynth-0.7.1/module/recordcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      701 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/recordcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10121 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/recordcontrol/recordcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.369648 eegsynth-0.7.1/module/recordsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/recordsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11451 2023-05-02 20:50:47.000000 eegsynth-0.7.1/module/recordsignal/recordsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.371213 eegsynth-0.7.1/module/recordtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/recordtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8005 2023-05-13 08:01:31.000000 eegsynth-0.7.1/module/recordtrigger/recordtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.372970 eegsynth-0.7.1/module/redis/
--rw-r--r--   0 roboos     (503) staff       (20)      683 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/redis/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     3599 2023-04-30 20:46:28.000000 eegsynth-0.7.1/module/redis/redis.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.374822 eegsynth-0.7.1/module/rms/
--rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/rms/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6500 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/rms/rms.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.379560 eegsynth-0.7.1/module/sampler/
--rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/sampler/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14409 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/sampler/sampler.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.383756 eegsynth-0.7.1/module/sequencer/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/sequencer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10356 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/sequencer/sequencer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.385909 eegsynth-0.7.1/module/slewlimiter/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/slewlimiter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4470 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/slewlimiter/slewlimiter.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.388170 eegsynth-0.7.1/module/sonification/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/sonification/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15140 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/sonification/sonification.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.389959 eegsynth-0.7.1/module/spectral/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/spectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7528 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/spectral/spectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.391802 eegsynth-0.7.1/module/synthesizer/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/synthesizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15026 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/synthesizer/synthesizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.394495 eegsynth-0.7.1/module/threshold/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/threshold/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7690 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/threshold/threshold.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.396261 eegsynth-0.7.1/module/unicorn2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/unicorn2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7588 2023-05-07 13:53:03.000000 eegsynth-0.7.1/module/unicorn2ft/unicorn2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.397686 eegsynth-0.7.1/module/videoprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-25 11:03:23.000000 eegsynth-0.7.1/module/videoprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    17749 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/videoprocessing/videoprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.398942 eegsynth-0.7.1/module/volcabass/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/volcabass/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9541 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/volcabass/volcabass.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.400369 eegsynth-0.7.1/module/volcabeats/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/volcabeats/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8370 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/volcabeats/volcabeats.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.401883 eegsynth-0.7.1/module/volcakeys/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/volcakeys/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9657 2023-04-30 15:10:12.000000 eegsynth-0.7.1/module/volcakeys/volcakeys.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 09:16:51.403691 eegsynth-0.7.1/module/vumeter/
--rw-r--r--   0 roboos     (503) staff       (20)      422 2023-03-21 19:58:52.000000 eegsynth-0.7.1/module/vumeter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6651 2023-04-30 20:44:11.000000 eegsynth-0.7.1/module/vumeter/vumeter.py
--rw-r--r--   0 roboos     (503) staff       (20)       38 2023-05-13 09:16:51.405296 eegsynth-0.7.1/setup.cfg
--rwxr-xr-x   0 roboos     (503) staff       (20)     3551 2023-05-13 09:15:27.000000 eegsynth-0.7.1/setup.py
--rw-r--r--   0 roboos     (503) staff       (20)       20 2023-05-13 08:19:44.000000 eegsynth-0.7.1/version.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.393834 eegsynth-0.7.2/
+-rw-r--r--   0 roboos     (503) staff       (20)    32472 2023-03-21 19:58:52.000000 eegsynth-0.7.2/LICENSE
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:05:59.393522 eegsynth-0.7.2/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     2698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/README.md
+-rwxr-xr-x   0 roboos     (503) staff       (20)    16538 2023-05-13 13:04:47.000000 eegsynth-0.7.2/eegsynth-gui.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.233022 eegsynth-0.7.2/eegsynth.egg-info/
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     5482 2023-05-13 13:05:59.000000 eegsynth-0.7.2/eegsynth.egg-info/SOURCES.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        1 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/dependency_links.txt
+-rw-r--r--   0 roboos     (503) staff       (20)       53 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/entry_points.txt
+-rw-r--r--   0 roboos     (503) staff       (20)      296 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/requires.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        9 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/top_level.txt
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13455 2023-05-13 13:03:24.000000 eegsynth-0.7.2/eegsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1388 2023-05-04 12:16:58.000000 eegsynth-0.7.2/hook-pylsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.240373 eegsynth-0.7.2/lib/
+-rw-r--r--   0 roboos     (503) staff       (20)     1656 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/ArtNet.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1450 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/DummyRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)    17162 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/EDF.py
+-rw-r--r--   0 roboos     (503) staff       (20)    35670 2023-05-02 20:55:48.000000 eegsynth-0.7.2/lib/EEGsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1975 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FakeRedis.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    27618 2023-04-30 19:35:59.000000 eegsynth-0.7.2/lib/FieldTrip.py
+-rw-r--r--   0 roboos     (503) staff       (20)      435 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FieldTrip_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)      301 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FieldTrip_test_server.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1131 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/Redis_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)     2193 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/RingBuffer.py
+-rw-r--r--   0 roboos     (503) staff       (20)     7184 2023-05-02 18:05:03.000000 eegsynth-0.7.2/lib/ZmqRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/__init__.py
+-rw-r--r--   0 roboos     (503) staff       (20)    59022 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/colormap.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.241599 eegsynth-0.7.2/module/
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/__init__.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.242744 eegsynth-0.7.2/module/accelerometer/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/accelerometer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5707 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/accelerometer/accelerometer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.244205 eegsynth-0.7.2/module/audio2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/audio2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6708 2023-04-29 08:49:58.000000 eegsynth-0.7.2/module/audio2ft/audio2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.245873 eegsynth-0.7.2/module/audiomixer/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/audiomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7220 2023-04-29 09:10:40.000000 eegsynth-0.7.2/module/audiomixer/audiomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.247534 eegsynth-0.7.2/module/bitalino2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/bitalino2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6396 2023-04-29 09:15:26.000000 eegsynth-0.7.2/module/bitalino2ft/bitalino2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.248989 eegsynth-0.7.2/module/brainflow2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/brainflow2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6322 2023-04-29 08:15:56.000000 eegsynth-0.7.2/module/brainflow2ft/brainflow2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.250591 eegsynth-0.7.2/module/buffer/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/buffer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3468 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/buffer/buffer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.252394 eegsynth-0.7.2/module/clockdivider/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/clockdivider/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5433 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/clockdivider/clockdivider.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.254085 eegsynth-0.7.2/module/clockmultiplier/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/clockmultiplier/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7267 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/clockmultiplier/clockmultiplier.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.257167 eegsynth-0.7.2/module/cogito/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/cogito/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12302 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/cogito/cogito.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/cogito/gtec2wav.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.259064 eegsynth-0.7.2/module/complexity/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/complexity/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8635 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/complexity/complexity.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.260953 eegsynth-0.7.2/module/compressor/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/compressor/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5131 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/compressor/compressor.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.263056 eegsynth-0.7.2/module/csp/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/csp/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12865 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/csp/csp.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.264906 eegsynth-0.7.2/module/delaytrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/delaytrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5784 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/delaytrigger/delaytrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.266834 eegsynth-0.7.2/module/demodulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/demodulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9517 2023-04-29 09:15:47.000000 eegsynth-0.7.2/module/demodulatetone/demodulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.268670 eegsynth-0.7.2/module/endorphines/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/endorphines/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9952 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/endorphines/endorphines.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.273639 eegsynth-0.7.2/module/example/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/example/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4008 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/example/example.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.275848 eegsynth-0.7.2/module/generateclock/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generateclock/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12009 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generateclock/generateclock.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.277526 eegsynth-0.7.2/module/generatecontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatecontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8392 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generatecontrol/generatecontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.279021 eegsynth-0.7.2/module/generatesignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatesignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10722 2023-05-02 20:11:22.000000 eegsynth-0.7.2/module/generatesignal/generatesignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.280641 eegsynth-0.7.2/module/generatetrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatetrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6763 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generatetrigger/generatetrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.282114 eegsynth-0.7.2/module/geomixer/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/geomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8648 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/geomixer/geomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.284002 eegsynth-0.7.2/module/heartrate/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/heartrate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8413 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/heartrate/heartrate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.285870 eegsynth-0.7.2/module/historycontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/historycontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9494 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/historycontrol/historycontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.287827 eegsynth-0.7.2/module/historysignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/historysignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9401 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/historysignal/historysignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.289588 eegsynth-0.7.2/module/inputcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17279 2023-05-10 07:50:04.000000 eegsynth-0.7.2/module/inputcontrol/inputcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.291905 eegsynth-0.7.2/module/inputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6618 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputlsl/inputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.293834 eegsynth-0.7.2/module/inputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5264 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputmidi/inputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.295414 eegsynth-0.7.2/module/inputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5957 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputmqtt/inputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.296812 eegsynth-0.7.2/module/inputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputosc/inputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.298192 eegsynth-0.7.2/module/inputzeromq/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5740 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputzeromq/inputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.299759 eegsynth-0.7.2/module/keyboard/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/keyboard/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14634 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/keyboard/keyboard.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.301272 eegsynth-0.7.2/module/launchcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/launchcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13953 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/launchcontrol/launchcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.302973 eegsynth-0.7.2/module/launchpad/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/launchpad/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14601 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/launchpad/launchpad.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.304802 eegsynth-0.7.2/module/logging/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-04-30 07:48:46.000000 eegsynth-0.7.2/module/logging/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7275 2023-04-30 20:43:41.000000 eegsynth-0.7.2/module/logging/logging.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.306819 eegsynth-0.7.2/module/lsl2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/lsl2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6768 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/lsl2ft/lsl2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.308636 eegsynth-0.7.2/module/modulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/modulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10550 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/modulatetone/modulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.310957 eegsynth-0.7.2/module/outputartnet/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputartnet/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6639 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputartnet/outputartnet.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.313783 eegsynth-0.7.2/module/outputaudio/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputaudio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12350 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputaudio/outputaudio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.317949 eegsynth-0.7.2/module/outputcvgate/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputcvgate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10263 2023-05-07 13:53:03.000000 eegsynth-0.7.2/module/outputcvgate/outputcvgate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.320309 eegsynth-0.7.2/module/outputdmx/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputdmx/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6984 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputdmx/outputdmx.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.325534 eegsynth-0.7.2/module/outputgpio/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputgpio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8490 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputgpio/outputgpio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.327160 eegsynth-0.7.2/module/outputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7652 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputlsl/outputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.329570 eegsynth-0.7.2/module/outputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13389 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputmidi/outputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.331851 eegsynth-0.7.2/module/outputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7263 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputmqtt/outputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.333841 eegsynth-0.7.2/module/outputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7596 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputosc/outputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.335248 eegsynth-0.7.2/module/outputzeromq/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6590 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputzeromq/outputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.336691 eegsynth-0.7.2/module/pepipiaf/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/pepipiaf/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    25727 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/pepipiaf/pepipiaf.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.338423 eegsynth-0.7.2/module/playbackcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/playbackcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6454 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/playbackcontrol/playbackcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.341223 eegsynth-0.7.2/module/playbacksignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/playbacksignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9858 2023-05-02 20:53:32.000000 eegsynth-0.7.2/module/playbacksignal/playbacksignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.343190 eegsynth-0.7.2/module/plotcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7058 2023-04-30 20:43:43.000000 eegsynth-0.7.2/module/plotcontrol/plotcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.345714 eegsynth-0.7.2/module/plotimage/
+-rw-r--r--   0 roboos     (503) staff       (20)      424 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotimage/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6780 2023-04-30 20:43:48.000000 eegsynth-0.7.2/module/plotimage/plotimage.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.348123 eegsynth-0.7.2/module/plotsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      425 2023-04-30 19:40:07.000000 eegsynth-0.7.2/module/plotsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11992 2023-04-30 20:43:51.000000 eegsynth-0.7.2/module/plotsignal/plotsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.349884 eegsynth-0.7.2/module/plotspectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotspectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    23337 2023-04-30 20:43:55.000000 eegsynth-0.7.2/module/plotspectral/plotspectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.352448 eegsynth-0.7.2/module/plottext/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/plottext/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7894 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/plottext/plottext.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.353935 eegsynth-0.7.2/module/plottopo/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plottopo/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8637 2023-04-30 20:44:05.000000 eegsynth-0.7.2/module/plottopo/plottopo.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.355359 eegsynth-0.7.2/module/plottrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plottrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8295 2023-04-30 20:44:08.000000 eegsynth-0.7.2/module/plottrigger/plottrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.357301 eegsynth-0.7.2/module/postprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/postprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6740 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/postprocessing/postprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.359448 eegsynth-0.7.2/module/preprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/preprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14798 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/preprocessing/preprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.361154 eegsynth-0.7.2/module/processtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/processtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9670 2023-05-02 19:32:40.000000 eegsynth-0.7.2/module/processtrigger/processtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.364027 eegsynth-0.7.2/module/quantizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/quantizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6181 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/quantizer/quantizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.365653 eegsynth-0.7.2/module/recordcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      701 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10121 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/recordcontrol/recordcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.367343 eegsynth-0.7.2/module/recordsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11451 2023-05-02 20:50:47.000000 eegsynth-0.7.2/module/recordsignal/recordsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.368889 eegsynth-0.7.2/module/recordtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8005 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/recordtrigger/recordtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.370732 eegsynth-0.7.2/module/redis/
+-rw-r--r--   0 roboos     (503) staff       (20)      683 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/redis/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3599 2023-04-30 20:46:28.000000 eegsynth-0.7.2/module/redis/redis.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.372222 eegsynth-0.7.2/module/rms/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/rms/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6500 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/rms/rms.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.373738 eegsynth-0.7.2/module/sampler/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sampler/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14409 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sampler/sampler.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.375500 eegsynth-0.7.2/module/sequencer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sequencer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10356 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sequencer/sequencer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.376913 eegsynth-0.7.2/module/slewlimiter/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/slewlimiter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4470 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/slewlimiter/slewlimiter.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.378603 eegsynth-0.7.2/module/sonification/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sonification/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15140 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sonification/sonification.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.380185 eegsynth-0.7.2/module/spectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/spectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7528 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/spectral/spectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.382029 eegsynth-0.7.2/module/synthesizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/synthesizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15026 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/synthesizer/synthesizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.383615 eegsynth-0.7.2/module/threshold/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/threshold/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7690 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/threshold/threshold.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.384866 eegsynth-0.7.2/module/unicorn2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/unicorn2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7588 2023-05-07 13:53:03.000000 eegsynth-0.7.2/module/unicorn2ft/unicorn2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.386197 eegsynth-0.7.2/module/videoprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-25 11:03:23.000000 eegsynth-0.7.2/module/videoprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17749 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/videoprocessing/videoprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.388028 eegsynth-0.7.2/module/volcabass/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcabass/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9541 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcabass/volcabass.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.389448 eegsynth-0.7.2/module/volcabeats/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcabeats/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8370 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcabeats/volcabeats.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.391328 eegsynth-0.7.2/module/volcakeys/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcakeys/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9657 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcakeys/volcakeys.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.392674 eegsynth-0.7.2/module/vumeter/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/vumeter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6651 2023-04-30 20:44:11.000000 eegsynth-0.7.2/module/vumeter/vumeter.py
+-rw-r--r--   0 roboos     (503) staff       (20)       38 2023-05-13 13:05:59.393987 eegsynth-0.7.2/setup.cfg
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3551 2023-05-13 09:15:27.000000 eegsynth-0.7.2/setup.py
+-rw-r--r--   0 roboos     (503) staff       (20)       20 2023-05-13 13:03:41.000000 eegsynth-0.7.2/version.py
```

### Comparing `eegsynth-0.7.1/LICENSE` & `eegsynth-0.7.2/LICENSE`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/PKG-INFO` & `eegsynth-0.7.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.7.1
+Version: 0.7.2
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
```

### Comparing `eegsynth-0.7.1/README.md` & `eegsynth-0.7.2/README.md`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/eegsynth-gui.py` & `eegsynth-0.7.2/eegsynth-gui.py`

 * *Files 1% similar despite different names*

```diff
@@ -39,15 +39,15 @@
 sys.path.insert(0, os.path.join(path))
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, 'lib'))
 import EEGsynth
 import FieldTrip
 from version import __version__
 
-from module import accelerometer, audio2ft, audiomixer, biochill, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
+from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
 
 # this will contain a list of modules and processes
 modules = []
 processes = []
 
 # command-line arguments
 args = []
@@ -185,16 +185,17 @@
 
             if name=='accelerometer':
                 module_to_start = accelerometer
             elif name=='audio2ft':
                 module_to_start = audio2ft
             elif name=='audiomixer':
                 module_to_start = audiomixer
-            elif name=='biochill':
-                module_to_start = biochill
+# This does not have an __init__.py
+#            elif name=='biochill':
+#                module_to_start = biochill
             elif name=='bitalino2ft':
                 module_to_start = bitalino2ft
 # This requires the brainflow package, which is not installed by default.
 #            elif name=='brainflow2ft':
 #                module_to_start = brainflow2ft
             elif name=='buffer':
                 module_to_start = buffer
```

### Comparing `eegsynth-0.7.1/eegsynth.egg-info/PKG-INFO` & `eegsynth-0.7.2/eegsynth.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.7.1
+Version: 0.7.2
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
```

### Comparing `eegsynth-0.7.1/eegsynth.egg-info/SOURCES.txt` & `eegsynth-0.7.2/eegsynth.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/eegsynth.py` & `eegsynth-0.7.2/eegsynth.py`

 * *Files 0% similar despite different names*

```diff
@@ -42,15 +42,15 @@
 sys.path.insert(0, os.path.join(path))
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, 'lib'))
 import EEGsynth
 import FieldTrip
 from version import __version__
 
-from module import accelerometer, audio2ft, audiomixer, biochill, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
+from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
 
 # this will contain a list of modules and processes
 modules = []
 processes = []
 
 def _setup():
     global monitor, modules, processes
@@ -115,16 +115,17 @@
 
         if name=='accelerometer':
             module_to_start = accelerometer
         elif name=='audio2ft':
             module_to_start = audio2ft
         elif name=='audiomixer':
             module_to_start = audiomixer
-        elif name=='biochill':
-            module_to_start = biochill
+# This does not have an __init__.py
+#         elif name=='biochill':
+#             module_to_start = biochill
         elif name=='bitalino2ft':
             module_to_start = bitalino2ft
 # This requires the brainflow package, which is not installed by default.
 #            elif name=='brainflow2ft':
 #                module_to_start = brainflow2ft
         elif name=='buffer':
             module_to_start = buffer
```

### Comparing `eegsynth-0.7.1/hook-pylsl.py` & `eegsynth-0.7.2/hook-pylsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/ArtNet.py` & `eegsynth-0.7.2/lib/ArtNet.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/DummyRedis.py` & `eegsynth-0.7.2/lib/DummyRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/EDF.py` & `eegsynth-0.7.2/lib/EDF.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/EEGsynth.py` & `eegsynth-0.7.2/lib/EEGsynth.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/FakeRedis.py` & `eegsynth-0.7.2/lib/FakeRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/FieldTrip.py` & `eegsynth-0.7.2/lib/FieldTrip.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/Redis_test_client.py` & `eegsynth-0.7.2/lib/Redis_test_client.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/RingBuffer.py` & `eegsynth-0.7.2/lib/RingBuffer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/ZmqRedis.py` & `eegsynth-0.7.2/lib/ZmqRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/lib/colormap.py` & `eegsynth-0.7.2/lib/colormap.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/accelerometer/__init__.py` & `eegsynth-0.7.2/module/accelerometer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/accelerometer/accelerometer.py` & `eegsynth-0.7.2/module/accelerometer/accelerometer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/audio2ft/__init__.py` & `eegsynth-0.7.2/module/audio2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/audio2ft/audio2ft.py` & `eegsynth-0.7.2/module/audio2ft/audio2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/audiomixer/__init__.py` & `eegsynth-0.7.2/module/audiomixer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/audiomixer/audiomixer.py` & `eegsynth-0.7.2/module/audiomixer/audiomixer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/bitalino2ft/__init__.py` & `eegsynth-0.7.2/module/bitalino2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/bitalino2ft/bitalino2ft.py` & `eegsynth-0.7.2/module/bitalino2ft/bitalino2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/brainflow2ft/__init__.py` & `eegsynth-0.7.2/module/brainflow2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/brainflow2ft/brainflow2ft.py` & `eegsynth-0.7.2/module/brainflow2ft/brainflow2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/buffer/__init__.py` & `eegsynth-0.7.2/module/buffer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/buffer/buffer.py` & `eegsynth-0.7.2/module/buffer/buffer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/clockdivider/__init__.py` & `eegsynth-0.7.2/module/clockdivider/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/clockdivider/clockdivider.py` & `eegsynth-0.7.2/module/clockdivider/clockdivider.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/clockmultiplier/__init__.py` & `eegsynth-0.7.2/module/clockmultiplier/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/clockmultiplier/clockmultiplier.py` & `eegsynth-0.7.2/module/clockmultiplier/clockmultiplier.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/cogito/__init__.py` & `eegsynth-0.7.2/module/cogito/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/cogito/cogito.py` & `eegsynth-0.7.2/module/cogito/cogito.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/cogito/gtec2wav.py` & `eegsynth-0.7.2/module/cogito/gtec2wav.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/complexity/__init__.py` & `eegsynth-0.7.2/module/complexity/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/complexity/complexity.py` & `eegsynth-0.7.2/module/complexity/complexity.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/compressor/__init__.py` & `eegsynth-0.7.2/module/compressor/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/compressor/compressor.py` & `eegsynth-0.7.2/module/compressor/compressor.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/csp/__init__.py` & `eegsynth-0.7.2/module/csp/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/csp/csp.py` & `eegsynth-0.7.2/module/csp/csp.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/delaytrigger/__init__.py` & `eegsynth-0.7.2/module/delaytrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/delaytrigger/delaytrigger.py` & `eegsynth-0.7.2/module/delaytrigger/delaytrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/demodulatetone/__init__.py` & `eegsynth-0.7.2/module/demodulatetone/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/demodulatetone/demodulatetone.py` & `eegsynth-0.7.2/module/demodulatetone/demodulatetone.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/endorphines/__init__.py` & `eegsynth-0.7.2/module/endorphines/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/endorphines/endorphines.py` & `eegsynth-0.7.2/module/endorphines/endorphines.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/example/__init__.py` & `eegsynth-0.7.2/module/example/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/example/example.py` & `eegsynth-0.7.2/module/example/example.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generateclock/__init__.py` & `eegsynth-0.7.2/module/generateclock/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generateclock/generateclock.py` & `eegsynth-0.7.2/module/generateclock/generateclock.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatecontrol/__init__.py` & `eegsynth-0.7.2/module/generatecontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatecontrol/generatecontrol.py` & `eegsynth-0.7.2/module/generatecontrol/generatecontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatesignal/__init__.py` & `eegsynth-0.7.2/module/generatesignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatesignal/generatesignal.py` & `eegsynth-0.7.2/module/generatesignal/generatesignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatetrigger/__init__.py` & `eegsynth-0.7.2/module/generatetrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/generatetrigger/generatetrigger.py` & `eegsynth-0.7.2/module/generatetrigger/generatetrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/geomixer/__init__.py` & `eegsynth-0.7.2/module/geomixer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/geomixer/geomixer.py` & `eegsynth-0.7.2/module/geomixer/geomixer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/heartrate/__init__.py` & `eegsynth-0.7.2/module/heartrate/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/heartrate/heartrate.py` & `eegsynth-0.7.2/module/heartrate/heartrate.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/historycontrol/__init__.py` & `eegsynth-0.7.2/module/historycontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/historycontrol/historycontrol.py` & `eegsynth-0.7.2/module/historycontrol/historycontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/historysignal/__init__.py` & `eegsynth-0.7.2/module/historysignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/historysignal/historysignal.py` & `eegsynth-0.7.2/module/historysignal/historysignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputcontrol/inputcontrol.py` & `eegsynth-0.7.2/module/inputcontrol/inputcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputlsl/__init__.py` & `eegsynth-0.7.2/module/inputlsl/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputlsl/inputlsl.py` & `eegsynth-0.7.2/module/inputlsl/inputlsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputmidi/__init__.py` & `eegsynth-0.7.2/module/inputmidi/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputmidi/inputmidi.py` & `eegsynth-0.7.2/module/inputmidi/inputmidi.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputmqtt/__init__.py` & `eegsynth-0.7.2/module/inputmqtt/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputmqtt/inputmqtt.py` & `eegsynth-0.7.2/module/inputmqtt/inputmqtt.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputosc/__init__.py` & `eegsynth-0.7.2/module/inputosc/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputosc/inputosc.py` & `eegsynth-0.7.2/module/inputosc/inputosc.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputzeromq/__init__.py` & `eegsynth-0.7.2/module/inputzeromq/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/inputzeromq/inputzeromq.py` & `eegsynth-0.7.2/module/inputzeromq/inputzeromq.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/keyboard/__init__.py` & `eegsynth-0.7.2/module/keyboard/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/keyboard/keyboard.py` & `eegsynth-0.7.2/module/keyboard/keyboard.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/launchcontrol/__init__.py` & `eegsynth-0.7.2/module/launchcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/launchcontrol/launchcontrol.py` & `eegsynth-0.7.2/module/launchcontrol/launchcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/launchpad/__init__.py` & `eegsynth-0.7.2/module/launchpad/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/launchpad/launchpad.py` & `eegsynth-0.7.2/module/launchpad/launchpad.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/logging/logging.py` & `eegsynth-0.7.2/module/logging/logging.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/lsl2ft/__init__.py` & `eegsynth-0.7.2/module/lsl2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/lsl2ft/lsl2ft.py` & `eegsynth-0.7.2/module/lsl2ft/lsl2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/modulatetone/__init__.py` & `eegsynth-0.7.2/module/modulatetone/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/modulatetone/modulatetone.py` & `eegsynth-0.7.2/module/modulatetone/modulatetone.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputartnet/__init__.py` & `eegsynth-0.7.2/module/outputartnet/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputartnet/outputartnet.py` & `eegsynth-0.7.2/module/outputartnet/outputartnet.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputaudio/__init__.py` & `eegsynth-0.7.2/module/outputaudio/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputaudio/outputaudio.py` & `eegsynth-0.7.2/module/outputaudio/outputaudio.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputcvgate/__init__.py` & `eegsynth-0.7.2/module/outputcvgate/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputcvgate/outputcvgate.py` & `eegsynth-0.7.2/module/outputcvgate/outputcvgate.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputdmx/__init__.py` & `eegsynth-0.7.2/module/outputdmx/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputdmx/outputdmx.py` & `eegsynth-0.7.2/module/outputdmx/outputdmx.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputgpio/__init__.py` & `eegsynth-0.7.2/module/outputgpio/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputgpio/outputgpio.py` & `eegsynth-0.7.2/module/outputgpio/outputgpio.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputlsl/__init__.py` & `eegsynth-0.7.2/module/outputlsl/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputlsl/outputlsl.py` & `eegsynth-0.7.2/module/outputlsl/outputlsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputmidi/__init__.py` & `eegsynth-0.7.2/module/outputmidi/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputmidi/outputmidi.py` & `eegsynth-0.7.2/module/outputmidi/outputmidi.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputmqtt/__init__.py` & `eegsynth-0.7.2/module/outputmqtt/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputmqtt/outputmqtt.py` & `eegsynth-0.7.2/module/outputmqtt/outputmqtt.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputosc/__init__.py` & `eegsynth-0.7.2/module/outputosc/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputosc/outputosc.py` & `eegsynth-0.7.2/module/outputosc/outputosc.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputzeromq/__init__.py` & `eegsynth-0.7.2/module/outputzeromq/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/outputzeromq/outputzeromq.py` & `eegsynth-0.7.2/module/outputzeromq/outputzeromq.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/pepipiaf/__init__.py` & `eegsynth-0.7.2/module/pepipiaf/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/pepipiaf/pepipiaf.py` & `eegsynth-0.7.2/module/pepipiaf/pepipiaf.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/playbackcontrol/__init__.py` & `eegsynth-0.7.2/module/playbackcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/playbackcontrol/playbackcontrol.py` & `eegsynth-0.7.2/module/playbackcontrol/playbackcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/playbacksignal/__init__.py` & `eegsynth-0.7.2/module/playbacksignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/playbacksignal/playbacksignal.py` & `eegsynth-0.7.2/module/playbacksignal/playbacksignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plotcontrol/plotcontrol.py` & `eegsynth-0.7.2/module/plotcontrol/plotcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plotimage/plotimage.py` & `eegsynth-0.7.2/module/plotimage/plotimage.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plotsignal/plotsignal.py` & `eegsynth-0.7.2/module/plotsignal/plotsignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plotspectral/plotspectral.py` & `eegsynth-0.7.2/module/plotspectral/plotspectral.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plottext/plottext.py` & `eegsynth-0.7.2/module/plottext/plottext.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plottopo/plottopo.py` & `eegsynth-0.7.2/module/plottopo/plottopo.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/plottrigger/plottrigger.py` & `eegsynth-0.7.2/module/plottrigger/plottrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/postprocessing/__init__.py` & `eegsynth-0.7.2/module/postprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/postprocessing/postprocessing.py` & `eegsynth-0.7.2/module/postprocessing/postprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/preprocessing/__init__.py` & `eegsynth-0.7.2/module/preprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/preprocessing/preprocessing.py` & `eegsynth-0.7.2/module/preprocessing/preprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/processtrigger/__init__.py` & `eegsynth-0.7.2/module/processtrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/processtrigger/processtrigger.py` & `eegsynth-0.7.2/module/processtrigger/processtrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/quantizer/__init__.py` & `eegsynth-0.7.2/module/quantizer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/quantizer/quantizer.py` & `eegsynth-0.7.2/module/quantizer/quantizer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordcontrol/__init__.py` & `eegsynth-0.7.2/module/recordcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordcontrol/recordcontrol.py` & `eegsynth-0.7.2/module/recordcontrol/recordcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordsignal/__init__.py` & `eegsynth-0.7.2/module/recordsignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordsignal/recordsignal.py` & `eegsynth-0.7.2/module/recordsignal/recordsignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordtrigger/__init__.py` & `eegsynth-0.7.2/module/recordtrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/recordtrigger/recordtrigger.py` & `eegsynth-0.7.2/module/recordtrigger/recordtrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/redis/__init__.py` & `eegsynth-0.7.2/module/redis/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/redis/redis.py` & `eegsynth-0.7.2/module/redis/redis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/rms/__init__.py` & `eegsynth-0.7.2/module/rms/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/rms/rms.py` & `eegsynth-0.7.2/module/rms/rms.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sampler/__init__.py` & `eegsynth-0.7.2/module/sampler/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sampler/sampler.py` & `eegsynth-0.7.2/module/sampler/sampler.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sequencer/__init__.py` & `eegsynth-0.7.2/module/sequencer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sequencer/sequencer.py` & `eegsynth-0.7.2/module/sequencer/sequencer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/slewlimiter/__init__.py` & `eegsynth-0.7.2/module/slewlimiter/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/slewlimiter/slewlimiter.py` & `eegsynth-0.7.2/module/slewlimiter/slewlimiter.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sonification/__init__.py` & `eegsynth-0.7.2/module/sonification/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/sonification/sonification.py` & `eegsynth-0.7.2/module/sonification/sonification.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/spectral/__init__.py` & `eegsynth-0.7.2/module/spectral/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/spectral/spectral.py` & `eegsynth-0.7.2/module/spectral/spectral.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/synthesizer/__init__.py` & `eegsynth-0.7.2/module/synthesizer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/synthesizer/synthesizer.py` & `eegsynth-0.7.2/module/synthesizer/synthesizer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/threshold/__init__.py` & `eegsynth-0.7.2/module/threshold/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/threshold/threshold.py` & `eegsynth-0.7.2/module/threshold/threshold.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/unicorn2ft/__init__.py` & `eegsynth-0.7.2/module/unicorn2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/unicorn2ft/unicorn2ft.py` & `eegsynth-0.7.2/module/unicorn2ft/unicorn2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/videoprocessing/__init__.py` & `eegsynth-0.7.2/module/videoprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/videoprocessing/videoprocessing.py` & `eegsynth-0.7.2/module/videoprocessing/videoprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcabass/__init__.py` & `eegsynth-0.7.2/module/volcabass/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcabass/volcabass.py` & `eegsynth-0.7.2/module/volcabass/volcabass.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcabeats/__init__.py` & `eegsynth-0.7.2/module/volcabeats/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcabeats/volcabeats.py` & `eegsynth-0.7.2/module/volcabeats/volcabeats.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcakeys/__init__.py` & `eegsynth-0.7.2/module/volcakeys/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/volcakeys/volcakeys.py` & `eegsynth-0.7.2/module/volcakeys/volcakeys.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/module/vumeter/vumeter.py` & `eegsynth-0.7.2/module/vumeter/vumeter.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.1/setup.py` & `eegsynth-0.7.2/setup.py`

 * *Files identical despite different names*

