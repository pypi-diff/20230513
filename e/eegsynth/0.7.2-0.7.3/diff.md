# Comparing `tmp/eegsynth-0.7.2.tar.gz` & `tmp/eegsynth-0.7.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eegsynth-0.7.2.tar", last modified: Sat May 13 13:05:59 2023, max compression
+gzip compressed data, was "eegsynth-0.7.3.tar", last modified: Sat May 13 13:09:45 2023, max compression
```

## Comparing `eegsynth-0.7.2.tar` & `eegsynth-0.7.3.tar`

### file list

```diff
@@ -1,268 +1,268 @@
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.393834 eegsynth-0.7.2/
--rw-r--r--   0 roboos     (503) staff       (20)    32472 2023-03-21 19:58:52.000000 eegsynth-0.7.2/LICENSE
--rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:05:59.393522 eegsynth-0.7.2/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     2698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/README.md
--rwxr-xr-x   0 roboos     (503) staff       (20)    16538 2023-05-13 13:04:47.000000 eegsynth-0.7.2/eegsynth-gui.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.233022 eegsynth-0.7.2/eegsynth.egg-info/
--rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/PKG-INFO
--rw-r--r--   0 roboos     (503) staff       (20)     5482 2023-05-13 13:05:59.000000 eegsynth-0.7.2/eegsynth.egg-info/SOURCES.txt
--rw-r--r--   0 roboos     (503) staff       (20)        1 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/dependency_links.txt
--rw-r--r--   0 roboos     (503) staff       (20)       53 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/entry_points.txt
--rw-r--r--   0 roboos     (503) staff       (20)      296 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/requires.txt
--rw-r--r--   0 roboos     (503) staff       (20)        9 2023-05-13 13:05:58.000000 eegsynth-0.7.2/eegsynth.egg-info/top_level.txt
--rwxr-xr-x   0 roboos     (503) staff       (20)    13455 2023-05-13 13:03:24.000000 eegsynth-0.7.2/eegsynth.py
--rw-r--r--   0 roboos     (503) staff       (20)     1388 2023-05-04 12:16:58.000000 eegsynth-0.7.2/hook-pylsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.240373 eegsynth-0.7.2/lib/
--rw-r--r--   0 roboos     (503) staff       (20)     1656 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/ArtNet.py
--rw-r--r--   0 roboos     (503) staff       (20)     1450 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/DummyRedis.py
--rw-r--r--   0 roboos     (503) staff       (20)    17162 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/EDF.py
--rw-r--r--   0 roboos     (503) staff       (20)    35670 2023-05-02 20:55:48.000000 eegsynth-0.7.2/lib/EEGsynth.py
--rw-r--r--   0 roboos     (503) staff       (20)     1975 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FakeRedis.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    27618 2023-04-30 19:35:59.000000 eegsynth-0.7.2/lib/FieldTrip.py
--rw-r--r--   0 roboos     (503) staff       (20)      435 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FieldTrip_test_client.py
--rw-r--r--   0 roboos     (503) staff       (20)      301 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/FieldTrip_test_server.py
--rw-r--r--   0 roboos     (503) staff       (20)     1131 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/Redis_test_client.py
--rw-r--r--   0 roboos     (503) staff       (20)     2193 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/RingBuffer.py
--rw-r--r--   0 roboos     (503) staff       (20)     7184 2023-05-02 18:05:03.000000 eegsynth-0.7.2/lib/ZmqRedis.py
--rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/__init__.py
--rw-r--r--   0 roboos     (503) staff       (20)    59022 2023-03-21 19:58:52.000000 eegsynth-0.7.2/lib/colormap.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.241599 eegsynth-0.7.2/module/
--rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/__init__.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.242744 eegsynth-0.7.2/module/accelerometer/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/accelerometer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5707 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/accelerometer/accelerometer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.244205 eegsynth-0.7.2/module/audio2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/audio2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6708 2023-04-29 08:49:58.000000 eegsynth-0.7.2/module/audio2ft/audio2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.245873 eegsynth-0.7.2/module/audiomixer/
--rwxr-xr-x   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/audiomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7220 2023-04-29 09:10:40.000000 eegsynth-0.7.2/module/audiomixer/audiomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.247534 eegsynth-0.7.2/module/bitalino2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/bitalino2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6396 2023-04-29 09:15:26.000000 eegsynth-0.7.2/module/bitalino2ft/bitalino2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.248989 eegsynth-0.7.2/module/brainflow2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/brainflow2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6322 2023-04-29 08:15:56.000000 eegsynth-0.7.2/module/brainflow2ft/brainflow2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.250591 eegsynth-0.7.2/module/buffer/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/buffer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     3468 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/buffer/buffer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.252394 eegsynth-0.7.2/module/clockdivider/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/clockdivider/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5433 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/clockdivider/clockdivider.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.254085 eegsynth-0.7.2/module/clockmultiplier/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/clockmultiplier/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7267 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/clockmultiplier/clockmultiplier.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.257167 eegsynth-0.7.2/module/cogito/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/cogito/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12302 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/cogito/cogito.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/cogito/gtec2wav.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.259064 eegsynth-0.7.2/module/complexity/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/complexity/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8635 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/complexity/complexity.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.260953 eegsynth-0.7.2/module/compressor/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/compressor/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5131 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/compressor/compressor.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.263056 eegsynth-0.7.2/module/csp/
--rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/csp/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12865 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/csp/csp.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.264906 eegsynth-0.7.2/module/delaytrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/delaytrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5784 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/delaytrigger/delaytrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.266834 eegsynth-0.7.2/module/demodulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/demodulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9517 2023-04-29 09:15:47.000000 eegsynth-0.7.2/module/demodulatetone/demodulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.268670 eegsynth-0.7.2/module/endorphines/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/endorphines/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9952 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/endorphines/endorphines.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.273639 eegsynth-0.7.2/module/example/
--rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/example/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4008 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/example/example.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.275848 eegsynth-0.7.2/module/generateclock/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generateclock/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12009 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generateclock/generateclock.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.277526 eegsynth-0.7.2/module/generatecontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatecontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8392 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generatecontrol/generatecontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.279021 eegsynth-0.7.2/module/generatesignal/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatesignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10722 2023-05-02 20:11:22.000000 eegsynth-0.7.2/module/generatesignal/generatesignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.280641 eegsynth-0.7.2/module/generatetrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/generatetrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6763 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/generatetrigger/generatetrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.282114 eegsynth-0.7.2/module/geomixer/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/geomixer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8648 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/geomixer/geomixer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.284002 eegsynth-0.7.2/module/heartrate/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/heartrate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8413 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/heartrate/heartrate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.285870 eegsynth-0.7.2/module/historycontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/historycontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9494 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/historycontrol/historycontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.287827 eegsynth-0.7.2/module/historysignal/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/historysignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9401 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/historysignal/historysignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.289588 eegsynth-0.7.2/module/inputcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    17279 2023-05-10 07:50:04.000000 eegsynth-0.7.2/module/inputcontrol/inputcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.291905 eegsynth-0.7.2/module/inputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6618 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputlsl/inputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.293834 eegsynth-0.7.2/module/inputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5264 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputmidi/inputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.295414 eegsynth-0.7.2/module/inputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5957 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputmqtt/inputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.296812 eegsynth-0.7.2/module/inputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputosc/inputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.298192 eegsynth-0.7.2/module/inputzeromq/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/inputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     5740 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/inputzeromq/inputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.299759 eegsynth-0.7.2/module/keyboard/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/keyboard/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14634 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/keyboard/keyboard.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.301272 eegsynth-0.7.2/module/launchcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/launchcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13953 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/launchcontrol/launchcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.302973 eegsynth-0.7.2/module/launchpad/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/launchpad/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14601 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/launchpad/launchpad.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.304802 eegsynth-0.7.2/module/logging/
--rw-r--r--   0 roboos     (503) staff       (20)      422 2023-04-30 07:48:46.000000 eegsynth-0.7.2/module/logging/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7275 2023-04-30 20:43:41.000000 eegsynth-0.7.2/module/logging/logging.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.306819 eegsynth-0.7.2/module/lsl2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/lsl2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6768 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/lsl2ft/lsl2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.308636 eegsynth-0.7.2/module/modulatetone/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/modulatetone/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10550 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/modulatetone/modulatetone.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.310957 eegsynth-0.7.2/module/outputartnet/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputartnet/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6639 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputartnet/outputartnet.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.313783 eegsynth-0.7.2/module/outputaudio/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputaudio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    12350 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputaudio/outputaudio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.317949 eegsynth-0.7.2/module/outputcvgate/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputcvgate/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10263 2023-05-07 13:53:03.000000 eegsynth-0.7.2/module/outputcvgate/outputcvgate.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.320309 eegsynth-0.7.2/module/outputdmx/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputdmx/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6984 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputdmx/outputdmx.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.325534 eegsynth-0.7.2/module/outputgpio/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputgpio/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8490 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputgpio/outputgpio.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.327160 eegsynth-0.7.2/module/outputlsl/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputlsl/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7652 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputlsl/outputlsl.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.329570 eegsynth-0.7.2/module/outputmidi/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputmidi/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    13389 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputmidi/outputmidi.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.331851 eegsynth-0.7.2/module/outputmqtt/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputmqtt/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7263 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputmqtt/outputmqtt.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.333841 eegsynth-0.7.2/module/outputosc/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputosc/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7596 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputosc/outputosc.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.335248 eegsynth-0.7.2/module/outputzeromq/
--rwxr-xr-x   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/outputzeromq/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6590 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/outputzeromq/outputzeromq.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.336691 eegsynth-0.7.2/module/pepipiaf/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/pepipiaf/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    25727 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/pepipiaf/pepipiaf.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.338423 eegsynth-0.7.2/module/playbackcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/playbackcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6454 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/playbackcontrol/playbackcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.341223 eegsynth-0.7.2/module/playbacksignal/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/playbacksignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9858 2023-05-02 20:53:32.000000 eegsynth-0.7.2/module/playbacksignal/playbacksignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.343190 eegsynth-0.7.2/module/plotcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7058 2023-04-30 20:43:43.000000 eegsynth-0.7.2/module/plotcontrol/plotcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.345714 eegsynth-0.7.2/module/plotimage/
--rw-r--r--   0 roboos     (503) staff       (20)      424 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotimage/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6780 2023-04-30 20:43:48.000000 eegsynth-0.7.2/module/plotimage/plotimage.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.348123 eegsynth-0.7.2/module/plotsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      425 2023-04-30 19:40:07.000000 eegsynth-0.7.2/module/plotsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11992 2023-04-30 20:43:51.000000 eegsynth-0.7.2/module/plotsignal/plotsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.349884 eegsynth-0.7.2/module/plotspectral/
--rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plotspectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    23337 2023-04-30 20:43:55.000000 eegsynth-0.7.2/module/plotspectral/plotspectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.352448 eegsynth-0.7.2/module/plottext/
--rw-r--r--   0 roboos     (503) staff       (20)      423 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/plottext/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7894 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/plottext/plottext.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.353935 eegsynth-0.7.2/module/plottopo/
--rw-r--r--   0 roboos     (503) staff       (20)      423 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plottopo/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8637 2023-04-30 20:44:05.000000 eegsynth-0.7.2/module/plottopo/plottopo.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.355359 eegsynth-0.7.2/module/plottrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/plottrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8295 2023-04-30 20:44:08.000000 eegsynth-0.7.2/module/plottrigger/plottrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.357301 eegsynth-0.7.2/module/postprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/postprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6740 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/postprocessing/postprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.359448 eegsynth-0.7.2/module/preprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/preprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14798 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/preprocessing/preprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.361154 eegsynth-0.7.2/module/processtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/processtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9670 2023-05-02 19:32:40.000000 eegsynth-0.7.2/module/processtrigger/processtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.364027 eegsynth-0.7.2/module/quantizer/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/quantizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6181 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/quantizer/quantizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.365653 eegsynth-0.7.2/module/recordcontrol/
--rw-r--r--   0 roboos     (503) staff       (20)      701 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordcontrol/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10121 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/recordcontrol/recordcontrol.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.367343 eegsynth-0.7.2/module/recordsignal/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordsignal/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    11451 2023-05-02 20:50:47.000000 eegsynth-0.7.2/module/recordsignal/recordsignal.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.368889 eegsynth-0.7.2/module/recordtrigger/
--rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/recordtrigger/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8005 2023-05-13 08:01:31.000000 eegsynth-0.7.2/module/recordtrigger/recordtrigger.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.370732 eegsynth-0.7.2/module/redis/
--rw-r--r--   0 roboos     (503) staff       (20)      683 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/redis/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     3599 2023-04-30 20:46:28.000000 eegsynth-0.7.2/module/redis/redis.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.372222 eegsynth-0.7.2/module/rms/
--rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/rms/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6500 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/rms/rms.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.373738 eegsynth-0.7.2/module/sampler/
--rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sampler/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    14409 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sampler/sampler.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.375500 eegsynth-0.7.2/module/sequencer/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sequencer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    10356 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sequencer/sequencer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.376913 eegsynth-0.7.2/module/slewlimiter/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/slewlimiter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     4470 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/slewlimiter/slewlimiter.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.378603 eegsynth-0.7.2/module/sonification/
--rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/sonification/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15140 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/sonification/sonification.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.380185 eegsynth-0.7.2/module/spectral/
--rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/spectral/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7528 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/spectral/spectral.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.382029 eegsynth-0.7.2/module/synthesizer/
--rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/synthesizer/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    15026 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/synthesizer/synthesizer.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.383615 eegsynth-0.7.2/module/threshold/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/threshold/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7690 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/threshold/threshold.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.384866 eegsynth-0.7.2/module/unicorn2ft/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/unicorn2ft/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     7588 2023-05-07 13:53:03.000000 eegsynth-0.7.2/module/unicorn2ft/unicorn2ft.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.386197 eegsynth-0.7.2/module/videoprocessing/
--rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-25 11:03:23.000000 eegsynth-0.7.2/module/videoprocessing/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)    17749 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/videoprocessing/videoprocessing.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.388028 eegsynth-0.7.2/module/volcabass/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcabass/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9541 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcabass/volcabass.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.389448 eegsynth-0.7.2/module/volcabeats/
--rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcabeats/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     8370 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcabeats/volcabeats.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.391328 eegsynth-0.7.2/module/volcakeys/
--rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/volcakeys/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     9657 2023-04-30 15:10:12.000000 eegsynth-0.7.2/module/volcakeys/volcakeys.py
-drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:05:59.392674 eegsynth-0.7.2/module/vumeter/
--rw-r--r--   0 roboos     (503) staff       (20)      422 2023-03-21 19:58:52.000000 eegsynth-0.7.2/module/vumeter/__init__.py
--rwxr-xr-x   0 roboos     (503) staff       (20)     6651 2023-04-30 20:44:11.000000 eegsynth-0.7.2/module/vumeter/vumeter.py
--rw-r--r--   0 roboos     (503) staff       (20)       38 2023-05-13 13:05:59.393987 eegsynth-0.7.2/setup.cfg
--rwxr-xr-x   0 roboos     (503) staff       (20)     3551 2023-05-13 09:15:27.000000 eegsynth-0.7.2/setup.py
--rw-r--r--   0 roboos     (503) staff       (20)       20 2023-05-13 13:03:41.000000 eegsynth-0.7.2/version.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.653636 eegsynth-0.7.3/
+-rw-r--r--   0 roboos     (503) staff       (20)    32472 2023-03-21 19:58:52.000000 eegsynth-0.7.3/LICENSE
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:09:45.653277 eegsynth-0.7.3/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     2698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/README.md
+-rwxr-xr-x   0 roboos     (503) staff       (20)    16565 2023-05-13 13:08:50.000000 eegsynth-0.7.3/eegsynth-gui.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.490214 eegsynth-0.7.3/eegsynth.egg-info/
+-rw-r--r--   0 roboos     (503) staff       (20)     4291 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/PKG-INFO
+-rw-r--r--   0 roboos     (503) staff       (20)     5482 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/SOURCES.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        1 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/dependency_links.txt
+-rw-r--r--   0 roboos     (503) staff       (20)       53 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/entry_points.txt
+-rw-r--r--   0 roboos     (503) staff       (20)      296 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/requires.txt
+-rw-r--r--   0 roboos     (503) staff       (20)        9 2023-05-13 13:09:45.000000 eegsynth-0.7.3/eegsynth.egg-info/top_level.txt
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13490 2023-05-13 13:08:42.000000 eegsynth-0.7.3/eegsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1388 2023-05-04 12:16:58.000000 eegsynth-0.7.3/hook-pylsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.499316 eegsynth-0.7.3/lib/
+-rw-r--r--   0 roboos     (503) staff       (20)     1656 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/ArtNet.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1450 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/DummyRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)    17162 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/EDF.py
+-rw-r--r--   0 roboos     (503) staff       (20)    35670 2023-05-02 20:55:48.000000 eegsynth-0.7.3/lib/EEGsynth.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1975 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/FakeRedis.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    27618 2023-04-30 19:35:59.000000 eegsynth-0.7.3/lib/FieldTrip.py
+-rw-r--r--   0 roboos     (503) staff       (20)      435 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/FieldTrip_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)      301 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/FieldTrip_test_server.py
+-rw-r--r--   0 roboos     (503) staff       (20)     1131 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/Redis_test_client.py
+-rw-r--r--   0 roboos     (503) staff       (20)     2193 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/RingBuffer.py
+-rw-r--r--   0 roboos     (503) staff       (20)     7184 2023-05-02 18:05:03.000000 eegsynth-0.7.3/lib/ZmqRedis.py
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/__init__.py
+-rw-r--r--   0 roboos     (503) staff       (20)    59022 2023-03-21 19:58:52.000000 eegsynth-0.7.3/lib/colormap.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.500552 eegsynth-0.7.3/module/
+-rw-r--r--   0 roboos     (503) staff       (20)        0 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/__init__.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.501536 eegsynth-0.7.3/module/accelerometer/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/accelerometer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5707 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/accelerometer/accelerometer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.503633 eegsynth-0.7.3/module/audio2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/audio2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6708 2023-04-29 08:49:58.000000 eegsynth-0.7.3/module/audio2ft/audio2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.505903 eegsynth-0.7.3/module/audiomixer/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/audiomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7220 2023-04-29 09:10:40.000000 eegsynth-0.7.3/module/audiomixer/audiomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.508027 eegsynth-0.7.3/module/bitalino2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/bitalino2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6396 2023-04-29 09:15:26.000000 eegsynth-0.7.3/module/bitalino2ft/bitalino2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.509487 eegsynth-0.7.3/module/brainflow2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/brainflow2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6322 2023-04-29 08:15:56.000000 eegsynth-0.7.3/module/brainflow2ft/brainflow2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.511034 eegsynth-0.7.3/module/buffer/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/buffer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3468 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/buffer/buffer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.512719 eegsynth-0.7.3/module/clockdivider/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/clockdivider/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5433 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/clockdivider/clockdivider.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.514294 eegsynth-0.7.3/module/clockmultiplier/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/clockmultiplier/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7267 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/clockmultiplier/clockmultiplier.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.517113 eegsynth-0.7.3/module/cogito/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/cogito/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12302 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/cogito/cogito.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4202 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/cogito/gtec2wav.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.518912 eegsynth-0.7.3/module/complexity/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/complexity/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8635 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/complexity/complexity.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.520434 eegsynth-0.7.3/module/compressor/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/compressor/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5131 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/compressor/compressor.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.522259 eegsynth-0.7.3/module/csp/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/csp/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12865 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/csp/csp.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.523900 eegsynth-0.7.3/module/delaytrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/delaytrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5784 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/delaytrigger/delaytrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.525643 eegsynth-0.7.3/module/demodulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/demodulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9517 2023-04-29 09:15:47.000000 eegsynth-0.7.3/module/demodulatetone/demodulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.527662 eegsynth-0.7.3/module/endorphines/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/endorphines/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9952 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/endorphines/endorphines.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.529733 eegsynth-0.7.3/module/example/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/example/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4008 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/example/example.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.531810 eegsynth-0.7.3/module/generateclock/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/generateclock/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12009 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/generateclock/generateclock.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.533755 eegsynth-0.7.3/module/generatecontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/generatecontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8392 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/generatecontrol/generatecontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.535895 eegsynth-0.7.3/module/generatesignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/generatesignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10722 2023-05-02 20:11:22.000000 eegsynth-0.7.3/module/generatesignal/generatesignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.538804 eegsynth-0.7.3/module/generatetrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/generatetrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6763 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/generatetrigger/generatetrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.540473 eegsynth-0.7.3/module/geomixer/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/geomixer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8648 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/geomixer/geomixer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.542472 eegsynth-0.7.3/module/heartrate/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/heartrate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8413 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/heartrate/heartrate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.544407 eegsynth-0.7.3/module/historycontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/historycontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9494 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/historycontrol/historycontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.547142 eegsynth-0.7.3/module/historysignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/historysignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9401 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/historysignal/historysignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.549512 eegsynth-0.7.3/module/inputcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17279 2023-05-10 07:50:04.000000 eegsynth-0.7.3/module/inputcontrol/inputcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.552507 eegsynth-0.7.3/module/inputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6618 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/inputlsl/inputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.554493 eegsynth-0.7.3/module/inputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5264 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/inputmidi/inputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.556397 eegsynth-0.7.3/module/inputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5957 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/inputmqtt/inputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.558038 eegsynth-0.7.3/module/inputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8044 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/inputosc/inputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.559863 eegsynth-0.7.3/module/inputzeromq/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/inputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     5740 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/inputzeromq/inputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.561476 eegsynth-0.7.3/module/keyboard/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/keyboard/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14634 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/keyboard/keyboard.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.563966 eegsynth-0.7.3/module/launchcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/launchcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13953 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/launchcontrol/launchcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.565552 eegsynth-0.7.3/module/launchpad/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/launchpad/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14601 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/launchpad/launchpad.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.567883 eegsynth-0.7.3/module/logging/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-04-30 07:48:46.000000 eegsynth-0.7.3/module/logging/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7275 2023-04-30 20:43:41.000000 eegsynth-0.7.3/module/logging/logging.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.570741 eegsynth-0.7.3/module/lsl2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      690 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/lsl2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6768 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/lsl2ft/lsl2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.573328 eegsynth-0.7.3/module/modulatetone/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/modulatetone/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10550 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/modulatetone/modulatetone.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.575478 eegsynth-0.7.3/module/outputartnet/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputartnet/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6639 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputartnet/outputartnet.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.578910 eegsynth-0.7.3/module/outputaudio/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputaudio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    12350 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputaudio/outputaudio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.580663 eegsynth-0.7.3/module/outputcvgate/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputcvgate/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10263 2023-05-07 13:53:03.000000 eegsynth-0.7.3/module/outputcvgate/outputcvgate.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.584130 eegsynth-0.7.3/module/outputdmx/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputdmx/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6984 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputdmx/outputdmx.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.585661 eegsynth-0.7.3/module/outputgpio/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputgpio/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8490 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputgpio/outputgpio.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.587821 eegsynth-0.7.3/module/outputlsl/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputlsl/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7652 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputlsl/outputlsl.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.589466 eegsynth-0.7.3/module/outputmidi/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputmidi/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    13389 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputmidi/outputmidi.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.590839 eegsynth-0.7.3/module/outputmqtt/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputmqtt/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7263 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputmqtt/outputmqtt.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.592136 eegsynth-0.7.3/module/outputosc/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputosc/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7596 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputosc/outputosc.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.593603 eegsynth-0.7.3/module/outputzeromq/
+-rwxr-xr-x   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/outputzeromq/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6590 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/outputzeromq/outputzeromq.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.597427 eegsynth-0.7.3/module/pepipiaf/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/pepipiaf/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    25727 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/pepipiaf/pepipiaf.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.600264 eegsynth-0.7.3/module/playbackcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/playbackcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6454 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/playbackcontrol/playbackcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.601900 eegsynth-0.7.3/module/playbacksignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/playbacksignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9858 2023-05-02 20:53:32.000000 eegsynth-0.7.3/module/playbacksignal/playbacksignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.605177 eegsynth-0.7.3/module/plotcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/plotcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7058 2023-04-30 20:43:43.000000 eegsynth-0.7.3/module/plotcontrol/plotcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.607948 eegsynth-0.7.3/module/plotimage/
+-rw-r--r--   0 roboos     (503) staff       (20)      424 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/plotimage/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6780 2023-04-30 20:43:48.000000 eegsynth-0.7.3/module/plotimage/plotimage.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.609500 eegsynth-0.7.3/module/plotsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      425 2023-04-30 19:40:07.000000 eegsynth-0.7.3/module/plotsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11992 2023-04-30 20:43:51.000000 eegsynth-0.7.3/module/plotsignal/plotsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.611470 eegsynth-0.7.3/module/plotspectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      427 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/plotspectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    23337 2023-04-30 20:43:55.000000 eegsynth-0.7.3/module/plotspectral/plotspectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.613976 eegsynth-0.7.3/module/plottext/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/plottext/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7894 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/plottext/plottext.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.615618 eegsynth-0.7.3/module/plottopo/
+-rw-r--r--   0 roboos     (503) staff       (20)      423 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/plottopo/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8637 2023-04-30 20:44:05.000000 eegsynth-0.7.3/module/plottopo/plottopo.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.617096 eegsynth-0.7.3/module/plottrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      426 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/plottrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8295 2023-04-30 20:44:08.000000 eegsynth-0.7.3/module/plottrigger/plottrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.618687 eegsynth-0.7.3/module/postprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/postprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6740 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/postprocessing/postprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.620006 eegsynth-0.7.3/module/preprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/preprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14798 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/preprocessing/preprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.621940 eegsynth-0.7.3/module/processtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      698 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/processtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9670 2023-05-02 19:32:40.000000 eegsynth-0.7.3/module/processtrigger/processtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.623495 eegsynth-0.7.3/module/quantizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/quantizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6181 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/quantizer/quantizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.624806 eegsynth-0.7.3/module/recordcontrol/
+-rw-r--r--   0 roboos     (503) staff       (20)      701 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/recordcontrol/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10121 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/recordcontrol/recordcontrol.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.626072 eegsynth-0.7.3/module/recordsignal/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/recordsignal/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    11451 2023-05-02 20:50:47.000000 eegsynth-0.7.3/module/recordsignal/recordsignal.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.627781 eegsynth-0.7.3/module/recordtrigger/
+-rw-r--r--   0 roboos     (503) staff       (20)      697 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/recordtrigger/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8005 2023-05-13 08:01:31.000000 eegsynth-0.7.3/module/recordtrigger/recordtrigger.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.629176 eegsynth-0.7.3/module/redis/
+-rw-r--r--   0 roboos     (503) staff       (20)      683 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/redis/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3599 2023-04-30 20:46:28.000000 eegsynth-0.7.3/module/redis/redis.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.630658 eegsynth-0.7.3/module/rms/
+-rw-r--r--   0 roboos     (503) staff       (20)      687 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/rms/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6500 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/rms/rms.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.632140 eegsynth-0.7.3/module/sampler/
+-rw-r--r--   0 roboos     (503) staff       (20)      691 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/sampler/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    14409 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/sampler/sampler.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.634030 eegsynth-0.7.3/module/sequencer/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/sequencer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    10356 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/sequencer/sequencer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.635546 eegsynth-0.7.3/module/slewlimiter/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/slewlimiter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     4470 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/slewlimiter/slewlimiter.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.637151 eegsynth-0.7.3/module/sonification/
+-rw-r--r--   0 roboos     (503) staff       (20)      696 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/sonification/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15140 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/sonification/sonification.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.639131 eegsynth-0.7.3/module/spectral/
+-rw-r--r--   0 roboos     (503) staff       (20)      692 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/spectral/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7528 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/spectral/spectral.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.640726 eegsynth-0.7.3/module/synthesizer/
+-rw-r--r--   0 roboos     (503) staff       (20)      695 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/synthesizer/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    15026 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/synthesizer/synthesizer.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.642125 eegsynth-0.7.3/module/threshold/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/threshold/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7690 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/threshold/threshold.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.643414 eegsynth-0.7.3/module/unicorn2ft/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/unicorn2ft/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     7588 2023-05-07 13:53:03.000000 eegsynth-0.7.3/module/unicorn2ft/unicorn2ft.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.645615 eegsynth-0.7.3/module/videoprocessing/
+-rw-r--r--   0 roboos     (503) staff       (20)      699 2023-03-25 11:03:23.000000 eegsynth-0.7.3/module/videoprocessing/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)    17749 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/videoprocessing/videoprocessing.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.647382 eegsynth-0.7.3/module/volcabass/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/volcabass/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9541 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/volcabass/volcabass.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.648990 eegsynth-0.7.3/module/volcabeats/
+-rw-r--r--   0 roboos     (503) staff       (20)      694 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/volcabeats/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     8370 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/volcabeats/volcabeats.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.650669 eegsynth-0.7.3/module/volcakeys/
+-rw-r--r--   0 roboos     (503) staff       (20)      693 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/volcakeys/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     9657 2023-04-30 15:10:12.000000 eegsynth-0.7.3/module/volcakeys/volcakeys.py
+drwxr-xr-x   0 roboos     (503) staff       (20)        0 2023-05-13 13:09:45.652332 eegsynth-0.7.3/module/vumeter/
+-rw-r--r--   0 roboos     (503) staff       (20)      422 2023-03-21 19:58:52.000000 eegsynth-0.7.3/module/vumeter/__init__.py
+-rwxr-xr-x   0 roboos     (503) staff       (20)     6651 2023-04-30 20:44:11.000000 eegsynth-0.7.3/module/vumeter/vumeter.py
+-rw-r--r--   0 roboos     (503) staff       (20)       38 2023-05-13 13:09:45.653774 eegsynth-0.7.3/setup.cfg
+-rwxr-xr-x   0 roboos     (503) staff       (20)     3551 2023-05-13 09:15:27.000000 eegsynth-0.7.3/setup.py
+-rw-r--r--   0 roboos     (503) staff       (20)       20 2023-05-13 13:08:56.000000 eegsynth-0.7.3/version.py
```

### Comparing `eegsynth-0.7.2/LICENSE` & `eegsynth-0.7.3/LICENSE`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/PKG-INFO` & `eegsynth-0.7.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.7.2
+Version: 0.7.3
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
```

### Comparing `eegsynth-0.7.2/README.md` & `eegsynth-0.7.3/README.md`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/eegsynth-gui.py` & `eegsynth-0.7.3/eegsynth-gui.py`

 * *Files 1% similar despite different names*

```diff
@@ -39,15 +39,15 @@
 sys.path.insert(0, os.path.join(path))
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, 'lib'))
 import EEGsynth
 import FieldTrip
 from version import __version__
 
-from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
+from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
 
 # this will contain a list of modules and processes
 modules = []
 processes = []
 
 # command-line arguments
 args = []
@@ -294,16 +294,17 @@
                 module_to_start = plotspectral
             elif name=='plottext':
                 module_to_start = plottext
             elif name=='plottopo':
                 module_to_start = plottopo
             elif name=='plottrigger':
                 module_to_start = plottrigger
-            elif name=='polarbelt':
-                module_to_start = polarbelt
+# This does not have an __init__.py
+#            elif name=='polarbelt':
+#                module_to_start = polarbelt
             elif name=='postprocessing':
                 module_to_start = postprocessing
             elif name=='preprocessing':
                 module_to_start = preprocessing
             elif name=='processtrigger':
                 module_to_start = processtrigger
             elif name=='quantizer':
```

### Comparing `eegsynth-0.7.2/eegsynth.egg-info/PKG-INFO` & `eegsynth-0.7.3/eegsynth.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eegsynth
-Version: 0.7.2
+Version: 0.7.3
 Summary: Converting real-time EEG into sounds, music and visual effects
 Home-page: http://www.eegsynth.org
 Author: Robert Oostenveld
 Author-email: r.oostenveld@gmail.com
 License: GPLv3
 Project-URL: Documentation, https://github.com/eegsynth/eegsynth/blob/master/doc/README.md
 Project-URL: Source, https://github.com/eegsynth/eegsynth/
```

### Comparing `eegsynth-0.7.2/eegsynth.egg-info/SOURCES.txt` & `eegsynth-0.7.3/eegsynth.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/eegsynth.py` & `eegsynth-0.7.3/eegsynth.py`

 * *Files 1% similar despite different names*

```diff
@@ -42,15 +42,15 @@
 sys.path.insert(0, os.path.join(path))
 # eegsynth/lib contains shared modules
 sys.path.insert(0, os.path.join(path, 'lib'))
 import EEGsynth
 import FieldTrip
 from version import __version__
 
-from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, polarbelt, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
+from module import accelerometer, audio2ft, audiomixer, bitalino2ft, buffer, clockdivider, clockmultiplier, cogito, compressor, csp, delaytrigger, demodulatetone, endorphines, example, generateclock, generatecontrol, generatesignal, generatetrigger, geomixer, heartrate, historycontrol, historysignal, inputcontrol, inputlsl, inputmidi, inputmqtt, inputosc, inputzeromq, keyboard, launchcontrol, launchpad, logging, lsl2ft, modulatetone, outputartnet, outputaudio, outputcvgate, outputdmx, outputlsl, outputmidi, outputmqtt, outputosc, outputzeromq, pepipiaf, playbackcontrol, playbacksignal, plotcontrol, plotimage, plotsignal, plotspectral, plottext, plottopo, plottrigger, postprocessing, preprocessing, processtrigger, redis, quantizer, recordcontrol, recordsignal, recordtrigger, rms, sampler, sequencer, slewlimiter, sonification, spectral, synthesizer, threshold, unicorn2ft, videoprocessing, volcabass, volcabeats, volcakeys, vumeter
 
 # this will contain a list of modules and processes
 modules = []
 processes = []
 
 def _setup():
     global monitor, modules, processes
@@ -224,16 +224,17 @@
             module_to_start = plotspectral
         elif name=='plottext':
             module_to_start = plottext
         elif name=='plottopo':
             module_to_start = plottopo
         elif name=='plottrigger':
             module_to_start = plottrigger
-        elif name=='polarbelt':
-            module_to_start = polarbelt
+# This does not have an __init__.py
+#            elif name=='polarbelt':
+#                module_to_start = polarbelt
         elif name=='postprocessing':
             module_to_start = postprocessing
         elif name=='preprocessing':
             module_to_start = preprocessing
         elif name=='processtrigger':
             module_to_start = processtrigger
         elif name=='quantizer':
```

### Comparing `eegsynth-0.7.2/hook-pylsl.py` & `eegsynth-0.7.3/hook-pylsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/ArtNet.py` & `eegsynth-0.7.3/lib/ArtNet.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/DummyRedis.py` & `eegsynth-0.7.3/lib/DummyRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/EDF.py` & `eegsynth-0.7.3/lib/EDF.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/EEGsynth.py` & `eegsynth-0.7.3/lib/EEGsynth.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/FakeRedis.py` & `eegsynth-0.7.3/lib/FakeRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/FieldTrip.py` & `eegsynth-0.7.3/lib/FieldTrip.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/Redis_test_client.py` & `eegsynth-0.7.3/lib/Redis_test_client.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/RingBuffer.py` & `eegsynth-0.7.3/lib/RingBuffer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/ZmqRedis.py` & `eegsynth-0.7.3/lib/ZmqRedis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/lib/colormap.py` & `eegsynth-0.7.3/lib/colormap.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/accelerometer/__init__.py` & `eegsynth-0.7.3/module/accelerometer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/accelerometer/accelerometer.py` & `eegsynth-0.7.3/module/accelerometer/accelerometer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/audio2ft/__init__.py` & `eegsynth-0.7.3/module/audio2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/audio2ft/audio2ft.py` & `eegsynth-0.7.3/module/audio2ft/audio2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/audiomixer/__init__.py` & `eegsynth-0.7.3/module/audiomixer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/audiomixer/audiomixer.py` & `eegsynth-0.7.3/module/audiomixer/audiomixer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/bitalino2ft/__init__.py` & `eegsynth-0.7.3/module/bitalino2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/bitalino2ft/bitalino2ft.py` & `eegsynth-0.7.3/module/bitalino2ft/bitalino2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/brainflow2ft/__init__.py` & `eegsynth-0.7.3/module/brainflow2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/brainflow2ft/brainflow2ft.py` & `eegsynth-0.7.3/module/brainflow2ft/brainflow2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/buffer/__init__.py` & `eegsynth-0.7.3/module/buffer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/buffer/buffer.py` & `eegsynth-0.7.3/module/buffer/buffer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/clockdivider/__init__.py` & `eegsynth-0.7.3/module/clockdivider/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/clockdivider/clockdivider.py` & `eegsynth-0.7.3/module/clockdivider/clockdivider.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/clockmultiplier/__init__.py` & `eegsynth-0.7.3/module/clockmultiplier/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/clockmultiplier/clockmultiplier.py` & `eegsynth-0.7.3/module/clockmultiplier/clockmultiplier.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/cogito/__init__.py` & `eegsynth-0.7.3/module/cogito/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/cogito/cogito.py` & `eegsynth-0.7.3/module/cogito/cogito.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/cogito/gtec2wav.py` & `eegsynth-0.7.3/module/cogito/gtec2wav.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/complexity/__init__.py` & `eegsynth-0.7.3/module/complexity/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/complexity/complexity.py` & `eegsynth-0.7.3/module/complexity/complexity.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/compressor/__init__.py` & `eegsynth-0.7.3/module/compressor/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/compressor/compressor.py` & `eegsynth-0.7.3/module/compressor/compressor.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/csp/__init__.py` & `eegsynth-0.7.3/module/csp/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/csp/csp.py` & `eegsynth-0.7.3/module/csp/csp.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/delaytrigger/__init__.py` & `eegsynth-0.7.3/module/delaytrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/delaytrigger/delaytrigger.py` & `eegsynth-0.7.3/module/delaytrigger/delaytrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/demodulatetone/__init__.py` & `eegsynth-0.7.3/module/demodulatetone/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/demodulatetone/demodulatetone.py` & `eegsynth-0.7.3/module/demodulatetone/demodulatetone.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/endorphines/__init__.py` & `eegsynth-0.7.3/module/endorphines/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/endorphines/endorphines.py` & `eegsynth-0.7.3/module/endorphines/endorphines.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/example/__init__.py` & `eegsynth-0.7.3/module/example/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/example/example.py` & `eegsynth-0.7.3/module/example/example.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generateclock/__init__.py` & `eegsynth-0.7.3/module/generateclock/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generateclock/generateclock.py` & `eegsynth-0.7.3/module/generateclock/generateclock.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatecontrol/__init__.py` & `eegsynth-0.7.3/module/generatecontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatecontrol/generatecontrol.py` & `eegsynth-0.7.3/module/generatecontrol/generatecontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatesignal/__init__.py` & `eegsynth-0.7.3/module/generatesignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatesignal/generatesignal.py` & `eegsynth-0.7.3/module/generatesignal/generatesignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatetrigger/__init__.py` & `eegsynth-0.7.3/module/generatetrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/generatetrigger/generatetrigger.py` & `eegsynth-0.7.3/module/generatetrigger/generatetrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/geomixer/__init__.py` & `eegsynth-0.7.3/module/geomixer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/geomixer/geomixer.py` & `eegsynth-0.7.3/module/geomixer/geomixer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/heartrate/__init__.py` & `eegsynth-0.7.3/module/heartrate/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/heartrate/heartrate.py` & `eegsynth-0.7.3/module/heartrate/heartrate.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/historycontrol/__init__.py` & `eegsynth-0.7.3/module/historycontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/historycontrol/historycontrol.py` & `eegsynth-0.7.3/module/historycontrol/historycontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/historysignal/__init__.py` & `eegsynth-0.7.3/module/historysignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/historysignal/historysignal.py` & `eegsynth-0.7.3/module/historysignal/historysignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputcontrol/inputcontrol.py` & `eegsynth-0.7.3/module/inputcontrol/inputcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputlsl/__init__.py` & `eegsynth-0.7.3/module/inputlsl/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputlsl/inputlsl.py` & `eegsynth-0.7.3/module/inputlsl/inputlsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputmidi/__init__.py` & `eegsynth-0.7.3/module/inputmidi/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputmidi/inputmidi.py` & `eegsynth-0.7.3/module/inputmidi/inputmidi.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputmqtt/__init__.py` & `eegsynth-0.7.3/module/inputmqtt/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputmqtt/inputmqtt.py` & `eegsynth-0.7.3/module/inputmqtt/inputmqtt.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputosc/__init__.py` & `eegsynth-0.7.3/module/inputosc/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputosc/inputosc.py` & `eegsynth-0.7.3/module/inputosc/inputosc.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputzeromq/__init__.py` & `eegsynth-0.7.3/module/inputzeromq/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/inputzeromq/inputzeromq.py` & `eegsynth-0.7.3/module/inputzeromq/inputzeromq.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/keyboard/__init__.py` & `eegsynth-0.7.3/module/keyboard/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/keyboard/keyboard.py` & `eegsynth-0.7.3/module/keyboard/keyboard.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/launchcontrol/__init__.py` & `eegsynth-0.7.3/module/launchcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/launchcontrol/launchcontrol.py` & `eegsynth-0.7.3/module/launchcontrol/launchcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/launchpad/__init__.py` & `eegsynth-0.7.3/module/launchpad/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/launchpad/launchpad.py` & `eegsynth-0.7.3/module/launchpad/launchpad.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/logging/logging.py` & `eegsynth-0.7.3/module/logging/logging.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/lsl2ft/__init__.py` & `eegsynth-0.7.3/module/lsl2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/lsl2ft/lsl2ft.py` & `eegsynth-0.7.3/module/lsl2ft/lsl2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/modulatetone/__init__.py` & `eegsynth-0.7.3/module/modulatetone/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/modulatetone/modulatetone.py` & `eegsynth-0.7.3/module/modulatetone/modulatetone.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputartnet/__init__.py` & `eegsynth-0.7.3/module/outputartnet/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputartnet/outputartnet.py` & `eegsynth-0.7.3/module/outputartnet/outputartnet.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputaudio/__init__.py` & `eegsynth-0.7.3/module/outputaudio/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputaudio/outputaudio.py` & `eegsynth-0.7.3/module/outputaudio/outputaudio.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputcvgate/__init__.py` & `eegsynth-0.7.3/module/outputcvgate/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputcvgate/outputcvgate.py` & `eegsynth-0.7.3/module/outputcvgate/outputcvgate.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputdmx/__init__.py` & `eegsynth-0.7.3/module/outputdmx/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputdmx/outputdmx.py` & `eegsynth-0.7.3/module/outputdmx/outputdmx.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputgpio/__init__.py` & `eegsynth-0.7.3/module/outputgpio/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputgpio/outputgpio.py` & `eegsynth-0.7.3/module/outputgpio/outputgpio.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputlsl/__init__.py` & `eegsynth-0.7.3/module/outputlsl/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputlsl/outputlsl.py` & `eegsynth-0.7.3/module/outputlsl/outputlsl.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputmidi/__init__.py` & `eegsynth-0.7.3/module/outputmidi/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputmidi/outputmidi.py` & `eegsynth-0.7.3/module/outputmidi/outputmidi.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputmqtt/__init__.py` & `eegsynth-0.7.3/module/outputmqtt/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputmqtt/outputmqtt.py` & `eegsynth-0.7.3/module/outputmqtt/outputmqtt.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputosc/__init__.py` & `eegsynth-0.7.3/module/outputosc/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputosc/outputosc.py` & `eegsynth-0.7.3/module/outputosc/outputosc.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputzeromq/__init__.py` & `eegsynth-0.7.3/module/outputzeromq/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/outputzeromq/outputzeromq.py` & `eegsynth-0.7.3/module/outputzeromq/outputzeromq.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/pepipiaf/__init__.py` & `eegsynth-0.7.3/module/pepipiaf/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/pepipiaf/pepipiaf.py` & `eegsynth-0.7.3/module/pepipiaf/pepipiaf.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/playbackcontrol/__init__.py` & `eegsynth-0.7.3/module/playbackcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/playbackcontrol/playbackcontrol.py` & `eegsynth-0.7.3/module/playbackcontrol/playbackcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/playbacksignal/__init__.py` & `eegsynth-0.7.3/module/playbacksignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/playbacksignal/playbacksignal.py` & `eegsynth-0.7.3/module/playbacksignal/playbacksignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plotcontrol/plotcontrol.py` & `eegsynth-0.7.3/module/plotcontrol/plotcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plotimage/plotimage.py` & `eegsynth-0.7.3/module/plotimage/plotimage.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plotsignal/plotsignal.py` & `eegsynth-0.7.3/module/plotsignal/plotsignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plotspectral/plotspectral.py` & `eegsynth-0.7.3/module/plotspectral/plotspectral.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plottext/plottext.py` & `eegsynth-0.7.3/module/plottext/plottext.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plottopo/plottopo.py` & `eegsynth-0.7.3/module/plottopo/plottopo.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/plottrigger/plottrigger.py` & `eegsynth-0.7.3/module/plottrigger/plottrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/postprocessing/__init__.py` & `eegsynth-0.7.3/module/postprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/postprocessing/postprocessing.py` & `eegsynth-0.7.3/module/postprocessing/postprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/preprocessing/__init__.py` & `eegsynth-0.7.3/module/preprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/preprocessing/preprocessing.py` & `eegsynth-0.7.3/module/preprocessing/preprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/processtrigger/__init__.py` & `eegsynth-0.7.3/module/processtrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/processtrigger/processtrigger.py` & `eegsynth-0.7.3/module/processtrigger/processtrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/quantizer/__init__.py` & `eegsynth-0.7.3/module/quantizer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/quantizer/quantizer.py` & `eegsynth-0.7.3/module/quantizer/quantizer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordcontrol/__init__.py` & `eegsynth-0.7.3/module/recordcontrol/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordcontrol/recordcontrol.py` & `eegsynth-0.7.3/module/recordcontrol/recordcontrol.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordsignal/__init__.py` & `eegsynth-0.7.3/module/recordsignal/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordsignal/recordsignal.py` & `eegsynth-0.7.3/module/recordsignal/recordsignal.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordtrigger/__init__.py` & `eegsynth-0.7.3/module/recordtrigger/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/recordtrigger/recordtrigger.py` & `eegsynth-0.7.3/module/recordtrigger/recordtrigger.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/redis/__init__.py` & `eegsynth-0.7.3/module/redis/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/redis/redis.py` & `eegsynth-0.7.3/module/redis/redis.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/rms/__init__.py` & `eegsynth-0.7.3/module/rms/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/rms/rms.py` & `eegsynth-0.7.3/module/rms/rms.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sampler/__init__.py` & `eegsynth-0.7.3/module/sampler/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sampler/sampler.py` & `eegsynth-0.7.3/module/sampler/sampler.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sequencer/__init__.py` & `eegsynth-0.7.3/module/sequencer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sequencer/sequencer.py` & `eegsynth-0.7.3/module/sequencer/sequencer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/slewlimiter/__init__.py` & `eegsynth-0.7.3/module/slewlimiter/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/slewlimiter/slewlimiter.py` & `eegsynth-0.7.3/module/slewlimiter/slewlimiter.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sonification/__init__.py` & `eegsynth-0.7.3/module/sonification/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/sonification/sonification.py` & `eegsynth-0.7.3/module/sonification/sonification.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/spectral/__init__.py` & `eegsynth-0.7.3/module/spectral/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/spectral/spectral.py` & `eegsynth-0.7.3/module/spectral/spectral.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/synthesizer/__init__.py` & `eegsynth-0.7.3/module/synthesizer/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/synthesizer/synthesizer.py` & `eegsynth-0.7.3/module/synthesizer/synthesizer.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/threshold/__init__.py` & `eegsynth-0.7.3/module/threshold/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/threshold/threshold.py` & `eegsynth-0.7.3/module/threshold/threshold.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/unicorn2ft/__init__.py` & `eegsynth-0.7.3/module/unicorn2ft/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/unicorn2ft/unicorn2ft.py` & `eegsynth-0.7.3/module/unicorn2ft/unicorn2ft.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/videoprocessing/__init__.py` & `eegsynth-0.7.3/module/videoprocessing/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/videoprocessing/videoprocessing.py` & `eegsynth-0.7.3/module/videoprocessing/videoprocessing.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcabass/__init__.py` & `eegsynth-0.7.3/module/volcabass/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcabass/volcabass.py` & `eegsynth-0.7.3/module/volcabass/volcabass.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcabeats/__init__.py` & `eegsynth-0.7.3/module/volcabeats/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcabeats/volcabeats.py` & `eegsynth-0.7.3/module/volcabeats/volcabeats.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcakeys/__init__.py` & `eegsynth-0.7.3/module/volcakeys/__init__.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/volcakeys/volcakeys.py` & `eegsynth-0.7.3/module/volcakeys/volcakeys.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/module/vumeter/vumeter.py` & `eegsynth-0.7.3/module/vumeter/vumeter.py`

 * *Files identical despite different names*

### Comparing `eegsynth-0.7.2/setup.py` & `eegsynth-0.7.3/setup.py`

 * *Files identical despite different names*

